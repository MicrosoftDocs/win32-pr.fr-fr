---
title: Attribut Supplemental-Credentials
description: Informations d’identification stockées pour une utilisation lors de l’authentification. Version chiffrée du mot de passe de l’utilisateur. Cet attribut n’est ni lisible ni accessible en écriture.
ms.assetid: 642aa699-094e-40ed-a2f8-ec7219c85de2
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Supplemental-Credentials
- Schéma AD de l’attribut supplementalCredentials
topic_type:
- apiref
api_name:
- Supplemental-Credentials
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e19a73b3ae3cf19745fc995a59c336b72d264e78
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104519657"
---
# <a name="supplemental-credentials-attribute"></a><span data-ttu-id="9a04d-107">Attribut Supplemental-Credentials</span><span class="sxs-lookup"><span data-stu-id="9a04d-107">Supplemental-Credentials attribute</span></span>

<span data-ttu-id="9a04d-108">Informations d’identification stockées pour une utilisation lors de l’authentification.</span><span class="sxs-lookup"><span data-stu-id="9a04d-108">Stored credentials for use in authenticating.</span></span> <span data-ttu-id="9a04d-109">Version chiffrée du mot de passe de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9a04d-109">The encrypted version of the user's password.</span></span> <span data-ttu-id="9a04d-110">Cet attribut n’est ni lisible ni accessible en écriture.</span><span class="sxs-lookup"><span data-stu-id="9a04d-110">This attribute is neither readable nor writable.</span></span>



