---
title: Attribut initial-auth-sortante
description: Contient des informations sur une authentification sortante initiale envoyée par le serveur d’authentification pour ce domaine au client qui a demandé l’authentification.
ms.assetid: cc5ceb14-0424-4caa-bcd9-1e48988af67a
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut initial-auth-sortante
- Schéma AD de l’attribut initialAuthOutgoing
topic_type:
- apiref
api_name:
- Initial-Auth-Outgoing
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e84faaa443c9589e04f4998dc41d72fe870b5f2e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107044"
---
# <a name="initial-auth-outgoing-attribute"></a><span data-ttu-id="a1f21-105">Attribut initial-auth-sortante</span><span class="sxs-lookup"><span data-stu-id="a1f21-105">Initial-Auth-Outgoing attribute</span></span>

<span data-ttu-id="a1f21-106">Contient des informations sur une authentification sortante initiale envoyée par le serveur d’authentification pour ce domaine au client qui a demandé l’authentification.</span><span class="sxs-lookup"><span data-stu-id="a1f21-106">Contains information about an initial outgoing authentication sent by the authentication server for this domain to the client that requested authentication.</span></span> <span data-ttu-id="a1f21-107">Le serveur qui utilise cet attribut reçoit l’autorisation du serveur d’authentification et l’envoie au client.</span><span class="sxs-lookup"><span data-stu-id="a1f21-107">The server that uses this attribute receives the authorization from the authentication server and sends it to the client.</span></span>



| <span data-ttu-id="a1f21-108">Entrée</span><span class="sxs-lookup"><span data-stu-id="a1f21-108">Entry</span></span> | <span data-ttu-id="a1f21-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="a1f21-109">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="a1f21-110">CN</span><span class="sxs-lookup"><span data-stu-id="a1f21-110">CN</span></span>                | <span data-ttu-id="a1f21-111">Initial-auth-sortante</span><span class="sxs-lookup"><span data-stu-id="a1f21-111">Initial-Auth-Outgoing</span></span>                       |
| <span data-ttu-id="a1f21-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="a1f21-112">Ldap-Display-Name</span></span> | <span data-ttu-id="a1f21-113">initialAuthOutgoing</span><span class="sxs-lookup"><span data-stu-id="a1f21-113">initialAuthOutgoing</span></span>                         |
| <span data-ttu-id="a1f21-114">Taille</span><span class="sxs-lookup"><span data-stu-id="a1f21-114">Size</span></span>              | \-                                          |
| <span data-ttu-id="a1f21-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="a1f21-115">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="a1f21-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="a1f21-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="a1f21-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a1f21-117">Attribute-Id</span></span>      | <span data-ttu-id="a1f21-118">1.2.840.113556.1.4.540</span><span class="sxs-lookup"><span data-stu-id="a1f21-118">1.2.840.113556.1.4.540</span></span>                      |
| <span data-ttu-id="a1f21-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a1f21-119">System-Id-Guid</span></span>    | <span data-ttu-id="a1f21-120">52458024-ca6a-11D0-AFFF-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="a1f21-120">52458024-ca6a-11d0-afff-0000f80367c1</span></span>        |
| <span data-ttu-id="a1f21-121">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a1f21-121">Syntax</span></span>            | [<span data-ttu-id="a1f21-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="a1f21-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="a1f21-123">Implémentations</span><span class="sxs-lookup"><span data-stu-id="a1f21-123">Implementations</span></span>

