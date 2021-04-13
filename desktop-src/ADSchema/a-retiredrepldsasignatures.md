---
title: Retirée-REPL-DSA-attribut signatures
description: Effectue le suivi des identités de réplication DS passées d’un contrôleur de domaine donné.
ms.assetid: 82e8b222-5635-41ad-b2ab-386c9e6aa280
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory retirée-REPL-DSA-signatures Attribute
- Schéma AD de l’attribut retiredReplDSASignatures
topic_type:
- apiref
api_name:
- Retired-Repl-DSA-Signatures
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a9a4cb4030a8d3aa24244bc2e7a2702e83686fc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104385431"
---
# <a name="retired-repl-dsa-signatures-attribute"></a><span data-ttu-id="61bdf-105">Retirée-REPL-DSA-attribut signatures</span><span class="sxs-lookup"><span data-stu-id="61bdf-105">Retired-Repl-DSA-Signatures attribute</span></span>

<span data-ttu-id="61bdf-106">Effectue le suivi des identités de réplication DS passées d’un contrôleur de domaine donné.</span><span class="sxs-lookup"><span data-stu-id="61bdf-106">Tracks the past DS replication identities of a given DC.</span></span>



| <span data-ttu-id="61bdf-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="61bdf-107">Entry</span></span> | <span data-ttu-id="61bdf-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="61bdf-108">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="61bdf-109">CN</span><span class="sxs-lookup"><span data-stu-id="61bdf-109">CN</span></span>                | <span data-ttu-id="61bdf-110">Retirée-REPL-DSA-signatures</span><span class="sxs-lookup"><span data-stu-id="61bdf-110">Retired-Repl-DSA-Signatures</span></span>                                                         |
| <span data-ttu-id="61bdf-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="61bdf-111">Ldap-Display-Name</span></span> | <span data-ttu-id="61bdf-112">retiredReplDSASignatures</span><span class="sxs-lookup"><span data-stu-id="61bdf-112">retiredReplDSASignatures</span></span>                                                            |
| <span data-ttu-id="61bdf-113">Taille</span><span class="sxs-lookup"><span data-stu-id="61bdf-113">Size</span></span>              | <span data-ttu-id="61bdf-114">La longueur est proportionnelle au nombre de fois où le DC a été restauré à partir d’une sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="61bdf-114">Length is proportional to the number of times the DC has been restored from backup.</span></span> |
| <span data-ttu-id="61bdf-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="61bdf-115">Update Privilege</span></span>  | <span data-ttu-id="61bdf-116">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="61bdf-116">This value is set by the system.</span></span>                                                    |
| <span data-ttu-id="61bdf-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="61bdf-117">Update Frequency</span></span>  | \-                                                                                  |
| <span data-ttu-id="61bdf-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="61bdf-118">Attribute-Id</span></span>      | <span data-ttu-id="61bdf-119">1.2.840.113556.1.4.673</span><span class="sxs-lookup"><span data-stu-id="61bdf-119">1.2.840.113556.1.4.673</span></span>                                                              |
| <span data-ttu-id="61bdf-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="61bdf-120">System-Id-Guid</span></span>    | <span data-ttu-id="61bdf-121">7bfdcb7f-4807-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="61bdf-121">7bfdcb7f-4807-11d1-a9c3-0000f80367c1</span></span>                                                |
| <span data-ttu-id="61bdf-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="61bdf-122">Syntax</span></span>            | [<span data-ttu-id="61bdf-123">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="61bdf-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                               |



## <a name="implementations"></a><span data-ttu-id="61bdf-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="61bdf-124">Implementations</span></span>

