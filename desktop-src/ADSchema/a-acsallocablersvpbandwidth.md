---
title: ACS-Allocable-RSVP-attribut de bande passante
description: Bande passante maximale pouvant être réservée.
ms.assetid: 18d9a5c5-e44c-49e9-a8f0-9386a7b1ff97
ms.tgt_platform: multiple
keywords:
- Schéma AD ACS-Allocable-RSVP-Bandwidth Attribute
- Schéma AD de l’attribut aCSAllocableRSVPBandwidth
topic_type:
- apiref
api_name:
- ACS-Allocable-RSVP-Bandwidth
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c6bfe98d30fb8ef959f2e75d078b3a04b325b6a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845654"
---
# <a name="acs-allocable-rsvp-bandwidth-attribute"></a><span data-ttu-id="d4d1e-105">ACS-Allocable-RSVP-attribut de bande passante</span><span class="sxs-lookup"><span data-stu-id="d4d1e-105">ACS-Allocable-RSVP-Bandwidth attribute</span></span>

<span data-ttu-id="d4d1e-106">Bande passante maximale pouvant être réservée.</span><span class="sxs-lookup"><span data-stu-id="d4d1e-106">The maximum bandwidth that can be reserved.</span></span>



| <span data-ttu-id="d4d1e-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="d4d1e-107">Entry</span></span> | <span data-ttu-id="d4d1e-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4d1e-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="d4d1e-109">CN</span><span class="sxs-lookup"><span data-stu-id="d4d1e-109">CN</span></span>                | <span data-ttu-id="d4d1e-110">ACS-allouée-RSVP-bande passante</span><span class="sxs-lookup"><span data-stu-id="d4d1e-110">ACS-Allocable-RSVP-Bandwidth</span></span>         |
| <span data-ttu-id="d4d1e-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="d4d1e-111">Ldap-Display-Name</span></span> | <span data-ttu-id="d4d1e-112">aCSAllocableRSVPBandwidth</span><span class="sxs-lookup"><span data-stu-id="d4d1e-112">aCSAllocableRSVPBandwidth</span></span>            |
| <span data-ttu-id="d4d1e-113">Taille</span><span class="sxs-lookup"><span data-stu-id="d4d1e-113">Size</span></span>              | <span data-ttu-id="d4d1e-114">8 octets</span><span class="sxs-lookup"><span data-stu-id="d4d1e-114">8 bytes</span></span>                              |
| <span data-ttu-id="d4d1e-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="d4d1e-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="d4d1e-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="d4d1e-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="d4d1e-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d4d1e-117">Attribute-Id</span></span>      | <span data-ttu-id="d4d1e-118">1.2.840.113556.1.4.766</span><span class="sxs-lookup"><span data-stu-id="d4d1e-118">1.2.840.113556.1.4.766</span></span>               |
| <span data-ttu-id="d4d1e-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="d4d1e-119">System-Id-Guid</span></span>    | <span data-ttu-id="d4d1e-120">7f561283-5301-11d1-a9c5-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="d4d1e-120">7f561283-5301-11d1-a9c5-0000f80367c1</span></span> |
| <span data-ttu-id="d4d1e-121">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d4d1e-121">Syntax</span></span>            | [<span data-ttu-id="d4d1e-122">**Défini**</span><span class="sxs-lookup"><span data-stu-id="d4d1e-122">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="d4d1e-123">Implémentations</span><span class="sxs-lookup"><span data-stu-id="d4d1e-123">Implementations</span></span>

