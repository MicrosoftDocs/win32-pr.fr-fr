---
description: La méthode GetGuidValue récupère une valeur GUID (type VT \_ CLSID) spécifiée par une clé.
ms.assetid: 1cfa75e8-2c3b-4893-954e-dae25a6b8220
title: 'IPortableDeviceValues :: GetGuidValue, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetGuidValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 362672daad835a2e843edeaf6dc517884c25f1ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531084"
---
# <a name="iportabledevicevaluesgetguidvalue-method"></a><span data-ttu-id="fbf08-103">IPortableDeviceValues :: GetGuidValue, méthode</span><span class="sxs-lookup"><span data-stu-id="fbf08-103">IPortableDeviceValues::GetGuidValue method</span></span>

<span data-ttu-id="fbf08-104">La méthode **GetGuidValue** récupère une valeur **GUID** (type VT \_ CLSID) spécifiée par une clé.</span><span class="sxs-lookup"><span data-stu-id="fbf08-104">The **GetGuidValue** method retrieves a **GUID** value (type VT\_CLSID) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbf08-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fbf08-105">Syntax</span></span>


```C++
HRESULT GetGuidValue(
  [in]  REFPROPERTYKEY key,
  [out] GUID           *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="fbf08-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fbf08-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbf08-107">*clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fbf08-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbf08-108">Clé **REFPROPERTYKEY** qui spécifie l’élément à récupérer.</span><span class="sxs-lookup"><span data-stu-id="fbf08-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="fbf08-109">*pValue* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="fbf08-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fbf08-110">Pointeur vers la valeur de **GUID** récupérée.</span><span class="sxs-lookup"><span data-stu-id="fbf08-110">Pointer to the retrieved **GUID** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbf08-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fbf08-111">Return value</span></span>

<span data-ttu-id="fbf08-112">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="fbf08-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="fbf08-113">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="fbf08-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="fbf08-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="fbf08-114">Return code</span></span>                                                                                                            | <span data-ttu-id="fbf08-115">Description</span><span class="sxs-lookup"><span data-stu-id="fbf08-115">Description</span></span>                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="fbf08-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fbf08-116"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="fbf08-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="fbf08-117">The method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="fbf08-118"><dt>**\_TYPEMISMATCH DISP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fbf08-118"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="fbf08-119">La propriété spécifiée par la *clé* n’est pas un type **GUID** .</span><span class="sxs-lookup"><span data-stu-id="fbf08-119">The property specified by *key* is not a **GUID** type.</span></span><br/>   |
| <dl> <span data-ttu-id="fbf08-120"><dt>**HRESULT \_ à partir de \_ Win32 (erreur \_ \_ introuvable)**</dt></span><span class="sxs-lookup"><span data-stu-id="fbf08-120"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="fbf08-121">La propriété spécifiée par la *clé* ne figure pas dans la collection.</span><span class="sxs-lookup"><span data-stu-id="fbf08-121">The property specified by *key* is not in the collection.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="fbf08-122">Exemples</span><span class="sxs-lookup"><span data-stu-id="fbf08-122">Examples</span></span>

<span data-ttu-id="fbf08-123">Pour obtenir un exemple d’utilisation de cette méthode, consultez [récupération des méthodes de service prises en charge](retrieving-supported-methods.md).</span><span class="sxs-lookup"><span data-stu-id="fbf08-123">For an example of how to use this method, see [Retrieving Supported Service Methods](retrieving-supported-methods.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fbf08-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fbf08-124">Requirements</span></span>



| <span data-ttu-id="fbf08-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fbf08-125">Requirement</span></span> | <span data-ttu-id="fbf08-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="fbf08-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbf08-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="fbf08-127">Header</span></span><br/>  | <dl> <span data-ttu-id="fbf08-128"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="fbf08-128"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="fbf08-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fbf08-129">Library</span></span><br/> | <dl> <span data-ttu-id="fbf08-130"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fbf08-130"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fbf08-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fbf08-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbf08-132">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="fbf08-132">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="fbf08-133">**IPortableDeviceValues::SetGuidValue**</span><span class="sxs-lookup"><span data-stu-id="fbf08-133">**IPortableDeviceValues::SetGuidValue**</span></span>](iportabledevicevalues-setguidvalue.md)
</dt> <dt>

[<span data-ttu-id="fbf08-134">Récupération des méthodes de service prises en charge</span><span class="sxs-lookup"><span data-stu-id="fbf08-134">Retrieving Supported Service Methods</span></span>](retrieving-supported-methods.md)
</dt> <dt>

[<span data-ttu-id="fbf08-135">Récupération des fonctionnalités de rendu prises en charge par un appareil</span><span class="sxs-lookup"><span data-stu-id="fbf08-135">Retrieving the Rendering Capabilities Supported by a Device</span></span>](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> </dl>

 

 




