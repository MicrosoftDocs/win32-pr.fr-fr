---
title: attribut de métadonnées ms-DS-REPL-value-
description: Liste de métadonnées pour chaque valeur d’un attribut. Les métadonnées indiquent qui a modifié la valeur en dernier.
ms.assetid: 79c01bda-ea1b-41ca-b4de-c16c5167b270
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut ms-DS-REPL-value-Meta Data
- Schéma Active Directory de l’attribut msDS-ReplValueMetaData
topic_type:
- apiref
api_name:
- ms-DS-Repl-Value-Meta-Data
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18e90cb5fd462fc75126b6ba80f10638826811d8
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106515113"
---
# <a name="ms-ds-repl-value-meta-data-attribute"></a><span data-ttu-id="cc14f-106">attribut de métadonnées ms-DS-REPL-value-</span><span class="sxs-lookup"><span data-stu-id="cc14f-106">ms-DS-Repl-Value-Meta-Data attribute</span></span>

<span data-ttu-id="cc14f-107">Liste de métadonnées pour chaque valeur d’un attribut.</span><span class="sxs-lookup"><span data-stu-id="cc14f-107">A list of metadata for each value of an attribute.</span></span> <span data-ttu-id="cc14f-108">Les métadonnées indiquent qui a modifié la valeur en dernier.</span><span class="sxs-lookup"><span data-stu-id="cc14f-108">The metadata indicates who changed the value last.</span></span>



