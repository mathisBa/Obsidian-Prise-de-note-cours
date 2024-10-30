# Qu'est-ce que UIKit ?

**UIKit** est le framework d'interface utilisateur d'Apple pour iOS, iPadOS et tvOS, permettant aux développeurs de créer et de gérer des interfaces utilisateur de manière impérative. UIKit, introduit en 2008 avec iOS, est un élément fondamental du développement d'applications pour l'écosystème mobile d'Apple, offrant un large éventail de composants UI, de contrôles et de gestions d’interactions utilisateur.

## Pourquoi utiliser UIKit ?

UIKit est largement utilisé pour les raisons suivantes :

- **Contrôle total de l’interface** : UIKit fonctionne avec une approche impérative, donnant aux développeurs un contrôle précis sur chaque élément de l'interface, son comportement et ses transitions.
  
- **Mature et robuste** : Utilisé depuis la première version d'iOS, UIKit est un framework stable, bien documenté et soutenu par une vaste communauté, ce qui en fait un choix sûr pour les projets mobiles.
  
- **Écosystème étendu de composants** : UIKit offre un large éventail de composants visuels prêts à l'emploi (comme `UIButton`, `UILabel`, `UITableView`) ainsi que des outils pour gérer les transitions, la navigation (`UINavigationController`), et les animations, couvrant ainsi la plupart des besoins des développeurs.

- **Contrôle de la compatibilité** : Bien que SwiftUI facilite la compatibilité multiplateforme, UIKit permet aux développeurs de gérer manuellement les adaptations pour les versions iOS spécifiques et d'optimiser les performances.

## Exemple de code UIKit

Un exemple d'interface de base en UIKit :

```swift
import UIKit

class ViewController: UIViewController {
    let label = UILabel()
    let button = UIButton()

    override func viewDidLoad() {
        super.viewDidLoad()

        label.text = "Bonjour, Monde!"
        label.font = UIFont.systemFont(ofSize: 24)
        label.translatesAutoresizingMaskIntoConstraints = false
        view.addSubview(label)
        
        button.setTitle("Appuyez-moi", for: .normal)
        button.setTitleColor(.systemBlue, for: .normal)
        button.translatesAutoresizingMaskIntoConstraints = false
        button.addTarget(self, action: #selector(buttonTapped), for: .touchUpInside)
        view.addSubview(button)

        NSLayoutConstraint.activate([
            label.centerXAnchor.constraint(equalTo: view.centerXAnchor),
            label.centerYAnchor.constraint(equalTo: view.centerYAnchor),
            button.topAnchor.constraint(equalTo: label.bottomAnchor, constant: 20),
            button.centerXAnchor.constraint(equalTo: view.centerXAnchor)
        ])
    }
    
    @objc func buttonTapped() {
        label.text = "Bouton appuyé !"
    }
}
