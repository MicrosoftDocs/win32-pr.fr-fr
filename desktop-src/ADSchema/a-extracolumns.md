---
title: Attribut Extra-Columns
description: Il s’agit d’un attribut à valeurs multiples dont les valeurs se composent d’un tuple de 5 (nom d’attribut), (titre de colonne), (visibilité par défaut (0, 1)), (largeur de colonne (\ 8211 ; 1 pour la largeur automatique)), 0 (réservé pour une utilisation future doit être égal à zéro).
ms.assetid: aafe4657-0295-4af2-a7d0-8c7561516e17
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Extra-Columns
- Schéma AD de l’attribut extraColumns
topic_type:
- apiref
api_name:
- Extra-Columns
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de0bc74532296c5e0f23da9635bb26df299ae60b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744380"
---
# <a name="extra-columns-attribute"></a><span data-ttu-id="b8c23-105">Attribut Extra-Columns</span><span class="sxs-lookup"><span data-stu-id="b8c23-105">Extra-Columns attribute</span></span>

<span data-ttu-id="b8c23-106">Il s’agit d’un attribut à valeurs multiples dont les valeurs se composent d’un tuple de 5 : (nom de l’attribut), (titre de colonne), (visibilité par défaut (0, 1)), (largeur de colonne (1 pour la largeur automatique), 0 (réservé à un usage futur).</span><span class="sxs-lookup"><span data-stu-id="b8c23-106">This is a multivalued attribute whose values consist of a 5 tuple: (attribute name), (column title), (default visibility (0,1)), (column width ( 1 for auto width)), 0 (reserved for future use must be zero).</span></span> <span data-ttu-id="b8c23-107">Cette valeur est utilisée par la console utilisateurs et ordinateurs Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b8c23-107">This value is used by the AD Users and Computers console.</span></span>



| <span data-ttu-id="b8c23-108">Entrée</span><span class="sxs-lookup"><span data-stu-id="b8c23-108">Entry</span></span> | <span data-ttu-id="b8c23-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="b8c23-109">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8c23-110">CN</span><span class="sxs-lookup"><span data-stu-id="b8c23-110">CN</span></span>                | <span data-ttu-id="b8c23-111">Extra-Columns</span><span class="sxs-lookup"><span data-stu-id="b8c23-111">Extra-Columns</span></span>                                                                                                                                                        |
| <span data-ttu-id="b8c23-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="b8c23-112">Ldap-Display-Name</span></span> | <span data-ttu-id="b8c23-113">extraColumns</span><span class="sxs-lookup"><span data-stu-id="b8c23-113">extraColumns</span></span>                                                                                                                                                         |
| <span data-ttu-id="b8c23-114">Taille</span><span class="sxs-lookup"><span data-stu-id="b8c23-114">Size</span></span>              | <span data-ttu-id="b8c23-115">Chaque valeur correspond à la taille de la chaîne des 5 tuples ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="b8c23-115">Each value would be the size of the string of the 5 tuple above.</span></span> <span data-ttu-id="b8c23-116">Par défaut, il y aura 22 valeurs sur l’objet d’affichage par défaut dans le conteneur DisplaySpecifier.</span><span class="sxs-lookup"><span data-stu-id="b8c23-116">By default there will be 22 values on the default-Display object in the DisplaySpecifier container.</span></span> |
| <span data-ttu-id="b8c23-117">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="b8c23-117">Update Privilege</span></span>  | <span data-ttu-id="b8c23-118">Administrateur de domaine</span><span class="sxs-lookup"><span data-stu-id="b8c23-118">Domain administrator</span></span>                                                                                                                                                 |
| <span data-ttu-id="b8c23-119">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="b8c23-119">Update Frequency</span></span>  | <span data-ttu-id="b8c23-120">Ce sera uniquement mis à jour si un service comme Exchange est installé.</span><span class="sxs-lookup"><span data-stu-id="b8c23-120">This will only be updated if a service like Exchange is installed.</span></span>                                                                                                   |
| <span data-ttu-id="b8c23-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b8c23-121">Attribute-Id</span></span>      | <span data-ttu-id="b8c23-122">1.2.840.113556.1.4.1687</span><span class="sxs-lookup"><span data-stu-id="b8c23-122">1.2.840.113556.1.4.1687</span></span>                                                                                                                                              |
| <span data-ttu-id="b8c23-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b8c23-123">System-Id-Guid</span></span>    | <span data-ttu-id="b8c23-124">d24e2846-1dd9-4bcf-99d7-a6227cc86da7</span><span class="sxs-lookup"><span data-stu-id="b8c23-124">d24e2846-1dd9-4bcf-99d7-a6227cc86da7</span></span>                                                                                                                                 |
| <span data-ttu-id="b8c23-125">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b8c23-125">Syntax</span></span>            | [<span data-ttu-id="b8c23-126">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="b8c23-126">**String(Unicode)**</span></span>](s-string-unicode.md)                                                                                                                          |



## <a name="implementations"></a><span data-ttu-id="b8c23-127">Implémentations</span><span class="sxs-lookup"><span data-stu-id="b8c23-127">Implementations</span></span>

-   [<span data-ttu-id="b8c23-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b8c23-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b8c23-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b8c23-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b8c23-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b8c23-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b8c23-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b8c23-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b8c23-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b8c23-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="b8c23-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b8c23-133">Windows Server 2003</span></span>



| <span data-ttu-id="b8c23-134">Entrée</span><span class="sxs-lookup"><span data-stu-id="b8c23-134">Entry</span></span> | <span data-ttu-id="b8c23-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="b8c23-135">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="b8c23-136">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b8c23-136">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="b8c23-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8c23-137">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="b8c23-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8c23-138">System-Only</span></span>            | <span data-ttu-id="b8c23-139">Faux</span><span class="sxs-lookup"><span data-stu-id="b8c23-139">False</span></span>                                                      |
| <span data-ttu-id="b8c23-140">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b8c23-140">Is-Single-Valued</span></span>       | <span data-ttu-id="b8c23-141">Faux</span><span class="sxs-lookup"><span data-stu-id="b8c23-141">False</span></span>                                                      |
| <span data-ttu-id="b8c23-142">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b8c23-142">Is Indexed</span></span>             | <span data-ttu-id="b8c23-143">Faux</span><span class="sxs-lookup"><span data-stu-id="b8c23-143">False</span></span>                                                      |
| <span data-ttu-id="b8c23-144">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b8c23-144">In Global Catalog</span></span>      | <span data-ttu-id="b8c23-145">Faux</span><span class="sxs-lookup"><span data-stu-id="b8c23-145">False</span></span>                                                      |
| <span data-ttu-id="b8c23-146">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b8c23-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8c23-147">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b8c23-147">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="b8c23-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8c23-148">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="b8c23-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8c23-149">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="b8c23-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8c23-150">Search-Flags</span></span>           | <span data-ttu-id="b8c23-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b8c23-151">0x00000000</span></span>                                                 |
| <span data-ttu-id="b8c23-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8c23-152">System-Flags</span></span>           | <span data-ttu-id="b8c23-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b8c23-153">0x00000010</span></span>                                                 |
| <span data-ttu-id="b8c23-154">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b8c23-154">Classes used in</span></span>        | [<span data-ttu-id="b8c23-155">**Display-specifier**</span><span class="sxs-lookup"><span data-stu-id="b8c23-155">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b8c23-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b8c23-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b8c23-157">Entrée</span><span class="sxs-lookup"><span data-stu-id="b8c23-157">Entry</span></span> | <span data-ttu-id="b8c23-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="b8c23-158">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="b8c23-159">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b8c23-159">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="b8c23-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8c23-160">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="b8c23-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8c23-161">System-Only</span></span>            | <span data-ttu-id="b8c23-162">Faux</span><span class="sxs-lookup"><span data-stu-id="b8c23-162">False</span></span>                                                      |
| <span data-ttu-id="b8c23-163">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b8c23-163">Is-Single-Valued</span></span>       | <span data-ttu-id="b8c23-164">Faux</span><span class="sxs-lookup"><span data-stu-id="b8c23-164">False</span></span>                                                      |
| <span data-ttu-id="b8c23-165">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b8c23-165">Is Indexed</span></span>             | <span data-ttu-id="b8c23-166">Faux</span><span class="sxs-lookup"><span data-stu-id="b8c23-166">False</span></span>                                                      |
| <span data-ttu-id="b8c23-167">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b8c23-167">In Global Catalog</span></span>      | <span data-ttu-id="b8c23-168">Faux</span><span class="sxs-lookup"><span data-stu-id="b8c23-168">False</span></span>                                                      |
| <span data-ttu-id="b8c23-169">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b8c23-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8c23-170">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b8c23-170">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="b8c23-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8c23-171">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="b8c23-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8c23-172">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="b8c23-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8c23-173">Search-Flags</span></span>           | <span data-ttu-id="b8c23-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b8c23-174">0x00000000</span></span>                                                 |
| <span data-ttu-id="b8c23-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8c23-175">System-Flags</span></span>           | <span data-ttu-id="b8c23-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b8c23-176">0x00000010</span></span>                                                 |
| <span data-ttu-id="b8c23-177">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b8c23-177">Classes used in</span></span>        | [<span data-ttu-id="b8c23-178">**Display-specifier**</span><span class="sxs-lookup"><span data-stu-id="b8c23-178">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b8c23-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b8c23-179">Windows Server 2008</span></span>



| <span data-ttu-id="b8c23-180">Entrée</span><span class="sxs-lookup"><span data-stu-id="b8c23-180">Entry</span></span> | <span data-ttu-id="b8c23-181">Valeur</span><span class="sxs-lookup"><span data-stu-id="b8c23-181">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="b8c23-182">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b8c23-182">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="b8c23-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8c23-183">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="b8c23-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8c23-184">System-Only</span></span>            | <span data-ttu-id="b8c23-185">Faux</span><span class="sxs-lookup"><span data-stu-id="b8c23-185">False</span></span>                                                      |
| <span data-ttu-id="b8c23-186">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b8c23-186">Is-Single-Valued</span></span>       | <span data-ttu-id="b8c23-187">Faux</span><span class="sxs-lookup"><span data-stu-id="b8c23-187">False</span></span>                                                      |
| <span data-ttu-id="b8c23-188">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b8c23-188">Is Indexed</span></span>             | <span data-ttu-id="b8c23-189">Faux</span><span class="sxs-lookup"><span data-stu-id="b8c23-189">False</span></span>                                                      |
| <span data-ttu-id="b8c23-190">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b8c23-190">In Global Catalog</span></span>      | <span data-ttu-id="b8c23-191">Faux</span><span class="sxs-lookup"><span data-stu-id="b8c23-191">False</span></span>                                                      |
| <span data-ttu-id="b8c23-192">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b8c23-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8c23-193">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b8c23-193">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="b8c23-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8c23-194">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="b8c23-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8c23-195">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="b8c23-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8c23-196">Search-Flags</span></span>           | <span data-ttu-id="b8c23-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b8c23-197">0x00000000</span></span>                                                 |
| <span data-ttu-id="b8c23-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8c23-198">System-Flags</span></span>           | <span data-ttu-id="b8c23-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b8c23-199">0x00000010</span></span>                                                 |
| <span data-ttu-id="b8c23-200">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b8c23-200">Classes used in</span></span>        | [<span data-ttu-id="b8c23-201">**Display-specifier**</span><span class="sxs-lookup"><span data-stu-id="b8c23-201">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b8c23-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b8c23-202">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b8c23-203">Entrée</span><span class="sxs-lookup"><span data-stu-id="b8c23-203">Entry</span></span> | <span data-ttu-id="b8c23-204">Valeur</span><span class="sxs-lookup"><span data-stu-id="b8c23-204">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="b8c23-205">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b8c23-205">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="b8c23-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8c23-206">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="b8c23-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8c23-207">System-Only</span></span>            | <span data-ttu-id="b8c23-208">Faux</span><span class="sxs-lookup"><span data-stu-id="b8c23-208">False</span></span>                                                      |
| <span data-ttu-id="b8c23-209">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b8c23-209">Is-Single-Valued</span></span>       | <span data-ttu-id="b8c23-210">Faux</span><span class="sxs-lookup"><span data-stu-id="b8c23-210">False</span></span>                                                      |
| <span data-ttu-id="b8c23-211">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b8c23-211">Is Indexed</span></span>             | <span data-ttu-id="b8c23-212">Faux</span><span class="sxs-lookup"><span data-stu-id="b8c23-212">False</span></span>                                                      |
| <span data-ttu-id="b8c23-213">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b8c23-213">In Global Catalog</span></span>      | <span data-ttu-id="b8c23-214">Faux</span><span class="sxs-lookup"><span data-stu-id="b8c23-214">False</span></span>                                                      |
| <span data-ttu-id="b8c23-215">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b8c23-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8c23-216">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b8c23-216">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="b8c23-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8c23-217">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="b8c23-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8c23-218">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="b8c23-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8c23-219">Search-Flags</span></span>           | <span data-ttu-id="b8c23-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b8c23-220">0x00000000</span></span>                                                 |
| <span data-ttu-id="b8c23-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8c23-221">System-Flags</span></span>           | <span data-ttu-id="b8c23-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b8c23-222">0x00000010</span></span>                                                 |
| <span data-ttu-id="b8c23-223">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b8c23-223">Classes used in</span></span>        | [<span data-ttu-id="b8c23-224">**Display-specifier**</span><span class="sxs-lookup"><span data-stu-id="b8c23-224">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b8c23-225">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b8c23-225">Windows Server 2012</span></span>



| <span data-ttu-id="b8c23-226">Entrée</span><span class="sxs-lookup"><span data-stu-id="b8c23-226">Entry</span></span> | <span data-ttu-id="b8c23-227">Valeur</span><span class="sxs-lookup"><span data-stu-id="b8c23-227">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="b8c23-228">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b8c23-228">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="b8c23-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8c23-229">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="b8c23-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8c23-230">System-Only</span></span>            | <span data-ttu-id="b8c23-231">Faux</span><span class="sxs-lookup"><span data-stu-id="b8c23-231">False</span></span>                                                      |
| <span data-ttu-id="b8c23-232">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b8c23-232">Is-Single-Valued</span></span>       | <span data-ttu-id="b8c23-233">Faux</span><span class="sxs-lookup"><span data-stu-id="b8c23-233">False</span></span>                                                      |
| <span data-ttu-id="b8c23-234">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b8c23-234">Is Indexed</span></span>             | <span data-ttu-id="b8c23-235">Faux</span><span class="sxs-lookup"><span data-stu-id="b8c23-235">False</span></span>                                                      |
| <span data-ttu-id="b8c23-236">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b8c23-236">In Global Catalog</span></span>      | <span data-ttu-id="b8c23-237">Faux</span><span class="sxs-lookup"><span data-stu-id="b8c23-237">False</span></span>                                                      |
| <span data-ttu-id="b8c23-238">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b8c23-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8c23-239">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b8c23-239">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="b8c23-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8c23-240">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="b8c23-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8c23-241">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="b8c23-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8c23-242">Search-Flags</span></span>           | <span data-ttu-id="b8c23-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b8c23-243">0x00000000</span></span>                                                 |
| <span data-ttu-id="b8c23-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8c23-244">System-Flags</span></span>           | <span data-ttu-id="b8c23-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b8c23-245">0x00000010</span></span>                                                 |
| <span data-ttu-id="b8c23-246">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b8c23-246">Classes used in</span></span>        | [<span data-ttu-id="b8c23-247">**Display-specifier**</span><span class="sxs-lookup"><span data-stu-id="b8c23-247">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



 

 





