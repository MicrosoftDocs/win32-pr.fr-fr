---
title: attribut ms-PKI-Certificate-Name-Flag
description: Contient les indicateurs associés à la construction du nom du sujet dans un certificat émis.
ms.assetid: 7aeeff69-86b5-4251-bd64-bd99b7c9ef4a
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut ms-PKI-Certificate-Name-Flag
- Attribut mspki-Certificate-nom-attribut d’indicateur-schéma Active Directory
topic_type:
- apiref
api_name:
- ms-PKI-Certificate-Name-Flag
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a9a5f8d6db36c3e3b86945fa529572df38ff6df
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104385439"
---
# <a name="ms-pki-certificate-name-flag-attribute"></a><span data-ttu-id="027cc-105">attribut ms-PKI-Certificate-Name-Flag</span><span class="sxs-lookup"><span data-stu-id="027cc-105">ms-PKI-Certificate-Name-Flag attribute</span></span>

<span data-ttu-id="027cc-106">Contient les indicateurs associés à la construction du nom du sujet dans un certificat émis.</span><span class="sxs-lookup"><span data-stu-id="027cc-106">Contains the flags related to constructing the subject name in an issued certificate.</span></span>



| <span data-ttu-id="027cc-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="027cc-107">Entry</span></span> | <span data-ttu-id="027cc-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="027cc-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="027cc-109">CN</span><span class="sxs-lookup"><span data-stu-id="027cc-109">CN</span></span>                | <span data-ttu-id="027cc-110">MS-PKI-Certificate-Name-Flag</span><span class="sxs-lookup"><span data-stu-id="027cc-110">ms-PKI-Certificate-Name-Flag</span></span>                                                                      |
| <span data-ttu-id="027cc-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="027cc-111">Ldap-Display-Name</span></span> | <span data-ttu-id="027cc-112">Attribut mspki-nom-certificat-indicateur</span><span class="sxs-lookup"><span data-stu-id="027cc-112">msPKI-Certificate-Name-Flag</span></span>                                                                       |
| <span data-ttu-id="027cc-113">Taille</span><span class="sxs-lookup"><span data-stu-id="027cc-113">Size</span></span>              | <span data-ttu-id="027cc-114">4 octets</span><span class="sxs-lookup"><span data-stu-id="027cc-114">4 bytes</span></span>                                                                                           |
| <span data-ttu-id="027cc-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="027cc-115">Update Privilege</span></span>  | <span data-ttu-id="027cc-116">Administrateur de domaine</span><span class="sxs-lookup"><span data-stu-id="027cc-116">Domain administrator</span></span>                                                                              |
| <span data-ttu-id="027cc-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="027cc-117">Update Frequency</span></span>  | <span data-ttu-id="027cc-118">Lorsque l’objet modèle de certificat (MS-PKI-Certificate-template) est modifié, créé ou cloné.</span><span class="sxs-lookup"><span data-stu-id="027cc-118">When the certificate template (ms-PKI-Certificate-Template) object is edited, created, or cloned.</span></span> |
| <span data-ttu-id="027cc-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="027cc-119">Attribute-Id</span></span>      | <span data-ttu-id="027cc-120">1.2.840.113556.1.4.1432</span><span class="sxs-lookup"><span data-stu-id="027cc-120">1.2.840.113556.1.4.1432</span></span>                                                                           |
| <span data-ttu-id="027cc-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="027cc-121">System-Id-Guid</span></span>    | <span data-ttu-id="027cc-122">ea1dddc4-60ff-416e-8cc0-17cee534bce7</span><span class="sxs-lookup"><span data-stu-id="027cc-122">ea1dddc4-60ff-416e-8cc0-17cee534bce7</span></span>                                                              |
| <span data-ttu-id="027cc-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="027cc-123">Syntax</span></span>            | [<span data-ttu-id="027cc-124">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="027cc-124">**Enumeration**</span></span>](s-enumeration.md)                                                              |



## <a name="implementations"></a><span data-ttu-id="027cc-125">Implémentations</span><span class="sxs-lookup"><span data-stu-id="027cc-125">Implementations</span></span>

