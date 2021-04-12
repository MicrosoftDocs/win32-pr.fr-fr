---
title: Attribut Flat-Name
description: Pour les domaines Windows NT, le nom plat est le nom NetBIOS. Pour les liens avec non-\ 8211 ; Domaines Windows NT, le nom plat est le nom d’identification de ce domaine, ou il a la valeur NULL.
ms.assetid: ec368657-a0e7-4416-ab80-1d18d98bbcfa
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Flat-Name
- Schéma AD de l’attribut flatName
topic_type:
- apiref
api_name:
- Flat-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 373ee0736c051932fdb6dd20701f0c5ec353ad3b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104479789"
---
# <a name="flat-name-attribute"></a><span data-ttu-id="b4f50-106">Attribut Flat-Name</span><span class="sxs-lookup"><span data-stu-id="b4f50-106">Flat-Name attribute</span></span>

<span data-ttu-id="b4f50-107">Pour les domaines Windows NT, le nom plat est le nom NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="b4f50-107">For Windows NT domains, the flat name is the NetBIOS name.</span></span> <span data-ttu-id="b4f50-108">Pour les liens avec des domaines non Windows NT, le nom plat est le nom d’identification de ce domaine, ou il a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="b4f50-108">For links with non Windows NT domains, the flat name is the identifying name of that domain, or it is **NULL**.</span></span>



