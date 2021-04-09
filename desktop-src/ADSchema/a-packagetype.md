---
title: Attribut Package-Type
description: Cet attribut décrit le type d’installation requis pour un package d’application, par exemple, MSI, EXE, CAB.
ms.assetid: 76505575-a2c9-4113-84ac-1d0689d9e0e4
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Package-Type
- Schéma AD de l’attribut packageType
topic_type:
- apiref
api_name:
- Package-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 325bb00484a3ee44cd23b98931c40fb440cdb3b1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107986"
---
# <a name="package-type-attribute"></a><span data-ttu-id="22196-105">Attribut Package-Type</span><span class="sxs-lookup"><span data-stu-id="22196-105">Package-Type attribute</span></span>

<span data-ttu-id="22196-106">Cet attribut décrit le type d’installation requis pour un package d’application, par exemple, MSI, EXE, CAB.</span><span class="sxs-lookup"><span data-stu-id="22196-106">This attribute describes the type of installation required for an application package, for example, MSI, EXE, CAB.</span></span>



| <span data-ttu-id="22196-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="22196-107">Entry</span></span> | <span data-ttu-id="22196-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="22196-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="22196-109">CN</span><span class="sxs-lookup"><span data-stu-id="22196-109">CN</span></span>                | <span data-ttu-id="22196-110">Package-Type</span><span class="sxs-lookup"><span data-stu-id="22196-110">Package-Type</span></span>                         |
| <span data-ttu-id="22196-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="22196-111">Ldap-Display-Name</span></span> | <span data-ttu-id="22196-112">packageType</span><span class="sxs-lookup"><span data-stu-id="22196-112">packageType</span></span>                          |
| <span data-ttu-id="22196-113">Taille</span><span class="sxs-lookup"><span data-stu-id="22196-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="22196-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="22196-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="22196-115">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="22196-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="22196-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="22196-116">Attribute-Id</span></span>      | <span data-ttu-id="22196-117">1.2.840.113556.1.4.324</span><span class="sxs-lookup"><span data-stu-id="22196-117">1.2.840.113556.1.4.324</span></span>               |
| <span data-ttu-id="22196-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="22196-118">System-Id-Guid</span></span>    | <span data-ttu-id="22196-119">7d6c0e96-7e20-11d0-afd6-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="22196-119">7d6c0e96-7e20-11d0-afd6-00c04fd930c9</span></span> |
| <span data-ttu-id="22196-120">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="22196-120">Syntax</span></span>            | [<span data-ttu-id="22196-121">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="22196-121">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="22196-122">Implémentations</span><span class="sxs-lookup"><span data-stu-id="22196-122">Implementations</span></span>

-   [<span data-ttu-id="22196-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="22196-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="22196-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="22196-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="22196-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="22196-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="22196-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="22196-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="22196-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="22196-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="22196-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="22196-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="22196-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="22196-129">Windows 2000 Server</span></span>



| <span data-ttu-id="22196-130">Entrée</span><span class="sxs-lookup"><span data-stu-id="22196-130">Entry</span></span> | <span data-ttu-id="22196-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="22196-131">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="22196-132">ID de lien</span><span class="sxs-lookup"><span data-stu-id="22196-132">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="22196-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="22196-133">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="22196-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="22196-134">System-Only</span></span>            | <span data-ttu-id="22196-135">Faux</span><span class="sxs-lookup"><span data-stu-id="22196-135">False</span></span>                                                            |
| <span data-ttu-id="22196-136">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="22196-136">Is-Single-Valued</span></span>       | <span data-ttu-id="22196-137">Vrai</span><span class="sxs-lookup"><span data-stu-id="22196-137">True</span></span>                                                             |
| <span data-ttu-id="22196-138">Est indexé</span><span class="sxs-lookup"><span data-stu-id="22196-138">Is Indexed</span></span>             | <span data-ttu-id="22196-139">Faux</span><span class="sxs-lookup"><span data-stu-id="22196-139">False</span></span>                                                            |
| <span data-ttu-id="22196-140">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="22196-140">In Global Catalog</span></span>      | <span data-ttu-id="22196-141">Faux</span><span class="sxs-lookup"><span data-stu-id="22196-141">False</span></span>                                                            |
| <span data-ttu-id="22196-142">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="22196-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="22196-143">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="22196-143">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="22196-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="22196-144">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="22196-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="22196-145">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="22196-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="22196-146">Search-Flags</span></span>           | <span data-ttu-id="22196-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="22196-147">0x00000000</span></span>                                                       |
| <span data-ttu-id="22196-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="22196-148">System-Flags</span></span>           | <span data-ttu-id="22196-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="22196-149">0x00000010</span></span>                                                       |
| <span data-ttu-id="22196-150">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="22196-150">Classes used in</span></span>        | [<span data-ttu-id="22196-151">**Inscription de packages**</span><span class="sxs-lookup"><span data-stu-id="22196-151">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="22196-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="22196-152">Windows Server 2003</span></span>



| <span data-ttu-id="22196-153">Entrée</span><span class="sxs-lookup"><span data-stu-id="22196-153">Entry</span></span> | <span data-ttu-id="22196-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="22196-154">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="22196-155">ID de lien</span><span class="sxs-lookup"><span data-stu-id="22196-155">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="22196-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="22196-156">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="22196-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="22196-157">System-Only</span></span>            | <span data-ttu-id="22196-158">Faux</span><span class="sxs-lookup"><span data-stu-id="22196-158">False</span></span>                                                            |
| <span data-ttu-id="22196-159">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="22196-159">Is-Single-Valued</span></span>       | <span data-ttu-id="22196-160">Vrai</span><span class="sxs-lookup"><span data-stu-id="22196-160">True</span></span>                                                             |
| <span data-ttu-id="22196-161">Est indexé</span><span class="sxs-lookup"><span data-stu-id="22196-161">Is Indexed</span></span>             | <span data-ttu-id="22196-162">Faux</span><span class="sxs-lookup"><span data-stu-id="22196-162">False</span></span>                                                            |
| <span data-ttu-id="22196-163">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="22196-163">In Global Catalog</span></span>      | <span data-ttu-id="22196-164">Faux</span><span class="sxs-lookup"><span data-stu-id="22196-164">False</span></span>                                                            |
| <span data-ttu-id="22196-165">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="22196-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="22196-166">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="22196-166">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="22196-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="22196-167">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="22196-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="22196-168">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="22196-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="22196-169">Search-Flags</span></span>           | <span data-ttu-id="22196-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="22196-170">0x00000000</span></span>                                                       |
| <span data-ttu-id="22196-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="22196-171">System-Flags</span></span>           | <span data-ttu-id="22196-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="22196-172">0x00000010</span></span>                                                       |
| <span data-ttu-id="22196-173">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="22196-173">Classes used in</span></span>        | [<span data-ttu-id="22196-174">**Inscription de packages**</span><span class="sxs-lookup"><span data-stu-id="22196-174">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="22196-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="22196-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="22196-176">Entrée</span><span class="sxs-lookup"><span data-stu-id="22196-176">Entry</span></span> | <span data-ttu-id="22196-177">Valeur</span><span class="sxs-lookup"><span data-stu-id="22196-177">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="22196-178">ID de lien</span><span class="sxs-lookup"><span data-stu-id="22196-178">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="22196-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="22196-179">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="22196-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="22196-180">System-Only</span></span>            | <span data-ttu-id="22196-181">Faux</span><span class="sxs-lookup"><span data-stu-id="22196-181">False</span></span>                                                            |
| <span data-ttu-id="22196-182">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="22196-182">Is-Single-Valued</span></span>       | <span data-ttu-id="22196-183">Vrai</span><span class="sxs-lookup"><span data-stu-id="22196-183">True</span></span>                                                             |
| <span data-ttu-id="22196-184">Est indexé</span><span class="sxs-lookup"><span data-stu-id="22196-184">Is Indexed</span></span>             | <span data-ttu-id="22196-185">Faux</span><span class="sxs-lookup"><span data-stu-id="22196-185">False</span></span>                                                            |
| <span data-ttu-id="22196-186">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="22196-186">In Global Catalog</span></span>      | <span data-ttu-id="22196-187">Faux</span><span class="sxs-lookup"><span data-stu-id="22196-187">False</span></span>                                                            |
| <span data-ttu-id="22196-188">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="22196-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="22196-189">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="22196-189">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="22196-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="22196-190">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="22196-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="22196-191">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="22196-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="22196-192">Search-Flags</span></span>           | <span data-ttu-id="22196-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="22196-193">0x00000000</span></span>                                                       |
| <span data-ttu-id="22196-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="22196-194">System-Flags</span></span>           | <span data-ttu-id="22196-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="22196-195">0x00000010</span></span>                                                       |
| <span data-ttu-id="22196-196">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="22196-196">Classes used in</span></span>        | [<span data-ttu-id="22196-197">**Inscription de packages**</span><span class="sxs-lookup"><span data-stu-id="22196-197">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="22196-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="22196-198">Windows Server 2008</span></span>



| <span data-ttu-id="22196-199">Entrée</span><span class="sxs-lookup"><span data-stu-id="22196-199">Entry</span></span> | <span data-ttu-id="22196-200">Valeur</span><span class="sxs-lookup"><span data-stu-id="22196-200">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="22196-201">ID de lien</span><span class="sxs-lookup"><span data-stu-id="22196-201">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="22196-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="22196-202">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="22196-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="22196-203">System-Only</span></span>            | <span data-ttu-id="22196-204">Faux</span><span class="sxs-lookup"><span data-stu-id="22196-204">False</span></span>                                                            |
| <span data-ttu-id="22196-205">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="22196-205">Is-Single-Valued</span></span>       | <span data-ttu-id="22196-206">Vrai</span><span class="sxs-lookup"><span data-stu-id="22196-206">True</span></span>                                                             |
| <span data-ttu-id="22196-207">Est indexé</span><span class="sxs-lookup"><span data-stu-id="22196-207">Is Indexed</span></span>             | <span data-ttu-id="22196-208">Faux</span><span class="sxs-lookup"><span data-stu-id="22196-208">False</span></span>                                                            |
| <span data-ttu-id="22196-209">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="22196-209">In Global Catalog</span></span>      | <span data-ttu-id="22196-210">Faux</span><span class="sxs-lookup"><span data-stu-id="22196-210">False</span></span>                                                            |
| <span data-ttu-id="22196-211">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="22196-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="22196-212">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="22196-212">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="22196-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="22196-213">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="22196-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="22196-214">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="22196-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="22196-215">Search-Flags</span></span>           | <span data-ttu-id="22196-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="22196-216">0x00000000</span></span>                                                       |
| <span data-ttu-id="22196-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="22196-217">System-Flags</span></span>           | <span data-ttu-id="22196-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="22196-218">0x00000010</span></span>                                                       |
| <span data-ttu-id="22196-219">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="22196-219">Classes used in</span></span>        | [<span data-ttu-id="22196-220">**Inscription de packages**</span><span class="sxs-lookup"><span data-stu-id="22196-220">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="22196-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="22196-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="22196-222">Entrée</span><span class="sxs-lookup"><span data-stu-id="22196-222">Entry</span></span> | <span data-ttu-id="22196-223">Valeur</span><span class="sxs-lookup"><span data-stu-id="22196-223">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="22196-224">ID de lien</span><span class="sxs-lookup"><span data-stu-id="22196-224">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="22196-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="22196-225">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="22196-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="22196-226">System-Only</span></span>            | <span data-ttu-id="22196-227">Faux</span><span class="sxs-lookup"><span data-stu-id="22196-227">False</span></span>                                                            |
| <span data-ttu-id="22196-228">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="22196-228">Is-Single-Valued</span></span>       | <span data-ttu-id="22196-229">Vrai</span><span class="sxs-lookup"><span data-stu-id="22196-229">True</span></span>                                                             |
| <span data-ttu-id="22196-230">Est indexé</span><span class="sxs-lookup"><span data-stu-id="22196-230">Is Indexed</span></span>             | <span data-ttu-id="22196-231">Faux</span><span class="sxs-lookup"><span data-stu-id="22196-231">False</span></span>                                                            |
| <span data-ttu-id="22196-232">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="22196-232">In Global Catalog</span></span>      | <span data-ttu-id="22196-233">Faux</span><span class="sxs-lookup"><span data-stu-id="22196-233">False</span></span>                                                            |
| <span data-ttu-id="22196-234">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="22196-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="22196-235">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="22196-235">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="22196-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="22196-236">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="22196-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="22196-237">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="22196-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="22196-238">Search-Flags</span></span>           | <span data-ttu-id="22196-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="22196-239">0x00000000</span></span>                                                       |
| <span data-ttu-id="22196-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="22196-240">System-Flags</span></span>           | <span data-ttu-id="22196-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="22196-241">0x00000010</span></span>                                                       |
| <span data-ttu-id="22196-242">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="22196-242">Classes used in</span></span>        | [<span data-ttu-id="22196-243">**Inscription de packages**</span><span class="sxs-lookup"><span data-stu-id="22196-243">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="22196-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="22196-244">Windows Server 2012</span></span>



| <span data-ttu-id="22196-245">Entrée</span><span class="sxs-lookup"><span data-stu-id="22196-245">Entry</span></span> | <span data-ttu-id="22196-246">Valeur</span><span class="sxs-lookup"><span data-stu-id="22196-246">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="22196-247">ID de lien</span><span class="sxs-lookup"><span data-stu-id="22196-247">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="22196-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="22196-248">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="22196-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="22196-249">System-Only</span></span>            | <span data-ttu-id="22196-250">Faux</span><span class="sxs-lookup"><span data-stu-id="22196-250">False</span></span>                                                            |
| <span data-ttu-id="22196-251">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="22196-251">Is-Single-Valued</span></span>       | <span data-ttu-id="22196-252">Vrai</span><span class="sxs-lookup"><span data-stu-id="22196-252">True</span></span>                                                             |
| <span data-ttu-id="22196-253">Est indexé</span><span class="sxs-lookup"><span data-stu-id="22196-253">Is Indexed</span></span>             | <span data-ttu-id="22196-254">Faux</span><span class="sxs-lookup"><span data-stu-id="22196-254">False</span></span>                                                            |
| <span data-ttu-id="22196-255">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="22196-255">In Global Catalog</span></span>      | <span data-ttu-id="22196-256">Faux</span><span class="sxs-lookup"><span data-stu-id="22196-256">False</span></span>                                                            |
| <span data-ttu-id="22196-257">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="22196-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="22196-258">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="22196-258">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="22196-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="22196-259">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="22196-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="22196-260">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="22196-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="22196-261">Search-Flags</span></span>           | <span data-ttu-id="22196-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="22196-262">0x00000000</span></span>                                                       |
| <span data-ttu-id="22196-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="22196-263">System-Flags</span></span>           | <span data-ttu-id="22196-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="22196-264">0x00000010</span></span>                                                       |
| <span data-ttu-id="22196-265">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="22196-265">Classes used in</span></span>        | [<span data-ttu-id="22196-266">**Inscription de packages**</span><span class="sxs-lookup"><span data-stu-id="22196-266">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



 

 





