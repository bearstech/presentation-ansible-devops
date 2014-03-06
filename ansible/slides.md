
!SLIDE

Ansible
=======

Ansible est un produit neutre et prévisible.

!SLIDE

Inventaire et scenario
----------------------

L'inventaire contient la liste des groupes, des machines à répartir dedans, et des paramètres correspondant à cet inventaire.

L'inventaire peut être statique, ou dynamique (cloud et clusters).

On utilise différents inventaires pour la prod et la préprod.

Le scénario regroupe des taches à effectuer par des groupes de machines.

Le DSL utilisé n'en est pas un, c'est un mélange de YAML et de Jinja2.

La lisibilité des recettes est une priorité, et il est toujours possible de tricher.


Taches
------

Pas de paraphrase de chose que l'on connait déja, la plupart des taches concernent la créattion de fichiers de configurations à partir de gabarits, et de lignes de commandes traditionnels.

Séquentielles
-------------

L'éxécution des taches s'effectue de manière séquentielle, pour limiter les surprises. Ansible ne croit pas à la gestion de dépendances et à la parallélisation.

Les actions sur un ensemble de machines, sont elles, parralélisés, par lots de tailles raisonnables.

Idempotance
-----------

Une action peut être rejoué plusieurs fois.

On demande un résultat, pas la méthode pour y arriver.

Normalement, un scénario peut être rejoué sans risques, mais il est plus sage de les travailler dans une VM.

