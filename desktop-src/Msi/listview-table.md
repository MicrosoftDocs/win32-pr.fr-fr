---
description: Les lignes d’un ListView ne sont pas traitées comme des contrôles individuels, mais elles font partie d’un ListView qui fonctionne comme un contrôle. Le tableau ListView définit les valeurs de tous les ListView.
ms.assetid: 0da4eab9-cabc-4bcc-8267-4aa1cd79e78b
title: Tableau ListView
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0e7296db9f71a7c40550fdcaab18d8f0d0f41f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518431"
---
# <a name="listview-table"></a><span data-ttu-id="b9f77-104">Tableau ListView</span><span class="sxs-lookup"><span data-stu-id="b9f77-104">ListView Table</span></span>

<span data-ttu-id="b9f77-105">Les lignes d’un ListView ne sont pas traitées comme des contrôles individuels, mais elles font partie d’un ListView qui fonctionne comme un contrôle.</span><span class="sxs-lookup"><span data-stu-id="b9f77-105">The lines of a listview are not treated as individual controls, but they are part of a listview that functions as a control.</span></span> <span data-ttu-id="b9f77-106">Le tableau ListView définit les valeurs de tous les ListView.</span><span class="sxs-lookup"><span data-stu-id="b9f77-106">The ListView table defines the values for all listviews.</span></span>

<span data-ttu-id="b9f77-107">La table ListView contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="b9f77-107">The ListView table has the following columns.</span></span>



