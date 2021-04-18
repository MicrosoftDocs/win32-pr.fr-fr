---
description: Une application envoie le \_ message WM MDIRESTORE à une fenêtre cliente d’interface multidocument (MDI) pour restaurer une fenêtre enfant MDI de taille agrandie ou réduite.
ms.assetid: bb99fda1-9eb5-4307-9326-9a417a046c22
title: Message WM_MDIRESTORE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc2cf36a0b428e1e9003682a5e766f613fd7ba81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516235"
---
# <a name="wm_mdirestore-message"></a><span data-ttu-id="3e540-103">\_Message WM MDIRESTORE</span><span class="sxs-lookup"><span data-stu-id="3e540-103">WM\_MDIRESTORE message</span></span>

<span data-ttu-id="3e540-104">Une application envoie le message **WM \_ MDIRESTORE** à une fenêtre cliente d’interface multidocument (MDI) pour restaurer une fenêtre enfant MDI de taille agrandie ou réduite.</span><span class="sxs-lookup"><span data-stu-id="3e540-104">An application sends the **WM\_MDIRESTORE** message to a multiple-document interface (MDI) client window to restore an MDI child window from maximized or minimized size.</span></span>


```C++
#define WM_MDIRESTORE                   0x0223
```



## <a name="parameters"></a><span data-ttu-id="3e540-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3e540-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e540-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3e540-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3e540-107">Handle de la fenêtre enfant MDI à restaurer.</span><span class="sxs-lookup"><span data-stu-id="3e540-107">A handle to the MDI child window to be restored.</span></span>

</dd> <dt>

<span data-ttu-id="3e540-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3e540-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3e540-109">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="3e540-109">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e540-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3e540-110">Return value</span></span>

<span data-ttu-id="3e540-111">Type : **zéro**</span><span class="sxs-lookup"><span data-stu-id="3e540-111">Type: **zero**</span></span>

<span data-ttu-id="3e540-112">La valeur de retour est toujours zéro.</span><span class="sxs-lookup"><span data-stu-id="3e540-112">The return value is always zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e540-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3e540-113">Requirements</span></span>



| <span data-ttu-id="3e540-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3e540-114">Requirement</span></span> | <span data-ttu-id="3e540-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="3e540-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e540-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3e540-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3e540-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3e540-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="3e540-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3e540-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3e540-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3e540-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3e540-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="3e540-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e540-121"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3e540-121"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e540-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3e540-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="3e540-123">**Référence**</span><span class="sxs-lookup"><span data-stu-id="3e540-123">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3e540-124">**\_MDIMAXIMIZE WM**</span><span class="sxs-lookup"><span data-stu-id="3e540-124">**WM\_MDIMAXIMIZE**</span></span>](wm-mdimaximize.md)
</dt> <dt>

<span data-ttu-id="3e540-125">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="3e540-125">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="3e540-126">Interface multidocument</span><span class="sxs-lookup"><span data-stu-id="3e540-126">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 




