---
title: Énumération MP_PERSISTENCE_LIMIT_TYPE (MpClient. h)
description: Type de limite de persistance.
ms.assetid: 57423110-7966-4240-8B15-1859D3D9EA4C
keywords:
- MP_PERSISTENCE_LIMIT_TYPE énumération des fonctionnalités d’environnement Windows héritées
- PMP_PERSISTENCE_LIMIT_TYPE des fonctionnalités d’environnement Windows héritées d’un pointeur d’énumération
topic_type:
- apiref
api_name:
- MP_PERSISTENCE_LIMIT_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fb52bc6ee630590ca189b88c1fdde5a30e17747
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033172"
---
# <a name="mp_persistence_limit_type-enumeration"></a><span data-ttu-id="aed24-105">\_ \_ Énumération de type limite de persistance de point de gestion \_</span><span class="sxs-lookup"><span data-stu-id="aed24-105">MP\_PERSISTENCE\_LIMIT\_TYPE enumeration</span></span>

<span data-ttu-id="aed24-106">Type de limite de persistance.</span><span class="sxs-lookup"><span data-stu-id="aed24-106">Persistence limit type.</span></span>

## <a name="syntax"></a><span data-ttu-id="aed24-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aed24-107">Syntax</span></span>


```C++
typedef enum tagMP_PERSISTENCE_LIMIT_TYPE { 
  MP_PERSISTENCE_UNKNOWN      = 0,
  MP_PERSISTENCE_NO_LIMIT     = 1,
  MP_PERSISTENCE_DURATION     = 2,
  MP_PERSISTENCE_VDM_VERSION  = 3,
  MP_PERSISTENCE_TIMESTAMP    = 4,
  MP_PERSISTENCE_FORCED       = 5
} MP_PERSISTENCE_LIMIT_TYPE, *PMP_PERSISTENCE_LIMIT_TYPE;
```



## <a name="constants"></a><span data-ttu-id="aed24-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="aed24-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="aed24-109"><span id="MP_PERSISTENCE_UNKNOWN"></span><span id="mp_persistence_unknown"></span>**persistance de point de gestion \_ \_ inconnue**</span><span class="sxs-lookup"><span data-stu-id="aed24-109"><span id="MP_PERSISTENCE_UNKNOWN"></span><span id="mp_persistence_unknown"></span>**MP\_PERSISTENCE\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="aed24-110">Inconnu.</span><span class="sxs-lookup"><span data-stu-id="aed24-110">Unknown.</span></span>

</dd> <dt>

<span data-ttu-id="aed24-111"><span id="MP_PERSISTENCE_NO_LIMIT"></span><span id="mp_persistence_no_limit"></span>**persistance de MP \_ \_ non \_ limitée**</span><span class="sxs-lookup"><span data-stu-id="aed24-111"><span id="MP_PERSISTENCE_NO_LIMIT"></span><span id="mp_persistence_no_limit"></span>**MP\_PERSISTENCE\_NO\_LIMIT**</span></span>
</dt> <dd>

<span data-ttu-id="aed24-112">Aucune limite.</span><span class="sxs-lookup"><span data-stu-id="aed24-112">No limit.</span></span>

</dd> <dt>

<span data-ttu-id="aed24-113"><span id="MP_PERSISTENCE_DURATION"></span><span id="mp_persistence_duration"></span>**durée de la \_ PERsistance du point de gestion \_**</span><span class="sxs-lookup"><span data-stu-id="aed24-113"><span id="MP_PERSISTENCE_DURATION"></span><span id="mp_persistence_duration"></span>**MP\_PERSISTENCE\_DURATION**</span></span>
</dt> <dd>

<span data-ttu-id="aed24-114">Durée.</span><span class="sxs-lookup"><span data-stu-id="aed24-114">Duration.</span></span>

</dd> <dt>

<span data-ttu-id="aed24-115"><span id="MP_PERSISTENCE_VDM_VERSION"></span><span id="mp_persistence_vdm_version"></span>**\_version de VDM de PERsistance de Pack d’e \_ \_**</span><span class="sxs-lookup"><span data-stu-id="aed24-115"><span id="MP_PERSISTENCE_VDM_VERSION"></span><span id="mp_persistence_vdm_version"></span>**MP\_PERSISTENCE\_VDM\_VERSION**</span></span>
</dt> <dd>

<span data-ttu-id="aed24-116">Version de VDM.</span><span class="sxs-lookup"><span data-stu-id="aed24-116">VDM version.</span></span>

</dd> <dt>

<span data-ttu-id="aed24-117"><span id="MP_PERSISTENCE_TIMESTAMP"></span><span id="mp_persistence_timestamp"></span>**horodateur de la \_ PERsistance de point de gestion \_**</span><span class="sxs-lookup"><span data-stu-id="aed24-117"><span id="MP_PERSISTENCE_TIMESTAMP"></span><span id="mp_persistence_timestamp"></span>**MP\_PERSISTENCE\_TIMESTAMP**</span></span>
</dt> <dd>

<span data-ttu-id="aed24-118">Timestamp.</span><span class="sxs-lookup"><span data-stu-id="aed24-118">Timestamp.</span></span>

</dd> <dt>

<span data-ttu-id="aed24-119"><span id="MP_PERSISTENCE_FORCED"></span><span id="mp_persistence_forced"></span>**persistance de point de gestion \_ \_ forcée**</span><span class="sxs-lookup"><span data-stu-id="aed24-119"><span id="MP_PERSISTENCE_FORCED"></span><span id="mp_persistence_forced"></span>**MP\_PERSISTENCE\_FORCED**</span></span>
</dt> <dd>

<span data-ttu-id="aed24-120">Obligation.</span><span class="sxs-lookup"><span data-stu-id="aed24-120">Forced.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="aed24-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aed24-121">Requirements</span></span>



| <span data-ttu-id="aed24-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aed24-122">Requirement</span></span> | <span data-ttu-id="aed24-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="aed24-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aed24-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aed24-124">Minimum supported client</span></span><br/> | <span data-ttu-id="aed24-125">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aed24-125">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="aed24-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aed24-126">Minimum supported server</span></span><br/> | <span data-ttu-id="aed24-127">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aed24-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="aed24-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="aed24-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="aed24-129"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="aed24-129"><dt>MpClient.h</dt></span></span> </dl> |



 

 





