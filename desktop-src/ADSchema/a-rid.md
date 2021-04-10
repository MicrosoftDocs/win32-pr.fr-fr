---
title: RID (attribut)
description: Identificateur relatif d’un objet.
ms.assetid: 52110cac-033c-475c-84d7-aff631af3413
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut RID
- Schéma AD de l’attribut RID
topic_type:
- apiref
api_name:
- Rid
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90ab6327fccf804b21a9ba7de6881f98ea4f97be
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103949837"
---
# <a name="rid-attribute"></a><span data-ttu-id="dd4f3-105">RID (attribut)</span><span class="sxs-lookup"><span data-stu-id="dd4f3-105">Rid attribute</span></span>

<span data-ttu-id="dd4f3-106">Identificateur relatif d’un objet.</span><span class="sxs-lookup"><span data-stu-id="dd4f3-106">The relative Identifier of an object.</span></span>



| <span data-ttu-id="dd4f3-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="dd4f3-107">Entry</span></span> | <span data-ttu-id="dd4f3-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="dd4f3-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="dd4f3-109">CN</span><span class="sxs-lookup"><span data-stu-id="dd4f3-109">CN</span></span>                | <span data-ttu-id="dd4f3-110">RID</span><span class="sxs-lookup"><span data-stu-id="dd4f3-110">Rid</span></span>                                         |
| <span data-ttu-id="dd4f3-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="dd4f3-111">Ldap-Display-Name</span></span> | <span data-ttu-id="dd4f3-112">rid</span><span class="sxs-lookup"><span data-stu-id="dd4f3-112">rid</span></span>                                         |
| <span data-ttu-id="dd4f3-113">Taille</span><span class="sxs-lookup"><span data-stu-id="dd4f3-113">Size</span></span>              | <span data-ttu-id="dd4f3-114">4 octets</span><span class="sxs-lookup"><span data-stu-id="dd4f3-114">4 bytes</span></span>                                     |
| <span data-ttu-id="dd4f3-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="dd4f3-115">Update Privilege</span></span>  | <span data-ttu-id="dd4f3-116">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="dd4f3-116">This value is set by the system.</span></span>            |
| <span data-ttu-id="dd4f3-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="dd4f3-117">Update Frequency</span></span>  | <span data-ttu-id="dd4f3-118">Lorsqu’un objet qui a besoin d’un RID est créé.</span><span class="sxs-lookup"><span data-stu-id="dd4f3-118">When an object that needs a RID is created.</span></span> |
| <span data-ttu-id="dd4f3-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="dd4f3-119">Attribute-Id</span></span>      | <span data-ttu-id="dd4f3-120">1.2.840.113556.1.4.153</span><span class="sxs-lookup"><span data-stu-id="dd4f3-120">1.2.840.113556.1.4.153</span></span>                      |
| <span data-ttu-id="dd4f3-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="dd4f3-121">System-Id-Guid</span></span>    | <span data-ttu-id="dd4f3-122">bf967a22-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="dd4f3-122">bf967a22-0de6-11d0-a285-00aa003049e2</span></span>        |
| <span data-ttu-id="dd4f3-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dd4f3-123">Syntax</span></span>            | [<span data-ttu-id="dd4f3-124">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="dd4f3-124">**Enumeration**</span></span>](s-enumeration.md)        |



## <a name="implementations"></a><span data-ttu-id="dd4f3-125">Implémentations</span><span class="sxs-lookup"><span data-stu-id="dd4f3-125">Implementations</span></span>

