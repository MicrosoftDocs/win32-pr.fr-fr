---
description: Énumération du contenu
ms.assetid: 86782a09-4fca-4ae0-beaf-296069e061dc
title: Énumération du contenu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b2e724b451d714516c4723edcd56936b71e4e50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536967"
---
# <a name="enumerating-content"></a><span data-ttu-id="ebc87-103">Énumération du contenu</span><span class="sxs-lookup"><span data-stu-id="ebc87-103">Enumerating Content</span></span>

<span data-ttu-id="ebc87-104">Le contenu d’un appareil (qu’il s’agisse d’un dossier, d’un annuaire, d’une vidéo ou d’une image fixe) est appelé un objet dans l’API WPD.</span><span class="sxs-lookup"><span data-stu-id="ebc87-104">The content on a device (whether that content is a folder, a phone book, a video, or a still image) is called an object in the WPD API.</span></span> <span data-ttu-id="ebc87-105">Ces objets sont référencés par des identificateurs d’objet et décrits par des propriétés.</span><span class="sxs-lookup"><span data-stu-id="ebc87-105">These objects are referenced by object identifiers and described by properties.</span></span> <span data-ttu-id="ebc87-106">Vous pouvez énumérer les objets sur un appareil en appelant des méthodes dans l' [**interface IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice), l' [**interface IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)et l' [**interface IEnumPortableDeviceObjectIDs**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids).</span><span class="sxs-lookup"><span data-stu-id="ebc87-106">You can enumerate the objects on a device by calling methods in the [**IPortableDevice interface**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice), the [**IPortableDeviceContent interface**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent), and the [**IEnumPortableDeviceObjectIDs interface**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids).</span></span>

<span data-ttu-id="ebc87-107">L’exemple d’application montre l’énumération du contenu dans la fonction EnumerateAllContent, qui se trouve dans le module ContentEnumeration. cpp.</span><span class="sxs-lookup"><span data-stu-id="ebc87-107">The sample application demonstrates content enumeration in the EnumerateAllContent function that is found in the ContentEnumeration.cpp module.</span></span> <span data-ttu-id="ebc87-108">Cette fonction appelle à son tour une fonction RecursiveEnumerate qui parcourt la hiérarchie des objets trouvés sur l’appareil sélectionné et retourne un identificateur d’objet pour chaque objet.</span><span class="sxs-lookup"><span data-stu-id="ebc87-108">This function, in turn, calls a RecursiveEnumerate function that walks the hierarchy of objects found on the selected device and returns an object identifier for each object.</span></span>

<span data-ttu-id="ebc87-109">Comme indiqué, la fonction RecursiveEnumerate récupère un identificateur d’objet pour chaque objet trouvé sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ebc87-109">As noted, the RecursiveEnumerate function retrieves an object identifier for each object found on the device.</span></span> <span data-ttu-id="ebc87-110">L’identificateur d’objet est une valeur de chaîne.</span><span class="sxs-lookup"><span data-stu-id="ebc87-110">The object identifier is a string value.</span></span> <span data-ttu-id="ebc87-111">Une fois que votre application a récupéré cet identificateur, elle peut obtenir des informations plus descriptives sur l’objet (par exemple, le nom de l’objet, l’identificateur pour le parent de l’objet, etc.).</span><span class="sxs-lookup"><span data-stu-id="ebc87-111">Once your application retrieves this identifier, it can obtain more descriptive object information (such as the object's name, the identifier for the object's parent, and so on).</span></span> <span data-ttu-id="ebc87-112">Ces informations descriptives sont appelées propriétés d’objet (ou métadonnées).</span><span class="sxs-lookup"><span data-stu-id="ebc87-112">This descriptive information is referred to as object properties (or metadata).</span></span> <span data-ttu-id="ebc87-113">Votre application peut récupérer ces propriétés en appelant les membres de l' [**interface IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties).</span><span class="sxs-lookup"><span data-stu-id="ebc87-113">Your application can retrieve these properties by calling members of the [**IPortableDeviceProperties interface**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties).</span></span>

<span data-ttu-id="ebc87-114">La fonction EnumerateAllContent commence par récupérer un pointeur vers une [**interface IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent).</span><span class="sxs-lookup"><span data-stu-id="ebc87-114">The EnumerateAllContent function begins by retrieving a pointer to an [**IPortableDeviceContent interface**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent).</span></span> <span data-ttu-id="ebc87-115">Il récupère ce pointeur en appelant la méthode [**IPortableDevice :: content**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-content) .</span><span class="sxs-lookup"><span data-stu-id="ebc87-115">It retrieves this pointer by calling the [**IPortableDevice::Content**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-content) method.</span></span>


```C++
void EnumerateAllContent(
    IPortableDevice* pDevice)
{
    HRESULT                         hr = S_OK;
    CComPtr<IPortableDeviceContent> pContent;

    if (pDevice == NULL)
    {
        printf("! A NULL IPortableDevice interface pointer was received\n");
        return;
    }

    // Get an IPortableDeviceContent interface from the IPortableDevice interface to
    // access the content-specific methods.
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }

    // Enumerate content starting from the "DEVICE" object.
    if (SUCCEEDED(hr))
    {
        printf("\n");
        RecursiveEnumerate(WPD_DEVICE_OBJECT_ID, pContent);
    }
}
```



