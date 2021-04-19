---
title: PlaylistCollection. isDeleted, méthode
description: La méthode isDeleted récupère une valeur indiquant si la sélection spécifiée se trouve dans le dossier éléments supprimés.
ms.assetid: 5023927a-5d1a-4b61-8122-476947d537c4
keywords:
- isDeleted, méthode Windows Media Player
- isDeleted, méthode lecteur Windows Media, classe PlaylistCollection
- Classe PlaylistCollection lecteur Windows Media, méthode isDeleted
topic_type:
- apiref
api_name:
- PlaylistCollection.isDeleted
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fed3e7e8ff41f23d0f9f741ea99f3382d20532e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545536"
---
# <a name="playlistcollectionisdeleted-method"></a>PlaylistCollection. isDeleted, méthode

La méthode **IsDeleted** récupère une valeur indiquant si la sélection spécifiée se trouve dans le dossier éléments supprimés.

## <a name="syntax"></a>Syntaxe


```JScript
bRetVal = PlaylistCollection.isDeleted(
  playlist
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*sélection* \[ dans\]
</dt> <dd>

Objet de la **sélection** à rechercher.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne une **valeur booléenne**.

**Windows Media Player 10 Mobile**: cette méthode retourne toujours la **valeur false**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0, lecteur Windows Media version 7,1 ou lecteur Windows Media pour Windows XP. Cette méthode n’est pas prise en charge pour le lecteur Windows Media série 9 ou version ultérieure.<br/> |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl>                                                                                                              |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet PlaylistCollection**](playlistcollection-object.md)
</dt> </dl>

 

 





