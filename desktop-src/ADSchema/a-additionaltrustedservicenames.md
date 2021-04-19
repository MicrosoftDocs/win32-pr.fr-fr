---
title: Attribut-Trust-Name-Names supplémentaire
description: Liste des services du domaine qui peuvent être approuvés. Non utilisé par Active Directory.
ms.assetid: 0c574a99-4036-408b-807c-b4b3394624c7
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory de l’attribut de noms de service de confiance supplémentaires
- Schéma AD de l’attribut additionalTrustedServiceNames
topic_type:
- apiref
api_name:
- Additional-Trusted-Service-Names
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8066190082cfe0f1bbb8825768ad135090a7a4f8
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106515116"
---
# <a name="additional-trusted-service-names-attribute"></a><span data-ttu-id="9265c-106">Attribut-Trust-Name-Names supplémentaire</span><span class="sxs-lookup"><span data-stu-id="9265c-106">Additional-Trusted-Service-Names attribute</span></span>

<span data-ttu-id="9265c-107">Liste des services du domaine qui peuvent être approuvés.</span><span class="sxs-lookup"><span data-stu-id="9265c-107">A list of services in the domain that can be trusted.</span></span> <span data-ttu-id="9265c-108">Non utilisé par Active Directory.</span><span class="sxs-lookup"><span data-stu-id="9265c-108">Not used by AD.</span></span>



