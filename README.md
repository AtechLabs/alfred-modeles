# alfred-modeles

Modèles publics servis à la page de l'orbe d'Alfred (assistant vocal) par GitHub Pages, qui envoie l'en-tête d'accès qu'une page web exige (`Access-Control-Allow-Origin: *`) ; les releases GitHub ne l'envoient pas.

Adresse : `https://atechlabs.github.io/alfred-modeles/vosk-model-small-fr-0.22.tar.gz`

| Fichier | Origine | Licence | Usage |
|---|---|---|---|
| `vosk-model-small-fr-0.22.tar.gz` (42 Mo) | [Vosk / Alpha Cephei](https://alphacephei.com/vosk/models), reconditionné en `.tar.gz` pour `vosk-browser` | Apache-2.0 | reconnaissance du mot d'appel (« Hey Alfred ») dans la page, hors ligne |

Rien d'autre ne vit ici : ni code, ni donnée personnelle.

## vosk-browser 0.0.8, révision alfred1

`vosk-browser-0.0.8-alfred1.js` : le moteur [vosk-browser](https://github.com/ccoreilly/vosk-browser) 0.0.8
(Apache-2.0, © ccoreilly), **modifié** : dans son worker, une adresse de modèle absolue n'est plus résolue contre
`location.href` (dans une page chargée depuis un fichier, cette base vaut « null/… » et le chargement échoue ; fil amont
#82). Reconstruit à l'identique par `tools/patch_vosk_browser.py` du dépôt Alfred, depuis `dist/vosk.js` du paquet npm
(sha256 `29504515526e974f4cb053cf08811c4de5fb2a74007c0a5a957db50eaa8d5d0c`). La licence Apache-2.0 s'applique aussi à ce fichier.
