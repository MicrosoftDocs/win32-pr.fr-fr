---
title: Attribut Security-Identifier
description: Valeur unique de longueur variable utilisée pour identifier un compte d’utilisateur, un compte de groupe ou une ouverture de session à laquelle une entrée du contrôle d’accès s’applique.
ms.assetid: bb6a16f6-d2c1-48f1-af9a-40fe2a59f281
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Security-Identifier
- Schéma AD d’attribut securityIdentifier
topic_type:
- apiref
api_name:
- Security-Identifier
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dd921d0bcba08c2174475007476add8e8787456
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744532"
---
# <a name="security-identifier-attribute"></a><span data-ttu-id="9e2a4-105">Attribut Security-Identifier</span><span class="sxs-lookup"><span data-stu-id="9e2a4-105">Security-Identifier attribute</span></span>

<span data-ttu-id="9e2a4-106">Valeur unique de longueur variable utilisée pour identifier un compte d’utilisateur, un compte de groupe ou une ouverture de session à laquelle une entrée du contrôle d’accès s’applique.</span><span class="sxs-lookup"><span data-stu-id="9e2a4-106">A unique value of variable length used to identify a user account, group account, or logon session to which an ACE applies.</span></span>



| <span data-ttu-id="9e2a4-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="9e2a4-107">Entry</span></span> | <span data-ttu-id="9e2a4-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="9e2a4-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="9e2a4-109">CN</span><span class="sxs-lookup"><span data-stu-id="9e2a4-109">CN</span></span>                | <span data-ttu-id="9e2a4-110">Security-Identifier</span><span class="sxs-lookup"><span data-stu-id="9e2a4-110">Security-Identifier</span></span>                  |
| <span data-ttu-id="9e2a4-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="9e2a4-111">Ldap-Display-Name</span></span> | <span data-ttu-id="9e2a4-112">securityIdentifier</span><span class="sxs-lookup"><span data-stu-id="9e2a4-112">securityIdentifier</span></span>                   |
| <span data-ttu-id="9e2a4-113">Taille</span><span class="sxs-lookup"><span data-stu-id="9e2a4-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="9e2a4-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="9e2a4-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="9e2a4-115">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="9e2a4-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="9e2a4-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9e2a4-116">Attribute-Id</span></span>      | <span data-ttu-id="9e2a4-117">1.2.840.113556.1.4.121</span><span class="sxs-lookup"><span data-stu-id="9e2a4-117">1.2.840.113556.1.4.121</span></span>               |
| <span data-ttu-id="9e2a4-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="9e2a4-118">System-Id-Guid</span></span>    | <span data-ttu-id="9e2a4-119">bf967a2f-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="9e2a4-119">bf967a2f-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="9e2a4-120">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9e2a4-120">Syntax</span></span>            | [<span data-ttu-id="9e2a4-121">**Chaîne (SID)**</span><span class="sxs-lookup"><span data-stu-id="9e2a4-121">**String(Sid)**</span></span>](s-string-sid.md)  |



## <a name="implementations"></a><span data-ttu-id="9e2a4-122">Implémentations</span><span class="sxs-lookup"><span data-stu-id="9e2a4-122">Implementations</span></span>

