---
title: Attribut SID-History
description: Contient les SID précédents utilisés pour l’objet si l’objet a été déplacé à partir d’un autre domaine.
ms.assetid: d738002b-fc05-4c60-aaf9-b83be61ed5a9
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut SID-History
- Schéma Active Directory de l’attribut sIDHistory
topic_type:
- apiref
api_name:
- SID-History
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16474a6463fc99e7ed2c1d2b1a2cdbf6ea9b6614
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104479924"
---
# <a name="sid-history-attribute"></a><span data-ttu-id="2d288-105">Attribut SID-History</span><span class="sxs-lookup"><span data-stu-id="2d288-105">SID-History attribute</span></span>

<span data-ttu-id="2d288-106">Contient les SID précédents utilisés pour l’objet si l’objet a été déplacé à partir d’un autre domaine.</span><span class="sxs-lookup"><span data-stu-id="2d288-106">Contains previous SIDs used for the object if the object was moved from another domain.</span></span> <span data-ttu-id="2d288-107">Chaque fois qu’un objet est déplacé d’un domaine à un autre, un nouveau SID est créé et le nouveau SID devient l’objectSID.</span><span class="sxs-lookup"><span data-stu-id="2d288-107">Whenever an object is moved from one domain to another, a new SID is created and that new SID becomes the objectSID.</span></span> <span data-ttu-id="2d288-108">Le SID précédent est ajouté à la propriété sIDHistory.</span><span class="sxs-lookup"><span data-stu-id="2d288-108">The previous SID is added to the sIDHistory property.</span></span>



| <span data-ttu-id="2d288-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="2d288-109">Entry</span></span> | <span data-ttu-id="2d288-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="2d288-110">Value</span></span> |
|-------------------|------------------------------------------------|
| <span data-ttu-id="2d288-111">CN</span><span class="sxs-lookup"><span data-stu-id="2d288-111">CN</span></span>                | <span data-ttu-id="2d288-112">SID-History</span><span class="sxs-lookup"><span data-stu-id="2d288-112">SID-History</span></span>                                    |
| <span data-ttu-id="2d288-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="2d288-113">Ldap-Display-Name</span></span> | <span data-ttu-id="2d288-114">sIDHistory</span><span class="sxs-lookup"><span data-stu-id="2d288-114">sIDHistory</span></span>                                     |
| <span data-ttu-id="2d288-115">Taille</span><span class="sxs-lookup"><span data-stu-id="2d288-115">Size</span></span>              | \-                                             |
| <span data-ttu-id="2d288-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="2d288-116">Update Privilege</span></span>  | <span data-ttu-id="2d288-117">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="2d288-117">This value is set by the system.</span></span>               |
| <span data-ttu-id="2d288-118">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="2d288-118">Update Frequency</span></span>  | <span data-ttu-id="2d288-119">Chaque fois que l’objet est déplacé vers un nouveau domaine.</span><span class="sxs-lookup"><span data-stu-id="2d288-119">Each time the object is moved to a new domain.</span></span> |
| <span data-ttu-id="2d288-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2d288-120">Attribute-Id</span></span>      | <span data-ttu-id="2d288-121">1.2.840.113556.1.4.609</span><span class="sxs-lookup"><span data-stu-id="2d288-121">1.2.840.113556.1.4.609</span></span>                         |
| <span data-ttu-id="2d288-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="2d288-122">System-Id-Guid</span></span>    | <span data-ttu-id="2d288-123">17eb4278-d167-11d0-b002-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="2d288-123">17eb4278-d167-11d0-b002-0000f80367c1</span></span>           |
| <span data-ttu-id="2d288-124">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2d288-124">Syntax</span></span>            | [<span data-ttu-id="2d288-125">**Chaîne (SID)**</span><span class="sxs-lookup"><span data-stu-id="2d288-125">**String(Sid)**</span></span>](s-string-sid.md)            |



## <a name="implementations"></a><span data-ttu-id="2d288-126">Implémentations</span><span class="sxs-lookup"><span data-stu-id="2d288-126">Implementations</span></span>

