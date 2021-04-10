---
title: ACS-non réservé-attribut de taux de pics
description: L’attribut ACS-non réservé-pic-rate est destiné à un usage interne uniquement.
ms.assetid: 4080839c-d99e-4527-8c81-6d23ab0d3d70
ms.tgt_platform: multiple
keywords:
- ACS-non réservé-attribut de taux de pics Active Directory
- Schéma AD de l’attribut aCSNonReservedPeakRate
topic_type:
- apiref
api_name:
- ACS-Non-Reserved-Peak-Rate
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ea3d2075e90648388a9a1277dbbe768a3fc616f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107326"
---
# <a name="acs-non-reserved-peak-rate-attribute"></a><span data-ttu-id="0e7ac-105">ACS-non réservé-attribut de taux de pics</span><span class="sxs-lookup"><span data-stu-id="0e7ac-105">ACS-Non-Reserved-Peak-Rate attribute</span></span>

<span data-ttu-id="0e7ac-106">L’attribut **ACS-non réservé-pic-rate** est destiné à un usage interne uniquement.</span><span class="sxs-lookup"><span data-stu-id="0e7ac-106">The **ACS-Non-Reserved-Peak-Rate** attribute is for internal use only.</span></span> <span data-ttu-id="0e7ac-107">Basé sur RFC2814.</span><span class="sxs-lookup"><span data-stu-id="0e7ac-107">Based on RFC2814.</span></span>



