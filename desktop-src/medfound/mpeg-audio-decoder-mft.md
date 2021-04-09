---
description: Le décodeur audio Microsoft MPEG est une transformation de Media Foundation synchrone (MFT) qui permet de décoder des formats de flux élémentaires MPEG Audio à l’aide du pipeline Media Foundation (MF).
ms.assetid: 29A0491D-CA0D-4909-96F0-5640D5EE77F9
title: Décodeur audio MPEG
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a98106ce4610c7c89a5e6212c225fd8eca3e4526
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951483"
---
# <a name="mpeg-audio-decoder"></a>Décodeur audio MPEG

Le décodeur audio Microsoft MPEG est une [transformation de Media Foundation](media-foundation-transforms.md) synchrone (MFT) qui permet de décoder des formats de flux élémentaires MPEG Audio à l’aide du pipeline Media Foundation (MF).

Le décodeur prend en charge les formats de flux élémentaires MPEG suivants.

-   MPEG-1 audio Layers I et II (ISO/IEC 11172-3). 2. MPEG-2 à compatibilité descendante, couches I et II (ISO

-   MPEG-2 à compatibilité descendante, couches I et II (ISO/IEC 13818-3), mono et stéréo uniquement

## <a name="class-identifier"></a>Identificateur de classe

L’identificateur de classe (CLSID) du décodeur audio MPEG est **CLSID \_ MSMPEGAudDecMFT**, défini dans le fichier d’en-tête wmcodecdsp. h.

## <a name="input-media-types"></a>Types de médias d’entrée

Le décodeur audio MPEG prend en charge les attributs de type de média d’entrée suivants.



| Attribut                                                                               | Valeur                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_type de \_ majeurese MF MT \_**](mf-mt-major-type-attribute.md)                               | **MFMediaType \_ audio**                                                                                                                                                                                                                                                |
| [**\_sous- \_ type MF MT**](mf-mt-subtype-attribute.md)                                      | **\_MPEG MFAudioFormat**                                                                                                                                                                                                                                               |
| [**\_canaux de \_ \_ numéros audio MF MT \_**](mf-mt-audio-num-channels-attribute.md)              | Facultatif Habituellement 1 pour mono ou 2 pour stéréo, il peut y avoir jusqu’à 6 canaux.<br/>                                                                                                                                                                                |
| [**\_masque de \_ \_ canal audio MF MT \_**](mf-mt-audio-channel-mask-attribute.md)              | Facultatif En général, 0x4 pour mono ou 0x3 pour stéréo, mais peut également être l’un des masques de canal associés à 6 canaux (3/2/1, 3/2, 3/1, 2/2, 2/1). Si elle est présente, le masque de canal doit être cohérent avec le nombre d’entrée spécifié de canaux.<br/> |
| [**\_ \_ échantillons audio MF \_ MT \_ par \_ seconde**](mf-mt-audio-samples-per-second-attribute.md) | Facultatif L’un des éléments suivants : 16000, 22050, 24000, 32000, 44100, 48000. S’il est spécifié, le taux d’échantillonnage d’entrée doit être l’un des taux d’échantillonnage MPEG valides.<br/>                                                                                             |



 

## <a name="output-media-types"></a>Types de médias de sortie

Le décodeur audio MPEG prend en charge jusqu’à quatre sous-types de médias de sortie, dans l’ordre suivant.

<dl> 1. Stéréo, virgule flottante.  
2. Stéréo, PCM 16 bits.  
3. Mono, à virgule flottante (uniquement si l’entrée est mono ou double mono).  
4. Mono, PCM 16 bits (uniquement si l’entrée est mono ou double mono).  
</dl>

Le décodeur prend toujours en charge la sortie stéréo et il est énuméré comme premier type de média de sortie.

Le décodeur prend en charge les attributs de type de média de sortie suivants.



| Attribut                                                                           | Valeur                                                                      |
|-------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [\_type de \_ majeurese MF MT \_](mf-mt-major-type-attribute.md)                               | **MFMediaType \_ audio**                                                     |
| [\_sous- \_ type MF MT](mf-mt-subtype-attribute.md)                                      | **MFAudioFormat \_ PCM** ou **MFAudioFormat \_ float**                  |
| [\_bits de \_ sortie audio MF \_ \_ par \_ échantillon](mf-mt-audio-bits-per-sample-attribute.md)       | 16 ou 32                                                                   |
| [\_canaux de \_ \_ numéros audio MF MT \_](mf-mt-audio-num-channels-attribute.md)              | 1 ou 2                                                                     |
| [\_masque de \_ \_ canal audio MF MT \_](mf-mt-audio-channel-mask-attribute.md)              | 0x4 pour mono ou 0x3 pour stéréo                                             |
| [\_ \_ échantillons audio MF \_ MT \_ par \_ seconde](mf-mt-audio-samples-per-second-attribute.md) | L’un des éléments suivants : 16000, 22050, 24000, 32000, 44100, 48000.<br/> |



 

## <a name="transform-attributes"></a>Attributs de transformation

Le décodeur audio MPEG implémente la méthode [**IMFTransform :: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) . Les applications peuvent utiliser cette méthode pour récupérer ou définir les attributs suivants.



| Attribut                                                                               | Description                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CODECAPI \_ AVDecAudioDualMono**](../directshow/avdecaudiodualmono-property.md)                   | Spécifie si le contenu audio à 2 canaux en cours de décodage est double mono ou non. Lecture seule. Défini par la table MFT. Pour plus d’informations, consultez [**eAVDecAudioDualMono**](/windows/win32/api/codecapi/ne-codecapi-eavdecaudiodualmono).                                                                                                                               |
| [**CODECAPI \_ AVDecAudioDualMonoReproMode**](../directshow/avdecaudiodualmonorepromode-property.md) | Spécifie comment le décodeur reproduit un double audio mono. La valeur par défaut **est \_ eAVDecAudioDualMonoReproMode \_ mono gauche**.<br/> Lecture/écriture. Les applications peuvent définir cette propriété pour modifier le comportement par défaut. Pour plus d’informations, consultez [**eAVDecAudioDualMono**](/windows/win32/api/codecapi/ne-codecapi-eavdecaudiodualmono).<br/> |
| [**CODECAPI \_ AVEncCommonMeanBitRate**](../directshow/avenccommonmeanbitrate-property.md)           | Spécifie la vitesse de transmission de flux compressée. Lecture seule. Défini par la table MFT.                                                                                                                                                                                                                                         |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Objets codec](codecobjects.md)
</dt> </dl>

 

 
