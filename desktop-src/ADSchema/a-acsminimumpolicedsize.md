---
title: ACS-attribut de taille minimale de police
description: L’attribut ACS-minimum-policiers-Size est destiné à un usage interne uniquement.
ms.assetid: 27b4273a-a625-430b-baa0-a6037e2aac1e
ms.tgt_platform: multiple
keywords:
- ACS-schéma AD d’attribut de taille minimale en police
- Schéma AD de l’attribut aCSMinimumPolicedSize
topic_type:
- apiref
api_name:
- ACS-Minimum-Policed-Size
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3de4bb2b33a45ab7d10bad72ba286d1695b980a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106536934"
---
# <a name="acs-minimum-policed-size-attribute"></a><span data-ttu-id="c23c1-105">ACS-attribut de taille minimale de police</span><span class="sxs-lookup"><span data-stu-id="c23c1-105">ACS-Minimum-Policed-Size attribute</span></span>

<span data-ttu-id="c23c1-106">L’attribut **ACS-minimum-policiers-Size** est destiné à un usage interne uniquement.</span><span class="sxs-lookup"><span data-stu-id="c23c1-106">The **ACS-Minimum-Policed-Size** attribute is for internal use only.</span></span> <span data-ttu-id="c23c1-107">Basé sur RFC2210.</span><span class="sxs-lookup"><span data-stu-id="c23c1-107">Based on RFC2210.</span></span>



