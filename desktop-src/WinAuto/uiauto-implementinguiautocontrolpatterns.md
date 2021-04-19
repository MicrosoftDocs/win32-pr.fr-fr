---
title: Implémentation des modèles de contrôle UI Automation
description: Cette section fournit des informations détaillées sur l’implémentation des interfaces de fournisseur Microsoft UI Automation qui prennent en charge les modèles de contrôle.
ms.assetid: d1baa245-62a1-40b1-a671-e227dd3df60a
keywords:
- UI Automation, implémenter des modèles de contrôle
- UI Automation, modèles de contrôle
- implémentation des modèles de contrôle UI Automation
- modèles de contrôle, implémenter UI Automation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bfb75b6b275fee9230eb25d9a0b02e1da26ad4d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106518021"
---
# <a name="implementing-ui-automation-control-patterns"></a><span data-ttu-id="7d673-107">Implémentation des modèles de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="7d673-107">Implementing UI Automation Control Patterns</span></span>

<span data-ttu-id="7d673-108">Cette section fournit des informations détaillées sur l’implémentation des interfaces de fournisseur Microsoft UI Automation qui prennent en charge les modèles de contrôle.</span><span class="sxs-lookup"><span data-stu-id="7d673-108">This section provides detailed information about implementing the Microsoft UI Automation provider interfaces that support control patterns.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7d673-109">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="7d673-109">In this section</span></span>

