---
description: La méthode GetErrorValue récupère une valeur HRESULT (type VT \_ ) spécifiée par une clé.
ms.assetid: af57ddbd-5503-4b9b-bd75-ba9c9c202b73
title: 'IPortableDeviceValues :: GetErrorValue, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetErrorValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 86e5dacfa398cfe2bb57bfd289e4c8e792f14a66
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532636"
---
# <a name="iportabledevicevaluesgeterrorvalue-method"></a><span data-ttu-id="8d72a-103">IPortableDeviceValues :: GetErrorValue, méthode</span><span class="sxs-lookup"><span data-stu-id="8d72a-103">IPortableDeviceValues::GetErrorValue method</span></span>

<span data-ttu-id="8d72a-104">La méthode **GetErrorValue** récupère une valeur **HRESULT** (type VT \_ ) spécifiée par une clé.</span><span class="sxs-lookup"><span data-stu-id="8d72a-104">The **GetErrorValue** method retrieves an **HRESULT** value (type VT\_ERROR) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d72a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8d72a-105">Syntax</span></span>


```C++
HRESULT GetErrorValue(
  [in]  REFPROPERTYKEY key,
  [out] HRESULT        *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="8d72a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8d72a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d72a-107">*clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8d72a-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d72a-108">Clé **REFPROPERTYKEY** qui spécifie l’élément à récupérer.</span><span class="sxs-lookup"><span data-stu-id="8d72a-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="8d72a-109">*pValue* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="8d72a-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8d72a-110">Pointeur vers la valeur **HRESULT** récupérée.</span><span class="sxs-lookup"><span data-stu-id="8d72a-110">Pointer to the retrieved **HRESULT** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d72a-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8d72a-111">Return value</span></span>

<span data-ttu-id="8d72a-112">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="8d72a-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="8d72a-113">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="8d72a-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="8d72a-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="8d72a-114">Return code</span></span>                                                                                                            | <span data-ttu-id="8d72a-115">Description</span><span class="sxs-lookup"><span data-stu-id="8d72a-115">Description</span></span>                                                            |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8d72a-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8d72a-116"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="8d72a-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="8d72a-117">The method succeeded.</span></span><br/>                                       |
| <dl> <span data-ttu-id="8d72a-118"><dt>**\_TYPEMISMATCH DISP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8d72a-118"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="8d72a-119">La propriété spécifiée par la *clé* n’est pas un type **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8d72a-119">The property specified by *key* is not an **HRESULT** type.</span></span><br/> |
| <dl> <span data-ttu-id="8d72a-120"><dt>**HRESULT \_ à partir de \_ Win32 (erreur \_ \_ introuvable)**</dt></span><span class="sxs-lookup"><span data-stu-id="8d72a-120"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="8d72a-121">La propriété spécifiée par la *clé* ne figure pas dans la collection.</span><span class="sxs-lookup"><span data-stu-id="8d72a-121">The property specified by *key* is not in the collection.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="8d72a-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8d72a-122">Requirements</span></span>



| <span data-ttu-id="8d72a-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8d72a-123">Requirement</span></span> | <span data-ttu-id="8d72a-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="8d72a-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d72a-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="8d72a-125">Header</span></span><br/>  | <dl> <span data-ttu-id="8d72a-126"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d72a-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="8d72a-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8d72a-127">Library</span></span><br/> | <dl> <span data-ttu-id="8d72a-128"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8d72a-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d72a-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8d72a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d72a-130">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="8d72a-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="8d72a-131">**IPortableDeviceValues::SetErrorValue**</span><span class="sxs-lookup"><span data-stu-id="8d72a-131">**IPortableDeviceValues::SetErrorValue**</span></span>](iportabledevicevalues-seterrorvalue.md)
</dt> </dl>

 

 




