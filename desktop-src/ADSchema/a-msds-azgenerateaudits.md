---
title: attribut ms-DS-AZ-Generate-audites
description: Champ booléen qui indique si les audits d’exécution doivent être activés (inclure les audits pour les vérifications d’accès, etc.).
ms.assetid: 23578f6a-7e7f-4871-9503-73f2ce598173
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory ms-DS-AZ-Generate-audites
- Schéma Active Directory de l’attribut msDS-AzGenerateAudits
topic_type:
- apiref
api_name:
- ms-DS-Az-Generate-Audits
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 645bdfd2f822139072391d401ecedfedee8680b8
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845501"
---
# <a name="ms-ds-az-generate-audits-attribute"></a><span data-ttu-id="6cdc7-105">attribut ms-DS-AZ-Generate-audites</span><span class="sxs-lookup"><span data-stu-id="6cdc7-105">ms-DS-Az-Generate-Audits attribute</span></span>

<span data-ttu-id="6cdc7-106">Champ booléen qui indique si les audits d’exécution doivent être activés (inclure les audits pour les vérifications d’accès, etc.).</span><span class="sxs-lookup"><span data-stu-id="6cdc7-106">A Boolean field that indicates whether runtime audits need to be turned on (include audits for access checks, and so on).</span></span>



| <span data-ttu-id="6cdc7-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="6cdc7-107">Entry</span></span> | <span data-ttu-id="6cdc7-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="6cdc7-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="6cdc7-109">CN</span><span class="sxs-lookup"><span data-stu-id="6cdc7-109">CN</span></span>                | <span data-ttu-id="6cdc7-110">ms-DS-AZ-Generate-audites</span><span class="sxs-lookup"><span data-stu-id="6cdc7-110">ms-DS-Az-Generate-Audits</span></span>                |
| <span data-ttu-id="6cdc7-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="6cdc7-111">Ldap-Display-Name</span></span> | <span data-ttu-id="6cdc7-112">msDS-AzGenerateAudits</span><span class="sxs-lookup"><span data-stu-id="6cdc7-112">msDS-AzGenerateAudits</span></span>                   |
| <span data-ttu-id="6cdc7-113">Taille</span><span class="sxs-lookup"><span data-stu-id="6cdc7-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="6cdc7-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="6cdc7-114">Update Privilege</span></span>  | <span data-ttu-id="6cdc7-115">Administrateur AzRoles</span><span class="sxs-lookup"><span data-stu-id="6cdc7-115">AzRoles admin</span></span>                           |
| <span data-ttu-id="6cdc7-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="6cdc7-116">Update Frequency</span></span>  | <span data-ttu-id="6cdc7-117">Pendant l’initialisation ou la modification de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="6cdc7-117">During initialization or policy change.</span></span> |
| <span data-ttu-id="6cdc7-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6cdc7-118">Attribute-Id</span></span>      | <span data-ttu-id="6cdc7-119">1.2.840.113556.1.4.1805</span><span class="sxs-lookup"><span data-stu-id="6cdc7-119">1.2.840.113556.1.4.1805</span></span>                 |
| <span data-ttu-id="6cdc7-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="6cdc7-120">System-Id-Guid</span></span>    | <span data-ttu-id="6cdc7-121">f90abab0-186C-4418-bb85-88447c87222a</span><span class="sxs-lookup"><span data-stu-id="6cdc7-121">f90abab0-186c-4418-bb85-88447c87222a</span></span>    |
| <span data-ttu-id="6cdc7-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6cdc7-122">Syntax</span></span>            | [<span data-ttu-id="6cdc7-123">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="6cdc7-123">**Boolean**</span></span>](s-boolean.md)            |



## <a name="implementations"></a><span data-ttu-id="6cdc7-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="6cdc7-124">Implementations</span></span>

