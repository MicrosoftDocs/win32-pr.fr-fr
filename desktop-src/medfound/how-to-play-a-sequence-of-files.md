---
description: Cette rubrique explique comment lire une séquence de fichiers audio/vidéo à l’aide de MFPlay.
ms.assetid: ee16eaa3-0506-4444-b139-f8a8498d6597
title: Comment lire une séquence de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58dc4d1523be4cc6cc09416096af260c9eae736c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106525009"
---
# <a name="how-to-play-a-sequence-of-files"></a>Comment lire une séquence de fichiers

\[MFPlay peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. \]

Cette rubrique explique comment lire une séquence de fichiers audio/vidéo à l’aide de MFPlay.


La rubrique [prise en main avec MFPlay](getting-started-with-mfplay.md) montre comment lire un fichier multimédia unique. Vous pouvez également utiliser MFPlay pour lire une séquence de fichiers.

### <a name="synchronous-blocking-method"></a>Méthode synchrone (blocage)

1.  Appelez la méthode [**IMFPMediaPlayer :: CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) . La méthode crée un élément multimédia.
2.  Appelez [**IMFPMediaPlayer :: SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) pour la mise en file d’attente de l’élément multimédia pour la lecture.
3.  Appelez [**IMFPMediaPlayer ::P poser**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) pour démarrer la lecture.

Ces étapes sont présentées dans le code suivant.


```C++
HRESULT OpenMediaFile(IMFPMediaPlayer *pPlayer, PCWSTR pwszURL)
{
    HRESULT hr = S_OK;
    
    IMFPMediaItem *pItem = NULL;

    hr = pPlayer->CreateMediaItemFromURL(
        sURL, 
        TRUE,  // Blocking call
        0,     // User data.
        &pItem
        );

    if (SUCCEEDED(hr))
    {
        hr = pPlayer->SetMediaItem(pItem);
    }

    if (SUCCEEDED(hr))
    {
       hr = pPlayer->Play();
    }

    if (pItem)
    {
        pItem->Release();
    }
    return hr;
}
```



La méthode [**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) accepte les paramètres suivants :

-   Le premier paramètre est l’URL du fichier.
-   Le deuxième paramètre spécifie si la méthode bloque. Si vous spécifiez la valeur **true**, comme illustré ici, la méthode est bloquée jusqu’à la création de l’élément multimédia.
-   Le troisième paramètre associe une **valeur \_ ptr DWORD** arbitraire à l’élément multimédia. Vous pouvez récupérer cette valeur ultérieurement en appelant [**IMFPMediaItem :: GetUserData**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-getuserdata).
-   Le quatrième paramètre reçoit un pointeur vers l’interface [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) de l’élément multimédia.

### <a name="asynchronous-non-blocking-method"></a>Méthode asynchrone (sans blocage)

Évitez l’option de blocage si vous appelez [**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) à partir de votre thread d’interface utilisateur, car cela peut prendre un certain temps. En général, la méthode ouvre une connexion de fichier ou réseau et lit suffisamment de données pour analyser les en-têtes de fichier, ce qui peut prendre du temps. Par conséquent, il est généralement préférable d’affecter la valeur **false** au second paramètre. Cette option fait en sorte que la méthode s’exécute de façon asynchrone. Lorsque l’option asynchrone est utilisée, le dernier paramètre doit avoir la **valeur null**:


```C++
    hr = pPlayer->CreateMediaItemFromURL(
        sURL, 
        FALSE,  // Non-blocking call.
        0,      // User data.
        NULL    // Must be NULL for the non-blocking call.
        );
```



Lorsque l’élément multimédia est créé, votre application reçoit un événement de **\_ type MFP \_ \_ MEDIAITEM \_ créé** . La structure de données de cet événement contient un pointeur vers l’élément multimédia. Transmettez ce pointeur à la méthode [**SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) pour la mise en file d’attente de l’élément pour la lecture.


```C++
void OnMediaItemCreated(MFP_MEDIAITEM_CREATED_EVENT *pEvent)
{
    HRESULT hr = S_OK;
    if (FAILED(pEvent->header.hrEvent))
    {
        // Handle error. (Not shown.)
    }
    else
    {
        hr = g_pPlayer->SetMediaItem(pEvent->pMediaItem);
    }
}
```



## <a name="requirements"></a>Configuration requise

MFPlay requiert Windows 7.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de MFPlay pour la lecture audio/vidéo](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



