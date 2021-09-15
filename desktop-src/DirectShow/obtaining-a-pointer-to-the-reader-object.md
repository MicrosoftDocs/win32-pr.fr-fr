---
description: en savoir plus sur l’obtention d’un pointeur vers l’objet lecteur de Windows Media Format SDK à l’aide de l’interface IWMReaderAdvanced2 dans DirectShow.
ms.assetid: d1292e2f-bd0e-4961-a6fa-8cdaeb28b692
title: Obtention d’un pointeur vers l’objet lecteur (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e131b9e111aa5e779d1208b68e04c9979e3b1d7f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127312373"
---
# <a name="obtaining-a-pointer-to-the-reader-object-directshow"></a>Obtention d’un pointeur vers l’objet lecteur (DirectShow)

dans certains cas, par exemple, lorsque vous déterminez quelles extensions d’unité de données sont définies sur un flux donné, vous devrez peut-être accéder directement à l’objet lecteur du kit de développement logiciel (SDK) de Format multimédia Windows. La fonction suivante montre comment obtenir l’interface [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) sur l’objet lecteur lui-même :


```C++
#include <wmsdk.h>
HRESULT GetReaderAdvanced(IGraphBuilder *pGraph, IWMReaderAdvanced2** pReaderAdvanced2) 
{
  CComPtr<IEnumFilters> pEnum;
  CComPtr<IBaseFilter> pFilter;
  ULONG cFetched;

  HRESULT hr = pGraph->EnumFilters(&pEnum);
  if (FAILED(hr)) 
  {
    return hr;
  }

  while(pEnum->Next(1, &pFilter, &cFetched) == S_OK)
  {
    IWMHeaderInfo *pHI = NULL;
    // Only the WM ASF Reader will have interface. 
    hr = pFilter->QueryInterface(__uuidof(IWMHeaderInfo), (void**)&pHI);
    if (SUCCEEDED(hr))
    {
      // We use the IWMDRMReader interface only as a way to get
      // a pointer to the Reader Object.
      CComPtr<IWMDRMReader> pWMDRMReader;
      CComQIPtr<IServiceProvider, &IID_IServiceProvider> pSP;
      hr = pHI->QueryInterface(__uuidof(IServiceProvider), (void**)&pSP);
      if (!pSP)
      {
        return E_NOINTERFACE;
      }
      
      hr = pSP->QueryService(IID_IWMDRMReader, IID_IWMDRMReader, (void **) &pWMDRMReader);
      if (FAILED(hr))
      {
        return hr;
      }

      CComQIPtr<IWMReaderAdvanced2, &IID_IWMReaderAdvanced2> pRA2(pWMDRMReader);
      if (pRA2)
      {
        *pReaderAdvanced2 = pRA2.Detach();
        return S_OK;
      }

    }
    pFilter.Release();
  }
  
  //if we get here, we didn't find the WM ASF Reader
  return E_FAIL;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Lecture des fichiers ASF dans DirectShow](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 
