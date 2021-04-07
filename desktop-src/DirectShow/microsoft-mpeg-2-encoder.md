---
description: Le filtre d’encodeur Microsoft MPEG-2 encode le contenu audio et vidéo MPEG-2 et multiplexe les flux pour générer un flux de données de programme MPEG-2 ou un flux de transport.
ms.assetid: 61e8918b-7f5a-4720-bb3b-df9ac7614894
title: Encodeur Microsoft MPEG-2 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef5fad3b316db9ac4e47efcb9de761227cdd3279
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745965"
---
# <a name="microsoft-mpeg-2-encoder"></a>Encodeur Microsoft MPEG-2

Le filtre d’encodeur Microsoft MPEG-2 encode le contenu audio et vidéo MPEG-2 et multiplexe les flux pour générer un flux de données de programme MPEG-2 ou un flux de transport.

> [!Note]  
> Ce filtre n’est pas pris en charge sur les plateformes IA-64.

 



Informations de filtre

Interfaces de filtre

[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> **IEncoderAPI**<br/> [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**IVideoEncoder**](/windows/win32/api/strmif/nn-strmif-ivideoencoder)<br/>

Types de média de broche d’entrée

Voir les notes

Interfaces pin d’entrée

[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Types de média de broche de sortie

Voir les notes

Interfaces de broche de sortie

[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

CLSID du filtre

**CLSID \_ CMPEG2EncoderDS** (déclaré dans wmcodecdsp. h)

Exécutable

msmpeg2enc.dll

[Mérite](merit.md)

**MÉRITE \_ n' \_ \_ utilise pas**

[Catégorie de filtre](filter-categories.md)

**CLSID \_ LegacyAmFilterCategory**



 

## <a name="remarks"></a>Notes

Ce filtre combine la fonctionnalité d’encodage de deux autres filtres :

-   [**Encodeur audio Microsoft MPEG-2**](microsoft-mpeg-2-audio-encoder.md)
-   [**Encodeur vidéo Microsoft MPEG-2**](microsoft-mpeg-2-video-encoder.md)

Sauf indication contraire, ce filtre prend en charge les mêmes fonctionnalités d’encodage que ces deux encodeurs.

Initialement, le filtre a une seule broche d’entrée, qui peut accepter les entrées audio ou vidéo. Lorsque ce code PIN est connecté, le filtre crée une deuxième broche d’entrée. Si la première broche d’entrée reçoit du son, la deuxième broche d’entrée n’accepte que la vidéo, et vice versa. Chaque broche d’entrée prend en charge les mêmes types de supports que le filtre d’encodeur correspondant.

Si une seule broche d’entrée est connectée, le filtre prend en charge les mêmes types de sortie que l’encodeur audio ou vidéo correspondant. Si les deux broches sont connectées, le filtre prend en charge les types de sortie suivants :

-   Audio-Visual dans un flux de programme MPEG-2
-   Audio-visuel dans un flux de transport MPEG-2

Elles correspondent aux types de sortie suivants :

-   **MediaType \_ Stream**, **\_ \_ programme MEDIASUBTYPE MPEG2**
-   **MediaType \_ Flux**, **\_ \_ transport MEDIASUBTYPE MPEG2**

Ce filtre ne peut pas multiplexer les flux qui ont été précédemment encodés. Les flux d’entrée doivent être des données audio/vidéo non compressées, que le filtre encode avant le multiplexage. Le flux multiplexé est limité à un programme, contenant jusqu’à un audio et un flux vidéo.

### <a name="codec-properties"></a>Propriétés du codec

Le filtre prend en charge les propriétés combinées des filtres d’encodeur [**audio MPEG-2**](microsoft-mpeg-2-audio-encoder.md) et d' [**encodeur vidéo MPEG-2**](microsoft-mpeg-2-video-encoder.md) , à la différence suivante :

-   La propriété [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md) définit la vitesse de transmission moyenne du flux vidéo.
-   La propriété [**AVEncAudioMeanBitRate**](avencaudiomeanbitrate.md) définit la vitesse de transmission moyenne du flux audio.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista Édition familiale Premium, Windows Vista Édition intégrale, Windows 7 Édition familiale Premium, Windows 7 professionnel, Windows 7 entreprise, applications de bureau Windows 7 édition intégrale \[ uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                                                                                     |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl>                                                                                       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Filtres DirectShow](directshow-filters.md)
</dt> </dl>

 

 
