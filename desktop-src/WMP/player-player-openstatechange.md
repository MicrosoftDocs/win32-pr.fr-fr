---
title: Événement Player. OpenStateChange
description: L’événement OpenStateChange se produit lorsque la propriété openState change de valeur. | Événement Player. OpenStateChange
ms.assetid: b6b840ab-72c7-4150-a259-1e7d8afcec81
keywords:
- Lecteur Windows Media d’événements OpenStateChange
- Lecteur Windows Media d’événements OpenStateChange, classe Player
- Lecteur Windows Media de classe Player, événement OpenStateChange
topic_type:
- apiref
api_name:
- Player.OpenStateChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b65436dee60a5207e09a57a39c32dc479ce110e1dafb07a7dbd7cab86e4f0a92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120003219"
---
# <a name="playeropenstatechange-event"></a>Événement Player. OpenStateChange

L’événement **OpenStateChange** se produit lorsque la propriété **openState** change de valeur.

## <a name="syntax"></a>Syntaxe


```JScript
Player.OpenStateChange(
  NewState
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*NewState* 
</dt> <dd>

**Nombre** (**long**) spécifiant le nouvel état ouvert. Consultez [openState](player-openstate.md) pour obtenir une table de valeurs.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Lecteur Windows Media pouvez parcourir plusieurs états ouverts pendant qu’il tente d’ouvrir un fichier réseau, par exemple en localisant le serveur, en se connectant au serveur et enfin en ouvrant le fichier. Cet événement est déclenché chaque fois que l’état ouvert change.

la valeur des paramètres d’événement est spécifiée par Lecteur Windows Media, et est accessible ou passée à une méthode dans un fichier JScript importé à l’aide du nom de paramètre donné. Ce nom de paramètre doit être tapé exactement comme indiqué, y compris la mise en majuscules.

il n’est pas garanti que les états de Lecteur Windows Media se produisent dans un ordre particulier. En outre, tous les États ne se produisent pas nécessairement au cours d’une séquence d’événements. Vous ne devez pas écrire du code qui s’appuie sur l’ordre de l’État.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet Player**](player-object.md)
</dt> <dt>

[**Player. openState**](player-openstate.md)
</dt> </dl>

 

 





