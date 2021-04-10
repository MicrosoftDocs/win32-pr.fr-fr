---
title: ACS-attribut de type de service
description: Type de service ACS. Charge contrôlée ou bande passante garantie.
ms.assetid: 3de23f2b-16dc-48c0-a8c5-e3130cd84ba8
ms.tgt_platform: multiple
keywords:
- ACS-schéma AD d’attribut de type service
- Schéma AD de l’attribut aCSServiceType
topic_type:
- apiref
api_name:
- ACS-Service-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b7dc97c17e9f7b38fa2f6f0ea863099bbef838a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107314"
---
# <a name="acs-service-type-attribute"></a><span data-ttu-id="e2c23-106">ACS-attribut de type de service</span><span class="sxs-lookup"><span data-stu-id="e2c23-106">ACS-Service-Type attribute</span></span>

<span data-ttu-id="e2c23-107">Type de service ACS.</span><span class="sxs-lookup"><span data-stu-id="e2c23-107">The ACS service type.</span></span> <span data-ttu-id="e2c23-108">Charge contrôlée ou bande passante garantie.</span><span class="sxs-lookup"><span data-stu-id="e2c23-108">Controlled load or guaranteed bandwidth.</span></span>



| <span data-ttu-id="e2c23-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="e2c23-109">Entry</span></span> | <span data-ttu-id="e2c23-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="e2c23-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="e2c23-111">CN</span><span class="sxs-lookup"><span data-stu-id="e2c23-111">CN</span></span>                | <span data-ttu-id="e2c23-112">ACS-type de service</span><span class="sxs-lookup"><span data-stu-id="e2c23-112">ACS-Service-Type</span></span>                     |
| <span data-ttu-id="e2c23-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="e2c23-113">Ldap-Display-Name</span></span> | <span data-ttu-id="e2c23-114">aCSServiceType</span><span class="sxs-lookup"><span data-stu-id="e2c23-114">aCSServiceType</span></span>                       |
| <span data-ttu-id="e2c23-115">Taille</span><span class="sxs-lookup"><span data-stu-id="e2c23-115">Size</span></span>              | <span data-ttu-id="e2c23-116">4 octets</span><span class="sxs-lookup"><span data-stu-id="e2c23-116">4 bytes</span></span>                              |
| <span data-ttu-id="e2c23-117">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="e2c23-117">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="e2c23-118">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="e2c23-118">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="e2c23-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e2c23-119">Attribute-Id</span></span>      | <span data-ttu-id="e2c23-120">1.2.840.113556.1.4.762</span><span class="sxs-lookup"><span data-stu-id="e2c23-120">1.2.840.113556.1.4.762</span></span>               |
| <span data-ttu-id="e2c23-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="e2c23-121">System-Id-Guid</span></span>    | <span data-ttu-id="e2c23-122">7f56127f-5301-11d1-a9c5-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="e2c23-122">7f56127f-5301-11d1-a9c5-0000f80367c1</span></span> |
| <span data-ttu-id="e2c23-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e2c23-123">Syntax</span></span>            | [<span data-ttu-id="e2c23-124">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="e2c23-124">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="e2c23-125">Implémentations</span><span class="sxs-lookup"><span data-stu-id="e2c23-125">Implementations</span></span>

-   [<span data-ttu-id="e2c23-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e2c23-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e2c23-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e2c23-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e2c23-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e2c23-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e2c23-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e2c23-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e2c23-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e2c23-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e2c23-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e2c23-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e2c23-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e2c23-132">Windows 2000 Server</span></span>



| <span data-ttu-id="e2c23-133">Entrée</span><span class="sxs-lookup"><span data-stu-id="e2c23-133">Entry</span></span> | <span data-ttu-id="e2c23-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="e2c23-134">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2c23-135">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e2c23-135">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="e2c23-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e2c23-136">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="e2c23-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="e2c23-137">System-Only</span></span>            | <span data-ttu-id="e2c23-138">Faux</span><span class="sxs-lookup"><span data-stu-id="e2c23-138">False</span></span>                                                                                                      |
| <span data-ttu-id="e2c23-139">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e2c23-139">Is-Single-Valued</span></span>       | <span data-ttu-id="e2c23-140">Vrai</span><span class="sxs-lookup"><span data-stu-id="e2c23-140">True</span></span>                                                                                                       |
| <span data-ttu-id="e2c23-141">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e2c23-141">Is Indexed</span></span>             | <span data-ttu-id="e2c23-142">Faux</span><span class="sxs-lookup"><span data-stu-id="e2c23-142">False</span></span>                                                                                                      |
| <span data-ttu-id="e2c23-143">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e2c23-143">In Global Catalog</span></span>      | <span data-ttu-id="e2c23-144">Faux</span><span class="sxs-lookup"><span data-stu-id="e2c23-144">False</span></span>                                                                                                      |
| <span data-ttu-id="e2c23-145">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e2c23-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="e2c23-146">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e2c23-146">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="e2c23-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e2c23-147">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="e2c23-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e2c23-148">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="e2c23-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e2c23-149">Search-Flags</span></span>           | <span data-ttu-id="e2c23-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e2c23-150">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="e2c23-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e2c23-151">System-Flags</span></span>           | <span data-ttu-id="e2c23-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e2c23-152">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="e2c23-153">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e2c23-153">Classes used in</span></span>        | [<span data-ttu-id="e2c23-154">**ACS-stratégie**</span><span class="sxs-lookup"><span data-stu-id="e2c23-154">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> [<span data-ttu-id="e2c23-155">**ACS-limites de ressources**</span><span class="sxs-lookup"><span data-stu-id="e2c23-155">**ACS-Resource-Limits**</span></span>](c-acsresourcelimits.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e2c23-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e2c23-156">Windows Server 2003</span></span>



| <span data-ttu-id="e2c23-157">Entrée</span><span class="sxs-lookup"><span data-stu-id="e2c23-157">Entry</span></span> | <span data-ttu-id="e2c23-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="e2c23-158">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2c23-159">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e2c23-159">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="e2c23-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e2c23-160">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="e2c23-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="e2c23-161">System-Only</span></span>            | <span data-ttu-id="e2c23-162">Faux</span><span class="sxs-lookup"><span data-stu-id="e2c23-162">False</span></span>                                                                                                      |
| <span data-ttu-id="e2c23-163">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e2c23-163">Is-Single-Valued</span></span>       | <span data-ttu-id="e2c23-164">Vrai</span><span class="sxs-lookup"><span data-stu-id="e2c23-164">True</span></span>                                                                                                       |
| <span data-ttu-id="e2c23-165">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e2c23-165">Is Indexed</span></span>             | <span data-ttu-id="e2c23-166">Faux</span><span class="sxs-lookup"><span data-stu-id="e2c23-166">False</span></span>                                                                                                      |
| <span data-ttu-id="e2c23-167">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e2c23-167">In Global Catalog</span></span>      | <span data-ttu-id="e2c23-168">Faux</span><span class="sxs-lookup"><span data-stu-id="e2c23-168">False</span></span>                                                                                                      |
| <span data-ttu-id="e2c23-169">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e2c23-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="e2c23-170">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e2c23-170">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="e2c23-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e2c23-171">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="e2c23-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e2c23-172">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="e2c23-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e2c23-173">Search-Flags</span></span>           | <span data-ttu-id="e2c23-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e2c23-174">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="e2c23-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e2c23-175">System-Flags</span></span>           | <span data-ttu-id="e2c23-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e2c23-176">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="e2c23-177">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e2c23-177">Classes used in</span></span>        | [<span data-ttu-id="e2c23-178">**ACS-stratégie**</span><span class="sxs-lookup"><span data-stu-id="e2c23-178">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> [<span data-ttu-id="e2c23-179">**ACS-limites de ressources**</span><span class="sxs-lookup"><span data-stu-id="e2c23-179">**ACS-Resource-Limits**</span></span>](c-acsresourcelimits.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e2c23-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e2c23-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e2c23-181">Entrée</span><span class="sxs-lookup"><span data-stu-id="e2c23-181">Entry</span></span> | <span data-ttu-id="e2c23-182">Valeur</span><span class="sxs-lookup"><span data-stu-id="e2c23-182">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2c23-183">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e2c23-183">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="e2c23-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e2c23-184">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="e2c23-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="e2c23-185">System-Only</span></span>            | <span data-ttu-id="e2c23-186">Faux</span><span class="sxs-lookup"><span data-stu-id="e2c23-186">False</span></span>                                                                                                      |
| <span data-ttu-id="e2c23-187">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e2c23-187">Is-Single-Valued</span></span>       | <span data-ttu-id="e2c23-188">Vrai</span><span class="sxs-lookup"><span data-stu-id="e2c23-188">True</span></span>                                                                                                       |
| <span data-ttu-id="e2c23-189">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e2c23-189">Is Indexed</span></span>             | <span data-ttu-id="e2c23-190">Faux</span><span class="sxs-lookup"><span data-stu-id="e2c23-190">False</span></span>                                                                                                      |
| <span data-ttu-id="e2c23-191">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e2c23-191">In Global Catalog</span></span>      | <span data-ttu-id="e2c23-192">Faux</span><span class="sxs-lookup"><span data-stu-id="e2c23-192">False</span></span>                                                                                                      |
| <span data-ttu-id="e2c23-193">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e2c23-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="e2c23-194">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e2c23-194">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="e2c23-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e2c23-195">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="e2c23-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e2c23-196">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="e2c23-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e2c23-197">Search-Flags</span></span>           | <span data-ttu-id="e2c23-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e2c23-198">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="e2c23-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e2c23-199">System-Flags</span></span>           | <span data-ttu-id="e2c23-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e2c23-200">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="e2c23-201">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e2c23-201">Classes used in</span></span>        | [<span data-ttu-id="e2c23-202">**ACS-stratégie**</span><span class="sxs-lookup"><span data-stu-id="e2c23-202">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> [<span data-ttu-id="e2c23-203">**ACS-limites de ressources**</span><span class="sxs-lookup"><span data-stu-id="e2c23-203">**ACS-Resource-Limits**</span></span>](c-acsresourcelimits.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e2c23-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e2c23-204">Windows Server 2008</span></span>



| <span data-ttu-id="e2c23-205">Entrée</span><span class="sxs-lookup"><span data-stu-id="e2c23-205">Entry</span></span> | <span data-ttu-id="e2c23-206">Valeur</span><span class="sxs-lookup"><span data-stu-id="e2c23-206">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2c23-207">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e2c23-207">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="e2c23-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e2c23-208">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="e2c23-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="e2c23-209">System-Only</span></span>            | <span data-ttu-id="e2c23-210">Faux</span><span class="sxs-lookup"><span data-stu-id="e2c23-210">False</span></span>                                                                                                      |
| <span data-ttu-id="e2c23-211">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e2c23-211">Is-Single-Valued</span></span>       | <span data-ttu-id="e2c23-212">Vrai</span><span class="sxs-lookup"><span data-stu-id="e2c23-212">True</span></span>                                                                                                       |
| <span data-ttu-id="e2c23-213">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e2c23-213">Is Indexed</span></span>             | <span data-ttu-id="e2c23-214">Faux</span><span class="sxs-lookup"><span data-stu-id="e2c23-214">False</span></span>                                                                                                      |
| <span data-ttu-id="e2c23-215">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e2c23-215">In Global Catalog</span></span>      | <span data-ttu-id="e2c23-216">Faux</span><span class="sxs-lookup"><span data-stu-id="e2c23-216">False</span></span>                                                                                                      |
| <span data-ttu-id="e2c23-217">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e2c23-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="e2c23-218">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e2c23-218">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="e2c23-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e2c23-219">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="e2c23-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e2c23-220">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="e2c23-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e2c23-221">Search-Flags</span></span>           | <span data-ttu-id="e2c23-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e2c23-222">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="e2c23-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e2c23-223">System-Flags</span></span>           | <span data-ttu-id="e2c23-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e2c23-224">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="e2c23-225">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e2c23-225">Classes used in</span></span>        | [<span data-ttu-id="e2c23-226">**ACS-stratégie**</span><span class="sxs-lookup"><span data-stu-id="e2c23-226">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> [<span data-ttu-id="e2c23-227">**ACS-limites de ressources**</span><span class="sxs-lookup"><span data-stu-id="e2c23-227">**ACS-Resource-Limits**</span></span>](c-acsresourcelimits.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e2c23-228">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e2c23-228">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e2c23-229">Entrée</span><span class="sxs-lookup"><span data-stu-id="e2c23-229">Entry</span></span> | <span data-ttu-id="e2c23-230">Valeur</span><span class="sxs-lookup"><span data-stu-id="e2c23-230">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2c23-231">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e2c23-231">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="e2c23-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e2c23-232">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="e2c23-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="e2c23-233">System-Only</span></span>            | <span data-ttu-id="e2c23-234">Faux</span><span class="sxs-lookup"><span data-stu-id="e2c23-234">False</span></span>                                                                                                      |
| <span data-ttu-id="e2c23-235">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e2c23-235">Is-Single-Valued</span></span>       | <span data-ttu-id="e2c23-236">Vrai</span><span class="sxs-lookup"><span data-stu-id="e2c23-236">True</span></span>                                                                                                       |
| <span data-ttu-id="e2c23-237">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e2c23-237">Is Indexed</span></span>             | <span data-ttu-id="e2c23-238">Faux</span><span class="sxs-lookup"><span data-stu-id="e2c23-238">False</span></span>                                                                                                      |
| <span data-ttu-id="e2c23-239">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e2c23-239">In Global Catalog</span></span>      | <span data-ttu-id="e2c23-240">Faux</span><span class="sxs-lookup"><span data-stu-id="e2c23-240">False</span></span>                                                                                                      |
| <span data-ttu-id="e2c23-241">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e2c23-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="e2c23-242">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e2c23-242">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="e2c23-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e2c23-243">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="e2c23-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e2c23-244">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="e2c23-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e2c23-245">Search-Flags</span></span>           | <span data-ttu-id="e2c23-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e2c23-246">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="e2c23-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e2c23-247">System-Flags</span></span>           | <span data-ttu-id="e2c23-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e2c23-248">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="e2c23-249">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e2c23-249">Classes used in</span></span>        | [<span data-ttu-id="e2c23-250">**ACS-stratégie**</span><span class="sxs-lookup"><span data-stu-id="e2c23-250">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> [<span data-ttu-id="e2c23-251">**ACS-limites de ressources**</span><span class="sxs-lookup"><span data-stu-id="e2c23-251">**ACS-Resource-Limits**</span></span>](c-acsresourcelimits.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e2c23-252">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e2c23-252">Windows Server 2012</span></span>



| <span data-ttu-id="e2c23-253">Entrée</span><span class="sxs-lookup"><span data-stu-id="e2c23-253">Entry</span></span> | <span data-ttu-id="e2c23-254">Valeur</span><span class="sxs-lookup"><span data-stu-id="e2c23-254">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2c23-255">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e2c23-255">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="e2c23-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e2c23-256">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="e2c23-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="e2c23-257">System-Only</span></span>            | <span data-ttu-id="e2c23-258">Faux</span><span class="sxs-lookup"><span data-stu-id="e2c23-258">False</span></span>                                                                                                      |
| <span data-ttu-id="e2c23-259">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e2c23-259">Is-Single-Valued</span></span>       | <span data-ttu-id="e2c23-260">Vrai</span><span class="sxs-lookup"><span data-stu-id="e2c23-260">True</span></span>                                                                                                       |
| <span data-ttu-id="e2c23-261">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e2c23-261">Is Indexed</span></span>             | <span data-ttu-id="e2c23-262">Faux</span><span class="sxs-lookup"><span data-stu-id="e2c23-262">False</span></span>                                                                                                      |
| <span data-ttu-id="e2c23-263">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e2c23-263">In Global Catalog</span></span>      | <span data-ttu-id="e2c23-264">Faux</span><span class="sxs-lookup"><span data-stu-id="e2c23-264">False</span></span>                                                                                                      |
| <span data-ttu-id="e2c23-265">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e2c23-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="e2c23-266">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e2c23-266">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="e2c23-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e2c23-267">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="e2c23-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e2c23-268">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="e2c23-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e2c23-269">Search-Flags</span></span>           | <span data-ttu-id="e2c23-270">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e2c23-270">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="e2c23-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e2c23-271">System-Flags</span></span>           | <span data-ttu-id="e2c23-272">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e2c23-272">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="e2c23-273">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e2c23-273">Classes used in</span></span>        | [<span data-ttu-id="e2c23-274">**ACS-stratégie**</span><span class="sxs-lookup"><span data-stu-id="e2c23-274">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> [<span data-ttu-id="e2c23-275">**ACS-limites de ressources**</span><span class="sxs-lookup"><span data-stu-id="e2c23-275">**ACS-Resource-Limits**</span></span>](c-acsresourcelimits.md)<br/> |



 

 





