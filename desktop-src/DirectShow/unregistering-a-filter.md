---
description: Annulation de l’inscription d’un filtre
ms.assetid: 5459d172-7dfe-4786-bcf2-031e441e30a2
title: Annulation de l’inscription d’un filtre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d161b7d1f169b84ba43ac734bf01708a37eb700a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866465"
---
# <a name="unregistering-a-filter"></a><span data-ttu-id="a1ed6-103">Annulation de l’inscription d’un filtre</span><span class="sxs-lookup"><span data-stu-id="a1ed6-103">Unregistering a Filter</span></span>

<span data-ttu-id="a1ed6-104">Pour annuler l’inscription d’un filtre, implémentez la fonction **DllUnregisterServer** .</span><span class="sxs-lookup"><span data-stu-id="a1ed6-104">To unregister a filter, implement the **DllUnregisterServer** function.</span></span> <span data-ttu-id="a1ed6-105">Dans cette fonction, appelez la fonction DirectShow [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) avec la valeur **false**.</span><span class="sxs-lookup"><span data-stu-id="a1ed6-105">Within this function, call the DirectShow [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) function with a value of **FALSE**.</span></span> <span data-ttu-id="a1ed6-106">Si vous avez appelé **IFilterMapper2 :: RegisterFilter** lorsque vous avez inscrit le filtre, appelez la méthode [**IFilterMapper2 :: UnregisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-unregisterfilter) ici.</span><span class="sxs-lookup"><span data-stu-id="a1ed6-106">If you called **IFilterMapper2::RegisterFilter** when you registered the filter, call the [**IFilterMapper2::UnregisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-unregisterfilter) method here.</span></span>

<span data-ttu-id="a1ed6-107">L’exemple suivant montre comment annuler l’inscription d’un filtre :</span><span class="sxs-lookup"><span data-stu-id="a1ed6-107">The following example shows how to unregister a filter:</span></span>


```C++
STDAPI DllUnregisterServer()
{
    HRESULT hr;
    IFilterMapper2 *pFM2 = NULL;

    hr = AMovieDllRegisterServer2(FALSE);
    if (FAILED(hr))
        return hr;
 
    hr = CoCreateInstance(CLSID_FilterMapper2, NULL, CLSCTX_INPROC_SERVER,
            IID_IFilterMapper2, (void **)&pFM2);

    if (FAILED(hr))
        return hr;

    hr = pFM2->UnregisterFilter(&CLSID_VideoCompressorCategory, 
            g_wszName, CLSID_SomeFilter);

    pFM2->Release();
    return hr;
}
```



 

 



