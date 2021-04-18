---
title: Prise en charge d'UI Automation pour les contrôles standard
description: Cette rubrique identifie les contrôles Windows standard pris en charge par Microsoft UI Automation. La prise en charge complète est fournie uniquement pour les contrôles de la version 6 de ComCtrl32.dll (disponible avec Windows XP et versions ultérieures).
ms.assetid: 4821684c-8a90-413c-8ddc-699926e3bb09
keywords:
- clients, prise en charge d’UI Automation pour les contrôles standard
- clients, prise en charge du contrôle standard
- clients, contrôles Win32
- UI Automation, prise en charge des contrôles standard
- UI Automation, prise en charge du contrôle standard
- UI Automation, contrôles Win32
- prise en charge pour les contrôles
- prise en charge du contrôle standard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae6e384b9ee0fd72fd8a41aa3f791a5c996fe6d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507079"
---
# <a name="ui-automation-support-for-standard-controls"></a><span data-ttu-id="58902-112">Prise en charge d'UI Automation pour les contrôles standard</span><span class="sxs-lookup"><span data-stu-id="58902-112">UI Automation Support for Standard Controls</span></span>

<span data-ttu-id="58902-113">Cette rubrique identifie les contrôles Windows standard pris en charge par Microsoft UI Automation.</span><span class="sxs-lookup"><span data-stu-id="58902-113">This topic identifies the standard Windows controls that are supported by Microsoft UI Automation.</span></span> <span data-ttu-id="58902-114">La prise en charge complète est fournie uniquement pour les contrôles de la version 6 de ComCtrl32.dll (disponible avec Windows XP et versions ultérieures).</span><span class="sxs-lookup"><span data-stu-id="58902-114">Full support is provided only for controls from version 6 of ComCtrl32.dll (available with Windows XP and later).</span></span>

> [!Note]  
> <span data-ttu-id="58902-115">Le contrôle RichEdit est pris en charge uniquement pour les versions fournies avec Windows Vista (dans RichEd20.dll version 3,1 et versions ultérieures, et MsftEdit.dll version 4,1 et versions ultérieures).</span><span class="sxs-lookup"><span data-stu-id="58902-115">The RichEdit control is supported only for versions shipped with Windows Vista (in RichEd20.dll version 3.1 and later, and MsftEdit.dll version 4.1 and later).</span></span>

 

<span data-ttu-id="58902-116">Le tableau suivant répertorie les noms de classes des contrôles standard pris en charge, ainsi que les types de contrôle UI Automation correspondants.</span><span class="sxs-lookup"><span data-stu-id="58902-116">The following table lists the class names of the supported standard controls, along with the corresponding UI Automation control types.</span></span>



