---
title: Message WM_ENTERMENULOOP (winuser. h)
description: Notifie la procédure de fenêtre principale d’une application qu’une boucle modale de menu a été entrée.
ms.assetid: 0a018b6f-fe4b-4e90-bbb6-9b5719253dc1
keywords:
- WM_ENTERMENULOOP des menus de message et d’autres ressources
topic_type:
- apiref
api_name:
- WM_ENTERMENULOOP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a7b325719c428dc7310503320b53f3a5f96182e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510122"
---
# <a name="wm_entermenuloop-message"></a><span data-ttu-id="97010-104">\_Message WM ENTERMENULOOP</span><span class="sxs-lookup"><span data-stu-id="97010-104">WM\_ENTERMENULOOP message</span></span>

<span data-ttu-id="97010-105">Notifie la procédure de fenêtre principale d’une application qu’une boucle modale de menu a été entrée.</span><span class="sxs-lookup"><span data-stu-id="97010-105">Notifies an application's main window procedure that a menu modal loop has been entered.</span></span>


```C++
#define WM_ENTERMENULOOP                0x0211
```



## <a name="parameters"></a><span data-ttu-id="97010-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="97010-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97010-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="97010-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="97010-108">Spécifie si le menu fenêtre a été entré à l’aide de la fonction [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) .</span><span class="sxs-lookup"><span data-stu-id="97010-108">Specifies whether the window menu was entered using the [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) function.</span></span> <span data-ttu-id="97010-109">Ce paramètre a la valeur **true** si le menu fenêtre a été entré à l’aide de **TrackPopupMenu**, et **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="97010-109">This parameter has a value of **TRUE** if the window menu was entered using **TrackPopupMenu**, and **FALSE** if it was not.</span></span>

</dd> <dt>

<span data-ttu-id="97010-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="97010-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="97010-111">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="97010-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97010-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="97010-112">Return value</span></span>

<span data-ttu-id="97010-113">Une application doit retourner zéro si elle traite ce message.</span><span class="sxs-lookup"><span data-stu-id="97010-113">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="97010-114">Notes</span><span class="sxs-lookup"><span data-stu-id="97010-114">Remarks</span></span>

<span data-ttu-id="97010-115">La fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) retourne la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="97010-115">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="97010-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="97010-116">Requirements</span></span>



| <span data-ttu-id="97010-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="97010-117">Requirement</span></span> | <span data-ttu-id="97010-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="97010-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97010-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="97010-119">Minimum supported client</span></span><br/> | <span data-ttu-id="97010-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="97010-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="97010-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="97010-121">Minimum supported server</span></span><br/> | <span data-ttu-id="97010-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="97010-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="97010-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="97010-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="97010-124"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="97010-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97010-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="97010-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="97010-126">**Référence**</span><span class="sxs-lookup"><span data-stu-id="97010-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="97010-127">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="97010-127">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="97010-128">**\_EXITMENULOOP WM**</span><span class="sxs-lookup"><span data-stu-id="97010-128">**WM\_EXITMENULOOP**</span></span>](wm-exitmenuloop.md)
</dt> <dt>

<span data-ttu-id="97010-129">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="97010-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="97010-130">Menus</span><span class="sxs-lookup"><span data-stu-id="97010-130">Menus</span></span>](menus.md)
</dt> </dl>

 

