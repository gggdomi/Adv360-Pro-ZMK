# 2022-11-20 - Gui
- super agréable Colemak DHm. Déjà pu faire tous les niveaux de https://www.colemak.academy/, j'aurai pas cru arriver à retenir toutes les lettres si vite (<10wpm cela dit)
- beaucoup plus confortable sans les supports de tenting avec des palm rests improvisés
- next:
  - continuer à pratiquer les lettres
  - démarrer les layers de nav / symbols
  - penser à faire des backups de la config sur le clavier

# 2022-11-19 - Gui
- il n'y a pas tous les onglets dans vial (notamment QMK Settings pour configurer les options) par rapport à la dernière release (https://get.vial.today/changelog/release-0.6.html)
  - ça semble en lien avec le firmware qui n'active pas toutes les features https://github.com/Bastardkb/bastardkb-qmk/issues/24
    - je sais pas trop à quel point c'est le matériel qui est limitant / si c'est fixable. Commençons sans.
    - related code: https://github.com/Bastardkb/bastardkb-qmk/blob/main/bastardkb_build_releases.py#L109
    - other related issues: https://github.com/Bastardkb/bastardkb-qmk/issues/30 + https://github.com/vial-kb/vial-qmk/issues/260
- pratique:
  - les home row mods s'activent facilement (notamment pour le petit doigt qui est plus lent)
  - il y a un délai bizarre quand on fait maj sur une touche elle même mod tap
  - c'est pas très confortable notamment pour le pouce
- next:
  - continuer à pratiquer les lettres
  - améliorer les autres layers / les touches en plus des lettres
  - trouver une position confortable

# 2022-11-19 - Gui
- relu https://precondition.github.io/home-row-mods avec plus de recul -> looks good avec `IGNORE_MOD_TAP_INTERRUPT` et `TAPPING_FORCE_HOLD`
  - le reste des options semble intéressant mais pas indispensable, sauf peut-être https://precondition.github.io/home-row-mods#combined-mod-taps-on-the-lower-row et éventuellement les thumbs si j'arrive pas à m'en sortir
- cheatsheet modtaps: https://cdn.discordapp.com/attachments/663573863480950808/757162393209012304/modtap.pdf
- la doc de QMK est très longue. La section "Software Features" semble être celle qui nous intéresse, ex: https://docs.qmk.fm/#/tap_hold
- la doc de VIAL est beaucoup plus brève et accessible bien que sûrement très laconique, ex: https://get.vial.today/manual/layers.html
- next: configurer le clavier en [Colemak DH](https://colemakmods.github.io/mod-dh/) avec les homerow mods (et un layer de nav?) et s'entrainer un peu

# 2022-11-17 - Gui
- après réflexion, les limitations de ZMK (notamment sur le hot reload) m'ont déchauffé (d'autant plus que le Advantage360 est un peu grand pour moi)
- j'ai tenté de démarrer avec le tractyl manuform -> avec vial c'est très confortable pour itérer
- il y a quelques astuces sur vial :
  - quand on branche le clavier, l'interface reste vide ("no keyboard detected")
  - récupérer le fichier charybdis-4x6.via.json sur https://github.com/Bastardkb/bastardkb-qmk/releases/
  - "Sideload via JSON..." ce fichier
  - le clavier apparait, on peut le configurer en direct, ça marche
  - note: la config est uniquement stockée sur le clavier -> faire des backups régulièrement
  - il y a de la doc supplémentaire ici pour le setup, mais pas besoin dans l'immédiat : https://github.com/Bastardkb/bastardkb-qmk
- je joue un peu avec le GUI pour tester les différents comportements... c'est top mais je me rends compte qu'il y a pleins d'options et d'abbréviation de tous les côtés - je suis un peu perdu.
- next: lire un peu de doc / tutos sur QMK et VIAL pour savoir ce que je fais

# 2022-11-03 - Gui

- lu precondition & xahlee
- tenter de mieux comprendre le feeling de frappe
  - peut-être pas fait pour un advantage 360Pro? (grand, pouces loin)
  - voire essayer du low profile
  - voire peut-être pas si mal QMK car effectivement sans vial ça semble bien relou d'expérimenter
- next:
  - trouver un keymap ZMK avec home row mods pour tester pour de vrai (sinon via kmonad)
  - sinon peut-être essayer le dactyl manuform?
  - cf plus bas

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
