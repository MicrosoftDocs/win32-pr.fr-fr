---
title: ACS-attribut non réservé-TX-Limit
description: Bande passante maximale qu’une application utilisateur peut transmettre avant qu’une réservation soit en place.
ms.assetid: 5ead8e5b-31e8-438e-8d1b-9aae8601dfc9
ms.tgt_platform: multiple
keywords:
- Schéma AD ACS-non réservé-TX-Limit Attribute
- Schéma AD de l’attribut aCSNonReservedTxLimit
topic_type:
- apiref
api_name:
- ACS-Non-Reserved-Tx-Limit
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 999b1775640624b7825b38ae1632d70773bc75b3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106515275"
---
# <a name="acs-non-reserved-tx-limit-attribute"></a><span data-ttu-id="4b25e-105">ACS-attribut non réservé-TX-Limit</span><span class="sxs-lookup"><span data-stu-id="4b25e-105">ACS-Non-Reserved-Tx-Limit attribute</span></span>

<span data-ttu-id="4b25e-106">Bande passante maximale qu’une application utilisateur peut transmettre avant qu’une réservation soit en place.</span><span class="sxs-lookup"><span data-stu-id="4b25e-106">The maximum bandwidth a user application can transmit before a reservation is in place.</span></span>



| <span data-ttu-id="4b25e-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="4b25e-107">Entry</span></span> | <span data-ttu-id="4b25e-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="4b25e-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="4b25e-109">CN</span><span class="sxs-lookup"><span data-stu-id="4b25e-109">CN</span></span>                | <span data-ttu-id="4b25e-110">ACS-non réservé-TX-Limit</span><span class="sxs-lookup"><span data-stu-id="4b25e-110">ACS-Non-Reserved-Tx-Limit</span></span>            |
| <span data-ttu-id="4b25e-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="4b25e-111">Ldap-Display-Name</span></span> | <span data-ttu-id="4b25e-112">aCSNonReservedTxLimit</span><span class="sxs-lookup"><span data-stu-id="4b25e-112">aCSNonReservedTxLimit</span></span>                |
| <span data-ttu-id="4b25e-113">Taille</span><span class="sxs-lookup"><span data-stu-id="4b25e-113">Size</span></span>              | <span data-ttu-id="4b25e-114">8 octets</span><span class="sxs-lookup"><span data-stu-id="4b25e-114">8 bytes</span></span>                              |
| <span data-ttu-id="4b25e-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="4b25e-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="4b25e-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="4b25e-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="4b25e-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4b25e-117">Attribute-Id</span></span>      | <span data-ttu-id="4b25e-118">1.2.840.113556.1.4.780</span><span class="sxs-lookup"><span data-stu-id="4b25e-118">1.2.840.113556.1.4.780</span></span>               |
| <span data-ttu-id="4b25e-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="4b25e-119">System-Id-Guid</span></span>    | <span data-ttu-id="4b25e-120">1cb355a2-56d0-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="4b25e-120">1cb355a2-56d0-11d1-a9c6-0000f80367c1</span></span> |
| <span data-ttu-id="4b25e-121">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4b25e-121">Syntax</span></span>            | [<span data-ttu-id="4b25e-122">**Défini**</span><span class="sxs-lookup"><span data-stu-id="4b25e-122">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="4b25e-123">Implémentations</span><span class="sxs-lookup"><span data-stu-id="4b25e-123">Implementations</span></span>

