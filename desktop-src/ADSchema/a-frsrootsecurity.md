---
title: Attribut de sécurité de la racine FRS
description: Descripteur de sécurité de la racine du jeu de réplicas pour la réplication de fichiers.
ms.assetid: 1db92f68-465a-4d93-ad4d-706ef4761ddc
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut de sécurité de la racine FRS
- Schéma AD de l’attribut fRSRootSecurity
topic_type:
- apiref
api_name:
- FRS-Root-Security
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a84059902998b120ad38215257fdddcb1c21ea6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106515692"
---
# <a name="frs-root-security-attribute"></a><span data-ttu-id="8f2bd-105">Attribut de sécurité de la racine FRS</span><span class="sxs-lookup"><span data-stu-id="8f2bd-105">FRS-Root-Security attribute</span></span>

<span data-ttu-id="8f2bd-106">Descripteur de sécurité de la racine du jeu de réplicas pour la réplication de fichiers.</span><span class="sxs-lookup"><span data-stu-id="8f2bd-106">The security descriptor of replica set root for file replication.</span></span>



| <span data-ttu-id="8f2bd-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="8f2bd-107">Entry</span></span> | <span data-ttu-id="8f2bd-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="8f2bd-108">Value</span></span> |
|-------------------|-----------------------------------------------------|
| <span data-ttu-id="8f2bd-109">CN</span><span class="sxs-lookup"><span data-stu-id="8f2bd-109">CN</span></span>                | <span data-ttu-id="8f2bd-110">Sécurité de la racine FRS</span><span class="sxs-lookup"><span data-stu-id="8f2bd-110">FRS-Root-Security</span></span>                                   |
| <span data-ttu-id="8f2bd-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="8f2bd-111">Ldap-Display-Name</span></span> | <span data-ttu-id="8f2bd-112">fRSRootSecurity</span><span class="sxs-lookup"><span data-stu-id="8f2bd-112">fRSRootSecurity</span></span>                                     |
| <span data-ttu-id="8f2bd-113">Taille</span><span class="sxs-lookup"><span data-stu-id="8f2bd-113">Size</span></span>              | \-                                                  |
| <span data-ttu-id="8f2bd-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="8f2bd-114">Update Privilege</span></span>  | \-                                                  |
| <span data-ttu-id="8f2bd-115">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="8f2bd-115">Update Frequency</span></span>  | \-                                                  |
| <span data-ttu-id="8f2bd-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8f2bd-116">Attribute-Id</span></span>      | <span data-ttu-id="8f2bd-117">1.2.840.113556.1.4.535</span><span class="sxs-lookup"><span data-stu-id="8f2bd-117">1.2.840.113556.1.4.535</span></span>                              |
| <span data-ttu-id="8f2bd-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="8f2bd-118">System-Id-Guid</span></span>    | <span data-ttu-id="8f2bd-119">5245801f-ca6a-11d0-afff-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="8f2bd-119">5245801f-ca6a-11d0-afff-0000f80367c1</span></span>                |
| <span data-ttu-id="8f2bd-120">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8f2bd-120">Syntax</span></span>            | [<span data-ttu-id="8f2bd-121">**String(NT-Sec-Desc)**</span><span class="sxs-lookup"><span data-stu-id="8f2bd-121">**String(NT-Sec-Desc)**</span></span>](s-string-nt-sec-desc.md) |



## <a name="implementations"></a><span data-ttu-id="8f2bd-122">Implémentations</span><span class="sxs-lookup"><span data-stu-id="8f2bd-122">Implementations</span></span>

