---
title: MS-DFSR-attribut Schedule
description: Contient la planification de réplication pour le service de réplication système de fichiers DFS (DFS).
ms.assetid: 6dfcce16-44a4-4f7a-93ba-0c0d50605682
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut de planification MS-DFSR
- msDFSR-schéma AD d’attribut de planification
topic_type:
- apiref
api_name:
- ms-DFSR-Schedule
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 118ab92c656899d8275f0ff63ae43b412cf9742e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104480132"
---
# <a name="ms-dfsr-schedule-attribute"></a><span data-ttu-id="c9087-105">MS-DFSR-attribut Schedule</span><span class="sxs-lookup"><span data-stu-id="c9087-105">ms-DFSR-Schedule attribute</span></span>

<span data-ttu-id="c9087-106">Contient la planification de réplication pour le service de réplication système de fichiers DFS (DFS).</span><span class="sxs-lookup"><span data-stu-id="c9087-106">Contains the replication schedule for the Distributed File System (DFS) Replication service.</span></span>



| <span data-ttu-id="c9087-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="c9087-107">Entry</span></span> | <span data-ttu-id="c9087-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="c9087-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="c9087-109">CN</span><span class="sxs-lookup"><span data-stu-id="c9087-109">CN</span></span>                | <span data-ttu-id="c9087-110">MS-DFSR-planification</span><span class="sxs-lookup"><span data-stu-id="c9087-110">ms-DFSR-Schedule</span></span>                                      |
| <span data-ttu-id="c9087-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="c9087-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c9087-112">msDFSR-planification</span><span class="sxs-lookup"><span data-stu-id="c9087-112">msDFSR-Schedule</span></span>                                       |
| <span data-ttu-id="c9087-113">Taille</span><span class="sxs-lookup"><span data-stu-id="c9087-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="c9087-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="c9087-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="c9087-115">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="c9087-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="c9087-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c9087-116">Attribute-Id</span></span>      | <span data-ttu-id="c9087-117">1.2.840.113556.1.6.13.3.14</span><span class="sxs-lookup"><span data-stu-id="c9087-117">1.2.840.113556.1.6.13.3.14</span></span>                            |
| <span data-ttu-id="c9087-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c9087-118">System-Id-Guid</span></span>    | <span data-ttu-id="c9087-119">4699f15f-a71f-48e2-9ff5-5897c0759205</span><span class="sxs-lookup"><span data-stu-id="c9087-119">4699f15f-a71f-48e2-9ff5-5897c0759205</span></span>                  |
| <span data-ttu-id="c9087-120">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c9087-120">Syntax</span></span>            | [<span data-ttu-id="c9087-121">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="c9087-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="c9087-122">Implémentations</span><span class="sxs-lookup"><span data-stu-id="c9087-122">Implementations</span></span>

