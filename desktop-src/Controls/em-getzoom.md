---
title: Message EM_GETZOOM (RichEdit. h)
description: Obtient le rapport de zoom actuel. Le taux de zoom est toujours compris entre 1/64 et 64. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.
ms.assetid: d4a1daee-4af7-44d1-80d6-0fcaaf3672a8
keywords:
- EM_GETZOOM les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETZOOM
api_location:
- Richedit.h
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40a88aa96787e1fda5cdeb8f77f478a4d51635cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740293"
---
# <a name="em_getzoom-message"></a><span data-ttu-id="8b1c5-106">\_Message GETZOOM em</span><span class="sxs-lookup"><span data-stu-id="8b1c5-106">EM\_GETZOOM message</span></span>

<span data-ttu-id="8b1c5-107">Obtient le taux de zoom actuel pour un contrôle d’édition multiligne ou un contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="8b1c5-107">Gets the current zoom ratio for a multiline edit control or a rich edit control.</span></span> <span data-ttu-id="8b1c5-108">Le taux de zoom est toujours compris entre 1/64 et 64.</span><span class="sxs-lookup"><span data-stu-id="8b1c5-108">The zoom ration is always between 1/64 and 64.</span></span>

## <a name="parameters"></a><span data-ttu-id="8b1c5-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8b1c5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b1c5-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8b1c5-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8b1c5-111">Reçoit le numérateur du rapport de zoom.</span><span class="sxs-lookup"><span data-stu-id="8b1c5-111">Receives the numerator of the zoom ratio.</span></span>

</dd> <dt>

<span data-ttu-id="8b1c5-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8b1c5-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8b1c5-113">Reçoit le dénominateur du rapport de zoom.</span><span class="sxs-lookup"><span data-stu-id="8b1c5-113">Receives the denominator of the zoom ratio.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b1c5-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8b1c5-114">Return value</span></span>

<span data-ttu-id="8b1c5-115">Le message retourne la **valeur true** si le message est traité, ce qui est le cas si *wParam* et *lParam* n’ont pas la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="8b1c5-115">The message returns **TRUE** if message is processed, which it will be if both *wParam* and *lParam* are not **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b1c5-116">Notes</span><span class="sxs-lookup"><span data-stu-id="8b1c5-116">Remarks</span></span>

<span data-ttu-id="8b1c5-117">**Modifier :** Pris en charge dans Windows 10 1809 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="8b1c5-117">**Edit:** Supported in Windows 10 1809 and later.</span></span> <span data-ttu-id="8b1c5-118">Le contrôle d’édition doit avoir le jeu de styles étendus **es \_ ex \_ zoomable** . pour que ce message ait un effet, consultez [modifier les styles étendus de contrôle](edit-control-window-extended-styles.md).</span><span class="sxs-lookup"><span data-stu-id="8b1c5-118">The edit control needs to have the **ES\_EX\_ZOOMABLE** extended style set, for this message to have an effect, see [Edit Control Extended Styles](edit-control-window-extended-styles.md).</span></span> <span data-ttu-id="8b1c5-119">Pour plus d’informations sur le contrôle d’édition, consultez [modifier des contrôles](edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="8b1c5-119">For information about the edit control, see [Edit Controls](edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8b1c5-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8b1c5-120">Requirements</span></span>



| <span data-ttu-id="8b1c5-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8b1c5-121">Requirement</span></span> | <span data-ttu-id="8b1c5-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="8b1c5-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8b1c5-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8b1c5-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8b1c5-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8b1c5-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8b1c5-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8b1c5-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8b1c5-126">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8b1c5-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8b1c5-127">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="8b1c5-127">Redistributable</span></span><br/>          | <span data-ttu-id="8b1c5-128">Édition enrichie 3,0</span><span class="sxs-lookup"><span data-stu-id="8b1c5-128">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="8b1c5-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="8b1c5-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b1c5-130"><dt>RichEdit. h/commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b1c5-130"><dt>Richedit.h/Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b1c5-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b1c5-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b1c5-132">**\_SETZOOM em**</span><span class="sxs-lookup"><span data-stu-id="8b1c5-132">**EM\_SETZOOM**</span></span>](em-setzoom.md)
</dt> </dl>

 

 





