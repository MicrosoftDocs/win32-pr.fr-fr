---
title: Inter-site-Topology-attribut Renew
description: Cette classe indique la fréquence à laquelle le générateur de topologie intersite met à jour le message KeepAlive qui est envoyé aux contrôleurs de domaine contenus dans le même site.
ms.assetid: 523d8161-0678-482f-8d66-55a112995fe5
ms.tgt_platform: multiple
keywords:
- Inter-site-topologie-renouveler l’attribut schéma AD
- Schéma AD de l’attribut interSiteTopologyRenew
topic_type:
- apiref
api_name:
- Inter-Site-Topology-Renew
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 821bd294f777fd29738ff102955cd170a42205e2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106516130"
---
# <a name="inter-site-topology-renew-attribute"></a><span data-ttu-id="d80b4-105">Inter-site-Topology-attribut Renew</span><span class="sxs-lookup"><span data-stu-id="d80b4-105">Inter-Site-Topology-Renew attribute</span></span>

<span data-ttu-id="d80b4-106">Cette classe indique la fréquence à laquelle le générateur de topologie intersite met à jour le message KeepAlive qui est envoyé aux contrôleurs de domaine contenus dans le même site.</span><span class="sxs-lookup"><span data-stu-id="d80b4-106">This class indicates how often the intersite topology generator updates the keep-alive message that is sent to domain controllers contained in the same site.</span></span>



| <span data-ttu-id="d80b4-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="d80b4-107">Entry</span></span> | <span data-ttu-id="d80b4-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="d80b4-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="d80b4-109">CN</span><span class="sxs-lookup"><span data-stu-id="d80b4-109">CN</span></span>                | <span data-ttu-id="d80b4-110">Inter-site-topologie-renouveler</span><span class="sxs-lookup"><span data-stu-id="d80b4-110">Inter-Site-Topology-Renew</span></span>            |
| <span data-ttu-id="d80b4-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="d80b4-111">Ldap-Display-Name</span></span> | <span data-ttu-id="d80b4-112">interSiteTopologyRenew</span><span class="sxs-lookup"><span data-stu-id="d80b4-112">interSiteTopologyRenew</span></span>               |
| <span data-ttu-id="d80b4-113">Taille</span><span class="sxs-lookup"><span data-stu-id="d80b4-113">Size</span></span>              | <span data-ttu-id="d80b4-114">4 octets</span><span class="sxs-lookup"><span data-stu-id="d80b4-114">4 bytes</span></span>                              |
| <span data-ttu-id="d80b4-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="d80b4-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="d80b4-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="d80b4-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="d80b4-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d80b4-117">Attribute-Id</span></span>      | <span data-ttu-id="d80b4-118">1.2.840.113556.1.4.1247</span><span class="sxs-lookup"><span data-stu-id="d80b4-118">1.2.840.113556.1.4.1247</span></span>              |
| <span data-ttu-id="d80b4-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="d80b4-119">System-Id-Guid</span></span>    | <span data-ttu-id="d80b4-120">b7c69e5f-2cc7-11d2-854e-00a0c983f608</span><span class="sxs-lookup"><span data-stu-id="d80b4-120">b7c69e5f-2cc7-11d2-854e-00a0c983f608</span></span> |
| <span data-ttu-id="d80b4-121">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d80b4-121">Syntax</span></span>            | [<span data-ttu-id="d80b4-122">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="d80b4-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="d80b4-123">Implémentations</span><span class="sxs-lookup"><span data-stu-id="d80b4-123">Implementations</span></span>