| <span data-ttu-id="9265c-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="9265c-109">Entry</span></span> | <span data-ttu-id="9265c-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="9265c-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="9265c-111">CN</span><span class="sxs-lookup"><span data-stu-id="9265c-111">CN</span></span>                | <span data-ttu-id="9265c-112">Noms de service de confiance supplémentaires</span><span class="sxs-lookup"><span data-stu-id="9265c-112">Additional-Trusted-Service-Names</span></span>            |
| <span data-ttu-id="9265c-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="9265c-113">Ldap-Display-Name</span></span> | <span data-ttu-id="9265c-114">additionalTrustedServiceNames</span><span class="sxs-lookup"><span data-stu-id="9265c-114">additionalTrustedServiceNames</span></span>               |
| <span data-ttu-id="9265c-115">Taille</span><span class="sxs-lookup"><span data-stu-id="9265c-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="9265c-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="9265c-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="9265c-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="9265c-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="9265c-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9265c-118">Attribute-Id</span></span>      | <span data-ttu-id="9265c-119">1.2.840.113556.1.4.889</span><span class="sxs-lookup"><span data-stu-id="9265c-119">1.2.840.113556.1.4.889</span></span>                      |
| <span data-ttu-id="9265c-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="9265c-120">System-Id-Guid</span></span>    | <span data-ttu-id="9265c-121">032160be-9824-11d1-aec0-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="9265c-121">032160be-9824-11d1-aec0-0000f80367c1</span></span>        |
| <span data-ttu-id="9265c-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9265c-122">Syntax</span></span>            | [<span data-ttu-id="9265c-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="9265c-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="9265c-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="9265c-124">Implementations</span></span>

-   [<span data-ttu-id="9265c-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="9265c-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="9265c-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9265c-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9265c-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9265c-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9265c-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9265c-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9265c-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9265c-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9265c-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9265c-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="9265c-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9265c-131">Windows 2000 Server</span></span>



| <span data-ttu-id="9265c-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="9265c-132">Entry</span></span> | <span data-ttu-id="9265c-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="9265c-133">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="9265c-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9265c-134">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="9265c-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9265c-135">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="9265c-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="9265c-136">System-Only</span></span>            | <span data-ttu-id="9265c-137">Faux</span><span class="sxs-lookup"><span data-stu-id="9265c-137">False</span></span>                                                |
| <span data-ttu-id="9265c-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9265c-138">Is-Single-Valued</span></span>       | <span data-ttu-id="9265c-139">Faux</span><span class="sxs-lookup"><span data-stu-id="9265c-139">False</span></span>                                                |
| <span data-ttu-id="9265c-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9265c-140">Is Indexed</span></span>             | <span data-ttu-id="9265c-141">Faux</span><span class="sxs-lookup"><span data-stu-id="9265c-141">False</span></span>                                                |
| <span data-ttu-id="9265c-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9265c-142">In Global Catalog</span></span>      | <span data-ttu-id="9265c-143">Faux</span><span class="sxs-lookup"><span data-stu-id="9265c-143">False</span></span>                                                |
| <span data-ttu-id="9265c-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9265c-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="9265c-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9265c-145">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="9265c-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9265c-146">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="9265c-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9265c-147">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="9265c-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9265c-148">Search-Flags</span></span>           | <span data-ttu-id="9265c-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9265c-149">0x00000000</span></span>                                           |
| <span data-ttu-id="9265c-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9265c-150">System-Flags</span></span>           | <span data-ttu-id="9265c-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9265c-151">0x00000010</span></span>                                           |
| <span data-ttu-id="9265c-152">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9265c-152">Classes used in</span></span>        | [<span data-ttu-id="9265c-153">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="9265c-153">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="9265c-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9265c-154">Windows Server 2003</span></span>



| <span data-ttu-id="9265c-155">Entrée</span><span class="sxs-lookup"><span data-stu-id="9265c-155">Entry</span></span> | <span data-ttu-id="9265c-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="9265c-156">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="9265c-157">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9265c-157">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="9265c-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9265c-158">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="9265c-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="9265c-159">System-Only</span></span>            | <span data-ttu-id="9265c-160">Faux</span><span class="sxs-lookup"><span data-stu-id="9265c-160">False</span></span>                                                |
| <span data-ttu-id="9265c-161">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9265c-161">Is-Single-Valued</span></span>       | <span data-ttu-id="9265c-162">Faux</span><span class="sxs-lookup"><span data-stu-id="9265c-162">False</span></span>                                                |
| <span data-ttu-id="9265c-163">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9265c-163">Is Indexed</span></span>             | <span data-ttu-id="9265c-164">Faux</span><span class="sxs-lookup"><span data-stu-id="9265c-164">False</span></span>                                                |
| <span data-ttu-id="9265c-165">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9265c-165">In Global Catalog</span></span>      | <span data-ttu-id="9265c-166">Faux</span><span class="sxs-lookup"><span data-stu-id="9265c-166">False</span></span>                                                |
| <span data-ttu-id="9265c-167">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9265c-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="9265c-168">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9265c-168">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="9265c-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9265c-169">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="9265c-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9265c-170">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="9265c-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9265c-171">Search-Flags</span></span>           | <span data-ttu-id="9265c-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9265c-172">0x00000000</span></span>                                           |
| <span data-ttu-id="9265c-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9265c-173">System-Flags</span></span>           | <span data-ttu-id="9265c-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9265c-174">0x00000010</span></span>                                           |
| <span data-ttu-id="9265c-175">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9265c-175">Classes used in</span></span>        | [<span data-ttu-id="9265c-176">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="9265c-176">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9265c-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9265c-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9265c-178">Entrée</span><span class="sxs-lookup"><span data-stu-id="9265c-178">Entry</span></span> | <span data-ttu-id="9265c-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="9265c-179">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="9265c-180">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9265c-180">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="9265c-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9265c-181">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="9265c-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="9265c-182">System-Only</span></span>            | <span data-ttu-id="9265c-183">Faux</span><span class="sxs-lookup"><span data-stu-id="9265c-183">False</span></span>                                                |
| <span data-ttu-id="9265c-184">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9265c-184">Is-Single-Valued</span></span>       | <span data-ttu-id="9265c-185">Faux</span><span class="sxs-lookup"><span data-stu-id="9265c-185">False</span></span>                                                |
| <span data-ttu-id="9265c-186">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9265c-186">Is Indexed</span></span>             | <span data-ttu-id="9265c-187">Faux</span><span class="sxs-lookup"><span data-stu-id="9265c-187">False</span></span>                                                |
| <span data-ttu-id="9265c-188">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9265c-188">In Global Catalog</span></span>      | <span data-ttu-id="9265c-189">Faux</span><span class="sxs-lookup"><span data-stu-id="9265c-189">False</span></span>                                                |
| <span data-ttu-id="9265c-190">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9265c-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="9265c-191">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9265c-191">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="9265c-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9265c-192">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="9265c-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9265c-193">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="9265c-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9265c-194">Search-Flags</span></span>           | <span data-ttu-id="9265c-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9265c-195">0x00000000</span></span>                                           |
| <span data-ttu-id="9265c-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9265c-196">System-Flags</span></span>           | <span data-ttu-id="9265c-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9265c-197">0x00000010</span></span>                                           |
| <span data-ttu-id="9265c-198">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9265c-198">Classes used in</span></span>        | [<span data-ttu-id="9265c-199">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="9265c-199">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9265c-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9265c-200">Windows Server 2008</span></span>



| <span data-ttu-id="9265c-201">Entrée</span><span class="sxs-lookup"><span data-stu-id="9265c-201">Entry</span></span> | <span data-ttu-id="9265c-202">Valeur</span><span class="sxs-lookup"><span data-stu-id="9265c-202">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="9265c-203">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9265c-203">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="9265c-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9265c-204">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="9265c-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="9265c-205">System-Only</span></span>            | <span data-ttu-id="9265c-206">Faux</span><span class="sxs-lookup"><span data-stu-id="9265c-206">False</span></span>                                                |
| <span data-ttu-id="9265c-207">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9265c-207">Is-Single-Valued</span></span>       | <span data-ttu-id="9265c-208">Faux</span><span class="sxs-lookup"><span data-stu-id="9265c-208">False</span></span>                                                |
| <span data-ttu-id="9265c-209">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9265c-209">Is Indexed</span></span>             | <span data-ttu-id="9265c-210">Faux</span><span class="sxs-lookup"><span data-stu-id="9265c-210">False</span></span>                                                |
| <span data-ttu-id="9265c-211">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9265c-211">In Global Catalog</span></span>      | <span data-ttu-id="9265c-212">Faux</span><span class="sxs-lookup"><span data-stu-id="9265c-212">False</span></span>                                                |
| <span data-ttu-id="9265c-213">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9265c-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="9265c-214">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9265c-214">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="9265c-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9265c-215">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="9265c-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9265c-216">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="9265c-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9265c-217">Search-Flags</span></span>           | <span data-ttu-id="9265c-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9265c-218">0x00000000</span></span>                                           |
| <span data-ttu-id="9265c-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9265c-219">System-Flags</span></span>           | <span data-ttu-id="9265c-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9265c-220">0x00000010</span></span>                                           |
| <span data-ttu-id="9265c-221">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9265c-221">Classes used in</span></span>        | [<span data-ttu-id="9265c-222">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="9265c-222">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9265c-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9265c-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9265c-224">Entrée</span><span class="sxs-lookup"><span data-stu-id="9265c-224">Entry</span></span> | <span data-ttu-id="9265c-225">Valeur</span><span class="sxs-lookup"><span data-stu-id="9265c-225">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="9265c-226">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9265c-226">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="9265c-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9265c-227">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="9265c-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="9265c-228">System-Only</span></span>            | <span data-ttu-id="9265c-229">Faux</span><span class="sxs-lookup"><span data-stu-id="9265c-229">False</span></span>                                                |
| <span data-ttu-id="9265c-230">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9265c-230">Is-Single-Valued</span></span>       | <span data-ttu-id="9265c-231">Faux</span><span class="sxs-lookup"><span data-stu-id="9265c-231">False</span></span>                                                |
| <span data-ttu-id="9265c-232">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9265c-232">Is Indexed</span></span>             | <span data-ttu-id="9265c-233">Faux</span><span class="sxs-lookup"><span data-stu-id="9265c-233">False</span></span>                                                |
| <span data-ttu-id="9265c-234">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9265c-234">In Global Catalog</span></span>      | <span data-ttu-id="9265c-235">Faux</span><span class="sxs-lookup"><span data-stu-id="9265c-235">False</span></span>                                                |
| <span data-ttu-id="9265c-236">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9265c-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="9265c-237">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9265c-237">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="9265c-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9265c-238">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="9265c-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9265c-239">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="9265c-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9265c-240">Search-Flags</span></span>           | <span data-ttu-id="9265c-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9265c-241">0x00000000</span></span>                                           |
| <span data-ttu-id="9265c-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9265c-242">System-Flags</span></span>           | <span data-ttu-id="9265c-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9265c-243">0x00000010</span></span>                                           |
| <span data-ttu-id="9265c-244">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9265c-244">Classes used in</span></span>        | [<span data-ttu-id="9265c-245">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="9265c-245">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9265c-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9265c-246">Windows Server 2012</span></span>



| <span data-ttu-id="9265c-247">Entrée</span><span class="sxs-lookup"><span data-stu-id="9265c-247">Entry</span></span> | <span data-ttu-id="9265c-248">Valeur</span><span class="sxs-lookup"><span data-stu-id="9265c-248">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="9265c-249">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9265c-249">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="9265c-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9265c-250">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="9265c-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="9265c-251">System-Only</span></span>            | <span data-ttu-id="9265c-252">Faux</span><span class="sxs-lookup"><span data-stu-id="9265c-252">False</span></span>                                                |
| <span data-ttu-id="9265c-253">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9265c-253">Is-Single-Valued</span></span>       | <span data-ttu-id="9265c-254">Faux</span><span class="sxs-lookup"><span data-stu-id="9265c-254">False</span></span>                                                |
| <span data-ttu-id="9265c-255">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9265c-255">Is Indexed</span></span>             | <span data-ttu-id="9265c-256">Faux</span><span class="sxs-lookup"><span data-stu-id="9265c-256">False</span></span>                                                |
| <span data-ttu-id="9265c-257">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9265c-257">In Global Catalog</span></span>      | <span data-ttu-id="9265c-258">Faux</span><span class="sxs-lookup"><span data-stu-id="9265c-258">False</span></span>                                                |
| <span data-ttu-id="9265c-259">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9265c-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="9265c-260">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9265c-260">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="9265c-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9265c-261">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="9265c-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9265c-262">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="9265c-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9265c-263">Search-Flags</span></span>           | <span data-ttu-id="9265c-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9265c-264">0x00000000</span></span>                                           |
| <span data-ttu-id="9265c-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9265c-265">System-Flags</span></span>           | <span data-ttu-id="9265c-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9265c-266">0x00000010</span></span>                                           |
| <span data-ttu-id="9265c-267">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9265c-267">Classes used in</span></span>        | [<span data-ttu-id="9265c-268">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="9265c-268">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





