---
title: Attribut Proxy-Addresses
description: Une adresse proxy est l’adresse par laquelle un objet destinataire Microsoft Exchange Server est reconnu dans un système de messagerie étranger. Des adresses proxy sont requises pour tous les objets destinataires, tels que les destinataires personnalisés et les listes de distribution.
ms.assetid: 7bb299d8-e67a-4062-91a3-b579fd71d5c9
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Proxy-Addresses
- Schéma Active Directory d’attribut proxyAddresses
topic_type:
- apiref
api_name:
- Proxy-Addresses
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a03542cef9bca48dbba1585e3837056b53673f34
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845326"
---
# <a name="proxy-addresses-attribute"></a><span data-ttu-id="e9dcb-106">Attribut Proxy-Addresses</span><span class="sxs-lookup"><span data-stu-id="e9dcb-106">Proxy-Addresses attribute</span></span>

<span data-ttu-id="e9dcb-107">Une adresse proxy est l’adresse par laquelle un objet destinataire Microsoft Exchange Server est reconnu dans un système de messagerie étranger.</span><span class="sxs-lookup"><span data-stu-id="e9dcb-107">A proxy address is the address by which a Microsoft Exchange Server recipient object is recognized in a foreign mail system.</span></span> <span data-ttu-id="e9dcb-108">Des adresses proxy sont requises pour tous les objets destinataires, tels que les destinataires personnalisés et les listes de distribution.</span><span class="sxs-lookup"><span data-stu-id="e9dcb-108">Proxy addresses are required for all recipient objects, such as custom recipients and distribution lists.</span></span>



| <span data-ttu-id="e9dcb-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="e9dcb-109">Entry</span></span> | <span data-ttu-id="e9dcb-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="e9dcb-110">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9dcb-111">CN</span><span class="sxs-lookup"><span data-stu-id="e9dcb-111">CN</span></span>                | <span data-ttu-id="e9dcb-112">Proxy-Addresses</span><span class="sxs-lookup"><span data-stu-id="e9dcb-112">Proxy-Addresses</span></span>                                                                                      |
| <span data-ttu-id="e9dcb-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="e9dcb-113">Ldap-Display-Name</span></span> | <span data-ttu-id="e9dcb-114">proxyAddresses</span><span class="sxs-lookup"><span data-stu-id="e9dcb-114">proxyAddresses</span></span>                                                                                       |
| <span data-ttu-id="e9dcb-115">Taille</span><span class="sxs-lookup"><span data-stu-id="e9dcb-115">Size</span></span>              | \-                                                                                                   |
| <span data-ttu-id="e9dcb-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="e9dcb-116">Update Privilege</span></span>  | <span data-ttu-id="e9dcb-117">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="e9dcb-117">This value is set by the system.</span></span>                                                                     |
| <span data-ttu-id="e9dcb-118">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="e9dcb-118">Update Frequency</span></span>  | <span data-ttu-id="e9dcb-119">Créé par une DLL fournie avec l’objet Address-Type Directory lorsque le type d’adresse est installé.</span><span class="sxs-lookup"><span data-stu-id="e9dcb-119">Created by a DLL provided with the Address-Type directory object when the address type is installed.</span></span> |
| <span data-ttu-id="e9dcb-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e9dcb-120">Attribute-Id</span></span>      | <span data-ttu-id="e9dcb-121">1.2.840.113556.1.2.210</span><span class="sxs-lookup"><span data-stu-id="e9dcb-121">1.2.840.113556.1.2.210</span></span>                                                                               |
| <span data-ttu-id="e9dcb-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="e9dcb-122">System-Id-Guid</span></span>    | <span data-ttu-id="e9dcb-123">bf967a06-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="e9dcb-123">bf967a06-0de6-11d0-a285-00aa003049e2</span></span>                                                                 |
| <span data-ttu-id="e9dcb-124">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e9dcb-124">Syntax</span></span>            | [<span data-ttu-id="e9dcb-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="e9dcb-125">**String(Unicode)**</span></span>](s-string-unicode.md)                                                          |



## <a name="implementations"></a><span data-ttu-id="e9dcb-126">Implémentations</span><span class="sxs-lookup"><span data-stu-id="e9dcb-126">Implementations</span></span>

