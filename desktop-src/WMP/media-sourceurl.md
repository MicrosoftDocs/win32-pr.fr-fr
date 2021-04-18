---
title: Media. sourceURL
description: La propriété sourceURL récupère l’URL de l’élément multimédia.
ms.assetid: 98ff6ed4-ad3d-44f8-893d-f016e5217ce5
keywords:
- Media. sourceURL Windows Media Player
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
ms.openlocfilehash: 2c32d594cd1c3b590001eedfd09e9a8c8eb21240
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540569"
---
# <a name="mediasourceurl"></a>Media. sourceURL

La propriété **sourceURL** récupère l’URL de l’élément multimédia.

## <a name="syntax"></a>Syntaxe

*lecteur*. *currentMedia*. sourceURL

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est une **chaîne** en lecture seule.

## <a name="examples"></a>Exemples

L’exemple JScript suivant utilise un *média*. **sourceURL** pour récupérer l’URL du premier élément multimédia dans l’exemple de sélection ; l’URL de l’élément multimédia est ensuite affectée à la propriété **URL** de l’objet lecteur. L’objet **Player** a été créé avec ID = "Player".


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

 

 