-   [<span data-ttu-id="dd4f3-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="dd4f3-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="dd4f3-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="dd4f3-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="dd4f3-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="dd4f3-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="dd4f3-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="dd4f3-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="dd4f3-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="dd4f3-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="dd4f3-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="dd4f3-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="dd4f3-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="dd4f3-132">Windows 2000 Server</span></span>



| <span data-ttu-id="dd4f3-133">Entrée</span><span class="sxs-lookup"><span data-stu-id="dd4f3-133">Entry</span></span> | <span data-ttu-id="dd4f3-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="dd4f3-134">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="dd4f3-135">ID de lien</span><span class="sxs-lookup"><span data-stu-id="dd4f3-135">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="dd4f3-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dd4f3-136">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="dd4f3-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="dd4f3-137">System-Only</span></span>            | <span data-ttu-id="dd4f3-138">Faux</span><span class="sxs-lookup"><span data-stu-id="dd4f3-138">False</span></span>                                                        |
| <span data-ttu-id="dd4f3-139">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="dd4f3-139">Is-Single-Valued</span></span>       | <span data-ttu-id="dd4f3-140">Vrai</span><span class="sxs-lookup"><span data-stu-id="dd4f3-140">True</span></span>                                                         |
| <span data-ttu-id="dd4f3-141">Est indexé</span><span class="sxs-lookup"><span data-stu-id="dd4f3-141">Is Indexed</span></span>             | <span data-ttu-id="dd4f3-142">Faux</span><span class="sxs-lookup"><span data-stu-id="dd4f3-142">False</span></span>                                                        |
| <span data-ttu-id="dd4f3-143">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="dd4f3-143">In Global Catalog</span></span>      | <span data-ttu-id="dd4f3-144">Faux</span><span class="sxs-lookup"><span data-stu-id="dd4f3-144">False</span></span>                                                        |
| <span data-ttu-id="dd4f3-145">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="dd4f3-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="dd4f3-146">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="dd4f3-146">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="dd4f3-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dd4f3-147">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="dd4f3-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dd4f3-148">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="dd4f3-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dd4f3-149">Search-Flags</span></span>           | <span data-ttu-id="dd4f3-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dd4f3-150">0x00000000</span></span>                                                   |
| <span data-ttu-id="dd4f3-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dd4f3-151">System-Flags</span></span>           | <span data-ttu-id="dd4f3-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dd4f3-152">0x00000010</span></span>                                                   |
| <span data-ttu-id="dd4f3-153">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="dd4f3-153">Classes used in</span></span>        | [<span data-ttu-id="dd4f3-154">**Sécurité-principal**</span><span class="sxs-lookup"><span data-stu-id="dd4f3-154">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="dd4f3-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="dd4f3-155">Windows Server 2003</span></span>



| <span data-ttu-id="dd4f3-156">Entrée</span><span class="sxs-lookup"><span data-stu-id="dd4f3-156">Entry</span></span> | <span data-ttu-id="dd4f3-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="dd4f3-157">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="dd4f3-158">ID de lien</span><span class="sxs-lookup"><span data-stu-id="dd4f3-158">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="dd4f3-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dd4f3-159">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="dd4f3-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="dd4f3-160">System-Only</span></span>            | <span data-ttu-id="dd4f3-161">Faux</span><span class="sxs-lookup"><span data-stu-id="dd4f3-161">False</span></span>                                                        |
| <span data-ttu-id="dd4f3-162">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="dd4f3-162">Is-Single-Valued</span></span>       | <span data-ttu-id="dd4f3-163">Vrai</span><span class="sxs-lookup"><span data-stu-id="dd4f3-163">True</span></span>                                                         |
| <span data-ttu-id="dd4f3-164">Est indexé</span><span class="sxs-lookup"><span data-stu-id="dd4f3-164">Is Indexed</span></span>             | <span data-ttu-id="dd4f3-165">Faux</span><span class="sxs-lookup"><span data-stu-id="dd4f3-165">False</span></span>                                                        |
| <span data-ttu-id="dd4f3-166">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="dd4f3-166">In Global Catalog</span></span>      | <span data-ttu-id="dd4f3-167">Faux</span><span class="sxs-lookup"><span data-stu-id="dd4f3-167">False</span></span>                                                        |
| <span data-ttu-id="dd4f3-168">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="dd4f3-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="dd4f3-169">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="dd4f3-169">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="dd4f3-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dd4f3-170">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="dd4f3-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dd4f3-171">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="dd4f3-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dd4f3-172">Search-Flags</span></span>           | <span data-ttu-id="dd4f3-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dd4f3-173">0x00000000</span></span>                                                   |
| <span data-ttu-id="dd4f3-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dd4f3-174">System-Flags</span></span>           | <span data-ttu-id="dd4f3-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dd4f3-175">0x00000010</span></span>                                                   |
| <span data-ttu-id="dd4f3-176">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="dd4f3-176">Classes used in</span></span>        | [<span data-ttu-id="dd4f3-177">**Sécurité-principal**</span><span class="sxs-lookup"><span data-stu-id="dd4f3-177">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="dd4f3-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="dd4f3-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="dd4f3-179">Entrée</span><span class="sxs-lookup"><span data-stu-id="dd4f3-179">Entry</span></span> | <span data-ttu-id="dd4f3-180">Valeur</span><span class="sxs-lookup"><span data-stu-id="dd4f3-180">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="dd4f3-181">ID de lien</span><span class="sxs-lookup"><span data-stu-id="dd4f3-181">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="dd4f3-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dd4f3-182">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="dd4f3-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="dd4f3-183">System-Only</span></span>            | <span data-ttu-id="dd4f3-184">Faux</span><span class="sxs-lookup"><span data-stu-id="dd4f3-184">False</span></span>                                                        |
| <span data-ttu-id="dd4f3-185">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="dd4f3-185">Is-Single-Valued</span></span>       | <span data-ttu-id="dd4f3-186">Vrai</span><span class="sxs-lookup"><span data-stu-id="dd4f3-186">True</span></span>                                                         |
| <span data-ttu-id="dd4f3-187">Est indexé</span><span class="sxs-lookup"><span data-stu-id="dd4f3-187">Is Indexed</span></span>             | <span data-ttu-id="dd4f3-188">Faux</span><span class="sxs-lookup"><span data-stu-id="dd4f3-188">False</span></span>                                                        |
| <span data-ttu-id="dd4f3-189">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="dd4f3-189">In Global Catalog</span></span>      | <span data-ttu-id="dd4f3-190">Faux</span><span class="sxs-lookup"><span data-stu-id="dd4f3-190">False</span></span>                                                        |
| <span data-ttu-id="dd4f3-191">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="dd4f3-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="dd4f3-192">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="dd4f3-192">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="dd4f3-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dd4f3-193">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="dd4f3-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dd4f3-194">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="dd4f3-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dd4f3-195">Search-Flags</span></span>           | <span data-ttu-id="dd4f3-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dd4f3-196">0x00000000</span></span>                                                   |
| <span data-ttu-id="dd4f3-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dd4f3-197">System-Flags</span></span>           | <span data-ttu-id="dd4f3-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dd4f3-198">0x00000010</span></span>                                                   |
| <span data-ttu-id="dd4f3-199">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="dd4f3-199">Classes used in</span></span>        | [<span data-ttu-id="dd4f3-200">**Sécurité-principal**</span><span class="sxs-lookup"><span data-stu-id="dd4f3-200">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="dd4f3-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dd4f3-201">Windows Server 2008</span></span>



| <span data-ttu-id="dd4f3-202">Entrée</span><span class="sxs-lookup"><span data-stu-id="dd4f3-202">Entry</span></span> | <span data-ttu-id="dd4f3-203">Valeur</span><span class="sxs-lookup"><span data-stu-id="dd4f3-203">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="dd4f3-204">ID de lien</span><span class="sxs-lookup"><span data-stu-id="dd4f3-204">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="dd4f3-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dd4f3-205">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="dd4f3-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="dd4f3-206">System-Only</span></span>            | <span data-ttu-id="dd4f3-207">Faux</span><span class="sxs-lookup"><span data-stu-id="dd4f3-207">False</span></span>                                                        |
| <span data-ttu-id="dd4f3-208">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="dd4f3-208">Is-Single-Valued</span></span>       | <span data-ttu-id="dd4f3-209">Vrai</span><span class="sxs-lookup"><span data-stu-id="dd4f3-209">True</span></span>                                                         |
| <span data-ttu-id="dd4f3-210">Est indexé</span><span class="sxs-lookup"><span data-stu-id="dd4f3-210">Is Indexed</span></span>             | <span data-ttu-id="dd4f3-211">Faux</span><span class="sxs-lookup"><span data-stu-id="dd4f3-211">False</span></span>                                                        |
| <span data-ttu-id="dd4f3-212">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="dd4f3-212">In Global Catalog</span></span>      | <span data-ttu-id="dd4f3-213">Faux</span><span class="sxs-lookup"><span data-stu-id="dd4f3-213">False</span></span>                                                        |
| <span data-ttu-id="dd4f3-214">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="dd4f3-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="dd4f3-215">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="dd4f3-215">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="dd4f3-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dd4f3-216">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="dd4f3-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dd4f3-217">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="dd4f3-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dd4f3-218">Search-Flags</span></span>           | <span data-ttu-id="dd4f3-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dd4f3-219">0x00000000</span></span>                                                   |
| <span data-ttu-id="dd4f3-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dd4f3-220">System-Flags</span></span>           | <span data-ttu-id="dd4f3-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dd4f3-221">0x00000010</span></span>                                                   |
| <span data-ttu-id="dd4f3-222">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="dd4f3-222">Classes used in</span></span>        | [<span data-ttu-id="dd4f3-223">**Sécurité-principal**</span><span class="sxs-lookup"><span data-stu-id="dd4f3-223">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="dd4f3-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="dd4f3-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="dd4f3-225">Entrée</span><span class="sxs-lookup"><span data-stu-id="dd4f3-225">Entry</span></span> | <span data-ttu-id="dd4f3-226">Valeur</span><span class="sxs-lookup"><span data-stu-id="dd4f3-226">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="dd4f3-227">ID de lien</span><span class="sxs-lookup"><span data-stu-id="dd4f3-227">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="dd4f3-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dd4f3-228">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="dd4f3-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="dd4f3-229">System-Only</span></span>            | <span data-ttu-id="dd4f3-230">Faux</span><span class="sxs-lookup"><span data-stu-id="dd4f3-230">False</span></span>                                                        |
| <span data-ttu-id="dd4f3-231">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="dd4f3-231">Is-Single-Valued</span></span>       | <span data-ttu-id="dd4f3-232">Vrai</span><span class="sxs-lookup"><span data-stu-id="dd4f3-232">True</span></span>                                                         |
| <span data-ttu-id="dd4f3-233">Est indexé</span><span class="sxs-lookup"><span data-stu-id="dd4f3-233">Is Indexed</span></span>             | <span data-ttu-id="dd4f3-234">Faux</span><span class="sxs-lookup"><span data-stu-id="dd4f3-234">False</span></span>                                                        |
| <span data-ttu-id="dd4f3-235">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="dd4f3-235">In Global Catalog</span></span>      | <span data-ttu-id="dd4f3-236">Faux</span><span class="sxs-lookup"><span data-stu-id="dd4f3-236">False</span></span>                                                        |
| <span data-ttu-id="dd4f3-237">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="dd4f3-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="dd4f3-238">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="dd4f3-238">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="dd4f3-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dd4f3-239">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="dd4f3-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dd4f3-240">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="dd4f3-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dd4f3-241">Search-Flags</span></span>           | <span data-ttu-id="dd4f3-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dd4f3-242">0x00000000</span></span>                                                   |
| <span data-ttu-id="dd4f3-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dd4f3-243">System-Flags</span></span>           | <span data-ttu-id="dd4f3-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dd4f3-244">0x00000010</span></span>                                                   |
| <span data-ttu-id="dd4f3-245">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="dd4f3-245">Classes used in</span></span>        | [<span data-ttu-id="dd4f3-246">**Sécurité-principal**</span><span class="sxs-lookup"><span data-stu-id="dd4f3-246">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="dd4f3-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="dd4f3-247">Windows Server 2012</span></span>



| <span data-ttu-id="dd4f3-248">Entrée</span><span class="sxs-lookup"><span data-stu-id="dd4f3-248">Entry</span></span> | <span data-ttu-id="dd4f3-249">Valeur</span><span class="sxs-lookup"><span data-stu-id="dd4f3-249">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="dd4f3-250">ID de lien</span><span class="sxs-lookup"><span data-stu-id="dd4f3-250">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="dd4f3-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dd4f3-251">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="dd4f3-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="dd4f3-252">System-Only</span></span>            | <span data-ttu-id="dd4f3-253">Faux</span><span class="sxs-lookup"><span data-stu-id="dd4f3-253">False</span></span>                                                        |
| <span data-ttu-id="dd4f3-254">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="dd4f3-254">Is-Single-Valued</span></span>       | <span data-ttu-id="dd4f3-255">Vrai</span><span class="sxs-lookup"><span data-stu-id="dd4f3-255">True</span></span>                                                         |
| <span data-ttu-id="dd4f3-256">Est indexé</span><span class="sxs-lookup"><span data-stu-id="dd4f3-256">Is Indexed</span></span>             | <span data-ttu-id="dd4f3-257">Faux</span><span class="sxs-lookup"><span data-stu-id="dd4f3-257">False</span></span>                                                        |
| <span data-ttu-id="dd4f3-258">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="dd4f3-258">In Global Catalog</span></span>      | <span data-ttu-id="dd4f3-259">Faux</span><span class="sxs-lookup"><span data-stu-id="dd4f3-259">False</span></span>                                                        |
| <span data-ttu-id="dd4f3-260">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="dd4f3-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="dd4f3-261">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="dd4f3-261">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="dd4f3-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dd4f3-262">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="dd4f3-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dd4f3-263">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="dd4f3-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dd4f3-264">Search-Flags</span></span>           | <span data-ttu-id="dd4f3-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dd4f3-265">0x00000000</span></span>                                                   |
| <span data-ttu-id="dd4f3-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dd4f3-266">System-Flags</span></span>           | <span data-ttu-id="dd4f3-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dd4f3-267">0x00000010</span></span>                                                   |
| <span data-ttu-id="dd4f3-268">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="dd4f3-268">Classes used in</span></span>        | [<span data-ttu-id="dd4f3-269">**Sécurité-principal**</span><span class="sxs-lookup"><span data-stu-id="dd4f3-269">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



 

 





