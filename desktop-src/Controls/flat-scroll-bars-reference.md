---
title: Barre de défilement plate
description: Cette section contient des informations sur les éléments de programmation utilisés pour contrôler les barres de défilement plat.
ms.assetid: vs|controls|~\controls\flatsb\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46e611e8d5755d119a8c24bdbccb9f10408d3d7d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839598"
---
# <a name="flat-scroll-bar"></a><span data-ttu-id="b62e7-103">Barre de défilement plate</span><span class="sxs-lookup"><span data-stu-id="b62e7-103">Flat Scroll Bar</span></span>

<span data-ttu-id="b62e7-104">Cette section contient des informations sur les éléments de programmation utilisés pour contrôler les barres de défilement plat.</span><span class="sxs-lookup"><span data-stu-id="b62e7-104">This section contains information about the programming elements used to control flat scroll bars.</span></span>

### <a name="overviews"></a><span data-ttu-id="b62e7-105">Vues d'ensemble</span><span class="sxs-lookup"><span data-stu-id="b62e7-105">Overviews</span></span>



| <span data-ttu-id="b62e7-106">Rubrique</span><span class="sxs-lookup"><span data-stu-id="b62e7-106">Topic</span></span>                                    | <span data-ttu-id="b62e7-107">Contenu</span><span class="sxs-lookup"><span data-stu-id="b62e7-107">Contents</span></span>                                                                                                                                                                                                                                                                              |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b62e7-108">Barres de défilement plat</span><span class="sxs-lookup"><span data-stu-id="b62e7-108">Flat Scroll Bars</span></span>](flat-scroll-bars.md) | <span data-ttu-id="b62e7-109">Microsoft Internet Explorer 4,0 a introduit une nouvelle technologie visuelle appelée barres de défilement plat.</span><span class="sxs-lookup"><span data-stu-id="b62e7-109">Microsoft Internet Explorer 4.0 introduced a new visual technology called flat scroll bars.</span></span> <span data-ttu-id="b62e7-110">Fonctionnellement, les barres de défilement plat se comportent comme des barres de défilement standard.</span><span class="sxs-lookup"><span data-stu-id="b62e7-110">Functionally, flat scroll bars behave just like standard scroll bars.</span></span> <span data-ttu-id="b62e7-111">La différence est que vous pouvez personnaliser leur apparence dans une plus grande mesure par rapport aux barres de défilement standard.</span><span class="sxs-lookup"><span data-stu-id="b62e7-111">The difference is that you can customize their appearance to a greater extent than standard scroll bars.</span></span><br/> |



 

