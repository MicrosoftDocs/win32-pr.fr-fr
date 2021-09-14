---
title: PLAYLIST. dropDownList
description: L’attribut dropDownList spécifie ou récupère une valeur indiquant les éléments qui apparaissent dans la zone de liste déroulante pour une instance donnée de l’élément de sélection.
ms.assetid: 583041b0-25dc-4015-a3b2-37f3cfdcd496
keywords:
- PLAYLIST. dropDownList Lecteur Windows Media
topic_type:
- apiref
api_name:
- PLAYLIST.dropDownList
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4acf98dec7d50e2a3cd0b53acc07b0b8695f8461
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404164"
---
# <a name="playlistdropdownlist"></a>PLAYLIST. dropDownList

L’attribut **dropDownList** spécifie ou récupère une valeur indiquant les éléments qui apparaissent dans la zone de liste déroulante pour une instance donnée de l’élément de **sélection** .

``` syntax
        elementID.dropDownList
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture contenant l’une des valeurs suivantes.



| Valeur       | Description                                                                                      |
|-------------|--------------------------------------------------------------------------------------------------|
| showAlbums  | Affiche les albums.                                                                                    |
| showAll     | Par défaut. Affiche tous les éléments disponibles, y compris les sélections de CD, les sélections utilisateur et les présélections radio. |
| showCD      | Affiche la sélection de CD.                                                                           |
| showClips   | Affiche tous les clips.                                                                                 |
| showCurrent | Affiche la sélection non enregistrée en cours.                                                             |
| showLibrary | Affiche uniquement les sélections de bibliothèque.                                                                    |
| showRadio   | Affiche les présélections radio.                                                                             |
| showQueries | Affiche les requêtes.                                                                                   |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément PLAYLIST**](playlist-element.md)
</dt> </dl>

 

 





