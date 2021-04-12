---
title: Inter-site-topologie-attribut de basculement
description: Indique le temps qui doit s’écouler depuis la dernière activité Keep-Alive pour que le générateur de topologie inter-site soit considéré comme mort.
ms.assetid: d351dbec-d5a3-46e1-87a9-0856d19e07c6
ms.tgt_platform: multiple
keywords:
- Inter-site-topologie-schéma AD d’attribut de basculement
- Schéma AD de l’attribut interSiteTopologyFailover
topic_type:
- apiref
api_name:
- Inter-Site-Topology-Failover
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78c4e9cad98bade7fd69178a8fce795d0b92f35b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104480189"
---
# <a name="inter-site-topology-failover-attribute"></a><span data-ttu-id="d5663-105">Inter-site-topologie-attribut de basculement</span><span class="sxs-lookup"><span data-stu-id="d5663-105">Inter-Site-Topology-Failover attribute</span></span>

<span data-ttu-id="d5663-106">Indique le temps qui doit s’écouler depuis la dernière activité Keep-Alive pour que le générateur de topologie inter-site soit considéré comme mort.</span><span class="sxs-lookup"><span data-stu-id="d5663-106">Indicates how much time must transpire since the last keep-alive for the inter-site topology generator to be considered dead.</span></span>



| <span data-ttu-id="d5663-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="d5663-107">Entry</span></span> | <span data-ttu-id="d5663-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="d5663-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="d5663-109">CN</span><span class="sxs-lookup"><span data-stu-id="d5663-109">CN</span></span>                | <span data-ttu-id="d5663-110">Inter-site-topologie-basculement</span><span class="sxs-lookup"><span data-stu-id="d5663-110">Inter-Site-Topology-Failover</span></span>         |
| <span data-ttu-id="d5663-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="d5663-111">Ldap-Display-Name</span></span> | <span data-ttu-id="d5663-112">interSiteTopologyFailover</span><span class="sxs-lookup"><span data-stu-id="d5663-112">interSiteTopologyFailover</span></span>            |
| <span data-ttu-id="d5663-113">Taille</span><span class="sxs-lookup"><span data-stu-id="d5663-113">Size</span></span>              | <span data-ttu-id="d5663-114">4 octets</span><span class="sxs-lookup"><span data-stu-id="d5663-114">4 bytes</span></span>                              |
| <span data-ttu-id="d5663-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="d5663-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="d5663-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="d5663-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="d5663-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d5663-117">Attribute-Id</span></span>      | <span data-ttu-id="d5663-118">1.2.840.113556.1.4.1248</span><span class="sxs-lookup"><span data-stu-id="d5663-118">1.2.840.113556.1.4.1248</span></span>              |
| <span data-ttu-id="d5663-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="d5663-119">System-Id-Guid</span></span>    | <span data-ttu-id="d5663-120">b7c69e60-2cc7-11d2-854e-00a0c983f608</span><span class="sxs-lookup"><span data-stu-id="d5663-120">b7c69e60-2cc7-11d2-854e-00a0c983f608</span></span> |
| <span data-ttu-id="d5663-121">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d5663-121">Syntax</span></span>            | [<span data-ttu-id="d5663-122">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="d5663-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="d5663-123">Implémentations</span><span class="sxs-lookup"><span data-stu-id="d5663-123">Implementations</span></span>

