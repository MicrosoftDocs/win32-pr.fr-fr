---
description: La \_ notification SPFILENOTIFY ENDCOPY est passée à la fonction de rappel lorsque la file d’attente termine une opération de copie. Cette notification est envoyée même si l’utilisateur annule ou si une erreur se produit.
ms.assetid: d58dc397-8803-466c-9069-728faf2c2030
title: Message d’SPFILENOTIFY_ENDCOPY (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75dba56c4a38ac87003a3b59b594135e55a462f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106533698"
---
# <a name="spfilenotify_endcopy-message"></a><span data-ttu-id="96ed8-104">\_Message SPFILENOTIFY ENDCOPY</span><span class="sxs-lookup"><span data-stu-id="96ed8-104">SPFILENOTIFY\_ENDCOPY message</span></span>

<span data-ttu-id="96ed8-105">La notification **SPFILENOTIFY \_ ENDCOPY** est passée à la fonction de rappel lorsque la file d’attente termine une opération de copie.</span><span class="sxs-lookup"><span data-stu-id="96ed8-105">The **SPFILENOTIFY\_ENDCOPY** notification is passed to the callback function when the queue completes a copy operation.</span></span> <span data-ttu-id="96ed8-106">Cette notification est envoyée même si l’utilisateur annule ou si une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="96ed8-106">This notification is sent even if the user cancels or if an error occurs.</span></span>


```C++
SPFILENOTIFY_ENDCOPY
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="96ed8-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="96ed8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96ed8-108">*Param1*</span><span class="sxs-lookup"><span data-stu-id="96ed8-108">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="96ed8-109">Pointeur vers une structure [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) .</span><span class="sxs-lookup"><span data-stu-id="96ed8-109">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span> <span data-ttu-id="96ed8-110">Le membre **Win32Error** de la structure **FILEPATHS** indique le résultat de l’opération de copie.</span><span class="sxs-lookup"><span data-stu-id="96ed8-110">The **Win32Error** member of the **FILEPATHS** structure indicates the outcome of the copy operation.</span></span>

</dd> <dt>

<span data-ttu-id="96ed8-111">*Param2*</span><span class="sxs-lookup"><span data-stu-id="96ed8-111">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="96ed8-112">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="96ed8-112">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96ed8-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="96ed8-113">Return value</span></span>

<span data-ttu-id="96ed8-114">Le code de retour est ignoré.</span><span class="sxs-lookup"><span data-stu-id="96ed8-114">The return code is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="96ed8-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="96ed8-115">Requirements</span></span>



| <span data-ttu-id="96ed8-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="96ed8-116">Requirement</span></span> | <span data-ttu-id="96ed8-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="96ed8-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="96ed8-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="96ed8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="96ed8-119">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="96ed8-119">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="96ed8-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="96ed8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="96ed8-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="96ed8-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="96ed8-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="96ed8-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="96ed8-123"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="96ed8-123"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96ed8-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="96ed8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96ed8-125">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="96ed8-125">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="96ed8-126">Notifications</span><span class="sxs-lookup"><span data-stu-id="96ed8-126">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="96ed8-127">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="96ed8-127">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="96ed8-128">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="96ed8-128">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="96ed8-129">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="96ed8-129">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

 




