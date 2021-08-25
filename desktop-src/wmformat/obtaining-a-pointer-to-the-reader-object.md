---
title: obtention d’un pointeur vers l’objet lecteur (kit de développement logiciel (SDK) Windows Media Format 11)
description: en savoir plus sur l’obtention d’un pointeur vers l’objet lecteur du kit de développement logiciel (SDK) Windows Media Format à l’aide de l’interface IWMReaderAdvanced2.
ms.assetid: 70696ffc-2612-460d-b445-f200ba85d3c7
keywords:
- Windows Media Format SDK, DirectShow
- Windows Media Format SDK, Reader, objets
- Windows Media Format SDK, interface IWMReaderAdvanced2
- ASF (Advanced Systems Format), DirectShow
- ASF (format avancé des systèmes), DirectShow
- ASF (Advanced Systems Format), objets Reader
- ASF (format des systèmes avancés), objets lecteur
- ASF (Advanced Systems Format), interface IWMReaderAdvanced2
- ASF (format des systèmes avancés), interface IWMReaderAdvanced2
- DirectShow, objets Reader
- DirectShow, pointeurs vers des objets Reader
- DirectShow, interface IWMReaderAdvanced2
- objets Reader, obtention de pointeurs
- flux, objets lecteur
- flux, pointeurs vers des objets de lecteur
- IWMReaderAdvanced2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e4b2829e56d08825234dcefdc4fb1012f48c894419e7c328f10afeb76cb6c4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808049"
---
# <a name="obtaining-a-pointer-to-the-reader-object-windows-media-format-11-sdk"></a>obtention d’un pointeur vers l’objet lecteur (kit de développement logiciel (SDK) Windows Media Format 11)

dans certains cas, par exemple, lorsque vous déterminez quelles extensions d’unité de données sont définies sur un flux donné, vous devrez peut-être accéder directement à l' [objet lecteur](reader-object.md) du kit de développement logiciel (SDK) de Format multimédia Windows. La fonction suivante montre comment obtenir l’interface [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) sur l’objet lecteur lui-même :


```C++
HRESULT GetReaderAdvanced (IGraphBuilder *pGraph, IWMReaderAdvanced2** pReaderAdvanced2) 
{
  // We use CComPtr's to avoid headaches at cleanup time
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
    // Only the WM ASF Reader will have interface. This filter should be
    // the first one returned in this loop.
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



 

 




