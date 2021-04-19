---
description: La méthode Add ajoute un élément à la collection.
ms.assetid: 3b06abc4-f0ab-4b02-b3a7-360615f86a2a
title: 'IPortableDeviceValuesCollection :: Add, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection.Add
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 1f423ac7243c8d16fa75978ae5c9bcf04136bb05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544065"
---
# <a name="iportabledevicevaluescollectionadd-method"></a><span data-ttu-id="1b52e-103">IPortableDeviceValuesCollection :: Add, méthode</span><span class="sxs-lookup"><span data-stu-id="1b52e-103">IPortableDeviceValuesCollection::Add method</span></span>

<span data-ttu-id="1b52e-104">La méthode **Add** ajoute un élément à la collection.</span><span class="sxs-lookup"><span data-stu-id="1b52e-104">The **Add** method adds an item to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b52e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1b52e-105">Syntax</span></span>


```C++
HRESULT Add(
  [in] IPortableDeviceValues *pValues
);
```



## <a name="parameters"></a><span data-ttu-id="1b52e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1b52e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b52e-107">*pValues* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1b52e-107">*pValues* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b52e-108">Pointeur vers une interface **IPortableDeviceValues** à ajouter à la collection.</span><span class="sxs-lookup"><span data-stu-id="1b52e-108">Pointer to an **IPortableDeviceValues** interface to add to the collection.</span></span> <span data-ttu-id="1b52e-109">L’interface n’est pas réellement copiée, mais **AddRef** est appelé dessus.</span><span class="sxs-lookup"><span data-stu-id="1b52e-109">The interface is not actually copied, but **AddRef** is called on it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b52e-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1b52e-110">Return value</span></span>

<span data-ttu-id="1b52e-111">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="1b52e-111">The method returns an **HRESULT**.</span></span> <span data-ttu-id="1b52e-112">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="1b52e-112">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="1b52e-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="1b52e-113">Return code</span></span>                                                                                   | <span data-ttu-id="1b52e-114">Description</span><span class="sxs-lookup"><span data-stu-id="1b52e-114">Description</span></span>                                                                         |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1b52e-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1b52e-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="1b52e-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="1b52e-116">The method succeeded.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="1b52e-117"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="1b52e-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="1b52e-118">La mémoire disponible est insuffisante pour ajouter la valeur à la collection.</span><span class="sxs-lookup"><span data-stu-id="1b52e-118">There is not enough memory available to add the value to the collection.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1b52e-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1b52e-119">Requirements</span></span>



| <span data-ttu-id="1b52e-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1b52e-120">Requirement</span></span> | <span data-ttu-id="1b52e-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="1b52e-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b52e-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="1b52e-122">Header</span></span><br/>  | <dl> <span data-ttu-id="1b52e-123"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b52e-123"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="1b52e-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1b52e-124">Library</span></span><br/> | <dl> <span data-ttu-id="1b52e-125"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1b52e-125"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b52e-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1b52e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b52e-127">**Interface IPortableDeviceValuesCollection**</span><span class="sxs-lookup"><span data-stu-id="1b52e-127">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




