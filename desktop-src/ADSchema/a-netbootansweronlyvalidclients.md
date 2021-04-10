---
title: attribut netboot-réponse uniquement-valide-clients
description: Détermine si le serveur répond à tous les ordinateurs clients prédéfinis ou non.
ms.assetid: b02438ba-11b3-497c-b57f-bd9a0045e6b0
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut netboot-réponse uniquement-valide-clients
- Schéma AD de l’attribut netbootAnswerOnlyValidClients
topic_type:
- apiref
api_name:
- netboot-Answer-Only-Valid-Clients
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e28f7ecfaa569f47d79249606029760b914b5ac
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107656"
---
# <a name="netboot-answer-only-valid-clients-attribute"></a><span data-ttu-id="9f387-105">attribut netboot-réponse uniquement-valide-clients</span><span class="sxs-lookup"><span data-stu-id="9f387-105">netboot-Answer-Only-Valid-Clients attribute</span></span>

<span data-ttu-id="9f387-106">Détermine si le serveur répond à tous les ordinateurs clients prédéfinis ou non.</span><span class="sxs-lookup"><span data-stu-id="9f387-106">Determines whether the server answers all, or only pre-staged, client computers.</span></span>



| <span data-ttu-id="9f387-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="9f387-107">Entry</span></span> | <span data-ttu-id="9f387-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="9f387-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="9f387-109">CN</span><span class="sxs-lookup"><span data-stu-id="9f387-109">CN</span></span>                | <span data-ttu-id="9f387-110">netboot-réponse seule-valide-clients</span><span class="sxs-lookup"><span data-stu-id="9f387-110">netboot-Answer-Only-Valid-Clients</span></span>    |
| <span data-ttu-id="9f387-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="9f387-111">Ldap-Display-Name</span></span> | <span data-ttu-id="9f387-112">netbootAnswerOnlyValidClients</span><span class="sxs-lookup"><span data-stu-id="9f387-112">netbootAnswerOnlyValidClients</span></span>        |
| <span data-ttu-id="9f387-113">Taille</span><span class="sxs-lookup"><span data-stu-id="9f387-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="9f387-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="9f387-114">Update Privilege</span></span>  | <span data-ttu-id="9f387-115">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="9f387-115">This value is set by the system.</span></span>     |
| <span data-ttu-id="9f387-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="9f387-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="9f387-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9f387-117">Attribute-Id</span></span>      | <span data-ttu-id="9f387-118">1.2.840.113556.1.4.854</span><span class="sxs-lookup"><span data-stu-id="9f387-118">1.2.840.113556.1.4.854</span></span>               |
| <span data-ttu-id="9f387-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="9f387-119">System-Id-Guid</span></span>    | <span data-ttu-id="9f387-120">0738307b-91df-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="9f387-120">0738307b-91df-11d1-aebc-0000f80367c1</span></span> |
| <span data-ttu-id="9f387-121">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9f387-121">Syntax</span></span>            | [<span data-ttu-id="9f387-122">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="9f387-122">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="9f387-123">Implémentations</span><span class="sxs-lookup"><span data-stu-id="9f387-123">Implementations</span></span>

