---
description: La méthode GetAt récupère un élément de la collection à l’aide d’un index de base zéro.
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
ms.openlocfilehash: 0833c69b537fa230320ef69707a6f4302a8ca1ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526005"
---
# <a name="iportabledevicepropvariantcollectiongetat-method"></a><span data-ttu-id="575c3-103">IPortableDevicePropVariantCollection :: GetAt, méthode</span><span class="sxs-lookup"><span data-stu-id="575c3-103">IPortableDevicePropVariantCollection::GetAt method</span></span>

<span data-ttu-id="575c3-104">La méthode **GetAt** récupère un élément de la collection à l’aide d’un index de base zéro.</span><span class="sxs-lookup"><span data-stu-id="575c3-104">The **GetAt** method retrieves an item from the collection by a zero-based index.</span></span>

## <a name="syntax"></a><span data-ttu-id="575c3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="575c3-105">Syntax</span></span>


```C++
HRESULT GetAt(
  [in]  const DWORD       dwIndex,
  [out]       PROPVARIANT *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="575c3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="575c3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="575c3-107">*dwIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="575c3-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="575c3-108">**Valeur DWORD** qui contient l’index de base zéro de l’élément à récupérer.</span><span class="sxs-lookup"><span data-stu-id="575c3-108">**DWORD** that contains the zero-based index of the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="575c3-109">*pValue* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="575c3-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="575c3-110">Pointeur vers une structure **PROPVARIANT** .</span><span class="sxs-lookup"><span data-stu-id="575c3-110">Pointer to a **PROPVARIANT** structure.</span></span> <span data-ttu-id="575c3-111">L’appelant est chargé de libérer cette mémoire en appelant **PropVariantClear**.</span><span class="sxs-lookup"><span data-stu-id="575c3-111">The caller is responsible for freeing this memory by calling **PropVariantClear**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="575c3-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="575c3-112">Return value</span></span>

<span data-ttu-id="575c3-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="575c3-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="575c3-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="575c3-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="575c3-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="575c3-115">Return code</span></span>                                                                                  | <span data-ttu-id="575c3-116">Description</span><span class="sxs-lookup"><span data-stu-id="575c3-116">Description</span></span>                                               |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="575c3-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="575c3-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="575c3-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="575c3-118">The method succeeded.</span></span><br/>                          |
| <dl> <span data-ttu-id="575c3-119"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="575c3-119"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="575c3-120">Un argument de pointeur obligatoire était **null**.</span><span class="sxs-lookup"><span data-stu-id="575c3-120">A required pointer argument was **NULL**.</span></span><br/>      |
| <dl> <span data-ttu-id="575c3-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="575c3-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="575c3-122">L’index qui a été passé était hors limites.</span><span class="sxs-lookup"><span data-stu-id="575c3-122">The index that was passed in was out of range.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="575c3-123">Exemples</span><span class="sxs-lookup"><span data-stu-id="575c3-123">Examples</span></span>

<span data-ttu-id="575c3-124">Pour obtenir un exemple d’utilisation de cette méthode [, consultez récupération des catégories fonctionnelles prises en charge par un appareil](retrieving-the-functional-categories-supported-by-a-device.md).</span><span class="sxs-lookup"><span data-stu-id="575c3-124">For an example of how to use this method see [Retrieving the Functional Categories Supported by a Device](retrieving-the-functional-categories-supported-by-a-device.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="575c3-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="575c3-125">Requirements</span></span>



| <span data-ttu-id="575c3-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="575c3-126">Requirement</span></span> | <span data-ttu-id="575c3-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="575c3-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="575c3-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="575c3-128">Header</span></span><br/>  | <dl> <span data-ttu-id="575c3-129"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="575c3-129"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="575c3-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="575c3-130">Library</span></span><br/> | <dl> <span data-ttu-id="575c3-131"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="575c3-131"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="575c3-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="575c3-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="575c3-133">**Interface IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="575c3-133">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="575c3-134">Récupération d’un identificateur d’objet à partir d’un identificateur unique persistant</span><span class="sxs-lookup"><span data-stu-id="575c3-134">Retrieving an Object Identifier from a Persistent Unique Identifier</span></span>](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)
</dt> <dt>

[<span data-ttu-id="575c3-135">Récupération des événements de service pris en charge</span><span class="sxs-lookup"><span data-stu-id="575c3-135">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="575c3-136">Récupération des formats de service pris en charge</span><span class="sxs-lookup"><span data-stu-id="575c3-136">Retrieving Supported Service Formats</span></span>](retrieving-supported-formats.md)
</dt> <dt>

[<span data-ttu-id="575c3-137">Récupération des méthodes de service prises en charge</span><span class="sxs-lookup"><span data-stu-id="575c3-137">Retrieving Supported Service Methods</span></span>](retrieving-supported-methods.md)
</dt> <dt>

[<span data-ttu-id="575c3-138">Récupération des types de contenu pris en charge par un appareil</span><span class="sxs-lookup"><span data-stu-id="575c3-138">Retrieving the Content Types Supported by a Device</span></span>](retrieving-the-content-types-supported-by-a-device.md)
</dt> <dt>

[<span data-ttu-id="575c3-139">Récupération des catégories fonctionnelles prises en charge par un appareil</span><span class="sxs-lookup"><span data-stu-id="575c3-139">Retrieving the Functional Categories Supported by a Device</span></span>](retrieving-the-functional-categories-supported-by-a-device.md)
</dt> <dt>

[<span data-ttu-id="575c3-140">Récupération des identificateurs d’objets fonctionnels pour un appareil</span><span class="sxs-lookup"><span data-stu-id="575c3-140">Retrieving the Functional Object Identifiers for a Device</span></span>](retrieving-the-functional-object-identifiers-for-a-device.md)
</dt> <dt>

[<span data-ttu-id="575c3-141">Récupération des fonctionnalités de rendu prises en charge par un appareil</span><span class="sxs-lookup"><span data-stu-id="575c3-141">Retrieving the Rendering Capabilities Supported by a Device</span></span>](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> <dt>

[<span data-ttu-id="575c3-142">Définition des propriétés de plusieurs objets</span><span class="sxs-lookup"><span data-stu-id="575c3-142">Setting Properties for Multiple Objects</span></span>](setting-properties-for-multiple-objects.md)
</dt> </dl>

 

 




