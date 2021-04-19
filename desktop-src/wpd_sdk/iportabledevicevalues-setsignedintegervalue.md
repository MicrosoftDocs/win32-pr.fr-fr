---
description: La méthode SetSignedIntegerValue ajoute une nouvelle valeur LONG (type VT \_ I4) ou remplace celle qui existe déjà.
ms.assetid: b0bb2992-2906-446c-be9a-20bff13f8e1d
title: 'IPortableDeviceValues :: SetSignedIntegerValue, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetSignedIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 26a5d01ec69203c39008de394e3693acc833d262
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523972"
---
# <a name="iportabledevicevaluessetsignedintegervalue-method"></a><span data-ttu-id="69757-103">IPortableDeviceValues :: SetSignedIntegerValue, méthode</span><span class="sxs-lookup"><span data-stu-id="69757-103">IPortableDeviceValues::SetSignedIntegerValue method</span></span>

<span data-ttu-id="69757-104">La méthode **SetSignedIntegerValue** ajoute une nouvelle valeur **long** (type VT \_ I4) ou remplace celle qui existe déjà.</span><span class="sxs-lookup"><span data-stu-id="69757-104">The **SetSignedIntegerValue** method adds a new **LONG** value (type VT\_I4) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="69757-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="69757-105">Syntax</span></span>


```C++
HRESULT SetSignedIntegerValue(
  [in]       REFPROPERTYKEY key,
  [in] const LONG           Value
);
```



## <a name="parameters"></a><span data-ttu-id="69757-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="69757-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69757-107">*clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="69757-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69757-108">**REFPROPERTYKEY** qui spécifie l’élément à créer ou à remplacer.</span><span class="sxs-lookup"><span data-stu-id="69757-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="69757-109">*Valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="69757-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69757-110">Valeur de **type long** qui spécifie la nouvelle valeur.</span><span class="sxs-lookup"><span data-stu-id="69757-110">A **LONG** that specifies the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69757-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="69757-111">Return value</span></span>

<span data-ttu-id="69757-112">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="69757-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="69757-113">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="69757-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="69757-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="69757-114">Return code</span></span>                                                                          | <span data-ttu-id="69757-115">Description</span><span class="sxs-lookup"><span data-stu-id="69757-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="69757-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="69757-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="69757-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="69757-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="69757-118">Notes</span><span class="sxs-lookup"><span data-stu-id="69757-118">Remarks</span></span>

<span data-ttu-id="69757-119">Si une valeur existante a la même clé que celle spécifiée par le paramètre de *clé* , elle remplace la valeur existante sans avertissement.</span><span class="sxs-lookup"><span data-stu-id="69757-119">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span>

## <a name="requirements"></a><span data-ttu-id="69757-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="69757-120">Requirements</span></span>



| <span data-ttu-id="69757-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="69757-121">Requirement</span></span> | <span data-ttu-id="69757-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="69757-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69757-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="69757-123">Header</span></span><br/>  | <dl> <span data-ttu-id="69757-124"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="69757-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="69757-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="69757-125">Library</span></span><br/> | <dl> <span data-ttu-id="69757-126"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="69757-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69757-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="69757-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69757-128">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="69757-128">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="69757-129">**IPortableDeviceValues::GetSignedIntegerValue**</span><span class="sxs-lookup"><span data-stu-id="69757-129">**IPortableDeviceValues::GetSignedIntegerValue**</span></span>](iportabledevicevalues-getsignedintegervalue.md)
</dt> </dl>

 

 




