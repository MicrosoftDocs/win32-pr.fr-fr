---
title: Inter-site-topologie-attribut-générateur
description: Cet attribut sera utilisé pour prendre en charge le basculement pour l’ordinateur désigné comme celui qui exécute le vérificateur de cohérence des connaissances génération de topologie inter-site dans un site donné.
ms.assetid: 077f4331-ead9-4f17-942e-d55cf253d03b
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory inter-site-Topology-Generator Attribute
- Schéma AD de l’attribut interSiteTopologyGenerator
topic_type:
- apiref
api_name:
- Inter-Site-Topology-Generator
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7df7b354d05e882373715e4c49498c9daff41652
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107026"
---
# <a name="inter-site-topology-generator-attribute"></a><span data-ttu-id="7ff16-105">Inter-site-topologie-attribut-générateur</span><span class="sxs-lookup"><span data-stu-id="7ff16-105">Inter-Site-Topology-Generator attribute</span></span>

<span data-ttu-id="7ff16-106">Cet attribut sera utilisé pour prendre en charge le basculement pour l’ordinateur désigné comme celui qui exécute le vérificateur de cohérence des connaissances génération de topologie inter-site dans un site donné.</span><span class="sxs-lookup"><span data-stu-id="7ff16-106">This attribute will be used to support failover for the computer designated as the one that runs Knowledge Consistency Checker inter-site topology generation in a given site.</span></span>



| <span data-ttu-id="7ff16-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="7ff16-107">Entry</span></span> | <span data-ttu-id="7ff16-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ff16-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="7ff16-109">CN</span><span class="sxs-lookup"><span data-stu-id="7ff16-109">CN</span></span>                | <span data-ttu-id="7ff16-110">Inter-site-Topology-Generator</span><span class="sxs-lookup"><span data-stu-id="7ff16-110">Inter-Site-Topology-Generator</span></span>           |
| <span data-ttu-id="7ff16-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="7ff16-111">Ldap-Display-Name</span></span> | <span data-ttu-id="7ff16-112">interSiteTopologyGenerator</span><span class="sxs-lookup"><span data-stu-id="7ff16-112">interSiteTopologyGenerator</span></span>              |
| <span data-ttu-id="7ff16-113">Taille</span><span class="sxs-lookup"><span data-stu-id="7ff16-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="7ff16-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="7ff16-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="7ff16-115">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="7ff16-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="7ff16-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7ff16-116">Attribute-Id</span></span>      | <span data-ttu-id="7ff16-117">1.2.840.113556.1.4.1246</span><span class="sxs-lookup"><span data-stu-id="7ff16-117">1.2.840.113556.1.4.1246</span></span>                 |
| <span data-ttu-id="7ff16-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="7ff16-118">System-Id-Guid</span></span>    | <span data-ttu-id="7ff16-119">b7c69e5e-2cc7-11d2-854e-00a0c983f608</span><span class="sxs-lookup"><span data-stu-id="7ff16-119">b7c69e5e-2cc7-11d2-854e-00a0c983f608</span></span>    |
| <span data-ttu-id="7ff16-120">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7ff16-120">Syntax</span></span>            | [<span data-ttu-id="7ff16-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="7ff16-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="7ff16-122">Implémentations</span><span class="sxs-lookup"><span data-stu-id="7ff16-122">Implementations</span></span>

