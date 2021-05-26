---
description: Appel des méthodes de service de façon asynchrone
ms.assetid: d3072e34-65f2-4eeb-bcfa-e2db2d34e680
title: Appel des méthodes de service de façon asynchrone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ef4f0eb2e75b977b53300bed6eab4c909fa7796
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423849"
---
# <a name="invoking-service-methods-asynchronously"></a>Appel des méthodes de service de façon asynchrone

L’application WpdServiceApiSample comprend du code qui montre comment une application peut appeler les méthodes de service de façon asynchrone. Cet exemple utilise les interfaces suivantes.



| Interface    | Description          |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                                | Utilisé pour récupérer l’interface **IPortableDeviceServiceMethods** pour appeler des méthodes sur un service donné.                                                                  |
| [**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods)                  | Utilisé pour appeler une méthode de service.                                                                                                                                        |
| [**IPortableDeviceValues**](iportabledevicevalues.md)                                  | Utilisé pour contenir les paramètres de méthode sortants et les résultats de méthode entrante. La valeur peut être **null** si la méthode ne requiert pas de paramètres ou ne retourne aucun résultat. |
| [**IPortableDeviceServiceMethodCallback**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceservicemethodcallback) | Implémenté par l’application pour recevoir les résultats de la méthode lorsqu’une méthode est terminée.                                                                               |



 

Quand l’utilisateur choisit l’option « 10 » sur la ligne de commande, l’application appelle la méthode **InvokeMethodsAsync** qui se trouve dans le module ServiceMethods. cpp. Notez qu’avant d’appeler les méthodes, l’exemple d’application ouvre un service de contacts sur un appareil connecté.

Les méthodes de service encapsulent les fonctionnalités que chaque service définit et implémente. Elles sont uniques à chaque type de service et sont représentées par un GUID. Par exemple, le service contacts définit une méthode **BeginSync** que les applications appellent pour préparer l’appareil à la synchronisation des objets contact, et une méthode **EndSync** pour informer l’appareil que la synchronisation est terminée. Les applications exécutent une méthode de service d’appareil mobile en appelant [**IPortableDeviceServiceMethods :: Invoke**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invoke).

Les méthodes de service ne doivent pas être confondues avec les commandes WPD. Les commandes WPD font partie de l’interface de pilote de périphérique WPD standard (DDI) et constituent le mécanisme de communication entre une application WPD et le pilote. Les commandes sont prédéfinies, regroupées par catégories (par exemple, la **\_ catégorie wpd \_ commun**) et sont représentées par une structure **PROPERTYKEY** . Une application envoie des commandes au pilote de périphérique en appelant [**IPortableDeviceService :: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand). Pour plus d’informations, consultez la rubrique commandes.

La méthode **InvokeMethodsAsync** appelle [**IPortableDeviceService :: Methods**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) pour récupérer une interface [**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) . À l’aide de cette interface, elle appelle à deux reprises la fonction d’assistance **InvokeMethodAsync** . une fois pour la méthode **BeginSync** et une fois pour la méthode **EndSync** . Dans cet exemple,, **InvokeMethodAsync** attend indéfiniment qu’un événement global soit signalé lorsque [**IPortableDeviceServiceMethodCallback :: OnComplete**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethodcallback-oncomplete) est appelé.

Le code suivant utilise la méthode **InvokeMethodsAsync** .


