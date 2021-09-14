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
ms.openlocfilehash: aaafb97f836135aa9dd112372b1931c8561cb40b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127292554"
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

## <a name="return-value"></a>Valeur de retour

Cette méthode retourne un objet **multimédia** .

## <a name="remarks"></a>Notes

Le paramètre *URL* ne doit pas être une chaîne vide ou avoir la valeur null.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet Player**](player-object.md)
</dt> </dl>

 

 





