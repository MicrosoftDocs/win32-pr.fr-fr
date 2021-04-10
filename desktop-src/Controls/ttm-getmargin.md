---
title: Message TTM_GETMARGIN (commctrl. h)
description: Récupère les marges supérieure, gauche, inférieure et droite définies pour une fenêtre d’info-bulle. Une marge est la distance, en pixels, entre la bordure de la fenêtre d’info-bulle et le texte contenu dans la fenêtre d’info-bulle.
ms.assetid: c33ee1de-5fbd-4c7e-a703-576c2ffd3052
keywords:
- TTM_GETMARGIN les contrôles de message Windows
topic_type:
- apiref
api_name:
- TTM_GETMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bb3e795d8eac14522f0994a342c7f781b7112ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942149"
---
# <a name="ttm_getmargin-message"></a><span data-ttu-id="d5356-105">\_Message atténuation GETMARGIN</span><span class="sxs-lookup"><span data-stu-id="d5356-105">TTM\_GETMARGIN message</span></span>

<span data-ttu-id="d5356-106">Récupère les marges supérieure, gauche, inférieure et droite définies pour une fenêtre d’info-bulle.</span><span class="sxs-lookup"><span data-stu-id="d5356-106">Retrieves the top, left, bottom, and right margins set for a tooltip window.</span></span> <span data-ttu-id="d5356-107">Une marge est la distance, en pixels, entre la bordure de la fenêtre d’info-bulle et le texte contenu dans la fenêtre d’info-bulle.</span><span class="sxs-lookup"><span data-stu-id="d5356-107">A margin is the distance, in pixels, between the tooltip window border and the text contained within the tooltip window.</span></span>

## <a name="parameters"></a><span data-ttu-id="d5356-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d5356-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5356-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d5356-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d5356-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="d5356-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d5356-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d5356-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d5356-112">Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui recevra les informations de marge.</span><span class="sxs-lookup"><span data-stu-id="d5356-112">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that will receive the margin information.</span></span> <span data-ttu-id="d5356-113">Les membres de la structure **Rect** ne définissent pas de rectangle englobant.</span><span class="sxs-lookup"><span data-stu-id="d5356-113">The members of the **RECT** structure do not define a bounding rectangle.</span></span> <span data-ttu-id="d5356-114">Dans le cadre de ce message, les membres de la structure sont interprétés comme suit :</span><span class="sxs-lookup"><span data-stu-id="d5356-114">For the purpose of this message, the structure members are interpreted as follows:</span></span>



| <span data-ttu-id="d5356-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="d5356-115">Value</span></span>                                                                                                                                   | <span data-ttu-id="d5356-116">Signification</span><span class="sxs-lookup"><span data-stu-id="d5356-116">Meaning</span></span>                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="top"></span><span id="TOP"></span><dl> <span data-ttu-id="d5356-117"><dt>**Retour au début**</dt></span><span class="sxs-lookup"><span data-stu-id="d5356-117"><dt>**top**</dt></span></span> </dl>          | <span data-ttu-id="d5356-118">Distance entre la bordure supérieure et le texte de l’info-bulle, en pixels.</span><span class="sxs-lookup"><span data-stu-id="d5356-118">Distance between top border and top of tooltip text, in pixels.</span></span><br/>         |
| <span id="left"></span><span id="LEFT"></span><dl> <span data-ttu-id="d5356-119"><dt>**gauche**</dt></span><span class="sxs-lookup"><span data-stu-id="d5356-119"><dt>**left**</dt></span></span> </dl>       | <span data-ttu-id="d5356-120">Distance entre la bordure gauche et l’extrémité gauche du texte d’info-bulle, en pixels.</span><span class="sxs-lookup"><span data-stu-id="d5356-120">Distance between left border and left end of tooltip text, in pixels.</span></span><br/>   |
| <span id="bottom"></span><span id="BOTTOM"></span><dl> <span data-ttu-id="d5356-121"><dt>**ballon**</dt></span><span class="sxs-lookup"><span data-stu-id="d5356-121"><dt>**bottom**</dt></span></span> </dl> | <span data-ttu-id="d5356-122">Distance entre la bordure inférieure et le bas du texte de l’info-bulle, en pixels.</span><span class="sxs-lookup"><span data-stu-id="d5356-122">Distance between bottom border and bottom of tooltip text, in pixels.</span></span><br/>   |
| <span id="right"></span><span id="RIGHT"></span><dl> <span data-ttu-id="d5356-123"><dt>**Oui**</dt></span><span class="sxs-lookup"><span data-stu-id="d5356-123"><dt>**right**</dt></span></span> </dl>    | <span data-ttu-id="d5356-124">Distance entre la bordure droite et l’extrémité droite du texte d’info-bulle, en pixels.</span><span class="sxs-lookup"><span data-stu-id="d5356-124">Distance between right border and right end of tooltip text, in pixels.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5356-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d5356-125">Return value</span></span>

<span data-ttu-id="d5356-126">La valeur de retour de ce message n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="d5356-126">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5356-127">Notes</span><span class="sxs-lookup"><span data-stu-id="d5356-127">Remarks</span></span>

<span data-ttu-id="d5356-128">Par défaut, les quatre marges sont égales à zéro lorsque vous créez le contrôle ToolTip.</span><span class="sxs-lookup"><span data-stu-id="d5356-128">All four margins default to zero when you create the tooltip control.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5356-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d5356-129">Requirements</span></span>



| <span data-ttu-id="d5356-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d5356-130">Requirement</span></span> | <span data-ttu-id="d5356-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="d5356-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d5356-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d5356-132">Minimum supported client</span></span><br/> | <span data-ttu-id="d5356-133">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d5356-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d5356-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d5356-134">Minimum supported server</span></span><br/> | <span data-ttu-id="d5356-135">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d5356-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d5356-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="d5356-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5356-137"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5356-137"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5356-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d5356-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5356-139">**ATTÉNUATION \_ SETMARGIN**</span><span class="sxs-lookup"><span data-stu-id="d5356-139">**TTM\_SETMARGIN**</span></span>](ttm-setmargin.md)
</dt> </dl>

 

