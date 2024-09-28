# Reconnaissance de Mots par Grammaire

Ce programme implémente un analyseur syntaxique simple qui vérifie si une chaîne de caractères est générée par une grammaire définie. Il fonctionne en analysant les parties d'une chaîne de caractères avec des fonctions représentant des non-terminaux de la grammaire.

## Fonctionnalités
- Accepte une chaîne de caractères et vérifie si elle est générée par la grammaire suivante :
  - `S -> A B C`
  - `A -> ab | a`
  - `B -> bc | ac`
  - `C -> d`
- Si la chaîne respecte cette grammaire, elle est acceptée, sinon elle est rejetée.

## Algorithme
L'analyseur fonctionne avec les non-terminaux suivants :
- `A` : Définit une règle simple avec deux possibilités : `ab` ou `a`.
- `B` : Définit deux alternatives pour la règle : `bc` ou `ac`.
- `C` : Accepte uniquement `d` comme terminal.
  
L'analyse se fait en appelant successivement les fonctions `A()`, `B()`, et `C()` qui vérifient les parties correspondantes du mot.
