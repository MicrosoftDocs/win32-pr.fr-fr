---
title: MS-PKI-RA-attribut de signature
description: Spécifie le nombre de signatures de l’autorité d’inscription d’inscription requises dans une demande d’inscription.
ms.assetid: da9d9357-6826-4511-b589-594c73114713
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory MS-PKI-RA-signature Attribute
- Attribut mspki-RA-schéma AD d’attribut de signature
topic_type:
- apiref
api_name:
- ms-PKI-RA-Signature
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 170793e46095e16a62d8e025ec16b67bf2be7131
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106513065"
---
# <a name="ms-pki-ra-signature-attribute"></a><span data-ttu-id="6fb6c-105">MS-PKI-RA-attribut de signature</span><span class="sxs-lookup"><span data-stu-id="6fb6c-105">ms-PKI-RA-Signature attribute</span></span>

<span data-ttu-id="6fb6c-106">Spécifie le nombre de signatures de l’autorité d’inscription d’inscription requises dans une demande d’inscription.</span><span class="sxs-lookup"><span data-stu-id="6fb6c-106">Specifies the number of enrollment registration authority signatures that are required in an enrollment request.</span></span>



| <span data-ttu-id="6fb6c-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="6fb6c-107">Entry</span></span> | <span data-ttu-id="6fb6c-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="6fb6c-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fb6c-109">CN</span><span class="sxs-lookup"><span data-stu-id="6fb6c-109">CN</span></span>                | <span data-ttu-id="6fb6c-110">MS-PKI-RA-signature</span><span class="sxs-lookup"><span data-stu-id="6fb6c-110">ms-PKI-RA-Signature</span></span>                                                                               |
| <span data-ttu-id="6fb6c-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="6fb6c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="6fb6c-112">Attribut mspki-RA-signature</span><span class="sxs-lookup"><span data-stu-id="6fb6c-112">msPKI-RA-Signature</span></span>                                                                                |
| <span data-ttu-id="6fb6c-113">Taille</span><span class="sxs-lookup"><span data-stu-id="6fb6c-113">Size</span></span>              | <span data-ttu-id="6fb6c-114">4 octets</span><span class="sxs-lookup"><span data-stu-id="6fb6c-114">4 bytes</span></span>                                                                                           |
| <span data-ttu-id="6fb6c-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="6fb6c-115">Update Privilege</span></span>  | <span data-ttu-id="6fb6c-116">Administrateur de domaine</span><span class="sxs-lookup"><span data-stu-id="6fb6c-116">Domain administrator</span></span>                                                                              |
| <span data-ttu-id="6fb6c-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="6fb6c-117">Update Frequency</span></span>  | <span data-ttu-id="6fb6c-118">Lorsque l’objet modèle de certificat (MS-PKI-Certificate-template) est modifié, créé ou cloné.</span><span class="sxs-lookup"><span data-stu-id="6fb6c-118">When the certificate template (ms-PKI-Certificate-Template) object is edited, created, or cloned.</span></span> |
| <span data-ttu-id="6fb6c-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6fb6c-119">Attribute-Id</span></span>      | <span data-ttu-id="6fb6c-120">1.2.840.113556.1.4.1429</span><span class="sxs-lookup"><span data-stu-id="6fb6c-120">1.2.840.113556.1.4.1429</span></span>                                                                           |
| <span data-ttu-id="6fb6c-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="6fb6c-121">System-Id-Guid</span></span>    | <span data-ttu-id="6fb6c-122">fe17e04b-937d-4f7e-8e0e-9292c8d5683e</span><span class="sxs-lookup"><span data-stu-id="6fb6c-122">fe17e04b-937d-4f7e-8e0e-9292c8d5683e</span></span>                                                              |
| <span data-ttu-id="6fb6c-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6fb6c-123">Syntax</span></span>            | [<span data-ttu-id="6fb6c-124">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="6fb6c-124">**Enumeration**</span></span>](s-enumeration.md)                                                              |



## <a name="implementations"></a><span data-ttu-id="6fb6c-125">Implémentations</span><span class="sxs-lookup"><span data-stu-id="6fb6c-125">Implementations</span></span>

