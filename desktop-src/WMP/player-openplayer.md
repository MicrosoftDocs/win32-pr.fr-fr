---
title: Player. openPlayer, méthode
description: La méthode openPlayer ouvre le lecteur Windows Media à l’aide de l’URL spécifiée. | Player. openPlayer, méthode
ms.assetid: 9ddd63c9-f4a0-490a-8543-51ad0fa74a26
keywords:
- méthode openPlayer lecteur Windows Media
- méthode openPlayer lecteur Windows Media, classe Player
- Classe player lecteur Windows Media, méthode openPlayer
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532220"
---
# <a name="playeropenplayer-method"></a>Player. openPlayer, méthode

La méthode **openPlayer** ouvre le lecteur Windows Media à l’aide de l’URL spécifiée.

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

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette méthode lance le lecteur Windows Media avec l’URL spécifiée définie en tant qu’élément multimédia actuel. Si le joueur a été précédemment fermé en mode apparence, il s’ouvre en utilisant la dernière apparence choisie par l’utilisateur. Dans le cas contraire, le joueur s’ouvre en mode complet.

Si cette méthode est appelée à partir d’un contrôle Windows Media PlayerActiveX incorporé en mode distant, son comportement est identique à celui de *PlayerApplication*. méthode **switchToPlayerApplication** .

**Lecteur Windows Media 10 Mobile :** Cette méthode n’est pas prise en charge.

## <a name="requirements"></a>Configuration requise



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

 

 





