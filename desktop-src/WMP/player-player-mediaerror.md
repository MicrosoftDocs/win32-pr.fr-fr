---
title: Événement Player. MediaError
description: L’événement MediaError se produit lorsque l’objet Media a une condition d’erreur.
ms.assetid: b2e0176a-cc52-4f59-8894-440f426a1b6e
keywords:
- Événement MediaError lecteur Windows Media
- Événement MediaError lecteur Windows Media, classe Player
- Classe de lecteur Windows Media Player, événement MediaError
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
ms.openlocfilehash: ec8c22825f4aa720efa85275ce520eb81f082fd9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545555"
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

 

 





