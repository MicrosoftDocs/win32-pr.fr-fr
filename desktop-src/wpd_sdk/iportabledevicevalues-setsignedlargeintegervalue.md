---
description: La méthode SetSignedLargeIntegerValue ajoute une nouvelle valeur LONGLONG (type VT \_ I8) ou remplace une valeur existante.
ms.assetid: 604b48ed-3e3f-4a06-91dd-7ece9f146824
title: 'IPortableDeviceValues :: SetSignedLargeIntegerValue, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetSignedLargeIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: f8c207a88e17c9a1ddf45d77e9da8b62a8396e23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106538764"
---
# <a name="iportabledevicevaluessetsignedlargeintegervalue-method"></a><span data-ttu-id="6966b-103">IPortableDeviceValues :: SetSignedLargeIntegerValue, méthode</span><span class="sxs-lookup"><span data-stu-id="6966b-103">IPortableDeviceValues::SetSignedLargeIntegerValue method</span></span>

<span data-ttu-id="6966b-104">La méthode **SetSignedLargeIntegerValue** ajoute une nouvelle valeur **LongLong** (type VT \_ I8) ou remplace une valeur existante.</span><span class="sxs-lookup"><span data-stu-id="6966b-104">The **SetSignedLargeIntegerValue** method adds a new **LONGLONG** value (type VT\_I8) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="6966b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6966b-105">Syntax</span></span>


```C++
HRESULT SetSignedLargeIntegerValue(
  [in]       REFPROPERTYKEY key,
  [in] const LONGLONG       Value
);
```



## <a name="parameters"></a><span data-ttu-id="6966b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6966b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6966b-107">*clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6966b-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6966b-108">**REFPROPERTYKEY** qui spécifie l’élément à créer ou à remplacer.</span><span class="sxs-lookup"><span data-stu-id="6966b-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="6966b-109">*Valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6966b-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6966b-110">**LongLong** qui spécifie la nouvelle valeur.</span><span class="sxs-lookup"><span data-stu-id="6966b-110">A **LONGLONG** that specifies the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6966b-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6966b-111">Return value</span></span>

<span data-ttu-id="6966b-112">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="6966b-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="6966b-113">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="6966b-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="6966b-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="6966b-114">Return code</span></span>                                                                          | <span data-ttu-id="6966b-115">Description</span><span class="sxs-lookup"><span data-stu-id="6966b-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="6966b-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6966b-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="6966b-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="6966b-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6966b-118">Notes</span><span class="sxs-lookup"><span data-stu-id="6966b-118">Remarks</span></span>

<span data-ttu-id="6966b-119">Si une valeur existante a la même clé que celle spécifiée par le paramètre de *clé* , elle remplace la valeur existante sans avertissement.</span><span class="sxs-lookup"><span data-stu-id="6966b-119">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span>

## <a name="requirements"></a><span data-ttu-id="6966b-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6966b-120">Requirements</span></span>



| <span data-ttu-id="6966b-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6966b-121">Requirement</span></span> | <span data-ttu-id="6966b-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="6966b-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6966b-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="6966b-123">Header</span></span><br/>  | <dl> <span data-ttu-id="6966b-124"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="6966b-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="6966b-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6966b-125">Library</span></span><br/> | <dl> <span data-ttu-id="6966b-126"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6966b-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6966b-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6966b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6966b-128">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="6966b-128">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="6966b-129">**IPortableDeviceValues::GetSignedLargeIntegerValue**</span><span class="sxs-lookup"><span data-stu-id="6966b-129">**IPortableDeviceValues::GetSignedLargeIntegerValue**</span></span>](iportabledevicevalues-getsignedlargeintegervalue.md)
</dt> </dl>

 

 




