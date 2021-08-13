---
title: Media. sourceURL
description: La propriété sourceURL récupère l’URL de l’élément multimédia.
ms.assetid: 98ff6ed4-ad3d-44f8-893d-f016e5217ce5
keywords:
- Media. sourceURL Lecteur Windows Media
topic_type:
- apiref
api_name:
- Media.sourceURL
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e2f99aeb64a73bcf36e2cbd472aedfa8f509a5073e70792e7b47343a1b37d60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119415949"
---
# <a name="mediasourceurl"></a>Media. sourceURL

La propriété **sourceURL** récupère l’URL de l’élément multimédia.

## <a name="syntax"></a>Syntaxe

*lecteur*. *currentMedia*. sourceURL

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est une **chaîne** en lecture seule.

## <a name="examples"></a>Exemples

l’exemple de JScript suivant utilise un *média*. **sourceURL** pour récupérer l’URL du premier élément multimédia dans l’exemple de sélection ; l’URL de l’élément multimédia est ensuite affectée à la propriété **URL** de l’objet lecteur. L’objet **Player** a été créé avec ID = "Player".


```JScript
// Store the sample playlist object in a variable. 
var pl = Player.playlistCollection.getByName("Sample Playlist").item(0);

// Store the first media item from the sample playlist.
var media = pl.item(0);

// Change the URL property of the player to the URL of the media item.
Player.URL = media.sourceURL;

// Play the media item.
Player.controls.play();

```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet Media**](media-object.md)
</dt> </dl>

 

 





