---
title: Active Directory-Core-Propagate-attribut de données
description: L’attribut DS-Core-Propagate-Data est destiné à un usage interne uniquement.
ms.assetid: 6483890a-b1ef-4c8d-941d-8f25f722a305
ms.tgt_platform: multiple
keywords:
- Schéma AD DS-Core-Propagate-attribut de données
- Schéma AD de l’attribut dSCorePropagationData
topic_type:
- apiref
api_name:
- DS-Core-Propagation-Data
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 324e3db3c71d11f47cb0a7afec875b9d129fa2d9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106514674"
---
# <a name="ds-core-propagation-data-attribute"></a><span data-ttu-id="e3d03-105">Active Directory-Core-Propagate-attribut de données</span><span class="sxs-lookup"><span data-stu-id="e3d03-105">DS-Core-Propagation-Data attribute</span></span>

<span data-ttu-id="e3d03-106">L’attribut **DS-Core-Propagate-Data** est destiné à un usage interne uniquement.</span><span class="sxs-lookup"><span data-stu-id="e3d03-106">The **DS-Core-Propagation-Data** attribute is for internal use only.</span></span>



| <span data-ttu-id="e3d03-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="e3d03-107">Entry</span></span> | <span data-ttu-id="e3d03-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="e3d03-108">Value</span></span> |
|-------------------|---------------------------------------------------------------|
| <span data-ttu-id="e3d03-109">CN</span><span class="sxs-lookup"><span data-stu-id="e3d03-109">CN</span></span>                | <span data-ttu-id="e3d03-110">DS-Core-propagation-données</span><span class="sxs-lookup"><span data-stu-id="e3d03-110">DS-Core-Propagation-Data</span></span>                                      |
| <span data-ttu-id="e3d03-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="e3d03-111">Ldap-Display-Name</span></span> | <span data-ttu-id="e3d03-112">dSCorePropagationData</span><span class="sxs-lookup"><span data-stu-id="e3d03-112">dSCorePropagationData</span></span>                                         |
| <span data-ttu-id="e3d03-113">Taille</span><span class="sxs-lookup"><span data-stu-id="e3d03-113">Size</span></span>              | \-                                                            |
| <span data-ttu-id="e3d03-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="e3d03-114">Update Privilege</span></span>  | \-                                                            |
| <span data-ttu-id="e3d03-115">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="e3d03-115">Update Frequency</span></span>  | \-                                                            |
| <span data-ttu-id="e3d03-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e3d03-116">Attribute-Id</span></span>      | <span data-ttu-id="e3d03-117">1.2.840.113556.1.4.1357</span><span class="sxs-lookup"><span data-stu-id="e3d03-117">1.2.840.113556.1.4.1357</span></span>                                       |
| <span data-ttu-id="e3d03-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="e3d03-118">System-Id-Guid</span></span>    | <span data-ttu-id="e3d03-119">d167aa4b-8b08-11d2-9939-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="e3d03-119">d167aa4b-8b08-11d2-9939-0000f87a57d4</span></span>                          |
| <span data-ttu-id="e3d03-120">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e3d03-120">Syntax</span></span>            | [<span data-ttu-id="e3d03-121">**String(Generalized-Time)**</span><span class="sxs-lookup"><span data-stu-id="e3d03-121">**String(Generalized-Time)**</span></span>](s-string-generalized-time.md) |



## <a name="implementations"></a><span data-ttu-id="e3d03-122">Implémentations</span><span class="sxs-lookup"><span data-stu-id="e3d03-122">Implementations</span></span>

