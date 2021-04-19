---
title: Attribut UAS-Compat
description: Indique si le gestionnaire de compte de sécurité appliquera des tailles de données pour rendre les Active Directory compatibles avec le système de comptes d’utilisateur LanManager (UAS).
ms.assetid: 745e271e-28f4-4012-83a8-606d88de0221
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut UAS-Compat
- Schéma AD de l’attribut uASCompat
topic_type:
- apiref
api_name:
- UAS-Compat
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6bbf1088f48c697b03c4ef423930be2dbd24617
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106514888"
---
# <a name="uas-compat-attribute"></a><span data-ttu-id="f6ec4-105">Attribut UAS-Compat</span><span class="sxs-lookup"><span data-stu-id="f6ec4-105">UAS-Compat attribute</span></span>

<span data-ttu-id="f6ec4-106">Indique si le gestionnaire de compte de sécurité appliquera des tailles de données pour rendre les Active Directory compatibles avec le système de comptes d’utilisateur LanManager (UAS).</span><span class="sxs-lookup"><span data-stu-id="f6ec4-106">Indicates if the security account manager will enforce data sizes to make Active Directory compatible with the LanManager User Account System (UAS).</span></span> <span data-ttu-id="f6ec4-107">Si cette valeur est égale à 0, aucune limite n’est appliquée.</span><span class="sxs-lookup"><span data-stu-id="f6ec4-107">If this value is 0, no limits are enforced.</span></span> <span data-ttu-id="f6ec4-108">Si cette valeur est 1, les limites suivantes sont appliquées.</span><span class="sxs-lookup"><span data-stu-id="f6ec4-108">If this value is 1, the following limits are enforced.</span></span>



| <span data-ttu-id="f6ec4-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="f6ec4-109">Value</span></span>                          | <span data-ttu-id="f6ec4-110">Longueur</span><span class="sxs-lookup"><span data-stu-id="f6ec4-110">Length</span></span>                         |
|--------------------------------|--------------------------------|
| <span data-ttu-id="f6ec4-111">Mot de passe</span><span class="sxs-lookup"><span data-stu-id="f6ec4-111">Password</span></span><br/>            | <span data-ttu-id="f6ec4-112">0 à 14 caractères</span><span class="sxs-lookup"><span data-stu-id="f6ec4-112">0 to 14 characters</span></span><br/>  |
| <span data-ttu-id="f6ec4-113">Nom du compte</span><span class="sxs-lookup"><span data-stu-id="f6ec4-113">Account Name</span></span><br/>        | <span data-ttu-id="f6ec4-114">de 0 à 20 caractères</span><span class="sxs-lookup"><span data-stu-id="f6ec4-114">0 to 20 characters</span></span><br/>  |
| <span data-ttu-id="f6ec4-115">Nom de domaine</span><span class="sxs-lookup"><span data-stu-id="f6ec4-115">Domain Name</span></span><br/>         | <span data-ttu-id="f6ec4-116">de 0 à 15 caractères</span><span class="sxs-lookup"><span data-stu-id="f6ec4-116">0 to 15 characters</span></span><br/>  |
| <span data-ttu-id="f6ec4-117">Nom d’ordinateur</span><span class="sxs-lookup"><span data-stu-id="f6ec4-117">Computer Name</span></span><br/>       | <span data-ttu-id="f6ec4-118">de 0 à 15 caractères</span><span class="sxs-lookup"><span data-stu-id="f6ec4-118">0 to 15 characters</span></span><br/>  |
| <span data-ttu-id="f6ec4-119">Commentaires</span><span class="sxs-lookup"><span data-stu-id="f6ec4-119">Comments</span></span><br/>            | <span data-ttu-id="f6ec4-120">0 à 48 caractères</span><span class="sxs-lookup"><span data-stu-id="f6ec4-120">0 to 48 characters</span></span><br/>  |
| <span data-ttu-id="f6ec4-121">Répertoire de base</span><span class="sxs-lookup"><span data-stu-id="f6ec4-121">Home Directory</span></span><br/>      | <span data-ttu-id="f6ec4-122">0 à 256 caractères</span><span class="sxs-lookup"><span data-stu-id="f6ec4-122">0 to 256 characters</span></span><br/> |
| <span data-ttu-id="f6ec4-123">Chemin du script</span><span class="sxs-lookup"><span data-stu-id="f6ec4-123">Script Path</span></span><br/>         | <span data-ttu-id="f6ec4-124">0 à 256 caractères</span><span class="sxs-lookup"><span data-stu-id="f6ec4-124">0 to 256 characters</span></span><br/> |
| <span data-ttu-id="f6ec4-125">Unités de temps par semaine</span><span class="sxs-lookup"><span data-stu-id="f6ec4-125">Time Units Per Week</span></span><br/> | <span data-ttu-id="f6ec4-126">168 bits (21 octets)</span><span class="sxs-lookup"><span data-stu-id="f6ec4-126">168 bits (21 bytes)</span></span><br/> |



 



