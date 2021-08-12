---
title: Événement Player. MediaError
description: L’événement MediaError se produit lorsque l’objet Media a une condition d’erreur.
ms.assetid: b2e0176a-cc52-4f59-8894-440f426a1b6e
keywords:
- Lecteur Windows Media d’événements MediaError
- Lecteur Windows Media d’événements MediaError, classe Player
- Lecteur Windows Media de classe Player, événement MediaError
topic_type:
- apiref
api_name:
- Player.MediaError
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb1eb94d245f0b0a91786b2b1a7b677429cc9040d8cbb1372164bf6e7ed209d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118572839"
---
# <a name="playermediaerror-event"></a>Événement Player. MediaError

L’événement **MediaError** se produit lorsque l’objet **Media** a une condition d’erreur.

## <a name="syntax"></a>Syntaxe


```JScript
Player.MediaError(
  pMediaObject
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pMediaObject* 
</dt> <dd>

Objet **multimédia** qui a une condition d’erreur.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Notes

la valeur des paramètres d’événement est spécifiée par Lecteur Windows Media, et est accessible ou passée à une méthode dans un fichier JScript importé à l’aide du nom de paramètre donné. Ce nom de paramètre doit être tapé exactement comme indiqué, y compris la mise en majuscules.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media pour Windows XP ou version ultérieure.<br/>                           |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet Player**](player-object.md)
</dt> </dl>

 

 