-   [<span data-ttu-id="a1f21-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a1f21-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a1f21-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a1f21-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a1f21-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a1f21-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a1f21-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a1f21-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a1f21-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a1f21-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a1f21-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a1f21-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a1f21-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a1f21-130">Windows 2000 Server</span></span>



| <span data-ttu-id="a1f21-131">Entrée</span><span class="sxs-lookup"><span data-stu-id="a1f21-131">Entry</span></span> | <span data-ttu-id="a1f21-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="a1f21-132">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="a1f21-133">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a1f21-133">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="a1f21-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a1f21-134">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="a1f21-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="a1f21-135">System-Only</span></span>            | <span data-ttu-id="a1f21-136">Faux</span><span class="sxs-lookup"><span data-stu-id="a1f21-136">False</span></span>                                                |
| <span data-ttu-id="a1f21-137">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a1f21-137">Is-Single-Valued</span></span>       | <span data-ttu-id="a1f21-138">Vrai</span><span class="sxs-lookup"><span data-stu-id="a1f21-138">True</span></span>                                                 |
| <span data-ttu-id="a1f21-139">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a1f21-139">Is Indexed</span></span>             | <span data-ttu-id="a1f21-140">Faux</span><span class="sxs-lookup"><span data-stu-id="a1f21-140">False</span></span>                                                |
| <span data-ttu-id="a1f21-141">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a1f21-141">In Global Catalog</span></span>      | <span data-ttu-id="a1f21-142">Faux</span><span class="sxs-lookup"><span data-stu-id="a1f21-142">False</span></span>                                                |
| <span data-ttu-id="a1f21-143">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a1f21-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="a1f21-144">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a1f21-144">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="a1f21-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a1f21-145">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="a1f21-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a1f21-146">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="a1f21-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a1f21-147">Search-Flags</span></span>           | <span data-ttu-id="a1f21-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a1f21-148">0x00000000</span></span>                                           |
| <span data-ttu-id="a1f21-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a1f21-149">System-Flags</span></span>           | <span data-ttu-id="a1f21-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a1f21-150">0x00000010</span></span>                                           |
| <span data-ttu-id="a1f21-151">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a1f21-151">Classes used in</span></span>        | [<span data-ttu-id="a1f21-152">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="a1f21-152">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a1f21-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a1f21-153">Windows Server 2003</span></span>



| <span data-ttu-id="a1f21-154">Entrée</span><span class="sxs-lookup"><span data-stu-id="a1f21-154">Entry</span></span> | <span data-ttu-id="a1f21-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="a1f21-155">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="a1f21-156">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a1f21-156">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="a1f21-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a1f21-157">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="a1f21-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="a1f21-158">System-Only</span></span>            | <span data-ttu-id="a1f21-159">Faux</span><span class="sxs-lookup"><span data-stu-id="a1f21-159">False</span></span>                                                |
| <span data-ttu-id="a1f21-160">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a1f21-160">Is-Single-Valued</span></span>       | <span data-ttu-id="a1f21-161">Vrai</span><span class="sxs-lookup"><span data-stu-id="a1f21-161">True</span></span>                                                 |
| <span data-ttu-id="a1f21-162">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a1f21-162">Is Indexed</span></span>             | <span data-ttu-id="a1f21-163">Faux</span><span class="sxs-lookup"><span data-stu-id="a1f21-163">False</span></span>                                                |
| <span data-ttu-id="a1f21-164">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a1f21-164">In Global Catalog</span></span>      | <span data-ttu-id="a1f21-165">Faux</span><span class="sxs-lookup"><span data-stu-id="a1f21-165">False</span></span>                                                |
| <span data-ttu-id="a1f21-166">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a1f21-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="a1f21-167">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a1f21-167">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="a1f21-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a1f21-168">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="a1f21-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a1f21-169">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="a1f21-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a1f21-170">Search-Flags</span></span>           | <span data-ttu-id="a1f21-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a1f21-171">0x00000000</span></span>                                           |
| <span data-ttu-id="a1f21-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a1f21-172">System-Flags</span></span>           | <span data-ttu-id="a1f21-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a1f21-173">0x00000010</span></span>                                           |
| <span data-ttu-id="a1f21-174">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a1f21-174">Classes used in</span></span>        | [<span data-ttu-id="a1f21-175">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="a1f21-175">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a1f21-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a1f21-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a1f21-177">Entrée</span><span class="sxs-lookup"><span data-stu-id="a1f21-177">Entry</span></span> | <span data-ttu-id="a1f21-178">Valeur</span><span class="sxs-lookup"><span data-stu-id="a1f21-178">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="a1f21-179">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a1f21-179">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="a1f21-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a1f21-180">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="a1f21-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="a1f21-181">System-Only</span></span>            | <span data-ttu-id="a1f21-182">Faux</span><span class="sxs-lookup"><span data-stu-id="a1f21-182">False</span></span>                                                |
| <span data-ttu-id="a1f21-183">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a1f21-183">Is-Single-Valued</span></span>       | <span data-ttu-id="a1f21-184">Vrai</span><span class="sxs-lookup"><span data-stu-id="a1f21-184">True</span></span>                                                 |
| <span data-ttu-id="a1f21-185">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a1f21-185">Is Indexed</span></span>             | <span data-ttu-id="a1f21-186">Faux</span><span class="sxs-lookup"><span data-stu-id="a1f21-186">False</span></span>                                                |
| <span data-ttu-id="a1f21-187">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a1f21-187">In Global Catalog</span></span>      | <span data-ttu-id="a1f21-188">Faux</span><span class="sxs-lookup"><span data-stu-id="a1f21-188">False</span></span>                                                |
| <span data-ttu-id="a1f21-189">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a1f21-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="a1f21-190">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a1f21-190">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="a1f21-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a1f21-191">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="a1f21-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a1f21-192">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="a1f21-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a1f21-193">Search-Flags</span></span>           | <span data-ttu-id="a1f21-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a1f21-194">0x00000000</span></span>                                           |
| <span data-ttu-id="a1f21-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a1f21-195">System-Flags</span></span>           | <span data-ttu-id="a1f21-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a1f21-196">0x00000010</span></span>                                           |
| <span data-ttu-id="a1f21-197">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a1f21-197">Classes used in</span></span>        | [<span data-ttu-id="a1f21-198">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="a1f21-198">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a1f21-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a1f21-199">Windows Server 2008</span></span>



| <span data-ttu-id="a1f21-200">Entrée</span><span class="sxs-lookup"><span data-stu-id="a1f21-200">Entry</span></span> | <span data-ttu-id="a1f21-201">Valeur</span><span class="sxs-lookup"><span data-stu-id="a1f21-201">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="a1f21-202">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a1f21-202">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="a1f21-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a1f21-203">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="a1f21-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="a1f21-204">System-Only</span></span>            | <span data-ttu-id="a1f21-205">Faux</span><span class="sxs-lookup"><span data-stu-id="a1f21-205">False</span></span>                                                |
| <span data-ttu-id="a1f21-206">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a1f21-206">Is-Single-Valued</span></span>       | <span data-ttu-id="a1f21-207">Vrai</span><span class="sxs-lookup"><span data-stu-id="a1f21-207">True</span></span>                                                 |
| <span data-ttu-id="a1f21-208">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a1f21-208">Is Indexed</span></span>             | <span data-ttu-id="a1f21-209">Faux</span><span class="sxs-lookup"><span data-stu-id="a1f21-209">False</span></span>                                                |
| <span data-ttu-id="a1f21-210">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a1f21-210">In Global Catalog</span></span>      | <span data-ttu-id="a1f21-211">Faux</span><span class="sxs-lookup"><span data-stu-id="a1f21-211">False</span></span>                                                |
| <span data-ttu-id="a1f21-212">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a1f21-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="a1f21-213">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a1f21-213">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="a1f21-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a1f21-214">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="a1f21-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a1f21-215">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="a1f21-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a1f21-216">Search-Flags</span></span>           | <span data-ttu-id="a1f21-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a1f21-217">0x00000000</span></span>                                           |
| <span data-ttu-id="a1f21-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a1f21-218">System-Flags</span></span>           | <span data-ttu-id="a1f21-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a1f21-219">0x00000010</span></span>                                           |
| <span data-ttu-id="a1f21-220">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a1f21-220">Classes used in</span></span>        | [<span data-ttu-id="a1f21-221">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="a1f21-221">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a1f21-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a1f21-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a1f21-223">Entrée</span><span class="sxs-lookup"><span data-stu-id="a1f21-223">Entry</span></span> | <span data-ttu-id="a1f21-224">Valeur</span><span class="sxs-lookup"><span data-stu-id="a1f21-224">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="a1f21-225">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a1f21-225">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="a1f21-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a1f21-226">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="a1f21-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="a1f21-227">System-Only</span></span>            | <span data-ttu-id="a1f21-228">Faux</span><span class="sxs-lookup"><span data-stu-id="a1f21-228">False</span></span>                                                |
| <span data-ttu-id="a1f21-229">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a1f21-229">Is-Single-Valued</span></span>       | <span data-ttu-id="a1f21-230">Vrai</span><span class="sxs-lookup"><span data-stu-id="a1f21-230">True</span></span>                                                 |
| <span data-ttu-id="a1f21-231">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a1f21-231">Is Indexed</span></span>             | <span data-ttu-id="a1f21-232">Faux</span><span class="sxs-lookup"><span data-stu-id="a1f21-232">False</span></span>                                                |
| <span data-ttu-id="a1f21-233">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a1f21-233">In Global Catalog</span></span>      | <span data-ttu-id="a1f21-234">Faux</span><span class="sxs-lookup"><span data-stu-id="a1f21-234">False</span></span>                                                |
| <span data-ttu-id="a1f21-235">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a1f21-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="a1f21-236">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a1f21-236">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="a1f21-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a1f21-237">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="a1f21-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a1f21-238">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="a1f21-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a1f21-239">Search-Flags</span></span>           | <span data-ttu-id="a1f21-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a1f21-240">0x00000000</span></span>                                           |
| <span data-ttu-id="a1f21-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a1f21-241">System-Flags</span></span>           | <span data-ttu-id="a1f21-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a1f21-242">0x00000010</span></span>                                           |
| <span data-ttu-id="a1f21-243">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a1f21-243">Classes used in</span></span>        | [<span data-ttu-id="a1f21-244">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="a1f21-244">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a1f21-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a1f21-245">Windows Server 2012</span></span>



| <span data-ttu-id="a1f21-246">Entrée</span><span class="sxs-lookup"><span data-stu-id="a1f21-246">Entry</span></span> | <span data-ttu-id="a1f21-247">Valeur</span><span class="sxs-lookup"><span data-stu-id="a1f21-247">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="a1f21-248">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a1f21-248">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="a1f21-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a1f21-249">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="a1f21-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="a1f21-250">System-Only</span></span>            | <span data-ttu-id="a1f21-251">Faux</span><span class="sxs-lookup"><span data-stu-id="a1f21-251">False</span></span>                                                |
| <span data-ttu-id="a1f21-252">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a1f21-252">Is-Single-Valued</span></span>       | <span data-ttu-id="a1f21-253">Vrai</span><span class="sxs-lookup"><span data-stu-id="a1f21-253">True</span></span>                                                 |
| <span data-ttu-id="a1f21-254">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a1f21-254">Is Indexed</span></span>             | <span data-ttu-id="a1f21-255">Faux</span><span class="sxs-lookup"><span data-stu-id="a1f21-255">False</span></span>                                                |
| <span data-ttu-id="a1f21-256">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a1f21-256">In Global Catalog</span></span>      | <span data-ttu-id="a1f21-257">Faux</span><span class="sxs-lookup"><span data-stu-id="a1f21-257">False</span></span>                                                |
| <span data-ttu-id="a1f21-258">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a1f21-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="a1f21-259">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a1f21-259">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="a1f21-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a1f21-260">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="a1f21-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a1f21-261">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="a1f21-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a1f21-262">Search-Flags</span></span>           | <span data-ttu-id="a1f21-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a1f21-263">0x00000000</span></span>                                           |
| <span data-ttu-id="a1f21-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a1f21-264">System-Flags</span></span>           | <span data-ttu-id="a1f21-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a1f21-265">0x00000010</span></span>                                           |
| <span data-ttu-id="a1f21-266">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a1f21-266">Classes used in</span></span>        | [<span data-ttu-id="a1f21-267">**Domaine approuvé**</span><span class="sxs-lookup"><span data-stu-id="a1f21-267">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





