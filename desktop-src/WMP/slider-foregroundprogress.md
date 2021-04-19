---
title: Slider. foregroundProgress
description: L’attribut foregroundProgress spécifie ou récupère la position actuelle de la barre de progression en premier plan sous la forme d’un pourcentage de la zone de curseur.
ms.assetid: 1218ca5a-445c-441b-aa62-74a184a25c2d
keywords:
- Slider. foregroundProgress lecteur Windows Media
topic_type:
- apiref
api_name:
- SLIDER.foregroundProgress
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4597630453444564411d0bcfad8dc6b39914d13
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537111"
---
# <a name="sliderforegroundprogress"></a>Slider. foregroundProgress

L’attribut **foregroundProgress** spécifie ou récupère la position actuelle de la barre de progression en premier plan sous la forme d’un pourcentage de la zone de curseur.

``` syntax
        elementID.foregroundProgress
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est un **nombre** en lecture/écriture (**float**) compris entre 0 et 100.

## <a name="remarks"></a>Notes

Cet attribut est utilisé principalement pour suivre la progression du téléchargement d’un fichier multimédia tout en effectuant un suivi simultané de la position de lecture actuelle du fichier à l’aide de l’attribut **value** . La position du curseur de défilement est restreinte à la zone de la progression du premier plan. Cela permet d’effectuer une recherche interactive uniquement dans la partie disponible d’un fichier de téléchargement.

Pour utiliser cette fonctionnalité, l’attribut **useForegroundProgress** doit avoir la valeur true.

## <a name="examples"></a>Exemples


```C++
<SLIDER
  id="seek"
  backgroundColor="blue"
  foregroundColor="red"
  thumbImage="seekthumb.bmp"
  min="0"
  max="wmpprop:player.currentMedia.duration"
  value="wmpprop:player.controls.currentPosition"
  useForegroundProgress="true"
  foregroundProgress="wmpprop:player.network.downloadProgress"
  ondragend="player.controls.currentposition=value"
/>

```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Slider (élément)**](slider-element.md)
</dt> <dt>

[**Slider. min.**](slider-min.md)
</dt> <dt>

[**Slider. Max**](slider-max.md)
</dt> <dt>

[**Slider. useForegroundProgress**](slider-useforegroundprogress.md)
</dt> <dt>

[**Slider. Value**](slider-value.md)
</dt> </dl>

 

 





