---
description: La méthode SetUnsignedLargeIntegerValue ajoute une nouvelle valeur ULONGLONG (type VT \_ UI8) ou remplace celle qui existe déjà.
ms.assetid: 64874b86-7bf1-407a-8fff-a2c07c22f0cb
title: 'IPortableDeviceValues :: SetUnsignedLargeIntegerValue, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetUnsignedLargeIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 0c1ade76b4242c7508cb325e90c567349afcdc9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541071"
---
# <a name="iportabledevicevaluessetunsignedlargeintegervalue-method"></a><span data-ttu-id="cc006-103">IPortableDeviceValues :: SetUnsignedLargeIntegerValue, méthode</span><span class="sxs-lookup"><span data-stu-id="cc006-103">IPortableDeviceValues::SetUnsignedLargeIntegerValue method</span></span>

<span data-ttu-id="cc006-104">La méthode **SetUnsignedLargeIntegerValue** ajoute une nouvelle valeur **ULONGLONG** (type VT \_ UI8) ou remplace celle qui existe déjà.</span><span class="sxs-lookup"><span data-stu-id="cc006-104">The **SetUnsignedLargeIntegerValue** method adds a new **ULONGLONG** value (type VT\_UI8) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc006-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cc006-105">Syntax</span></span>


```C++
HRESULT SetUnsignedLargeIntegerValue(
  [in]       REFPROPERTYKEY key,
  [in] const ULONGLONG      Value
);
```



## <a name="parameters"></a><span data-ttu-id="cc006-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cc006-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc006-107">*clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cc006-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc006-108">**REFPROPERTYKEY** qui spécifie l’élément à créer ou à remplacer.</span><span class="sxs-lookup"><span data-stu-id="cc006-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="cc006-109">*Valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cc006-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc006-110">**ULONGLONG** qui spécifie la nouvelle valeur.</span><span class="sxs-lookup"><span data-stu-id="cc006-110">A **ULONGLONG** that specifies the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc006-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cc006-111">Return value</span></span>

<span data-ttu-id="cc006-112">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="cc006-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="cc006-113">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="cc006-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="cc006-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="cc006-114">Return code</span></span>                                                                          | <span data-ttu-id="cc006-115">Description</span><span class="sxs-lookup"><span data-stu-id="cc006-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="cc006-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="cc006-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="cc006-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="cc006-117">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="cc006-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cc006-118">Requirements</span></span>



| <span data-ttu-id="cc006-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cc006-119">Requirement</span></span> | <span data-ttu-id="cc006-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc006-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc006-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="cc006-121">Header</span></span><br/>  | <dl> <span data-ttu-id="cc006-122"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc006-122"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="cc006-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="cc006-123">Library</span></span><br/> | <dl> <span data-ttu-id="cc006-124"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cc006-124"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc006-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cc006-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc006-126">Ajout d’une ressource à un objet</span><span class="sxs-lookup"><span data-stu-id="cc006-126">Adding a Resource to an Object</span></span>](adding-a-resource-to-an-object.md)
</dt> <dt>

[<span data-ttu-id="cc006-127">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="cc006-127">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="cc006-128">**IPortableDeviceValues::GetUnsignedLargeIntegerValue**</span><span class="sxs-lookup"><span data-stu-id="cc006-128">**IPortableDeviceValues::GetUnsignedLargeIntegerValue**</span></span>](iportabledevicevalues-getunsignedlargeintegervalue.md)
</dt> </dl>

 

 




