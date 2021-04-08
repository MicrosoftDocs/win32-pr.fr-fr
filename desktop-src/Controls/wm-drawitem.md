---
title: Message WM_DRAWITEM (winuser. h)
description: Envoyé à la fenêtre parente d’un bouton owner-drawn, d’une zone de liste modifiable, d’une zone de liste ou d’un menu lorsqu’un aspect visuel du bouton, zone de liste déroulante, zone de liste ou menu a changé.
ms.assetid: e54bae5e-10d6-43b0-a766-1b270c8873a9
keywords:
- WM_DRAWITEM les contrôles de message Windows
topic_type:
- apiref
api_name:
- WM_DRAWITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5bd6465a560a0590ed9f5b483afae4c0d72d637
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741364"
---
# <a name="wm_drawitem-message"></a><span data-ttu-id="74108-104">\_Message WM DRAWITEM</span><span class="sxs-lookup"><span data-stu-id="74108-104">WM\_DRAWITEM message</span></span>

<span data-ttu-id="74108-105">Envoyé à la fenêtre parente d’un bouton owner-drawn, d’une zone de liste modifiable, d’une zone de liste ou d’un menu lorsqu’un aspect visuel du bouton, zone de liste déroulante, zone de liste ou menu a changé.</span><span class="sxs-lookup"><span data-stu-id="74108-105">Sent to the parent window of an owner-drawn button, combo box, list box, or menu when a visual aspect of the button, combo box, list box, or menu has changed.</span></span>

<span data-ttu-id="74108-106">Une fenêtre reçoit ce message par le biais de sa fonction [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="74108-106">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
WM_DRAWITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="74108-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="74108-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74108-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="74108-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="74108-109">Spécifie l’identificateur du contrôle qui a envoyé le message **WM \_ DRAWITEM** .</span><span class="sxs-lookup"><span data-stu-id="74108-109">Specifies the identifier of the control that sent the **WM\_DRAWITEM** message.</span></span> <span data-ttu-id="74108-110">Si le message a été envoyé par un menu, ce paramètre est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="74108-110">If the message was sent by a menu, this parameter is zero.</span></span>

</dd> <dt>

<span data-ttu-id="74108-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="74108-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="74108-112">Pointeur vers une structure [**drawitemstruct,**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) contenant des informations sur l’élément à dessiner et le type de dessin requis.</span><span class="sxs-lookup"><span data-stu-id="74108-112">Pointer to a [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure containing information about the item to be drawn and the type of drawing required.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74108-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="74108-113">Return value</span></span>

<span data-ttu-id="74108-114">Si une application traite ce message, elle doit retourner la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="74108-114">If an application processes this message, it should return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="74108-115">Notes</span><span class="sxs-lookup"><span data-stu-id="74108-115">Remarks</span></span>

<span data-ttu-id="74108-116">Par défaut, la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) dessine le rectangle de focus pour un élément de zone de liste owner-drawn.</span><span class="sxs-lookup"><span data-stu-id="74108-116">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function draws the focus rectangle for an owner-drawn list box item.</span></span>

<span data-ttu-id="74108-117">Le membre *itemAction* de la structure [**drawitemstruct,**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) spécifie l’opération de dessin qu’une application doit effectuer.</span><span class="sxs-lookup"><span data-stu-id="74108-117">The *itemAction* member of the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure specifies the drawing operation that an application should perform.</span></span>

<span data-ttu-id="74108-118">Avant de revenir au traitement de ce message, une application doit s’assurer que le contexte de périphérique identifié par le membre *HDC* de la structure [**drawitemstruct,**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) est dans l’État par défaut.</span><span class="sxs-lookup"><span data-stu-id="74108-118">Before returning from processing this message, an application should ensure that the device context identified by the *hDC* member of the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure is in the default state.</span></span>

## <a name="requirements"></a><span data-ttu-id="74108-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="74108-119">Requirements</span></span>



| <span data-ttu-id="74108-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="74108-120">Requirement</span></span> | <span data-ttu-id="74108-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="74108-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74108-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="74108-122">Minimum supported client</span></span><br/> | <span data-ttu-id="74108-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="74108-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="74108-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="74108-124">Minimum supported server</span></span><br/> | <span data-ttu-id="74108-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="74108-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="74108-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="74108-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="74108-127"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="74108-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74108-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="74108-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="74108-129">**Référence**</span><span class="sxs-lookup"><span data-stu-id="74108-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="74108-130">**DRAWITEMSTRUCT,**</span><span class="sxs-lookup"><span data-stu-id="74108-130">**DRAWITEMSTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-drawitemstruct)
</dt> <dt>

<span data-ttu-id="74108-131">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="74108-131">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="74108-132">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="74108-132">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> </dl>

 

