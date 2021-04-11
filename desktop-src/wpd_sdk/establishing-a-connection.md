---
description: Établissement d’une connexion
ms.assetid: 16286da5-5979-413b-a4db-ca157b10a571
title: Établissement d’une connexion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56ea922b3cd44430dc7c213a513c44fa8ef2ab9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042826"
---
# <a name="establishing-a-connection"></a>Établissement d’une connexion

Une fois que l’utilisateur a sélectionné un appareil, la fonction ChooseDevice appelle à son tour la méthode [**IPortableDevice :: Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open) pour établir une connexion entre l’application et l’appareil. La méthode IPortableDevice :: Open accepte deux arguments :

-   Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom Plug-and-Play du périphérique. (Cette chaîne est récupérée en appelant la méthode [**IPortableDeviceManager :: GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices) .)
-   Pointeur vers une [**interface IPortableDeviceValues**](iportabledevicevalues.md) qui spécifie les informations sur le client pour l’application.


```C++
// CoCreate the IPortableDevice interface and call Open() with
// the chosen PnPDeviceID string.
hr = CoCreateInstance(CLSID_PortableDeviceFTM,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(ppDevice));
if (SUCCEEDED(hr))
{
    hr = (*ppDevice)->Open(pPnpDeviceIDs[uiCurrentDevice], pClientInformation);
    if (FAILED(hr))
    {
        if (hr == E_ACCESSDENIED)
        {
            printf("Failed to Open the device for Read Write access, will open it for Read-only access instead\n");
            pClientInformation->SetUnsignedIntegerValue(WPD_CLIENT_DESIRED_ACCESS, GENERIC_READ);
            hr = (*ppDevice)->Open(pPnpDeviceIDs[uiCurrentDevice], pClientInformation);
            if (FAILED(hr))
            {
                printf("! Failed to Open the device, hr = 0x%lx\n",hr);
                // Release the IPortableDevice interface, because we cannot proceed
                // with an unopen device.
                (*ppDevice)->Release();
                *ppDevice = NULL;
            }
        }
        else
        {
            printf("! Failed to Open the device, hr = 0x%lx\n",hr);
            // Release the IPortableDevice interface, because we cannot proceed
            // with an unopen device.
            (*ppDevice)->Release();
            *ppDevice = NULL;
        }
    }
}
else
{
    printf("! Failed to CoCreateInstance CLSID_PortableDeviceFTM, hr = 0x%lx\n",hr);
}
```



Pour Windows 7, [**IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice) prend en charge deux CLSID pour **CoCreateInstance**. **CLSID \_ PortableDevice** retourne un pointeur **IPortableDevice** qui n’agrège pas le marshaleur libre de threads. **CLSID \_ PortableDeviceFTM** est un nouveau CLSID qui retourne un pointeur **IPortableDevice** qui agrège le marshaleur libre de threads. Les deux pointeurs prennent en charge la même fonctionnalité dans le cas contraire.

Les applications qui résident dans des cloisonnements à thread unique doivent utiliser le **CLSID \_ PortableDeviceFTM** , car cela élimine la surcharge du marshaling de pointeur d’interface. **CLSID \_ PortableDevice** est toujours pris en charge pour les applications héritées.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Sélection d’un appareil**](selecting-a-device.md)
</dt> </dl>

 

 