-   [<span data-ttu-id="9f387-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="9f387-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="9f387-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9f387-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9f387-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9f387-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9f387-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9f387-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9f387-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9f387-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9f387-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9f387-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="9f387-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9f387-130">Windows 2000 Server</span></span>



| <span data-ttu-id="9f387-131">Entrée</span><span class="sxs-lookup"><span data-stu-id="9f387-131">Entry</span></span> | <span data-ttu-id="9f387-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="9f387-132">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="9f387-133">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9f387-133">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="9f387-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9f387-134">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="9f387-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="9f387-135">System-Only</span></span>            | <span data-ttu-id="9f387-136">Faux</span><span class="sxs-lookup"><span data-stu-id="9f387-136">False</span></span>                                                      |
| <span data-ttu-id="9f387-137">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9f387-137">Is-Single-Valued</span></span>       | <span data-ttu-id="9f387-138">Vrai</span><span class="sxs-lookup"><span data-stu-id="9f387-138">True</span></span>                                                       |
| <span data-ttu-id="9f387-139">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9f387-139">Is Indexed</span></span>             | <span data-ttu-id="9f387-140">Faux</span><span class="sxs-lookup"><span data-stu-id="9f387-140">False</span></span>                                                      |
| <span data-ttu-id="9f387-141">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9f387-141">In Global Catalog</span></span>      | <span data-ttu-id="9f387-142">Faux</span><span class="sxs-lookup"><span data-stu-id="9f387-142">False</span></span>                                                      |
| <span data-ttu-id="9f387-143">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9f387-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="9f387-144">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9f387-144">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="9f387-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9f387-145">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="9f387-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9f387-146">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="9f387-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9f387-147">Search-Flags</span></span>           | <span data-ttu-id="9f387-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9f387-148">0x00000000</span></span>                                                 |
| <span data-ttu-id="9f387-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9f387-149">System-Flags</span></span>           | <span data-ttu-id="9f387-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9f387-150">0x00000010</span></span>                                                 |
| <span data-ttu-id="9f387-151">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9f387-151">Classes used in</span></span>        | [<span data-ttu-id="9f387-152">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="9f387-152">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="9f387-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9f387-153">Windows Server 2003</span></span>



| <span data-ttu-id="9f387-154">Entrée</span><span class="sxs-lookup"><span data-stu-id="9f387-154">Entry</span></span> | <span data-ttu-id="9f387-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="9f387-155">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="9f387-156">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9f387-156">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="9f387-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9f387-157">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="9f387-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="9f387-158">System-Only</span></span>            | <span data-ttu-id="9f387-159">Faux</span><span class="sxs-lookup"><span data-stu-id="9f387-159">False</span></span>                                                      |
| <span data-ttu-id="9f387-160">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9f387-160">Is-Single-Valued</span></span>       | <span data-ttu-id="9f387-161">Vrai</span><span class="sxs-lookup"><span data-stu-id="9f387-161">True</span></span>                                                       |
| <span data-ttu-id="9f387-162">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9f387-162">Is Indexed</span></span>             | <span data-ttu-id="9f387-163">Faux</span><span class="sxs-lookup"><span data-stu-id="9f387-163">False</span></span>                                                      |
| <span data-ttu-id="9f387-164">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9f387-164">In Global Catalog</span></span>      | <span data-ttu-id="9f387-165">Faux</span><span class="sxs-lookup"><span data-stu-id="9f387-165">False</span></span>                                                      |
| <span data-ttu-id="9f387-166">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9f387-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="9f387-167">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9f387-167">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="9f387-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9f387-168">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="9f387-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9f387-169">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="9f387-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9f387-170">Search-Flags</span></span>           | <span data-ttu-id="9f387-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9f387-171">0x00000000</span></span>                                                 |
| <span data-ttu-id="9f387-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9f387-172">System-Flags</span></span>           | <span data-ttu-id="9f387-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9f387-173">0x00000010</span></span>                                                 |
| <span data-ttu-id="9f387-174">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9f387-174">Classes used in</span></span>        | [<span data-ttu-id="9f387-175">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="9f387-175">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9f387-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9f387-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9f387-177">Entrée</span><span class="sxs-lookup"><span data-stu-id="9f387-177">Entry</span></span> | <span data-ttu-id="9f387-178">Valeur</span><span class="sxs-lookup"><span data-stu-id="9f387-178">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="9f387-179">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9f387-179">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="9f387-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9f387-180">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="9f387-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="9f387-181">System-Only</span></span>            | <span data-ttu-id="9f387-182">Faux</span><span class="sxs-lookup"><span data-stu-id="9f387-182">False</span></span>                                                      |
| <span data-ttu-id="9f387-183">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9f387-183">Is-Single-Valued</span></span>       | <span data-ttu-id="9f387-184">Vrai</span><span class="sxs-lookup"><span data-stu-id="9f387-184">True</span></span>                                                       |
| <span data-ttu-id="9f387-185">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9f387-185">Is Indexed</span></span>             | <span data-ttu-id="9f387-186">Faux</span><span class="sxs-lookup"><span data-stu-id="9f387-186">False</span></span>                                                      |
| <span data-ttu-id="9f387-187">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9f387-187">In Global Catalog</span></span>      | <span data-ttu-id="9f387-188">Faux</span><span class="sxs-lookup"><span data-stu-id="9f387-188">False</span></span>                                                      |
| <span data-ttu-id="9f387-189">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9f387-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="9f387-190">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9f387-190">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="9f387-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9f387-191">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="9f387-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9f387-192">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="9f387-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9f387-193">Search-Flags</span></span>           | <span data-ttu-id="9f387-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9f387-194">0x00000000</span></span>                                                 |
| <span data-ttu-id="9f387-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9f387-195">System-Flags</span></span>           | <span data-ttu-id="9f387-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9f387-196">0x00000010</span></span>                                                 |
| <span data-ttu-id="9f387-197">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9f387-197">Classes used in</span></span>        | [<span data-ttu-id="9f387-198">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="9f387-198">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9f387-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9f387-199">Windows Server 2008</span></span>



| <span data-ttu-id="9f387-200">Entrée</span><span class="sxs-lookup"><span data-stu-id="9f387-200">Entry</span></span> | <span data-ttu-id="9f387-201">Valeur</span><span class="sxs-lookup"><span data-stu-id="9f387-201">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="9f387-202">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9f387-202">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="9f387-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9f387-203">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="9f387-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="9f387-204">System-Only</span></span>            | <span data-ttu-id="9f387-205">Faux</span><span class="sxs-lookup"><span data-stu-id="9f387-205">False</span></span>                                                      |
| <span data-ttu-id="9f387-206">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9f387-206">Is-Single-Valued</span></span>       | <span data-ttu-id="9f387-207">Vrai</span><span class="sxs-lookup"><span data-stu-id="9f387-207">True</span></span>                                                       |
| <span data-ttu-id="9f387-208">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9f387-208">Is Indexed</span></span>             | <span data-ttu-id="9f387-209">Faux</span><span class="sxs-lookup"><span data-stu-id="9f387-209">False</span></span>                                                      |
| <span data-ttu-id="9f387-210">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9f387-210">In Global Catalog</span></span>      | <span data-ttu-id="9f387-211">Faux</span><span class="sxs-lookup"><span data-stu-id="9f387-211">False</span></span>                                                      |
| <span data-ttu-id="9f387-212">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9f387-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="9f387-213">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9f387-213">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="9f387-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9f387-214">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="9f387-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9f387-215">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="9f387-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9f387-216">Search-Flags</span></span>           | <span data-ttu-id="9f387-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9f387-217">0x00000000</span></span>                                                 |
| <span data-ttu-id="9f387-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9f387-218">System-Flags</span></span>           | <span data-ttu-id="9f387-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9f387-219">0x00000010</span></span>                                                 |
| <span data-ttu-id="9f387-220">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9f387-220">Classes used in</span></span>        | [<span data-ttu-id="9f387-221">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="9f387-221">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9f387-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9f387-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9f387-223">Entrée</span><span class="sxs-lookup"><span data-stu-id="9f387-223">Entry</span></span> | <span data-ttu-id="9f387-224">Valeur</span><span class="sxs-lookup"><span data-stu-id="9f387-224">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="9f387-225">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9f387-225">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="9f387-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9f387-226">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="9f387-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="9f387-227">System-Only</span></span>            | <span data-ttu-id="9f387-228">Faux</span><span class="sxs-lookup"><span data-stu-id="9f387-228">False</span></span>                                                      |
| <span data-ttu-id="9f387-229">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9f387-229">Is-Single-Valued</span></span>       | <span data-ttu-id="9f387-230">Vrai</span><span class="sxs-lookup"><span data-stu-id="9f387-230">True</span></span>                                                       |
| <span data-ttu-id="9f387-231">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9f387-231">Is Indexed</span></span>             | <span data-ttu-id="9f387-232">Faux</span><span class="sxs-lookup"><span data-stu-id="9f387-232">False</span></span>                                                      |
| <span data-ttu-id="9f387-233">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9f387-233">In Global Catalog</span></span>      | <span data-ttu-id="9f387-234">Faux</span><span class="sxs-lookup"><span data-stu-id="9f387-234">False</span></span>                                                      |
| <span data-ttu-id="9f387-235">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9f387-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="9f387-236">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9f387-236">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="9f387-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9f387-237">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="9f387-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9f387-238">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="9f387-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9f387-239">Search-Flags</span></span>           | <span data-ttu-id="9f387-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9f387-240">0x00000000</span></span>                                                 |
| <span data-ttu-id="9f387-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9f387-241">System-Flags</span></span>           | <span data-ttu-id="9f387-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9f387-242">0x00000010</span></span>                                                 |
| <span data-ttu-id="9f387-243">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9f387-243">Classes used in</span></span>        | [<span data-ttu-id="9f387-244">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="9f387-244">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9f387-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9f387-245">Windows Server 2012</span></span>



| <span data-ttu-id="9f387-246">Entrée</span><span class="sxs-lookup"><span data-stu-id="9f387-246">Entry</span></span> | <span data-ttu-id="9f387-247">Valeur</span><span class="sxs-lookup"><span data-stu-id="9f387-247">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="9f387-248">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9f387-248">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="9f387-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9f387-249">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="9f387-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="9f387-250">System-Only</span></span>            | <span data-ttu-id="9f387-251">Faux</span><span class="sxs-lookup"><span data-stu-id="9f387-251">False</span></span>                                                      |
| <span data-ttu-id="9f387-252">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9f387-252">Is-Single-Valued</span></span>       | <span data-ttu-id="9f387-253">Vrai</span><span class="sxs-lookup"><span data-stu-id="9f387-253">True</span></span>                                                       |
| <span data-ttu-id="9f387-254">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9f387-254">Is Indexed</span></span>             | <span data-ttu-id="9f387-255">Faux</span><span class="sxs-lookup"><span data-stu-id="9f387-255">False</span></span>                                                      |
| <span data-ttu-id="9f387-256">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9f387-256">In Global Catalog</span></span>      | <span data-ttu-id="9f387-257">Faux</span><span class="sxs-lookup"><span data-stu-id="9f387-257">False</span></span>                                                      |
| <span data-ttu-id="9f387-258">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9f387-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="9f387-259">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9f387-259">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="9f387-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9f387-260">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="9f387-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9f387-261">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="9f387-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9f387-262">Search-Flags</span></span>           | <span data-ttu-id="9f387-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9f387-263">0x00000000</span></span>                                                 |
| <span data-ttu-id="9f387-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9f387-264">System-Flags</span></span>           | <span data-ttu-id="9f387-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9f387-265">0x00000010</span></span>                                                 |
| <span data-ttu-id="9f387-266">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9f387-266">Classes used in</span></span>        | [<span data-ttu-id="9f387-267">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="9f387-267">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



 

 





