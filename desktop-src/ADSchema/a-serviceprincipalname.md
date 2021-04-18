---
title: Attribut de nom de principal du service
description: Liste des noms principaux utilisés pour l’authentification mutuelle avec une instance d’un service sur cet ordinateur.
ms.assetid: 0ad1694f-0d6f-4350-a088-fdf3ef798c46
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut de nom de principal du service
- Schéma AD de l’attribut servicePrincipalName
topic_type:
- apiref
api_name:
- Service-Principal-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 861f160d2c9b71d2c9914c7ff9c2ea0ee43c8528
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106511992"
---
# <a name="service-principal-name-attribute"></a><span data-ttu-id="273ce-105">Attribut de nom de principal du service</span><span class="sxs-lookup"><span data-stu-id="273ce-105">Service-Principal-Name attribute</span></span>

<span data-ttu-id="273ce-106">Liste des noms principaux utilisés pour l’authentification mutuelle avec une instance d’un service sur cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="273ce-106">List of principal names used for mutual authentication with an instance of a service on this computer.</span></span>



| <span data-ttu-id="273ce-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="273ce-107">Entry</span></span> | <span data-ttu-id="273ce-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="273ce-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="273ce-109">CN</span><span class="sxs-lookup"><span data-stu-id="273ce-109">CN</span></span>                | <span data-ttu-id="273ce-110">Nom de principal du service</span><span class="sxs-lookup"><span data-stu-id="273ce-110">Service-Principal-Name</span></span>                      |
| <span data-ttu-id="273ce-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="273ce-111">Ldap-Display-Name</span></span> | <span data-ttu-id="273ce-112">servicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="273ce-112">servicePrincipalName</span></span>                        |
| <span data-ttu-id="273ce-113">Taille</span><span class="sxs-lookup"><span data-stu-id="273ce-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="273ce-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="273ce-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="273ce-115">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="273ce-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="273ce-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="273ce-116">Attribute-Id</span></span>      | <span data-ttu-id="273ce-117">1.2.840.113556.1.4.771</span><span class="sxs-lookup"><span data-stu-id="273ce-117">1.2.840.113556.1.4.771</span></span>                      |
| <span data-ttu-id="273ce-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="273ce-118">System-Id-Guid</span></span>    | <span data-ttu-id="273ce-119">f3a64788-5306-11d1-a9c5-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="273ce-119">f3a64788-5306-11d1-a9c5-0000f80367c1</span></span>        |
| <span data-ttu-id="273ce-120">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="273ce-120">Syntax</span></span>            | [<span data-ttu-id="273ce-121">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="273ce-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="273ce-122">Implémentations</span><span class="sxs-lookup"><span data-stu-id="273ce-122">Implementations</span></span>

-   [<span data-ttu-id="273ce-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="273ce-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="273ce-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="273ce-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="273ce-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="273ce-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="273ce-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="273ce-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="273ce-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="273ce-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="273ce-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="273ce-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="273ce-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="273ce-129">Windows 2000 Server</span></span>



| <span data-ttu-id="273ce-130">Entrée</span><span class="sxs-lookup"><span data-stu-id="273ce-130">Entry</span></span> | <span data-ttu-id="273ce-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="273ce-131">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="273ce-132">ID de lien</span><span class="sxs-lookup"><span data-stu-id="273ce-132">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="273ce-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="273ce-133">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="273ce-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="273ce-134">System-Only</span></span>            | <span data-ttu-id="273ce-135">Faux</span><span class="sxs-lookup"><span data-stu-id="273ce-135">False</span></span>                             |
| <span data-ttu-id="273ce-136">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="273ce-136">Is-Single-Valued</span></span>       | <span data-ttu-id="273ce-137">Faux</span><span class="sxs-lookup"><span data-stu-id="273ce-137">False</span></span>                             |
| <span data-ttu-id="273ce-138">Est indexé</span><span class="sxs-lookup"><span data-stu-id="273ce-138">Is Indexed</span></span>             | <span data-ttu-id="273ce-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="273ce-139">True</span></span>                              |
| <span data-ttu-id="273ce-140">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="273ce-140">In Global Catalog</span></span>      | <span data-ttu-id="273ce-141">Vrai</span><span class="sxs-lookup"><span data-stu-id="273ce-141">True</span></span>                              |
| <span data-ttu-id="273ce-142">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="273ce-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="273ce-143">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="273ce-143">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="273ce-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="273ce-144">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="273ce-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="273ce-145">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="273ce-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="273ce-146">Search-Flags</span></span>           | <span data-ttu-id="273ce-147">0x00000001</span><span class="sxs-lookup"><span data-stu-id="273ce-147">0x00000001</span></span>                        |
| <span data-ttu-id="273ce-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="273ce-148">System-Flags</span></span>           | <span data-ttu-id="273ce-149">0x00000012</span><span class="sxs-lookup"><span data-stu-id="273ce-149">0x00000012</span></span>                        |
| <span data-ttu-id="273ce-150">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="273ce-150">Classes used in</span></span>        | [<span data-ttu-id="273ce-151">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="273ce-151">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="273ce-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="273ce-152">Windows Server 2003</span></span>



| <span data-ttu-id="273ce-153">Entrée</span><span class="sxs-lookup"><span data-stu-id="273ce-153">Entry</span></span> | <span data-ttu-id="273ce-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="273ce-154">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="273ce-155">ID de lien</span><span class="sxs-lookup"><span data-stu-id="273ce-155">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="273ce-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="273ce-156">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="273ce-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="273ce-157">System-Only</span></span>            | <span data-ttu-id="273ce-158">Faux</span><span class="sxs-lookup"><span data-stu-id="273ce-158">False</span></span>                             |
| <span data-ttu-id="273ce-159">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="273ce-159">Is-Single-Valued</span></span>       | <span data-ttu-id="273ce-160">Faux</span><span class="sxs-lookup"><span data-stu-id="273ce-160">False</span></span>                             |
| <span data-ttu-id="273ce-161">Est indexé</span><span class="sxs-lookup"><span data-stu-id="273ce-161">Is Indexed</span></span>             | <span data-ttu-id="273ce-162">Vrai</span><span class="sxs-lookup"><span data-stu-id="273ce-162">True</span></span>                              |
| <span data-ttu-id="273ce-163">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="273ce-163">In Global Catalog</span></span>      | <span data-ttu-id="273ce-164">Vrai</span><span class="sxs-lookup"><span data-stu-id="273ce-164">True</span></span>                              |
| <span data-ttu-id="273ce-165">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="273ce-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="273ce-166">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="273ce-166">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="273ce-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="273ce-167">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="273ce-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="273ce-168">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="273ce-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="273ce-169">Search-Flags</span></span>           | <span data-ttu-id="273ce-170">0x00000001</span><span class="sxs-lookup"><span data-stu-id="273ce-170">0x00000001</span></span>                        |
| <span data-ttu-id="273ce-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="273ce-171">System-Flags</span></span>           | <span data-ttu-id="273ce-172">0x00000012</span><span class="sxs-lookup"><span data-stu-id="273ce-172">0x00000012</span></span>                        |
| <span data-ttu-id="273ce-173">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="273ce-173">Classes used in</span></span>        | [<span data-ttu-id="273ce-174">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="273ce-174">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="273ce-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="273ce-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="273ce-176">Entrée</span><span class="sxs-lookup"><span data-stu-id="273ce-176">Entry</span></span> | <span data-ttu-id="273ce-177">Valeur</span><span class="sxs-lookup"><span data-stu-id="273ce-177">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="273ce-178">ID de lien</span><span class="sxs-lookup"><span data-stu-id="273ce-178">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="273ce-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="273ce-179">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="273ce-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="273ce-180">System-Only</span></span>            | <span data-ttu-id="273ce-181">Faux</span><span class="sxs-lookup"><span data-stu-id="273ce-181">False</span></span>                             |
| <span data-ttu-id="273ce-182">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="273ce-182">Is-Single-Valued</span></span>       | <span data-ttu-id="273ce-183">Faux</span><span class="sxs-lookup"><span data-stu-id="273ce-183">False</span></span>                             |
| <span data-ttu-id="273ce-184">Est indexé</span><span class="sxs-lookup"><span data-stu-id="273ce-184">Is Indexed</span></span>             | <span data-ttu-id="273ce-185">Vrai</span><span class="sxs-lookup"><span data-stu-id="273ce-185">True</span></span>                              |
| <span data-ttu-id="273ce-186">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="273ce-186">In Global Catalog</span></span>      | <span data-ttu-id="273ce-187">Vrai</span><span class="sxs-lookup"><span data-stu-id="273ce-187">True</span></span>                              |
| <span data-ttu-id="273ce-188">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="273ce-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="273ce-189">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="273ce-189">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="273ce-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="273ce-190">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="273ce-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="273ce-191">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="273ce-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="273ce-192">Search-Flags</span></span>           | <span data-ttu-id="273ce-193">0x00000001</span><span class="sxs-lookup"><span data-stu-id="273ce-193">0x00000001</span></span>                        |
| <span data-ttu-id="273ce-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="273ce-194">System-Flags</span></span>           | <span data-ttu-id="273ce-195">0x00000012</span><span class="sxs-lookup"><span data-stu-id="273ce-195">0x00000012</span></span>                        |
| <span data-ttu-id="273ce-196">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="273ce-196">Classes used in</span></span>        | [<span data-ttu-id="273ce-197">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="273ce-197">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="273ce-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="273ce-198">Windows Server 2008</span></span>



| <span data-ttu-id="273ce-199">Entrée</span><span class="sxs-lookup"><span data-stu-id="273ce-199">Entry</span></span> | <span data-ttu-id="273ce-200">Valeur</span><span class="sxs-lookup"><span data-stu-id="273ce-200">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="273ce-201">ID de lien</span><span class="sxs-lookup"><span data-stu-id="273ce-201">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="273ce-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="273ce-202">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="273ce-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="273ce-203">System-Only</span></span>            | <span data-ttu-id="273ce-204">Faux</span><span class="sxs-lookup"><span data-stu-id="273ce-204">False</span></span>                             |
| <span data-ttu-id="273ce-205">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="273ce-205">Is-Single-Valued</span></span>       | <span data-ttu-id="273ce-206">Faux</span><span class="sxs-lookup"><span data-stu-id="273ce-206">False</span></span>                             |
| <span data-ttu-id="273ce-207">Est indexé</span><span class="sxs-lookup"><span data-stu-id="273ce-207">Is Indexed</span></span>             | <span data-ttu-id="273ce-208">Vrai</span><span class="sxs-lookup"><span data-stu-id="273ce-208">True</span></span>                              |
| <span data-ttu-id="273ce-209">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="273ce-209">In Global Catalog</span></span>      | <span data-ttu-id="273ce-210">Vrai</span><span class="sxs-lookup"><span data-stu-id="273ce-210">True</span></span>                              |
| <span data-ttu-id="273ce-211">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="273ce-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="273ce-212">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="273ce-212">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="273ce-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="273ce-213">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="273ce-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="273ce-214">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="273ce-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="273ce-215">Search-Flags</span></span>           | <span data-ttu-id="273ce-216">0x00000001</span><span class="sxs-lookup"><span data-stu-id="273ce-216">0x00000001</span></span>                        |
| <span data-ttu-id="273ce-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="273ce-217">System-Flags</span></span>           | <span data-ttu-id="273ce-218">0x00000012</span><span class="sxs-lookup"><span data-stu-id="273ce-218">0x00000012</span></span>                        |
| <span data-ttu-id="273ce-219">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="273ce-219">Classes used in</span></span>        | [<span data-ttu-id="273ce-220">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="273ce-220">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="273ce-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="273ce-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="273ce-222">Entrée</span><span class="sxs-lookup"><span data-stu-id="273ce-222">Entry</span></span> | <span data-ttu-id="273ce-223">Valeur</span><span class="sxs-lookup"><span data-stu-id="273ce-223">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="273ce-224">ID de lien</span><span class="sxs-lookup"><span data-stu-id="273ce-224">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="273ce-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="273ce-225">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="273ce-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="273ce-226">System-Only</span></span>            | <span data-ttu-id="273ce-227">Faux</span><span class="sxs-lookup"><span data-stu-id="273ce-227">False</span></span>                             |
| <span data-ttu-id="273ce-228">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="273ce-228">Is-Single-Valued</span></span>       | <span data-ttu-id="273ce-229">Faux</span><span class="sxs-lookup"><span data-stu-id="273ce-229">False</span></span>                             |
| <span data-ttu-id="273ce-230">Est indexé</span><span class="sxs-lookup"><span data-stu-id="273ce-230">Is Indexed</span></span>             | <span data-ttu-id="273ce-231">Vrai</span><span class="sxs-lookup"><span data-stu-id="273ce-231">True</span></span>                              |
| <span data-ttu-id="273ce-232">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="273ce-232">In Global Catalog</span></span>      | <span data-ttu-id="273ce-233">Vrai</span><span class="sxs-lookup"><span data-stu-id="273ce-233">True</span></span>                              |
| <span data-ttu-id="273ce-234">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="273ce-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="273ce-235">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="273ce-235">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="273ce-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="273ce-236">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="273ce-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="273ce-237">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="273ce-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="273ce-238">Search-Flags</span></span>           | <span data-ttu-id="273ce-239">0x00000001</span><span class="sxs-lookup"><span data-stu-id="273ce-239">0x00000001</span></span>                        |
| <span data-ttu-id="273ce-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="273ce-240">System-Flags</span></span>           | <span data-ttu-id="273ce-241">0x00000012</span><span class="sxs-lookup"><span data-stu-id="273ce-241">0x00000012</span></span>                        |
| <span data-ttu-id="273ce-242">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="273ce-242">Classes used in</span></span>        | [<span data-ttu-id="273ce-243">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="273ce-243">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="273ce-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="273ce-244">Windows Server 2012</span></span>



| <span data-ttu-id="273ce-245">Entrée</span><span class="sxs-lookup"><span data-stu-id="273ce-245">Entry</span></span> | <span data-ttu-id="273ce-246">Valeur</span><span class="sxs-lookup"><span data-stu-id="273ce-246">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="273ce-247">ID de lien</span><span class="sxs-lookup"><span data-stu-id="273ce-247">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="273ce-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="273ce-248">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="273ce-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="273ce-249">System-Only</span></span>            | <span data-ttu-id="273ce-250">Faux</span><span class="sxs-lookup"><span data-stu-id="273ce-250">False</span></span>                             |
| <span data-ttu-id="273ce-251">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="273ce-251">Is-Single-Valued</span></span>       | <span data-ttu-id="273ce-252">Faux</span><span class="sxs-lookup"><span data-stu-id="273ce-252">False</span></span>                             |
| <span data-ttu-id="273ce-253">Est indexé</span><span class="sxs-lookup"><span data-stu-id="273ce-253">Is Indexed</span></span>             | <span data-ttu-id="273ce-254">Vrai</span><span class="sxs-lookup"><span data-stu-id="273ce-254">True</span></span>                              |
| <span data-ttu-id="273ce-255">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="273ce-255">In Global Catalog</span></span>      | <span data-ttu-id="273ce-256">Vrai</span><span class="sxs-lookup"><span data-stu-id="273ce-256">True</span></span>                              |
| <span data-ttu-id="273ce-257">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="273ce-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="273ce-258">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="273ce-258">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="273ce-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="273ce-259">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="273ce-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="273ce-260">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="273ce-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="273ce-261">Search-Flags</span></span>           | <span data-ttu-id="273ce-262">0x00000001</span><span class="sxs-lookup"><span data-stu-id="273ce-262">0x00000001</span></span>                        |
| <span data-ttu-id="273ce-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="273ce-263">System-Flags</span></span>           | <span data-ttu-id="273ce-264">0x00000012</span><span class="sxs-lookup"><span data-stu-id="273ce-264">0x00000012</span></span>                        |
| <span data-ttu-id="273ce-265">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="273ce-265">Classes used in</span></span>        | [<span data-ttu-id="273ce-266">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="273ce-266">**User**</span></span>](c-user.md)<br/> |



 

 