-   [<span data-ttu-id="6cdc7-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6cdc7-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6cdc7-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6cdc7-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6cdc7-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6cdc7-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6cdc7-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6cdc7-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6cdc7-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6cdc7-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="6cdc7-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6cdc7-130">Windows Server 2003</span></span>



| <span data-ttu-id="6cdc7-131">Entrée</span><span class="sxs-lookup"><span data-stu-id="6cdc7-131">Entry</span></span> | <span data-ttu-id="6cdc7-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="6cdc7-132">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cdc7-133">ID de lien</span><span class="sxs-lookup"><span data-stu-id="6cdc7-133">Link-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="6cdc7-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6cdc7-134">MAPI-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="6cdc7-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="6cdc7-135">System-Only</span></span>            | <span data-ttu-id="6cdc7-136">Faux</span><span class="sxs-lookup"><span data-stu-id="6cdc7-136">False</span></span>                                                                                                                              |
| <span data-ttu-id="6cdc7-137">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="6cdc7-137">Is-Single-Valued</span></span>       | <span data-ttu-id="6cdc7-138">Vrai</span><span class="sxs-lookup"><span data-stu-id="6cdc7-138">True</span></span>                                                                                                                               |
| <span data-ttu-id="6cdc7-139">Est indexé</span><span class="sxs-lookup"><span data-stu-id="6cdc7-139">Is Indexed</span></span>             | <span data-ttu-id="6cdc7-140">Faux</span><span class="sxs-lookup"><span data-stu-id="6cdc7-140">False</span></span>                                                                                                                              |
| <span data-ttu-id="6cdc7-141">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="6cdc7-141">In Global Catalog</span></span>      | <span data-ttu-id="6cdc7-142">Faux</span><span class="sxs-lookup"><span data-stu-id="6cdc7-142">False</span></span>                                                                                                                              |
| <span data-ttu-id="6cdc7-143">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="6cdc7-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="6cdc7-144">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="6cdc7-144">O:BAG:BAD:S:</span></span>                                                                                                                       |
| <span data-ttu-id="6cdc7-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6cdc7-145">Range-Lower</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="6cdc7-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6cdc7-146">Range-Upper</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="6cdc7-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6cdc7-147">Search-Flags</span></span>           | <span data-ttu-id="6cdc7-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6cdc7-148">0x00000000</span></span>                                                                                                                         |
| <span data-ttu-id="6cdc7-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6cdc7-149">System-Flags</span></span>           | <span data-ttu-id="6cdc7-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6cdc7-150">0x00000010</span></span>                                                                                                                         |
| <span data-ttu-id="6cdc7-151">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="6cdc7-151">Classes used in</span></span>        | [<span data-ttu-id="6cdc7-152">**ms-DS-AZ-admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="6cdc7-152">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> [<span data-ttu-id="6cdc7-153">**ms-DS-AZ-application**</span><span class="sxs-lookup"><span data-stu-id="6cdc7-153">**ms-DS-Az-Application**</span></span>](c-msds-azapplication.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6cdc7-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6cdc7-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6cdc7-155">Entrée</span><span class="sxs-lookup"><span data-stu-id="6cdc7-155">Entry</span></span> | <span data-ttu-id="6cdc7-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="6cdc7-156">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cdc7-157">ID de lien</span><span class="sxs-lookup"><span data-stu-id="6cdc7-157">Link-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="6cdc7-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6cdc7-158">MAPI-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="6cdc7-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="6cdc7-159">System-Only</span></span>            | <span data-ttu-id="6cdc7-160">Faux</span><span class="sxs-lookup"><span data-stu-id="6cdc7-160">False</span></span>                                                                                                                              |
| <span data-ttu-id="6cdc7-161">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="6cdc7-161">Is-Single-Valued</span></span>       | <span data-ttu-id="6cdc7-162">Vrai</span><span class="sxs-lookup"><span data-stu-id="6cdc7-162">True</span></span>                                                                                                                               |
| <span data-ttu-id="6cdc7-163">Est indexé</span><span class="sxs-lookup"><span data-stu-id="6cdc7-163">Is Indexed</span></span>             | <span data-ttu-id="6cdc7-164">Faux</span><span class="sxs-lookup"><span data-stu-id="6cdc7-164">False</span></span>                                                                                                                              |
| <span data-ttu-id="6cdc7-165">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="6cdc7-165">In Global Catalog</span></span>      | <span data-ttu-id="6cdc7-166">Faux</span><span class="sxs-lookup"><span data-stu-id="6cdc7-166">False</span></span>                                                                                                                              |
| <span data-ttu-id="6cdc7-167">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="6cdc7-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="6cdc7-168">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="6cdc7-168">O:BAG:BAD:S:</span></span>                                                                                                                       |
| <span data-ttu-id="6cdc7-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6cdc7-169">Range-Lower</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="6cdc7-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6cdc7-170">Range-Upper</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="6cdc7-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6cdc7-171">Search-Flags</span></span>           | <span data-ttu-id="6cdc7-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6cdc7-172">0x00000000</span></span>                                                                                                                         |
| <span data-ttu-id="6cdc7-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6cdc7-173">System-Flags</span></span>           | <span data-ttu-id="6cdc7-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6cdc7-174">0x00000010</span></span>                                                                                                                         |
| <span data-ttu-id="6cdc7-175">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="6cdc7-175">Classes used in</span></span>        | [<span data-ttu-id="6cdc7-176">**ms-DS-AZ-admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="6cdc7-176">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> [<span data-ttu-id="6cdc7-177">**ms-DS-AZ-application**</span><span class="sxs-lookup"><span data-stu-id="6cdc7-177">**ms-DS-Az-Application**</span></span>](c-msds-azapplication.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6cdc7-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6cdc7-178">Windows Server 2008</span></span>



| <span data-ttu-id="6cdc7-179">Entrée</span><span class="sxs-lookup"><span data-stu-id="6cdc7-179">Entry</span></span> | <span data-ttu-id="6cdc7-180">Valeur</span><span class="sxs-lookup"><span data-stu-id="6cdc7-180">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cdc7-181">ID de lien</span><span class="sxs-lookup"><span data-stu-id="6cdc7-181">Link-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="6cdc7-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6cdc7-182">MAPI-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="6cdc7-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="6cdc7-183">System-Only</span></span>            | <span data-ttu-id="6cdc7-184">Faux</span><span class="sxs-lookup"><span data-stu-id="6cdc7-184">False</span></span>                                                                                                                              |
| <span data-ttu-id="6cdc7-185">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="6cdc7-185">Is-Single-Valued</span></span>       | <span data-ttu-id="6cdc7-186">Vrai</span><span class="sxs-lookup"><span data-stu-id="6cdc7-186">True</span></span>                                                                                                                               |
| <span data-ttu-id="6cdc7-187">Est indexé</span><span class="sxs-lookup"><span data-stu-id="6cdc7-187">Is Indexed</span></span>             | <span data-ttu-id="6cdc7-188">Faux</span><span class="sxs-lookup"><span data-stu-id="6cdc7-188">False</span></span>                                                                                                                              |
| <span data-ttu-id="6cdc7-189">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="6cdc7-189">In Global Catalog</span></span>      | <span data-ttu-id="6cdc7-190">Faux</span><span class="sxs-lookup"><span data-stu-id="6cdc7-190">False</span></span>                                                                                                                              |
| <span data-ttu-id="6cdc7-191">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="6cdc7-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="6cdc7-192">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="6cdc7-192">O:BAG:BAD:S:</span></span>                                                                                                                       |
| <span data-ttu-id="6cdc7-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6cdc7-193">Range-Lower</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="6cdc7-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6cdc7-194">Range-Upper</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="6cdc7-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6cdc7-195">Search-Flags</span></span>           | <span data-ttu-id="6cdc7-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6cdc7-196">0x00000000</span></span>                                                                                                                         |
| <span data-ttu-id="6cdc7-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6cdc7-197">System-Flags</span></span>           | <span data-ttu-id="6cdc7-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6cdc7-198">0x00000010</span></span>                                                                                                                         |
| <span data-ttu-id="6cdc7-199">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="6cdc7-199">Classes used in</span></span>        | [<span data-ttu-id="6cdc7-200">**ms-DS-AZ-admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="6cdc7-200">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> [<span data-ttu-id="6cdc7-201">**ms-DS-AZ-application**</span><span class="sxs-lookup"><span data-stu-id="6cdc7-201">**ms-DS-Az-Application**</span></span>](c-msds-azapplication.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6cdc7-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6cdc7-202">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6cdc7-203">Entrée</span><span class="sxs-lookup"><span data-stu-id="6cdc7-203">Entry</span></span> | <span data-ttu-id="6cdc7-204">Valeur</span><span class="sxs-lookup"><span data-stu-id="6cdc7-204">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cdc7-205">ID de lien</span><span class="sxs-lookup"><span data-stu-id="6cdc7-205">Link-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="6cdc7-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6cdc7-206">MAPI-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="6cdc7-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="6cdc7-207">System-Only</span></span>            | <span data-ttu-id="6cdc7-208">Faux</span><span class="sxs-lookup"><span data-stu-id="6cdc7-208">False</span></span>                                                                                                                              |
| <span data-ttu-id="6cdc7-209">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="6cdc7-209">Is-Single-Valued</span></span>       | <span data-ttu-id="6cdc7-210">Vrai</span><span class="sxs-lookup"><span data-stu-id="6cdc7-210">True</span></span>                                                                                                                               |
| <span data-ttu-id="6cdc7-211">Est indexé</span><span class="sxs-lookup"><span data-stu-id="6cdc7-211">Is Indexed</span></span>             | <span data-ttu-id="6cdc7-212">Faux</span><span class="sxs-lookup"><span data-stu-id="6cdc7-212">False</span></span>                                                                                                                              |
| <span data-ttu-id="6cdc7-213">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="6cdc7-213">In Global Catalog</span></span>      | <span data-ttu-id="6cdc7-214">Faux</span><span class="sxs-lookup"><span data-stu-id="6cdc7-214">False</span></span>                                                                                                                              |
| <span data-ttu-id="6cdc7-215">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="6cdc7-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="6cdc7-216">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="6cdc7-216">O:BAG:BAD:S:</span></span>                                                                                                                       |
| <span data-ttu-id="6cdc7-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6cdc7-217">Range-Lower</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="6cdc7-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6cdc7-218">Range-Upper</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="6cdc7-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6cdc7-219">Search-Flags</span></span>           | <span data-ttu-id="6cdc7-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6cdc7-220">0x00000000</span></span>                                                                                                                         |
| <span data-ttu-id="6cdc7-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6cdc7-221">System-Flags</span></span>           | <span data-ttu-id="6cdc7-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6cdc7-222">0x00000010</span></span>                                                                                                                         |
| <span data-ttu-id="6cdc7-223">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="6cdc7-223">Classes used in</span></span>        | [<span data-ttu-id="6cdc7-224">**ms-DS-AZ-admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="6cdc7-224">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> [<span data-ttu-id="6cdc7-225">**ms-DS-AZ-application**</span><span class="sxs-lookup"><span data-stu-id="6cdc7-225">**ms-DS-Az-Application**</span></span>](c-msds-azapplication.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6cdc7-226">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6cdc7-226">Windows Server 2012</span></span>



| <span data-ttu-id="6cdc7-227">Entrée</span><span class="sxs-lookup"><span data-stu-id="6cdc7-227">Entry</span></span> | <span data-ttu-id="6cdc7-228">Valeur</span><span class="sxs-lookup"><span data-stu-id="6cdc7-228">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cdc7-229">ID de lien</span><span class="sxs-lookup"><span data-stu-id="6cdc7-229">Link-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="6cdc7-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6cdc7-230">MAPI-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="6cdc7-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="6cdc7-231">System-Only</span></span>            | <span data-ttu-id="6cdc7-232">Faux</span><span class="sxs-lookup"><span data-stu-id="6cdc7-232">False</span></span>                                                                                                                              |
| <span data-ttu-id="6cdc7-233">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="6cdc7-233">Is-Single-Valued</span></span>       | <span data-ttu-id="6cdc7-234">Vrai</span><span class="sxs-lookup"><span data-stu-id="6cdc7-234">True</span></span>                                                                                                                               |
| <span data-ttu-id="6cdc7-235">Est indexé</span><span class="sxs-lookup"><span data-stu-id="6cdc7-235">Is Indexed</span></span>             | <span data-ttu-id="6cdc7-236">Faux</span><span class="sxs-lookup"><span data-stu-id="6cdc7-236">False</span></span>                                                                                                                              |
| <span data-ttu-id="6cdc7-237">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="6cdc7-237">In Global Catalog</span></span>      | <span data-ttu-id="6cdc7-238">Faux</span><span class="sxs-lookup"><span data-stu-id="6cdc7-238">False</span></span>                                                                                                                              |
| <span data-ttu-id="6cdc7-239">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="6cdc7-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="6cdc7-240">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="6cdc7-240">O:BAG:BAD:S:</span></span>                                                                                                                       |
| <span data-ttu-id="6cdc7-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6cdc7-241">Range-Lower</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="6cdc7-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6cdc7-242">Range-Upper</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="6cdc7-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6cdc7-243">Search-Flags</span></span>           | <span data-ttu-id="6cdc7-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6cdc7-244">0x00000000</span></span>                                                                                                                         |
| <span data-ttu-id="6cdc7-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6cdc7-245">System-Flags</span></span>           | <span data-ttu-id="6cdc7-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6cdc7-246">0x00000010</span></span>                                                                                                                         |
| <span data-ttu-id="6cdc7-247">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="6cdc7-247">Classes used in</span></span>        | [<span data-ttu-id="6cdc7-248">**ms-DS-AZ-admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="6cdc7-248">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> [<span data-ttu-id="6cdc7-249">**ms-DS-AZ-application**</span><span class="sxs-lookup"><span data-stu-id="6cdc7-249">**ms-DS-Az-Application**</span></span>](c-msds-azapplication.md)<br/> |



 

 





