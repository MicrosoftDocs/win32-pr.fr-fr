---
title: DN-Reference-attribut Update
description: Si un objet est renommé, cet attribut est utilisé pour effectuer le suivi de tous les noms précédents et actuels qui ont été assignés à un objet afin que les objets liés puissent toujours le trouver.
ms.assetid: 28e02a38-eed8-475c-a381-145857477ec6
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory-référence-mise à jour d’attribut DN
- Schéma AD de l’attribut dNReferenceUpdate
topic_type:
- apiref
api_name:
- DN-Reference-Update
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a71e8360be6e7ed6697363daa0f6ff32e2ec5fb9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106536092"
---
# <a name="dn-reference-update-attribute"></a><span data-ttu-id="4cfde-105">DN-Reference-attribut Update</span><span class="sxs-lookup"><span data-stu-id="4cfde-105">DN-Reference-Update attribute</span></span>

<span data-ttu-id="4cfde-106">Si un objet est renommé, cet attribut est utilisé pour effectuer le suivi de tous les noms précédents et actuels qui ont été assignés à un objet afin que les objets liés puissent toujours le trouver.</span><span class="sxs-lookup"><span data-stu-id="4cfde-106">If an object is renamed, this attribute is used to track all of the previous and current names that have been assigned to an object so that linked objects can still find it.</span></span>



| <span data-ttu-id="4cfde-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="4cfde-107">Entry</span></span> | <span data-ttu-id="4cfde-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="4cfde-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="4cfde-109">CN</span><span class="sxs-lookup"><span data-stu-id="4cfde-109">CN</span></span>                | <span data-ttu-id="4cfde-110">DN-Reference-Update</span><span class="sxs-lookup"><span data-stu-id="4cfde-110">DN-Reference-Update</span></span>                     |
| <span data-ttu-id="4cfde-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="4cfde-111">Ldap-Display-Name</span></span> | <span data-ttu-id="4cfde-112">dNReferenceUpdate</span><span class="sxs-lookup"><span data-stu-id="4cfde-112">dNReferenceUpdate</span></span>                       |
| <span data-ttu-id="4cfde-113">Taille</span><span class="sxs-lookup"><span data-stu-id="4cfde-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="4cfde-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="4cfde-114">Update Privilege</span></span>  | <span data-ttu-id="4cfde-115">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="4cfde-115">This is set by the system.</span></span>              |
| <span data-ttu-id="4cfde-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="4cfde-116">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="4cfde-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4cfde-117">Attribute-Id</span></span>      | <span data-ttu-id="4cfde-118">1.2.840.113556.1.4.1242</span><span class="sxs-lookup"><span data-stu-id="4cfde-118">1.2.840.113556.1.4.1242</span></span>                 |
| <span data-ttu-id="4cfde-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="4cfde-119">System-Id-Guid</span></span>    | <span data-ttu-id="4cfde-120">2df90d86-009f-11d2-aa4c-00c04fd7d83a</span><span class="sxs-lookup"><span data-stu-id="4cfde-120">2df90d86-009f-11d2-aa4c-00c04fd7d83a</span></span>    |
| <span data-ttu-id="4cfde-121">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4cfde-121">Syntax</span></span>            | [<span data-ttu-id="4cfde-122">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="4cfde-122">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="4cfde-123">Implémentations</span><span class="sxs-lookup"><span data-stu-id="4cfde-123">Implementations</span></span>

