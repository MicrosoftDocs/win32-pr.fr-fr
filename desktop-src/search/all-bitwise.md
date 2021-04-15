---
description: TOUT au niveau du bit et certains mots clés au niveau du bit sont utilisés pour tester les bits dans un type intégral.
ms.assetid: 649f763f-45aa-4086-9e7f-b8934b5bd22c
title: Toutes les opérations de bits and au niveau du bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 709db4829f5b620bcb14e0b4261fac7e7d9a6f95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525473"
---
# <a name="all-bitwise-and-some-bitwise"></a><span data-ttu-id="1e43d-103">Toutes les opérations de bits and au niveau du bit</span><span class="sxs-lookup"><span data-stu-id="1e43d-103">ALL BITWISE and SOME BITWISE</span></span>

<span data-ttu-id="1e43d-104">**Tout au niveau du bit** et certains mots clés au niveau du **bit** sont utilisés pour tester les bits dans un type intégral.</span><span class="sxs-lookup"><span data-stu-id="1e43d-104">The **ALL BITWISE** and **SOME BITWISE** keywords are used for testing the bits in an integral type.</span></span> <span data-ttu-id="1e43d-105">Si tous les bits définis dans une propriété correspondent au masque, **tout le bit** est true.</span><span class="sxs-lookup"><span data-stu-id="1e43d-105">If all of the set bits in a property match the mask, **ALL BITWISE** is true.</span></span> <span data-ttu-id="1e43d-106">Si au moins l’un des bits définis dans une propriété correspond au masque, **une partie du bit** est vraie.</span><span class="sxs-lookup"><span data-stu-id="1e43d-106">If at least one of the set bits in a property matches the mask, **SOME BITWISE** is true.</span></span>

<span data-ttu-id="1e43d-107">Les opérateurs peuvent être appliqués aux propriétés scalaires (à valeur unique) et aux propriétés vectorielles (valeurs multiples).</span><span class="sxs-lookup"><span data-stu-id="1e43d-107">Operators can be applied to both scalar (single-value) properties and vector (multiple-value) properties.</span></span> <span data-ttu-id="1e43d-108">L’exemple de code suivant montre comment tester des valeurs de propriété avec l' **opération de bits** and au **niveau du bit**.</span><span class="sxs-lookup"><span data-stu-id="1e43d-108">The following code example shows how to test property values with **ALL BITWISE** and **SOME BITWISE**.</span></span>


```sql
ALL array ALL BITWISE [values?]
ALL array SOME BITWISE [values?]
            
```



## <a name="comparison-operators"></a><span data-ttu-id="1e43d-109">Opérateurs de comparaison</span><span class="sxs-lookup"><span data-stu-id="1e43d-109">Comparison Operators</span></span>

<span data-ttu-id="1e43d-110">Les opérateurs de comparaison pris en charge pour les tests au niveau du bit sont répertoriés dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="1e43d-110">The supported comparison operators for BITWISE tests are listed in the following table.</span></span>



| <span data-ttu-id="1e43d-111">Opérateur de comparaison</span><span class="sxs-lookup"><span data-stu-id="1e43d-111">Comparison operator</span></span> | <span data-ttu-id="1e43d-112">Description</span><span class="sxs-lookup"><span data-stu-id="1e43d-112">Description</span></span>  |
|---------------------|--------------|
| =                   | <span data-ttu-id="1e43d-113">Égal à</span><span class="sxs-lookup"><span data-stu-id="1e43d-113">Equal to</span></span>     |
| <span data-ttu-id="1e43d-114">! = ou <></span><span class="sxs-lookup"><span data-stu-id="1e43d-114">!= or <></span></span>      | <span data-ttu-id="1e43d-115">Différent de</span><span class="sxs-lookup"><span data-stu-id="1e43d-115">Not equal to</span></span> |



 

<span data-ttu-id="1e43d-116">La logique des tests au niveau du bit est indiquée dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="1e43d-116">The logic of BITWISE tests is listed in the following table.</span></span>