| <span data-ttu-id="58902-117">Nom de la classe</span><span class="sxs-lookup"><span data-stu-id="58902-117">Class Name</span></span>          | <span data-ttu-id="58902-118">Type de contrôle</span><span class="sxs-lookup"><span data-stu-id="58902-118">Control Type</span></span>        |
|---------------------|---------------------|
| <span data-ttu-id="58902-119">Button</span><span class="sxs-lookup"><span data-stu-id="58902-119">Button</span></span>              | <span data-ttu-id="58902-120">Button</span><span class="sxs-lookup"><span data-stu-id="58902-120">Button</span></span>              |
| <span data-ttu-id="58902-121">Button</span><span class="sxs-lookup"><span data-stu-id="58902-121">Button</span></span>              | <span data-ttu-id="58902-122">RadioButton</span><span class="sxs-lookup"><span data-stu-id="58902-122">RadioButton</span></span>         |
| <span data-ttu-id="58902-123">Bouton</span><span class="sxs-lookup"><span data-stu-id="58902-123">Button</span></span>              | <span data-ttu-id="58902-124">Group</span><span class="sxs-lookup"><span data-stu-id="58902-124">Group</span></span>               |
| <span data-ttu-id="58902-125">Bouton</span><span class="sxs-lookup"><span data-stu-id="58902-125">Button</span></span>              | <span data-ttu-id="58902-126">Case à cocher</span><span class="sxs-lookup"><span data-stu-id="58902-126">CheckBox</span></span>            |
| <span data-ttu-id="58902-127">Bouton</span><span class="sxs-lookup"><span data-stu-id="58902-127">Button</span></span>              | <span data-ttu-id="58902-128">Hyperlink</span><span class="sxs-lookup"><span data-stu-id="58902-128">Hyperlink</span></span>           |
| <span data-ttu-id="58902-129">Bouton</span><span class="sxs-lookup"><span data-stu-id="58902-129">Button</span></span>              | <span data-ttu-id="58902-130">SplitButton</span><span class="sxs-lookup"><span data-stu-id="58902-130">SplitButton</span></span>         |
| <span data-ttu-id="58902-131">Bouton</span><span class="sxs-lookup"><span data-stu-id="58902-131">Button</span></span>              | <span data-ttu-id="58902-132">Case à cocher</span><span class="sxs-lookup"><span data-stu-id="58902-132">CheckBox</span></span>            |
| <span data-ttu-id="58902-133">ComboBoxEx32</span><span class="sxs-lookup"><span data-stu-id="58902-133">ComboBoxEx32</span></span>        | <span data-ttu-id="58902-134">Liste déroulante</span><span class="sxs-lookup"><span data-stu-id="58902-134">ComboBox</span></span>            |
| <span data-ttu-id="58902-135">Liste déroulante</span><span class="sxs-lookup"><span data-stu-id="58902-135">ComboBox</span></span>            | <span data-ttu-id="58902-136">Liste déroulante</span><span class="sxs-lookup"><span data-stu-id="58902-136">ComboBox</span></span>            |
| <span data-ttu-id="58902-137">Modifier</span><span class="sxs-lookup"><span data-stu-id="58902-137">Edit</span></span>                | <span data-ttu-id="58902-138">Document</span><span class="sxs-lookup"><span data-stu-id="58902-138">Document</span></span>            |
| <span data-ttu-id="58902-139">Modifier</span><span class="sxs-lookup"><span data-stu-id="58902-139">Edit</span></span>                | <span data-ttu-id="58902-140">Modifier</span><span class="sxs-lookup"><span data-stu-id="58902-140">Edit</span></span>                |
| <span data-ttu-id="58902-141">SysLink</span><span class="sxs-lookup"><span data-stu-id="58902-141">SysLink</span></span>             | <span data-ttu-id="58902-142">Hyperlink</span><span class="sxs-lookup"><span data-stu-id="58902-142">Hyperlink</span></span>           |
| <span data-ttu-id="58902-143">statique</span><span class="sxs-lookup"><span data-stu-id="58902-143">Static</span></span>              | <span data-ttu-id="58902-144">Texte</span><span class="sxs-lookup"><span data-stu-id="58902-144">Text</span></span>                |
| <span data-ttu-id="58902-145">statique</span><span class="sxs-lookup"><span data-stu-id="58902-145">Static</span></span>              | <span data-ttu-id="58902-146">Image</span><span class="sxs-lookup"><span data-stu-id="58902-146">Image</span></span>               |
| <span data-ttu-id="58902-147">SysIPAddress32</span><span class="sxs-lookup"><span data-stu-id="58902-147">SysIPAddress32</span></span>      | <span data-ttu-id="58902-148">Custom</span><span class="sxs-lookup"><span data-stu-id="58902-148">Custom</span></span>              |
| <span data-ttu-id="58902-149">SysHeader32</span><span class="sxs-lookup"><span data-stu-id="58902-149">SysHeader32</span></span>         | <span data-ttu-id="58902-150">Header/HeaderItem</span><span class="sxs-lookup"><span data-stu-id="58902-150">Header/HeaderItem</span></span>   |
| <span data-ttu-id="58902-151">SysListView32</span><span class="sxs-lookup"><span data-stu-id="58902-151">SysListView32</span></span>       | <span data-ttu-id="58902-152">DataGrid</span><span class="sxs-lookup"><span data-stu-id="58902-152">DataGrid</span></span>            |
| <span data-ttu-id="58902-153">SysListView32</span><span class="sxs-lookup"><span data-stu-id="58902-153">SysListView32</span></span>       | <span data-ttu-id="58902-154">List</span><span class="sxs-lookup"><span data-stu-id="58902-154">List</span></span>                |
| <span data-ttu-id="58902-155">ListBox</span><span class="sxs-lookup"><span data-stu-id="58902-155">ListBox</span></span>             | <span data-ttu-id="58902-156">List</span><span class="sxs-lookup"><span data-stu-id="58902-156">List</span></span>                |
| <span data-ttu-id="58902-157">ListBox</span><span class="sxs-lookup"><span data-stu-id="58902-157">ListBox</span></span>             | <span data-ttu-id="58902-158">ListItem</span><span class="sxs-lookup"><span data-stu-id="58902-158">ListItem</span></span>            |
| <span data-ttu-id="58902-159">\#32768</span><span class="sxs-lookup"><span data-stu-id="58902-159">\#32768</span></span>             | <span data-ttu-id="58902-160">Menu</span><span class="sxs-lookup"><span data-stu-id="58902-160">Menu</span></span>                |
| <span data-ttu-id="58902-161">\#32768</span><span class="sxs-lookup"><span data-stu-id="58902-161">\#32768</span></span>             | <span data-ttu-id="58902-162">MenuItem</span><span class="sxs-lookup"><span data-stu-id="58902-162">MenuItem</span></span>            |
| <span data-ttu-id="58902-163">msctls \_ progress32</span><span class="sxs-lookup"><span data-stu-id="58902-163">msctls\_progress32</span></span>  | <span data-ttu-id="58902-164">Barre de progression</span><span class="sxs-lookup"><span data-stu-id="58902-164">ProgressBar</span></span>         |
| <span data-ttu-id="58902-165">RichEdit</span><span class="sxs-lookup"><span data-stu-id="58902-165">RichEdit</span></span>            | <span data-ttu-id="58902-166">Document.</span><span class="sxs-lookup"><span data-stu-id="58902-166">Document.</span></span> <span data-ttu-id="58902-167">Consultez la remarque.</span><span class="sxs-lookup"><span data-stu-id="58902-167">See note.</span></span> |
| <span data-ttu-id="58902-168">RichEdit20A</span><span class="sxs-lookup"><span data-stu-id="58902-168">RichEdit20A</span></span>         | <span data-ttu-id="58902-169">Document</span><span class="sxs-lookup"><span data-stu-id="58902-169">Document</span></span>            |
| <span data-ttu-id="58902-170">RichEdit20W</span><span class="sxs-lookup"><span data-stu-id="58902-170">RichEdit20W</span></span>         | <span data-ttu-id="58902-171">Document</span><span class="sxs-lookup"><span data-stu-id="58902-171">Document</span></span>            |
| <span data-ttu-id="58902-172">RichEdit50W</span><span class="sxs-lookup"><span data-stu-id="58902-172">RichEdit50W</span></span>         | <span data-ttu-id="58902-173">Document</span><span class="sxs-lookup"><span data-stu-id="58902-173">Document</span></span>            |
| <span data-ttu-id="58902-174">ScrollBar</span><span class="sxs-lookup"><span data-stu-id="58902-174">ScrollBar</span></span>           | <span data-ttu-id="58902-175">Curseur</span><span class="sxs-lookup"><span data-stu-id="58902-175">Slider</span></span>              |
| <span data-ttu-id="58902-176">msctls \_ trackbar32</span><span class="sxs-lookup"><span data-stu-id="58902-176">msctls\_trackbar32</span></span>  | <span data-ttu-id="58902-177">Curseur</span><span class="sxs-lookup"><span data-stu-id="58902-177">Slider</span></span>              |
| <span data-ttu-id="58902-178">msctls \_ updown32</span><span class="sxs-lookup"><span data-stu-id="58902-178">msctls\_updown32</span></span>    | <span data-ttu-id="58902-179">Spinner</span><span class="sxs-lookup"><span data-stu-id="58902-179">Spinner</span></span>             |
| <span data-ttu-id="58902-180">msctls \_ statusbar32</span><span class="sxs-lookup"><span data-stu-id="58902-180">msctls\_statusbar32</span></span> | <span data-ttu-id="58902-181">StatusBar</span><span class="sxs-lookup"><span data-stu-id="58902-181">StatusBar</span></span>           |
| <span data-ttu-id="58902-182">SysTabControl32</span><span class="sxs-lookup"><span data-stu-id="58902-182">SysTabControl32</span></span>     | <span data-ttu-id="58902-183">Onglet</span><span class="sxs-lookup"><span data-stu-id="58902-183">Tab</span></span>                 |
| <span data-ttu-id="58902-184">SysTabControl32</span><span class="sxs-lookup"><span data-stu-id="58902-184">SysTabControl32</span></span>     | <span data-ttu-id="58902-185">TabItem</span><span class="sxs-lookup"><span data-stu-id="58902-185">TabItem</span></span>             |
| <span data-ttu-id="58902-186">ToolbarWindow32</span><span class="sxs-lookup"><span data-stu-id="58902-186">ToolbarWindow32</span></span>     | <span data-ttu-id="58902-187">ToolBar</span><span class="sxs-lookup"><span data-stu-id="58902-187">ToolBar</span></span>             |
| <span data-ttu-id="58902-188">ToolbarWindow32</span><span class="sxs-lookup"><span data-stu-id="58902-188">ToolbarWindow32</span></span>     | <span data-ttu-id="58902-189">MenuItem</span><span class="sxs-lookup"><span data-stu-id="58902-189">MenuItem</span></span>            |
| <span data-ttu-id="58902-190">ToolbarWindow32</span><span class="sxs-lookup"><span data-stu-id="58902-190">ToolbarWindow32</span></span>     | <span data-ttu-id="58902-191">Bouton</span><span class="sxs-lookup"><span data-stu-id="58902-191">Button</span></span>              |
| <span data-ttu-id="58902-192">ToolbarWindow32</span><span class="sxs-lookup"><span data-stu-id="58902-192">ToolbarWindow32</span></span>     | <span data-ttu-id="58902-193">Case à cocher</span><span class="sxs-lookup"><span data-stu-id="58902-193">CheckBox</span></span>            |
| <span data-ttu-id="58902-194">ToolbarWindow32</span><span class="sxs-lookup"><span data-stu-id="58902-194">ToolbarWindow32</span></span>     | <span data-ttu-id="58902-195">RadioButton</span><span class="sxs-lookup"><span data-stu-id="58902-195">RadioButton</span></span>         |
| <span data-ttu-id="58902-196">ToolbarWindow32</span><span class="sxs-lookup"><span data-stu-id="58902-196">ToolbarWindow32</span></span>     | <span data-ttu-id="58902-197">Séparateur</span><span class="sxs-lookup"><span data-stu-id="58902-197">Separator</span></span>           |
| <span data-ttu-id="58902-198">info-bulles \_ Class32</span><span class="sxs-lookup"><span data-stu-id="58902-198">tooltips\_class32</span></span>   | <span data-ttu-id="58902-199">Info-bulle</span><span class="sxs-lookup"><span data-stu-id="58902-199">ToolTip</span></span>             |
| <span data-ttu-id="58902-200">\#32774</span><span class="sxs-lookup"><span data-stu-id="58902-200">\#32774</span></span>             | <span data-ttu-id="58902-201">Info-bulle</span><span class="sxs-lookup"><span data-stu-id="58902-201">ToolTip</span></span>             |
| <span data-ttu-id="58902-202">ReBarWindow32</span><span class="sxs-lookup"><span data-stu-id="58902-202">ReBarWindow32</span></span>       | <span data-ttu-id="58902-203">Barre d’outils</span><span class="sxs-lookup"><span data-stu-id="58902-203">Toolbar</span></span>             |
| <span data-ttu-id="58902-204">SysTreeView32</span><span class="sxs-lookup"><span data-stu-id="58902-204">SysTreeView32</span></span>       | <span data-ttu-id="58902-205">Arborescence</span><span class="sxs-lookup"><span data-stu-id="58902-205">Tree</span></span>                |
| <span data-ttu-id="58902-206">SysTreeView32</span><span class="sxs-lookup"><span data-stu-id="58902-206">SysTreeView32</span></span>       | <span data-ttu-id="58902-207">TreeItem</span><span class="sxs-lookup"><span data-stu-id="58902-207">TreeItem</span></span>            |



 

