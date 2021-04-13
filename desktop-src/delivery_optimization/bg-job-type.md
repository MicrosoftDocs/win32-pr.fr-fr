---
title: Énumération BG_JOB_TYPE (Deliveryoptimization. h)
description: L’énumération BG_JOB_TYPE définit des valeurs constantes qui spécifient le type de tâche de transfert, par exemple télécharger.
ms.assetid: 696A43C3-1FA2-436D-B34A-3544E7C9A66A
keywords:
- Énumération BG_JOB_TYPE
topic_type:
- apiref
api_name:
- BG_JOB_TYPE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f1f672bcf2d2538bfaa9b9573fa1dfa71ee7b9cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464946"
---
# <a name="bg_job_type-enumeration"></a><span data-ttu-id="4cf5f-104">Énumération BG_JOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="4cf5f-104">BG_JOB_TYPE enumeration</span></span>

<span data-ttu-id="4cf5f-105">L’énumération **BG_JOB_TYPE** définit des valeurs constantes qui spécifient le type de tâche de transfert, par exemple télécharger.</span><span class="sxs-lookup"><span data-stu-id="4cf5f-105">The **BG_JOB_TYPE** enumeration defines constant values that specify the type of transfer job, such as download.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cf5f-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4cf5f-106">Syntax</span></span>


```C++
typedef enum  { 
  BG_JOB_TYPE_DOWNLOAD
} BG_JOB_TYPE;
```



## <a name="constants"></a><span data-ttu-id="4cf5f-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="4cf5f-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="4cf5f-108"><span id="BG_JOB_TYPE_DOWNLOAD"></span><span id="bg_job_type_download"></span>**BG_JOB_TYPE_DOWNLOAD**</span><span class="sxs-lookup"><span data-stu-id="4cf5f-108"><span id="BG_JOB_TYPE_DOWNLOAD"></span><span id="bg_job_type_download"></span>**BG_JOB_TYPE_DOWNLOAD**</span></span>
</dt> <dd>

<span data-ttu-id="4cf5f-109">Spécifie que le travail télécharge des fichiers sur le client.</span><span class="sxs-lookup"><span data-stu-id="4cf5f-109">Specifies that the job downloads files to the client.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4cf5f-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4cf5f-110">Requirements</span></span>



| <span data-ttu-id="4cf5f-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4cf5f-111">Requirement</span></span> | <span data-ttu-id="4cf5f-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="4cf5f-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cf5f-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4cf5f-113">Minimum supported client</span></span><br/> | <span data-ttu-id="4cf5f-114">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4cf5f-114">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="4cf5f-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4cf5f-115">Minimum supported server</span></span><br/> | <span data-ttu-id="4cf5f-116">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4cf5f-116">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4cf5f-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="4cf5f-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="4cf5f-118"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="4cf5f-118"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cf5f-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4cf5f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cf5f-120">**Méthode ibackgroundcopyjob :: GetType**</span><span class="sxs-lookup"><span data-stu-id="4cf5f-120">**IBackgroundCopyJob::GetType**</span></span>](ibackgroundcopyjob-gettype.md)
</dt> <dt>

[<span data-ttu-id="4cf5f-121">**IBackgroundCopyManager :: CreateJob**</span><span class="sxs-lookup"><span data-stu-id="4cf5f-121">**IBackgroundCopyManager::CreateJob**</span></span>](ibackgroundcopymanager-createjob.md)
</dt> </dl>

 

 





