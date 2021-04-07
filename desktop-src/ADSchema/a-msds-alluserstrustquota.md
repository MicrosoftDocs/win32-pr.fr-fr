---
title: MS-DS-tous les utilisateurs-attribut de quota de confiance
description: Utilisé pour appliquer un quota d’utilisateurs combinés sur le nombre total d’objets Trusted-Domain créés à l’aide du nouveau droit d’accès de contrôle, créez-entrant-forêt-confiance.
ms.assetid: 77e70a26-99b4-4b49-a984-6809d02f6fb8
ms.tgt_platform: multiple
keywords:
- Schéma AD des attributs MS-DS-All-Users-Trust-quota
- Schéma Active Directory de l’attribut msDS-AllUsersTrustQuota
topic_type:
- apiref
api_name:
- MS-DS-All-Users-Trust-Quota
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0538ff38f1eb57f339a8e0e244a378a36dd92498
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103745188"
---
# <a name="ms-ds-all-users-trust-quota-attribute"></a><span data-ttu-id="c44f0-105">MS-DS-tous les utilisateurs-attribut de quota de confiance</span><span class="sxs-lookup"><span data-stu-id="c44f0-105">MS-DS-All-Users-Trust-Quota attribute</span></span>

<span data-ttu-id="c44f0-106">Utilisé pour appliquer un quota d’utilisateurs combinés sur le nombre total d’objets Trusted-Domain créés à l’aide du nouveau droit d’accès de contrôle, créez-entrant-forêt-confiance.</span><span class="sxs-lookup"><span data-stu-id="c44f0-106">Used to enforce a combined users quota on the total number of Trusted-Domain objects created by using the new control access right, Create-Inbound-Forest-Trust.</span></span>



| <span data-ttu-id="c44f0-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="c44f0-107">Entry</span></span> | <span data-ttu-id="c44f0-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="c44f0-108">Value</span></span> |
|-------------------|-------------------------------------------|
| <span data-ttu-id="c44f0-109">CN</span><span class="sxs-lookup"><span data-stu-id="c44f0-109">CN</span></span>                | <span data-ttu-id="c44f0-110">MS-DS-tout-utilisateurs-approbation-quota</span><span class="sxs-lookup"><span data-stu-id="c44f0-110">MS-DS-All-Users-Trust-Quota</span></span>               |
| <span data-ttu-id="c44f0-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="c44f0-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c44f0-112">msDS-AllUsersTrustQuota</span><span class="sxs-lookup"><span data-stu-id="c44f0-112">msDS-AllUsersTrustQuota</span></span>                   |
| <span data-ttu-id="c44f0-113">Taille</span><span class="sxs-lookup"><span data-stu-id="c44f0-113">Size</span></span>              | \-                                        |
| <span data-ttu-id="c44f0-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="c44f0-114">Update Privilege</span></span>  | <span data-ttu-id="c44f0-115">Administrateur de domaine</span><span class="sxs-lookup"><span data-stu-id="c44f0-115">Domain administrator</span></span>                      |
| <span data-ttu-id="c44f0-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="c44f0-116">Update Frequency</span></span>  | <span data-ttu-id="c44f0-117">À la création de la forêt et rarement après cela.</span><span class="sxs-lookup"><span data-stu-id="c44f0-117">At forest creation and rarely after that.</span></span> |
| <span data-ttu-id="c44f0-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c44f0-118">Attribute-Id</span></span>      | <span data-ttu-id="c44f0-119">1.2.840.113556.1.4.1789</span><span class="sxs-lookup"><span data-stu-id="c44f0-119">1.2.840.113556.1.4.1789</span></span>                   |
| <span data-ttu-id="c44f0-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c44f0-120">System-Id-Guid</span></span>    | <span data-ttu-id="c44f0-121">d3aa4a5c-4e03-4810-97aa-2b339e7a434b</span><span class="sxs-lookup"><span data-stu-id="c44f0-121">d3aa4a5c-4e03-4810-97aa-2b339e7a434b</span></span>      |
| <span data-ttu-id="c44f0-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c44f0-122">Syntax</span></span>            | [<span data-ttu-id="c44f0-123">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="c44f0-123">**Enumeration**</span></span>](s-enumeration.md)      |



## <a name="implementations"></a><span data-ttu-id="c44f0-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="c44f0-124">Implementations</span></span>