-   [<span data-ttu-id="e3d03-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e3d03-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e3d03-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e3d03-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e3d03-125">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="e3d03-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="e3d03-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e3d03-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e3d03-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e3d03-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e3d03-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e3d03-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e3d03-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e3d03-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e3d03-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e3d03-130">Windows 2000 Server</span></span>



| <span data-ttu-id="e3d03-131">Entrée</span><span class="sxs-lookup"><span data-stu-id="e3d03-131">Entry</span></span> | <span data-ttu-id="e3d03-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="e3d03-132">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e3d03-133">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e3d03-133">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e3d03-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e3d03-134">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="e3d03-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="e3d03-135">System-Only</span></span>            | <span data-ttu-id="e3d03-136">Vrai</span><span class="sxs-lookup"><span data-stu-id="e3d03-136">True</span></span>                            |
| <span data-ttu-id="e3d03-137">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e3d03-137">Is-Single-Valued</span></span>       | <span data-ttu-id="e3d03-138">Faux</span><span class="sxs-lookup"><span data-stu-id="e3d03-138">False</span></span>                           |
| <span data-ttu-id="e3d03-139">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e3d03-139">Is Indexed</span></span>             | <span data-ttu-id="e3d03-140">Faux</span><span class="sxs-lookup"><span data-stu-id="e3d03-140">False</span></span>                           |
| <span data-ttu-id="e3d03-141">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e3d03-141">In Global Catalog</span></span>      | <span data-ttu-id="e3d03-142">Vrai</span><span class="sxs-lookup"><span data-stu-id="e3d03-142">True</span></span>                            |
| <span data-ttu-id="e3d03-143">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e3d03-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="e3d03-144">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e3d03-144">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e3d03-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e3d03-145">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e3d03-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e3d03-146">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e3d03-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e3d03-147">Search-Flags</span></span>           | <span data-ttu-id="e3d03-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e3d03-148">0x00000000</span></span>                      |
| <span data-ttu-id="e3d03-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e3d03-149">System-Flags</span></span>           | <span data-ttu-id="e3d03-150">0x00000013</span><span class="sxs-lookup"><span data-stu-id="e3d03-150">0x00000013</span></span>                      |
| <span data-ttu-id="e3d03-151">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e3d03-151">Classes used in</span></span>        | [<span data-ttu-id="e3d03-152">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="e3d03-152">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e3d03-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e3d03-153">Windows Server 2003</span></span>



| <span data-ttu-id="e3d03-154">Entrée</span><span class="sxs-lookup"><span data-stu-id="e3d03-154">Entry</span></span> | <span data-ttu-id="e3d03-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="e3d03-155">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e3d03-156">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e3d03-156">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e3d03-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e3d03-157">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="e3d03-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="e3d03-158">System-Only</span></span>            | <span data-ttu-id="e3d03-159">Vrai</span><span class="sxs-lookup"><span data-stu-id="e3d03-159">True</span></span>                            |
| <span data-ttu-id="e3d03-160">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e3d03-160">Is-Single-Valued</span></span>       | <span data-ttu-id="e3d03-161">Faux</span><span class="sxs-lookup"><span data-stu-id="e3d03-161">False</span></span>                           |
| <span data-ttu-id="e3d03-162">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e3d03-162">Is Indexed</span></span>             | <span data-ttu-id="e3d03-163">Faux</span><span class="sxs-lookup"><span data-stu-id="e3d03-163">False</span></span>                           |
| <span data-ttu-id="e3d03-164">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e3d03-164">In Global Catalog</span></span>      | <span data-ttu-id="e3d03-165">Vrai</span><span class="sxs-lookup"><span data-stu-id="e3d03-165">True</span></span>                            |
| <span data-ttu-id="e3d03-166">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e3d03-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="e3d03-167">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e3d03-167">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e3d03-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e3d03-168">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e3d03-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e3d03-169">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e3d03-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e3d03-170">Search-Flags</span></span>           | <span data-ttu-id="e3d03-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e3d03-171">0x00000000</span></span>                      |
| <span data-ttu-id="e3d03-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e3d03-172">System-Flags</span></span>           | <span data-ttu-id="e3d03-173">0x00000013</span><span class="sxs-lookup"><span data-stu-id="e3d03-173">0x00000013</span></span>                      |
| <span data-ttu-id="e3d03-174">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e3d03-174">Classes used in</span></span>        | [<span data-ttu-id="e3d03-175">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="e3d03-175">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="e3d03-176">ADAM</span><span class="sxs-lookup"><span data-stu-id="e3d03-176">ADAM</span></span>



| <span data-ttu-id="e3d03-177">Entrée</span><span class="sxs-lookup"><span data-stu-id="e3d03-177">Entry</span></span> | <span data-ttu-id="e3d03-178">Valeur</span><span class="sxs-lookup"><span data-stu-id="e3d03-178">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e3d03-179">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e3d03-179">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e3d03-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e3d03-180">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="e3d03-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="e3d03-181">System-Only</span></span>            | <span data-ttu-id="e3d03-182">Vrai</span><span class="sxs-lookup"><span data-stu-id="e3d03-182">True</span></span>                            |
| <span data-ttu-id="e3d03-183">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e3d03-183">Is-Single-Valued</span></span>       | <span data-ttu-id="e3d03-184">Faux</span><span class="sxs-lookup"><span data-stu-id="e3d03-184">False</span></span>                           |
| <span data-ttu-id="e3d03-185">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e3d03-185">Is Indexed</span></span>             | <span data-ttu-id="e3d03-186">Faux</span><span class="sxs-lookup"><span data-stu-id="e3d03-186">False</span></span>                           |
| <span data-ttu-id="e3d03-187">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e3d03-187">In Global Catalog</span></span>      | <span data-ttu-id="e3d03-188">Vrai</span><span class="sxs-lookup"><span data-stu-id="e3d03-188">True</span></span>                            |
| <span data-ttu-id="e3d03-189">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e3d03-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="e3d03-190">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e3d03-190">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e3d03-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e3d03-191">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e3d03-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e3d03-192">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e3d03-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e3d03-193">Search-Flags</span></span>           | <span data-ttu-id="e3d03-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e3d03-194">0x00000000</span></span>                      |
| <span data-ttu-id="e3d03-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e3d03-195">System-Flags</span></span>           | <span data-ttu-id="e3d03-196">0x00000013</span><span class="sxs-lookup"><span data-stu-id="e3d03-196">0x00000013</span></span>                      |
| <span data-ttu-id="e3d03-197">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e3d03-197">Classes used in</span></span>        | [<span data-ttu-id="e3d03-198">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="e3d03-198">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e3d03-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e3d03-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e3d03-200">Entrée</span><span class="sxs-lookup"><span data-stu-id="e3d03-200">Entry</span></span> | <span data-ttu-id="e3d03-201">Valeur</span><span class="sxs-lookup"><span data-stu-id="e3d03-201">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e3d03-202">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e3d03-202">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e3d03-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e3d03-203">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="e3d03-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="e3d03-204">System-Only</span></span>            | <span data-ttu-id="e3d03-205">Vrai</span><span class="sxs-lookup"><span data-stu-id="e3d03-205">True</span></span>                            |
| <span data-ttu-id="e3d03-206">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e3d03-206">Is-Single-Valued</span></span>       | <span data-ttu-id="e3d03-207">Faux</span><span class="sxs-lookup"><span data-stu-id="e3d03-207">False</span></span>                           |
| <span data-ttu-id="e3d03-208">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e3d03-208">Is Indexed</span></span>             | <span data-ttu-id="e3d03-209">Faux</span><span class="sxs-lookup"><span data-stu-id="e3d03-209">False</span></span>                           |
| <span data-ttu-id="e3d03-210">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e3d03-210">In Global Catalog</span></span>      | <span data-ttu-id="e3d03-211">Vrai</span><span class="sxs-lookup"><span data-stu-id="e3d03-211">True</span></span>                            |
| <span data-ttu-id="e3d03-212">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e3d03-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="e3d03-213">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e3d03-213">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e3d03-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e3d03-214">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e3d03-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e3d03-215">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e3d03-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e3d03-216">Search-Flags</span></span>           | <span data-ttu-id="e3d03-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e3d03-217">0x00000000</span></span>                      |
| <span data-ttu-id="e3d03-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e3d03-218">System-Flags</span></span>           | <span data-ttu-id="e3d03-219">0x00000013</span><span class="sxs-lookup"><span data-stu-id="e3d03-219">0x00000013</span></span>                      |
| <span data-ttu-id="e3d03-220">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e3d03-220">Classes used in</span></span>        | [<span data-ttu-id="e3d03-221">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="e3d03-221">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e3d03-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e3d03-222">Windows Server 2008</span></span>



| <span data-ttu-id="e3d03-223">Entrée</span><span class="sxs-lookup"><span data-stu-id="e3d03-223">Entry</span></span> | <span data-ttu-id="e3d03-224">Valeur</span><span class="sxs-lookup"><span data-stu-id="e3d03-224">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e3d03-225">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e3d03-225">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e3d03-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e3d03-226">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="e3d03-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="e3d03-227">System-Only</span></span>            | <span data-ttu-id="e3d03-228">Vrai</span><span class="sxs-lookup"><span data-stu-id="e3d03-228">True</span></span>                            |
| <span data-ttu-id="e3d03-229">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e3d03-229">Is-Single-Valued</span></span>       | <span data-ttu-id="e3d03-230">Faux</span><span class="sxs-lookup"><span data-stu-id="e3d03-230">False</span></span>                           |
| <span data-ttu-id="e3d03-231">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e3d03-231">Is Indexed</span></span>             | <span data-ttu-id="e3d03-232">Faux</span><span class="sxs-lookup"><span data-stu-id="e3d03-232">False</span></span>                           |
| <span data-ttu-id="e3d03-233">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e3d03-233">In Global Catalog</span></span>      | <span data-ttu-id="e3d03-234">Vrai</span><span class="sxs-lookup"><span data-stu-id="e3d03-234">True</span></span>                            |
| <span data-ttu-id="e3d03-235">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e3d03-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="e3d03-236">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e3d03-236">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e3d03-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e3d03-237">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e3d03-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e3d03-238">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e3d03-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e3d03-239">Search-Flags</span></span>           | <span data-ttu-id="e3d03-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e3d03-240">0x00000000</span></span>                      |
| <span data-ttu-id="e3d03-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e3d03-241">System-Flags</span></span>           | <span data-ttu-id="e3d03-242">0x00000013</span><span class="sxs-lookup"><span data-stu-id="e3d03-242">0x00000013</span></span>                      |
| <span data-ttu-id="e3d03-243">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e3d03-243">Classes used in</span></span>        | [<span data-ttu-id="e3d03-244">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="e3d03-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e3d03-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e3d03-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e3d03-246">Entrée</span><span class="sxs-lookup"><span data-stu-id="e3d03-246">Entry</span></span> | <span data-ttu-id="e3d03-247">Valeur</span><span class="sxs-lookup"><span data-stu-id="e3d03-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e3d03-248">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e3d03-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e3d03-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e3d03-249">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="e3d03-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="e3d03-250">System-Only</span></span>            | <span data-ttu-id="e3d03-251">Vrai</span><span class="sxs-lookup"><span data-stu-id="e3d03-251">True</span></span>                            |
| <span data-ttu-id="e3d03-252">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e3d03-252">Is-Single-Valued</span></span>       | <span data-ttu-id="e3d03-253">Faux</span><span class="sxs-lookup"><span data-stu-id="e3d03-253">False</span></span>                           |
| <span data-ttu-id="e3d03-254">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e3d03-254">Is Indexed</span></span>             | <span data-ttu-id="e3d03-255">Faux</span><span class="sxs-lookup"><span data-stu-id="e3d03-255">False</span></span>                           |
| <span data-ttu-id="e3d03-256">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e3d03-256">In Global Catalog</span></span>      | <span data-ttu-id="e3d03-257">Vrai</span><span class="sxs-lookup"><span data-stu-id="e3d03-257">True</span></span>                            |
| <span data-ttu-id="e3d03-258">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e3d03-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="e3d03-259">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e3d03-259">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e3d03-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e3d03-260">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e3d03-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e3d03-261">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e3d03-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e3d03-262">Search-Flags</span></span>           | <span data-ttu-id="e3d03-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e3d03-263">0x00000000</span></span>                      |
| <span data-ttu-id="e3d03-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e3d03-264">System-Flags</span></span>           | <span data-ttu-id="e3d03-265">0x00000013</span><span class="sxs-lookup"><span data-stu-id="e3d03-265">0x00000013</span></span>                      |
| <span data-ttu-id="e3d03-266">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e3d03-266">Classes used in</span></span>        | [<span data-ttu-id="e3d03-267">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="e3d03-267">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e3d03-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e3d03-268">Windows Server 2012</span></span>



| <span data-ttu-id="e3d03-269">Entrée</span><span class="sxs-lookup"><span data-stu-id="e3d03-269">Entry</span></span> | <span data-ttu-id="e3d03-270">Valeur</span><span class="sxs-lookup"><span data-stu-id="e3d03-270">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e3d03-271">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e3d03-271">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e3d03-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e3d03-272">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="e3d03-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="e3d03-273">System-Only</span></span>            | <span data-ttu-id="e3d03-274">Vrai</span><span class="sxs-lookup"><span data-stu-id="e3d03-274">True</span></span>                            |
| <span data-ttu-id="e3d03-275">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e3d03-275">Is-Single-Valued</span></span>       | <span data-ttu-id="e3d03-276">Faux</span><span class="sxs-lookup"><span data-stu-id="e3d03-276">False</span></span>                           |
| <span data-ttu-id="e3d03-277">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e3d03-277">Is Indexed</span></span>             | <span data-ttu-id="e3d03-278">Faux</span><span class="sxs-lookup"><span data-stu-id="e3d03-278">False</span></span>                           |
| <span data-ttu-id="e3d03-279">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e3d03-279">In Global Catalog</span></span>      | <span data-ttu-id="e3d03-280">Vrai</span><span class="sxs-lookup"><span data-stu-id="e3d03-280">True</span></span>                            |
| <span data-ttu-id="e3d03-281">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e3d03-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="e3d03-282">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e3d03-282">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e3d03-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e3d03-283">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e3d03-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e3d03-284">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e3d03-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e3d03-285">Search-Flags</span></span>           | <span data-ttu-id="e3d03-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e3d03-286">0x00000000</span></span>                      |
| <span data-ttu-id="e3d03-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e3d03-287">System-Flags</span></span>           | <span data-ttu-id="e3d03-288">0x00000013</span><span class="sxs-lookup"><span data-stu-id="e3d03-288">0x00000013</span></span>                      |
| <span data-ttu-id="e3d03-289">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e3d03-289">Classes used in</span></span>        | [<span data-ttu-id="e3d03-290">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="e3d03-290">**Top**</span></span>](c-top.md)<br/> |



 

 





