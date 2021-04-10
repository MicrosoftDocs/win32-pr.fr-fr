---
title: Attribut Domain-Component
description: Attribut de nom pour les objets Domain et DNS. Généralement affiché en tant que DC DomainName.
ms.assetid: 1d674af1-ed2f-4266-9704-8c6ed5a9bdd8
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Domain-Component
- Schéma AD d’attribut de contrôleur de domaine
topic_type:
- apiref
api_name:
- Domain-Component
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a97a6958d51c6e0e29f70685b2624fb194d42e05
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107149"
---
# <a name="domain-component-attribute"></a><span data-ttu-id="ca739-106">Attribut Domain-Component</span><span class="sxs-lookup"><span data-stu-id="ca739-106">Domain-Component attribute</span></span>

<span data-ttu-id="ca739-107">Attribut de nom pour les objets Domain et DNS.</span><span class="sxs-lookup"><span data-stu-id="ca739-107">The naming attribute for Domain and DNS objects.</span></span> <span data-ttu-id="ca739-108">Généralement affiché sous la forme DC = DomainName.</span><span class="sxs-lookup"><span data-stu-id="ca739-108">Usually displayed as dc=DomainName.</span></span>



| <span data-ttu-id="ca739-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="ca739-109">Entry</span></span> | <span data-ttu-id="ca739-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="ca739-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="ca739-111">CN</span><span class="sxs-lookup"><span data-stu-id="ca739-111">CN</span></span>                | <span data-ttu-id="ca739-112">Domain-Component</span><span class="sxs-lookup"><span data-stu-id="ca739-112">Domain-Component</span></span>                            |
| <span data-ttu-id="ca739-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="ca739-113">Ldap-Display-Name</span></span> | <span data-ttu-id="ca739-114">dc</span><span class="sxs-lookup"><span data-stu-id="ca739-114">dc</span></span>                                          |
| <span data-ttu-id="ca739-115">Taille</span><span class="sxs-lookup"><span data-stu-id="ca739-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="ca739-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="ca739-116">Update Privilege</span></span>  | <span data-ttu-id="ca739-117">Administrateur de domaine</span><span class="sxs-lookup"><span data-stu-id="ca739-117">Domain administrator</span></span>                        |
| <span data-ttu-id="ca739-118">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="ca739-118">Update Frequency</span></span>  | <span data-ttu-id="ca739-119">Lors de la création du domaine.</span><span class="sxs-lookup"><span data-stu-id="ca739-119">When the domain is created.</span></span>                 |
| <span data-ttu-id="ca739-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ca739-120">Attribute-Id</span></span>      | <span data-ttu-id="ca739-121">0.9.2342.19200300.100.1.25</span><span class="sxs-lookup"><span data-stu-id="ca739-121">0.9.2342.19200300.100.1.25</span></span>                  |
| <span data-ttu-id="ca739-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ca739-122">System-Id-Guid</span></span>    | <span data-ttu-id="ca739-123">19195a55-6da0-11d0-afd3-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="ca739-123">19195a55-6da0-11d0-afd3-00c04fd930c9</span></span>        |
| <span data-ttu-id="ca739-124">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ca739-124">Syntax</span></span>            | [<span data-ttu-id="ca739-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="ca739-125">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="ca739-126">Implémentations</span><span class="sxs-lookup"><span data-stu-id="ca739-126">Implementations</span></span>

