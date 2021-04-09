---
title: Énumération BITS_JOB_TRANSFER_POLICY (Deliveryoptimization. h)
description: L’énumération BITS_JOB_TRANSFER_POLICY définit les valeurs d’ID correspondant aux propriétés DO.
ms.assetid: 4811ADBF-F097-4340-BFF2-52CC9556ACF6
keywords:
- Énumération BITS_JOB_TRANSFER_POLICY
- Énumération BITS_JOB_TRANSFER_POLICY
topic_type:
- apiref
api_name:
- BITS_JOB_TRANSFER_POLICY
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 455752375b76e574923ccdd96d1d05fc9142c16c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103244"
---
# <a name="bits_job_transfer_policy-enumeration"></a><span data-ttu-id="8e940-105">Énumération BITS_JOB_TRANSFER_POLICY</span><span class="sxs-lookup"><span data-stu-id="8e940-105">BITS_JOB_TRANSFER_POLICY enumeration</span></span>

<span data-ttu-id="8e940-106">L’énumération **BITS_JOB_TRANSFER_POLICY** définit les valeurs d’ID correspondant aux propriétés do.</span><span class="sxs-lookup"><span data-stu-id="8e940-106">The **BITS_JOB_TRANSFER_POLICY** enumeration defines ID values corresponding to DO properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e940-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8e940-107">Syntax</span></span>


```C++
typedef enum _BITS_JOB_TRANSFER_POLICY { 
  BITS_JOB_TRANSFER_POLICY_ALWAYS        = 0x800000ff,
  BITS_JOB_TRANSFER_POLICY_NOT_ROAMING   = 0x8000007f,
  BITS_JOB_TRANSFER_POLICY_NO_SURCHARGE  = 0x8000006f,
  BITS_JOB_TRANSFER_POLICY_STANDARD      = 0x80000067,
  BITS_JOB_TRANSFER_POLICY_UNRESTRICTED  = 0x80000021
} BITS_JOB_TRANSFER_POLICY;
```



## <a name="constants"></a><span data-ttu-id="8e940-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="8e940-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="8e940-109"><span id="BITS_JOB_TRANSFER_POLICY_ALWAYS"></span><span id="bits_job_transfer_policy_always"></span>**BITS_JOB_TRANSFER_POLICY_ALWAYS**</span><span class="sxs-lookup"><span data-stu-id="8e940-109"><span id="BITS_JOB_TRANSFER_POLICY_ALWAYS"></span><span id="bits_job_transfer_policy_always"></span>**BITS_JOB_TRANSFER_POLICY_ALWAYS**</span></span>
</dt> <dd>

<span data-ttu-id="8e940-110">Spécifie que le travail sera transféré lorsque la connectivité sera disponible, quel que soit le coût.</span><span class="sxs-lookup"><span data-stu-id="8e940-110">Specifies that the job will be transferred when connectivity is available, regardless of the cost.</span></span>

</dd> <dt>

<span data-ttu-id="8e940-111"><span id="BITS_JOB_TRANSFER_POLICY_NOT_ROAMING"></span><span id="bits_job_transfer_policy_not_roaming"></span>**BITS_JOB_TRANSFER_POLICY_NOT_ROAMING**</span><span class="sxs-lookup"><span data-stu-id="8e940-111"><span id="BITS_JOB_TRANSFER_POLICY_NOT_ROAMING"></span><span id="bits_job_transfer_policy_not_roaming"></span>**BITS_JOB_TRANSFER_POLICY_NOT_ROAMING**</span></span>
</dt> <dd>

<span data-ttu-id="8e940-112">Spécifie que le travail sera transféré lorsque la connectivité sera disponible, à moins que cette connectivité soit soumise à des surcharges d’itinérance.</span><span class="sxs-lookup"><span data-stu-id="8e940-112">Specifies that the job will be transferred when connectivity is available, unless that connectivity is subject to roaming surcharges.</span></span>

</dd> <dt>

<span data-ttu-id="8e940-113"><span id="BITS_JOB_TRANSFER_POLICY_NO_SURCHARGE"></span><span id="bits_job_transfer_policy_no_surcharge"></span>**BITS_JOB_TRANSFER_POLICY_NO_SURCHARGE**</span><span class="sxs-lookup"><span data-stu-id="8e940-113"><span id="BITS_JOB_TRANSFER_POLICY_NO_SURCHARGE"></span><span id="bits_job_transfer_policy_no_surcharge"></span>**BITS_JOB_TRANSFER_POLICY_NO_SURCHARGE**</span></span>
</dt> <dd>

<span data-ttu-id="8e940-114">Spécifie que le travail sera transféré uniquement lorsque la connectivité est disponible, ce qui n’est pas soumis à une surcharge.</span><span class="sxs-lookup"><span data-stu-id="8e940-114">Specifies that the job will be transferred only when connectivity is available which is not subject to a surcharge.</span></span>

</dd> <dt>

<span data-ttu-id="8e940-115"><span id="BITS_JOB_TRANSFER_POLICY_STANDARD"></span><span id="bits_job_transfer_policy_standard"></span>**BITS_JOB_TRANSFER_POLICY_STANDARD**</span><span class="sxs-lookup"><span data-stu-id="8e940-115"><span id="BITS_JOB_TRANSFER_POLICY_STANDARD"></span><span id="bits_job_transfer_policy_standard"></span>**BITS_JOB_TRANSFER_POLICY_STANDARD**</span></span>
</dt> <dd>

<span data-ttu-id="8e940-116">Spécifie que le travail sera transféré uniquement lorsque la connectivité est disponible, ce qui n’est pas soumis à une surcharge ou à une épuisement proche.</span><span class="sxs-lookup"><span data-stu-id="8e940-116">Specifies that the job will be transferred only when connectivity is available which is neither subject to a surcharge nor near exhaustion.</span></span>

</dd> <dt>

<span data-ttu-id="8e940-117"><span id="BITS_JOB_TRANSFER_POLICY_UNRESTRICTED"></span><span id="bits_job_transfer_policy_unrestricted"></span>**BITS_JOB_TRANSFER_POLICY_UNRESTRICTED**</span><span class="sxs-lookup"><span data-stu-id="8e940-117"><span id="BITS_JOB_TRANSFER_POLICY_UNRESTRICTED"></span><span id="bits_job_transfer_policy_unrestricted"></span>**BITS_JOB_TRANSFER_POLICY_UNRESTRICTED**</span></span>
</dt> <dd>

<span data-ttu-id="8e940-118">Spécifie que le travail sera transféré uniquement lorsque la connectivité est disponible, ce qui n’impose pas de coûts ou de limites de trafic.</span><span class="sxs-lookup"><span data-stu-id="8e940-118">Specifies that the job will be transferred only when connectivity is available which does not impose costs or traffic limits.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8e940-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8e940-119">Requirements</span></span>



| <span data-ttu-id="8e940-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8e940-120">Requirement</span></span> | <span data-ttu-id="8e940-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="8e940-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e940-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8e940-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8e940-123">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8e940-123">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="8e940-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8e940-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8e940-125">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8e940-125">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8e940-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="8e940-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e940-127"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e940-127"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



 

 





