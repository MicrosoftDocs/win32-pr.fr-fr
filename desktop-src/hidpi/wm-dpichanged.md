---
title: Message WM_DPICHANGED (WinUser. h)
description: Envoyé lorsque les points effectifs par pouce (dpi) d’une fenêtre ont été modifiés.
ms.assetid: 97C458F2-89CD-45FF-ABEE-F158A3BCE0B8
keywords:
- WM_DPICHANGED message haute résolution
topic_type:
- apiref
api_name:
- WM_DPICHANGED
api_location:
- WinUser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aafbce1e784e1f205f0d32e045785125c1fb5aaa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741836"
---
# <a name="wm_dpichanged-message"></a><span data-ttu-id="5c964-104">\_Message WM DPICHANGED</span><span class="sxs-lookup"><span data-stu-id="5c964-104">WM\_DPICHANGED message</span></span>

<span data-ttu-id="5c964-105">Envoyé lorsque les points effectifs par pouce (dpi) d’une fenêtre ont été modifiés.</span><span class="sxs-lookup"><span data-stu-id="5c964-105">Sent when the effective dots per inch (dpi) for a window has changed.</span></span> <span data-ttu-id="5c964-106">La résolution PPP est le facteur d’échelle d’une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="5c964-106">The DPI is the scale factor for a window.</span></span> <span data-ttu-id="5c964-107">Plusieurs événements peuvent entraîner la modification de la résolution PPP.</span><span class="sxs-lookup"><span data-stu-id="5c964-107">There are multiple events that can cause the DPI to change.</span></span> <span data-ttu-id="5c964-108">La liste suivante indique les causes possibles de la modification de PPP.</span><span class="sxs-lookup"><span data-stu-id="5c964-108">The following list indicates the possible causes for the change in DPI.</span></span>

-   <span data-ttu-id="5c964-109">La fenêtre est déplacée vers une nouvelle analyse qui a une résolution différente.</span><span class="sxs-lookup"><span data-stu-id="5c964-109">The window is moved to a new monitor that has a different DPI.</span></span>
-   <span data-ttu-id="5c964-110">La résolution du moniteur qui héberge la fenêtre change.</span><span class="sxs-lookup"><span data-stu-id="5c964-110">The DPI of the monitor hosting the window changes.</span></span>

<span data-ttu-id="5c964-111">La valeur PPP actuelle d’une fenêtre est toujours égale à la dernière DPI envoyée par **WM \_ DPICHANGED**.</span><span class="sxs-lookup"><span data-stu-id="5c964-111">The current DPI for a window always equals the last DPI sent by **WM\_DPICHANGED**.</span></span> <span data-ttu-id="5c964-112">Il s’agit du facteur d’échelle auquel la fenêtre doit être mise à l’échelle pour les threads qui prennent en charge les modifications PPP.</span><span class="sxs-lookup"><span data-stu-id="5c964-112">This is the scale factor that the window should be scaling to for threads that are aware of DPI changes.</span></span>


```C++
#define WM_DPICHANGED       0x02E0
```



## <a name="parameters"></a><span data-ttu-id="5c964-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5c964-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c964-114">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5c964-114">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5c964-115">Le [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) du *wParam* contient la valeur de l’axe Y de la nouvelle résolution PPP de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="5c964-115">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) of the *wParam* contains the Y-axis value of the new dpi of the window.</span></span> <span data-ttu-id="5c964-116">Le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) du *wParam* contient la valeur de l’axe X de la nouvelle résolution PPP de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="5c964-116">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) of the *wParam* contains the X-axis value of the new DPI of the window.</span></span> <span data-ttu-id="5c964-117">Par exemple, 96, 120, 144 ou 192.</span><span class="sxs-lookup"><span data-stu-id="5c964-117">For example, 96, 120, 144, or 192.</span></span> <span data-ttu-id="5c964-118">Les valeurs de l’axe des X et de l’axe des Y sont identiques pour les applications Windows.</span><span class="sxs-lookup"><span data-stu-id="5c964-118">The values of the X-axis and the Y-axis are identical for Windows apps.</span></span>

</dd> <dt>

<span data-ttu-id="5c964-119">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5c964-119">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5c964-120">Pointeur vers une structure [**Rect**](/windows/desktop/api/windef/ns-windef-rect) qui fournit une taille et une position suggérées de la fenêtre active mise à l’échelle pour la nouvelle résolution.</span><span class="sxs-lookup"><span data-stu-id="5c964-120">A pointer to a [**RECT**](/windows/desktop/api/windef/ns-windef-rect) structure that provides a suggested size and position of the current window scaled for the new DPI.</span></span> <span data-ttu-id="5c964-121">Dans l’attente, les applications repositionneront et redimensionneront les fenêtres en fonction des suggestions fournies par *lParam* lors du traitement de ce message.</span><span class="sxs-lookup"><span data-stu-id="5c964-121">The expectation is that apps will reposition and resize windows based on the suggestions provided by *lParam* when handling this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c964-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5c964-122">Return value</span></span>