| <span data-ttu-id="9a04d-111">Entrée</span><span class="sxs-lookup"><span data-stu-id="9a04d-111">Entry</span></span> | <span data-ttu-id="9a04d-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="9a04d-112">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="9a04d-113">CN</span><span class="sxs-lookup"><span data-stu-id="9a04d-113">CN</span></span>                | <span data-ttu-id="9a04d-114">Supplemental-Credentials</span><span class="sxs-lookup"><span data-stu-id="9a04d-114">Supplemental-Credentials</span></span>                              |
| <span data-ttu-id="9a04d-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="9a04d-115">Ldap-Display-Name</span></span> | <span data-ttu-id="9a04d-116">supplementalCredentials</span><span class="sxs-lookup"><span data-stu-id="9a04d-116">supplementalCredentials</span></span>                               |
| <span data-ttu-id="9a04d-117">Taille</span><span class="sxs-lookup"><span data-stu-id="9a04d-117">Size</span></span>              | \-                                                    |
| <span data-ttu-id="9a04d-118">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="9a04d-118">Update Privilege</span></span>  | <span data-ttu-id="9a04d-119">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="9a04d-119">This value is set by the system.</span></span>                      |
| <span data-ttu-id="9a04d-120">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="9a04d-120">Update Frequency</span></span>  | <span data-ttu-id="9a04d-121">Lorsque le mot de passe de l’utilisateur change.</span><span class="sxs-lookup"><span data-stu-id="9a04d-121">When the user's password changes.</span></span>                     |
| <span data-ttu-id="9a04d-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9a04d-122">Attribute-Id</span></span>      | <span data-ttu-id="9a04d-123">1.2.840.113556.1.4.125</span><span class="sxs-lookup"><span data-stu-id="9a04d-123">1.2.840.113556.1.4.125</span></span>                                |
| <span data-ttu-id="9a04d-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="9a04d-124">System-Id-Guid</span></span>    | <span data-ttu-id="9a04d-125">bf967a3f-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="9a04d-125">bf967a3f-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="9a04d-126">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9a04d-126">Syntax</span></span>            | [<span data-ttu-id="9a04d-127">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="9a04d-127">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="9a04d-128">Implémentations</span><span class="sxs-lookup"><span data-stu-id="9a04d-128">Implementations</span></span>

-   [<span data-ttu-id="9a04d-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="9a04d-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="9a04d-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9a04d-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9a04d-131">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="9a04d-131">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="9a04d-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9a04d-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9a04d-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9a04d-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9a04d-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9a04d-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9a04d-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9a04d-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="9a04d-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9a04d-136">Windows 2000 Server</span></span>



| <span data-ttu-id="9a04d-137">Entrée</span><span class="sxs-lookup"><span data-stu-id="9a04d-137">Entry</span></span> | <span data-ttu-id="9a04d-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="9a04d-138">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="9a04d-139">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9a04d-139">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="9a04d-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9a04d-140">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="9a04d-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="9a04d-141">System-Only</span></span>            | <span data-ttu-id="9a04d-142">Faux</span><span class="sxs-lookup"><span data-stu-id="9a04d-142">False</span></span>                                                        |
| <span data-ttu-id="9a04d-143">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9a04d-143">Is-Single-Valued</span></span>       | <span data-ttu-id="9a04d-144">Faux</span><span class="sxs-lookup"><span data-stu-id="9a04d-144">False</span></span>                                                        |
| <span data-ttu-id="9a04d-145">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9a04d-145">Is Indexed</span></span>             | <span data-ttu-id="9a04d-146">Faux</span><span class="sxs-lookup"><span data-stu-id="9a04d-146">False</span></span>                                                        |
| <span data-ttu-id="9a04d-147">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9a04d-147">In Global Catalog</span></span>      | <span data-ttu-id="9a04d-148">Faux</span><span class="sxs-lookup"><span data-stu-id="9a04d-148">False</span></span>                                                        |
| <span data-ttu-id="9a04d-149">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9a04d-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="9a04d-150">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9a04d-150">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="9a04d-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9a04d-151">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="9a04d-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9a04d-152">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="9a04d-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9a04d-153">Search-Flags</span></span>           | <span data-ttu-id="9a04d-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9a04d-154">0x00000000</span></span>                                                   |
| <span data-ttu-id="9a04d-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9a04d-155">System-Flags</span></span>           | <span data-ttu-id="9a04d-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9a04d-156">0x00000010</span></span>                                                   |
| <span data-ttu-id="9a04d-157">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9a04d-157">Classes used in</span></span>        | [<span data-ttu-id="9a04d-158">**Sécurité-principal**</span><span class="sxs-lookup"><span data-stu-id="9a04d-158">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="9a04d-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9a04d-159">Windows Server 2003</span></span>



| <span data-ttu-id="9a04d-160">Entrée</span><span class="sxs-lookup"><span data-stu-id="9a04d-160">Entry</span></span> | <span data-ttu-id="9a04d-161">Valeur</span><span class="sxs-lookup"><span data-stu-id="9a04d-161">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="9a04d-162">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9a04d-162">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="9a04d-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9a04d-163">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="9a04d-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="9a04d-164">System-Only</span></span>            | <span data-ttu-id="9a04d-165">Faux</span><span class="sxs-lookup"><span data-stu-id="9a04d-165">False</span></span>                                                        |
| <span data-ttu-id="9a04d-166">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9a04d-166">Is-Single-Valued</span></span>       | <span data-ttu-id="9a04d-167">Faux</span><span class="sxs-lookup"><span data-stu-id="9a04d-167">False</span></span>                                                        |
| <span data-ttu-id="9a04d-168">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9a04d-168">Is Indexed</span></span>             | <span data-ttu-id="9a04d-169">Faux</span><span class="sxs-lookup"><span data-stu-id="9a04d-169">False</span></span>                                                        |
| <span data-ttu-id="9a04d-170">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9a04d-170">In Global Catalog</span></span>      | <span data-ttu-id="9a04d-171">Faux</span><span class="sxs-lookup"><span data-stu-id="9a04d-171">False</span></span>                                                        |
| <span data-ttu-id="9a04d-172">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9a04d-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="9a04d-173">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9a04d-173">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="9a04d-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9a04d-174">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="9a04d-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9a04d-175">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="9a04d-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9a04d-176">Search-Flags</span></span>           | <span data-ttu-id="9a04d-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9a04d-177">0x00000000</span></span>                                                   |
| <span data-ttu-id="9a04d-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9a04d-178">System-Flags</span></span>           | <span data-ttu-id="9a04d-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9a04d-179">0x00000010</span></span>                                                   |
| <span data-ttu-id="9a04d-180">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9a04d-180">Classes used in</span></span>        | [<span data-ttu-id="9a04d-181">**Sécurité-principal**</span><span class="sxs-lookup"><span data-stu-id="9a04d-181">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="adam"></a><span data-ttu-id="9a04d-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="9a04d-182">ADAM</span></span>



| <span data-ttu-id="9a04d-183">Entrée</span><span class="sxs-lookup"><span data-stu-id="9a04d-183">Entry</span></span> | <span data-ttu-id="9a04d-184">Valeur</span><span class="sxs-lookup"><span data-stu-id="9a04d-184">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="9a04d-185">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9a04d-185">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="9a04d-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9a04d-186">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="9a04d-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="9a04d-187">System-Only</span></span>            | <span data-ttu-id="9a04d-188">Faux</span><span class="sxs-lookup"><span data-stu-id="9a04d-188">False</span></span>                                                        |
| <span data-ttu-id="9a04d-189">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9a04d-189">Is-Single-Valued</span></span>       | <span data-ttu-id="9a04d-190">Faux</span><span class="sxs-lookup"><span data-stu-id="9a04d-190">False</span></span>                                                        |
| <span data-ttu-id="9a04d-191">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9a04d-191">Is Indexed</span></span>             | <span data-ttu-id="9a04d-192">Faux</span><span class="sxs-lookup"><span data-stu-id="9a04d-192">False</span></span>                                                        |
| <span data-ttu-id="9a04d-193">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9a04d-193">In Global Catalog</span></span>      | <span data-ttu-id="9a04d-194">Faux</span><span class="sxs-lookup"><span data-stu-id="9a04d-194">False</span></span>                                                        |
| <span data-ttu-id="9a04d-195">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9a04d-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="9a04d-196">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9a04d-196">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="9a04d-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9a04d-197">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="9a04d-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9a04d-198">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="9a04d-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9a04d-199">Search-Flags</span></span>           | <span data-ttu-id="9a04d-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9a04d-200">0x00000000</span></span>                                                   |
| <span data-ttu-id="9a04d-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9a04d-201">System-Flags</span></span>           | <span data-ttu-id="9a04d-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9a04d-202">0x00000010</span></span>                                                   |
| <span data-ttu-id="9a04d-203">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9a04d-203">Classes used in</span></span>        | [<span data-ttu-id="9a04d-204">**Sécurité-principal**</span><span class="sxs-lookup"><span data-stu-id="9a04d-204">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9a04d-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9a04d-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9a04d-206">Entrée</span><span class="sxs-lookup"><span data-stu-id="9a04d-206">Entry</span></span> | <span data-ttu-id="9a04d-207">Valeur</span><span class="sxs-lookup"><span data-stu-id="9a04d-207">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="9a04d-208">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9a04d-208">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="9a04d-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9a04d-209">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="9a04d-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="9a04d-210">System-Only</span></span>            | <span data-ttu-id="9a04d-211">Faux</span><span class="sxs-lookup"><span data-stu-id="9a04d-211">False</span></span>                                                        |
| <span data-ttu-id="9a04d-212">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9a04d-212">Is-Single-Valued</span></span>       | <span data-ttu-id="9a04d-213">Faux</span><span class="sxs-lookup"><span data-stu-id="9a04d-213">False</span></span>                                                        |
| <span data-ttu-id="9a04d-214">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9a04d-214">Is Indexed</span></span>             | <span data-ttu-id="9a04d-215">Faux</span><span class="sxs-lookup"><span data-stu-id="9a04d-215">False</span></span>                                                        |
| <span data-ttu-id="9a04d-216">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9a04d-216">In Global Catalog</span></span>      | <span data-ttu-id="9a04d-217">Faux</span><span class="sxs-lookup"><span data-stu-id="9a04d-217">False</span></span>                                                        |
| <span data-ttu-id="9a04d-218">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9a04d-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="9a04d-219">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9a04d-219">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="9a04d-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9a04d-220">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="9a04d-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9a04d-221">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="9a04d-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9a04d-222">Search-Flags</span></span>           | <span data-ttu-id="9a04d-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9a04d-223">0x00000000</span></span>                                                   |
| <span data-ttu-id="9a04d-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9a04d-224">System-Flags</span></span>           | <span data-ttu-id="9a04d-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9a04d-225">0x00000010</span></span>                                                   |
| <span data-ttu-id="9a04d-226">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9a04d-226">Classes used in</span></span>        | [<span data-ttu-id="9a04d-227">**Sécurité-principal**</span><span class="sxs-lookup"><span data-stu-id="9a04d-227">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9a04d-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9a04d-228">Windows Server 2008</span></span>



| <span data-ttu-id="9a04d-229">Entrée</span><span class="sxs-lookup"><span data-stu-id="9a04d-229">Entry</span></span> | <span data-ttu-id="9a04d-230">Valeur</span><span class="sxs-lookup"><span data-stu-id="9a04d-230">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="9a04d-231">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9a04d-231">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="9a04d-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9a04d-232">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="9a04d-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="9a04d-233">System-Only</span></span>            | <span data-ttu-id="9a04d-234">Faux</span><span class="sxs-lookup"><span data-stu-id="9a04d-234">False</span></span>                                                        |
| <span data-ttu-id="9a04d-235">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9a04d-235">Is-Single-Valued</span></span>       | <span data-ttu-id="9a04d-236">Faux</span><span class="sxs-lookup"><span data-stu-id="9a04d-236">False</span></span>                                                        |
| <span data-ttu-id="9a04d-237">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9a04d-237">Is Indexed</span></span>             | <span data-ttu-id="9a04d-238">Faux</span><span class="sxs-lookup"><span data-stu-id="9a04d-238">False</span></span>                                                        |
| <span data-ttu-id="9a04d-239">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9a04d-239">In Global Catalog</span></span>      | <span data-ttu-id="9a04d-240">Faux</span><span class="sxs-lookup"><span data-stu-id="9a04d-240">False</span></span>                                                        |
| <span data-ttu-id="9a04d-241">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9a04d-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="9a04d-242">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9a04d-242">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="9a04d-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9a04d-243">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="9a04d-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9a04d-244">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="9a04d-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9a04d-245">Search-Flags</span></span>           | <span data-ttu-id="9a04d-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9a04d-246">0x00000000</span></span>                                                   |
| <span data-ttu-id="9a04d-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9a04d-247">System-Flags</span></span>           | <span data-ttu-id="9a04d-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9a04d-248">0x00000010</span></span>                                                   |
| <span data-ttu-id="9a04d-249">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9a04d-249">Classes used in</span></span>        | [<span data-ttu-id="9a04d-250">**Sécurité-principal**</span><span class="sxs-lookup"><span data-stu-id="9a04d-250">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9a04d-251">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9a04d-251">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9a04d-252">Entrée</span><span class="sxs-lookup"><span data-stu-id="9a04d-252">Entry</span></span> | <span data-ttu-id="9a04d-253">Valeur</span><span class="sxs-lookup"><span data-stu-id="9a04d-253">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="9a04d-254">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9a04d-254">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="9a04d-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9a04d-255">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="9a04d-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="9a04d-256">System-Only</span></span>            | <span data-ttu-id="9a04d-257">Faux</span><span class="sxs-lookup"><span data-stu-id="9a04d-257">False</span></span>                                                        |
| <span data-ttu-id="9a04d-258">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9a04d-258">Is-Single-Valued</span></span>       | <span data-ttu-id="9a04d-259">Faux</span><span class="sxs-lookup"><span data-stu-id="9a04d-259">False</span></span>                                                        |
| <span data-ttu-id="9a04d-260">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9a04d-260">Is Indexed</span></span>             | <span data-ttu-id="9a04d-261">Faux</span><span class="sxs-lookup"><span data-stu-id="9a04d-261">False</span></span>                                                        |
| <span data-ttu-id="9a04d-262">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9a04d-262">In Global Catalog</span></span>      | <span data-ttu-id="9a04d-263">Faux</span><span class="sxs-lookup"><span data-stu-id="9a04d-263">False</span></span>                                                        |
| <span data-ttu-id="9a04d-264">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9a04d-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="9a04d-265">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9a04d-265">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="9a04d-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9a04d-266">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="9a04d-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9a04d-267">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="9a04d-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9a04d-268">Search-Flags</span></span>           | <span data-ttu-id="9a04d-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9a04d-269">0x00000000</span></span>                                                   |
| <span data-ttu-id="9a04d-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9a04d-270">System-Flags</span></span>           | <span data-ttu-id="9a04d-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9a04d-271">0x00000010</span></span>                                                   |
| <span data-ttu-id="9a04d-272">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9a04d-272">Classes used in</span></span>        | [<span data-ttu-id="9a04d-273">**Sécurité-principal**</span><span class="sxs-lookup"><span data-stu-id="9a04d-273">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9a04d-274">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9a04d-274">Windows Server 2012</span></span>



| <span data-ttu-id="9a04d-275">Entrée</span><span class="sxs-lookup"><span data-stu-id="9a04d-275">Entry</span></span> | <span data-ttu-id="9a04d-276">Valeur</span><span class="sxs-lookup"><span data-stu-id="9a04d-276">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="9a04d-277">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9a04d-277">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="9a04d-278">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9a04d-278">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="9a04d-279">System-Only</span><span class="sxs-lookup"><span data-stu-id="9a04d-279">System-Only</span></span>            | <span data-ttu-id="9a04d-280">Faux</span><span class="sxs-lookup"><span data-stu-id="9a04d-280">False</span></span>                                                        |
| <span data-ttu-id="9a04d-281">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9a04d-281">Is-Single-Valued</span></span>       | <span data-ttu-id="9a04d-282">Faux</span><span class="sxs-lookup"><span data-stu-id="9a04d-282">False</span></span>                                                        |
| <span data-ttu-id="9a04d-283">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9a04d-283">Is Indexed</span></span>             | <span data-ttu-id="9a04d-284">Faux</span><span class="sxs-lookup"><span data-stu-id="9a04d-284">False</span></span>                                                        |
| <span data-ttu-id="9a04d-285">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9a04d-285">In Global Catalog</span></span>      | <span data-ttu-id="9a04d-286">Faux</span><span class="sxs-lookup"><span data-stu-id="9a04d-286">False</span></span>                                                        |
| <span data-ttu-id="9a04d-287">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9a04d-287">NT-Security-Descriptor</span></span> | <span data-ttu-id="9a04d-288">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9a04d-288">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="9a04d-289">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9a04d-289">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="9a04d-290">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9a04d-290">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="9a04d-291">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9a04d-291">Search-Flags</span></span>           | <span data-ttu-id="9a04d-292">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9a04d-292">0x00000000</span></span>                                                   |
| <span data-ttu-id="9a04d-293">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9a04d-293">System-Flags</span></span>           | <span data-ttu-id="9a04d-294">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9a04d-294">0x00000010</span></span>                                                   |
| <span data-ttu-id="9a04d-295">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9a04d-295">Classes used in</span></span>        | [<span data-ttu-id="9a04d-296">**Sécurité-principal**</span><span class="sxs-lookup"><span data-stu-id="9a04d-296">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



 

 





