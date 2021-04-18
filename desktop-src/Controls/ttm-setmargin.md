---
title: Message TTM_SETMARGIN (commctrl. h)
description: Définit les marges supérieure, gauche, inférieure et droite d’une fenêtre d’info-bulle. Une marge est la distance, en pixels, entre la bordure de la fenêtre d’info-bulle et le texte contenu dans la fenêtre d’info-bulle.
ms.assetid: f1663861-c217-42dd-8249-7647b1651910
keywords:
- TTM_SETMARGIN les contrôles de message Windows
topic_type:
- apiref
api_name:
- TTM_SETMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ed46bf40833a3046d15386782897eb6b573b29c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509322"
---
# <a name="ttm_setmargin-message"></a><span data-ttu-id="fc2d1-105">\_Message atténuation SETMARGIN</span><span class="sxs-lookup"><span data-stu-id="fc2d1-105">TTM\_SETMARGIN message</span></span>

<span data-ttu-id="fc2d1-106">Définit les marges supérieure, gauche, inférieure et droite d’une fenêtre d’info-bulle.</span><span class="sxs-lookup"><span data-stu-id="fc2d1-106">Sets the top, left, bottom, and right margins for a tooltip window.</span></span> <span data-ttu-id="fc2d1-107">Une marge est la distance, en pixels, entre la bordure de la fenêtre d’info-bulle et le texte contenu dans la fenêtre d’info-bulle.</span><span class="sxs-lookup"><span data-stu-id="fc2d1-107">A margin is the distance, in pixels, between the tooltip window border and the text contained within the tooltip window.</span></span>

## <a name="parameters"></a><span data-ttu-id="fc2d1-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fc2d1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc2d1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fc2d1-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="fc2d1-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="fc2d1-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="fc2d1-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fc2d1-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fc2d1-112">Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui contient les informations sur les marges à définir.</span><span class="sxs-lookup"><span data-stu-id="fc2d1-112">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the margin information to be set.</span></span> <span data-ttu-id="fc2d1-113">Les membres de la structure **Rect** ne définissent pas de rectangle englobant.</span><span class="sxs-lookup"><span data-stu-id="fc2d1-113">The members of the **RECT** structure do not define a bounding rectangle.</span></span> <span data-ttu-id="fc2d1-114">Dans le cadre de ce message, les membres de la structure sont interprétés comme suit :</span><span class="sxs-lookup"><span data-stu-id="fc2d1-114">For the purpose of this message, the structure members are interpreted as follows:</span></span>



| <span data-ttu-id="fc2d1-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="fc2d1-115">Value</span></span>                                                                                                                                   | <span data-ttu-id="fc2d1-116">Signification</span><span class="sxs-lookup"><span data-stu-id="fc2d1-116">Meaning</span></span>                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="top"></span><span id="TOP"></span><dl> <span data-ttu-id="fc2d1-117"><dt>**Retour au début**</dt></span><span class="sxs-lookup"><span data-stu-id="fc2d1-117"><dt>**top**</dt></span></span> </dl>          | <span data-ttu-id="fc2d1-118">Distance entre la bordure supérieure et le texte de l’info-bulle, en pixels.</span><span class="sxs-lookup"><span data-stu-id="fc2d1-118">Distance between top border and top of tooltip text, in pixels.</span></span><br/>         |
| <span id="left"></span><span id="LEFT"></span><dl> <span data-ttu-id="fc2d1-119"><dt>**gauche**</dt></span><span class="sxs-lookup"><span data-stu-id="fc2d1-119"><dt>**left**</dt></span></span> </dl>       | <span data-ttu-id="fc2d1-120">Distance entre la bordure gauche et l’extrémité gauche du texte d’info-bulle, en pixels.</span><span class="sxs-lookup"><span data-stu-id="fc2d1-120">Distance between left border and left end of tooltip text, in pixels.</span></span><br/>   |
| <span id="bottom"></span><span id="BOTTOM"></span><dl> <span data-ttu-id="fc2d1-121"><dt>**ballon**</dt></span><span class="sxs-lookup"><span data-stu-id="fc2d1-121"><dt>**bottom**</dt></span></span> </dl> | <span data-ttu-id="fc2d1-122">Distance entre la bordure inférieure et le bas du texte de l’info-bulle, en pixels.</span><span class="sxs-lookup"><span data-stu-id="fc2d1-122">Distance between bottom border and bottom of tooltip text, in pixels.</span></span><br/>   |
| <span id="right"></span><span id="RIGHT"></span><dl> <span data-ttu-id="fc2d1-123"><dt>**Oui**</dt></span><span class="sxs-lookup"><span data-stu-id="fc2d1-123"><dt>**right**</dt></span></span> </dl>    | <span data-ttu-id="fc2d1-124">Distance entre la bordure droite et l’extrémité droite du texte d’info-bulle, en pixels.</span><span class="sxs-lookup"><span data-stu-id="fc2d1-124">Distance between right border and right end of tooltip text, in pixels.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc2d1-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fc2d1-125">Return value</span></span>

<span data-ttu-id="fc2d1-126">La valeur de retour de ce message n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="fc2d1-126">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc2d1-127">Notes</span><span class="sxs-lookup"><span data-stu-id="fc2d1-127">Remarks</span></span>

<span data-ttu-id="fc2d1-128">Ce message n’a aucun effet lorsque l’application s’exécute sur Windows Vista et que les styles visuels sont activés pour l’info-bulle.</span><span class="sxs-lookup"><span data-stu-id="fc2d1-128">This message has no effect when the application runs on Windows Vista and visual styles are enabled for the tooltip.</span></span> <span data-ttu-id="fc2d1-129">Vous pouvez désactiver les styles visuels pour l’info-bulle à l’aide de [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme).</span><span class="sxs-lookup"><span data-stu-id="fc2d1-129">You can disable visual styles for the tooltip by using [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme).</span></span>

## <a name="requirements"></a><span data-ttu-id="fc2d1-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fc2d1-130">Requirements</span></span>



| <span data-ttu-id="fc2d1-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fc2d1-131">Requirement</span></span> | <span data-ttu-id="fc2d1-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="fc2d1-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fc2d1-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fc2d1-133">Minimum supported client</span></span><br/> | <span data-ttu-id="fc2d1-134">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fc2d1-134">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fc2d1-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fc2d1-135">Minimum supported server</span></span><br/> | <span data-ttu-id="fc2d1-136">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fc2d1-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fc2d1-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="fc2d1-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc2d1-138"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc2d1-138"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc2d1-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fc2d1-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc2d1-140">**ATTÉNUATION \_ GETMARGIN**</span><span class="sxs-lookup"><span data-stu-id="fc2d1-140">**TTM\_GETMARGIN**</span></span>](ttm-getmargin.md)
</dt> </dl>

 

