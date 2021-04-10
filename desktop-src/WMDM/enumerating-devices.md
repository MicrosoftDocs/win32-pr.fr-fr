---
title: Énumération des appareils Windows Media Gestionnaire de périphériques
description: Énumération des appareils
ms.assetid: c5935681-b530-4446-a026-7ddc74084d23
keywords:
- Gestionnaire de périphériques Windows Media, énumération des appareils
- Gestionnaire de périphériques, énumération des appareils
- Guide de programmation, énumération des appareils
- applications de bureau, énumération des appareils
- création d’applications Windows Media Gestionnaire de périphériques, énumération d’appareils
- énumération des appareils
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3584e625f54ea4e5c601f2a32865515c824cfcd
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/23/2019
ms.locfileid: "104101117"
---
# <a name="enumerating-windows-media-device-manager-devices"></a><span data-ttu-id="fa9ee-109">Énumération des appareils Windows Media Gestionnaire de périphériques</span><span class="sxs-lookup"><span data-stu-id="fa9ee-109">Enumerating Windows Media Device Manager devices</span></span>

<span data-ttu-id="fa9ee-110">Après l’authentification d’une application, vous pouvez commencer à énumérer les appareils détectés par les Gestionnaire de périphériques Windows Media.</span><span class="sxs-lookup"><span data-stu-id="fa9ee-110">After authenticating an application, you can begin to enumerate the devices detected by Windows Media Device Manager.</span></span> <span data-ttu-id="fa9ee-111">L’énumération est effectuée à l’aide d’une interface d’énumération, [**IWMDMEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice), obtenue à l’aide de [**IWMDeviceManager2 :: EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2) ou [**IWMDeviceManager :: EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices).</span><span class="sxs-lookup"><span data-stu-id="fa9ee-111">Enumeration is done by using an enumeration interface, [**IWMDMEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice), obtained by using either [**IWMDeviceManager2::EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2) or [**IWMDeviceManager::EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices).</span></span> <span data-ttu-id="fa9ee-112">En cas de prise en charge, utilisez la méthode **EnumDevices2** , car la version antérieure retournait uniquement les interfaces héritées sur les appareils, tandis que la nouvelle version retourne à la fois les interfaces héritées et nouvelles.</span><span class="sxs-lookup"><span data-stu-id="fa9ee-112">If supported, use the **EnumDevices2** method, because the earlier version only returned legacy interfaces on devices, whereas the new version returns both the legacy and the new interfaces.</span></span>

<span data-ttu-id="fa9ee-113">Avant d’obtenir un énumérateur, vous devez décider de la vue d’énumération à utiliser.</span><span class="sxs-lookup"><span data-stu-id="fa9ee-113">Before obtaining an enumerator, you should decide what enumeration view to use.</span></span> <span data-ttu-id="fa9ee-114">Certains appareils exposent chaque stockage sous la forme d’un autre appareil.</span><span class="sxs-lookup"><span data-stu-id="fa9ee-114">Some devices expose each storage as a different device.</span></span> <span data-ttu-id="fa9ee-115">Par exemple, deux cartes mémoire flash sur un appareil sont énumérées comme s’il s’agissait de périphériques distincts.</span><span class="sxs-lookup"><span data-stu-id="fa9ee-115">For example, two flash memory cards on a device will enumerate as if they were separate devices.</span></span> <span data-ttu-id="fa9ee-116">Vous pouvez spécifier que tous les stockages sur un appareil sont énumérés comme un seul appareil.</span><span class="sxs-lookup"><span data-stu-id="fa9ee-116">You can specify that all storages on a device are enumerated together as a single device.</span></span> <span data-ttu-id="fa9ee-117">Vous ne pouvez définir cette préférence qu’une seule fois dans votre application ; Si vous souhaitez le modifier, vous devez arrêter l’application et la redémarrer.</span><span class="sxs-lookup"><span data-stu-id="fa9ee-117">You can set this preference only once in your application; if you want to change it, you must shut down the application and restart it.</span></span> <span data-ttu-id="fa9ee-118">Toutefois, Notez que les appareils hérités ignorent parfois une demande d’énumération de stockages d’appareils distincts comme un seul appareil et continuent de les énumérer séparément.</span><span class="sxs-lookup"><span data-stu-id="fa9ee-118">However, note that legacy devices will sometimes ignore a request to enumerate separate device storages as a single device, and continue to enumerate them separately.</span></span>

<span data-ttu-id="fa9ee-119">Les étapes suivantes montrent comment énumérer les appareils connectés :</span><span class="sxs-lookup"><span data-stu-id="fa9ee-119">The following steps show how to enumerate connected devices:</span></span>

