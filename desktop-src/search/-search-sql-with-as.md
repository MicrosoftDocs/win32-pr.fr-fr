---
description: Les alias de groupes de colonnes permettent d’utiliser des noms plus courts à la place du nom d’une colonne ou d’un groupe de colonnes. Le prédicat facultatif alias de groupe fait partie de la clause WHERE.
ms.assetid: 7782ac24-ea6c-4a97-b1b6-982f276fcefc
title: Prédicat WITH--AS Group alias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29218e11fbffe5f47128eeefba3a7fe847a5b21d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750365"
---
# <a name="with----as-group-alias-predicate"></a>Prédicat WITH--AS Group alias

Les alias de groupes de colonnes permettent d’utiliser des noms plus courts à la place du nom d’une colonne ou d’un groupe de colonnes. Le prédicat facultatif alias de groupe fait partie de la clause WHERE. Sa syntaxe est la suivante :


```
...WHERE[ WITH(<columns>) AS #<alias_name>]
[,WITH(<columns>) AS #<alias_name>]
```



Vous pouvez spécifier plusieurs alias de groupe, en séparant les avec... En tant que prédicats par des virgules.

Quand un alias de groupe est référencé dans un prédicat de clause WHERE, la condition est appliquée à chaque colonne du groupe. Les valeurs logiques résultant de la correspondance de chaque colonne sont combinées à l’aide de l’opérateur logique **or** .

Un alias doit être défini avant de pouvoir être utilisé, et il peut être utilisé uniquement dans la clause WHERE. Le nom d’alias doit être un identificateur régulier précédé d’un signe dièse () requis \# .

Le spécificateur de colonne peut contenir un ou plusieurs spécificateurs de colonne, séparés par des virgules. La liste de colonnes doit être placée entre parenthèses et la pondération peut être assignée à chacune. Chaque colonne a la syntaxe suivante :


```
<column_identifier> [<weight_assignment>]
```



Pour plus d’informations sur la spécification des pondérations de colonnes, consultez [prédicat FREETEXT](-search-sql-freetext.md) et [Contains Predicate](-search-sql-contains.md).

L’identificateur de colonne peut être normal ou délimité.

## <a name="examples"></a>Exemples

Les exemples de clause WHERE suivants montrent quand et comment vous pouvez utiliser le prédicat d’alias de groupe. Le premier exemple montre une clause WHERE plus répétitive qui n’utilise pas l’alias de groupe.


```
...WHERE
    FREETEXT("System.ItemNameDisplay",'"computer software"')
    OR
    FREETEXT("System.Title",'"computer software"')
    OR 
    FREETEXT("System.Keywords",'"computer software"')
```



L’exemple précédent peut être simplifié à l’aide d’un alias de groupe, comme illustré dans l’exemple suivant.


```
...WHERE
    WITH("System.ItemNameDisplay","System.Title","System.Keywords")
    AS #Doc-Descriptions
    FREETEXT(#Doc-Descriptions,'"computer software"')
```



Voici un exemple de pondération positive dans laquelle la propriété **title** reçoit davantage de poids en déterminant le rang relatif.


```
...WHERE
    WITH("System.Title":0.8,*:0.5,
         "System.Keywords")
    AS #Doc-Descriptions
    FREETEXT(#Doc-Descriptions,'"computer software"')
```



Voici un exemple de pondération négative dans laquelle la propriété de **titre** avec un poids de 0 n’est pas prise en compte.


```
...WHERE
    WITH("System.Title":0,*:1.0,
         "System.Keywords")
    AS #Doc-Descriptions
    FREETEXT(#Doc-Descriptions,'"computer software"')
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Informations de référence**
</dt> <dt>

[Prédicat FREETEXT](-search-sql-freetext.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Prédicats de texte intégral](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Prédicats de texte non intégral](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



