---
title: Message WM_ENTERIDLE (winuser. h)
description: Envoyé à la fenêtre propriétaire d’un menu ou d’une boîte de dialogue modale qui passe à l’état inactif. Un menu ou une boîte de dialogue modale passe à l’état inactif quand aucun message n’est en attente dans sa file d’attente après avoir traité un ou plusieurs messages précédents.
ms.assetid: 11b1f942-185f-4de4-90a2-e2934bb1394f
keywords:
- Boîtes de dialogue de WM_ENTERIDLE message
topic_type:
- apiref
api_name:
- WM_ENTERIDLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f99b3150a0dbc1a81b78498c8e295fbf2397c22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385036"
---
# <a name="wm_enteridle-message"></a><span data-ttu-id="94eb1-105">\_Message WM ENTERIDLE</span><span class="sxs-lookup"><span data-stu-id="94eb1-105">WM\_ENTERIDLE message</span></span>

<span data-ttu-id="94eb1-106">Envoyé à la fenêtre propriétaire d’un menu ou d’une boîte de dialogue modale qui passe à l’état inactif.</span><span class="sxs-lookup"><span data-stu-id="94eb1-106">Sent to the owner window of a modal dialog box or menu that is entering an idle state.</span></span> <span data-ttu-id="94eb1-107">Un menu ou une boîte de dialogue modale passe à l’état inactif quand aucun message n’est en attente dans sa file d’attente après avoir traité un ou plusieurs messages précédents.</span><span class="sxs-lookup"><span data-stu-id="94eb1-107">A modal dialog box or menu enters an idle state when no messages are waiting in its queue after it has processed one or more previous messages.</span></span>


```C++
#define WM_ENTERIDLE                    0x0121
```



## <a name="parameters"></a><span data-ttu-id="94eb1-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="94eb1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94eb1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="94eb1-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="94eb1-110">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="94eb1-110">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="94eb1-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="94eb1-111">Value</span></span>                                                                                                                                                                                                                   | <span data-ttu-id="94eb1-112">Signification</span><span class="sxs-lookup"><span data-stu-id="94eb1-112">Meaning</span></span>                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="MSGF_DIALOGBOX"></span><span id="msgf_dialogbox"></span><dl> <span data-ttu-id="94eb1-113"><dt>**MSGF \_ DIALOGBOX**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="94eb1-113"><dt>**MSGF\_DIALOGBOX**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="94eb1-114">Le système est inactif, car une boîte de dialogue s’affiche.</span><span class="sxs-lookup"><span data-stu-id="94eb1-114">The system is idle because a dialog box is displayed.</span></span><br/> |
| <span id="MSGF_MENU"></span><span id="msgf_menu"></span><dl> <span data-ttu-id="94eb1-115"><dt>**MSGF \_ MENU**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="94eb1-115"><dt>**MSGF\_MENU**</dt> <dt>2</dt></span></span> </dl>                | <span data-ttu-id="94eb1-116">Le système est inactif, car un menu est affiché.</span><span class="sxs-lookup"><span data-stu-id="94eb1-116">The system is idle because a menu is displayed.</span></span><br/>       |



 

</dd> <dt>

<span data-ttu-id="94eb1-117">*lParam*</span><span class="sxs-lookup"><span data-stu-id="94eb1-117">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="94eb1-118">Handle de la boîte de dialogue (si *wParam* est **MSGF \_ DialogBox**) ou fenêtre contenant le menu affiché (si *wParam* est **le \_ menu MSGF**).</span><span class="sxs-lookup"><span data-stu-id="94eb1-118">A handle to the dialog box (if *wParam* is **MSGF\_DIALOGBOX**) or window containing the displayed menu (if *wParam* is **MSGF\_MENU**).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94eb1-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="94eb1-119">Return value</span></span>

<span data-ttu-id="94eb1-120">Une application doit retourner zéro si elle traite ce message.</span><span class="sxs-lookup"><span data-stu-id="94eb1-120">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="94eb1-121">Notes</span><span class="sxs-lookup"><span data-stu-id="94eb1-121">Remarks</span></span>

<span data-ttu-id="94eb1-122">Vous pouvez supprimer le message **WM \_ ENTERIDLE** pour une boîte de dialogue en créant la boîte de dialogue avec le style **DS \_ NOIDLEMSG** .</span><span class="sxs-lookup"><span data-stu-id="94eb1-122">You can suppress the **WM\_ENTERIDLE** message for a dialog box by creating the dialog box with the **DS\_NOIDLEMSG** style.</span></span>

## <a name="requirements"></a><span data-ttu-id="94eb1-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="94eb1-123">Requirements</span></span>



| <span data-ttu-id="94eb1-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="94eb1-124">Requirement</span></span> | <span data-ttu-id="94eb1-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="94eb1-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94eb1-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="94eb1-126">Minimum supported client</span></span><br/> | <span data-ttu-id="94eb1-127">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="94eb1-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="94eb1-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="94eb1-128">Minimum supported server</span></span><br/> | <span data-ttu-id="94eb1-129">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="94eb1-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="94eb1-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="94eb1-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="94eb1-131"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="94eb1-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94eb1-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="94eb1-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="94eb1-133">**Référence**</span><span class="sxs-lookup"><span data-stu-id="94eb1-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="94eb1-134">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="94eb1-134">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

<span data-ttu-id="94eb1-135">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="94eb1-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="94eb1-136">Boîtes de dialogue</span><span class="sxs-lookup"><span data-stu-id="94eb1-136">Dialog Boxes</span></span>](dialog-boxes.md)
</dt> </dl>

 