-   [<span data-ttu-id="d5663-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d5663-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d5663-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d5663-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d5663-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="d5663-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="d5663-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d5663-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d5663-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d5663-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d5663-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d5663-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d5663-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d5663-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d5663-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d5663-131">Windows 2000 Server</span></span>



| <span data-ttu-id="d5663-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="d5663-132">Entry</span></span> | <span data-ttu-id="d5663-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="d5663-133">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="d5663-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d5663-134">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d5663-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d5663-135">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d5663-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="d5663-136">System-Only</span></span>            | <span data-ttu-id="d5663-137">Faux</span><span class="sxs-lookup"><span data-stu-id="d5663-137">False</span></span>                                                       |
| <span data-ttu-id="d5663-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d5663-138">Is-Single-Valued</span></span>       | <span data-ttu-id="d5663-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="d5663-139">True</span></span>                                                        |
| <span data-ttu-id="d5663-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d5663-140">Is Indexed</span></span>             | <span data-ttu-id="d5663-141">Faux</span><span class="sxs-lookup"><span data-stu-id="d5663-141">False</span></span>                                                       |
| <span data-ttu-id="d5663-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d5663-142">In Global Catalog</span></span>      | <span data-ttu-id="d5663-143">Faux</span><span class="sxs-lookup"><span data-stu-id="d5663-143">False</span></span>                                                       |
| <span data-ttu-id="d5663-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d5663-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="d5663-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d5663-145">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="d5663-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d5663-146">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="d5663-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d5663-147">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="d5663-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d5663-148">Search-Flags</span></span>           | <span data-ttu-id="d5663-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d5663-149">0x00000000</span></span>                                                  |
| <span data-ttu-id="d5663-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d5663-150">System-Flags</span></span>           | <span data-ttu-id="d5663-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d5663-151">0x00000010</span></span>                                                  |
| <span data-ttu-id="d5663-152">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d5663-152">Classes used in</span></span>        | [<span data-ttu-id="d5663-153">**NTDS-site-paramètres**</span><span class="sxs-lookup"><span data-stu-id="d5663-153">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d5663-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d5663-154">Windows Server 2003</span></span>



| <span data-ttu-id="d5663-155">Entrée</span><span class="sxs-lookup"><span data-stu-id="d5663-155">Entry</span></span> | <span data-ttu-id="d5663-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="d5663-156">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="d5663-157">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d5663-157">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d5663-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d5663-158">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d5663-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="d5663-159">System-Only</span></span>            | <span data-ttu-id="d5663-160">Faux</span><span class="sxs-lookup"><span data-stu-id="d5663-160">False</span></span>                                                       |
| <span data-ttu-id="d5663-161">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d5663-161">Is-Single-Valued</span></span>       | <span data-ttu-id="d5663-162">Vrai</span><span class="sxs-lookup"><span data-stu-id="d5663-162">True</span></span>                                                        |
| <span data-ttu-id="d5663-163">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d5663-163">Is Indexed</span></span>             | <span data-ttu-id="d5663-164">Faux</span><span class="sxs-lookup"><span data-stu-id="d5663-164">False</span></span>                                                       |
| <span data-ttu-id="d5663-165">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d5663-165">In Global Catalog</span></span>      | <span data-ttu-id="d5663-166">Faux</span><span class="sxs-lookup"><span data-stu-id="d5663-166">False</span></span>                                                       |
| <span data-ttu-id="d5663-167">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d5663-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="d5663-168">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d5663-168">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="d5663-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d5663-169">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="d5663-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d5663-170">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="d5663-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d5663-171">Search-Flags</span></span>           | <span data-ttu-id="d5663-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d5663-172">0x00000000</span></span>                                                  |
| <span data-ttu-id="d5663-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d5663-173">System-Flags</span></span>           | <span data-ttu-id="d5663-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d5663-174">0x00000010</span></span>                                                  |
| <span data-ttu-id="d5663-175">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d5663-175">Classes used in</span></span>        | [<span data-ttu-id="d5663-176">**NTDS-site-paramètres**</span><span class="sxs-lookup"><span data-stu-id="d5663-176">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="adam"></a><span data-ttu-id="d5663-177">ADAM</span><span class="sxs-lookup"><span data-stu-id="d5663-177">ADAM</span></span>



| <span data-ttu-id="d5663-178">Entrée</span><span class="sxs-lookup"><span data-stu-id="d5663-178">Entry</span></span> | <span data-ttu-id="d5663-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="d5663-179">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="d5663-180">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d5663-180">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d5663-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d5663-181">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d5663-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="d5663-182">System-Only</span></span>            | <span data-ttu-id="d5663-183">Faux</span><span class="sxs-lookup"><span data-stu-id="d5663-183">False</span></span>                                                       |
| <span data-ttu-id="d5663-184">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d5663-184">Is-Single-Valued</span></span>       | <span data-ttu-id="d5663-185">Vrai</span><span class="sxs-lookup"><span data-stu-id="d5663-185">True</span></span>                                                        |
| <span data-ttu-id="d5663-186">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d5663-186">Is Indexed</span></span>             | <span data-ttu-id="d5663-187">Faux</span><span class="sxs-lookup"><span data-stu-id="d5663-187">False</span></span>                                                       |
| <span data-ttu-id="d5663-188">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d5663-188">In Global Catalog</span></span>      | <span data-ttu-id="d5663-189">Faux</span><span class="sxs-lookup"><span data-stu-id="d5663-189">False</span></span>                                                       |
| <span data-ttu-id="d5663-190">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d5663-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="d5663-191">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d5663-191">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="d5663-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d5663-192">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="d5663-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d5663-193">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="d5663-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d5663-194">Search-Flags</span></span>           | <span data-ttu-id="d5663-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d5663-195">0x00000000</span></span>                                                  |
| <span data-ttu-id="d5663-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d5663-196">System-Flags</span></span>           | <span data-ttu-id="d5663-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d5663-197">0x00000010</span></span>                                                  |
| <span data-ttu-id="d5663-198">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d5663-198">Classes used in</span></span>        | [<span data-ttu-id="d5663-199">**NTDS-site-paramètres**</span><span class="sxs-lookup"><span data-stu-id="d5663-199">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d5663-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d5663-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d5663-201">Entrée</span><span class="sxs-lookup"><span data-stu-id="d5663-201">Entry</span></span> | <span data-ttu-id="d5663-202">Valeur</span><span class="sxs-lookup"><span data-stu-id="d5663-202">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="d5663-203">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d5663-203">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d5663-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d5663-204">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d5663-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="d5663-205">System-Only</span></span>            | <span data-ttu-id="d5663-206">Faux</span><span class="sxs-lookup"><span data-stu-id="d5663-206">False</span></span>                                                       |
| <span data-ttu-id="d5663-207">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d5663-207">Is-Single-Valued</span></span>       | <span data-ttu-id="d5663-208">Vrai</span><span class="sxs-lookup"><span data-stu-id="d5663-208">True</span></span>                                                        |
| <span data-ttu-id="d5663-209">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d5663-209">Is Indexed</span></span>             | <span data-ttu-id="d5663-210">Faux</span><span class="sxs-lookup"><span data-stu-id="d5663-210">False</span></span>                                                       |
| <span data-ttu-id="d5663-211">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d5663-211">In Global Catalog</span></span>      | <span data-ttu-id="d5663-212">Faux</span><span class="sxs-lookup"><span data-stu-id="d5663-212">False</span></span>                                                       |
| <span data-ttu-id="d5663-213">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d5663-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="d5663-214">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d5663-214">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="d5663-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d5663-215">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="d5663-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d5663-216">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="d5663-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d5663-217">Search-Flags</span></span>           | <span data-ttu-id="d5663-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d5663-218">0x00000000</span></span>                                                  |
| <span data-ttu-id="d5663-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d5663-219">System-Flags</span></span>           | <span data-ttu-id="d5663-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d5663-220">0x00000010</span></span>                                                  |
| <span data-ttu-id="d5663-221">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d5663-221">Classes used in</span></span>        | [<span data-ttu-id="d5663-222">**NTDS-site-paramètres**</span><span class="sxs-lookup"><span data-stu-id="d5663-222">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d5663-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d5663-223">Windows Server 2008</span></span>



| <span data-ttu-id="d5663-224">Entrée</span><span class="sxs-lookup"><span data-stu-id="d5663-224">Entry</span></span> | <span data-ttu-id="d5663-225">Valeur</span><span class="sxs-lookup"><span data-stu-id="d5663-225">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="d5663-226">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d5663-226">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d5663-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d5663-227">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d5663-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="d5663-228">System-Only</span></span>            | <span data-ttu-id="d5663-229">Faux</span><span class="sxs-lookup"><span data-stu-id="d5663-229">False</span></span>                                                       |
| <span data-ttu-id="d5663-230">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d5663-230">Is-Single-Valued</span></span>       | <span data-ttu-id="d5663-231">Vrai</span><span class="sxs-lookup"><span data-stu-id="d5663-231">True</span></span>                                                        |
| <span data-ttu-id="d5663-232">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d5663-232">Is Indexed</span></span>             | <span data-ttu-id="d5663-233">Faux</span><span class="sxs-lookup"><span data-stu-id="d5663-233">False</span></span>                                                       |
| <span data-ttu-id="d5663-234">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d5663-234">In Global Catalog</span></span>      | <span data-ttu-id="d5663-235">Faux</span><span class="sxs-lookup"><span data-stu-id="d5663-235">False</span></span>                                                       |
| <span data-ttu-id="d5663-236">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d5663-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="d5663-237">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d5663-237">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="d5663-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d5663-238">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="d5663-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d5663-239">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="d5663-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d5663-240">Search-Flags</span></span>           | <span data-ttu-id="d5663-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d5663-241">0x00000000</span></span>                                                  |
| <span data-ttu-id="d5663-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d5663-242">System-Flags</span></span>           | <span data-ttu-id="d5663-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d5663-243">0x00000010</span></span>                                                  |
| <span data-ttu-id="d5663-244">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d5663-244">Classes used in</span></span>        | [<span data-ttu-id="d5663-245">**NTDS-site-paramètres**</span><span class="sxs-lookup"><span data-stu-id="d5663-245">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d5663-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d5663-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d5663-247">Entrée</span><span class="sxs-lookup"><span data-stu-id="d5663-247">Entry</span></span> | <span data-ttu-id="d5663-248">Valeur</span><span class="sxs-lookup"><span data-stu-id="d5663-248">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="d5663-249">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d5663-249">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d5663-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d5663-250">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d5663-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="d5663-251">System-Only</span></span>            | <span data-ttu-id="d5663-252">Faux</span><span class="sxs-lookup"><span data-stu-id="d5663-252">False</span></span>                                                       |
| <span data-ttu-id="d5663-253">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d5663-253">Is-Single-Valued</span></span>       | <span data-ttu-id="d5663-254">Vrai</span><span class="sxs-lookup"><span data-stu-id="d5663-254">True</span></span>                                                        |
| <span data-ttu-id="d5663-255">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d5663-255">Is Indexed</span></span>             | <span data-ttu-id="d5663-256">Faux</span><span class="sxs-lookup"><span data-stu-id="d5663-256">False</span></span>                                                       |
| <span data-ttu-id="d5663-257">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d5663-257">In Global Catalog</span></span>      | <span data-ttu-id="d5663-258">Faux</span><span class="sxs-lookup"><span data-stu-id="d5663-258">False</span></span>                                                       |
| <span data-ttu-id="d5663-259">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d5663-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="d5663-260">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d5663-260">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="d5663-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d5663-261">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="d5663-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d5663-262">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="d5663-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d5663-263">Search-Flags</span></span>           | <span data-ttu-id="d5663-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d5663-264">0x00000000</span></span>                                                  |
| <span data-ttu-id="d5663-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d5663-265">System-Flags</span></span>           | <span data-ttu-id="d5663-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d5663-266">0x00000010</span></span>                                                  |
| <span data-ttu-id="d5663-267">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d5663-267">Classes used in</span></span>        | [<span data-ttu-id="d5663-268">**NTDS-site-paramètres**</span><span class="sxs-lookup"><span data-stu-id="d5663-268">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d5663-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d5663-269">Windows Server 2012</span></span>



| <span data-ttu-id="d5663-270">Entrée</span><span class="sxs-lookup"><span data-stu-id="d5663-270">Entry</span></span> | <span data-ttu-id="d5663-271">Valeur</span><span class="sxs-lookup"><span data-stu-id="d5663-271">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="d5663-272">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d5663-272">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d5663-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d5663-273">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d5663-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="d5663-274">System-Only</span></span>            | <span data-ttu-id="d5663-275">Faux</span><span class="sxs-lookup"><span data-stu-id="d5663-275">False</span></span>                                                       |
| <span data-ttu-id="d5663-276">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d5663-276">Is-Single-Valued</span></span>       | <span data-ttu-id="d5663-277">Vrai</span><span class="sxs-lookup"><span data-stu-id="d5663-277">True</span></span>                                                        |
| <span data-ttu-id="d5663-278">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d5663-278">Is Indexed</span></span>             | <span data-ttu-id="d5663-279">Faux</span><span class="sxs-lookup"><span data-stu-id="d5663-279">False</span></span>                                                       |
| <span data-ttu-id="d5663-280">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d5663-280">In Global Catalog</span></span>      | <span data-ttu-id="d5663-281">Faux</span><span class="sxs-lookup"><span data-stu-id="d5663-281">False</span></span>                                                       |
| <span data-ttu-id="d5663-282">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d5663-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="d5663-283">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d5663-283">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="d5663-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d5663-284">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="d5663-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d5663-285">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="d5663-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d5663-286">Search-Flags</span></span>           | <span data-ttu-id="d5663-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d5663-287">0x00000000</span></span>                                                  |
| <span data-ttu-id="d5663-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d5663-288">System-Flags</span></span>           | <span data-ttu-id="d5663-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d5663-289">0x00000010</span></span>                                                  |
| <span data-ttu-id="d5663-290">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d5663-290">Classes used in</span></span>        | [<span data-ttu-id="d5663-291">**NTDS-site-paramètres**</span><span class="sxs-lookup"><span data-stu-id="d5663-291">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



 

 





