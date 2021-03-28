---
description: Une application envoie le \_ message WM SETREDRAW à une fenêtre pour autoriser le rafraîchissement des modifications apportées à cette fenêtre ou empêcher le rafraîchissement des modifications apportées à cette fenêtre.
ms.assetid: 0085a55e-7bf6-4eb6-a649-832b685db1cc
title: Message WM_SETREDRAW (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 184401e70c8233b03c57db4f8a01bbd6a42e1a35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203877"
---
# <a name="wm_setredraw-message"></a><span data-ttu-id="1b030-103">\_Message WM SETREDRAW</span><span class="sxs-lookup"><span data-stu-id="1b030-103">WM\_SETREDRAW message</span></span>

<span data-ttu-id="1b030-104">Une application envoie le message **WM \_ SETREDRAW** à une fenêtre pour autoriser le rafraîchissement des modifications apportées à cette fenêtre ou empêcher le rafraîchissement des modifications apportées à cette fenêtre.</span><span class="sxs-lookup"><span data-stu-id="1b030-104">An application sends the **WM\_SETREDRAW** message to a window to allow changes in that window to be redrawn or to prevent changes in that window from being redrawn.</span></span>

<span data-ttu-id="1b030-105">Pour envoyer ce message, appelez la fonction [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="1b030-105">To send this message, call the [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) function with the following parameters.</span></span>


```C++
SendMessage( 
  (HWND) hWnd,              
  WM_SETREDRAW,             
  (WPARAM) wParam,          
  (LPARAM) lParam            
);
```



## <a name="parameters"></a><span data-ttu-id="1b030-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1b030-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b030-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1b030-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1b030-108">État du redessin.</span><span class="sxs-lookup"><span data-stu-id="1b030-108">The redraw state.</span></span> <span data-ttu-id="1b030-109">Si ce paramètre a la **valeur true**, le contenu peut être redessiné après une modification.</span><span class="sxs-lookup"><span data-stu-id="1b030-109">If this parameter is **TRUE**, the content can be redrawn after a change.</span></span> <span data-ttu-id="1b030-110">Si ce paramètre a la **valeur false**, le contenu ne peut pas être redessiné après une modification.</span><span class="sxs-lookup"><span data-stu-id="1b030-110">If this parameter is **FALSE**, the content cannot be redrawn after a change.</span></span>

</dd> <dt>

<span data-ttu-id="1b030-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1b030-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1b030-112">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="1b030-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b030-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1b030-113">Return value</span></span>

<span data-ttu-id="1b030-114">Une application retourne la valeur zéro si elle traite ce message.</span><span class="sxs-lookup"><span data-stu-id="1b030-114">An application returns zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b030-115">Notes</span><span class="sxs-lookup"><span data-stu-id="1b030-115">Remarks</span></span>

<span data-ttu-id="1b030-116">Ce message peut être utile si une application doit ajouter plusieurs éléments à une zone de liste.</span><span class="sxs-lookup"><span data-stu-id="1b030-116">This message can be useful if an application must add several items to a list box.</span></span> <span data-ttu-id="1b030-117">L’application peut appeler ce message avec *wParam* défini sur **false**, ajouter les éléments, puis appeler à nouveau le message avec *wParam* défini sur **true**.</span><span class="sxs-lookup"><span data-stu-id="1b030-117">The application can call this message with *wParam* set to **FALSE**, add the items, and then call the message again with *wParam* set to **TRUE**.</span></span> <span data-ttu-id="1b030-118">Enfin, l’application peut appeler [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow)(*HWND*, **null**, **null**, RDW \_ Erase \| RDW \_ frame \| RDW non \_ valide \| RDW \_ ALLCHILDREN) pour provoquer la redessination de la zone de liste.</span><span class="sxs-lookup"><span data-stu-id="1b030-118">Finally, the application can call [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow)(*hWnd*, **NULL**, **NULL**, RDW\_ERASE \| RDW\_FRAME \| RDW\_INVALIDATE \| RDW\_ALLCHILDREN) to cause the list box to be repainted.</span></span>

> [!Note]  
> <span data-ttu-id="1b030-119">[**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) avec les indicateurs spécifiés est utilisé à la place de [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) , car le premier est nécessaire pour certains contrôles qui ont eux-mêmes une zone non cliente, ou qui ont des styles de fenêtre qui les empêchent de recevoir une zone non cliente (par exemple, **WS \_ THICKFRAME**, **WS \_ Border** ou **WS \_ ex \_ CLIENTEDGE**).</span><span class="sxs-lookup"><span data-stu-id="1b030-119">[**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) with the specified flags is used instead of [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) because the former is necessary for some controls that have nonclient area on their own, or have window styles that cause them to be given a nonclient area (such as **WS\_THICKFRAME**, **WS\_BORDER**, or **WS\_EX\_CLIENTEDGE**).</span></span> <span data-ttu-id="1b030-120">Si le contrôle n’a pas de zone non cliente, **RedrawWindow** avec ces indicateurs n’effectuera qu’un maximum d’invalidation, comme le ferait **InvalidateRect** .</span><span class="sxs-lookup"><span data-stu-id="1b030-120">If the control does not have a nonclient area, **RedrawWindow** with these flags will do only as much invalidation as **InvalidateRect** would.</span></span>

 

<span data-ttu-id="1b030-121">Si l’application envoie le message **WM \_ SETREDRAW** à une fenêtre masquée, la fenêtre devient visible (autrement dit, le système d’exploitation ajoute le style **WS \_ visible** à la fenêtre).</span><span class="sxs-lookup"><span data-stu-id="1b030-121">If the application sends the **WM\_SETREDRAW** message to a hidden window, the window becomes visible (that is, the operating system adds the **WS\_VISIBLE** style to the window).</span></span>

## <a name="requirements"></a><span data-ttu-id="1b030-122">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1b030-122">Requirements</span></span>



| <span data-ttu-id="1b030-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1b030-123">Requirement</span></span> | <span data-ttu-id="1b030-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="1b030-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b030-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1b030-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1b030-126">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1b030-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="1b030-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1b030-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1b030-128">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1b030-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1b030-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="1b030-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b030-130"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1b030-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b030-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1b030-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b030-132">Vue d’ensemble de la peinture et du dessin</span><span class="sxs-lookup"><span data-stu-id="1b030-132">Painting and Drawing Overview</span></span>](painting-and-drawing.md)
</dt> <dt>

[<span data-ttu-id="1b030-133">Peinture et dessin de messages</span><span class="sxs-lookup"><span data-stu-id="1b030-133">Painting and Drawing Messages</span></span>](painting-and-drawing-messages.md)
</dt> <dt>

[<span data-ttu-id="1b030-134">**RedrawWindow**</span><span class="sxs-lookup"><span data-stu-id="1b030-134">**RedrawWindow**</span></span>](/windows/desktop/api/Winuser/nf-winuser-redrawwindow)
</dt> </dl>

 

 
