---
description: Récupération des propriétés de plusieurs objets par format d’objet
ms.assetid: c3f5edfd-8a6a-4bbd-9787-a4268c38f18f
title: Récupération des propriétés de plusieurs objets par format d’objet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a352704b3ce5d063c544a41c467f372554bc901
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485457"
---
# <a name="retrieving-properties-for-multiple-objects-by-object-format"></a><span data-ttu-id="2fe82-103">Récupération des propriétés de plusieurs objets par format d’objet</span><span class="sxs-lookup"><span data-stu-id="2fe82-103">Retrieving Properties for Multiple Objects by Object Format</span></span>

<span data-ttu-id="2fe82-104">En plus d’une récupération en bloc des propriétés d’une collection d’identificateurs d’objet, une application peut également effectuer une récupération en bloc de propriétés pour tous les objets d’un type particulier.</span><span class="sxs-lookup"><span data-stu-id="2fe82-104">In addition to a bulk retrieval of properties for a collection of object identifiers, an application can also perform a bulk retrieval of properties for all objects of a particular type.</span></span> <span data-ttu-id="2fe82-105">Comme dans l’exemple précédent, la récupération en bloc pour un type donné requiert que le pilote de périphérique prenne en charge les récupérations en bloc.</span><span class="sxs-lookup"><span data-stu-id="2fe82-105">As in the previous example, bulk retrieval for a given type requires that the device driver support bulk retrievals.</span></span>

<span data-ttu-id="2fe82-106">Votre application peut effectuer une récupération en bloc à l’aide des interfaces décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="2fe82-106">Your application can perform a bulk retrieval using the interfaces described in the following table.</span></span>



| <span data-ttu-id="2fe82-107">Interface</span><span class="sxs-lookup"><span data-stu-id="2fe82-107">Interface</span></span>                                                                                      | <span data-ttu-id="2fe82-108">Description</span><span class="sxs-lookup"><span data-stu-id="2fe82-108">Description</span></span>                                                        |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="2fe82-109">**Interface IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="2fe82-109">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | <span data-ttu-id="2fe82-110">Fournit l’accès aux méthodes spécifiques au contenu.</span><span class="sxs-lookup"><span data-stu-id="2fe82-110">Provides access to the content-specific methods.</span></span>                   |
| [<span data-ttu-id="2fe82-111">**Interface IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="2fe82-111">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)                 | <span data-ttu-id="2fe82-112">Utilisé pour identifier les propriétés à récupérer.</span><span class="sxs-lookup"><span data-stu-id="2fe82-112">Used to identify the properties to be retrieved.</span></span>                   |
| [<span data-ttu-id="2fe82-113">**Interface IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="2fe82-113">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)                       | <span data-ttu-id="2fe82-114">Utilisé pour déterminer si un pilote donné prend en charge les opérations en bloc.</span><span class="sxs-lookup"><span data-stu-id="2fe82-114">Used to determine whether a given driver supports bulk operations.</span></span> |
| [<span data-ttu-id="2fe82-115">**Interface IPortableDevicePropertiesBulk**</span><span class="sxs-lookup"><span data-stu-id="2fe82-115">**IPortableDevicePropertiesBulk Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)               | <span data-ttu-id="2fe82-116">Prend en charge l’opération de récupération en bloc.</span><span class="sxs-lookup"><span data-stu-id="2fe82-116">Supports the bulk retrieval operation.</span></span>                             |
| [<span data-ttu-id="2fe82-117">**Interface IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="2fe82-117">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="2fe82-118">Utilisé pour stocker les identificateurs d’objet pour l’opération en bloc.</span><span class="sxs-lookup"><span data-stu-id="2fe82-118">Used to store the object identifiers for the bulk operation.</span></span>       |



 

<span data-ttu-id="2fe82-119">La fonction ReadContentPropertiesBulkFilteringFormat dans le module ContentProperties. cpp de l’exemple d’application illustre une opération de récupération en bloc pour les objets d’un type ou d’un format particulier.</span><span class="sxs-lookup"><span data-stu-id="2fe82-119">The ReadContentPropertiesBulkFilteringFormat function in the sample application's ContentProperties.cpp module demonstrates a bulk retrieval operation for objects of a particular type or format.</span></span>

<span data-ttu-id="2fe82-120">Le code trouvé dans la fonction ReadContentPropertiesBulkFilteringFormat est presque identique au code trouvé dans la fonction ReadContentPropertiesBulk.</span><span class="sxs-lookup"><span data-stu-id="2fe82-120">The code found in the ReadContentPropertiesBulkFilteringFormat function is almost identical to the code found in the ReadContentPropertiesBulk function.</span></span> <span data-ttu-id="2fe82-121">(Pour obtenir une description complète de cette fonction, consultez la rubrique [extraction des propriétés de plusieurs objets](retrieving-properties-for-multiple-objects.md) .)</span><span class="sxs-lookup"><span data-stu-id="2fe82-121">(See the [Retrieving Properties for Multiple Objects](retrieving-properties-for-multiple-objects.md) topic for a complete description of this function.)</span></span>

<span data-ttu-id="2fe82-122">La principale différence se produit lorsque l’opération est mise en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="2fe82-122">The one primary difference occurs when the operation is queued.</span></span> <span data-ttu-id="2fe82-123">Lors du filtrage par type ou format, la méthode [**IPortableDevicePropertiesBulk :: QueueGetValuesByObjectFormat**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuegetvaluesbyobjectformat) est appelée à la place de la méthode [**IPortableDevicePropertiesBulk :: QueueGetValuesByObjectList**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuegetvaluesbyobjectlist) .</span><span class="sxs-lookup"><span data-stu-id="2fe82-123">When filtering by type or format, the [**IPortableDevicePropertiesBulk::QueueGetValuesByObjectFormat**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuegetvaluesbyobjectformat) method is called instead of the [**IPortableDevicePropertiesBulk::QueueGetValuesByObjectList**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuegetvaluesbyobjectlist) method.</span></span>


```C++
hr = pPropertiesBulk->QueueGetValuesByObjectFormat(WPD_OBJECT_FORMAT_WMA,
                                                   WPD_DEVICE_OBJECT_ID,
                                                   100,
                                                   pPropertiesToRead,
                                                   pCallback,
                                                   &guidContext);
```



## <a name="related-topics"></a><span data-ttu-id="2fe82-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2fe82-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2fe82-125">**Interface IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="2fe82-125">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="2fe82-126">**Interface IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="2fe82-126">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="2fe82-127">**Interface IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="2fe82-127">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="2fe82-128">**Interface IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="2fe82-128">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[<span data-ttu-id="2fe82-129">**Interface IPortableDevicePropertiesBulk**</span><span class="sxs-lookup"><span data-stu-id="2fe82-129">**IPortableDevicePropertiesBulk Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)
</dt> <dt>

[<span data-ttu-id="2fe82-130">**Interface IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="2fe82-130">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="2fe82-131">**Guide de programmation**</span><span class="sxs-lookup"><span data-stu-id="2fe82-131">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



