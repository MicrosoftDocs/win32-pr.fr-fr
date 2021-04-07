---
title: attribut ms-DS-DnsRootAlias
description: Utilisé pour stocker l’alias de domaine.
ms.assetid: 36b64363-947f-4af9-947f-eefead55bb02
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut ms-DS-DnsRootAlias
- Schéma Active Directory de l’attribut msDS-DnsRootAlias
topic_type:
- apiref
api_name:
- ms-DS-DnsRootAlias
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f0b20b9316aaa9e68ab1ed907135c5640c1480f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103745172"
---
# <a name="ms-ds-dnsrootalias-attribute"></a><span data-ttu-id="e0429-105">attribut ms-DS-DnsRootAlias</span><span class="sxs-lookup"><span data-stu-id="e0429-105">ms-DS-DnsRootAlias attribute</span></span>

<span data-ttu-id="e0429-106">Utilisé pour stocker l’alias de domaine.</span><span class="sxs-lookup"><span data-stu-id="e0429-106">Used to store the domain alias.</span></span>



| <span data-ttu-id="e0429-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="e0429-107">Entry</span></span> | <span data-ttu-id="e0429-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="e0429-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="e0429-109">CN</span><span class="sxs-lookup"><span data-stu-id="e0429-109">CN</span></span>                | <span data-ttu-id="e0429-110">ms-DS-DnsRootAlias</span><span class="sxs-lookup"><span data-stu-id="e0429-110">ms-DS-DnsRootAlias</span></span>                          |
| <span data-ttu-id="e0429-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="e0429-111">Ldap-Display-Name</span></span> | <span data-ttu-id="e0429-112">msDS-DnsRootAlias</span><span class="sxs-lookup"><span data-stu-id="e0429-112">msDS-DnsRootAlias</span></span>                           |
| <span data-ttu-id="e0429-113">Taille</span><span class="sxs-lookup"><span data-stu-id="e0429-113">Size</span></span>              | <span data-ttu-id="e0429-114">Taille maximale de 255 octets.</span><span class="sxs-lookup"><span data-stu-id="e0429-114">Maximum size 255 bytes.</span></span>                     |
| <span data-ttu-id="e0429-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="e0429-115">Update Privilege</span></span>  | <span data-ttu-id="e0429-116">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="e0429-116">This value is set by the system.</span></span>            |
| <span data-ttu-id="e0429-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="e0429-117">Update Frequency</span></span>  | <span data-ttu-id="e0429-118">Uniquement pendant la restructuration de domaine.</span><span class="sxs-lookup"><span data-stu-id="e0429-118">Only during domain restructure.</span></span>             |
| <span data-ttu-id="e0429-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e0429-119">Attribute-Id</span></span>      | <span data-ttu-id="e0429-120">1.2.840.113556.1.4.1719</span><span class="sxs-lookup"><span data-stu-id="e0429-120">1.2.840.113556.1.4.1719</span></span>                     |
| <span data-ttu-id="e0429-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="e0429-121">System-Id-Guid</span></span>    | <span data-ttu-id="e0429-122">2143acca-eead-4d29-b591-85fa49ce9173</span><span class="sxs-lookup"><span data-stu-id="e0429-122">2143acca-eead-4d29-b591-85fa49ce9173</span></span>        |
| <span data-ttu-id="e0429-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e0429-123">Syntax</span></span>            | [<span data-ttu-id="e0429-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="e0429-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="e0429-125">Implémentations</span><span class="sxs-lookup"><span data-stu-id="e0429-125">Implementations</span></span>

-   [<span data-ttu-id="e0429-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e0429-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e0429-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="e0429-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="e0429-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e0429-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e0429-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e0429-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e0429-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e0429-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e0429-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e0429-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="e0429-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e0429-132">Windows Server 2003</span></span>



| <span data-ttu-id="e0429-133">Entrée</span><span class="sxs-lookup"><span data-stu-id="e0429-133">Entry</span></span> | <span data-ttu-id="e0429-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="e0429-134">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="e0429-135">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e0429-135">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="e0429-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e0429-136">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="e0429-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="e0429-137">System-Only</span></span>            | <span data-ttu-id="e0429-138">Faux</span><span class="sxs-lookup"><span data-stu-id="e0429-138">False</span></span>                                      |
| <span data-ttu-id="e0429-139">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e0429-139">Is-Single-Valued</span></span>       | <span data-ttu-id="e0429-140">Vrai</span><span class="sxs-lookup"><span data-stu-id="e0429-140">True</span></span>                                       |
| <span data-ttu-id="e0429-141">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e0429-141">Is Indexed</span></span>             | <span data-ttu-id="e0429-142">Faux</span><span class="sxs-lookup"><span data-stu-id="e0429-142">False</span></span>                                      |
| <span data-ttu-id="e0429-143">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e0429-143">In Global Catalog</span></span>      | <span data-ttu-id="e0429-144">Faux</span><span class="sxs-lookup"><span data-stu-id="e0429-144">False</span></span>                                      |
| <span data-ttu-id="e0429-145">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e0429-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="e0429-146">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e0429-146">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="e0429-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e0429-147">Range-Lower</span></span>            | <span data-ttu-id="e0429-148">0</span><span class="sxs-lookup"><span data-stu-id="e0429-148">0</span></span>                                          |
| <span data-ttu-id="e0429-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e0429-149">Range-Upper</span></span>            | <span data-ttu-id="e0429-150">255</span><span class="sxs-lookup"><span data-stu-id="e0429-150">255</span></span>                                        |
| <span data-ttu-id="e0429-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e0429-151">Search-Flags</span></span>           | <span data-ttu-id="e0429-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e0429-152">0x00000000</span></span>                                 |
| <span data-ttu-id="e0429-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e0429-153">System-Flags</span></span>           | <span data-ttu-id="e0429-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e0429-154">0x00000010</span></span>                                 |
| <span data-ttu-id="e0429-155">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e0429-155">Classes used in</span></span>        | [<span data-ttu-id="e0429-156">**Référence croisée**</span><span class="sxs-lookup"><span data-stu-id="e0429-156">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="adam"></a><span data-ttu-id="e0429-157">ADAM</span><span class="sxs-lookup"><span data-stu-id="e0429-157">ADAM</span></span>



| <span data-ttu-id="e0429-158">Entrée</span><span class="sxs-lookup"><span data-stu-id="e0429-158">Entry</span></span> | <span data-ttu-id="e0429-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="e0429-159">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="e0429-160">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e0429-160">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="e0429-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e0429-161">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="e0429-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="e0429-162">System-Only</span></span>            | <span data-ttu-id="e0429-163">Faux</span><span class="sxs-lookup"><span data-stu-id="e0429-163">False</span></span>                                      |
| <span data-ttu-id="e0429-164">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e0429-164">Is-Single-Valued</span></span>       | <span data-ttu-id="e0429-165">Vrai</span><span class="sxs-lookup"><span data-stu-id="e0429-165">True</span></span>                                       |
| <span data-ttu-id="e0429-166">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e0429-166">Is Indexed</span></span>             | <span data-ttu-id="e0429-167">Faux</span><span class="sxs-lookup"><span data-stu-id="e0429-167">False</span></span>                                      |
| <span data-ttu-id="e0429-168">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e0429-168">In Global Catalog</span></span>      | <span data-ttu-id="e0429-169">Faux</span><span class="sxs-lookup"><span data-stu-id="e0429-169">False</span></span>                                      |
| <span data-ttu-id="e0429-170">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e0429-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="e0429-171">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e0429-171">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="e0429-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e0429-172">Range-Lower</span></span>            | <span data-ttu-id="e0429-173">0</span><span class="sxs-lookup"><span data-stu-id="e0429-173">0</span></span>                                          |
| <span data-ttu-id="e0429-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e0429-174">Range-Upper</span></span>            | <span data-ttu-id="e0429-175">255</span><span class="sxs-lookup"><span data-stu-id="e0429-175">255</span></span>                                        |
| <span data-ttu-id="e0429-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e0429-176">Search-Flags</span></span>           | <span data-ttu-id="e0429-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e0429-177">0x00000000</span></span>                                 |
| <span data-ttu-id="e0429-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e0429-178">System-Flags</span></span>           | <span data-ttu-id="e0429-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e0429-179">0x00000010</span></span>                                 |
| <span data-ttu-id="e0429-180">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e0429-180">Classes used in</span></span>        | [<span data-ttu-id="e0429-181">**Référence croisée**</span><span class="sxs-lookup"><span data-stu-id="e0429-181">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e0429-182">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e0429-182">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e0429-183">Entrée</span><span class="sxs-lookup"><span data-stu-id="e0429-183">Entry</span></span> | <span data-ttu-id="e0429-184">Valeur</span><span class="sxs-lookup"><span data-stu-id="e0429-184">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="e0429-185">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e0429-185">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="e0429-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e0429-186">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="e0429-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="e0429-187">System-Only</span></span>            | <span data-ttu-id="e0429-188">Faux</span><span class="sxs-lookup"><span data-stu-id="e0429-188">False</span></span>                                      |
| <span data-ttu-id="e0429-189">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e0429-189">Is-Single-Valued</span></span>       | <span data-ttu-id="e0429-190">Vrai</span><span class="sxs-lookup"><span data-stu-id="e0429-190">True</span></span>                                       |
| <span data-ttu-id="e0429-191">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e0429-191">Is Indexed</span></span>             | <span data-ttu-id="e0429-192">Faux</span><span class="sxs-lookup"><span data-stu-id="e0429-192">False</span></span>                                      |
| <span data-ttu-id="e0429-193">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e0429-193">In Global Catalog</span></span>      | <span data-ttu-id="e0429-194">Faux</span><span class="sxs-lookup"><span data-stu-id="e0429-194">False</span></span>                                      |
| <span data-ttu-id="e0429-195">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e0429-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="e0429-196">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e0429-196">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="e0429-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e0429-197">Range-Lower</span></span>            | <span data-ttu-id="e0429-198">0</span><span class="sxs-lookup"><span data-stu-id="e0429-198">0</span></span>                                          |
| <span data-ttu-id="e0429-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e0429-199">Range-Upper</span></span>            | <span data-ttu-id="e0429-200">255</span><span class="sxs-lookup"><span data-stu-id="e0429-200">255</span></span>                                        |
| <span data-ttu-id="e0429-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e0429-201">Search-Flags</span></span>           | <span data-ttu-id="e0429-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e0429-202">0x00000000</span></span>                                 |
| <span data-ttu-id="e0429-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e0429-203">System-Flags</span></span>           | <span data-ttu-id="e0429-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e0429-204">0x00000010</span></span>                                 |
| <span data-ttu-id="e0429-205">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e0429-205">Classes used in</span></span>        | [<span data-ttu-id="e0429-206">**Référence croisée**</span><span class="sxs-lookup"><span data-stu-id="e0429-206">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e0429-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e0429-207">Windows Server 2008</span></span>



| <span data-ttu-id="e0429-208">Entrée</span><span class="sxs-lookup"><span data-stu-id="e0429-208">Entry</span></span> | <span data-ttu-id="e0429-209">Valeur</span><span class="sxs-lookup"><span data-stu-id="e0429-209">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="e0429-210">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e0429-210">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="e0429-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e0429-211">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="e0429-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="e0429-212">System-Only</span></span>            | <span data-ttu-id="e0429-213">Faux</span><span class="sxs-lookup"><span data-stu-id="e0429-213">False</span></span>                                      |
| <span data-ttu-id="e0429-214">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e0429-214">Is-Single-Valued</span></span>       | <span data-ttu-id="e0429-215">Vrai</span><span class="sxs-lookup"><span data-stu-id="e0429-215">True</span></span>                                       |
| <span data-ttu-id="e0429-216">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e0429-216">Is Indexed</span></span>             | <span data-ttu-id="e0429-217">Faux</span><span class="sxs-lookup"><span data-stu-id="e0429-217">False</span></span>                                      |
| <span data-ttu-id="e0429-218">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e0429-218">In Global Catalog</span></span>      | <span data-ttu-id="e0429-219">Faux</span><span class="sxs-lookup"><span data-stu-id="e0429-219">False</span></span>                                      |
| <span data-ttu-id="e0429-220">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e0429-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="e0429-221">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e0429-221">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="e0429-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e0429-222">Range-Lower</span></span>            | <span data-ttu-id="e0429-223">0</span><span class="sxs-lookup"><span data-stu-id="e0429-223">0</span></span>                                          |
| <span data-ttu-id="e0429-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e0429-224">Range-Upper</span></span>            | <span data-ttu-id="e0429-225">255</span><span class="sxs-lookup"><span data-stu-id="e0429-225">255</span></span>                                        |
| <span data-ttu-id="e0429-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e0429-226">Search-Flags</span></span>           | <span data-ttu-id="e0429-227">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e0429-227">0x00000000</span></span>                                 |
| <span data-ttu-id="e0429-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e0429-228">System-Flags</span></span>           | <span data-ttu-id="e0429-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e0429-229">0x00000010</span></span>                                 |
| <span data-ttu-id="e0429-230">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e0429-230">Classes used in</span></span>        | [<span data-ttu-id="e0429-231">**Référence croisée**</span><span class="sxs-lookup"><span data-stu-id="e0429-231">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e0429-232">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e0429-232">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e0429-233">Entrée</span><span class="sxs-lookup"><span data-stu-id="e0429-233">Entry</span></span> | <span data-ttu-id="e0429-234">Valeur</span><span class="sxs-lookup"><span data-stu-id="e0429-234">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="e0429-235">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e0429-235">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="e0429-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e0429-236">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="e0429-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="e0429-237">System-Only</span></span>            | <span data-ttu-id="e0429-238">Faux</span><span class="sxs-lookup"><span data-stu-id="e0429-238">False</span></span>                                      |
| <span data-ttu-id="e0429-239">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e0429-239">Is-Single-Valued</span></span>       | <span data-ttu-id="e0429-240">Vrai</span><span class="sxs-lookup"><span data-stu-id="e0429-240">True</span></span>                                       |
| <span data-ttu-id="e0429-241">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e0429-241">Is Indexed</span></span>             | <span data-ttu-id="e0429-242">Faux</span><span class="sxs-lookup"><span data-stu-id="e0429-242">False</span></span>                                      |
| <span data-ttu-id="e0429-243">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e0429-243">In Global Catalog</span></span>      | <span data-ttu-id="e0429-244">Faux</span><span class="sxs-lookup"><span data-stu-id="e0429-244">False</span></span>                                      |
| <span data-ttu-id="e0429-245">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e0429-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="e0429-246">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e0429-246">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="e0429-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e0429-247">Range-Lower</span></span>            | <span data-ttu-id="e0429-248">0</span><span class="sxs-lookup"><span data-stu-id="e0429-248">0</span></span>                                          |
| <span data-ttu-id="e0429-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e0429-249">Range-Upper</span></span>            | <span data-ttu-id="e0429-250">255</span><span class="sxs-lookup"><span data-stu-id="e0429-250">255</span></span>                                        |
| <span data-ttu-id="e0429-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e0429-251">Search-Flags</span></span>           | <span data-ttu-id="e0429-252">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e0429-252">0x00000000</span></span>                                 |
| <span data-ttu-id="e0429-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e0429-253">System-Flags</span></span>           | <span data-ttu-id="e0429-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e0429-254">0x00000010</span></span>                                 |
| <span data-ttu-id="e0429-255">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e0429-255">Classes used in</span></span>        | [<span data-ttu-id="e0429-256">**Référence croisée**</span><span class="sxs-lookup"><span data-stu-id="e0429-256">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e0429-257">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e0429-257">Windows Server 2012</span></span>



| <span data-ttu-id="e0429-258">Entrée</span><span class="sxs-lookup"><span data-stu-id="e0429-258">Entry</span></span> | <span data-ttu-id="e0429-259">Valeur</span><span class="sxs-lookup"><span data-stu-id="e0429-259">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="e0429-260">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e0429-260">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="e0429-261">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e0429-261">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="e0429-262">System-Only</span><span class="sxs-lookup"><span data-stu-id="e0429-262">System-Only</span></span>            | <span data-ttu-id="e0429-263">Faux</span><span class="sxs-lookup"><span data-stu-id="e0429-263">False</span></span>                                      |
| <span data-ttu-id="e0429-264">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e0429-264">Is-Single-Valued</span></span>       | <span data-ttu-id="e0429-265">Vrai</span><span class="sxs-lookup"><span data-stu-id="e0429-265">True</span></span>                                       |
| <span data-ttu-id="e0429-266">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e0429-266">Is Indexed</span></span>             | <span data-ttu-id="e0429-267">Faux</span><span class="sxs-lookup"><span data-stu-id="e0429-267">False</span></span>                                      |
| <span data-ttu-id="e0429-268">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e0429-268">In Global Catalog</span></span>      | <span data-ttu-id="e0429-269">Faux</span><span class="sxs-lookup"><span data-stu-id="e0429-269">False</span></span>                                      |
| <span data-ttu-id="e0429-270">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e0429-270">NT-Security-Descriptor</span></span> | <span data-ttu-id="e0429-271">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e0429-271">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="e0429-272">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e0429-272">Range-Lower</span></span>            | <span data-ttu-id="e0429-273">0</span><span class="sxs-lookup"><span data-stu-id="e0429-273">0</span></span>                                          |
| <span data-ttu-id="e0429-274">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e0429-274">Range-Upper</span></span>            | <span data-ttu-id="e0429-275">255</span><span class="sxs-lookup"><span data-stu-id="e0429-275">255</span></span>                                        |
| <span data-ttu-id="e0429-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e0429-276">Search-Flags</span></span>           | <span data-ttu-id="e0429-277">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e0429-277">0x00000000</span></span>                                 |
| <span data-ttu-id="e0429-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e0429-278">System-Flags</span></span>           | <span data-ttu-id="e0429-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e0429-279">0x00000010</span></span>                                 |
| <span data-ttu-id="e0429-280">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e0429-280">Classes used in</span></span>        | [<span data-ttu-id="e0429-281">**Référence croisée**</span><span class="sxs-lookup"><span data-stu-id="e0429-281">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



 

 





