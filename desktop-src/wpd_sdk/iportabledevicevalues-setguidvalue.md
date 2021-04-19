---
description: La méthode SetGuidValue ajoute une nouvelle valeur GUID (type VT \_ CLSID) ou remplace celle qui existe déjà.
ms.assetid: 429a83c0-59b6-4e2f-a657-cbec1dfb9070
title: 'IPortableDeviceValues :: SetGuidValue, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetGuidValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 9d9f85def6ba487163f7c4c7d7441a89e0747ed6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530532"
---
# <a name="iportabledevicevaluessetguidvalue-method"></a><span data-ttu-id="c8711-103">IPortableDeviceValues :: SetGuidValue, méthode</span><span class="sxs-lookup"><span data-stu-id="c8711-103">IPortableDeviceValues::SetGuidValue method</span></span>

<span data-ttu-id="c8711-104">La méthode **SetGuidValue** ajoute une nouvelle valeur **GUID** (type VT \_ CLSID) ou remplace celle qui existe déjà.</span><span class="sxs-lookup"><span data-stu-id="c8711-104">The **SetGuidValue** method adds a new **GUID** value (type VT\_CLSID) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8711-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c8711-105">Syntax</span></span>


```C++
HRESULT SetGuidValue(
  [in] REFPROPERTYKEY key,
  [in] REFGUID        Value
);
```



## <a name="parameters"></a><span data-ttu-id="c8711-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c8711-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8711-107">*clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c8711-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8711-108">**REFPROPERTYKEY** qui spécifie l’élément à créer ou à remplacer.</span><span class="sxs-lookup"><span data-stu-id="c8711-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="c8711-109">*Valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c8711-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8711-110">**REFGUID** qui contient la nouvelle valeur.</span><span class="sxs-lookup"><span data-stu-id="c8711-110">A **REFGUID** that contains the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8711-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c8711-111">Return value</span></span>

<span data-ttu-id="c8711-112">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="c8711-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="c8711-113">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="c8711-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="c8711-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="c8711-114">Return code</span></span>                                                                          | <span data-ttu-id="c8711-115">Description</span><span class="sxs-lookup"><span data-stu-id="c8711-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="c8711-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c8711-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="c8711-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="c8711-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c8711-118">Notes</span><span class="sxs-lookup"><span data-stu-id="c8711-118">Remarks</span></span>

<span data-ttu-id="c8711-119">Si une valeur existante a la même clé que celle spécifiée par le paramètre de *clé* , elle remplace la valeur existante sans avertissement.</span><span class="sxs-lookup"><span data-stu-id="c8711-119">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8711-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c8711-120">Requirements</span></span>



| <span data-ttu-id="c8711-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c8711-121">Requirement</span></span> | <span data-ttu-id="c8711-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="c8711-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8711-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="c8711-123">Header</span></span><br/>  | <dl> <span data-ttu-id="c8711-124"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8711-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="c8711-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c8711-125">Library</span></span><br/> | <dl> <span data-ttu-id="c8711-126"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c8711-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8711-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c8711-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8711-128">Ajout d’une ressource à un objet</span><span class="sxs-lookup"><span data-stu-id="c8711-128">Adding a Resource to an Object</span></span>](adding-a-resource-to-an-object.md)
</dt> <dt>

[<span data-ttu-id="c8711-129">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="c8711-129">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="c8711-130">**IPortableDeviceValues::GetGuidValue**</span><span class="sxs-lookup"><span data-stu-id="c8711-130">**IPortableDeviceValues::GetGuidValue**</span></span>](iportabledevicevalues-getguidvalue.md)
</dt> </dl>

 

 




