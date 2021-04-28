---
title: Fonctions d’entrée de souris
description: Fonctions d’entrée de souris
ms.assetid: a666b25b-a75c-4500-8077-fabe07589a1d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a952a9ce90284f284b176c608228c0b852f5f4c8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112877"
---
# <a name="mouse-input-functions"></a><span data-ttu-id="ea694-103">Fonctions d’entrée de souris</span><span class="sxs-lookup"><span data-stu-id="ea694-103">Mouse Input Functions</span></span>


## <a name="in-this-section"></a><span data-ttu-id="ea694-104">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="ea694-104">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ea694-105">Rubrique</span><span class="sxs-lookup"><span data-stu-id="ea694-105">Topic</span></span></th>
<th><span data-ttu-id="ea694-106">Description</span><span class="sxs-lookup"><span data-stu-id="ea694-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ea694-107"><a href="/windows/win32/api/commctrl/nf-commctrl-_trackmouseevent"><strong>_TrackMouseEvent</strong></a></span><span class="sxs-lookup"><span data-stu-id="ea694-107"><a href="/windows/win32/api/commctrl/nf-commctrl-_trackmouseevent"><strong>_TrackMouseEvent</strong></a></span></span><br/></td>
<td><span data-ttu-id="ea694-108">Publie des messages lorsque le pointeur de la souris quitte une fenêtre ou pointe sur une fenêtre pendant un laps de temps spécifié.</span><span class="sxs-lookup"><span data-stu-id="ea694-108">Posts messages when the mouse pointer leaves a window or hovers over a window for a specified amount of time.</span></span> <span data-ttu-id="ea694-109">Cette fonction appelle <a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>TrackMouseEvent</strong></a> si elle existe, sinon elle l’émule.</span><span class="sxs-lookup"><span data-stu-id="ea694-109">This function calls <a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>TrackMouseEvent</strong></a> if it exists, otherwise it emulates it.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ea694-110"><a href="/windows/desktop/api/winuser/nf-winuser-dragdetect"><strong>DragDetect</strong></a></span><span class="sxs-lookup"><span data-stu-id="ea694-110"><a href="/windows/desktop/api/winuser/nf-winuser-dragdetect"><strong>DragDetect</strong></a></span></span><br/></td>
<td><span data-ttu-id="ea694-111">Capture la souris et suit ses déplacements jusqu'à ce que l'utilisateur relâche le bouton gauche, appuie sur la touche Échap ou déplace la souris en dehors du rectangle de glissement entourant le point spécifié.</span><span class="sxs-lookup"><span data-stu-id="ea694-111">Captures the mouse and tracks its movement until the user releases the left button, presses the ESC key, or moves the mouse outside the drag rectangle around the specified point.</span></span> <span data-ttu-id="ea694-112">La largeur et la hauteur du rectangle de glissement sont spécifiées par le <strong>SM_CXDRAG</strong> et <strong>SM_CYDRAG</strong> valeurs retournées par la fonction <a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics"><strong>GetSystemMetrics</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="ea694-112">The width and height of the drag rectangle are specified by the <strong>SM_CXDRAG</strong> and <strong>SM_CYDRAG</strong> values returned by the <a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics"><strong>GetSystemMetrics</strong></a> function.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ea694-113"><a href="/windows/desktop/api/winuser/nf-winuser-getcapture"><strong>GetCapture</strong></a></span><span class="sxs-lookup"><span data-stu-id="ea694-113"><a href="/windows/desktop/api/winuser/nf-winuser-getcapture"><strong>GetCapture</strong></a></span></span><br/></td>
<td><span data-ttu-id="ea694-114">Récupère un handle vers la fenêtre (le cas échéant) qui a capturé la souris.</span><span class="sxs-lookup"><span data-stu-id="ea694-114">Retrieves a handle to the window (if any) that has captured the mouse.</span></span> <span data-ttu-id="ea694-115">Une seule fenêtre à la fois peut capturer la souris ; Cette fenêtre reçoit l’entrée de la souris, que le curseur figure ou non dans ses limites.</span><span class="sxs-lookup"><span data-stu-id="ea694-115">Only one window at a time can capture the mouse; this window receives mouse input whether or not the cursor is within its borders.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ea694-116"><a href="/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime"><strong>GetDoubleClickTime</strong></a></span><span class="sxs-lookup"><span data-stu-id="ea694-116"><a href="/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime"><strong>GetDoubleClickTime</strong></a></span></span><br/></td>
<td><span data-ttu-id="ea694-117">Récupère le temps de double-clic actuel pour la souris.</span><span class="sxs-lookup"><span data-stu-id="ea694-117">Retrieves the current double-click time for the mouse.</span></span> <span data-ttu-id="ea694-118">Un double-clic est une série de deux clics du bouton de la souris, le second se produisant dans un délai spécifié après le premier.</span><span class="sxs-lookup"><span data-stu-id="ea694-118">A double-click is a series of two clicks of the mouse button, the second occurring within a specified time after the first.</span></span> <span data-ttu-id="ea694-119">L’heure du double-clic correspond au nombre maximal de millisecondes qui peuvent se produire entre le premier et le deuxième clic d’un double-clic.</span><span class="sxs-lookup"><span data-stu-id="ea694-119">The double-click time is the maximum number of milliseconds that may occur between the first and second click of a double-click.</span></span> <span data-ttu-id="ea694-120">La durée maximale de double-clic est de 5000 millisecondes.</span><span class="sxs-lookup"><span data-stu-id="ea694-120">The maximum double-click time is 5000 milliseconds.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ea694-121"><a href="/windows/desktop/api/winuser/nf-winuser-getmousemovepointsex"><strong>GetMouseMovePointsEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="ea694-121"><a href="/windows/desktop/api/winuser/nf-winuser-getmousemovepointsex"><strong>GetMouseMovePointsEx</strong></a></span></span><br/></td>
<td><span data-ttu-id="ea694-122">Récupère un historique allant jusqu’à 64 coordonnées précédentes de la souris ou du stylet.</span><span class="sxs-lookup"><span data-stu-id="ea694-122">Retrieves a history of up to 64 previous coordinates of the mouse or pen.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ea694-123"><a href="/windows/desktop/api/winuser/nf-winuser-mouse_event"><strong>mouse_event</strong></a></span><span class="sxs-lookup"><span data-stu-id="ea694-123"><a href="/windows/desktop/api/winuser/nf-winuser-mouse_event"><strong>mouse_event</strong></a></span></span><br/></td>
<td><span data-ttu-id="ea694-124">La fonction <a href="/windows/desktop/api/winuser/nf-winuser-mouse_event"><strong>mouse_event</strong></a> synthétise le mouvement de la souris et les clics de bouton.</span><span class="sxs-lookup"><span data-stu-id="ea694-124">The <a href="/windows/desktop/api/winuser/nf-winuser-mouse_event"><strong>mouse_event</strong></a> function synthesizes mouse motion and button clicks.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="ea694-125">Cette fonction a été remplacée.</span><span class="sxs-lookup"><span data-stu-id="ea694-125">This function has been superseded.</span></span> <span data-ttu-id="ea694-126">Utilisez plutôt <a href="/windows/desktop/api/winuser/nf-winuser-sendinput"><strong>SendInput</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="ea694-126">Use <a href="/windows/desktop/api/winuser/nf-winuser-sendinput"><strong>SendInput</strong></a> instead.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ea694-127"><a href="/windows/desktop/api/winuser/nf-winuser-releasecapture"><strong>ReleaseCapture</strong></a></span><span class="sxs-lookup"><span data-stu-id="ea694-127"><a href="/windows/desktop/api/winuser/nf-winuser-releasecapture"><strong>ReleaseCapture</strong></a></span></span><br/></td>
<td><span data-ttu-id="ea694-128">Libère la capture de la souris d’une fenêtre dans le thread actuel et restaure le traitement d’entrée de souris normal.</span><span class="sxs-lookup"><span data-stu-id="ea694-128">Releases the mouse capture from a window in the current thread and restores normal mouse input processing.</span></span> <span data-ttu-id="ea694-129">Une fenêtre qui a capturé la souris reçoit toutes les entrées de la souris, quelle que soit la position du curseur, sauf si l’utilisateur clique sur un bouton de la souris alors que la zone réactive du curseur se trouve dans la fenêtre d’un autre thread.</span><span class="sxs-lookup"><span data-stu-id="ea694-129">A window that has captured the mouse receives all mouse input, regardless of the position of the cursor, except when a mouse button is clicked while the cursor hot spot is in the window of another thread.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ea694-130"><a href="/windows/desktop/api/winuser/nf-winuser-setcapture"><strong>SetCapture</strong></a></span><span class="sxs-lookup"><span data-stu-id="ea694-130"><a href="/windows/desktop/api/winuser/nf-winuser-setcapture"><strong>SetCapture</strong></a></span></span><br/></td>
<td><span data-ttu-id="ea694-131">Définit la capture de la souris sur la fenêtre spécifiée qui appartient au thread actuel.</span><span class="sxs-lookup"><span data-stu-id="ea694-131">Sets the mouse capture to the specified window belonging to the current thread.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ea694-132"><a href="/windows/desktop/api/winuser/nf-winuser-setdoubleclicktime"><strong>SetDoubleClickTime</strong></a></span><span class="sxs-lookup"><span data-stu-id="ea694-132"><a href="/windows/desktop/api/winuser/nf-winuser-setdoubleclicktime"><strong>SetDoubleClickTime</strong></a></span></span><br/></td>
<td><span data-ttu-id="ea694-133">Définit l’heure du double-clic de la souris.</span><span class="sxs-lookup"><span data-stu-id="ea694-133">Sets the double-click time for the mouse.</span></span> <span data-ttu-id="ea694-134">Un double-clic est une série de deux clics du bouton de la souris, le second se produisant dans un délai spécifié après le premier.</span><span class="sxs-lookup"><span data-stu-id="ea694-134">A double-click is a series of two clicks of a mouse button, the second occurring within a specified time after the first.</span></span> <span data-ttu-id="ea694-135">L’heure du double-clic correspond au nombre maximal de millisecondes qui peuvent se produire entre le premier et le deuxième clic d’un double-clic.</span><span class="sxs-lookup"><span data-stu-id="ea694-135">The double-click time is the maximum number of milliseconds that may occur between the first and second clicks of a double-click.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ea694-136"><a href="/windows/desktop/api/winuser/nf-winuser-swapmousebutton"><strong>SwapMouseButton</strong></a></span><span class="sxs-lookup"><span data-stu-id="ea694-136"><a href="/windows/desktop/api/winuser/nf-winuser-swapmousebutton"><strong>SwapMouseButton</strong></a></span></span><br/></td>
<td><span data-ttu-id="ea694-137">Inverse ou restaure la signification des boutons gauche et droit de la souris.</span><span class="sxs-lookup"><span data-stu-id="ea694-137">Reverses or restores the meaning of the left and right mouse buttons.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ea694-138"><a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>TrackMouseEvent</strong></a></span><span class="sxs-lookup"><span data-stu-id="ea694-138"><a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>TrackMouseEvent</strong></a></span></span><br/></td>
<td><span data-ttu-id="ea694-139">Publie des messages lorsque le pointeur de la souris quitte une fenêtre ou pointe sur une fenêtre pendant un laps de temps spécifié.</span><span class="sxs-lookup"><span data-stu-id="ea694-139">Posts messages when the mouse pointer leaves a window or hovers over a window for a specified amount of time.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="ea694-140">La fonction <a href="/windows/win32/api/commctrl/nf-commctrl-_trackmouseevent"><strong>_TrackMouseEvent</strong></a> appelle <a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>TrackMouseEvent</strong></a> si elle existe, sinon <strong>_TrackMouseEvent</strong> émule <strong>TrackMouseEvent</strong>.</span><span class="sxs-lookup"><span data-stu-id="ea694-140">The <a href="/windows/win32/api/commctrl/nf-commctrl-_trackmouseevent"><strong>_TrackMouseEvent</strong></a> function calls <a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>TrackMouseEvent</strong></a> if it exists, otherwise <strong>_TrackMouseEvent</strong> emulates <strong>TrackMouseEvent</strong>.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 

