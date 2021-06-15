---
title: Énumération des appareils (WPD)
description: Découvrez comment une application énumère les appareils à l’aide de la fonction EnumerateAllDevices, qui obtient le nombre d’appareils connectés et les informations spécifiques à l’appareil.
ms.assetid: 28ded3cf-b0c8-4c90-ab39-efc879adb6e7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6465b04e6f1a18a0bdb74f0ce883cf9161371fb6
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068595"
---
# <a name="enumerating-devices-wpd"></a><span data-ttu-id="6b700-103">Énumération des appareils (WPD)</span><span class="sxs-lookup"><span data-stu-id="6b700-103">Enumerating devices (WPD)</span></span>

<span data-ttu-id="6b700-104">La première tâche effectuée par la plupart des applications est l’énumération des appareils connectés à l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="6b700-104">The first task completed by most applications is the enumeration of the devices connected to the computer.</span></span> <span data-ttu-id="6b700-105">Cette tâche et la récupération des informations de l’appareil (telles que le fabricant, le nom convivial et la description) sont prises en charge par l’interface [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) .</span><span class="sxs-lookup"><span data-stu-id="6b700-105">This task, and the retrieval of device information (such as manufacturer, friendly name, and description), is supported by the [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) interface.</span></span>

<span data-ttu-id="6b700-106">La fonction EnumerateAllDevices dans le module DeviceEnumeration. cpp contient du code qui illustre la récupération du nombre d’appareils connectés et, une fois le nombre récupéré, la récupération des informations spécifiques à l’appareil pour chaque périphérique connecté.</span><span class="sxs-lookup"><span data-stu-id="6b700-106">The EnumerateAllDevices function in the DeviceEnumeration.cpp module contains code that demonstrates the retrieval of the count of connected devices and, once the count is retrieved, the retrieval of device-specific information for each connected device.</span></span>

<span data-ttu-id="6b700-107">La fonction EnumerateAllDevices effectue quatre tâches principales :</span><span class="sxs-lookup"><span data-stu-id="6b700-107">The EnumerateAllDevices function accomplishes four primary tasks:</span></span>

1.  <span data-ttu-id="6b700-108">Crée l’objet portable Device Manager.</span><span class="sxs-lookup"><span data-stu-id="6b700-108">Creates the portable device manager object.</span></span>
2.  <span data-ttu-id="6b700-109">Récupère le nombre d’appareils connectés.</span><span class="sxs-lookup"><span data-stu-id="6b700-109">Retrieves a count of connected devices.</span></span>
3.  <span data-ttu-id="6b700-110">Récupère les informations de l’appareil (pour les appareils connectés).</span><span class="sxs-lookup"><span data-stu-id="6b700-110">Retrieves device information (for the connected devices).</span></span>
4.  <span data-ttu-id="6b700-111">Libère la mémoire utilisée lors de la récupération des informations de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6b700-111">Frees the memory used when retrieving the device information.</span></span>

<span data-ttu-id="6b700-112">Chacune de ces quatre tâches est décrite plus en détail dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="6b700-112">Each of these four tasks is described in more detail in the following sections.</span></span>

<span data-ttu-id="6b700-113">La première étape du processus d’énumération des appareils consiste à créer un objet portable Device Manager.</span><span class="sxs-lookup"><span data-stu-id="6b700-113">The first step in the device enumeration process is the creation of a portable device manager object.</span></span> <span data-ttu-id="6b700-114">Pour ce faire, appelez la fonction CoCreateInstance et passez l’identificateur de classe (CLSID) de l’objet, en spécifiant le contexte dans lequel le code s’exécutera, en spécifiant un identificateur de référence pour l’interface IPortableDeviceManager, puis en fournissant une variable pointeur qui reçoit le pointeur d’interface IPortableDeviceManager.</span><span class="sxs-lookup"><span data-stu-id="6b700-114">This is done by calling the CoCreateInstance function and passing the class identifier (CLSID) for the object, specifying the context in which the code will run, specifying a reference identifier for the IPortableDeviceManager interface, and then supplying a pointer variable that receives the IPortableDeviceManager interface pointer.</span></span>


```C++
HRESULT hr = CoCreateInstance(CLSID_PortableDeviceManager,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(&pPortableDeviceManager));
if (FAILED(hr))
{
    printf("! Failed to CoCreateInstance CLSID_PortableDeviceManager, hr = 0x%lx\n",hr);
}
```



<span data-ttu-id="6b700-115">Une fois que vous obtenez un pointeur d’interface [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) , vous pouvez commencer à appeler des méthodes sur cette interface.</span><span class="sxs-lookup"><span data-stu-id="6b700-115">Once you obtain an [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) interface pointer, you can begin calling methods on this interface.</span></span> <span data-ttu-id="6b700-116">La première méthode appelée dans la fonction EnumerateAllDevices est [**IPortableDeviceManager :: GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices).</span><span class="sxs-lookup"><span data-stu-id="6b700-116">The first method called in the EnumerateAllDevices function is [**IPortableDeviceManager::GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices).</span></span> <span data-ttu-id="6b700-117">Lorsque cette méthode est appelée avec le premier argument ayant la valeur **null**, elle retourne le nombre d’appareils connectés.</span><span class="sxs-lookup"><span data-stu-id="6b700-117">When this method is called with the first argument set to **NULL**, it returns the count of connected devices.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = pPortableDeviceManager->GetDevices(NULL, &cPnPDeviceIDs);
    if (FAILED(hr))
    {
        printf("! Failed to get number of devices on the system, hr = 0x%lx\n",hr);
    }
}

