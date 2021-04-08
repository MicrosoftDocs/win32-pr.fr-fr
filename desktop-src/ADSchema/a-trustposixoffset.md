---
title: Trust-POSIX-offset, attribut
description: Décalage POSIX (Portable Operating System Interface) du domaine approuvé.
ms.assetid: a1263f9f-1577-44b8-b7cc-317a8ecb37f1
ms.tgt_platform: multiple
keywords:
- Trust-POSIX-attribut de décalage-schéma AD
- Schéma AD de l’attribut trustPosixOffset
topic_type:
- apiref
api_name:
- Trust-Posix-Offset
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de8f3dca090d44ea545dcc290b04d99131d50dc7
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104033332"
---
# <a name="trust-posix-offset-attribute"></a><span data-ttu-id="5d081-105">Trust-POSIX-offset, attribut</span><span class="sxs-lookup"><span data-stu-id="5d081-105">Trust-Posix-Offset attribute</span></span>

<span data-ttu-id="5d081-106">Décalage POSIX (Portable Operating System Interface) du domaine approuvé.</span><span class="sxs-lookup"><span data-stu-id="5d081-106">The Portable Operating System Interface (POSIX) offset for the trusted domain.</span></span>



| <span data-ttu-id="5d081-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="5d081-107">Entry</span></span> | <span data-ttu-id="5d081-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d081-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="5d081-109">CN</span><span class="sxs-lookup"><span data-stu-id="5d081-109">CN</span></span>                | <span data-ttu-id="5d081-110">Trust-POSIX-offset</span><span class="sxs-lookup"><span data-stu-id="5d081-110">Trust-Posix-Offset</span></span>                   |
| <span data-ttu-id="5d081-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="5d081-111">Ldap-Display-Name</span></span> | <span data-ttu-id="5d081-112">trustPosixOffset</span><span class="sxs-lookup"><span data-stu-id="5d081-112">trustPosixOffset</span></span>                     |
| <span data-ttu-id="5d081-113">Taille</span><span class="sxs-lookup"><span data-stu-id="5d081-113">Size</span></span>              | <span data-ttu-id="5d081-114">4 octets</span><span class="sxs-lookup"><span data-stu-id="5d081-114">4 bytes</span></span>                              |
| <span data-ttu-id="5d081-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="5d081-115">Update Privilege</span></span>  | <span data-ttu-id="5d081-116">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="5d081-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="5d081-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="5d081-117">Update Frequency</span></span>  | <span data-ttu-id="5d081-118">Lors de la création d’une approbation.</span><span class="sxs-lookup"><span data-stu-id="5d081-118">When a new trust is created.</span></span>         |
| <span data-ttu-id="5d081-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5d081-119">Attribute-Id</span></span>      | <span data-ttu-id="5d081-120">1.2.840.113556.1.4.134</span><span class="sxs-lookup"><span data-stu-id="5d081-120">1.2.840.113556.1.4.134</span></span>               |
| <span data-ttu-id="5d081-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="5d081-121">System-Id-Guid</span></span>    | <span data-ttu-id="5d081-122">bf967a5e-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="5d081-122">bf967a5e-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="5d081-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5d081-123">Syntax</span></span>            | [<span data-ttu-id="5d081-124">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="5d081-124">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="5d081-125">Implémentations</span><span class="sxs-lookup"><span data-stu-id="5d081-125">Implementations</span></span>

