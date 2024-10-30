Nos recherches sont basées sur une liste de ressources disponible [[Ressources utilisées créer et implémenter une UI sur écosystème Apple|ici]]. Le compte rendu de ces recherches est présenté dans ce document à l'aide d'[[L'application Obsidian|Obsidian md]].

Les **Human Interface Guidelines ** d'Apple fournissent des recommandations essentielles pour créer des interfaces intuitives et cohérentes sur leurs plateformes. Elles mettent l'accent sur :
- Couleurs : Utilisation de palettes adaptées qui respectent les normes de contraste.
- Typographie : Choix de polices standardisées, telles que San Francisco.
- Navigation : Structuration de l'interface avec des éléments familiers aux utilisateurs d’Apple, comme les barres de navigation et les gestes tactiles.
- Interaction : Conception d’éléments interactifs, tels que les boutons et les curseurs, qui réagissent de manière tactile et visuelle, intégrant des retours haptiques sur les appareils compatibles.

## Accessibilité

Apple priorise l’**accessibilité** pour garantir que toutes les applications soient utilisables par un large éventail d'utilisateurs. Les fonctionnalités clés incluent :

- **VoiceOver** : Un lecteur d'écran intégré permettant aux utilisateurs malvoyants d'interagir avec leurs appareils Apple via des gestes tactiles.
- **Tailles de texte adaptatives** : Options pour ajuster la taille et le style du texte dans les applications, en utilisant des paramètres dynamiques pour s'adapter aux préférences de l'utilisateur.
- **Accessibilité tactile **: Ajustements possibles pour la taille et la sensibilité des éléments tactiles, facilitant l'interaction sur les appareils Apple.
- **Descriptions alternatives** : Intégration de descriptions pour les images et éléments non textuels, permettant aux utilisateurs d’accéder aux contenus visuels à travers des lecteurs d'écran.
    

**
## Les technologies
SwiftUI vs UIKit

[[Swift UI]] est une technologie plus récente, introduite en 2019 avec iOS 13, qui adopte une approche de développement basée sur une syntaxe déclarative. Cela permet aux développeurs de créer des interfaces utilisateur de manière plus intuitive et rapide, en se concentrant sur ce que l’interface doit afficher plutôt que sur la manière de le faire.[[Swift UI]] offre également des fonctionnalités avancées comme la gestion des états, des animations fluides et un écosystème de composants réutilisables.

[[UI Kit]] est la technologie historique d’Apple, utilisée depuis le début de l’OS. Elle repose sur un codage impératif, ce qui la rend plus complexe à appréhender, mais aussi beaucoup plus complète et flexible pour des applications nécessitant des interfaces utilisateurs très personnalisées. UIKit est mature et largement adopté, avec une vaste documentation et de nombreux exemples disponibles.
### Compatibilité et Performance
- **Langage** : SwiftUI n’est compatible qu’avec Swift, tandis que UIKit prend également en charge Objective-C, ce qui facilite l’intégration dans des projets existants.
- **Performance** : UIKit est généralement plus performant, notamment pour des projets plus complexes, grâce à son optimisation et à son ancienneté. Il est souvent privilégié pour des personnalisations avancées et pour des projets nécessitant des fonctionnalités spécifiques non encore disponibles dans SwiftUI. De plus, UIKit est idéal pour les applications devant être compatibles avec des versions antérieures d’iOS.
### Intégration
La classe **UIHostingController** permet d’intégrer du code SwiftUI dans un projet UIKit. Cela offre une grande flexibilité aux développeurs qui souhaitent tirer parti des avantages de SwiftUI tout en continuant d’utiliser UIKit pour des parties de leur application.
### Écosystème et Avenir
SwiftUI s’inscrit dans la tendance actuelle de simplification du développement d’applications, favorisant la rapidité et la productivité. Il est conçu pour l'avenir, avec un soutien continu de la part d’Apple. À l’inverse, UIKit, bien qu’il soit plus ancien, reste incontournable pour de nombreuses applications en raison de sa richesse fonctionnelle et de son écosystème établi.
### Conclusion
Le choix entre SwiftUI et UIKit dépend des besoins spécifiques du projet. Pour des applications modernes nécessitant une interface simple et rapide à développer, SwiftUI est souvent le meilleur choix. Pour des projets plus complexes, nécessitant une personnalisation avancée et une compatibilité avec des versions antérieures, UIKit demeure la référence.


## Spécifications liées à l'environnement 3D Apple
Guidelines générales sur l’expérience utilisateur et le design d’interface dans un environnement 3D Apple, de manière à rendre l’expérience la plus agréable et confortable possible.
### Perception de profondeur
Les décisions de conception et leur impact sur le confort visuel des spectateurs. Les indices de profondeur sont importants ; s’ils sont mal réalisés, cela peut exposer le spectateur à une fatigue oculaire. Les informations de profondeur peuvent être données par le flou, la couleur, une taille relative à l’espace, un mouvement doux, l’arrière-plan, la lumière et l’ombre, l’occlusion et la densité de la texture. Plus ces indices visuels sont “faux” (par rapport à notre perception de la réalité), plus cela devient une charge lourde pour les yeux.

Note sur les motifs : pour rendre un motif répétitif plus attrayant, utilisez des parties plus petites du motif, ou cassez le motif avec un autre design. (Cf vidéo)

Note sur la 3D : Les indices de profondeur ne sont pas la seule chose qui compte. Une disparité correcte pour chaque œil est également nécessaire pour éviter des indices visuels conflictuels et un inconfort visuel sévère.

### Paramètres de contenus
La taille et le contraste sont un bon exemple de paramètres qu’on pourrait laisser en accès à l’utilisateur. Ceux-ci sont conçus pour réduire l’effort visuel. Les paramètres doivent être adaptés à chaque expérience visuelle et utilisateur.

Les expériences nécessitant que les yeux se concentrent pendant une période prolongée, comme la lecture, peuvent induire de la fatigue. Pour maximiser le confort, le contenu doit être placé à environ un mètre de l’utilisateur. Permettre à ce dernier d’ajuster la profondeur est une bonne chose.

Mais pour les expériences nécessitant un effort visuel de courte durée (comme une notification) ou les expériences invitant à une interaction directe (appel téléphonique), ils peuvent rester au plus proche de l’utilisateur. Mais des indices visuels tels que la transparence ou le flou restent utiles pour rediriger les yeux.

Les paramètres tels que le contrôle de la taille du texte ou du contenu sont importants : seuls les yeux doivent bouger. Les paramètres doivent permettre à l’utilisateur de se reposer sans bouger son corps ou sa tête.

Luminosité du contenu : passer lentement de l’obscurité à la lumière permet aux yeux de l’utilisateur de s’adapter à la lumière et assure un confort visuel.

### Effort occulaire
Soyez attentif à l’effort des yeux de l’utilisateur et minimisez-le. Garder les yeux vers le bas, ainsi que les mouvements vers la gauche ou la droite, sont plus confortables et demandent moins d’effort musculaire.

Autre chose : la lecture, ou bien le focus dirigé vers des cibles (comme dans un jeu), doivent être placées vers le centre et légèrement en dessous de la ligne de vision. L’expérience est plus confortable de cette manière.

Tout mouvement oculaire inconfortable, s’il est vraiment nécessaire dans notre conception d’expérience, doit être bref et/ou déplacé vers le centre de la ligne de vue.

Concevoir des “break points” naturels pour l’utilisateur est important : l’utilisateur pourrait avoir besoin de faire une pause. L’expérience doit lui permettre de reposer ses yeux lorsqu’il en recent le besoin.
### Mouvement des objets virtuels
La science derrière le mouvement des objets virtuels, et leur interprétation par le cerveau humain, est particulièrement intéressante. Pour expérimenter le monde réel et virtuel, nous utilisons nos yeux pour capturer la lumière, mais nous utilisons aussi notre propre mouvement comme outil de perception. L’oreille interne participe à ces sensations. Si ce que nous voyons ne correspond pas à la sensation de notre oreille interne, nous pouvons ressentir des vertiges et même vomir (comme le fait de lire dans une voiture en mouvement). Un bon design doit permettre au cerveau de comprendre l’expérience comme étant stationnaire, et fournir un sentiment de stabilité.

On peut éviter l’inconfort de l’utilisateur en rendant les objets transparents lorsqu’ils bougent, ce qui évite à l’utilisateur l’impression visuelle de bouger lui-même.
### Contenu collé à l’axe de la tête
De même, il faut éviter d’utiliser des objets 3D “collés” à l’axe du visage. Si une fenêtre collée à cet axe est vraiment nécessaire pour l’expérience, sa taille devra être réduite et visuellement éloignée de l’utilisateur. Un objet stationnaire devrait, au contraire, rester en place dans l’espace 3D, pour que l’utilisateur puisse bouger sa tête et son regard librement vers d’autres choses. Une autre solution citée dans la vidéo serait d’utiliser un mouvement lent et légèrement en retard par rapport à l’axe de la tête.
### Mouvement dans une fenêtre
Le contenu mouvant d’une fenêtre contenue dans l’espace vidéo est aussi important. Si une vidéo, dans une fenêtre stationnaire, est un espace qui bouge par exemple, le cerveau pourrait l’interpréter comme étant un mouvement de l’utilisateur lui-même. Dans ce cas, il pourrait être plus agréable de garder l’horizon de ce paysage en alignement avec l’horizon de l’espace réel. Aussi, le mouvement doit se faire vers le point focus (centre de l’horizon, idéalement en face des yeux), mais aussi rester lent et prédictible. Tout mouvement de rotation trop brusque pourrait donner des nausées à l’utilisateur. L’expérience utilisateur est aussi plus agréable si les objets virtuels que rencontrent le joueur sont petits, et visuellement loin. L’utilisation de textures plus “plates”, moins détaillées et moins contrastées, seraient, dans cet exemple précis, plus agréables étant donné que l’oreille interne ne perçoit pas ce mouvement comme étant celui du corps de l’utilisateur.
### Mouvement oscillants
Par rapport aux animations en elle-même, les oscillations sont à éviter. Ou alors en baisser l’amplitude pour la rendre moins perceptible par l'œil. Des mouvements en douceur sont la meilleure solution dans ce genre d’environnement utilisateur.