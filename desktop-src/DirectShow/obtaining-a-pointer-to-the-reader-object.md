---
description: Obtention d’un pointeur vers l’objet lecteur
ms.assetid: d1292e2f-bd0e-4961-a6fa-8cdaeb28b692
title: Obtention d’un pointeur vers l’objet lecteur (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3be22a22581c8f262ac4c6898271ebccb53a0e4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745597"
---
# <a name="obtaining-a-pointer-to-the-reader-object-directshow"></a><span data-ttu-id="afeae-103">Obtention d’un pointeur vers l’objet lecteur (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="afeae-103">Obtaining a Pointer to the Reader Object (DirectShow)</span></span>

<span data-ttu-id="afeae-104">Dans certains cas, par exemple, lorsque vous déterminez quelles extensions d’unité de données sont définies sur un flux donné, vous devrez peut-être accéder directement à l’objet lecteur du kit de développement logiciel (SDK) du format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="afeae-104">In certain cases, for example when determining which data unit extensions are set on a given stream, you may need to access the Reader Object of the Windows Media Format SDK directly.</span></span> <span data-ttu-id="afeae-105">La fonction suivante montre comment obtenir l’interface [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) sur l’objet lecteur lui-même :</span><span class="sxs-lookup"><span data-stu-id="afeae-105">The following function shows how to obtain the [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) interface on the Reader Object itself:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="afeae-106">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="afeae-106">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="afeae-107">Lecture de fichiers ASF dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="afeae-107">Reading ASF Files in DirectShow</span></span>](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 
