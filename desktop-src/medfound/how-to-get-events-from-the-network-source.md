---
description: Obtention d’événements à partir de la source réseau
ms.assetid: 46869f52-323c-41ec-95f7-e7e5d177b782
title: Obtention d’événements à partir de la source réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 100241b069ae8976c20c68b6055571d5ff1e5c1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753581"
---
# <a name="how-to-get-events-from-the-network-source"></a><span data-ttu-id="af193-103">Obtention d’événements à partir de la source réseau</span><span class="sxs-lookup"><span data-stu-id="af193-103">How to Get Events from the Network Source</span></span>

<span data-ttu-id="af193-104">Le programme de résolution source permet à une application de créer une source réseau et d’ouvrir une connexion à une URL spécifique.</span><span class="sxs-lookup"><span data-stu-id="af193-104">The source resolver enables an application to create a network source and open a connection to a specific URL.</span></span> <span data-ttu-id="af193-105">La source réseau déclenche des événements pour marquer le début et la fin de l’opération asynchrone d’ouverture d’une connexion.</span><span class="sxs-lookup"><span data-stu-id="af193-105">The network source raises events to mark the beginning and the end of the asynchronous operation of opening a connection.</span></span> <span data-ttu-id="af193-106">Une application peut s’inscrire à ces événements à l’aide de l’interface [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) .</span><span class="sxs-lookup"><span data-stu-id="af193-106">An application can register for these events by using the [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) interface.</span></span>

<span data-ttu-id="af193-107">Cette interface expose la méthode [**IMFSourceOpenMonitor :: OnSourceEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) que la source réseau appelle directement lorsqu’elle ouvre l’URL de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="af193-107">This interface exposes the [**IMFSourceOpenMonitor::OnSourceEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) method that the network source calls directly when it opens the URL asynchronously.</span></span> <span data-ttu-id="af193-108">La source réseau avertit l’application lorsqu’elle commence à ouvrir l’URL en déclenchant l’événement [MEConnectStart](meconnectstart.md) .</span><span class="sxs-lookup"><span data-stu-id="af193-108">The network source notifies the application when it starts opening the URL by raising the [MEConnectStart](meconnectstart.md) event.</span></span> <span data-ttu-id="af193-109">La source réseau déclenche ensuite l’événement [MEConnectEnd](meconnectend.md) lorsqu’il termine l’opération d’ouverture.</span><span class="sxs-lookup"><span data-stu-id="af193-109">The network source then raises the [MEConnectEnd](meconnectend.md) event when it completes the open operation.</span></span>

> [!Note]  
> <span data-ttu-id="af193-110">Pour envoyer ces événements à l’application, la source réseau n’utilise pas l’interface [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) , car ces événements sont déclenchés avant la création de la source réseau.</span><span class="sxs-lookup"><span data-stu-id="af193-110">To send these events to the application, the network source does not use the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface because these events are raised before the network source is created.</span></span> <span data-ttu-id="af193-111">L’application peut récupérer tous les autres événements de la source réseau à l’aide de l’interface **IMFMediaEventGenerator** de la session de média.</span><span class="sxs-lookup"><span data-stu-id="af193-111">The application can get all other network source events by using the Media Session's **IMFMediaEventGenerator** interface.</span></span>

 

## <a name="to-get-events-from-the-network-source"></a><span data-ttu-id="af193-112">Pour récupérer les événements de la source réseau</span><span class="sxs-lookup"><span data-stu-id="af193-112">To get events from the network source</span></span>

