---
title: MS-PKI-inscription-attribut d’indicateur
description: Contient les indicateurs liés à l’inscription.
ms.assetid: e854acb1-75f4-4379-b404-8fa096419ee6
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory pour l’attribut d’inscription MS-PKI-Flag
- Attribut mspki-inscription-schéma AD (attribut d’indicateur)
topic_type:
- apiref
api_name:
- ms-PKI-Enrollment-Flag
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2df092e28633bd5825c422e306bf7a65982b32a8
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103943148"
---
# <a name="ms-pki-enrollment-flag-attribute"></a><span data-ttu-id="99ff1-105">MS-PKI-inscription-attribut d’indicateur</span><span class="sxs-lookup"><span data-stu-id="99ff1-105">ms-PKI-Enrollment-Flag attribute</span></span>

<span data-ttu-id="99ff1-106">Contient les indicateurs liés à l’inscription.</span><span class="sxs-lookup"><span data-stu-id="99ff1-106">Contains the enrollment related flags.</span></span>



| <span data-ttu-id="99ff1-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="99ff1-107">Entry</span></span> | <span data-ttu-id="99ff1-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="99ff1-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99ff1-109">CN</span><span class="sxs-lookup"><span data-stu-id="99ff1-109">CN</span></span>                | <span data-ttu-id="99ff1-110">MS-PKI-inscription-indicateur</span><span class="sxs-lookup"><span data-stu-id="99ff1-110">ms-PKI-Enrollment-Flag</span></span>                                                                            |
| <span data-ttu-id="99ff1-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="99ff1-111">Ldap-Display-Name</span></span> | <span data-ttu-id="99ff1-112">Attribut mspki-indicateur d’inscription</span><span class="sxs-lookup"><span data-stu-id="99ff1-112">msPKI-Enrollment-Flag</span></span>                                                                             |
| <span data-ttu-id="99ff1-113">Taille</span><span class="sxs-lookup"><span data-stu-id="99ff1-113">Size</span></span>              | <span data-ttu-id="99ff1-114">4 octets</span><span class="sxs-lookup"><span data-stu-id="99ff1-114">4 bytes</span></span>                                                                                           |
| <span data-ttu-id="99ff1-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="99ff1-115">Update Privilege</span></span>  | <span data-ttu-id="99ff1-116">Administrateur de domaine</span><span class="sxs-lookup"><span data-stu-id="99ff1-116">Domain administrator</span></span>                                                                              |
| <span data-ttu-id="99ff1-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="99ff1-117">Update Frequency</span></span>  | <span data-ttu-id="99ff1-118">Lorsque l’objet modèle de certificat (MS-PKI-Certificate-template) est modifié, créé ou cloné.</span><span class="sxs-lookup"><span data-stu-id="99ff1-118">When the certificate template (ms-PKI-Certificate-Template) object is edited, created, or cloned.</span></span> |
| <span data-ttu-id="99ff1-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="99ff1-119">Attribute-Id</span></span>      | <span data-ttu-id="99ff1-120">1.2.840.113556.1.4.1430</span><span class="sxs-lookup"><span data-stu-id="99ff1-120">1.2.840.113556.1.4.1430</span></span>                                                                           |
| <span data-ttu-id="99ff1-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="99ff1-121">System-Id-Guid</span></span>    | <span data-ttu-id="99ff1-122">d15ef7d8-f226-46db-ae79-b34e560bd12c</span><span class="sxs-lookup"><span data-stu-id="99ff1-122">d15ef7d8-f226-46db-ae79-b34e560bd12c</span></span>                                                              |
| <span data-ttu-id="99ff1-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="99ff1-123">Syntax</span></span>            | [<span data-ttu-id="99ff1-124">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="99ff1-124">**Enumeration**</span></span>](s-enumeration.md)                                                              |



## <a name="implementations"></a><span data-ttu-id="99ff1-125">Implémentations</span><span class="sxs-lookup"><span data-stu-id="99ff1-125">Implementations</span></span>