-   [<span data-ttu-id="9e2a4-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="9e2a4-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="9e2a4-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9e2a4-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9e2a4-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9e2a4-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9e2a4-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9e2a4-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9e2a4-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9e2a4-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9e2a4-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9e2a4-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="9e2a4-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9e2a4-129">Windows 2000 Server</span></span>



| <span data-ttu-id="9e2a4-130">Entrée</span><span class="sxs-lookup"><span data-stu-id="9e2a4-130">Entry</span></span> | <span data-ttu-id="9e2a4-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="9e2a4-131">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e2a4-132">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9e2a4-132">Link-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="9e2a4-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9e2a4-133">MAPI-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="9e2a4-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="9e2a4-134">System-Only</span></span>            | <span data-ttu-id="9e2a4-135">Faux</span><span class="sxs-lookup"><span data-stu-id="9e2a4-135">False</span></span>                                                                                                             |
| <span data-ttu-id="9e2a4-136">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9e2a4-136">Is-Single-Valued</span></span>       | <span data-ttu-id="9e2a4-137">Vrai</span><span class="sxs-lookup"><span data-stu-id="9e2a4-137">True</span></span>                                                                                                              |
| <span data-ttu-id="9e2a4-138">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9e2a4-138">Is Indexed</span></span>             | <span data-ttu-id="9e2a4-139">Faux</span><span class="sxs-lookup"><span data-stu-id="9e2a4-139">False</span></span>                                                                                                             |
| <span data-ttu-id="9e2a4-140">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9e2a4-140">In Global Catalog</span></span>      | <span data-ttu-id="9e2a4-141">Faux</span><span class="sxs-lookup"><span data-stu-id="9e2a4-141">False</span></span>                                                                                                             |
| <span data-ttu-id="9e2a4-142">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9e2a4-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="9e2a4-143">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9e2a4-143">O:BAG:BAD:S:</span></span>                                                                                                      |
| <span data-ttu-id="9e2a4-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9e2a4-144">Range-Lower</span></span>            | \-                                                                                                                |
| <span data-ttu-id="9e2a4-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9e2a4-145">Range-Upper</span></span>            | \-                                                                                                                |
| <span data-ttu-id="9e2a4-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9e2a4-146">Search-Flags</span></span>           | <span data-ttu-id="9e2a4-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9e2a4-147">0x00000000</span></span>                                                                                                        |
| <span data-ttu-id="9e2a4-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9e2a4-148">System-Flags</span></span>           | <span data-ttu-id="9e2a4-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9e2a4-149">0x00000010</span></span>                                                                                                        |
| <span data-ttu-id="9e2a4-150">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9e2a4-150">Classes used in</span></span>        | [<span data-ttu-id="9e2a4-151">**Sécurité-principal**</span><span class="sxs-lookup"><span data-stu-id="9e2a4-151">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> [<span data-ttu-id="9e2a4-152">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="9e2a4-152">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="9e2a4-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9e2a4-153">Windows Server 2003</span></span>



| <span data-ttu-id="9e2a4-154">Entrée</span><span class="sxs-lookup"><span data-stu-id="9e2a4-154">Entry</span></span> | <span data-ttu-id="9e2a4-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="9e2a4-155">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e2a4-156">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9e2a4-156">Link-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="9e2a4-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9e2a4-157">MAPI-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="9e2a4-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="9e2a4-158">System-Only</span></span>            | <span data-ttu-id="9e2a4-159">Faux</span><span class="sxs-lookup"><span data-stu-id="9e2a4-159">False</span></span>                                                                                                             |
| <span data-ttu-id="9e2a4-160">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9e2a4-160">Is-Single-Valued</span></span>       | <span data-ttu-id="9e2a4-161">Vrai</span><span class="sxs-lookup"><span data-stu-id="9e2a4-161">True</span></span>                                                                                                              |
| <span data-ttu-id="9e2a4-162">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9e2a4-162">Is Indexed</span></span>             | <span data-ttu-id="9e2a4-163">Faux</span><span class="sxs-lookup"><span data-stu-id="9e2a4-163">False</span></span>                                                                                                             |
| <span data-ttu-id="9e2a4-164">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9e2a4-164">In Global Catalog</span></span>      | <span data-ttu-id="9e2a4-165">Vrai</span><span class="sxs-lookup"><span data-stu-id="9e2a4-165">True</span></span>                                                                                                              |
| <span data-ttu-id="9e2a4-166">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9e2a4-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="9e2a4-167">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9e2a4-167">O:BAG:BAD:S:</span></span>                                                                                                      |
| <span data-ttu-id="9e2a4-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9e2a4-168">Range-Lower</span></span>            | \-                                                                                                                |
| <span data-ttu-id="9e2a4-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9e2a4-169">Range-Upper</span></span>            | \-                                                                                                                |
| <span data-ttu-id="9e2a4-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9e2a4-170">Search-Flags</span></span>           | <span data-ttu-id="9e2a4-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9e2a4-171">0x00000000</span></span>                                                                                                        |
| <span data-ttu-id="9e2a4-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9e2a4-172">System-Flags</span></span>           | <span data-ttu-id="9e2a4-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9e2a4-173">0x00000010</span></span>                                                                                                        |
| <span data-ttu-id="9e2a4-174">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9e2a4-174">Classes used in</span></span>        | [<span data-ttu-id="9e2a4-175">**Sécurité-principal**</span><span class="sxs-lookup"><span data-stu-id="9e2a4-175">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> [<span data-ttu-id="9e2a4-176">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="9e2a4-176">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9e2a4-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9e2a4-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9e2a4-178">Entrée</span><span class="sxs-lookup"><span data-stu-id="9e2a4-178">Entry</span></span> | <span data-ttu-id="9e2a4-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="9e2a4-179">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e2a4-180">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9e2a4-180">Link-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="9e2a4-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9e2a4-181">MAPI-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="9e2a4-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="9e2a4-182">System-Only</span></span>            | <span data-ttu-id="9e2a4-183">Faux</span><span class="sxs-lookup"><span data-stu-id="9e2a4-183">False</span></span>                                                                                                             |
| <span data-ttu-id="9e2a4-184">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9e2a4-184">Is-Single-Valued</span></span>       | <span data-ttu-id="9e2a4-185">Vrai</span><span class="sxs-lookup"><span data-stu-id="9e2a4-185">True</span></span>                                                                                                              |
| <span data-ttu-id="9e2a4-186">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9e2a4-186">Is Indexed</span></span>             | <span data-ttu-id="9e2a4-187">Faux</span><span class="sxs-lookup"><span data-stu-id="9e2a4-187">False</span></span>                                                                                                             |
| <span data-ttu-id="9e2a4-188">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9e2a4-188">In Global Catalog</span></span>      | <span data-ttu-id="9e2a4-189">Vrai</span><span class="sxs-lookup"><span data-stu-id="9e2a4-189">True</span></span>                                                                                                              |
| <span data-ttu-id="9e2a4-190">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9e2a4-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="9e2a4-191">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9e2a4-191">O:BAG:BAD:S:</span></span>                                                                                                      |
| <span data-ttu-id="9e2a4-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9e2a4-192">Range-Lower</span></span>            | \-                                                                                                                |
| <span data-ttu-id="9e2a4-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9e2a4-193">Range-Upper</span></span>            | \-                                                                                                                |
| <span data-ttu-id="9e2a4-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9e2a4-194">Search-Flags</span></span>           | <span data-ttu-id="9e2a4-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9e2a4-195">0x00000000</span></span>                                                                                                        |
| <span data-ttu-id="9e2a4-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9e2a4-196">System-Flags</span></span>           | <span data-ttu-id="9e2a4-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9e2a4-197">0x00000010</span></span>                                                                                                        |
| <span data-ttu-id="9e2a4-198">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9e2a4-198">Classes used in</span></span>        | [<span data-ttu-id="9e2a4-199">**Sécurité-principal**</span><span class="sxs-lookup"><span data-stu-id="9e2a4-199">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> [<span data-ttu-id="9e2a4-200">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="9e2a4-200">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9e2a4-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9e2a4-201">Windows Server 2008</span></span>



| <span data-ttu-id="9e2a4-202">Entrée</span><span class="sxs-lookup"><span data-stu-id="9e2a4-202">Entry</span></span> | <span data-ttu-id="9e2a4-203">Valeur</span><span class="sxs-lookup"><span data-stu-id="9e2a4-203">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e2a4-204">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9e2a4-204">Link-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="9e2a4-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9e2a4-205">MAPI-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="9e2a4-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="9e2a4-206">System-Only</span></span>            | <span data-ttu-id="9e2a4-207">Faux</span><span class="sxs-lookup"><span data-stu-id="9e2a4-207">False</span></span>                                                                                                             |
| <span data-ttu-id="9e2a4-208">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9e2a4-208">Is-Single-Valued</span></span>       | <span data-ttu-id="9e2a4-209">Vrai</span><span class="sxs-lookup"><span data-stu-id="9e2a4-209">True</span></span>                                                                                                              |
| <span data-ttu-id="9e2a4-210">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9e2a4-210">Is Indexed</span></span>             | <span data-ttu-id="9e2a4-211">Faux</span><span class="sxs-lookup"><span data-stu-id="9e2a4-211">False</span></span>                                                                                                             |
| <span data-ttu-id="9e2a4-212">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9e2a4-212">In Global Catalog</span></span>      | <span data-ttu-id="9e2a4-213">Vrai</span><span class="sxs-lookup"><span data-stu-id="9e2a4-213">True</span></span>                                                                                                              |
| <span data-ttu-id="9e2a4-214">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9e2a4-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="9e2a4-215">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9e2a4-215">O:BAG:BAD:S:</span></span>                                                                                                      |
| <span data-ttu-id="9e2a4-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9e2a4-216">Range-Lower</span></span>            | \-                                                                                                                |
| <span data-ttu-id="9e2a4-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9e2a4-217">Range-Upper</span></span>            | \-                                                                                                                |
| <span data-ttu-id="9e2a4-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9e2a4-218">Search-Flags</span></span>           | <span data-ttu-id="9e2a4-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9e2a4-219">0x00000000</span></span>                                                                                                        |
| <span data-ttu-id="9e2a4-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9e2a4-220">System-Flags</span></span>           | <span data-ttu-id="9e2a4-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9e2a4-221">0x00000010</span></span>                                                                                                        |
| <span data-ttu-id="9e2a4-222">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9e2a4-222">Classes used in</span></span>        | [<span data-ttu-id="9e2a4-223">**Sécurité-principal**</span><span class="sxs-lookup"><span data-stu-id="9e2a4-223">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> [<span data-ttu-id="9e2a4-224">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="9e2a4-224">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9e2a4-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9e2a4-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9e2a4-226">Entrée</span><span class="sxs-lookup"><span data-stu-id="9e2a4-226">Entry</span></span> | <span data-ttu-id="9e2a4-227">Valeur</span><span class="sxs-lookup"><span data-stu-id="9e2a4-227">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e2a4-228">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9e2a4-228">Link-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="9e2a4-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9e2a4-229">MAPI-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="9e2a4-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="9e2a4-230">System-Only</span></span>            | <span data-ttu-id="9e2a4-231">Faux</span><span class="sxs-lookup"><span data-stu-id="9e2a4-231">False</span></span>                                                                                                             |
| <span data-ttu-id="9e2a4-232">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9e2a4-232">Is-Single-Valued</span></span>       | <span data-ttu-id="9e2a4-233">Vrai</span><span class="sxs-lookup"><span data-stu-id="9e2a4-233">True</span></span>                                                                                                              |
| <span data-ttu-id="9e2a4-234">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9e2a4-234">Is Indexed</span></span>             | <span data-ttu-id="9e2a4-235">Faux</span><span class="sxs-lookup"><span data-stu-id="9e2a4-235">False</span></span>                                                                                                             |
| <span data-ttu-id="9e2a4-236">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9e2a4-236">In Global Catalog</span></span>      | <span data-ttu-id="9e2a4-237">Vrai</span><span class="sxs-lookup"><span data-stu-id="9e2a4-237">True</span></span>                                                                                                              |
| <span data-ttu-id="9e2a4-238">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9e2a4-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="9e2a4-239">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9e2a4-239">O:BAG:BAD:S:</span></span>                                                                                                      |
| <span data-ttu-id="9e2a4-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9e2a4-240">Range-Lower</span></span>            | \-                                                                                                                |
| <span data-ttu-id="9e2a4-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9e2a4-241">Range-Upper</span></span>            | \-                                                                                                                |
| <span data-ttu-id="9e2a4-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9e2a4-242">Search-Flags</span></span>           | <span data-ttu-id="9e2a4-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9e2a4-243">0x00000000</span></span>                                                                                                        |
| <span data-ttu-id="9e2a4-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9e2a4-244">System-Flags</span></span>           | <span data-ttu-id="9e2a4-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9e2a4-245">0x00000010</span></span>                                                                                                        |
| <span data-ttu-id="9e2a4-246">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9e2a4-246">Classes used in</span></span>        | [<span data-ttu-id="9e2a4-247">**Sécurité-principal**</span><span class="sxs-lookup"><span data-stu-id="9e2a4-247">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> [<span data-ttu-id="9e2a4-248">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="9e2a4-248">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9e2a4-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9e2a4-249">Windows Server 2012</span></span>



| <span data-ttu-id="9e2a4-250">Entrée</span><span class="sxs-lookup"><span data-stu-id="9e2a4-250">Entry</span></span> | <span data-ttu-id="9e2a4-251">Valeur</span><span class="sxs-lookup"><span data-stu-id="9e2a4-251">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e2a4-252">ID de lien</span><span class="sxs-lookup"><span data-stu-id="9e2a4-252">Link-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="9e2a4-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9e2a4-253">MAPI-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="9e2a4-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="9e2a4-254">System-Only</span></span>            | <span data-ttu-id="9e2a4-255">Faux</span><span class="sxs-lookup"><span data-stu-id="9e2a4-255">False</span></span>                                                                                                             |
| <span data-ttu-id="9e2a4-256">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="9e2a4-256">Is-Single-Valued</span></span>       | <span data-ttu-id="9e2a4-257">Vrai</span><span class="sxs-lookup"><span data-stu-id="9e2a4-257">True</span></span>                                                                                                              |
| <span data-ttu-id="9e2a4-258">Est indexé</span><span class="sxs-lookup"><span data-stu-id="9e2a4-258">Is Indexed</span></span>             | <span data-ttu-id="9e2a4-259">Faux</span><span class="sxs-lookup"><span data-stu-id="9e2a4-259">False</span></span>                                                                                                             |
| <span data-ttu-id="9e2a4-260">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="9e2a4-260">In Global Catalog</span></span>      | <span data-ttu-id="9e2a4-261">Vrai</span><span class="sxs-lookup"><span data-stu-id="9e2a4-261">True</span></span>                                                                                                              |
| <span data-ttu-id="9e2a4-262">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="9e2a4-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="9e2a4-263">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="9e2a4-263">O:BAG:BAD:S:</span></span>                                                                                                      |
| <span data-ttu-id="9e2a4-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9e2a4-264">Range-Lower</span></span>            | \-                                                                                                                |
| <span data-ttu-id="9e2a4-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9e2a4-265">Range-Upper</span></span>            | \-                                                                                                                |
| <span data-ttu-id="9e2a4-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9e2a4-266">Search-Flags</span></span>           | <span data-ttu-id="9e2a4-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9e2a4-267">0x00000000</span></span>                                                                                                        |
| <span data-ttu-id="9e2a4-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9e2a4-268">System-Flags</span></span>           | <span data-ttu-id="9e2a4-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9e2a4-269">0x00000010</span></span>                                                                                                        |
| <span data-ttu-id="9e2a4-270">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="9e2a4-270">Classes used in</span></span>        | [<span data-ttu-id="9e2a4-271">**Sécurité-principal**</span><span class="sxs-lookup"><span data-stu-id="9e2a4-271">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> [<span data-ttu-id="9e2a4-272">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="9e2a4-272">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





