---
description: Ajuste les caractéristiques de couleur d’un flux vidéo.
ms.assetid: 738c1f0c-8417-4b12-a7f1-9bbf3c7e9dd3
title: Transformation de contrôle de couleur DSP (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c51321a8ffd725306f570619b9bcbe70fe7160e784358ce265157145b40347e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606209"
---
# <a name="color-control-transform-dsp"></a>Transformation de contrôle de couleur DSP

Ajuste les caractéristiques de couleur d’un flux vidéo.

## <a name="clsid"></a>CLSID

CLSID \_ CColorControlDmo

## <a name="interfaces"></a>Interfaces

-   **IMediaObject**
-   **IMFTransform**
-   **IPropertyStore**

## <a name="formats"></a>Formats

-   RVB 24
-   RGB 32
-   RGB 555
-   RGB 565
-   AYUV
-   UYVY
-   YUY2
-   YV12

## <a name="properties"></a>Propriétés

-   [\_luminosité des couleurs MFPKEY \_](mfpkey-color-brightness.md)
-   [\_contraste des couleurs MFPKEY \_](mfpkey-color-contrast.md)
-   [\_teinte de couleur MFPKEY \_](mfpkey-color-hue.md)
-   [SATURATION de la \_ couleur MFPKEY \_](mfpkey-color-saturation.md)

## <a name="remarks"></a>Remarques

Ce DSP modifie le contenu du flux vidéo. Pour la lecture, vous pourrez peut-être obtenir des effets similaires plus efficacement à l’aide de l’interface **IMFVideoProcessor** , qui contrôle le traitement vidéo dans la carte graphique.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Mfvdsp.dll</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Processeurs de signaux numériques](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 




