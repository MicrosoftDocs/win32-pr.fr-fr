---
title: GUID déconseillés
description: Cette rubrique décrit les GUID utilisés avec la fonction UiaLookupId.
ms.assetid: b8e9e33c-9781-4f50-bbb7-a9950409f2e6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c5203f63fa3f05e1d25e5623815101cd48ada34
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839377"
---
# <a name="deprecated-guids"></a><span data-ttu-id="bf778-103">GUID déconseillés</span><span class="sxs-lookup"><span data-stu-id="bf778-103">Deprecated GUIDs</span></span>

<span data-ttu-id="bf778-104">Cette rubrique décrit les GUID utilisés avec la fonction [**UiaLookupId**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uialookupid) .</span><span class="sxs-lookup"><span data-stu-id="bf778-104">This topic describes the GUIDs that are used with the [**UiaLookupId**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uialookupid) function.</span></span>

> [!Note]  
> <span data-ttu-id="bf778-105">La fonction [**UiaLookupId**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uialookupid) et les GUID décrits dans cette rubrique sont déconseillés.</span><span class="sxs-lookup"><span data-stu-id="bf778-105">The [**UiaLookupId**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uialookupid) function and the GUIDs described in this topic are deprecated.</span></span> <span data-ttu-id="bf778-106">Au lieu de cela, les applications doivent utiliser les identificateurs décrits dans les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="bf778-106">Instead, applications should use the identifiers described in the following sections:</span></span>

 

-   [<span data-ttu-id="bf778-107">Identificateurs de modèle de contrôle</span><span class="sxs-lookup"><span data-stu-id="bf778-107">Control Pattern Identifiers</span></span>](uiauto-controlpattern-ids.md)
-   [<span data-ttu-id="bf778-108">Identificateurs de type de contrôle</span><span class="sxs-lookup"><span data-stu-id="bf778-108">Control Type Identifiers</span></span>](uiauto-controltype-ids.md)
-   [<span data-ttu-id="bf778-109">Identificateurs d’événements</span><span class="sxs-lookup"><span data-stu-id="bf778-109">Event Identifiers</span></span>](uiauto-event-ids.md)
-   [<span data-ttu-id="bf778-110">Identificateurs de propriété</span><span class="sxs-lookup"><span data-stu-id="bf778-110">Property Identifiers</span></span>](uiauto-entry-propids.md)
-   [<span data-ttu-id="bf778-111">Identificateurs d’attribut de texte</span><span class="sxs-lookup"><span data-stu-id="bf778-111">Text Attribute Identifiers</span></span>](uiauto-textattribute-ids.md)

<span data-ttu-id="bf778-112">Cette section répertorie les GUID suivants :</span><span class="sxs-lookup"><span data-stu-id="bf778-112">This section lists the following GUIDs:</span></span>

