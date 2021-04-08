---
title: ACS-DSBM-Refresh (attribut)
description: Cet attribut contient la valeur du minuteur de l’intervalle qui détermine le moment où le gestionnaire de bande passante de sous-réseau (DSBM) désigné envoie un message d’actualisation (« \_ \_ DSBM ») à tous les gestionnaires de bande passante du sous-réseau dans un domaine.
ms.assetid: 018fd748-ca2e-41e1-a920-224a32e13e21
ms.tgt_platform: multiple
keywords:
- Schéma AD ACS-DSBM-Refresh Attribute
- Schéma AD de l’attribut aCSDSBMRefresh
topic_type:
- apiref
api_name:
- ACS-DSBM-Refresh
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d662b886a8c97f3d155d3c1b40efcef67f7f1f0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103943056"
---
# <a name="acs-dsbm-refresh-attribute"></a><span data-ttu-id="52100-105">ACS-DSBM-Refresh (attribut)</span><span class="sxs-lookup"><span data-stu-id="52100-105">ACS-DSBM-Refresh attribute</span></span>

<span data-ttu-id="52100-106">Cet attribut contient la valeur du minuteur de l’intervalle qui détermine le moment où le gestionnaire de bande passante de sous-réseau (DSBM) désigné envoie un message d’actualisation (« \_ \_ DSBM ») à tous les gestionnaires de bande passante du sous-réseau dans un domaine.</span><span class="sxs-lookup"><span data-stu-id="52100-106">This attribute contains the interval timer value that determines when the Designated Subnet Bandwidth Manager (DSBM) sends out a refresh message (I\_AM\_DSBM) to all of the Subnet Bandwidth Managers in a domain.</span></span>



