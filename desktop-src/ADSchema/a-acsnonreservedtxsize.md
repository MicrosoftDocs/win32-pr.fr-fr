---
title: ACS-attribut non réservé-TX-Size
description: Taille de compartiment de jeton qu’une application peut utiliser avant qu’une réservation soit en place.
ms.assetid: 67a0d6fd-b556-49d2-8c5b-6efebf1052c3
ms.tgt_platform: multiple
keywords:
- ACS-schéma AD des attributs non réservés-TX-Size
- Schéma AD de l’attribut aCSNonReservedTxSize
topic_type:
- apiref
api_name:
- ACS-Non-Reserved-Tx-Size
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66cd19dde97e3a9fc6ef58165c8dbcbfbebba729
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845646"
---
# <a name="acs-non-reserved-tx-size-attribute"></a><span data-ttu-id="4f5af-105">ACS-attribut non réservé-TX-Size</span><span class="sxs-lookup"><span data-stu-id="4f5af-105">ACS-Non-Reserved-Tx-Size attribute</span></span>

<span data-ttu-id="4f5af-106">Taille de compartiment de jeton qu’une application peut utiliser avant qu’une réservation soit en place.</span><span class="sxs-lookup"><span data-stu-id="4f5af-106">The token bucket size an application can use before a reservation is in place.</span></span>



| <span data-ttu-id="4f5af-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="4f5af-107">Entry</span></span> | <span data-ttu-id="4f5af-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f5af-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="4f5af-109">CN</span><span class="sxs-lookup"><span data-stu-id="4f5af-109">CN</span></span>                | <span data-ttu-id="4f5af-110">ACS-non réservé-TX-Size</span><span class="sxs-lookup"><span data-stu-id="4f5af-110">ACS-Non-Reserved-Tx-Size</span></span>             |
| <span data-ttu-id="4f5af-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="4f5af-111">Ldap-Display-Name</span></span> | <span data-ttu-id="4f5af-112">aCSNonReservedTxSize</span><span class="sxs-lookup"><span data-stu-id="4f5af-112">aCSNonReservedTxSize</span></span>                 |
| <span data-ttu-id="4f5af-113">Taille</span><span class="sxs-lookup"><span data-stu-id="4f5af-113">Size</span></span>              | <span data-ttu-id="4f5af-114">8 octets</span><span class="sxs-lookup"><span data-stu-id="4f5af-114">8 bytes</span></span>                              |
| <span data-ttu-id="4f5af-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="4f5af-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="4f5af-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="4f5af-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="4f5af-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4f5af-117">Attribute-Id</span></span>      | <span data-ttu-id="4f5af-118">1.2.840.113556.1.4.898</span><span class="sxs-lookup"><span data-stu-id="4f5af-118">1.2.840.113556.1.4.898</span></span>               |
| <span data-ttu-id="4f5af-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="4f5af-119">System-Id-Guid</span></span>    | <span data-ttu-id="4f5af-120">f072230d-aef5-11d1-bdcf-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="4f5af-120">f072230d-aef5-11d1-bdcf-0000f80367c1</span></span> |
| <span data-ttu-id="4f5af-121">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4f5af-121">Syntax</span></span>            | [<span data-ttu-id="4f5af-122">**Défini**</span><span class="sxs-lookup"><span data-stu-id="4f5af-122">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="4f5af-123">Implémentations</span><span class="sxs-lookup"><span data-stu-id="4f5af-123">Implementations</span></span>

