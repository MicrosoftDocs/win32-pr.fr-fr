---
title: Message EM_SETCTFOPENSTATUS (RichEdit. h)
description: Ouvre ou ferme le clavier Text Services Framework (TSF).
ms.assetid: 9bdabf5a-93db-4b0e-9528-807d262de866
keywords:
- EM_SETCTFOPENSTATUS les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SETCTFOPENSTATUS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf4163a415f129dfc5d3f98aa06578d13bb462e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033151"
---
# <a name="em_setctfopenstatus-message"></a><span data-ttu-id="f47d2-104">\_Message SETCTFOPENSTATUS em</span><span class="sxs-lookup"><span data-stu-id="f47d2-104">EM\_SETCTFOPENSTATUS message</span></span>

<span data-ttu-id="f47d2-105">Ouvre ou ferme le clavier Text Services Framework (TSF).</span><span class="sxs-lookup"><span data-stu-id="f47d2-105">Opens or closes the Text Services Framework (TSF) keyboard.</span></span>

## <a name="parameters"></a><span data-ttu-id="f47d2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f47d2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f47d2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f47d2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f47d2-108">Pour activer le clavier TSF, utilisez **true**.</span><span class="sxs-lookup"><span data-stu-id="f47d2-108">To turn on the TSF keyboard, use **TRUE**.</span></span> <span data-ttu-id="f47d2-109">Pour désactiver le clavier TSF, utilisez **false**.</span><span class="sxs-lookup"><span data-stu-id="f47d2-109">To turn off the TSF keyboard, use **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="f47d2-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f47d2-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f47d2-111">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="f47d2-111">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f47d2-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f47d2-112">Return value</span></span>

<span data-ttu-id="f47d2-113">En cas de réussite, ce message retourne la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="f47d2-113">If successful, this message returns **TRUE**.</span></span> <span data-ttu-id="f47d2-114">En cas d’échec, ce message retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="f47d2-114">If unsuccessful, this message returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f47d2-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f47d2-115">Requirements</span></span>



| <span data-ttu-id="f47d2-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f47d2-116">Requirement</span></span> | <span data-ttu-id="f47d2-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="f47d2-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f47d2-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f47d2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f47d2-119">Windows XP avec les \[ applications de bureau SP1 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f47d2-119">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f47d2-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f47d2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f47d2-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f47d2-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f47d2-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="f47d2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f47d2-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f47d2-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f47d2-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f47d2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f47d2-125">**\_GETCTFOPENSTATUS em**</span><span class="sxs-lookup"><span data-stu-id="f47d2-125">**EM\_GETCTFOPENSTATUS**</span></span>](em-getctfopenstatus.md)
</dt> </dl>

 

 





