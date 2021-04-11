---
title: Attribut MS-DS-Replicas-NC-Reason
description: Attribut de l’objet ntdsConnection qui indique pourquoi (ou si) le KCC affiche la connexion est utile dans la topologie de réplication. Est à valeurs multiples et a une syntaxe DistName + Binary, où la partie binaire est un champ de bits de taille int.
ms.assetid: ba66e346-d288-4c0b-b41e-599c3f8e8405
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut MS-DS-Replicas-NC-Reason
- Schéma AD de l’attribut mS-DS-ReplicatesNCReason
topic_type:
- apiref
api_name:
- MS-DS-Replicates-NC-Reason
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a45c587ef82773b5e7fd310e8e8591f18ad27ab
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104385339"
---
# <a name="ms-ds-replicates-nc-reason-attribute"></a><span data-ttu-id="cc605-106">Attribut MS-DS-Replicas-NC-Reason</span><span class="sxs-lookup"><span data-stu-id="cc605-106">MS-DS-Replicates-NC-Reason attribute</span></span>

<span data-ttu-id="cc605-107">Attribut de l’objet ntdsConnection qui indique pourquoi (ou si) le KCC affiche la connexion est utile dans la topologie de réplication.</span><span class="sxs-lookup"><span data-stu-id="cc605-107">Attribute of ntdsConnection object that indicates why (or whether) the KCC shows the connection is useful in the replication topology.</span></span> <span data-ttu-id="cc605-108">Est à valeurs multiples et a une syntaxe DistName + Binary, où la partie binaire est un champ de bits de taille int.</span><span class="sxs-lookup"><span data-stu-id="cc605-108">Is multiple-valued and has DistName+Binary syntax, where the binary part is an int-size bitfield.</span></span>



| <span data-ttu-id="cc605-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="cc605-109">Entry</span></span> | <span data-ttu-id="cc605-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc605-110">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc605-111">CN</span><span class="sxs-lookup"><span data-stu-id="cc605-111">CN</span></span>                | <span data-ttu-id="cc605-112">MS-DS-répliques-NC-raison</span><span class="sxs-lookup"><span data-stu-id="cc605-112">MS-DS-Replicates-NC-Reason</span></span>                                                                                                                 |
| <span data-ttu-id="cc605-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="cc605-113">Ldap-Display-Name</span></span> | <span data-ttu-id="cc605-114">mS-DS-ReplicatesNCReason</span><span class="sxs-lookup"><span data-stu-id="cc605-114">mS-DS-ReplicatesNCReason</span></span>                                                                                                                   |
| <span data-ttu-id="cc605-115">Taille</span><span class="sxs-lookup"><span data-stu-id="cc605-115">Size</span></span>              | <span data-ttu-id="cc605-116">Valeur de la partie binaire : 0 = aucune \_ raison, 1 = \_ topologie GC, 2 = \_ topologie en anneau, 4 = réduire \_ la \_ topologie des TRONÇONs, 8 = topologie des serveurs obsolètes \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="cc605-116">Value for binary portion: 0 = NO\_REASON,1 = GC\_TOPOLOGY, 2 = RING\_TOPOLOGY, 4 = MINIMIZE\_HOPS\_TOPOLOGY, 8 = STALE\_SERVERS\_TOPOLOGY.</span></span> |
| <span data-ttu-id="cc605-117">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="cc605-117">Update Privilege</span></span>  | <span data-ttu-id="cc605-118">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="cc605-118">This value is set by the system.</span></span>                                                                                                           |
| <span data-ttu-id="cc605-119">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="cc605-119">Update Frequency</span></span>  | <span data-ttu-id="cc605-120">Peut changer en réponse aux modifications apportées à la topologie du réseau.</span><span class="sxs-lookup"><span data-stu-id="cc605-120">Can change in response to changes in the network topology.</span></span>                                                                                 |
| <span data-ttu-id="cc605-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="cc605-121">Attribute-Id</span></span>      | <span data-ttu-id="cc605-122">1.2.840.113556.1.4.1408</span><span class="sxs-lookup"><span data-stu-id="cc605-122">1.2.840.113556.1.4.1408</span></span>                                                                                                                    |
| <span data-ttu-id="cc605-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="cc605-123">System-Id-Guid</span></span>    | <span data-ttu-id="cc605-124">0ea12b84-08b3-11d3-91bc-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="cc605-124">0ea12b84-08b3-11d3-91bc-0000f87a57d4</span></span>                                                                                                       |
| <span data-ttu-id="cc605-125">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cc605-125">Syntax</span></span>            | [<span data-ttu-id="cc605-126">**Object(DN-Binary)**</span><span class="sxs-lookup"><span data-stu-id="cc605-126">**Object(DN-Binary)**</span></span>](s-object-dn-binary.md)                                                                                            |



