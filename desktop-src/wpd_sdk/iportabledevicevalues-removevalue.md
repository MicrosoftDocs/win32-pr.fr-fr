---
description: La méthode RemoveValue supprime un élément de la collection.
ms.assetid: 864c23ee-5a4e-4e06-add0-f6aef5562430
title: 'IPortableDeviceValues :: RemoveValue, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.RemoveValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: f65160cc2798524d88471382c855f65dea2e6033
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523516"
---
# <a name="iportabledevicevaluesremovevalue-method"></a><span data-ttu-id="09d11-103">IPortableDeviceValues :: RemoveValue, méthode</span><span class="sxs-lookup"><span data-stu-id="09d11-103">IPortableDeviceValues::RemoveValue method</span></span>

<span data-ttu-id="09d11-104">La méthode **RemoveValue** supprime un élément de la collection.</span><span class="sxs-lookup"><span data-stu-id="09d11-104">The **RemoveValue** method removes an item from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="09d11-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="09d11-105">Syntax</span></span>


```C++
HRESULT RemoveValue(
  [in] REFPROPERTYKEY key
);
```



## <a name="parameters"></a><span data-ttu-id="09d11-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="09d11-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09d11-107">*clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="09d11-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09d11-108">**REFPROPERTYKEY** qui spécifie l’élément à supprimer.</span><span class="sxs-lookup"><span data-stu-id="09d11-108">A **REFPROPERTYKEY** that specifies the item to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09d11-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="09d11-109">Return value</span></span>

<span data-ttu-id="09d11-110">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="09d11-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="09d11-111">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="09d11-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="09d11-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="09d11-112">Return code</span></span>                                                                          | <span data-ttu-id="09d11-113">Description</span><span class="sxs-lookup"><span data-stu-id="09d11-113">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="09d11-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="09d11-114"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="09d11-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="09d11-115">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="09d11-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="09d11-116">Requirements</span></span>



| <span data-ttu-id="09d11-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="09d11-117">Requirement</span></span> | <span data-ttu-id="09d11-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="09d11-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09d11-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="09d11-119">Header</span></span><br/>  | <dl> <span data-ttu-id="09d11-120"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="09d11-120"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="09d11-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="09d11-121">Library</span></span><br/> | <dl> <span data-ttu-id="09d11-122"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="09d11-122"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09d11-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="09d11-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09d11-124">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="09d11-124">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="09d11-125">**IPortableDeviceValues :: GetValue**</span><span class="sxs-lookup"><span data-stu-id="09d11-125">**IPortableDeviceValues::GetValue**</span></span>](iportabledevicevalues-getvalue.md)
</dt> <dt>

[<span data-ttu-id="09d11-126">**IPortableDeviceValues :: SetValue**</span><span class="sxs-lookup"><span data-stu-id="09d11-126">**IPortableDeviceValues::SetValue**</span></span>](iportabledevicevalues-setvalue.md)
</dt> </dl>

 

 




