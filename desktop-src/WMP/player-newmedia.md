---
title: Player. newMedia, méthode
description: La méthode newMedia crée un nouvel objet multimédia.
ms.assetid: fccf1559-bac3-4edf-bd88-da2c72cdec21
keywords:
- méthode newMedia lecteur Windows Media
- méthode newMedia lecteur Windows Media, classe Player
- Classe player lecteur Windows Media, méthode newMedia
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
ms.openlocfilehash: aaafb97f836135aa9dd112372b1931c8561cb40b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545646"
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

## <a name="remarks"></a>Notes

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

 

 





