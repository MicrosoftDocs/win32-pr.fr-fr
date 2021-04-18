---
description: La méthode GetCount récupère le nombre de clés de cette collection.
ms.assetid: 963f514e-3e0f-4334-ac29-6de7cc8aa336
title: 'IPortableDeviceKeyCollection :: GetCount, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceKeyCollection.GetCount
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: e867a171039a97cc0f83198f72eecaeb57ad3c16
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543308"
---
# <a name="iportabledevicekeycollectiongetcount-method"></a><span data-ttu-id="4023e-103">IPortableDeviceKeyCollection :: GetCount, méthode</span><span class="sxs-lookup"><span data-stu-id="4023e-103">IPortableDeviceKeyCollection::GetCount method</span></span>

<span data-ttu-id="4023e-104">La méthode **GetCount** récupère le nombre de clés de cette collection.</span><span class="sxs-lookup"><span data-stu-id="4023e-104">The **GetCount** method retrieves the number of keys in this collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="4023e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4023e-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [in] DWORD *pcElems
);
```



## <a name="parameters"></a><span data-ttu-id="4023e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4023e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4023e-107">*pcElems* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4023e-107">*pcElems* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4023e-108">Pointeur vers une **valeur DWORD** qui contient le nombre de clés dans la collection.</span><span class="sxs-lookup"><span data-stu-id="4023e-108">Pointer to a **DWORD** that contains the number of keys in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4023e-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4023e-109">Return value</span></span>

<span data-ttu-id="4023e-110">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="4023e-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="4023e-111">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="4023e-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="4023e-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="4023e-112">Return code</span></span>                                                                               | <span data-ttu-id="4023e-113">Description</span><span class="sxs-lookup"><span data-stu-id="4023e-113">Description</span></span>                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="4023e-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4023e-114"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="4023e-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="4023e-115">The method succeeded.</span></span><br/>                     |
| <dl> <span data-ttu-id="4023e-116"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="4023e-116"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="4023e-117">Un argument de pointeur obligatoire était **null**.</span><span class="sxs-lookup"><span data-stu-id="4023e-117">A required pointer argument was **NULL**.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="4023e-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="4023e-118">Examples</span></span>

<span data-ttu-id="4023e-119">Pour obtenir un exemple d’utilisation de cette méthode, consultez [récupération des événements de service pris en charge](retrieving-supported-events.md).</span><span class="sxs-lookup"><span data-stu-id="4023e-119">For an example of how to use this method, see [Retrieving Supported Service Events](retrieving-supported-events.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4023e-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4023e-120">Requirements</span></span>



| <span data-ttu-id="4023e-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4023e-121">Requirement</span></span> | <span data-ttu-id="4023e-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="4023e-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4023e-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="4023e-123">Header</span></span><br/>  | <dl> <span data-ttu-id="4023e-124"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="4023e-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="4023e-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4023e-125">Library</span></span><br/> | <dl> <span data-ttu-id="4023e-126"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4023e-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4023e-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4023e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4023e-128">**Interface IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="4023e-128">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="4023e-129">Récupération des événements de service pris en charge</span><span class="sxs-lookup"><span data-stu-id="4023e-129">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="4023e-130">Récupération des méthodes de service prises en charge</span><span class="sxs-lookup"><span data-stu-id="4023e-130">Retrieving Supported Service Methods</span></span>](retrieving-supported-methods.md)
</dt> </dl>

 

 




