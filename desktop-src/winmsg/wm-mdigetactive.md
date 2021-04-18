---
description: Une application envoie le \_ message WM MDIGETACTIVE à une fenêtre cliente d’interface multidocument (MDI) pour récupérer le handle de la fenêtre enfant MDI active.
ms.assetid: 3ee445be-dd55-4825-8508-fa18a346ffcd
title: Message WM_MDIGETACTIVE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c49f4ec321f526cd4c9766555e2361ef2cfbd040
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520038"
---
# <a name="wm_mdigetactive-message"></a><span data-ttu-id="c9309-103">\_Message WM MDIGETACTIVE</span><span class="sxs-lookup"><span data-stu-id="c9309-103">WM\_MDIGETACTIVE message</span></span>

<span data-ttu-id="c9309-104">Une application envoie le message **WM \_ MDIGETACTIVE** à une fenêtre cliente d’interface multidocument (MDI) pour récupérer le handle de la fenêtre enfant MDI active.</span><span class="sxs-lookup"><span data-stu-id="c9309-104">An application sends the **WM\_MDIGETACTIVE** message to a multiple-document interface (MDI) client window to retrieve the handle to the active MDI child window.</span></span>


```C++
#define WM_MDIGETACTIVE                  0x0229
```



## <a name="parameters"></a><span data-ttu-id="c9309-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c9309-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9309-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c9309-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c9309-107">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="c9309-107">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c9309-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c9309-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c9309-109">État agrandi.</span><span class="sxs-lookup"><span data-stu-id="c9309-109">The maximized state.</span></span> <span data-ttu-id="c9309-110">Si ce paramètre n’est pas **null**, il s’agit d’un pointeur vers une valeur qui indique l’État agrandi de la fenêtre enfant MDI.</span><span class="sxs-lookup"><span data-stu-id="c9309-110">If this parameter is not **NULL**, it is a pointer to a value that indicates the maximized state of the MDI child window.</span></span> <span data-ttu-id="c9309-111">Si la valeur est **true**, la fenêtre est agrandie ; la valeur **false** indique qu’elle ne l’est pas.</span><span class="sxs-lookup"><span data-stu-id="c9309-111">If the value is **TRUE**, the window is maximized; a value of **FALSE** indicates that it is not.</span></span> <span data-ttu-id="c9309-112">Si ce paramètre a la **valeur null**, le paramètre est ignoré.</span><span class="sxs-lookup"><span data-stu-id="c9309-112">If this parameter is **NULL**, the parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9309-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c9309-113">Return value</span></span>

<span data-ttu-id="c9309-114">Type : **HWND**</span><span class="sxs-lookup"><span data-stu-id="c9309-114">Type: **HWND**</span></span>

<span data-ttu-id="c9309-115">La valeur de retour est le handle de la fenêtre enfant MDI active.</span><span class="sxs-lookup"><span data-stu-id="c9309-115">The return value is the handle to the active MDI child window.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9309-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c9309-116">Requirements</span></span>



| <span data-ttu-id="c9309-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c9309-117">Requirement</span></span> | <span data-ttu-id="c9309-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="c9309-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9309-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c9309-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c9309-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c9309-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c9309-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c9309-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c9309-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c9309-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c9309-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="c9309-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9309-124"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c9309-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9309-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9309-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9309-126">Vue d’ensemble de l’interface multidocument</span><span class="sxs-lookup"><span data-stu-id="c9309-126">Multiple Document Interface Overview</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 




