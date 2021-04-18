---
description: Cette rubrique explique comment utiliser des effets audio/video avec MFPlay.
ms.assetid: 90f34bf3-899f-46e0-80c8-af83caa4835d
title: Comment ajouter des effets audio ou vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8d2b02453ce4561ead7fee0d272a07e694e8388
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519654"
---
# <a name="how-to-add-audio-or-video-effects"></a>Comment ajouter des effets audio ou vidéo

\[MFPlay peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. \]

Cette rubrique explique comment utiliser des effets audio/video avec MFPlay.

Pour utiliser un effet avec MFPlay, l’effet doit être implémenté en tant que transformation de Media Foundation (MFT). Pour plus d’informations, consultez [Media Foundation transformations](media-foundation-transforms.md).

**Pour ajouter un effet audio ou vidéo**

1.  Créez une instance de la table MFT qui implémente l’effet.
2.  Appelez [**IMFPMediaPlayer :: InsertEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect).

Appelez [**InsertEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect) avant d’ouvrir le fichier multimédia pour la lecture. MFPlay détermine automatiquement si l’effet est un effet vidéo ou audio.

La méthode [**InsertEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect) prend également un paramètre booléen qui spécifie si l’effet est facultatif ou obligatoire. Si MFPlay ne peut pas ajouter un effet requis (par exemple, parce que le format de flux est incompatible), une erreur de lecture se produit. Dans la plupart des cas, il est préférable de définir un effet comme facultatif.

MFPlay continue à utiliser l’effet pour la lecture suivante. Pour supprimer l’effet, appelez [**IMFPMediaPlayer :: RemoveEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-removeeffect) ou [**IMFPMediaPlayer :: RemoveAllEffects**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-removealleffects).


```C++
HRESULT AddPlaybackEffect(REFGUID clsid, IMFPMediaPlayer *pPlayer)
{
    IMFTransform *pMFT = NULL;

    HRESULT hr = CoCreateInstance(clsid, NULL, CLSCTX_INPROC_SERVER, 
        IID_PPV_ARGS(&pMFT));

    if (SUCCEEDED(hr))
    {
        hr = pPlayer->InsertEffect(pMFT, TRUE); // Set as optional.
    }

    SafeRelease(&pMFT);
    return hr;
}
```



## <a name="requirements"></a>Configuration requise

MFPlay requiert Windows 7.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de MFPlay pour la lecture audio/vidéo](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



