---
title: Handle de DPI_AWARENESS_CONTEXT (WINDEF. h)
description: Identifie le contexte de sensibilisation pour une fenêtre.
ms.assetid: BFD54A9F-642B-4A3A-BBB9-F3A80779251D
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: 1663fad828a2fb29aa0d65ef58ae79616f64edcd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317277"
---
# <a name="dpi_awareness_context-handle"></a><span data-ttu-id="c90e2-103">Handle de contexte de \_ détection PPP \_</span><span class="sxs-lookup"><span data-stu-id="c90e2-103">DPI\_AWARENESS\_CONTEXT handle</span></span>

<span data-ttu-id="c90e2-104">Identifie le contexte de sensibilisation pour une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="c90e2-104">Identifies the awareness context for a window.</span></span>

## <a name="syntax"></a><span data-ttu-id="c90e2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c90e2-105">Syntax</span></span>

``` syntax
#define DPI_AWARENESS_CONTEXT_UNAWARE              ((DPI_AWARENESS_CONTEXT)-1)
#define DPI_AWARENESS_CONTEXT_SYSTEM_AWARE         ((DPI_AWARENESS_CONTEXT)-2)
#define DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE    ((DPI_AWARENESS_CONTEXT)-3)
#define DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2 ((DPI_AWARENESS_CONTEXT)-4)
#define DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED    ((DPI_AWARENESS_CONTEXT)-5)
```

## <a name="constants"></a><span data-ttu-id="c90e2-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="c90e2-106">Constants</span></span>

<span data-ttu-id="c90e2-107">**contexte de détection DPI ne \_ \_ \_ connaissant pas**</span><span class="sxs-lookup"><span data-stu-id="c90e2-107">**DPI\_AWARENESS\_CONTEXT\_UNAWARE**</span></span><dl> <span data-ttu-id="c90e2-108">Prise en charge de DPI ignorée.</span><span class="sxs-lookup"><span data-stu-id="c90e2-108">DPI unaware.</span></span> <span data-ttu-id="c90e2-109">Cette fenêtre n’est pas mise à l’échelle pour les modifications PPP et est toujours supposée avoir un facteur d’échelle de 100% (96 ppp).</span><span class="sxs-lookup"><span data-stu-id="c90e2-109">This window does not scale for DPI changes and is always assumed to have a scale factor of 100% (96 DPI).</span></span> <span data-ttu-id="c90e2-110">Il est automatiquement mis à l’échelle par le système sur n’importe quel autre paramètre PPP.</span><span class="sxs-lookup"><span data-stu-id="c90e2-110">It will be automatically scaled by the system on any other DPI setting.</span></span>  
</dl>

<span data-ttu-id="c90e2-111">**\_prise en \_ charge du contexte de détection dpi \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c90e2-111">**DPI\_AWARENESS\_CONTEXT\_SYSTEM\_AWARE**</span></span><dl> <span data-ttu-id="c90e2-112">Prise en charge DPI système.</span><span class="sxs-lookup"><span data-stu-id="c90e2-112">System DPI aware.</span></span> <span data-ttu-id="c90e2-113">Cette fenêtre n’est pas mise à l’échelle pour les modifications PPP.</span><span class="sxs-lookup"><span data-stu-id="c90e2-113">This window does not scale for DPI changes.</span></span> <span data-ttu-id="c90e2-114">Elle interroge l’PPP une fois et utilise cette valeur pour la durée de vie du processus.</span><span class="sxs-lookup"><span data-stu-id="c90e2-114">It will query for the DPI once and use that value for the lifetime of the process.</span></span> <span data-ttu-id="c90e2-115">Si les PPP changent, le processus ne s’ajuste pas à la nouvelle valeur PPP.</span><span class="sxs-lookup"><span data-stu-id="c90e2-115">If the DPI changes, the process will not adjust to the new DPI value.</span></span> <span data-ttu-id="c90e2-116">Il est automatiquement mis à l’échelle par le système lorsque la valeur PPP change de la valeur système.</span><span class="sxs-lookup"><span data-stu-id="c90e2-116">It will be automatically scaled up or down by the system when the DPI changes from the system value.</span></span>  
</dl>

<span data-ttu-id="c90e2-117">**\_prise en charge du contexte de détection dpi \_ \_ par \_ moniteur \_**</span><span class="sxs-lookup"><span data-stu-id="c90e2-117">**DPI\_AWARENESS\_CONTEXT\_PER\_MONITOR\_AWARE**</span></span><dl> <span data-ttu-id="c90e2-118">Prise en charge de la résolution par moniteur.</span><span class="sxs-lookup"><span data-stu-id="c90e2-118">Per monitor DPI aware.</span></span> <span data-ttu-id="c90e2-119">Cette fenêtre vérifie la résolution des PPP lorsqu’elle est créée et ajuste le facteur d’échelle à chaque modification de la résolution.</span><span class="sxs-lookup"><span data-stu-id="c90e2-119">This window checks for the DPI when it is created and adjusts the scale factor whenever the DPI changes.</span></span> <span data-ttu-id="c90e2-120">Ces processus ne sont pas automatiquement mis à l’échelle par le système.</span><span class="sxs-lookup"><span data-stu-id="c90e2-120">These processes are not automatically scaled by the system.</span></span>  
</dl>

