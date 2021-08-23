---
title: Player. currentMedia
description: La propriété currentMedia spécifie ou récupère l’objet multimédia actuel.
ms.assetid: 5cf45a10-9d0d-435e-97f1-d2c9c51f4b47
keywords:
- Lecteur Windows Media Player. currentMedia
topic_type:
- apiref
api_name:
- Player.currentMedia
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7df5e8cd2032d772cbd781d0b45794e86cc19eff7c730a6a963778d54a6f283d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054397"
---
# <a name="playercurrentmedia"></a>Player. currentMedia

La propriété **currentMedia** spécifie ou récupère l’objet multimédia actuel.

## <a name="syntax"></a>Syntaxe

*lecteur* . **currentMedia**

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est un objet multimédia en lecture/écriture.

## <a name="remarks"></a>Remarques

si le *Paramètres*. la propriété **AutoStart** a la valeur true, la lecture commence automatiquement chaque fois que vous définissez **currentMedia**.

Cette propriété prend un objet multimédia, qui peut être acquis à l’aide de la *sélection*. **élément**. Pour charger un élément **multimédia** à l’aide d’un nom de fichier, définissez la propriété URL ou utilisez **newMedia**.

## <a name="examples"></a>Exemples

l’exemple de JScript suivant récupère le premier élément multimédia de la bibliothèque. Il utilise ensuite **currentMedia** pour transformer l’élément multimédia récupéré en élément multimédia actuel, puis pour afficher le nom de l’élément multimédia en cours. L’objet **Player** a été créé avec ID = "Player".


```JScript
// Retrieve the first media item from the library.
var firstMedia = Player.mediaCollection.getAll().item(0);

// Make the retrieved media item the current media item.
Player.currentMedia = firstMedia;

// Display the name of the current media item.
document.write("Found first media item. Name = " + Player.currentMedia.name);
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet Media**](media-object.md)
</dt> <dt>

[**Objet Player**](player-object.md)
</dt> <dt>

[**Player. newMedia**](player-newmedia.md)
</dt> <dt>

[**Playlist. Item**](playlist-item.md)
</dt> <dt>

[**Paramètres. démarrage automatique**](settings-autostart.md)
</dt> </dl>

 

 





