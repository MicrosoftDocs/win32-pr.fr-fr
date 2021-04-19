---
description: Récupération des identificateurs d’objets fonctionnels pour un appareil
ms.assetid: 9a13071a-95a1-4330-92d5-11fa72a8f211
title: Récupération des identificateurs d’objets fonctionnels pour un appareil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6a753324e24a6b78625a78b4128380288b6672f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106544961"
---
# <a name="retrieving-the-functional-object-identifiers-for-a-device"></a><span data-ttu-id="85407-103">Récupération des identificateurs d’objets fonctionnels pour un appareil</span><span class="sxs-lookup"><span data-stu-id="85407-103">Retrieving the Functional Object Identifiers for a Device</span></span>

<span data-ttu-id="85407-104">Comme indiqué dans la rubrique [récupération des catégories fonctionnelles prises en charge par un appareil](retrieving-the-functional-categories-supported-by-a-device.md) , les périphériques mobiles Windows peuvent prendre en charge une ou plusieurs catégories fonctionnelles.</span><span class="sxs-lookup"><span data-stu-id="85407-104">As noted in the [Retrieving the Functional Categories Supported by a Device](retrieving-the-functional-categories-supported-by-a-device.md) topic, Windows Portable Devices may support one or more functional categories.</span></span> <span data-ttu-id="85407-105">Toute catégorie fonctionnelle donnée peut prendre en charge un ou plusieurs objets fonctionnels.</span><span class="sxs-lookup"><span data-stu-id="85407-105">Any given functional category may support one or more functional objects.</span></span> <span data-ttu-id="85407-106">Par exemple, la catégorie de stockage peut prendre en charge trois objets de stockage fonctionnels, chacun étant identifié par une chaîne d’identificateur unique.</span><span class="sxs-lookup"><span data-stu-id="85407-106">For example, the storage category may support three functional storage objects, each of which is identified by a unique identifier string.</span></span> <span data-ttu-id="85407-107">Le premier objet de stockage peut ensuite être identifié par la chaîne « Storage1 », le deuxième par la chaîne « Storage2 » et le troisième par la chaîne « Storage3 ».</span><span class="sxs-lookup"><span data-stu-id="85407-107">The first storage object may then be identified by the string "Storage1", the second by the string "Storage2", and the third by the string "Storage3".</span></span>

<span data-ttu-id="85407-108">La fonction ListFunctionalObjects dans le module DeviceCapabilities. cpp illustre la récupération des types de contenu pour les catégories fonctionnelles prises en charge par un périphérique sélectionné.</span><span class="sxs-lookup"><span data-stu-id="85407-108">The ListFunctionalObjects function in the DeviceCapabilities.cpp module demonstrates the retrieval of content types for the functional categories supported by a selected device.</span></span>

<span data-ttu-id="85407-109">Votre application peut récupérer les catégories fonctionnelles prises en charge par un appareil à l’aide des interfaces décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="85407-109">Your application can retrieve the functional categories supported by a device using the interfaces described in the following table.</span></span>



| <span data-ttu-id="85407-110">Interface</span><span class="sxs-lookup"><span data-stu-id="85407-110">Interface</span></span>                                                                                      | <span data-ttu-id="85407-111">Description</span><span class="sxs-lookup"><span data-stu-id="85407-111">Description</span></span>                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [<span data-ttu-id="85407-112">**Interface IPortableDeviceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="85407-112">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | <span data-ttu-id="85407-113">Fournit l’accès aux méthodes de récupération de catégorie fonctionnelle.</span><span class="sxs-lookup"><span data-stu-id="85407-113">Provides access to the functional-category retrieval methods.</span></span> |
| [<span data-ttu-id="85407-114">**Interface IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="85407-114">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="85407-115">Permet d’énumérer et de stocker les données de catégorie fonctionnelle.</span><span class="sxs-lookup"><span data-stu-id="85407-115">Used to enumerate and store functional-category data.</span></span>         |



 

<span data-ttu-id="85407-116">Le code trouvé dans la fonction ListFunctionalObjects est presque identique au code trouvé dans la fonction ListFunctionalCategories.</span><span class="sxs-lookup"><span data-stu-id="85407-116">The code found in the ListFunctionalObjects function is almost identical to the code found in the ListFunctionalCategories function.</span></span> <span data-ttu-id="85407-117">(Voir la rubrique [récupération des catégories fonctionnelles prises en charge par un appareil](retrieving-the-functional-categories-supported-by-a-device.md) .) La seule différence est l’appel à la méthode [**IPortableDeviceCapabilities :: GetFunctionalObjects**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getfunctionalobjects) , qui apparaît dans la boucle qui itère au sein des catégories fonctionnelles.</span><span class="sxs-lookup"><span data-stu-id="85407-117">(See the [Retrieving Functional Categories Supported by a Device](retrieving-the-functional-categories-supported-by-a-device.md) topic.) The one difference is the call to the [**IPortableDeviceCapabilities::GetFunctionalObjects**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getfunctionalobjects) method, which appears within the loop that iterates through the functional categories.</span></span>


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

// Loop through each functional category and get the list of
// functional object identifiers associated with a particular
// category.
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

                // Display the object identifiers for all
                // functional objects within this category
                CComPtr<IPortableDevicePropVariantCollection> pFunctionalObjectIds;
                hr = pCapabilities->GetFunctionalObjects(*pv.puuid, &pFunctionalObjectIds);
                if (SUCCEEDED(hr))
                {
                    printf("Functional Objects: ");
                    DisplayFunctionalObjectIDs(pFunctionalObjectIds);
                    printf("\n\n");
                }
                else
                {
                    printf("! Failed to get functional objects, hr = 0x%lx\n", hr);
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



## <a name="related-topics"></a><span data-ttu-id="85407-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="85407-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85407-119">**Interface IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="85407-119">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="85407-120">**Interface IPortableDeviceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="85407-120">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)
</dt> <dt>

[<span data-ttu-id="85407-121">**Interface IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="85407-121">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="85407-122">**Guide de programmation**</span><span class="sxs-lookup"><span data-stu-id="85407-122">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