| <span data-ttu-id="c23c1-108">Entrée</span><span class="sxs-lookup"><span data-stu-id="c23c1-108">Entry</span></span> | <span data-ttu-id="c23c1-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="c23c1-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="c23c1-110">CN</span><span class="sxs-lookup"><span data-stu-id="c23c1-110">CN</span></span>                | <span data-ttu-id="c23c1-111">ACS-taille minimale de la police</span><span class="sxs-lookup"><span data-stu-id="c23c1-111">ACS-Minimum-Policed-Size</span></span>             |
| <span data-ttu-id="c23c1-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="c23c1-112">Ldap-Display-Name</span></span> | <span data-ttu-id="c23c1-113">aCSMinimumPolicedSize</span><span class="sxs-lookup"><span data-stu-id="c23c1-113">aCSMinimumPolicedSize</span></span>                |
| <span data-ttu-id="c23c1-114">Taille</span><span class="sxs-lookup"><span data-stu-id="c23c1-114">Size</span></span>              | <span data-ttu-id="c23c1-115">8 octets</span><span class="sxs-lookup"><span data-stu-id="c23c1-115">8 bytes</span></span>                              |
| <span data-ttu-id="c23c1-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="c23c1-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="c23c1-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="c23c1-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="c23c1-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c23c1-118">Attribute-Id</span></span>      | <span data-ttu-id="c23c1-119">1.2.840.113556.1.4.1315</span><span class="sxs-lookup"><span data-stu-id="c23c1-119">1.2.840.113556.1.4.1315</span></span>              |
| <span data-ttu-id="c23c1-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c23c1-120">System-Id-Guid</span></span>    | <span data-ttu-id="c23c1-121">8d0e7195-3b90-11d2-90cc-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="c23c1-121">8d0e7195-3b90-11d2-90cc-00c04fd91ab1</span></span> |
| <span data-ttu-id="c23c1-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c23c1-122">Syntax</span></span>            | [<span data-ttu-id="c23c1-123">**Défini**</span><span class="sxs-lookup"><span data-stu-id="c23c1-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="c23c1-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="c23c1-124">Implementations</span></span>

-   [<span data-ttu-id="c23c1-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c23c1-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c23c1-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c23c1-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c23c1-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c23c1-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c23c1-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c23c1-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c23c1-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c23c1-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c23c1-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c23c1-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c23c1-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c23c1-131">Windows 2000 Server</span></span>



| <span data-ttu-id="c23c1-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="c23c1-132">Entry</span></span> | <span data-ttu-id="c23c1-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="c23c1-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="c23c1-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c23c1-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="c23c1-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c23c1-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="c23c1-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="c23c1-136">System-Only</span></span>            | <span data-ttu-id="c23c1-137">Faux</span><span class="sxs-lookup"><span data-stu-id="c23c1-137">False</span></span>                                        |
| <span data-ttu-id="c23c1-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c23c1-138">Is-Single-Valued</span></span>       | <span data-ttu-id="c23c1-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="c23c1-139">True</span></span>                                         |
| <span data-ttu-id="c23c1-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c23c1-140">Is Indexed</span></span>             | <span data-ttu-id="c23c1-141">Faux</span><span class="sxs-lookup"><span data-stu-id="c23c1-141">False</span></span>                                        |
| <span data-ttu-id="c23c1-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c23c1-142">In Global Catalog</span></span>      | <span data-ttu-id="c23c1-143">Faux</span><span class="sxs-lookup"><span data-stu-id="c23c1-143">False</span></span>                                        |
| <span data-ttu-id="c23c1-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c23c1-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="c23c1-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c23c1-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="c23c1-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c23c1-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="c23c1-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c23c1-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="c23c1-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c23c1-148">Search-Flags</span></span>           | <span data-ttu-id="c23c1-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c23c1-149">0x00000000</span></span>                                   |
| <span data-ttu-id="c23c1-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c23c1-150">System-Flags</span></span>           | <span data-ttu-id="c23c1-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c23c1-151">0x00000010</span></span>                                   |
| <span data-ttu-id="c23c1-152">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c23c1-152">Classes used in</span></span>        | [<span data-ttu-id="c23c1-153">**ACS-stratégie**</span><span class="sxs-lookup"><span data-stu-id="c23c1-153">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c23c1-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c23c1-154">Windows Server 2003</span></span>



| <span data-ttu-id="c23c1-155">Entrée</span><span class="sxs-lookup"><span data-stu-id="c23c1-155">Entry</span></span> | <span data-ttu-id="c23c1-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="c23c1-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="c23c1-157">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c23c1-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="c23c1-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c23c1-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="c23c1-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="c23c1-159">System-Only</span></span>            | <span data-ttu-id="c23c1-160">Faux</span><span class="sxs-lookup"><span data-stu-id="c23c1-160">False</span></span>                                        |
| <span data-ttu-id="c23c1-161">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c23c1-161">Is-Single-Valued</span></span>       | <span data-ttu-id="c23c1-162">Vrai</span><span class="sxs-lookup"><span data-stu-id="c23c1-162">True</span></span>                                         |
| <span data-ttu-id="c23c1-163">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c23c1-163">Is Indexed</span></span>             | <span data-ttu-id="c23c1-164">Faux</span><span class="sxs-lookup"><span data-stu-id="c23c1-164">False</span></span>                                        |
| <span data-ttu-id="c23c1-165">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c23c1-165">In Global Catalog</span></span>      | <span data-ttu-id="c23c1-166">Faux</span><span class="sxs-lookup"><span data-stu-id="c23c1-166">False</span></span>                                        |
| <span data-ttu-id="c23c1-167">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c23c1-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="c23c1-168">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c23c1-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="c23c1-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c23c1-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="c23c1-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c23c1-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="c23c1-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c23c1-171">Search-Flags</span></span>           | <span data-ttu-id="c23c1-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c23c1-172">0x00000000</span></span>                                   |
| <span data-ttu-id="c23c1-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c23c1-173">System-Flags</span></span>           | <span data-ttu-id="c23c1-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c23c1-174">0x00000010</span></span>                                   |
| <span data-ttu-id="c23c1-175">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c23c1-175">Classes used in</span></span>        | [<span data-ttu-id="c23c1-176">**ACS-stratégie**</span><span class="sxs-lookup"><span data-stu-id="c23c1-176">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c23c1-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c23c1-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c23c1-178">Entrée</span><span class="sxs-lookup"><span data-stu-id="c23c1-178">Entry</span></span> | <span data-ttu-id="c23c1-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="c23c1-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="c23c1-180">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c23c1-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="c23c1-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c23c1-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="c23c1-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="c23c1-182">System-Only</span></span>            | <span data-ttu-id="c23c1-183">Faux</span><span class="sxs-lookup"><span data-stu-id="c23c1-183">False</span></span>                                        |
| <span data-ttu-id="c23c1-184">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c23c1-184">Is-Single-Valued</span></span>       | <span data-ttu-id="c23c1-185">Vrai</span><span class="sxs-lookup"><span data-stu-id="c23c1-185">True</span></span>                                         |
| <span data-ttu-id="c23c1-186">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c23c1-186">Is Indexed</span></span>             | <span data-ttu-id="c23c1-187">Faux</span><span class="sxs-lookup"><span data-stu-id="c23c1-187">False</span></span>                                        |
| <span data-ttu-id="c23c1-188">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c23c1-188">In Global Catalog</span></span>      | <span data-ttu-id="c23c1-189">Faux</span><span class="sxs-lookup"><span data-stu-id="c23c1-189">False</span></span>                                        |
| <span data-ttu-id="c23c1-190">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c23c1-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="c23c1-191">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c23c1-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="c23c1-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c23c1-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="c23c1-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c23c1-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="c23c1-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c23c1-194">Search-Flags</span></span>           | <span data-ttu-id="c23c1-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c23c1-195">0x00000000</span></span>                                   |
| <span data-ttu-id="c23c1-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c23c1-196">System-Flags</span></span>           | <span data-ttu-id="c23c1-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c23c1-197">0x00000010</span></span>                                   |
| <span data-ttu-id="c23c1-198">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c23c1-198">Classes used in</span></span>        | [<span data-ttu-id="c23c1-199">**ACS-stratégie**</span><span class="sxs-lookup"><span data-stu-id="c23c1-199">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c23c1-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c23c1-200">Windows Server 2008</span></span>



| <span data-ttu-id="c23c1-201">Entrée</span><span class="sxs-lookup"><span data-stu-id="c23c1-201">Entry</span></span> | <span data-ttu-id="c23c1-202">Valeur</span><span class="sxs-lookup"><span data-stu-id="c23c1-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="c23c1-203">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c23c1-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="c23c1-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c23c1-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="c23c1-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="c23c1-205">System-Only</span></span>            | <span data-ttu-id="c23c1-206">Faux</span><span class="sxs-lookup"><span data-stu-id="c23c1-206">False</span></span>                                        |
| <span data-ttu-id="c23c1-207">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c23c1-207">Is-Single-Valued</span></span>       | <span data-ttu-id="c23c1-208">Vrai</span><span class="sxs-lookup"><span data-stu-id="c23c1-208">True</span></span>                                         |
| <span data-ttu-id="c23c1-209">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c23c1-209">Is Indexed</span></span>             | <span data-ttu-id="c23c1-210">Faux</span><span class="sxs-lookup"><span data-stu-id="c23c1-210">False</span></span>                                        |
| <span data-ttu-id="c23c1-211">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c23c1-211">In Global Catalog</span></span>      | <span data-ttu-id="c23c1-212">Faux</span><span class="sxs-lookup"><span data-stu-id="c23c1-212">False</span></span>                                        |
| <span data-ttu-id="c23c1-213">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c23c1-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="c23c1-214">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c23c1-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="c23c1-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c23c1-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="c23c1-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c23c1-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="c23c1-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c23c1-217">Search-Flags</span></span>           | <span data-ttu-id="c23c1-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c23c1-218">0x00000000</span></span>                                   |
| <span data-ttu-id="c23c1-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c23c1-219">System-Flags</span></span>           | <span data-ttu-id="c23c1-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c23c1-220">0x00000010</span></span>                                   |
| <span data-ttu-id="c23c1-221">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c23c1-221">Classes used in</span></span>        | [<span data-ttu-id="c23c1-222">**ACS-stratégie**</span><span class="sxs-lookup"><span data-stu-id="c23c1-222">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c23c1-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c23c1-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c23c1-224">Entrée</span><span class="sxs-lookup"><span data-stu-id="c23c1-224">Entry</span></span> | <span data-ttu-id="c23c1-225">Valeur</span><span class="sxs-lookup"><span data-stu-id="c23c1-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="c23c1-226">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c23c1-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="c23c1-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c23c1-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="c23c1-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="c23c1-228">System-Only</span></span>            | <span data-ttu-id="c23c1-229">Faux</span><span class="sxs-lookup"><span data-stu-id="c23c1-229">False</span></span>                                        |
| <span data-ttu-id="c23c1-230">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c23c1-230">Is-Single-Valued</span></span>       | <span data-ttu-id="c23c1-231">Vrai</span><span class="sxs-lookup"><span data-stu-id="c23c1-231">True</span></span>                                         |
| <span data-ttu-id="c23c1-232">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c23c1-232">Is Indexed</span></span>             | <span data-ttu-id="c23c1-233">Faux</span><span class="sxs-lookup"><span data-stu-id="c23c1-233">False</span></span>                                        |
| <span data-ttu-id="c23c1-234">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c23c1-234">In Global Catalog</span></span>      | <span data-ttu-id="c23c1-235">Faux</span><span class="sxs-lookup"><span data-stu-id="c23c1-235">False</span></span>                                        |
| <span data-ttu-id="c23c1-236">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c23c1-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="c23c1-237">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c23c1-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="c23c1-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c23c1-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="c23c1-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c23c1-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="c23c1-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c23c1-240">Search-Flags</span></span>           | <span data-ttu-id="c23c1-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c23c1-241">0x00000000</span></span>                                   |
| <span data-ttu-id="c23c1-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c23c1-242">System-Flags</span></span>           | <span data-ttu-id="c23c1-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c23c1-243">0x00000010</span></span>                                   |
| <span data-ttu-id="c23c1-244">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c23c1-244">Classes used in</span></span>        | [<span data-ttu-id="c23c1-245">**ACS-stratégie**</span><span class="sxs-lookup"><span data-stu-id="c23c1-245">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c23c1-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c23c1-246">Windows Server 2012</span></span>



| <span data-ttu-id="c23c1-247">Entrée</span><span class="sxs-lookup"><span data-stu-id="c23c1-247">Entry</span></span> | <span data-ttu-id="c23c1-248">Valeur</span><span class="sxs-lookup"><span data-stu-id="c23c1-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="c23c1-249">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c23c1-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="c23c1-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c23c1-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="c23c1-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="c23c1-251">System-Only</span></span>            | <span data-ttu-id="c23c1-252">Faux</span><span class="sxs-lookup"><span data-stu-id="c23c1-252">False</span></span>                                        |
| <span data-ttu-id="c23c1-253">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c23c1-253">Is-Single-Valued</span></span>       | <span data-ttu-id="c23c1-254">Vrai</span><span class="sxs-lookup"><span data-stu-id="c23c1-254">True</span></span>                                         |
| <span data-ttu-id="c23c1-255">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c23c1-255">Is Indexed</span></span>             | <span data-ttu-id="c23c1-256">Faux</span><span class="sxs-lookup"><span data-stu-id="c23c1-256">False</span></span>                                        |
| <span data-ttu-id="c23c1-257">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c23c1-257">In Global Catalog</span></span>      | <span data-ttu-id="c23c1-258">Faux</span><span class="sxs-lookup"><span data-stu-id="c23c1-258">False</span></span>                                        |
| <span data-ttu-id="c23c1-259">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c23c1-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="c23c1-260">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c23c1-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="c23c1-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c23c1-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="c23c1-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c23c1-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="c23c1-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c23c1-263">Search-Flags</span></span>           | <span data-ttu-id="c23c1-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c23c1-264">0x00000000</span></span>                                   |
| <span data-ttu-id="c23c1-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c23c1-265">System-Flags</span></span>           | <span data-ttu-id="c23c1-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c23c1-266">0x00000010</span></span>                                   |
| <span data-ttu-id="c23c1-267">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c23c1-267">Classes used in</span></span>        | [<span data-ttu-id="c23c1-268">**ACS-stratégie**</span><span class="sxs-lookup"><span data-stu-id="c23c1-268">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



 

 





