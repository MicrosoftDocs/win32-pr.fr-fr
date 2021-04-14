---
title: Message WM_MENUCOMMAND (winuser. h)
description: Envoyé lorsque l’utilisateur effectue une sélection à partir d’un menu.
ms.assetid: 1ed702ef-8d32-4d4c-a68a-ffd199112ced
keywords:
- WM_MENUCOMMAND des menus de message et d’autres ressources
topic_type:
- apiref
api_name:
- WM_MENUCOMMAND
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13288c49327b536db6ebef8a41526facd3fb2d51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385279"
---
# <a name="wm_menucommand-message"></a><span data-ttu-id="e636b-104">\_Message WM MENUCOMMAND</span><span class="sxs-lookup"><span data-stu-id="e636b-104">WM\_MENUCOMMAND message</span></span>

<span data-ttu-id="e636b-105">Envoyé lorsque l’utilisateur effectue une sélection à partir d’un menu.</span><span class="sxs-lookup"><span data-stu-id="e636b-105">Sent when the user makes a selection from a menu.</span></span>


```C++
#define WM_MENUCOMMAND                  0x0126
```



## <a name="parameters"></a><span data-ttu-id="e636b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e636b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e636b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e636b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e636b-108">Index de base zéro de l’élément sélectionné.</span><span class="sxs-lookup"><span data-stu-id="e636b-108">The zero-based index of the item selected.</span></span>

</dd> <dt>

<span data-ttu-id="e636b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e636b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e636b-110">Handle vers le menu de l’élément sélectionné.</span><span class="sxs-lookup"><span data-stu-id="e636b-110">A handle to the menu for the item selected.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e636b-111">Notes</span><span class="sxs-lookup"><span data-stu-id="e636b-111">Remarks</span></span>

<span data-ttu-id="e636b-112">Le message **WM \_ MENUCOMMAND** vous donne un handle au menu qui vous permet d’accéder aux données de menu dans la structure [**MENUINFO**](/windows/win32/api/winuser/ns-winuser-menuinfo) et vous donne également l’index de l’élément sélectionné, ce qui est généralement ce dont les applications ont besoin.</span><span class="sxs-lookup"><span data-stu-id="e636b-112">The **WM\_MENUCOMMAND** message gives you a handle to the menu so you can access the menu data in the [**MENUINFO**](/windows/win32/api/winuser/ns-winuser-menuinfo) structure and also gives you the index of the selected item, which is typically what applications need.</span></span> <span data-ttu-id="e636b-113">En revanche, le message de [**\_ commande WM**](wm-command.md) vous donne l’identificateur d’élément de menu.</span><span class="sxs-lookup"><span data-stu-id="e636b-113">In contrast, the [**WM\_COMMAND**](wm-command.md) message gives you the menu item identifier.</span></span>

<span data-ttu-id="e636b-114">Le **message WM \_ MENUCOMMAND** est envoyé uniquement pour les menus définis avec l’indicateur **MNS \_ NOTIFYBYPOS** défini dans le membre **dwStyle** de la structure [**MENUINFO**](/windows/win32/api/winuser/ns-winuser-menuinfo) .</span><span class="sxs-lookup"><span data-stu-id="e636b-114">The **WM\_MENUCOMMAND** message is sent only for menus that are defined with the **MNS\_NOTIFYBYPOS** flag set in the **dwStyle** member of the [**MENUINFO**](/windows/win32/api/winuser/ns-winuser-menuinfo) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="e636b-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e636b-115">Requirements</span></span>



| <span data-ttu-id="e636b-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e636b-116">Requirement</span></span> | <span data-ttu-id="e636b-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="e636b-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e636b-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e636b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e636b-119">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e636b-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e636b-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e636b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e636b-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e636b-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e636b-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="e636b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e636b-123"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e636b-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e636b-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e636b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e636b-125">Vue d’ensemble des menus</span><span class="sxs-lookup"><span data-stu-id="e636b-125">Menus Overview</span></span>](menus.md)
</dt> </dl>

 

 





