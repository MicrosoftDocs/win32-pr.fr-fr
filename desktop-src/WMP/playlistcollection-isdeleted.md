---
title: PlaylistCollection. isDeleted, méthode
description: La méthode isDeleted récupère une valeur indiquant si la sélection spécifiée se trouve dans le dossier éléments supprimés.
ms.assetid: 5023927a-5d1a-4b61-8122-476947d537c4
keywords:
- isDeleted, méthode Lecteur Windows Media
- isDeleted, méthode Lecteur Windows Media, classe PlaylistCollection
- PlaylistCollection, classe Lecteur Windows Media, méthode isDeleted
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
ms.openlocfilehash: a59f6ad587740911d55ae2837607c651e3f3be875bfb24f8bfa765ba415e9bc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862199"
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

**Lecteur Windows Media 10 Mobile**: cette méthode retourne toujours **false**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0, Lecteur Windows Media version 7,1 ou Lecteur Windows Media pour Windows XP. cette méthode n’est pas prise en charge pour Lecteur Windows Media série 9 ou version ultérieure.<br/> |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl>                                                                                                              |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet PlaylistCollection**](playlistcollection-object.md)
</dt> </dl>

 

 





