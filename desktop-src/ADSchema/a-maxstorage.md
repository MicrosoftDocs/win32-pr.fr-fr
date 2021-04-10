---
title: Attribut Max-Storage
description: Quantité maximale d’espace disque que l’utilisateur peut utiliser. Utilisez la valeur spécifiée dans USER \_ MAXSTORAGE \_ Unlimited pour utiliser tout l’espace disque disponible.
ms.assetid: 69302641-ecfc-4b0f-81f8-f69b48c6faa7
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Max-Storage
- Schéma AD de l’attribut maxStorage
topic_type:
- apiref
api_name:
- Max-Storage
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac6caff3f85de7073818096324445b63a3c1c9be
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845222"
---
# <a name="max-storage-attribute"></a><span data-ttu-id="e748f-106">Attribut Max-Storage</span><span class="sxs-lookup"><span data-stu-id="e748f-106">Max-Storage attribute</span></span>

<span data-ttu-id="e748f-107">Quantité maximale d’espace disque que l’utilisateur peut utiliser.</span><span class="sxs-lookup"><span data-stu-id="e748f-107">The maximum amount of disk space the user can use.</span></span> <span data-ttu-id="e748f-108">Utilisez la valeur spécifiée dans USER \_ MAXSTORAGE \_ Unlimited pour utiliser tout l’espace disque disponible.</span><span class="sxs-lookup"><span data-stu-id="e748f-108">Use the value specified in USER\_MAXSTORAGE\_UNLIMITED to use all available disk space.</span></span>



| <span data-ttu-id="e748f-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="e748f-109">Entry</span></span> | <span data-ttu-id="e748f-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="e748f-110">Value</span></span> |
|-------------------|------------------------------------------------------------|
| <span data-ttu-id="e748f-111">CN</span><span class="sxs-lookup"><span data-stu-id="e748f-111">CN</span></span>                | <span data-ttu-id="e748f-112">Max-Storage</span><span class="sxs-lookup"><span data-stu-id="e748f-112">Max-Storage</span></span>                                                |
| <span data-ttu-id="e748f-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="e748f-113">Ldap-Display-Name</span></span> | <span data-ttu-id="e748f-114">maxStorage</span><span class="sxs-lookup"><span data-stu-id="e748f-114">maxStorage</span></span>                                                 |
| <span data-ttu-id="e748f-115">Taille</span><span class="sxs-lookup"><span data-stu-id="e748f-115">Size</span></span>              | <span data-ttu-id="e748f-116">8 octets : USER \_ MAXSTORAGE \_ Unlimited ((unsigned long)-1L)</span><span class="sxs-lookup"><span data-stu-id="e748f-116">8 bytes: USER\_MAXSTORAGE\_UNLIMITED ((unsigned long) -1L)</span></span> |
| <span data-ttu-id="e748f-117">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="e748f-117">Update Privilege</span></span>  | <span data-ttu-id="e748f-118">Administrateur de domaine</span><span class="sxs-lookup"><span data-stu-id="e748f-118">Domain administrator</span></span>                                       |
| <span data-ttu-id="e748f-119">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="e748f-119">Update Frequency</span></span>  | <span data-ttu-id="e748f-120">Chaque fois que le quota de disque doit être modifié.</span><span class="sxs-lookup"><span data-stu-id="e748f-120">Whenever the disk quota needs to change.</span></span>                   |
| <span data-ttu-id="e748f-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e748f-121">Attribute-Id</span></span>      | <span data-ttu-id="e748f-122">1.2.840.113556.1.4.76</span><span class="sxs-lookup"><span data-stu-id="e748f-122">1.2.840.113556.1.4.76</span></span>                                      |
| <span data-ttu-id="e748f-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="e748f-123">System-Id-Guid</span></span>    | <span data-ttu-id="e748f-124">bf9679bd-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="e748f-124">bf9679bd-0de6-11d0-a285-00aa003049e2</span></span>                       |
| <span data-ttu-id="e748f-125">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e748f-125">Syntax</span></span>            | [<span data-ttu-id="e748f-126">**Défini**</span><span class="sxs-lookup"><span data-stu-id="e748f-126">**Interval**</span></span>](s-interval.md)                             |



