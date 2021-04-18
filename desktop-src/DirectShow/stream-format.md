---
description: Format de flux
ms.assetid: 7ed095f2-b541-4b99-8afc-9acba58081cd
title: Format de flux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75413c28f0871db0168e27685de49fd35b682224
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106542968"
---
# <a name="stream-format"></a><span data-ttu-id="71828-103">Format de flux</span><span class="sxs-lookup"><span data-stu-id="71828-103">Stream Format</span></span>

<span data-ttu-id="71828-104">Les pilotes MSDV et UVC peuvent tous les deux générer deux formats DV : audio entrelacé, vidéo ou vidéo entrelacé.</span><span class="sxs-lookup"><span data-stu-id="71828-104">Both the MSDV and the UVC driver can output two DV formats: interleaved audio-video, or video only.</span></span> <span data-ttu-id="71828-105">Audio entrelacé-vidéo est le format d’origine de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="71828-105">Interleaved audio-video is the original format from the device.</span></span> <span data-ttu-id="71828-106">Le format vidéo uniquement contient les mêmes données, mais les exemples sont marqués comme n’ayant pas de données audio.</span><span class="sxs-lookup"><span data-stu-id="71828-106">The video-only format contains the same data, but the samples are marked as having no audio data.</span></span> <span data-ttu-id="71828-107">Le format vidéo uniquement existe principalement pour la compatibilité avec les applications qui utilisent la vidéo pour Windows.</span><span class="sxs-lookup"><span data-stu-id="71828-107">The video-only format exists mainly for compatibility with applications that use Video for Windows.</span></span> <span data-ttu-id="71828-108">Pour plus d’informations, consultez [type-1 et fichiers AVI DV](type-1-vs--type-2-dv-avi-files.md)type-2.</span><span class="sxs-lookup"><span data-stu-id="71828-108">For more information, see [Type-1 vs. Type-2 DV AVI Files](type-1-vs--type-2-dv-avi-files.md).</span></span>

<span data-ttu-id="71828-109">**Pilote MSDV**</span><span class="sxs-lookup"><span data-stu-id="71828-109">**MSDV Driver**</span></span>

<span data-ttu-id="71828-110">Le pilote MSDV a deux broches de sortie.</span><span class="sxs-lookup"><span data-stu-id="71828-110">The MSDV driver has two output pins.</span></span> <span data-ttu-id="71828-111">La première broche de sortie envoie des données entrelacées, et la deuxième broche de sortie envoie des données vidéo uniquement.</span><span class="sxs-lookup"><span data-stu-id="71828-111">The first output pin sends interleaved data, and the second output pin sends video-only data.</span></span> <span data-ttu-id="71828-112">Une seule broche de sortie peut être connectée à la fois.</span><span class="sxs-lookup"><span data-stu-id="71828-112">Only one output pin can be connected at a time.</span></span> <span data-ttu-id="71828-113">Pour sélectionner un format, connectez la broche de sortie appropriée.</span><span class="sxs-lookup"><span data-stu-id="71828-113">To select a format, connect the appropriate output pin.</span></span> <span data-ttu-id="71828-114">Vous pouvez utiliser l’interface [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) sur la broche de sortie pour rechercher le format.</span><span class="sxs-lookup"><span data-stu-id="71828-114">You can use the [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) interface on the output pin to find the format.</span></span>

<span data-ttu-id="71828-115">**Pilote UVC**</span><span class="sxs-lookup"><span data-stu-id="71828-115">**UVC Driver**</span></span>

