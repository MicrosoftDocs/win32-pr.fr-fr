---
title: Attribut RDN
description: Nom unique relatif (RDN) d’un objet.
ms.assetid: 07fe0e81-1b18-4dbb-abca-a059a8bf993e
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut RDN
- Schéma Active Directory de l’attribut Name
topic_type:
- apiref
api_name:
- RDN
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe49bd525d0fa3f4ed95874f2020d9d2a5eb9554
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106516724"
---
# <a name="rdn-attribute"></a><span data-ttu-id="86413-105">Attribut RDN</span><span class="sxs-lookup"><span data-stu-id="86413-105">RDN attribute</span></span>

<span data-ttu-id="86413-106">Nom unique relatif (RDN) d’un objet.</span><span class="sxs-lookup"><span data-stu-id="86413-106">The Relative Distinguished Name (RDN) of an object.</span></span> <span data-ttu-id="86413-107">Un RDN est la partie relative d’un nom unique (DN), qui identifie de façon unique un objet LDAP.</span><span class="sxs-lookup"><span data-stu-id="86413-107">An RDN is the relative portion of a distinguished name (DN), which uniquely identifies an LDAP object.</span></span>



| <span data-ttu-id="86413-108">Entrée</span><span class="sxs-lookup"><span data-stu-id="86413-108">Entry</span></span> | <span data-ttu-id="86413-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="86413-109">Value</span></span> |
|-------------------|------------------------------------------------|
| <span data-ttu-id="86413-110">CN</span><span class="sxs-lookup"><span data-stu-id="86413-110">CN</span></span>                | <span data-ttu-id="86413-111">UNIQUE</span><span class="sxs-lookup"><span data-stu-id="86413-111">RDN</span></span>                                            |
| <span data-ttu-id="86413-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="86413-112">Ldap-Display-Name</span></span> | <span data-ttu-id="86413-113">name</span><span class="sxs-lookup"><span data-stu-id="86413-113">name</span></span>                                           |
| <span data-ttu-id="86413-114">Taille</span><span class="sxs-lookup"><span data-stu-id="86413-114">Size</span></span>              | \-                                             |
| <span data-ttu-id="86413-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="86413-115">Update Privilege</span></span>  | <span data-ttu-id="86413-116">Cette valeur est définie par l’administrateur de schéma.</span><span class="sxs-lookup"><span data-stu-id="86413-116">This value is set by the schema administrator.</span></span> |
| <span data-ttu-id="86413-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="86413-117">Update Frequency</span></span>  | \-                                             |
| <span data-ttu-id="86413-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="86413-118">Attribute-Id</span></span>      | <span data-ttu-id="86413-119">1.2.840.113556.1.4.1</span><span class="sxs-lookup"><span data-stu-id="86413-119">1.2.840.113556.1.4.1</span></span>                           |
| <span data-ttu-id="86413-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="86413-120">System-Id-Guid</span></span>    | <span data-ttu-id="86413-121">bf967a0e-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="86413-121">bf967a0e-0de6-11d0-a285-00aa003049e2</span></span>           |
| <span data-ttu-id="86413-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="86413-122">Syntax</span></span>            | [<span data-ttu-id="86413-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="86413-123">**String(Unicode)**</span></span>](s-string-unicode.md)    |



## <a name="implementations"></a><span data-ttu-id="86413-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="86413-124">Implementations</span></span>

