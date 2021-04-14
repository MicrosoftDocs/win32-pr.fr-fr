---
title: Prise en charge des types de contrôle UI Automation
description: Cette section contient des informations détaillées sur l’arborescence, les propriétés, les modèles de contrôle et les événements que chaque type de contrôle UI Automation de Microsoft doit prendre en charge.
ms.assetid: 35232907-6c54-47cd-b82a-0daee279ef17
keywords:
- UI Automation, à propos des types de contrôle
- UI Automation, vue d’ensemble du type de contrôle
- prise en charge du type de contrôle
- types de contrôles, prise en charge
- types de contrôle, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26ac6f857da87691428c747cfe5dbff5102218f6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382479"
---
# <a name="supporting-ui-automation-control-types"></a><span data-ttu-id="77828-108">Prise en charge des types de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="77828-108">Supporting UI Automation Control Types</span></span>

<span data-ttu-id="77828-109">Cette section contient des informations détaillées sur l’arborescence, les propriétés, les modèles de contrôle et les événements que chaque type de contrôle UI Automation de Microsoft doit prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="77828-109">This section contains detailed information about the tree structure, properties, control patterns, and events that each Microsoft UI Automation control type is required to support.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="77828-110">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="77828-110">In this section</span></span>

-   [<span data-ttu-id="77828-111">Type de contrôle AppBar</span><span class="sxs-lookup"><span data-stu-id="77828-111">AppBar Control Type</span></span>](uiauto-supportappbarcontroltype.md)
-   [<span data-ttu-id="77828-112">Button (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="77828-112">Button Control Type</span></span>](uiauto-supportbuttoncontroltype.md)
-   [<span data-ttu-id="77828-113">Calendar (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="77828-113">Calendar Control Type</span></span>](uiauto-supportcalendarcontroltype.md)
-   [<span data-ttu-id="77828-114">CheckBox (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="77828-114">CheckBox Control Type</span></span>](uiauto-supportcheckboxcontroltype.md)
-   [<span data-ttu-id="77828-115">ComboBox (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="77828-115">ComboBox Control Type</span></span>](uiauto-supportcomboboxcontroltype.md)
-   [<span data-ttu-id="77828-116">DataGrid (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="77828-116">DataGrid Control Type</span></span>](uiauto-supportdatagridcontroltype.md)
-   [<span data-ttu-id="77828-117">DataItem (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="77828-117">DataItem Control Type</span></span>](uiauto-supportdataitemcontroltype.md)
-   [<span data-ttu-id="77828-118">Document (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="77828-118">Document Control Type</span></span>](uiauto-supportdocumentcontroltype.md)
-   [<span data-ttu-id="77828-119">Modifier le type de contrôle</span><span class="sxs-lookup"><span data-stu-id="77828-119">Edit Control Type</span></span>](uiauto-supporteditcontroltype.md)
-   [<span data-ttu-id="77828-120">Group (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="77828-120">Group Control Type</span></span>](uiauto-supportgroupcontroltype.md)
-   [<span data-ttu-id="77828-121">Header (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="77828-121">Header Control Type</span></span>](uiauto-supportheadercontroltype.md)
-   [<span data-ttu-id="77828-122">Type de contrôle HeaderItem</span><span class="sxs-lookup"><span data-stu-id="77828-122">HeaderItem Control Type</span></span>](uiauto-supportheaderitemcontroltype.md)
-   [<span data-ttu-id="77828-123">HYPERLINK (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="77828-123">Hyperlink Control Type</span></span>](uiauto-supporthyperlinkcontroltype.md)
-   [<span data-ttu-id="77828-124">Image (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="77828-124">Image Control Type</span></span>](uiauto-supportimagecontroltype.md)
-   [<span data-ttu-id="77828-125">List (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="77828-125">List Control Type</span></span>](uiauto-supportlistcontroltype.md)
-   [<span data-ttu-id="77828-126">ListItem (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="77828-126">ListItem Control Type</span></span>](uiauto-supportlistitemcontroltype.md)
-   [<span data-ttu-id="77828-127">Menu (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="77828-127">Menu Control Type</span></span>](uiauto-supportmenucontroltype.md)
-   [<span data-ttu-id="77828-128">BarreMenus (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="77828-128">MenuBar Control Type</span></span>](uiauto-supportmenubarcontroltype.md)
-   [<span data-ttu-id="77828-129">MenuItem (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="77828-129">MenuItem Control Type</span></span>](uiauto-supportmenuitemcontroltype.md)
-   [<span data-ttu-id="77828-130">Pane (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="77828-130">Pane Control Type</span></span>](uiauto-supportpanecontroltype.md)
-   [<span data-ttu-id="77828-131">ProgressBar (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="77828-131">ProgressBar Control Type</span></span>](uiauto-supportprogressbarcontroltype.md)
-   [<span data-ttu-id="77828-132">RadioButton (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="77828-132">RadioButton Control Type</span></span>](uiauto-supportradiobuttoncontroltype.md)
-   [<span data-ttu-id="77828-133">ScrollBar (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="77828-133">ScrollBar Control Type</span></span>](uiauto-supportscrollbarcontroltype.md)
-   [<span data-ttu-id="77828-134">Type de contrôle SemanticZoom</span><span class="sxs-lookup"><span data-stu-id="77828-134">SemanticZoom Control Type</span></span>](/windows/desktop/WinAuto/uiauto-supportsemanticzoomcontroltype)
-   [<span data-ttu-id="77828-135">Separator (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="77828-135">Separator Control Type</span></span>](uiauto-supportseparatorcontroltype.md)
-   [<span data-ttu-id="77828-136">Slider (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="77828-136">Slider Control Type</span></span>](uiauto-supportslidercontroltype.md)
-   [<span data-ttu-id="77828-137">Spinner (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="77828-137">Spinner Control Type</span></span>](uiauto-supportspinnercontroltype.md)
-   [<span data-ttu-id="77828-138">SplitButton (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="77828-138">SplitButton Control Type</span></span>](uiauto-supportsplitbuttoncontroltype.md)
-   [<span data-ttu-id="77828-139">StatusBar (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="77828-139">StatusBar Control Type</span></span>](uiauto-supportstatusbarcontroltype.md)
-   [<span data-ttu-id="77828-140">Tab (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="77828-140">Tab Control Type</span></span>](uiauto-supporttabcontroltype.md)
-   [<span data-ttu-id="77828-141">TabItem (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="77828-141">TabItem Control Type</span></span>](uiauto-supporttabitemcontroltype.md)
-   [<span data-ttu-id="77828-142">Table (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="77828-142">Table Control Type</span></span>](uiauto-supporttablecontroltype.md)
-   [<span data-ttu-id="77828-143">Text (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="77828-143">Text Control Type</span></span>](uiauto-supporttextcontroltype.md)
-   [<span data-ttu-id="77828-144">Thumb (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="77828-144">Thumb Control Type</span></span>](uiauto-supportthumbcontroltype.md)
-   [<span data-ttu-id="77828-145">TitleBar (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="77828-145">TitleBar Control Type</span></span>](uiauto-supporttitlebarcontroltype.md)
-   [<span data-ttu-id="77828-146">ToolBar (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="77828-146">ToolBar Control Type</span></span>](uiauto-supporttoolbarcontroltype.md)
-   [<span data-ttu-id="77828-147">ToolTip (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="77828-147">ToolTip Control Type</span></span>](uiauto-supporttooltipcontroltype.md)
-   [<span data-ttu-id="77828-148">Tree (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="77828-148">Tree Control Type</span></span>](uiauto-supporttreecontroltype.md)
-   [<span data-ttu-id="77828-149">TreeItem (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="77828-149">TreeItem Control Type</span></span>](uiauto-supporttreeitemcontroltype.md)
-   [<span data-ttu-id="77828-150">Window (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="77828-150">Window Control Type</span></span>](uiauto-supportwindowcontroltype.md)

## <a name="related-topics"></a><span data-ttu-id="77828-151">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="77828-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77828-152">Guide du programmeur du fournisseur UI Automation</span><span class="sxs-lookup"><span data-stu-id="77828-152">UI Automation Provider Programmer's Guide</span></span>](uiauto-providerportal.md)
</dt> </dl>

 

 