<span data-ttu-id="c90e2-121">**\_Contexte de sensibilisation dpi \_ \_ par \_ analyse \_ \_ v2**</span><span class="sxs-lookup"><span data-stu-id="c90e2-121">**DPI\_AWARENESS\_CONTEXT\_PER\_MONITOR\_AWARE\_V2**</span></span><dl> <span data-ttu-id="c90e2-122">Également appelé **par moniteur v2**.</span><span class="sxs-lookup"><span data-stu-id="c90e2-122">Also known as **Per Monitor v2**.</span></span> <span data-ttu-id="c90e2-123">Progression sur le mode de prise en charge DPI par moniteur d’origine, qui permet aux applications d’accéder aux nouveaux comportements de mise à l’échelle en fonction de la DPI sur une base de fenêtre de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="c90e2-123">An advancement over the original per-monitor DPI awareness mode, which enables applications to access new DPI-related scaling behaviors on a per top-level window basis.</span></span>  
<span data-ttu-id="c90e2-124">Par moniteur V2 a été mis à disposition dans le créateur mise à jour de Windows 10, et n’est pas disponible dans les versions antérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="c90e2-124">Per Monitor v2 was made available in the Creators Update of Windows 10, and is not available on earlier versions of the operating system.</span></span>  
<span data-ttu-id="c90e2-125">Les comportements supplémentaires introduits sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="c90e2-125">The additional behaviors introduced are as follows:</span></span>

-   <span data-ttu-id="c90e2-126">**Notifications de modification dpi de la fenêtre enfant** : dans les contextes de l’analyse, la totalité de l’arborescence de la fenêtre est notifiée des modifications PPP qui se produisent.</span><span class="sxs-lookup"><span data-stu-id="c90e2-126">**Child window DPI change notifications** - In Per Monitor v2 contexts, the entire window tree is notified of any DPI changes that occur.</span></span>
-   <span data-ttu-id="c90e2-127">**Mise à l’échelle d’une zone non cliente** : toutes les fenêtres ont automatiquement leur zone non cliente dessinée en fonction des PPP.</span><span class="sxs-lookup"><span data-stu-id="c90e2-127">**Scaling of non-client area** - All windows will automatically have their non-client area drawn in a DPI sensitive fashion.</span></span> <span data-ttu-id="c90e2-128">Les appels à [**EnableNonClientDpiScaling**](/windows/desktop/api/Winuser/nf-winuser-enablenonclientdpiscaling) ne sont pas nécessaires.</span><span class="sxs-lookup"><span data-stu-id="c90e2-128">Calls to [**EnableNonClientDpiScaling**](/windows/desktop/api/Winuser/nf-winuser-enablenonclientdpiscaling) are unnecessary.</span></span>
-   <span data-ttu-id="c90e2-129">**Mise à l’échelle des menus Win32** : tous les menus Ntuser créés dans les contextes de par moniteur v2 feront l’d’une mise à l’échelle en fonction de chaque moniteur.</span><span class="sxs-lookup"><span data-stu-id="c90e2-129">**Scaling of Win32 menus** - All NTUSER menus created in Per Monitor v2 contexts will be scaling in a per-monitor fashion.</span></span>
-   <span data-ttu-id="c90e2-130">**Mise à l’échelle** de la boîte de dialogue : les boîtes de dialogue Win32 créées dans les contextes par moniteur v2 répondent automatiquement aux modifications PPP.</span><span class="sxs-lookup"><span data-stu-id="c90e2-130">**Dialog Scaling** - Win32 dialogs created in Per Monitor v2 contexts will automatically respond to DPI changes.</span></span>
-   <span data-ttu-id="c90e2-131">**Amélioration de la mise à l’échelle des contrôles Comctl32** : divers contrôles Comctl32 ont amélioré le comportement de mise à l’échelle PPP dans les contextes de chaque moniteur v2.</span><span class="sxs-lookup"><span data-stu-id="c90e2-131">**Improved scaling of comctl32 controls** - Various comctl32 controls have improved DPI scaling behavior in Per Monitor v2 contexts.</span></span>
-   <span data-ttu-id="c90e2-132">**Amélioration du comportement des thèmes** : les descripteurs Uxtheme ouverts dans le contexte d’une fenêtre par moniteur v2 fonctionnent en fonction de la résolution associée à cette fenêtre.</span><span class="sxs-lookup"><span data-stu-id="c90e2-132">**Improved theming behavior** - UxTheme handles opened in the context of a Per Monitor v2 window will operate in terms of the DPI associated with that window.</span></span>

  
</dl>

<span data-ttu-id="c90e2-133">**DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED**</span><span class="sxs-lookup"><span data-stu-id="c90e2-133">**DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED**</span></span>

