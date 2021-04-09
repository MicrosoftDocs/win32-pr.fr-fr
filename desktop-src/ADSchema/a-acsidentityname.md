---
title: ACS-Identity-Name (attribut)
description: Cet attribut contient le nom unique d’un utilisateur ou d’une unité d’organisation et est l’identité d’un utilisateur ou d’un groupe d’utilisateurs auxquels cette stratégie de QoS s’applique.
ms.assetid: 00e6e2bd-aec8-426f-b89e-0661c15cfd46
ms.tgt_platform: multiple
keywords:
- AD-attribut de nom d’identité ACS
- Schéma AD de l’attribut aCSIdentityName
topic_type:
- apiref
api_name:
- ACS-Identity-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33ef1db92b908ef8474dfb125aca678d3c22d09f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104108315"
---
# <a name="acs-identity-name-attribute"></a><span data-ttu-id="6b5ce-105">ACS-Identity-Name (attribut)</span><span class="sxs-lookup"><span data-stu-id="6b5ce-105">ACS-Identity-Name attribute</span></span>

<span data-ttu-id="6b5ce-106">Cet attribut contient le nom unique d’un utilisateur ou d’une unité d’organisation et est l’identité d’un utilisateur ou d’un groupe d’utilisateurs auxquels cette stratégie de QoS s’applique.</span><span class="sxs-lookup"><span data-stu-id="6b5ce-106">This attribute contains the DN of a user or OU and is the identity of a user or a group of users to which this QoS policy applies.</span></span>



| <span data-ttu-id="6b5ce-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="6b5ce-107">Entry</span></span> | <span data-ttu-id="6b5ce-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="6b5ce-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="6b5ce-109">CN</span><span class="sxs-lookup"><span data-stu-id="6b5ce-109">CN</span></span>                | <span data-ttu-id="6b5ce-110">ACS-Identity-Name</span><span class="sxs-lookup"><span data-stu-id="6b5ce-110">ACS-Identity-Name</span></span>                           |
| <span data-ttu-id="6b5ce-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="6b5ce-111">Ldap-Display-Name</span></span> | <span data-ttu-id="6b5ce-112">aCSIdentityName</span><span class="sxs-lookup"><span data-stu-id="6b5ce-112">aCSIdentityName</span></span>                             |
| <span data-ttu-id="6b5ce-113">Taille</span><span class="sxs-lookup"><span data-stu-id="6b5ce-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="6b5ce-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="6b5ce-114">Update Privilege</span></span>  | <span data-ttu-id="6b5ce-115">Administrateur de domaine</span><span class="sxs-lookup"><span data-stu-id="6b5ce-115">Domain administrator</span></span>                        |
| <span data-ttu-id="6b5ce-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="6b5ce-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="6b5ce-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6b5ce-117">Attribute-Id</span></span>      | <span data-ttu-id="6b5ce-118">1.2.840.113556.1.4.784</span><span class="sxs-lookup"><span data-stu-id="6b5ce-118">1.2.840.113556.1.4.784</span></span>                      |
| <span data-ttu-id="6b5ce-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="6b5ce-119">System-Id-Guid</span></span>    | <span data-ttu-id="6b5ce-120">dab029b6-ddf7-11d1-90a5-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="6b5ce-120">dab029b6-ddf7-11d1-90a5-00c04fd91ab1</span></span>        |
| <span data-ttu-id="6b5ce-121">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6b5ce-121">Syntax</span></span>            | [<span data-ttu-id="6b5ce-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="6b5ce-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="6b5ce-123">Implémentations</span><span class="sxs-lookup"><span data-stu-id="6b5ce-123">Implementations</span></span>

