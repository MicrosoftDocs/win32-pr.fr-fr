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
# <a name="unregistering-a-filter"></a>Annulation de l’inscription d’un filtre

Pour annuler l’inscription d’un filtre, implémentez la fonction **DllUnregisterServer** . Dans cette fonction, appelez la fonction DirectShow [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) avec la valeur **false**. Si vous avez appelé **IFilterMapper2 :: RegisterFilter** lorsque vous avez inscrit le filtre, appelez la méthode [**IFilterMapper2 :: UnregisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-unregisterfilter) ici.

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



 

 



