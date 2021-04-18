---
title: Attribut de limite de niveau FRS
description: Limitez la profondeur de l’arborescence de répertoires à répliquer pour la réplication de fichiers.
ms.assetid: e2916cbd-1ce7-4ff7-82a2-5fbdae3c6a1b
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory au niveau de la limite de niveau FRS
- Schéma AD de l’attribut fRSLevelLimit
topic_type:
- apiref
api_name:
- FRS-Level-Limit
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c587565eb10014ef638a2320dd9229d8409ba06
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106516112"
---
# <a name="frs-level-limit-attribute"></a><span data-ttu-id="3e228-105">Attribut de limite de niveau FRS</span><span class="sxs-lookup"><span data-stu-id="3e228-105">FRS-Level-Limit attribute</span></span>

<span data-ttu-id="3e228-106">Limitez la profondeur de l’arborescence de répertoires à répliquer pour la réplication de fichiers.</span><span class="sxs-lookup"><span data-stu-id="3e228-106">Limit depth of directory tree to replicate for file replication.</span></span>



| <span data-ttu-id="3e228-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="3e228-107">Entry</span></span> | <span data-ttu-id="3e228-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="3e228-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="3e228-109">CN</span><span class="sxs-lookup"><span data-stu-id="3e228-109">CN</span></span>                | <span data-ttu-id="3e228-110">Limite de niveau de service FRS</span><span class="sxs-lookup"><span data-stu-id="3e228-110">FRS-Level-Limit</span></span>                      |
| <span data-ttu-id="3e228-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="3e228-111">Ldap-Display-Name</span></span> | <span data-ttu-id="3e228-112">fRSLevelLimit</span><span class="sxs-lookup"><span data-stu-id="3e228-112">fRSLevelLimit</span></span>                        |
| <span data-ttu-id="3e228-113">Taille</span><span class="sxs-lookup"><span data-stu-id="3e228-113">Size</span></span>              | <span data-ttu-id="3e228-114">4 octets</span><span class="sxs-lookup"><span data-stu-id="3e228-114">4 bytes</span></span>                              |
| <span data-ttu-id="3e228-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="3e228-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="3e228-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="3e228-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="3e228-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="3e228-117">Attribute-Id</span></span>      | <span data-ttu-id="3e228-118">1.2.840.113556.1.4.534</span><span class="sxs-lookup"><span data-stu-id="3e228-118">1.2.840.113556.1.4.534</span></span>               |
| <span data-ttu-id="3e228-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="3e228-119">System-Id-Guid</span></span>    | <span data-ttu-id="3e228-120">5245801e-ca6a-11d0-afff-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="3e228-120">5245801e-ca6a-11d0-afff-0000f80367c1</span></span> |
| <span data-ttu-id="3e228-121">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3e228-121">Syntax</span></span>            | [<span data-ttu-id="3e228-122">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="3e228-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="3e228-123">Implémentations</span><span class="sxs-lookup"><span data-stu-id="3e228-123">Implementations</span></span>

