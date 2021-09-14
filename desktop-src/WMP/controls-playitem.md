---
title: Controls. playItem, méthode
description: La méthode playItem lit l’élément multimédia spécifié. | Controls. playItem, méthode
ms.assetid: 410e315d-8d5f-4f45-82a7-4249e656c809
keywords:
- Lecteur Windows Media de la méthode playItem
- méthode playItem Lecteur Windows Media, classe controls
- controls, classe Lecteur Windows Media, méthode playItem
topic_type:
- apiref
api_name:
- Controls.playItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9096e378a328f43147a0a94d97034c8e566b611
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126919332"
---
# <a name="controlsplayitem-method"></a>Controls. playItem, méthode

La méthode **playItem** lit l’élément multimédia spécifié.

## <a name="syntax"></a>Syntaxe


```JScript
Controls.playItem(
  theMediaItem
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*theMediaItem* \[ dans\]
</dt> <dd>

Objet **multimédia** à lire.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

l’élément multimédia est chargé et lu automatiquement, quelle que soit la valeur de la *Paramètres*. propriété **AutoStart** . pour charger un élément sans le relire automatiquement, définissez *Paramètres*. **démarrage automatique** sur false et attribution d’une valeur à *Player*. **URL**, après laquelle la **lecture** peut être appelée pour démarrer la lecture de l’élément.

Remarque

**playItem** fonctionne uniquement avec les éléments dans *currentPlaylist*. L’appel de **playItem** avec une référence à un élément multimédia enregistré n’est pas pris en charge.

## <a name="examples"></a>Exemples

l’exemple de JScript suivant utilise **playItem** pour lire un élément multimédia à partir de la sélection actuelle. L’élément à lire est choisi en fonction de sa position dans la sélection. L’objet **Player** a été créé avec ID = "Player".


```JScript
// Declare a variable to hold the position of the media item 
// in the current playlist. An arbitrary value is supplied here.
var index = 3

// Retrieve the media item at the fourth position in the current playlist.
var media = Player.currentPlaylist.item(index);

// Play the media item.
Player.controls.playItem(media);

```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Controls (objet)**](controls-object.md)
</dt> <dt>

[**Playlist. Item**](playlist-item.md)
</dt> </dl>

 

 





