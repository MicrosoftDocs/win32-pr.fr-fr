---
title: MS-PKI-remplace-attribut templates
description: Spécifie les noms des modèles de certificat qui sont remplacés par le modèle actuel.
ms.assetid: 4e247932-1c50-4bfb-b723-52b7c36a8571
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut ms-PKI-remplace-templates
- Attribut mspki-remplace-attribut templates Active Directory Schema
topic_type:
- apiref
api_name:
- ms-PKI-Supersede-Templates
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd11ac2b96846912b0c6b1e8d01c6fd558f5f6db
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104519761"
---
# <a name="ms-pki-supersede-templates-attribute"></a><span data-ttu-id="4236c-105">MS-PKI-remplace-attribut templates</span><span class="sxs-lookup"><span data-stu-id="4236c-105">ms-PKI-Supersede-Templates attribute</span></span>

<span data-ttu-id="4236c-106">Spécifie les noms des modèles de certificat qui sont remplacés par le modèle actuel.</span><span class="sxs-lookup"><span data-stu-id="4236c-106">Specifies the names of the certificate templates that are superseded by the current template.</span></span>



| <span data-ttu-id="4236c-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="4236c-107">Entry</span></span> | <span data-ttu-id="4236c-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="4236c-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4236c-109">CN</span><span class="sxs-lookup"><span data-stu-id="4236c-109">CN</span></span>                | <span data-ttu-id="4236c-110">MS-PKI-remplace-templates</span><span class="sxs-lookup"><span data-stu-id="4236c-110">ms-PKI-Supersede-Templates</span></span>                                                                        |
| <span data-ttu-id="4236c-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="4236c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="4236c-112">Attribut mspki-remplace-templates</span><span class="sxs-lookup"><span data-stu-id="4236c-112">msPKI-Supersede-Templates</span></span>                                                                         |
| <span data-ttu-id="4236c-113">Taille</span><span class="sxs-lookup"><span data-stu-id="4236c-113">Size</span></span>              | <span data-ttu-id="4236c-114">64 octets</span><span class="sxs-lookup"><span data-stu-id="4236c-114">64 bytes</span></span>                                                                                          |
| <span data-ttu-id="4236c-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="4236c-115">Update Privilege</span></span>  | <span data-ttu-id="4236c-116">Administrateur de domaine</span><span class="sxs-lookup"><span data-stu-id="4236c-116">Domain administrator</span></span>                                                                              |
| <span data-ttu-id="4236c-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="4236c-117">Update Frequency</span></span>  | <span data-ttu-id="4236c-118">Lorsque l’objet modèle de certificat (MS-PKI-Certificate-template) est modifié, créé ou cloné.</span><span class="sxs-lookup"><span data-stu-id="4236c-118">When the certificate template (ms-PKI-Certificate-Template) object is edited, created, or cloned.</span></span> |
| <span data-ttu-id="4236c-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4236c-119">Attribute-Id</span></span>      | <span data-ttu-id="4236c-120">1.2.840.113556.1.4.1437</span><span class="sxs-lookup"><span data-stu-id="4236c-120">1.2.840.113556.1.4.1437</span></span>                                                                           |
| <span data-ttu-id="4236c-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="4236c-121">System-Id-Guid</span></span>    | <span data-ttu-id="4236c-122">9de8ae7d-7a5b-421d-b5e4-061f79dfd5d7</span><span class="sxs-lookup"><span data-stu-id="4236c-122">9de8ae7d-7a5b-421d-b5e4-061f79dfd5d7</span></span>                                                              |
| <span data-ttu-id="4236c-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4236c-123">Syntax</span></span>            | [<span data-ttu-id="4236c-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="4236c-124">**String(Unicode)**</span></span>](s-string-unicode.md)                                                       |



## <a name="implementations"></a><span data-ttu-id="4236c-125">Implémentations</span><span class="sxs-lookup"><span data-stu-id="4236c-125">Implementations</span></span>

-   [<span data-ttu-id="4236c-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4236c-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4236c-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4236c-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4236c-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4236c-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4236c-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4236c-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4236c-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4236c-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="4236c-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4236c-131">Windows Server 2003</span></span>



| <span data-ttu-id="4236c-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="4236c-132">Entry</span></span> | <span data-ttu-id="4236c-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="4236c-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="4236c-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="4236c-134">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="4236c-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4236c-135">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="4236c-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="4236c-136">System-Only</span></span>            | <span data-ttu-id="4236c-137">Faux</span><span class="sxs-lookup"><span data-stu-id="4236c-137">False</span></span>                                                                   |
| <span data-ttu-id="4236c-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="4236c-138">Is-Single-Valued</span></span>       | <span data-ttu-id="4236c-139">Faux</span><span class="sxs-lookup"><span data-stu-id="4236c-139">False</span></span>                                                                   |
| <span data-ttu-id="4236c-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="4236c-140">Is Indexed</span></span>             | <span data-ttu-id="4236c-141">Faux</span><span class="sxs-lookup"><span data-stu-id="4236c-141">False</span></span>                                                                   |
| <span data-ttu-id="4236c-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="4236c-142">In Global Catalog</span></span>      | <span data-ttu-id="4236c-143">Faux</span><span class="sxs-lookup"><span data-stu-id="4236c-143">False</span></span>                                                                   |
| <span data-ttu-id="4236c-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="4236c-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="4236c-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="4236c-145">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="4236c-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4236c-146">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="4236c-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4236c-147">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="4236c-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4236c-148">Search-Flags</span></span>           | <span data-ttu-id="4236c-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4236c-149">0x00000000</span></span>                                                              |
| <span data-ttu-id="4236c-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4236c-150">System-Flags</span></span>           | <span data-ttu-id="4236c-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4236c-151">0x00000010</span></span>                                                              |
| <span data-ttu-id="4236c-152">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="4236c-152">Classes used in</span></span>        | [<span data-ttu-id="4236c-153">**PKI-Certificate-modèle**</span><span class="sxs-lookup"><span data-stu-id="4236c-153">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4236c-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4236c-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4236c-155">Entrée</span><span class="sxs-lookup"><span data-stu-id="4236c-155">Entry</span></span> | <span data-ttu-id="4236c-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="4236c-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="4236c-157">ID de lien</span><span class="sxs-lookup"><span data-stu-id="4236c-157">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="4236c-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4236c-158">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="4236c-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="4236c-159">System-Only</span></span>            | <span data-ttu-id="4236c-160">Faux</span><span class="sxs-lookup"><span data-stu-id="4236c-160">False</span></span>                                                                   |
| <span data-ttu-id="4236c-161">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="4236c-161">Is-Single-Valued</span></span>       | <span data-ttu-id="4236c-162">Faux</span><span class="sxs-lookup"><span data-stu-id="4236c-162">False</span></span>                                                                   |
| <span data-ttu-id="4236c-163">Est indexé</span><span class="sxs-lookup"><span data-stu-id="4236c-163">Is Indexed</span></span>             | <span data-ttu-id="4236c-164">Faux</span><span class="sxs-lookup"><span data-stu-id="4236c-164">False</span></span>                                                                   |
| <span data-ttu-id="4236c-165">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="4236c-165">In Global Catalog</span></span>      | <span data-ttu-id="4236c-166">Faux</span><span class="sxs-lookup"><span data-stu-id="4236c-166">False</span></span>                                                                   |
| <span data-ttu-id="4236c-167">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="4236c-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="4236c-168">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="4236c-168">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="4236c-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4236c-169">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="4236c-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4236c-170">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="4236c-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4236c-171">Search-Flags</span></span>           | <span data-ttu-id="4236c-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4236c-172">0x00000000</span></span>                                                              |
| <span data-ttu-id="4236c-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4236c-173">System-Flags</span></span>           | <span data-ttu-id="4236c-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4236c-174">0x00000010</span></span>                                                              |
| <span data-ttu-id="4236c-175">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="4236c-175">Classes used in</span></span>        | [<span data-ttu-id="4236c-176">**PKI-Certificate-modèle**</span><span class="sxs-lookup"><span data-stu-id="4236c-176">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4236c-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4236c-177">Windows Server 2008</span></span>



| <span data-ttu-id="4236c-178">Entrée</span><span class="sxs-lookup"><span data-stu-id="4236c-178">Entry</span></span> | <span data-ttu-id="4236c-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="4236c-179">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="4236c-180">ID de lien</span><span class="sxs-lookup"><span data-stu-id="4236c-180">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="4236c-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4236c-181">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="4236c-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="4236c-182">System-Only</span></span>            | <span data-ttu-id="4236c-183">Faux</span><span class="sxs-lookup"><span data-stu-id="4236c-183">False</span></span>                                                                   |
| <span data-ttu-id="4236c-184">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="4236c-184">Is-Single-Valued</span></span>       | <span data-ttu-id="4236c-185">Faux</span><span class="sxs-lookup"><span data-stu-id="4236c-185">False</span></span>                                                                   |
| <span data-ttu-id="4236c-186">Est indexé</span><span class="sxs-lookup"><span data-stu-id="4236c-186">Is Indexed</span></span>             | <span data-ttu-id="4236c-187">Faux</span><span class="sxs-lookup"><span data-stu-id="4236c-187">False</span></span>                                                                   |
| <span data-ttu-id="4236c-188">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="4236c-188">In Global Catalog</span></span>      | <span data-ttu-id="4236c-189">Faux</span><span class="sxs-lookup"><span data-stu-id="4236c-189">False</span></span>                                                                   |
| <span data-ttu-id="4236c-190">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="4236c-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="4236c-191">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="4236c-191">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="4236c-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4236c-192">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="4236c-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4236c-193">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="4236c-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4236c-194">Search-Flags</span></span>           | <span data-ttu-id="4236c-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4236c-195">0x00000000</span></span>                                                              |
| <span data-ttu-id="4236c-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4236c-196">System-Flags</span></span>           | <span data-ttu-id="4236c-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4236c-197">0x00000010</span></span>                                                              |
| <span data-ttu-id="4236c-198">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="4236c-198">Classes used in</span></span>        | [<span data-ttu-id="4236c-199">**PKI-Certificate-modèle**</span><span class="sxs-lookup"><span data-stu-id="4236c-199">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4236c-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4236c-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4236c-201">Entrée</span><span class="sxs-lookup"><span data-stu-id="4236c-201">Entry</span></span> | <span data-ttu-id="4236c-202">Valeur</span><span class="sxs-lookup"><span data-stu-id="4236c-202">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="4236c-203">ID de lien</span><span class="sxs-lookup"><span data-stu-id="4236c-203">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="4236c-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4236c-204">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="4236c-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="4236c-205">System-Only</span></span>            | <span data-ttu-id="4236c-206">Faux</span><span class="sxs-lookup"><span data-stu-id="4236c-206">False</span></span>                                                                   |
| <span data-ttu-id="4236c-207">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="4236c-207">Is-Single-Valued</span></span>       | <span data-ttu-id="4236c-208">Faux</span><span class="sxs-lookup"><span data-stu-id="4236c-208">False</span></span>                                                                   |
| <span data-ttu-id="4236c-209">Est indexé</span><span class="sxs-lookup"><span data-stu-id="4236c-209">Is Indexed</span></span>             | <span data-ttu-id="4236c-210">Faux</span><span class="sxs-lookup"><span data-stu-id="4236c-210">False</span></span>                                                                   |
| <span data-ttu-id="4236c-211">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="4236c-211">In Global Catalog</span></span>      | <span data-ttu-id="4236c-212">Faux</span><span class="sxs-lookup"><span data-stu-id="4236c-212">False</span></span>                                                                   |
| <span data-ttu-id="4236c-213">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="4236c-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="4236c-214">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="4236c-214">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="4236c-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4236c-215">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="4236c-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4236c-216">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="4236c-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4236c-217">Search-Flags</span></span>           | <span data-ttu-id="4236c-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4236c-218">0x00000000</span></span>                                                              |
| <span data-ttu-id="4236c-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4236c-219">System-Flags</span></span>           | <span data-ttu-id="4236c-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4236c-220">0x00000010</span></span>                                                              |
| <span data-ttu-id="4236c-221">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="4236c-221">Classes used in</span></span>        | [<span data-ttu-id="4236c-222">**PKI-Certificate-modèle**</span><span class="sxs-lookup"><span data-stu-id="4236c-222">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4236c-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4236c-223">Windows Server 2012</span></span>



| <span data-ttu-id="4236c-224">Entrée</span><span class="sxs-lookup"><span data-stu-id="4236c-224">Entry</span></span> | <span data-ttu-id="4236c-225">Valeur</span><span class="sxs-lookup"><span data-stu-id="4236c-225">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="4236c-226">ID de lien</span><span class="sxs-lookup"><span data-stu-id="4236c-226">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="4236c-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4236c-227">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="4236c-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="4236c-228">System-Only</span></span>            | <span data-ttu-id="4236c-229">Faux</span><span class="sxs-lookup"><span data-stu-id="4236c-229">False</span></span>                                                                   |
| <span data-ttu-id="4236c-230">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="4236c-230">Is-Single-Valued</span></span>       | <span data-ttu-id="4236c-231">Faux</span><span class="sxs-lookup"><span data-stu-id="4236c-231">False</span></span>                                                                   |
| <span data-ttu-id="4236c-232">Est indexé</span><span class="sxs-lookup"><span data-stu-id="4236c-232">Is Indexed</span></span>             | <span data-ttu-id="4236c-233">Faux</span><span class="sxs-lookup"><span data-stu-id="4236c-233">False</span></span>                                                                   |
| <span data-ttu-id="4236c-234">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="4236c-234">In Global Catalog</span></span>      | <span data-ttu-id="4236c-235">Faux</span><span class="sxs-lookup"><span data-stu-id="4236c-235">False</span></span>                                                                   |
| <span data-ttu-id="4236c-236">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="4236c-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="4236c-237">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="4236c-237">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="4236c-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4236c-238">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="4236c-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4236c-239">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="4236c-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4236c-240">Search-Flags</span></span>           | <span data-ttu-id="4236c-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4236c-241">0x00000000</span></span>                                                              |
| <span data-ttu-id="4236c-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4236c-242">System-Flags</span></span>           | <span data-ttu-id="4236c-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4236c-243">0x00000010</span></span>                                                              |
| <span data-ttu-id="4236c-244">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="4236c-244">Classes used in</span></span>        | [<span data-ttu-id="4236c-245">**PKI-Certificate-modèle**</span><span class="sxs-lookup"><span data-stu-id="4236c-245">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 





