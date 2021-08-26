---
description: Annulation de l’inscription d’un filtre
ms.assetid: 5459d172-7dfe-4786-bcf2-031e441e30a2
title: Annulation de l’inscription d’un filtre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74e26f2d524ff501fcff1db645c9ccdf1a1c9c80c4056af1af206b996f801207
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049679"
---
# <a name="unregistering-a-filter"></a>Annulation de l’inscription d’un filtre

Pour annuler l’inscription d’un filtre, implémentez la fonction **DllUnregisterServer** . dans cette fonction, appelez la fonction DirectShow [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) avec la valeur **false**. Si vous avez appelé **IFilterMapper2 :: RegisterFilter** lorsque vous avez inscrit le filtre, appelez la méthode [**IFilterMapper2 :: UnregisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-unregisterfilter) ici.

L’exemple suivant montre comment annuler l’inscription d’un filtre :


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



 

 