-   [<span data-ttu-id="027cc-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="027cc-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="027cc-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="027cc-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="027cc-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="027cc-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="027cc-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="027cc-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="027cc-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="027cc-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="027cc-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="027cc-131">Windows Server 2003</span></span>



| <span data-ttu-id="027cc-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="027cc-132">Entry</span></span> | <span data-ttu-id="027cc-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="027cc-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="027cc-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="027cc-134">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="027cc-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="027cc-135">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="027cc-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="027cc-136">System-Only</span></span>            | <span data-ttu-id="027cc-137">Faux</span><span class="sxs-lookup"><span data-stu-id="027cc-137">False</span></span>                                                                   |
| <span data-ttu-id="027cc-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="027cc-138">Is-Single-Valued</span></span>       | <span data-ttu-id="027cc-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="027cc-139">True</span></span>                                                                    |
| <span data-ttu-id="027cc-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="027cc-140">Is Indexed</span></span>             | <span data-ttu-id="027cc-141">Faux</span><span class="sxs-lookup"><span data-stu-id="027cc-141">False</span></span>                                                                   |
| <span data-ttu-id="027cc-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="027cc-142">In Global Catalog</span></span>      | <span data-ttu-id="027cc-143">Faux</span><span class="sxs-lookup"><span data-stu-id="027cc-143">False</span></span>                                                                   |
| <span data-ttu-id="027cc-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="027cc-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="027cc-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="027cc-145">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="027cc-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="027cc-146">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="027cc-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="027cc-147">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="027cc-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="027cc-148">Search-Flags</span></span>           | <span data-ttu-id="027cc-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="027cc-149">0x00000000</span></span>                                                              |
| <span data-ttu-id="027cc-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="027cc-150">System-Flags</span></span>           | <span data-ttu-id="027cc-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="027cc-151">0x00000010</span></span>                                                              |
| <span data-ttu-id="027cc-152">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="027cc-152">Classes used in</span></span>        | [<span data-ttu-id="027cc-153">**PKI-Certificate-modèle**</span><span class="sxs-lookup"><span data-stu-id="027cc-153">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="027cc-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="027cc-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="027cc-155">Entrée</span><span class="sxs-lookup"><span data-stu-id="027cc-155">Entry</span></span> | <span data-ttu-id="027cc-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="027cc-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="027cc-157">ID de lien</span><span class="sxs-lookup"><span data-stu-id="027cc-157">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="027cc-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="027cc-158">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="027cc-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="027cc-159">System-Only</span></span>            | <span data-ttu-id="027cc-160">Faux</span><span class="sxs-lookup"><span data-stu-id="027cc-160">False</span></span>                                                                   |
| <span data-ttu-id="027cc-161">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="027cc-161">Is-Single-Valued</span></span>       | <span data-ttu-id="027cc-162">Vrai</span><span class="sxs-lookup"><span data-stu-id="027cc-162">True</span></span>                                                                    |
| <span data-ttu-id="027cc-163">Est indexé</span><span class="sxs-lookup"><span data-stu-id="027cc-163">Is Indexed</span></span>             | <span data-ttu-id="027cc-164">Faux</span><span class="sxs-lookup"><span data-stu-id="027cc-164">False</span></span>                                                                   |
| <span data-ttu-id="027cc-165">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="027cc-165">In Global Catalog</span></span>      | <span data-ttu-id="027cc-166">Faux</span><span class="sxs-lookup"><span data-stu-id="027cc-166">False</span></span>                                                                   |
| <span data-ttu-id="027cc-167">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="027cc-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="027cc-168">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="027cc-168">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="027cc-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="027cc-169">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="027cc-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="027cc-170">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="027cc-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="027cc-171">Search-Flags</span></span>           | <span data-ttu-id="027cc-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="027cc-172">0x00000000</span></span>                                                              |
| <span data-ttu-id="027cc-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="027cc-173">System-Flags</span></span>           | <span data-ttu-id="027cc-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="027cc-174">0x00000010</span></span>                                                              |
| <span data-ttu-id="027cc-175">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="027cc-175">Classes used in</span></span>        | [<span data-ttu-id="027cc-176">**PKI-Certificate-modèle**</span><span class="sxs-lookup"><span data-stu-id="027cc-176">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="027cc-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="027cc-177">Windows Server 2008</span></span>



| <span data-ttu-id="027cc-178">Entrée</span><span class="sxs-lookup"><span data-stu-id="027cc-178">Entry</span></span> | <span data-ttu-id="027cc-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="027cc-179">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="027cc-180">ID de lien</span><span class="sxs-lookup"><span data-stu-id="027cc-180">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="027cc-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="027cc-181">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="027cc-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="027cc-182">System-Only</span></span>            | <span data-ttu-id="027cc-183">Faux</span><span class="sxs-lookup"><span data-stu-id="027cc-183">False</span></span>                                                                   |
| <span data-ttu-id="027cc-184">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="027cc-184">Is-Single-Valued</span></span>       | <span data-ttu-id="027cc-185">Vrai</span><span class="sxs-lookup"><span data-stu-id="027cc-185">True</span></span>                                                                    |
| <span data-ttu-id="027cc-186">Est indexé</span><span class="sxs-lookup"><span data-stu-id="027cc-186">Is Indexed</span></span>             | <span data-ttu-id="027cc-187">Faux</span><span class="sxs-lookup"><span data-stu-id="027cc-187">False</span></span>                                                                   |
| <span data-ttu-id="027cc-188">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="027cc-188">In Global Catalog</span></span>      | <span data-ttu-id="027cc-189">Faux</span><span class="sxs-lookup"><span data-stu-id="027cc-189">False</span></span>                                                                   |
| <span data-ttu-id="027cc-190">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="027cc-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="027cc-191">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="027cc-191">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="027cc-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="027cc-192">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="027cc-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="027cc-193">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="027cc-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="027cc-194">Search-Flags</span></span>           | <span data-ttu-id="027cc-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="027cc-195">0x00000000</span></span>                                                              |
| <span data-ttu-id="027cc-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="027cc-196">System-Flags</span></span>           | <span data-ttu-id="027cc-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="027cc-197">0x00000010</span></span>                                                              |
| <span data-ttu-id="027cc-198">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="027cc-198">Classes used in</span></span>        | [<span data-ttu-id="027cc-199">**PKI-Certificate-modèle**</span><span class="sxs-lookup"><span data-stu-id="027cc-199">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="027cc-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="027cc-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="027cc-201">Entrée</span><span class="sxs-lookup"><span data-stu-id="027cc-201">Entry</span></span> | <span data-ttu-id="027cc-202">Valeur</span><span class="sxs-lookup"><span data-stu-id="027cc-202">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="027cc-203">ID de lien</span><span class="sxs-lookup"><span data-stu-id="027cc-203">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="027cc-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="027cc-204">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="027cc-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="027cc-205">System-Only</span></span>            | <span data-ttu-id="027cc-206">Faux</span><span class="sxs-lookup"><span data-stu-id="027cc-206">False</span></span>                                                                   |
| <span data-ttu-id="027cc-207">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="027cc-207">Is-Single-Valued</span></span>       | <span data-ttu-id="027cc-208">Vrai</span><span class="sxs-lookup"><span data-stu-id="027cc-208">True</span></span>                                                                    |
| <span data-ttu-id="027cc-209">Est indexé</span><span class="sxs-lookup"><span data-stu-id="027cc-209">Is Indexed</span></span>             | <span data-ttu-id="027cc-210">Faux</span><span class="sxs-lookup"><span data-stu-id="027cc-210">False</span></span>                                                                   |
| <span data-ttu-id="027cc-211">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="027cc-211">In Global Catalog</span></span>      | <span data-ttu-id="027cc-212">Faux</span><span class="sxs-lookup"><span data-stu-id="027cc-212">False</span></span>                                                                   |
| <span data-ttu-id="027cc-213">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="027cc-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="027cc-214">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="027cc-214">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="027cc-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="027cc-215">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="027cc-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="027cc-216">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="027cc-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="027cc-217">Search-Flags</span></span>           | <span data-ttu-id="027cc-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="027cc-218">0x00000000</span></span>                                                              |
| <span data-ttu-id="027cc-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="027cc-219">System-Flags</span></span>           | <span data-ttu-id="027cc-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="027cc-220">0x00000010</span></span>                                                              |
| <span data-ttu-id="027cc-221">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="027cc-221">Classes used in</span></span>        | [<span data-ttu-id="027cc-222">**PKI-Certificate-modèle**</span><span class="sxs-lookup"><span data-stu-id="027cc-222">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="027cc-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="027cc-223">Windows Server 2012</span></span>



| <span data-ttu-id="027cc-224">Entrée</span><span class="sxs-lookup"><span data-stu-id="027cc-224">Entry</span></span> | <span data-ttu-id="027cc-225">Valeur</span><span class="sxs-lookup"><span data-stu-id="027cc-225">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="027cc-226">ID de lien</span><span class="sxs-lookup"><span data-stu-id="027cc-226">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="027cc-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="027cc-227">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="027cc-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="027cc-228">System-Only</span></span>            | <span data-ttu-id="027cc-229">Faux</span><span class="sxs-lookup"><span data-stu-id="027cc-229">False</span></span>                                                                   |
| <span data-ttu-id="027cc-230">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="027cc-230">Is-Single-Valued</span></span>       | <span data-ttu-id="027cc-231">Vrai</span><span class="sxs-lookup"><span data-stu-id="027cc-231">True</span></span>                                                                    |
| <span data-ttu-id="027cc-232">Est indexé</span><span class="sxs-lookup"><span data-stu-id="027cc-232">Is Indexed</span></span>             | <span data-ttu-id="027cc-233">Faux</span><span class="sxs-lookup"><span data-stu-id="027cc-233">False</span></span>                                                                   |
| <span data-ttu-id="027cc-234">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="027cc-234">In Global Catalog</span></span>      | <span data-ttu-id="027cc-235">Faux</span><span class="sxs-lookup"><span data-stu-id="027cc-235">False</span></span>                                                                   |
| <span data-ttu-id="027cc-236">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="027cc-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="027cc-237">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="027cc-237">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="027cc-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="027cc-238">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="027cc-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="027cc-239">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="027cc-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="027cc-240">Search-Flags</span></span>           | <span data-ttu-id="027cc-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="027cc-241">0x00000000</span></span>                                                              |
| <span data-ttu-id="027cc-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="027cc-242">System-Flags</span></span>           | <span data-ttu-id="027cc-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="027cc-243">0x00000010</span></span>                                                              |
| <span data-ttu-id="027cc-244">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="027cc-244">Classes used in</span></span>        | [<span data-ttu-id="027cc-245">**PKI-Certificate-modèle**</span><span class="sxs-lookup"><span data-stu-id="027cc-245">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 





