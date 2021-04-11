---
title: Message WM_INITMENUPOPUP (winuser. h)
description: Envoyé lorsqu’un menu déroulant ou un sous-menu est sur le paragraphe actif. Cela permet à une application de modifier le menu avant qu’il ne soit affiché, sans modifier le menu entier.
ms.assetid: 08ae1a78-5e68-488c-9b77-ee42044ca3ab
keywords:
- WM_INITMENUPOPUP des menus de message et d’autres ressources
topic_type:
- apiref
api_name:
- WM_INITMENUPOPUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e02bf0f9b8e196c27990cc1bc839daed4c92f8c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032576"
---
# <a name="wm_initmenupopup-message"></a><span data-ttu-id="fd9ac-105">\_Message WM INITMENUPOPUP</span><span class="sxs-lookup"><span data-stu-id="fd9ac-105">WM\_INITMENUPOPUP message</span></span>

<span data-ttu-id="fd9ac-106">Envoyé lorsqu’un menu déroulant ou un sous-menu est sur le paragraphe actif.</span><span class="sxs-lookup"><span data-stu-id="fd9ac-106">Sent when a drop-down menu or submenu is about to become active.</span></span> <span data-ttu-id="fd9ac-107">Cela permet à une application de modifier le menu avant qu’il ne soit affiché, sans modifier le menu entier.</span><span class="sxs-lookup"><span data-stu-id="fd9ac-107">This allows an application to modify the menu before it is displayed, without changing the entire menu.</span></span>


```C++
#define WM_INITMENUPOPUP                0x0117
```



## <a name="parameters"></a><span data-ttu-id="fd9ac-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fd9ac-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd9ac-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fd9ac-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fd9ac-110">Handle vers le menu ou le sous-menu déroulant.</span><span class="sxs-lookup"><span data-stu-id="fd9ac-110">A handle to the drop-down menu or submenu.</span></span>

</dd> <dt>

<span data-ttu-id="fd9ac-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fd9ac-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fd9ac-112">Le mot de poids faible spécifie la position relative de base zéro de l’élément de menu qui ouvre le menu déroulant ou le sous-menu.</span><span class="sxs-lookup"><span data-stu-id="fd9ac-112">The low-order word specifies the zero-based relative position of the menu item that opens the drop-down menu or submenu.</span></span>

<span data-ttu-id="fd9ac-113">Le mot de poids fort indique si le menu déroulant est le menu fenêtre.</span><span class="sxs-lookup"><span data-stu-id="fd9ac-113">The high-order word indicates whether the drop-down menu is the window menu.</span></span> <span data-ttu-id="fd9ac-114">Si le menu est le menu fenêtre, ce paramètre a la **valeur true**; Sinon, la **valeur est false**.</span><span class="sxs-lookup"><span data-stu-id="fd9ac-114">If the menu is the window menu, this parameter is **TRUE**; otherwise, it is **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd9ac-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fd9ac-115">Return value</span></span>

<span data-ttu-id="fd9ac-116">Si une application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="fd9ac-116">If an application processes this message, it should return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd9ac-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fd9ac-117">Requirements</span></span>



| <span data-ttu-id="fd9ac-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fd9ac-118">Requirement</span></span> | <span data-ttu-id="fd9ac-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd9ac-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd9ac-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd9ac-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fd9ac-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fd9ac-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="fd9ac-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd9ac-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fd9ac-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fd9ac-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fd9ac-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="fd9ac-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd9ac-125"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fd9ac-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd9ac-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd9ac-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="fd9ac-127">**Référence**</span><span class="sxs-lookup"><span data-stu-id="fd9ac-127">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="fd9ac-128">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fd9ac-128">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="fd9ac-129">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fd9ac-129">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="fd9ac-130">**\_INITMENU WM**</span><span class="sxs-lookup"><span data-stu-id="fd9ac-130">**WM\_INITMENU**</span></span>](wm-initmenu.md)
</dt> <dt>

<span data-ttu-id="fd9ac-131">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="fd9ac-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="fd9ac-132">Raccourcis clavier</span><span class="sxs-lookup"><span data-stu-id="fd9ac-132">Keyboard Accelerators</span></span>](keyboard-accelerators.md)
</dt> </dl>

 

