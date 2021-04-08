---
title: Attribut Last-Backup-Restoring-Time
description: Lorsque la dernière restauration du système s’est produite.
ms.assetid: 44850c16-3f17-4883-9a54-3e82ca7d63da
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut Last-Backup-Restoring-Time
- Schéma AD de l’attribut lastBackupRestorationTime
topic_type:
- apiref
api_name:
- Last-Backup-Restoration-Time
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9220d06a4cdd562599611d2ad19cf09fa279ef3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104033288"
---
# <a name="last-backup-restoration-time-attribute"></a><span data-ttu-id="f9a52-105">Attribut Last-Backup-Restoring-Time</span><span class="sxs-lookup"><span data-stu-id="f9a52-105">Last-Backup-Restoration-Time attribute</span></span>

<span data-ttu-id="f9a52-106">Lorsque la dernière restauration du système s’est produite.</span><span class="sxs-lookup"><span data-stu-id="f9a52-106">When the last system restore occurred.</span></span>



| <span data-ttu-id="f9a52-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="f9a52-107">Entry</span></span> | <span data-ttu-id="f9a52-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="f9a52-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="f9a52-109">CN</span><span class="sxs-lookup"><span data-stu-id="f9a52-109">CN</span></span>                | <span data-ttu-id="f9a52-110">Dernière-sauvegarde-restauration-heure</span><span class="sxs-lookup"><span data-stu-id="f9a52-110">Last-Backup-Restoration-Time</span></span>         |
| <span data-ttu-id="f9a52-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-111">Ldap-Display-Name</span></span> | <span data-ttu-id="f9a52-112">lastBackupRestorationTime</span><span class="sxs-lookup"><span data-stu-id="f9a52-112">lastBackupRestorationTime</span></span>            |
| <span data-ttu-id="f9a52-113">Taille</span><span class="sxs-lookup"><span data-stu-id="f9a52-113">Size</span></span>              | <span data-ttu-id="f9a52-114">8 octets</span><span class="sxs-lookup"><span data-stu-id="f9a52-114">8 bytes</span></span>                              |
| <span data-ttu-id="f9a52-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="f9a52-115">Update Privilege</span></span>  | <span data-ttu-id="f9a52-116">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="f9a52-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="f9a52-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="f9a52-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="f9a52-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f9a52-118">Attribute-Id</span></span>      | <span data-ttu-id="f9a52-119">1.2.840.113556.1.4.519</span><span class="sxs-lookup"><span data-stu-id="f9a52-119">1.2.840.113556.1.4.519</span></span>               |
| <span data-ttu-id="f9a52-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-120">System-Id-Guid</span></span>    | <span data-ttu-id="f9a52-121">1fbb0be8-ba63-11d0-afef-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="f9a52-121">1fbb0be8-ba63-11d0-afef-0000f80367c1</span></span> |
| <span data-ttu-id="f9a52-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f9a52-122">Syntax</span></span>            | [<span data-ttu-id="f9a52-123">**Défini**</span><span class="sxs-lookup"><span data-stu-id="f9a52-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="f9a52-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="f9a52-124">Implementations</span></span>

-   [<span data-ttu-id="f9a52-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f9a52-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f9a52-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f9a52-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f9a52-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="f9a52-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="f9a52-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f9a52-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f9a52-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f9a52-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f9a52-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f9a52-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f9a52-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f9a52-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f9a52-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f9a52-132">Windows 2000 Server</span></span>



| <span data-ttu-id="f9a52-133">Entrée</span><span class="sxs-lookup"><span data-stu-id="f9a52-133">Entry</span></span> | <span data-ttu-id="f9a52-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="f9a52-134">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="f9a52-135">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f9a52-135">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="f9a52-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f9a52-136">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="f9a52-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="f9a52-137">System-Only</span></span>            | <span data-ttu-id="f9a52-138">Faux</span><span class="sxs-lookup"><span data-stu-id="f9a52-138">False</span></span>                                    |
| <span data-ttu-id="f9a52-139">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f9a52-139">Is-Single-Valued</span></span>       | <span data-ttu-id="f9a52-140">Vrai</span><span class="sxs-lookup"><span data-stu-id="f9a52-140">True</span></span>                                     |
| <span data-ttu-id="f9a52-141">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f9a52-141">Is Indexed</span></span>             | <span data-ttu-id="f9a52-142">Faux</span><span class="sxs-lookup"><span data-stu-id="f9a52-142">False</span></span>                                    |
| <span data-ttu-id="f9a52-143">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f9a52-143">In Global Catalog</span></span>      | <span data-ttu-id="f9a52-144">Faux</span><span class="sxs-lookup"><span data-stu-id="f9a52-144">False</span></span>                                    |
| <span data-ttu-id="f9a52-145">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f9a52-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="f9a52-146">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f9a52-146">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="f9a52-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f9a52-147">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="f9a52-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f9a52-148">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="f9a52-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f9a52-149">Search-Flags</span></span>           | <span data-ttu-id="f9a52-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f9a52-150">0x00000000</span></span>                               |
| <span data-ttu-id="f9a52-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f9a52-151">System-Flags</span></span>           | <span data-ttu-id="f9a52-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f9a52-152">0x00000010</span></span>                               |
| <span data-ttu-id="f9a52-153">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f9a52-153">Classes used in</span></span>        | [<span data-ttu-id="f9a52-154">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="f9a52-154">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f9a52-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f9a52-155">Windows Server 2003</span></span>



| <span data-ttu-id="f9a52-156">Entrée</span><span class="sxs-lookup"><span data-stu-id="f9a52-156">Entry</span></span> | <span data-ttu-id="f9a52-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="f9a52-157">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="f9a52-158">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f9a52-158">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="f9a52-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f9a52-159">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="f9a52-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="f9a52-160">System-Only</span></span>            | <span data-ttu-id="f9a52-161">Faux</span><span class="sxs-lookup"><span data-stu-id="f9a52-161">False</span></span>                                    |
| <span data-ttu-id="f9a52-162">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f9a52-162">Is-Single-Valued</span></span>       | <span data-ttu-id="f9a52-163">Vrai</span><span class="sxs-lookup"><span data-stu-id="f9a52-163">True</span></span>                                     |
| <span data-ttu-id="f9a52-164">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f9a52-164">Is Indexed</span></span>             | <span data-ttu-id="f9a52-165">Faux</span><span class="sxs-lookup"><span data-stu-id="f9a52-165">False</span></span>                                    |
| <span data-ttu-id="f9a52-166">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f9a52-166">In Global Catalog</span></span>      | <span data-ttu-id="f9a52-167">Faux</span><span class="sxs-lookup"><span data-stu-id="f9a52-167">False</span></span>                                    |
| <span data-ttu-id="f9a52-168">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f9a52-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="f9a52-169">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f9a52-169">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="f9a52-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f9a52-170">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="f9a52-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f9a52-171">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="f9a52-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f9a52-172">Search-Flags</span></span>           | <span data-ttu-id="f9a52-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f9a52-173">0x00000000</span></span>                               |
| <span data-ttu-id="f9a52-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f9a52-174">System-Flags</span></span>           | <span data-ttu-id="f9a52-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f9a52-175">0x00000010</span></span>                               |
| <span data-ttu-id="f9a52-176">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f9a52-176">Classes used in</span></span>        | [<span data-ttu-id="f9a52-177">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="f9a52-177">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="adam"></a><span data-ttu-id="f9a52-178">ADAM</span><span class="sxs-lookup"><span data-stu-id="f9a52-178">ADAM</span></span>



| <span data-ttu-id="f9a52-179">Entrée</span><span class="sxs-lookup"><span data-stu-id="f9a52-179">Entry</span></span> | <span data-ttu-id="f9a52-180">Valeur</span><span class="sxs-lookup"><span data-stu-id="f9a52-180">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="f9a52-181">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f9a52-181">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="f9a52-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f9a52-182">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="f9a52-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="f9a52-183">System-Only</span></span>            | <span data-ttu-id="f9a52-184">Faux</span><span class="sxs-lookup"><span data-stu-id="f9a52-184">False</span></span>                                    |
| <span data-ttu-id="f9a52-185">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f9a52-185">Is-Single-Valued</span></span>       | <span data-ttu-id="f9a52-186">Vrai</span><span class="sxs-lookup"><span data-stu-id="f9a52-186">True</span></span>                                     |
| <span data-ttu-id="f9a52-187">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f9a52-187">Is Indexed</span></span>             | <span data-ttu-id="f9a52-188">Faux</span><span class="sxs-lookup"><span data-stu-id="f9a52-188">False</span></span>                                    |
| <span data-ttu-id="f9a52-189">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f9a52-189">In Global Catalog</span></span>      | <span data-ttu-id="f9a52-190">Faux</span><span class="sxs-lookup"><span data-stu-id="f9a52-190">False</span></span>                                    |
| <span data-ttu-id="f9a52-191">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f9a52-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="f9a52-192">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f9a52-192">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="f9a52-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f9a52-193">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="f9a52-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f9a52-194">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="f9a52-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f9a52-195">Search-Flags</span></span>           | <span data-ttu-id="f9a52-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f9a52-196">0x00000000</span></span>                               |
| <span data-ttu-id="f9a52-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f9a52-197">System-Flags</span></span>           | <span data-ttu-id="f9a52-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f9a52-198">0x00000010</span></span>                               |
| <span data-ttu-id="f9a52-199">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f9a52-199">Classes used in</span></span>        | [<span data-ttu-id="f9a52-200">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="f9a52-200">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f9a52-201">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f9a52-201">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f9a52-202">Entrée</span><span class="sxs-lookup"><span data-stu-id="f9a52-202">Entry</span></span> | <span data-ttu-id="f9a52-203">Valeur</span><span class="sxs-lookup"><span data-stu-id="f9a52-203">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="f9a52-204">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f9a52-204">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="f9a52-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f9a52-205">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="f9a52-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="f9a52-206">System-Only</span></span>            | <span data-ttu-id="f9a52-207">Faux</span><span class="sxs-lookup"><span data-stu-id="f9a52-207">False</span></span>                                    |
| <span data-ttu-id="f9a52-208">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f9a52-208">Is-Single-Valued</span></span>       | <span data-ttu-id="f9a52-209">Vrai</span><span class="sxs-lookup"><span data-stu-id="f9a52-209">True</span></span>                                     |
| <span data-ttu-id="f9a52-210">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f9a52-210">Is Indexed</span></span>             | <span data-ttu-id="f9a52-211">Faux</span><span class="sxs-lookup"><span data-stu-id="f9a52-211">False</span></span>                                    |
| <span data-ttu-id="f9a52-212">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f9a52-212">In Global Catalog</span></span>      | <span data-ttu-id="f9a52-213">Faux</span><span class="sxs-lookup"><span data-stu-id="f9a52-213">False</span></span>                                    |
| <span data-ttu-id="f9a52-214">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f9a52-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="f9a52-215">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f9a52-215">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="f9a52-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f9a52-216">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="f9a52-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f9a52-217">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="f9a52-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f9a52-218">Search-Flags</span></span>           | <span data-ttu-id="f9a52-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f9a52-219">0x00000000</span></span>                               |
| <span data-ttu-id="f9a52-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f9a52-220">System-Flags</span></span>           | <span data-ttu-id="f9a52-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f9a52-221">0x00000010</span></span>                               |
| <span data-ttu-id="f9a52-222">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f9a52-222">Classes used in</span></span>        | [<span data-ttu-id="f9a52-223">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="f9a52-223">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f9a52-224">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f9a52-224">Windows Server 2008</span></span>



| <span data-ttu-id="f9a52-225">Entrée</span><span class="sxs-lookup"><span data-stu-id="f9a52-225">Entry</span></span> | <span data-ttu-id="f9a52-226">Valeur</span><span class="sxs-lookup"><span data-stu-id="f9a52-226">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="f9a52-227">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f9a52-227">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="f9a52-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f9a52-228">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="f9a52-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="f9a52-229">System-Only</span></span>            | <span data-ttu-id="f9a52-230">Faux</span><span class="sxs-lookup"><span data-stu-id="f9a52-230">False</span></span>                                    |
| <span data-ttu-id="f9a52-231">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f9a52-231">Is-Single-Valued</span></span>       | <span data-ttu-id="f9a52-232">Vrai</span><span class="sxs-lookup"><span data-stu-id="f9a52-232">True</span></span>                                     |
| <span data-ttu-id="f9a52-233">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f9a52-233">Is Indexed</span></span>             | <span data-ttu-id="f9a52-234">Faux</span><span class="sxs-lookup"><span data-stu-id="f9a52-234">False</span></span>                                    |
| <span data-ttu-id="f9a52-235">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f9a52-235">In Global Catalog</span></span>      | <span data-ttu-id="f9a52-236">Faux</span><span class="sxs-lookup"><span data-stu-id="f9a52-236">False</span></span>                                    |
| <span data-ttu-id="f9a52-237">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f9a52-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="f9a52-238">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f9a52-238">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="f9a52-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f9a52-239">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="f9a52-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f9a52-240">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="f9a52-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f9a52-241">Search-Flags</span></span>           | <span data-ttu-id="f9a52-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f9a52-242">0x00000000</span></span>                               |
| <span data-ttu-id="f9a52-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f9a52-243">System-Flags</span></span>           | <span data-ttu-id="f9a52-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f9a52-244">0x00000010</span></span>                               |
| <span data-ttu-id="f9a52-245">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f9a52-245">Classes used in</span></span>        | [<span data-ttu-id="f9a52-246">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="f9a52-246">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f9a52-247">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f9a52-247">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f9a52-248">Entrée</span><span class="sxs-lookup"><span data-stu-id="f9a52-248">Entry</span></span> | <span data-ttu-id="f9a52-249">Valeur</span><span class="sxs-lookup"><span data-stu-id="f9a52-249">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="f9a52-250">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f9a52-250">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="f9a52-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f9a52-251">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="f9a52-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="f9a52-252">System-Only</span></span>            | <span data-ttu-id="f9a52-253">Faux</span><span class="sxs-lookup"><span data-stu-id="f9a52-253">False</span></span>                                    |
| <span data-ttu-id="f9a52-254">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f9a52-254">Is-Single-Valued</span></span>       | <span data-ttu-id="f9a52-255">Vrai</span><span class="sxs-lookup"><span data-stu-id="f9a52-255">True</span></span>                                     |
| <span data-ttu-id="f9a52-256">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f9a52-256">Is Indexed</span></span>             | <span data-ttu-id="f9a52-257">Faux</span><span class="sxs-lookup"><span data-stu-id="f9a52-257">False</span></span>                                    |
| <span data-ttu-id="f9a52-258">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f9a52-258">In Global Catalog</span></span>      | <span data-ttu-id="f9a52-259">Faux</span><span class="sxs-lookup"><span data-stu-id="f9a52-259">False</span></span>                                    |
| <span data-ttu-id="f9a52-260">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f9a52-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="f9a52-261">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f9a52-261">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="f9a52-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f9a52-262">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="f9a52-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f9a52-263">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="f9a52-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f9a52-264">Search-Flags</span></span>           | <span data-ttu-id="f9a52-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f9a52-265">0x00000000</span></span>                               |
| <span data-ttu-id="f9a52-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f9a52-266">System-Flags</span></span>           | <span data-ttu-id="f9a52-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f9a52-267">0x00000010</span></span>                               |
| <span data-ttu-id="f9a52-268">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f9a52-268">Classes used in</span></span>        | [<span data-ttu-id="f9a52-269">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="f9a52-269">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f9a52-270">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f9a52-270">Windows Server 2012</span></span>



| <span data-ttu-id="f9a52-271">Entrée</span><span class="sxs-lookup"><span data-stu-id="f9a52-271">Entry</span></span> | <span data-ttu-id="f9a52-272">Valeur</span><span class="sxs-lookup"><span data-stu-id="f9a52-272">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="f9a52-273">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f9a52-273">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="f9a52-274">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f9a52-274">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="f9a52-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="f9a52-275">System-Only</span></span>            | <span data-ttu-id="f9a52-276">Faux</span><span class="sxs-lookup"><span data-stu-id="f9a52-276">False</span></span>                                    |
| <span data-ttu-id="f9a52-277">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f9a52-277">Is-Single-Valued</span></span>       | <span data-ttu-id="f9a52-278">Vrai</span><span class="sxs-lookup"><span data-stu-id="f9a52-278">True</span></span>                                     |
| <span data-ttu-id="f9a52-279">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f9a52-279">Is Indexed</span></span>             | <span data-ttu-id="f9a52-280">Faux</span><span class="sxs-lookup"><span data-stu-id="f9a52-280">False</span></span>                                    |
| <span data-ttu-id="f9a52-281">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f9a52-281">In Global Catalog</span></span>      | <span data-ttu-id="f9a52-282">Faux</span><span class="sxs-lookup"><span data-stu-id="f9a52-282">False</span></span>                                    |
| <span data-ttu-id="f9a52-283">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f9a52-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="f9a52-284">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f9a52-284">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="f9a52-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f9a52-285">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="f9a52-286">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f9a52-286">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="f9a52-287">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f9a52-287">Search-Flags</span></span>           | <span data-ttu-id="f9a52-288">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f9a52-288">0x00000000</span></span>                               |
| <span data-ttu-id="f9a52-289">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f9a52-289">System-Flags</span></span>           | <span data-ttu-id="f9a52-290">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f9a52-290">0x00000010</span></span>                               |
| <span data-ttu-id="f9a52-291">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f9a52-291">Classes used in</span></span>        | [<span data-ttu-id="f9a52-292">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="f9a52-292">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