```C++
// Invoke methods on the Contacts Service asynchornously.
// BeginSync and EndSync are methods defined by the FullEnumerationSync Device Service.
void InvokeMethodsAsync(IPortableDeviceService* pService)
{
    HRESULT hr = S_OK;
    CComPtr<IPortableDeviceServiceMethods> pMethods;

    if (pService == NULL)
    {
        printf("! A NULL IPortableDeviceService interface pointer was received\n");
        return;
    }

    // Get an IPortableDeviceServiceMethods interface from the IPortableDeviceService interface to
    // invoke methods.
    hr = pService->Methods(&pMethods);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceServiceMethods from IPortableDeviceService, hr = 0x%lx\n",hr);
    }

    // Invoke the BeginSync method asynchronously
    if (SUCCEEDED(hr))
    {
        printf("Invoking %ws asynchronously...\n",NAME_FullEnumSyncSvc_BeginSync);

        // This method does not take any parameters, so we pass in NULL
        hr = InvokeMethodAsync(pMethods, METHOD_FullEnumSyncSvc_BeginSync, NULL);
        if (FAILED(hr))
        {
            printf("! Failed to invoke %ws asynchronously, hr = 0x%lx\n",NAME_FullEnumSyncSvc_BeginSync, hr);
        }
    }

    // Invoke the EndSync method asynchronously
    if (SUCCEEDED(hr))
    {
        printf("Invoking %ws asynchronously...\n",NAME_FullEnumSyncSvc_EndSync);

        hr = InvokeMethodAsync(pMethods, METHOD_FullEnumSyncSvc_EndSync, NULL);
        if (FAILED(hr))
        {
            printf("! Failed to invoke %ws asynchronously, hr = 0x%lx\n",NAME_FullEnumSyncSvc_EndSync, hr);
        }
    }
}
```



La fonction d’assistance **InvokeMethodAsync** effectue les opérations suivantes pour chaque méthode qu’elle appelle :

-   Crée un handle d’événement global qu’il surveille pour déterminer la fin de la méthode.
-   Crée un objet **CMethodCallback** fourni en tant qu’argument pour [**IPortableDeviceServiceMethods : InvokeAsync**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invokeasync).
-   Appelle la méthode **IPortableDeviceServiceMethods :: InvokeAsync** pour appeler la méthode donnée.
-   Surveille l’achèvement du handle d’événement global.
-   Effectue le nettoyage.

La classe **CMethodCallback** montre comment une application peut implémenter [**IPortableDeviceServiceMethodCallback**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethodcallback). L’implémentation de **OnComplete** dans cette classe signale un événement pour avertir l’application que la méthode de service est terminée. En plus de la méthode **OnComplete** , cette classe implémente **AddRef**, **QueryInterface** et **Release**, qui sont utilisés pour maintenir le décompte de références de l’objet et les interfaces qu’il implémente.


```C++
class CMethodCallback : public IPortableDeviceServiceMethodCallback
{
public:
   CMethodCallback () : m_cRef(1)
   {
   }

   ~CMethodCallback ()
   {
   }

public:
    // IPortableDeviceServiceMethodCallback::QueryInterface
    virtual HRESULT STDMETHODCALLTYPE OnComplete(
        HRESULT                 hrStatus,
        IPortableDeviceValues*  /*pResults*/) // We are ignoring results as our methods will not return any results
    {
        printf("** Method completed, status HRESULT = 0x%lx **\n", hrStatus);

        if (g_hMethodCompleteEvent != NULL)
        {
            SetEvent(g_hMethodCompleteEvent);
        }          
        return S_OK;
    }

    // IUnknown::AddRef
    virtual ULONG STDMETHODCALLTYPE AddRef(void)
    {
        InterlockedIncrement((long*) &m_cRef);
        return m_cRef;
    }

    // IUnknown::QueryInterface
    virtual HRESULT STDMETHODCALLTYPE QueryInterface(
        REFIID  riid,
        LPVOID* ppvObj)
    {
        HRESULT hr = S_OK;
        if (ppvObj == NULL)
        {
            hr = E_INVALIDARG;
            return hr;
        }

        if ((riid == IID_IUnknown) ||
            (riid == IID_IPortableDeviceServiceMethodCallback))
        {
            AddRef();
            *ppvObj = this;
        }
        else
        {
            *ppvObj = NULL;
            hr = E_NOINTERFACE;
        }
        return hr;
    }

    // IUnknown::Release
    virtual ULONG STDMETHODCALLTYPE Release(void)
    {
        ULONG ulRefCount = m_cRef - 1;

        if (InterlockedDecrement((long*) &m_cRef) == 0)
        {
            delete this;
            return 0;
        }
        return ulRefCount;
    }

private:
    DWORD   m_cRef;
};
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[**IPortableDeviceServiceMethodCallback**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethodcallback)
</dt> <dt>

[**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods)
</dt> <dt>

[WpdServicesApiSample](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 