| <span data-ttu-id="1e43d-117">Test de bits et opérateur de comparaison</span><span class="sxs-lookup"><span data-stu-id="1e43d-117">BITWISE test and comparison operator</span></span> | <span data-ttu-id="1e43d-118">Logique</span><span class="sxs-lookup"><span data-stu-id="1e43d-118">Logic</span></span>                   |
|--------------------------------------|-------------------------|
| <span data-ttu-id="1e43d-119">= TOUTES LES OPÉRATIONS AU NIVEAU DU BIT</span><span class="sxs-lookup"><span data-stu-id="1e43d-119">= ALL BITWISE</span></span>                        | <span data-ttu-id="1e43d-120">Propriété & Masque = Masque</span><span class="sxs-lookup"><span data-stu-id="1e43d-120">Property & Mask = Mask</span></span>  |
| <span data-ttu-id="1e43d-121">= UN OPÉRATEUR DE BITS</span><span class="sxs-lookup"><span data-stu-id="1e43d-121">= SOME BITWISE</span></span>                       | <span data-ttu-id="1e43d-122">Masque de & de propriété ! = 0</span><span class="sxs-lookup"><span data-stu-id="1e43d-122">Property & Mask != 0</span></span>    |
| <span data-ttu-id="1e43d-123"><> TOUTES LES OPÉRATIONS AU NIVEAU DU BIT</span><span class="sxs-lookup"><span data-stu-id="1e43d-123"><> ALL BITWISE</span></span>                 | <span data-ttu-id="1e43d-124">Masque de & de propriété ! = masque</span><span class="sxs-lookup"><span data-stu-id="1e43d-124">Property & Mask != Mask</span></span> |
| <span data-ttu-id="1e43d-125"><> UN OPÉRATEUR DE BITS</span><span class="sxs-lookup"><span data-stu-id="1e43d-125"><> SOME BITWISE</span></span>                | <span data-ttu-id="1e43d-126">Propriété & masque = 0</span><span class="sxs-lookup"><span data-stu-id="1e43d-126">Property & Mask = 0</span></span>     |



 

<span data-ttu-id="1e43d-127">La table de vérité suivante utilise des exemples de valeurs binaires et hexadécimales pour expliquer la logique des tests au niveau du bit.</span><span class="sxs-lookup"><span data-stu-id="1e43d-127">The following truth table uses example binary and hex values to demonstate the logic of BITWISE tests.</span></span>



