---
description: Récupération des types de contenu pris en charge par un appareil
ms.assetid: 1cedb8d9-2476-420c-bab4-c8a032af781b
title: Récupération des types de contenu pris en charge par un appareil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e1b37160065be3130fca687f5f3277d9108a6ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530659"
---
# <a name="retrieving-the-content-types-supported-by-a-device"></a><span data-ttu-id="dbba9-103">Récupération des types de contenu pris en charge par un appareil</span><span class="sxs-lookup"><span data-stu-id="dbba9-103">Retrieving the Content Types Supported by a Device</span></span>

<span data-ttu-id="dbba9-104">Comme indiqué dans la rubrique [récupération des catégories fonctionnelles prises en charge par un appareil](retrieving-the-functional-categories-supported-by-a-device.md) , les périphériques mobiles Windows peuvent prendre en charge une ou plusieurs catégories fonctionnelles.</span><span class="sxs-lookup"><span data-stu-id="dbba9-104">As noted in the [Retrieving the Functional Categories Supported by a Device](retrieving-the-functional-categories-supported-by-a-device.md) topic, Windows Portable Devices may support one or more functional categories.</span></span> <span data-ttu-id="dbba9-105">Toute catégorie fonctionnelle donnée peut prendre en charge un ou plusieurs types de contenu.</span><span class="sxs-lookup"><span data-stu-id="dbba9-105">Any given functional category may support one or more content types.</span></span> <span data-ttu-id="dbba9-106">Par exemple, la catégorie stockage peut prendre en charge les types de contenu de dossier, audio et image.</span><span class="sxs-lookup"><span data-stu-id="dbba9-106">For example, the storage category may support content types of folder, audio, and image.</span></span>

<span data-ttu-id="dbba9-107">Pour obtenir une description des types de contenu pris en charge par WPD, consultez la rubrique [**\_ type de contenu wpd \_ \_ tout**](wpd-content-type-all.md) .</span><span class="sxs-lookup"><span data-stu-id="dbba9-107">For a description of the content types supported by WPD, see the [**WPD\_CONTENT\_TYPE\_ALL**](wpd-content-type-all.md) topic.</span></span>

<span data-ttu-id="dbba9-108">La fonction ListSupportedContentTypes dans le module DeviceCapabilities. cpp illustre la récupération des types de contenu pour les catégories fonctionnelles prises en charge par un périphérique sélectionné.</span><span class="sxs-lookup"><span data-stu-id="dbba9-108">The ListSupportedContentTypes function in the DeviceCapabilities.cpp module demonstrates the retrieval of content types for the functional categories supported by a selected device.</span></span>

<span data-ttu-id="dbba9-109">Votre application peut récupérer les catégories fonctionnelles prises en charge par un appareil à l’aide des interfaces décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="dbba9-109">Your application can retrieve the functional categories supported by a device using the interfaces described in the following table.</span></span>



| <span data-ttu-id="dbba9-110">Interface</span><span class="sxs-lookup"><span data-stu-id="dbba9-110">Interface</span></span>                                                                                      | <span data-ttu-id="dbba9-111">Description</span><span class="sxs-lookup"><span data-stu-id="dbba9-111">Description</span></span>                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [<span data-ttu-id="dbba9-112">**Interface IPortableDeviceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="dbba9-112">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | <span data-ttu-id="dbba9-113">Fournit l’accès aux méthodes de récupération de catégorie fonctionnelle.</span><span class="sxs-lookup"><span data-stu-id="dbba9-113">Provides access to the functional-category retrieval methods.</span></span> |
| [<span data-ttu-id="dbba9-114">**Interface IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="dbba9-114">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="dbba9-115">Permet d’énumérer et de stocker les données de catégorie fonctionnelle.</span><span class="sxs-lookup"><span data-stu-id="dbba9-115">Used to enumerate and store functional-category data.</span></span>         |



 

<span data-ttu-id="dbba9-116">Le code trouvé dans la fonction ListSupportedContentTypes est presque identique au code trouvé dans la fonction ListFunctionalCategories.</span><span class="sxs-lookup"><span data-stu-id="dbba9-116">The code found in the ListSupportedContentTypes function is almost identical to the code found in the ListFunctionalCategories function.</span></span> <span data-ttu-id="dbba9-117">(Voir la rubrique [récupération des catégories fonctionnelles prises en charge par un appareil](retrieving-the-functional-categories-supported-by-a-device.md) .) La seule différence est l’appel à la méthode [**IPortableDeviceCapabilities :: GetSupportedContentTypes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getsupportedcontenttypes) , qui apparaît dans la boucle qui itère au sein des catégories fonctionnelles.</span><span class="sxs-lookup"><span data-stu-id="dbba9-117">(See the [Retrieving Functional Categories Supported by a Device](retrieving-the-functional-categories-supported-by-a-device.md) topic.) The one difference is the call to the [**IPortableDeviceCapabilities::GetSupportedContentTypes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getsupportedcontenttypes) method, which appears within the loop that iterates through the functional categories.</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceCapabilities>            pCapabilities;
CComPtr<IPortableDevicePropVariantCollection>   pCategories;
DWORD dwNumCategories   = 0;

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
// We will use these categories to enumerate functional objects
// that fall within them.
if (SUCCEEDED(hr))
{
    hr = pCapabilities->GetFunctionalCategories(&pCategories);
    if (FAILED(hr))
    {
        printf("! Failed to get functional categories from the device, hr = 0x%lx\n",hr);
    }
}

// Get the number of functional categories found on the device.
if (SUCCEEDED(hr))
{
    hr = pCategories->GetCount(&dwNumCategories);
    if (FAILED(hr))
    {
        printf("! Failed to get number of functional categories, hr = 0x%lx\n",hr);
    }
}

printf("\n%d Functional Categories Found on the device\n\n", dwNumCategories);

// Loop through each functional category and display its name and supported content types.
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

            if ((pv.puuid != NULL)      &&
                (pv.vt    == VT_CLSID))
            {
                // Display the functional category name
                printf("Functional Category: ");
                DisplayFunctionalCategory(*pv.puuid);
                printf("\n");

                // Display the content types supported for this category
                CComPtr<IPortableDevicePropVariantCollection> pContentTypes;
                hr = pCapabilities->GetSupportedContentTypes(*pv.puuid, &pContentTypes);
                if (SUCCEEDED(hr))
                {
                    printf("Supported Content Types: ");
                    DisplayContentTypes(pContentTypes);
                    printf("\n\n");
                }
                else
                {
                    printf("! Failed to get supported content types from the device, hr = 0x%lx\n",hr);
                }
            }
            else
            {
                printf("! Invalid functional category found\n");
            }
        }

        PropVariantClear(&pv);
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="dbba9-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="dbba9-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dbba9-119">**Interface IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="dbba9-119">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="dbba9-120">**Interface IPortableDeviceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="dbba9-120">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)
</dt> <dt>

[<span data-ttu-id="dbba9-121">**Interface IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="dbba9-121">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="dbba9-122">**Guide de programmation**</span><span class="sxs-lookup"><span data-stu-id="dbba9-122">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



