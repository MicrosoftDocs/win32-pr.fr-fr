---
title: Display-Name-Printable (attribut)
description: Nom complet imprimable d’un objet.
ms.assetid: e8e5ff25-66dd-4c74-9571-9ec765d6d1af
ms.tgt_platform: multiple
keywords:
- Display-Name-attribut imprimable-schéma AD
- Schéma AD de l’attribut displayNamePrintable
topic_type:
- apiref
api_name:
- Display-Name-Printable
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0eff05c2279f026e3a94b707b522509b4801ff27
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845570"
---
# <a name="display-name-printable-attribute"></a><span data-ttu-id="23593-105">Display-Name-Printable (attribut)</span><span class="sxs-lookup"><span data-stu-id="23593-105">Display-Name-Printable attribute</span></span>

<span data-ttu-id="23593-106">Nom complet imprimable d’un objet.</span><span class="sxs-lookup"><span data-stu-id="23593-106">The printable display name for an object.</span></span> <span data-ttu-id="23593-107">Le nom d’affichage imprimable est généralement la combinaison du prénom, de l’initiale du deuxième prénom et du nom de famille de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="23593-107">The printable display name is usually the combination of the user's first name, middle initial, and last name.</span></span>



| <span data-ttu-id="23593-108">Entrée</span><span class="sxs-lookup"><span data-stu-id="23593-108">Entry</span></span> | <span data-ttu-id="23593-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="23593-109">Value</span></span> |
|-------------------|----------------------------------------|
| <span data-ttu-id="23593-110">CN</span><span class="sxs-lookup"><span data-stu-id="23593-110">CN</span></span>                | <span data-ttu-id="23593-111">Nom complet-imprimable</span><span class="sxs-lookup"><span data-stu-id="23593-111">Display-Name-Printable</span></span>                 |
| <span data-ttu-id="23593-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="23593-112">Ldap-Display-Name</span></span> | <span data-ttu-id="23593-113">displayNamePrintable</span><span class="sxs-lookup"><span data-stu-id="23593-113">displayNamePrintable</span></span>                   |
| <span data-ttu-id="23593-114">Taille</span><span class="sxs-lookup"><span data-stu-id="23593-114">Size</span></span>              | \-                                     |
| <span data-ttu-id="23593-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="23593-115">Update Privilege</span></span>  | <span data-ttu-id="23593-116">Administrateur de domaine ou propriétaire du compte.</span><span class="sxs-lookup"><span data-stu-id="23593-116">Domain administrator or account owner.</span></span> |
| <span data-ttu-id="23593-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="23593-117">Update Frequency</span></span>  | \-                                     |
| <span data-ttu-id="23593-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="23593-118">Attribute-Id</span></span>      | <span data-ttu-id="23593-119">1.2.840.113556.1.2.353</span><span class="sxs-lookup"><span data-stu-id="23593-119">1.2.840.113556.1.2.353</span></span>                 |
| <span data-ttu-id="23593-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="23593-120">System-Id-Guid</span></span>    | <span data-ttu-id="23593-121">bf967954-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="23593-121">bf967954-0de6-11d0-a285-00aa003049e2</span></span>   |
| <span data-ttu-id="23593-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="23593-122">Syntax</span></span>            | [<span data-ttu-id="23593-123">**String(IA5)**</span><span class="sxs-lookup"><span data-stu-id="23593-123">**String(IA5)**</span></span>](s-string-ia5.md)    |



## <a name="implementations"></a><span data-ttu-id="23593-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="23593-124">Implementations</span></span>

