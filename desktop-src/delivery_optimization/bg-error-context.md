---
title: Énumération BG_ERROR_CONTEXT (Deliveryoptimization. h)
description: L’énumération BG_ERROR_CONTEXT définit les valeurs constantes qui spécifient le contexte dans lequel l’erreur s’est produite.
ms.assetid: 86202343-5B5B-4A2E-A58D-7634BCB41E1C
keywords:
- Énumération BG_ERROR_CONTEXT
topic_type:
- apiref
api_name:
- BG_ERROR_CONTEXT
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cf6c68c20a5117e6cd8a02f8b4608b494c0ea93f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464947"
---
# <a name="bg_error_context-enumeration"></a><span data-ttu-id="8bddc-104">Énumération BG_ERROR_CONTEXT</span><span class="sxs-lookup"><span data-stu-id="8bddc-104">BG_ERROR_CONTEXT enumeration</span></span>

<span data-ttu-id="8bddc-105">L’énumération **BG_ERROR_CONTEXT** définit les valeurs constantes qui spécifient le contexte dans lequel l’erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="8bddc-105">The **BG_ERROR_CONTEXT** enumeration defines the constant values that specify the context in which the error occurred.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bddc-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8bddc-106">Syntax</span></span>


```C++
typedef enum  { 
  BG_ERROR_CONTEXT_NONE                        = 0,
  BG_ERROR_CONTEXT_UNKNOWN                     = 1,
  BG_ERROR_CONTEXT_GENERAL_QUEUE_MANAGER       = 2,
  BG_ERROR_CONTEXT_QUEUE_MANAGER_NOTIFICATION  = 3,
  BG_ERROR_CONTEXT_LOCAL_FILE                  = 4,
  BG_ERROR_CONTEXT_REMOTE_FILE                 = 5,
  BG_ERROR_CONTEXT_GENERAL_TRANSPORT           = 6,
  BG_ERROR_CONTEXT_REMOTE_APPLICATION          = 7
} BG_ERROR_CONTEXT;
```



## <a name="constants"></a><span data-ttu-id="8bddc-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="8bddc-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="8bddc-108"><span id="BG_ERROR_CONTEXT_NONE"></span><span id="bg_error_context_none"></span>**BG_ERROR_CONTEXT_NONE**</span><span class="sxs-lookup"><span data-stu-id="8bddc-108"><span id="BG_ERROR_CONTEXT_NONE"></span><span id="bg_error_context_none"></span>**BG_ERROR_CONTEXT_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="8bddc-109">Aucune erreur ne s’est produite.</span><span class="sxs-lookup"><span data-stu-id="8bddc-109">An error has not occurred.</span></span>

</dd> <dt>

<span data-ttu-id="8bddc-110"><span id="BG_ERROR_CONTEXT_UNKNOWN"></span><span id="bg_error_context_unknown"></span>**BG_ERROR_CONTEXT_UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="8bddc-110"><span id="BG_ERROR_CONTEXT_UNKNOWN"></span><span id="bg_error_context_unknown"></span>**BG_ERROR_CONTEXT_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="8bddc-111">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="8bddc-111">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="8bddc-112"><span id="BG_ERROR_CONTEXT_GENERAL_QUEUE_MANAGER"></span><span id="bg_error_context_general_queue_manager"></span>**BG_ERROR_CONTEXT_GENERAL_QUEUE_MANAGER**</span><span class="sxs-lookup"><span data-stu-id="8bddc-112"><span id="BG_ERROR_CONTEXT_GENERAL_QUEUE_MANAGER"></span><span id="bg_error_context_general_queue_manager"></span>**BG_ERROR_CONTEXT_GENERAL_QUEUE_MANAGER**</span></span>
</dt> <dd>