| <span data-ttu-id="b9f77-108">Colonne</span><span class="sxs-lookup"><span data-stu-id="b9f77-108">Column</span></span>   | <span data-ttu-id="b9f77-109">Type</span><span class="sxs-lookup"><span data-stu-id="b9f77-109">Type</span></span>                         | <span data-ttu-id="b9f77-110">Clé</span><span class="sxs-lookup"><span data-stu-id="b9f77-110">Key</span></span> | <span data-ttu-id="b9f77-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="b9f77-111">Nullable</span></span> |
|----------|------------------------------|-----|----------|
| <span data-ttu-id="b9f77-112">Propriété</span><span class="sxs-lookup"><span data-stu-id="b9f77-112">Property</span></span> | [<span data-ttu-id="b9f77-113">Identificateur</span><span class="sxs-lookup"><span data-stu-id="b9f77-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="b9f77-114">O</span><span class="sxs-lookup"><span data-stu-id="b9f77-114">Y</span></span>   | <span data-ttu-id="b9f77-115">N</span><span class="sxs-lookup"><span data-stu-id="b9f77-115">N</span></span>        |
| <span data-ttu-id="b9f77-116">Commande</span><span class="sxs-lookup"><span data-stu-id="b9f77-116">Order</span></span>    | [<span data-ttu-id="b9f77-117">Integer</span><span class="sxs-lookup"><span data-stu-id="b9f77-117">Integer</span></span>](integer.md)       | <span data-ttu-id="b9f77-118">O</span><span class="sxs-lookup"><span data-stu-id="b9f77-118">Y</span></span>   | <span data-ttu-id="b9f77-119">N</span><span class="sxs-lookup"><span data-stu-id="b9f77-119">N</span></span>        |
| <span data-ttu-id="b9f77-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="b9f77-120">Value</span></span>    | [<span data-ttu-id="b9f77-121">Correct</span><span class="sxs-lookup"><span data-stu-id="b9f77-121">Formatted</span></span>](formatted.md)   | <span data-ttu-id="b9f77-122">N</span><span class="sxs-lookup"><span data-stu-id="b9f77-122">N</span></span>   | <span data-ttu-id="b9f77-123">N</span><span class="sxs-lookup"><span data-stu-id="b9f77-123">N</span></span>        |
| <span data-ttu-id="b9f77-124">Texte</span><span class="sxs-lookup"><span data-stu-id="b9f77-124">Text</span></span>     | [<span data-ttu-id="b9f77-125">Correct</span><span class="sxs-lookup"><span data-stu-id="b9f77-125">Formatted</span></span>](formatted.md)   | <span data-ttu-id="b9f77-126">N</span><span class="sxs-lookup"><span data-stu-id="b9f77-126">N</span></span>   | <span data-ttu-id="b9f77-127">O</span><span class="sxs-lookup"><span data-stu-id="b9f77-127">Y</span></span>        |
| <span data-ttu-id="b9f77-128">Binary\_</span><span class="sxs-lookup"><span data-stu-id="b9f77-128">Binary\_</span></span> | [<span data-ttu-id="b9f77-129">Identificateur</span><span class="sxs-lookup"><span data-stu-id="b9f77-129">Identifier</span></span>](identifier.md) | <span data-ttu-id="b9f77-130">N</span><span class="sxs-lookup"><span data-stu-id="b9f77-130">N</span></span>   | <span data-ttu-id="b9f77-131">O</span><span class="sxs-lookup"><span data-stu-id="b9f77-131">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="b9f77-132">Colonnes</span><span class="sxs-lookup"><span data-stu-id="b9f77-132">Columns</span></span>

<dl> <dt>

<span data-ttu-id="b9f77-133"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Propriété</span><span class="sxs-lookup"><span data-stu-id="b9f77-133"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property</span></span>
</dt> <dd>

<span data-ttu-id="b9f77-134">Propriété nommée à être liée à cet élément.</span><span class="sxs-lookup"><span data-stu-id="b9f77-134">A named property to be tied to this item.</span></span> <span data-ttu-id="b9f77-135">Tous les éléments liés à la même propriété deviennent partie intégrante du même ListView.</span><span class="sxs-lookup"><span data-stu-id="b9f77-135">All the items tied to the same property become part of the same listview.</span></span>

</dd> <dt>

<span data-ttu-id="b9f77-136"><span id="Order"></span><span id="order"></span><span id="ORDER"></span>Ordre</span><span class="sxs-lookup"><span data-stu-id="b9f77-136"><span id="Order"></span><span id="order"></span><span id="ORDER"></span>Order</span></span>
</dt> <dd>

<span data-ttu-id="b9f77-137">Entier positif utilisé pour déterminer l’ordre des éléments qui s’affichent dans une liste ListView unique.</span><span class="sxs-lookup"><span data-stu-id="b9f77-137">A positive integer used to determine the ordering of the items that appear in a single listview list.</span></span> <span data-ttu-id="b9f77-138">Il n’est pas nécessaire que les entiers soient consécutifs.</span><span class="sxs-lookup"><span data-stu-id="b9f77-138">The integers do not have to be consecutive.</span></span> <span data-ttu-id="b9f77-139">Si un ListView est défini comme étant ordonné, tous les éléments doivent avoir une valeur de classement.</span><span class="sxs-lookup"><span data-stu-id="b9f77-139">If a listview is defined as ordered, then all the items should have an Ordering value.</span></span> <span data-ttu-id="b9f77-140">Si le ListView est défini comme non ordonné, cette colonne est ignorée.</span><span class="sxs-lookup"><span data-stu-id="b9f77-140">If the listview is defined as unordered, then this column is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="b9f77-141"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Ajoutée</span><span class="sxs-lookup"><span data-stu-id="b9f77-141"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="b9f77-142">Chaîne de valeur associée à cet élément.</span><span class="sxs-lookup"><span data-stu-id="b9f77-142">The value string associated with this item.</span></span> <span data-ttu-id="b9f77-143">La sélection de la ligne affecte cette valeur à la propriété associée.</span><span class="sxs-lookup"><span data-stu-id="b9f77-143">Selecting the line sets the associated property to this value.</span></span>

</dd> <dt>

<span data-ttu-id="b9f77-144"><span id="Text"></span><span id="text"></span><span id="TEXT"></span>Financière</span><span class="sxs-lookup"><span data-stu-id="b9f77-144"><span id="Text"></span><span id="text"></span><span id="TEXT"></span>Text</span></span>
</dt> <dd>

<span data-ttu-id="b9f77-145">Texte visible et localisable à assigner à l’élément.</span><span class="sxs-lookup"><span data-stu-id="b9f77-145">The visible, localizable text to be assigned to the item.</span></span> <span data-ttu-id="b9f77-146">Si cette entrée ou la colonne entière est manquante, le texte prend par défaut l’entrée correspondante dans la valeur.</span><span class="sxs-lookup"><span data-stu-id="b9f77-146">If this entry or the entire column is missing, then the text defaults to the corresponding entry in Value.</span></span>

</dd> <dt>

<span data-ttu-id="b9f77-147"><span id="Binary_"></span><span id="binary_"></span><span id="BINARY_"></span>Binaire2\_</span><span class="sxs-lookup"><span data-stu-id="b9f77-147"><span id="Binary_"></span><span id="binary_"></span><span id="BINARY_"></span>Binary\_</span></span>
</dt> <dd>

<span data-ttu-id="b9f77-148">Données de l’image de l’icône.</span><span class="sxs-lookup"><span data-stu-id="b9f77-148">The image data for the icon.</span></span> <span data-ttu-id="b9f77-149">Il s’agit d’une clé étrangère de la [table binaire](binary-table.md).</span><span class="sxs-lookup"><span data-stu-id="b9f77-149">This is a foreign key to the [Binary table](binary-table.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b9f77-150">Notes</span><span class="sxs-lookup"><span data-stu-id="b9f77-150">Remarks</span></span>

<span data-ttu-id="b9f77-151">Le contenu des champs de valeur et de texte est mis en forme par la fonction [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) lorsque le contrôle est créé. par conséquent, ils peuvent contenir toute expression que la fonction MsiFormatRecord peut interpréter.</span><span class="sxs-lookup"><span data-stu-id="b9f77-151">The contents of the Value and Text fields are formatted by the [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) function when the control is created, therefore they can contain any expression that the MsiFormatRecord function can interpret.</span></span> <span data-ttu-id="b9f77-152">La mise en forme se produit uniquement lorsque le contrôle est créé et qu’elle n’est pas mise à jour si une propriété impliquée dans l’expression est modifiée pendant la durée de vie du contrôle.</span><span class="sxs-lookup"><span data-stu-id="b9f77-152">The formatting occurs only when the control is created, and it is not updated if a property involved in the expression is modified during the life of the control.</span></span>

## <a name="validation"></a><span data-ttu-id="b9f77-153">Validation</span><span class="sxs-lookup"><span data-stu-id="b9f77-153">Validation</span></span>

<dl>

[<span data-ttu-id="b9f77-154">ICE03</span><span class="sxs-lookup"><span data-stu-id="b9f77-154">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="b9f77-155">ICE06</span><span class="sxs-lookup"><span data-stu-id="b9f77-155">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="b9f77-156">ICE17</span><span class="sxs-lookup"><span data-stu-id="b9f77-156">ICE17</span></span>](ice17.md)  
[<span data-ttu-id="b9f77-157">ICE32</span><span class="sxs-lookup"><span data-stu-id="b9f77-157">ICE32</span></span>](ice32.md)  
</dl>

 

 



