---
title: Attribut de filtre de répertoire FRS
description: Liste des répertoires exclus de la réplication de fichiers, par exemple, TEMP ou obj.
ms.assetid: 3ce37a96-0cb2-46bf-aad1-80fc1304855d
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut de filtre de répertoire FRS
- Schéma AD de l’attribut fRSDirectoryFilter
topic_type:
- apiref
api_name:
- FRS-Directory-Filter
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b547cd431d7f51af698a137b7edd7dd299a3ec2f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104479700"
---
# <a name="frs-directory-filter-attribute"></a><span data-ttu-id="fa9c8-105">Attribut de filtre de répertoire FRS</span><span class="sxs-lookup"><span data-stu-id="fa9c8-105">FRS-Directory-Filter attribute</span></span>

<span data-ttu-id="fa9c8-106">Liste des répertoires exclus de la réplication de fichiers, par exemple, TEMP ou obj.</span><span class="sxs-lookup"><span data-stu-id="fa9c8-106">The list of directories excluded from file replication, for example, temp, or obj.</span></span>



| <span data-ttu-id="fa9c8-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="fa9c8-107">Entry</span></span> | <span data-ttu-id="fa9c8-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="fa9c8-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="fa9c8-109">CN</span><span class="sxs-lookup"><span data-stu-id="fa9c8-109">CN</span></span>                | <span data-ttu-id="fa9c8-110">FRS-filtre de répertoire</span><span class="sxs-lookup"><span data-stu-id="fa9c8-110">FRS-Directory-Filter</span></span>                        |
| <span data-ttu-id="fa9c8-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="fa9c8-111">Ldap-Display-Name</span></span> | <span data-ttu-id="fa9c8-112">fRSDirectoryFilter</span><span class="sxs-lookup"><span data-stu-id="fa9c8-112">fRSDirectoryFilter</span></span>                          |
| <span data-ttu-id="fa9c8-113">Taille</span><span class="sxs-lookup"><span data-stu-id="fa9c8-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="fa9c8-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="fa9c8-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="fa9c8-115">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="fa9c8-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="fa9c8-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="fa9c8-116">Attribute-Id</span></span>      | <span data-ttu-id="fa9c8-117">1.2.840.113556.1.4.484</span><span class="sxs-lookup"><span data-stu-id="fa9c8-117">1.2.840.113556.1.4.484</span></span>                      |
| <span data-ttu-id="fa9c8-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="fa9c8-118">System-Id-Guid</span></span>    | <span data-ttu-id="fa9c8-119">1be8f171-a9ff-11d0-afe2-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="fa9c8-119">1be8f171-a9ff-11d0-afe2-00c04fd930c9</span></span>        |
| <span data-ttu-id="fa9c8-120">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fa9c8-120">Syntax</span></span>            | [<span data-ttu-id="fa9c8-121">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="fa9c8-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="fa9c8-122">Implémentations</span><span class="sxs-lookup"><span data-stu-id="fa9c8-122">Implementations</span></span>

