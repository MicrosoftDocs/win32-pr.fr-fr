---
title: attribut ms-DS-Logon-Time-Sync-Interval
description: Cet attribut contrôle la granularité, en jours, à laquelle l’heure de la dernière ouverture de session d’un utilisateur ou d’un ordinateur, enregistrée dans l’attribut lastLogonTimestamp, est répliquée sur tous les contrôleurs de domaine d’un domaine.
ms.assetid: f1f9f1f8-df60-44b5-965d-631c4dd4ef84
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut ms-DS-Logon-Time-Sync-Interval
- Schéma Active Directory de l’attribut msDS-LogonTimeSyncInterval
topic_type:
- apiref
api_name:
- ms-DS-Logon-Time-Sync-Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dbf23ca77bda9dac76f02986be1c05c80559199
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104520169"
---
# <a name="ms-ds-logon-time-sync-interval-attribute"></a><span data-ttu-id="ed58b-105">attribut ms-DS-Logon-Time-Sync-Interval</span><span class="sxs-lookup"><span data-stu-id="ed58b-105">ms-DS-Logon-Time-Sync-Interval attribute</span></span>

<span data-ttu-id="ed58b-106">Cet attribut contrôle la granularité, en jours, à laquelle l’heure de la dernière ouverture de session d’un utilisateur ou d’un ordinateur, enregistrée dans l’attribut lastLogonTimestamp, est répliquée sur tous les contrôleurs de domaine d’un domaine.</span><span class="sxs-lookup"><span data-stu-id="ed58b-106">This attribute controls the granularity, in days, with which the last logon time for a user or computer, recorded in the lastLogonTimestamp attribute, is replicated to all DCs in a domain.</span></span>



| <span data-ttu-id="ed58b-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="ed58b-107">Entry</span></span> | <span data-ttu-id="ed58b-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="ed58b-108">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed58b-109">CN</span><span class="sxs-lookup"><span data-stu-id="ed58b-109">CN</span></span>                | <span data-ttu-id="ed58b-110">ms-DS-Logon-Time-Sync-Interval</span><span class="sxs-lookup"><span data-stu-id="ed58b-110">ms-DS-Logon-Time-Sync-Interval</span></span>                                                                             |
| <span data-ttu-id="ed58b-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="ed58b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="ed58b-112">msDS-LogonTimeSyncInterval</span><span class="sxs-lookup"><span data-stu-id="ed58b-112">msDS-LogonTimeSyncInterval</span></span>                                                                                 |
| <span data-ttu-id="ed58b-113">Taille</span><span class="sxs-lookup"><span data-stu-id="ed58b-113">Size</span></span>              | <span data-ttu-id="ed58b-114">4 octets</span><span class="sxs-lookup"><span data-stu-id="ed58b-114">4 bytes</span></span>                                                                                                    |
| <span data-ttu-id="ed58b-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="ed58b-115">Update Privilege</span></span>  | <span data-ttu-id="ed58b-116">Administrateur de domaine</span><span class="sxs-lookup"><span data-stu-id="ed58b-116">Domain administrator</span></span>                                                                                       |
| <span data-ttu-id="ed58b-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="ed58b-117">Update Frequency</span></span>  | <span data-ttu-id="ed58b-118">Rarement, étant donné qu’il s’agit d’un paramètre de stratégie, il est mis à jour uniquement lorsqu’une modification de la stratégie à l’ensemble du domaine est souhaitée.</span><span class="sxs-lookup"><span data-stu-id="ed58b-118">Rarely, since this is a policy setting, it is updated only when a change in domain-wide policy is desired.</span></span> |
| <span data-ttu-id="ed58b-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ed58b-119">Attribute-Id</span></span>      | <span data-ttu-id="ed58b-120">1.2.840.113556.1.4.1784</span><span class="sxs-lookup"><span data-stu-id="ed58b-120">1.2.840.113556.1.4.1784</span></span>                                                                                    |
| <span data-ttu-id="ed58b-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ed58b-121">System-Id-Guid</span></span>    | <span data-ttu-id="ed58b-122">ad7940f8-e43a-4a42-83bc-d688e59ea605</span><span class="sxs-lookup"><span data-stu-id="ed58b-122">ad7940f8-e43a-4a42-83bc-d688e59ea605</span></span>                                                                       |
| <span data-ttu-id="ed58b-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ed58b-123">Syntax</span></span>            | [<span data-ttu-id="ed58b-124">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="ed58b-124">**Enumeration**</span></span>](s-enumeration.md)                                                                       |



## <a name="implementations"></a><span data-ttu-id="ed58b-125">Implémentations</span><span class="sxs-lookup"><span data-stu-id="ed58b-125">Implementations</span></span>

