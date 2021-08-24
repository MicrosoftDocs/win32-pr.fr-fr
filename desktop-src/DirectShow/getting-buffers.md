---
description: Obtention de mémoires tampons
ms.assetid: be61aee9-41d5-42bc-b905-d0216d301faf
title: Obtention de mémoires tampons
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f727045142b9432da93511ecea1f3238aa24ad213fdc7715f5e2e45a91ab19a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119536899"
---
# <a name="getting-buffers"></a>Obtention de mémoires tampons

Si votre filtre a un allocateur personnalisé qui utilise des ressources de filtre, la méthode [**IMemAllocator :: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) de l’allocateur doit conserver le verrou de diffusion en continu, comme avec les autres méthodes de streaming :


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Threads et sections critiques](threads-and-critical-sections.md)
</dt> </dl>

 

 



