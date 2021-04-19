---
description: La méthode SetBoolValue, ajoute une nouvelle valeur booléenne (type VT \_ bool) ou remplace celle qui existe déjà.
ms.assetid: add30665-78f7-4037-801e-af51a4ab2f60
title: 'IPortableDeviceValues :: SetBoolValue,, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetBoolValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7adf311e863c08873aa8300f9e940d4a5b49417f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539589"
---
# <a name="iportabledevicevaluessetboolvalue-method"></a><span data-ttu-id="757bb-103">IPortableDeviceValues :: SetBoolValue,, méthode</span><span class="sxs-lookup"><span data-stu-id="757bb-103">IPortableDeviceValues::SetBoolValue method</span></span>

<span data-ttu-id="757bb-104">La méthode **SetBoolValue,** ajoute une nouvelle valeur **BOOLÉENNE** (type VT \_ bool) ou remplace celle qui existe déjà.</span><span class="sxs-lookup"><span data-stu-id="757bb-104">The **SetBoolValue** method adds a new **Boolean** value (type VT\_BOOL) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="757bb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="757bb-105">Syntax</span></span>


```C++
HRESULT SetBoolValue(
  [in]       REFPROPERTYKEY key,
  [in] const BOOL           Value
);
```



## <a name="parameters"></a><span data-ttu-id="757bb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="757bb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="757bb-107">*clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="757bb-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="757bb-108">**REFPROPERTYKEY** qui spécifie l’élément à créer ou à remplacer.</span><span class="sxs-lookup"><span data-stu-id="757bb-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="757bb-109">*Valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="757bb-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="757bb-110">Valeur **booléenne** qui spécifie la nouvelle valeur.</span><span class="sxs-lookup"><span data-stu-id="757bb-110">A **BOOL** that specifies the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="757bb-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="757bb-111">Return value</span></span>

<span data-ttu-id="757bb-112">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="757bb-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="757bb-113">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="757bb-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="757bb-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="757bb-114">Return code</span></span>                                                                          | <span data-ttu-id="757bb-115">Description</span><span class="sxs-lookup"><span data-stu-id="757bb-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="757bb-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="757bb-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="757bb-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="757bb-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="757bb-118">Notes</span><span class="sxs-lookup"><span data-stu-id="757bb-118">Remarks</span></span>

<span data-ttu-id="757bb-119">Si une valeur existante a la même clé que celle spécifiée par le paramètre de *clé* , elle remplace la valeur existante sans avertissement.</span><span class="sxs-lookup"><span data-stu-id="757bb-119">If an existing value has the same key specified by the *key* parameter, it overwrites the existing value without any warning.</span></span> <span data-ttu-id="757bb-120">La mémoire clé existante est libérée de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="757bb-120">The existing key memory is released appropriately.</span></span>

## <a name="requirements"></a><span data-ttu-id="757bb-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="757bb-121">Requirements</span></span>



| <span data-ttu-id="757bb-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="757bb-122">Requirement</span></span> | <span data-ttu-id="757bb-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="757bb-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="757bb-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="757bb-124">Header</span></span><br/>  | <dl> <span data-ttu-id="757bb-125"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="757bb-125"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="757bb-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="757bb-126">Library</span></span><br/> | <dl> <span data-ttu-id="757bb-127"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="757bb-127"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="757bb-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="757bb-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="757bb-129">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="757bb-129">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="757bb-130">**IPortableDeviceValues::GetBoolValue**</span><span class="sxs-lookup"><span data-stu-id="757bb-130">**IPortableDeviceValues::GetBoolValue**</span></span>](iportabledevicevalues-getboolvalue.md)
</dt> </dl>

 

 




