---
description: La \_ structure Job info \_ 3 permet de lier un ensemble de travaux d’impression.
ms.assetid: a110f555-dc33-450c-ae77-ea26f0f69448
title: Structure JOB_INFO_3 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JOB_INFO_3
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: c76cbb6c019878d9c392d21caa40c604df3a5f12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210466"
---
# <a name="job_info_3-structure"></a><span data-ttu-id="f3096-103">\_Structure des informations sur le travail \_ 3</span><span class="sxs-lookup"><span data-stu-id="f3096-103">JOB\_INFO\_3 structure</span></span>

<span data-ttu-id="f3096-104">La structure **Job \_ info \_ 3** permet de lier un ensemble de travaux d’impression.</span><span class="sxs-lookup"><span data-stu-id="f3096-104">The **JOB\_INFO\_3** structure is used to link together a set of print jobs.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3096-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f3096-105">Syntax</span></span>


```C++
typedef struct _JOB_INFO_3 {
  DWORD JobId;
  DWORD NextJobId;
  DWORD Reserved;
} JOB_INFO_3, *PJOB_INFO_3;
```



## <a name="members"></a><span data-ttu-id="f3096-106">Membres</span><span class="sxs-lookup"><span data-stu-id="f3096-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f3096-107">**JobId**</span><span class="sxs-lookup"><span data-stu-id="f3096-107">**JobId**</span></span>
</dt> <dd>

<span data-ttu-id="f3096-108">Identificateur du travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="f3096-108">The print job identifier.</span></span>

</dd> <dt>

<span data-ttu-id="f3096-109">**NextJobId**</span><span class="sxs-lookup"><span data-stu-id="f3096-109">**NextJobId**</span></span>
</dt> <dd>

<span data-ttu-id="f3096-110">Identificateur du travail d’impression pour le travail d’impression suivant dans l’ensemble lié de travaux d’impression.</span><span class="sxs-lookup"><span data-stu-id="f3096-110">The print job identifier for the next print job in the linked set of print jobs.</span></span>

</dd> <dt>

<span data-ttu-id="f3096-111">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="f3096-111">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="f3096-112">Cette valeur est réservée à une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="f3096-112">This value is reserved for future use.</span></span> <span data-ttu-id="f3096-113">Vous devez la définir sur zéro.</span><span class="sxs-lookup"><span data-stu-id="f3096-113">You must set it to zero.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f3096-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f3096-114">Requirements</span></span>



| <span data-ttu-id="f3096-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f3096-115">Requirement</span></span> | <span data-ttu-id="f3096-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3096-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3096-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f3096-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f3096-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f3096-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f3096-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f3096-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f3096-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f3096-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f3096-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="f3096-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3096-122"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f3096-122"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3096-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f3096-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3096-124">Impression</span><span class="sxs-lookup"><span data-stu-id="f3096-124">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="f3096-125">Structures de l’API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="f3096-125">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="f3096-126">**EnumJobs**</span><span class="sxs-lookup"><span data-stu-id="f3096-126">**EnumJobs**</span></span>](enumjobs.md)
</dt> <dt>

[<span data-ttu-id="f3096-127">**GetJob**</span><span class="sxs-lookup"><span data-stu-id="f3096-127">**GetJob**</span></span>](getjob.md)
</dt> <dt>

[<span data-ttu-id="f3096-128">**SetJob**</span><span class="sxs-lookup"><span data-stu-id="f3096-128">**SetJob**</span></span>](setjob.md)
</dt> </dl>

 

 




