---
title: Énumération des appareils (kit de développement logiciel (SDK) WMP)
description: Énumération des appareils
ms.assetid: 0236a629-c09a-4687-a8ba-fa05107fab33
keywords:
- Lecteur Windows Media, appareils mobiles
- Modèle objet du lecteur Windows Media, appareils mobiles
- modèle objet, appareils mobiles
- Contrôle ActiveX du lecteur Windows Media, appareils mobiles
- Contrôle ActiveX, appareils mobiles
- Windows Media Player Mobile contrôle ActiveX, appareils mobiles
- Windows Media Player Mobile, appareils mobiles
- appareils mobiles, énumération
- énumérations, appareils mobiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5025d0e0a7e99028b22cc24ebc56337ea84d2fb
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103940685"
---
# <a name="enumerating-devices"></a>Énumération des appareils

Le lecteur Windows Media représente des appareils portables à l’aide de l’interface **IWMPSyncDevice** . L’exemple de code suivant montre une fonction qui crée un tableau de pointeurs vers **IWMPSyncDevice**. Chaque pointeur dans le tableau représente un appareil pour lequel le lecteur Windows Media a stocké des informations. Il n’est pas nécessaire qu’un appareil soit connecté à l’ordinateur. il ne doit pas non plus être associé à l’instance actuelle du lecteur Windows Media.

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

 

 




