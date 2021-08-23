---
description: Le filtre d’encodeur audio Microsoft MPEG-2 encode les couches audio MPEG-1 et II, y compris la prise en charge des extensions LSF (Low échantillonnage Frequency) MPEG-2.
ms.assetid: a36e838b-8b11-4851-9dd2-efd9fe070770
title: Encodeur audio Microsoft MPEG-2 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 030821905862a9698ee24c3227f2846cd8c892e20c501d2776cdf2f9bb88f3e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119584119"
---
# <a name="microsoft-mpeg-2-audio-encoder"></a>Encodeur audio Microsoft MPEG-2

Le filtre d’encodeur audio Microsoft MPEG-2 encode les couches audio MPEG-1 et II, y compris la prise en charge des extensions LSF (Low échantillonnage Frequency) MPEG-2.

Pour encoder et multiplexer des flux audio/vidéo, utilisez le filtre d' [**encodeur Microsoft MPEG-2**](microsoft-mpeg-2-encoder.md) , qui encapsule les fonctions de ce filtre et du filtre d' [**encodeur vidéo Microsoft MPEG-2**](microsoft-mpeg-2-video-encoder.md) .

> [!Note]  
> Ce filtre n’est pas pris en charge sur les plateformes IA-64.

 



Informations de filtre

Interfaces de filtre

[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> **IEncoderAPI**<br/> [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**IVideoEncoder**](/windows/win32/api/strmif/nn-strmif-ivideoencoder)<br/>

Types de média de broche d’entrée

**MediaType \_ Audio**, **MEDIASUBTYPE \_ PCM**

Interfaces pin d’entrée

[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Types de média de broche de sortie

**MediaType \_ Audio**, **MEDIASUBTYPE \_ MPEG2 \_ audio**<br/> **MediaType \_ Flux**, **MEDIASUBTYPE \_ MPEG2 \_ audio**<br/> **MediaType \_ Stream**, **\_ \_ programme MEDIASUBTYPE MPEG2**<br/> **MediaType \_ Flux**, **\_ \_ transport MEDIASUBTYPE MPEG2**<br/>

Interfaces de broche de sortie

[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

CLSID du filtre

**CLSID \_ CMPEG2EncoderAudioDS** (déclaré dans wmcodecdsp. h)

Exécutable

msmpeg2enc.dll

[Mérite](merit.md)

**MÉRITE \_ n' \_ \_ utilise pas**

[Catégorie de filtre](filter-categories.md)

**CLSID \_ LegacyAmFilterCategory**



 

## <a name="remarks"></a>Remarques

L’encodeur audio MPEG-2 peut générer les types de sortie suivants :

-   Flux élémentaire audio
-   Audio dans un flux de programme MPEG-2
-   Audio dans un flux de transport MPEG-2

Il prend en charge les couches MPEG-1 I et II et les extensions LSF (Low échantillonnage Frequency) MPEG-2

Les échantillons d’entrée doivent être de 16 bits par échantillon, avec un taux d’échantillonnage audio de 48, 44,1, 32, 22,05 ou 16 KHz. L’encodeur ne peut pas rééchantillonner le flux audio. l’audio encodé présente le même taux d’échantillonnage que l’entrée.

Les échantillons d’entrée doivent être mono ou stéréo. L’audio encodé a le nombre de canaux comme entrée.

### <a name="limitations"></a>Limites

L’encodeur ne prend pas en charge les éléments suivants :

-   Séquences binaires audio MPEG Layer III.
-   Flux de bits d’extension multicanaux MPEG-2.
-   Flux de bits AAC MPEG-4.
-   Flux de bits MPEG-2 NBC (non-backward compatible).
-   Génération de paquets d’extension de flux élémentaires (PES) paquets.
-   Encodage Dolby Digital.

### <a name="codec-properties"></a>Propriétés du codec

Le filtre prend en charge les propriétés suivantes par le biais de [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):

-   [**AVAudioChannelCount**](avaudiochannelcount-property.md)
-   [**AVAudioSampleRate**](avaudiosamplerate-property.md)
-   [**AVEncAudioIntervalToEncode**](avencaudiointervaltoencode-property.md)
-   [**AVEncCommonFormatConstraint**](avenccommonformatconstraint-property.md)
-   [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md)
-   [**AVEncMPACodingMode**](avencmpacodingmode-property.md)
-   [**AVEncMPACopyright**](avencmpacopyright-property.md)
-   [**AVEncMPAEmphasisType**](avencmpaemphasistype-property.md)
-   [**AVEncMPAEnableRedundancyProtection**](avencmpaenableredundancyprotection-property.md)
-   [**AVEncMPALayer**](avencmpalayer-property.md)
-   [**AVEncMPAOriginalBitstream**](avencmpaoriginalbitstream-property.md)
-   [**AVEncMPAPrivateUserBit**](avencmpaprivateuserbit-property.md)

> [!Note]  
> Une version antérieure de la documentation répertorie de manière incorrecte des propriétés supplémentaires qui ne sont pas prises en charge.

 

Pour la compatibilité descendante, le filtre prend en charge la propriété suivante par le biais de l’interface **IEncoderAPI** :



| Propriété                 | Description                                                                      |
|--------------------------|----------------------------------------------------------------------------------|
| **\_débit binaire ENCAPIPARAM** | Équivalent à [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md). |



 

Il est recommandé de définir des propriétés dans l’ordre suivant :

1.  [**AVEncCommonFormatConstraint**](avenccommonformatconstraint-property.md)
2.  [**AVEncMPALayer**](avencmpalayer-property.md)
3.  [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md)
4.  [**AVEncMPACodingMode**](avencmpacodingmode-property.md)

Définissez les propriétés restantes dans n’importe quel ordre.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows vista familial Premium, Windows vista Ultimate, Windows 7 Édition Familiale Premium, Windows 7 Professionnel, Windows 7 Entreprise, Windows 7 Édition Intégrale les \[ applications de bureau uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                                                                                     |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl>                                                                                       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[DirectShow Filtres](directshow-filters.md)
</dt> <dt>

[**Types de média du démultiplexeur MPEG-2**](mpeg-2-demultiplexer-media-types.md)
</dt> </dl>

 

 
