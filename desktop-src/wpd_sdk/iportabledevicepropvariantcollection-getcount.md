---
description: La méthode GetCount récupère le nombre d’éléments de cette collection.
ms.assetid: b7c8acd2-67f2-47d3-b42a-26aa701fd613
title: 'IPortableDevicePropVariantCollection :: GetCount, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.GetCount
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: d3a06cb5d89bc09a35a58f9269ba19c488c11e0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542270"
---
# <a name="iportabledevicepropvariantcollectiongetcount-method"></a><span data-ttu-id="610bc-103">IPortableDevicePropVariantCollection :: GetCount, méthode</span><span class="sxs-lookup"><span data-stu-id="610bc-103">IPortableDevicePropVariantCollection::GetCount method</span></span>

<span data-ttu-id="610bc-104">La méthode **GetCount** récupère le nombre d’éléments de cette collection.</span><span class="sxs-lookup"><span data-stu-id="610bc-104">The **GetCount** method retrieves the number of items in this collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="610bc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="610bc-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [in] DWORD *pcElems
);
```



## <a name="parameters"></a><span data-ttu-id="610bc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="610bc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="610bc-107">*pcElems* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="610bc-107">*pcElems* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="610bc-108">Pointeur vers une **valeur DWORD** qui contient le nombre d’éléments dans la collection.</span><span class="sxs-lookup"><span data-stu-id="610bc-108">Pointer to a **DWORD** that contains the number of items in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="610bc-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="610bc-109">Return value</span></span>

<span data-ttu-id="610bc-110">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="610bc-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="610bc-111">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="610bc-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="610bc-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="610bc-112">Return code</span></span>                                                                               | <span data-ttu-id="610bc-113">Description</span><span class="sxs-lookup"><span data-stu-id="610bc-113">Description</span></span>                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="610bc-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="610bc-114"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="610bc-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="610bc-115">The method succeeded.</span></span><br/>                     |
| <dl> <span data-ttu-id="610bc-116"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="610bc-116"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="610bc-117">Un argument de pointeur obligatoire était **null**.</span><span class="sxs-lookup"><span data-stu-id="610bc-117">A required pointer argument was **NULL**.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="610bc-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="610bc-118">Examples</span></span>

<span data-ttu-id="610bc-119">Pour obtenir un exemple d’utilisation de cette méthode [, consultez récupération des catégories fonctionnelles prises en charge par un appareil](retrieving-the-functional-categories-supported-by-a-device.md).</span><span class="sxs-lookup"><span data-stu-id="610bc-119">For an example of how to use this method see [Retrieving the Functional Categories Supported by a Device](retrieving-the-functional-categories-supported-by-a-device.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="610bc-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="610bc-120">Requirements</span></span>



| <span data-ttu-id="610bc-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="610bc-121">Requirement</span></span> | <span data-ttu-id="610bc-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="610bc-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="610bc-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="610bc-123">Header</span></span><br/>  | <dl> <span data-ttu-id="610bc-124"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="610bc-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="610bc-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="610bc-125">Library</span></span><br/> | <dl> <span data-ttu-id="610bc-126"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="610bc-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="610bc-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="610bc-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="610bc-128">**Interface IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="610bc-128">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="610bc-129">Récupération des événements de service pris en charge</span><span class="sxs-lookup"><span data-stu-id="610bc-129">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="610bc-130">Récupération des formats de service pris en charge</span><span class="sxs-lookup"><span data-stu-id="610bc-130">Retrieving Supported Service Formats</span></span>](retrieving-supported-formats.md)
</dt> <dt>

[<span data-ttu-id="610bc-131">Récupération des méthodes de service prises en charge</span><span class="sxs-lookup"><span data-stu-id="610bc-131">Retrieving Supported Service Methods</span></span>](retrieving-supported-methods.md)
</dt> <dt>

[<span data-ttu-id="610bc-132">Récupération des catégories fonctionnelles prises en charge par un appareil</span><span class="sxs-lookup"><span data-stu-id="610bc-132">Retrieving the Functional Categories Supported by a Device</span></span>](retrieving-the-functional-categories-supported-by-a-device.md)
</dt> <dt>

[<span data-ttu-id="610bc-133">Définition des propriétés de plusieurs objets</span><span class="sxs-lookup"><span data-stu-id="610bc-133">Setting Properties for Multiple Objects</span></span>](setting-properties-for-multiple-objects.md)
</dt> </dl>

 

 




