---
title: PKI-attribut d’utilisation de clé étendue
description: OID de l’utilisation améliorée de la clé pour le modèle de certificat.
ms.assetid: 2e2b55a0-6c55-481d-9ebf-9c204e7fe030
ms.tgt_platform: multiple
keywords:
- PKI-attribut d’utilisation de clé étendue-schéma Active Directory
- Schéma AD de l’attribut pKIExtendedKeyUsage
topic_type:
- apiref
api_name:
- PKI-Extended-Key-Usage
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cc138a90100f89496dc4076235a1cc4161c1694
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106510376"
---
# <a name="pki-extended-key-usage-attribute"></a><span data-ttu-id="b8c8d-105">PKI-attribut d’utilisation de clé étendue</span><span class="sxs-lookup"><span data-stu-id="b8c8d-105">PKI-Extended-Key-Usage attribute</span></span>

<span data-ttu-id="b8c8d-106">OID de l’utilisation améliorée de la clé pour le modèle de certificat.</span><span class="sxs-lookup"><span data-stu-id="b8c8d-106">The enhanced key usage OIDs for the certificate template.</span></span>



| <span data-ttu-id="b8c8d-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="b8c8d-107">Entry</span></span> | <span data-ttu-id="b8c8d-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="b8c8d-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="b8c8d-109">CN</span><span class="sxs-lookup"><span data-stu-id="b8c8d-109">CN</span></span>                | <span data-ttu-id="b8c8d-110">Infrastructure à clé publique-étendue-utilisation</span><span class="sxs-lookup"><span data-stu-id="b8c8d-110">PKI-Extended-Key-Usage</span></span>                      |
| <span data-ttu-id="b8c8d-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="b8c8d-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b8c8d-112">pKIExtendedKeyUsage</span><span class="sxs-lookup"><span data-stu-id="b8c8d-112">pKIExtendedKeyUsage</span></span>                         |
| <span data-ttu-id="b8c8d-113">Taille</span><span class="sxs-lookup"><span data-stu-id="b8c8d-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="b8c8d-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="b8c8d-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="b8c8d-115">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="b8c8d-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="b8c8d-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b8c8d-116">Attribute-Id</span></span>      | <span data-ttu-id="b8c8d-117">1.2.840.113556.1.4.1333</span><span class="sxs-lookup"><span data-stu-id="b8c8d-117">1.2.840.113556.1.4.1333</span></span>                     |
| <span data-ttu-id="b8c8d-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b8c8d-118">System-Id-Guid</span></span>    | <span data-ttu-id="b8c8d-119">18976af6-3b9e-11d2-90cc-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="b8c8d-119">18976af6-3b9e-11d2-90cc-00c04fd91ab1</span></span>        |
| <span data-ttu-id="b8c8d-120">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b8c8d-120">Syntax</span></span>            | [<span data-ttu-id="b8c8d-121">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="b8c8d-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="b8c8d-122">Implémentations</span><span class="sxs-lookup"><span data-stu-id="b8c8d-122">Implementations</span></span>