-   [<span data-ttu-id="99ff1-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="99ff1-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="99ff1-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="99ff1-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="99ff1-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="99ff1-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="99ff1-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="99ff1-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="99ff1-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="99ff1-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="99ff1-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="99ff1-131">Windows Server 2003</span></span>



| <span data-ttu-id="99ff1-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="99ff1-132">Entry</span></span> | <span data-ttu-id="99ff1-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="99ff1-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="99ff1-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="99ff1-134">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="99ff1-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="99ff1-135">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="99ff1-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="99ff1-136">System-Only</span></span>            | <span data-ttu-id="99ff1-137">Faux</span><span class="sxs-lookup"><span data-stu-id="99ff1-137">False</span></span>                                                                   |
| <span data-ttu-id="99ff1-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="99ff1-138">Is-Single-Valued</span></span>       | <span data-ttu-id="99ff1-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="99ff1-139">True</span></span>                                                                    |
| <span data-ttu-id="99ff1-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="99ff1-140">Is Indexed</span></span>             | <span data-ttu-id="99ff1-141">Faux</span><span class="sxs-lookup"><span data-stu-id="99ff1-141">False</span></span>                                                                   |
| <span data-ttu-id="99ff1-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="99ff1-142">In Global Catalog</span></span>      | <span data-ttu-id="99ff1-143">Faux</span><span class="sxs-lookup"><span data-stu-id="99ff1-143">False</span></span>                                                                   |
| <span data-ttu-id="99ff1-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="99ff1-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="99ff1-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="99ff1-145">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="99ff1-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="99ff1-146">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="99ff1-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="99ff1-147">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="99ff1-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="99ff1-148">Search-Flags</span></span>           | <span data-ttu-id="99ff1-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="99ff1-149">0x00000000</span></span>                                                              |
| <span data-ttu-id="99ff1-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="99ff1-150">System-Flags</span></span>           | <span data-ttu-id="99ff1-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="99ff1-151">0x00000010</span></span>                                                              |
| <span data-ttu-id="99ff1-152">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="99ff1-152">Classes used in</span></span>        | [<span data-ttu-id="99ff1-153">**PKI-Certificate-modèle**</span><span class="sxs-lookup"><span data-stu-id="99ff1-153">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="99ff1-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="99ff1-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="99ff1-155">Entrée</span><span class="sxs-lookup"><span data-stu-id="99ff1-155">Entry</span></span> | <span data-ttu-id="99ff1-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="99ff1-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="99ff1-157">ID de lien</span><span class="sxs-lookup"><span data-stu-id="99ff1-157">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="99ff1-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="99ff1-158">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="99ff1-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="99ff1-159">System-Only</span></span>            | <span data-ttu-id="99ff1-160">Faux</span><span class="sxs-lookup"><span data-stu-id="99ff1-160">False</span></span>                                                                   |
| <span data-ttu-id="99ff1-161">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="99ff1-161">Is-Single-Valued</span></span>       | <span data-ttu-id="99ff1-162">Vrai</span><span class="sxs-lookup"><span data-stu-id="99ff1-162">True</span></span>                                                                    |
| <span data-ttu-id="99ff1-163">Est indexé</span><span class="sxs-lookup"><span data-stu-id="99ff1-163">Is Indexed</span></span>             | <span data-ttu-id="99ff1-164">Faux</span><span class="sxs-lookup"><span data-stu-id="99ff1-164">False</span></span>                                                                   |
| <span data-ttu-id="99ff1-165">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="99ff1-165">In Global Catalog</span></span>      | <span data-ttu-id="99ff1-166">Faux</span><span class="sxs-lookup"><span data-stu-id="99ff1-166">False</span></span>                                                                   |
| <span data-ttu-id="99ff1-167">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="99ff1-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="99ff1-168">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="99ff1-168">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="99ff1-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="99ff1-169">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="99ff1-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="99ff1-170">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="99ff1-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="99ff1-171">Search-Flags</span></span>           | <span data-ttu-id="99ff1-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="99ff1-172">0x00000000</span></span>                                                              |
| <span data-ttu-id="99ff1-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="99ff1-173">System-Flags</span></span>           | <span data-ttu-id="99ff1-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="99ff1-174">0x00000010</span></span>                                                              |
| <span data-ttu-id="99ff1-175">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="99ff1-175">Classes used in</span></span>        | [<span data-ttu-id="99ff1-176">**PKI-Certificate-modèle**</span><span class="sxs-lookup"><span data-stu-id="99ff1-176">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="99ff1-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="99ff1-177">Windows Server 2008</span></span>



| <span data-ttu-id="99ff1-178">Entrée</span><span class="sxs-lookup"><span data-stu-id="99ff1-178">Entry</span></span> | <span data-ttu-id="99ff1-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="99ff1-179">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="99ff1-180">ID de lien</span><span class="sxs-lookup"><span data-stu-id="99ff1-180">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="99ff1-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="99ff1-181">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="99ff1-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="99ff1-182">System-Only</span></span>            | <span data-ttu-id="99ff1-183">Faux</span><span class="sxs-lookup"><span data-stu-id="99ff1-183">False</span></span>                                                                   |
| <span data-ttu-id="99ff1-184">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="99ff1-184">Is-Single-Valued</span></span>       | <span data-ttu-id="99ff1-185">Vrai</span><span class="sxs-lookup"><span data-stu-id="99ff1-185">True</span></span>                                                                    |
| <span data-ttu-id="99ff1-186">Est indexé</span><span class="sxs-lookup"><span data-stu-id="99ff1-186">Is Indexed</span></span>             | <span data-ttu-id="99ff1-187">Faux</span><span class="sxs-lookup"><span data-stu-id="99ff1-187">False</span></span>                                                                   |
| <span data-ttu-id="99ff1-188">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="99ff1-188">In Global Catalog</span></span>      | <span data-ttu-id="99ff1-189">Faux</span><span class="sxs-lookup"><span data-stu-id="99ff1-189">False</span></span>                                                                   |
| <span data-ttu-id="99ff1-190">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="99ff1-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="99ff1-191">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="99ff1-191">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="99ff1-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="99ff1-192">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="99ff1-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="99ff1-193">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="99ff1-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="99ff1-194">Search-Flags</span></span>           | <span data-ttu-id="99ff1-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="99ff1-195">0x00000000</span></span>                                                              |
| <span data-ttu-id="99ff1-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="99ff1-196">System-Flags</span></span>           | <span data-ttu-id="99ff1-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="99ff1-197">0x00000010</span></span>                                                              |
| <span data-ttu-id="99ff1-198">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="99ff1-198">Classes used in</span></span>        | [<span data-ttu-id="99ff1-199">**PKI-Certificate-modèle**</span><span class="sxs-lookup"><span data-stu-id="99ff1-199">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="99ff1-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="99ff1-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="99ff1-201">Entrée</span><span class="sxs-lookup"><span data-stu-id="99ff1-201">Entry</span></span> | <span data-ttu-id="99ff1-202">Valeur</span><span class="sxs-lookup"><span data-stu-id="99ff1-202">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="99ff1-203">ID de lien</span><span class="sxs-lookup"><span data-stu-id="99ff1-203">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="99ff1-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="99ff1-204">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="99ff1-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="99ff1-205">System-Only</span></span>            | <span data-ttu-id="99ff1-206">Faux</span><span class="sxs-lookup"><span data-stu-id="99ff1-206">False</span></span>                                                                   |
| <span data-ttu-id="99ff1-207">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="99ff1-207">Is-Single-Valued</span></span>       | <span data-ttu-id="99ff1-208">Vrai</span><span class="sxs-lookup"><span data-stu-id="99ff1-208">True</span></span>                                                                    |
| <span data-ttu-id="99ff1-209">Est indexé</span><span class="sxs-lookup"><span data-stu-id="99ff1-209">Is Indexed</span></span>             | <span data-ttu-id="99ff1-210">Faux</span><span class="sxs-lookup"><span data-stu-id="99ff1-210">False</span></span>                                                                   |
| <span data-ttu-id="99ff1-211">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="99ff1-211">In Global Catalog</span></span>      | <span data-ttu-id="99ff1-212">Faux</span><span class="sxs-lookup"><span data-stu-id="99ff1-212">False</span></span>                                                                   |
| <span data-ttu-id="99ff1-213">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="99ff1-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="99ff1-214">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="99ff1-214">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="99ff1-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="99ff1-215">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="99ff1-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="99ff1-216">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="99ff1-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="99ff1-217">Search-Flags</span></span>           | <span data-ttu-id="99ff1-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="99ff1-218">0x00000000</span></span>                                                              |
| <span data-ttu-id="99ff1-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="99ff1-219">System-Flags</span></span>           | <span data-ttu-id="99ff1-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="99ff1-220">0x00000010</span></span>                                                              |
| <span data-ttu-id="99ff1-221">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="99ff1-221">Classes used in</span></span>        | [<span data-ttu-id="99ff1-222">**PKI-Certificate-modèle**</span><span class="sxs-lookup"><span data-stu-id="99ff1-222">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="99ff1-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="99ff1-223">Windows Server 2012</span></span>



| <span data-ttu-id="99ff1-224">Entrée</span><span class="sxs-lookup"><span data-stu-id="99ff1-224">Entry</span></span> | <span data-ttu-id="99ff1-225">Valeur</span><span class="sxs-lookup"><span data-stu-id="99ff1-225">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="99ff1-226">ID de lien</span><span class="sxs-lookup"><span data-stu-id="99ff1-226">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="99ff1-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="99ff1-227">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="99ff1-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="99ff1-228">System-Only</span></span>            | <span data-ttu-id="99ff1-229">Faux</span><span class="sxs-lookup"><span data-stu-id="99ff1-229">False</span></span>                                                                   |
| <span data-ttu-id="99ff1-230">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="99ff1-230">Is-Single-Valued</span></span>       | <span data-ttu-id="99ff1-231">Vrai</span><span class="sxs-lookup"><span data-stu-id="99ff1-231">True</span></span>                                                                    |
| <span data-ttu-id="99ff1-232">Est indexé</span><span class="sxs-lookup"><span data-stu-id="99ff1-232">Is Indexed</span></span>             | <span data-ttu-id="99ff1-233">Faux</span><span class="sxs-lookup"><span data-stu-id="99ff1-233">False</span></span>                                                                   |
| <span data-ttu-id="99ff1-234">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="99ff1-234">In Global Catalog</span></span>      | <span data-ttu-id="99ff1-235">Faux</span><span class="sxs-lookup"><span data-stu-id="99ff1-235">False</span></span>                                                                   |
| <span data-ttu-id="99ff1-236">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="99ff1-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="99ff1-237">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="99ff1-237">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="99ff1-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="99ff1-238">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="99ff1-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="99ff1-239">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="99ff1-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="99ff1-240">Search-Flags</span></span>           | <span data-ttu-id="99ff1-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="99ff1-241">0x00000000</span></span>                                                              |
| <span data-ttu-id="99ff1-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="99ff1-242">System-Flags</span></span>           | <span data-ttu-id="99ff1-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="99ff1-243">0x00000010</span></span>                                                              |
| <span data-ttu-id="99ff1-244">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="99ff1-244">Classes used in</span></span>        | [<span data-ttu-id="99ff1-245">**PKI-Certificate-modèle**</span><span class="sxs-lookup"><span data-stu-id="99ff1-245">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 





