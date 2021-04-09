---
title: attribut de stratégie d’attribution de nom pour netboot-New-machine
description: Indique le schéma d’affectation de noms que les nouveaux comptes d’ordinateurs clients utiliseront.
ms.assetid: e8ffc9b1-b2a2-4216-8498-85cb6c8cc7ae
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory de l’attribut de stratégie d’attribution de noms pour netboot-New-machine
- Schéma AD de l’attribut netbootNewMachineNamingPolicy
topic_type:
- apiref
api_name:
- netboot-New-Machine-Naming-Policy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6da6cb51ced16da6510f3fb85ec80e4fa641603b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104108006"
---
# <a name="netboot-new-machine-naming-policy-attribute"></a><span data-ttu-id="b51d9-105">attribut de stratégie d’attribution de nom pour netboot-New-machine</span><span class="sxs-lookup"><span data-stu-id="b51d9-105">netboot-New-Machine-Naming-Policy attribute</span></span>

<span data-ttu-id="b51d9-106">Indique le schéma d’affectation de noms que les nouveaux comptes d’ordinateurs clients utiliseront.</span><span class="sxs-lookup"><span data-stu-id="b51d9-106">Indicates the naming scheme which new client computer accounts will use.</span></span>



| <span data-ttu-id="b51d9-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="b51d9-107">Entry</span></span> | <span data-ttu-id="b51d9-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="b51d9-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="b51d9-109">CN</span><span class="sxs-lookup"><span data-stu-id="b51d9-109">CN</span></span>                | <span data-ttu-id="b51d9-110">netboot-New-machine-nommage-stratégie</span><span class="sxs-lookup"><span data-stu-id="b51d9-110">netboot-New-Machine-Naming-Policy</span></span>           |
| <span data-ttu-id="b51d9-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="b51d9-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b51d9-112">netbootNewMachineNamingPolicy</span><span class="sxs-lookup"><span data-stu-id="b51d9-112">netbootNewMachineNamingPolicy</span></span>               |
| <span data-ttu-id="b51d9-113">Taille</span><span class="sxs-lookup"><span data-stu-id="b51d9-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="b51d9-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="b51d9-114">Update Privilege</span></span>  | <span data-ttu-id="b51d9-115">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="b51d9-115">This value is set by the system.</span></span>            |
| <span data-ttu-id="b51d9-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="b51d9-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="b51d9-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b51d9-117">Attribute-Id</span></span>      | <span data-ttu-id="b51d9-118">1.2.840.113556.1.4.855</span><span class="sxs-lookup"><span data-stu-id="b51d9-118">1.2.840.113556.1.4.855</span></span>                      |
| <span data-ttu-id="b51d9-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b51d9-119">System-Id-Guid</span></span>    | <span data-ttu-id="b51d9-120">0738307c-91df-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="b51d9-120">0738307c-91df-11d1-aebc-0000f80367c1</span></span>        |
| <span data-ttu-id="b51d9-121">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b51d9-121">Syntax</span></span>            | [<span data-ttu-id="b51d9-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="b51d9-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="b51d9-123">Implémentations</span><span class="sxs-lookup"><span data-stu-id="b51d9-123">Implementations</span></span>

