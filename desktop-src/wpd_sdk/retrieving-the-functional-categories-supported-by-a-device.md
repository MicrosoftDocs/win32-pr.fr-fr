---
description: Récupération des catégories fonctionnelles prises en charge par un appareil
ms.assetid: 7748e111-9987-4685-8fc8-10c5d4631080
title: Récupération des catégories fonctionnelles prises en charge par un appareil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6514c6255fa089dc235b5edd8a25b5ef581aee84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866742"
---
# <a name="retrieving-the-functional-categories-supported-by-a-device"></a><span data-ttu-id="c3b5c-103">Récupération des catégories fonctionnelles prises en charge par un appareil</span><span class="sxs-lookup"><span data-stu-id="c3b5c-103">Retrieving the Functional Categories Supported by a Device</span></span>

<span data-ttu-id="c3b5c-104">Les appareils mobiles Windows peuvent prendre en charge une ou plusieurs catégories fonctionnelles.</span><span class="sxs-lookup"><span data-stu-id="c3b5c-104">Windows Portable Devices may support one or more functional categories.</span></span> <span data-ttu-id="c3b5c-105">Ces catégories sont décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="c3b5c-105">These categories are described in the following table.</span></span>



| <span data-ttu-id="c3b5c-106">Category</span><span class="sxs-lookup"><span data-stu-id="c3b5c-106">Category</span></span>                    | <span data-ttu-id="c3b5c-107">Description</span><span class="sxs-lookup"><span data-stu-id="c3b5c-107">Description</span></span>                                                                          |
|-----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c3b5c-108">Capture audio</span><span class="sxs-lookup"><span data-stu-id="c3b5c-108">Audio capture</span></span>               | <span data-ttu-id="c3b5c-109">L’appareil peut être utilisé pour enregistrer l’audio.</span><span class="sxs-lookup"><span data-stu-id="c3b5c-109">The device can be used to record audio.</span></span>                                              |
| <span data-ttu-id="c3b5c-110">Informations de rendu</span><span class="sxs-lookup"><span data-stu-id="c3b5c-110">Rendering information</span></span>       | <span data-ttu-id="c3b5c-111">L’appareil fournit des données décrivant les fichiers multimédias qu’il est capable de rendre.</span><span class="sxs-lookup"><span data-stu-id="c3b5c-111">The device provides data describing the media files that it is capable of rendering.</span></span> |
| <span data-ttu-id="c3b5c-112">SMS (Short Message Service)</span><span class="sxs-lookup"><span data-stu-id="c3b5c-112">Short message service (SMS)</span></span> | <span data-ttu-id="c3b5c-113">L’appareil prend en charge la messagerie texte.</span><span class="sxs-lookup"><span data-stu-id="c3b5c-113">The device supports text messaging.</span></span>                                                  |
| <span data-ttu-id="c3b5c-114">Capture d’image continue</span><span class="sxs-lookup"><span data-stu-id="c3b5c-114">Still image capture</span></span>         | <span data-ttu-id="c3b5c-115">L’appareil peut être utilisé pour capturer des images fixes.</span><span class="sxs-lookup"><span data-stu-id="c3b5c-115">The device can be used to capture still images.</span></span>                                      |
| <span data-ttu-id="c3b5c-116">Stockage</span><span class="sxs-lookup"><span data-stu-id="c3b5c-116">Storage</span></span>                     | <span data-ttu-id="c3b5c-117">L’appareil peut être utilisé pour stocker des fichiers.</span><span class="sxs-lookup"><span data-stu-id="c3b5c-117">The device can be used to store files.</span></span>                                               |



 

<span data-ttu-id="c3b5c-118">La fonction ListFunctionalCategories dans le module DeviceCapabilities. cpp illustre la récupération des catégories fonctionnelles pour un appareil sélectionné.</span><span class="sxs-lookup"><span data-stu-id="c3b5c-118">The ListFunctionalCategories function in the DeviceCapabilities.cpp module demonstrates the retrieval of functional categories for a selected device.</span></span>

<span data-ttu-id="c3b5c-119">Votre application peut récupérer les catégories fonctionnelles prises en charge par un appareil à l’aide des interfaces décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="c3b5c-119">Your application can retrieve the functional categories supported by a device by using the interfaces described in the following table.</span></span>