## <a name="implementations"></a><span data-ttu-id="cc605-127">Implémentations</span><span class="sxs-lookup"><span data-stu-id="cc605-127">Implementations</span></span>

-   [<span data-ttu-id="cc605-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="cc605-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="cc605-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="cc605-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="cc605-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="cc605-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="cc605-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="cc605-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="cc605-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="cc605-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="cc605-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="cc605-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="cc605-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="cc605-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="cc605-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cc605-135">Windows 2000 Server</span></span>



| <span data-ttu-id="cc605-136">Entrée</span><span class="sxs-lookup"><span data-stu-id="cc605-136">Entry</span></span> | <span data-ttu-id="cc605-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc605-137">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="cc605-138">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cc605-138">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="cc605-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cc605-139">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="cc605-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="cc605-140">System-Only</span></span>            | <span data-ttu-id="cc605-141">Faux</span><span class="sxs-lookup"><span data-stu-id="cc605-141">False</span></span>                                                  |
| <span data-ttu-id="cc605-142">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cc605-142">Is-Single-Valued</span></span>       | <span data-ttu-id="cc605-143">Faux</span><span class="sxs-lookup"><span data-stu-id="cc605-143">False</span></span>                                                  |
| <span data-ttu-id="cc605-144">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cc605-144">Is Indexed</span></span>             | <span data-ttu-id="cc605-145">Faux</span><span class="sxs-lookup"><span data-stu-id="cc605-145">False</span></span>                                                  |
| <span data-ttu-id="cc605-146">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cc605-146">In Global Catalog</span></span>      | <span data-ttu-id="cc605-147">Faux</span><span class="sxs-lookup"><span data-stu-id="cc605-147">False</span></span>                                                  |
| <span data-ttu-id="cc605-148">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cc605-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="cc605-149">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cc605-149">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="cc605-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cc605-150">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="cc605-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cc605-151">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="cc605-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cc605-152">Search-Flags</span></span>           | <span data-ttu-id="cc605-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc605-153">0x00000000</span></span>                                             |
| <span data-ttu-id="cc605-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cc605-154">System-Flags</span></span>           | <span data-ttu-id="cc605-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cc605-155">0x00000010</span></span>                                             |
| <span data-ttu-id="cc605-156">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cc605-156">Classes used in</span></span>        | [<span data-ttu-id="cc605-157">**NTDS-connexion**</span><span class="sxs-lookup"><span data-stu-id="cc605-157">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="cc605-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cc605-158">Windows Server 2003</span></span>



| <span data-ttu-id="cc605-159">Entrée</span><span class="sxs-lookup"><span data-stu-id="cc605-159">Entry</span></span> | <span data-ttu-id="cc605-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc605-160">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="cc605-161">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cc605-161">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="cc605-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cc605-162">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="cc605-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="cc605-163">System-Only</span></span>            | <span data-ttu-id="cc605-164">Faux</span><span class="sxs-lookup"><span data-stu-id="cc605-164">False</span></span>                                                  |
| <span data-ttu-id="cc605-165">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cc605-165">Is-Single-Valued</span></span>       | <span data-ttu-id="cc605-166">Faux</span><span class="sxs-lookup"><span data-stu-id="cc605-166">False</span></span>                                                  |
| <span data-ttu-id="cc605-167">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cc605-167">Is Indexed</span></span>             | <span data-ttu-id="cc605-168">Faux</span><span class="sxs-lookup"><span data-stu-id="cc605-168">False</span></span>                                                  |
| <span data-ttu-id="cc605-169">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cc605-169">In Global Catalog</span></span>      | <span data-ttu-id="cc605-170">Faux</span><span class="sxs-lookup"><span data-stu-id="cc605-170">False</span></span>                                                  |
| <span data-ttu-id="cc605-171">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cc605-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="cc605-172">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cc605-172">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="cc605-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cc605-173">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="cc605-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cc605-174">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="cc605-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cc605-175">Search-Flags</span></span>           | <span data-ttu-id="cc605-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc605-176">0x00000000</span></span>                                             |
| <span data-ttu-id="cc605-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cc605-177">System-Flags</span></span>           | <span data-ttu-id="cc605-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cc605-178">0x00000010</span></span>                                             |
| <span data-ttu-id="cc605-179">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cc605-179">Classes used in</span></span>        | [<span data-ttu-id="cc605-180">**NTDS-connexion**</span><span class="sxs-lookup"><span data-stu-id="cc605-180">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="adam"></a><span data-ttu-id="cc605-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="cc605-181">ADAM</span></span>



| <span data-ttu-id="cc605-182">Entrée</span><span class="sxs-lookup"><span data-stu-id="cc605-182">Entry</span></span> | <span data-ttu-id="cc605-183">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc605-183">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="cc605-184">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cc605-184">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="cc605-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cc605-185">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="cc605-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="cc605-186">System-Only</span></span>            | <span data-ttu-id="cc605-187">Faux</span><span class="sxs-lookup"><span data-stu-id="cc605-187">False</span></span>                                                  |
| <span data-ttu-id="cc605-188">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cc605-188">Is-Single-Valued</span></span>       | <span data-ttu-id="cc605-189">Faux</span><span class="sxs-lookup"><span data-stu-id="cc605-189">False</span></span>                                                  |
| <span data-ttu-id="cc605-190">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cc605-190">Is Indexed</span></span>             | <span data-ttu-id="cc605-191">Faux</span><span class="sxs-lookup"><span data-stu-id="cc605-191">False</span></span>                                                  |
| <span data-ttu-id="cc605-192">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cc605-192">In Global Catalog</span></span>      | <span data-ttu-id="cc605-193">Faux</span><span class="sxs-lookup"><span data-stu-id="cc605-193">False</span></span>                                                  |
| <span data-ttu-id="cc605-194">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cc605-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="cc605-195">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cc605-195">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="cc605-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cc605-196">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="cc605-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cc605-197">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="cc605-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cc605-198">Search-Flags</span></span>           | <span data-ttu-id="cc605-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc605-199">0x00000000</span></span>                                             |
| <span data-ttu-id="cc605-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cc605-200">System-Flags</span></span>           | <span data-ttu-id="cc605-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cc605-201">0x00000010</span></span>                                             |
| <span data-ttu-id="cc605-202">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cc605-202">Classes used in</span></span>        | [<span data-ttu-id="cc605-203">**NTDS-connexion**</span><span class="sxs-lookup"><span data-stu-id="cc605-203">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="cc605-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="cc605-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="cc605-205">Entrée</span><span class="sxs-lookup"><span data-stu-id="cc605-205">Entry</span></span> | <span data-ttu-id="cc605-206">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc605-206">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="cc605-207">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cc605-207">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="cc605-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cc605-208">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="cc605-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="cc605-209">System-Only</span></span>            | <span data-ttu-id="cc605-210">Faux</span><span class="sxs-lookup"><span data-stu-id="cc605-210">False</span></span>                                                  |
| <span data-ttu-id="cc605-211">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cc605-211">Is-Single-Valued</span></span>       | <span data-ttu-id="cc605-212">Faux</span><span class="sxs-lookup"><span data-stu-id="cc605-212">False</span></span>                                                  |
| <span data-ttu-id="cc605-213">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cc605-213">Is Indexed</span></span>             | <span data-ttu-id="cc605-214">Faux</span><span class="sxs-lookup"><span data-stu-id="cc605-214">False</span></span>                                                  |
| <span data-ttu-id="cc605-215">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cc605-215">In Global Catalog</span></span>      | <span data-ttu-id="cc605-216">Faux</span><span class="sxs-lookup"><span data-stu-id="cc605-216">False</span></span>                                                  |
| <span data-ttu-id="cc605-217">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cc605-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="cc605-218">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cc605-218">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="cc605-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cc605-219">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="cc605-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cc605-220">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="cc605-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cc605-221">Search-Flags</span></span>           | <span data-ttu-id="cc605-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc605-222">0x00000000</span></span>                                             |
| <span data-ttu-id="cc605-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cc605-223">System-Flags</span></span>           | <span data-ttu-id="cc605-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cc605-224">0x00000010</span></span>                                             |
| <span data-ttu-id="cc605-225">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cc605-225">Classes used in</span></span>        | [<span data-ttu-id="cc605-226">**NTDS-connexion**</span><span class="sxs-lookup"><span data-stu-id="cc605-226">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="cc605-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cc605-227">Windows Server 2008</span></span>



| <span data-ttu-id="cc605-228">Entrée</span><span class="sxs-lookup"><span data-stu-id="cc605-228">Entry</span></span> | <span data-ttu-id="cc605-229">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc605-229">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="cc605-230">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cc605-230">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="cc605-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cc605-231">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="cc605-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="cc605-232">System-Only</span></span>            | <span data-ttu-id="cc605-233">Faux</span><span class="sxs-lookup"><span data-stu-id="cc605-233">False</span></span>                                                  |
| <span data-ttu-id="cc605-234">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cc605-234">Is-Single-Valued</span></span>       | <span data-ttu-id="cc605-235">Faux</span><span class="sxs-lookup"><span data-stu-id="cc605-235">False</span></span>                                                  |
| <span data-ttu-id="cc605-236">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cc605-236">Is Indexed</span></span>             | <span data-ttu-id="cc605-237">Faux</span><span class="sxs-lookup"><span data-stu-id="cc605-237">False</span></span>                                                  |
| <span data-ttu-id="cc605-238">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cc605-238">In Global Catalog</span></span>      | <span data-ttu-id="cc605-239">Faux</span><span class="sxs-lookup"><span data-stu-id="cc605-239">False</span></span>                                                  |
| <span data-ttu-id="cc605-240">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cc605-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="cc605-241">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cc605-241">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="cc605-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cc605-242">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="cc605-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cc605-243">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="cc605-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cc605-244">Search-Flags</span></span>           | <span data-ttu-id="cc605-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc605-245">0x00000000</span></span>                                             |
| <span data-ttu-id="cc605-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cc605-246">System-Flags</span></span>           | <span data-ttu-id="cc605-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cc605-247">0x00000010</span></span>                                             |
| <span data-ttu-id="cc605-248">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cc605-248">Classes used in</span></span>        | [<span data-ttu-id="cc605-249">**NTDS-connexion**</span><span class="sxs-lookup"><span data-stu-id="cc605-249">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="cc605-250">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cc605-250">Windows Server 2008 R2</span></span>



| <span data-ttu-id="cc605-251">Entrée</span><span class="sxs-lookup"><span data-stu-id="cc605-251">Entry</span></span> | <span data-ttu-id="cc605-252">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc605-252">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="cc605-253">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cc605-253">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="cc605-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cc605-254">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="cc605-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="cc605-255">System-Only</span></span>            | <span data-ttu-id="cc605-256">Faux</span><span class="sxs-lookup"><span data-stu-id="cc605-256">False</span></span>                                                  |
| <span data-ttu-id="cc605-257">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cc605-257">Is-Single-Valued</span></span>       | <span data-ttu-id="cc605-258">Faux</span><span class="sxs-lookup"><span data-stu-id="cc605-258">False</span></span>                                                  |
| <span data-ttu-id="cc605-259">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cc605-259">Is Indexed</span></span>             | <span data-ttu-id="cc605-260">Faux</span><span class="sxs-lookup"><span data-stu-id="cc605-260">False</span></span>                                                  |
| <span data-ttu-id="cc605-261">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cc605-261">In Global Catalog</span></span>      | <span data-ttu-id="cc605-262">Faux</span><span class="sxs-lookup"><span data-stu-id="cc605-262">False</span></span>                                                  |
| <span data-ttu-id="cc605-263">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cc605-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="cc605-264">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cc605-264">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="cc605-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cc605-265">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="cc605-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cc605-266">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="cc605-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cc605-267">Search-Flags</span></span>           | <span data-ttu-id="cc605-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc605-268">0x00000000</span></span>                                             |
| <span data-ttu-id="cc605-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cc605-269">System-Flags</span></span>           | <span data-ttu-id="cc605-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cc605-270">0x00000010</span></span>                                             |
| <span data-ttu-id="cc605-271">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cc605-271">Classes used in</span></span>        | [<span data-ttu-id="cc605-272">**NTDS-connexion**</span><span class="sxs-lookup"><span data-stu-id="cc605-272">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="cc605-273">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cc605-273">Windows Server 2012</span></span>



| <span data-ttu-id="cc605-274">Entrée</span><span class="sxs-lookup"><span data-stu-id="cc605-274">Entry</span></span> | <span data-ttu-id="cc605-275">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc605-275">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="cc605-276">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cc605-276">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="cc605-277">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cc605-277">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="cc605-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="cc605-278">System-Only</span></span>            | <span data-ttu-id="cc605-279">Faux</span><span class="sxs-lookup"><span data-stu-id="cc605-279">False</span></span>                                                  |
| <span data-ttu-id="cc605-280">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cc605-280">Is-Single-Valued</span></span>       | <span data-ttu-id="cc605-281">Faux</span><span class="sxs-lookup"><span data-stu-id="cc605-281">False</span></span>                                                  |
| <span data-ttu-id="cc605-282">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cc605-282">Is Indexed</span></span>             | <span data-ttu-id="cc605-283">Faux</span><span class="sxs-lookup"><span data-stu-id="cc605-283">False</span></span>                                                  |
| <span data-ttu-id="cc605-284">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cc605-284">In Global Catalog</span></span>      | <span data-ttu-id="cc605-285">Faux</span><span class="sxs-lookup"><span data-stu-id="cc605-285">False</span></span>                                                  |
| <span data-ttu-id="cc605-286">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cc605-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="cc605-287">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cc605-287">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="cc605-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cc605-288">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="cc605-289">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cc605-289">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="cc605-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cc605-290">Search-Flags</span></span>           | <span data-ttu-id="cc605-291">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc605-291">0x00000000</span></span>                                             |
| <span data-ttu-id="cc605-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cc605-292">System-Flags</span></span>           | <span data-ttu-id="cc605-293">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cc605-293">0x00000010</span></span>                                             |
| <span data-ttu-id="cc605-294">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cc605-294">Classes used in</span></span>        | [<span data-ttu-id="cc605-295">**NTDS-connexion**</span><span class="sxs-lookup"><span data-stu-id="cc605-295">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



 

 





