---
title: Regroupements de périphériques retournés par les recherches synchrones
description: Les regroupements d’appareils sont des objets qui contiennent un ou plusieurs objets appareil. Une collection de périphériques expose l’interface IUPnPDevices qui fournit des méthodes et des propriétés pour parcourir la collection et extraire des objets périphériques individuels.
ms.assetid: 45455c3f-7281-4f96-a609-2efd2cf36aa2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94901dd2f3988327c32d7c21799ff4db7647e76fd987247e903501bd8937851a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117755525"
---
# <a name="device-collections-returned-by-synchronous-searches"></a>Regroupements de périphériques retournés par les recherches synchrones

Les regroupements d’appareils sont des objets qui contiennent un ou plusieurs objets appareil. Une collection de périphériques expose l’interface [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) qui fournit des méthodes et des propriétés pour parcourir la collection et extraire des objets périphériques individuels.

## <a name="vbscript-example"></a>Exemple VBScript

Les applications VBScript peuvent accéder aux objets de la collection de deux façons. Tout d’abord, ils peuvent traverser les éléments de manière séquentielle à l’aide d’une boucle for... chaque... Next, comme illustré dans l’exemple suivant :


```VB
for each deviceObj in devices
    MsgBox(deviceObj.FriendlyName)
next
```



Dans cet exemple, la variable Devices est supposée avoir été initialisée avec le résultat d’une recherche antérieure. La boucle parcourt les objets d’appareil de la collection, en affectant la variable deviceObj la valeur de chaque objet d’appareil. Le corps de la boucle peut contenir du code qui traite l’objet appareil.

## <a name="c-example"></a>Exemple C++

L’exemple suivant montre le code C++ requis pour accéder aux objets dans une collection d’objets appareil. La fonction illustrée, **TraverseCollection**, reçoit un pointeur vers l’interface [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) en tant que paramètre d’entrée. Ce pointeur d’interface peut être retourné par la méthode [**FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) , ou d’autres méthodes **Find** , de l’objet de recherche d’appareil.


```C++
#include <windows.h>
#include <upnp.h>

#pragma comment(lib, "oleaut32.lib")

HRESULT TraverseCollection(IUPnPDevices * pDevices)
{
    IUnknown * pUnk = NULL;
    HRESULT hr = pDevices->get__NewEnum(&pUnk);
    if (SUCCEEDED(hr))
    {
        IEnumVARIANT * pEnumVar = NULL;
        hr = pUnk->QueryInterface(IID_IEnumVARIANT, (void **) &pEnumVar);
        if (SUCCEEDED(hr))
        {
            VARIANT varCurDevice;
            VariantInit(&varCurDevice);
            pEnumVar->Reset();
            // Loop through each device in the collection
            while (S_OK == pEnumVar->Next(1, &varCurDevice, NULL))
            {
                IUPnPDevice * pDevice = NULL;
                IDispatch * pdispDevice = V_DISPATCH(&varCurDevice);
                if (SUCCEEDED(pdispDevice->QueryInterface(IID_IUPnPDevice, (void **) &pDevice)))
                {
                    // Do something interesting with pDevice
                    BSTR bstrName = NULL;
                    if (SUCCEEDED(pDevice->get_FriendlyName(&bstrName)))
                    {
                        OutputDebugStringW(bstrName);
                        SysFreeString(bstrName);
                    }
                }
                VariantClear(&varCurDevice);
                pDevice->Release();
            }
            pEnumVar->Release();
        }
        pUnk->Release();
    }
    return hr;
}
```



La première étape consiste à demander un nouvel énumérateur pour la collection à l’aide de la propriété [**\_ NewEnum**](/windows/win32/api/upnp/nf-upnp-iupnpdevices-get__newenum) . Cela retourne un énumérateur comme interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . L’exemple de code appelle [**IUnknown :: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) pour obtenir l’interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) . L’exemple de code définit ensuite l’énumérateur au début de la collection en appelant la méthode [**IEnumVARIANT :: Reset**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-reset) . Enfin, l’exemple de code appelle la méthode [**IEnumVARIANT :: Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next) pour parcourir la collection. Les objets d’appareil de la collection sont contenus dans des structures de **variantes** . Ces structures contiennent des pointeurs vers des interfaces [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) sur les objets d’appareil. Pour obtenir l’interface [**IUPnPDevice**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevice) , l’exemple de code appelle **QueryInterface** sur l’interface **IDispatch** .

 

 