---
description: La \_ notification SPFILENOTIFY ENDQUEUE est envoyée à la routine de rappel lorsque toutes les opérations de mise en file d’attente ont été effectuées.
ms.assetid: f4540ab6-edea-4f84-b7eb-4ab3f774068b
title: Message d’SPFILENOTIFY_ENDQUEUE (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f3ed2ca896f91ec09cb49f89731b41c5d099465
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952995"
---
# <a name="spfilenotify_endqueue-message"></a><span data-ttu-id="98685-103">\_Message SPFILENOTIFY ENDQUEUE</span><span class="sxs-lookup"><span data-stu-id="98685-103">SPFILENOTIFY\_ENDQUEUE message</span></span>

<span data-ttu-id="98685-104">La notification **SPFILENOTIFY \_ ENDQUEUE** est envoyée à la routine de rappel lorsque toutes les opérations de mise en file d’attente ont été effectuées.</span><span class="sxs-lookup"><span data-stu-id="98685-104">The **SPFILENOTIFY\_ENDQUEUE** notification is sent to the callback routine when all of the queued operations have been completed.</span></span>


```C++
SPFILENOTIFY_ENDQUEUE
  Param1 = (UINT) Result;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="98685-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="98685-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98685-106">*Param1*</span><span class="sxs-lookup"><span data-stu-id="98685-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="98685-107">**True** si la file d’attente a été traitée avec succès ; sinon, **false** .</span><span class="sxs-lookup"><span data-stu-id="98685-107">**TRUE** if the queue was processed successfully, **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="98685-108">*Param2*</span><span class="sxs-lookup"><span data-stu-id="98685-108">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="98685-109">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="98685-109">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98685-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="98685-110">Return value</span></span>

<span data-ttu-id="98685-111">La valeur de retour est ignorée.</span><span class="sxs-lookup"><span data-stu-id="98685-111">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="98685-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="98685-112">Requirements</span></span>



| <span data-ttu-id="98685-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="98685-113">Requirement</span></span> | <span data-ttu-id="98685-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="98685-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="98685-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="98685-115">Minimum supported client</span></span><br/> | <span data-ttu-id="98685-116">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="98685-116">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="98685-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="98685-117">Minimum supported server</span></span><br/> | <span data-ttu-id="98685-118">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="98685-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="98685-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="98685-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="98685-120"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="98685-120"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98685-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="98685-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98685-122">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="98685-122">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="98685-123">Notifications</span><span class="sxs-lookup"><span data-stu-id="98685-123">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="98685-124">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="98685-124">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="98685-125">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="98685-125">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

 




