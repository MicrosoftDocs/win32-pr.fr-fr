---
description: Utilisation des exemples de supports
ms.assetid: 10b547b1-6624-4d49-9852-a5fff4eb70e7
title: Utilisation des exemples de supports
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a31fa8ff17c2dabcac9d110b530751d22fdf7b0
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103953352"
---
# <a name="working-with-media-samples"></a>Utilisation des exemples de supports

Cette rubrique explique comment utiliser l’interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) pour manipuler des exemples d’objets multimédias. Pour obtenir une vue d’ensemble générale des exemples de supports, consultez [Media Samples](media-samples.md).

Pour créer un nouvel exemple de support, appelez la fonction [**MFCreateSample**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatesample) . Initialement, la liste de mémoires tampons de l’exemple est vide. Pour ajouter une mémoire tampon à la fin de la liste, appelez [**IMFSample :: AddBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer).

Le code suivant montre comment créer un exemple et y ajouter une mémoire tampon.


```C++
HRESULT CreateMediaSample(DWORD cbData, IMFSample **ppSample)
{
    HRESULT hr = S_OK;

    IMFSample *pSample = NULL;
    IMFMediaBuffer *pBuffer = NULL;

    hr = MFCreateSample(&pSample);

    if (SUCCEEDED(hr))
    {
        hr = MFCreateMemoryBuffer(cbData, &pBuffer);
    }

    if (SUCCEEDED(hr))
    {
        hr = pSample->AddBuffer(pBuffer);
    }

    if (SUCCEEDED(hr))
    {
        *ppSample = pSample;
        (*ppSample)->AddRef();
    }

    SafeRelease(&pSample);
    SafeRelease(&pBuffer);
    return hr;
}
```



La méthode recommandée pour récupérer les mémoires tampons à partir de l’exemple consiste à appeler [**IMFSample :: ConvertToContiguousBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-converttocontiguousbuffer). Cette méthode retourne une seule mémoire tampon continguous.

Pour itérer au sein des mémoires tampons de la liste, commencez par appeler [**IMFSample :: GetBufferCount**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbuffercount). Cette méthode retourne le nombre de mémoires tampons. Appelez ensuite [**IMFSample :: GetBufferByIndex**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) et spécifiez l’index de la mémoire tampon à récupérer. Les mémoires tampons sont indexées à partir de zéro.

Le code suivant montre comment itérer au sein des mémoires tampons dans un exemple.


```C++
IMFMediaBuffer *pBuffer = NULL;
DWORD cBuffers = 0;

hr = pSample->GetBufferCount(&cBuffers);

if (SUCCEEDED(hr))
{
    for (DWORD i = 0; i < cBuffers; i++)
    {
        hr = pSample->GetBufferByIndex(i, &pBuffer);

        // Use buffer (not shown).

        SafeRelease(&pBuffer);

        if (FAILED(hr))
        {
            break;
        }
    }
}
```



Les exemples ont un horodatage et une durée. L’horodatage indique le moment où les données de l’exemple doivent être rendues, par rapport à l’horloge de présentation. La durée correspond à la durée pendant laquelle les données doivent être rendues. En général, le composant qui génère les données définit l’horodatage et la durée initiaux. Ces valeurs peuvent être modifiées par la session multimédia. Pour définir l’horodatage, appelez [**IMFSample :: SetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampletime). Pour définir la durée, appelez [**IMFSample :: SetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleduration).

Les exemples peuvent également avoir des attributs, qui contiennent des informations supplémentaires sur l’exemple. Pour obtenir la liste des exemples d’attributs, consultez [exemples d’attributs](sample-attributes.md). Pour définir et récupérer des attributs, utilisez l' [**interface IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes), qui hérite de [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemples de supports](media-samples.md)
</dt> <dt>

[Mémoires tampons de média](media-buffers.md)
</dt> </dl>

 

 



