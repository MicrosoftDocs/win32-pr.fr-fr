---
title: MS-PKI-attribut minimal-Key-Size
description: Indique la taille minimale de la clé privée.
ms.assetid: e38fbab5-14db-40d1-80c4-c14477c6f0da
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory MS-PKI-attribut minimal-Key-Size
- Schéma AD attribut mspki-attribut de taille minimale de clé
topic_type:
- apiref
api_name:
- ms-PKI-Minimal-Key-Size
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4eb1a3f168393bb203f7c590ba52924670d3dab2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107722"
---
# <a name="ms-pki-minimal-key-size-attribute"></a><span data-ttu-id="9534c-105">MS-PKI-attribut minimal-Key-Size</span><span class="sxs-lookup"><span data-stu-id="9534c-105">ms-PKI-Minimal-Key-Size attribute</span></span>

<span data-ttu-id="9534c-106">Indique la taille minimale de la clé privée.</span><span class="sxs-lookup"><span data-stu-id="9534c-106">Indicates the minimum private key size.</span></span>



| <span data-ttu-id="9534c-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="9534c-107">Entry</span></span> | <span data-ttu-id="9534c-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="9534c-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9534c-109">CN</span><span class="sxs-lookup"><span data-stu-id="9534c-109">CN</span></span>                | <span data-ttu-id="9534c-110">MS-PKI-minimum-Key-Size</span><span class="sxs-lookup"><span data-stu-id="9534c-110">ms-PKI-Minimal-Key-Size</span></span>                                                                           |
| <span data-ttu-id="9534c-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="9534c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="9534c-112">Attribut mspki-minimal-Key-Size</span><span class="sxs-lookup"><span data-stu-id="9534c-112">msPKI-Minimal-Key-Size</span></span>                                                                            |
| <span data-ttu-id="9534c-113">Taille</span><span class="sxs-lookup"><span data-stu-id="9534c-113">Size</span></span>              | <span data-ttu-id="9534c-114">4 octets</span><span class="sxs-lookup"><span data-stu-id="9534c-114">4 bytes</span></span>                                                                                           |
| <span data-ttu-id="9534c-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="9534c-115">Update Privilege</span></span>  | <span data-ttu-id="9534c-116">Administrateur de domaine</span><span class="sxs-lookup"><span data-stu-id="9534c-116">Domain administrator</span></span>                                                                              |
| <span data-ttu-id="9534c-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="9534c-117">Update Frequency</span></span>  | <span data-ttu-id="9534c-118">Lorsque l’objet modèle de certificat (MS-PKI-Certificate-template) est modifié, créé ou cloné.</span><span class="sxs-lookup"><span data-stu-id="9534c-118">When the certificate template (ms-PKI-Certificate-Template) object is edited, created, or cloned.</span></span> |
| <span data-ttu-id="9534c-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9534c-119">Attribute-Id</span></span>      | <span data-ttu-id="9534c-120">1.2.840.113556.1.4.1433</span><span class="sxs-lookup"><span data-stu-id="9534c-120">1.2.840.113556.1.4.1433</span></span>                                                                           |
| <span data-ttu-id="9534c-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="9534c-121">System-Id-Guid</span></span>    | <span data-ttu-id="9534c-122">e96a63f5-417f-46d3-be52-db7703c503df</span><span class="sxs-lookup"><span data-stu-id="9534c-122">e96a63f5-417f-46d3-be52-db7703c503df</span></span>                                                              |
| <span data-ttu-id="9534c-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9534c-123">Syntax</span></span>            | [<span data-ttu-id="9534c-124">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="9534c-124">**Enumeration**</span></span>](s-enumeration.md)                                                              |



## <a name="implementations"></a><span data-ttu-id="9534c-125">Implémentations</span><span class="sxs-lookup"><span data-stu-id="9534c-125">Implementations</span></span>

