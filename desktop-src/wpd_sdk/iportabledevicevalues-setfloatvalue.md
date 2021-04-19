---
description: La méthode SetFloatValue ajoute une nouvelle valeur FLOTTante (type VT \_ R4) ou remplace celle qui existe déjà.
ms.assetid: 1e0c9d19-47bf-4d93-a0c0-27e2c4897012
title: 'IPortableDeviceValues :: SetFloatValue, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetFloatValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 60b42217c925c83e96f2c893c7bc7f11449ebdd6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106522793"
---
# <a name="iportabledevicevaluessetfloatvalue-method"></a><span data-ttu-id="f38e1-103">IPortableDeviceValues :: SetFloatValue, méthode</span><span class="sxs-lookup"><span data-stu-id="f38e1-103">IPortableDeviceValues::SetFloatValue method</span></span>

<span data-ttu-id="f38e1-104">La méthode **SetFloatValue** ajoute une nouvelle valeur **flottante** (type VT \_ R4) ou remplace celle qui existe déjà.</span><span class="sxs-lookup"><span data-stu-id="f38e1-104">The **SetFloatValue** method adds a new **FLOAT** value (type VT\_R4) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="f38e1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f38e1-105">Syntax</span></span>


```C++
HRESULT SetFloatValue(
  [in]       REFPROPERTYKEY key,
  [in] const FLOAT          Value
);
```



## <a name="parameters"></a><span data-ttu-id="f38e1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f38e1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f38e1-107">*clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f38e1-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f38e1-108">**REFPROPERTYKEY** qui spécifie l’élément à créer ou à remplacer.</span><span class="sxs-lookup"><span data-stu-id="f38e1-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="f38e1-109">*Valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f38e1-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f38e1-110">Valeur **float** qui contient la nouvelle valeur.</span><span class="sxs-lookup"><span data-stu-id="f38e1-110">A **FLOAT** that contains the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f38e1-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f38e1-111">Return value</span></span>

<span data-ttu-id="f38e1-112">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f38e1-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f38e1-113">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f38e1-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f38e1-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="f38e1-114">Return code</span></span>                                                                          | <span data-ttu-id="f38e1-115">Description</span><span class="sxs-lookup"><span data-stu-id="f38e1-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="f38e1-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f38e1-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="f38e1-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="f38e1-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f38e1-118">Notes</span><span class="sxs-lookup"><span data-stu-id="f38e1-118">Remarks</span></span>

<span data-ttu-id="f38e1-119">Si une valeur existante a la même clé que celle spécifiée par le paramètre de *clé* , elle remplace la valeur existante sans avertissement.</span><span class="sxs-lookup"><span data-stu-id="f38e1-119">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span>

## <a name="requirements"></a><span data-ttu-id="f38e1-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f38e1-120">Requirements</span></span>



| <span data-ttu-id="f38e1-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f38e1-121">Requirement</span></span> | <span data-ttu-id="f38e1-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="f38e1-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f38e1-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="f38e1-123">Header</span></span><br/>  | <dl> <span data-ttu-id="f38e1-124"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="f38e1-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="f38e1-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f38e1-125">Library</span></span><br/> | <dl> <span data-ttu-id="f38e1-126"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f38e1-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f38e1-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f38e1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f38e1-128">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="f38e1-128">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="f38e1-129">**IPortableDeviceValues::GetFloatValue**</span><span class="sxs-lookup"><span data-stu-id="f38e1-129">**IPortableDeviceValues::GetFloatValue**</span></span>](iportabledevicevalues-getfloatvalue.md)
</dt> </dl>

 

 