| <span data-ttu-id="cc14f-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="cc14f-109">Entry</span></span> | <span data-ttu-id="cc14f-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc14f-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="cc14f-111">CN</span><span class="sxs-lookup"><span data-stu-id="cc14f-111">CN</span></span>                | <span data-ttu-id="cc14f-112">ms-DS-REPL-value-Meta-Data</span><span class="sxs-lookup"><span data-stu-id="cc14f-112">ms-DS-Repl-Value-Meta-Data</span></span>                  |
| <span data-ttu-id="cc14f-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="cc14f-113">Ldap-Display-Name</span></span> | <span data-ttu-id="cc14f-114">msDS-ReplValueMetaData</span><span class="sxs-lookup"><span data-stu-id="cc14f-114">msDS-ReplValueMetaData</span></span>                      |
| <span data-ttu-id="cc14f-115">Taille</span><span class="sxs-lookup"><span data-stu-id="cc14f-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="cc14f-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="cc14f-116">Update Privilege</span></span>  | <span data-ttu-id="cc14f-117">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="cc14f-117">This value is set by the system.</span></span>            |
| <span data-ttu-id="cc14f-118">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="cc14f-118">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="cc14f-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="cc14f-119">Attribute-Id</span></span>      | <span data-ttu-id="cc14f-120">1.2.840.113556.1.4.1708</span><span class="sxs-lookup"><span data-stu-id="cc14f-120">1.2.840.113556.1.4.1708</span></span>                     |
| <span data-ttu-id="cc14f-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="cc14f-121">System-Id-Guid</span></span>    | <span data-ttu-id="cc14f-122">2f5c8145-e1bd-410b-8957-8bfa81d5acfd</span><span class="sxs-lookup"><span data-stu-id="cc14f-122">2f5c8145-e1bd-410b-8957-8bfa81d5acfd</span></span>        |
| <span data-ttu-id="cc14f-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cc14f-123">Syntax</span></span>            | [<span data-ttu-id="cc14f-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="cc14f-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="cc14f-125">Implémentations</span><span class="sxs-lookup"><span data-stu-id="cc14f-125">Implementations</span></span>

-   [<span data-ttu-id="cc14f-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="cc14f-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="cc14f-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="cc14f-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="cc14f-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="cc14f-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="cc14f-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="cc14f-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="cc14f-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="cc14f-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="cc14f-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="cc14f-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="cc14f-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cc14f-132">Windows Server 2003</span></span>



| <span data-ttu-id="cc14f-133">Entrée</span><span class="sxs-lookup"><span data-stu-id="cc14f-133">Entry</span></span> | <span data-ttu-id="cc14f-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc14f-134">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cc14f-135">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cc14f-135">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cc14f-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cc14f-136">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cc14f-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="cc14f-137">System-Only</span></span>            | <span data-ttu-id="cc14f-138">Faux</span><span class="sxs-lookup"><span data-stu-id="cc14f-138">False</span></span>                           |
| <span data-ttu-id="cc14f-139">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cc14f-139">Is-Single-Valued</span></span>       | <span data-ttu-id="cc14f-140">Faux</span><span class="sxs-lookup"><span data-stu-id="cc14f-140">False</span></span>                           |
| <span data-ttu-id="cc14f-141">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cc14f-141">Is Indexed</span></span>             | <span data-ttu-id="cc14f-142">Faux</span><span class="sxs-lookup"><span data-stu-id="cc14f-142">False</span></span>                           |
| <span data-ttu-id="cc14f-143">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cc14f-143">In Global Catalog</span></span>      | <span data-ttu-id="cc14f-144">Faux</span><span class="sxs-lookup"><span data-stu-id="cc14f-144">False</span></span>                           |
| <span data-ttu-id="cc14f-145">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cc14f-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="cc14f-146">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cc14f-146">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cc14f-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cc14f-147">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cc14f-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cc14f-148">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cc14f-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cc14f-149">Search-Flags</span></span>           | <span data-ttu-id="cc14f-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc14f-150">0x00000000</span></span>                      |
| <span data-ttu-id="cc14f-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cc14f-151">System-Flags</span></span>           | <span data-ttu-id="cc14f-152">0x00000014</span><span class="sxs-lookup"><span data-stu-id="cc14f-152">0x00000014</span></span>                      |
| <span data-ttu-id="cc14f-153">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cc14f-153">Classes used in</span></span>        | [<span data-ttu-id="cc14f-154">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="cc14f-154">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="cc14f-155">ADAM</span><span class="sxs-lookup"><span data-stu-id="cc14f-155">ADAM</span></span>



| <span data-ttu-id="cc14f-156">Entrée</span><span class="sxs-lookup"><span data-stu-id="cc14f-156">Entry</span></span> | <span data-ttu-id="cc14f-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc14f-157">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cc14f-158">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cc14f-158">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cc14f-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cc14f-159">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cc14f-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="cc14f-160">System-Only</span></span>            | <span data-ttu-id="cc14f-161">Faux</span><span class="sxs-lookup"><span data-stu-id="cc14f-161">False</span></span>                           |
| <span data-ttu-id="cc14f-162">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cc14f-162">Is-Single-Valued</span></span>       | <span data-ttu-id="cc14f-163">Faux</span><span class="sxs-lookup"><span data-stu-id="cc14f-163">False</span></span>                           |
| <span data-ttu-id="cc14f-164">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cc14f-164">Is Indexed</span></span>             | <span data-ttu-id="cc14f-165">Faux</span><span class="sxs-lookup"><span data-stu-id="cc14f-165">False</span></span>                           |
| <span data-ttu-id="cc14f-166">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cc14f-166">In Global Catalog</span></span>      | <span data-ttu-id="cc14f-167">Faux</span><span class="sxs-lookup"><span data-stu-id="cc14f-167">False</span></span>                           |
| <span data-ttu-id="cc14f-168">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cc14f-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="cc14f-169">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cc14f-169">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cc14f-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cc14f-170">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cc14f-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cc14f-171">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cc14f-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cc14f-172">Search-Flags</span></span>           | <span data-ttu-id="cc14f-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc14f-173">0x00000000</span></span>                      |
| <span data-ttu-id="cc14f-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cc14f-174">System-Flags</span></span>           | <span data-ttu-id="cc14f-175">0x00000014</span><span class="sxs-lookup"><span data-stu-id="cc14f-175">0x00000014</span></span>                      |
| <span data-ttu-id="cc14f-176">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cc14f-176">Classes used in</span></span>        | [<span data-ttu-id="cc14f-177">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="cc14f-177">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="cc14f-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="cc14f-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="cc14f-179">Entrée</span><span class="sxs-lookup"><span data-stu-id="cc14f-179">Entry</span></span> | <span data-ttu-id="cc14f-180">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc14f-180">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cc14f-181">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cc14f-181">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cc14f-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cc14f-182">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cc14f-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="cc14f-183">System-Only</span></span>            | <span data-ttu-id="cc14f-184">Faux</span><span class="sxs-lookup"><span data-stu-id="cc14f-184">False</span></span>                           |
| <span data-ttu-id="cc14f-185">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cc14f-185">Is-Single-Valued</span></span>       | <span data-ttu-id="cc14f-186">Faux</span><span class="sxs-lookup"><span data-stu-id="cc14f-186">False</span></span>                           |
| <span data-ttu-id="cc14f-187">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cc14f-187">Is Indexed</span></span>             | <span data-ttu-id="cc14f-188">Faux</span><span class="sxs-lookup"><span data-stu-id="cc14f-188">False</span></span>                           |
| <span data-ttu-id="cc14f-189">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cc14f-189">In Global Catalog</span></span>      | <span data-ttu-id="cc14f-190">Faux</span><span class="sxs-lookup"><span data-stu-id="cc14f-190">False</span></span>                           |
| <span data-ttu-id="cc14f-191">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cc14f-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="cc14f-192">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cc14f-192">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cc14f-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cc14f-193">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cc14f-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cc14f-194">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cc14f-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cc14f-195">Search-Flags</span></span>           | <span data-ttu-id="cc14f-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc14f-196">0x00000000</span></span>                      |
| <span data-ttu-id="cc14f-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cc14f-197">System-Flags</span></span>           | <span data-ttu-id="cc14f-198">0x00000014</span><span class="sxs-lookup"><span data-stu-id="cc14f-198">0x00000014</span></span>                      |
| <span data-ttu-id="cc14f-199">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cc14f-199">Classes used in</span></span>        | [<span data-ttu-id="cc14f-200">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="cc14f-200">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="cc14f-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cc14f-201">Windows Server 2008</span></span>



| <span data-ttu-id="cc14f-202">Entrée</span><span class="sxs-lookup"><span data-stu-id="cc14f-202">Entry</span></span> | <span data-ttu-id="cc14f-203">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc14f-203">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cc14f-204">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cc14f-204">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cc14f-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cc14f-205">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cc14f-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="cc14f-206">System-Only</span></span>            | <span data-ttu-id="cc14f-207">Faux</span><span class="sxs-lookup"><span data-stu-id="cc14f-207">False</span></span>                           |
| <span data-ttu-id="cc14f-208">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cc14f-208">Is-Single-Valued</span></span>       | <span data-ttu-id="cc14f-209">Faux</span><span class="sxs-lookup"><span data-stu-id="cc14f-209">False</span></span>                           |
| <span data-ttu-id="cc14f-210">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cc14f-210">Is Indexed</span></span>             | <span data-ttu-id="cc14f-211">Faux</span><span class="sxs-lookup"><span data-stu-id="cc14f-211">False</span></span>                           |
| <span data-ttu-id="cc14f-212">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cc14f-212">In Global Catalog</span></span>      | <span data-ttu-id="cc14f-213">Faux</span><span class="sxs-lookup"><span data-stu-id="cc14f-213">False</span></span>                           |
| <span data-ttu-id="cc14f-214">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cc14f-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="cc14f-215">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cc14f-215">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cc14f-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cc14f-216">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cc14f-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cc14f-217">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cc14f-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cc14f-218">Search-Flags</span></span>           | <span data-ttu-id="cc14f-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc14f-219">0x00000000</span></span>                      |
| <span data-ttu-id="cc14f-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cc14f-220">System-Flags</span></span>           | <span data-ttu-id="cc14f-221">0x00000014</span><span class="sxs-lookup"><span data-stu-id="cc14f-221">0x00000014</span></span>                      |
| <span data-ttu-id="cc14f-222">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cc14f-222">Classes used in</span></span>        | [<span data-ttu-id="cc14f-223">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="cc14f-223">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="cc14f-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cc14f-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="cc14f-225">Entrée</span><span class="sxs-lookup"><span data-stu-id="cc14f-225">Entry</span></span> | <span data-ttu-id="cc14f-226">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc14f-226">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cc14f-227">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cc14f-227">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cc14f-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cc14f-228">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cc14f-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="cc14f-229">System-Only</span></span>            | <span data-ttu-id="cc14f-230">Faux</span><span class="sxs-lookup"><span data-stu-id="cc14f-230">False</span></span>                           |
| <span data-ttu-id="cc14f-231">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cc14f-231">Is-Single-Valued</span></span>       | <span data-ttu-id="cc14f-232">Faux</span><span class="sxs-lookup"><span data-stu-id="cc14f-232">False</span></span>                           |
| <span data-ttu-id="cc14f-233">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cc14f-233">Is Indexed</span></span>             | <span data-ttu-id="cc14f-234">Faux</span><span class="sxs-lookup"><span data-stu-id="cc14f-234">False</span></span>                           |
| <span data-ttu-id="cc14f-235">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cc14f-235">In Global Catalog</span></span>      | <span data-ttu-id="cc14f-236">Faux</span><span class="sxs-lookup"><span data-stu-id="cc14f-236">False</span></span>                           |
| <span data-ttu-id="cc14f-237">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cc14f-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="cc14f-238">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cc14f-238">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cc14f-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cc14f-239">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cc14f-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cc14f-240">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cc14f-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cc14f-241">Search-Flags</span></span>           | <span data-ttu-id="cc14f-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc14f-242">0x00000000</span></span>                      |
| <span data-ttu-id="cc14f-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cc14f-243">System-Flags</span></span>           | <span data-ttu-id="cc14f-244">0x00000014</span><span class="sxs-lookup"><span data-stu-id="cc14f-244">0x00000014</span></span>                      |
| <span data-ttu-id="cc14f-245">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cc14f-245">Classes used in</span></span>        | [<span data-ttu-id="cc14f-246">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="cc14f-246">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="cc14f-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cc14f-247">Windows Server 2012</span></span>



| <span data-ttu-id="cc14f-248">Entrée</span><span class="sxs-lookup"><span data-stu-id="cc14f-248">Entry</span></span> | <span data-ttu-id="cc14f-249">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc14f-249">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cc14f-250">ID de lien</span><span class="sxs-lookup"><span data-stu-id="cc14f-250">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cc14f-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cc14f-251">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cc14f-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="cc14f-252">System-Only</span></span>            | <span data-ttu-id="cc14f-253">Faux</span><span class="sxs-lookup"><span data-stu-id="cc14f-253">False</span></span>                           |
| <span data-ttu-id="cc14f-254">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="cc14f-254">Is-Single-Valued</span></span>       | <span data-ttu-id="cc14f-255">Faux</span><span class="sxs-lookup"><span data-stu-id="cc14f-255">False</span></span>                           |
| <span data-ttu-id="cc14f-256">Est indexé</span><span class="sxs-lookup"><span data-stu-id="cc14f-256">Is Indexed</span></span>             | <span data-ttu-id="cc14f-257">Faux</span><span class="sxs-lookup"><span data-stu-id="cc14f-257">False</span></span>                           |
| <span data-ttu-id="cc14f-258">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="cc14f-258">In Global Catalog</span></span>      | <span data-ttu-id="cc14f-259">Faux</span><span class="sxs-lookup"><span data-stu-id="cc14f-259">False</span></span>                           |
| <span data-ttu-id="cc14f-260">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="cc14f-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="cc14f-261">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="cc14f-261">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cc14f-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cc14f-262">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cc14f-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cc14f-263">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cc14f-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cc14f-264">Search-Flags</span></span>           | <span data-ttu-id="cc14f-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc14f-265">0x00000000</span></span>                      |
| <span data-ttu-id="cc14f-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cc14f-266">System-Flags</span></span>           | <span data-ttu-id="cc14f-267">0x00000014</span><span class="sxs-lookup"><span data-stu-id="cc14f-267">0x00000014</span></span>                      |
| <span data-ttu-id="cc14f-268">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="cc14f-268">Classes used in</span></span>        | [<span data-ttu-id="cc14f-269">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="cc14f-269">**Top**</span></span>](c-top.md)<br/> |



 

 





