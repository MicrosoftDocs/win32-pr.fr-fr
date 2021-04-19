---
description: Récupération des propriétés d’un objet unique
ms.assetid: e4e3b286-6330-4147-a367-57accf5beae6
title: Récupération des propriétés d’un objet unique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5851b31256659c2ca036bac504a53fa51a20ee14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521867"
---
# <a name="retrieving-properties-for-a-single-object"></a><span data-ttu-id="ce40c-103">Récupération des propriétés d’un objet unique</span><span class="sxs-lookup"><span data-stu-id="ce40c-103">Retrieving Properties for a Single Object</span></span>

<span data-ttu-id="ce40c-104">Une fois que votre application a récupéré un identificateur d’objet (voir la rubrique [énumération du contenu](enumerating-content.md) ) pour un objet donné, elle peut récupérer des informations descriptives sur cet objet en appelant des méthodes dans l' [**interface IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) et l' [**interface IPortableDeviceKeyCollection**](iportabledevicekeycollection.md).</span><span class="sxs-lookup"><span data-stu-id="ce40c-104">After your application retrieves an object identifier (see the [Enumerating Content](enumerating-content.md) topic) for a given object, it can retrieve descriptive information about that object by calling methods in the [**IPortableDeviceProperties interface**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) and the [**IPortableDeviceKeyCollection interface**](iportabledevicekeycollection.md).</span></span>

<span data-ttu-id="ce40c-105">La méthode [**IPortableDeviceProperties :: GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) récupère une liste des propriétés spécifiées pour un objet donné.</span><span class="sxs-lookup"><span data-stu-id="ce40c-105">The [**IPortableDeviceProperties::GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) method retrieves a list of specified properties for a given object.</span></span> <span data-ttu-id="ce40c-106">(Votre application peut également appeler la méthode GetValues et spécifier une valeur **null** pour le paramètre pKeys pour récupérer toutes les propriétés d’un objet donné ; toutefois, les performances de cette méthode peuvent être beaucoup plus lentes lors de la récupération de toutes les propriétés.)</span><span class="sxs-lookup"><span data-stu-id="ce40c-106">(Your application could also call the GetValues method and specify a **NULL** value for the pKeys parameter to retrieve all properties for a given object; however, the performance of this method may be significantly slower when retrieving all properties.)</span></span>

<span data-ttu-id="ce40c-107">Toutefois, avant que votre application appelle GetValue, il doit identifier les propriétés à récupérer en définissant les clés correspondantes dans un [**objet IPortableDeviceKeyCollection**](iportabledevicekeycollection.md).</span><span class="sxs-lookup"><span data-stu-id="ce40c-107">Before your application calls GetValues, however, it needs to identify the properties to retrieve by setting corresponding keys in an [**IPortableDeviceKeyCollection object**](iportabledevicekeycollection.md).</span></span> <span data-ttu-id="ce40c-108">Votre application identifie les propriétés qui vous intéressent en appelant la méthode [**IPortableDeviceKeyCollection :: Add**](iportabledevicekeycollection-add.md) et en fournissant une valeur PROPERTYKEY qui identifie chaque propriété qu’elle va récupérer.</span><span class="sxs-lookup"><span data-stu-id="ce40c-108">Your application will identify the properties of interest by calling the [**IPortableDeviceKeyCollection::Add**](iportabledevicekeycollection-add.md) method and supplying a PROPERTYKEY value that identifies each property that it will retrieve.</span></span>

<span data-ttu-id="ce40c-109">La fonction ReadContentProperties dans le module ContentProperties. cpp de l’exemple d’application montre comment les cinq propriétés ont été récupérées pour un objet sélectionné.</span><span class="sxs-lookup"><span data-stu-id="ce40c-109">The ReadContentProperties function in the ContentProperties.cpp module of the sample application demonstrates how the five properties were retrieved for a selected object.</span></span> <span data-ttu-id="ce40c-110">Le tableau suivant décrit chacune de ces propriétés et leur valeur REFPROPERTYKEY correspondante.</span><span class="sxs-lookup"><span data-stu-id="ce40c-110">The following table describes each of these properties and their corresponding REFPROPERTYKEY value.</span></span>



