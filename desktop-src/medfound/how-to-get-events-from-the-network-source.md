---
description: Obtention d’événements à partir de la source réseau
ms.assetid: 46869f52-323c-41ec-95f7-e7e5d177b782
title: Obtention d’événements à partir de la source réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 100241b069ae8976c20c68b6055571d5ff1e5c1f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414269"
---
# <a name="how-to-get-events-from-the-network-source"></a>Obtention d’événements à partir de la source réseau

Le programme de résolution source permet à une application de créer une source réseau et d’ouvrir une connexion à une URL spécifique. La source réseau déclenche des événements pour marquer le début et la fin de l’opération asynchrone d’ouverture d’une connexion. Une application peut s’inscrire à ces événements à l’aide de l’interface [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) .

Cette interface expose la méthode [**IMFSourceOpenMonitor :: OnSourceEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) que la source réseau appelle directement lorsqu’elle ouvre l’URL de manière asynchrone. La source réseau avertit l’application lorsqu’elle commence à ouvrir l’URL en déclenchant l’événement [MEConnectStart](meconnectstart.md) . La source réseau déclenche ensuite l’événement [MEConnectEnd](meconnectend.md) lorsqu’il termine l’opération d’ouverture.

> [!Note]  
> Pour envoyer ces événements à l’application, la source réseau n’utilise pas l’interface [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) , car ces événements sont déclenchés avant la création de la source réseau. L’application peut récupérer tous les autres événements de la source réseau à l’aide de l’interface **IMFMediaEventGenerator** de la session de média.

 

## <a name="to-get-events-from-the-network-source"></a>Pour récupérer les événements de la source réseau

1.  Implémentez l’interface [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) . Dans votre implémentation de la méthode [**IMFSourceOpenMonitor :: OnSourceEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) , procédez comme suit :
    1.  Récupérez l’état de l’événement en appelant [**IMFMediaEvent :: GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus). Cette méthode indique si l’opération qui a déclenché l’événement, telle qu’un appel de méthode de programme de résolution source, a réussi. Si l’opération échoue, l’État est un code d’échec.
    2.  Traitez l’événement en fonction du type d’événement : [MEConnectStart](meconnectstart.md) ou [MEConnectEnd](meconnectend.md), que l’application peut recevoir en appelant [**IMFMediaEvent :: GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype).
2.  Configurez une paire clé-valeur dans un objet de magasin de propriétés pour stocker un pointeur vers l’implémentation [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) décrite à l’étape 1.
    1.  Créez un objet de magasin de propriétés en appelant la fonction **PSCreateMemoryPropertyStore** .
    2.  Définissez la propriété [**MFPKEY \_ SourceOpenMonitor**](mfpkey-sourceopenmonitor-property.md) dans une structure **PROPERTYKEY** .
    3.  Fournissez la \_ valeur de données de type inconnu VT dans une structure **PROPVARIANT** en définissant le pointeur **IUnknown** sur l’implémentation de l’interface [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) de l’application.
    4.  Définissez la paire clé-valeur dans la Banque de propriétés en appelant **IPropertyStore :: SetValue**.
3.  Transmettez le pointeur de la Banque de propriétés aux méthodes de résolution source que l’application utilise pour créer la source réseau, par exemple [**IMFSourceResolver :: CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) et d’autres.

## <a name="example"></a>Exemple

L’exemple suivant montre comment implémenter l’interface [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) pour récupérer des événements à partir de la source réseau.


```C++
class CSourceOpenMonitor : public IMFSourceOpenMonitor
{
public:
    CSourceOpenMonitor () : m_cRef(1) { }

    STDMETHODIMP QueryInterface(REFIID riid, void** ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(CSourceOpenMonitor, IMFSourceOpenMonitor),
            { 0 }
        };
        return QISearch(this, qit, riid, ppv);
    }

    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_cRef);
    }

    STDMETHODIMP_(ULONG) Release()
    {
        LONG cRef = InterlockedDecrement(&m_cRef);
        if (cRef == 0)
        {
            delete this;
        }
        // For thread safety, return a temporary variable.
        return cRef;
    }


    STDMETHODIMP OnSourceEvent(IMFMediaEvent* pEvent)
    {
        MediaEventType eventType = MEUnknown;   // Event type
        HRESULT hrStatus = S_OK;                // Event status

        // Get the event type.
        HRESULT hr = pEvent->GetType(&eventType);

        // Get the event status. If the operation that triggered the event
        // did not succeed, the status is a failure code.
        if (SUCCEEDED(hr))
        {
            hr = pEvent->GetStatus(&hrStatus);
        }

        if (FAILED(hrStatus))
        {
            hr = hrStatus;
        }

        if (SUCCEEDED(hr))
        {
            // Switch on the event type.
            switch(eventType)
            {
                case MEConnectStart:
                    // The application does something. (Not shown.)
                    OutputDebugString(L"Connecting...\n");
                    break;

                case MEConnectEnd:
                    // The application does something. (Not shown.)
                    OutputDebugString(L"Connect End.\n");
                    break;
            }
        }
        else
        {
            // Event failed.
            // The application handled a failure. (Not shown.)
        }
        return S_OK;
    }
private:
    long    m_cRef;
};
```



L’exemple suivant montre comment définir la propriété [**MFPKEY \_ SourceOpenMonitor**](mfpkey-sourceopenmonitor-property.md) sur la source réseau lorsque vous ouvrez l’URL :


```C++
HRESULT CreateMediaSourceWithSourceOpenMonitor(
    PCWSTR pszURL, 
    IMFMediaSource **ppSource
    )
{
    IPropertyStore *pConfig = NULL;

    CSourceOpenMonitor *pMonitor = new (std::nothrow) CSourceOpenMonitor();

    if (pMonitor == NULL)
    {
        return E_OUTOFMEMORY;
    }

    // Configure the property store.
    HRESULT hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&pConfig));

    if (SUCCEEDED(hr))
    {
        PROPVARIANT var;
        var.vt = VT_UNKNOWN;
        pMonitor->QueryInterface(IID_PPV_ARGS(&var.punkVal));

        hr = pConfig->SetValue(MFPKEY_SourceOpenMonitor, var);

        PropVariantClear(&var);
    }

    // Create the source media source.
    if (SUCCEEDED(hr))
    {
        hr = CreateMediaSource(pszURL, pConfig, ppSource);
    }

    SafeRelease(&pConfig);
    SafeRelease(&pMonitor);

    return hr;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Mise en réseau dans Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 



