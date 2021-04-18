---
title: Show-in-Address-attribute Book
description: Cet attribut est utilisé pour indiquer dans quels carnets d’adresses MAPI un objet s’affiche.
ms.assetid: de00da4d-7c04-4d1d-b375-ce3b5eb2f50f
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut afficher dans l’adresse du livre
- Schéma Active Directory d’attribut showInAddressBook
topic_type:
- apiref
api_name:
- Show-In-Address-Book
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f44632604c539278c67e9dd46537d8e797e2d70d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104479925"
---
# <a name="show-in-address-book-attribute"></a><span data-ttu-id="221a6-105">Show-in-Address-attribute Book</span><span class="sxs-lookup"><span data-stu-id="221a6-105">Show-In-Address-Book attribute</span></span>

<span data-ttu-id="221a6-106">Cet attribut est utilisé pour indiquer dans quels carnets d’adresses MAPI un objet s’affiche.</span><span class="sxs-lookup"><span data-stu-id="221a6-106">This attribute is used to indicate in which MAPI address books an object will appear.</span></span> <span data-ttu-id="221a6-107">Il est généralement géré par le service de mise à jour de destinataire Exchange.</span><span class="sxs-lookup"><span data-stu-id="221a6-107">It is usually maintained by the Exchange Recipient Update Service.</span></span>



| <span data-ttu-id="221a6-108">Entrée</span><span class="sxs-lookup"><span data-stu-id="221a6-108">Entry</span></span> | <span data-ttu-id="221a6-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="221a6-109">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="221a6-110">CN</span><span class="sxs-lookup"><span data-stu-id="221a6-110">CN</span></span>                | <span data-ttu-id="221a6-111">Afficher dans l’adresse-livre</span><span class="sxs-lookup"><span data-stu-id="221a6-111">Show-In-Address-Book</span></span>                    |
| <span data-ttu-id="221a6-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="221a6-112">Ldap-Display-Name</span></span> | <span data-ttu-id="221a6-113">showInAddressBook</span><span class="sxs-lookup"><span data-stu-id="221a6-113">showInAddressBook</span></span>                       |
| <span data-ttu-id="221a6-114">Taille</span><span class="sxs-lookup"><span data-stu-id="221a6-114">Size</span></span>              | \-                                      |
| <span data-ttu-id="221a6-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="221a6-115">Update Privilege</span></span>  | <span data-ttu-id="221a6-116">Utilisé par le système.</span><span class="sxs-lookup"><span data-stu-id="221a6-116">This is used by the system.</span></span>             |
| <span data-ttu-id="221a6-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="221a6-117">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="221a6-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="221a6-118">Attribute-Id</span></span>      | <span data-ttu-id="221a6-119">1.2.840.113556.1.4.644</span><span class="sxs-lookup"><span data-stu-id="221a6-119">1.2.840.113556.1.4.644</span></span>                  |
| <span data-ttu-id="221a6-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="221a6-120">System-Id-Guid</span></span>    | <span data-ttu-id="221a6-121">3e74f60e-3e73-11d1-a9c0-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="221a6-121">3e74f60e-3e73-11d1-a9c0-0000f80367c1</span></span>    |
| <span data-ttu-id="221a6-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="221a6-122">Syntax</span></span>            | [<span data-ttu-id="221a6-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="221a6-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="221a6-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="221a6-124">Implementations</span></span>

