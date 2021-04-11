---
title: Shell-Property-pages (attribut)
description: Le numéro d’ordre et le GUID des pages de propriétés pour la gestion des objets Active Directory. Ces pages de propriétés sont accessibles à partir du shell Windows. Pour plus d’informations, consultez le document, extension de l’interface utilisateur pour les objets d’annuaire.
ms.assetid: e0edd91b-bdb6-47aa-9be2-8a23a89adb26
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory de l’attribut Shell-Property-pages
- Schéma AD de l’attribut shellPropertyPages
topic_type:
- apiref
api_name:
- Shell-Property-Pages
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: befad2334a754843fa0ae412565db8c82260f7cd
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107524"
---
# <a name="shell-property-pages-attribute"></a><span data-ttu-id="b4288-107">Shell-Property-pages (attribut)</span><span class="sxs-lookup"><span data-stu-id="b4288-107">Shell-Property-Pages attribute</span></span>

<span data-ttu-id="b4288-108">Le numéro d’ordre et le GUID des pages de propriétés pour la gestion des objets Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b4288-108">The order number and GUID of property pages for managing Active Directory objects.</span></span> <span data-ttu-id="b4288-109">Ces pages de propriétés sont accessibles à partir du shell Windows.</span><span class="sxs-lookup"><span data-stu-id="b4288-109">These property pages can be accessed from the Windows shell.</span></span> <span data-ttu-id="b4288-110">Pour plus d’informations, consultez le document, extension de l’interface utilisateur pour les objets d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="b4288-110">For more information see the document, Extending the User Interface for Directory Objects.</span></span>



| <span data-ttu-id="b4288-111">Entrée</span><span class="sxs-lookup"><span data-stu-id="b4288-111">Entry</span></span> | <span data-ttu-id="b4288-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4288-112">Value</span></span> |
|-------------------|------------------------------------------------|
| <span data-ttu-id="b4288-113">CN</span><span class="sxs-lookup"><span data-stu-id="b4288-113">CN</span></span>                | <span data-ttu-id="b4288-114">Shell-Property-pages</span><span class="sxs-lookup"><span data-stu-id="b4288-114">Shell-Property-Pages</span></span>                           |
| <span data-ttu-id="b4288-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="b4288-115">Ldap-Display-Name</span></span> | <span data-ttu-id="b4288-116">shellPropertyPages</span><span class="sxs-lookup"><span data-stu-id="b4288-116">shellPropertyPages</span></span>                             |
| <span data-ttu-id="b4288-117">Taille</span><span class="sxs-lookup"><span data-stu-id="b4288-117">Size</span></span>              | \-                                             |
| <span data-ttu-id="b4288-118">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="b4288-118">Update Privilege</span></span>  | <span data-ttu-id="b4288-119">Administrateur de domaine ou développeur d’applications.</span><span class="sxs-lookup"><span data-stu-id="b4288-119">Domain administrator or application developer.</span></span> |
| <span data-ttu-id="b4288-120">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="b4288-120">Update Frequency</span></span>  | <span data-ttu-id="b4288-121">Chaque fois qu’une page de propriétés est ajoutée ou supprimée.</span><span class="sxs-lookup"><span data-stu-id="b4288-121">Whenever a property page is added or removed.</span></span>  |
| <span data-ttu-id="b4288-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b4288-122">Attribute-Id</span></span>      | <span data-ttu-id="b4288-123">1.2.840.113556.1.4.563</span><span class="sxs-lookup"><span data-stu-id="b4288-123">1.2.840.113556.1.4.563</span></span>                         |
| <span data-ttu-id="b4288-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b4288-124">System-Id-Guid</span></span>    | <span data-ttu-id="b4288-125">52458039-ca6a-11D0-AFFF-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="b4288-125">52458039-ca6a-11d0-afff-0000f80367c1</span></span>           |
| <span data-ttu-id="b4288-126">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b4288-126">Syntax</span></span>            | [<span data-ttu-id="b4288-127">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="b4288-127">**String(Unicode)**</span></span>](s-string-unicode.md)    |