-   [<span data-ttu-id="c44f0-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c44f0-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c44f0-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c44f0-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c44f0-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c44f0-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c44f0-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c44f0-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c44f0-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c44f0-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="c44f0-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c44f0-130">Windows Server 2003</span></span>



| <span data-ttu-id="c44f0-131">Entrée</span><span class="sxs-lookup"><span data-stu-id="c44f0-131">Entry</span></span> | <span data-ttu-id="c44f0-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="c44f0-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="c44f0-133">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c44f0-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="c44f0-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c44f0-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="c44f0-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="c44f0-135">System-Only</span></span>            | <span data-ttu-id="c44f0-136">Faux</span><span class="sxs-lookup"><span data-stu-id="c44f0-136">False</span></span>                                        |
| <span data-ttu-id="c44f0-137">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c44f0-137">Is-Single-Valued</span></span>       | <span data-ttu-id="c44f0-138">Vrai</span><span class="sxs-lookup"><span data-stu-id="c44f0-138">True</span></span>                                         |
| <span data-ttu-id="c44f0-139">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c44f0-139">Is Indexed</span></span>             | <span data-ttu-id="c44f0-140">Faux</span><span class="sxs-lookup"><span data-stu-id="c44f0-140">False</span></span>                                        |
| <span data-ttu-id="c44f0-141">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c44f0-141">In Global Catalog</span></span>      | <span data-ttu-id="c44f0-142">Faux</span><span class="sxs-lookup"><span data-stu-id="c44f0-142">False</span></span>                                        |
| <span data-ttu-id="c44f0-143">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c44f0-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="c44f0-144">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c44f0-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="c44f0-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c44f0-145">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="c44f0-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c44f0-146">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="c44f0-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c44f0-147">Search-Flags</span></span>           | <span data-ttu-id="c44f0-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c44f0-148">0x00000000</span></span>                                   |
| <span data-ttu-id="c44f0-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c44f0-149">System-Flags</span></span>           | <span data-ttu-id="c44f0-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c44f0-150">0x00000010</span></span>                                   |
| <span data-ttu-id="c44f0-151">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c44f0-151">Classes used in</span></span>        | [<span data-ttu-id="c44f0-152">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="c44f0-152">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c44f0-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c44f0-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c44f0-154">Entrée</span><span class="sxs-lookup"><span data-stu-id="c44f0-154">Entry</span></span> | <span data-ttu-id="c44f0-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="c44f0-155">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="c44f0-156">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c44f0-156">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="c44f0-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c44f0-157">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="c44f0-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="c44f0-158">System-Only</span></span>            | <span data-ttu-id="c44f0-159">Faux</span><span class="sxs-lookup"><span data-stu-id="c44f0-159">False</span></span>                                        |
| <span data-ttu-id="c44f0-160">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c44f0-160">Is-Single-Valued</span></span>       | <span data-ttu-id="c44f0-161">Vrai</span><span class="sxs-lookup"><span data-stu-id="c44f0-161">True</span></span>                                         |
| <span data-ttu-id="c44f0-162">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c44f0-162">Is Indexed</span></span>             | <span data-ttu-id="c44f0-163">Faux</span><span class="sxs-lookup"><span data-stu-id="c44f0-163">False</span></span>                                        |
| <span data-ttu-id="c44f0-164">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c44f0-164">In Global Catalog</span></span>      | <span data-ttu-id="c44f0-165">Faux</span><span class="sxs-lookup"><span data-stu-id="c44f0-165">False</span></span>                                        |
| <span data-ttu-id="c44f0-166">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c44f0-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="c44f0-167">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c44f0-167">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="c44f0-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c44f0-168">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="c44f0-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c44f0-169">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="c44f0-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c44f0-170">Search-Flags</span></span>           | <span data-ttu-id="c44f0-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c44f0-171">0x00000000</span></span>                                   |
| <span data-ttu-id="c44f0-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c44f0-172">System-Flags</span></span>           | <span data-ttu-id="c44f0-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c44f0-173">0x00000010</span></span>                                   |
| <span data-ttu-id="c44f0-174">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c44f0-174">Classes used in</span></span>        | [<span data-ttu-id="c44f0-175">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="c44f0-175">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c44f0-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c44f0-176">Windows Server 2008</span></span>



| <span data-ttu-id="c44f0-177">Entrée</span><span class="sxs-lookup"><span data-stu-id="c44f0-177">Entry</span></span> | <span data-ttu-id="c44f0-178">Valeur</span><span class="sxs-lookup"><span data-stu-id="c44f0-178">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="c44f0-179">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c44f0-179">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="c44f0-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c44f0-180">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="c44f0-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="c44f0-181">System-Only</span></span>            | <span data-ttu-id="c44f0-182">Faux</span><span class="sxs-lookup"><span data-stu-id="c44f0-182">False</span></span>                                        |
| <span data-ttu-id="c44f0-183">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c44f0-183">Is-Single-Valued</span></span>       | <span data-ttu-id="c44f0-184">Vrai</span><span class="sxs-lookup"><span data-stu-id="c44f0-184">True</span></span>                                         |
| <span data-ttu-id="c44f0-185">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c44f0-185">Is Indexed</span></span>             | <span data-ttu-id="c44f0-186">Faux</span><span class="sxs-lookup"><span data-stu-id="c44f0-186">False</span></span>                                        |
| <span data-ttu-id="c44f0-187">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c44f0-187">In Global Catalog</span></span>      | <span data-ttu-id="c44f0-188">Faux</span><span class="sxs-lookup"><span data-stu-id="c44f0-188">False</span></span>                                        |
| <span data-ttu-id="c44f0-189">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c44f0-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="c44f0-190">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c44f0-190">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="c44f0-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c44f0-191">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="c44f0-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c44f0-192">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="c44f0-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c44f0-193">Search-Flags</span></span>           | <span data-ttu-id="c44f0-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c44f0-194">0x00000000</span></span>                                   |
| <span data-ttu-id="c44f0-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c44f0-195">System-Flags</span></span>           | <span data-ttu-id="c44f0-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c44f0-196">0x00000010</span></span>                                   |
| <span data-ttu-id="c44f0-197">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c44f0-197">Classes used in</span></span>        | [<span data-ttu-id="c44f0-198">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="c44f0-198">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c44f0-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c44f0-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c44f0-200">Entrée</span><span class="sxs-lookup"><span data-stu-id="c44f0-200">Entry</span></span> | <span data-ttu-id="c44f0-201">Valeur</span><span class="sxs-lookup"><span data-stu-id="c44f0-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="c44f0-202">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c44f0-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="c44f0-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c44f0-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="c44f0-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="c44f0-204">System-Only</span></span>            | <span data-ttu-id="c44f0-205">Faux</span><span class="sxs-lookup"><span data-stu-id="c44f0-205">False</span></span>                                        |
| <span data-ttu-id="c44f0-206">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c44f0-206">Is-Single-Valued</span></span>       | <span data-ttu-id="c44f0-207">Vrai</span><span class="sxs-lookup"><span data-stu-id="c44f0-207">True</span></span>                                         |
| <span data-ttu-id="c44f0-208">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c44f0-208">Is Indexed</span></span>             | <span data-ttu-id="c44f0-209">Faux</span><span class="sxs-lookup"><span data-stu-id="c44f0-209">False</span></span>                                        |
| <span data-ttu-id="c44f0-210">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c44f0-210">In Global Catalog</span></span>      | <span data-ttu-id="c44f0-211">Faux</span><span class="sxs-lookup"><span data-stu-id="c44f0-211">False</span></span>                                        |
| <span data-ttu-id="c44f0-212">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c44f0-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="c44f0-213">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c44f0-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="c44f0-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c44f0-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="c44f0-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c44f0-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="c44f0-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c44f0-216">Search-Flags</span></span>           | <span data-ttu-id="c44f0-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c44f0-217">0x00000000</span></span>                                   |
| <span data-ttu-id="c44f0-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c44f0-218">System-Flags</span></span>           | <span data-ttu-id="c44f0-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c44f0-219">0x00000010</span></span>                                   |
| <span data-ttu-id="c44f0-220">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c44f0-220">Classes used in</span></span>        | [<span data-ttu-id="c44f0-221">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="c44f0-221">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c44f0-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c44f0-222">Windows Server 2012</span></span>



| <span data-ttu-id="c44f0-223">Entrée</span><span class="sxs-lookup"><span data-stu-id="c44f0-223">Entry</span></span> | <span data-ttu-id="c44f0-224">Valeur</span><span class="sxs-lookup"><span data-stu-id="c44f0-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="c44f0-225">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c44f0-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="c44f0-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c44f0-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="c44f0-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="c44f0-227">System-Only</span></span>            | <span data-ttu-id="c44f0-228">Faux</span><span class="sxs-lookup"><span data-stu-id="c44f0-228">False</span></span>                                        |
| <span data-ttu-id="c44f0-229">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c44f0-229">Is-Single-Valued</span></span>       | <span data-ttu-id="c44f0-230">Vrai</span><span class="sxs-lookup"><span data-stu-id="c44f0-230">True</span></span>                                         |
| <span data-ttu-id="c44f0-231">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c44f0-231">Is Indexed</span></span>             | <span data-ttu-id="c44f0-232">Faux</span><span class="sxs-lookup"><span data-stu-id="c44f0-232">False</span></span>                                        |
| <span data-ttu-id="c44f0-233">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c44f0-233">In Global Catalog</span></span>      | <span data-ttu-id="c44f0-234">Faux</span><span class="sxs-lookup"><span data-stu-id="c44f0-234">False</span></span>                                        |
| <span data-ttu-id="c44f0-235">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c44f0-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="c44f0-236">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c44f0-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="c44f0-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c44f0-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="c44f0-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c44f0-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="c44f0-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c44f0-239">Search-Flags</span></span>           | <span data-ttu-id="c44f0-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c44f0-240">0x00000000</span></span>                                   |
| <span data-ttu-id="c44f0-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c44f0-241">System-Flags</span></span>           | <span data-ttu-id="c44f0-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c44f0-242">0x00000010</span></span>                                   |
| <span data-ttu-id="c44f0-243">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c44f0-243">Classes used in</span></span>        | [<span data-ttu-id="c44f0-244">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="c44f0-244">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 





