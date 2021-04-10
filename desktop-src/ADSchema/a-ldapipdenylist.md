---
title: Attribut LDAP-IPDeny-List
description: Contient une liste d’adresses IP binaires auxquelles l’accès à un serveur LDAP est refusé.
ms.assetid: 7d554d49-8934-4d71-b32f-8e59c22faf8c
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut LDAP-IPDeny-List
- Schéma AD de l’attribut lDAPIPDenyList
topic_type:
- apiref
api_name:
- LDAP-IPDeny-List
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43246b5bb5786eefafc8598e9d729d9a2f308e08
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107894"
---
# <a name="ldap-ipdeny-list-attribute"></a><span data-ttu-id="59fd3-105">Attribut LDAP-IPDeny-List</span><span class="sxs-lookup"><span data-stu-id="59fd3-105">LDAP-IPDeny-List attribute</span></span>

<span data-ttu-id="59fd3-106">Contient une liste d’adresses IP binaires auxquelles l’accès à un serveur LDAP est refusé.</span><span class="sxs-lookup"><span data-stu-id="59fd3-106">Holds a list of binary IP addresses that are denied access to an LDAP server.</span></span>



| <span data-ttu-id="59fd3-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="59fd3-107">Entry</span></span> | <span data-ttu-id="59fd3-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="59fd3-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="59fd3-109">CN</span><span class="sxs-lookup"><span data-stu-id="59fd3-109">CN</span></span>                | <span data-ttu-id="59fd3-110">LDAP-IPDeny-List</span><span class="sxs-lookup"><span data-stu-id="59fd3-110">LDAP-IPDeny-List</span></span>                                      |
| <span data-ttu-id="59fd3-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="59fd3-111">Ldap-Display-Name</span></span> | <span data-ttu-id="59fd3-112">lDAPIPDenyList</span><span class="sxs-lookup"><span data-stu-id="59fd3-112">lDAPIPDenyList</span></span>                                        |
| <span data-ttu-id="59fd3-113">Taille</span><span class="sxs-lookup"><span data-stu-id="59fd3-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="59fd3-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="59fd3-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="59fd3-115">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="59fd3-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="59fd3-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="59fd3-116">Attribute-Id</span></span>      | <span data-ttu-id="59fd3-117">1.2.840.113556.1.4.844</span><span class="sxs-lookup"><span data-stu-id="59fd3-117">1.2.840.113556.1.4.844</span></span>                                |
| <span data-ttu-id="59fd3-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="59fd3-118">System-Id-Guid</span></span>    | <span data-ttu-id="59fd3-119">7359a353-90f7-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="59fd3-119">7359a353-90f7-11d1-aebc-0000f80367c1</span></span>                  |
| <span data-ttu-id="59fd3-120">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="59fd3-120">Syntax</span></span>            | [<span data-ttu-id="59fd3-121">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="59fd3-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="59fd3-122">Implémentations</span><span class="sxs-lookup"><span data-stu-id="59fd3-122">Implementations</span></span>

-   [<span data-ttu-id="59fd3-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="59fd3-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="59fd3-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="59fd3-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="59fd3-125">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="59fd3-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="59fd3-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="59fd3-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="59fd3-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="59fd3-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="59fd3-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="59fd3-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="59fd3-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="59fd3-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="59fd3-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="59fd3-130">Windows 2000 Server</span></span>



| <span data-ttu-id="59fd3-131">Entrée</span><span class="sxs-lookup"><span data-stu-id="59fd3-131">Entry</span></span> | <span data-ttu-id="59fd3-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="59fd3-132">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="59fd3-133">ID de lien</span><span class="sxs-lookup"><span data-stu-id="59fd3-133">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="59fd3-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="59fd3-134">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="59fd3-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="59fd3-135">System-Only</span></span>            | <span data-ttu-id="59fd3-136">Faux</span><span class="sxs-lookup"><span data-stu-id="59fd3-136">False</span></span>                                            |
| <span data-ttu-id="59fd3-137">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="59fd3-137">Is-Single-Valued</span></span>       | <span data-ttu-id="59fd3-138">Faux</span><span class="sxs-lookup"><span data-stu-id="59fd3-138">False</span></span>                                            |
| <span data-ttu-id="59fd3-139">Est indexé</span><span class="sxs-lookup"><span data-stu-id="59fd3-139">Is Indexed</span></span>             | <span data-ttu-id="59fd3-140">Faux</span><span class="sxs-lookup"><span data-stu-id="59fd3-140">False</span></span>                                            |
| <span data-ttu-id="59fd3-141">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="59fd3-141">In Global Catalog</span></span>      | <span data-ttu-id="59fd3-142">Faux</span><span class="sxs-lookup"><span data-stu-id="59fd3-142">False</span></span>                                            |
| <span data-ttu-id="59fd3-143">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="59fd3-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="59fd3-144">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="59fd3-144">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="59fd3-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="59fd3-145">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="59fd3-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="59fd3-146">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="59fd3-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="59fd3-147">Search-Flags</span></span>           | <span data-ttu-id="59fd3-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="59fd3-148">0x00000000</span></span>                                       |
| <span data-ttu-id="59fd3-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="59fd3-149">System-Flags</span></span>           | <span data-ttu-id="59fd3-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="59fd3-150">0x00000010</span></span>                                       |
| <span data-ttu-id="59fd3-151">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="59fd3-151">Classes used in</span></span>        | [<span data-ttu-id="59fd3-152">**Requête-stratégie**</span><span class="sxs-lookup"><span data-stu-id="59fd3-152">**Query-Policy**</span></span>](c-querypolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="59fd3-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="59fd3-153">Windows Server 2003</span></span>



| <span data-ttu-id="59fd3-154">Entrée</span><span class="sxs-lookup"><span data-stu-id="59fd3-154">Entry</span></span> | <span data-ttu-id="59fd3-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="59fd3-155">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="59fd3-156">ID de lien</span><span class="sxs-lookup"><span data-stu-id="59fd3-156">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="59fd3-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="59fd3-157">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="59fd3-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="59fd3-158">System-Only</span></span>            | <span data-ttu-id="59fd3-159">Faux</span><span class="sxs-lookup"><span data-stu-id="59fd3-159">False</span></span>                                            |
| <span data-ttu-id="59fd3-160">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="59fd3-160">Is-Single-Valued</span></span>       | <span data-ttu-id="59fd3-161">Faux</span><span class="sxs-lookup"><span data-stu-id="59fd3-161">False</span></span>                                            |
| <span data-ttu-id="59fd3-162">Est indexé</span><span class="sxs-lookup"><span data-stu-id="59fd3-162">Is Indexed</span></span>             | <span data-ttu-id="59fd3-163">Faux</span><span class="sxs-lookup"><span data-stu-id="59fd3-163">False</span></span>                                            |
| <span data-ttu-id="59fd3-164">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="59fd3-164">In Global Catalog</span></span>      | <span data-ttu-id="59fd3-165">Faux</span><span class="sxs-lookup"><span data-stu-id="59fd3-165">False</span></span>                                            |
| <span data-ttu-id="59fd3-166">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="59fd3-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="59fd3-167">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="59fd3-167">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="59fd3-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="59fd3-168">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="59fd3-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="59fd3-169">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="59fd3-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="59fd3-170">Search-Flags</span></span>           | <span data-ttu-id="59fd3-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="59fd3-171">0x00000000</span></span>                                       |
| <span data-ttu-id="59fd3-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="59fd3-172">System-Flags</span></span>           | <span data-ttu-id="59fd3-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="59fd3-173">0x00000010</span></span>                                       |
| <span data-ttu-id="59fd3-174">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="59fd3-174">Classes used in</span></span>        | [<span data-ttu-id="59fd3-175">**Requête-stratégie**</span><span class="sxs-lookup"><span data-stu-id="59fd3-175">**Query-Policy**</span></span>](c-querypolicy.md)<br/> |



## <a name="adam"></a><span data-ttu-id="59fd3-176">ADAM</span><span class="sxs-lookup"><span data-stu-id="59fd3-176">ADAM</span></span>



| <span data-ttu-id="59fd3-177">Entrée</span><span class="sxs-lookup"><span data-stu-id="59fd3-177">Entry</span></span> | <span data-ttu-id="59fd3-178">Valeur</span><span class="sxs-lookup"><span data-stu-id="59fd3-178">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="59fd3-179">ID de lien</span><span class="sxs-lookup"><span data-stu-id="59fd3-179">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="59fd3-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="59fd3-180">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="59fd3-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="59fd3-181">System-Only</span></span>            | <span data-ttu-id="59fd3-182">Faux</span><span class="sxs-lookup"><span data-stu-id="59fd3-182">False</span></span>                                            |
| <span data-ttu-id="59fd3-183">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="59fd3-183">Is-Single-Valued</span></span>       | <span data-ttu-id="59fd3-184">Faux</span><span class="sxs-lookup"><span data-stu-id="59fd3-184">False</span></span>                                            |
| <span data-ttu-id="59fd3-185">Est indexé</span><span class="sxs-lookup"><span data-stu-id="59fd3-185">Is Indexed</span></span>             | <span data-ttu-id="59fd3-186">Faux</span><span class="sxs-lookup"><span data-stu-id="59fd3-186">False</span></span>                                            |
| <span data-ttu-id="59fd3-187">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="59fd3-187">In Global Catalog</span></span>      | <span data-ttu-id="59fd3-188">Faux</span><span class="sxs-lookup"><span data-stu-id="59fd3-188">False</span></span>                                            |
| <span data-ttu-id="59fd3-189">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="59fd3-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="59fd3-190">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="59fd3-190">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="59fd3-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="59fd3-191">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="59fd3-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="59fd3-192">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="59fd3-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="59fd3-193">Search-Flags</span></span>           | <span data-ttu-id="59fd3-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="59fd3-194">0x00000000</span></span>                                       |
| <span data-ttu-id="59fd3-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="59fd3-195">System-Flags</span></span>           | <span data-ttu-id="59fd3-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="59fd3-196">0x00000010</span></span>                                       |
| <span data-ttu-id="59fd3-197">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="59fd3-197">Classes used in</span></span>        | [<span data-ttu-id="59fd3-198">**Requête-stratégie**</span><span class="sxs-lookup"><span data-stu-id="59fd3-198">**Query-Policy**</span></span>](c-querypolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="59fd3-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="59fd3-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="59fd3-200">Entrée</span><span class="sxs-lookup"><span data-stu-id="59fd3-200">Entry</span></span> | <span data-ttu-id="59fd3-201">Valeur</span><span class="sxs-lookup"><span data-stu-id="59fd3-201">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="59fd3-202">ID de lien</span><span class="sxs-lookup"><span data-stu-id="59fd3-202">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="59fd3-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="59fd3-203">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="59fd3-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="59fd3-204">System-Only</span></span>            | <span data-ttu-id="59fd3-205">Faux</span><span class="sxs-lookup"><span data-stu-id="59fd3-205">False</span></span>                                            |
| <span data-ttu-id="59fd3-206">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="59fd3-206">Is-Single-Valued</span></span>       | <span data-ttu-id="59fd3-207">Faux</span><span class="sxs-lookup"><span data-stu-id="59fd3-207">False</span></span>                                            |
| <span data-ttu-id="59fd3-208">Est indexé</span><span class="sxs-lookup"><span data-stu-id="59fd3-208">Is Indexed</span></span>             | <span data-ttu-id="59fd3-209">Faux</span><span class="sxs-lookup"><span data-stu-id="59fd3-209">False</span></span>                                            |
| <span data-ttu-id="59fd3-210">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="59fd3-210">In Global Catalog</span></span>      | <span data-ttu-id="59fd3-211">Faux</span><span class="sxs-lookup"><span data-stu-id="59fd3-211">False</span></span>                                            |
| <span data-ttu-id="59fd3-212">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="59fd3-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="59fd3-213">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="59fd3-213">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="59fd3-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="59fd3-214">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="59fd3-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="59fd3-215">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="59fd3-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="59fd3-216">Search-Flags</span></span>           | <span data-ttu-id="59fd3-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="59fd3-217">0x00000000</span></span>                                       |
| <span data-ttu-id="59fd3-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="59fd3-218">System-Flags</span></span>           | <span data-ttu-id="59fd3-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="59fd3-219">0x00000010</span></span>                                       |
| <span data-ttu-id="59fd3-220">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="59fd3-220">Classes used in</span></span>        | [<span data-ttu-id="59fd3-221">**Requête-stratégie**</span><span class="sxs-lookup"><span data-stu-id="59fd3-221">**Query-Policy**</span></span>](c-querypolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="59fd3-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="59fd3-222">Windows Server 2008</span></span>



| <span data-ttu-id="59fd3-223">Entrée</span><span class="sxs-lookup"><span data-stu-id="59fd3-223">Entry</span></span> | <span data-ttu-id="59fd3-224">Valeur</span><span class="sxs-lookup"><span data-stu-id="59fd3-224">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="59fd3-225">ID de lien</span><span class="sxs-lookup"><span data-stu-id="59fd3-225">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="59fd3-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="59fd3-226">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="59fd3-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="59fd3-227">System-Only</span></span>            | <span data-ttu-id="59fd3-228">Faux</span><span class="sxs-lookup"><span data-stu-id="59fd3-228">False</span></span>                                            |
| <span data-ttu-id="59fd3-229">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="59fd3-229">Is-Single-Valued</span></span>       | <span data-ttu-id="59fd3-230">Faux</span><span class="sxs-lookup"><span data-stu-id="59fd3-230">False</span></span>                                            |
| <span data-ttu-id="59fd3-231">Est indexé</span><span class="sxs-lookup"><span data-stu-id="59fd3-231">Is Indexed</span></span>             | <span data-ttu-id="59fd3-232">Faux</span><span class="sxs-lookup"><span data-stu-id="59fd3-232">False</span></span>                                            |
| <span data-ttu-id="59fd3-233">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="59fd3-233">In Global Catalog</span></span>      | <span data-ttu-id="59fd3-234">Faux</span><span class="sxs-lookup"><span data-stu-id="59fd3-234">False</span></span>                                            |
| <span data-ttu-id="59fd3-235">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="59fd3-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="59fd3-236">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="59fd3-236">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="59fd3-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="59fd3-237">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="59fd3-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="59fd3-238">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="59fd3-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="59fd3-239">Search-Flags</span></span>           | <span data-ttu-id="59fd3-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="59fd3-240">0x00000000</span></span>                                       |
| <span data-ttu-id="59fd3-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="59fd3-241">System-Flags</span></span>           | <span data-ttu-id="59fd3-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="59fd3-242">0x00000010</span></span>                                       |
| <span data-ttu-id="59fd3-243">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="59fd3-243">Classes used in</span></span>        | [<span data-ttu-id="59fd3-244">**Requête-stratégie**</span><span class="sxs-lookup"><span data-stu-id="59fd3-244">**Query-Policy**</span></span>](c-querypolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="59fd3-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="59fd3-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="59fd3-246">Entrée</span><span class="sxs-lookup"><span data-stu-id="59fd3-246">Entry</span></span> | <span data-ttu-id="59fd3-247">Valeur</span><span class="sxs-lookup"><span data-stu-id="59fd3-247">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="59fd3-248">ID de lien</span><span class="sxs-lookup"><span data-stu-id="59fd3-248">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="59fd3-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="59fd3-249">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="59fd3-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="59fd3-250">System-Only</span></span>            | <span data-ttu-id="59fd3-251">Faux</span><span class="sxs-lookup"><span data-stu-id="59fd3-251">False</span></span>                                            |
| <span data-ttu-id="59fd3-252">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="59fd3-252">Is-Single-Valued</span></span>       | <span data-ttu-id="59fd3-253">Faux</span><span class="sxs-lookup"><span data-stu-id="59fd3-253">False</span></span>                                            |
| <span data-ttu-id="59fd3-254">Est indexé</span><span class="sxs-lookup"><span data-stu-id="59fd3-254">Is Indexed</span></span>             | <span data-ttu-id="59fd3-255">Faux</span><span class="sxs-lookup"><span data-stu-id="59fd3-255">False</span></span>                                            |
| <span data-ttu-id="59fd3-256">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="59fd3-256">In Global Catalog</span></span>      | <span data-ttu-id="59fd3-257">Faux</span><span class="sxs-lookup"><span data-stu-id="59fd3-257">False</span></span>                                            |
| <span data-ttu-id="59fd3-258">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="59fd3-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="59fd3-259">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="59fd3-259">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="59fd3-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="59fd3-260">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="59fd3-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="59fd3-261">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="59fd3-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="59fd3-262">Search-Flags</span></span>           | <span data-ttu-id="59fd3-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="59fd3-263">0x00000000</span></span>                                       |
| <span data-ttu-id="59fd3-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="59fd3-264">System-Flags</span></span>           | <span data-ttu-id="59fd3-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="59fd3-265">0x00000010</span></span>                                       |
| <span data-ttu-id="59fd3-266">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="59fd3-266">Classes used in</span></span>        | [<span data-ttu-id="59fd3-267">**Requête-stratégie**</span><span class="sxs-lookup"><span data-stu-id="59fd3-267">**Query-Policy**</span></span>](c-querypolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="59fd3-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="59fd3-268">Windows Server 2012</span></span>



| <span data-ttu-id="59fd3-269">Entrée</span><span class="sxs-lookup"><span data-stu-id="59fd3-269">Entry</span></span> | <span data-ttu-id="59fd3-270">Valeur</span><span class="sxs-lookup"><span data-stu-id="59fd3-270">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="59fd3-271">ID de lien</span><span class="sxs-lookup"><span data-stu-id="59fd3-271">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="59fd3-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="59fd3-272">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="59fd3-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="59fd3-273">System-Only</span></span>            | <span data-ttu-id="59fd3-274">Faux</span><span class="sxs-lookup"><span data-stu-id="59fd3-274">False</span></span>                                            |
| <span data-ttu-id="59fd3-275">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="59fd3-275">Is-Single-Valued</span></span>       | <span data-ttu-id="59fd3-276">Faux</span><span class="sxs-lookup"><span data-stu-id="59fd3-276">False</span></span>                                            |
| <span data-ttu-id="59fd3-277">Est indexé</span><span class="sxs-lookup"><span data-stu-id="59fd3-277">Is Indexed</span></span>             | <span data-ttu-id="59fd3-278">Faux</span><span class="sxs-lookup"><span data-stu-id="59fd3-278">False</span></span>                                            |
| <span data-ttu-id="59fd3-279">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="59fd3-279">In Global Catalog</span></span>      | <span data-ttu-id="59fd3-280">Faux</span><span class="sxs-lookup"><span data-stu-id="59fd3-280">False</span></span>                                            |
| <span data-ttu-id="59fd3-281">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="59fd3-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="59fd3-282">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="59fd3-282">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="59fd3-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="59fd3-283">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="59fd3-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="59fd3-284">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="59fd3-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="59fd3-285">Search-Flags</span></span>           | <span data-ttu-id="59fd3-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="59fd3-286">0x00000000</span></span>                                       |
| <span data-ttu-id="59fd3-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="59fd3-287">System-Flags</span></span>           | <span data-ttu-id="59fd3-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="59fd3-288">0x00000010</span></span>                                       |
| <span data-ttu-id="59fd3-289">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="59fd3-289">Classes used in</span></span>        | [<span data-ttu-id="59fd3-290">**Requête-stratégie**</span><span class="sxs-lookup"><span data-stu-id="59fd3-290">**Query-Policy**</span></span>](c-querypolicy.md)<br/> |



 

 