-   [<span data-ttu-id="fa9c8-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="fa9c8-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="fa9c8-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="fa9c8-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="fa9c8-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="fa9c8-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="fa9c8-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="fa9c8-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="fa9c8-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="fa9c8-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="fa9c8-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="fa9c8-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="fa9c8-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fa9c8-129">Windows 2000 Server</span></span>



| <span data-ttu-id="fa9c8-130">Entrée</span><span class="sxs-lookup"><span data-stu-id="fa9c8-130">Entry</span></span> | <span data-ttu-id="fa9c8-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="fa9c8-131">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="fa9c8-132">ID de lien</span><span class="sxs-lookup"><span data-stu-id="fa9c8-132">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="fa9c8-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fa9c8-133">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="fa9c8-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="fa9c8-134">System-Only</span></span>            | <span data-ttu-id="fa9c8-135">Faux</span><span class="sxs-lookup"><span data-stu-id="fa9c8-135">False</span></span>                                                     |
| <span data-ttu-id="fa9c8-136">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="fa9c8-136">Is-Single-Valued</span></span>       | <span data-ttu-id="fa9c8-137">Vrai</span><span class="sxs-lookup"><span data-stu-id="fa9c8-137">True</span></span>                                                      |
| <span data-ttu-id="fa9c8-138">Est indexé</span><span class="sxs-lookup"><span data-stu-id="fa9c8-138">Is Indexed</span></span>             | <span data-ttu-id="fa9c8-139">Faux</span><span class="sxs-lookup"><span data-stu-id="fa9c8-139">False</span></span>                                                     |
| <span data-ttu-id="fa9c8-140">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="fa9c8-140">In Global Catalog</span></span>      | <span data-ttu-id="fa9c8-141">Faux</span><span class="sxs-lookup"><span data-stu-id="fa9c8-141">False</span></span>                                                     |
| <span data-ttu-id="fa9c8-142">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="fa9c8-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="fa9c8-143">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="fa9c8-143">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="fa9c8-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fa9c8-144">Range-Lower</span></span>            | <span data-ttu-id="fa9c8-145">0</span><span class="sxs-lookup"><span data-stu-id="fa9c8-145">0</span></span>                                                         |
| <span data-ttu-id="fa9c8-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fa9c8-146">Range-Upper</span></span>            | <span data-ttu-id="fa9c8-147">2 048</span><span class="sxs-lookup"><span data-stu-id="fa9c8-147">2048</span></span>                                                      |
| <span data-ttu-id="fa9c8-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fa9c8-148">Search-Flags</span></span>           | <span data-ttu-id="fa9c8-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fa9c8-149">0x00000000</span></span>                                                |
| <span data-ttu-id="fa9c8-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fa9c8-150">System-Flags</span></span>           | <span data-ttu-id="fa9c8-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fa9c8-151">0x00000010</span></span>                                                |
| <span data-ttu-id="fa9c8-152">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="fa9c8-152">Classes used in</span></span>        | [<span data-ttu-id="fa9c8-153">**NTFRS-jeu de réplicas**</span><span class="sxs-lookup"><span data-stu-id="fa9c8-153">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="fa9c8-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fa9c8-154">Windows Server 2003</span></span>



| <span data-ttu-id="fa9c8-155">Entrée</span><span class="sxs-lookup"><span data-stu-id="fa9c8-155">Entry</span></span> | <span data-ttu-id="fa9c8-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="fa9c8-156">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="fa9c8-157">ID de lien</span><span class="sxs-lookup"><span data-stu-id="fa9c8-157">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="fa9c8-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fa9c8-158">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="fa9c8-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="fa9c8-159">System-Only</span></span>            | <span data-ttu-id="fa9c8-160">Faux</span><span class="sxs-lookup"><span data-stu-id="fa9c8-160">False</span></span>                                                     |
| <span data-ttu-id="fa9c8-161">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="fa9c8-161">Is-Single-Valued</span></span>       | <span data-ttu-id="fa9c8-162">Vrai</span><span class="sxs-lookup"><span data-stu-id="fa9c8-162">True</span></span>                                                      |
| <span data-ttu-id="fa9c8-163">Est indexé</span><span class="sxs-lookup"><span data-stu-id="fa9c8-163">Is Indexed</span></span>             | <span data-ttu-id="fa9c8-164">Faux</span><span class="sxs-lookup"><span data-stu-id="fa9c8-164">False</span></span>                                                     |
| <span data-ttu-id="fa9c8-165">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="fa9c8-165">In Global Catalog</span></span>      | <span data-ttu-id="fa9c8-166">Faux</span><span class="sxs-lookup"><span data-stu-id="fa9c8-166">False</span></span>                                                     |
| <span data-ttu-id="fa9c8-167">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="fa9c8-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="fa9c8-168">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="fa9c8-168">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="fa9c8-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fa9c8-169">Range-Lower</span></span>            | <span data-ttu-id="fa9c8-170">0</span><span class="sxs-lookup"><span data-stu-id="fa9c8-170">0</span></span>                                                         |
| <span data-ttu-id="fa9c8-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fa9c8-171">Range-Upper</span></span>            | <span data-ttu-id="fa9c8-172">2 048</span><span class="sxs-lookup"><span data-stu-id="fa9c8-172">2048</span></span>                                                      |
| <span data-ttu-id="fa9c8-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fa9c8-173">Search-Flags</span></span>           | <span data-ttu-id="fa9c8-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fa9c8-174">0x00000000</span></span>                                                |
| <span data-ttu-id="fa9c8-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fa9c8-175">System-Flags</span></span>           | <span data-ttu-id="fa9c8-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fa9c8-176">0x00000010</span></span>                                                |
| <span data-ttu-id="fa9c8-177">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="fa9c8-177">Classes used in</span></span>        | [<span data-ttu-id="fa9c8-178">**NTFRS-jeu de réplicas**</span><span class="sxs-lookup"><span data-stu-id="fa9c8-178">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="fa9c8-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="fa9c8-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="fa9c8-180">Entrée</span><span class="sxs-lookup"><span data-stu-id="fa9c8-180">Entry</span></span> | <span data-ttu-id="fa9c8-181">Valeur</span><span class="sxs-lookup"><span data-stu-id="fa9c8-181">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="fa9c8-182">ID de lien</span><span class="sxs-lookup"><span data-stu-id="fa9c8-182">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="fa9c8-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fa9c8-183">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="fa9c8-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="fa9c8-184">System-Only</span></span>            | <span data-ttu-id="fa9c8-185">Faux</span><span class="sxs-lookup"><span data-stu-id="fa9c8-185">False</span></span>                                                     |
| <span data-ttu-id="fa9c8-186">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="fa9c8-186">Is-Single-Valued</span></span>       | <span data-ttu-id="fa9c8-187">Vrai</span><span class="sxs-lookup"><span data-stu-id="fa9c8-187">True</span></span>                                                      |
| <span data-ttu-id="fa9c8-188">Est indexé</span><span class="sxs-lookup"><span data-stu-id="fa9c8-188">Is Indexed</span></span>             | <span data-ttu-id="fa9c8-189">Faux</span><span class="sxs-lookup"><span data-stu-id="fa9c8-189">False</span></span>                                                     |
| <span data-ttu-id="fa9c8-190">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="fa9c8-190">In Global Catalog</span></span>      | <span data-ttu-id="fa9c8-191">Faux</span><span class="sxs-lookup"><span data-stu-id="fa9c8-191">False</span></span>                                                     |
| <span data-ttu-id="fa9c8-192">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="fa9c8-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="fa9c8-193">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="fa9c8-193">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="fa9c8-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fa9c8-194">Range-Lower</span></span>            | <span data-ttu-id="fa9c8-195">0</span><span class="sxs-lookup"><span data-stu-id="fa9c8-195">0</span></span>                                                         |
| <span data-ttu-id="fa9c8-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fa9c8-196">Range-Upper</span></span>            | <span data-ttu-id="fa9c8-197">2 048</span><span class="sxs-lookup"><span data-stu-id="fa9c8-197">2048</span></span>                                                      |
| <span data-ttu-id="fa9c8-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fa9c8-198">Search-Flags</span></span>           | <span data-ttu-id="fa9c8-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fa9c8-199">0x00000000</span></span>                                                |
| <span data-ttu-id="fa9c8-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fa9c8-200">System-Flags</span></span>           | <span data-ttu-id="fa9c8-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fa9c8-201">0x00000010</span></span>                                                |
| <span data-ttu-id="fa9c8-202">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="fa9c8-202">Classes used in</span></span>        | [<span data-ttu-id="fa9c8-203">**NTFRS-jeu de réplicas**</span><span class="sxs-lookup"><span data-stu-id="fa9c8-203">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="fa9c8-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fa9c8-204">Windows Server 2008</span></span>



| <span data-ttu-id="fa9c8-205">Entrée</span><span class="sxs-lookup"><span data-stu-id="fa9c8-205">Entry</span></span> | <span data-ttu-id="fa9c8-206">Valeur</span><span class="sxs-lookup"><span data-stu-id="fa9c8-206">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="fa9c8-207">ID de lien</span><span class="sxs-lookup"><span data-stu-id="fa9c8-207">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="fa9c8-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fa9c8-208">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="fa9c8-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="fa9c8-209">System-Only</span></span>            | <span data-ttu-id="fa9c8-210">Faux</span><span class="sxs-lookup"><span data-stu-id="fa9c8-210">False</span></span>                                                     |
| <span data-ttu-id="fa9c8-211">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="fa9c8-211">Is-Single-Valued</span></span>       | <span data-ttu-id="fa9c8-212">Vrai</span><span class="sxs-lookup"><span data-stu-id="fa9c8-212">True</span></span>                                                      |
| <span data-ttu-id="fa9c8-213">Est indexé</span><span class="sxs-lookup"><span data-stu-id="fa9c8-213">Is Indexed</span></span>             | <span data-ttu-id="fa9c8-214">Faux</span><span class="sxs-lookup"><span data-stu-id="fa9c8-214">False</span></span>                                                     |
| <span data-ttu-id="fa9c8-215">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="fa9c8-215">In Global Catalog</span></span>      | <span data-ttu-id="fa9c8-216">Faux</span><span class="sxs-lookup"><span data-stu-id="fa9c8-216">False</span></span>                                                     |
| <span data-ttu-id="fa9c8-217">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="fa9c8-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="fa9c8-218">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="fa9c8-218">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="fa9c8-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fa9c8-219">Range-Lower</span></span>            | <span data-ttu-id="fa9c8-220">0</span><span class="sxs-lookup"><span data-stu-id="fa9c8-220">0</span></span>                                                         |
| <span data-ttu-id="fa9c8-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fa9c8-221">Range-Upper</span></span>            | <span data-ttu-id="fa9c8-222">2 048</span><span class="sxs-lookup"><span data-stu-id="fa9c8-222">2048</span></span>                                                      |
| <span data-ttu-id="fa9c8-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fa9c8-223">Search-Flags</span></span>           | <span data-ttu-id="fa9c8-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fa9c8-224">0x00000000</span></span>                                                |
| <span data-ttu-id="fa9c8-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fa9c8-225">System-Flags</span></span>           | <span data-ttu-id="fa9c8-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fa9c8-226">0x00000010</span></span>                                                |
| <span data-ttu-id="fa9c8-227">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="fa9c8-227">Classes used in</span></span>        | [<span data-ttu-id="fa9c8-228">**NTFRS-jeu de réplicas**</span><span class="sxs-lookup"><span data-stu-id="fa9c8-228">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="fa9c8-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fa9c8-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="fa9c8-230">Entrée</span><span class="sxs-lookup"><span data-stu-id="fa9c8-230">Entry</span></span> | <span data-ttu-id="fa9c8-231">Valeur</span><span class="sxs-lookup"><span data-stu-id="fa9c8-231">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="fa9c8-232">ID de lien</span><span class="sxs-lookup"><span data-stu-id="fa9c8-232">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="fa9c8-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fa9c8-233">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="fa9c8-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="fa9c8-234">System-Only</span></span>            | <span data-ttu-id="fa9c8-235">Faux</span><span class="sxs-lookup"><span data-stu-id="fa9c8-235">False</span></span>                                                     |
| <span data-ttu-id="fa9c8-236">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="fa9c8-236">Is-Single-Valued</span></span>       | <span data-ttu-id="fa9c8-237">Vrai</span><span class="sxs-lookup"><span data-stu-id="fa9c8-237">True</span></span>                                                      |
| <span data-ttu-id="fa9c8-238">Est indexé</span><span class="sxs-lookup"><span data-stu-id="fa9c8-238">Is Indexed</span></span>             | <span data-ttu-id="fa9c8-239">Faux</span><span class="sxs-lookup"><span data-stu-id="fa9c8-239">False</span></span>                                                     |
| <span data-ttu-id="fa9c8-240">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="fa9c8-240">In Global Catalog</span></span>      | <span data-ttu-id="fa9c8-241">Faux</span><span class="sxs-lookup"><span data-stu-id="fa9c8-241">False</span></span>                                                     |
| <span data-ttu-id="fa9c8-242">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="fa9c8-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="fa9c8-243">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="fa9c8-243">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="fa9c8-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fa9c8-244">Range-Lower</span></span>            | <span data-ttu-id="fa9c8-245">0</span><span class="sxs-lookup"><span data-stu-id="fa9c8-245">0</span></span>                                                         |
| <span data-ttu-id="fa9c8-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fa9c8-246">Range-Upper</span></span>            | <span data-ttu-id="fa9c8-247">2 048</span><span class="sxs-lookup"><span data-stu-id="fa9c8-247">2048</span></span>                                                      |
| <span data-ttu-id="fa9c8-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fa9c8-248">Search-Flags</span></span>           | <span data-ttu-id="fa9c8-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fa9c8-249">0x00000000</span></span>                                                |
| <span data-ttu-id="fa9c8-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fa9c8-250">System-Flags</span></span>           | <span data-ttu-id="fa9c8-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fa9c8-251">0x00000010</span></span>                                                |
| <span data-ttu-id="fa9c8-252">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="fa9c8-252">Classes used in</span></span>        | [<span data-ttu-id="fa9c8-253">**NTFRS-jeu de réplicas**</span><span class="sxs-lookup"><span data-stu-id="fa9c8-253">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="fa9c8-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fa9c8-254">Windows Server 2012</span></span>



| <span data-ttu-id="fa9c8-255">Entrée</span><span class="sxs-lookup"><span data-stu-id="fa9c8-255">Entry</span></span> | <span data-ttu-id="fa9c8-256">Valeur</span><span class="sxs-lookup"><span data-stu-id="fa9c8-256">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="fa9c8-257">ID de lien</span><span class="sxs-lookup"><span data-stu-id="fa9c8-257">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="fa9c8-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fa9c8-258">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="fa9c8-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="fa9c8-259">System-Only</span></span>            | <span data-ttu-id="fa9c8-260">Faux</span><span class="sxs-lookup"><span data-stu-id="fa9c8-260">False</span></span>                                                     |
| <span data-ttu-id="fa9c8-261">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="fa9c8-261">Is-Single-Valued</span></span>       | <span data-ttu-id="fa9c8-262">Vrai</span><span class="sxs-lookup"><span data-stu-id="fa9c8-262">True</span></span>                                                      |
| <span data-ttu-id="fa9c8-263">Est indexé</span><span class="sxs-lookup"><span data-stu-id="fa9c8-263">Is Indexed</span></span>             | <span data-ttu-id="fa9c8-264">Faux</span><span class="sxs-lookup"><span data-stu-id="fa9c8-264">False</span></span>                                                     |
| <span data-ttu-id="fa9c8-265">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="fa9c8-265">In Global Catalog</span></span>      | <span data-ttu-id="fa9c8-266">Faux</span><span class="sxs-lookup"><span data-stu-id="fa9c8-266">False</span></span>                                                     |
| <span data-ttu-id="fa9c8-267">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="fa9c8-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="fa9c8-268">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="fa9c8-268">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="fa9c8-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fa9c8-269">Range-Lower</span></span>            | <span data-ttu-id="fa9c8-270">0</span><span class="sxs-lookup"><span data-stu-id="fa9c8-270">0</span></span>                                                         |
| <span data-ttu-id="fa9c8-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fa9c8-271">Range-Upper</span></span>            | <span data-ttu-id="fa9c8-272">2 048</span><span class="sxs-lookup"><span data-stu-id="fa9c8-272">2048</span></span>                                                      |
| <span data-ttu-id="fa9c8-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fa9c8-273">Search-Flags</span></span>           | <span data-ttu-id="fa9c8-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fa9c8-274">0x00000000</span></span>                                                |
| <span data-ttu-id="fa9c8-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fa9c8-275">System-Flags</span></span>           | <span data-ttu-id="fa9c8-276">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fa9c8-276">0x00000010</span></span>                                                |
| <span data-ttu-id="fa9c8-277">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="fa9c8-277">Classes used in</span></span>        | [<span data-ttu-id="fa9c8-278">**NTFRS-jeu de réplicas**</span><span class="sxs-lookup"><span data-stu-id="fa9c8-278">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



 

 





