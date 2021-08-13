---
description: Utilisation des mémoires tampons de média
ms.assetid: c7e079e0-99f3-4bff-9163-1c5a022c14ae
title: Utilisation des mémoires tampons de média (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c559e54d38c5a601a51bf3d6a879cbfe5b8403e1df48117e15d23f6264554437
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118736610"
---
# <a name="working-with-media-buffers-microsoft-media-foundation"></a>Utilisation des mémoires tampons de média (Microsoft Media Foundation)

Cette rubrique explique comment utiliser l’interface [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) pour accéder aux données dans une mémoire tampon de média. Toutes les mémoires tampons de média exposent **IMFMediaBuffer**, qui est conçu pour tout type de données. Les images vidéo non compressées sont un cas particulier, décrit dans la rubrique [mémoires tampons vidéo non compressées](uncompressed-video-buffers.md).

## <a name="buffer-size"></a>Taille de la mémoire tampon

Une mémoire tampon de support est associée à deux tailles :

-   La *longueur maximale* est la taille physique de la mémoire allouée pour la mémoire tampon. Cette valeur est définie lorsque la mémoire tampon est créée et ne change pas pendant la durée de vie de la mémoire tampon. La longueur maximale indique la quantité de données pouvant être stockées dans la mémoire tampon. Pour trouver la taille maximale, appelez [**IMFMediaBuffer :: GetMaxLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getmaxlength).

-   La *longueur actuelle* correspond à la quantité de données valides actuellement dans la mémoire tampon. Lorsque la mémoire tampon est allouée pour la première fois, la longueur actuelle est égale à zéro, car il n’y a pas de données valides dans la mémoire tampon. Si vous écrivez des données dans la mémoire tampon, vous devez mettre à jour la longueur actuelle en appelant [**IMFMediaBuffer :: SetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength). Par exemple, si vous écrivez 100 octets de données dans la mémoire tampon, appelez **SetCurrentLength** avec la valeur 100. Si vous lisez des données à partir d’une mémoire tampon de média, appelez [**IMFMediaBuffer :: GetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getcurrentlength) pour connaître la quantité de données actuellement dans la mémoire tampon. Ne pas lire au-delà de la longueur actuelle. La longueur actuelle ne peut jamais dépasser la longueur maximale de la mémoire tampon.

## <a name="accessing-the-buffer-memory"></a>Accès à la mémoire tampon

Pour accéder à la mémoire dans la mémoire tampon, appelez [**IMFMediaBuffer :: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock). Cette méthode retourne un pointeur vers le début du bloc de mémoire. Elle retourne également la longueur maximale et la longueur actuelle. Quand vous avez fini d’utiliser le pointeur, appelez [**IMFMediaBuffer :: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock).

Pour écrire des données dans une mémoire tampon de média :

1.  Appelez [**IMFMediaBuffer :: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) pour obtenir un pointeur vers la mémoire. La méthode retourne également la longueur maximale de la mémoire tampon.
2.  Écrivez vos données dans la mémoire, jusqu’à la longueur maximale de la mémoire tampon.
3.  Appelez [**IMFMediaBuffer :: SetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength) pour mettre à jour la longueur actuelle. Définissez la longueur actuelle égale à la quantité de données que vous avez écrites à l’étape 2.
4.  Appelez [**IMFMediaBuffer :: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) pour déverrouiller la mémoire tampon.

Pour lire des données à partir d’une mémoire tampon de média :

1.  Appelez [**IMFMediaBuffer :: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) pour obtenir un pointeur vers la mémoire. La méthode retourne également la longueur actuelle de la mémoire tampon (la quantité de données valides dans la mémoire tampon).
2.  Lire le contenu de la mémoire, jusqu’à la longueur actuelle.
3.  Appelez [**IMFMediaBuffer :: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) pour déverrouiller la mémoire tampon.

## <a name="creating-system-memory-buffers"></a>Création de mémoires tampons système

La mémoire tampon système est une mémoire tampon de média qui gère un bloc de mémoire système. Pour créer une instance de cet objet, appelez [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) ou [**MFCreateAlignedMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatealignedmemorybuffer) et spécifiez une taille de mémoire tampon. Les deux fonctions allouent un bloc de mémoire et retournent un pointeur [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) . La mémoire est automatiquement libérée lorsque le nombre de références de la mémoire tampon du média atteint zéro et que l’objet est détruit.

L’exemple suivant montre comment créer une mémoire tampon système et écrire dans la mémoire tampon.


```C++
HRESULT CreateSystemMemoryBuffer(
    BYTE *pSrc, 
    DWORD cbData, 
    IMFMediaBuffer **ppBuffer
    )
{
    HRESULT hr = S_OK;
    BYTE *pData = NULL;

    IMFMediaBuffer *pBuffer = NULL;

    // Create the media buffer.
    hr = MFCreateMemoryBuffer(
        cbData,   // Amount of memory to allocate, in bytes.
        &pBuffer        
        );

    // Lock the buffer to get a pointer to the memory.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->Lock(&pData, NULL, NULL);
    }

    if (SUCCEEDED(hr))
    {
        memcpy_s(pData, cbData, pSrc, cbData);
    }

    // Update the current length.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->SetCurrentLength(cbData);
    }

    // Unlock the buffer.
    if (pData)
    {
        hr = pBuffer->Unlock();
    }

    if (SUCCEEDED(hr))
    {
        *ppBuffer = pBuffer;
        (*ppBuffer)->AddRef();
    }

    return hr;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Mémoires tampons de média](media-buffers.md)
</dt> <dt>

[API de plateforme Media Foundation](media-foundation-platform-apis.md)
</dt> </dl>

 

 



