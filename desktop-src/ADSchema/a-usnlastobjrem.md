---
title: Attribut USN-Last-obj-REM
description: Contient le numéro de séquence de mise à jour (USN) pour le dernier objet non-système qui a été supprimé d’un serveur.
ms.assetid: 34718bea-fa19-4084-b97f-d72a1681c3f4
ms.tgt_platform: multiple
keywords:
- Attribut USN-Last-obj-REM Attribute
- Schéma AD de l’attribut uSNLastObjRem
topic_type:
- apiref
api_name:
- USN-Last-Obj-Rem
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9836bd93ca065fdfa53b0246a5bab0142e84ced6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104519946"
---
# <a name="usn-last-obj-rem-attribute"></a><span data-ttu-id="aa6ff-105">Attribut USN-Last-obj-REM</span><span class="sxs-lookup"><span data-stu-id="aa6ff-105">USN-Last-Obj-Rem attribute</span></span>

<span data-ttu-id="aa6ff-106">Contient le numéro de séquence de mise à jour (USN) pour le dernier objet non-système qui a été supprimé d’un serveur.</span><span class="sxs-lookup"><span data-stu-id="aa6ff-106">Contains the update sequence number (USN) for the last non-system object that was removed from a server.</span></span>



| <span data-ttu-id="aa6ff-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="aa6ff-107">Entry</span></span> | <span data-ttu-id="aa6ff-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="aa6ff-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="aa6ff-109">CN</span><span class="sxs-lookup"><span data-stu-id="aa6ff-109">CN</span></span>                | <span data-ttu-id="aa6ff-110">USN-Last-obj-REM</span><span class="sxs-lookup"><span data-stu-id="aa6ff-110">USN-Last-Obj-Rem</span></span>                     |
| <span data-ttu-id="aa6ff-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="aa6ff-111">Ldap-Display-Name</span></span> | <span data-ttu-id="aa6ff-112">uSNLastObjRem</span><span class="sxs-lookup"><span data-stu-id="aa6ff-112">uSNLastObjRem</span></span>                        |
| <span data-ttu-id="aa6ff-113">Taille</span><span class="sxs-lookup"><span data-stu-id="aa6ff-113">Size</span></span>              | <span data-ttu-id="aa6ff-114">8 octets</span><span class="sxs-lookup"><span data-stu-id="aa6ff-114">8 bytes</span></span>                              |
| <span data-ttu-id="aa6ff-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="aa6ff-115">Update Privilege</span></span>  | <span data-ttu-id="aa6ff-116">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="aa6ff-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="aa6ff-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="aa6ff-117">Update Frequency</span></span>  | <span data-ttu-id="aa6ff-118">À chaque modification d’un objet d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="aa6ff-118">Whenever a directory object changes.</span></span> |
| <span data-ttu-id="aa6ff-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="aa6ff-119">Attribute-Id</span></span>      | <span data-ttu-id="aa6ff-120">1.2.840.113556.1.2.121</span><span class="sxs-lookup"><span data-stu-id="aa6ff-120">1.2.840.113556.1.2.121</span></span>               |
| <span data-ttu-id="aa6ff-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="aa6ff-121">System-Id-Guid</span></span>    | <span data-ttu-id="aa6ff-122">bf967a73-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="aa6ff-122">bf967a73-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="aa6ff-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aa6ff-123">Syntax</span></span>            | [<span data-ttu-id="aa6ff-124">**Défini**</span><span class="sxs-lookup"><span data-stu-id="aa6ff-124">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="aa6ff-125">Implémentations</span><span class="sxs-lookup"><span data-stu-id="aa6ff-125">Implementations</span></span>

