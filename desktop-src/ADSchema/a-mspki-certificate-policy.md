---
title: attribut ms-PKI-Certificate-Policy
description: Contient la liste des OID de stratégie et leurs CSP facultatifs dans le certificat émis.
ms.assetid: bc84c5ff-9cb1-406c-825c-97fa479d52eb
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut ms-PKI-Certificate-Policy
- Schéma AD de l’attribut de stratégie de certificat attribut mspki
topic_type:
- apiref
api_name:
- ms-PKI-Certificate-Policy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d2d6857b6035cc72271c7276b679b8a497aaab9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845066"
---
# <a name="ms-pki-certificate-policy-attribute"></a><span data-ttu-id="62653-105">attribut ms-PKI-Certificate-Policy</span><span class="sxs-lookup"><span data-stu-id="62653-105">ms-PKI-Certificate-Policy attribute</span></span>

<span data-ttu-id="62653-106">Contient la liste des OID de stratégie et leurs CSP facultatifs dans le certificat émis.</span><span class="sxs-lookup"><span data-stu-id="62653-106">Contains the list of policy OIDs and their optional CSPs in the issued certificate.</span></span>



| <span data-ttu-id="62653-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="62653-107">Entry</span></span> | <span data-ttu-id="62653-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="62653-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62653-109">CN</span><span class="sxs-lookup"><span data-stu-id="62653-109">CN</span></span>                | <span data-ttu-id="62653-110">MS-PKI-certificat-stratégie</span><span class="sxs-lookup"><span data-stu-id="62653-110">ms-PKI-Certificate-Policy</span></span>                                                                         |
| <span data-ttu-id="62653-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="62653-111">Ldap-Display-Name</span></span> | <span data-ttu-id="62653-112">Attribut mspki-certificat-Policy</span><span class="sxs-lookup"><span data-stu-id="62653-112">msPKI-Certificate-Policy</span></span>                                                                          |
| <span data-ttu-id="62653-113">Taille</span><span class="sxs-lookup"><span data-stu-id="62653-113">Size</span></span>              | <span data-ttu-id="62653-114">64 octets multiplié par le nombre d’entrées.</span><span class="sxs-lookup"><span data-stu-id="62653-114">64 bytes times the number of entries.</span></span>                                                             |
| <span data-ttu-id="62653-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="62653-115">Update Privilege</span></span>  | <span data-ttu-id="62653-116">Administrateur de domaine</span><span class="sxs-lookup"><span data-stu-id="62653-116">Domain administrator</span></span>                                                                              |
| <span data-ttu-id="62653-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="62653-117">Update Frequency</span></span>  | <span data-ttu-id="62653-118">Lorsque l’objet modèle de certificat (MS-PKI-Certificate-template) est modifié, créé ou cloné.</span><span class="sxs-lookup"><span data-stu-id="62653-118">When the certificate template (ms-PKI-Certificate-Template) object is edited, created, or cloned.</span></span> |
| <span data-ttu-id="62653-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="62653-119">Attribute-Id</span></span>      | <span data-ttu-id="62653-120">1.2.840.113556.1.4.1439</span><span class="sxs-lookup"><span data-stu-id="62653-120">1.2.840.113556.1.4.1439</span></span>                                                                           |
| <span data-ttu-id="62653-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="62653-121">System-Id-Guid</span></span>    | <span data-ttu-id="62653-122">38942346-cc5b-424B-a7d8-6ffd12029c5f</span><span class="sxs-lookup"><span data-stu-id="62653-122">38942346-cc5b-424b-a7d8-6ffd12029c5f</span></span>                                                              |
| <span data-ttu-id="62653-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="62653-123">Syntax</span></span>            | [<span data-ttu-id="62653-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="62653-124">**String(Unicode)**</span></span>](s-string-unicode.md)                                                       |



## <a name="implementations"></a><span data-ttu-id="62653-125">Implémentations</span><span class="sxs-lookup"><span data-stu-id="62653-125">Implementations</span></span>

