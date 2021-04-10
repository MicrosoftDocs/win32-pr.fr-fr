---
title: ACS-attribut de bits d’autorisation
description: Autorise l’origine du transit de multidiffusion pour un utilisateur donné.
ms.assetid: c7e7866d-b906-4a64-bd51-4e9cc7b8fb86
ms.tgt_platform: multiple
keywords:
- ACS-schéma AD d’attribut de bits d’autorisation
- Schéma AD de l’attribut aCSPermissionBits
topic_type:
- apiref
api_name:
- ACS-Permission-Bits
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a27370178dd46fd50df44b1226686db5a70a846
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107323"
---
# <a name="acs-permission-bits-attribute"></a><span data-ttu-id="a2b9e-105">ACS-attribut de bits d’autorisation</span><span class="sxs-lookup"><span data-stu-id="a2b9e-105">ACS-Permission-Bits attribute</span></span>

<span data-ttu-id="a2b9e-106">Autorise l’origine du transit de multidiffusion pour un utilisateur donné.</span><span class="sxs-lookup"><span data-stu-id="a2b9e-106">Allows multicast flow origination for a given user.</span></span>



| <span data-ttu-id="a2b9e-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="a2b9e-107">Entry</span></span> | <span data-ttu-id="a2b9e-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="a2b9e-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="a2b9e-109">CN</span><span class="sxs-lookup"><span data-stu-id="a2b9e-109">CN</span></span>                | <span data-ttu-id="a2b9e-110">ACS-bits d’autorisation</span><span class="sxs-lookup"><span data-stu-id="a2b9e-110">ACS-Permission-Bits</span></span>                  |
| <span data-ttu-id="a2b9e-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="a2b9e-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a2b9e-112">aCSPermissionBits</span><span class="sxs-lookup"><span data-stu-id="a2b9e-112">aCSPermissionBits</span></span>                    |
| <span data-ttu-id="a2b9e-113">Taille</span><span class="sxs-lookup"><span data-stu-id="a2b9e-113">Size</span></span>              | <span data-ttu-id="a2b9e-114">8 octets</span><span class="sxs-lookup"><span data-stu-id="a2b9e-114">8 bytes</span></span>                              |
| <span data-ttu-id="a2b9e-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="a2b9e-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="a2b9e-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="a2b9e-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="a2b9e-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a2b9e-117">Attribute-Id</span></span>      | <span data-ttu-id="a2b9e-118">1.2.840.113556.1.4.765</span><span class="sxs-lookup"><span data-stu-id="a2b9e-118">1.2.840.113556.1.4.765</span></span>               |
| <span data-ttu-id="a2b9e-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a2b9e-119">System-Id-Guid</span></span>    | <span data-ttu-id="a2b9e-120">7f561282-5301-11d1-a9c5-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="a2b9e-120">7f561282-5301-11d1-a9c5-0000f80367c1</span></span> |
| <span data-ttu-id="a2b9e-121">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a2b9e-121">Syntax</span></span>            | [<span data-ttu-id="a2b9e-122">**Défini**</span><span class="sxs-lookup"><span data-stu-id="a2b9e-122">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="a2b9e-123">Implémentations</span><span class="sxs-lookup"><span data-stu-id="a2b9e-123">Implementations</span></span>

