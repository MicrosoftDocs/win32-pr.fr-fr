---
title: Attribut Last-Logon
description: La dernière fois que l’utilisateur a ouvert une session.
ms.assetid: 271f4f38-90f9-4add-a3ed-413c224e1fae
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Last-Logon
- Schéma AD de l’attribut lastLogon
topic_type:
- apiref
api_name:
- Last-Logon
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae01ffabf2d4862c030607b997a4d9057b934f8f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845234"
---
# <a name="last-logon-attribute"></a><span data-ttu-id="687cb-105">Attribut Last-Logon</span><span class="sxs-lookup"><span data-stu-id="687cb-105">Last-Logon attribute</span></span>

<span data-ttu-id="687cb-106">La dernière fois que l’utilisateur a ouvert une session.</span><span class="sxs-lookup"><span data-stu-id="687cb-106">The last time the user logged on.</span></span> <span data-ttu-id="687cb-107">Cette valeur est stockée sous la forme d’un grand entier qui représente le nombre d’intervalles de 100 nanosecondes depuis le 1er janvier 1601 (UTC).</span><span class="sxs-lookup"><span data-stu-id="687cb-107">This value is stored as a large integer that represents the number of 100-nanosecond intervals since January 1, 1601 (UTC).</span></span> <span data-ttu-id="687cb-108">La valeur zéro signifie que l’heure de la dernière connexion est inconnue.</span><span class="sxs-lookup"><span data-stu-id="687cb-108">A value of zero means that the last logon time is unknown.</span></span>



| <span data-ttu-id="687cb-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="687cb-109">Entry</span></span> | <span data-ttu-id="687cb-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="687cb-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="687cb-111">CN</span><span class="sxs-lookup"><span data-stu-id="687cb-111">CN</span></span>                | <span data-ttu-id="687cb-112">Last-Logon</span><span class="sxs-lookup"><span data-stu-id="687cb-112">Last-Logon</span></span>                           |
| <span data-ttu-id="687cb-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="687cb-113">Ldap-Display-Name</span></span> | <span data-ttu-id="687cb-114">lastLogon</span><span class="sxs-lookup"><span data-stu-id="687cb-114">lastLogon</span></span>                            |
| <span data-ttu-id="687cb-115">Taille</span><span class="sxs-lookup"><span data-stu-id="687cb-115">Size</span></span>              | <span data-ttu-id="687cb-116">8 octets</span><span class="sxs-lookup"><span data-stu-id="687cb-116">8 bytes</span></span>                              |
| <span data-ttu-id="687cb-117">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="687cb-117">Update Privilege</span></span>  | <span data-ttu-id="687cb-118">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="687cb-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="687cb-119">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="687cb-119">Update Frequency</span></span>  | <span data-ttu-id="687cb-120">Chaque fois que l’utilisateur ouvre une session.</span><span class="sxs-lookup"><span data-stu-id="687cb-120">Each time the user logs on.</span></span>          |
| <span data-ttu-id="687cb-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="687cb-121">Attribute-Id</span></span>      | <span data-ttu-id="687cb-122">1.2.840.113556.1.4.52</span><span class="sxs-lookup"><span data-stu-id="687cb-122">1.2.840.113556.1.4.52</span></span>                |
| <span data-ttu-id="687cb-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="687cb-123">System-Id-Guid</span></span>    | <span data-ttu-id="687cb-124">bf967997-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="687cb-124">bf967997-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="687cb-125">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="687cb-125">Syntax</span></span>            | [<span data-ttu-id="687cb-126">**Défini**</span><span class="sxs-lookup"><span data-stu-id="687cb-126">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="687cb-127">Implémentations</span><span class="sxs-lookup"><span data-stu-id="687cb-127">Implementations</span></span>

