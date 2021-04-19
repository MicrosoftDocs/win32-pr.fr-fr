---
title: Attribut de référence croisée de domaine
description: Il s’agit d’une référence d’un objet de domaine approuvé à l’objet de référence croisée du domaine approuvé.
ms.assetid: aa6fe6f9-a45c-448c-9fc5-17bc2994c764
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut de référence croisée de domaine
- Schéma AD de l’attribut domainCrossRef
topic_type:
- apiref
api_name:
- Domain-Cross-Ref
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b85e1293ce8141a3614c9401dbb34c1031de5935
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106511192"
---
# <a name="domain-cross-ref-attribute"></a><span data-ttu-id="f922e-105">Attribut de référence croisée de domaine</span><span class="sxs-lookup"><span data-stu-id="f922e-105">Domain-Cross-Ref attribute</span></span>

<span data-ttu-id="f922e-106">Il s’agit d’une référence d’un objet de domaine approuvé à l’objet de référence croisée du domaine approuvé.</span><span class="sxs-lookup"><span data-stu-id="f922e-106">This is a reference from a trusted domain object to the cross reference object of the trusted domain.</span></span>



| <span data-ttu-id="f922e-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="f922e-107">Entry</span></span> | <span data-ttu-id="f922e-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="f922e-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="f922e-109">CN</span><span class="sxs-lookup"><span data-stu-id="f922e-109">CN</span></span>                | <span data-ttu-id="f922e-110">Référence croisée de domaine</span><span class="sxs-lookup"><span data-stu-id="f922e-110">Domain-Cross-Ref</span></span>                        |
| <span data-ttu-id="f922e-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f922e-111">Ldap-Display-Name</span></span> | <span data-ttu-id="f922e-112">domainCrossRef</span><span class="sxs-lookup"><span data-stu-id="f922e-112">domainCrossRef</span></span>                          |
| <span data-ttu-id="f922e-113">Taille</span><span class="sxs-lookup"><span data-stu-id="f922e-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="f922e-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="f922e-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="f922e-115">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="f922e-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="f922e-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f922e-116">Attribute-Id</span></span>      | <span data-ttu-id="f922e-117">1.2.840.113556.1.4.472</span><span class="sxs-lookup"><span data-stu-id="f922e-117">1.2.840.113556.1.4.472</span></span>                  |
| <span data-ttu-id="f922e-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f922e-118">System-Id-Guid</span></span>    | <span data-ttu-id="f922e-119">b000ea7b-a086-11d0-afdd-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="f922e-119">b000ea7b-a086-11d0-afdd-00c04fd930c9</span></span>    |
| <span data-ttu-id="f922e-120">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f922e-120">Syntax</span></span>            | [<span data-ttu-id="f922e-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="f922e-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="f922e-122">Implémentations</span><span class="sxs-lookup"><span data-stu-id="f922e-122">Implementations</span></span>

