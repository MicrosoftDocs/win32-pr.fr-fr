---
description: La méthode GetUnsignedIntegerValue récupère une valeur ULONG (type VT \_ UI4) spécifiée par une clé.
ms.assetid: 167163fa-6583-4e6b-b801-3a441a95644b
title: 'IPortableDeviceValues :: GetUnsignedIntegerValue, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetUnsignedIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 5c7deb0b6ebfdb8feb90248f9d8e1cdf68411d9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528666"
---
# <a name="iportabledevicevaluesgetunsignedintegervalue-method"></a><span data-ttu-id="eb297-103">IPortableDeviceValues :: GetUnsignedIntegerValue, méthode</span><span class="sxs-lookup"><span data-stu-id="eb297-103">IPortableDeviceValues::GetUnsignedIntegerValue method</span></span>

<span data-ttu-id="eb297-104">La méthode **GetUnsignedIntegerValue** récupère une valeur **ULong** (type VT \_ UI4) spécifiée par une clé.</span><span class="sxs-lookup"><span data-stu-id="eb297-104">The **GetUnsignedIntegerValue** method retrieves a **ULONG** value (type VT\_UI4) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb297-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eb297-105">Syntax</span></span>


```C++
HRESULT GetUnsignedIntegerValue(
  [in]  REFPROPERTYKEY key,
  [out] ULONG          *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="eb297-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eb297-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb297-107">*clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="eb297-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb297-108">Clé **REFPROPERTYKEY** qui spécifie l’élément à récupérer.</span><span class="sxs-lookup"><span data-stu-id="eb297-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="eb297-109">*pValue* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="eb297-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eb297-110">Pointeur vers la valeur **ULong** récupérée.</span><span class="sxs-lookup"><span data-stu-id="eb297-110">Pointer to the retrieved **ULONG** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb297-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="eb297-111">Return value</span></span>

<span data-ttu-id="eb297-112">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="eb297-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="eb297-113">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="eb297-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="eb297-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="eb297-114">Return code</span></span>                                                                                                            | <span data-ttu-id="eb297-115">Description</span><span class="sxs-lookup"><span data-stu-id="eb297-115">Description</span></span>                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="eb297-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="eb297-116"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="eb297-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="eb297-117">The method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="eb297-118"><dt>**\_TYPEMISMATCH DISP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="eb297-118"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="eb297-119">La propriété spécifiée par la *clé* n’est pas un type **ULong** .</span><span class="sxs-lookup"><span data-stu-id="eb297-119">The property specified by *key* is not a **ULONG** type.</span></span><br/>  |
| <dl> <span data-ttu-id="eb297-120"><dt>**HRESULT \_ à partir de \_ Win32 (erreur \_ \_ introuvable)**</dt></span><span class="sxs-lookup"><span data-stu-id="eb297-120"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="eb297-121">La propriété spécifiée par la *clé* ne figure pas dans la collection.</span><span class="sxs-lookup"><span data-stu-id="eb297-121">The property specified by *key* is not in the collection.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="eb297-122">Exemples</span><span class="sxs-lookup"><span data-stu-id="eb297-122">Examples</span></span>

<span data-ttu-id="eb297-123">Pour obtenir un exemple d’utilisation de cette méthode, consultez [récupération des événements de service pris en charge](retrieving-supported-events.md).</span><span class="sxs-lookup"><span data-stu-id="eb297-123">For an example of how to use this method, see [Retrieving Supported Service Events](retrieving-supported-events.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="eb297-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eb297-124">Requirements</span></span>



| <span data-ttu-id="eb297-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eb297-125">Requirement</span></span> | <span data-ttu-id="eb297-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="eb297-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb297-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="eb297-127">Header</span></span><br/>  | <dl> <span data-ttu-id="eb297-128"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb297-128"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="eb297-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="eb297-129">Library</span></span><br/> | <dl> <span data-ttu-id="eb297-130"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eb297-130"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb297-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb297-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb297-132">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="eb297-132">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="eb297-133">**IPortableDeviceValues::SetUnsignedIntegerValue**</span><span class="sxs-lookup"><span data-stu-id="eb297-133">**IPortableDeviceValues::SetUnsignedIntegerValue**</span></span>](iportabledevicevalues-setunsignedintegervalue.md)
</dt> <dt>

[<span data-ttu-id="eb297-134">Récupération des événements de service pris en charge</span><span class="sxs-lookup"><span data-stu-id="eb297-134">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="eb297-135">Récupération des méthodes de service prises en charge</span><span class="sxs-lookup"><span data-stu-id="eb297-135">Retrieving Supported Service Methods</span></span>](retrieving-supported-methods.md)
</dt> <dt>

[<span data-ttu-id="eb297-136">Récupération des fonctionnalités de rendu prises en charge par un appareil</span><span class="sxs-lookup"><span data-stu-id="eb297-136">Retrieving the Rendering Capabilities Supported by a Device</span></span>](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> </dl>

 

 




