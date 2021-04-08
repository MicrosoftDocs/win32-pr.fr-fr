---
title: Message WM_EXITMENULOOP (winuser. h)
description: Notifie la procédure de fenêtre principale d’une application qu’une boucle modale de menu a été quittée.
ms.assetid: b2a9d537-af7c-4c8a-932a-95e45eb8deb5
keywords:
- WM_EXITMENULOOP des menus de message et d’autres ressources
topic_type:
- apiref
api_name:
- WM_EXITMENULOOP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8440e1a255968eb3e1607b5d54375900f7b5de16
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741708"
---
# <a name="wm_exitmenuloop-message"></a><span data-ttu-id="71db4-104">\_Message WM EXITMENULOOP</span><span class="sxs-lookup"><span data-stu-id="71db4-104">WM\_EXITMENULOOP message</span></span>

<span data-ttu-id="71db4-105">Notifie la procédure de fenêtre principale d’une application qu’une boucle modale de menu a été quittée.</span><span class="sxs-lookup"><span data-stu-id="71db4-105">Notifies an application's main window procedure that a menu modal loop has been exited.</span></span>


```C++
#define WM_EXITMENULOOP                 0x0212
```



## <a name="parameters"></a><span data-ttu-id="71db4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="71db4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71db4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="71db4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="71db4-108">Spécifie si le menu est un menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="71db4-108">Specifies whether the menu is a shortcut menu.</span></span> <span data-ttu-id="71db4-109">Ce paramètre a la valeur **true** s’il s’agit d’un menu contextuel, **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="71db4-109">This parameter has a value of **TRUE** if it is a shortcut menu, **FALSE** if it is not.</span></span>

</dd> <dt>

<span data-ttu-id="71db4-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="71db4-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="71db4-111">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="71db4-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71db4-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="71db4-112">Return value</span></span>

<span data-ttu-id="71db4-113">Une application doit retourner zéro si elle traite ce message.</span><span class="sxs-lookup"><span data-stu-id="71db4-113">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="71db4-114">Notes</span><span class="sxs-lookup"><span data-stu-id="71db4-114">Remarks</span></span>

<span data-ttu-id="71db4-115">La fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) retourne la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="71db4-115">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="71db4-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="71db4-116">Requirements</span></span>



| <span data-ttu-id="71db4-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="71db4-117">Requirement</span></span> | <span data-ttu-id="71db4-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="71db4-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71db4-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="71db4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="71db4-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="71db4-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="71db4-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="71db4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="71db4-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="71db4-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="71db4-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="71db4-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="71db4-124"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="71db4-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71db4-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="71db4-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="71db4-126">**Référence**</span><span class="sxs-lookup"><span data-stu-id="71db4-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="71db4-127">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="71db4-127">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="71db4-128">**\_ENTERMENULOOP WM**</span><span class="sxs-lookup"><span data-stu-id="71db4-128">**WM\_ENTERMENULOOP**</span></span>](wm-entermenuloop.md)
</dt> <dt>

<span data-ttu-id="71db4-129">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="71db4-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="71db4-130">Menus</span><span class="sxs-lookup"><span data-stu-id="71db4-130">Menus</span></span>](menus.md)
</dt> </dl>

 

