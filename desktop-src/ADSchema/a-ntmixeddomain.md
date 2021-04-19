---
title: NT-attribut mixte de domaine
description: Indique que le domaine est en mode natif ou en mode mixte. Cet attribut se trouve dans l’objet domainDNS (Head) pour le domaine.
ms.assetid: 49872cbc-844f-4d60-89b6-0150b9116740
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut de domaine mixte NT
- Schéma AD de l’attribut nTMixedDomain
topic_type:
- apiref
api_name:
- NT-Mixed-Domain
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 217d73291f392141b80ca8916b86fffa0055226c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106544519"
---
# <a name="nt-mixed-domain-attribute"></a><span data-ttu-id="a1224-106">NT-attribut mixte de domaine</span><span class="sxs-lookup"><span data-stu-id="a1224-106">NT-Mixed-Domain attribute</span></span>

<span data-ttu-id="a1224-107">Indique que le domaine est en mode natif ou en mode mixte.</span><span class="sxs-lookup"><span data-stu-id="a1224-107">Indicates that the domain is in native mode or mixed mode.</span></span> <span data-ttu-id="a1224-108">Cet attribut se trouve dans l’objet domainDNS (Head) pour le domaine.</span><span class="sxs-lookup"><span data-stu-id="a1224-108">This attribute is found in the domainDNS (head) object for the domain.</span></span>



| <span data-ttu-id="a1224-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="a1224-109">Entry</span></span> | <span data-ttu-id="a1224-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="a1224-110">Value</span></span> |
|-------------------|---------------------------------------|
| <span data-ttu-id="a1224-111">CN</span><span class="sxs-lookup"><span data-stu-id="a1224-111">CN</span></span>                | <span data-ttu-id="a1224-112">NT-mixte-domaine</span><span class="sxs-lookup"><span data-stu-id="a1224-112">NT-Mixed-Domain</span></span>                       |
| <span data-ttu-id="a1224-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="a1224-113">Ldap-Display-Name</span></span> | <span data-ttu-id="a1224-114">nTMixedDomain</span><span class="sxs-lookup"><span data-stu-id="a1224-114">nTMixedDomain</span></span>                         |
| <span data-ttu-id="a1224-115">Taille</span><span class="sxs-lookup"><span data-stu-id="a1224-115">Size</span></span>              | <span data-ttu-id="a1224-116">4 octets.</span><span class="sxs-lookup"><span data-stu-id="a1224-116">4 bytes.</span></span> <span data-ttu-id="a1224-117">Mode mixte 1, mode natif 0.</span><span class="sxs-lookup"><span data-stu-id="a1224-117">Mixed mode 1, native mode 0.</span></span> |
| <span data-ttu-id="a1224-118">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="a1224-118">Update Privilege</span></span>  | \-                                    |
| <span data-ttu-id="a1224-119">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="a1224-119">Update Frequency</span></span>  | \-                                    |
| <span data-ttu-id="a1224-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a1224-120">Attribute-Id</span></span>      | <span data-ttu-id="a1224-121">1.2.840.113556.1.4.357</span><span class="sxs-lookup"><span data-stu-id="a1224-121">1.2.840.113556.1.4.357</span></span>                |
| <span data-ttu-id="a1224-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a1224-122">System-Id-Guid</span></span>    | <span data-ttu-id="a1224-123">3e97891f-8c01-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="a1224-123">3e97891f-8c01-11d0-afda-00c04fd930c9</span></span>  |
| <span data-ttu-id="a1224-124">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a1224-124">Syntax</span></span>            | [<span data-ttu-id="a1224-125">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="a1224-125">**Enumeration**</span></span>](s-enumeration.md)  |



## <a name="implementations"></a><span data-ttu-id="a1224-126">Implémentations</span><span class="sxs-lookup"><span data-stu-id="a1224-126">Implementations</span></span>

