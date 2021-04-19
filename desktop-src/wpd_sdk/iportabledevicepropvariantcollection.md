---
description: L’interface IPortableDevicePropVariantCollection contient une collection de valeurs PROPVARIANT indexées du même VARTYPE.
ms.assetid: 41224958-a5a0-4e09-8733-d0ae036f68b9
title: Interface IPortableDevicePropVariantCollection (PortableDeviceTypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 14ba07894c74567487704bb1f63e7242542af313
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528068"
---
# <a name="iportabledevicepropvariantcollection-interface"></a><span data-ttu-id="4b2f4-103">Interface IPortableDevicePropVariantCollection</span><span class="sxs-lookup"><span data-stu-id="4b2f4-103">IPortableDevicePropVariantCollection interface</span></span>

<span data-ttu-id="4b2f4-104">L’interface **IPortableDevicePropVariantCollection** contient une collection de valeurs **PROPVARIANT** indexées du même VarType.</span><span class="sxs-lookup"><span data-stu-id="4b2f4-104">The **IPortableDevicePropVariantCollection** interface holds a collection of indexed **PROPVARIANT** values of the same VARTYPE.</span></span> <span data-ttu-id="4b2f4-105">Le VARTYPE du premier élément ajouté à la collection détermine le VARTYPE de la collection.</span><span class="sxs-lookup"><span data-stu-id="4b2f4-105">The VARTYPE of the first item that is added to the collection determines the VARTYPE of the collection.</span></span> <span data-ttu-id="4b2f4-106">Une tentative d’ajout d’un élément d’un autre VARTYPE peut échouer si la valeur **PROPVARIANT** ne peut pas être modifiée en VarType actuel de la collection.</span><span class="sxs-lookup"><span data-stu-id="4b2f4-106">An attempt to add an item of a different VARTYPE may fail if the **PROPVARIANT** value cannot be changed to the collection's current VARTYPE.</span></span> <span data-ttu-id="4b2f4-107">Pour modifier le VARTYPE de la collection, appelez **ChangeType**.</span><span class="sxs-lookup"><span data-stu-id="4b2f4-107">To change the VARTYPE of the collection, call **ChangeType**.</span></span>

<span data-ttu-id="4b2f4-108">Cette interface peut être récupérée à partir d’une méthode ou, si un nouvel objet est requis, appeler **CoCreate** avec **CLSID \_ PortableDevicePropVariantCollection**.</span><span class="sxs-lookup"><span data-stu-id="4b2f4-108">This interface can be retrieved from a method or, if a new object is required, call **CoCreate** with **CLSID\_PortableDevicePropVariantCollection**.</span></span>

## <a name="members"></a><span data-ttu-id="4b2f4-109">Membres</span><span class="sxs-lookup"><span data-stu-id="4b2f4-109">Members</span></span>

<span data-ttu-id="4b2f4-110">L’interface **IPortableDevicePropVariantCollection** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="4b2f4-110">The **IPortableDevicePropVariantCollection** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="4b2f4-111">**IPortableDevicePropVariantCollection** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="4b2f4-111">**IPortableDevicePropVariantCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="4b2f4-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4b2f4-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4b2f4-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4b2f4-113">Methods</span></span>

<span data-ttu-id="4b2f4-114">L’interface **IPortableDevicePropVariantCollection** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="4b2f4-114">The **IPortableDevicePropVariantCollection** interface has these methods.</span></span>



| <span data-ttu-id="4b2f4-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="4b2f4-115">Method</span></span>                                                                | <span data-ttu-id="4b2f4-116">Description</span><span class="sxs-lookup"><span data-stu-id="4b2f4-116">Description</span></span>                                                                         |
|:----------------------------------------------------------------------|:------------------------------------------------------------------------------------|
| [<span data-ttu-id="4b2f4-117">**Complémentaires**</span><span class="sxs-lookup"><span data-stu-id="4b2f4-117">**Add**</span></span>](iportabledevicepropvariantcollection-add.md)               | <span data-ttu-id="4b2f4-118">Ajoute un élément à la collection.</span><span class="sxs-lookup"><span data-stu-id="4b2f4-118">Adds an item to the collection.</span></span><br/>                                          |
| [<span data-ttu-id="4b2f4-119">**ChangeType**</span><span class="sxs-lookup"><span data-stu-id="4b2f4-119">**ChangeType**</span></span>](iportabledevicepropvariantcollection-changetype.md) | <span data-ttu-id="4b2f4-120">Convertit tous les éléments de la collection au VARTYPE spécifié.</span><span class="sxs-lookup"><span data-stu-id="4b2f4-120">Converts all items in the collection to the specified VARTYPE.</span></span><br/>           |
| [<span data-ttu-id="4b2f4-121">**Effacé**</span><span class="sxs-lookup"><span data-stu-id="4b2f4-121">**Clear**</span></span>](iportabledevicepropvariantcollection-clear.md)           | <span data-ttu-id="4b2f4-122">Libère, puis supprime tous les éléments de la collection.</span><span class="sxs-lookup"><span data-stu-id="4b2f4-122">Frees, and then removes, all items from the collection.</span></span><br/>                  |
| [<span data-ttu-id="4b2f4-123">**GetAt**</span><span class="sxs-lookup"><span data-stu-id="4b2f4-123">**GetAt**</span></span>](iportabledevicepropvariantcollection-getat.md)           | <span data-ttu-id="4b2f4-124">Récupère un élément de la collection par un index de base zéro.</span><span class="sxs-lookup"><span data-stu-id="4b2f4-124">Retrieves an item from the collection by a zero-based index.</span></span><br/>             |
| [<span data-ttu-id="4b2f4-125">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="4b2f4-125">**GetCount**</span></span>](iportabledevicepropvariantcollection-getcount.md)     | <span data-ttu-id="4b2f4-126">Récupère le nombre d’éléments de cette collection.</span><span class="sxs-lookup"><span data-stu-id="4b2f4-126">Retrieves the number of items in this collection.</span></span><br/>                        |
| [<span data-ttu-id="4b2f4-127">**GetType**</span><span class="sxs-lookup"><span data-stu-id="4b2f4-127">**GetType**</span></span>](iportabledevicepropvariantcollection-gettype.md)       | <span data-ttu-id="4b2f4-128">Récupère le type de données des éléments de la collection.</span><span class="sxs-lookup"><span data-stu-id="4b2f4-128">Retrieves the data type of the items in the collection.</span></span><br/>                  |
| [<span data-ttu-id="4b2f4-129">**RemoveAt**</span><span class="sxs-lookup"><span data-stu-id="4b2f4-129">**RemoveAt**</span></span>](iportabledevicepropvariantcollection-removeat.md)     | <span data-ttu-id="4b2f4-130">Supprime l’élément stocké à l’emplacement spécifié par l’index donné.</span><span class="sxs-lookup"><span data-stu-id="4b2f4-130">Removes the element stored at the location specified by the given index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4b2f4-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4b2f4-131">Requirements</span></span>



| <span data-ttu-id="4b2f4-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4b2f4-132">Requirement</span></span> | <span data-ttu-id="4b2f4-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="4b2f4-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b2f4-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="4b2f4-134">Header</span></span><br/>  | <dl> <span data-ttu-id="4b2f4-135"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b2f4-135"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="4b2f4-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4b2f4-136">Library</span></span><br/> | <dl> <span data-ttu-id="4b2f4-137"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4b2f4-137"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b2f4-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4b2f4-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b2f4-139">**Interfaces de collection**</span><span class="sxs-lookup"><span data-stu-id="4b2f4-139">**Collection Interfaces**</span></span>](collection-interfaces.md)
</dt> </dl>

 

