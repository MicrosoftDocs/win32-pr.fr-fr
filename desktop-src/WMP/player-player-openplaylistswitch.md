---
title: Événement Player. OpenPlaylistSwitch
description: L’événement OpenPlaylistSwitch se produit lorsqu’un titre sur un DVD commence à être lu. | Événement Player. OpenPlaylistSwitch
ms.assetid: 97d69716-602f-4522-b743-83f2dbc852a2
keywords:
- Événement OpenPlaylistSwitch lecteur Windows Media
- Événement OpenPlaylistSwitch lecteur Windows Media, classe Player
- Classe de lecteur Windows Media Player, événement OpenPlaylistSwitch
topic_type:
- apiref
api_name:
- Player.OpenPlaylistSwitch
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d35d4568356365cc9276c13ea33f866e937da1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520851"
---
# <a name="playeropenplaylistswitch-event"></a>Événement Player. OpenPlaylistSwitch

L’événement **OpenPlaylistSwitch** se produit lorsqu’un titre sur un DVD commence à être lu.

## <a name="syntax"></a>Syntaxe


```JScript
Player.OpenPlaylistSwitch(
  pItem
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pItem* 
</dt> <dd>

Objet **playlist** représentant le titre.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Notes

La valeur des paramètres d’événement est spécifiée par le lecteur Windows Media et est accessible ou transmise à une méthode dans un fichier JScript importé à l’aide du nom de paramètre donné. Ce nom de paramètre doit être tapé exactement comme indiqué, y compris la mise en majuscules.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media pour Windows XP ou version ultérieure.<br/>                           |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet Player**](player-object.md)
</dt> </dl>

 

 





