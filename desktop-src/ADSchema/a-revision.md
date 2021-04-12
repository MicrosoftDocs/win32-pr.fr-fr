---
title: Attribut de révision
description: Niveau de révision pour un descripteur de sécurité ou autre modification. Utilisé uniquement dans les objets Sam-Server et DS-UI-Settings.
ms.assetid: 480de80f-3e76-4a62-a4a7-29a67f910a62
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut de révision
- Schéma AD d’attribut de révision
topic_type:
- apiref
api_name:
- Revision
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8948bd865db776c52ac021d296792a6f7d0720dc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104519673"
---
# <a name="revision-attribute"></a><span data-ttu-id="ec12f-106">Attribut de révision</span><span class="sxs-lookup"><span data-stu-id="ec12f-106">Revision attribute</span></span>

<span data-ttu-id="ec12f-107">Niveau de révision pour un descripteur de sécurité ou autre modification.</span><span class="sxs-lookup"><span data-stu-id="ec12f-107">The revision level for a security descriptor or other change.</span></span> <span data-ttu-id="ec12f-108">Utilisé uniquement dans les objets Sam-Server et DS-UI-Settings.</span><span class="sxs-lookup"><span data-stu-id="ec12f-108">Only used in the sam-server and ds-ui-settings objects.</span></span>



| <span data-ttu-id="ec12f-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="ec12f-109">Entry</span></span> | <span data-ttu-id="ec12f-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="ec12f-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="ec12f-111">CN</span><span class="sxs-lookup"><span data-stu-id="ec12f-111">CN</span></span>                | <span data-ttu-id="ec12f-112">Révision</span><span class="sxs-lookup"><span data-stu-id="ec12f-112">Revision</span></span>                             |
| <span data-ttu-id="ec12f-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="ec12f-113">Ldap-Display-Name</span></span> | <span data-ttu-id="ec12f-114">revision</span><span class="sxs-lookup"><span data-stu-id="ec12f-114">revision</span></span>                             |
| <span data-ttu-id="ec12f-115">Taille</span><span class="sxs-lookup"><span data-stu-id="ec12f-115">Size</span></span>              | <span data-ttu-id="ec12f-116">4 octets</span><span class="sxs-lookup"><span data-stu-id="ec12f-116">4 bytes</span></span>                              |
| <span data-ttu-id="ec12f-117">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="ec12f-117">Update Privilege</span></span>  | <span data-ttu-id="ec12f-118">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="ec12f-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="ec12f-119">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="ec12f-119">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="ec12f-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ec12f-120">Attribute-Id</span></span>      | <span data-ttu-id="ec12f-121">1.2.840.113556.1.4.145</span><span class="sxs-lookup"><span data-stu-id="ec12f-121">1.2.840.113556.1.4.145</span></span>               |
| <span data-ttu-id="ec12f-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ec12f-122">System-Id-Guid</span></span>    | <span data-ttu-id="ec12f-123">bf967a21-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="ec12f-123">bf967a21-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="ec12f-124">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ec12f-124">Syntax</span></span>            | [<span data-ttu-id="ec12f-125">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="ec12f-125">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="ec12f-126">Implémentations</span><span class="sxs-lookup"><span data-stu-id="ec12f-126">Implementations</span></span>

