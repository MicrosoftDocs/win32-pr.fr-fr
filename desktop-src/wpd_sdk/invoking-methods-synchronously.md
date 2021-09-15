---
description: Appel de méthodes de service
ms.assetid: 3a2796c8-1a39-49eb-98e1-c9e06c61f397
title: Appel de méthodes de service
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15b9540cf7378e13d56af2611d6216897c6750f6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127520985"
---
# <a name="invoking-service-methods"></a>Appel de méthodes de service

L’application WpdServicesApiSample comprend du code qui montre comment une application peut appeler de façon synchrone les méthodes prises en charge par un service de contacts donné. Cet exemple utilise les interfaces suivantes :



| Interface    | Description    |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)               | Utilisé pour récupérer l’interface **IPortableDeviceServiceMethods** pour appeler des méthodes sur un service donné.                                                                  |
| [**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods) | Utilisé pour appeler une méthode de service.                                                                                                                                        |
| [**IPortableDeviceValues**](iportabledevicevalues.md)                 | Utilisé pour contenir les paramètres de méthode sortants et les résultats de méthode entrante. La valeur peut être **null** si la méthode ne requiert pas de paramètres ou ne retourne aucun résultat. |



 

Quand l’utilisateur choisit l’option « 9 » sur la ligne de commande, l’application appelle la méthode **InvokeMethods** qui se trouve dans le module ServiceMethods. cpp. Notez qu’avant d’appeler les méthodes, l’exemple d’application ouvre un service de contacts sur un appareil connecté.

Les méthodes de service encapsulent les fonctionnalités que chaque service définit et implémente. Elles sont uniques à chaque type de service et sont représentées par un GUID. Par exemple, le service contacts définit une méthode **BeginSync** que les applications appellent pour préparer l’appareil à la synchronisation des objets contact, et une méthode **EndSync** pour informer l’appareil que la synchronisation est terminée. Les applications exécutent une méthode en appelant [**IPortableDeviceServiceMethods :: Invoke**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invoke).

Les méthodes de service ne doivent pas être confondues avec les commandes WPD. Les commandes WPD font partie de l’interface de pilote de périphérique WPD standard (DDI) et constituent le mécanisme de communication entre une application WPD et le pilote. Les commandes sont prédéfinies, regroupées par catégories, par exemple, la **\_ catégorie wpd \_ commun** et sont représentées par une structure **PROPERTYKEY** . Une application envoie des commandes au pilote de périphérique en appelant [**IPortableDeviceService :: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand). Pour plus d’informations, consultez la rubrique commandes.

La méthode **InvokeMethods** appelle la méthode [**IPortableDeviceService :: Methods**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) pour récupérer une interface [**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) . À l’aide de cette interface, il appelle les méthodes **BeginSync** et **EndSync** en appelant la méthode [**IPortableDeviceServiceMethods :: Invoke**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedmethods) . À chaque fois qu’il appelle **Invoke**, l’application fournit le REFGUID pour la méthode appelée.

Le code suivant utilise la méthode **InvokeMethods** .


```C++
// Invoke methods on the Contacts Service.
// BeginSync and EndSync are methods defined by the FullEnumerationSync Device Service.
void InvokeMethods(IPortableDeviceService* pService)
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

    // Invoke() the BeginSync method
    if (SUCCEEDED(hr))
    {
        // This method does not take any parameters or results, so we pass in NULL
        hr = pMethods->Invoke(METHOD_FullEnumSyncSvc_BeginSync, NULL, NULL);
        if (SUCCEEDED(hr))
        {
            printf("%ws called, hr = 0x%lx\n",NAME_FullEnumSyncSvc_BeginSync, hr);
        }
        else
        {
            printf("! Failed to invoke %ws, hr = 0x%lx\n",NAME_FullEnumSyncSvc_BeginSync, hr);
        }
    }

    // Invoke the EndSync method asynchronously
    if (SUCCEEDED(hr))
    {
        // This method does not take any parameters or results, so we pass in NULL
        hr = pMethods->Invoke(METHOD_FullEnumSyncSvc_EndSync, NULL, NULL);
        if (SUCCEEDED(hr))
        {
            printf("%ws called, hr = 0x%lx\n",NAME_FullEnumSyncSvc_EndSync, hr);
        }
        else
        {
            printf("! Failed to invoke %ws, hr = 0x%lx\n",NAME_FullEnumSyncSvc_EndSync, hr);
        } 
    }
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods)
</dt> <dt>

[WpdServicesApiSample](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