| <span data-ttu-id="ce40c-111">Propriété</span><span class="sxs-lookup"><span data-stu-id="ce40c-111">Property</span></span>                     | <span data-ttu-id="ce40c-112">Description</span><span class="sxs-lookup"><span data-stu-id="ce40c-112">Description</span></span>                                                                                                                                      | <span data-ttu-id="ce40c-113">PROPERTYKEY</span><span class="sxs-lookup"><span data-stu-id="ce40c-113">PROPERTYKEY</span></span>                         |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <span data-ttu-id="ce40c-114">Identificateur de l’objet parent</span><span class="sxs-lookup"><span data-stu-id="ce40c-114">Parent-object identifier</span></span>     | <span data-ttu-id="ce40c-115">Chaîne qui spécifie l’identificateur pour le parent de l’objet donné.</span><span class="sxs-lookup"><span data-stu-id="ce40c-115">A string that specifies the identifier for the given object's parent.</span></span>                                                                            | <span data-ttu-id="ce40c-116">\_ \_ ID parent de l’objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="ce40c-116">WPD\_OBJECT\_PARENT\_ID</span></span>             |
| <span data-ttu-id="ce40c-117">Nom d’objet</span><span class="sxs-lookup"><span data-stu-id="ce40c-117">Object name</span></span>                  | <span data-ttu-id="ce40c-118">Chaîne qui spécifie le nom de l’objet donné.</span><span class="sxs-lookup"><span data-stu-id="ce40c-118">A string that specifies the name of the given object.</span></span>                                                                                            | <span data-ttu-id="ce40c-119">nom de l' \_ objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="ce40c-119">WPD\_OBJECT\_NAME</span></span>                   |
| <span data-ttu-id="ce40c-120">Identificateur unique persistant</span><span class="sxs-lookup"><span data-stu-id="ce40c-120">Persistent unique identifier</span></span> | <span data-ttu-id="ce40c-121">Chaîne qui spécifie un identificateur unique pour l’objet donné.</span><span class="sxs-lookup"><span data-stu-id="ce40c-121">A string that specifies a unique identifier for the given object.</span></span> <span data-ttu-id="ce40c-122">(Cet identificateur est persistant entre les sessions, contrairement à l’identificateur d’objet.)</span><span class="sxs-lookup"><span data-stu-id="ce40c-122">(This identifier is persistent across sessions, unlike the object identifier.)</span></span> | <span data-ttu-id="ce40c-123">\_ \_ \_ ID unique persistant de l’objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="ce40c-123">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span> |
| <span data-ttu-id="ce40c-124">Format de l’objet</span><span class="sxs-lookup"><span data-stu-id="ce40c-124">Object format</span></span>                | <span data-ttu-id="ce40c-125">Identificateur global unique (GUID) qui spécifie le format du fichier correspondant à un objet donné.</span><span class="sxs-lookup"><span data-stu-id="ce40c-125">A globally unique identifier (GUID) that specifies the format of the file corresponding to a given object.</span></span>                                       | <span data-ttu-id="ce40c-126">\_format d’objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="ce40c-126">WPD\_OBJECT\_FORMAT</span></span>                 |
| <span data-ttu-id="ce40c-127">Type de contenu d’objet</span><span class="sxs-lookup"><span data-stu-id="ce40c-127">Object content type</span></span>          | <span data-ttu-id="ce40c-128">GUID qui spécifie le type de contenu associé à un objet donné.</span><span class="sxs-lookup"><span data-stu-id="ce40c-128">A GUID that specifies the type of content associated with a given object.</span></span>                                                                        | <span data-ttu-id="ce40c-129">TYPE de contenu de l' \_ objet wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="ce40c-129">WPD\_OBJECT\_CONTENT\_TYPE</span></span>          |



 

<span data-ttu-id="ce40c-130">L’extrait suivant de la fonction ReadContentProperties montre comment l’exemple d’application a utilisé l' [**interface IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) et la méthode [**IPortableDeviceKeyCollection :: Add**](iportabledevicekeycollection-add.md) pour identifier les propriétés qu’elle récupérerait.</span><span class="sxs-lookup"><span data-stu-id="ce40c-130">The following excerpt from the ReadContentProperties function demonstrates how the sample application used the [**IPortableDeviceKeyCollection interface**](iportabledevicekeycollection.md) and the [**IPortableDeviceKeyCollection::Add**](iportabledevicekeycollection-add.md) method to identify the properties it would retrieve.</span></span>


```C++
hr = CoCreateInstance(CLSID_PortableDeviceKeyCollection,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(&pPropertiesToRead));
if (SUCCEEDED(hr))
{
    // 4) Populate the IPortableDeviceKeyCollection with the keys we wish to read.
    // NOTE: We are not handling any special error cases here so we can proceed with
    // adding as many of the target properties as we can.
    if (pPropertiesToRead != NULL)
    {
        HRESULT hrTemp = S_OK;
        hrTemp = pPropertiesToRead->Add(WPD_OBJECT_PARENT_ID);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_OBJECT_PARENT_ID to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }

        hrTemp = pPropertiesToRead->Add(WPD_OBJECT_NAME);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_OBJECT_NAME to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }

        hrTemp = pPropertiesToRead->Add(WPD_OBJECT_PERSISTENT_UNIQUE_ID);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_OBJECT_PERSISTENT_UNIQUE_ID to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }

        hrTemp = pPropertiesToRead->Add(WPD_OBJECT_FORMAT);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_OBJECT_FORMAT to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }

        hrTemp = pPropertiesToRead->Add(WPD_OBJECT_CONTENT_TYPE);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_OBJECT_CONTENT_TYPE to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }
    }
}
```



<span data-ttu-id="ce40c-131">Une fois que l’exemple d’application a défini les clés appropriées, il a appelé la méthode [**IPortableDeviceProperties :: GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) pour récupérer les valeurs spécifiées pour l’objet donné.</span><span class="sxs-lookup"><span data-stu-id="ce40c-131">Once the sample application set the appropriate keys, it called the [**IPortableDeviceProperties::GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) method to retrieve the specified values for the given object.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = pProperties->GetValues(szSelection,         // The object whose properties we are reading
                                pPropertiesToRead,   // The properties we want to read
                                &pObjectProperties); // Driver supplied property values for the specified object
    if (FAILED(hr))
    {
        printf("! Failed to get all properties for object '%ws', hr= 0x%lx\n", szSelection, hr);
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="ce40c-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ce40c-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce40c-133">**Interface IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="ce40c-133">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="ce40c-134">**Interface IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="ce40c-134">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="ce40c-135">**Interface IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="ce40c-135">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[<span data-ttu-id="ce40c-136">**Guide de programmation**</span><span class="sxs-lookup"><span data-stu-id="ce40c-136">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



