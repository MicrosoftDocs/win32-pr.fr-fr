---
title: énumération des appareils Windows Media Gestionnaire de périphériques
description: en savoir plus sur l’énumération des appareils détectés par Windows Media Gestionnaire de périphériques à l’aide d’une interface d’énumération.
ms.assetid: c5935681-b530-4446-a026-7ddc74084d23
keywords:
- Windows Gestionnaire de périphériques de média, énumération des appareils
- Gestionnaire de périphériques, énumération des appareils
- Guide de programmation, énumération des appareils
- applications de bureau, énumération des appareils
- création d’applications Windows Media Gestionnaire de périphériques, énumération d’appareils
- énumération des appareils
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0009e2206bf7c97839d890d00c08a8e1806196efee9af95db72336b95d8b2cdf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118584657"
---
# <a name="enumerating-windows-media-device-manager-devices"></a>énumération des appareils Windows Media Gestionnaire de périphériques

après l’authentification d’une application, vous pouvez commencer à énumérer les appareils détectés par Windows Gestionnaire de périphériques de média. L’énumération est effectuée à l’aide d’une interface d’énumération, [**IWMDMEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice), obtenue à l’aide de [**IWMDeviceManager2 :: EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2) ou [**IWMDeviceManager :: EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices). En cas de prise en charge, utilisez la méthode **EnumDevices2** , car la version antérieure retournait uniquement les interfaces héritées sur les appareils, tandis que la nouvelle version retourne à la fois les interfaces héritées et nouvelles.

Avant d’obtenir un énumérateur, vous devez décider de la vue d’énumération à utiliser. Certains appareils exposent chaque stockage sous la forme d’un autre appareil. Par exemple, deux cartes mémoire flash sur un appareil sont énumérées comme s’il s’agissait de périphériques distincts. Vous pouvez spécifier que tous les stockages sur un appareil sont énumérés comme un seul appareil. Vous ne pouvez définir cette préférence qu’une seule fois dans votre application ; Si vous souhaitez le modifier, vous devez arrêter l’application et la redémarrer. Toutefois, Notez que les appareils hérités ignorent parfois une demande d’énumération de stockages d’appareils distincts comme un seul appareil et continuent de les énumérer séparément.

Les étapes suivantes montrent comment énumérer les appareils connectés :

1.  Définissez la préférence d’énumération des appareils à l’aide de [**IWMDeviceManager3 :: SetDeviceEnumPreference**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager3-setdeviceenumpreference). Si cette méthode n’est pas appelée, la méthode par défaut consiste à afficher les stockages comme des appareils distincts. Pour déterminer si les « appareils » individuels sont en fait des stockages sur le même appareil, appelez [**IWMDMDevice2 :: GetCanonicalName**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice2-getcanonicalname); les stockages à partir du même appareil retournent des valeurs identiques, à l’exception du chiffre final situé après le dernier signe « $ ».
2.  Interrogez [**IWMDeviceManager**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager) ou [**IWMDeviceManager2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager2), puis appelez [**IWMDeviceManager2 :: EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2) pour obtenir l’interface de l’énumérateur d’appareil, [**IWMDMEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice). (S’il est pris en charge, utilisez **EnumDevices2**, ce qui est plus efficace, car la version antérieure peut ne pas retourner de périphériques MTP).
3.  Appelez la méthode [**IWMDMEnumDevices :: Next**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmenumdevice-next) pour récupérer un ou plusieurs appareils à la fois. Continuez à appeler cette méthode jusqu’à ce que la méthode retourne S \_ false ou un message d’erreur. Si vous récupérez un seul appareil à la fois, vous n’avez pas besoin d’allouer un tableau pour stocker les appareils.

Étant donné que les utilisateurs peuvent attacher ou supprimer des appareils de l’ordinateur pendant l’exécution de votre application, il est conseillé d’implémenter la notification de la connexion ou de la suppression de l’appareil. Cela s’effectue en implémentant l’interface [**IWMDMNotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification) et en l’inscrivant. Pour plus d’informations, consultez la page [activation des notifications](enabling-notifications.md).

Le code C++ suivant énumère les appareils et demande des informations sur chaque appareil.


