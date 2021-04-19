---
description: Le rééchantillonneur audio effectue l’une des actions suivantes, ou les deux, sur un flux audio. Modifiez le taux d’échantillonnage. Modifiez le nombre de canaux.
ms.assetid: bee755c4-0585-40fb-aa4d-4e964f5144a3
title: Resampler audio - DSP (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fb173fa4f8d964bec1102c4cfeefa4bf83f1ffe
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106524790"
---
# <a name="audio-resampler-dsp"></a>Modèle de rééchantillonnage audio DSP

Le rééchantillonneur audio effectue l’une des actions suivantes, ou les deux, sur un flux audio.

-   Modifiez le taux d’échantillonnage.
-   Modifiez le nombre de canaux.

## <a name="clsid"></a>CLSID

CLSID \_ CResamplerMediaObject

## <a name="interfaces"></a>Interfaces

-   [**IMediaObject**](/previous-versions/ms785953(v=vs.85))
-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)
-   [**IWMResamplerProps**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmresamplerprops)

## <a name="formats"></a>Formats

Virgule flottante PCM ou IEEE

Le type de média doit spécifier un format audio PCM ou à virgule flottante non compressé.

-   Pour l’interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) , initialisez le type de média comme décrit dans [types de médias audio non compressés](uncompressed-audio-media-types.md).
-   Pour l’interface [**IMediaObject**](/previous-versions/ms785953%28v%3dvs.85%29) , le type de support doit être de type **\_ WaveFormatEx** . Pour plus d’informations, [**consultez \_ \_ type de média DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type).

## <a name="properties"></a>Propriétés

-   [MFPKEY \_ WMRESAMP \_ FILTERQUALITY](mfpkey-wmresamp-filterquality.md)
-   [MFPKEY \_ WMRESAMP \_ CHANNELMTX](mfpkey-wmresamp-channelmtx.md)
-   [MFPKEY \_ WMRESAMP \_ passe-bas \_ bande passante](mfpkey-wmresamp-lowpass-bandwidth.md)

## <a name="required-attributes"></a>Attributs requis

Le rééchantillonneur requiert la définition des attributs suivants :

-   [\_masque de \_ \_ canal audio MF MT \_](mf-mt-audio-channel-mask-attribute.md)
-   [\_octets de \_ données audio MF MT- \_ \_ octets \_ par \_ seconde](mf-mt-audio-avg-bytes-per-second-attribute.md)
-   [\_alignement de \_ \_ bloc audio MF MT \_](mf-mt-audio-block-alignment-attribute.md)

## <a name="custom-channel-mapping"></a>Mappage de canal personnalisé

Le rééchantillonneur audio mappe les canaux audio d’entrée aux canaux audio de sortie, en fonction des informations suivantes :

-   Le nombre de canaux. Cela est indiqué dans l’attribut [MF \_ MT \_ audio \_ num \_ Channels](mf-mt-audio-num-channels-attribute.md) du type de média ou le membre **nChannels** de la structure [WAVEFORMATEX](mf-mt-audio-prefer-waveformatex-attribute.md) .
-   Masque de canal qui attribue des canaux à la position du haut-parleur. Le masque de canal est fourni dans l' \_ \_ \_ attribut de masque de canal audio MF MT audio \_ du type de média ou dans le membre **dwChannelMask** de la structure [**WAVEFORMATEXTENSIBLE**](/windows/desktop/api/mmreg/ns-mmreg-waveformatextensible) .
-   Matrice de poids de mappage.

La matrice contient une série de pondérations, de telle sorte que chaque canal de sortie est une moyenne pondérée des canaux d’entrée.

Vous pouvez spécifier une matrice personnalisée pour le mappage de canal en appelant [**IWMResamplerProps :: SetUserChannelMtx**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmresamplerprops-setuserchannelmtx) ou en définissant la propriété [**MFPKEY \_ WMRESAMP \_ CHANNELMTX**](mfpkey-wmresamp-channelmtx.md) . Si aucune matrice personnalisée n’est fournie, le rééchantillonneur audio utilise un ensemble de matrices par défaut.

## <a name="default-channel-mapping"></a>Mappage de canal par défaut

Si vous ne spécifiez pas de matrice personnalisée, le fournisseur de rééchantillonnages audio utilise les valeurs par défaut pour le mappage de canal.

Dans les tableaux qui suivent, les canaux sont abrégés :

-   L : à gauche
-   R : droite
-   C : Centre
-   LFE : effets fréquence bas
-   BL : arrière gauche
-   BR : retour à droite
-   SL : Surround à gauche
-   SR : placer à droite

Le tableau suivant présente les coefficients par défaut pour le mappage de 6 canaux (masque 0x3F) à 2 canaux.



|     | L     | R     | C     | LFE   | BL    | BR    |
|-----|-------|-------|-------|-------|-------|-------|
| L   | 0,314 | 0     | 0,222 | 0,031 | 0,268 | 0,164 |
| R   | 0     | 0,314 | 0,222 | 0,031 | 0,164 | 0,268 |



 

Le tableau suivant indique les coefficients par défaut pour le mappage de 6 canaux (masque 0x60F) à 2 canaux.



