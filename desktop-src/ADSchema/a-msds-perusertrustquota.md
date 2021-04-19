---
title: Attribut de quota d’approbation MS-DS-per-utilisateur
description: Utilisé pour appliquer un quota par utilisateur pour la création de Trusted-Domain objets autorisés par le nouveau droit d’accès au contrôle, Create-entrant-Forest-Trust.
ms.assetid: 3b198b24-5282-4d13-8d35-88f34c11ce94
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory pour les attributs de niveau de confiance MS-DS-per-utilisateur
- Schéma Active Directory de l’attribut msDS-PerUserTrustQuota
topic_type:
- apiref
api_name:
- MS-DS-Per-User-Trust-Quota
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3bd6ffcac01de8997f806e6aa8a8e3bd6afbb66
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106522652"
---
# <a name="ms-ds-per-user-trust-quota-attribute"></a><span data-ttu-id="8b822-105">Attribut de quota d’approbation MS-DS-per-utilisateur</span><span class="sxs-lookup"><span data-stu-id="8b822-105">MS-DS-Per-User-Trust-Quota attribute</span></span>

<span data-ttu-id="8b822-106">Utilisé pour appliquer un quota par utilisateur pour la création de Trusted-Domain objets autorisés par le nouveau droit d’accès au contrôle, Create-entrant-Forest-Trust.</span><span class="sxs-lookup"><span data-stu-id="8b822-106">Used to enforce a per-user quota for creating Trusted-Domain objects that are authorized by the new control access right, Create-Inbound-Forest-Trust.</span></span> <span data-ttu-id="8b822-107">Cet attribut limite le nombre d’objets Trusted-Domain qui peuvent être créés par un utilisateur non-administrateur unique.</span><span class="sxs-lookup"><span data-stu-id="8b822-107">This attribute limits the number of Trusted-Domain objects that can be created by a single non-admin user.</span></span>



| <span data-ttu-id="8b822-108">Entrée</span><span class="sxs-lookup"><span data-stu-id="8b822-108">Entry</span></span> | <span data-ttu-id="8b822-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="8b822-109">Value</span></span> |
|-------------------|-------------------------------------------|
| <span data-ttu-id="8b822-110">CN</span><span class="sxs-lookup"><span data-stu-id="8b822-110">CN</span></span>                | <span data-ttu-id="8b822-111">MS-DS-per-utilisateur-quota de confiance</span><span class="sxs-lookup"><span data-stu-id="8b822-111">MS-DS-Per-User-Trust-Quota</span></span>                |
| <span data-ttu-id="8b822-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="8b822-112">Ldap-Display-Name</span></span> | <span data-ttu-id="8b822-113">msDS-PerUserTrustQuota</span><span class="sxs-lookup"><span data-stu-id="8b822-113">msDS-PerUserTrustQuota</span></span>                    |
| <span data-ttu-id="8b822-114">Taille</span><span class="sxs-lookup"><span data-stu-id="8b822-114">Size</span></span>              | \-                                        |
| <span data-ttu-id="8b822-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="8b822-115">Update Privilege</span></span>  | <span data-ttu-id="8b822-116">Administrateur de domaine</span><span class="sxs-lookup"><span data-stu-id="8b822-116">Domain administrator</span></span>                      |
| <span data-ttu-id="8b822-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="8b822-117">Update Frequency</span></span>  | <span data-ttu-id="8b822-118">À la création de la forêt et rarement après cela.</span><span class="sxs-lookup"><span data-stu-id="8b822-118">At forest creation and rarely after that.</span></span> |
| <span data-ttu-id="8b822-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8b822-119">Attribute-Id</span></span>      | <span data-ttu-id="8b822-120">1.2.840.113556.1.4.1788</span><span class="sxs-lookup"><span data-stu-id="8b822-120">1.2.840.113556.1.4.1788</span></span>                   |
| <span data-ttu-id="8b822-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="8b822-121">System-Id-Guid</span></span>    | <span data-ttu-id="8b822-122">d161adf0-ca24-4993-a3aa-8b2c981302e8</span><span class="sxs-lookup"><span data-stu-id="8b822-122">d161adf0-ca24-4993-a3aa-8b2c981302e8</span></span>      |
| <span data-ttu-id="8b822-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8b822-123">Syntax</span></span>            | [<span data-ttu-id="8b822-124">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="8b822-124">**Enumeration**</span></span>](s-enumeration.md)      |



## <a name="implementations"></a><span data-ttu-id="8b822-125">Implémentations</span><span class="sxs-lookup"><span data-stu-id="8b822-125">Implementations</span></span>