-   [<span data-ttu-id="ed58b-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ed58b-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ed58b-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ed58b-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ed58b-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ed58b-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ed58b-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ed58b-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ed58b-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ed58b-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="ed58b-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ed58b-131">Windows Server 2003</span></span>



| <span data-ttu-id="ed58b-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="ed58b-132">Entry</span></span> | <span data-ttu-id="ed58b-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="ed58b-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ed58b-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ed58b-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ed58b-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ed58b-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ed58b-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="ed58b-136">System-Only</span></span>            | <span data-ttu-id="ed58b-137">Faux</span><span class="sxs-lookup"><span data-stu-id="ed58b-137">False</span></span>                                        |
| <span data-ttu-id="ed58b-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ed58b-138">Is-Single-Valued</span></span>       | <span data-ttu-id="ed58b-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="ed58b-139">True</span></span>                                         |
| <span data-ttu-id="ed58b-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ed58b-140">Is Indexed</span></span>             | <span data-ttu-id="ed58b-141">Faux</span><span class="sxs-lookup"><span data-stu-id="ed58b-141">False</span></span>                                        |
| <span data-ttu-id="ed58b-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ed58b-142">In Global Catalog</span></span>      | <span data-ttu-id="ed58b-143">Faux</span><span class="sxs-lookup"><span data-stu-id="ed58b-143">False</span></span>                                        |
| <span data-ttu-id="ed58b-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ed58b-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="ed58b-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ed58b-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ed58b-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ed58b-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ed58b-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ed58b-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ed58b-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ed58b-148">Search-Flags</span></span>           | <span data-ttu-id="ed58b-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ed58b-149">0x00000000</span></span>                                   |
| <span data-ttu-id="ed58b-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ed58b-150">System-Flags</span></span>           | <span data-ttu-id="ed58b-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ed58b-151">0x00000010</span></span>                                   |
| <span data-ttu-id="ed58b-152">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ed58b-152">Classes used in</span></span>        | [<span data-ttu-id="ed58b-153">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="ed58b-153">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ed58b-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ed58b-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ed58b-155">Entrée</span><span class="sxs-lookup"><span data-stu-id="ed58b-155">Entry</span></span> | <span data-ttu-id="ed58b-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="ed58b-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ed58b-157">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ed58b-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ed58b-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ed58b-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ed58b-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="ed58b-159">System-Only</span></span>            | <span data-ttu-id="ed58b-160">Faux</span><span class="sxs-lookup"><span data-stu-id="ed58b-160">False</span></span>                                        |
| <span data-ttu-id="ed58b-161">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ed58b-161">Is-Single-Valued</span></span>       | <span data-ttu-id="ed58b-162">Vrai</span><span class="sxs-lookup"><span data-stu-id="ed58b-162">True</span></span>                                         |
| <span data-ttu-id="ed58b-163">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ed58b-163">Is Indexed</span></span>             | <span data-ttu-id="ed58b-164">Faux</span><span class="sxs-lookup"><span data-stu-id="ed58b-164">False</span></span>                                        |
| <span data-ttu-id="ed58b-165">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ed58b-165">In Global Catalog</span></span>      | <span data-ttu-id="ed58b-166">Faux</span><span class="sxs-lookup"><span data-stu-id="ed58b-166">False</span></span>                                        |
| <span data-ttu-id="ed58b-167">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ed58b-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="ed58b-168">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ed58b-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ed58b-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ed58b-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ed58b-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ed58b-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ed58b-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ed58b-171">Search-Flags</span></span>           | <span data-ttu-id="ed58b-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ed58b-172">0x00000000</span></span>                                   |
| <span data-ttu-id="ed58b-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ed58b-173">System-Flags</span></span>           | <span data-ttu-id="ed58b-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ed58b-174">0x00000010</span></span>                                   |
| <span data-ttu-id="ed58b-175">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ed58b-175">Classes used in</span></span>        | [<span data-ttu-id="ed58b-176">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="ed58b-176">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ed58b-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ed58b-177">Windows Server 2008</span></span>



| <span data-ttu-id="ed58b-178">Entrée</span><span class="sxs-lookup"><span data-stu-id="ed58b-178">Entry</span></span> | <span data-ttu-id="ed58b-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="ed58b-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ed58b-180">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ed58b-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ed58b-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ed58b-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ed58b-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="ed58b-182">System-Only</span></span>            | <span data-ttu-id="ed58b-183">Faux</span><span class="sxs-lookup"><span data-stu-id="ed58b-183">False</span></span>                                        |
| <span data-ttu-id="ed58b-184">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ed58b-184">Is-Single-Valued</span></span>       | <span data-ttu-id="ed58b-185">Vrai</span><span class="sxs-lookup"><span data-stu-id="ed58b-185">True</span></span>                                         |
| <span data-ttu-id="ed58b-186">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ed58b-186">Is Indexed</span></span>             | <span data-ttu-id="ed58b-187">Faux</span><span class="sxs-lookup"><span data-stu-id="ed58b-187">False</span></span>                                        |
| <span data-ttu-id="ed58b-188">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ed58b-188">In Global Catalog</span></span>      | <span data-ttu-id="ed58b-189">Faux</span><span class="sxs-lookup"><span data-stu-id="ed58b-189">False</span></span>                                        |
| <span data-ttu-id="ed58b-190">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ed58b-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="ed58b-191">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ed58b-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ed58b-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ed58b-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ed58b-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ed58b-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ed58b-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ed58b-194">Search-Flags</span></span>           | <span data-ttu-id="ed58b-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ed58b-195">0x00000000</span></span>                                   |
| <span data-ttu-id="ed58b-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ed58b-196">System-Flags</span></span>           | <span data-ttu-id="ed58b-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ed58b-197">0x00000010</span></span>                                   |
| <span data-ttu-id="ed58b-198">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ed58b-198">Classes used in</span></span>        | [<span data-ttu-id="ed58b-199">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="ed58b-199">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ed58b-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ed58b-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ed58b-201">Entrée</span><span class="sxs-lookup"><span data-stu-id="ed58b-201">Entry</span></span> | <span data-ttu-id="ed58b-202">Valeur</span><span class="sxs-lookup"><span data-stu-id="ed58b-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ed58b-203">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ed58b-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ed58b-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ed58b-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ed58b-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="ed58b-205">System-Only</span></span>            | <span data-ttu-id="ed58b-206">Faux</span><span class="sxs-lookup"><span data-stu-id="ed58b-206">False</span></span>                                        |
| <span data-ttu-id="ed58b-207">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ed58b-207">Is-Single-Valued</span></span>       | <span data-ttu-id="ed58b-208">Vrai</span><span class="sxs-lookup"><span data-stu-id="ed58b-208">True</span></span>                                         |
| <span data-ttu-id="ed58b-209">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ed58b-209">Is Indexed</span></span>             | <span data-ttu-id="ed58b-210">Faux</span><span class="sxs-lookup"><span data-stu-id="ed58b-210">False</span></span>                                        |
| <span data-ttu-id="ed58b-211">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ed58b-211">In Global Catalog</span></span>      | <span data-ttu-id="ed58b-212">Faux</span><span class="sxs-lookup"><span data-stu-id="ed58b-212">False</span></span>                                        |
| <span data-ttu-id="ed58b-213">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ed58b-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="ed58b-214">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ed58b-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ed58b-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ed58b-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ed58b-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ed58b-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ed58b-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ed58b-217">Search-Flags</span></span>           | <span data-ttu-id="ed58b-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ed58b-218">0x00000000</span></span>                                   |
| <span data-ttu-id="ed58b-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ed58b-219">System-Flags</span></span>           | <span data-ttu-id="ed58b-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ed58b-220">0x00000010</span></span>                                   |
| <span data-ttu-id="ed58b-221">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ed58b-221">Classes used in</span></span>        | [<span data-ttu-id="ed58b-222">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="ed58b-222">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ed58b-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ed58b-223">Windows Server 2012</span></span>



| <span data-ttu-id="ed58b-224">Entrée</span><span class="sxs-lookup"><span data-stu-id="ed58b-224">Entry</span></span> | <span data-ttu-id="ed58b-225">Valeur</span><span class="sxs-lookup"><span data-stu-id="ed58b-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ed58b-226">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ed58b-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ed58b-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ed58b-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ed58b-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="ed58b-228">System-Only</span></span>            | <span data-ttu-id="ed58b-229">Faux</span><span class="sxs-lookup"><span data-stu-id="ed58b-229">False</span></span>                                        |
| <span data-ttu-id="ed58b-230">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ed58b-230">Is-Single-Valued</span></span>       | <span data-ttu-id="ed58b-231">Vrai</span><span class="sxs-lookup"><span data-stu-id="ed58b-231">True</span></span>                                         |
| <span data-ttu-id="ed58b-232">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ed58b-232">Is Indexed</span></span>             | <span data-ttu-id="ed58b-233">Faux</span><span class="sxs-lookup"><span data-stu-id="ed58b-233">False</span></span>                                        |
| <span data-ttu-id="ed58b-234">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ed58b-234">In Global Catalog</span></span>      | <span data-ttu-id="ed58b-235">Faux</span><span class="sxs-lookup"><span data-stu-id="ed58b-235">False</span></span>                                        |
| <span data-ttu-id="ed58b-236">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ed58b-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="ed58b-237">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ed58b-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ed58b-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ed58b-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ed58b-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ed58b-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ed58b-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ed58b-240">Search-Flags</span></span>           | <span data-ttu-id="ed58b-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ed58b-241">0x00000000</span></span>                                   |
| <span data-ttu-id="ed58b-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ed58b-242">System-Flags</span></span>           | <span data-ttu-id="ed58b-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ed58b-243">0x00000010</span></span>                                   |
| <span data-ttu-id="ed58b-244">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ed58b-244">Classes used in</span></span>        | [<span data-ttu-id="ed58b-245">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="ed58b-245">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 





