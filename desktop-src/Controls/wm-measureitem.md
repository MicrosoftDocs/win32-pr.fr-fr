---
title: Message WM_MEASUREITEM (winuser. h)
description: Envoyé à la fenêtre propriétaire d’une zone de liste déroulante, d’une zone de liste, d’un contrôle de vue de liste ou d’un élément de menu lors de la création du contrôle ou du menu.
ms.assetid: 6947bcd1-fd40-4238-b8f2-d4e06b90c0dc
keywords:
- WM_MEASUREITEM les contrôles de message Windows
topic_type:
- apiref
api_name:
- WM_MEASUREITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43e14cc0c39e1d319fb9190f8ad7d51ea25f821c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843877"
---
# <a name="wm_measureitem-message"></a><span data-ttu-id="13a81-104">\_Message WM MEASUREITEM</span><span class="sxs-lookup"><span data-stu-id="13a81-104">WM\_MEASUREITEM message</span></span>

<span data-ttu-id="13a81-105">Envoyé à la fenêtre propriétaire d’une zone de liste déroulante, d’une zone de liste, d’un contrôle de vue de liste ou d’un élément de menu lors de la création du contrôle ou du menu.</span><span class="sxs-lookup"><span data-stu-id="13a81-105">Sent to the owner window of a combo box, list box, list-view control, or menu item when the control or menu is created.</span></span>

<span data-ttu-id="13a81-106">Une fenêtre reçoit ce message par le biais de sa fonction [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="13a81-106">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
WM_MEASUREITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="13a81-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="13a81-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13a81-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="13a81-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="13a81-109">Contient la valeur du membre **CtlID** de la structure [**measureitemstruct,**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) vers laquelle pointe le paramètre *lParam* .</span><span class="sxs-lookup"><span data-stu-id="13a81-109">Contains the value of the **CtlID** member of the [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) structure pointed to by the *lParam* parameter.</span></span> <span data-ttu-id="13a81-110">Cette valeur identifie le contrôle qui a envoyé le message **WM \_ MEASUREITEM** .</span><span class="sxs-lookup"><span data-stu-id="13a81-110">This value identifies the control that sent the **WM\_MEASUREITEM** message.</span></span> <span data-ttu-id="13a81-111">Si la valeur est égale à zéro, le message a été envoyé par un menu.</span><span class="sxs-lookup"><span data-stu-id="13a81-111">If the value is zero, the message was sent by a menu.</span></span> <span data-ttu-id="13a81-112">Si la valeur est différente de zéro, le message a été envoyé par une zone de liste déroulante ou par une zone de liste.</span><span class="sxs-lookup"><span data-stu-id="13a81-112">If the value is nonzero, the message was sent by a combo box or by a list box.</span></span> <span data-ttu-id="13a81-113">Si la valeur est différente de zéro, et que la valeur du membre **ItemId** du **Measureitemstruct,** pointé par *lParam* est (uint) 1, le message a été envoyé par un champ d’édition de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="13a81-113">If the value is nonzero, and the value of the **itemID** member of the **MEASUREITEMSTRUCT** pointed to by *lParam* is (UINT)  1, the message was sent by a combo edit field.</span></span>

</dd> <dt>

<span data-ttu-id="13a81-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="13a81-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="13a81-115">Pointeur vers une structure [**measureitemstruct,**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) qui contient les dimensions de l’élément de menu ou de contrôle owner-drawn.</span><span class="sxs-lookup"><span data-stu-id="13a81-115">Pointer to a [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) structure that contains the dimensions of the owner-drawn control or menu item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13a81-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="13a81-116">Return value</span></span>

<span data-ttu-id="13a81-117">Si une application traite ce message, elle doit retourner la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="13a81-117">If an application processes this message, it should return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="13a81-118">Notes</span><span class="sxs-lookup"><span data-stu-id="13a81-118">Remarks</span></span>

<span data-ttu-id="13a81-119">Lorsque la fenêtre propriétaire reçoit le message **WM \_ MEASUREITEM** , le propriétaire remplit la structure [**measureitemstruct,**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) désignée par le paramètre *lParam* du message et retourne la valeur, et indique au système les dimensions du contrôle.</span><span class="sxs-lookup"><span data-stu-id="13a81-119">When the owner window receives the **WM\_MEASUREITEM** message, the owner fills in the [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) structure pointed to by the *lParam* parameter of the message and returns; this informs the system of the dimensions of the control.</span></span> <span data-ttu-id="13a81-120">Si une zone de liste ou une zone de liste déroulante est créée avec le style [**\_ OWNERDRAWVARIABLE**](list-box-styles.md) ou [**CBS \_ OWNERDRAWVARIABLE**](combo-box-styles.md) , ce message est envoyé au propriétaire de chaque élément du contrôle ; sinon, ce message est envoyé une seule fois.</span><span class="sxs-lookup"><span data-stu-id="13a81-120">If a list box or combo box is created with the [**LBS\_OWNERDRAWVARIABLE**](list-box-styles.md) or [**CBS\_OWNERDRAWVARIABLE**](combo-box-styles.md) style, this message is sent to the owner for each item in the control; otherwise, this message is sent once.</span></span>

<span data-ttu-id="13a81-121">Le système envoie le message **WM \_ MEASUREITEM** à la fenêtre propriétaire des zones de liste modifiable et des zones de liste créées avec le style OWNERDRAWFIXED avant d’envoyer le message [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) .</span><span class="sxs-lookup"><span data-stu-id="13a81-121">The system sends the **WM\_MEASUREITEM** message to the owner window of combo boxes and list boxes created with the OWNERDRAWFIXED style before sending the [**WM\_INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) message.</span></span> <span data-ttu-id="13a81-122">Par conséquent, lorsque le propriétaire reçoit ce message, le système n’a pas encore déterminé la hauteur et la largeur de la police utilisée dans le contrôle ; les appels de fonction et les calculs nécessitant ces valeurs doivent se produire dans la fonction principale de l’application ou de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="13a81-122">As a result, when the owner receives this message, the system has not yet determined the height and width of the font used in the control; function calls and calculations requiring these values should occur in the main function of the application or library.</span></span>

## <a name="requirements"></a><span data-ttu-id="13a81-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="13a81-123">Requirements</span></span>



| <span data-ttu-id="13a81-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="13a81-124">Requirement</span></span> | <span data-ttu-id="13a81-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="13a81-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13a81-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="13a81-126">Minimum supported client</span></span><br/> | <span data-ttu-id="13a81-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="13a81-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="13a81-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="13a81-128">Minimum supported server</span></span><br/> | <span data-ttu-id="13a81-129">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="13a81-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="13a81-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="13a81-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="13a81-131"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="13a81-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13a81-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="13a81-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="13a81-133">**Référence**</span><span class="sxs-lookup"><span data-stu-id="13a81-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="13a81-134">**MEASUREITEMSTRUCT,**</span><span class="sxs-lookup"><span data-stu-id="13a81-134">**MEASUREITEMSTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-measureitemstruct)
</dt> <dt>

<span data-ttu-id="13a81-135">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="13a81-135">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="13a81-136">**\_INITDIALOG WM**</span><span class="sxs-lookup"><span data-stu-id="13a81-136">**WM\_INITDIALOG**</span></span>](/windows/desktop/dlgbox/wm-initdialog)
</dt> </dl>

 

