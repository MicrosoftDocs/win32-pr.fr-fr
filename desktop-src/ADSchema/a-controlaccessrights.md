---
title: Attribut Control-Access-Rights
description: Utilisé par la sécurité DS pour déterminer quels utilisateurs peuvent effectuer des opérations spécifiques sur l’objet hôte.
ms.assetid: 5e717160-519c-4e5a-b18f-05ee767a66a3
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory de l’attribut Control-Access-Rights
- Schéma AD de l’attribut controlAccessRights
topic_type:
- apiref
api_name:
- Control-Access-Rights
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e3ee9075cfaf4c5bbfbf17e8e2cfef6166be032
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104480461"
---
# <a name="control-access-rights-attribute"></a><span data-ttu-id="f3d8c-105">Attribut Control-Access-Rights</span><span class="sxs-lookup"><span data-stu-id="f3d8c-105">Control-Access-Rights attribute</span></span>

<span data-ttu-id="f3d8c-106">Utilisé par la sécurité DS pour déterminer quels utilisateurs peuvent effectuer des opérations spécifiques sur l’objet hôte.</span><span class="sxs-lookup"><span data-stu-id="f3d8c-106">Used by DS Security to determine which users can perform specific operations on the host object.</span></span>



| <span data-ttu-id="f3d8c-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="f3d8c-107">Entry</span></span> | <span data-ttu-id="f3d8c-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3d8c-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="f3d8c-109">CN</span><span class="sxs-lookup"><span data-stu-id="f3d8c-109">CN</span></span>                | <span data-ttu-id="f3d8c-110">Droits de contrôle-accès</span><span class="sxs-lookup"><span data-stu-id="f3d8c-110">Control-Access-Rights</span></span>                                 |
| <span data-ttu-id="f3d8c-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f3d8c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="f3d8c-112">controlAccessRights</span><span class="sxs-lookup"><span data-stu-id="f3d8c-112">controlAccessRights</span></span>                                   |
| <span data-ttu-id="f3d8c-113">Taille</span><span class="sxs-lookup"><span data-stu-id="f3d8c-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="f3d8c-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="f3d8c-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="f3d8c-115">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="f3d8c-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="f3d8c-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f3d8c-116">Attribute-Id</span></span>      | <span data-ttu-id="f3d8c-117">1.2.840.113556.1.4.200</span><span class="sxs-lookup"><span data-stu-id="f3d8c-117">1.2.840.113556.1.4.200</span></span>                                |
| <span data-ttu-id="f3d8c-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f3d8c-118">System-Id-Guid</span></span>    | <span data-ttu-id="f3d8c-119">6da8a4fc-0e52-11d0-a286-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="f3d8c-119">6da8a4fc-0e52-11d0-a286-00aa003049e2</span></span>                  |
| <span data-ttu-id="f3d8c-120">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f3d8c-120">Syntax</span></span>            | [<span data-ttu-id="f3d8c-121">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="f3d8c-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="f3d8c-122">Implémentations</span><span class="sxs-lookup"><span data-stu-id="f3d8c-122">Implementations</span></span>

