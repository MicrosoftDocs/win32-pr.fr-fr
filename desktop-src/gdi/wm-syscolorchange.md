---
description: Le \_ message WM SYSCOLORCHANGE est envoyé à toutes les fenêtres de niveau supérieur quand une modification est apportée à un paramètre de couleur système.
ms.assetid: ffe61768-86d6-4ea8-ae2d-1095a9afa925
title: Message WM_SYSCOLORCHANGE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac3883f0534d91a6d852b0e70fbb4edabdcab56b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973767"
---
# <a name="wm_syscolorchange-message"></a><span data-ttu-id="d101e-103">\_Message WM SYSCOLORCHANGE</span><span class="sxs-lookup"><span data-stu-id="d101e-103">WM\_SYSCOLORCHANGE message</span></span>

<span data-ttu-id="d101e-104">Le message **WM \_ SYSCOLORCHANGE** est envoyé à toutes les fenêtres de niveau supérieur quand une modification est apportée à un paramètre de couleur système.</span><span class="sxs-lookup"><span data-stu-id="d101e-104">The **WM\_SYSCOLORCHANGE** message is sent to all top-level windows when a change is made to a system color setting.</span></span>

<span data-ttu-id="d101e-105">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="d101e-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="d101e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d101e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d101e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d101e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d101e-108">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="d101e-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d101e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d101e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d101e-110">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="d101e-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d101e-111">Notes</span><span class="sxs-lookup"><span data-stu-id="d101e-111">Remarks</span></span>

<span data-ttu-id="d101e-112">Le système envoie un message de [**\_ peinture WM**](wm-paint.md) à toute fenêtre affectée par une modification de couleur système.</span><span class="sxs-lookup"><span data-stu-id="d101e-112">The system sends a [**WM\_PAINT**](wm-paint.md) message to any window that is affected by a system color change.</span></span>

<span data-ttu-id="d101e-113">Les applications qui ont des pinceaux utilisant les couleurs système existantes doivent supprimer ces pinceaux et les recréer à l’aide des nouvelles couleurs système.</span><span class="sxs-lookup"><span data-stu-id="d101e-113">Applications that have brushes using the existing system colors should delete those brushes and re-create them using the new system colors.</span></span>

<span data-ttu-id="d101e-114">Les fenêtres de niveau supérieur qui utilisent des contrôles communs doivent transférer le message **WM \_ SYSCOLORCHANGE** aux contrôles ; sinon, les contrôles ne sont pas notifiés de la modification de la couleur.</span><span class="sxs-lookup"><span data-stu-id="d101e-114">Top level windows that use common controls must forward the **WM\_SYSCOLORCHANGE** message to the controls; otherwise, the controls will not be notified of the color change.</span></span> <span data-ttu-id="d101e-115">Cela garantit que les couleurs utilisées par vos contrôles communs sont cohérentes avec celles utilisées par d’autres objets de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d101e-115">This ensures that the colors used by your common controls are consistent with those used by other user interface objects.</span></span> <span data-ttu-id="d101e-116">Par exemple, un contrôle ToolBar utilise la couleur « objets 3D » pour dessiner ses boutons.</span><span class="sxs-lookup"><span data-stu-id="d101e-116">For example, a toolbar control uses the "3D Objects" color to draw its buttons.</span></span> <span data-ttu-id="d101e-117">Si l’utilisateur modifie la couleur des objets 3D mais que le message **WM \_ SYSCOLORCHANGE** n’est pas transféré à la barre d’outils, les boutons de la barre d’outils restent dans leur couleur d’origine, tandis que la couleur des autres boutons du système change.</span><span class="sxs-lookup"><span data-stu-id="d101e-117">If the user changes the 3D Objects color but the **WM\_SYSCOLORCHANGE** message is not forwarded to the toolbar, the toolbar buttons will remain in their original color while the color of other buttons in the system changes.</span></span>

## <a name="requirements"></a><span data-ttu-id="d101e-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d101e-118">Requirements</span></span>



| <span data-ttu-id="d101e-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d101e-119">Requirement</span></span> | <span data-ttu-id="d101e-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="d101e-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d101e-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d101e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d101e-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d101e-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d101e-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d101e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d101e-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d101e-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d101e-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="d101e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="d101e-126"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d101e-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d101e-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d101e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d101e-128">Vue d’ensemble des couleurs</span><span class="sxs-lookup"><span data-stu-id="d101e-128">Colors Overview</span></span>](colors.md)
</dt> <dt>

[<span data-ttu-id="d101e-129">Messages de couleur</span><span class="sxs-lookup"><span data-stu-id="d101e-129">Color Messages</span></span>](color-messages.md)
</dt> <dt>

[<span data-ttu-id="d101e-130">**\_peinture WM**</span><span class="sxs-lookup"><span data-stu-id="d101e-130">**WM\_PAINT**</span></span>](wm-paint.md)
</dt> </dl>

 

 