-   [<span data-ttu-id="ca739-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ca739-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ca739-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ca739-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ca739-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="ca739-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="ca739-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ca739-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ca739-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ca739-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ca739-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ca739-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ca739-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ca739-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ca739-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ca739-134">Windows 2000 Server</span></span>



| <span data-ttu-id="ca739-135">Entrée</span><span class="sxs-lookup"><span data-stu-id="ca739-135">Entry</span></span> | <span data-ttu-id="ca739-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="ca739-136">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca739-137">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ca739-137">Link-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="ca739-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ca739-138">MAPI-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="ca739-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="ca739-139">System-Only</span></span>            | <span data-ttu-id="ca739-140">Faux</span><span class="sxs-lookup"><span data-stu-id="ca739-140">False</span></span>                                                                                                                   |
| <span data-ttu-id="ca739-141">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ca739-141">Is-Single-Valued</span></span>       | <span data-ttu-id="ca739-142">Vrai</span><span class="sxs-lookup"><span data-stu-id="ca739-142">True</span></span>                                                                                                                    |
| <span data-ttu-id="ca739-143">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ca739-143">Is Indexed</span></span>             | <span data-ttu-id="ca739-144">Faux</span><span class="sxs-lookup"><span data-stu-id="ca739-144">False</span></span>                                                                                                                   |
| <span data-ttu-id="ca739-145">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ca739-145">In Global Catalog</span></span>      | <span data-ttu-id="ca739-146">Vrai</span><span class="sxs-lookup"><span data-stu-id="ca739-146">True</span></span>                                                                                                                    |
| <span data-ttu-id="ca739-147">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ca739-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="ca739-148">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ca739-148">O:BAG:BAD:S:</span></span>                                                                                                            |
| <span data-ttu-id="ca739-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ca739-149">Range-Lower</span></span>            | <span data-ttu-id="ca739-150">1</span><span class="sxs-lookup"><span data-stu-id="ca739-150">1</span></span>                                                                                                                       |
| <span data-ttu-id="ca739-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ca739-151">Range-Upper</span></span>            | <span data-ttu-id="ca739-152">255</span><span class="sxs-lookup"><span data-stu-id="ca739-152">255</span></span>                                                                                                                     |
| <span data-ttu-id="ca739-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ca739-153">Search-Flags</span></span>           | <span data-ttu-id="ca739-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ca739-154">0x00000000</span></span>                                                                                                              |
| <span data-ttu-id="ca739-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ca739-155">System-Flags</span></span>           | <span data-ttu-id="ca739-156">0x00000012</span><span class="sxs-lookup"><span data-stu-id="ca739-156">0x00000012</span></span>                                                                                                              |
| <span data-ttu-id="ca739-157">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ca739-157">Classes used in</span></span>        | [<span data-ttu-id="ca739-158">**Nœud DNS**</span><span class="sxs-lookup"><span data-stu-id="ca739-158">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="ca739-159">**Zone DNS**</span><span class="sxs-lookup"><span data-stu-id="ca739-159">**Dns-Zone**</span></span>](c-dnszone.md)<br/> [<span data-ttu-id="ca739-160">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="ca739-160">**Domain**</span></span>](c-domain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ca739-161">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ca739-161">Windows Server 2003</span></span>



| <span data-ttu-id="ca739-162">Entrée</span><span class="sxs-lookup"><span data-stu-id="ca739-162">Entry</span></span> | <span data-ttu-id="ca739-163">Valeur</span><span class="sxs-lookup"><span data-stu-id="ca739-163">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca739-164">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ca739-164">Link-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="ca739-165">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ca739-165">MAPI-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="ca739-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="ca739-166">System-Only</span></span>            | <span data-ttu-id="ca739-167">Faux</span><span class="sxs-lookup"><span data-stu-id="ca739-167">False</span></span>                                                                                                                   |
| <span data-ttu-id="ca739-168">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ca739-168">Is-Single-Valued</span></span>       | <span data-ttu-id="ca739-169">Vrai</span><span class="sxs-lookup"><span data-stu-id="ca739-169">True</span></span>                                                                                                                    |
| <span data-ttu-id="ca739-170">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ca739-170">Is Indexed</span></span>             | <span data-ttu-id="ca739-171">Faux</span><span class="sxs-lookup"><span data-stu-id="ca739-171">False</span></span>                                                                                                                   |
| <span data-ttu-id="ca739-172">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ca739-172">In Global Catalog</span></span>      | <span data-ttu-id="ca739-173">Vrai</span><span class="sxs-lookup"><span data-stu-id="ca739-173">True</span></span>                                                                                                                    |
| <span data-ttu-id="ca739-174">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ca739-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="ca739-175">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ca739-175">O:BAG:BAD:S:</span></span>                                                                                                            |
| <span data-ttu-id="ca739-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ca739-176">Range-Lower</span></span>            | <span data-ttu-id="ca739-177">1</span><span class="sxs-lookup"><span data-stu-id="ca739-177">1</span></span>                                                                                                                       |
| <span data-ttu-id="ca739-178">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ca739-178">Range-Upper</span></span>            | <span data-ttu-id="ca739-179">255</span><span class="sxs-lookup"><span data-stu-id="ca739-179">255</span></span>                                                                                                                     |
| <span data-ttu-id="ca739-180">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ca739-180">Search-Flags</span></span>           | <span data-ttu-id="ca739-181">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ca739-181">0x00000000</span></span>                                                                                                              |
| <span data-ttu-id="ca739-182">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ca739-182">System-Flags</span></span>           | <span data-ttu-id="ca739-183">0x00000012</span><span class="sxs-lookup"><span data-stu-id="ca739-183">0x00000012</span></span>                                                                                                              |
| <span data-ttu-id="ca739-184">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ca739-184">Classes used in</span></span>        | [<span data-ttu-id="ca739-185">**Nœud DNS**</span><span class="sxs-lookup"><span data-stu-id="ca739-185">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="ca739-186">**Zone DNS**</span><span class="sxs-lookup"><span data-stu-id="ca739-186">**Dns-Zone**</span></span>](c-dnszone.md)<br/> [<span data-ttu-id="ca739-187">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="ca739-187">**Domain**</span></span>](c-domain.md)<br/> |



## <a name="adam"></a><span data-ttu-id="ca739-188">ADAM</span><span class="sxs-lookup"><span data-stu-id="ca739-188">ADAM</span></span>



| <span data-ttu-id="ca739-189">Entrée</span><span class="sxs-lookup"><span data-stu-id="ca739-189">Entry</span></span> | <span data-ttu-id="ca739-190">Valeur</span><span class="sxs-lookup"><span data-stu-id="ca739-190">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="ca739-191">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ca739-191">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="ca739-192">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ca739-192">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="ca739-193">System-Only</span><span class="sxs-lookup"><span data-stu-id="ca739-193">System-Only</span></span>            | <span data-ttu-id="ca739-194">Faux</span><span class="sxs-lookup"><span data-stu-id="ca739-194">False</span></span>                                 |
| <span data-ttu-id="ca739-195">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ca739-195">Is-Single-Valued</span></span>       | <span data-ttu-id="ca739-196">Vrai</span><span class="sxs-lookup"><span data-stu-id="ca739-196">True</span></span>                                  |
| <span data-ttu-id="ca739-197">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ca739-197">Is Indexed</span></span>             | <span data-ttu-id="ca739-198">Faux</span><span class="sxs-lookup"><span data-stu-id="ca739-198">False</span></span>                                 |
| <span data-ttu-id="ca739-199">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ca739-199">In Global Catalog</span></span>      | <span data-ttu-id="ca739-200">Vrai</span><span class="sxs-lookup"><span data-stu-id="ca739-200">True</span></span>                                  |
| <span data-ttu-id="ca739-201">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ca739-201">NT-Security-Descriptor</span></span> | <span data-ttu-id="ca739-202">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ca739-202">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="ca739-203">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ca739-203">Range-Lower</span></span>            | <span data-ttu-id="ca739-204">1</span><span class="sxs-lookup"><span data-stu-id="ca739-204">1</span></span>                                     |
| <span data-ttu-id="ca739-205">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ca739-205">Range-Upper</span></span>            | <span data-ttu-id="ca739-206">255</span><span class="sxs-lookup"><span data-stu-id="ca739-206">255</span></span>                                   |
| <span data-ttu-id="ca739-207">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ca739-207">Search-Flags</span></span>           | <span data-ttu-id="ca739-208">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ca739-208">0x00000000</span></span>                            |
| <span data-ttu-id="ca739-209">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ca739-209">System-Flags</span></span>           | <span data-ttu-id="ca739-210">0x00000012</span><span class="sxs-lookup"><span data-stu-id="ca739-210">0x00000012</span></span>                            |
| <span data-ttu-id="ca739-211">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ca739-211">Classes used in</span></span>        | [<span data-ttu-id="ca739-212">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="ca739-212">**Domain**</span></span>](c-domain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ca739-213">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ca739-213">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ca739-214">Entrée</span><span class="sxs-lookup"><span data-stu-id="ca739-214">Entry</span></span> | <span data-ttu-id="ca739-215">Valeur</span><span class="sxs-lookup"><span data-stu-id="ca739-215">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca739-216">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ca739-216">Link-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="ca739-217">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ca739-217">MAPI-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="ca739-218">System-Only</span><span class="sxs-lookup"><span data-stu-id="ca739-218">System-Only</span></span>            | <span data-ttu-id="ca739-219">Faux</span><span class="sxs-lookup"><span data-stu-id="ca739-219">False</span></span>                                                                                                                   |
| <span data-ttu-id="ca739-220">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ca739-220">Is-Single-Valued</span></span>       | <span data-ttu-id="ca739-221">Vrai</span><span class="sxs-lookup"><span data-stu-id="ca739-221">True</span></span>                                                                                                                    |
| <span data-ttu-id="ca739-222">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ca739-222">Is Indexed</span></span>             | <span data-ttu-id="ca739-223">Faux</span><span class="sxs-lookup"><span data-stu-id="ca739-223">False</span></span>                                                                                                                   |
| <span data-ttu-id="ca739-224">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ca739-224">In Global Catalog</span></span>      | <span data-ttu-id="ca739-225">Vrai</span><span class="sxs-lookup"><span data-stu-id="ca739-225">True</span></span>                                                                                                                    |
| <span data-ttu-id="ca739-226">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ca739-226">NT-Security-Descriptor</span></span> | <span data-ttu-id="ca739-227">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ca739-227">O:BAG:BAD:S:</span></span>                                                                                                            |
| <span data-ttu-id="ca739-228">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ca739-228">Range-Lower</span></span>            | <span data-ttu-id="ca739-229">1</span><span class="sxs-lookup"><span data-stu-id="ca739-229">1</span></span>                                                                                                                       |
| <span data-ttu-id="ca739-230">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ca739-230">Range-Upper</span></span>            | <span data-ttu-id="ca739-231">255</span><span class="sxs-lookup"><span data-stu-id="ca739-231">255</span></span>                                                                                                                     |
| <span data-ttu-id="ca739-232">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ca739-232">Search-Flags</span></span>           | <span data-ttu-id="ca739-233">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ca739-233">0x00000000</span></span>                                                                                                              |
| <span data-ttu-id="ca739-234">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ca739-234">System-Flags</span></span>           | <span data-ttu-id="ca739-235">0x00000012</span><span class="sxs-lookup"><span data-stu-id="ca739-235">0x00000012</span></span>                                                                                                              |
| <span data-ttu-id="ca739-236">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ca739-236">Classes used in</span></span>        | [<span data-ttu-id="ca739-237">**Nœud DNS**</span><span class="sxs-lookup"><span data-stu-id="ca739-237">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="ca739-238">**Zone DNS**</span><span class="sxs-lookup"><span data-stu-id="ca739-238">**Dns-Zone**</span></span>](c-dnszone.md)<br/> [<span data-ttu-id="ca739-239">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="ca739-239">**Domain**</span></span>](c-domain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ca739-240">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ca739-240">Windows Server 2008</span></span>



| <span data-ttu-id="ca739-241">Entrée</span><span class="sxs-lookup"><span data-stu-id="ca739-241">Entry</span></span> | <span data-ttu-id="ca739-242">Valeur</span><span class="sxs-lookup"><span data-stu-id="ca739-242">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca739-243">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ca739-243">Link-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="ca739-244">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ca739-244">MAPI-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="ca739-245">System-Only</span><span class="sxs-lookup"><span data-stu-id="ca739-245">System-Only</span></span>            | <span data-ttu-id="ca739-246">Faux</span><span class="sxs-lookup"><span data-stu-id="ca739-246">False</span></span>                                                                                                                   |
| <span data-ttu-id="ca739-247">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ca739-247">Is-Single-Valued</span></span>       | <span data-ttu-id="ca739-248">Vrai</span><span class="sxs-lookup"><span data-stu-id="ca739-248">True</span></span>                                                                                                                    |
| <span data-ttu-id="ca739-249">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ca739-249">Is Indexed</span></span>             | <span data-ttu-id="ca739-250">Faux</span><span class="sxs-lookup"><span data-stu-id="ca739-250">False</span></span>                                                                                                                   |
| <span data-ttu-id="ca739-251">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ca739-251">In Global Catalog</span></span>      | <span data-ttu-id="ca739-252">Vrai</span><span class="sxs-lookup"><span data-stu-id="ca739-252">True</span></span>                                                                                                                    |
| <span data-ttu-id="ca739-253">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ca739-253">NT-Security-Descriptor</span></span> | <span data-ttu-id="ca739-254">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ca739-254">O:BAG:BAD:S:</span></span>                                                                                                            |
| <span data-ttu-id="ca739-255">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ca739-255">Range-Lower</span></span>            | <span data-ttu-id="ca739-256">1</span><span class="sxs-lookup"><span data-stu-id="ca739-256">1</span></span>                                                                                                                       |
| <span data-ttu-id="ca739-257">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ca739-257">Range-Upper</span></span>            | <span data-ttu-id="ca739-258">255</span><span class="sxs-lookup"><span data-stu-id="ca739-258">255</span></span>                                                                                                                     |
| <span data-ttu-id="ca739-259">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ca739-259">Search-Flags</span></span>           | <span data-ttu-id="ca739-260">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ca739-260">0x00000000</span></span>                                                                                                              |
| <span data-ttu-id="ca739-261">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ca739-261">System-Flags</span></span>           | <span data-ttu-id="ca739-262">0x00000012</span><span class="sxs-lookup"><span data-stu-id="ca739-262">0x00000012</span></span>                                                                                                              |
| <span data-ttu-id="ca739-263">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ca739-263">Classes used in</span></span>        | [<span data-ttu-id="ca739-264">**Nœud DNS**</span><span class="sxs-lookup"><span data-stu-id="ca739-264">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="ca739-265">**Zone DNS**</span><span class="sxs-lookup"><span data-stu-id="ca739-265">**Dns-Zone**</span></span>](c-dnszone.md)<br/> [<span data-ttu-id="ca739-266">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="ca739-266">**Domain**</span></span>](c-domain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ca739-267">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ca739-267">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ca739-268">Entrée</span><span class="sxs-lookup"><span data-stu-id="ca739-268">Entry</span></span> | <span data-ttu-id="ca739-269">Valeur</span><span class="sxs-lookup"><span data-stu-id="ca739-269">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca739-270">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ca739-270">Link-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="ca739-271">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ca739-271">MAPI-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="ca739-272">System-Only</span><span class="sxs-lookup"><span data-stu-id="ca739-272">System-Only</span></span>            | <span data-ttu-id="ca739-273">Faux</span><span class="sxs-lookup"><span data-stu-id="ca739-273">False</span></span>                                                                                                                   |
| <span data-ttu-id="ca739-274">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ca739-274">Is-Single-Valued</span></span>       | <span data-ttu-id="ca739-275">Vrai</span><span class="sxs-lookup"><span data-stu-id="ca739-275">True</span></span>                                                                                                                    |
| <span data-ttu-id="ca739-276">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ca739-276">Is Indexed</span></span>             | <span data-ttu-id="ca739-277">Faux</span><span class="sxs-lookup"><span data-stu-id="ca739-277">False</span></span>                                                                                                                   |
| <span data-ttu-id="ca739-278">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ca739-278">In Global Catalog</span></span>      | <span data-ttu-id="ca739-279">Vrai</span><span class="sxs-lookup"><span data-stu-id="ca739-279">True</span></span>                                                                                                                    |
| <span data-ttu-id="ca739-280">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ca739-280">NT-Security-Descriptor</span></span> | <span data-ttu-id="ca739-281">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ca739-281">O:BAG:BAD:S:</span></span>                                                                                                            |
| <span data-ttu-id="ca739-282">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ca739-282">Range-Lower</span></span>            | <span data-ttu-id="ca739-283">1</span><span class="sxs-lookup"><span data-stu-id="ca739-283">1</span></span>                                                                                                                       |
| <span data-ttu-id="ca739-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ca739-284">Range-Upper</span></span>            | <span data-ttu-id="ca739-285">255</span><span class="sxs-lookup"><span data-stu-id="ca739-285">255</span></span>                                                                                                                     |
| <span data-ttu-id="ca739-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ca739-286">Search-Flags</span></span>           | <span data-ttu-id="ca739-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ca739-287">0x00000000</span></span>                                                                                                              |
| <span data-ttu-id="ca739-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ca739-288">System-Flags</span></span>           | <span data-ttu-id="ca739-289">0x00000012</span><span class="sxs-lookup"><span data-stu-id="ca739-289">0x00000012</span></span>                                                                                                              |
| <span data-ttu-id="ca739-290">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ca739-290">Classes used in</span></span>        | [<span data-ttu-id="ca739-291">**Nœud DNS**</span><span class="sxs-lookup"><span data-stu-id="ca739-291">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="ca739-292">**Zone DNS**</span><span class="sxs-lookup"><span data-stu-id="ca739-292">**Dns-Zone**</span></span>](c-dnszone.md)<br/> [<span data-ttu-id="ca739-293">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="ca739-293">**Domain**</span></span>](c-domain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ca739-294">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ca739-294">Windows Server 2012</span></span>



| <span data-ttu-id="ca739-295">Entrée</span><span class="sxs-lookup"><span data-stu-id="ca739-295">Entry</span></span> | <span data-ttu-id="ca739-296">Valeur</span><span class="sxs-lookup"><span data-stu-id="ca739-296">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca739-297">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ca739-297">Link-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="ca739-298">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ca739-298">MAPI-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="ca739-299">System-Only</span><span class="sxs-lookup"><span data-stu-id="ca739-299">System-Only</span></span>            | <span data-ttu-id="ca739-300">Faux</span><span class="sxs-lookup"><span data-stu-id="ca739-300">False</span></span>                                                                                                                   |
| <span data-ttu-id="ca739-301">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ca739-301">Is-Single-Valued</span></span>       | <span data-ttu-id="ca739-302">Vrai</span><span class="sxs-lookup"><span data-stu-id="ca739-302">True</span></span>                                                                                                                    |
| <span data-ttu-id="ca739-303">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ca739-303">Is Indexed</span></span>             | <span data-ttu-id="ca739-304">Faux</span><span class="sxs-lookup"><span data-stu-id="ca739-304">False</span></span>                                                                                                                   |
| <span data-ttu-id="ca739-305">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ca739-305">In Global Catalog</span></span>      | <span data-ttu-id="ca739-306">Vrai</span><span class="sxs-lookup"><span data-stu-id="ca739-306">True</span></span>                                                                                                                    |
| <span data-ttu-id="ca739-307">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ca739-307">NT-Security-Descriptor</span></span> | <span data-ttu-id="ca739-308">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ca739-308">O:BAG:BAD:S:</span></span>                                                                                                            |
| <span data-ttu-id="ca739-309">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ca739-309">Range-Lower</span></span>            | <span data-ttu-id="ca739-310">1</span><span class="sxs-lookup"><span data-stu-id="ca739-310">1</span></span>                                                                                                                       |
| <span data-ttu-id="ca739-311">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ca739-311">Range-Upper</span></span>            | <span data-ttu-id="ca739-312">255</span><span class="sxs-lookup"><span data-stu-id="ca739-312">255</span></span>                                                                                                                     |
| <span data-ttu-id="ca739-313">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ca739-313">Search-Flags</span></span>           | <span data-ttu-id="ca739-314">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ca739-314">0x00000000</span></span>                                                                                                              |
| <span data-ttu-id="ca739-315">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ca739-315">System-Flags</span></span>           | <span data-ttu-id="ca739-316">0x00000012</span><span class="sxs-lookup"><span data-stu-id="ca739-316">0x00000012</span></span>                                                                                                              |
| <span data-ttu-id="ca739-317">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ca739-317">Classes used in</span></span>        | [<span data-ttu-id="ca739-318">**Nœud DNS**</span><span class="sxs-lookup"><span data-stu-id="ca739-318">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="ca739-319">**Zone DNS**</span><span class="sxs-lookup"><span data-stu-id="ca739-319">**Dns-Zone**</span></span>](c-dnszone.md)<br/> [<span data-ttu-id="ca739-320">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="ca739-320">**Domain**</span></span>](c-domain.md)<br/> |



 

 