-   [<span data-ttu-id="f3d8c-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f3d8c-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f3d8c-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f3d8c-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f3d8c-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f3d8c-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f3d8c-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f3d8c-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f3d8c-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f3d8c-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f3d8c-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f3d8c-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f3d8c-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f3d8c-129">Windows 2000 Server</span></span>



| <span data-ttu-id="f3d8c-130">Entrée</span><span class="sxs-lookup"><span data-stu-id="f3d8c-130">Entry</span></span> | <span data-ttu-id="f3d8c-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3d8c-131">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3d8c-132">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f3d8c-132">Link-Id</span></span>                | \-                                                                                                                 |
| <span data-ttu-id="f3d8c-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f3d8c-133">MAPI-Id</span></span>                | \-                                                                                                                 |
| <span data-ttu-id="f3d8c-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="f3d8c-134">System-Only</span></span>            | <span data-ttu-id="f3d8c-135">Faux</span><span class="sxs-lookup"><span data-stu-id="f3d8c-135">False</span></span>                                                                                                              |
| <span data-ttu-id="f3d8c-136">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f3d8c-136">Is-Single-Valued</span></span>       | <span data-ttu-id="f3d8c-137">Faux</span><span class="sxs-lookup"><span data-stu-id="f3d8c-137">False</span></span>                                                                                                              |
| <span data-ttu-id="f3d8c-138">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f3d8c-138">Is Indexed</span></span>             | <span data-ttu-id="f3d8c-139">Faux</span><span class="sxs-lookup"><span data-stu-id="f3d8c-139">False</span></span>                                                                                                              |
| <span data-ttu-id="f3d8c-140">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f3d8c-140">In Global Catalog</span></span>      | <span data-ttu-id="f3d8c-141">Faux</span><span class="sxs-lookup"><span data-stu-id="f3d8c-141">False</span></span>                                                                                                              |
| <span data-ttu-id="f3d8c-142">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f3d8c-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="f3d8c-143">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f3d8c-143">O:BAG:BAD:S:</span></span>                                                                                                       |
| <span data-ttu-id="f3d8c-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f3d8c-144">Range-Lower</span></span>            | <span data-ttu-id="f3d8c-145">16</span><span class="sxs-lookup"><span data-stu-id="f3d8c-145">16</span></span>                                                                                                                 |
| <span data-ttu-id="f3d8c-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f3d8c-146">Range-Upper</span></span>            | <span data-ttu-id="f3d8c-147">16</span><span class="sxs-lookup"><span data-stu-id="f3d8c-147">16</span></span>                                                                                                                 |
| <span data-ttu-id="f3d8c-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f3d8c-148">Search-Flags</span></span>           | <span data-ttu-id="f3d8c-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f3d8c-149">0x00000000</span></span>                                                                                                         |
| <span data-ttu-id="f3d8c-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f3d8c-150">System-Flags</span></span>           | <span data-ttu-id="f3d8c-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f3d8c-151">0x00000010</span></span>                                                                                                         |
| <span data-ttu-id="f3d8c-152">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f3d8c-152">Classes used in</span></span>        | [<span data-ttu-id="f3d8c-153">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="f3d8c-153">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="f3d8c-154">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="f3d8c-154">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="f3d8c-155">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="f3d8c-155">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f3d8c-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f3d8c-156">Windows Server 2003</span></span>



| <span data-ttu-id="f3d8c-157">Entrée</span><span class="sxs-lookup"><span data-stu-id="f3d8c-157">Entry</span></span> | <span data-ttu-id="f3d8c-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3d8c-158">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3d8c-159">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f3d8c-159">Link-Id</span></span>                | \-                                                                                                                 |
| <span data-ttu-id="f3d8c-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f3d8c-160">MAPI-Id</span></span>                | \-                                                                                                                 |
| <span data-ttu-id="f3d8c-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="f3d8c-161">System-Only</span></span>            | <span data-ttu-id="f3d8c-162">Faux</span><span class="sxs-lookup"><span data-stu-id="f3d8c-162">False</span></span>                                                                                                              |
| <span data-ttu-id="f3d8c-163">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f3d8c-163">Is-Single-Valued</span></span>       | <span data-ttu-id="f3d8c-164">Faux</span><span class="sxs-lookup"><span data-stu-id="f3d8c-164">False</span></span>                                                                                                              |
| <span data-ttu-id="f3d8c-165">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f3d8c-165">Is Indexed</span></span>             | <span data-ttu-id="f3d8c-166">Faux</span><span class="sxs-lookup"><span data-stu-id="f3d8c-166">False</span></span>                                                                                                              |
| <span data-ttu-id="f3d8c-167">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f3d8c-167">In Global Catalog</span></span>      | <span data-ttu-id="f3d8c-168">Faux</span><span class="sxs-lookup"><span data-stu-id="f3d8c-168">False</span></span>                                                                                                              |
| <span data-ttu-id="f3d8c-169">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f3d8c-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="f3d8c-170">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f3d8c-170">O:BAG:BAD:S:</span></span>                                                                                                       |
| <span data-ttu-id="f3d8c-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f3d8c-171">Range-Lower</span></span>            | <span data-ttu-id="f3d8c-172">16</span><span class="sxs-lookup"><span data-stu-id="f3d8c-172">16</span></span>                                                                                                                 |
| <span data-ttu-id="f3d8c-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f3d8c-173">Range-Upper</span></span>            | <span data-ttu-id="f3d8c-174">16</span><span class="sxs-lookup"><span data-stu-id="f3d8c-174">16</span></span>                                                                                                                 |
| <span data-ttu-id="f3d8c-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f3d8c-175">Search-Flags</span></span>           | <span data-ttu-id="f3d8c-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f3d8c-176">0x00000000</span></span>                                                                                                         |
| <span data-ttu-id="f3d8c-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f3d8c-177">System-Flags</span></span>           | <span data-ttu-id="f3d8c-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f3d8c-178">0x00000010</span></span>                                                                                                         |
| <span data-ttu-id="f3d8c-179">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f3d8c-179">Classes used in</span></span>        | [<span data-ttu-id="f3d8c-180">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="f3d8c-180">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="f3d8c-181">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="f3d8c-181">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="f3d8c-182">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="f3d8c-182">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f3d8c-183">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f3d8c-183">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f3d8c-184">Entrée</span><span class="sxs-lookup"><span data-stu-id="f3d8c-184">Entry</span></span> | <span data-ttu-id="f3d8c-185">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3d8c-185">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3d8c-186">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f3d8c-186">Link-Id</span></span>                | \-                                                                                                                 |
| <span data-ttu-id="f3d8c-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f3d8c-187">MAPI-Id</span></span>                | \-                                                                                                                 |
| <span data-ttu-id="f3d8c-188">System-Only</span><span class="sxs-lookup"><span data-stu-id="f3d8c-188">System-Only</span></span>            | <span data-ttu-id="f3d8c-189">Faux</span><span class="sxs-lookup"><span data-stu-id="f3d8c-189">False</span></span>                                                                                                              |
| <span data-ttu-id="f3d8c-190">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f3d8c-190">Is-Single-Valued</span></span>       | <span data-ttu-id="f3d8c-191">Faux</span><span class="sxs-lookup"><span data-stu-id="f3d8c-191">False</span></span>                                                                                                              |
| <span data-ttu-id="f3d8c-192">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f3d8c-192">Is Indexed</span></span>             | <span data-ttu-id="f3d8c-193">Faux</span><span class="sxs-lookup"><span data-stu-id="f3d8c-193">False</span></span>                                                                                                              |
| <span data-ttu-id="f3d8c-194">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f3d8c-194">In Global Catalog</span></span>      | <span data-ttu-id="f3d8c-195">Faux</span><span class="sxs-lookup"><span data-stu-id="f3d8c-195">False</span></span>                                                                                                              |
| <span data-ttu-id="f3d8c-196">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f3d8c-196">NT-Security-Descriptor</span></span> | <span data-ttu-id="f3d8c-197">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f3d8c-197">O:BAG:BAD:S:</span></span>                                                                                                       |
| <span data-ttu-id="f3d8c-198">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f3d8c-198">Range-Lower</span></span>            | <span data-ttu-id="f3d8c-199">16</span><span class="sxs-lookup"><span data-stu-id="f3d8c-199">16</span></span>                                                                                                                 |
| <span data-ttu-id="f3d8c-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f3d8c-200">Range-Upper</span></span>            | <span data-ttu-id="f3d8c-201">16</span><span class="sxs-lookup"><span data-stu-id="f3d8c-201">16</span></span>                                                                                                                 |
| <span data-ttu-id="f3d8c-202">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f3d8c-202">Search-Flags</span></span>           | <span data-ttu-id="f3d8c-203">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f3d8c-203">0x00000000</span></span>                                                                                                         |
| <span data-ttu-id="f3d8c-204">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f3d8c-204">System-Flags</span></span>           | <span data-ttu-id="f3d8c-205">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f3d8c-205">0x00000010</span></span>                                                                                                         |
| <span data-ttu-id="f3d8c-206">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f3d8c-206">Classes used in</span></span>        | [<span data-ttu-id="f3d8c-207">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="f3d8c-207">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="f3d8c-208">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="f3d8c-208">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="f3d8c-209">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="f3d8c-209">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f3d8c-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f3d8c-210">Windows Server 2008</span></span>



| <span data-ttu-id="f3d8c-211">Entrée</span><span class="sxs-lookup"><span data-stu-id="f3d8c-211">Entry</span></span> | <span data-ttu-id="f3d8c-212">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3d8c-212">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3d8c-213">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f3d8c-213">Link-Id</span></span>                | \-                                                                                                                 |
| <span data-ttu-id="f3d8c-214">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f3d8c-214">MAPI-Id</span></span>                | \-                                                                                                                 |
| <span data-ttu-id="f3d8c-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="f3d8c-215">System-Only</span></span>            | <span data-ttu-id="f3d8c-216">Faux</span><span class="sxs-lookup"><span data-stu-id="f3d8c-216">False</span></span>                                                                                                              |
| <span data-ttu-id="f3d8c-217">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f3d8c-217">Is-Single-Valued</span></span>       | <span data-ttu-id="f3d8c-218">Faux</span><span class="sxs-lookup"><span data-stu-id="f3d8c-218">False</span></span>                                                                                                              |
| <span data-ttu-id="f3d8c-219">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f3d8c-219">Is Indexed</span></span>             | <span data-ttu-id="f3d8c-220">Faux</span><span class="sxs-lookup"><span data-stu-id="f3d8c-220">False</span></span>                                                                                                              |
| <span data-ttu-id="f3d8c-221">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f3d8c-221">In Global Catalog</span></span>      | <span data-ttu-id="f3d8c-222">Faux</span><span class="sxs-lookup"><span data-stu-id="f3d8c-222">False</span></span>                                                                                                              |
| <span data-ttu-id="f3d8c-223">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f3d8c-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="f3d8c-224">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f3d8c-224">O:BAG:BAD:S:</span></span>                                                                                                       |
| <span data-ttu-id="f3d8c-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f3d8c-225">Range-Lower</span></span>            | <span data-ttu-id="f3d8c-226">16</span><span class="sxs-lookup"><span data-stu-id="f3d8c-226">16</span></span>                                                                                                                 |
| <span data-ttu-id="f3d8c-227">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f3d8c-227">Range-Upper</span></span>            | <span data-ttu-id="f3d8c-228">16</span><span class="sxs-lookup"><span data-stu-id="f3d8c-228">16</span></span>                                                                                                                 |
| <span data-ttu-id="f3d8c-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f3d8c-229">Search-Flags</span></span>           | <span data-ttu-id="f3d8c-230">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f3d8c-230">0x00000000</span></span>                                                                                                         |
| <span data-ttu-id="f3d8c-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f3d8c-231">System-Flags</span></span>           | <span data-ttu-id="f3d8c-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f3d8c-232">0x00000010</span></span>                                                                                                         |
| <span data-ttu-id="f3d8c-233">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f3d8c-233">Classes used in</span></span>        | [<span data-ttu-id="f3d8c-234">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="f3d8c-234">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="f3d8c-235">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="f3d8c-235">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="f3d8c-236">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="f3d8c-236">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f3d8c-237">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f3d8c-237">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f3d8c-238">Entrée</span><span class="sxs-lookup"><span data-stu-id="f3d8c-238">Entry</span></span> | <span data-ttu-id="f3d8c-239">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3d8c-239">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3d8c-240">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f3d8c-240">Link-Id</span></span>                | \-                                                                                                                 |
| <span data-ttu-id="f3d8c-241">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f3d8c-241">MAPI-Id</span></span>                | \-                                                                                                                 |
| <span data-ttu-id="f3d8c-242">System-Only</span><span class="sxs-lookup"><span data-stu-id="f3d8c-242">System-Only</span></span>            | <span data-ttu-id="f3d8c-243">Faux</span><span class="sxs-lookup"><span data-stu-id="f3d8c-243">False</span></span>                                                                                                              |
| <span data-ttu-id="f3d8c-244">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f3d8c-244">Is-Single-Valued</span></span>       | <span data-ttu-id="f3d8c-245">Faux</span><span class="sxs-lookup"><span data-stu-id="f3d8c-245">False</span></span>                                                                                                              |
| <span data-ttu-id="f3d8c-246">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f3d8c-246">Is Indexed</span></span>             | <span data-ttu-id="f3d8c-247">Faux</span><span class="sxs-lookup"><span data-stu-id="f3d8c-247">False</span></span>                                                                                                              |
| <span data-ttu-id="f3d8c-248">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f3d8c-248">In Global Catalog</span></span>      | <span data-ttu-id="f3d8c-249">Faux</span><span class="sxs-lookup"><span data-stu-id="f3d8c-249">False</span></span>                                                                                                              |
| <span data-ttu-id="f3d8c-250">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f3d8c-250">NT-Security-Descriptor</span></span> | <span data-ttu-id="f3d8c-251">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f3d8c-251">O:BAG:BAD:S:</span></span>                                                                                                       |
| <span data-ttu-id="f3d8c-252">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f3d8c-252">Range-Lower</span></span>            | <span data-ttu-id="f3d8c-253">16</span><span class="sxs-lookup"><span data-stu-id="f3d8c-253">16</span></span>                                                                                                                 |
| <span data-ttu-id="f3d8c-254">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f3d8c-254">Range-Upper</span></span>            | <span data-ttu-id="f3d8c-255">16</span><span class="sxs-lookup"><span data-stu-id="f3d8c-255">16</span></span>                                                                                                                 |
| <span data-ttu-id="f3d8c-256">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f3d8c-256">Search-Flags</span></span>           | <span data-ttu-id="f3d8c-257">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f3d8c-257">0x00000000</span></span>                                                                                                         |
| <span data-ttu-id="f3d8c-258">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f3d8c-258">System-Flags</span></span>           | <span data-ttu-id="f3d8c-259">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f3d8c-259">0x00000010</span></span>                                                                                                         |
| <span data-ttu-id="f3d8c-260">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f3d8c-260">Classes used in</span></span>        | [<span data-ttu-id="f3d8c-261">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="f3d8c-261">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="f3d8c-262">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="f3d8c-262">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="f3d8c-263">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="f3d8c-263">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f3d8c-264">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f3d8c-264">Windows Server 2012</span></span>



| <span data-ttu-id="f3d8c-265">Entrée</span><span class="sxs-lookup"><span data-stu-id="f3d8c-265">Entry</span></span> | <span data-ttu-id="f3d8c-266">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3d8c-266">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3d8c-267">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f3d8c-267">Link-Id</span></span>                | \-                                                                                                                 |
| <span data-ttu-id="f3d8c-268">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f3d8c-268">MAPI-Id</span></span>                | \-                                                                                                                 |
| <span data-ttu-id="f3d8c-269">System-Only</span><span class="sxs-lookup"><span data-stu-id="f3d8c-269">System-Only</span></span>            | <span data-ttu-id="f3d8c-270">Faux</span><span class="sxs-lookup"><span data-stu-id="f3d8c-270">False</span></span>                                                                                                              |
| <span data-ttu-id="f3d8c-271">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f3d8c-271">Is-Single-Valued</span></span>       | <span data-ttu-id="f3d8c-272">Faux</span><span class="sxs-lookup"><span data-stu-id="f3d8c-272">False</span></span>                                                                                                              |
| <span data-ttu-id="f3d8c-273">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f3d8c-273">Is Indexed</span></span>             | <span data-ttu-id="f3d8c-274">Faux</span><span class="sxs-lookup"><span data-stu-id="f3d8c-274">False</span></span>                                                                                                              |
| <span data-ttu-id="f3d8c-275">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f3d8c-275">In Global Catalog</span></span>      | <span data-ttu-id="f3d8c-276">Faux</span><span class="sxs-lookup"><span data-stu-id="f3d8c-276">False</span></span>                                                                                                              |
| <span data-ttu-id="f3d8c-277">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f3d8c-277">NT-Security-Descriptor</span></span> | <span data-ttu-id="f3d8c-278">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f3d8c-278">O:BAG:BAD:S:</span></span>                                                                                                       |
| <span data-ttu-id="f3d8c-279">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f3d8c-279">Range-Lower</span></span>            | <span data-ttu-id="f3d8c-280">16</span><span class="sxs-lookup"><span data-stu-id="f3d8c-280">16</span></span>                                                                                                                 |
| <span data-ttu-id="f3d8c-281">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f3d8c-281">Range-Upper</span></span>            | <span data-ttu-id="f3d8c-282">16</span><span class="sxs-lookup"><span data-stu-id="f3d8c-282">16</span></span>                                                                                                                 |
| <span data-ttu-id="f3d8c-283">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f3d8c-283">Search-Flags</span></span>           | <span data-ttu-id="f3d8c-284">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f3d8c-284">0x00000000</span></span>                                                                                                         |
| <span data-ttu-id="f3d8c-285">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f3d8c-285">System-Flags</span></span>           | <span data-ttu-id="f3d8c-286">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f3d8c-286">0x00000010</span></span>                                                                                                         |
| <span data-ttu-id="f3d8c-287">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f3d8c-287">Classes used in</span></span>        | [<span data-ttu-id="f3d8c-288">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="f3d8c-288">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="f3d8c-289">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="f3d8c-289">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="f3d8c-290">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="f3d8c-290">**User**</span></span>](c-user.md)<br/> |



 

 