-   [<span data-ttu-id="c9087-123">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c9087-123">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c9087-124">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c9087-124">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c9087-125">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c9087-125">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c9087-126">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c9087-126">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003-r2"></a><span data-ttu-id="c9087-127">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c9087-127">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c9087-128">Entrée</span><span class="sxs-lookup"><span data-stu-id="c9087-128">Entry</span></span> | <span data-ttu-id="c9087-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="c9087-129">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9087-130">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c9087-130">Link-Id</span></span>                | \-                                                                                                                                    |
| <span data-ttu-id="c9087-131">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9087-131">MAPI-Id</span></span>                | \-                                                                                                                                    |
| <span data-ttu-id="c9087-132">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9087-132">System-Only</span></span>            | <span data-ttu-id="c9087-133">Faux</span><span class="sxs-lookup"><span data-stu-id="c9087-133">False</span></span>                                                                                                                                 |
| <span data-ttu-id="c9087-134">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c9087-134">Is-Single-Valued</span></span>       | <span data-ttu-id="c9087-135">Vrai</span><span class="sxs-lookup"><span data-stu-id="c9087-135">True</span></span>                                                                                                                                  |
| <span data-ttu-id="c9087-136">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c9087-136">Is Indexed</span></span>             | <span data-ttu-id="c9087-137">Faux</span><span class="sxs-lookup"><span data-stu-id="c9087-137">False</span></span>                                                                                                                                 |
| <span data-ttu-id="c9087-138">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c9087-138">In Global Catalog</span></span>      | <span data-ttu-id="c9087-139">Faux</span><span class="sxs-lookup"><span data-stu-id="c9087-139">False</span></span>                                                                                                                                 |
| <span data-ttu-id="c9087-140">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c9087-140">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9087-141">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c9087-141">O:BAG:BAD:S:</span></span>                                                                                                                          |
| <span data-ttu-id="c9087-142">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9087-142">Range-Lower</span></span>            | <span data-ttu-id="c9087-143">336</span><span class="sxs-lookup"><span data-stu-id="c9087-143">336</span></span>                                                                                                                                   |
| <span data-ttu-id="c9087-144">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9087-144">Range-Upper</span></span>            | <span data-ttu-id="c9087-145">336</span><span class="sxs-lookup"><span data-stu-id="c9087-145">336</span></span>                                                                                                                                   |
| <span data-ttu-id="c9087-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9087-146">Search-Flags</span></span>           | <span data-ttu-id="c9087-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9087-147">0x00000000</span></span>                                                                                                                            |
| <span data-ttu-id="c9087-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9087-148">System-Flags</span></span>           | <span data-ttu-id="c9087-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9087-149">0x00000000</span></span>                                                                                                                            |
| <span data-ttu-id="c9087-150">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c9087-150">Classes used in</span></span>        | [<span data-ttu-id="c9087-151">**MS-DFSR-le groupe**</span><span class="sxs-lookup"><span data-stu-id="c9087-151">**ms-DFSR-ReplicationGroup**</span></span>](c-msdfsr-replicationgroup.md)<br/> [<span data-ttu-id="c9087-152">**MS-DFSR-connexion**</span><span class="sxs-lookup"><span data-stu-id="c9087-152">**ms-DFSR-Connection**</span></span>](c-msdfsr-connection.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c9087-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c9087-153">Windows Server 2008</span></span>



| <span data-ttu-id="c9087-154">Entrée</span><span class="sxs-lookup"><span data-stu-id="c9087-154">Entry</span></span> | <span data-ttu-id="c9087-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="c9087-155">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9087-156">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c9087-156">Link-Id</span></span>                | \-                                                                                                                                    |
| <span data-ttu-id="c9087-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9087-157">MAPI-Id</span></span>                | \-                                                                                                                                    |
| <span data-ttu-id="c9087-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9087-158">System-Only</span></span>            | <span data-ttu-id="c9087-159">Faux</span><span class="sxs-lookup"><span data-stu-id="c9087-159">False</span></span>                                                                                                                                 |
| <span data-ttu-id="c9087-160">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c9087-160">Is-Single-Valued</span></span>       | <span data-ttu-id="c9087-161">Vrai</span><span class="sxs-lookup"><span data-stu-id="c9087-161">True</span></span>                                                                                                                                  |
| <span data-ttu-id="c9087-162">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c9087-162">Is Indexed</span></span>             | <span data-ttu-id="c9087-163">Faux</span><span class="sxs-lookup"><span data-stu-id="c9087-163">False</span></span>                                                                                                                                 |
| <span data-ttu-id="c9087-164">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c9087-164">In Global Catalog</span></span>      | <span data-ttu-id="c9087-165">Faux</span><span class="sxs-lookup"><span data-stu-id="c9087-165">False</span></span>                                                                                                                                 |
| <span data-ttu-id="c9087-166">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c9087-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9087-167">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c9087-167">O:BAG:BAD:S:</span></span>                                                                                                                          |
| <span data-ttu-id="c9087-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9087-168">Range-Lower</span></span>            | <span data-ttu-id="c9087-169">336</span><span class="sxs-lookup"><span data-stu-id="c9087-169">336</span></span>                                                                                                                                   |
| <span data-ttu-id="c9087-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9087-170">Range-Upper</span></span>            | <span data-ttu-id="c9087-171">336</span><span class="sxs-lookup"><span data-stu-id="c9087-171">336</span></span>                                                                                                                                   |
| <span data-ttu-id="c9087-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9087-172">Search-Flags</span></span>           | <span data-ttu-id="c9087-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9087-173">0x00000000</span></span>                                                                                                                            |
| <span data-ttu-id="c9087-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9087-174">System-Flags</span></span>           | <span data-ttu-id="c9087-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9087-175">0x00000000</span></span>                                                                                                                            |
| <span data-ttu-id="c9087-176">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c9087-176">Classes used in</span></span>        | [<span data-ttu-id="c9087-177">**MS-DFSR-le groupe**</span><span class="sxs-lookup"><span data-stu-id="c9087-177">**ms-DFSR-ReplicationGroup**</span></span>](c-msdfsr-replicationgroup.md)<br/> [<span data-ttu-id="c9087-178">**MS-DFSR-connexion**</span><span class="sxs-lookup"><span data-stu-id="c9087-178">**ms-DFSR-Connection**</span></span>](c-msdfsr-connection.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c9087-179">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c9087-179">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c9087-180">Entrée</span><span class="sxs-lookup"><span data-stu-id="c9087-180">Entry</span></span> | <span data-ttu-id="c9087-181">Valeur</span><span class="sxs-lookup"><span data-stu-id="c9087-181">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9087-182">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c9087-182">Link-Id</span></span>                | \-                                                                                                                                    |
| <span data-ttu-id="c9087-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9087-183">MAPI-Id</span></span>                | \-                                                                                                                                    |
| <span data-ttu-id="c9087-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9087-184">System-Only</span></span>            | <span data-ttu-id="c9087-185">Faux</span><span class="sxs-lookup"><span data-stu-id="c9087-185">False</span></span>                                                                                                                                 |
| <span data-ttu-id="c9087-186">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c9087-186">Is-Single-Valued</span></span>       | <span data-ttu-id="c9087-187">Vrai</span><span class="sxs-lookup"><span data-stu-id="c9087-187">True</span></span>                                                                                                                                  |
| <span data-ttu-id="c9087-188">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c9087-188">Is Indexed</span></span>             | <span data-ttu-id="c9087-189">Faux</span><span class="sxs-lookup"><span data-stu-id="c9087-189">False</span></span>                                                                                                                                 |
| <span data-ttu-id="c9087-190">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c9087-190">In Global Catalog</span></span>      | <span data-ttu-id="c9087-191">Faux</span><span class="sxs-lookup"><span data-stu-id="c9087-191">False</span></span>                                                                                                                                 |
| <span data-ttu-id="c9087-192">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c9087-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9087-193">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c9087-193">O:BAG:BAD:S:</span></span>                                                                                                                          |
| <span data-ttu-id="c9087-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9087-194">Range-Lower</span></span>            | <span data-ttu-id="c9087-195">336</span><span class="sxs-lookup"><span data-stu-id="c9087-195">336</span></span>                                                                                                                                   |
| <span data-ttu-id="c9087-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9087-196">Range-Upper</span></span>            | <span data-ttu-id="c9087-197">336</span><span class="sxs-lookup"><span data-stu-id="c9087-197">336</span></span>                                                                                                                                   |
| <span data-ttu-id="c9087-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9087-198">Search-Flags</span></span>           | <span data-ttu-id="c9087-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9087-199">0x00000000</span></span>                                                                                                                            |
| <span data-ttu-id="c9087-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9087-200">System-Flags</span></span>           | <span data-ttu-id="c9087-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9087-201">0x00000000</span></span>                                                                                                                            |
| <span data-ttu-id="c9087-202">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c9087-202">Classes used in</span></span>        | [<span data-ttu-id="c9087-203">**MS-DFSR-le groupe**</span><span class="sxs-lookup"><span data-stu-id="c9087-203">**ms-DFSR-ReplicationGroup**</span></span>](c-msdfsr-replicationgroup.md)<br/> [<span data-ttu-id="c9087-204">**MS-DFSR-connexion**</span><span class="sxs-lookup"><span data-stu-id="c9087-204">**ms-DFSR-Connection**</span></span>](c-msdfsr-connection.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c9087-205">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c9087-205">Windows Server 2012</span></span>



| <span data-ttu-id="c9087-206">Entrée</span><span class="sxs-lookup"><span data-stu-id="c9087-206">Entry</span></span> | <span data-ttu-id="c9087-207">Valeur</span><span class="sxs-lookup"><span data-stu-id="c9087-207">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9087-208">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c9087-208">Link-Id</span></span>                | \-                                                                                                                                    |
| <span data-ttu-id="c9087-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9087-209">MAPI-Id</span></span>                | \-                                                                                                                                    |
| <span data-ttu-id="c9087-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9087-210">System-Only</span></span>            | <span data-ttu-id="c9087-211">Faux</span><span class="sxs-lookup"><span data-stu-id="c9087-211">False</span></span>                                                                                                                                 |
| <span data-ttu-id="c9087-212">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c9087-212">Is-Single-Valued</span></span>       | <span data-ttu-id="c9087-213">Vrai</span><span class="sxs-lookup"><span data-stu-id="c9087-213">True</span></span>                                                                                                                                  |
| <span data-ttu-id="c9087-214">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c9087-214">Is Indexed</span></span>             | <span data-ttu-id="c9087-215">Faux</span><span class="sxs-lookup"><span data-stu-id="c9087-215">False</span></span>                                                                                                                                 |
| <span data-ttu-id="c9087-216">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c9087-216">In Global Catalog</span></span>      | <span data-ttu-id="c9087-217">Faux</span><span class="sxs-lookup"><span data-stu-id="c9087-217">False</span></span>                                                                                                                                 |
| <span data-ttu-id="c9087-218">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c9087-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9087-219">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c9087-219">O:BAG:BAD:S:</span></span>                                                                                                                          |
| <span data-ttu-id="c9087-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9087-220">Range-Lower</span></span>            | <span data-ttu-id="c9087-221">336</span><span class="sxs-lookup"><span data-stu-id="c9087-221">336</span></span>                                                                                                                                   |
| <span data-ttu-id="c9087-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9087-222">Range-Upper</span></span>            | <span data-ttu-id="c9087-223">336</span><span class="sxs-lookup"><span data-stu-id="c9087-223">336</span></span>                                                                                                                                   |
| <span data-ttu-id="c9087-224">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9087-224">Search-Flags</span></span>           | <span data-ttu-id="c9087-225">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9087-225">0x00000000</span></span>                                                                                                                            |
| <span data-ttu-id="c9087-226">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9087-226">System-Flags</span></span>           | <span data-ttu-id="c9087-227">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9087-227">0x00000000</span></span>                                                                                                                            |
| <span data-ttu-id="c9087-228">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c9087-228">Classes used in</span></span>        | [<span data-ttu-id="c9087-229">**MS-DFSR-le groupe**</span><span class="sxs-lookup"><span data-stu-id="c9087-229">**ms-DFSR-ReplicationGroup**</span></span>](c-msdfsr-replicationgroup.md)<br/> [<span data-ttu-id="c9087-230">**MS-DFSR-connexion**</span><span class="sxs-lookup"><span data-stu-id="c9087-230">**ms-DFSR-Connection**</span></span>](c-msdfsr-connection.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="c9087-231">Notes</span><span class="sxs-lookup"><span data-stu-id="c9087-231">Remarks</span></span>

<span data-ttu-id="c9087-232">L’attribut fait partie de la prise en charge du service de réplication système de fichiers DFS (DFS).</span><span class="sxs-lookup"><span data-stu-id="c9087-232">The attribute is a part of the Distributed File System (DFS) Replication service support.</span></span>

 

 





