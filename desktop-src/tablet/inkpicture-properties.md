---
description: Cette section contient les propriétés du contrôle InkPicture.
ms.assetid: d724c177-af57-4c99-94f2-c70904910b49
title: Propriétés de InkPicture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0ae8149098b34a70af5e088814e2a5258b0fa0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759526"
---
# <a name="inkpicture-properties"></a><span data-ttu-id="6bcd2-103">Propriétés de InkPicture</span><span class="sxs-lookup"><span data-stu-id="6bcd2-103">InkPicture Properties</span></span>

<span data-ttu-id="6bcd2-104">Cette section contient les propriétés du contrôle InkPicture.</span><span class="sxs-lookup"><span data-stu-id="6bcd2-104">This section contains Properties for the InkPicture Control.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6bcd2-105">Propriété</span><span class="sxs-lookup"><span data-stu-id="6bcd2-105">Property</span></span></th>
<th><span data-ttu-id="6bcd2-106">Description</span><span class="sxs-lookup"><span data-stu-id="6bcd2-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6bcd2-107"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_autoredraw"><strong>AutoRedraw, propriété</strong></a></span><span class="sxs-lookup"><span data-stu-id="6bcd2-107"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_autoredraw"><strong>AutoRedraw Property</strong></a></span></span></td>
<td><span data-ttu-id="6bcd2-108">Obtient ou définit une valeur qui spécifie si le contrôle <a href="inkpicture-control-reference.md">InkPicture</a> est repeint quand la fenêtre est invalidée (si l’objet <a href="inkdisp-class.md"><strong>InkDisp</strong></a> actuellement associé au contrôle InkPicture est redessiné automatiquement lorsque la fenêtre associée à l’inkpicture reçoit un message WM_PAINT).</span><span class="sxs-lookup"><span data-stu-id="6bcd2-108">Gets or sets a value that specifies whether the <a href="inkpicture-control-reference.md">InkPicture</a> control repaints when the window is invalidated (whether the <a href="inkdisp-class.md"><strong>InkDisp</strong></a> object currently associated with InkPicture control is automatically redrawn when the window associated with the InkPicture receives a WM_PAINT message).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6bcd2-109"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_backcolor"><strong>BackColor</strong></a></span><span class="sxs-lookup"><span data-stu-id="6bcd2-109"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_backcolor"><strong>BackColor</strong></a></span></span></td>
<td><span data-ttu-id="6bcd2-110">Obtient ou définit la couleur d’arrière-plan du contrôle <a href="inkpicture-control-reference.md">InkPicture</a> .</span><span class="sxs-lookup"><span data-stu-id="6bcd2-110">Gets or sets the background color for the <a href="inkpicture-control-reference.md">InkPicture</a> control.</span></span> <span data-ttu-id="6bcd2-111">La couleur d’arrière-plan par défaut est la couleur d’arrière-plan de la fenêtre système, qui est généralement blanche.</span><span class="sxs-lookup"><span data-stu-id="6bcd2-111">The default background color is the system window background color, which is typically white.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6bcd2-112"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectingink"><strong>Propriété CollectingInk</strong></a></span><span class="sxs-lookup"><span data-stu-id="6bcd2-112"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectingink"><strong>CollectingInk Property</strong></a></span></span></td>
<td><span data-ttu-id="6bcd2-113">Obtient la valeur qui spécifie si le contrôle <a href="inkpicture-control-reference.md">InkPicture</a> collecte l’encre (heure de l’exécution uniquement).</span><span class="sxs-lookup"><span data-stu-id="6bcd2-113">Gets the value that specifies whether the <a href="inkpicture-control-reference.md">InkPicture</a> control is collecting ink (run time only).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6bcd2-114"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode"><strong>CollectionMode</strong></a></span><span class="sxs-lookup"><span data-stu-id="6bcd2-114"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode"><strong>CollectionMode</strong></a></span></span></td>
<td><span data-ttu-id="6bcd2-115">Obtient ou définit le mode de collecte qui détermine si l’encre, les gestes ou l’encre et les gestes sont reconnus lorsque l’utilisateur écrit.</span><span class="sxs-lookup"><span data-stu-id="6bcd2-115">Gets or sets the collection mode that determines whether ink, gestures, or ink and gestures are recognized as the user writes.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6bcd2-116"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_cursors"><strong>Curseurs, propriété</strong></a></span><span class="sxs-lookup"><span data-stu-id="6bcd2-116"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_cursors"><strong>Cursors Property</strong></a></span></span></td>
<td><span data-ttu-id="6bcd2-117">Obtient la collection <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursors"><strong>IInkCursors</strong></a> disponible pour une utilisation dans la région d’entrée manuscrite du contrôle <a href="inkpicture-control-reference.md">InkPicture</a> .</span><span class="sxs-lookup"><span data-stu-id="6bcd2-117">Gets the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursors"><strong>IInkCursors</strong></a> collection available for use in the <a href="inkpicture-control-reference.md">InkPicture</a> control's inking region.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6bcd2-118"><a href="/previous-versions/windows/desktop/legacy/ms703274(v=vs.85)"><strong>CustomStrokes</strong></a></span><span class="sxs-lookup"><span data-stu-id="6bcd2-118"><a href="/previous-versions/windows/desktop/legacy/ms703274(v=vs.85)"><strong>CustomStrokes</strong></a></span></span></td>
<td><span data-ttu-id="6bcd2-119">Obtient la collection <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes"><strong>IInkCustomStrokes</strong></a> à rendre persistante avec l’encre (au moment de la conception uniquement).</span><span class="sxs-lookup"><span data-stu-id="6bcd2-119">Gets the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes"><strong>IInkCustomStrokes</strong></a> collection to be persisted with the ink (design-time only).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6bcd2-120"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_defaultdrawingattributes"><strong>Propriété DefaultDrawingAttributes</strong></a></span><span class="sxs-lookup"><span data-stu-id="6bcd2-120"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_defaultdrawingattributes"><strong>DefaultDrawingAttributes Property</strong></a></span></span></td>
<td><span data-ttu-id="6bcd2-121">Obtient ou définit la collection <a href="inkdrawingattributes-class.md"><strong>InkDrawingAttributes</strong></a> par défaut à utiliser lors du dessin et de l’affichage de l’encre (heure de l’exécution uniquement).</span><span class="sxs-lookup"><span data-stu-id="6bcd2-121">Gets or sets the default <a href="inkdrawingattributes-class.md"><strong>InkDrawingAttributes</strong></a> collection to use when drawing and displaying ink (run time only).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6bcd2-122"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_desiredpacketdescription"><strong>Propriété DesiredPacketDescription</strong></a></span><span class="sxs-lookup"><span data-stu-id="6bcd2-122"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_desiredpacketdescription"><strong>DesiredPacketDescription Property</strong></a></span></span></td>
<td><span data-ttu-id="6bcd2-123">Obtient ou définit la description du paquet du contrôle <a href="inkpicture-control-reference.md">InkPicture</a> (heure de l’exécution uniquement).</span><span class="sxs-lookup"><span data-stu-id="6bcd2-123">Gets or sets the packet description of the <a href="inkpicture-control-reference.md">InkPicture</a> control (run time only).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6bcd2-124"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_dynamicrendering"><strong>Propriété DynamicRendering</strong></a></span><span class="sxs-lookup"><span data-stu-id="6bcd2-124"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_dynamicrendering"><strong>DynamicRendering Property</strong></a></span></span></td>
<td><span data-ttu-id="6bcd2-125">Obtient ou définit la valeur qui spécifie si le contrôle <a href="inkpicture-control-reference.md">InkPicture</a> affiche dynamiquement l’encre au fur et à mesure de sa collecte.</span><span class="sxs-lookup"><span data-stu-id="6bcd2-125">Gets or sets the value that specifies whether the <a href="inkpicture-control-reference.md">InkPicture</a> control dynamically renders the ink as it is collected.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6bcd2-126"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_editingmode"><strong>EditingMode</strong></a></span><span class="sxs-lookup"><span data-stu-id="6bcd2-126"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_editingmode"><strong>EditingMode</strong></a></span></span></td>
<td><span data-ttu-id="6bcd2-127">Obtient ou définit une valeur qui spécifie si le contrôle <a href="inkpicture-control-reference.md">InkPicture</a> est en mode Ink, en mode de suppression ou en mode de sélection/modification.</span><span class="sxs-lookup"><span data-stu-id="6bcd2-127">Gets or sets a value that specifies whether the <a href="inkpicture-control-reference.md">InkPicture</a> control is in ink mode, deletion mode, or selecting/editing mode.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6bcd2-128"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_enabled"><strong>Enabled</strong></a></span><span class="sxs-lookup"><span data-stu-id="6bcd2-128"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_enabled"><strong>Enabled</strong></a></span></span></td>
<td><span data-ttu-id="6bcd2-129">Obtient ou définit une valeur qui détermine si le contrôle <a href="inkpicture-control-reference.md">InkPicture</a> peut répondre aux événements générés par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6bcd2-129">Gets or sets a value that determines whether the <a href="inkpicture-control-reference.md">InkPicture</a> control can respond to user-generated events.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="6bcd2-130">Cette propriété est équivalente à la propriété <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled"><strong>InkEnabled</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="6bcd2-130">This property is equivalent to the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled"><strong>InkEnabled</strong></a> property.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6bcd2-131"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_erasermode"><strong>EraserMode</strong></a></span><span class="sxs-lookup"><span data-stu-id="6bcd2-131"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_erasermode"><strong>EraserMode</strong></a></span></span></td>
<td><span data-ttu-id="6bcd2-132">Obtient ou définit la valeur qui spécifie si l’encre est effacée par trait ou par point.</span><span class="sxs-lookup"><span data-stu-id="6bcd2-132">Gets or sets the value that specifies whether ink is erased by stroke or by point.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6bcd2-133"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_eraserwidth"><strong>EraserWidth</strong></a></span><span class="sxs-lookup"><span data-stu-id="6bcd2-133"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_eraserwidth"><strong>EraserWidth</strong></a></span></span></td>
<td><span data-ttu-id="6bcd2-134">Obtient ou définit la valeur qui spécifie la largeur de l’info-bulle du stylet de gomme.</span><span class="sxs-lookup"><span data-stu-id="6bcd2-134">Gets or sets the value that specifies the width of the eraser pen tip.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6bcd2-135"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_hwnd"><strong>hWnd</strong></a></span><span class="sxs-lookup"><span data-stu-id="6bcd2-135"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_hwnd"><strong>hWnd</strong></a></span></span></td>
<td><span data-ttu-id="6bcd2-136">Obtient le handle de fenêtre auquel le contrôle <a href="inkpicture-control-reference.md">InkPicture</a> est lié.</span><span class="sxs-lookup"><span data-stu-id="6bcd2-136">Gets the window handle to which the <a href="inkpicture-control-reference.md">InkPicture</a> control is bound.</span></span> <span data-ttu-id="6bcd2-137">(heure de l’exécution uniquement)</span><span class="sxs-lookup"><span data-stu-id="6bcd2-137">(run time only)</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6bcd2-138"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink"><strong>Entrée manuscrite</strong></a></span><span class="sxs-lookup"><span data-stu-id="6bcd2-138"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink"><strong>Ink</strong></a></span></span></td>
<td><span data-ttu-id="6bcd2-139">Obtient ou définit l’objet <a href="inkdisp-class.md"><strong>InkDisp</strong></a> associé au contrôle <a href="inkpicture-control-reference.md">InkPicture</a> (heure de l’exécution uniquement).</span><span class="sxs-lookup"><span data-stu-id="6bcd2-139">Gets or sets the <a href="inkdisp-class.md"><strong>InkDisp</strong></a> object that is associated with the <a href="inkpicture-control-reference.md">InkPicture</a> control (run time only).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6bcd2-140"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled"><strong>InkEnabled</strong></a></span><span class="sxs-lookup"><span data-stu-id="6bcd2-140"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled"><strong>InkEnabled</strong></a></span></span></td>
<td><span data-ttu-id="6bcd2-141">Obtient ou définit une valeur qui spécifie si le contrôle <a href="inkpicture-control-reference.md">InkPicture</a> collecte les entrées de stylet (paquets in-air, curseurs dans les événements de plage, etc.).</span><span class="sxs-lookup"><span data-stu-id="6bcd2-141">Gets or sets a value that specifies whether the <a href="inkpicture-control-reference.md">InkPicture</a> control collects pen input (in-air packets, cursor in range events, and so on).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6bcd2-142"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_marginx"><strong>Propriété MarginX</strong></a></span><span class="sxs-lookup"><span data-stu-id="6bcd2-142"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_marginx"><strong>MarginX Property</strong></a></span></span></td>
<td><span data-ttu-id="6bcd2-143">Obtient ou définit la marge de l’axe x autour du rectangle de la fenêtre en coordonnées d’écran.</span><span class="sxs-lookup"><span data-stu-id="6bcd2-143">Gets or sets the x-axis margin around the window rectangle in screen coordinates.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6bcd2-144"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_marginy"><strong>MarginY (propriété)</strong></a></span><span class="sxs-lookup"><span data-stu-id="6bcd2-144"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_marginy"><strong>MarginY Property</strong></a></span></span></td>
<td><span data-ttu-id="6bcd2-145">Obtient ou définit la marge de l’axe y autour du rectangle de la fenêtre en coordonnées d’écran.</span><span class="sxs-lookup"><span data-stu-id="6bcd2-145">Gets or sets the y-axis margin around the window rectangle in screen coordinates.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6bcd2-146"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_mouseicon"><strong>Propriété MouseIcon</strong></a></span><span class="sxs-lookup"><span data-stu-id="6bcd2-146"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_mouseicon"><strong>MouseIcon Property</strong></a></span></span></td>
<td><span data-ttu-id="6bcd2-147">Obtient ou définit l’icône de souris personnalisée actuelle.</span><span class="sxs-lookup"><span data-stu-id="6bcd2-147">Gets or sets the current custom mouse icon.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6bcd2-148"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_mousepointer"><strong>MousePointer, propriété</strong></a></span><span class="sxs-lookup"><span data-stu-id="6bcd2-148"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_mousepointer"><strong>MousePointer Property</strong></a></span></span></td>
<td><span data-ttu-id="6bcd2-149">Obtient ou définit une valeur qui indique le type de pointeur de la souris qui apparaît lorsque la souris se trouve sur une partie particulière du contrôle <a href="inkpicture-control-reference.md">InkPicture</a> .</span><span class="sxs-lookup"><span data-stu-id="6bcd2-149">Gets or sets a value that indicates the type of mouse pointer that appears when the mouse is over a particular part of the <a href="inkpicture-control-reference.md">InkPicture</a> control.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6bcd2-150"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_picture"><strong>Aperçu</strong></a></span><span class="sxs-lookup"><span data-stu-id="6bcd2-150"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_picture"><strong>Picture</strong></a></span></span></td>
<td><span data-ttu-id="6bcd2-151">Obtient le fichier graphique à afficher sur le contrôle <a href="inkpicture-control-reference.md">InkPicture</a> .</span><span class="sxs-lookup"><span data-stu-id="6bcd2-151">Gets the graphics file to appear on the <a href="inkpicture-control-reference.md">InkPicture</a> control.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6bcd2-152"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_renderer"><strong>Renderer (propriété)</strong></a></span><span class="sxs-lookup"><span data-stu-id="6bcd2-152"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_renderer"><strong>Renderer Property</strong></a></span></span></td>
<td><span data-ttu-id="6bcd2-153">Obtient ou définit l’objet <a href="inkrenderer-class.md"><strong>InkRenderer</strong></a> utilisé pour dessiner de l’encre sur le contrôle <a href="inkpicture-control-reference.md">InkPicture</a> (heure de l’exécution uniquement).</span><span class="sxs-lookup"><span data-stu-id="6bcd2-153">Gets or sets the <a href="inkrenderer-class.md"><strong>InkRenderer</strong></a> object that is used to draw ink on the <a href="inkpicture-control-reference.md">InkPicture</a> control (run time only).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6bcd2-154"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection"><strong>Sélection</strong></a></span><span class="sxs-lookup"><span data-stu-id="6bcd2-154"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection"><strong>Selection</strong></a></span></span></td>
<td><span data-ttu-id="6bcd2-155">Obtient la collection <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> actuellement sélectionnée dans le contrôle <a href="inkpicture-control-reference.md">InkPicture</a> (heure de l’exécution uniquement).</span><span class="sxs-lookup"><span data-stu-id="6bcd2-155">Gets the <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection currently selected inside the <a href="inkpicture-control-reference.md">InkPicture</a> control (run time only).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6bcd2-156"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode"><strong>SizeMode</strong></a></span><span class="sxs-lookup"><span data-stu-id="6bcd2-156"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode"><strong>SizeMode</strong></a></span></span></td>
<td><span data-ttu-id="6bcd2-157">Obtient ou définit la manière dont le contrôle gère le placement et le dimensionnement de l’image.</span><span class="sxs-lookup"><span data-stu-id="6bcd2-157">Gets or sets how the control handles image placement and sizing.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6bcd2-158"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_supporthighcontrastink"><strong>Propriété SupportHighContrastInk</strong></a></span><span class="sxs-lookup"><span data-stu-id="6bcd2-158"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_supporthighcontrastink"><strong>SupportHighContrastInk Property</strong></a></span></span></td>
<td><span data-ttu-id="6bcd2-159">Obtient une valeur qui spécifie si l’entrée manuscrite est rendue sous la forme d’une seule couleur, Color = COLOR_WINDOWTEXT (à partir de l’appel GetSystemMetrics) lorsque le système est en mode contraste élevé.</span><span class="sxs-lookup"><span data-stu-id="6bcd2-159">Gets a value that specifies whether ink is rendered as just one color, Color = COLOR_WINDOWTEXT (from the GetSystemMetrics call) when the system is in High Contrast mode.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6bcd2-160"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_supporthighcontrastselectionui"><strong>SupportHighContrastSelectionUI</strong></a></span><span class="sxs-lookup"><span data-stu-id="6bcd2-160"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_supporthighcontrastselectionui"><strong>SupportHighContrastSelectionUI</strong></a></span></span></td>
<td><span data-ttu-id="6bcd2-161">Obtient ou définit une valeur qui spécifie si toutes les interfaces utilisateur de sélection (poignées de sélection et de cadre englobant de sélection) sont dessinées en contraste élevé lorsque le système est en mode contraste élevé.</span><span class="sxs-lookup"><span data-stu-id="6bcd2-161">Gets or sets a value that specifies whether all selection user interfaces (selection bounding box and selection handles) are drawn in high contrast when the system is in High Contrast mode.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6bcd2-162"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_tablet"><strong>Propriété de tablette</strong></a></span><span class="sxs-lookup"><span data-stu-id="6bcd2-162"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_tablet"><strong>Tablet Property</strong></a></span></span></td>
<td><span data-ttu-id="6bcd2-163">Obtient l’objet <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet"><strong>IInkTablet</strong></a> actuellement utilisé par le contrôle <a href="inkpicture-control-reference.md">InkPicture</a> pour collecter l’entrée.</span><span class="sxs-lookup"><span data-stu-id="6bcd2-163">Gets the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet"><strong>IInkTablet</strong></a> object that the <a href="inkpicture-control-reference.md">InkPicture</a> control is currently using to collect input.</span></span><br/></td>
</tr>
</tbody>
</table>



 

