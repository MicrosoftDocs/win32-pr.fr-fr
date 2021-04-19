---
title: Attribut Dns-Root
description: Nom de domaine DNS le plus élevé affecté à une partition de domaine/répertoire.
ms.assetid: 0b33daad-b5c5-4126-86fa-abd3e0006c5f
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Dns-Root
- Schéma AD de l’attribut dnsRoot
topic_type:
- apiref
api_name:
- Dns-Root
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a2c2fd2c39e8f0015d7641eccd27279b3478ec4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106514877"
---
# <a name="dns-root-attribute"></a><span data-ttu-id="475da-105">Attribut Dns-Root</span><span class="sxs-lookup"><span data-stu-id="475da-105">Dns-Root attribute</span></span>

<span data-ttu-id="475da-106">Nom de domaine DNS le plus élevé affecté à une partition de domaine/répertoire.</span><span class="sxs-lookup"><span data-stu-id="475da-106">The uppermost DNS domain name assigned to a domain/directory partition.</span></span> <span data-ttu-id="475da-107">Cette valeur est définie sur un objet crossRef et est utilisée, entre autres, pour la génération de références.</span><span class="sxs-lookup"><span data-stu-id="475da-107">This is set on a crossRef object and is used, among other things, for referral generation.</span></span> <span data-ttu-id="475da-108">Lors de la recherche dans l’ensemble de l’arborescence de domaine, la recherche doit être lancée au niveau de l’objet Dns-Root.</span><span class="sxs-lookup"><span data-stu-id="475da-108">When searching through an entire domain tree, the search must be initiated at the Dns-Root object.</span></span> <span data-ttu-id="475da-109">Cet attribut peut être à valeurs multiples, auquel cas plusieurs références sont générées.</span><span class="sxs-lookup"><span data-stu-id="475da-109">This attribute can be multi-valued, in which case multiple referrals are generated.</span></span>