-   [<span data-ttu-id="23593-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="23593-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="23593-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="23593-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="23593-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="23593-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="23593-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="23593-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="23593-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="23593-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="23593-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="23593-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="23593-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="23593-131">Windows 2000 Server</span></span>



| <span data-ttu-id="23593-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="23593-132">Entry</span></span> | <span data-ttu-id="23593-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="23593-133">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="23593-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="23593-134">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="23593-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="23593-135">MAPI-Id</span></span>                | <span data-ttu-id="23593-136">0x39FF</span><span class="sxs-lookup"><span data-stu-id="23593-136">0x39FF</span></span>                          |
| <span data-ttu-id="23593-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="23593-137">System-Only</span></span>            | <span data-ttu-id="23593-138">Faux</span><span class="sxs-lookup"><span data-stu-id="23593-138">False</span></span>                           |
| <span data-ttu-id="23593-139">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="23593-139">Is-Single-Valued</span></span>       | <span data-ttu-id="23593-140">Vrai</span><span class="sxs-lookup"><span data-stu-id="23593-140">True</span></span>                            |
| <span data-ttu-id="23593-141">Est indexé</span><span class="sxs-lookup"><span data-stu-id="23593-141">Is Indexed</span></span>             | <span data-ttu-id="23593-142">Faux</span><span class="sxs-lookup"><span data-stu-id="23593-142">False</span></span>                           |
| <span data-ttu-id="23593-143">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="23593-143">In Global Catalog</span></span>      | <span data-ttu-id="23593-144">Faux</span><span class="sxs-lookup"><span data-stu-id="23593-144">False</span></span>                           |
| <span data-ttu-id="23593-145">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="23593-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="23593-146">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="23593-146">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="23593-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="23593-147">Range-Lower</span></span>            | <span data-ttu-id="23593-148">1</span><span class="sxs-lookup"><span data-stu-id="23593-148">1</span></span>                               |
| <span data-ttu-id="23593-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="23593-149">Range-Upper</span></span>            | <span data-ttu-id="23593-150">256</span><span class="sxs-lookup"><span data-stu-id="23593-150">256</span></span>                             |
| <span data-ttu-id="23593-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="23593-151">Search-Flags</span></span>           | <span data-ttu-id="23593-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="23593-152">0x00000000</span></span>                      |
| <span data-ttu-id="23593-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="23593-153">System-Flags</span></span>           | <span data-ttu-id="23593-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="23593-154">0x00000010</span></span>                      |
| <span data-ttu-id="23593-155">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="23593-155">Classes used in</span></span>        | [<span data-ttu-id="23593-156">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="23593-156">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="23593-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="23593-157">Windows Server 2003</span></span>



| <span data-ttu-id="23593-158">Entrée</span><span class="sxs-lookup"><span data-stu-id="23593-158">Entry</span></span> | <span data-ttu-id="23593-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="23593-159">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="23593-160">ID de lien</span><span class="sxs-lookup"><span data-stu-id="23593-160">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="23593-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="23593-161">MAPI-Id</span></span>                | <span data-ttu-id="23593-162">0x39FF</span><span class="sxs-lookup"><span data-stu-id="23593-162">0x39FF</span></span>                          |
| <span data-ttu-id="23593-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="23593-163">System-Only</span></span>            | <span data-ttu-id="23593-164">Faux</span><span class="sxs-lookup"><span data-stu-id="23593-164">False</span></span>                           |
| <span data-ttu-id="23593-165">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="23593-165">Is-Single-Valued</span></span>       | <span data-ttu-id="23593-166">Vrai</span><span class="sxs-lookup"><span data-stu-id="23593-166">True</span></span>                            |
| <span data-ttu-id="23593-167">Est indexé</span><span class="sxs-lookup"><span data-stu-id="23593-167">Is Indexed</span></span>             | <span data-ttu-id="23593-168">Faux</span><span class="sxs-lookup"><span data-stu-id="23593-168">False</span></span>                           |
| <span data-ttu-id="23593-169">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="23593-169">In Global Catalog</span></span>      | <span data-ttu-id="23593-170">Faux</span><span class="sxs-lookup"><span data-stu-id="23593-170">False</span></span>                           |
| <span data-ttu-id="23593-171">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="23593-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="23593-172">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="23593-172">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="23593-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="23593-173">Range-Lower</span></span>            | <span data-ttu-id="23593-174">1</span><span class="sxs-lookup"><span data-stu-id="23593-174">1</span></span>                               |
| <span data-ttu-id="23593-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="23593-175">Range-Upper</span></span>            | <span data-ttu-id="23593-176">256</span><span class="sxs-lookup"><span data-stu-id="23593-176">256</span></span>                             |
| <span data-ttu-id="23593-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="23593-177">Search-Flags</span></span>           | <span data-ttu-id="23593-178">0x00000000</span><span class="sxs-lookup"><span data-stu-id="23593-178">0x00000000</span></span>                      |
| <span data-ttu-id="23593-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="23593-179">System-Flags</span></span>           | <span data-ttu-id="23593-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="23593-180">0x00000010</span></span>                      |
| <span data-ttu-id="23593-181">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="23593-181">Classes used in</span></span>        | [<span data-ttu-id="23593-182">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="23593-182">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="23593-183">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="23593-183">Windows Server 2003 R2</span></span>



| <span data-ttu-id="23593-184">Entrée</span><span class="sxs-lookup"><span data-stu-id="23593-184">Entry</span></span> | <span data-ttu-id="23593-185">Valeur</span><span class="sxs-lookup"><span data-stu-id="23593-185">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="23593-186">ID de lien</span><span class="sxs-lookup"><span data-stu-id="23593-186">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="23593-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="23593-187">MAPI-Id</span></span>                | <span data-ttu-id="23593-188">0x39FF</span><span class="sxs-lookup"><span data-stu-id="23593-188">0x39FF</span></span>                          |
| <span data-ttu-id="23593-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="23593-189">System-Only</span></span>            | <span data-ttu-id="23593-190">Faux</span><span class="sxs-lookup"><span data-stu-id="23593-190">False</span></span>                           |
| <span data-ttu-id="23593-191">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="23593-191">Is-Single-Valued</span></span>       | <span data-ttu-id="23593-192">Vrai</span><span class="sxs-lookup"><span data-stu-id="23593-192">True</span></span>                            |
| <span data-ttu-id="23593-193">Est indexé</span><span class="sxs-lookup"><span data-stu-id="23593-193">Is Indexed</span></span>             | <span data-ttu-id="23593-194">Faux</span><span class="sxs-lookup"><span data-stu-id="23593-194">False</span></span>                           |
| <span data-ttu-id="23593-195">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="23593-195">In Global Catalog</span></span>      | <span data-ttu-id="23593-196">Faux</span><span class="sxs-lookup"><span data-stu-id="23593-196">False</span></span>                           |
| <span data-ttu-id="23593-197">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="23593-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="23593-198">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="23593-198">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="23593-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="23593-199">Range-Lower</span></span>            | <span data-ttu-id="23593-200">1</span><span class="sxs-lookup"><span data-stu-id="23593-200">1</span></span>                               |
| <span data-ttu-id="23593-201">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="23593-201">Range-Upper</span></span>            | <span data-ttu-id="23593-202">256</span><span class="sxs-lookup"><span data-stu-id="23593-202">256</span></span>                             |
| <span data-ttu-id="23593-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="23593-203">Search-Flags</span></span>           | <span data-ttu-id="23593-204">0x00000000</span><span class="sxs-lookup"><span data-stu-id="23593-204">0x00000000</span></span>                      |
| <span data-ttu-id="23593-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="23593-205">System-Flags</span></span>           | <span data-ttu-id="23593-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="23593-206">0x00000010</span></span>                      |
| <span data-ttu-id="23593-207">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="23593-207">Classes used in</span></span>        | [<span data-ttu-id="23593-208">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="23593-208">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="23593-209">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="23593-209">Windows Server 2008</span></span>



| <span data-ttu-id="23593-210">Entrée</span><span class="sxs-lookup"><span data-stu-id="23593-210">Entry</span></span> | <span data-ttu-id="23593-211">Valeur</span><span class="sxs-lookup"><span data-stu-id="23593-211">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="23593-212">ID de lien</span><span class="sxs-lookup"><span data-stu-id="23593-212">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="23593-213">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="23593-213">MAPI-Id</span></span>                | <span data-ttu-id="23593-214">0x39FF</span><span class="sxs-lookup"><span data-stu-id="23593-214">0x39FF</span></span>                          |
| <span data-ttu-id="23593-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="23593-215">System-Only</span></span>            | <span data-ttu-id="23593-216">Faux</span><span class="sxs-lookup"><span data-stu-id="23593-216">False</span></span>                           |
| <span data-ttu-id="23593-217">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="23593-217">Is-Single-Valued</span></span>       | <span data-ttu-id="23593-218">Vrai</span><span class="sxs-lookup"><span data-stu-id="23593-218">True</span></span>                            |
| <span data-ttu-id="23593-219">Est indexé</span><span class="sxs-lookup"><span data-stu-id="23593-219">Is Indexed</span></span>             | <span data-ttu-id="23593-220">Faux</span><span class="sxs-lookup"><span data-stu-id="23593-220">False</span></span>                           |
| <span data-ttu-id="23593-221">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="23593-221">In Global Catalog</span></span>      | <span data-ttu-id="23593-222">Faux</span><span class="sxs-lookup"><span data-stu-id="23593-222">False</span></span>                           |
| <span data-ttu-id="23593-223">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="23593-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="23593-224">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="23593-224">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="23593-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="23593-225">Range-Lower</span></span>            | <span data-ttu-id="23593-226">1</span><span class="sxs-lookup"><span data-stu-id="23593-226">1</span></span>                               |
| <span data-ttu-id="23593-227">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="23593-227">Range-Upper</span></span>            | <span data-ttu-id="23593-228">256</span><span class="sxs-lookup"><span data-stu-id="23593-228">256</span></span>                             |
| <span data-ttu-id="23593-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="23593-229">Search-Flags</span></span>           | <span data-ttu-id="23593-230">0x00000000</span><span class="sxs-lookup"><span data-stu-id="23593-230">0x00000000</span></span>                      |
| <span data-ttu-id="23593-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="23593-231">System-Flags</span></span>           | <span data-ttu-id="23593-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="23593-232">0x00000010</span></span>                      |
| <span data-ttu-id="23593-233">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="23593-233">Classes used in</span></span>        | [<span data-ttu-id="23593-234">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="23593-234">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="23593-235">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="23593-235">Windows Server 2008 R2</span></span>



| <span data-ttu-id="23593-236">Entrée</span><span class="sxs-lookup"><span data-stu-id="23593-236">Entry</span></span> | <span data-ttu-id="23593-237">Valeur</span><span class="sxs-lookup"><span data-stu-id="23593-237">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="23593-238">ID de lien</span><span class="sxs-lookup"><span data-stu-id="23593-238">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="23593-239">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="23593-239">MAPI-Id</span></span>                | <span data-ttu-id="23593-240">0x39FF</span><span class="sxs-lookup"><span data-stu-id="23593-240">0x39FF</span></span>                          |
| <span data-ttu-id="23593-241">System-Only</span><span class="sxs-lookup"><span data-stu-id="23593-241">System-Only</span></span>            | <span data-ttu-id="23593-242">Faux</span><span class="sxs-lookup"><span data-stu-id="23593-242">False</span></span>                           |
| <span data-ttu-id="23593-243">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="23593-243">Is-Single-Valued</span></span>       | <span data-ttu-id="23593-244">Vrai</span><span class="sxs-lookup"><span data-stu-id="23593-244">True</span></span>                            |
| <span data-ttu-id="23593-245">Est indexé</span><span class="sxs-lookup"><span data-stu-id="23593-245">Is Indexed</span></span>             | <span data-ttu-id="23593-246">Faux</span><span class="sxs-lookup"><span data-stu-id="23593-246">False</span></span>                           |
| <span data-ttu-id="23593-247">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="23593-247">In Global Catalog</span></span>      | <span data-ttu-id="23593-248">Faux</span><span class="sxs-lookup"><span data-stu-id="23593-248">False</span></span>                           |
| <span data-ttu-id="23593-249">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="23593-249">NT-Security-Descriptor</span></span> | <span data-ttu-id="23593-250">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="23593-250">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="23593-251">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="23593-251">Range-Lower</span></span>            | <span data-ttu-id="23593-252">1</span><span class="sxs-lookup"><span data-stu-id="23593-252">1</span></span>                               |
| <span data-ttu-id="23593-253">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="23593-253">Range-Upper</span></span>            | <span data-ttu-id="23593-254">256</span><span class="sxs-lookup"><span data-stu-id="23593-254">256</span></span>                             |
| <span data-ttu-id="23593-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="23593-255">Search-Flags</span></span>           | <span data-ttu-id="23593-256">0x00000000</span><span class="sxs-lookup"><span data-stu-id="23593-256">0x00000000</span></span>                      |
| <span data-ttu-id="23593-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="23593-257">System-Flags</span></span>           | <span data-ttu-id="23593-258">0x00000010</span><span class="sxs-lookup"><span data-stu-id="23593-258">0x00000010</span></span>                      |
| <span data-ttu-id="23593-259">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="23593-259">Classes used in</span></span>        | [<span data-ttu-id="23593-260">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="23593-260">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="23593-261">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="23593-261">Windows Server 2012</span></span>



| <span data-ttu-id="23593-262">Entrée</span><span class="sxs-lookup"><span data-stu-id="23593-262">Entry</span></span> | <span data-ttu-id="23593-263">Valeur</span><span class="sxs-lookup"><span data-stu-id="23593-263">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="23593-264">ID de lien</span><span class="sxs-lookup"><span data-stu-id="23593-264">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="23593-265">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="23593-265">MAPI-Id</span></span>                | <span data-ttu-id="23593-266">0x39FF</span><span class="sxs-lookup"><span data-stu-id="23593-266">0x39FF</span></span>                          |
| <span data-ttu-id="23593-267">System-Only</span><span class="sxs-lookup"><span data-stu-id="23593-267">System-Only</span></span>            | <span data-ttu-id="23593-268">Faux</span><span class="sxs-lookup"><span data-stu-id="23593-268">False</span></span>                           |
| <span data-ttu-id="23593-269">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="23593-269">Is-Single-Valued</span></span>       | <span data-ttu-id="23593-270">Vrai</span><span class="sxs-lookup"><span data-stu-id="23593-270">True</span></span>                            |
| <span data-ttu-id="23593-271">Est indexé</span><span class="sxs-lookup"><span data-stu-id="23593-271">Is Indexed</span></span>             | <span data-ttu-id="23593-272">Faux</span><span class="sxs-lookup"><span data-stu-id="23593-272">False</span></span>                           |
| <span data-ttu-id="23593-273">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="23593-273">In Global Catalog</span></span>      | <span data-ttu-id="23593-274">Faux</span><span class="sxs-lookup"><span data-stu-id="23593-274">False</span></span>                           |
| <span data-ttu-id="23593-275">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="23593-275">NT-Security-Descriptor</span></span> | <span data-ttu-id="23593-276">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="23593-276">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="23593-277">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="23593-277">Range-Lower</span></span>            | <span data-ttu-id="23593-278">1</span><span class="sxs-lookup"><span data-stu-id="23593-278">1</span></span>                               |
| <span data-ttu-id="23593-279">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="23593-279">Range-Upper</span></span>            | <span data-ttu-id="23593-280">256</span><span class="sxs-lookup"><span data-stu-id="23593-280">256</span></span>                             |
| <span data-ttu-id="23593-281">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="23593-281">Search-Flags</span></span>           | <span data-ttu-id="23593-282">0x00000000</span><span class="sxs-lookup"><span data-stu-id="23593-282">0x00000000</span></span>                      |
| <span data-ttu-id="23593-283">System-Flags</span><span class="sxs-lookup"><span data-stu-id="23593-283">System-Flags</span></span>           | <span data-ttu-id="23593-284">0x00000010</span><span class="sxs-lookup"><span data-stu-id="23593-284">0x00000010</span></span>                      |
| <span data-ttu-id="23593-285">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="23593-285">Classes used in</span></span>        | [<span data-ttu-id="23593-286">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="23593-286">**Top**</span></span>](c-top.md)<br/> |



 

 





