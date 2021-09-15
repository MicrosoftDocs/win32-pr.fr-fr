---
title: Player. openPlayer, méthode
description: la méthode openPlayer ouvre Lecteur Windows Media à l’aide de l’URL spécifiée. | Player. openPlayer, méthode
ms.assetid: 9ddd63c9-f4a0-490a-8543-51ad0fa74a26
keywords:
- Lecteur Windows Media de la méthode openPlayer
- méthode openPlayer Lecteur Windows Media, classe Player
- Lecteur Windows Media de classe Player, méthode openPlayer
topic_type:
- apiref
api_name:
- Player.openPlayer
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3378df48f961f1aa5e3fccec72e79b7f1c26ff08
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403997"
---
# <a name="playeropenplayer-method"></a>Player. openPlayer, méthode

la méthode **openPlayer** ouvre Lecteur Windows Media à l’aide de l’URL spécifiée.

## <a name="syntax"></a>Syntaxe


```JScript
Player.openPlayer(
  URL
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*URL* \[ dans\]
</dt> <dd>

**Chaîne** représentant l’URL de l’élément multimédia à lire.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

cette méthode lance Lecteur Windows Media avec l’URL spécifiée définie en tant qu’élément multimédia actuel. Si le joueur a été précédemment fermé en mode apparence, il s’ouvre en utilisant la dernière apparence choisie par l’utilisateur. Dans le cas contraire, le joueur s’ouvre en mode complet.

si cette méthode est appelée à partir d’Windows un contrôle PlayerActiveX Media incorporé en mode distant, son comportement est identique à celui de *PlayerApplication*. méthode **switchToPlayerApplication** .

**Lecteur Windows Media 10 Mobile :** Cette méthode n’est pas prise en charge.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet Player**](player-object.md)
</dt> <dt>

[**PlayerApplication.switchToPlayerApplication**](playerapplication-switchtoplayerapplication.md)
</dt> </dl>

 

 





