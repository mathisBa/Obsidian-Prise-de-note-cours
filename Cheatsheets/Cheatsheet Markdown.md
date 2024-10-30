[[Le Markdown|Qu'est ce que le markdown ?]]
## Syntaxe de base

| Élément                | Syntaxe                                       | Rendu                                       |
| ---------------------- | --------------------------------------------- | ------------------------------------------- |
| **Titre**              | `# Titre 1`<br>`## Titre 2`<br>`### Titre 3`  | # Titre 1 <br> ## Titre 2 <br> ### Titre 3  |
| **Gras**               | `**texte en gras**`                           | **texte en gras**                           |
| **Italique**           | `*texte en italique*`                         | *texte en italique*                         |
| **Bloc de citation**   | `> citation`                                  | > citation                                  |
| **Liste ordonnée**     | `1. Premier élément`<br>`2. Deuxième élément` | 1. Premier élément <br> 2. Deuxième élément |
| **Liste non ordonnée** | `- Premier élément`<br>`- Deuxième élément`   | - Premier élément <br> - Deuxième élément   |
| **Code**               | `` `code` ``                                  | `code`                                      |
| **Ligne horizontale**  | `---`                                         | ---                                         |
| **Lien**               | `[titre](https://www.example.com)`            | [titre](https://www.example.com)            |
| **Image**              | `![texte alternatif](image.jpg)`              |              |

---

## Syntaxe étendue

| Élément                      | Syntaxe                                                            | Rendu                                                            |
| ---------------------------- | ------------------------------------------------------------------ | ---------------------------------------------------------------- |
| **Bloc de code clôturé**     | <pre>```<br>{<br> "clé": "valeur"<br>}<br>```</pre>                | ```<br>{<br> "clé": "valeur"<br>}<br>```                         |
| **Note de bas de page**      | `Voici une phrase avec une note.[^1]`<br>`[^1]: Ceci est la note.` | Voici une phrase avec une note.[^1] <br> [^1]: Ceci est la note. |
| **ID de titre personnalisé** | `### Mon Titre {#custom-id}`                                       | ### Mon Titre {#custom-id}                                       |
| **Liste de définitions**     | `terme`<br>`: définition`                                          | terme <br> : définition                                          |
| **Barré**                    | `~~Le monde est plat.~~`                                           | ~~Le monde est plat.~~                                           |
| **Liste de tâches**          | `- [x] Terminé`<br>`- [ ] En attente`                              | - [x] Terminé <br> - [ ] En attente                              |
| **Emoji**                    | `C'est drôle! :joy:`                                               | C'est drôle! :joy:                                               |
| **Surligné**                 | `==mot important==`                                                | ==mot important==                                                |
| **Indice**                   | `H~2~O`                                                            | H~2~O                                                            |
| **Exposant**                 | `X^2^`                                                             | X^2^                                                             |

--- 