-   [<span data-ttu-id="d4d1e-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d4d1e-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d4d1e-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d4d1e-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d4d1e-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d4d1e-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d4d1e-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d4d1e-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d4d1e-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d4d1e-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d4d1e-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d4d1e-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d4d1e-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d4d1e-130">Windows 2000 Server</span></span>



| <span data-ttu-id="d4d1e-131">Entrée</span><span class="sxs-lookup"><span data-stu-id="d4d1e-131">Entry</span></span> | <span data-ttu-id="d4d1e-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4d1e-132">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4d1e-133">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d4d1e-133">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="d4d1e-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d4d1e-134">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="d4d1e-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="d4d1e-135">System-Only</span></span>            | <span data-ttu-id="d4d1e-136">Faux</span><span class="sxs-lookup"><span data-stu-id="d4d1e-136">False</span></span>                                                                                                      |
| <span data-ttu-id="d4d1e-137">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d4d1e-137">Is-Single-Valued</span></span>       | <span data-ttu-id="d4d1e-138">Vrai</span><span class="sxs-lookup"><span data-stu-id="d4d1e-138">True</span></span>                                                                                                       |
| <span data-ttu-id="d4d1e-139">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d4d1e-139">Is Indexed</span></span>             | <span data-ttu-id="d4d1e-140">Faux</span><span class="sxs-lookup"><span data-stu-id="d4d1e-140">False</span></span>                                                                                                      |
| <span data-ttu-id="d4d1e-141">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d4d1e-141">In Global Catalog</span></span>      | <span data-ttu-id="d4d1e-142">Faux</span><span class="sxs-lookup"><span data-stu-id="d4d1e-142">False</span></span>                                                                                                      |
| <span data-ttu-id="d4d1e-143">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d4d1e-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="d4d1e-144">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d4d1e-144">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="d4d1e-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d4d1e-145">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="d4d1e-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d4d1e-146">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="d4d1e-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d4d1e-147">Search-Flags</span></span>           | <span data-ttu-id="d4d1e-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d4d1e-148">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="d4d1e-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d4d1e-149">System-Flags</span></span>           | <span data-ttu-id="d4d1e-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d4d1e-150">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="d4d1e-151">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d4d1e-151">Classes used in</span></span>        | [<span data-ttu-id="d4d1e-152">**ACS-limites de ressources**</span><span class="sxs-lookup"><span data-stu-id="d4d1e-152">**ACS-Resource-Limits**</span></span>](c-acsresourcelimits.md)<br/> [<span data-ttu-id="d4d1e-153">**ACS-sous-réseau**</span><span class="sxs-lookup"><span data-stu-id="d4d1e-153">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d4d1e-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d4d1e-154">Windows Server 2003</span></span>



| <span data-ttu-id="d4d1e-155">Entrée</span><span class="sxs-lookup"><span data-stu-id="d4d1e-155">Entry</span></span> | <span data-ttu-id="d4d1e-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4d1e-156">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4d1e-157">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d4d1e-157">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="d4d1e-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d4d1e-158">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="d4d1e-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="d4d1e-159">System-Only</span></span>            | <span data-ttu-id="d4d1e-160">Faux</span><span class="sxs-lookup"><span data-stu-id="d4d1e-160">False</span></span>                                                                                                      |
| <span data-ttu-id="d4d1e-161">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d4d1e-161">Is-Single-Valued</span></span>       | <span data-ttu-id="d4d1e-162">Vrai</span><span class="sxs-lookup"><span data-stu-id="d4d1e-162">True</span></span>                                                                                                       |
| <span data-ttu-id="d4d1e-163">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d4d1e-163">Is Indexed</span></span>             | <span data-ttu-id="d4d1e-164">Faux</span><span class="sxs-lookup"><span data-stu-id="d4d1e-164">False</span></span>                                                                                                      |
| <span data-ttu-id="d4d1e-165">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d4d1e-165">In Global Catalog</span></span>      | <span data-ttu-id="d4d1e-166">Faux</span><span class="sxs-lookup"><span data-stu-id="d4d1e-166">False</span></span>                                                                                                      |
| <span data-ttu-id="d4d1e-167">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d4d1e-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="d4d1e-168">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d4d1e-168">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="d4d1e-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d4d1e-169">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="d4d1e-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d4d1e-170">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="d4d1e-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d4d1e-171">Search-Flags</span></span>           | <span data-ttu-id="d4d1e-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d4d1e-172">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="d4d1e-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d4d1e-173">System-Flags</span></span>           | <span data-ttu-id="d4d1e-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d4d1e-174">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="d4d1e-175">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d4d1e-175">Classes used in</span></span>        | [<span data-ttu-id="d4d1e-176">**ACS-limites de ressources**</span><span class="sxs-lookup"><span data-stu-id="d4d1e-176">**ACS-Resource-Limits**</span></span>](c-acsresourcelimits.md)<br/> [<span data-ttu-id="d4d1e-177">**ACS-sous-réseau**</span><span class="sxs-lookup"><span data-stu-id="d4d1e-177">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d4d1e-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d4d1e-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d4d1e-179">Entrée</span><span class="sxs-lookup"><span data-stu-id="d4d1e-179">Entry</span></span> | <span data-ttu-id="d4d1e-180">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4d1e-180">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4d1e-181">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d4d1e-181">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="d4d1e-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d4d1e-182">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="d4d1e-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="d4d1e-183">System-Only</span></span>            | <span data-ttu-id="d4d1e-184">Faux</span><span class="sxs-lookup"><span data-stu-id="d4d1e-184">False</span></span>                                                                                                      |
| <span data-ttu-id="d4d1e-185">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d4d1e-185">Is-Single-Valued</span></span>       | <span data-ttu-id="d4d1e-186">Vrai</span><span class="sxs-lookup"><span data-stu-id="d4d1e-186">True</span></span>                                                                                                       |
| <span data-ttu-id="d4d1e-187">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d4d1e-187">Is Indexed</span></span>             | <span data-ttu-id="d4d1e-188">Faux</span><span class="sxs-lookup"><span data-stu-id="d4d1e-188">False</span></span>                                                                                                      |
| <span data-ttu-id="d4d1e-189">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d4d1e-189">In Global Catalog</span></span>      | <span data-ttu-id="d4d1e-190">Faux</span><span class="sxs-lookup"><span data-stu-id="d4d1e-190">False</span></span>                                                                                                      |
| <span data-ttu-id="d4d1e-191">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d4d1e-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="d4d1e-192">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d4d1e-192">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="d4d1e-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d4d1e-193">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="d4d1e-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d4d1e-194">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="d4d1e-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d4d1e-195">Search-Flags</span></span>           | <span data-ttu-id="d4d1e-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d4d1e-196">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="d4d1e-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d4d1e-197">System-Flags</span></span>           | <span data-ttu-id="d4d1e-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d4d1e-198">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="d4d1e-199">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d4d1e-199">Classes used in</span></span>        | [<span data-ttu-id="d4d1e-200">**ACS-limites de ressources**</span><span class="sxs-lookup"><span data-stu-id="d4d1e-200">**ACS-Resource-Limits**</span></span>](c-acsresourcelimits.md)<br/> [<span data-ttu-id="d4d1e-201">**ACS-sous-réseau**</span><span class="sxs-lookup"><span data-stu-id="d4d1e-201">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d4d1e-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d4d1e-202">Windows Server 2008</span></span>



| <span data-ttu-id="d4d1e-203">Entrée</span><span class="sxs-lookup"><span data-stu-id="d4d1e-203">Entry</span></span> | <span data-ttu-id="d4d1e-204">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4d1e-204">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4d1e-205">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d4d1e-205">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="d4d1e-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d4d1e-206">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="d4d1e-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="d4d1e-207">System-Only</span></span>            | <span data-ttu-id="d4d1e-208">Faux</span><span class="sxs-lookup"><span data-stu-id="d4d1e-208">False</span></span>                                                                                                      |
| <span data-ttu-id="d4d1e-209">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d4d1e-209">Is-Single-Valued</span></span>       | <span data-ttu-id="d4d1e-210">Vrai</span><span class="sxs-lookup"><span data-stu-id="d4d1e-210">True</span></span>                                                                                                       |
| <span data-ttu-id="d4d1e-211">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d4d1e-211">Is Indexed</span></span>             | <span data-ttu-id="d4d1e-212">Faux</span><span class="sxs-lookup"><span data-stu-id="d4d1e-212">False</span></span>                                                                                                      |
| <span data-ttu-id="d4d1e-213">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d4d1e-213">In Global Catalog</span></span>      | <span data-ttu-id="d4d1e-214">Faux</span><span class="sxs-lookup"><span data-stu-id="d4d1e-214">False</span></span>                                                                                                      |
| <span data-ttu-id="d4d1e-215">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d4d1e-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="d4d1e-216">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d4d1e-216">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="d4d1e-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d4d1e-217">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="d4d1e-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d4d1e-218">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="d4d1e-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d4d1e-219">Search-Flags</span></span>           | <span data-ttu-id="d4d1e-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d4d1e-220">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="d4d1e-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d4d1e-221">System-Flags</span></span>           | <span data-ttu-id="d4d1e-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d4d1e-222">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="d4d1e-223">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d4d1e-223">Classes used in</span></span>        | [<span data-ttu-id="d4d1e-224">**ACS-limites de ressources**</span><span class="sxs-lookup"><span data-stu-id="d4d1e-224">**ACS-Resource-Limits**</span></span>](c-acsresourcelimits.md)<br/> [<span data-ttu-id="d4d1e-225">**ACS-sous-réseau**</span><span class="sxs-lookup"><span data-stu-id="d4d1e-225">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d4d1e-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d4d1e-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d4d1e-227">Entrée</span><span class="sxs-lookup"><span data-stu-id="d4d1e-227">Entry</span></span> | <span data-ttu-id="d4d1e-228">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4d1e-228">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4d1e-229">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d4d1e-229">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="d4d1e-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d4d1e-230">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="d4d1e-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="d4d1e-231">System-Only</span></span>            | <span data-ttu-id="d4d1e-232">Faux</span><span class="sxs-lookup"><span data-stu-id="d4d1e-232">False</span></span>                                                                                                      |
| <span data-ttu-id="d4d1e-233">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d4d1e-233">Is-Single-Valued</span></span>       | <span data-ttu-id="d4d1e-234">Vrai</span><span class="sxs-lookup"><span data-stu-id="d4d1e-234">True</span></span>                                                                                                       |
| <span data-ttu-id="d4d1e-235">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d4d1e-235">Is Indexed</span></span>             | <span data-ttu-id="d4d1e-236">Faux</span><span class="sxs-lookup"><span data-stu-id="d4d1e-236">False</span></span>                                                                                                      |
| <span data-ttu-id="d4d1e-237">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d4d1e-237">In Global Catalog</span></span>      | <span data-ttu-id="d4d1e-238">Faux</span><span class="sxs-lookup"><span data-stu-id="d4d1e-238">False</span></span>                                                                                                      |
| <span data-ttu-id="d4d1e-239">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d4d1e-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="d4d1e-240">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d4d1e-240">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="d4d1e-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d4d1e-241">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="d4d1e-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d4d1e-242">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="d4d1e-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d4d1e-243">Search-Flags</span></span>           | <span data-ttu-id="d4d1e-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d4d1e-244">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="d4d1e-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d4d1e-245">System-Flags</span></span>           | <span data-ttu-id="d4d1e-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d4d1e-246">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="d4d1e-247">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d4d1e-247">Classes used in</span></span>        | [<span data-ttu-id="d4d1e-248">**ACS-limites de ressources**</span><span class="sxs-lookup"><span data-stu-id="d4d1e-248">**ACS-Resource-Limits**</span></span>](c-acsresourcelimits.md)<br/> [<span data-ttu-id="d4d1e-249">**ACS-sous-réseau**</span><span class="sxs-lookup"><span data-stu-id="d4d1e-249">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d4d1e-250">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d4d1e-250">Windows Server 2012</span></span>



| <span data-ttu-id="d4d1e-251">Entrée</span><span class="sxs-lookup"><span data-stu-id="d4d1e-251">Entry</span></span> | <span data-ttu-id="d4d1e-252">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4d1e-252">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4d1e-253">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d4d1e-253">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="d4d1e-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d4d1e-254">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="d4d1e-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="d4d1e-255">System-Only</span></span>            | <span data-ttu-id="d4d1e-256">Faux</span><span class="sxs-lookup"><span data-stu-id="d4d1e-256">False</span></span>                                                                                                      |
| <span data-ttu-id="d4d1e-257">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d4d1e-257">Is-Single-Valued</span></span>       | <span data-ttu-id="d4d1e-258">Vrai</span><span class="sxs-lookup"><span data-stu-id="d4d1e-258">True</span></span>                                                                                                       |
| <span data-ttu-id="d4d1e-259">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d4d1e-259">Is Indexed</span></span>             | <span data-ttu-id="d4d1e-260">Faux</span><span class="sxs-lookup"><span data-stu-id="d4d1e-260">False</span></span>                                                                                                      |
| <span data-ttu-id="d4d1e-261">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d4d1e-261">In Global Catalog</span></span>      | <span data-ttu-id="d4d1e-262">Faux</span><span class="sxs-lookup"><span data-stu-id="d4d1e-262">False</span></span>                                                                                                      |
| <span data-ttu-id="d4d1e-263">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d4d1e-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="d4d1e-264">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d4d1e-264">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="d4d1e-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d4d1e-265">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="d4d1e-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d4d1e-266">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="d4d1e-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d4d1e-267">Search-Flags</span></span>           | <span data-ttu-id="d4d1e-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d4d1e-268">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="d4d1e-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d4d1e-269">System-Flags</span></span>           | <span data-ttu-id="d4d1e-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d4d1e-270">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="d4d1e-271">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d4d1e-271">Classes used in</span></span>        | [<span data-ttu-id="d4d1e-272">**ACS-limites de ressources**</span><span class="sxs-lookup"><span data-stu-id="d4d1e-272">**ACS-Resource-Limits**</span></span>](c-acsresourcelimits.md)<br/> [<span data-ttu-id="d4d1e-273">**ACS-sous-réseau**</span><span class="sxs-lookup"><span data-stu-id="d4d1e-273">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 