-   [<span data-ttu-id="d80b4-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d80b4-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d80b4-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d80b4-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d80b4-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="d80b4-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="d80b4-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d80b4-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d80b4-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d80b4-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d80b4-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d80b4-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d80b4-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d80b4-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d80b4-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d80b4-131">Windows 2000 Server</span></span>



| <span data-ttu-id="d80b4-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="d80b4-132">Entry</span></span> | <span data-ttu-id="d80b4-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="d80b4-133">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="d80b4-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d80b4-134">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d80b4-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d80b4-135">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d80b4-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="d80b4-136">System-Only</span></span>            | <span data-ttu-id="d80b4-137">Faux</span><span class="sxs-lookup"><span data-stu-id="d80b4-137">False</span></span>                                                       |
| <span data-ttu-id="d80b4-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d80b4-138">Is-Single-Valued</span></span>       | <span data-ttu-id="d80b4-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="d80b4-139">True</span></span>                                                        |
| <span data-ttu-id="d80b4-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d80b4-140">Is Indexed</span></span>             | <span data-ttu-id="d80b4-141">Faux</span><span class="sxs-lookup"><span data-stu-id="d80b4-141">False</span></span>                                                       |
| <span data-ttu-id="d80b4-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d80b4-142">In Global Catalog</span></span>      | <span data-ttu-id="d80b4-143">Faux</span><span class="sxs-lookup"><span data-stu-id="d80b4-143">False</span></span>                                                       |
| <span data-ttu-id="d80b4-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d80b4-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="d80b4-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d80b4-145">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="d80b4-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d80b4-146">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="d80b4-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d80b4-147">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="d80b4-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d80b4-148">Search-Flags</span></span>           | <span data-ttu-id="d80b4-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d80b4-149">0x00000000</span></span>                                                  |
| <span data-ttu-id="d80b4-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d80b4-150">System-Flags</span></span>           | <span data-ttu-id="d80b4-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d80b4-151">0x00000010</span></span>                                                  |
| <span data-ttu-id="d80b4-152">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d80b4-152">Classes used in</span></span>        | [<span data-ttu-id="d80b4-153">**NTDS-site-paramètres**</span><span class="sxs-lookup"><span data-stu-id="d80b4-153">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d80b4-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d80b4-154">Windows Server 2003</span></span>



| <span data-ttu-id="d80b4-155">Entrée</span><span class="sxs-lookup"><span data-stu-id="d80b4-155">Entry</span></span> | <span data-ttu-id="d80b4-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="d80b4-156">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="d80b4-157">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d80b4-157">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d80b4-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d80b4-158">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d80b4-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="d80b4-159">System-Only</span></span>            | <span data-ttu-id="d80b4-160">Faux</span><span class="sxs-lookup"><span data-stu-id="d80b4-160">False</span></span>                                                       |
| <span data-ttu-id="d80b4-161">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d80b4-161">Is-Single-Valued</span></span>       | <span data-ttu-id="d80b4-162">Vrai</span><span class="sxs-lookup"><span data-stu-id="d80b4-162">True</span></span>                                                        |
| <span data-ttu-id="d80b4-163">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d80b4-163">Is Indexed</span></span>             | <span data-ttu-id="d80b4-164">Faux</span><span class="sxs-lookup"><span data-stu-id="d80b4-164">False</span></span>                                                       |
| <span data-ttu-id="d80b4-165">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d80b4-165">In Global Catalog</span></span>      | <span data-ttu-id="d80b4-166">Faux</span><span class="sxs-lookup"><span data-stu-id="d80b4-166">False</span></span>                                                       |
| <span data-ttu-id="d80b4-167">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d80b4-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="d80b4-168">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d80b4-168">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="d80b4-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d80b4-169">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="d80b4-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d80b4-170">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="d80b4-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d80b4-171">Search-Flags</span></span>           | <span data-ttu-id="d80b4-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d80b4-172">0x00000000</span></span>                                                  |
| <span data-ttu-id="d80b4-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d80b4-173">System-Flags</span></span>           | <span data-ttu-id="d80b4-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d80b4-174">0x00000010</span></span>                                                  |
| <span data-ttu-id="d80b4-175">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d80b4-175">Classes used in</span></span>        | [<span data-ttu-id="d80b4-176">**NTDS-site-paramètres**</span><span class="sxs-lookup"><span data-stu-id="d80b4-176">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="adam"></a><span data-ttu-id="d80b4-177">ADAM</span><span class="sxs-lookup"><span data-stu-id="d80b4-177">ADAM</span></span>



| <span data-ttu-id="d80b4-178">Entrée</span><span class="sxs-lookup"><span data-stu-id="d80b4-178">Entry</span></span> | <span data-ttu-id="d80b4-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="d80b4-179">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="d80b4-180">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d80b4-180">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d80b4-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d80b4-181">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d80b4-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="d80b4-182">System-Only</span></span>            | <span data-ttu-id="d80b4-183">Faux</span><span class="sxs-lookup"><span data-stu-id="d80b4-183">False</span></span>                                                       |
| <span data-ttu-id="d80b4-184">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d80b4-184">Is-Single-Valued</span></span>       | <span data-ttu-id="d80b4-185">Vrai</span><span class="sxs-lookup"><span data-stu-id="d80b4-185">True</span></span>                                                        |
| <span data-ttu-id="d80b4-186">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d80b4-186">Is Indexed</span></span>             | <span data-ttu-id="d80b4-187">Faux</span><span class="sxs-lookup"><span data-stu-id="d80b4-187">False</span></span>                                                       |
| <span data-ttu-id="d80b4-188">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d80b4-188">In Global Catalog</span></span>      | <span data-ttu-id="d80b4-189">Faux</span><span class="sxs-lookup"><span data-stu-id="d80b4-189">False</span></span>                                                       |
| <span data-ttu-id="d80b4-190">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d80b4-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="d80b4-191">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d80b4-191">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="d80b4-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d80b4-192">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="d80b4-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d80b4-193">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="d80b4-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d80b4-194">Search-Flags</span></span>           | <span data-ttu-id="d80b4-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d80b4-195">0x00000000</span></span>                                                  |
| <span data-ttu-id="d80b4-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d80b4-196">System-Flags</span></span>           | <span data-ttu-id="d80b4-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d80b4-197">0x00000010</span></span>                                                  |
| <span data-ttu-id="d80b4-198">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d80b4-198">Classes used in</span></span>        | [<span data-ttu-id="d80b4-199">**NTDS-site-paramètres**</span><span class="sxs-lookup"><span data-stu-id="d80b4-199">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d80b4-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d80b4-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d80b4-201">Entrée</span><span class="sxs-lookup"><span data-stu-id="d80b4-201">Entry</span></span> | <span data-ttu-id="d80b4-202">Valeur</span><span class="sxs-lookup"><span data-stu-id="d80b4-202">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="d80b4-203">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d80b4-203">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d80b4-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d80b4-204">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d80b4-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="d80b4-205">System-Only</span></span>            | <span data-ttu-id="d80b4-206">Faux</span><span class="sxs-lookup"><span data-stu-id="d80b4-206">False</span></span>                                                       |
| <span data-ttu-id="d80b4-207">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d80b4-207">Is-Single-Valued</span></span>       | <span data-ttu-id="d80b4-208">Vrai</span><span class="sxs-lookup"><span data-stu-id="d80b4-208">True</span></span>                                                        |
| <span data-ttu-id="d80b4-209">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d80b4-209">Is Indexed</span></span>             | <span data-ttu-id="d80b4-210">Faux</span><span class="sxs-lookup"><span data-stu-id="d80b4-210">False</span></span>                                                       |
| <span data-ttu-id="d80b4-211">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d80b4-211">In Global Catalog</span></span>      | <span data-ttu-id="d80b4-212">Faux</span><span class="sxs-lookup"><span data-stu-id="d80b4-212">False</span></span>                                                       |
| <span data-ttu-id="d80b4-213">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d80b4-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="d80b4-214">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d80b4-214">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="d80b4-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d80b4-215">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="d80b4-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d80b4-216">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="d80b4-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d80b4-217">Search-Flags</span></span>           | <span data-ttu-id="d80b4-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d80b4-218">0x00000000</span></span>                                                  |
| <span data-ttu-id="d80b4-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d80b4-219">System-Flags</span></span>           | <span data-ttu-id="d80b4-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d80b4-220">0x00000010</span></span>                                                  |
| <span data-ttu-id="d80b4-221">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d80b4-221">Classes used in</span></span>        | [<span data-ttu-id="d80b4-222">**NTDS-site-paramètres**</span><span class="sxs-lookup"><span data-stu-id="d80b4-222">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d80b4-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d80b4-223">Windows Server 2008</span></span>



| <span data-ttu-id="d80b4-224">Entrée</span><span class="sxs-lookup"><span data-stu-id="d80b4-224">Entry</span></span> | <span data-ttu-id="d80b4-225">Valeur</span><span class="sxs-lookup"><span data-stu-id="d80b4-225">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="d80b4-226">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d80b4-226">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d80b4-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d80b4-227">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d80b4-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="d80b4-228">System-Only</span></span>            | <span data-ttu-id="d80b4-229">Faux</span><span class="sxs-lookup"><span data-stu-id="d80b4-229">False</span></span>                                                       |
| <span data-ttu-id="d80b4-230">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d80b4-230">Is-Single-Valued</span></span>       | <span data-ttu-id="d80b4-231">Vrai</span><span class="sxs-lookup"><span data-stu-id="d80b4-231">True</span></span>                                                        |
| <span data-ttu-id="d80b4-232">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d80b4-232">Is Indexed</span></span>             | <span data-ttu-id="d80b4-233">Faux</span><span class="sxs-lookup"><span data-stu-id="d80b4-233">False</span></span>                                                       |
| <span data-ttu-id="d80b4-234">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d80b4-234">In Global Catalog</span></span>      | <span data-ttu-id="d80b4-235">Faux</span><span class="sxs-lookup"><span data-stu-id="d80b4-235">False</span></span>                                                       |
| <span data-ttu-id="d80b4-236">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d80b4-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="d80b4-237">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d80b4-237">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="d80b4-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d80b4-238">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="d80b4-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d80b4-239">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="d80b4-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d80b4-240">Search-Flags</span></span>           | <span data-ttu-id="d80b4-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d80b4-241">0x00000000</span></span>                                                  |
| <span data-ttu-id="d80b4-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d80b4-242">System-Flags</span></span>           | <span data-ttu-id="d80b4-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d80b4-243">0x00000010</span></span>                                                  |
| <span data-ttu-id="d80b4-244">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d80b4-244">Classes used in</span></span>        | [<span data-ttu-id="d80b4-245">**NTDS-site-paramètres**</span><span class="sxs-lookup"><span data-stu-id="d80b4-245">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d80b4-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d80b4-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d80b4-247">Entrée</span><span class="sxs-lookup"><span data-stu-id="d80b4-247">Entry</span></span> | <span data-ttu-id="d80b4-248">Valeur</span><span class="sxs-lookup"><span data-stu-id="d80b4-248">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="d80b4-249">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d80b4-249">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d80b4-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d80b4-250">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d80b4-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="d80b4-251">System-Only</span></span>            | <span data-ttu-id="d80b4-252">Faux</span><span class="sxs-lookup"><span data-stu-id="d80b4-252">False</span></span>                                                       |
| <span data-ttu-id="d80b4-253">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d80b4-253">Is-Single-Valued</span></span>       | <span data-ttu-id="d80b4-254">Vrai</span><span class="sxs-lookup"><span data-stu-id="d80b4-254">True</span></span>                                                        |
| <span data-ttu-id="d80b4-255">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d80b4-255">Is Indexed</span></span>             | <span data-ttu-id="d80b4-256">Faux</span><span class="sxs-lookup"><span data-stu-id="d80b4-256">False</span></span>                                                       |
| <span data-ttu-id="d80b4-257">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d80b4-257">In Global Catalog</span></span>      | <span data-ttu-id="d80b4-258">Faux</span><span class="sxs-lookup"><span data-stu-id="d80b4-258">False</span></span>                                                       |
| <span data-ttu-id="d80b4-259">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d80b4-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="d80b4-260">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d80b4-260">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="d80b4-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d80b4-261">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="d80b4-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d80b4-262">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="d80b4-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d80b4-263">Search-Flags</span></span>           | <span data-ttu-id="d80b4-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d80b4-264">0x00000000</span></span>                                                  |
| <span data-ttu-id="d80b4-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d80b4-265">System-Flags</span></span>           | <span data-ttu-id="d80b4-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d80b4-266">0x00000010</span></span>                                                  |
| <span data-ttu-id="d80b4-267">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d80b4-267">Classes used in</span></span>        | [<span data-ttu-id="d80b4-268">**NTDS-site-paramètres**</span><span class="sxs-lookup"><span data-stu-id="d80b4-268">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d80b4-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d80b4-269">Windows Server 2012</span></span>



| <span data-ttu-id="d80b4-270">Entrée</span><span class="sxs-lookup"><span data-stu-id="d80b4-270">Entry</span></span> | <span data-ttu-id="d80b4-271">Valeur</span><span class="sxs-lookup"><span data-stu-id="d80b4-271">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="d80b4-272">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d80b4-272">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d80b4-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d80b4-273">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d80b4-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="d80b4-274">System-Only</span></span>            | <span data-ttu-id="d80b4-275">Faux</span><span class="sxs-lookup"><span data-stu-id="d80b4-275">False</span></span>                                                       |
| <span data-ttu-id="d80b4-276">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d80b4-276">Is-Single-Valued</span></span>       | <span data-ttu-id="d80b4-277">Vrai</span><span class="sxs-lookup"><span data-stu-id="d80b4-277">True</span></span>                                                        |
| <span data-ttu-id="d80b4-278">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d80b4-278">Is Indexed</span></span>             | <span data-ttu-id="d80b4-279">Faux</span><span class="sxs-lookup"><span data-stu-id="d80b4-279">False</span></span>                                                       |
| <span data-ttu-id="d80b4-280">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d80b4-280">In Global Catalog</span></span>      | <span data-ttu-id="d80b4-281">Faux</span><span class="sxs-lookup"><span data-stu-id="d80b4-281">False</span></span>                                                       |
| <span data-ttu-id="d80b4-282">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d80b4-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="d80b4-283">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d80b4-283">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="d80b4-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d80b4-284">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="d80b4-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d80b4-285">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="d80b4-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d80b4-286">Search-Flags</span></span>           | <span data-ttu-id="d80b4-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d80b4-287">0x00000000</span></span>                                                  |
| <span data-ttu-id="d80b4-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d80b4-288">System-Flags</span></span>           | <span data-ttu-id="d80b4-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d80b4-289">0x00000010</span></span>                                                  |
| <span data-ttu-id="d80b4-290">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d80b4-290">Classes used in</span></span>        | [<span data-ttu-id="d80b4-291">**NTDS-site-paramètres**</span><span class="sxs-lookup"><span data-stu-id="d80b4-291">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



 

 