| <span data-ttu-id="52100-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="52100-107">Entry</span></span> | <span data-ttu-id="52100-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="52100-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="52100-109">CN</span><span class="sxs-lookup"><span data-stu-id="52100-109">CN</span></span>                | <span data-ttu-id="52100-110">ACS-DSBM-actualiser</span><span class="sxs-lookup"><span data-stu-id="52100-110">ACS-DSBM-Refresh</span></span>                     |
| <span data-ttu-id="52100-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="52100-111">Ldap-Display-Name</span></span> | <span data-ttu-id="52100-112">aCSDSBMRefresh</span><span class="sxs-lookup"><span data-stu-id="52100-112">aCSDSBMRefresh</span></span>                       |
| <span data-ttu-id="52100-113">Taille</span><span class="sxs-lookup"><span data-stu-id="52100-113">Size</span></span>              | <span data-ttu-id="52100-114">4 octets</span><span class="sxs-lookup"><span data-stu-id="52100-114">4 bytes</span></span>                              |
| <span data-ttu-id="52100-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="52100-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="52100-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="52100-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="52100-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="52100-117">Attribute-Id</span></span>      | <span data-ttu-id="52100-118">1.2.840.113556.1.4.777</span><span class="sxs-lookup"><span data-stu-id="52100-118">1.2.840.113556.1.4.777</span></span>               |
| <span data-ttu-id="52100-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="52100-119">System-Id-Guid</span></span>    | <span data-ttu-id="52100-120">1cb3559f-56d0-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="52100-120">1cb3559f-56d0-11d1-a9c6-0000f80367c1</span></span> |
| <span data-ttu-id="52100-121">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="52100-121">Syntax</span></span>            | [<span data-ttu-id="52100-122">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="52100-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="52100-123">Implémentations</span><span class="sxs-lookup"><span data-stu-id="52100-123">Implementations</span></span>

-   [<span data-ttu-id="52100-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="52100-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="52100-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="52100-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="52100-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="52100-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="52100-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="52100-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="52100-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="52100-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="52100-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="52100-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="52100-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="52100-130">Windows 2000 Server</span></span>



| <span data-ttu-id="52100-131">Entrée</span><span class="sxs-lookup"><span data-stu-id="52100-131">Entry</span></span> | <span data-ttu-id="52100-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="52100-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="52100-133">ID de lien</span><span class="sxs-lookup"><span data-stu-id="52100-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="52100-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="52100-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="52100-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="52100-135">System-Only</span></span>            | <span data-ttu-id="52100-136">Faux</span><span class="sxs-lookup"><span data-stu-id="52100-136">False</span></span>                                        |
| <span data-ttu-id="52100-137">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="52100-137">Is-Single-Valued</span></span>       | <span data-ttu-id="52100-138">Vrai</span><span class="sxs-lookup"><span data-stu-id="52100-138">True</span></span>                                         |
| <span data-ttu-id="52100-139">Est indexé</span><span class="sxs-lookup"><span data-stu-id="52100-139">Is Indexed</span></span>             | <span data-ttu-id="52100-140">Faux</span><span class="sxs-lookup"><span data-stu-id="52100-140">False</span></span>                                        |
| <span data-ttu-id="52100-141">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="52100-141">In Global Catalog</span></span>      | <span data-ttu-id="52100-142">Faux</span><span class="sxs-lookup"><span data-stu-id="52100-142">False</span></span>                                        |
| <span data-ttu-id="52100-143">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="52100-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="52100-144">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="52100-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="52100-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="52100-145">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="52100-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="52100-146">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="52100-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="52100-147">Search-Flags</span></span>           | <span data-ttu-id="52100-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="52100-148">0x00000000</span></span>                                   |
| <span data-ttu-id="52100-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="52100-149">System-Flags</span></span>           | <span data-ttu-id="52100-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="52100-150">0x00000010</span></span>                                   |
| <span data-ttu-id="52100-151">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="52100-151">Classes used in</span></span>        | [<span data-ttu-id="52100-152">**ACS-sous-réseau**</span><span class="sxs-lookup"><span data-stu-id="52100-152">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="52100-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="52100-153">Windows Server 2003</span></span>



| <span data-ttu-id="52100-154">Entrée</span><span class="sxs-lookup"><span data-stu-id="52100-154">Entry</span></span> | <span data-ttu-id="52100-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="52100-155">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="52100-156">ID de lien</span><span class="sxs-lookup"><span data-stu-id="52100-156">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="52100-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="52100-157">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="52100-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="52100-158">System-Only</span></span>            | <span data-ttu-id="52100-159">Faux</span><span class="sxs-lookup"><span data-stu-id="52100-159">False</span></span>                                        |
| <span data-ttu-id="52100-160">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="52100-160">Is-Single-Valued</span></span>       | <span data-ttu-id="52100-161">Vrai</span><span class="sxs-lookup"><span data-stu-id="52100-161">True</span></span>                                         |
| <span data-ttu-id="52100-162">Est indexé</span><span class="sxs-lookup"><span data-stu-id="52100-162">Is Indexed</span></span>             | <span data-ttu-id="52100-163">Faux</span><span class="sxs-lookup"><span data-stu-id="52100-163">False</span></span>                                        |
| <span data-ttu-id="52100-164">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="52100-164">In Global Catalog</span></span>      | <span data-ttu-id="52100-165">Faux</span><span class="sxs-lookup"><span data-stu-id="52100-165">False</span></span>                                        |
| <span data-ttu-id="52100-166">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="52100-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="52100-167">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="52100-167">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="52100-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="52100-168">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="52100-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="52100-169">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="52100-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="52100-170">Search-Flags</span></span>           | <span data-ttu-id="52100-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="52100-171">0x00000000</span></span>                                   |
| <span data-ttu-id="52100-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="52100-172">System-Flags</span></span>           | <span data-ttu-id="52100-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="52100-173">0x00000010</span></span>                                   |
| <span data-ttu-id="52100-174">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="52100-174">Classes used in</span></span>        | [<span data-ttu-id="52100-175">**ACS-sous-réseau**</span><span class="sxs-lookup"><span data-stu-id="52100-175">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="52100-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="52100-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="52100-177">Entrée</span><span class="sxs-lookup"><span data-stu-id="52100-177">Entry</span></span> | <span data-ttu-id="52100-178">Valeur</span><span class="sxs-lookup"><span data-stu-id="52100-178">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="52100-179">ID de lien</span><span class="sxs-lookup"><span data-stu-id="52100-179">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="52100-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="52100-180">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="52100-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="52100-181">System-Only</span></span>            | <span data-ttu-id="52100-182">Faux</span><span class="sxs-lookup"><span data-stu-id="52100-182">False</span></span>                                        |
| <span data-ttu-id="52100-183">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="52100-183">Is-Single-Valued</span></span>       | <span data-ttu-id="52100-184">Vrai</span><span class="sxs-lookup"><span data-stu-id="52100-184">True</span></span>                                         |
| <span data-ttu-id="52100-185">Est indexé</span><span class="sxs-lookup"><span data-stu-id="52100-185">Is Indexed</span></span>             | <span data-ttu-id="52100-186">Faux</span><span class="sxs-lookup"><span data-stu-id="52100-186">False</span></span>                                        |
| <span data-ttu-id="52100-187">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="52100-187">In Global Catalog</span></span>      | <span data-ttu-id="52100-188">Faux</span><span class="sxs-lookup"><span data-stu-id="52100-188">False</span></span>                                        |
| <span data-ttu-id="52100-189">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="52100-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="52100-190">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="52100-190">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="52100-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="52100-191">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="52100-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="52100-192">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="52100-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="52100-193">Search-Flags</span></span>           | <span data-ttu-id="52100-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="52100-194">0x00000000</span></span>                                   |
| <span data-ttu-id="52100-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="52100-195">System-Flags</span></span>           | <span data-ttu-id="52100-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="52100-196">0x00000010</span></span>                                   |
| <span data-ttu-id="52100-197">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="52100-197">Classes used in</span></span>        | [<span data-ttu-id="52100-198">**ACS-sous-réseau**</span><span class="sxs-lookup"><span data-stu-id="52100-198">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="52100-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="52100-199">Windows Server 2008</span></span>



| <span data-ttu-id="52100-200">Entrée</span><span class="sxs-lookup"><span data-stu-id="52100-200">Entry</span></span> | <span data-ttu-id="52100-201">Valeur</span><span class="sxs-lookup"><span data-stu-id="52100-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="52100-202">ID de lien</span><span class="sxs-lookup"><span data-stu-id="52100-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="52100-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="52100-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="52100-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="52100-204">System-Only</span></span>            | <span data-ttu-id="52100-205">Faux</span><span class="sxs-lookup"><span data-stu-id="52100-205">False</span></span>                                        |
| <span data-ttu-id="52100-206">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="52100-206">Is-Single-Valued</span></span>       | <span data-ttu-id="52100-207">Vrai</span><span class="sxs-lookup"><span data-stu-id="52100-207">True</span></span>                                         |
| <span data-ttu-id="52100-208">Est indexé</span><span class="sxs-lookup"><span data-stu-id="52100-208">Is Indexed</span></span>             | <span data-ttu-id="52100-209">Faux</span><span class="sxs-lookup"><span data-stu-id="52100-209">False</span></span>                                        |
| <span data-ttu-id="52100-210">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="52100-210">In Global Catalog</span></span>      | <span data-ttu-id="52100-211">Faux</span><span class="sxs-lookup"><span data-stu-id="52100-211">False</span></span>                                        |
| <span data-ttu-id="52100-212">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="52100-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="52100-213">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="52100-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="52100-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="52100-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="52100-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="52100-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="52100-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="52100-216">Search-Flags</span></span>           | <span data-ttu-id="52100-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="52100-217">0x00000000</span></span>                                   |
| <span data-ttu-id="52100-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="52100-218">System-Flags</span></span>           | <span data-ttu-id="52100-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="52100-219">0x00000010</span></span>                                   |
| <span data-ttu-id="52100-220">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="52100-220">Classes used in</span></span>        | [<span data-ttu-id="52100-221">**ACS-sous-réseau**</span><span class="sxs-lookup"><span data-stu-id="52100-221">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="52100-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="52100-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="52100-223">Entrée</span><span class="sxs-lookup"><span data-stu-id="52100-223">Entry</span></span> | <span data-ttu-id="52100-224">Valeur</span><span class="sxs-lookup"><span data-stu-id="52100-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="52100-225">ID de lien</span><span class="sxs-lookup"><span data-stu-id="52100-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="52100-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="52100-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="52100-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="52100-227">System-Only</span></span>            | <span data-ttu-id="52100-228">Faux</span><span class="sxs-lookup"><span data-stu-id="52100-228">False</span></span>                                        |
| <span data-ttu-id="52100-229">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="52100-229">Is-Single-Valued</span></span>       | <span data-ttu-id="52100-230">Vrai</span><span class="sxs-lookup"><span data-stu-id="52100-230">True</span></span>                                         |
| <span data-ttu-id="52100-231">Est indexé</span><span class="sxs-lookup"><span data-stu-id="52100-231">Is Indexed</span></span>             | <span data-ttu-id="52100-232">Faux</span><span class="sxs-lookup"><span data-stu-id="52100-232">False</span></span>                                        |
| <span data-ttu-id="52100-233">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="52100-233">In Global Catalog</span></span>      | <span data-ttu-id="52100-234">Faux</span><span class="sxs-lookup"><span data-stu-id="52100-234">False</span></span>                                        |
| <span data-ttu-id="52100-235">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="52100-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="52100-236">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="52100-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="52100-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="52100-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="52100-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="52100-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="52100-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="52100-239">Search-Flags</span></span>           | <span data-ttu-id="52100-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="52100-240">0x00000000</span></span>                                   |
| <span data-ttu-id="52100-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="52100-241">System-Flags</span></span>           | <span data-ttu-id="52100-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="52100-242">0x00000010</span></span>                                   |
| <span data-ttu-id="52100-243">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="52100-243">Classes used in</span></span>        | [<span data-ttu-id="52100-244">**ACS-sous-réseau**</span><span class="sxs-lookup"><span data-stu-id="52100-244">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="52100-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="52100-245">Windows Server 2012</span></span>



| <span data-ttu-id="52100-246">Entrée</span><span class="sxs-lookup"><span data-stu-id="52100-246">Entry</span></span> | <span data-ttu-id="52100-247">Valeur</span><span class="sxs-lookup"><span data-stu-id="52100-247">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="52100-248">ID de lien</span><span class="sxs-lookup"><span data-stu-id="52100-248">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="52100-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="52100-249">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="52100-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="52100-250">System-Only</span></span>            | <span data-ttu-id="52100-251">Faux</span><span class="sxs-lookup"><span data-stu-id="52100-251">False</span></span>                                        |
| <span data-ttu-id="52100-252">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="52100-252">Is-Single-Valued</span></span>       | <span data-ttu-id="52100-253">Vrai</span><span class="sxs-lookup"><span data-stu-id="52100-253">True</span></span>                                         |
| <span data-ttu-id="52100-254">Est indexé</span><span class="sxs-lookup"><span data-stu-id="52100-254">Is Indexed</span></span>             | <span data-ttu-id="52100-255">Faux</span><span class="sxs-lookup"><span data-stu-id="52100-255">False</span></span>                                        |
| <span data-ttu-id="52100-256">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="52100-256">In Global Catalog</span></span>      | <span data-ttu-id="52100-257">Faux</span><span class="sxs-lookup"><span data-stu-id="52100-257">False</span></span>                                        |
| <span data-ttu-id="52100-258">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="52100-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="52100-259">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="52100-259">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="52100-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="52100-260">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="52100-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="52100-261">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="52100-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="52100-262">Search-Flags</span></span>           | <span data-ttu-id="52100-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="52100-263">0x00000000</span></span>                                   |
| <span data-ttu-id="52100-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="52100-264">System-Flags</span></span>           | <span data-ttu-id="52100-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="52100-265">0x00000010</span></span>                                   |
| <span data-ttu-id="52100-266">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="52100-266">Classes used in</span></span>        | [<span data-ttu-id="52100-267">**ACS-sous-réseau**</span><span class="sxs-lookup"><span data-stu-id="52100-267">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 





