---
description: La clause ORDER IN GROUP est utilisée conjointement avec l’instruction GROUP ON, qui retourne des jeux de résultats dans des groupes.
ms.assetid: edfa2037-3360-411d-8a12-cdb9680222f2
title: COMMANDE dans la clause GROUP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83b17981f6368b67852e393d38ef8c4b856601d73014d9bdce40292e7e4a499d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119944649"
---
# <a name="order-in-group-clause"></a>COMMANDE dans la clause GROUP

La clause ORDER IN GROUP est utilisée conjointement avec l’instruction [Group on](-search-sql-group-on-over.md) , qui retourne des jeux de résultats dans des groupes. La clause ORDER IN GROUP vous permet de trier chaque groupe retourné d’une manière différente. Si vous regroupez sur System. genre, par exemple, vous pouvez trier tous les documents en System.Document. LastAuthor, tous les fichiers musicaux par système. Musique. AlbumArtist et tous les courriers électroniques par System. message. FromName.

## <a name="syntax"></a>Syntaxe

Voici la syntaxe de la clause ORDER dans le groupe :


```
GROUP ON <group column and optional ranges>
OVER (SELECT ... FROM SystemIndex
    ORDER 
        IN GROUP '<group name>' BY <column> [<direction>] [,<column> [<direction>]]
        [IN GROUP '<group name>' BY <column> [<direction>] [,<column> [<direction>]] ]
        [BY <column> [<direction>] [,<column> [<direction>]] ])
```



Le spécificateur de nom de groupe est une plage ou une valeur connue de la colonne de groupe, comme spécifié dans l’instruction GROUP ON. Par exemple, les valeurs connues pour System. photo. ISOSpeed incluent « ISO-100 », « ISO-200 », et ainsi de suite. Une plage pour System. photo. DateTaken inclut « 2006-1-1 » et « 2007-1-1 » pour une instruction comme GROUP sur System. ItemDate \[ « 2006-1-1 », « 2007-1-1 » \] .

Le spécificateur de colonne doit être une colonne valide spécifiée dans l’instruction GROUP ON ou SELECT. Vous pouvez inclure plusieurs colonnes, séparées par des virgules. Par exemple, si vous regroupez sur System. photo. ISOSpeed, vous pouvez trier toutes les photos ISO-100, d’abord par System. photo. ShutterSpeed, puis par System. photo. ouverture.

Le spécificateur de direction facultatif peut être ASC pour l’ordre croissant (de faible à élevé) ou DESC pour l’ordre décroissant (de haut en bas). Si vous ne fournissez pas de spécificateur de direction, la valeur par défaut, par ordre croissant, est utilisée. Si vous spécifiez plusieurs colonnes, mais que vous ne spécifiez pas toutes les directions, la direction que vous spécifiez en dernier est appliquée à chaque colonne consécutive jusqu’à ce que vous modifiiez explicitement la direction.

Les plages ou valeurs qui ne sont pas explicitement spécifiées dans une clause ORDER GROUP IN sont triées dans l’ordre croissant en fonction des valeurs de la colonne GROUP ON.

## <a name="examples"></a>Exemples

L’exemple suivant regroupe les résultats par la propriété System. Kind. La requête commanderait le groupe « Program » par le nom de l’application et le groupe « Music » par titre d’album et par numéro de suivi. Le groupe **null** serait classé par le nom de l’élément. Tous les autres groupes seraient triés par date d’élément.


```
GROUP ON System.Kind 
OVER (SELECT System.ItemUrl, System.Music.AlbumTitle, System.Music.TrackNumber, System.ItemName, System.ItemDate, System.Kind FROM SystemIndex
    ORDER 
        IN GROUP 'program' BY System.ApplicationName ASC
        IN GROUP 'music' BY System.Music.AlbumTitle ASC, System.Music.TrackNumber ASC
        IN GROUP NULL BY System.ItemName
        BY System.ItemDate DESC)
```



L’exemple suivant regroupe les résultats par la propriété System. ItemDate, puis trie chaque URL de groupe par élément, type ou nom.


```
GROUP ON System.ItemDate ['2006-1-1', '2007-1-1', '2008-1-1'] 
OVER (SELECT System.ItemUrl, System.ItemName, System.ItemDate System.Kind FROM SystemIndex
    ORDER 
        IN GROUP MINVALUE BY System.ItemUrl ASC
        IN GROUP '2007-1-1' BY System.Kind
        IN GROUP NULL BY System.ItemName)
```



Les résultats de la requête précédente sont retournés dans cinq groupes et triés comme indiqué dans le tableau suivant.



| Groupe    | Description                                               | Trié par                                    |
|----------|-----------------------------------------------------------|----------------------------------------------|
| MINVALUE | Éléments dont la date est antérieure à 2006-1-1                          | Trié par l’URL de l’élément, dans l’ordre croissant |
| 2006-1-1 | Éléments dont la date est le ou après le 2006-1-1 mais avant 2007-1-1 | Trié par date de l’élément, dans l’ordre croissant      |
| 2007-1-1 | Éléments dont la date est le ou après le 2007-1-1 mais avant 2008-1-1 | Trié par valeur de genre, dans l’ordre croissant     |
| 2008-1-1 | Éléments dont la date est le ou après le 2008-1-1                     | Trié par date de l’élément, dans l’ordre croissant      |
| **NULL** | Éléments sans valeur dans la colonne System. ItemDate         | Trié par nom d’élément, dans l’ordre croissant      |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Informations de référence**
</dt> <dt>

[REGROUPER... ... Gestion](-search-sql-group-on-over.md)
</dt> <dt>

[Clause ORDER BY](-search-sql-orderby.md)
</dt> </dl>

 

 



