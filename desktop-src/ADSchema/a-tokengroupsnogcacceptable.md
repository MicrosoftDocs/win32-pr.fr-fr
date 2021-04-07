---
title: Token-Groups-no-GC-attribut acceptable
description: Cet attribut contient la liste des SID en raison d’une opération d’extension d’appartenance de groupe transitive sur un utilisateur ou un ordinateur donné. Les groupes de jetons ne peuvent pas être récupérés si aucun catalogue global n’est présent pour récupérer les appartenances indirectes transitives.
ms.assetid: 08718c69-6339-40dc-8486-a7cd72028ed1
ms.tgt_platform: multiple
keywords:
- Jeton-Groups-no-GC-attribut acceptable-schéma AD
- Schéma AD de l’attribut tokenGroupsNoGCAcceptable
topic_type:
- apiref
api_name:
- Token-Groups-No-GC-Acceptable
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a87c4b8996586c8c35ed4c815b954dad02b5db03
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103844902"
---
# <a name="token-groups-no-gc-acceptable-attribute"></a><span data-ttu-id="36cd3-106">Token-Groups-no-GC-attribut acceptable</span><span class="sxs-lookup"><span data-stu-id="36cd3-106">Token-Groups-No-GC-Acceptable attribute</span></span>

<span data-ttu-id="36cd3-107">Cet attribut contient la liste des SID en raison d’une opération d’extension d’appartenance de groupe transitive sur un utilisateur ou un ordinateur donné.</span><span class="sxs-lookup"><span data-stu-id="36cd3-107">This attribute contains the list of SIDs due to a transitive group membership expansion operation on a given user or computer.</span></span> <span data-ttu-id="36cd3-108">Les groupes de jetons ne peuvent pas être récupérés si aucun catalogue global n’est présent pour récupérer les appartenances indirectes transitives.</span><span class="sxs-lookup"><span data-stu-id="36cd3-108">Token groups cannot be retrieved if a Global Catalog is not present to retrieve the transitive reverse memberships.</span></span>



| <span data-ttu-id="36cd3-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="36cd3-109">Entry</span></span> | <span data-ttu-id="36cd3-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="36cd3-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="36cd3-111">CN</span><span class="sxs-lookup"><span data-stu-id="36cd3-111">CN</span></span>                | <span data-ttu-id="36cd3-112">Token-Groups-non-GC-acceptable</span><span class="sxs-lookup"><span data-stu-id="36cd3-112">Token-Groups-No-GC-Acceptable</span></span>        |
| <span data-ttu-id="36cd3-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="36cd3-113">Ldap-Display-Name</span></span> | <span data-ttu-id="36cd3-114">tokenGroupsNoGCAcceptable</span><span class="sxs-lookup"><span data-stu-id="36cd3-114">tokenGroupsNoGCAcceptable</span></span>            |
| <span data-ttu-id="36cd3-115">Taille</span><span class="sxs-lookup"><span data-stu-id="36cd3-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="36cd3-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="36cd3-116">Update Privilege</span></span>  | <span data-ttu-id="36cd3-117">Le système définit cette valeur.</span><span class="sxs-lookup"><span data-stu-id="36cd3-117">The system sets this value.</span></span>          |
| <span data-ttu-id="36cd3-118">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="36cd3-118">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="36cd3-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="36cd3-119">Attribute-Id</span></span>      | <span data-ttu-id="36cd3-120">1.2.840.113556.1.4.1303</span><span class="sxs-lookup"><span data-stu-id="36cd3-120">1.2.840.113556.1.4.1303</span></span>              |
| <span data-ttu-id="36cd3-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="36cd3-121">System-Id-Guid</span></span>    | <span data-ttu-id="36cd3-122">040fc392-33df-11d2-98b2-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="36cd3-122">040fc392-33df-11d2-98b2-0000f87a57d4</span></span> |
| <span data-ttu-id="36cd3-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="36cd3-123">Syntax</span></span>            | [<span data-ttu-id="36cd3-124">**Chaîne (SID)**</span><span class="sxs-lookup"><span data-stu-id="36cd3-124">**String(Sid)**</span></span>](s-string-sid.md)  |



## <a name="implementations"></a><span data-ttu-id="36cd3-125">Implémentations</span><span class="sxs-lookup"><span data-stu-id="36cd3-125">Implementations</span></span>

