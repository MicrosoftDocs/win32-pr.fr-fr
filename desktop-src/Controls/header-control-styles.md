---
title: Styles de contrôle d’en-tête (CommCtrl. h)
description: Les contrôles Header ont plusieurs styles, décrits dans cette section, qui déterminent l’apparence et le comportement du contrôle. Vous définissez les styles initiaux lorsque vous créez le contrôle header.
ms.assetid: e47dc6c3-a1af-456c-9235-29ce63f1e13b
topic_type:
- apiref
api_name:
- HDS_BUTTONS
- HDS_DRAGDROP
- HDS_FILTERBAR
- HDS_FLAT
- HDS_FULLDRAG
- HDS_HIDDEN
- HDS_HORZ
- HDS_HOTTRACK
- HDS_CHECKBOXES
- HDS_NOSIZING
- HDS_OVERFLOW
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d8450ad39cdb965e3e4be15f0093ec4737a87c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545444"
---
# <a name="header-control-styles"></a><span data-ttu-id="879b7-104">Styles de contrôle d’en-tête</span><span class="sxs-lookup"><span data-stu-id="879b7-104">Header Control Styles</span></span>

<span data-ttu-id="879b7-105">Les contrôles Header ont plusieurs styles, décrits dans cette section, qui déterminent l’apparence et le comportement du contrôle.</span><span class="sxs-lookup"><span data-stu-id="879b7-105">Header controls have a number of styles, described in this section, that determine the control's appearance and behavior.</span></span> <span data-ttu-id="879b7-106">Vous définissez les styles initiaux lorsque vous créez le contrôle header.</span><span class="sxs-lookup"><span data-stu-id="879b7-106">You set the initial styles when you create the header control.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="879b7-107">Constante</span><span class="sxs-lookup"><span data-stu-id="879b7-107">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="879b7-108">Description</span><span class="sxs-lookup"><span data-stu-id="879b7-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_BUTTONS"></span><span id="hds_buttons"></span><dl> <span data-ttu-id="879b7-109"><dt><strong>HDS_BUTTONS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="879b7-109"><dt><strong>HDS_BUTTONS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="879b7-110">Chaque élément du contrôle apparaît et se comporte comme un bouton de commande.</span><span class="sxs-lookup"><span data-stu-id="879b7-110">Each item in the control looks and behaves like a push button.</span></span> <span data-ttu-id="879b7-111">Ce style est utile si une application exécute une tâche quand l’utilisateur clique sur un élément dans le contrôle d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="879b7-111">This style is useful if an application carries out a task when the user clicks an item in the header control.</span></span> <span data-ttu-id="879b7-112">Par exemple, une application peut trier les informations dans les colonnes différemment en fonction de l’élément sur lequel l’utilisateur clique.</span><span class="sxs-lookup"><span data-stu-id="879b7-112">For example, an application could sort information in the columns differently depending on which item the user clicks.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_DRAGDROP"></span><span id="hds_dragdrop"></span><dl> <span data-ttu-id="879b7-113"><dt><strong>HDS_DRAGDROP</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="879b7-113"><dt><strong>HDS_DRAGDROP</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="879b7-114">Autorise la réorganisation des éléments d’en-tête par glisser-déplacer.</span><span class="sxs-lookup"><span data-stu-id="879b7-114">Allows drag-and-drop reordering of header items.</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_FILTERBAR"></span><span id="hds_filterbar"></span><dl> <span data-ttu-id="879b7-115"><dt><strong>HDS_FILTERBAR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="879b7-115"><dt><strong>HDS_FILTERBAR</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="879b7-116">Ajoutez une barre de filtre dans le cadre du contrôle d’en-tête standard.</span><span class="sxs-lookup"><span data-stu-id="879b7-116">Include a filter bar as part of the standard header control.</span></span> <span data-ttu-id="879b7-117">Cette barre permet aux utilisateurs d’appliquer facilement un filtre à l’affichage.</span><span class="sxs-lookup"><span data-stu-id="879b7-117">This bar allows users to conveniently apply a filter to the display.</span></span> <span data-ttu-id="879b7-118">Les appels à <a href="hdm-layout.md"><strong>HDM_LAYOUT</strong></a> entraînent une nouvelle taille pour le contrôle et provoquent la mise à jour du mode liste.</span><span class="sxs-lookup"><span data-stu-id="879b7-118">Calls to <a href="hdm-layout.md"><strong>HDM_LAYOUT</strong></a> will yield a new size for the control and cause the list view to update.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_FLAT"></span><span id="hds_flat"></span><dl> <span data-ttu-id="879b7-119"><dt><strong>HDS_FLAT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="879b7-119"><dt><strong>HDS_FLAT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="879b7-120"><a href="common-control-versions.md">Version 6,0 et versions ultérieures</a>.</span><span class="sxs-lookup"><span data-stu-id="879b7-120"><a href="common-control-versions.md">Version 6.0 and later</a>.</span></span> <span data-ttu-id="879b7-121">Fait en sorte que le contrôle d’en-tête soit dessiné à plat lorsque le système d’exploitation s’exécute en mode classique.</span><span class="sxs-lookup"><span data-stu-id="879b7-121">Causes the header control to be drawn flat when the operating system is running in classic mode.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="879b7-122">Comctl32.dll version 6 n’est pas redistribuable, mais elle est incluse dans Windows.</span><span class="sxs-lookup"><span data-stu-id="879b7-122">Comctl32.dll version 6 is not redistributable but it is included in Windows.</span></span> <span data-ttu-id="879b7-123">Pour utiliser Comctl32.dll version 6, spécifiez-la dans un manifeste.</span><span class="sxs-lookup"><span data-stu-id="879b7-123">To use Comctl32.dll version 6, specify it in a manifest.</span></span> <span data-ttu-id="879b7-124">Pour plus d’informations sur les manifestes, consultez <a href="cookbook-overview.md">activation des styles visuels</a>.</span><span class="sxs-lookup"><span data-stu-id="879b7-124">For more information on manifests, see <a href="cookbook-overview.md">Enabling Visual Styles</a>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_FULLDRAG"></span><span id="hds_fulldrag"></span><dl> <span data-ttu-id="879b7-125"><dt><strong>HDS_FULLDRAG</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="879b7-125"><dt><strong>HDS_FULLDRAG</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="879b7-126">Fait en sorte que le contrôle header affiche le contenu des colonnes même lorsque l’utilisateur redimensionne une colonne.</span><span class="sxs-lookup"><span data-stu-id="879b7-126">Causes the header control to display column contents even while the user resizes a column.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_HIDDEN"></span><span id="hds_hidden"></span><dl> <span data-ttu-id="879b7-127"><dt><strong>HDS_HIDDEN</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="879b7-127"><dt><strong>HDS_HIDDEN</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="879b7-128">Indique un contrôle d’en-tête destiné à être masqué.</span><span class="sxs-lookup"><span data-stu-id="879b7-128">Indicates a header control that is intended to be hidden.</span></span> <span data-ttu-id="879b7-129">Ce style ne masque pas le contrôle.</span><span class="sxs-lookup"><span data-stu-id="879b7-129">This style does not hide the control.</span></span> <span data-ttu-id="879b7-130">Au lieu de cela, lorsque vous envoyez le message <a href="hdm-layout.md"><strong>HDM_LAYOUT</strong></a> à un contrôle d’en-tête avec le style HDS_HIDDEN, le contrôle retourne zéro dans le membre <strong>CY</strong> de la structure <a href="/windows/win32/api/winuser/ns-winuser-windowpos"><strong>WINDOWPOS</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="879b7-130">Instead, when you send the <a href="hdm-layout.md"><strong>HDM_LAYOUT</strong></a> message to a header control with the HDS_HIDDEN style, the control returns zero in the <strong>cy</strong> member of the <a href="/windows/win32/api/winuser/ns-winuser-windowpos"><strong>WINDOWPOS</strong></a> structure.</span></span> <span data-ttu-id="879b7-131">Vous masquez ensuite le contrôle en affectant à sa hauteur la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="879b7-131">You would then hide the control by setting its height to zero.</span></span> <span data-ttu-id="879b7-132">Cela peut être utile lorsque vous souhaitez utiliser le contrôle comme conteneur d’informations au lieu d’un contrôle visuel.</span><span class="sxs-lookup"><span data-stu-id="879b7-132">This can be useful when you want to use the control as an information container instead of a visual control.</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_HORZ"></span><span id="hds_horz"></span><dl> <span data-ttu-id="879b7-133"><dt><strong>HDS_HORZ</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="879b7-133"><dt><strong>HDS_HORZ</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="879b7-134">Crée un contrôle d’en-tête avec une orientation horizontale.</span><span class="sxs-lookup"><span data-stu-id="879b7-134">Creates a header control with a horizontal orientation.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_HOTTRACK"></span><span id="hds_hottrack"></span><dl> <span data-ttu-id="879b7-135"><dt><strong>HDS_HOTTRACK</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="879b7-135"><dt><strong>HDS_HOTTRACK</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="879b7-136">Active le suivi réactif.</span><span class="sxs-lookup"><span data-stu-id="879b7-136">Enables hot tracking.</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_CHECKBOXES"></span><span id="hds_checkboxes"></span><dl> <span data-ttu-id="879b7-137"><dt><strong>HDS_CHECKBOXES</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="879b7-137"><dt><strong>HDS_CHECKBOXES</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="879b7-138"><a href="common-control-versions.md">Version 6,00 et versions ultérieures</a>.</span><span class="sxs-lookup"><span data-stu-id="879b7-138"><a href="common-control-versions.md">Version 6.00 and later</a>.</span></span> <span data-ttu-id="879b7-139">Autorise le placement de cases à cocher sur les éléments d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="879b7-139">Allows the placing of checkboxes on header items.</span></span> <span data-ttu-id="879b7-140">Pour plus d’informations, consultez le membre <strong>fmt</strong> de <a href="/windows/win32/api/commctrl/ns-commctrl-hditema"><strong>HDITEM</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="879b7-140">For more information, see the <strong>fmt</strong> member of <a href="/windows/win32/api/commctrl/ns-commctrl-hditema"><strong>HDITEM</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_NOSIZING"></span><span id="hds_nosizing"></span><dl> <span data-ttu-id="879b7-141"><dt><strong>HDS_NOSIZING</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="879b7-141"><dt><strong>HDS_NOSIZING</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="879b7-142"><a href="common-control-versions.md">Version 6,00 et versions ultérieures</a>.</span><span class="sxs-lookup"><span data-stu-id="879b7-142"><a href="common-control-versions.md">Version 6.00 and later</a>.</span></span> <span data-ttu-id="879b7-143">L’utilisateur ne peut pas faire glisser le séparateur sur le contrôle header.</span><span class="sxs-lookup"><span data-stu-id="879b7-143">The user cannot drag the divider on the header control.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_OVERFLOW"></span><span id="hds_overflow"></span><dl> <span data-ttu-id="879b7-144"><dt><strong>HDS_OVERFLOW</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="879b7-144"><dt><strong>HDS_OVERFLOW</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="879b7-145"><a href="common-control-versions.md">Version 6,00 et versions ultérieures</a>.</span><span class="sxs-lookup"><span data-stu-id="879b7-145"><a href="common-control-versions.md">Version 6.00 and later</a>.</span></span> <span data-ttu-id="879b7-146">Un bouton s’affiche lorsque tous les éléments ne peuvent pas être affichés dans le rectangle du contrôle header.</span><span class="sxs-lookup"><span data-stu-id="879b7-146">A button is displayed when not all items can be displayed within the header control's rectangle.</span></span> <span data-ttu-id="879b7-147">Lorsque vous cliquez dessus, ce bouton envoie une notification <a href="hdn-overflowclick.md">HDN_OVERFLOWCLICK</a> .</span><span class="sxs-lookup"><span data-stu-id="879b7-147">When clicked, this button sends an <a href="hdn-overflowclick.md">HDN_OVERFLOWCLICK</a> notification.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="879b7-148">Notes</span><span class="sxs-lookup"><span data-stu-id="879b7-148">Remarks</span></span>

<span data-ttu-id="879b7-149">Pour récupérer et modifier les styles après avoir créé le contrôle, utilisez les fonctions [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) et [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) .</span><span class="sxs-lookup"><span data-stu-id="879b7-149">To retrieve and change the styles after creating the control, use the [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) and [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="879b7-150">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="879b7-150">Requirements</span></span>



| <span data-ttu-id="879b7-151">Condition requise</span><span class="sxs-lookup"><span data-stu-id="879b7-151">Requirement</span></span> | <span data-ttu-id="879b7-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="879b7-152">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="879b7-153">En-tête</span><span class="sxs-lookup"><span data-stu-id="879b7-153">Header</span></span><br/> | <dl> <span data-ttu-id="879b7-154"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="879b7-154"><dt>CommCtrl.h</dt></span></span> </dl> |



