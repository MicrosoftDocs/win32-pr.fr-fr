---
title: Recherche synchrone
description: L’objet de recherche d’appareils active les recherches synchrones et asynchrones. Les recherches synchrones sont terminées et retournent le contrôle à l’application appelante uniquement après la détection de tous les appareils disponibles.
ms.assetid: fa22cd53-6468-4958-b4e3-b1a41b3cb2f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f852957bed4bb73d9b31d0e26e099eb545b804953718d8cfd4e3cb44ea5f6c62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999499"
---
# <a name="synchronous-searching"></a>Recherche synchrone

L’objet de recherche d’appareils active les recherches synchrones et asynchrones. Les recherches synchrones sont terminées et retournent le contrôle à l’application appelante uniquement après la détection de tous les appareils disponibles. Pour effectuer une recherche synchrone, utilisez l’une des méthodes de recherche synchrone de l’interface [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) .

> [!Note]  
> Les recherches synchrones prennent au moins neuf secondes pour être retournées. Le délai est dû au fait que le message de recherche UDP initial doit être envoyé plusieurs fois. Cette duplication tient compte de l’infiabilité du protocole réseau sous-jacent. Les recherches synchrones sont idéales pour les interfaces de ligne de commande. Elles ne sont pas recommandées pour les interfaces utilisateur graphiques.

 

La méthode [**IUPnPDeviceFinder :: FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) effectue une recherche par type d’appareil ou de service. Cette méthode prend un URI de type comme paramètre d’entrée et retourne une collection d’objets périphériques. Un objet appareil représente un appareil individuel.

Les exemples suivants montrent comment effectuer une recherche synchrone des appareils dans VBScript. Chaque script utilise [**IUPnPDeviceFinder :: FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype), appelé avec l’URI de type (ID de service) pour le type d’appareil Media Player, *urn : schemas-UPnP-org : Device : MediaPlayer. v 1.00.00*. La méthode retourne une collection d’objets Device qui correspond aux périphériques Media Player qui ont été trouvés. Pour plus d’informations sur l’extraction d’objets d’appareil individuels à partir d’une collection, consultez [regroupements de périphériques retournés par les recherches synchrones](device-collections-returned-by-synchronous-searches.md).

## <a name="search-for-devices-by-type-in-vbscript"></a>Rechercher des appareils par type dans VBScript


```VB
Dim deviceFinder

Set deviceFinder = CreateObject( "UPnP.UPnPDeviceFinder" )

Dim devices

Set devices = deviceFinder.FindByType( "urn:schemas-upnp-org:device:multidisk-dvd", 0 )
```



## <a name="search-for-device-by-type-in-c"></a>Rechercher des appareils par type en C++

L’exemple suivant illustre une recherche synchrone de périphériques Media Player à l’aide de C++. La fonction prend un pointeur vers l’interface [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) comme entrée et retourne le pointeur d’interface [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) .

L’exemple alloue d’abord un **BSTR** pour représenter l’URI du type d’appareil, puis le transmet à la méthode [**IUPnPDeviceFinder :: FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) . Il transmet également l’adresse d’un pointeur [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) local dans la mémoire tampon dans laquelle la méthode stocke ensuite la collection d’appareils trouvés. Si l’appel de fonction réussit, il retourne le pointeur vers cette collection.


```C++
#include <windows.h>
#include <upnp.h>
#include <stdio.h>

#pragma comment(lib, "oleaut32.lib")

IUPnPDevices *FindMediaPlayerDevices(IUPnPDeviceFinder *pDeviceFinder)
{
    HRESULT         hr = S_OK;
    IUPnPDevices    * pFoundDevices = NULL;
    BSTR            bstrTypeURI = NULL;

    bstrTypeURI = 
        SysAllocString(L"urn:schemas-upnp-org:device:multidisk-dvd");

    if (bstrTypeURI)
    {
        hr = pDeviceFinder->FindByType(bstrTypeURI, 
                                       0,
                                       &pFoundDevices);

        if (SUCCEEDED(hr))
        {
            wprintf(L"FindMediaPlayerDevices(): "
                    L"Search returned successfully\n");
        }
        else
        {
            fwprintf(stderr, L"FindMediaPlayerDevices(): "
                     L"FindByType search failed - returned "
                     L"HRESULT 0x%x\n",
                     hr);
            pFoundDevices = NULL;
        }
        SysFreeString(bstrTypeURI);
    }
    else
    {
        fwprintf(stderr, L"FindMediaPlayerDevices(): "
                 L"Could not allocate BSTR for type URI\n");
    }

    return pFoundDevices;
}
```



 

 




