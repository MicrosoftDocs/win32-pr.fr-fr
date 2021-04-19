---
title: Initials (attribut)
description: Contient les initiales des parties du nom complet de l’utilisateur. Cela peut être utilisé comme initiale du deuxième prénom dans le carnet d’adresses Windows.
ms.assetid: 220b4448-5276-4c3f-8a1b-217cec06135a
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory des attributs initiaux
- Schéma Active Directory des attributs initiaux
topic_type:
- apiref
api_name:
- Initials
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 946f6c9633c1126a30ae4898274096a54db9a402
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106509969"
---
# <a name="initials-attribute"></a><span data-ttu-id="2ab9b-106">Initials (attribut)</span><span class="sxs-lookup"><span data-stu-id="2ab9b-106">Initials attribute</span></span>

<span data-ttu-id="2ab9b-107">Contient les initiales des parties du nom complet de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2ab9b-107">Contains the initials for parts of the user's full name.</span></span> <span data-ttu-id="2ab9b-108">Cela peut être utilisé comme initiale du deuxième prénom dans le carnet d’adresses Windows.</span><span class="sxs-lookup"><span data-stu-id="2ab9b-108">This may be used as the middle initial in the Windows Address Book.</span></span>



| <span data-ttu-id="2ab9b-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="2ab9b-109">Entry</span></span> | <span data-ttu-id="2ab9b-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="2ab9b-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="2ab9b-111">CN</span><span class="sxs-lookup"><span data-stu-id="2ab9b-111">CN</span></span>                | <span data-ttu-id="2ab9b-112">Initiales</span><span class="sxs-lookup"><span data-stu-id="2ab9b-112">Initials</span></span>                                    |
| <span data-ttu-id="2ab9b-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="2ab9b-113">Ldap-Display-Name</span></span> | <span data-ttu-id="2ab9b-114">Initials</span><span class="sxs-lookup"><span data-stu-id="2ab9b-114">initials</span></span>                                    |
| <span data-ttu-id="2ab9b-115">Taille</span><span class="sxs-lookup"><span data-stu-id="2ab9b-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="2ab9b-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="2ab9b-116">Update Privilege</span></span>  | <span data-ttu-id="2ab9b-117">Administrateur de domaine ou propriétaire du compte.</span><span class="sxs-lookup"><span data-stu-id="2ab9b-117">Domain administrator or account owner.</span></span>      |
| <span data-ttu-id="2ab9b-118">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="2ab9b-118">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="2ab9b-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2ab9b-119">Attribute-Id</span></span>      | <span data-ttu-id="2ab9b-120">2.5.4.43</span><span class="sxs-lookup"><span data-stu-id="2ab9b-120">2.5.4.43</span></span>                                    |
| <span data-ttu-id="2ab9b-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="2ab9b-121">System-Id-Guid</span></span>    | <span data-ttu-id="2ab9b-122">f0f8ff90-1191-11d0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="2ab9b-122">f0f8ff90-1191-11d0-a060-00aa006c33ed</span></span>        |
| <span data-ttu-id="2ab9b-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2ab9b-123">Syntax</span></span>            | [<span data-ttu-id="2ab9b-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="2ab9b-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="2ab9b-125">Implémentations</span><span class="sxs-lookup"><span data-stu-id="2ab9b-125">Implementations</span></span>

-   [<span data-ttu-id="2ab9b-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2ab9b-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2ab9b-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2ab9b-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2ab9b-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2ab9b-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2ab9b-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2ab9b-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2ab9b-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2ab9b-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2ab9b-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2ab9b-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2ab9b-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2ab9b-132">Windows 2000 Server</span></span>



| <span data-ttu-id="2ab9b-133">Entrée</span><span class="sxs-lookup"><span data-stu-id="2ab9b-133">Entry</span></span> | <span data-ttu-id="2ab9b-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="2ab9b-134">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="2ab9b-135">ID de lien</span><span class="sxs-lookup"><span data-stu-id="2ab9b-135">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="2ab9b-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2ab9b-136">MAPI-Id</span></span>                | <span data-ttu-id="2ab9b-137">0x3A0A</span><span class="sxs-lookup"><span data-stu-id="2ab9b-137">0x3A0A</span></span>                                                             |
| <span data-ttu-id="2ab9b-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="2ab9b-138">System-Only</span></span>            | <span data-ttu-id="2ab9b-139">Faux</span><span class="sxs-lookup"><span data-stu-id="2ab9b-139">False</span></span>                                                              |
| <span data-ttu-id="2ab9b-140">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="2ab9b-140">Is-Single-Valued</span></span>       | <span data-ttu-id="2ab9b-141">Vrai</span><span class="sxs-lookup"><span data-stu-id="2ab9b-141">True</span></span>                                                               |
| <span data-ttu-id="2ab9b-142">Est indexé</span><span class="sxs-lookup"><span data-stu-id="2ab9b-142">Is Indexed</span></span>             | <span data-ttu-id="2ab9b-143">Faux</span><span class="sxs-lookup"><span data-stu-id="2ab9b-143">False</span></span>                                                              |
| <span data-ttu-id="2ab9b-144">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="2ab9b-144">In Global Catalog</span></span>      | <span data-ttu-id="2ab9b-145">Faux</span><span class="sxs-lookup"><span data-stu-id="2ab9b-145">False</span></span>                                                              |
| <span data-ttu-id="2ab9b-146">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="2ab9b-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="2ab9b-147">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="2ab9b-147">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="2ab9b-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2ab9b-148">Range-Lower</span></span>            | <span data-ttu-id="2ab9b-149">1</span><span class="sxs-lookup"><span data-stu-id="2ab9b-149">1</span></span>                                                                  |
| <span data-ttu-id="2ab9b-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2ab9b-150">Range-Upper</span></span>            | <span data-ttu-id="2ab9b-151">6</span><span class="sxs-lookup"><span data-stu-id="2ab9b-151">6</span></span>                                                                  |
| <span data-ttu-id="2ab9b-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2ab9b-152">Search-Flags</span></span>           | <span data-ttu-id="2ab9b-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2ab9b-153">0x00000000</span></span>                                                         |
| <span data-ttu-id="2ab9b-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2ab9b-154">System-Flags</span></span>           | <span data-ttu-id="2ab9b-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2ab9b-155">0x00000010</span></span>                                                         |
| <span data-ttu-id="2ab9b-156">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="2ab9b-156">Classes used in</span></span>        | [<span data-ttu-id="2ab9b-157">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="2ab9b-157">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2ab9b-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2ab9b-158">Windows Server 2003</span></span>



| <span data-ttu-id="2ab9b-159">Entrée</span><span class="sxs-lookup"><span data-stu-id="2ab9b-159">Entry</span></span> | <span data-ttu-id="2ab9b-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="2ab9b-160">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ab9b-161">ID de lien</span><span class="sxs-lookup"><span data-stu-id="2ab9b-161">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="2ab9b-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2ab9b-162">MAPI-Id</span></span>                | <span data-ttu-id="2ab9b-163">0x3A0A</span><span class="sxs-lookup"><span data-stu-id="2ab9b-163">0x3A0A</span></span>                                                                                                                 |
| <span data-ttu-id="2ab9b-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="2ab9b-164">System-Only</span></span>            | <span data-ttu-id="2ab9b-165">Faux</span><span class="sxs-lookup"><span data-stu-id="2ab9b-165">False</span></span>                                                                                                                  |
| <span data-ttu-id="2ab9b-166">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="2ab9b-166">Is-Single-Valued</span></span>       | <span data-ttu-id="2ab9b-167">Vrai</span><span class="sxs-lookup"><span data-stu-id="2ab9b-167">True</span></span>                                                                                                                   |
| <span data-ttu-id="2ab9b-168">Est indexé</span><span class="sxs-lookup"><span data-stu-id="2ab9b-168">Is Indexed</span></span>             | <span data-ttu-id="2ab9b-169">Faux</span><span class="sxs-lookup"><span data-stu-id="2ab9b-169">False</span></span>                                                                                                                  |
| <span data-ttu-id="2ab9b-170">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="2ab9b-170">In Global Catalog</span></span>      | <span data-ttu-id="2ab9b-171">Faux</span><span class="sxs-lookup"><span data-stu-id="2ab9b-171">False</span></span>                                                                                                                  |
| <span data-ttu-id="2ab9b-172">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="2ab9b-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="2ab9b-173">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="2ab9b-173">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="2ab9b-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2ab9b-174">Range-Lower</span></span>            | <span data-ttu-id="2ab9b-175">1</span><span class="sxs-lookup"><span data-stu-id="2ab9b-175">1</span></span>                                                                                                                      |
| <span data-ttu-id="2ab9b-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2ab9b-176">Range-Upper</span></span>            | <span data-ttu-id="2ab9b-177">6</span><span class="sxs-lookup"><span data-stu-id="2ab9b-177">6</span></span>                                                                                                                      |
| <span data-ttu-id="2ab9b-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2ab9b-178">Search-Flags</span></span>           | <span data-ttu-id="2ab9b-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2ab9b-179">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="2ab9b-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2ab9b-180">System-Flags</span></span>           | <span data-ttu-id="2ab9b-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2ab9b-181">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="2ab9b-182">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="2ab9b-182">Classes used in</span></span>        | [<span data-ttu-id="2ab9b-183">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="2ab9b-183">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="2ab9b-184">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="2ab9b-184">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2ab9b-185">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2ab9b-185">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2ab9b-186">Entrée</span><span class="sxs-lookup"><span data-stu-id="2ab9b-186">Entry</span></span> | <span data-ttu-id="2ab9b-187">Valeur</span><span class="sxs-lookup"><span data-stu-id="2ab9b-187">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ab9b-188">ID de lien</span><span class="sxs-lookup"><span data-stu-id="2ab9b-188">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="2ab9b-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2ab9b-189">MAPI-Id</span></span>                | <span data-ttu-id="2ab9b-190">0x3A0A</span><span class="sxs-lookup"><span data-stu-id="2ab9b-190">0x3A0A</span></span>                                                                                                                 |
| <span data-ttu-id="2ab9b-191">System-Only</span><span class="sxs-lookup"><span data-stu-id="2ab9b-191">System-Only</span></span>            | <span data-ttu-id="2ab9b-192">Faux</span><span class="sxs-lookup"><span data-stu-id="2ab9b-192">False</span></span>                                                                                                                  |
| <span data-ttu-id="2ab9b-193">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="2ab9b-193">Is-Single-Valued</span></span>       | <span data-ttu-id="2ab9b-194">Vrai</span><span class="sxs-lookup"><span data-stu-id="2ab9b-194">True</span></span>                                                                                                                   |
| <span data-ttu-id="2ab9b-195">Est indexé</span><span class="sxs-lookup"><span data-stu-id="2ab9b-195">Is Indexed</span></span>             | <span data-ttu-id="2ab9b-196">Faux</span><span class="sxs-lookup"><span data-stu-id="2ab9b-196">False</span></span>                                                                                                                  |
| <span data-ttu-id="2ab9b-197">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="2ab9b-197">In Global Catalog</span></span>      | <span data-ttu-id="2ab9b-198">Faux</span><span class="sxs-lookup"><span data-stu-id="2ab9b-198">False</span></span>                                                                                                                  |
| <span data-ttu-id="2ab9b-199">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="2ab9b-199">NT-Security-Descriptor</span></span> | <span data-ttu-id="2ab9b-200">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="2ab9b-200">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="2ab9b-201">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2ab9b-201">Range-Lower</span></span>            | <span data-ttu-id="2ab9b-202">1</span><span class="sxs-lookup"><span data-stu-id="2ab9b-202">1</span></span>                                                                                                                      |
| <span data-ttu-id="2ab9b-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2ab9b-203">Range-Upper</span></span>            | <span data-ttu-id="2ab9b-204">6</span><span class="sxs-lookup"><span data-stu-id="2ab9b-204">6</span></span>                                                                                                                      |
| <span data-ttu-id="2ab9b-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2ab9b-205">Search-Flags</span></span>           | <span data-ttu-id="2ab9b-206">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2ab9b-206">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="2ab9b-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2ab9b-207">System-Flags</span></span>           | <span data-ttu-id="2ab9b-208">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2ab9b-208">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="2ab9b-209">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="2ab9b-209">Classes used in</span></span>        | [<span data-ttu-id="2ab9b-210">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="2ab9b-210">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="2ab9b-211">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="2ab9b-211">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2ab9b-212">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2ab9b-212">Windows Server 2008</span></span>



| <span data-ttu-id="2ab9b-213">Entrée</span><span class="sxs-lookup"><span data-stu-id="2ab9b-213">Entry</span></span> | <span data-ttu-id="2ab9b-214">Valeur</span><span class="sxs-lookup"><span data-stu-id="2ab9b-214">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ab9b-215">ID de lien</span><span class="sxs-lookup"><span data-stu-id="2ab9b-215">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="2ab9b-216">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2ab9b-216">MAPI-Id</span></span>                | <span data-ttu-id="2ab9b-217">0x3A0A</span><span class="sxs-lookup"><span data-stu-id="2ab9b-217">0x3A0A</span></span>                                                                                                                 |
| <span data-ttu-id="2ab9b-218">System-Only</span><span class="sxs-lookup"><span data-stu-id="2ab9b-218">System-Only</span></span>            | <span data-ttu-id="2ab9b-219">Faux</span><span class="sxs-lookup"><span data-stu-id="2ab9b-219">False</span></span>                                                                                                                  |
| <span data-ttu-id="2ab9b-220">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="2ab9b-220">Is-Single-Valued</span></span>       | <span data-ttu-id="2ab9b-221">Vrai</span><span class="sxs-lookup"><span data-stu-id="2ab9b-221">True</span></span>                                                                                                                   |
| <span data-ttu-id="2ab9b-222">Est indexé</span><span class="sxs-lookup"><span data-stu-id="2ab9b-222">Is Indexed</span></span>             | <span data-ttu-id="2ab9b-223">Faux</span><span class="sxs-lookup"><span data-stu-id="2ab9b-223">False</span></span>                                                                                                                  |
| <span data-ttu-id="2ab9b-224">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="2ab9b-224">In Global Catalog</span></span>      | <span data-ttu-id="2ab9b-225">Faux</span><span class="sxs-lookup"><span data-stu-id="2ab9b-225">False</span></span>                                                                                                                  |
| <span data-ttu-id="2ab9b-226">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="2ab9b-226">NT-Security-Descriptor</span></span> | <span data-ttu-id="2ab9b-227">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="2ab9b-227">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="2ab9b-228">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2ab9b-228">Range-Lower</span></span>            | <span data-ttu-id="2ab9b-229">1</span><span class="sxs-lookup"><span data-stu-id="2ab9b-229">1</span></span>                                                                                                                      |
| <span data-ttu-id="2ab9b-230">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2ab9b-230">Range-Upper</span></span>            | <span data-ttu-id="2ab9b-231">6</span><span class="sxs-lookup"><span data-stu-id="2ab9b-231">6</span></span>                                                                                                                      |
| <span data-ttu-id="2ab9b-232">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2ab9b-232">Search-Flags</span></span>           | <span data-ttu-id="2ab9b-233">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2ab9b-233">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="2ab9b-234">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2ab9b-234">System-Flags</span></span>           | <span data-ttu-id="2ab9b-235">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2ab9b-235">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="2ab9b-236">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="2ab9b-236">Classes used in</span></span>        | [<span data-ttu-id="2ab9b-237">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="2ab9b-237">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="2ab9b-238">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="2ab9b-238">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2ab9b-239">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2ab9b-239">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2ab9b-240">Entrée</span><span class="sxs-lookup"><span data-stu-id="2ab9b-240">Entry</span></span> | <span data-ttu-id="2ab9b-241">Valeur</span><span class="sxs-lookup"><span data-stu-id="2ab9b-241">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ab9b-242">ID de lien</span><span class="sxs-lookup"><span data-stu-id="2ab9b-242">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="2ab9b-243">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2ab9b-243">MAPI-Id</span></span>                | <span data-ttu-id="2ab9b-244">0x3A0A</span><span class="sxs-lookup"><span data-stu-id="2ab9b-244">0x3A0A</span></span>                                                                                                                 |
| <span data-ttu-id="2ab9b-245">System-Only</span><span class="sxs-lookup"><span data-stu-id="2ab9b-245">System-Only</span></span>            | <span data-ttu-id="2ab9b-246">Faux</span><span class="sxs-lookup"><span data-stu-id="2ab9b-246">False</span></span>                                                                                                                  |
| <span data-ttu-id="2ab9b-247">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="2ab9b-247">Is-Single-Valued</span></span>       | <span data-ttu-id="2ab9b-248">Vrai</span><span class="sxs-lookup"><span data-stu-id="2ab9b-248">True</span></span>                                                                                                                   |
| <span data-ttu-id="2ab9b-249">Est indexé</span><span class="sxs-lookup"><span data-stu-id="2ab9b-249">Is Indexed</span></span>             | <span data-ttu-id="2ab9b-250">Faux</span><span class="sxs-lookup"><span data-stu-id="2ab9b-250">False</span></span>                                                                                                                  |
| <span data-ttu-id="2ab9b-251">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="2ab9b-251">In Global Catalog</span></span>      | <span data-ttu-id="2ab9b-252">Faux</span><span class="sxs-lookup"><span data-stu-id="2ab9b-252">False</span></span>                                                                                                                  |
| <span data-ttu-id="2ab9b-253">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="2ab9b-253">NT-Security-Descriptor</span></span> | <span data-ttu-id="2ab9b-254">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="2ab9b-254">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="2ab9b-255">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2ab9b-255">Range-Lower</span></span>            | <span data-ttu-id="2ab9b-256">1</span><span class="sxs-lookup"><span data-stu-id="2ab9b-256">1</span></span>                                                                                                                      |
| <span data-ttu-id="2ab9b-257">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2ab9b-257">Range-Upper</span></span>            | <span data-ttu-id="2ab9b-258">6</span><span class="sxs-lookup"><span data-stu-id="2ab9b-258">6</span></span>                                                                                                                      |
| <span data-ttu-id="2ab9b-259">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2ab9b-259">Search-Flags</span></span>           | <span data-ttu-id="2ab9b-260">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2ab9b-260">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="2ab9b-261">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2ab9b-261">System-Flags</span></span>           | <span data-ttu-id="2ab9b-262">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2ab9b-262">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="2ab9b-263">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="2ab9b-263">Classes used in</span></span>        | [<span data-ttu-id="2ab9b-264">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="2ab9b-264">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="2ab9b-265">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="2ab9b-265">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2ab9b-266">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2ab9b-266">Windows Server 2012</span></span>



| <span data-ttu-id="2ab9b-267">Entrée</span><span class="sxs-lookup"><span data-stu-id="2ab9b-267">Entry</span></span> | <span data-ttu-id="2ab9b-268">Valeur</span><span class="sxs-lookup"><span data-stu-id="2ab9b-268">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ab9b-269">ID de lien</span><span class="sxs-lookup"><span data-stu-id="2ab9b-269">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="2ab9b-270">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2ab9b-270">MAPI-Id</span></span>                | <span data-ttu-id="2ab9b-271">0x3A0A</span><span class="sxs-lookup"><span data-stu-id="2ab9b-271">0x3A0A</span></span>                                                                                                                 |
| <span data-ttu-id="2ab9b-272">System-Only</span><span class="sxs-lookup"><span data-stu-id="2ab9b-272">System-Only</span></span>            | <span data-ttu-id="2ab9b-273">Faux</span><span class="sxs-lookup"><span data-stu-id="2ab9b-273">False</span></span>                                                                                                                  |
| <span data-ttu-id="2ab9b-274">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="2ab9b-274">Is-Single-Valued</span></span>       | <span data-ttu-id="2ab9b-275">Vrai</span><span class="sxs-lookup"><span data-stu-id="2ab9b-275">True</span></span>                                                                                                                   |
| <span data-ttu-id="2ab9b-276">Est indexé</span><span class="sxs-lookup"><span data-stu-id="2ab9b-276">Is Indexed</span></span>             | <span data-ttu-id="2ab9b-277">Faux</span><span class="sxs-lookup"><span data-stu-id="2ab9b-277">False</span></span>                                                                                                                  |
| <span data-ttu-id="2ab9b-278">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="2ab9b-278">In Global Catalog</span></span>      | <span data-ttu-id="2ab9b-279">Faux</span><span class="sxs-lookup"><span data-stu-id="2ab9b-279">False</span></span>                                                                                                                  |
| <span data-ttu-id="2ab9b-280">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="2ab9b-280">NT-Security-Descriptor</span></span> | <span data-ttu-id="2ab9b-281">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="2ab9b-281">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="2ab9b-282">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2ab9b-282">Range-Lower</span></span>            | <span data-ttu-id="2ab9b-283">1</span><span class="sxs-lookup"><span data-stu-id="2ab9b-283">1</span></span>                                                                                                                      |
| <span data-ttu-id="2ab9b-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2ab9b-284">Range-Upper</span></span>            | <span data-ttu-id="2ab9b-285">6</span><span class="sxs-lookup"><span data-stu-id="2ab9b-285">6</span></span>                                                                                                                      |
| <span data-ttu-id="2ab9b-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2ab9b-286">Search-Flags</span></span>           | <span data-ttu-id="2ab9b-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2ab9b-287">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="2ab9b-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2ab9b-288">System-Flags</span></span>           | <span data-ttu-id="2ab9b-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2ab9b-289">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="2ab9b-290">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="2ab9b-290">Classes used in</span></span>        | [<span data-ttu-id="2ab9b-291">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="2ab9b-291">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="2ab9b-292">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="2ab9b-292">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



 

 