-   [<span data-ttu-id="7ff16-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7ff16-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7ff16-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7ff16-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7ff16-125">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="7ff16-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="7ff16-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7ff16-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7ff16-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7ff16-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7ff16-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7ff16-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7ff16-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7ff16-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7ff16-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7ff16-130">Windows 2000 Server</span></span>



| <span data-ttu-id="7ff16-131">Entrée</span><span class="sxs-lookup"><span data-stu-id="7ff16-131">Entry</span></span> | <span data-ttu-id="7ff16-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ff16-132">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="7ff16-133">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7ff16-133">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7ff16-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7ff16-134">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7ff16-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="7ff16-135">System-Only</span></span>            | <span data-ttu-id="7ff16-136">Faux</span><span class="sxs-lookup"><span data-stu-id="7ff16-136">False</span></span>                                                       |
| <span data-ttu-id="7ff16-137">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7ff16-137">Is-Single-Valued</span></span>       | <span data-ttu-id="7ff16-138">Vrai</span><span class="sxs-lookup"><span data-stu-id="7ff16-138">True</span></span>                                                        |
| <span data-ttu-id="7ff16-139">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7ff16-139">Is Indexed</span></span>             | <span data-ttu-id="7ff16-140">Faux</span><span class="sxs-lookup"><span data-stu-id="7ff16-140">False</span></span>                                                       |
| <span data-ttu-id="7ff16-141">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7ff16-141">In Global Catalog</span></span>      | <span data-ttu-id="7ff16-142">Faux</span><span class="sxs-lookup"><span data-stu-id="7ff16-142">False</span></span>                                                       |
| <span data-ttu-id="7ff16-143">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7ff16-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="7ff16-144">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7ff16-144">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="7ff16-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7ff16-145">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="7ff16-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7ff16-146">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="7ff16-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7ff16-147">Search-Flags</span></span>           | <span data-ttu-id="7ff16-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7ff16-148">0x00000000</span></span>                                                  |
| <span data-ttu-id="7ff16-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7ff16-149">System-Flags</span></span>           | <span data-ttu-id="7ff16-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7ff16-150">0x00000010</span></span>                                                  |
| <span data-ttu-id="7ff16-151">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7ff16-151">Classes used in</span></span>        | [<span data-ttu-id="7ff16-152">**NTDS-site-paramètres**</span><span class="sxs-lookup"><span data-stu-id="7ff16-152">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7ff16-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7ff16-153">Windows Server 2003</span></span>



| <span data-ttu-id="7ff16-154">Entrée</span><span class="sxs-lookup"><span data-stu-id="7ff16-154">Entry</span></span> | <span data-ttu-id="7ff16-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ff16-155">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="7ff16-156">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7ff16-156">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7ff16-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7ff16-157">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7ff16-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="7ff16-158">System-Only</span></span>            | <span data-ttu-id="7ff16-159">Faux</span><span class="sxs-lookup"><span data-stu-id="7ff16-159">False</span></span>                                                       |
| <span data-ttu-id="7ff16-160">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7ff16-160">Is-Single-Valued</span></span>       | <span data-ttu-id="7ff16-161">Vrai</span><span class="sxs-lookup"><span data-stu-id="7ff16-161">True</span></span>                                                        |
| <span data-ttu-id="7ff16-162">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7ff16-162">Is Indexed</span></span>             | <span data-ttu-id="7ff16-163">Faux</span><span class="sxs-lookup"><span data-stu-id="7ff16-163">False</span></span>                                                       |
| <span data-ttu-id="7ff16-164">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7ff16-164">In Global Catalog</span></span>      | <span data-ttu-id="7ff16-165">Faux</span><span class="sxs-lookup"><span data-stu-id="7ff16-165">False</span></span>                                                       |
| <span data-ttu-id="7ff16-166">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7ff16-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="7ff16-167">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7ff16-167">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="7ff16-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7ff16-168">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="7ff16-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7ff16-169">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="7ff16-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7ff16-170">Search-Flags</span></span>           | <span data-ttu-id="7ff16-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7ff16-171">0x00000000</span></span>                                                  |
| <span data-ttu-id="7ff16-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7ff16-172">System-Flags</span></span>           | <span data-ttu-id="7ff16-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7ff16-173">0x00000010</span></span>                                                  |
| <span data-ttu-id="7ff16-174">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7ff16-174">Classes used in</span></span>        | [<span data-ttu-id="7ff16-175">**NTDS-site-paramètres**</span><span class="sxs-lookup"><span data-stu-id="7ff16-175">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="adam"></a><span data-ttu-id="7ff16-176">ADAM</span><span class="sxs-lookup"><span data-stu-id="7ff16-176">ADAM</span></span>



| <span data-ttu-id="7ff16-177">Entrée</span><span class="sxs-lookup"><span data-stu-id="7ff16-177">Entry</span></span> | <span data-ttu-id="7ff16-178">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ff16-178">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="7ff16-179">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7ff16-179">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7ff16-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7ff16-180">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7ff16-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="7ff16-181">System-Only</span></span>            | <span data-ttu-id="7ff16-182">Faux</span><span class="sxs-lookup"><span data-stu-id="7ff16-182">False</span></span>                                                       |
| <span data-ttu-id="7ff16-183">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7ff16-183">Is-Single-Valued</span></span>       | <span data-ttu-id="7ff16-184">Vrai</span><span class="sxs-lookup"><span data-stu-id="7ff16-184">True</span></span>                                                        |
| <span data-ttu-id="7ff16-185">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7ff16-185">Is Indexed</span></span>             | <span data-ttu-id="7ff16-186">Faux</span><span class="sxs-lookup"><span data-stu-id="7ff16-186">False</span></span>                                                       |
| <span data-ttu-id="7ff16-187">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7ff16-187">In Global Catalog</span></span>      | <span data-ttu-id="7ff16-188">Faux</span><span class="sxs-lookup"><span data-stu-id="7ff16-188">False</span></span>                                                       |
| <span data-ttu-id="7ff16-189">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7ff16-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="7ff16-190">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7ff16-190">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="7ff16-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7ff16-191">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="7ff16-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7ff16-192">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="7ff16-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7ff16-193">Search-Flags</span></span>           | <span data-ttu-id="7ff16-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7ff16-194">0x00000000</span></span>                                                  |
| <span data-ttu-id="7ff16-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7ff16-195">System-Flags</span></span>           | <span data-ttu-id="7ff16-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7ff16-196">0x00000010</span></span>                                                  |
| <span data-ttu-id="7ff16-197">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7ff16-197">Classes used in</span></span>        | [<span data-ttu-id="7ff16-198">**NTDS-site-paramètres**</span><span class="sxs-lookup"><span data-stu-id="7ff16-198">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7ff16-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7ff16-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7ff16-200">Entrée</span><span class="sxs-lookup"><span data-stu-id="7ff16-200">Entry</span></span> | <span data-ttu-id="7ff16-201">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ff16-201">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="7ff16-202">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7ff16-202">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7ff16-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7ff16-203">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7ff16-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="7ff16-204">System-Only</span></span>            | <span data-ttu-id="7ff16-205">Faux</span><span class="sxs-lookup"><span data-stu-id="7ff16-205">False</span></span>                                                       |
| <span data-ttu-id="7ff16-206">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7ff16-206">Is-Single-Valued</span></span>       | <span data-ttu-id="7ff16-207">Vrai</span><span class="sxs-lookup"><span data-stu-id="7ff16-207">True</span></span>                                                        |
| <span data-ttu-id="7ff16-208">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7ff16-208">Is Indexed</span></span>             | <span data-ttu-id="7ff16-209">Faux</span><span class="sxs-lookup"><span data-stu-id="7ff16-209">False</span></span>                                                       |
| <span data-ttu-id="7ff16-210">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7ff16-210">In Global Catalog</span></span>      | <span data-ttu-id="7ff16-211">Faux</span><span class="sxs-lookup"><span data-stu-id="7ff16-211">False</span></span>                                                       |
| <span data-ttu-id="7ff16-212">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7ff16-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="7ff16-213">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7ff16-213">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="7ff16-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7ff16-214">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="7ff16-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7ff16-215">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="7ff16-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7ff16-216">Search-Flags</span></span>           | <span data-ttu-id="7ff16-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7ff16-217">0x00000000</span></span>                                                  |
| <span data-ttu-id="7ff16-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7ff16-218">System-Flags</span></span>           | <span data-ttu-id="7ff16-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7ff16-219">0x00000010</span></span>                                                  |
| <span data-ttu-id="7ff16-220">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7ff16-220">Classes used in</span></span>        | [<span data-ttu-id="7ff16-221">**NTDS-site-paramètres**</span><span class="sxs-lookup"><span data-stu-id="7ff16-221">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7ff16-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7ff16-222">Windows Server 2008</span></span>



| <span data-ttu-id="7ff16-223">Entrée</span><span class="sxs-lookup"><span data-stu-id="7ff16-223">Entry</span></span> | <span data-ttu-id="7ff16-224">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ff16-224">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="7ff16-225">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7ff16-225">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7ff16-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7ff16-226">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7ff16-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="7ff16-227">System-Only</span></span>            | <span data-ttu-id="7ff16-228">Faux</span><span class="sxs-lookup"><span data-stu-id="7ff16-228">False</span></span>                                                       |
| <span data-ttu-id="7ff16-229">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7ff16-229">Is-Single-Valued</span></span>       | <span data-ttu-id="7ff16-230">Vrai</span><span class="sxs-lookup"><span data-stu-id="7ff16-230">True</span></span>                                                        |
| <span data-ttu-id="7ff16-231">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7ff16-231">Is Indexed</span></span>             | <span data-ttu-id="7ff16-232">Faux</span><span class="sxs-lookup"><span data-stu-id="7ff16-232">False</span></span>                                                       |
| <span data-ttu-id="7ff16-233">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7ff16-233">In Global Catalog</span></span>      | <span data-ttu-id="7ff16-234">Faux</span><span class="sxs-lookup"><span data-stu-id="7ff16-234">False</span></span>                                                       |
| <span data-ttu-id="7ff16-235">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7ff16-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="7ff16-236">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7ff16-236">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="7ff16-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7ff16-237">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="7ff16-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7ff16-238">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="7ff16-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7ff16-239">Search-Flags</span></span>           | <span data-ttu-id="7ff16-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7ff16-240">0x00000000</span></span>                                                  |
| <span data-ttu-id="7ff16-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7ff16-241">System-Flags</span></span>           | <span data-ttu-id="7ff16-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7ff16-242">0x00000010</span></span>                                                  |
| <span data-ttu-id="7ff16-243">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7ff16-243">Classes used in</span></span>        | [<span data-ttu-id="7ff16-244">**NTDS-site-paramètres**</span><span class="sxs-lookup"><span data-stu-id="7ff16-244">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7ff16-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7ff16-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7ff16-246">Entrée</span><span class="sxs-lookup"><span data-stu-id="7ff16-246">Entry</span></span> | <span data-ttu-id="7ff16-247">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ff16-247">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="7ff16-248">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7ff16-248">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7ff16-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7ff16-249">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7ff16-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="7ff16-250">System-Only</span></span>            | <span data-ttu-id="7ff16-251">Faux</span><span class="sxs-lookup"><span data-stu-id="7ff16-251">False</span></span>                                                       |
| <span data-ttu-id="7ff16-252">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7ff16-252">Is-Single-Valued</span></span>       | <span data-ttu-id="7ff16-253">Vrai</span><span class="sxs-lookup"><span data-stu-id="7ff16-253">True</span></span>                                                        |
| <span data-ttu-id="7ff16-254">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7ff16-254">Is Indexed</span></span>             | <span data-ttu-id="7ff16-255">Faux</span><span class="sxs-lookup"><span data-stu-id="7ff16-255">False</span></span>                                                       |
| <span data-ttu-id="7ff16-256">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7ff16-256">In Global Catalog</span></span>      | <span data-ttu-id="7ff16-257">Faux</span><span class="sxs-lookup"><span data-stu-id="7ff16-257">False</span></span>                                                       |
| <span data-ttu-id="7ff16-258">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7ff16-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="7ff16-259">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7ff16-259">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="7ff16-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7ff16-260">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="7ff16-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7ff16-261">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="7ff16-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7ff16-262">Search-Flags</span></span>           | <span data-ttu-id="7ff16-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7ff16-263">0x00000000</span></span>                                                  |
| <span data-ttu-id="7ff16-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7ff16-264">System-Flags</span></span>           | <span data-ttu-id="7ff16-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7ff16-265">0x00000010</span></span>                                                  |
| <span data-ttu-id="7ff16-266">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7ff16-266">Classes used in</span></span>        | [<span data-ttu-id="7ff16-267">**NTDS-site-paramètres**</span><span class="sxs-lookup"><span data-stu-id="7ff16-267">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7ff16-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7ff16-268">Windows Server 2012</span></span>



| <span data-ttu-id="7ff16-269">Entrée</span><span class="sxs-lookup"><span data-stu-id="7ff16-269">Entry</span></span> | <span data-ttu-id="7ff16-270">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ff16-270">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="7ff16-271">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7ff16-271">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7ff16-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7ff16-272">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7ff16-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="7ff16-273">System-Only</span></span>            | <span data-ttu-id="7ff16-274">Faux</span><span class="sxs-lookup"><span data-stu-id="7ff16-274">False</span></span>                                                       |
| <span data-ttu-id="7ff16-275">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7ff16-275">Is-Single-Valued</span></span>       | <span data-ttu-id="7ff16-276">Vrai</span><span class="sxs-lookup"><span data-stu-id="7ff16-276">True</span></span>                                                        |
| <span data-ttu-id="7ff16-277">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7ff16-277">Is Indexed</span></span>             | <span data-ttu-id="7ff16-278">Faux</span><span class="sxs-lookup"><span data-stu-id="7ff16-278">False</span></span>                                                       |
| <span data-ttu-id="7ff16-279">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7ff16-279">In Global Catalog</span></span>      | <span data-ttu-id="7ff16-280">Faux</span><span class="sxs-lookup"><span data-stu-id="7ff16-280">False</span></span>                                                       |
| <span data-ttu-id="7ff16-281">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7ff16-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="7ff16-282">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7ff16-282">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="7ff16-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7ff16-283">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="7ff16-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7ff16-284">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="7ff16-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7ff16-285">Search-Flags</span></span>           | <span data-ttu-id="7ff16-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7ff16-286">0x00000000</span></span>                                                  |
| <span data-ttu-id="7ff16-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7ff16-287">System-Flags</span></span>           | <span data-ttu-id="7ff16-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7ff16-288">0x00000010</span></span>                                                  |
| <span data-ttu-id="7ff16-289">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7ff16-289">Classes used in</span></span>        | [<span data-ttu-id="7ff16-290">**NTDS-site-paramètres**</span><span class="sxs-lookup"><span data-stu-id="7ff16-290">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



 

 





