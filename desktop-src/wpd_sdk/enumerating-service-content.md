---
description: Énumération du contenu du service
ms.assetid: 4af4201c-d3f6-4630-91ec-6509c51871a5
title: Énumération du contenu du service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd9846565b7cdc4b0a4475cb99806b671452dcbe134e40d4b1e3d70df249c510
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083563"
---
# <a name="enumerating-service-content"></a>Énumération du contenu du service

Une fois que votre application a ouvert un service, elle peut commencer à effectuer des opérations liées au service. Dans le cas de l’application WpdServicesApiSample, l’une de ces opérations est l’énumération du contenu pour un service de contacts donné. Le tableau suivant décrit les interfaces utilisées.



| Interface                                                            | Description                                                                                      |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)             | Utilisé pour récupérer l’interface IPortableDeviceContent2 pour accéder au contenu sur le service.         |
| [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)           | Utilisé pour récupérer l’interface IEnumPortableDeviceObjectIDs pour énumérer des objets sur le service. |
| [**IEnumPortableDeviceObjectIDs**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids) | Utilisé pour énumérer des objets sur le service.                                                        |



 

Le code d’énumération du contenu se trouve dans le module ContentEnumeration. cpp. Ce code se trouve dans les méthodes **EnumerateAllContent** et **RecursiveEnumerate** . La première méthode appelle la dernière.

La méthode **EnumerateContent** prend un pointeur vers un objet [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) en tant que paramètre unique. Cet objet correspond à un service que l’application a ouvert précédemment quand elle a appelé la méthode [**IPortableDeviceService :: Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open) .

La méthode **EnumerateContent** crée un objet [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2) et passe cet objet à la méthode [**IPortableDeviceService :: content**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-content) . Cette méthode récupère ensuite le contenu au niveau racine du service, puis commence à récupérer de façon récursive le contenu trouvé sous la racine.

Le code suivant correspond à la méthode **EnumerateContent** .


```C++
// Enumerate all content on the service starting with the
// "DEVICE" object
void EnumerateAllContent(
    IPortableDeviceService* pService)
{
    HRESULT                          hr = S_OK;
    CComPtr<IPortableDeviceContent2> pContent;

    if (pService == NULL)
    {
        printf("! A NULL IPortableDeviceService interface pointer was received\n");
        return;
    }

    // Get an IPortableDeviceContent2 interface from the IPortableDeviceService interface to
    // access the content-specific methods.
    hr = pService->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent2 from IPortableDeviceService, hr = 0x%lx\n",hr);
    }

    // Enumerate content starting from the "DEVICE" object.
    if (SUCCEEDED(hr))
    {
        printf("\n");
        RecursiveEnumerate(WPD_DEVICE_OBJECT_ID, pContent);
    }
}
```



Le code suivant correspond à la méthode **RecursiveEnumerate** . La méthode RecursiveEnumerate instancie une interface **IEnumPortableDeviceObjectIDs** pour l’objet parent fourni et appelle **IEnumPortableDeviceObjectIDs :: Next**, en extrayant un lot d’objets enfants immédiats. Pour chaque objet enfant, RecursiveEnumerate est rappelé pour retourner ses objets enfants descendants, et ainsi de suite.


```C++
// Recursively called function which enumerates using the specified
// object identifier as the parent.
void RecursiveEnumerate(
    PCWSTR                   pszObjectID,
    IPortableDeviceContent2* pContent)
{
    CComPtr<IEnumPortableDeviceObjectIDs> pEnumObjectIDs;

    // Print the object identifier being used as the parent during enumeration.
    printf("%ws\n",pszObjectID);

    // Get an IEnumPortableDeviceObjectIDs interface by calling EnumObjects with the
    // specified parent object identifier.
    HRESULT hr = pContent->EnumObjects(0,               // Flags are unused
                                       pszObjectID,     // Starting from the passed in object
                                       NULL,            // Filter is unused
                                       &pEnumObjectIDs);
    if (FAILED(hr))
    {
        printf("! Failed to get IEnumPortableDeviceObjectIDs from IPortableDeviceContent2, hr = 0x%lx\n",hr);
    }

    // Loop calling Next() while S_OK is being returned.
    while(hr == S_OK)
    {
        DWORD  cFetched = 0;
        PWSTR  szObjectIDArray[NUM_OBJECTS_TO_REQUEST] = {0};
        hr = pEnumObjectIDs->Next(NUM_OBJECTS_TO_REQUEST,   // Number of objects to request on each NEXT call
                                  szObjectIDArray,          // Array of PWSTR array which will be populated on each NEXT call
                                  &cFetched);               // Number of objects written to the PWSTR array
        if (SUCCEEDED(hr))
        {
            // Traverse the results of the Next() operation and recursively enumerate
            // Remember to free all returned object identifiers using CoTaskMemFree()
            for (DWORD dwIndex = 0; dwIndex < cFetched; dwIndex++)
            {
                RecursiveEnumerate(szObjectIDArray[dwIndex],pContent);

                // Free allocated PWSTRs after the recursive enumeration call has completed.
                CoTaskMemFree(szObjectIDArray[dwIndex]);
                szObjectIDArray[dwIndex] = NULL;
            }
        }
    }
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IEnumPortableDeviceObjectIDs**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids)
</dt> <dt>

[**Interface IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)
</dt> <dt>

[**Interface IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[Ouverture d’un service](opening-a-service.md)
</dt> <dt>

[WpdServicesApiSample](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



