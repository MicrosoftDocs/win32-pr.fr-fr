---
title: Attribut Lockout-Threshold
description: Nombre de tentatives de connexion non valides autorisées avant le verrouillage du compte.
ms.assetid: c4dcbbb6-0680-45f3-9b0b-f9c4bbf2b349
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Lockout-Threshold
- Schéma AD de l’attribut lockoutThreshold
topic_type:
- apiref
api_name:
- Lockout-Threshold
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 345977055597c48d70e30a20ce9bfbc9f07f3929
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103844729"
---
# <a name="lockout-threshold-attribute"></a><span data-ttu-id="bee1b-105">Attribut Lockout-Threshold</span><span class="sxs-lookup"><span data-stu-id="bee1b-105">Lockout-Threshold attribute</span></span>

<span data-ttu-id="bee1b-106">Nombre de tentatives de connexion non valides autorisées avant le verrouillage du compte.</span><span class="sxs-lookup"><span data-stu-id="bee1b-106">The number of invalid logon attempts that are permitted before the account is locked out.</span></span>



| <span data-ttu-id="bee1b-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="bee1b-107">Entry</span></span> | <span data-ttu-id="bee1b-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="bee1b-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="bee1b-109">CN</span><span class="sxs-lookup"><span data-stu-id="bee1b-109">CN</span></span>                | <span data-ttu-id="bee1b-110">Lockout-Threshold</span><span class="sxs-lookup"><span data-stu-id="bee1b-110">Lockout-Threshold</span></span>                    |
| <span data-ttu-id="bee1b-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="bee1b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="bee1b-112">lockoutThreshold</span><span class="sxs-lookup"><span data-stu-id="bee1b-112">lockoutThreshold</span></span>                     |
| <span data-ttu-id="bee1b-113">Taille</span><span class="sxs-lookup"><span data-stu-id="bee1b-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="bee1b-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="bee1b-114">Update Privilege</span></span>  | <span data-ttu-id="bee1b-115">Administrateur de domaine</span><span class="sxs-lookup"><span data-stu-id="bee1b-115">Domain administrator</span></span>                 |
| <span data-ttu-id="bee1b-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="bee1b-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="bee1b-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="bee1b-117">Attribute-Id</span></span>      | <span data-ttu-id="bee1b-118">1.2.840.113556.1.4.73</span><span class="sxs-lookup"><span data-stu-id="bee1b-118">1.2.840.113556.1.4.73</span></span>                |
| <span data-ttu-id="bee1b-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="bee1b-119">System-Id-Guid</span></span>    | <span data-ttu-id="bee1b-120">bf9679a6-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="bee1b-120">bf9679a6-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="bee1b-121">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bee1b-121">Syntax</span></span>            | [<span data-ttu-id="bee1b-122">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="bee1b-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="bee1b-123">Implémentations</span><span class="sxs-lookup"><span data-stu-id="bee1b-123">Implementations</span></span>

-   [<span data-ttu-id="bee1b-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="bee1b-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="bee1b-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="bee1b-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="bee1b-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="bee1b-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="bee1b-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="bee1b-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="bee1b-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="bee1b-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="bee1b-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="bee1b-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="bee1b-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bee1b-130">Windows 2000 Server</span></span>



| <span data-ttu-id="bee1b-131">Entrée</span><span class="sxs-lookup"><span data-stu-id="bee1b-131">Entry</span></span> | <span data-ttu-id="bee1b-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="bee1b-132">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bee1b-133">ID de lien</span><span class="sxs-lookup"><span data-stu-id="bee1b-133">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="bee1b-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bee1b-134">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="bee1b-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="bee1b-135">System-Only</span></span>            | <span data-ttu-id="bee1b-136">Faux</span><span class="sxs-lookup"><span data-stu-id="bee1b-136">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="bee1b-137">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="bee1b-137">Is-Single-Valued</span></span>       | <span data-ttu-id="bee1b-138">Vrai</span><span class="sxs-lookup"><span data-stu-id="bee1b-138">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="bee1b-139">Est indexé</span><span class="sxs-lookup"><span data-stu-id="bee1b-139">Is Indexed</span></span>             | <span data-ttu-id="bee1b-140">Faux</span><span class="sxs-lookup"><span data-stu-id="bee1b-140">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="bee1b-141">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="bee1b-141">In Global Catalog</span></span>      | <span data-ttu-id="bee1b-142">Faux</span><span class="sxs-lookup"><span data-stu-id="bee1b-142">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="bee1b-143">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="bee1b-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="bee1b-144">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="bee1b-144">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="bee1b-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bee1b-145">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="bee1b-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bee1b-146">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="bee1b-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bee1b-147">Search-Flags</span></span>           | <span data-ttu-id="bee1b-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bee1b-148">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="bee1b-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bee1b-149">System-Flags</span></span>           | <span data-ttu-id="bee1b-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bee1b-150">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="bee1b-151">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="bee1b-151">Classes used in</span></span>        | [<span data-ttu-id="bee1b-152">**Stratégie de domaine**</span><span class="sxs-lookup"><span data-stu-id="bee1b-152">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="bee1b-153">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="bee1b-153">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="bee1b-154">**Sam-domaine-base**</span><span class="sxs-lookup"><span data-stu-id="bee1b-154">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="bee1b-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bee1b-155">Windows Server 2003</span></span>



| <span data-ttu-id="bee1b-156">Entrée</span><span class="sxs-lookup"><span data-stu-id="bee1b-156">Entry</span></span> | <span data-ttu-id="bee1b-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="bee1b-157">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bee1b-158">ID de lien</span><span class="sxs-lookup"><span data-stu-id="bee1b-158">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="bee1b-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bee1b-159">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="bee1b-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="bee1b-160">System-Only</span></span>            | <span data-ttu-id="bee1b-161">Faux</span><span class="sxs-lookup"><span data-stu-id="bee1b-161">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="bee1b-162">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="bee1b-162">Is-Single-Valued</span></span>       | <span data-ttu-id="bee1b-163">Vrai</span><span class="sxs-lookup"><span data-stu-id="bee1b-163">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="bee1b-164">Est indexé</span><span class="sxs-lookup"><span data-stu-id="bee1b-164">Is Indexed</span></span>             | <span data-ttu-id="bee1b-165">Faux</span><span class="sxs-lookup"><span data-stu-id="bee1b-165">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="bee1b-166">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="bee1b-166">In Global Catalog</span></span>      | <span data-ttu-id="bee1b-167">Faux</span><span class="sxs-lookup"><span data-stu-id="bee1b-167">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="bee1b-168">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="bee1b-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="bee1b-169">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="bee1b-169">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="bee1b-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bee1b-170">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="bee1b-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bee1b-171">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="bee1b-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bee1b-172">Search-Flags</span></span>           | <span data-ttu-id="bee1b-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bee1b-173">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="bee1b-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bee1b-174">System-Flags</span></span>           | <span data-ttu-id="bee1b-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bee1b-175">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="bee1b-176">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="bee1b-176">Classes used in</span></span>        | [<span data-ttu-id="bee1b-177">**Stratégie de domaine**</span><span class="sxs-lookup"><span data-stu-id="bee1b-177">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="bee1b-178">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="bee1b-178">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="bee1b-179">**Sam-domaine-base**</span><span class="sxs-lookup"><span data-stu-id="bee1b-179">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="bee1b-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="bee1b-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="bee1b-181">Entrée</span><span class="sxs-lookup"><span data-stu-id="bee1b-181">Entry</span></span> | <span data-ttu-id="bee1b-182">Valeur</span><span class="sxs-lookup"><span data-stu-id="bee1b-182">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bee1b-183">ID de lien</span><span class="sxs-lookup"><span data-stu-id="bee1b-183">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="bee1b-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bee1b-184">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="bee1b-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="bee1b-185">System-Only</span></span>            | <span data-ttu-id="bee1b-186">Faux</span><span class="sxs-lookup"><span data-stu-id="bee1b-186">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="bee1b-187">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="bee1b-187">Is-Single-Valued</span></span>       | <span data-ttu-id="bee1b-188">Vrai</span><span class="sxs-lookup"><span data-stu-id="bee1b-188">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="bee1b-189">Est indexé</span><span class="sxs-lookup"><span data-stu-id="bee1b-189">Is Indexed</span></span>             | <span data-ttu-id="bee1b-190">Faux</span><span class="sxs-lookup"><span data-stu-id="bee1b-190">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="bee1b-191">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="bee1b-191">In Global Catalog</span></span>      | <span data-ttu-id="bee1b-192">Faux</span><span class="sxs-lookup"><span data-stu-id="bee1b-192">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="bee1b-193">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="bee1b-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="bee1b-194">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="bee1b-194">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="bee1b-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bee1b-195">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="bee1b-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bee1b-196">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="bee1b-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bee1b-197">Search-Flags</span></span>           | <span data-ttu-id="bee1b-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bee1b-198">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="bee1b-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bee1b-199">System-Flags</span></span>           | <span data-ttu-id="bee1b-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bee1b-200">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="bee1b-201">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="bee1b-201">Classes used in</span></span>        | [<span data-ttu-id="bee1b-202">**Stratégie de domaine**</span><span class="sxs-lookup"><span data-stu-id="bee1b-202">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="bee1b-203">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="bee1b-203">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="bee1b-204">**Sam-domaine-base**</span><span class="sxs-lookup"><span data-stu-id="bee1b-204">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="bee1b-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bee1b-205">Windows Server 2008</span></span>



| <span data-ttu-id="bee1b-206">Entrée</span><span class="sxs-lookup"><span data-stu-id="bee1b-206">Entry</span></span> | <span data-ttu-id="bee1b-207">Valeur</span><span class="sxs-lookup"><span data-stu-id="bee1b-207">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bee1b-208">ID de lien</span><span class="sxs-lookup"><span data-stu-id="bee1b-208">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="bee1b-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bee1b-209">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="bee1b-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="bee1b-210">System-Only</span></span>            | <span data-ttu-id="bee1b-211">Faux</span><span class="sxs-lookup"><span data-stu-id="bee1b-211">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="bee1b-212">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="bee1b-212">Is-Single-Valued</span></span>       | <span data-ttu-id="bee1b-213">Vrai</span><span class="sxs-lookup"><span data-stu-id="bee1b-213">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="bee1b-214">Est indexé</span><span class="sxs-lookup"><span data-stu-id="bee1b-214">Is Indexed</span></span>             | <span data-ttu-id="bee1b-215">Faux</span><span class="sxs-lookup"><span data-stu-id="bee1b-215">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="bee1b-216">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="bee1b-216">In Global Catalog</span></span>      | <span data-ttu-id="bee1b-217">Faux</span><span class="sxs-lookup"><span data-stu-id="bee1b-217">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="bee1b-218">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="bee1b-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="bee1b-219">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="bee1b-219">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="bee1b-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bee1b-220">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="bee1b-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bee1b-221">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="bee1b-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bee1b-222">Search-Flags</span></span>           | <span data-ttu-id="bee1b-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bee1b-223">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="bee1b-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bee1b-224">System-Flags</span></span>           | <span data-ttu-id="bee1b-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bee1b-225">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="bee1b-226">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="bee1b-226">Classes used in</span></span>        | [<span data-ttu-id="bee1b-227">**Stratégie de domaine**</span><span class="sxs-lookup"><span data-stu-id="bee1b-227">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="bee1b-228">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="bee1b-228">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="bee1b-229">**Sam-domaine-base**</span><span class="sxs-lookup"><span data-stu-id="bee1b-229">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="bee1b-230">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bee1b-230">Windows Server 2008 R2</span></span>



| <span data-ttu-id="bee1b-231">Entrée</span><span class="sxs-lookup"><span data-stu-id="bee1b-231">Entry</span></span> | <span data-ttu-id="bee1b-232">Valeur</span><span class="sxs-lookup"><span data-stu-id="bee1b-232">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bee1b-233">ID de lien</span><span class="sxs-lookup"><span data-stu-id="bee1b-233">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="bee1b-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bee1b-234">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="bee1b-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="bee1b-235">System-Only</span></span>            | <span data-ttu-id="bee1b-236">Faux</span><span class="sxs-lookup"><span data-stu-id="bee1b-236">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="bee1b-237">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="bee1b-237">Is-Single-Valued</span></span>       | <span data-ttu-id="bee1b-238">Vrai</span><span class="sxs-lookup"><span data-stu-id="bee1b-238">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="bee1b-239">Est indexé</span><span class="sxs-lookup"><span data-stu-id="bee1b-239">Is Indexed</span></span>             | <span data-ttu-id="bee1b-240">Faux</span><span class="sxs-lookup"><span data-stu-id="bee1b-240">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="bee1b-241">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="bee1b-241">In Global Catalog</span></span>      | <span data-ttu-id="bee1b-242">Faux</span><span class="sxs-lookup"><span data-stu-id="bee1b-242">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="bee1b-243">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="bee1b-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="bee1b-244">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="bee1b-244">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="bee1b-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bee1b-245">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="bee1b-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bee1b-246">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="bee1b-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bee1b-247">Search-Flags</span></span>           | <span data-ttu-id="bee1b-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bee1b-248">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="bee1b-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bee1b-249">System-Flags</span></span>           | <span data-ttu-id="bee1b-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bee1b-250">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="bee1b-251">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="bee1b-251">Classes used in</span></span>        | [<span data-ttu-id="bee1b-252">**Stratégie de domaine**</span><span class="sxs-lookup"><span data-stu-id="bee1b-252">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="bee1b-253">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="bee1b-253">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="bee1b-254">**Sam-domaine-base**</span><span class="sxs-lookup"><span data-stu-id="bee1b-254">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="bee1b-255">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bee1b-255">Windows Server 2012</span></span>



| <span data-ttu-id="bee1b-256">Entrée</span><span class="sxs-lookup"><span data-stu-id="bee1b-256">Entry</span></span> | <span data-ttu-id="bee1b-257">Valeur</span><span class="sxs-lookup"><span data-stu-id="bee1b-257">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bee1b-258">ID de lien</span><span class="sxs-lookup"><span data-stu-id="bee1b-258">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="bee1b-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bee1b-259">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="bee1b-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="bee1b-260">System-Only</span></span>            | <span data-ttu-id="bee1b-261">Faux</span><span class="sxs-lookup"><span data-stu-id="bee1b-261">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="bee1b-262">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="bee1b-262">Is-Single-Valued</span></span>       | <span data-ttu-id="bee1b-263">Vrai</span><span class="sxs-lookup"><span data-stu-id="bee1b-263">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="bee1b-264">Est indexé</span><span class="sxs-lookup"><span data-stu-id="bee1b-264">Is Indexed</span></span>             | <span data-ttu-id="bee1b-265">Faux</span><span class="sxs-lookup"><span data-stu-id="bee1b-265">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="bee1b-266">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="bee1b-266">In Global Catalog</span></span>      | <span data-ttu-id="bee1b-267">Faux</span><span class="sxs-lookup"><span data-stu-id="bee1b-267">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="bee1b-268">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="bee1b-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="bee1b-269">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="bee1b-269">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="bee1b-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bee1b-270">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="bee1b-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bee1b-271">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="bee1b-272">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bee1b-272">Search-Flags</span></span>           | <span data-ttu-id="bee1b-273">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bee1b-273">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="bee1b-274">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bee1b-274">System-Flags</span></span>           | <span data-ttu-id="bee1b-275">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bee1b-275">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="bee1b-276">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="bee1b-276">Classes used in</span></span>        | [<span data-ttu-id="bee1b-277">**Stratégie de domaine**</span><span class="sxs-lookup"><span data-stu-id="bee1b-277">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="bee1b-278">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="bee1b-278">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="bee1b-279">**Sam-domaine-base**</span><span class="sxs-lookup"><span data-stu-id="bee1b-279">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="see-also"></a><span data-ttu-id="bee1b-280">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bee1b-280">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bee1b-281">**Verrouillage-durée**</span><span class="sxs-lookup"><span data-stu-id="bee1b-281">**Lockout-Duration**</span></span>](a-lockoutduration.md)
</dt> </dl>

 

 