-   [<span data-ttu-id="b8c8d-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b8c8d-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b8c8d-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b8c8d-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b8c8d-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b8c8d-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b8c8d-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b8c8d-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b8c8d-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b8c8d-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b8c8d-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b8c8d-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b8c8d-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b8c8d-129">Windows 2000 Server</span></span>



| <span data-ttu-id="b8c8d-130">Entrée</span><span class="sxs-lookup"><span data-stu-id="b8c8d-130">Entry</span></span> | <span data-ttu-id="b8c8d-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="b8c8d-131">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="b8c8d-132">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b8c8d-132">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="b8c8d-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8c8d-133">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="b8c8d-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8c8d-134">System-Only</span></span>            | <span data-ttu-id="b8c8d-135">Faux</span><span class="sxs-lookup"><span data-stu-id="b8c8d-135">False</span></span>                                                                   |
| <span data-ttu-id="b8c8d-136">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b8c8d-136">Is-Single-Valued</span></span>       | <span data-ttu-id="b8c8d-137">Faux</span><span class="sxs-lookup"><span data-stu-id="b8c8d-137">False</span></span>                                                                   |
| <span data-ttu-id="b8c8d-138">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b8c8d-138">Is Indexed</span></span>             | <span data-ttu-id="b8c8d-139">Faux</span><span class="sxs-lookup"><span data-stu-id="b8c8d-139">False</span></span>                                                                   |
| <span data-ttu-id="b8c8d-140">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b8c8d-140">In Global Catalog</span></span>      | <span data-ttu-id="b8c8d-141">Vrai</span><span class="sxs-lookup"><span data-stu-id="b8c8d-141">True</span></span>                                                                    |
| <span data-ttu-id="b8c8d-142">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b8c8d-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8c8d-143">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b8c8d-143">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="b8c8d-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8c8d-144">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="b8c8d-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8c8d-145">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="b8c8d-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8c8d-146">Search-Flags</span></span>           | <span data-ttu-id="b8c8d-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b8c8d-147">0x00000000</span></span>                                                              |
| <span data-ttu-id="b8c8d-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8c8d-148">System-Flags</span></span>           | <span data-ttu-id="b8c8d-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b8c8d-149">0x00000010</span></span>                                                              |
| <span data-ttu-id="b8c8d-150">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b8c8d-150">Classes used in</span></span>        | [<span data-ttu-id="b8c8d-151">**PKI-Certificate-modèle**</span><span class="sxs-lookup"><span data-stu-id="b8c8d-151">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b8c8d-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b8c8d-152">Windows Server 2003</span></span>



| <span data-ttu-id="b8c8d-153">Entrée</span><span class="sxs-lookup"><span data-stu-id="b8c8d-153">Entry</span></span> | <span data-ttu-id="b8c8d-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="b8c8d-154">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="b8c8d-155">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b8c8d-155">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="b8c8d-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8c8d-156">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="b8c8d-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8c8d-157">System-Only</span></span>            | <span data-ttu-id="b8c8d-158">Faux</span><span class="sxs-lookup"><span data-stu-id="b8c8d-158">False</span></span>                                                                   |
| <span data-ttu-id="b8c8d-159">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b8c8d-159">Is-Single-Valued</span></span>       | <span data-ttu-id="b8c8d-160">Faux</span><span class="sxs-lookup"><span data-stu-id="b8c8d-160">False</span></span>                                                                   |
| <span data-ttu-id="b8c8d-161">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b8c8d-161">Is Indexed</span></span>             | <span data-ttu-id="b8c8d-162">Faux</span><span class="sxs-lookup"><span data-stu-id="b8c8d-162">False</span></span>                                                                   |
| <span data-ttu-id="b8c8d-163">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b8c8d-163">In Global Catalog</span></span>      | <span data-ttu-id="b8c8d-164">Vrai</span><span class="sxs-lookup"><span data-stu-id="b8c8d-164">True</span></span>                                                                    |
| <span data-ttu-id="b8c8d-165">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b8c8d-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8c8d-166">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b8c8d-166">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="b8c8d-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8c8d-167">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="b8c8d-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8c8d-168">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="b8c8d-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8c8d-169">Search-Flags</span></span>           | <span data-ttu-id="b8c8d-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b8c8d-170">0x00000000</span></span>                                                              |
| <span data-ttu-id="b8c8d-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8c8d-171">System-Flags</span></span>           | <span data-ttu-id="b8c8d-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b8c8d-172">0x00000010</span></span>                                                              |
| <span data-ttu-id="b8c8d-173">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b8c8d-173">Classes used in</span></span>        | [<span data-ttu-id="b8c8d-174">**PKI-Certificate-modèle**</span><span class="sxs-lookup"><span data-stu-id="b8c8d-174">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b8c8d-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b8c8d-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b8c8d-176">Entrée</span><span class="sxs-lookup"><span data-stu-id="b8c8d-176">Entry</span></span> | <span data-ttu-id="b8c8d-177">Valeur</span><span class="sxs-lookup"><span data-stu-id="b8c8d-177">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="b8c8d-178">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b8c8d-178">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="b8c8d-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8c8d-179">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="b8c8d-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8c8d-180">System-Only</span></span>            | <span data-ttu-id="b8c8d-181">Faux</span><span class="sxs-lookup"><span data-stu-id="b8c8d-181">False</span></span>                                                                   |
| <span data-ttu-id="b8c8d-182">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b8c8d-182">Is-Single-Valued</span></span>       | <span data-ttu-id="b8c8d-183">Faux</span><span class="sxs-lookup"><span data-stu-id="b8c8d-183">False</span></span>                                                                   |
| <span data-ttu-id="b8c8d-184">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b8c8d-184">Is Indexed</span></span>             | <span data-ttu-id="b8c8d-185">Faux</span><span class="sxs-lookup"><span data-stu-id="b8c8d-185">False</span></span>                                                                   |
| <span data-ttu-id="b8c8d-186">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b8c8d-186">In Global Catalog</span></span>      | <span data-ttu-id="b8c8d-187">Vrai</span><span class="sxs-lookup"><span data-stu-id="b8c8d-187">True</span></span>                                                                    |
| <span data-ttu-id="b8c8d-188">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b8c8d-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8c8d-189">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b8c8d-189">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="b8c8d-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8c8d-190">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="b8c8d-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8c8d-191">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="b8c8d-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8c8d-192">Search-Flags</span></span>           | <span data-ttu-id="b8c8d-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b8c8d-193">0x00000000</span></span>                                                              |
| <span data-ttu-id="b8c8d-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8c8d-194">System-Flags</span></span>           | <span data-ttu-id="b8c8d-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b8c8d-195">0x00000010</span></span>                                                              |
| <span data-ttu-id="b8c8d-196">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b8c8d-196">Classes used in</span></span>        | [<span data-ttu-id="b8c8d-197">**PKI-Certificate-modèle**</span><span class="sxs-lookup"><span data-stu-id="b8c8d-197">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b8c8d-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b8c8d-198">Windows Server 2008</span></span>



| <span data-ttu-id="b8c8d-199">Entrée</span><span class="sxs-lookup"><span data-stu-id="b8c8d-199">Entry</span></span> | <span data-ttu-id="b8c8d-200">Valeur</span><span class="sxs-lookup"><span data-stu-id="b8c8d-200">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="b8c8d-201">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b8c8d-201">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="b8c8d-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8c8d-202">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="b8c8d-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8c8d-203">System-Only</span></span>            | <span data-ttu-id="b8c8d-204">Faux</span><span class="sxs-lookup"><span data-stu-id="b8c8d-204">False</span></span>                                                                   |
| <span data-ttu-id="b8c8d-205">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b8c8d-205">Is-Single-Valued</span></span>       | <span data-ttu-id="b8c8d-206">Faux</span><span class="sxs-lookup"><span data-stu-id="b8c8d-206">False</span></span>                                                                   |
| <span data-ttu-id="b8c8d-207">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b8c8d-207">Is Indexed</span></span>             | <span data-ttu-id="b8c8d-208">Faux</span><span class="sxs-lookup"><span data-stu-id="b8c8d-208">False</span></span>                                                                   |
| <span data-ttu-id="b8c8d-209">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b8c8d-209">In Global Catalog</span></span>      | <span data-ttu-id="b8c8d-210">Vrai</span><span class="sxs-lookup"><span data-stu-id="b8c8d-210">True</span></span>                                                                    |
| <span data-ttu-id="b8c8d-211">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b8c8d-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8c8d-212">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b8c8d-212">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="b8c8d-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8c8d-213">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="b8c8d-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8c8d-214">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="b8c8d-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8c8d-215">Search-Flags</span></span>           | <span data-ttu-id="b8c8d-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b8c8d-216">0x00000000</span></span>                                                              |
| <span data-ttu-id="b8c8d-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8c8d-217">System-Flags</span></span>           | <span data-ttu-id="b8c8d-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b8c8d-218">0x00000010</span></span>                                                              |
| <span data-ttu-id="b8c8d-219">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b8c8d-219">Classes used in</span></span>        | [<span data-ttu-id="b8c8d-220">**PKI-Certificate-modèle**</span><span class="sxs-lookup"><span data-stu-id="b8c8d-220">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b8c8d-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b8c8d-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b8c8d-222">Entrée</span><span class="sxs-lookup"><span data-stu-id="b8c8d-222">Entry</span></span> | <span data-ttu-id="b8c8d-223">Valeur</span><span class="sxs-lookup"><span data-stu-id="b8c8d-223">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="b8c8d-224">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b8c8d-224">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="b8c8d-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8c8d-225">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="b8c8d-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8c8d-226">System-Only</span></span>            | <span data-ttu-id="b8c8d-227">Faux</span><span class="sxs-lookup"><span data-stu-id="b8c8d-227">False</span></span>                                                                   |
| <span data-ttu-id="b8c8d-228">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b8c8d-228">Is-Single-Valued</span></span>       | <span data-ttu-id="b8c8d-229">Faux</span><span class="sxs-lookup"><span data-stu-id="b8c8d-229">False</span></span>                                                                   |
| <span data-ttu-id="b8c8d-230">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b8c8d-230">Is Indexed</span></span>             | <span data-ttu-id="b8c8d-231">Faux</span><span class="sxs-lookup"><span data-stu-id="b8c8d-231">False</span></span>                                                                   |
| <span data-ttu-id="b8c8d-232">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b8c8d-232">In Global Catalog</span></span>      | <span data-ttu-id="b8c8d-233">Vrai</span><span class="sxs-lookup"><span data-stu-id="b8c8d-233">True</span></span>                                                                    |
| <span data-ttu-id="b8c8d-234">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b8c8d-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8c8d-235">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b8c8d-235">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="b8c8d-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8c8d-236">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="b8c8d-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8c8d-237">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="b8c8d-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8c8d-238">Search-Flags</span></span>           | <span data-ttu-id="b8c8d-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b8c8d-239">0x00000000</span></span>                                                              |
| <span data-ttu-id="b8c8d-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8c8d-240">System-Flags</span></span>           | <span data-ttu-id="b8c8d-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b8c8d-241">0x00000010</span></span>                                                              |
| <span data-ttu-id="b8c8d-242">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b8c8d-242">Classes used in</span></span>        | [<span data-ttu-id="b8c8d-243">**PKI-Certificate-modèle**</span><span class="sxs-lookup"><span data-stu-id="b8c8d-243">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b8c8d-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b8c8d-244">Windows Server 2012</span></span>



| <span data-ttu-id="b8c8d-245">Entrée</span><span class="sxs-lookup"><span data-stu-id="b8c8d-245">Entry</span></span> | <span data-ttu-id="b8c8d-246">Valeur</span><span class="sxs-lookup"><span data-stu-id="b8c8d-246">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="b8c8d-247">ID de lien</span><span class="sxs-lookup"><span data-stu-id="b8c8d-247">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="b8c8d-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8c8d-248">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="b8c8d-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8c8d-249">System-Only</span></span>            | <span data-ttu-id="b8c8d-250">Faux</span><span class="sxs-lookup"><span data-stu-id="b8c8d-250">False</span></span>                                                                   |
| <span data-ttu-id="b8c8d-251">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="b8c8d-251">Is-Single-Valued</span></span>       | <span data-ttu-id="b8c8d-252">Faux</span><span class="sxs-lookup"><span data-stu-id="b8c8d-252">False</span></span>                                                                   |
| <span data-ttu-id="b8c8d-253">Est indexé</span><span class="sxs-lookup"><span data-stu-id="b8c8d-253">Is Indexed</span></span>             | <span data-ttu-id="b8c8d-254">Faux</span><span class="sxs-lookup"><span data-stu-id="b8c8d-254">False</span></span>                                                                   |
| <span data-ttu-id="b8c8d-255">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="b8c8d-255">In Global Catalog</span></span>      | <span data-ttu-id="b8c8d-256">Vrai</span><span class="sxs-lookup"><span data-stu-id="b8c8d-256">True</span></span>                                                                    |
| <span data-ttu-id="b8c8d-257">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="b8c8d-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8c8d-258">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="b8c8d-258">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="b8c8d-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8c8d-259">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="b8c8d-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8c8d-260">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="b8c8d-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8c8d-261">Search-Flags</span></span>           | <span data-ttu-id="b8c8d-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b8c8d-262">0x00000000</span></span>                                                              |
| <span data-ttu-id="b8c8d-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8c8d-263">System-Flags</span></span>           | <span data-ttu-id="b8c8d-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b8c8d-264">0x00000010</span></span>                                                              |
| <span data-ttu-id="b8c8d-265">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="b8c8d-265">Classes used in</span></span>        | [<span data-ttu-id="b8c8d-266">**PKI-Certificate-modèle**</span><span class="sxs-lookup"><span data-stu-id="b8c8d-266">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 





