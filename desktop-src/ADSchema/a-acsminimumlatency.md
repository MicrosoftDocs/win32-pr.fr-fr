---
title: ACS-attribut de latence minimale
description: L’attribut ACS-minimum-latence est destiné à un usage interne uniquement.
ms.assetid: ec2cca55-9e31-49da-98aa-aa2f6664ea90
ms.tgt_platform: multiple
keywords:
- ACS-schéma AD d’attribut de latence minimale
- Schéma AD de l’attribut aCSMinimumLatency
topic_type:
- apiref
api_name:
- ACS-Minimum-Latency
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ab7e9e6d5a9ccf626cdf8849ffe0e29504b4a0b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104033302"
---
# <a name="acs-minimum-latency-attribute"></a><span data-ttu-id="b24a7-105">ACS-attribut de latence minimale</span><span class="sxs-lookup"><span data-stu-id="b24a7-105">ACS-Minimum-Latency attribute</span></span>

<span data-ttu-id="b24a7-106">L’attribut **ACS-minimum-latence** est destiné à un usage interne uniquement.</span><span class="sxs-lookup"><span data-stu-id="b24a7-106">The **ACS-Minimum-Latency** attribute is for internal use only.</span></span> <span data-ttu-id="b24a7-107">Basé sur RFC2210.</span><span class="sxs-lookup"><span data-stu-id="b24a7-107">Based on RFC2210.</span></span>



