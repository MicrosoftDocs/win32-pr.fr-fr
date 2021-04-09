---
description: Si ce bit est défini, les éléments répertoriés dans le contrôle sont affichés dans un ordre spécifié. Si le bit n’est pas défini, les éléments sont affichés par ordre alphabétique.
ms.assetid: c55bf6bf-6625-47cb-867a-14b3ef8aea0a
title: Attribut de contrôle trié
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a84af4b0683e35c66e159602b9ed2fe1b3005d8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033864"
---
# <a name="sorted-control-attribute"></a><span data-ttu-id="00a9f-104">Attribut de contrôle trié</span><span class="sxs-lookup"><span data-stu-id="00a9f-104">Sorted Control Attribute</span></span>

<span data-ttu-id="00a9f-105">Si ce bit est défini, les éléments répertoriés dans le contrôle sont affichés dans un ordre spécifié.</span><span class="sxs-lookup"><span data-stu-id="00a9f-105">If this bit is set, the items listed in the control are displayed in a specified order.</span></span> <span data-ttu-id="00a9f-106">Si le bit n’est pas défini, les éléments sont affichés par ordre alphabétique.</span><span class="sxs-lookup"><span data-stu-id="00a9f-106">If the bit is not set, items are displayed in alphabetical order.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="00a9f-107">Contrôles valides</span><span class="sxs-lookup"><span data-stu-id="00a9f-107">Valid Controls</span></span>

[<span data-ttu-id="00a9f-108">ComboBox</span><span class="sxs-lookup"><span data-stu-id="00a9f-108">ComboBox</span></span>](combobox-control.md)

 

[<span data-ttu-id="00a9f-109">ListBox</span><span class="sxs-lookup"><span data-stu-id="00a9f-109">ListBox</span></span>](listbox-control.md)

 

[<span data-ttu-id="00a9f-110">Contrôle ListView</span><span class="sxs-lookup"><span data-stu-id="00a9f-110">ListView Control</span></span>](listview-control.md)

## <a name="value"></a><span data-ttu-id="00a9f-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="00a9f-111">Value</span></span>



| <span data-ttu-id="00a9f-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="00a9f-112">Decimal</span></span> | <span data-ttu-id="00a9f-113">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="00a9f-113">Hexadecimal</span></span> | <span data-ttu-id="00a9f-114">Constante</span><span class="sxs-lookup"><span data-stu-id="00a9f-114">Constant</span></span>                         |
|---------|-------------|----------------------------------|
| <span data-ttu-id="00a9f-115">65536</span><span class="sxs-lookup"><span data-stu-id="00a9f-115">65536</span></span>   | <span data-ttu-id="00a9f-116">0x00010000</span><span class="sxs-lookup"><span data-stu-id="00a9f-116">0x00010000</span></span>  | <span data-ttu-id="00a9f-117">**msidbControlAttributesSorted**</span><span class="sxs-lookup"><span data-stu-id="00a9f-117">**msidbControlAttributesSorted**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="00a9f-118">Notes</span><span class="sxs-lookup"><span data-stu-id="00a9f-118">Remarks</span></span>

<span data-ttu-id="00a9f-119">Pour trier les éléments d’une [zone de liste déroulante](combobox-control.md), incluez le bit trié dans la colonne attributs de la [table de contrôle](control-table.md) et spécifiez l’ordre des éléments dans la colonne Order de la table de [zone de liste déroulante](combobox-table.md).</span><span class="sxs-lookup"><span data-stu-id="00a9f-119">To sort the items in a [ComboBox](combobox-control.md), include the Sorted bit in the Attributes column of the [Control table](control-table.md) and specify the item order in the Order column of the [ComboBox table](combobox-table.md).</span></span>

<span data-ttu-id="00a9f-120">Pour trier les éléments d’une [zone de liste](listbox-control.md), incluez le bit trié dans la colonne attributs de la [table de contrôle](control-table.md) et spécifiez l’ordre des éléments dans la colonne Order de la table de [zone de liste déroulante](combobox-table.md).</span><span class="sxs-lookup"><span data-stu-id="00a9f-120">To sort the items in a [ListBox](listbox-control.md), include the Sorted bit in the Attributes column of the [Control table](control-table.md) and specify the item order in the Order column of the [ComboBox table](combobox-table.md).</span></span>

<span data-ttu-id="00a9f-121">Pour trier les éléments dans un [ListView](listview-control.md), incluez le bit trié dans la colonne attributs de la [table de contrôle](control-table.md) et spécifiez l’ordre des éléments dans la table de zone de [liste déroulante](combobox-table.md).</span><span class="sxs-lookup"><span data-stu-id="00a9f-121">To sort the items in a [ListView](listview-control.md), include the Sorted bit in the Attributes column of the [Control table](control-table.md) and specify the order of items in the [ComboBox table](combobox-table.md).</span></span>

<span data-ttu-id="00a9f-122">Consultez [contrôle des attributs](control-attributes.md) et des [contrôles](controls.md).</span><span class="sxs-lookup"><span data-stu-id="00a9f-122">See [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



