---
title: Attribut admin-MultiSelect-Property-pages
description: Il s’agit d’un attribut à valeurs multiples dont les valeurs sont un nombre qui représente l’ordre dans lequel les pages sont ajoutées et le GUID d’un objet COM qui implémente des pages de propriétés à sélection multiple pour le composant logiciel enfichable utilisateurs et ordinateurs Active Directory.
ms.assetid: b2b4aafe-ac2d-44b3-80eb-910ba9852bb0
ms.tgt_platform: multiple
keywords:
- Attribut admin-Select-Property-Property-pages-schéma Active Directory
- Schéma AD de l’attribut adminMultiselectPropertyPages
topic_type:
- apiref
api_name:
- Admin-Multiselect-Property-Pages
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e653568d4f8f6653e4c7dc939c91a7d3cd8b83c6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106514879"
---
# <a name="admin-multiselect-property-pages-attribute"></a><span data-ttu-id="efe30-105">Attribut admin-MultiSelect-Property-pages</span><span class="sxs-lookup"><span data-stu-id="efe30-105">Admin-Multiselect-Property-Pages attribute</span></span>

<span data-ttu-id="efe30-106">Il s’agit d’un attribut à valeurs multiples dont les valeurs sont un nombre qui représente l’ordre dans lequel les pages sont ajoutées et le GUID d’un objet COM qui implémente des pages de propriétés à sélection multiple pour le composant logiciel enfichable utilisateurs et ordinateurs Active Directory.</span><span class="sxs-lookup"><span data-stu-id="efe30-106">This is a multivalued attribute whose values are a number that represents the order in which the pages are added and a GUID of a COM object that implements multi-select property pages for the AD Users and Computers snap-in.</span></span>



| <span data-ttu-id="efe30-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="efe30-107">Entry</span></span> | <span data-ttu-id="efe30-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="efe30-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="efe30-109">CN</span><span class="sxs-lookup"><span data-stu-id="efe30-109">CN</span></span>                | <span data-ttu-id="efe30-110">Admin-MultiSelect-Property-pages</span><span class="sxs-lookup"><span data-stu-id="efe30-110">Admin-Multiselect-Property-Pages</span></span>                                                                                                            |
| <span data-ttu-id="efe30-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="efe30-111">Ldap-Display-Name</span></span> | <span data-ttu-id="efe30-112">adminMultiselectPropertyPages</span><span class="sxs-lookup"><span data-stu-id="efe30-112">adminMultiselectPropertyPages</span></span>                                                                                                               |
| <span data-ttu-id="efe30-113">Taille</span><span class="sxs-lookup"><span data-stu-id="efe30-113">Size</span></span>              | <span data-ttu-id="efe30-114">40 octets</span><span class="sxs-lookup"><span data-stu-id="efe30-114">40 bytes</span></span>                                                                                                                                    |
| <span data-ttu-id="efe30-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="efe30-115">Update Privilege</span></span>  | <span data-ttu-id="efe30-116">Administrateur de domaine</span><span class="sxs-lookup"><span data-stu-id="efe30-116">Domain administrator</span></span>                                                                                                                        |
| <span data-ttu-id="efe30-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="efe30-117">Update Frequency</span></span>  | <span data-ttu-id="efe30-118">Cela sera uniquement mis à jour si un service comme Exchange ou Terminal Server est installé et implémente ses propres pages de propriétés à sélection multiple.</span><span class="sxs-lookup"><span data-stu-id="efe30-118">This will only be updated if a service like Exchange or Terminal Server is installed that implements their own multi-select property pages.</span></span> |
| <span data-ttu-id="efe30-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="efe30-119">Attribute-Id</span></span>      | <span data-ttu-id="efe30-120">1.2.840.113556.1.4.1690</span><span class="sxs-lookup"><span data-stu-id="efe30-120">1.2.840.113556.1.4.1690</span></span>                                                                                                                     |
| <span data-ttu-id="efe30-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="efe30-121">System-Id-Guid</span></span>    | <span data-ttu-id="efe30-122">18f9b67d-5ac6-4b3b-97db-d0a406afb7ba</span><span class="sxs-lookup"><span data-stu-id="efe30-122">18f9b67d-5ac6-4b3b-97db-d0a406afb7ba</span></span>                                                                                                        |
| <span data-ttu-id="efe30-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="efe30-123">Syntax</span></span>            | [<span data-ttu-id="efe30-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="efe30-124">**String(Unicode)**</span></span>](s-string-unicode.md)                                                                                                 |



