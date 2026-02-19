# controle-materiel

 TP : Explorer les Contrôles Material – Flutter
1.  Objectif :

L’objectif de ce TP est de découvrir et manipuler les principaux composants Material Design proposés par Flutter.

Ce TP permet de comprendre :

- L’utilisation des boutons Material

- Les contrôles interactifs (Switch, Slider)

- La gestion d’état avec StatefulWidget

- L’utilisation des cartes (Card)

- L’intégration d’un FloatingActionButton

2.  Structure de l’application :

L’application utilise :

- MaterialApp avec thème personnalisé

- Scaffold pour la structure

- StatefulWidget pour gérer l’interactivité

Le thème est configuré avec :

ThemeData(

  primarySwatch: Colors.indigo,
  
  useMaterial3: true

)

 3. Composants explorés
    
🔹 1. Boutons Material

Trois types de boutons ont été utilisés :

ElevatedButton

TextButton

OutlinedButton

Ces boutons représentent différents niveaux d’importance dans Material Design.

🔹 2. Contrôles interactifs

✅ SwitchListTile

Permet d’activer ou désactiver une option :

bool _switch = false;


La mise à jour se fait avec :

setState(() {

  _switch = value;
  
});

✅ Slider

Permet de sélectionner une valeur entre 0 et 1 :

double _slider = 0.5;


La valeur est affichée dynamiquement :

Text('Valeur: ${(_slider * 100).round()}')

🔹 3. Card (Carte Material)

Le widget Card est utilisé pour afficher un contenu structuré avec :

- Un titre

- Une description

- Une élévation (elevation: 4)

Les cartes sont utiles pour organiser des informations liées.

🔹 4. FloatingActionButton

Bouton flottant placé en bas à droite :

FloatingActionButton(

  onPressed: () {},
  
  child: Icon(Icons.add),
  
)


Il représente une action principale dans l’application.

4.  Gestion d’état

L’application utilise un StatefulWidget car certains éléments changent dynamiquement :

- La valeur du Switch

- La valeur du Slider

La mise à jour de l’interface est réalisée grâce à :

setState()


Cela permet de reconstruire le widget lorsque l’état change.

🏗️ Hiérarchie simplifiée

MaterialApp

 └── Scaffold
 
      ├── AppBar
      
      ├── Column
      
      │    ├── Boutons
      
      │    ├── Switch
      
      │    ├── Slider
      
      │    ├── Text
      
      │    └── Card
      
      └── FloatingActionButton
      

✅ Résultat obtenu

L’application affiche :

- Plusieurs types de boutons

- Un switch interactif

- Un slider avec valeur dynamique

- Une carte stylisée

- Un bouton flottant

L’utilisateur peut interagir avec les contrôles et voir les changements en temps réel.


 Conclusion :

Ce TP permet de découvrir les principaux composants Material Design et d’introduire la notion de gestion d’état dans Flutter.

Il constitue une étape importante pour développer des interfaces interactives et dynamiques. 