-   [<span data-ttu-id="bf778-113">GUID PATTERNID</span><span class="sxs-lookup"><span data-stu-id="bf778-113">PATTERNID GUIDs</span></span>](#patternid-guids)
-   [<span data-ttu-id="bf778-114">GUID CONTROLTYPEID</span><span class="sxs-lookup"><span data-stu-id="bf778-114">CONTROLTYPEID GUIDs</span></span>](#controltypeid-guids)
-   [<span data-ttu-id="bf778-115">GUID d’ID d’événement</span><span class="sxs-lookup"><span data-stu-id="bf778-115">EVENTID GUIDs</span></span>](#eventid-guids)
-   [<span data-ttu-id="bf778-116">GUID de PROPERTYID</span><span class="sxs-lookup"><span data-stu-id="bf778-116">PROPERTYID GUIDs</span></span>](#propertyid-guids)
-   [<span data-ttu-id="bf778-117">GUID TEXTATTRIBUTEID</span><span class="sxs-lookup"><span data-stu-id="bf778-117">TEXTATTRIBUTEID GUIDs</span></span>](#textattributeid-guids)

## <a name="patternid-guids"></a><span data-ttu-id="bf778-118">GUID PATTERNID</span><span class="sxs-lookup"><span data-stu-id="bf778-118">PATTERNID GUIDs</span></span>

<span data-ttu-id="bf778-119">Les GUID PATTERNID qui représentent des modèles de contrôle dans la fonction [**UiaLookupId**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uialookupid) sont répertoriés dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="bf778-119">The PATTERNID GUIDs that represent control patterns in the [**UiaLookupId**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uialookupid) function are listed in the following table.</span></span>



| <span data-ttu-id="bf778-120">GUID PATTERNID</span><span class="sxs-lookup"><span data-stu-id="bf778-120">PATTERNID GUIDs</span></span>                  |
|----------------------------------|
| <span data-ttu-id="bf778-121">\_GUID du modèle d’annotation \_</span><span class="sxs-lookup"><span data-stu-id="bf778-121">Annotation\_Pattern\_GUID</span></span>        |
| <span data-ttu-id="bf778-122">\_GUID du modèle d’ancrage \_</span><span class="sxs-lookup"><span data-stu-id="bf778-122">Dock\_Pattern\_GUID</span></span>              |
| <span data-ttu-id="bf778-123">Faire glisser le \_ modèle \_ GUID</span><span class="sxs-lookup"><span data-stu-id="bf778-123">Drag\_Pattern\_GUID</span></span>              |
| <span data-ttu-id="bf778-124">\_GUID du modèle dropTarget \_</span><span class="sxs-lookup"><span data-stu-id="bf778-124">DropTarget\_Pattern\_GUID</span></span>        |
| <span data-ttu-id="bf778-125">\_GUID du modèle ExpandCollpase \_</span><span class="sxs-lookup"><span data-stu-id="bf778-125">ExpandCollpase\_Pattern\_GUID</span></span>    |
| <span data-ttu-id="bf778-126">\_GUID du modèle de grille \_</span><span class="sxs-lookup"><span data-stu-id="bf778-126">Grid\_Pattern\_GUID</span></span>              |
| <span data-ttu-id="bf778-127">\_GUID du modèle GridItem \_</span><span class="sxs-lookup"><span data-stu-id="bf778-127">GridItem\_Pattern\_GUID</span></span>          |
| <span data-ttu-id="bf778-128">Appeler \_ le \_ GUID du modèle</span><span class="sxs-lookup"><span data-stu-id="bf778-128">Invoke\_Pattern\_GUID</span></span>            |
| <span data-ttu-id="bf778-129">\_GUID du modèle ItemContainer \_</span><span class="sxs-lookup"><span data-stu-id="bf778-129">ItemContainer\_Pattern\_GUID</span></span>     |
| <span data-ttu-id="bf778-130">\_GUID du modèle LegacyIAccessible \_</span><span class="sxs-lookup"><span data-stu-id="bf778-130">LegacyIAccessible\_Pattern\_GUID</span></span> |
| <span data-ttu-id="bf778-131">\_GUID du modèle ObjectModel \_</span><span class="sxs-lookup"><span data-stu-id="bf778-131">ObjectModel\_Pattern\_GUID</span></span>       |
| <span data-ttu-id="bf778-132">\_GUID du modèle RangeValue \_</span><span class="sxs-lookup"><span data-stu-id="bf778-132">RangeValue\_Pattern\_GUID</span></span>        |
| <span data-ttu-id="bf778-133">\_GUID du modèle Scroll \_</span><span class="sxs-lookup"><span data-stu-id="bf778-133">Scroll\_Pattern\_GUID</span></span>            |
| <span data-ttu-id="bf778-134">\_GUID du modèle ScrollItem \_</span><span class="sxs-lookup"><span data-stu-id="bf778-134">ScrollItem\_Pattern\_GUID</span></span>        |
| <span data-ttu-id="bf778-135">Modèle de sélection \_</span><span class="sxs-lookup"><span data-stu-id="bf778-135">Selection\_Pattern</span></span>               |
| <span data-ttu-id="bf778-136">\_GUID du modèle SelectionItem \_</span><span class="sxs-lookup"><span data-stu-id="bf778-136">SelectionItem\_Pattern\_GUID</span></span>     |
| <span data-ttu-id="bf778-137">\_GUID du modèle de feuille de calcul \_</span><span class="sxs-lookup"><span data-stu-id="bf778-137">Spreadsheet\_Pattern\_GUID</span></span>       |
| <span data-ttu-id="bf778-138">\_GUID du modèle SpreadsheetItem \_</span><span class="sxs-lookup"><span data-stu-id="bf778-138">SpreadsheetItem\_Pattern\_GUID</span></span>   |
| <span data-ttu-id="bf778-139">\_GUID du modèle SynchronizedInput \_</span><span class="sxs-lookup"><span data-stu-id="bf778-139">SynchronizedInput\_Pattern\_GUID</span></span> |
| <span data-ttu-id="bf778-140">\_GUID du modèle de styles \_</span><span class="sxs-lookup"><span data-stu-id="bf778-140">Styles\_Pattern\_GUID</span></span>            |
| <span data-ttu-id="bf778-141">\_GUID de modèle de table \_</span><span class="sxs-lookup"><span data-stu-id="bf778-141">Table\_Pattern\_GUID</span></span>             |
| <span data-ttu-id="bf778-142">\_GUID du modèle TableItem \_</span><span class="sxs-lookup"><span data-stu-id="bf778-142">TableItem\_Pattern\_GUID</span></span>         |
| <span data-ttu-id="bf778-143">\_GUID du modèle TextChild \_</span><span class="sxs-lookup"><span data-stu-id="bf778-143">TextChild\_Pattern\_GUID</span></span>         |
| <span data-ttu-id="bf778-144">\_GUID du modèle de texte \_</span><span class="sxs-lookup"><span data-stu-id="bf778-144">Text\_Pattern\_GUID</span></span>              |
| <span data-ttu-id="bf778-145">\_GUID de Pattern2 de texte \_</span><span class="sxs-lookup"><span data-stu-id="bf778-145">Text\_Pattern2\_GUID</span></span>             |
| <span data-ttu-id="bf778-146">Activer/désactiver le \_ GUID du modèle \_</span><span class="sxs-lookup"><span data-stu-id="bf778-146">Toggle\_Pattern\_GUID</span></span>            |
| <span data-ttu-id="bf778-147">Modèle de transformation \_</span><span class="sxs-lookup"><span data-stu-id="bf778-147">Transform\_Pattern</span></span>               |
| <span data-ttu-id="bf778-148">GUID de transformation \_ Pattern2 \_</span><span class="sxs-lookup"><span data-stu-id="bf778-148">Transform\_Pattern2\_GUID</span></span>        |
| <span data-ttu-id="bf778-149">\_GUID du modèle de valeur \_</span><span class="sxs-lookup"><span data-stu-id="bf778-149">Value\_Pattern\_GUID</span></span>             |
| <span data-ttu-id="bf778-150">\_GUID du modèle VirtualizedItem \_</span><span class="sxs-lookup"><span data-stu-id="bf778-150">VirtualizedItem\_Pattern\_GUID</span></span>   |
| <span data-ttu-id="bf778-151">\_GUID du modèle de fenêtre \_</span><span class="sxs-lookup"><span data-stu-id="bf778-151">Window\_Pattern\_GUID</span></span>            |



 

## <a name="controltypeid-guids"></a><span data-ttu-id="bf778-152">GUID CONTROLTYPEID</span><span class="sxs-lookup"><span data-stu-id="bf778-152">CONTROLTYPEID GUIDs</span></span>

<span data-ttu-id="bf778-153">Les GUID CONTROLTYPEID qui représentent les types de contrôle dans la fonction [**UiaLookupId**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uialookupid) sont répertoriés dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="bf778-153">The CONTROLTYPEID GUIDs that represent control types in the [**UiaLookupId**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uialookupid) function are listed in the following table.</span></span>



| <span data-ttu-id="bf778-154">GUID CONTROLTYPEID</span><span class="sxs-lookup"><span data-stu-id="bf778-154">CONTROLTYPEID GUIDs</span></span>        |
|----------------------------|
| <span data-ttu-id="bf778-155">\_GUID de contrôle Button \_</span><span class="sxs-lookup"><span data-stu-id="bf778-155">Button\_Control\_GUID</span></span>      |
| <span data-ttu-id="bf778-156">\_GUID du contrôle Calendar \_</span><span class="sxs-lookup"><span data-stu-id="bf778-156">Calendar\_Control\_GUID</span></span>    |
| <span data-ttu-id="bf778-157">\_GUID du contrôle CheckBox \_</span><span class="sxs-lookup"><span data-stu-id="bf778-157">CheckBox\_Control\_GUID</span></span>    |
| <span data-ttu-id="bf778-158">\_GUID du contrôle ComboBox \_</span><span class="sxs-lookup"><span data-stu-id="bf778-158">ComboBox\_Control\_GUID</span></span>    |
| <span data-ttu-id="bf778-159">\_GUID de contrôle personnalisé \_</span><span class="sxs-lookup"><span data-stu-id="bf778-159">Custom\_Control\_GUID</span></span>      |
| <span data-ttu-id="bf778-160">\_GUID du contrôle DataGrid \_</span><span class="sxs-lookup"><span data-stu-id="bf778-160">DataGrid\_Control\_GUID</span></span>    |
| <span data-ttu-id="bf778-161">\_GUID de contrôle DataItem \_</span><span class="sxs-lookup"><span data-stu-id="bf778-161">DataItem\_Control\_GUID</span></span>    |
| <span data-ttu-id="bf778-162">\_GUID de contrôle de document \_</span><span class="sxs-lookup"><span data-stu-id="bf778-162">Document\_Control\_GUID</span></span>    |
| <span data-ttu-id="bf778-163">Modifier \_ le \_ GUID du contrôle</span><span class="sxs-lookup"><span data-stu-id="bf778-163">Edit\_Control\_GUID</span></span>        |
| <span data-ttu-id="bf778-164">\_GUID de contrôle de groupe \_</span><span class="sxs-lookup"><span data-stu-id="bf778-164">Group\_Control\_GUID</span></span>       |
| <span data-ttu-id="bf778-165">\_GUID de contrôle d’en-tête \_</span><span class="sxs-lookup"><span data-stu-id="bf778-165">Header\_Control\_GUID</span></span>      |
| <span data-ttu-id="bf778-166">\_GUID du contrôle HeaderItem \_</span><span class="sxs-lookup"><span data-stu-id="bf778-166">HeaderItem\_Control\_GUID</span></span>  |
| <span data-ttu-id="bf778-167">\_GUID du contrôle HyperLink \_</span><span class="sxs-lookup"><span data-stu-id="bf778-167">Hyperlink\_Control\_GUID</span></span>   |
| <span data-ttu-id="bf778-168">\_GUID de contrôle d’image \_</span><span class="sxs-lookup"><span data-stu-id="bf778-168">Image\_Control\_GUID</span></span>       |
| <span data-ttu-id="bf778-169">\_GUID du contrôle de liste \_</span><span class="sxs-lookup"><span data-stu-id="bf778-169">List\_Control\_GUID</span></span>        |
| <span data-ttu-id="bf778-170">\_GUID du contrôle ListItem \_</span><span class="sxs-lookup"><span data-stu-id="bf778-170">ListItem\_Control\_GUID</span></span>    |
| <span data-ttu-id="bf778-171">\_GUID de contrôle de menu \_</span><span class="sxs-lookup"><span data-stu-id="bf778-171">Menu\_Control\_GUID</span></span>        |
| <span data-ttu-id="bf778-172">\_GUID du contrôle MenuBar \_</span><span class="sxs-lookup"><span data-stu-id="bf778-172">MenuBar\_Control\_GUID</span></span>     |
| <span data-ttu-id="bf778-173">\_GUID du contrôle MenuItem \_</span><span class="sxs-lookup"><span data-stu-id="bf778-173">MenuItem\_Control\_GUID</span></span>    |
| <span data-ttu-id="bf778-174">\_GUID du contrôle de volet \_</span><span class="sxs-lookup"><span data-stu-id="bf778-174">Pane\_Control\_GUID</span></span>        |
| <span data-ttu-id="bf778-175">\_GUID du contrôle ProgressBar \_</span><span class="sxs-lookup"><span data-stu-id="bf778-175">ProgressBar\_Control\_GUID</span></span> |
| <span data-ttu-id="bf778-176">\_GUID de contrôle RadioButton \_</span><span class="sxs-lookup"><span data-stu-id="bf778-176">RadioButton\_Control\_GUID</span></span> |
| <span data-ttu-id="bf778-177">\_GUID du contrôle ScrollBar \_</span><span class="sxs-lookup"><span data-stu-id="bf778-177">ScrollBar\_Control\_GUID</span></span>   |
| <span data-ttu-id="bf778-178">\_GUID du contrôle Separator \_</span><span class="sxs-lookup"><span data-stu-id="bf778-178">Separator\_Control\_GUID</span></span>   |
| <span data-ttu-id="bf778-179">GUID du \_ contrôle \_ Slider</span><span class="sxs-lookup"><span data-stu-id="bf778-179">Slider\_Control\_GUID</span></span>      |
| <span data-ttu-id="bf778-180">\_GUID de contrôle Spinner \_</span><span class="sxs-lookup"><span data-stu-id="bf778-180">Spinner\_Control\_GUID</span></span>     |
| <span data-ttu-id="bf778-181">\_GUID du contrôle SplitButton \_</span><span class="sxs-lookup"><span data-stu-id="bf778-181">SplitButton\_Control\_GUID</span></span> |
| <span data-ttu-id="bf778-182">\_GUID du contrôle StatusBar \_</span><span class="sxs-lookup"><span data-stu-id="bf778-182">StatusBar\_Control\_GUID</span></span>   |
| <span data-ttu-id="bf778-183">\_GUID du contrôle Tab \_</span><span class="sxs-lookup"><span data-stu-id="bf778-183">Tab\_Control\_GUID</span></span>         |
| <span data-ttu-id="bf778-184">\_GUID de contrôle TabItem \_</span><span class="sxs-lookup"><span data-stu-id="bf778-184">TabItem\_Control\_GUID</span></span>     |
| <span data-ttu-id="bf778-185">\_GUID de contrôle de table \_</span><span class="sxs-lookup"><span data-stu-id="bf778-185">Table\_Control\_GUID</span></span>       |
| <span data-ttu-id="bf778-186">\_GUID de contrôle de texte \_</span><span class="sxs-lookup"><span data-stu-id="bf778-186">Text\_Control\_GUID</span></span>        |
| <span data-ttu-id="bf778-187">\_GUID de contrôle Thumb \_</span><span class="sxs-lookup"><span data-stu-id="bf778-187">Thumb\_Control\_GUID</span></span>       |
| <span data-ttu-id="bf778-188">\_GUID du contrôle TitleBar \_</span><span class="sxs-lookup"><span data-stu-id="bf778-188">TitleBar\_Control\_GUID</span></span>    |
| <span data-ttu-id="bf778-189">\_GUID du contrôle ToolBar \_</span><span class="sxs-lookup"><span data-stu-id="bf778-189">ToolBar\_Control\_GUID</span></span>     |
| <span data-ttu-id="bf778-190">\_GUID du contrôle ToolTip \_</span><span class="sxs-lookup"><span data-stu-id="bf778-190">ToolTip\_Control\_GUID</span></span>     |
| <span data-ttu-id="bf778-191">\_GUID de contrôle d’arborescence \_</span><span class="sxs-lookup"><span data-stu-id="bf778-191">Tree\_Control\_GUID</span></span>        |
| <span data-ttu-id="bf778-192">\_GUID de contrôle TreeItem \_</span><span class="sxs-lookup"><span data-stu-id="bf778-192">TreeItem\_Control\_GUID</span></span>    |
| <span data-ttu-id="bf778-193">\_GUID du contrôle de fenêtre \_</span><span class="sxs-lookup"><span data-stu-id="bf778-193">Window\_Control\_GUID</span></span>      |



 

## <a name="eventid-guids"></a><span data-ttu-id="bf778-194">GUID d’ID d’événement</span><span class="sxs-lookup"><span data-stu-id="bf778-194">EVENTID GUIDs</span></span>

<span data-ttu-id="bf778-195">Les GUID EVENTID qui représentent des événements Microsoft UI Automation dans la fonction [**UiaLookupId**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uialookupid) sont répertoriés dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="bf778-195">The EVENTID GUIDs that represent Microsoft UI Automation events in the [**UiaLookupId**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uialookupid) function are listed in the following table.</span></span>



| <span data-ttu-id="bf778-196">GUID d’ID d’événement</span><span class="sxs-lookup"><span data-stu-id="bf778-196">EVENTID GUIDs</span></span>                                                |
|--------------------------------------------------------------|
| <span data-ttu-id="bf778-197">GUID de l' \_ événement AsyncContentLoaded \_</span><span class="sxs-lookup"><span data-stu-id="bf778-197">AsyncContentLoaded\_Event\_GUID</span></span>                              |
| <span data-ttu-id="bf778-198">GUID de l' \_ événement AutomationFocusChanged \_</span><span class="sxs-lookup"><span data-stu-id="bf778-198">AutomationFocusChanged\_Event\_GUID</span></span>                          |
| <span data-ttu-id="bf778-199">GUID de l' \_ événement AutomationPropertyChanged \_</span><span class="sxs-lookup"><span data-stu-id="bf778-199">AutomationPropertyChanged\_Event\_GUID</span></span>                       |
| <span data-ttu-id="bf778-200">Faire glisser le \_ \_ GUID d’événement DragCancel \_</span><span class="sxs-lookup"><span data-stu-id="bf778-200">Drag\_DragCancel\_Event\_GUID</span></span>                                |
| <span data-ttu-id="bf778-201">Faire glisser le \_ \_ GUID d’événement DragComplete \_</span><span class="sxs-lookup"><span data-stu-id="bf778-201">Drag\_DragComplete\_Event\_GUID</span></span>                              |
| <span data-ttu-id="bf778-202">Faire glisser le \_ \_ GUID d’événement DragStart \_</span><span class="sxs-lookup"><span data-stu-id="bf778-202">Drag\_DragStart\_Event\_GUID</span></span>                                 |
| <span data-ttu-id="bf778-203">\_GUID d' \_ événement dropTarget DragEnter \_</span><span class="sxs-lookup"><span data-stu-id="bf778-203">DropTarget\_DragEnter\_Event\_GUID</span></span>                           |
| <span data-ttu-id="bf778-204">GUID de l' \_ événement dropTarget DragLeave \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-204">DropTarget\_DragLeave\_Event\_GUID</span></span>                           |
| <span data-ttu-id="bf778-205">\_GUID d' \_ événement dropTarget supprimé \_</span><span class="sxs-lookup"><span data-stu-id="bf778-205">DropTarget\_Dropped\_Event\_GUID</span></span>                             |
| <span data-ttu-id="bf778-206">GUID de l' \_ événement HostedFragmentRootsInvalidated \_</span><span class="sxs-lookup"><span data-stu-id="bf778-206">HostedFragmentRootsInvalidated\_Event\_GUID</span></span>                  |
| <span data-ttu-id="bf778-207">GUID de l' \_ événement InputDiscarded \_</span><span class="sxs-lookup"><span data-stu-id="bf778-207">InputDiscarded\_Event\_GUID</span></span>                                  |
| <span data-ttu-id="bf778-208">GUID de l' \_ événement InputReachedOtherElement \_</span><span class="sxs-lookup"><span data-stu-id="bf778-208">InputReachedOtherElement\_Event\_GUID</span></span>                        |
| <span data-ttu-id="bf778-209">GUID de l' \_ événement InputReachedTarget \_</span><span class="sxs-lookup"><span data-stu-id="bf778-209">InputReachedTarget\_Event\_GUID</span></span>                              |
| <span data-ttu-id="bf778-210">Appeler le \_ GUID d' \_ événement appelé \_</span><span class="sxs-lookup"><span data-stu-id="bf778-210">Invoke\_Invoked\_Event\_GUID</span></span>                                 |
| <span data-ttu-id="bf778-211">GUID de l' \_ événement LayoutInvalidated \_</span><span class="sxs-lookup"><span data-stu-id="bf778-211">LayoutInvalidated\_Event\_GUID</span></span>                               |
| <span data-ttu-id="bf778-212">GUID de l' \_ événement LiveRegionChanged \_</span><span class="sxs-lookup"><span data-stu-id="bf778-212">LiveRegionChanged\_Event\_GUID</span></span>                               |
| <span data-ttu-id="bf778-213">GUID de l' \_ événement MenuClosed \_</span><span class="sxs-lookup"><span data-stu-id="bf778-213">MenuClosed\_Event\_GUID</span></span>                                      |
| <span data-ttu-id="bf778-214">GUID de l' \_ événement MenuModeEnd \_</span><span class="sxs-lookup"><span data-stu-id="bf778-214">MenuModeEnd\_Event\_GUID</span></span>                                     |
| <span data-ttu-id="bf778-215">GUID de l' \_ événement MenuModeStart \_</span><span class="sxs-lookup"><span data-stu-id="bf778-215">MenuModeStart\_Event\_GUID</span></span>                                   |
| <span data-ttu-id="bf778-216">GUID de l' \_ événement MenuOpened \_</span><span class="sxs-lookup"><span data-stu-id="bf778-216">MenuOpened\_Event\_GUID</span></span>                                      |
| <span data-ttu-id="bf778-217">GUID d’événement de sélection \_ InvalidatedEvent \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-217">Selection\_InvalidatedEvent\_Event\_GUID</span></span>                     |
| <span data-ttu-id="bf778-218">GUID de l' \_ événement SelectionItem ElementAddedToSelectionEvent \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-218">SelectionItem\_ElementAddedToSelectionEvent\_Event\_GUID</span></span>     |
| <span data-ttu-id="bf778-219">GUID de l' \_ événement SelectionItem ElementRemovedFromSelectionEvent \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-219">SelectionItem\_ElementRemovedFromSelectionEvent\_Event\_GUID</span></span> |
| <span data-ttu-id="bf778-220">GUID de l' \_ événement SelectionItem ElementSelectedEvent \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-220">SelectionItem\_ElementSelectedEvent\_Event\_GUID</span></span>             |
| <span data-ttu-id="bf778-221">GUID de l' \_ événement StructureChanged \_</span><span class="sxs-lookup"><span data-stu-id="bf778-221">StructureChanged\_Event\_GUID</span></span>                                |
| <span data-ttu-id="bf778-222">GUID de l' \_ événement SystemAlert \_</span><span class="sxs-lookup"><span data-stu-id="bf778-222">SystemAlert\_Event\_GUID</span></span>                                     |
| <span data-ttu-id="bf778-223">GUID de l' \_ événement Text TextChangedEvent \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-223">Text\_TextChangedEvent\_Event\_GUID</span></span>                          |
| <span data-ttu-id="bf778-224">GUID de l' \_ événement Text TextSelectionChangedEvent \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-224">Text\_TextSelectionChangedEvent\_Event\_GUID</span></span>                 |
| <span data-ttu-id="bf778-225">GUID de l' \_ événement ToolTipClosed \_</span><span class="sxs-lookup"><span data-stu-id="bf778-225">ToolTipClosed\_Event\_GUID</span></span>                                   |
| <span data-ttu-id="bf778-226">GUID d’événement de fenêtre \_ WindowOpened \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-226">Window\_WindowOpened\_Event\_GUID</span></span>                            |
| <span data-ttu-id="bf778-227">GUID de l' \_ événement ToolTipOpened \_</span><span class="sxs-lookup"><span data-stu-id="bf778-227">ToolTipOpened\_Event\_GUID</span></span>                                   |
| <span data-ttu-id="bf778-228">GUID d’événement de fenêtre \_ WindowClosed que \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-228">Window\_WindowClosed\_Event\_GUID</span></span>                            |



 

## <a name="propertyid-guids"></a><span data-ttu-id="bf778-229">GUID de PROPERTYID</span><span class="sxs-lookup"><span data-stu-id="bf778-229">PROPERTYID GUIDs</span></span>

<span data-ttu-id="bf778-230">Les GUIDs PROPERTYID qui représentent les propriétés UI Automation dans la fonction [**UiaLookupId**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uialookupid) sont répertoriés dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="bf778-230">The PROPERTYID GUIDs that represent UI Automation properties in the [**UiaLookupId**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uialookupid) function are listed in the following table.</span></span>



| <span data-ttu-id="bf778-231">GUID de PROPERTYID</span><span class="sxs-lookup"><span data-stu-id="bf778-231">PROPERTYID GUIDs</span></span>                                    |
|-----------------------------------------------------|
| <span data-ttu-id="bf778-232">GUID de la \_ propriété AcceleratorKey \_</span><span class="sxs-lookup"><span data-stu-id="bf778-232">AcceleratorKey\_Property\_GUID</span></span>                      |
| <span data-ttu-id="bf778-233">GUID de la \_ propriété AccessKey \_</span><span class="sxs-lookup"><span data-stu-id="bf778-233">AccessKey\_Property\_GUID</span></span>                           |
| <span data-ttu-id="bf778-234">GUID de la propriété d’annotation \_ AnnotationTypeId \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-234">Annotation\_AnnotationTypeId\_Property\_GUID</span></span>        |
| <span data-ttu-id="bf778-235">GUID de la propriété d’annotation \_ AnnotationTypeName \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-235">Annotation\_AnnotationTypeName\_Property\_GUID</span></span>      |
| <span data-ttu-id="bf778-236">GUID de la propriété de l’auteur de l’annotation \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-236">Annotation\_Author\_Property\_GUID</span></span>                  |
| <span data-ttu-id="bf778-237">GUID de la \_ propriété DateTime de l’annotation \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-237">Annotation\_DateTime\_Property\_GUID</span></span>                |
| <span data-ttu-id="bf778-238">GUID de la \_ propriété cible de l’annotation \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-238">Annotation\_Target\_Property\_GUID</span></span>                  |
| <span data-ttu-id="bf778-239">GUID de la \_ propriété AriaProperties \_</span><span class="sxs-lookup"><span data-stu-id="bf778-239">AriaProperties\_Property\_GUID</span></span>                      |
| <span data-ttu-id="bf778-240">GUID de la \_ Propriété AriaRole \_</span><span class="sxs-lookup"><span data-stu-id="bf778-240">AriaRole\_Property\_GUID</span></span>                            |
| <span data-ttu-id="bf778-241">GUID de la \_ propriété AutomationId \_</span><span class="sxs-lookup"><span data-stu-id="bf778-241">AutomationId\_Property\_GUID</span></span>                        |
| <span data-ttu-id="bf778-242">GUID de la \_ propriété BoundingRectangle \_</span><span class="sxs-lookup"><span data-stu-id="bf778-242">BoundingRectangle\_Property\_GUID</span></span>                   |
| <span data-ttu-id="bf778-243">GUID de la \_ propriété ClassName \_</span><span class="sxs-lookup"><span data-stu-id="bf778-243">ClassName\_Property\_GUID</span></span>                           |
| <span data-ttu-id="bf778-244">GUID de la \_ propriété ClickablePoint \_</span><span class="sxs-lookup"><span data-stu-id="bf778-244">ClickablePoint\_Property\_GUID</span></span>                      |
| <span data-ttu-id="bf778-245">GUID de la \_ propriété ControllerFor \_</span><span class="sxs-lookup"><span data-stu-id="bf778-245">ControllerFor\_Property\_GUID</span></span>                       |
| <span data-ttu-id="bf778-246">GUID de la \_ propriété ControlType \_</span><span class="sxs-lookup"><span data-stu-id="bf778-246">ControlType\_Property\_GUID</span></span>                         |
| <span data-ttu-id="bf778-247">\_GUID de propriété de culture \_</span><span class="sxs-lookup"><span data-stu-id="bf778-247">Culture\_Property\_GUID</span></span>                             |
| <span data-ttu-id="bf778-248">GUID de la \_ propriété DescribedBy \_</span><span class="sxs-lookup"><span data-stu-id="bf778-248">DescribedBy\_Property\_GUID</span></span>                         |
| <span data-ttu-id="bf778-249">GUID de la \_ propriété Dock DockPosition \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-249">Dock\_DockPosition\_Property\_GUID</span></span>                  |
| <span data-ttu-id="bf778-250">Déplacer le GUID de la \_ \_ propriété DropEffect \_</span><span class="sxs-lookup"><span data-stu-id="bf778-250">Drag\_DropEffect\_Property\_GUID</span></span>                    |
| <span data-ttu-id="bf778-251">Déplacer le GUID de la \_ \_ propriété DropEffects \_</span><span class="sxs-lookup"><span data-stu-id="bf778-251">Drag\_DropEffects\_Property\_GUID</span></span>                   |
| <span data-ttu-id="bf778-252">Déplacer le GUID de la \_ \_ propriété GrabbedItems \_</span><span class="sxs-lookup"><span data-stu-id="bf778-252">Drag\_GrabbedItems\_Property\_GUID</span></span>                  |
| <span data-ttu-id="bf778-253">Déplacer le GUID de la \_ \_ propriété IsGrabbed \_</span><span class="sxs-lookup"><span data-stu-id="bf778-253">Drag\_IsGrabbed\_Property\_GUID</span></span>                     |
| <span data-ttu-id="bf778-254">GUID de la \_ propriété dropTarget DropTargetEffect \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-254">DropTarget\_DropTargetEffect\_Property\_GUID</span></span>        |
| <span data-ttu-id="bf778-255">GUID de la \_ propriété dropTarget DropTargetEffects \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-255">DropTarget\_DropTargetEffects\_Property\_GUID</span></span>       |
| <span data-ttu-id="bf778-256">GUID de la \_ propriété ExpandCollapse ExpandCollapseState \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-256">ExpandCollapse\_ExpandCollapseState\_Property\_GUID</span></span> |
| <span data-ttu-id="bf778-257">GUID de la \_ propriété FlowsTo \_</span><span class="sxs-lookup"><span data-stu-id="bf778-257">FlowsTo\_Property\_GUID</span></span>                             |
| <span data-ttu-id="bf778-258">GUID de la \_ propriété FrameworkId \_</span><span class="sxs-lookup"><span data-stu-id="bf778-258">FrameworkId\_Property\_GUID</span></span>                         |
| <span data-ttu-id="bf778-259">GUID de la propriété de la grille \_ ColumnCount \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-259">Grid\_ColumnCount\_Property\_GUID</span></span>                   |
| <span data-ttu-id="bf778-260">GUID de la propriété de la grille \_ RowCount \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-260">Grid\_RowCount\_Property\_GUID</span></span>                      |
| <span data-ttu-id="bf778-261">GUID de la propriété de la \_ colonne GridItem \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-261">GridItem\_Column\_Property\_GUID</span></span>                    |
| <span data-ttu-id="bf778-262">GUID de la \_ propriété GridItem ColumnSpan \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-262">GridItem\_ColumnSpan\_Property\_GUID</span></span>                |
| <span data-ttu-id="bf778-263">GUID de la \_ propriété Parent GridItem \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-263">GridItem\_Parent\_Property\_GUID</span></span>                    |
| <span data-ttu-id="bf778-264">\_GUID de \_ propriété de ligne GridItem \_</span><span class="sxs-lookup"><span data-stu-id="bf778-264">GridItem\_Row\_Property\_GUID</span></span>                       |
| <span data-ttu-id="bf778-265">\_GUID de \_ propriété GridItem RowSpan \_</span><span class="sxs-lookup"><span data-stu-id="bf778-265">GridItem\_RowSpan\_Property\_GUID</span></span>                   |
| <span data-ttu-id="bf778-266">GUID de la \_ propriété HasKeyboardFocus \_</span><span class="sxs-lookup"><span data-stu-id="bf778-266">HasKeyboardFocus\_Property\_GUID</span></span>                    |
| <span data-ttu-id="bf778-267">GUID de la \_ propriété HelpText \_</span><span class="sxs-lookup"><span data-stu-id="bf778-267">HelpText\_Property\_GUID</span></span>                            |
| <span data-ttu-id="bf778-268">GUID de la \_ propriété IsAnnotationPatternAvailable \_</span><span class="sxs-lookup"><span data-stu-id="bf778-268">IsAnnotationPatternAvailable\_Property\_GUID</span></span>        |
| <span data-ttu-id="bf778-269">GUID de la \_ propriété IsContentElement \_</span><span class="sxs-lookup"><span data-stu-id="bf778-269">IsContentElement\_Property\_GUID</span></span>                    |
| <span data-ttu-id="bf778-270">GUID de la \_ propriété IsControlElement \_</span><span class="sxs-lookup"><span data-stu-id="bf778-270">IsControlElement\_Property\_GUID</span></span>                    |
| <span data-ttu-id="bf778-271">GUID de la \_ propriété IsDataValidForForm \_</span><span class="sxs-lookup"><span data-stu-id="bf778-271">IsDataValidForForm\_Property\_GUID</span></span>                  |
| <span data-ttu-id="bf778-272">GUID de la \_ propriété IsDockPatternAvailable \_</span><span class="sxs-lookup"><span data-stu-id="bf778-272">IsDockPatternAvailable\_Property\_GUID</span></span>              |
| <span data-ttu-id="bf778-273">GUID de la \_ propriété IsDragPatternAvailable \_</span><span class="sxs-lookup"><span data-stu-id="bf778-273">IsDragPatternAvailable\_Property\_GUID</span></span>              |
| <span data-ttu-id="bf778-274">GUID de la \_ propriété IsDropTargetPatternAvailable \_</span><span class="sxs-lookup"><span data-stu-id="bf778-274">IsDropTargetPatternAvailable\_Property\_GUID</span></span>        |
| <span data-ttu-id="bf778-275">GUID de la \_ propriété IsEnabled \_</span><span class="sxs-lookup"><span data-stu-id="bf778-275">IsEnabled\_Property\_GUID</span></span>                           |
| <span data-ttu-id="bf778-276">GUID de la \_ propriété IsExpandCollapsePatternAvailable \_</span><span class="sxs-lookup"><span data-stu-id="bf778-276">IsExpandCollapsePatternAvailable\_Property\_GUID</span></span>    |
| <span data-ttu-id="bf778-277">GUID de la \_ propriété IsGridItemPatternAvailable \_</span><span class="sxs-lookup"><span data-stu-id="bf778-277">IsGridItemPatternAvailable\_Property\_GUID</span></span>          |
| <span data-ttu-id="bf778-278">GUID de la \_ propriété IsGridPatternAvailable \_</span><span class="sxs-lookup"><span data-stu-id="bf778-278">IsGridPatternAvailable\_Property\_GUID</span></span>              |
| <span data-ttu-id="bf778-279">GUID de la \_ propriété IsInvokePatternAvailable \_</span><span class="sxs-lookup"><span data-stu-id="bf778-279">IsInvokePatternAvailable\_Property\_GUID</span></span>            |
| <span data-ttu-id="bf778-280">GUID de la \_ propriété IsItemContainerPatternAvailable \_</span><span class="sxs-lookup"><span data-stu-id="bf778-280">IsItemContainerPatternAvailable\_Property\_GUID</span></span>     |
| <span data-ttu-id="bf778-281">GUID de la \_ propriété IsKeyboardFocusable \_</span><span class="sxs-lookup"><span data-stu-id="bf778-281">IsKeyboardFocusable\_Property\_GUID</span></span>                 |
| <span data-ttu-id="bf778-282">GUID de la \_ propriété IsLegacyIAccessiblePatternAvailable \_</span><span class="sxs-lookup"><span data-stu-id="bf778-282">IsLegacyIAccessiblePatternAvailable\_Property\_GUID</span></span> |
| <span data-ttu-id="bf778-283">GUID de la \_ propriété IsMultipleViewPatternAvailable \_</span><span class="sxs-lookup"><span data-stu-id="bf778-283">IsMultipleViewPatternAvailable\_Property\_GUID</span></span>      |
| <span data-ttu-id="bf778-284">GUID de la \_ propriété IsObjectModelPatternAvailable \_</span><span class="sxs-lookup"><span data-stu-id="bf778-284">IsObjectModelPatternAvailable\_Property\_GUID</span></span>       |
| <span data-ttu-id="bf778-285">GUID de la \_ propriété IsOffscreen \_</span><span class="sxs-lookup"><span data-stu-id="bf778-285">IsOffscreen\_Property\_GUID</span></span>                         |
| <span data-ttu-id="bf778-286">GUID de la \_ propriété IsPassword \_</span><span class="sxs-lookup"><span data-stu-id="bf778-286">IsPassword\_Property\_GUID</span></span>                          |
| <span data-ttu-id="bf778-287">GUID de la \_ propriété IsRangeValuePatternAvailable \_</span><span class="sxs-lookup"><span data-stu-id="bf778-287">IsRangeValuePatternAvailable\_Property\_GUID</span></span>        |
| <span data-ttu-id="bf778-288">GUID de la \_ propriété IsRequiredForForm \_</span><span class="sxs-lookup"><span data-stu-id="bf778-288">IsRequiredForForm\_Property\_GUID</span></span>                   |
| <span data-ttu-id="bf778-289">GUID de la \_ propriété IsScrollItemPatternAvailable \_</span><span class="sxs-lookup"><span data-stu-id="bf778-289">IsScrollItemPatternAvailable\_Property\_GUID</span></span>        |
| <span data-ttu-id="bf778-290">GUID de la \_ propriété IsScrollPatternAvailable \_</span><span class="sxs-lookup"><span data-stu-id="bf778-290">IsScrollPatternAvailable\_Property\_GUID</span></span>            |
| <span data-ttu-id="bf778-291">GUID de la \_ propriété IsSelectionItemPatternAvailable \_</span><span class="sxs-lookup"><span data-stu-id="bf778-291">IsSelectionItemPatternAvailable\_Property\_GUID</span></span>     |
| <span data-ttu-id="bf778-292">GUID de la \_ propriété IsSelectionPatternAvailable \_</span><span class="sxs-lookup"><span data-stu-id="bf778-292">IsSelectionPatternAvailable\_Property\_GUID</span></span>         |
| <span data-ttu-id="bf778-293">GUID de la \_ propriété IsSpreadsheetPatternAvailable \_</span><span class="sxs-lookup"><span data-stu-id="bf778-293">IsSpreadsheetPatternAvailable\_Property\_GUID</span></span>       |
| <span data-ttu-id="bf778-294">GUID de la \_ propriété IsSpreadsheetItemPatternAvailable \_</span><span class="sxs-lookup"><span data-stu-id="bf778-294">IsSpreadsheetItemPatternAvailable\_Property\_GUID</span></span>   |
| <span data-ttu-id="bf778-295">GUID de la \_ propriété IsStylesPatternAvailable \_</span><span class="sxs-lookup"><span data-stu-id="bf778-295">IsStylesPatternAvailable\_Property\_GUID</span></span>            |
| <span data-ttu-id="bf778-296">GUID de la \_ propriété IsSynchronizedInputPatternAvailable \_</span><span class="sxs-lookup"><span data-stu-id="bf778-296">IsSynchronizedInputPatternAvailable\_Property\_GUID</span></span> |
| <span data-ttu-id="bf778-297">GUID de la \_ propriété IsTableItemPatternAvailable \_</span><span class="sxs-lookup"><span data-stu-id="bf778-297">IsTableItemPatternAvailable\_Property\_GUID</span></span>         |
| <span data-ttu-id="bf778-298">GUID de la \_ propriété IsTablePatternAvailable \_</span><span class="sxs-lookup"><span data-stu-id="bf778-298">IsTablePatternAvailable\_Property\_GUID</span></span>             |
| <span data-ttu-id="bf778-299">GUID de la \_ propriété IsTextChildPatternAvailable \_</span><span class="sxs-lookup"><span data-stu-id="bf778-299">IsTextChildPatternAvailable\_Property\_GUID</span></span>         |
| <span data-ttu-id="bf778-300">GUID de la \_ propriété IsTextPatternAvailable \_</span><span class="sxs-lookup"><span data-stu-id="bf778-300">IsTextPatternAvailable\_Property\_GUID</span></span>              |
| <span data-ttu-id="bf778-301">GUID de la \_ propriété IsTextPattern2Available \_</span><span class="sxs-lookup"><span data-stu-id="bf778-301">IsTextPattern2Available\_Property\_GUID</span></span>             |
| <span data-ttu-id="bf778-302">GUID de la \_ propriété IsTogglePatternAvailable \_</span><span class="sxs-lookup"><span data-stu-id="bf778-302">IsTogglePatternAvailable\_Property\_GUID</span></span>            |
| <span data-ttu-id="bf778-303">GUID de la \_ propriété IsTransformPatternAvailable \_</span><span class="sxs-lookup"><span data-stu-id="bf778-303">IsTransformPatternAvailable\_Property\_GUID</span></span>         |
| <span data-ttu-id="bf778-304">GUID de la \_ propriété IsTransformPattern2Available \_</span><span class="sxs-lookup"><span data-stu-id="bf778-304">IsTransformPattern2Available\_Property\_GUID</span></span>        |
| <span data-ttu-id="bf778-305">GUID de la \_ propriété IsValuePatternAvailable \_</span><span class="sxs-lookup"><span data-stu-id="bf778-305">IsValuePatternAvailable\_Property\_GUID</span></span>             |
| <span data-ttu-id="bf778-306">GUID de la \_ propriété IsVirtualizedItemPatternAvailable \_</span><span class="sxs-lookup"><span data-stu-id="bf778-306">IsVirtualizedItemPatternAvailable\_Property\_GUID</span></span>   |
| <span data-ttu-id="bf778-307">GUID de la \_ propriété IsWindowPatternAvailable \_</span><span class="sxs-lookup"><span data-stu-id="bf778-307">IsWindowPatternAvailable\_Property\_GUID</span></span>            |
| <span data-ttu-id="bf778-308">GUID de la \_ propriété ItemStatus \_</span><span class="sxs-lookup"><span data-stu-id="bf778-308">ItemStatus\_Property\_GUID</span></span>                          |
| <span data-ttu-id="bf778-309">GUID de la \_ propriété ItemType \_</span><span class="sxs-lookup"><span data-stu-id="bf778-309">ItemType\_Property\_GUID</span></span>                            |
| <span data-ttu-id="bf778-310">GUID de la \_ propriété LabeledBy \_</span><span class="sxs-lookup"><span data-stu-id="bf778-310">LabeledBy\_Property\_GUID</span></span>                           |
| <span data-ttu-id="bf778-311">GUID de la \_ propriété LegacyIAccessible childID \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-311">LegacyIAccessible\_ChildId\_Property\_GUID</span></span>          |
| <span data-ttu-id="bf778-312">GUID de la \_ propriété DEFAULTACTION LegacyIAccessible \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-312">LegacyIAccessible\_DefaultAction\_Property\_GUID</span></span>    |
| <span data-ttu-id="bf778-313">\_GUID de \_ propriété de description LegacyIAccessible \_</span><span class="sxs-lookup"><span data-stu-id="bf778-313">LegacyIAccessible\_Description\_Property\_GUID</span></span>      |
| <span data-ttu-id="bf778-314">GUID de la \_ propriété d’aide LegacyIAccessible \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-314">LegacyIAccessible\_Help\_Property\_GUID</span></span>             |
| <span data-ttu-id="bf778-315">GUID de la \_ propriété LegacyIAccessible KeyboardShortcut \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-315">LegacyIAccessible\_KeyboardShortcut\_Property\_GUID</span></span> |
| <span data-ttu-id="bf778-316">GUID de la propriété de nom de LegacyIAccessible \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-316">LegacyIAccessible\_Name\_Property\_GUID</span></span>             |
| <span data-ttu-id="bf778-317">GUID de la \_ propriété de rôle LegacyIAccessible \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-317">LegacyIAccessible\_Role\_Property\_GUID</span></span>             |
| <span data-ttu-id="bf778-318">GUID de la \_ propriété de sélection LegacyIAccessible \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-318">LegacyIAccessible\_Selection\_Property\_GUID</span></span>        |
| <span data-ttu-id="bf778-319">\_GUID de \_ propriété d’État LegacyIAccessible \_</span><span class="sxs-lookup"><span data-stu-id="bf778-319">LegacyIAccessible\_State\_Property\_GUID</span></span>            |
| <span data-ttu-id="bf778-320">GUID de la \_ propriété de valeur LegacyIAccessible \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-320">LegacyIAccessible\_Value\_Property\_GUID</span></span>            |
| <span data-ttu-id="bf778-321">GUID de la \_ propriété LiveSetting \_</span><span class="sxs-lookup"><span data-stu-id="bf778-321">LiveSetting\_Property\_GUID</span></span>                         |
| <span data-ttu-id="bf778-322">GUID de la \_ propriété LocalizedControlType \_</span><span class="sxs-lookup"><span data-stu-id="bf778-322">LocalizedControlType\_Property\_GUID</span></span>                |
| <span data-ttu-id="bf778-323">GUID de la \_ propriété CurrentView MultipleView \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-323">MultipleView\_CurrentView\_Property\_GUID</span></span>           |
| <span data-ttu-id="bf778-324">GUID de la \_ propriété MultipleView SupportedViews \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-324">MultipleView\_SupportedViews\_Property\_GUID</span></span>        |
| <span data-ttu-id="bf778-325">GUID de la \_ propriété Name \_</span><span class="sxs-lookup"><span data-stu-id="bf778-325">Name\_Property\_GUID</span></span>                                |
| <span data-ttu-id="bf778-326">GUID de la \_ propriété NewNativeWindowHandle \_</span><span class="sxs-lookup"><span data-stu-id="bf778-326">NewNativeWindowHandle\_Property\_GUID</span></span>               |
| <span data-ttu-id="bf778-327">GUID de la \_ propriété OptimizeForVisualContent \_</span><span class="sxs-lookup"><span data-stu-id="bf778-327">OptimizeForVisualContent\_Property\_GUID</span></span>            |
| <span data-ttu-id="bf778-328">GUID de la \_ propriété orientation \_</span><span class="sxs-lookup"><span data-stu-id="bf778-328">Orientation\_Property\_GUID</span></span>                         |
| <span data-ttu-id="bf778-329">GUID de la \_ propriété ProcessId \_</span><span class="sxs-lookup"><span data-stu-id="bf778-329">ProcessId\_Property\_GUID</span></span>                           |
| <span data-ttu-id="bf778-330">GUID de la \_ propriété ProviderDescription \_</span><span class="sxs-lookup"><span data-stu-id="bf778-330">ProviderDescription\_Property\_GUID</span></span>                 |
| <span data-ttu-id="bf778-331">GUID de la \_ propriété IsReadOnly RangeValue \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-331">RangeValue\_IsReadOnly\_Property\_GUID</span></span>              |
| <span data-ttu-id="bf778-332">GUID de la \_ propriété LargeChange RangeValue \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-332">RangeValue\_LargeChange\_Property\_GUID</span></span>             |
| <span data-ttu-id="bf778-333">\_GUID de \_ propriété \_ maximale RangeValue</span><span class="sxs-lookup"><span data-stu-id="bf778-333">RangeValue\_Maximum\_Property\_GUID</span></span>                 |
| <span data-ttu-id="bf778-334">GUID de la \_ propriété RangeValue minimum \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-334">RangeValue\_Minimum\_Property\_GUID</span></span>                 |
| <span data-ttu-id="bf778-335">GUID de la \_ propriété SmallChange RangeValue \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-335">RangeValue\_SmallChange\_Property\_GUID</span></span>             |
| <span data-ttu-id="bf778-336">GUID de la \_ propriété de valeur RangeValue \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-336">RangeValue\_Value\_Property\_GUID</span></span>                   |
| <span data-ttu-id="bf778-337">GUID de la \_ propriété RuntimeId \_</span><span class="sxs-lookup"><span data-stu-id="bf778-337">RuntimeId\_Property\_GUID</span></span>                           |
| <span data-ttu-id="bf778-338">GUID de la \_ propriété Scroll HorizontallyScrollable \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-338">Scroll\_HorizontallyScrollable\_Property\_GUID</span></span>      |
| <span data-ttu-id="bf778-339">GUID de la \_ propriété Scroll HorizontalScrollPercent \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-339">Scroll\_HorizontalScrollPercent\_Property\_GUID</span></span>     |
| <span data-ttu-id="bf778-340">GUID de la \_ propriété Scroll HorizontalViewSize \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-340">Scroll\_HorizontalViewSize\_Property\_GUID</span></span>          |
| <span data-ttu-id="bf778-341">GUID de la \_ propriété Scroll VerticallyScrollable \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-341">Scroll\_VerticallyScrollable\_Property\_GUID</span></span>        |
| <span data-ttu-id="bf778-342">GUID de la \_ propriété Scroll VerticalScrollPercent \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-342">Scroll\_VerticalScrollPercent\_Property\_GUID</span></span>       |
| <span data-ttu-id="bf778-343">GUID de la \_ propriété Scroll VerticalViewSize \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-343">Scroll\_VerticalViewSize\_Property\_GUID</span></span>            |
| <span data-ttu-id="bf778-344">GUID de la \_ propriété CanSelectMultiple de la sélection \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-344">Selection\_CanSelectMultiple\_Property\_GUID</span></span>        |
| <span data-ttu-id="bf778-345">GUID de la \_ propriété IsSelectionRequired de la sélection \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-345">Selection\_IsSelectionRequired\_Property\_GUID</span></span>      |
| <span data-ttu-id="bf778-346">GUID de la propriété sélection de la sélection \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-346">Selection\_Selection\_Property\_GUID</span></span>                |
| <span data-ttu-id="bf778-347">GUID de la \_ propriété IsSelected de SelectionItem \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-347">SelectionItem\_IsSelected\_Property\_GUID</span></span>           |
| <span data-ttu-id="bf778-348">GUID de la \_ propriété SelectionContainer SelectionItem \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-348">SelectionItem\_SelectionContainer\_Property\_GUID</span></span>   |
| <span data-ttu-id="bf778-349">GUID de la \_ propriété SpreadsheetItem AnnotationObjects \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-349">SpreadsheetItem\_AnnotationObjects\_Property\_GUID</span></span>  |
| <span data-ttu-id="bf778-350">GUID de la \_ propriété SpreadsheetItem AnnotationTypes \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-350">SpreadsheetItem\_AnnotationTypes\_Property\_GUID</span></span>    |
| <span data-ttu-id="bf778-351">GUID de la \_ propriété de formule SpreadsheetItem \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-351">SpreadsheetItem\_Formula\_Property\_GUID</span></span>            |
| <span data-ttu-id="bf778-352">Style \_ GUID de la \_ Propriété ExtendedProperties \_</span><span class="sxs-lookup"><span data-stu-id="bf778-352">Styles\_ExtendedProperties\_Property\_GUID</span></span>          |
| <span data-ttu-id="bf778-353">GUID de la \_ propriété FillColor des styles \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-353">Styles\_FillColor\_Property\_GUID</span></span>                   |
| <span data-ttu-id="bf778-354">GUID de la \_ propriété FillPatternColor des styles \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-354">Styles\_FillPatternColor\_Property\_GUID</span></span>            |
| <span data-ttu-id="bf778-355">GUID de la \_ propriété FillPatternStyle des styles \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-355">Styles\_FillPatternStyle\_Property\_GUID</span></span>            |
| <span data-ttu-id="bf778-356">GUID de la \_ propriété Shape styles \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-356">Styles\_Shape\_Property\_GUID</span></span>                       |
| <span data-ttu-id="bf778-357">GUID de la \_ propriété StyleId des styles \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-357">Styles\_StyleId\_Property\_GUID</span></span>                     |
| <span data-ttu-id="bf778-358">GUID de la propriété de styles \_ styleName \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-358">Styles\_StyleName\_Property\_GUID</span></span>                   |
| <span data-ttu-id="bf778-359">GUID de la propriété de table \_ têtes \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-359">Table\_ColumnHeaders\_Property\_GUID</span></span>                |
| <span data-ttu-id="bf778-360">GUID de la propriété de table \_ RowHeaders \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-360">Table\_RowHeaders\_Property\_GUID</span></span>                   |
| <span data-ttu-id="bf778-361">GUID de la propriété de table \_ RowOrColumnMajor \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-361">Table\_RowOrColumnMajor\_Property\_GUID</span></span>             |
| <span data-ttu-id="bf778-362">GUID de la \_ propriété TableItem ColumnHeaderItems \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-362">TableItem\_ColumnHeaderItems\_Property\_GUID</span></span>        |
| <span data-ttu-id="bf778-363">GUID de la \_ propriété TableItem RowHeaderItems \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-363">TableItem\_RowHeaderItems\_Property\_GUID</span></span>           |
| <span data-ttu-id="bf778-364">Activer/désactiver le GUID de la \_ \_ propriété ToggleState \_</span><span class="sxs-lookup"><span data-stu-id="bf778-364">Toggle\_ToggleState\_Property\_GUID</span></span>                 |
| <span data-ttu-id="bf778-365">GUID de la propriété de transformation \_ CanMove \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-365">Transform\_CanMove\_Property\_GUID</span></span>                  |
| <span data-ttu-id="bf778-366">GUID de la propriété de transformation \_ CanResize \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-366">Transform\_CanResize\_Property\_GUID</span></span>                |
| <span data-ttu-id="bf778-367">GUID de la propriété de transformation \_ CanRotate \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-367">Transform\_CanRotate\_Property\_GUID</span></span>                |
| <span data-ttu-id="bf778-368">GUID de la \_ propriété Transform2 CanZoom \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-368">Transform2\_CanZoom\_Property\_GUID</span></span>                 |
| <span data-ttu-id="bf778-369">GUID de la \_ propriété Transform2 zoomLevel \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-369">Transform2\_ZoomLevel\_Property\_GUID</span></span>               |
| <span data-ttu-id="bf778-370">GUID de la \_ propriété Transform2 ZoomMaximum \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-370">Transform2\_ZoomMaximum\_Property\_GUID</span></span>             |
| <span data-ttu-id="bf778-371">GUID de la \_ propriété Transform2 ZoomMinimum \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-371">Transform2\_ZoomMinimum\_Property\_GUID</span></span>             |
| <span data-ttu-id="bf778-372">Valeur \_ GUID de la \_ propriété IsReadOnly \_</span><span class="sxs-lookup"><span data-stu-id="bf778-372">Value\_IsReadOnly\_Property\_GUID</span></span>                   |
| <span data-ttu-id="bf778-373">Valeur \_ GUID de la \_ propriété value \_</span><span class="sxs-lookup"><span data-stu-id="bf778-373">Value\_Value\_Property\_GUID</span></span>                        |
| <span data-ttu-id="bf778-374">GUID de la \_ propriété CanMaximize de la fenêtre \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-374">Window\_CanMaximize\_Property\_GUID</span></span>                 |
| <span data-ttu-id="bf778-375">GUID de la \_ propriété CanMinimize de la fenêtre \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-375">Window\_CanMinimize\_Property\_GUID</span></span>                 |
| <span data-ttu-id="bf778-376">GUID de la \_ propriété IsModal de la fenêtre \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-376">Window\_IsModal\_Property\_GUID</span></span>                     |
| <span data-ttu-id="bf778-377">GUID de la \_ propriété IsTopmost de la fenêtre \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-377">Window\_IsTopmost\_Property\_GUID</span></span>                   |
| <span data-ttu-id="bf778-378">GUID de la \_ propriété WindowInteractionState de la fenêtre \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-378">Window\_WindowInteractionState\_Property\_GUID</span></span>      |
| <span data-ttu-id="bf778-379">GUID de la \_ propriété WindowVisualState de la fenêtre \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-379">Window\_WindowVisualState\_Property\_GUID</span></span>           |



 

## <a name="textattributeid-guids"></a><span data-ttu-id="bf778-380">GUID TEXTATTRIBUTEID</span><span class="sxs-lookup"><span data-stu-id="bf778-380">TEXTATTRIBUTEID GUIDs</span></span>

<span data-ttu-id="bf778-381">Les GUID TEXTATTRIBUTEID qui représentent des attributs de texte dans la fonction [**UiaLookupId**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uialookupid) sont répertoriés dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="bf778-381">The TEXTATTRIBUTEID GUIDs that represent text attributes in the [**UiaLookupId**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uialookupid) function are listed in the following table.</span></span>



| <span data-ttu-id="bf778-382">GUID TEXTATTRIBUTEID</span><span class="sxs-lookup"><span data-stu-id="bf778-382">TEXTATTRIBUTEID GUIDs</span></span>                          |
|------------------------------------------------|
| <span data-ttu-id="bf778-383">GUID de l' \_ attribut AnimationStyle de texte \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-383">Text\_AnimationStyle\_Attribute\_GUID</span></span>          |
| <span data-ttu-id="bf778-384">GUID de l' \_ attribut AnnotationObjects de texte \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-384">Text\_AnnotationObjects\_Attribute\_GUID</span></span>       |
| <span data-ttu-id="bf778-385">GUID de l' \_ attribut AnnotationTypes de texte \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-385">Text\_AnnotationTypes\_Attribute\_GUID</span></span>         |
| <span data-ttu-id="bf778-386">GUID de l' \_ attribut Text BackgroundColor \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-386">Text\_BackgroundColor\_Attribute\_GUID</span></span>         |
| <span data-ttu-id="bf778-387">GUID de l' \_ attribut BulletStyle de texte \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-387">Text\_BulletStyle\_Attribute\_GUID</span></span>             |
| <span data-ttu-id="bf778-388">GUID de l' \_ attribut CapStyle de texte \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-388">Text\_CapStyle\_Attribute\_GUID</span></span>                |
| <span data-ttu-id="bf778-389">GUID de l' \_ attribut CaretBidiMode de texte \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-389">Text\_CaretBidiMode\_Attribute\_GUID</span></span>           |
| <span data-ttu-id="bf778-390">GUID de l' \_ attribut CaretPosition de texte \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-390">Text\_CaretPosition\_Attribute\_GUID</span></span>           |
| <span data-ttu-id="bf778-391">GUID de l’attribut de culture du texte \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-391">Text\_Culture\_Attribute\_GUID</span></span>                 |
| <span data-ttu-id="bf778-392">GUID de l' \_ attribut FontName du texte \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-392">Text\_FontName\_Attribute\_GUID</span></span>                |
| <span data-ttu-id="bf778-393">GUID de l' \_ attribut Text FontSize \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-393">Text\_FontSize\_Attribute\_GUID</span></span>                |
| <span data-ttu-id="bf778-394">GUID de l' \_ attribut FontWeight de texte \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-394">Text\_FontWeight\_Attribute\_GUID</span></span>              |
| <span data-ttu-id="bf778-395">GUID de l' \_ attribut ForegroundColor de texte \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-395">Text\_ForegroundColor\_Attribute\_GUID</span></span>         |
| <span data-ttu-id="bf778-396">GUID de l' \_ attribut HorizontalTextAlignment de texte \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-396">Text\_HorizontalTextAlignment\_Attribute\_GUID</span></span> |
| <span data-ttu-id="bf778-397">GUID de l' \_ attribut IndentationFirstLine de texte \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-397">Text\_IndentationFirstLine\_Attribute\_GUID</span></span>    |
| <span data-ttu-id="bf778-398">GUID de l' \_ attribut IndentationLeading de texte \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-398">Text\_IndentationLeading\_Attribute\_GUID</span></span>      |
| <span data-ttu-id="bf778-399">GUID de l' \_ attribut IndentationTrailing de texte \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-399">Text\_IndentationTrailing\_Attribute\_GUID</span></span>     |
| <span data-ttu-id="bf778-400">GUID de l' \_ attribut IsActive Text \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-400">Text\_IsActive\_Attribute\_GUID</span></span>                |
| <span data-ttu-id="bf778-401">GUID de l' \_ attribut IsHidden de texte \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-401">Text\_IsHidden\_Attribute\_GUID</span></span>                |
| <span data-ttu-id="bf778-402">GUID de l' \_ attribut IsItalic de texte \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-402">Text\_IsItalic\_Attribute\_GUID</span></span>                |
| <span data-ttu-id="bf778-403">GUID de l’attribut de texte \_ IsReadOnly \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-403">Text\_IsReadOnly\_Attribute\_GUID</span></span>              |
| <span data-ttu-id="bf778-404">GUID de l' \_ attribut IsSubscript de texte \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-404">Text\_IsSubscript\_Attribute\_GUID</span></span>             |
| <span data-ttu-id="bf778-405">GUID de l' \_ attribut IsSuperscript de texte \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-405">Text\_IsSuperscript\_Attribute\_GUID</span></span>           |
| <span data-ttu-id="bf778-406">GUID de l’attribut de lien de texte \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-406">Text\_Link\_Attribute\_GUID</span></span>                    |
| <span data-ttu-id="bf778-407">GUID de l' \_ attribut marginBottom Text \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-407">Text\_MarginBottom\_Attribute\_GUID</span></span>            |
| <span data-ttu-id="bf778-408">GUID de l' \_ attribut MarginLeading de texte \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-408">Text\_MarginLeading\_Attribute\_GUID</span></span>           |
| <span data-ttu-id="bf778-409">GUID de l' \_ attribut marginTop de texte \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-409">Text\_MarginTop\_Attribute\_GUID</span></span>               |
| <span data-ttu-id="bf778-410">GUID de l' \_ attribut MarginTrailing de texte \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-410">Text\_MarginTrailing\_Attribute\_GUID</span></span>          |
| <span data-ttu-id="bf778-411">GUID de l' \_ attribut OutlineStyles de texte \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-411">Text\_OutlineStyles\_Attribute\_GUID</span></span>           |
| <span data-ttu-id="bf778-412">GUID de l' \_ attribut OverlineColor de texte \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-412">Text\_OverlineColor\_Attribute\_GUID</span></span>           |
| <span data-ttu-id="bf778-413">GUID de l' \_ attribut OverlineStyle de texte \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-413">Text\_OverlineStyle\_Attribute\_GUID</span></span>           |
| <span data-ttu-id="bf778-414">GUID de l' \_ attribut SelectionActiveEnd de texte \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-414">Text\_SelectionActiveEnd\_Attribute\_GUID</span></span>      |
| <span data-ttu-id="bf778-415">GUID de l' \_ attribut StrikethroughColor de texte \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-415">Text\_StrikethroughColor\_Attribute\_GUID</span></span>      |
| <span data-ttu-id="bf778-416">GUID de l' \_ attribut StrikethroughStyle de texte \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-416">Text\_StrikethroughStyle\_Attribute\_GUID</span></span>      |
| <span data-ttu-id="bf778-417">GUID de l' \_ attribut StyleId de texte \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-417">Text\_StyleId\_Attribute\_GUID</span></span>                 |
| <span data-ttu-id="bf778-418">GUID de l' \_ attribut styleName Text \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-418">Text\_StyleName\_Attribute\_GUID</span></span>               |
| <span data-ttu-id="bf778-419">GUID de l' \_ attribut Text Tabs \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-419">Text\_Tabs\_Attribute\_GUID</span></span>                    |
| <span data-ttu-id="bf778-420">GUID de l' \_ attribut TextFlowDirection de texte \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-420">Text\_TextFlowDirection\_Attribute\_GUID</span></span>       |
| <span data-ttu-id="bf778-421">GUID de l' \_ attribut UnderlineColor de texte \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-421">Text\_UnderlineColor\_Attribute\_GUID</span></span>          |
| <span data-ttu-id="bf778-422">GUID de l' \_ attribut UnderlineStyle de texte \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf778-422">Text\_UnderlineStyle\_Attribute\_GUID</span></span>          |



 

 

 




