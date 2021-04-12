---
title: attribut ms-DS-NC repl
description: Liste des partenaires de réplication passés et présents, et de la manière dont nous sommes en cours avec chacun d’eux.
ms.assetid: febe8614-b68a-4001-b6ae-dae3fe6eb25f
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory pour l’attribut ms-DS-CN-REPL-Cursors
- Schéma Active Directory de l’attribut msDS-NCReplCursors
topic_type:
- apiref
api_name:
- ms-DS-NC-Repl-Cursors
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 555a09520079df624fffb2cb3cb3aa34b81502c2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107800"
---
# <a name="ms-ds-nc-repl-cursors-attribute"></a><span data-ttu-id="5d6c3-105">attribut ms-DS-NC repl</span><span class="sxs-lookup"><span data-stu-id="5d6c3-105">ms-DS-NC-Repl-Cursors attribute</span></span>

<span data-ttu-id="5d6c3-106">Liste des partenaires de réplication passés et présents, et de la manière dont nous sommes en cours avec chacun d’eux.</span><span class="sxs-lookup"><span data-stu-id="5d6c3-106">A list of past and present replication partners, and how current we are with each of them.</span></span>



| <span data-ttu-id="5d6c3-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="5d6c3-107">Entry</span></span> | <span data-ttu-id="5d6c3-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d6c3-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="5d6c3-109">CN</span><span class="sxs-lookup"><span data-stu-id="5d6c3-109">CN</span></span>                | <span data-ttu-id="5d6c3-110">ms-DS-NC REPL-curseurs</span><span class="sxs-lookup"><span data-stu-id="5d6c3-110">ms-DS-NC-Repl-Cursors</span></span>                       |
| <span data-ttu-id="5d6c3-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="5d6c3-111">Ldap-Display-Name</span></span> | <span data-ttu-id="5d6c3-112">msDS-NCReplCursors</span><span class="sxs-lookup"><span data-stu-id="5d6c3-112">msDS-NCReplCursors</span></span>                          |
| <span data-ttu-id="5d6c3-113">Taille</span><span class="sxs-lookup"><span data-stu-id="5d6c3-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="5d6c3-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="5d6c3-114">Update Privilege</span></span>  | <span data-ttu-id="5d6c3-115">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="5d6c3-115">This value is set by the system.</span></span>            |
| <span data-ttu-id="5d6c3-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="5d6c3-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="5d6c3-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5d6c3-117">Attribute-Id</span></span>      | <span data-ttu-id="5d6c3-118">1.2.840.113556.1.4.1704</span><span class="sxs-lookup"><span data-stu-id="5d6c3-118">1.2.840.113556.1.4.1704</span></span>                     |
| <span data-ttu-id="5d6c3-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="5d6c3-119">System-Id-Guid</span></span>    | <span data-ttu-id="5d6c3-120">8a167ce4-f9e8-47eb-8d78-f7fe80abb2cc</span><span class="sxs-lookup"><span data-stu-id="5d6c3-120">8a167ce4-f9e8-47eb-8d78-f7fe80abb2cc</span></span>        |
| <span data-ttu-id="5d6c3-121">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5d6c3-121">Syntax</span></span>            | [<span data-ttu-id="5d6c3-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="5d6c3-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="5d6c3-123">Implémentations</span><span class="sxs-lookup"><span data-stu-id="5d6c3-123">Implementations</span></span>

