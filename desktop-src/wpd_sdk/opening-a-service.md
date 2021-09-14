---
description: Ouverture d’un service
ms.assetid: 722d657d-332a-40df-ac30-bc2050deda74
title: Ouverture d’un service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8b273b8709a4d750085f14075d605f88ed0faa6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127225716"
---
# <a name="opening-a-service"></a>Ouverture d’un service

Pour que votre application puisse effectuer des opérations sur un service, par exemple, en énumérant du contenu ou en extrayant des descriptions d’événements ou de méthodes pris en charge, il doit ouvrir le service. Dans l’application WpdServicesApiSample, cette tâche est présentée dans le module ServiceEnumeration. cpp à l’aide des interfaces décrites dans le tableau suivant.



| Interface                                                              | Description                                        |
|------------------------------------------------------------------------|----------------------------------------------------|
| [**IPortableDeviceServiceManager**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemanager) | Utilisé pour énumérer les services sur un appareil.        |
| [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)               | Utilisé pour ouvrir une connexion à un service d’appareil.     |
| [**IPortableDeviceValues**](iportabledevicevalues.md)                 | Utilisé pour contenir les informations du client de l’application. |



 

La méthode qui ouvre un service est [**IPortableDeviceService :: Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open). Cette méthode accepte deux arguments : un identificateur plug-and-Play (PnP) pour le service et un objet [**IPortableDeviceValues**](iportabledevicevalues.md) qui contient les informations sur le client de l’application.

Pour obtenir un identificateur PnP pour un service donné, votre application appelle la méthode [**IPortableDeviceServiceManager :: GetDeviceServices**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices) . Cette méthode récupère un tableau d’identificateurs PnP pour les services d’un GUID de catégorie de service (par exemple, contacts de SERVICE).

L’exemple d’application de service récupère un identificateur PnP pour les services de contacts au sein de la méthode **EnumerateContactsServices** dans le module ServiceEnumeration. cpp. L’exemple de code suivant est extrait de cette méthode.


```C++
// For each device found, find the contacts service
for (dwIndex = 0; dwIndex < cPnpDeviceIDs; dwIndex++)
{
    DWORD   cPnpServiceIDs = 0;
    PWSTR   pPnpServiceID  = NULL;

    // First, pass NULL as the PWSTR array pointer to get the total number
    // of contacts services (SERVICE_Contacts) found on the device.
    // To find the total number of all services on the device, use GUID_DEVINTERFACE_WPD_SERVICE.
    hr = pServiceManager->GetDeviceServices(pPnpDeviceIDs[dwIndex], SERVICE_Contacts, NULL, &cPnpServiceIDs);
    
    if (SUCCEEDED(hr) && (cPnpServiceIDs > 0))
    {                               
        // For simplicity, we are only using the first contacts service on each device
        cPnpServiceIDs = 1;
        hr = pServiceManager->GetDeviceServices(pPnpDeviceIDs[dwIndex], SERVICE_Contacts, &pPnpServiceID, &cPnpServiceIDs);

        if (SUCCEEDED(hr))
        {
            // We've found the service, display it and save its PnP Identifier
            ContactsServicePnpIDs.Add(pPnpServiceID);

            printf("[%d] ", static_cast<DWORD>(ContactsServicePnpIDs.GetCount()-1));

            // Display information about the device that contains this service.
            DisplayDeviceInformation(pServiceManager, pPnpServiceID);

            // ContactsServicePnpIDs now owns the memory for this string
            pPnpServiceID = NULL;
        }
        else
        {
            printf("! Failed to get the first contacts service from '%ws, hr = 0x%lx\n",pPnpDeviceIDs[dwIndex],hr);
        }
    }
}
```



Une fois que votre application a récupéré l’identificateur PnP pour le service, elle peut configurer les informations du client et appeler [**IPortableDeviceService :: Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open).

Dans l’exemple d’application, cette méthode est appelée dans **ChooseDeviceService** dans le module ServiceEnumeration. cpp.

[**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) prend en charge deux CLSID pour **CoCreateInstance**. **CLSID \_ PortableDeviceService** retourne un pointeur **IPortableDeviceService** qui n’agrège pas le marshaleur libre de threads. **CLSID \_ PortableDeviceServiceFTM** est un nouveau CLSID qui retourne un pointeur **IPortableDeviceService** qui agrège le marshaleur libre de threads. Les deux pointeurs prennent en charge la même fonctionnalité dans le cas contraire.

Les applications qui résident dans des cloisonnements à thread unique doivent utiliser le **CLSID \_ PortableDeviceServiceFTM** , car cela élimine la surcharge du marshaling de pointeur d’interface. **CLSID \_ PortableDeviceService** est toujours pris en charge pour les applications héritées.


```C++
hr = CoCreateInstance(CLSID_PortableDeviceServiceFTM,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(&pService));
if (SUCCEEDED(hr))
{
    hr = pService->Open(ContactsServicesArray[uiCurrentService], pClientInformation);
    if (FAILED(hr))
    {
        if (hr == E_ACCESSDENIED)
        {
            printf("Failed to Open the service for Read Write access, will open it for Read-only access instead\n");

            pClientInformation->SetUnsignedIntegerValue(WPD_CLIENT_DESIRED_ACCESS, GENERIC_READ);

            hr = pService->Open(ContactsServicesArray[uiCurrentService], pClientInformation);

            if (FAILED(hr))
            {
                printf("! Failed to Open the service for Read access, hr = 0x%lx\n",hr);
            }
        }
        else
        {
            printf("! Failed to Open the service, hr = 0x%lx\n",hr);
        }
    }
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Interface IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[**Interface IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**Interface IPortableDeviceServiceManager**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemanager)
</dt> <dt>

[WpdServicesApiSample](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



