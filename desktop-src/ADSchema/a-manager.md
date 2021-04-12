---
title: Attribut Manager
description: Contient le nom unique de l’utilisateur qui est le responsable de l’utilisateur. L’objet utilisateur du gestionnaire contient une propriété directReports qui contient des références à tous les objets utilisateur dont les propriétés Manager ont pour valeur ce nom unique.
ms.assetid: 40743784-a99c-4ec0-9140-9f865c073244
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory des attributs du gestionnaire
- Schéma Active Directory des attributs du gestionnaire
topic_type:
- apiref
api_name:
- Manager
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f42c659a436f9798861f5c37df19f8d10db91127
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104385411"
---
# <a name="manager-attribute"></a><span data-ttu-id="3f4ea-106">Attribut Manager</span><span class="sxs-lookup"><span data-stu-id="3f4ea-106">Manager attribute</span></span>

<span data-ttu-id="3f4ea-107">Contient le nom unique de l’utilisateur qui est le responsable de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3f4ea-107">Contains the distinguished name of the user who is the user's manager.</span></span> <span data-ttu-id="3f4ea-108">L’objet utilisateur du gestionnaire contient une propriété directReports qui contient des références à tous les objets utilisateur dont les propriétés Manager ont pour valeur ce nom unique.</span><span class="sxs-lookup"><span data-stu-id="3f4ea-108">The manager's user object contains a directReports property that contains references to all user objects that have their manager properties set to this distinguished name.</span></span>



| <span data-ttu-id="3f4ea-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="3f4ea-109">Entry</span></span> | <span data-ttu-id="3f4ea-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="3f4ea-110">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="3f4ea-111">CN</span><span class="sxs-lookup"><span data-stu-id="3f4ea-111">CN</span></span>                | <span data-ttu-id="3f4ea-112">Manager</span><span class="sxs-lookup"><span data-stu-id="3f4ea-112">Manager</span></span>                                                                     |
| <span data-ttu-id="3f4ea-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="3f4ea-113">Ldap-Display-Name</span></span> | <span data-ttu-id="3f4ea-114">manager</span><span class="sxs-lookup"><span data-stu-id="3f4ea-114">manager</span></span>                                                                     |
| <span data-ttu-id="3f4ea-115">Taille</span><span class="sxs-lookup"><span data-stu-id="3f4ea-115">Size</span></span>              | \-                                                                          |
| <span data-ttu-id="3f4ea-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="3f4ea-116">Update Privilege</span></span>  | <span data-ttu-id="3f4ea-117">Administrateur de domaine ou propriétaire du compte.</span><span class="sxs-lookup"><span data-stu-id="3f4ea-117">Domain administrator or account owner.</span></span>                                      |
| <span data-ttu-id="3f4ea-118">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="3f4ea-118">Update Frequency</span></span>  | <span data-ttu-id="3f4ea-119">Lorsque l’enregistrement de l’utilisateur est créé et chaque fois que le gestionnaire doit être modifié.</span><span class="sxs-lookup"><span data-stu-id="3f4ea-119">When the user's record is created and whenever the manager needs to change.</span></span> |
| <span data-ttu-id="3f4ea-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="3f4ea-120">Attribute-Id</span></span>      | <span data-ttu-id="3f4ea-121">0.9.2342.19200300.100.1.10</span><span class="sxs-lookup"><span data-stu-id="3f4ea-121">0.9.2342.19200300.100.1.10</span></span>                                                  |
| <span data-ttu-id="3f4ea-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="3f4ea-122">System-Id-Guid</span></span>    | <span data-ttu-id="3f4ea-123">bf9679b5-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="3f4ea-123">bf9679b5-0de6-11d0-a285-00aa003049e2</span></span>                                        |
| <span data-ttu-id="3f4ea-124">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3f4ea-124">Syntax</span></span>            | [<span data-ttu-id="3f4ea-125">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="3f4ea-125">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)                                     |



## <a name="implementations"></a><span data-ttu-id="3f4ea-126">Implémentations</span><span class="sxs-lookup"><span data-stu-id="3f4ea-126">Implementations</span></span>

