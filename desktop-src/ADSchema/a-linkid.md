---
title: Attribut de l’ID de lien
description: Entier qui indique que l’attribut est un attribut lié. Un entier pair est un lien suivant et un entier impair est un lien vers l’arrière.
ms.assetid: 73851839-f70c-40c6-976c-0bf727083791
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory de l’attribut Link-ID
- Schéma AD de l’attribut linkID
topic_type:
- apiref
api_name:
- Link-ID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a64ad1d26ce5510ac5643419ade46d0565df6487
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104519905"
---
# <a name="link-id-attribute"></a><span data-ttu-id="ef8e0-106">Attribut de l’ID de lien</span><span class="sxs-lookup"><span data-stu-id="ef8e0-106">Link-ID attribute</span></span>

<span data-ttu-id="ef8e0-107">Entier qui indique que l’attribut est un attribut lié.</span><span class="sxs-lookup"><span data-stu-id="ef8e0-107">An integer that indicates that the attribute is a linked attribute.</span></span> <span data-ttu-id="ef8e0-108">Un entier pair est un lien suivant et un entier impair est un lien vers l’arrière.</span><span class="sxs-lookup"><span data-stu-id="ef8e0-108">An even integer is a forward link and an odd integer is a backward link.</span></span>



| <span data-ttu-id="ef8e0-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="ef8e0-109">Entry</span></span> | <span data-ttu-id="ef8e0-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef8e0-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="ef8e0-111">CN</span><span class="sxs-lookup"><span data-stu-id="ef8e0-111">CN</span></span>                | <span data-ttu-id="ef8e0-112">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ef8e0-112">Link-ID</span></span>                              |
| <span data-ttu-id="ef8e0-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="ef8e0-113">Ldap-Display-Name</span></span> | <span data-ttu-id="ef8e0-114">Égale</span><span class="sxs-lookup"><span data-stu-id="ef8e0-114">linkID</span></span>                               |
| <span data-ttu-id="ef8e0-115">Taille</span><span class="sxs-lookup"><span data-stu-id="ef8e0-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="ef8e0-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="ef8e0-116">Update Privilege</span></span>  | <span data-ttu-id="ef8e0-117">Administrateur de schéma</span><span class="sxs-lookup"><span data-stu-id="ef8e0-117">Schema administrator</span></span>                 |
| <span data-ttu-id="ef8e0-118">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="ef8e0-118">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="ef8e0-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ef8e0-119">Attribute-Id</span></span>      | <span data-ttu-id="ef8e0-120">1.2.840.113556.1.2.50</span><span class="sxs-lookup"><span data-stu-id="ef8e0-120">1.2.840.113556.1.2.50</span></span>                |
| <span data-ttu-id="ef8e0-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ef8e0-121">System-Id-Guid</span></span>    | <span data-ttu-id="ef8e0-122">bf96799b-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="ef8e0-122">bf96799b-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="ef8e0-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ef8e0-123">Syntax</span></span>            | [<span data-ttu-id="ef8e0-124">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="ef8e0-124">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="ef8e0-125">Implémentations</span><span class="sxs-lookup"><span data-stu-id="ef8e0-125">Implementations</span></span>

-   [<span data-ttu-id="ef8e0-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ef8e0-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ef8e0-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ef8e0-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ef8e0-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="ef8e0-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="ef8e0-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ef8e0-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ef8e0-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ef8e0-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ef8e0-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ef8e0-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ef8e0-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ef8e0-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ef8e0-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ef8e0-133">Windows 2000 Server</span></span>



| <span data-ttu-id="ef8e0-134">Entrée</span><span class="sxs-lookup"><span data-stu-id="ef8e0-134">Entry</span></span> | <span data-ttu-id="ef8e0-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef8e0-135">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="ef8e0-136">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ef8e0-136">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="ef8e0-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ef8e0-137">MAPI-Id</span></span>                | <span data-ttu-id="ef8e0-138">0x80C5</span><span class="sxs-lookup"><span data-stu-id="ef8e0-138">0x80C5</span></span>                                                   |
| <span data-ttu-id="ef8e0-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="ef8e0-139">System-Only</span></span>            | <span data-ttu-id="ef8e0-140">Vrai</span><span class="sxs-lookup"><span data-stu-id="ef8e0-140">True</span></span>                                                     |
| <span data-ttu-id="ef8e0-141">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ef8e0-141">Is-Single-Valued</span></span>       | <span data-ttu-id="ef8e0-142">Vrai</span><span class="sxs-lookup"><span data-stu-id="ef8e0-142">True</span></span>                                                     |
| <span data-ttu-id="ef8e0-143">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ef8e0-143">Is Indexed</span></span>             | <span data-ttu-id="ef8e0-144">Faux</span><span class="sxs-lookup"><span data-stu-id="ef8e0-144">False</span></span>                                                    |
| <span data-ttu-id="ef8e0-145">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ef8e0-145">In Global Catalog</span></span>      | <span data-ttu-id="ef8e0-146">Faux</span><span class="sxs-lookup"><span data-stu-id="ef8e0-146">False</span></span>                                                    |
| <span data-ttu-id="ef8e0-147">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ef8e0-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="ef8e0-148">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ef8e0-148">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="ef8e0-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ef8e0-149">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="ef8e0-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ef8e0-150">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="ef8e0-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ef8e0-151">Search-Flags</span></span>           | <span data-ttu-id="ef8e0-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ef8e0-152">0x00000000</span></span>                                               |
| <span data-ttu-id="ef8e0-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ef8e0-153">System-Flags</span></span>           | <span data-ttu-id="ef8e0-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ef8e0-154">0x00000010</span></span>                                               |
| <span data-ttu-id="ef8e0-155">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ef8e0-155">Classes used in</span></span>        | [<span data-ttu-id="ef8e0-156">**Attribut-schéma**</span><span class="sxs-lookup"><span data-stu-id="ef8e0-156">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ef8e0-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ef8e0-157">Windows Server 2003</span></span>



| <span data-ttu-id="ef8e0-158">Entrée</span><span class="sxs-lookup"><span data-stu-id="ef8e0-158">Entry</span></span> | <span data-ttu-id="ef8e0-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef8e0-159">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="ef8e0-160">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ef8e0-160">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="ef8e0-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ef8e0-161">MAPI-Id</span></span>                | <span data-ttu-id="ef8e0-162">0x80C5</span><span class="sxs-lookup"><span data-stu-id="ef8e0-162">0x80C5</span></span>                                                   |
| <span data-ttu-id="ef8e0-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="ef8e0-163">System-Only</span></span>            | <span data-ttu-id="ef8e0-164">Vrai</span><span class="sxs-lookup"><span data-stu-id="ef8e0-164">True</span></span>                                                     |
| <span data-ttu-id="ef8e0-165">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ef8e0-165">Is-Single-Valued</span></span>       | <span data-ttu-id="ef8e0-166">Vrai</span><span class="sxs-lookup"><span data-stu-id="ef8e0-166">True</span></span>                                                     |
| <span data-ttu-id="ef8e0-167">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ef8e0-167">Is Indexed</span></span>             | <span data-ttu-id="ef8e0-168">Faux</span><span class="sxs-lookup"><span data-stu-id="ef8e0-168">False</span></span>                                                    |
| <span data-ttu-id="ef8e0-169">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ef8e0-169">In Global Catalog</span></span>      | <span data-ttu-id="ef8e0-170">Faux</span><span class="sxs-lookup"><span data-stu-id="ef8e0-170">False</span></span>                                                    |
| <span data-ttu-id="ef8e0-171">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ef8e0-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="ef8e0-172">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ef8e0-172">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="ef8e0-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ef8e0-173">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="ef8e0-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ef8e0-174">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="ef8e0-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ef8e0-175">Search-Flags</span></span>           | <span data-ttu-id="ef8e0-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ef8e0-176">0x00000000</span></span>                                               |
| <span data-ttu-id="ef8e0-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ef8e0-177">System-Flags</span></span>           | <span data-ttu-id="ef8e0-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ef8e0-178">0x00000010</span></span>                                               |
| <span data-ttu-id="ef8e0-179">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ef8e0-179">Classes used in</span></span>        | [<span data-ttu-id="ef8e0-180">**Attribut-schéma**</span><span class="sxs-lookup"><span data-stu-id="ef8e0-180">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="ef8e0-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="ef8e0-181">ADAM</span></span>



| <span data-ttu-id="ef8e0-182">Entrée</span><span class="sxs-lookup"><span data-stu-id="ef8e0-182">Entry</span></span> | <span data-ttu-id="ef8e0-183">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef8e0-183">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="ef8e0-184">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ef8e0-184">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="ef8e0-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ef8e0-185">MAPI-Id</span></span>                | <span data-ttu-id="ef8e0-186">0x80C5</span><span class="sxs-lookup"><span data-stu-id="ef8e0-186">0x80C5</span></span>                                                   |
| <span data-ttu-id="ef8e0-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="ef8e0-187">System-Only</span></span>            | <span data-ttu-id="ef8e0-188">Vrai</span><span class="sxs-lookup"><span data-stu-id="ef8e0-188">True</span></span>                                                     |
| <span data-ttu-id="ef8e0-189">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ef8e0-189">Is-Single-Valued</span></span>       | <span data-ttu-id="ef8e0-190">Vrai</span><span class="sxs-lookup"><span data-stu-id="ef8e0-190">True</span></span>                                                     |
| <span data-ttu-id="ef8e0-191">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ef8e0-191">Is Indexed</span></span>             | <span data-ttu-id="ef8e0-192">Faux</span><span class="sxs-lookup"><span data-stu-id="ef8e0-192">False</span></span>                                                    |
| <span data-ttu-id="ef8e0-193">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ef8e0-193">In Global Catalog</span></span>      | <span data-ttu-id="ef8e0-194">Faux</span><span class="sxs-lookup"><span data-stu-id="ef8e0-194">False</span></span>                                                    |
| <span data-ttu-id="ef8e0-195">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ef8e0-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="ef8e0-196">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ef8e0-196">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="ef8e0-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ef8e0-197">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="ef8e0-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ef8e0-198">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="ef8e0-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ef8e0-199">Search-Flags</span></span>           | <span data-ttu-id="ef8e0-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ef8e0-200">0x00000000</span></span>                                               |
| <span data-ttu-id="ef8e0-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ef8e0-201">System-Flags</span></span>           | <span data-ttu-id="ef8e0-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ef8e0-202">0x00000010</span></span>                                               |
| <span data-ttu-id="ef8e0-203">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ef8e0-203">Classes used in</span></span>        | [<span data-ttu-id="ef8e0-204">**Attribut-schéma**</span><span class="sxs-lookup"><span data-stu-id="ef8e0-204">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ef8e0-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ef8e0-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ef8e0-206">Entrée</span><span class="sxs-lookup"><span data-stu-id="ef8e0-206">Entry</span></span> | <span data-ttu-id="ef8e0-207">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef8e0-207">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="ef8e0-208">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ef8e0-208">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="ef8e0-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ef8e0-209">MAPI-Id</span></span>                | <span data-ttu-id="ef8e0-210">0x80C5</span><span class="sxs-lookup"><span data-stu-id="ef8e0-210">0x80C5</span></span>                                                   |
| <span data-ttu-id="ef8e0-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="ef8e0-211">System-Only</span></span>            | <span data-ttu-id="ef8e0-212">Vrai</span><span class="sxs-lookup"><span data-stu-id="ef8e0-212">True</span></span>                                                     |
| <span data-ttu-id="ef8e0-213">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ef8e0-213">Is-Single-Valued</span></span>       | <span data-ttu-id="ef8e0-214">Vrai</span><span class="sxs-lookup"><span data-stu-id="ef8e0-214">True</span></span>                                                     |
| <span data-ttu-id="ef8e0-215">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ef8e0-215">Is Indexed</span></span>             | <span data-ttu-id="ef8e0-216">Faux</span><span class="sxs-lookup"><span data-stu-id="ef8e0-216">False</span></span>                                                    |
| <span data-ttu-id="ef8e0-217">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ef8e0-217">In Global Catalog</span></span>      | <span data-ttu-id="ef8e0-218">Faux</span><span class="sxs-lookup"><span data-stu-id="ef8e0-218">False</span></span>                                                    |
| <span data-ttu-id="ef8e0-219">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ef8e0-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="ef8e0-220">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ef8e0-220">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="ef8e0-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ef8e0-221">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="ef8e0-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ef8e0-222">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="ef8e0-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ef8e0-223">Search-Flags</span></span>           | <span data-ttu-id="ef8e0-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ef8e0-224">0x00000000</span></span>                                               |
| <span data-ttu-id="ef8e0-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ef8e0-225">System-Flags</span></span>           | <span data-ttu-id="ef8e0-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ef8e0-226">0x00000010</span></span>                                               |
| <span data-ttu-id="ef8e0-227">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ef8e0-227">Classes used in</span></span>        | [<span data-ttu-id="ef8e0-228">**Attribut-schéma**</span><span class="sxs-lookup"><span data-stu-id="ef8e0-228">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ef8e0-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ef8e0-229">Windows Server 2008</span></span>



| <span data-ttu-id="ef8e0-230">Entrée</span><span class="sxs-lookup"><span data-stu-id="ef8e0-230">Entry</span></span> | <span data-ttu-id="ef8e0-231">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef8e0-231">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="ef8e0-232">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ef8e0-232">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="ef8e0-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ef8e0-233">MAPI-Id</span></span>                | <span data-ttu-id="ef8e0-234">0x80C5</span><span class="sxs-lookup"><span data-stu-id="ef8e0-234">0x80C5</span></span>                                                   |
| <span data-ttu-id="ef8e0-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="ef8e0-235">System-Only</span></span>            | <span data-ttu-id="ef8e0-236">Vrai</span><span class="sxs-lookup"><span data-stu-id="ef8e0-236">True</span></span>                                                     |
| <span data-ttu-id="ef8e0-237">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ef8e0-237">Is-Single-Valued</span></span>       | <span data-ttu-id="ef8e0-238">Vrai</span><span class="sxs-lookup"><span data-stu-id="ef8e0-238">True</span></span>                                                     |
| <span data-ttu-id="ef8e0-239">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ef8e0-239">Is Indexed</span></span>             | <span data-ttu-id="ef8e0-240">Faux</span><span class="sxs-lookup"><span data-stu-id="ef8e0-240">False</span></span>                                                    |
| <span data-ttu-id="ef8e0-241">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ef8e0-241">In Global Catalog</span></span>      | <span data-ttu-id="ef8e0-242">Faux</span><span class="sxs-lookup"><span data-stu-id="ef8e0-242">False</span></span>                                                    |
| <span data-ttu-id="ef8e0-243">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ef8e0-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="ef8e0-244">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ef8e0-244">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="ef8e0-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ef8e0-245">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="ef8e0-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ef8e0-246">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="ef8e0-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ef8e0-247">Search-Flags</span></span>           | <span data-ttu-id="ef8e0-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ef8e0-248">0x00000000</span></span>                                               |
| <span data-ttu-id="ef8e0-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ef8e0-249">System-Flags</span></span>           | <span data-ttu-id="ef8e0-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ef8e0-250">0x00000010</span></span>                                               |
| <span data-ttu-id="ef8e0-251">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ef8e0-251">Classes used in</span></span>        | [<span data-ttu-id="ef8e0-252">**Attribut-schéma**</span><span class="sxs-lookup"><span data-stu-id="ef8e0-252">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ef8e0-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ef8e0-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ef8e0-254">Entrée</span><span class="sxs-lookup"><span data-stu-id="ef8e0-254">Entry</span></span> | <span data-ttu-id="ef8e0-255">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef8e0-255">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="ef8e0-256">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ef8e0-256">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="ef8e0-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ef8e0-257">MAPI-Id</span></span>                | <span data-ttu-id="ef8e0-258">0x80C5</span><span class="sxs-lookup"><span data-stu-id="ef8e0-258">0x80C5</span></span>                                                   |
| <span data-ttu-id="ef8e0-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="ef8e0-259">System-Only</span></span>            | <span data-ttu-id="ef8e0-260">Vrai</span><span class="sxs-lookup"><span data-stu-id="ef8e0-260">True</span></span>                                                     |
| <span data-ttu-id="ef8e0-261">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ef8e0-261">Is-Single-Valued</span></span>       | <span data-ttu-id="ef8e0-262">Vrai</span><span class="sxs-lookup"><span data-stu-id="ef8e0-262">True</span></span>                                                     |
| <span data-ttu-id="ef8e0-263">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ef8e0-263">Is Indexed</span></span>             | <span data-ttu-id="ef8e0-264">Faux</span><span class="sxs-lookup"><span data-stu-id="ef8e0-264">False</span></span>                                                    |
| <span data-ttu-id="ef8e0-265">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ef8e0-265">In Global Catalog</span></span>      | <span data-ttu-id="ef8e0-266">Faux</span><span class="sxs-lookup"><span data-stu-id="ef8e0-266">False</span></span>                                                    |
| <span data-ttu-id="ef8e0-267">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ef8e0-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="ef8e0-268">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ef8e0-268">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="ef8e0-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ef8e0-269">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="ef8e0-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ef8e0-270">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="ef8e0-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ef8e0-271">Search-Flags</span></span>           | <span data-ttu-id="ef8e0-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ef8e0-272">0x00000000</span></span>                                               |
| <span data-ttu-id="ef8e0-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ef8e0-273">System-Flags</span></span>           | <span data-ttu-id="ef8e0-274">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ef8e0-274">0x00000010</span></span>                                               |
| <span data-ttu-id="ef8e0-275">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ef8e0-275">Classes used in</span></span>        | [<span data-ttu-id="ef8e0-276">**Attribut-schéma**</span><span class="sxs-lookup"><span data-stu-id="ef8e0-276">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ef8e0-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ef8e0-277">Windows Server 2012</span></span>



| <span data-ttu-id="ef8e0-278">Entrée</span><span class="sxs-lookup"><span data-stu-id="ef8e0-278">Entry</span></span> | <span data-ttu-id="ef8e0-279">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef8e0-279">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="ef8e0-280">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ef8e0-280">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="ef8e0-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ef8e0-281">MAPI-Id</span></span>                | <span data-ttu-id="ef8e0-282">0x80C5</span><span class="sxs-lookup"><span data-stu-id="ef8e0-282">0x80C5</span></span>                                                   |
| <span data-ttu-id="ef8e0-283">System-Only</span><span class="sxs-lookup"><span data-stu-id="ef8e0-283">System-Only</span></span>            | <span data-ttu-id="ef8e0-284">Vrai</span><span class="sxs-lookup"><span data-stu-id="ef8e0-284">True</span></span>                                                     |
| <span data-ttu-id="ef8e0-285">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ef8e0-285">Is-Single-Valued</span></span>       | <span data-ttu-id="ef8e0-286">Vrai</span><span class="sxs-lookup"><span data-stu-id="ef8e0-286">True</span></span>                                                     |
| <span data-ttu-id="ef8e0-287">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ef8e0-287">Is Indexed</span></span>             | <span data-ttu-id="ef8e0-288">Faux</span><span class="sxs-lookup"><span data-stu-id="ef8e0-288">False</span></span>                                                    |
| <span data-ttu-id="ef8e0-289">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ef8e0-289">In Global Catalog</span></span>      | <span data-ttu-id="ef8e0-290">Faux</span><span class="sxs-lookup"><span data-stu-id="ef8e0-290">False</span></span>                                                    |
| <span data-ttu-id="ef8e0-291">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ef8e0-291">NT-Security-Descriptor</span></span> | <span data-ttu-id="ef8e0-292">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ef8e0-292">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="ef8e0-293">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ef8e0-293">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="ef8e0-294">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ef8e0-294">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="ef8e0-295">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ef8e0-295">Search-Flags</span></span>           | <span data-ttu-id="ef8e0-296">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ef8e0-296">0x00000000</span></span>                                               |
| <span data-ttu-id="ef8e0-297">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ef8e0-297">System-Flags</span></span>           | <span data-ttu-id="ef8e0-298">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ef8e0-298">0x00000010</span></span>                                               |
| <span data-ttu-id="ef8e0-299">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ef8e0-299">Classes used in</span></span>        | [<span data-ttu-id="ef8e0-300">**Attribut-schéma**</span><span class="sxs-lookup"><span data-stu-id="ef8e0-300">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



 

 





