---
description: La \_ notification SPFILENOTIFY ENDDELETE est retournée à la routine de rappel lorsqu’une file d’attente termine une opération de suppression. Cette notification est envoyée même si l’utilisateur annule ou si une erreur se produit.
ms.assetid: 78859854-8411-4c51-9c3c-628315cf1c41
title: Message d’SPFILENOTIFY_ENDDELETE (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4ee4762dc33f8b8ec16a6be273cb42f41aeafce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106532282"
---
# <a name="spfilenotify_enddelete-message"></a><span data-ttu-id="a5ef4-104">\_Message SPFILENOTIFY ENDDELETE</span><span class="sxs-lookup"><span data-stu-id="a5ef4-104">SPFILENOTIFY\_ENDDELETE message</span></span>

<span data-ttu-id="a5ef4-105">La notification **SPFILENOTIFY \_ ENDDELETE** est retournée à la routine de rappel lorsqu’une file d’attente termine une opération de suppression.</span><span class="sxs-lookup"><span data-stu-id="a5ef4-105">The **SPFILENOTIFY\_ENDDELETE** notification is returned to the callback routine when a queue completes a delete operation.</span></span> <span data-ttu-id="a5ef4-106">Cette notification est envoyée même si l’utilisateur annule ou si une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="a5ef4-106">This notification is sent even if the user cancels or if an error occurs.</span></span>


```C++
SPFILENOTIFY_ENDDELETE
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="a5ef4-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a5ef4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5ef4-108">*Param1*</span><span class="sxs-lookup"><span data-stu-id="a5ef4-108">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="a5ef4-109">Pointeur vers une structure [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) .</span><span class="sxs-lookup"><span data-stu-id="a5ef4-109">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span> <span data-ttu-id="a5ef4-110">Le membre **Win32Error** de la structure **FILEPATHS** indique le résultat d’une opération de copie.</span><span class="sxs-lookup"><span data-stu-id="a5ef4-110">The **Win32Error** member of the **FILEPATHS** structure indicates the outcome of a copy operation.</span></span>

</dd> <dt>

<span data-ttu-id="a5ef4-111">*Param2*</span><span class="sxs-lookup"><span data-stu-id="a5ef4-111">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="a5ef4-112">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="a5ef4-112">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5ef4-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a5ef4-113">Return value</span></span>

<span data-ttu-id="a5ef4-114">Le code de retour est ignoré.</span><span class="sxs-lookup"><span data-stu-id="a5ef4-114">The return code is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5ef4-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a5ef4-115">Requirements</span></span>



| <span data-ttu-id="a5ef4-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a5ef4-116">Requirement</span></span> | <span data-ttu-id="a5ef4-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="a5ef4-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a5ef4-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a5ef4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a5ef4-119">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a5ef4-119">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a5ef4-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a5ef4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a5ef4-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a5ef4-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a5ef4-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="a5ef4-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5ef4-123"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5ef4-123"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5ef4-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a5ef4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5ef4-125">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="a5ef4-125">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="a5ef4-126">Notifications</span><span class="sxs-lookup"><span data-stu-id="a5ef4-126">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="a5ef4-127">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="a5ef4-127">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="a5ef4-128">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="a5ef4-128">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="a5ef4-129">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="a5ef4-129">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

 