<span data-ttu-id="c90e2-134">DPI ne connaissant pas la qualité améliorée du contenu basé sur GDI.</span><span class="sxs-lookup"><span data-stu-id="c90e2-134">DPI unaware with improved quality of GDI-based content.</span></span> <span data-ttu-id="c90e2-135">Ce mode se comporte de la même façon que DPI_AWARENESS_CONTEXT_UNAWARE, mais il permet également au système d’améliorer automatiquement la qualité de rendu du texte et d’autres primitives basées sur GDI lorsque la fenêtre est affichée sur un moniteur haute résolution.</span><span class="sxs-lookup"><span data-stu-id="c90e2-135">This mode behaves similarly to DPI_AWARENESS_CONTEXT_UNAWARE, but also enables the system to automatically improve the rendering quality of text and other GDI-based primitives when the window is displayed on a high-DPI monitor.</span></span>

<span data-ttu-id="c90e2-136">Pour plus d’informations, consultez [amélioration de l’expérience haute résolution dans les applications de bureau GDI](https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/#Uwv9gY1SvpbgQ4dK.97).</span><span class="sxs-lookup"><span data-stu-id="c90e2-136">For more details, see [Improving the high-DPI experience in GDI-based Desktop apps](https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/#Uwv9gY1SvpbgQ4dK.97).</span></span>

<span data-ttu-id="c90e2-137">DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED a été introduite dans la mise à jour 2018 d’octobre de Windows 10 (également connue sous le nom de version 1809).</span><span class="sxs-lookup"><span data-stu-id="c90e2-137">DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED was introduced in the October 2018 update of Windows 10 (also known as version 1809).</span></span>


## <a name="requirements"></a><span data-ttu-id="c90e2-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c90e2-138">Requirements</span></span>

| <span data-ttu-id="c90e2-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c90e2-139">Requirement</span></span> | <span data-ttu-id="c90e2-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="c90e2-140">Value</span></span> |
|----|-----------|
| <span data-ttu-id="c90e2-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c90e2-141">Minimum supported client</span></span><br/> | <span data-ttu-id="c90e2-142">Applications de bureau Windows 10, version 1607 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c90e2-142">Windows 10, version 1607 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c90e2-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c90e2-143">Minimum supported server</span></span><br/> | <span data-ttu-id="c90e2-144">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="c90e2-144">None supported</span></span> <br/>  |
| <span data-ttu-id="c90e2-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="c90e2-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="c90e2-146"><dt>WINDEF. h</dt></span><span class="sxs-lookup"><span data-stu-id="c90e2-146"><dt>windef.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="c90e2-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c90e2-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c90e2-148">**AreDpiAwarenessContextsEqual**</span><span class="sxs-lookup"><span data-stu-id="c90e2-148">**AreDpiAwarenessContextsEqual**</span></span>](/windows/desktop/api/winuser/nf-winuser-aredpiawarenesscontextsequal)
</dt> <dt>

[<span data-ttu-id="c90e2-149">**GetAwarenessFromDpiAwarenessContext**</span><span class="sxs-lookup"><span data-stu-id="c90e2-149">**GetAwarenessFromDpiAwarenessContext**</span></span>](/windows/desktop/api/winuser/nf-winuser-getawarenessfromdpiawarenesscontext)
</dt> </dl>

[<span data-ttu-id="c90e2-150">**GetDpiFromDpiAwarenessContext**</span><span class="sxs-lookup"><span data-stu-id="c90e2-150">**GetDpiFromDpiAwarenessContext**</span></span>](/windows/desktop/api/winuser/nf-winuser-getdpifromdpiawarenesscontext)
</dt> </dl>

[<span data-ttu-id="c90e2-151">**GetThreadDpiAwarenessContext**</span><span class="sxs-lookup"><span data-stu-id="c90e2-151">**GetThreadDpiAwarenessContext**</span></span>](/windows/desktop/api/winuser/nf-winuser-getthreaddpiawarenesscontext)
</dt> </dl>

[<span data-ttu-id="c90e2-152">**GetWindowDpiAwarenessContext**</span><span class="sxs-lookup"><span data-stu-id="c90e2-152">**GetWindowDpiAwarenessContext**</span></span>](/windows/desktop/api/winuser/nf-winuser-getwindowdpiawarenesscontext)
</dt> </dl>

[<span data-ttu-id="c90e2-153">**IsValidDpiAwarenessContext**</span><span class="sxs-lookup"><span data-stu-id="c90e2-153">**IsValidDpiAwarenessContext**</span></span>](/windows/desktop/api/winuser/nf-winuser-isvaliddpiawarenesscontext)
</dt> </dl>

[<span data-ttu-id="c90e2-154">**SetProcessDpiAwarenessContext**</span><span class="sxs-lookup"><span data-stu-id="c90e2-154">**SetProcessDpiAwarenessContext**</span></span>](/windows/desktop/api/winuser/nf-winuser-setprocessdpiawarenesscontext)
</dt> </dl>

[<span data-ttu-id="c90e2-155">**SetThreadDpiAwarenessContext**</span><span class="sxs-lookup"><span data-stu-id="c90e2-155">**SetThreadDpiAwarenessContext**</span></span>](/windows/desktop/api/winuser/nf-winuser-setthreaddpiawarenesscontext)
