---
description: La méthode GetUnsignedLargeIntegerValue récupère une valeur ULONGLONG (type VT \_ UI8) spécifiée par une clé.
ms.assetid: de37c49b-a5f4-424d-8320-1de2d5a624aa
title: 'IPortableDeviceValues :: GetUnsignedLargeIntegerValue, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetUnsignedLargeIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 48f6093f32d43737b1999c3474f74569ecd3f8cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526000"
---
# <a name="iportabledevicevaluesgetunsignedlargeintegervalue-method"></a><span data-ttu-id="3fe3f-103">IPortableDeviceValues :: GetUnsignedLargeIntegerValue, méthode</span><span class="sxs-lookup"><span data-stu-id="3fe3f-103">IPortableDeviceValues::GetUnsignedLargeIntegerValue method</span></span>

<span data-ttu-id="3fe3f-104">La méthode **GetUnsignedLargeIntegerValue** récupère une valeur **ULONGLONG** (type VT \_ UI8) spécifiée par une clé.</span><span class="sxs-lookup"><span data-stu-id="3fe3f-104">The **GetUnsignedLargeIntegerValue** method retrieves a **ULONGLONG** value (type VT\_UI8) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fe3f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3fe3f-105">Syntax</span></span>


```C++
HRESULT GetUnsignedLargeIntegerValue(
  [in]  REFPROPERTYKEY key,
  [out] ULONGLONG      *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="3fe3f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3fe3f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fe3f-107">*clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3fe3f-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fe3f-108">Clé **REFPROPERTYKEY** qui spécifie l’élément à récupérer.</span><span class="sxs-lookup"><span data-stu-id="3fe3f-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="3fe3f-109">*pValue* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3fe3f-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3fe3f-110">Pointeur vers la valeur **ULONGLONG** récupérée.</span><span class="sxs-lookup"><span data-stu-id="3fe3f-110">Pointer to the retrieved **ULONGLONG** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3fe3f-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3fe3f-111">Return value</span></span>

<span data-ttu-id="3fe3f-112">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="3fe3f-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="3fe3f-113">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="3fe3f-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="3fe3f-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="3fe3f-114">Return code</span></span>                                                                                                            | <span data-ttu-id="3fe3f-115">Description</span><span class="sxs-lookup"><span data-stu-id="3fe3f-115">Description</span></span>                                                             |
|------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3fe3f-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3fe3f-116"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="3fe3f-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="3fe3f-117">The method succeeded.</span></span><br/>                                        |
| <dl> <span data-ttu-id="3fe3f-118"><dt>**\_TYPEMISMATCH DISP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3fe3f-118"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="3fe3f-119">La propriété spécifiée par la *clé* n’est pas un type **ULONGLONG** .</span><span class="sxs-lookup"><span data-stu-id="3fe3f-119">The property specified by *key* is not a **ULONGLONG** type.</span></span><br/> |
| <dl> <span data-ttu-id="3fe3f-120"><dt>**HRESULT \_ à partir de \_ Win32 (erreur \_ \_ introuvable)**</dt></span><span class="sxs-lookup"><span data-stu-id="3fe3f-120"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="3fe3f-121">La propriété spécifiée par la *clé* ne figure pas dans la collection.</span><span class="sxs-lookup"><span data-stu-id="3fe3f-121">The property specified by *key* is not in the collection.</span></span><br/>    |



 

## <a name="requirements"></a><span data-ttu-id="3fe3f-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3fe3f-122">Requirements</span></span>



| <span data-ttu-id="3fe3f-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3fe3f-123">Requirement</span></span> | <span data-ttu-id="3fe3f-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="3fe3f-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fe3f-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="3fe3f-125">Header</span></span><br/>  | <dl> <span data-ttu-id="3fe3f-126"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="3fe3f-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="3fe3f-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3fe3f-127">Library</span></span><br/> | <dl> <span data-ttu-id="3fe3f-128"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3fe3f-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3fe3f-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3fe3f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fe3f-130">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="3fe3f-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="3fe3f-131">**IPortableDeviceValues::SetUnsignedLargeIntegerValue**</span><span class="sxs-lookup"><span data-stu-id="3fe3f-131">**IPortableDeviceValues::SetUnsignedLargeIntegerValue**</span></span>](iportabledevicevalues-setunsignedlargeintegervalue.md)
</dt> </dl>

 

 




