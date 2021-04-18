---
description: La méthode GetKeyValue récupère une valeur PROPERTYKEY spécifiée par une clé.
ms.assetid: 2c92b1c0-3ea6-4a14-8b63-d57752b649b8
title: 'IPortableDeviceValues :: GetKeyValue, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetKeyValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 3d5080a35faa5555d2813c6e419a1965def05bdd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540425"
---
# <a name="iportabledevicevaluesgetkeyvalue-method"></a><span data-ttu-id="a15bd-103">IPortableDeviceValues :: GetKeyValue, méthode</span><span class="sxs-lookup"><span data-stu-id="a15bd-103">IPortableDeviceValues::GetKeyValue method</span></span>

<span data-ttu-id="a15bd-104">La méthode **GetKeyValue** récupère une valeur **PROPERTYKEY** spécifiée par une clé.</span><span class="sxs-lookup"><span data-stu-id="a15bd-104">The **GetKeyValue** method retrieves a **PROPERTYKEY** value specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="a15bd-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a15bd-105">Syntax</span></span>


```C++
HRESULT GetKeyValue(
  [in]  REFPROPERTYKEY key,
  [out] PROPERTYKEY    *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="a15bd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a15bd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a15bd-107">*clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a15bd-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a15bd-108">Clé **REFPROPERTYKEY** qui spécifie l’élément à récupérer.</span><span class="sxs-lookup"><span data-stu-id="a15bd-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="a15bd-109">*pValue* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a15bd-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a15bd-110">Pointeur vers la valeur **PROPERTYKEY** récupérée.</span><span class="sxs-lookup"><span data-stu-id="a15bd-110">Pointer to the retrieved **PROPERTYKEY** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a15bd-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a15bd-111">Return value</span></span>

<span data-ttu-id="a15bd-112">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="a15bd-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="a15bd-113">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="a15bd-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="a15bd-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="a15bd-114">Return code</span></span>                                                                                                            | <span data-ttu-id="a15bd-115">Description</span><span class="sxs-lookup"><span data-stu-id="a15bd-115">Description</span></span>                                                               |
|------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a15bd-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a15bd-116"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="a15bd-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="a15bd-117">The method succeeded.</span></span><br/>                                          |
| <dl> <span data-ttu-id="a15bd-118"><dt>**\_TYPEMISMATCH DISP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a15bd-118"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="a15bd-119">La propriété spécifiée par *Key* n’est pas un type **PROPERTYKEY** .</span><span class="sxs-lookup"><span data-stu-id="a15bd-119">The property specified by *key* is not a **PROPERTYKEY** type.</span></span><br/> |
| <dl> <span data-ttu-id="a15bd-120"><dt>**HRESULT \_ à partir de \_ Win32 (erreur \_ \_ introuvable)**</dt></span><span class="sxs-lookup"><span data-stu-id="a15bd-120"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="a15bd-121">La propriété spécifiée par la *clé* ne figure pas dans la collection.</span><span class="sxs-lookup"><span data-stu-id="a15bd-121">The property specified by *key* is not in the collection.</span></span><br/>      |



 

## <a name="requirements"></a><span data-ttu-id="a15bd-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a15bd-122">Requirements</span></span>



| <span data-ttu-id="a15bd-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a15bd-123">Requirement</span></span> | <span data-ttu-id="a15bd-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="a15bd-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a15bd-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="a15bd-125">Header</span></span><br/>  | <dl> <span data-ttu-id="a15bd-126"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="a15bd-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="a15bd-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a15bd-127">Library</span></span><br/> | <dl> <span data-ttu-id="a15bd-128"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a15bd-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a15bd-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a15bd-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a15bd-130">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="a15bd-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="a15bd-131">**IPortableDeviceValues::SetKeyValue**</span><span class="sxs-lookup"><span data-stu-id="a15bd-131">**IPortableDeviceValues::SetKeyValue**</span></span>](iportabledevicevalues-setkeyvalue.md)
</dt> </dl>

 

 




