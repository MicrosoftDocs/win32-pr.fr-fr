---
title: USN-DSA-Last-obj-attribut supprimé
description: Contient le numéro de séquence de mise à jour (USN) pour le dernier objet système qui a été supprimé d’un serveur.
ms.assetid: af0afd80-fe4a-4bc6-84e3-14c2900bec93
ms.tgt_platform: multiple
keywords:
- USN-DSA-Last-obj-attribut supprimé-schéma AD
- Schéma AD de l’attribut uSNDSALastObjRemoved
topic_type:
- apiref
api_name:
- USN-DSA-Last-Obj-Removed
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcbc246aa1a0f7c794b9dc0a9d2a725273a918e3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103943222"
---
# <a name="usn-dsa-last-obj-removed-attribute"></a><span data-ttu-id="18859-105">USN-DSA-Last-obj-attribut supprimé</span><span class="sxs-lookup"><span data-stu-id="18859-105">USN-DSA-Last-Obj-Removed attribute</span></span>

<span data-ttu-id="18859-106">Contient le numéro de séquence de mise à jour (USN) pour le dernier objet système qui a été supprimé d’un serveur.</span><span class="sxs-lookup"><span data-stu-id="18859-106">Contains the update sequence number (USN) for the last system object that was removed from a server.</span></span>