-   [<span data-ttu-id="221a6-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="221a6-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="221a6-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="221a6-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="221a6-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="221a6-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="221a6-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="221a6-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="221a6-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="221a6-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="221a6-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="221a6-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="221a6-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="221a6-131">Windows 2000 Server</span></span>



| <span data-ttu-id="221a6-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="221a6-132">Entry</span></span> | <span data-ttu-id="221a6-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="221a6-133">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="221a6-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="221a6-134">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="221a6-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="221a6-135">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="221a6-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="221a6-136">System-Only</span></span>            | <span data-ttu-id="221a6-137">Faux</span><span class="sxs-lookup"><span data-stu-id="221a6-137">False</span></span>                                                |
| <span data-ttu-id="221a6-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="221a6-138">Is-Single-Valued</span></span>       | <span data-ttu-id="221a6-139">Faux</span><span class="sxs-lookup"><span data-stu-id="221a6-139">False</span></span>                                                |
| <span data-ttu-id="221a6-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="221a6-140">Is Indexed</span></span>             | <span data-ttu-id="221a6-141">Faux</span><span class="sxs-lookup"><span data-stu-id="221a6-141">False</span></span>                                                |
| <span data-ttu-id="221a6-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="221a6-142">In Global Catalog</span></span>      | <span data-ttu-id="221a6-143">Faux</span><span class="sxs-lookup"><span data-stu-id="221a6-143">False</span></span>                                                |
| <span data-ttu-id="221a6-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="221a6-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="221a6-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="221a6-145">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="221a6-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="221a6-146">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="221a6-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="221a6-147">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="221a6-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="221a6-148">Search-Flags</span></span>           | <span data-ttu-id="221a6-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="221a6-149">0x00000010</span></span>                                           |
| <span data-ttu-id="221a6-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="221a6-150">System-Flags</span></span>           | <span data-ttu-id="221a6-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="221a6-151">0x00000010</span></span>                                           |
| <span data-ttu-id="221a6-152">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="221a6-152">Classes used in</span></span>        | [<span data-ttu-id="221a6-153">**E-mail-destinataire**</span><span class="sxs-lookup"><span data-stu-id="221a6-153">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="221a6-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="221a6-154">Windows Server 2003</span></span>



| <span data-ttu-id="221a6-155">Entrée</span><span class="sxs-lookup"><span data-stu-id="221a6-155">Entry</span></span> | <span data-ttu-id="221a6-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="221a6-156">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="221a6-157">ID de lien</span><span class="sxs-lookup"><span data-stu-id="221a6-157">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="221a6-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="221a6-158">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="221a6-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="221a6-159">System-Only</span></span>            | <span data-ttu-id="221a6-160">Faux</span><span class="sxs-lookup"><span data-stu-id="221a6-160">False</span></span>                                                |
| <span data-ttu-id="221a6-161">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="221a6-161">Is-Single-Valued</span></span>       | <span data-ttu-id="221a6-162">Faux</span><span class="sxs-lookup"><span data-stu-id="221a6-162">False</span></span>                                                |
| <span data-ttu-id="221a6-163">Est indexé</span><span class="sxs-lookup"><span data-stu-id="221a6-163">Is Indexed</span></span>             | <span data-ttu-id="221a6-164">Faux</span><span class="sxs-lookup"><span data-stu-id="221a6-164">False</span></span>                                                |
| <span data-ttu-id="221a6-165">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="221a6-165">In Global Catalog</span></span>      | <span data-ttu-id="221a6-166">Faux</span><span class="sxs-lookup"><span data-stu-id="221a6-166">False</span></span>                                                |
| <span data-ttu-id="221a6-167">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="221a6-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="221a6-168">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="221a6-168">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="221a6-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="221a6-169">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="221a6-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="221a6-170">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="221a6-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="221a6-171">Search-Flags</span></span>           | <span data-ttu-id="221a6-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="221a6-172">0x00000010</span></span>                                           |
| <span data-ttu-id="221a6-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="221a6-173">System-Flags</span></span>           | <span data-ttu-id="221a6-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="221a6-174">0x00000010</span></span>                                           |
| <span data-ttu-id="221a6-175">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="221a6-175">Classes used in</span></span>        | [<span data-ttu-id="221a6-176">**E-mail-destinataire**</span><span class="sxs-lookup"><span data-stu-id="221a6-176">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="221a6-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="221a6-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="221a6-178">Entrée</span><span class="sxs-lookup"><span data-stu-id="221a6-178">Entry</span></span> | <span data-ttu-id="221a6-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="221a6-179">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="221a6-180">ID de lien</span><span class="sxs-lookup"><span data-stu-id="221a6-180">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="221a6-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="221a6-181">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="221a6-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="221a6-182">System-Only</span></span>            | <span data-ttu-id="221a6-183">Faux</span><span class="sxs-lookup"><span data-stu-id="221a6-183">False</span></span>                                                |
| <span data-ttu-id="221a6-184">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="221a6-184">Is-Single-Valued</span></span>       | <span data-ttu-id="221a6-185">Faux</span><span class="sxs-lookup"><span data-stu-id="221a6-185">False</span></span>                                                |
| <span data-ttu-id="221a6-186">Est indexé</span><span class="sxs-lookup"><span data-stu-id="221a6-186">Is Indexed</span></span>             | <span data-ttu-id="221a6-187">Faux</span><span class="sxs-lookup"><span data-stu-id="221a6-187">False</span></span>                                                |
| <span data-ttu-id="221a6-188">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="221a6-188">In Global Catalog</span></span>      | <span data-ttu-id="221a6-189">Faux</span><span class="sxs-lookup"><span data-stu-id="221a6-189">False</span></span>                                                |
| <span data-ttu-id="221a6-190">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="221a6-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="221a6-191">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="221a6-191">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="221a6-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="221a6-192">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="221a6-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="221a6-193">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="221a6-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="221a6-194">Search-Flags</span></span>           | <span data-ttu-id="221a6-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="221a6-195">0x00000010</span></span>                                           |
| <span data-ttu-id="221a6-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="221a6-196">System-Flags</span></span>           | <span data-ttu-id="221a6-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="221a6-197">0x00000010</span></span>                                           |
| <span data-ttu-id="221a6-198">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="221a6-198">Classes used in</span></span>        | [<span data-ttu-id="221a6-199">**E-mail-destinataire**</span><span class="sxs-lookup"><span data-stu-id="221a6-199">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="221a6-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="221a6-200">Windows Server 2008</span></span>



| <span data-ttu-id="221a6-201">Entrée</span><span class="sxs-lookup"><span data-stu-id="221a6-201">Entry</span></span> | <span data-ttu-id="221a6-202">Valeur</span><span class="sxs-lookup"><span data-stu-id="221a6-202">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="221a6-203">ID de lien</span><span class="sxs-lookup"><span data-stu-id="221a6-203">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="221a6-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="221a6-204">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="221a6-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="221a6-205">System-Only</span></span>            | <span data-ttu-id="221a6-206">Faux</span><span class="sxs-lookup"><span data-stu-id="221a6-206">False</span></span>                                                |
| <span data-ttu-id="221a6-207">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="221a6-207">Is-Single-Valued</span></span>       | <span data-ttu-id="221a6-208">Faux</span><span class="sxs-lookup"><span data-stu-id="221a6-208">False</span></span>                                                |
| <span data-ttu-id="221a6-209">Est indexé</span><span class="sxs-lookup"><span data-stu-id="221a6-209">Is Indexed</span></span>             | <span data-ttu-id="221a6-210">Faux</span><span class="sxs-lookup"><span data-stu-id="221a6-210">False</span></span>                                                |
| <span data-ttu-id="221a6-211">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="221a6-211">In Global Catalog</span></span>      | <span data-ttu-id="221a6-212">Faux</span><span class="sxs-lookup"><span data-stu-id="221a6-212">False</span></span>                                                |
| <span data-ttu-id="221a6-213">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="221a6-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="221a6-214">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="221a6-214">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="221a6-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="221a6-215">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="221a6-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="221a6-216">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="221a6-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="221a6-217">Search-Flags</span></span>           | <span data-ttu-id="221a6-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="221a6-218">0x00000010</span></span>                                           |
| <span data-ttu-id="221a6-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="221a6-219">System-Flags</span></span>           | <span data-ttu-id="221a6-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="221a6-220">0x00000010</span></span>                                           |
| <span data-ttu-id="221a6-221">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="221a6-221">Classes used in</span></span>        | [<span data-ttu-id="221a6-222">**E-mail-destinataire**</span><span class="sxs-lookup"><span data-stu-id="221a6-222">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="221a6-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="221a6-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="221a6-224">Entrée</span><span class="sxs-lookup"><span data-stu-id="221a6-224">Entry</span></span> | <span data-ttu-id="221a6-225">Valeur</span><span class="sxs-lookup"><span data-stu-id="221a6-225">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="221a6-226">ID de lien</span><span class="sxs-lookup"><span data-stu-id="221a6-226">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="221a6-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="221a6-227">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="221a6-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="221a6-228">System-Only</span></span>            | <span data-ttu-id="221a6-229">Faux</span><span class="sxs-lookup"><span data-stu-id="221a6-229">False</span></span>                                                |
| <span data-ttu-id="221a6-230">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="221a6-230">Is-Single-Valued</span></span>       | <span data-ttu-id="221a6-231">Faux</span><span class="sxs-lookup"><span data-stu-id="221a6-231">False</span></span>                                                |
| <span data-ttu-id="221a6-232">Est indexé</span><span class="sxs-lookup"><span data-stu-id="221a6-232">Is Indexed</span></span>             | <span data-ttu-id="221a6-233">Faux</span><span class="sxs-lookup"><span data-stu-id="221a6-233">False</span></span>                                                |
| <span data-ttu-id="221a6-234">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="221a6-234">In Global Catalog</span></span>      | <span data-ttu-id="221a6-235">Faux</span><span class="sxs-lookup"><span data-stu-id="221a6-235">False</span></span>                                                |
| <span data-ttu-id="221a6-236">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="221a6-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="221a6-237">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="221a6-237">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="221a6-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="221a6-238">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="221a6-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="221a6-239">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="221a6-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="221a6-240">Search-Flags</span></span>           | <span data-ttu-id="221a6-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="221a6-241">0x00000010</span></span>                                           |
| <span data-ttu-id="221a6-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="221a6-242">System-Flags</span></span>           | <span data-ttu-id="221a6-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="221a6-243">0x00000010</span></span>                                           |
| <span data-ttu-id="221a6-244">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="221a6-244">Classes used in</span></span>        | [<span data-ttu-id="221a6-245">**E-mail-destinataire**</span><span class="sxs-lookup"><span data-stu-id="221a6-245">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="221a6-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="221a6-246">Windows Server 2012</span></span>



| <span data-ttu-id="221a6-247">Entrée</span><span class="sxs-lookup"><span data-stu-id="221a6-247">Entry</span></span> | <span data-ttu-id="221a6-248">Valeur</span><span class="sxs-lookup"><span data-stu-id="221a6-248">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="221a6-249">ID de lien</span><span class="sxs-lookup"><span data-stu-id="221a6-249">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="221a6-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="221a6-250">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="221a6-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="221a6-251">System-Only</span></span>            | <span data-ttu-id="221a6-252">Faux</span><span class="sxs-lookup"><span data-stu-id="221a6-252">False</span></span>                                                |
| <span data-ttu-id="221a6-253">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="221a6-253">Is-Single-Valued</span></span>       | <span data-ttu-id="221a6-254">Faux</span><span class="sxs-lookup"><span data-stu-id="221a6-254">False</span></span>                                                |
| <span data-ttu-id="221a6-255">Est indexé</span><span class="sxs-lookup"><span data-stu-id="221a6-255">Is Indexed</span></span>             | <span data-ttu-id="221a6-256">Faux</span><span class="sxs-lookup"><span data-stu-id="221a6-256">False</span></span>                                                |
| <span data-ttu-id="221a6-257">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="221a6-257">In Global Catalog</span></span>      | <span data-ttu-id="221a6-258">Faux</span><span class="sxs-lookup"><span data-stu-id="221a6-258">False</span></span>                                                |
| <span data-ttu-id="221a6-259">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="221a6-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="221a6-260">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="221a6-260">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="221a6-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="221a6-261">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="221a6-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="221a6-262">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="221a6-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="221a6-263">Search-Flags</span></span>           | <span data-ttu-id="221a6-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="221a6-264">0x00000010</span></span>                                           |
| <span data-ttu-id="221a6-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="221a6-265">System-Flags</span></span>           | <span data-ttu-id="221a6-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="221a6-266">0x00000010</span></span>                                           |
| <span data-ttu-id="221a6-267">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="221a6-267">Classes used in</span></span>        | [<span data-ttu-id="221a6-268">**E-mail-destinataire**</span><span class="sxs-lookup"><span data-stu-id="221a6-268">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



 

 





