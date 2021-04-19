---
title: Attribut Root-DNS supérieur
description: Il s’agit d’un attribut système utilisé pour la génération de références.
ms.assetid: 421f8315-26e2-457d-ae76-868b7fc6551a
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut racine DNS supérieur
- Schéma AD de l’attribut superiorDNSRoot
topic_type:
- apiref
api_name:
- Superior-DNS-Root
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6561839cf5137968adbac628ad6046b8b86dab85
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106514683"
---
# <a name="superior-dns-root-attribute"></a><span data-ttu-id="35ea9-105">Attribut Root-DNS supérieur</span><span class="sxs-lookup"><span data-stu-id="35ea9-105">Superior-DNS-Root attribute</span></span>

<span data-ttu-id="35ea9-106">Il s’agit d’un attribut système utilisé pour la génération de références.</span><span class="sxs-lookup"><span data-stu-id="35ea9-106">This is a system attribute that is used for referrals generation.</span></span>



| <span data-ttu-id="35ea9-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="35ea9-107">Entry</span></span> | <span data-ttu-id="35ea9-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="35ea9-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="35ea9-109">CN</span><span class="sxs-lookup"><span data-stu-id="35ea9-109">CN</span></span>                | <span data-ttu-id="35ea9-110">Supérieure-DNS-racine</span><span class="sxs-lookup"><span data-stu-id="35ea9-110">Superior-DNS-Root</span></span>                           |
| <span data-ttu-id="35ea9-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="35ea9-111">Ldap-Display-Name</span></span> | <span data-ttu-id="35ea9-112">superiorDNSRoot</span><span class="sxs-lookup"><span data-stu-id="35ea9-112">superiorDNSRoot</span></span>                             |
| <span data-ttu-id="35ea9-113">Taille</span><span class="sxs-lookup"><span data-stu-id="35ea9-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="35ea9-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="35ea9-114">Update Privilege</span></span>  | <span data-ttu-id="35ea9-115">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="35ea9-115">This value is set by the system.</span></span>            |
| <span data-ttu-id="35ea9-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="35ea9-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="35ea9-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="35ea9-117">Attribute-Id</span></span>      | <span data-ttu-id="35ea9-118">1.2.840.113556.1.4.532</span><span class="sxs-lookup"><span data-stu-id="35ea9-118">1.2.840.113556.1.4.532</span></span>                      |
| <span data-ttu-id="35ea9-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="35ea9-119">System-Id-Guid</span></span>    | <span data-ttu-id="35ea9-120">5245801d-ca6a-11d0-afff-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="35ea9-120">5245801d-ca6a-11d0-afff-0000f80367c1</span></span>        |
| <span data-ttu-id="35ea9-121">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="35ea9-121">Syntax</span></span>            | [<span data-ttu-id="35ea9-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="35ea9-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="35ea9-123">Implémentations</span><span class="sxs-lookup"><span data-stu-id="35ea9-123">Implementations</span></span>

-   [<span data-ttu-id="35ea9-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="35ea9-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="35ea9-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="35ea9-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="35ea9-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="35ea9-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="35ea9-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="35ea9-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="35ea9-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="35ea9-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="35ea9-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="35ea9-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="35ea9-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="35ea9-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="35ea9-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="35ea9-131">Windows 2000 Server</span></span>



| <span data-ttu-id="35ea9-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="35ea9-132">Entry</span></span> | <span data-ttu-id="35ea9-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="35ea9-133">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="35ea9-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="35ea9-134">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="35ea9-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="35ea9-135">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="35ea9-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="35ea9-136">System-Only</span></span>            | <span data-ttu-id="35ea9-137">Faux</span><span class="sxs-lookup"><span data-stu-id="35ea9-137">False</span></span>                                      |
| <span data-ttu-id="35ea9-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="35ea9-138">Is-Single-Valued</span></span>       | <span data-ttu-id="35ea9-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="35ea9-139">True</span></span>                                       |
| <span data-ttu-id="35ea9-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="35ea9-140">Is Indexed</span></span>             | <span data-ttu-id="35ea9-141">Faux</span><span class="sxs-lookup"><span data-stu-id="35ea9-141">False</span></span>                                      |
| <span data-ttu-id="35ea9-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="35ea9-142">In Global Catalog</span></span>      | <span data-ttu-id="35ea9-143">Faux</span><span class="sxs-lookup"><span data-stu-id="35ea9-143">False</span></span>                                      |
| <span data-ttu-id="35ea9-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="35ea9-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="35ea9-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="35ea9-145">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="35ea9-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="35ea9-146">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="35ea9-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="35ea9-147">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="35ea9-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="35ea9-148">Search-Flags</span></span>           | <span data-ttu-id="35ea9-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="35ea9-149">0x00000000</span></span>                                 |
| <span data-ttu-id="35ea9-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="35ea9-150">System-Flags</span></span>           | <span data-ttu-id="35ea9-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="35ea9-151">0x00000010</span></span>                                 |
| <span data-ttu-id="35ea9-152">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="35ea9-152">Classes used in</span></span>        | [<span data-ttu-id="35ea9-153">**Référence croisée**</span><span class="sxs-lookup"><span data-stu-id="35ea9-153">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="35ea9-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="35ea9-154">Windows Server 2003</span></span>



| <span data-ttu-id="35ea9-155">Entrée</span><span class="sxs-lookup"><span data-stu-id="35ea9-155">Entry</span></span> | <span data-ttu-id="35ea9-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="35ea9-156">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="35ea9-157">ID de lien</span><span class="sxs-lookup"><span data-stu-id="35ea9-157">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="35ea9-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="35ea9-158">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="35ea9-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="35ea9-159">System-Only</span></span>            | <span data-ttu-id="35ea9-160">Faux</span><span class="sxs-lookup"><span data-stu-id="35ea9-160">False</span></span>                                      |
| <span data-ttu-id="35ea9-161">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="35ea9-161">Is-Single-Valued</span></span>       | <span data-ttu-id="35ea9-162">Vrai</span><span class="sxs-lookup"><span data-stu-id="35ea9-162">True</span></span>                                       |
| <span data-ttu-id="35ea9-163">Est indexé</span><span class="sxs-lookup"><span data-stu-id="35ea9-163">Is Indexed</span></span>             | <span data-ttu-id="35ea9-164">Faux</span><span class="sxs-lookup"><span data-stu-id="35ea9-164">False</span></span>                                      |
| <span data-ttu-id="35ea9-165">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="35ea9-165">In Global Catalog</span></span>      | <span data-ttu-id="35ea9-166">Faux</span><span class="sxs-lookup"><span data-stu-id="35ea9-166">False</span></span>                                      |
| <span data-ttu-id="35ea9-167">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="35ea9-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="35ea9-168">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="35ea9-168">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="35ea9-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="35ea9-169">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="35ea9-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="35ea9-170">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="35ea9-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="35ea9-171">Search-Flags</span></span>           | <span data-ttu-id="35ea9-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="35ea9-172">0x00000000</span></span>                                 |
| <span data-ttu-id="35ea9-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="35ea9-173">System-Flags</span></span>           | <span data-ttu-id="35ea9-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="35ea9-174">0x00000010</span></span>                                 |
| <span data-ttu-id="35ea9-175">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="35ea9-175">Classes used in</span></span>        | [<span data-ttu-id="35ea9-176">**Référence croisée**</span><span class="sxs-lookup"><span data-stu-id="35ea9-176">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="adam"></a><span data-ttu-id="35ea9-177">ADAM</span><span class="sxs-lookup"><span data-stu-id="35ea9-177">ADAM</span></span>



| <span data-ttu-id="35ea9-178">Entrée</span><span class="sxs-lookup"><span data-stu-id="35ea9-178">Entry</span></span> | <span data-ttu-id="35ea9-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="35ea9-179">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="35ea9-180">ID de lien</span><span class="sxs-lookup"><span data-stu-id="35ea9-180">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="35ea9-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="35ea9-181">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="35ea9-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="35ea9-182">System-Only</span></span>            | <span data-ttu-id="35ea9-183">Faux</span><span class="sxs-lookup"><span data-stu-id="35ea9-183">False</span></span>                                      |
| <span data-ttu-id="35ea9-184">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="35ea9-184">Is-Single-Valued</span></span>       | <span data-ttu-id="35ea9-185">Vrai</span><span class="sxs-lookup"><span data-stu-id="35ea9-185">True</span></span>                                       |
| <span data-ttu-id="35ea9-186">Est indexé</span><span class="sxs-lookup"><span data-stu-id="35ea9-186">Is Indexed</span></span>             | <span data-ttu-id="35ea9-187">Faux</span><span class="sxs-lookup"><span data-stu-id="35ea9-187">False</span></span>                                      |
| <span data-ttu-id="35ea9-188">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="35ea9-188">In Global Catalog</span></span>      | <span data-ttu-id="35ea9-189">Faux</span><span class="sxs-lookup"><span data-stu-id="35ea9-189">False</span></span>                                      |
| <span data-ttu-id="35ea9-190">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="35ea9-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="35ea9-191">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="35ea9-191">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="35ea9-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="35ea9-192">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="35ea9-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="35ea9-193">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="35ea9-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="35ea9-194">Search-Flags</span></span>           | <span data-ttu-id="35ea9-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="35ea9-195">0x00000000</span></span>                                 |
| <span data-ttu-id="35ea9-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="35ea9-196">System-Flags</span></span>           | <span data-ttu-id="35ea9-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="35ea9-197">0x00000010</span></span>                                 |
| <span data-ttu-id="35ea9-198">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="35ea9-198">Classes used in</span></span>        | [<span data-ttu-id="35ea9-199">**Référence croisée**</span><span class="sxs-lookup"><span data-stu-id="35ea9-199">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="35ea9-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="35ea9-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="35ea9-201">Entrée</span><span class="sxs-lookup"><span data-stu-id="35ea9-201">Entry</span></span> | <span data-ttu-id="35ea9-202">Valeur</span><span class="sxs-lookup"><span data-stu-id="35ea9-202">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="35ea9-203">ID de lien</span><span class="sxs-lookup"><span data-stu-id="35ea9-203">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="35ea9-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="35ea9-204">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="35ea9-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="35ea9-205">System-Only</span></span>            | <span data-ttu-id="35ea9-206">Faux</span><span class="sxs-lookup"><span data-stu-id="35ea9-206">False</span></span>                                      |
| <span data-ttu-id="35ea9-207">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="35ea9-207">Is-Single-Valued</span></span>       | <span data-ttu-id="35ea9-208">Vrai</span><span class="sxs-lookup"><span data-stu-id="35ea9-208">True</span></span>                                       |
| <span data-ttu-id="35ea9-209">Est indexé</span><span class="sxs-lookup"><span data-stu-id="35ea9-209">Is Indexed</span></span>             | <span data-ttu-id="35ea9-210">Faux</span><span class="sxs-lookup"><span data-stu-id="35ea9-210">False</span></span>                                      |
| <span data-ttu-id="35ea9-211">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="35ea9-211">In Global Catalog</span></span>      | <span data-ttu-id="35ea9-212">Faux</span><span class="sxs-lookup"><span data-stu-id="35ea9-212">False</span></span>                                      |
| <span data-ttu-id="35ea9-213">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="35ea9-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="35ea9-214">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="35ea9-214">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="35ea9-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="35ea9-215">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="35ea9-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="35ea9-216">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="35ea9-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="35ea9-217">Search-Flags</span></span>           | <span data-ttu-id="35ea9-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="35ea9-218">0x00000000</span></span>                                 |
| <span data-ttu-id="35ea9-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="35ea9-219">System-Flags</span></span>           | <span data-ttu-id="35ea9-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="35ea9-220">0x00000010</span></span>                                 |
| <span data-ttu-id="35ea9-221">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="35ea9-221">Classes used in</span></span>        | [<span data-ttu-id="35ea9-222">**Référence croisée**</span><span class="sxs-lookup"><span data-stu-id="35ea9-222">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="35ea9-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="35ea9-223">Windows Server 2008</span></span>



| <span data-ttu-id="35ea9-224">Entrée</span><span class="sxs-lookup"><span data-stu-id="35ea9-224">Entry</span></span> | <span data-ttu-id="35ea9-225">Valeur</span><span class="sxs-lookup"><span data-stu-id="35ea9-225">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="35ea9-226">ID de lien</span><span class="sxs-lookup"><span data-stu-id="35ea9-226">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="35ea9-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="35ea9-227">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="35ea9-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="35ea9-228">System-Only</span></span>            | <span data-ttu-id="35ea9-229">Faux</span><span class="sxs-lookup"><span data-stu-id="35ea9-229">False</span></span>                                      |
| <span data-ttu-id="35ea9-230">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="35ea9-230">Is-Single-Valued</span></span>       | <span data-ttu-id="35ea9-231">Vrai</span><span class="sxs-lookup"><span data-stu-id="35ea9-231">True</span></span>                                       |
| <span data-ttu-id="35ea9-232">Est indexé</span><span class="sxs-lookup"><span data-stu-id="35ea9-232">Is Indexed</span></span>             | <span data-ttu-id="35ea9-233">Faux</span><span class="sxs-lookup"><span data-stu-id="35ea9-233">False</span></span>                                      |
| <span data-ttu-id="35ea9-234">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="35ea9-234">In Global Catalog</span></span>      | <span data-ttu-id="35ea9-235">Faux</span><span class="sxs-lookup"><span data-stu-id="35ea9-235">False</span></span>                                      |
| <span data-ttu-id="35ea9-236">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="35ea9-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="35ea9-237">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="35ea9-237">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="35ea9-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="35ea9-238">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="35ea9-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="35ea9-239">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="35ea9-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="35ea9-240">Search-Flags</span></span>           | <span data-ttu-id="35ea9-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="35ea9-241">0x00000000</span></span>                                 |
| <span data-ttu-id="35ea9-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="35ea9-242">System-Flags</span></span>           | <span data-ttu-id="35ea9-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="35ea9-243">0x00000010</span></span>                                 |
| <span data-ttu-id="35ea9-244">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="35ea9-244">Classes used in</span></span>        | [<span data-ttu-id="35ea9-245">**Référence croisée**</span><span class="sxs-lookup"><span data-stu-id="35ea9-245">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="35ea9-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="35ea9-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="35ea9-247">Entrée</span><span class="sxs-lookup"><span data-stu-id="35ea9-247">Entry</span></span> | <span data-ttu-id="35ea9-248">Valeur</span><span class="sxs-lookup"><span data-stu-id="35ea9-248">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="35ea9-249">ID de lien</span><span class="sxs-lookup"><span data-stu-id="35ea9-249">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="35ea9-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="35ea9-250">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="35ea9-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="35ea9-251">System-Only</span></span>            | <span data-ttu-id="35ea9-252">Faux</span><span class="sxs-lookup"><span data-stu-id="35ea9-252">False</span></span>                                      |
| <span data-ttu-id="35ea9-253">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="35ea9-253">Is-Single-Valued</span></span>       | <span data-ttu-id="35ea9-254">Vrai</span><span class="sxs-lookup"><span data-stu-id="35ea9-254">True</span></span>                                       |
| <span data-ttu-id="35ea9-255">Est indexé</span><span class="sxs-lookup"><span data-stu-id="35ea9-255">Is Indexed</span></span>             | <span data-ttu-id="35ea9-256">Faux</span><span class="sxs-lookup"><span data-stu-id="35ea9-256">False</span></span>                                      |
| <span data-ttu-id="35ea9-257">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="35ea9-257">In Global Catalog</span></span>      | <span data-ttu-id="35ea9-258">Faux</span><span class="sxs-lookup"><span data-stu-id="35ea9-258">False</span></span>                                      |
| <span data-ttu-id="35ea9-259">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="35ea9-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="35ea9-260">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="35ea9-260">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="35ea9-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="35ea9-261">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="35ea9-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="35ea9-262">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="35ea9-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="35ea9-263">Search-Flags</span></span>           | <span data-ttu-id="35ea9-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="35ea9-264">0x00000000</span></span>                                 |
| <span data-ttu-id="35ea9-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="35ea9-265">System-Flags</span></span>           | <span data-ttu-id="35ea9-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="35ea9-266">0x00000010</span></span>                                 |
| <span data-ttu-id="35ea9-267">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="35ea9-267">Classes used in</span></span>        | [<span data-ttu-id="35ea9-268">**Référence croisée**</span><span class="sxs-lookup"><span data-stu-id="35ea9-268">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="35ea9-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="35ea9-269">Windows Server 2012</span></span>



| <span data-ttu-id="35ea9-270">Entrée</span><span class="sxs-lookup"><span data-stu-id="35ea9-270">Entry</span></span> | <span data-ttu-id="35ea9-271">Valeur</span><span class="sxs-lookup"><span data-stu-id="35ea9-271">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="35ea9-272">ID de lien</span><span class="sxs-lookup"><span data-stu-id="35ea9-272">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="35ea9-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="35ea9-273">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="35ea9-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="35ea9-274">System-Only</span></span>            | <span data-ttu-id="35ea9-275">Faux</span><span class="sxs-lookup"><span data-stu-id="35ea9-275">False</span></span>                                      |
| <span data-ttu-id="35ea9-276">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="35ea9-276">Is-Single-Valued</span></span>       | <span data-ttu-id="35ea9-277">Vrai</span><span class="sxs-lookup"><span data-stu-id="35ea9-277">True</span></span>                                       |
| <span data-ttu-id="35ea9-278">Est indexé</span><span class="sxs-lookup"><span data-stu-id="35ea9-278">Is Indexed</span></span>             | <span data-ttu-id="35ea9-279">Faux</span><span class="sxs-lookup"><span data-stu-id="35ea9-279">False</span></span>                                      |
| <span data-ttu-id="35ea9-280">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="35ea9-280">In Global Catalog</span></span>      | <span data-ttu-id="35ea9-281">Faux</span><span class="sxs-lookup"><span data-stu-id="35ea9-281">False</span></span>                                      |
| <span data-ttu-id="35ea9-282">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="35ea9-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="35ea9-283">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="35ea9-283">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="35ea9-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="35ea9-284">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="35ea9-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="35ea9-285">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="35ea9-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="35ea9-286">Search-Flags</span></span>           | <span data-ttu-id="35ea9-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="35ea9-287">0x00000000</span></span>                                 |
| <span data-ttu-id="35ea9-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="35ea9-288">System-Flags</span></span>           | <span data-ttu-id="35ea9-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="35ea9-289">0x00000010</span></span>                                 |
| <span data-ttu-id="35ea9-290">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="35ea9-290">Classes used in</span></span>        | [<span data-ttu-id="35ea9-291">**Référence croisée**</span><span class="sxs-lookup"><span data-stu-id="35ea9-291">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



 

 