<span data-ttu-id="5c964-123">Si une application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="5c964-123">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c964-124">Notes</span><span class="sxs-lookup"><span data-stu-id="5c964-124">Remarks</span></span>

<span data-ttu-id="5c964-125">Ce message concerne uniquement les applications **\_ prenant en \_ \_ \_ charge la résolution par moniteur** ou la prise en charge **dpi par threads \_ \_ \_ \_ sensibles** à l’analyse.</span><span class="sxs-lookup"><span data-stu-id="5c964-125">This message is only relevant for **PROCESS\_PER\_MONITOR\_DPI\_AWARE** applications or **DPI\_AWARENESS\_PER\_MONITOR\_AWARE** threads.</span></span> <span data-ttu-id="5c964-126">Il peut être reçu sur certaines modifications PPP si la fenêtre ou le processus de niveau supérieur s’exécute avec une prise en charge **dpi** ou si le système prend en **charge** les DPI, mais dans ce cas, il peut être ignoré en toute sécurité.</span><span class="sxs-lookup"><span data-stu-id="5c964-126">It may be received on certain DPI changes if your top-level window or process is running as **DPI unaware** or **system DPI aware**, but in those situations it can be safely ignored.</span></span> <span data-ttu-id="5c964-127">Pour plus d’informations sur les différents types de reconnaissance, [**consultez \_ \_ prise**](/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-process_dpi_awareness) en la reconnaissance de la résolution des processus et [**\_ prise en dpi**](/windows/desktop/api/windef/ne-windef-dpi_awareness).</span><span class="sxs-lookup"><span data-stu-id="5c964-127">For more information about the different types of awareness, see [**PROCESS\_DPI\_AWARENESS**](/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-process_dpi_awareness) and [**DPI\_AWARENESS**](/windows/desktop/api/windef/ne-windef-dpi_awareness).</span></span> <span data-ttu-id="5c964-128">Les versions antérieures de Windows nécessitaient une reconnaissance DPI pour être liées au niveau d’une application.</span><span class="sxs-lookup"><span data-stu-id="5c964-128">Older versions of Windows required DPI awareness to be tied at the level of an application.</span></span> <span data-ttu-id="5c964-129">Ces applications utilisent **la \_ \_ reconnaissance des PPP de processus**.</span><span class="sxs-lookup"><span data-stu-id="5c964-129">Those apps use **PROCESS\_DPI\_AWARENESS**.</span></span> <span data-ttu-id="5c964-130">Actuellement, la reconnaissance DPI est liée aux threads et aux fenêtres individuelles plutôt qu’à l’ensemble de l’application.</span><span class="sxs-lookup"><span data-stu-id="5c964-130">Currently, DPI awareness is tied to threads and individual windows rather than the entire application.</span></span> <span data-ttu-id="5c964-131">Ces applications utilisent **la \_ reconnaissance dpi**.</span><span class="sxs-lookup"><span data-stu-id="5c964-131">These apps use **DPI\_AWARENESS**.</span></span>

<span data-ttu-id="5c964-132">Vous devez uniquement utiliser l’axe des X ou la valeur de l’axe des Y lors de la mise à l’échelle de votre application, car elles sont identiques.</span><span class="sxs-lookup"><span data-stu-id="5c964-132">You only need to use either the X-axis or the Y-axis value when scaling your application since they are the same.</span></span>

<span data-ttu-id="5c964-133">Pour gérer correctement ce message, vous devez redimensionner et repositionner votre fenêtre en fonction des suggestions fournies par *lParam* et à l’aide de [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos).</span><span class="sxs-lookup"><span data-stu-id="5c964-133">In order to handle this message correctly, you will need to resize and reposition your window based on the suggestions provided by *lParam* and using [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos).</span></span> <span data-ttu-id="5c964-134">Si vous ne le faites pas, votre fenêtre augmente ou diminue par rapport à tout le reste sur le nouvel écran.</span><span class="sxs-lookup"><span data-stu-id="5c964-134">If you do not do this, your window will grow or shrink with respect to everything else on the new monitor.</span></span> <span data-ttu-id="5c964-135">Par exemple, si un utilisateur utilise plusieurs moniteurs et fait glisser votre fenêtre d’un moniteur 96 ppp vers une analyse 192 PPP, votre fenêtre apparaîtra en moitié aussi importante que d’autres éléments sur le moniteur de 192 PPP.</span><span class="sxs-lookup"><span data-stu-id="5c964-135">For example, if a user is using multiple monitors and drags your window from a 96 DPI monitor to a 192 DPI monitor, your window will appear to be half as large with respect to other items on the 192 DPI monitor.</span></span>

<span data-ttu-id="5c964-136">La valeur de base de DPI est définie en tant que **\_ \_ \_ dpi d’écran par défaut** de l’utilisateur, qui est défini sur 96.</span><span class="sxs-lookup"><span data-stu-id="5c964-136">The base value of DPI is defined as **USER\_DEFAULT\_SCREEN\_DPI** which is set to 96.</span></span> <span data-ttu-id="5c964-137">Pour déterminer le facteur de mise à l’échelle d’une analyse, prenez la valeur PPP et divisez par la valeur **\_ \_ \_ PPP d’écran par défaut** de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5c964-137">To determine the scaling factor for a monitor, take the DPI value and divide by **USER\_DEFAULT\_SCREEN\_DPI**.</span></span> <span data-ttu-id="5c964-138">Le tableau suivant fournit des exemples de valeurs PPP et les facteurs de mise à l’échelle associés.</span><span class="sxs-lookup"><span data-stu-id="5c964-138">The following table provides some sample DPI values and associated scaling factors.</span></span>



