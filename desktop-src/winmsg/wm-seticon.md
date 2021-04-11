---
description: Associe une nouvelle grande ou petite icône à une fenêtre. Le système affiche la grande icône dans la boîte de dialogue ALT + TAB et la petite icône dans le titre de la fenêtre.
ms.assetid: c86620f2-893b-46f8-8254-1d7c4c142f37
title: Message WM_SETICON (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88bec7fc653123ba0a950c96bc1f54ebf436b0d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202878"
---
# <a name="wm_seticon-message"></a><span data-ttu-id="e2883-104">\_Message WM SETICON</span><span class="sxs-lookup"><span data-stu-id="e2883-104">WM\_SETICON message</span></span>

<span data-ttu-id="e2883-105">Associe une nouvelle grande ou petite icône à une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e2883-105">Associates a new large or small icon with a window.</span></span> <span data-ttu-id="e2883-106">Le système affiche la grande icône dans la boîte de dialogue ALT + TAB et la petite icône dans le titre de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e2883-106">The system displays the large icon in the ALT+TAB dialog box, and the small icon in the window caption.</span></span>


```C++
#define WM_SETICON                      0x0080
```



## <a name="parameters"></a><span data-ttu-id="e2883-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e2883-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2883-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e2883-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e2883-109">Type d’icône à définir.</span><span class="sxs-lookup"><span data-stu-id="e2883-109">The type of icon to be set.</span></span> <span data-ttu-id="e2883-110">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="e2883-110">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="e2883-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="e2883-111">Value</span></span>                                                                                                                                                                                                       | <span data-ttu-id="e2883-112">Signification</span><span class="sxs-lookup"><span data-stu-id="e2883-112">Meaning</span></span>                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="ICON_BIG"></span><span id="icon_big"></span><dl> <span data-ttu-id="e2883-113"><dt>**Icône \_ BIG**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e2883-113"><dt>**ICON\_BIG**</dt> <dt>1</dt></span></span> </dl>       | <span data-ttu-id="e2883-114">Définissez la grande icône pour la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e2883-114">Set the large icon for the window.</span></span><br/> |
| <span id="ICON_SMALL"></span><span id="icon_small"></span><dl> <span data-ttu-id="e2883-115"><dt>**Icône \_ PETIT**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e2883-115"><dt>**ICON\_SMALL**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="e2883-116">Définissez la petite icône pour la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e2883-116">Set the small icon for the window.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e2883-117">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e2883-117">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e2883-118">Handle vers la nouvelle icône de grande taille ou petite.</span><span class="sxs-lookup"><span data-stu-id="e2883-118">A handle to the new large or small icon.</span></span> <span data-ttu-id="e2883-119">Si ce paramètre a la **valeur null**, l’icône indiquée par *wParam* est supprimée.</span><span class="sxs-lookup"><span data-stu-id="e2883-119">If this parameter is **NULL**, the icon indicated by *wParam* is removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2883-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e2883-120">Return value</span></span>

<span data-ttu-id="e2883-121">Type : **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="e2883-121">Type: **LRESULT**</span></span>

<span data-ttu-id="e2883-122">La valeur de retour est un handle vers la grande icône précédente ou petite, en fonction de la valeur de *wParam*.</span><span class="sxs-lookup"><span data-stu-id="e2883-122">The return value is a handle to the previous large or small icon, depending on the value of *wParam*.</span></span> <span data-ttu-id="e2883-123">La **valeur est null** si la fenêtre n’avait pas précédemment d’icône de type indiquée par *wParam*.</span><span class="sxs-lookup"><span data-stu-id="e2883-123">It is **NULL** if the window previously had no icon of the type indicated by *wParam*.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2883-124">Notes</span><span class="sxs-lookup"><span data-stu-id="e2883-124">Remarks</span></span>

<span data-ttu-id="e2883-125">La fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) retourne un descripteur à la grande ou petite icône précédente associée à la fenêtre, en fonction de la valeur de *wParam*.</span><span class="sxs-lookup"><span data-stu-id="e2883-125">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function returns a handle to the previous large or small icon associated with the window, depending on the value of *wParam*.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2883-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e2883-126">Requirements</span></span>



| <span data-ttu-id="e2883-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e2883-127">Requirement</span></span> | <span data-ttu-id="e2883-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="e2883-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2883-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e2883-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e2883-130">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e2883-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e2883-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e2883-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e2883-132">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e2883-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e2883-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="e2883-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2883-134"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e2883-134"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2883-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e2883-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="e2883-136">**Référence**</span><span class="sxs-lookup"><span data-stu-id="e2883-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e2883-137">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="e2883-137">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="e2883-138">**\_GETICON WM**</span><span class="sxs-lookup"><span data-stu-id="e2883-138">**WM\_GETICON**</span></span>](wm-geticon.md)
</dt> <dt>

<span data-ttu-id="e2883-139">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="e2883-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e2883-140">Windows</span><span class="sxs-lookup"><span data-stu-id="e2883-140">Windows</span></span>](windows.md)
</dt> </dl>

 

 