## <a name="implementations"></a><span data-ttu-id="e748f-127">Implémentations</span><span class="sxs-lookup"><span data-stu-id="e748f-127">Implementations</span></span>

-   [<span data-ttu-id="e748f-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e748f-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e748f-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e748f-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e748f-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e748f-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e748f-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e748f-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e748f-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e748f-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e748f-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e748f-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e748f-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e748f-134">Windows 2000 Server</span></span>



| <span data-ttu-id="e748f-135">Entrée</span><span class="sxs-lookup"><span data-stu-id="e748f-135">Entry</span></span> | <span data-ttu-id="e748f-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="e748f-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e748f-137">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e748f-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e748f-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e748f-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e748f-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="e748f-139">System-Only</span></span>            | <span data-ttu-id="e748f-140">Faux</span><span class="sxs-lookup"><span data-stu-id="e748f-140">False</span></span>                             |
| <span data-ttu-id="e748f-141">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e748f-141">Is-Single-Valued</span></span>       | <span data-ttu-id="e748f-142">Vrai</span><span class="sxs-lookup"><span data-stu-id="e748f-142">True</span></span>                              |
| <span data-ttu-id="e748f-143">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e748f-143">Is Indexed</span></span>             | <span data-ttu-id="e748f-144">Faux</span><span class="sxs-lookup"><span data-stu-id="e748f-144">False</span></span>                             |
| <span data-ttu-id="e748f-145">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e748f-145">In Global Catalog</span></span>      | <span data-ttu-id="e748f-146">Faux</span><span class="sxs-lookup"><span data-stu-id="e748f-146">False</span></span>                             |
| <span data-ttu-id="e748f-147">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e748f-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="e748f-148">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e748f-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e748f-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e748f-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="e748f-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e748f-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="e748f-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e748f-151">Search-Flags</span></span>           | <span data-ttu-id="e748f-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e748f-152">0x00000010</span></span>                        |
| <span data-ttu-id="e748f-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e748f-153">System-Flags</span></span>           | <span data-ttu-id="e748f-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e748f-154">0x00000010</span></span>                        |
| <span data-ttu-id="e748f-155">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e748f-155">Classes used in</span></span>        | [<span data-ttu-id="e748f-156">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="e748f-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e748f-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e748f-157">Windows Server 2003</span></span>



| <span data-ttu-id="e748f-158">Entrée</span><span class="sxs-lookup"><span data-stu-id="e748f-158">Entry</span></span> | <span data-ttu-id="e748f-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="e748f-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e748f-160">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e748f-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e748f-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e748f-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e748f-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="e748f-162">System-Only</span></span>            | <span data-ttu-id="e748f-163">Faux</span><span class="sxs-lookup"><span data-stu-id="e748f-163">False</span></span>                             |
| <span data-ttu-id="e748f-164">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e748f-164">Is-Single-Valued</span></span>       | <span data-ttu-id="e748f-165">Vrai</span><span class="sxs-lookup"><span data-stu-id="e748f-165">True</span></span>                              |
| <span data-ttu-id="e748f-166">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e748f-166">Is Indexed</span></span>             | <span data-ttu-id="e748f-167">Faux</span><span class="sxs-lookup"><span data-stu-id="e748f-167">False</span></span>                             |
| <span data-ttu-id="e748f-168">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e748f-168">In Global Catalog</span></span>      | <span data-ttu-id="e748f-169">Faux</span><span class="sxs-lookup"><span data-stu-id="e748f-169">False</span></span>                             |
| <span data-ttu-id="e748f-170">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e748f-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="e748f-171">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e748f-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e748f-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e748f-172">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="e748f-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e748f-173">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="e748f-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e748f-174">Search-Flags</span></span>           | <span data-ttu-id="e748f-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e748f-175">0x00000010</span></span>                        |
| <span data-ttu-id="e748f-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e748f-176">System-Flags</span></span>           | <span data-ttu-id="e748f-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e748f-177">0x00000010</span></span>                        |
| <span data-ttu-id="e748f-178">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e748f-178">Classes used in</span></span>        | [<span data-ttu-id="e748f-179">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="e748f-179">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e748f-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e748f-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e748f-181">Entrée</span><span class="sxs-lookup"><span data-stu-id="e748f-181">Entry</span></span> | <span data-ttu-id="e748f-182">Valeur</span><span class="sxs-lookup"><span data-stu-id="e748f-182">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e748f-183">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e748f-183">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e748f-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e748f-184">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e748f-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="e748f-185">System-Only</span></span>            | <span data-ttu-id="e748f-186">Faux</span><span class="sxs-lookup"><span data-stu-id="e748f-186">False</span></span>                             |
| <span data-ttu-id="e748f-187">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e748f-187">Is-Single-Valued</span></span>       | <span data-ttu-id="e748f-188">Vrai</span><span class="sxs-lookup"><span data-stu-id="e748f-188">True</span></span>                              |
| <span data-ttu-id="e748f-189">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e748f-189">Is Indexed</span></span>             | <span data-ttu-id="e748f-190">Faux</span><span class="sxs-lookup"><span data-stu-id="e748f-190">False</span></span>                             |
| <span data-ttu-id="e748f-191">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e748f-191">In Global Catalog</span></span>      | <span data-ttu-id="e748f-192">Faux</span><span class="sxs-lookup"><span data-stu-id="e748f-192">False</span></span>                             |
| <span data-ttu-id="e748f-193">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e748f-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="e748f-194">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e748f-194">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e748f-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e748f-195">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="e748f-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e748f-196">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="e748f-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e748f-197">Search-Flags</span></span>           | <span data-ttu-id="e748f-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e748f-198">0x00000010</span></span>                        |
| <span data-ttu-id="e748f-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e748f-199">System-Flags</span></span>           | <span data-ttu-id="e748f-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e748f-200">0x00000010</span></span>                        |
| <span data-ttu-id="e748f-201">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e748f-201">Classes used in</span></span>        | [<span data-ttu-id="e748f-202">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="e748f-202">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e748f-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e748f-203">Windows Server 2008</span></span>



| <span data-ttu-id="e748f-204">Entrée</span><span class="sxs-lookup"><span data-stu-id="e748f-204">Entry</span></span> | <span data-ttu-id="e748f-205">Valeur</span><span class="sxs-lookup"><span data-stu-id="e748f-205">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e748f-206">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e748f-206">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e748f-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e748f-207">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e748f-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="e748f-208">System-Only</span></span>            | <span data-ttu-id="e748f-209">Faux</span><span class="sxs-lookup"><span data-stu-id="e748f-209">False</span></span>                             |
| <span data-ttu-id="e748f-210">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e748f-210">Is-Single-Valued</span></span>       | <span data-ttu-id="e748f-211">Vrai</span><span class="sxs-lookup"><span data-stu-id="e748f-211">True</span></span>                              |
| <span data-ttu-id="e748f-212">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e748f-212">Is Indexed</span></span>             | <span data-ttu-id="e748f-213">Faux</span><span class="sxs-lookup"><span data-stu-id="e748f-213">False</span></span>                             |
| <span data-ttu-id="e748f-214">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e748f-214">In Global Catalog</span></span>      | <span data-ttu-id="e748f-215">Faux</span><span class="sxs-lookup"><span data-stu-id="e748f-215">False</span></span>                             |
| <span data-ttu-id="e748f-216">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e748f-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="e748f-217">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e748f-217">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e748f-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e748f-218">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="e748f-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e748f-219">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="e748f-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e748f-220">Search-Flags</span></span>           | <span data-ttu-id="e748f-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e748f-221">0x00000010</span></span>                        |
| <span data-ttu-id="e748f-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e748f-222">System-Flags</span></span>           | <span data-ttu-id="e748f-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e748f-223">0x00000010</span></span>                        |
| <span data-ttu-id="e748f-224">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e748f-224">Classes used in</span></span>        | [<span data-ttu-id="e748f-225">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="e748f-225">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e748f-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e748f-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e748f-227">Entrée</span><span class="sxs-lookup"><span data-stu-id="e748f-227">Entry</span></span> | <span data-ttu-id="e748f-228">Valeur</span><span class="sxs-lookup"><span data-stu-id="e748f-228">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e748f-229">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e748f-229">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e748f-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e748f-230">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e748f-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="e748f-231">System-Only</span></span>            | <span data-ttu-id="e748f-232">Faux</span><span class="sxs-lookup"><span data-stu-id="e748f-232">False</span></span>                             |
| <span data-ttu-id="e748f-233">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e748f-233">Is-Single-Valued</span></span>       | <span data-ttu-id="e748f-234">Vrai</span><span class="sxs-lookup"><span data-stu-id="e748f-234">True</span></span>                              |
| <span data-ttu-id="e748f-235">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e748f-235">Is Indexed</span></span>             | <span data-ttu-id="e748f-236">Faux</span><span class="sxs-lookup"><span data-stu-id="e748f-236">False</span></span>                             |
| <span data-ttu-id="e748f-237">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e748f-237">In Global Catalog</span></span>      | <span data-ttu-id="e748f-238">Faux</span><span class="sxs-lookup"><span data-stu-id="e748f-238">False</span></span>                             |
| <span data-ttu-id="e748f-239">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e748f-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="e748f-240">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e748f-240">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e748f-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e748f-241">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="e748f-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e748f-242">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="e748f-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e748f-243">Search-Flags</span></span>           | <span data-ttu-id="e748f-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e748f-244">0x00000010</span></span>                        |
| <span data-ttu-id="e748f-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e748f-245">System-Flags</span></span>           | <span data-ttu-id="e748f-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e748f-246">0x00000010</span></span>                        |
| <span data-ttu-id="e748f-247">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e748f-247">Classes used in</span></span>        | [<span data-ttu-id="e748f-248">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="e748f-248">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e748f-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e748f-249">Windows Server 2012</span></span>



| <span data-ttu-id="e748f-250">Entrée</span><span class="sxs-lookup"><span data-stu-id="e748f-250">Entry</span></span> | <span data-ttu-id="e748f-251">Valeur</span><span class="sxs-lookup"><span data-stu-id="e748f-251">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e748f-252">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e748f-252">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e748f-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e748f-253">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e748f-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="e748f-254">System-Only</span></span>            | <span data-ttu-id="e748f-255">Faux</span><span class="sxs-lookup"><span data-stu-id="e748f-255">False</span></span>                             |
| <span data-ttu-id="e748f-256">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e748f-256">Is-Single-Valued</span></span>       | <span data-ttu-id="e748f-257">Vrai</span><span class="sxs-lookup"><span data-stu-id="e748f-257">True</span></span>                              |
| <span data-ttu-id="e748f-258">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e748f-258">Is Indexed</span></span>             | <span data-ttu-id="e748f-259">Faux</span><span class="sxs-lookup"><span data-stu-id="e748f-259">False</span></span>                             |
| <span data-ttu-id="e748f-260">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e748f-260">In Global Catalog</span></span>      | <span data-ttu-id="e748f-261">Faux</span><span class="sxs-lookup"><span data-stu-id="e748f-261">False</span></span>                             |
| <span data-ttu-id="e748f-262">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e748f-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="e748f-263">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e748f-263">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e748f-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e748f-264">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="e748f-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e748f-265">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="e748f-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e748f-266">Search-Flags</span></span>           | <span data-ttu-id="e748f-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e748f-267">0x00000010</span></span>                        |
| <span data-ttu-id="e748f-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e748f-268">System-Flags</span></span>           | <span data-ttu-id="e748f-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e748f-269">0x00000010</span></span>                        |
| <span data-ttu-id="e748f-270">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e748f-270">Classes used in</span></span>        | [<span data-ttu-id="e748f-271">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="e748f-271">**User**</span></span>](c-user.md)<br/> |



 

 





