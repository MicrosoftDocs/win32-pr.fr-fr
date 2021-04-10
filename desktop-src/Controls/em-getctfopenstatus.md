---
title: Message EM_GETCTFOPENSTATUS (RichEdit. h)
description: Détermine si le clavier de l’infrastructure TSF (Text Services Framework) est ouvert ou fermé.
ms.assetid: a50fedf4-b4e5-4b99-be46-1bbbf08e85a8
keywords:
- EM_GETCTFOPENSTATUS les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETCTFOPENSTATUS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ce1bbf09af6c61a33c33c4172ff699fa5bd26f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942241"
---
# <a name="em_getctfopenstatus-message"></a><span data-ttu-id="559f8-104">\_Message GETCTFOPENSTATUS em</span><span class="sxs-lookup"><span data-stu-id="559f8-104">EM\_GETCTFOPENSTATUS message</span></span>

<span data-ttu-id="559f8-105">Détermine si le clavier de l’infrastructure TSF (Text Services Framework) est ouvert ou fermé.</span><span class="sxs-lookup"><span data-stu-id="559f8-105">Determines if the Text Services Framework (TSF) keyboard is open or closed.</span></span>

## <a name="parameters"></a><span data-ttu-id="559f8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="559f8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="559f8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="559f8-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="559f8-108">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="559f8-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="559f8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="559f8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="559f8-110">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="559f8-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="559f8-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="559f8-111">Return value</span></span>

<span data-ttu-id="559f8-112">Si le clavier TSF est ouvert, la valeur de retour est **true**.</span><span class="sxs-lookup"><span data-stu-id="559f8-112">If the TSF keyboard is open, the return value is **TRUE**.</span></span> <span data-ttu-id="559f8-113">Sinon, la **valeur est false**.</span><span class="sxs-lookup"><span data-stu-id="559f8-113">Otherwise, it is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="559f8-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="559f8-114">Requirements</span></span>



| <span data-ttu-id="559f8-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="559f8-115">Requirement</span></span> | <span data-ttu-id="559f8-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="559f8-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="559f8-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="559f8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="559f8-118">Windows XP avec les \[ applications de bureau SP1 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="559f8-118">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="559f8-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="559f8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="559f8-120">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="559f8-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="559f8-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="559f8-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="559f8-122"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="559f8-122"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="559f8-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="559f8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="559f8-124">**\_SETCTFOPENSTATUS em**</span><span class="sxs-lookup"><span data-stu-id="559f8-124">**EM\_SETCTFOPENSTATUS**</span></span>](em-setctfopenstatus.md)
</dt> </dl>

 

 





