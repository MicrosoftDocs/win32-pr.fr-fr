---
description: La méthode GetBoolValue récupère une valeur booléenne (type VT \_ bool) spécifiée par une clé.
ms.assetid: cb5fed7a-50b5-4af1-806a-c6582409d265
title: 'IPortableDeviceValues :: GetBoolValue, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetBoolValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 8554fc30a1b66226f6e4f8de4e5d8ac0e8abfabf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528703"
---
# <a name="iportabledevicevaluesgetboolvalue-method"></a><span data-ttu-id="64a01-103">IPortableDeviceValues :: GetBoolValue, méthode</span><span class="sxs-lookup"><span data-stu-id="64a01-103">IPortableDeviceValues::GetBoolValue method</span></span>

<span data-ttu-id="64a01-104">La méthode **GetBoolValue** récupère une valeur **BOOLÉENNE** (type VT \_ bool) spécifiée par une clé.</span><span class="sxs-lookup"><span data-stu-id="64a01-104">The **GetBoolValue** method retrieves a **Boolean** value (type VT\_BOOL) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="64a01-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="64a01-105">Syntax</span></span>


```C++
HRESULT GetBoolValue(
  [in]  REFPROPERTYKEY key,
  [out] BOOL           *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="64a01-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="64a01-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64a01-107">*clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="64a01-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64a01-108">Clé **REFPROPERTYKEY** qui spécifie l’élément à récupérer.</span><span class="sxs-lookup"><span data-stu-id="64a01-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="64a01-109">*pValue* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="64a01-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="64a01-110">Pointeur vers la valeur **booléenne** récupérée.</span><span class="sxs-lookup"><span data-stu-id="64a01-110">Pointer to the retrieved **BOOL** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64a01-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="64a01-111">Return value</span></span>

<span data-ttu-id="64a01-112">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="64a01-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="64a01-113">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="64a01-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="64a01-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="64a01-114">Return code</span></span>                                                                                                            | <span data-ttu-id="64a01-115">Description</span><span class="sxs-lookup"><span data-stu-id="64a01-115">Description</span></span>                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="64a01-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="64a01-116"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="64a01-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="64a01-117">The method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="64a01-118"><dt>**\_TYPEMISMATCH DISP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="64a01-118"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="64a01-119">La propriété spécifiée par la *clé* n’est pas un type **bool** .</span><span class="sxs-lookup"><span data-stu-id="64a01-119">The property specified by *key* is not a **BOOL** type.</span></span><br/>   |
| <dl> <span data-ttu-id="64a01-120"><dt>**HRESULT \_ à partir de \_ Win32 (erreur \_ \_ introuvable)**</dt></span><span class="sxs-lookup"><span data-stu-id="64a01-120"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="64a01-121">La propriété spécifiée par la *clé* ne figure pas dans la collection.</span><span class="sxs-lookup"><span data-stu-id="64a01-121">The property specified by *key* is not in the collection.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="64a01-122">Exemples</span><span class="sxs-lookup"><span data-stu-id="64a01-122">Examples</span></span>

<span data-ttu-id="64a01-123">Pour obtenir un exemple d’utilisation de cette méthode, consultez [définition des propriétés d’un objet unique](setting-properties-for-a-single-object.md).</span><span class="sxs-lookup"><span data-stu-id="64a01-123">For an example of how to use this method, see [Setting Properties for a Single Object](setting-properties-for-a-single-object.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="64a01-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="64a01-124">Requirements</span></span>



| <span data-ttu-id="64a01-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="64a01-125">Requirement</span></span> | <span data-ttu-id="64a01-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="64a01-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64a01-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="64a01-127">Header</span></span><br/>  | <dl> <span data-ttu-id="64a01-128"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="64a01-128"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="64a01-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="64a01-129">Library</span></span><br/> | <dl> <span data-ttu-id="64a01-130"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="64a01-130"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64a01-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="64a01-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64a01-132">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="64a01-132">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="64a01-133">**IPortableDeviceValues :: SetBoolValue,**</span><span class="sxs-lookup"><span data-stu-id="64a01-133">**IPortableDeviceValues::SetBoolValue**</span></span>](iportabledevicevalues-setboolvalue.md)
</dt> <dt>

[<span data-ttu-id="64a01-134">Récupération des événements de service pris en charge</span><span class="sxs-lookup"><span data-stu-id="64a01-134">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="64a01-135">Définition des propriétés d’un objet unique</span><span class="sxs-lookup"><span data-stu-id="64a01-135">Setting Properties for a Single Object</span></span>](setting-properties-for-a-single-object.md)
</dt> <dt>

[<span data-ttu-id="64a01-136">Écriture de propriétés Content-Object</span><span class="sxs-lookup"><span data-stu-id="64a01-136">Writing Content-Object Properties</span></span>](writing-content-object-properties.md)
</dt> </dl>

 

 




