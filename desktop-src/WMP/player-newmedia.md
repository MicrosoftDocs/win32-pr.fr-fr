---
title: Player. newMedia, méthode
description: La méthode newMedia crée un nouvel objet multimédia.
ms.assetid: fccf1559-bac3-4edf-bd88-da2c72cdec21
keywords:
- Lecteur Windows Media de la méthode newMedia
- méthode newMedia Lecteur Windows Media, classe Player
- Lecteur Windows Media de classe Player, méthode newMedia
topic_type:
- apiref
api_name:
- Player.newMedia
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6e3ad30db7ec43bcc0ee6c1470dc608ccf1625390486d9fcd0fd4bf018affdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118338104"
---
# <a name="playernewmedia-method"></a>Player. newMedia, méthode

La méthode **newMedia** crée un nouvel objet **multimédia** .

## <a name="syntax"></a>Syntaxe


```JScript
retVal = Player.newMedia(
  URL
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*URL* \[ dans\]
</dt> <dd>

**Chaîne** contenant l’URL du fichier multimédia numérique avec lequel créer l’objet **multimédia** .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un objet **multimédia** .

## <a name="remarks"></a>Remarques

Le paramètre *URL* ne doit pas être une chaîne vide ou avoir la valeur null.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet Player**](player-object.md)
</dt> </dl>

 

 





