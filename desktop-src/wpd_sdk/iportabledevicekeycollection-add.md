---
description: La méthode Add ajoute une clé de propriété à la collection.
ms.assetid: 640ef1c4-2843-48dd-a30a-9a2ef9de35b9
title: 'IPortableDeviceKeyCollection :: Add, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceKeyCollection.Add
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: e43fea25a08969b2ae8169884d51ddc46f8c7136
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533436"
---
# <a name="iportabledevicekeycollectionadd-method"></a><span data-ttu-id="531c3-103">IPortableDeviceKeyCollection :: Add, méthode</span><span class="sxs-lookup"><span data-stu-id="531c3-103">IPortableDeviceKeyCollection::Add method</span></span>

<span data-ttu-id="531c3-104">La méthode **Add** ajoute une clé de propriété à la collection.</span><span class="sxs-lookup"><span data-stu-id="531c3-104">The **Add** method adds a property key to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="531c3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="531c3-105">Syntax</span></span>


```C++
HRESULT Add(
  [in] REFPROPERTYKEY Key
);
```



## <a name="parameters"></a><span data-ttu-id="531c3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="531c3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="531c3-107">*Clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="531c3-107">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="531c3-108">**REFPROPERTYKEY** à ajouter à la collection.</span><span class="sxs-lookup"><span data-stu-id="531c3-108">A **REFPROPERTYKEY** to add to the collection.</span></span> <span data-ttu-id="531c3-109">Cette méthode copie la clé dans la collection, ce qui vous permet de libérer la variable locale après avoir appelé cette méthode.</span><span class="sxs-lookup"><span data-stu-id="531c3-109">This method copies the key to the collection, so you can release the local variable after calling this method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="531c3-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="531c3-110">Return value</span></span>

<span data-ttu-id="531c3-111">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="531c3-111">The method returns an **HRESULT**.</span></span> <span data-ttu-id="531c3-112">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="531c3-112">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="531c3-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="531c3-113">Return code</span></span>                                                                                   | <span data-ttu-id="531c3-114">Description</span><span class="sxs-lookup"><span data-stu-id="531c3-114">Description</span></span>                                                                       |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="531c3-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="531c3-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="531c3-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="531c3-116">The method succeeded.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="531c3-117"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="531c3-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="531c3-118">La mémoire disponible est insuffisante pour ajouter la clé à la collection.</span><span class="sxs-lookup"><span data-stu-id="531c3-118">There is not enough memory available to add the key to the collection.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="531c3-119">Exemples</span><span class="sxs-lookup"><span data-stu-id="531c3-119">Examples</span></span>

<span data-ttu-id="531c3-120">Pour obtenir un exemple d’utilisation de cette méthode, consultez [récupération des propriétés pour un seul objet](retrieving-properties-for-a-single-object.md).</span><span class="sxs-lookup"><span data-stu-id="531c3-120">For an example of how to use this method, see [Retrieving Properties for a Single Object](retrieving-properties-for-a-single-object.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="531c3-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="531c3-121">Requirements</span></span>



| <span data-ttu-id="531c3-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="531c3-122">Requirement</span></span> | <span data-ttu-id="531c3-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="531c3-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="531c3-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="531c3-124">Header</span></span><br/>  | <dl> <span data-ttu-id="531c3-125"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="531c3-125"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="531c3-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="531c3-126">Library</span></span><br/> | <dl> <span data-ttu-id="531c3-127"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="531c3-127"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="531c3-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="531c3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="531c3-129">**Interface IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="531c3-129">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="531c3-130">Récupération des propriétés Content-Object</span><span class="sxs-lookup"><span data-stu-id="531c3-130">Retrieving Content-Object Properties</span></span>](retrieving-content-object-properties.md)
</dt> <dt>

[<span data-ttu-id="531c3-131">Récupération des propriétés d’un objet unique</span><span class="sxs-lookup"><span data-stu-id="531c3-131">Retrieving Properties for a Single Object</span></span>](retrieving-properties-for-a-single-object.md)
</dt> <dt>

[<span data-ttu-id="531c3-132">Récupération des fonctionnalités de rendu prises en charge par un appareil</span><span class="sxs-lookup"><span data-stu-id="531c3-132">Retrieving the Rendering Capabilities Supported by a Device</span></span>](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> </dl>

 

 