-   [<span data-ttu-id="61bdf-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="61bdf-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="61bdf-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="61bdf-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="61bdf-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="61bdf-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="61bdf-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="61bdf-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="61bdf-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="61bdf-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="61bdf-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="61bdf-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="61bdf-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="61bdf-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="61bdf-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="61bdf-132">Windows 2000 Server</span></span>



| <span data-ttu-id="61bdf-133">Entrée</span><span class="sxs-lookup"><span data-stu-id="61bdf-133">Entry</span></span> | <span data-ttu-id="61bdf-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="61bdf-134">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="61bdf-135">ID de lien</span><span class="sxs-lookup"><span data-stu-id="61bdf-135">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="61bdf-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="61bdf-136">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="61bdf-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="61bdf-137">System-Only</span></span>            | <span data-ttu-id="61bdf-138">Vrai</span><span class="sxs-lookup"><span data-stu-id="61bdf-138">True</span></span>                                     |
| <span data-ttu-id="61bdf-139">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="61bdf-139">Is-Single-Valued</span></span>       | <span data-ttu-id="61bdf-140">Vrai</span><span class="sxs-lookup"><span data-stu-id="61bdf-140">True</span></span>                                     |
| <span data-ttu-id="61bdf-141">Est indexé</span><span class="sxs-lookup"><span data-stu-id="61bdf-141">Is Indexed</span></span>             | <span data-ttu-id="61bdf-142">Faux</span><span class="sxs-lookup"><span data-stu-id="61bdf-142">False</span></span>                                    |
| <span data-ttu-id="61bdf-143">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="61bdf-143">In Global Catalog</span></span>      | <span data-ttu-id="61bdf-144">Faux</span><span class="sxs-lookup"><span data-stu-id="61bdf-144">False</span></span>                                    |
| <span data-ttu-id="61bdf-145">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="61bdf-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="61bdf-146">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="61bdf-146">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="61bdf-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="61bdf-147">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="61bdf-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="61bdf-148">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="61bdf-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="61bdf-149">Search-Flags</span></span>           | <span data-ttu-id="61bdf-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="61bdf-150">0x00000000</span></span>                               |
| <span data-ttu-id="61bdf-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="61bdf-151">System-Flags</span></span>           | <span data-ttu-id="61bdf-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="61bdf-152">0x00000010</span></span>                               |
| <span data-ttu-id="61bdf-153">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="61bdf-153">Classes used in</span></span>        | [<span data-ttu-id="61bdf-154">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="61bdf-154">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="61bdf-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="61bdf-155">Windows Server 2003</span></span>



| <span data-ttu-id="61bdf-156">Entrée</span><span class="sxs-lookup"><span data-stu-id="61bdf-156">Entry</span></span> | <span data-ttu-id="61bdf-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="61bdf-157">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="61bdf-158">ID de lien</span><span class="sxs-lookup"><span data-stu-id="61bdf-158">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="61bdf-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="61bdf-159">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="61bdf-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="61bdf-160">System-Only</span></span>            | <span data-ttu-id="61bdf-161">Vrai</span><span class="sxs-lookup"><span data-stu-id="61bdf-161">True</span></span>                                     |
| <span data-ttu-id="61bdf-162">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="61bdf-162">Is-Single-Valued</span></span>       | <span data-ttu-id="61bdf-163">Vrai</span><span class="sxs-lookup"><span data-stu-id="61bdf-163">True</span></span>                                     |
| <span data-ttu-id="61bdf-164">Est indexé</span><span class="sxs-lookup"><span data-stu-id="61bdf-164">Is Indexed</span></span>             | <span data-ttu-id="61bdf-165">Faux</span><span class="sxs-lookup"><span data-stu-id="61bdf-165">False</span></span>                                    |
| <span data-ttu-id="61bdf-166">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="61bdf-166">In Global Catalog</span></span>      | <span data-ttu-id="61bdf-167">Faux</span><span class="sxs-lookup"><span data-stu-id="61bdf-167">False</span></span>                                    |
| <span data-ttu-id="61bdf-168">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="61bdf-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="61bdf-169">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="61bdf-169">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="61bdf-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="61bdf-170">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="61bdf-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="61bdf-171">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="61bdf-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="61bdf-172">Search-Flags</span></span>           | <span data-ttu-id="61bdf-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="61bdf-173">0x00000000</span></span>                               |
| <span data-ttu-id="61bdf-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="61bdf-174">System-Flags</span></span>           | <span data-ttu-id="61bdf-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="61bdf-175">0x00000010</span></span>                               |
| <span data-ttu-id="61bdf-176">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="61bdf-176">Classes used in</span></span>        | [<span data-ttu-id="61bdf-177">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="61bdf-177">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="adam"></a><span data-ttu-id="61bdf-178">ADAM</span><span class="sxs-lookup"><span data-stu-id="61bdf-178">ADAM</span></span>



| <span data-ttu-id="61bdf-179">Entrée</span><span class="sxs-lookup"><span data-stu-id="61bdf-179">Entry</span></span> | <span data-ttu-id="61bdf-180">Valeur</span><span class="sxs-lookup"><span data-stu-id="61bdf-180">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="61bdf-181">ID de lien</span><span class="sxs-lookup"><span data-stu-id="61bdf-181">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="61bdf-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="61bdf-182">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="61bdf-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="61bdf-183">System-Only</span></span>            | <span data-ttu-id="61bdf-184">Vrai</span><span class="sxs-lookup"><span data-stu-id="61bdf-184">True</span></span>                                     |
| <span data-ttu-id="61bdf-185">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="61bdf-185">Is-Single-Valued</span></span>       | <span data-ttu-id="61bdf-186">Vrai</span><span class="sxs-lookup"><span data-stu-id="61bdf-186">True</span></span>                                     |
| <span data-ttu-id="61bdf-187">Est indexé</span><span class="sxs-lookup"><span data-stu-id="61bdf-187">Is Indexed</span></span>             | <span data-ttu-id="61bdf-188">Faux</span><span class="sxs-lookup"><span data-stu-id="61bdf-188">False</span></span>                                    |
| <span data-ttu-id="61bdf-189">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="61bdf-189">In Global Catalog</span></span>      | <span data-ttu-id="61bdf-190">Faux</span><span class="sxs-lookup"><span data-stu-id="61bdf-190">False</span></span>                                    |
| <span data-ttu-id="61bdf-191">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="61bdf-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="61bdf-192">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="61bdf-192">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="61bdf-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="61bdf-193">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="61bdf-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="61bdf-194">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="61bdf-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="61bdf-195">Search-Flags</span></span>           | <span data-ttu-id="61bdf-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="61bdf-196">0x00000000</span></span>                               |
| <span data-ttu-id="61bdf-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="61bdf-197">System-Flags</span></span>           | <span data-ttu-id="61bdf-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="61bdf-198">0x00000010</span></span>                               |
| <span data-ttu-id="61bdf-199">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="61bdf-199">Classes used in</span></span>        | [<span data-ttu-id="61bdf-200">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="61bdf-200">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="61bdf-201">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="61bdf-201">Windows Server 2003 R2</span></span>



| <span data-ttu-id="61bdf-202">Entrée</span><span class="sxs-lookup"><span data-stu-id="61bdf-202">Entry</span></span> | <span data-ttu-id="61bdf-203">Valeur</span><span class="sxs-lookup"><span data-stu-id="61bdf-203">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="61bdf-204">ID de lien</span><span class="sxs-lookup"><span data-stu-id="61bdf-204">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="61bdf-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="61bdf-205">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="61bdf-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="61bdf-206">System-Only</span></span>            | <span data-ttu-id="61bdf-207">Vrai</span><span class="sxs-lookup"><span data-stu-id="61bdf-207">True</span></span>                                     |
| <span data-ttu-id="61bdf-208">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="61bdf-208">Is-Single-Valued</span></span>       | <span data-ttu-id="61bdf-209">Vrai</span><span class="sxs-lookup"><span data-stu-id="61bdf-209">True</span></span>                                     |
| <span data-ttu-id="61bdf-210">Est indexé</span><span class="sxs-lookup"><span data-stu-id="61bdf-210">Is Indexed</span></span>             | <span data-ttu-id="61bdf-211">Faux</span><span class="sxs-lookup"><span data-stu-id="61bdf-211">False</span></span>                                    |
| <span data-ttu-id="61bdf-212">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="61bdf-212">In Global Catalog</span></span>      | <span data-ttu-id="61bdf-213">Faux</span><span class="sxs-lookup"><span data-stu-id="61bdf-213">False</span></span>                                    |
| <span data-ttu-id="61bdf-214">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="61bdf-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="61bdf-215">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="61bdf-215">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="61bdf-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="61bdf-216">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="61bdf-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="61bdf-217">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="61bdf-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="61bdf-218">Search-Flags</span></span>           | <span data-ttu-id="61bdf-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="61bdf-219">0x00000000</span></span>                               |
| <span data-ttu-id="61bdf-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="61bdf-220">System-Flags</span></span>           | <span data-ttu-id="61bdf-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="61bdf-221">0x00000010</span></span>                               |
| <span data-ttu-id="61bdf-222">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="61bdf-222">Classes used in</span></span>        | [<span data-ttu-id="61bdf-223">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="61bdf-223">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="61bdf-224">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="61bdf-224">Windows Server 2008</span></span>



| <span data-ttu-id="61bdf-225">Entrée</span><span class="sxs-lookup"><span data-stu-id="61bdf-225">Entry</span></span> | <span data-ttu-id="61bdf-226">Valeur</span><span class="sxs-lookup"><span data-stu-id="61bdf-226">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="61bdf-227">ID de lien</span><span class="sxs-lookup"><span data-stu-id="61bdf-227">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="61bdf-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="61bdf-228">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="61bdf-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="61bdf-229">System-Only</span></span>            | <span data-ttu-id="61bdf-230">Vrai</span><span class="sxs-lookup"><span data-stu-id="61bdf-230">True</span></span>                                     |
| <span data-ttu-id="61bdf-231">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="61bdf-231">Is-Single-Valued</span></span>       | <span data-ttu-id="61bdf-232">Vrai</span><span class="sxs-lookup"><span data-stu-id="61bdf-232">True</span></span>                                     |
| <span data-ttu-id="61bdf-233">Est indexé</span><span class="sxs-lookup"><span data-stu-id="61bdf-233">Is Indexed</span></span>             | <span data-ttu-id="61bdf-234">Faux</span><span class="sxs-lookup"><span data-stu-id="61bdf-234">False</span></span>                                    |
| <span data-ttu-id="61bdf-235">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="61bdf-235">In Global Catalog</span></span>      | <span data-ttu-id="61bdf-236">Faux</span><span class="sxs-lookup"><span data-stu-id="61bdf-236">False</span></span>                                    |
| <span data-ttu-id="61bdf-237">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="61bdf-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="61bdf-238">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="61bdf-238">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="61bdf-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="61bdf-239">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="61bdf-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="61bdf-240">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="61bdf-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="61bdf-241">Search-Flags</span></span>           | <span data-ttu-id="61bdf-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="61bdf-242">0x00000000</span></span>                               |
| <span data-ttu-id="61bdf-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="61bdf-243">System-Flags</span></span>           | <span data-ttu-id="61bdf-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="61bdf-244">0x00000010</span></span>                               |
| <span data-ttu-id="61bdf-245">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="61bdf-245">Classes used in</span></span>        | [<span data-ttu-id="61bdf-246">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="61bdf-246">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="61bdf-247">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="61bdf-247">Windows Server 2008 R2</span></span>



| <span data-ttu-id="61bdf-248">Entrée</span><span class="sxs-lookup"><span data-stu-id="61bdf-248">Entry</span></span> | <span data-ttu-id="61bdf-249">Valeur</span><span class="sxs-lookup"><span data-stu-id="61bdf-249">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="61bdf-250">ID de lien</span><span class="sxs-lookup"><span data-stu-id="61bdf-250">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="61bdf-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="61bdf-251">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="61bdf-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="61bdf-252">System-Only</span></span>            | <span data-ttu-id="61bdf-253">Vrai</span><span class="sxs-lookup"><span data-stu-id="61bdf-253">True</span></span>                                     |
| <span data-ttu-id="61bdf-254">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="61bdf-254">Is-Single-Valued</span></span>       | <span data-ttu-id="61bdf-255">Vrai</span><span class="sxs-lookup"><span data-stu-id="61bdf-255">True</span></span>                                     |
| <span data-ttu-id="61bdf-256">Est indexé</span><span class="sxs-lookup"><span data-stu-id="61bdf-256">Is Indexed</span></span>             | <span data-ttu-id="61bdf-257">Faux</span><span class="sxs-lookup"><span data-stu-id="61bdf-257">False</span></span>                                    |
| <span data-ttu-id="61bdf-258">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="61bdf-258">In Global Catalog</span></span>      | <span data-ttu-id="61bdf-259">Faux</span><span class="sxs-lookup"><span data-stu-id="61bdf-259">False</span></span>                                    |
| <span data-ttu-id="61bdf-260">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="61bdf-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="61bdf-261">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="61bdf-261">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="61bdf-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="61bdf-262">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="61bdf-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="61bdf-263">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="61bdf-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="61bdf-264">Search-Flags</span></span>           | <span data-ttu-id="61bdf-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="61bdf-265">0x00000000</span></span>                               |
| <span data-ttu-id="61bdf-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="61bdf-266">System-Flags</span></span>           | <span data-ttu-id="61bdf-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="61bdf-267">0x00000010</span></span>                               |
| <span data-ttu-id="61bdf-268">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="61bdf-268">Classes used in</span></span>        | [<span data-ttu-id="61bdf-269">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="61bdf-269">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="61bdf-270">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="61bdf-270">Windows Server 2012</span></span>



| <span data-ttu-id="61bdf-271">Entrée</span><span class="sxs-lookup"><span data-stu-id="61bdf-271">Entry</span></span> | <span data-ttu-id="61bdf-272">Valeur</span><span class="sxs-lookup"><span data-stu-id="61bdf-272">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="61bdf-273">ID de lien</span><span class="sxs-lookup"><span data-stu-id="61bdf-273">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="61bdf-274">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="61bdf-274">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="61bdf-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="61bdf-275">System-Only</span></span>            | <span data-ttu-id="61bdf-276">Vrai</span><span class="sxs-lookup"><span data-stu-id="61bdf-276">True</span></span>                                     |
| <span data-ttu-id="61bdf-277">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="61bdf-277">Is-Single-Valued</span></span>       | <span data-ttu-id="61bdf-278">Vrai</span><span class="sxs-lookup"><span data-stu-id="61bdf-278">True</span></span>                                     |
| <span data-ttu-id="61bdf-279">Est indexé</span><span class="sxs-lookup"><span data-stu-id="61bdf-279">Is Indexed</span></span>             | <span data-ttu-id="61bdf-280">Faux</span><span class="sxs-lookup"><span data-stu-id="61bdf-280">False</span></span>                                    |
| <span data-ttu-id="61bdf-281">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="61bdf-281">In Global Catalog</span></span>      | <span data-ttu-id="61bdf-282">Faux</span><span class="sxs-lookup"><span data-stu-id="61bdf-282">False</span></span>                                    |
| <span data-ttu-id="61bdf-283">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="61bdf-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="61bdf-284">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="61bdf-284">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="61bdf-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="61bdf-285">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="61bdf-286">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="61bdf-286">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="61bdf-287">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="61bdf-287">Search-Flags</span></span>           | <span data-ttu-id="61bdf-288">0x00000000</span><span class="sxs-lookup"><span data-stu-id="61bdf-288">0x00000000</span></span>                               |
| <span data-ttu-id="61bdf-289">System-Flags</span><span class="sxs-lookup"><span data-stu-id="61bdf-289">System-Flags</span></span>           | <span data-ttu-id="61bdf-290">0x00000010</span><span class="sxs-lookup"><span data-stu-id="61bdf-290">0x00000010</span></span>                               |
| <span data-ttu-id="61bdf-291">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="61bdf-291">Classes used in</span></span>        | [<span data-ttu-id="61bdf-292">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="61bdf-292">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