-   [<span data-ttu-id="4cfde-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="4cfde-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="4cfde-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4cfde-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4cfde-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4cfde-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4cfde-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4cfde-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4cfde-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4cfde-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4cfde-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4cfde-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="4cfde-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4cfde-130">Windows 2000 Server</span></span>



| <span data-ttu-id="4cfde-131">Entrée</span><span class="sxs-lookup"><span data-stu-id="4cfde-131">Entry</span></span> | <span data-ttu-id="4cfde-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="4cfde-132">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="4cfde-133">ID de lien</span><span class="sxs-lookup"><span data-stu-id="4cfde-133">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="4cfde-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4cfde-134">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="4cfde-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="4cfde-135">System-Only</span></span>            | <span data-ttu-id="4cfde-136">Vrai</span><span class="sxs-lookup"><span data-stu-id="4cfde-136">True</span></span>                                                               |
| <span data-ttu-id="4cfde-137">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="4cfde-137">Is-Single-Valued</span></span>       | <span data-ttu-id="4cfde-138">Faux</span><span class="sxs-lookup"><span data-stu-id="4cfde-138">False</span></span>                                                              |
| <span data-ttu-id="4cfde-139">Est indexé</span><span class="sxs-lookup"><span data-stu-id="4cfde-139">Is Indexed</span></span>             | <span data-ttu-id="4cfde-140">Faux</span><span class="sxs-lookup"><span data-stu-id="4cfde-140">False</span></span>                                                              |
| <span data-ttu-id="4cfde-141">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="4cfde-141">In Global Catalog</span></span>      | <span data-ttu-id="4cfde-142">Faux</span><span class="sxs-lookup"><span data-stu-id="4cfde-142">False</span></span>                                                              |
| <span data-ttu-id="4cfde-143">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="4cfde-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="4cfde-144">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="4cfde-144">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="4cfde-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4cfde-145">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="4cfde-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4cfde-146">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="4cfde-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4cfde-147">Search-Flags</span></span>           | <span data-ttu-id="4cfde-148">0x00000008</span><span class="sxs-lookup"><span data-stu-id="4cfde-148">0x00000008</span></span>                                                         |
| <span data-ttu-id="4cfde-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4cfde-149">System-Flags</span></span>           | <span data-ttu-id="4cfde-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4cfde-150">0x00000010</span></span>                                                         |
| <span data-ttu-id="4cfde-151">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="4cfde-151">Classes used in</span></span>        | [<span data-ttu-id="4cfde-152">**Infrastructure-mise à jour**</span><span class="sxs-lookup"><span data-stu-id="4cfde-152">**Infrastructure-Update**</span></span>](c-infrastructureupdate.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="4cfde-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4cfde-153">Windows Server 2003</span></span>



| <span data-ttu-id="4cfde-154">Entrée</span><span class="sxs-lookup"><span data-stu-id="4cfde-154">Entry</span></span> | <span data-ttu-id="4cfde-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="4cfde-155">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="4cfde-156">ID de lien</span><span class="sxs-lookup"><span data-stu-id="4cfde-156">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="4cfde-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4cfde-157">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="4cfde-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="4cfde-158">System-Only</span></span>            | <span data-ttu-id="4cfde-159">Vrai</span><span class="sxs-lookup"><span data-stu-id="4cfde-159">True</span></span>                                                               |
| <span data-ttu-id="4cfde-160">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="4cfde-160">Is-Single-Valued</span></span>       | <span data-ttu-id="4cfde-161">Faux</span><span class="sxs-lookup"><span data-stu-id="4cfde-161">False</span></span>                                                              |
| <span data-ttu-id="4cfde-162">Est indexé</span><span class="sxs-lookup"><span data-stu-id="4cfde-162">Is Indexed</span></span>             | <span data-ttu-id="4cfde-163">Faux</span><span class="sxs-lookup"><span data-stu-id="4cfde-163">False</span></span>                                                              |
| <span data-ttu-id="4cfde-164">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="4cfde-164">In Global Catalog</span></span>      | <span data-ttu-id="4cfde-165">Faux</span><span class="sxs-lookup"><span data-stu-id="4cfde-165">False</span></span>                                                              |
| <span data-ttu-id="4cfde-166">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="4cfde-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="4cfde-167">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="4cfde-167">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="4cfde-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4cfde-168">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="4cfde-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4cfde-169">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="4cfde-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4cfde-170">Search-Flags</span></span>           | <span data-ttu-id="4cfde-171">0x00000008</span><span class="sxs-lookup"><span data-stu-id="4cfde-171">0x00000008</span></span>                                                         |
| <span data-ttu-id="4cfde-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4cfde-172">System-Flags</span></span>           | <span data-ttu-id="4cfde-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4cfde-173">0x00000010</span></span>                                                         |
| <span data-ttu-id="4cfde-174">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="4cfde-174">Classes used in</span></span>        | [<span data-ttu-id="4cfde-175">**Infrastructure-mise à jour**</span><span class="sxs-lookup"><span data-stu-id="4cfde-175">**Infrastructure-Update**</span></span>](c-infrastructureupdate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4cfde-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4cfde-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4cfde-177">Entrée</span><span class="sxs-lookup"><span data-stu-id="4cfde-177">Entry</span></span> | <span data-ttu-id="4cfde-178">Valeur</span><span class="sxs-lookup"><span data-stu-id="4cfde-178">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="4cfde-179">ID de lien</span><span class="sxs-lookup"><span data-stu-id="4cfde-179">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="4cfde-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4cfde-180">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="4cfde-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="4cfde-181">System-Only</span></span>            | <span data-ttu-id="4cfde-182">Vrai</span><span class="sxs-lookup"><span data-stu-id="4cfde-182">True</span></span>                                                               |
| <span data-ttu-id="4cfde-183">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="4cfde-183">Is-Single-Valued</span></span>       | <span data-ttu-id="4cfde-184">Faux</span><span class="sxs-lookup"><span data-stu-id="4cfde-184">False</span></span>                                                              |
| <span data-ttu-id="4cfde-185">Est indexé</span><span class="sxs-lookup"><span data-stu-id="4cfde-185">Is Indexed</span></span>             | <span data-ttu-id="4cfde-186">Faux</span><span class="sxs-lookup"><span data-stu-id="4cfde-186">False</span></span>                                                              |
| <span data-ttu-id="4cfde-187">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="4cfde-187">In Global Catalog</span></span>      | <span data-ttu-id="4cfde-188">Faux</span><span class="sxs-lookup"><span data-stu-id="4cfde-188">False</span></span>                                                              |
| <span data-ttu-id="4cfde-189">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="4cfde-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="4cfde-190">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="4cfde-190">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="4cfde-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4cfde-191">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="4cfde-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4cfde-192">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="4cfde-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4cfde-193">Search-Flags</span></span>           | <span data-ttu-id="4cfde-194">0x00000008</span><span class="sxs-lookup"><span data-stu-id="4cfde-194">0x00000008</span></span>                                                         |
| <span data-ttu-id="4cfde-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4cfde-195">System-Flags</span></span>           | <span data-ttu-id="4cfde-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4cfde-196">0x00000010</span></span>                                                         |
| <span data-ttu-id="4cfde-197">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="4cfde-197">Classes used in</span></span>        | [<span data-ttu-id="4cfde-198">**Infrastructure-mise à jour**</span><span class="sxs-lookup"><span data-stu-id="4cfde-198">**Infrastructure-Update**</span></span>](c-infrastructureupdate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4cfde-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4cfde-199">Windows Server 2008</span></span>



| <span data-ttu-id="4cfde-200">Entrée</span><span class="sxs-lookup"><span data-stu-id="4cfde-200">Entry</span></span> | <span data-ttu-id="4cfde-201">Valeur</span><span class="sxs-lookup"><span data-stu-id="4cfde-201">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="4cfde-202">ID de lien</span><span class="sxs-lookup"><span data-stu-id="4cfde-202">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="4cfde-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4cfde-203">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="4cfde-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="4cfde-204">System-Only</span></span>            | <span data-ttu-id="4cfde-205">Vrai</span><span class="sxs-lookup"><span data-stu-id="4cfde-205">True</span></span>                                                               |
| <span data-ttu-id="4cfde-206">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="4cfde-206">Is-Single-Valued</span></span>       | <span data-ttu-id="4cfde-207">Faux</span><span class="sxs-lookup"><span data-stu-id="4cfde-207">False</span></span>                                                              |
| <span data-ttu-id="4cfde-208">Est indexé</span><span class="sxs-lookup"><span data-stu-id="4cfde-208">Is Indexed</span></span>             | <span data-ttu-id="4cfde-209">Faux</span><span class="sxs-lookup"><span data-stu-id="4cfde-209">False</span></span>                                                              |
| <span data-ttu-id="4cfde-210">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="4cfde-210">In Global Catalog</span></span>      | <span data-ttu-id="4cfde-211">Faux</span><span class="sxs-lookup"><span data-stu-id="4cfde-211">False</span></span>                                                              |
| <span data-ttu-id="4cfde-212">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="4cfde-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="4cfde-213">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="4cfde-213">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="4cfde-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4cfde-214">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="4cfde-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4cfde-215">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="4cfde-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4cfde-216">Search-Flags</span></span>           | <span data-ttu-id="4cfde-217">0x00000008</span><span class="sxs-lookup"><span data-stu-id="4cfde-217">0x00000008</span></span>                                                         |
| <span data-ttu-id="4cfde-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4cfde-218">System-Flags</span></span>           | <span data-ttu-id="4cfde-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4cfde-219">0x00000010</span></span>                                                         |
| <span data-ttu-id="4cfde-220">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="4cfde-220">Classes used in</span></span>        | [<span data-ttu-id="4cfde-221">**Infrastructure-mise à jour**</span><span class="sxs-lookup"><span data-stu-id="4cfde-221">**Infrastructure-Update**</span></span>](c-infrastructureupdate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4cfde-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4cfde-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4cfde-223">Entrée</span><span class="sxs-lookup"><span data-stu-id="4cfde-223">Entry</span></span> | <span data-ttu-id="4cfde-224">Valeur</span><span class="sxs-lookup"><span data-stu-id="4cfde-224">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="4cfde-225">ID de lien</span><span class="sxs-lookup"><span data-stu-id="4cfde-225">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="4cfde-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4cfde-226">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="4cfde-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="4cfde-227">System-Only</span></span>            | <span data-ttu-id="4cfde-228">Vrai</span><span class="sxs-lookup"><span data-stu-id="4cfde-228">True</span></span>                                                               |
| <span data-ttu-id="4cfde-229">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="4cfde-229">Is-Single-Valued</span></span>       | <span data-ttu-id="4cfde-230">Faux</span><span class="sxs-lookup"><span data-stu-id="4cfde-230">False</span></span>                                                              |
| <span data-ttu-id="4cfde-231">Est indexé</span><span class="sxs-lookup"><span data-stu-id="4cfde-231">Is Indexed</span></span>             | <span data-ttu-id="4cfde-232">Faux</span><span class="sxs-lookup"><span data-stu-id="4cfde-232">False</span></span>                                                              |
| <span data-ttu-id="4cfde-233">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="4cfde-233">In Global Catalog</span></span>      | <span data-ttu-id="4cfde-234">Faux</span><span class="sxs-lookup"><span data-stu-id="4cfde-234">False</span></span>                                                              |
| <span data-ttu-id="4cfde-235">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="4cfde-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="4cfde-236">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="4cfde-236">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="4cfde-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4cfde-237">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="4cfde-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4cfde-238">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="4cfde-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4cfde-239">Search-Flags</span></span>           | <span data-ttu-id="4cfde-240">0x00000008</span><span class="sxs-lookup"><span data-stu-id="4cfde-240">0x00000008</span></span>                                                         |
| <span data-ttu-id="4cfde-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4cfde-241">System-Flags</span></span>           | <span data-ttu-id="4cfde-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4cfde-242">0x00000010</span></span>                                                         |
| <span data-ttu-id="4cfde-243">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="4cfde-243">Classes used in</span></span>        | [<span data-ttu-id="4cfde-244">**Infrastructure-mise à jour**</span><span class="sxs-lookup"><span data-stu-id="4cfde-244">**Infrastructure-Update**</span></span>](c-infrastructureupdate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4cfde-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4cfde-245">Windows Server 2012</span></span>



| <span data-ttu-id="4cfde-246">Entrée</span><span class="sxs-lookup"><span data-stu-id="4cfde-246">Entry</span></span> | <span data-ttu-id="4cfde-247">Valeur</span><span class="sxs-lookup"><span data-stu-id="4cfde-247">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="4cfde-248">ID de lien</span><span class="sxs-lookup"><span data-stu-id="4cfde-248">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="4cfde-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4cfde-249">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="4cfde-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="4cfde-250">System-Only</span></span>            | <span data-ttu-id="4cfde-251">Vrai</span><span class="sxs-lookup"><span data-stu-id="4cfde-251">True</span></span>                                                               |
| <span data-ttu-id="4cfde-252">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="4cfde-252">Is-Single-Valued</span></span>       | <span data-ttu-id="4cfde-253">Faux</span><span class="sxs-lookup"><span data-stu-id="4cfde-253">False</span></span>                                                              |
| <span data-ttu-id="4cfde-254">Est indexé</span><span class="sxs-lookup"><span data-stu-id="4cfde-254">Is Indexed</span></span>             | <span data-ttu-id="4cfde-255">Faux</span><span class="sxs-lookup"><span data-stu-id="4cfde-255">False</span></span>                                                              |
| <span data-ttu-id="4cfde-256">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="4cfde-256">In Global Catalog</span></span>      | <span data-ttu-id="4cfde-257">Faux</span><span class="sxs-lookup"><span data-stu-id="4cfde-257">False</span></span>                                                              |
| <span data-ttu-id="4cfde-258">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="4cfde-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="4cfde-259">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="4cfde-259">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="4cfde-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4cfde-260">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="4cfde-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4cfde-261">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="4cfde-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4cfde-262">Search-Flags</span></span>           | <span data-ttu-id="4cfde-263">0x00000008</span><span class="sxs-lookup"><span data-stu-id="4cfde-263">0x00000008</span></span>                                                         |
| <span data-ttu-id="4cfde-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4cfde-264">System-Flags</span></span>           | <span data-ttu-id="4cfde-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4cfde-265">0x00000010</span></span>                                                         |
| <span data-ttu-id="4cfde-266">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="4cfde-266">Classes used in</span></span>        | [<span data-ttu-id="4cfde-267">**Infrastructure-mise à jour**</span><span class="sxs-lookup"><span data-stu-id="4cfde-267">**Infrastructure-Update**</span></span>](c-infrastructureupdate.md)<br/> |



 

 





