---
title: Attribut Reps-From
description: Répertorie les serveurs à partir desquels l’annuaire accepte les modifications pour le contexte d’appellation défini.
ms.assetid: 2e18410b-d383-4838-aeaf-dd479be5f44d
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Reps-From
- Schéma AD de l’attribut repsFrom
topic_type:
- apiref
api_name:
- Reps-From
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc6981b71b6ec251eb27af0e7570fe1558d1ff20
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106515705"
---
# <a name="reps-from-attribute"></a><span data-ttu-id="7e97c-105">Attribut Reps-From</span><span class="sxs-lookup"><span data-stu-id="7e97c-105">Reps-From attribute</span></span>

<span data-ttu-id="7e97c-106">Répertorie les serveurs à partir desquels l’annuaire accepte les modifications pour le contexte d’appellation défini.</span><span class="sxs-lookup"><span data-stu-id="7e97c-106">Lists the servers from which the directory will accept changes for the defined naming context.</span></span>



| <span data-ttu-id="7e97c-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="7e97c-107">Entry</span></span> | <span data-ttu-id="7e97c-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="7e97c-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="7e97c-109">CN</span><span class="sxs-lookup"><span data-stu-id="7e97c-109">CN</span></span>                | <span data-ttu-id="7e97c-110">Reps-From</span><span class="sxs-lookup"><span data-stu-id="7e97c-110">Reps-From</span></span>                                             |
| <span data-ttu-id="7e97c-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="7e97c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="7e97c-112">repsFrom</span><span class="sxs-lookup"><span data-stu-id="7e97c-112">repsFrom</span></span>                                              |
| <span data-ttu-id="7e97c-113">Taille</span><span class="sxs-lookup"><span data-stu-id="7e97c-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="7e97c-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="7e97c-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="7e97c-115">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="7e97c-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="7e97c-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7e97c-116">Attribute-Id</span></span>      | <span data-ttu-id="7e97c-117">1.2.840.113556.1.2.91</span><span class="sxs-lookup"><span data-stu-id="7e97c-117">1.2.840.113556.1.2.91</span></span>                                 |
| <span data-ttu-id="7e97c-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="7e97c-118">System-Id-Guid</span></span>    | <span data-ttu-id="7e97c-119">bf967a1d-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="7e97c-119">bf967a1d-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="7e97c-120">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7e97c-120">Syntax</span></span>            | [<span data-ttu-id="7e97c-121">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="7e97c-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="7e97c-122">Implémentations</span><span class="sxs-lookup"><span data-stu-id="7e97c-122">Implementations</span></span>

-   [<span data-ttu-id="7e97c-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7e97c-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7e97c-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7e97c-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7e97c-125">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="7e97c-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="7e97c-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7e97c-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7e97c-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7e97c-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7e97c-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7e97c-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7e97c-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7e97c-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7e97c-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7e97c-130">Windows 2000 Server</span></span>



| <span data-ttu-id="7e97c-131">Entrée</span><span class="sxs-lookup"><span data-stu-id="7e97c-131">Entry</span></span> | <span data-ttu-id="7e97c-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="7e97c-132">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7e97c-133">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7e97c-133">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7e97c-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e97c-134">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="7e97c-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e97c-135">System-Only</span></span>            | <span data-ttu-id="7e97c-136">Vrai</span><span class="sxs-lookup"><span data-stu-id="7e97c-136">True</span></span>                            |
| <span data-ttu-id="7e97c-137">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7e97c-137">Is-Single-Valued</span></span>       | <span data-ttu-id="7e97c-138">Faux</span><span class="sxs-lookup"><span data-stu-id="7e97c-138">False</span></span>                           |
| <span data-ttu-id="7e97c-139">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7e97c-139">Is Indexed</span></span>             | <span data-ttu-id="7e97c-140">Faux</span><span class="sxs-lookup"><span data-stu-id="7e97c-140">False</span></span>                           |
| <span data-ttu-id="7e97c-141">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7e97c-141">In Global Catalog</span></span>      | <span data-ttu-id="7e97c-142">Vrai</span><span class="sxs-lookup"><span data-stu-id="7e97c-142">True</span></span>                            |
| <span data-ttu-id="7e97c-143">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7e97c-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e97c-144">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7e97c-144">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7e97c-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e97c-145">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7e97c-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e97c-146">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7e97c-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e97c-147">Search-Flags</span></span>           | <span data-ttu-id="7e97c-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e97c-148">0x00000000</span></span>                      |
| <span data-ttu-id="7e97c-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e97c-149">System-Flags</span></span>           | <span data-ttu-id="7e97c-150">0x00000013</span><span class="sxs-lookup"><span data-stu-id="7e97c-150">0x00000013</span></span>                      |
| <span data-ttu-id="7e97c-151">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7e97c-151">Classes used in</span></span>        | [<span data-ttu-id="7e97c-152">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="7e97c-152">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7e97c-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7e97c-153">Windows Server 2003</span></span>



| <span data-ttu-id="7e97c-154">Entrée</span><span class="sxs-lookup"><span data-stu-id="7e97c-154">Entry</span></span> | <span data-ttu-id="7e97c-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="7e97c-155">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7e97c-156">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7e97c-156">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7e97c-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e97c-157">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="7e97c-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e97c-158">System-Only</span></span>            | <span data-ttu-id="7e97c-159">Vrai</span><span class="sxs-lookup"><span data-stu-id="7e97c-159">True</span></span>                            |
| <span data-ttu-id="7e97c-160">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7e97c-160">Is-Single-Valued</span></span>       | <span data-ttu-id="7e97c-161">Faux</span><span class="sxs-lookup"><span data-stu-id="7e97c-161">False</span></span>                           |
| <span data-ttu-id="7e97c-162">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7e97c-162">Is Indexed</span></span>             | <span data-ttu-id="7e97c-163">Faux</span><span class="sxs-lookup"><span data-stu-id="7e97c-163">False</span></span>                           |
| <span data-ttu-id="7e97c-164">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7e97c-164">In Global Catalog</span></span>      | <span data-ttu-id="7e97c-165">Vrai</span><span class="sxs-lookup"><span data-stu-id="7e97c-165">True</span></span>                            |
| <span data-ttu-id="7e97c-166">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7e97c-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e97c-167">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7e97c-167">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7e97c-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e97c-168">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7e97c-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e97c-169">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7e97c-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e97c-170">Search-Flags</span></span>           | <span data-ttu-id="7e97c-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e97c-171">0x00000000</span></span>                      |
| <span data-ttu-id="7e97c-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e97c-172">System-Flags</span></span>           | <span data-ttu-id="7e97c-173">0x00000013</span><span class="sxs-lookup"><span data-stu-id="7e97c-173">0x00000013</span></span>                      |
| <span data-ttu-id="7e97c-174">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7e97c-174">Classes used in</span></span>        | [<span data-ttu-id="7e97c-175">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="7e97c-175">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="7e97c-176">ADAM</span><span class="sxs-lookup"><span data-stu-id="7e97c-176">ADAM</span></span>



| <span data-ttu-id="7e97c-177">Entrée</span><span class="sxs-lookup"><span data-stu-id="7e97c-177">Entry</span></span> | <span data-ttu-id="7e97c-178">Valeur</span><span class="sxs-lookup"><span data-stu-id="7e97c-178">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7e97c-179">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7e97c-179">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7e97c-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e97c-180">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="7e97c-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e97c-181">System-Only</span></span>            | <span data-ttu-id="7e97c-182">Vrai</span><span class="sxs-lookup"><span data-stu-id="7e97c-182">True</span></span>                            |
| <span data-ttu-id="7e97c-183">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7e97c-183">Is-Single-Valued</span></span>       | <span data-ttu-id="7e97c-184">Faux</span><span class="sxs-lookup"><span data-stu-id="7e97c-184">False</span></span>                           |
| <span data-ttu-id="7e97c-185">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7e97c-185">Is Indexed</span></span>             | <span data-ttu-id="7e97c-186">Faux</span><span class="sxs-lookup"><span data-stu-id="7e97c-186">False</span></span>                           |
| <span data-ttu-id="7e97c-187">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7e97c-187">In Global Catalog</span></span>      | <span data-ttu-id="7e97c-188">Vrai</span><span class="sxs-lookup"><span data-stu-id="7e97c-188">True</span></span>                            |
| <span data-ttu-id="7e97c-189">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7e97c-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e97c-190">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7e97c-190">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7e97c-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e97c-191">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7e97c-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e97c-192">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7e97c-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e97c-193">Search-Flags</span></span>           | <span data-ttu-id="7e97c-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e97c-194">0x00000000</span></span>                      |
| <span data-ttu-id="7e97c-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e97c-195">System-Flags</span></span>           | <span data-ttu-id="7e97c-196">0x00000013</span><span class="sxs-lookup"><span data-stu-id="7e97c-196">0x00000013</span></span>                      |
| <span data-ttu-id="7e97c-197">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7e97c-197">Classes used in</span></span>        | [<span data-ttu-id="7e97c-198">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="7e97c-198">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7e97c-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7e97c-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7e97c-200">Entrée</span><span class="sxs-lookup"><span data-stu-id="7e97c-200">Entry</span></span> | <span data-ttu-id="7e97c-201">Valeur</span><span class="sxs-lookup"><span data-stu-id="7e97c-201">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7e97c-202">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7e97c-202">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7e97c-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e97c-203">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="7e97c-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e97c-204">System-Only</span></span>            | <span data-ttu-id="7e97c-205">Vrai</span><span class="sxs-lookup"><span data-stu-id="7e97c-205">True</span></span>                            |
| <span data-ttu-id="7e97c-206">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7e97c-206">Is-Single-Valued</span></span>       | <span data-ttu-id="7e97c-207">Faux</span><span class="sxs-lookup"><span data-stu-id="7e97c-207">False</span></span>                           |
| <span data-ttu-id="7e97c-208">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7e97c-208">Is Indexed</span></span>             | <span data-ttu-id="7e97c-209">Faux</span><span class="sxs-lookup"><span data-stu-id="7e97c-209">False</span></span>                           |
| <span data-ttu-id="7e97c-210">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7e97c-210">In Global Catalog</span></span>      | <span data-ttu-id="7e97c-211">Vrai</span><span class="sxs-lookup"><span data-stu-id="7e97c-211">True</span></span>                            |
| <span data-ttu-id="7e97c-212">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7e97c-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e97c-213">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7e97c-213">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7e97c-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e97c-214">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7e97c-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e97c-215">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7e97c-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e97c-216">Search-Flags</span></span>           | <span data-ttu-id="7e97c-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e97c-217">0x00000000</span></span>                      |
| <span data-ttu-id="7e97c-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e97c-218">System-Flags</span></span>           | <span data-ttu-id="7e97c-219">0x00000013</span><span class="sxs-lookup"><span data-stu-id="7e97c-219">0x00000013</span></span>                      |
| <span data-ttu-id="7e97c-220">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7e97c-220">Classes used in</span></span>        | [<span data-ttu-id="7e97c-221">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="7e97c-221">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7e97c-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7e97c-222">Windows Server 2008</span></span>



| <span data-ttu-id="7e97c-223">Entrée</span><span class="sxs-lookup"><span data-stu-id="7e97c-223">Entry</span></span> | <span data-ttu-id="7e97c-224">Valeur</span><span class="sxs-lookup"><span data-stu-id="7e97c-224">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7e97c-225">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7e97c-225">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7e97c-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e97c-226">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="7e97c-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e97c-227">System-Only</span></span>            | <span data-ttu-id="7e97c-228">Vrai</span><span class="sxs-lookup"><span data-stu-id="7e97c-228">True</span></span>                            |
| <span data-ttu-id="7e97c-229">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7e97c-229">Is-Single-Valued</span></span>       | <span data-ttu-id="7e97c-230">Faux</span><span class="sxs-lookup"><span data-stu-id="7e97c-230">False</span></span>                           |
| <span data-ttu-id="7e97c-231">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7e97c-231">Is Indexed</span></span>             | <span data-ttu-id="7e97c-232">Faux</span><span class="sxs-lookup"><span data-stu-id="7e97c-232">False</span></span>                           |
| <span data-ttu-id="7e97c-233">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7e97c-233">In Global Catalog</span></span>      | <span data-ttu-id="7e97c-234">Vrai</span><span class="sxs-lookup"><span data-stu-id="7e97c-234">True</span></span>                            |
| <span data-ttu-id="7e97c-235">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7e97c-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e97c-236">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7e97c-236">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7e97c-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e97c-237">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7e97c-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e97c-238">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7e97c-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e97c-239">Search-Flags</span></span>           | <span data-ttu-id="7e97c-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e97c-240">0x00000000</span></span>                      |
| <span data-ttu-id="7e97c-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e97c-241">System-Flags</span></span>           | <span data-ttu-id="7e97c-242">0x00000013</span><span class="sxs-lookup"><span data-stu-id="7e97c-242">0x00000013</span></span>                      |
| <span data-ttu-id="7e97c-243">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7e97c-243">Classes used in</span></span>        | [<span data-ttu-id="7e97c-244">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="7e97c-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7e97c-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7e97c-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7e97c-246">Entrée</span><span class="sxs-lookup"><span data-stu-id="7e97c-246">Entry</span></span> | <span data-ttu-id="7e97c-247">Valeur</span><span class="sxs-lookup"><span data-stu-id="7e97c-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7e97c-248">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7e97c-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7e97c-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e97c-249">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="7e97c-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e97c-250">System-Only</span></span>            | <span data-ttu-id="7e97c-251">Vrai</span><span class="sxs-lookup"><span data-stu-id="7e97c-251">True</span></span>                            |
| <span data-ttu-id="7e97c-252">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7e97c-252">Is-Single-Valued</span></span>       | <span data-ttu-id="7e97c-253">Faux</span><span class="sxs-lookup"><span data-stu-id="7e97c-253">False</span></span>                           |
| <span data-ttu-id="7e97c-254">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7e97c-254">Is Indexed</span></span>             | <span data-ttu-id="7e97c-255">Faux</span><span class="sxs-lookup"><span data-stu-id="7e97c-255">False</span></span>                           |
| <span data-ttu-id="7e97c-256">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7e97c-256">In Global Catalog</span></span>      | <span data-ttu-id="7e97c-257">Vrai</span><span class="sxs-lookup"><span data-stu-id="7e97c-257">True</span></span>                            |
| <span data-ttu-id="7e97c-258">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7e97c-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e97c-259">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7e97c-259">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7e97c-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e97c-260">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7e97c-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e97c-261">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7e97c-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e97c-262">Search-Flags</span></span>           | <span data-ttu-id="7e97c-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e97c-263">0x00000000</span></span>                      |
| <span data-ttu-id="7e97c-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e97c-264">System-Flags</span></span>           | <span data-ttu-id="7e97c-265">0x00000013</span><span class="sxs-lookup"><span data-stu-id="7e97c-265">0x00000013</span></span>                      |
| <span data-ttu-id="7e97c-266">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7e97c-266">Classes used in</span></span>        | [<span data-ttu-id="7e97c-267">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="7e97c-267">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7e97c-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7e97c-268">Windows Server 2012</span></span>



| <span data-ttu-id="7e97c-269">Entrée</span><span class="sxs-lookup"><span data-stu-id="7e97c-269">Entry</span></span> | <span data-ttu-id="7e97c-270">Valeur</span><span class="sxs-lookup"><span data-stu-id="7e97c-270">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7e97c-271">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7e97c-271">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7e97c-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e97c-272">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="7e97c-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e97c-273">System-Only</span></span>            | <span data-ttu-id="7e97c-274">Vrai</span><span class="sxs-lookup"><span data-stu-id="7e97c-274">True</span></span>                            |
| <span data-ttu-id="7e97c-275">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7e97c-275">Is-Single-Valued</span></span>       | <span data-ttu-id="7e97c-276">Faux</span><span class="sxs-lookup"><span data-stu-id="7e97c-276">False</span></span>                           |
| <span data-ttu-id="7e97c-277">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7e97c-277">Is Indexed</span></span>             | <span data-ttu-id="7e97c-278">Faux</span><span class="sxs-lookup"><span data-stu-id="7e97c-278">False</span></span>                           |
| <span data-ttu-id="7e97c-279">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7e97c-279">In Global Catalog</span></span>      | <span data-ttu-id="7e97c-280">Vrai</span><span class="sxs-lookup"><span data-stu-id="7e97c-280">True</span></span>                            |
| <span data-ttu-id="7e97c-281">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7e97c-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e97c-282">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7e97c-282">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7e97c-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e97c-283">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7e97c-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e97c-284">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7e97c-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e97c-285">Search-Flags</span></span>           | <span data-ttu-id="7e97c-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e97c-286">0x00000000</span></span>                      |
| <span data-ttu-id="7e97c-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e97c-287">System-Flags</span></span>           | <span data-ttu-id="7e97c-288">0x00000013</span><span class="sxs-lookup"><span data-stu-id="7e97c-288">0x00000013</span></span>                      |
| <span data-ttu-id="7e97c-289">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7e97c-289">Classes used in</span></span>        | [<span data-ttu-id="7e97c-290">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="7e97c-290">**Top**</span></span>](c-top.md)<br/> |



 

 