// Report the number of devices found.  NOTE: we will report 0, if an error
// occured.

printf("\n%d Windows Portable Device(s) found on the system\n\n", cPnPDeviceIDs);
```



<span data-ttu-id="6b700-118">Une fois que vous avez récupéré le nombre d’appareils connectés, vous pouvez utiliser cette valeur pour récupérer les informations de chaque appareil connecté.</span><span class="sxs-lookup"><span data-stu-id="6b700-118">After you have retrieved the count of connected devices, you can use this value to retrieve device information for each connected device.</span></span> <span data-ttu-id="6b700-119">Ce processus commence par passer un tableau de pointeurs de chaîne comme premier argument et le nombre d’éléments que ce tableau peut conserver comme deuxième argument (ce nombre doit être au moins égal au nombre d’appareils disponibles).</span><span class="sxs-lookup"><span data-stu-id="6b700-119">This process begins by passing an array of string pointers as the first argument and a count of the number of elements that this array can hold as the second argument (this count should at least be equal to the number of available devices).</span></span>

<span data-ttu-id="6b700-120">Les chaînes retournées par cette méthode sont les noms Plug-and-Play des appareils connectés.</span><span class="sxs-lookup"><span data-stu-id="6b700-120">The strings returned by this method are the Plug and Play names of the connected devices.</span></span> <span data-ttu-id="6b700-121">Ces noms, à leur tour, sont passés à d’autres méthodes sur l’interface [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) pour récupérer des informations spécifiques à l’appareil, telles que le nom convivial, le nom du fabricant et la description de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6b700-121">These names, in turn, are passed to other methods on the [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) interface to retrieve device-specific information such as the friendly name, the manufacturer's name, and the device description.</span></span> <span data-ttu-id="6b700-122">(Ces noms sont également utilisés pour ouvrir une connexion à l’appareil quand une application appelle la méthode [**IPortableDevice :: Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open) .)</span><span class="sxs-lookup"><span data-stu-id="6b700-122">(These names are also used to open a connection to the device when an application calls the [**IPortableDevice::Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open) method.)</span></span>


```C++
if (SUCCEEDED(hr) && (cPnPDeviceIDs > 0))
{
    pPnpDeviceIDs = new (std::nothrow) PWSTR[cPnPDeviceIDs];
    if (pPnpDeviceIDs != NULL)
    {
        DWORD dwIndex = 0;

        hr = pPortableDeviceManager->GetDevices(pPnpDeviceIDs, &cPnPDeviceIDs);
        if (SUCCEEDED(hr))
        {
            // For each device found, display the devices friendly name,
            // manufacturer, and description strings.
            for (dwIndex = 0; dwIndex < cPnPDeviceIDs; dwIndex++)
            {
                printf("[%d] ", dwIndex);
                DisplayFriendlyName(pPortableDeviceManager, pPnpDeviceIDs[dwIndex]);
                printf("    ");
                DisplayManufacturer(pPortableDeviceManager, pPnpDeviceIDs[dwIndex]);
                printf("    ");
                DisplayDescription(pPortableDeviceManager, pPnpDeviceIDs[dwIndex]);
            }
        }
        else
        {
            printf("! Failed to get the device list from the system, hr = 0x%lx\n",hr);
        }
```



<span data-ttu-id="6b700-123">Une fois que vous avez récupéré les informations de l’appareil, vous devrez libérer la mémoire associée aux chaînes pointées par le tableau de pointeurs de chaîne.</span><span class="sxs-lookup"><span data-stu-id="6b700-123">Once you've retrieved the device information, you will need to free the memory associated with the strings pointed to by the array of string pointers.</span></span> <span data-ttu-id="6b700-124">Vous devrez également supprimer ce tableau.</span><span class="sxs-lookup"><span data-stu-id="6b700-124">You will also need to delete this array.</span></span>


```C++
for (dwIndex = 0; dwIndex < cPnPDeviceIDs; dwIndex++)
{
    CoTaskMemFree(pPnpDeviceIDs[dwIndex]);
    pPnpDeviceIDs[dwIndex] = NULL;
}

// Delete the array of PWSTR pointers
delete [] pPnpDeviceIDs;
pPnpDeviceIDs = NULL;
```



## <a name="related-topics"></a><span data-ttu-id="6b700-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6b700-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b700-126">**Interface IPortableDeviceManager**</span><span class="sxs-lookup"><span data-stu-id="6b700-126">**IPortableDeviceManager Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager)
</dt> <dt>

[<span data-ttu-id="6b700-127">**Guide de programmation**</span><span class="sxs-lookup"><span data-stu-id="6b700-127">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



