---
title: Attribut User-Account-Control
description: Indicateurs qui contrôlent le comportement du compte d’utilisateur.
ms.assetid: fc81a16a-f537-44cc-957c-5d7ca66b9755
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut de contrôle de compte d’utilisateur
- Schéma AD d’attribut userAccountControl
topic_type:
- apiref
api_name:
- User-Account-Control
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f60297d22aad76b229c691a667ac22a87271402c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107923"
---
# <a name="user-account-control-attribute"></a><span data-ttu-id="46356-105">Attribut User-Account-Control</span><span class="sxs-lookup"><span data-stu-id="46356-105">User-Account-Control attribute</span></span>

<span data-ttu-id="46356-106">Indicateurs qui contrôlent le comportement du compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="46356-106">Flags that control the behavior of the user account.</span></span>



| <span data-ttu-id="46356-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="46356-107">Entry</span></span> | <span data-ttu-id="46356-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="46356-108">Value</span></span> |
|-------------------|---------------------------------------|
| <span data-ttu-id="46356-109">CN</span><span class="sxs-lookup"><span data-stu-id="46356-109">CN</span></span>                | <span data-ttu-id="46356-110">Contrôle de compte d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="46356-110">User-Account-Control</span></span>                  |
| <span data-ttu-id="46356-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="46356-111">Ldap-Display-Name</span></span> | <span data-ttu-id="46356-112">userAccountControl</span><span class="sxs-lookup"><span data-stu-id="46356-112">userAccountControl</span></span>                    |
| <span data-ttu-id="46356-113">Taille</span><span class="sxs-lookup"><span data-stu-id="46356-113">Size</span></span>              | <span data-ttu-id="46356-114">4 octets.</span><span class="sxs-lookup"><span data-stu-id="46356-114">4 bytes.</span></span>                              |
| <span data-ttu-id="46356-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="46356-115">Update Privilege</span></span>  | <span data-ttu-id="46356-116">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="46356-116">This value is set by the system.</span></span>      |
| <span data-ttu-id="46356-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="46356-117">Update Frequency</span></span>  | <span data-ttu-id="46356-118">Chaque fois que la stratégie de compte change.</span><span class="sxs-lookup"><span data-stu-id="46356-118">Each time the account policy changes.</span></span> |
| <span data-ttu-id="46356-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="46356-119">Attribute-Id</span></span>      | <span data-ttu-id="46356-120">1.2.840.113556.1.4.8</span><span class="sxs-lookup"><span data-stu-id="46356-120">1.2.840.113556.1.4.8</span></span>                  |
| <span data-ttu-id="46356-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="46356-121">System-Id-Guid</span></span>    | <span data-ttu-id="46356-122">bf967a68-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="46356-122">bf967a68-0de6-11d0-a285-00aa003049e2</span></span>  |
| <span data-ttu-id="46356-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="46356-123">Syntax</span></span>            | [<span data-ttu-id="46356-124">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="46356-124">**Enumeration**</span></span>](s-enumeration.md)  |



## <a name="implementations"></a><span data-ttu-id="46356-125">Implémentations</span><span class="sxs-lookup"><span data-stu-id="46356-125">Implementations</span></span>

