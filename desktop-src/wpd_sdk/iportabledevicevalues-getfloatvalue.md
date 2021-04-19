---
description: La méthode GetFloatValue récupère une valeur FLOTTante (type VT \_ R4) spécifiée par une clé.
ms.assetid: 8a134dfb-f671-4cde-ae35-c8a41be270cf
title: 'IPortableDeviceValues :: GetFloatValue, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetFloatValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 0c99dcbb2d8436df7e3d593aa53efd086dc965ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520909"
---
# <a name="iportabledevicevaluesgetfloatvalue-method"></a><span data-ttu-id="d86e7-103">IPortableDeviceValues :: GetFloatValue, méthode</span><span class="sxs-lookup"><span data-stu-id="d86e7-103">IPortableDeviceValues::GetFloatValue method</span></span>

<span data-ttu-id="d86e7-104">La méthode **getFloatValue** récupère une valeur **flottante** (type VT \_ R4) spécifiée par une clé.</span><span class="sxs-lookup"><span data-stu-id="d86e7-104">The **GetFloatValue** method retrieves a **FLOAT** value (type VT\_R4) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="d86e7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d86e7-105">Syntax</span></span>


```C++
HRESULT GetFloatValue(
  [in]  REFPROPERTYKEY key,
  [out] FLOAT          *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="d86e7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d86e7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d86e7-107">*clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d86e7-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d86e7-108">Clé **REFPROPERTYKEY** qui spécifie l’élément à récupérer.</span><span class="sxs-lookup"><span data-stu-id="d86e7-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="d86e7-109">*pValue* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d86e7-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d86e7-110">Pointeur vers la valeur **float** récupérée.</span><span class="sxs-lookup"><span data-stu-id="d86e7-110">Pointer to the retrieved **FLOAT** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d86e7-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d86e7-111">Return value</span></span>

<span data-ttu-id="d86e7-112">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="d86e7-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="d86e7-113">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="d86e7-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="d86e7-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="d86e7-114">Return code</span></span>                                                                                             | <span data-ttu-id="d86e7-115">Description</span><span class="sxs-lookup"><span data-stu-id="d86e7-115">Description</span></span>                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="d86e7-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d86e7-116"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="d86e7-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="d86e7-117">The method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="d86e7-118"><dt>**\_TYPEMISMATCH DISP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d86e7-118"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>    | <span data-ttu-id="d86e7-119">La propriété spécifiée par la *clé* n’est pas un type **float** .</span><span class="sxs-lookup"><span data-stu-id="d86e7-119">The property specified by *key* is not a **FLOAT** type.</span></span><br/>  |
| <dl> <span data-ttu-id="d86e7-120"><dt>**\_ID prop \_ \_ non pris en charge**</dt></span><span class="sxs-lookup"><span data-stu-id="d86e7-120"><dt>**E\_PROP\_ID\_UNSUPPORTED**</dt></span></span> </dl> | <span data-ttu-id="d86e7-121">La propriété spécifiée par la *clé* ne figure pas dans la collection.</span><span class="sxs-lookup"><span data-stu-id="d86e7-121">The property specified by *key* is not in the collection.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d86e7-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d86e7-122">Requirements</span></span>



| <span data-ttu-id="d86e7-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d86e7-123">Requirement</span></span> | <span data-ttu-id="d86e7-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="d86e7-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d86e7-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="d86e7-125">Header</span></span><br/>  | <dl> <span data-ttu-id="d86e7-126"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="d86e7-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="d86e7-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d86e7-127">Library</span></span><br/> | <dl> <span data-ttu-id="d86e7-128"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d86e7-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d86e7-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d86e7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d86e7-130">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="d86e7-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="d86e7-131">**IPortableDeviceValues::SetFloatValue**</span><span class="sxs-lookup"><span data-stu-id="d86e7-131">**IPortableDeviceValues::SetFloatValue**</span></span>](iportabledevicevalues-setfloatvalue.md)
</dt> </dl>

 

 




