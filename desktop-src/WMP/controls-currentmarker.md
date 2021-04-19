---
title: Controls. currentMarker
description: La propriété currentMarker spécifie ou récupère le numéro de marqueur actuel.
ms.assetid: 4b4eacd4-3df0-4e11-8755-1ac326fad027
keywords:
- Controls. currentMarker Windows Media Player
topic_type:
- apiref
api_name:
- Controls.currentMarker
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8aae8af226b62550b3faae9389385d321bf10aad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544465"
---
# <a name="controlscurrentmarker"></a>Controls. currentMarker

La propriété **currentMarker** spécifie ou récupère le numéro de marqueur actuel.

``` syntax
player.controls.currentMarker
      
```

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est un **nombre** en lecture/écriture (**long**) avec une valeur par défaut de zéro.

## <a name="remarks"></a>Notes

La définition de **currentMarker** entraîne le démarrage de la lecture à partir du marqueur spécifié. Avant de tenter de définir **currentMarker**, déterminez si un fichier a des marqueurs et combien il a à l’aide de **markerCount**. Si un fichier n’a pas de marqueur, la définition de **currentMarker** sur n’importe quelle valeur, sauf zéro, génère une erreur. Si vous définissez **currentMarker** sur un nombre supérieur à **markerCount** , une erreur est également générée.

La propriété **currentMarker** retourne toujours le marqueur actuel ou le dernier marqueur, ce qui signifie que la position de fichier réelle peut être soit au marqueur actuel, soit avant le marqueur suivant. Les marqueurs sont numérotés à partir de 1. par conséquent, si un fichier a des marqueurs, vous pouvez affecter la valeur zéro à **currentMarker** pour changer la position du fichier.

Jusqu’à ce que l’élément multimédia actuel soit défini (à l’aide de *Player*.**URL** ou *lecteur*. **currentMedia**), **currentMarker** retourne zéro.

## <a name="examples"></a>Exemples

L’exemple JScript suivant utilise **currentMarker** pour démarrer la lecture vidéo à partir du marqueur qui correspond à la propriété **SelectedIndex** d’un élément Select HTML. L’objet **Player** a été créé avec ID = "Player".


```JScript
<SELECT ID = "markers"  NAME = "markers"  LANGUAGE = "JScript"

    /* Seek to the marker number that corresponds to the SELECT element
       selectedIndex value when the list selection changes. */
    onChange = "Player.controls.currentMarker = markers.selectedIndex + 1;
">

    /* Fill the SELECT element with the marker identifiers. */
    <OPTION SELECTED>Sunrise
    <OPTION>Car chase 
    <OPTION>Happy ending
</SELECT>

```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Controls (objet)**](controls-object.md)
</dt> <dt>

[**Media. markerCount**](media-markercount.md)
</dt> <dt>

[**Player. currentMedia**](player-currentmedia.md)
</dt> <dt>

[**Player. URL**](player-url.md)
</dt> </dl>

 

 