-   [<span data-ttu-id="b51d9-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b51d9-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b51d9-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b51d9-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b51d9-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b51d9-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b51d9-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b51d9-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b51d9-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b51d9-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b51d9-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b51d9-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b51d9-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b51d9-130">Windows 2000 Server</span></span>



| <span data-ttu-id="b51d9-131">Entrée</span><span class="sxs-lookup"><span data-stu-id="b51d9-131">Entry</span></span> | <span data-ttu-id="b51d9-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="b51d9-132">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="b51d9-133">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b51d9-133">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="b51d9-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b51d9-134">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="b51d9-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="b51d9-135">System-Only</span></span>            | <span data-ttu-id="b51d9-136">Faux</span><span class="sxs-lookup"><span data-stu-id="b51d9-136">False</span></span>                                                      |
| <span data-ttu-id="b51d9-137">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b51d9-137">Is-Single-Valued</span></span>       | <span data-ttu-id="b51d9-138">Faux</span><span class="sxs-lookup"><span data-stu-id="b51d9-138">False</span></span>                                                      |
| <span data-ttu-id="b51d9-139">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b51d9-139">Is Indexed</span></span>             | <span data-ttu-id="b51d9-140">Faux</span><span class="sxs-lookup"><span data-stu-id="b51d9-140">False</span></span>                                                      |
| <span data-ttu-id="b51d9-141">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b51d9-141">In Global Catalog</span></span>      | <span data-ttu-id="b51d9-142">Faux</span><span class="sxs-lookup"><span data-stu-id="b51d9-142">False</span></span>                                                      |
| <span data-ttu-id="b51d9-143">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b51d9-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="b51d9-144">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b51d9-144">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="b51d9-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b51d9-145">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="b51d9-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b51d9-146">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="b51d9-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b51d9-147">Search-Flags</span></span>           | <span data-ttu-id="b51d9-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b51d9-148">0x00000000</span></span>                                                 |
| <span data-ttu-id="b51d9-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b51d9-149">System-Flags</span></span>           | <span data-ttu-id="b51d9-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b51d9-150">0x00000010</span></span>                                                 |
| <span data-ttu-id="b51d9-151">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b51d9-151">Classes used in</span></span>        | [<span data-ttu-id="b51d9-152">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="b51d9-152">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b51d9-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b51d9-153">Windows Server 2003</span></span>



| <span data-ttu-id="b51d9-154">Entrée</span><span class="sxs-lookup"><span data-stu-id="b51d9-154">Entry</span></span> | <span data-ttu-id="b51d9-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="b51d9-155">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="b51d9-156">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b51d9-156">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="b51d9-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b51d9-157">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="b51d9-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="b51d9-158">System-Only</span></span>            | <span data-ttu-id="b51d9-159">Faux</span><span class="sxs-lookup"><span data-stu-id="b51d9-159">False</span></span>                                                      |
| <span data-ttu-id="b51d9-160">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b51d9-160">Is-Single-Valued</span></span>       | <span data-ttu-id="b51d9-161">Faux</span><span class="sxs-lookup"><span data-stu-id="b51d9-161">False</span></span>                                                      |
| <span data-ttu-id="b51d9-162">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b51d9-162">Is Indexed</span></span>             | <span data-ttu-id="b51d9-163">Faux</span><span class="sxs-lookup"><span data-stu-id="b51d9-163">False</span></span>                                                      |
| <span data-ttu-id="b51d9-164">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b51d9-164">In Global Catalog</span></span>      | <span data-ttu-id="b51d9-165">Faux</span><span class="sxs-lookup"><span data-stu-id="b51d9-165">False</span></span>                                                      |
| <span data-ttu-id="b51d9-166">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b51d9-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="b51d9-167">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b51d9-167">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="b51d9-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b51d9-168">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="b51d9-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b51d9-169">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="b51d9-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b51d9-170">Search-Flags</span></span>           | <span data-ttu-id="b51d9-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b51d9-171">0x00000000</span></span>                                                 |
| <span data-ttu-id="b51d9-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b51d9-172">System-Flags</span></span>           | <span data-ttu-id="b51d9-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b51d9-173">0x00000010</span></span>                                                 |
| <span data-ttu-id="b51d9-174">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b51d9-174">Classes used in</span></span>        | [<span data-ttu-id="b51d9-175">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="b51d9-175">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b51d9-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b51d9-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b51d9-177">Entrée</span><span class="sxs-lookup"><span data-stu-id="b51d9-177">Entry</span></span> | <span data-ttu-id="b51d9-178">Valeur</span><span class="sxs-lookup"><span data-stu-id="b51d9-178">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="b51d9-179">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b51d9-179">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="b51d9-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b51d9-180">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="b51d9-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="b51d9-181">System-Only</span></span>            | <span data-ttu-id="b51d9-182">Faux</span><span class="sxs-lookup"><span data-stu-id="b51d9-182">False</span></span>                                                      |
| <span data-ttu-id="b51d9-183">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b51d9-183">Is-Single-Valued</span></span>       | <span data-ttu-id="b51d9-184">Faux</span><span class="sxs-lookup"><span data-stu-id="b51d9-184">False</span></span>                                                      |
| <span data-ttu-id="b51d9-185">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b51d9-185">Is Indexed</span></span>             | <span data-ttu-id="b51d9-186">Faux</span><span class="sxs-lookup"><span data-stu-id="b51d9-186">False</span></span>                                                      |
| <span data-ttu-id="b51d9-187">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b51d9-187">In Global Catalog</span></span>      | <span data-ttu-id="b51d9-188">Faux</span><span class="sxs-lookup"><span data-stu-id="b51d9-188">False</span></span>                                                      |
| <span data-ttu-id="b51d9-189">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b51d9-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="b51d9-190">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b51d9-190">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="b51d9-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b51d9-191">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="b51d9-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b51d9-192">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="b51d9-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b51d9-193">Search-Flags</span></span>           | <span data-ttu-id="b51d9-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b51d9-194">0x00000000</span></span>                                                 |
| <span data-ttu-id="b51d9-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b51d9-195">System-Flags</span></span>           | <span data-ttu-id="b51d9-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b51d9-196">0x00000010</span></span>                                                 |
| <span data-ttu-id="b51d9-197">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b51d9-197">Classes used in</span></span>        | [<span data-ttu-id="b51d9-198">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="b51d9-198">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b51d9-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b51d9-199">Windows Server 2008</span></span>



| <span data-ttu-id="b51d9-200">Entrée</span><span class="sxs-lookup"><span data-stu-id="b51d9-200">Entry</span></span> | <span data-ttu-id="b51d9-201">Valeur</span><span class="sxs-lookup"><span data-stu-id="b51d9-201">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="b51d9-202">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b51d9-202">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="b51d9-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b51d9-203">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="b51d9-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="b51d9-204">System-Only</span></span>            | <span data-ttu-id="b51d9-205">Faux</span><span class="sxs-lookup"><span data-stu-id="b51d9-205">False</span></span>                                                      |
| <span data-ttu-id="b51d9-206">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b51d9-206">Is-Single-Valued</span></span>       | <span data-ttu-id="b51d9-207">Faux</span><span class="sxs-lookup"><span data-stu-id="b51d9-207">False</span></span>                                                      |
| <span data-ttu-id="b51d9-208">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b51d9-208">Is Indexed</span></span>             | <span data-ttu-id="b51d9-209">Faux</span><span class="sxs-lookup"><span data-stu-id="b51d9-209">False</span></span>                                                      |
| <span data-ttu-id="b51d9-210">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b51d9-210">In Global Catalog</span></span>      | <span data-ttu-id="b51d9-211">Faux</span><span class="sxs-lookup"><span data-stu-id="b51d9-211">False</span></span>                                                      |
| <span data-ttu-id="b51d9-212">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b51d9-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="b51d9-213">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b51d9-213">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="b51d9-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b51d9-214">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="b51d9-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b51d9-215">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="b51d9-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b51d9-216">Search-Flags</span></span>           | <span data-ttu-id="b51d9-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b51d9-217">0x00000000</span></span>                                                 |
| <span data-ttu-id="b51d9-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b51d9-218">System-Flags</span></span>           | <span data-ttu-id="b51d9-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b51d9-219">0x00000010</span></span>                                                 |
| <span data-ttu-id="b51d9-220">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b51d9-220">Classes used in</span></span>        | [<span data-ttu-id="b51d9-221">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="b51d9-221">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b51d9-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b51d9-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b51d9-223">Entrée</span><span class="sxs-lookup"><span data-stu-id="b51d9-223">Entry</span></span> | <span data-ttu-id="b51d9-224">Valeur</span><span class="sxs-lookup"><span data-stu-id="b51d9-224">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="b51d9-225">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b51d9-225">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="b51d9-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b51d9-226">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="b51d9-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="b51d9-227">System-Only</span></span>            | <span data-ttu-id="b51d9-228">Faux</span><span class="sxs-lookup"><span data-stu-id="b51d9-228">False</span></span>                                                      |
| <span data-ttu-id="b51d9-229">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b51d9-229">Is-Single-Valued</span></span>       | <span data-ttu-id="b51d9-230">Faux</span><span class="sxs-lookup"><span data-stu-id="b51d9-230">False</span></span>                                                      |
| <span data-ttu-id="b51d9-231">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b51d9-231">Is Indexed</span></span>             | <span data-ttu-id="b51d9-232">Faux</span><span class="sxs-lookup"><span data-stu-id="b51d9-232">False</span></span>                                                      |
| <span data-ttu-id="b51d9-233">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b51d9-233">In Global Catalog</span></span>      | <span data-ttu-id="b51d9-234">Faux</span><span class="sxs-lookup"><span data-stu-id="b51d9-234">False</span></span>                                                      |
| <span data-ttu-id="b51d9-235">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b51d9-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="b51d9-236">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b51d9-236">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="b51d9-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b51d9-237">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="b51d9-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b51d9-238">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="b51d9-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b51d9-239">Search-Flags</span></span>           | <span data-ttu-id="b51d9-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b51d9-240">0x00000000</span></span>                                                 |
| <span data-ttu-id="b51d9-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b51d9-241">System-Flags</span></span>           | <span data-ttu-id="b51d9-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b51d9-242">0x00000010</span></span>                                                 |
| <span data-ttu-id="b51d9-243">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b51d9-243">Classes used in</span></span>        | [<span data-ttu-id="b51d9-244">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="b51d9-244">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b51d9-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b51d9-245">Windows Server 2012</span></span>



| <span data-ttu-id="b51d9-246">Entrée</span><span class="sxs-lookup"><span data-stu-id="b51d9-246">Entry</span></span> | <span data-ttu-id="b51d9-247">Valeur</span><span class="sxs-lookup"><span data-stu-id="b51d9-247">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="b51d9-248">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b51d9-248">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="b51d9-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b51d9-249">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="b51d9-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="b51d9-250">System-Only</span></span>            | <span data-ttu-id="b51d9-251">Faux</span><span class="sxs-lookup"><span data-stu-id="b51d9-251">False</span></span>                                                      |
| <span data-ttu-id="b51d9-252">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b51d9-252">Is-Single-Valued</span></span>       | <span data-ttu-id="b51d9-253">Faux</span><span class="sxs-lookup"><span data-stu-id="b51d9-253">False</span></span>                                                      |
| <span data-ttu-id="b51d9-254">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b51d9-254">Is Indexed</span></span>             | <span data-ttu-id="b51d9-255">Faux</span><span class="sxs-lookup"><span data-stu-id="b51d9-255">False</span></span>                                                      |
| <span data-ttu-id="b51d9-256">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b51d9-256">In Global Catalog</span></span>      | <span data-ttu-id="b51d9-257">Faux</span><span class="sxs-lookup"><span data-stu-id="b51d9-257">False</span></span>                                                      |
| <span data-ttu-id="b51d9-258">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b51d9-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="b51d9-259">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b51d9-259">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="b51d9-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b51d9-260">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="b51d9-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b51d9-261">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="b51d9-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b51d9-262">Search-Flags</span></span>           | <span data-ttu-id="b51d9-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b51d9-263">0x00000000</span></span>                                                 |
| <span data-ttu-id="b51d9-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b51d9-264">System-Flags</span></span>           | <span data-ttu-id="b51d9-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b51d9-265">0x00000010</span></span>                                                 |
| <span data-ttu-id="b51d9-266">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b51d9-266">Classes used in</span></span>        | [<span data-ttu-id="b51d9-267">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="b51d9-267">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



 

 





