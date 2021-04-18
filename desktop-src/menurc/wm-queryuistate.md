---
title: Message WM_QUERYUISTATE (winuser. h)
description: Une application envoie le \_ message WM QUERYUISTATE pour récupérer l’état de l’interface utilisateur d’une fenêtre.
ms.assetid: 3a9e3477-b5d7-4c55-b6d4-8a479451fee8
keywords:
- WM_QUERYUISTATE des menus de message et d’autres ressources
topic_type:
- apiref
api_name:
- WM_QUERYUISTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1574fe0dab2a0885c8012bf19eed50facfd6cce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512212"
---
# <a name="wm_queryuistate-message"></a><span data-ttu-id="d7adb-104">\_Message WM QUERYUISTATE</span><span class="sxs-lookup"><span data-stu-id="d7adb-104">WM\_QUERYUISTATE message</span></span>

<span data-ttu-id="d7adb-105">Une application envoie le message **WM \_ QUERYUISTATE** pour récupérer l’état de l’interface utilisateur d’une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="d7adb-105">An application sends the **WM\_QUERYUISTATE** message to retrieve the UI state for a window.</span></span>


```C++
#define WM_QUERYUISTATE                 0x0129
```



## <a name="parameters"></a><span data-ttu-id="d7adb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d7adb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7adb-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d7adb-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d7adb-108">Ce paramètre n’est pas utilisé et doit être égal à 0.</span><span class="sxs-lookup"><span data-stu-id="d7adb-108">This parameter is not used and must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="d7adb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d7adb-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d7adb-110">Ce paramètre n’est pas utilisé et doit être égal à 0.</span><span class="sxs-lookup"><span data-stu-id="d7adb-110">This parameter is not used and must be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7adb-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d7adb-111">Return value</span></span>

<span data-ttu-id="d7adb-112">La valeur de retour est **null** si les indicateurs de focus et les accélérateurs de clavier sont visibles.</span><span class="sxs-lookup"><span data-stu-id="d7adb-112">The return value is **NULL** if the focus indicators and the keyboard accelerators are visible.</span></span> <span data-ttu-id="d7adb-113">Dans le cas contraire, la valeur de retour peut être une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="d7adb-113">Otherwise, the return value can be one or more of the following values.</span></span>



| <span data-ttu-id="d7adb-114">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="d7adb-114">Return code/value</span></span>                                                                                                                                       | <span data-ttu-id="d7adb-115">Description</span><span class="sxs-lookup"><span data-stu-id="d7adb-115">Description</span></span>                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d7adb-116"><dt>**UISF \_**</dt> <dt>0x4</dt> actif</span><span class="sxs-lookup"><span data-stu-id="d7adb-116"><dt>**UISF\_ACTIVE**</dt> <dt>0x4</dt></span></span> </dl>    | <span data-ttu-id="d7adb-117">Un contrôle doit être dessiné dans le style utilisé pour les contrôles actifs.</span><span class="sxs-lookup"><span data-stu-id="d7adb-117">A control should be drawn in the style used for active controls.</span></span><br/> |
| <dl> <span data-ttu-id="d7adb-118"><dt>**UISF \_ HIDEACCEL**</dt> <dt>0X2</dt></span><span class="sxs-lookup"><span data-stu-id="d7adb-118"><dt>**UISF\_HIDEACCEL**</dt> <dt>0x2</dt></span></span> </dl> | <span data-ttu-id="d7adb-119">Les accélérateurs clavier sont masqués.</span><span class="sxs-lookup"><span data-stu-id="d7adb-119">Keyboard accelerators are hidden.</span></span><br/>                                |
| <dl> <span data-ttu-id="d7adb-120"><dt>**UISF \_ HIDEFOCUS**</dt> <dt>0x1</dt></span><span class="sxs-lookup"><span data-stu-id="d7adb-120"><dt>**UISF\_HIDEFOCUS**</dt> <dt>0x1</dt></span></span> </dl> | <span data-ttu-id="d7adb-121">Les indicateurs de focus sont masqués.</span><span class="sxs-lookup"><span data-stu-id="d7adb-121">Focus indicators are hidden.</span></span><br/>                                     |



 

## <a name="requirements"></a><span data-ttu-id="d7adb-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d7adb-122">Requirements</span></span>



| <span data-ttu-id="d7adb-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d7adb-123">Requirement</span></span> | <span data-ttu-id="d7adb-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="d7adb-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7adb-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7adb-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d7adb-126">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d7adb-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d7adb-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7adb-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d7adb-128">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d7adb-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d7adb-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="d7adb-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7adb-130"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d7adb-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7adb-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d7adb-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="d7adb-132">**Référence**</span><span class="sxs-lookup"><span data-stu-id="d7adb-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d7adb-133">**\_CHANGEUISTATE WM**</span><span class="sxs-lookup"><span data-stu-id="d7adb-133">**WM\_CHANGEUISTATE**</span></span>](wm-changeuistate.md)
</dt> <dt>

[<span data-ttu-id="d7adb-134">**\_UPDATEUISTATE WM**</span><span class="sxs-lookup"><span data-stu-id="d7adb-134">**WM\_UPDATEUISTATE**</span></span>](wm-updateuistate.md)
</dt> <dt>

<span data-ttu-id="d7adb-135">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="d7adb-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d7adb-136">Raccourcis clavier</span><span class="sxs-lookup"><span data-stu-id="d7adb-136">Keyboard Accelerators</span></span>](keyboard-accelerators.md)
</dt> </dl>

 

 