| <span data-ttu-id="475da-110">Entrée</span><span class="sxs-lookup"><span data-stu-id="475da-110">Entry</span></span> | <span data-ttu-id="475da-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="475da-111">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="475da-112">CN</span><span class="sxs-lookup"><span data-stu-id="475da-112">CN</span></span>                | <span data-ttu-id="475da-113">Dns-Root</span><span class="sxs-lookup"><span data-stu-id="475da-113">Dns-Root</span></span>                                    |
| <span data-ttu-id="475da-114">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="475da-114">Ldap-Display-Name</span></span> | <span data-ttu-id="475da-115">dnsRoot</span><span class="sxs-lookup"><span data-stu-id="475da-115">dnsRoot</span></span>                                     |
| <span data-ttu-id="475da-116">Taille</span><span class="sxs-lookup"><span data-stu-id="475da-116">Size</span></span>              | \-                                          |
| <span data-ttu-id="475da-117">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="475da-117">Update Privilege</span></span>  | <span data-ttu-id="475da-118">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="475da-118">This value is set by the system.</span></span>            |
| <span data-ttu-id="475da-119">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="475da-119">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="475da-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="475da-120">Attribute-Id</span></span>      | <span data-ttu-id="475da-121">1.2.840.113556.1.4.28</span><span class="sxs-lookup"><span data-stu-id="475da-121">1.2.840.113556.1.4.28</span></span>                       |
| <span data-ttu-id="475da-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="475da-122">System-Id-Guid</span></span>    | <span data-ttu-id="475da-123">bf967959-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="475da-123">bf967959-0de6-11d0-a285-00aa003049e2</span></span>        |
| <span data-ttu-id="475da-124">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="475da-124">Syntax</span></span>            | [<span data-ttu-id="475da-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="475da-125">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="475da-126">Implémentations</span><span class="sxs-lookup"><span data-stu-id="475da-126">Implementations</span></span>

-   [<span data-ttu-id="475da-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="475da-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="475da-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="475da-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="475da-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="475da-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="475da-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="475da-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="475da-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="475da-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="475da-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="475da-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="475da-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="475da-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="475da-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="475da-134">Windows 2000 Server</span></span>



| <span data-ttu-id="475da-135">Entrée</span><span class="sxs-lookup"><span data-stu-id="475da-135">Entry</span></span> | <span data-ttu-id="475da-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="475da-136">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="475da-137">ID de lien</span><span class="sxs-lookup"><span data-stu-id="475da-137">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="475da-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="475da-138">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="475da-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="475da-139">System-Only</span></span>            | <span data-ttu-id="475da-140">Faux</span><span class="sxs-lookup"><span data-stu-id="475da-140">False</span></span>                                      |
| <span data-ttu-id="475da-141">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="475da-141">Is-Single-Valued</span></span>       | <span data-ttu-id="475da-142">Faux</span><span class="sxs-lookup"><span data-stu-id="475da-142">False</span></span>                                      |
| <span data-ttu-id="475da-143">Est indexé</span><span class="sxs-lookup"><span data-stu-id="475da-143">Is Indexed</span></span>             | <span data-ttu-id="475da-144">Vrai</span><span class="sxs-lookup"><span data-stu-id="475da-144">True</span></span>                                       |
| <span data-ttu-id="475da-145">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="475da-145">In Global Catalog</span></span>      | <span data-ttu-id="475da-146">Faux</span><span class="sxs-lookup"><span data-stu-id="475da-146">False</span></span>                                      |
| <span data-ttu-id="475da-147">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="475da-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="475da-148">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="475da-148">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="475da-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="475da-149">Range-Lower</span></span>            | <span data-ttu-id="475da-150">1</span><span class="sxs-lookup"><span data-stu-id="475da-150">1</span></span>                                          |
| <span data-ttu-id="475da-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="475da-151">Range-Upper</span></span>            | <span data-ttu-id="475da-152">255</span><span class="sxs-lookup"><span data-stu-id="475da-152">255</span></span>                                        |
| <span data-ttu-id="475da-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="475da-153">Search-Flags</span></span>           | <span data-ttu-id="475da-154">0x00000001</span><span class="sxs-lookup"><span data-stu-id="475da-154">0x00000001</span></span>                                 |
| <span data-ttu-id="475da-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="475da-155">System-Flags</span></span>           | <span data-ttu-id="475da-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="475da-156">0x00000010</span></span>                                 |
| <span data-ttu-id="475da-157">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="475da-157">Classes used in</span></span>        | [<span data-ttu-id="475da-158">**Référence croisée**</span><span class="sxs-lookup"><span data-stu-id="475da-158">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="475da-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="475da-159">Windows Server 2003</span></span>



| <span data-ttu-id="475da-160">Entrée</span><span class="sxs-lookup"><span data-stu-id="475da-160">Entry</span></span> | <span data-ttu-id="475da-161">Valeur</span><span class="sxs-lookup"><span data-stu-id="475da-161">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="475da-162">ID de lien</span><span class="sxs-lookup"><span data-stu-id="475da-162">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="475da-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="475da-163">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="475da-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="475da-164">System-Only</span></span>            | <span data-ttu-id="475da-165">Faux</span><span class="sxs-lookup"><span data-stu-id="475da-165">False</span></span>                                      |
| <span data-ttu-id="475da-166">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="475da-166">Is-Single-Valued</span></span>       | <span data-ttu-id="475da-167">Faux</span><span class="sxs-lookup"><span data-stu-id="475da-167">False</span></span>                                      |
| <span data-ttu-id="475da-168">Est indexé</span><span class="sxs-lookup"><span data-stu-id="475da-168">Is Indexed</span></span>             | <span data-ttu-id="475da-169">Vrai</span><span class="sxs-lookup"><span data-stu-id="475da-169">True</span></span>                                       |
| <span data-ttu-id="475da-170">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="475da-170">In Global Catalog</span></span>      | <span data-ttu-id="475da-171">Faux</span><span class="sxs-lookup"><span data-stu-id="475da-171">False</span></span>                                      |
| <span data-ttu-id="475da-172">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="475da-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="475da-173">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="475da-173">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="475da-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="475da-174">Range-Lower</span></span>            | <span data-ttu-id="475da-175">1</span><span class="sxs-lookup"><span data-stu-id="475da-175">1</span></span>                                          |
| <span data-ttu-id="475da-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="475da-176">Range-Upper</span></span>            | <span data-ttu-id="475da-177">255</span><span class="sxs-lookup"><span data-stu-id="475da-177">255</span></span>                                        |
| <span data-ttu-id="475da-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="475da-178">Search-Flags</span></span>           | <span data-ttu-id="475da-179">0x00000001</span><span class="sxs-lookup"><span data-stu-id="475da-179">0x00000001</span></span>                                 |
| <span data-ttu-id="475da-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="475da-180">System-Flags</span></span>           | <span data-ttu-id="475da-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="475da-181">0x00000010</span></span>                                 |
| <span data-ttu-id="475da-182">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="475da-182">Classes used in</span></span>        | [<span data-ttu-id="475da-183">**Référence croisée**</span><span class="sxs-lookup"><span data-stu-id="475da-183">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="adam"></a><span data-ttu-id="475da-184">ADAM</span><span class="sxs-lookup"><span data-stu-id="475da-184">ADAM</span></span>



| <span data-ttu-id="475da-185">Entrée</span><span class="sxs-lookup"><span data-stu-id="475da-185">Entry</span></span> | <span data-ttu-id="475da-186">Valeur</span><span class="sxs-lookup"><span data-stu-id="475da-186">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="475da-187">ID de lien</span><span class="sxs-lookup"><span data-stu-id="475da-187">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="475da-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="475da-188">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="475da-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="475da-189">System-Only</span></span>            | <span data-ttu-id="475da-190">Faux</span><span class="sxs-lookup"><span data-stu-id="475da-190">False</span></span>                                      |
| <span data-ttu-id="475da-191">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="475da-191">Is-Single-Valued</span></span>       | <span data-ttu-id="475da-192">Faux</span><span class="sxs-lookup"><span data-stu-id="475da-192">False</span></span>                                      |
| <span data-ttu-id="475da-193">Est indexé</span><span class="sxs-lookup"><span data-stu-id="475da-193">Is Indexed</span></span>             | <span data-ttu-id="475da-194">Vrai</span><span class="sxs-lookup"><span data-stu-id="475da-194">True</span></span>                                       |
| <span data-ttu-id="475da-195">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="475da-195">In Global Catalog</span></span>      | <span data-ttu-id="475da-196">Faux</span><span class="sxs-lookup"><span data-stu-id="475da-196">False</span></span>                                      |
| <span data-ttu-id="475da-197">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="475da-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="475da-198">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="475da-198">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="475da-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="475da-199">Range-Lower</span></span>            | <span data-ttu-id="475da-200">1</span><span class="sxs-lookup"><span data-stu-id="475da-200">1</span></span>                                          |
| <span data-ttu-id="475da-201">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="475da-201">Range-Upper</span></span>            | <span data-ttu-id="475da-202">255</span><span class="sxs-lookup"><span data-stu-id="475da-202">255</span></span>                                        |
| <span data-ttu-id="475da-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="475da-203">Search-Flags</span></span>           | <span data-ttu-id="475da-204">0x00000001</span><span class="sxs-lookup"><span data-stu-id="475da-204">0x00000001</span></span>                                 |
| <span data-ttu-id="475da-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="475da-205">System-Flags</span></span>           | <span data-ttu-id="475da-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="475da-206">0x00000010</span></span>                                 |
| <span data-ttu-id="475da-207">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="475da-207">Classes used in</span></span>        | [<span data-ttu-id="475da-208">**Référence croisée**</span><span class="sxs-lookup"><span data-stu-id="475da-208">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="475da-209">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="475da-209">Windows Server 2003 R2</span></span>



| <span data-ttu-id="475da-210">Entrée</span><span class="sxs-lookup"><span data-stu-id="475da-210">Entry</span></span> | <span data-ttu-id="475da-211">Valeur</span><span class="sxs-lookup"><span data-stu-id="475da-211">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="475da-212">ID de lien</span><span class="sxs-lookup"><span data-stu-id="475da-212">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="475da-213">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="475da-213">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="475da-214">System-Only</span><span class="sxs-lookup"><span data-stu-id="475da-214">System-Only</span></span>            | <span data-ttu-id="475da-215">Faux</span><span class="sxs-lookup"><span data-stu-id="475da-215">False</span></span>                                      |
| <span data-ttu-id="475da-216">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="475da-216">Is-Single-Valued</span></span>       | <span data-ttu-id="475da-217">Faux</span><span class="sxs-lookup"><span data-stu-id="475da-217">False</span></span>                                      |
| <span data-ttu-id="475da-218">Est indexé</span><span class="sxs-lookup"><span data-stu-id="475da-218">Is Indexed</span></span>             | <span data-ttu-id="475da-219">Vrai</span><span class="sxs-lookup"><span data-stu-id="475da-219">True</span></span>                                       |
| <span data-ttu-id="475da-220">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="475da-220">In Global Catalog</span></span>      | <span data-ttu-id="475da-221">Faux</span><span class="sxs-lookup"><span data-stu-id="475da-221">False</span></span>                                      |
| <span data-ttu-id="475da-222">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="475da-222">NT-Security-Descriptor</span></span> | <span data-ttu-id="475da-223">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="475da-223">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="475da-224">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="475da-224">Range-Lower</span></span>            | <span data-ttu-id="475da-225">1</span><span class="sxs-lookup"><span data-stu-id="475da-225">1</span></span>                                          |
| <span data-ttu-id="475da-226">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="475da-226">Range-Upper</span></span>            | <span data-ttu-id="475da-227">255</span><span class="sxs-lookup"><span data-stu-id="475da-227">255</span></span>                                        |
| <span data-ttu-id="475da-228">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="475da-228">Search-Flags</span></span>           | <span data-ttu-id="475da-229">0x00000001</span><span class="sxs-lookup"><span data-stu-id="475da-229">0x00000001</span></span>                                 |
| <span data-ttu-id="475da-230">System-Flags</span><span class="sxs-lookup"><span data-stu-id="475da-230">System-Flags</span></span>           | <span data-ttu-id="475da-231">0x00000010</span><span class="sxs-lookup"><span data-stu-id="475da-231">0x00000010</span></span>                                 |
| <span data-ttu-id="475da-232">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="475da-232">Classes used in</span></span>        | [<span data-ttu-id="475da-233">**Référence croisée**</span><span class="sxs-lookup"><span data-stu-id="475da-233">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="475da-234">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="475da-234">Windows Server 2008</span></span>



| <span data-ttu-id="475da-235">Entrée</span><span class="sxs-lookup"><span data-stu-id="475da-235">Entry</span></span> | <span data-ttu-id="475da-236">Valeur</span><span class="sxs-lookup"><span data-stu-id="475da-236">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="475da-237">ID de lien</span><span class="sxs-lookup"><span data-stu-id="475da-237">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="475da-238">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="475da-238">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="475da-239">System-Only</span><span class="sxs-lookup"><span data-stu-id="475da-239">System-Only</span></span>            | <span data-ttu-id="475da-240">Faux</span><span class="sxs-lookup"><span data-stu-id="475da-240">False</span></span>                                      |
| <span data-ttu-id="475da-241">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="475da-241">Is-Single-Valued</span></span>       | <span data-ttu-id="475da-242">Faux</span><span class="sxs-lookup"><span data-stu-id="475da-242">False</span></span>                                      |
| <span data-ttu-id="475da-243">Est indexé</span><span class="sxs-lookup"><span data-stu-id="475da-243">Is Indexed</span></span>             | <span data-ttu-id="475da-244">Vrai</span><span class="sxs-lookup"><span data-stu-id="475da-244">True</span></span>                                       |
| <span data-ttu-id="475da-245">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="475da-245">In Global Catalog</span></span>      | <span data-ttu-id="475da-246">Faux</span><span class="sxs-lookup"><span data-stu-id="475da-246">False</span></span>                                      |
| <span data-ttu-id="475da-247">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="475da-247">NT-Security-Descriptor</span></span> | <span data-ttu-id="475da-248">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="475da-248">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="475da-249">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="475da-249">Range-Lower</span></span>            | <span data-ttu-id="475da-250">1</span><span class="sxs-lookup"><span data-stu-id="475da-250">1</span></span>                                          |
| <span data-ttu-id="475da-251">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="475da-251">Range-Upper</span></span>            | <span data-ttu-id="475da-252">255</span><span class="sxs-lookup"><span data-stu-id="475da-252">255</span></span>                                        |
| <span data-ttu-id="475da-253">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="475da-253">Search-Flags</span></span>           | <span data-ttu-id="475da-254">0x00000001</span><span class="sxs-lookup"><span data-stu-id="475da-254">0x00000001</span></span>                                 |
| <span data-ttu-id="475da-255">System-Flags</span><span class="sxs-lookup"><span data-stu-id="475da-255">System-Flags</span></span>           | <span data-ttu-id="475da-256">0x00000010</span><span class="sxs-lookup"><span data-stu-id="475da-256">0x00000010</span></span>                                 |
| <span data-ttu-id="475da-257">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="475da-257">Classes used in</span></span>        | [<span data-ttu-id="475da-258">**Référence croisée**</span><span class="sxs-lookup"><span data-stu-id="475da-258">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="475da-259">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="475da-259">Windows Server 2008 R2</span></span>



| <span data-ttu-id="475da-260">Entrée</span><span class="sxs-lookup"><span data-stu-id="475da-260">Entry</span></span> | <span data-ttu-id="475da-261">Valeur</span><span class="sxs-lookup"><span data-stu-id="475da-261">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="475da-262">ID de lien</span><span class="sxs-lookup"><span data-stu-id="475da-262">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="475da-263">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="475da-263">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="475da-264">System-Only</span><span class="sxs-lookup"><span data-stu-id="475da-264">System-Only</span></span>            | <span data-ttu-id="475da-265">Faux</span><span class="sxs-lookup"><span data-stu-id="475da-265">False</span></span>                                      |
| <span data-ttu-id="475da-266">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="475da-266">Is-Single-Valued</span></span>       | <span data-ttu-id="475da-267">Faux</span><span class="sxs-lookup"><span data-stu-id="475da-267">False</span></span>                                      |
| <span data-ttu-id="475da-268">Est indexé</span><span class="sxs-lookup"><span data-stu-id="475da-268">Is Indexed</span></span>             | <span data-ttu-id="475da-269">Vrai</span><span class="sxs-lookup"><span data-stu-id="475da-269">True</span></span>                                       |
| <span data-ttu-id="475da-270">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="475da-270">In Global Catalog</span></span>      | <span data-ttu-id="475da-271">Faux</span><span class="sxs-lookup"><span data-stu-id="475da-271">False</span></span>                                      |
| <span data-ttu-id="475da-272">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="475da-272">NT-Security-Descriptor</span></span> | <span data-ttu-id="475da-273">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="475da-273">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="475da-274">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="475da-274">Range-Lower</span></span>            | <span data-ttu-id="475da-275">1</span><span class="sxs-lookup"><span data-stu-id="475da-275">1</span></span>                                          |
| <span data-ttu-id="475da-276">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="475da-276">Range-Upper</span></span>            | <span data-ttu-id="475da-277">255</span><span class="sxs-lookup"><span data-stu-id="475da-277">255</span></span>                                        |
| <span data-ttu-id="475da-278">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="475da-278">Search-Flags</span></span>           | <span data-ttu-id="475da-279">0x00000001</span><span class="sxs-lookup"><span data-stu-id="475da-279">0x00000001</span></span>                                 |
| <span data-ttu-id="475da-280">System-Flags</span><span class="sxs-lookup"><span data-stu-id="475da-280">System-Flags</span></span>           | <span data-ttu-id="475da-281">0x00000010</span><span class="sxs-lookup"><span data-stu-id="475da-281">0x00000010</span></span>                                 |
| <span data-ttu-id="475da-282">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="475da-282">Classes used in</span></span>        | [<span data-ttu-id="475da-283">**Référence croisée**</span><span class="sxs-lookup"><span data-stu-id="475da-283">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="475da-284">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="475da-284">Windows Server 2012</span></span>



| <span data-ttu-id="475da-285">Entrée</span><span class="sxs-lookup"><span data-stu-id="475da-285">Entry</span></span> | <span data-ttu-id="475da-286">Valeur</span><span class="sxs-lookup"><span data-stu-id="475da-286">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="475da-287">ID de lien</span><span class="sxs-lookup"><span data-stu-id="475da-287">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="475da-288">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="475da-288">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="475da-289">System-Only</span><span class="sxs-lookup"><span data-stu-id="475da-289">System-Only</span></span>            | <span data-ttu-id="475da-290">Faux</span><span class="sxs-lookup"><span data-stu-id="475da-290">False</span></span>                                      |
| <span data-ttu-id="475da-291">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="475da-291">Is-Single-Valued</span></span>       | <span data-ttu-id="475da-292">Faux</span><span class="sxs-lookup"><span data-stu-id="475da-292">False</span></span>                                      |
| <span data-ttu-id="475da-293">Est indexé</span><span class="sxs-lookup"><span data-stu-id="475da-293">Is Indexed</span></span>             | <span data-ttu-id="475da-294">Vrai</span><span class="sxs-lookup"><span data-stu-id="475da-294">True</span></span>                                       |
| <span data-ttu-id="475da-295">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="475da-295">In Global Catalog</span></span>      | <span data-ttu-id="475da-296">Faux</span><span class="sxs-lookup"><span data-stu-id="475da-296">False</span></span>                                      |
| <span data-ttu-id="475da-297">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="475da-297">NT-Security-Descriptor</span></span> | <span data-ttu-id="475da-298">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="475da-298">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="475da-299">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="475da-299">Range-Lower</span></span>            | <span data-ttu-id="475da-300">1</span><span class="sxs-lookup"><span data-stu-id="475da-300">1</span></span>                                          |
| <span data-ttu-id="475da-301">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="475da-301">Range-Upper</span></span>            | <span data-ttu-id="475da-302">255</span><span class="sxs-lookup"><span data-stu-id="475da-302">255</span></span>                                        |
| <span data-ttu-id="475da-303">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="475da-303">Search-Flags</span></span>           | <span data-ttu-id="475da-304">0x00000001</span><span class="sxs-lookup"><span data-stu-id="475da-304">0x00000001</span></span>                                 |
| <span data-ttu-id="475da-305">System-Flags</span><span class="sxs-lookup"><span data-stu-id="475da-305">System-Flags</span></span>           | <span data-ttu-id="475da-306">0x00000010</span><span class="sxs-lookup"><span data-stu-id="475da-306">0x00000010</span></span>                                 |
| <span data-ttu-id="475da-307">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="475da-307">Classes used in</span></span>        | [<span data-ttu-id="475da-308">**Référence croisée**</span><span class="sxs-lookup"><span data-stu-id="475da-308">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



 

 