| <span data-ttu-id="b24a7-108">Entrée</span><span class="sxs-lookup"><span data-stu-id="b24a7-108">Entry</span></span> | <span data-ttu-id="b24a7-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="b24a7-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="b24a7-110">CN</span><span class="sxs-lookup"><span data-stu-id="b24a7-110">CN</span></span>                | <span data-ttu-id="b24a7-111">ACS-latence minimale</span><span class="sxs-lookup"><span data-stu-id="b24a7-111">ACS-Minimum-Latency</span></span>                  |
| <span data-ttu-id="b24a7-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="b24a7-112">Ldap-Display-Name</span></span> | <span data-ttu-id="b24a7-113">aCSMinimumLatency</span><span class="sxs-lookup"><span data-stu-id="b24a7-113">aCSMinimumLatency</span></span>                    |
| <span data-ttu-id="b24a7-114">Taille</span><span class="sxs-lookup"><span data-stu-id="b24a7-114">Size</span></span>              | <span data-ttu-id="b24a7-115">8 octets</span><span class="sxs-lookup"><span data-stu-id="b24a7-115">8 bytes</span></span>                              |
| <span data-ttu-id="b24a7-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="b24a7-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="b24a7-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="b24a7-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="b24a7-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b24a7-118">Attribute-Id</span></span>      | <span data-ttu-id="b24a7-119">1.2.840.113556.1.4.1316</span><span class="sxs-lookup"><span data-stu-id="b24a7-119">1.2.840.113556.1.4.1316</span></span>              |
| <span data-ttu-id="b24a7-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b24a7-120">System-Id-Guid</span></span>    | <span data-ttu-id="b24a7-121">9517fefb-3b90-11d2-90cc-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="b24a7-121">9517fefb-3b90-11d2-90cc-00c04fd91ab1</span></span> |
| <span data-ttu-id="b24a7-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b24a7-122">Syntax</span></span>            | [<span data-ttu-id="b24a7-123">**Défini**</span><span class="sxs-lookup"><span data-stu-id="b24a7-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="b24a7-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="b24a7-124">Implementations</span></span>

-   [<span data-ttu-id="b24a7-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b24a7-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b24a7-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b24a7-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b24a7-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b24a7-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b24a7-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b24a7-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b24a7-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b24a7-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b24a7-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b24a7-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b24a7-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b24a7-131">Windows 2000 Server</span></span>



| <span data-ttu-id="b24a7-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="b24a7-132">Entry</span></span> | <span data-ttu-id="b24a7-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="b24a7-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b24a7-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b24a7-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b24a7-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b24a7-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b24a7-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="b24a7-136">System-Only</span></span>            | <span data-ttu-id="b24a7-137">Faux</span><span class="sxs-lookup"><span data-stu-id="b24a7-137">False</span></span>                                        |
| <span data-ttu-id="b24a7-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b24a7-138">Is-Single-Valued</span></span>       | <span data-ttu-id="b24a7-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="b24a7-139">True</span></span>                                         |
| <span data-ttu-id="b24a7-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b24a7-140">Is Indexed</span></span>             | <span data-ttu-id="b24a7-141">Faux</span><span class="sxs-lookup"><span data-stu-id="b24a7-141">False</span></span>                                        |
| <span data-ttu-id="b24a7-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b24a7-142">In Global Catalog</span></span>      | <span data-ttu-id="b24a7-143">Faux</span><span class="sxs-lookup"><span data-stu-id="b24a7-143">False</span></span>                                        |
| <span data-ttu-id="b24a7-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b24a7-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="b24a7-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b24a7-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b24a7-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b24a7-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b24a7-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b24a7-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b24a7-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b24a7-148">Search-Flags</span></span>           | <span data-ttu-id="b24a7-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b24a7-149">0x00000000</span></span>                                   |
| <span data-ttu-id="b24a7-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b24a7-150">System-Flags</span></span>           | <span data-ttu-id="b24a7-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b24a7-151">0x00000010</span></span>                                   |
| <span data-ttu-id="b24a7-152">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b24a7-152">Classes used in</span></span>        | [<span data-ttu-id="b24a7-153">**ACS-stratégie**</span><span class="sxs-lookup"><span data-stu-id="b24a7-153">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b24a7-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b24a7-154">Windows Server 2003</span></span>



| <span data-ttu-id="b24a7-155">Entrée</span><span class="sxs-lookup"><span data-stu-id="b24a7-155">Entry</span></span> | <span data-ttu-id="b24a7-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="b24a7-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b24a7-157">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b24a7-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b24a7-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b24a7-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b24a7-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="b24a7-159">System-Only</span></span>            | <span data-ttu-id="b24a7-160">Faux</span><span class="sxs-lookup"><span data-stu-id="b24a7-160">False</span></span>                                        |
| <span data-ttu-id="b24a7-161">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b24a7-161">Is-Single-Valued</span></span>       | <span data-ttu-id="b24a7-162">Vrai</span><span class="sxs-lookup"><span data-stu-id="b24a7-162">True</span></span>                                         |
| <span data-ttu-id="b24a7-163">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b24a7-163">Is Indexed</span></span>             | <span data-ttu-id="b24a7-164">Faux</span><span class="sxs-lookup"><span data-stu-id="b24a7-164">False</span></span>                                        |
| <span data-ttu-id="b24a7-165">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b24a7-165">In Global Catalog</span></span>      | <span data-ttu-id="b24a7-166">Faux</span><span class="sxs-lookup"><span data-stu-id="b24a7-166">False</span></span>                                        |
| <span data-ttu-id="b24a7-167">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b24a7-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="b24a7-168">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b24a7-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b24a7-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b24a7-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b24a7-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b24a7-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b24a7-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b24a7-171">Search-Flags</span></span>           | <span data-ttu-id="b24a7-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b24a7-172">0x00000000</span></span>                                   |
| <span data-ttu-id="b24a7-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b24a7-173">System-Flags</span></span>           | <span data-ttu-id="b24a7-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b24a7-174">0x00000010</span></span>                                   |
| <span data-ttu-id="b24a7-175">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b24a7-175">Classes used in</span></span>        | [<span data-ttu-id="b24a7-176">**ACS-stratégie**</span><span class="sxs-lookup"><span data-stu-id="b24a7-176">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b24a7-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b24a7-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b24a7-178">Entrée</span><span class="sxs-lookup"><span data-stu-id="b24a7-178">Entry</span></span> | <span data-ttu-id="b24a7-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="b24a7-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b24a7-180">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b24a7-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b24a7-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b24a7-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b24a7-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="b24a7-182">System-Only</span></span>            | <span data-ttu-id="b24a7-183">Faux</span><span class="sxs-lookup"><span data-stu-id="b24a7-183">False</span></span>                                        |
| <span data-ttu-id="b24a7-184">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b24a7-184">Is-Single-Valued</span></span>       | <span data-ttu-id="b24a7-185">Vrai</span><span class="sxs-lookup"><span data-stu-id="b24a7-185">True</span></span>                                         |
| <span data-ttu-id="b24a7-186">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b24a7-186">Is Indexed</span></span>             | <span data-ttu-id="b24a7-187">Faux</span><span class="sxs-lookup"><span data-stu-id="b24a7-187">False</span></span>                                        |
| <span data-ttu-id="b24a7-188">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b24a7-188">In Global Catalog</span></span>      | <span data-ttu-id="b24a7-189">Faux</span><span class="sxs-lookup"><span data-stu-id="b24a7-189">False</span></span>                                        |
| <span data-ttu-id="b24a7-190">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b24a7-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="b24a7-191">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b24a7-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b24a7-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b24a7-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b24a7-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b24a7-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b24a7-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b24a7-194">Search-Flags</span></span>           | <span data-ttu-id="b24a7-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b24a7-195">0x00000000</span></span>                                   |
| <span data-ttu-id="b24a7-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b24a7-196">System-Flags</span></span>           | <span data-ttu-id="b24a7-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b24a7-197">0x00000010</span></span>                                   |
| <span data-ttu-id="b24a7-198">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b24a7-198">Classes used in</span></span>        | [<span data-ttu-id="b24a7-199">**ACS-stratégie**</span><span class="sxs-lookup"><span data-stu-id="b24a7-199">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b24a7-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b24a7-200">Windows Server 2008</span></span>



| <span data-ttu-id="b24a7-201">Entrée</span><span class="sxs-lookup"><span data-stu-id="b24a7-201">Entry</span></span> | <span data-ttu-id="b24a7-202">Valeur</span><span class="sxs-lookup"><span data-stu-id="b24a7-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b24a7-203">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b24a7-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b24a7-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b24a7-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b24a7-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="b24a7-205">System-Only</span></span>            | <span data-ttu-id="b24a7-206">Faux</span><span class="sxs-lookup"><span data-stu-id="b24a7-206">False</span></span>                                        |
| <span data-ttu-id="b24a7-207">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b24a7-207">Is-Single-Valued</span></span>       | <span data-ttu-id="b24a7-208">Vrai</span><span class="sxs-lookup"><span data-stu-id="b24a7-208">True</span></span>                                         |
| <span data-ttu-id="b24a7-209">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b24a7-209">Is Indexed</span></span>             | <span data-ttu-id="b24a7-210">Faux</span><span class="sxs-lookup"><span data-stu-id="b24a7-210">False</span></span>                                        |
| <span data-ttu-id="b24a7-211">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b24a7-211">In Global Catalog</span></span>      | <span data-ttu-id="b24a7-212">Faux</span><span class="sxs-lookup"><span data-stu-id="b24a7-212">False</span></span>                                        |
| <span data-ttu-id="b24a7-213">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b24a7-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="b24a7-214">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b24a7-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b24a7-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b24a7-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b24a7-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b24a7-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b24a7-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b24a7-217">Search-Flags</span></span>           | <span data-ttu-id="b24a7-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b24a7-218">0x00000000</span></span>                                   |
| <span data-ttu-id="b24a7-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b24a7-219">System-Flags</span></span>           | <span data-ttu-id="b24a7-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b24a7-220">0x00000010</span></span>                                   |
| <span data-ttu-id="b24a7-221">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b24a7-221">Classes used in</span></span>        | [<span data-ttu-id="b24a7-222">**ACS-stratégie**</span><span class="sxs-lookup"><span data-stu-id="b24a7-222">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b24a7-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b24a7-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b24a7-224">Entrée</span><span class="sxs-lookup"><span data-stu-id="b24a7-224">Entry</span></span> | <span data-ttu-id="b24a7-225">Valeur</span><span class="sxs-lookup"><span data-stu-id="b24a7-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b24a7-226">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b24a7-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b24a7-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b24a7-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b24a7-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="b24a7-228">System-Only</span></span>            | <span data-ttu-id="b24a7-229">Faux</span><span class="sxs-lookup"><span data-stu-id="b24a7-229">False</span></span>                                        |
| <span data-ttu-id="b24a7-230">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b24a7-230">Is-Single-Valued</span></span>       | <span data-ttu-id="b24a7-231">Vrai</span><span class="sxs-lookup"><span data-stu-id="b24a7-231">True</span></span>                                         |
| <span data-ttu-id="b24a7-232">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b24a7-232">Is Indexed</span></span>             | <span data-ttu-id="b24a7-233">Faux</span><span class="sxs-lookup"><span data-stu-id="b24a7-233">False</span></span>                                        |
| <span data-ttu-id="b24a7-234">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b24a7-234">In Global Catalog</span></span>      | <span data-ttu-id="b24a7-235">Faux</span><span class="sxs-lookup"><span data-stu-id="b24a7-235">False</span></span>                                        |
| <span data-ttu-id="b24a7-236">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b24a7-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="b24a7-237">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b24a7-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b24a7-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b24a7-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b24a7-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b24a7-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b24a7-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b24a7-240">Search-Flags</span></span>           | <span data-ttu-id="b24a7-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b24a7-241">0x00000000</span></span>                                   |
| <span data-ttu-id="b24a7-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b24a7-242">System-Flags</span></span>           | <span data-ttu-id="b24a7-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b24a7-243">0x00000010</span></span>                                   |
| <span data-ttu-id="b24a7-244">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b24a7-244">Classes used in</span></span>        | [<span data-ttu-id="b24a7-245">**ACS-stratégie**</span><span class="sxs-lookup"><span data-stu-id="b24a7-245">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b24a7-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b24a7-246">Windows Server 2012</span></span>



| <span data-ttu-id="b24a7-247">Entrée</span><span class="sxs-lookup"><span data-stu-id="b24a7-247">Entry</span></span> | <span data-ttu-id="b24a7-248">Valeur</span><span class="sxs-lookup"><span data-stu-id="b24a7-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b24a7-249">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b24a7-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b24a7-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b24a7-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b24a7-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="b24a7-251">System-Only</span></span>            | <span data-ttu-id="b24a7-252">Faux</span><span class="sxs-lookup"><span data-stu-id="b24a7-252">False</span></span>                                        |
| <span data-ttu-id="b24a7-253">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b24a7-253">Is-Single-Valued</span></span>       | <span data-ttu-id="b24a7-254">Vrai</span><span class="sxs-lookup"><span data-stu-id="b24a7-254">True</span></span>                                         |
| <span data-ttu-id="b24a7-255">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b24a7-255">Is Indexed</span></span>             | <span data-ttu-id="b24a7-256">Faux</span><span class="sxs-lookup"><span data-stu-id="b24a7-256">False</span></span>                                        |
| <span data-ttu-id="b24a7-257">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b24a7-257">In Global Catalog</span></span>      | <span data-ttu-id="b24a7-258">Faux</span><span class="sxs-lookup"><span data-stu-id="b24a7-258">False</span></span>                                        |
| <span data-ttu-id="b24a7-259">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b24a7-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="b24a7-260">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b24a7-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b24a7-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b24a7-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b24a7-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b24a7-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b24a7-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b24a7-263">Search-Flags</span></span>           | <span data-ttu-id="b24a7-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b24a7-264">0x00000000</span></span>                                   |
| <span data-ttu-id="b24a7-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b24a7-265">System-Flags</span></span>           | <span data-ttu-id="b24a7-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b24a7-266">0x00000010</span></span>                                   |
| <span data-ttu-id="b24a7-267">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b24a7-267">Classes used in</span></span>        | [<span data-ttu-id="b24a7-268">**ACS-stratégie**</span><span class="sxs-lookup"><span data-stu-id="b24a7-268">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



 

 





