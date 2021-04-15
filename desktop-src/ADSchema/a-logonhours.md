---
title: Attribut Logon-Hours
description: Heures auxquelles l’utilisateur est autorisé à se connecter au domaine.
ms.assetid: b97cc8b0-7f26-45c1-b1c9-bae6467bdfb6
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Logon-Hours
- Schéma AD de l’attribut logonHours
topic_type:
- apiref
api_name:
- Logon-Hours
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f764192ac57efdb1f14d55f691183240f0eddfc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104479772"
---
# <a name="logon-hours-attribute"></a><span data-ttu-id="b325a-105">Attribut Logon-Hours</span><span class="sxs-lookup"><span data-stu-id="b325a-105">Logon-Hours attribute</span></span>

<span data-ttu-id="b325a-106">Heures auxquelles l’utilisateur est autorisé à se connecter au domaine.</span><span class="sxs-lookup"><span data-stu-id="b325a-106">The hours that the user is allowed to logon to the domain.</span></span>



| <span data-ttu-id="b325a-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="b325a-107">Entry</span></span> | <span data-ttu-id="b325a-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="b325a-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="b325a-109">CN</span><span class="sxs-lookup"><span data-stu-id="b325a-109">CN</span></span>                | <span data-ttu-id="b325a-110">Logon-Hours</span><span class="sxs-lookup"><span data-stu-id="b325a-110">Logon-Hours</span></span>                                           |
| <span data-ttu-id="b325a-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="b325a-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b325a-112">logonHours</span><span class="sxs-lookup"><span data-stu-id="b325a-112">logonHours</span></span>                                            |
| <span data-ttu-id="b325a-113">Taille</span><span class="sxs-lookup"><span data-stu-id="b325a-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="b325a-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="b325a-114">Update Privilege</span></span>  | <span data-ttu-id="b325a-115">Administrateur de domaine</span><span class="sxs-lookup"><span data-stu-id="b325a-115">Domain administrator</span></span>                                  |
| <span data-ttu-id="b325a-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="b325a-116">Update Frequency</span></span>  | <span data-ttu-id="b325a-117">Chaque fois que les heures d’ouverture de session du compte doivent être modifiées.</span><span class="sxs-lookup"><span data-stu-id="b325a-117">Whenever the account's logon hours needs to change.</span></span>   |
| <span data-ttu-id="b325a-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b325a-118">Attribute-Id</span></span>      | <span data-ttu-id="b325a-119">1.2.840.113556.1.4.64</span><span class="sxs-lookup"><span data-stu-id="b325a-119">1.2.840.113556.1.4.64</span></span>                                 |
| <span data-ttu-id="b325a-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b325a-120">System-Id-Guid</span></span>    | <span data-ttu-id="b325a-121">bf9679ab-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="b325a-121">bf9679ab-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="b325a-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b325a-122">Syntax</span></span>            | [<span data-ttu-id="b325a-123">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="b325a-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="b325a-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="b325a-124">Implementations</span></span>

-   [<span data-ttu-id="b325a-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b325a-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b325a-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b325a-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b325a-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b325a-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b325a-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b325a-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b325a-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b325a-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b325a-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b325a-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b325a-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b325a-131">Windows 2000 Server</span></span>



| <span data-ttu-id="b325a-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="b325a-132">Entry</span></span> | <span data-ttu-id="b325a-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="b325a-133">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="b325a-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b325a-134">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="b325a-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b325a-135">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="b325a-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="b325a-136">System-Only</span></span>            | <span data-ttu-id="b325a-137">Faux</span><span class="sxs-lookup"><span data-stu-id="b325a-137">False</span></span>                             |
| <span data-ttu-id="b325a-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b325a-138">Is-Single-Valued</span></span>       | <span data-ttu-id="b325a-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="b325a-139">True</span></span>                              |
| <span data-ttu-id="b325a-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b325a-140">Is Indexed</span></span>             | <span data-ttu-id="b325a-141">Faux</span><span class="sxs-lookup"><span data-stu-id="b325a-141">False</span></span>                             |
| <span data-ttu-id="b325a-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b325a-142">In Global Catalog</span></span>      | <span data-ttu-id="b325a-143">Faux</span><span class="sxs-lookup"><span data-stu-id="b325a-143">False</span></span>                             |
| <span data-ttu-id="b325a-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b325a-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="b325a-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b325a-145">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="b325a-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b325a-146">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="b325a-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b325a-147">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="b325a-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b325a-148">Search-Flags</span></span>           | <span data-ttu-id="b325a-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b325a-149">0x00000010</span></span>                        |
| <span data-ttu-id="b325a-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b325a-150">System-Flags</span></span>           | <span data-ttu-id="b325a-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b325a-151">0x00000010</span></span>                        |
| <span data-ttu-id="b325a-152">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b325a-152">Classes used in</span></span>        | [<span data-ttu-id="b325a-153">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="b325a-153">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b325a-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b325a-154">Windows Server 2003</span></span>



| <span data-ttu-id="b325a-155">Entrée</span><span class="sxs-lookup"><span data-stu-id="b325a-155">Entry</span></span> | <span data-ttu-id="b325a-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="b325a-156">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="b325a-157">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b325a-157">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="b325a-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b325a-158">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="b325a-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="b325a-159">System-Only</span></span>            | <span data-ttu-id="b325a-160">Faux</span><span class="sxs-lookup"><span data-stu-id="b325a-160">False</span></span>                             |
| <span data-ttu-id="b325a-161">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b325a-161">Is-Single-Valued</span></span>       | <span data-ttu-id="b325a-162">Vrai</span><span class="sxs-lookup"><span data-stu-id="b325a-162">True</span></span>                              |
| <span data-ttu-id="b325a-163">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b325a-163">Is Indexed</span></span>             | <span data-ttu-id="b325a-164">Faux</span><span class="sxs-lookup"><span data-stu-id="b325a-164">False</span></span>                             |
| <span data-ttu-id="b325a-165">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b325a-165">In Global Catalog</span></span>      | <span data-ttu-id="b325a-166">Faux</span><span class="sxs-lookup"><span data-stu-id="b325a-166">False</span></span>                             |
| <span data-ttu-id="b325a-167">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b325a-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="b325a-168">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b325a-168">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="b325a-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b325a-169">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="b325a-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b325a-170">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="b325a-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b325a-171">Search-Flags</span></span>           | <span data-ttu-id="b325a-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b325a-172">0x00000010</span></span>                        |
| <span data-ttu-id="b325a-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b325a-173">System-Flags</span></span>           | <span data-ttu-id="b325a-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b325a-174">0x00000010</span></span>                        |
| <span data-ttu-id="b325a-175">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b325a-175">Classes used in</span></span>        | [<span data-ttu-id="b325a-176">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="b325a-176">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b325a-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b325a-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b325a-178">Entrée</span><span class="sxs-lookup"><span data-stu-id="b325a-178">Entry</span></span> | <span data-ttu-id="b325a-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="b325a-179">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="b325a-180">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b325a-180">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="b325a-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b325a-181">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="b325a-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="b325a-182">System-Only</span></span>            | <span data-ttu-id="b325a-183">Faux</span><span class="sxs-lookup"><span data-stu-id="b325a-183">False</span></span>                             |
| <span data-ttu-id="b325a-184">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b325a-184">Is-Single-Valued</span></span>       | <span data-ttu-id="b325a-185">Vrai</span><span class="sxs-lookup"><span data-stu-id="b325a-185">True</span></span>                              |
| <span data-ttu-id="b325a-186">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b325a-186">Is Indexed</span></span>             | <span data-ttu-id="b325a-187">Faux</span><span class="sxs-lookup"><span data-stu-id="b325a-187">False</span></span>                             |
| <span data-ttu-id="b325a-188">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b325a-188">In Global Catalog</span></span>      | <span data-ttu-id="b325a-189">Faux</span><span class="sxs-lookup"><span data-stu-id="b325a-189">False</span></span>                             |
| <span data-ttu-id="b325a-190">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b325a-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="b325a-191">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b325a-191">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="b325a-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b325a-192">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="b325a-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b325a-193">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="b325a-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b325a-194">Search-Flags</span></span>           | <span data-ttu-id="b325a-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b325a-195">0x00000010</span></span>                        |
| <span data-ttu-id="b325a-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b325a-196">System-Flags</span></span>           | <span data-ttu-id="b325a-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b325a-197">0x00000010</span></span>                        |
| <span data-ttu-id="b325a-198">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b325a-198">Classes used in</span></span>        | [<span data-ttu-id="b325a-199">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="b325a-199">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b325a-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b325a-200">Windows Server 2008</span></span>



| <span data-ttu-id="b325a-201">Entrée</span><span class="sxs-lookup"><span data-stu-id="b325a-201">Entry</span></span> | <span data-ttu-id="b325a-202">Valeur</span><span class="sxs-lookup"><span data-stu-id="b325a-202">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="b325a-203">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b325a-203">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="b325a-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b325a-204">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="b325a-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="b325a-205">System-Only</span></span>            | <span data-ttu-id="b325a-206">Faux</span><span class="sxs-lookup"><span data-stu-id="b325a-206">False</span></span>                             |
| <span data-ttu-id="b325a-207">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b325a-207">Is-Single-Valued</span></span>       | <span data-ttu-id="b325a-208">Vrai</span><span class="sxs-lookup"><span data-stu-id="b325a-208">True</span></span>                              |
| <span data-ttu-id="b325a-209">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b325a-209">Is Indexed</span></span>             | <span data-ttu-id="b325a-210">Faux</span><span class="sxs-lookup"><span data-stu-id="b325a-210">False</span></span>                             |
| <span data-ttu-id="b325a-211">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b325a-211">In Global Catalog</span></span>      | <span data-ttu-id="b325a-212">Faux</span><span class="sxs-lookup"><span data-stu-id="b325a-212">False</span></span>                             |
| <span data-ttu-id="b325a-213">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b325a-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="b325a-214">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b325a-214">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="b325a-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b325a-215">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="b325a-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b325a-216">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="b325a-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b325a-217">Search-Flags</span></span>           | <span data-ttu-id="b325a-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b325a-218">0x00000010</span></span>                        |
| <span data-ttu-id="b325a-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b325a-219">System-Flags</span></span>           | <span data-ttu-id="b325a-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b325a-220">0x00000010</span></span>                        |
| <span data-ttu-id="b325a-221">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b325a-221">Classes used in</span></span>        | [<span data-ttu-id="b325a-222">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="b325a-222">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b325a-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b325a-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b325a-224">Entrée</span><span class="sxs-lookup"><span data-stu-id="b325a-224">Entry</span></span> | <span data-ttu-id="b325a-225">Valeur</span><span class="sxs-lookup"><span data-stu-id="b325a-225">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="b325a-226">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b325a-226">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="b325a-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b325a-227">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="b325a-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="b325a-228">System-Only</span></span>            | <span data-ttu-id="b325a-229">Faux</span><span class="sxs-lookup"><span data-stu-id="b325a-229">False</span></span>                             |
| <span data-ttu-id="b325a-230">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b325a-230">Is-Single-Valued</span></span>       | <span data-ttu-id="b325a-231">Vrai</span><span class="sxs-lookup"><span data-stu-id="b325a-231">True</span></span>                              |
| <span data-ttu-id="b325a-232">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b325a-232">Is Indexed</span></span>             | <span data-ttu-id="b325a-233">Faux</span><span class="sxs-lookup"><span data-stu-id="b325a-233">False</span></span>                             |
| <span data-ttu-id="b325a-234">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b325a-234">In Global Catalog</span></span>      | <span data-ttu-id="b325a-235">Faux</span><span class="sxs-lookup"><span data-stu-id="b325a-235">False</span></span>                             |
| <span data-ttu-id="b325a-236">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b325a-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="b325a-237">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b325a-237">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="b325a-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b325a-238">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="b325a-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b325a-239">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="b325a-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b325a-240">Search-Flags</span></span>           | <span data-ttu-id="b325a-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b325a-241">0x00000010</span></span>                        |
| <span data-ttu-id="b325a-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b325a-242">System-Flags</span></span>           | <span data-ttu-id="b325a-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b325a-243">0x00000010</span></span>                        |
| <span data-ttu-id="b325a-244">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b325a-244">Classes used in</span></span>        | [<span data-ttu-id="b325a-245">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="b325a-245">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b325a-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b325a-246">Windows Server 2012</span></span>



| <span data-ttu-id="b325a-247">Entrée</span><span class="sxs-lookup"><span data-stu-id="b325a-247">Entry</span></span> | <span data-ttu-id="b325a-248">Valeur</span><span class="sxs-lookup"><span data-stu-id="b325a-248">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="b325a-249">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b325a-249">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="b325a-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b325a-250">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="b325a-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="b325a-251">System-Only</span></span>            | <span data-ttu-id="b325a-252">Faux</span><span class="sxs-lookup"><span data-stu-id="b325a-252">False</span></span>                             |
| <span data-ttu-id="b325a-253">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b325a-253">Is-Single-Valued</span></span>       | <span data-ttu-id="b325a-254">Vrai</span><span class="sxs-lookup"><span data-stu-id="b325a-254">True</span></span>                              |
| <span data-ttu-id="b325a-255">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b325a-255">Is Indexed</span></span>             | <span data-ttu-id="b325a-256">Faux</span><span class="sxs-lookup"><span data-stu-id="b325a-256">False</span></span>                             |
| <span data-ttu-id="b325a-257">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b325a-257">In Global Catalog</span></span>      | <span data-ttu-id="b325a-258">Faux</span><span class="sxs-lookup"><span data-stu-id="b325a-258">False</span></span>                             |
| <span data-ttu-id="b325a-259">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b325a-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="b325a-260">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b325a-260">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="b325a-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b325a-261">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="b325a-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b325a-262">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="b325a-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b325a-263">Search-Flags</span></span>           | <span data-ttu-id="b325a-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b325a-264">0x00000010</span></span>                        |
| <span data-ttu-id="b325a-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b325a-265">System-Flags</span></span>           | <span data-ttu-id="b325a-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b325a-266">0x00000010</span></span>                        |
| <span data-ttu-id="b325a-267">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b325a-267">Classes used in</span></span>        | [<span data-ttu-id="b325a-268">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="b325a-268">**User**</span></span>](c-user.md)<br/> |



 

 





