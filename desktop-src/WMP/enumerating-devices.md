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
# <a name="enumerating-devices"></a><span data-ttu-id="55b74-112">Énumération des appareils</span><span class="sxs-lookup"><span data-stu-id="55b74-112">Enumerating Devices</span></span>

<span data-ttu-id="55b74-113">Le lecteur Windows Media représente des appareils portables à l’aide de l’interface **IWMPSyncDevice** .</span><span class="sxs-lookup"><span data-stu-id="55b74-113">Windows Media Player represents portable devices by using the **IWMPSyncDevice** interface.</span></span> <span data-ttu-id="55b74-114">L’exemple de code suivant montre une fonction qui crée un tableau de pointeurs vers **IWMPSyncDevice**.</span><span class="sxs-lookup"><span data-stu-id="55b74-114">The following example code shows a function that creates an array of pointers to **IWMPSyncDevice**.</span></span> <span data-ttu-id="55b74-115">Chaque pointeur dans le tableau représente un appareil pour lequel le lecteur Windows Media a stocké des informations.</span><span class="sxs-lookup"><span data-stu-id="55b74-115">Each pointer in the array represents a device for which Windows Media Player has stored information.</span></span> <span data-ttu-id="55b74-116">Il n’est pas nécessaire qu’un appareil soit connecté à l’ordinateur. il ne doit pas non plus être associé à l’instance actuelle du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="55b74-116">A device is not required to be connected to the computer, nor is it required to have a partnership with the current Windows Media Player instance.</span></span>

<span data-ttu-id="55b74-117">Vous devez énumérer les appareils chaque fois que vous recevez l’événement **DeviceConnect** ou **DeviceDisconnect** .</span><span class="sxs-lookup"><span data-stu-id="55b74-117">You should enumerate devices whenever you receive the **DeviceConnect** event or the **DeviceDisconnect** event.</span></span>

<span data-ttu-id="55b74-118">La fonction suivante énumère les appareils.</span><span class="sxs-lookup"><span data-stu-id="55b74-118">The following function enumerates devices.</span></span> <span data-ttu-id="55b74-119">Le paramètre *bConnectedOnly* spécifie s’il faut énumérer uniquement les appareils actuellement connectés à l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="55b74-119">The *bConnectedOnly* parameter specifies whether to enumerate only devices currently connected to the user's computer.</span></span>


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



<span data-ttu-id="55b74-120">Vous pouvez utiliser du code similaire pour récupérer d’autres listes d’appareils de ce type.</span><span class="sxs-lookup"><span data-stu-id="55b74-120">You might use similar code to retrieve other such device lists.</span></span> <span data-ttu-id="55b74-121">Par exemple, vous pouvez utiliser [IWMPSyncDevice :: obtenir l' \_ État](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) pour créer un tableau d’appareils pour lequel un partenariat existe.</span><span class="sxs-lookup"><span data-stu-id="55b74-121">For example, you could use [IWMPSyncDevice::get\_status](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) to create an array of devices for which a partnership exists.</span></span>

## <a name="related-topics"></a><span data-ttu-id="55b74-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="55b74-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55b74-123">**IWMPEvents2 ::D eviceConnect**</span><span class="sxs-lookup"><span data-stu-id="55b74-123">**IWMPEvents2::DeviceConnect**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents2-deviceconnect)
</dt> <dt>

[<span data-ttu-id="55b74-124">**IWMPEvents2 ::D eviceDisconnect**</span><span class="sxs-lookup"><span data-stu-id="55b74-124">**IWMPEvents2::DeviceDisconnect**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents2-devicedisconnect)
</dt> <dt>

[<span data-ttu-id="55b74-125">**Interface IWMPSyncDevice**</span><span class="sxs-lookup"><span data-stu-id="55b74-125">**IWMPSyncDevice Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)
</dt> <dt>

[<span data-ttu-id="55b74-126">**IWMPSyncDevice : \_ : Connectez-vous**</span><span class="sxs-lookup"><span data-stu-id="55b74-126">**IWMPSyncDevice::get\_connected**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_connected)
</dt> <dt>

[<span data-ttu-id="55b74-127">**Interface IWMPSyncServices**</span><span class="sxs-lookup"><span data-stu-id="55b74-127">**IWMPSyncServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncservices)
</dt> <dt>

[<span data-ttu-id="55b74-128">**Utilisation d’appareils mobiles**</span><span class="sxs-lookup"><span data-stu-id="55b74-128">**Working with Portable Devices**</span></span>](working-with-portable-devices.md)
</dt> </dl>

 

 