-   [<span data-ttu-id="46356-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="46356-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="46356-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="46356-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="46356-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="46356-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="46356-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="46356-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="46356-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="46356-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="46356-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="46356-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="46356-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="46356-132">Windows 2000 Server</span></span>



| <span data-ttu-id="46356-133">Entrée</span><span class="sxs-lookup"><span data-stu-id="46356-133">Entry</span></span> | <span data-ttu-id="46356-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="46356-134">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="46356-135">ID de lien</span><span class="sxs-lookup"><span data-stu-id="46356-135">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="46356-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="46356-136">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="46356-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="46356-137">System-Only</span></span>            | <span data-ttu-id="46356-138">Faux</span><span class="sxs-lookup"><span data-stu-id="46356-138">False</span></span>                             |
| <span data-ttu-id="46356-139">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="46356-139">Is-Single-Valued</span></span>       | <span data-ttu-id="46356-140">Vrai</span><span class="sxs-lookup"><span data-stu-id="46356-140">True</span></span>                              |
| <span data-ttu-id="46356-141">Est indexé</span><span class="sxs-lookup"><span data-stu-id="46356-141">Is Indexed</span></span>             | <span data-ttu-id="46356-142">Vrai</span><span class="sxs-lookup"><span data-stu-id="46356-142">True</span></span>                              |
| <span data-ttu-id="46356-143">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="46356-143">In Global Catalog</span></span>      | <span data-ttu-id="46356-144">Vrai</span><span class="sxs-lookup"><span data-stu-id="46356-144">True</span></span>                              |
| <span data-ttu-id="46356-145">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="46356-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="46356-146">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="46356-146">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="46356-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="46356-147">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="46356-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="46356-148">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="46356-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="46356-149">Search-Flags</span></span>           | <span data-ttu-id="46356-150">0x00000019</span><span class="sxs-lookup"><span data-stu-id="46356-150">0x00000019</span></span>                        |
| <span data-ttu-id="46356-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="46356-151">System-Flags</span></span>           | <span data-ttu-id="46356-152">0x00000012</span><span class="sxs-lookup"><span data-stu-id="46356-152">0x00000012</span></span>                        |
| <span data-ttu-id="46356-153">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="46356-153">Classes used in</span></span>        | [<span data-ttu-id="46356-154">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="46356-154">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="46356-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="46356-155">Windows Server 2003</span></span>



| <span data-ttu-id="46356-156">Entrée</span><span class="sxs-lookup"><span data-stu-id="46356-156">Entry</span></span> | <span data-ttu-id="46356-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="46356-157">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="46356-158">ID de lien</span><span class="sxs-lookup"><span data-stu-id="46356-158">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="46356-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="46356-159">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="46356-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="46356-160">System-Only</span></span>            | <span data-ttu-id="46356-161">Faux</span><span class="sxs-lookup"><span data-stu-id="46356-161">False</span></span>                             |
| <span data-ttu-id="46356-162">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="46356-162">Is-Single-Valued</span></span>       | <span data-ttu-id="46356-163">Vrai</span><span class="sxs-lookup"><span data-stu-id="46356-163">True</span></span>                              |
| <span data-ttu-id="46356-164">Est indexé</span><span class="sxs-lookup"><span data-stu-id="46356-164">Is Indexed</span></span>             | <span data-ttu-id="46356-165">Vrai</span><span class="sxs-lookup"><span data-stu-id="46356-165">True</span></span>                              |
| <span data-ttu-id="46356-166">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="46356-166">In Global Catalog</span></span>      | <span data-ttu-id="46356-167">Vrai</span><span class="sxs-lookup"><span data-stu-id="46356-167">True</span></span>                              |
| <span data-ttu-id="46356-168">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="46356-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="46356-169">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="46356-169">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="46356-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="46356-170">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="46356-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="46356-171">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="46356-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="46356-172">Search-Flags</span></span>           | <span data-ttu-id="46356-173">0x00000019</span><span class="sxs-lookup"><span data-stu-id="46356-173">0x00000019</span></span>                        |
| <span data-ttu-id="46356-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="46356-174">System-Flags</span></span>           | <span data-ttu-id="46356-175">0x00000012</span><span class="sxs-lookup"><span data-stu-id="46356-175">0x00000012</span></span>                        |
| <span data-ttu-id="46356-176">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="46356-176">Classes used in</span></span>        | [<span data-ttu-id="46356-177">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="46356-177">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="46356-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="46356-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="46356-179">Entrée</span><span class="sxs-lookup"><span data-stu-id="46356-179">Entry</span></span> | <span data-ttu-id="46356-180">Valeur</span><span class="sxs-lookup"><span data-stu-id="46356-180">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="46356-181">ID de lien</span><span class="sxs-lookup"><span data-stu-id="46356-181">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="46356-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="46356-182">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="46356-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="46356-183">System-Only</span></span>            | <span data-ttu-id="46356-184">Faux</span><span class="sxs-lookup"><span data-stu-id="46356-184">False</span></span>                             |
| <span data-ttu-id="46356-185">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="46356-185">Is-Single-Valued</span></span>       | <span data-ttu-id="46356-186">Vrai</span><span class="sxs-lookup"><span data-stu-id="46356-186">True</span></span>                              |
| <span data-ttu-id="46356-187">Est indexé</span><span class="sxs-lookup"><span data-stu-id="46356-187">Is Indexed</span></span>             | <span data-ttu-id="46356-188">Vrai</span><span class="sxs-lookup"><span data-stu-id="46356-188">True</span></span>                              |
| <span data-ttu-id="46356-189">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="46356-189">In Global Catalog</span></span>      | <span data-ttu-id="46356-190">Vrai</span><span class="sxs-lookup"><span data-stu-id="46356-190">True</span></span>                              |
| <span data-ttu-id="46356-191">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="46356-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="46356-192">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="46356-192">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="46356-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="46356-193">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="46356-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="46356-194">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="46356-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="46356-195">Search-Flags</span></span>           | <span data-ttu-id="46356-196">0x00000019</span><span class="sxs-lookup"><span data-stu-id="46356-196">0x00000019</span></span>                        |
| <span data-ttu-id="46356-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="46356-197">System-Flags</span></span>           | <span data-ttu-id="46356-198">0x00000012</span><span class="sxs-lookup"><span data-stu-id="46356-198">0x00000012</span></span>                        |
| <span data-ttu-id="46356-199">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="46356-199">Classes used in</span></span>        | [<span data-ttu-id="46356-200">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="46356-200">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="46356-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="46356-201">Windows Server 2008</span></span>



| <span data-ttu-id="46356-202">Entrée</span><span class="sxs-lookup"><span data-stu-id="46356-202">Entry</span></span> | <span data-ttu-id="46356-203">Valeur</span><span class="sxs-lookup"><span data-stu-id="46356-203">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="46356-204">ID de lien</span><span class="sxs-lookup"><span data-stu-id="46356-204">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="46356-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="46356-205">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="46356-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="46356-206">System-Only</span></span>            | <span data-ttu-id="46356-207">Faux</span><span class="sxs-lookup"><span data-stu-id="46356-207">False</span></span>                             |
| <span data-ttu-id="46356-208">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="46356-208">Is-Single-Valued</span></span>       | <span data-ttu-id="46356-209">Vrai</span><span class="sxs-lookup"><span data-stu-id="46356-209">True</span></span>                              |
| <span data-ttu-id="46356-210">Est indexé</span><span class="sxs-lookup"><span data-stu-id="46356-210">Is Indexed</span></span>             | <span data-ttu-id="46356-211">Vrai</span><span class="sxs-lookup"><span data-stu-id="46356-211">True</span></span>                              |
| <span data-ttu-id="46356-212">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="46356-212">In Global Catalog</span></span>      | <span data-ttu-id="46356-213">Vrai</span><span class="sxs-lookup"><span data-stu-id="46356-213">True</span></span>                              |
| <span data-ttu-id="46356-214">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="46356-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="46356-215">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="46356-215">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="46356-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="46356-216">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="46356-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="46356-217">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="46356-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="46356-218">Search-Flags</span></span>           | <span data-ttu-id="46356-219">0x00000019</span><span class="sxs-lookup"><span data-stu-id="46356-219">0x00000019</span></span>                        |
| <span data-ttu-id="46356-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="46356-220">System-Flags</span></span>           | <span data-ttu-id="46356-221">0x00000012</span><span class="sxs-lookup"><span data-stu-id="46356-221">0x00000012</span></span>                        |
| <span data-ttu-id="46356-222">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="46356-222">Classes used in</span></span>        | [<span data-ttu-id="46356-223">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="46356-223">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="46356-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="46356-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="46356-225">Entrée</span><span class="sxs-lookup"><span data-stu-id="46356-225">Entry</span></span> | <span data-ttu-id="46356-226">Valeur</span><span class="sxs-lookup"><span data-stu-id="46356-226">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="46356-227">ID de lien</span><span class="sxs-lookup"><span data-stu-id="46356-227">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="46356-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="46356-228">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="46356-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="46356-229">System-Only</span></span>            | <span data-ttu-id="46356-230">Faux</span><span class="sxs-lookup"><span data-stu-id="46356-230">False</span></span>                             |
| <span data-ttu-id="46356-231">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="46356-231">Is-Single-Valued</span></span>       | <span data-ttu-id="46356-232">Vrai</span><span class="sxs-lookup"><span data-stu-id="46356-232">True</span></span>                              |
| <span data-ttu-id="46356-233">Est indexé</span><span class="sxs-lookup"><span data-stu-id="46356-233">Is Indexed</span></span>             | <span data-ttu-id="46356-234">Vrai</span><span class="sxs-lookup"><span data-stu-id="46356-234">True</span></span>                              |
| <span data-ttu-id="46356-235">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="46356-235">In Global Catalog</span></span>      | <span data-ttu-id="46356-236">Vrai</span><span class="sxs-lookup"><span data-stu-id="46356-236">True</span></span>                              |
| <span data-ttu-id="46356-237">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="46356-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="46356-238">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="46356-238">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="46356-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="46356-239">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="46356-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="46356-240">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="46356-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="46356-241">Search-Flags</span></span>           | <span data-ttu-id="46356-242">0x00000019</span><span class="sxs-lookup"><span data-stu-id="46356-242">0x00000019</span></span>                        |
| <span data-ttu-id="46356-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="46356-243">System-Flags</span></span>           | <span data-ttu-id="46356-244">0x00000012</span><span class="sxs-lookup"><span data-stu-id="46356-244">0x00000012</span></span>                        |
| <span data-ttu-id="46356-245">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="46356-245">Classes used in</span></span>        | [<span data-ttu-id="46356-246">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="46356-246">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="46356-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="46356-247">Windows Server 2012</span></span>



| <span data-ttu-id="46356-248">Entrée</span><span class="sxs-lookup"><span data-stu-id="46356-248">Entry</span></span> | <span data-ttu-id="46356-249">Valeur</span><span class="sxs-lookup"><span data-stu-id="46356-249">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="46356-250">ID de lien</span><span class="sxs-lookup"><span data-stu-id="46356-250">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="46356-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="46356-251">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="46356-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="46356-252">System-Only</span></span>            | <span data-ttu-id="46356-253">Faux</span><span class="sxs-lookup"><span data-stu-id="46356-253">False</span></span>                             |
| <span data-ttu-id="46356-254">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="46356-254">Is-Single-Valued</span></span>       | <span data-ttu-id="46356-255">Vrai</span><span class="sxs-lookup"><span data-stu-id="46356-255">True</span></span>                              |
| <span data-ttu-id="46356-256">Est indexé</span><span class="sxs-lookup"><span data-stu-id="46356-256">Is Indexed</span></span>             | <span data-ttu-id="46356-257">Vrai</span><span class="sxs-lookup"><span data-stu-id="46356-257">True</span></span>                              |
| <span data-ttu-id="46356-258">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="46356-258">In Global Catalog</span></span>      | <span data-ttu-id="46356-259">Vrai</span><span class="sxs-lookup"><span data-stu-id="46356-259">True</span></span>                              |
| <span data-ttu-id="46356-260">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="46356-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="46356-261">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="46356-261">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="46356-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="46356-262">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="46356-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="46356-263">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="46356-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="46356-264">Search-Flags</span></span>           | <span data-ttu-id="46356-265">0x00000019</span><span class="sxs-lookup"><span data-stu-id="46356-265">0x00000019</span></span>                        |
| <span data-ttu-id="46356-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="46356-266">System-Flags</span></span>           | <span data-ttu-id="46356-267">0x00000012</span><span class="sxs-lookup"><span data-stu-id="46356-267">0x00000012</span></span>                        |
| <span data-ttu-id="46356-268">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="46356-268">Classes used in</span></span>        | [<span data-ttu-id="46356-269">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="46356-269">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="46356-270">Notes</span><span class="sxs-lookup"><span data-stu-id="46356-270">Remarks</span></span>

<span data-ttu-id="46356-271">Cette valeur d’attribut peut être zéro ou une combinaison d’une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="46356-271">This attribute value can be zero or a combination of one or more of the following values.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="46356-272">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="46356-272">Hexadecimal value</span></span></th>
<th><span data-ttu-id="46356-273">Identificateur (défini dans IADs. h)</span><span class="sxs-lookup"><span data-stu-id="46356-273">Identifier (defined in iads.h)</span></span></th>
<th><span data-ttu-id="46356-274">Description</span><span class="sxs-lookup"><span data-stu-id="46356-274">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="46356-275">0x00000001</span><span class="sxs-lookup"><span data-stu-id="46356-275">0x00000001</span></span></td>
<td><span data-ttu-id="46356-276"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_SCRIPT</strong></a></span><span class="sxs-lookup"><span data-stu-id="46356-276"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_SCRIPT</strong></a></span></span></td>
<td><span data-ttu-id="46356-277">Le script d’ouverture de session est exécuté.</span><span class="sxs-lookup"><span data-stu-id="46356-277">The logon script is executed.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="46356-278">0x00000002</span><span class="sxs-lookup"><span data-stu-id="46356-278">0x00000002</span></span></td>
<td><span data-ttu-id="46356-279"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_ACCOUNTDISABLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="46356-279"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_ACCOUNTDISABLE</strong></a></span></span></td>
<td><span data-ttu-id="46356-280">Le compte d’utilisateur est désactivé.</span><span class="sxs-lookup"><span data-stu-id="46356-280">The user account is disabled.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="46356-281">0x00000008</span><span class="sxs-lookup"><span data-stu-id="46356-281">0x00000008</span></span></td>
<td><span data-ttu-id="46356-282"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_HOMEDIR_REQUIRED</strong></a></span><span class="sxs-lookup"><span data-stu-id="46356-282"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_HOMEDIR_REQUIRED</strong></a></span></span></td>
<td><span data-ttu-id="46356-283">Le répertoire de départ est requis.</span><span class="sxs-lookup"><span data-stu-id="46356-283">The home directory is required.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="46356-284">0x00000010</span><span class="sxs-lookup"><span data-stu-id="46356-284">0x00000010</span></span></td>
<td><span data-ttu-id="46356-285"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_LOCKOUT</strong></a></span><span class="sxs-lookup"><span data-stu-id="46356-285"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_LOCKOUT</strong></a></span></span></td>
<td><span data-ttu-id="46356-286">Le compte est actuellement verrouillé.</span><span class="sxs-lookup"><span data-stu-id="46356-286">The account is currently locked out.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="46356-287">0x00000020</span><span class="sxs-lookup"><span data-stu-id="46356-287">0x00000020</span></span></td>
<td><span data-ttu-id="46356-288"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_PASSWD_NOTREQD</strong></a></span><span class="sxs-lookup"><span data-stu-id="46356-288"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_PASSWD_NOTREQD</strong></a></span></span></td>
<td><span data-ttu-id="46356-289">Aucun mot de passe n'est requis.</span><span class="sxs-lookup"><span data-stu-id="46356-289">No password is required.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="46356-290">0x00000040</span><span class="sxs-lookup"><span data-stu-id="46356-290">0x00000040</span></span></td>
<td><span data-ttu-id="46356-291"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_PASSWD_CANT_CHANGE</strong></a></span><span class="sxs-lookup"><span data-stu-id="46356-291"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_PASSWD_CANT_CHANGE</strong></a></span></span></td>
<td><span data-ttu-id="46356-292">L’utilisateur ne peut pas modifier le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="46356-292">The user cannot change the password.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="46356-293">Vous ne pouvez pas assigner les paramètres d’autorisation de PASSWD_CANT_CHANGE en modifiant directement l’attribut UserAccountControl.</span><span class="sxs-lookup"><span data-stu-id="46356-293">You cannot assign the permission settings of PASSWD_CANT_CHANGE by directly modifying the UserAccountControl attribute.</span></span> <span data-ttu-id="46356-294">Pour plus d’informations et pour obtenir un exemple de code qui montre comment empêcher un utilisateur de modifier le mot de passe, consultez l' <a href="/windows/desktop/ADSI/user-cannot-change-password">utilisateur ne peut pas changer de mot de passe</a>.</span><span class="sxs-lookup"><span data-stu-id="46356-294">For more information and a code example that shows how to prevent a user from changing the password, see <a href="/windows/desktop/ADSI/user-cannot-change-password">User Cannot Change Password</a>.</span></span>
</blockquote>
<br/> <span data-ttu-id="46356-295">:</span><span class="sxs-lookup"><span data-stu-id="46356-295">:</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="46356-296">0x00000080</span><span class="sxs-lookup"><span data-stu-id="46356-296">0x00000080</span></span></td>
<td><span data-ttu-id="46356-297"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_ENCRYPTED_TEXT_PASSWORD_ALLOWED</strong></a></span><span class="sxs-lookup"><span data-stu-id="46356-297"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_ENCRYPTED_TEXT_PASSWORD_ALLOWED</strong></a></span></span></td>
<td><span data-ttu-id="46356-298">L’utilisateur peut envoyer un mot de passe chiffré.</span><span class="sxs-lookup"><span data-stu-id="46356-298">The user can send an encrypted password.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="46356-299">0x00000100</span><span class="sxs-lookup"><span data-stu-id="46356-299">0x00000100</span></span></td>
<td><span data-ttu-id="46356-300"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_TEMP_DUPLICATE_ACCOUNT</strong></a></span><span class="sxs-lookup"><span data-stu-id="46356-300"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_TEMP_DUPLICATE_ACCOUNT</strong></a></span></span></td>
<td><span data-ttu-id="46356-301">Il s’agit d’un compte pour les utilisateurs dont le compte principal se trouve dans un autre domaine.</span><span class="sxs-lookup"><span data-stu-id="46356-301">This is an account for users whose primary account is in another domain.</span></span> <span data-ttu-id="46356-302">Ce compte fournit l’accès utilisateur à ce domaine, mais pas à un domaine qui approuve ce domaine.</span><span class="sxs-lookup"><span data-stu-id="46356-302">This account provides user access to this domain, but not to any domain that trusts this domain.</span></span> <span data-ttu-id="46356-303">Également connu sous le nom de compte d’utilisateur local.</span><span class="sxs-lookup"><span data-stu-id="46356-303">Also known as a local user account.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="46356-304">0x00000200</span><span class="sxs-lookup"><span data-stu-id="46356-304">0x00000200</span></span></td>
<td><span data-ttu-id="46356-305"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_NORMAL_ACCOUNT</strong></a></span><span class="sxs-lookup"><span data-stu-id="46356-305"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_NORMAL_ACCOUNT</strong></a></span></span></td>
<td><span data-ttu-id="46356-306">Il s’agit d’un type de compte par défaut qui représente un utilisateur standard.</span><span class="sxs-lookup"><span data-stu-id="46356-306">This is a default account type that represents a typical user.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="46356-307">0x00000800</span><span class="sxs-lookup"><span data-stu-id="46356-307">0x00000800</span></span></td>
<td><span data-ttu-id="46356-308"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_INTERDOMAIN_TRUST_ACCOUNT</strong></a></span><span class="sxs-lookup"><span data-stu-id="46356-308"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_INTERDOMAIN_TRUST_ACCOUNT</strong></a></span></span></td>
<td><span data-ttu-id="46356-309">Il s’agit d’un permis de faire confiance à un compte de domaine système qui approuve d’autres domaines.</span><span class="sxs-lookup"><span data-stu-id="46356-309">This is a permit to trust account for a system domain that trusts other domains.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="46356-310">0x00001000</span><span class="sxs-lookup"><span data-stu-id="46356-310">0x00001000</span></span></td>
<td><span data-ttu-id="46356-311"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_WORKSTATION_TRUST_ACCOUNT</strong></a></span><span class="sxs-lookup"><span data-stu-id="46356-311"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_WORKSTATION_TRUST_ACCOUNT</strong></a></span></span></td>
<td><span data-ttu-id="46356-312">Il s’agit d’un compte d’ordinateur pour un ordinateur qui est membre de ce domaine.</span><span class="sxs-lookup"><span data-stu-id="46356-312">This is a computer account for a computer that is a member of this domain.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="46356-313">0x00002000</span><span class="sxs-lookup"><span data-stu-id="46356-313">0x00002000</span></span></td>
<td><span data-ttu-id="46356-314"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_SERVER_TRUST_ACCOUNT</strong></a></span><span class="sxs-lookup"><span data-stu-id="46356-314"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_SERVER_TRUST_ACCOUNT</strong></a></span></span></td>
<td><span data-ttu-id="46356-315">Il s’agit d’un compte d’ordinateur pour un contrôleur de domaine de sauvegarde du système qui est membre de ce domaine.</span><span class="sxs-lookup"><span data-stu-id="46356-315">This is a computer account for a system backup domain controller that is a member of this domain.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="46356-316">0x00004000</span><span class="sxs-lookup"><span data-stu-id="46356-316">0x00004000</span></span></td>
<td><span data-ttu-id="46356-317">N/A</span><span class="sxs-lookup"><span data-stu-id="46356-317">N/A</span></span></td>
<td><span data-ttu-id="46356-318">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="46356-318">Not used.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="46356-319">0x00008000</span><span class="sxs-lookup"><span data-stu-id="46356-319">0x00008000</span></span></td>
<td><span data-ttu-id="46356-320">N/A</span><span class="sxs-lookup"><span data-stu-id="46356-320">N/A</span></span></td>
<td><span data-ttu-id="46356-321">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="46356-321">Not used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="46356-322">0x00010000</span><span class="sxs-lookup"><span data-stu-id="46356-322">0x00010000</span></span></td>
<td><span data-ttu-id="46356-323"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_DONT_EXPIRE_PASSWD</strong></a></span><span class="sxs-lookup"><span data-stu-id="46356-323"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_DONT_EXPIRE_PASSWD</strong></a></span></span></td>
<td><span data-ttu-id="46356-324">Le mot de passe de ce compte n’expire jamais.</span><span class="sxs-lookup"><span data-stu-id="46356-324">The password for this account will never expire.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="46356-325">0x00020000</span><span class="sxs-lookup"><span data-stu-id="46356-325">0x00020000</span></span></td>
<td><span data-ttu-id="46356-326"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_MNS_LOGON_ACCOUNT</strong></a></span><span class="sxs-lookup"><span data-stu-id="46356-326"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_MNS_LOGON_ACCOUNT</strong></a></span></span></td>
<td><span data-ttu-id="46356-327">Il s’agit d’un compte MNS Logon.</span><span class="sxs-lookup"><span data-stu-id="46356-327">This is an MNS logon account.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="46356-328">0x00040000</span><span class="sxs-lookup"><span data-stu-id="46356-328">0x00040000</span></span></td>
<td><span data-ttu-id="46356-329"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_SMARTCARD_REQUIRED</strong></a></span><span class="sxs-lookup"><span data-stu-id="46356-329"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_SMARTCARD_REQUIRED</strong></a></span></span></td>
<td><span data-ttu-id="46356-330">L’utilisateur doit se connecter à l’aide d’une carte à puce.</span><span class="sxs-lookup"><span data-stu-id="46356-330">The user must log on using a smart card.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="46356-331">0x00080000</span><span class="sxs-lookup"><span data-stu-id="46356-331">0x00080000</span></span></td>
<td><span data-ttu-id="46356-332"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_TRUSTED_FOR_DELEGATION</strong></a></span><span class="sxs-lookup"><span data-stu-id="46356-332"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_TRUSTED_FOR_DELEGATION</strong></a></span></span></td>
<td><span data-ttu-id="46356-333">Le compte de service (compte d’utilisateur ou d’ordinateur), sous lequel un service s’exécute, est approuvé pour la délégation Kerberos.</span><span class="sxs-lookup"><span data-stu-id="46356-333">The service account (user or computer account), under which a service runs, is trusted for Kerberos delegation.</span></span> <span data-ttu-id="46356-334">N’importe quel service peut emprunter l’identité d’un client qui demande le service.</span><span class="sxs-lookup"><span data-stu-id="46356-334">Any such service can impersonate a client requesting the service.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="46356-335">0x00100000</span><span class="sxs-lookup"><span data-stu-id="46356-335">0x00100000</span></span></td>
<td><span data-ttu-id="46356-336"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_NOT_DELEGATED</strong></a></span><span class="sxs-lookup"><span data-stu-id="46356-336"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_NOT_DELEGATED</strong></a></span></span></td>
<td><span data-ttu-id="46356-337">Le contexte de sécurité de l’utilisateur ne sera pas délégué à un service même si le compte de service est défini comme approuvé pour la délégation Kerberos.</span><span class="sxs-lookup"><span data-stu-id="46356-337">The security context of the user will not be delegated to a service even if the service account is set as trusted for Kerberos delegation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="46356-338">0x00200000</span><span class="sxs-lookup"><span data-stu-id="46356-338">0x00200000</span></span></td>
<td><span data-ttu-id="46356-339"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_USE_DES_KEY_ONLY</strong></a></span><span class="sxs-lookup"><span data-stu-id="46356-339"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_USE_DES_KEY_ONLY</strong></a></span></span></td>
<td><span data-ttu-id="46356-340">Limitez ce principal pour qu’il utilise uniquement des types de chiffrement DES (Data Encryption Standard) pour les clés.</span><span class="sxs-lookup"><span data-stu-id="46356-340">Restrict this principal to use only Data Encryption Standard (DES) encryption types for keys.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="46356-341">0x00400000</span><span class="sxs-lookup"><span data-stu-id="46356-341">0x00400000</span></span></td>
<td><span data-ttu-id="46356-342"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_DONT_REQUIRE_PREAUTH</strong></a></span><span class="sxs-lookup"><span data-stu-id="46356-342"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_DONT_REQUIRE_PREAUTH</strong></a></span></span></td>
<td><span data-ttu-id="46356-343">Ce compte ne nécessite pas l’authentification préalable Kerberos pour l’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="46356-343">This account does not require Kerberos pre-authentication for logon.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="46356-344">0x00800000</span><span class="sxs-lookup"><span data-stu-id="46356-344">0x00800000</span></span></td>
<td><span data-ttu-id="46356-345"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_PASSWORD_EXPIRED</strong></a></span><span class="sxs-lookup"><span data-stu-id="46356-345"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_PASSWORD_EXPIRED</strong></a></span></span></td>
<td><span data-ttu-id="46356-346">Le mot de passe de l’utilisateur a expiré.</span><span class="sxs-lookup"><span data-stu-id="46356-346">The user password has expired.</span></span> <span data-ttu-id="46356-347">Cet indicateur est créé par le système à l’aide des données de l’attribut <a href="a-pwdlastset.md"><strong>PWD-Last-Set</strong></a> et de la stratégie de domaine.</span><span class="sxs-lookup"><span data-stu-id="46356-347">This flag is created by the system using data from the <a href="a-pwdlastset.md"><strong>Pwd-Last-Set</strong></a> attribute and the domain policy.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="46356-348">0x01000000</span><span class="sxs-lookup"><span data-stu-id="46356-348">0x01000000</span></span></td>
<td><span data-ttu-id="46356-349"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_TRUSTED_TO_AUTHENTICATE_FOR_DELEGATION</strong></a></span><span class="sxs-lookup"><span data-stu-id="46356-349"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_TRUSTED_TO_AUTHENTICATE_FOR_DELEGATION</strong></a></span></span></td>
<td><span data-ttu-id="46356-350">Le compte est activé pour la délégation.</span><span class="sxs-lookup"><span data-stu-id="46356-350">The account is enabled for delegation.</span></span> <span data-ttu-id="46356-351">Il s’agit d’un paramètre sensible à la sécurité. les comptes pour lesquels cette option est activée doivent être contrôlés de manière stricte.</span><span class="sxs-lookup"><span data-stu-id="46356-351">This is a security-sensitive setting; accounts with this option enabled should be strictly controlled.</span></span> <span data-ttu-id="46356-352">Ce paramètre permet à un service s’exécutant sous le compte de supposer une identité client et de s’authentifier en tant qu’utilisateur sur d’autres serveurs distants sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="46356-352">This setting enables a service running under the account to assume a client identity and authenticate as that user to other remote servers on the network.</span></span></td>
</tr>
</tbody>
</table>



 

