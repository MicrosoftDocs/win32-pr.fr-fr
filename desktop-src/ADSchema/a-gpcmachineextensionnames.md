---
title: Attribut GPC-machine-extension-Names
description: Utilisé par l’objet stratégie de groupe pour les stratégies de l’ordinateur.
ms.assetid: a5e00bf6-d311-4ccd-a2cf-4f7506fec419
ms.tgt_platform: multiple
keywords:
- Attribut de nom de conteneur GPC-machine-extensions de noms
- Schéma AD de l’attribut gPCMachineExtensionNames
topic_type:
- apiref
api_name:
- GPC-Machine-Extension-Names
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc9d9c1ce435a017bfefe88d728004f619e193f9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103943213"
---
# <a name="gpc-machine-extension-names-attribute"></a><span data-ttu-id="03f08-105">Attribut GPC-machine-extension-Names</span><span class="sxs-lookup"><span data-stu-id="03f08-105">GPC-Machine-Extension-Names attribute</span></span>

<span data-ttu-id="03f08-106">Utilisé par l’objet stratégie de groupe pour les stratégies de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="03f08-106">Used by the Group Policy Object for computer policies.</span></span>



| <span data-ttu-id="03f08-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="03f08-107">Entry</span></span> | <span data-ttu-id="03f08-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="03f08-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="03f08-109">CN</span><span class="sxs-lookup"><span data-stu-id="03f08-109">CN</span></span>                | <span data-ttu-id="03f08-110">GPC-machine-extension-Names</span><span class="sxs-lookup"><span data-stu-id="03f08-110">GPC-Machine-Extension-Names</span></span>                                                     |
| <span data-ttu-id="03f08-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="03f08-111">Ldap-Display-Name</span></span> | <span data-ttu-id="03f08-112">gPCMachineExtensionNames</span><span class="sxs-lookup"><span data-stu-id="03f08-112">gPCMachineExtensionNames</span></span>                                                        |
| <span data-ttu-id="03f08-113">Taille</span><span class="sxs-lookup"><span data-stu-id="03f08-113">Size</span></span>              | <span data-ttu-id="03f08-114">Dépend du nombre d’extensions côté client qui ont une stratégie dans cet objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="03f08-114">Depends on the number of client-side extensions that have a policy in this GPO.</span></span> |
| <span data-ttu-id="03f08-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="03f08-115">Update Privilege</span></span>  | <span data-ttu-id="03f08-116">Administrateur de domaine ou de stratégie.</span><span class="sxs-lookup"><span data-stu-id="03f08-116">Domain or policy administrator.</span></span>                                                 |
| <span data-ttu-id="03f08-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="03f08-117">Update Frequency</span></span>  | <span data-ttu-id="03f08-118">Chaque fois qu’un objet de stratégie de groupe est mis à jour via le GPE.</span><span class="sxs-lookup"><span data-stu-id="03f08-118">Whenever a GPO is updated through the GPE.</span></span>                                      |
| <span data-ttu-id="03f08-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="03f08-119">Attribute-Id</span></span>      | <span data-ttu-id="03f08-120">1.2.840.113556.1.4.1348</span><span class="sxs-lookup"><span data-stu-id="03f08-120">1.2.840.113556.1.4.1348</span></span>                                                         |
| <span data-ttu-id="03f08-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="03f08-121">System-Id-Guid</span></span>    | <span data-ttu-id="03f08-122">32ff8ecc-783f-11d2-9916-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="03f08-122">32ff8ecc-783f-11d2-9916-0000f87a57d4</span></span>                                            |
| <span data-ttu-id="03f08-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="03f08-123">Syntax</span></span>            | [<span data-ttu-id="03f08-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="03f08-124">**String(Unicode)**</span></span>](s-string-unicode.md)                                     |



## <a name="implementations"></a><span data-ttu-id="03f08-125">Implémentations</span><span class="sxs-lookup"><span data-stu-id="03f08-125">Implementations</span></span>