-   [<span data-ttu-id="6b5ce-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6b5ce-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6b5ce-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6b5ce-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6b5ce-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6b5ce-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6b5ce-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6b5ce-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6b5ce-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6b5ce-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6b5ce-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6b5ce-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6b5ce-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6b5ce-130">Windows 2000 Server</span></span>



| <span data-ttu-id="6b5ce-131">Entrée</span><span class="sxs-lookup"><span data-stu-id="6b5ce-131">Entry</span></span> | <span data-ttu-id="6b5ce-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="6b5ce-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="6b5ce-133">ID de lien</span><span class="sxs-lookup"><span data-stu-id="6b5ce-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="6b5ce-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6b5ce-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="6b5ce-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="6b5ce-135">System-Only</span></span>            | <span data-ttu-id="6b5ce-136">Faux</span><span class="sxs-lookup"><span data-stu-id="6b5ce-136">False</span></span>                                        |
| <span data-ttu-id="6b5ce-137">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="6b5ce-137">Is-Single-Valued</span></span>       | <span data-ttu-id="6b5ce-138">Faux</span><span class="sxs-lookup"><span data-stu-id="6b5ce-138">False</span></span>                                        |
| <span data-ttu-id="6b5ce-139">Est indexé</span><span class="sxs-lookup"><span data-stu-id="6b5ce-139">Is Indexed</span></span>             | <span data-ttu-id="6b5ce-140">Faux</span><span class="sxs-lookup"><span data-stu-id="6b5ce-140">False</span></span>                                        |
| <span data-ttu-id="6b5ce-141">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="6b5ce-141">In Global Catalog</span></span>      | <span data-ttu-id="6b5ce-142">Faux</span><span class="sxs-lookup"><span data-stu-id="6b5ce-142">False</span></span>                                        |
| <span data-ttu-id="6b5ce-143">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="6b5ce-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="6b5ce-144">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="6b5ce-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="6b5ce-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6b5ce-145">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="6b5ce-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6b5ce-146">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="6b5ce-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6b5ce-147">Search-Flags</span></span>           | <span data-ttu-id="6b5ce-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6b5ce-148">0x00000000</span></span>                                   |
| <span data-ttu-id="6b5ce-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6b5ce-149">System-Flags</span></span>           | <span data-ttu-id="6b5ce-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6b5ce-150">0x00000010</span></span>                                   |
| <span data-ttu-id="6b5ce-151">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="6b5ce-151">Classes used in</span></span>        | [<span data-ttu-id="6b5ce-152">**ACS-stratégie**</span><span class="sxs-lookup"><span data-stu-id="6b5ce-152">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6b5ce-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6b5ce-153">Windows Server 2003</span></span>



| <span data-ttu-id="6b5ce-154">Entrée</span><span class="sxs-lookup"><span data-stu-id="6b5ce-154">Entry</span></span> | <span data-ttu-id="6b5ce-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="6b5ce-155">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="6b5ce-156">ID de lien</span><span class="sxs-lookup"><span data-stu-id="6b5ce-156">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="6b5ce-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6b5ce-157">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="6b5ce-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="6b5ce-158">System-Only</span></span>            | <span data-ttu-id="6b5ce-159">Faux</span><span class="sxs-lookup"><span data-stu-id="6b5ce-159">False</span></span>                                        |
| <span data-ttu-id="6b5ce-160">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="6b5ce-160">Is-Single-Valued</span></span>       | <span data-ttu-id="6b5ce-161">Faux</span><span class="sxs-lookup"><span data-stu-id="6b5ce-161">False</span></span>                                        |
| <span data-ttu-id="6b5ce-162">Est indexé</span><span class="sxs-lookup"><span data-stu-id="6b5ce-162">Is Indexed</span></span>             | <span data-ttu-id="6b5ce-163">Faux</span><span class="sxs-lookup"><span data-stu-id="6b5ce-163">False</span></span>                                        |
| <span data-ttu-id="6b5ce-164">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="6b5ce-164">In Global Catalog</span></span>      | <span data-ttu-id="6b5ce-165">Faux</span><span class="sxs-lookup"><span data-stu-id="6b5ce-165">False</span></span>                                        |
| <span data-ttu-id="6b5ce-166">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="6b5ce-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="6b5ce-167">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="6b5ce-167">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="6b5ce-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6b5ce-168">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="6b5ce-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6b5ce-169">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="6b5ce-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6b5ce-170">Search-Flags</span></span>           | <span data-ttu-id="6b5ce-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6b5ce-171">0x00000000</span></span>                                   |
| <span data-ttu-id="6b5ce-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6b5ce-172">System-Flags</span></span>           | <span data-ttu-id="6b5ce-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6b5ce-173">0x00000010</span></span>                                   |
| <span data-ttu-id="6b5ce-174">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="6b5ce-174">Classes used in</span></span>        | [<span data-ttu-id="6b5ce-175">**ACS-stratégie**</span><span class="sxs-lookup"><span data-stu-id="6b5ce-175">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6b5ce-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6b5ce-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6b5ce-177">Entrée</span><span class="sxs-lookup"><span data-stu-id="6b5ce-177">Entry</span></span> | <span data-ttu-id="6b5ce-178">Valeur</span><span class="sxs-lookup"><span data-stu-id="6b5ce-178">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="6b5ce-179">ID de lien</span><span class="sxs-lookup"><span data-stu-id="6b5ce-179">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="6b5ce-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6b5ce-180">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="6b5ce-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="6b5ce-181">System-Only</span></span>            | <span data-ttu-id="6b5ce-182">Faux</span><span class="sxs-lookup"><span data-stu-id="6b5ce-182">False</span></span>                                        |
| <span data-ttu-id="6b5ce-183">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="6b5ce-183">Is-Single-Valued</span></span>       | <span data-ttu-id="6b5ce-184">Faux</span><span class="sxs-lookup"><span data-stu-id="6b5ce-184">False</span></span>                                        |
| <span data-ttu-id="6b5ce-185">Est indexé</span><span class="sxs-lookup"><span data-stu-id="6b5ce-185">Is Indexed</span></span>             | <span data-ttu-id="6b5ce-186">Faux</span><span class="sxs-lookup"><span data-stu-id="6b5ce-186">False</span></span>                                        |
| <span data-ttu-id="6b5ce-187">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="6b5ce-187">In Global Catalog</span></span>      | <span data-ttu-id="6b5ce-188">Faux</span><span class="sxs-lookup"><span data-stu-id="6b5ce-188">False</span></span>                                        |
| <span data-ttu-id="6b5ce-189">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="6b5ce-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="6b5ce-190">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="6b5ce-190">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="6b5ce-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6b5ce-191">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="6b5ce-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6b5ce-192">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="6b5ce-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6b5ce-193">Search-Flags</span></span>           | <span data-ttu-id="6b5ce-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6b5ce-194">0x00000000</span></span>                                   |
| <span data-ttu-id="6b5ce-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6b5ce-195">System-Flags</span></span>           | <span data-ttu-id="6b5ce-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6b5ce-196">0x00000010</span></span>                                   |
| <span data-ttu-id="6b5ce-197">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="6b5ce-197">Classes used in</span></span>        | [<span data-ttu-id="6b5ce-198">**ACS-stratégie**</span><span class="sxs-lookup"><span data-stu-id="6b5ce-198">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6b5ce-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6b5ce-199">Windows Server 2008</span></span>



| <span data-ttu-id="6b5ce-200">Entrée</span><span class="sxs-lookup"><span data-stu-id="6b5ce-200">Entry</span></span> | <span data-ttu-id="6b5ce-201">Valeur</span><span class="sxs-lookup"><span data-stu-id="6b5ce-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="6b5ce-202">ID de lien</span><span class="sxs-lookup"><span data-stu-id="6b5ce-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="6b5ce-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6b5ce-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="6b5ce-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="6b5ce-204">System-Only</span></span>            | <span data-ttu-id="6b5ce-205">Faux</span><span class="sxs-lookup"><span data-stu-id="6b5ce-205">False</span></span>                                        |
| <span data-ttu-id="6b5ce-206">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="6b5ce-206">Is-Single-Valued</span></span>       | <span data-ttu-id="6b5ce-207">Faux</span><span class="sxs-lookup"><span data-stu-id="6b5ce-207">False</span></span>                                        |
| <span data-ttu-id="6b5ce-208">Est indexé</span><span class="sxs-lookup"><span data-stu-id="6b5ce-208">Is Indexed</span></span>             | <span data-ttu-id="6b5ce-209">Faux</span><span class="sxs-lookup"><span data-stu-id="6b5ce-209">False</span></span>                                        |
| <span data-ttu-id="6b5ce-210">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="6b5ce-210">In Global Catalog</span></span>      | <span data-ttu-id="6b5ce-211">Faux</span><span class="sxs-lookup"><span data-stu-id="6b5ce-211">False</span></span>                                        |
| <span data-ttu-id="6b5ce-212">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="6b5ce-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="6b5ce-213">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="6b5ce-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="6b5ce-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6b5ce-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="6b5ce-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6b5ce-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="6b5ce-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6b5ce-216">Search-Flags</span></span>           | <span data-ttu-id="6b5ce-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6b5ce-217">0x00000000</span></span>                                   |
| <span data-ttu-id="6b5ce-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6b5ce-218">System-Flags</span></span>           | <span data-ttu-id="6b5ce-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6b5ce-219">0x00000010</span></span>                                   |
| <span data-ttu-id="6b5ce-220">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="6b5ce-220">Classes used in</span></span>        | [<span data-ttu-id="6b5ce-221">**ACS-stratégie**</span><span class="sxs-lookup"><span data-stu-id="6b5ce-221">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6b5ce-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6b5ce-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6b5ce-223">Entrée</span><span class="sxs-lookup"><span data-stu-id="6b5ce-223">Entry</span></span> | <span data-ttu-id="6b5ce-224">Valeur</span><span class="sxs-lookup"><span data-stu-id="6b5ce-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="6b5ce-225">ID de lien</span><span class="sxs-lookup"><span data-stu-id="6b5ce-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="6b5ce-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6b5ce-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="6b5ce-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="6b5ce-227">System-Only</span></span>            | <span data-ttu-id="6b5ce-228">Faux</span><span class="sxs-lookup"><span data-stu-id="6b5ce-228">False</span></span>                                        |
| <span data-ttu-id="6b5ce-229">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="6b5ce-229">Is-Single-Valued</span></span>       | <span data-ttu-id="6b5ce-230">Faux</span><span class="sxs-lookup"><span data-stu-id="6b5ce-230">False</span></span>                                        |
| <span data-ttu-id="6b5ce-231">Est indexé</span><span class="sxs-lookup"><span data-stu-id="6b5ce-231">Is Indexed</span></span>             | <span data-ttu-id="6b5ce-232">Faux</span><span class="sxs-lookup"><span data-stu-id="6b5ce-232">False</span></span>                                        |
| <span data-ttu-id="6b5ce-233">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="6b5ce-233">In Global Catalog</span></span>      | <span data-ttu-id="6b5ce-234">Faux</span><span class="sxs-lookup"><span data-stu-id="6b5ce-234">False</span></span>                                        |
| <span data-ttu-id="6b5ce-235">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="6b5ce-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="6b5ce-236">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="6b5ce-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="6b5ce-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6b5ce-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="6b5ce-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6b5ce-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="6b5ce-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6b5ce-239">Search-Flags</span></span>           | <span data-ttu-id="6b5ce-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6b5ce-240">0x00000000</span></span>                                   |
| <span data-ttu-id="6b5ce-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6b5ce-241">System-Flags</span></span>           | <span data-ttu-id="6b5ce-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6b5ce-242">0x00000010</span></span>                                   |
| <span data-ttu-id="6b5ce-243">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="6b5ce-243">Classes used in</span></span>        | [<span data-ttu-id="6b5ce-244">**ACS-stratégie**</span><span class="sxs-lookup"><span data-stu-id="6b5ce-244">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6b5ce-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6b5ce-245">Windows Server 2012</span></span>



| <span data-ttu-id="6b5ce-246">Entrée</span><span class="sxs-lookup"><span data-stu-id="6b5ce-246">Entry</span></span> | <span data-ttu-id="6b5ce-247">Valeur</span><span class="sxs-lookup"><span data-stu-id="6b5ce-247">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="6b5ce-248">ID de lien</span><span class="sxs-lookup"><span data-stu-id="6b5ce-248">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="6b5ce-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6b5ce-249">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="6b5ce-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="6b5ce-250">System-Only</span></span>            | <span data-ttu-id="6b5ce-251">Faux</span><span class="sxs-lookup"><span data-stu-id="6b5ce-251">False</span></span>                                        |
| <span data-ttu-id="6b5ce-252">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="6b5ce-252">Is-Single-Valued</span></span>       | <span data-ttu-id="6b5ce-253">Faux</span><span class="sxs-lookup"><span data-stu-id="6b5ce-253">False</span></span>                                        |
| <span data-ttu-id="6b5ce-254">Est indexé</span><span class="sxs-lookup"><span data-stu-id="6b5ce-254">Is Indexed</span></span>             | <span data-ttu-id="6b5ce-255">Faux</span><span class="sxs-lookup"><span data-stu-id="6b5ce-255">False</span></span>                                        |
| <span data-ttu-id="6b5ce-256">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="6b5ce-256">In Global Catalog</span></span>      | <span data-ttu-id="6b5ce-257">Faux</span><span class="sxs-lookup"><span data-stu-id="6b5ce-257">False</span></span>                                        |
| <span data-ttu-id="6b5ce-258">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="6b5ce-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="6b5ce-259">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="6b5ce-259">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="6b5ce-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6b5ce-260">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="6b5ce-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6b5ce-261">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="6b5ce-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6b5ce-262">Search-Flags</span></span>           | <span data-ttu-id="6b5ce-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6b5ce-263">0x00000000</span></span>                                   |
| <span data-ttu-id="6b5ce-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6b5ce-264">System-Flags</span></span>           | <span data-ttu-id="6b5ce-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6b5ce-265">0x00000010</span></span>                                   |
| <span data-ttu-id="6b5ce-266">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="6b5ce-266">Classes used in</span></span>        | [<span data-ttu-id="6b5ce-267">**ACS-stratégie**</span><span class="sxs-lookup"><span data-stu-id="6b5ce-267">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



 

 





