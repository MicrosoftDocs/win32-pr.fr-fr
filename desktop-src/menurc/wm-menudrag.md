---
title: Message WM_MENUDRAG (winuser. h)
description: Envoyé au propriétaire d’un menu glisser-déplacer lorsque l’utilisateur fait glisser un élément de menu.
ms.assetid: 99e8f490-ef1e-4964-a3a1-47030a88f10c
keywords:
- WM_MENUDRAG des menus de message et d’autres ressources
topic_type:
- apiref
api_name:
- WM_MENUDRAG
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b67e83c41576a716d292187df4cb08fa803271c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106516102"
---
# <a name="wm_menudrag-message"></a><span data-ttu-id="f9372-104">\_Message WM MENUDRAG</span><span class="sxs-lookup"><span data-stu-id="f9372-104">WM\_MENUDRAG message</span></span>

<span data-ttu-id="f9372-105">Envoyé au propriétaire d’un menu glisser-déplacer lorsque l’utilisateur fait glisser un élément de menu.</span><span class="sxs-lookup"><span data-stu-id="f9372-105">Sent to the owner of a drag-and-drop menu when the user drags a menu item.</span></span>


```C++
#define WM_MENUDRAG                     0x0123
```



## <a name="parameters"></a><span data-ttu-id="f9372-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f9372-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9372-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f9372-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f9372-108">Position de l’élément où l’opération glisser a commencé.</span><span class="sxs-lookup"><span data-stu-id="f9372-108">The position of the item where the drag operation began.</span></span>

</dd> <dt>

<span data-ttu-id="f9372-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f9372-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f9372-110">Handle du menu contenant l’élément.</span><span class="sxs-lookup"><span data-stu-id="f9372-110">A handle to the menu containing the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9372-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f9372-111">Return value</span></span>

<span data-ttu-id="f9372-112">L’application doit retourner l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="f9372-112">The application should return one of the following values.</span></span>



| <span data-ttu-id="f9372-113">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="f9372-113">Return code/value</span></span>                                                                                                                                   | <span data-ttu-id="f9372-114">Description</span><span class="sxs-lookup"><span data-stu-id="f9372-114">Description</span></span>                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f9372-115"><dt>**MND \_ CONTINUER**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f9372-115"><dt>**MND\_CONTINUE**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="f9372-116">Le menu doit rester actif.</span><span class="sxs-lookup"><span data-stu-id="f9372-116">Menu should remain active.</span></span> <span data-ttu-id="f9372-117">Si la souris est relâchée, elle doit être ignorée.</span><span class="sxs-lookup"><span data-stu-id="f9372-117">If the mouse is released, it should be ignored.</span></span><br/> |
| <dl> <span data-ttu-id="f9372-118"><dt>**MND \_ ENDMENU**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="f9372-118"><dt>**MND\_ENDMENU**</dt> <dt>1</dt></span></span> </dl>  | <span data-ttu-id="f9372-119">Le menu doit être terminé.</span><span class="sxs-lookup"><span data-stu-id="f9372-119">Menu should be ended.</span></span><br/>                                                      |



 

## <a name="remarks"></a><span data-ttu-id="f9372-120">Notes</span><span class="sxs-lookup"><span data-stu-id="f9372-120">Remarks</span></span>

<span data-ttu-id="f9372-121">L’application peut appeler la fonction [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) en réponse à ce message.</span><span class="sxs-lookup"><span data-stu-id="f9372-121">The application can call the [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) function in response to this message.</span></span>

<span data-ttu-id="f9372-122">Pour créer un menu glisser-déplacer, appelez [**SetMenuInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuinfo) avec **MNS \_ DRAGDROP**.</span><span class="sxs-lookup"><span data-stu-id="f9372-122">To create a drag-and-drop menu, call [**SetMenuInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuinfo) with **MNS\_DRAGDROP**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9372-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f9372-123">Requirements</span></span>



| <span data-ttu-id="f9372-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f9372-124">Requirement</span></span> | <span data-ttu-id="f9372-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="f9372-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9372-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f9372-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f9372-127">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f9372-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f9372-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f9372-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f9372-129">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f9372-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f9372-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="f9372-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9372-131"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f9372-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9372-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f9372-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="f9372-133">**Référence**</span><span class="sxs-lookup"><span data-stu-id="f9372-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f9372-134">**SetMenuInfo**</span><span class="sxs-lookup"><span data-stu-id="f9372-134">**SetMenuInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setmenuinfo)
</dt> <dt>

<span data-ttu-id="f9372-135">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="f9372-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f9372-136">Menus</span><span class="sxs-lookup"><span data-stu-id="f9372-136">Menus</span></span>](menus.md)
</dt> </dl>

 