## <a name="implementations"></a><span data-ttu-id="b4288-128">Implémentations</span><span class="sxs-lookup"><span data-stu-id="b4288-128">Implementations</span></span>

-   [<span data-ttu-id="b4288-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b4288-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b4288-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b4288-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b4288-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b4288-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b4288-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b4288-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b4288-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b4288-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b4288-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b4288-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b4288-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b4288-135">Windows 2000 Server</span></span>



| <span data-ttu-id="b4288-136">Entrée</span><span class="sxs-lookup"><span data-stu-id="b4288-136">Entry</span></span> | <span data-ttu-id="b4288-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4288-137">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="b4288-138">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b4288-138">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="b4288-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4288-139">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="b4288-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4288-140">System-Only</span></span>            | <span data-ttu-id="b4288-141">Faux</span><span class="sxs-lookup"><span data-stu-id="b4288-141">False</span></span>                                                      |
| <span data-ttu-id="b4288-142">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b4288-142">Is-Single-Valued</span></span>       | <span data-ttu-id="b4288-143">Faux</span><span class="sxs-lookup"><span data-stu-id="b4288-143">False</span></span>                                                      |
| <span data-ttu-id="b4288-144">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b4288-144">Is Indexed</span></span>             | <span data-ttu-id="b4288-145">Faux</span><span class="sxs-lookup"><span data-stu-id="b4288-145">False</span></span>                                                      |
| <span data-ttu-id="b4288-146">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b4288-146">In Global Catalog</span></span>      | <span data-ttu-id="b4288-147">Faux</span><span class="sxs-lookup"><span data-stu-id="b4288-147">False</span></span>                                                      |
| <span data-ttu-id="b4288-148">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b4288-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4288-149">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b4288-149">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="b4288-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4288-150">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="b4288-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4288-151">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="b4288-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4288-152">Search-Flags</span></span>           | <span data-ttu-id="b4288-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b4288-153">0x00000000</span></span>                                                 |
| <span data-ttu-id="b4288-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4288-154">System-Flags</span></span>           | <span data-ttu-id="b4288-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b4288-155">0x00000010</span></span>                                                 |
| <span data-ttu-id="b4288-156">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b4288-156">Classes used in</span></span>        | [<span data-ttu-id="b4288-157">**Display-specifier**</span><span class="sxs-lookup"><span data-stu-id="b4288-157">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b4288-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b4288-158">Windows Server 2003</span></span>



| <span data-ttu-id="b4288-159">Entrée</span><span class="sxs-lookup"><span data-stu-id="b4288-159">Entry</span></span> | <span data-ttu-id="b4288-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4288-160">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="b4288-161">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b4288-161">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="b4288-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4288-162">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="b4288-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4288-163">System-Only</span></span>            | <span data-ttu-id="b4288-164">Faux</span><span class="sxs-lookup"><span data-stu-id="b4288-164">False</span></span>                                                      |
| <span data-ttu-id="b4288-165">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b4288-165">Is-Single-Valued</span></span>       | <span data-ttu-id="b4288-166">Faux</span><span class="sxs-lookup"><span data-stu-id="b4288-166">False</span></span>                                                      |
| <span data-ttu-id="b4288-167">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b4288-167">Is Indexed</span></span>             | <span data-ttu-id="b4288-168">Faux</span><span class="sxs-lookup"><span data-stu-id="b4288-168">False</span></span>                                                      |
| <span data-ttu-id="b4288-169">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b4288-169">In Global Catalog</span></span>      | <span data-ttu-id="b4288-170">Faux</span><span class="sxs-lookup"><span data-stu-id="b4288-170">False</span></span>                                                      |
| <span data-ttu-id="b4288-171">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b4288-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4288-172">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b4288-172">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="b4288-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4288-173">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="b4288-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4288-174">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="b4288-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4288-175">Search-Flags</span></span>           | <span data-ttu-id="b4288-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b4288-176">0x00000000</span></span>                                                 |
| <span data-ttu-id="b4288-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4288-177">System-Flags</span></span>           | <span data-ttu-id="b4288-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b4288-178">0x00000010</span></span>                                                 |
| <span data-ttu-id="b4288-179">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b4288-179">Classes used in</span></span>        | [<span data-ttu-id="b4288-180">**Display-specifier**</span><span class="sxs-lookup"><span data-stu-id="b4288-180">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b4288-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b4288-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b4288-182">Entrée</span><span class="sxs-lookup"><span data-stu-id="b4288-182">Entry</span></span> | <span data-ttu-id="b4288-183">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4288-183">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="b4288-184">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b4288-184">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="b4288-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4288-185">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="b4288-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4288-186">System-Only</span></span>            | <span data-ttu-id="b4288-187">Faux</span><span class="sxs-lookup"><span data-stu-id="b4288-187">False</span></span>                                                      |
| <span data-ttu-id="b4288-188">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b4288-188">Is-Single-Valued</span></span>       | <span data-ttu-id="b4288-189">Faux</span><span class="sxs-lookup"><span data-stu-id="b4288-189">False</span></span>                                                      |
| <span data-ttu-id="b4288-190">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b4288-190">Is Indexed</span></span>             | <span data-ttu-id="b4288-191">Faux</span><span class="sxs-lookup"><span data-stu-id="b4288-191">False</span></span>                                                      |
| <span data-ttu-id="b4288-192">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b4288-192">In Global Catalog</span></span>      | <span data-ttu-id="b4288-193">Faux</span><span class="sxs-lookup"><span data-stu-id="b4288-193">False</span></span>                                                      |
| <span data-ttu-id="b4288-194">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b4288-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4288-195">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b4288-195">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="b4288-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4288-196">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="b4288-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4288-197">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="b4288-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4288-198">Search-Flags</span></span>           | <span data-ttu-id="b4288-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b4288-199">0x00000000</span></span>                                                 |
| <span data-ttu-id="b4288-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4288-200">System-Flags</span></span>           | <span data-ttu-id="b4288-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b4288-201">0x00000010</span></span>                                                 |
| <span data-ttu-id="b4288-202">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b4288-202">Classes used in</span></span>        | [<span data-ttu-id="b4288-203">**Display-specifier**</span><span class="sxs-lookup"><span data-stu-id="b4288-203">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b4288-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b4288-204">Windows Server 2008</span></span>



| <span data-ttu-id="b4288-205">Entrée</span><span class="sxs-lookup"><span data-stu-id="b4288-205">Entry</span></span> | <span data-ttu-id="b4288-206">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4288-206">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="b4288-207">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b4288-207">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="b4288-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4288-208">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="b4288-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4288-209">System-Only</span></span>            | <span data-ttu-id="b4288-210">Faux</span><span class="sxs-lookup"><span data-stu-id="b4288-210">False</span></span>                                                      |
| <span data-ttu-id="b4288-211">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b4288-211">Is-Single-Valued</span></span>       | <span data-ttu-id="b4288-212">Faux</span><span class="sxs-lookup"><span data-stu-id="b4288-212">False</span></span>                                                      |
| <span data-ttu-id="b4288-213">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b4288-213">Is Indexed</span></span>             | <span data-ttu-id="b4288-214">Faux</span><span class="sxs-lookup"><span data-stu-id="b4288-214">False</span></span>                                                      |
| <span data-ttu-id="b4288-215">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b4288-215">In Global Catalog</span></span>      | <span data-ttu-id="b4288-216">Faux</span><span class="sxs-lookup"><span data-stu-id="b4288-216">False</span></span>                                                      |
| <span data-ttu-id="b4288-217">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b4288-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4288-218">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b4288-218">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="b4288-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4288-219">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="b4288-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4288-220">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="b4288-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4288-221">Search-Flags</span></span>           | <span data-ttu-id="b4288-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b4288-222">0x00000000</span></span>                                                 |
| <span data-ttu-id="b4288-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4288-223">System-Flags</span></span>           | <span data-ttu-id="b4288-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b4288-224">0x00000010</span></span>                                                 |
| <span data-ttu-id="b4288-225">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b4288-225">Classes used in</span></span>        | [<span data-ttu-id="b4288-226">**Display-specifier**</span><span class="sxs-lookup"><span data-stu-id="b4288-226">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b4288-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b4288-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b4288-228">Entrée</span><span class="sxs-lookup"><span data-stu-id="b4288-228">Entry</span></span> | <span data-ttu-id="b4288-229">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4288-229">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="b4288-230">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b4288-230">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="b4288-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4288-231">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="b4288-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4288-232">System-Only</span></span>            | <span data-ttu-id="b4288-233">Faux</span><span class="sxs-lookup"><span data-stu-id="b4288-233">False</span></span>                                                      |
| <span data-ttu-id="b4288-234">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b4288-234">Is-Single-Valued</span></span>       | <span data-ttu-id="b4288-235">Faux</span><span class="sxs-lookup"><span data-stu-id="b4288-235">False</span></span>                                                      |
| <span data-ttu-id="b4288-236">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b4288-236">Is Indexed</span></span>             | <span data-ttu-id="b4288-237">Faux</span><span class="sxs-lookup"><span data-stu-id="b4288-237">False</span></span>                                                      |
| <span data-ttu-id="b4288-238">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b4288-238">In Global Catalog</span></span>      | <span data-ttu-id="b4288-239">Faux</span><span class="sxs-lookup"><span data-stu-id="b4288-239">False</span></span>                                                      |
| <span data-ttu-id="b4288-240">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b4288-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4288-241">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b4288-241">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="b4288-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4288-242">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="b4288-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4288-243">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="b4288-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4288-244">Search-Flags</span></span>           | <span data-ttu-id="b4288-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b4288-245">0x00000000</span></span>                                                 |
| <span data-ttu-id="b4288-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4288-246">System-Flags</span></span>           | <span data-ttu-id="b4288-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b4288-247">0x00000010</span></span>                                                 |
| <span data-ttu-id="b4288-248">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b4288-248">Classes used in</span></span>        | [<span data-ttu-id="b4288-249">**Display-specifier**</span><span class="sxs-lookup"><span data-stu-id="b4288-249">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b4288-250">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b4288-250">Windows Server 2012</span></span>



| <span data-ttu-id="b4288-251">Entrée</span><span class="sxs-lookup"><span data-stu-id="b4288-251">Entry</span></span> | <span data-ttu-id="b4288-252">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4288-252">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="b4288-253">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b4288-253">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="b4288-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4288-254">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="b4288-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4288-255">System-Only</span></span>            | <span data-ttu-id="b4288-256">Faux</span><span class="sxs-lookup"><span data-stu-id="b4288-256">False</span></span>                                                      |
| <span data-ttu-id="b4288-257">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b4288-257">Is-Single-Valued</span></span>       | <span data-ttu-id="b4288-258">Faux</span><span class="sxs-lookup"><span data-stu-id="b4288-258">False</span></span>                                                      |
| <span data-ttu-id="b4288-259">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b4288-259">Is Indexed</span></span>             | <span data-ttu-id="b4288-260">Faux</span><span class="sxs-lookup"><span data-stu-id="b4288-260">False</span></span>                                                      |
| <span data-ttu-id="b4288-261">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b4288-261">In Global Catalog</span></span>      | <span data-ttu-id="b4288-262">Faux</span><span class="sxs-lookup"><span data-stu-id="b4288-262">False</span></span>                                                      |
| <span data-ttu-id="b4288-263">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b4288-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4288-264">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b4288-264">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="b4288-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4288-265">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="b4288-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4288-266">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="b4288-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4288-267">Search-Flags</span></span>           | <span data-ttu-id="b4288-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b4288-268">0x00000000</span></span>                                                 |
| <span data-ttu-id="b4288-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4288-269">System-Flags</span></span>           | <span data-ttu-id="b4288-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b4288-270">0x00000010</span></span>                                                 |
| <span data-ttu-id="b4288-271">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b4288-271">Classes used in</span></span>        | [<span data-ttu-id="b4288-272">**Display-specifier**</span><span class="sxs-lookup"><span data-stu-id="b4288-272">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



 

 