-   [<span data-ttu-id="8f2bd-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8f2bd-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8f2bd-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8f2bd-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8f2bd-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8f2bd-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8f2bd-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8f2bd-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8f2bd-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8f2bd-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8f2bd-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8f2bd-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8f2bd-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8f2bd-129">Windows 2000 Server</span></span>



| <span data-ttu-id="8f2bd-130">Entrée</span><span class="sxs-lookup"><span data-stu-id="8f2bd-130">Entry</span></span> | <span data-ttu-id="8f2bd-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="8f2bd-131">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f2bd-132">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8f2bd-132">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="8f2bd-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8f2bd-133">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="8f2bd-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="8f2bd-134">System-Only</span></span>            | <span data-ttu-id="8f2bd-135">Faux</span><span class="sxs-lookup"><span data-stu-id="8f2bd-135">False</span></span>                                                                                                      |
| <span data-ttu-id="8f2bd-136">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8f2bd-136">Is-Single-Valued</span></span>       | <span data-ttu-id="8f2bd-137">Vrai</span><span class="sxs-lookup"><span data-stu-id="8f2bd-137">True</span></span>                                                                                                       |
| <span data-ttu-id="8f2bd-138">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8f2bd-138">Is Indexed</span></span>             | <span data-ttu-id="8f2bd-139">Faux</span><span class="sxs-lookup"><span data-stu-id="8f2bd-139">False</span></span>                                                                                                      |
| <span data-ttu-id="8f2bd-140">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8f2bd-140">In Global Catalog</span></span>      | <span data-ttu-id="8f2bd-141">Faux</span><span class="sxs-lookup"><span data-stu-id="8f2bd-141">False</span></span>                                                                                                      |
| <span data-ttu-id="8f2bd-142">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8f2bd-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="8f2bd-143">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8f2bd-143">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="8f2bd-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8f2bd-144">Range-Lower</span></span>            | <span data-ttu-id="8f2bd-145">0</span><span class="sxs-lookup"><span data-stu-id="8f2bd-145">0</span></span>                                                                                                          |
| <span data-ttu-id="8f2bd-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8f2bd-146">Range-Upper</span></span>            | <span data-ttu-id="8f2bd-147">65535</span><span class="sxs-lookup"><span data-stu-id="8f2bd-147">65535</span></span>                                                                                                      |
| <span data-ttu-id="8f2bd-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8f2bd-148">Search-Flags</span></span>           | <span data-ttu-id="8f2bd-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8f2bd-149">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="8f2bd-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8f2bd-150">System-Flags</span></span>           | <span data-ttu-id="8f2bd-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8f2bd-151">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="8f2bd-152">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8f2bd-152">Classes used in</span></span>        | [<span data-ttu-id="8f2bd-153">**NTFRS-Member**</span><span class="sxs-lookup"><span data-stu-id="8f2bd-153">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="8f2bd-154">**NTFRS-jeu de réplicas**</span><span class="sxs-lookup"><span data-stu-id="8f2bd-154">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8f2bd-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8f2bd-155">Windows Server 2003</span></span>



| <span data-ttu-id="8f2bd-156">Entrée</span><span class="sxs-lookup"><span data-stu-id="8f2bd-156">Entry</span></span> | <span data-ttu-id="8f2bd-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="8f2bd-157">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f2bd-158">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8f2bd-158">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="8f2bd-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8f2bd-159">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="8f2bd-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="8f2bd-160">System-Only</span></span>            | <span data-ttu-id="8f2bd-161">Faux</span><span class="sxs-lookup"><span data-stu-id="8f2bd-161">False</span></span>                                                                                                      |
| <span data-ttu-id="8f2bd-162">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8f2bd-162">Is-Single-Valued</span></span>       | <span data-ttu-id="8f2bd-163">Vrai</span><span class="sxs-lookup"><span data-stu-id="8f2bd-163">True</span></span>                                                                                                       |
| <span data-ttu-id="8f2bd-164">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8f2bd-164">Is Indexed</span></span>             | <span data-ttu-id="8f2bd-165">Faux</span><span class="sxs-lookup"><span data-stu-id="8f2bd-165">False</span></span>                                                                                                      |
| <span data-ttu-id="8f2bd-166">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8f2bd-166">In Global Catalog</span></span>      | <span data-ttu-id="8f2bd-167">Faux</span><span class="sxs-lookup"><span data-stu-id="8f2bd-167">False</span></span>                                                                                                      |
| <span data-ttu-id="8f2bd-168">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8f2bd-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="8f2bd-169">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8f2bd-169">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="8f2bd-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8f2bd-170">Range-Lower</span></span>            | <span data-ttu-id="8f2bd-171">0</span><span class="sxs-lookup"><span data-stu-id="8f2bd-171">0</span></span>                                                                                                          |
| <span data-ttu-id="8f2bd-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8f2bd-172">Range-Upper</span></span>            | <span data-ttu-id="8f2bd-173">65535</span><span class="sxs-lookup"><span data-stu-id="8f2bd-173">65535</span></span>                                                                                                      |
| <span data-ttu-id="8f2bd-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8f2bd-174">Search-Flags</span></span>           | <span data-ttu-id="8f2bd-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8f2bd-175">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="8f2bd-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8f2bd-176">System-Flags</span></span>           | <span data-ttu-id="8f2bd-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8f2bd-177">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="8f2bd-178">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8f2bd-178">Classes used in</span></span>        | [<span data-ttu-id="8f2bd-179">**NTFRS-Member**</span><span class="sxs-lookup"><span data-stu-id="8f2bd-179">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="8f2bd-180">**NTFRS-jeu de réplicas**</span><span class="sxs-lookup"><span data-stu-id="8f2bd-180">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8f2bd-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8f2bd-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8f2bd-182">Entrée</span><span class="sxs-lookup"><span data-stu-id="8f2bd-182">Entry</span></span> | <span data-ttu-id="8f2bd-183">Valeur</span><span class="sxs-lookup"><span data-stu-id="8f2bd-183">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f2bd-184">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8f2bd-184">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="8f2bd-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8f2bd-185">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="8f2bd-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="8f2bd-186">System-Only</span></span>            | <span data-ttu-id="8f2bd-187">Faux</span><span class="sxs-lookup"><span data-stu-id="8f2bd-187">False</span></span>                                                                                                      |
| <span data-ttu-id="8f2bd-188">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8f2bd-188">Is-Single-Valued</span></span>       | <span data-ttu-id="8f2bd-189">Vrai</span><span class="sxs-lookup"><span data-stu-id="8f2bd-189">True</span></span>                                                                                                       |
| <span data-ttu-id="8f2bd-190">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8f2bd-190">Is Indexed</span></span>             | <span data-ttu-id="8f2bd-191">Faux</span><span class="sxs-lookup"><span data-stu-id="8f2bd-191">False</span></span>                                                                                                      |
| <span data-ttu-id="8f2bd-192">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8f2bd-192">In Global Catalog</span></span>      | <span data-ttu-id="8f2bd-193">Faux</span><span class="sxs-lookup"><span data-stu-id="8f2bd-193">False</span></span>                                                                                                      |
| <span data-ttu-id="8f2bd-194">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8f2bd-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="8f2bd-195">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8f2bd-195">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="8f2bd-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8f2bd-196">Range-Lower</span></span>            | <span data-ttu-id="8f2bd-197">0</span><span class="sxs-lookup"><span data-stu-id="8f2bd-197">0</span></span>                                                                                                          |
| <span data-ttu-id="8f2bd-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8f2bd-198">Range-Upper</span></span>            | <span data-ttu-id="8f2bd-199">65535</span><span class="sxs-lookup"><span data-stu-id="8f2bd-199">65535</span></span>                                                                                                      |
| <span data-ttu-id="8f2bd-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8f2bd-200">Search-Flags</span></span>           | <span data-ttu-id="8f2bd-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8f2bd-201">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="8f2bd-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8f2bd-202">System-Flags</span></span>           | <span data-ttu-id="8f2bd-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8f2bd-203">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="8f2bd-204">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8f2bd-204">Classes used in</span></span>        | [<span data-ttu-id="8f2bd-205">**NTFRS-Member**</span><span class="sxs-lookup"><span data-stu-id="8f2bd-205">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="8f2bd-206">**NTFRS-jeu de réplicas**</span><span class="sxs-lookup"><span data-stu-id="8f2bd-206">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8f2bd-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8f2bd-207">Windows Server 2008</span></span>



| <span data-ttu-id="8f2bd-208">Entrée</span><span class="sxs-lookup"><span data-stu-id="8f2bd-208">Entry</span></span> | <span data-ttu-id="8f2bd-209">Valeur</span><span class="sxs-lookup"><span data-stu-id="8f2bd-209">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f2bd-210">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8f2bd-210">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="8f2bd-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8f2bd-211">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="8f2bd-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="8f2bd-212">System-Only</span></span>            | <span data-ttu-id="8f2bd-213">Faux</span><span class="sxs-lookup"><span data-stu-id="8f2bd-213">False</span></span>                                                                                                      |
| <span data-ttu-id="8f2bd-214">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8f2bd-214">Is-Single-Valued</span></span>       | <span data-ttu-id="8f2bd-215">Vrai</span><span class="sxs-lookup"><span data-stu-id="8f2bd-215">True</span></span>                                                                                                       |
| <span data-ttu-id="8f2bd-216">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8f2bd-216">Is Indexed</span></span>             | <span data-ttu-id="8f2bd-217">Faux</span><span class="sxs-lookup"><span data-stu-id="8f2bd-217">False</span></span>                                                                                                      |
| <span data-ttu-id="8f2bd-218">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8f2bd-218">In Global Catalog</span></span>      | <span data-ttu-id="8f2bd-219">Faux</span><span class="sxs-lookup"><span data-stu-id="8f2bd-219">False</span></span>                                                                                                      |
| <span data-ttu-id="8f2bd-220">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8f2bd-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="8f2bd-221">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8f2bd-221">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="8f2bd-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8f2bd-222">Range-Lower</span></span>            | <span data-ttu-id="8f2bd-223">0</span><span class="sxs-lookup"><span data-stu-id="8f2bd-223">0</span></span>                                                                                                          |
| <span data-ttu-id="8f2bd-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8f2bd-224">Range-Upper</span></span>            | <span data-ttu-id="8f2bd-225">65535</span><span class="sxs-lookup"><span data-stu-id="8f2bd-225">65535</span></span>                                                                                                      |
| <span data-ttu-id="8f2bd-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8f2bd-226">Search-Flags</span></span>           | <span data-ttu-id="8f2bd-227">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8f2bd-227">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="8f2bd-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8f2bd-228">System-Flags</span></span>           | <span data-ttu-id="8f2bd-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8f2bd-229">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="8f2bd-230">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8f2bd-230">Classes used in</span></span>        | [<span data-ttu-id="8f2bd-231">**NTFRS-Member**</span><span class="sxs-lookup"><span data-stu-id="8f2bd-231">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="8f2bd-232">**NTFRS-jeu de réplicas**</span><span class="sxs-lookup"><span data-stu-id="8f2bd-232">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8f2bd-233">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8f2bd-233">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8f2bd-234">Entrée</span><span class="sxs-lookup"><span data-stu-id="8f2bd-234">Entry</span></span> | <span data-ttu-id="8f2bd-235">Valeur</span><span class="sxs-lookup"><span data-stu-id="8f2bd-235">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f2bd-236">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8f2bd-236">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="8f2bd-237">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8f2bd-237">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="8f2bd-238">System-Only</span><span class="sxs-lookup"><span data-stu-id="8f2bd-238">System-Only</span></span>            | <span data-ttu-id="8f2bd-239">Faux</span><span class="sxs-lookup"><span data-stu-id="8f2bd-239">False</span></span>                                                                                                      |
| <span data-ttu-id="8f2bd-240">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8f2bd-240">Is-Single-Valued</span></span>       | <span data-ttu-id="8f2bd-241">Vrai</span><span class="sxs-lookup"><span data-stu-id="8f2bd-241">True</span></span>                                                                                                       |
| <span data-ttu-id="8f2bd-242">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8f2bd-242">Is Indexed</span></span>             | <span data-ttu-id="8f2bd-243">Faux</span><span class="sxs-lookup"><span data-stu-id="8f2bd-243">False</span></span>                                                                                                      |
| <span data-ttu-id="8f2bd-244">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8f2bd-244">In Global Catalog</span></span>      | <span data-ttu-id="8f2bd-245">Faux</span><span class="sxs-lookup"><span data-stu-id="8f2bd-245">False</span></span>                                                                                                      |
| <span data-ttu-id="8f2bd-246">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8f2bd-246">NT-Security-Descriptor</span></span> | <span data-ttu-id="8f2bd-247">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8f2bd-247">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="8f2bd-248">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8f2bd-248">Range-Lower</span></span>            | <span data-ttu-id="8f2bd-249">0</span><span class="sxs-lookup"><span data-stu-id="8f2bd-249">0</span></span>                                                                                                          |
| <span data-ttu-id="8f2bd-250">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8f2bd-250">Range-Upper</span></span>            | <span data-ttu-id="8f2bd-251">65535</span><span class="sxs-lookup"><span data-stu-id="8f2bd-251">65535</span></span>                                                                                                      |
| <span data-ttu-id="8f2bd-252">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8f2bd-252">Search-Flags</span></span>           | <span data-ttu-id="8f2bd-253">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8f2bd-253">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="8f2bd-254">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8f2bd-254">System-Flags</span></span>           | <span data-ttu-id="8f2bd-255">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8f2bd-255">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="8f2bd-256">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8f2bd-256">Classes used in</span></span>        | [<span data-ttu-id="8f2bd-257">**NTFRS-Member**</span><span class="sxs-lookup"><span data-stu-id="8f2bd-257">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="8f2bd-258">**NTFRS-jeu de réplicas**</span><span class="sxs-lookup"><span data-stu-id="8f2bd-258">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8f2bd-259">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8f2bd-259">Windows Server 2012</span></span>



| <span data-ttu-id="8f2bd-260">Entrée</span><span class="sxs-lookup"><span data-stu-id="8f2bd-260">Entry</span></span> | <span data-ttu-id="8f2bd-261">Valeur</span><span class="sxs-lookup"><span data-stu-id="8f2bd-261">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f2bd-262">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8f2bd-262">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="8f2bd-263">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8f2bd-263">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="8f2bd-264">System-Only</span><span class="sxs-lookup"><span data-stu-id="8f2bd-264">System-Only</span></span>            | <span data-ttu-id="8f2bd-265">Faux</span><span class="sxs-lookup"><span data-stu-id="8f2bd-265">False</span></span>                                                                                                      |
| <span data-ttu-id="8f2bd-266">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8f2bd-266">Is-Single-Valued</span></span>       | <span data-ttu-id="8f2bd-267">Vrai</span><span class="sxs-lookup"><span data-stu-id="8f2bd-267">True</span></span>                                                                                                       |
| <span data-ttu-id="8f2bd-268">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8f2bd-268">Is Indexed</span></span>             | <span data-ttu-id="8f2bd-269">Faux</span><span class="sxs-lookup"><span data-stu-id="8f2bd-269">False</span></span>                                                                                                      |
| <span data-ttu-id="8f2bd-270">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8f2bd-270">In Global Catalog</span></span>      | <span data-ttu-id="8f2bd-271">Faux</span><span class="sxs-lookup"><span data-stu-id="8f2bd-271">False</span></span>                                                                                                      |
| <span data-ttu-id="8f2bd-272">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8f2bd-272">NT-Security-Descriptor</span></span> | <span data-ttu-id="8f2bd-273">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8f2bd-273">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="8f2bd-274">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8f2bd-274">Range-Lower</span></span>            | <span data-ttu-id="8f2bd-275">0</span><span class="sxs-lookup"><span data-stu-id="8f2bd-275">0</span></span>                                                                                                          |
| <span data-ttu-id="8f2bd-276">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8f2bd-276">Range-Upper</span></span>            | <span data-ttu-id="8f2bd-277">65535</span><span class="sxs-lookup"><span data-stu-id="8f2bd-277">65535</span></span>                                                                                                      |
| <span data-ttu-id="8f2bd-278">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8f2bd-278">Search-Flags</span></span>           | <span data-ttu-id="8f2bd-279">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8f2bd-279">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="8f2bd-280">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8f2bd-280">System-Flags</span></span>           | <span data-ttu-id="8f2bd-281">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8f2bd-281">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="8f2bd-282">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8f2bd-282">Classes used in</span></span>        | [<span data-ttu-id="8f2bd-283">**NTFRS-Member**</span><span class="sxs-lookup"><span data-stu-id="8f2bd-283">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="8f2bd-284">**NTFRS-jeu de réplicas**</span><span class="sxs-lookup"><span data-stu-id="8f2bd-284">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



 

 