-   [<span data-ttu-id="9534c-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9534c-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9534c-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9534c-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9534c-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9534c-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9534c-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9534c-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9534c-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9534c-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="9534c-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9534c-131">Windows Server 2003</span></span>



| <span data-ttu-id="9534c-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="9534c-132">Entry</span></span> | <span data-ttu-id="9534c-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="9534c-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="9534c-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9534c-134">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="9534c-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9534c-135">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="9534c-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="9534c-136">System-Only</span></span>            | <span data-ttu-id="9534c-137">Faux</span><span class="sxs-lookup"><span data-stu-id="9534c-137">False</span></span>                                                                   |
| <span data-ttu-id="9534c-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9534c-138">Is-Single-Valued</span></span>       | <span data-ttu-id="9534c-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="9534c-139">True</span></span>                                                                    |
| <span data-ttu-id="9534c-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9534c-140">Is Indexed</span></span>             | <span data-ttu-id="9534c-141">Faux</span><span class="sxs-lookup"><span data-stu-id="9534c-141">False</span></span>                                                                   |
| <span data-ttu-id="9534c-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9534c-142">In Global Catalog</span></span>      | <span data-ttu-id="9534c-143">Faux</span><span class="sxs-lookup"><span data-stu-id="9534c-143">False</span></span>                                                                   |
| <span data-ttu-id="9534c-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9534c-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="9534c-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9534c-145">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="9534c-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9534c-146">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="9534c-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9534c-147">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="9534c-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9534c-148">Search-Flags</span></span>           | <span data-ttu-id="9534c-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9534c-149">0x00000000</span></span>                                                              |
| <span data-ttu-id="9534c-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9534c-150">System-Flags</span></span>           | <span data-ttu-id="9534c-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9534c-151">0x00000010</span></span>                                                              |
| <span data-ttu-id="9534c-152">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9534c-152">Classes used in</span></span>        | [<span data-ttu-id="9534c-153">**PKI-Certificate-modèle**</span><span class="sxs-lookup"><span data-stu-id="9534c-153">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9534c-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9534c-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9534c-155">Entrée</span><span class="sxs-lookup"><span data-stu-id="9534c-155">Entry</span></span> | <span data-ttu-id="9534c-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="9534c-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="9534c-157">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9534c-157">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="9534c-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9534c-158">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="9534c-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="9534c-159">System-Only</span></span>            | <span data-ttu-id="9534c-160">Faux</span><span class="sxs-lookup"><span data-stu-id="9534c-160">False</span></span>                                                                   |
| <span data-ttu-id="9534c-161">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9534c-161">Is-Single-Valued</span></span>       | <span data-ttu-id="9534c-162">Vrai</span><span class="sxs-lookup"><span data-stu-id="9534c-162">True</span></span>                                                                    |
| <span data-ttu-id="9534c-163">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9534c-163">Is Indexed</span></span>             | <span data-ttu-id="9534c-164">Faux</span><span class="sxs-lookup"><span data-stu-id="9534c-164">False</span></span>                                                                   |
| <span data-ttu-id="9534c-165">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9534c-165">In Global Catalog</span></span>      | <span data-ttu-id="9534c-166">Faux</span><span class="sxs-lookup"><span data-stu-id="9534c-166">False</span></span>                                                                   |
| <span data-ttu-id="9534c-167">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9534c-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="9534c-168">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9534c-168">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="9534c-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9534c-169">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="9534c-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9534c-170">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="9534c-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9534c-171">Search-Flags</span></span>           | <span data-ttu-id="9534c-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9534c-172">0x00000000</span></span>                                                              |
| <span data-ttu-id="9534c-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9534c-173">System-Flags</span></span>           | <span data-ttu-id="9534c-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9534c-174">0x00000010</span></span>                                                              |
| <span data-ttu-id="9534c-175">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9534c-175">Classes used in</span></span>        | [<span data-ttu-id="9534c-176">**PKI-Certificate-modèle**</span><span class="sxs-lookup"><span data-stu-id="9534c-176">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9534c-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9534c-177">Windows Server 2008</span></span>



| <span data-ttu-id="9534c-178">Entrée</span><span class="sxs-lookup"><span data-stu-id="9534c-178">Entry</span></span> | <span data-ttu-id="9534c-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="9534c-179">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="9534c-180">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9534c-180">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="9534c-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9534c-181">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="9534c-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="9534c-182">System-Only</span></span>            | <span data-ttu-id="9534c-183">Faux</span><span class="sxs-lookup"><span data-stu-id="9534c-183">False</span></span>                                                                   |
| <span data-ttu-id="9534c-184">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9534c-184">Is-Single-Valued</span></span>       | <span data-ttu-id="9534c-185">Vrai</span><span class="sxs-lookup"><span data-stu-id="9534c-185">True</span></span>                                                                    |
| <span data-ttu-id="9534c-186">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9534c-186">Is Indexed</span></span>             | <span data-ttu-id="9534c-187">Faux</span><span class="sxs-lookup"><span data-stu-id="9534c-187">False</span></span>                                                                   |
| <span data-ttu-id="9534c-188">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9534c-188">In Global Catalog</span></span>      | <span data-ttu-id="9534c-189">Faux</span><span class="sxs-lookup"><span data-stu-id="9534c-189">False</span></span>                                                                   |
| <span data-ttu-id="9534c-190">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9534c-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="9534c-191">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9534c-191">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="9534c-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9534c-192">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="9534c-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9534c-193">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="9534c-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9534c-194">Search-Flags</span></span>           | <span data-ttu-id="9534c-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9534c-195">0x00000000</span></span>                                                              |
| <span data-ttu-id="9534c-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9534c-196">System-Flags</span></span>           | <span data-ttu-id="9534c-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9534c-197">0x00000010</span></span>                                                              |
| <span data-ttu-id="9534c-198">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9534c-198">Classes used in</span></span>        | [<span data-ttu-id="9534c-199">**PKI-Certificate-modèle**</span><span class="sxs-lookup"><span data-stu-id="9534c-199">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9534c-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9534c-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9534c-201">Entrée</span><span class="sxs-lookup"><span data-stu-id="9534c-201">Entry</span></span> | <span data-ttu-id="9534c-202">Valeur</span><span class="sxs-lookup"><span data-stu-id="9534c-202">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="9534c-203">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9534c-203">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="9534c-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9534c-204">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="9534c-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="9534c-205">System-Only</span></span>            | <span data-ttu-id="9534c-206">Faux</span><span class="sxs-lookup"><span data-stu-id="9534c-206">False</span></span>                                                                   |
| <span data-ttu-id="9534c-207">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9534c-207">Is-Single-Valued</span></span>       | <span data-ttu-id="9534c-208">Vrai</span><span class="sxs-lookup"><span data-stu-id="9534c-208">True</span></span>                                                                    |
| <span data-ttu-id="9534c-209">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9534c-209">Is Indexed</span></span>             | <span data-ttu-id="9534c-210">Faux</span><span class="sxs-lookup"><span data-stu-id="9534c-210">False</span></span>                                                                   |
| <span data-ttu-id="9534c-211">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9534c-211">In Global Catalog</span></span>      | <span data-ttu-id="9534c-212">Faux</span><span class="sxs-lookup"><span data-stu-id="9534c-212">False</span></span>                                                                   |
| <span data-ttu-id="9534c-213">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9534c-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="9534c-214">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9534c-214">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="9534c-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9534c-215">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="9534c-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9534c-216">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="9534c-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9534c-217">Search-Flags</span></span>           | <span data-ttu-id="9534c-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9534c-218">0x00000000</span></span>                                                              |
| <span data-ttu-id="9534c-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9534c-219">System-Flags</span></span>           | <span data-ttu-id="9534c-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9534c-220">0x00000010</span></span>                                                              |
| <span data-ttu-id="9534c-221">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9534c-221">Classes used in</span></span>        | [<span data-ttu-id="9534c-222">**PKI-Certificate-modèle**</span><span class="sxs-lookup"><span data-stu-id="9534c-222">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9534c-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9534c-223">Windows Server 2012</span></span>



| <span data-ttu-id="9534c-224">Entrée</span><span class="sxs-lookup"><span data-stu-id="9534c-224">Entry</span></span> | <span data-ttu-id="9534c-225">Valeur</span><span class="sxs-lookup"><span data-stu-id="9534c-225">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="9534c-226">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9534c-226">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="9534c-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9534c-227">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="9534c-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="9534c-228">System-Only</span></span>            | <span data-ttu-id="9534c-229">Faux</span><span class="sxs-lookup"><span data-stu-id="9534c-229">False</span></span>                                                                   |
| <span data-ttu-id="9534c-230">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9534c-230">Is-Single-Valued</span></span>       | <span data-ttu-id="9534c-231">Vrai</span><span class="sxs-lookup"><span data-stu-id="9534c-231">True</span></span>                                                                    |
| <span data-ttu-id="9534c-232">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9534c-232">Is Indexed</span></span>             | <span data-ttu-id="9534c-233">Faux</span><span class="sxs-lookup"><span data-stu-id="9534c-233">False</span></span>                                                                   |
| <span data-ttu-id="9534c-234">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9534c-234">In Global Catalog</span></span>      | <span data-ttu-id="9534c-235">Faux</span><span class="sxs-lookup"><span data-stu-id="9534c-235">False</span></span>                                                                   |
| <span data-ttu-id="9534c-236">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9534c-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="9534c-237">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9534c-237">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="9534c-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9534c-238">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="9534c-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9534c-239">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="9534c-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9534c-240">Search-Flags</span></span>           | <span data-ttu-id="9534c-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9534c-241">0x00000000</span></span>                                                              |
| <span data-ttu-id="9534c-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9534c-242">System-Flags</span></span>           | <span data-ttu-id="9534c-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9534c-243">0x00000010</span></span>                                                              |
| <span data-ttu-id="9534c-244">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9534c-244">Classes used in</span></span>        | [<span data-ttu-id="9534c-245">**PKI-Certificate-modèle**</span><span class="sxs-lookup"><span data-stu-id="9534c-245">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 





