---
title: Attribut Authentication-Options
description: Options d’authentification utilisées dans l’interface ADSI pour la liaison aux objets des services d’annuaire.
ms.assetid: a6dc4591-d825-456a-8f77-78cb3c91af9f
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Authentication-Options
- Schéma AD de l’attribut authenticationOptions
topic_type:
- apiref
api_name:
- Authentication-Options
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cfa9c422dfe196ab002c02c361759461f43965d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107293"
---
# <a name="authentication-options-attribute"></a><span data-ttu-id="47308-105">Attribut Authentication-Options</span><span class="sxs-lookup"><span data-stu-id="47308-105">Authentication-Options attribute</span></span>

<span data-ttu-id="47308-106">Options d’authentification utilisées dans l’interface ADSI pour la liaison aux objets des services d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="47308-106">The authentication options used in ADSI to bind to directory services objects.</span></span>



| <span data-ttu-id="47308-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="47308-107">Entry</span></span> | <span data-ttu-id="47308-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="47308-108">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47308-109">CN</span><span class="sxs-lookup"><span data-stu-id="47308-109">CN</span></span>                | <span data-ttu-id="47308-110">Authentication-Options</span><span class="sxs-lookup"><span data-stu-id="47308-110">Authentication-Options</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="47308-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="47308-111">Ldap-Display-Name</span></span> | <span data-ttu-id="47308-112">authenticationOptions</span><span class="sxs-lookup"><span data-stu-id="47308-112">authenticationOptions</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="47308-113">Taille</span><span class="sxs-lookup"><span data-stu-id="47308-113">Size</span></span>              | <span data-ttu-id="47308-114">4 octets.</span><span class="sxs-lookup"><span data-stu-id="47308-114">4 bytes.</span></span> <span data-ttu-id="47308-115">Valeurs définies dans IADS. h : \_ authentification sécurisée des publicités \_ 0x1, annonces \_ utiliser le \_ chiffrement 0X2, ad \_ use \_ SSL 0X2, ADS \_ ReadOnly \_ Server 0x4, \_ \_ informations d’identification de l’invite ADS, informations d’identification ADS, ad \_ no \_ Authentication 0x10, ADS \_ Fast \_ Bind 0x20, ad \_ use \_ Signing 0x40 \_ \_</span><span class="sxs-lookup"><span data-stu-id="47308-115">Values defined in IADS.h: ADS\_SECURE\_AUTHENTICATION 0x1, ADS\_USE\_ENCRYPTION 0x2, ADS\_USE\_SSL 0x2, ADS\_READONLY\_SERVER 0x4, ADS\_PROMPT\_CREDENTIALS 0x8, ADS\_NO\_AUTHENTICATION 0x10, ADS\_FAST\_BIND 0x20, ADS\_USE\_SIGNING 0x40, ADS\_USE\_SEALING 0x80</span></span> |
| <span data-ttu-id="47308-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="47308-116">Update Privilege</span></span>  | \-                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="47308-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="47308-117">Update Frequency</span></span>  | \-                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="47308-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="47308-118">Attribute-Id</span></span>      | <span data-ttu-id="47308-119">1.2.840.113556.1.4.11</span><span class="sxs-lookup"><span data-stu-id="47308-119">1.2.840.113556.1.4.11</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="47308-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="47308-120">System-Id-Guid</span></span>    | <span data-ttu-id="47308-121">bf967928-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="47308-121">bf967928-0de6-11d0-a285-00aa003049e2</span></span>                                                                                                                                                                                                                                         |
| <span data-ttu-id="47308-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="47308-122">Syntax</span></span>            | [<span data-ttu-id="47308-123">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="47308-123">**Enumeration**</span></span>](s-enumeration.md)                                                                                                                                                                                                                                         |



## <a name="implementations"></a><span data-ttu-id="47308-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="47308-124">Implementations</span></span>

