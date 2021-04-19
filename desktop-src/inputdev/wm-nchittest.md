---
title: Message WM_NCHITTEST (winuser. h)
description: Envoyé à une fenêtre afin de déterminer quelle partie de la fenêtre correspond à une coordonnée d’écran particulière.
ms.assetid: 4c860466-a9f8-4af8-96b9-cee005481875
keywords:
- WM_NCHITTEST l’entrée du clavier et de la souris du message
topic_type:
- apiref
api_name:
- WM_NCHITTEST
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bf14e817831c099988e9fb3fee57ae0731ef621
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512567"
---
# <a name="wm_nchittest-message"></a><span data-ttu-id="7c380-104">\_Message WM NCHITTEST</span><span class="sxs-lookup"><span data-stu-id="7c380-104">WM\_NCHITTEST message</span></span>

<span data-ttu-id="7c380-105">Envoyé à une fenêtre afin de déterminer quelle partie de la fenêtre correspond à une coordonnée d’écran particulière.</span><span class="sxs-lookup"><span data-stu-id="7c380-105">Sent to a window in order to determine what part of the window corresponds to a particular screen coordinate.</span></span> <span data-ttu-id="7c380-106">Cela peut se produire, par exemple, lorsque le curseur se déplace, lorsqu’un bouton de la souris est enfoncé ou relâché, ou en réponse à un appel à une fonction telle que [**WindowFromPoint**](/windows/desktop/api/winuser/nf-winuser-windowfrompoint).</span><span class="sxs-lookup"><span data-stu-id="7c380-106">This can happen, for example, when the cursor moves, when a mouse button is pressed or released, or in response to a call to a function such as [**WindowFromPoint**](/windows/desktop/api/winuser/nf-winuser-windowfrompoint).</span></span> <span data-ttu-id="7c380-107">Si la souris n’est pas capturée, le message est envoyé à la fenêtre située sous le curseur.</span><span class="sxs-lookup"><span data-stu-id="7c380-107">If the mouse is not captured, the message is sent to the window beneath the cursor.</span></span> <span data-ttu-id="7c380-108">Dans le cas contraire, le message est envoyé à la fenêtre qui a capturé la souris.</span><span class="sxs-lookup"><span data-stu-id="7c380-108">Otherwise, the message is sent to the window that has captured the mouse.</span></span>

