---
description: ICE79 valide les références aux composants et aux fonctionnalités entrées dans les champs de la base de données à l’aide du type de données condition.
ms.assetid: f0a8ceac-084a-4693-b27d-f610eec4702a
title: ICE79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9081297f2bf2f11283380c0f057bd0fbec417975
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113850"
---
# <a name="ice79"></a>ICE79

ICE79 valide les références aux composants et aux fonctionnalités entrées dans les champs de la base de données à l’aide du type de données [condition](condition.md) .

## <a name="result"></a>Résultats

ICE79 publie deux avertissements.



| AVERTISSEMENT ICE79                                                                      | Description                                                      |
|------------------------------------------------------------------------------------|------------------------------------------------------------------|
| La base de données ne contient pas de \_ table de validation. Impossible de vérifier complètement les noms de propriété. | La base de données ne contient pas de [ \_ table de validation](-validation-table.md). |
| Erreur lors de la récupération des valeurs de la colonne \[ 2 \] du tableau \[ 1 \] . Colonne ignorée.         | Erreur lors de la récupération de la valeur.                                          |



 

ICE79 publie deux erreurs.



| Erreur ICE79                                                          | Description                               |
|----------------------------------------------------------------------|-------------------------------------------|
| Composant'% ls’référencé dans la colonne'% s'. ' % s’de la ligne% s n’est pas valide. | Une référence de composant non valide a été trouvée. |
| La fonctionnalité'% ls’est référencée dans la colonne'% s'. ' % s’de la ligne% s n’est pas valide.   | Une référence de fonctionnalité non valide a été trouvée    |



 

## <a name="example"></a>Exemple

ICE79 signale les erreurs suivantes pour l’exemple :

``` syntax
Component 'NoSuchComponent' referenced in column 
'InstallExecuteSequence'.'Condition' of row Custom2 is invalid.
Feature 'NoSuchFeature' referenced in column 
'InstallExecuteSequence'.'Condition' of row Custom1 is invalid.
```

Dans cet exemple, NoSuchComponent est absent de la [table Component](component-table.md) et NoSuchFeature est absent de la [table Feature](feature-table.md).

[Table InstallExecuteSequence](installexecutesequence-table.md) (partielle)



| Action  | Condition                                |
|---------|------------------------------------------|
| CUSTOM1 | TESTACTION = 1046 et &NoSuchFeature>2  |
| CUSTOM2 | TESTACTION = 146 et $NoSuchComponent>2 |



 

Pour corriger ces erreurs, entrez des enregistrements valides pour NoSuchFeature et NoSuchComponent dans les tables des fonctionnalités et des composants.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