-   [<span data-ttu-id="47308-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="47308-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="47308-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="47308-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="47308-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="47308-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="47308-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="47308-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="47308-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="47308-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="47308-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="47308-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="47308-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="47308-131">Windows 2000 Server</span></span>



| <span data-ttu-id="47308-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="47308-132">Entry</span></span> | <span data-ttu-id="47308-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="47308-133">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="47308-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="47308-134">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="47308-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="47308-135">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="47308-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="47308-136">System-Only</span></span>            | <span data-ttu-id="47308-137">Faux</span><span class="sxs-lookup"><span data-stu-id="47308-137">False</span></span>                                              |
| <span data-ttu-id="47308-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="47308-138">Is-Single-Valued</span></span>       | <span data-ttu-id="47308-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="47308-139">True</span></span>                                               |
| <span data-ttu-id="47308-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="47308-140">Is Indexed</span></span>             | <span data-ttu-id="47308-141">Faux</span><span class="sxs-lookup"><span data-stu-id="47308-141">False</span></span>                                              |
| <span data-ttu-id="47308-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="47308-142">In Global Catalog</span></span>      | <span data-ttu-id="47308-143">Faux</span><span class="sxs-lookup"><span data-stu-id="47308-143">False</span></span>                                              |
| <span data-ttu-id="47308-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="47308-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="47308-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="47308-145">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="47308-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="47308-146">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="47308-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="47308-147">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="47308-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="47308-148">Search-Flags</span></span>           | <span data-ttu-id="47308-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="47308-149">0x00000000</span></span>                                         |
| <span data-ttu-id="47308-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="47308-150">System-Flags</span></span>           | <span data-ttu-id="47308-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="47308-151">0x00000010</span></span>                                         |
| <span data-ttu-id="47308-152">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="47308-152">Classes used in</span></span>        | [<span data-ttu-id="47308-153">**Stratégie de domaine**</span><span class="sxs-lookup"><span data-stu-id="47308-153">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="47308-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="47308-154">Windows Server 2003</span></span>



| <span data-ttu-id="47308-155">Entrée</span><span class="sxs-lookup"><span data-stu-id="47308-155">Entry</span></span> | <span data-ttu-id="47308-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="47308-156">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="47308-157">ID de lien</span><span class="sxs-lookup"><span data-stu-id="47308-157">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="47308-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="47308-158">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="47308-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="47308-159">System-Only</span></span>            | <span data-ttu-id="47308-160">Faux</span><span class="sxs-lookup"><span data-stu-id="47308-160">False</span></span>                                              |
| <span data-ttu-id="47308-161">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="47308-161">Is-Single-Valued</span></span>       | <span data-ttu-id="47308-162">Vrai</span><span class="sxs-lookup"><span data-stu-id="47308-162">True</span></span>                                               |
| <span data-ttu-id="47308-163">Est indexé</span><span class="sxs-lookup"><span data-stu-id="47308-163">Is Indexed</span></span>             | <span data-ttu-id="47308-164">Faux</span><span class="sxs-lookup"><span data-stu-id="47308-164">False</span></span>                                              |
| <span data-ttu-id="47308-165">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="47308-165">In Global Catalog</span></span>      | <span data-ttu-id="47308-166">Faux</span><span class="sxs-lookup"><span data-stu-id="47308-166">False</span></span>                                              |
| <span data-ttu-id="47308-167">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="47308-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="47308-168">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="47308-168">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="47308-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="47308-169">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="47308-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="47308-170">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="47308-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="47308-171">Search-Flags</span></span>           | <span data-ttu-id="47308-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="47308-172">0x00000000</span></span>                                         |
| <span data-ttu-id="47308-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="47308-173">System-Flags</span></span>           | <span data-ttu-id="47308-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="47308-174">0x00000010</span></span>                                         |
| <span data-ttu-id="47308-175">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="47308-175">Classes used in</span></span>        | [<span data-ttu-id="47308-176">**Stratégie de domaine**</span><span class="sxs-lookup"><span data-stu-id="47308-176">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="47308-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="47308-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="47308-178">Entrée</span><span class="sxs-lookup"><span data-stu-id="47308-178">Entry</span></span> | <span data-ttu-id="47308-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="47308-179">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="47308-180">ID de lien</span><span class="sxs-lookup"><span data-stu-id="47308-180">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="47308-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="47308-181">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="47308-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="47308-182">System-Only</span></span>            | <span data-ttu-id="47308-183">Faux</span><span class="sxs-lookup"><span data-stu-id="47308-183">False</span></span>                                              |
| <span data-ttu-id="47308-184">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="47308-184">Is-Single-Valued</span></span>       | <span data-ttu-id="47308-185">Vrai</span><span class="sxs-lookup"><span data-stu-id="47308-185">True</span></span>                                               |
| <span data-ttu-id="47308-186">Est indexé</span><span class="sxs-lookup"><span data-stu-id="47308-186">Is Indexed</span></span>             | <span data-ttu-id="47308-187">Faux</span><span class="sxs-lookup"><span data-stu-id="47308-187">False</span></span>                                              |
| <span data-ttu-id="47308-188">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="47308-188">In Global Catalog</span></span>      | <span data-ttu-id="47308-189">Faux</span><span class="sxs-lookup"><span data-stu-id="47308-189">False</span></span>                                              |
| <span data-ttu-id="47308-190">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="47308-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="47308-191">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="47308-191">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="47308-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="47308-192">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="47308-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="47308-193">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="47308-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="47308-194">Search-Flags</span></span>           | <span data-ttu-id="47308-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="47308-195">0x00000000</span></span>                                         |
| <span data-ttu-id="47308-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="47308-196">System-Flags</span></span>           | <span data-ttu-id="47308-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="47308-197">0x00000010</span></span>                                         |
| <span data-ttu-id="47308-198">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="47308-198">Classes used in</span></span>        | [<span data-ttu-id="47308-199">**Stratégie de domaine**</span><span class="sxs-lookup"><span data-stu-id="47308-199">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="47308-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="47308-200">Windows Server 2008</span></span>



| <span data-ttu-id="47308-201">Entrée</span><span class="sxs-lookup"><span data-stu-id="47308-201">Entry</span></span> | <span data-ttu-id="47308-202">Valeur</span><span class="sxs-lookup"><span data-stu-id="47308-202">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="47308-203">ID de lien</span><span class="sxs-lookup"><span data-stu-id="47308-203">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="47308-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="47308-204">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="47308-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="47308-205">System-Only</span></span>            | <span data-ttu-id="47308-206">Faux</span><span class="sxs-lookup"><span data-stu-id="47308-206">False</span></span>                                              |
| <span data-ttu-id="47308-207">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="47308-207">Is-Single-Valued</span></span>       | <span data-ttu-id="47308-208">Vrai</span><span class="sxs-lookup"><span data-stu-id="47308-208">True</span></span>                                               |
| <span data-ttu-id="47308-209">Est indexé</span><span class="sxs-lookup"><span data-stu-id="47308-209">Is Indexed</span></span>             | <span data-ttu-id="47308-210">Faux</span><span class="sxs-lookup"><span data-stu-id="47308-210">False</span></span>                                              |
| <span data-ttu-id="47308-211">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="47308-211">In Global Catalog</span></span>      | <span data-ttu-id="47308-212">Faux</span><span class="sxs-lookup"><span data-stu-id="47308-212">False</span></span>                                              |
| <span data-ttu-id="47308-213">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="47308-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="47308-214">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="47308-214">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="47308-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="47308-215">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="47308-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="47308-216">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="47308-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="47308-217">Search-Flags</span></span>           | <span data-ttu-id="47308-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="47308-218">0x00000000</span></span>                                         |
| <span data-ttu-id="47308-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="47308-219">System-Flags</span></span>           | <span data-ttu-id="47308-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="47308-220">0x00000010</span></span>                                         |
| <span data-ttu-id="47308-221">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="47308-221">Classes used in</span></span>        | [<span data-ttu-id="47308-222">**Stratégie de domaine**</span><span class="sxs-lookup"><span data-stu-id="47308-222">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="47308-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="47308-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="47308-224">Entrée</span><span class="sxs-lookup"><span data-stu-id="47308-224">Entry</span></span> | <span data-ttu-id="47308-225">Valeur</span><span class="sxs-lookup"><span data-stu-id="47308-225">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="47308-226">ID de lien</span><span class="sxs-lookup"><span data-stu-id="47308-226">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="47308-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="47308-227">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="47308-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="47308-228">System-Only</span></span>            | <span data-ttu-id="47308-229">Faux</span><span class="sxs-lookup"><span data-stu-id="47308-229">False</span></span>                                              |
| <span data-ttu-id="47308-230">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="47308-230">Is-Single-Valued</span></span>       | <span data-ttu-id="47308-231">Vrai</span><span class="sxs-lookup"><span data-stu-id="47308-231">True</span></span>                                               |
| <span data-ttu-id="47308-232">Est indexé</span><span class="sxs-lookup"><span data-stu-id="47308-232">Is Indexed</span></span>             | <span data-ttu-id="47308-233">Faux</span><span class="sxs-lookup"><span data-stu-id="47308-233">False</span></span>                                              |
| <span data-ttu-id="47308-234">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="47308-234">In Global Catalog</span></span>      | <span data-ttu-id="47308-235">Faux</span><span class="sxs-lookup"><span data-stu-id="47308-235">False</span></span>                                              |
| <span data-ttu-id="47308-236">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="47308-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="47308-237">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="47308-237">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="47308-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="47308-238">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="47308-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="47308-239">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="47308-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="47308-240">Search-Flags</span></span>           | <span data-ttu-id="47308-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="47308-241">0x00000000</span></span>                                         |
| <span data-ttu-id="47308-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="47308-242">System-Flags</span></span>           | <span data-ttu-id="47308-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="47308-243">0x00000010</span></span>                                         |
| <span data-ttu-id="47308-244">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="47308-244">Classes used in</span></span>        | [<span data-ttu-id="47308-245">**Stratégie de domaine**</span><span class="sxs-lookup"><span data-stu-id="47308-245">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="47308-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="47308-246">Windows Server 2012</span></span>



| <span data-ttu-id="47308-247">Entrée</span><span class="sxs-lookup"><span data-stu-id="47308-247">Entry</span></span> | <span data-ttu-id="47308-248">Valeur</span><span class="sxs-lookup"><span data-stu-id="47308-248">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="47308-249">ID de lien</span><span class="sxs-lookup"><span data-stu-id="47308-249">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="47308-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="47308-250">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="47308-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="47308-251">System-Only</span></span>            | <span data-ttu-id="47308-252">Faux</span><span class="sxs-lookup"><span data-stu-id="47308-252">False</span></span>                                              |
| <span data-ttu-id="47308-253">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="47308-253">Is-Single-Valued</span></span>       | <span data-ttu-id="47308-254">Vrai</span><span class="sxs-lookup"><span data-stu-id="47308-254">True</span></span>                                               |
| <span data-ttu-id="47308-255">Est indexé</span><span class="sxs-lookup"><span data-stu-id="47308-255">Is Indexed</span></span>             | <span data-ttu-id="47308-256">Faux</span><span class="sxs-lookup"><span data-stu-id="47308-256">False</span></span>                                              |
| <span data-ttu-id="47308-257">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="47308-257">In Global Catalog</span></span>      | <span data-ttu-id="47308-258">Faux</span><span class="sxs-lookup"><span data-stu-id="47308-258">False</span></span>                                              |
| <span data-ttu-id="47308-259">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="47308-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="47308-260">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="47308-260">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="47308-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="47308-261">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="47308-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="47308-262">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="47308-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="47308-263">Search-Flags</span></span>           | <span data-ttu-id="47308-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="47308-264">0x00000000</span></span>                                         |
| <span data-ttu-id="47308-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="47308-265">System-Flags</span></span>           | <span data-ttu-id="47308-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="47308-266">0x00000010</span></span>                                         |
| <span data-ttu-id="47308-267">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="47308-267">Classes used in</span></span>        | [<span data-ttu-id="47308-268">**Stratégie de domaine**</span><span class="sxs-lookup"><span data-stu-id="47308-268">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



 

 





