---
title: Styles étendus de la barre d’outils (CommCtrl. h)
description: Cette section répertorie les styles étendus pris en charge par les contrôles ToolBar.
ms.assetid: da31dbbf-8d0a-4711-a1af-382c62e653cd
topic_type:
- apiref
api_name:
- TBSTYLE_EX_DRAWDDARROWS
- TBSTYLE_EX_HIDECLIPPEDBUTTONS
- TBSTYLE_EX_DOUBLEBUFFER
- TBSTYLE_EX_MIXEDBUTTONS
- TBSTYLE_EX_MULTICOLUMN
- TBSTYLE_EX_VERTICAL
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 056e48753485364017f04f7b84e609b19473bf5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528697"
---
# <a name="toolbar-extended-styles"></a><span data-ttu-id="cc321-103">Styles étendus de la barre d’outils</span><span class="sxs-lookup"><span data-stu-id="cc321-103">Toolbar Extended Styles</span></span>

<span data-ttu-id="cc321-104">Cette section répertorie les styles étendus pris en charge par les contrôles ToolBar.</span><span class="sxs-lookup"><span data-stu-id="cc321-104">This section lists the extended styles supported by toolbar controls.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="cc321-105">Constante</span><span class="sxs-lookup"><span data-stu-id="cc321-105">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="cc321-106">Description</span><span class="sxs-lookup"><span data-stu-id="cc321-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="TBSTYLE_EX_DRAWDDARROWS"></span><span id="tbstyle_ex_drawddarrows"></span><dl> <span data-ttu-id="cc321-107"><dt><strong>TBSTYLE_EX_DRAWDDARROWS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="cc321-107"><dt><strong>TBSTYLE_EX_DRAWDDARROWS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="cc321-108"><a href="common-control-versions.md">Version 4,71</a>.</span><span class="sxs-lookup"><span data-stu-id="cc321-108"><a href="common-control-versions.md">Version 4.71</a>.</span></span> <span data-ttu-id="cc321-109">Ce style permet aux boutons d’avoir une flèche déroulante distincte.</span><span class="sxs-lookup"><span data-stu-id="cc321-109">This style allows buttons to have a separate dropdown arrow.</span></span> <span data-ttu-id="cc321-110">Les boutons qui ont le style <a href="toolbar-control-and-button-styles.md"><strong>BTNS_DROPDOWN</strong></a> sont dessinés avec une flèche déroulante dans une section distincte, à droite du bouton.</span><span class="sxs-lookup"><span data-stu-id="cc321-110">Buttons that have the <a href="toolbar-control-and-button-styles.md"><strong>BTNS_DROPDOWN</strong></a> style will be drawn with a dropdown arrow in a separate section, to the right of the button.</span></span> <span data-ttu-id="cc321-111">Si vous cliquez sur la flèche, seule la partie de la flèche du bouton est déenfoncée et le contrôle ToolBar envoie un <a href="tbn-dropdown.md">TBN_DROPDOWN</a> code de notification pour inviter l’application à afficher le menu déroulant.</span><span class="sxs-lookup"><span data-stu-id="cc321-111">If the arrow is clicked, only the arrow portion of the button will depress, and the toolbar control will send a <a href="tbn-dropdown.md">TBN_DROPDOWN</a> notification code to prompt the application to display the dropdown menu.</span></span> <span data-ttu-id="cc321-112">Si l’utilisateur clique sur la partie principale du bouton, le contrôle ToolBar envoie un message WM_COMMAND avec l’ID du bouton.</span><span class="sxs-lookup"><span data-stu-id="cc321-112">If the main part of the button is clicked, the toolbar control sends a WM_COMMAND message with the button's ID.</span></span> <span data-ttu-id="cc321-113">L’application répond normalement en lançant la première commande dans le menu.</span><span class="sxs-lookup"><span data-stu-id="cc321-113">The application normally responds by launching the first command on the menu.</span></span><br/> <span data-ttu-id="cc321-114">Dans de nombreuses situations, vous pouvez souhaiter avoir uniquement certains des boutons déroulants dans une barre d’outils avec des flèches séparées.</span><span class="sxs-lookup"><span data-stu-id="cc321-114">There are many situations where you may want to have only some of the dropdown buttons on a toolbar with separated arrows.</span></span> <span data-ttu-id="cc321-115">Pour ce faire, définissez le TBSTYLE_EX_DRAWDDARROWS style étendu.</span><span class="sxs-lookup"><span data-stu-id="cc321-115">To do so, set the TBSTYLE_EX_DRAWDDARROWS extended style.</span></span> <span data-ttu-id="cc321-116">Donnez aux boutons qui n’ont pas de flèches séparées le style <a href="toolbar-control-and-button-styles.md"><strong>BTNS_WHOLEDROPDOWN</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="cc321-116">Give those buttons that will not have separated arrows the <a href="toolbar-control-and-button-styles.md"><strong>BTNS_WHOLEDROPDOWN</strong></a> style.</span></span> <span data-ttu-id="cc321-117">Les boutons avec ce style comporteront une flèche affichée en regard de l’image.</span><span class="sxs-lookup"><span data-stu-id="cc321-117">Buttons with this style will have an arrow displayed next to the image.</span></span> <span data-ttu-id="cc321-118">Toutefois, la flèche n’est pas distincte et lorsqu’un utilisateur clique sur une partie du bouton, le contrôle ToolBar envoie un <a href="tbn-dropdown.md">TBN_DROPDOWN</a> code de notification.</span><span class="sxs-lookup"><span data-stu-id="cc321-118">However, the arrow will not be separate and when any part of the button is clicked, the toolbar control will send a <a href="tbn-dropdown.md">TBN_DROPDOWN</a> notification code.</span></span> <span data-ttu-id="cc321-119">Pour éviter les problèmes de redessination, ce style doit être défini avant que le contrôle de barre d’outils ne devienne visible.</span><span class="sxs-lookup"><span data-stu-id="cc321-119">To prevent repainting problems, this style should be set before the toolbar control becomes visible.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="TBSTYLE_EX_HIDECLIPPEDBUTTONS"></span><span id="tbstyle_ex_hideclippedbuttons"></span><dl> <span data-ttu-id="cc321-120"><dt><strong>TBSTYLE_EX_HIDECLIPPEDBUTTONS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="cc321-120"><dt><strong>TBSTYLE_EX_HIDECLIPPEDBUTTONS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="cc321-121"><a href="common-control-versions.md">Version 5,81</a>.</span><span class="sxs-lookup"><span data-stu-id="cc321-121"><a href="common-control-versions.md">Version 5.81</a>.</span></span> <span data-ttu-id="cc321-122">Ce style masque les boutons partiellement découpés.</span><span class="sxs-lookup"><span data-stu-id="cc321-122">This style hides partially clipped buttons.</span></span> <span data-ttu-id="cc321-123">L’utilisation la plus courante de ce style est pour les barres d’outils qui font partie d’un contrôle rebar.</span><span class="sxs-lookup"><span data-stu-id="cc321-123">The most common use of this style is for toolbars that are part of a rebar control.</span></span> <span data-ttu-id="cc321-124">Si une bande adjacente couvre une partie d’un bouton, le bouton ne s’affiche pas.</span><span class="sxs-lookup"><span data-stu-id="cc321-124">If an adjacent band covers part of a button, the button will not be displayed.</span></span> <span data-ttu-id="cc321-125">Toutefois, si la bande rebar a le style <a href="/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa"><strong>RBBS_USECHEVRON</strong></a> , le bouton s’affiche dans le menu déroulant du Chevron.</span><span class="sxs-lookup"><span data-stu-id="cc321-125">However, if the rebar band has the <a href="/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa"><strong>RBBS_USECHEVRON</strong></a> style, the button will be displayed on the chevron's dropdown menu.</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="TBSTYLE_EX_DOUBLEBUFFER"></span><span id="tbstyle_ex_doublebuffer"></span><dl> <span data-ttu-id="cc321-126"><dt><strong>TBSTYLE_EX_DOUBLEBUFFER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="cc321-126"><dt><strong>TBSTYLE_EX_DOUBLEBUFFER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="cc321-127"><a href="common-control-versions.md">Version 6</a>.</span><span class="sxs-lookup"><span data-stu-id="cc321-127"><a href="common-control-versions.md">Version 6</a>.</span></span> <span data-ttu-id="cc321-128">Ce style requiert la double mise en mémoire tampon de la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="cc321-128">This style requires the toolbar to be double buffered.</span></span> <span data-ttu-id="cc321-129">La double mise en mémoire tampon est un mécanisme qui détecte quand la barre d’outils a changé.</span><span class="sxs-lookup"><span data-stu-id="cc321-129">Double buffering is a mechanism that detects when the toolbar has changed.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="cc321-130">Comctl32.dll version 6 n’est pas redistribuable, mais elle est incluse dans Windows ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="cc321-130">Comctl32.dll version 6 is not redistributable but it is included in Windows or later.</span></span> <span data-ttu-id="cc321-131">Pour utiliser Comctl32.dll version 6, spécifiez-la dans un manifeste.</span><span class="sxs-lookup"><span data-stu-id="cc321-131">To use Comctl32.dll version 6, specify it in a manifest.</span></span> <span data-ttu-id="cc321-132">Pour plus d’informations sur les manifestes, consultez <a href="cookbook-overview.md">activation des styles visuels</a>.</span><span class="sxs-lookup"><span data-stu-id="cc321-132">For more information on manifests, see <a href="cookbook-overview.md">Enabling Visual Styles</a>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="TBSTYLE_EX_MIXEDBUTTONS"></span><span id="tbstyle_ex_mixedbuttons"></span><dl> <span data-ttu-id="cc321-133"><dt><strong>TBSTYLE_EX_MIXEDBUTTONS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="cc321-133"><dt><strong>TBSTYLE_EX_MIXEDBUTTONS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="cc321-134"><a href="common-control-versions.md">Version 5,81</a>.</span><span class="sxs-lookup"><span data-stu-id="cc321-134"><a href="common-control-versions.md">Version 5.81</a>.</span></span> <span data-ttu-id="cc321-135">Ce style vous permet de définir du texte pour tous les boutons, mais uniquement de les afficher pour ces boutons avec le style de bouton <a href="toolbar-control-and-button-styles.md"><strong>BTNS_SHOWTEXT</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="cc321-135">This style allows you to set text for all buttons, but only display it for those buttons with the <a href="toolbar-control-and-button-styles.md"><strong>BTNS_SHOWTEXT</strong></a> button style.</span></span> <span data-ttu-id="cc321-136">Le style de <a href="toolbar-control-and-button-styles.md"><strong>TBSTYLE_LIST</strong></a> doit également être défini.</span><span class="sxs-lookup"><span data-stu-id="cc321-136">The <a href="toolbar-control-and-button-styles.md"><strong>TBSTYLE_LIST</strong></a> style must also be set.</span></span> <span data-ttu-id="cc321-137">Normalement, lorsqu’un bouton n’affiche pas de texte, votre application doit gérer <a href="tbn-getinfotip.md">TBN_GETINFOTIP</a> ou <a href="ttn-getdispinfo.md">TTN_GETDISPINFO</a> pour afficher une info-bulle.</span><span class="sxs-lookup"><span data-stu-id="cc321-137">Normally, when a button does not display text, your application must handle <a href="tbn-getinfotip.md">TBN_GETINFOTIP</a> or <a href="ttn-getdispinfo.md">TTN_GETDISPINFO</a> to display a tooltip.</span></span> <span data-ttu-id="cc321-138">Avec le style étendu TBSTYLE_EX_MIXEDBUTTONS, le texte qui est défini mais qui n’est pas affiché sur un bouton sera automatiquement utilisé comme texte info-bulle du bouton.</span><span class="sxs-lookup"><span data-stu-id="cc321-138">With the TBSTYLE_EX_MIXEDBUTTONS extended style, text that is set but not displayed on a button will automatically be used as the button's tooltip text.</span></span> <span data-ttu-id="cc321-139">Votre application doit uniquement gérer TBN_GETINFOTIP ou ou TTN_GETDISPINFO si elle a besoin d’une plus grande flexibilité pour la spécification du texte d’info-bulle.</span><span class="sxs-lookup"><span data-stu-id="cc321-139">Your application only needs to handle TBN_GETINFOTIP or or TTN_GETDISPINFO if it needs more flexibility in specifying the tooltip text.</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="TBSTYLE_EX_MULTICOLUMN"></span><span id="tbstyle_ex_multicolumn"></span><dl> <span data-ttu-id="cc321-140"><dt><strong>TBSTYLE_EX_MULTICOLUMN</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="cc321-140"><dt><strong>TBSTYLE_EX_MULTICOLUMN</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="cc321-141"><a href="common-control-versions.md">Version 5,82</a>.</span><span class="sxs-lookup"><span data-stu-id="cc321-141"><a href="common-control-versions.md">Version 5.82</a>.</span></span> <span data-ttu-id="cc321-142"><strong>Destiné à un usage interne ; non recommandé pour une utilisation dans les applications.</strong></span><span class="sxs-lookup"><span data-stu-id="cc321-142"><strong>Intended for internal use; not recommended for use in applications.</strong></span></span> <span data-ttu-id="cc321-143">Ce style donne à la barre d’outils un orientation verticale et organise les boutons de la barre d’outils en colonnes.</span><span class="sxs-lookup"><span data-stu-id="cc321-143">This style gives the toolbar a vertical orientation and organizes the toolbar buttons into columns.</span></span> <span data-ttu-id="cc321-144">Les boutons s’affichent verticalement jusqu’à ce qu’un bouton ait dépassé la hauteur limite de la barre d’outils (voir <a href="tb-setboundingsize.md"><strong>TB_SETBOUNDINGSIZE</strong></a>), puis qu’une nouvelle colonne est créée.</span><span class="sxs-lookup"><span data-stu-id="cc321-144">The buttons flow down vertically until a button has exceeded the bounding height of the toolbar (see <a href="tb-setboundingsize.md"><strong>TB_SETBOUNDINGSIZE</strong></a>), and then a new column is created.</span></span> <span data-ttu-id="cc321-145">La barre d’outils repasse les boutons de cette manière jusqu’à ce que tous les boutons soient positionnés.</span><span class="sxs-lookup"><span data-stu-id="cc321-145">The toolbar flows the buttons in this manner until all buttons are positioned.</span></span> <span data-ttu-id="cc321-146">Pour utiliser ce style, le style de TBSTYLE_EX_VERTICAL doit également être défini.</span><span class="sxs-lookup"><span data-stu-id="cc321-146">To use this style, the TBSTYLE_EX_VERTICAL style must also be set.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="cc321-147">Ce style n’est peut-être pas pris en charge dans les versions ultérieures de Comctl32.dll.</span><span class="sxs-lookup"><span data-stu-id="cc321-147">This style may not be supported in future versions of Comctl32.dll.</span></span> <span data-ttu-id="cc321-148">En outre, ce style n’est pas défini dans commctrl. h.</span><span class="sxs-lookup"><span data-stu-id="cc321-148">Also, this style is not defined in commctrl.h.</span></span> <span data-ttu-id="cc321-149">Ajoutez la définition suivante aux fichiers sources de votre application pour utiliser ce style : <code>#define TBSTYLE_EX_MULTICOLUMN 0x00000002</code>
</span><span class="sxs-lookup"><span data-stu-id="cc321-149">Add the following definition to the source files of your application to use this style: <code>#define TBSTYLE_EX_MULTICOLUMN 0x00000002</code>
</span></span></blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="TBSTYLE_EX_VERTICAL"></span><span id="tbstyle_ex_vertical"></span><dl> <span data-ttu-id="cc321-150"><dt><strong>TBSTYLE_EX_VERTICAL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="cc321-150"><dt><strong>TBSTYLE_EX_VERTICAL</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="cc321-151"><a href="common-control-versions.md">Version 5,82</a>.</span><span class="sxs-lookup"><span data-stu-id="cc321-151"><a href="common-control-versions.md">Version 5.82</a>.</span></span> <span data-ttu-id="cc321-152"><strong>Destiné à un usage interne ; non recommandé pour une utilisation dans les applications.</strong></span><span class="sxs-lookup"><span data-stu-id="cc321-152"><strong>Intended for internal use; not recommended for use in applications.</strong></span></span> <span data-ttu-id="cc321-153">Ce style donne une orientation verticale à la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="cc321-153">This style gives the toolbar a vertical orientation.</span></span> <span data-ttu-id="cc321-154">Les boutons de la barre d’outils se déplacent de haut en bas et non horizontalement.</span><span class="sxs-lookup"><span data-stu-id="cc321-154">Toolbar buttons flow from top to bottom instead of horizontally.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="cc321-155">Ce style n’est peut-être pas pris en charge dans les versions ultérieures de Comctl32.dll.</span><span class="sxs-lookup"><span data-stu-id="cc321-155">This style may not be supported in future versions of Comctl32.dll.</span></span> <span data-ttu-id="cc321-156">En outre, ce style n’est pas défini dans commctrl. h.</span><span class="sxs-lookup"><span data-stu-id="cc321-156">Also, this style is not defined in commctrl.h.</span></span> <span data-ttu-id="cc321-157">Ajoutez la définition suivante aux fichiers sources de votre application pour utiliser ce style : <code>#define TBSTYLE_EX_VERTICAL 0x00000004</code>
</span><span class="sxs-lookup"><span data-stu-id="cc321-157">Add the following definition to the source files of your application to use this style: <code>#define TBSTYLE_EX_VERTICAL 0x00000004</code>
</span></span></blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="cc321-158">Notes</span><span class="sxs-lookup"><span data-stu-id="cc321-158">Remarks</span></span>

<span data-ttu-id="cc321-159">Pour définir un style étendu, envoyez le contrôle de barre d’outils à un message [**\_ SETEXTENDEDSTYLE to**](tb-setextendedstyle.md) .</span><span class="sxs-lookup"><span data-stu-id="cc321-159">To set an extended style, send the toolbar control a [**TB\_SETEXTENDEDSTYLE**](tb-setextendedstyle.md) message.</span></span> <span data-ttu-id="cc321-160">Pour déterminer les styles étendus actuellement définis, envoyez un message [**to \_ GETEXTENDEDSTYLE**](tb-getextendedstyle.md) .</span><span class="sxs-lookup"><span data-stu-id="cc321-160">To determine what extended styles are currently set, send a [**TB\_GETEXTENDEDSTYLE**](tb-getextendedstyle.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc321-161">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cc321-161">Requirements</span></span>



| <span data-ttu-id="cc321-162">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cc321-162">Requirement</span></span> | <span data-ttu-id="cc321-163">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc321-163">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cc321-164">En-tête</span><span class="sxs-lookup"><span data-stu-id="cc321-164">Header</span></span><br/> | <dl> <span data-ttu-id="cc321-165"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc321-165"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





