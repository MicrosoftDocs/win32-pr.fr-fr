---
description: Convertit un flux vidéo entre des formats de couleur.
ms.assetid: 1c15dc2b-0e69-4d16-af02-8056a1eb2c5c
title: Convertisseur de couleurs DSP (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73a8418d6eeeffcf83a38452b19f18a6baa60bcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484105"
---
# <a name="color-converter-dsp"></a>Convertisseur de couleurs DSP

Convertit un flux vidéo entre des formats de couleur.

## <a name="clsid"></a>CLSID

CLSID \_ CColorConvertDMO

## <a name="interfaces"></a>Interfaces

-   [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)
-   [**IMFRealTimeClient**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)
-   [IWMColorConvProps](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcolorconvprops)

## <a name="input-formats"></a>Formats d’entrée

-   RVB 24
-   RGB 32
-   RGB 555
-   RGB 565
-   RVB 8
-   AYUV
-   I420
-   IYUV
-   NV11
-   NV12
-   UYVY
-   V216
-   V410
-   Y41P
-   Y41T
-   Y42T
-   YUY2
-   YV12
-   YVU9
-   YVYU

## <a name="output-formats"></a>Formats de sortie

-   RVB 24
-   RGB 32
-   RGB 555
-   RGB 565
-   RVB 8
-   AYUV
-   I420
-   IYUV
-   NV11
-   NV12
-   UYVY
-   V216
-   V410
-   YUY2
-   YV12
-   YVYU

## <a name="properties"></a>Propriétés

-   [MFPKEY \_ COLORCONV \_ SRCLEFT](mfpkey-colorconv-srcleft.md)
-   [MFPKEY \_ COLORCONV \_ SRCTOP](mfpkey-colorconv-srctop.md)
-   [MFPKEY \_ COLORCONV \_ DSTLEFT](mfpkey-colorconv-dstleft.md)
-   [MFPKEY \_ COLORCONV \_ DSTTOP](mfpkey-colorconv-dsttop.md)
-   [largeur de MFPKEY \_ COLORCONV \_](mfpkey-colorconv-width.md)
-   [\_hauteur MFPKEY COLORCONV \_](mfpkey-colorconv-height.md)
-   [MFPKEY \_ \_ mode COLORCONV](mfpkey-colorconv-mode.md)

## <a name="remarks"></a>Notes

Le convertisseur de couleur DSP est implémenté en tant qu’objet COM pouvant agir comme un objet DirectXMedia (DMO) ou une transformation de Media Foundation (MFT). L’objet a un identificateur de classe unique (CLSID), qu’il agisse comme DMO ou MFT. Pour plus d’informations sur le moment où un DSP agit comme DMO ou MFT, consultez [processeurs de signal numérique](windowsmediadigitalsignalprocessors.md).

Les identificateurs globaux uniques (GUID) pour les sous-types de média RVB diffèrent selon qu’un DSP fait office de modèle DMO ou MFT. Les GUID pour les sous-types de média non RVB sont les mêmes, qu’un DSP agisse comme DMO ou MFT. Pour plus d’informations sur les GUID qui représentent des sous-types de médias, consultez [GUID de sous-type de vidéo](video-subtype-guids.md).

Par défaut, ce DSP copie l’intégralité de l’image source dans la mémoire tampon de sortie. Si vous le souhaitez, vous pouvez spécifier des rectangles sources et de destination. Le DSP copie la partie de l’image source définie par le rectangle source et l’écrit dans le rectangle de destination de la mémoire tampon de sortie. Le DSP n’effectue aucune mise à l’échelle ; les rectangles source et de destination doivent avoir la même taille. Les rectangles source et de destination ne peuvent pas dépasser les limites de la trame vidéo.

Toutes les propriétés, à l’exception du [**\_ \_ mode MFPKEY COLORCONV**](mfpkey-colorconv-mode.md) , doivent être définies dans un groupe. Si vous définissez l’une de ces propriétés, vous devez définir tous les autres. Dans le cas contraire, les rectangles source et de destination peuvent être non valides, auquel cas les méthodes [**IMFTransform ::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) et [**IMediaObject ::P rocessoutput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput) retournent **E \_ INVALIDARG**.

Le convertisseur de couleur ne prend pas en charge toutes les combinaisons de format d’entrée et de sortie. En règle générale, vous devez définir le format de média que vous connaissez, en entrée ou en sortie, puis énumérer les formats disponibles sur le flux de données opposé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Colorcnv.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Processeurs de signaux numériques](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 