-   [<span data-ttu-id="86413-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="86413-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="86413-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="86413-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="86413-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="86413-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="86413-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="86413-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="86413-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="86413-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="86413-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="86413-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="86413-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="86413-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="86413-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="86413-132">Windows 2000 Server</span></span>



| <span data-ttu-id="86413-133">Entrée</span><span class="sxs-lookup"><span data-stu-id="86413-133">Entry</span></span> | <span data-ttu-id="86413-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="86413-134">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="86413-135">ID de lien</span><span class="sxs-lookup"><span data-stu-id="86413-135">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="86413-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="86413-136">MAPI-Id</span></span>                | <span data-ttu-id="86413-137">0x8202</span><span class="sxs-lookup"><span data-stu-id="86413-137">0x8202</span></span>                          |
| <span data-ttu-id="86413-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="86413-138">System-Only</span></span>            | <span data-ttu-id="86413-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="86413-139">True</span></span>                            |
| <span data-ttu-id="86413-140">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="86413-140">Is-Single-Valued</span></span>       | <span data-ttu-id="86413-141">Vrai</span><span class="sxs-lookup"><span data-stu-id="86413-141">True</span></span>                            |
| <span data-ttu-id="86413-142">Est indexé</span><span class="sxs-lookup"><span data-stu-id="86413-142">Is Indexed</span></span>             | <span data-ttu-id="86413-143">Vrai</span><span class="sxs-lookup"><span data-stu-id="86413-143">True</span></span>                            |
| <span data-ttu-id="86413-144">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="86413-144">In Global Catalog</span></span>      | <span data-ttu-id="86413-145">Vrai</span><span class="sxs-lookup"><span data-stu-id="86413-145">True</span></span>                            |
| <span data-ttu-id="86413-146">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="86413-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="86413-147">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="86413-147">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="86413-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="86413-148">Range-Lower</span></span>            | <span data-ttu-id="86413-149">1</span><span class="sxs-lookup"><span data-stu-id="86413-149">1</span></span>                               |
| <span data-ttu-id="86413-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="86413-150">Range-Upper</span></span>            | <span data-ttu-id="86413-151">255</span><span class="sxs-lookup"><span data-stu-id="86413-151">255</span></span>                             |
| <span data-ttu-id="86413-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="86413-152">Search-Flags</span></span>           | <span data-ttu-id="86413-153">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="86413-153">0x0000000D</span></span>                      |
| <span data-ttu-id="86413-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="86413-154">System-Flags</span></span>           | <span data-ttu-id="86413-155">0x00000012</span><span class="sxs-lookup"><span data-stu-id="86413-155">0x00000012</span></span>                      |
| <span data-ttu-id="86413-156">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="86413-156">Classes used in</span></span>        | [<span data-ttu-id="86413-157">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="86413-157">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="86413-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="86413-158">Windows Server 2003</span></span>



| <span data-ttu-id="86413-159">Entrée</span><span class="sxs-lookup"><span data-stu-id="86413-159">Entry</span></span> | <span data-ttu-id="86413-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="86413-160">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="86413-161">ID de lien</span><span class="sxs-lookup"><span data-stu-id="86413-161">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="86413-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="86413-162">MAPI-Id</span></span>                | <span data-ttu-id="86413-163">0x8202</span><span class="sxs-lookup"><span data-stu-id="86413-163">0x8202</span></span>                          |
| <span data-ttu-id="86413-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="86413-164">System-Only</span></span>            | <span data-ttu-id="86413-165">Vrai</span><span class="sxs-lookup"><span data-stu-id="86413-165">True</span></span>                            |
| <span data-ttu-id="86413-166">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="86413-166">Is-Single-Valued</span></span>       | <span data-ttu-id="86413-167">Vrai</span><span class="sxs-lookup"><span data-stu-id="86413-167">True</span></span>                            |
| <span data-ttu-id="86413-168">Est indexé</span><span class="sxs-lookup"><span data-stu-id="86413-168">Is Indexed</span></span>             | <span data-ttu-id="86413-169">Vrai</span><span class="sxs-lookup"><span data-stu-id="86413-169">True</span></span>                            |
| <span data-ttu-id="86413-170">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="86413-170">In Global Catalog</span></span>      | <span data-ttu-id="86413-171">Vrai</span><span class="sxs-lookup"><span data-stu-id="86413-171">True</span></span>                            |
| <span data-ttu-id="86413-172">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="86413-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="86413-173">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="86413-173">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="86413-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="86413-174">Range-Lower</span></span>            | <span data-ttu-id="86413-175">1</span><span class="sxs-lookup"><span data-stu-id="86413-175">1</span></span>                               |
| <span data-ttu-id="86413-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="86413-176">Range-Upper</span></span>            | <span data-ttu-id="86413-177">255</span><span class="sxs-lookup"><span data-stu-id="86413-177">255</span></span>                             |
| <span data-ttu-id="86413-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="86413-178">Search-Flags</span></span>           | <span data-ttu-id="86413-179">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="86413-179">0x0000000D</span></span>                      |
| <span data-ttu-id="86413-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="86413-180">System-Flags</span></span>           | <span data-ttu-id="86413-181">0x00000012</span><span class="sxs-lookup"><span data-stu-id="86413-181">0x00000012</span></span>                      |
| <span data-ttu-id="86413-182">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="86413-182">Classes used in</span></span>        | [<span data-ttu-id="86413-183">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="86413-183">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="86413-184">ADAM</span><span class="sxs-lookup"><span data-stu-id="86413-184">ADAM</span></span>



| <span data-ttu-id="86413-185">Entrée</span><span class="sxs-lookup"><span data-stu-id="86413-185">Entry</span></span> | <span data-ttu-id="86413-186">Valeur</span><span class="sxs-lookup"><span data-stu-id="86413-186">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="86413-187">ID de lien</span><span class="sxs-lookup"><span data-stu-id="86413-187">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="86413-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="86413-188">MAPI-Id</span></span>                | <span data-ttu-id="86413-189">0x8202</span><span class="sxs-lookup"><span data-stu-id="86413-189">0x8202</span></span>                          |
| <span data-ttu-id="86413-190">System-Only</span><span class="sxs-lookup"><span data-stu-id="86413-190">System-Only</span></span>            | <span data-ttu-id="86413-191">Vrai</span><span class="sxs-lookup"><span data-stu-id="86413-191">True</span></span>                            |
| <span data-ttu-id="86413-192">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="86413-192">Is-Single-Valued</span></span>       | <span data-ttu-id="86413-193">Vrai</span><span class="sxs-lookup"><span data-stu-id="86413-193">True</span></span>                            |
| <span data-ttu-id="86413-194">Est indexé</span><span class="sxs-lookup"><span data-stu-id="86413-194">Is Indexed</span></span>             | <span data-ttu-id="86413-195">Vrai</span><span class="sxs-lookup"><span data-stu-id="86413-195">True</span></span>                            |
| <span data-ttu-id="86413-196">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="86413-196">In Global Catalog</span></span>      | <span data-ttu-id="86413-197">Vrai</span><span class="sxs-lookup"><span data-stu-id="86413-197">True</span></span>                            |
| <span data-ttu-id="86413-198">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="86413-198">NT-Security-Descriptor</span></span> | <span data-ttu-id="86413-199">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="86413-199">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="86413-200">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="86413-200">Range-Lower</span></span>            | <span data-ttu-id="86413-201">1</span><span class="sxs-lookup"><span data-stu-id="86413-201">1</span></span>                               |
| <span data-ttu-id="86413-202">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="86413-202">Range-Upper</span></span>            | <span data-ttu-id="86413-203">255</span><span class="sxs-lookup"><span data-stu-id="86413-203">255</span></span>                             |
| <span data-ttu-id="86413-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="86413-204">Search-Flags</span></span>           | <span data-ttu-id="86413-205">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="86413-205">0x0000000D</span></span>                      |
| <span data-ttu-id="86413-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="86413-206">System-Flags</span></span>           | <span data-ttu-id="86413-207">0x00000012</span><span class="sxs-lookup"><span data-stu-id="86413-207">0x00000012</span></span>                      |
| <span data-ttu-id="86413-208">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="86413-208">Classes used in</span></span>        | [<span data-ttu-id="86413-209">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="86413-209">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="86413-210">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="86413-210">Windows Server 2003 R2</span></span>



| <span data-ttu-id="86413-211">Entrée</span><span class="sxs-lookup"><span data-stu-id="86413-211">Entry</span></span> | <span data-ttu-id="86413-212">Valeur</span><span class="sxs-lookup"><span data-stu-id="86413-212">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="86413-213">ID de lien</span><span class="sxs-lookup"><span data-stu-id="86413-213">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="86413-214">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="86413-214">MAPI-Id</span></span>                | <span data-ttu-id="86413-215">0x8202</span><span class="sxs-lookup"><span data-stu-id="86413-215">0x8202</span></span>                          |
| <span data-ttu-id="86413-216">System-Only</span><span class="sxs-lookup"><span data-stu-id="86413-216">System-Only</span></span>            | <span data-ttu-id="86413-217">Vrai</span><span class="sxs-lookup"><span data-stu-id="86413-217">True</span></span>                            |
| <span data-ttu-id="86413-218">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="86413-218">Is-Single-Valued</span></span>       | <span data-ttu-id="86413-219">Vrai</span><span class="sxs-lookup"><span data-stu-id="86413-219">True</span></span>                            |
| <span data-ttu-id="86413-220">Est indexé</span><span class="sxs-lookup"><span data-stu-id="86413-220">Is Indexed</span></span>             | <span data-ttu-id="86413-221">Vrai</span><span class="sxs-lookup"><span data-stu-id="86413-221">True</span></span>                            |
| <span data-ttu-id="86413-222">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="86413-222">In Global Catalog</span></span>      | <span data-ttu-id="86413-223">Vrai</span><span class="sxs-lookup"><span data-stu-id="86413-223">True</span></span>                            |
| <span data-ttu-id="86413-224">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="86413-224">NT-Security-Descriptor</span></span> | <span data-ttu-id="86413-225">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="86413-225">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="86413-226">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="86413-226">Range-Lower</span></span>            | <span data-ttu-id="86413-227">1</span><span class="sxs-lookup"><span data-stu-id="86413-227">1</span></span>                               |
| <span data-ttu-id="86413-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="86413-228">Range-Upper</span></span>            | <span data-ttu-id="86413-229">255</span><span class="sxs-lookup"><span data-stu-id="86413-229">255</span></span>                             |
| <span data-ttu-id="86413-230">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="86413-230">Search-Flags</span></span>           | <span data-ttu-id="86413-231">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="86413-231">0x0000000D</span></span>                      |
| <span data-ttu-id="86413-232">System-Flags</span><span class="sxs-lookup"><span data-stu-id="86413-232">System-Flags</span></span>           | <span data-ttu-id="86413-233">0x00000012</span><span class="sxs-lookup"><span data-stu-id="86413-233">0x00000012</span></span>                      |
| <span data-ttu-id="86413-234">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="86413-234">Classes used in</span></span>        | [<span data-ttu-id="86413-235">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="86413-235">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="86413-236">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="86413-236">Windows Server 2008</span></span>



| <span data-ttu-id="86413-237">Entrée</span><span class="sxs-lookup"><span data-stu-id="86413-237">Entry</span></span> | <span data-ttu-id="86413-238">Valeur</span><span class="sxs-lookup"><span data-stu-id="86413-238">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="86413-239">ID de lien</span><span class="sxs-lookup"><span data-stu-id="86413-239">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="86413-240">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="86413-240">MAPI-Id</span></span>                | <span data-ttu-id="86413-241">0x8202</span><span class="sxs-lookup"><span data-stu-id="86413-241">0x8202</span></span>                          |
| <span data-ttu-id="86413-242">System-Only</span><span class="sxs-lookup"><span data-stu-id="86413-242">System-Only</span></span>            | <span data-ttu-id="86413-243">Vrai</span><span class="sxs-lookup"><span data-stu-id="86413-243">True</span></span>                            |
| <span data-ttu-id="86413-244">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="86413-244">Is-Single-Valued</span></span>       | <span data-ttu-id="86413-245">Vrai</span><span class="sxs-lookup"><span data-stu-id="86413-245">True</span></span>                            |
| <span data-ttu-id="86413-246">Est indexé</span><span class="sxs-lookup"><span data-stu-id="86413-246">Is Indexed</span></span>             | <span data-ttu-id="86413-247">Vrai</span><span class="sxs-lookup"><span data-stu-id="86413-247">True</span></span>                            |
| <span data-ttu-id="86413-248">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="86413-248">In Global Catalog</span></span>      | <span data-ttu-id="86413-249">Vrai</span><span class="sxs-lookup"><span data-stu-id="86413-249">True</span></span>                            |
| <span data-ttu-id="86413-250">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="86413-250">NT-Security-Descriptor</span></span> | <span data-ttu-id="86413-251">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="86413-251">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="86413-252">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="86413-252">Range-Lower</span></span>            | <span data-ttu-id="86413-253">1</span><span class="sxs-lookup"><span data-stu-id="86413-253">1</span></span>                               |
| <span data-ttu-id="86413-254">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="86413-254">Range-Upper</span></span>            | <span data-ttu-id="86413-255">255</span><span class="sxs-lookup"><span data-stu-id="86413-255">255</span></span>                             |
| <span data-ttu-id="86413-256">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="86413-256">Search-Flags</span></span>           | <span data-ttu-id="86413-257">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="86413-257">0x0000000D</span></span>                      |
| <span data-ttu-id="86413-258">System-Flags</span><span class="sxs-lookup"><span data-stu-id="86413-258">System-Flags</span></span>           | <span data-ttu-id="86413-259">0x00000012</span><span class="sxs-lookup"><span data-stu-id="86413-259">0x00000012</span></span>                      |
| <span data-ttu-id="86413-260">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="86413-260">Classes used in</span></span>        | [<span data-ttu-id="86413-261">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="86413-261">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="86413-262">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="86413-262">Windows Server 2008 R2</span></span>



| <span data-ttu-id="86413-263">Entrée</span><span class="sxs-lookup"><span data-stu-id="86413-263">Entry</span></span> | <span data-ttu-id="86413-264">Valeur</span><span class="sxs-lookup"><span data-stu-id="86413-264">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="86413-265">ID de lien</span><span class="sxs-lookup"><span data-stu-id="86413-265">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="86413-266">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="86413-266">MAPI-Id</span></span>                | <span data-ttu-id="86413-267">0x8202</span><span class="sxs-lookup"><span data-stu-id="86413-267">0x8202</span></span>                          |
| <span data-ttu-id="86413-268">System-Only</span><span class="sxs-lookup"><span data-stu-id="86413-268">System-Only</span></span>            | <span data-ttu-id="86413-269">Vrai</span><span class="sxs-lookup"><span data-stu-id="86413-269">True</span></span>                            |
| <span data-ttu-id="86413-270">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="86413-270">Is-Single-Valued</span></span>       | <span data-ttu-id="86413-271">Vrai</span><span class="sxs-lookup"><span data-stu-id="86413-271">True</span></span>                            |
| <span data-ttu-id="86413-272">Est indexé</span><span class="sxs-lookup"><span data-stu-id="86413-272">Is Indexed</span></span>             | <span data-ttu-id="86413-273">Vrai</span><span class="sxs-lookup"><span data-stu-id="86413-273">True</span></span>                            |
| <span data-ttu-id="86413-274">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="86413-274">In Global Catalog</span></span>      | <span data-ttu-id="86413-275">Vrai</span><span class="sxs-lookup"><span data-stu-id="86413-275">True</span></span>                            |
| <span data-ttu-id="86413-276">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="86413-276">NT-Security-Descriptor</span></span> | <span data-ttu-id="86413-277">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="86413-277">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="86413-278">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="86413-278">Range-Lower</span></span>            | <span data-ttu-id="86413-279">1</span><span class="sxs-lookup"><span data-stu-id="86413-279">1</span></span>                               |
| <span data-ttu-id="86413-280">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="86413-280">Range-Upper</span></span>            | <span data-ttu-id="86413-281">255</span><span class="sxs-lookup"><span data-stu-id="86413-281">255</span></span>                             |
| <span data-ttu-id="86413-282">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="86413-282">Search-Flags</span></span>           | <span data-ttu-id="86413-283">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="86413-283">0x0000000D</span></span>                      |
| <span data-ttu-id="86413-284">System-Flags</span><span class="sxs-lookup"><span data-stu-id="86413-284">System-Flags</span></span>           | <span data-ttu-id="86413-285">0x00000012</span><span class="sxs-lookup"><span data-stu-id="86413-285">0x00000012</span></span>                      |
| <span data-ttu-id="86413-286">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="86413-286">Classes used in</span></span>        | [<span data-ttu-id="86413-287">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="86413-287">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="86413-288">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="86413-288">Windows Server 2012</span></span>



| <span data-ttu-id="86413-289">Entrée</span><span class="sxs-lookup"><span data-stu-id="86413-289">Entry</span></span> | <span data-ttu-id="86413-290">Valeur</span><span class="sxs-lookup"><span data-stu-id="86413-290">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="86413-291">ID de lien</span><span class="sxs-lookup"><span data-stu-id="86413-291">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="86413-292">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="86413-292">MAPI-Id</span></span>                | <span data-ttu-id="86413-293">0x8202</span><span class="sxs-lookup"><span data-stu-id="86413-293">0x8202</span></span>                          |
| <span data-ttu-id="86413-294">System-Only</span><span class="sxs-lookup"><span data-stu-id="86413-294">System-Only</span></span>            | <span data-ttu-id="86413-295">Vrai</span><span class="sxs-lookup"><span data-stu-id="86413-295">True</span></span>                            |
| <span data-ttu-id="86413-296">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="86413-296">Is-Single-Valued</span></span>       | <span data-ttu-id="86413-297">Vrai</span><span class="sxs-lookup"><span data-stu-id="86413-297">True</span></span>                            |
| <span data-ttu-id="86413-298">Est indexé</span><span class="sxs-lookup"><span data-stu-id="86413-298">Is Indexed</span></span>             | <span data-ttu-id="86413-299">Vrai</span><span class="sxs-lookup"><span data-stu-id="86413-299">True</span></span>                            |
| <span data-ttu-id="86413-300">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="86413-300">In Global Catalog</span></span>      | <span data-ttu-id="86413-301">Vrai</span><span class="sxs-lookup"><span data-stu-id="86413-301">True</span></span>                            |
| <span data-ttu-id="86413-302">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="86413-302">NT-Security-Descriptor</span></span> | <span data-ttu-id="86413-303">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="86413-303">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="86413-304">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="86413-304">Range-Lower</span></span>            | <span data-ttu-id="86413-305">1</span><span class="sxs-lookup"><span data-stu-id="86413-305">1</span></span>                               |
| <span data-ttu-id="86413-306">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="86413-306">Range-Upper</span></span>            | <span data-ttu-id="86413-307">255</span><span class="sxs-lookup"><span data-stu-id="86413-307">255</span></span>                             |
| <span data-ttu-id="86413-308">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="86413-308">Search-Flags</span></span>           | <span data-ttu-id="86413-309">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="86413-309">0x0000000D</span></span>                      |
| <span data-ttu-id="86413-310">System-Flags</span><span class="sxs-lookup"><span data-stu-id="86413-310">System-Flags</span></span>           | <span data-ttu-id="86413-311">0x00000012</span><span class="sxs-lookup"><span data-stu-id="86413-311">0x00000012</span></span>                      |
| <span data-ttu-id="86413-312">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="86413-312">Classes used in</span></span>        | [<span data-ttu-id="86413-313">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="86413-313">**Top**</span></span>](c-top.md)<br/> |



 

 





