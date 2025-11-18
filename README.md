# Boutique Diayma
#Explorez l’application. Signalez 2 bugs trouvés ?
## Bugs trouvés

### 1. Le changement de langue en espagnol ne fonctionne pas
- Lorsque l’utilisateur choisit “Espagnol”, l’interface reste en français.
- Le sélecteur de langue ne met pas à jour la culture.
- Cause probable : middleware de localisation mal configuré ou fichiers .resx manquants.

### 2. Le stock ne se met pas à jour après une commande
- Lorsqu’une commande est validée, la quantité en stock reste identique.
- Le système enregistre la commande mais ne décrémente pas le stock.
- Cause probable : la logique de mise à jour du stock n’est pas exécutée dans OrderController ou le service du panier.
  
###4) Placez un point d’arrêt sur les lignes suivantes du code :(fait dans vscode)

### 5) les namespaces, classes et méthodes visités avant l’affichage des #produits sur l’écran d’accueil de votre navigateur, en mode "Pas à pas #détaillé" sont :
### 1. Première étape
- L’exécution arrive d’abord dans le constructeur du controller :
- Namespace : P2FixAnAppDotNetCode.Controllers
- Classe : ProductController
- Méthode : ProductController (constructeur)
### 2. Deuxième étape
- Après être passé par le constructeur du ProductController, l’exécution arrive dans la méthode :
- Namespace : P2FixAnAppDotNetCode.Controllers
- Classe : ProductController
- Méthode : Index()
- Cette méthode appelle le service pour récupérer la liste des produits.
### 3. Troisième étape
 - Le controller appelle ensuite le service :
 - Namespace : P2FixAnAppDotNetCode.Models.Services
 - Classe :  ProductService
 - Méthode : GetAllProducts()
 - Le service appelle le repository pour récupérer les données des produits.
### 4. Quatrième étape
 - Le service appelle ensuite le repository pour accéder aux données :
 - Namespace :P2FixAnAppDotNetCode.Models.Repositories
 - Classe : ProductRepository
 - Méthode : GetAllProducts()
 - Cette méthode filtre les produits en stock, les trie par nom, et renvoie la liste au service.
### 5. Dernière étape
 - Une fois les produits récupérés par le repository, le service les renvoie au controller.
 - Le controller exécute return View(products), ce qui envoie les données à la vue Razor.
 - La page d’accueil affiche alors la liste des produits.
