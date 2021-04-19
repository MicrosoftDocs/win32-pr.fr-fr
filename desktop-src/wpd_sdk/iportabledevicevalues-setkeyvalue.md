---
description: La méthode SetKeyValue ajoute une nouvelle valeur REFPROPERTYKEY (type VT \_ inconnu) ou remplace celle qui existe déjà.
ms.assetid: 344c52ec-91b1-43f9-b16a-28c24971d805
title: 'IPortableDeviceValues :: SetKeyValue, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetKeyValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: ae55b47687043bba92afbab09f25de8a5fc679d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532584"
---
# <a name="iportabledevicevaluessetkeyvalue-method"></a><span data-ttu-id="605cf-103">IPortableDeviceValues :: SetKeyValue, méthode</span><span class="sxs-lookup"><span data-stu-id="605cf-103">IPortableDeviceValues::SetKeyValue method</span></span>

<span data-ttu-id="605cf-104">La méthode **SetKeyValue** ajoute une nouvelle valeur **REFPROPERTYKEY** (type VT \_ inconnu) ou remplace celle qui existe déjà.</span><span class="sxs-lookup"><span data-stu-id="605cf-104">The **SetKeyValue** method adds a new **REFPROPERTYKEY** value (type VT\_UNKNOWN) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="605cf-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="605cf-105">Syntax</span></span>


```C++
HRESULT SetKeyValue(
  [in] REFPROPERTYKEY key,
  [in] REFPROPERTYKEY Value
);
```



## <a name="parameters"></a><span data-ttu-id="605cf-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="605cf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="605cf-107">*clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="605cf-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="605cf-108">**REFPROPERTYKEY** qui spécifie l’élément à créer ou à remplacer.</span><span class="sxs-lookup"><span data-stu-id="605cf-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="605cf-109">*Valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="605cf-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="605cf-110">**REFPROPERTYKEY** qui spécifie la nouvelle valeur.</span><span class="sxs-lookup"><span data-stu-id="605cf-110">A **REFPROPERTYKEY** that specifies the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="605cf-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="605cf-111">Return value</span></span>

<span data-ttu-id="605cf-112">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="605cf-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="605cf-113">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="605cf-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="605cf-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="605cf-114">Return code</span></span>                                                                          | <span data-ttu-id="605cf-115">Description</span><span class="sxs-lookup"><span data-stu-id="605cf-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="605cf-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="605cf-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="605cf-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="605cf-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="605cf-118">Notes</span><span class="sxs-lookup"><span data-stu-id="605cf-118">Remarks</span></span>

<span data-ttu-id="605cf-119">Si une valeur existante a la même clé que celle spécifiée par le paramètre de *clé* , elle remplace la valeur existante sans avertissement.</span><span class="sxs-lookup"><span data-stu-id="605cf-119">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span> <span data-ttu-id="605cf-120">La mémoire clé existante est libérée de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="605cf-120">The existing key memory is released appropriately.</span></span>

## <a name="requirements"></a><span data-ttu-id="605cf-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="605cf-121">Requirements</span></span>



| <span data-ttu-id="605cf-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="605cf-122">Requirement</span></span> | <span data-ttu-id="605cf-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="605cf-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="605cf-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="605cf-124">Header</span></span><br/>  | <dl> <span data-ttu-id="605cf-125"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="605cf-125"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="605cf-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="605cf-126">Library</span></span><br/> | <dl> <span data-ttu-id="605cf-127"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="605cf-127"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="605cf-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="605cf-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="605cf-129">Ajout d’une ressource à un objet</span><span class="sxs-lookup"><span data-stu-id="605cf-129">Adding a Resource to an Object</span></span>](adding-a-resource-to-an-object.md)
</dt> <dt>

[<span data-ttu-id="605cf-130">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="605cf-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="605cf-131">**IPortableDeviceValues::GetKeyValue**</span><span class="sxs-lookup"><span data-stu-id="605cf-131">**IPortableDeviceValues::GetKeyValue**</span></span>](iportabledevicevalues-getkeyvalue.md)
</dt> </dl>

 

 