-   [<span data-ttu-id="ec12f-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ec12f-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ec12f-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ec12f-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ec12f-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="ec12f-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="ec12f-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ec12f-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ec12f-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ec12f-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ec12f-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ec12f-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ec12f-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ec12f-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ec12f-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ec12f-134">Windows 2000 Server</span></span>



| <span data-ttu-id="ec12f-135">Entrée</span><span class="sxs-lookup"><span data-stu-id="ec12f-135">Entry</span></span> | <span data-ttu-id="ec12f-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="ec12f-136">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ec12f-137">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ec12f-137">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="ec12f-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec12f-138">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="ec12f-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec12f-139">System-Only</span></span>            | <span data-ttu-id="ec12f-140">Faux</span><span class="sxs-lookup"><span data-stu-id="ec12f-140">False</span></span>                                                                                 |
| <span data-ttu-id="ec12f-141">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ec12f-141">Is-Single-Valued</span></span>       | <span data-ttu-id="ec12f-142">Vrai</span><span class="sxs-lookup"><span data-stu-id="ec12f-142">True</span></span>                                                                                  |
| <span data-ttu-id="ec12f-143">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ec12f-143">Is Indexed</span></span>             | <span data-ttu-id="ec12f-144">Faux</span><span class="sxs-lookup"><span data-stu-id="ec12f-144">False</span></span>                                                                                 |
| <span data-ttu-id="ec12f-145">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ec12f-145">In Global Catalog</span></span>      | <span data-ttu-id="ec12f-146">Faux</span><span class="sxs-lookup"><span data-stu-id="ec12f-146">False</span></span>                                                                                 |
| <span data-ttu-id="ec12f-147">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ec12f-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec12f-148">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ec12f-148">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="ec12f-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec12f-149">Range-Lower</span></span>            | \-                                                                                    |
| <span data-ttu-id="ec12f-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec12f-150">Range-Upper</span></span>            | \-                                                                                    |
| <span data-ttu-id="ec12f-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec12f-151">Search-Flags</span></span>           | <span data-ttu-id="ec12f-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec12f-152">0x00000000</span></span>                                                                            |
| <span data-ttu-id="ec12f-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec12f-153">System-Flags</span></span>           | <span data-ttu-id="ec12f-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ec12f-154">0x00000010</span></span>                                                                            |
| <span data-ttu-id="ec12f-155">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ec12f-155">Classes used in</span></span>        | [<span data-ttu-id="ec12f-156">**Sam-domaine-base**</span><span class="sxs-lookup"><span data-stu-id="ec12f-156">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> [<span data-ttu-id="ec12f-157">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="ec12f-157">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ec12f-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ec12f-158">Windows Server 2003</span></span>



| <span data-ttu-id="ec12f-159">Entrée</span><span class="sxs-lookup"><span data-stu-id="ec12f-159">Entry</span></span> | <span data-ttu-id="ec12f-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="ec12f-160">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ec12f-161">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ec12f-161">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="ec12f-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec12f-162">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="ec12f-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec12f-163">System-Only</span></span>            | <span data-ttu-id="ec12f-164">Faux</span><span class="sxs-lookup"><span data-stu-id="ec12f-164">False</span></span>                                                                                 |
| <span data-ttu-id="ec12f-165">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ec12f-165">Is-Single-Valued</span></span>       | <span data-ttu-id="ec12f-166">Vrai</span><span class="sxs-lookup"><span data-stu-id="ec12f-166">True</span></span>                                                                                  |
| <span data-ttu-id="ec12f-167">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ec12f-167">Is Indexed</span></span>             | <span data-ttu-id="ec12f-168">Faux</span><span class="sxs-lookup"><span data-stu-id="ec12f-168">False</span></span>                                                                                 |
| <span data-ttu-id="ec12f-169">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ec12f-169">In Global Catalog</span></span>      | <span data-ttu-id="ec12f-170">Faux</span><span class="sxs-lookup"><span data-stu-id="ec12f-170">False</span></span>                                                                                 |
| <span data-ttu-id="ec12f-171">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ec12f-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec12f-172">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ec12f-172">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="ec12f-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec12f-173">Range-Lower</span></span>            | \-                                                                                    |
| <span data-ttu-id="ec12f-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec12f-174">Range-Upper</span></span>            | \-                                                                                    |
| <span data-ttu-id="ec12f-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec12f-175">Search-Flags</span></span>           | <span data-ttu-id="ec12f-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec12f-176">0x00000000</span></span>                                                                            |
| <span data-ttu-id="ec12f-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec12f-177">System-Flags</span></span>           | <span data-ttu-id="ec12f-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ec12f-178">0x00000010</span></span>                                                                            |
| <span data-ttu-id="ec12f-179">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ec12f-179">Classes used in</span></span>        | [<span data-ttu-id="ec12f-180">**Sam-domaine-base**</span><span class="sxs-lookup"><span data-stu-id="ec12f-180">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> [<span data-ttu-id="ec12f-181">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="ec12f-181">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="ec12f-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="ec12f-182">ADAM</span></span>



| <span data-ttu-id="ec12f-183">Entrée</span><span class="sxs-lookup"><span data-stu-id="ec12f-183">Entry</span></span> | <span data-ttu-id="ec12f-184">Valeur</span><span class="sxs-lookup"><span data-stu-id="ec12f-184">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ec12f-185">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ec12f-185">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ec12f-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec12f-186">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ec12f-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec12f-187">System-Only</span></span>            | <span data-ttu-id="ec12f-188">Faux</span><span class="sxs-lookup"><span data-stu-id="ec12f-188">False</span></span>                           |
| <span data-ttu-id="ec12f-189">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ec12f-189">Is-Single-Valued</span></span>       | <span data-ttu-id="ec12f-190">Vrai</span><span class="sxs-lookup"><span data-stu-id="ec12f-190">True</span></span>                            |
| <span data-ttu-id="ec12f-191">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ec12f-191">Is Indexed</span></span>             | <span data-ttu-id="ec12f-192">Faux</span><span class="sxs-lookup"><span data-stu-id="ec12f-192">False</span></span>                           |
| <span data-ttu-id="ec12f-193">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ec12f-193">In Global Catalog</span></span>      | <span data-ttu-id="ec12f-194">Faux</span><span class="sxs-lookup"><span data-stu-id="ec12f-194">False</span></span>                           |
| <span data-ttu-id="ec12f-195">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ec12f-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec12f-196">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ec12f-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ec12f-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec12f-197">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ec12f-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec12f-198">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ec12f-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec12f-199">Search-Flags</span></span>           | <span data-ttu-id="ec12f-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec12f-200">0x00000000</span></span>                      |
| <span data-ttu-id="ec12f-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec12f-201">System-Flags</span></span>           | <span data-ttu-id="ec12f-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ec12f-202">0x00000010</span></span>                      |
| <span data-ttu-id="ec12f-203">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ec12f-203">Classes used in</span></span>        | [<span data-ttu-id="ec12f-204">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="ec12f-204">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ec12f-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ec12f-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ec12f-206">Entrée</span><span class="sxs-lookup"><span data-stu-id="ec12f-206">Entry</span></span> | <span data-ttu-id="ec12f-207">Valeur</span><span class="sxs-lookup"><span data-stu-id="ec12f-207">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ec12f-208">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ec12f-208">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="ec12f-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec12f-209">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="ec12f-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec12f-210">System-Only</span></span>            | <span data-ttu-id="ec12f-211">Faux</span><span class="sxs-lookup"><span data-stu-id="ec12f-211">False</span></span>                                                                                 |
| <span data-ttu-id="ec12f-212">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ec12f-212">Is-Single-Valued</span></span>       | <span data-ttu-id="ec12f-213">Vrai</span><span class="sxs-lookup"><span data-stu-id="ec12f-213">True</span></span>                                                                                  |
| <span data-ttu-id="ec12f-214">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ec12f-214">Is Indexed</span></span>             | <span data-ttu-id="ec12f-215">Faux</span><span class="sxs-lookup"><span data-stu-id="ec12f-215">False</span></span>                                                                                 |
| <span data-ttu-id="ec12f-216">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ec12f-216">In Global Catalog</span></span>      | <span data-ttu-id="ec12f-217">Faux</span><span class="sxs-lookup"><span data-stu-id="ec12f-217">False</span></span>                                                                                 |
| <span data-ttu-id="ec12f-218">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ec12f-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec12f-219">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ec12f-219">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="ec12f-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec12f-220">Range-Lower</span></span>            | \-                                                                                    |
| <span data-ttu-id="ec12f-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec12f-221">Range-Upper</span></span>            | \-                                                                                    |
| <span data-ttu-id="ec12f-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec12f-222">Search-Flags</span></span>           | <span data-ttu-id="ec12f-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec12f-223">0x00000000</span></span>                                                                            |
| <span data-ttu-id="ec12f-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec12f-224">System-Flags</span></span>           | <span data-ttu-id="ec12f-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ec12f-225">0x00000010</span></span>                                                                            |
| <span data-ttu-id="ec12f-226">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ec12f-226">Classes used in</span></span>        | [<span data-ttu-id="ec12f-227">**Sam-domaine-base**</span><span class="sxs-lookup"><span data-stu-id="ec12f-227">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> [<span data-ttu-id="ec12f-228">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="ec12f-228">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ec12f-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ec12f-229">Windows Server 2008</span></span>



| <span data-ttu-id="ec12f-230">Entrée</span><span class="sxs-lookup"><span data-stu-id="ec12f-230">Entry</span></span> | <span data-ttu-id="ec12f-231">Valeur</span><span class="sxs-lookup"><span data-stu-id="ec12f-231">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ec12f-232">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ec12f-232">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="ec12f-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec12f-233">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="ec12f-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec12f-234">System-Only</span></span>            | <span data-ttu-id="ec12f-235">Faux</span><span class="sxs-lookup"><span data-stu-id="ec12f-235">False</span></span>                                                                                 |
| <span data-ttu-id="ec12f-236">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ec12f-236">Is-Single-Valued</span></span>       | <span data-ttu-id="ec12f-237">Vrai</span><span class="sxs-lookup"><span data-stu-id="ec12f-237">True</span></span>                                                                                  |
| <span data-ttu-id="ec12f-238">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ec12f-238">Is Indexed</span></span>             | <span data-ttu-id="ec12f-239">Faux</span><span class="sxs-lookup"><span data-stu-id="ec12f-239">False</span></span>                                                                                 |
| <span data-ttu-id="ec12f-240">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ec12f-240">In Global Catalog</span></span>      | <span data-ttu-id="ec12f-241">Faux</span><span class="sxs-lookup"><span data-stu-id="ec12f-241">False</span></span>                                                                                 |
| <span data-ttu-id="ec12f-242">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ec12f-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec12f-243">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ec12f-243">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="ec12f-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec12f-244">Range-Lower</span></span>            | \-                                                                                    |
| <span data-ttu-id="ec12f-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec12f-245">Range-Upper</span></span>            | \-                                                                                    |
| <span data-ttu-id="ec12f-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec12f-246">Search-Flags</span></span>           | <span data-ttu-id="ec12f-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec12f-247">0x00000000</span></span>                                                                            |
| <span data-ttu-id="ec12f-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec12f-248">System-Flags</span></span>           | <span data-ttu-id="ec12f-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ec12f-249">0x00000010</span></span>                                                                            |
| <span data-ttu-id="ec12f-250">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ec12f-250">Classes used in</span></span>        | [<span data-ttu-id="ec12f-251">**Sam-domaine-base**</span><span class="sxs-lookup"><span data-stu-id="ec12f-251">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> [<span data-ttu-id="ec12f-252">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="ec12f-252">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ec12f-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ec12f-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ec12f-254">Entrée</span><span class="sxs-lookup"><span data-stu-id="ec12f-254">Entry</span></span> | <span data-ttu-id="ec12f-255">Valeur</span><span class="sxs-lookup"><span data-stu-id="ec12f-255">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ec12f-256">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ec12f-256">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="ec12f-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec12f-257">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="ec12f-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec12f-258">System-Only</span></span>            | <span data-ttu-id="ec12f-259">Faux</span><span class="sxs-lookup"><span data-stu-id="ec12f-259">False</span></span>                                                                                 |
| <span data-ttu-id="ec12f-260">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ec12f-260">Is-Single-Valued</span></span>       | <span data-ttu-id="ec12f-261">Vrai</span><span class="sxs-lookup"><span data-stu-id="ec12f-261">True</span></span>                                                                                  |
| <span data-ttu-id="ec12f-262">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ec12f-262">Is Indexed</span></span>             | <span data-ttu-id="ec12f-263">Faux</span><span class="sxs-lookup"><span data-stu-id="ec12f-263">False</span></span>                                                                                 |
| <span data-ttu-id="ec12f-264">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ec12f-264">In Global Catalog</span></span>      | <span data-ttu-id="ec12f-265">Faux</span><span class="sxs-lookup"><span data-stu-id="ec12f-265">False</span></span>                                                                                 |
| <span data-ttu-id="ec12f-266">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ec12f-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec12f-267">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ec12f-267">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="ec12f-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec12f-268">Range-Lower</span></span>            | \-                                                                                    |
| <span data-ttu-id="ec12f-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec12f-269">Range-Upper</span></span>            | \-                                                                                    |
| <span data-ttu-id="ec12f-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec12f-270">Search-Flags</span></span>           | <span data-ttu-id="ec12f-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec12f-271">0x00000000</span></span>                                                                            |
| <span data-ttu-id="ec12f-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec12f-272">System-Flags</span></span>           | <span data-ttu-id="ec12f-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ec12f-273">0x00000010</span></span>                                                                            |
| <span data-ttu-id="ec12f-274">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ec12f-274">Classes used in</span></span>        | [<span data-ttu-id="ec12f-275">**Sam-domaine-base**</span><span class="sxs-lookup"><span data-stu-id="ec12f-275">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> [<span data-ttu-id="ec12f-276">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="ec12f-276">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ec12f-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ec12f-277">Windows Server 2012</span></span>



| <span data-ttu-id="ec12f-278">Entrée</span><span class="sxs-lookup"><span data-stu-id="ec12f-278">Entry</span></span> | <span data-ttu-id="ec12f-279">Valeur</span><span class="sxs-lookup"><span data-stu-id="ec12f-279">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ec12f-280">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ec12f-280">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="ec12f-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec12f-281">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="ec12f-282">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec12f-282">System-Only</span></span>            | <span data-ttu-id="ec12f-283">Faux</span><span class="sxs-lookup"><span data-stu-id="ec12f-283">False</span></span>                                                                                 |
| <span data-ttu-id="ec12f-284">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ec12f-284">Is-Single-Valued</span></span>       | <span data-ttu-id="ec12f-285">Vrai</span><span class="sxs-lookup"><span data-stu-id="ec12f-285">True</span></span>                                                                                  |
| <span data-ttu-id="ec12f-286">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ec12f-286">Is Indexed</span></span>             | <span data-ttu-id="ec12f-287">Faux</span><span class="sxs-lookup"><span data-stu-id="ec12f-287">False</span></span>                                                                                 |
| <span data-ttu-id="ec12f-288">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ec12f-288">In Global Catalog</span></span>      | <span data-ttu-id="ec12f-289">Faux</span><span class="sxs-lookup"><span data-stu-id="ec12f-289">False</span></span>                                                                                 |
| <span data-ttu-id="ec12f-290">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ec12f-290">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec12f-291">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ec12f-291">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="ec12f-292">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec12f-292">Range-Lower</span></span>            | \-                                                                                    |
| <span data-ttu-id="ec12f-293">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec12f-293">Range-Upper</span></span>            | \-                                                                                    |
| <span data-ttu-id="ec12f-294">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec12f-294">Search-Flags</span></span>           | <span data-ttu-id="ec12f-295">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec12f-295">0x00000000</span></span>                                                                            |
| <span data-ttu-id="ec12f-296">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec12f-296">System-Flags</span></span>           | <span data-ttu-id="ec12f-297">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ec12f-297">0x00000010</span></span>                                                                            |
| <span data-ttu-id="ec12f-298">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ec12f-298">Classes used in</span></span>        | [<span data-ttu-id="ec12f-299">**Sam-domaine-base**</span><span class="sxs-lookup"><span data-stu-id="ec12f-299">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> [<span data-ttu-id="ec12f-300">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="ec12f-300">**Top**</span></span>](c-top.md)<br/> |



 

 