-   [<span data-ttu-id="3e228-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="3e228-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="3e228-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="3e228-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="3e228-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="3e228-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="3e228-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="3e228-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="3e228-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="3e228-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="3e228-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3e228-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="3e228-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3e228-130">Windows 2000 Server</span></span>



| <span data-ttu-id="3e228-131">Entrée</span><span class="sxs-lookup"><span data-stu-id="3e228-131">Entry</span></span> | <span data-ttu-id="3e228-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="3e228-132">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="3e228-133">ID de lien</span><span class="sxs-lookup"><span data-stu-id="3e228-133">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="3e228-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3e228-134">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="3e228-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="3e228-135">System-Only</span></span>            | <span data-ttu-id="3e228-136">Faux</span><span class="sxs-lookup"><span data-stu-id="3e228-136">False</span></span>                                                     |
| <span data-ttu-id="3e228-137">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="3e228-137">Is-Single-Valued</span></span>       | <span data-ttu-id="3e228-138">Vrai</span><span class="sxs-lookup"><span data-stu-id="3e228-138">True</span></span>                                                      |
| <span data-ttu-id="3e228-139">Est indexé</span><span class="sxs-lookup"><span data-stu-id="3e228-139">Is Indexed</span></span>             | <span data-ttu-id="3e228-140">Faux</span><span class="sxs-lookup"><span data-stu-id="3e228-140">False</span></span>                                                     |
| <span data-ttu-id="3e228-141">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="3e228-141">In Global Catalog</span></span>      | <span data-ttu-id="3e228-142">Faux</span><span class="sxs-lookup"><span data-stu-id="3e228-142">False</span></span>                                                     |
| <span data-ttu-id="3e228-143">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="3e228-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="3e228-144">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="3e228-144">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="3e228-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3e228-145">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="3e228-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3e228-146">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="3e228-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3e228-147">Search-Flags</span></span>           | <span data-ttu-id="3e228-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3e228-148">0x00000000</span></span>                                                |
| <span data-ttu-id="3e228-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3e228-149">System-Flags</span></span>           | <span data-ttu-id="3e228-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3e228-150">0x00000010</span></span>                                                |
| <span data-ttu-id="3e228-151">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="3e228-151">Classes used in</span></span>        | [<span data-ttu-id="3e228-152">**NTFRS-jeu de réplicas**</span><span class="sxs-lookup"><span data-stu-id="3e228-152">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="3e228-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3e228-153">Windows Server 2003</span></span>



| <span data-ttu-id="3e228-154">Entrée</span><span class="sxs-lookup"><span data-stu-id="3e228-154">Entry</span></span> | <span data-ttu-id="3e228-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="3e228-155">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="3e228-156">ID de lien</span><span class="sxs-lookup"><span data-stu-id="3e228-156">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="3e228-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3e228-157">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="3e228-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="3e228-158">System-Only</span></span>            | <span data-ttu-id="3e228-159">Faux</span><span class="sxs-lookup"><span data-stu-id="3e228-159">False</span></span>                                                     |
| <span data-ttu-id="3e228-160">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="3e228-160">Is-Single-Valued</span></span>       | <span data-ttu-id="3e228-161">Vrai</span><span class="sxs-lookup"><span data-stu-id="3e228-161">True</span></span>                                                      |
| <span data-ttu-id="3e228-162">Est indexé</span><span class="sxs-lookup"><span data-stu-id="3e228-162">Is Indexed</span></span>             | <span data-ttu-id="3e228-163">Faux</span><span class="sxs-lookup"><span data-stu-id="3e228-163">False</span></span>                                                     |
| <span data-ttu-id="3e228-164">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="3e228-164">In Global Catalog</span></span>      | <span data-ttu-id="3e228-165">Faux</span><span class="sxs-lookup"><span data-stu-id="3e228-165">False</span></span>                                                     |
| <span data-ttu-id="3e228-166">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="3e228-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="3e228-167">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="3e228-167">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="3e228-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3e228-168">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="3e228-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3e228-169">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="3e228-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3e228-170">Search-Flags</span></span>           | <span data-ttu-id="3e228-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3e228-171">0x00000000</span></span>                                                |
| <span data-ttu-id="3e228-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3e228-172">System-Flags</span></span>           | <span data-ttu-id="3e228-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3e228-173">0x00000010</span></span>                                                |
| <span data-ttu-id="3e228-174">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="3e228-174">Classes used in</span></span>        | [<span data-ttu-id="3e228-175">**NTFRS-jeu de réplicas**</span><span class="sxs-lookup"><span data-stu-id="3e228-175">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="3e228-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="3e228-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="3e228-177">Entrée</span><span class="sxs-lookup"><span data-stu-id="3e228-177">Entry</span></span> | <span data-ttu-id="3e228-178">Valeur</span><span class="sxs-lookup"><span data-stu-id="3e228-178">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="3e228-179">ID de lien</span><span class="sxs-lookup"><span data-stu-id="3e228-179">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="3e228-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3e228-180">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="3e228-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="3e228-181">System-Only</span></span>            | <span data-ttu-id="3e228-182">Faux</span><span class="sxs-lookup"><span data-stu-id="3e228-182">False</span></span>                                                     |
| <span data-ttu-id="3e228-183">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="3e228-183">Is-Single-Valued</span></span>       | <span data-ttu-id="3e228-184">Vrai</span><span class="sxs-lookup"><span data-stu-id="3e228-184">True</span></span>                                                      |
| <span data-ttu-id="3e228-185">Est indexé</span><span class="sxs-lookup"><span data-stu-id="3e228-185">Is Indexed</span></span>             | <span data-ttu-id="3e228-186">Faux</span><span class="sxs-lookup"><span data-stu-id="3e228-186">False</span></span>                                                     |
| <span data-ttu-id="3e228-187">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="3e228-187">In Global Catalog</span></span>      | <span data-ttu-id="3e228-188">Faux</span><span class="sxs-lookup"><span data-stu-id="3e228-188">False</span></span>                                                     |
| <span data-ttu-id="3e228-189">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="3e228-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="3e228-190">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="3e228-190">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="3e228-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3e228-191">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="3e228-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3e228-192">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="3e228-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3e228-193">Search-Flags</span></span>           | <span data-ttu-id="3e228-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3e228-194">0x00000000</span></span>                                                |
| <span data-ttu-id="3e228-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3e228-195">System-Flags</span></span>           | <span data-ttu-id="3e228-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3e228-196">0x00000010</span></span>                                                |
| <span data-ttu-id="3e228-197">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="3e228-197">Classes used in</span></span>        | [<span data-ttu-id="3e228-198">**NTFRS-jeu de réplicas**</span><span class="sxs-lookup"><span data-stu-id="3e228-198">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="3e228-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3e228-199">Windows Server 2008</span></span>



| <span data-ttu-id="3e228-200">Entrée</span><span class="sxs-lookup"><span data-stu-id="3e228-200">Entry</span></span> | <span data-ttu-id="3e228-201">Valeur</span><span class="sxs-lookup"><span data-stu-id="3e228-201">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="3e228-202">ID de lien</span><span class="sxs-lookup"><span data-stu-id="3e228-202">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="3e228-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3e228-203">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="3e228-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="3e228-204">System-Only</span></span>            | <span data-ttu-id="3e228-205">Faux</span><span class="sxs-lookup"><span data-stu-id="3e228-205">False</span></span>                                                     |
| <span data-ttu-id="3e228-206">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="3e228-206">Is-Single-Valued</span></span>       | <span data-ttu-id="3e228-207">Vrai</span><span class="sxs-lookup"><span data-stu-id="3e228-207">True</span></span>                                                      |
| <span data-ttu-id="3e228-208">Est indexé</span><span class="sxs-lookup"><span data-stu-id="3e228-208">Is Indexed</span></span>             | <span data-ttu-id="3e228-209">Faux</span><span class="sxs-lookup"><span data-stu-id="3e228-209">False</span></span>                                                     |
| <span data-ttu-id="3e228-210">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="3e228-210">In Global Catalog</span></span>      | <span data-ttu-id="3e228-211">Faux</span><span class="sxs-lookup"><span data-stu-id="3e228-211">False</span></span>                                                     |
| <span data-ttu-id="3e228-212">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="3e228-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="3e228-213">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="3e228-213">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="3e228-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3e228-214">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="3e228-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3e228-215">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="3e228-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3e228-216">Search-Flags</span></span>           | <span data-ttu-id="3e228-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3e228-217">0x00000000</span></span>                                                |
| <span data-ttu-id="3e228-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3e228-218">System-Flags</span></span>           | <span data-ttu-id="3e228-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3e228-219">0x00000010</span></span>                                                |
| <span data-ttu-id="3e228-220">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="3e228-220">Classes used in</span></span>        | [<span data-ttu-id="3e228-221">**NTFRS-jeu de réplicas**</span><span class="sxs-lookup"><span data-stu-id="3e228-221">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="3e228-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3e228-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="3e228-223">Entrée</span><span class="sxs-lookup"><span data-stu-id="3e228-223">Entry</span></span> | <span data-ttu-id="3e228-224">Valeur</span><span class="sxs-lookup"><span data-stu-id="3e228-224">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="3e228-225">ID de lien</span><span class="sxs-lookup"><span data-stu-id="3e228-225">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="3e228-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3e228-226">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="3e228-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="3e228-227">System-Only</span></span>            | <span data-ttu-id="3e228-228">Faux</span><span class="sxs-lookup"><span data-stu-id="3e228-228">False</span></span>                                                     |
| <span data-ttu-id="3e228-229">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="3e228-229">Is-Single-Valued</span></span>       | <span data-ttu-id="3e228-230">Vrai</span><span class="sxs-lookup"><span data-stu-id="3e228-230">True</span></span>                                                      |
| <span data-ttu-id="3e228-231">Est indexé</span><span class="sxs-lookup"><span data-stu-id="3e228-231">Is Indexed</span></span>             | <span data-ttu-id="3e228-232">Faux</span><span class="sxs-lookup"><span data-stu-id="3e228-232">False</span></span>                                                     |
| <span data-ttu-id="3e228-233">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="3e228-233">In Global Catalog</span></span>      | <span data-ttu-id="3e228-234">Faux</span><span class="sxs-lookup"><span data-stu-id="3e228-234">False</span></span>                                                     |
| <span data-ttu-id="3e228-235">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="3e228-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="3e228-236">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="3e228-236">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="3e228-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3e228-237">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="3e228-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3e228-238">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="3e228-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3e228-239">Search-Flags</span></span>           | <span data-ttu-id="3e228-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3e228-240">0x00000000</span></span>                                                |
| <span data-ttu-id="3e228-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3e228-241">System-Flags</span></span>           | <span data-ttu-id="3e228-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3e228-242">0x00000010</span></span>                                                |
| <span data-ttu-id="3e228-243">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="3e228-243">Classes used in</span></span>        | [<span data-ttu-id="3e228-244">**NTFRS-jeu de réplicas**</span><span class="sxs-lookup"><span data-stu-id="3e228-244">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="3e228-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3e228-245">Windows Server 2012</span></span>



| <span data-ttu-id="3e228-246">Entrée</span><span class="sxs-lookup"><span data-stu-id="3e228-246">Entry</span></span> | <span data-ttu-id="3e228-247">Valeur</span><span class="sxs-lookup"><span data-stu-id="3e228-247">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="3e228-248">ID de lien</span><span class="sxs-lookup"><span data-stu-id="3e228-248">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="3e228-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3e228-249">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="3e228-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="3e228-250">System-Only</span></span>            | <span data-ttu-id="3e228-251">Faux</span><span class="sxs-lookup"><span data-stu-id="3e228-251">False</span></span>                                                     |
| <span data-ttu-id="3e228-252">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="3e228-252">Is-Single-Valued</span></span>       | <span data-ttu-id="3e228-253">Vrai</span><span class="sxs-lookup"><span data-stu-id="3e228-253">True</span></span>                                                      |
| <span data-ttu-id="3e228-254">Est indexé</span><span class="sxs-lookup"><span data-stu-id="3e228-254">Is Indexed</span></span>             | <span data-ttu-id="3e228-255">Faux</span><span class="sxs-lookup"><span data-stu-id="3e228-255">False</span></span>                                                     |
| <span data-ttu-id="3e228-256">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="3e228-256">In Global Catalog</span></span>      | <span data-ttu-id="3e228-257">Faux</span><span class="sxs-lookup"><span data-stu-id="3e228-257">False</span></span>                                                     |
| <span data-ttu-id="3e228-258">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="3e228-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="3e228-259">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="3e228-259">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="3e228-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3e228-260">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="3e228-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3e228-261">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="3e228-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3e228-262">Search-Flags</span></span>           | <span data-ttu-id="3e228-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3e228-263">0x00000000</span></span>                                                |
| <span data-ttu-id="3e228-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3e228-264">System-Flags</span></span>           | <span data-ttu-id="3e228-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3e228-265">0x00000010</span></span>                                                |
| <span data-ttu-id="3e228-266">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="3e228-266">Classes used in</span></span>        | [<span data-ttu-id="3e228-267">**NTFRS-jeu de réplicas**</span><span class="sxs-lookup"><span data-stu-id="3e228-267">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



 

 