<span data-ttu-id="ebc87-116">Une fois qu’il a récupéré le pointeur vers l’interface IPortableDeviceContent, la fonction EnumerateAllContent appelle la fonction RecursiveEnumerate, qui parcourt la hiérarchie des objets trouvés sur le périphérique donné et retourne un identificateur d’objet pour chacun d’eux.</span><span class="sxs-lookup"><span data-stu-id="ebc87-116">Once it retrieves the pointer to the IPortableDeviceContent interface, the EnumerateAllContent function calls the RecursiveEnumerate function, which walks the hierarchy of objects found on the given device and returns an object identifier for each.</span></span>

<span data-ttu-id="ebc87-117">La fonction RecursiveEnumerate commence par récupérer un pointeur vers une [**interface IEnumPortableDeviceObjectIDs**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids).</span><span class="sxs-lookup"><span data-stu-id="ebc87-117">The RecursiveEnumerate function begins by retrieving a pointer to an [**IEnumPortableDeviceObjectIDs interface**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids).</span></span> <span data-ttu-id="ebc87-118">Cette interface expose les méthodes utilisées par une application pour naviguer dans la liste des objets trouvés sur un appareil donné.</span><span class="sxs-lookup"><span data-stu-id="ebc87-118">This interface exposes the methods that an application uses to navigate the list of objects found on a given device.</span></span>

<span data-ttu-id="ebc87-119">Dans cet exemple, la fonction RecursiveEnumerate appelle la méthode [**IEnumPortableDeviceObjectIDs :: Next**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-ienumportabledeviceobjectids-next) pour parcourir la liste d’objets.</span><span class="sxs-lookup"><span data-stu-id="ebc87-119">In this sample, the RecursiveEnumerate function calls the [**IEnumPortableDeviceObjectIDs::Next**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-ienumportabledeviceobjectids-next) method to traverse the list of objects.</span></span>

<span data-ttu-id="ebc87-120">Chaque appel à la méthode [**IEnumPortableDeviceObjects :: Next**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-ienumportabledeviceobjectids-next) demande un lot de 10 identificateurs.</span><span class="sxs-lookup"><span data-stu-id="ebc87-120">Each call to the [**IEnumPortableDeviceObjects::Next**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-ienumportabledeviceobjectids-next) method requests a batch of 10 identifiers.</span></span> <span data-ttu-id="ebc87-121">(Cette valeur est spécifiée par le nombre \_ OBJETS \_ pour \_ demander une constante fournie comme premier argument.)</span><span class="sxs-lookup"><span data-stu-id="ebc87-121">(This value is specified by the NUM\_OBJECTS\_TO\_REQUEST constant that is supplied as the first argument.)</span></span>


```C++
#define NUM_OBJECTS_TO_REQUEST  10

// Recursively called function which enumerates using the specified
// object identifier as the parent.
void RecursiveEnumerate(
    PCWSTR                  pszObjectID,
    IPortableDeviceContent* pContent)
{
    CComPtr<IEnumPortableDeviceObjectIDs> pEnumObjectIDs;

    // Print the object identifier being used as the parent during enumeration.
    printf("%ws\n",pszObjectID);

    // Get an IEnumPortableDeviceObjectIDs interface by calling EnumObjects with the
    // specified parent object identifier.
    HRESULT hr = pContent->EnumObjects(0,               // Flags are unused
                                       pszObjectID,     // Starting from the passed in object
                                       NULL,            // Filter is unused
                                       &pEnumObjectIDs);
    if (FAILED(hr))
    {
        printf("! Failed to get IEnumPortableDeviceObjectIDs from IPortableDeviceContent, hr = 0x%lx\n",hr);
    }

    // Loop calling Next() while S_OK is being returned.
    while(hr == S_OK)
    {
        DWORD  cFetched = 0;
        PWSTR  szObjectIDArray[NUM_OBJECTS_TO_REQUEST] = {0};
        hr = pEnumObjectIDs->Next(NUM_OBJECTS_TO_REQUEST,   // Number of objects to request on each NEXT call
                                  szObjectIDArray,          // Array of PWSTR array which will be populated on each NEXT call
                                  &cFetched);               // Number of objects written to the PWSTR array
        if (SUCCEEDED(hr))
        {
            // Traverse the results of the Next() operation and recursively enumerate
            // Remember to free all returned object identifiers using CoTaskMemFree()
            for (DWORD dwIndex = 0; dwIndex < cFetched; dwIndex++)
            {
                RecursiveEnumerate(szObjectIDArray[dwIndex],pContent);

                // Free allocated PWSTRs after the recursive enumeration call has completed.
                CoTaskMemFree(szObjectIDArray[dwIndex]);
                szObjectIDArray[dwIndex] = NULL;
            }
        }
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="ebc87-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ebc87-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ebc87-123">**Interface IEnumPortableDeviceObjectIDs**</span><span class="sxs-lookup"><span data-stu-id="ebc87-123">**IEnumPortableDeviceObjectIDs Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids)
</dt> <dt>

[<span data-ttu-id="ebc87-124">**Interface IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="ebc87-124">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="ebc87-125">**Interface IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="ebc87-125">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="ebc87-126">**Interface IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="ebc87-126">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[<span data-ttu-id="ebc87-127">**Guide de programmation**</span><span class="sxs-lookup"><span data-stu-id="ebc87-127">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



