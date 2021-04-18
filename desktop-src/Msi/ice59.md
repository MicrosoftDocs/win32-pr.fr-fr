---
description: ICE59 vérifie que les raccourcis publiés appartiennent à des composants installés par la fonctionnalité cible du raccourci.
ms.assetid: 9cd19137-792d-4fde-92d2-7d96942448d6
title: ICE59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5631b723a158bb371fff3211654a70d694b6cb5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519866"
---
# <a name="ice59"></a>ICE59

ICE59 vérifie que les raccourcis publiés appartiennent à des composants installés par la fonctionnalité cible du raccourci.

Les erreurs signalées par ICE59 entraînent généralement le comportement suivant :

1.  Le raccourci publié lance le Windows Installer pour installer la fonctionnalité indiquée dans la colonne cible.
2.  Toutefois, étant donné que la [table FeatureComponents](featurecomponents-table.md) ne mappe pas la fonctionnalité cible au composant contenant le raccourci, le fichier keyfile du composant (qui est activé par le raccourci) n’est pas installé.
3.  Par conséquent, le raccourci est rompu et n’a rien à faire.

## <a name="result"></a>Résultats

ICE59 publie une erreur si un raccourci publié n’appartient pas aux composants installés par la fonctionnalité cible du raccourci.

## <a name="example"></a>Exemple

ICE59 signale l’erreur suivante pour l’exemple ci-dessous :

``` syntax
The shortcut ShortcutB activates component ComponentB and advertises feature FeatureA, but there is no mapping between FeatureA and ComponentB in the FeatureComponents table.
```

Dans ce cas, ShortcutB publie Feature et, lorsqu’il est activé, démarre le fichier de clé de ComponentB. Pourtant, ComponentB n’est jamais installé par Feature. par conséquent, même après la fin de la phase d’installation à la demande, la cible du raccourci n’existe pas.

Pour corriger cette erreur, ajoutez une ligne à la [table FeatureComponents](featurecomponents-table.md) qui associe Feature et ComponentB.

[Table de raccourcis](shortcut-table.md) (partielle)



| Raccourci  | Cible   | -\_ |
|-----------|----------|-------------|
| ShortcutB | FeatureA | ComponentB  |



 

[Table FeatureComponents](featurecomponents-table.md)



| Fonctionnalité\_ | -\_ |
|-----------|-------------|
| FeatureA  | Composant  |



 

[Table des fonctionnalités](feature-table.md) (partielle)



| Fonctionnalité  | Level |
|----------|-------|
| FeatureA | 10    |



 

[Table des composants](component-table.md) (partielle)



| Composant  | KeyPath |
|------------|---------|
| Composant | Filea   |
| ComponentB | FileB   |



 

[Table de fichiers](file-table.md) (partielle)



| Fichier  | -\_ | Séquence |
|-------|-------------|----------|
| Filea | Composant  | 1        |
| FileB | ComponentB  | 2        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



