---
title: Attribut initial-auth-entrant
description: Contient des informations sur une demande d’authentification entrante initiale par un client sur ce serveur. Cette demande est ensuite envoyée par ce serveur au serveur d’authentification du domaine.
ms.assetid: d49d45ae-87fe-415d-8110-79b2b321f2b6
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut initial-auth-entrant
- Schéma AD de l’attribut initialAuthIncoming
topic_type:
- apiref
api_name:
- Initial-Auth-Incoming
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 973b00abd5b77b713fc03b5efb3d4cf45b97fc19
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744837"
---
# <a name="initial-auth-incoming-attribute"></a><span data-ttu-id="90e7f-106">Attribut initial-auth-entrant</span><span class="sxs-lookup"><span data-stu-id="90e7f-106">Initial-Auth-Incoming attribute</span></span>

<span data-ttu-id="90e7f-107">Contient des informations sur une demande d’authentification entrante initiale par un client sur ce serveur.</span><span class="sxs-lookup"><span data-stu-id="90e7f-107">Contains information about an initial incoming authentication request by a client to this server.</span></span> <span data-ttu-id="90e7f-108">Cette demande est ensuite envoyée par ce serveur au serveur d’authentification du domaine.</span><span class="sxs-lookup"><span data-stu-id="90e7f-108">This request is then sent by this server to the authentication server for the domain.</span></span>



| <span data-ttu-id="90e7f-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="90e7f-109">Entry</span></span> | <span data-ttu-id="90e7f-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="90e7f-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="90e7f-111">CN</span><span class="sxs-lookup"><span data-stu-id="90e7f-111">CN</span></span>                | <span data-ttu-id="90e7f-112">Initial-auth-entrant</span><span class="sxs-lookup"><span data-stu-id="90e7f-112">Initial-Auth-Incoming</span></span>                       |
| <span data-ttu-id="90e7f-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="90e7f-113">Ldap-Display-Name</span></span> | <span data-ttu-id="90e7f-114">initialAuthIncoming</span><span class="sxs-lookup"><span data-stu-id="90e7f-114">initialAuthIncoming</span></span>                         |
| <span data-ttu-id="90e7f-115">Taille</span><span class="sxs-lookup"><span data-stu-id="90e7f-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="90e7f-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="90e7f-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="90e7f-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="90e7f-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="90e7f-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="90e7f-118">Attribute-Id</span></span>      | <span data-ttu-id="90e7f-119">1.2.840.113556.1.4.539</span><span class="sxs-lookup"><span data-stu-id="90e7f-119">1.2.840.113556.1.4.539</span></span>                      |
| <span data-ttu-id="90e7f-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="90e7f-120">System-Id-Guid</span></span>    | <span data-ttu-id="90e7f-121">52458023-ca6a-11D0-AFFF-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="90e7f-121">52458023-ca6a-11d0-afff-0000f80367c1</span></span>        |
| <span data-ttu-id="90e7f-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="90e7f-122">Syntax</span></span>            | [<span data-ttu-id="90e7f-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="90e7f-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="90e7f-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="90e7f-124">Implementations</span></span>