1.  <span data-ttu-id="fa9ee-120">Définissez la préférence d’énumération des appareils à l’aide de [**IWMDeviceManager3 :: SetDeviceEnumPreference**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager3-setdeviceenumpreference).</span><span class="sxs-lookup"><span data-stu-id="fa9ee-120">Set the device enumeration preference using [**IWMDeviceManager3::SetDeviceEnumPreference**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager3-setdeviceenumpreference).</span></span> <span data-ttu-id="fa9ee-121">Si cette méthode n’est pas appelée, la méthode par défaut consiste à afficher les stockages comme des appareils distincts.</span><span class="sxs-lookup"><span data-stu-id="fa9ee-121">If this method is not called, the default method is to show storages as separate devices.</span></span> <span data-ttu-id="fa9ee-122">Pour déterminer si les « appareils » individuels sont en fait des stockages sur le même appareil, appelez [**IWMDMDevice2 :: GetCanonicalName**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice2-getcanonicalname); les stockages à partir du même appareil retournent des valeurs identiques, à l’exception du chiffre final situé après le dernier signe « $ ».</span><span class="sxs-lookup"><span data-stu-id="fa9ee-122">To determine whether individual "devices" are actually storages on the same device, call [**IWMDMDevice2::GetCanonicalName**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice2-getcanonicalname); storages from the same device will return identical values, except for the final digit after the last "$" sign.</span></span>
2.  <span data-ttu-id="fa9ee-123">Interrogez [**IWMDeviceManager**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager) ou [**IWMDeviceManager2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager2), puis appelez [**IWMDeviceManager2 :: EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2) pour obtenir l’interface de l’énumérateur d’appareil, [**IWMDMEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice).</span><span class="sxs-lookup"><span data-stu-id="fa9ee-123">Query for [**IWMDeviceManager**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager) or [**IWMDeviceManager2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager2), and then call [**IWMDeviceManager2::EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2) to obtain the device enumerator interface, [**IWMDMEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice).</span></span> <span data-ttu-id="fa9ee-124">(S’il est pris en charge, utilisez **EnumDevices2**, ce qui est plus efficace, car la version antérieure peut ne pas retourner de périphériques MTP).</span><span class="sxs-lookup"><span data-stu-id="fa9ee-124">(If supported, use **EnumDevices2**, which is more efficient, as the earlier version may not return MTP devices).</span></span>
3.  <span data-ttu-id="fa9ee-125">Appelez la méthode [**IWMDMEnumDevices :: Next**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmenumdevice-next) pour récupérer un ou plusieurs appareils à la fois.</span><span class="sxs-lookup"><span data-stu-id="fa9ee-125">Call the [**IWMDMEnumDevices::Next**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmenumdevice-next) method to retrieve one or more devices at a time.</span></span> <span data-ttu-id="fa9ee-126">Continuez à appeler cette méthode jusqu’à ce que la méthode retourne S \_ false ou un message d’erreur.</span><span class="sxs-lookup"><span data-stu-id="fa9ee-126">Continue to call this method until the method returns S\_FALSE or an error message.</span></span> <span data-ttu-id="fa9ee-127">Si vous récupérez un seul appareil à la fois, vous n’avez pas besoin d’allouer un tableau pour stocker les appareils.</span><span class="sxs-lookup"><span data-stu-id="fa9ee-127">If retrieving only one device at a time, you do not need to allocate an array to hold the devices.</span></span>

<span data-ttu-id="fa9ee-128">Étant donné que les utilisateurs peuvent attacher ou supprimer des appareils de l’ordinateur pendant l’exécution de votre application, il est conseillé d’implémenter la notification de la connexion ou de la suppression de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="fa9ee-128">Because users can attach or remove devices from the computer while your application is running, it is a good idea to implement notification of device connection or removal.</span></span> <span data-ttu-id="fa9ee-129">Cela s’effectue en implémentant l’interface [**IWMDMNotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification) et en l’inscrivant.</span><span class="sxs-lookup"><span data-stu-id="fa9ee-129">This is done by implementing the [**IWMDMNotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification) interface and registering it.</span></span> <span data-ttu-id="fa9ee-130">Pour plus d’informations, consultez la page [activation des notifications](enabling-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="fa9ee-130">For more information on this, see [Enabling Notifications](enabling-notifications.md).</span></span>

<span data-ttu-id="fa9ee-131">Le code C++ suivant énumère les appareils et demande des informations sur chaque appareil.</span><span class="sxs-lookup"><span data-stu-id="fa9ee-131">The following C++ code enumerates devices and requests information about each device.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="fa9ee-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fa9ee-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa9ee-133">**Création d’une application Windows Media Gestionnaire de périphériques**</span><span class="sxs-lookup"><span data-stu-id="fa9ee-133">**Creating a Windows Media Device Manager Application**</span></span>](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 




