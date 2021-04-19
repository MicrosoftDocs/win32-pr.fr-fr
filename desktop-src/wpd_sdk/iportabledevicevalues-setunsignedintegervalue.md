---
description: La méthode SetUnsignedIntegerValue ajoute une nouvelle valeur ULONG (type VT \_ UI4) ou remplace celle qui existe déjà.
ms.assetid: 9b5d1b8c-7863-4807-a34b-56d30a47bd5c
title: 'IPortableDeviceValues :: SetUnsignedIntegerValue, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetUnsignedIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7dc237e5cdba120a08899035dc20f6fb6b2b63f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523970"
---
# <a name="iportabledevicevaluessetunsignedintegervalue-method"></a><span data-ttu-id="0b564-103">IPortableDeviceValues :: SetUnsignedIntegerValue, méthode</span><span class="sxs-lookup"><span data-stu-id="0b564-103">IPortableDeviceValues::SetUnsignedIntegerValue method</span></span>

<span data-ttu-id="0b564-104">La méthode **SetUnsignedIntegerValue** ajoute une nouvelle valeur **ULong** (type VT \_ UI4) ou remplace celle qui existe déjà.</span><span class="sxs-lookup"><span data-stu-id="0b564-104">The **SetUnsignedIntegerValue** method adds a new **ULONG** value (type VT\_UI4) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b564-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0b564-105">Syntax</span></span>


```C++
HRESULT SetUnsignedIntegerValue(
  [in]       REFPROPERTYKEY key,
  [in] const ULONG          Value
);
```



## <a name="parameters"></a><span data-ttu-id="0b564-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0b564-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b564-107">*clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0b564-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b564-108">**REFPROPERTYKEY** qui spécifie l’élément à créer ou à remplacer.</span><span class="sxs-lookup"><span data-stu-id="0b564-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="0b564-109">*Valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0b564-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b564-110">**ULong** qui spécifie la nouvelle valeur.</span><span class="sxs-lookup"><span data-stu-id="0b564-110">A **ULONG** that specifies the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b564-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0b564-111">Return value</span></span>

<span data-ttu-id="0b564-112">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="0b564-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="0b564-113">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="0b564-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="0b564-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="0b564-114">Return code</span></span>                                                                          | <span data-ttu-id="0b564-115">Description</span><span class="sxs-lookup"><span data-stu-id="0b564-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="0b564-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0b564-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="0b564-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="0b564-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0b564-118">Notes</span><span class="sxs-lookup"><span data-stu-id="0b564-118">Remarks</span></span>

<span data-ttu-id="0b564-119">Si une valeur existante a la même clé que celle spécifiée par le paramètre de *clé* , elle remplace la valeur existante sans avertissement.</span><span class="sxs-lookup"><span data-stu-id="0b564-119">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span>

## <a name="examples"></a><span data-ttu-id="0b564-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="0b564-120">Examples</span></span>

<span data-ttu-id="0b564-121">Pour obtenir un exemple d’utilisation de cette méthode, consultez [**spécification des informations sur le client**](specifying-client-information.md).</span><span class="sxs-lookup"><span data-stu-id="0b564-121">For an example of how to use this method, see [**Specifying Client Information**](specifying-client-information.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0b564-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0b564-122">Requirements</span></span>



| <span data-ttu-id="0b564-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0b564-123">Requirement</span></span> | <span data-ttu-id="0b564-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="0b564-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b564-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="0b564-125">Header</span></span><br/>  | <dl> <span data-ttu-id="0b564-126"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b564-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="0b564-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0b564-127">Library</span></span><br/> | <dl> <span data-ttu-id="0b564-128"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0b564-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b564-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0b564-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b564-130">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="0b564-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="0b564-131">**IPortableDeviceValues::GetUnsignedIntegerValue**</span><span class="sxs-lookup"><span data-stu-id="0b564-131">**IPortableDeviceValues::GetUnsignedIntegerValue**</span></span>](iportabledevicevalues-getunsignedintegervalue.md)
</dt> <dt>

[<span data-ttu-id="0b564-132">**Spécification des informations sur le client**</span><span class="sxs-lookup"><span data-stu-id="0b564-132">**Specifying Client Information**</span></span>](specifying-client-information.md)
</dt> </dl>

 

 