| <span data-ttu-id="0e7ac-108">Entrée</span><span class="sxs-lookup"><span data-stu-id="0e7ac-108">Entry</span></span> | <span data-ttu-id="0e7ac-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e7ac-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="0e7ac-110">CN</span><span class="sxs-lookup"><span data-stu-id="0e7ac-110">CN</span></span>                | <span data-ttu-id="0e7ac-111">ACS-non réservé-taux de pointe</span><span class="sxs-lookup"><span data-stu-id="0e7ac-111">ACS-Non-Reserved-Peak-Rate</span></span>           |
| <span data-ttu-id="0e7ac-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="0e7ac-112">Ldap-Display-Name</span></span> | <span data-ttu-id="0e7ac-113">aCSNonReservedPeakRate</span><span class="sxs-lookup"><span data-stu-id="0e7ac-113">aCSNonReservedPeakRate</span></span>               |
| <span data-ttu-id="0e7ac-114">Taille</span><span class="sxs-lookup"><span data-stu-id="0e7ac-114">Size</span></span>              | <span data-ttu-id="0e7ac-115">8 octets</span><span class="sxs-lookup"><span data-stu-id="0e7ac-115">8 bytes</span></span>                              |
| <span data-ttu-id="0e7ac-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="0e7ac-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="0e7ac-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="0e7ac-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="0e7ac-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0e7ac-118">Attribute-Id</span></span>      | <span data-ttu-id="0e7ac-119">1.2.840.113556.1.4.1318</span><span class="sxs-lookup"><span data-stu-id="0e7ac-119">1.2.840.113556.1.4.1318</span></span>              |
| <span data-ttu-id="0e7ac-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="0e7ac-120">System-Id-Guid</span></span>    | <span data-ttu-id="0e7ac-121">a331a73f-3b90-11d2-90cc-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="0e7ac-121">a331a73f-3b90-11d2-90cc-00c04fd91ab1</span></span> |
| <span data-ttu-id="0e7ac-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0e7ac-122">Syntax</span></span>            | [<span data-ttu-id="0e7ac-123">**Défini**</span><span class="sxs-lookup"><span data-stu-id="0e7ac-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="0e7ac-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="0e7ac-124">Implementations</span></span>

-   [<span data-ttu-id="0e7ac-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="0e7ac-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="0e7ac-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="0e7ac-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="0e7ac-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="0e7ac-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="0e7ac-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0e7ac-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0e7ac-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0e7ac-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0e7ac-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0e7ac-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="0e7ac-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0e7ac-131">Windows 2000 Server</span></span>



| <span data-ttu-id="0e7ac-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="0e7ac-132">Entry</span></span> | <span data-ttu-id="0e7ac-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e7ac-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="0e7ac-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="0e7ac-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="0e7ac-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0e7ac-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="0e7ac-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="0e7ac-136">System-Only</span></span>            | <span data-ttu-id="0e7ac-137">Faux</span><span class="sxs-lookup"><span data-stu-id="0e7ac-137">False</span></span>                                        |
| <span data-ttu-id="0e7ac-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="0e7ac-138">Is-Single-Valued</span></span>       | <span data-ttu-id="0e7ac-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="0e7ac-139">True</span></span>                                         |
| <span data-ttu-id="0e7ac-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="0e7ac-140">Is Indexed</span></span>             | <span data-ttu-id="0e7ac-141">Faux</span><span class="sxs-lookup"><span data-stu-id="0e7ac-141">False</span></span>                                        |
| <span data-ttu-id="0e7ac-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="0e7ac-142">In Global Catalog</span></span>      | <span data-ttu-id="0e7ac-143">Faux</span><span class="sxs-lookup"><span data-stu-id="0e7ac-143">False</span></span>                                        |
| <span data-ttu-id="0e7ac-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="0e7ac-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="0e7ac-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="0e7ac-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="0e7ac-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0e7ac-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="0e7ac-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0e7ac-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="0e7ac-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0e7ac-148">Search-Flags</span></span>           | <span data-ttu-id="0e7ac-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0e7ac-149">0x00000000</span></span>                                   |
| <span data-ttu-id="0e7ac-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0e7ac-150">System-Flags</span></span>           | <span data-ttu-id="0e7ac-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0e7ac-151">0x00000010</span></span>                                   |
| <span data-ttu-id="0e7ac-152">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="0e7ac-152">Classes used in</span></span>        | [<span data-ttu-id="0e7ac-153">**ACS-sous-réseau**</span><span class="sxs-lookup"><span data-stu-id="0e7ac-153">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="0e7ac-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0e7ac-154">Windows Server 2003</span></span>



| <span data-ttu-id="0e7ac-155">Entrée</span><span class="sxs-lookup"><span data-stu-id="0e7ac-155">Entry</span></span> | <span data-ttu-id="0e7ac-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e7ac-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="0e7ac-157">ID de lien</span><span class="sxs-lookup"><span data-stu-id="0e7ac-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="0e7ac-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0e7ac-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="0e7ac-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="0e7ac-159">System-Only</span></span>            | <span data-ttu-id="0e7ac-160">Faux</span><span class="sxs-lookup"><span data-stu-id="0e7ac-160">False</span></span>                                        |
| <span data-ttu-id="0e7ac-161">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="0e7ac-161">Is-Single-Valued</span></span>       | <span data-ttu-id="0e7ac-162">Vrai</span><span class="sxs-lookup"><span data-stu-id="0e7ac-162">True</span></span>                                         |
| <span data-ttu-id="0e7ac-163">Est indexé</span><span class="sxs-lookup"><span data-stu-id="0e7ac-163">Is Indexed</span></span>             | <span data-ttu-id="0e7ac-164">Faux</span><span class="sxs-lookup"><span data-stu-id="0e7ac-164">False</span></span>                                        |
| <span data-ttu-id="0e7ac-165">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="0e7ac-165">In Global Catalog</span></span>      | <span data-ttu-id="0e7ac-166">Faux</span><span class="sxs-lookup"><span data-stu-id="0e7ac-166">False</span></span>                                        |
| <span data-ttu-id="0e7ac-167">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="0e7ac-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="0e7ac-168">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="0e7ac-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="0e7ac-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0e7ac-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="0e7ac-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0e7ac-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="0e7ac-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0e7ac-171">Search-Flags</span></span>           | <span data-ttu-id="0e7ac-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0e7ac-172">0x00000000</span></span>                                   |
| <span data-ttu-id="0e7ac-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0e7ac-173">System-Flags</span></span>           | <span data-ttu-id="0e7ac-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0e7ac-174">0x00000010</span></span>                                   |
| <span data-ttu-id="0e7ac-175">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="0e7ac-175">Classes used in</span></span>        | [<span data-ttu-id="0e7ac-176">**ACS-sous-réseau**</span><span class="sxs-lookup"><span data-stu-id="0e7ac-176">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="0e7ac-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0e7ac-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="0e7ac-178">Entrée</span><span class="sxs-lookup"><span data-stu-id="0e7ac-178">Entry</span></span> | <span data-ttu-id="0e7ac-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e7ac-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="0e7ac-180">ID de lien</span><span class="sxs-lookup"><span data-stu-id="0e7ac-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="0e7ac-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0e7ac-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="0e7ac-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="0e7ac-182">System-Only</span></span>            | <span data-ttu-id="0e7ac-183">Faux</span><span class="sxs-lookup"><span data-stu-id="0e7ac-183">False</span></span>                                        |
| <span data-ttu-id="0e7ac-184">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="0e7ac-184">Is-Single-Valued</span></span>       | <span data-ttu-id="0e7ac-185">Vrai</span><span class="sxs-lookup"><span data-stu-id="0e7ac-185">True</span></span>                                         |
| <span data-ttu-id="0e7ac-186">Est indexé</span><span class="sxs-lookup"><span data-stu-id="0e7ac-186">Is Indexed</span></span>             | <span data-ttu-id="0e7ac-187">Faux</span><span class="sxs-lookup"><span data-stu-id="0e7ac-187">False</span></span>                                        |
| <span data-ttu-id="0e7ac-188">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="0e7ac-188">In Global Catalog</span></span>      | <span data-ttu-id="0e7ac-189">Faux</span><span class="sxs-lookup"><span data-stu-id="0e7ac-189">False</span></span>                                        |
| <span data-ttu-id="0e7ac-190">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="0e7ac-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="0e7ac-191">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="0e7ac-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="0e7ac-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0e7ac-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="0e7ac-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0e7ac-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="0e7ac-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0e7ac-194">Search-Flags</span></span>           | <span data-ttu-id="0e7ac-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0e7ac-195">0x00000000</span></span>                                   |
| <span data-ttu-id="0e7ac-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0e7ac-196">System-Flags</span></span>           | <span data-ttu-id="0e7ac-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0e7ac-197">0x00000010</span></span>                                   |
| <span data-ttu-id="0e7ac-198">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="0e7ac-198">Classes used in</span></span>        | [<span data-ttu-id="0e7ac-199">**ACS-sous-réseau**</span><span class="sxs-lookup"><span data-stu-id="0e7ac-199">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="0e7ac-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0e7ac-200">Windows Server 2008</span></span>



| <span data-ttu-id="0e7ac-201">Entrée</span><span class="sxs-lookup"><span data-stu-id="0e7ac-201">Entry</span></span> | <span data-ttu-id="0e7ac-202">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e7ac-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="0e7ac-203">ID de lien</span><span class="sxs-lookup"><span data-stu-id="0e7ac-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="0e7ac-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0e7ac-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="0e7ac-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="0e7ac-205">System-Only</span></span>            | <span data-ttu-id="0e7ac-206">Faux</span><span class="sxs-lookup"><span data-stu-id="0e7ac-206">False</span></span>                                        |
| <span data-ttu-id="0e7ac-207">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="0e7ac-207">Is-Single-Valued</span></span>       | <span data-ttu-id="0e7ac-208">Vrai</span><span class="sxs-lookup"><span data-stu-id="0e7ac-208">True</span></span>                                         |
| <span data-ttu-id="0e7ac-209">Est indexé</span><span class="sxs-lookup"><span data-stu-id="0e7ac-209">Is Indexed</span></span>             | <span data-ttu-id="0e7ac-210">Faux</span><span class="sxs-lookup"><span data-stu-id="0e7ac-210">False</span></span>                                        |
| <span data-ttu-id="0e7ac-211">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="0e7ac-211">In Global Catalog</span></span>      | <span data-ttu-id="0e7ac-212">Faux</span><span class="sxs-lookup"><span data-stu-id="0e7ac-212">False</span></span>                                        |
| <span data-ttu-id="0e7ac-213">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="0e7ac-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="0e7ac-214">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="0e7ac-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="0e7ac-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0e7ac-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="0e7ac-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0e7ac-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="0e7ac-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0e7ac-217">Search-Flags</span></span>           | <span data-ttu-id="0e7ac-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0e7ac-218">0x00000000</span></span>                                   |
| <span data-ttu-id="0e7ac-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0e7ac-219">System-Flags</span></span>           | <span data-ttu-id="0e7ac-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0e7ac-220">0x00000010</span></span>                                   |
| <span data-ttu-id="0e7ac-221">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="0e7ac-221">Classes used in</span></span>        | [<span data-ttu-id="0e7ac-222">**ACS-sous-réseau**</span><span class="sxs-lookup"><span data-stu-id="0e7ac-222">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0e7ac-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0e7ac-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0e7ac-224">Entrée</span><span class="sxs-lookup"><span data-stu-id="0e7ac-224">Entry</span></span> | <span data-ttu-id="0e7ac-225">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e7ac-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="0e7ac-226">ID de lien</span><span class="sxs-lookup"><span data-stu-id="0e7ac-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="0e7ac-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0e7ac-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="0e7ac-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="0e7ac-228">System-Only</span></span>            | <span data-ttu-id="0e7ac-229">Faux</span><span class="sxs-lookup"><span data-stu-id="0e7ac-229">False</span></span>                                        |
| <span data-ttu-id="0e7ac-230">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="0e7ac-230">Is-Single-Valued</span></span>       | <span data-ttu-id="0e7ac-231">Vrai</span><span class="sxs-lookup"><span data-stu-id="0e7ac-231">True</span></span>                                         |
| <span data-ttu-id="0e7ac-232">Est indexé</span><span class="sxs-lookup"><span data-stu-id="0e7ac-232">Is Indexed</span></span>             | <span data-ttu-id="0e7ac-233">Faux</span><span class="sxs-lookup"><span data-stu-id="0e7ac-233">False</span></span>                                        |
| <span data-ttu-id="0e7ac-234">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="0e7ac-234">In Global Catalog</span></span>      | <span data-ttu-id="0e7ac-235">Faux</span><span class="sxs-lookup"><span data-stu-id="0e7ac-235">False</span></span>                                        |
| <span data-ttu-id="0e7ac-236">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="0e7ac-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="0e7ac-237">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="0e7ac-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="0e7ac-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0e7ac-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="0e7ac-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0e7ac-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="0e7ac-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0e7ac-240">Search-Flags</span></span>           | <span data-ttu-id="0e7ac-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0e7ac-241">0x00000000</span></span>                                   |
| <span data-ttu-id="0e7ac-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0e7ac-242">System-Flags</span></span>           | <span data-ttu-id="0e7ac-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0e7ac-243">0x00000010</span></span>                                   |
| <span data-ttu-id="0e7ac-244">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="0e7ac-244">Classes used in</span></span>        | [<span data-ttu-id="0e7ac-245">**ACS-sous-réseau**</span><span class="sxs-lookup"><span data-stu-id="0e7ac-245">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0e7ac-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0e7ac-246">Windows Server 2012</span></span>



| <span data-ttu-id="0e7ac-247">Entrée</span><span class="sxs-lookup"><span data-stu-id="0e7ac-247">Entry</span></span> | <span data-ttu-id="0e7ac-248">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e7ac-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="0e7ac-249">ID de lien</span><span class="sxs-lookup"><span data-stu-id="0e7ac-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="0e7ac-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0e7ac-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="0e7ac-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="0e7ac-251">System-Only</span></span>            | <span data-ttu-id="0e7ac-252">Faux</span><span class="sxs-lookup"><span data-stu-id="0e7ac-252">False</span></span>                                        |
| <span data-ttu-id="0e7ac-253">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="0e7ac-253">Is-Single-Valued</span></span>       | <span data-ttu-id="0e7ac-254">Vrai</span><span class="sxs-lookup"><span data-stu-id="0e7ac-254">True</span></span>                                         |
| <span data-ttu-id="0e7ac-255">Est indexé</span><span class="sxs-lookup"><span data-stu-id="0e7ac-255">Is Indexed</span></span>             | <span data-ttu-id="0e7ac-256">Faux</span><span class="sxs-lookup"><span data-stu-id="0e7ac-256">False</span></span>                                        |
| <span data-ttu-id="0e7ac-257">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="0e7ac-257">In Global Catalog</span></span>      | <span data-ttu-id="0e7ac-258">Faux</span><span class="sxs-lookup"><span data-stu-id="0e7ac-258">False</span></span>                                        |
| <span data-ttu-id="0e7ac-259">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="0e7ac-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="0e7ac-260">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="0e7ac-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="0e7ac-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0e7ac-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="0e7ac-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0e7ac-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="0e7ac-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0e7ac-263">Search-Flags</span></span>           | <span data-ttu-id="0e7ac-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0e7ac-264">0x00000000</span></span>                                   |
| <span data-ttu-id="0e7ac-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0e7ac-265">System-Flags</span></span>           | <span data-ttu-id="0e7ac-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0e7ac-266">0x00000010</span></span>                                   |
| <span data-ttu-id="0e7ac-267">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="0e7ac-267">Classes used in</span></span>        | [<span data-ttu-id="0e7ac-268">**ACS-sous-réseau**</span><span class="sxs-lookup"><span data-stu-id="0e7ac-268">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 





