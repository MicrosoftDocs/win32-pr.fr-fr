---
title: Attribut Country-Code
description: Spécifie le code de pays/région pour la langue choisie par l’utilisateur. Cette valeur n’est pas utilisée par Windows 2000.
ms.assetid: 7011cb76-aa86-4203-bcc4-0136bb11c403
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Country-Code
- Schéma AD de l’attribut countryCode
topic_type:
- apiref
api_name:
- Country-Code
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9523a5aab21e81c2b0a5479def8ed8923751daed
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106543639"
---
# <a name="country-code-attribute"></a><span data-ttu-id="e1b9a-106">Attribut Country-Code</span><span class="sxs-lookup"><span data-stu-id="e1b9a-106">Country-Code attribute</span></span>

<span data-ttu-id="e1b9a-107">Spécifie le code de pays/région pour la langue choisie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e1b9a-107">Specifies the country/region code for the user's language of choice.</span></span> <span data-ttu-id="e1b9a-108">Cette valeur n’est pas utilisée par Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="e1b9a-108">This value is not used by Windows 2000.</span></span>



| <span data-ttu-id="e1b9a-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="e1b9a-109">Entry</span></span> | <span data-ttu-id="e1b9a-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1b9a-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="e1b9a-111">CN</span><span class="sxs-lookup"><span data-stu-id="e1b9a-111">CN</span></span>                | <span data-ttu-id="e1b9a-112">Country-Code</span><span class="sxs-lookup"><span data-stu-id="e1b9a-112">Country-Code</span></span>                            |
| <span data-ttu-id="e1b9a-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="e1b9a-113">Ldap-Display-Name</span></span> | <span data-ttu-id="e1b9a-114">countryCode</span><span class="sxs-lookup"><span data-stu-id="e1b9a-114">countryCode</span></span>                             |
| <span data-ttu-id="e1b9a-115">Taille</span><span class="sxs-lookup"><span data-stu-id="e1b9a-115">Size</span></span>              | <span data-ttu-id="e1b9a-116">2 octets</span><span class="sxs-lookup"><span data-stu-id="e1b9a-116">2 bytes</span></span>                                 |
| <span data-ttu-id="e1b9a-117">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="e1b9a-117">Update Privilege</span></span>  | <span data-ttu-id="e1b9a-118">Propriétaire du compte ou administrateur de domaine</span><span class="sxs-lookup"><span data-stu-id="e1b9a-118">Account owner or domain administrator</span></span>   |
| <span data-ttu-id="e1b9a-119">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="e1b9a-119">Update Frequency</span></span>  | <span data-ttu-id="e1b9a-120">Lorsque le pays ou la région de l’utilisateur change.</span><span class="sxs-lookup"><span data-stu-id="e1b9a-120">When the user's country/region changes.</span></span> |
| <span data-ttu-id="e1b9a-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e1b9a-121">Attribute-Id</span></span>      | <span data-ttu-id="e1b9a-122">1.2.840.113556.1.4.25</span><span class="sxs-lookup"><span data-stu-id="e1b9a-122">1.2.840.113556.1.4.25</span></span>                   |
| <span data-ttu-id="e1b9a-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="e1b9a-123">System-Id-Guid</span></span>    | <span data-ttu-id="e1b9a-124">5fd42471-1262-11d0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="e1b9a-124">5fd42471-1262-11d0-a060-00aa006c33ed</span></span>    |
| <span data-ttu-id="e1b9a-125">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e1b9a-125">Syntax</span></span>            | [<span data-ttu-id="e1b9a-126">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="e1b9a-126">**Enumeration**</span></span>](s-enumeration.md)    |



## <a name="implementations"></a><span data-ttu-id="e1b9a-127">Implémentations</span><span class="sxs-lookup"><span data-stu-id="e1b9a-127">Implementations</span></span>