-   [<span data-ttu-id="3f4ea-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="3f4ea-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="3f4ea-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="3f4ea-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="3f4ea-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="3f4ea-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="3f4ea-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="3f4ea-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="3f4ea-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="3f4ea-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="3f4ea-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3f4ea-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="3f4ea-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3f4ea-133">Windows 2000 Server</span></span>



| <span data-ttu-id="3f4ea-134">Entrée</span><span class="sxs-lookup"><span data-stu-id="3f4ea-134">Entry</span></span> | <span data-ttu-id="3f4ea-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="3f4ea-135">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="3f4ea-136">ID de lien</span><span class="sxs-lookup"><span data-stu-id="3f4ea-136">Link-Id</span></span>                | <span data-ttu-id="3f4ea-137">42</span><span class="sxs-lookup"><span data-stu-id="3f4ea-137">42</span></span>                                                                 |
| <span data-ttu-id="3f4ea-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3f4ea-138">MAPI-Id</span></span>                | <span data-ttu-id="3f4ea-139">0x8005</span><span class="sxs-lookup"><span data-stu-id="3f4ea-139">0x8005</span></span>                                                             |
| <span data-ttu-id="3f4ea-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="3f4ea-140">System-Only</span></span>            | <span data-ttu-id="3f4ea-141">Faux</span><span class="sxs-lookup"><span data-stu-id="3f4ea-141">False</span></span>                                                              |
| <span data-ttu-id="3f4ea-142">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="3f4ea-142">Is-Single-Valued</span></span>       | <span data-ttu-id="3f4ea-143">Vrai</span><span class="sxs-lookup"><span data-stu-id="3f4ea-143">True</span></span>                                                               |
| <span data-ttu-id="3f4ea-144">Est indexé</span><span class="sxs-lookup"><span data-stu-id="3f4ea-144">Is Indexed</span></span>             | <span data-ttu-id="3f4ea-145">Faux</span><span class="sxs-lookup"><span data-stu-id="3f4ea-145">False</span></span>                                                              |
| <span data-ttu-id="3f4ea-146">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="3f4ea-146">In Global Catalog</span></span>      | <span data-ttu-id="3f4ea-147">Vrai</span><span class="sxs-lookup"><span data-stu-id="3f4ea-147">True</span></span>                                                               |
| <span data-ttu-id="3f4ea-148">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="3f4ea-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="3f4ea-149">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="3f4ea-149">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="3f4ea-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3f4ea-150">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="3f4ea-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3f4ea-151">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="3f4ea-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3f4ea-152">Search-Flags</span></span>           | <span data-ttu-id="3f4ea-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3f4ea-153">0x00000010</span></span>                                                         |
| <span data-ttu-id="3f4ea-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3f4ea-154">System-Flags</span></span>           | <span data-ttu-id="3f4ea-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3f4ea-155">0x00000010</span></span>                                                         |
| <span data-ttu-id="3f4ea-156">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="3f4ea-156">Classes used in</span></span>        | [<span data-ttu-id="3f4ea-157">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="3f4ea-157">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="3f4ea-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3f4ea-158">Windows Server 2003</span></span>



| <span data-ttu-id="3f4ea-159">Entrée</span><span class="sxs-lookup"><span data-stu-id="3f4ea-159">Entry</span></span> | <span data-ttu-id="3f4ea-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="3f4ea-160">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f4ea-161">ID de lien</span><span class="sxs-lookup"><span data-stu-id="3f4ea-161">Link-Id</span></span>                | <span data-ttu-id="3f4ea-162">42</span><span class="sxs-lookup"><span data-stu-id="3f4ea-162">42</span></span>                                                                                                                     |
| <span data-ttu-id="3f4ea-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3f4ea-163">MAPI-Id</span></span>                | <span data-ttu-id="3f4ea-164">0x8005</span><span class="sxs-lookup"><span data-stu-id="3f4ea-164">0x8005</span></span>                                                                                                                 |
| <span data-ttu-id="3f4ea-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="3f4ea-165">System-Only</span></span>            | <span data-ttu-id="3f4ea-166">Faux</span><span class="sxs-lookup"><span data-stu-id="3f4ea-166">False</span></span>                                                                                                                  |
| <span data-ttu-id="3f4ea-167">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="3f4ea-167">Is-Single-Valued</span></span>       | <span data-ttu-id="3f4ea-168">Vrai</span><span class="sxs-lookup"><span data-stu-id="3f4ea-168">True</span></span>                                                                                                                   |
| <span data-ttu-id="3f4ea-169">Est indexé</span><span class="sxs-lookup"><span data-stu-id="3f4ea-169">Is Indexed</span></span>             | <span data-ttu-id="3f4ea-170">Faux</span><span class="sxs-lookup"><span data-stu-id="3f4ea-170">False</span></span>                                                                                                                  |
| <span data-ttu-id="3f4ea-171">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="3f4ea-171">In Global Catalog</span></span>      | <span data-ttu-id="3f4ea-172">Vrai</span><span class="sxs-lookup"><span data-stu-id="3f4ea-172">True</span></span>                                                                                                                   |
| <span data-ttu-id="3f4ea-173">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="3f4ea-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="3f4ea-174">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="3f4ea-174">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="3f4ea-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3f4ea-175">Range-Lower</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="3f4ea-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3f4ea-176">Range-Upper</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="3f4ea-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3f4ea-177">Search-Flags</span></span>           | <span data-ttu-id="3f4ea-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3f4ea-178">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="3f4ea-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3f4ea-179">System-Flags</span></span>           | <span data-ttu-id="3f4ea-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3f4ea-180">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="3f4ea-181">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="3f4ea-181">Classes used in</span></span>        | [<span data-ttu-id="3f4ea-182">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="3f4ea-182">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="3f4ea-183">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="3f4ea-183">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="3f4ea-184">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="3f4ea-184">Windows Server 2003 R2</span></span>



| <span data-ttu-id="3f4ea-185">Entrée</span><span class="sxs-lookup"><span data-stu-id="3f4ea-185">Entry</span></span> | <span data-ttu-id="3f4ea-186">Valeur</span><span class="sxs-lookup"><span data-stu-id="3f4ea-186">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f4ea-187">ID de lien</span><span class="sxs-lookup"><span data-stu-id="3f4ea-187">Link-Id</span></span>                | <span data-ttu-id="3f4ea-188">42</span><span class="sxs-lookup"><span data-stu-id="3f4ea-188">42</span></span>                                                                                                                     |
| <span data-ttu-id="3f4ea-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3f4ea-189">MAPI-Id</span></span>                | <span data-ttu-id="3f4ea-190">0x8005</span><span class="sxs-lookup"><span data-stu-id="3f4ea-190">0x8005</span></span>                                                                                                                 |
| <span data-ttu-id="3f4ea-191">System-Only</span><span class="sxs-lookup"><span data-stu-id="3f4ea-191">System-Only</span></span>            | <span data-ttu-id="3f4ea-192">Faux</span><span class="sxs-lookup"><span data-stu-id="3f4ea-192">False</span></span>                                                                                                                  |
| <span data-ttu-id="3f4ea-193">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="3f4ea-193">Is-Single-Valued</span></span>       | <span data-ttu-id="3f4ea-194">Vrai</span><span class="sxs-lookup"><span data-stu-id="3f4ea-194">True</span></span>                                                                                                                   |
| <span data-ttu-id="3f4ea-195">Est indexé</span><span class="sxs-lookup"><span data-stu-id="3f4ea-195">Is Indexed</span></span>             | <span data-ttu-id="3f4ea-196">Faux</span><span class="sxs-lookup"><span data-stu-id="3f4ea-196">False</span></span>                                                                                                                  |
| <span data-ttu-id="3f4ea-197">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="3f4ea-197">In Global Catalog</span></span>      | <span data-ttu-id="3f4ea-198">Vrai</span><span class="sxs-lookup"><span data-stu-id="3f4ea-198">True</span></span>                                                                                                                   |
| <span data-ttu-id="3f4ea-199">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="3f4ea-199">NT-Security-Descriptor</span></span> | <span data-ttu-id="3f4ea-200">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="3f4ea-200">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="3f4ea-201">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3f4ea-201">Range-Lower</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="3f4ea-202">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3f4ea-202">Range-Upper</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="3f4ea-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3f4ea-203">Search-Flags</span></span>           | <span data-ttu-id="3f4ea-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3f4ea-204">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="3f4ea-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3f4ea-205">System-Flags</span></span>           | <span data-ttu-id="3f4ea-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3f4ea-206">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="3f4ea-207">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="3f4ea-207">Classes used in</span></span>        | [<span data-ttu-id="3f4ea-208">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="3f4ea-208">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="3f4ea-209">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="3f4ea-209">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="3f4ea-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3f4ea-210">Windows Server 2008</span></span>



| <span data-ttu-id="3f4ea-211">Entrée</span><span class="sxs-lookup"><span data-stu-id="3f4ea-211">Entry</span></span> | <span data-ttu-id="3f4ea-212">Valeur</span><span class="sxs-lookup"><span data-stu-id="3f4ea-212">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f4ea-213">ID de lien</span><span class="sxs-lookup"><span data-stu-id="3f4ea-213">Link-Id</span></span>                | <span data-ttu-id="3f4ea-214">42</span><span class="sxs-lookup"><span data-stu-id="3f4ea-214">42</span></span>                                                                                                                     |
| <span data-ttu-id="3f4ea-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3f4ea-215">MAPI-Id</span></span>                | <span data-ttu-id="3f4ea-216">0x8005</span><span class="sxs-lookup"><span data-stu-id="3f4ea-216">0x8005</span></span>                                                                                                                 |
| <span data-ttu-id="3f4ea-217">System-Only</span><span class="sxs-lookup"><span data-stu-id="3f4ea-217">System-Only</span></span>            | <span data-ttu-id="3f4ea-218">Faux</span><span class="sxs-lookup"><span data-stu-id="3f4ea-218">False</span></span>                                                                                                                  |
| <span data-ttu-id="3f4ea-219">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="3f4ea-219">Is-Single-Valued</span></span>       | <span data-ttu-id="3f4ea-220">Vrai</span><span class="sxs-lookup"><span data-stu-id="3f4ea-220">True</span></span>                                                                                                                   |
| <span data-ttu-id="3f4ea-221">Est indexé</span><span class="sxs-lookup"><span data-stu-id="3f4ea-221">Is Indexed</span></span>             | <span data-ttu-id="3f4ea-222">Faux</span><span class="sxs-lookup"><span data-stu-id="3f4ea-222">False</span></span>                                                                                                                  |
| <span data-ttu-id="3f4ea-223">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="3f4ea-223">In Global Catalog</span></span>      | <span data-ttu-id="3f4ea-224">Vrai</span><span class="sxs-lookup"><span data-stu-id="3f4ea-224">True</span></span>                                                                                                                   |
| <span data-ttu-id="3f4ea-225">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="3f4ea-225">NT-Security-Descriptor</span></span> | <span data-ttu-id="3f4ea-226">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="3f4ea-226">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="3f4ea-227">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3f4ea-227">Range-Lower</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="3f4ea-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3f4ea-228">Range-Upper</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="3f4ea-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3f4ea-229">Search-Flags</span></span>           | <span data-ttu-id="3f4ea-230">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3f4ea-230">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="3f4ea-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3f4ea-231">System-Flags</span></span>           | <span data-ttu-id="3f4ea-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3f4ea-232">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="3f4ea-233">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="3f4ea-233">Classes used in</span></span>        | [<span data-ttu-id="3f4ea-234">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="3f4ea-234">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="3f4ea-235">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="3f4ea-235">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="3f4ea-236">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3f4ea-236">Windows Server 2008 R2</span></span>



| <span data-ttu-id="3f4ea-237">Entrée</span><span class="sxs-lookup"><span data-stu-id="3f4ea-237">Entry</span></span> | <span data-ttu-id="3f4ea-238">Valeur</span><span class="sxs-lookup"><span data-stu-id="3f4ea-238">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f4ea-239">ID de lien</span><span class="sxs-lookup"><span data-stu-id="3f4ea-239">Link-Id</span></span>                | <span data-ttu-id="3f4ea-240">42</span><span class="sxs-lookup"><span data-stu-id="3f4ea-240">42</span></span>                                                                                                                     |
| <span data-ttu-id="3f4ea-241">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3f4ea-241">MAPI-Id</span></span>                | <span data-ttu-id="3f4ea-242">0x8005</span><span class="sxs-lookup"><span data-stu-id="3f4ea-242">0x8005</span></span>                                                                                                                 |
| <span data-ttu-id="3f4ea-243">System-Only</span><span class="sxs-lookup"><span data-stu-id="3f4ea-243">System-Only</span></span>            | <span data-ttu-id="3f4ea-244">Faux</span><span class="sxs-lookup"><span data-stu-id="3f4ea-244">False</span></span>                                                                                                                  |
| <span data-ttu-id="3f4ea-245">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="3f4ea-245">Is-Single-Valued</span></span>       | <span data-ttu-id="3f4ea-246">Vrai</span><span class="sxs-lookup"><span data-stu-id="3f4ea-246">True</span></span>                                                                                                                   |
| <span data-ttu-id="3f4ea-247">Est indexé</span><span class="sxs-lookup"><span data-stu-id="3f4ea-247">Is Indexed</span></span>             | <span data-ttu-id="3f4ea-248">Faux</span><span class="sxs-lookup"><span data-stu-id="3f4ea-248">False</span></span>                                                                                                                  |
| <span data-ttu-id="3f4ea-249">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="3f4ea-249">In Global Catalog</span></span>      | <span data-ttu-id="3f4ea-250">Vrai</span><span class="sxs-lookup"><span data-stu-id="3f4ea-250">True</span></span>                                                                                                                   |
| <span data-ttu-id="3f4ea-251">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="3f4ea-251">NT-Security-Descriptor</span></span> | <span data-ttu-id="3f4ea-252">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="3f4ea-252">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="3f4ea-253">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3f4ea-253">Range-Lower</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="3f4ea-254">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3f4ea-254">Range-Upper</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="3f4ea-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3f4ea-255">Search-Flags</span></span>           | <span data-ttu-id="3f4ea-256">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3f4ea-256">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="3f4ea-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3f4ea-257">System-Flags</span></span>           | <span data-ttu-id="3f4ea-258">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3f4ea-258">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="3f4ea-259">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="3f4ea-259">Classes used in</span></span>        | [<span data-ttu-id="3f4ea-260">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="3f4ea-260">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="3f4ea-261">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="3f4ea-261">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="3f4ea-262">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3f4ea-262">Windows Server 2012</span></span>



| <span data-ttu-id="3f4ea-263">Entrée</span><span class="sxs-lookup"><span data-stu-id="3f4ea-263">Entry</span></span> | <span data-ttu-id="3f4ea-264">Valeur</span><span class="sxs-lookup"><span data-stu-id="3f4ea-264">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f4ea-265">ID de lien</span><span class="sxs-lookup"><span data-stu-id="3f4ea-265">Link-Id</span></span>                | <span data-ttu-id="3f4ea-266">42</span><span class="sxs-lookup"><span data-stu-id="3f4ea-266">42</span></span>                                                                                                                     |
| <span data-ttu-id="3f4ea-267">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3f4ea-267">MAPI-Id</span></span>                | <span data-ttu-id="3f4ea-268">0x8005</span><span class="sxs-lookup"><span data-stu-id="3f4ea-268">0x8005</span></span>                                                                                                                 |
| <span data-ttu-id="3f4ea-269">System-Only</span><span class="sxs-lookup"><span data-stu-id="3f4ea-269">System-Only</span></span>            | <span data-ttu-id="3f4ea-270">Faux</span><span class="sxs-lookup"><span data-stu-id="3f4ea-270">False</span></span>                                                                                                                  |
| <span data-ttu-id="3f4ea-271">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="3f4ea-271">Is-Single-Valued</span></span>       | <span data-ttu-id="3f4ea-272">Vrai</span><span class="sxs-lookup"><span data-stu-id="3f4ea-272">True</span></span>                                                                                                                   |
| <span data-ttu-id="3f4ea-273">Est indexé</span><span class="sxs-lookup"><span data-stu-id="3f4ea-273">Is Indexed</span></span>             | <span data-ttu-id="3f4ea-274">Faux</span><span class="sxs-lookup"><span data-stu-id="3f4ea-274">False</span></span>                                                                                                                  |
| <span data-ttu-id="3f4ea-275">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="3f4ea-275">In Global Catalog</span></span>      | <span data-ttu-id="3f4ea-276">Vrai</span><span class="sxs-lookup"><span data-stu-id="3f4ea-276">True</span></span>                                                                                                                   |
| <span data-ttu-id="3f4ea-277">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="3f4ea-277">NT-Security-Descriptor</span></span> | <span data-ttu-id="3f4ea-278">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="3f4ea-278">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="3f4ea-279">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3f4ea-279">Range-Lower</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="3f4ea-280">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3f4ea-280">Range-Upper</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="3f4ea-281">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3f4ea-281">Search-Flags</span></span>           | <span data-ttu-id="3f4ea-282">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3f4ea-282">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="3f4ea-283">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3f4ea-283">System-Flags</span></span>           | <span data-ttu-id="3f4ea-284">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3f4ea-284">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="3f4ea-285">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="3f4ea-285">Classes used in</span></span>        | [<span data-ttu-id="3f4ea-286">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="3f4ea-286">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="3f4ea-287">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="3f4ea-287">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



 

 





