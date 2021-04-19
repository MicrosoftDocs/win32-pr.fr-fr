---
description: La méthode SetErrorValue ajoute une nouvelle valeur HRESULT (type VT \_ Error) ou remplace une valeur existante.
ms.assetid: 87369791-42bd-4523-b15a-acf0ea1e5af8
title: 'IPortableDeviceValues :: SetErrorValue, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetErrorValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 19c7ca57d325e31fd9cd8e0bf5130dc594b0b8cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534794"
---
# <a name="iportabledevicevaluesseterrorvalue-method"></a><span data-ttu-id="72f2c-103">IPortableDeviceValues :: SetErrorValue, méthode</span><span class="sxs-lookup"><span data-stu-id="72f2c-103">IPortableDeviceValues::SetErrorValue method</span></span>

<span data-ttu-id="72f2c-104">La méthode **SetErrorValue** ajoute une nouvelle valeur **HRESULT** (type VT \_ Error) ou remplace une valeur existante.</span><span class="sxs-lookup"><span data-stu-id="72f2c-104">The **SetErrorValue** method adds a new **HRESULT** value (type VT\_ERROR) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="72f2c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="72f2c-105">Syntax</span></span>


```C++
HRESULT SetErrorValue(
  [in]       REFPROPERTYKEY key,
  [in] const HRESULT        Value
);
```



## <a name="parameters"></a><span data-ttu-id="72f2c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="72f2c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72f2c-107">*clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="72f2c-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72f2c-108">**REFPROPERTYKEY** qui spécifie l’élément à créer ou à remplacer.</span><span class="sxs-lookup"><span data-stu-id="72f2c-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="72f2c-109">*Valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="72f2c-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72f2c-110">**HRESULT** qui contient la nouvelle valeur.</span><span class="sxs-lookup"><span data-stu-id="72f2c-110">An **HRESULT** that contains the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72f2c-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="72f2c-111">Return value</span></span>

<span data-ttu-id="72f2c-112">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="72f2c-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="72f2c-113">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="72f2c-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="72f2c-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="72f2c-114">Return code</span></span>                                                                          | <span data-ttu-id="72f2c-115">Description</span><span class="sxs-lookup"><span data-stu-id="72f2c-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="72f2c-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="72f2c-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="72f2c-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="72f2c-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="72f2c-118">Notes</span><span class="sxs-lookup"><span data-stu-id="72f2c-118">Remarks</span></span>

<span data-ttu-id="72f2c-119">Si une valeur existante a la même clé que celle spécifiée par le paramètre de *clé* , elle remplace la valeur existante sans avertissement.</span><span class="sxs-lookup"><span data-stu-id="72f2c-119">If an existing value has the same key specified by the *key* parameter, it overwrites the existing value without any warning.</span></span>

## <a name="requirements"></a><span data-ttu-id="72f2c-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="72f2c-120">Requirements</span></span>



| <span data-ttu-id="72f2c-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="72f2c-121">Requirement</span></span> | <span data-ttu-id="72f2c-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="72f2c-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72f2c-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="72f2c-123">Header</span></span><br/>  | <dl> <span data-ttu-id="72f2c-124"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="72f2c-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="72f2c-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="72f2c-125">Library</span></span><br/> | <dl> <span data-ttu-id="72f2c-126"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="72f2c-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72f2c-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="72f2c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72f2c-128">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="72f2c-128">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="72f2c-129">**IPortableDeviceValues::GetErrorValue**</span><span class="sxs-lookup"><span data-stu-id="72f2c-129">**IPortableDeviceValues::GetErrorValue**</span></span>](iportabledevicevalues-geterrorvalue.md)
</dt> </dl>

 

 




