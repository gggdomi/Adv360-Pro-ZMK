# 2022-11-02 - Rémi

- auteurs connus: manna-harbour (miryoku), precondition, xahlee.info
- communautés sur discord (oh key caps, 40% keyboard)
- reddit: https://www.reddit.com/r/ErgoMechKeyboards/ (regarder les tops comments)
- pour choisir son layout, très discrimant
  1. home row mods
  2. combos
- à tester, ça va être cool: symbol layer
- on peut faire pleins de layers, des layers d'application, des layers qui changent en fonction de l'app actuelle avec karabiner
- le plus important c'est d'avoir une feedback loop rapide
  - compliqué avec zmk? -> tester via kmonad pour pouvoir itérer vite
- config rapide sur karabiner: https://github.com/yqrashawn/GokuRakuJoudo
- bon il y a beaucoup de trucs
- next:
  1. lire quelques astuces de pro, regarder des layouts sur https://keymapdb.com/?isSplit=true&firmwares=ZMK
  2. tester les homerow mods sur kmonad
- on hold
  1. continuer à lire la doc (descendre juste toutes les sections dans l'ordre)
  2. partir d'un layout existant
  3. trouver un moyen de flasher plus vite
  4. clarifier le besoin

# 2022-10-31 - Gui

- yay, le clavier est réparé en reflashant avec le trombone
- @globidev found a vscode extension: "ZMK Tools" (notably syntax highlighting)
  - also install "DeviceTree" extension for .dts(i) files
- le format de config est un peu weird au premier abord et pas très lisible, mais finalement ne semble pas si compliqué. Il semble y avoir assez peu de concepts, lire bêtement la doc pour les connaître et après ça doit se comprendre.
- next:
  1. continuer à lire la doc (descendre juste toutes les sections dans l'ordre)
  2. on verra ensuite pour le besoin

# 2022-10-29 - Gui

- j'ai passé ~2h dessus entre hier soir et ce matin -> je pense faire une pause, probablement jusqu'à lundi
- j'ai tenté de flasher au bureau, bonne et mauvaise nouvelle: le gauche success (la touche "a" qu'on avait ajouté fonctionne 🤯), le droit ne marche plus du tout, et je n'arrivais même pas à le remettre en bootloader -> j'amène un trombone au bureau lundi pour le mettre en bootloader mécaniquement + j'ai trouvé un peu de docs de procédures à suivre
- exploration ZMK, TLDR:
  - combos + tap dance + hold-tap looks good
  - update without re-flashing (vial like) = zmk-studio. Few info on the web, most content seem to be on discord, Studio section. Not digged yet. Probablement plusieurs mois/années avant de pouvoir compter dessus.
  - mouse keys = rien trouvé en cherchant superficiellement. Je sais même pas si c'est indispensable pour nos use-cases. Probablement pas sur la roadmap avant un moment, si on a des besoins ce sera probablement à faire via via karabiner
- sur les conseils de @globidev j'ai commencé à setup Vimium -> très cool. Quelques bugs/missing features -> Vimium-C looks better. Je commence à l'utiliser doucement.
- j'ai commencé un fichier [./notes.md](./notes.md) pour synthétiser mes besoins -> illisible pour l'instant mais à compléter petit à petit
- next:
  1. lire un peu sur le language de configuration (niveau **zéro** pour l'instant)
  2. fixer le clavier 😅
  3. continuer à réfléchir en fond et documenter le besoin
