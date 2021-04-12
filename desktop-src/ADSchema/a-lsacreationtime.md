---
title: LSA-attribut de date/heure de création
description: L’attribut LSA-Creation-Time est utilisé pour prendre en charge la réplication vers des domaines Windows NT 4,0.
ms.assetid: a5446cbf-aa35-4ea6-a2e0-9d0ea58edaf1
ms.tgt_platform: multiple
keywords:
- LSA-schéma AD d’attribut de création
- Schéma AD de l’attribut lSACreationTime
topic_type:
- apiref
api_name:
- LSA-Creation-Time
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f32092e7d71d02807f4700d381da0ce099ccaf7
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104385343"
---
# <a name="lsa-creation-time-attribute"></a><span data-ttu-id="13d22-105">LSA-attribut de date/heure de création</span><span class="sxs-lookup"><span data-stu-id="13d22-105">LSA-Creation-Time attribute</span></span>

<span data-ttu-id="13d22-106">L’attribut **LSA-Creation-Time** est utilisé pour prendre en charge la réplication vers des domaines Windows NT 4,0.</span><span class="sxs-lookup"><span data-stu-id="13d22-106">The **LSA-Creation-Time** attribute is used to support replication to Windows NT 4.0 domains.</span></span>



| <span data-ttu-id="13d22-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="13d22-107">Entry</span></span> | <span data-ttu-id="13d22-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="13d22-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="13d22-109">CN</span><span class="sxs-lookup"><span data-stu-id="13d22-109">CN</span></span>                | <span data-ttu-id="13d22-110">LSA-temps de création</span><span class="sxs-lookup"><span data-stu-id="13d22-110">LSA-Creation-Time</span></span>                    |
| <span data-ttu-id="13d22-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="13d22-111">Ldap-Display-Name</span></span> | <span data-ttu-id="13d22-112">lSACreationTime</span><span class="sxs-lookup"><span data-stu-id="13d22-112">lSACreationTime</span></span>                      |
| <span data-ttu-id="13d22-113">Taille</span><span class="sxs-lookup"><span data-stu-id="13d22-113">Size</span></span>              | <span data-ttu-id="13d22-114">8 octets</span><span class="sxs-lookup"><span data-stu-id="13d22-114">8 bytes</span></span>                              |
| <span data-ttu-id="13d22-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="13d22-115">Update Privilege</span></span>  | <span data-ttu-id="13d22-116">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="13d22-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="13d22-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="13d22-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="13d22-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="13d22-118">Attribute-Id</span></span>      | <span data-ttu-id="13d22-119">1.2.840.113556.1.4.66</span><span class="sxs-lookup"><span data-stu-id="13d22-119">1.2.840.113556.1.4.66</span></span>                |
| <span data-ttu-id="13d22-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="13d22-120">System-Id-Guid</span></span>    | <span data-ttu-id="13d22-121">bf9679ad-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="13d22-121">bf9679ad-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="13d22-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="13d22-122">Syntax</span></span>            | [<span data-ttu-id="13d22-123">**Défini**</span><span class="sxs-lookup"><span data-stu-id="13d22-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="13d22-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="13d22-124">Implementations</span></span>

-   [<span data-ttu-id="13d22-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="13d22-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="13d22-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="13d22-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="13d22-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="13d22-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="13d22-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="13d22-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="13d22-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="13d22-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="13d22-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="13d22-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="13d22-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="13d22-131">Windows 2000 Server</span></span>



| <span data-ttu-id="13d22-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="13d22-132">Entry</span></span> | <span data-ttu-id="13d22-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="13d22-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="13d22-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="13d22-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="13d22-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="13d22-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="13d22-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="13d22-136">System-Only</span></span>            | <span data-ttu-id="13d22-137">Faux</span><span class="sxs-lookup"><span data-stu-id="13d22-137">False</span></span>                                        |
| <span data-ttu-id="13d22-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="13d22-138">Is-Single-Valued</span></span>       | <span data-ttu-id="13d22-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="13d22-139">True</span></span>                                         |
| <span data-ttu-id="13d22-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="13d22-140">Is Indexed</span></span>             | <span data-ttu-id="13d22-141">Faux</span><span class="sxs-lookup"><span data-stu-id="13d22-141">False</span></span>                                        |
| <span data-ttu-id="13d22-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="13d22-142">In Global Catalog</span></span>      | <span data-ttu-id="13d22-143">Faux</span><span class="sxs-lookup"><span data-stu-id="13d22-143">False</span></span>                                        |
| <span data-ttu-id="13d22-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="13d22-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="13d22-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="13d22-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="13d22-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="13d22-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="13d22-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="13d22-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="13d22-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="13d22-148">Search-Flags</span></span>           | <span data-ttu-id="13d22-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="13d22-149">0x00000000</span></span>                                   |
| <span data-ttu-id="13d22-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="13d22-150">System-Flags</span></span>           | <span data-ttu-id="13d22-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="13d22-151">0x00000010</span></span>                                   |
| <span data-ttu-id="13d22-152">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="13d22-152">Classes used in</span></span>        | [<span data-ttu-id="13d22-153">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="13d22-153">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="13d22-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="13d22-154">Windows Server 2003</span></span>



| <span data-ttu-id="13d22-155">Entrée</span><span class="sxs-lookup"><span data-stu-id="13d22-155">Entry</span></span> | <span data-ttu-id="13d22-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="13d22-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="13d22-157">ID de lien</span><span class="sxs-lookup"><span data-stu-id="13d22-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="13d22-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="13d22-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="13d22-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="13d22-159">System-Only</span></span>            | <span data-ttu-id="13d22-160">Faux</span><span class="sxs-lookup"><span data-stu-id="13d22-160">False</span></span>                                        |
| <span data-ttu-id="13d22-161">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="13d22-161">Is-Single-Valued</span></span>       | <span data-ttu-id="13d22-162">Vrai</span><span class="sxs-lookup"><span data-stu-id="13d22-162">True</span></span>                                         |
| <span data-ttu-id="13d22-163">Est indexé</span><span class="sxs-lookup"><span data-stu-id="13d22-163">Is Indexed</span></span>             | <span data-ttu-id="13d22-164">Faux</span><span class="sxs-lookup"><span data-stu-id="13d22-164">False</span></span>                                        |
| <span data-ttu-id="13d22-165">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="13d22-165">In Global Catalog</span></span>      | <span data-ttu-id="13d22-166">Faux</span><span class="sxs-lookup"><span data-stu-id="13d22-166">False</span></span>                                        |
| <span data-ttu-id="13d22-167">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="13d22-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="13d22-168">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="13d22-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="13d22-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="13d22-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="13d22-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="13d22-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="13d22-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="13d22-171">Search-Flags</span></span>           | <span data-ttu-id="13d22-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="13d22-172">0x00000000</span></span>                                   |
| <span data-ttu-id="13d22-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="13d22-173">System-Flags</span></span>           | <span data-ttu-id="13d22-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="13d22-174">0x00000010</span></span>                                   |
| <span data-ttu-id="13d22-175">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="13d22-175">Classes used in</span></span>        | [<span data-ttu-id="13d22-176">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="13d22-176">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="13d22-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="13d22-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="13d22-178">Entrée</span><span class="sxs-lookup"><span data-stu-id="13d22-178">Entry</span></span> | <span data-ttu-id="13d22-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="13d22-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="13d22-180">ID de lien</span><span class="sxs-lookup"><span data-stu-id="13d22-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="13d22-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="13d22-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="13d22-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="13d22-182">System-Only</span></span>            | <span data-ttu-id="13d22-183">Faux</span><span class="sxs-lookup"><span data-stu-id="13d22-183">False</span></span>                                        |
| <span data-ttu-id="13d22-184">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="13d22-184">Is-Single-Valued</span></span>       | <span data-ttu-id="13d22-185">Vrai</span><span class="sxs-lookup"><span data-stu-id="13d22-185">True</span></span>                                         |
| <span data-ttu-id="13d22-186">Est indexé</span><span class="sxs-lookup"><span data-stu-id="13d22-186">Is Indexed</span></span>             | <span data-ttu-id="13d22-187">Faux</span><span class="sxs-lookup"><span data-stu-id="13d22-187">False</span></span>                                        |
| <span data-ttu-id="13d22-188">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="13d22-188">In Global Catalog</span></span>      | <span data-ttu-id="13d22-189">Faux</span><span class="sxs-lookup"><span data-stu-id="13d22-189">False</span></span>                                        |
| <span data-ttu-id="13d22-190">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="13d22-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="13d22-191">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="13d22-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="13d22-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="13d22-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="13d22-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="13d22-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="13d22-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="13d22-194">Search-Flags</span></span>           | <span data-ttu-id="13d22-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="13d22-195">0x00000000</span></span>                                   |
| <span data-ttu-id="13d22-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="13d22-196">System-Flags</span></span>           | <span data-ttu-id="13d22-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="13d22-197">0x00000010</span></span>                                   |
| <span data-ttu-id="13d22-198">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="13d22-198">Classes used in</span></span>        | [<span data-ttu-id="13d22-199">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="13d22-199">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="13d22-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="13d22-200">Windows Server 2008</span></span>



| <span data-ttu-id="13d22-201">Entrée</span><span class="sxs-lookup"><span data-stu-id="13d22-201">Entry</span></span> | <span data-ttu-id="13d22-202">Valeur</span><span class="sxs-lookup"><span data-stu-id="13d22-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="13d22-203">ID de lien</span><span class="sxs-lookup"><span data-stu-id="13d22-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="13d22-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="13d22-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="13d22-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="13d22-205">System-Only</span></span>            | <span data-ttu-id="13d22-206">Faux</span><span class="sxs-lookup"><span data-stu-id="13d22-206">False</span></span>                                        |
| <span data-ttu-id="13d22-207">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="13d22-207">Is-Single-Valued</span></span>       | <span data-ttu-id="13d22-208">Vrai</span><span class="sxs-lookup"><span data-stu-id="13d22-208">True</span></span>                                         |
| <span data-ttu-id="13d22-209">Est indexé</span><span class="sxs-lookup"><span data-stu-id="13d22-209">Is Indexed</span></span>             | <span data-ttu-id="13d22-210">Faux</span><span class="sxs-lookup"><span data-stu-id="13d22-210">False</span></span>                                        |
| <span data-ttu-id="13d22-211">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="13d22-211">In Global Catalog</span></span>      | <span data-ttu-id="13d22-212">Faux</span><span class="sxs-lookup"><span data-stu-id="13d22-212">False</span></span>                                        |
| <span data-ttu-id="13d22-213">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="13d22-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="13d22-214">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="13d22-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="13d22-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="13d22-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="13d22-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="13d22-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="13d22-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="13d22-217">Search-Flags</span></span>           | <span data-ttu-id="13d22-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="13d22-218">0x00000000</span></span>                                   |
| <span data-ttu-id="13d22-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="13d22-219">System-Flags</span></span>           | <span data-ttu-id="13d22-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="13d22-220">0x00000010</span></span>                                   |
| <span data-ttu-id="13d22-221">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="13d22-221">Classes used in</span></span>        | [<span data-ttu-id="13d22-222">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="13d22-222">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="13d22-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="13d22-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="13d22-224">Entrée</span><span class="sxs-lookup"><span data-stu-id="13d22-224">Entry</span></span> | <span data-ttu-id="13d22-225">Valeur</span><span class="sxs-lookup"><span data-stu-id="13d22-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="13d22-226">ID de lien</span><span class="sxs-lookup"><span data-stu-id="13d22-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="13d22-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="13d22-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="13d22-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="13d22-228">System-Only</span></span>            | <span data-ttu-id="13d22-229">Faux</span><span class="sxs-lookup"><span data-stu-id="13d22-229">False</span></span>                                        |
| <span data-ttu-id="13d22-230">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="13d22-230">Is-Single-Valued</span></span>       | <span data-ttu-id="13d22-231">Vrai</span><span class="sxs-lookup"><span data-stu-id="13d22-231">True</span></span>                                         |
| <span data-ttu-id="13d22-232">Est indexé</span><span class="sxs-lookup"><span data-stu-id="13d22-232">Is Indexed</span></span>             | <span data-ttu-id="13d22-233">Faux</span><span class="sxs-lookup"><span data-stu-id="13d22-233">False</span></span>                                        |
| <span data-ttu-id="13d22-234">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="13d22-234">In Global Catalog</span></span>      | <span data-ttu-id="13d22-235">Faux</span><span class="sxs-lookup"><span data-stu-id="13d22-235">False</span></span>                                        |
| <span data-ttu-id="13d22-236">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="13d22-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="13d22-237">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="13d22-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="13d22-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="13d22-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="13d22-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="13d22-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="13d22-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="13d22-240">Search-Flags</span></span>           | <span data-ttu-id="13d22-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="13d22-241">0x00000000</span></span>                                   |
| <span data-ttu-id="13d22-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="13d22-242">System-Flags</span></span>           | <span data-ttu-id="13d22-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="13d22-243">0x00000010</span></span>                                   |
| <span data-ttu-id="13d22-244">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="13d22-244">Classes used in</span></span>        | [<span data-ttu-id="13d22-245">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="13d22-245">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="13d22-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="13d22-246">Windows Server 2012</span></span>



| <span data-ttu-id="13d22-247">Entrée</span><span class="sxs-lookup"><span data-stu-id="13d22-247">Entry</span></span> | <span data-ttu-id="13d22-248">Valeur</span><span class="sxs-lookup"><span data-stu-id="13d22-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="13d22-249">ID de lien</span><span class="sxs-lookup"><span data-stu-id="13d22-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="13d22-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="13d22-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="13d22-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="13d22-251">System-Only</span></span>            | <span data-ttu-id="13d22-252">Faux</span><span class="sxs-lookup"><span data-stu-id="13d22-252">False</span></span>                                        |
| <span data-ttu-id="13d22-253">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="13d22-253">Is-Single-Valued</span></span>       | <span data-ttu-id="13d22-254">Vrai</span><span class="sxs-lookup"><span data-stu-id="13d22-254">True</span></span>                                         |
| <span data-ttu-id="13d22-255">Est indexé</span><span class="sxs-lookup"><span data-stu-id="13d22-255">Is Indexed</span></span>             | <span data-ttu-id="13d22-256">Faux</span><span class="sxs-lookup"><span data-stu-id="13d22-256">False</span></span>                                        |
| <span data-ttu-id="13d22-257">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="13d22-257">In Global Catalog</span></span>      | <span data-ttu-id="13d22-258">Faux</span><span class="sxs-lookup"><span data-stu-id="13d22-258">False</span></span>                                        |
| <span data-ttu-id="13d22-259">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="13d22-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="13d22-260">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="13d22-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="13d22-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="13d22-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="13d22-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="13d22-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="13d22-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="13d22-263">Search-Flags</span></span>           | <span data-ttu-id="13d22-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="13d22-264">0x00000000</span></span>                                   |
| <span data-ttu-id="13d22-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="13d22-265">System-Flags</span></span>           | <span data-ttu-id="13d22-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="13d22-266">0x00000010</span></span>                                   |
| <span data-ttu-id="13d22-267">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="13d22-267">Classes used in</span></span>        | [<span data-ttu-id="13d22-268">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="13d22-268">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 