| <span data-ttu-id="1e43d-128">Propriété en binaire (hex)</span><span class="sxs-lookup"><span data-stu-id="1e43d-128">Property in binary (hex)</span></span> | <span data-ttu-id="1e43d-129">Masque en binaire (hex)</span><span class="sxs-lookup"><span data-stu-id="1e43d-129">Mask in binary (hex)</span></span> | <span data-ttu-id="1e43d-130">Propriété & masque = Binary (hex)</span><span class="sxs-lookup"><span data-stu-id="1e43d-130">Property & Mask = binary (hex)</span></span> | <span data-ttu-id="1e43d-131">= UN OPÉRATEUR DE BITS</span><span class="sxs-lookup"><span data-stu-id="1e43d-131">= SOME BITWISE</span></span> | <span data-ttu-id="1e43d-132">= TOUTES LES OPÉRATIONS AU NIVEAU DU BIT</span><span class="sxs-lookup"><span data-stu-id="1e43d-132">= ALL BITWISE</span></span> |
|--------------------------|----------------------|--------------------------------|----------------|---------------|
| <span data-ttu-id="1e43d-133">0001 (0x1)</span><span class="sxs-lookup"><span data-stu-id="1e43d-133">0001 (0x1)</span></span>               | <span data-ttu-id="1e43d-134">0001 (0x1)</span><span class="sxs-lookup"><span data-stu-id="1e43d-134">0001 (0x1)</span></span>           | <span data-ttu-id="1e43d-135">0001 (0x1)</span><span class="sxs-lookup"><span data-stu-id="1e43d-135">0001 (0x1)</span></span>                     | <span data-ttu-id="1e43d-136">True</span><span class="sxs-lookup"><span data-stu-id="1e43d-136">True</span></span>           | <span data-ttu-id="1e43d-137">True</span><span class="sxs-lookup"><span data-stu-id="1e43d-137">True</span></span>          |
| <span data-ttu-id="1e43d-138">0001 (0x1)</span><span class="sxs-lookup"><span data-stu-id="1e43d-138">0001 (0x1)</span></span>               | <span data-ttu-id="1e43d-139">0011 (0x3)</span><span class="sxs-lookup"><span data-stu-id="1e43d-139">0011 (0x3)</span></span>           | <span data-ttu-id="1e43d-140">0001 (0x1)</span><span class="sxs-lookup"><span data-stu-id="1e43d-140">0001 (0x1)</span></span>                     | <span data-ttu-id="1e43d-141">Vrai</span><span class="sxs-lookup"><span data-stu-id="1e43d-141">True</span></span>           | <span data-ttu-id="1e43d-142">Faux</span><span class="sxs-lookup"><span data-stu-id="1e43d-142">False</span></span>         |
| <span data-ttu-id="1e43d-143">0011 (0x3)</span><span class="sxs-lookup"><span data-stu-id="1e43d-143">0011 (0x3)</span></span>               | <span data-ttu-id="1e43d-144">0001 (0x1)</span><span class="sxs-lookup"><span data-stu-id="1e43d-144">0001 (0x1)</span></span>           | <span data-ttu-id="1e43d-145">0001 (0x1)</span><span class="sxs-lookup"><span data-stu-id="1e43d-145">0001 (0x1)</span></span>                     | <span data-ttu-id="1e43d-146">True</span><span class="sxs-lookup"><span data-stu-id="1e43d-146">True</span></span>           | <span data-ttu-id="1e43d-147">True</span><span class="sxs-lookup"><span data-stu-id="1e43d-147">True</span></span>          |
| <span data-ttu-id="1e43d-148">0010 (0X2)</span><span class="sxs-lookup"><span data-stu-id="1e43d-148">0010 (0x2)</span></span>               | <span data-ttu-id="1e43d-149">0001 (0x1)</span><span class="sxs-lookup"><span data-stu-id="1e43d-149">0001 (0x1)</span></span>           | <span data-ttu-id="1e43d-150">0000 (0x0)</span><span class="sxs-lookup"><span data-stu-id="1e43d-150">0000 (0x0)</span></span>                     | <span data-ttu-id="1e43d-151">Faux</span><span class="sxs-lookup"><span data-stu-id="1e43d-151">False</span></span>          | <span data-ttu-id="1e43d-152">False</span><span class="sxs-lookup"><span data-stu-id="1e43d-152">False</span></span>         |
| <span data-ttu-id="1e43d-153">11110000 (0xF0)</span><span class="sxs-lookup"><span data-stu-id="1e43d-153">11110000 (0xF0)</span></span>          | <span data-ttu-id="1e43d-154">00000011 (0x03)</span><span class="sxs-lookup"><span data-stu-id="1e43d-154">00000011 (0x03)</span></span>      | <span data-ttu-id="1e43d-155">00000000 (0x00)</span><span class="sxs-lookup"><span data-stu-id="1e43d-155">00000000 (0x00)</span></span>                | <span data-ttu-id="1e43d-156">Faux</span><span class="sxs-lookup"><span data-stu-id="1e43d-156">False</span></span>          | <span data-ttu-id="1e43d-157">False</span><span class="sxs-lookup"><span data-stu-id="1e43d-157">False</span></span>         |
| <span data-ttu-id="1e43d-158">11110010 (0xF2)</span><span class="sxs-lookup"><span data-stu-id="1e43d-158">11110010 (0xF2)</span></span>          | <span data-ttu-id="1e43d-159">11110010 (0xF2)</span><span class="sxs-lookup"><span data-stu-id="1e43d-159">11110010 (0xF2)</span></span>      | <span data-ttu-id="1e43d-160">11110010 (0xF2)</span><span class="sxs-lookup"><span data-stu-id="1e43d-160">11110010 (0xF2)</span></span>                | <span data-ttu-id="1e43d-161">True</span><span class="sxs-lookup"><span data-stu-id="1e43d-161">True</span></span>           | <span data-ttu-id="1e43d-162">True</span><span class="sxs-lookup"><span data-stu-id="1e43d-162">True</span></span>          |
| <span data-ttu-id="1e43d-163">11110010 (0xF2)</span><span class="sxs-lookup"><span data-stu-id="1e43d-163">11110010 (0xF2)</span></span>          | <span data-ttu-id="1e43d-164">00000011 (0x03)</span><span class="sxs-lookup"><span data-stu-id="1e43d-164">00000011 (0x03)</span></span>      | <span data-ttu-id="1e43d-165">00000010 (0x02)</span><span class="sxs-lookup"><span data-stu-id="1e43d-165">00000010 (0x02)</span></span>                | <span data-ttu-id="1e43d-166">Vrai</span><span class="sxs-lookup"><span data-stu-id="1e43d-166">True</span></span>           | <span data-ttu-id="1e43d-167">Faux</span><span class="sxs-lookup"><span data-stu-id="1e43d-167">False</span></span>         |



 

## <a name="example"></a><span data-ttu-id="1e43d-168">Exemple</span><span class="sxs-lookup"><span data-stu-id="1e43d-168">Example</span></span>

<span data-ttu-id="1e43d-169">Voici un exemple de prédicat All au **niveau du bit** .</span><span class="sxs-lookup"><span data-stu-id="1e43d-169">The following is an example of the **ALL BITWISE** predicate.</span></span>


```sql
Select system.itemnamedisplay, system.FileAttributes from SystemIndex Where System.FileAttributes <> ALL BITWISE 0x4 AND Scope = 'file:c:\bitwise'
                
```



## <a name="related-topics"></a><span data-ttu-id="1e43d-170">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1e43d-170">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="1e43d-171">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="1e43d-171">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1e43d-172">Prédicats de texte intégral</span><span class="sxs-lookup"><span data-stu-id="1e43d-172">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="1e43d-173">Prédicats de texte non intégral</span><span class="sxs-lookup"><span data-stu-id="1e43d-173">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