| <span data-ttu-id="b4f50-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="b4f50-109">Entry</span></span> | <span data-ttu-id="b4f50-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4f50-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="b4f50-111">CN</span><span class="sxs-lookup"><span data-stu-id="b4f50-111">CN</span></span>                | <span data-ttu-id="b4f50-112">Flat-Name</span><span class="sxs-lookup"><span data-stu-id="b4f50-112">Flat-Name</span></span>                                   |
| <span data-ttu-id="b4f50-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="b4f50-113">Ldap-Display-Name</span></span> | <span data-ttu-id="b4f50-114">flatName</span><span class="sxs-lookup"><span data-stu-id="b4f50-114">flatName</span></span>                                    |
| <span data-ttu-id="b4f50-115">Taille</span><span class="sxs-lookup"><span data-stu-id="b4f50-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="b4f50-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="b4f50-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="b4f50-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="b4f50-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="b4f50-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b4f50-118">Attribute-Id</span></span>      | <span data-ttu-id="b4f50-119">1.2.840.113556.1.4.511</span><span class="sxs-lookup"><span data-stu-id="b4f50-119">1.2.840.113556.1.4.511</span></span>                      |
| <span data-ttu-id="b4f50-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b4f50-120">System-Id-Guid</span></span>    | <span data-ttu-id="b4f50-121">b7b13117-b82e-11d0-afee-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="b4f50-121">b7b13117-b82e-11d0-afee-0000f80367c1</span></span>        |
| <span data-ttu-id="b4f50-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b4f50-122">Syntax</span></span>            | [<span data-ttu-id="b4f50-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="b4f50-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="b4f50-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="b4f50-124">Implementations</span></span>

-   [<span data-ttu-id="b4f50-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b4f50-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b4f50-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b4f50-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b4f50-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b4f50-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b4f50-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b4f50-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b4f50-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b4f50-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b4f50-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b4f50-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b4f50-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b4f50-131">Windows 2000 Server</span></span>



| <span data-ttu-id="b4f50-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="b4f50-132">Entry</span></span> | <span data-ttu-id="b4f50-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4f50-133">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="b4f50-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b4f50-134">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b4f50-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4f50-135">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b4f50-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4f50-136">System-Only</span></span>            | <span data-ttu-id="b4f50-137">Faux</span><span class="sxs-lookup"><span data-stu-id="b4f50-137">False</span></span>                                                |
| <span data-ttu-id="b4f50-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b4f50-138">Is-Single-Valued</span></span>       | <span data-ttu-id="b4f50-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="b4f50-139">True</span></span>                                                 |
| <span data-ttu-id="b4f50-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b4f50-140">Is Indexed</span></span>             | <span data-ttu-id="b4f50-141">Vrai</span><span class="sxs-lookup"><span data-stu-id="b4f50-141">True</span></span>                                                 |
| <span data-ttu-id="b4f50-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b4f50-142">In Global Catalog</span></span>      | <span data-ttu-id="b4f50-143">Faux</span><span class="sxs-lookup"><span data-stu-id="b4f50-143">False</span></span>                                                |
| <span data-ttu-id="b4f50-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b4f50-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4f50-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b4f50-145">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="b4f50-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4f50-146">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="b4f50-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4f50-147">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="b4f50-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4f50-148">Search-Flags</span></span>           | <span data-ttu-id="b4f50-149">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b4f50-149">0x00000001</span></span>                                           |
| <span data-ttu-id="b4f50-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4f50-150">System-Flags</span></span>           | <span data-ttu-id="b4f50-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b4f50-151">0x00000010</span></span>                                           |
| <span data-ttu-id="b4f50-152">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b4f50-152">Classes used in</span></span>        | [<span data-ttu-id="b4f50-153">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="b4f50-153">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b4f50-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b4f50-154">Windows Server 2003</span></span>



| <span data-ttu-id="b4f50-155">Entrée</span><span class="sxs-lookup"><span data-stu-id="b4f50-155">Entry</span></span> | <span data-ttu-id="b4f50-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4f50-156">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="b4f50-157">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b4f50-157">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b4f50-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4f50-158">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b4f50-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4f50-159">System-Only</span></span>            | <span data-ttu-id="b4f50-160">Faux</span><span class="sxs-lookup"><span data-stu-id="b4f50-160">False</span></span>                                                |
| <span data-ttu-id="b4f50-161">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b4f50-161">Is-Single-Valued</span></span>       | <span data-ttu-id="b4f50-162">Vrai</span><span class="sxs-lookup"><span data-stu-id="b4f50-162">True</span></span>                                                 |
| <span data-ttu-id="b4f50-163">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b4f50-163">Is Indexed</span></span>             | <span data-ttu-id="b4f50-164">Vrai</span><span class="sxs-lookup"><span data-stu-id="b4f50-164">True</span></span>                                                 |
| <span data-ttu-id="b4f50-165">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b4f50-165">In Global Catalog</span></span>      | <span data-ttu-id="b4f50-166">Faux</span><span class="sxs-lookup"><span data-stu-id="b4f50-166">False</span></span>                                                |
| <span data-ttu-id="b4f50-167">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b4f50-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4f50-168">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b4f50-168">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="b4f50-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4f50-169">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="b4f50-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4f50-170">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="b4f50-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4f50-171">Search-Flags</span></span>           | <span data-ttu-id="b4f50-172">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b4f50-172">0x00000001</span></span>                                           |
| <span data-ttu-id="b4f50-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4f50-173">System-Flags</span></span>           | <span data-ttu-id="b4f50-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b4f50-174">0x00000010</span></span>                                           |
| <span data-ttu-id="b4f50-175">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b4f50-175">Classes used in</span></span>        | [<span data-ttu-id="b4f50-176">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="b4f50-176">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b4f50-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b4f50-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b4f50-178">Entrée</span><span class="sxs-lookup"><span data-stu-id="b4f50-178">Entry</span></span> | <span data-ttu-id="b4f50-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4f50-179">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="b4f50-180">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b4f50-180">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b4f50-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4f50-181">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b4f50-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4f50-182">System-Only</span></span>            | <span data-ttu-id="b4f50-183">Faux</span><span class="sxs-lookup"><span data-stu-id="b4f50-183">False</span></span>                                                |
| <span data-ttu-id="b4f50-184">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b4f50-184">Is-Single-Valued</span></span>       | <span data-ttu-id="b4f50-185">Vrai</span><span class="sxs-lookup"><span data-stu-id="b4f50-185">True</span></span>                                                 |
| <span data-ttu-id="b4f50-186">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b4f50-186">Is Indexed</span></span>             | <span data-ttu-id="b4f50-187">Vrai</span><span class="sxs-lookup"><span data-stu-id="b4f50-187">True</span></span>                                                 |
| <span data-ttu-id="b4f50-188">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b4f50-188">In Global Catalog</span></span>      | <span data-ttu-id="b4f50-189">Faux</span><span class="sxs-lookup"><span data-stu-id="b4f50-189">False</span></span>                                                |
| <span data-ttu-id="b4f50-190">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b4f50-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4f50-191">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b4f50-191">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="b4f50-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4f50-192">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="b4f50-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4f50-193">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="b4f50-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4f50-194">Search-Flags</span></span>           | <span data-ttu-id="b4f50-195">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b4f50-195">0x00000001</span></span>                                           |
| <span data-ttu-id="b4f50-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4f50-196">System-Flags</span></span>           | <span data-ttu-id="b4f50-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b4f50-197">0x00000010</span></span>                                           |
| <span data-ttu-id="b4f50-198">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b4f50-198">Classes used in</span></span>        | [<span data-ttu-id="b4f50-199">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="b4f50-199">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b4f50-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b4f50-200">Windows Server 2008</span></span>



| <span data-ttu-id="b4f50-201">Entrée</span><span class="sxs-lookup"><span data-stu-id="b4f50-201">Entry</span></span> | <span data-ttu-id="b4f50-202">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4f50-202">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="b4f50-203">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b4f50-203">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b4f50-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4f50-204">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b4f50-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4f50-205">System-Only</span></span>            | <span data-ttu-id="b4f50-206">Faux</span><span class="sxs-lookup"><span data-stu-id="b4f50-206">False</span></span>                                                |
| <span data-ttu-id="b4f50-207">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b4f50-207">Is-Single-Valued</span></span>       | <span data-ttu-id="b4f50-208">Vrai</span><span class="sxs-lookup"><span data-stu-id="b4f50-208">True</span></span>                                                 |
| <span data-ttu-id="b4f50-209">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b4f50-209">Is Indexed</span></span>             | <span data-ttu-id="b4f50-210">Vrai</span><span class="sxs-lookup"><span data-stu-id="b4f50-210">True</span></span>                                                 |
| <span data-ttu-id="b4f50-211">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b4f50-211">In Global Catalog</span></span>      | <span data-ttu-id="b4f50-212">Faux</span><span class="sxs-lookup"><span data-stu-id="b4f50-212">False</span></span>                                                |
| <span data-ttu-id="b4f50-213">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b4f50-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4f50-214">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b4f50-214">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="b4f50-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4f50-215">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="b4f50-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4f50-216">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="b4f50-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4f50-217">Search-Flags</span></span>           | <span data-ttu-id="b4f50-218">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b4f50-218">0x00000001</span></span>                                           |
| <span data-ttu-id="b4f50-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4f50-219">System-Flags</span></span>           | <span data-ttu-id="b4f50-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b4f50-220">0x00000010</span></span>                                           |
| <span data-ttu-id="b4f50-221">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b4f50-221">Classes used in</span></span>        | [<span data-ttu-id="b4f50-222">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="b4f50-222">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b4f50-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b4f50-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b4f50-224">Entrée</span><span class="sxs-lookup"><span data-stu-id="b4f50-224">Entry</span></span> | <span data-ttu-id="b4f50-225">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4f50-225">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="b4f50-226">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b4f50-226">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b4f50-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4f50-227">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b4f50-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4f50-228">System-Only</span></span>            | <span data-ttu-id="b4f50-229">Faux</span><span class="sxs-lookup"><span data-stu-id="b4f50-229">False</span></span>                                                |
| <span data-ttu-id="b4f50-230">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b4f50-230">Is-Single-Valued</span></span>       | <span data-ttu-id="b4f50-231">Vrai</span><span class="sxs-lookup"><span data-stu-id="b4f50-231">True</span></span>                                                 |
| <span data-ttu-id="b4f50-232">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b4f50-232">Is Indexed</span></span>             | <span data-ttu-id="b4f50-233">Vrai</span><span class="sxs-lookup"><span data-stu-id="b4f50-233">True</span></span>                                                 |
| <span data-ttu-id="b4f50-234">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b4f50-234">In Global Catalog</span></span>      | <span data-ttu-id="b4f50-235">Faux</span><span class="sxs-lookup"><span data-stu-id="b4f50-235">False</span></span>                                                |
| <span data-ttu-id="b4f50-236">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b4f50-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4f50-237">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b4f50-237">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="b4f50-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4f50-238">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="b4f50-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4f50-239">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="b4f50-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4f50-240">Search-Flags</span></span>           | <span data-ttu-id="b4f50-241">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b4f50-241">0x00000001</span></span>                                           |
| <span data-ttu-id="b4f50-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4f50-242">System-Flags</span></span>           | <span data-ttu-id="b4f50-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b4f50-243">0x00000010</span></span>                                           |
| <span data-ttu-id="b4f50-244">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b4f50-244">Classes used in</span></span>        | [<span data-ttu-id="b4f50-245">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="b4f50-245">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b4f50-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b4f50-246">Windows Server 2012</span></span>



| <span data-ttu-id="b4f50-247">Entrée</span><span class="sxs-lookup"><span data-stu-id="b4f50-247">Entry</span></span> | <span data-ttu-id="b4f50-248">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4f50-248">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="b4f50-249">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b4f50-249">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b4f50-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4f50-250">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b4f50-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4f50-251">System-Only</span></span>            | <span data-ttu-id="b4f50-252">Faux</span><span class="sxs-lookup"><span data-stu-id="b4f50-252">False</span></span>                                                |
| <span data-ttu-id="b4f50-253">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b4f50-253">Is-Single-Valued</span></span>       | <span data-ttu-id="b4f50-254">Vrai</span><span class="sxs-lookup"><span data-stu-id="b4f50-254">True</span></span>                                                 |
| <span data-ttu-id="b4f50-255">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b4f50-255">Is Indexed</span></span>             | <span data-ttu-id="b4f50-256">Vrai</span><span class="sxs-lookup"><span data-stu-id="b4f50-256">True</span></span>                                                 |
| <span data-ttu-id="b4f50-257">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b4f50-257">In Global Catalog</span></span>      | <span data-ttu-id="b4f50-258">Faux</span><span class="sxs-lookup"><span data-stu-id="b4f50-258">False</span></span>                                                |
| <span data-ttu-id="b4f50-259">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b4f50-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4f50-260">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b4f50-260">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="b4f50-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4f50-261">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="b4f50-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4f50-262">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="b4f50-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4f50-263">Search-Flags</span></span>           | <span data-ttu-id="b4f50-264">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b4f50-264">0x00000001</span></span>                                           |
| <span data-ttu-id="b4f50-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4f50-265">System-Flags</span></span>           | <span data-ttu-id="b4f50-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b4f50-266">0x00000010</span></span>                                           |
| <span data-ttu-id="b4f50-267">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b4f50-267">Classes used in</span></span>        | [<span data-ttu-id="b4f50-268">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="b4f50-268">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