<span data-ttu-id="58902-208">Les contrôles répertoriés dans le tableau suivant ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="58902-208">The controls listed in the following table are not supported.</span></span>



| <span data-ttu-id="58902-209">Nom de la classe</span><span class="sxs-lookup"><span data-stu-id="58902-209">Class Name</span></span>                                    | <span data-ttu-id="58902-210">Type de contrôle</span><span class="sxs-lookup"><span data-stu-id="58902-210">Control Type</span></span> |
|-----------------------------------------------|--------------|
| <span data-ttu-id="58902-211">SysAnimate32</span><span class="sxs-lookup"><span data-stu-id="58902-211">SysAnimate32</span></span>                                  | <span data-ttu-id="58902-212">Image</span><span class="sxs-lookup"><span data-stu-id="58902-212">Image</span></span>        |
| <span data-ttu-id="58902-213">SysPager</span><span class="sxs-lookup"><span data-stu-id="58902-213">SysPager</span></span>                                      | <span data-ttu-id="58902-214">Spinner</span><span class="sxs-lookup"><span data-stu-id="58902-214">Spinner</span></span>      |
| <span data-ttu-id="58902-215">SysDateTimePick32</span><span class="sxs-lookup"><span data-stu-id="58902-215">SysDateTimePick32</span></span>                             | <span data-ttu-id="58902-216">Custom</span><span class="sxs-lookup"><span data-stu-id="58902-216">Custom</span></span>       |
| <span data-ttu-id="58902-217">SysMonthCal32</span><span class="sxs-lookup"><span data-stu-id="58902-217">SysMonthCal32</span></span>                                 | <span data-ttu-id="58902-218">Calendrier</span><span class="sxs-lookup"><span data-stu-id="58902-218">Calendar</span></span>     |
| <span data-ttu-id="58902-219">MS \_ WINNOTE</span><span class="sxs-lookup"><span data-stu-id="58902-219">MS\_WINNOTE</span></span>                                   | <span data-ttu-id="58902-220">Info-bulle</span><span class="sxs-lookup"><span data-stu-id="58902-220">Tooltip</span></span>      |
| <span data-ttu-id="58902-221">VBBubble</span><span class="sxs-lookup"><span data-stu-id="58902-221">VBBubble</span></span>                                      | <span data-ttu-id="58902-222">Info-bulle</span><span class="sxs-lookup"><span data-stu-id="58902-222">Tooltip</span></span>      |
| <span data-ttu-id="58902-223">ScrollBar (quand il est utilisé comme contrôle autonome)</span><span class="sxs-lookup"><span data-stu-id="58902-223">ScrollBar (when used as a standalone control)</span></span> | <span data-ttu-id="58902-224">Curseur</span><span class="sxs-lookup"><span data-stu-id="58902-224">Slider</span></span>       |
| <span data-ttu-id="58902-225">SuperGrid</span><span class="sxs-lookup"><span data-stu-id="58902-225">SuperGrid</span></span>                                     | <span data-ttu-id="58902-226">Custom</span><span class="sxs-lookup"><span data-stu-id="58902-226">Custom</span></span>       |



 

## <a name="related-topics"></a><span data-ttu-id="58902-227">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="58902-227">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58902-228">Vue d'ensemble des types de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="58902-228">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> </dl>

 

 




