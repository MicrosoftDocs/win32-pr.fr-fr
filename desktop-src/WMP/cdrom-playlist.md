---
title: Cdrom. playlist
description: La propriété playlist récupère un objet playlist représentant les pistes sur le CD-ROM actuellement dans le lecteur de CD ou les entrées de titre au niveau de la racine pour le DVD.
ms.assetid: 71c76b6c-1344-4d45-b86b-7e49be44dba8
keywords:
- Lecteur Windows Media cdrom. playlist
topic_type:
- apiref
api_name:
- Cdrom.playlist
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcdb50daa169c6f6eb0690de376abd4433ffe130
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512163"
---
# <a name="cdromplaylist"></a>Cdrom. playlist

La propriété **playlist** récupère un objet **playlist** représentant les pistes sur le CD-ROM actuellement dans le lecteur de CD ou les entrées de titre au niveau de la racine pour le DVD.

``` syntax
player.cdromCollection.item(
        index
        ).playlist
      
```

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est un objet de **sélection** en lecture seule.

## <a name="remarks"></a>Notes

En règle générale, les DVD sont organisés en titres. Chaque titre contient un ou plusieurs chapitres. Chaque DVD étant créé différemment, la façon dont les titres et les chapitres sont utilisés est celle de l’auteur du contenu.

Pour le DVD, cette méthode récupère une sélection qui contient comme premier élément un objet **multimédia** qui représente le support DVD. La lecture de l’élément entraîne la lecture du DVD à partir du début s’il s’agit de la première lecture après l’insertion d’un nouveau DVD, ou la reprise de la lecture si le DVD est le même que le dernier DVD affiché. La définition de cet élément en tant qu’élément actuel pendant la lecture entraîne la lecture du DVD à partir du début.

Les éléments supplémentaires (objets **multimédias** ) de la sélection sont des titres de DVD représentés par des sélections imbriquées. Lorsque vous spécifiez des *contrôles*. **CurrentItem** pour correspondre à l’un de ces éléments de sélection imbriqués, le lecteur Windows Media définit automatiquement la sélection imbriquée en tant que *lecteur*. **currentPlaylist** après le début de la lecture du chapitre. Vous pouvez ensuite utiliser les propriétés, méthodes et événements de l’objet **currentPlaylist** pour travailler avec des chapitres DVD, qui sont également des éléments de sélection.

Pour récupérer la valeur de cette propriété, l’accès en lecture à la bibliothèque est requis. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

**Lecteur Windows Media 10 Mobile :** Cette propriété n’est pas prise en charge.

## <a name="examples"></a>Exemples

L’exemple suivant utilise *cdrom*. **pour remplir un élément de texte** html, nommé myText, avec les titres du CD audio actuellement présent dans le premier lecteur de CD. Utilisez *CdromCollection*. **nombre** pour déterminer le nombre de lecteurs de CD disponibles. L’objet **Player** a été créé avec ID = "Player".


```
// Store the CD playlist object.
var pl = Player.cdromCollection.Item(0).Playlist;

// Iterate through the CD track list.
for(var i = 0; i < pl.count; i++){

   // Print each CD track name.
   myText.value += pl.Item(i).name + "\n"; 
}
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                               |
| Version<br/>                  | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>                      | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet cdrom**](cdrom-object.md)
</dt> <dt>

[**Paramètres. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Paramètres. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





