---
description: La méthode GetAt récupère un PROPERTYKEY de la collection par index.
ms.assetid: 9a3c5c28-39b4-4d53-a8d7-0f5a0d4d89ad
title: 'IPortableDeviceKeyCollection :: GetAt, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceKeyCollection.GetAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: b75285f6dcdb0961312fa1db8f5c912b771bd786
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106522811"
---
# <a name="iportabledevicekeycollectiongetat-method"></a><span data-ttu-id="35217-103">IPortableDeviceKeyCollection :: GetAt, méthode</span><span class="sxs-lookup"><span data-stu-id="35217-103">IPortableDeviceKeyCollection::GetAt method</span></span>

<span data-ttu-id="35217-104">La méthode **GetAt** récupère un **PROPERTYKEY** de la collection par index.</span><span class="sxs-lookup"><span data-stu-id="35217-104">The **GetAt** method retrieves a **PROPERTYKEY** from the collection by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="35217-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="35217-105">Syntax</span></span>


```C++
HRESULT GetAt(
  [in]  const DWORD       dwIndex,
  [out]       PROPERTYKEY *pKey
);
```



## <a name="parameters"></a><span data-ttu-id="35217-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="35217-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35217-107">*dwIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="35217-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35217-108">**Valeur DWORD** qui contient l’index de la clé à récupérer.</span><span class="sxs-lookup"><span data-stu-id="35217-108">**DWORD** that contains the index of the key to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="35217-109">A-la  \[ à\]</span><span class="sxs-lookup"><span data-stu-id="35217-109">*pKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="35217-110">Pointeur vers un objet **PROPERTYKEY** .</span><span class="sxs-lookup"><span data-stu-id="35217-110">Pointer to a **PROPERTYKEY** object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35217-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="35217-111">Return value</span></span>

<span data-ttu-id="35217-112">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="35217-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="35217-113">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="35217-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="35217-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="35217-114">Return code</span></span>                                                                                  | <span data-ttu-id="35217-115">Description</span><span class="sxs-lookup"><span data-stu-id="35217-115">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="35217-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="35217-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="35217-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="35217-117">The method succeeded.</span></span><br/>                     |
| <dl> <span data-ttu-id="35217-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="35217-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="35217-119">L’index passé est hors limites.</span><span class="sxs-lookup"><span data-stu-id="35217-119">The index passed in was out of range.</span></span><br/>     |
| <dl> <span data-ttu-id="35217-120"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="35217-120"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="35217-121">Un argument de pointeur obligatoire était **null**.</span><span class="sxs-lookup"><span data-stu-id="35217-121">A required pointer argument was **NULL**.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="35217-122">Exemples</span><span class="sxs-lookup"><span data-stu-id="35217-122">Examples</span></span>

<span data-ttu-id="35217-123">Pour obtenir un exemple d’utilisation de cette méthode, consultez [récupération des événements de service pris en charge](retrieving-supported-events.md).</span><span class="sxs-lookup"><span data-stu-id="35217-123">For an example of how to use this method, see [Retrieving Supported Service Events](retrieving-supported-events.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="35217-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="35217-124">Requirements</span></span>



| <span data-ttu-id="35217-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="35217-125">Requirement</span></span> | <span data-ttu-id="35217-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="35217-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35217-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="35217-127">Header</span></span><br/>  | <dl> <span data-ttu-id="35217-128"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="35217-128"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="35217-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="35217-129">Library</span></span><br/> | <dl> <span data-ttu-id="35217-130"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="35217-130"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35217-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="35217-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35217-132">**Interface IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="35217-132">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="35217-133">Récupération des événements de service pris en charge</span><span class="sxs-lookup"><span data-stu-id="35217-133">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="35217-134">Récupération des méthodes de service prises en charge</span><span class="sxs-lookup"><span data-stu-id="35217-134">Retrieving Supported Service Methods</span></span>](retrieving-supported-methods.md)
</dt> </dl>

 

 




