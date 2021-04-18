---
title: Message WM_CONTEXTMENU (winuser. h)
description: Avertit une fenêtre que l’utilisateur a cliqué avec le bouton droit de la souris (cliquez avec le bouton droit) dans la fenêtre.
ms.assetid: e607a61a-0f9b-4d11-b8c0-b01a2e7fb35b
keywords:
- WM_CONTEXTMENU des menus de message et d’autres ressources
topic_type:
- apiref
api_name:
- WM_CONTEXTMENU
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff7764926709bfc8ab6aa95be330a9d45d38bc48
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509521"
---
# <a name="wm_contextmenu-message"></a><span data-ttu-id="c3387-104">\_Message WM CONTEXTMENU</span><span class="sxs-lookup"><span data-stu-id="c3387-104">WM\_CONTEXTMENU message</span></span>

<span data-ttu-id="c3387-105">Avertit une fenêtre que l’utilisateur souhaite afficher un menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="c3387-105">Notifies a window that the user desires a context menu to appear.</span></span>  <span data-ttu-id="c3387-106">Il se peut que l’utilisateur ait cliqué sur le bouton droit de la souris (clic droit) dans la fenêtre, appuyé sur MAJ + F10 ou appuyé sur la touche applications (touche de menu contextuel) disponible sur certains claviers.</span><span class="sxs-lookup"><span data-stu-id="c3387-106">The user may have clicked the right mouse button (right-clicked) in the window, pressed Shift+F10 or pressed the applications key (context menu key) available on some keyboards.</span></span>


```C++
#define WM_CONTEXTMENU                  0x007B
```



## <a name="parameters"></a><span data-ttu-id="c3387-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c3387-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3387-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c3387-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c3387-109">Handle vers la fenêtre dans laquelle l’utilisateur a cliqué avec le bouton droit de la souris.</span><span class="sxs-lookup"><span data-stu-id="c3387-109">A handle to the window in which the user right-clicked the mouse.</span></span> <span data-ttu-id="c3387-110">Il peut s’agir d’une fenêtre enfant de la fenêtre recevant le message.</span><span class="sxs-lookup"><span data-stu-id="c3387-110">This can be a child window of the window receiving the message.</span></span> <span data-ttu-id="c3387-111">Pour plus d’informations sur le traitement de ce message, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="c3387-111">For more information about processing this message, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="c3387-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c3387-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c3387-113">Le mot de poids faible spécifie la position horizontale du curseur, en coordonnées d’écran, au moment du clic de la souris.</span><span class="sxs-lookup"><span data-stu-id="c3387-113">The low-order word specifies the horizontal position of the cursor, in screen coordinates, at the time of the mouse click.</span></span>

<span data-ttu-id="c3387-114">Le mot de poids fort spécifie la position verticale du curseur, en coordonnées d’écran, au moment du clic de la souris.</span><span class="sxs-lookup"><span data-stu-id="c3387-114">The high-order word specifies the vertical position of the cursor, in screen coordinates, at the time of the mouse click.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3387-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c3387-115">Return value</span></span>

<span data-ttu-id="c3387-116">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="c3387-116">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3387-117">Notes</span><span class="sxs-lookup"><span data-stu-id="c3387-117">Remarks</span></span>

<span data-ttu-id="c3387-118">Une fenêtre peut traiter ce message en affichant un menu contextuel à l’aide des fonctions [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) ou [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) .</span><span class="sxs-lookup"><span data-stu-id="c3387-118">A window can process this message by displaying a shortcut menu using the [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) or [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) functions.</span></span> <span data-ttu-id="c3387-119">Pour obtenir les positions horizontale et verticale, utilisez le code suivant.</span><span class="sxs-lookup"><span data-stu-id="c3387-119">To obtain the horizontal and vertical positions, use the following code.</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



