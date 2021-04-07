---
description: Les lignes d’une zone de liste ne sont pas traitées comme des contrôles individuels, mais elles font partie d’une zone de liste qui fonctionne comme un contrôle. La table ListBox définit les valeurs de toutes les zones de liste.
ms.assetid: 1963adcf-f682-4371-ab44-f91e90105dc0
title: Table ListBox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5f60fb6ac48860c7893b0320b54e6e54dcf1691
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952284"
---
# <a name="listbox-table"></a><span data-ttu-id="a22fb-104">Table ListBox</span><span class="sxs-lookup"><span data-stu-id="a22fb-104">ListBox Table</span></span>

<span data-ttu-id="a22fb-105">Les lignes d’une zone de liste ne sont pas traitées comme des contrôles individuels, mais elles font partie d’une zone de liste qui fonctionne comme un contrôle.</span><span class="sxs-lookup"><span data-stu-id="a22fb-105">The lines of a list box are not treated as individual controls, but they are part of a list box that functions as a control.</span></span> <span data-ttu-id="a22fb-106">La table ListBox définit les valeurs de toutes les zones de liste.</span><span class="sxs-lookup"><span data-stu-id="a22fb-106">The ListBox table defines the values for all list boxes.</span></span>

<span data-ttu-id="a22fb-107">La table ListBox contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="a22fb-107">The ListBox table has the following columns.</span></span>