-   [<span data-ttu-id="a1224-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a1224-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a1224-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a1224-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a1224-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a1224-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a1224-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a1224-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a1224-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a1224-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a1224-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a1224-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a1224-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a1224-133">Windows 2000 Server</span></span>



| <span data-ttu-id="a1224-134">Entrée</span><span class="sxs-lookup"><span data-stu-id="a1224-134">Entry</span></span> | <span data-ttu-id="a1224-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="a1224-135">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a1224-136">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a1224-136">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a1224-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a1224-137">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a1224-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="a1224-138">System-Only</span></span>            | <span data-ttu-id="a1224-139">Faux</span><span class="sxs-lookup"><span data-stu-id="a1224-139">False</span></span>                                        |
| <span data-ttu-id="a1224-140">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a1224-140">Is-Single-Valued</span></span>       | <span data-ttu-id="a1224-141">Vrai</span><span class="sxs-lookup"><span data-stu-id="a1224-141">True</span></span>                                         |
| <span data-ttu-id="a1224-142">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a1224-142">Is Indexed</span></span>             | <span data-ttu-id="a1224-143">Faux</span><span class="sxs-lookup"><span data-stu-id="a1224-143">False</span></span>                                        |
| <span data-ttu-id="a1224-144">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a1224-144">In Global Catalog</span></span>      | <span data-ttu-id="a1224-145">Faux</span><span class="sxs-lookup"><span data-stu-id="a1224-145">False</span></span>                                        |
| <span data-ttu-id="a1224-146">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a1224-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="a1224-147">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a1224-147">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a1224-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a1224-148">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a1224-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a1224-149">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a1224-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a1224-150">Search-Flags</span></span>           | <span data-ttu-id="a1224-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a1224-151">0x00000000</span></span>                                   |
| <span data-ttu-id="a1224-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a1224-152">System-Flags</span></span>           | <span data-ttu-id="a1224-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a1224-153">0x00000010</span></span>                                   |
| <span data-ttu-id="a1224-154">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a1224-154">Classes used in</span></span>        | [<span data-ttu-id="a1224-155">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="a1224-155">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a1224-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a1224-156">Windows Server 2003</span></span>



| <span data-ttu-id="a1224-157">Entrée</span><span class="sxs-lookup"><span data-stu-id="a1224-157">Entry</span></span> | <span data-ttu-id="a1224-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="a1224-158">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1224-159">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a1224-159">Link-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="a1224-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a1224-160">MAPI-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="a1224-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="a1224-161">System-Only</span></span>            | <span data-ttu-id="a1224-162">Faux</span><span class="sxs-lookup"><span data-stu-id="a1224-162">False</span></span>                                                                                   |
| <span data-ttu-id="a1224-163">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a1224-163">Is-Single-Valued</span></span>       | <span data-ttu-id="a1224-164">Vrai</span><span class="sxs-lookup"><span data-stu-id="a1224-164">True</span></span>                                                                                    |
| <span data-ttu-id="a1224-165">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a1224-165">Is Indexed</span></span>             | <span data-ttu-id="a1224-166">Faux</span><span class="sxs-lookup"><span data-stu-id="a1224-166">False</span></span>                                                                                   |
| <span data-ttu-id="a1224-167">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a1224-167">In Global Catalog</span></span>      | <span data-ttu-id="a1224-168">Faux</span><span class="sxs-lookup"><span data-stu-id="a1224-168">False</span></span>                                                                                   |
| <span data-ttu-id="a1224-169">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a1224-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="a1224-170">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a1224-170">O:BAG:BAD:S:</span></span>                                                                            |
| <span data-ttu-id="a1224-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a1224-171">Range-Lower</span></span>            | \-                                                                                      |
| <span data-ttu-id="a1224-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a1224-172">Range-Upper</span></span>            | \-                                                                                      |
| <span data-ttu-id="a1224-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a1224-173">Search-Flags</span></span>           | <span data-ttu-id="a1224-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a1224-174">0x00000000</span></span>                                                                              |
| <span data-ttu-id="a1224-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a1224-175">System-Flags</span></span>           | <span data-ttu-id="a1224-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a1224-176">0x00000010</span></span>                                                                              |
| <span data-ttu-id="a1224-177">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a1224-177">Classes used in</span></span>        | [<span data-ttu-id="a1224-178">**Référence croisée**</span><span class="sxs-lookup"><span data-stu-id="a1224-178">**Cross-Ref**</span></span>](c-crossref.md)<br/> [<span data-ttu-id="a1224-179">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="a1224-179">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a1224-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a1224-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a1224-181">Entrée</span><span class="sxs-lookup"><span data-stu-id="a1224-181">Entry</span></span> | <span data-ttu-id="a1224-182">Valeur</span><span class="sxs-lookup"><span data-stu-id="a1224-182">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1224-183">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a1224-183">Link-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="a1224-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a1224-184">MAPI-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="a1224-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="a1224-185">System-Only</span></span>            | <span data-ttu-id="a1224-186">Faux</span><span class="sxs-lookup"><span data-stu-id="a1224-186">False</span></span>                                                                                   |
| <span data-ttu-id="a1224-187">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a1224-187">Is-Single-Valued</span></span>       | <span data-ttu-id="a1224-188">Vrai</span><span class="sxs-lookup"><span data-stu-id="a1224-188">True</span></span>                                                                                    |
| <span data-ttu-id="a1224-189">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a1224-189">Is Indexed</span></span>             | <span data-ttu-id="a1224-190">Faux</span><span class="sxs-lookup"><span data-stu-id="a1224-190">False</span></span>                                                                                   |
| <span data-ttu-id="a1224-191">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a1224-191">In Global Catalog</span></span>      | <span data-ttu-id="a1224-192">Faux</span><span class="sxs-lookup"><span data-stu-id="a1224-192">False</span></span>                                                                                   |
| <span data-ttu-id="a1224-193">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a1224-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="a1224-194">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a1224-194">O:BAG:BAD:S:</span></span>                                                                            |
| <span data-ttu-id="a1224-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a1224-195">Range-Lower</span></span>            | \-                                                                                      |
| <span data-ttu-id="a1224-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a1224-196">Range-Upper</span></span>            | \-                                                                                      |
| <span data-ttu-id="a1224-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a1224-197">Search-Flags</span></span>           | <span data-ttu-id="a1224-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a1224-198">0x00000000</span></span>                                                                              |
| <span data-ttu-id="a1224-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a1224-199">System-Flags</span></span>           | <span data-ttu-id="a1224-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a1224-200">0x00000010</span></span>                                                                              |
| <span data-ttu-id="a1224-201">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a1224-201">Classes used in</span></span>        | [<span data-ttu-id="a1224-202">**Référence croisée**</span><span class="sxs-lookup"><span data-stu-id="a1224-202">**Cross-Ref**</span></span>](c-crossref.md)<br/> [<span data-ttu-id="a1224-203">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="a1224-203">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a1224-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a1224-204">Windows Server 2008</span></span>



| <span data-ttu-id="a1224-205">Entrée</span><span class="sxs-lookup"><span data-stu-id="a1224-205">Entry</span></span> | <span data-ttu-id="a1224-206">Valeur</span><span class="sxs-lookup"><span data-stu-id="a1224-206">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1224-207">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a1224-207">Link-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="a1224-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a1224-208">MAPI-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="a1224-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="a1224-209">System-Only</span></span>            | <span data-ttu-id="a1224-210">Faux</span><span class="sxs-lookup"><span data-stu-id="a1224-210">False</span></span>                                                                                   |
| <span data-ttu-id="a1224-211">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a1224-211">Is-Single-Valued</span></span>       | <span data-ttu-id="a1224-212">Vrai</span><span class="sxs-lookup"><span data-stu-id="a1224-212">True</span></span>                                                                                    |
| <span data-ttu-id="a1224-213">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a1224-213">Is Indexed</span></span>             | <span data-ttu-id="a1224-214">Faux</span><span class="sxs-lookup"><span data-stu-id="a1224-214">False</span></span>                                                                                   |
| <span data-ttu-id="a1224-215">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a1224-215">In Global Catalog</span></span>      | <span data-ttu-id="a1224-216">Faux</span><span class="sxs-lookup"><span data-stu-id="a1224-216">False</span></span>                                                                                   |
| <span data-ttu-id="a1224-217">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a1224-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="a1224-218">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a1224-218">O:BAG:BAD:S:</span></span>                                                                            |
| <span data-ttu-id="a1224-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a1224-219">Range-Lower</span></span>            | \-                                                                                      |
| <span data-ttu-id="a1224-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a1224-220">Range-Upper</span></span>            | \-                                                                                      |
| <span data-ttu-id="a1224-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a1224-221">Search-Flags</span></span>           | <span data-ttu-id="a1224-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a1224-222">0x00000000</span></span>                                                                              |
| <span data-ttu-id="a1224-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a1224-223">System-Flags</span></span>           | <span data-ttu-id="a1224-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a1224-224">0x00000010</span></span>                                                                              |
| <span data-ttu-id="a1224-225">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a1224-225">Classes used in</span></span>        | [<span data-ttu-id="a1224-226">**Référence croisée**</span><span class="sxs-lookup"><span data-stu-id="a1224-226">**Cross-Ref**</span></span>](c-crossref.md)<br/> [<span data-ttu-id="a1224-227">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="a1224-227">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a1224-228">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a1224-228">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a1224-229">Entrée</span><span class="sxs-lookup"><span data-stu-id="a1224-229">Entry</span></span> | <span data-ttu-id="a1224-230">Valeur</span><span class="sxs-lookup"><span data-stu-id="a1224-230">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1224-231">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a1224-231">Link-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="a1224-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a1224-232">MAPI-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="a1224-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="a1224-233">System-Only</span></span>            | <span data-ttu-id="a1224-234">Faux</span><span class="sxs-lookup"><span data-stu-id="a1224-234">False</span></span>                                                                                   |
| <span data-ttu-id="a1224-235">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a1224-235">Is-Single-Valued</span></span>       | <span data-ttu-id="a1224-236">Vrai</span><span class="sxs-lookup"><span data-stu-id="a1224-236">True</span></span>                                                                                    |
| <span data-ttu-id="a1224-237">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a1224-237">Is Indexed</span></span>             | <span data-ttu-id="a1224-238">Faux</span><span class="sxs-lookup"><span data-stu-id="a1224-238">False</span></span>                                                                                   |
| <span data-ttu-id="a1224-239">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a1224-239">In Global Catalog</span></span>      | <span data-ttu-id="a1224-240">Faux</span><span class="sxs-lookup"><span data-stu-id="a1224-240">False</span></span>                                                                                   |
| <span data-ttu-id="a1224-241">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a1224-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="a1224-242">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a1224-242">O:BAG:BAD:S:</span></span>                                                                            |
| <span data-ttu-id="a1224-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a1224-243">Range-Lower</span></span>            | \-                                                                                      |
| <span data-ttu-id="a1224-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a1224-244">Range-Upper</span></span>            | \-                                                                                      |
| <span data-ttu-id="a1224-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a1224-245">Search-Flags</span></span>           | <span data-ttu-id="a1224-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a1224-246">0x00000000</span></span>                                                                              |
| <span data-ttu-id="a1224-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a1224-247">System-Flags</span></span>           | <span data-ttu-id="a1224-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a1224-248">0x00000010</span></span>                                                                              |
| <span data-ttu-id="a1224-249">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a1224-249">Classes used in</span></span>        | [<span data-ttu-id="a1224-250">**Référence croisée**</span><span class="sxs-lookup"><span data-stu-id="a1224-250">**Cross-Ref**</span></span>](c-crossref.md)<br/> [<span data-ttu-id="a1224-251">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="a1224-251">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a1224-252">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a1224-252">Windows Server 2012</span></span>



| <span data-ttu-id="a1224-253">Entrée</span><span class="sxs-lookup"><span data-stu-id="a1224-253">Entry</span></span> | <span data-ttu-id="a1224-254">Valeur</span><span class="sxs-lookup"><span data-stu-id="a1224-254">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1224-255">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a1224-255">Link-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="a1224-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a1224-256">MAPI-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="a1224-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="a1224-257">System-Only</span></span>            | <span data-ttu-id="a1224-258">Faux</span><span class="sxs-lookup"><span data-stu-id="a1224-258">False</span></span>                                                                                   |
| <span data-ttu-id="a1224-259">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a1224-259">Is-Single-Valued</span></span>       | <span data-ttu-id="a1224-260">Vrai</span><span class="sxs-lookup"><span data-stu-id="a1224-260">True</span></span>                                                                                    |
| <span data-ttu-id="a1224-261">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a1224-261">Is Indexed</span></span>             | <span data-ttu-id="a1224-262">Faux</span><span class="sxs-lookup"><span data-stu-id="a1224-262">False</span></span>                                                                                   |
| <span data-ttu-id="a1224-263">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a1224-263">In Global Catalog</span></span>      | <span data-ttu-id="a1224-264">Faux</span><span class="sxs-lookup"><span data-stu-id="a1224-264">False</span></span>                                                                                   |
| <span data-ttu-id="a1224-265">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a1224-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="a1224-266">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a1224-266">O:BAG:BAD:S:</span></span>                                                                            |
| <span data-ttu-id="a1224-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a1224-267">Range-Lower</span></span>            | \-                                                                                      |
| <span data-ttu-id="a1224-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a1224-268">Range-Upper</span></span>            | \-                                                                                      |
| <span data-ttu-id="a1224-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a1224-269">Search-Flags</span></span>           | <span data-ttu-id="a1224-270">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a1224-270">0x00000000</span></span>                                                                              |
| <span data-ttu-id="a1224-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a1224-271">System-Flags</span></span>           | <span data-ttu-id="a1224-272">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a1224-272">0x00000010</span></span>                                                                              |
| <span data-ttu-id="a1224-273">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a1224-273">Classes used in</span></span>        | [<span data-ttu-id="a1224-274">**Référence croisée**</span><span class="sxs-lookup"><span data-stu-id="a1224-274">**Cross-Ref**</span></span>](c-crossref.md)<br/> [<span data-ttu-id="a1224-275">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="a1224-275">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 