-   [<span data-ttu-id="687cb-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="687cb-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="687cb-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="687cb-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="687cb-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="687cb-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="687cb-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="687cb-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="687cb-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="687cb-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="687cb-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="687cb-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="687cb-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="687cb-134">Windows 2000 Server</span></span>



| <span data-ttu-id="687cb-135">Entrée</span><span class="sxs-lookup"><span data-stu-id="687cb-135">Entry</span></span> | <span data-ttu-id="687cb-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="687cb-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="687cb-137">ID de lien</span><span class="sxs-lookup"><span data-stu-id="687cb-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="687cb-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="687cb-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="687cb-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="687cb-139">System-Only</span></span>            | <span data-ttu-id="687cb-140">Faux</span><span class="sxs-lookup"><span data-stu-id="687cb-140">False</span></span>                             |
| <span data-ttu-id="687cb-141">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="687cb-141">Is-Single-Valued</span></span>       | <span data-ttu-id="687cb-142">Vrai</span><span class="sxs-lookup"><span data-stu-id="687cb-142">True</span></span>                              |
| <span data-ttu-id="687cb-143">Est indexé</span><span class="sxs-lookup"><span data-stu-id="687cb-143">Is Indexed</span></span>             | <span data-ttu-id="687cb-144">Faux</span><span class="sxs-lookup"><span data-stu-id="687cb-144">False</span></span>                             |
| <span data-ttu-id="687cb-145">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="687cb-145">In Global Catalog</span></span>      | <span data-ttu-id="687cb-146">Faux</span><span class="sxs-lookup"><span data-stu-id="687cb-146">False</span></span>                             |
| <span data-ttu-id="687cb-147">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="687cb-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="687cb-148">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="687cb-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="687cb-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="687cb-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="687cb-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="687cb-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="687cb-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="687cb-151">Search-Flags</span></span>           | <span data-ttu-id="687cb-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="687cb-152">0x00000000</span></span>                        |
| <span data-ttu-id="687cb-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="687cb-153">System-Flags</span></span>           | <span data-ttu-id="687cb-154">0x00000011</span><span class="sxs-lookup"><span data-stu-id="687cb-154">0x00000011</span></span>                        |
| <span data-ttu-id="687cb-155">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="687cb-155">Classes used in</span></span>        | [<span data-ttu-id="687cb-156">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="687cb-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="687cb-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="687cb-157">Windows Server 2003</span></span>



| <span data-ttu-id="687cb-158">Entrée</span><span class="sxs-lookup"><span data-stu-id="687cb-158">Entry</span></span> | <span data-ttu-id="687cb-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="687cb-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="687cb-160">ID de lien</span><span class="sxs-lookup"><span data-stu-id="687cb-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="687cb-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="687cb-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="687cb-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="687cb-162">System-Only</span></span>            | <span data-ttu-id="687cb-163">Faux</span><span class="sxs-lookup"><span data-stu-id="687cb-163">False</span></span>                             |
| <span data-ttu-id="687cb-164">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="687cb-164">Is-Single-Valued</span></span>       | <span data-ttu-id="687cb-165">Vrai</span><span class="sxs-lookup"><span data-stu-id="687cb-165">True</span></span>                              |
| <span data-ttu-id="687cb-166">Est indexé</span><span class="sxs-lookup"><span data-stu-id="687cb-166">Is Indexed</span></span>             | <span data-ttu-id="687cb-167">Faux</span><span class="sxs-lookup"><span data-stu-id="687cb-167">False</span></span>                             |
| <span data-ttu-id="687cb-168">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="687cb-168">In Global Catalog</span></span>      | <span data-ttu-id="687cb-169">Faux</span><span class="sxs-lookup"><span data-stu-id="687cb-169">False</span></span>                             |
| <span data-ttu-id="687cb-170">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="687cb-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="687cb-171">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="687cb-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="687cb-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="687cb-172">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="687cb-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="687cb-173">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="687cb-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="687cb-174">Search-Flags</span></span>           | <span data-ttu-id="687cb-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="687cb-175">0x00000000</span></span>                        |
| <span data-ttu-id="687cb-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="687cb-176">System-Flags</span></span>           | <span data-ttu-id="687cb-177">0x00000011</span><span class="sxs-lookup"><span data-stu-id="687cb-177">0x00000011</span></span>                        |
| <span data-ttu-id="687cb-178">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="687cb-178">Classes used in</span></span>        | [<span data-ttu-id="687cb-179">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="687cb-179">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="687cb-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="687cb-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="687cb-181">Entrée</span><span class="sxs-lookup"><span data-stu-id="687cb-181">Entry</span></span> | <span data-ttu-id="687cb-182">Valeur</span><span class="sxs-lookup"><span data-stu-id="687cb-182">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="687cb-183">ID de lien</span><span class="sxs-lookup"><span data-stu-id="687cb-183">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="687cb-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="687cb-184">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="687cb-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="687cb-185">System-Only</span></span>            | <span data-ttu-id="687cb-186">Faux</span><span class="sxs-lookup"><span data-stu-id="687cb-186">False</span></span>                             |
| <span data-ttu-id="687cb-187">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="687cb-187">Is-Single-Valued</span></span>       | <span data-ttu-id="687cb-188">Vrai</span><span class="sxs-lookup"><span data-stu-id="687cb-188">True</span></span>                              |
| <span data-ttu-id="687cb-189">Est indexé</span><span class="sxs-lookup"><span data-stu-id="687cb-189">Is Indexed</span></span>             | <span data-ttu-id="687cb-190">Faux</span><span class="sxs-lookup"><span data-stu-id="687cb-190">False</span></span>                             |
| <span data-ttu-id="687cb-191">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="687cb-191">In Global Catalog</span></span>      | <span data-ttu-id="687cb-192">Faux</span><span class="sxs-lookup"><span data-stu-id="687cb-192">False</span></span>                             |
| <span data-ttu-id="687cb-193">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="687cb-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="687cb-194">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="687cb-194">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="687cb-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="687cb-195">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="687cb-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="687cb-196">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="687cb-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="687cb-197">Search-Flags</span></span>           | <span data-ttu-id="687cb-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="687cb-198">0x00000000</span></span>                        |
| <span data-ttu-id="687cb-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="687cb-199">System-Flags</span></span>           | <span data-ttu-id="687cb-200">0x00000011</span><span class="sxs-lookup"><span data-stu-id="687cb-200">0x00000011</span></span>                        |
| <span data-ttu-id="687cb-201">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="687cb-201">Classes used in</span></span>        | [<span data-ttu-id="687cb-202">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="687cb-202">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="687cb-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="687cb-203">Windows Server 2008</span></span>



| <span data-ttu-id="687cb-204">Entrée</span><span class="sxs-lookup"><span data-stu-id="687cb-204">Entry</span></span> | <span data-ttu-id="687cb-205">Valeur</span><span class="sxs-lookup"><span data-stu-id="687cb-205">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="687cb-206">ID de lien</span><span class="sxs-lookup"><span data-stu-id="687cb-206">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="687cb-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="687cb-207">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="687cb-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="687cb-208">System-Only</span></span>            | <span data-ttu-id="687cb-209">Faux</span><span class="sxs-lookup"><span data-stu-id="687cb-209">False</span></span>                             |
| <span data-ttu-id="687cb-210">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="687cb-210">Is-Single-Valued</span></span>       | <span data-ttu-id="687cb-211">Vrai</span><span class="sxs-lookup"><span data-stu-id="687cb-211">True</span></span>                              |
| <span data-ttu-id="687cb-212">Est indexé</span><span class="sxs-lookup"><span data-stu-id="687cb-212">Is Indexed</span></span>             | <span data-ttu-id="687cb-213">Faux</span><span class="sxs-lookup"><span data-stu-id="687cb-213">False</span></span>                             |
| <span data-ttu-id="687cb-214">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="687cb-214">In Global Catalog</span></span>      | <span data-ttu-id="687cb-215">Faux</span><span class="sxs-lookup"><span data-stu-id="687cb-215">False</span></span>                             |
| <span data-ttu-id="687cb-216">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="687cb-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="687cb-217">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="687cb-217">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="687cb-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="687cb-218">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="687cb-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="687cb-219">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="687cb-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="687cb-220">Search-Flags</span></span>           | <span data-ttu-id="687cb-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="687cb-221">0x00000000</span></span>                        |
| <span data-ttu-id="687cb-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="687cb-222">System-Flags</span></span>           | <span data-ttu-id="687cb-223">0x00000011</span><span class="sxs-lookup"><span data-stu-id="687cb-223">0x00000011</span></span>                        |
| <span data-ttu-id="687cb-224">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="687cb-224">Classes used in</span></span>        | [<span data-ttu-id="687cb-225">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="687cb-225">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="687cb-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="687cb-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="687cb-227">Entrée</span><span class="sxs-lookup"><span data-stu-id="687cb-227">Entry</span></span> | <span data-ttu-id="687cb-228">Valeur</span><span class="sxs-lookup"><span data-stu-id="687cb-228">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="687cb-229">ID de lien</span><span class="sxs-lookup"><span data-stu-id="687cb-229">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="687cb-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="687cb-230">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="687cb-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="687cb-231">System-Only</span></span>            | <span data-ttu-id="687cb-232">Faux</span><span class="sxs-lookup"><span data-stu-id="687cb-232">False</span></span>                             |
| <span data-ttu-id="687cb-233">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="687cb-233">Is-Single-Valued</span></span>       | <span data-ttu-id="687cb-234">Vrai</span><span class="sxs-lookup"><span data-stu-id="687cb-234">True</span></span>                              |
| <span data-ttu-id="687cb-235">Est indexé</span><span class="sxs-lookup"><span data-stu-id="687cb-235">Is Indexed</span></span>             | <span data-ttu-id="687cb-236">Faux</span><span class="sxs-lookup"><span data-stu-id="687cb-236">False</span></span>                             |
| <span data-ttu-id="687cb-237">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="687cb-237">In Global Catalog</span></span>      | <span data-ttu-id="687cb-238">Faux</span><span class="sxs-lookup"><span data-stu-id="687cb-238">False</span></span>                             |
| <span data-ttu-id="687cb-239">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="687cb-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="687cb-240">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="687cb-240">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="687cb-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="687cb-241">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="687cb-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="687cb-242">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="687cb-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="687cb-243">Search-Flags</span></span>           | <span data-ttu-id="687cb-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="687cb-244">0x00000000</span></span>                        |
| <span data-ttu-id="687cb-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="687cb-245">System-Flags</span></span>           | <span data-ttu-id="687cb-246">0x00000011</span><span class="sxs-lookup"><span data-stu-id="687cb-246">0x00000011</span></span>                        |
| <span data-ttu-id="687cb-247">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="687cb-247">Classes used in</span></span>        | [<span data-ttu-id="687cb-248">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="687cb-248">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="687cb-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="687cb-249">Windows Server 2012</span></span>



| <span data-ttu-id="687cb-250">Entrée</span><span class="sxs-lookup"><span data-stu-id="687cb-250">Entry</span></span> | <span data-ttu-id="687cb-251">Valeur</span><span class="sxs-lookup"><span data-stu-id="687cb-251">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="687cb-252">ID de lien</span><span class="sxs-lookup"><span data-stu-id="687cb-252">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="687cb-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="687cb-253">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="687cb-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="687cb-254">System-Only</span></span>            | <span data-ttu-id="687cb-255">Faux</span><span class="sxs-lookup"><span data-stu-id="687cb-255">False</span></span>                             |
| <span data-ttu-id="687cb-256">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="687cb-256">Is-Single-Valued</span></span>       | <span data-ttu-id="687cb-257">Vrai</span><span class="sxs-lookup"><span data-stu-id="687cb-257">True</span></span>                              |
| <span data-ttu-id="687cb-258">Est indexé</span><span class="sxs-lookup"><span data-stu-id="687cb-258">Is Indexed</span></span>             | <span data-ttu-id="687cb-259">Faux</span><span class="sxs-lookup"><span data-stu-id="687cb-259">False</span></span>                             |
| <span data-ttu-id="687cb-260">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="687cb-260">In Global Catalog</span></span>      | <span data-ttu-id="687cb-261">Faux</span><span class="sxs-lookup"><span data-stu-id="687cb-261">False</span></span>                             |
| <span data-ttu-id="687cb-262">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="687cb-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="687cb-263">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="687cb-263">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="687cb-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="687cb-264">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="687cb-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="687cb-265">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="687cb-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="687cb-266">Search-Flags</span></span>           | <span data-ttu-id="687cb-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="687cb-267">0x00000000</span></span>                        |
| <span data-ttu-id="687cb-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="687cb-268">System-Flags</span></span>           | <span data-ttu-id="687cb-269">0x00000011</span><span class="sxs-lookup"><span data-stu-id="687cb-269">0x00000011</span></span>                        |
| <span data-ttu-id="687cb-270">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="687cb-270">Classes used in</span></span>        | [<span data-ttu-id="687cb-271">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="687cb-271">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="687cb-272">Notes</span><span class="sxs-lookup"><span data-stu-id="687cb-272">Remarks</span></span>

<span data-ttu-id="687cb-273">La partie haute de ce grand entier correspond au membre **dwHighDateTime** de la structure [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) et la partie inférieure correspond au membre **dwLowDateTime** de la structure **fileTime** .</span><span class="sxs-lookup"><span data-stu-id="687cb-273">The high part of this large integer corresponds to the **dwHighDateTime** member of the [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure and the low part corresponds to the **dwLowDateTime** member of the **FILETIME** structure.</span></span>

<span data-ttu-id="687cb-274">Cet attribut n’est pas répliqué et est conservé séparément sur chaque contrôleur de domaine du domaine.</span><span class="sxs-lookup"><span data-stu-id="687cb-274">This attribute is not replicated and is maintained separately on each domain controller in the domain.</span></span> <span data-ttu-id="687cb-275">Pour obtenir une valeur précise pour la dernière ouverture de session de l’utilisateur dans le domaine, l’attribut **Last-Logon** de l’utilisateur doit être récupéré à partir de chaque contrôleur de domaine du domaine.</span><span class="sxs-lookup"><span data-stu-id="687cb-275">To get an accurate value for the user's last logon in the domain, the **Last-Logon** attribute for the user must be retrieved from every domain controller in the domain.</span></span> <span data-ttu-id="687cb-276">La valeur la plus élevée Récupérée est l’heure de la dernière ouverture de session pour cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="687cb-276">The largest value that is retrieved is the true last logon time for that user.</span></span>

## <a name="see-also"></a><span data-ttu-id="687cb-277">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="687cb-277">See also</span></span>

<dl> <dt>

[<span data-ttu-id="687cb-278">**FILETIME**</span><span class="sxs-lookup"><span data-stu-id="687cb-278">**FILETIME**</span></span>](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)
</dt> </dl>

 

