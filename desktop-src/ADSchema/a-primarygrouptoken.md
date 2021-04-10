---
title: Attribut Primary-Group-Token
description: Attribut calculé utilisé pour récupérer la liste d’appartenance d’un groupe, par exemple les utilisateurs du domaine. L’appartenance complète de ces groupes n’est pas stockée explicitement pour des raisons de mise à l’échelle.
ms.assetid: b23d3b7f-074b-4f1b-bc06-b22738a8a79e
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory de l’attribut Primary-Group-Token
- Schéma AD de l’attribut primaryGroupToken
topic_type:
- apiref
api_name:
- Primary-Group-Token
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b237ab5998ca3f38f2d07128b36d9337c96935d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107608"
---
# <a name="primary-group-token-attribute"></a><span data-ttu-id="03b85-106">Attribut Primary-Group-Token</span><span class="sxs-lookup"><span data-stu-id="03b85-106">Primary-Group-Token attribute</span></span>

<span data-ttu-id="03b85-107">Attribut calculé utilisé pour récupérer la liste d’appartenance d’un groupe, par exemple les utilisateurs du domaine.</span><span class="sxs-lookup"><span data-stu-id="03b85-107">A computed attribute that is used in retrieving the membership list of a group, such as Domain Users.</span></span> <span data-ttu-id="03b85-108">L’appartenance complète de ces groupes n’est pas stockée explicitement pour des raisons de mise à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="03b85-108">The complete membership of such groups is not stored explicitly for scaling reasons.</span></span>



| <span data-ttu-id="03b85-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="03b85-109">Entry</span></span> | <span data-ttu-id="03b85-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="03b85-110">Value</span></span> |
|-------------------|--------------------------------------------|
| <span data-ttu-id="03b85-111">CN</span><span class="sxs-lookup"><span data-stu-id="03b85-111">CN</span></span>                | <span data-ttu-id="03b85-112">Primary-Group-Token</span><span class="sxs-lookup"><span data-stu-id="03b85-112">Primary-Group-Token</span></span>                        |
| <span data-ttu-id="03b85-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="03b85-113">Ldap-Display-Name</span></span> | <span data-ttu-id="03b85-114">primaryGroupToken</span><span class="sxs-lookup"><span data-stu-id="03b85-114">primaryGroupToken</span></span>                          |
| <span data-ttu-id="03b85-115">Taille</span><span class="sxs-lookup"><span data-stu-id="03b85-115">Size</span></span>              | <span data-ttu-id="03b85-116">4 octets</span><span class="sxs-lookup"><span data-stu-id="03b85-116">4 bytes</span></span>                                    |
| <span data-ttu-id="03b85-117">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="03b85-117">Update Privilege</span></span>  | <span data-ttu-id="03b85-118">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="03b85-118">This value is set by the system.</span></span>           |
| <span data-ttu-id="03b85-119">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="03b85-119">Update Frequency</span></span>  | <span data-ttu-id="03b85-120">À chaque fois qu’un groupe principal d’objets change.</span><span class="sxs-lookup"><span data-stu-id="03b85-120">Whenever an objects primary group changes.</span></span> |
| <span data-ttu-id="03b85-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="03b85-121">Attribute-Id</span></span>      | <span data-ttu-id="03b85-122">1.2.840.113556.1.4.1412</span><span class="sxs-lookup"><span data-stu-id="03b85-122">1.2.840.113556.1.4.1412</span></span>                    |
| <span data-ttu-id="03b85-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="03b85-123">System-Id-Guid</span></span>    | <span data-ttu-id="03b85-124">c0ed8738-7efd-4481-84d9-66d2db8be369</span><span class="sxs-lookup"><span data-stu-id="03b85-124">c0ed8738-7efd-4481-84d9-66d2db8be369</span></span>       |
| <span data-ttu-id="03b85-125">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="03b85-125">Syntax</span></span>            | [<span data-ttu-id="03b85-126">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="03b85-126">**Enumeration**</span></span>](s-enumeration.md)       |