1.  <span data-ttu-id="af193-113">Implémentez l’interface [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) .</span><span class="sxs-lookup"><span data-stu-id="af193-113">Implement the [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) interface.</span></span> <span data-ttu-id="af193-114">Dans votre implémentation de la méthode [**IMFSourceOpenMonitor :: OnSourceEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) , procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="af193-114">In your implementation of [**IMFSourceOpenMonitor::OnSourceEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) method, do the following:</span></span>
    1.  <span data-ttu-id="af193-115">Récupérez l’état de l’événement en appelant [**IMFMediaEvent :: GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus).</span><span class="sxs-lookup"><span data-stu-id="af193-115">Get the event status by calling [**IMFMediaEvent::GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus).</span></span> <span data-ttu-id="af193-116">Cette méthode indique si l’opération qui a déclenché l’événement, telle qu’un appel de méthode de programme de résolution source, a réussi.</span><span class="sxs-lookup"><span data-stu-id="af193-116">This method indicates whether the operation that triggered the event, such as a source resolver method call, succeeded.</span></span> <span data-ttu-id="af193-117">Si l’opération échoue, l’État est un code d’échec.</span><span class="sxs-lookup"><span data-stu-id="af193-117">If the operation is not successful, the status is a failure code.</span></span>
    2.  <span data-ttu-id="af193-118">Traitez l’événement en fonction du type d’événement : [MEConnectStart](meconnectstart.md) ou [MEConnectEnd](meconnectend.md), que l’application peut recevoir en appelant [**IMFMediaEvent :: GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype).</span><span class="sxs-lookup"><span data-stu-id="af193-118">Process the event based on the event type: [MEConnectStart](meconnectstart.md) or [MEConnectEnd](meconnectend.md), which the application can get by calling [**IMFMediaEvent::GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype).</span></span>
2.  <span data-ttu-id="af193-119">Configurez une paire clé-valeur dans un objet de magasin de propriétés pour stocker un pointeur vers l’implémentation [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) décrite à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="af193-119">Configure a key-value pair in a property store object to store a pointer to the [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) implementation described in step 1.</span></span>
    1.  <span data-ttu-id="af193-120">Créez un objet de magasin de propriétés en appelant la fonction **PSCreateMemoryPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="af193-120">Create a property store object by calling the **PSCreateMemoryPropertyStore** function.</span></span>
    2.  <span data-ttu-id="af193-121">Définissez la propriété [**MFPKEY \_ SourceOpenMonitor**](mfpkey-sourceopenmonitor-property.md) dans une structure **PROPERTYKEY** .</span><span class="sxs-lookup"><span data-stu-id="af193-121">Set the [**MFPKEY\_SourceOpenMonitor**](mfpkey-sourceopenmonitor-property.md) property in a **PROPERTYKEY** structure.</span></span>
    3.  <span data-ttu-id="af193-122">Fournissez la \_ valeur de données de type inconnu VT dans une structure **PROPVARIANT** en définissant le pointeur **IUnknown** sur l’implémentation de l’interface [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) de l’application.</span><span class="sxs-lookup"><span data-stu-id="af193-122">Provide the VT\_UNKNOWN type data value in a **PROPVARIANT** structure by setting the **IUnknown** pointer to the application's implementation of the [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) interface.</span></span>
    4.  <span data-ttu-id="af193-123">Définissez la paire clé-valeur dans la Banque de propriétés en appelant **IPropertyStore :: SetValue**.</span><span class="sxs-lookup"><span data-stu-id="af193-123">Set the key-value pair in the property store by calling **IPropertyStore::SetValue**.</span></span>
3.  <span data-ttu-id="af193-124">Transmettez le pointeur de la Banque de propriétés aux méthodes de résolution source que l’application utilise pour créer la source réseau, par exemple [**IMFSourceResolver :: CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) et d’autres.</span><span class="sxs-lookup"><span data-stu-id="af193-124">Pass the property store pointer to the source resolver methods that the application is using to create the network source, such as [**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) and others.</span></span>

## <a name="example"></a><span data-ttu-id="af193-125">Exemple</span><span class="sxs-lookup"><span data-stu-id="af193-125">Example</span></span>

<span data-ttu-id="af193-126">L’exemple suivant montre comment implémenter l’interface [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) pour récupérer des événements à partir de la source réseau.</span><span class="sxs-lookup"><span data-stu-id="af193-126">The following example shows how to implement the [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) interface to get events from the network source.</span></span>


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



<span data-ttu-id="af193-127">L’exemple suivant montre comment définir la propriété [**MFPKEY \_ SourceOpenMonitor**](mfpkey-sourceopenmonitor-property.md) sur la source réseau lorsque vous ouvrez l’URL :</span><span class="sxs-lookup"><span data-stu-id="af193-127">The following example shows how to set the [**MFPKEY\_SourceOpenMonitor**](mfpkey-sourceopenmonitor-property.md) property on the network source when you open the URL:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="af193-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="af193-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af193-129">Mise en réseau dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="af193-129">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 