-   [<span data-ttu-id="90e7f-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="90e7f-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="90e7f-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="90e7f-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="90e7f-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="90e7f-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="90e7f-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="90e7f-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="90e7f-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="90e7f-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="90e7f-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="90e7f-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="90e7f-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="90e7f-131">Windows 2000 Server</span></span>



| <span data-ttu-id="90e7f-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="90e7f-132">Entry</span></span> | <span data-ttu-id="90e7f-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="90e7f-133">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="90e7f-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="90e7f-134">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="90e7f-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="90e7f-135">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="90e7f-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="90e7f-136">System-Only</span></span>            | <span data-ttu-id="90e7f-137">Faux</span><span class="sxs-lookup"><span data-stu-id="90e7f-137">False</span></span>                                                |
| <span data-ttu-id="90e7f-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="90e7f-138">Is-Single-Valued</span></span>       | <span data-ttu-id="90e7f-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="90e7f-139">True</span></span>                                                 |
| <span data-ttu-id="90e7f-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="90e7f-140">Is Indexed</span></span>             | <span data-ttu-id="90e7f-141">Faux</span><span class="sxs-lookup"><span data-stu-id="90e7f-141">False</span></span>                                                |
| <span data-ttu-id="90e7f-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="90e7f-142">In Global Catalog</span></span>      | <span data-ttu-id="90e7f-143">Faux</span><span class="sxs-lookup"><span data-stu-id="90e7f-143">False</span></span>                                                |
| <span data-ttu-id="90e7f-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="90e7f-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="90e7f-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="90e7f-145">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="90e7f-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="90e7f-146">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="90e7f-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="90e7f-147">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="90e7f-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="90e7f-148">Search-Flags</span></span>           | <span data-ttu-id="90e7f-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="90e7f-149">0x00000000</span></span>                                           |
| <span data-ttu-id="90e7f-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="90e7f-150">System-Flags</span></span>           | <span data-ttu-id="90e7f-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="90e7f-151">0x00000010</span></span>                                           |
| <span data-ttu-id="90e7f-152">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="90e7f-152">Classes used in</span></span>        | [<span data-ttu-id="90e7f-153">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="90e7f-153">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="90e7f-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="90e7f-154">Windows Server 2003</span></span>



| <span data-ttu-id="90e7f-155">Entrée</span><span class="sxs-lookup"><span data-stu-id="90e7f-155">Entry</span></span> | <span data-ttu-id="90e7f-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="90e7f-156">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="90e7f-157">ID de lien</span><span class="sxs-lookup"><span data-stu-id="90e7f-157">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="90e7f-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="90e7f-158">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="90e7f-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="90e7f-159">System-Only</span></span>            | <span data-ttu-id="90e7f-160">Faux</span><span class="sxs-lookup"><span data-stu-id="90e7f-160">False</span></span>                                                |
| <span data-ttu-id="90e7f-161">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="90e7f-161">Is-Single-Valued</span></span>       | <span data-ttu-id="90e7f-162">Vrai</span><span class="sxs-lookup"><span data-stu-id="90e7f-162">True</span></span>                                                 |
| <span data-ttu-id="90e7f-163">Est indexé</span><span class="sxs-lookup"><span data-stu-id="90e7f-163">Is Indexed</span></span>             | <span data-ttu-id="90e7f-164">Faux</span><span class="sxs-lookup"><span data-stu-id="90e7f-164">False</span></span>                                                |
| <span data-ttu-id="90e7f-165">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="90e7f-165">In Global Catalog</span></span>      | <span data-ttu-id="90e7f-166">Faux</span><span class="sxs-lookup"><span data-stu-id="90e7f-166">False</span></span>                                                |
| <span data-ttu-id="90e7f-167">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="90e7f-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="90e7f-168">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="90e7f-168">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="90e7f-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="90e7f-169">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="90e7f-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="90e7f-170">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="90e7f-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="90e7f-171">Search-Flags</span></span>           | <span data-ttu-id="90e7f-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="90e7f-172">0x00000000</span></span>                                           |
| <span data-ttu-id="90e7f-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="90e7f-173">System-Flags</span></span>           | <span data-ttu-id="90e7f-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="90e7f-174">0x00000010</span></span>                                           |
| <span data-ttu-id="90e7f-175">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="90e7f-175">Classes used in</span></span>        | [<span data-ttu-id="90e7f-176">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="90e7f-176">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="90e7f-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="90e7f-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="90e7f-178">Entrée</span><span class="sxs-lookup"><span data-stu-id="90e7f-178">Entry</span></span> | <span data-ttu-id="90e7f-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="90e7f-179">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="90e7f-180">ID de lien</span><span class="sxs-lookup"><span data-stu-id="90e7f-180">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="90e7f-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="90e7f-181">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="90e7f-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="90e7f-182">System-Only</span></span>            | <span data-ttu-id="90e7f-183">Faux</span><span class="sxs-lookup"><span data-stu-id="90e7f-183">False</span></span>                                                |
| <span data-ttu-id="90e7f-184">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="90e7f-184">Is-Single-Valued</span></span>       | <span data-ttu-id="90e7f-185">Vrai</span><span class="sxs-lookup"><span data-stu-id="90e7f-185">True</span></span>                                                 |
| <span data-ttu-id="90e7f-186">Est indexé</span><span class="sxs-lookup"><span data-stu-id="90e7f-186">Is Indexed</span></span>             | <span data-ttu-id="90e7f-187">Faux</span><span class="sxs-lookup"><span data-stu-id="90e7f-187">False</span></span>                                                |
| <span data-ttu-id="90e7f-188">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="90e7f-188">In Global Catalog</span></span>      | <span data-ttu-id="90e7f-189">Faux</span><span class="sxs-lookup"><span data-stu-id="90e7f-189">False</span></span>                                                |
| <span data-ttu-id="90e7f-190">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="90e7f-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="90e7f-191">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="90e7f-191">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="90e7f-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="90e7f-192">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="90e7f-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="90e7f-193">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="90e7f-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="90e7f-194">Search-Flags</span></span>           | <span data-ttu-id="90e7f-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="90e7f-195">0x00000000</span></span>                                           |
| <span data-ttu-id="90e7f-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="90e7f-196">System-Flags</span></span>           | <span data-ttu-id="90e7f-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="90e7f-197">0x00000010</span></span>                                           |
| <span data-ttu-id="90e7f-198">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="90e7f-198">Classes used in</span></span>        | [<span data-ttu-id="90e7f-199">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="90e7f-199">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="90e7f-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="90e7f-200">Windows Server 2008</span></span>



| <span data-ttu-id="90e7f-201">Entrée</span><span class="sxs-lookup"><span data-stu-id="90e7f-201">Entry</span></span> | <span data-ttu-id="90e7f-202">Valeur</span><span class="sxs-lookup"><span data-stu-id="90e7f-202">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="90e7f-203">ID de lien</span><span class="sxs-lookup"><span data-stu-id="90e7f-203">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="90e7f-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="90e7f-204">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="90e7f-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="90e7f-205">System-Only</span></span>            | <span data-ttu-id="90e7f-206">Faux</span><span class="sxs-lookup"><span data-stu-id="90e7f-206">False</span></span>                                                |
| <span data-ttu-id="90e7f-207">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="90e7f-207">Is-Single-Valued</span></span>       | <span data-ttu-id="90e7f-208">Vrai</span><span class="sxs-lookup"><span data-stu-id="90e7f-208">True</span></span>                                                 |
| <span data-ttu-id="90e7f-209">Est indexé</span><span class="sxs-lookup"><span data-stu-id="90e7f-209">Is Indexed</span></span>             | <span data-ttu-id="90e7f-210">Faux</span><span class="sxs-lookup"><span data-stu-id="90e7f-210">False</span></span>                                                |
| <span data-ttu-id="90e7f-211">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="90e7f-211">In Global Catalog</span></span>      | <span data-ttu-id="90e7f-212">Faux</span><span class="sxs-lookup"><span data-stu-id="90e7f-212">False</span></span>                                                |
| <span data-ttu-id="90e7f-213">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="90e7f-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="90e7f-214">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="90e7f-214">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="90e7f-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="90e7f-215">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="90e7f-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="90e7f-216">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="90e7f-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="90e7f-217">Search-Flags</span></span>           | <span data-ttu-id="90e7f-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="90e7f-218">0x00000000</span></span>                                           |
| <span data-ttu-id="90e7f-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="90e7f-219">System-Flags</span></span>           | <span data-ttu-id="90e7f-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="90e7f-220">0x00000010</span></span>                                           |
| <span data-ttu-id="90e7f-221">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="90e7f-221">Classes used in</span></span>        | [<span data-ttu-id="90e7f-222">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="90e7f-222">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="90e7f-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="90e7f-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="90e7f-224">Entrée</span><span class="sxs-lookup"><span data-stu-id="90e7f-224">Entry</span></span> | <span data-ttu-id="90e7f-225">Valeur</span><span class="sxs-lookup"><span data-stu-id="90e7f-225">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="90e7f-226">ID de lien</span><span class="sxs-lookup"><span data-stu-id="90e7f-226">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="90e7f-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="90e7f-227">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="90e7f-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="90e7f-228">System-Only</span></span>            | <span data-ttu-id="90e7f-229">Faux</span><span class="sxs-lookup"><span data-stu-id="90e7f-229">False</span></span>                                                |
| <span data-ttu-id="90e7f-230">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="90e7f-230">Is-Single-Valued</span></span>       | <span data-ttu-id="90e7f-231">Vrai</span><span class="sxs-lookup"><span data-stu-id="90e7f-231">True</span></span>                                                 |
| <span data-ttu-id="90e7f-232">Est indexé</span><span class="sxs-lookup"><span data-stu-id="90e7f-232">Is Indexed</span></span>             | <span data-ttu-id="90e7f-233">Faux</span><span class="sxs-lookup"><span data-stu-id="90e7f-233">False</span></span>                                                |
| <span data-ttu-id="90e7f-234">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="90e7f-234">In Global Catalog</span></span>      | <span data-ttu-id="90e7f-235">Faux</span><span class="sxs-lookup"><span data-stu-id="90e7f-235">False</span></span>                                                |
| <span data-ttu-id="90e7f-236">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="90e7f-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="90e7f-237">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="90e7f-237">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="90e7f-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="90e7f-238">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="90e7f-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="90e7f-239">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="90e7f-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="90e7f-240">Search-Flags</span></span>           | <span data-ttu-id="90e7f-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="90e7f-241">0x00000000</span></span>                                           |
| <span data-ttu-id="90e7f-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="90e7f-242">System-Flags</span></span>           | <span data-ttu-id="90e7f-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="90e7f-243">0x00000010</span></span>                                           |
| <span data-ttu-id="90e7f-244">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="90e7f-244">Classes used in</span></span>        | [<span data-ttu-id="90e7f-245">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="90e7f-245">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="90e7f-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="90e7f-246">Windows Server 2012</span></span>



| <span data-ttu-id="90e7f-247">Entrée</span><span class="sxs-lookup"><span data-stu-id="90e7f-247">Entry</span></span> | <span data-ttu-id="90e7f-248">Valeur</span><span class="sxs-lookup"><span data-stu-id="90e7f-248">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="90e7f-249">ID de lien</span><span class="sxs-lookup"><span data-stu-id="90e7f-249">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="90e7f-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="90e7f-250">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="90e7f-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="90e7f-251">System-Only</span></span>            | <span data-ttu-id="90e7f-252">Faux</span><span class="sxs-lookup"><span data-stu-id="90e7f-252">False</span></span>                                                |
| <span data-ttu-id="90e7f-253">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="90e7f-253">Is-Single-Valued</span></span>       | <span data-ttu-id="90e7f-254">Vrai</span><span class="sxs-lookup"><span data-stu-id="90e7f-254">True</span></span>                                                 |
| <span data-ttu-id="90e7f-255">Est indexé</span><span class="sxs-lookup"><span data-stu-id="90e7f-255">Is Indexed</span></span>             | <span data-ttu-id="90e7f-256">Faux</span><span class="sxs-lookup"><span data-stu-id="90e7f-256">False</span></span>                                                |
| <span data-ttu-id="90e7f-257">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="90e7f-257">In Global Catalog</span></span>      | <span data-ttu-id="90e7f-258">Faux</span><span class="sxs-lookup"><span data-stu-id="90e7f-258">False</span></span>                                                |
| <span data-ttu-id="90e7f-259">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="90e7f-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="90e7f-260">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="90e7f-260">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="90e7f-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="90e7f-261">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="90e7f-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="90e7f-262">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="90e7f-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="90e7f-263">Search-Flags</span></span>           | <span data-ttu-id="90e7f-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="90e7f-264">0x00000000</span></span>                                           |
| <span data-ttu-id="90e7f-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="90e7f-265">System-Flags</span></span>           | <span data-ttu-id="90e7f-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="90e7f-266">0x00000010</span></span>                                           |
| <span data-ttu-id="90e7f-267">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="90e7f-267">Classes used in</span></span>        | [<span data-ttu-id="90e7f-268">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="90e7f-268">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





