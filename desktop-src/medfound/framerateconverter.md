---
description: Modifie la fréquence d’images d’un flux vidéo.
ms.assetid: a66b9c52-a015-41d2-b27a-3ce6a4d95be9
title: Convertisseur de fréquence d’images DSP (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ca4a728f37caa43ee99a0d293d5113e9c26cfb1dcfe51f399482fb614283737
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600489"
---
# <a name="frame-rate-converter-dsp"></a>Convertisseur de fréquence d’images DSP

Modifie la fréquence d’images d’un flux vidéo.

## <a name="clsid"></a>CLSID

CLSID \_ CFrameRateConvertDmo

## <a name="interfaces"></a>Interfaces

-   **IMediaObject**
-   **IMFTransform**
-   **IPropertyStore**

## <a name="formats"></a>Formats

-   ARGB 32
-   RVB 24
-   RGB 32
-   RGB 555
-   RGB 565
-   AYUV
-   IYUV
-   UYVY
-   Y211
-   Y411
-   Y41P
-   YUY2
-   YUYV
-   YV12
-   YVYU

## <a name="properties"></a>Propriétés

-   [MFPKEY \_ conv \_ INPUTFRAMERATE](mfpkey-conv-inputframerate.md)
-   [MFPKEY \_ conv \_ OUTPUTFRAMERATE](mfpkey-conv-outputframerate.md)

## <a name="remarks"></a>Remarques

Ce DSP modifie la fréquence d’images en répétant ou en supprimant des frames.

Par défaut, le DSP obtient les fréquences d’images des types de médias. Si vous le souhaitez, vous pouvez spécifier les fréquences d’images en définissant les \_ Propriétés MFPKEY CONV \_ INPUTFRAMERATE et MFPKEY \_ conv \_ OUTPUTFRAMERATE. Ces valeurs remplacent la fréquence d’images donnée dans le type de média. Toutefois, si vous utilisez ce DSP dans le pipeline Media Foundation, vous ne devez pas définir ces propriétés.

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

 

 




