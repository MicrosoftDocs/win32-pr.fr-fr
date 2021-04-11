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
# <a name="establishing-a-connection"></a><span data-ttu-id="70d8e-103">Établissement d’une connexion</span><span class="sxs-lookup"><span data-stu-id="70d8e-103">Establishing a Connection</span></span>

<span data-ttu-id="70d8e-104">Une fois que l’utilisateur a sélectionné un appareil, la fonction ChooseDevice appelle à son tour la méthode [**IPortableDevice :: Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open) pour établir une connexion entre l’application et l’appareil.</span><span class="sxs-lookup"><span data-stu-id="70d8e-104">Once the user selects a device, the ChooseDevice function, in turn, calls the [**IPortableDevice::Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open) method to establish a connection between the application and the device.</span></span> <span data-ttu-id="70d8e-105">La méthode IPortableDevice :: Open accepte deux arguments :</span><span class="sxs-lookup"><span data-stu-id="70d8e-105">The IPortableDevice::Open method takes two arguments:</span></span>

-   <span data-ttu-id="70d8e-106">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom Plug-and-Play du périphérique.</span><span class="sxs-lookup"><span data-stu-id="70d8e-106">A pointer to a null-terminated string that specifies the Plug and Play name of the device.</span></span> <span data-ttu-id="70d8e-107">(Cette chaîne est récupérée en appelant la méthode [**IPortableDeviceManager :: GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices) .)</span><span class="sxs-lookup"><span data-stu-id="70d8e-107">(This string is retrieved by calling the [**IPortableDeviceManager::GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices) method.)</span></span>
-   <span data-ttu-id="70d8e-108">Pointeur vers une [**interface IPortableDeviceValues**](iportabledevicevalues.md) qui spécifie les informations sur le client pour l’application.</span><span class="sxs-lookup"><span data-stu-id="70d8e-108">A pointer to an [**IPortableDeviceValues interface**](iportabledevicevalues.md) that specifies client information for the application.</span></span>


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



<span data-ttu-id="70d8e-109">Pour Windows 7, [**IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice) prend en charge deux CLSID pour **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="70d8e-109">For Windows 7, [**IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice) supports two CLSIDs for **CoCreateInstance**.</span></span> <span data-ttu-id="70d8e-110">**CLSID \_ PortableDevice** retourne un pointeur **IPortableDevice** qui n’agrège pas le marshaleur libre de threads. **CLSID \_ PortableDeviceFTM** est un nouveau CLSID qui retourne un pointeur **IPortableDevice** qui agrège le marshaleur libre de threads.</span><span class="sxs-lookup"><span data-stu-id="70d8e-110">**CLSID\_PortableDevice** returns an **IPortableDevice** pointer that does not aggregate the free-threaded marshaler; **CLSID\_PortableDeviceFTM** is a new CLSID that returns an **IPortableDevice** pointer that aggregates the free-threaded marshaler.</span></span> <span data-ttu-id="70d8e-111">Les deux pointeurs prennent en charge la même fonctionnalité dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="70d8e-111">Both pointers support the same functionality otherwise.</span></span>

<span data-ttu-id="70d8e-112">Les applications qui résident dans des cloisonnements à thread unique doivent utiliser le **CLSID \_ PortableDeviceFTM** , car cela élimine la surcharge du marshaling de pointeur d’interface.</span><span class="sxs-lookup"><span data-stu-id="70d8e-112">Applications that live in Single Threaded Apartments should use **CLSID\_PortableDeviceFTM** as this eliminates the overhead of interface pointer marshaling.</span></span> <span data-ttu-id="70d8e-113">**CLSID \_ PortableDevice** est toujours pris en charge pour les applications héritées.</span><span class="sxs-lookup"><span data-stu-id="70d8e-113">**CLSID\_PortableDevice** is still supported for legacy applications.</span></span>

## <a name="related-topics"></a><span data-ttu-id="70d8e-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="70d8e-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70d8e-115">**Sélection d’un appareil**</span><span class="sxs-lookup"><span data-stu-id="70d8e-115">**Selecting a Device**</span></span>](selecting-a-device.md)
</dt> </dl>

 

 