-   [<span data-ttu-id="4f5af-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="4f5af-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="4f5af-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4f5af-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4f5af-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4f5af-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4f5af-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4f5af-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4f5af-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4f5af-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4f5af-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4f5af-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="4f5af-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4f5af-130">Windows 2000 Server</span></span>



| <span data-ttu-id="4f5af-131">Entrée</span><span class="sxs-lookup"><span data-stu-id="4f5af-131">Entry</span></span> | <span data-ttu-id="4f5af-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f5af-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="4f5af-133">ID de lien</span><span class="sxs-lookup"><span data-stu-id="4f5af-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="4f5af-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4f5af-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="4f5af-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="4f5af-135">System-Only</span></span>            | <span data-ttu-id="4f5af-136">Faux</span><span class="sxs-lookup"><span data-stu-id="4f5af-136">False</span></span>                                        |
| <span data-ttu-id="4f5af-137">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="4f5af-137">Is-Single-Valued</span></span>       | <span data-ttu-id="4f5af-138">Vrai</span><span class="sxs-lookup"><span data-stu-id="4f5af-138">True</span></span>                                         |
| <span data-ttu-id="4f5af-139">Est indexé</span><span class="sxs-lookup"><span data-stu-id="4f5af-139">Is Indexed</span></span>             | <span data-ttu-id="4f5af-140">Faux</span><span class="sxs-lookup"><span data-stu-id="4f5af-140">False</span></span>                                        |
| <span data-ttu-id="4f5af-141">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="4f5af-141">In Global Catalog</span></span>      | <span data-ttu-id="4f5af-142">Faux</span><span class="sxs-lookup"><span data-stu-id="4f5af-142">False</span></span>                                        |
| <span data-ttu-id="4f5af-143">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="4f5af-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="4f5af-144">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="4f5af-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="4f5af-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4f5af-145">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="4f5af-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4f5af-146">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="4f5af-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4f5af-147">Search-Flags</span></span>           | <span data-ttu-id="4f5af-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4f5af-148">0x00000000</span></span>                                   |
| <span data-ttu-id="4f5af-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4f5af-149">System-Flags</span></span>           | <span data-ttu-id="4f5af-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4f5af-150">0x00000010</span></span>                                   |
| <span data-ttu-id="4f5af-151">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="4f5af-151">Classes used in</span></span>        | [<span data-ttu-id="4f5af-152">**ACS-sous-réseau**</span><span class="sxs-lookup"><span data-stu-id="4f5af-152">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="4f5af-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4f5af-153">Windows Server 2003</span></span>



| <span data-ttu-id="4f5af-154">Entrée</span><span class="sxs-lookup"><span data-stu-id="4f5af-154">Entry</span></span> | <span data-ttu-id="4f5af-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f5af-155">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="4f5af-156">ID de lien</span><span class="sxs-lookup"><span data-stu-id="4f5af-156">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="4f5af-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4f5af-157">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="4f5af-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="4f5af-158">System-Only</span></span>            | <span data-ttu-id="4f5af-159">Faux</span><span class="sxs-lookup"><span data-stu-id="4f5af-159">False</span></span>                                        |
| <span data-ttu-id="4f5af-160">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="4f5af-160">Is-Single-Valued</span></span>       | <span data-ttu-id="4f5af-161">Vrai</span><span class="sxs-lookup"><span data-stu-id="4f5af-161">True</span></span>                                         |
| <span data-ttu-id="4f5af-162">Est indexé</span><span class="sxs-lookup"><span data-stu-id="4f5af-162">Is Indexed</span></span>             | <span data-ttu-id="4f5af-163">Faux</span><span class="sxs-lookup"><span data-stu-id="4f5af-163">False</span></span>                                        |
| <span data-ttu-id="4f5af-164">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="4f5af-164">In Global Catalog</span></span>      | <span data-ttu-id="4f5af-165">Faux</span><span class="sxs-lookup"><span data-stu-id="4f5af-165">False</span></span>                                        |
| <span data-ttu-id="4f5af-166">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="4f5af-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="4f5af-167">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="4f5af-167">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="4f5af-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4f5af-168">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="4f5af-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4f5af-169">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="4f5af-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4f5af-170">Search-Flags</span></span>           | <span data-ttu-id="4f5af-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4f5af-171">0x00000000</span></span>                                   |
| <span data-ttu-id="4f5af-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4f5af-172">System-Flags</span></span>           | <span data-ttu-id="4f5af-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4f5af-173">0x00000010</span></span>                                   |
| <span data-ttu-id="4f5af-174">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="4f5af-174">Classes used in</span></span>        | [<span data-ttu-id="4f5af-175">**ACS-sous-réseau**</span><span class="sxs-lookup"><span data-stu-id="4f5af-175">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4f5af-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4f5af-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4f5af-177">Entrée</span><span class="sxs-lookup"><span data-stu-id="4f5af-177">Entry</span></span> | <span data-ttu-id="4f5af-178">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f5af-178">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="4f5af-179">ID de lien</span><span class="sxs-lookup"><span data-stu-id="4f5af-179">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="4f5af-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4f5af-180">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="4f5af-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="4f5af-181">System-Only</span></span>            | <span data-ttu-id="4f5af-182">Faux</span><span class="sxs-lookup"><span data-stu-id="4f5af-182">False</span></span>                                        |
| <span data-ttu-id="4f5af-183">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="4f5af-183">Is-Single-Valued</span></span>       | <span data-ttu-id="4f5af-184">Vrai</span><span class="sxs-lookup"><span data-stu-id="4f5af-184">True</span></span>                                         |
| <span data-ttu-id="4f5af-185">Est indexé</span><span class="sxs-lookup"><span data-stu-id="4f5af-185">Is Indexed</span></span>             | <span data-ttu-id="4f5af-186">Faux</span><span class="sxs-lookup"><span data-stu-id="4f5af-186">False</span></span>                                        |
| <span data-ttu-id="4f5af-187">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="4f5af-187">In Global Catalog</span></span>      | <span data-ttu-id="4f5af-188">Faux</span><span class="sxs-lookup"><span data-stu-id="4f5af-188">False</span></span>                                        |
| <span data-ttu-id="4f5af-189">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="4f5af-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="4f5af-190">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="4f5af-190">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="4f5af-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4f5af-191">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="4f5af-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4f5af-192">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="4f5af-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4f5af-193">Search-Flags</span></span>           | <span data-ttu-id="4f5af-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4f5af-194">0x00000000</span></span>                                   |
| <span data-ttu-id="4f5af-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4f5af-195">System-Flags</span></span>           | <span data-ttu-id="4f5af-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4f5af-196">0x00000010</span></span>                                   |
| <span data-ttu-id="4f5af-197">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="4f5af-197">Classes used in</span></span>        | [<span data-ttu-id="4f5af-198">**ACS-sous-réseau**</span><span class="sxs-lookup"><span data-stu-id="4f5af-198">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4f5af-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4f5af-199">Windows Server 2008</span></span>



| <span data-ttu-id="4f5af-200">Entrée</span><span class="sxs-lookup"><span data-stu-id="4f5af-200">Entry</span></span> | <span data-ttu-id="4f5af-201">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f5af-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="4f5af-202">ID de lien</span><span class="sxs-lookup"><span data-stu-id="4f5af-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="4f5af-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4f5af-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="4f5af-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="4f5af-204">System-Only</span></span>            | <span data-ttu-id="4f5af-205">Faux</span><span class="sxs-lookup"><span data-stu-id="4f5af-205">False</span></span>                                        |
| <span data-ttu-id="4f5af-206">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="4f5af-206">Is-Single-Valued</span></span>       | <span data-ttu-id="4f5af-207">Vrai</span><span class="sxs-lookup"><span data-stu-id="4f5af-207">True</span></span>                                         |
| <span data-ttu-id="4f5af-208">Est indexé</span><span class="sxs-lookup"><span data-stu-id="4f5af-208">Is Indexed</span></span>             | <span data-ttu-id="4f5af-209">Faux</span><span class="sxs-lookup"><span data-stu-id="4f5af-209">False</span></span>                                        |
| <span data-ttu-id="4f5af-210">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="4f5af-210">In Global Catalog</span></span>      | <span data-ttu-id="4f5af-211">Faux</span><span class="sxs-lookup"><span data-stu-id="4f5af-211">False</span></span>                                        |
| <span data-ttu-id="4f5af-212">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="4f5af-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="4f5af-213">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="4f5af-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="4f5af-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4f5af-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="4f5af-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4f5af-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="4f5af-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4f5af-216">Search-Flags</span></span>           | <span data-ttu-id="4f5af-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4f5af-217">0x00000000</span></span>                                   |
| <span data-ttu-id="4f5af-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4f5af-218">System-Flags</span></span>           | <span data-ttu-id="4f5af-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4f5af-219">0x00000010</span></span>                                   |
| <span data-ttu-id="4f5af-220">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="4f5af-220">Classes used in</span></span>        | [<span data-ttu-id="4f5af-221">**ACS-sous-réseau**</span><span class="sxs-lookup"><span data-stu-id="4f5af-221">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4f5af-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4f5af-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4f5af-223">Entrée</span><span class="sxs-lookup"><span data-stu-id="4f5af-223">Entry</span></span> | <span data-ttu-id="4f5af-224">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f5af-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="4f5af-225">ID de lien</span><span class="sxs-lookup"><span data-stu-id="4f5af-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="4f5af-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4f5af-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="4f5af-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="4f5af-227">System-Only</span></span>            | <span data-ttu-id="4f5af-228">Faux</span><span class="sxs-lookup"><span data-stu-id="4f5af-228">False</span></span>                                        |
| <span data-ttu-id="4f5af-229">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="4f5af-229">Is-Single-Valued</span></span>       | <span data-ttu-id="4f5af-230">Vrai</span><span class="sxs-lookup"><span data-stu-id="4f5af-230">True</span></span>                                         |
| <span data-ttu-id="4f5af-231">Est indexé</span><span class="sxs-lookup"><span data-stu-id="4f5af-231">Is Indexed</span></span>             | <span data-ttu-id="4f5af-232">Faux</span><span class="sxs-lookup"><span data-stu-id="4f5af-232">False</span></span>                                        |
| <span data-ttu-id="4f5af-233">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="4f5af-233">In Global Catalog</span></span>      | <span data-ttu-id="4f5af-234">Faux</span><span class="sxs-lookup"><span data-stu-id="4f5af-234">False</span></span>                                        |
| <span data-ttu-id="4f5af-235">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="4f5af-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="4f5af-236">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="4f5af-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="4f5af-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4f5af-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="4f5af-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4f5af-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="4f5af-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4f5af-239">Search-Flags</span></span>           | <span data-ttu-id="4f5af-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4f5af-240">0x00000000</span></span>                                   |
| <span data-ttu-id="4f5af-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4f5af-241">System-Flags</span></span>           | <span data-ttu-id="4f5af-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4f5af-242">0x00000010</span></span>                                   |
| <span data-ttu-id="4f5af-243">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="4f5af-243">Classes used in</span></span>        | [<span data-ttu-id="4f5af-244">**ACS-sous-réseau**</span><span class="sxs-lookup"><span data-stu-id="4f5af-244">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4f5af-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4f5af-245">Windows Server 2012</span></span>



| <span data-ttu-id="4f5af-246">Entrée</span><span class="sxs-lookup"><span data-stu-id="4f5af-246">Entry</span></span> | <span data-ttu-id="4f5af-247">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f5af-247">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="4f5af-248">ID de lien</span><span class="sxs-lookup"><span data-stu-id="4f5af-248">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="4f5af-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4f5af-249">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="4f5af-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="4f5af-250">System-Only</span></span>            | <span data-ttu-id="4f5af-251">Faux</span><span class="sxs-lookup"><span data-stu-id="4f5af-251">False</span></span>                                        |
| <span data-ttu-id="4f5af-252">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="4f5af-252">Is-Single-Valued</span></span>       | <span data-ttu-id="4f5af-253">Vrai</span><span class="sxs-lookup"><span data-stu-id="4f5af-253">True</span></span>                                         |
| <span data-ttu-id="4f5af-254">Est indexé</span><span class="sxs-lookup"><span data-stu-id="4f5af-254">Is Indexed</span></span>             | <span data-ttu-id="4f5af-255">Faux</span><span class="sxs-lookup"><span data-stu-id="4f5af-255">False</span></span>                                        |
| <span data-ttu-id="4f5af-256">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="4f5af-256">In Global Catalog</span></span>      | <span data-ttu-id="4f5af-257">Faux</span><span class="sxs-lookup"><span data-stu-id="4f5af-257">False</span></span>                                        |
| <span data-ttu-id="4f5af-258">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="4f5af-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="4f5af-259">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="4f5af-259">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="4f5af-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4f5af-260">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="4f5af-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4f5af-261">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="4f5af-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4f5af-262">Search-Flags</span></span>           | <span data-ttu-id="4f5af-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4f5af-263">0x00000000</span></span>                                   |
| <span data-ttu-id="4f5af-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4f5af-264">System-Flags</span></span>           | <span data-ttu-id="4f5af-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4f5af-265">0x00000010</span></span>                                   |
| <span data-ttu-id="4f5af-266">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="4f5af-266">Classes used in</span></span>        | [<span data-ttu-id="4f5af-267">**ACS-sous-réseau**</span><span class="sxs-lookup"><span data-stu-id="4f5af-267">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 





