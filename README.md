# Boutique Diayma

8. Quels sont les namespaces, classes et méthodes visités avant l’affichage des produits sur l’écran d’accueil de votre navigateur ?
9. 
10. *les namespaces :*
    1. `P2FixAnAppDotNetCode`
    2. `P2FixAnAppDotNetCode.Models.Services `
    3. `P2FixAnAppDotNetCode.Controllers`
    4. `P2FixAnAppDotNetCode.Components`
11. les classes :
    1. Program
    2. startup
    3. ProductRepository
    4. ProductController
    5. ProductService
    6. CartSummaryViewComponent
    7. LanguageSelectorViewComponent
12. les Methodes :
    1. Main
    2. buildwebhost
    3. `ConfigureServices`
    4. configure
    5. index
    6. GetAllProducts

## Mode de pas à pas choisi : Pas à pas principal (F10)

**Pourquoi.** Les points d'arrêt posés dans les constructeurs (`Startup`, `ProductController`, `CartSummaryViewComponent`) arrêtent déjà le débogueur sur les méthodes de l'application. Entre deux arrêts, F10 exécute un appel d'un seul bloc. On suit ainsi le déroulement de l'application (démarrage, contrôleur, vue, composants) sans se perdre dans le code interne 

Le parcours observé au débogueur (pas à pas principal) jusqu'à l'affichage de l'accueil :

```
        public Startup(IConfiguration configuration)
```

```
        public void ConfigureServices(IServiceCollection services)
```

services.Configure<RequestLocalizationOptions></requestlocalizationoptions>(opts =>

```
        public void Configure(IApplicationBuilder app, IHostingEnvironment env)
```

```
        public static IWebHost BuildWebHost(string[] args) =>
```

```
        public static void Main(string[] args)
```

```
        public ProductController(IProductService productService, ILanguageService languageService)
```

```
        public IActionResult Index()
```

```
        public CartSummaryViewComponent(ICart cart)
```

```
        public IViewComponentResult Invoke()
```

```
        public IViewComponentResult Invoke(ILanguageService languageService)
```
