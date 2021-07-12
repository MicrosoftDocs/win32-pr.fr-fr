---
description: Vous envoyez le message **WM_SETREDRAW** à une fenêtre pour autoriser le rafraîchissement des modifications de cette fenêtre, ou pour empêcher que les modifications apportées à cette fenêtre soient redessinées.
ms.assetid: 0085a55e-7bf6-4eb6-a649-832b685db1cc
title: Message WM_SETREDRAW (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1232833fc4465e2341541a0036af47fdd3b53393
ms.sourcegitcommit: e5d6fb49928cc8cea4ec77dce03b740d40076348
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/10/2021
ms.locfileid: "113593455"
---
# <a name="wm_setredraw-message"></a><span data-ttu-id="1767d-103">Message WM_SETREDRAW</span><span class="sxs-lookup"><span data-stu-id="1767d-103">WM_SETREDRAW message</span></span>

<span data-ttu-id="1767d-104">Vous envoyez le message **WM \_ SETREDRAW** à une fenêtre pour que les modifications apportées à cette fenêtre soient redessinées ou pour empêcher que les modifications apportées à cette fenêtre soient redessinées.</span><span class="sxs-lookup"><span data-stu-id="1767d-104">You send the **WM\_SETREDRAW** message to a window to allow changes in that window to be redrawn, or to prevent changes in that window from being redrawn.</span></span>

<span data-ttu-id="1767d-105">Pour envoyer ce message, appelez la fonction [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="1767d-105">To send this message, call the [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) function with the following parameters.</span></span>

```C++
SendMessage(
  (HWND) hWnd,
  WM_SETREDRAW,
  (WPARAM) wParam,
  (LPARAM) lParam
);
```

## <a name="parameters"></a><span data-ttu-id="1767d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1767d-106">Parameters</span></span>

`wParam`

<span data-ttu-id="1767d-107">État du redessin.</span><span class="sxs-lookup"><span data-stu-id="1767d-107">The redraw state.</span></span> <span data-ttu-id="1767d-108">Si ce paramètre a la **valeur true**, le contenu peut être redessiné après une modification.</span><span class="sxs-lookup"><span data-stu-id="1767d-108">If this parameter is **TRUE**, then the content can be redrawn after a change.</span></span> <span data-ttu-id="1767d-109">Si ce paramètre a la **valeur false**, le contenu ne peut pas être redessiné après une modification.</span><span class="sxs-lookup"><span data-stu-id="1767d-109">If this parameter is **FALSE**, then the content can't be redrawn after a change.</span></span>

`lParam`

<span data-ttu-id="1767d-110">Ce paramètre n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="1767d-110">This parameter isn't used.</span></span>

## <a name="return-value"></a><span data-ttu-id="1767d-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1767d-111">Return value</span></span>

<span data-ttu-id="1767d-112">Votre application doit retourner 0 si elle traite ce message.</span><span class="sxs-lookup"><span data-stu-id="1767d-112">Your application should return 0 if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="1767d-113">Notes</span><span class="sxs-lookup"><span data-stu-id="1767d-113">Remarks</span></span>

<span data-ttu-id="1767d-114">Ce message peut être utile si votre application doit ajouter plusieurs éléments à une zone de liste.</span><span class="sxs-lookup"><span data-stu-id="1767d-114">This message can be useful if your application must add several items to a list box.</span></span> <span data-ttu-id="1767d-115">Votre application peut appeler ce message avec *wParam* défini sur **false**, ajouter les éléments, puis appeler à nouveau le message avec *wParam* défini sur **true**.</span><span class="sxs-lookup"><span data-stu-id="1767d-115">Your application can call this message with *wParam* set to **FALSE**, add the items, and then call the message again with *wParam* set to **TRUE**.</span></span> <span data-ttu-id="1767d-116">Enfin, votre application peut appeler [**RedrawWindow**](/windows/win32/api/Winuser/nf-winuser-redrawwindow)(*HWND*, **null**, **null**, RDW \_ Erase \| RDW \_ frame \| RDW non \_ valide \| RDW \_ ALLCHILDREN) pour provoquer la redessination de la zone de liste.</span><span class="sxs-lookup"><span data-stu-id="1767d-116">Finally, your application can call [**RedrawWindow**](/windows/win32/api/Winuser/nf-winuser-redrawwindow)(*hWnd*, **NULL**, **NULL**, RDW\_ERASE \| RDW\_FRAME \| RDW\_INVALIDATE \| RDW\_ALLCHILDREN) to cause the list box to be repainted.</span></span>

> [!NOTE] 
> <span data-ttu-id="1767d-117">Vous devez utiliser [**RedrawWindow**](/windows/win32/api/Winuser/nf-winuser-redrawwindow) avec les indicateurs spécifiés, au lieu de [**InvalidateRect**](/windows/win32/api/Winuser/nf-winuser-invalidaterect), car le premier est nécessaire pour certains contrôles qui ont eux-mêmes une zone non cliente, ou qui ont des styles de fenêtre qui les empêchent de recevoir une zone non cliente (par exemple **WS_THICKFRAME**, **WS_BORDER** ou **WS_EX_CLIENTEDGE**).</span><span class="sxs-lookup"><span data-stu-id="1767d-117">You should use [**RedrawWindow**](/windows/win32/api/Winuser/nf-winuser-redrawwindow) with the specified flags, instead of [**InvalidateRect**](/windows/win32/api/Winuser/nf-winuser-invalidaterect), because the former is necessary for some controls that have nonclient area of their own, or have window styles that cause them to be given a nonclient area (such as **WS_THICKFRAME**, **WS_BORDER**, or **WS_EX_CLIENTEDGE**).</span></span> <span data-ttu-id="1767d-118">Si le contrôle n’a pas de zone non cliente, les **RedrawWindow** avec ces indicateurs effectuent uniquement la même invalidation que le nombre de **InvalidateRect** .</span><span class="sxs-lookup"><span data-stu-id="1767d-118">If the control does not have a nonclient area, then **RedrawWindow** with these flags will do only as much invalidation as **InvalidateRect** would.</span></span>

<span data-ttu-id="1767d-119">La transmission d’un message **WM_SETREDRAW** à la fonction **DefWindowProc** supprime le style **WS_VISIBLE** de la fenêtre lorsque *wParam* a la valeur **false**.</span><span class="sxs-lookup"><span data-stu-id="1767d-119">Passing a **WM_SETREDRAW** message to the **DefWindowProc** function removes the **WS_VISIBLE** style from the window when *wParam* is set to **FALSE**.</span></span> <span data-ttu-id="1767d-120">Bien que le contenu de la fenêtre reste visible à l’écran, la fonction [**IsWindowVisible**](/windows/win32/api/winuser/nf-winuser-iswindowvisible) retourne la **valeur false** lorsqu’elle est appelée sur une fenêtre dans cet État.</span><span class="sxs-lookup"><span data-stu-id="1767d-120">Although the window content remains visible on screen, the [**IsWindowVisible**](/windows/win32/api/winuser/nf-winuser-iswindowvisible) function returns **FALSE** when called on a window in this state.</span></span> 

<span data-ttu-id="1767d-121">La transmission d’un message **WM_SETREDRAW** à la fonction **DefWindowProc** ajoute le style **WS_VISIBLE** à la fenêtre, s’il n’est pas défini, lorsque *wParam* a la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="1767d-121">Passing a **WM_SETREDRAW** message to the **DefWindowProc** function adds the **WS_VISIBLE** style to the window, if not set, when *wParam* is set to **TRUE**.</span></span> <span data-ttu-id="1767d-122">Si votre application envoie le message d' **WM_SETREDRAW** avec *wParam* défini sur **true** dans une fenêtre masquée, la fenêtre devient visible.</span><span class="sxs-lookup"><span data-stu-id="1767d-122">If your application sends the **WM_SETREDRAW** message with *wParam* set to **TRUE** to a hidden window, then the window becomes visible.</span></span> 

<span data-ttu-id="1767d-123">**Windows 10 et versions ultérieures ; Windows Server 2016 et versions ultérieures**.</span><span class="sxs-lookup"><span data-stu-id="1767d-123">**Windows 10 and later; Windows Server 2016 and later**.</span></span> <span data-ttu-id="1767d-124">Le système définit une propriété nommée *SysSetRedraw* dans une fenêtre dont la procédure de fenêtre transmet **WM_SETREDRAW** messages à **DefWindowProc**.</span><span class="sxs-lookup"><span data-stu-id="1767d-124">The system sets a property named *SysSetRedraw* on a window whose window procedure passes **WM_SETREDRAW** messages to **DefWindowProc**.</span></span> <span data-ttu-id="1767d-125">Vous pouvez utiliser la fonction [**getprop**](/windows/win32/api/Winuser/nf-winuser-getpropa) pour récupérer la valeur de la propriété lorsqu’elle est disponible.</span><span class="sxs-lookup"><span data-stu-id="1767d-125">You can use the [**GetProp**](/windows/win32/api/Winuser/nf-winuser-getpropa) function to get the property value when it's available.</span></span> <span data-ttu-id="1767d-126">**Getprop** retourne une valeur différente de zéro quand redessin est désactivé.</span><span class="sxs-lookup"><span data-stu-id="1767d-126">**GetProp** returns a non-zero value when redraw is disabled.</span></span> <span data-ttu-id="1767d-127">**Getprop** retourne zéro lorsque redessin est activé, ou lorsque la propriété de fenêtre n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="1767d-127">**GetProp** will return zero when redraw is enabled, or when the window property doesn't exist.</span></span> 

## <a name="requirements"></a><span data-ttu-id="1767d-128">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1767d-128">Requirements</span></span>

| <span data-ttu-id="1767d-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1767d-129">Requirement</span></span> | <span data-ttu-id="1767d-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="1767d-130">Value</span></span> |
|-|-|
| <span data-ttu-id="1767d-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1767d-131">Minimum supported client</span></span> | <span data-ttu-id="1767d-132">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1767d-132">Windows 2000 Professional \[desktop apps only\]</span></span> |
| <span data-ttu-id="1767d-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1767d-133">Minimum supported server</span></span> | <span data-ttu-id="1767d-134">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1767d-134">Windows 2000 Server \[desktop apps only\]</span></span> |
| <span data-ttu-id="1767d-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="1767d-135">Header</span></span> | <dl><span data-ttu-id="1767d-136"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1767d-136"><dt>Winuser.h (include Windows.h)</dt></span></span></dl> |

## <a name="see-also"></a><span data-ttu-id="1767d-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1767d-137">See also</span></span>

* [<span data-ttu-id="1767d-138">Vue d’ensemble de la peinture et du dessin</span><span class="sxs-lookup"><span data-stu-id="1767d-138">Painting and drawing overview</span></span>](painting-and-drawing.md)
* [<span data-ttu-id="1767d-139">Peinture et dessin de messages</span><span class="sxs-lookup"><span data-stu-id="1767d-139">Painting and drawing messages</span></span>](painting-and-drawing-messages.md)
* [<span data-ttu-id="1767d-140">RedrawWindow</span><span class="sxs-lookup"><span data-stu-id="1767d-140">RedrawWindow</span></span>](/windows/win32/api/Winuser/nf-winuser-redrawwindow)
