---
description: La \_ notification SPFILENOTIFY ENDSUBQUEUE est envoyée à la fonction de rappel lorsque la file d’attente effectue toutes les opérations dans la sous-file d’attente de suppression, de renommage ou de copie.
ms.assetid: 76bd027a-0f00-46e3-b502-0c97827308a8
title: Message d’SPFILENOTIFY_ENDSUBQUEUE (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7eadc7546487b308313b7cb31088a22420e27af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042766"
---
# <a name="spfilenotify_endsubqueue-message"></a><span data-ttu-id="d987d-103">\_Message SPFILENOTIFY ENDSUBQUEUE</span><span class="sxs-lookup"><span data-stu-id="d987d-103">SPFILENOTIFY\_ENDSUBQUEUE message</span></span>

<span data-ttu-id="d987d-104">La notification **SPFILENOTIFY \_ ENDSUBQUEUE** est envoyée à la fonction de rappel lorsque la file d’attente effectue toutes les opérations dans la sous-file d’attente de suppression, de renommage ou de copie.</span><span class="sxs-lookup"><span data-stu-id="d987d-104">The **SPFILENOTIFY\_ENDSUBQUEUE** notification is sent to the callback function when the queue completes all the operations in the delete, rename, or copy subqueue.</span></span>


```C++
SPFILENOTIFY_ENDSUBQUEUE
  Param1 = (UINT) SubQueue;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="d987d-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d987d-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d987d-106">*Param1*</span><span class="sxs-lookup"><span data-stu-id="d987d-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="d987d-107">Sous-file d’attente qui s’est terminée.</span><span class="sxs-lookup"><span data-stu-id="d987d-107">Subqueue that has been completed.</span></span> <span data-ttu-id="d987d-108">Ce paramètre peut prendre l’une des valeurs suivantes FILEOP \_ Delete, FILEOP \_ Rename ou FILEOP \_ Copy.</span><span class="sxs-lookup"><span data-stu-id="d987d-108">This parameter can be one of the following values FILEOP\_DELETE, FILEOP\_RENAME, or FILEOP\_COPY.</span></span>

</dd> <dt>

<span data-ttu-id="d987d-109">*Param2*</span><span class="sxs-lookup"><span data-stu-id="d987d-109">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="d987d-110">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="d987d-110">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d987d-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d987d-111">Return value</span></span>

<span data-ttu-id="d987d-112">La valeur de retour est ignorée.</span><span class="sxs-lookup"><span data-stu-id="d987d-112">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="d987d-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d987d-113">Requirements</span></span>



| <span data-ttu-id="d987d-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d987d-114">Requirement</span></span> | <span data-ttu-id="d987d-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="d987d-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d987d-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d987d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d987d-117">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d987d-117">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d987d-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d987d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d987d-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d987d-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d987d-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="d987d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d987d-121"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d987d-121"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d987d-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d987d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d987d-123">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="d987d-123">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="d987d-124">Notifications</span><span class="sxs-lookup"><span data-stu-id="d987d-124">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="d987d-125">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="d987d-125">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="d987d-126">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="d987d-126">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

 




