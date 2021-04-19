---
title: Attribut de filtre de fichier FRS
description: Liste des extensions de nom de fichier exclues de la réplication de fichiers.
ms.assetid: 094a393a-9e1a-4da8-a38a-161102f164fd
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut de filtre de fichier FRS
- Schéma AD de l’attribut fRSFileFilter
topic_type:
- apiref
api_name:
- FRS-File-Filter
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 234cf7d6e56e84c2ed9578fc56036e581a2f0ad2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106514460"
---
# <a name="frs-file-filter-attribute"></a><span data-ttu-id="bc22f-105">Attribut de filtre de fichier FRS</span><span class="sxs-lookup"><span data-stu-id="bc22f-105">FRS-File-Filter attribute</span></span>

<span data-ttu-id="bc22f-106">Liste des extensions de nom de fichier exclues de la réplication de fichiers.</span><span class="sxs-lookup"><span data-stu-id="bc22f-106">A list of file name extensions excluded from file replication.</span></span>



| <span data-ttu-id="bc22f-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="bc22f-107">Entry</span></span> | <span data-ttu-id="bc22f-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="bc22f-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="bc22f-109">CN</span><span class="sxs-lookup"><span data-stu-id="bc22f-109">CN</span></span>                | <span data-ttu-id="bc22f-110">Fichier FRS-filtre de fichiers</span><span class="sxs-lookup"><span data-stu-id="bc22f-110">FRS-File-Filter</span></span>                             |
| <span data-ttu-id="bc22f-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="bc22f-111">Ldap-Display-Name</span></span> | <span data-ttu-id="bc22f-112">fRSFileFilter</span><span class="sxs-lookup"><span data-stu-id="bc22f-112">fRSFileFilter</span></span>                               |
| <span data-ttu-id="bc22f-113">Taille</span><span class="sxs-lookup"><span data-stu-id="bc22f-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="bc22f-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="bc22f-114">Update Privilege</span></span>  | <span data-ttu-id="bc22f-115">Administrateur de domaine</span><span class="sxs-lookup"><span data-stu-id="bc22f-115">Domain administrator</span></span>                        |
| <span data-ttu-id="bc22f-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="bc22f-116">Update Frequency</span></span>  | <span data-ttu-id="bc22f-117">Lorsque la réplication est configurée.</span><span class="sxs-lookup"><span data-stu-id="bc22f-117">When replication is setup.</span></span>                  |
| <span data-ttu-id="bc22f-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="bc22f-118">Attribute-Id</span></span>      | <span data-ttu-id="bc22f-119">1.2.840.113556.1.4.483</span><span class="sxs-lookup"><span data-stu-id="bc22f-119">1.2.840.113556.1.4.483</span></span>                      |
| <span data-ttu-id="bc22f-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="bc22f-120">System-Id-Guid</span></span>    | <span data-ttu-id="bc22f-121">1be8f170-a9ff-11d0-afe2-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="bc22f-121">1be8f170-a9ff-11d0-afe2-00c04fd930c9</span></span>        |
| <span data-ttu-id="bc22f-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bc22f-122">Syntax</span></span>            | [<span data-ttu-id="bc22f-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="bc22f-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="bc22f-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="bc22f-124">Implementations</span></span>

-   [<span data-ttu-id="bc22f-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="bc22f-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="bc22f-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="bc22f-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="bc22f-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="bc22f-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="bc22f-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="bc22f-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="bc22f-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="bc22f-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="bc22f-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="bc22f-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="bc22f-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bc22f-131">Windows 2000 Server</span></span>



| <span data-ttu-id="bc22f-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="bc22f-132">Entry</span></span> | <span data-ttu-id="bc22f-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="bc22f-133">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="bc22f-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="bc22f-134">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="bc22f-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bc22f-135">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="bc22f-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="bc22f-136">System-Only</span></span>            | <span data-ttu-id="bc22f-137">Faux</span><span class="sxs-lookup"><span data-stu-id="bc22f-137">False</span></span>                                                     |
| <span data-ttu-id="bc22f-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="bc22f-138">Is-Single-Valued</span></span>       | <span data-ttu-id="bc22f-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="bc22f-139">True</span></span>                                                      |
| <span data-ttu-id="bc22f-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="bc22f-140">Is Indexed</span></span>             | <span data-ttu-id="bc22f-141">Faux</span><span class="sxs-lookup"><span data-stu-id="bc22f-141">False</span></span>                                                     |
| <span data-ttu-id="bc22f-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="bc22f-142">In Global Catalog</span></span>      | <span data-ttu-id="bc22f-143">Faux</span><span class="sxs-lookup"><span data-stu-id="bc22f-143">False</span></span>                                                     |
| <span data-ttu-id="bc22f-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="bc22f-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="bc22f-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="bc22f-145">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="bc22f-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bc22f-146">Range-Lower</span></span>            | <span data-ttu-id="bc22f-147">0</span><span class="sxs-lookup"><span data-stu-id="bc22f-147">0</span></span>                                                         |
| <span data-ttu-id="bc22f-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bc22f-148">Range-Upper</span></span>            | <span data-ttu-id="bc22f-149">2 048</span><span class="sxs-lookup"><span data-stu-id="bc22f-149">2048</span></span>                                                      |
| <span data-ttu-id="bc22f-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bc22f-150">Search-Flags</span></span>           | <span data-ttu-id="bc22f-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bc22f-151">0x00000000</span></span>                                                |
| <span data-ttu-id="bc22f-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bc22f-152">System-Flags</span></span>           | <span data-ttu-id="bc22f-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bc22f-153">0x00000010</span></span>                                                |
| <span data-ttu-id="bc22f-154">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="bc22f-154">Classes used in</span></span>        | [<span data-ttu-id="bc22f-155">**NTFRS-jeu de réplicas**</span><span class="sxs-lookup"><span data-stu-id="bc22f-155">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="bc22f-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bc22f-156">Windows Server 2003</span></span>



| <span data-ttu-id="bc22f-157">Entrée</span><span class="sxs-lookup"><span data-stu-id="bc22f-157">Entry</span></span> | <span data-ttu-id="bc22f-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="bc22f-158">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="bc22f-159">ID de lien</span><span class="sxs-lookup"><span data-stu-id="bc22f-159">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="bc22f-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bc22f-160">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="bc22f-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="bc22f-161">System-Only</span></span>            | <span data-ttu-id="bc22f-162">Faux</span><span class="sxs-lookup"><span data-stu-id="bc22f-162">False</span></span>                                                     |
| <span data-ttu-id="bc22f-163">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="bc22f-163">Is-Single-Valued</span></span>       | <span data-ttu-id="bc22f-164">Vrai</span><span class="sxs-lookup"><span data-stu-id="bc22f-164">True</span></span>                                                      |
| <span data-ttu-id="bc22f-165">Est indexé</span><span class="sxs-lookup"><span data-stu-id="bc22f-165">Is Indexed</span></span>             | <span data-ttu-id="bc22f-166">Faux</span><span class="sxs-lookup"><span data-stu-id="bc22f-166">False</span></span>                                                     |
| <span data-ttu-id="bc22f-167">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="bc22f-167">In Global Catalog</span></span>      | <span data-ttu-id="bc22f-168">Faux</span><span class="sxs-lookup"><span data-stu-id="bc22f-168">False</span></span>                                                     |
| <span data-ttu-id="bc22f-169">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="bc22f-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="bc22f-170">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="bc22f-170">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="bc22f-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bc22f-171">Range-Lower</span></span>            | <span data-ttu-id="bc22f-172">0</span><span class="sxs-lookup"><span data-stu-id="bc22f-172">0</span></span>                                                         |
| <span data-ttu-id="bc22f-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bc22f-173">Range-Upper</span></span>            | <span data-ttu-id="bc22f-174">2 048</span><span class="sxs-lookup"><span data-stu-id="bc22f-174">2048</span></span>                                                      |
| <span data-ttu-id="bc22f-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bc22f-175">Search-Flags</span></span>           | <span data-ttu-id="bc22f-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bc22f-176">0x00000000</span></span>                                                |
| <span data-ttu-id="bc22f-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bc22f-177">System-Flags</span></span>           | <span data-ttu-id="bc22f-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bc22f-178">0x00000010</span></span>                                                |
| <span data-ttu-id="bc22f-179">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="bc22f-179">Classes used in</span></span>        | [<span data-ttu-id="bc22f-180">**NTFRS-jeu de réplicas**</span><span class="sxs-lookup"><span data-stu-id="bc22f-180">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="bc22f-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="bc22f-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="bc22f-182">Entrée</span><span class="sxs-lookup"><span data-stu-id="bc22f-182">Entry</span></span> | <span data-ttu-id="bc22f-183">Valeur</span><span class="sxs-lookup"><span data-stu-id="bc22f-183">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="bc22f-184">ID de lien</span><span class="sxs-lookup"><span data-stu-id="bc22f-184">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="bc22f-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bc22f-185">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="bc22f-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="bc22f-186">System-Only</span></span>            | <span data-ttu-id="bc22f-187">Faux</span><span class="sxs-lookup"><span data-stu-id="bc22f-187">False</span></span>                                                     |
| <span data-ttu-id="bc22f-188">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="bc22f-188">Is-Single-Valued</span></span>       | <span data-ttu-id="bc22f-189">Vrai</span><span class="sxs-lookup"><span data-stu-id="bc22f-189">True</span></span>                                                      |
| <span data-ttu-id="bc22f-190">Est indexé</span><span class="sxs-lookup"><span data-stu-id="bc22f-190">Is Indexed</span></span>             | <span data-ttu-id="bc22f-191">Faux</span><span class="sxs-lookup"><span data-stu-id="bc22f-191">False</span></span>                                                     |
| <span data-ttu-id="bc22f-192">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="bc22f-192">In Global Catalog</span></span>      | <span data-ttu-id="bc22f-193">Faux</span><span class="sxs-lookup"><span data-stu-id="bc22f-193">False</span></span>                                                     |
| <span data-ttu-id="bc22f-194">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="bc22f-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="bc22f-195">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="bc22f-195">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="bc22f-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bc22f-196">Range-Lower</span></span>            | <span data-ttu-id="bc22f-197">0</span><span class="sxs-lookup"><span data-stu-id="bc22f-197">0</span></span>                                                         |
| <span data-ttu-id="bc22f-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bc22f-198">Range-Upper</span></span>            | <span data-ttu-id="bc22f-199">2 048</span><span class="sxs-lookup"><span data-stu-id="bc22f-199">2048</span></span>                                                      |
| <span data-ttu-id="bc22f-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bc22f-200">Search-Flags</span></span>           | <span data-ttu-id="bc22f-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bc22f-201">0x00000000</span></span>                                                |
| <span data-ttu-id="bc22f-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bc22f-202">System-Flags</span></span>           | <span data-ttu-id="bc22f-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bc22f-203">0x00000010</span></span>                                                |
| <span data-ttu-id="bc22f-204">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="bc22f-204">Classes used in</span></span>        | [<span data-ttu-id="bc22f-205">**NTFRS-jeu de réplicas**</span><span class="sxs-lookup"><span data-stu-id="bc22f-205">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="bc22f-206">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bc22f-206">Windows Server 2008</span></span>



| <span data-ttu-id="bc22f-207">Entrée</span><span class="sxs-lookup"><span data-stu-id="bc22f-207">Entry</span></span> | <span data-ttu-id="bc22f-208">Valeur</span><span class="sxs-lookup"><span data-stu-id="bc22f-208">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="bc22f-209">ID de lien</span><span class="sxs-lookup"><span data-stu-id="bc22f-209">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="bc22f-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bc22f-210">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="bc22f-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="bc22f-211">System-Only</span></span>            | <span data-ttu-id="bc22f-212">Faux</span><span class="sxs-lookup"><span data-stu-id="bc22f-212">False</span></span>                                                     |
| <span data-ttu-id="bc22f-213">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="bc22f-213">Is-Single-Valued</span></span>       | <span data-ttu-id="bc22f-214">Vrai</span><span class="sxs-lookup"><span data-stu-id="bc22f-214">True</span></span>                                                      |
| <span data-ttu-id="bc22f-215">Est indexé</span><span class="sxs-lookup"><span data-stu-id="bc22f-215">Is Indexed</span></span>             | <span data-ttu-id="bc22f-216">Faux</span><span class="sxs-lookup"><span data-stu-id="bc22f-216">False</span></span>                                                     |
| <span data-ttu-id="bc22f-217">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="bc22f-217">In Global Catalog</span></span>      | <span data-ttu-id="bc22f-218">Faux</span><span class="sxs-lookup"><span data-stu-id="bc22f-218">False</span></span>                                                     |
| <span data-ttu-id="bc22f-219">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="bc22f-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="bc22f-220">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="bc22f-220">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="bc22f-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bc22f-221">Range-Lower</span></span>            | <span data-ttu-id="bc22f-222">0</span><span class="sxs-lookup"><span data-stu-id="bc22f-222">0</span></span>                                                         |
| <span data-ttu-id="bc22f-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bc22f-223">Range-Upper</span></span>            | <span data-ttu-id="bc22f-224">2 048</span><span class="sxs-lookup"><span data-stu-id="bc22f-224">2048</span></span>                                                      |
| <span data-ttu-id="bc22f-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bc22f-225">Search-Flags</span></span>           | <span data-ttu-id="bc22f-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bc22f-226">0x00000000</span></span>                                                |
| <span data-ttu-id="bc22f-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bc22f-227">System-Flags</span></span>           | <span data-ttu-id="bc22f-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bc22f-228">0x00000010</span></span>                                                |
| <span data-ttu-id="bc22f-229">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="bc22f-229">Classes used in</span></span>        | [<span data-ttu-id="bc22f-230">**NTFRS-jeu de réplicas**</span><span class="sxs-lookup"><span data-stu-id="bc22f-230">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="bc22f-231">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bc22f-231">Windows Server 2008 R2</span></span>



| <span data-ttu-id="bc22f-232">Entrée</span><span class="sxs-lookup"><span data-stu-id="bc22f-232">Entry</span></span> | <span data-ttu-id="bc22f-233">Valeur</span><span class="sxs-lookup"><span data-stu-id="bc22f-233">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="bc22f-234">ID de lien</span><span class="sxs-lookup"><span data-stu-id="bc22f-234">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="bc22f-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bc22f-235">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="bc22f-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="bc22f-236">System-Only</span></span>            | <span data-ttu-id="bc22f-237">Faux</span><span class="sxs-lookup"><span data-stu-id="bc22f-237">False</span></span>                                                     |
| <span data-ttu-id="bc22f-238">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="bc22f-238">Is-Single-Valued</span></span>       | <span data-ttu-id="bc22f-239">Vrai</span><span class="sxs-lookup"><span data-stu-id="bc22f-239">True</span></span>                                                      |
| <span data-ttu-id="bc22f-240">Est indexé</span><span class="sxs-lookup"><span data-stu-id="bc22f-240">Is Indexed</span></span>             | <span data-ttu-id="bc22f-241">Faux</span><span class="sxs-lookup"><span data-stu-id="bc22f-241">False</span></span>                                                     |
| <span data-ttu-id="bc22f-242">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="bc22f-242">In Global Catalog</span></span>      | <span data-ttu-id="bc22f-243">Faux</span><span class="sxs-lookup"><span data-stu-id="bc22f-243">False</span></span>                                                     |
| <span data-ttu-id="bc22f-244">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="bc22f-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="bc22f-245">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="bc22f-245">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="bc22f-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bc22f-246">Range-Lower</span></span>            | <span data-ttu-id="bc22f-247">0</span><span class="sxs-lookup"><span data-stu-id="bc22f-247">0</span></span>                                                         |
| <span data-ttu-id="bc22f-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bc22f-248">Range-Upper</span></span>            | <span data-ttu-id="bc22f-249">2 048</span><span class="sxs-lookup"><span data-stu-id="bc22f-249">2048</span></span>                                                      |
| <span data-ttu-id="bc22f-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bc22f-250">Search-Flags</span></span>           | <span data-ttu-id="bc22f-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bc22f-251">0x00000000</span></span>                                                |
| <span data-ttu-id="bc22f-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bc22f-252">System-Flags</span></span>           | <span data-ttu-id="bc22f-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bc22f-253">0x00000010</span></span>                                                |
| <span data-ttu-id="bc22f-254">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="bc22f-254">Classes used in</span></span>        | [<span data-ttu-id="bc22f-255">**NTFRS-jeu de réplicas**</span><span class="sxs-lookup"><span data-stu-id="bc22f-255">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="bc22f-256">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bc22f-256">Windows Server 2012</span></span>



| <span data-ttu-id="bc22f-257">Entrée</span><span class="sxs-lookup"><span data-stu-id="bc22f-257">Entry</span></span> | <span data-ttu-id="bc22f-258">Valeur</span><span class="sxs-lookup"><span data-stu-id="bc22f-258">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="bc22f-259">ID de lien</span><span class="sxs-lookup"><span data-stu-id="bc22f-259">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="bc22f-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bc22f-260">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="bc22f-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="bc22f-261">System-Only</span></span>            | <span data-ttu-id="bc22f-262">Faux</span><span class="sxs-lookup"><span data-stu-id="bc22f-262">False</span></span>                                                     |
| <span data-ttu-id="bc22f-263">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="bc22f-263">Is-Single-Valued</span></span>       | <span data-ttu-id="bc22f-264">Vrai</span><span class="sxs-lookup"><span data-stu-id="bc22f-264">True</span></span>                                                      |
| <span data-ttu-id="bc22f-265">Est indexé</span><span class="sxs-lookup"><span data-stu-id="bc22f-265">Is Indexed</span></span>             | <span data-ttu-id="bc22f-266">Faux</span><span class="sxs-lookup"><span data-stu-id="bc22f-266">False</span></span>                                                     |
| <span data-ttu-id="bc22f-267">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="bc22f-267">In Global Catalog</span></span>      | <span data-ttu-id="bc22f-268">Faux</span><span class="sxs-lookup"><span data-stu-id="bc22f-268">False</span></span>                                                     |
| <span data-ttu-id="bc22f-269">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="bc22f-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="bc22f-270">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="bc22f-270">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="bc22f-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bc22f-271">Range-Lower</span></span>            | <span data-ttu-id="bc22f-272">0</span><span class="sxs-lookup"><span data-stu-id="bc22f-272">0</span></span>                                                         |
| <span data-ttu-id="bc22f-273">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bc22f-273">Range-Upper</span></span>            | <span data-ttu-id="bc22f-274">2 048</span><span class="sxs-lookup"><span data-stu-id="bc22f-274">2048</span></span>                                                      |
| <span data-ttu-id="bc22f-275">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bc22f-275">Search-Flags</span></span>           | <span data-ttu-id="bc22f-276">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bc22f-276">0x00000000</span></span>                                                |
| <span data-ttu-id="bc22f-277">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bc22f-277">System-Flags</span></span>           | <span data-ttu-id="bc22f-278">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bc22f-278">0x00000010</span></span>                                                |
| <span data-ttu-id="bc22f-279">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="bc22f-279">Classes used in</span></span>        | [<span data-ttu-id="bc22f-280">**NTFRS-jeu de réplicas**</span><span class="sxs-lookup"><span data-stu-id="bc22f-280">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



 

 





