---
title: Attribut REPL-UpToDate-Vector
description: Effectue le suivi des informations d’état de la réplication interne pour un contexte de nommage entier. Les informations fournies ici peuvent être extraites sous forme publique via l’API DsReplicaGetInfo (). Présente sur tous les objets racines NC.
ms.assetid: f23d94f8-c31b-447f-98c3-c35a4f5f1d43
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut REPL-UpToDate-Vector
- Schéma AD de l’attribut l’replUpToDateVector
topic_type:
- apiref
api_name:
- Repl-UpToDate-Vector
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9263111459d01d99cf5990d1c818b5ff2a7a19be
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106517131"
---
# <a name="repl-uptodate-vector-attribute"></a><span data-ttu-id="f1a5f-107">Attribut REPL-UpToDate-Vector</span><span class="sxs-lookup"><span data-stu-id="f1a5f-107">Repl-UpToDate-Vector attribute</span></span>

<span data-ttu-id="f1a5f-108">Effectue le suivi des informations d’état de la réplication interne pour un contexte de nommage entier.</span><span class="sxs-lookup"><span data-stu-id="f1a5f-108">Tracks internal replication state information for an entire NC.</span></span> <span data-ttu-id="f1a5f-109">Les informations fournies ici peuvent être extraites sous forme publique via l’API DsReplicaGetInfo ().</span><span class="sxs-lookup"><span data-stu-id="f1a5f-109">Information here can be extracted in public form through the API DsReplicaGetInfo().</span></span> <span data-ttu-id="f1a5f-110">Présente sur tous les objets racines NC.</span><span class="sxs-lookup"><span data-stu-id="f1a5f-110">Present on all NC root objects.</span></span>



| <span data-ttu-id="f1a5f-111">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1a5f-111">Entry</span></span> | <span data-ttu-id="f1a5f-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1a5f-112">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="f1a5f-113">CN</span><span class="sxs-lookup"><span data-stu-id="f1a5f-113">CN</span></span>                | <span data-ttu-id="f1a5f-114">REPL-UpToDate-Vector</span><span class="sxs-lookup"><span data-stu-id="f1a5f-114">Repl-UpToDate-Vector</span></span>                                                           |
| <span data-ttu-id="f1a5f-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f1a5f-115">Ldap-Display-Name</span></span> | <span data-ttu-id="f1a5f-116">L’replUpToDateVector</span><span class="sxs-lookup"><span data-stu-id="f1a5f-116">replUpToDateVector</span></span>                                                             |
| <span data-ttu-id="f1a5f-117">Taille</span><span class="sxs-lookup"><span data-stu-id="f1a5f-117">Size</span></span>              | <span data-ttu-id="f1a5f-118">La longueur est proportionnelle au nombre de réplicas (passés et présents) du contexte de nommage.</span><span class="sxs-lookup"><span data-stu-id="f1a5f-118">Length is proportional to the number of replicas (past and present) of the NC.</span></span> |
| <span data-ttu-id="f1a5f-119">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="f1a5f-119">Update Privilege</span></span>  | <span data-ttu-id="f1a5f-120">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="f1a5f-120">This value is set by the system.</span></span>                                               |
| <span data-ttu-id="f1a5f-121">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="f1a5f-121">Update Frequency</span></span>  | <span data-ttu-id="f1a5f-122">Modifications en réponse aux cycles de réplication entrante terminées.</span><span class="sxs-lookup"><span data-stu-id="f1a5f-122">Changes in response to completed inbound replication cycles.</span></span>                   |
| <span data-ttu-id="f1a5f-123">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f1a5f-123">Attribute-Id</span></span>      | <span data-ttu-id="f1a5f-124">1.2.840.113556.1.4.4</span><span class="sxs-lookup"><span data-stu-id="f1a5f-124">1.2.840.113556.1.4.4</span></span>                                                           |
| <span data-ttu-id="f1a5f-125">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f1a5f-125">System-Id-Guid</span></span>    | <span data-ttu-id="f1a5f-126">bf967a16-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="f1a5f-126">bf967a16-0de6-11d0-a285-00aa003049e2</span></span>                                           |
| <span data-ttu-id="f1a5f-127">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f1a5f-127">Syntax</span></span>            | [<span data-ttu-id="f1a5f-128">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="f1a5f-128">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                          |