<span data-ttu-id="8bddc-113">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="8bddc-113">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="8bddc-114"><span id="BG_ERROR_CONTEXT_QUEUE_MANAGER_NOTIFICATION"></span><span id="bg_error_context_queue_manager_notification"></span>**BG_ERROR_CONTEXT_QUEUE_MANAGER_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="8bddc-114"><span id="BG_ERROR_CONTEXT_QUEUE_MANAGER_NOTIFICATION"></span><span id="bg_error_context_queue_manager_notification"></span>**BG_ERROR_CONTEXT_QUEUE_MANAGER_NOTIFICATION**</span></span>
</dt> <dd>

<span data-ttu-id="8bddc-115">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="8bddc-115">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="8bddc-116"><span id="BG_ERROR_CONTEXT_LOCAL_FILE"></span><span id="bg_error_context_local_file"></span>**BG_ERROR_CONTEXT_LOCAL_FILE**</span><span class="sxs-lookup"><span data-stu-id="8bddc-116"><span id="BG_ERROR_CONTEXT_LOCAL_FILE"></span><span id="bg_error_context_local_file"></span>**BG_ERROR_CONTEXT_LOCAL_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="8bddc-117">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="8bddc-117">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="8bddc-118"><span id="BG_ERROR_CONTEXT_REMOTE_FILE"></span><span id="bg_error_context_remote_file"></span>**BG_ERROR_CONTEXT_REMOTE_FILE**</span><span class="sxs-lookup"><span data-stu-id="8bddc-118"><span id="BG_ERROR_CONTEXT_REMOTE_FILE"></span><span id="bg_error_context_remote_file"></span>**BG_ERROR_CONTEXT_REMOTE_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="8bddc-119">L’erreur est liée au fichier distant spécifié.</span><span class="sxs-lookup"><span data-stu-id="8bddc-119">The error was related to the specified remote file.</span></span> <span data-ttu-id="8bddc-120">Par exemple, l’URL n’était pas accessible.</span><span class="sxs-lookup"><span data-stu-id="8bddc-120">For example, the URL was not accessible.</span></span>

</dd> <dt>

<span data-ttu-id="8bddc-121"><span id="BG_ERROR_CONTEXT_GENERAL_TRANSPORT"></span><span id="bg_error_context_general_transport"></span>**BG_ERROR_CONTEXT_GENERAL_TRANSPORT**</span><span class="sxs-lookup"><span data-stu-id="8bddc-121"><span id="BG_ERROR_CONTEXT_GENERAL_TRANSPORT"></span><span id="bg_error_context_general_transport"></span>**BG_ERROR_CONTEXT_GENERAL_TRANSPORT**</span></span>
</dt> <dd>

<span data-ttu-id="8bddc-122">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="8bddc-122">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="8bddc-123"><span id="BG_ERROR_CONTEXT_REMOTE_APPLICATION"></span><span id="bg_error_context_remote_application"></span>**BG_ERROR_CONTEXT_REMOTE_APPLICATION**</span><span class="sxs-lookup"><span data-stu-id="8bddc-123"><span id="BG_ERROR_CONTEXT_REMOTE_APPLICATION"></span><span id="bg_error_context_remote_application"></span>**BG_ERROR_CONTEXT_REMOTE_APPLICATION**</span></span>
</dt> <dd>

<span data-ttu-id="8bddc-124">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="8bddc-124">Not supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8bddc-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8bddc-125">Requirements</span></span>



| <span data-ttu-id="8bddc-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8bddc-126">Requirement</span></span> | <span data-ttu-id="8bddc-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="8bddc-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8bddc-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8bddc-128">Minimum supported client</span></span><br/> | <span data-ttu-id="8bddc-129">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8bddc-129">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="8bddc-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8bddc-130">Minimum supported server</span></span><br/> | <span data-ttu-id="8bddc-131">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8bddc-131">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8bddc-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="8bddc-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="8bddc-133"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="8bddc-133"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8bddc-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8bddc-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bddc-135">**IBackgroundCopyError::GetError**</span><span class="sxs-lookup"><span data-stu-id="8bddc-135">**IBackgroundCopyError::GetError**</span></span>](ibackgroundcopyerror-geterror-method.md)
</dt> </dl>

 

 





