---
title: attribut ms-PKI-RA-Policies
description: Contient la liste des OID de stratégie requis des autorités d’inscription qui signent la demande d’inscription.
ms.assetid: ebbdf95e-05c8-4b54-b7a5-4bb81d425225
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut ms-PKI-RA-Policies
- Schéma AD de l’attribut attribut mspki-RA-Policies
topic_type:
- apiref
api_name:
- ms-PKI-RA-Policies
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b948dac7a95ae8b46972ace4d1ab46260b476da
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103949864"
---
# <a name="ms-pki-ra-policies-attribute"></a><span data-ttu-id="b1dd0-105">attribut ms-PKI-RA-Policies</span><span class="sxs-lookup"><span data-stu-id="b1dd0-105">ms-PKI-RA-Policies attribute</span></span>

<span data-ttu-id="b1dd0-106">Contient la liste des OID de stratégie requis des autorités d’inscription qui signent la demande d’inscription.</span><span class="sxs-lookup"><span data-stu-id="b1dd0-106">Contains the list of required policy OIDs from registration authorities who sign the enrollment request.</span></span>



| <span data-ttu-id="b1dd0-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="b1dd0-107">Entry</span></span> | <span data-ttu-id="b1dd0-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="b1dd0-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1dd0-109">CN</span><span class="sxs-lookup"><span data-stu-id="b1dd0-109">CN</span></span>                | <span data-ttu-id="b1dd0-110">MS-PKI-RA-stratégies</span><span class="sxs-lookup"><span data-stu-id="b1dd0-110">ms-PKI-RA-Policies</span></span>                                                                                |
| <span data-ttu-id="b1dd0-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="b1dd0-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b1dd0-112">Attribut mspki-RA-stratégies</span><span class="sxs-lookup"><span data-stu-id="b1dd0-112">msPKI-RA-Policies</span></span>                                                                                 |
| <span data-ttu-id="b1dd0-113">Taille</span><span class="sxs-lookup"><span data-stu-id="b1dd0-113">Size</span></span>              | <span data-ttu-id="b1dd0-114">64 octets multiplié par le nombre d’entrées.</span><span class="sxs-lookup"><span data-stu-id="b1dd0-114">64 bytes times the number of entries.</span></span>                                                             |
| <span data-ttu-id="b1dd0-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="b1dd0-115">Update Privilege</span></span>  | <span data-ttu-id="b1dd0-116">Administrateur de domaine</span><span class="sxs-lookup"><span data-stu-id="b1dd0-116">Domain administrator</span></span>                                                                              |
| <span data-ttu-id="b1dd0-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="b1dd0-117">Update Frequency</span></span>  | <span data-ttu-id="b1dd0-118">Lorsque l’objet modèle de certificat (MS-PKI-Certificate-template) est modifié, créé ou cloné.</span><span class="sxs-lookup"><span data-stu-id="b1dd0-118">When the certificate template (ms-PKI-Certificate-Template) object is edited, created, or cloned.</span></span> |
| <span data-ttu-id="b1dd0-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b1dd0-119">Attribute-Id</span></span>      | <span data-ttu-id="b1dd0-120">1.2.840.113556.1.4.1438</span><span class="sxs-lookup"><span data-stu-id="b1dd0-120">1.2.840.113556.1.4.1438</span></span>                                                                           |
| <span data-ttu-id="b1dd0-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b1dd0-121">System-Id-Guid</span></span>    | <span data-ttu-id="b1dd0-122">d546ae22-0951-4d47-817e-1c9f96faad46</span><span class="sxs-lookup"><span data-stu-id="b1dd0-122">d546ae22-0951-4d47-817e-1c9f96faad46</span></span>                                                              |
| <span data-ttu-id="b1dd0-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b1dd0-123">Syntax</span></span>            | [<span data-ttu-id="b1dd0-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="b1dd0-124">**String(Unicode)**</span></span>](s-string-unicode.md)                                                       |



## <a name="implementations"></a><span data-ttu-id="b1dd0-125">Implémentations</span><span class="sxs-lookup"><span data-stu-id="b1dd0-125">Implementations</span></span>

-   [<span data-ttu-id="b1dd0-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b1dd0-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b1dd0-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b1dd0-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b1dd0-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b1dd0-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b1dd0-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b1dd0-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b1dd0-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b1dd0-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="b1dd0-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b1dd0-131">Windows Server 2003</span></span>



| <span data-ttu-id="b1dd0-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="b1dd0-132">Entry</span></span> | <span data-ttu-id="b1dd0-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="b1dd0-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="b1dd0-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b1dd0-134">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="b1dd0-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1dd0-135">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="b1dd0-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1dd0-136">System-Only</span></span>            | <span data-ttu-id="b1dd0-137">Faux</span><span class="sxs-lookup"><span data-stu-id="b1dd0-137">False</span></span>                                                                   |
| <span data-ttu-id="b1dd0-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b1dd0-138">Is-Single-Valued</span></span>       | <span data-ttu-id="b1dd0-139">Faux</span><span class="sxs-lookup"><span data-stu-id="b1dd0-139">False</span></span>                                                                   |
| <span data-ttu-id="b1dd0-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b1dd0-140">Is Indexed</span></span>             | <span data-ttu-id="b1dd0-141">Faux</span><span class="sxs-lookup"><span data-stu-id="b1dd0-141">False</span></span>                                                                   |
| <span data-ttu-id="b1dd0-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b1dd0-142">In Global Catalog</span></span>      | <span data-ttu-id="b1dd0-143">Faux</span><span class="sxs-lookup"><span data-stu-id="b1dd0-143">False</span></span>                                                                   |
| <span data-ttu-id="b1dd0-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b1dd0-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1dd0-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b1dd0-145">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="b1dd0-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1dd0-146">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="b1dd0-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1dd0-147">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="b1dd0-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1dd0-148">Search-Flags</span></span>           | <span data-ttu-id="b1dd0-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b1dd0-149">0x00000000</span></span>                                                              |
| <span data-ttu-id="b1dd0-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1dd0-150">System-Flags</span></span>           | <span data-ttu-id="b1dd0-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b1dd0-151">0x00000010</span></span>                                                              |
| <span data-ttu-id="b1dd0-152">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b1dd0-152">Classes used in</span></span>        | [<span data-ttu-id="b1dd0-153">**PKI-Certificate-modèle**</span><span class="sxs-lookup"><span data-stu-id="b1dd0-153">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b1dd0-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b1dd0-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b1dd0-155">Entrée</span><span class="sxs-lookup"><span data-stu-id="b1dd0-155">Entry</span></span> | <span data-ttu-id="b1dd0-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="b1dd0-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="b1dd0-157">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b1dd0-157">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="b1dd0-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1dd0-158">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="b1dd0-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1dd0-159">System-Only</span></span>            | <span data-ttu-id="b1dd0-160">Faux</span><span class="sxs-lookup"><span data-stu-id="b1dd0-160">False</span></span>                                                                   |
| <span data-ttu-id="b1dd0-161">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b1dd0-161">Is-Single-Valued</span></span>       | <span data-ttu-id="b1dd0-162">Faux</span><span class="sxs-lookup"><span data-stu-id="b1dd0-162">False</span></span>                                                                   |
| <span data-ttu-id="b1dd0-163">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b1dd0-163">Is Indexed</span></span>             | <span data-ttu-id="b1dd0-164">Faux</span><span class="sxs-lookup"><span data-stu-id="b1dd0-164">False</span></span>                                                                   |
| <span data-ttu-id="b1dd0-165">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b1dd0-165">In Global Catalog</span></span>      | <span data-ttu-id="b1dd0-166">Faux</span><span class="sxs-lookup"><span data-stu-id="b1dd0-166">False</span></span>                                                                   |
| <span data-ttu-id="b1dd0-167">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b1dd0-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1dd0-168">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b1dd0-168">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="b1dd0-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1dd0-169">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="b1dd0-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1dd0-170">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="b1dd0-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1dd0-171">Search-Flags</span></span>           | <span data-ttu-id="b1dd0-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b1dd0-172">0x00000000</span></span>                                                              |
| <span data-ttu-id="b1dd0-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1dd0-173">System-Flags</span></span>           | <span data-ttu-id="b1dd0-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b1dd0-174">0x00000010</span></span>                                                              |
| <span data-ttu-id="b1dd0-175">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b1dd0-175">Classes used in</span></span>        | [<span data-ttu-id="b1dd0-176">**PKI-Certificate-modèle**</span><span class="sxs-lookup"><span data-stu-id="b1dd0-176">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b1dd0-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b1dd0-177">Windows Server 2008</span></span>



| <span data-ttu-id="b1dd0-178">Entrée</span><span class="sxs-lookup"><span data-stu-id="b1dd0-178">Entry</span></span> | <span data-ttu-id="b1dd0-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="b1dd0-179">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="b1dd0-180">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b1dd0-180">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="b1dd0-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1dd0-181">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="b1dd0-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1dd0-182">System-Only</span></span>            | <span data-ttu-id="b1dd0-183">Faux</span><span class="sxs-lookup"><span data-stu-id="b1dd0-183">False</span></span>                                                                   |
| <span data-ttu-id="b1dd0-184">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b1dd0-184">Is-Single-Valued</span></span>       | <span data-ttu-id="b1dd0-185">Faux</span><span class="sxs-lookup"><span data-stu-id="b1dd0-185">False</span></span>                                                                   |
| <span data-ttu-id="b1dd0-186">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b1dd0-186">Is Indexed</span></span>             | <span data-ttu-id="b1dd0-187">Faux</span><span class="sxs-lookup"><span data-stu-id="b1dd0-187">False</span></span>                                                                   |
| <span data-ttu-id="b1dd0-188">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b1dd0-188">In Global Catalog</span></span>      | <span data-ttu-id="b1dd0-189">Faux</span><span class="sxs-lookup"><span data-stu-id="b1dd0-189">False</span></span>                                                                   |
| <span data-ttu-id="b1dd0-190">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b1dd0-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1dd0-191">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b1dd0-191">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="b1dd0-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1dd0-192">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="b1dd0-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1dd0-193">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="b1dd0-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1dd0-194">Search-Flags</span></span>           | <span data-ttu-id="b1dd0-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b1dd0-195">0x00000000</span></span>                                                              |
| <span data-ttu-id="b1dd0-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1dd0-196">System-Flags</span></span>           | <span data-ttu-id="b1dd0-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b1dd0-197">0x00000010</span></span>                                                              |
| <span data-ttu-id="b1dd0-198">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b1dd0-198">Classes used in</span></span>        | [<span data-ttu-id="b1dd0-199">**PKI-Certificate-modèle**</span><span class="sxs-lookup"><span data-stu-id="b1dd0-199">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b1dd0-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b1dd0-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b1dd0-201">Entrée</span><span class="sxs-lookup"><span data-stu-id="b1dd0-201">Entry</span></span> | <span data-ttu-id="b1dd0-202">Valeur</span><span class="sxs-lookup"><span data-stu-id="b1dd0-202">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="b1dd0-203">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b1dd0-203">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="b1dd0-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1dd0-204">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="b1dd0-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1dd0-205">System-Only</span></span>            | <span data-ttu-id="b1dd0-206">Faux</span><span class="sxs-lookup"><span data-stu-id="b1dd0-206">False</span></span>                                                                   |
| <span data-ttu-id="b1dd0-207">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b1dd0-207">Is-Single-Valued</span></span>       | <span data-ttu-id="b1dd0-208">Faux</span><span class="sxs-lookup"><span data-stu-id="b1dd0-208">False</span></span>                                                                   |
| <span data-ttu-id="b1dd0-209">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b1dd0-209">Is Indexed</span></span>             | <span data-ttu-id="b1dd0-210">Faux</span><span class="sxs-lookup"><span data-stu-id="b1dd0-210">False</span></span>                                                                   |
| <span data-ttu-id="b1dd0-211">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b1dd0-211">In Global Catalog</span></span>      | <span data-ttu-id="b1dd0-212">Faux</span><span class="sxs-lookup"><span data-stu-id="b1dd0-212">False</span></span>                                                                   |
| <span data-ttu-id="b1dd0-213">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b1dd0-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1dd0-214">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b1dd0-214">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="b1dd0-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1dd0-215">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="b1dd0-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1dd0-216">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="b1dd0-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1dd0-217">Search-Flags</span></span>           | <span data-ttu-id="b1dd0-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b1dd0-218">0x00000000</span></span>                                                              |
| <span data-ttu-id="b1dd0-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1dd0-219">System-Flags</span></span>           | <span data-ttu-id="b1dd0-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b1dd0-220">0x00000010</span></span>                                                              |
| <span data-ttu-id="b1dd0-221">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b1dd0-221">Classes used in</span></span>        | [<span data-ttu-id="b1dd0-222">**PKI-Certificate-modèle**</span><span class="sxs-lookup"><span data-stu-id="b1dd0-222">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b1dd0-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b1dd0-223">Windows Server 2012</span></span>



| <span data-ttu-id="b1dd0-224">Entrée</span><span class="sxs-lookup"><span data-stu-id="b1dd0-224">Entry</span></span> | <span data-ttu-id="b1dd0-225">Valeur</span><span class="sxs-lookup"><span data-stu-id="b1dd0-225">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="b1dd0-226">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b1dd0-226">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="b1dd0-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1dd0-227">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="b1dd0-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1dd0-228">System-Only</span></span>            | <span data-ttu-id="b1dd0-229">Faux</span><span class="sxs-lookup"><span data-stu-id="b1dd0-229">False</span></span>                                                                   |
| <span data-ttu-id="b1dd0-230">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b1dd0-230">Is-Single-Valued</span></span>       | <span data-ttu-id="b1dd0-231">Faux</span><span class="sxs-lookup"><span data-stu-id="b1dd0-231">False</span></span>                                                                   |
| <span data-ttu-id="b1dd0-232">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b1dd0-232">Is Indexed</span></span>             | <span data-ttu-id="b1dd0-233">Faux</span><span class="sxs-lookup"><span data-stu-id="b1dd0-233">False</span></span>                                                                   |
| <span data-ttu-id="b1dd0-234">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b1dd0-234">In Global Catalog</span></span>      | <span data-ttu-id="b1dd0-235">Faux</span><span class="sxs-lookup"><span data-stu-id="b1dd0-235">False</span></span>                                                                   |
| <span data-ttu-id="b1dd0-236">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b1dd0-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1dd0-237">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b1dd0-237">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="b1dd0-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1dd0-238">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="b1dd0-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1dd0-239">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="b1dd0-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1dd0-240">Search-Flags</span></span>           | <span data-ttu-id="b1dd0-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b1dd0-241">0x00000000</span></span>                                                              |
| <span data-ttu-id="b1dd0-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1dd0-242">System-Flags</span></span>           | <span data-ttu-id="b1dd0-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b1dd0-243">0x00000010</span></span>                                                              |
| <span data-ttu-id="b1dd0-244">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b1dd0-244">Classes used in</span></span>        | [<span data-ttu-id="b1dd0-245">**PKI-Certificate-modèle**</span><span class="sxs-lookup"><span data-stu-id="b1dd0-245">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 





