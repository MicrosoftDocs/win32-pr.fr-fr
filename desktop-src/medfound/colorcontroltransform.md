---
description: Ajuste les caractéristiques de couleur d’un flux vidéo.
ms.assetid: 738c1f0c-8417-4b12-a7f1-9bbf3c7e9dd3
title: Transformation de contrôle de couleur DSP (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b94c8314bfd2be85a3bbc392bfa0e83767ff0b0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127227796"
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

## <a name="remarks"></a>Notes

Ce DSP modifie le contenu du flux vidéo. Pour la lecture, vous pourrez peut-être obtenir des effets similaires plus efficacement à l’aide de l’interface **IMFVideoProcessor** , qui contrôle le traitement vidéo dans la carte graphique.

## <a name="requirements"></a>Spécifications



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

 

 




