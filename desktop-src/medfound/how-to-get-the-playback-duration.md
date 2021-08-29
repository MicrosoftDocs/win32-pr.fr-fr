---
description: Cette rubrique explique comment obtenir la durée de lecture d’un fichier multimédia à l’aide de MFPlay.
ms.assetid: b1ea4f21-55d1-47b0-b6d3-8951dce79f7c
title: Comment connaître la durée de lecture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c715ae82c63006ef8ad375fa9624cbd65ee5516be2d3e3379e5ca58a2fb5166
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958339"
---
# <a name="how-to-get-the-playback-duration"></a>Comment connaître la durée de lecture

\[MFPlay peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. \]

Cette rubrique explique comment obtenir la durée de lecture d’un fichier multimédia à l’aide de MFPlay.

**Pour connaître la durée de lecture**

1.  Appelez [**IMFPMediaPlayer :: CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) ou [**IMFPMediaPlayer :: CreateMediaItemFromObject**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject) pour créer un élément multimédia pour le fichier.
2.  Appelez [**IMFPMediaItem :: GetDuration**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-getduration). Spécifiez **MFP \_ POSITIONTYPE \_ 100 ns** pour le premier paramètre. La durée est retournée sous la forme d’un **PROPVARIANT** qui contient une valeur **\_ entière importante** . La durée est donnée en unités de 100 nanosecondes.

L’exemple suivant illustre l’étape 2 :


```C++
#include <propvarutil.h>

HRESULT GetPlaybackDuration(IMFPMediaItem *pItem, ULONGLONG *phnsDuration)
{
    PROPVARIANT var;

    HRESULT hr = pItem->GetDuration(MFP_POSITIONTYPE_100NS, &var);

    if (SUCCEEDED(hr))
    {
        hr = PropVariantToUInt64(var, phnsDuration);
        PropVariantClear(&var);
    }

    return hr;
}
```



## <a name="requirements"></a>Configuration requise

MFPlay requiert Windows 7.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de MFPlay pour la lecture audio/vidéo](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



