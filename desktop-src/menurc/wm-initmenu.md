---
title: Message WM_INITMENU (winuser. h)
description: Envoyé lorsqu’un menu va devenir actif.
ms.assetid: d0fcc6d8-f57c-4d04-b9e7-4cfab6add173
keywords:
- WM_INITMENU des menus de message et d’autres ressources
topic_type:
- apiref
api_name:
- WM_INITMENU
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94626b99a5016efaa9427d1ae8b3b3122e599965
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106543633"
---
# <a name="wm_initmenu-message"></a><span data-ttu-id="b1333-104">\_Message WM INITMENU</span><span class="sxs-lookup"><span data-stu-id="b1333-104">WM\_INITMENU message</span></span>

<span data-ttu-id="b1333-105">Envoyé lorsqu’un menu va devenir actif.</span><span class="sxs-lookup"><span data-stu-id="b1333-105">Sent when a menu is about to become active.</span></span> <span data-ttu-id="b1333-106">Il se produit lorsque l’utilisateur clique sur un élément dans la barre de menus ou appuie sur une touche de menu.</span><span class="sxs-lookup"><span data-stu-id="b1333-106">It occurs when the user clicks an item on the menu bar or presses a menu key.</span></span> <span data-ttu-id="b1333-107">Cela permet à l’application de modifier le menu avant qu’il ne soit affiché.</span><span class="sxs-lookup"><span data-stu-id="b1333-107">This allows the application to modify the menu before it is displayed.</span></span>

<span data-ttu-id="b1333-108">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b1333-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_INITMENU                     0x0116
```



## <a name="parameters"></a><span data-ttu-id="b1333-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b1333-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1333-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b1333-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b1333-111">Handle du menu à initialiser.</span><span class="sxs-lookup"><span data-stu-id="b1333-111">A handle to the menu to be initialized.</span></span>

</dd> <dt>

<span data-ttu-id="b1333-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b1333-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b1333-113">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="b1333-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1333-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b1333-114">Return value</span></span>

<span data-ttu-id="b1333-115">Si une application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="b1333-115">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1333-116">Notes</span><span class="sxs-lookup"><span data-stu-id="b1333-116">Remarks</span></span>

<span data-ttu-id="b1333-117">Un message **WM \_ INITMENU** est envoyé uniquement lors d’un premier accès à un menu ; un seul message **WM \_ INITMENU** est généré pour chaque accès.</span><span class="sxs-lookup"><span data-stu-id="b1333-117">A **WM\_INITMENU** message is sent only when a menu is first accessed; only one **WM\_INITMENU** message is generated for each access.</span></span> <span data-ttu-id="b1333-118">Par exemple, le déplacement de la souris sur plusieurs éléments de menu tout en maintenant le bouton enfoncé ne génère pas de nouveaux messages.</span><span class="sxs-lookup"><span data-stu-id="b1333-118">For example, moving the mouse across several menu items while holding down the button does not generate new messages.</span></span> <span data-ttu-id="b1333-119">**WM \_ INITMENU** ne fournit pas d’informations sur les éléments de menu.</span><span class="sxs-lookup"><span data-stu-id="b1333-119">**WM\_INITMENU** does not provide information about menu items.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1333-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b1333-120">Requirements</span></span>



| <span data-ttu-id="b1333-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b1333-121">Requirement</span></span> | <span data-ttu-id="b1333-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="b1333-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1333-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b1333-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b1333-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b1333-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b1333-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b1333-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b1333-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b1333-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b1333-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="b1333-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1333-128"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b1333-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1333-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b1333-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="b1333-130">**Référence**</span><span class="sxs-lookup"><span data-stu-id="b1333-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b1333-131">**\_INITMENUPOPUP WM**</span><span class="sxs-lookup"><span data-stu-id="b1333-131">**WM\_INITMENUPOPUP**</span></span>](wm-initmenupopup.md)
</dt> <dt>

<span data-ttu-id="b1333-132">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="b1333-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b1333-133">Raccourcis clavier</span><span class="sxs-lookup"><span data-stu-id="b1333-133">Keyboard Accelerators</span></span>](keyboard-accelerators.md)
</dt> </dl>

 