-   [<span data-ttu-id="6fb6c-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6fb6c-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6fb6c-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6fb6c-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6fb6c-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6fb6c-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6fb6c-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6fb6c-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6fb6c-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6fb6c-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="6fb6c-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6fb6c-131">Windows Server 2003</span></span>



| <span data-ttu-id="6fb6c-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="6fb6c-132">Entry</span></span> | <span data-ttu-id="6fb6c-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="6fb6c-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="6fb6c-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="6fb6c-134">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="6fb6c-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6fb6c-135">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="6fb6c-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="6fb6c-136">System-Only</span></span>            | <span data-ttu-id="6fb6c-137">Faux</span><span class="sxs-lookup"><span data-stu-id="6fb6c-137">False</span></span>                                                                   |
| <span data-ttu-id="6fb6c-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="6fb6c-138">Is-Single-Valued</span></span>       | <span data-ttu-id="6fb6c-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="6fb6c-139">True</span></span>                                                                    |
| <span data-ttu-id="6fb6c-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="6fb6c-140">Is Indexed</span></span>             | <span data-ttu-id="6fb6c-141">Faux</span><span class="sxs-lookup"><span data-stu-id="6fb6c-141">False</span></span>                                                                   |
| <span data-ttu-id="6fb6c-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="6fb6c-142">In Global Catalog</span></span>      | <span data-ttu-id="6fb6c-143">Faux</span><span class="sxs-lookup"><span data-stu-id="6fb6c-143">False</span></span>                                                                   |
| <span data-ttu-id="6fb6c-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="6fb6c-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="6fb6c-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="6fb6c-145">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="6fb6c-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6fb6c-146">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="6fb6c-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6fb6c-147">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="6fb6c-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6fb6c-148">Search-Flags</span></span>           | <span data-ttu-id="6fb6c-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6fb6c-149">0x00000000</span></span>                                                              |
| <span data-ttu-id="6fb6c-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6fb6c-150">System-Flags</span></span>           | <span data-ttu-id="6fb6c-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6fb6c-151">0x00000010</span></span>                                                              |
| <span data-ttu-id="6fb6c-152">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="6fb6c-152">Classes used in</span></span>        | [<span data-ttu-id="6fb6c-153">**PKI-Certificate-modèle**</span><span class="sxs-lookup"><span data-stu-id="6fb6c-153">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6fb6c-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6fb6c-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6fb6c-155">Entrée</span><span class="sxs-lookup"><span data-stu-id="6fb6c-155">Entry</span></span> | <span data-ttu-id="6fb6c-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="6fb6c-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="6fb6c-157">ID de lien</span><span class="sxs-lookup"><span data-stu-id="6fb6c-157">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="6fb6c-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6fb6c-158">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="6fb6c-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="6fb6c-159">System-Only</span></span>            | <span data-ttu-id="6fb6c-160">Faux</span><span class="sxs-lookup"><span data-stu-id="6fb6c-160">False</span></span>                                                                   |
| <span data-ttu-id="6fb6c-161">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="6fb6c-161">Is-Single-Valued</span></span>       | <span data-ttu-id="6fb6c-162">Vrai</span><span class="sxs-lookup"><span data-stu-id="6fb6c-162">True</span></span>                                                                    |
| <span data-ttu-id="6fb6c-163">Est indexé</span><span class="sxs-lookup"><span data-stu-id="6fb6c-163">Is Indexed</span></span>             | <span data-ttu-id="6fb6c-164">Faux</span><span class="sxs-lookup"><span data-stu-id="6fb6c-164">False</span></span>                                                                   |
| <span data-ttu-id="6fb6c-165">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="6fb6c-165">In Global Catalog</span></span>      | <span data-ttu-id="6fb6c-166">Faux</span><span class="sxs-lookup"><span data-stu-id="6fb6c-166">False</span></span>                                                                   |
| <span data-ttu-id="6fb6c-167">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="6fb6c-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="6fb6c-168">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="6fb6c-168">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="6fb6c-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6fb6c-169">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="6fb6c-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6fb6c-170">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="6fb6c-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6fb6c-171">Search-Flags</span></span>           | <span data-ttu-id="6fb6c-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6fb6c-172">0x00000000</span></span>                                                              |
| <span data-ttu-id="6fb6c-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6fb6c-173">System-Flags</span></span>           | <span data-ttu-id="6fb6c-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6fb6c-174">0x00000010</span></span>                                                              |
| <span data-ttu-id="6fb6c-175">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="6fb6c-175">Classes used in</span></span>        | [<span data-ttu-id="6fb6c-176">**PKI-Certificate-modèle**</span><span class="sxs-lookup"><span data-stu-id="6fb6c-176">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6fb6c-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6fb6c-177">Windows Server 2008</span></span>



| <span data-ttu-id="6fb6c-178">Entrée</span><span class="sxs-lookup"><span data-stu-id="6fb6c-178">Entry</span></span> | <span data-ttu-id="6fb6c-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="6fb6c-179">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="6fb6c-180">ID de lien</span><span class="sxs-lookup"><span data-stu-id="6fb6c-180">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="6fb6c-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6fb6c-181">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="6fb6c-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="6fb6c-182">System-Only</span></span>            | <span data-ttu-id="6fb6c-183">Faux</span><span class="sxs-lookup"><span data-stu-id="6fb6c-183">False</span></span>                                                                   |
| <span data-ttu-id="6fb6c-184">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="6fb6c-184">Is-Single-Valued</span></span>       | <span data-ttu-id="6fb6c-185">Vrai</span><span class="sxs-lookup"><span data-stu-id="6fb6c-185">True</span></span>                                                                    |
| <span data-ttu-id="6fb6c-186">Est indexé</span><span class="sxs-lookup"><span data-stu-id="6fb6c-186">Is Indexed</span></span>             | <span data-ttu-id="6fb6c-187">Faux</span><span class="sxs-lookup"><span data-stu-id="6fb6c-187">False</span></span>                                                                   |
| <span data-ttu-id="6fb6c-188">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="6fb6c-188">In Global Catalog</span></span>      | <span data-ttu-id="6fb6c-189">Faux</span><span class="sxs-lookup"><span data-stu-id="6fb6c-189">False</span></span>                                                                   |
| <span data-ttu-id="6fb6c-190">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="6fb6c-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="6fb6c-191">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="6fb6c-191">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="6fb6c-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6fb6c-192">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="6fb6c-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6fb6c-193">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="6fb6c-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6fb6c-194">Search-Flags</span></span>           | <span data-ttu-id="6fb6c-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6fb6c-195">0x00000000</span></span>                                                              |
| <span data-ttu-id="6fb6c-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6fb6c-196">System-Flags</span></span>           | <span data-ttu-id="6fb6c-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6fb6c-197">0x00000010</span></span>                                                              |
| <span data-ttu-id="6fb6c-198">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="6fb6c-198">Classes used in</span></span>        | [<span data-ttu-id="6fb6c-199">**PKI-Certificate-modèle**</span><span class="sxs-lookup"><span data-stu-id="6fb6c-199">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6fb6c-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6fb6c-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6fb6c-201">Entrée</span><span class="sxs-lookup"><span data-stu-id="6fb6c-201">Entry</span></span> | <span data-ttu-id="6fb6c-202">Valeur</span><span class="sxs-lookup"><span data-stu-id="6fb6c-202">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="6fb6c-203">ID de lien</span><span class="sxs-lookup"><span data-stu-id="6fb6c-203">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="6fb6c-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6fb6c-204">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="6fb6c-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="6fb6c-205">System-Only</span></span>            | <span data-ttu-id="6fb6c-206">Faux</span><span class="sxs-lookup"><span data-stu-id="6fb6c-206">False</span></span>                                                                   |
| <span data-ttu-id="6fb6c-207">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="6fb6c-207">Is-Single-Valued</span></span>       | <span data-ttu-id="6fb6c-208">Vrai</span><span class="sxs-lookup"><span data-stu-id="6fb6c-208">True</span></span>                                                                    |
| <span data-ttu-id="6fb6c-209">Est indexé</span><span class="sxs-lookup"><span data-stu-id="6fb6c-209">Is Indexed</span></span>             | <span data-ttu-id="6fb6c-210">Faux</span><span class="sxs-lookup"><span data-stu-id="6fb6c-210">False</span></span>                                                                   |
| <span data-ttu-id="6fb6c-211">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="6fb6c-211">In Global Catalog</span></span>      | <span data-ttu-id="6fb6c-212">Faux</span><span class="sxs-lookup"><span data-stu-id="6fb6c-212">False</span></span>                                                                   |
| <span data-ttu-id="6fb6c-213">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="6fb6c-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="6fb6c-214">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="6fb6c-214">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="6fb6c-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6fb6c-215">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="6fb6c-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6fb6c-216">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="6fb6c-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6fb6c-217">Search-Flags</span></span>           | <span data-ttu-id="6fb6c-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6fb6c-218">0x00000000</span></span>                                                              |
| <span data-ttu-id="6fb6c-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6fb6c-219">System-Flags</span></span>           | <span data-ttu-id="6fb6c-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6fb6c-220">0x00000010</span></span>                                                              |
| <span data-ttu-id="6fb6c-221">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="6fb6c-221">Classes used in</span></span>        | [<span data-ttu-id="6fb6c-222">**PKI-Certificate-modèle**</span><span class="sxs-lookup"><span data-stu-id="6fb6c-222">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6fb6c-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6fb6c-223">Windows Server 2012</span></span>



| <span data-ttu-id="6fb6c-224">Entrée</span><span class="sxs-lookup"><span data-stu-id="6fb6c-224">Entry</span></span> | <span data-ttu-id="6fb6c-225">Valeur</span><span class="sxs-lookup"><span data-stu-id="6fb6c-225">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="6fb6c-226">ID de lien</span><span class="sxs-lookup"><span data-stu-id="6fb6c-226">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="6fb6c-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6fb6c-227">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="6fb6c-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="6fb6c-228">System-Only</span></span>            | <span data-ttu-id="6fb6c-229">Faux</span><span class="sxs-lookup"><span data-stu-id="6fb6c-229">False</span></span>                                                                   |
| <span data-ttu-id="6fb6c-230">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="6fb6c-230">Is-Single-Valued</span></span>       | <span data-ttu-id="6fb6c-231">Vrai</span><span class="sxs-lookup"><span data-stu-id="6fb6c-231">True</span></span>                                                                    |
| <span data-ttu-id="6fb6c-232">Est indexé</span><span class="sxs-lookup"><span data-stu-id="6fb6c-232">Is Indexed</span></span>             | <span data-ttu-id="6fb6c-233">Faux</span><span class="sxs-lookup"><span data-stu-id="6fb6c-233">False</span></span>                                                                   |
| <span data-ttu-id="6fb6c-234">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="6fb6c-234">In Global Catalog</span></span>      | <span data-ttu-id="6fb6c-235">Faux</span><span class="sxs-lookup"><span data-stu-id="6fb6c-235">False</span></span>                                                                   |
| <span data-ttu-id="6fb6c-236">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="6fb6c-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="6fb6c-237">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="6fb6c-237">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="6fb6c-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6fb6c-238">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="6fb6c-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6fb6c-239">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="6fb6c-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6fb6c-240">Search-Flags</span></span>           | <span data-ttu-id="6fb6c-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6fb6c-241">0x00000000</span></span>                                                              |
| <span data-ttu-id="6fb6c-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6fb6c-242">System-Flags</span></span>           | <span data-ttu-id="6fb6c-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6fb6c-243">0x00000010</span></span>                                                              |
| <span data-ttu-id="6fb6c-244">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="6fb6c-244">Classes used in</span></span>        | [<span data-ttu-id="6fb6c-245">**PKI-Certificate-modèle**</span><span class="sxs-lookup"><span data-stu-id="6fb6c-245">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 