<span data-ttu-id="c3387-120">Si une fenêtre n’affiche pas de menu contextuel, elle doit transmettre ce message à la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="c3387-120">If a window does not display a shortcut menu it should pass this message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span> <span data-ttu-id="c3387-121">Si une fenêtre est une fenêtre enfant, **DefWindowProc** envoie le message au parent.</span><span class="sxs-lookup"><span data-stu-id="c3387-121">If a window is a child window, **DefWindowProc** sends the message to the parent.</span></span> <span data-ttu-id="c3387-122">Sinon, **DefWindowProc** affiche un menu contextuel par défaut si la position spécifiée se trouve dans la légende de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="c3387-122">Otherwise, **DefWindowProc** displays a default shortcut menu if the specified position is in the window's caption.</span></span>

<span data-ttu-id="c3387-123">[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) génère le message **WM \_ CONTEXTMENU** lorsqu’il traite le [**message \_ WM RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup) ou [**WM \_ NCRBUTTONUP**](/windows/desktop/inputdev/wm-ncrbuttonup) ou lorsque l’utilisateur tape Shift + F10.</span><span class="sxs-lookup"><span data-stu-id="c3387-123">[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) generates the **WM\_CONTEXTMENU** message when it processes the [**WM\_RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup) or [**WM\_NCRBUTTONUP**](/windows/desktop/inputdev/wm-ncrbuttonup) message or when the user types SHIFT+F10.</span></span> <span data-ttu-id="c3387-124">Le message **WM \_ CONTEXTMENU** est également généré quand l’utilisateur appuie sur la touche [**VK \_ apps**](/windows/desktop/inputdev/virtual-key-codes) et la libère.</span><span class="sxs-lookup"><span data-stu-id="c3387-124">The **WM\_CONTEXTMENU** message is also generated when the user presses and releases the [**VK\_APPS**](/windows/desktop/inputdev/virtual-key-codes) key.</span></span>

<span data-ttu-id="c3387-125">Si le menu contextuel est généré à partir du clavier, par exemple, si l’utilisateur tape MAJ + F10, les coordonnées x et y sont-1 et que l’application doit afficher le menu contextuel à l’emplacement de la sélection actuelle plutôt qu’à (xPos, yPos).</span><span class="sxs-lookup"><span data-stu-id="c3387-125">If the context menu is generated from the keyboard for example, if the user types SHIFT+F10 then the x- and y-coordinates are -1 and the application should display the context menu at the location of the current selection rather than at (xPos, yPos).</span></span>

## <a name="requirements"></a><span data-ttu-id="c3387-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c3387-126">Requirements</span></span>



| <span data-ttu-id="c3387-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c3387-127">Requirement</span></span> | <span data-ttu-id="c3387-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="c3387-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3387-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3387-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c3387-130">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c3387-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c3387-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3387-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c3387-132">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c3387-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c3387-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="c3387-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3387-134"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c3387-134"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3387-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c3387-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="c3387-136">**Référence**</span><span class="sxs-lookup"><span data-stu-id="c3387-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c3387-137">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="c3387-137">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="c3387-138">**Obtient \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="c3387-138">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="c3387-139">**Obtient \_ le \_ lParam Y**</span><span class="sxs-lookup"><span data-stu-id="c3387-139">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="c3387-140">**TrackPopupMenu**</span><span class="sxs-lookup"><span data-stu-id="c3387-140">**TrackPopupMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu)
</dt> <dt>

[<span data-ttu-id="c3387-141">**TrackPopupMenuEx**</span><span class="sxs-lookup"><span data-stu-id="c3387-141">**TrackPopupMenuEx**</span></span>](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex)
</dt> <dt>

[<span data-ttu-id="c3387-142">**\_NCRBUTTONUP WM**</span><span class="sxs-lookup"><span data-stu-id="c3387-142">**WM\_NCRBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-ncrbuttonup)
</dt> <dt>

[<span data-ttu-id="c3387-143">**\_RBUTTONUP WM**</span><span class="sxs-lookup"><span data-stu-id="c3387-143">**WM\_RBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-rbuttonup)
</dt> <dt>

<span data-ttu-id="c3387-144">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="c3387-144">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c3387-145">Menus</span><span class="sxs-lookup"><span data-stu-id="c3387-145">Menus</span></span>](menus.md)
</dt> </dl>

 

