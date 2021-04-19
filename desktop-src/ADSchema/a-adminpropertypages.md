---
title: Attribut admin-Property-pages
description: Le numéro d’ordre et le GUID des pages de propriétés d’un objet à afficher sur les écrans d’administration Active Directory. Pour plus d’informations, consultez le document, extension de l’interface utilisateur pour les objets d’annuaire.
ms.assetid: 70455768-11e0-4d12-ad44-4b3115aa1594
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory de l’attribut admin-Property-pages
- Schéma AD de l’attribut adminPropertyPages
topic_type:
- apiref
api_name:
- Admin-Property-Pages
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97d4e3814662cc8acf1a987cb92a1b9579cc43a4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106515726"
---
# <a name="admin-property-pages-attribute"></a><span data-ttu-id="dac51-106">Attribut admin-Property-pages</span><span class="sxs-lookup"><span data-stu-id="dac51-106">Admin-Property-Pages attribute</span></span>

<span data-ttu-id="dac51-107">Le numéro d’ordre et le GUID des pages de propriétés d’un objet à afficher sur les écrans d’administration Active Directory.</span><span class="sxs-lookup"><span data-stu-id="dac51-107">The order number and GUID of the property pages for an object to be displayed on Active Directory administration screens.</span></span> <span data-ttu-id="dac51-108">Pour plus d’informations, consultez le document, extension de l’interface utilisateur pour les objets d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="dac51-108">For more information see the document, Extending the User Interface for Directory Objects.</span></span>



| <span data-ttu-id="dac51-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="dac51-109">Entry</span></span> | <span data-ttu-id="dac51-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="dac51-110">Value</span></span> |
|-------------------|------------------------------------------------|
| <span data-ttu-id="dac51-111">CN</span><span class="sxs-lookup"><span data-stu-id="dac51-111">CN</span></span>                | <span data-ttu-id="dac51-112">Admin-propriété-pages</span><span class="sxs-lookup"><span data-stu-id="dac51-112">Admin-Property-Pages</span></span>                           |
| <span data-ttu-id="dac51-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="dac51-113">Ldap-Display-Name</span></span> | <span data-ttu-id="dac51-114">adminPropertyPages</span><span class="sxs-lookup"><span data-stu-id="dac51-114">adminPropertyPages</span></span>                             |
| <span data-ttu-id="dac51-115">Taille</span><span class="sxs-lookup"><span data-stu-id="dac51-115">Size</span></span>              | \-                                             |
| <span data-ttu-id="dac51-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="dac51-116">Update Privilege</span></span>  | <span data-ttu-id="dac51-117">Administrateur de domaine ou développeur d’applications.</span><span class="sxs-lookup"><span data-stu-id="dac51-117">Domain administrator or application developer.</span></span> |
| <span data-ttu-id="dac51-118">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="dac51-118">Update Frequency</span></span>  | <span data-ttu-id="dac51-119">Chaque fois qu’une page de propriétés est ajoutée ou supprimée.</span><span class="sxs-lookup"><span data-stu-id="dac51-119">Whenever a property page is added or removed.</span></span>  |
| <span data-ttu-id="dac51-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="dac51-120">Attribute-Id</span></span>      | <span data-ttu-id="dac51-121">1.2.840.113556.1.4.562</span><span class="sxs-lookup"><span data-stu-id="dac51-121">1.2.840.113556.1.4.562</span></span>                         |
| <span data-ttu-id="dac51-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="dac51-122">System-Id-Guid</span></span>    | <span data-ttu-id="dac51-123">52458038-ca6a-11D0-AFFF-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="dac51-123">52458038-ca6a-11d0-afff-0000f80367c1</span></span>           |
| <span data-ttu-id="dac51-124">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dac51-124">Syntax</span></span>            | [<span data-ttu-id="dac51-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="dac51-125">**String(Unicode)**</span></span>](s-string-unicode.md)    |



## <a name="implementations"></a><span data-ttu-id="dac51-126">Implémentations</span><span class="sxs-lookup"><span data-stu-id="dac51-126">Implementations</span></span>