-   [<span data-ttu-id="2d288-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2d288-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2d288-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2d288-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2d288-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2d288-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2d288-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2d288-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2d288-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2d288-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2d288-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2d288-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2d288-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2d288-133">Windows 2000 Server</span></span>



| <span data-ttu-id="2d288-134">Entrée</span><span class="sxs-lookup"><span data-stu-id="2d288-134">Entry</span></span> | <span data-ttu-id="2d288-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="2d288-135">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="2d288-136">ID de lien</span><span class="sxs-lookup"><span data-stu-id="2d288-136">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="2d288-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2d288-137">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="2d288-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="2d288-138">System-Only</span></span>            | <span data-ttu-id="2d288-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="2d288-139">True</span></span>                                                         |
| <span data-ttu-id="2d288-140">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="2d288-140">Is-Single-Valued</span></span>       | <span data-ttu-id="2d288-141">Faux</span><span class="sxs-lookup"><span data-stu-id="2d288-141">False</span></span>                                                        |
| <span data-ttu-id="2d288-142">Est indexé</span><span class="sxs-lookup"><span data-stu-id="2d288-142">Is Indexed</span></span>             | <span data-ttu-id="2d288-143">Vrai</span><span class="sxs-lookup"><span data-stu-id="2d288-143">True</span></span>                                                         |
| <span data-ttu-id="2d288-144">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="2d288-144">In Global Catalog</span></span>      | <span data-ttu-id="2d288-145">Vrai</span><span class="sxs-lookup"><span data-stu-id="2d288-145">True</span></span>                                                         |
| <span data-ttu-id="2d288-146">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="2d288-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="2d288-147">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="2d288-147">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="2d288-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2d288-148">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="2d288-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2d288-149">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="2d288-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2d288-150">Search-Flags</span></span>           | <span data-ttu-id="2d288-151">0x00000001</span><span class="sxs-lookup"><span data-stu-id="2d288-151">0x00000001</span></span>                                                   |
| <span data-ttu-id="2d288-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2d288-152">System-Flags</span></span>           | <span data-ttu-id="2d288-153">0x00000012</span><span class="sxs-lookup"><span data-stu-id="2d288-153">0x00000012</span></span>                                                   |
| <span data-ttu-id="2d288-154">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="2d288-154">Classes used in</span></span>        | [<span data-ttu-id="2d288-155">**Sécurité-principal**</span><span class="sxs-lookup"><span data-stu-id="2d288-155">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2d288-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2d288-156">Windows Server 2003</span></span>



| <span data-ttu-id="2d288-157">Entrée</span><span class="sxs-lookup"><span data-stu-id="2d288-157">Entry</span></span> | <span data-ttu-id="2d288-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="2d288-158">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="2d288-159">ID de lien</span><span class="sxs-lookup"><span data-stu-id="2d288-159">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="2d288-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2d288-160">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="2d288-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="2d288-161">System-Only</span></span>            | <span data-ttu-id="2d288-162">Faux</span><span class="sxs-lookup"><span data-stu-id="2d288-162">False</span></span>                                                        |
| <span data-ttu-id="2d288-163">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="2d288-163">Is-Single-Valued</span></span>       | <span data-ttu-id="2d288-164">Faux</span><span class="sxs-lookup"><span data-stu-id="2d288-164">False</span></span>                                                        |
| <span data-ttu-id="2d288-165">Est indexé</span><span class="sxs-lookup"><span data-stu-id="2d288-165">Is Indexed</span></span>             | <span data-ttu-id="2d288-166">Vrai</span><span class="sxs-lookup"><span data-stu-id="2d288-166">True</span></span>                                                         |
| <span data-ttu-id="2d288-167">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="2d288-167">In Global Catalog</span></span>      | <span data-ttu-id="2d288-168">Vrai</span><span class="sxs-lookup"><span data-stu-id="2d288-168">True</span></span>                                                         |
| <span data-ttu-id="2d288-169">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="2d288-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="2d288-170">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="2d288-170">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="2d288-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2d288-171">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="2d288-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2d288-172">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="2d288-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2d288-173">Search-Flags</span></span>           | <span data-ttu-id="2d288-174">0x00000001</span><span class="sxs-lookup"><span data-stu-id="2d288-174">0x00000001</span></span>                                                   |
| <span data-ttu-id="2d288-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2d288-175">System-Flags</span></span>           | <span data-ttu-id="2d288-176">0x00000012</span><span class="sxs-lookup"><span data-stu-id="2d288-176">0x00000012</span></span>                                                   |
| <span data-ttu-id="2d288-177">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="2d288-177">Classes used in</span></span>        | [<span data-ttu-id="2d288-178">**Sécurité-principal**</span><span class="sxs-lookup"><span data-stu-id="2d288-178">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2d288-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2d288-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2d288-180">Entrée</span><span class="sxs-lookup"><span data-stu-id="2d288-180">Entry</span></span> | <span data-ttu-id="2d288-181">Valeur</span><span class="sxs-lookup"><span data-stu-id="2d288-181">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="2d288-182">ID de lien</span><span class="sxs-lookup"><span data-stu-id="2d288-182">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="2d288-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2d288-183">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="2d288-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="2d288-184">System-Only</span></span>            | <span data-ttu-id="2d288-185">Faux</span><span class="sxs-lookup"><span data-stu-id="2d288-185">False</span></span>                                                        |
| <span data-ttu-id="2d288-186">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="2d288-186">Is-Single-Valued</span></span>       | <span data-ttu-id="2d288-187">Faux</span><span class="sxs-lookup"><span data-stu-id="2d288-187">False</span></span>                                                        |
| <span data-ttu-id="2d288-188">Est indexé</span><span class="sxs-lookup"><span data-stu-id="2d288-188">Is Indexed</span></span>             | <span data-ttu-id="2d288-189">Vrai</span><span class="sxs-lookup"><span data-stu-id="2d288-189">True</span></span>                                                         |
| <span data-ttu-id="2d288-190">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="2d288-190">In Global Catalog</span></span>      | <span data-ttu-id="2d288-191">Vrai</span><span class="sxs-lookup"><span data-stu-id="2d288-191">True</span></span>                                                         |
| <span data-ttu-id="2d288-192">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="2d288-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="2d288-193">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="2d288-193">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="2d288-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2d288-194">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="2d288-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2d288-195">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="2d288-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2d288-196">Search-Flags</span></span>           | <span data-ttu-id="2d288-197">0x00000001</span><span class="sxs-lookup"><span data-stu-id="2d288-197">0x00000001</span></span>                                                   |
| <span data-ttu-id="2d288-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2d288-198">System-Flags</span></span>           | <span data-ttu-id="2d288-199">0x00000012</span><span class="sxs-lookup"><span data-stu-id="2d288-199">0x00000012</span></span>                                                   |
| <span data-ttu-id="2d288-200">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="2d288-200">Classes used in</span></span>        | [<span data-ttu-id="2d288-201">**Sécurité-principal**</span><span class="sxs-lookup"><span data-stu-id="2d288-201">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2d288-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2d288-202">Windows Server 2008</span></span>



| <span data-ttu-id="2d288-203">Entrée</span><span class="sxs-lookup"><span data-stu-id="2d288-203">Entry</span></span> | <span data-ttu-id="2d288-204">Valeur</span><span class="sxs-lookup"><span data-stu-id="2d288-204">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="2d288-205">ID de lien</span><span class="sxs-lookup"><span data-stu-id="2d288-205">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="2d288-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2d288-206">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="2d288-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="2d288-207">System-Only</span></span>            | <span data-ttu-id="2d288-208">Faux</span><span class="sxs-lookup"><span data-stu-id="2d288-208">False</span></span>                                                        |
| <span data-ttu-id="2d288-209">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="2d288-209">Is-Single-Valued</span></span>       | <span data-ttu-id="2d288-210">Faux</span><span class="sxs-lookup"><span data-stu-id="2d288-210">False</span></span>                                                        |
| <span data-ttu-id="2d288-211">Est indexé</span><span class="sxs-lookup"><span data-stu-id="2d288-211">Is Indexed</span></span>             | <span data-ttu-id="2d288-212">Vrai</span><span class="sxs-lookup"><span data-stu-id="2d288-212">True</span></span>                                                         |
| <span data-ttu-id="2d288-213">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="2d288-213">In Global Catalog</span></span>      | <span data-ttu-id="2d288-214">Vrai</span><span class="sxs-lookup"><span data-stu-id="2d288-214">True</span></span>                                                         |
| <span data-ttu-id="2d288-215">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="2d288-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="2d288-216">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="2d288-216">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="2d288-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2d288-217">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="2d288-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2d288-218">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="2d288-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2d288-219">Search-Flags</span></span>           | <span data-ttu-id="2d288-220">0x00000001</span><span class="sxs-lookup"><span data-stu-id="2d288-220">0x00000001</span></span>                                                   |
| <span data-ttu-id="2d288-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2d288-221">System-Flags</span></span>           | <span data-ttu-id="2d288-222">0x00000012</span><span class="sxs-lookup"><span data-stu-id="2d288-222">0x00000012</span></span>                                                   |
| <span data-ttu-id="2d288-223">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="2d288-223">Classes used in</span></span>        | [<span data-ttu-id="2d288-224">**Sécurité-principal**</span><span class="sxs-lookup"><span data-stu-id="2d288-224">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2d288-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2d288-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2d288-226">Entrée</span><span class="sxs-lookup"><span data-stu-id="2d288-226">Entry</span></span> | <span data-ttu-id="2d288-227">Valeur</span><span class="sxs-lookup"><span data-stu-id="2d288-227">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="2d288-228">ID de lien</span><span class="sxs-lookup"><span data-stu-id="2d288-228">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="2d288-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2d288-229">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="2d288-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="2d288-230">System-Only</span></span>            | <span data-ttu-id="2d288-231">Faux</span><span class="sxs-lookup"><span data-stu-id="2d288-231">False</span></span>                                                        |
| <span data-ttu-id="2d288-232">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="2d288-232">Is-Single-Valued</span></span>       | <span data-ttu-id="2d288-233">Faux</span><span class="sxs-lookup"><span data-stu-id="2d288-233">False</span></span>                                                        |
| <span data-ttu-id="2d288-234">Est indexé</span><span class="sxs-lookup"><span data-stu-id="2d288-234">Is Indexed</span></span>             | <span data-ttu-id="2d288-235">Vrai</span><span class="sxs-lookup"><span data-stu-id="2d288-235">True</span></span>                                                         |
| <span data-ttu-id="2d288-236">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="2d288-236">In Global Catalog</span></span>      | <span data-ttu-id="2d288-237">Vrai</span><span class="sxs-lookup"><span data-stu-id="2d288-237">True</span></span>                                                         |
| <span data-ttu-id="2d288-238">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="2d288-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="2d288-239">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="2d288-239">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="2d288-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2d288-240">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="2d288-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2d288-241">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="2d288-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2d288-242">Search-Flags</span></span>           | <span data-ttu-id="2d288-243">0x00000001</span><span class="sxs-lookup"><span data-stu-id="2d288-243">0x00000001</span></span>                                                   |
| <span data-ttu-id="2d288-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2d288-244">System-Flags</span></span>           | <span data-ttu-id="2d288-245">0x00000012</span><span class="sxs-lookup"><span data-stu-id="2d288-245">0x00000012</span></span>                                                   |
| <span data-ttu-id="2d288-246">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="2d288-246">Classes used in</span></span>        | [<span data-ttu-id="2d288-247">**Sécurité-principal**</span><span class="sxs-lookup"><span data-stu-id="2d288-247">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2d288-248">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2d288-248">Windows Server 2012</span></span>



| <span data-ttu-id="2d288-249">Entrée</span><span class="sxs-lookup"><span data-stu-id="2d288-249">Entry</span></span> | <span data-ttu-id="2d288-250">Valeur</span><span class="sxs-lookup"><span data-stu-id="2d288-250">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="2d288-251">ID de lien</span><span class="sxs-lookup"><span data-stu-id="2d288-251">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="2d288-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2d288-252">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="2d288-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="2d288-253">System-Only</span></span>            | <span data-ttu-id="2d288-254">Faux</span><span class="sxs-lookup"><span data-stu-id="2d288-254">False</span></span>                                                        |
| <span data-ttu-id="2d288-255">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="2d288-255">Is-Single-Valued</span></span>       | <span data-ttu-id="2d288-256">Faux</span><span class="sxs-lookup"><span data-stu-id="2d288-256">False</span></span>                                                        |
| <span data-ttu-id="2d288-257">Est indexé</span><span class="sxs-lookup"><span data-stu-id="2d288-257">Is Indexed</span></span>             | <span data-ttu-id="2d288-258">Vrai</span><span class="sxs-lookup"><span data-stu-id="2d288-258">True</span></span>                                                         |
| <span data-ttu-id="2d288-259">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="2d288-259">In Global Catalog</span></span>      | <span data-ttu-id="2d288-260">Vrai</span><span class="sxs-lookup"><span data-stu-id="2d288-260">True</span></span>                                                         |
| <span data-ttu-id="2d288-261">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="2d288-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="2d288-262">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="2d288-262">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="2d288-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2d288-263">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="2d288-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2d288-264">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="2d288-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2d288-265">Search-Flags</span></span>           | <span data-ttu-id="2d288-266">0x00000001</span><span class="sxs-lookup"><span data-stu-id="2d288-266">0x00000001</span></span>                                                   |
| <span data-ttu-id="2d288-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2d288-267">System-Flags</span></span>           | <span data-ttu-id="2d288-268">0x00000012</span><span class="sxs-lookup"><span data-stu-id="2d288-268">0x00000012</span></span>                                                   |
| <span data-ttu-id="2d288-269">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="2d288-269">Classes used in</span></span>        | [<span data-ttu-id="2d288-270">**Sécurité-principal**</span><span class="sxs-lookup"><span data-stu-id="2d288-270">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



 

 