| <span data-ttu-id="5c964-139">Valeur DPI</span><span class="sxs-lookup"><span data-stu-id="5c964-139">DPI value</span></span> | <span data-ttu-id="5c964-140">Pourcentage de mise à l’échelle</span><span class="sxs-lookup"><span data-stu-id="5c964-140">Scaling percentage</span></span> |
|-----------|--------------------|
| <span data-ttu-id="5c964-141">96</span><span class="sxs-lookup"><span data-stu-id="5c964-141">96</span></span>        | <span data-ttu-id="5c964-142">100 %</span><span class="sxs-lookup"><span data-stu-id="5c964-142">100%</span></span>               |
| <span data-ttu-id="5c964-143">120</span><span class="sxs-lookup"><span data-stu-id="5c964-143">120</span></span>       | <span data-ttu-id="5c964-144">125%</span><span class="sxs-lookup"><span data-stu-id="5c964-144">125%</span></span>               |
| <span data-ttu-id="5c964-145">144</span><span class="sxs-lookup"><span data-stu-id="5c964-145">144</span></span>       | <span data-ttu-id="5c964-146">150%</span><span class="sxs-lookup"><span data-stu-id="5c964-146">150%</span></span>               |
| <span data-ttu-id="5c964-147">192</span><span class="sxs-lookup"><span data-stu-id="5c964-147">192</span></span>       | <span data-ttu-id="5c964-148">200%</span><span class="sxs-lookup"><span data-stu-id="5c964-148">200%</span></span>               |



 

<span data-ttu-id="5c964-149">L’exemple suivant fournit un exemple de gestionnaire de modifications de PPP.</span><span class="sxs-lookup"><span data-stu-id="5c964-149">The following example provides a sample DPI change handler.</span></span>


```C++
    case WM_DPICHANGED:
    {
        g_dpi = HIWORD(wParam);
        UpdateDpiDependentFontsAndResources();

        RECT* const prcNewWindow = (RECT*)lParam;
        SetWindowPos(hWnd,
            NULL,
            prcNewWindow ->left,
            prcNewWindow ->top,
            prcNewWindow->right - prcNewWindow->left,
            prcNewWindow->bottom - prcNewWindow->top,
            SWP_NOZORDER | SWP_NOACTIVATE);
        break;
    }
```



<span data-ttu-id="5c964-150">Le code suivant met à l’échelle de façon linéaire une valeur comprise entre 100% (96 ppp) et une valeur PPP arbitraire définie par *g \_ PPP*.</span><span class="sxs-lookup"><span data-stu-id="5c964-150">The following code linearly scales a value from 100% (96 DPI) to an arbitrary DPI defined by *g\_dpi*.</span></span>


```C++
    INT iBorderWidth100 = 5;
    iBorderWidth = MulDiv(iBorderWidth100, g_dpi, USER_DEFAULT_SCREEN_DPI);
```



<span data-ttu-id="5c964-151">Une autre façon de mettre à l’échelle une valeur consiste à convertir la valeur PPP en un facteur d’échelle et à l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="5c964-151">An alternative way to scale a value is to convert the DPI value into a scale factor and use that.</span></span>


```C++
    INT iBorderWidth100 = 5;
    FLOAT fscale = (float) g_dpi / USER_DEFAULT_SCREEN_DPI;
    iBorderWidth = iBorderWidth100 * fscale;
```



## <a name="requirements"></a><span data-ttu-id="5c964-152">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5c964-152">Requirements</span></span>



| <span data-ttu-id="5c964-153">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5c964-153">Requirement</span></span> | <span data-ttu-id="5c964-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="5c964-154">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5c964-155">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5c964-155">Minimum supported client</span></span><br/> | <span data-ttu-id="5c964-156">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5c964-156">Windows 8.1 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5c964-157">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5c964-157">Minimum supported server</span></span><br/> | <span data-ttu-id="5c964-158">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5c964-158">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="5c964-159">En-tête</span><span class="sxs-lookup"><span data-stu-id="5c964-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c964-160"><dt>WinUser. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c964-160"><dt>WinUser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c964-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5c964-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c964-162">**\_reconnaissance dpi**</span><span class="sxs-lookup"><span data-stu-id="5c964-162">**DPI\_AWARENESS**</span></span>](/windows/desktop/api/windef/ne-windef-dpi_awareness)
</dt> <dt>

[<span data-ttu-id="5c964-163">**\_détection des PPP de processus \_**</span><span class="sxs-lookup"><span data-stu-id="5c964-163">**PROCESS\_DPI\_AWARENESS**</span></span>](/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-process_dpi_awareness)
</dt> </dl>

 

