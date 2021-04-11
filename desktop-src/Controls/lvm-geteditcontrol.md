---
title: Message LVM_GETEDITCONTROL (commctrl. h)
description: Obtient le handle du contrôle d’édition utilisé pour modifier le texte d’un élément d’affichage de liste. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView GetEditControl.
ms.assetid: 70450b24-9879-4be8-9bc9-f87008b66415
keywords:
- LVM_GETEDITCONTROL les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETEDITCONTROL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79a8790f86fee17f72078f61899edcd79b331759
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032357"
---
# <a name="lvm_geteditcontrol-message"></a><span data-ttu-id="7c76b-105">\_Message GETEDITCONTROL LVM</span><span class="sxs-lookup"><span data-stu-id="7c76b-105">LVM\_GETEDITCONTROL message</span></span>

<span data-ttu-id="7c76b-106">Obtient le handle du contrôle d’édition utilisé pour modifier le texte d’un élément d’affichage de liste.</span><span class="sxs-lookup"><span data-stu-id="7c76b-106">Gets the handle to the edit control being used to edit a list-view item's text.</span></span> <span data-ttu-id="7c76b-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ GetEditControl**](/windows/desktop/api/Commctrl/nf-commctrl-listview_geteditcontrol) .</span><span class="sxs-lookup"><span data-stu-id="7c76b-107">You can send this message explicitly or by using the [**ListView\_GetEditControl**](/windows/desktop/api/Commctrl/nf-commctrl-listview_geteditcontrol) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="7c76b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7c76b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c76b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7c76b-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="7c76b-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="7c76b-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="7c76b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7c76b-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="7c76b-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="7c76b-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c76b-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7c76b-113">Return value</span></span>

<span data-ttu-id="7c76b-114">Retourne le handle du contrôle d’édition en cas de réussite, ou **null** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="7c76b-114">Returns the handle to the edit control if successful, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c76b-115">Notes</span><span class="sxs-lookup"><span data-stu-id="7c76b-115">Remarks</span></span>

<span data-ttu-id="7c76b-116">Lorsque la modification d’étiquette commence, un contrôle d’édition est créé, positionné et initialisé.</span><span class="sxs-lookup"><span data-stu-id="7c76b-116">When label editing begins, an edit control is created, positioned, and initialized.</span></span> <span data-ttu-id="7c76b-117">Avant qu’il ne soit affiché, le contrôle List-View envoie sa fenêtre parente à un code de notification [LVN \_ BEGINLABELEDIT](lvn-beginlabeledit.md) .</span><span class="sxs-lookup"><span data-stu-id="7c76b-117">Before it is displayed, the list-view control sends its parent window an [LVN\_BEGINLABELEDIT](lvn-beginlabeledit.md) notification code.</span></span>

<span data-ttu-id="7c76b-118">Pour personnaliser la modification des étiquettes, implémentez un gestionnaire pour [LVN \_ BEGINLABELEDIT](lvn-beginlabeledit.md) et envoyez-lui un message **\_ GETEDITCONTROL LVM** vers le contrôle List-View.</span><span class="sxs-lookup"><span data-stu-id="7c76b-118">To customize label editing, implement a handler for [LVN\_BEGINLABELEDIT](lvn-beginlabeledit.md) and have it send an **LVM\_GETEDITCONTROL** message to the list-view control.</span></span> <span data-ttu-id="7c76b-119">Si une étiquette est en cours de modification, la valeur de retour est un handle pour le contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="7c76b-119">If a label is being edited, the return value will be a handle to the edit control.</span></span> <span data-ttu-id="7c76b-120">Utilisez ce handle pour personnaliser le contrôle d’édition en envoyant les messages **em \_ xxx** habituels.</span><span class="sxs-lookup"><span data-stu-id="7c76b-120">Use this handle to customize the edit control by sending the usual **EM\_XXX** messages.</span></span>

<span data-ttu-id="7c76b-121">Lorsque l’utilisateur termine ou annule la modification, le contrôle d’édition est détruit et le descripteur n’est plus valide.</span><span class="sxs-lookup"><span data-stu-id="7c76b-121">When the user completes or cancels editing, the edit control is destroyed and the handle is no longer valid.</span></span> <span data-ttu-id="7c76b-122">Vous pouvez sous-définir le contrôle d’édition, mais vous ne devez pas le détruire.</span><span class="sxs-lookup"><span data-stu-id="7c76b-122">You can subclass the edit control, but you should not destroy it.</span></span> <span data-ttu-id="7c76b-123">Pour annuler la modification, envoyez le contrôle d’affichage de liste à un message [**WM \_ CANCELMODE**](/windows/desktop/winmsg/wm-cancelmode) .</span><span class="sxs-lookup"><span data-stu-id="7c76b-123">To cancel editing, send the list-view control a [**WM\_CANCELMODE**](/windows/desktop/winmsg/wm-cancelmode) message.</span></span>

<span data-ttu-id="7c76b-124">L’élément de vue de liste en cours de modification est l’élément ayant actuellement le focus, c’est-à-dire l’élément dans l’État focus.</span><span class="sxs-lookup"><span data-stu-id="7c76b-124">The list-view item being edited is the currently focused item that is, the item in the focused state.</span></span> <span data-ttu-id="7c76b-125">Pour rechercher un élément en fonction de son état, utilisez le message [**LVM \_ GETNEXTITEM**](lvm-getnextitem.md) .</span><span class="sxs-lookup"><span data-stu-id="7c76b-125">To find an item based on its state, use the [**LVM\_GETNEXTITEM**](lvm-getnextitem.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c76b-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7c76b-126">Requirements</span></span>



| <span data-ttu-id="7c76b-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7c76b-127">Requirement</span></span> | <span data-ttu-id="7c76b-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c76b-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7c76b-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c76b-129">Minimum supported client</span></span><br/> | <span data-ttu-id="7c76b-130">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7c76b-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7c76b-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c76b-131">Minimum supported server</span></span><br/> | <span data-ttu-id="7c76b-132">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7c76b-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7c76b-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="7c76b-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c76b-134"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c76b-134"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c76b-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7c76b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c76b-136">**\_GetEditControl ListView**</span><span class="sxs-lookup"><span data-stu-id="7c76b-136">**ListView\_GetEditControl**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-listview_geteditcontrol)
</dt> </dl>

 