-   [<span data-ttu-id="4b25e-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="4b25e-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="4b25e-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4b25e-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4b25e-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4b25e-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4b25e-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4b25e-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4b25e-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4b25e-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4b25e-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4b25e-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="4b25e-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4b25e-130">Windows 2000 Server</span></span>



| <span data-ttu-id="4b25e-131">Entrée</span><span class="sxs-lookup"><span data-stu-id="4b25e-131">Entry</span></span> | <span data-ttu-id="4b25e-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="4b25e-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="4b25e-133">ID de lien</span><span class="sxs-lookup"><span data-stu-id="4b25e-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="4b25e-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4b25e-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="4b25e-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="4b25e-135">System-Only</span></span>            | <span data-ttu-id="4b25e-136">Faux</span><span class="sxs-lookup"><span data-stu-id="4b25e-136">False</span></span>                                        |
| <span data-ttu-id="4b25e-137">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="4b25e-137">Is-Single-Valued</span></span>       | <span data-ttu-id="4b25e-138">Vrai</span><span class="sxs-lookup"><span data-stu-id="4b25e-138">True</span></span>                                         |
| <span data-ttu-id="4b25e-139">Est indexé</span><span class="sxs-lookup"><span data-stu-id="4b25e-139">Is Indexed</span></span>             | <span data-ttu-id="4b25e-140">Faux</span><span class="sxs-lookup"><span data-stu-id="4b25e-140">False</span></span>                                        |
| <span data-ttu-id="4b25e-141">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="4b25e-141">In Global Catalog</span></span>      | <span data-ttu-id="4b25e-142">Faux</span><span class="sxs-lookup"><span data-stu-id="4b25e-142">False</span></span>                                        |
| <span data-ttu-id="4b25e-143">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="4b25e-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="4b25e-144">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="4b25e-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="4b25e-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4b25e-145">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="4b25e-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4b25e-146">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="4b25e-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4b25e-147">Search-Flags</span></span>           | <span data-ttu-id="4b25e-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4b25e-148">0x00000000</span></span>                                   |
| <span data-ttu-id="4b25e-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4b25e-149">System-Flags</span></span>           | <span data-ttu-id="4b25e-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4b25e-150">0x00000010</span></span>                                   |
| <span data-ttu-id="4b25e-151">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="4b25e-151">Classes used in</span></span>        | [<span data-ttu-id="4b25e-152">**ACS-sous-réseau**</span><span class="sxs-lookup"><span data-stu-id="4b25e-152">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="4b25e-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4b25e-153">Windows Server 2003</span></span>



| <span data-ttu-id="4b25e-154">Entrée</span><span class="sxs-lookup"><span data-stu-id="4b25e-154">Entry</span></span> | <span data-ttu-id="4b25e-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="4b25e-155">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="4b25e-156">ID de lien</span><span class="sxs-lookup"><span data-stu-id="4b25e-156">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="4b25e-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4b25e-157">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="4b25e-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="4b25e-158">System-Only</span></span>            | <span data-ttu-id="4b25e-159">Faux</span><span class="sxs-lookup"><span data-stu-id="4b25e-159">False</span></span>                                        |
| <span data-ttu-id="4b25e-160">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="4b25e-160">Is-Single-Valued</span></span>       | <span data-ttu-id="4b25e-161">Vrai</span><span class="sxs-lookup"><span data-stu-id="4b25e-161">True</span></span>                                         |
| <span data-ttu-id="4b25e-162">Est indexé</span><span class="sxs-lookup"><span data-stu-id="4b25e-162">Is Indexed</span></span>             | <span data-ttu-id="4b25e-163">Faux</span><span class="sxs-lookup"><span data-stu-id="4b25e-163">False</span></span>                                        |
| <span data-ttu-id="4b25e-164">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="4b25e-164">In Global Catalog</span></span>      | <span data-ttu-id="4b25e-165">Faux</span><span class="sxs-lookup"><span data-stu-id="4b25e-165">False</span></span>                                        |
| <span data-ttu-id="4b25e-166">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="4b25e-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="4b25e-167">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="4b25e-167">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="4b25e-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4b25e-168">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="4b25e-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4b25e-169">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="4b25e-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4b25e-170">Search-Flags</span></span>           | <span data-ttu-id="4b25e-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4b25e-171">0x00000000</span></span>                                   |
| <span data-ttu-id="4b25e-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4b25e-172">System-Flags</span></span>           | <span data-ttu-id="4b25e-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4b25e-173">0x00000010</span></span>                                   |
| <span data-ttu-id="4b25e-174">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="4b25e-174">Classes used in</span></span>        | [<span data-ttu-id="4b25e-175">**ACS-sous-réseau**</span><span class="sxs-lookup"><span data-stu-id="4b25e-175">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4b25e-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4b25e-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4b25e-177">Entrée</span><span class="sxs-lookup"><span data-stu-id="4b25e-177">Entry</span></span> | <span data-ttu-id="4b25e-178">Valeur</span><span class="sxs-lookup"><span data-stu-id="4b25e-178">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="4b25e-179">ID de lien</span><span class="sxs-lookup"><span data-stu-id="4b25e-179">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="4b25e-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4b25e-180">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="4b25e-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="4b25e-181">System-Only</span></span>            | <span data-ttu-id="4b25e-182">Faux</span><span class="sxs-lookup"><span data-stu-id="4b25e-182">False</span></span>                                        |
| <span data-ttu-id="4b25e-183">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="4b25e-183">Is-Single-Valued</span></span>       | <span data-ttu-id="4b25e-184">Vrai</span><span class="sxs-lookup"><span data-stu-id="4b25e-184">True</span></span>                                         |
| <span data-ttu-id="4b25e-185">Est indexé</span><span class="sxs-lookup"><span data-stu-id="4b25e-185">Is Indexed</span></span>             | <span data-ttu-id="4b25e-186">Faux</span><span class="sxs-lookup"><span data-stu-id="4b25e-186">False</span></span>                                        |
| <span data-ttu-id="4b25e-187">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="4b25e-187">In Global Catalog</span></span>      | <span data-ttu-id="4b25e-188">Faux</span><span class="sxs-lookup"><span data-stu-id="4b25e-188">False</span></span>                                        |
| <span data-ttu-id="4b25e-189">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="4b25e-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="4b25e-190">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="4b25e-190">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="4b25e-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4b25e-191">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="4b25e-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4b25e-192">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="4b25e-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4b25e-193">Search-Flags</span></span>           | <span data-ttu-id="4b25e-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4b25e-194">0x00000000</span></span>                                   |
| <span data-ttu-id="4b25e-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4b25e-195">System-Flags</span></span>           | <span data-ttu-id="4b25e-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4b25e-196">0x00000010</span></span>                                   |
| <span data-ttu-id="4b25e-197">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="4b25e-197">Classes used in</span></span>        | [<span data-ttu-id="4b25e-198">**ACS-sous-réseau**</span><span class="sxs-lookup"><span data-stu-id="4b25e-198">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4b25e-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4b25e-199">Windows Server 2008</span></span>



| <span data-ttu-id="4b25e-200">Entrée</span><span class="sxs-lookup"><span data-stu-id="4b25e-200">Entry</span></span> | <span data-ttu-id="4b25e-201">Valeur</span><span class="sxs-lookup"><span data-stu-id="4b25e-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="4b25e-202">ID de lien</span><span class="sxs-lookup"><span data-stu-id="4b25e-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="4b25e-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4b25e-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="4b25e-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="4b25e-204">System-Only</span></span>            | <span data-ttu-id="4b25e-205">Faux</span><span class="sxs-lookup"><span data-stu-id="4b25e-205">False</span></span>                                        |
| <span data-ttu-id="4b25e-206">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="4b25e-206">Is-Single-Valued</span></span>       | <span data-ttu-id="4b25e-207">Vrai</span><span class="sxs-lookup"><span data-stu-id="4b25e-207">True</span></span>                                         |
| <span data-ttu-id="4b25e-208">Est indexé</span><span class="sxs-lookup"><span data-stu-id="4b25e-208">Is Indexed</span></span>             | <span data-ttu-id="4b25e-209">Faux</span><span class="sxs-lookup"><span data-stu-id="4b25e-209">False</span></span>                                        |
| <span data-ttu-id="4b25e-210">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="4b25e-210">In Global Catalog</span></span>      | <span data-ttu-id="4b25e-211">Faux</span><span class="sxs-lookup"><span data-stu-id="4b25e-211">False</span></span>                                        |
| <span data-ttu-id="4b25e-212">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="4b25e-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="4b25e-213">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="4b25e-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="4b25e-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4b25e-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="4b25e-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4b25e-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="4b25e-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4b25e-216">Search-Flags</span></span>           | <span data-ttu-id="4b25e-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4b25e-217">0x00000000</span></span>                                   |
| <span data-ttu-id="4b25e-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4b25e-218">System-Flags</span></span>           | <span data-ttu-id="4b25e-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4b25e-219">0x00000010</span></span>                                   |
| <span data-ttu-id="4b25e-220">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="4b25e-220">Classes used in</span></span>        | [<span data-ttu-id="4b25e-221">**ACS-sous-réseau**</span><span class="sxs-lookup"><span data-stu-id="4b25e-221">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4b25e-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4b25e-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4b25e-223">Entrée</span><span class="sxs-lookup"><span data-stu-id="4b25e-223">Entry</span></span> | <span data-ttu-id="4b25e-224">Valeur</span><span class="sxs-lookup"><span data-stu-id="4b25e-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="4b25e-225">ID de lien</span><span class="sxs-lookup"><span data-stu-id="4b25e-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="4b25e-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4b25e-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="4b25e-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="4b25e-227">System-Only</span></span>            | <span data-ttu-id="4b25e-228">Faux</span><span class="sxs-lookup"><span data-stu-id="4b25e-228">False</span></span>                                        |
| <span data-ttu-id="4b25e-229">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="4b25e-229">Is-Single-Valued</span></span>       | <span data-ttu-id="4b25e-230">Vrai</span><span class="sxs-lookup"><span data-stu-id="4b25e-230">True</span></span>                                         |
| <span data-ttu-id="4b25e-231">Est indexé</span><span class="sxs-lookup"><span data-stu-id="4b25e-231">Is Indexed</span></span>             | <span data-ttu-id="4b25e-232">Faux</span><span class="sxs-lookup"><span data-stu-id="4b25e-232">False</span></span>                                        |
| <span data-ttu-id="4b25e-233">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="4b25e-233">In Global Catalog</span></span>      | <span data-ttu-id="4b25e-234">Faux</span><span class="sxs-lookup"><span data-stu-id="4b25e-234">False</span></span>                                        |
| <span data-ttu-id="4b25e-235">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="4b25e-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="4b25e-236">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="4b25e-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="4b25e-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4b25e-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="4b25e-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4b25e-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="4b25e-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4b25e-239">Search-Flags</span></span>           | <span data-ttu-id="4b25e-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4b25e-240">0x00000000</span></span>                                   |
| <span data-ttu-id="4b25e-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4b25e-241">System-Flags</span></span>           | <span data-ttu-id="4b25e-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4b25e-242">0x00000010</span></span>                                   |
| <span data-ttu-id="4b25e-243">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="4b25e-243">Classes used in</span></span>        | [<span data-ttu-id="4b25e-244">**ACS-sous-réseau**</span><span class="sxs-lookup"><span data-stu-id="4b25e-244">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4b25e-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4b25e-245">Windows Server 2012</span></span>



| <span data-ttu-id="4b25e-246">Entrée</span><span class="sxs-lookup"><span data-stu-id="4b25e-246">Entry</span></span> | <span data-ttu-id="4b25e-247">Valeur</span><span class="sxs-lookup"><span data-stu-id="4b25e-247">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="4b25e-248">ID de lien</span><span class="sxs-lookup"><span data-stu-id="4b25e-248">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="4b25e-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4b25e-249">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="4b25e-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="4b25e-250">System-Only</span></span>            | <span data-ttu-id="4b25e-251">Faux</span><span class="sxs-lookup"><span data-stu-id="4b25e-251">False</span></span>                                        |
| <span data-ttu-id="4b25e-252">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="4b25e-252">Is-Single-Valued</span></span>       | <span data-ttu-id="4b25e-253">Vrai</span><span class="sxs-lookup"><span data-stu-id="4b25e-253">True</span></span>                                         |
| <span data-ttu-id="4b25e-254">Est indexé</span><span class="sxs-lookup"><span data-stu-id="4b25e-254">Is Indexed</span></span>             | <span data-ttu-id="4b25e-255">Faux</span><span class="sxs-lookup"><span data-stu-id="4b25e-255">False</span></span>                                        |
| <span data-ttu-id="4b25e-256">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="4b25e-256">In Global Catalog</span></span>      | <span data-ttu-id="4b25e-257">Faux</span><span class="sxs-lookup"><span data-stu-id="4b25e-257">False</span></span>                                        |
| <span data-ttu-id="4b25e-258">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="4b25e-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="4b25e-259">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="4b25e-259">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="4b25e-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4b25e-260">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="4b25e-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4b25e-261">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="4b25e-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4b25e-262">Search-Flags</span></span>           | <span data-ttu-id="4b25e-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4b25e-263">0x00000000</span></span>                                   |
| <span data-ttu-id="4b25e-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4b25e-264">System-Flags</span></span>           | <span data-ttu-id="4b25e-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4b25e-265">0x00000010</span></span>                                   |
| <span data-ttu-id="4b25e-266">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="4b25e-266">Classes used in</span></span>        | [<span data-ttu-id="4b25e-267">**ACS-sous-réseau**</span><span class="sxs-lookup"><span data-stu-id="4b25e-267">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 





