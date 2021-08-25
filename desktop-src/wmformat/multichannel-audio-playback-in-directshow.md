---
title: Lecture audio multicanal dans DirectShow
description: Lecture audio multicanal dans DirectShow
ms.assetid: 5123854a-0f1f-40f4-bf57-47622b91103f
keywords:
- Windows Media Format SDK, DirectShow
- Windows Media Format SDK, lecture audio multicanal
- Windows Media Format SDK, lecture audio
- ASF (Advanced Systems Format), DirectShow
- ASF (format avancé des systèmes), DirectShow
- ASF (Advanced Systems Format), lecture audio multicanal
- ASF (format de systèmes avancés), lecture audio multicanal
- ASF (Advanced Systems Format), lecture audio
- ASF (format des systèmes avancés), lecture audio
- DirectShow, lecture audio multicanal
- DirectShow, lecture audio
- audio multicanal, lecture
- lecture audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99734ddf32be6e0340e26fafef0f22f1127ec3652cc0db0a9d2e94ce2f694b96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808159"
---
# <a name="multichannel-audio-playback-in-directshow"></a>Lecture audio multicanal dans DirectShow

pour lire un fichier de Windows Media Audio multicanal dans DirectShow, vous devez définir la propriété " \_ HIRESOUTPUT" directement sur le décodeur après qu’il a été connecté au lecteur ASF WM. Aucune configuration de l’objet lecteur n’est nécessaire. toutefois, pour travailler directement avec l’DMO, vous avez besoin de wmcodecconst. h dans l' [exemple de Code pour utiliser le package de téléchargement des Interfaces Windows Media Audio et vidéo](https://www.microsoft.com/downloads/details.aspx?FamilyId=92490D8A-4F2E-46F1-8835-B1D987B3C985&displaylang=en) .

**Remarque** Cette procédure de configuration est prise en charge uniquement pour les fichiers qui ne sont pas protégés par le Rights Management numérique.

Les étapes de base pour activer la sortie multicanal sont les suivantes :

1.  Appelez RenderFile pour créer le graphique de filtre.
2.  obtenir un pointeur vers le filtre de Wrapper DMO
3.  déconnecter le Wrapper de DMO du convertisseur Audio
4.  Définissez la \_ propriété « HIRESOUTPUT » sur le décodeur.
5.  reconnectez le Wrapper DMO et le convertisseur Audio.
6.  Exécutez le graphique.

Les extraits de code suivants illustrent ces étapes. (Toutes les vérifications d’erreurs ont été omises par souci de simplicité. Si vous utilisez ce code dans une application, vous devez ajouter les routines de gestion des erreurs appropriées.


```C++
    ...
    //ENABLE MULTICHANNEL OUTPUT
    //Render the file
    hr = m_pGraphBuilder->RenderFile(wFileName, NULL);

    // Get pointers to the two DMO Wrapper interfaces we need.
    // (Function bodies provided at the end of this snippet.)
    hr = GetDMOWrapper(pGB, &m_pDMOBaseFilter, &m_pWrapper); 

    //Disconnect the DMO Wrapper from the Audio Renderer
    CComPtr<IPin> pDMOOut;
    CComPtr<IPin> pRendererIn;
    hr = GetPin(m_pDMOBaseFilter, PINDIR_OUTPUT, &pDMOOut);
    hr = pDMOOut->ConnectedTo(&pRendererIn);
    hr = pDMOOut->Disconnect();
    hr = pRendererIn->Disconnect();

    //Set the property on the DMO
    VARIANT varg;
    ::VariantInit(&varg);
    varg.vt    = VT_BOOL;
    varg.boolVal = TRUE;
    CComQIPtr<IMediaObject, &IID_IMediaObject> pMediaObject(m_pWrapper);
    CComQIPtr<IPropertyBag, &IID_IPropertyBag> pPropertyBag(pMediaObject);
    hr = pPropertyBag->Write(g_wszWMACHiResOutput, &varg);

    // Reconnect the DMO Wrapper and the Audio Renderer
    hr = pGB->Connect(pDMOOut, pRendererIn);
    //END MULTICHANNEL (now the graph can be run)
...

```



Les fonctions GetDMOWrapper et GetPin de l’extrait de code précédent sont implémentées comme suit :


```C++
// In this example, the IBaseFilter and IDMOWrapperFilter interfaces are
// declared  at global scope
HRESULT GetDMOWrapper (IFilterGraph *pGraph, IBaseFilter** m_pDMOBaseFilter, IDMOWrapperFilter** m_pWrapper) 
{
    CComPtr<IEnumFilters> pEnum;
    CComPtr<IBaseFilter> pFilter;
    ULONG cFetched;

    HRESULT hr = pGraph->EnumFilters(&pEnum);
    if (FAILED(hr)) return hr;

    while(pEnum->Next(1, &pFilter, &cFetched) == S_OK)
    {
        // If we find the IDMOWrapperFilter interface, that means we 
        // have the DMO Wrapper filter. Store both interfaces for future use.
        CComPtr<IDMOWrapperFilter> pWrapper;
        hr = pFilter->QueryInterface(IID_IDMOWrapperFilter, (void**) &pWrapper);
        if (SUCCEEDED(hr))
        {
            *m_pWrapper = pWrapper.Detach();
            *m_pDMOBaseFilter = pFilter.Detach();
            return S_OK;
        }

        pFilter.Release();
    }

    return E_FAIL;
}

HRESULT GetPin(IBaseFilter *pFilter, PIN_DIRECTION PinDir, IPin** ppPin)
{
    CComPtr<IEnumPins>  pEnum;
    CComPtr<IPin>       pPin;

         HRESULT hr = pFilter->EnumPins(&pEnum);
    if (FAILED(hr))
    {
        return hr;
    }
    while(pEnum->Next(1, &pPin, 0) == S_OK)
    {
        PIN_DIRECTION PinDirThis;
        pPin->QueryDirection(&PinDirThis);
        if (PinDir == PinDirThis)
        {
            *ppPin = pPin.Detach();
            return S_OK;
        }
        pPin.Release();
    }
    
    return E_FAIL;
}
```



 

 




