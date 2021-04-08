---
title: Message LVM_EDITLABEL (commctrl. h)
description: Commence la modification sur place du texte de l’élément d’affichage de liste spécifié. Le message sélectionne et concentre implicitement l’élément spécifié. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView EditLabel.
ms.assetid: b63f13f1-6e66-4770-af84-30bcdb241727
keywords:
- LVM_EDITLABEL les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_EDITLABEL
- LVM_EDITLABELA
- LVM_EDITLABELW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25cb4e119731c41130e1c19fdea2f74882796435
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739965"
---
# <a name="lvm_editlabel-message"></a><span data-ttu-id="e1b92-106">\_Message EDITLABEL LVM</span><span class="sxs-lookup"><span data-stu-id="e1b92-106">LVM\_EDITLABEL message</span></span>

<span data-ttu-id="e1b92-107">Commence la modification sur place du texte de l’élément d’affichage de liste spécifié.</span><span class="sxs-lookup"><span data-stu-id="e1b92-107">Begins in-place editing of the specified list-view item's text.</span></span> <span data-ttu-id="e1b92-108">Le message sélectionne et concentre implicitement l’élément spécifié.</span><span class="sxs-lookup"><span data-stu-id="e1b92-108">The message implicitly selects and focuses the specified item.</span></span> <span data-ttu-id="e1b92-109">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ EditLabel**](/windows/desktop/api/Commctrl/nf-commctrl-listview_editlabel) .</span><span class="sxs-lookup"><span data-stu-id="e1b92-109">You can send this message explicitly or by using the [**ListView\_EditLabel**](/windows/desktop/api/Commctrl/nf-commctrl-listview_editlabel) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e1b92-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e1b92-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1b92-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e1b92-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e1b92-112">Index de l’élément de vue de liste.</span><span class="sxs-lookup"><span data-stu-id="e1b92-112">The index of the list-view item.</span></span> <span data-ttu-id="e1b92-113">Pour annuler la modification, affectez la valeur-1 à l’index.</span><span class="sxs-lookup"><span data-stu-id="e1b92-113">To cancel editing, set the index to -1.</span></span>

</dd> <dt>

<span data-ttu-id="e1b92-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e1b92-114">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="e1b92-115">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="e1b92-115">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1b92-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e1b92-116">Return value</span></span>

<span data-ttu-id="e1b92-117">Retourne le handle du contrôle d’édition utilisé pour modifier le texte de l’élément en cas de réussite, ou **null** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="e1b92-117">Returns the handle to the edit control that is used to edit the item text if successful, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1b92-118">Notes</span><span class="sxs-lookup"><span data-stu-id="e1b92-118">Remarks</span></span>

<span data-ttu-id="e1b92-119">Lorsque l’utilisateur termine ou annule la modification, le contrôle d’édition est détruit et le descripteur n’est plus valide.</span><span class="sxs-lookup"><span data-stu-id="e1b92-119">When the user completes or cancels editing, the edit control is destroyed and the handle is no longer valid.</span></span> <span data-ttu-id="e1b92-120">Vous pouvez sous-définir le contrôle d’édition, mais vous ne devez pas le détruire.</span><span class="sxs-lookup"><span data-stu-id="e1b92-120">You can subclass the edit control, but you should not destroy it.</span></span>

<span data-ttu-id="e1b92-121">Le contrôle doit avoir le focus avant d’envoyer ce message au contrôle.</span><span class="sxs-lookup"><span data-stu-id="e1b92-121">The control must have the focus before you send this message to the control.</span></span> <span data-ttu-id="e1b92-122">Le focus peut être défini à l’aide de la fonction [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) .</span><span class="sxs-lookup"><span data-stu-id="e1b92-122">Focus can be set using the [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) function.</span></span>

<span data-ttu-id="e1b92-123">Si *wParam* est-1, un code de notification [LVN \_ ENDLABELEDIT](lvn-endlabeledit.md) est envoyé.</span><span class="sxs-lookup"><span data-stu-id="e1b92-123">If *wParam* is -1, an [LVN\_ENDLABELEDIT](lvn-endlabeledit.md) notification code is sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1b92-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e1b92-124">Requirements</span></span>



| <span data-ttu-id="e1b92-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e1b92-125">Requirement</span></span> | <span data-ttu-id="e1b92-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1b92-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e1b92-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e1b92-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e1b92-128">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e1b92-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e1b92-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e1b92-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e1b92-130">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e1b92-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e1b92-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="e1b92-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1b92-132"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1b92-132"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="e1b92-133">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="e1b92-133">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e1b92-134">**LVM \_ EDITLABELW** (Unicode) et **LVM \_ EDITLABELA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="e1b92-134">**LVM\_EDITLABELW** (Unicode) and **LVM\_EDITLABELA** (ANSI)</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="e1b92-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e1b92-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1b92-136">**\_CANCELMODE WM**</span><span class="sxs-lookup"><span data-stu-id="e1b92-136">**WM\_CANCELMODE**</span></span>](/windows/desktop/winmsg/wm-cancelmode)
</dt> </dl>

 

