---
title: Attribut UPN-Suffixes
description: Liste des suffixes de nom d’utilisateur principal d’un domaine.
ms.assetid: ad861d2d-b643-468c-a346-36ad6a828359
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut UPN-Suffixes
- Schéma AD de l’attribut uPNSuffixes
topic_type:
- apiref
api_name:
- UPN-Suffixes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4aa5fb9398478e4b91fb8f36b8cf96a244935fd
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845270"
---
# <a name="upn-suffixes-attribute"></a><span data-ttu-id="376ce-105">Attribut UPN-Suffixes</span><span class="sxs-lookup"><span data-stu-id="376ce-105">UPN-Suffixes attribute</span></span>

<span data-ttu-id="376ce-106">Liste des suffixes de nom d’utilisateur principal d’un domaine.</span><span class="sxs-lookup"><span data-stu-id="376ce-106">The list of User-Principal-Name suffixes for a domain.</span></span>



| <span data-ttu-id="376ce-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="376ce-107">Entry</span></span> | <span data-ttu-id="376ce-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="376ce-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="376ce-109">CN</span><span class="sxs-lookup"><span data-stu-id="376ce-109">CN</span></span>                | <span data-ttu-id="376ce-110">UPN-Suffixes</span><span class="sxs-lookup"><span data-stu-id="376ce-110">UPN-Suffixes</span></span>                                |
| <span data-ttu-id="376ce-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="376ce-111">Ldap-Display-Name</span></span> | <span data-ttu-id="376ce-112">uPNSuffixes</span><span class="sxs-lookup"><span data-stu-id="376ce-112">uPNSuffixes</span></span>                                 |
| <span data-ttu-id="376ce-113">Taille</span><span class="sxs-lookup"><span data-stu-id="376ce-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="376ce-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="376ce-114">Update Privilege</span></span>  | <span data-ttu-id="376ce-115">Administrateur de domaine</span><span class="sxs-lookup"><span data-stu-id="376ce-115">Domain Administrator</span></span>                        |
| <span data-ttu-id="376ce-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="376ce-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="376ce-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="376ce-117">Attribute-Id</span></span>      | <span data-ttu-id="376ce-118">1.2.840.113556.1.4.890</span><span class="sxs-lookup"><span data-stu-id="376ce-118">1.2.840.113556.1.4.890</span></span>                      |
| <span data-ttu-id="376ce-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="376ce-119">System-Id-Guid</span></span>    | <span data-ttu-id="376ce-120">032160bf-9824-11d1-aec0-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="376ce-120">032160bf-9824-11d1-aec0-0000f80367c1</span></span>        |
| <span data-ttu-id="376ce-121">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="376ce-121">Syntax</span></span>            | [<span data-ttu-id="376ce-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="376ce-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="376ce-123">Implémentations</span><span class="sxs-lookup"><span data-stu-id="376ce-123">Implementations</span></span>

-   [<span data-ttu-id="376ce-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="376ce-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="376ce-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="376ce-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="376ce-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="376ce-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="376ce-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="376ce-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="376ce-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="376ce-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="376ce-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="376ce-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="376ce-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="376ce-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="376ce-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="376ce-131">Windows 2000 Server</span></span>



| <span data-ttu-id="376ce-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="376ce-132">Entry</span></span> | <span data-ttu-id="376ce-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="376ce-133">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="376ce-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="376ce-134">Link-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="376ce-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="376ce-135">MAPI-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="376ce-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="376ce-136">System-Only</span></span>            | <span data-ttu-id="376ce-137">Faux</span><span class="sxs-lookup"><span data-stu-id="376ce-137">False</span></span>                                                                                                                        |
| <span data-ttu-id="376ce-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="376ce-138">Is-Single-Valued</span></span>       | <span data-ttu-id="376ce-139">Faux</span><span class="sxs-lookup"><span data-stu-id="376ce-139">False</span></span>                                                                                                                        |
| <span data-ttu-id="376ce-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="376ce-140">Is Indexed</span></span>             | <span data-ttu-id="376ce-141">Faux</span><span class="sxs-lookup"><span data-stu-id="376ce-141">False</span></span>                                                                                                                        |
| <span data-ttu-id="376ce-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="376ce-142">In Global Catalog</span></span>      | <span data-ttu-id="376ce-143">Faux</span><span class="sxs-lookup"><span data-stu-id="376ce-143">False</span></span>                                                                                                                        |
| <span data-ttu-id="376ce-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="376ce-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="376ce-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="376ce-145">O:BAG:BAD:S:</span></span>                                                                                                                 |
| <span data-ttu-id="376ce-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="376ce-146">Range-Lower</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="376ce-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="376ce-147">Range-Upper</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="376ce-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="376ce-148">Search-Flags</span></span>           | <span data-ttu-id="376ce-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="376ce-149">0x00000000</span></span>                                                                                                                   |
| <span data-ttu-id="376ce-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="376ce-150">System-Flags</span></span>           | <span data-ttu-id="376ce-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="376ce-151">0x00000010</span></span>                                                                                                                   |
| <span data-ttu-id="376ce-152">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="376ce-152">Classes used in</span></span>        | [<span data-ttu-id="376ce-153">**Cross-Ref-Container**</span><span class="sxs-lookup"><span data-stu-id="376ce-153">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> [<span data-ttu-id="376ce-154">**Unité d’organisation**</span><span class="sxs-lookup"><span data-stu-id="376ce-154">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="376ce-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="376ce-155">Windows Server 2003</span></span>



| <span data-ttu-id="376ce-156">Entrée</span><span class="sxs-lookup"><span data-stu-id="376ce-156">Entry</span></span> | <span data-ttu-id="376ce-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="376ce-157">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="376ce-158">ID de lien</span><span class="sxs-lookup"><span data-stu-id="376ce-158">Link-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="376ce-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="376ce-159">MAPI-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="376ce-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="376ce-160">System-Only</span></span>            | <span data-ttu-id="376ce-161">Faux</span><span class="sxs-lookup"><span data-stu-id="376ce-161">False</span></span>                                                                                                                        |
| <span data-ttu-id="376ce-162">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="376ce-162">Is-Single-Valued</span></span>       | <span data-ttu-id="376ce-163">Faux</span><span class="sxs-lookup"><span data-stu-id="376ce-163">False</span></span>                                                                                                                        |
| <span data-ttu-id="376ce-164">Est indexé</span><span class="sxs-lookup"><span data-stu-id="376ce-164">Is Indexed</span></span>             | <span data-ttu-id="376ce-165">Faux</span><span class="sxs-lookup"><span data-stu-id="376ce-165">False</span></span>                                                                                                                        |
| <span data-ttu-id="376ce-166">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="376ce-166">In Global Catalog</span></span>      | <span data-ttu-id="376ce-167">Faux</span><span class="sxs-lookup"><span data-stu-id="376ce-167">False</span></span>                                                                                                                        |
| <span data-ttu-id="376ce-168">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="376ce-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="376ce-169">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="376ce-169">O:BAG:BAD:S:</span></span>                                                                                                                 |
| <span data-ttu-id="376ce-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="376ce-170">Range-Lower</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="376ce-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="376ce-171">Range-Upper</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="376ce-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="376ce-172">Search-Flags</span></span>           | <span data-ttu-id="376ce-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="376ce-173">0x00000000</span></span>                                                                                                                   |
| <span data-ttu-id="376ce-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="376ce-174">System-Flags</span></span>           | <span data-ttu-id="376ce-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="376ce-175">0x00000010</span></span>                                                                                                                   |
| <span data-ttu-id="376ce-176">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="376ce-176">Classes used in</span></span>        | [<span data-ttu-id="376ce-177">**Cross-Ref-Container**</span><span class="sxs-lookup"><span data-stu-id="376ce-177">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> [<span data-ttu-id="376ce-178">**Unité d’organisation**</span><span class="sxs-lookup"><span data-stu-id="376ce-178">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="adam"></a><span data-ttu-id="376ce-179">ADAM</span><span class="sxs-lookup"><span data-stu-id="376ce-179">ADAM</span></span>



| <span data-ttu-id="376ce-180">Entrée</span><span class="sxs-lookup"><span data-stu-id="376ce-180">Entry</span></span> | <span data-ttu-id="376ce-181">Valeur</span><span class="sxs-lookup"><span data-stu-id="376ce-181">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="376ce-182">ID de lien</span><span class="sxs-lookup"><span data-stu-id="376ce-182">Link-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="376ce-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="376ce-183">MAPI-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="376ce-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="376ce-184">System-Only</span></span>            | <span data-ttu-id="376ce-185">Faux</span><span class="sxs-lookup"><span data-stu-id="376ce-185">False</span></span>                                                                                                                        |
| <span data-ttu-id="376ce-186">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="376ce-186">Is-Single-Valued</span></span>       | <span data-ttu-id="376ce-187">Faux</span><span class="sxs-lookup"><span data-stu-id="376ce-187">False</span></span>                                                                                                                        |
| <span data-ttu-id="376ce-188">Est indexé</span><span class="sxs-lookup"><span data-stu-id="376ce-188">Is Indexed</span></span>             | <span data-ttu-id="376ce-189">Faux</span><span class="sxs-lookup"><span data-stu-id="376ce-189">False</span></span>                                                                                                                        |
| <span data-ttu-id="376ce-190">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="376ce-190">In Global Catalog</span></span>      | <span data-ttu-id="376ce-191">Faux</span><span class="sxs-lookup"><span data-stu-id="376ce-191">False</span></span>                                                                                                                        |
| <span data-ttu-id="376ce-192">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="376ce-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="376ce-193">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="376ce-193">O:BAG:BAD:S:</span></span>                                                                                                                 |
| <span data-ttu-id="376ce-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="376ce-194">Range-Lower</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="376ce-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="376ce-195">Range-Upper</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="376ce-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="376ce-196">Search-Flags</span></span>           | <span data-ttu-id="376ce-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="376ce-197">0x00000000</span></span>                                                                                                                   |
| <span data-ttu-id="376ce-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="376ce-198">System-Flags</span></span>           | <span data-ttu-id="376ce-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="376ce-199">0x00000010</span></span>                                                                                                                   |
| <span data-ttu-id="376ce-200">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="376ce-200">Classes used in</span></span>        | [<span data-ttu-id="376ce-201">**Cross-Ref-Container**</span><span class="sxs-lookup"><span data-stu-id="376ce-201">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> [<span data-ttu-id="376ce-202">**Unité d’organisation**</span><span class="sxs-lookup"><span data-stu-id="376ce-202">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="376ce-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="376ce-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="376ce-204">Entrée</span><span class="sxs-lookup"><span data-stu-id="376ce-204">Entry</span></span> | <span data-ttu-id="376ce-205">Valeur</span><span class="sxs-lookup"><span data-stu-id="376ce-205">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="376ce-206">ID de lien</span><span class="sxs-lookup"><span data-stu-id="376ce-206">Link-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="376ce-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="376ce-207">MAPI-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="376ce-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="376ce-208">System-Only</span></span>            | <span data-ttu-id="376ce-209">Faux</span><span class="sxs-lookup"><span data-stu-id="376ce-209">False</span></span>                                                                                                                        |
| <span data-ttu-id="376ce-210">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="376ce-210">Is-Single-Valued</span></span>       | <span data-ttu-id="376ce-211">Faux</span><span class="sxs-lookup"><span data-stu-id="376ce-211">False</span></span>                                                                                                                        |
| <span data-ttu-id="376ce-212">Est indexé</span><span class="sxs-lookup"><span data-stu-id="376ce-212">Is Indexed</span></span>             | <span data-ttu-id="376ce-213">Faux</span><span class="sxs-lookup"><span data-stu-id="376ce-213">False</span></span>                                                                                                                        |
| <span data-ttu-id="376ce-214">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="376ce-214">In Global Catalog</span></span>      | <span data-ttu-id="376ce-215">Faux</span><span class="sxs-lookup"><span data-stu-id="376ce-215">False</span></span>                                                                                                                        |
| <span data-ttu-id="376ce-216">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="376ce-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="376ce-217">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="376ce-217">O:BAG:BAD:S:</span></span>                                                                                                                 |
| <span data-ttu-id="376ce-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="376ce-218">Range-Lower</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="376ce-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="376ce-219">Range-Upper</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="376ce-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="376ce-220">Search-Flags</span></span>           | <span data-ttu-id="376ce-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="376ce-221">0x00000000</span></span>                                                                                                                   |
| <span data-ttu-id="376ce-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="376ce-222">System-Flags</span></span>           | <span data-ttu-id="376ce-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="376ce-223">0x00000010</span></span>                                                                                                                   |
| <span data-ttu-id="376ce-224">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="376ce-224">Classes used in</span></span>        | [<span data-ttu-id="376ce-225">**Cross-Ref-Container**</span><span class="sxs-lookup"><span data-stu-id="376ce-225">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> [<span data-ttu-id="376ce-226">**Unité d’organisation**</span><span class="sxs-lookup"><span data-stu-id="376ce-226">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="376ce-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="376ce-227">Windows Server 2008</span></span>



| <span data-ttu-id="376ce-228">Entrée</span><span class="sxs-lookup"><span data-stu-id="376ce-228">Entry</span></span> | <span data-ttu-id="376ce-229">Valeur</span><span class="sxs-lookup"><span data-stu-id="376ce-229">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="376ce-230">ID de lien</span><span class="sxs-lookup"><span data-stu-id="376ce-230">Link-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="376ce-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="376ce-231">MAPI-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="376ce-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="376ce-232">System-Only</span></span>            | <span data-ttu-id="376ce-233">Faux</span><span class="sxs-lookup"><span data-stu-id="376ce-233">False</span></span>                                                                                                                        |
| <span data-ttu-id="376ce-234">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="376ce-234">Is-Single-Valued</span></span>       | <span data-ttu-id="376ce-235">Faux</span><span class="sxs-lookup"><span data-stu-id="376ce-235">False</span></span>                                                                                                                        |
| <span data-ttu-id="376ce-236">Est indexé</span><span class="sxs-lookup"><span data-stu-id="376ce-236">Is Indexed</span></span>             | <span data-ttu-id="376ce-237">Faux</span><span class="sxs-lookup"><span data-stu-id="376ce-237">False</span></span>                                                                                                                        |
| <span data-ttu-id="376ce-238">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="376ce-238">In Global Catalog</span></span>      | <span data-ttu-id="376ce-239">Faux</span><span class="sxs-lookup"><span data-stu-id="376ce-239">False</span></span>                                                                                                                        |
| <span data-ttu-id="376ce-240">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="376ce-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="376ce-241">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="376ce-241">O:BAG:BAD:S:</span></span>                                                                                                                 |
| <span data-ttu-id="376ce-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="376ce-242">Range-Lower</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="376ce-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="376ce-243">Range-Upper</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="376ce-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="376ce-244">Search-Flags</span></span>           | <span data-ttu-id="376ce-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="376ce-245">0x00000000</span></span>                                                                                                                   |
| <span data-ttu-id="376ce-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="376ce-246">System-Flags</span></span>           | <span data-ttu-id="376ce-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="376ce-247">0x00000010</span></span>                                                                                                                   |
| <span data-ttu-id="376ce-248">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="376ce-248">Classes used in</span></span>        | [<span data-ttu-id="376ce-249">**Cross-Ref-Container**</span><span class="sxs-lookup"><span data-stu-id="376ce-249">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> [<span data-ttu-id="376ce-250">**Unité d’organisation**</span><span class="sxs-lookup"><span data-stu-id="376ce-250">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="376ce-251">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="376ce-251">Windows Server 2008 R2</span></span>



| <span data-ttu-id="376ce-252">Entrée</span><span class="sxs-lookup"><span data-stu-id="376ce-252">Entry</span></span> | <span data-ttu-id="376ce-253">Valeur</span><span class="sxs-lookup"><span data-stu-id="376ce-253">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="376ce-254">ID de lien</span><span class="sxs-lookup"><span data-stu-id="376ce-254">Link-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="376ce-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="376ce-255">MAPI-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="376ce-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="376ce-256">System-Only</span></span>            | <span data-ttu-id="376ce-257">Faux</span><span class="sxs-lookup"><span data-stu-id="376ce-257">False</span></span>                                                                                                                        |
| <span data-ttu-id="376ce-258">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="376ce-258">Is-Single-Valued</span></span>       | <span data-ttu-id="376ce-259">Faux</span><span class="sxs-lookup"><span data-stu-id="376ce-259">False</span></span>                                                                                                                        |
| <span data-ttu-id="376ce-260">Est indexé</span><span class="sxs-lookup"><span data-stu-id="376ce-260">Is Indexed</span></span>             | <span data-ttu-id="376ce-261">Faux</span><span class="sxs-lookup"><span data-stu-id="376ce-261">False</span></span>                                                                                                                        |
| <span data-ttu-id="376ce-262">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="376ce-262">In Global Catalog</span></span>      | <span data-ttu-id="376ce-263">Faux</span><span class="sxs-lookup"><span data-stu-id="376ce-263">False</span></span>                                                                                                                        |
| <span data-ttu-id="376ce-264">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="376ce-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="376ce-265">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="376ce-265">O:BAG:BAD:S:</span></span>                                                                                                                 |
| <span data-ttu-id="376ce-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="376ce-266">Range-Lower</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="376ce-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="376ce-267">Range-Upper</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="376ce-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="376ce-268">Search-Flags</span></span>           | <span data-ttu-id="376ce-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="376ce-269">0x00000000</span></span>                                                                                                                   |
| <span data-ttu-id="376ce-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="376ce-270">System-Flags</span></span>           | <span data-ttu-id="376ce-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="376ce-271">0x00000010</span></span>                                                                                                                   |
| <span data-ttu-id="376ce-272">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="376ce-272">Classes used in</span></span>        | [<span data-ttu-id="376ce-273">**Cross-Ref-Container**</span><span class="sxs-lookup"><span data-stu-id="376ce-273">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> [<span data-ttu-id="376ce-274">**Unité d’organisation**</span><span class="sxs-lookup"><span data-stu-id="376ce-274">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="376ce-275">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="376ce-275">Windows Server 2012</span></span>



| <span data-ttu-id="376ce-276">Entrée</span><span class="sxs-lookup"><span data-stu-id="376ce-276">Entry</span></span> | <span data-ttu-id="376ce-277">Valeur</span><span class="sxs-lookup"><span data-stu-id="376ce-277">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="376ce-278">ID de lien</span><span class="sxs-lookup"><span data-stu-id="376ce-278">Link-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="376ce-279">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="376ce-279">MAPI-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="376ce-280">System-Only</span><span class="sxs-lookup"><span data-stu-id="376ce-280">System-Only</span></span>            | <span data-ttu-id="376ce-281">Faux</span><span class="sxs-lookup"><span data-stu-id="376ce-281">False</span></span>                                                                                                                        |
| <span data-ttu-id="376ce-282">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="376ce-282">Is-Single-Valued</span></span>       | <span data-ttu-id="376ce-283">Faux</span><span class="sxs-lookup"><span data-stu-id="376ce-283">False</span></span>                                                                                                                        |
| <span data-ttu-id="376ce-284">Est indexé</span><span class="sxs-lookup"><span data-stu-id="376ce-284">Is Indexed</span></span>             | <span data-ttu-id="376ce-285">Faux</span><span class="sxs-lookup"><span data-stu-id="376ce-285">False</span></span>                                                                                                                        |
| <span data-ttu-id="376ce-286">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="376ce-286">In Global Catalog</span></span>      | <span data-ttu-id="376ce-287">Faux</span><span class="sxs-lookup"><span data-stu-id="376ce-287">False</span></span>                                                                                                                        |
| <span data-ttu-id="376ce-288">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="376ce-288">NT-Security-Descriptor</span></span> | <span data-ttu-id="376ce-289">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="376ce-289">O:BAG:BAD:S:</span></span>                                                                                                                 |
| <span data-ttu-id="376ce-290">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="376ce-290">Range-Lower</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="376ce-291">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="376ce-291">Range-Upper</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="376ce-292">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="376ce-292">Search-Flags</span></span>           | <span data-ttu-id="376ce-293">0x00000000</span><span class="sxs-lookup"><span data-stu-id="376ce-293">0x00000000</span></span>                                                                                                                   |
| <span data-ttu-id="376ce-294">System-Flags</span><span class="sxs-lookup"><span data-stu-id="376ce-294">System-Flags</span></span>           | <span data-ttu-id="376ce-295">0x00000010</span><span class="sxs-lookup"><span data-stu-id="376ce-295">0x00000010</span></span>                                                                                                                   |
| <span data-ttu-id="376ce-296">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="376ce-296">Classes used in</span></span>        | [<span data-ttu-id="376ce-297">**Cross-Ref-Container**</span><span class="sxs-lookup"><span data-stu-id="376ce-297">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> [<span data-ttu-id="376ce-298">**Unité d’organisation**</span><span class="sxs-lookup"><span data-stu-id="376ce-298">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



 

 





