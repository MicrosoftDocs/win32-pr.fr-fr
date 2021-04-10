---
title: SAM-Account-Name (attribut)
description: Nom d’ouverture de session utilisé pour prendre en charge les clients et les serveurs exécutant des versions antérieures du système d’exploitation, tels que Windows NT 4,0, Windows 95, Windows 98 et LAN Manager.
ms.assetid: dc661e59-9a36-4d2b-93f0-f88edf7efd66
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut SAM-Account-Name
- Schéma AD de l’attribut sAMAccountName
topic_type:
- apiref
api_name:
- SAM-Account-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cb64cba7825c3b4400641cdc5c62890f64bc299
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845313"
---
# <a name="sam-account-name-attribute"></a><span data-ttu-id="02db2-105">SAM-Account-Name (attribut)</span><span class="sxs-lookup"><span data-stu-id="02db2-105">SAM-Account-Name attribute</span></span>

<span data-ttu-id="02db2-106">Nom d’ouverture de session utilisé pour prendre en charge les clients et les serveurs exécutant des versions antérieures du système d’exploitation, tels que Windows NT 4,0, Windows 95, Windows 98 et LAN Manager.</span><span class="sxs-lookup"><span data-stu-id="02db2-106">The logon name used to support clients and servers running earlier versions of the operating system, such as Windows NT 4.0, Windows 95, Windows 98, and LAN Manager.</span></span>

<span data-ttu-id="02db2-107">Cet attribut doit comporter 20 caractères ou moins pour prendre en charge les clients antérieurs, et ne peut pas contenir l’un des caractères suivants :</span><span class="sxs-lookup"><span data-stu-id="02db2-107">This attribute must be 20 characters or less to support earlier clients, and cannot contain any of these characters:</span></span>

-   <span data-ttu-id="02db2-108">"/ \\ \[ \] : ; \| = , + \* ?</span><span class="sxs-lookup"><span data-stu-id="02db2-108">"/ \\ \[ \] : ; \| = , + \* ?</span></span> <span data-ttu-id="02db2-109">< ></span><span class="sxs-lookup"><span data-stu-id="02db2-109">< ></span></span>



| <span data-ttu-id="02db2-110">Entrée</span><span class="sxs-lookup"><span data-stu-id="02db2-110">Entry</span></span> | <span data-ttu-id="02db2-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="02db2-111">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="02db2-112">CN</span><span class="sxs-lookup"><span data-stu-id="02db2-112">CN</span></span>                | <span data-ttu-id="02db2-113">Nom de compte SAM</span><span class="sxs-lookup"><span data-stu-id="02db2-113">SAM-Account-Name</span></span>                                                                         |
| <span data-ttu-id="02db2-114">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="02db2-114">Ldap-Display-Name</span></span> | <span data-ttu-id="02db2-115">sAMAccountName</span><span class="sxs-lookup"><span data-stu-id="02db2-115">sAMAccountName</span></span>                                                                           |
| <span data-ttu-id="02db2-116">Taille</span><span class="sxs-lookup"><span data-stu-id="02db2-116">Size</span></span>              | <span data-ttu-id="02db2-117">20 caractères au maximum.</span><span class="sxs-lookup"><span data-stu-id="02db2-117">20 characters or less.</span></span>                                                                   |
| <span data-ttu-id="02db2-118">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="02db2-118">Update Privilege</span></span>  | <span data-ttu-id="02db2-119">Administrateur de domaine</span><span class="sxs-lookup"><span data-stu-id="02db2-119">Domain administrator</span></span>                                                                     |
| <span data-ttu-id="02db2-120">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="02db2-120">Update Frequency</span></span>  | <span data-ttu-id="02db2-121">Cette valeur doit être affectée lorsque l’enregistrement de compte est créé et ne doit pas être modifié.</span><span class="sxs-lookup"><span data-stu-id="02db2-121">This value should be assigned when the account record is created, and should not change.</span></span> |
| <span data-ttu-id="02db2-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="02db2-122">Attribute-Id</span></span>      | <span data-ttu-id="02db2-123">1.2.840.113556.1.4.221</span><span class="sxs-lookup"><span data-stu-id="02db2-123">1.2.840.113556.1.4.221</span></span>                                                                   |
| <span data-ttu-id="02db2-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="02db2-124">System-Id-Guid</span></span>    | <span data-ttu-id="02db2-125">3e0abfd0-126a-11d0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="02db2-125">3e0abfd0-126a-11d0-a060-00aa006c33ed</span></span>                                                     |
| <span data-ttu-id="02db2-126">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="02db2-126">Syntax</span></span>            | [<span data-ttu-id="02db2-127">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="02db2-127">**String(Unicode)**</span></span>](s-string-unicode.md)                                              |



