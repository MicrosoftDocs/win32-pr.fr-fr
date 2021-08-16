---
title: Énumération des appareils (kit de développement logiciel (SDK) WMP)
description: Cet exemple de code montre une fonction qui énumère des appareils en créant un tableau de pointeurs qui représentent chacun un appareil.
ms.assetid: 0236a629-c09a-4687-a8ba-fa05107fab33
keywords:
- Lecteur Windows Media, appareils mobiles
- modèle objet Lecteur Windows Media, appareils mobiles
- modèle objet, appareils mobiles
- contrôle de ActiveX Lecteur Windows Media, appareils mobiles
- contrôle de ActiveX, appareils mobiles
- Lecteur Windows Media contrôle Mobile ActiveX, appareils mobiles
- Lecteur Windows Media Mobile, appareils mobiles
- appareils mobiles, énumération
- énumérations, appareils mobiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64f62ecc599e8a9610bf01b5f8a1651b330c9f8ed6abb4197fac89daeb751c4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118339857"
---
# <a name="enumerating-devices"></a>Énumération des appareils

Lecteur Windows Media représente des appareils mobiles à l’aide de l’interface **IWMPSyncDevice** . L’exemple de code suivant montre une fonction qui crée un tableau de pointeurs vers **IWMPSyncDevice**. chaque pointeur dans le tableau représente un appareil pour lequel Lecteur Windows Media contient des informations stockées. il n’est pas nécessaire qu’un appareil soit connecté à l’ordinateur et qu’il ne soit pas obligé d’avoir un partenariat avec l’instance de Lecteur Windows Media actuelle.

Vous devez énumérer les appareils chaque fois que vous recevez l’événement **DeviceConnect** ou **DeviceDisconnect** .

La fonction suivante énumère les appareils. Le paramètre *bConnectedOnly* spécifie s’il faut énumérer uniquement les appareils actuellement connectés à l’ordinateur de l’utilisateur.


```C++
STDMETHODIMP CMainDlg::EnumDevices(BOOL bConnectedOnly)
{
    HRESULT hr = S_OK;
    CComPtr<IWMPSyncServices>  spSyncServices;
    long cDeviceArray = 0;  // Size to make the array
    long cAllDevices = 0;  // Count of all devices
    long cDeviceIndex = 0; // Index for adding devices to array.
    CComPtr<IWMPSyncDevice> spTempDevice;
    VARIANT_BOOL vbIsConnected = VARIANT_FALSE;

    // Delete any existing array.
    FreeDeviceArray();

    // Retrieve a pointer to IWMPSyncServices.
    hr = m_spPlayer->QueryInterface(&spSyncServices);

    if(SUCCEEDED(hr) && spSyncServices.p)
    {  
        hr = spSyncServices->get_deviceCount(&cAllDevices);
    }

    if(SUCCEEDED(hr) && cAllDevices > 0)
    {
        if(bConnectedOnly)
        {
            // Count the number of connected devices.
            for(long i = 0; i < cAllDevices; i++)
            {     
                spTempDevice.Release();
                hr = spSyncServices->getDevice(i, &spTempDevice);

                if(SUCCEEDED(hr) && spTempDevice.p)
                {
                    spTempDevice->get_connected(&vbIsConnected);

                    if(vbIsConnected == VARIANT_TRUE)
                    {
                        // Count only the connected devices.
                        cDeviceArray++;
                    }
                }
            }
        }
        else
        {
            cDeviceArray = cAllDevices;
        }

        if(cDeviceArray == 0)
        {
            return hr;
        }

        // Cache the device count.
        m_cDevices = cDeviceArray;

        // Create a new device array.
        m_ppWMPDevices = new IWMPSyncDevice*[cDeviceArray];
        if(!m_ppWMPDevices)
        {
            return E_OUTOFMEMORY;
        }
        
        ZeroMemory(m_ppWMPDevices, sizeof (IWMPSyncDevice*) * cDeviceArray);

        // Fill the array.
        for(long i = 0; i < cAllDevices; i++)
        {
            spTempDevice.Release();
            hr = spSyncServices->getDevice(i, &spTempDevice);
            if(SUCCEEDED(hr) && spTempDevice.p)
            {
                spTempDevice->get_connected(&vbIsConnected);

                if( (bConnectedOnly && vbIsConnected == VARIANT_TRUE) ||
                     !bConnectedOnly )
                {
                    // Add the device to the custom array.
                    spTempDevice.CopyTo(&m_ppWMPDevices[cDeviceIndex++]);
                }
            }
        }
    }

    return hr;
}
```



Vous pouvez utiliser du code similaire pour récupérer d’autres listes d’appareils de ce type. Par exemple, vous pouvez utiliser [IWMPSyncDevice :: obtenir l' \_ État](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) pour créer un tableau d’appareils pour lequel un partenariat existe.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IWMPEvents2 ::D eviceConnect**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents2-deviceconnect)
</dt> <dt>

[**IWMPEvents2 ::D eviceDisconnect**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents2-devicedisconnect)
</dt> <dt>

[**Interface IWMPSyncDevice**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)
</dt> <dt>

[**IWMPSyncDevice : \_ : Connectez-vous**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_connected)
</dt> <dt>

[**Interface IWMPSyncServices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncservices)
</dt> <dt>

[**Utilisation d’appareils mobiles**](working-with-portable-devices.md)
</dt> </dl>

 

 




