# Qu'est-ce que SwiftUI ?

**SwiftUI** est un framework développé par Apple pour créer des interfaces utilisateur (UI) de manière déclarative sur ses différentes plateformes : iOS, macOS, watchOS et tvOS. Lancé en 2019, SwiftUI simplifie le développement d’interfaces en permettant aux développeurs de décrire ce qu’ils veulent voir à l’écran, plutôt que de définir comment y arriver.

## Pourquoi utiliser SwiftUI ?

SwiftUI est apprécié pour plusieurs raisons :

- **Syntaxe déclarative** : Contrairement aux approches impératives traditionnelles, SwiftUI permet de définir l'interface utilisateur en se concentrant sur ce que l’UI doit montrer plutôt que sur les étapes pour y parvenir. Par exemple, `Text("Bonjour, Monde!")` crée un élément texte affichant "Bonjour, Monde!".
  
- **Réactivité en temps réel** : Avec SwiftUI, les interfaces utilisateur sont réactives, ce qui signifie qu’elles s’ajustent automatiquement aux changements d’état de l’application. Grâce aux mécanismes comme `@State` et `@Binding`, les éléments visuels se mettent à jour en temps réel selon les données.

- **Intégration multiplateforme** : SwiftUI fonctionne sur toutes les plateformes Apple avec un code unique ou très peu d’adaptations, rendant le développement d'applications multi-supports plus rapide et simple.

- **Prévisualisation en direct** : SwiftUI s’intègre avec Xcode pour permettre des prévisualisations en temps réel, ce qui améliore le flux de travail en permettant aux développeurs de voir les changements de code instantanément dans l’interface utilisateur.

## Exemple de code SwiftUI

Un exemple d'interface en SwiftUI :

```swift
import SwiftUI

struct ContentView: View {
    @State private var isOn = false

    var body: some View {
        VStack {
            Text("Bonjour, Monde!")
                .font(.title)
                .padding()
            
            Toggle("Activer", isOn: $isOn)
                .padding()
            
            if isOn {
                Text("Le bouton est activé")
            }
        }
    }
}