| <span data-ttu-id="a22fb-108">Colonne</span><span class="sxs-lookup"><span data-stu-id="a22fb-108">Column</span></span>   | <span data-ttu-id="a22fb-109">Type</span><span class="sxs-lookup"><span data-stu-id="a22fb-109">Type</span></span>                         | <span data-ttu-id="a22fb-110">Clé</span><span class="sxs-lookup"><span data-stu-id="a22fb-110">Key</span></span> | <span data-ttu-id="a22fb-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="a22fb-111">Nullable</span></span> |
|----------|------------------------------|-----|----------|
| <span data-ttu-id="a22fb-112">Propriété</span><span class="sxs-lookup"><span data-stu-id="a22fb-112">Property</span></span> | [<span data-ttu-id="a22fb-113">Identificateur</span><span class="sxs-lookup"><span data-stu-id="a22fb-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="a22fb-114">O</span><span class="sxs-lookup"><span data-stu-id="a22fb-114">Y</span></span>   | <span data-ttu-id="a22fb-115">N</span><span class="sxs-lookup"><span data-stu-id="a22fb-115">N</span></span>        |
| <span data-ttu-id="a22fb-116">Commande</span><span class="sxs-lookup"><span data-stu-id="a22fb-116">Order</span></span>    | [<span data-ttu-id="a22fb-117">Integer</span><span class="sxs-lookup"><span data-stu-id="a22fb-117">Integer</span></span>](integer.md)       | <span data-ttu-id="a22fb-118">O</span><span class="sxs-lookup"><span data-stu-id="a22fb-118">Y</span></span>   | <span data-ttu-id="a22fb-119">N</span><span class="sxs-lookup"><span data-stu-id="a22fb-119">N</span></span>        |
| <span data-ttu-id="a22fb-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="a22fb-120">Value</span></span>    | [<span data-ttu-id="a22fb-121">Correct</span><span class="sxs-lookup"><span data-stu-id="a22fb-121">Formatted</span></span>](formatted.md)   | <span data-ttu-id="a22fb-122">N</span><span class="sxs-lookup"><span data-stu-id="a22fb-122">N</span></span>   | <span data-ttu-id="a22fb-123">N</span><span class="sxs-lookup"><span data-stu-id="a22fb-123">N</span></span>        |
| <span data-ttu-id="a22fb-124">Texte</span><span class="sxs-lookup"><span data-stu-id="a22fb-124">Text</span></span>     | [<span data-ttu-id="a22fb-125">Correct</span><span class="sxs-lookup"><span data-stu-id="a22fb-125">Formatted</span></span>](formatted.md)   | <span data-ttu-id="a22fb-126">N</span><span class="sxs-lookup"><span data-stu-id="a22fb-126">N</span></span>   | <span data-ttu-id="a22fb-127">O</span><span class="sxs-lookup"><span data-stu-id="a22fb-127">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="a22fb-128">Colonnes</span><span class="sxs-lookup"><span data-stu-id="a22fb-128">Columns</span></span>

<dl> <dt>

<span data-ttu-id="a22fb-129"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Propriété</span><span class="sxs-lookup"><span data-stu-id="a22fb-129"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property</span></span>
</dt> <dd>

<span data-ttu-id="a22fb-130">Propriété nommée à être liée à cet élément.</span><span class="sxs-lookup"><span data-stu-id="a22fb-130">A named property to be tied to this item.</span></span> <span data-ttu-id="a22fb-131">Tous les éléments liés à la même propriété deviennent partie intégrante de la même zone de liste.</span><span class="sxs-lookup"><span data-stu-id="a22fb-131">All the items tied to the same property become part of the same list box.</span></span>

</dd> <dt>

<span data-ttu-id="a22fb-132"><span id="Order"></span><span id="order"></span><span id="ORDER"></span>Ordre</span><span class="sxs-lookup"><span data-stu-id="a22fb-132"><span id="Order"></span><span id="order"></span><span id="ORDER"></span>Order</span></span>
</dt> <dd>

<span data-ttu-id="a22fb-133">Entier positif utilisé pour déterminer l’ordre des éléments qui s’affichent dans une zone de liste unique.</span><span class="sxs-lookup"><span data-stu-id="a22fb-133">A positive integer used to determine the ordering of the items that appear in a single list box.</span></span> <span data-ttu-id="a22fb-134">Si la zone de liste est définie comme étant ordonnée, tous les éléments doivent avoir une valeur d’ordre.</span><span class="sxs-lookup"><span data-stu-id="a22fb-134">If the list box is defined as ordered, then all items should have an Order value.</span></span> <span data-ttu-id="a22fb-135">Il n’est pas nécessaire que les entiers soient consécutifs.</span><span class="sxs-lookup"><span data-stu-id="a22fb-135">The integers do not have to be consecutive.</span></span> <span data-ttu-id="a22fb-136">Si la zone de liste est définie comme non triée, cette colonne est ignorée.</span><span class="sxs-lookup"><span data-stu-id="a22fb-136">If the list box is defined as unordered, then this column is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="a22fb-137"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Ajoutée</span><span class="sxs-lookup"><span data-stu-id="a22fb-137"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="a22fb-138">Chaîne de valeur associée à cet élément.</span><span class="sxs-lookup"><span data-stu-id="a22fb-138">The value string associated with this item.</span></span> <span data-ttu-id="a22fb-139">La sélection de la ligne affecte cette valeur à la propriété associée.</span><span class="sxs-lookup"><span data-stu-id="a22fb-139">Selecting the line sets the associated property to this value.</span></span>

</dd> <dt>

<span data-ttu-id="a22fb-140"><span id="Text"></span><span id="text"></span><span id="TEXT"></span>Financière</span><span class="sxs-lookup"><span data-stu-id="a22fb-140"><span id="Text"></span><span id="text"></span><span id="TEXT"></span>Text</span></span>
</dt> <dd>

<span data-ttu-id="a22fb-141">Texte visible localisable à assigner à l’élément.</span><span class="sxs-lookup"><span data-stu-id="a22fb-141">The localizable, visible text to be assigned to the item.</span></span> <span data-ttu-id="a22fb-142">Si cette entrée ou la colonne entière est manquante, le texte prend par défaut l’entrée correspondante dans la valeur.</span><span class="sxs-lookup"><span data-stu-id="a22fb-142">If this entry or the entire column is missing, the text defaults to the corresponding entry in Value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a22fb-143">Notes</span><span class="sxs-lookup"><span data-stu-id="a22fb-143">Remarks</span></span>

<span data-ttu-id="a22fb-144">Le contenu des champs de valeur et de texte est mis en forme par la fonction [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) lorsque le contrôle est créé. par conséquent, ils peuvent contenir toute expression que la fonction **MsiFormatRecord** peut interpréter.</span><span class="sxs-lookup"><span data-stu-id="a22fb-144">The contents of the Value and Text fields are formatted by the [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) function when the control is created, therefore they can contain any expression that the **MsiFormatRecord** function can interpret.</span></span> <span data-ttu-id="a22fb-145">La mise en forme se produit uniquement lorsque le contrôle est créé et qu’elle n’est pas mise à jour si une propriété impliquée dans l’expression est modifiée pendant la durée de vie du contrôle.</span><span class="sxs-lookup"><span data-stu-id="a22fb-145">The formatting occurs only when the control is created, and it is not updated if a property involved in the expression is modified during the life of the control.</span></span>

## <a name="validation"></a><span data-ttu-id="a22fb-146">Validation</span><span class="sxs-lookup"><span data-stu-id="a22fb-146">Validation</span></span>

<dl>

[<span data-ttu-id="a22fb-147">ICE03</span><span class="sxs-lookup"><span data-stu-id="a22fb-147">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="a22fb-148">ICE06</span><span class="sxs-lookup"><span data-stu-id="a22fb-148">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="a22fb-149">ICE17</span><span class="sxs-lookup"><span data-stu-id="a22fb-149">ICE17</span></span>](ice17.md)  
[<span data-ttu-id="a22fb-150">ICE20</span><span class="sxs-lookup"><span data-stu-id="a22fb-150">ICE20</span></span>](ice20.md)  
[<span data-ttu-id="a22fb-151">ICE46</span><span class="sxs-lookup"><span data-stu-id="a22fb-151">ICE46</span></span>](ice46.md)  
</dl>

 

 



