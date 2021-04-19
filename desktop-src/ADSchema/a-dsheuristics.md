---
title: Attribut DS-Heuristics
description: Contient des paramètres globaux pour l’ensemble de la forêt.
ms.assetid: d5fd990b-7bbf-4ede-a3af-7f3f7ac959b3
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut DS-Heuristics
- Schéma AD attribut dSHeuristics
topic_type:
- apiref
api_name:
- DS-Heuristics
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65922b580975ec05877ae33d213ff3a3675ec72f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106543635"
---
# <a name="ds-heuristics-attribute"></a><span data-ttu-id="b97d5-105">Attribut DS-Heuristics</span><span class="sxs-lookup"><span data-stu-id="b97d5-105">DS-Heuristics attribute</span></span>

<span data-ttu-id="b97d5-106">Contient des paramètres globaux pour l’ensemble de la forêt.</span><span class="sxs-lookup"><span data-stu-id="b97d5-106">Contains global settings for the entire forest.</span></span>

<span data-ttu-id="b97d5-107">Des informations sur les bits d’exclusion adminSDholder sont disponibles sur le site Web aide et support Microsoft dans un article numéro [817433, les autorisations déléguées ne sont pas disponibles et l’héritage est automatiquement désactivé](https://support.microsoft.com/default.aspx?scid=kb;EN-US;817433).</span><span class="sxs-lookup"><span data-stu-id="b97d5-107">There is information about adminSDholder exclusion bits available on the Microsoft Help and Support website in an article number [817433, Delegated permissions are not available and inheritance is automatically disabled](https://support.microsoft.com/default.aspx?scid=kb;EN-US;817433).</span></span>



| <span data-ttu-id="b97d5-108">Entrée</span><span class="sxs-lookup"><span data-stu-id="b97d5-108">Entry</span></span> | <span data-ttu-id="b97d5-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="b97d5-109">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="b97d5-110">CN</span><span class="sxs-lookup"><span data-stu-id="b97d5-110">CN</span></span>                | <span data-ttu-id="b97d5-111">DS-Heuristics</span><span class="sxs-lookup"><span data-stu-id="b97d5-111">DS-Heuristics</span></span>                               |
| <span data-ttu-id="b97d5-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="b97d5-112">Ldap-Display-Name</span></span> | <span data-ttu-id="b97d5-113">dSHeuristics</span><span class="sxs-lookup"><span data-stu-id="b97d5-113">dSHeuristics</span></span>                                |
| <span data-ttu-id="b97d5-114">Taille</span><span class="sxs-lookup"><span data-stu-id="b97d5-114">Size</span></span>              | \-                                          |
| <span data-ttu-id="b97d5-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="b97d5-115">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="b97d5-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="b97d5-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="b97d5-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b97d5-117">Attribute-Id</span></span>      | <span data-ttu-id="b97d5-118">1.2.840.113556.1.2.212</span><span class="sxs-lookup"><span data-stu-id="b97d5-118">1.2.840.113556.1.2.212</span></span>                      |
| <span data-ttu-id="b97d5-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b97d5-119">System-Id-Guid</span></span>    | <span data-ttu-id="b97d5-120">f0f8ff86-1191-11d0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="b97d5-120">f0f8ff86-1191-11d0-a060-00aa006c33ed</span></span>        |
| <span data-ttu-id="b97d5-121">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b97d5-121">Syntax</span></span>            | [<span data-ttu-id="b97d5-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="b97d5-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="b97d5-123">Implémentations</span><span class="sxs-lookup"><span data-stu-id="b97d5-123">Implementations</span></span>

-   [<span data-ttu-id="b97d5-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b97d5-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b97d5-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b97d5-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b97d5-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="b97d5-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="b97d5-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b97d5-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b97d5-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b97d5-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b97d5-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b97d5-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b97d5-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b97d5-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b97d5-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b97d5-131">Windows 2000 Server</span></span>



| <span data-ttu-id="b97d5-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="b97d5-132">Entry</span></span> | <span data-ttu-id="b97d5-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="b97d5-133">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="b97d5-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b97d5-134">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="b97d5-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b97d5-135">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="b97d5-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="b97d5-136">System-Only</span></span>            | <span data-ttu-id="b97d5-137">Faux</span><span class="sxs-lookup"><span data-stu-id="b97d5-137">False</span></span>                                            |
| <span data-ttu-id="b97d5-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b97d5-138">Is-Single-Valued</span></span>       | <span data-ttu-id="b97d5-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="b97d5-139">True</span></span>                                             |
| <span data-ttu-id="b97d5-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b97d5-140">Is Indexed</span></span>             | <span data-ttu-id="b97d5-141">Faux</span><span class="sxs-lookup"><span data-stu-id="b97d5-141">False</span></span>                                            |
| <span data-ttu-id="b97d5-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b97d5-142">In Global Catalog</span></span>      | <span data-ttu-id="b97d5-143">Faux</span><span class="sxs-lookup"><span data-stu-id="b97d5-143">False</span></span>                                            |
| <span data-ttu-id="b97d5-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b97d5-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="b97d5-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b97d5-145">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="b97d5-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b97d5-146">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="b97d5-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b97d5-147">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="b97d5-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b97d5-148">Search-Flags</span></span>           | <span data-ttu-id="b97d5-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b97d5-149">0x00000000</span></span>                                       |
| <span data-ttu-id="b97d5-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b97d5-150">System-Flags</span></span>           | <span data-ttu-id="b97d5-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b97d5-151">0x00000010</span></span>                                       |
| <span data-ttu-id="b97d5-152">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b97d5-152">Classes used in</span></span>        | [<span data-ttu-id="b97d5-153">**NTDS-service**</span><span class="sxs-lookup"><span data-stu-id="b97d5-153">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b97d5-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b97d5-154">Windows Server 2003</span></span>



| <span data-ttu-id="b97d5-155">Entrée</span><span class="sxs-lookup"><span data-stu-id="b97d5-155">Entry</span></span> | <span data-ttu-id="b97d5-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="b97d5-156">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="b97d5-157">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b97d5-157">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="b97d5-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b97d5-158">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="b97d5-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="b97d5-159">System-Only</span></span>            | <span data-ttu-id="b97d5-160">Faux</span><span class="sxs-lookup"><span data-stu-id="b97d5-160">False</span></span>                                            |
| <span data-ttu-id="b97d5-161">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b97d5-161">Is-Single-Valued</span></span>       | <span data-ttu-id="b97d5-162">Vrai</span><span class="sxs-lookup"><span data-stu-id="b97d5-162">True</span></span>                                             |
| <span data-ttu-id="b97d5-163">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b97d5-163">Is Indexed</span></span>             | <span data-ttu-id="b97d5-164">Faux</span><span class="sxs-lookup"><span data-stu-id="b97d5-164">False</span></span>                                            |
| <span data-ttu-id="b97d5-165">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b97d5-165">In Global Catalog</span></span>      | <span data-ttu-id="b97d5-166">Faux</span><span class="sxs-lookup"><span data-stu-id="b97d5-166">False</span></span>                                            |
| <span data-ttu-id="b97d5-167">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b97d5-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="b97d5-168">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b97d5-168">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="b97d5-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b97d5-169">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="b97d5-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b97d5-170">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="b97d5-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b97d5-171">Search-Flags</span></span>           | <span data-ttu-id="b97d5-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b97d5-172">0x00000000</span></span>                                       |
| <span data-ttu-id="b97d5-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b97d5-173">System-Flags</span></span>           | <span data-ttu-id="b97d5-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b97d5-174">0x00000010</span></span>                                       |
| <span data-ttu-id="b97d5-175">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b97d5-175">Classes used in</span></span>        | [<span data-ttu-id="b97d5-176">**NTDS-service**</span><span class="sxs-lookup"><span data-stu-id="b97d5-176">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="adam"></a><span data-ttu-id="b97d5-177">ADAM</span><span class="sxs-lookup"><span data-stu-id="b97d5-177">ADAM</span></span>



| <span data-ttu-id="b97d5-178">Entrée</span><span class="sxs-lookup"><span data-stu-id="b97d5-178">Entry</span></span> | <span data-ttu-id="b97d5-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="b97d5-179">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="b97d5-180">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b97d5-180">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="b97d5-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b97d5-181">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="b97d5-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="b97d5-182">System-Only</span></span>            | <span data-ttu-id="b97d5-183">Faux</span><span class="sxs-lookup"><span data-stu-id="b97d5-183">False</span></span>                                            |
| <span data-ttu-id="b97d5-184">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b97d5-184">Is-Single-Valued</span></span>       | <span data-ttu-id="b97d5-185">Vrai</span><span class="sxs-lookup"><span data-stu-id="b97d5-185">True</span></span>                                             |
| <span data-ttu-id="b97d5-186">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b97d5-186">Is Indexed</span></span>             | <span data-ttu-id="b97d5-187">Faux</span><span class="sxs-lookup"><span data-stu-id="b97d5-187">False</span></span>                                            |
| <span data-ttu-id="b97d5-188">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b97d5-188">In Global Catalog</span></span>      | <span data-ttu-id="b97d5-189">Faux</span><span class="sxs-lookup"><span data-stu-id="b97d5-189">False</span></span>                                            |
| <span data-ttu-id="b97d5-190">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b97d5-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="b97d5-191">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b97d5-191">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="b97d5-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b97d5-192">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="b97d5-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b97d5-193">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="b97d5-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b97d5-194">Search-Flags</span></span>           | <span data-ttu-id="b97d5-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b97d5-195">0x00000000</span></span>                                       |
| <span data-ttu-id="b97d5-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b97d5-196">System-Flags</span></span>           | <span data-ttu-id="b97d5-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b97d5-197">0x00000010</span></span>                                       |
| <span data-ttu-id="b97d5-198">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b97d5-198">Classes used in</span></span>        | [<span data-ttu-id="b97d5-199">**NTDS-service**</span><span class="sxs-lookup"><span data-stu-id="b97d5-199">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b97d5-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b97d5-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b97d5-201">Entrée</span><span class="sxs-lookup"><span data-stu-id="b97d5-201">Entry</span></span> | <span data-ttu-id="b97d5-202">Valeur</span><span class="sxs-lookup"><span data-stu-id="b97d5-202">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="b97d5-203">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b97d5-203">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="b97d5-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b97d5-204">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="b97d5-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="b97d5-205">System-Only</span></span>            | <span data-ttu-id="b97d5-206">Faux</span><span class="sxs-lookup"><span data-stu-id="b97d5-206">False</span></span>                                            |
| <span data-ttu-id="b97d5-207">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b97d5-207">Is-Single-Valued</span></span>       | <span data-ttu-id="b97d5-208">Vrai</span><span class="sxs-lookup"><span data-stu-id="b97d5-208">True</span></span>                                             |
| <span data-ttu-id="b97d5-209">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b97d5-209">Is Indexed</span></span>             | <span data-ttu-id="b97d5-210">Faux</span><span class="sxs-lookup"><span data-stu-id="b97d5-210">False</span></span>                                            |
| <span data-ttu-id="b97d5-211">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b97d5-211">In Global Catalog</span></span>      | <span data-ttu-id="b97d5-212">Faux</span><span class="sxs-lookup"><span data-stu-id="b97d5-212">False</span></span>                                            |
| <span data-ttu-id="b97d5-213">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b97d5-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="b97d5-214">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b97d5-214">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="b97d5-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b97d5-215">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="b97d5-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b97d5-216">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="b97d5-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b97d5-217">Search-Flags</span></span>           | <span data-ttu-id="b97d5-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b97d5-218">0x00000000</span></span>                                       |
| <span data-ttu-id="b97d5-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b97d5-219">System-Flags</span></span>           | <span data-ttu-id="b97d5-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b97d5-220">0x00000010</span></span>                                       |
| <span data-ttu-id="b97d5-221">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b97d5-221">Classes used in</span></span>        | [<span data-ttu-id="b97d5-222">**NTDS-service**</span><span class="sxs-lookup"><span data-stu-id="b97d5-222">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b97d5-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b97d5-223">Windows Server 2008</span></span>



| <span data-ttu-id="b97d5-224">Entrée</span><span class="sxs-lookup"><span data-stu-id="b97d5-224">Entry</span></span> | <span data-ttu-id="b97d5-225">Valeur</span><span class="sxs-lookup"><span data-stu-id="b97d5-225">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="b97d5-226">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b97d5-226">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="b97d5-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b97d5-227">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="b97d5-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="b97d5-228">System-Only</span></span>            | <span data-ttu-id="b97d5-229">Faux</span><span class="sxs-lookup"><span data-stu-id="b97d5-229">False</span></span>                                            |
| <span data-ttu-id="b97d5-230">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b97d5-230">Is-Single-Valued</span></span>       | <span data-ttu-id="b97d5-231">Vrai</span><span class="sxs-lookup"><span data-stu-id="b97d5-231">True</span></span>                                             |
| <span data-ttu-id="b97d5-232">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b97d5-232">Is Indexed</span></span>             | <span data-ttu-id="b97d5-233">Faux</span><span class="sxs-lookup"><span data-stu-id="b97d5-233">False</span></span>                                            |
| <span data-ttu-id="b97d5-234">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b97d5-234">In Global Catalog</span></span>      | <span data-ttu-id="b97d5-235">Faux</span><span class="sxs-lookup"><span data-stu-id="b97d5-235">False</span></span>                                            |
| <span data-ttu-id="b97d5-236">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b97d5-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="b97d5-237">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b97d5-237">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="b97d5-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b97d5-238">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="b97d5-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b97d5-239">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="b97d5-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b97d5-240">Search-Flags</span></span>           | <span data-ttu-id="b97d5-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b97d5-241">0x00000000</span></span>                                       |
| <span data-ttu-id="b97d5-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b97d5-242">System-Flags</span></span>           | <span data-ttu-id="b97d5-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b97d5-243">0x00000010</span></span>                                       |
| <span data-ttu-id="b97d5-244">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b97d5-244">Classes used in</span></span>        | [<span data-ttu-id="b97d5-245">**NTDS-service**</span><span class="sxs-lookup"><span data-stu-id="b97d5-245">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b97d5-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b97d5-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b97d5-247">Entrée</span><span class="sxs-lookup"><span data-stu-id="b97d5-247">Entry</span></span> | <span data-ttu-id="b97d5-248">Valeur</span><span class="sxs-lookup"><span data-stu-id="b97d5-248">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="b97d5-249">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b97d5-249">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="b97d5-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b97d5-250">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="b97d5-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="b97d5-251">System-Only</span></span>            | <span data-ttu-id="b97d5-252">Faux</span><span class="sxs-lookup"><span data-stu-id="b97d5-252">False</span></span>                                            |
| <span data-ttu-id="b97d5-253">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b97d5-253">Is-Single-Valued</span></span>       | <span data-ttu-id="b97d5-254">Vrai</span><span class="sxs-lookup"><span data-stu-id="b97d5-254">True</span></span>                                             |
| <span data-ttu-id="b97d5-255">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b97d5-255">Is Indexed</span></span>             | <span data-ttu-id="b97d5-256">Faux</span><span class="sxs-lookup"><span data-stu-id="b97d5-256">False</span></span>                                            |
| <span data-ttu-id="b97d5-257">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b97d5-257">In Global Catalog</span></span>      | <span data-ttu-id="b97d5-258">Faux</span><span class="sxs-lookup"><span data-stu-id="b97d5-258">False</span></span>                                            |
| <span data-ttu-id="b97d5-259">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b97d5-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="b97d5-260">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b97d5-260">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="b97d5-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b97d5-261">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="b97d5-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b97d5-262">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="b97d5-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b97d5-263">Search-Flags</span></span>           | <span data-ttu-id="b97d5-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b97d5-264">0x00000000</span></span>                                       |
| <span data-ttu-id="b97d5-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b97d5-265">System-Flags</span></span>           | <span data-ttu-id="b97d5-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b97d5-266">0x00000010</span></span>                                       |
| <span data-ttu-id="b97d5-267">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b97d5-267">Classes used in</span></span>        | [<span data-ttu-id="b97d5-268">**NTDS-service**</span><span class="sxs-lookup"><span data-stu-id="b97d5-268">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b97d5-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b97d5-269">Windows Server 2012</span></span>



| <span data-ttu-id="b97d5-270">Entrée</span><span class="sxs-lookup"><span data-stu-id="b97d5-270">Entry</span></span> | <span data-ttu-id="b97d5-271">Valeur</span><span class="sxs-lookup"><span data-stu-id="b97d5-271">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="b97d5-272">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b97d5-272">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="b97d5-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b97d5-273">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="b97d5-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="b97d5-274">System-Only</span></span>            | <span data-ttu-id="b97d5-275">Faux</span><span class="sxs-lookup"><span data-stu-id="b97d5-275">False</span></span>                                            |
| <span data-ttu-id="b97d5-276">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b97d5-276">Is-Single-Valued</span></span>       | <span data-ttu-id="b97d5-277">Vrai</span><span class="sxs-lookup"><span data-stu-id="b97d5-277">True</span></span>                                             |
| <span data-ttu-id="b97d5-278">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b97d5-278">Is Indexed</span></span>             | <span data-ttu-id="b97d5-279">Faux</span><span class="sxs-lookup"><span data-stu-id="b97d5-279">False</span></span>                                            |
| <span data-ttu-id="b97d5-280">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b97d5-280">In Global Catalog</span></span>      | <span data-ttu-id="b97d5-281">Faux</span><span class="sxs-lookup"><span data-stu-id="b97d5-281">False</span></span>                                            |
| <span data-ttu-id="b97d5-282">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b97d5-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="b97d5-283">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b97d5-283">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="b97d5-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b97d5-284">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="b97d5-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b97d5-285">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="b97d5-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b97d5-286">Search-Flags</span></span>           | <span data-ttu-id="b97d5-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b97d5-287">0x00000000</span></span>                                       |
| <span data-ttu-id="b97d5-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b97d5-288">System-Flags</span></span>           | <span data-ttu-id="b97d5-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b97d5-289">0x00000010</span></span>                                       |
| <span data-ttu-id="b97d5-290">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b97d5-290">Classes used in</span></span>        | [<span data-ttu-id="b97d5-291">**NTDS-service**</span><span class="sxs-lookup"><span data-stu-id="b97d5-291">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="b97d5-292">Notes</span><span class="sxs-lookup"><span data-stu-id="b97d5-292">Remarks</span></span>

<span data-ttu-id="b97d5-293">Chaque forêt Active Directory contient un attribut DS-Heuristics qui contient des paramètres pour l’ensemble de la forêt.</span><span class="sxs-lookup"><span data-stu-id="b97d5-293">Each Active Directory forest contains a DS-Heuristics attribute that contains settings for the entire forest.</span></span> <span data-ttu-id="b97d5-294">L’attribut DS-Heuristics est un attribut de l’objet « CN = Directory Service, CN = Windows NT, CN = Services, CN = Configuration <Domain> ».</span><span class="sxs-lookup"><span data-stu-id="b97d5-294">The DS-Heuristics attribute is an attribute of the "CN=Directory Service,CN=Windows NT,CN=Services,CN=Configuration,<Domain>" object.</span></span>

<span data-ttu-id="b97d5-295">DS-Heuristics est une chaîne Unicode dans laquelle chaque caractère contient une valeur pour un seul paramètre à l’ensemble du domaine.</span><span class="sxs-lookup"><span data-stu-id="b97d5-295">DS-Heuristics is a Unicode string in which each character contains a value for a single domain-wide setting.</span></span> <span data-ttu-id="b97d5-296">La chaîne DS-Heuristics prend le format suivant.</span><span class="sxs-lookup"><span data-stu-id="b97d5-296">The DS-Heuristics string takes the following format.</span></span>

``` syntax
|<1>|<2>|<3>|<4>|<5>|<6>|<7>|<8>|<9>|<10>|<11>|<12>|<13>|<14>|<15>|<16>|<17>|<18>|<19>|<20>|<21>|<22>|<23>|<24>|<25>|
```

<span data-ttu-id="b97d5-297">Pour fournir la validation des données, chaque dixième caractère est défini sur le nombre de caractères divisé par dix.</span><span class="sxs-lookup"><span data-stu-id="b97d5-297">To provide data validation, each tenth character is set to the character number divided by ten.</span></span> <span data-ttu-id="b97d5-298">Par exemple, le dixième caractère est « 1 ». le vingtième caractère est « 2 », et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="b97d5-298">For example, the tenth character is '1'; the twentieth character is '2', and so on.</span></span>

<span data-ttu-id="b97d5-299">Tout caractère qui n’est pas défini est supposé être un « 0 ».</span><span class="sxs-lookup"><span data-stu-id="b97d5-299">Any character that is not set is assumed to be a '0'.</span></span> <span data-ttu-id="b97d5-300">Si l’attribut DS-Heuristics n’est pas défini, toutes les valeurs sont supposées être « 0 ».</span><span class="sxs-lookup"><span data-stu-id="b97d5-300">If the DS-Heuristics attribute is not set, all values are assumed to be '0'.</span></span> <span data-ttu-id="b97d5-301">Il y a actuellement 25 caractères en cours d’utilisation et il n’est pas nécessaire de remplir la chaîne pour remplir les 25 caractères.</span><span class="sxs-lookup"><span data-stu-id="b97d5-301">There are currently 25 characters being used and it is not necessary to pad the string to fill all 25 characters.</span></span> <span data-ttu-id="b97d5-302">Par exemple, si le caractère le plus élevé utilisé est 7, la chaîne « 0000002 » est acceptable.</span><span class="sxs-lookup"><span data-stu-id="b97d5-302">For example, if the highest character being used is 7, then the string "0000002" is acceptable.</span></span>

<span data-ttu-id="b97d5-303">Pour plus d’informations sur chaque caractère, consultez [dSHeuristics dans \[ MS-ADTS \] Active Directory spécification technique](/openspecs/windows_protocols/ms-adts/e5899be4-862e-496f-9a38-33950617d2c5).</span><span class="sxs-lookup"><span data-stu-id="b97d5-303">For details about each character, see [dSHeuristics in \[MS-ADTS\] Active Directory Technical Specification](/openspecs/windows_protocols/ms-adts/e5899be4-862e-496f-9a38-33950617d2c5).</span></span>

### <a name="anr-search-filters"></a><span data-ttu-id="b97d5-304">Filtres de recherche ANR</span><span class="sxs-lookup"><span data-stu-id="b97d5-304">ANR Search Filters</span></span>

<span data-ttu-id="b97d5-305">Les caractères 1, 2 et 4 sont utilisés pour modifier le comportement des filtres de recherche ANR.</span><span class="sxs-lookup"><span data-stu-id="b97d5-305">Characters 1, 2, and 4 are used to modify the behavior of ANR search filters.</span></span> <span data-ttu-id="b97d5-306">Si le caractère 1 est défini sur « 1 », l’expansion du filtre ANR pour inclure **GivenName**  -  **Surname** (lorsque l’espace est trouvé) est désactivée.</span><span class="sxs-lookup"><span data-stu-id="b97d5-306">If character 1 is set to '1', then the expansion of the ANR filter to include **GivenName** - **Surname** (when space is found) is disabled.</span></span> <span data-ttu-id="b97d5-307">Si le caractère 2 est défini sur « 1 », l’expansion du filtre ANR pour inclure **Surname**  -  **GivenName** est désactivée.</span><span class="sxs-lookup"><span data-stu-id="b97d5-307">If character 2 is set to '1', the expansion of the ANR filter to include **Surname** - **GivenName** is disabled.</span></span> <span data-ttu-id="b97d5-308">Si un espace incorporé est présent dans la chaîne de recherche, la chaîne recherchée est normalement divisée en deux chaînes, qui sont comparées par paire avec les attributs **GivenName** et **Surname** .</span><span class="sxs-lookup"><span data-stu-id="b97d5-308">If an embedded space is present in the search string, the search string will normally be divided into two strings, which are compared pair-wise against the **GivenName** and **Surname** attributes.</span></span> <span data-ttu-id="b97d5-309">Le fait de définir les caractères 1 et 2 sur « 1 » empêchera ces correspondances d’être tentées.</span><span class="sxs-lookup"><span data-stu-id="b97d5-309">Setting characters 1 and 2 to '1' will prevent those matches from being attempted.</span></span> <span data-ttu-id="b97d5-310">Cette correspondance peut être désactivée si l’administrateur est convaincu que les recherches de « Jeff Smith » sont toujours fournies sous la forme « Jeff Smith » et non « Smith, Jeff ».</span><span class="sxs-lookup"><span data-stu-id="b97d5-310">This matching might be disabled if the administrator is confident that searches for "Jeff Smith" would always be provided as "jeff smith" and not "smith, jeff".</span></span> <span data-ttu-id="b97d5-311">Normalement, une seule correspondance est supprimée, conformément à la Convention locale.</span><span class="sxs-lookup"><span data-stu-id="b97d5-311">Normally only one or the other match would be suppressed, according to local convention.</span></span>

<span data-ttu-id="b97d5-312">Si le caractère 4 est défini sur « 1 », Active Directory effectue une « résolution de surnom préventive ».</span><span class="sxs-lookup"><span data-stu-id="b97d5-312">If the character 4 is set to '1' then Active Directory will perform "pre-emptive nickname resolution".</span></span> <span data-ttu-id="b97d5-313">Autrement dit, si la chaîne recherchée correspond exactement au surnom d’un objet dans l’étendue de recherche, cet objet est retourné en tant que résultat de la recherche, et le reste de la fonction ANR est ignoré.</span><span class="sxs-lookup"><span data-stu-id="b97d5-313">That is, if the search string exactly matches the nickname of exactly one object in the search scope, that one object is returned as the result of the search, and the rest of ANR is skipped.</span></span> <span data-ttu-id="b97d5-314">Notez que, si le reste de la recherche ANR est disponible via LDAP, la résolution de surnom préventif (également appelée « alignement de surnom ») est disponible uniquement via MAPI.</span><span class="sxs-lookup"><span data-stu-id="b97d5-314">Note that while the rest of ANR searching is available through LDAP, pre-emptive nickname resolution (also known as "nickname snap") is available only through MAPI.</span></span>

## <a name="see-also"></a><span data-ttu-id="b97d5-315">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b97d5-315">See also</span></span>

<dl> <dt>

<span data-ttu-id="b97d5-316">[dSHeuristics dans \[ MS-ADTS \] Active Directory spécification technique](/openspecs/windows_protocols/ms-adts/e5899be4-862e-496f-9a38-33950617d2c5)</span><span class="sxs-lookup"><span data-stu-id="b97d5-316">[dSHeuristics in \[MS-ADTS\] Active Directory Technical Specification](/openspecs/windows_protocols/ms-adts/e5899be4-862e-496f-9a38-33950617d2c5)</span></span>
</dt> </dl>

 

