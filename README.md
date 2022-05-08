# Validátor
```bash
<script>
    $.validator.methods.number = function (value, element) {
        return this.optional(element) || /-?(?:\d+|\d{1,3}(?:[\s\.,]\d{3})+)(?:[\.,]\d+)?$/.test(value);
    }
</script>
```

# Kereső  csicsásan: 
```bash
<div class="container d-flex justify-content-center align-items-center mt-5 mb-5">
    <div class="row">
        <div class="col-lg">
            <div class="card shadow">
                <div class="card-body">
                    <h1>Termék keresés</h1>
                    <p>
                        <a asp-action="Create" class="btn btn-primary">Új létrehozása</a>
                    </p>
                    <form asp-action="Index" asp-controller="Raktar" method="get">
                        Megnevezés:
                        <input asp-for="Megnevezes" class="form-control" />

                        Beszállító:
                        <select asp-for="Beszallito" asp-items="Model.BeszallitoLista" class="form-control">
                            <option value="">Összes</option>
                        </select>
                        <button type="submit" class="btn btn-success mt-3">Keresés</button>
                    </form>
                </div>
            </div>
        </div>
    </div>
</div>
```