## <a name="implementations"></a><span data-ttu-id="02db2-128">Implémentations</span><span class="sxs-lookup"><span data-stu-id="02db2-128">Implementations</span></span>

-   [<span data-ttu-id="02db2-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="02db2-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="02db2-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="02db2-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="02db2-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="02db2-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="02db2-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="02db2-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="02db2-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="02db2-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="02db2-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="02db2-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="02db2-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="02db2-135">Windows 2000 Server</span></span>



| <span data-ttu-id="02db2-136">Entrée</span><span class="sxs-lookup"><span data-stu-id="02db2-136">Entry</span></span> | <span data-ttu-id="02db2-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="02db2-137">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="02db2-138">ID de lien</span><span class="sxs-lookup"><span data-stu-id="02db2-138">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="02db2-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="02db2-139">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="02db2-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="02db2-140">System-Only</span></span>            | <span data-ttu-id="02db2-141">Faux</span><span class="sxs-lookup"><span data-stu-id="02db2-141">False</span></span>                                                        |
| <span data-ttu-id="02db2-142">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="02db2-142">Is-Single-Valued</span></span>       | <span data-ttu-id="02db2-143">Vrai</span><span class="sxs-lookup"><span data-stu-id="02db2-143">True</span></span>                                                         |
| <span data-ttu-id="02db2-144">Est indexé</span><span class="sxs-lookup"><span data-stu-id="02db2-144">Is Indexed</span></span>             | <span data-ttu-id="02db2-145">Vrai</span><span class="sxs-lookup"><span data-stu-id="02db2-145">True</span></span>                                                         |
| <span data-ttu-id="02db2-146">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="02db2-146">In Global Catalog</span></span>      | <span data-ttu-id="02db2-147">Vrai</span><span class="sxs-lookup"><span data-stu-id="02db2-147">True</span></span>                                                         |
| <span data-ttu-id="02db2-148">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="02db2-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="02db2-149">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="02db2-149">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="02db2-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="02db2-150">Range-Lower</span></span>            | <span data-ttu-id="02db2-151">0</span><span class="sxs-lookup"><span data-stu-id="02db2-151">0</span></span>                                                            |
| <span data-ttu-id="02db2-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="02db2-152">Range-Upper</span></span>            | <span data-ttu-id="02db2-153">256</span><span class="sxs-lookup"><span data-stu-id="02db2-153">256</span></span>                                                          |
| <span data-ttu-id="02db2-154">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="02db2-154">Search-Flags</span></span>           | <span data-ttu-id="02db2-155">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="02db2-155">0x0000000D</span></span>                                                   |
| <span data-ttu-id="02db2-156">System-Flags</span><span class="sxs-lookup"><span data-stu-id="02db2-156">System-Flags</span></span>           | <span data-ttu-id="02db2-157">0x00000012</span><span class="sxs-lookup"><span data-stu-id="02db2-157">0x00000012</span></span>                                                   |
| <span data-ttu-id="02db2-158">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="02db2-158">Classes used in</span></span>        | [<span data-ttu-id="02db2-159">**Sécurité-principal**</span><span class="sxs-lookup"><span data-stu-id="02db2-159">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="02db2-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="02db2-160">Windows Server 2003</span></span>



| <span data-ttu-id="02db2-161">Entrée</span><span class="sxs-lookup"><span data-stu-id="02db2-161">Entry</span></span> | <span data-ttu-id="02db2-162">Valeur</span><span class="sxs-lookup"><span data-stu-id="02db2-162">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="02db2-163">ID de lien</span><span class="sxs-lookup"><span data-stu-id="02db2-163">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="02db2-164">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="02db2-164">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="02db2-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="02db2-165">System-Only</span></span>            | <span data-ttu-id="02db2-166">Faux</span><span class="sxs-lookup"><span data-stu-id="02db2-166">False</span></span>                                                        |
| <span data-ttu-id="02db2-167">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="02db2-167">Is-Single-Valued</span></span>       | <span data-ttu-id="02db2-168">Vrai</span><span class="sxs-lookup"><span data-stu-id="02db2-168">True</span></span>                                                         |
| <span data-ttu-id="02db2-169">Est indexé</span><span class="sxs-lookup"><span data-stu-id="02db2-169">Is Indexed</span></span>             | <span data-ttu-id="02db2-170">Vrai</span><span class="sxs-lookup"><span data-stu-id="02db2-170">True</span></span>                                                         |
| <span data-ttu-id="02db2-171">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="02db2-171">In Global Catalog</span></span>      | <span data-ttu-id="02db2-172">Vrai</span><span class="sxs-lookup"><span data-stu-id="02db2-172">True</span></span>                                                         |
| <span data-ttu-id="02db2-173">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="02db2-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="02db2-174">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="02db2-174">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="02db2-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="02db2-175">Range-Lower</span></span>            | <span data-ttu-id="02db2-176">0</span><span class="sxs-lookup"><span data-stu-id="02db2-176">0</span></span>                                                            |
| <span data-ttu-id="02db2-177">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="02db2-177">Range-Upper</span></span>            | <span data-ttu-id="02db2-178">256</span><span class="sxs-lookup"><span data-stu-id="02db2-178">256</span></span>                                                          |
| <span data-ttu-id="02db2-179">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="02db2-179">Search-Flags</span></span>           | <span data-ttu-id="02db2-180">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="02db2-180">0x0000000D</span></span>                                                   |
| <span data-ttu-id="02db2-181">System-Flags</span><span class="sxs-lookup"><span data-stu-id="02db2-181">System-Flags</span></span>           | <span data-ttu-id="02db2-182">0x00000012</span><span class="sxs-lookup"><span data-stu-id="02db2-182">0x00000012</span></span>                                                   |
| <span data-ttu-id="02db2-183">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="02db2-183">Classes used in</span></span>        | [<span data-ttu-id="02db2-184">**Sécurité-principal**</span><span class="sxs-lookup"><span data-stu-id="02db2-184">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="02db2-185">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="02db2-185">Windows Server 2003 R2</span></span>



| <span data-ttu-id="02db2-186">Entrée</span><span class="sxs-lookup"><span data-stu-id="02db2-186">Entry</span></span> | <span data-ttu-id="02db2-187">Valeur</span><span class="sxs-lookup"><span data-stu-id="02db2-187">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="02db2-188">ID de lien</span><span class="sxs-lookup"><span data-stu-id="02db2-188">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="02db2-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="02db2-189">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="02db2-190">System-Only</span><span class="sxs-lookup"><span data-stu-id="02db2-190">System-Only</span></span>            | <span data-ttu-id="02db2-191">Faux</span><span class="sxs-lookup"><span data-stu-id="02db2-191">False</span></span>                                                        |
| <span data-ttu-id="02db2-192">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="02db2-192">Is-Single-Valued</span></span>       | <span data-ttu-id="02db2-193">Vrai</span><span class="sxs-lookup"><span data-stu-id="02db2-193">True</span></span>                                                         |
| <span data-ttu-id="02db2-194">Est indexé</span><span class="sxs-lookup"><span data-stu-id="02db2-194">Is Indexed</span></span>             | <span data-ttu-id="02db2-195">Vrai</span><span class="sxs-lookup"><span data-stu-id="02db2-195">True</span></span>                                                         |
| <span data-ttu-id="02db2-196">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="02db2-196">In Global Catalog</span></span>      | <span data-ttu-id="02db2-197">Vrai</span><span class="sxs-lookup"><span data-stu-id="02db2-197">True</span></span>                                                         |
| <span data-ttu-id="02db2-198">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="02db2-198">NT-Security-Descriptor</span></span> | <span data-ttu-id="02db2-199">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="02db2-199">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="02db2-200">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="02db2-200">Range-Lower</span></span>            | <span data-ttu-id="02db2-201">0</span><span class="sxs-lookup"><span data-stu-id="02db2-201">0</span></span>                                                            |
| <span data-ttu-id="02db2-202">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="02db2-202">Range-Upper</span></span>            | <span data-ttu-id="02db2-203">256</span><span class="sxs-lookup"><span data-stu-id="02db2-203">256</span></span>                                                          |
| <span data-ttu-id="02db2-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="02db2-204">Search-Flags</span></span>           | <span data-ttu-id="02db2-205">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="02db2-205">0x0000000D</span></span>                                                   |
| <span data-ttu-id="02db2-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="02db2-206">System-Flags</span></span>           | <span data-ttu-id="02db2-207">0x00000012</span><span class="sxs-lookup"><span data-stu-id="02db2-207">0x00000012</span></span>                                                   |
| <span data-ttu-id="02db2-208">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="02db2-208">Classes used in</span></span>        | [<span data-ttu-id="02db2-209">**Sécurité-principal**</span><span class="sxs-lookup"><span data-stu-id="02db2-209">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="02db2-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="02db2-210">Windows Server 2008</span></span>



| <span data-ttu-id="02db2-211">Entrée</span><span class="sxs-lookup"><span data-stu-id="02db2-211">Entry</span></span> | <span data-ttu-id="02db2-212">Valeur</span><span class="sxs-lookup"><span data-stu-id="02db2-212">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="02db2-213">ID de lien</span><span class="sxs-lookup"><span data-stu-id="02db2-213">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="02db2-214">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="02db2-214">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="02db2-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="02db2-215">System-Only</span></span>            | <span data-ttu-id="02db2-216">Faux</span><span class="sxs-lookup"><span data-stu-id="02db2-216">False</span></span>                                                        |
| <span data-ttu-id="02db2-217">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="02db2-217">Is-Single-Valued</span></span>       | <span data-ttu-id="02db2-218">Vrai</span><span class="sxs-lookup"><span data-stu-id="02db2-218">True</span></span>                                                         |
| <span data-ttu-id="02db2-219">Est indexé</span><span class="sxs-lookup"><span data-stu-id="02db2-219">Is Indexed</span></span>             | <span data-ttu-id="02db2-220">Vrai</span><span class="sxs-lookup"><span data-stu-id="02db2-220">True</span></span>                                                         |
| <span data-ttu-id="02db2-221">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="02db2-221">In Global Catalog</span></span>      | <span data-ttu-id="02db2-222">Vrai</span><span class="sxs-lookup"><span data-stu-id="02db2-222">True</span></span>                                                         |
| <span data-ttu-id="02db2-223">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="02db2-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="02db2-224">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="02db2-224">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="02db2-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="02db2-225">Range-Lower</span></span>            | <span data-ttu-id="02db2-226">0</span><span class="sxs-lookup"><span data-stu-id="02db2-226">0</span></span>                                                            |
| <span data-ttu-id="02db2-227">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="02db2-227">Range-Upper</span></span>            | <span data-ttu-id="02db2-228">256</span><span class="sxs-lookup"><span data-stu-id="02db2-228">256</span></span>                                                          |
| <span data-ttu-id="02db2-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="02db2-229">Search-Flags</span></span>           | <span data-ttu-id="02db2-230">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="02db2-230">0x0000000D</span></span>                                                   |
| <span data-ttu-id="02db2-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="02db2-231">System-Flags</span></span>           | <span data-ttu-id="02db2-232">0x00000012</span><span class="sxs-lookup"><span data-stu-id="02db2-232">0x00000012</span></span>                                                   |
| <span data-ttu-id="02db2-233">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="02db2-233">Classes used in</span></span>        | [<span data-ttu-id="02db2-234">**Sécurité-principal**</span><span class="sxs-lookup"><span data-stu-id="02db2-234">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="02db2-235">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="02db2-235">Windows Server 2008 R2</span></span>



| <span data-ttu-id="02db2-236">Entrée</span><span class="sxs-lookup"><span data-stu-id="02db2-236">Entry</span></span> | <span data-ttu-id="02db2-237">Valeur</span><span class="sxs-lookup"><span data-stu-id="02db2-237">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="02db2-238">ID de lien</span><span class="sxs-lookup"><span data-stu-id="02db2-238">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="02db2-239">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="02db2-239">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="02db2-240">System-Only</span><span class="sxs-lookup"><span data-stu-id="02db2-240">System-Only</span></span>            | <span data-ttu-id="02db2-241">Faux</span><span class="sxs-lookup"><span data-stu-id="02db2-241">False</span></span>                                                        |
| <span data-ttu-id="02db2-242">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="02db2-242">Is-Single-Valued</span></span>       | <span data-ttu-id="02db2-243">Vrai</span><span class="sxs-lookup"><span data-stu-id="02db2-243">True</span></span>                                                         |
| <span data-ttu-id="02db2-244">Est indexé</span><span class="sxs-lookup"><span data-stu-id="02db2-244">Is Indexed</span></span>             | <span data-ttu-id="02db2-245">Vrai</span><span class="sxs-lookup"><span data-stu-id="02db2-245">True</span></span>                                                         |
| <span data-ttu-id="02db2-246">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="02db2-246">In Global Catalog</span></span>      | <span data-ttu-id="02db2-247">Vrai</span><span class="sxs-lookup"><span data-stu-id="02db2-247">True</span></span>                                                         |
| <span data-ttu-id="02db2-248">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="02db2-248">NT-Security-Descriptor</span></span> | <span data-ttu-id="02db2-249">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="02db2-249">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="02db2-250">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="02db2-250">Range-Lower</span></span>            | <span data-ttu-id="02db2-251">0</span><span class="sxs-lookup"><span data-stu-id="02db2-251">0</span></span>                                                            |
| <span data-ttu-id="02db2-252">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="02db2-252">Range-Upper</span></span>            | <span data-ttu-id="02db2-253">256</span><span class="sxs-lookup"><span data-stu-id="02db2-253">256</span></span>                                                          |
| <span data-ttu-id="02db2-254">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="02db2-254">Search-Flags</span></span>           | <span data-ttu-id="02db2-255">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="02db2-255">0x0000000D</span></span>                                                   |
| <span data-ttu-id="02db2-256">System-Flags</span><span class="sxs-lookup"><span data-stu-id="02db2-256">System-Flags</span></span>           | <span data-ttu-id="02db2-257">0x00000012</span><span class="sxs-lookup"><span data-stu-id="02db2-257">0x00000012</span></span>                                                   |
| <span data-ttu-id="02db2-258">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="02db2-258">Classes used in</span></span>        | [<span data-ttu-id="02db2-259">**Sécurité-principal**</span><span class="sxs-lookup"><span data-stu-id="02db2-259">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="02db2-260">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="02db2-260">Windows Server 2012</span></span>



| <span data-ttu-id="02db2-261">Entrée</span><span class="sxs-lookup"><span data-stu-id="02db2-261">Entry</span></span> | <span data-ttu-id="02db2-262">Valeur</span><span class="sxs-lookup"><span data-stu-id="02db2-262">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="02db2-263">ID de lien</span><span class="sxs-lookup"><span data-stu-id="02db2-263">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="02db2-264">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="02db2-264">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="02db2-265">System-Only</span><span class="sxs-lookup"><span data-stu-id="02db2-265">System-Only</span></span>            | <span data-ttu-id="02db2-266">Faux</span><span class="sxs-lookup"><span data-stu-id="02db2-266">False</span></span>                                                        |
| <span data-ttu-id="02db2-267">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="02db2-267">Is-Single-Valued</span></span>       | <span data-ttu-id="02db2-268">Vrai</span><span class="sxs-lookup"><span data-stu-id="02db2-268">True</span></span>                                                         |
| <span data-ttu-id="02db2-269">Est indexé</span><span class="sxs-lookup"><span data-stu-id="02db2-269">Is Indexed</span></span>             | <span data-ttu-id="02db2-270">Vrai</span><span class="sxs-lookup"><span data-stu-id="02db2-270">True</span></span>                                                         |
| <span data-ttu-id="02db2-271">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="02db2-271">In Global Catalog</span></span>      | <span data-ttu-id="02db2-272">Vrai</span><span class="sxs-lookup"><span data-stu-id="02db2-272">True</span></span>                                                         |
| <span data-ttu-id="02db2-273">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="02db2-273">NT-Security-Descriptor</span></span> | <span data-ttu-id="02db2-274">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="02db2-274">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="02db2-275">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="02db2-275">Range-Lower</span></span>            | <span data-ttu-id="02db2-276">0</span><span class="sxs-lookup"><span data-stu-id="02db2-276">0</span></span>                                                            |
| <span data-ttu-id="02db2-277">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="02db2-277">Range-Upper</span></span>            | <span data-ttu-id="02db2-278">256</span><span class="sxs-lookup"><span data-stu-id="02db2-278">256</span></span>                                                          |
| <span data-ttu-id="02db2-279">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="02db2-279">Search-Flags</span></span>           | <span data-ttu-id="02db2-280">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="02db2-280">0x0000000D</span></span>                                                   |
| <span data-ttu-id="02db2-281">System-Flags</span><span class="sxs-lookup"><span data-stu-id="02db2-281">System-Flags</span></span>           | <span data-ttu-id="02db2-282">0x00000012</span><span class="sxs-lookup"><span data-stu-id="02db2-282">0x00000012</span></span>                                                   |
| <span data-ttu-id="02db2-283">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="02db2-283">Classes used in</span></span>        | [<span data-ttu-id="02db2-284">**Sécurité-principal**</span><span class="sxs-lookup"><span data-stu-id="02db2-284">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



 

 





