---
title: Attribut alt-Security-Identities
description: Contient des mappages pour les certificats X. 509 ou des comptes d’utilisateur Kerberos externes à cet utilisateur à des fins d’authentification.
ms.assetid: 40b2af9c-fd4f-4883-8494-2b64682ee50c
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory de Alt-Security-Identities Attribute
- Schéma AD de l’attribut altSecurityIdentities
topic_type:
- apiref
api_name:
- Alt-Security-Identities
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2548e337f29778400bb173a8c15d928d7b06d988
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103943052"
---
# <a name="alt-security-identities-attribute"></a><span data-ttu-id="8faff-105">Attribut alt-Security-Identities</span><span class="sxs-lookup"><span data-stu-id="8faff-105">Alt-Security-Identities attribute</span></span>

<span data-ttu-id="8faff-106">Contient des mappages pour les certificats X. 509 ou des comptes d’utilisateur Kerberos externes à cet utilisateur à des fins d’authentification.</span><span class="sxs-lookup"><span data-stu-id="8faff-106">Contains mappings for X.509 certificates or external Kerberos user accounts to this user for the purpose of authentication.</span></span>



| <span data-ttu-id="8faff-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="8faff-107">Entry</span></span> | <span data-ttu-id="8faff-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="8faff-108">Value</span></span> |
|-------------------|-----------------------------------------------------|
| <span data-ttu-id="8faff-109">CN</span><span class="sxs-lookup"><span data-stu-id="8faff-109">CN</span></span>                | <span data-ttu-id="8faff-110">Alt-sécurité-identités</span><span class="sxs-lookup"><span data-stu-id="8faff-110">Alt-Security-Identities</span></span>                             |
| <span data-ttu-id="8faff-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="8faff-111">Ldap-Display-Name</span></span> | <span data-ttu-id="8faff-112">altSecurityIdentities</span><span class="sxs-lookup"><span data-stu-id="8faff-112">altSecurityIdentities</span></span>                               |
| <span data-ttu-id="8faff-113">Taille</span><span class="sxs-lookup"><span data-stu-id="8faff-113">Size</span></span>              | \-                                                  |
| <span data-ttu-id="8faff-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="8faff-114">Update Privilege</span></span>  | <span data-ttu-id="8faff-115">Administrateur de domaine</span><span class="sxs-lookup"><span data-stu-id="8faff-115">Domain administrator</span></span>                                |
| <span data-ttu-id="8faff-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="8faff-116">Update Frequency</span></span>  | <span data-ttu-id="8faff-117">Chaque fois qu’un nouveau mécanisme d’authentification est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="8faff-117">Each time a new authentication mechanism is needed.</span></span> |
| <span data-ttu-id="8faff-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8faff-118">Attribute-Id</span></span>      | <span data-ttu-id="8faff-119">1.2.840.113556.1.4.867</span><span class="sxs-lookup"><span data-stu-id="8faff-119">1.2.840.113556.1.4.867</span></span>                              |
| <span data-ttu-id="8faff-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="8faff-120">System-Id-Guid</span></span>    | <span data-ttu-id="8faff-121">00fbf30c-91fe-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="8faff-121">00fbf30c-91fe-11d1-aebc-0000f80367c1</span></span>                |
| <span data-ttu-id="8faff-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8faff-122">Syntax</span></span>            | [<span data-ttu-id="8faff-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="8faff-123">**String(Unicode)**</span></span>](s-string-unicode.md)         |



## <a name="implementations"></a><span data-ttu-id="8faff-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="8faff-124">Implementations</span></span>

-   [<span data-ttu-id="8faff-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8faff-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8faff-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8faff-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8faff-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8faff-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8faff-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8faff-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8faff-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8faff-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8faff-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8faff-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8faff-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8faff-131">Windows 2000 Server</span></span>



| <span data-ttu-id="8faff-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="8faff-132">Entry</span></span> | <span data-ttu-id="8faff-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="8faff-133">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="8faff-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8faff-134">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="8faff-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8faff-135">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="8faff-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="8faff-136">System-Only</span></span>            | <span data-ttu-id="8faff-137">Faux</span><span class="sxs-lookup"><span data-stu-id="8faff-137">False</span></span>                                                        |
| <span data-ttu-id="8faff-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8faff-138">Is-Single-Valued</span></span>       | <span data-ttu-id="8faff-139">Faux</span><span class="sxs-lookup"><span data-stu-id="8faff-139">False</span></span>                                                        |
| <span data-ttu-id="8faff-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8faff-140">Is Indexed</span></span>             | <span data-ttu-id="8faff-141">Vrai</span><span class="sxs-lookup"><span data-stu-id="8faff-141">True</span></span>                                                         |
| <span data-ttu-id="8faff-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8faff-142">In Global Catalog</span></span>      | <span data-ttu-id="8faff-143">Vrai</span><span class="sxs-lookup"><span data-stu-id="8faff-143">True</span></span>                                                         |
| <span data-ttu-id="8faff-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8faff-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="8faff-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8faff-145">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="8faff-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8faff-146">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="8faff-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8faff-147">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="8faff-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8faff-148">Search-Flags</span></span>           | <span data-ttu-id="8faff-149">0x00000001</span><span class="sxs-lookup"><span data-stu-id="8faff-149">0x00000001</span></span>                                                   |
| <span data-ttu-id="8faff-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8faff-150">System-Flags</span></span>           | <span data-ttu-id="8faff-151">0x00000012</span><span class="sxs-lookup"><span data-stu-id="8faff-151">0x00000012</span></span>                                                   |
| <span data-ttu-id="8faff-152">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8faff-152">Classes used in</span></span>        | [<span data-ttu-id="8faff-153">**Sécurité-principal**</span><span class="sxs-lookup"><span data-stu-id="8faff-153">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8faff-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8faff-154">Windows Server 2003</span></span>



| <span data-ttu-id="8faff-155">Entrée</span><span class="sxs-lookup"><span data-stu-id="8faff-155">Entry</span></span> | <span data-ttu-id="8faff-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="8faff-156">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="8faff-157">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8faff-157">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="8faff-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8faff-158">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="8faff-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="8faff-159">System-Only</span></span>            | <span data-ttu-id="8faff-160">Faux</span><span class="sxs-lookup"><span data-stu-id="8faff-160">False</span></span>                                                        |
| <span data-ttu-id="8faff-161">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8faff-161">Is-Single-Valued</span></span>       | <span data-ttu-id="8faff-162">Faux</span><span class="sxs-lookup"><span data-stu-id="8faff-162">False</span></span>                                                        |
| <span data-ttu-id="8faff-163">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8faff-163">Is Indexed</span></span>             | <span data-ttu-id="8faff-164">Vrai</span><span class="sxs-lookup"><span data-stu-id="8faff-164">True</span></span>                                                         |
| <span data-ttu-id="8faff-165">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8faff-165">In Global Catalog</span></span>      | <span data-ttu-id="8faff-166">Vrai</span><span class="sxs-lookup"><span data-stu-id="8faff-166">True</span></span>                                                         |
| <span data-ttu-id="8faff-167">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8faff-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="8faff-168">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8faff-168">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="8faff-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8faff-169">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="8faff-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8faff-170">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="8faff-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8faff-171">Search-Flags</span></span>           | <span data-ttu-id="8faff-172">0x00000001</span><span class="sxs-lookup"><span data-stu-id="8faff-172">0x00000001</span></span>                                                   |
| <span data-ttu-id="8faff-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8faff-173">System-Flags</span></span>           | <span data-ttu-id="8faff-174">0x00000012</span><span class="sxs-lookup"><span data-stu-id="8faff-174">0x00000012</span></span>                                                   |
| <span data-ttu-id="8faff-175">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8faff-175">Classes used in</span></span>        | [<span data-ttu-id="8faff-176">**Sécurité-principal**</span><span class="sxs-lookup"><span data-stu-id="8faff-176">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8faff-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8faff-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8faff-178">Entrée</span><span class="sxs-lookup"><span data-stu-id="8faff-178">Entry</span></span> | <span data-ttu-id="8faff-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="8faff-179">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="8faff-180">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8faff-180">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="8faff-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8faff-181">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="8faff-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="8faff-182">System-Only</span></span>            | <span data-ttu-id="8faff-183">Faux</span><span class="sxs-lookup"><span data-stu-id="8faff-183">False</span></span>                                                        |
| <span data-ttu-id="8faff-184">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8faff-184">Is-Single-Valued</span></span>       | <span data-ttu-id="8faff-185">Faux</span><span class="sxs-lookup"><span data-stu-id="8faff-185">False</span></span>                                                        |
| <span data-ttu-id="8faff-186">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8faff-186">Is Indexed</span></span>             | <span data-ttu-id="8faff-187">Vrai</span><span class="sxs-lookup"><span data-stu-id="8faff-187">True</span></span>                                                         |
| <span data-ttu-id="8faff-188">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8faff-188">In Global Catalog</span></span>      | <span data-ttu-id="8faff-189">Vrai</span><span class="sxs-lookup"><span data-stu-id="8faff-189">True</span></span>                                                         |
| <span data-ttu-id="8faff-190">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8faff-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="8faff-191">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8faff-191">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="8faff-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8faff-192">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="8faff-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8faff-193">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="8faff-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8faff-194">Search-Flags</span></span>           | <span data-ttu-id="8faff-195">0x00000001</span><span class="sxs-lookup"><span data-stu-id="8faff-195">0x00000001</span></span>                                                   |
| <span data-ttu-id="8faff-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8faff-196">System-Flags</span></span>           | <span data-ttu-id="8faff-197">0x00000012</span><span class="sxs-lookup"><span data-stu-id="8faff-197">0x00000012</span></span>                                                   |
| <span data-ttu-id="8faff-198">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8faff-198">Classes used in</span></span>        | [<span data-ttu-id="8faff-199">**Sécurité-principal**</span><span class="sxs-lookup"><span data-stu-id="8faff-199">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8faff-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8faff-200">Windows Server 2008</span></span>



| <span data-ttu-id="8faff-201">Entrée</span><span class="sxs-lookup"><span data-stu-id="8faff-201">Entry</span></span> | <span data-ttu-id="8faff-202">Valeur</span><span class="sxs-lookup"><span data-stu-id="8faff-202">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="8faff-203">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8faff-203">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="8faff-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8faff-204">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="8faff-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="8faff-205">System-Only</span></span>            | <span data-ttu-id="8faff-206">Faux</span><span class="sxs-lookup"><span data-stu-id="8faff-206">False</span></span>                                                        |
| <span data-ttu-id="8faff-207">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8faff-207">Is-Single-Valued</span></span>       | <span data-ttu-id="8faff-208">Faux</span><span class="sxs-lookup"><span data-stu-id="8faff-208">False</span></span>                                                        |
| <span data-ttu-id="8faff-209">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8faff-209">Is Indexed</span></span>             | <span data-ttu-id="8faff-210">Vrai</span><span class="sxs-lookup"><span data-stu-id="8faff-210">True</span></span>                                                         |
| <span data-ttu-id="8faff-211">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8faff-211">In Global Catalog</span></span>      | <span data-ttu-id="8faff-212">Vrai</span><span class="sxs-lookup"><span data-stu-id="8faff-212">True</span></span>                                                         |
| <span data-ttu-id="8faff-213">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8faff-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="8faff-214">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8faff-214">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="8faff-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8faff-215">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="8faff-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8faff-216">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="8faff-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8faff-217">Search-Flags</span></span>           | <span data-ttu-id="8faff-218">0x00000001</span><span class="sxs-lookup"><span data-stu-id="8faff-218">0x00000001</span></span>                                                   |
| <span data-ttu-id="8faff-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8faff-219">System-Flags</span></span>           | <span data-ttu-id="8faff-220">0x00000012</span><span class="sxs-lookup"><span data-stu-id="8faff-220">0x00000012</span></span>                                                   |
| <span data-ttu-id="8faff-221">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8faff-221">Classes used in</span></span>        | [<span data-ttu-id="8faff-222">**Sécurité-principal**</span><span class="sxs-lookup"><span data-stu-id="8faff-222">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8faff-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8faff-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8faff-224">Entrée</span><span class="sxs-lookup"><span data-stu-id="8faff-224">Entry</span></span> | <span data-ttu-id="8faff-225">Valeur</span><span class="sxs-lookup"><span data-stu-id="8faff-225">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="8faff-226">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8faff-226">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="8faff-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8faff-227">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="8faff-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="8faff-228">System-Only</span></span>            | <span data-ttu-id="8faff-229">Faux</span><span class="sxs-lookup"><span data-stu-id="8faff-229">False</span></span>                                                        |
| <span data-ttu-id="8faff-230">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8faff-230">Is-Single-Valued</span></span>       | <span data-ttu-id="8faff-231">Faux</span><span class="sxs-lookup"><span data-stu-id="8faff-231">False</span></span>                                                        |
| <span data-ttu-id="8faff-232">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8faff-232">Is Indexed</span></span>             | <span data-ttu-id="8faff-233">Vrai</span><span class="sxs-lookup"><span data-stu-id="8faff-233">True</span></span>                                                         |
| <span data-ttu-id="8faff-234">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8faff-234">In Global Catalog</span></span>      | <span data-ttu-id="8faff-235">Vrai</span><span class="sxs-lookup"><span data-stu-id="8faff-235">True</span></span>                                                         |
| <span data-ttu-id="8faff-236">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8faff-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="8faff-237">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8faff-237">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="8faff-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8faff-238">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="8faff-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8faff-239">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="8faff-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8faff-240">Search-Flags</span></span>           | <span data-ttu-id="8faff-241">0x00000001</span><span class="sxs-lookup"><span data-stu-id="8faff-241">0x00000001</span></span>                                                   |
| <span data-ttu-id="8faff-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8faff-242">System-Flags</span></span>           | <span data-ttu-id="8faff-243">0x00000012</span><span class="sxs-lookup"><span data-stu-id="8faff-243">0x00000012</span></span>                                                   |
| <span data-ttu-id="8faff-244">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8faff-244">Classes used in</span></span>        | [<span data-ttu-id="8faff-245">**Sécurité-principal**</span><span class="sxs-lookup"><span data-stu-id="8faff-245">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8faff-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8faff-246">Windows Server 2012</span></span>



| <span data-ttu-id="8faff-247">Entrée</span><span class="sxs-lookup"><span data-stu-id="8faff-247">Entry</span></span> | <span data-ttu-id="8faff-248">Valeur</span><span class="sxs-lookup"><span data-stu-id="8faff-248">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="8faff-249">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8faff-249">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="8faff-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8faff-250">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="8faff-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="8faff-251">System-Only</span></span>            | <span data-ttu-id="8faff-252">Faux</span><span class="sxs-lookup"><span data-stu-id="8faff-252">False</span></span>                                                        |
| <span data-ttu-id="8faff-253">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8faff-253">Is-Single-Valued</span></span>       | <span data-ttu-id="8faff-254">Faux</span><span class="sxs-lookup"><span data-stu-id="8faff-254">False</span></span>                                                        |
| <span data-ttu-id="8faff-255">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8faff-255">Is Indexed</span></span>             | <span data-ttu-id="8faff-256">Vrai</span><span class="sxs-lookup"><span data-stu-id="8faff-256">True</span></span>                                                         |
| <span data-ttu-id="8faff-257">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8faff-257">In Global Catalog</span></span>      | <span data-ttu-id="8faff-258">Vrai</span><span class="sxs-lookup"><span data-stu-id="8faff-258">True</span></span>                                                         |
| <span data-ttu-id="8faff-259">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8faff-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="8faff-260">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8faff-260">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="8faff-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8faff-261">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="8faff-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8faff-262">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="8faff-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8faff-263">Search-Flags</span></span>           | <span data-ttu-id="8faff-264">0x00000001</span><span class="sxs-lookup"><span data-stu-id="8faff-264">0x00000001</span></span>                                                   |
| <span data-ttu-id="8faff-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8faff-265">System-Flags</span></span>           | <span data-ttu-id="8faff-266">0x00000012</span><span class="sxs-lookup"><span data-stu-id="8faff-266">0x00000012</span></span>                                                   |
| <span data-ttu-id="8faff-267">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8faff-267">Classes used in</span></span>        | [<span data-ttu-id="8faff-268">**Sécurité-principal**</span><span class="sxs-lookup"><span data-stu-id="8faff-268">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



 

 





