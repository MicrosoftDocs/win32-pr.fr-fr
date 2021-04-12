---
title: Message WM_MENURBUTTONUP (winuser. h)
description: Envoyé lorsque l’utilisateur relâche le bouton droit de la souris alors que le curseur se trouve sur un élément de menu.
ms.assetid: e061cba0-6aea-4df4-a39a-7e55f0db45c0
keywords:
- WM_MENURBUTTONUP des menus de message et d’autres ressources
topic_type:
- apiref
api_name:
- WM_MENURBUTTONUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7206fc79f6f990611c81ad0e844ae26af3764c6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317517"
---
# <a name="wm_menurbuttonup-message"></a><span data-ttu-id="2c41c-104">\_Message WM MENURBUTTONUP</span><span class="sxs-lookup"><span data-stu-id="2c41c-104">WM\_MENURBUTTONUP message</span></span>

<span data-ttu-id="2c41c-105">Envoyé lorsque l’utilisateur relâche le bouton droit de la souris alors que le curseur se trouve sur un élément de menu.</span><span class="sxs-lookup"><span data-stu-id="2c41c-105">Sent when the user releases the right mouse button while the cursor is on a menu item.</span></span>


```C++
#define WM_MENURBUTTONUP                0x0122
```



## <a name="parameters"></a><span data-ttu-id="2c41c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2c41c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c41c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2c41c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2c41c-108">Index de base zéro de l’élément de menu sur lequel le bouton droit de la souris a été relâché.</span><span class="sxs-lookup"><span data-stu-id="2c41c-108">The zero-based index of the menu item on which the right mouse button was released.</span></span>

</dd> <dt>

<span data-ttu-id="2c41c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2c41c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2c41c-110">Handle du menu contenant l’élément.</span><span class="sxs-lookup"><span data-stu-id="2c41c-110">A handle to the menu containing the item.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2c41c-111">Notes</span><span class="sxs-lookup"><span data-stu-id="2c41c-111">Remarks</span></span>

<span data-ttu-id="2c41c-112">Le message **WM \_ MENURBUTTONUP** permet aux applications de fournir un menu contextuel également appelé menu contextuel pour l’élément de menu spécifié dans ce message.</span><span class="sxs-lookup"><span data-stu-id="2c41c-112">The **WM\_MENURBUTTONUP** message allows applications to provide a context-sensitive menu also known as a shortcut menu for the menu item specified in this message.</span></span> <span data-ttu-id="2c41c-113">Pour afficher un menu contextuel pour un élément de menu, appelez la fonction [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) avec le **module TPM \_ recurse**.</span><span class="sxs-lookup"><span data-stu-id="2c41c-113">To display a context-sensitive menu for a menu item, call the [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) function with **TPM\_RECURSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c41c-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2c41c-114">Requirements</span></span>



| <span data-ttu-id="2c41c-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2c41c-115">Requirement</span></span> | <span data-ttu-id="2c41c-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="2c41c-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c41c-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2c41c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2c41c-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2c41c-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="2c41c-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2c41c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2c41c-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2c41c-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2c41c-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="2c41c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c41c-122"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2c41c-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c41c-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2c41c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c41c-124">Vue d’ensemble des menus</span><span class="sxs-lookup"><span data-stu-id="2c41c-124">Menus Overview</span></span>](menus.md)
</dt> </dl>

 

 