-   [<span data-ttu-id="5d6c3-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="5d6c3-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="5d6c3-125">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="5d6c3-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="5d6c3-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="5d6c3-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="5d6c3-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5d6c3-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5d6c3-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5d6c3-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5d6c3-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5d6c3-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="5d6c3-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5d6c3-130">Windows Server 2003</span></span>



| <span data-ttu-id="5d6c3-131">Entrée</span><span class="sxs-lookup"><span data-stu-id="5d6c3-131">Entry</span></span> | <span data-ttu-id="5d6c3-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d6c3-132">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="5d6c3-133">ID de lien</span><span class="sxs-lookup"><span data-stu-id="5d6c3-133">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="5d6c3-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5d6c3-134">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="5d6c3-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="5d6c3-135">System-Only</span></span>            | <span data-ttu-id="5d6c3-136">Faux</span><span class="sxs-lookup"><span data-stu-id="5d6c3-136">False</span></span>                           |
| <span data-ttu-id="5d6c3-137">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="5d6c3-137">Is-Single-Valued</span></span>       | <span data-ttu-id="5d6c3-138">Faux</span><span class="sxs-lookup"><span data-stu-id="5d6c3-138">False</span></span>                           |
| <span data-ttu-id="5d6c3-139">Est indexé</span><span class="sxs-lookup"><span data-stu-id="5d6c3-139">Is Indexed</span></span>             | <span data-ttu-id="5d6c3-140">Faux</span><span class="sxs-lookup"><span data-stu-id="5d6c3-140">False</span></span>                           |
| <span data-ttu-id="5d6c3-141">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="5d6c3-141">In Global Catalog</span></span>      | <span data-ttu-id="5d6c3-142">Faux</span><span class="sxs-lookup"><span data-stu-id="5d6c3-142">False</span></span>                           |
| <span data-ttu-id="5d6c3-143">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="5d6c3-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="5d6c3-144">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="5d6c3-144">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="5d6c3-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5d6c3-145">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="5d6c3-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5d6c3-146">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="5d6c3-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5d6c3-147">Search-Flags</span></span>           | <span data-ttu-id="5d6c3-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5d6c3-148">0x00000000</span></span>                      |
| <span data-ttu-id="5d6c3-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5d6c3-149">System-Flags</span></span>           | <span data-ttu-id="5d6c3-150">0x00000014</span><span class="sxs-lookup"><span data-stu-id="5d6c3-150">0x00000014</span></span>                      |
| <span data-ttu-id="5d6c3-151">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="5d6c3-151">Classes used in</span></span>        | [<span data-ttu-id="5d6c3-152">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="5d6c3-152">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="5d6c3-153">ADAM</span><span class="sxs-lookup"><span data-stu-id="5d6c3-153">ADAM</span></span>



| <span data-ttu-id="5d6c3-154">Entrée</span><span class="sxs-lookup"><span data-stu-id="5d6c3-154">Entry</span></span> | <span data-ttu-id="5d6c3-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d6c3-155">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="5d6c3-156">ID de lien</span><span class="sxs-lookup"><span data-stu-id="5d6c3-156">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="5d6c3-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5d6c3-157">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="5d6c3-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="5d6c3-158">System-Only</span></span>            | <span data-ttu-id="5d6c3-159">Faux</span><span class="sxs-lookup"><span data-stu-id="5d6c3-159">False</span></span>                           |
| <span data-ttu-id="5d6c3-160">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="5d6c3-160">Is-Single-Valued</span></span>       | <span data-ttu-id="5d6c3-161">Faux</span><span class="sxs-lookup"><span data-stu-id="5d6c3-161">False</span></span>                           |
| <span data-ttu-id="5d6c3-162">Est indexé</span><span class="sxs-lookup"><span data-stu-id="5d6c3-162">Is Indexed</span></span>             | <span data-ttu-id="5d6c3-163">Faux</span><span class="sxs-lookup"><span data-stu-id="5d6c3-163">False</span></span>                           |
| <span data-ttu-id="5d6c3-164">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="5d6c3-164">In Global Catalog</span></span>      | <span data-ttu-id="5d6c3-165">Faux</span><span class="sxs-lookup"><span data-stu-id="5d6c3-165">False</span></span>                           |
| <span data-ttu-id="5d6c3-166">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="5d6c3-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="5d6c3-167">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="5d6c3-167">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="5d6c3-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5d6c3-168">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="5d6c3-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5d6c3-169">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="5d6c3-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5d6c3-170">Search-Flags</span></span>           | <span data-ttu-id="5d6c3-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5d6c3-171">0x00000000</span></span>                      |
| <span data-ttu-id="5d6c3-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5d6c3-172">System-Flags</span></span>           | <span data-ttu-id="5d6c3-173">0x00000014</span><span class="sxs-lookup"><span data-stu-id="5d6c3-173">0x00000014</span></span>                      |
| <span data-ttu-id="5d6c3-174">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="5d6c3-174">Classes used in</span></span>        | [<span data-ttu-id="5d6c3-175">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="5d6c3-175">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="5d6c3-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="5d6c3-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="5d6c3-177">Entrée</span><span class="sxs-lookup"><span data-stu-id="5d6c3-177">Entry</span></span> | <span data-ttu-id="5d6c3-178">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d6c3-178">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="5d6c3-179">ID de lien</span><span class="sxs-lookup"><span data-stu-id="5d6c3-179">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="5d6c3-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5d6c3-180">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="5d6c3-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="5d6c3-181">System-Only</span></span>            | <span data-ttu-id="5d6c3-182">Faux</span><span class="sxs-lookup"><span data-stu-id="5d6c3-182">False</span></span>                           |
| <span data-ttu-id="5d6c3-183">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="5d6c3-183">Is-Single-Valued</span></span>       | <span data-ttu-id="5d6c3-184">Faux</span><span class="sxs-lookup"><span data-stu-id="5d6c3-184">False</span></span>                           |
| <span data-ttu-id="5d6c3-185">Est indexé</span><span class="sxs-lookup"><span data-stu-id="5d6c3-185">Is Indexed</span></span>             | <span data-ttu-id="5d6c3-186">Faux</span><span class="sxs-lookup"><span data-stu-id="5d6c3-186">False</span></span>                           |
| <span data-ttu-id="5d6c3-187">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="5d6c3-187">In Global Catalog</span></span>      | <span data-ttu-id="5d6c3-188">Faux</span><span class="sxs-lookup"><span data-stu-id="5d6c3-188">False</span></span>                           |
| <span data-ttu-id="5d6c3-189">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="5d6c3-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="5d6c3-190">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="5d6c3-190">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="5d6c3-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5d6c3-191">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="5d6c3-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5d6c3-192">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="5d6c3-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5d6c3-193">Search-Flags</span></span>           | <span data-ttu-id="5d6c3-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5d6c3-194">0x00000000</span></span>                      |
| <span data-ttu-id="5d6c3-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5d6c3-195">System-Flags</span></span>           | <span data-ttu-id="5d6c3-196">0x00000014</span><span class="sxs-lookup"><span data-stu-id="5d6c3-196">0x00000014</span></span>                      |
| <span data-ttu-id="5d6c3-197">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="5d6c3-197">Classes used in</span></span>        | [<span data-ttu-id="5d6c3-198">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="5d6c3-198">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="5d6c3-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5d6c3-199">Windows Server 2008</span></span>



| <span data-ttu-id="5d6c3-200">Entrée</span><span class="sxs-lookup"><span data-stu-id="5d6c3-200">Entry</span></span> | <span data-ttu-id="5d6c3-201">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d6c3-201">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="5d6c3-202">ID de lien</span><span class="sxs-lookup"><span data-stu-id="5d6c3-202">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="5d6c3-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5d6c3-203">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="5d6c3-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="5d6c3-204">System-Only</span></span>            | <span data-ttu-id="5d6c3-205">Faux</span><span class="sxs-lookup"><span data-stu-id="5d6c3-205">False</span></span>                           |
| <span data-ttu-id="5d6c3-206">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="5d6c3-206">Is-Single-Valued</span></span>       | <span data-ttu-id="5d6c3-207">Faux</span><span class="sxs-lookup"><span data-stu-id="5d6c3-207">False</span></span>                           |
| <span data-ttu-id="5d6c3-208">Est indexé</span><span class="sxs-lookup"><span data-stu-id="5d6c3-208">Is Indexed</span></span>             | <span data-ttu-id="5d6c3-209">Faux</span><span class="sxs-lookup"><span data-stu-id="5d6c3-209">False</span></span>                           |
| <span data-ttu-id="5d6c3-210">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="5d6c3-210">In Global Catalog</span></span>      | <span data-ttu-id="5d6c3-211">Faux</span><span class="sxs-lookup"><span data-stu-id="5d6c3-211">False</span></span>                           |
| <span data-ttu-id="5d6c3-212">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="5d6c3-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="5d6c3-213">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="5d6c3-213">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="5d6c3-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5d6c3-214">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="5d6c3-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5d6c3-215">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="5d6c3-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5d6c3-216">Search-Flags</span></span>           | <span data-ttu-id="5d6c3-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5d6c3-217">0x00000000</span></span>                      |
| <span data-ttu-id="5d6c3-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5d6c3-218">System-Flags</span></span>           | <span data-ttu-id="5d6c3-219">0x00000014</span><span class="sxs-lookup"><span data-stu-id="5d6c3-219">0x00000014</span></span>                      |
| <span data-ttu-id="5d6c3-220">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="5d6c3-220">Classes used in</span></span>        | [<span data-ttu-id="5d6c3-221">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="5d6c3-221">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5d6c3-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5d6c3-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5d6c3-223">Entrée</span><span class="sxs-lookup"><span data-stu-id="5d6c3-223">Entry</span></span> | <span data-ttu-id="5d6c3-224">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d6c3-224">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="5d6c3-225">ID de lien</span><span class="sxs-lookup"><span data-stu-id="5d6c3-225">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="5d6c3-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5d6c3-226">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="5d6c3-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="5d6c3-227">System-Only</span></span>            | <span data-ttu-id="5d6c3-228">Faux</span><span class="sxs-lookup"><span data-stu-id="5d6c3-228">False</span></span>                           |
| <span data-ttu-id="5d6c3-229">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="5d6c3-229">Is-Single-Valued</span></span>       | <span data-ttu-id="5d6c3-230">Faux</span><span class="sxs-lookup"><span data-stu-id="5d6c3-230">False</span></span>                           |
| <span data-ttu-id="5d6c3-231">Est indexé</span><span class="sxs-lookup"><span data-stu-id="5d6c3-231">Is Indexed</span></span>             | <span data-ttu-id="5d6c3-232">Faux</span><span class="sxs-lookup"><span data-stu-id="5d6c3-232">False</span></span>                           |
| <span data-ttu-id="5d6c3-233">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="5d6c3-233">In Global Catalog</span></span>      | <span data-ttu-id="5d6c3-234">Faux</span><span class="sxs-lookup"><span data-stu-id="5d6c3-234">False</span></span>                           |
| <span data-ttu-id="5d6c3-235">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="5d6c3-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="5d6c3-236">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="5d6c3-236">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="5d6c3-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5d6c3-237">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="5d6c3-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5d6c3-238">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="5d6c3-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5d6c3-239">Search-Flags</span></span>           | <span data-ttu-id="5d6c3-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5d6c3-240">0x00000000</span></span>                      |
| <span data-ttu-id="5d6c3-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5d6c3-241">System-Flags</span></span>           | <span data-ttu-id="5d6c3-242">0x00000014</span><span class="sxs-lookup"><span data-stu-id="5d6c3-242">0x00000014</span></span>                      |
| <span data-ttu-id="5d6c3-243">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="5d6c3-243">Classes used in</span></span>        | [<span data-ttu-id="5d6c3-244">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="5d6c3-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5d6c3-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5d6c3-245">Windows Server 2012</span></span>



| <span data-ttu-id="5d6c3-246">Entrée</span><span class="sxs-lookup"><span data-stu-id="5d6c3-246">Entry</span></span> | <span data-ttu-id="5d6c3-247">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d6c3-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="5d6c3-248">ID de lien</span><span class="sxs-lookup"><span data-stu-id="5d6c3-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="5d6c3-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5d6c3-249">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="5d6c3-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="5d6c3-250">System-Only</span></span>            | <span data-ttu-id="5d6c3-251">Faux</span><span class="sxs-lookup"><span data-stu-id="5d6c3-251">False</span></span>                           |
| <span data-ttu-id="5d6c3-252">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="5d6c3-252">Is-Single-Valued</span></span>       | <span data-ttu-id="5d6c3-253">Faux</span><span class="sxs-lookup"><span data-stu-id="5d6c3-253">False</span></span>                           |
| <span data-ttu-id="5d6c3-254">Est indexé</span><span class="sxs-lookup"><span data-stu-id="5d6c3-254">Is Indexed</span></span>             | <span data-ttu-id="5d6c3-255">Faux</span><span class="sxs-lookup"><span data-stu-id="5d6c3-255">False</span></span>                           |
| <span data-ttu-id="5d6c3-256">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="5d6c3-256">In Global Catalog</span></span>      | <span data-ttu-id="5d6c3-257">Faux</span><span class="sxs-lookup"><span data-stu-id="5d6c3-257">False</span></span>                           |
| <span data-ttu-id="5d6c3-258">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="5d6c3-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="5d6c3-259">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="5d6c3-259">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="5d6c3-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5d6c3-260">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="5d6c3-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5d6c3-261">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="5d6c3-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5d6c3-262">Search-Flags</span></span>           | <span data-ttu-id="5d6c3-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5d6c3-263">0x00000000</span></span>                      |
| <span data-ttu-id="5d6c3-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5d6c3-264">System-Flags</span></span>           | <span data-ttu-id="5d6c3-265">0x00000014</span><span class="sxs-lookup"><span data-stu-id="5d6c3-265">0x00000014</span></span>                      |
| <span data-ttu-id="5d6c3-266">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="5d6c3-266">Classes used in</span></span>        | [<span data-ttu-id="5d6c3-267">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="5d6c3-267">**Top**</span></span>](c-top.md)<br/> |



 

 