-   [<span data-ttu-id="dac51-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="dac51-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="dac51-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="dac51-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="dac51-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="dac51-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="dac51-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="dac51-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="dac51-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="dac51-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="dac51-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="dac51-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="dac51-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="dac51-133">Windows 2000 Server</span></span>



| <span data-ttu-id="dac51-134">Entrée</span><span class="sxs-lookup"><span data-stu-id="dac51-134">Entry</span></span> | <span data-ttu-id="dac51-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="dac51-135">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="dac51-136">ID de lien</span><span class="sxs-lookup"><span data-stu-id="dac51-136">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="dac51-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dac51-137">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="dac51-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="dac51-138">System-Only</span></span>            | <span data-ttu-id="dac51-139">Faux</span><span class="sxs-lookup"><span data-stu-id="dac51-139">False</span></span>                                                      |
| <span data-ttu-id="dac51-140">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="dac51-140">Is-Single-Valued</span></span>       | <span data-ttu-id="dac51-141">Faux</span><span class="sxs-lookup"><span data-stu-id="dac51-141">False</span></span>                                                      |
| <span data-ttu-id="dac51-142">Est indexé</span><span class="sxs-lookup"><span data-stu-id="dac51-142">Is Indexed</span></span>             | <span data-ttu-id="dac51-143">Faux</span><span class="sxs-lookup"><span data-stu-id="dac51-143">False</span></span>                                                      |
| <span data-ttu-id="dac51-144">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="dac51-144">In Global Catalog</span></span>      | <span data-ttu-id="dac51-145">Faux</span><span class="sxs-lookup"><span data-stu-id="dac51-145">False</span></span>                                                      |
| <span data-ttu-id="dac51-146">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="dac51-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="dac51-147">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="dac51-147">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="dac51-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dac51-148">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="dac51-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dac51-149">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="dac51-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dac51-150">Search-Flags</span></span>           | <span data-ttu-id="dac51-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dac51-151">0x00000000</span></span>                                                 |
| <span data-ttu-id="dac51-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dac51-152">System-Flags</span></span>           | <span data-ttu-id="dac51-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dac51-153">0x00000010</span></span>                                                 |
| <span data-ttu-id="dac51-154">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="dac51-154">Classes used in</span></span>        | [<span data-ttu-id="dac51-155">**Display-specifier**</span><span class="sxs-lookup"><span data-stu-id="dac51-155">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="dac51-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="dac51-156">Windows Server 2003</span></span>



| <span data-ttu-id="dac51-157">Entrée</span><span class="sxs-lookup"><span data-stu-id="dac51-157">Entry</span></span> | <span data-ttu-id="dac51-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="dac51-158">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="dac51-159">ID de lien</span><span class="sxs-lookup"><span data-stu-id="dac51-159">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="dac51-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dac51-160">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="dac51-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="dac51-161">System-Only</span></span>            | <span data-ttu-id="dac51-162">Faux</span><span class="sxs-lookup"><span data-stu-id="dac51-162">False</span></span>                                                      |
| <span data-ttu-id="dac51-163">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="dac51-163">Is-Single-Valued</span></span>       | <span data-ttu-id="dac51-164">Faux</span><span class="sxs-lookup"><span data-stu-id="dac51-164">False</span></span>                                                      |
| <span data-ttu-id="dac51-165">Est indexé</span><span class="sxs-lookup"><span data-stu-id="dac51-165">Is Indexed</span></span>             | <span data-ttu-id="dac51-166">Faux</span><span class="sxs-lookup"><span data-stu-id="dac51-166">False</span></span>                                                      |
| <span data-ttu-id="dac51-167">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="dac51-167">In Global Catalog</span></span>      | <span data-ttu-id="dac51-168">Faux</span><span class="sxs-lookup"><span data-stu-id="dac51-168">False</span></span>                                                      |
| <span data-ttu-id="dac51-169">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="dac51-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="dac51-170">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="dac51-170">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="dac51-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dac51-171">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="dac51-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dac51-172">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="dac51-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dac51-173">Search-Flags</span></span>           | <span data-ttu-id="dac51-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dac51-174">0x00000000</span></span>                                                 |
| <span data-ttu-id="dac51-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dac51-175">System-Flags</span></span>           | <span data-ttu-id="dac51-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dac51-176">0x00000010</span></span>                                                 |
| <span data-ttu-id="dac51-177">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="dac51-177">Classes used in</span></span>        | [<span data-ttu-id="dac51-178">**Display-specifier**</span><span class="sxs-lookup"><span data-stu-id="dac51-178">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="dac51-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="dac51-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="dac51-180">Entrée</span><span class="sxs-lookup"><span data-stu-id="dac51-180">Entry</span></span> | <span data-ttu-id="dac51-181">Valeur</span><span class="sxs-lookup"><span data-stu-id="dac51-181">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="dac51-182">ID de lien</span><span class="sxs-lookup"><span data-stu-id="dac51-182">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="dac51-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dac51-183">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="dac51-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="dac51-184">System-Only</span></span>            | <span data-ttu-id="dac51-185">Faux</span><span class="sxs-lookup"><span data-stu-id="dac51-185">False</span></span>                                                      |
| <span data-ttu-id="dac51-186">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="dac51-186">Is-Single-Valued</span></span>       | <span data-ttu-id="dac51-187">Faux</span><span class="sxs-lookup"><span data-stu-id="dac51-187">False</span></span>                                                      |
| <span data-ttu-id="dac51-188">Est indexé</span><span class="sxs-lookup"><span data-stu-id="dac51-188">Is Indexed</span></span>             | <span data-ttu-id="dac51-189">Faux</span><span class="sxs-lookup"><span data-stu-id="dac51-189">False</span></span>                                                      |
| <span data-ttu-id="dac51-190">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="dac51-190">In Global Catalog</span></span>      | <span data-ttu-id="dac51-191">Faux</span><span class="sxs-lookup"><span data-stu-id="dac51-191">False</span></span>                                                      |
| <span data-ttu-id="dac51-192">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="dac51-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="dac51-193">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="dac51-193">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="dac51-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dac51-194">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="dac51-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dac51-195">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="dac51-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dac51-196">Search-Flags</span></span>           | <span data-ttu-id="dac51-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dac51-197">0x00000000</span></span>                                                 |
| <span data-ttu-id="dac51-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dac51-198">System-Flags</span></span>           | <span data-ttu-id="dac51-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dac51-199">0x00000010</span></span>                                                 |
| <span data-ttu-id="dac51-200">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="dac51-200">Classes used in</span></span>        | [<span data-ttu-id="dac51-201">**Display-specifier**</span><span class="sxs-lookup"><span data-stu-id="dac51-201">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="dac51-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dac51-202">Windows Server 2008</span></span>



| <span data-ttu-id="dac51-203">Entrée</span><span class="sxs-lookup"><span data-stu-id="dac51-203">Entry</span></span> | <span data-ttu-id="dac51-204">Valeur</span><span class="sxs-lookup"><span data-stu-id="dac51-204">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="dac51-205">ID de lien</span><span class="sxs-lookup"><span data-stu-id="dac51-205">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="dac51-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dac51-206">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="dac51-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="dac51-207">System-Only</span></span>            | <span data-ttu-id="dac51-208">Faux</span><span class="sxs-lookup"><span data-stu-id="dac51-208">False</span></span>                                                      |
| <span data-ttu-id="dac51-209">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="dac51-209">Is-Single-Valued</span></span>       | <span data-ttu-id="dac51-210">Faux</span><span class="sxs-lookup"><span data-stu-id="dac51-210">False</span></span>                                                      |
| <span data-ttu-id="dac51-211">Est indexé</span><span class="sxs-lookup"><span data-stu-id="dac51-211">Is Indexed</span></span>             | <span data-ttu-id="dac51-212">Faux</span><span class="sxs-lookup"><span data-stu-id="dac51-212">False</span></span>                                                      |
| <span data-ttu-id="dac51-213">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="dac51-213">In Global Catalog</span></span>      | <span data-ttu-id="dac51-214">Faux</span><span class="sxs-lookup"><span data-stu-id="dac51-214">False</span></span>                                                      |
| <span data-ttu-id="dac51-215">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="dac51-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="dac51-216">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="dac51-216">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="dac51-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dac51-217">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="dac51-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dac51-218">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="dac51-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dac51-219">Search-Flags</span></span>           | <span data-ttu-id="dac51-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dac51-220">0x00000000</span></span>                                                 |
| <span data-ttu-id="dac51-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dac51-221">System-Flags</span></span>           | <span data-ttu-id="dac51-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dac51-222">0x00000010</span></span>                                                 |
| <span data-ttu-id="dac51-223">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="dac51-223">Classes used in</span></span>        | [<span data-ttu-id="dac51-224">**Display-specifier**</span><span class="sxs-lookup"><span data-stu-id="dac51-224">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="dac51-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="dac51-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="dac51-226">Entrée</span><span class="sxs-lookup"><span data-stu-id="dac51-226">Entry</span></span> | <span data-ttu-id="dac51-227">Valeur</span><span class="sxs-lookup"><span data-stu-id="dac51-227">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="dac51-228">ID de lien</span><span class="sxs-lookup"><span data-stu-id="dac51-228">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="dac51-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dac51-229">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="dac51-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="dac51-230">System-Only</span></span>            | <span data-ttu-id="dac51-231">Faux</span><span class="sxs-lookup"><span data-stu-id="dac51-231">False</span></span>                                                      |
| <span data-ttu-id="dac51-232">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="dac51-232">Is-Single-Valued</span></span>       | <span data-ttu-id="dac51-233">Faux</span><span class="sxs-lookup"><span data-stu-id="dac51-233">False</span></span>                                                      |
| <span data-ttu-id="dac51-234">Est indexé</span><span class="sxs-lookup"><span data-stu-id="dac51-234">Is Indexed</span></span>             | <span data-ttu-id="dac51-235">Faux</span><span class="sxs-lookup"><span data-stu-id="dac51-235">False</span></span>                                                      |
| <span data-ttu-id="dac51-236">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="dac51-236">In Global Catalog</span></span>      | <span data-ttu-id="dac51-237">Faux</span><span class="sxs-lookup"><span data-stu-id="dac51-237">False</span></span>                                                      |
| <span data-ttu-id="dac51-238">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="dac51-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="dac51-239">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="dac51-239">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="dac51-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dac51-240">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="dac51-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dac51-241">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="dac51-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dac51-242">Search-Flags</span></span>           | <span data-ttu-id="dac51-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dac51-243">0x00000000</span></span>                                                 |
| <span data-ttu-id="dac51-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dac51-244">System-Flags</span></span>           | <span data-ttu-id="dac51-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dac51-245">0x00000010</span></span>                                                 |
| <span data-ttu-id="dac51-246">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="dac51-246">Classes used in</span></span>        | [<span data-ttu-id="dac51-247">**Display-specifier**</span><span class="sxs-lookup"><span data-stu-id="dac51-247">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="dac51-248">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="dac51-248">Windows Server 2012</span></span>



| <span data-ttu-id="dac51-249">Entrée</span><span class="sxs-lookup"><span data-stu-id="dac51-249">Entry</span></span> | <span data-ttu-id="dac51-250">Valeur</span><span class="sxs-lookup"><span data-stu-id="dac51-250">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="dac51-251">ID de lien</span><span class="sxs-lookup"><span data-stu-id="dac51-251">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="dac51-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dac51-252">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="dac51-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="dac51-253">System-Only</span></span>            | <span data-ttu-id="dac51-254">Faux</span><span class="sxs-lookup"><span data-stu-id="dac51-254">False</span></span>                                                      |
| <span data-ttu-id="dac51-255">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="dac51-255">Is-Single-Valued</span></span>       | <span data-ttu-id="dac51-256">Faux</span><span class="sxs-lookup"><span data-stu-id="dac51-256">False</span></span>                                                      |
| <span data-ttu-id="dac51-257">Est indexé</span><span class="sxs-lookup"><span data-stu-id="dac51-257">Is Indexed</span></span>             | <span data-ttu-id="dac51-258">Faux</span><span class="sxs-lookup"><span data-stu-id="dac51-258">False</span></span>                                                      |
| <span data-ttu-id="dac51-259">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="dac51-259">In Global Catalog</span></span>      | <span data-ttu-id="dac51-260">Faux</span><span class="sxs-lookup"><span data-stu-id="dac51-260">False</span></span>                                                      |
| <span data-ttu-id="dac51-261">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="dac51-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="dac51-262">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="dac51-262">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="dac51-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dac51-263">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="dac51-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dac51-264">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="dac51-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dac51-265">Search-Flags</span></span>           | <span data-ttu-id="dac51-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dac51-266">0x00000000</span></span>                                                 |
| <span data-ttu-id="dac51-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dac51-267">System-Flags</span></span>           | <span data-ttu-id="dac51-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dac51-268">0x00000010</span></span>                                                 |
| <span data-ttu-id="dac51-269">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="dac51-269">Classes used in</span></span>        | [<span data-ttu-id="dac51-270">**Display-specifier**</span><span class="sxs-lookup"><span data-stu-id="dac51-270">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



 

 





