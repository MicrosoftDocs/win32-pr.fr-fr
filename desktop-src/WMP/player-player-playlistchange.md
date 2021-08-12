---
title: Événement Player. PlaylistChange
description: L’événement PlaylistChange se produit lorsqu’une sélection est modifiée. | Événement Player. PlaylistChange
ms.assetid: 09ab0560-e18d-4ee8-a649-2b2468b40c31
keywords:
- Lecteur Windows Media d’événements PlaylistChange
- Lecteur Windows Media d’événements PlaylistChange, classe Player
- Lecteur Windows Media de classe Player, événement PlaylistChange
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
ms.openlocfilehash: 3ff4c45449c8de2062aa53ce9bda89c8d634dd30bc1ac8c03f091e8b97e9ce60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118572802"
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

*Sélection* 
</dt> <dd>

Objet **playlist** modifié.

</dd> <dt>

*change* 
</dt> <dd>

**Nombre** (**long**) indiquant le type de modification qui s’est produite dans la sélection. Contient l'une des valeurs suivantes :



| Nombre | Nom          |
|--------|---------------|
| 0      | Unknown       |
| 1      | Effacer         |
| 2      | InfoChange    |
| 3      | Déplacer          |
| 4      | Supprimer        |
| 5      | Insérer        |
| 6      | Ajouter        |
| 7      | Non pris en charge |
| 8      | NameChange,    |
| 9      | Non pris en charge |
| 10     | Trier          |



 

La constante d’énumération de style C peut être dérivée en préfixant la valeur de nom avec « wmplc ». Par exemple, la constante de l’État Move est **wmplcMove**.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Notes

la valeur des paramètres d’événement est spécifiée par Lecteur Windows Media, et est accessible ou passée à une méthode dans un fichier JScript importé à l’aide du nom de paramètre donné. Ce nom de paramètre doit être tapé exactement comme indiqué, y compris la mise en majuscules.

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

 

 





