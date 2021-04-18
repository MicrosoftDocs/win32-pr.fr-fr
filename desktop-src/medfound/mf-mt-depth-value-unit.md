---
description: Valeur qui définit les unités pour une valeur de profondeur dans une image vidéo.
ms.assetid: 0D7238F3-C224-48BD-8654-B3182DFB244C
title: Attribut MF_MT_DEPTH_VALUE_UNIT (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f6086a34f62c26b3fe1fa611318792c9056a50c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519597"
---
# <a name="mf_mt_depth_value_unit-attribute"></a>\_Attribut d' \_ \_ unité de valeur de profondeur MT MF \_

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]

Valeur qui définit les unités pour une valeur de profondeur dans une image vidéo.

## <a name="data-type"></a>Type de données

**UINT64**

## <a name="remarks"></a>Notes

La valeur d’unité est une valeur UINT64 en nanomètres, dans la plage de 1e à 9 mètres. Si cette valeur n’est pas présente, la valeur par défaut de l’unité est 1e-3, ce qui indique que chaque niveau de pixel est mesuré en 1 millimètre dans l’espace physique.

Les caméras de profondeur ne peuvent pas détecter la profondeur de tous les pixels. Lorsque la confiance d’un pixel est faible, en raison d’un matériau, d’une occlusion ou d’une plage de valeurs, etc., la valeur de profondeur sur ce pixel peut être non valide.

Lorsqu’une valeur de pixel de profondeur est 0, le pixel n’est pas valide.

Certaines caméras de profondeur attachent des métadonnées de masque de bits pour chaque pixel, en plus de la valeur de profondeur pour représenter la raison pour laquelle la profondeur de pixel n’est pas valide, en raison d’un matériau, d’une occlusion ou d’une plage de valeurs, etc. Nous vous recommandons d’éviter d’attacher ces métadonnées en tant que bits en valeur de profondeur, car cela entraîne généralement des difficultés lors de l’utilisation de ces valeurs dans le nuanceur de pixels. Qu'. Nous vous recommandons d’utiliser une mémoire tampon d’image 8 bits distincte avec la même résolution et de l’attacher en tant qu’attribut du [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample). Ces métadonnées varient pour chaque fournisseur d’appareils photo et ne sont pas standardisées par la plateforme. Nous vous recommandons d’utiliser 16 bits complets pour la valeur de profondeur pour un traitement plus facile en aval et en utilisant une valeur fixe telle que 0 pour l’invalidation.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows 10, version 1709 \[ uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows Server, version 1709, \[ applications de bureau uniquement\]<br/>                      |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



 

 