## <a name="implementations"></a><span data-ttu-id="03b85-127">Implémentations</span><span class="sxs-lookup"><span data-stu-id="03b85-127">Implementations</span></span>

-   [<span data-ttu-id="03b85-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="03b85-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="03b85-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="03b85-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="03b85-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="03b85-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="03b85-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="03b85-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="03b85-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="03b85-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="03b85-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="03b85-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="03b85-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="03b85-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="03b85-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="03b85-135">Windows 2000 Server</span></span>



| <span data-ttu-id="03b85-136">Entrée</span><span class="sxs-lookup"><span data-stu-id="03b85-136">Entry</span></span> | <span data-ttu-id="03b85-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="03b85-137">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="03b85-138">ID de lien</span><span class="sxs-lookup"><span data-stu-id="03b85-138">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="03b85-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="03b85-139">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="03b85-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="03b85-140">System-Only</span></span>            | <span data-ttu-id="03b85-141">Vrai</span><span class="sxs-lookup"><span data-stu-id="03b85-141">True</span></span>                                |
| <span data-ttu-id="03b85-142">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="03b85-142">Is-Single-Valued</span></span>       | <span data-ttu-id="03b85-143">Vrai</span><span class="sxs-lookup"><span data-stu-id="03b85-143">True</span></span>                                |
| <span data-ttu-id="03b85-144">Est indexé</span><span class="sxs-lookup"><span data-stu-id="03b85-144">Is Indexed</span></span>             | <span data-ttu-id="03b85-145">Faux</span><span class="sxs-lookup"><span data-stu-id="03b85-145">False</span></span>                               |
| <span data-ttu-id="03b85-146">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="03b85-146">In Global Catalog</span></span>      | <span data-ttu-id="03b85-147">Faux</span><span class="sxs-lookup"><span data-stu-id="03b85-147">False</span></span>                               |
| <span data-ttu-id="03b85-148">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="03b85-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="03b85-149">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="03b85-149">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="03b85-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="03b85-150">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="03b85-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="03b85-151">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="03b85-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="03b85-152">Search-Flags</span></span>           | <span data-ttu-id="03b85-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="03b85-153">0x00000000</span></span>                          |
| <span data-ttu-id="03b85-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="03b85-154">System-Flags</span></span>           | <span data-ttu-id="03b85-155">0x00000014</span><span class="sxs-lookup"><span data-stu-id="03b85-155">0x00000014</span></span>                          |
| <span data-ttu-id="03b85-156">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="03b85-156">Classes used in</span></span>        | [<span data-ttu-id="03b85-157">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="03b85-157">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="03b85-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="03b85-158">Windows Server 2003</span></span>



| <span data-ttu-id="03b85-159">Entrée</span><span class="sxs-lookup"><span data-stu-id="03b85-159">Entry</span></span> | <span data-ttu-id="03b85-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="03b85-160">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="03b85-161">ID de lien</span><span class="sxs-lookup"><span data-stu-id="03b85-161">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="03b85-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="03b85-162">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="03b85-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="03b85-163">System-Only</span></span>            | <span data-ttu-id="03b85-164">Vrai</span><span class="sxs-lookup"><span data-stu-id="03b85-164">True</span></span>                                |
| <span data-ttu-id="03b85-165">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="03b85-165">Is-Single-Valued</span></span>       | <span data-ttu-id="03b85-166">Vrai</span><span class="sxs-lookup"><span data-stu-id="03b85-166">True</span></span>                                |
| <span data-ttu-id="03b85-167">Est indexé</span><span class="sxs-lookup"><span data-stu-id="03b85-167">Is Indexed</span></span>             | <span data-ttu-id="03b85-168">Faux</span><span class="sxs-lookup"><span data-stu-id="03b85-168">False</span></span>                               |
| <span data-ttu-id="03b85-169">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="03b85-169">In Global Catalog</span></span>      | <span data-ttu-id="03b85-170">Faux</span><span class="sxs-lookup"><span data-stu-id="03b85-170">False</span></span>                               |
| <span data-ttu-id="03b85-171">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="03b85-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="03b85-172">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="03b85-172">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="03b85-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="03b85-173">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="03b85-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="03b85-174">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="03b85-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="03b85-175">Search-Flags</span></span>           | <span data-ttu-id="03b85-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="03b85-176">0x00000000</span></span>                          |
| <span data-ttu-id="03b85-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="03b85-177">System-Flags</span></span>           | <span data-ttu-id="03b85-178">0x00000014</span><span class="sxs-lookup"><span data-stu-id="03b85-178">0x00000014</span></span>                          |
| <span data-ttu-id="03b85-179">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="03b85-179">Classes used in</span></span>        | [<span data-ttu-id="03b85-180">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="03b85-180">**Group**</span></span>](c-group.md)<br/> |



## <a name="adam"></a><span data-ttu-id="03b85-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="03b85-181">ADAM</span></span>



| <span data-ttu-id="03b85-182">Entrée</span><span class="sxs-lookup"><span data-stu-id="03b85-182">Entry</span></span> | <span data-ttu-id="03b85-183">Valeur</span><span class="sxs-lookup"><span data-stu-id="03b85-183">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="03b85-184">ID de lien</span><span class="sxs-lookup"><span data-stu-id="03b85-184">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="03b85-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="03b85-185">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="03b85-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="03b85-186">System-Only</span></span>            | <span data-ttu-id="03b85-187">Vrai</span><span class="sxs-lookup"><span data-stu-id="03b85-187">True</span></span>                                |
| <span data-ttu-id="03b85-188">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="03b85-188">Is-Single-Valued</span></span>       | <span data-ttu-id="03b85-189">Vrai</span><span class="sxs-lookup"><span data-stu-id="03b85-189">True</span></span>                                |
| <span data-ttu-id="03b85-190">Est indexé</span><span class="sxs-lookup"><span data-stu-id="03b85-190">Is Indexed</span></span>             | <span data-ttu-id="03b85-191">Faux</span><span class="sxs-lookup"><span data-stu-id="03b85-191">False</span></span>                               |
| <span data-ttu-id="03b85-192">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="03b85-192">In Global Catalog</span></span>      | <span data-ttu-id="03b85-193">Faux</span><span class="sxs-lookup"><span data-stu-id="03b85-193">False</span></span>                               |
| <span data-ttu-id="03b85-194">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="03b85-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="03b85-195">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="03b85-195">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="03b85-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="03b85-196">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="03b85-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="03b85-197">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="03b85-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="03b85-198">Search-Flags</span></span>           | <span data-ttu-id="03b85-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="03b85-199">0x00000000</span></span>                          |
| <span data-ttu-id="03b85-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="03b85-200">System-Flags</span></span>           | <span data-ttu-id="03b85-201">0x00000014</span><span class="sxs-lookup"><span data-stu-id="03b85-201">0x00000014</span></span>                          |
| <span data-ttu-id="03b85-202">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="03b85-202">Classes used in</span></span>        | [<span data-ttu-id="03b85-203">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="03b85-203">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="03b85-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="03b85-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="03b85-205">Entrée</span><span class="sxs-lookup"><span data-stu-id="03b85-205">Entry</span></span> | <span data-ttu-id="03b85-206">Valeur</span><span class="sxs-lookup"><span data-stu-id="03b85-206">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="03b85-207">ID de lien</span><span class="sxs-lookup"><span data-stu-id="03b85-207">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="03b85-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="03b85-208">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="03b85-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="03b85-209">System-Only</span></span>            | <span data-ttu-id="03b85-210">Vrai</span><span class="sxs-lookup"><span data-stu-id="03b85-210">True</span></span>                                |
| <span data-ttu-id="03b85-211">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="03b85-211">Is-Single-Valued</span></span>       | <span data-ttu-id="03b85-212">Vrai</span><span class="sxs-lookup"><span data-stu-id="03b85-212">True</span></span>                                |
| <span data-ttu-id="03b85-213">Est indexé</span><span class="sxs-lookup"><span data-stu-id="03b85-213">Is Indexed</span></span>             | <span data-ttu-id="03b85-214">Faux</span><span class="sxs-lookup"><span data-stu-id="03b85-214">False</span></span>                               |
| <span data-ttu-id="03b85-215">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="03b85-215">In Global Catalog</span></span>      | <span data-ttu-id="03b85-216">Faux</span><span class="sxs-lookup"><span data-stu-id="03b85-216">False</span></span>                               |
| <span data-ttu-id="03b85-217">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="03b85-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="03b85-218">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="03b85-218">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="03b85-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="03b85-219">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="03b85-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="03b85-220">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="03b85-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="03b85-221">Search-Flags</span></span>           | <span data-ttu-id="03b85-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="03b85-222">0x00000000</span></span>                          |
| <span data-ttu-id="03b85-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="03b85-223">System-Flags</span></span>           | <span data-ttu-id="03b85-224">0x00000014</span><span class="sxs-lookup"><span data-stu-id="03b85-224">0x00000014</span></span>                          |
| <span data-ttu-id="03b85-225">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="03b85-225">Classes used in</span></span>        | [<span data-ttu-id="03b85-226">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="03b85-226">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="03b85-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="03b85-227">Windows Server 2008</span></span>



| <span data-ttu-id="03b85-228">Entrée</span><span class="sxs-lookup"><span data-stu-id="03b85-228">Entry</span></span> | <span data-ttu-id="03b85-229">Valeur</span><span class="sxs-lookup"><span data-stu-id="03b85-229">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="03b85-230">ID de lien</span><span class="sxs-lookup"><span data-stu-id="03b85-230">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="03b85-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="03b85-231">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="03b85-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="03b85-232">System-Only</span></span>            | <span data-ttu-id="03b85-233">Vrai</span><span class="sxs-lookup"><span data-stu-id="03b85-233">True</span></span>                                |
| <span data-ttu-id="03b85-234">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="03b85-234">Is-Single-Valued</span></span>       | <span data-ttu-id="03b85-235">Vrai</span><span class="sxs-lookup"><span data-stu-id="03b85-235">True</span></span>                                |
| <span data-ttu-id="03b85-236">Est indexé</span><span class="sxs-lookup"><span data-stu-id="03b85-236">Is Indexed</span></span>             | <span data-ttu-id="03b85-237">Faux</span><span class="sxs-lookup"><span data-stu-id="03b85-237">False</span></span>                               |
| <span data-ttu-id="03b85-238">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="03b85-238">In Global Catalog</span></span>      | <span data-ttu-id="03b85-239">Faux</span><span class="sxs-lookup"><span data-stu-id="03b85-239">False</span></span>                               |
| <span data-ttu-id="03b85-240">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="03b85-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="03b85-241">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="03b85-241">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="03b85-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="03b85-242">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="03b85-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="03b85-243">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="03b85-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="03b85-244">Search-Flags</span></span>           | <span data-ttu-id="03b85-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="03b85-245">0x00000000</span></span>                          |
| <span data-ttu-id="03b85-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="03b85-246">System-Flags</span></span>           | <span data-ttu-id="03b85-247">0x00000014</span><span class="sxs-lookup"><span data-stu-id="03b85-247">0x00000014</span></span>                          |
| <span data-ttu-id="03b85-248">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="03b85-248">Classes used in</span></span>        | [<span data-ttu-id="03b85-249">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="03b85-249">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="03b85-250">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="03b85-250">Windows Server 2008 R2</span></span>



| <span data-ttu-id="03b85-251">Entrée</span><span class="sxs-lookup"><span data-stu-id="03b85-251">Entry</span></span> | <span data-ttu-id="03b85-252">Valeur</span><span class="sxs-lookup"><span data-stu-id="03b85-252">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="03b85-253">ID de lien</span><span class="sxs-lookup"><span data-stu-id="03b85-253">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="03b85-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="03b85-254">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="03b85-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="03b85-255">System-Only</span></span>            | <span data-ttu-id="03b85-256">Vrai</span><span class="sxs-lookup"><span data-stu-id="03b85-256">True</span></span>                                |
| <span data-ttu-id="03b85-257">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="03b85-257">Is-Single-Valued</span></span>       | <span data-ttu-id="03b85-258">Vrai</span><span class="sxs-lookup"><span data-stu-id="03b85-258">True</span></span>                                |
| <span data-ttu-id="03b85-259">Est indexé</span><span class="sxs-lookup"><span data-stu-id="03b85-259">Is Indexed</span></span>             | <span data-ttu-id="03b85-260">Faux</span><span class="sxs-lookup"><span data-stu-id="03b85-260">False</span></span>                               |
| <span data-ttu-id="03b85-261">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="03b85-261">In Global Catalog</span></span>      | <span data-ttu-id="03b85-262">Faux</span><span class="sxs-lookup"><span data-stu-id="03b85-262">False</span></span>                               |
| <span data-ttu-id="03b85-263">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="03b85-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="03b85-264">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="03b85-264">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="03b85-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="03b85-265">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="03b85-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="03b85-266">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="03b85-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="03b85-267">Search-Flags</span></span>           | <span data-ttu-id="03b85-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="03b85-268">0x00000000</span></span>                          |
| <span data-ttu-id="03b85-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="03b85-269">System-Flags</span></span>           | <span data-ttu-id="03b85-270">0x00000014</span><span class="sxs-lookup"><span data-stu-id="03b85-270">0x00000014</span></span>                          |
| <span data-ttu-id="03b85-271">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="03b85-271">Classes used in</span></span>        | [<span data-ttu-id="03b85-272">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="03b85-272">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="03b85-273">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="03b85-273">Windows Server 2012</span></span>



| <span data-ttu-id="03b85-274">Entrée</span><span class="sxs-lookup"><span data-stu-id="03b85-274">Entry</span></span> | <span data-ttu-id="03b85-275">Valeur</span><span class="sxs-lookup"><span data-stu-id="03b85-275">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="03b85-276">ID de lien</span><span class="sxs-lookup"><span data-stu-id="03b85-276">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="03b85-277">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="03b85-277">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="03b85-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="03b85-278">System-Only</span></span>            | <span data-ttu-id="03b85-279">Vrai</span><span class="sxs-lookup"><span data-stu-id="03b85-279">True</span></span>                                |
| <span data-ttu-id="03b85-280">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="03b85-280">Is-Single-Valued</span></span>       | <span data-ttu-id="03b85-281">Vrai</span><span class="sxs-lookup"><span data-stu-id="03b85-281">True</span></span>                                |
| <span data-ttu-id="03b85-282">Est indexé</span><span class="sxs-lookup"><span data-stu-id="03b85-282">Is Indexed</span></span>             | <span data-ttu-id="03b85-283">Faux</span><span class="sxs-lookup"><span data-stu-id="03b85-283">False</span></span>                               |
| <span data-ttu-id="03b85-284">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="03b85-284">In Global Catalog</span></span>      | <span data-ttu-id="03b85-285">Faux</span><span class="sxs-lookup"><span data-stu-id="03b85-285">False</span></span>                               |
| <span data-ttu-id="03b85-286">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="03b85-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="03b85-287">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="03b85-287">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="03b85-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="03b85-288">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="03b85-289">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="03b85-289">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="03b85-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="03b85-290">Search-Flags</span></span>           | <span data-ttu-id="03b85-291">0x00000000</span><span class="sxs-lookup"><span data-stu-id="03b85-291">0x00000000</span></span>                          |
| <span data-ttu-id="03b85-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="03b85-292">System-Flags</span></span>           | <span data-ttu-id="03b85-293">0x00000014</span><span class="sxs-lookup"><span data-stu-id="03b85-293">0x00000014</span></span>                          |
| <span data-ttu-id="03b85-294">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="03b85-294">Classes used in</span></span>        | [<span data-ttu-id="03b85-295">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="03b85-295">**Group**</span></span>](c-group.md)<br/> |



 

 





