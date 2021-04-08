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
# <a name="working-with-media-samples"></a><span data-ttu-id="1e27e-103">Utilisation des exemples de supports</span><span class="sxs-lookup"><span data-stu-id="1e27e-103">Working with Media Samples</span></span>

<span data-ttu-id="1e27e-104">Cette rubrique explique comment utiliser l’interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) pour manipuler des exemples d’objets multimédias.</span><span class="sxs-lookup"><span data-stu-id="1e27e-104">This topic describes how to use the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface to manipulate media sample objects.</span></span> <span data-ttu-id="1e27e-105">Pour obtenir une vue d’ensemble générale des exemples de supports, consultez [Media Samples](media-samples.md).</span><span class="sxs-lookup"><span data-stu-id="1e27e-105">For a general overview of media samples, see [Media Samples](media-samples.md).</span></span>

<span data-ttu-id="1e27e-106">Pour créer un nouvel exemple de support, appelez la fonction [**MFCreateSample**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatesample) .</span><span class="sxs-lookup"><span data-stu-id="1e27e-106">To create a new media sample, call the [**MFCreateSample**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatesample) function.</span></span> <span data-ttu-id="1e27e-107">Initialement, la liste de mémoires tampons de l’exemple est vide.</span><span class="sxs-lookup"><span data-stu-id="1e27e-107">Initially, the sample's buffer list is empty.</span></span> <span data-ttu-id="1e27e-108">Pour ajouter une mémoire tampon à la fin de la liste, appelez [**IMFSample :: AddBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer).</span><span class="sxs-lookup"><span data-stu-id="1e27e-108">To add a buffer to the end of the list, call [**IMFSample::AddBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer).</span></span>

<span data-ttu-id="1e27e-109">Le code suivant montre comment créer un exemple et y ajouter une mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="1e27e-109">The following code shows how to create a sample and add a buffer to it.</span></span>


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



<span data-ttu-id="1e27e-110">La méthode recommandée pour récupérer les mémoires tampons à partir de l’exemple consiste à appeler [**IMFSample :: ConvertToContiguousBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-converttocontiguousbuffer).</span><span class="sxs-lookup"><span data-stu-id="1e27e-110">The recommended way to get the buffers from the sample is to call [**IMFSample::ConvertToContiguousBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-converttocontiguousbuffer).</span></span> <span data-ttu-id="1e27e-111">Cette méthode retourne une seule mémoire tampon continguous.</span><span class="sxs-lookup"><span data-stu-id="1e27e-111">This method returns a single continguous buffer.</span></span>

<span data-ttu-id="1e27e-112">Pour itérer au sein des mémoires tampons de la liste, commencez par appeler [**IMFSample :: GetBufferCount**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbuffercount).</span><span class="sxs-lookup"><span data-stu-id="1e27e-112">To iterate through the buffers in the list, start by calling [**IMFSample::GetBufferCount**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbuffercount).</span></span> <span data-ttu-id="1e27e-113">Cette méthode retourne le nombre de mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="1e27e-113">This method returns the number of buffers.</span></span> <span data-ttu-id="1e27e-114">Appelez ensuite [**IMFSample :: GetBufferByIndex**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) et spécifiez l’index de la mémoire tampon à récupérer.</span><span class="sxs-lookup"><span data-stu-id="1e27e-114">Then call [**IMFSample::GetBufferByIndex**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) and specify the index of the buffer to retrieve.</span></span> <span data-ttu-id="1e27e-115">Les mémoires tampons sont indexées à partir de zéro.</span><span class="sxs-lookup"><span data-stu-id="1e27e-115">Buffers are indexed from zero.</span></span>

<span data-ttu-id="1e27e-116">Le code suivant montre comment itérer au sein des mémoires tampons dans un exemple.</span><span class="sxs-lookup"><span data-stu-id="1e27e-116">The following code shows how to iterate through the buffers in a sample.</span></span>


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



<span data-ttu-id="1e27e-117">Les exemples ont un horodatage et une durée.</span><span class="sxs-lookup"><span data-stu-id="1e27e-117">Samples have a time stamp and a duration.</span></span> <span data-ttu-id="1e27e-118">L’horodatage indique le moment où les données de l’exemple doivent être rendues, par rapport à l’horloge de présentation.</span><span class="sxs-lookup"><span data-stu-id="1e27e-118">The time stamp indicates when the data in the sample should be rendered, relative to the presentation clock.</span></span> <span data-ttu-id="1e27e-119">La durée correspond à la durée pendant laquelle les données doivent être rendues.</span><span class="sxs-lookup"><span data-stu-id="1e27e-119">The duration is the length of time for which the data should be rendered.</span></span> <span data-ttu-id="1e27e-120">En général, le composant qui génère les données définit l’horodatage et la durée initiaux.</span><span class="sxs-lookup"><span data-stu-id="1e27e-120">Typically the component that generates the data sets the initial time stamp and duration.</span></span> <span data-ttu-id="1e27e-121">Ces valeurs peuvent être modifiées par la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="1e27e-121">These values might get modified by the Media Session.</span></span> <span data-ttu-id="1e27e-122">Pour définir l’horodatage, appelez [**IMFSample :: SetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampletime).</span><span class="sxs-lookup"><span data-stu-id="1e27e-122">To set the time stamp, call [**IMFSample::SetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampletime).</span></span> <span data-ttu-id="1e27e-123">Pour définir la durée, appelez [**IMFSample :: SetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleduration).</span><span class="sxs-lookup"><span data-stu-id="1e27e-123">To set the duration, call [**IMFSample::SetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleduration).</span></span>

<span data-ttu-id="1e27e-124">Les exemples peuvent également avoir des attributs, qui contiennent des informations supplémentaires sur l’exemple.</span><span class="sxs-lookup"><span data-stu-id="1e27e-124">Samples can also have attributes, which contain additional information about the sample.</span></span> <span data-ttu-id="1e27e-125">Pour obtenir la liste des exemples d’attributs, consultez [exemples d’attributs](sample-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="1e27e-125">For a list of sample attributes, see [Sample Attributes](sample-attributes.md).</span></span> <span data-ttu-id="1e27e-126">Pour définir et récupérer des attributs, utilisez l' [**interface IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes), qui hérite de [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) .</span><span class="sxs-lookup"><span data-stu-id="1e27e-126">To set and retrieve attributes, use the [**IMFAttributes Interface**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes), which [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) inherits.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1e27e-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1e27e-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e27e-128">Exemples de supports</span><span class="sxs-lookup"><span data-stu-id="1e27e-128">Media Samples</span></span>](media-samples.md)
</dt> <dt>

[<span data-ttu-id="1e27e-129">Mémoires tampons de média</span><span class="sxs-lookup"><span data-stu-id="1e27e-129">Media Buffers</span></span>](media-buffers.md)
</dt> </dl>

 

 



