---
title: Attribut Logon-Count
description: Nombre de fois où le compte s’est connecté avec succès. La valeur 0 indique que la valeur est inconnue.
ms.assetid: 8b12bea7-dfc3-46e3-a4a2-92b5f1239b98
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Logon-Count
- Schéma AD de l’attribut logonCount
topic_type:
- apiref
api_name:
- Logon-Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6ba7865cb3b90f42ede71b169f98f8ce45e722d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845226"
---
# <a name="logon-count-attribute"></a><span data-ttu-id="d3cfb-106">Attribut Logon-Count</span><span class="sxs-lookup"><span data-stu-id="d3cfb-106">Logon-Count attribute</span></span>

<span data-ttu-id="d3cfb-107">Nombre de fois où le compte s’est connecté avec succès.</span><span class="sxs-lookup"><span data-stu-id="d3cfb-107">The number of times the account has successfully logged on.</span></span> <span data-ttu-id="d3cfb-108">La valeur 0 indique que la valeur est inconnue.</span><span class="sxs-lookup"><span data-stu-id="d3cfb-108">A value of 0 indicates that the value is unknown.</span></span>



| <span data-ttu-id="d3cfb-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="d3cfb-109">Entry</span></span> | <span data-ttu-id="d3cfb-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="d3cfb-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="d3cfb-111">CN</span><span class="sxs-lookup"><span data-stu-id="d3cfb-111">CN</span></span>                | <span data-ttu-id="d3cfb-112">Logon-Count</span><span class="sxs-lookup"><span data-stu-id="d3cfb-112">Logon-Count</span></span>                          |
| <span data-ttu-id="d3cfb-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="d3cfb-113">Ldap-Display-Name</span></span> | <span data-ttu-id="d3cfb-114">logonCount</span><span class="sxs-lookup"><span data-stu-id="d3cfb-114">logonCount</span></span>                           |
| <span data-ttu-id="d3cfb-115">Taille</span><span class="sxs-lookup"><span data-stu-id="d3cfb-115">Size</span></span>              | <span data-ttu-id="d3cfb-116">4 octets</span><span class="sxs-lookup"><span data-stu-id="d3cfb-116">4 bytes</span></span>                              |
| <span data-ttu-id="d3cfb-117">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="d3cfb-117">Update Privilege</span></span>  | <span data-ttu-id="d3cfb-118">Administrateur de domaine</span><span class="sxs-lookup"><span data-stu-id="d3cfb-118">Domain administrator</span></span>                 |
| <span data-ttu-id="d3cfb-119">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="d3cfb-119">Update Frequency</span></span>  | <span data-ttu-id="d3cfb-120">Chaque fois que l’utilisateur ouvre une session.</span><span class="sxs-lookup"><span data-stu-id="d3cfb-120">Each time the user logs on.</span></span>          |
| <span data-ttu-id="d3cfb-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d3cfb-121">Attribute-Id</span></span>      | <span data-ttu-id="d3cfb-122">1.2.840.113556.1.4.169</span><span class="sxs-lookup"><span data-stu-id="d3cfb-122">1.2.840.113556.1.4.169</span></span>               |
| <span data-ttu-id="d3cfb-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="d3cfb-123">System-Id-Guid</span></span>    | <span data-ttu-id="d3cfb-124">bf9679aa-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="d3cfb-124">bf9679aa-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="d3cfb-125">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d3cfb-125">Syntax</span></span>            | [<span data-ttu-id="d3cfb-126">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="d3cfb-126">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="d3cfb-127">Implémentations</span><span class="sxs-lookup"><span data-stu-id="d3cfb-127">Implementations</span></span>

-   [<span data-ttu-id="d3cfb-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d3cfb-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d3cfb-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d3cfb-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d3cfb-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d3cfb-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d3cfb-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d3cfb-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d3cfb-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d3cfb-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d3cfb-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d3cfb-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d3cfb-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d3cfb-134">Windows 2000 Server</span></span>



| <span data-ttu-id="d3cfb-135">Entrée</span><span class="sxs-lookup"><span data-stu-id="d3cfb-135">Entry</span></span> | <span data-ttu-id="d3cfb-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="d3cfb-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="d3cfb-137">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d3cfb-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="d3cfb-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d3cfb-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="d3cfb-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="d3cfb-139">System-Only</span></span>            | <span data-ttu-id="d3cfb-140">Faux</span><span class="sxs-lookup"><span data-stu-id="d3cfb-140">False</span></span>                             |
| <span data-ttu-id="d3cfb-141">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d3cfb-141">Is-Single-Valued</span></span>       | <span data-ttu-id="d3cfb-142">Vrai</span><span class="sxs-lookup"><span data-stu-id="d3cfb-142">True</span></span>                              |
| <span data-ttu-id="d3cfb-143">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d3cfb-143">Is Indexed</span></span>             | <span data-ttu-id="d3cfb-144">Faux</span><span class="sxs-lookup"><span data-stu-id="d3cfb-144">False</span></span>                             |
| <span data-ttu-id="d3cfb-145">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d3cfb-145">In Global Catalog</span></span>      | <span data-ttu-id="d3cfb-146">Faux</span><span class="sxs-lookup"><span data-stu-id="d3cfb-146">False</span></span>                             |
| <span data-ttu-id="d3cfb-147">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d3cfb-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="d3cfb-148">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d3cfb-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="d3cfb-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d3cfb-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="d3cfb-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d3cfb-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="d3cfb-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d3cfb-151">Search-Flags</span></span>           | <span data-ttu-id="d3cfb-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d3cfb-152">0x00000000</span></span>                        |
| <span data-ttu-id="d3cfb-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d3cfb-153">System-Flags</span></span>           | <span data-ttu-id="d3cfb-154">0x00000011</span><span class="sxs-lookup"><span data-stu-id="d3cfb-154">0x00000011</span></span>                        |
| <span data-ttu-id="d3cfb-155">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d3cfb-155">Classes used in</span></span>        | [<span data-ttu-id="d3cfb-156">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="d3cfb-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d3cfb-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d3cfb-157">Windows Server 2003</span></span>



| <span data-ttu-id="d3cfb-158">Entrée</span><span class="sxs-lookup"><span data-stu-id="d3cfb-158">Entry</span></span> | <span data-ttu-id="d3cfb-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="d3cfb-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="d3cfb-160">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d3cfb-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="d3cfb-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d3cfb-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="d3cfb-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="d3cfb-162">System-Only</span></span>            | <span data-ttu-id="d3cfb-163">Faux</span><span class="sxs-lookup"><span data-stu-id="d3cfb-163">False</span></span>                             |
| <span data-ttu-id="d3cfb-164">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d3cfb-164">Is-Single-Valued</span></span>       | <span data-ttu-id="d3cfb-165">Vrai</span><span class="sxs-lookup"><span data-stu-id="d3cfb-165">True</span></span>                              |
| <span data-ttu-id="d3cfb-166">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d3cfb-166">Is Indexed</span></span>             | <span data-ttu-id="d3cfb-167">Faux</span><span class="sxs-lookup"><span data-stu-id="d3cfb-167">False</span></span>                             |
| <span data-ttu-id="d3cfb-168">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d3cfb-168">In Global Catalog</span></span>      | <span data-ttu-id="d3cfb-169">Faux</span><span class="sxs-lookup"><span data-stu-id="d3cfb-169">False</span></span>                             |
| <span data-ttu-id="d3cfb-170">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d3cfb-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="d3cfb-171">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d3cfb-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="d3cfb-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d3cfb-172">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="d3cfb-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d3cfb-173">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="d3cfb-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d3cfb-174">Search-Flags</span></span>           | <span data-ttu-id="d3cfb-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d3cfb-175">0x00000000</span></span>                        |
| <span data-ttu-id="d3cfb-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d3cfb-176">System-Flags</span></span>           | <span data-ttu-id="d3cfb-177">0x00000011</span><span class="sxs-lookup"><span data-stu-id="d3cfb-177">0x00000011</span></span>                        |
| <span data-ttu-id="d3cfb-178">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d3cfb-178">Classes used in</span></span>        | [<span data-ttu-id="d3cfb-179">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="d3cfb-179">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d3cfb-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d3cfb-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d3cfb-181">Entrée</span><span class="sxs-lookup"><span data-stu-id="d3cfb-181">Entry</span></span> | <span data-ttu-id="d3cfb-182">Valeur</span><span class="sxs-lookup"><span data-stu-id="d3cfb-182">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="d3cfb-183">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d3cfb-183">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="d3cfb-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d3cfb-184">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="d3cfb-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="d3cfb-185">System-Only</span></span>            | <span data-ttu-id="d3cfb-186">Faux</span><span class="sxs-lookup"><span data-stu-id="d3cfb-186">False</span></span>                             |
| <span data-ttu-id="d3cfb-187">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d3cfb-187">Is-Single-Valued</span></span>       | <span data-ttu-id="d3cfb-188">Vrai</span><span class="sxs-lookup"><span data-stu-id="d3cfb-188">True</span></span>                              |
| <span data-ttu-id="d3cfb-189">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d3cfb-189">Is Indexed</span></span>             | <span data-ttu-id="d3cfb-190">Faux</span><span class="sxs-lookup"><span data-stu-id="d3cfb-190">False</span></span>                             |
| <span data-ttu-id="d3cfb-191">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d3cfb-191">In Global Catalog</span></span>      | <span data-ttu-id="d3cfb-192">Faux</span><span class="sxs-lookup"><span data-stu-id="d3cfb-192">False</span></span>                             |
| <span data-ttu-id="d3cfb-193">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d3cfb-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="d3cfb-194">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d3cfb-194">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="d3cfb-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d3cfb-195">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="d3cfb-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d3cfb-196">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="d3cfb-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d3cfb-197">Search-Flags</span></span>           | <span data-ttu-id="d3cfb-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d3cfb-198">0x00000000</span></span>                        |
| <span data-ttu-id="d3cfb-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d3cfb-199">System-Flags</span></span>           | <span data-ttu-id="d3cfb-200">0x00000011</span><span class="sxs-lookup"><span data-stu-id="d3cfb-200">0x00000011</span></span>                        |
| <span data-ttu-id="d3cfb-201">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d3cfb-201">Classes used in</span></span>        | [<span data-ttu-id="d3cfb-202">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="d3cfb-202">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d3cfb-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d3cfb-203">Windows Server 2008</span></span>



| <span data-ttu-id="d3cfb-204">Entrée</span><span class="sxs-lookup"><span data-stu-id="d3cfb-204">Entry</span></span> | <span data-ttu-id="d3cfb-205">Valeur</span><span class="sxs-lookup"><span data-stu-id="d3cfb-205">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="d3cfb-206">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d3cfb-206">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="d3cfb-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d3cfb-207">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="d3cfb-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="d3cfb-208">System-Only</span></span>            | <span data-ttu-id="d3cfb-209">Faux</span><span class="sxs-lookup"><span data-stu-id="d3cfb-209">False</span></span>                             |
| <span data-ttu-id="d3cfb-210">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d3cfb-210">Is-Single-Valued</span></span>       | <span data-ttu-id="d3cfb-211">Vrai</span><span class="sxs-lookup"><span data-stu-id="d3cfb-211">True</span></span>                              |
| <span data-ttu-id="d3cfb-212">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d3cfb-212">Is Indexed</span></span>             | <span data-ttu-id="d3cfb-213">Faux</span><span class="sxs-lookup"><span data-stu-id="d3cfb-213">False</span></span>                             |
| <span data-ttu-id="d3cfb-214">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d3cfb-214">In Global Catalog</span></span>      | <span data-ttu-id="d3cfb-215">Faux</span><span class="sxs-lookup"><span data-stu-id="d3cfb-215">False</span></span>                             |
| <span data-ttu-id="d3cfb-216">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d3cfb-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="d3cfb-217">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d3cfb-217">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="d3cfb-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d3cfb-218">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="d3cfb-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d3cfb-219">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="d3cfb-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d3cfb-220">Search-Flags</span></span>           | <span data-ttu-id="d3cfb-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d3cfb-221">0x00000000</span></span>                        |
| <span data-ttu-id="d3cfb-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d3cfb-222">System-Flags</span></span>           | <span data-ttu-id="d3cfb-223">0x00000011</span><span class="sxs-lookup"><span data-stu-id="d3cfb-223">0x00000011</span></span>                        |
| <span data-ttu-id="d3cfb-224">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d3cfb-224">Classes used in</span></span>        | [<span data-ttu-id="d3cfb-225">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="d3cfb-225">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d3cfb-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d3cfb-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d3cfb-227">Entrée</span><span class="sxs-lookup"><span data-stu-id="d3cfb-227">Entry</span></span> | <span data-ttu-id="d3cfb-228">Valeur</span><span class="sxs-lookup"><span data-stu-id="d3cfb-228">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="d3cfb-229">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d3cfb-229">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="d3cfb-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d3cfb-230">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="d3cfb-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="d3cfb-231">System-Only</span></span>            | <span data-ttu-id="d3cfb-232">Faux</span><span class="sxs-lookup"><span data-stu-id="d3cfb-232">False</span></span>                             |
| <span data-ttu-id="d3cfb-233">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d3cfb-233">Is-Single-Valued</span></span>       | <span data-ttu-id="d3cfb-234">Vrai</span><span class="sxs-lookup"><span data-stu-id="d3cfb-234">True</span></span>                              |
| <span data-ttu-id="d3cfb-235">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d3cfb-235">Is Indexed</span></span>             | <span data-ttu-id="d3cfb-236">Faux</span><span class="sxs-lookup"><span data-stu-id="d3cfb-236">False</span></span>                             |
| <span data-ttu-id="d3cfb-237">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d3cfb-237">In Global Catalog</span></span>      | <span data-ttu-id="d3cfb-238">Faux</span><span class="sxs-lookup"><span data-stu-id="d3cfb-238">False</span></span>                             |
| <span data-ttu-id="d3cfb-239">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d3cfb-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="d3cfb-240">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d3cfb-240">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="d3cfb-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d3cfb-241">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="d3cfb-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d3cfb-242">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="d3cfb-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d3cfb-243">Search-Flags</span></span>           | <span data-ttu-id="d3cfb-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d3cfb-244">0x00000000</span></span>                        |
| <span data-ttu-id="d3cfb-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d3cfb-245">System-Flags</span></span>           | <span data-ttu-id="d3cfb-246">0x00000011</span><span class="sxs-lookup"><span data-stu-id="d3cfb-246">0x00000011</span></span>                        |
| <span data-ttu-id="d3cfb-247">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d3cfb-247">Classes used in</span></span>        | [<span data-ttu-id="d3cfb-248">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="d3cfb-248">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d3cfb-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d3cfb-249">Windows Server 2012</span></span>



| <span data-ttu-id="d3cfb-250">Entrée</span><span class="sxs-lookup"><span data-stu-id="d3cfb-250">Entry</span></span> | <span data-ttu-id="d3cfb-251">Valeur</span><span class="sxs-lookup"><span data-stu-id="d3cfb-251">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="d3cfb-252">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d3cfb-252">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="d3cfb-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d3cfb-253">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="d3cfb-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="d3cfb-254">System-Only</span></span>            | <span data-ttu-id="d3cfb-255">Faux</span><span class="sxs-lookup"><span data-stu-id="d3cfb-255">False</span></span>                             |
| <span data-ttu-id="d3cfb-256">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d3cfb-256">Is-Single-Valued</span></span>       | <span data-ttu-id="d3cfb-257">Vrai</span><span class="sxs-lookup"><span data-stu-id="d3cfb-257">True</span></span>                              |
| <span data-ttu-id="d3cfb-258">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d3cfb-258">Is Indexed</span></span>             | <span data-ttu-id="d3cfb-259">Faux</span><span class="sxs-lookup"><span data-stu-id="d3cfb-259">False</span></span>                             |
| <span data-ttu-id="d3cfb-260">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d3cfb-260">In Global Catalog</span></span>      | <span data-ttu-id="d3cfb-261">Faux</span><span class="sxs-lookup"><span data-stu-id="d3cfb-261">False</span></span>                             |
| <span data-ttu-id="d3cfb-262">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d3cfb-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="d3cfb-263">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d3cfb-263">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="d3cfb-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d3cfb-264">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="d3cfb-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d3cfb-265">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="d3cfb-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d3cfb-266">Search-Flags</span></span>           | <span data-ttu-id="d3cfb-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d3cfb-267">0x00000000</span></span>                        |
| <span data-ttu-id="d3cfb-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d3cfb-268">System-Flags</span></span>           | <span data-ttu-id="d3cfb-269">0x00000011</span><span class="sxs-lookup"><span data-stu-id="d3cfb-269">0x00000011</span></span>                        |
| <span data-ttu-id="d3cfb-270">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d3cfb-270">Classes used in</span></span>        | [<span data-ttu-id="d3cfb-271">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="d3cfb-271">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="d3cfb-272">Notes</span><span class="sxs-lookup"><span data-stu-id="d3cfb-272">Remarks</span></span>

<span data-ttu-id="d3cfb-273">Cet attribut n’est pas répliqué et est conservé sur chaque contrôleur de domaine du domaine.</span><span class="sxs-lookup"><span data-stu-id="d3cfb-273">This attribute is not replicated and is maintained on each domain controller in the domain.</span></span> <span data-ttu-id="d3cfb-274">Pour obtenir une valeur précise pour le nombre total de tentatives de connexion réussies de l’utilisateur dans le domaine, chaque contrôleur de domaine dans le domaine doit être interrogé et la somme des valeurs doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="d3cfb-274">To get an accurate value for the user's total number of successful logon attempts in the domain, each domain controller in the domain must be queried and the sum of the values should be used.</span></span> <span data-ttu-id="d3cfb-275">Gardez à l’esprit que l’attribut n’est pas répliqué. par conséquent, les contrôleurs de domaine qui sont retirés peuvent avoir compté des ouvertures de session pour l’utilisateur, et ils ne seront pas pris en compte dans le nombre.</span><span class="sxs-lookup"><span data-stu-id="d3cfb-275">Keep in mind that the attribute is not replicated, therefore domain controllers that are retired may have counted logons for the user as well, and these will be missing from the count.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d3cfb-276">En raison de la compatibilité avec les versions 16 bits de LAN Manager, l’attribut a une limite supérieure de 65535.</span><span class="sxs-lookup"><span data-stu-id="d3cfb-276">Due to compatibility with 16-bit versions of LAN Manager, the attribute has an upper limit of 65535.</span></span> <span data-ttu-id="d3cfb-277">Une fois cette limite atteinte, vous ne pouvez pas l’utiliser comme indicateur de l’activité de l’utilisateur sur ce contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="d3cfb-277">After this limit has been reached, you cannot use it as an indicator of user activity on this domain controller.</span></span>

 

 

 