<span data-ttu-id="71828-116">Contrairement au pilote MSDV, le pilote UVC remet les deux formats du même code PIN.</span><span class="sxs-lookup"><span data-stu-id="71828-116">Unlike the MSDV driver, the UVC driver delivers both formats from the same pin.</span></span> <span data-ttu-id="71828-117">Le format par défaut est vidéo uniquement.</span><span class="sxs-lookup"><span data-stu-id="71828-117">The default format is video-only.</span></span> <span data-ttu-id="71828-118">Pour sélectionner le format, utilisez l’interface **IAMStreamConfig** sur la broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="71828-118">To select the format, use the **IAMStreamConfig** interface on the output pin.</span></span> <span data-ttu-id="71828-119">Appelez la méthode **GetStreamCaps** pour énumérer les types de média sur la broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="71828-119">Call the **GetStreamCaps** method to enumerate the media types on the output pin.</span></span> <span data-ttu-id="71828-120">Pour chaque type de média, si le type principal correspond au format souhaité, appelez **SetFormat** et transmettez ce type de média.</span><span class="sxs-lookup"><span data-stu-id="71828-120">For each media type, if the major type matches the desired format, call **SetFormat** and pass in that media type.</span></span>



| <span data-ttu-id="71828-121">Format</span><span class="sxs-lookup"><span data-stu-id="71828-121">Format</span></span>                      | <span data-ttu-id="71828-122">Type principal</span><span class="sxs-lookup"><span data-stu-id="71828-122">Major type</span></span>             |
|-----------------------------|------------------------|
| <span data-ttu-id="71828-123">Audio et vidéo entrelacés</span><span class="sxs-lookup"><span data-stu-id="71828-123">Interleaved audio and video</span></span> | <span data-ttu-id="71828-124">MEDIATYPE \_ entrelacé</span><span class="sxs-lookup"><span data-stu-id="71828-124">MEDIATYPE\_Interleaved</span></span> |
| <span data-ttu-id="71828-125">Vidéo uniquement</span><span class="sxs-lookup"><span data-stu-id="71828-125">Video only</span></span>                  | <span data-ttu-id="71828-126">Vidéo de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="71828-126">MEDIATYPE\_Video</span></span>       |



 

<span data-ttu-id="71828-127">La fonction suivante définit le format en fonction du GUID du type principal.</span><span class="sxs-lookup"><span data-stu-id="71828-127">The following function sets the format based on the major type GUID.</span></span>


```C++
HRESULT SetStreamFormat(IAMStreamConfig *pConfig, const GUID& majorType)
{
    if (pConfig == NULL)
    {
        return E_POINTER;
    }

    // Get the number of stream capabilities.
    int count = 0, size = 0;
    HRESULT hr = pConfig->GetNumberOfCapabilities(&count, &size);
    if (FAILED(hr))
    {
        return hr;
    }

    // Allocate memory for the stream capabilities structure.
    BYTE *pCaps = new BYTE[size];
    if (pCaps == NULL)
    {
        return E_OUTOFMEMORY;
    }
    
    // Enumerate the stream capabilities.
    bool bFoundType = false;
    for (int ix = 0; ix < count; ix++)
    {
        AM_MEDIA_TYPE *pmt;
        hr = pConfig->GetStreamCaps(ix, &pmt, pCaps);
        if (FAILED(hr))
        {
            break;
        }
        else if (pmt->majortype == majorType)
        {
            // This is the media type we want.
            bFoundType = true;
            hr = pConfig->SetFormat(pmt);
            DeleteMediaType(pmt);
            break;
        }
        DeleteMediaType(pmt);
    }
    delete [] pCaps;
    if (FAILED(hr))
    {
        return hr;
    }
    return bFoundType ? S_OK : E_FAIL;
}
```



<span data-ttu-id="71828-128">Le pilote MSDV prend également en charge **IAMStreamConfig**. vous pouvez donc écrire du code qui fonctionne pour les deux types d’appareils.</span><span class="sxs-lookup"><span data-stu-id="71828-128">The MSDV driver also supports **IAMStreamConfig**, so you can write code that works for both device types.</span></span>

## <a name="related-topics"></a><span data-ttu-id="71828-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="71828-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71828-130">Contrôle d’un caméscope DV</span><span class="sxs-lookup"><span data-stu-id="71828-130">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



