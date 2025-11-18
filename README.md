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
  
# 4) Placez un point d’arrêt sur les lignes suivantes du code :
#    a) CartSummaryViewComponent ligne 12
#    b) ProductController ligne 15
#    c) OrderController ligne 17
#    d) CartController ligne 15
#    e) Startup ligne 20
# 5) les namespaces, classes et méthodes visités avant l’affichage des #produits sur l’écran d’accueil de votre navigateur, en mode "Pas à pas #détaillé" sont :
#
#