<span data-ttu-id="7c380-109">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="7c380-109">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCHITTEST                    0x0084
```



## <a name="parameters"></a><span data-ttu-id="7c380-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7c380-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c380-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7c380-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7c380-112">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="7c380-112">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7c380-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7c380-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7c380-114">Le mot de poids faible spécifie la coordonnée x du curseur.</span><span class="sxs-lookup"><span data-stu-id="7c380-114">The low-order word specifies the x-coordinate of the cursor.</span></span> <span data-ttu-id="7c380-115">La coordonnée est relative au coin supérieur gauche de l’écran.</span><span class="sxs-lookup"><span data-stu-id="7c380-115">The coordinate is relative to the upper-left corner of the screen.</span></span>

<span data-ttu-id="7c380-116">Le mot de poids fort spécifie la coordonnée y du curseur.</span><span class="sxs-lookup"><span data-stu-id="7c380-116">The high-order word specifies the y-coordinate of the cursor.</span></span> <span data-ttu-id="7c380-117">La coordonnée est relative au coin supérieur gauche de l’écran.</span><span class="sxs-lookup"><span data-stu-id="7c380-117">The coordinate is relative to the upper-left corner of the screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c380-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7c380-118">Return value</span></span>

<span data-ttu-id="7c380-119">La valeur de retour de la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) est l’une des valeurs suivantes, indiquant la position de la zone réactive du curseur.</span><span class="sxs-lookup"><span data-stu-id="7c380-119">The return value of the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function is one of the following values, indicating the position of the cursor hot spot.</span></span>



| <span data-ttu-id="7c380-120">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="7c380-120">Return code/value</span></span>                                                                                                                                    | <span data-ttu-id="7c380-121">Description</span><span class="sxs-lookup"><span data-stu-id="7c380-121">Description</span></span>                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7c380-122"><dt>**HTBORDER**</dt> <dt>18</dt></span><span class="sxs-lookup"><span data-stu-id="7c380-122"><dt>**HTBORDER**</dt> <dt>18</dt></span></span> </dl>      | <span data-ttu-id="7c380-123">Dans la bordure d’une fenêtre qui n’a pas de bordure de redimensionnement.</span><span class="sxs-lookup"><span data-stu-id="7c380-123">In the border of a window that does not have a sizing border.</span></span><br/>                                                                                                                                           |
| <dl> <span data-ttu-id="7c380-124"><dt>**HTBOTTOM**</dt> <dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="7c380-124"><dt>**HTBOTTOM**</dt> <dt>15</dt></span></span> </dl>      | <span data-ttu-id="7c380-125">Dans la bordure inférieure horizontale d’une fenêtre redimensionnable (l’utilisateur peut cliquer sur la souris pour redimensionner la fenêtre verticalement).</span><span class="sxs-lookup"><span data-stu-id="7c380-125">In the lower-horizontal border of a resizable window (the user can click the mouse to resize the window vertically).</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="7c380-126"><dt>**HTBOTTOMLEFT**</dt> <dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="7c380-126"><dt>**HTBOTTOMLEFT**</dt> <dt>16</dt></span></span> </dl>  | <span data-ttu-id="7c380-127">Dans le coin inférieur gauche d’une bordure d’une fenêtre redimensionnable (l’utilisateur peut cliquer sur la souris pour redimensionner la fenêtre en diagonale).</span><span class="sxs-lookup"><span data-stu-id="7c380-127">In the lower-left corner of a border of a resizable window (the user can click the mouse to resize the window diagonally).</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="7c380-128"><dt>**HTBOTTOMRIGHT**</dt> <dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="7c380-128"><dt>**HTBOTTOMRIGHT**</dt> <dt>17</dt></span></span> </dl> | <span data-ttu-id="7c380-129">Dans le coin inférieur droit d’une bordure d’une fenêtre redimensionnable (l’utilisateur peut cliquer sur la souris pour redimensionner la fenêtre en diagonale).</span><span class="sxs-lookup"><span data-stu-id="7c380-129">In the lower-right corner of a border of a resizable window (the user can click the mouse to resize the window diagonally).</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="7c380-130"><dt>**HTCAPTION**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="7c380-130"><dt>**HTCAPTION**</dt> <dt>2</dt></span></span> </dl>      | <span data-ttu-id="7c380-131">Dans une barre de titre.</span><span class="sxs-lookup"><span data-stu-id="7c380-131">In a title bar.</span></span><br/>                                                                                                                                                                                         |
| <dl> <span data-ttu-id="7c380-132"><dt>**HTCLIENT**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="7c380-132"><dt>**HTCLIENT**</dt> <dt>1</dt></span></span> </dl>       | <span data-ttu-id="7c380-133">Dans une zone cliente.</span><span class="sxs-lookup"><span data-stu-id="7c380-133">In a client area.</span></span><br/>                                                                                                                                                                                       |
| <dl> <span data-ttu-id="7c380-134"><dt>**HTCLOSE**</dt> <dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="7c380-134"><dt>**HTCLOSE**</dt> <dt>20</dt></span></span> </dl>       | <span data-ttu-id="7c380-135">Dans un bouton **Fermer** .</span><span class="sxs-lookup"><span data-stu-id="7c380-135">In a **Close** button.</span></span><br/>                                                                                                                                                                                  |
| <dl> <span data-ttu-id="7c380-136"><dt>**HTERROR**</dt> <dt>-2</dt></span><span class="sxs-lookup"><span data-stu-id="7c380-136"><dt>**HTERROR**</dt> <dt>-2</dt></span></span> </dl>       | <span data-ttu-id="7c380-137">Sur l’arrière-plan de l’écran ou sur une ligne de séparation entre les fenêtres (identique à **HTNOWHERE**, sauf que la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) génère un bip système pour indiquer une erreur).</span><span class="sxs-lookup"><span data-stu-id="7c380-137">On the screen background or on a dividing line between windows (same as **HTNOWHERE**, except that the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function produces a system beep to indicate an error).</span></span><br/> |
| <dl> <span data-ttu-id="7c380-138"><dt>**HTGROWBOX**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="7c380-138"><dt>**HTGROWBOX**</dt> <dt>4</dt></span></span> </dl>      | <span data-ttu-id="7c380-139">Dans une zone de taille (identique à **HTSIZE**).</span><span class="sxs-lookup"><span data-stu-id="7c380-139">In a size box (same as **HTSIZE**).</span></span><br/>                                                                                                                                                                     |
| <dl> <span data-ttu-id="7c380-140"><dt>**HTHELP**</dt> <dt>21</dt></span><span class="sxs-lookup"><span data-stu-id="7c380-140"><dt>**HTHELP**</dt> <dt>21</dt></span></span> </dl>        | <span data-ttu-id="7c380-141">Dans un bouton **d’aide** .</span><span class="sxs-lookup"><span data-stu-id="7c380-141">In a **Help** button.</span></span><br/>                                                                                                                                                                                   |
| <dl> <span data-ttu-id="7c380-142"><dt>**HTHSCROLL**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="7c380-142"><dt>**HTHSCROLL**</dt> <dt>6</dt></span></span> </dl>      | <span data-ttu-id="7c380-143">Dans une barre de défilement horizontale.</span><span class="sxs-lookup"><span data-stu-id="7c380-143">In a horizontal scroll bar.</span></span><br/>                                                                                                                                                                             |
| <dl> <span data-ttu-id="7c380-144"><dt>**HTLEFT**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="7c380-144"><dt>**HTLEFT**</dt> <dt>10</dt></span></span> </dl>        | <span data-ttu-id="7c380-145">Dans la bordure gauche d’une fenêtre redimensionnable (l’utilisateur peut cliquer sur la souris pour redimensionner la fenêtre horizontalement).</span><span class="sxs-lookup"><span data-stu-id="7c380-145">In the left border of a resizable window (the user can click the mouse to resize the window horizontally).</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="7c380-146"><dt>**HTMENU**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="7c380-146"><dt>**HTMENU**</dt> <dt>5</dt></span></span> </dl>         | <span data-ttu-id="7c380-147">Dans un menu.</span><span class="sxs-lookup"><span data-stu-id="7c380-147">In a menu.</span></span><br/>                                                                                                                                                                                              |
| <dl> <span data-ttu-id="7c380-148"><dt>**HTMAXBUTTON**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="7c380-148"><dt>**HTMAXBUTTON**</dt> <dt>9</dt></span></span> </dl>    | <span data-ttu-id="7c380-149">Dans un bouton **agrandir** .</span><span class="sxs-lookup"><span data-stu-id="7c380-149">In a **Maximize** button.</span></span><br/>                                                                                                                                                                               |
| <dl> <span data-ttu-id="7c380-150"><dt>**HTMINBUTTON**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="7c380-150"><dt>**HTMINBUTTON**</dt> <dt>8</dt></span></span> </dl>    | <span data-ttu-id="7c380-151">Dans un bouton **réduire** .</span><span class="sxs-lookup"><span data-stu-id="7c380-151">In a **Minimize** button.</span></span><br/>                                                                                                                                                                               |
| <dl> <span data-ttu-id="7c380-152"><dt>**HTNOWHERE**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7c380-152"><dt>**HTNOWHERE**</dt> <dt>0</dt></span></span> </dl>      | <span data-ttu-id="7c380-153">Sur l’arrière-plan de l’écran ou sur une ligne de séparation entre les fenêtres.</span><span class="sxs-lookup"><span data-stu-id="7c380-153">On the screen background or on a dividing line between windows.</span></span><br/>                                                                                                                                         |
| <dl> <span data-ttu-id="7c380-154"><dt>**HTREDUCE**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="7c380-154"><dt>**HTREDUCE**</dt> <dt>8</dt></span></span> </dl>       | <span data-ttu-id="7c380-155">Dans un bouton **réduire** .</span><span class="sxs-lookup"><span data-stu-id="7c380-155">In a **Minimize** button.</span></span><br/>                                                                                                                                                                               |
| <dl> <span data-ttu-id="7c380-156"><dt>**HTRIGHT**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="7c380-156"><dt>**HTRIGHT**</dt> <dt>11</dt></span></span> </dl>       | <span data-ttu-id="7c380-157">Dans la bordure droite d’une fenêtre redimensionnable (l’utilisateur peut cliquer sur la souris pour redimensionner la fenêtre horizontalement).</span><span class="sxs-lookup"><span data-stu-id="7c380-157">In the right border of a resizable window (the user can click the mouse to resize the window horizontally).</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="7c380-158"><dt>**HTSIZE**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="7c380-158"><dt>**HTSIZE**</dt> <dt>4</dt></span></span> </dl>         | <span data-ttu-id="7c380-159">Dans une zone de taille (identique à **HTGROWBOX**).</span><span class="sxs-lookup"><span data-stu-id="7c380-159">In a size box (same as **HTGROWBOX**).</span></span><br/>                                                                                                                                                                  |
| <dl> <span data-ttu-id="7c380-160"><dt>**HTSYSMENU**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="7c380-160"><dt>**HTSYSMENU**</dt> <dt>3</dt></span></span> </dl>      | <span data-ttu-id="7c380-161">Dans un menu fenêtre ou dans un bouton **Fermer** dans une fenêtre enfant.</span><span class="sxs-lookup"><span data-stu-id="7c380-161">In a window menu or in a **Close** button in a child window.</span></span><br/>                                                                                                                                            |
| <dl> <span data-ttu-id="7c380-162"><dt>**HTTOP**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="7c380-162"><dt>**HTTOP**</dt> <dt>12</dt></span></span> </dl>         | <span data-ttu-id="7c380-163">Dans la bordure supérieure horizontale d’une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="7c380-163">In the upper-horizontal border of a window.</span></span><br/>                                                                                                                                                             |
| <dl> <span data-ttu-id="7c380-164"><dt>**HTTOPLEFT**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="7c380-164"><dt>**HTTOPLEFT**</dt> <dt>13</dt></span></span> </dl>     | <span data-ttu-id="7c380-165">Dans l’angle supérieur gauche d’une bordure de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="7c380-165">In the upper-left corner of a window border.</span></span><br/>                                                                                                                                                            |
| <dl> <span data-ttu-id="7c380-166"><dt>**HTTOPRIGHT**</dt> <dt>14</dt></span><span class="sxs-lookup"><span data-stu-id="7c380-166"><dt>**HTTOPRIGHT**</dt> <dt>14</dt></span></span> </dl>    | <span data-ttu-id="7c380-167">Dans l’angle supérieur droit d’une bordure de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="7c380-167">In the upper-right corner of a window border.</span></span><br/>                                                                                                                                                           |
| <dl> <span data-ttu-id="7c380-168"><dt>**HTTRANSPARENT**</dt> <dt>-1</dt></span><span class="sxs-lookup"><span data-stu-id="7c380-168"><dt>**HTTRANSPARENT**</dt> <dt>-1</dt></span></span> </dl> | <span data-ttu-id="7c380-169">Dans une fenêtre actuellement couverte par une autre fenêtre dans le même thread (le message est envoyé aux fenêtres sous-jacentes dans le même thread jusqu’à ce que l’un d’eux retourne un code qui n’est pas **HTTRANSPARENT**).</span><span class="sxs-lookup"><span data-stu-id="7c380-169">In a window currently covered by another window in the same thread (the message will be sent to underlying windows in the same thread until one of them returns a code that is not **HTTRANSPARENT**).</span></span><br/>  |
| <dl> <span data-ttu-id="7c380-170"><dt>**HTVSCROLL**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="7c380-170"><dt>**HTVSCROLL**</dt> <dt>7</dt></span></span> </dl>      | <span data-ttu-id="7c380-171">Dans la barre de défilement verticale.</span><span class="sxs-lookup"><span data-stu-id="7c380-171">In the vertical scroll bar.</span></span><br/>                                                                                                                                                                             |
| <dl> <span data-ttu-id="7c380-172"><dt>**HTZOOM**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="7c380-172"><dt>**HTZOOM**</dt> <dt>9</dt></span></span> </dl>         | <span data-ttu-id="7c380-173">Dans un bouton **agrandir** .</span><span class="sxs-lookup"><span data-stu-id="7c380-173">In a **Maximize** button.</span></span><br/>                                                                                                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="7c380-174">Notes</span><span class="sxs-lookup"><span data-stu-id="7c380-174">Remarks</span></span>

<span data-ttu-id="7c380-175">Utilisez le code suivant pour obtenir la position horizontale et verticale :</span><span class="sxs-lookup"><span data-stu-id="7c380-175">Use the following code to obtain the horizontal and vertical position:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam);
```



