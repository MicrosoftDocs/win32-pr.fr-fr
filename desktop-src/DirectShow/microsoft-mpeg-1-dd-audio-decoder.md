---
description: 'Ce filtre décode les formats audio suivants :'
ms.assetid: 2fd14296-9eed-4e25-b140-6281c707fdb7
title: Décodeur audio Microsoft MPEG-1/DD/AAC (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dd20bfc2ad8a366b46ac0c0600d8cc7a8bca5abacae621e8ea7d02f5f1cb4d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051249"
---
# <a name="microsoft-mpeg-1ddaac-audio-decoder"></a>Décodeur audio Microsoft MPEG-1/DD/AAC

Ce filtre décode les formats audio suivants :

-   Couches audio MPEG-1 I et II.
-   MPEG-2 audio à compatibilité descendante, couches I et II (ISO/IEC 13818-3), mono et stéréo uniquement.
-   Profil du codage audio avancé (AAC) faible.
-   High-Efficiency AAC (HE-AAC) version 1 et version 2.
-   Systèmes de cinéma numérique direct (DTS) pour la sortie numérique.
-   LPCM, mono et stéréo uniquement, avec ou sans en-têtes PES.
-   Dolby Digital.
-   Dolby Digital plus, y compris la conversion de Dolby Digital plus en Dolby Digital pour la sortie numérique.

> [!Note]  
> L’implémentation Microsoft de la technologie Dolby Digital est limitée aux termes du programme de gestion de licences Dolby Digital à utiliser par les applications Microsoft.

 

> [!Note]  
> Ce filtre n’est pas pris en charge sur les plateformes IA-64.

 

le décodage des formats Dolby Digital Plus, AAC et HE-aac requiert Windows 7. le décodage de dolby digital ou dolby digital Plus n’est pas pris en charge sur Windows 7 Édition Familiale Basique ou Windows 7 Édition Starter.

Dans le registre, le nom convivial de ce filtre est « Microsoft DTV-DVD audio décoder ».



Informations de filtre

Interfaces de filtre

[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/>

Types de média de broche d’entrée

dans Windows Vista et versions ultérieures, le filtre prend en charge les types d’entrée suivants :<br/>

-   **MediaType \_ Audio**, **MEDIASUBTYPE \_ Dolby \_ AC3** (voir la remarque 1.)
-   **MediaType \_ Audio**, **MEDIASUBTYPE \_ MPEG1Audio**
-   **MediaType \_ Audio**, **MEDIASUBTYPE \_ MPEG1Payload**
-   **MediaType \_ Audio**, **MEDIASUBTYPE \_ MPEG2 \_ audio**
-   **MediaType \_ \_ \_ Pack chiffré de DVD**, **MEDIASUBTYPE \_ Dolby \_ AC3** (voir la remarque 1.)
-   **MediaType \_ \_ \_ Pack chiffré de DVD**, **MEDIASUBTYPE \_ DTS** (voir la remarque 2.)
-   **MediaType \_ \_ \_ Pack chiffré DVD**, **MEDIASUBTYPE \_ DVD \_ LPCM \_ audio**
-   **MediaType \_ \_ \_ Pack chiffré DVD**, **MEDIASUBTYPE \_ MPEG2 \_ audio**
-   **MediaType \_ MPEG2 \_ PES**, **MEDIASUBTYPE \_ Dolby \_ AC3** (voir la remarque 1.)
-   **MediaType \_ MPEG2 \_ PES**, **MEDIASUBTYPE \_ DTS** (voir la remarque 2.)
-   **MediaType \_ MPEG2 \_ PES**, **MEDIASUBTYPE \_ DVD \_ LPCM \_ audio**
-   **MediaType \_ MPEG2 \_ PES**, **MEDIASUBTYPE \_ MPEG2 \_ audio**
-   **MediaType \_ Stream**, **MEDIASUBTYPE \_ Dolby \_ AC3** (voir la remarque 1.)
-   **MediaType \_ Stream**, **MEDIASUBTYPE \_ MPEG1Audio**
-   **MediaType \_ Flux**, **MEDIASUBTYPE \_ MPEG2 \_ audio**

à partir de Windows 7, le filtre prend également en charge les types d’entrée suivants :<br/>

-   **MediaType \_ Audio**, **MEDIASUBTYPE \_ Dolby \_ DDplus** (voir la remarque 1.)
-   **MediaType \_ Audio**, **MEDIASUBTYPE \_ DTS2** (voir la remarque 2.)
-   **MediaType \_ Audio**, **MEDIASUBTYPE \_ DVD \_ LPCM \_ audio**
-   **MediaType \_ Audio**, **MEDIASUBTYPE \_ DVM** (voir la remarque 1.)
-   **MediaType \_ Audio**, **MEDIASUBTYPE \_ MPEG \_ ADTS \_ AAC**
-   **MediaType \_ Audio**, **MEDIASUBTYPE \_ MPEG \_ garantie**
-   **MediaType \_ Audio**, **MEDIASUBTYPE \_ MPEG1AudioPayload**
-   **MediaType \_ Audio**, **MEDIASUBTYPE \_ RAW \_ AAC1**
-   **MediaType \_ Stream**, **MEDIASUBTYPE \_ Dolby \_ DDplus** (voir la remarque 1.)
-   **MediaType \_ Stream**, **MEDIASUBTYPE \_ MPEG \_ ADTS \_ AAC**
-   **MediaType \_ Stream**, **MEDIASUBTYPE \_ MPEG \_ garantie**

Le type d’entrée peut changer dynamiquement pendant la diffusion en continu.<br/> Pour plus d’informations sur ces types de médias, consultez [**sous-types audio**](audio-subtypes.md).<br/>

> [!Note]  
> 1. L’implémentation Microsoft de la technologie Dolby Digital est limitée aux termes du programme de gestion de licences Dolby Digital à utiliser par les applications Microsoft.

<br/>

> [!Note]  
> 2. Pour l’entrée de systèmes de cinéma numérique (DTS), seule la sortie S/PDIF est prise en charge (DTS sur S/PDIF). Le décodage audio n’est pas pris en charge.

<br/>

Interfaces pin d’entrée

[**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> [**IKsPropertySet**](ikspropertyset.md)<br/> [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Types de média de broche de sortie

dans Windows Vista et versions ultérieures, le filtre prend en charge les types de sortie suivants :<br/>

-   **MediaType \_ Audio**, **MEDIASUBTYPE \_ Dolby \_ AC3 \_ SPDIF** (identique au sous- **\_ type KSDATAFORMAT \_ IEC61937 \_ Dolby \_ Digital**)
-   **MediaType \_ Audio**, **MEDIASUBTYPE \_ PCM**

à partir de Windows 7, le filtre prend également en charge les types de sortie suivants :<br/>

-   **MediaType \_ Audio**, **\_ sous-type KSDATAFORMAT \_ IEC61937 \_ DTS**
-   **MediaType \_ Audio**, **MEDIASUBTYPE \_ IEEE \_ float**

Interfaces de broche de sortie

[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

CLSID du filtre

**CLSID \_ CMPEG2AudDecoderDS** (déclaré dans wmcodecdsp. h)

Exécutable

msmpeg2adec.dll

[Mérite](merit.md)

**Mérite \_ NORMAL** -1

[Catégorie de filtre](filter-categories.md)

**CLSID \_ LegacyAmFilterCategory**



 

> [!Note]  
> Une version antérieure de la documentation indiquait que ce filtre peut décoder « audio MPEG-2 ». Le filtre décode uniquement le son MPEG-2 à compatibilité descendante.

 

## <a name="remarks"></a>Remarques

Les flux mono sont toujours décodés en stéréo.

Pour les flux avec une configuration de canal de deux ou plusieurs haut-parleurs, le décodeur effectue l’une des opérations suivantes :

-   Mixages jusqu’à six canaux, à l’aide de la configuration de l’orateur 5,1 courant.
-   Downmixes en stéréo.

Pour choisir entre ces deux options, utilisez l’interface [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) pour définir la propriété [**AVDecCommonOutputFormat**](avdeccommonoutputformat-property.md) , avant de connecter les broches. En guise d’alternative, lorsque l’application génère le graphique de filtre, elle peut définir le type de média souhaité sur la broche de sortie.

### <a name="aac-decoding"></a>Décodage AAC

Pour AAC, le décodeur a certaines contraintes de format sur l’entrée AAC compressée. Ces contraintes de format sont les mêmes que le [**décodeur Media Foundation AAC**](../medfound/aac-decoder.md)et sont documentées dans la section «[**contraintes de format**](../medfound/aac-decoder.md)».

le décodeur DirectShow accepte également différents types d’entrée que le décodeur Media Foundation. le décodeur DirectShow prend en charge les types d’entrée AAC suivants :

-   **MEDIASUBTYPE \_ \_AAC1 brut**: AAC brut, généralement trouvé dans AVI ou Matroska (. MKV).
-   **MEDIASUBTYPE \_ MPEG \_ ADTS \_ AAC**: AAC dans un flux de transport de données audio (ADTS) pour la diffusion en continu.
-   **MEDIASUBTYPE \_ MPEG \_ garantie**: flux de transport avec une couche de synchronisation (garantie) et une couche multiplex (LATM).

Le décodeur Media Foundation prend en charge les types d’entrée AAC suivants :

-   MFAudioFormat \_ AAC (identique à **MEDIASUBTYPE \_ MPEG \_ HEAAC**) pour la lecture de fichiers MP4.
-   **MEDIASUBTYPE \_ \_AAC1 brut**.

### <a name="property-sets"></a>Jeux de propriétés

La broche d’entrée du décodeur prend en charge les jeux de propriétés suivants via [**IKsPropertySet**](ikspropertyset.md):

-   [**Jeu de propriétés protection de copie de DVD**](dvd-copy-protection-property-set.md)
-   [**Propriété rate-change définie**](rate-change-property-set.md).

> [!Note]  
> à partir de Windows 7, le décodeur prend en charge le mode d’astuce par le biais du jeu de propriétés rate-change. Il prend en charge les vitesses de lecture dans la plage \[ 0,501 – 2,0 \] , où 1,0 est la vitesse de lecture normale et 2,0 est le double de la vitesse normale.

 

### <a name="codec-properties"></a>Propriétés du codec

La broche d’entrée du décodeur prend en charge les propriétés suivantes par le biais de [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):



| Propriété                                                          | Nécessite                                                 |
|-------------------------------------------------------------------|----------------------------------------------------------|
| [**AVAudioChannelConfig**](avaudiochannelconfig-property.md)     | Windows Vista                                            |
| [**AVAudioChannelCount**](avaudiochannelcount-property.md)       | Windows Vista                                            |
| [**AVAudioSampleRate**](avaudiosamplerate-property.md)           | Windows Vista                                            |
| [**AVDDSurroundMode**](avddsurroundmode-property.md)             | Windows Vista uniquement ; non pris en charge dans Windows 7 ou version ultérieure. |
| [**AVDecAudioDualMono**](avdecaudiodualmono-property.md)         | Windows Vista                                            |
| [**AVDecCommonInputFormat**](avdeccommoninputformat-property.md) | Windows Vista                                            |
| [**AVDecCommonMeanBitRate**](avdeccommonmeanbitrate.md)          | Windows 7                                                |



 

Le filtre prend en charge les propriétés suivantes par le biais de [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):



| Propriété                                                                          | Nécessite      |
|-----------------------------------------------------------------------------------|---------------|
| [**AVDecAACDownmixMode**](avdecaacdownmixmode-property.md)                       | Windows 7     |
| [**AVDecAudioDualMonoReproMode**](avdecaudiodualmonorepromode-property.md)       | Windows Vista |
| [**AVDecCommonOutputFormat**](avdeccommonoutputformat-property.md) (voir la remarque 3.) | Windows Vista |
| [**AVDecDDDynamicRangeScaleHigh**](avdecdddynamicrangescalehigh-property.md)     | Windows Vista |
| [**AVDecDDDynamicRangeScaleLow**](avdecdddynamicrangescalelow-property.md)       | Windows Vista |
| [**AVDecDDOperationalMode**](avdecddoperationalmode-property.md)                 | Windows Vista |
| [**AVDecMmcssClass**](avdecmmcss-property.md)                                    | Windows Vista |
| [**AVDSPLoudnessEqualization**](avdsploudnessequalization-property.md)           | Windows 7     |
| [**AVDSPSpeakerFill**](avdspspeakerfill-property.md)                             | Windows 7     |



 

> [!Note]  
> 3. La propriété [**AVDecCommonOutputFormat**](avdeccommonoutputformat-property.md) doit être définie avant que la broche de sortie du décodeur soit connectée. Dans le cas contraire, la modification n’a aucun effet.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows vista familial Premium, Windows vista édition intégrale, Windows 7 \[ desktop apps uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                      |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl>        |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Sous-types audio**](audio-subtypes.md)
</dt> <dt>

[DirectShow Filtres](directshow-filters.md)
</dt> <dt>

[**Types de supports DVD**](dvd-media-types.md)
</dt> </dl>

 

 
