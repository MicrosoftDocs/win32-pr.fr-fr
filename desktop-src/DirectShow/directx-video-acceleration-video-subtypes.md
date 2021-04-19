---
description: Les sous-types suivants sont utilisés par les décodeurs qui utilisent DirectX Video Acceleration (DXVA).
ms.assetid: 031b076b-cdfa-407f-8efa-391bce3075ef
title: Sous-types vidéo DirectX Video Acceleration (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0df0f079e795638c6802570c95e2468209a7256
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525269"
---
# <a name="directx-video-acceleration-video-subtypes"></a>Sous-types vidéo DirectX Video Acceleration

Les sous-types suivants sont utilisés par les décodeurs qui utilisent DirectX Video Acceleration (DXVA). AI44 et IA44 sont des surfaces avec une valeur de bits par pixel de 8. Il y a 4 bits d’I et 4 bits de *a*. *Je* représente un index dans une palette YUV à 16 entrées. *Un* représente 4 bits d’informations de transparence (également appelées par pixel-alpha). Par conséquent, les surfaces AI44 et IA44 autorisent 16 couleurs différentes à 16 valeurs de transparence différentes, ou 256 représentations de pixels différentes. Avec AI44, l’alpha est stocké dans le grignot-Quartet, en IA44, le alpha est stocké dans le grignot-Quartet. Les deux formats sont très utiles pour les images de sous-image de DVD et les images Line21 et Teletext. Microsoft préfère la version AI44, car il est légèrement plus facile de générer du texte à l’aide de ce format.

| Subtype            | Description                                                 |
|--------------------|-------------------------------------------------------------|
| MEDIASUBTYPE \_ AI44 | Pour les superpositions de sous-image et de texte. Consultez la description précédente. |
| MEDIASUBTYPE \_ IA44 | Pour les superpositions de sous-image et de texte. Consultez la description précédente. |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Sous-types de vidéos](video-subtypes.md)
</dt> </dl>

 

 