-   [<span data-ttu-id="5d081-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="5d081-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="5d081-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="5d081-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="5d081-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="5d081-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="5d081-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5d081-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5d081-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5d081-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5d081-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5d081-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="5d081-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5d081-132">Windows 2000 Server</span></span>



| <span data-ttu-id="5d081-133">Entrée</span><span class="sxs-lookup"><span data-stu-id="5d081-133">Entry</span></span> | <span data-ttu-id="5d081-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d081-134">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="5d081-135">ID de lien</span><span class="sxs-lookup"><span data-stu-id="5d081-135">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="5d081-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5d081-136">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="5d081-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="5d081-137">System-Only</span></span>            | <span data-ttu-id="5d081-138">Faux</span><span class="sxs-lookup"><span data-stu-id="5d081-138">False</span></span>                                                |
| <span data-ttu-id="5d081-139">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="5d081-139">Is-Single-Valued</span></span>       | <span data-ttu-id="5d081-140">Vrai</span><span class="sxs-lookup"><span data-stu-id="5d081-140">True</span></span>                                                 |
| <span data-ttu-id="5d081-141">Est indexé</span><span class="sxs-lookup"><span data-stu-id="5d081-141">Is Indexed</span></span>             | <span data-ttu-id="5d081-142">Faux</span><span class="sxs-lookup"><span data-stu-id="5d081-142">False</span></span>                                                |
| <span data-ttu-id="5d081-143">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="5d081-143">In Global Catalog</span></span>      | <span data-ttu-id="5d081-144">Faux</span><span class="sxs-lookup"><span data-stu-id="5d081-144">False</span></span>                                                |
| <span data-ttu-id="5d081-145">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="5d081-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="5d081-146">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="5d081-146">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="5d081-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5d081-147">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="5d081-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5d081-148">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="5d081-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5d081-149">Search-Flags</span></span>           | <span data-ttu-id="5d081-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5d081-150">0x00000000</span></span>                                           |
| <span data-ttu-id="5d081-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5d081-151">System-Flags</span></span>           | <span data-ttu-id="5d081-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5d081-152">0x00000010</span></span>                                           |
| <span data-ttu-id="5d081-153">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="5d081-153">Classes used in</span></span>        | [<span data-ttu-id="5d081-154">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="5d081-154">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="5d081-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5d081-155">Windows Server 2003</span></span>



| <span data-ttu-id="5d081-156">Entrée</span><span class="sxs-lookup"><span data-stu-id="5d081-156">Entry</span></span> | <span data-ttu-id="5d081-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d081-157">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="5d081-158">ID de lien</span><span class="sxs-lookup"><span data-stu-id="5d081-158">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="5d081-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5d081-159">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="5d081-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="5d081-160">System-Only</span></span>            | <span data-ttu-id="5d081-161">Faux</span><span class="sxs-lookup"><span data-stu-id="5d081-161">False</span></span>                                                |
| <span data-ttu-id="5d081-162">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="5d081-162">Is-Single-Valued</span></span>       | <span data-ttu-id="5d081-163">Vrai</span><span class="sxs-lookup"><span data-stu-id="5d081-163">True</span></span>                                                 |
| <span data-ttu-id="5d081-164">Est indexé</span><span class="sxs-lookup"><span data-stu-id="5d081-164">Is Indexed</span></span>             | <span data-ttu-id="5d081-165">Faux</span><span class="sxs-lookup"><span data-stu-id="5d081-165">False</span></span>                                                |
| <span data-ttu-id="5d081-166">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="5d081-166">In Global Catalog</span></span>      | <span data-ttu-id="5d081-167">Faux</span><span class="sxs-lookup"><span data-stu-id="5d081-167">False</span></span>                                                |
| <span data-ttu-id="5d081-168">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="5d081-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="5d081-169">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="5d081-169">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="5d081-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5d081-170">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="5d081-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5d081-171">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="5d081-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5d081-172">Search-Flags</span></span>           | <span data-ttu-id="5d081-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5d081-173">0x00000000</span></span>                                           |
| <span data-ttu-id="5d081-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5d081-174">System-Flags</span></span>           | <span data-ttu-id="5d081-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5d081-175">0x00000010</span></span>                                           |
| <span data-ttu-id="5d081-176">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="5d081-176">Classes used in</span></span>        | [<span data-ttu-id="5d081-177">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="5d081-177">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="5d081-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="5d081-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="5d081-179">Entrée</span><span class="sxs-lookup"><span data-stu-id="5d081-179">Entry</span></span> | <span data-ttu-id="5d081-180">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d081-180">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="5d081-181">ID de lien</span><span class="sxs-lookup"><span data-stu-id="5d081-181">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="5d081-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5d081-182">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="5d081-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="5d081-183">System-Only</span></span>            | <span data-ttu-id="5d081-184">Faux</span><span class="sxs-lookup"><span data-stu-id="5d081-184">False</span></span>                                                |
| <span data-ttu-id="5d081-185">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="5d081-185">Is-Single-Valued</span></span>       | <span data-ttu-id="5d081-186">Vrai</span><span class="sxs-lookup"><span data-stu-id="5d081-186">True</span></span>                                                 |
| <span data-ttu-id="5d081-187">Est indexé</span><span class="sxs-lookup"><span data-stu-id="5d081-187">Is Indexed</span></span>             | <span data-ttu-id="5d081-188">Faux</span><span class="sxs-lookup"><span data-stu-id="5d081-188">False</span></span>                                                |
| <span data-ttu-id="5d081-189">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="5d081-189">In Global Catalog</span></span>      | <span data-ttu-id="5d081-190">Faux</span><span class="sxs-lookup"><span data-stu-id="5d081-190">False</span></span>                                                |
| <span data-ttu-id="5d081-191">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="5d081-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="5d081-192">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="5d081-192">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="5d081-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5d081-193">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="5d081-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5d081-194">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="5d081-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5d081-195">Search-Flags</span></span>           | <span data-ttu-id="5d081-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5d081-196">0x00000000</span></span>                                           |
| <span data-ttu-id="5d081-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5d081-197">System-Flags</span></span>           | <span data-ttu-id="5d081-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5d081-198">0x00000010</span></span>                                           |
| <span data-ttu-id="5d081-199">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="5d081-199">Classes used in</span></span>        | [<span data-ttu-id="5d081-200">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="5d081-200">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="5d081-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5d081-201">Windows Server 2008</span></span>



| <span data-ttu-id="5d081-202">Entrée</span><span class="sxs-lookup"><span data-stu-id="5d081-202">Entry</span></span> | <span data-ttu-id="5d081-203">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d081-203">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="5d081-204">ID de lien</span><span class="sxs-lookup"><span data-stu-id="5d081-204">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="5d081-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5d081-205">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="5d081-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="5d081-206">System-Only</span></span>            | <span data-ttu-id="5d081-207">Faux</span><span class="sxs-lookup"><span data-stu-id="5d081-207">False</span></span>                                                |
| <span data-ttu-id="5d081-208">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="5d081-208">Is-Single-Valued</span></span>       | <span data-ttu-id="5d081-209">Vrai</span><span class="sxs-lookup"><span data-stu-id="5d081-209">True</span></span>                                                 |
| <span data-ttu-id="5d081-210">Est indexé</span><span class="sxs-lookup"><span data-stu-id="5d081-210">Is Indexed</span></span>             | <span data-ttu-id="5d081-211">Faux</span><span class="sxs-lookup"><span data-stu-id="5d081-211">False</span></span>                                                |
| <span data-ttu-id="5d081-212">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="5d081-212">In Global Catalog</span></span>      | <span data-ttu-id="5d081-213">Faux</span><span class="sxs-lookup"><span data-stu-id="5d081-213">False</span></span>                                                |
| <span data-ttu-id="5d081-214">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="5d081-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="5d081-215">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="5d081-215">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="5d081-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5d081-216">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="5d081-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5d081-217">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="5d081-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5d081-218">Search-Flags</span></span>           | <span data-ttu-id="5d081-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5d081-219">0x00000000</span></span>                                           |
| <span data-ttu-id="5d081-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5d081-220">System-Flags</span></span>           | <span data-ttu-id="5d081-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5d081-221">0x00000010</span></span>                                           |
| <span data-ttu-id="5d081-222">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="5d081-222">Classes used in</span></span>        | [<span data-ttu-id="5d081-223">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="5d081-223">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5d081-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5d081-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5d081-225">Entrée</span><span class="sxs-lookup"><span data-stu-id="5d081-225">Entry</span></span> | <span data-ttu-id="5d081-226">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d081-226">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="5d081-227">ID de lien</span><span class="sxs-lookup"><span data-stu-id="5d081-227">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="5d081-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5d081-228">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="5d081-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="5d081-229">System-Only</span></span>            | <span data-ttu-id="5d081-230">Faux</span><span class="sxs-lookup"><span data-stu-id="5d081-230">False</span></span>                                                |
| <span data-ttu-id="5d081-231">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="5d081-231">Is-Single-Valued</span></span>       | <span data-ttu-id="5d081-232">Vrai</span><span class="sxs-lookup"><span data-stu-id="5d081-232">True</span></span>                                                 |
| <span data-ttu-id="5d081-233">Est indexé</span><span class="sxs-lookup"><span data-stu-id="5d081-233">Is Indexed</span></span>             | <span data-ttu-id="5d081-234">Faux</span><span class="sxs-lookup"><span data-stu-id="5d081-234">False</span></span>                                                |
| <span data-ttu-id="5d081-235">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="5d081-235">In Global Catalog</span></span>      | <span data-ttu-id="5d081-236">Faux</span><span class="sxs-lookup"><span data-stu-id="5d081-236">False</span></span>                                                |
| <span data-ttu-id="5d081-237">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="5d081-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="5d081-238">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="5d081-238">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="5d081-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5d081-239">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="5d081-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5d081-240">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="5d081-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5d081-241">Search-Flags</span></span>           | <span data-ttu-id="5d081-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5d081-242">0x00000000</span></span>                                           |
| <span data-ttu-id="5d081-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5d081-243">System-Flags</span></span>           | <span data-ttu-id="5d081-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5d081-244">0x00000010</span></span>                                           |
| <span data-ttu-id="5d081-245">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="5d081-245">Classes used in</span></span>        | [<span data-ttu-id="5d081-246">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="5d081-246">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5d081-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5d081-247">Windows Server 2012</span></span>



| <span data-ttu-id="5d081-248">Entrée</span><span class="sxs-lookup"><span data-stu-id="5d081-248">Entry</span></span> | <span data-ttu-id="5d081-249">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d081-249">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="5d081-250">ID de lien</span><span class="sxs-lookup"><span data-stu-id="5d081-250">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="5d081-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5d081-251">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="5d081-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="5d081-252">System-Only</span></span>            | <span data-ttu-id="5d081-253">Faux</span><span class="sxs-lookup"><span data-stu-id="5d081-253">False</span></span>                                                |
| <span data-ttu-id="5d081-254">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="5d081-254">Is-Single-Valued</span></span>       | <span data-ttu-id="5d081-255">Vrai</span><span class="sxs-lookup"><span data-stu-id="5d081-255">True</span></span>                                                 |
| <span data-ttu-id="5d081-256">Est indexé</span><span class="sxs-lookup"><span data-stu-id="5d081-256">Is Indexed</span></span>             | <span data-ttu-id="5d081-257">Faux</span><span class="sxs-lookup"><span data-stu-id="5d081-257">False</span></span>                                                |
| <span data-ttu-id="5d081-258">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="5d081-258">In Global Catalog</span></span>      | <span data-ttu-id="5d081-259">Faux</span><span class="sxs-lookup"><span data-stu-id="5d081-259">False</span></span>                                                |
| <span data-ttu-id="5d081-260">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="5d081-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="5d081-261">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="5d081-261">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="5d081-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5d081-262">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="5d081-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5d081-263">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="5d081-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5d081-264">Search-Flags</span></span>           | <span data-ttu-id="5d081-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5d081-265">0x00000000</span></span>                                           |
| <span data-ttu-id="5d081-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5d081-266">System-Flags</span></span>           | <span data-ttu-id="5d081-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5d081-267">0x00000010</span></span>                                           |
| <span data-ttu-id="5d081-268">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="5d081-268">Classes used in</span></span>        | [<span data-ttu-id="5d081-269">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="5d081-269">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





