---
description: ICE94 vérifie le tableau de raccourcis, la table des fonctionnalités et la table MsiAssembly et publie un avertissement s’il existe des raccourcis non publiés pointant vers un fichier d’assembly dans le Global Assembly Cache.
ms.assetid: 9b1b25b5-b190-47c2-8d43-fa3964e87a6f
title: ICE94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dd203fe35b6bedc7d36f3e5a5c18fc6a235d3e65924b41909803e67ab79337e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894889"
---
# <a name="ice94"></a>ICE94

ICE94 vérifie le tableau de [raccourcis](shortcut-table.md), la table des [fonctionnalités](feature-table.md)et la [table MsiAssembly](msiassembly-table.md) et publie un avertissement s’il existe des raccourcis non publiés pointant vers un fichier d’assembly dans le global assembly cache. Si l’entrée dans le champ cible de la table de raccourcis n’est pas une fonctionnalité de la table de fonctionnalités, le raccourci n’est pas publié. Si l’entrée dans le \_ champ composant du tableau de raccourcis est également indiquée dans la table MsiAssembly, le raccourci pointe vers un fichier d’assembly. Si l’entrée dans le \_ champ application de fichier de la table MsiAssembly est vide, le fichier d’assembly se trouve dans le global assembly cache.

## <a name="result"></a>Résultat

ICE94 publie l’avertissement suivant.



| AVERTISSEMENT ICE94                                                                                | Description                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| Le raccourci' 2 'non publié \[ \] pointe vers un fichier d’assembly dans le global assembly cache. | Un raccourci non publié pointe vers un fichier d’assembly dans le Global Assembly Cache. |



 

## <a name="example"></a>Exemple

ICE94 signale l’erreur suivante pour l’exemple :

``` syntax
The non-advertised shortcut 'shortcut1' points to an assembly file in the global assembly cache.
```

[Table de raccourcis](shortcut-table.md) (partielle)



| Raccourci  | Composant\_ | Cible    |
|-----------|-------------|-----------|
| shortcut1 | c1          | \[file1\] |
| shortcut2 | c2          | Feature1  |
| shortcut3 | c3          | \[fichier2\] |



 

[Table des fonctionnalités](feature-table.md) (partielle)



| Fonctionnalité  |
|----------|
| Feature1 |



 

[Table MsiAssembly](msiassembly-table.md) (partielle)



| Composant\_ | Application de fichier \_ |
|-------------|-------------------|
| c1          |                   |
| c2          |                   |
| c3          | fa1               |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



