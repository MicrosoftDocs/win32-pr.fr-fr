---
description: 'IPortableDevicePropVariantCollection :: GetAt, méthode-la méthode GetAt récupère un élément de la collection à l’aide d’un index de base zéro.'
ms.assetid: c7119ba6-e6fc-4cb6-a8ab-3bf7b6bfe850
title: 'IPortableDevicePropVariantCollection :: GetAt, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.GetAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: b901e8fcfa065813e4c0942632f80901800ef0a9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106797"
---
# <a name="iportabledevicepropvariantcollectiongetat-method"></a><span data-ttu-id="11a9d-103">IPortableDevicePropVariantCollection :: GetAt, méthode</span><span class="sxs-lookup"><span data-stu-id="11a9d-103">IPortableDevicePropVariantCollection::GetAt method</span></span>

<span data-ttu-id="11a9d-104">La méthode **GetAt** récupère un élément de la collection à l’aide d’un index de base zéro.</span><span class="sxs-lookup"><span data-stu-id="11a9d-104">The **GetAt** method retrieves an item from the collection by a zero-based index.</span></span>

## <a name="syntax"></a><span data-ttu-id="11a9d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="11a9d-105">Syntax</span></span>


```C++
HRESULT GetAt(
  [in]  const DWORD       dwIndex,
  [out]       PROPVARIANT *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="11a9d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="11a9d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11a9d-107">*dwIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="11a9d-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11a9d-108">**Valeur DWORD** qui contient l’index de base zéro de l’élément à récupérer.</span><span class="sxs-lookup"><span data-stu-id="11a9d-108">**DWORD** that contains the zero-based index of the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="11a9d-109">*pValue* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="11a9d-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="11a9d-110">Pointeur vers une structure **PROPVARIANT** .</span><span class="sxs-lookup"><span data-stu-id="11a9d-110">Pointer to a **PROPVARIANT** structure.</span></span> <span data-ttu-id="11a9d-111">L’appelant est chargé de libérer cette mémoire en appelant **PropVariantClear**.</span><span class="sxs-lookup"><span data-stu-id="11a9d-111">The caller is responsible for freeing this memory by calling **PropVariantClear**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11a9d-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="11a9d-112">Return value</span></span>

<span data-ttu-id="11a9d-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="11a9d-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="11a9d-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="11a9d-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="11a9d-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="11a9d-115">Return code</span></span>                                                                                  | <span data-ttu-id="11a9d-116">Description</span><span class="sxs-lookup"><span data-stu-id="11a9d-116">Description</span></span>                                               |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="11a9d-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="11a9d-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="11a9d-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="11a9d-118">The method succeeded.</span></span><br/>                          |
| <dl> <span data-ttu-id="11a9d-119"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="11a9d-119"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="11a9d-120">Un argument de pointeur obligatoire était **null**.</span><span class="sxs-lookup"><span data-stu-id="11a9d-120">A required pointer argument was **NULL**.</span></span><br/>      |
| <dl> <span data-ttu-id="11a9d-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="11a9d-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="11a9d-122">L’index qui a été passé était hors limites.</span><span class="sxs-lookup"><span data-stu-id="11a9d-122">The index that was passed in was out of range.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="11a9d-123">Exemples</span><span class="sxs-lookup"><span data-stu-id="11a9d-123">Examples</span></span>

<span data-ttu-id="11a9d-124">Pour obtenir un exemple d’utilisation de cette méthode [, consultez récupération des catégories fonctionnelles prises en charge par un appareil](retrieving-the-functional-categories-supported-by-a-device.md).</span><span class="sxs-lookup"><span data-stu-id="11a9d-124">For an example of how to use this method see [Retrieving the Functional Categories Supported by a Device](retrieving-the-functional-categories-supported-by-a-device.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="11a9d-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="11a9d-125">Requirements</span></span>



| <span data-ttu-id="11a9d-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="11a9d-126">Requirement</span></span> | <span data-ttu-id="11a9d-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="11a9d-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11a9d-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="11a9d-128">Header</span></span><br/>  | <dl> <span data-ttu-id="11a9d-129"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="11a9d-129"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="11a9d-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="11a9d-130">Library</span></span><br/> | <dl> <span data-ttu-id="11a9d-131"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="11a9d-131"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11a9d-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="11a9d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11a9d-133">**Interface IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="11a9d-133">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="11a9d-134">Récupération d’un identificateur d’objet à partir d’un identificateur unique persistant</span><span class="sxs-lookup"><span data-stu-id="11a9d-134">Retrieving an Object Identifier from a Persistent Unique Identifier</span></span>](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)
</dt> <dt>

[<span data-ttu-id="11a9d-135">Récupération des événements de service pris en charge</span><span class="sxs-lookup"><span data-stu-id="11a9d-135">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="11a9d-136">Récupération des formats de service pris en charge</span><span class="sxs-lookup"><span data-stu-id="11a9d-136">Retrieving Supported Service Formats</span></span>](retrieving-supported-formats.md)
</dt> <dt>

[<span data-ttu-id="11a9d-137">Récupération des méthodes de service prises en charge</span><span class="sxs-lookup"><span data-stu-id="11a9d-137">Retrieving Supported Service Methods</span></span>](retrieving-supported-methods.md)
</dt> <dt>

[<span data-ttu-id="11a9d-138">Récupération des types de contenu pris en charge par un appareil</span><span class="sxs-lookup"><span data-stu-id="11a9d-138">Retrieving the Content Types Supported by a Device</span></span>](retrieving-the-content-types-supported-by-a-device.md)
</dt> <dt>

[<span data-ttu-id="11a9d-139">Récupération des catégories fonctionnelles prises en charge par un appareil</span><span class="sxs-lookup"><span data-stu-id="11a9d-139">Retrieving the Functional Categories Supported by a Device</span></span>](retrieving-the-functional-categories-supported-by-a-device.md)
</dt> <dt>

[<span data-ttu-id="11a9d-140">Récupération des identificateurs d’objets fonctionnels pour un appareil</span><span class="sxs-lookup"><span data-stu-id="11a9d-140">Retrieving the Functional Object Identifiers for a Device</span></span>](retrieving-the-functional-object-identifiers-for-a-device.md)
</dt> <dt>

[<span data-ttu-id="11a9d-141">Récupération des fonctionnalités de rendu prises en charge par un appareil</span><span class="sxs-lookup"><span data-stu-id="11a9d-141">Retrieving the Rendering Capabilities Supported by a Device</span></span>](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> <dt>

[<span data-ttu-id="11a9d-142">Définition des propriétés de plusieurs objets</span><span class="sxs-lookup"><span data-stu-id="11a9d-142">Setting Properties for Multiple Objects</span></span>](setting-properties-for-multiple-objects.md)
</dt> </dl>

 

 




