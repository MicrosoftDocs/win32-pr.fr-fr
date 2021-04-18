---
description: La méthode GetIPortableDeviceValuesValue récupère une valeur IPortableDeviceValues (type VT \_ inconnu) spécifiée par une clé.
ms.assetid: bf62c6a9-560b-4667-94d0-2dea6657eed1
title: 'IPortableDeviceValues :: GetIPortableDeviceValuesValue, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetIPortableDeviceValuesValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 9583ea157c1e3395fd9814b1a2e78af3f1985b9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543314"
---
# <a name="iportabledevicevaluesgetiportabledevicevaluesvalue-method"></a><span data-ttu-id="0c66a-103">IPortableDeviceValues :: GetIPortableDeviceValuesValue, méthode</span><span class="sxs-lookup"><span data-stu-id="0c66a-103">IPortableDeviceValues::GetIPortableDeviceValuesValue method</span></span>

<span data-ttu-id="0c66a-104">La méthode **GetIPortableDeviceValuesValue** récupère une valeur **IPORTABLEDEVICEVALUES** (type VT \_ inconnu) spécifiée par une clé.</span><span class="sxs-lookup"><span data-stu-id="0c66a-104">The **GetIPortableDeviceValuesValue** method retrieves an **IPortableDeviceValues** value (type VT\_UNKNOWN) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c66a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0c66a-105">Syntax</span></span>


```C++
HRESULT GetIPortableDeviceValuesValue(
  [in]  REFPROPERTYKEY        key,
  [out] IPortableDeviceValues **ppValue
);
```



## <a name="parameters"></a><span data-ttu-id="0c66a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0c66a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c66a-107">*clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0c66a-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c66a-108">Clé **REFPROPERTYKEY** qui spécifie l’élément à récupérer.</span><span class="sxs-lookup"><span data-stu-id="0c66a-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="0c66a-109">*ppValue* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="0c66a-109">*ppValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0c66a-110">Adresse d’une variable qui reçoit un pointeur vers l’interface [**IPortableDeviceValues**](iportabledevicevalues.md) récupérée.</span><span class="sxs-lookup"><span data-stu-id="0c66a-110">Address of a variable that receives a pointer to the retrieved [**IPortableDeviceValues**](iportabledevicevalues.md) interface.</span></span> <span data-ttu-id="0c66a-111">L’appelant est responsable de l’appel de **Release** sur l’interface récupérée.</span><span class="sxs-lookup"><span data-stu-id="0c66a-111">The caller is responsible for calling **Release** on the retrieved interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c66a-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0c66a-112">Return value</span></span>

<span data-ttu-id="0c66a-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="0c66a-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="0c66a-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="0c66a-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="0c66a-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="0c66a-115">Return code</span></span>                                                                                                            | <span data-ttu-id="0c66a-116">Description</span><span class="sxs-lookup"><span data-stu-id="0c66a-116">Description</span></span>                                                                               |
|------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0c66a-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0c66a-117"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="0c66a-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="0c66a-118">The method succeeded.</span></span><br/>                                                          |
| <dl> <span data-ttu-id="0c66a-119"><dt>**\_TYPEMISMATCH DISP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0c66a-119"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="0c66a-120">La propriété spécifiée par *Key* n’est pas une interface **IPortableDeviceValues** .</span><span class="sxs-lookup"><span data-stu-id="0c66a-120">The property specified by *key* is not an **IPortableDeviceValues** interface.</span></span><br/> |
| <dl> <span data-ttu-id="0c66a-121"><dt>**HRESULT \_ à partir de \_ Win32 (erreur \_ \_ introuvable)**</dt></span><span class="sxs-lookup"><span data-stu-id="0c66a-121"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="0c66a-122">La propriété spécifiée par la *clé* ne figure pas dans la collection.</span><span class="sxs-lookup"><span data-stu-id="0c66a-122">The property specified by *key* is not in the collection.</span></span><br/>                      |



 

## <a name="examples"></a><span data-ttu-id="0c66a-123">Exemples</span><span class="sxs-lookup"><span data-stu-id="0c66a-123">Examples</span></span>

<span data-ttu-id="0c66a-124">Pour obtenir un exemple d’utilisation de cette méthode, consultez [récupération des événements de service pris en charge](retrieving-supported-events.md).</span><span class="sxs-lookup"><span data-stu-id="0c66a-124">For an example of how to use this method, see [Retrieving Supported Service Events](retrieving-supported-events.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0c66a-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0c66a-125">Requirements</span></span>



| <span data-ttu-id="0c66a-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0c66a-126">Requirement</span></span> | <span data-ttu-id="0c66a-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="0c66a-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c66a-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="0c66a-128">Header</span></span><br/>  | <dl> <span data-ttu-id="0c66a-129"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c66a-129"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="0c66a-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0c66a-130">Library</span></span><br/> | <dl> <span data-ttu-id="0c66a-131"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0c66a-131"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c66a-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c66a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c66a-133">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="0c66a-133">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="0c66a-134">**IPortableDeviceValues::SetIPortableDeviceValuesValue**</span><span class="sxs-lookup"><span data-stu-id="0c66a-134">**IPortableDeviceValues::SetIPortableDeviceValuesValue**</span></span>](iportabledevicevalues-setiportabledevicevaluesvalue.md)
</dt> <dt>

[<span data-ttu-id="0c66a-135">Récupération des événements de service pris en charge</span><span class="sxs-lookup"><span data-stu-id="0c66a-135">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="0c66a-136">Récupération des fonctionnalités de rendu prises en charge par un appareil</span><span class="sxs-lookup"><span data-stu-id="0c66a-136">Retrieving the Rendering Capabilities Supported by a Device</span></span>](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> </dl>

 

 