-   [<span data-ttu-id="a2b9e-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a2b9e-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a2b9e-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a2b9e-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a2b9e-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a2b9e-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a2b9e-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a2b9e-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a2b9e-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a2b9e-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a2b9e-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a2b9e-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a2b9e-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a2b9e-130">Windows 2000 Server</span></span>



| <span data-ttu-id="a2b9e-131">Entrée</span><span class="sxs-lookup"><span data-stu-id="a2b9e-131">Entry</span></span> | <span data-ttu-id="a2b9e-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="a2b9e-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a2b9e-133">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a2b9e-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a2b9e-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a2b9e-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a2b9e-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="a2b9e-135">System-Only</span></span>            | <span data-ttu-id="a2b9e-136">Faux</span><span class="sxs-lookup"><span data-stu-id="a2b9e-136">False</span></span>                                        |
| <span data-ttu-id="a2b9e-137">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a2b9e-137">Is-Single-Valued</span></span>       | <span data-ttu-id="a2b9e-138">Vrai</span><span class="sxs-lookup"><span data-stu-id="a2b9e-138">True</span></span>                                         |
| <span data-ttu-id="a2b9e-139">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a2b9e-139">Is Indexed</span></span>             | <span data-ttu-id="a2b9e-140">Faux</span><span class="sxs-lookup"><span data-stu-id="a2b9e-140">False</span></span>                                        |
| <span data-ttu-id="a2b9e-141">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a2b9e-141">In Global Catalog</span></span>      | <span data-ttu-id="a2b9e-142">Faux</span><span class="sxs-lookup"><span data-stu-id="a2b9e-142">False</span></span>                                        |
| <span data-ttu-id="a2b9e-143">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a2b9e-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="a2b9e-144">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a2b9e-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a2b9e-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a2b9e-145">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a2b9e-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a2b9e-146">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a2b9e-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a2b9e-147">Search-Flags</span></span>           | <span data-ttu-id="a2b9e-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a2b9e-148">0x00000000</span></span>                                   |
| <span data-ttu-id="a2b9e-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a2b9e-149">System-Flags</span></span>           | <span data-ttu-id="a2b9e-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a2b9e-150">0x00000010</span></span>                                   |
| <span data-ttu-id="a2b9e-151">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a2b9e-151">Classes used in</span></span>        | [<span data-ttu-id="a2b9e-152">**ACS-stratégie**</span><span class="sxs-lookup"><span data-stu-id="a2b9e-152">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a2b9e-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a2b9e-153">Windows Server 2003</span></span>



| <span data-ttu-id="a2b9e-154">Entrée</span><span class="sxs-lookup"><span data-stu-id="a2b9e-154">Entry</span></span> | <span data-ttu-id="a2b9e-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="a2b9e-155">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a2b9e-156">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a2b9e-156">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a2b9e-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a2b9e-157">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a2b9e-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="a2b9e-158">System-Only</span></span>            | <span data-ttu-id="a2b9e-159">Faux</span><span class="sxs-lookup"><span data-stu-id="a2b9e-159">False</span></span>                                        |
| <span data-ttu-id="a2b9e-160">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a2b9e-160">Is-Single-Valued</span></span>       | <span data-ttu-id="a2b9e-161">Vrai</span><span class="sxs-lookup"><span data-stu-id="a2b9e-161">True</span></span>                                         |
| <span data-ttu-id="a2b9e-162">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a2b9e-162">Is Indexed</span></span>             | <span data-ttu-id="a2b9e-163">Faux</span><span class="sxs-lookup"><span data-stu-id="a2b9e-163">False</span></span>                                        |
| <span data-ttu-id="a2b9e-164">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a2b9e-164">In Global Catalog</span></span>      | <span data-ttu-id="a2b9e-165">Faux</span><span class="sxs-lookup"><span data-stu-id="a2b9e-165">False</span></span>                                        |
| <span data-ttu-id="a2b9e-166">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a2b9e-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="a2b9e-167">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a2b9e-167">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a2b9e-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a2b9e-168">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a2b9e-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a2b9e-169">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a2b9e-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a2b9e-170">Search-Flags</span></span>           | <span data-ttu-id="a2b9e-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a2b9e-171">0x00000000</span></span>                                   |
| <span data-ttu-id="a2b9e-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a2b9e-172">System-Flags</span></span>           | <span data-ttu-id="a2b9e-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a2b9e-173">0x00000010</span></span>                                   |
| <span data-ttu-id="a2b9e-174">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a2b9e-174">Classes used in</span></span>        | [<span data-ttu-id="a2b9e-175">**ACS-stratégie**</span><span class="sxs-lookup"><span data-stu-id="a2b9e-175">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a2b9e-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a2b9e-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a2b9e-177">Entrée</span><span class="sxs-lookup"><span data-stu-id="a2b9e-177">Entry</span></span> | <span data-ttu-id="a2b9e-178">Valeur</span><span class="sxs-lookup"><span data-stu-id="a2b9e-178">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a2b9e-179">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a2b9e-179">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a2b9e-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a2b9e-180">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a2b9e-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="a2b9e-181">System-Only</span></span>            | <span data-ttu-id="a2b9e-182">Faux</span><span class="sxs-lookup"><span data-stu-id="a2b9e-182">False</span></span>                                        |
| <span data-ttu-id="a2b9e-183">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a2b9e-183">Is-Single-Valued</span></span>       | <span data-ttu-id="a2b9e-184">Vrai</span><span class="sxs-lookup"><span data-stu-id="a2b9e-184">True</span></span>                                         |
| <span data-ttu-id="a2b9e-185">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a2b9e-185">Is Indexed</span></span>             | <span data-ttu-id="a2b9e-186">Faux</span><span class="sxs-lookup"><span data-stu-id="a2b9e-186">False</span></span>                                        |
| <span data-ttu-id="a2b9e-187">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a2b9e-187">In Global Catalog</span></span>      | <span data-ttu-id="a2b9e-188">Faux</span><span class="sxs-lookup"><span data-stu-id="a2b9e-188">False</span></span>                                        |
| <span data-ttu-id="a2b9e-189">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a2b9e-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="a2b9e-190">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a2b9e-190">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a2b9e-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a2b9e-191">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a2b9e-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a2b9e-192">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a2b9e-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a2b9e-193">Search-Flags</span></span>           | <span data-ttu-id="a2b9e-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a2b9e-194">0x00000000</span></span>                                   |
| <span data-ttu-id="a2b9e-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a2b9e-195">System-Flags</span></span>           | <span data-ttu-id="a2b9e-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a2b9e-196">0x00000010</span></span>                                   |
| <span data-ttu-id="a2b9e-197">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a2b9e-197">Classes used in</span></span>        | [<span data-ttu-id="a2b9e-198">**ACS-stratégie**</span><span class="sxs-lookup"><span data-stu-id="a2b9e-198">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a2b9e-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a2b9e-199">Windows Server 2008</span></span>



| <span data-ttu-id="a2b9e-200">Entrée</span><span class="sxs-lookup"><span data-stu-id="a2b9e-200">Entry</span></span> | <span data-ttu-id="a2b9e-201">Valeur</span><span class="sxs-lookup"><span data-stu-id="a2b9e-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a2b9e-202">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a2b9e-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a2b9e-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a2b9e-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a2b9e-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="a2b9e-204">System-Only</span></span>            | <span data-ttu-id="a2b9e-205">Faux</span><span class="sxs-lookup"><span data-stu-id="a2b9e-205">False</span></span>                                        |
| <span data-ttu-id="a2b9e-206">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a2b9e-206">Is-Single-Valued</span></span>       | <span data-ttu-id="a2b9e-207">Vrai</span><span class="sxs-lookup"><span data-stu-id="a2b9e-207">True</span></span>                                         |
| <span data-ttu-id="a2b9e-208">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a2b9e-208">Is Indexed</span></span>             | <span data-ttu-id="a2b9e-209">Faux</span><span class="sxs-lookup"><span data-stu-id="a2b9e-209">False</span></span>                                        |
| <span data-ttu-id="a2b9e-210">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a2b9e-210">In Global Catalog</span></span>      | <span data-ttu-id="a2b9e-211">Faux</span><span class="sxs-lookup"><span data-stu-id="a2b9e-211">False</span></span>                                        |
| <span data-ttu-id="a2b9e-212">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a2b9e-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="a2b9e-213">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a2b9e-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a2b9e-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a2b9e-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a2b9e-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a2b9e-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a2b9e-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a2b9e-216">Search-Flags</span></span>           | <span data-ttu-id="a2b9e-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a2b9e-217">0x00000000</span></span>                                   |
| <span data-ttu-id="a2b9e-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a2b9e-218">System-Flags</span></span>           | <span data-ttu-id="a2b9e-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a2b9e-219">0x00000010</span></span>                                   |
| <span data-ttu-id="a2b9e-220">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a2b9e-220">Classes used in</span></span>        | [<span data-ttu-id="a2b9e-221">**ACS-stratégie**</span><span class="sxs-lookup"><span data-stu-id="a2b9e-221">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a2b9e-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a2b9e-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a2b9e-223">Entrée</span><span class="sxs-lookup"><span data-stu-id="a2b9e-223">Entry</span></span> | <span data-ttu-id="a2b9e-224">Valeur</span><span class="sxs-lookup"><span data-stu-id="a2b9e-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a2b9e-225">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a2b9e-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a2b9e-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a2b9e-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a2b9e-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="a2b9e-227">System-Only</span></span>            | <span data-ttu-id="a2b9e-228">Faux</span><span class="sxs-lookup"><span data-stu-id="a2b9e-228">False</span></span>                                        |
| <span data-ttu-id="a2b9e-229">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a2b9e-229">Is-Single-Valued</span></span>       | <span data-ttu-id="a2b9e-230">Vrai</span><span class="sxs-lookup"><span data-stu-id="a2b9e-230">True</span></span>                                         |
| <span data-ttu-id="a2b9e-231">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a2b9e-231">Is Indexed</span></span>             | <span data-ttu-id="a2b9e-232">Faux</span><span class="sxs-lookup"><span data-stu-id="a2b9e-232">False</span></span>                                        |
| <span data-ttu-id="a2b9e-233">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a2b9e-233">In Global Catalog</span></span>      | <span data-ttu-id="a2b9e-234">Faux</span><span class="sxs-lookup"><span data-stu-id="a2b9e-234">False</span></span>                                        |
| <span data-ttu-id="a2b9e-235">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a2b9e-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="a2b9e-236">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a2b9e-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a2b9e-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a2b9e-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a2b9e-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a2b9e-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a2b9e-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a2b9e-239">Search-Flags</span></span>           | <span data-ttu-id="a2b9e-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a2b9e-240">0x00000000</span></span>                                   |
| <span data-ttu-id="a2b9e-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a2b9e-241">System-Flags</span></span>           | <span data-ttu-id="a2b9e-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a2b9e-242">0x00000010</span></span>                                   |
| <span data-ttu-id="a2b9e-243">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a2b9e-243">Classes used in</span></span>        | [<span data-ttu-id="a2b9e-244">**ACS-stratégie**</span><span class="sxs-lookup"><span data-stu-id="a2b9e-244">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a2b9e-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a2b9e-245">Windows Server 2012</span></span>



| <span data-ttu-id="a2b9e-246">Entrée</span><span class="sxs-lookup"><span data-stu-id="a2b9e-246">Entry</span></span> | <span data-ttu-id="a2b9e-247">Valeur</span><span class="sxs-lookup"><span data-stu-id="a2b9e-247">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a2b9e-248">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a2b9e-248">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a2b9e-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a2b9e-249">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a2b9e-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="a2b9e-250">System-Only</span></span>            | <span data-ttu-id="a2b9e-251">Faux</span><span class="sxs-lookup"><span data-stu-id="a2b9e-251">False</span></span>                                        |
| <span data-ttu-id="a2b9e-252">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a2b9e-252">Is-Single-Valued</span></span>       | <span data-ttu-id="a2b9e-253">Vrai</span><span class="sxs-lookup"><span data-stu-id="a2b9e-253">True</span></span>                                         |
| <span data-ttu-id="a2b9e-254">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a2b9e-254">Is Indexed</span></span>             | <span data-ttu-id="a2b9e-255">Faux</span><span class="sxs-lookup"><span data-stu-id="a2b9e-255">False</span></span>                                        |
| <span data-ttu-id="a2b9e-256">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a2b9e-256">In Global Catalog</span></span>      | <span data-ttu-id="a2b9e-257">Faux</span><span class="sxs-lookup"><span data-stu-id="a2b9e-257">False</span></span>                                        |
| <span data-ttu-id="a2b9e-258">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a2b9e-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="a2b9e-259">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a2b9e-259">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a2b9e-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a2b9e-260">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a2b9e-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a2b9e-261">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a2b9e-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a2b9e-262">Search-Flags</span></span>           | <span data-ttu-id="a2b9e-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a2b9e-263">0x00000000</span></span>                                   |
| <span data-ttu-id="a2b9e-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a2b9e-264">System-Flags</span></span>           | <span data-ttu-id="a2b9e-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a2b9e-265">0x00000010</span></span>                                   |
| <span data-ttu-id="a2b9e-266">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a2b9e-266">Classes used in</span></span>        | [<span data-ttu-id="a2b9e-267">**ACS-stratégie**</span><span class="sxs-lookup"><span data-stu-id="a2b9e-267">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



 

 