```C++
HRESULT CWMDMController::EnumDevices()
{
    HRESULT hr = S_OK;

    // Change behavior to show devices as one object, not each storage as a device.
    // This can be called only once for each instance of this application.
    CComQIPtr<IWMDeviceManager3>pDevMgr3(m_IWMDMDeviceMgr);
    hr = pDevMgr3->SetDeviceEnumPreference(DO_NOT_VIRTUALIZE_STORAGES_AS_DEVICES);
    
    // Get number of attached devices.
    DWORD iDevices = 0;
    hr = m_IWMDMDeviceMgr->GetDeviceCount(&iDevices);
    if (hr == S_OK)
    {
        // TODO: Display count of devices.
    }

    //
    // Get a device enumerator to enumerate devices.
    //
    CComPtr<IWMDeviceManager2> pDevMgr2;
    hr = m_IWMDMDeviceMgr->QueryInterface (__uuidof(IWMDeviceManager2), (void**) &pDevMgr2);
    if (hr == S_OK)
    {
        // TODO: Display message indicating that application obtained IWMDeviceManager2.
    }
    else
    {
        // TODO: Display message indicating that we couldn't 
        // get IWMDeviceManager2 in EnumDevices.
        return hr;
    }
   CComPtr<IWMDMEnumDevice> pEnumDevice;
   hr = pDevMgr2->EnumDevices2(&pEnumDevice);
    if (hr != S_OK)
    {
        // TODO: Display messaging indicating that an error occurred 
        // in calling EnumDevices2.
        return hr;
    }

    // Length of all the strings we'll send in. 
    const UINT MAX_CHARS = 100;

    // Iterate through devices.
    while(TRUE)
    {
        // Get a device handle.
        IWMDMDevice *pIWMDMDevice;
        ULONG ulFetched = 0;
        hr = pEnumDevice->Next(1, &pIWMDMDevice, &ulFetched);
        if ((hr != S_OK) || (ulFetched != 1))
        {
            break;
        }
        
        // Get a display icon for the device.
        ULONG deviceIcon = 0;
        hr = pIWMDMDevice->GetDeviceIcon(&deviceIcon);

        // Print the device manufacturer.
        WCHAR manufacturer[MAX_CHARS];
        hr = pIWMDMDevice->GetManufacturer((LPWSTR)&manufacturer, MAX_CHARS);
        if (hr == S_OK)
        {
            // TODO: Display manufacturer name.
        }

        // Get the device name.
        WCHAR name[MAX_CHARS];
        hr = pIWMDMDevice->GetName((LPWSTR)&name, MAX_CHARS);
        if (hr == S_OK)
        {
            // TODO: Display name.
        }

        // TODO: Get other device information if wanted.

        // Obtain an IWMDMDevice2 interface and call some methods.
        CComQIPtr<IWMDMDevice2> pIWMDMDevice2(pIWMDMDevice);
        if (pIWMDMDevice2 != NULL)
        {
            // Get the canonical name.
            WCHAR canonicalName[MAX_CHARS];
            hr = pIWMDMDevice2->GetCanonicalName(canonicalName, MAX_CHARS);
            if (hr == S_OK)
            {
                // TODO: Display canonical name.
            }
        }

        // Obtain an IWMDMDevice3 interface and call some methods.
        CComQIPtr<IWMDMDevice3>pIWMDMDevice3(pIWMDMDevice);
        if (pIWMDMDevice3 != NULL)
        {
            // Find out what protocol is being used.
            PROPVARIANT val;
            PropVariantInit(&val);
            hr = pIWMDMDevice3->GetProperty(g_wszWMDMDeviceProtocol, &val);

            if (hr == S_OK)
            {
                if (*val.puuid == WMDM_DEVICE_PROTOCOL_RAPI)
                {
                    // TODO: Display message indicating device is a RAPI device.
                }
                else if (*val.puuid == WMDM_DEVICE_PROTOCOL_MTP)
                {
                    / /TODO: Display message indicating device is an MTP device.
                }
                else if (*val.puuid == WMDM_DEVICE_PROTOCOL_MSC)
                {
                    // TODO: Display message indicating device is an MSC device.
                }
                else
                {
                    // TODO: Display message indicating that the 
                    // application encountered an unknown protocol.
                }
                PropVariantClear(&val);
            }
        }

        // Examine the device capabilities. You could use some of these
        // to enable or disable the application's UI elements.
        CComQIPtr<IWMDMDeviceControl> pDeviceControl(pIWMDMDevice);
        if (pDeviceControl != NULL)
        {
            DWORD caps = 0;
            hr = pDeviceControl->GetCapabilities(&caps);
            if (caps & WMDM_DEVICECAP_CANPLAY)
            {
                // TODO: Display message indicating that the media 
                // device can play MP3 audio.
            }
            // TODO: Test for other capabilities here.
        }
    } // Get the next device.
    return hr;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**création d’une Application de Gestionnaire de périphériques multimédia Windows**](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 