-   [<span data-ttu-id="e9dcb-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e9dcb-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e9dcb-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e9dcb-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e9dcb-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="e9dcb-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="e9dcb-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e9dcb-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e9dcb-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e9dcb-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e9dcb-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e9dcb-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e9dcb-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e9dcb-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e9dcb-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e9dcb-134">Windows 2000 Server</span></span>



| <span data-ttu-id="e9dcb-135">Entrée</span><span class="sxs-lookup"><span data-stu-id="e9dcb-135">Entry</span></span> | <span data-ttu-id="e9dcb-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="e9dcb-136">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e9dcb-137">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e9dcb-137">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e9dcb-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e9dcb-138">MAPI-Id</span></span>                | <span data-ttu-id="e9dcb-139">0x800F</span><span class="sxs-lookup"><span data-stu-id="e9dcb-139">0x800F</span></span>                          |
| <span data-ttu-id="e9dcb-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="e9dcb-140">System-Only</span></span>            | <span data-ttu-id="e9dcb-141">Faux</span><span class="sxs-lookup"><span data-stu-id="e9dcb-141">False</span></span>                           |
| <span data-ttu-id="e9dcb-142">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e9dcb-142">Is-Single-Valued</span></span>       | <span data-ttu-id="e9dcb-143">Faux</span><span class="sxs-lookup"><span data-stu-id="e9dcb-143">False</span></span>                           |
| <span data-ttu-id="e9dcb-144">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e9dcb-144">Is Indexed</span></span>             | <span data-ttu-id="e9dcb-145">Vrai</span><span class="sxs-lookup"><span data-stu-id="e9dcb-145">True</span></span>                            |
| <span data-ttu-id="e9dcb-146">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e9dcb-146">In Global Catalog</span></span>      | <span data-ttu-id="e9dcb-147">Faux</span><span class="sxs-lookup"><span data-stu-id="e9dcb-147">False</span></span>                           |
| <span data-ttu-id="e9dcb-148">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e9dcb-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="e9dcb-149">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e9dcb-149">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e9dcb-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e9dcb-150">Range-Lower</span></span>            | <span data-ttu-id="e9dcb-151">1</span><span class="sxs-lookup"><span data-stu-id="e9dcb-151">1</span></span>                               |
| <span data-ttu-id="e9dcb-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e9dcb-152">Range-Upper</span></span>            | <span data-ttu-id="e9dcb-153">1123</span><span class="sxs-lookup"><span data-stu-id="e9dcb-153">1123</span></span>                            |
| <span data-ttu-id="e9dcb-154">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e9dcb-154">Search-Flags</span></span>           | <span data-ttu-id="e9dcb-155">0x00000005</span><span class="sxs-lookup"><span data-stu-id="e9dcb-155">0x00000005</span></span>                      |
| <span data-ttu-id="e9dcb-156">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e9dcb-156">System-Flags</span></span>           | <span data-ttu-id="e9dcb-157">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e9dcb-157">0x00000010</span></span>                      |
| <span data-ttu-id="e9dcb-158">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e9dcb-158">Classes used in</span></span>        | [<span data-ttu-id="e9dcb-159">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="e9dcb-159">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e9dcb-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e9dcb-160">Windows Server 2003</span></span>



| <span data-ttu-id="e9dcb-161">Entrée</span><span class="sxs-lookup"><span data-stu-id="e9dcb-161">Entry</span></span> | <span data-ttu-id="e9dcb-162">Valeur</span><span class="sxs-lookup"><span data-stu-id="e9dcb-162">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e9dcb-163">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e9dcb-163">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e9dcb-164">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e9dcb-164">MAPI-Id</span></span>                | <span data-ttu-id="e9dcb-165">0x800F</span><span class="sxs-lookup"><span data-stu-id="e9dcb-165">0x800F</span></span>                          |
| <span data-ttu-id="e9dcb-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="e9dcb-166">System-Only</span></span>            | <span data-ttu-id="e9dcb-167">Faux</span><span class="sxs-lookup"><span data-stu-id="e9dcb-167">False</span></span>                           |
| <span data-ttu-id="e9dcb-168">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e9dcb-168">Is-Single-Valued</span></span>       | <span data-ttu-id="e9dcb-169">Faux</span><span class="sxs-lookup"><span data-stu-id="e9dcb-169">False</span></span>                           |
| <span data-ttu-id="e9dcb-170">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e9dcb-170">Is Indexed</span></span>             | <span data-ttu-id="e9dcb-171">Vrai</span><span class="sxs-lookup"><span data-stu-id="e9dcb-171">True</span></span>                            |
| <span data-ttu-id="e9dcb-172">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e9dcb-172">In Global Catalog</span></span>      | <span data-ttu-id="e9dcb-173">Faux</span><span class="sxs-lookup"><span data-stu-id="e9dcb-173">False</span></span>                           |
| <span data-ttu-id="e9dcb-174">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e9dcb-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="e9dcb-175">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e9dcb-175">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e9dcb-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e9dcb-176">Range-Lower</span></span>            | <span data-ttu-id="e9dcb-177">1</span><span class="sxs-lookup"><span data-stu-id="e9dcb-177">1</span></span>                               |
| <span data-ttu-id="e9dcb-178">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e9dcb-178">Range-Upper</span></span>            | <span data-ttu-id="e9dcb-179">1123</span><span class="sxs-lookup"><span data-stu-id="e9dcb-179">1123</span></span>                            |
| <span data-ttu-id="e9dcb-180">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e9dcb-180">Search-Flags</span></span>           | <span data-ttu-id="e9dcb-181">0x00000005</span><span class="sxs-lookup"><span data-stu-id="e9dcb-181">0x00000005</span></span>                      |
| <span data-ttu-id="e9dcb-182">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e9dcb-182">System-Flags</span></span>           | <span data-ttu-id="e9dcb-183">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e9dcb-183">0x00000010</span></span>                      |
| <span data-ttu-id="e9dcb-184">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e9dcb-184">Classes used in</span></span>        | [<span data-ttu-id="e9dcb-185">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="e9dcb-185">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="e9dcb-186">ADAM</span><span class="sxs-lookup"><span data-stu-id="e9dcb-186">ADAM</span></span>



| <span data-ttu-id="e9dcb-187">Entrée</span><span class="sxs-lookup"><span data-stu-id="e9dcb-187">Entry</span></span> | <span data-ttu-id="e9dcb-188">Valeur</span><span class="sxs-lookup"><span data-stu-id="e9dcb-188">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e9dcb-189">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e9dcb-189">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e9dcb-190">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e9dcb-190">MAPI-Id</span></span>                | <span data-ttu-id="e9dcb-191">0x800F</span><span class="sxs-lookup"><span data-stu-id="e9dcb-191">0x800F</span></span>                          |
| <span data-ttu-id="e9dcb-192">System-Only</span><span class="sxs-lookup"><span data-stu-id="e9dcb-192">System-Only</span></span>            | <span data-ttu-id="e9dcb-193">Faux</span><span class="sxs-lookup"><span data-stu-id="e9dcb-193">False</span></span>                           |
| <span data-ttu-id="e9dcb-194">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e9dcb-194">Is-Single-Valued</span></span>       | <span data-ttu-id="e9dcb-195">Faux</span><span class="sxs-lookup"><span data-stu-id="e9dcb-195">False</span></span>                           |
| <span data-ttu-id="e9dcb-196">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e9dcb-196">Is Indexed</span></span>             | <span data-ttu-id="e9dcb-197">Vrai</span><span class="sxs-lookup"><span data-stu-id="e9dcb-197">True</span></span>                            |
| <span data-ttu-id="e9dcb-198">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e9dcb-198">In Global Catalog</span></span>      | <span data-ttu-id="e9dcb-199">Faux</span><span class="sxs-lookup"><span data-stu-id="e9dcb-199">False</span></span>                           |
| <span data-ttu-id="e9dcb-200">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e9dcb-200">NT-Security-Descriptor</span></span> | <span data-ttu-id="e9dcb-201">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e9dcb-201">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e9dcb-202">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e9dcb-202">Range-Lower</span></span>            | <span data-ttu-id="e9dcb-203">1</span><span class="sxs-lookup"><span data-stu-id="e9dcb-203">1</span></span>                               |
| <span data-ttu-id="e9dcb-204">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e9dcb-204">Range-Upper</span></span>            | <span data-ttu-id="e9dcb-205">1123</span><span class="sxs-lookup"><span data-stu-id="e9dcb-205">1123</span></span>                            |
| <span data-ttu-id="e9dcb-206">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e9dcb-206">Search-Flags</span></span>           | <span data-ttu-id="e9dcb-207">0x00000005</span><span class="sxs-lookup"><span data-stu-id="e9dcb-207">0x00000005</span></span>                      |
| <span data-ttu-id="e9dcb-208">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e9dcb-208">System-Flags</span></span>           | <span data-ttu-id="e9dcb-209">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e9dcb-209">0x00000010</span></span>                      |
| <span data-ttu-id="e9dcb-210">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e9dcb-210">Classes used in</span></span>        | [<span data-ttu-id="e9dcb-211">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="e9dcb-211">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e9dcb-212">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e9dcb-212">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e9dcb-213">Entrée</span><span class="sxs-lookup"><span data-stu-id="e9dcb-213">Entry</span></span> | <span data-ttu-id="e9dcb-214">Valeur</span><span class="sxs-lookup"><span data-stu-id="e9dcb-214">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e9dcb-215">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e9dcb-215">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e9dcb-216">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e9dcb-216">MAPI-Id</span></span>                | <span data-ttu-id="e9dcb-217">0x800F</span><span class="sxs-lookup"><span data-stu-id="e9dcb-217">0x800F</span></span>                          |
| <span data-ttu-id="e9dcb-218">System-Only</span><span class="sxs-lookup"><span data-stu-id="e9dcb-218">System-Only</span></span>            | <span data-ttu-id="e9dcb-219">Faux</span><span class="sxs-lookup"><span data-stu-id="e9dcb-219">False</span></span>                           |
| <span data-ttu-id="e9dcb-220">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e9dcb-220">Is-Single-Valued</span></span>       | <span data-ttu-id="e9dcb-221">Faux</span><span class="sxs-lookup"><span data-stu-id="e9dcb-221">False</span></span>                           |
| <span data-ttu-id="e9dcb-222">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e9dcb-222">Is Indexed</span></span>             | <span data-ttu-id="e9dcb-223">Vrai</span><span class="sxs-lookup"><span data-stu-id="e9dcb-223">True</span></span>                            |
| <span data-ttu-id="e9dcb-224">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e9dcb-224">In Global Catalog</span></span>      | <span data-ttu-id="e9dcb-225">Faux</span><span class="sxs-lookup"><span data-stu-id="e9dcb-225">False</span></span>                           |
| <span data-ttu-id="e9dcb-226">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e9dcb-226">NT-Security-Descriptor</span></span> | <span data-ttu-id="e9dcb-227">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e9dcb-227">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e9dcb-228">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e9dcb-228">Range-Lower</span></span>            | <span data-ttu-id="e9dcb-229">1</span><span class="sxs-lookup"><span data-stu-id="e9dcb-229">1</span></span>                               |
| <span data-ttu-id="e9dcb-230">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e9dcb-230">Range-Upper</span></span>            | <span data-ttu-id="e9dcb-231">1123</span><span class="sxs-lookup"><span data-stu-id="e9dcb-231">1123</span></span>                            |
| <span data-ttu-id="e9dcb-232">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e9dcb-232">Search-Flags</span></span>           | <span data-ttu-id="e9dcb-233">0x00000005</span><span class="sxs-lookup"><span data-stu-id="e9dcb-233">0x00000005</span></span>                      |
| <span data-ttu-id="e9dcb-234">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e9dcb-234">System-Flags</span></span>           | <span data-ttu-id="e9dcb-235">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e9dcb-235">0x00000010</span></span>                      |
| <span data-ttu-id="e9dcb-236">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e9dcb-236">Classes used in</span></span>        | [<span data-ttu-id="e9dcb-237">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="e9dcb-237">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e9dcb-238">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e9dcb-238">Windows Server 2008</span></span>



| <span data-ttu-id="e9dcb-239">Entrée</span><span class="sxs-lookup"><span data-stu-id="e9dcb-239">Entry</span></span> | <span data-ttu-id="e9dcb-240">Valeur</span><span class="sxs-lookup"><span data-stu-id="e9dcb-240">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e9dcb-241">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e9dcb-241">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e9dcb-242">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e9dcb-242">MAPI-Id</span></span>                | <span data-ttu-id="e9dcb-243">0x800F</span><span class="sxs-lookup"><span data-stu-id="e9dcb-243">0x800F</span></span>                          |
| <span data-ttu-id="e9dcb-244">System-Only</span><span class="sxs-lookup"><span data-stu-id="e9dcb-244">System-Only</span></span>            | <span data-ttu-id="e9dcb-245">Faux</span><span class="sxs-lookup"><span data-stu-id="e9dcb-245">False</span></span>                           |
| <span data-ttu-id="e9dcb-246">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e9dcb-246">Is-Single-Valued</span></span>       | <span data-ttu-id="e9dcb-247">Faux</span><span class="sxs-lookup"><span data-stu-id="e9dcb-247">False</span></span>                           |
| <span data-ttu-id="e9dcb-248">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e9dcb-248">Is Indexed</span></span>             | <span data-ttu-id="e9dcb-249">Vrai</span><span class="sxs-lookup"><span data-stu-id="e9dcb-249">True</span></span>                            |
| <span data-ttu-id="e9dcb-250">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e9dcb-250">In Global Catalog</span></span>      | <span data-ttu-id="e9dcb-251">Faux</span><span class="sxs-lookup"><span data-stu-id="e9dcb-251">False</span></span>                           |
| <span data-ttu-id="e9dcb-252">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e9dcb-252">NT-Security-Descriptor</span></span> | <span data-ttu-id="e9dcb-253">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e9dcb-253">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e9dcb-254">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e9dcb-254">Range-Lower</span></span>            | <span data-ttu-id="e9dcb-255">1</span><span class="sxs-lookup"><span data-stu-id="e9dcb-255">1</span></span>                               |
| <span data-ttu-id="e9dcb-256">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e9dcb-256">Range-Upper</span></span>            | <span data-ttu-id="e9dcb-257">1123</span><span class="sxs-lookup"><span data-stu-id="e9dcb-257">1123</span></span>                            |
| <span data-ttu-id="e9dcb-258">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e9dcb-258">Search-Flags</span></span>           | <span data-ttu-id="e9dcb-259">0x00000005</span><span class="sxs-lookup"><span data-stu-id="e9dcb-259">0x00000005</span></span>                      |
| <span data-ttu-id="e9dcb-260">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e9dcb-260">System-Flags</span></span>           | <span data-ttu-id="e9dcb-261">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e9dcb-261">0x00000010</span></span>                      |
| <span data-ttu-id="e9dcb-262">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e9dcb-262">Classes used in</span></span>        | [<span data-ttu-id="e9dcb-263">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="e9dcb-263">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e9dcb-264">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e9dcb-264">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e9dcb-265">Entrée</span><span class="sxs-lookup"><span data-stu-id="e9dcb-265">Entry</span></span> | <span data-ttu-id="e9dcb-266">Valeur</span><span class="sxs-lookup"><span data-stu-id="e9dcb-266">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e9dcb-267">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e9dcb-267">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e9dcb-268">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e9dcb-268">MAPI-Id</span></span>                | <span data-ttu-id="e9dcb-269">0x800F</span><span class="sxs-lookup"><span data-stu-id="e9dcb-269">0x800F</span></span>                          |
| <span data-ttu-id="e9dcb-270">System-Only</span><span class="sxs-lookup"><span data-stu-id="e9dcb-270">System-Only</span></span>            | <span data-ttu-id="e9dcb-271">Faux</span><span class="sxs-lookup"><span data-stu-id="e9dcb-271">False</span></span>                           |
| <span data-ttu-id="e9dcb-272">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e9dcb-272">Is-Single-Valued</span></span>       | <span data-ttu-id="e9dcb-273">Faux</span><span class="sxs-lookup"><span data-stu-id="e9dcb-273">False</span></span>                           |
| <span data-ttu-id="e9dcb-274">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e9dcb-274">Is Indexed</span></span>             | <span data-ttu-id="e9dcb-275">Vrai</span><span class="sxs-lookup"><span data-stu-id="e9dcb-275">True</span></span>                            |
| <span data-ttu-id="e9dcb-276">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e9dcb-276">In Global Catalog</span></span>      | <span data-ttu-id="e9dcb-277">Faux</span><span class="sxs-lookup"><span data-stu-id="e9dcb-277">False</span></span>                           |
| <span data-ttu-id="e9dcb-278">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e9dcb-278">NT-Security-Descriptor</span></span> | <span data-ttu-id="e9dcb-279">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e9dcb-279">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e9dcb-280">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e9dcb-280">Range-Lower</span></span>            | <span data-ttu-id="e9dcb-281">1</span><span class="sxs-lookup"><span data-stu-id="e9dcb-281">1</span></span>                               |
| <span data-ttu-id="e9dcb-282">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e9dcb-282">Range-Upper</span></span>            | <span data-ttu-id="e9dcb-283">1123</span><span class="sxs-lookup"><span data-stu-id="e9dcb-283">1123</span></span>                            |
| <span data-ttu-id="e9dcb-284">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e9dcb-284">Search-Flags</span></span>           | <span data-ttu-id="e9dcb-285">0x00000005</span><span class="sxs-lookup"><span data-stu-id="e9dcb-285">0x00000005</span></span>                      |
| <span data-ttu-id="e9dcb-286">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e9dcb-286">System-Flags</span></span>           | <span data-ttu-id="e9dcb-287">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e9dcb-287">0x00000010</span></span>                      |
| <span data-ttu-id="e9dcb-288">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e9dcb-288">Classes used in</span></span>        | [<span data-ttu-id="e9dcb-289">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="e9dcb-289">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e9dcb-290">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e9dcb-290">Windows Server 2012</span></span>



| <span data-ttu-id="e9dcb-291">Entrée</span><span class="sxs-lookup"><span data-stu-id="e9dcb-291">Entry</span></span> | <span data-ttu-id="e9dcb-292">Valeur</span><span class="sxs-lookup"><span data-stu-id="e9dcb-292">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e9dcb-293">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e9dcb-293">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e9dcb-294">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e9dcb-294">MAPI-Id</span></span>                | <span data-ttu-id="e9dcb-295">0x800F</span><span class="sxs-lookup"><span data-stu-id="e9dcb-295">0x800F</span></span>                          |
| <span data-ttu-id="e9dcb-296">System-Only</span><span class="sxs-lookup"><span data-stu-id="e9dcb-296">System-Only</span></span>            | <span data-ttu-id="e9dcb-297">Faux</span><span class="sxs-lookup"><span data-stu-id="e9dcb-297">False</span></span>                           |
| <span data-ttu-id="e9dcb-298">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e9dcb-298">Is-Single-Valued</span></span>       | <span data-ttu-id="e9dcb-299">Faux</span><span class="sxs-lookup"><span data-stu-id="e9dcb-299">False</span></span>                           |
| <span data-ttu-id="e9dcb-300">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e9dcb-300">Is Indexed</span></span>             | <span data-ttu-id="e9dcb-301">Vrai</span><span class="sxs-lookup"><span data-stu-id="e9dcb-301">True</span></span>                            |
| <span data-ttu-id="e9dcb-302">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e9dcb-302">In Global Catalog</span></span>      | <span data-ttu-id="e9dcb-303">Faux</span><span class="sxs-lookup"><span data-stu-id="e9dcb-303">False</span></span>                           |
| <span data-ttu-id="e9dcb-304">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e9dcb-304">NT-Security-Descriptor</span></span> | <span data-ttu-id="e9dcb-305">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e9dcb-305">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e9dcb-306">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e9dcb-306">Range-Lower</span></span>            | <span data-ttu-id="e9dcb-307">1</span><span class="sxs-lookup"><span data-stu-id="e9dcb-307">1</span></span>                               |
| <span data-ttu-id="e9dcb-308">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e9dcb-308">Range-Upper</span></span>            | <span data-ttu-id="e9dcb-309">1123</span><span class="sxs-lookup"><span data-stu-id="e9dcb-309">1123</span></span>                            |
| <span data-ttu-id="e9dcb-310">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e9dcb-310">Search-Flags</span></span>           | <span data-ttu-id="e9dcb-311">0x00000005</span><span class="sxs-lookup"><span data-stu-id="e9dcb-311">0x00000005</span></span>                      |
| <span data-ttu-id="e9dcb-312">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e9dcb-312">System-Flags</span></span>           | <span data-ttu-id="e9dcb-313">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e9dcb-313">0x00000010</span></span>                      |
| <span data-ttu-id="e9dcb-314">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e9dcb-314">Classes used in</span></span>        | [<span data-ttu-id="e9dcb-315">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="e9dcb-315">**Top**</span></span>](c-top.md)<br/> |



 

 