-   [<span data-ttu-id="e1b9a-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e1b9a-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e1b9a-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e1b9a-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e1b9a-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="e1b9a-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="e1b9a-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e1b9a-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e1b9a-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e1b9a-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e1b9a-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e1b9a-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e1b9a-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e1b9a-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e1b9a-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e1b9a-135">Windows 2000 Server</span></span>



| <span data-ttu-id="e1b9a-136">Entrée</span><span class="sxs-lookup"><span data-stu-id="e1b9a-136">Entry</span></span> | <span data-ttu-id="e1b9a-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1b9a-137">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1b9a-138">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e1b9a-138">Link-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="e1b9a-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e1b9a-139">MAPI-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="e1b9a-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="e1b9a-140">System-Only</span></span>            | <span data-ttu-id="e1b9a-141">Faux</span><span class="sxs-lookup"><span data-stu-id="e1b9a-141">False</span></span>                                                                                                                             |
| <span data-ttu-id="e1b9a-142">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e1b9a-142">Is-Single-Valued</span></span>       | <span data-ttu-id="e1b9a-143">Vrai</span><span class="sxs-lookup"><span data-stu-id="e1b9a-143">True</span></span>                                                                                                                              |
| <span data-ttu-id="e1b9a-144">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e1b9a-144">Is Indexed</span></span>             | <span data-ttu-id="e1b9a-145">Faux</span><span class="sxs-lookup"><span data-stu-id="e1b9a-145">False</span></span>                                                                                                                             |
| <span data-ttu-id="e1b9a-146">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e1b9a-146">In Global Catalog</span></span>      | <span data-ttu-id="e1b9a-147">Faux</span><span class="sxs-lookup"><span data-stu-id="e1b9a-147">False</span></span>                                                                                                                             |
| <span data-ttu-id="e1b9a-148">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e1b9a-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="e1b9a-149">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e1b9a-149">O:BAG:BAD:S:</span></span>                                                                                                                      |
| <span data-ttu-id="e1b9a-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e1b9a-150">Range-Lower</span></span>            | \-                                                                                                                                |
| <span data-ttu-id="e1b9a-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e1b9a-151">Range-Upper</span></span>            | \-                                                                                                                                |
| <span data-ttu-id="e1b9a-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e1b9a-152">Search-Flags</span></span>           | <span data-ttu-id="e1b9a-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e1b9a-153">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="e1b9a-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e1b9a-154">System-Flags</span></span>           | <span data-ttu-id="e1b9a-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e1b9a-155">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="e1b9a-156">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e1b9a-156">Classes used in</span></span>        | [<span data-ttu-id="e1b9a-157">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="e1b9a-157">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> [<span data-ttu-id="e1b9a-158">**Unité d’organisation**</span><span class="sxs-lookup"><span data-stu-id="e1b9a-158">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e1b9a-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e1b9a-159">Windows Server 2003</span></span>



| <span data-ttu-id="e1b9a-160">Entrée</span><span class="sxs-lookup"><span data-stu-id="e1b9a-160">Entry</span></span> | <span data-ttu-id="e1b9a-161">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1b9a-161">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1b9a-162">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e1b9a-162">Link-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="e1b9a-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e1b9a-163">MAPI-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="e1b9a-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="e1b9a-164">System-Only</span></span>            | <span data-ttu-id="e1b9a-165">Faux</span><span class="sxs-lookup"><span data-stu-id="e1b9a-165">False</span></span>                                                                                                                             |
| <span data-ttu-id="e1b9a-166">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e1b9a-166">Is-Single-Valued</span></span>       | <span data-ttu-id="e1b9a-167">Vrai</span><span class="sxs-lookup"><span data-stu-id="e1b9a-167">True</span></span>                                                                                                                              |
| <span data-ttu-id="e1b9a-168">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e1b9a-168">Is Indexed</span></span>             | <span data-ttu-id="e1b9a-169">Faux</span><span class="sxs-lookup"><span data-stu-id="e1b9a-169">False</span></span>                                                                                                                             |
| <span data-ttu-id="e1b9a-170">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e1b9a-170">In Global Catalog</span></span>      | <span data-ttu-id="e1b9a-171">Faux</span><span class="sxs-lookup"><span data-stu-id="e1b9a-171">False</span></span>                                                                                                                             |
| <span data-ttu-id="e1b9a-172">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e1b9a-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="e1b9a-173">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e1b9a-173">O:BAG:BAD:S:</span></span>                                                                                                                      |
| <span data-ttu-id="e1b9a-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e1b9a-174">Range-Lower</span></span>            | <span data-ttu-id="e1b9a-175">0</span><span class="sxs-lookup"><span data-stu-id="e1b9a-175">0</span></span>                                                                                                                                 |
| <span data-ttu-id="e1b9a-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e1b9a-176">Range-Upper</span></span>            | <span data-ttu-id="e1b9a-177">65535</span><span class="sxs-lookup"><span data-stu-id="e1b9a-177">65535</span></span>                                                                                                                             |
| <span data-ttu-id="e1b9a-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e1b9a-178">Search-Flags</span></span>           | <span data-ttu-id="e1b9a-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e1b9a-179">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="e1b9a-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e1b9a-180">System-Flags</span></span>           | <span data-ttu-id="e1b9a-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e1b9a-181">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="e1b9a-182">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e1b9a-182">Classes used in</span></span>        | [<span data-ttu-id="e1b9a-183">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="e1b9a-183">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> [<span data-ttu-id="e1b9a-184">**Unité d’organisation**</span><span class="sxs-lookup"><span data-stu-id="e1b9a-184">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="adam"></a><span data-ttu-id="e1b9a-185">ADAM</span><span class="sxs-lookup"><span data-stu-id="e1b9a-185">ADAM</span></span>



| <span data-ttu-id="e1b9a-186">Entrée</span><span class="sxs-lookup"><span data-stu-id="e1b9a-186">Entry</span></span> | <span data-ttu-id="e1b9a-187">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1b9a-187">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="e1b9a-188">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e1b9a-188">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="e1b9a-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e1b9a-189">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="e1b9a-190">System-Only</span><span class="sxs-lookup"><span data-stu-id="e1b9a-190">System-Only</span></span>            | <span data-ttu-id="e1b9a-191">Faux</span><span class="sxs-lookup"><span data-stu-id="e1b9a-191">False</span></span>                                                          |
| <span data-ttu-id="e1b9a-192">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e1b9a-192">Is-Single-Valued</span></span>       | <span data-ttu-id="e1b9a-193">Vrai</span><span class="sxs-lookup"><span data-stu-id="e1b9a-193">True</span></span>                                                           |
| <span data-ttu-id="e1b9a-194">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e1b9a-194">Is Indexed</span></span>             | <span data-ttu-id="e1b9a-195">Faux</span><span class="sxs-lookup"><span data-stu-id="e1b9a-195">False</span></span>                                                          |
| <span data-ttu-id="e1b9a-196">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e1b9a-196">In Global Catalog</span></span>      | <span data-ttu-id="e1b9a-197">Faux</span><span class="sxs-lookup"><span data-stu-id="e1b9a-197">False</span></span>                                                          |
| <span data-ttu-id="e1b9a-198">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e1b9a-198">NT-Security-Descriptor</span></span> | <span data-ttu-id="e1b9a-199">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e1b9a-199">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="e1b9a-200">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e1b9a-200">Range-Lower</span></span>            | <span data-ttu-id="e1b9a-201">0</span><span class="sxs-lookup"><span data-stu-id="e1b9a-201">0</span></span>                                                              |
| <span data-ttu-id="e1b9a-202">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e1b9a-202">Range-Upper</span></span>            | <span data-ttu-id="e1b9a-203">65535</span><span class="sxs-lookup"><span data-stu-id="e1b9a-203">65535</span></span>                                                          |
| <span data-ttu-id="e1b9a-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e1b9a-204">Search-Flags</span></span>           | <span data-ttu-id="e1b9a-205">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e1b9a-205">0x00000010</span></span>                                                     |
| <span data-ttu-id="e1b9a-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e1b9a-206">System-Flags</span></span>           | <span data-ttu-id="e1b9a-207">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e1b9a-207">0x00000010</span></span>                                                     |
| <span data-ttu-id="e1b9a-208">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e1b9a-208">Classes used in</span></span>        | [<span data-ttu-id="e1b9a-209">**Unité d’organisation**</span><span class="sxs-lookup"><span data-stu-id="e1b9a-209">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e1b9a-210">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e1b9a-210">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e1b9a-211">Entrée</span><span class="sxs-lookup"><span data-stu-id="e1b9a-211">Entry</span></span> | <span data-ttu-id="e1b9a-212">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1b9a-212">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1b9a-213">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e1b9a-213">Link-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="e1b9a-214">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e1b9a-214">MAPI-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="e1b9a-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="e1b9a-215">System-Only</span></span>            | <span data-ttu-id="e1b9a-216">Faux</span><span class="sxs-lookup"><span data-stu-id="e1b9a-216">False</span></span>                                                                                                                             |
| <span data-ttu-id="e1b9a-217">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e1b9a-217">Is-Single-Valued</span></span>       | <span data-ttu-id="e1b9a-218">Vrai</span><span class="sxs-lookup"><span data-stu-id="e1b9a-218">True</span></span>                                                                                                                              |
| <span data-ttu-id="e1b9a-219">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e1b9a-219">Is Indexed</span></span>             | <span data-ttu-id="e1b9a-220">Faux</span><span class="sxs-lookup"><span data-stu-id="e1b9a-220">False</span></span>                                                                                                                             |
| <span data-ttu-id="e1b9a-221">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e1b9a-221">In Global Catalog</span></span>      | <span data-ttu-id="e1b9a-222">Faux</span><span class="sxs-lookup"><span data-stu-id="e1b9a-222">False</span></span>                                                                                                                             |
| <span data-ttu-id="e1b9a-223">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e1b9a-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="e1b9a-224">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e1b9a-224">O:BAG:BAD:S:</span></span>                                                                                                                      |
| <span data-ttu-id="e1b9a-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e1b9a-225">Range-Lower</span></span>            | <span data-ttu-id="e1b9a-226">0</span><span class="sxs-lookup"><span data-stu-id="e1b9a-226">0</span></span>                                                                                                                                 |
| <span data-ttu-id="e1b9a-227">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e1b9a-227">Range-Upper</span></span>            | <span data-ttu-id="e1b9a-228">65535</span><span class="sxs-lookup"><span data-stu-id="e1b9a-228">65535</span></span>                                                                                                                             |
| <span data-ttu-id="e1b9a-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e1b9a-229">Search-Flags</span></span>           | <span data-ttu-id="e1b9a-230">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e1b9a-230">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="e1b9a-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e1b9a-231">System-Flags</span></span>           | <span data-ttu-id="e1b9a-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e1b9a-232">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="e1b9a-233">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e1b9a-233">Classes used in</span></span>        | [<span data-ttu-id="e1b9a-234">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="e1b9a-234">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> [<span data-ttu-id="e1b9a-235">**Unité d’organisation**</span><span class="sxs-lookup"><span data-stu-id="e1b9a-235">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e1b9a-236">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e1b9a-236">Windows Server 2008</span></span>



| <span data-ttu-id="e1b9a-237">Entrée</span><span class="sxs-lookup"><span data-stu-id="e1b9a-237">Entry</span></span> | <span data-ttu-id="e1b9a-238">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1b9a-238">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1b9a-239">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e1b9a-239">Link-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="e1b9a-240">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e1b9a-240">MAPI-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="e1b9a-241">System-Only</span><span class="sxs-lookup"><span data-stu-id="e1b9a-241">System-Only</span></span>            | <span data-ttu-id="e1b9a-242">Faux</span><span class="sxs-lookup"><span data-stu-id="e1b9a-242">False</span></span>                                                                                                                             |
| <span data-ttu-id="e1b9a-243">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e1b9a-243">Is-Single-Valued</span></span>       | <span data-ttu-id="e1b9a-244">Vrai</span><span class="sxs-lookup"><span data-stu-id="e1b9a-244">True</span></span>                                                                                                                              |
| <span data-ttu-id="e1b9a-245">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e1b9a-245">Is Indexed</span></span>             | <span data-ttu-id="e1b9a-246">Faux</span><span class="sxs-lookup"><span data-stu-id="e1b9a-246">False</span></span>                                                                                                                             |
| <span data-ttu-id="e1b9a-247">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e1b9a-247">In Global Catalog</span></span>      | <span data-ttu-id="e1b9a-248">Faux</span><span class="sxs-lookup"><span data-stu-id="e1b9a-248">False</span></span>                                                                                                                             |
| <span data-ttu-id="e1b9a-249">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e1b9a-249">NT-Security-Descriptor</span></span> | <span data-ttu-id="e1b9a-250">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e1b9a-250">O:BAG:BAD:S:</span></span>                                                                                                                      |
| <span data-ttu-id="e1b9a-251">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e1b9a-251">Range-Lower</span></span>            | <span data-ttu-id="e1b9a-252">0</span><span class="sxs-lookup"><span data-stu-id="e1b9a-252">0</span></span>                                                                                                                                 |
| <span data-ttu-id="e1b9a-253">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e1b9a-253">Range-Upper</span></span>            | <span data-ttu-id="e1b9a-254">65535</span><span class="sxs-lookup"><span data-stu-id="e1b9a-254">65535</span></span>                                                                                                                             |
| <span data-ttu-id="e1b9a-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e1b9a-255">Search-Flags</span></span>           | <span data-ttu-id="e1b9a-256">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e1b9a-256">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="e1b9a-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e1b9a-257">System-Flags</span></span>           | <span data-ttu-id="e1b9a-258">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e1b9a-258">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="e1b9a-259">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e1b9a-259">Classes used in</span></span>        | [<span data-ttu-id="e1b9a-260">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="e1b9a-260">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> [<span data-ttu-id="e1b9a-261">**Unité d’organisation**</span><span class="sxs-lookup"><span data-stu-id="e1b9a-261">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e1b9a-262">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e1b9a-262">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e1b9a-263">Entrée</span><span class="sxs-lookup"><span data-stu-id="e1b9a-263">Entry</span></span> | <span data-ttu-id="e1b9a-264">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1b9a-264">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1b9a-265">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e1b9a-265">Link-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="e1b9a-266">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e1b9a-266">MAPI-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="e1b9a-267">System-Only</span><span class="sxs-lookup"><span data-stu-id="e1b9a-267">System-Only</span></span>            | <span data-ttu-id="e1b9a-268">Faux</span><span class="sxs-lookup"><span data-stu-id="e1b9a-268">False</span></span>                                                                                                                             |
| <span data-ttu-id="e1b9a-269">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e1b9a-269">Is-Single-Valued</span></span>       | <span data-ttu-id="e1b9a-270">Vrai</span><span class="sxs-lookup"><span data-stu-id="e1b9a-270">True</span></span>                                                                                                                              |
| <span data-ttu-id="e1b9a-271">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e1b9a-271">Is Indexed</span></span>             | <span data-ttu-id="e1b9a-272">Faux</span><span class="sxs-lookup"><span data-stu-id="e1b9a-272">False</span></span>                                                                                                                             |
| <span data-ttu-id="e1b9a-273">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e1b9a-273">In Global Catalog</span></span>      | <span data-ttu-id="e1b9a-274">Faux</span><span class="sxs-lookup"><span data-stu-id="e1b9a-274">False</span></span>                                                                                                                             |
| <span data-ttu-id="e1b9a-275">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e1b9a-275">NT-Security-Descriptor</span></span> | <span data-ttu-id="e1b9a-276">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e1b9a-276">O:BAG:BAD:S:</span></span>                                                                                                                      |
| <span data-ttu-id="e1b9a-277">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e1b9a-277">Range-Lower</span></span>            | <span data-ttu-id="e1b9a-278">0</span><span class="sxs-lookup"><span data-stu-id="e1b9a-278">0</span></span>                                                                                                                                 |
| <span data-ttu-id="e1b9a-279">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e1b9a-279">Range-Upper</span></span>            | <span data-ttu-id="e1b9a-280">65535</span><span class="sxs-lookup"><span data-stu-id="e1b9a-280">65535</span></span>                                                                                                                             |
| <span data-ttu-id="e1b9a-281">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e1b9a-281">Search-Flags</span></span>           | <span data-ttu-id="e1b9a-282">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e1b9a-282">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="e1b9a-283">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e1b9a-283">System-Flags</span></span>           | <span data-ttu-id="e1b9a-284">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e1b9a-284">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="e1b9a-285">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e1b9a-285">Classes used in</span></span>        | [<span data-ttu-id="e1b9a-286">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="e1b9a-286">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> [<span data-ttu-id="e1b9a-287">**Unité d’organisation**</span><span class="sxs-lookup"><span data-stu-id="e1b9a-287">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e1b9a-288">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e1b9a-288">Windows Server 2012</span></span>



| <span data-ttu-id="e1b9a-289">Entrée</span><span class="sxs-lookup"><span data-stu-id="e1b9a-289">Entry</span></span> | <span data-ttu-id="e1b9a-290">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1b9a-290">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1b9a-291">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e1b9a-291">Link-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="e1b9a-292">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e1b9a-292">MAPI-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="e1b9a-293">System-Only</span><span class="sxs-lookup"><span data-stu-id="e1b9a-293">System-Only</span></span>            | <span data-ttu-id="e1b9a-294">Faux</span><span class="sxs-lookup"><span data-stu-id="e1b9a-294">False</span></span>                                                                                                                             |
| <span data-ttu-id="e1b9a-295">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e1b9a-295">Is-Single-Valued</span></span>       | <span data-ttu-id="e1b9a-296">Vrai</span><span class="sxs-lookup"><span data-stu-id="e1b9a-296">True</span></span>                                                                                                                              |
| <span data-ttu-id="e1b9a-297">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e1b9a-297">Is Indexed</span></span>             | <span data-ttu-id="e1b9a-298">Faux</span><span class="sxs-lookup"><span data-stu-id="e1b9a-298">False</span></span>                                                                                                                             |
| <span data-ttu-id="e1b9a-299">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e1b9a-299">In Global Catalog</span></span>      | <span data-ttu-id="e1b9a-300">Faux</span><span class="sxs-lookup"><span data-stu-id="e1b9a-300">False</span></span>                                                                                                                             |
| <span data-ttu-id="e1b9a-301">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e1b9a-301">NT-Security-Descriptor</span></span> | <span data-ttu-id="e1b9a-302">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e1b9a-302">O:BAG:BAD:S:</span></span>                                                                                                                      |
| <span data-ttu-id="e1b9a-303">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e1b9a-303">Range-Lower</span></span>            | <span data-ttu-id="e1b9a-304">0</span><span class="sxs-lookup"><span data-stu-id="e1b9a-304">0</span></span>                                                                                                                                 |
| <span data-ttu-id="e1b9a-305">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e1b9a-305">Range-Upper</span></span>            | <span data-ttu-id="e1b9a-306">65535</span><span class="sxs-lookup"><span data-stu-id="e1b9a-306">65535</span></span>                                                                                                                             |
| <span data-ttu-id="e1b9a-307">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e1b9a-307">Search-Flags</span></span>           | <span data-ttu-id="e1b9a-308">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e1b9a-308">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="e1b9a-309">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e1b9a-309">System-Flags</span></span>           | <span data-ttu-id="e1b9a-310">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e1b9a-310">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="e1b9a-311">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e1b9a-311">Classes used in</span></span>        | [<span data-ttu-id="e1b9a-312">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="e1b9a-312">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> [<span data-ttu-id="e1b9a-313">**Unité d’organisation**</span><span class="sxs-lookup"><span data-stu-id="e1b9a-313">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



 

 