-   [<span data-ttu-id="62653-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="62653-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="62653-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="62653-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="62653-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="62653-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="62653-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="62653-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="62653-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="62653-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="62653-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="62653-131">Windows Server 2003</span></span>



| <span data-ttu-id="62653-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="62653-132">Entry</span></span> | <span data-ttu-id="62653-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="62653-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="62653-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="62653-134">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="62653-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="62653-135">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="62653-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="62653-136">System-Only</span></span>            | <span data-ttu-id="62653-137">Faux</span><span class="sxs-lookup"><span data-stu-id="62653-137">False</span></span>                                                                   |
| <span data-ttu-id="62653-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="62653-138">Is-Single-Valued</span></span>       | <span data-ttu-id="62653-139">Faux</span><span class="sxs-lookup"><span data-stu-id="62653-139">False</span></span>                                                                   |
| <span data-ttu-id="62653-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="62653-140">Is Indexed</span></span>             | <span data-ttu-id="62653-141">Faux</span><span class="sxs-lookup"><span data-stu-id="62653-141">False</span></span>                                                                   |
| <span data-ttu-id="62653-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="62653-142">In Global Catalog</span></span>      | <span data-ttu-id="62653-143">Faux</span><span class="sxs-lookup"><span data-stu-id="62653-143">False</span></span>                                                                   |
| <span data-ttu-id="62653-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="62653-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="62653-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="62653-145">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="62653-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="62653-146">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="62653-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="62653-147">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="62653-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="62653-148">Search-Flags</span></span>           | <span data-ttu-id="62653-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="62653-149">0x00000000</span></span>                                                              |
| <span data-ttu-id="62653-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="62653-150">System-Flags</span></span>           | <span data-ttu-id="62653-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="62653-151">0x00000010</span></span>                                                              |
| <span data-ttu-id="62653-152">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="62653-152">Classes used in</span></span>        | [<span data-ttu-id="62653-153">**PKI-Certificate-modèle**</span><span class="sxs-lookup"><span data-stu-id="62653-153">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="62653-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="62653-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="62653-155">Entrée</span><span class="sxs-lookup"><span data-stu-id="62653-155">Entry</span></span> | <span data-ttu-id="62653-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="62653-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="62653-157">ID de lien</span><span class="sxs-lookup"><span data-stu-id="62653-157">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="62653-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="62653-158">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="62653-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="62653-159">System-Only</span></span>            | <span data-ttu-id="62653-160">Faux</span><span class="sxs-lookup"><span data-stu-id="62653-160">False</span></span>                                                                   |
| <span data-ttu-id="62653-161">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="62653-161">Is-Single-Valued</span></span>       | <span data-ttu-id="62653-162">Faux</span><span class="sxs-lookup"><span data-stu-id="62653-162">False</span></span>                                                                   |
| <span data-ttu-id="62653-163">Est indexé</span><span class="sxs-lookup"><span data-stu-id="62653-163">Is Indexed</span></span>             | <span data-ttu-id="62653-164">Faux</span><span class="sxs-lookup"><span data-stu-id="62653-164">False</span></span>                                                                   |
| <span data-ttu-id="62653-165">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="62653-165">In Global Catalog</span></span>      | <span data-ttu-id="62653-166">Faux</span><span class="sxs-lookup"><span data-stu-id="62653-166">False</span></span>                                                                   |
| <span data-ttu-id="62653-167">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="62653-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="62653-168">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="62653-168">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="62653-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="62653-169">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="62653-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="62653-170">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="62653-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="62653-171">Search-Flags</span></span>           | <span data-ttu-id="62653-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="62653-172">0x00000000</span></span>                                                              |
| <span data-ttu-id="62653-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="62653-173">System-Flags</span></span>           | <span data-ttu-id="62653-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="62653-174">0x00000010</span></span>                                                              |
| <span data-ttu-id="62653-175">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="62653-175">Classes used in</span></span>        | [<span data-ttu-id="62653-176">**PKI-Certificate-modèle**</span><span class="sxs-lookup"><span data-stu-id="62653-176">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="62653-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="62653-177">Windows Server 2008</span></span>



| <span data-ttu-id="62653-178">Entrée</span><span class="sxs-lookup"><span data-stu-id="62653-178">Entry</span></span> | <span data-ttu-id="62653-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="62653-179">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="62653-180">ID de lien</span><span class="sxs-lookup"><span data-stu-id="62653-180">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="62653-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="62653-181">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="62653-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="62653-182">System-Only</span></span>            | <span data-ttu-id="62653-183">Faux</span><span class="sxs-lookup"><span data-stu-id="62653-183">False</span></span>                                                                   |
| <span data-ttu-id="62653-184">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="62653-184">Is-Single-Valued</span></span>       | <span data-ttu-id="62653-185">Faux</span><span class="sxs-lookup"><span data-stu-id="62653-185">False</span></span>                                                                   |
| <span data-ttu-id="62653-186">Est indexé</span><span class="sxs-lookup"><span data-stu-id="62653-186">Is Indexed</span></span>             | <span data-ttu-id="62653-187">Faux</span><span class="sxs-lookup"><span data-stu-id="62653-187">False</span></span>                                                                   |
| <span data-ttu-id="62653-188">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="62653-188">In Global Catalog</span></span>      | <span data-ttu-id="62653-189">Faux</span><span class="sxs-lookup"><span data-stu-id="62653-189">False</span></span>                                                                   |
| <span data-ttu-id="62653-190">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="62653-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="62653-191">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="62653-191">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="62653-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="62653-192">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="62653-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="62653-193">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="62653-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="62653-194">Search-Flags</span></span>           | <span data-ttu-id="62653-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="62653-195">0x00000000</span></span>                                                              |
| <span data-ttu-id="62653-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="62653-196">System-Flags</span></span>           | <span data-ttu-id="62653-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="62653-197">0x00000010</span></span>                                                              |
| <span data-ttu-id="62653-198">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="62653-198">Classes used in</span></span>        | [<span data-ttu-id="62653-199">**PKI-Certificate-modèle**</span><span class="sxs-lookup"><span data-stu-id="62653-199">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="62653-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="62653-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="62653-201">Entrée</span><span class="sxs-lookup"><span data-stu-id="62653-201">Entry</span></span> | <span data-ttu-id="62653-202">Valeur</span><span class="sxs-lookup"><span data-stu-id="62653-202">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="62653-203">ID de lien</span><span class="sxs-lookup"><span data-stu-id="62653-203">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="62653-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="62653-204">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="62653-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="62653-205">System-Only</span></span>            | <span data-ttu-id="62653-206">Faux</span><span class="sxs-lookup"><span data-stu-id="62653-206">False</span></span>                                                                   |
| <span data-ttu-id="62653-207">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="62653-207">Is-Single-Valued</span></span>       | <span data-ttu-id="62653-208">Faux</span><span class="sxs-lookup"><span data-stu-id="62653-208">False</span></span>                                                                   |
| <span data-ttu-id="62653-209">Est indexé</span><span class="sxs-lookup"><span data-stu-id="62653-209">Is Indexed</span></span>             | <span data-ttu-id="62653-210">Faux</span><span class="sxs-lookup"><span data-stu-id="62653-210">False</span></span>                                                                   |
| <span data-ttu-id="62653-211">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="62653-211">In Global Catalog</span></span>      | <span data-ttu-id="62653-212">Faux</span><span class="sxs-lookup"><span data-stu-id="62653-212">False</span></span>                                                                   |
| <span data-ttu-id="62653-213">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="62653-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="62653-214">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="62653-214">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="62653-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="62653-215">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="62653-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="62653-216">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="62653-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="62653-217">Search-Flags</span></span>           | <span data-ttu-id="62653-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="62653-218">0x00000000</span></span>                                                              |
| <span data-ttu-id="62653-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="62653-219">System-Flags</span></span>           | <span data-ttu-id="62653-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="62653-220">0x00000010</span></span>                                                              |
| <span data-ttu-id="62653-221">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="62653-221">Classes used in</span></span>        | [<span data-ttu-id="62653-222">**PKI-Certificate-modèle**</span><span class="sxs-lookup"><span data-stu-id="62653-222">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="62653-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="62653-223">Windows Server 2012</span></span>



| <span data-ttu-id="62653-224">Entrée</span><span class="sxs-lookup"><span data-stu-id="62653-224">Entry</span></span> | <span data-ttu-id="62653-225">Valeur</span><span class="sxs-lookup"><span data-stu-id="62653-225">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="62653-226">ID de lien</span><span class="sxs-lookup"><span data-stu-id="62653-226">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="62653-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="62653-227">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="62653-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="62653-228">System-Only</span></span>            | <span data-ttu-id="62653-229">Faux</span><span class="sxs-lookup"><span data-stu-id="62653-229">False</span></span>                                                                   |
| <span data-ttu-id="62653-230">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="62653-230">Is-Single-Valued</span></span>       | <span data-ttu-id="62653-231">Faux</span><span class="sxs-lookup"><span data-stu-id="62653-231">False</span></span>                                                                   |
| <span data-ttu-id="62653-232">Est indexé</span><span class="sxs-lookup"><span data-stu-id="62653-232">Is Indexed</span></span>             | <span data-ttu-id="62653-233">Faux</span><span class="sxs-lookup"><span data-stu-id="62653-233">False</span></span>                                                                   |
| <span data-ttu-id="62653-234">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="62653-234">In Global Catalog</span></span>      | <span data-ttu-id="62653-235">Faux</span><span class="sxs-lookup"><span data-stu-id="62653-235">False</span></span>                                                                   |
| <span data-ttu-id="62653-236">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="62653-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="62653-237">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="62653-237">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="62653-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="62653-238">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="62653-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="62653-239">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="62653-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="62653-240">Search-Flags</span></span>           | <span data-ttu-id="62653-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="62653-241">0x00000000</span></span>                                                              |
| <span data-ttu-id="62653-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="62653-242">System-Flags</span></span>           | <span data-ttu-id="62653-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="62653-243">0x00000010</span></span>                                                              |
| <span data-ttu-id="62653-244">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="62653-244">Classes used in</span></span>        | [<span data-ttu-id="62653-245">**PKI-Certificate-modèle**</span><span class="sxs-lookup"><span data-stu-id="62653-245">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 