-   [<span data-ttu-id="8b822-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8b822-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8b822-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8b822-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8b822-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8b822-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8b822-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8b822-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8b822-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8b822-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="8b822-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8b822-131">Windows Server 2003</span></span>



| <span data-ttu-id="8b822-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="8b822-132">Entry</span></span> | <span data-ttu-id="8b822-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="8b822-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="8b822-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8b822-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="8b822-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8b822-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="8b822-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="8b822-136">System-Only</span></span>            | <span data-ttu-id="8b822-137">Faux</span><span class="sxs-lookup"><span data-stu-id="8b822-137">False</span></span>                                        |
| <span data-ttu-id="8b822-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8b822-138">Is-Single-Valued</span></span>       | <span data-ttu-id="8b822-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="8b822-139">True</span></span>                                         |
| <span data-ttu-id="8b822-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8b822-140">Is Indexed</span></span>             | <span data-ttu-id="8b822-141">Faux</span><span class="sxs-lookup"><span data-stu-id="8b822-141">False</span></span>                                        |
| <span data-ttu-id="8b822-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8b822-142">In Global Catalog</span></span>      | <span data-ttu-id="8b822-143">Faux</span><span class="sxs-lookup"><span data-stu-id="8b822-143">False</span></span>                                        |
| <span data-ttu-id="8b822-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8b822-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="8b822-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8b822-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="8b822-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8b822-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="8b822-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8b822-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="8b822-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8b822-148">Search-Flags</span></span>           | <span data-ttu-id="8b822-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8b822-149">0x00000000</span></span>                                   |
| <span data-ttu-id="8b822-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8b822-150">System-Flags</span></span>           | <span data-ttu-id="8b822-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8b822-151">0x00000010</span></span>                                   |
| <span data-ttu-id="8b822-152">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8b822-152">Classes used in</span></span>        | [<span data-ttu-id="8b822-153">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="8b822-153">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8b822-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8b822-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8b822-155">Entrée</span><span class="sxs-lookup"><span data-stu-id="8b822-155">Entry</span></span> | <span data-ttu-id="8b822-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="8b822-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="8b822-157">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8b822-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="8b822-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8b822-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="8b822-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="8b822-159">System-Only</span></span>            | <span data-ttu-id="8b822-160">Faux</span><span class="sxs-lookup"><span data-stu-id="8b822-160">False</span></span>                                        |
| <span data-ttu-id="8b822-161">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8b822-161">Is-Single-Valued</span></span>       | <span data-ttu-id="8b822-162">Vrai</span><span class="sxs-lookup"><span data-stu-id="8b822-162">True</span></span>                                         |
| <span data-ttu-id="8b822-163">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8b822-163">Is Indexed</span></span>             | <span data-ttu-id="8b822-164">Faux</span><span class="sxs-lookup"><span data-stu-id="8b822-164">False</span></span>                                        |
| <span data-ttu-id="8b822-165">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8b822-165">In Global Catalog</span></span>      | <span data-ttu-id="8b822-166">Faux</span><span class="sxs-lookup"><span data-stu-id="8b822-166">False</span></span>                                        |
| <span data-ttu-id="8b822-167">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8b822-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="8b822-168">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8b822-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="8b822-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8b822-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="8b822-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8b822-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="8b822-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8b822-171">Search-Flags</span></span>           | <span data-ttu-id="8b822-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8b822-172">0x00000000</span></span>                                   |
| <span data-ttu-id="8b822-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8b822-173">System-Flags</span></span>           | <span data-ttu-id="8b822-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8b822-174">0x00000010</span></span>                                   |
| <span data-ttu-id="8b822-175">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8b822-175">Classes used in</span></span>        | [<span data-ttu-id="8b822-176">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="8b822-176">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8b822-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8b822-177">Windows Server 2008</span></span>



| <span data-ttu-id="8b822-178">Entrée</span><span class="sxs-lookup"><span data-stu-id="8b822-178">Entry</span></span> | <span data-ttu-id="8b822-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="8b822-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="8b822-180">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8b822-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="8b822-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8b822-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="8b822-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="8b822-182">System-Only</span></span>            | <span data-ttu-id="8b822-183">Faux</span><span class="sxs-lookup"><span data-stu-id="8b822-183">False</span></span>                                        |
| <span data-ttu-id="8b822-184">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8b822-184">Is-Single-Valued</span></span>       | <span data-ttu-id="8b822-185">Vrai</span><span class="sxs-lookup"><span data-stu-id="8b822-185">True</span></span>                                         |
| <span data-ttu-id="8b822-186">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8b822-186">Is Indexed</span></span>             | <span data-ttu-id="8b822-187">Faux</span><span class="sxs-lookup"><span data-stu-id="8b822-187">False</span></span>                                        |
| <span data-ttu-id="8b822-188">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8b822-188">In Global Catalog</span></span>      | <span data-ttu-id="8b822-189">Faux</span><span class="sxs-lookup"><span data-stu-id="8b822-189">False</span></span>                                        |
| <span data-ttu-id="8b822-190">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8b822-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="8b822-191">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8b822-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="8b822-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8b822-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="8b822-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8b822-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="8b822-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8b822-194">Search-Flags</span></span>           | <span data-ttu-id="8b822-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8b822-195">0x00000000</span></span>                                   |
| <span data-ttu-id="8b822-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8b822-196">System-Flags</span></span>           | <span data-ttu-id="8b822-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8b822-197">0x00000010</span></span>                                   |
| <span data-ttu-id="8b822-198">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8b822-198">Classes used in</span></span>        | [<span data-ttu-id="8b822-199">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="8b822-199">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8b822-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8b822-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8b822-201">Entrée</span><span class="sxs-lookup"><span data-stu-id="8b822-201">Entry</span></span> | <span data-ttu-id="8b822-202">Valeur</span><span class="sxs-lookup"><span data-stu-id="8b822-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="8b822-203">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8b822-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="8b822-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8b822-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="8b822-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="8b822-205">System-Only</span></span>            | <span data-ttu-id="8b822-206">Faux</span><span class="sxs-lookup"><span data-stu-id="8b822-206">False</span></span>                                        |
| <span data-ttu-id="8b822-207">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8b822-207">Is-Single-Valued</span></span>       | <span data-ttu-id="8b822-208">Vrai</span><span class="sxs-lookup"><span data-stu-id="8b822-208">True</span></span>                                         |
| <span data-ttu-id="8b822-209">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8b822-209">Is Indexed</span></span>             | <span data-ttu-id="8b822-210">Faux</span><span class="sxs-lookup"><span data-stu-id="8b822-210">False</span></span>                                        |
| <span data-ttu-id="8b822-211">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8b822-211">In Global Catalog</span></span>      | <span data-ttu-id="8b822-212">Faux</span><span class="sxs-lookup"><span data-stu-id="8b822-212">False</span></span>                                        |
| <span data-ttu-id="8b822-213">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8b822-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="8b822-214">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8b822-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="8b822-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8b822-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="8b822-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8b822-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="8b822-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8b822-217">Search-Flags</span></span>           | <span data-ttu-id="8b822-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8b822-218">0x00000000</span></span>                                   |
| <span data-ttu-id="8b822-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8b822-219">System-Flags</span></span>           | <span data-ttu-id="8b822-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8b822-220">0x00000010</span></span>                                   |
| <span data-ttu-id="8b822-221">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8b822-221">Classes used in</span></span>        | [<span data-ttu-id="8b822-222">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="8b822-222">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8b822-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8b822-223">Windows Server 2012</span></span>



| <span data-ttu-id="8b822-224">Entrée</span><span class="sxs-lookup"><span data-stu-id="8b822-224">Entry</span></span> | <span data-ttu-id="8b822-225">Valeur</span><span class="sxs-lookup"><span data-stu-id="8b822-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="8b822-226">ID de lien</span><span class="sxs-lookup"><span data-stu-id="8b822-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="8b822-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8b822-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="8b822-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="8b822-228">System-Only</span></span>            | <span data-ttu-id="8b822-229">Faux</span><span class="sxs-lookup"><span data-stu-id="8b822-229">False</span></span>                                        |
| <span data-ttu-id="8b822-230">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="8b822-230">Is-Single-Valued</span></span>       | <span data-ttu-id="8b822-231">Vrai</span><span class="sxs-lookup"><span data-stu-id="8b822-231">True</span></span>                                         |
| <span data-ttu-id="8b822-232">Est indexé</span><span class="sxs-lookup"><span data-stu-id="8b822-232">Is Indexed</span></span>             | <span data-ttu-id="8b822-233">Faux</span><span class="sxs-lookup"><span data-stu-id="8b822-233">False</span></span>                                        |
| <span data-ttu-id="8b822-234">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="8b822-234">In Global Catalog</span></span>      | <span data-ttu-id="8b822-235">Faux</span><span class="sxs-lookup"><span data-stu-id="8b822-235">False</span></span>                                        |
| <span data-ttu-id="8b822-236">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="8b822-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="8b822-237">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="8b822-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="8b822-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8b822-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="8b822-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8b822-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="8b822-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8b822-240">Search-Flags</span></span>           | <span data-ttu-id="8b822-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8b822-241">0x00000000</span></span>                                   |
| <span data-ttu-id="8b822-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8b822-242">System-Flags</span></span>           | <span data-ttu-id="8b822-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8b822-243">0x00000010</span></span>                                   |
| <span data-ttu-id="8b822-244">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="8b822-244">Classes used in</span></span>        | [<span data-ttu-id="8b822-245">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="8b822-245">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 