| <span data-ttu-id="18859-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="18859-107">Entry</span></span> | <span data-ttu-id="18859-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="18859-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="18859-109">CN</span><span class="sxs-lookup"><span data-stu-id="18859-109">CN</span></span>                | <span data-ttu-id="18859-110">USN-DSA-Last-obj-supprimé</span><span class="sxs-lookup"><span data-stu-id="18859-110">USN-DSA-Last-Obj-Removed</span></span>             |
| <span data-ttu-id="18859-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="18859-111">Ldap-Display-Name</span></span> | <span data-ttu-id="18859-112">uSNDSALastObjRemoved</span><span class="sxs-lookup"><span data-stu-id="18859-112">uSNDSALastObjRemoved</span></span>                 |
| <span data-ttu-id="18859-113">Taille</span><span class="sxs-lookup"><span data-stu-id="18859-113">Size</span></span>              | <span data-ttu-id="18859-114">8 octets</span><span class="sxs-lookup"><span data-stu-id="18859-114">8 bytes</span></span>                              |
| <span data-ttu-id="18859-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="18859-115">Update Privilege</span></span>  | <span data-ttu-id="18859-116">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="18859-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="18859-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="18859-117">Update Frequency</span></span>  | <span data-ttu-id="18859-118">À chaque modification d’un objet d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="18859-118">Whenever a directory object changes.</span></span> |
| <span data-ttu-id="18859-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="18859-119">Attribute-Id</span></span>      | <span data-ttu-id="18859-120">1.2.840.113556.1.2.267</span><span class="sxs-lookup"><span data-stu-id="18859-120">1.2.840.113556.1.2.267</span></span>               |
| <span data-ttu-id="18859-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="18859-121">System-Id-Guid</span></span>    | <span data-ttu-id="18859-122">bf967a71-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="18859-122">bf967a71-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="18859-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="18859-123">Syntax</span></span>            | [<span data-ttu-id="18859-124">**Défini**</span><span class="sxs-lookup"><span data-stu-id="18859-124">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="18859-125">Implémentations</span><span class="sxs-lookup"><span data-stu-id="18859-125">Implementations</span></span>

-   [<span data-ttu-id="18859-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="18859-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="18859-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="18859-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="18859-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="18859-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="18859-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="18859-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="18859-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="18859-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="18859-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="18859-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="18859-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="18859-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="18859-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="18859-133">Windows 2000 Server</span></span>



| <span data-ttu-id="18859-134">Entrée</span><span class="sxs-lookup"><span data-stu-id="18859-134">Entry</span></span> | <span data-ttu-id="18859-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="18859-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="18859-136">ID de lien</span><span class="sxs-lookup"><span data-stu-id="18859-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="18859-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18859-137">MAPI-Id</span></span>                | <span data-ttu-id="18859-138">0x8155</span><span class="sxs-lookup"><span data-stu-id="18859-138">0x8155</span></span>                          |
| <span data-ttu-id="18859-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="18859-139">System-Only</span></span>            | <span data-ttu-id="18859-140">Vrai</span><span class="sxs-lookup"><span data-stu-id="18859-140">True</span></span>                            |
| <span data-ttu-id="18859-141">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="18859-141">Is-Single-Valued</span></span>       | <span data-ttu-id="18859-142">Vrai</span><span class="sxs-lookup"><span data-stu-id="18859-142">True</span></span>                            |
| <span data-ttu-id="18859-143">Est indexé</span><span class="sxs-lookup"><span data-stu-id="18859-143">Is Indexed</span></span>             | <span data-ttu-id="18859-144">Faux</span><span class="sxs-lookup"><span data-stu-id="18859-144">False</span></span>                           |
| <span data-ttu-id="18859-145">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="18859-145">In Global Catalog</span></span>      | <span data-ttu-id="18859-146">Faux</span><span class="sxs-lookup"><span data-stu-id="18859-146">False</span></span>                           |
| <span data-ttu-id="18859-147">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="18859-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="18859-148">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="18859-148">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="18859-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18859-149">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="18859-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18859-150">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="18859-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18859-151">Search-Flags</span></span>           | <span data-ttu-id="18859-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="18859-152">0x00000000</span></span>                      |
| <span data-ttu-id="18859-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18859-153">System-Flags</span></span>           | <span data-ttu-id="18859-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="18859-154">0x00000010</span></span>                      |
| <span data-ttu-id="18859-155">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="18859-155">Classes used in</span></span>        | [<span data-ttu-id="18859-156">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="18859-156">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="18859-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="18859-157">Windows Server 2003</span></span>



| <span data-ttu-id="18859-158">Entrée</span><span class="sxs-lookup"><span data-stu-id="18859-158">Entry</span></span> | <span data-ttu-id="18859-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="18859-159">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="18859-160">ID de lien</span><span class="sxs-lookup"><span data-stu-id="18859-160">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="18859-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18859-161">MAPI-Id</span></span>                | <span data-ttu-id="18859-162">0x8155</span><span class="sxs-lookup"><span data-stu-id="18859-162">0x8155</span></span>                          |
| <span data-ttu-id="18859-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="18859-163">System-Only</span></span>            | <span data-ttu-id="18859-164">Vrai</span><span class="sxs-lookup"><span data-stu-id="18859-164">True</span></span>                            |
| <span data-ttu-id="18859-165">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="18859-165">Is-Single-Valued</span></span>       | <span data-ttu-id="18859-166">Vrai</span><span class="sxs-lookup"><span data-stu-id="18859-166">True</span></span>                            |
| <span data-ttu-id="18859-167">Est indexé</span><span class="sxs-lookup"><span data-stu-id="18859-167">Is Indexed</span></span>             | <span data-ttu-id="18859-168">Faux</span><span class="sxs-lookup"><span data-stu-id="18859-168">False</span></span>                           |
| <span data-ttu-id="18859-169">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="18859-169">In Global Catalog</span></span>      | <span data-ttu-id="18859-170">Faux</span><span class="sxs-lookup"><span data-stu-id="18859-170">False</span></span>                           |
| <span data-ttu-id="18859-171">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="18859-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="18859-172">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="18859-172">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="18859-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18859-173">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="18859-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18859-174">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="18859-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18859-175">Search-Flags</span></span>           | <span data-ttu-id="18859-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="18859-176">0x00000000</span></span>                      |
| <span data-ttu-id="18859-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18859-177">System-Flags</span></span>           | <span data-ttu-id="18859-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="18859-178">0x00000010</span></span>                      |
| <span data-ttu-id="18859-179">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="18859-179">Classes used in</span></span>        | [<span data-ttu-id="18859-180">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="18859-180">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="18859-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="18859-181">ADAM</span></span>



| <span data-ttu-id="18859-182">Entrée</span><span class="sxs-lookup"><span data-stu-id="18859-182">Entry</span></span> | <span data-ttu-id="18859-183">Valeur</span><span class="sxs-lookup"><span data-stu-id="18859-183">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="18859-184">ID de lien</span><span class="sxs-lookup"><span data-stu-id="18859-184">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="18859-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18859-185">MAPI-Id</span></span>                | <span data-ttu-id="18859-186">0x8155</span><span class="sxs-lookup"><span data-stu-id="18859-186">0x8155</span></span>                          |
| <span data-ttu-id="18859-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="18859-187">System-Only</span></span>            | <span data-ttu-id="18859-188">Vrai</span><span class="sxs-lookup"><span data-stu-id="18859-188">True</span></span>                            |
| <span data-ttu-id="18859-189">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="18859-189">Is-Single-Valued</span></span>       | <span data-ttu-id="18859-190">Vrai</span><span class="sxs-lookup"><span data-stu-id="18859-190">True</span></span>                            |
| <span data-ttu-id="18859-191">Est indexé</span><span class="sxs-lookup"><span data-stu-id="18859-191">Is Indexed</span></span>             | <span data-ttu-id="18859-192">Faux</span><span class="sxs-lookup"><span data-stu-id="18859-192">False</span></span>                           |
| <span data-ttu-id="18859-193">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="18859-193">In Global Catalog</span></span>      | <span data-ttu-id="18859-194">Faux</span><span class="sxs-lookup"><span data-stu-id="18859-194">False</span></span>                           |
| <span data-ttu-id="18859-195">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="18859-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="18859-196">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="18859-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="18859-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18859-197">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="18859-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18859-198">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="18859-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18859-199">Search-Flags</span></span>           | <span data-ttu-id="18859-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="18859-200">0x00000000</span></span>                      |
| <span data-ttu-id="18859-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18859-201">System-Flags</span></span>           | <span data-ttu-id="18859-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="18859-202">0x00000010</span></span>                      |
| <span data-ttu-id="18859-203">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="18859-203">Classes used in</span></span>        | [<span data-ttu-id="18859-204">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="18859-204">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="18859-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="18859-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="18859-206">Entrée</span><span class="sxs-lookup"><span data-stu-id="18859-206">Entry</span></span> | <span data-ttu-id="18859-207">Valeur</span><span class="sxs-lookup"><span data-stu-id="18859-207">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="18859-208">ID de lien</span><span class="sxs-lookup"><span data-stu-id="18859-208">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="18859-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18859-209">MAPI-Id</span></span>                | <span data-ttu-id="18859-210">0x8155</span><span class="sxs-lookup"><span data-stu-id="18859-210">0x8155</span></span>                          |
| <span data-ttu-id="18859-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="18859-211">System-Only</span></span>            | <span data-ttu-id="18859-212">Vrai</span><span class="sxs-lookup"><span data-stu-id="18859-212">True</span></span>                            |
| <span data-ttu-id="18859-213">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="18859-213">Is-Single-Valued</span></span>       | <span data-ttu-id="18859-214">Vrai</span><span class="sxs-lookup"><span data-stu-id="18859-214">True</span></span>                            |
| <span data-ttu-id="18859-215">Est indexé</span><span class="sxs-lookup"><span data-stu-id="18859-215">Is Indexed</span></span>             | <span data-ttu-id="18859-216">Faux</span><span class="sxs-lookup"><span data-stu-id="18859-216">False</span></span>                           |
| <span data-ttu-id="18859-217">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="18859-217">In Global Catalog</span></span>      | <span data-ttu-id="18859-218">Faux</span><span class="sxs-lookup"><span data-stu-id="18859-218">False</span></span>                           |
| <span data-ttu-id="18859-219">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="18859-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="18859-220">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="18859-220">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="18859-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18859-221">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="18859-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18859-222">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="18859-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18859-223">Search-Flags</span></span>           | <span data-ttu-id="18859-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="18859-224">0x00000000</span></span>                      |
| <span data-ttu-id="18859-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18859-225">System-Flags</span></span>           | <span data-ttu-id="18859-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="18859-226">0x00000010</span></span>                      |
| <span data-ttu-id="18859-227">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="18859-227">Classes used in</span></span>        | [<span data-ttu-id="18859-228">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="18859-228">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="18859-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="18859-229">Windows Server 2008</span></span>



| <span data-ttu-id="18859-230">Entrée</span><span class="sxs-lookup"><span data-stu-id="18859-230">Entry</span></span> | <span data-ttu-id="18859-231">Valeur</span><span class="sxs-lookup"><span data-stu-id="18859-231">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="18859-232">ID de lien</span><span class="sxs-lookup"><span data-stu-id="18859-232">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="18859-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18859-233">MAPI-Id</span></span>                | <span data-ttu-id="18859-234">0x8155</span><span class="sxs-lookup"><span data-stu-id="18859-234">0x8155</span></span>                          |
| <span data-ttu-id="18859-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="18859-235">System-Only</span></span>            | <span data-ttu-id="18859-236">Vrai</span><span class="sxs-lookup"><span data-stu-id="18859-236">True</span></span>                            |
| <span data-ttu-id="18859-237">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="18859-237">Is-Single-Valued</span></span>       | <span data-ttu-id="18859-238">Vrai</span><span class="sxs-lookup"><span data-stu-id="18859-238">True</span></span>                            |
| <span data-ttu-id="18859-239">Est indexé</span><span class="sxs-lookup"><span data-stu-id="18859-239">Is Indexed</span></span>             | <span data-ttu-id="18859-240">Faux</span><span class="sxs-lookup"><span data-stu-id="18859-240">False</span></span>                           |
| <span data-ttu-id="18859-241">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="18859-241">In Global Catalog</span></span>      | <span data-ttu-id="18859-242">Faux</span><span class="sxs-lookup"><span data-stu-id="18859-242">False</span></span>                           |
| <span data-ttu-id="18859-243">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="18859-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="18859-244">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="18859-244">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="18859-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18859-245">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="18859-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18859-246">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="18859-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18859-247">Search-Flags</span></span>           | <span data-ttu-id="18859-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="18859-248">0x00000000</span></span>                      |
| <span data-ttu-id="18859-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18859-249">System-Flags</span></span>           | <span data-ttu-id="18859-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="18859-250">0x00000010</span></span>                      |
| <span data-ttu-id="18859-251">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="18859-251">Classes used in</span></span>        | [<span data-ttu-id="18859-252">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="18859-252">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="18859-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="18859-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="18859-254">Entrée</span><span class="sxs-lookup"><span data-stu-id="18859-254">Entry</span></span> | <span data-ttu-id="18859-255">Valeur</span><span class="sxs-lookup"><span data-stu-id="18859-255">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="18859-256">ID de lien</span><span class="sxs-lookup"><span data-stu-id="18859-256">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="18859-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18859-257">MAPI-Id</span></span>                | <span data-ttu-id="18859-258">0x8155</span><span class="sxs-lookup"><span data-stu-id="18859-258">0x8155</span></span>                          |
| <span data-ttu-id="18859-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="18859-259">System-Only</span></span>            | <span data-ttu-id="18859-260">Vrai</span><span class="sxs-lookup"><span data-stu-id="18859-260">True</span></span>                            |
| <span data-ttu-id="18859-261">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="18859-261">Is-Single-Valued</span></span>       | <span data-ttu-id="18859-262">Vrai</span><span class="sxs-lookup"><span data-stu-id="18859-262">True</span></span>                            |
| <span data-ttu-id="18859-263">Est indexé</span><span class="sxs-lookup"><span data-stu-id="18859-263">Is Indexed</span></span>             | <span data-ttu-id="18859-264">Faux</span><span class="sxs-lookup"><span data-stu-id="18859-264">False</span></span>                           |
| <span data-ttu-id="18859-265">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="18859-265">In Global Catalog</span></span>      | <span data-ttu-id="18859-266">Faux</span><span class="sxs-lookup"><span data-stu-id="18859-266">False</span></span>                           |
| <span data-ttu-id="18859-267">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="18859-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="18859-268">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="18859-268">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="18859-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18859-269">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="18859-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18859-270">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="18859-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18859-271">Search-Flags</span></span>           | <span data-ttu-id="18859-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="18859-272">0x00000000</span></span>                      |
| <span data-ttu-id="18859-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18859-273">System-Flags</span></span>           | <span data-ttu-id="18859-274">0x00000010</span><span class="sxs-lookup"><span data-stu-id="18859-274">0x00000010</span></span>                      |
| <span data-ttu-id="18859-275">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="18859-275">Classes used in</span></span>        | [<span data-ttu-id="18859-276">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="18859-276">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="18859-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="18859-277">Windows Server 2012</span></span>



| <span data-ttu-id="18859-278">Entrée</span><span class="sxs-lookup"><span data-stu-id="18859-278">Entry</span></span> | <span data-ttu-id="18859-279">Valeur</span><span class="sxs-lookup"><span data-stu-id="18859-279">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="18859-280">ID de lien</span><span class="sxs-lookup"><span data-stu-id="18859-280">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="18859-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18859-281">MAPI-Id</span></span>                | <span data-ttu-id="18859-282">0x8155</span><span class="sxs-lookup"><span data-stu-id="18859-282">0x8155</span></span>                          |
| <span data-ttu-id="18859-283">System-Only</span><span class="sxs-lookup"><span data-stu-id="18859-283">System-Only</span></span>            | <span data-ttu-id="18859-284">Vrai</span><span class="sxs-lookup"><span data-stu-id="18859-284">True</span></span>                            |
| <span data-ttu-id="18859-285">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="18859-285">Is-Single-Valued</span></span>       | <span data-ttu-id="18859-286">Vrai</span><span class="sxs-lookup"><span data-stu-id="18859-286">True</span></span>                            |
| <span data-ttu-id="18859-287">Est indexé</span><span class="sxs-lookup"><span data-stu-id="18859-287">Is Indexed</span></span>             | <span data-ttu-id="18859-288">Faux</span><span class="sxs-lookup"><span data-stu-id="18859-288">False</span></span>                           |
| <span data-ttu-id="18859-289">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="18859-289">In Global Catalog</span></span>      | <span data-ttu-id="18859-290">Faux</span><span class="sxs-lookup"><span data-stu-id="18859-290">False</span></span>                           |
| <span data-ttu-id="18859-291">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="18859-291">NT-Security-Descriptor</span></span> | <span data-ttu-id="18859-292">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="18859-292">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="18859-293">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18859-293">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="18859-294">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18859-294">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="18859-295">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18859-295">Search-Flags</span></span>           | <span data-ttu-id="18859-296">0x00000000</span><span class="sxs-lookup"><span data-stu-id="18859-296">0x00000000</span></span>                      |
| <span data-ttu-id="18859-297">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18859-297">System-Flags</span></span>           | <span data-ttu-id="18859-298">0x00000010</span><span class="sxs-lookup"><span data-stu-id="18859-298">0x00000010</span></span>                      |
| <span data-ttu-id="18859-299">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="18859-299">Classes used in</span></span>        | [<span data-ttu-id="18859-300">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="18859-300">**Top**</span></span>](c-top.md)<br/> |



## <a name="see-also"></a><span data-ttu-id="18859-301">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18859-301">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18859-302">**USN-Last-obj-REM**</span><span class="sxs-lookup"><span data-stu-id="18859-302">**USN-Last-Obj-Rem**</span></span>](a-usnlastobjrem.md)
</dt> </dl>

 

 





