---
title: Structure BG_JOB_TIMES (Deliveryoptimization. h)
description: La structure BG_JOB_TIMES fournit des horodatages liés aux travaux.
ms.assetid: 0147478F-C850-4B66-AB15-042C1A81D6B5
keywords:
- Structure BG_JOB_TIMES
topic_type:
- apiref
api_name:
- BG_JOB_TIMES
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0a2d4e56bb616254537e26fc1ba0fdf5b9e251a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740324"
---
# <a name="bg_job_times-structure"></a><span data-ttu-id="7e787-104">Structure BG_JOB_TIMES</span><span class="sxs-lookup"><span data-stu-id="7e787-104">BG_JOB_TIMES structure</span></span>

<span data-ttu-id="7e787-105">La structure **BG_JOB_TIMES** fournit des horodatages liés aux travaux.</span><span class="sxs-lookup"><span data-stu-id="7e787-105">The **BG_JOB_TIMES** structure provides job-related time stamps.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e787-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7e787-106">Syntax</span></span>


```C++
typedef struct _BG_JOB_TIMES {
  FILETIME CreationTime;
  FILETIME ModificationTime;
  FILETIME TransferCompletionTime;
} BG_JOB_TIMES;
```



## <a name="members"></a><span data-ttu-id="7e787-107">Membres</span><span class="sxs-lookup"><span data-stu-id="7e787-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="7e787-108">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="7e787-108">**CreationTime**</span></span>
</dt> <dd>

<span data-ttu-id="7e787-109">Heure de création du travail.</span><span class="sxs-lookup"><span data-stu-id="7e787-109">Time the job was created.</span></span> <span data-ttu-id="7e787-110">L’heure est spécifiée en tant que [fileTime](/windows/win32/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="7e787-110">The time is specified as [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="7e787-111">**ModificationTime**</span><span class="sxs-lookup"><span data-stu-id="7e787-111">**ModificationTime**</span></span>
</dt> <dd>

<span data-ttu-id="7e787-112">Heure de la dernière modification du travail ou du transfert d’octets.</span><span class="sxs-lookup"><span data-stu-id="7e787-112">Time the job was last modified or bytes were transferred.</span></span> <span data-ttu-id="7e787-113">L’ajout de fichiers ou l’appel de l’une des méthodes Set dans les interfaces [ \* *méthode ibackgroundcopyjob \** _](/previous-versions//mt811348(v=vs.85)) modifie cette valeur.</span><span class="sxs-lookup"><span data-stu-id="7e787-113">Adding files or calling any of the set methods in the [\**IBackgroundCopyJob\** _](/previous-versions//mt811348(v=vs.85)) interfaces changes this value.</span></span> <span data-ttu-id="7e787-114">En outre, les modifications apportées à l’état du travail et l’appel des méthodes [_ *suspend* \*](ibackgroundcopyjob-suspend.md), [**Resume**](ibackgroundcopyjob-resume.md), [**Cancel**](ibackgroundcopyjob-cancel.md)et [**complet**](ibackgroundcopyjob-complete.md) modifient cette valeur.</span><span class="sxs-lookup"><span data-stu-id="7e787-114">In addition, changes to the state of the job and calling the [_ *Suspend*\*](ibackgroundcopyjob-suspend.md), [**Resume**](ibackgroundcopyjob-resume.md), [**Cancel**](ibackgroundcopyjob-cancel.md), and [**Complete**](ibackgroundcopyjob-complete.md) methods change this value.</span></span> <span data-ttu-id="7e787-115">L’heure est spécifiée en tant que [fileTime](/windows/win32/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="7e787-115">The time is specified as [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="7e787-116">**TransferCompletionTime**</span><span class="sxs-lookup"><span data-stu-id="7e787-116">**TransferCompletionTime**</span></span>
</dt> <dd>

<span data-ttu-id="7e787-117">Heure à laquelle le travail est passé à l’État BG_JOB_STATE_TRANSFERRED.</span><span class="sxs-lookup"><span data-stu-id="7e787-117">Time the job entered the BG_JOB_STATE_TRANSFERRED state.</span></span> <span data-ttu-id="7e787-118">L’heure est spécifiée en tant que [fileTime](/windows/win32/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="7e787-118">The time is specified as [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7e787-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7e787-119">Requirements</span></span>



| <span data-ttu-id="7e787-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7e787-120">Requirement</span></span> | <span data-ttu-id="7e787-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="7e787-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e787-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7e787-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7e787-123">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7e787-123">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="7e787-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7e787-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7e787-125">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7e787-125">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="7e787-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="7e787-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e787-127"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e787-127"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e787-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7e787-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e787-129">**Méthode ibackgroundcopyjob :: GetTimes**</span><span class="sxs-lookup"><span data-stu-id="7e787-129">**IBackgroundCopyJob::GetTimes**</span></span>](ibackgroundcopyjob-gettimes.md)
</dt> </dl>

 