-   [<span data-ttu-id="f922e-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f922e-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f922e-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f922e-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f922e-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f922e-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f922e-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f922e-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f922e-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f922e-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f922e-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f922e-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f922e-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f922e-129">Windows 2000 Server</span></span>



| <span data-ttu-id="f922e-130">Entrée</span><span class="sxs-lookup"><span data-stu-id="f922e-130">Entry</span></span> | <span data-ttu-id="f922e-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="f922e-131">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="f922e-132">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f922e-132">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="f922e-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f922e-133">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="f922e-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="f922e-134">System-Only</span></span>            | <span data-ttu-id="f922e-135">Faux</span><span class="sxs-lookup"><span data-stu-id="f922e-135">False</span></span>                                                |
| <span data-ttu-id="f922e-136">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f922e-136">Is-Single-Valued</span></span>       | <span data-ttu-id="f922e-137">Vrai</span><span class="sxs-lookup"><span data-stu-id="f922e-137">True</span></span>                                                 |
| <span data-ttu-id="f922e-138">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f922e-138">Is Indexed</span></span>             | <span data-ttu-id="f922e-139">Faux</span><span class="sxs-lookup"><span data-stu-id="f922e-139">False</span></span>                                                |
| <span data-ttu-id="f922e-140">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f922e-140">In Global Catalog</span></span>      | <span data-ttu-id="f922e-141">Faux</span><span class="sxs-lookup"><span data-stu-id="f922e-141">False</span></span>                                                |
| <span data-ttu-id="f922e-142">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f922e-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="f922e-143">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f922e-143">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="f922e-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f922e-144">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="f922e-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f922e-145">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="f922e-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f922e-146">Search-Flags</span></span>           | <span data-ttu-id="f922e-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f922e-147">0x00000000</span></span>                                           |
| <span data-ttu-id="f922e-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f922e-148">System-Flags</span></span>           | <span data-ttu-id="f922e-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f922e-149">0x00000010</span></span>                                           |
| <span data-ttu-id="f922e-150">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f922e-150">Classes used in</span></span>        | [<span data-ttu-id="f922e-151">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="f922e-151">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f922e-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f922e-152">Windows Server 2003</span></span>



| <span data-ttu-id="f922e-153">Entrée</span><span class="sxs-lookup"><span data-stu-id="f922e-153">Entry</span></span> | <span data-ttu-id="f922e-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="f922e-154">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="f922e-155">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f922e-155">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="f922e-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f922e-156">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="f922e-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="f922e-157">System-Only</span></span>            | <span data-ttu-id="f922e-158">Faux</span><span class="sxs-lookup"><span data-stu-id="f922e-158">False</span></span>                                                |
| <span data-ttu-id="f922e-159">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f922e-159">Is-Single-Valued</span></span>       | <span data-ttu-id="f922e-160">Vrai</span><span class="sxs-lookup"><span data-stu-id="f922e-160">True</span></span>                                                 |
| <span data-ttu-id="f922e-161">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f922e-161">Is Indexed</span></span>             | <span data-ttu-id="f922e-162">Faux</span><span class="sxs-lookup"><span data-stu-id="f922e-162">False</span></span>                                                |
| <span data-ttu-id="f922e-163">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f922e-163">In Global Catalog</span></span>      | <span data-ttu-id="f922e-164">Faux</span><span class="sxs-lookup"><span data-stu-id="f922e-164">False</span></span>                                                |
| <span data-ttu-id="f922e-165">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f922e-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="f922e-166">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f922e-166">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="f922e-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f922e-167">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="f922e-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f922e-168">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="f922e-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f922e-169">Search-Flags</span></span>           | <span data-ttu-id="f922e-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f922e-170">0x00000000</span></span>                                           |
| <span data-ttu-id="f922e-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f922e-171">System-Flags</span></span>           | <span data-ttu-id="f922e-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f922e-172">0x00000010</span></span>                                           |
| <span data-ttu-id="f922e-173">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f922e-173">Classes used in</span></span>        | [<span data-ttu-id="f922e-174">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="f922e-174">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f922e-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f922e-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f922e-176">Entrée</span><span class="sxs-lookup"><span data-stu-id="f922e-176">Entry</span></span> | <span data-ttu-id="f922e-177">Valeur</span><span class="sxs-lookup"><span data-stu-id="f922e-177">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="f922e-178">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f922e-178">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="f922e-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f922e-179">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="f922e-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="f922e-180">System-Only</span></span>            | <span data-ttu-id="f922e-181">Faux</span><span class="sxs-lookup"><span data-stu-id="f922e-181">False</span></span>                                                |
| <span data-ttu-id="f922e-182">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f922e-182">Is-Single-Valued</span></span>       | <span data-ttu-id="f922e-183">Vrai</span><span class="sxs-lookup"><span data-stu-id="f922e-183">True</span></span>                                                 |
| <span data-ttu-id="f922e-184">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f922e-184">Is Indexed</span></span>             | <span data-ttu-id="f922e-185">Faux</span><span class="sxs-lookup"><span data-stu-id="f922e-185">False</span></span>                                                |
| <span data-ttu-id="f922e-186">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f922e-186">In Global Catalog</span></span>      | <span data-ttu-id="f922e-187">Faux</span><span class="sxs-lookup"><span data-stu-id="f922e-187">False</span></span>                                                |
| <span data-ttu-id="f922e-188">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f922e-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="f922e-189">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f922e-189">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="f922e-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f922e-190">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="f922e-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f922e-191">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="f922e-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f922e-192">Search-Flags</span></span>           | <span data-ttu-id="f922e-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f922e-193">0x00000000</span></span>                                           |
| <span data-ttu-id="f922e-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f922e-194">System-Flags</span></span>           | <span data-ttu-id="f922e-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f922e-195">0x00000010</span></span>                                           |
| <span data-ttu-id="f922e-196">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f922e-196">Classes used in</span></span>        | [<span data-ttu-id="f922e-197">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="f922e-197">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f922e-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f922e-198">Windows Server 2008</span></span>



| <span data-ttu-id="f922e-199">Entrée</span><span class="sxs-lookup"><span data-stu-id="f922e-199">Entry</span></span> | <span data-ttu-id="f922e-200">Valeur</span><span class="sxs-lookup"><span data-stu-id="f922e-200">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="f922e-201">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f922e-201">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="f922e-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f922e-202">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="f922e-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="f922e-203">System-Only</span></span>            | <span data-ttu-id="f922e-204">Faux</span><span class="sxs-lookup"><span data-stu-id="f922e-204">False</span></span>                                                |
| <span data-ttu-id="f922e-205">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f922e-205">Is-Single-Valued</span></span>       | <span data-ttu-id="f922e-206">Vrai</span><span class="sxs-lookup"><span data-stu-id="f922e-206">True</span></span>                                                 |
| <span data-ttu-id="f922e-207">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f922e-207">Is Indexed</span></span>             | <span data-ttu-id="f922e-208">Faux</span><span class="sxs-lookup"><span data-stu-id="f922e-208">False</span></span>                                                |
| <span data-ttu-id="f922e-209">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f922e-209">In Global Catalog</span></span>      | <span data-ttu-id="f922e-210">Faux</span><span class="sxs-lookup"><span data-stu-id="f922e-210">False</span></span>                                                |
| <span data-ttu-id="f922e-211">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f922e-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="f922e-212">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f922e-212">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="f922e-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f922e-213">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="f922e-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f922e-214">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="f922e-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f922e-215">Search-Flags</span></span>           | <span data-ttu-id="f922e-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f922e-216">0x00000000</span></span>                                           |
| <span data-ttu-id="f922e-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f922e-217">System-Flags</span></span>           | <span data-ttu-id="f922e-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f922e-218">0x00000010</span></span>                                           |
| <span data-ttu-id="f922e-219">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f922e-219">Classes used in</span></span>        | [<span data-ttu-id="f922e-220">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="f922e-220">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f922e-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f922e-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f922e-222">Entrée</span><span class="sxs-lookup"><span data-stu-id="f922e-222">Entry</span></span> | <span data-ttu-id="f922e-223">Valeur</span><span class="sxs-lookup"><span data-stu-id="f922e-223">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="f922e-224">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f922e-224">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="f922e-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f922e-225">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="f922e-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="f922e-226">System-Only</span></span>            | <span data-ttu-id="f922e-227">Faux</span><span class="sxs-lookup"><span data-stu-id="f922e-227">False</span></span>                                                |
| <span data-ttu-id="f922e-228">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f922e-228">Is-Single-Valued</span></span>       | <span data-ttu-id="f922e-229">Vrai</span><span class="sxs-lookup"><span data-stu-id="f922e-229">True</span></span>                                                 |
| <span data-ttu-id="f922e-230">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f922e-230">Is Indexed</span></span>             | <span data-ttu-id="f922e-231">Faux</span><span class="sxs-lookup"><span data-stu-id="f922e-231">False</span></span>                                                |
| <span data-ttu-id="f922e-232">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f922e-232">In Global Catalog</span></span>      | <span data-ttu-id="f922e-233">Faux</span><span class="sxs-lookup"><span data-stu-id="f922e-233">False</span></span>                                                |
| <span data-ttu-id="f922e-234">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f922e-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="f922e-235">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f922e-235">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="f922e-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f922e-236">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="f922e-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f922e-237">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="f922e-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f922e-238">Search-Flags</span></span>           | <span data-ttu-id="f922e-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f922e-239">0x00000000</span></span>                                           |
| <span data-ttu-id="f922e-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f922e-240">System-Flags</span></span>           | <span data-ttu-id="f922e-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f922e-241">0x00000010</span></span>                                           |
| <span data-ttu-id="f922e-242">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f922e-242">Classes used in</span></span>        | [<span data-ttu-id="f922e-243">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="f922e-243">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f922e-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f922e-244">Windows Server 2012</span></span>



| <span data-ttu-id="f922e-245">Entrée</span><span class="sxs-lookup"><span data-stu-id="f922e-245">Entry</span></span> | <span data-ttu-id="f922e-246">Valeur</span><span class="sxs-lookup"><span data-stu-id="f922e-246">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="f922e-247">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f922e-247">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="f922e-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f922e-248">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="f922e-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="f922e-249">System-Only</span></span>            | <span data-ttu-id="f922e-250">Faux</span><span class="sxs-lookup"><span data-stu-id="f922e-250">False</span></span>                                                |
| <span data-ttu-id="f922e-251">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f922e-251">Is-Single-Valued</span></span>       | <span data-ttu-id="f922e-252">Vrai</span><span class="sxs-lookup"><span data-stu-id="f922e-252">True</span></span>                                                 |
| <span data-ttu-id="f922e-253">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f922e-253">Is Indexed</span></span>             | <span data-ttu-id="f922e-254">Faux</span><span class="sxs-lookup"><span data-stu-id="f922e-254">False</span></span>                                                |
| <span data-ttu-id="f922e-255">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f922e-255">In Global Catalog</span></span>      | <span data-ttu-id="f922e-256">Faux</span><span class="sxs-lookup"><span data-stu-id="f922e-256">False</span></span>                                                |
| <span data-ttu-id="f922e-257">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f922e-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="f922e-258">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f922e-258">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="f922e-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f922e-259">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="f922e-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f922e-260">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="f922e-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f922e-261">Search-Flags</span></span>           | <span data-ttu-id="f922e-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f922e-262">0x00000000</span></span>                                           |
| <span data-ttu-id="f922e-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f922e-263">System-Flags</span></span>           | <span data-ttu-id="f922e-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f922e-264">0x00000010</span></span>                                           |
| <span data-ttu-id="f922e-265">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f922e-265">Classes used in</span></span>        | [<span data-ttu-id="f922e-266">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="f922e-266">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





