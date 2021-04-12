---
title: Attribut GPC-User-extension-Names
description: Utilisé par l’objet stratégie de groupe pour les stratégies utilisateur.
ms.assetid: 3c6fa679-7597-4286-bd79-7a0030212810
ms.tgt_platform: multiple
keywords:
- Schéma AD GPC-User-extension-Names
- Schéma AD de l’attribut gPCUserExtensionNames
topic_type:
- apiref
api_name:
- GPC-User-Extension-Names
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12de39539af6ee523838f8081aa04a5d21b8a1d3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104479685"
---
# <a name="gpc-user-extension-names-attribute"></a><span data-ttu-id="ecf32-105">Attribut GPC-User-extension-Names</span><span class="sxs-lookup"><span data-stu-id="ecf32-105">GPC-User-Extension-Names attribute</span></span>

<span data-ttu-id="ecf32-106">Utilisé par l’objet stratégie de groupe pour les stratégies utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ecf32-106">Used by the Group Policy Object for user policies.</span></span>



| <span data-ttu-id="ecf32-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="ecf32-107">Entry</span></span> | <span data-ttu-id="ecf32-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="ecf32-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="ecf32-109">CN</span><span class="sxs-lookup"><span data-stu-id="ecf32-109">CN</span></span>                | <span data-ttu-id="ecf32-110">GPC-User-extension-Names</span><span class="sxs-lookup"><span data-stu-id="ecf32-110">GPC-User-Extension-Names</span></span>                                                        |
| <span data-ttu-id="ecf32-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="ecf32-111">Ldap-Display-Name</span></span> | <span data-ttu-id="ecf32-112">gPCUserExtensionNames</span><span class="sxs-lookup"><span data-stu-id="ecf32-112">gPCUserExtensionNames</span></span>                                                           |
| <span data-ttu-id="ecf32-113">Taille</span><span class="sxs-lookup"><span data-stu-id="ecf32-113">Size</span></span>              | <span data-ttu-id="ecf32-114">Dépend du nombre d’extensions côté client qui ont une stratégie dans cet objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="ecf32-114">Depends on the number of client-side extensions that have a policy in this GPO.</span></span> |
| <span data-ttu-id="ecf32-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="ecf32-115">Update Privilege</span></span>  | <span data-ttu-id="ecf32-116">Administrateur de domaine ou de stratégie.</span><span class="sxs-lookup"><span data-stu-id="ecf32-116">Domain or policy administrator.</span></span>                                                 |
| <span data-ttu-id="ecf32-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="ecf32-117">Update Frequency</span></span>  | <span data-ttu-id="ecf32-118">Chaque fois qu’un objet de stratégie de groupe est mis à jour via le GPE.</span><span class="sxs-lookup"><span data-stu-id="ecf32-118">Whenever a GPO is updated through the GPE.</span></span>                                      |
| <span data-ttu-id="ecf32-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ecf32-119">Attribute-Id</span></span>      | <span data-ttu-id="ecf32-120">1.2.840.113556.1.4.1349</span><span class="sxs-lookup"><span data-stu-id="ecf32-120">1.2.840.113556.1.4.1349</span></span>                                                         |
| <span data-ttu-id="ecf32-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ecf32-121">System-Id-Guid</span></span>    | <span data-ttu-id="ecf32-122">42a75fc6-783f-11d2-9916-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="ecf32-122">42a75fc6-783f-11d2-9916-0000f87a57d4</span></span>                                            |
| <span data-ttu-id="ecf32-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ecf32-123">Syntax</span></span>            | [<span data-ttu-id="ecf32-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="ecf32-124">**String(Unicode)**</span></span>](s-string-unicode.md)                                     |



## <a name="implementations"></a><span data-ttu-id="ecf32-125">Implémentations</span><span class="sxs-lookup"><span data-stu-id="ecf32-125">Implementations</span></span>

-   [<span data-ttu-id="ecf32-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ecf32-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ecf32-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ecf32-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ecf32-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ecf32-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ecf32-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ecf32-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ecf32-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ecf32-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ecf32-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ecf32-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ecf32-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ecf32-132">Windows 2000 Server</span></span>



| <span data-ttu-id="ecf32-133">Entrée</span><span class="sxs-lookup"><span data-stu-id="ecf32-133">Entry</span></span> | <span data-ttu-id="ecf32-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="ecf32-134">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="ecf32-135">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ecf32-135">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="ecf32-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ecf32-136">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="ecf32-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="ecf32-137">System-Only</span></span>            | <span data-ttu-id="ecf32-138">Faux</span><span class="sxs-lookup"><span data-stu-id="ecf32-138">False</span></span>                                                               |
| <span data-ttu-id="ecf32-139">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ecf32-139">Is-Single-Valued</span></span>       | <span data-ttu-id="ecf32-140">Vrai</span><span class="sxs-lookup"><span data-stu-id="ecf32-140">True</span></span>                                                                |
| <span data-ttu-id="ecf32-141">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ecf32-141">Is Indexed</span></span>             | <span data-ttu-id="ecf32-142">Faux</span><span class="sxs-lookup"><span data-stu-id="ecf32-142">False</span></span>                                                               |
| <span data-ttu-id="ecf32-143">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ecf32-143">In Global Catalog</span></span>      | <span data-ttu-id="ecf32-144">Faux</span><span class="sxs-lookup"><span data-stu-id="ecf32-144">False</span></span>                                                               |
| <span data-ttu-id="ecf32-145">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ecf32-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="ecf32-146">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ecf32-146">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="ecf32-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ecf32-147">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="ecf32-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ecf32-148">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="ecf32-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ecf32-149">Search-Flags</span></span>           | <span data-ttu-id="ecf32-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ecf32-150">0x00000000</span></span>                                                          |
| <span data-ttu-id="ecf32-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ecf32-151">System-Flags</span></span>           | <span data-ttu-id="ecf32-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ecf32-152">0x00000010</span></span>                                                          |
| <span data-ttu-id="ecf32-153">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ecf32-153">Classes used in</span></span>        | [<span data-ttu-id="ecf32-154">**Conteneur de stratégie de groupe**</span><span class="sxs-lookup"><span data-stu-id="ecf32-154">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ecf32-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ecf32-155">Windows Server 2003</span></span>



| <span data-ttu-id="ecf32-156">Entrée</span><span class="sxs-lookup"><span data-stu-id="ecf32-156">Entry</span></span> | <span data-ttu-id="ecf32-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="ecf32-157">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="ecf32-158">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ecf32-158">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="ecf32-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ecf32-159">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="ecf32-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="ecf32-160">System-Only</span></span>            | <span data-ttu-id="ecf32-161">Faux</span><span class="sxs-lookup"><span data-stu-id="ecf32-161">False</span></span>                                                               |
| <span data-ttu-id="ecf32-162">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ecf32-162">Is-Single-Valued</span></span>       | <span data-ttu-id="ecf32-163">Vrai</span><span class="sxs-lookup"><span data-stu-id="ecf32-163">True</span></span>                                                                |
| <span data-ttu-id="ecf32-164">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ecf32-164">Is Indexed</span></span>             | <span data-ttu-id="ecf32-165">Faux</span><span class="sxs-lookup"><span data-stu-id="ecf32-165">False</span></span>                                                               |
| <span data-ttu-id="ecf32-166">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ecf32-166">In Global Catalog</span></span>      | <span data-ttu-id="ecf32-167">Faux</span><span class="sxs-lookup"><span data-stu-id="ecf32-167">False</span></span>                                                               |
| <span data-ttu-id="ecf32-168">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ecf32-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="ecf32-169">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ecf32-169">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="ecf32-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ecf32-170">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="ecf32-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ecf32-171">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="ecf32-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ecf32-172">Search-Flags</span></span>           | <span data-ttu-id="ecf32-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ecf32-173">0x00000000</span></span>                                                          |
| <span data-ttu-id="ecf32-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ecf32-174">System-Flags</span></span>           | <span data-ttu-id="ecf32-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ecf32-175">0x00000010</span></span>                                                          |
| <span data-ttu-id="ecf32-176">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ecf32-176">Classes used in</span></span>        | [<span data-ttu-id="ecf32-177">**Conteneur de stratégie de groupe**</span><span class="sxs-lookup"><span data-stu-id="ecf32-177">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ecf32-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ecf32-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ecf32-179">Entrée</span><span class="sxs-lookup"><span data-stu-id="ecf32-179">Entry</span></span> | <span data-ttu-id="ecf32-180">Valeur</span><span class="sxs-lookup"><span data-stu-id="ecf32-180">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="ecf32-181">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ecf32-181">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="ecf32-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ecf32-182">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="ecf32-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="ecf32-183">System-Only</span></span>            | <span data-ttu-id="ecf32-184">Faux</span><span class="sxs-lookup"><span data-stu-id="ecf32-184">False</span></span>                                                               |
| <span data-ttu-id="ecf32-185">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ecf32-185">Is-Single-Valued</span></span>       | <span data-ttu-id="ecf32-186">Vrai</span><span class="sxs-lookup"><span data-stu-id="ecf32-186">True</span></span>                                                                |
| <span data-ttu-id="ecf32-187">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ecf32-187">Is Indexed</span></span>             | <span data-ttu-id="ecf32-188">Faux</span><span class="sxs-lookup"><span data-stu-id="ecf32-188">False</span></span>                                                               |
| <span data-ttu-id="ecf32-189">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ecf32-189">In Global Catalog</span></span>      | <span data-ttu-id="ecf32-190">Faux</span><span class="sxs-lookup"><span data-stu-id="ecf32-190">False</span></span>                                                               |
| <span data-ttu-id="ecf32-191">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ecf32-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="ecf32-192">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ecf32-192">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="ecf32-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ecf32-193">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="ecf32-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ecf32-194">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="ecf32-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ecf32-195">Search-Flags</span></span>           | <span data-ttu-id="ecf32-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ecf32-196">0x00000000</span></span>                                                          |
| <span data-ttu-id="ecf32-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ecf32-197">System-Flags</span></span>           | <span data-ttu-id="ecf32-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ecf32-198">0x00000010</span></span>                                                          |
| <span data-ttu-id="ecf32-199">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ecf32-199">Classes used in</span></span>        | [<span data-ttu-id="ecf32-200">**Conteneur de stratégie de groupe**</span><span class="sxs-lookup"><span data-stu-id="ecf32-200">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ecf32-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ecf32-201">Windows Server 2008</span></span>



| <span data-ttu-id="ecf32-202">Entrée</span><span class="sxs-lookup"><span data-stu-id="ecf32-202">Entry</span></span> | <span data-ttu-id="ecf32-203">Valeur</span><span class="sxs-lookup"><span data-stu-id="ecf32-203">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="ecf32-204">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ecf32-204">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="ecf32-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ecf32-205">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="ecf32-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="ecf32-206">System-Only</span></span>            | <span data-ttu-id="ecf32-207">Faux</span><span class="sxs-lookup"><span data-stu-id="ecf32-207">False</span></span>                                                               |
| <span data-ttu-id="ecf32-208">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ecf32-208">Is-Single-Valued</span></span>       | <span data-ttu-id="ecf32-209">Vrai</span><span class="sxs-lookup"><span data-stu-id="ecf32-209">True</span></span>                                                                |
| <span data-ttu-id="ecf32-210">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ecf32-210">Is Indexed</span></span>             | <span data-ttu-id="ecf32-211">Faux</span><span class="sxs-lookup"><span data-stu-id="ecf32-211">False</span></span>                                                               |
| <span data-ttu-id="ecf32-212">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ecf32-212">In Global Catalog</span></span>      | <span data-ttu-id="ecf32-213">Faux</span><span class="sxs-lookup"><span data-stu-id="ecf32-213">False</span></span>                                                               |
| <span data-ttu-id="ecf32-214">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ecf32-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="ecf32-215">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ecf32-215">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="ecf32-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ecf32-216">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="ecf32-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ecf32-217">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="ecf32-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ecf32-218">Search-Flags</span></span>           | <span data-ttu-id="ecf32-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ecf32-219">0x00000000</span></span>                                                          |
| <span data-ttu-id="ecf32-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ecf32-220">System-Flags</span></span>           | <span data-ttu-id="ecf32-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ecf32-221">0x00000010</span></span>                                                          |
| <span data-ttu-id="ecf32-222">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ecf32-222">Classes used in</span></span>        | [<span data-ttu-id="ecf32-223">**Conteneur de stratégie de groupe**</span><span class="sxs-lookup"><span data-stu-id="ecf32-223">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ecf32-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ecf32-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ecf32-225">Entrée</span><span class="sxs-lookup"><span data-stu-id="ecf32-225">Entry</span></span> | <span data-ttu-id="ecf32-226">Valeur</span><span class="sxs-lookup"><span data-stu-id="ecf32-226">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="ecf32-227">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ecf32-227">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="ecf32-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ecf32-228">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="ecf32-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="ecf32-229">System-Only</span></span>            | <span data-ttu-id="ecf32-230">Faux</span><span class="sxs-lookup"><span data-stu-id="ecf32-230">False</span></span>                                                               |
| <span data-ttu-id="ecf32-231">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ecf32-231">Is-Single-Valued</span></span>       | <span data-ttu-id="ecf32-232">Vrai</span><span class="sxs-lookup"><span data-stu-id="ecf32-232">True</span></span>                                                                |
| <span data-ttu-id="ecf32-233">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ecf32-233">Is Indexed</span></span>             | <span data-ttu-id="ecf32-234">Faux</span><span class="sxs-lookup"><span data-stu-id="ecf32-234">False</span></span>                                                               |
| <span data-ttu-id="ecf32-235">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ecf32-235">In Global Catalog</span></span>      | <span data-ttu-id="ecf32-236">Faux</span><span class="sxs-lookup"><span data-stu-id="ecf32-236">False</span></span>                                                               |
| <span data-ttu-id="ecf32-237">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ecf32-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="ecf32-238">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ecf32-238">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="ecf32-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ecf32-239">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="ecf32-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ecf32-240">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="ecf32-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ecf32-241">Search-Flags</span></span>           | <span data-ttu-id="ecf32-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ecf32-242">0x00000000</span></span>                                                          |
| <span data-ttu-id="ecf32-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ecf32-243">System-Flags</span></span>           | <span data-ttu-id="ecf32-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ecf32-244">0x00000010</span></span>                                                          |
| <span data-ttu-id="ecf32-245">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ecf32-245">Classes used in</span></span>        | [<span data-ttu-id="ecf32-246">**Conteneur de stratégie de groupe**</span><span class="sxs-lookup"><span data-stu-id="ecf32-246">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ecf32-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ecf32-247">Windows Server 2012</span></span>



| <span data-ttu-id="ecf32-248">Entrée</span><span class="sxs-lookup"><span data-stu-id="ecf32-248">Entry</span></span> | <span data-ttu-id="ecf32-249">Valeur</span><span class="sxs-lookup"><span data-stu-id="ecf32-249">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="ecf32-250">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ecf32-250">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="ecf32-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ecf32-251">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="ecf32-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="ecf32-252">System-Only</span></span>            | <span data-ttu-id="ecf32-253">Faux</span><span class="sxs-lookup"><span data-stu-id="ecf32-253">False</span></span>                                                               |
| <span data-ttu-id="ecf32-254">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ecf32-254">Is-Single-Valued</span></span>       | <span data-ttu-id="ecf32-255">Vrai</span><span class="sxs-lookup"><span data-stu-id="ecf32-255">True</span></span>                                                                |
| <span data-ttu-id="ecf32-256">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ecf32-256">Is Indexed</span></span>             | <span data-ttu-id="ecf32-257">Faux</span><span class="sxs-lookup"><span data-stu-id="ecf32-257">False</span></span>                                                               |
| <span data-ttu-id="ecf32-258">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ecf32-258">In Global Catalog</span></span>      | <span data-ttu-id="ecf32-259">Faux</span><span class="sxs-lookup"><span data-stu-id="ecf32-259">False</span></span>                                                               |
| <span data-ttu-id="ecf32-260">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ecf32-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="ecf32-261">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ecf32-261">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="ecf32-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ecf32-262">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="ecf32-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ecf32-263">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="ecf32-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ecf32-264">Search-Flags</span></span>           | <span data-ttu-id="ecf32-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ecf32-265">0x00000000</span></span>                                                          |
| <span data-ttu-id="ecf32-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ecf32-266">System-Flags</span></span>           | <span data-ttu-id="ecf32-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ecf32-267">0x00000010</span></span>                                                          |
| <span data-ttu-id="ecf32-268">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ecf32-268">Classes used in</span></span>        | [<span data-ttu-id="ecf32-269">**Conteneur de stratégie de groupe**</span><span class="sxs-lookup"><span data-stu-id="ecf32-269">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



 

 