## <a name="implementations"></a><span data-ttu-id="efe30-125">Implémentations</span><span class="sxs-lookup"><span data-stu-id="efe30-125">Implementations</span></span>

-   [<span data-ttu-id="efe30-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="efe30-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="efe30-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="efe30-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="efe30-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="efe30-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="efe30-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="efe30-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="efe30-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="efe30-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="efe30-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="efe30-131">Windows Server 2003</span></span>



| <span data-ttu-id="efe30-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="efe30-132">Entry</span></span> | <span data-ttu-id="efe30-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="efe30-133">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="efe30-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="efe30-134">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="efe30-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="efe30-135">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="efe30-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="efe30-136">System-Only</span></span>            | <span data-ttu-id="efe30-137">Faux</span><span class="sxs-lookup"><span data-stu-id="efe30-137">False</span></span>                                                      |
| <span data-ttu-id="efe30-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="efe30-138">Is-Single-Valued</span></span>       | <span data-ttu-id="efe30-139">Faux</span><span class="sxs-lookup"><span data-stu-id="efe30-139">False</span></span>                                                      |
| <span data-ttu-id="efe30-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="efe30-140">Is Indexed</span></span>             | <span data-ttu-id="efe30-141">Faux</span><span class="sxs-lookup"><span data-stu-id="efe30-141">False</span></span>                                                      |
| <span data-ttu-id="efe30-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="efe30-142">In Global Catalog</span></span>      | <span data-ttu-id="efe30-143">Faux</span><span class="sxs-lookup"><span data-stu-id="efe30-143">False</span></span>                                                      |
| <span data-ttu-id="efe30-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="efe30-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="efe30-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="efe30-145">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="efe30-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="efe30-146">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="efe30-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="efe30-147">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="efe30-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="efe30-148">Search-Flags</span></span>           | <span data-ttu-id="efe30-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="efe30-149">0x00000000</span></span>                                                 |
| <span data-ttu-id="efe30-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="efe30-150">System-Flags</span></span>           | <span data-ttu-id="efe30-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="efe30-151">0x00000010</span></span>                                                 |
| <span data-ttu-id="efe30-152">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="efe30-152">Classes used in</span></span>        | [<span data-ttu-id="efe30-153">**Display-specifier**</span><span class="sxs-lookup"><span data-stu-id="efe30-153">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="efe30-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="efe30-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="efe30-155">Entrée</span><span class="sxs-lookup"><span data-stu-id="efe30-155">Entry</span></span> | <span data-ttu-id="efe30-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="efe30-156">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="efe30-157">ID de lien</span><span class="sxs-lookup"><span data-stu-id="efe30-157">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="efe30-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="efe30-158">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="efe30-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="efe30-159">System-Only</span></span>            | <span data-ttu-id="efe30-160">Faux</span><span class="sxs-lookup"><span data-stu-id="efe30-160">False</span></span>                                                      |
| <span data-ttu-id="efe30-161">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="efe30-161">Is-Single-Valued</span></span>       | <span data-ttu-id="efe30-162">Faux</span><span class="sxs-lookup"><span data-stu-id="efe30-162">False</span></span>                                                      |
| <span data-ttu-id="efe30-163">Est indexé</span><span class="sxs-lookup"><span data-stu-id="efe30-163">Is Indexed</span></span>             | <span data-ttu-id="efe30-164">Faux</span><span class="sxs-lookup"><span data-stu-id="efe30-164">False</span></span>                                                      |
| <span data-ttu-id="efe30-165">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="efe30-165">In Global Catalog</span></span>      | <span data-ttu-id="efe30-166">Faux</span><span class="sxs-lookup"><span data-stu-id="efe30-166">False</span></span>                                                      |
| <span data-ttu-id="efe30-167">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="efe30-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="efe30-168">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="efe30-168">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="efe30-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="efe30-169">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="efe30-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="efe30-170">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="efe30-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="efe30-171">Search-Flags</span></span>           | <span data-ttu-id="efe30-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="efe30-172">0x00000000</span></span>                                                 |
| <span data-ttu-id="efe30-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="efe30-173">System-Flags</span></span>           | <span data-ttu-id="efe30-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="efe30-174">0x00000010</span></span>                                                 |
| <span data-ttu-id="efe30-175">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="efe30-175">Classes used in</span></span>        | [<span data-ttu-id="efe30-176">**Display-specifier**</span><span class="sxs-lookup"><span data-stu-id="efe30-176">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="efe30-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="efe30-177">Windows Server 2008</span></span>



| <span data-ttu-id="efe30-178">Entrée</span><span class="sxs-lookup"><span data-stu-id="efe30-178">Entry</span></span> | <span data-ttu-id="efe30-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="efe30-179">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="efe30-180">ID de lien</span><span class="sxs-lookup"><span data-stu-id="efe30-180">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="efe30-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="efe30-181">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="efe30-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="efe30-182">System-Only</span></span>            | <span data-ttu-id="efe30-183">Faux</span><span class="sxs-lookup"><span data-stu-id="efe30-183">False</span></span>                                                      |
| <span data-ttu-id="efe30-184">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="efe30-184">Is-Single-Valued</span></span>       | <span data-ttu-id="efe30-185">Faux</span><span class="sxs-lookup"><span data-stu-id="efe30-185">False</span></span>                                                      |
| <span data-ttu-id="efe30-186">Est indexé</span><span class="sxs-lookup"><span data-stu-id="efe30-186">Is Indexed</span></span>             | <span data-ttu-id="efe30-187">Faux</span><span class="sxs-lookup"><span data-stu-id="efe30-187">False</span></span>                                                      |
| <span data-ttu-id="efe30-188">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="efe30-188">In Global Catalog</span></span>      | <span data-ttu-id="efe30-189">Faux</span><span class="sxs-lookup"><span data-stu-id="efe30-189">False</span></span>                                                      |
| <span data-ttu-id="efe30-190">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="efe30-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="efe30-191">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="efe30-191">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="efe30-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="efe30-192">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="efe30-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="efe30-193">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="efe30-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="efe30-194">Search-Flags</span></span>           | <span data-ttu-id="efe30-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="efe30-195">0x00000000</span></span>                                                 |
| <span data-ttu-id="efe30-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="efe30-196">System-Flags</span></span>           | <span data-ttu-id="efe30-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="efe30-197">0x00000010</span></span>                                                 |
| <span data-ttu-id="efe30-198">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="efe30-198">Classes used in</span></span>        | [<span data-ttu-id="efe30-199">**Display-specifier**</span><span class="sxs-lookup"><span data-stu-id="efe30-199">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="efe30-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="efe30-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="efe30-201">Entrée</span><span class="sxs-lookup"><span data-stu-id="efe30-201">Entry</span></span> | <span data-ttu-id="efe30-202">Valeur</span><span class="sxs-lookup"><span data-stu-id="efe30-202">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="efe30-203">ID de lien</span><span class="sxs-lookup"><span data-stu-id="efe30-203">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="efe30-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="efe30-204">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="efe30-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="efe30-205">System-Only</span></span>            | <span data-ttu-id="efe30-206">Faux</span><span class="sxs-lookup"><span data-stu-id="efe30-206">False</span></span>                                                      |
| <span data-ttu-id="efe30-207">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="efe30-207">Is-Single-Valued</span></span>       | <span data-ttu-id="efe30-208">Faux</span><span class="sxs-lookup"><span data-stu-id="efe30-208">False</span></span>                                                      |
| <span data-ttu-id="efe30-209">Est indexé</span><span class="sxs-lookup"><span data-stu-id="efe30-209">Is Indexed</span></span>             | <span data-ttu-id="efe30-210">Faux</span><span class="sxs-lookup"><span data-stu-id="efe30-210">False</span></span>                                                      |
| <span data-ttu-id="efe30-211">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="efe30-211">In Global Catalog</span></span>      | <span data-ttu-id="efe30-212">Faux</span><span class="sxs-lookup"><span data-stu-id="efe30-212">False</span></span>                                                      |
| <span data-ttu-id="efe30-213">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="efe30-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="efe30-214">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="efe30-214">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="efe30-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="efe30-215">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="efe30-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="efe30-216">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="efe30-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="efe30-217">Search-Flags</span></span>           | <span data-ttu-id="efe30-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="efe30-218">0x00000000</span></span>                                                 |
| <span data-ttu-id="efe30-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="efe30-219">System-Flags</span></span>           | <span data-ttu-id="efe30-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="efe30-220">0x00000010</span></span>                                                 |
| <span data-ttu-id="efe30-221">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="efe30-221">Classes used in</span></span>        | [<span data-ttu-id="efe30-222">**Display-specifier**</span><span class="sxs-lookup"><span data-stu-id="efe30-222">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="efe30-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="efe30-223">Windows Server 2012</span></span>



| <span data-ttu-id="efe30-224">Entrée</span><span class="sxs-lookup"><span data-stu-id="efe30-224">Entry</span></span> | <span data-ttu-id="efe30-225">Valeur</span><span class="sxs-lookup"><span data-stu-id="efe30-225">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="efe30-226">ID de lien</span><span class="sxs-lookup"><span data-stu-id="efe30-226">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="efe30-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="efe30-227">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="efe30-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="efe30-228">System-Only</span></span>            | <span data-ttu-id="efe30-229">Faux</span><span class="sxs-lookup"><span data-stu-id="efe30-229">False</span></span>                                                      |
| <span data-ttu-id="efe30-230">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="efe30-230">Is-Single-Valued</span></span>       | <span data-ttu-id="efe30-231">Faux</span><span class="sxs-lookup"><span data-stu-id="efe30-231">False</span></span>                                                      |
| <span data-ttu-id="efe30-232">Est indexé</span><span class="sxs-lookup"><span data-stu-id="efe30-232">Is Indexed</span></span>             | <span data-ttu-id="efe30-233">Faux</span><span class="sxs-lookup"><span data-stu-id="efe30-233">False</span></span>                                                      |
| <span data-ttu-id="efe30-234">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="efe30-234">In Global Catalog</span></span>      | <span data-ttu-id="efe30-235">Faux</span><span class="sxs-lookup"><span data-stu-id="efe30-235">False</span></span>                                                      |
| <span data-ttu-id="efe30-236">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="efe30-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="efe30-237">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="efe30-237">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="efe30-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="efe30-238">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="efe30-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="efe30-239">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="efe30-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="efe30-240">Search-Flags</span></span>           | <span data-ttu-id="efe30-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="efe30-241">0x00000000</span></span>                                                 |
| <span data-ttu-id="efe30-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="efe30-242">System-Flags</span></span>           | <span data-ttu-id="efe30-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="efe30-243">0x00000010</span></span>                                                 |
| <span data-ttu-id="efe30-244">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="efe30-244">Classes used in</span></span>        | [<span data-ttu-id="efe30-245">**Display-specifier**</span><span class="sxs-lookup"><span data-stu-id="efe30-245">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



 

 