| <span data-ttu-id="c3b5c-120">Interface</span><span class="sxs-lookup"><span data-stu-id="c3b5c-120">Interface</span></span>                                                                                      | <span data-ttu-id="c3b5c-121">Description</span><span class="sxs-lookup"><span data-stu-id="c3b5c-121">Description</span></span>                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [<span data-ttu-id="c3b5c-122">**Interface IPortableDeviceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="c3b5c-122">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | <span data-ttu-id="c3b5c-123">Fournit l’accès aux méthodes de récupération de catégorie fonctionnelle.</span><span class="sxs-lookup"><span data-stu-id="c3b5c-123">Provides access to the functional-category retrieval methods.</span></span> |
| [<span data-ttu-id="c3b5c-124">**Interface IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="c3b5c-124">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="c3b5c-125">Permet d’énumérer et de stocker les données de catégorie fonctionnelle.</span><span class="sxs-lookup"><span data-stu-id="c3b5c-125">Used to enumerate and store functional-category data.</span></span>         |



 

<span data-ttu-id="c3b5c-126">La première tâche accomplie par l’exemple d’application est la récupération d’un objet [**IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities) , qui est utilisé pour récupérer les catégories fonctionnelles sur l’appareil sélectionné.</span><span class="sxs-lookup"><span data-stu-id="c3b5c-126">The first task accomplished by the sample application is the retrieval of an [**IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities) object, which is used to retrieve the functional categories on the selected device.</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceCapabilities>            pCapabilities;
CComPtr<IPortableDevicePropVariantCollection>   pCategories;
DWORD dwNumCategories = 0;

if (pDevice == NULL)
{
    printf("! A NULL IPortableDevice interface pointer was received\n");
    return;
}

// Get an IPortableDeviceCapabilities interface from the IPortableDevice interface to
// access the device capabilities-specific methods.
hr = pDevice->Capabilities(&pCapabilities);
if (FAILED(hr))
{
    printf("! Failed to get IPortableDeviceCapabilities from IPortableDevice, hr = 0x%lx\n",hr);
}

// Get all functional categories supported by the device.
if (SUCCEEDED(hr))
{
    hr = pCapabilities->GetFunctionalCategories(&pCategories);
    if (FAILED(hr))
    {
        printf("! Failed to get functional categories from the device, hr = 0x%lx\n",hr);
    }
}
```



<span data-ttu-id="c3b5c-127">Les catégories récupérées sont stockées dans un objet [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="c3b5c-127">The retrieved categories are stored in an [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) object.</span></span>

<span data-ttu-id="c3b5c-128">L’étape suivante est l’énumération et l’affichage des catégories prises en charge.</span><span class="sxs-lookup"><span data-stu-id="c3b5c-128">The next step is the enumeration and display of the supported categories.</span></span> <span data-ttu-id="c3b5c-129">La première étape que l’exemple d’application effectue est de récupérer le nombre de catégories prises en charge.</span><span class="sxs-lookup"><span data-stu-id="c3b5c-129">The first step that the sample application accomplishes is to retrieve the count of supported categories.</span></span> <span data-ttu-id="c3b5c-130">Il utilise ensuite ce nombre pour itérer au sein de l’objet [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) qui contient les catégories prises en charge.</span><span class="sxs-lookup"><span data-stu-id="c3b5c-130">It then uses this count to iterate through the [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) object that contains the supported categories.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = pCategories->GetCount(&dwNumCategories);
    if (FAILED(hr))
    {
        printf("! Failed to get number of functional categories, hr = 0x%lx\n",hr);
    }
}

printf("\n%d Functional Categories Found on the device\n\n", dwNumCategories);

// Loop through each functional category and display its name
if (SUCCEEDED(hr))
{
    for (DWORD dwIndex = 0; dwIndex < dwNumCategories; dwIndex++)
    {
        PROPVARIANT pv = {0};
        PropVariantInit(&pv);
        hr = pCategories->GetAt(dwIndex, &pv);
        if (SUCCEEDED(hr))
        {
            // We have a functional category.  It is assumed that
            // functional categories are returned as VT_CLSID
            // VarTypes.

            if (pv.puuid != NULL)
            {
                // Display the functional category name
                DisplayFunctionalCategory(*pv.puuid);
                printf("\n");
            }
        }

        PropVariantClear(&pv);
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="c3b5c-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c3b5c-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3b5c-132">**Interface IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="c3b5c-132">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="c3b5c-133">**Interface IPortableDeviceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="c3b5c-133">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)
</dt> <dt>

[<span data-ttu-id="c3b5c-134">**Interface IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="c3b5c-134">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="c3b5c-135">**Guide de programmation**</span><span class="sxs-lookup"><span data-stu-id="c3b5c-135">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



