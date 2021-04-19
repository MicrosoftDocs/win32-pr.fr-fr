---
description: La méthode SetStringValue ajoute une nouvelle valeur de chaîne (type VT \_ LPWStr) ou remplace une valeur existante.
ms.assetid: a6eba2b9-de18-431e-874e-af68695e8d3f
title: 'IPortableDeviceValues :: SetStringValue, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetStringValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 163b5cd81ce8da64fc6d9f4304de5783b248522f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523971"
---
# <a name="iportabledevicevaluessetstringvalue-method"></a><span data-ttu-id="b6c48-103">IPortableDeviceValues :: SetStringValue, méthode</span><span class="sxs-lookup"><span data-stu-id="b6c48-103">IPortableDeviceValues::SetStringValue method</span></span>

<span data-ttu-id="b6c48-104">La méthode **SetStringValue** ajoute une nouvelle valeur de chaîne (type VT \_ LPWStr) ou remplace une valeur existante.</span><span class="sxs-lookup"><span data-stu-id="b6c48-104">The **SetStringValue** method adds a new string value (type VT\_LPWSTR) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6c48-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b6c48-105">Syntax</span></span>


```C++
HRESULT SetStringValue(
  [in] REFPROPERTYKEY key,
  [in] LPCWSTR        Value
);
```



## <a name="parameters"></a><span data-ttu-id="b6c48-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b6c48-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6c48-107">*clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b6c48-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6c48-108">**REFPROPERTYKEY** qui spécifie l’élément à créer ou à remplacer.</span><span class="sxs-lookup"><span data-stu-id="b6c48-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="b6c48-109">*Valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b6c48-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6c48-110">**LPCWSTR** qui spécifie la nouvelle valeur.</span><span class="sxs-lookup"><span data-stu-id="b6c48-110">A **LPCWSTR** that specifies the new value.</span></span> <span data-ttu-id="b6c48-111">La chaîne étant copiée, l’appelant peut libérer la mémoire allouée pour cette valeur après l’appel de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="b6c48-111">The string is copied, so the caller can release the memory allocated for this value after calling this method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6c48-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b6c48-112">Return value</span></span>

<span data-ttu-id="b6c48-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="b6c48-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="b6c48-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="b6c48-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="b6c48-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="b6c48-115">Return code</span></span>                                                                          | <span data-ttu-id="b6c48-116">Description</span><span class="sxs-lookup"><span data-stu-id="b6c48-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="b6c48-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b6c48-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="b6c48-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="b6c48-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b6c48-119">Notes</span><span class="sxs-lookup"><span data-stu-id="b6c48-119">Remarks</span></span>

<span data-ttu-id="b6c48-120">Toute mémoire de clé existante sera libérée de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="b6c48-120">Any existing key memory will be released appropriately.</span></span>

## <a name="examples"></a><span data-ttu-id="b6c48-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="b6c48-121">Examples</span></span>

<span data-ttu-id="b6c48-122">Pour obtenir un exemple d’utilisation de cette méthode, consultez [spécification des informations sur le client](specifying-client-information.md).</span><span class="sxs-lookup"><span data-stu-id="b6c48-122">For an example of how to use this method, see [Specifying Client Information](specifying-client-information.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b6c48-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b6c48-123">Requirements</span></span>



| <span data-ttu-id="b6c48-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b6c48-124">Requirement</span></span> | <span data-ttu-id="b6c48-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="b6c48-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6c48-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="b6c48-126">Header</span></span><br/>  | <dl> <span data-ttu-id="b6c48-127"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6c48-127"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="b6c48-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b6c48-128">Library</span></span><br/> | <dl> <span data-ttu-id="b6c48-129"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b6c48-129"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6c48-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6c48-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6c48-131">Ajout d’une ressource à un objet</span><span class="sxs-lookup"><span data-stu-id="b6c48-131">Adding a Resource to an Object</span></span>](adding-a-resource-to-an-object.md)
</dt> <dt>

[<span data-ttu-id="b6c48-132">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="b6c48-132">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="b6c48-133">**IPortableDeviceValues :: GetStringValue**</span><span class="sxs-lookup"><span data-stu-id="b6c48-133">**IPortableDeviceValues::GetStringValue**</span></span>](iportabledevicevalues-getstringvalue.md)
</dt> <dt>

[<span data-ttu-id="b6c48-134">Définition des propriétés d’un objet unique</span><span class="sxs-lookup"><span data-stu-id="b6c48-134">Setting Properties for a Single Object</span></span>](setting-properties-for-a-single-object.md)
</dt> <dt>

[<span data-ttu-id="b6c48-135">Définition des propriétés de plusieurs objets</span><span class="sxs-lookup"><span data-stu-id="b6c48-135">Setting Properties for Multiple Objects</span></span>](setting-properties-for-multiple-objects.md)
</dt> <dt>

[<span data-ttu-id="b6c48-136">Spécification des informations sur le client</span><span class="sxs-lookup"><span data-stu-id="b6c48-136">Specifying Client Information</span></span>](specifying-client-information.md)
</dt> <dt>

[<span data-ttu-id="b6c48-137">Écriture de propriétés Content-Object</span><span class="sxs-lookup"><span data-stu-id="b6c48-137">Writing Content-Object Properties</span></span>](writing-content-object-properties.md)
</dt> </dl>

 

 