-   [<span data-ttu-id="aa6ff-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="aa6ff-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="aa6ff-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="aa6ff-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="aa6ff-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="aa6ff-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="aa6ff-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="aa6ff-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="aa6ff-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="aa6ff-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="aa6ff-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="aa6ff-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="aa6ff-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="aa6ff-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="aa6ff-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="aa6ff-133">Windows 2000 Server</span></span>



| <span data-ttu-id="aa6ff-134">Entrée</span><span class="sxs-lookup"><span data-stu-id="aa6ff-134">Entry</span></span> | <span data-ttu-id="aa6ff-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="aa6ff-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="aa6ff-136">ID de lien</span><span class="sxs-lookup"><span data-stu-id="aa6ff-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="aa6ff-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aa6ff-137">MAPI-Id</span></span>                | <span data-ttu-id="aa6ff-138">0x8156</span><span class="sxs-lookup"><span data-stu-id="aa6ff-138">0x8156</span></span>                          |
| <span data-ttu-id="aa6ff-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="aa6ff-139">System-Only</span></span>            | <span data-ttu-id="aa6ff-140">Vrai</span><span class="sxs-lookup"><span data-stu-id="aa6ff-140">True</span></span>                            |
| <span data-ttu-id="aa6ff-141">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="aa6ff-141">Is-Single-Valued</span></span>       | <span data-ttu-id="aa6ff-142">Vrai</span><span class="sxs-lookup"><span data-stu-id="aa6ff-142">True</span></span>                            |
| <span data-ttu-id="aa6ff-143">Est indexé</span><span class="sxs-lookup"><span data-stu-id="aa6ff-143">Is Indexed</span></span>             | <span data-ttu-id="aa6ff-144">Faux</span><span class="sxs-lookup"><span data-stu-id="aa6ff-144">False</span></span>                           |
| <span data-ttu-id="aa6ff-145">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="aa6ff-145">In Global Catalog</span></span>      | <span data-ttu-id="aa6ff-146">Vrai</span><span class="sxs-lookup"><span data-stu-id="aa6ff-146">True</span></span>                            |
| <span data-ttu-id="aa6ff-147">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="aa6ff-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="aa6ff-148">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="aa6ff-148">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="aa6ff-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aa6ff-149">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="aa6ff-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aa6ff-150">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="aa6ff-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aa6ff-151">Search-Flags</span></span>           | <span data-ttu-id="aa6ff-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="aa6ff-152">0x00000000</span></span>                      |
| <span data-ttu-id="aa6ff-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aa6ff-153">System-Flags</span></span>           | <span data-ttu-id="aa6ff-154">0x00000013</span><span class="sxs-lookup"><span data-stu-id="aa6ff-154">0x00000013</span></span>                      |
| <span data-ttu-id="aa6ff-155">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="aa6ff-155">Classes used in</span></span>        | [<span data-ttu-id="aa6ff-156">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="aa6ff-156">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="aa6ff-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="aa6ff-157">Windows Server 2003</span></span>



| <span data-ttu-id="aa6ff-158">Entrée</span><span class="sxs-lookup"><span data-stu-id="aa6ff-158">Entry</span></span> | <span data-ttu-id="aa6ff-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="aa6ff-159">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="aa6ff-160">ID de lien</span><span class="sxs-lookup"><span data-stu-id="aa6ff-160">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="aa6ff-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aa6ff-161">MAPI-Id</span></span>                | <span data-ttu-id="aa6ff-162">0x8156</span><span class="sxs-lookup"><span data-stu-id="aa6ff-162">0x8156</span></span>                          |
| <span data-ttu-id="aa6ff-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="aa6ff-163">System-Only</span></span>            | <span data-ttu-id="aa6ff-164">Vrai</span><span class="sxs-lookup"><span data-stu-id="aa6ff-164">True</span></span>                            |
| <span data-ttu-id="aa6ff-165">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="aa6ff-165">Is-Single-Valued</span></span>       | <span data-ttu-id="aa6ff-166">Vrai</span><span class="sxs-lookup"><span data-stu-id="aa6ff-166">True</span></span>                            |
| <span data-ttu-id="aa6ff-167">Est indexé</span><span class="sxs-lookup"><span data-stu-id="aa6ff-167">Is Indexed</span></span>             | <span data-ttu-id="aa6ff-168">Faux</span><span class="sxs-lookup"><span data-stu-id="aa6ff-168">False</span></span>                           |
| <span data-ttu-id="aa6ff-169">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="aa6ff-169">In Global Catalog</span></span>      | <span data-ttu-id="aa6ff-170">Vrai</span><span class="sxs-lookup"><span data-stu-id="aa6ff-170">True</span></span>                            |
| <span data-ttu-id="aa6ff-171">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="aa6ff-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="aa6ff-172">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="aa6ff-172">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="aa6ff-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aa6ff-173">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="aa6ff-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aa6ff-174">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="aa6ff-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aa6ff-175">Search-Flags</span></span>           | <span data-ttu-id="aa6ff-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="aa6ff-176">0x00000000</span></span>                      |
| <span data-ttu-id="aa6ff-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aa6ff-177">System-Flags</span></span>           | <span data-ttu-id="aa6ff-178">0x00000013</span><span class="sxs-lookup"><span data-stu-id="aa6ff-178">0x00000013</span></span>                      |
| <span data-ttu-id="aa6ff-179">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="aa6ff-179">Classes used in</span></span>        | [<span data-ttu-id="aa6ff-180">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="aa6ff-180">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="aa6ff-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="aa6ff-181">ADAM</span></span>



| <span data-ttu-id="aa6ff-182">Entrée</span><span class="sxs-lookup"><span data-stu-id="aa6ff-182">Entry</span></span> | <span data-ttu-id="aa6ff-183">Valeur</span><span class="sxs-lookup"><span data-stu-id="aa6ff-183">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="aa6ff-184">ID de lien</span><span class="sxs-lookup"><span data-stu-id="aa6ff-184">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="aa6ff-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aa6ff-185">MAPI-Id</span></span>                | <span data-ttu-id="aa6ff-186">0x8156</span><span class="sxs-lookup"><span data-stu-id="aa6ff-186">0x8156</span></span>                          |
| <span data-ttu-id="aa6ff-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="aa6ff-187">System-Only</span></span>            | <span data-ttu-id="aa6ff-188">Vrai</span><span class="sxs-lookup"><span data-stu-id="aa6ff-188">True</span></span>                            |
| <span data-ttu-id="aa6ff-189">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="aa6ff-189">Is-Single-Valued</span></span>       | <span data-ttu-id="aa6ff-190">Vrai</span><span class="sxs-lookup"><span data-stu-id="aa6ff-190">True</span></span>                            |
| <span data-ttu-id="aa6ff-191">Est indexé</span><span class="sxs-lookup"><span data-stu-id="aa6ff-191">Is Indexed</span></span>             | <span data-ttu-id="aa6ff-192">Faux</span><span class="sxs-lookup"><span data-stu-id="aa6ff-192">False</span></span>                           |
| <span data-ttu-id="aa6ff-193">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="aa6ff-193">In Global Catalog</span></span>      | <span data-ttu-id="aa6ff-194">Vrai</span><span class="sxs-lookup"><span data-stu-id="aa6ff-194">True</span></span>                            |
| <span data-ttu-id="aa6ff-195">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="aa6ff-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="aa6ff-196">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="aa6ff-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="aa6ff-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aa6ff-197">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="aa6ff-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aa6ff-198">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="aa6ff-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aa6ff-199">Search-Flags</span></span>           | <span data-ttu-id="aa6ff-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="aa6ff-200">0x00000000</span></span>                      |
| <span data-ttu-id="aa6ff-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aa6ff-201">System-Flags</span></span>           | <span data-ttu-id="aa6ff-202">0x00000013</span><span class="sxs-lookup"><span data-stu-id="aa6ff-202">0x00000013</span></span>                      |
| <span data-ttu-id="aa6ff-203">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="aa6ff-203">Classes used in</span></span>        | [<span data-ttu-id="aa6ff-204">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="aa6ff-204">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="aa6ff-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="aa6ff-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="aa6ff-206">Entrée</span><span class="sxs-lookup"><span data-stu-id="aa6ff-206">Entry</span></span> | <span data-ttu-id="aa6ff-207">Valeur</span><span class="sxs-lookup"><span data-stu-id="aa6ff-207">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="aa6ff-208">ID de lien</span><span class="sxs-lookup"><span data-stu-id="aa6ff-208">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="aa6ff-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aa6ff-209">MAPI-Id</span></span>                | <span data-ttu-id="aa6ff-210">0x8156</span><span class="sxs-lookup"><span data-stu-id="aa6ff-210">0x8156</span></span>                          |
| <span data-ttu-id="aa6ff-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="aa6ff-211">System-Only</span></span>            | <span data-ttu-id="aa6ff-212">Vrai</span><span class="sxs-lookup"><span data-stu-id="aa6ff-212">True</span></span>                            |
| <span data-ttu-id="aa6ff-213">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="aa6ff-213">Is-Single-Valued</span></span>       | <span data-ttu-id="aa6ff-214">Vrai</span><span class="sxs-lookup"><span data-stu-id="aa6ff-214">True</span></span>                            |
| <span data-ttu-id="aa6ff-215">Est indexé</span><span class="sxs-lookup"><span data-stu-id="aa6ff-215">Is Indexed</span></span>             | <span data-ttu-id="aa6ff-216">Faux</span><span class="sxs-lookup"><span data-stu-id="aa6ff-216">False</span></span>                           |
| <span data-ttu-id="aa6ff-217">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="aa6ff-217">In Global Catalog</span></span>      | <span data-ttu-id="aa6ff-218">Vrai</span><span class="sxs-lookup"><span data-stu-id="aa6ff-218">True</span></span>                            |
| <span data-ttu-id="aa6ff-219">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="aa6ff-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="aa6ff-220">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="aa6ff-220">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="aa6ff-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aa6ff-221">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="aa6ff-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aa6ff-222">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="aa6ff-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aa6ff-223">Search-Flags</span></span>           | <span data-ttu-id="aa6ff-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="aa6ff-224">0x00000000</span></span>                      |
| <span data-ttu-id="aa6ff-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aa6ff-225">System-Flags</span></span>           | <span data-ttu-id="aa6ff-226">0x00000013</span><span class="sxs-lookup"><span data-stu-id="aa6ff-226">0x00000013</span></span>                      |
| <span data-ttu-id="aa6ff-227">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="aa6ff-227">Classes used in</span></span>        | [<span data-ttu-id="aa6ff-228">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="aa6ff-228">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="aa6ff-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aa6ff-229">Windows Server 2008</span></span>



| <span data-ttu-id="aa6ff-230">Entrée</span><span class="sxs-lookup"><span data-stu-id="aa6ff-230">Entry</span></span> | <span data-ttu-id="aa6ff-231">Valeur</span><span class="sxs-lookup"><span data-stu-id="aa6ff-231">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="aa6ff-232">ID de lien</span><span class="sxs-lookup"><span data-stu-id="aa6ff-232">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="aa6ff-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aa6ff-233">MAPI-Id</span></span>                | <span data-ttu-id="aa6ff-234">0x8156</span><span class="sxs-lookup"><span data-stu-id="aa6ff-234">0x8156</span></span>                          |
| <span data-ttu-id="aa6ff-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="aa6ff-235">System-Only</span></span>            | <span data-ttu-id="aa6ff-236">Vrai</span><span class="sxs-lookup"><span data-stu-id="aa6ff-236">True</span></span>                            |
| <span data-ttu-id="aa6ff-237">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="aa6ff-237">Is-Single-Valued</span></span>       | <span data-ttu-id="aa6ff-238">Vrai</span><span class="sxs-lookup"><span data-stu-id="aa6ff-238">True</span></span>                            |
| <span data-ttu-id="aa6ff-239">Est indexé</span><span class="sxs-lookup"><span data-stu-id="aa6ff-239">Is Indexed</span></span>             | <span data-ttu-id="aa6ff-240">Faux</span><span class="sxs-lookup"><span data-stu-id="aa6ff-240">False</span></span>                           |
| <span data-ttu-id="aa6ff-241">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="aa6ff-241">In Global Catalog</span></span>      | <span data-ttu-id="aa6ff-242">Vrai</span><span class="sxs-lookup"><span data-stu-id="aa6ff-242">True</span></span>                            |
| <span data-ttu-id="aa6ff-243">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="aa6ff-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="aa6ff-244">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="aa6ff-244">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="aa6ff-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aa6ff-245">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="aa6ff-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aa6ff-246">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="aa6ff-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aa6ff-247">Search-Flags</span></span>           | <span data-ttu-id="aa6ff-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="aa6ff-248">0x00000000</span></span>                      |
| <span data-ttu-id="aa6ff-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aa6ff-249">System-Flags</span></span>           | <span data-ttu-id="aa6ff-250">0x00000013</span><span class="sxs-lookup"><span data-stu-id="aa6ff-250">0x00000013</span></span>                      |
| <span data-ttu-id="aa6ff-251">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="aa6ff-251">Classes used in</span></span>        | [<span data-ttu-id="aa6ff-252">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="aa6ff-252">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="aa6ff-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="aa6ff-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="aa6ff-254">Entrée</span><span class="sxs-lookup"><span data-stu-id="aa6ff-254">Entry</span></span> | <span data-ttu-id="aa6ff-255">Valeur</span><span class="sxs-lookup"><span data-stu-id="aa6ff-255">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="aa6ff-256">ID de lien</span><span class="sxs-lookup"><span data-stu-id="aa6ff-256">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="aa6ff-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aa6ff-257">MAPI-Id</span></span>                | <span data-ttu-id="aa6ff-258">0x8156</span><span class="sxs-lookup"><span data-stu-id="aa6ff-258">0x8156</span></span>                          |
| <span data-ttu-id="aa6ff-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="aa6ff-259">System-Only</span></span>            | <span data-ttu-id="aa6ff-260">Vrai</span><span class="sxs-lookup"><span data-stu-id="aa6ff-260">True</span></span>                            |
| <span data-ttu-id="aa6ff-261">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="aa6ff-261">Is-Single-Valued</span></span>       | <span data-ttu-id="aa6ff-262">Vrai</span><span class="sxs-lookup"><span data-stu-id="aa6ff-262">True</span></span>                            |
| <span data-ttu-id="aa6ff-263">Est indexé</span><span class="sxs-lookup"><span data-stu-id="aa6ff-263">Is Indexed</span></span>             | <span data-ttu-id="aa6ff-264">Faux</span><span class="sxs-lookup"><span data-stu-id="aa6ff-264">False</span></span>                           |
| <span data-ttu-id="aa6ff-265">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="aa6ff-265">In Global Catalog</span></span>      | <span data-ttu-id="aa6ff-266">Vrai</span><span class="sxs-lookup"><span data-stu-id="aa6ff-266">True</span></span>                            |
| <span data-ttu-id="aa6ff-267">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="aa6ff-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="aa6ff-268">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="aa6ff-268">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="aa6ff-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aa6ff-269">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="aa6ff-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aa6ff-270">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="aa6ff-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aa6ff-271">Search-Flags</span></span>           | <span data-ttu-id="aa6ff-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="aa6ff-272">0x00000000</span></span>                      |
| <span data-ttu-id="aa6ff-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aa6ff-273">System-Flags</span></span>           | <span data-ttu-id="aa6ff-274">0x00000013</span><span class="sxs-lookup"><span data-stu-id="aa6ff-274">0x00000013</span></span>                      |
| <span data-ttu-id="aa6ff-275">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="aa6ff-275">Classes used in</span></span>        | [<span data-ttu-id="aa6ff-276">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="aa6ff-276">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="aa6ff-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="aa6ff-277">Windows Server 2012</span></span>



| <span data-ttu-id="aa6ff-278">Entrée</span><span class="sxs-lookup"><span data-stu-id="aa6ff-278">Entry</span></span> | <span data-ttu-id="aa6ff-279">Valeur</span><span class="sxs-lookup"><span data-stu-id="aa6ff-279">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="aa6ff-280">ID de lien</span><span class="sxs-lookup"><span data-stu-id="aa6ff-280">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="aa6ff-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aa6ff-281">MAPI-Id</span></span>                | <span data-ttu-id="aa6ff-282">0x8156</span><span class="sxs-lookup"><span data-stu-id="aa6ff-282">0x8156</span></span>                          |
| <span data-ttu-id="aa6ff-283">System-Only</span><span class="sxs-lookup"><span data-stu-id="aa6ff-283">System-Only</span></span>            | <span data-ttu-id="aa6ff-284">Vrai</span><span class="sxs-lookup"><span data-stu-id="aa6ff-284">True</span></span>                            |
| <span data-ttu-id="aa6ff-285">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="aa6ff-285">Is-Single-Valued</span></span>       | <span data-ttu-id="aa6ff-286">Vrai</span><span class="sxs-lookup"><span data-stu-id="aa6ff-286">True</span></span>                            |
| <span data-ttu-id="aa6ff-287">Est indexé</span><span class="sxs-lookup"><span data-stu-id="aa6ff-287">Is Indexed</span></span>             | <span data-ttu-id="aa6ff-288">Faux</span><span class="sxs-lookup"><span data-stu-id="aa6ff-288">False</span></span>                           |
| <span data-ttu-id="aa6ff-289">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="aa6ff-289">In Global Catalog</span></span>      | <span data-ttu-id="aa6ff-290">Vrai</span><span class="sxs-lookup"><span data-stu-id="aa6ff-290">True</span></span>                            |
| <span data-ttu-id="aa6ff-291">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="aa6ff-291">NT-Security-Descriptor</span></span> | <span data-ttu-id="aa6ff-292">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="aa6ff-292">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="aa6ff-293">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aa6ff-293">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="aa6ff-294">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aa6ff-294">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="aa6ff-295">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aa6ff-295">Search-Flags</span></span>           | <span data-ttu-id="aa6ff-296">0x00000000</span><span class="sxs-lookup"><span data-stu-id="aa6ff-296">0x00000000</span></span>                      |
| <span data-ttu-id="aa6ff-297">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aa6ff-297">System-Flags</span></span>           | <span data-ttu-id="aa6ff-298">0x00000013</span><span class="sxs-lookup"><span data-stu-id="aa6ff-298">0x00000013</span></span>                      |
| <span data-ttu-id="aa6ff-299">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="aa6ff-299">Classes used in</span></span>        | [<span data-ttu-id="aa6ff-300">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="aa6ff-300">**Top**</span></span>](c-top.md)<br/> |



## <a name="see-also"></a><span data-ttu-id="aa6ff-301">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aa6ff-301">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa6ff-302">**USN-DSA-Last-obj-supprimé**</span><span class="sxs-lookup"><span data-stu-id="aa6ff-302">**USN-DSA-Last-Obj-Removed**</span></span>](a-usndsalastobjremoved.md)
</dt> </dl>

 

 





