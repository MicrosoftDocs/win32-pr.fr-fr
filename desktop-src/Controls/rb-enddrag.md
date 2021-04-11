---
title: Message RB_ENDDRAG (commctrl. h)
description: Termine l’opération de glisser-déplacer du contrôle rebar. Ce message n’entraîne pas l’envoi d’une \_ notification ENDDRAG RBN.
ms.assetid: 4991dda6-32ea-4d3e-9d39-17c2b6995f09
keywords:
- RB_ENDDRAG les contrôles de message Windows
topic_type:
- apiref
api_name:
- RB_ENDDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b6f201471b6f260555aacb9d89c1363492ed6bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942461"
---
# <a name="rb_enddrag-message"></a><span data-ttu-id="8798f-105">\_Message ENDDRAG RB</span><span class="sxs-lookup"><span data-stu-id="8798f-105">RB\_ENDDRAG message</span></span>

<span data-ttu-id="8798f-106">Termine l’opération de glisser-déplacer du contrôle rebar.</span><span class="sxs-lookup"><span data-stu-id="8798f-106">Terminates the rebar control's drag-and-drop operation.</span></span> <span data-ttu-id="8798f-107">Ce message n’entraîne pas l’envoi d’une notification [ \_ ENDDRAG RBN](rbn-enddrag.md) .</span><span class="sxs-lookup"><span data-stu-id="8798f-107">This message does not cause an [RBN\_ENDDRAG](rbn-enddrag.md) notification to be sent.</span></span>

## <a name="parameters"></a><span data-ttu-id="8798f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8798f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8798f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8798f-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="8798f-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="8798f-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="8798f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8798f-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="8798f-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="8798f-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8798f-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8798f-113">Return value</span></span>

<span data-ttu-id="8798f-114">La valeur de retour de ce message n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="8798f-114">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="8798f-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8798f-115">Requirements</span></span>



| <span data-ttu-id="8798f-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8798f-116">Requirement</span></span> | <span data-ttu-id="8798f-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="8798f-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8798f-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8798f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8798f-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8798f-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8798f-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8798f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8798f-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8798f-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8798f-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="8798f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8798f-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8798f-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8798f-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8798f-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="8798f-125">**Référence**</span><span class="sxs-lookup"><span data-stu-id="8798f-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8798f-126">**\_BEGINDRAG RB**</span><span class="sxs-lookup"><span data-stu-id="8798f-126">**RB\_BEGINDRAG**</span></span>](rb-begindrag.md)
</dt> <dt>

[<span data-ttu-id="8798f-127">**\_DRAGMOVE RB**</span><span class="sxs-lookup"><span data-stu-id="8798f-127">**RB\_DRAGMOVE**</span></span>](rb-dragmove.md)
</dt> </dl>

 

 





