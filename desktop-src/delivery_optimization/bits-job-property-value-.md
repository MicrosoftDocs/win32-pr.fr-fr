---
title: Structure BITS_JOB_PROPERTY_VALUE (Deliveryoptimization. h)
description: L’BITS_JOB_PROPERTY_VALUE Union fournit la valeur de propriété du travail DO en fonction de la valeur de l’énumération BITS_JOB_PROPERTY_ID.
ms.assetid: C24D9EA1-2E72-4403-939A-7B01D7133FE7
keywords:
- Structure BITS_JOB_PROPERTY_VALUE
- Structure BITS_JOB_PROPERTY_VALUE
topic_type:
- apiref
api_name:
- BITS_JOB_PROPERTY_VALUE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c48c1fe550db51b6b838379d44df21c95fa95e41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103663"
---
# <a name="bits_job_property_value-structure"></a><span data-ttu-id="3baad-105">Structure BITS_JOB_PROPERTY_VALUE</span><span class="sxs-lookup"><span data-stu-id="3baad-105">BITS_JOB_PROPERTY_VALUE structure</span></span>

<span data-ttu-id="3baad-106">L' **BITS_JOB_PROPERTY_VALUE** Union fournit la valeur de propriété du travail do en fonction de la valeur de l’énumération [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) .</span><span class="sxs-lookup"><span data-stu-id="3baad-106">The **BITS_JOB_PROPERTY_VALUE** union provides the property value of the DO job based on the value of the [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="3baad-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3baad-107">Syntax</span></span>


```C++
typedef struct {
  DWORD          Dword;
  GUID           ClsID;
  BOOL           Enable;
  UINT64         Uint64;
  BG_AUTH_TARGET Target;
} BITS_JOB_PROPERTY_VALUE;
```



## <a name="members"></a><span data-ttu-id="3baad-108">Membres</span><span class="sxs-lookup"><span data-stu-id="3baad-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="3baad-109">**Grande**</span><span class="sxs-lookup"><span data-stu-id="3baad-109">**Dword**</span></span>
</dt> <dd>

<span data-ttu-id="3baad-110">Cette valeur est retournée en cas d’utilisation de l’ID de propriété d’énumération **BITS_JOB_PROPERTY_ID_COST_FLAGS** et est appliquée comme [stratégie de transfert](https://www.bing.com/search?q=transfer+policy) sur le travail do.</span><span class="sxs-lookup"><span data-stu-id="3baad-110">This value is returned when using the enum property ID **BITS_JOB_PROPERTY_ID_COST_FLAGS** and is applied as the [transfer policy](https://www.bing.com/search?q=transfer+policy) on the DO job.</span></span>

</dd> <dt>

<span data-ttu-id="3baad-111">**Identificateur**</span><span class="sxs-lookup"><span data-stu-id="3baad-111">**ClsID**</span></span>
</dt> <dd>

<span data-ttu-id="3baad-112">Cette valeur est retournée en cas d’utilisation de l’ID de propriété enum **BITS_JOB_PROPERTY_NOTIFICATION_CLSID** et représente le CLSID de l’objet de rappel à inscrire avec le travail do.</span><span class="sxs-lookup"><span data-stu-id="3baad-112">This value is returned when using the enum property ID **BITS_JOB_PROPERTY_NOTIFICATION_CLSID** and represents the CLSID of the callback object to register with the DO job.</span></span>

</dd> <dt>

<span data-ttu-id="3baad-113">**Activer**</span><span class="sxs-lookup"><span data-stu-id="3baad-113">**Enable**</span></span>
</dt> <dd>

<span data-ttu-id="3baad-114">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="3baad-114">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="3baad-115">**Uint64**</span><span class="sxs-lookup"><span data-stu-id="3baad-115">**Uint64**</span></span>
</dt> <dd>

<span data-ttu-id="3baad-116">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="3baad-116">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="3baad-117">**Cible**</span><span class="sxs-lookup"><span data-stu-id="3baad-117">**Target**</span></span>
</dt> <dd>

<span data-ttu-id="3baad-118">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="3baad-118">Not supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3baad-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3baad-119">Requirements</span></span>



| <span data-ttu-id="3baad-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3baad-120">Requirement</span></span> | <span data-ttu-id="3baad-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="3baad-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3baad-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3baad-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3baad-123">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3baad-123">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="3baad-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3baad-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3baad-125">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3baad-125">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3baad-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="3baad-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="3baad-127"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="3baad-127"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3baad-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3baad-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3baad-129">**BITS_JOB_PROPERTY_ID**</span><span class="sxs-lookup"><span data-stu-id="3baad-129">**BITS_JOB_PROPERTY_ID**</span></span>](bits-job-property-id.md)
</dt> <dt>

[<span data-ttu-id="3baad-130">**BITS_JOB_TRANSFER_POLICY**</span><span class="sxs-lookup"><span data-stu-id="3baad-130">**BITS_JOB_TRANSFER_POLICY**</span></span>](bits-job-transfer-policy-.md)
</dt> </dl>

 

 





