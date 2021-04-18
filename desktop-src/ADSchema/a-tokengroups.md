---
title: Attribut Token-Groups
description: Attribut calculé qui contient la liste des SID en raison d’une opération d’expansion d’appartenance de groupe transitive sur un utilisateur ou un ordinateur donné. Les groupes de jetons ne peuvent pas être récupérés si aucun catalogue global n’est présent pour récupérer les appartenances de contrepassation transitives.
ms.assetid: bb430c9f-20b7-4f21-804d-fbd4864b6505
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Token-Groups
- Schéma AD de l’attribut tokenGroups
topic_type:
- apiref
api_name:
- Token-Groups
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5342d1ff2bf549796340532b0514d5c5b060c2c1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106533578"
---
# <a name="token-groups-attribute"></a><span data-ttu-id="6f652-106">Attribut Token-Groups</span><span class="sxs-lookup"><span data-stu-id="6f652-106">Token-Groups attribute</span></span>

<span data-ttu-id="6f652-107">Attribut calculé qui contient la liste des SID en raison d’une opération d’expansion d’appartenance de groupe transitive sur un utilisateur ou un ordinateur donné.</span><span class="sxs-lookup"><span data-stu-id="6f652-107">A computed attribute that contains the list of SIDs due to a transitive group membership expansion operation on a given user or computer.</span></span> <span data-ttu-id="6f652-108">Les groupes de jetons ne peuvent pas être récupérés si aucun catalogue global n’est présent pour récupérer les appartenances de contrepassation transitives.</span><span class="sxs-lookup"><span data-stu-id="6f652-108">Token Groups cannot be retrieved if no Global Catalog is present to retrieve the transitive reverse memberships.</span></span>



| <span data-ttu-id="6f652-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="6f652-109">Entry</span></span> | <span data-ttu-id="6f652-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="6f652-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="6f652-111">CN</span><span class="sxs-lookup"><span data-stu-id="6f652-111">CN</span></span>                | <span data-ttu-id="6f652-112">Token-Groups</span><span class="sxs-lookup"><span data-stu-id="6f652-112">Token-Groups</span></span>                         |
| <span data-ttu-id="6f652-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="6f652-113">Ldap-Display-Name</span></span> | <span data-ttu-id="6f652-114">tokenGroups</span><span class="sxs-lookup"><span data-stu-id="6f652-114">tokenGroups</span></span>                          |
| <span data-ttu-id="6f652-115">Taille</span><span class="sxs-lookup"><span data-stu-id="6f652-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="6f652-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="6f652-116">Update Privilege</span></span>  | <span data-ttu-id="6f652-117">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="6f652-117">This value is set by the system.</span></span>     |
| <span data-ttu-id="6f652-118">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="6f652-118">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="6f652-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6f652-119">Attribute-Id</span></span>      | <span data-ttu-id="6f652-120">1.2.840.113556.1.4.1301</span><span class="sxs-lookup"><span data-stu-id="6f652-120">1.2.840.113556.1.4.1301</span></span>              |
| <span data-ttu-id="6f652-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="6f652-121">System-Id-Guid</span></span>    | <span data-ttu-id="6f652-122">b7c69e6d-2cc7-11d2-854e-00a0c983f608</span><span class="sxs-lookup"><span data-stu-id="6f652-122">b7c69e6d-2cc7-11d2-854e-00a0c983f608</span></span> |
| <span data-ttu-id="6f652-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6f652-123">Syntax</span></span>            | [<span data-ttu-id="6f652-124">**Chaîne (SID)**</span><span class="sxs-lookup"><span data-stu-id="6f652-124">**String(Sid)**</span></span>](s-string-sid.md)  |



## <a name="implementations"></a><span data-ttu-id="6f652-125">Implémentations</span><span class="sxs-lookup"><span data-stu-id="6f652-125">Implementations</span></span>