-   [<span data-ttu-id="7d673-110">Annotation (modèle de contrôle)</span><span class="sxs-lookup"><span data-stu-id="7d673-110">Annotation Control Pattern</span></span>](uiauto-implementingannotation.md)
-   [<span data-ttu-id="7d673-111">Modèle de contrôle CustomNavigation</span><span class="sxs-lookup"><span data-stu-id="7d673-111">CustomNavigation Control Pattern</span></span>](uiauto-implementingcustomnavigation.md)
-   [<span data-ttu-id="7d673-112">Dock (modèle de contrôle)</span><span class="sxs-lookup"><span data-stu-id="7d673-112">Dock Control Pattern</span></span>](uiauto-implementingdock.md)
-   [<span data-ttu-id="7d673-113">Faire glisser le modèle de contrôle</span><span class="sxs-lookup"><span data-stu-id="7d673-113">Drag Control Pattern</span></span>](/windows/desktop/WinAuto/uiauto-implementingdrag)
-   [<span data-ttu-id="7d673-114">Modèle de contrôle DropTarget</span><span class="sxs-lookup"><span data-stu-id="7d673-114">DropTarget Control Pattern</span></span>](/windows/desktop/WinAuto/uiauto-implementingdroptarget)
-   [<span data-ttu-id="7d673-115">Modèle de contrôle ExpandCollapse</span><span class="sxs-lookup"><span data-stu-id="7d673-115">ExpandCollapse Control Pattern</span></span>](uiauto-implementingexpandcollapse.md)
-   [<span data-ttu-id="7d673-116">Grid (modèle de contrôle)</span><span class="sxs-lookup"><span data-stu-id="7d673-116">Grid Control Pattern</span></span>](uiauto-implementinggrid.md)
-   [<span data-ttu-id="7d673-117">GridItem (modèle de contrôle)</span><span class="sxs-lookup"><span data-stu-id="7d673-117">GridItem Control Pattern</span></span>](uiauto-implementinggriditem.md)
-   [<span data-ttu-id="7d673-118">Invoke (modèle de contrôle)</span><span class="sxs-lookup"><span data-stu-id="7d673-118">Invoke Control Pattern</span></span>](uiauto-implementinginvoke.md)
-   [<span data-ttu-id="7d673-119">Modèle de contrôle ItemContainer</span><span class="sxs-lookup"><span data-stu-id="7d673-119">ItemContainer Control Pattern</span></span>](uiauto-implementingitemcontainer.md)
-   [<span data-ttu-id="7d673-120">Modèle de contrôle LegacyIAccessible</span><span class="sxs-lookup"><span data-stu-id="7d673-120">LegacyIAccessible Control Pattern</span></span>](uiauto-implementinglegacyiaccessible.md)
-   [<span data-ttu-id="7d673-121">Modèle de contrôle MultipleView</span><span class="sxs-lookup"><span data-stu-id="7d673-121">MultipleView Control Pattern</span></span>](uiauto-implementingmultipleview.md)
-   [<span data-ttu-id="7d673-122">ObjectModel (modèle de contrôle)</span><span class="sxs-lookup"><span data-stu-id="7d673-122">ObjectModel Control Pattern</span></span>](uiauto-implementingobjectmodel.md)
-   [<span data-ttu-id="7d673-123">Modèle de contrôle RangeValue</span><span class="sxs-lookup"><span data-stu-id="7d673-123">RangeValue Control Pattern</span></span>](uiauto-implementingrangevalue.md)
-   [<span data-ttu-id="7d673-124">Scroll (modèle de contrôle)</span><span class="sxs-lookup"><span data-stu-id="7d673-124">Scroll Control Pattern</span></span>](uiauto-implementingscroll.md)
-   [<span data-ttu-id="7d673-125">Modèle de contrôle ScrollItem</span><span class="sxs-lookup"><span data-stu-id="7d673-125">ScrollItem Control Pattern</span></span>](uiauto-implementingscrollitem.md)
-   [<span data-ttu-id="7d673-126">Selection (modèle de contrôle)</span><span class="sxs-lookup"><span data-stu-id="7d673-126">Selection Control Pattern</span></span>](uiauto-implementingselection.md)
-   [<span data-ttu-id="7d673-127">Modèle de contrôle SelectionItem</span><span class="sxs-lookup"><span data-stu-id="7d673-127">SelectionItem Control Pattern</span></span>](uiauto-implementingselectionitem.md)
-   [<span data-ttu-id="7d673-128">Spreadsheet (modèle de contrôle)</span><span class="sxs-lookup"><span data-stu-id="7d673-128">Spreadsheet Control Pattern</span></span>](uiauto-implementingspreadsheet.md)
-   [<span data-ttu-id="7d673-129">Modèle de contrôle SpreadsheetItem</span><span class="sxs-lookup"><span data-stu-id="7d673-129">SpreadsheetItem Control Pattern</span></span>](uiauto-implementingspreadsheetitem.md)
-   [<span data-ttu-id="7d673-130">Styles (modèle de contrôle)</span><span class="sxs-lookup"><span data-stu-id="7d673-130">Styles Control Pattern</span></span>](/windows/desktop/WinAuto/uiauto-implementingstyles)
-   [<span data-ttu-id="7d673-131">Modèle de contrôle SynchronizedInput</span><span class="sxs-lookup"><span data-stu-id="7d673-131">SynchronizedInput Control Pattern</span></span>](uiauto-implementingsynchronizedinput.md)
-   [<span data-ttu-id="7d673-132">Table (modèle de contrôle)</span><span class="sxs-lookup"><span data-stu-id="7d673-132">Table Control Pattern</span></span>](uiauto-implementingtable.md)
-   [<span data-ttu-id="7d673-133">Modèle de contrôle TableItem</span><span class="sxs-lookup"><span data-stu-id="7d673-133">TableItem Control Pattern</span></span>](uiauto-implementingtableitem.md)
-   [<span data-ttu-id="7d673-134">Modèles de contrôle Text et TextRange</span><span class="sxs-lookup"><span data-stu-id="7d673-134">Text and TextRange Control Patterns</span></span>](uiauto-implementingtextandtextrange.md)
-   [<span data-ttu-id="7d673-135">Modèle de contrôle TextChild</span><span class="sxs-lookup"><span data-stu-id="7d673-135">TextChild Control Pattern</span></span>](textchild-control-pattern.md)
-   [<span data-ttu-id="7d673-136">TextEdit (modèle de contrôle)</span><span class="sxs-lookup"><span data-stu-id="7d673-136">TextEdit Control Pattern</span></span>](textedit-control-pattern.md)
-   [<span data-ttu-id="7d673-137">Basculer le modèle de contrôle</span><span class="sxs-lookup"><span data-stu-id="7d673-137">Toggle Control Pattern</span></span>](uiauto-implementingtoggle.md)
-   [<span data-ttu-id="7d673-138">Transform (modèle de contrôle)</span><span class="sxs-lookup"><span data-stu-id="7d673-138">Transform Control Pattern</span></span>](uiauto-implementingtransform.md)
-   [<span data-ttu-id="7d673-139">Value (modèle de contrôle)</span><span class="sxs-lookup"><span data-stu-id="7d673-139">Value Control Pattern</span></span>](uiauto-implementingvalue.md)
-   [<span data-ttu-id="7d673-140">Modèle de contrôle VirtualizedItem</span><span class="sxs-lookup"><span data-stu-id="7d673-140">VirtualizedItem Control Pattern</span></span>](uiauto-implementingvirtualizeditem.md)
-   [<span data-ttu-id="7d673-141">Window (modèle de contrôle)</span><span class="sxs-lookup"><span data-stu-id="7d673-141">Window Control Pattern</span></span>](uiauto-implementingwindow.md)

## <a name="related-topics"></a><span data-ttu-id="7d673-142">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7d673-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d673-143">Guide du programmeur du fournisseur UI Automation</span><span class="sxs-lookup"><span data-stu-id="7d673-143">UI Automation Provider Programmer's Guide</span></span>](uiauto-providerportal.md)
</dt> <dt>

[<span data-ttu-id="7d673-144">Vue d'ensemble des modèles de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="7d673-144">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="7d673-145">Prise en charge des types de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="7d673-145">Supporting UI Automation Control Types</span></span>](uiauto-supportinguiautocontroltypes.md)
</dt> </dl>

 

 