### <a name="functions"></a><span data-ttu-id="b62e7-112">Fonctions</span><span class="sxs-lookup"><span data-stu-id="b62e7-112">Functions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b62e7-113">Rubrique</span><span class="sxs-lookup"><span data-stu-id="b62e7-113">Topic</span></span></th>
<th><span data-ttu-id="b62e7-114">Contenu</span><span class="sxs-lookup"><span data-stu-id="b62e7-114">Contents</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b62e7-115"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_enablescrollbar"><strong>FlatSB_EnableScrollBar</strong></a></span><span class="sxs-lookup"><span data-stu-id="b62e7-115"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_enablescrollbar"><strong>FlatSB_EnableScrollBar</strong></a></span></span></td>
<td><span data-ttu-id="b62e7-116">Active ou désactive les boutons de direction de la barre de défilement plate.</span><span class="sxs-lookup"><span data-stu-id="b62e7-116">Enables or disables one or both flat scroll bar direction buttons.</span></span> <span data-ttu-id="b62e7-117">Si les barres de défilement plat ne sont pas initialisées pour la fenêtre, cette fonction appelle la fonction <a href="/windows/desktop/api/Winuser/nf-winuser-enablescrollbar"><strong>EnableScrollBar</strong></a> standard.</span><span class="sxs-lookup"><span data-stu-id="b62e7-117">If flat scroll bars are not initialized for the window, this function calls the standard <a href="/windows/desktop/api/Winuser/nf-winuser-enablescrollbar"><strong>EnableScrollBar</strong></a> function.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b62e7-118"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollinfo"><strong>FlatSB_GetScrollInfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="b62e7-118"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollinfo"><strong>FlatSB_GetScrollInfo</strong></a></span></span></td>
<td><span data-ttu-id="b62e7-119">Obtient les informations pour une barre de défilement en 2D.</span><span class="sxs-lookup"><span data-stu-id="b62e7-119">Gets the information for a flat scroll bar.</span></span> <span data-ttu-id="b62e7-120">Si les barres de défilement plat ne sont pas initialisées pour la fenêtre, cette fonction appelle la fonction <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollinfo"><strong>GetScrollInfo</strong></a> standard.</span><span class="sxs-lookup"><span data-stu-id="b62e7-120">If flat scroll bars are not initialized for the window, this function calls the standard <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollinfo"><strong>GetScrollInfo</strong></a> function.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b62e7-121"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollpos"><strong>FlatSB_GetScrollPos</strong></a></span><span class="sxs-lookup"><span data-stu-id="b62e7-121"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollpos"><strong>FlatSB_GetScrollPos</strong></a></span></span></td>
<td><span data-ttu-id="b62e7-122">Obtient la position du curseur dans une barre de défilement plate.</span><span class="sxs-lookup"><span data-stu-id="b62e7-122">Gets the thumb position in a flat scroll bar.</span></span> <span data-ttu-id="b62e7-123">Si les barres de défilement plat ne sont pas initialisées pour la fenêtre, cette fonction appelle la fonction <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollpos"><strong>GetScrollPos</strong></a> standard.</span><span class="sxs-lookup"><span data-stu-id="b62e7-123">If flat scroll bars are not initialized for the window, this function calls the standard <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollpos"><strong>GetScrollPos</strong></a> function.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b62e7-124"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollprop"><strong>FlatSB_GetScrollProp</strong></a></span><span class="sxs-lookup"><span data-stu-id="b62e7-124"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollprop"><strong>FlatSB_GetScrollProp</strong></a></span></span></td>
<td><span data-ttu-id="b62e7-125">Obtient les propriétés d’une barre de défilement en 2D.</span><span class="sxs-lookup"><span data-stu-id="b62e7-125">Gets the properties for a flat scroll bar.</span></span> <span data-ttu-id="b62e7-126">Cette fonction peut également être utilisée pour déterminer si <a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>InitializeFlatSB</strong></a> a été appelé pour cette fenêtre.</span><span class="sxs-lookup"><span data-stu-id="b62e7-126">This function can also be used to determine if <a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>InitializeFlatSB</strong></a> has been called for this window.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b62e7-127"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollpropptr"><strong>FlatSB_GetScrollPropPtr</strong></a></span><span class="sxs-lookup"><span data-stu-id="b62e7-127"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollpropptr"><strong>FlatSB_GetScrollPropPtr</strong></a></span></span></td>
<td><span data-ttu-id="b62e7-128">Obtient les propriétés d’une barre de défilement en 2D.</span><span class="sxs-lookup"><span data-stu-id="b62e7-128">Gets the properties for a flat scroll bar.</span></span> <span data-ttu-id="b62e7-129">Cette fonction peut également être utilisée pour déterminer si <a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>InitializeFlatSB</strong></a> a été appelé pour cette fenêtre.</span><span class="sxs-lookup"><span data-stu-id="b62e7-129">This function can also be used to determine if <a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>InitializeFlatSB</strong></a> has been called for this window.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="b62e7-130">Identique à <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollprop"><strong>FlatSB_GetScrollProp</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b62e7-130">This is identical to <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollprop"><strong>FlatSB_GetScrollProp</strong></a>.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b62e7-131"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollrange"><strong>FlatSB_GetScrollRange</strong></a></span><span class="sxs-lookup"><span data-stu-id="b62e7-131"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollrange"><strong>FlatSB_GetScrollRange</strong></a></span></span></td>
<td><span data-ttu-id="b62e7-132">Obtient la plage de défilement pour une barre de défilement en 2D.</span><span class="sxs-lookup"><span data-stu-id="b62e7-132">Gets the scroll range for a flat scroll bar.</span></span> <span data-ttu-id="b62e7-133">Si les barres de défilement plat ne sont pas initialisées pour la fenêtre, cette fonction appelle la fonction <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollrange"><strong>GetScrollRange</strong></a> standard.</span><span class="sxs-lookup"><span data-stu-id="b62e7-133">If flat scroll bars are not initialized for the window, this function calls the standard <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollrange"><strong>GetScrollRange</strong></a> function.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b62e7-134"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollinfo"><strong>FlatSB_SetScrollInfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="b62e7-134"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollinfo"><strong>FlatSB_SetScrollInfo</strong></a></span></span></td>
<td><span data-ttu-id="b62e7-135">Définit les informations pour une barre de défilement en 2D.</span><span class="sxs-lookup"><span data-stu-id="b62e7-135">Sets the information for a flat scroll bar.</span></span> <span data-ttu-id="b62e7-136">Si les barres de défilement plat ne sont pas initialisées pour la fenêtre, cette fonction appelle la fonction <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollinfo"><strong>SetScrollInfo</strong></a> standard.</span><span class="sxs-lookup"><span data-stu-id="b62e7-136">If flat scroll bars are not initialized for the window, this function calls the standard <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollinfo"><strong>SetScrollInfo</strong></a> function.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b62e7-137"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollpos"><strong>FlatSB_SetScrollPos</strong></a></span><span class="sxs-lookup"><span data-stu-id="b62e7-137"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollpos"><strong>FlatSB_SetScrollPos</strong></a></span></span></td>
<td><span data-ttu-id="b62e7-138">Définit la position actuelle du curseur dans une barre de défilement plate.</span><span class="sxs-lookup"><span data-stu-id="b62e7-138">Sets the current position of the thumb in a flat scroll bar.</span></span> <span data-ttu-id="b62e7-139">Si les barres de défilement plat ne sont pas initialisées pour la fenêtre, cette fonction appelle la fonction <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollpos"><strong>SetScrollPos</strong></a> standard.</span><span class="sxs-lookup"><span data-stu-id="b62e7-139">If flat scroll bars are not initialized for the window, this function calls the standard <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollpos"><strong>SetScrollPos</strong></a> function.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b62e7-140"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop"><strong>FlatSB_SetScrollProp</strong></a></span><span class="sxs-lookup"><span data-stu-id="b62e7-140"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop"><strong>FlatSB_SetScrollProp</strong></a></span></span></td>
<td><span data-ttu-id="b62e7-141">Définit les propriétés d’une barre de défilement en 2D.</span><span class="sxs-lookup"><span data-stu-id="b62e7-141">Sets the properties for a flat scroll bar.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b62e7-142"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollrange"><strong>FlatSB_SetScrollRange</strong></a></span><span class="sxs-lookup"><span data-stu-id="b62e7-142"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollrange"><strong>FlatSB_SetScrollRange</strong></a></span></span></td>
<td><span data-ttu-id="b62e7-143">Définit la plage de défilement d’une barre de défilement en 2D.</span><span class="sxs-lookup"><span data-stu-id="b62e7-143">Sets the scroll range of a flat scroll bar.</span></span> <span data-ttu-id="b62e7-144">Si les barres de défilement plat ne sont pas initialisées pour la fenêtre, cette fonction appelle la fonction <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollrange"><strong>SetScrollRange</strong></a> standard.</span><span class="sxs-lookup"><span data-stu-id="b62e7-144">If flat scroll bars are not initialized for the window, this function calls the standard <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollrange"><strong>SetScrollRange</strong></a> function.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b62e7-145"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_showscrollbar"><strong>FlatSB_ShowScrollBar</strong></a></span><span class="sxs-lookup"><span data-stu-id="b62e7-145"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_showscrollbar"><strong>FlatSB_ShowScrollBar</strong></a></span></span></td>
<td><span data-ttu-id="b62e7-146">Affiche ou masque une barre de défilement en 2D.</span><span class="sxs-lookup"><span data-stu-id="b62e7-146">Shows or hides a flat scroll bar.</span></span> <span data-ttu-id="b62e7-147">Si les barres de défilement plat ne sont pas initialisées pour la fenêtre, cette fonction appelle la fonction <a href="/windows/desktop/api/Winuser/nf-winuser-showscrollbar"><strong>ShowScrollBar</strong></a> standard.</span><span class="sxs-lookup"><span data-stu-id="b62e7-147">If flat scroll bars are not initialized for the window, this function calls the standard <a href="/windows/desktop/api/Winuser/nf-winuser-showscrollbar"><strong>ShowScrollBar</strong></a> function.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b62e7-148"><a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>InitializeFlatSB</strong></a></span><span class="sxs-lookup"><span data-stu-id="b62e7-148"><a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>InitializeFlatSB</strong></a></span></span></td>
<td><span data-ttu-id="b62e7-149">Initialise des barres de défilement plates pour une fenêtre particulière.</span><span class="sxs-lookup"><span data-stu-id="b62e7-149">Initializes flat scroll bars for a particular window.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b62e7-150"><a href="/windows/desktop/api/Commctrl/nf-commctrl-uninitializeflatsb"><strong>UninitializeFlatSB</strong></a></span><span class="sxs-lookup"><span data-stu-id="b62e7-150"><a href="/windows/desktop/api/Commctrl/nf-commctrl-uninitializeflatsb"><strong>UninitializeFlatSB</strong></a></span></span></td>
<td><span data-ttu-id="b62e7-151">Désinitialise les barres de défilement plat pour une fenêtre particulière.</span><span class="sxs-lookup"><span data-stu-id="b62e7-151">Uninitializes flat scroll bars for a particular window.</span></span> <span data-ttu-id="b62e7-152">La fenêtre spécifiée reviendra aux barres de défilement standard.</span><span class="sxs-lookup"><span data-stu-id="b62e7-152">The specified window will revert to standard scroll bars.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

 

 