-   [<span data-ttu-id="6f652-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6f652-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6f652-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6f652-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6f652-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="6f652-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="6f652-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6f652-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6f652-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6f652-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6f652-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6f652-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6f652-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6f652-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6f652-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6f652-133">Windows 2000 Server</span></span>



| <span data-ttu-id="6f652-134">Entrée</span><span class="sxs-lookup"><span data-stu-id="6f652-134">Entry</span></span> | <span data-ttu-id="6f652-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="6f652-135">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="6f652-136">ID de lien</span><span class="sxs-lookup"><span data-stu-id="6f652-136">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="6f652-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6f652-137">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="6f652-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="6f652-138">System-Only</span></span>            | <span data-ttu-id="6f652-139">Faux</span><span class="sxs-lookup"><span data-stu-id="6f652-139">False</span></span>                                                        |
| <span data-ttu-id="6f652-140">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="6f652-140">Is-Single-Valued</span></span>       | <span data-ttu-id="6f652-141">Faux</span><span class="sxs-lookup"><span data-stu-id="6f652-141">False</span></span>                                                        |
| <span data-ttu-id="6f652-142">Est indexé</span><span class="sxs-lookup"><span data-stu-id="6f652-142">Is Indexed</span></span>             | <span data-ttu-id="6f652-143">Faux</span><span class="sxs-lookup"><span data-stu-id="6f652-143">False</span></span>                                                        |
| <span data-ttu-id="6f652-144">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="6f652-144">In Global Catalog</span></span>      | <span data-ttu-id="6f652-145">Faux</span><span class="sxs-lookup"><span data-stu-id="6f652-145">False</span></span>                                                        |
| <span data-ttu-id="6f652-146">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="6f652-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="6f652-147">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="6f652-147">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="6f652-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6f652-148">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="6f652-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6f652-149">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="6f652-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6f652-150">Search-Flags</span></span>           | <span data-ttu-id="6f652-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6f652-151">0x00000000</span></span>                                                   |
| <span data-ttu-id="6f652-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6f652-152">System-Flags</span></span>           | <span data-ttu-id="6f652-153">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6f652-153">0x08000014</span></span>                                                   |
| <span data-ttu-id="6f652-154">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="6f652-154">Classes used in</span></span>        | [<span data-ttu-id="6f652-155">**Sécurité-principal**</span><span class="sxs-lookup"><span data-stu-id="6f652-155">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6f652-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6f652-156">Windows Server 2003</span></span>



| <span data-ttu-id="6f652-157">Entrée</span><span class="sxs-lookup"><span data-stu-id="6f652-157">Entry</span></span> | <span data-ttu-id="6f652-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="6f652-158">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="6f652-159">ID de lien</span><span class="sxs-lookup"><span data-stu-id="6f652-159">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="6f652-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6f652-160">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="6f652-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="6f652-161">System-Only</span></span>            | <span data-ttu-id="6f652-162">Faux</span><span class="sxs-lookup"><span data-stu-id="6f652-162">False</span></span>                                                        |
| <span data-ttu-id="6f652-163">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="6f652-163">Is-Single-Valued</span></span>       | <span data-ttu-id="6f652-164">Faux</span><span class="sxs-lookup"><span data-stu-id="6f652-164">False</span></span>                                                        |
| <span data-ttu-id="6f652-165">Est indexé</span><span class="sxs-lookup"><span data-stu-id="6f652-165">Is Indexed</span></span>             | <span data-ttu-id="6f652-166">Faux</span><span class="sxs-lookup"><span data-stu-id="6f652-166">False</span></span>                                                        |
| <span data-ttu-id="6f652-167">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="6f652-167">In Global Catalog</span></span>      | <span data-ttu-id="6f652-168">Faux</span><span class="sxs-lookup"><span data-stu-id="6f652-168">False</span></span>                                                        |
| <span data-ttu-id="6f652-169">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="6f652-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="6f652-170">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="6f652-170">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="6f652-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6f652-171">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="6f652-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6f652-172">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="6f652-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6f652-173">Search-Flags</span></span>           | <span data-ttu-id="6f652-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6f652-174">0x00000000</span></span>                                                   |
| <span data-ttu-id="6f652-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6f652-175">System-Flags</span></span>           | <span data-ttu-id="6f652-176">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6f652-176">0x08000014</span></span>                                                   |
| <span data-ttu-id="6f652-177">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="6f652-177">Classes used in</span></span>        | [<span data-ttu-id="6f652-178">**Sécurité-principal**</span><span class="sxs-lookup"><span data-stu-id="6f652-178">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="adam"></a><span data-ttu-id="6f652-179">ADAM</span><span class="sxs-lookup"><span data-stu-id="6f652-179">ADAM</span></span>



| <span data-ttu-id="6f652-180">Entrée</span><span class="sxs-lookup"><span data-stu-id="6f652-180">Entry</span></span> | <span data-ttu-id="6f652-181">Valeur</span><span class="sxs-lookup"><span data-stu-id="6f652-181">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="6f652-182">ID de lien</span><span class="sxs-lookup"><span data-stu-id="6f652-182">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="6f652-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6f652-183">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="6f652-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="6f652-184">System-Only</span></span>            | <span data-ttu-id="6f652-185">Faux</span><span class="sxs-lookup"><span data-stu-id="6f652-185">False</span></span>                                                        |
| <span data-ttu-id="6f652-186">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="6f652-186">Is-Single-Valued</span></span>       | <span data-ttu-id="6f652-187">Faux</span><span class="sxs-lookup"><span data-stu-id="6f652-187">False</span></span>                                                        |
| <span data-ttu-id="6f652-188">Est indexé</span><span class="sxs-lookup"><span data-stu-id="6f652-188">Is Indexed</span></span>             | <span data-ttu-id="6f652-189">Faux</span><span class="sxs-lookup"><span data-stu-id="6f652-189">False</span></span>                                                        |
| <span data-ttu-id="6f652-190">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="6f652-190">In Global Catalog</span></span>      | <span data-ttu-id="6f652-191">Faux</span><span class="sxs-lookup"><span data-stu-id="6f652-191">False</span></span>                                                        |
| <span data-ttu-id="6f652-192">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="6f652-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="6f652-193">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="6f652-193">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="6f652-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6f652-194">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="6f652-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6f652-195">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="6f652-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6f652-196">Search-Flags</span></span>           | <span data-ttu-id="6f652-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6f652-197">0x00000000</span></span>                                                   |
| <span data-ttu-id="6f652-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6f652-198">System-Flags</span></span>           | <span data-ttu-id="6f652-199">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6f652-199">0x08000014</span></span>                                                   |
| <span data-ttu-id="6f652-200">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="6f652-200">Classes used in</span></span>        | [<span data-ttu-id="6f652-201">**Sécurité-principal**</span><span class="sxs-lookup"><span data-stu-id="6f652-201">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6f652-202">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6f652-202">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6f652-203">Entrée</span><span class="sxs-lookup"><span data-stu-id="6f652-203">Entry</span></span> | <span data-ttu-id="6f652-204">Valeur</span><span class="sxs-lookup"><span data-stu-id="6f652-204">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="6f652-205">ID de lien</span><span class="sxs-lookup"><span data-stu-id="6f652-205">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="6f652-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6f652-206">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="6f652-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="6f652-207">System-Only</span></span>            | <span data-ttu-id="6f652-208">Faux</span><span class="sxs-lookup"><span data-stu-id="6f652-208">False</span></span>                                                        |
| <span data-ttu-id="6f652-209">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="6f652-209">Is-Single-Valued</span></span>       | <span data-ttu-id="6f652-210">Faux</span><span class="sxs-lookup"><span data-stu-id="6f652-210">False</span></span>                                                        |
| <span data-ttu-id="6f652-211">Est indexé</span><span class="sxs-lookup"><span data-stu-id="6f652-211">Is Indexed</span></span>             | <span data-ttu-id="6f652-212">Faux</span><span class="sxs-lookup"><span data-stu-id="6f652-212">False</span></span>                                                        |
| <span data-ttu-id="6f652-213">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="6f652-213">In Global Catalog</span></span>      | <span data-ttu-id="6f652-214">Faux</span><span class="sxs-lookup"><span data-stu-id="6f652-214">False</span></span>                                                        |
| <span data-ttu-id="6f652-215">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="6f652-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="6f652-216">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="6f652-216">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="6f652-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6f652-217">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="6f652-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6f652-218">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="6f652-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6f652-219">Search-Flags</span></span>           | <span data-ttu-id="6f652-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6f652-220">0x00000000</span></span>                                                   |
| <span data-ttu-id="6f652-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6f652-221">System-Flags</span></span>           | <span data-ttu-id="6f652-222">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6f652-222">0x08000014</span></span>                                                   |
| <span data-ttu-id="6f652-223">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="6f652-223">Classes used in</span></span>        | [<span data-ttu-id="6f652-224">**Sécurité-principal**</span><span class="sxs-lookup"><span data-stu-id="6f652-224">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6f652-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6f652-225">Windows Server 2008</span></span>



| <span data-ttu-id="6f652-226">Entrée</span><span class="sxs-lookup"><span data-stu-id="6f652-226">Entry</span></span> | <span data-ttu-id="6f652-227">Valeur</span><span class="sxs-lookup"><span data-stu-id="6f652-227">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="6f652-228">ID de lien</span><span class="sxs-lookup"><span data-stu-id="6f652-228">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="6f652-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6f652-229">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="6f652-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="6f652-230">System-Only</span></span>            | <span data-ttu-id="6f652-231">Faux</span><span class="sxs-lookup"><span data-stu-id="6f652-231">False</span></span>                                                        |
| <span data-ttu-id="6f652-232">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="6f652-232">Is-Single-Valued</span></span>       | <span data-ttu-id="6f652-233">Faux</span><span class="sxs-lookup"><span data-stu-id="6f652-233">False</span></span>                                                        |
| <span data-ttu-id="6f652-234">Est indexé</span><span class="sxs-lookup"><span data-stu-id="6f652-234">Is Indexed</span></span>             | <span data-ttu-id="6f652-235">Faux</span><span class="sxs-lookup"><span data-stu-id="6f652-235">False</span></span>                                                        |
| <span data-ttu-id="6f652-236">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="6f652-236">In Global Catalog</span></span>      | <span data-ttu-id="6f652-237">Faux</span><span class="sxs-lookup"><span data-stu-id="6f652-237">False</span></span>                                                        |
| <span data-ttu-id="6f652-238">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="6f652-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="6f652-239">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="6f652-239">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="6f652-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6f652-240">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="6f652-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6f652-241">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="6f652-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6f652-242">Search-Flags</span></span>           | <span data-ttu-id="6f652-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6f652-243">0x00000000</span></span>                                                   |
| <span data-ttu-id="6f652-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6f652-244">System-Flags</span></span>           | <span data-ttu-id="6f652-245">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6f652-245">0x08000014</span></span>                                                   |
| <span data-ttu-id="6f652-246">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="6f652-246">Classes used in</span></span>        | [<span data-ttu-id="6f652-247">**Sécurité-principal**</span><span class="sxs-lookup"><span data-stu-id="6f652-247">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6f652-248">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6f652-248">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6f652-249">Entrée</span><span class="sxs-lookup"><span data-stu-id="6f652-249">Entry</span></span> | <span data-ttu-id="6f652-250">Valeur</span><span class="sxs-lookup"><span data-stu-id="6f652-250">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="6f652-251">ID de lien</span><span class="sxs-lookup"><span data-stu-id="6f652-251">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="6f652-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6f652-252">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="6f652-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="6f652-253">System-Only</span></span>            | <span data-ttu-id="6f652-254">Faux</span><span class="sxs-lookup"><span data-stu-id="6f652-254">False</span></span>                                                        |
| <span data-ttu-id="6f652-255">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="6f652-255">Is-Single-Valued</span></span>       | <span data-ttu-id="6f652-256">Faux</span><span class="sxs-lookup"><span data-stu-id="6f652-256">False</span></span>                                                        |
| <span data-ttu-id="6f652-257">Est indexé</span><span class="sxs-lookup"><span data-stu-id="6f652-257">Is Indexed</span></span>             | <span data-ttu-id="6f652-258">Faux</span><span class="sxs-lookup"><span data-stu-id="6f652-258">False</span></span>                                                        |
| <span data-ttu-id="6f652-259">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="6f652-259">In Global Catalog</span></span>      | <span data-ttu-id="6f652-260">Faux</span><span class="sxs-lookup"><span data-stu-id="6f652-260">False</span></span>                                                        |
| <span data-ttu-id="6f652-261">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="6f652-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="6f652-262">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="6f652-262">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="6f652-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6f652-263">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="6f652-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6f652-264">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="6f652-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6f652-265">Search-Flags</span></span>           | <span data-ttu-id="6f652-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6f652-266">0x00000000</span></span>                                                   |
| <span data-ttu-id="6f652-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6f652-267">System-Flags</span></span>           | <span data-ttu-id="6f652-268">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6f652-268">0x08000014</span></span>                                                   |
| <span data-ttu-id="6f652-269">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="6f652-269">Classes used in</span></span>        | [<span data-ttu-id="6f652-270">**Sécurité-principal**</span><span class="sxs-lookup"><span data-stu-id="6f652-270">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6f652-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6f652-271">Windows Server 2012</span></span>



| <span data-ttu-id="6f652-272">Entrée</span><span class="sxs-lookup"><span data-stu-id="6f652-272">Entry</span></span> | <span data-ttu-id="6f652-273">Valeur</span><span class="sxs-lookup"><span data-stu-id="6f652-273">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="6f652-274">ID de lien</span><span class="sxs-lookup"><span data-stu-id="6f652-274">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="6f652-275">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6f652-275">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="6f652-276">System-Only</span><span class="sxs-lookup"><span data-stu-id="6f652-276">System-Only</span></span>            | <span data-ttu-id="6f652-277">Faux</span><span class="sxs-lookup"><span data-stu-id="6f652-277">False</span></span>                                                        |
| <span data-ttu-id="6f652-278">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="6f652-278">Is-Single-Valued</span></span>       | <span data-ttu-id="6f652-279">Faux</span><span class="sxs-lookup"><span data-stu-id="6f652-279">False</span></span>                                                        |
| <span data-ttu-id="6f652-280">Est indexé</span><span class="sxs-lookup"><span data-stu-id="6f652-280">Is Indexed</span></span>             | <span data-ttu-id="6f652-281">Faux</span><span class="sxs-lookup"><span data-stu-id="6f652-281">False</span></span>                                                        |
| <span data-ttu-id="6f652-282">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="6f652-282">In Global Catalog</span></span>      | <span data-ttu-id="6f652-283">Faux</span><span class="sxs-lookup"><span data-stu-id="6f652-283">False</span></span>                                                        |
| <span data-ttu-id="6f652-284">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="6f652-284">NT-Security-Descriptor</span></span> | <span data-ttu-id="6f652-285">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="6f652-285">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="6f652-286">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6f652-286">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="6f652-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6f652-287">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="6f652-288">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6f652-288">Search-Flags</span></span>           | <span data-ttu-id="6f652-289">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6f652-289">0x00000000</span></span>                                                   |
| <span data-ttu-id="6f652-290">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6f652-290">System-Flags</span></span>           | <span data-ttu-id="6f652-291">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6f652-291">0x08000014</span></span>                                                   |
| <span data-ttu-id="6f652-292">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="6f652-292">Classes used in</span></span>        | [<span data-ttu-id="6f652-293">**Sécurité-principal**</span><span class="sxs-lookup"><span data-stu-id="6f652-293">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



 

 