<span data-ttu-id="7c380-176">Comme indiqué ci-dessus, la coordonnée x est dans le sens le **plus** bas de la valeur de retour ; la coordonnée y est dans le sens le **plus** élevé (les deux représentent des valeurs *signées* , car elles peuvent accepter des valeurs négatives sur les systèmes avec plusieurs analyses).</span><span class="sxs-lookup"><span data-stu-id="7c380-176">As noted above, the x-coordinate is in the low-order **short** of the return value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="7c380-177">Si la valeur de retour est assignée à une variable, vous pouvez utiliser la macro [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) pour obtenir une structure de [**points**](/previous-versions//dd162808(v=vs.85)) à partir de la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="7c380-177">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="7c380-178">Vous pouvez également utiliser la macro [**obten \_ x \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) ou [**obten \_ Y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) pour extraire la coordonnée x ou y.</span><span class="sxs-lookup"><span data-stu-id="7c380-178">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7c380-179">N’utilisez pas les macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ou [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) pour extraire les coordonnées x et y de la position du curseur, car ces macros renvoient des résultats incorrects sur les systèmes avec plusieurs moniteurs.</span><span class="sxs-lookup"><span data-stu-id="7c380-179">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="7c380-180">Les systèmes avec plusieurs moniteurs peuvent avoir des coordonnées x et y négatives, et **LOWORD** et **HIWORD** traitent les coordonnées comme des quantités non signées.</span><span class="sxs-lookup"><span data-stu-id="7c380-180">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="7c380-181">**Windows Vista :** Lorsque vous créez des frames personnalisés qui incluent les boutons de légende standard, ce message doit d’abord être transmis à la fonction [**DwmDefWindowProc**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmdefwindowproc) .</span><span class="sxs-lookup"><span data-stu-id="7c380-181">**Windows Vista:** When creating custom frames that include the standard caption buttons, this message should first be passed to the [**DwmDefWindowProc**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmdefwindowproc) function.</span></span> <span data-ttu-id="7c380-182">Cela permet à l’Gestionnaire de fenêtrage (DWM) de fournir des tests de positionnement pour les boutons de légende.</span><span class="sxs-lookup"><span data-stu-id="7c380-182">This enables the Desktop Window Manager (DWM) to provide hit-testing for the captions buttons.</span></span> <span data-ttu-id="7c380-183">Si **DwmDefWindowProc** ne gère pas le message, un traitement supplémentaire de **WM \_ NCHITTEST** peut être nécessaire.</span><span class="sxs-lookup"><span data-stu-id="7c380-183">If **DwmDefWindowProc** does not handle the message, further processing of **WM\_NCHITTEST** may be needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c380-184">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7c380-184">Requirements</span></span>



| <span data-ttu-id="7c380-185">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7c380-185">Requirement</span></span> | <span data-ttu-id="7c380-186">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c380-186">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c380-187">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c380-187">Minimum supported client</span></span><br/> | <span data-ttu-id="7c380-188">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7c380-188">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="7c380-189">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c380-189">Minimum supported server</span></span><br/> | <span data-ttu-id="7c380-190">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7c380-190">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="7c380-191">En-tête</span><span class="sxs-lookup"><span data-stu-id="7c380-191">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c380-192"><dt>Winuser. h (inclure Windowsx. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7c380-192"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c380-193">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7c380-193">See also</span></span>

<dl> <dt>

<span data-ttu-id="7c380-194">**Référence**</span><span class="sxs-lookup"><span data-stu-id="7c380-194">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7c380-195">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="7c380-195">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="7c380-196">**Obtient \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="7c380-196">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="7c380-197">**Obtient \_ le \_ lParam Y**</span><span class="sxs-lookup"><span data-stu-id="7c380-197">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

<span data-ttu-id="7c380-198">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="7c380-198">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7c380-199">Entrée de la souris</span><span class="sxs-lookup"><span data-stu-id="7c380-199">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="7c380-200">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="7c380-200">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="7c380-201">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="7c380-201">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="7c380-202">[**MOMENTS**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7c380-202">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

