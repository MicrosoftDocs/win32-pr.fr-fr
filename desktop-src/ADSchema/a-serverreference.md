---
title: Attribut Server-Reference
description: Trouvé dans un objet ordinateur de site. Contient le nom unique du contrôleur de domaine dans le contexte d’appellation du domaine.
ms.assetid: 6c0ebe85-b4ed-4284-ad96-0b711d5acce7
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Server-Reference
- Schéma AD de l’attribut serverReference
topic_type:
- apiref
api_name:
- Server-Reference
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83fed3b44feeaccb87cb1f55435bbac915c1c262
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845305"
---
# <a name="server-reference-attribute"></a><span data-ttu-id="14faf-106">Attribut Server-Reference</span><span class="sxs-lookup"><span data-stu-id="14faf-106">Server-Reference attribute</span></span>

<span data-ttu-id="14faf-107">Trouvé dans un objet ordinateur de site.</span><span class="sxs-lookup"><span data-stu-id="14faf-107">Found in a site computer object.</span></span> <span data-ttu-id="14faf-108">Contient le nom unique du contrôleur de domaine dans le contexte d’appellation du domaine.</span><span class="sxs-lookup"><span data-stu-id="14faf-108">Contains the distinguished name of the domain controller in the domain naming context.</span></span>



| <span data-ttu-id="14faf-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="14faf-109">Entry</span></span> | <span data-ttu-id="14faf-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="14faf-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="14faf-111">CN</span><span class="sxs-lookup"><span data-stu-id="14faf-111">CN</span></span>                | <span data-ttu-id="14faf-112">Server-Reference</span><span class="sxs-lookup"><span data-stu-id="14faf-112">Server-Reference</span></span>                        |
| <span data-ttu-id="14faf-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="14faf-113">Ldap-Display-Name</span></span> | <span data-ttu-id="14faf-114">serverReference</span><span class="sxs-lookup"><span data-stu-id="14faf-114">serverReference</span></span>                         |
| <span data-ttu-id="14faf-115">Taille</span><span class="sxs-lookup"><span data-stu-id="14faf-115">Size</span></span>              | \-                                      |
| <span data-ttu-id="14faf-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="14faf-116">Update Privilege</span></span>  | <span data-ttu-id="14faf-117">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="14faf-117">This value is set by the system.</span></span>        |
| <span data-ttu-id="14faf-118">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="14faf-118">Update Frequency</span></span>  | <span data-ttu-id="14faf-119">Chaque fois qu’un site est créé.</span><span class="sxs-lookup"><span data-stu-id="14faf-119">Whenever a site is created.</span></span>             |
| <span data-ttu-id="14faf-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="14faf-120">Attribute-Id</span></span>      | <span data-ttu-id="14faf-121">1.2.840.113556.1.4.515</span><span class="sxs-lookup"><span data-stu-id="14faf-121">1.2.840.113556.1.4.515</span></span>                  |
| <span data-ttu-id="14faf-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="14faf-122">System-Id-Guid</span></span>    | <span data-ttu-id="14faf-123">26d9736d-6070-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="14faf-123">26d9736d-6070-11d1-a9c6-0000f80367c1</span></span>    |
| <span data-ttu-id="14faf-124">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="14faf-124">Syntax</span></span>            | [<span data-ttu-id="14faf-125">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="14faf-125">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="14faf-126">Implémentations</span><span class="sxs-lookup"><span data-stu-id="14faf-126">Implementations</span></span>

-   [<span data-ttu-id="14faf-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="14faf-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="14faf-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="14faf-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="14faf-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="14faf-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="14faf-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="14faf-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="14faf-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="14faf-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="14faf-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="14faf-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="14faf-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="14faf-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="14faf-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="14faf-134">Windows 2000 Server</span></span>



| <span data-ttu-id="14faf-135">Entrée</span><span class="sxs-lookup"><span data-stu-id="14faf-135">Entry</span></span> | <span data-ttu-id="14faf-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="14faf-136">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14faf-137">ID de lien</span><span class="sxs-lookup"><span data-stu-id="14faf-137">Link-Id</span></span>                | <span data-ttu-id="14faf-138">94</span><span class="sxs-lookup"><span data-stu-id="14faf-138">94</span></span>                                                                                                                              |
| <span data-ttu-id="14faf-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="14faf-139">MAPI-Id</span></span>                | \-                                                                                                                              |
| <span data-ttu-id="14faf-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="14faf-140">System-Only</span></span>            | <span data-ttu-id="14faf-141">Faux</span><span class="sxs-lookup"><span data-stu-id="14faf-141">False</span></span>                                                                                                                           |
| <span data-ttu-id="14faf-142">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="14faf-142">Is-Single-Valued</span></span>       | <span data-ttu-id="14faf-143">Vrai</span><span class="sxs-lookup"><span data-stu-id="14faf-143">True</span></span>                                                                                                                            |
| <span data-ttu-id="14faf-144">Est indexé</span><span class="sxs-lookup"><span data-stu-id="14faf-144">Is Indexed</span></span>             | <span data-ttu-id="14faf-145">Faux</span><span class="sxs-lookup"><span data-stu-id="14faf-145">False</span></span>                                                                                                                           |
| <span data-ttu-id="14faf-146">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="14faf-146">In Global Catalog</span></span>      | <span data-ttu-id="14faf-147">Faux</span><span class="sxs-lookup"><span data-stu-id="14faf-147">False</span></span>                                                                                                                           |
| <span data-ttu-id="14faf-148">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="14faf-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="14faf-149">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="14faf-149">O:BAG:BAD:S:</span></span>                                                                                                                    |
| <span data-ttu-id="14faf-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="14faf-150">Range-Lower</span></span>            | \-                                                                                                                              |
| <span data-ttu-id="14faf-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="14faf-151">Range-Upper</span></span>            | \-                                                                                                                              |
| <span data-ttu-id="14faf-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="14faf-152">Search-Flags</span></span>           | <span data-ttu-id="14faf-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="14faf-153">0x00000000</span></span>                                                                                                                      |
| <span data-ttu-id="14faf-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="14faf-154">System-Flags</span></span>           | <span data-ttu-id="14faf-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="14faf-155">0x00000010</span></span>                                                                                                                      |
| <span data-ttu-id="14faf-156">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="14faf-156">Classes used in</span></span>        | [<span data-ttu-id="14faf-157">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="14faf-157">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> [<span data-ttu-id="14faf-158">**NTFRS-Member**</span><span class="sxs-lookup"><span data-stu-id="14faf-158">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="14faf-159">**Serveur**</span><span class="sxs-lookup"><span data-stu-id="14faf-159">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="14faf-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="14faf-160">Windows Server 2003</span></span>



| <span data-ttu-id="14faf-161">Entrée</span><span class="sxs-lookup"><span data-stu-id="14faf-161">Entry</span></span> | <span data-ttu-id="14faf-162">Valeur</span><span class="sxs-lookup"><span data-stu-id="14faf-162">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14faf-163">ID de lien</span><span class="sxs-lookup"><span data-stu-id="14faf-163">Link-Id</span></span>                | <span data-ttu-id="14faf-164">94</span><span class="sxs-lookup"><span data-stu-id="14faf-164">94</span></span>                                                                                                                              |
| <span data-ttu-id="14faf-165">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="14faf-165">MAPI-Id</span></span>                | \-                                                                                                                              |
| <span data-ttu-id="14faf-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="14faf-166">System-Only</span></span>            | <span data-ttu-id="14faf-167">Faux</span><span class="sxs-lookup"><span data-stu-id="14faf-167">False</span></span>                                                                                                                           |
| <span data-ttu-id="14faf-168">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="14faf-168">Is-Single-Valued</span></span>       | <span data-ttu-id="14faf-169">Vrai</span><span class="sxs-lookup"><span data-stu-id="14faf-169">True</span></span>                                                                                                                            |
| <span data-ttu-id="14faf-170">Est indexé</span><span class="sxs-lookup"><span data-stu-id="14faf-170">Is Indexed</span></span>             | <span data-ttu-id="14faf-171">Faux</span><span class="sxs-lookup"><span data-stu-id="14faf-171">False</span></span>                                                                                                                           |
| <span data-ttu-id="14faf-172">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="14faf-172">In Global Catalog</span></span>      | <span data-ttu-id="14faf-173">Faux</span><span class="sxs-lookup"><span data-stu-id="14faf-173">False</span></span>                                                                                                                           |
| <span data-ttu-id="14faf-174">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="14faf-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="14faf-175">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="14faf-175">O:BAG:BAD:S:</span></span>                                                                                                                    |
| <span data-ttu-id="14faf-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="14faf-176">Range-Lower</span></span>            | \-                                                                                                                              |
| <span data-ttu-id="14faf-177">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="14faf-177">Range-Upper</span></span>            | \-                                                                                                                              |
| <span data-ttu-id="14faf-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="14faf-178">Search-Flags</span></span>           | <span data-ttu-id="14faf-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="14faf-179">0x00000000</span></span>                                                                                                                      |
| <span data-ttu-id="14faf-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="14faf-180">System-Flags</span></span>           | <span data-ttu-id="14faf-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="14faf-181">0x00000010</span></span>                                                                                                                      |
| <span data-ttu-id="14faf-182">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="14faf-182">Classes used in</span></span>        | [<span data-ttu-id="14faf-183">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="14faf-183">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> [<span data-ttu-id="14faf-184">**NTFRS-Member**</span><span class="sxs-lookup"><span data-stu-id="14faf-184">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="14faf-185">**Serveur**</span><span class="sxs-lookup"><span data-stu-id="14faf-185">**Server**</span></span>](c-server.md)<br/> |



## <a name="adam"></a><span data-ttu-id="14faf-186">ADAM</span><span class="sxs-lookup"><span data-stu-id="14faf-186">ADAM</span></span>



| <span data-ttu-id="14faf-187">Entrée</span><span class="sxs-lookup"><span data-stu-id="14faf-187">Entry</span></span> | <span data-ttu-id="14faf-188">Valeur</span><span class="sxs-lookup"><span data-stu-id="14faf-188">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="14faf-189">ID de lien</span><span class="sxs-lookup"><span data-stu-id="14faf-189">Link-Id</span></span>                | <span data-ttu-id="14faf-190">94</span><span class="sxs-lookup"><span data-stu-id="14faf-190">94</span></span>                                                                             |
| <span data-ttu-id="14faf-191">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="14faf-191">MAPI-Id</span></span>                | \-                                                                             |
| <span data-ttu-id="14faf-192">System-Only</span><span class="sxs-lookup"><span data-stu-id="14faf-192">System-Only</span></span>            | <span data-ttu-id="14faf-193">Faux</span><span class="sxs-lookup"><span data-stu-id="14faf-193">False</span></span>                                                                          |
| <span data-ttu-id="14faf-194">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="14faf-194">Is-Single-Valued</span></span>       | <span data-ttu-id="14faf-195">Vrai</span><span class="sxs-lookup"><span data-stu-id="14faf-195">True</span></span>                                                                           |
| <span data-ttu-id="14faf-196">Est indexé</span><span class="sxs-lookup"><span data-stu-id="14faf-196">Is Indexed</span></span>             | <span data-ttu-id="14faf-197">Faux</span><span class="sxs-lookup"><span data-stu-id="14faf-197">False</span></span>                                                                          |
| <span data-ttu-id="14faf-198">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="14faf-198">In Global Catalog</span></span>      | <span data-ttu-id="14faf-199">Faux</span><span class="sxs-lookup"><span data-stu-id="14faf-199">False</span></span>                                                                          |
| <span data-ttu-id="14faf-200">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="14faf-200">NT-Security-Descriptor</span></span> | <span data-ttu-id="14faf-201">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="14faf-201">O:BAG:BAD:S:</span></span>                                                                   |
| <span data-ttu-id="14faf-202">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="14faf-202">Range-Lower</span></span>            | \-                                                                             |
| <span data-ttu-id="14faf-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="14faf-203">Range-Upper</span></span>            | \-                                                                             |
| <span data-ttu-id="14faf-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="14faf-204">Search-Flags</span></span>           | <span data-ttu-id="14faf-205">0x00000000</span><span class="sxs-lookup"><span data-stu-id="14faf-205">0x00000000</span></span>                                                                     |
| <span data-ttu-id="14faf-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="14faf-206">System-Flags</span></span>           | <span data-ttu-id="14faf-207">0x00000010</span><span class="sxs-lookup"><span data-stu-id="14faf-207">0x00000010</span></span>                                                                     |
| <span data-ttu-id="14faf-208">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="14faf-208">Classes used in</span></span>        | [<span data-ttu-id="14faf-209">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="14faf-209">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> [<span data-ttu-id="14faf-210">**Serveur**</span><span class="sxs-lookup"><span data-stu-id="14faf-210">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="14faf-211">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="14faf-211">Windows Server 2003 R2</span></span>



| <span data-ttu-id="14faf-212">Entrée</span><span class="sxs-lookup"><span data-stu-id="14faf-212">Entry</span></span> | <span data-ttu-id="14faf-213">Valeur</span><span class="sxs-lookup"><span data-stu-id="14faf-213">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14faf-214">ID de lien</span><span class="sxs-lookup"><span data-stu-id="14faf-214">Link-Id</span></span>                | <span data-ttu-id="14faf-215">94</span><span class="sxs-lookup"><span data-stu-id="14faf-215">94</span></span>                                                                                                                              |
| <span data-ttu-id="14faf-216">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="14faf-216">MAPI-Id</span></span>                | \-                                                                                                                              |
| <span data-ttu-id="14faf-217">System-Only</span><span class="sxs-lookup"><span data-stu-id="14faf-217">System-Only</span></span>            | <span data-ttu-id="14faf-218">Faux</span><span class="sxs-lookup"><span data-stu-id="14faf-218">False</span></span>                                                                                                                           |
| <span data-ttu-id="14faf-219">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="14faf-219">Is-Single-Valued</span></span>       | <span data-ttu-id="14faf-220">Vrai</span><span class="sxs-lookup"><span data-stu-id="14faf-220">True</span></span>                                                                                                                            |
| <span data-ttu-id="14faf-221">Est indexé</span><span class="sxs-lookup"><span data-stu-id="14faf-221">Is Indexed</span></span>             | <span data-ttu-id="14faf-222">Faux</span><span class="sxs-lookup"><span data-stu-id="14faf-222">False</span></span>                                                                                                                           |
| <span data-ttu-id="14faf-223">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="14faf-223">In Global Catalog</span></span>      | <span data-ttu-id="14faf-224">Faux</span><span class="sxs-lookup"><span data-stu-id="14faf-224">False</span></span>                                                                                                                           |
| <span data-ttu-id="14faf-225">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="14faf-225">NT-Security-Descriptor</span></span> | <span data-ttu-id="14faf-226">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="14faf-226">O:BAG:BAD:S:</span></span>                                                                                                                    |
| <span data-ttu-id="14faf-227">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="14faf-227">Range-Lower</span></span>            | \-                                                                                                                              |
| <span data-ttu-id="14faf-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="14faf-228">Range-Upper</span></span>            | \-                                                                                                                              |
| <span data-ttu-id="14faf-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="14faf-229">Search-Flags</span></span>           | <span data-ttu-id="14faf-230">0x00000000</span><span class="sxs-lookup"><span data-stu-id="14faf-230">0x00000000</span></span>                                                                                                                      |
| <span data-ttu-id="14faf-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="14faf-231">System-Flags</span></span>           | <span data-ttu-id="14faf-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="14faf-232">0x00000010</span></span>                                                                                                                      |
| <span data-ttu-id="14faf-233">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="14faf-233">Classes used in</span></span>        | [<span data-ttu-id="14faf-234">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="14faf-234">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> [<span data-ttu-id="14faf-235">**NTFRS-Member**</span><span class="sxs-lookup"><span data-stu-id="14faf-235">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="14faf-236">**Serveur**</span><span class="sxs-lookup"><span data-stu-id="14faf-236">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="14faf-237">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="14faf-237">Windows Server 2008</span></span>



| <span data-ttu-id="14faf-238">Entrée</span><span class="sxs-lookup"><span data-stu-id="14faf-238">Entry</span></span> | <span data-ttu-id="14faf-239">Valeur</span><span class="sxs-lookup"><span data-stu-id="14faf-239">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14faf-240">ID de lien</span><span class="sxs-lookup"><span data-stu-id="14faf-240">Link-Id</span></span>                | <span data-ttu-id="14faf-241">94</span><span class="sxs-lookup"><span data-stu-id="14faf-241">94</span></span>                                                                                                                              |
| <span data-ttu-id="14faf-242">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="14faf-242">MAPI-Id</span></span>                | \-                                                                                                                              |
| <span data-ttu-id="14faf-243">System-Only</span><span class="sxs-lookup"><span data-stu-id="14faf-243">System-Only</span></span>            | <span data-ttu-id="14faf-244">Faux</span><span class="sxs-lookup"><span data-stu-id="14faf-244">False</span></span>                                                                                                                           |
| <span data-ttu-id="14faf-245">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="14faf-245">Is-Single-Valued</span></span>       | <span data-ttu-id="14faf-246">Vrai</span><span class="sxs-lookup"><span data-stu-id="14faf-246">True</span></span>                                                                                                                            |
| <span data-ttu-id="14faf-247">Est indexé</span><span class="sxs-lookup"><span data-stu-id="14faf-247">Is Indexed</span></span>             | <span data-ttu-id="14faf-248">Faux</span><span class="sxs-lookup"><span data-stu-id="14faf-248">False</span></span>                                                                                                                           |
| <span data-ttu-id="14faf-249">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="14faf-249">In Global Catalog</span></span>      | <span data-ttu-id="14faf-250">Faux</span><span class="sxs-lookup"><span data-stu-id="14faf-250">False</span></span>                                                                                                                           |
| <span data-ttu-id="14faf-251">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="14faf-251">NT-Security-Descriptor</span></span> | <span data-ttu-id="14faf-252">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="14faf-252">O:BAG:BAD:S:</span></span>                                                                                                                    |
| <span data-ttu-id="14faf-253">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="14faf-253">Range-Lower</span></span>            | \-                                                                                                                              |
| <span data-ttu-id="14faf-254">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="14faf-254">Range-Upper</span></span>            | \-                                                                                                                              |
| <span data-ttu-id="14faf-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="14faf-255">Search-Flags</span></span>           | <span data-ttu-id="14faf-256">0x00000000</span><span class="sxs-lookup"><span data-stu-id="14faf-256">0x00000000</span></span>                                                                                                                      |
| <span data-ttu-id="14faf-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="14faf-257">System-Flags</span></span>           | <span data-ttu-id="14faf-258">0x00000010</span><span class="sxs-lookup"><span data-stu-id="14faf-258">0x00000010</span></span>                                                                                                                      |
| <span data-ttu-id="14faf-259">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="14faf-259">Classes used in</span></span>        | [<span data-ttu-id="14faf-260">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="14faf-260">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> [<span data-ttu-id="14faf-261">**NTFRS-Member**</span><span class="sxs-lookup"><span data-stu-id="14faf-261">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="14faf-262">**Serveur**</span><span class="sxs-lookup"><span data-stu-id="14faf-262">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="14faf-263">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="14faf-263">Windows Server 2008 R2</span></span>



| <span data-ttu-id="14faf-264">Entrée</span><span class="sxs-lookup"><span data-stu-id="14faf-264">Entry</span></span> | <span data-ttu-id="14faf-265">Valeur</span><span class="sxs-lookup"><span data-stu-id="14faf-265">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14faf-266">ID de lien</span><span class="sxs-lookup"><span data-stu-id="14faf-266">Link-Id</span></span>                | <span data-ttu-id="14faf-267">94</span><span class="sxs-lookup"><span data-stu-id="14faf-267">94</span></span>                                                                                                                              |
| <span data-ttu-id="14faf-268">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="14faf-268">MAPI-Id</span></span>                | \-                                                                                                                              |
| <span data-ttu-id="14faf-269">System-Only</span><span class="sxs-lookup"><span data-stu-id="14faf-269">System-Only</span></span>            | <span data-ttu-id="14faf-270">Faux</span><span class="sxs-lookup"><span data-stu-id="14faf-270">False</span></span>                                                                                                                           |
| <span data-ttu-id="14faf-271">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="14faf-271">Is-Single-Valued</span></span>       | <span data-ttu-id="14faf-272">Vrai</span><span class="sxs-lookup"><span data-stu-id="14faf-272">True</span></span>                                                                                                                            |
| <span data-ttu-id="14faf-273">Est indexé</span><span class="sxs-lookup"><span data-stu-id="14faf-273">Is Indexed</span></span>             | <span data-ttu-id="14faf-274">Faux</span><span class="sxs-lookup"><span data-stu-id="14faf-274">False</span></span>                                                                                                                           |
| <span data-ttu-id="14faf-275">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="14faf-275">In Global Catalog</span></span>      | <span data-ttu-id="14faf-276">Faux</span><span class="sxs-lookup"><span data-stu-id="14faf-276">False</span></span>                                                                                                                           |
| <span data-ttu-id="14faf-277">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="14faf-277">NT-Security-Descriptor</span></span> | <span data-ttu-id="14faf-278">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="14faf-278">O:BAG:BAD:S:</span></span>                                                                                                                    |
| <span data-ttu-id="14faf-279">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="14faf-279">Range-Lower</span></span>            | \-                                                                                                                              |
| <span data-ttu-id="14faf-280">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="14faf-280">Range-Upper</span></span>            | \-                                                                                                                              |
| <span data-ttu-id="14faf-281">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="14faf-281">Search-Flags</span></span>           | <span data-ttu-id="14faf-282">0x00000000</span><span class="sxs-lookup"><span data-stu-id="14faf-282">0x00000000</span></span>                                                                                                                      |
| <span data-ttu-id="14faf-283">System-Flags</span><span class="sxs-lookup"><span data-stu-id="14faf-283">System-Flags</span></span>           | <span data-ttu-id="14faf-284">0x00000010</span><span class="sxs-lookup"><span data-stu-id="14faf-284">0x00000010</span></span>                                                                                                                      |
| <span data-ttu-id="14faf-285">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="14faf-285">Classes used in</span></span>        | [<span data-ttu-id="14faf-286">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="14faf-286">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> [<span data-ttu-id="14faf-287">**NTFRS-Member**</span><span class="sxs-lookup"><span data-stu-id="14faf-287">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="14faf-288">**Serveur**</span><span class="sxs-lookup"><span data-stu-id="14faf-288">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="14faf-289">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="14faf-289">Windows Server 2012</span></span>



| <span data-ttu-id="14faf-290">Entrée</span><span class="sxs-lookup"><span data-stu-id="14faf-290">Entry</span></span> | <span data-ttu-id="14faf-291">Valeur</span><span class="sxs-lookup"><span data-stu-id="14faf-291">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14faf-292">ID de lien</span><span class="sxs-lookup"><span data-stu-id="14faf-292">Link-Id</span></span>                | <span data-ttu-id="14faf-293">94</span><span class="sxs-lookup"><span data-stu-id="14faf-293">94</span></span>                                                                                                                              |
| <span data-ttu-id="14faf-294">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="14faf-294">MAPI-Id</span></span>                | \-                                                                                                                              |
| <span data-ttu-id="14faf-295">System-Only</span><span class="sxs-lookup"><span data-stu-id="14faf-295">System-Only</span></span>            | <span data-ttu-id="14faf-296">Faux</span><span class="sxs-lookup"><span data-stu-id="14faf-296">False</span></span>                                                                                                                           |
| <span data-ttu-id="14faf-297">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="14faf-297">Is-Single-Valued</span></span>       | <span data-ttu-id="14faf-298">Vrai</span><span class="sxs-lookup"><span data-stu-id="14faf-298">True</span></span>                                                                                                                            |
| <span data-ttu-id="14faf-299">Est indexé</span><span class="sxs-lookup"><span data-stu-id="14faf-299">Is Indexed</span></span>             | <span data-ttu-id="14faf-300">Faux</span><span class="sxs-lookup"><span data-stu-id="14faf-300">False</span></span>                                                                                                                           |
| <span data-ttu-id="14faf-301">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="14faf-301">In Global Catalog</span></span>      | <span data-ttu-id="14faf-302">Faux</span><span class="sxs-lookup"><span data-stu-id="14faf-302">False</span></span>                                                                                                                           |
| <span data-ttu-id="14faf-303">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="14faf-303">NT-Security-Descriptor</span></span> | <span data-ttu-id="14faf-304">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="14faf-304">O:BAG:BAD:S:</span></span>                                                                                                                    |
| <span data-ttu-id="14faf-305">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="14faf-305">Range-Lower</span></span>            | \-                                                                                                                              |
| <span data-ttu-id="14faf-306">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="14faf-306">Range-Upper</span></span>            | \-                                                                                                                              |
| <span data-ttu-id="14faf-307">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="14faf-307">Search-Flags</span></span>           | <span data-ttu-id="14faf-308">0x00000000</span><span class="sxs-lookup"><span data-stu-id="14faf-308">0x00000000</span></span>                                                                                                                      |
| <span data-ttu-id="14faf-309">System-Flags</span><span class="sxs-lookup"><span data-stu-id="14faf-309">System-Flags</span></span>           | <span data-ttu-id="14faf-310">0x00000010</span><span class="sxs-lookup"><span data-stu-id="14faf-310">0x00000010</span></span>                                                                                                                      |
| <span data-ttu-id="14faf-311">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="14faf-311">Classes used in</span></span>        | [<span data-ttu-id="14faf-312">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="14faf-312">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> [<span data-ttu-id="14faf-313">**NTFRS-Member**</span><span class="sxs-lookup"><span data-stu-id="14faf-313">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="14faf-314">**Serveurs**</span><span class="sxs-lookup"><span data-stu-id="14faf-314">**Server**</span></span>](c-server.md)<br/> |



 

 





