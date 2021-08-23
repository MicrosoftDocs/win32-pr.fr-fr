---
description: Valeur qui définit le système de mesure pour une valeur de profondeur dans une image vidéo.
ms.assetid: 7BFA846B-E614-4117-A196-298E065CB7F8
title: Attribut MF_MT_DEPTH_MEASUREMENT (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a292e5a96cec7490917ef0bb897a9a7a67dd303d29692bf6db5ff58e1d4388c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119605796"
---
# <a name="mf_mt_depth_measurement-attribute"></a>\_Attribut de \_ mesure de profondeur du Mt MF \_

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft exclut toute garantie, expresse ou implicite, concernant les informations fournies ici.\]

Valeur qui définit le système de mesure pour une valeur de profondeur dans une image vidéo.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Remarques

Cette valeur est un membre de l’énumération [**\_ MFDepthMeasurement**](/windows/win32/api/mfapi/ne-mfapi-mfdepthmeasurement)

Si cet attribut n’est pas présent, il est supposé être **DistanceToFocalPlane**. La distance au plan focal est généralement plus facile à consommer dans un système de coordonnées 3D euclidienne.

![illustration de distancetofocalplane](images/distance-to-focal-plane.png)

La distance au format Centre focal est généralement des données brutes provenant d’un capteur, telles que le temps des caméras de vol.

![illustration de distancetoopticalcenter](images/distance-to-optical-center.png)

Les caméras de profondeur ne peuvent pas détecter la profondeur de tous les pixels. Lorsque la confiance d’un pixel est faible, en raison d’un matériau, d’une occlusion ou d’une plage de valeurs, etc., la valeur de profondeur sur ce pixel peut être non valide.

Lorsqu’une valeur de pixel de profondeur est 0, le pixel n’est pas valide.

Certaines caméras de profondeur attachent des métadonnées de masque de bits pour chaque pixel, en plus de la valeur de profondeur pour représenter la raison pour laquelle la profondeur de pixel n’est pas valide, en raison d’un matériau, d’une occlusion ou d’une plage de valeurs, etc. Nous vous recommandons d’éviter d’attacher ces métadonnées en tant que bits en valeur de profondeur, car cela entraîne généralement des difficultés lors de l’utilisation de ces valeurs dans le nuanceur de pixels. Qu'. Nous vous recommandons d’utiliser une mémoire tampon d’image 8 bits distincte avec la même résolution et de l’attacher en tant qu’attribut du [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample). Ces métadonnées varient pour chaque fournisseur d’appareils photo et ne sont pas standardisées par la plateforme. Nous vous recommandons d’utiliser 16 bits complets pour la valeur de profondeur pour un traitement plus facile en aval et en utilisant une valeur fixe telle que 0 pour l’invalidation.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, les applications de bureau version 1709 \[ uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows Serveur, version 1709 \[ applications de bureau uniquement\]<br/>                      |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



 

 




