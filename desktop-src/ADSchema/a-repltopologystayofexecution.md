---
title: Attribut REPL-Topology-Rest-of-Execution
description: Délai entre la suppression d’un objet serveur et sa suppression définitive de la topologie de réplication.
ms.assetid: 770231b0-4886-41c2-a3b5-ac488ac09669
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory REPL-Topology-Rest-Execution Attribute
- Schéma AD de l’attribut replTopologyStayOfExecution
topic_type:
- apiref
api_name:
- Repl-Topology-Stay-Of-Execution
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a51c74c477cce926dd18ea17b8df2b1adcf99df1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744556"
---
# <a name="repl-topology-stay-of-execution-attribute"></a><span data-ttu-id="d987b-105">Attribut REPL-Topology-Rest-of-Execution</span><span class="sxs-lookup"><span data-stu-id="d987b-105">Repl-Topology-Stay-Of-Execution attribute</span></span>

<span data-ttu-id="d987b-106">Délai entre la suppression d’un objet serveur et sa suppression définitive de la topologie de réplication.</span><span class="sxs-lookup"><span data-stu-id="d987b-106">The delay between deleting a server object and it being permanently removed from the replication topology.</span></span>



| <span data-ttu-id="d987b-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="d987b-107">Entry</span></span> | <span data-ttu-id="d987b-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="d987b-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="d987b-109">CN</span><span class="sxs-lookup"><span data-stu-id="d987b-109">CN</span></span>                | <span data-ttu-id="d987b-110">REPL-Topology-Rest-of-Execution</span><span class="sxs-lookup"><span data-stu-id="d987b-110">Repl-Topology-Stay-Of-Execution</span></span>      |
| <span data-ttu-id="d987b-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="d987b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="d987b-112">replTopologyStayOfExecution</span><span class="sxs-lookup"><span data-stu-id="d987b-112">replTopologyStayOfExecution</span></span>          |
| <span data-ttu-id="d987b-113">Taille</span><span class="sxs-lookup"><span data-stu-id="d987b-113">Size</span></span>              | <span data-ttu-id="d987b-114">4 octets</span><span class="sxs-lookup"><span data-stu-id="d987b-114">4 bytes</span></span>                              |
| <span data-ttu-id="d987b-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="d987b-115">Update Privilege</span></span>  | <span data-ttu-id="d987b-116">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="d987b-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="d987b-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="d987b-117">Update Frequency</span></span>  | <span data-ttu-id="d987b-118">Chaque fois qu’un objet serveur est supprimé.</span><span class="sxs-lookup"><span data-stu-id="d987b-118">Whenever a server object is deleted.</span></span> |
| <span data-ttu-id="d987b-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d987b-119">Attribute-Id</span></span>      | <span data-ttu-id="d987b-120">1.2.840.113556.1.4.677</span><span class="sxs-lookup"><span data-stu-id="d987b-120">1.2.840.113556.1.4.677</span></span>               |
| <span data-ttu-id="d987b-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="d987b-121">System-Id-Guid</span></span>    | <span data-ttu-id="d987b-122">7bfdcb83-4807-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="d987b-122">7bfdcb83-4807-11d1-a9c3-0000f80367c1</span></span> |
| <span data-ttu-id="d987b-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d987b-123">Syntax</span></span>            | [<span data-ttu-id="d987b-124">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="d987b-124">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="d987b-125">Implémentations</span><span class="sxs-lookup"><span data-stu-id="d987b-125">Implementations</span></span>

-   [<span data-ttu-id="d987b-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d987b-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d987b-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d987b-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d987b-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="d987b-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="d987b-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d987b-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d987b-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d987b-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d987b-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d987b-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d987b-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d987b-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d987b-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d987b-133">Windows 2000 Server</span></span>



| <span data-ttu-id="d987b-134">Entrée</span><span class="sxs-lookup"><span data-stu-id="d987b-134">Entry</span></span> | <span data-ttu-id="d987b-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="d987b-135">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="d987b-136">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d987b-136">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="d987b-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d987b-137">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="d987b-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="d987b-138">System-Only</span></span>            | <span data-ttu-id="d987b-139">Faux</span><span class="sxs-lookup"><span data-stu-id="d987b-139">False</span></span>                                            |
| <span data-ttu-id="d987b-140">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d987b-140">Is-Single-Valued</span></span>       | <span data-ttu-id="d987b-141">Vrai</span><span class="sxs-lookup"><span data-stu-id="d987b-141">True</span></span>                                             |
| <span data-ttu-id="d987b-142">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d987b-142">Is Indexed</span></span>             | <span data-ttu-id="d987b-143">Faux</span><span class="sxs-lookup"><span data-stu-id="d987b-143">False</span></span>                                            |
| <span data-ttu-id="d987b-144">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d987b-144">In Global Catalog</span></span>      | <span data-ttu-id="d987b-145">Faux</span><span class="sxs-lookup"><span data-stu-id="d987b-145">False</span></span>                                            |
| <span data-ttu-id="d987b-146">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d987b-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="d987b-147">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d987b-147">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="d987b-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d987b-148">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="d987b-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d987b-149">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="d987b-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d987b-150">Search-Flags</span></span>           | <span data-ttu-id="d987b-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d987b-151">0x00000000</span></span>                                       |
| <span data-ttu-id="d987b-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d987b-152">System-Flags</span></span>           | <span data-ttu-id="d987b-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d987b-153">0x00000010</span></span>                                       |
| <span data-ttu-id="d987b-154">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d987b-154">Classes used in</span></span>        | [<span data-ttu-id="d987b-155">**NTDS-service**</span><span class="sxs-lookup"><span data-stu-id="d987b-155">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d987b-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d987b-156">Windows Server 2003</span></span>



| <span data-ttu-id="d987b-157">Entrée</span><span class="sxs-lookup"><span data-stu-id="d987b-157">Entry</span></span> | <span data-ttu-id="d987b-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="d987b-158">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="d987b-159">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d987b-159">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="d987b-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d987b-160">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="d987b-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="d987b-161">System-Only</span></span>            | <span data-ttu-id="d987b-162">Faux</span><span class="sxs-lookup"><span data-stu-id="d987b-162">False</span></span>                                            |
| <span data-ttu-id="d987b-163">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d987b-163">Is-Single-Valued</span></span>       | <span data-ttu-id="d987b-164">Vrai</span><span class="sxs-lookup"><span data-stu-id="d987b-164">True</span></span>                                             |
| <span data-ttu-id="d987b-165">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d987b-165">Is Indexed</span></span>             | <span data-ttu-id="d987b-166">Faux</span><span class="sxs-lookup"><span data-stu-id="d987b-166">False</span></span>                                            |
| <span data-ttu-id="d987b-167">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d987b-167">In Global Catalog</span></span>      | <span data-ttu-id="d987b-168">Faux</span><span class="sxs-lookup"><span data-stu-id="d987b-168">False</span></span>                                            |
| <span data-ttu-id="d987b-169">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d987b-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="d987b-170">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d987b-170">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="d987b-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d987b-171">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="d987b-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d987b-172">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="d987b-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d987b-173">Search-Flags</span></span>           | <span data-ttu-id="d987b-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d987b-174">0x00000000</span></span>                                       |
| <span data-ttu-id="d987b-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d987b-175">System-Flags</span></span>           | <span data-ttu-id="d987b-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d987b-176">0x00000010</span></span>                                       |
| <span data-ttu-id="d987b-177">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d987b-177">Classes used in</span></span>        | [<span data-ttu-id="d987b-178">**NTDS-service**</span><span class="sxs-lookup"><span data-stu-id="d987b-178">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="adam"></a><span data-ttu-id="d987b-179">ADAM</span><span class="sxs-lookup"><span data-stu-id="d987b-179">ADAM</span></span>



| <span data-ttu-id="d987b-180">Entrée</span><span class="sxs-lookup"><span data-stu-id="d987b-180">Entry</span></span> | <span data-ttu-id="d987b-181">Valeur</span><span class="sxs-lookup"><span data-stu-id="d987b-181">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="d987b-182">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d987b-182">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="d987b-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d987b-183">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="d987b-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="d987b-184">System-Only</span></span>            | <span data-ttu-id="d987b-185">Faux</span><span class="sxs-lookup"><span data-stu-id="d987b-185">False</span></span>                                            |
| <span data-ttu-id="d987b-186">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d987b-186">Is-Single-Valued</span></span>       | <span data-ttu-id="d987b-187">Vrai</span><span class="sxs-lookup"><span data-stu-id="d987b-187">True</span></span>                                             |
| <span data-ttu-id="d987b-188">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d987b-188">Is Indexed</span></span>             | <span data-ttu-id="d987b-189">Faux</span><span class="sxs-lookup"><span data-stu-id="d987b-189">False</span></span>                                            |
| <span data-ttu-id="d987b-190">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d987b-190">In Global Catalog</span></span>      | <span data-ttu-id="d987b-191">Faux</span><span class="sxs-lookup"><span data-stu-id="d987b-191">False</span></span>                                            |
| <span data-ttu-id="d987b-192">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d987b-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="d987b-193">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d987b-193">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="d987b-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d987b-194">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="d987b-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d987b-195">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="d987b-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d987b-196">Search-Flags</span></span>           | <span data-ttu-id="d987b-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d987b-197">0x00000000</span></span>                                       |
| <span data-ttu-id="d987b-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d987b-198">System-Flags</span></span>           | <span data-ttu-id="d987b-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d987b-199">0x00000010</span></span>                                       |
| <span data-ttu-id="d987b-200">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d987b-200">Classes used in</span></span>        | [<span data-ttu-id="d987b-201">**NTDS-service**</span><span class="sxs-lookup"><span data-stu-id="d987b-201">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d987b-202">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d987b-202">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d987b-203">Entrée</span><span class="sxs-lookup"><span data-stu-id="d987b-203">Entry</span></span> | <span data-ttu-id="d987b-204">Valeur</span><span class="sxs-lookup"><span data-stu-id="d987b-204">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="d987b-205">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d987b-205">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="d987b-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d987b-206">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="d987b-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="d987b-207">System-Only</span></span>            | <span data-ttu-id="d987b-208">Faux</span><span class="sxs-lookup"><span data-stu-id="d987b-208">False</span></span>                                            |
| <span data-ttu-id="d987b-209">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d987b-209">Is-Single-Valued</span></span>       | <span data-ttu-id="d987b-210">Vrai</span><span class="sxs-lookup"><span data-stu-id="d987b-210">True</span></span>                                             |
| <span data-ttu-id="d987b-211">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d987b-211">Is Indexed</span></span>             | <span data-ttu-id="d987b-212">Faux</span><span class="sxs-lookup"><span data-stu-id="d987b-212">False</span></span>                                            |
| <span data-ttu-id="d987b-213">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d987b-213">In Global Catalog</span></span>      | <span data-ttu-id="d987b-214">Faux</span><span class="sxs-lookup"><span data-stu-id="d987b-214">False</span></span>                                            |
| <span data-ttu-id="d987b-215">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d987b-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="d987b-216">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d987b-216">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="d987b-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d987b-217">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="d987b-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d987b-218">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="d987b-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d987b-219">Search-Flags</span></span>           | <span data-ttu-id="d987b-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d987b-220">0x00000000</span></span>                                       |
| <span data-ttu-id="d987b-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d987b-221">System-Flags</span></span>           | <span data-ttu-id="d987b-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d987b-222">0x00000010</span></span>                                       |
| <span data-ttu-id="d987b-223">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d987b-223">Classes used in</span></span>        | [<span data-ttu-id="d987b-224">**NTDS-service**</span><span class="sxs-lookup"><span data-stu-id="d987b-224">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d987b-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d987b-225">Windows Server 2008</span></span>



| <span data-ttu-id="d987b-226">Entrée</span><span class="sxs-lookup"><span data-stu-id="d987b-226">Entry</span></span> | <span data-ttu-id="d987b-227">Valeur</span><span class="sxs-lookup"><span data-stu-id="d987b-227">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="d987b-228">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d987b-228">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="d987b-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d987b-229">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="d987b-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="d987b-230">System-Only</span></span>            | <span data-ttu-id="d987b-231">Faux</span><span class="sxs-lookup"><span data-stu-id="d987b-231">False</span></span>                                            |
| <span data-ttu-id="d987b-232">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d987b-232">Is-Single-Valued</span></span>       | <span data-ttu-id="d987b-233">Vrai</span><span class="sxs-lookup"><span data-stu-id="d987b-233">True</span></span>                                             |
| <span data-ttu-id="d987b-234">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d987b-234">Is Indexed</span></span>             | <span data-ttu-id="d987b-235">Faux</span><span class="sxs-lookup"><span data-stu-id="d987b-235">False</span></span>                                            |
| <span data-ttu-id="d987b-236">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d987b-236">In Global Catalog</span></span>      | <span data-ttu-id="d987b-237">Faux</span><span class="sxs-lookup"><span data-stu-id="d987b-237">False</span></span>                                            |
| <span data-ttu-id="d987b-238">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d987b-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="d987b-239">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d987b-239">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="d987b-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d987b-240">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="d987b-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d987b-241">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="d987b-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d987b-242">Search-Flags</span></span>           | <span data-ttu-id="d987b-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d987b-243">0x00000000</span></span>                                       |
| <span data-ttu-id="d987b-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d987b-244">System-Flags</span></span>           | <span data-ttu-id="d987b-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d987b-245">0x00000010</span></span>                                       |
| <span data-ttu-id="d987b-246">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d987b-246">Classes used in</span></span>        | [<span data-ttu-id="d987b-247">**NTDS-service**</span><span class="sxs-lookup"><span data-stu-id="d987b-247">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d987b-248">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d987b-248">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d987b-249">Entrée</span><span class="sxs-lookup"><span data-stu-id="d987b-249">Entry</span></span> | <span data-ttu-id="d987b-250">Valeur</span><span class="sxs-lookup"><span data-stu-id="d987b-250">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="d987b-251">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d987b-251">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="d987b-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d987b-252">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="d987b-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="d987b-253">System-Only</span></span>            | <span data-ttu-id="d987b-254">Faux</span><span class="sxs-lookup"><span data-stu-id="d987b-254">False</span></span>                                            |
| <span data-ttu-id="d987b-255">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d987b-255">Is-Single-Valued</span></span>       | <span data-ttu-id="d987b-256">Vrai</span><span class="sxs-lookup"><span data-stu-id="d987b-256">True</span></span>                                             |
| <span data-ttu-id="d987b-257">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d987b-257">Is Indexed</span></span>             | <span data-ttu-id="d987b-258">Faux</span><span class="sxs-lookup"><span data-stu-id="d987b-258">False</span></span>                                            |
| <span data-ttu-id="d987b-259">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d987b-259">In Global Catalog</span></span>      | <span data-ttu-id="d987b-260">Faux</span><span class="sxs-lookup"><span data-stu-id="d987b-260">False</span></span>                                            |
| <span data-ttu-id="d987b-261">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d987b-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="d987b-262">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d987b-262">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="d987b-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d987b-263">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="d987b-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d987b-264">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="d987b-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d987b-265">Search-Flags</span></span>           | <span data-ttu-id="d987b-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d987b-266">0x00000000</span></span>                                       |
| <span data-ttu-id="d987b-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d987b-267">System-Flags</span></span>           | <span data-ttu-id="d987b-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d987b-268">0x00000010</span></span>                                       |
| <span data-ttu-id="d987b-269">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d987b-269">Classes used in</span></span>        | [<span data-ttu-id="d987b-270">**NTDS-service**</span><span class="sxs-lookup"><span data-stu-id="d987b-270">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d987b-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d987b-271">Windows Server 2012</span></span>



| <span data-ttu-id="d987b-272">Entrée</span><span class="sxs-lookup"><span data-stu-id="d987b-272">Entry</span></span> | <span data-ttu-id="d987b-273">Valeur</span><span class="sxs-lookup"><span data-stu-id="d987b-273">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="d987b-274">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d987b-274">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="d987b-275">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d987b-275">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="d987b-276">System-Only</span><span class="sxs-lookup"><span data-stu-id="d987b-276">System-Only</span></span>            | <span data-ttu-id="d987b-277">Faux</span><span class="sxs-lookup"><span data-stu-id="d987b-277">False</span></span>                                            |
| <span data-ttu-id="d987b-278">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d987b-278">Is-Single-Valued</span></span>       | <span data-ttu-id="d987b-279">Vrai</span><span class="sxs-lookup"><span data-stu-id="d987b-279">True</span></span>                                             |
| <span data-ttu-id="d987b-280">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d987b-280">Is Indexed</span></span>             | <span data-ttu-id="d987b-281">Faux</span><span class="sxs-lookup"><span data-stu-id="d987b-281">False</span></span>                                            |
| <span data-ttu-id="d987b-282">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d987b-282">In Global Catalog</span></span>      | <span data-ttu-id="d987b-283">Faux</span><span class="sxs-lookup"><span data-stu-id="d987b-283">False</span></span>                                            |
| <span data-ttu-id="d987b-284">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d987b-284">NT-Security-Descriptor</span></span> | <span data-ttu-id="d987b-285">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d987b-285">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="d987b-286">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d987b-286">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="d987b-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d987b-287">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="d987b-288">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d987b-288">Search-Flags</span></span>           | <span data-ttu-id="d987b-289">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d987b-289">0x00000000</span></span>                                       |
| <span data-ttu-id="d987b-290">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d987b-290">System-Flags</span></span>           | <span data-ttu-id="d987b-291">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d987b-291">0x00000010</span></span>                                       |
| <span data-ttu-id="d987b-292">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d987b-292">Classes used in</span></span>        | [<span data-ttu-id="d987b-293">**NTDS-service**</span><span class="sxs-lookup"><span data-stu-id="d987b-293">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



 

 





