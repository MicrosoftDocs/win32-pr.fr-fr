---
description: Obtention de mémoires tampons
ms.assetid: be61aee9-41d5-42bc-b905-d0216d301faf
title: Obtention de mémoires tampons
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecf516096397eca1fce3a023ee4987d8e8feaa4b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520540"
---
# <a name="getting-buffers"></a><span data-ttu-id="0c525-103">Obtention de mémoires tampons</span><span class="sxs-lookup"><span data-stu-id="0c525-103">Getting Buffers</span></span>

<span data-ttu-id="0c525-104">Si votre filtre a un allocateur personnalisé qui utilise des ressources de filtre, la méthode [**IMemAllocator :: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) de l’allocateur doit conserver le verrou de diffusion en continu, comme avec les autres méthodes de streaming :</span><span class="sxs-lookup"><span data-stu-id="0c525-104">If your filter has a custom allocator that uses filter resources, the allocator's [**IMemAllocator::GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) method should hold the streaming lock, as with other streaming methods:</span></span>


```C++
HRESULT CMyInputAllocator::GetBuffer(
    IMediaSample **ppBuffer,
    REFERENCE_TIME *pStartTime, 
    REFERENCE_TIME *pEndTime,
    DWORD dwFlags)
{
    CAutoLock cObjectLock(&m_csReceive);

    /* Use resources. */

    return CMemAllocator::GetBuffer(ppBuffer, pStartTime, pEndTime, dwFlags);    
}
```



## <a name="related-topics"></a><span data-ttu-id="0c525-105">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0c525-105">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c525-106">Threads et sections critiques</span><span class="sxs-lookup"><span data-stu-id="0c525-106">Threads and Critical Sections</span></span>](threads-and-critical-sections.md)
</dt> </dl>

 

 



