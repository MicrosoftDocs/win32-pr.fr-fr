---
title: VIDEO. Zoom
description: L’attribut zoom spécifie le pourcentage de mise à l’échelle de la vidéo.
ms.assetid: 71c0e5a6-f7c4-46cf-a180-083d2926ba20
keywords:
- VIDEO. Zoom lecteur Windows Media
topic_type:
- apiref
api_name:
- VIDEO.zoom
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b989cabcf84244976bda728d12c97697338f742
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525323"
---
# <a name="videozoom"></a>VIDEO. Zoom

L’attribut **Zoom** spécifie le pourcentage de mise à l’échelle de la vidéo.

``` syntax
        elementID.zoom
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est un **nombre** en lecture/écriture (**long**) compris entre 1 et la taille maximale prise en charge par la largeur et la hauteur du contrôle Video. Sa valeur par défaut est 100.

## <a name="remarks"></a>Notes

Cet attribut ne peut pas être utilisé conjointement avec l’attribut **fullscreen** .

Si la **largeur** et la **hauteur** sont spécifiées et que la fenêtre vidéo obtenue est plus grande que la vidéo en cours de lecture, la vidéo peut être agrandie en augmentant jusqu’à la taille maximale prise en charge par la fenêtre. Si la **largeur** et la **hauteur** ne sont pas spécifiées, le **zoom** est limité aux valeurs 100 ou inférieures.

Si la propriété **shrinkToFit** a la valeur false, la vidéo change de proportion lors du zoom, pour s’adapter à l’espace disponible. Si **shrinkToFit** a la valeur true, la vidéo sera réduite pour s’ajuster à la dimension la plus restrictive, tout en conservant ses proportions d’origine.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément VIDEO**](video-element.md)
</dt> <dt>

[**VIDEO. fullScreen**](video-fullscreen.md)
</dt> <dt>

[**VIDÉO. shrinkToFit**](video-shrinktofit.md)
</dt> </dl>

 

 





