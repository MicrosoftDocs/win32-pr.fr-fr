---
description: La \_ notification SPFILENOTIFY ENDRENAME est envoyée à la routine de rappel lorsque la file d’attente termine une opération de changement de nom. Cette notification est envoyée même si l’utilisateur annule ou si une erreur se produit.
ms.assetid: 8d5a8d17-de4f-4100-aa72-dfefeb8d4db9
title: Message d’SPFILENOTIFY_ENDRENAME (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a316d4dfe72ee9eb7d85fdb70eb90e1cf3d3f463
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523674"
---
# <a name="spfilenotify_endrename-message"></a><span data-ttu-id="b7ef6-104">\_Message SPFILENOTIFY ENDRENAME</span><span class="sxs-lookup"><span data-stu-id="b7ef6-104">SPFILENOTIFY\_ENDRENAME message</span></span>

<span data-ttu-id="b7ef6-105">La notification **SPFILENOTIFY \_ ENDRENAME** est envoyée à la routine de rappel lorsque la file d’attente termine une opération de changement de nom.</span><span class="sxs-lookup"><span data-stu-id="b7ef6-105">The **SPFILENOTIFY\_ENDRENAME** notification is sent to the callback routine when the queue completes a rename operation.</span></span> <span data-ttu-id="b7ef6-106">Cette notification est envoyée même si l’utilisateur annule ou si une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="b7ef6-106">This notification is sent even if the user cancels or if an error occurs.</span></span>


```C++
SPFILENOTIFY_ENDRENAME
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="b7ef6-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b7ef6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7ef6-108">*Param1*</span><span class="sxs-lookup"><span data-stu-id="b7ef6-108">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="b7ef6-109">Pointeur vers une structure [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) .</span><span class="sxs-lookup"><span data-stu-id="b7ef6-109">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span> <span data-ttu-id="b7ef6-110">Le membre **Win32Error** de la structure **FILEPATHS** indique le résultat de l’opération de copie.</span><span class="sxs-lookup"><span data-stu-id="b7ef6-110">The **Win32Error** member of the **FILEPATHS** structure indicates the outcome of the copy operation.</span></span>

</dd> <dt>

<span data-ttu-id="b7ef6-111">*Param2*</span><span class="sxs-lookup"><span data-stu-id="b7ef6-111">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="b7ef6-112">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="b7ef6-112">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7ef6-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b7ef6-113">Return value</span></span>

<span data-ttu-id="b7ef6-114">La valeur de retour est ignorée.</span><span class="sxs-lookup"><span data-stu-id="b7ef6-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7ef6-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b7ef6-115">Requirements</span></span>



| <span data-ttu-id="b7ef6-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b7ef6-116">Requirement</span></span> | <span data-ttu-id="b7ef6-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="b7ef6-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b7ef6-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7ef6-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b7ef6-119">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b7ef6-119">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b7ef6-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7ef6-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b7ef6-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b7ef6-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b7ef6-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="b7ef6-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7ef6-123"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7ef6-123"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7ef6-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b7ef6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7ef6-125">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="b7ef6-125">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="b7ef6-126">Notifications</span><span class="sxs-lookup"><span data-stu-id="b7ef6-126">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="b7ef6-127">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="b7ef6-127">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="b7ef6-128">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="b7ef6-128">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="b7ef6-129">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="b7ef6-129">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

 




