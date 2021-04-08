---
title: Attribut de stratégie à l’ensemble du domaine
description: Il s’agit de la stratégie extensible utilisateur à répliquer sur les clients.
ms.assetid: 930a2733-31c4-45de-a611-437e3d61d304
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut de stratégie à l’ensemble du domaine
- Schéma AD de l’attribut domainWidePolicy
topic_type:
- apiref
api_name:
- Domain-Wide-Policy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dc732ee761ee6c294ffb14dac832c36d5821927
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744252"
---
# <a name="domain-wide-policy-attribute"></a><span data-ttu-id="091ce-105">Attribut de stratégie à l’ensemble du domaine</span><span class="sxs-lookup"><span data-stu-id="091ce-105">Domain-Wide-Policy attribute</span></span>

<span data-ttu-id="091ce-106">Il s’agit de la stratégie extensible utilisateur à répliquer sur les clients.</span><span class="sxs-lookup"><span data-stu-id="091ce-106">This is for user extensible policy to be replicated to the clients.</span></span>



| <span data-ttu-id="091ce-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="091ce-107">Entry</span></span> | <span data-ttu-id="091ce-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="091ce-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="091ce-109">CN</span><span class="sxs-lookup"><span data-stu-id="091ce-109">CN</span></span>                | <span data-ttu-id="091ce-110">Stratégie à l’ensemble du domaine</span><span class="sxs-lookup"><span data-stu-id="091ce-110">Domain-Wide-Policy</span></span>                                    |
| <span data-ttu-id="091ce-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="091ce-111">Ldap-Display-Name</span></span> | <span data-ttu-id="091ce-112">domainWidePolicy</span><span class="sxs-lookup"><span data-stu-id="091ce-112">domainWidePolicy</span></span>                                      |
| <span data-ttu-id="091ce-113">Taille</span><span class="sxs-lookup"><span data-stu-id="091ce-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="091ce-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="091ce-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="091ce-115">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="091ce-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="091ce-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="091ce-116">Attribute-Id</span></span>      | <span data-ttu-id="091ce-117">1.2.840.113556.1.4.421</span><span class="sxs-lookup"><span data-stu-id="091ce-117">1.2.840.113556.1.4.421</span></span>                                |
| <span data-ttu-id="091ce-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="091ce-118">System-Id-Guid</span></span>    | <span data-ttu-id="091ce-119">80a67e29-9f22-11d0-afdd-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="091ce-119">80a67e29-9f22-11d0-afdd-00c04fd930c9</span></span>                  |
| <span data-ttu-id="091ce-120">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="091ce-120">Syntax</span></span>            | [<span data-ttu-id="091ce-121">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="091ce-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="091ce-122">Implémentations</span><span class="sxs-lookup"><span data-stu-id="091ce-122">Implementations</span></span>

-   [<span data-ttu-id="091ce-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="091ce-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="091ce-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="091ce-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="091ce-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="091ce-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="091ce-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="091ce-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="091ce-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="091ce-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="091ce-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="091ce-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="091ce-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="091ce-129">Windows 2000 Server</span></span>



| <span data-ttu-id="091ce-130">Entrée</span><span class="sxs-lookup"><span data-stu-id="091ce-130">Entry</span></span> | <span data-ttu-id="091ce-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="091ce-131">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="091ce-132">ID de lien</span><span class="sxs-lookup"><span data-stu-id="091ce-132">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="091ce-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="091ce-133">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="091ce-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="091ce-134">System-Only</span></span>            | <span data-ttu-id="091ce-135">Faux</span><span class="sxs-lookup"><span data-stu-id="091ce-135">False</span></span>                                              |
| <span data-ttu-id="091ce-136">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="091ce-136">Is-Single-Valued</span></span>       | <span data-ttu-id="091ce-137">Faux</span><span class="sxs-lookup"><span data-stu-id="091ce-137">False</span></span>                                              |
| <span data-ttu-id="091ce-138">Est indexé</span><span class="sxs-lookup"><span data-stu-id="091ce-138">Is Indexed</span></span>             | <span data-ttu-id="091ce-139">Faux</span><span class="sxs-lookup"><span data-stu-id="091ce-139">False</span></span>                                              |
| <span data-ttu-id="091ce-140">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="091ce-140">In Global Catalog</span></span>      | <span data-ttu-id="091ce-141">Faux</span><span class="sxs-lookup"><span data-stu-id="091ce-141">False</span></span>                                              |
| <span data-ttu-id="091ce-142">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="091ce-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="091ce-143">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="091ce-143">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="091ce-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="091ce-144">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="091ce-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="091ce-145">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="091ce-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="091ce-146">Search-Flags</span></span>           | <span data-ttu-id="091ce-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="091ce-147">0x00000000</span></span>                                         |
| <span data-ttu-id="091ce-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="091ce-148">System-Flags</span></span>           | <span data-ttu-id="091ce-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="091ce-149">0x00000010</span></span>                                         |
| <span data-ttu-id="091ce-150">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="091ce-150">Classes used in</span></span>        | [<span data-ttu-id="091ce-151">**Stratégie de domaine**</span><span class="sxs-lookup"><span data-stu-id="091ce-151">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="091ce-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="091ce-152">Windows Server 2003</span></span>



| <span data-ttu-id="091ce-153">Entrée</span><span class="sxs-lookup"><span data-stu-id="091ce-153">Entry</span></span> | <span data-ttu-id="091ce-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="091ce-154">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="091ce-155">ID de lien</span><span class="sxs-lookup"><span data-stu-id="091ce-155">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="091ce-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="091ce-156">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="091ce-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="091ce-157">System-Only</span></span>            | <span data-ttu-id="091ce-158">Faux</span><span class="sxs-lookup"><span data-stu-id="091ce-158">False</span></span>                                              |
| <span data-ttu-id="091ce-159">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="091ce-159">Is-Single-Valued</span></span>       | <span data-ttu-id="091ce-160">Faux</span><span class="sxs-lookup"><span data-stu-id="091ce-160">False</span></span>                                              |
| <span data-ttu-id="091ce-161">Est indexé</span><span class="sxs-lookup"><span data-stu-id="091ce-161">Is Indexed</span></span>             | <span data-ttu-id="091ce-162">Faux</span><span class="sxs-lookup"><span data-stu-id="091ce-162">False</span></span>                                              |
| <span data-ttu-id="091ce-163">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="091ce-163">In Global Catalog</span></span>      | <span data-ttu-id="091ce-164">Faux</span><span class="sxs-lookup"><span data-stu-id="091ce-164">False</span></span>                                              |
| <span data-ttu-id="091ce-165">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="091ce-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="091ce-166">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="091ce-166">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="091ce-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="091ce-167">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="091ce-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="091ce-168">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="091ce-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="091ce-169">Search-Flags</span></span>           | <span data-ttu-id="091ce-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="091ce-170">0x00000000</span></span>                                         |
| <span data-ttu-id="091ce-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="091ce-171">System-Flags</span></span>           | <span data-ttu-id="091ce-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="091ce-172">0x00000010</span></span>                                         |
| <span data-ttu-id="091ce-173">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="091ce-173">Classes used in</span></span>        | [<span data-ttu-id="091ce-174">**Stratégie de domaine**</span><span class="sxs-lookup"><span data-stu-id="091ce-174">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="091ce-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="091ce-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="091ce-176">Entrée</span><span class="sxs-lookup"><span data-stu-id="091ce-176">Entry</span></span> | <span data-ttu-id="091ce-177">Valeur</span><span class="sxs-lookup"><span data-stu-id="091ce-177">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="091ce-178">ID de lien</span><span class="sxs-lookup"><span data-stu-id="091ce-178">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="091ce-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="091ce-179">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="091ce-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="091ce-180">System-Only</span></span>            | <span data-ttu-id="091ce-181">Faux</span><span class="sxs-lookup"><span data-stu-id="091ce-181">False</span></span>                                              |
| <span data-ttu-id="091ce-182">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="091ce-182">Is-Single-Valued</span></span>       | <span data-ttu-id="091ce-183">Faux</span><span class="sxs-lookup"><span data-stu-id="091ce-183">False</span></span>                                              |
| <span data-ttu-id="091ce-184">Est indexé</span><span class="sxs-lookup"><span data-stu-id="091ce-184">Is Indexed</span></span>             | <span data-ttu-id="091ce-185">Faux</span><span class="sxs-lookup"><span data-stu-id="091ce-185">False</span></span>                                              |
| <span data-ttu-id="091ce-186">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="091ce-186">In Global Catalog</span></span>      | <span data-ttu-id="091ce-187">Faux</span><span class="sxs-lookup"><span data-stu-id="091ce-187">False</span></span>                                              |
| <span data-ttu-id="091ce-188">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="091ce-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="091ce-189">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="091ce-189">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="091ce-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="091ce-190">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="091ce-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="091ce-191">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="091ce-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="091ce-192">Search-Flags</span></span>           | <span data-ttu-id="091ce-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="091ce-193">0x00000000</span></span>                                         |
| <span data-ttu-id="091ce-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="091ce-194">System-Flags</span></span>           | <span data-ttu-id="091ce-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="091ce-195">0x00000010</span></span>                                         |
| <span data-ttu-id="091ce-196">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="091ce-196">Classes used in</span></span>        | [<span data-ttu-id="091ce-197">**Stratégie de domaine**</span><span class="sxs-lookup"><span data-stu-id="091ce-197">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="091ce-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="091ce-198">Windows Server 2008</span></span>



| <span data-ttu-id="091ce-199">Entrée</span><span class="sxs-lookup"><span data-stu-id="091ce-199">Entry</span></span> | <span data-ttu-id="091ce-200">Valeur</span><span class="sxs-lookup"><span data-stu-id="091ce-200">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="091ce-201">ID de lien</span><span class="sxs-lookup"><span data-stu-id="091ce-201">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="091ce-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="091ce-202">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="091ce-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="091ce-203">System-Only</span></span>            | <span data-ttu-id="091ce-204">Faux</span><span class="sxs-lookup"><span data-stu-id="091ce-204">False</span></span>                                              |
| <span data-ttu-id="091ce-205">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="091ce-205">Is-Single-Valued</span></span>       | <span data-ttu-id="091ce-206">Faux</span><span class="sxs-lookup"><span data-stu-id="091ce-206">False</span></span>                                              |
| <span data-ttu-id="091ce-207">Est indexé</span><span class="sxs-lookup"><span data-stu-id="091ce-207">Is Indexed</span></span>             | <span data-ttu-id="091ce-208">Faux</span><span class="sxs-lookup"><span data-stu-id="091ce-208">False</span></span>                                              |
| <span data-ttu-id="091ce-209">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="091ce-209">In Global Catalog</span></span>      | <span data-ttu-id="091ce-210">Faux</span><span class="sxs-lookup"><span data-stu-id="091ce-210">False</span></span>                                              |
| <span data-ttu-id="091ce-211">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="091ce-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="091ce-212">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="091ce-212">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="091ce-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="091ce-213">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="091ce-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="091ce-214">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="091ce-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="091ce-215">Search-Flags</span></span>           | <span data-ttu-id="091ce-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="091ce-216">0x00000000</span></span>                                         |
| <span data-ttu-id="091ce-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="091ce-217">System-Flags</span></span>           | <span data-ttu-id="091ce-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="091ce-218">0x00000010</span></span>                                         |
| <span data-ttu-id="091ce-219">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="091ce-219">Classes used in</span></span>        | [<span data-ttu-id="091ce-220">**Stratégie de domaine**</span><span class="sxs-lookup"><span data-stu-id="091ce-220">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="091ce-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="091ce-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="091ce-222">Entrée</span><span class="sxs-lookup"><span data-stu-id="091ce-222">Entry</span></span> | <span data-ttu-id="091ce-223">Valeur</span><span class="sxs-lookup"><span data-stu-id="091ce-223">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="091ce-224">ID de lien</span><span class="sxs-lookup"><span data-stu-id="091ce-224">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="091ce-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="091ce-225">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="091ce-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="091ce-226">System-Only</span></span>            | <span data-ttu-id="091ce-227">Faux</span><span class="sxs-lookup"><span data-stu-id="091ce-227">False</span></span>                                              |
| <span data-ttu-id="091ce-228">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="091ce-228">Is-Single-Valued</span></span>       | <span data-ttu-id="091ce-229">Faux</span><span class="sxs-lookup"><span data-stu-id="091ce-229">False</span></span>                                              |
| <span data-ttu-id="091ce-230">Est indexé</span><span class="sxs-lookup"><span data-stu-id="091ce-230">Is Indexed</span></span>             | <span data-ttu-id="091ce-231">Faux</span><span class="sxs-lookup"><span data-stu-id="091ce-231">False</span></span>                                              |
| <span data-ttu-id="091ce-232">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="091ce-232">In Global Catalog</span></span>      | <span data-ttu-id="091ce-233">Faux</span><span class="sxs-lookup"><span data-stu-id="091ce-233">False</span></span>                                              |
| <span data-ttu-id="091ce-234">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="091ce-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="091ce-235">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="091ce-235">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="091ce-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="091ce-236">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="091ce-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="091ce-237">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="091ce-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="091ce-238">Search-Flags</span></span>           | <span data-ttu-id="091ce-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="091ce-239">0x00000000</span></span>                                         |
| <span data-ttu-id="091ce-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="091ce-240">System-Flags</span></span>           | <span data-ttu-id="091ce-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="091ce-241">0x00000010</span></span>                                         |
| <span data-ttu-id="091ce-242">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="091ce-242">Classes used in</span></span>        | [<span data-ttu-id="091ce-243">**Stratégie de domaine**</span><span class="sxs-lookup"><span data-stu-id="091ce-243">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="091ce-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="091ce-244">Windows Server 2012</span></span>



| <span data-ttu-id="091ce-245">Entrée</span><span class="sxs-lookup"><span data-stu-id="091ce-245">Entry</span></span> | <span data-ttu-id="091ce-246">Valeur</span><span class="sxs-lookup"><span data-stu-id="091ce-246">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="091ce-247">ID de lien</span><span class="sxs-lookup"><span data-stu-id="091ce-247">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="091ce-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="091ce-248">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="091ce-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="091ce-249">System-Only</span></span>            | <span data-ttu-id="091ce-250">Faux</span><span class="sxs-lookup"><span data-stu-id="091ce-250">False</span></span>                                              |
| <span data-ttu-id="091ce-251">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="091ce-251">Is-Single-Valued</span></span>       | <span data-ttu-id="091ce-252">Faux</span><span class="sxs-lookup"><span data-stu-id="091ce-252">False</span></span>                                              |
| <span data-ttu-id="091ce-253">Est indexé</span><span class="sxs-lookup"><span data-stu-id="091ce-253">Is Indexed</span></span>             | <span data-ttu-id="091ce-254">Faux</span><span class="sxs-lookup"><span data-stu-id="091ce-254">False</span></span>                                              |
| <span data-ttu-id="091ce-255">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="091ce-255">In Global Catalog</span></span>      | <span data-ttu-id="091ce-256">Faux</span><span class="sxs-lookup"><span data-stu-id="091ce-256">False</span></span>                                              |
| <span data-ttu-id="091ce-257">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="091ce-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="091ce-258">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="091ce-258">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="091ce-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="091ce-259">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="091ce-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="091ce-260">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="091ce-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="091ce-261">Search-Flags</span></span>           | <span data-ttu-id="091ce-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="091ce-262">0x00000000</span></span>                                         |
| <span data-ttu-id="091ce-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="091ce-263">System-Flags</span></span>           | <span data-ttu-id="091ce-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="091ce-264">0x00000010</span></span>                                         |
| <span data-ttu-id="091ce-265">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="091ce-265">Classes used in</span></span>        | [<span data-ttu-id="091ce-266">**Stratégie de domaine**</span><span class="sxs-lookup"><span data-stu-id="091ce-266">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



 

 