|     | L     | R     | C     | LFE   | SL    | SR    |
|-----|-------|-------|-------|-------|-------|-------|
| L   | 0,320 | 0     | 0,226 | 0,032 | 0,292 | 0,130 |
| R   | 0     | 0,320 | 0,226 | 0,032 | 0,130 | 0,292 |



 

Le tableau suivant indique les coefficients par défaut pour le mappage de canaux 6 (Mask 0x3F ou 0x60F) à 1 canal.



|     | L     | R     | C     | LFE   | BL (SL) | BR (SR) |
|-----|-------|-------|-------|-------|--------|--------|
| C   | 0,192 | 0,192 | 0,192 | 0,038 | 0,192  | 0,192  |



 

Le tableau suivant indique les coefficients par défaut pour le mappage de 8 canaux (masque 0x63F) à 2 canaux.



|     | L     | R     | C     | LFE   | BL    | BR    | SL    | SR    |
|-----|-------|-------|-------|-------|-------|-------|-------|-------|
| L   | 0,222 | 0     | 0,157 | 0,022 | 0,189 | 0,116 | 0,203 | 0,090 |
| R   | 0     | 0,222 | 0,157 | 0,022 | 0,116 | 0,189 | 0,090 | 0,203 |



 

Le tableau suivant indique les coefficients par défaut pour le mappage de 8 canaux (masque 0x63F) à 1 canal.



|     | L     | R     | C     | LFE   | BL    | BR    | SL    | SR    |
|-----|-------|-------|-------|-------|-------|-------|-------|-------|
| C   | 0,139 | 0,139 | 0,139 | 0,028 | 0,139 | 0,139 | 0,139 | 0,139 |



 

Le tableau suivant présente les coefficients par défaut pour le mappage de 8 canaux (masque 0x63F) à 6 canaux (masque 0x3F).



|     | L     | R     | C     | LFE   | BL    | BR    | SL    | SR    |
|-----|-------|-------|-------|-------|-------|-------|-------|-------|
| L   | 0,518 | 0     | 0     | 0     | 0     | 0     | 0,189 | 0     |
| R   | 0     | 0,518 | 0     | 0     | 0     | 0     | 0     | 0,189 |
| C   | 0     | 0     | 0,518 | 0     | 0     | 0     | 0     | 0     |
| LFE | 0     | 0     | 0     | 0,518 | 0     | 0     | 0     | 0     |
| BL  | 0     | 0     | 0     | 0     | 0,518 | 0     | 0,482 | 0     |
| BR  | 0     | 0     | 0     | 0     | 0     | 0,518 | 0     | 0,482 |



 

Le tableau suivant présente les coefficients par défaut pour le mappage de 8 canaux (masque 0x63F) à 6 canaux (masque 0x60F).



|     | L     | R     | C     | LFE   | BL    | BR    | SL    | SR    |
|-----|-------|-------|-------|-------|-------|-------|-------|-------|
| L   | 0,447 | 0     | 0     | 0     | 0     | 0     | 0     | 0     |
| R   | 0     | 0,447 | 0     | 0     | 0     | 0     | 0     | 0     |
| C   | 0     | 0     | 0,447 | 0     | 0     | 0     | 0     | 0     |
| LFE | 0     | 0     | 0     | 0,447 | 0     | 0     | 0     | 0     |
| SL  | 0     | 0     | 0     | 0     | 0,429 | 0,124 | 0,447 | 0     |
| SR  | 0     | 0     | 0     | 0     | 0,124 | 0,429 | 0     | 0,447 |



 

Pour comprendre comment interpréter les tables de coefficients, considérez la première table, qui mappe 6 canaux à 2. La première ligne de la table (0,314, 0, 0,222, 0,031, 0,268, 0,164) est un vecteur de poids qui spécifie la manière dont chaque canal d’entrée contribue au canal gauche de la sortie. La deuxième ligne de la table (0, 0,314, 0,222, 0,031, 0,164, 0,268) est un vecteur de pondérations qui spécifie la manière dont chaque canal d’entrée contribue au canal approprié de la sortie.

Les formules suivantes montrent comment les canaux de sortie sont calculés.

``` syntax
L_out = L*0.314 + C*0.222 + LFE*0.031 + BL*0.268 + BR*0.164 
R_out = R*0.314 + C*0.222 + LFE*0.031 + BL*0.164 + BR*0.268
```

> [!Note]  
> Si vous utilisez le DSP audio sampler pour augmenter le nombre de canaux, les valeurs affectées aux canaux ajoutés sont 0.

 

## <a name="output-quality"></a>Qualité de sortie

Vous pouvez spécifier la qualité de sortie du modèle DSP de l’échantillon audio en appelant [**IWMResamplerProps :: SetHalfFilterLength**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmresamplerprops-sethalffilterlength) ou en définissant la propriété [**MFPKEY \_ WMRESAMP \_ FILTERQUALITY**](mfpkey-wmresamp-filterquality.md) . Si vous ne spécifiez pas la qualité de sortie, le fournisseur de rééchantillonnages audio utilise une valeur de qualité par défaut de 30.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                       |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>Resampledmo.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

[Processeurs de signaux numériques](windowsmediadigitalsignalprocessors.md)