## <a name="implementations"></a><span data-ttu-id="f1a5f-129">Implémentations</span><span class="sxs-lookup"><span data-stu-id="f1a5f-129">Implementations</span></span>

-   [<span data-ttu-id="f1a5f-130">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f1a5f-130">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f1a5f-131">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f1a5f-131">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f1a5f-132">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="f1a5f-132">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="f1a5f-133">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f1a5f-133">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f1a5f-134">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f1a5f-134">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f1a5f-135">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f1a5f-135">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f1a5f-136">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f1a5f-136">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f1a5f-137">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f1a5f-137">Windows 2000 Server</span></span>



| <span data-ttu-id="f1a5f-138">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1a5f-138">Entry</span></span> | <span data-ttu-id="f1a5f-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1a5f-139">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f1a5f-140">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f1a5f-140">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f1a5f-141">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f1a5f-141">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f1a5f-142">System-Only</span><span class="sxs-lookup"><span data-stu-id="f1a5f-142">System-Only</span></span>            | <span data-ttu-id="f1a5f-143">Vrai</span><span class="sxs-lookup"><span data-stu-id="f1a5f-143">True</span></span>                            |
| <span data-ttu-id="f1a5f-144">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f1a5f-144">Is-Single-Valued</span></span>       | <span data-ttu-id="f1a5f-145">Vrai</span><span class="sxs-lookup"><span data-stu-id="f1a5f-145">True</span></span>                            |
| <span data-ttu-id="f1a5f-146">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f1a5f-146">Is Indexed</span></span>             | <span data-ttu-id="f1a5f-147">Faux</span><span class="sxs-lookup"><span data-stu-id="f1a5f-147">False</span></span>                           |
| <span data-ttu-id="f1a5f-148">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f1a5f-148">In Global Catalog</span></span>      | <span data-ttu-id="f1a5f-149">Vrai</span><span class="sxs-lookup"><span data-stu-id="f1a5f-149">True</span></span>                            |
| <span data-ttu-id="f1a5f-150">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f1a5f-150">NT-Security-Descriptor</span></span> | <span data-ttu-id="f1a5f-151">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f1a5f-151">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f1a5f-152">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f1a5f-152">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f1a5f-153">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f1a5f-153">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f1a5f-154">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f1a5f-154">Search-Flags</span></span>           | <span data-ttu-id="f1a5f-155">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f1a5f-155">0x00000000</span></span>                      |
| <span data-ttu-id="f1a5f-156">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f1a5f-156">System-Flags</span></span>           | <span data-ttu-id="f1a5f-157">0x00000013</span><span class="sxs-lookup"><span data-stu-id="f1a5f-157">0x00000013</span></span>                      |
| <span data-ttu-id="f1a5f-158">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f1a5f-158">Classes used in</span></span>        | [<span data-ttu-id="f1a5f-159">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="f1a5f-159">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f1a5f-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f1a5f-160">Windows Server 2003</span></span>



| <span data-ttu-id="f1a5f-161">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1a5f-161">Entry</span></span> | <span data-ttu-id="f1a5f-162">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1a5f-162">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f1a5f-163">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f1a5f-163">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f1a5f-164">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f1a5f-164">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f1a5f-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="f1a5f-165">System-Only</span></span>            | <span data-ttu-id="f1a5f-166">Vrai</span><span class="sxs-lookup"><span data-stu-id="f1a5f-166">True</span></span>                            |
| <span data-ttu-id="f1a5f-167">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f1a5f-167">Is-Single-Valued</span></span>       | <span data-ttu-id="f1a5f-168">Vrai</span><span class="sxs-lookup"><span data-stu-id="f1a5f-168">True</span></span>                            |
| <span data-ttu-id="f1a5f-169">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f1a5f-169">Is Indexed</span></span>             | <span data-ttu-id="f1a5f-170">Faux</span><span class="sxs-lookup"><span data-stu-id="f1a5f-170">False</span></span>                           |
| <span data-ttu-id="f1a5f-171">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f1a5f-171">In Global Catalog</span></span>      | <span data-ttu-id="f1a5f-172">Vrai</span><span class="sxs-lookup"><span data-stu-id="f1a5f-172">True</span></span>                            |
| <span data-ttu-id="f1a5f-173">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f1a5f-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="f1a5f-174">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f1a5f-174">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f1a5f-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f1a5f-175">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f1a5f-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f1a5f-176">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f1a5f-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f1a5f-177">Search-Flags</span></span>           | <span data-ttu-id="f1a5f-178">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f1a5f-178">0x00000000</span></span>                      |
| <span data-ttu-id="f1a5f-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f1a5f-179">System-Flags</span></span>           | <span data-ttu-id="f1a5f-180">0x00000013</span><span class="sxs-lookup"><span data-stu-id="f1a5f-180">0x00000013</span></span>                      |
| <span data-ttu-id="f1a5f-181">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f1a5f-181">Classes used in</span></span>        | [<span data-ttu-id="f1a5f-182">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="f1a5f-182">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="f1a5f-183">ADAM</span><span class="sxs-lookup"><span data-stu-id="f1a5f-183">ADAM</span></span>



| <span data-ttu-id="f1a5f-184">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1a5f-184">Entry</span></span> | <span data-ttu-id="f1a5f-185">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1a5f-185">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f1a5f-186">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f1a5f-186">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f1a5f-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f1a5f-187">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f1a5f-188">System-Only</span><span class="sxs-lookup"><span data-stu-id="f1a5f-188">System-Only</span></span>            | <span data-ttu-id="f1a5f-189">Vrai</span><span class="sxs-lookup"><span data-stu-id="f1a5f-189">True</span></span>                            |
| <span data-ttu-id="f1a5f-190">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f1a5f-190">Is-Single-Valued</span></span>       | <span data-ttu-id="f1a5f-191">Vrai</span><span class="sxs-lookup"><span data-stu-id="f1a5f-191">True</span></span>                            |
| <span data-ttu-id="f1a5f-192">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f1a5f-192">Is Indexed</span></span>             | <span data-ttu-id="f1a5f-193">Faux</span><span class="sxs-lookup"><span data-stu-id="f1a5f-193">False</span></span>                           |
| <span data-ttu-id="f1a5f-194">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f1a5f-194">In Global Catalog</span></span>      | <span data-ttu-id="f1a5f-195">Vrai</span><span class="sxs-lookup"><span data-stu-id="f1a5f-195">True</span></span>                            |
| <span data-ttu-id="f1a5f-196">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f1a5f-196">NT-Security-Descriptor</span></span> | <span data-ttu-id="f1a5f-197">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f1a5f-197">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f1a5f-198">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f1a5f-198">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f1a5f-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f1a5f-199">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f1a5f-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f1a5f-200">Search-Flags</span></span>           | <span data-ttu-id="f1a5f-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f1a5f-201">0x00000000</span></span>                      |
| <span data-ttu-id="f1a5f-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f1a5f-202">System-Flags</span></span>           | <span data-ttu-id="f1a5f-203">0x00000013</span><span class="sxs-lookup"><span data-stu-id="f1a5f-203">0x00000013</span></span>                      |
| <span data-ttu-id="f1a5f-204">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f1a5f-204">Classes used in</span></span>        | [<span data-ttu-id="f1a5f-205">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="f1a5f-205">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f1a5f-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f1a5f-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f1a5f-207">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1a5f-207">Entry</span></span> | <span data-ttu-id="f1a5f-208">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1a5f-208">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f1a5f-209">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f1a5f-209">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f1a5f-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f1a5f-210">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f1a5f-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="f1a5f-211">System-Only</span></span>            | <span data-ttu-id="f1a5f-212">Vrai</span><span class="sxs-lookup"><span data-stu-id="f1a5f-212">True</span></span>                            |
| <span data-ttu-id="f1a5f-213">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f1a5f-213">Is-Single-Valued</span></span>       | <span data-ttu-id="f1a5f-214">Vrai</span><span class="sxs-lookup"><span data-stu-id="f1a5f-214">True</span></span>                            |
| <span data-ttu-id="f1a5f-215">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f1a5f-215">Is Indexed</span></span>             | <span data-ttu-id="f1a5f-216">Faux</span><span class="sxs-lookup"><span data-stu-id="f1a5f-216">False</span></span>                           |
| <span data-ttu-id="f1a5f-217">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f1a5f-217">In Global Catalog</span></span>      | <span data-ttu-id="f1a5f-218">Vrai</span><span class="sxs-lookup"><span data-stu-id="f1a5f-218">True</span></span>                            |
| <span data-ttu-id="f1a5f-219">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f1a5f-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="f1a5f-220">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f1a5f-220">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f1a5f-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f1a5f-221">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f1a5f-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f1a5f-222">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f1a5f-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f1a5f-223">Search-Flags</span></span>           | <span data-ttu-id="f1a5f-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f1a5f-224">0x00000000</span></span>                      |
| <span data-ttu-id="f1a5f-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f1a5f-225">System-Flags</span></span>           | <span data-ttu-id="f1a5f-226">0x00000013</span><span class="sxs-lookup"><span data-stu-id="f1a5f-226">0x00000013</span></span>                      |
| <span data-ttu-id="f1a5f-227">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f1a5f-227">Classes used in</span></span>        | [<span data-ttu-id="f1a5f-228">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="f1a5f-228">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f1a5f-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f1a5f-229">Windows Server 2008</span></span>



| <span data-ttu-id="f1a5f-230">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1a5f-230">Entry</span></span> | <span data-ttu-id="f1a5f-231">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1a5f-231">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f1a5f-232">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f1a5f-232">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f1a5f-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f1a5f-233">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f1a5f-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="f1a5f-234">System-Only</span></span>            | <span data-ttu-id="f1a5f-235">Vrai</span><span class="sxs-lookup"><span data-stu-id="f1a5f-235">True</span></span>                            |
| <span data-ttu-id="f1a5f-236">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f1a5f-236">Is-Single-Valued</span></span>       | <span data-ttu-id="f1a5f-237">Vrai</span><span class="sxs-lookup"><span data-stu-id="f1a5f-237">True</span></span>                            |
| <span data-ttu-id="f1a5f-238">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f1a5f-238">Is Indexed</span></span>             | <span data-ttu-id="f1a5f-239">Faux</span><span class="sxs-lookup"><span data-stu-id="f1a5f-239">False</span></span>                           |
| <span data-ttu-id="f1a5f-240">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f1a5f-240">In Global Catalog</span></span>      | <span data-ttu-id="f1a5f-241">Vrai</span><span class="sxs-lookup"><span data-stu-id="f1a5f-241">True</span></span>                            |
| <span data-ttu-id="f1a5f-242">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f1a5f-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="f1a5f-243">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f1a5f-243">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f1a5f-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f1a5f-244">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f1a5f-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f1a5f-245">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f1a5f-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f1a5f-246">Search-Flags</span></span>           | <span data-ttu-id="f1a5f-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f1a5f-247">0x00000000</span></span>                      |
| <span data-ttu-id="f1a5f-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f1a5f-248">System-Flags</span></span>           | <span data-ttu-id="f1a5f-249">0x00000013</span><span class="sxs-lookup"><span data-stu-id="f1a5f-249">0x00000013</span></span>                      |
| <span data-ttu-id="f1a5f-250">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f1a5f-250">Classes used in</span></span>        | [<span data-ttu-id="f1a5f-251">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="f1a5f-251">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f1a5f-252">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f1a5f-252">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f1a5f-253">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1a5f-253">Entry</span></span> | <span data-ttu-id="f1a5f-254">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1a5f-254">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f1a5f-255">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f1a5f-255">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f1a5f-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f1a5f-256">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f1a5f-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="f1a5f-257">System-Only</span></span>            | <span data-ttu-id="f1a5f-258">Vrai</span><span class="sxs-lookup"><span data-stu-id="f1a5f-258">True</span></span>                            |
| <span data-ttu-id="f1a5f-259">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f1a5f-259">Is-Single-Valued</span></span>       | <span data-ttu-id="f1a5f-260">Vrai</span><span class="sxs-lookup"><span data-stu-id="f1a5f-260">True</span></span>                            |
| <span data-ttu-id="f1a5f-261">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f1a5f-261">Is Indexed</span></span>             | <span data-ttu-id="f1a5f-262">Faux</span><span class="sxs-lookup"><span data-stu-id="f1a5f-262">False</span></span>                           |
| <span data-ttu-id="f1a5f-263">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f1a5f-263">In Global Catalog</span></span>      | <span data-ttu-id="f1a5f-264">Vrai</span><span class="sxs-lookup"><span data-stu-id="f1a5f-264">True</span></span>                            |
| <span data-ttu-id="f1a5f-265">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f1a5f-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="f1a5f-266">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f1a5f-266">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f1a5f-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f1a5f-267">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f1a5f-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f1a5f-268">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f1a5f-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f1a5f-269">Search-Flags</span></span>           | <span data-ttu-id="f1a5f-270">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f1a5f-270">0x00000000</span></span>                      |
| <span data-ttu-id="f1a5f-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f1a5f-271">System-Flags</span></span>           | <span data-ttu-id="f1a5f-272">0x00000013</span><span class="sxs-lookup"><span data-stu-id="f1a5f-272">0x00000013</span></span>                      |
| <span data-ttu-id="f1a5f-273">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f1a5f-273">Classes used in</span></span>        | [<span data-ttu-id="f1a5f-274">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="f1a5f-274">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f1a5f-275">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f1a5f-275">Windows Server 2012</span></span>



| <span data-ttu-id="f1a5f-276">Entrée</span><span class="sxs-lookup"><span data-stu-id="f1a5f-276">Entry</span></span> | <span data-ttu-id="f1a5f-277">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1a5f-277">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f1a5f-278">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f1a5f-278">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f1a5f-279">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f1a5f-279">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f1a5f-280">System-Only</span><span class="sxs-lookup"><span data-stu-id="f1a5f-280">System-Only</span></span>            | <span data-ttu-id="f1a5f-281">Vrai</span><span class="sxs-lookup"><span data-stu-id="f1a5f-281">True</span></span>                            |
| <span data-ttu-id="f1a5f-282">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f1a5f-282">Is-Single-Valued</span></span>       | <span data-ttu-id="f1a5f-283">Vrai</span><span class="sxs-lookup"><span data-stu-id="f1a5f-283">True</span></span>                            |
| <span data-ttu-id="f1a5f-284">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f1a5f-284">Is Indexed</span></span>             | <span data-ttu-id="f1a5f-285">Faux</span><span class="sxs-lookup"><span data-stu-id="f1a5f-285">False</span></span>                           |
| <span data-ttu-id="f1a5f-286">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f1a5f-286">In Global Catalog</span></span>      | <span data-ttu-id="f1a5f-287">Vrai</span><span class="sxs-lookup"><span data-stu-id="f1a5f-287">True</span></span>                            |
| <span data-ttu-id="f1a5f-288">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f1a5f-288">NT-Security-Descriptor</span></span> | <span data-ttu-id="f1a5f-289">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f1a5f-289">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f1a5f-290">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f1a5f-290">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f1a5f-291">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f1a5f-291">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f1a5f-292">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f1a5f-292">Search-Flags</span></span>           | <span data-ttu-id="f1a5f-293">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f1a5f-293">0x00000000</span></span>                      |
| <span data-ttu-id="f1a5f-294">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f1a5f-294">System-Flags</span></span>           | <span data-ttu-id="f1a5f-295">0x00000013</span><span class="sxs-lookup"><span data-stu-id="f1a5f-295">0x00000013</span></span>                      |
| <span data-ttu-id="f1a5f-296">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f1a5f-296">Classes used in</span></span>        | [<span data-ttu-id="f1a5f-297">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="f1a5f-297">**Top**</span></span>](c-top.md)<br/> |



 

 





