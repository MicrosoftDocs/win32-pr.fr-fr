---
title: Événement Player. PlaylistChange
description: L’événement PlaylistChange se produit lorsqu’une sélection est modifiée. | Événement Player. PlaylistChange
ms.assetid: 09ab0560-e18d-4ee8-a649-2b2468b40c31
keywords:
- Événement PlaylistChange lecteur Windows Media
- Événement PlaylistChange lecteur Windows Media, classe Player
- Classe de lecteur Windows Media Player, événement PlaylistChange
topic_type:
- apiref
api_name:
- Player.PlaylistChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83d371818e8166b536543246eeecf0090509e62b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542292"
---
# <a name="playerplaylistchange-event"></a>Événement Player. PlaylistChange

L’événement **PlaylistChange** se produit lorsqu’une sélection est modifiée.

## <a name="syntax"></a>Syntaxe


```JScript
Player.PlaylistChange(
  Playlist,
  change
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Playlist* 
</dt> <dd>

Objet **playlist** modifié.

</dd> <dt>

*change* 
</dt> <dd>

**Nombre** (**long**) indiquant le type de modification qui s’est produite dans la sélection. Contient l'une des valeurs suivantes :



| Number | Nom          |
|--------|---------------|
| 0      | Unknown       |
| 1      | Effacer         |
| 2      | InfoChange    |
| 3      | Déplacer          |
| 4      | DELETE        |
| 5      | Insérer        |
| 6      | Ajouter (Append)        |
| 7      | Non pris en charge |
| 8      | NameChange,    |
| 9      | Non pris en charge |
| 10     | Trier          |



 

La constante d’énumération de style C peut être dérivée en préfixant la valeur de nom avec « wmplc ». Par exemple, la constante de l’État Move est **wmplcMove**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Notes

La valeur des paramètres d’événement est spécifiée par le lecteur Windows Media et est accessible ou transmise à une méthode dans un fichier JScript importé à l’aide du nom de paramètre donné. Ce nom de paramètre doit être tapé exactement comme indiqué, y compris la mise en majuscules.

**Lecteur Windows Media 10 Mobile :** Cet événement n’est pas pris en charge.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet Player**](player-object.md)
</dt> </dl>

 

 





