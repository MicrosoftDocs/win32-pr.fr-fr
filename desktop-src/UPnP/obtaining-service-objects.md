---
title: Obtention d’objets de service
description: Les objets appareil exposent une propriété appelée services qui retourne une collection d’objets de service qui contient un objet de service pour chaque service exporté par l’appareil.
ms.assetid: 8ef12b6e-cb9b-4406-95be-002117b8fc3f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b7fca24bfc79a9458cfb964af28edba813a90ef17924a68fd0d1689e047884c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999569"
---
# <a name="obtaining-service-objects"></a>Obtention d’objets de service

Les objets appareil exposent une propriété appelée [**services**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) qui retourne une collection d’objets de service qui contient un objet de service pour chaque service exporté par l’appareil. Les applications peuvent parcourir cette collection séquentiellement ou demander un service particulier à l’aide de son ID de service.

## <a name="vbscript-example"></a>Exemple VBScript

L’exemple suivant est un code VBScript qui extrait des objets de service pour deux des services exportés par un appareil.


```VB
' Get the service objects
services = device.Services
    
Set appService = services( "urn:upnp-org:serviceId:DVDVideo" )
Set xportService = services( "urn:upnp-org:serviceId:AVTransport" )
```



La première ligne extrait la collection services de l’objet Device en interrogeant la propriété [**services**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) . Les deux lignes suivantes obtiennent les deux objets de service souhaités à partir de la collection en spécifiant leurs ID de service. La collection services peut également être parcourue de manière séquentielle à l’aide d’une boucle **for each... Next** .

## <a name="c-example"></a>Exemple C++

L’exemple suivant montre le code C++ requis pour obtenir des objets de service à partir d’un appareil. Tout d’abord, l’exemple de code interroge la propriété [**IUPnPDevice :: services**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) sur l’interface qui a été passée à la fonction. Cela retourne une collection de services à l’aide de l’interface [**IUPnPServices**](/windows/desktop/api/Upnp/nn-upnp-iupnpservices) . Pour obtenir des objets de service individuels, utilisez la méthode [**Item**](/windows/win32/api/upnp/nf-upnp-iupnpservices-get_item) et spécifiez les ID de service demandés. Pour parcourir la collection de manière séquentielle, utilisez les méthodes [**IEnumVARIANT :: Reset**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-reset), [**IEnumVARIANT :: Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next)et [**IEnumVARIANT :: Skip**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-skip) . Cet exemple est similaire à l’exemple utilisé pour parcourir la collection [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) .


```C++
#include <windows.h>
#include <upnp.h>

#pragma comment(lib, "oleaut32.lib")


HRESULT ExtractServices(IUPnPDevice * pDevice)
{
    // Create a BSTR to hold the service name
    BSTR bstrServiceName = SysAllocString(L"urn:upnp-org:servicId:DVDVideo");
    if (NULL == bstrServiceName)
    {
        return E_OUTOFMEMORY;
    }
    // Get the list of services available on the device
    IUPnPServices * pServices = NULL;
    HRESULT hr = pDevice->get_Services(&pServices);
    if (SUCCEEDED(hr))
    {
        // Retrieve the service we are interested in
        IUPnPService * pAppService = NULL;
        hr = pServices->get_Item(bstrServiceName, &pAppService);
        if (SUCCEEDED(hr))
        {
            // Do something interesting with the service object
            pAppService->Release();
        }
        pServices->Release();
    }
    SysFreeString(bstrServiceName);
    return hr;
}
```



 

 