| <span data-ttu-id="f6ec4-127">Entrée</span><span class="sxs-lookup"><span data-stu-id="f6ec4-127">Entry</span></span> | <span data-ttu-id="f6ec4-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="f6ec4-128">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="f6ec4-129">CN</span><span class="sxs-lookup"><span data-stu-id="f6ec4-129">CN</span></span>                | <span data-ttu-id="f6ec4-130">UAS-Compat</span><span class="sxs-lookup"><span data-stu-id="f6ec4-130">UAS-Compat</span></span>                           |
| <span data-ttu-id="f6ec4-131">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f6ec4-131">Ldap-Display-Name</span></span> | <span data-ttu-id="f6ec4-132">uASCompat</span><span class="sxs-lookup"><span data-stu-id="f6ec4-132">uASCompat</span></span>                            |
| <span data-ttu-id="f6ec4-133">Taille</span><span class="sxs-lookup"><span data-stu-id="f6ec4-133">Size</span></span>              | \-                                   |
| <span data-ttu-id="f6ec4-134">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="f6ec4-134">Update Privilege</span></span>  | <span data-ttu-id="f6ec4-135">Effectuée par un administrateur.</span><span class="sxs-lookup"><span data-stu-id="f6ec4-135">Performed by an administrator.</span></span>       |
| <span data-ttu-id="f6ec4-136">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="f6ec4-136">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="f6ec4-137">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f6ec4-137">Attribute-Id</span></span>      | <span data-ttu-id="f6ec4-138">1.2.840.113556.1.4.155</span><span class="sxs-lookup"><span data-stu-id="f6ec4-138">1.2.840.113556.1.4.155</span></span>               |
| <span data-ttu-id="f6ec4-139">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f6ec4-139">System-Id-Guid</span></span>    | <span data-ttu-id="f6ec4-140">bf967a61-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="f6ec4-140">bf967a61-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="f6ec4-141">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f6ec4-141">Syntax</span></span>            | [<span data-ttu-id="f6ec4-142">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="f6ec4-142">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="f6ec4-143">Implémentations</span><span class="sxs-lookup"><span data-stu-id="f6ec4-143">Implementations</span></span>

-   [<span data-ttu-id="f6ec4-144">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f6ec4-144">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f6ec4-145">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f6ec4-145">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f6ec4-146">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f6ec4-146">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f6ec4-147">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f6ec4-147">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f6ec4-148">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f6ec4-148">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f6ec4-149">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f6ec4-149">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f6ec4-150">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f6ec4-150">Windows 2000 Server</span></span>



| <span data-ttu-id="f6ec4-151">Entrée</span><span class="sxs-lookup"><span data-stu-id="f6ec4-151">Entry</span></span> | <span data-ttu-id="f6ec4-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="f6ec4-152">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="f6ec4-153">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f6ec4-153">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="f6ec4-154">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f6ec4-154">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="f6ec4-155">System-Only</span><span class="sxs-lookup"><span data-stu-id="f6ec4-155">System-Only</span></span>            | <span data-ttu-id="f6ec4-156">Faux</span><span class="sxs-lookup"><span data-stu-id="f6ec4-156">False</span></span>                                                 |
| <span data-ttu-id="f6ec4-157">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f6ec4-157">Is-Single-Valued</span></span>       | <span data-ttu-id="f6ec4-158">Vrai</span><span class="sxs-lookup"><span data-stu-id="f6ec4-158">True</span></span>                                                  |
| <span data-ttu-id="f6ec4-159">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f6ec4-159">Is Indexed</span></span>             | <span data-ttu-id="f6ec4-160">Faux</span><span class="sxs-lookup"><span data-stu-id="f6ec4-160">False</span></span>                                                 |
| <span data-ttu-id="f6ec4-161">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f6ec4-161">In Global Catalog</span></span>      | <span data-ttu-id="f6ec4-162">Faux</span><span class="sxs-lookup"><span data-stu-id="f6ec4-162">False</span></span>                                                 |
| <span data-ttu-id="f6ec4-163">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f6ec4-163">NT-Security-Descriptor</span></span> | <span data-ttu-id="f6ec4-164">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f6ec4-164">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="f6ec4-165">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f6ec4-165">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="f6ec4-166">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f6ec4-166">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="f6ec4-167">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f6ec4-167">Search-Flags</span></span>           | <span data-ttu-id="f6ec4-168">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f6ec4-168">0x00000000</span></span>                                            |
| <span data-ttu-id="f6ec4-169">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f6ec4-169">System-Flags</span></span>           | <span data-ttu-id="f6ec4-170">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f6ec4-170">0x00000010</span></span>                                            |
| <span data-ttu-id="f6ec4-171">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f6ec4-171">Classes used in</span></span>        | [<span data-ttu-id="f6ec4-172">**Sam-domaine-base**</span><span class="sxs-lookup"><span data-stu-id="f6ec4-172">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f6ec4-173">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f6ec4-173">Windows Server 2003</span></span>



| <span data-ttu-id="f6ec4-174">Entrée</span><span class="sxs-lookup"><span data-stu-id="f6ec4-174">Entry</span></span> | <span data-ttu-id="f6ec4-175">Valeur</span><span class="sxs-lookup"><span data-stu-id="f6ec4-175">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="f6ec4-176">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f6ec4-176">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="f6ec4-177">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f6ec4-177">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="f6ec4-178">System-Only</span><span class="sxs-lookup"><span data-stu-id="f6ec4-178">System-Only</span></span>            | <span data-ttu-id="f6ec4-179">Faux</span><span class="sxs-lookup"><span data-stu-id="f6ec4-179">False</span></span>                                                 |
| <span data-ttu-id="f6ec4-180">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f6ec4-180">Is-Single-Valued</span></span>       | <span data-ttu-id="f6ec4-181">Vrai</span><span class="sxs-lookup"><span data-stu-id="f6ec4-181">True</span></span>                                                  |
| <span data-ttu-id="f6ec4-182">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f6ec4-182">Is Indexed</span></span>             | <span data-ttu-id="f6ec4-183">Faux</span><span class="sxs-lookup"><span data-stu-id="f6ec4-183">False</span></span>                                                 |
| <span data-ttu-id="f6ec4-184">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f6ec4-184">In Global Catalog</span></span>      | <span data-ttu-id="f6ec4-185">Faux</span><span class="sxs-lookup"><span data-stu-id="f6ec4-185">False</span></span>                                                 |
| <span data-ttu-id="f6ec4-186">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f6ec4-186">NT-Security-Descriptor</span></span> | <span data-ttu-id="f6ec4-187">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f6ec4-187">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="f6ec4-188">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f6ec4-188">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="f6ec4-189">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f6ec4-189">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="f6ec4-190">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f6ec4-190">Search-Flags</span></span>           | <span data-ttu-id="f6ec4-191">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f6ec4-191">0x00000000</span></span>                                            |
| <span data-ttu-id="f6ec4-192">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f6ec4-192">System-Flags</span></span>           | <span data-ttu-id="f6ec4-193">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f6ec4-193">0x00000010</span></span>                                            |
| <span data-ttu-id="f6ec4-194">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f6ec4-194">Classes used in</span></span>        | [<span data-ttu-id="f6ec4-195">**Sam-domaine-base**</span><span class="sxs-lookup"><span data-stu-id="f6ec4-195">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f6ec4-196">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f6ec4-196">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f6ec4-197">Entrée</span><span class="sxs-lookup"><span data-stu-id="f6ec4-197">Entry</span></span> | <span data-ttu-id="f6ec4-198">Valeur</span><span class="sxs-lookup"><span data-stu-id="f6ec4-198">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="f6ec4-199">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f6ec4-199">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="f6ec4-200">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f6ec4-200">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="f6ec4-201">System-Only</span><span class="sxs-lookup"><span data-stu-id="f6ec4-201">System-Only</span></span>            | <span data-ttu-id="f6ec4-202">Faux</span><span class="sxs-lookup"><span data-stu-id="f6ec4-202">False</span></span>                                                 |
| <span data-ttu-id="f6ec4-203">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f6ec4-203">Is-Single-Valued</span></span>       | <span data-ttu-id="f6ec4-204">Vrai</span><span class="sxs-lookup"><span data-stu-id="f6ec4-204">True</span></span>                                                  |
| <span data-ttu-id="f6ec4-205">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f6ec4-205">Is Indexed</span></span>             | <span data-ttu-id="f6ec4-206">Faux</span><span class="sxs-lookup"><span data-stu-id="f6ec4-206">False</span></span>                                                 |
| <span data-ttu-id="f6ec4-207">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f6ec4-207">In Global Catalog</span></span>      | <span data-ttu-id="f6ec4-208">Faux</span><span class="sxs-lookup"><span data-stu-id="f6ec4-208">False</span></span>                                                 |
| <span data-ttu-id="f6ec4-209">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f6ec4-209">NT-Security-Descriptor</span></span> | <span data-ttu-id="f6ec4-210">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f6ec4-210">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="f6ec4-211">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f6ec4-211">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="f6ec4-212">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f6ec4-212">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="f6ec4-213">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f6ec4-213">Search-Flags</span></span>           | <span data-ttu-id="f6ec4-214">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f6ec4-214">0x00000000</span></span>                                            |
| <span data-ttu-id="f6ec4-215">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f6ec4-215">System-Flags</span></span>           | <span data-ttu-id="f6ec4-216">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f6ec4-216">0x00000010</span></span>                                            |
| <span data-ttu-id="f6ec4-217">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f6ec4-217">Classes used in</span></span>        | [<span data-ttu-id="f6ec4-218">**Sam-domaine-base**</span><span class="sxs-lookup"><span data-stu-id="f6ec4-218">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f6ec4-219">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f6ec4-219">Windows Server 2008</span></span>



| <span data-ttu-id="f6ec4-220">Entrée</span><span class="sxs-lookup"><span data-stu-id="f6ec4-220">Entry</span></span> | <span data-ttu-id="f6ec4-221">Valeur</span><span class="sxs-lookup"><span data-stu-id="f6ec4-221">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="f6ec4-222">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f6ec4-222">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="f6ec4-223">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f6ec4-223">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="f6ec4-224">System-Only</span><span class="sxs-lookup"><span data-stu-id="f6ec4-224">System-Only</span></span>            | <span data-ttu-id="f6ec4-225">Faux</span><span class="sxs-lookup"><span data-stu-id="f6ec4-225">False</span></span>                                                 |
| <span data-ttu-id="f6ec4-226">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f6ec4-226">Is-Single-Valued</span></span>       | <span data-ttu-id="f6ec4-227">Vrai</span><span class="sxs-lookup"><span data-stu-id="f6ec4-227">True</span></span>                                                  |
| <span data-ttu-id="f6ec4-228">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f6ec4-228">Is Indexed</span></span>             | <span data-ttu-id="f6ec4-229">Faux</span><span class="sxs-lookup"><span data-stu-id="f6ec4-229">False</span></span>                                                 |
| <span data-ttu-id="f6ec4-230">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f6ec4-230">In Global Catalog</span></span>      | <span data-ttu-id="f6ec4-231">Faux</span><span class="sxs-lookup"><span data-stu-id="f6ec4-231">False</span></span>                                                 |
| <span data-ttu-id="f6ec4-232">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f6ec4-232">NT-Security-Descriptor</span></span> | <span data-ttu-id="f6ec4-233">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f6ec4-233">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="f6ec4-234">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f6ec4-234">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="f6ec4-235">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f6ec4-235">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="f6ec4-236">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f6ec4-236">Search-Flags</span></span>           | <span data-ttu-id="f6ec4-237">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f6ec4-237">0x00000000</span></span>                                            |
| <span data-ttu-id="f6ec4-238">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f6ec4-238">System-Flags</span></span>           | <span data-ttu-id="f6ec4-239">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f6ec4-239">0x00000010</span></span>                                            |
| <span data-ttu-id="f6ec4-240">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f6ec4-240">Classes used in</span></span>        | [<span data-ttu-id="f6ec4-241">**Sam-domaine-base**</span><span class="sxs-lookup"><span data-stu-id="f6ec4-241">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f6ec4-242">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f6ec4-242">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f6ec4-243">Entrée</span><span class="sxs-lookup"><span data-stu-id="f6ec4-243">Entry</span></span> | <span data-ttu-id="f6ec4-244">Valeur</span><span class="sxs-lookup"><span data-stu-id="f6ec4-244">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="f6ec4-245">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f6ec4-245">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="f6ec4-246">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f6ec4-246">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="f6ec4-247">System-Only</span><span class="sxs-lookup"><span data-stu-id="f6ec4-247">System-Only</span></span>            | <span data-ttu-id="f6ec4-248">Faux</span><span class="sxs-lookup"><span data-stu-id="f6ec4-248">False</span></span>                                                 |
| <span data-ttu-id="f6ec4-249">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f6ec4-249">Is-Single-Valued</span></span>       | <span data-ttu-id="f6ec4-250">Vrai</span><span class="sxs-lookup"><span data-stu-id="f6ec4-250">True</span></span>                                                  |
| <span data-ttu-id="f6ec4-251">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f6ec4-251">Is Indexed</span></span>             | <span data-ttu-id="f6ec4-252">Faux</span><span class="sxs-lookup"><span data-stu-id="f6ec4-252">False</span></span>                                                 |
| <span data-ttu-id="f6ec4-253">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f6ec4-253">In Global Catalog</span></span>      | <span data-ttu-id="f6ec4-254">Faux</span><span class="sxs-lookup"><span data-stu-id="f6ec4-254">False</span></span>                                                 |
| <span data-ttu-id="f6ec4-255">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f6ec4-255">NT-Security-Descriptor</span></span> | <span data-ttu-id="f6ec4-256">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f6ec4-256">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="f6ec4-257">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f6ec4-257">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="f6ec4-258">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f6ec4-258">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="f6ec4-259">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f6ec4-259">Search-Flags</span></span>           | <span data-ttu-id="f6ec4-260">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f6ec4-260">0x00000000</span></span>                                            |
| <span data-ttu-id="f6ec4-261">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f6ec4-261">System-Flags</span></span>           | <span data-ttu-id="f6ec4-262">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f6ec4-262">0x00000010</span></span>                                            |
| <span data-ttu-id="f6ec4-263">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f6ec4-263">Classes used in</span></span>        | [<span data-ttu-id="f6ec4-264">**Sam-domaine-base**</span><span class="sxs-lookup"><span data-stu-id="f6ec4-264">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f6ec4-265">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f6ec4-265">Windows Server 2012</span></span>



| <span data-ttu-id="f6ec4-266">Entrée</span><span class="sxs-lookup"><span data-stu-id="f6ec4-266">Entry</span></span> | <span data-ttu-id="f6ec4-267">Valeur</span><span class="sxs-lookup"><span data-stu-id="f6ec4-267">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="f6ec4-268">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f6ec4-268">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="f6ec4-269">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f6ec4-269">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="f6ec4-270">System-Only</span><span class="sxs-lookup"><span data-stu-id="f6ec4-270">System-Only</span></span>            | <span data-ttu-id="f6ec4-271">Faux</span><span class="sxs-lookup"><span data-stu-id="f6ec4-271">False</span></span>                                                 |
| <span data-ttu-id="f6ec4-272">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f6ec4-272">Is-Single-Valued</span></span>       | <span data-ttu-id="f6ec4-273">Vrai</span><span class="sxs-lookup"><span data-stu-id="f6ec4-273">True</span></span>                                                  |
| <span data-ttu-id="f6ec4-274">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f6ec4-274">Is Indexed</span></span>             | <span data-ttu-id="f6ec4-275">Faux</span><span class="sxs-lookup"><span data-stu-id="f6ec4-275">False</span></span>                                                 |
| <span data-ttu-id="f6ec4-276">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f6ec4-276">In Global Catalog</span></span>      | <span data-ttu-id="f6ec4-277">Faux</span><span class="sxs-lookup"><span data-stu-id="f6ec4-277">False</span></span>                                                 |
| <span data-ttu-id="f6ec4-278">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f6ec4-278">NT-Security-Descriptor</span></span> | <span data-ttu-id="f6ec4-279">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f6ec4-279">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="f6ec4-280">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f6ec4-280">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="f6ec4-281">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f6ec4-281">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="f6ec4-282">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f6ec4-282">Search-Flags</span></span>           | <span data-ttu-id="f6ec4-283">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f6ec4-283">0x00000000</span></span>                                            |
| <span data-ttu-id="f6ec4-284">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f6ec4-284">System-Flags</span></span>           | <span data-ttu-id="f6ec4-285">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f6ec4-285">0x00000010</span></span>                                            |
| <span data-ttu-id="f6ec4-286">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f6ec4-286">Classes used in</span></span>        | [<span data-ttu-id="f6ec4-287">**Sam-domaine-base**</span><span class="sxs-lookup"><span data-stu-id="f6ec4-287">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



 

 





