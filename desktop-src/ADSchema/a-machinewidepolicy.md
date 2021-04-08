---
title: Attribut de stratégie à l’ensemble de l’ordinateur
description: Utilisé pour répliquer la stratégie extensible par l’utilisateur sur les clients.
ms.assetid: e8ce40b8-7658-4e4b-b0e1-b68031811dd1
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut de stratégie à l’ensemble de la machine
- Schéma AD de l’attribut machineWidePolicy
topic_type:
- apiref
api_name:
- Machine-Wide-Policy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dd3af77dfb501000369b3c4ae23b3f5f64f0da9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103943034"
---
# <a name="machine-wide-policy-attribute"></a><span data-ttu-id="990c2-105">Attribut de stratégie à l’ensemble de l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="990c2-105">Machine-Wide-Policy attribute</span></span>

<span data-ttu-id="990c2-106">Utilisé pour répliquer la stratégie extensible par l’utilisateur sur les clients.</span><span class="sxs-lookup"><span data-stu-id="990c2-106">Used to replicate the user-extensible policy to the clients.</span></span>



| <span data-ttu-id="990c2-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="990c2-107">Entry</span></span> | <span data-ttu-id="990c2-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="990c2-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="990c2-109">CN</span><span class="sxs-lookup"><span data-stu-id="990c2-109">CN</span></span>                | <span data-ttu-id="990c2-110">Stratégie à l’ensemble de l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="990c2-110">Machine-Wide-Policy</span></span>                                   |
| <span data-ttu-id="990c2-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="990c2-111">Ldap-Display-Name</span></span> | <span data-ttu-id="990c2-112">machineWidePolicy</span><span class="sxs-lookup"><span data-stu-id="990c2-112">machineWidePolicy</span></span>                                     |
| <span data-ttu-id="990c2-113">Taille</span><span class="sxs-lookup"><span data-stu-id="990c2-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="990c2-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="990c2-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="990c2-115">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="990c2-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="990c2-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="990c2-116">Attribute-Id</span></span>      | <span data-ttu-id="990c2-117">1.2.840.113556.1.4.459</span><span class="sxs-lookup"><span data-stu-id="990c2-117">1.2.840.113556.1.4.459</span></span>                                |
| <span data-ttu-id="990c2-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="990c2-118">System-Id-Guid</span></span>    | <span data-ttu-id="990c2-119">80a67e4f-9f22-11d0-afdd-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="990c2-119">80a67e4f-9f22-11d0-afdd-00c04fd930c9</span></span>                  |
| <span data-ttu-id="990c2-120">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="990c2-120">Syntax</span></span>            | [<span data-ttu-id="990c2-121">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="990c2-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="990c2-122">Implémentations</span><span class="sxs-lookup"><span data-stu-id="990c2-122">Implementations</span></span>

-   [<span data-ttu-id="990c2-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="990c2-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="990c2-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="990c2-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="990c2-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="990c2-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="990c2-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="990c2-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="990c2-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="990c2-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="990c2-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="990c2-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="990c2-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="990c2-129">Windows 2000 Server</span></span>



| <span data-ttu-id="990c2-130">Entrée</span><span class="sxs-lookup"><span data-stu-id="990c2-130">Entry</span></span> | <span data-ttu-id="990c2-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="990c2-131">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="990c2-132">ID de lien</span><span class="sxs-lookup"><span data-stu-id="990c2-132">Link-Id</span></span>                | \-           |
| <span data-ttu-id="990c2-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="990c2-133">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="990c2-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="990c2-134">System-Only</span></span>            | <span data-ttu-id="990c2-135">Faux</span><span class="sxs-lookup"><span data-stu-id="990c2-135">False</span></span>        |
| <span data-ttu-id="990c2-136">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="990c2-136">Is-Single-Valued</span></span>       | <span data-ttu-id="990c2-137">Faux</span><span class="sxs-lookup"><span data-stu-id="990c2-137">False</span></span>        |
| <span data-ttu-id="990c2-138">Est indexé</span><span class="sxs-lookup"><span data-stu-id="990c2-138">Is Indexed</span></span>             | <span data-ttu-id="990c2-139">Faux</span><span class="sxs-lookup"><span data-stu-id="990c2-139">False</span></span>        |
| <span data-ttu-id="990c2-140">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="990c2-140">In Global Catalog</span></span>      | <span data-ttu-id="990c2-141">Faux</span><span class="sxs-lookup"><span data-stu-id="990c2-141">False</span></span>        |
| <span data-ttu-id="990c2-142">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="990c2-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="990c2-143">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="990c2-143">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="990c2-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="990c2-144">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="990c2-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="990c2-145">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="990c2-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="990c2-146">Search-Flags</span></span>           | <span data-ttu-id="990c2-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="990c2-147">0x00000000</span></span>   |
| <span data-ttu-id="990c2-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="990c2-148">System-Flags</span></span>           | <span data-ttu-id="990c2-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="990c2-149">0x00000010</span></span>   |
| <span data-ttu-id="990c2-150">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="990c2-150">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003"></a><span data-ttu-id="990c2-151">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="990c2-151">Windows Server 2003</span></span>



| <span data-ttu-id="990c2-152">Entrée</span><span class="sxs-lookup"><span data-stu-id="990c2-152">Entry</span></span> | <span data-ttu-id="990c2-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="990c2-153">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="990c2-154">ID de lien</span><span class="sxs-lookup"><span data-stu-id="990c2-154">Link-Id</span></span>                | \-           |
| <span data-ttu-id="990c2-155">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="990c2-155">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="990c2-156">System-Only</span><span class="sxs-lookup"><span data-stu-id="990c2-156">System-Only</span></span>            | <span data-ttu-id="990c2-157">Faux</span><span class="sxs-lookup"><span data-stu-id="990c2-157">False</span></span>        |
| <span data-ttu-id="990c2-158">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="990c2-158">Is-Single-Valued</span></span>       | <span data-ttu-id="990c2-159">Faux</span><span class="sxs-lookup"><span data-stu-id="990c2-159">False</span></span>        |
| <span data-ttu-id="990c2-160">Est indexé</span><span class="sxs-lookup"><span data-stu-id="990c2-160">Is Indexed</span></span>             | <span data-ttu-id="990c2-161">Faux</span><span class="sxs-lookup"><span data-stu-id="990c2-161">False</span></span>        |
| <span data-ttu-id="990c2-162">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="990c2-162">In Global Catalog</span></span>      | <span data-ttu-id="990c2-163">Faux</span><span class="sxs-lookup"><span data-stu-id="990c2-163">False</span></span>        |
| <span data-ttu-id="990c2-164">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="990c2-164">NT-Security-Descriptor</span></span> | <span data-ttu-id="990c2-165">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="990c2-165">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="990c2-166">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="990c2-166">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="990c2-167">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="990c2-167">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="990c2-168">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="990c2-168">Search-Flags</span></span>           | <span data-ttu-id="990c2-169">0x00000000</span><span class="sxs-lookup"><span data-stu-id="990c2-169">0x00000000</span></span>   |
| <span data-ttu-id="990c2-170">System-Flags</span><span class="sxs-lookup"><span data-stu-id="990c2-170">System-Flags</span></span>           | <span data-ttu-id="990c2-171">0x00000010</span><span class="sxs-lookup"><span data-stu-id="990c2-171">0x00000010</span></span>   |
| <span data-ttu-id="990c2-172">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="990c2-172">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="990c2-173">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="990c2-173">Windows Server 2003 R2</span></span>



| <span data-ttu-id="990c2-174">Entrée</span><span class="sxs-lookup"><span data-stu-id="990c2-174">Entry</span></span> | <span data-ttu-id="990c2-175">Valeur</span><span class="sxs-lookup"><span data-stu-id="990c2-175">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="990c2-176">ID de lien</span><span class="sxs-lookup"><span data-stu-id="990c2-176">Link-Id</span></span>                | \-           |
| <span data-ttu-id="990c2-177">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="990c2-177">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="990c2-178">System-Only</span><span class="sxs-lookup"><span data-stu-id="990c2-178">System-Only</span></span>            | <span data-ttu-id="990c2-179">Faux</span><span class="sxs-lookup"><span data-stu-id="990c2-179">False</span></span>        |
| <span data-ttu-id="990c2-180">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="990c2-180">Is-Single-Valued</span></span>       | <span data-ttu-id="990c2-181">Faux</span><span class="sxs-lookup"><span data-stu-id="990c2-181">False</span></span>        |
| <span data-ttu-id="990c2-182">Est indexé</span><span class="sxs-lookup"><span data-stu-id="990c2-182">Is Indexed</span></span>             | <span data-ttu-id="990c2-183">Faux</span><span class="sxs-lookup"><span data-stu-id="990c2-183">False</span></span>        |
| <span data-ttu-id="990c2-184">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="990c2-184">In Global Catalog</span></span>      | <span data-ttu-id="990c2-185">Faux</span><span class="sxs-lookup"><span data-stu-id="990c2-185">False</span></span>        |
| <span data-ttu-id="990c2-186">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="990c2-186">NT-Security-Descriptor</span></span> | <span data-ttu-id="990c2-187">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="990c2-187">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="990c2-188">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="990c2-188">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="990c2-189">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="990c2-189">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="990c2-190">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="990c2-190">Search-Flags</span></span>           | <span data-ttu-id="990c2-191">0x00000000</span><span class="sxs-lookup"><span data-stu-id="990c2-191">0x00000000</span></span>   |
| <span data-ttu-id="990c2-192">System-Flags</span><span class="sxs-lookup"><span data-stu-id="990c2-192">System-Flags</span></span>           | <span data-ttu-id="990c2-193">0x00000010</span><span class="sxs-lookup"><span data-stu-id="990c2-193">0x00000010</span></span>   |
| <span data-ttu-id="990c2-194">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="990c2-194">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008"></a><span data-ttu-id="990c2-195">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="990c2-195">Windows Server 2008</span></span>



| <span data-ttu-id="990c2-196">Entrée</span><span class="sxs-lookup"><span data-stu-id="990c2-196">Entry</span></span> | <span data-ttu-id="990c2-197">Valeur</span><span class="sxs-lookup"><span data-stu-id="990c2-197">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="990c2-198">ID de lien</span><span class="sxs-lookup"><span data-stu-id="990c2-198">Link-Id</span></span>                | \-           |
| <span data-ttu-id="990c2-199">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="990c2-199">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="990c2-200">System-Only</span><span class="sxs-lookup"><span data-stu-id="990c2-200">System-Only</span></span>            | <span data-ttu-id="990c2-201">Faux</span><span class="sxs-lookup"><span data-stu-id="990c2-201">False</span></span>        |
| <span data-ttu-id="990c2-202">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="990c2-202">Is-Single-Valued</span></span>       | <span data-ttu-id="990c2-203">Faux</span><span class="sxs-lookup"><span data-stu-id="990c2-203">False</span></span>        |
| <span data-ttu-id="990c2-204">Est indexé</span><span class="sxs-lookup"><span data-stu-id="990c2-204">Is Indexed</span></span>             | <span data-ttu-id="990c2-205">Faux</span><span class="sxs-lookup"><span data-stu-id="990c2-205">False</span></span>        |
| <span data-ttu-id="990c2-206">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="990c2-206">In Global Catalog</span></span>      | <span data-ttu-id="990c2-207">Faux</span><span class="sxs-lookup"><span data-stu-id="990c2-207">False</span></span>        |
| <span data-ttu-id="990c2-208">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="990c2-208">NT-Security-Descriptor</span></span> | <span data-ttu-id="990c2-209">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="990c2-209">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="990c2-210">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="990c2-210">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="990c2-211">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="990c2-211">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="990c2-212">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="990c2-212">Search-Flags</span></span>           | <span data-ttu-id="990c2-213">0x00000000</span><span class="sxs-lookup"><span data-stu-id="990c2-213">0x00000000</span></span>   |
| <span data-ttu-id="990c2-214">System-Flags</span><span class="sxs-lookup"><span data-stu-id="990c2-214">System-Flags</span></span>           | <span data-ttu-id="990c2-215">0x00000010</span><span class="sxs-lookup"><span data-stu-id="990c2-215">0x00000010</span></span>   |
| <span data-ttu-id="990c2-216">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="990c2-216">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="990c2-217">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="990c2-217">Windows Server 2008 R2</span></span>



| <span data-ttu-id="990c2-218">Entrée</span><span class="sxs-lookup"><span data-stu-id="990c2-218">Entry</span></span> | <span data-ttu-id="990c2-219">Valeur</span><span class="sxs-lookup"><span data-stu-id="990c2-219">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="990c2-220">ID de lien</span><span class="sxs-lookup"><span data-stu-id="990c2-220">Link-Id</span></span>                | \-           |
| <span data-ttu-id="990c2-221">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="990c2-221">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="990c2-222">System-Only</span><span class="sxs-lookup"><span data-stu-id="990c2-222">System-Only</span></span>            | <span data-ttu-id="990c2-223">Faux</span><span class="sxs-lookup"><span data-stu-id="990c2-223">False</span></span>        |
| <span data-ttu-id="990c2-224">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="990c2-224">Is-Single-Valued</span></span>       | <span data-ttu-id="990c2-225">Faux</span><span class="sxs-lookup"><span data-stu-id="990c2-225">False</span></span>        |
| <span data-ttu-id="990c2-226">Est indexé</span><span class="sxs-lookup"><span data-stu-id="990c2-226">Is Indexed</span></span>             | <span data-ttu-id="990c2-227">Faux</span><span class="sxs-lookup"><span data-stu-id="990c2-227">False</span></span>        |
| <span data-ttu-id="990c2-228">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="990c2-228">In Global Catalog</span></span>      | <span data-ttu-id="990c2-229">Faux</span><span class="sxs-lookup"><span data-stu-id="990c2-229">False</span></span>        |
| <span data-ttu-id="990c2-230">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="990c2-230">NT-Security-Descriptor</span></span> | <span data-ttu-id="990c2-231">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="990c2-231">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="990c2-232">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="990c2-232">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="990c2-233">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="990c2-233">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="990c2-234">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="990c2-234">Search-Flags</span></span>           | <span data-ttu-id="990c2-235">0x00000000</span><span class="sxs-lookup"><span data-stu-id="990c2-235">0x00000000</span></span>   |
| <span data-ttu-id="990c2-236">System-Flags</span><span class="sxs-lookup"><span data-stu-id="990c2-236">System-Flags</span></span>           | <span data-ttu-id="990c2-237">0x00000010</span><span class="sxs-lookup"><span data-stu-id="990c2-237">0x00000010</span></span>   |
| <span data-ttu-id="990c2-238">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="990c2-238">Classes used in</span></span>        | \-           |



## <a name="windows-server-2012"></a><span data-ttu-id="990c2-239">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="990c2-239">Windows Server 2012</span></span>



| <span data-ttu-id="990c2-240">Entrée</span><span class="sxs-lookup"><span data-stu-id="990c2-240">Entry</span></span> | <span data-ttu-id="990c2-241">Valeur</span><span class="sxs-lookup"><span data-stu-id="990c2-241">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="990c2-242">ID de lien</span><span class="sxs-lookup"><span data-stu-id="990c2-242">Link-Id</span></span>                | \-           |
| <span data-ttu-id="990c2-243">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="990c2-243">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="990c2-244">System-Only</span><span class="sxs-lookup"><span data-stu-id="990c2-244">System-Only</span></span>            | <span data-ttu-id="990c2-245">Faux</span><span class="sxs-lookup"><span data-stu-id="990c2-245">False</span></span>        |
| <span data-ttu-id="990c2-246">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="990c2-246">Is-Single-Valued</span></span>       | <span data-ttu-id="990c2-247">Faux</span><span class="sxs-lookup"><span data-stu-id="990c2-247">False</span></span>        |
| <span data-ttu-id="990c2-248">Est indexé</span><span class="sxs-lookup"><span data-stu-id="990c2-248">Is Indexed</span></span>             | <span data-ttu-id="990c2-249">Faux</span><span class="sxs-lookup"><span data-stu-id="990c2-249">False</span></span>        |
| <span data-ttu-id="990c2-250">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="990c2-250">In Global Catalog</span></span>      | <span data-ttu-id="990c2-251">Faux</span><span class="sxs-lookup"><span data-stu-id="990c2-251">False</span></span>        |
| <span data-ttu-id="990c2-252">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="990c2-252">NT-Security-Descriptor</span></span> | <span data-ttu-id="990c2-253">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="990c2-253">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="990c2-254">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="990c2-254">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="990c2-255">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="990c2-255">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="990c2-256">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="990c2-256">Search-Flags</span></span>           | <span data-ttu-id="990c2-257">0x00000000</span><span class="sxs-lookup"><span data-stu-id="990c2-257">0x00000000</span></span>   |
| <span data-ttu-id="990c2-258">System-Flags</span><span class="sxs-lookup"><span data-stu-id="990c2-258">System-Flags</span></span>           | <span data-ttu-id="990c2-259">0x00000010</span><span class="sxs-lookup"><span data-stu-id="990c2-259">0x00000010</span></span>   |
| <span data-ttu-id="990c2-260">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="990c2-260">Classes used in</span></span>        | \-           |



 

 