-   [<span data-ttu-id="03f08-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="03f08-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="03f08-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="03f08-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="03f08-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="03f08-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="03f08-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="03f08-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="03f08-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="03f08-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="03f08-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="03f08-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="03f08-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="03f08-132">Windows 2000 Server</span></span>



| <span data-ttu-id="03f08-133">Entrée</span><span class="sxs-lookup"><span data-stu-id="03f08-133">Entry</span></span> | <span data-ttu-id="03f08-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="03f08-134">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="03f08-135">ID de lien</span><span class="sxs-lookup"><span data-stu-id="03f08-135">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="03f08-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="03f08-136">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="03f08-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="03f08-137">System-Only</span></span>            | <span data-ttu-id="03f08-138">Faux</span><span class="sxs-lookup"><span data-stu-id="03f08-138">False</span></span>                                                               |
| <span data-ttu-id="03f08-139">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="03f08-139">Is-Single-Valued</span></span>       | <span data-ttu-id="03f08-140">Vrai</span><span class="sxs-lookup"><span data-stu-id="03f08-140">True</span></span>                                                                |
| <span data-ttu-id="03f08-141">Est indexé</span><span class="sxs-lookup"><span data-stu-id="03f08-141">Is Indexed</span></span>             | <span data-ttu-id="03f08-142">Faux</span><span class="sxs-lookup"><span data-stu-id="03f08-142">False</span></span>                                                               |
| <span data-ttu-id="03f08-143">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="03f08-143">In Global Catalog</span></span>      | <span data-ttu-id="03f08-144">Faux</span><span class="sxs-lookup"><span data-stu-id="03f08-144">False</span></span>                                                               |
| <span data-ttu-id="03f08-145">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="03f08-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="03f08-146">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="03f08-146">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="03f08-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="03f08-147">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="03f08-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="03f08-148">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="03f08-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="03f08-149">Search-Flags</span></span>           | <span data-ttu-id="03f08-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="03f08-150">0x00000000</span></span>                                                          |
| <span data-ttu-id="03f08-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="03f08-151">System-Flags</span></span>           | <span data-ttu-id="03f08-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="03f08-152">0x00000010</span></span>                                                          |
| <span data-ttu-id="03f08-153">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="03f08-153">Classes used in</span></span>        | [<span data-ttu-id="03f08-154">**Conteneur de stratégie de groupe**</span><span class="sxs-lookup"><span data-stu-id="03f08-154">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="03f08-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="03f08-155">Windows Server 2003</span></span>



| <span data-ttu-id="03f08-156">Entrée</span><span class="sxs-lookup"><span data-stu-id="03f08-156">Entry</span></span> | <span data-ttu-id="03f08-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="03f08-157">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="03f08-158">ID de lien</span><span class="sxs-lookup"><span data-stu-id="03f08-158">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="03f08-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="03f08-159">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="03f08-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="03f08-160">System-Only</span></span>            | <span data-ttu-id="03f08-161">Faux</span><span class="sxs-lookup"><span data-stu-id="03f08-161">False</span></span>                                                               |
| <span data-ttu-id="03f08-162">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="03f08-162">Is-Single-Valued</span></span>       | <span data-ttu-id="03f08-163">Vrai</span><span class="sxs-lookup"><span data-stu-id="03f08-163">True</span></span>                                                                |
| <span data-ttu-id="03f08-164">Est indexé</span><span class="sxs-lookup"><span data-stu-id="03f08-164">Is Indexed</span></span>             | <span data-ttu-id="03f08-165">Faux</span><span class="sxs-lookup"><span data-stu-id="03f08-165">False</span></span>                                                               |
| <span data-ttu-id="03f08-166">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="03f08-166">In Global Catalog</span></span>      | <span data-ttu-id="03f08-167">Faux</span><span class="sxs-lookup"><span data-stu-id="03f08-167">False</span></span>                                                               |
| <span data-ttu-id="03f08-168">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="03f08-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="03f08-169">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="03f08-169">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="03f08-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="03f08-170">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="03f08-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="03f08-171">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="03f08-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="03f08-172">Search-Flags</span></span>           | <span data-ttu-id="03f08-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="03f08-173">0x00000000</span></span>                                                          |
| <span data-ttu-id="03f08-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="03f08-174">System-Flags</span></span>           | <span data-ttu-id="03f08-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="03f08-175">0x00000010</span></span>                                                          |
| <span data-ttu-id="03f08-176">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="03f08-176">Classes used in</span></span>        | [<span data-ttu-id="03f08-177">**Conteneur de stratégie de groupe**</span><span class="sxs-lookup"><span data-stu-id="03f08-177">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="03f08-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="03f08-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="03f08-179">Entrée</span><span class="sxs-lookup"><span data-stu-id="03f08-179">Entry</span></span> | <span data-ttu-id="03f08-180">Valeur</span><span class="sxs-lookup"><span data-stu-id="03f08-180">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="03f08-181">ID de lien</span><span class="sxs-lookup"><span data-stu-id="03f08-181">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="03f08-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="03f08-182">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="03f08-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="03f08-183">System-Only</span></span>            | <span data-ttu-id="03f08-184">Faux</span><span class="sxs-lookup"><span data-stu-id="03f08-184">False</span></span>                                                               |
| <span data-ttu-id="03f08-185">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="03f08-185">Is-Single-Valued</span></span>       | <span data-ttu-id="03f08-186">Vrai</span><span class="sxs-lookup"><span data-stu-id="03f08-186">True</span></span>                                                                |
| <span data-ttu-id="03f08-187">Est indexé</span><span class="sxs-lookup"><span data-stu-id="03f08-187">Is Indexed</span></span>             | <span data-ttu-id="03f08-188">Faux</span><span class="sxs-lookup"><span data-stu-id="03f08-188">False</span></span>                                                               |
| <span data-ttu-id="03f08-189">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="03f08-189">In Global Catalog</span></span>      | <span data-ttu-id="03f08-190">Faux</span><span class="sxs-lookup"><span data-stu-id="03f08-190">False</span></span>                                                               |
| <span data-ttu-id="03f08-191">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="03f08-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="03f08-192">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="03f08-192">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="03f08-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="03f08-193">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="03f08-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="03f08-194">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="03f08-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="03f08-195">Search-Flags</span></span>           | <span data-ttu-id="03f08-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="03f08-196">0x00000000</span></span>                                                          |
| <span data-ttu-id="03f08-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="03f08-197">System-Flags</span></span>           | <span data-ttu-id="03f08-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="03f08-198">0x00000010</span></span>                                                          |
| <span data-ttu-id="03f08-199">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="03f08-199">Classes used in</span></span>        | [<span data-ttu-id="03f08-200">**Conteneur de stratégie de groupe**</span><span class="sxs-lookup"><span data-stu-id="03f08-200">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="03f08-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="03f08-201">Windows Server 2008</span></span>



| <span data-ttu-id="03f08-202">Entrée</span><span class="sxs-lookup"><span data-stu-id="03f08-202">Entry</span></span> | <span data-ttu-id="03f08-203">Valeur</span><span class="sxs-lookup"><span data-stu-id="03f08-203">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="03f08-204">ID de lien</span><span class="sxs-lookup"><span data-stu-id="03f08-204">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="03f08-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="03f08-205">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="03f08-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="03f08-206">System-Only</span></span>            | <span data-ttu-id="03f08-207">Faux</span><span class="sxs-lookup"><span data-stu-id="03f08-207">False</span></span>                                                               |
| <span data-ttu-id="03f08-208">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="03f08-208">Is-Single-Valued</span></span>       | <span data-ttu-id="03f08-209">Vrai</span><span class="sxs-lookup"><span data-stu-id="03f08-209">True</span></span>                                                                |
| <span data-ttu-id="03f08-210">Est indexé</span><span class="sxs-lookup"><span data-stu-id="03f08-210">Is Indexed</span></span>             | <span data-ttu-id="03f08-211">Faux</span><span class="sxs-lookup"><span data-stu-id="03f08-211">False</span></span>                                                               |
| <span data-ttu-id="03f08-212">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="03f08-212">In Global Catalog</span></span>      | <span data-ttu-id="03f08-213">Faux</span><span class="sxs-lookup"><span data-stu-id="03f08-213">False</span></span>                                                               |
| <span data-ttu-id="03f08-214">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="03f08-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="03f08-215">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="03f08-215">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="03f08-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="03f08-216">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="03f08-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="03f08-217">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="03f08-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="03f08-218">Search-Flags</span></span>           | <span data-ttu-id="03f08-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="03f08-219">0x00000000</span></span>                                                          |
| <span data-ttu-id="03f08-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="03f08-220">System-Flags</span></span>           | <span data-ttu-id="03f08-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="03f08-221">0x00000010</span></span>                                                          |
| <span data-ttu-id="03f08-222">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="03f08-222">Classes used in</span></span>        | [<span data-ttu-id="03f08-223">**Conteneur de stratégie de groupe**</span><span class="sxs-lookup"><span data-stu-id="03f08-223">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="03f08-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="03f08-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="03f08-225">Entrée</span><span class="sxs-lookup"><span data-stu-id="03f08-225">Entry</span></span> | <span data-ttu-id="03f08-226">Valeur</span><span class="sxs-lookup"><span data-stu-id="03f08-226">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="03f08-227">ID de lien</span><span class="sxs-lookup"><span data-stu-id="03f08-227">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="03f08-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="03f08-228">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="03f08-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="03f08-229">System-Only</span></span>            | <span data-ttu-id="03f08-230">Faux</span><span class="sxs-lookup"><span data-stu-id="03f08-230">False</span></span>                                                               |
| <span data-ttu-id="03f08-231">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="03f08-231">Is-Single-Valued</span></span>       | <span data-ttu-id="03f08-232">Vrai</span><span class="sxs-lookup"><span data-stu-id="03f08-232">True</span></span>                                                                |
| <span data-ttu-id="03f08-233">Est indexé</span><span class="sxs-lookup"><span data-stu-id="03f08-233">Is Indexed</span></span>             | <span data-ttu-id="03f08-234">Faux</span><span class="sxs-lookup"><span data-stu-id="03f08-234">False</span></span>                                                               |
| <span data-ttu-id="03f08-235">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="03f08-235">In Global Catalog</span></span>      | <span data-ttu-id="03f08-236">Faux</span><span class="sxs-lookup"><span data-stu-id="03f08-236">False</span></span>                                                               |
| <span data-ttu-id="03f08-237">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="03f08-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="03f08-238">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="03f08-238">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="03f08-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="03f08-239">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="03f08-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="03f08-240">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="03f08-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="03f08-241">Search-Flags</span></span>           | <span data-ttu-id="03f08-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="03f08-242">0x00000000</span></span>                                                          |
| <span data-ttu-id="03f08-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="03f08-243">System-Flags</span></span>           | <span data-ttu-id="03f08-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="03f08-244">0x00000010</span></span>                                                          |
| <span data-ttu-id="03f08-245">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="03f08-245">Classes used in</span></span>        | [<span data-ttu-id="03f08-246">**Conteneur de stratégie de groupe**</span><span class="sxs-lookup"><span data-stu-id="03f08-246">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="03f08-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="03f08-247">Windows Server 2012</span></span>



| <span data-ttu-id="03f08-248">Entrée</span><span class="sxs-lookup"><span data-stu-id="03f08-248">Entry</span></span> | <span data-ttu-id="03f08-249">Valeur</span><span class="sxs-lookup"><span data-stu-id="03f08-249">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="03f08-250">ID de lien</span><span class="sxs-lookup"><span data-stu-id="03f08-250">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="03f08-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="03f08-251">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="03f08-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="03f08-252">System-Only</span></span>            | <span data-ttu-id="03f08-253">Faux</span><span class="sxs-lookup"><span data-stu-id="03f08-253">False</span></span>                                                               |
| <span data-ttu-id="03f08-254">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="03f08-254">Is-Single-Valued</span></span>       | <span data-ttu-id="03f08-255">Vrai</span><span class="sxs-lookup"><span data-stu-id="03f08-255">True</span></span>                                                                |
| <span data-ttu-id="03f08-256">Est indexé</span><span class="sxs-lookup"><span data-stu-id="03f08-256">Is Indexed</span></span>             | <span data-ttu-id="03f08-257">Faux</span><span class="sxs-lookup"><span data-stu-id="03f08-257">False</span></span>                                                               |
| <span data-ttu-id="03f08-258">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="03f08-258">In Global Catalog</span></span>      | <span data-ttu-id="03f08-259">Faux</span><span class="sxs-lookup"><span data-stu-id="03f08-259">False</span></span>                                                               |
| <span data-ttu-id="03f08-260">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="03f08-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="03f08-261">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="03f08-261">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="03f08-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="03f08-262">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="03f08-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="03f08-263">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="03f08-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="03f08-264">Search-Flags</span></span>           | <span data-ttu-id="03f08-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="03f08-265">0x00000000</span></span>                                                          |
| <span data-ttu-id="03f08-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="03f08-266">System-Flags</span></span>           | <span data-ttu-id="03f08-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="03f08-267">0x00000010</span></span>                                                          |
| <span data-ttu-id="03f08-268">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="03f08-268">Classes used in</span></span>        | [<span data-ttu-id="03f08-269">**Conteneur de stratégie de groupe**</span><span class="sxs-lookup"><span data-stu-id="03f08-269">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



 

 