-   [<span data-ttu-id="36cd3-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="36cd3-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="36cd3-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="36cd3-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="36cd3-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="36cd3-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="36cd3-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="36cd3-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="36cd3-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="36cd3-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="36cd3-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="36cd3-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="36cd3-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="36cd3-132">Windows 2000 Server</span></span>



| <span data-ttu-id="36cd3-133">Entrée</span><span class="sxs-lookup"><span data-stu-id="36cd3-133">Entry</span></span> | <span data-ttu-id="36cd3-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="36cd3-134">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="36cd3-135">ID de lien</span><span class="sxs-lookup"><span data-stu-id="36cd3-135">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="36cd3-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="36cd3-136">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="36cd3-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="36cd3-137">System-Only</span></span>            | <span data-ttu-id="36cd3-138">Faux</span><span class="sxs-lookup"><span data-stu-id="36cd3-138">False</span></span>                                                        |
| <span data-ttu-id="36cd3-139">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="36cd3-139">Is-Single-Valued</span></span>       | <span data-ttu-id="36cd3-140">Faux</span><span class="sxs-lookup"><span data-stu-id="36cd3-140">False</span></span>                                                        |
| <span data-ttu-id="36cd3-141">Est indexé</span><span class="sxs-lookup"><span data-stu-id="36cd3-141">Is Indexed</span></span>             | <span data-ttu-id="36cd3-142">Faux</span><span class="sxs-lookup"><span data-stu-id="36cd3-142">False</span></span>                                                        |
| <span data-ttu-id="36cd3-143">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="36cd3-143">In Global Catalog</span></span>      | <span data-ttu-id="36cd3-144">Faux</span><span class="sxs-lookup"><span data-stu-id="36cd3-144">False</span></span>                                                        |
| <span data-ttu-id="36cd3-145">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="36cd3-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="36cd3-146">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="36cd3-146">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="36cd3-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="36cd3-147">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="36cd3-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="36cd3-148">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="36cd3-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="36cd3-149">Search-Flags</span></span>           | <span data-ttu-id="36cd3-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="36cd3-150">0x00000000</span></span>                                                   |
| <span data-ttu-id="36cd3-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="36cd3-151">System-Flags</span></span>           | <span data-ttu-id="36cd3-152">0x08000014</span><span class="sxs-lookup"><span data-stu-id="36cd3-152">0x08000014</span></span>                                                   |
| <span data-ttu-id="36cd3-153">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="36cd3-153">Classes used in</span></span>        | [<span data-ttu-id="36cd3-154">**Sécurité-principal**</span><span class="sxs-lookup"><span data-stu-id="36cd3-154">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="36cd3-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="36cd3-155">Windows Server 2003</span></span>



| <span data-ttu-id="36cd3-156">Entrée</span><span class="sxs-lookup"><span data-stu-id="36cd3-156">Entry</span></span> | <span data-ttu-id="36cd3-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="36cd3-157">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="36cd3-158">ID de lien</span><span class="sxs-lookup"><span data-stu-id="36cd3-158">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="36cd3-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="36cd3-159">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="36cd3-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="36cd3-160">System-Only</span></span>            | <span data-ttu-id="36cd3-161">Faux</span><span class="sxs-lookup"><span data-stu-id="36cd3-161">False</span></span>                                                        |
| <span data-ttu-id="36cd3-162">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="36cd3-162">Is-Single-Valued</span></span>       | <span data-ttu-id="36cd3-163">Faux</span><span class="sxs-lookup"><span data-stu-id="36cd3-163">False</span></span>                                                        |
| <span data-ttu-id="36cd3-164">Est indexé</span><span class="sxs-lookup"><span data-stu-id="36cd3-164">Is Indexed</span></span>             | <span data-ttu-id="36cd3-165">Faux</span><span class="sxs-lookup"><span data-stu-id="36cd3-165">False</span></span>                                                        |
| <span data-ttu-id="36cd3-166">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="36cd3-166">In Global Catalog</span></span>      | <span data-ttu-id="36cd3-167">Faux</span><span class="sxs-lookup"><span data-stu-id="36cd3-167">False</span></span>                                                        |
| <span data-ttu-id="36cd3-168">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="36cd3-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="36cd3-169">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="36cd3-169">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="36cd3-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="36cd3-170">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="36cd3-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="36cd3-171">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="36cd3-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="36cd3-172">Search-Flags</span></span>           | <span data-ttu-id="36cd3-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="36cd3-173">0x00000000</span></span>                                                   |
| <span data-ttu-id="36cd3-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="36cd3-174">System-Flags</span></span>           | <span data-ttu-id="36cd3-175">0x08000014</span><span class="sxs-lookup"><span data-stu-id="36cd3-175">0x08000014</span></span>                                                   |
| <span data-ttu-id="36cd3-176">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="36cd3-176">Classes used in</span></span>        | [<span data-ttu-id="36cd3-177">**Sécurité-principal**</span><span class="sxs-lookup"><span data-stu-id="36cd3-177">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="36cd3-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="36cd3-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="36cd3-179">Entrée</span><span class="sxs-lookup"><span data-stu-id="36cd3-179">Entry</span></span> | <span data-ttu-id="36cd3-180">Valeur</span><span class="sxs-lookup"><span data-stu-id="36cd3-180">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="36cd3-181">ID de lien</span><span class="sxs-lookup"><span data-stu-id="36cd3-181">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="36cd3-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="36cd3-182">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="36cd3-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="36cd3-183">System-Only</span></span>            | <span data-ttu-id="36cd3-184">Faux</span><span class="sxs-lookup"><span data-stu-id="36cd3-184">False</span></span>                                                        |
| <span data-ttu-id="36cd3-185">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="36cd3-185">Is-Single-Valued</span></span>       | <span data-ttu-id="36cd3-186">Faux</span><span class="sxs-lookup"><span data-stu-id="36cd3-186">False</span></span>                                                        |
| <span data-ttu-id="36cd3-187">Est indexé</span><span class="sxs-lookup"><span data-stu-id="36cd3-187">Is Indexed</span></span>             | <span data-ttu-id="36cd3-188">Faux</span><span class="sxs-lookup"><span data-stu-id="36cd3-188">False</span></span>                                                        |
| <span data-ttu-id="36cd3-189">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="36cd3-189">In Global Catalog</span></span>      | <span data-ttu-id="36cd3-190">Faux</span><span class="sxs-lookup"><span data-stu-id="36cd3-190">False</span></span>                                                        |
| <span data-ttu-id="36cd3-191">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="36cd3-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="36cd3-192">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="36cd3-192">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="36cd3-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="36cd3-193">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="36cd3-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="36cd3-194">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="36cd3-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="36cd3-195">Search-Flags</span></span>           | <span data-ttu-id="36cd3-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="36cd3-196">0x00000000</span></span>                                                   |
| <span data-ttu-id="36cd3-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="36cd3-197">System-Flags</span></span>           | <span data-ttu-id="36cd3-198">0x08000014</span><span class="sxs-lookup"><span data-stu-id="36cd3-198">0x08000014</span></span>                                                   |
| <span data-ttu-id="36cd3-199">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="36cd3-199">Classes used in</span></span>        | [<span data-ttu-id="36cd3-200">**Sécurité-principal**</span><span class="sxs-lookup"><span data-stu-id="36cd3-200">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="36cd3-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="36cd3-201">Windows Server 2008</span></span>



| <span data-ttu-id="36cd3-202">Entrée</span><span class="sxs-lookup"><span data-stu-id="36cd3-202">Entry</span></span> | <span data-ttu-id="36cd3-203">Valeur</span><span class="sxs-lookup"><span data-stu-id="36cd3-203">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="36cd3-204">ID de lien</span><span class="sxs-lookup"><span data-stu-id="36cd3-204">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="36cd3-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="36cd3-205">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="36cd3-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="36cd3-206">System-Only</span></span>            | <span data-ttu-id="36cd3-207">Faux</span><span class="sxs-lookup"><span data-stu-id="36cd3-207">False</span></span>                                                        |
| <span data-ttu-id="36cd3-208">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="36cd3-208">Is-Single-Valued</span></span>       | <span data-ttu-id="36cd3-209">Faux</span><span class="sxs-lookup"><span data-stu-id="36cd3-209">False</span></span>                                                        |
| <span data-ttu-id="36cd3-210">Est indexé</span><span class="sxs-lookup"><span data-stu-id="36cd3-210">Is Indexed</span></span>             | <span data-ttu-id="36cd3-211">Faux</span><span class="sxs-lookup"><span data-stu-id="36cd3-211">False</span></span>                                                        |
| <span data-ttu-id="36cd3-212">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="36cd3-212">In Global Catalog</span></span>      | <span data-ttu-id="36cd3-213">Faux</span><span class="sxs-lookup"><span data-stu-id="36cd3-213">False</span></span>                                                        |
| <span data-ttu-id="36cd3-214">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="36cd3-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="36cd3-215">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="36cd3-215">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="36cd3-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="36cd3-216">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="36cd3-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="36cd3-217">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="36cd3-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="36cd3-218">Search-Flags</span></span>           | <span data-ttu-id="36cd3-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="36cd3-219">0x00000000</span></span>                                                   |
| <span data-ttu-id="36cd3-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="36cd3-220">System-Flags</span></span>           | <span data-ttu-id="36cd3-221">0x08000014</span><span class="sxs-lookup"><span data-stu-id="36cd3-221">0x08000014</span></span>                                                   |
| <span data-ttu-id="36cd3-222">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="36cd3-222">Classes used in</span></span>        | [<span data-ttu-id="36cd3-223">**Sécurité-principal**</span><span class="sxs-lookup"><span data-stu-id="36cd3-223">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="36cd3-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="36cd3-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="36cd3-225">Entrée</span><span class="sxs-lookup"><span data-stu-id="36cd3-225">Entry</span></span> | <span data-ttu-id="36cd3-226">Valeur</span><span class="sxs-lookup"><span data-stu-id="36cd3-226">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="36cd3-227">ID de lien</span><span class="sxs-lookup"><span data-stu-id="36cd3-227">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="36cd3-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="36cd3-228">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="36cd3-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="36cd3-229">System-Only</span></span>            | <span data-ttu-id="36cd3-230">Faux</span><span class="sxs-lookup"><span data-stu-id="36cd3-230">False</span></span>                                                        |
| <span data-ttu-id="36cd3-231">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="36cd3-231">Is-Single-Valued</span></span>       | <span data-ttu-id="36cd3-232">Faux</span><span class="sxs-lookup"><span data-stu-id="36cd3-232">False</span></span>                                                        |
| <span data-ttu-id="36cd3-233">Est indexé</span><span class="sxs-lookup"><span data-stu-id="36cd3-233">Is Indexed</span></span>             | <span data-ttu-id="36cd3-234">Faux</span><span class="sxs-lookup"><span data-stu-id="36cd3-234">False</span></span>                                                        |
| <span data-ttu-id="36cd3-235">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="36cd3-235">In Global Catalog</span></span>      | <span data-ttu-id="36cd3-236">Faux</span><span class="sxs-lookup"><span data-stu-id="36cd3-236">False</span></span>                                                        |
| <span data-ttu-id="36cd3-237">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="36cd3-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="36cd3-238">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="36cd3-238">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="36cd3-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="36cd3-239">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="36cd3-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="36cd3-240">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="36cd3-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="36cd3-241">Search-Flags</span></span>           | <span data-ttu-id="36cd3-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="36cd3-242">0x00000000</span></span>                                                   |
| <span data-ttu-id="36cd3-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="36cd3-243">System-Flags</span></span>           | <span data-ttu-id="36cd3-244">0x08000014</span><span class="sxs-lookup"><span data-stu-id="36cd3-244">0x08000014</span></span>                                                   |
| <span data-ttu-id="36cd3-245">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="36cd3-245">Classes used in</span></span>        | [<span data-ttu-id="36cd3-246">**Sécurité-principal**</span><span class="sxs-lookup"><span data-stu-id="36cd3-246">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="36cd3-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="36cd3-247">Windows Server 2012</span></span>



| <span data-ttu-id="36cd3-248">Entrée</span><span class="sxs-lookup"><span data-stu-id="36cd3-248">Entry</span></span> | <span data-ttu-id="36cd3-249">Valeur</span><span class="sxs-lookup"><span data-stu-id="36cd3-249">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="36cd3-250">ID de lien</span><span class="sxs-lookup"><span data-stu-id="36cd3-250">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="36cd3-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="36cd3-251">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="36cd3-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="36cd3-252">System-Only</span></span>            | <span data-ttu-id="36cd3-253">Faux</span><span class="sxs-lookup"><span data-stu-id="36cd3-253">False</span></span>                                                        |
| <span data-ttu-id="36cd3-254">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="36cd3-254">Is-Single-Valued</span></span>       | <span data-ttu-id="36cd3-255">Faux</span><span class="sxs-lookup"><span data-stu-id="36cd3-255">False</span></span>                                                        |
| <span data-ttu-id="36cd3-256">Est indexé</span><span class="sxs-lookup"><span data-stu-id="36cd3-256">Is Indexed</span></span>             | <span data-ttu-id="36cd3-257">Faux</span><span class="sxs-lookup"><span data-stu-id="36cd3-257">False</span></span>                                                        |
| <span data-ttu-id="36cd3-258">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="36cd3-258">In Global Catalog</span></span>      | <span data-ttu-id="36cd3-259">Faux</span><span class="sxs-lookup"><span data-stu-id="36cd3-259">False</span></span>                                                        |
| <span data-ttu-id="36cd3-260">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="36cd3-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="36cd3-261">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="36cd3-261">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="36cd3-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="36cd3-262">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="36cd3-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="36cd3-263">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="36cd3-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="36cd3-264">Search-Flags</span></span>           | <span data-ttu-id="36cd3-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="36cd3-265">0x00000000</span></span>                                                   |
| <span data-ttu-id="36cd3-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="36cd3-266">System-Flags</span></span>           | <span data-ttu-id="36cd3-267">0x08000014</span><span class="sxs-lookup"><span data-stu-id="36cd3-267">0x08000014</span></span>                                                   |
| <span data-ttu-id="36cd3-268">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="36cd3-268">Classes used in</span></span>        | [<span data-ttu-id="36cd3-269">**Sécurité-principal**</span><span class="sxs-lookup"><span data-stu-id="36cd3-269">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



 

 





