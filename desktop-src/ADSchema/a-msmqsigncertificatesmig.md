---
title: MSMQ-Sign-Certificates-attribut MIG
description: En mode mixte MSMQ, l’attribut contient la valeur précédente de mSMQSignCertificates. MSMQ prend en charge la migration à partir du service d’annuaire MSMQ 1,0 vers le DS Windows 2000, et le mode mixte spécifie un État dans lequel certains serveurs d’annuaire n’ont pas été mis à niveau vers Windows 2000.
ms.assetid: 0dbc5d97-39e6-4863-a386-541ea2abaadc
ms.tgt_platform: multiple
keywords:
- MSMQ-Sign-Certificates-schéma AD d’attribut MIG
- Schéma AD de l’attribut mSMQSignCertificatesMig
topic_type:
- apiref
api_name:
- MSMQ-Sign-Certificates-Mig
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91a1916cf98d15da1bd84603a2305543e899d868
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106515289"
---
# <a name="msmq-sign-certificates-mig-attribute"></a><span data-ttu-id="ae8fc-106">MSMQ-Sign-Certificates-attribut MIG</span><span class="sxs-lookup"><span data-stu-id="ae8fc-106">MSMQ-Sign-Certificates-Mig attribute</span></span>

<span data-ttu-id="ae8fc-107">En mode mixte MSMQ, l’attribut contient la valeur précédente de mSMQSignCertificates.</span><span class="sxs-lookup"><span data-stu-id="ae8fc-107">In MSMQ mixed-mode, the attribute contains the previous value of mSMQSignCertificates.</span></span> <span data-ttu-id="ae8fc-108">MSMQ prend en charge la migration à partir du service d’annuaire MSMQ 1,0 vers le DS Windows 2000, et le mode mixte spécifie un État dans lequel certains serveurs d’annuaire n’ont pas été mis à niveau vers Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="ae8fc-108">MSMQ supports migration from the MSMQ 1.0 DS to the Windows 2000 DS, and mixed mode specifies a state in which some of the DS severs were not upgraded to Windows 2000.</span></span>



| <span data-ttu-id="ae8fc-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="ae8fc-109">Entry</span></span> | <span data-ttu-id="ae8fc-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="ae8fc-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="ae8fc-111">CN</span><span class="sxs-lookup"><span data-stu-id="ae8fc-111">CN</span></span>                | <span data-ttu-id="ae8fc-112">MSMQ-Sign-Certificates-MIG</span><span class="sxs-lookup"><span data-stu-id="ae8fc-112">MSMQ-Sign-Certificates-Mig</span></span>                            |
| <span data-ttu-id="ae8fc-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="ae8fc-113">Ldap-Display-Name</span></span> | <span data-ttu-id="ae8fc-114">mSMQSignCertificatesMig</span><span class="sxs-lookup"><span data-stu-id="ae8fc-114">mSMQSignCertificatesMig</span></span>                               |
| <span data-ttu-id="ae8fc-115">Taille</span><span class="sxs-lookup"><span data-stu-id="ae8fc-115">Size</span></span>              | \-                                                    |
| <span data-ttu-id="ae8fc-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="ae8fc-116">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="ae8fc-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="ae8fc-117">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="ae8fc-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ae8fc-118">Attribute-Id</span></span>      | <span data-ttu-id="ae8fc-119">1.2.840.113556.1.4.967</span><span class="sxs-lookup"><span data-stu-id="ae8fc-119">1.2.840.113556.1.4.967</span></span>                                |
| <span data-ttu-id="ae8fc-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ae8fc-120">System-Id-Guid</span></span>    | <span data-ttu-id="ae8fc-121">3881b8ea-da3b-11d1-90a5-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="ae8fc-121">3881b8ea-da3b-11d1-90a5-00c04fd91ab1</span></span>                  |
| <span data-ttu-id="ae8fc-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ae8fc-122">Syntax</span></span>            | [<span data-ttu-id="ae8fc-123">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="ae8fc-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="ae8fc-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="ae8fc-124">Implementations</span></span>

-   [<span data-ttu-id="ae8fc-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ae8fc-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ae8fc-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ae8fc-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ae8fc-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ae8fc-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ae8fc-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ae8fc-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ae8fc-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ae8fc-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ae8fc-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ae8fc-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ae8fc-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ae8fc-131">Windows 2000 Server</span></span>



| <span data-ttu-id="ae8fc-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="ae8fc-132">Entry</span></span> | <span data-ttu-id="ae8fc-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="ae8fc-133">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae8fc-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ae8fc-134">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="ae8fc-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ae8fc-135">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="ae8fc-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="ae8fc-136">System-Only</span></span>            | <span data-ttu-id="ae8fc-137">Faux</span><span class="sxs-lookup"><span data-stu-id="ae8fc-137">False</span></span>                                                                                         |
| <span data-ttu-id="ae8fc-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ae8fc-138">Is-Single-Valued</span></span>       | <span data-ttu-id="ae8fc-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="ae8fc-139">True</span></span>                                                                                          |
| <span data-ttu-id="ae8fc-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ae8fc-140">Is Indexed</span></span>             | <span data-ttu-id="ae8fc-141">Faux</span><span class="sxs-lookup"><span data-stu-id="ae8fc-141">False</span></span>                                                                                         |
| <span data-ttu-id="ae8fc-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ae8fc-142">In Global Catalog</span></span>      | <span data-ttu-id="ae8fc-143">Vrai</span><span class="sxs-lookup"><span data-stu-id="ae8fc-143">True</span></span>                                                                                          |
| <span data-ttu-id="ae8fc-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ae8fc-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="ae8fc-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ae8fc-145">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="ae8fc-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ae8fc-146">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="ae8fc-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ae8fc-147">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="ae8fc-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ae8fc-148">Search-Flags</span></span>           | <span data-ttu-id="ae8fc-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ae8fc-149">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="ae8fc-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ae8fc-150">System-Flags</span></span>           | <span data-ttu-id="ae8fc-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ae8fc-151">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="ae8fc-152">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ae8fc-152">Classes used in</span></span>        | [<span data-ttu-id="ae8fc-153">**MSMQ-migrated-User**</span><span class="sxs-lookup"><span data-stu-id="ae8fc-153">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="ae8fc-154">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="ae8fc-154">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ae8fc-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ae8fc-155">Windows Server 2003</span></span>



| <span data-ttu-id="ae8fc-156">Entrée</span><span class="sxs-lookup"><span data-stu-id="ae8fc-156">Entry</span></span> | <span data-ttu-id="ae8fc-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="ae8fc-157">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae8fc-158">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ae8fc-158">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="ae8fc-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ae8fc-159">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="ae8fc-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="ae8fc-160">System-Only</span></span>            | <span data-ttu-id="ae8fc-161">Faux</span><span class="sxs-lookup"><span data-stu-id="ae8fc-161">False</span></span>                                                                                         |
| <span data-ttu-id="ae8fc-162">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ae8fc-162">Is-Single-Valued</span></span>       | <span data-ttu-id="ae8fc-163">Vrai</span><span class="sxs-lookup"><span data-stu-id="ae8fc-163">True</span></span>                                                                                          |
| <span data-ttu-id="ae8fc-164">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ae8fc-164">Is Indexed</span></span>             | <span data-ttu-id="ae8fc-165">Faux</span><span class="sxs-lookup"><span data-stu-id="ae8fc-165">False</span></span>                                                                                         |
| <span data-ttu-id="ae8fc-166">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ae8fc-166">In Global Catalog</span></span>      | <span data-ttu-id="ae8fc-167">Vrai</span><span class="sxs-lookup"><span data-stu-id="ae8fc-167">True</span></span>                                                                                          |
| <span data-ttu-id="ae8fc-168">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ae8fc-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="ae8fc-169">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ae8fc-169">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="ae8fc-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ae8fc-170">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="ae8fc-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ae8fc-171">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="ae8fc-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ae8fc-172">Search-Flags</span></span>           | <span data-ttu-id="ae8fc-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ae8fc-173">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="ae8fc-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ae8fc-174">System-Flags</span></span>           | <span data-ttu-id="ae8fc-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ae8fc-175">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="ae8fc-176">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ae8fc-176">Classes used in</span></span>        | [<span data-ttu-id="ae8fc-177">**MSMQ-migrated-User**</span><span class="sxs-lookup"><span data-stu-id="ae8fc-177">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="ae8fc-178">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="ae8fc-178">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ae8fc-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ae8fc-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ae8fc-180">Entrée</span><span class="sxs-lookup"><span data-stu-id="ae8fc-180">Entry</span></span> | <span data-ttu-id="ae8fc-181">Valeur</span><span class="sxs-lookup"><span data-stu-id="ae8fc-181">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae8fc-182">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ae8fc-182">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="ae8fc-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ae8fc-183">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="ae8fc-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="ae8fc-184">System-Only</span></span>            | <span data-ttu-id="ae8fc-185">Faux</span><span class="sxs-lookup"><span data-stu-id="ae8fc-185">False</span></span>                                                                                         |
| <span data-ttu-id="ae8fc-186">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ae8fc-186">Is-Single-Valued</span></span>       | <span data-ttu-id="ae8fc-187">Vrai</span><span class="sxs-lookup"><span data-stu-id="ae8fc-187">True</span></span>                                                                                          |
| <span data-ttu-id="ae8fc-188">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ae8fc-188">Is Indexed</span></span>             | <span data-ttu-id="ae8fc-189">Faux</span><span class="sxs-lookup"><span data-stu-id="ae8fc-189">False</span></span>                                                                                         |
| <span data-ttu-id="ae8fc-190">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ae8fc-190">In Global Catalog</span></span>      | <span data-ttu-id="ae8fc-191">Vrai</span><span class="sxs-lookup"><span data-stu-id="ae8fc-191">True</span></span>                                                                                          |
| <span data-ttu-id="ae8fc-192">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ae8fc-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="ae8fc-193">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ae8fc-193">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="ae8fc-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ae8fc-194">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="ae8fc-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ae8fc-195">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="ae8fc-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ae8fc-196">Search-Flags</span></span>           | <span data-ttu-id="ae8fc-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ae8fc-197">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="ae8fc-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ae8fc-198">System-Flags</span></span>           | <span data-ttu-id="ae8fc-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ae8fc-199">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="ae8fc-200">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ae8fc-200">Classes used in</span></span>        | [<span data-ttu-id="ae8fc-201">**MSMQ-migrated-User**</span><span class="sxs-lookup"><span data-stu-id="ae8fc-201">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="ae8fc-202">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="ae8fc-202">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ae8fc-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ae8fc-203">Windows Server 2008</span></span>



| <span data-ttu-id="ae8fc-204">Entrée</span><span class="sxs-lookup"><span data-stu-id="ae8fc-204">Entry</span></span> | <span data-ttu-id="ae8fc-205">Valeur</span><span class="sxs-lookup"><span data-stu-id="ae8fc-205">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae8fc-206">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ae8fc-206">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="ae8fc-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ae8fc-207">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="ae8fc-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="ae8fc-208">System-Only</span></span>            | <span data-ttu-id="ae8fc-209">Faux</span><span class="sxs-lookup"><span data-stu-id="ae8fc-209">False</span></span>                                                                                         |
| <span data-ttu-id="ae8fc-210">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ae8fc-210">Is-Single-Valued</span></span>       | <span data-ttu-id="ae8fc-211">Vrai</span><span class="sxs-lookup"><span data-stu-id="ae8fc-211">True</span></span>                                                                                          |
| <span data-ttu-id="ae8fc-212">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ae8fc-212">Is Indexed</span></span>             | <span data-ttu-id="ae8fc-213">Faux</span><span class="sxs-lookup"><span data-stu-id="ae8fc-213">False</span></span>                                                                                         |
| <span data-ttu-id="ae8fc-214">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ae8fc-214">In Global Catalog</span></span>      | <span data-ttu-id="ae8fc-215">Vrai</span><span class="sxs-lookup"><span data-stu-id="ae8fc-215">True</span></span>                                                                                          |
| <span data-ttu-id="ae8fc-216">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ae8fc-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="ae8fc-217">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ae8fc-217">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="ae8fc-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ae8fc-218">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="ae8fc-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ae8fc-219">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="ae8fc-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ae8fc-220">Search-Flags</span></span>           | <span data-ttu-id="ae8fc-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ae8fc-221">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="ae8fc-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ae8fc-222">System-Flags</span></span>           | <span data-ttu-id="ae8fc-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ae8fc-223">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="ae8fc-224">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ae8fc-224">Classes used in</span></span>        | [<span data-ttu-id="ae8fc-225">**MSMQ-migrated-User**</span><span class="sxs-lookup"><span data-stu-id="ae8fc-225">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="ae8fc-226">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="ae8fc-226">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ae8fc-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ae8fc-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ae8fc-228">Entrée</span><span class="sxs-lookup"><span data-stu-id="ae8fc-228">Entry</span></span> | <span data-ttu-id="ae8fc-229">Valeur</span><span class="sxs-lookup"><span data-stu-id="ae8fc-229">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae8fc-230">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ae8fc-230">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="ae8fc-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ae8fc-231">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="ae8fc-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="ae8fc-232">System-Only</span></span>            | <span data-ttu-id="ae8fc-233">Faux</span><span class="sxs-lookup"><span data-stu-id="ae8fc-233">False</span></span>                                                                                         |
| <span data-ttu-id="ae8fc-234">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ae8fc-234">Is-Single-Valued</span></span>       | <span data-ttu-id="ae8fc-235">Vrai</span><span class="sxs-lookup"><span data-stu-id="ae8fc-235">True</span></span>                                                                                          |
| <span data-ttu-id="ae8fc-236">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ae8fc-236">Is Indexed</span></span>             | <span data-ttu-id="ae8fc-237">Faux</span><span class="sxs-lookup"><span data-stu-id="ae8fc-237">False</span></span>                                                                                         |
| <span data-ttu-id="ae8fc-238">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ae8fc-238">In Global Catalog</span></span>      | <span data-ttu-id="ae8fc-239">Vrai</span><span class="sxs-lookup"><span data-stu-id="ae8fc-239">True</span></span>                                                                                          |
| <span data-ttu-id="ae8fc-240">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ae8fc-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="ae8fc-241">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ae8fc-241">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="ae8fc-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ae8fc-242">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="ae8fc-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ae8fc-243">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="ae8fc-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ae8fc-244">Search-Flags</span></span>           | <span data-ttu-id="ae8fc-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ae8fc-245">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="ae8fc-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ae8fc-246">System-Flags</span></span>           | <span data-ttu-id="ae8fc-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ae8fc-247">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="ae8fc-248">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ae8fc-248">Classes used in</span></span>        | [<span data-ttu-id="ae8fc-249">**MSMQ-migrated-User**</span><span class="sxs-lookup"><span data-stu-id="ae8fc-249">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="ae8fc-250">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="ae8fc-250">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ae8fc-251">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ae8fc-251">Windows Server 2012</span></span>



| <span data-ttu-id="ae8fc-252">Entrée</span><span class="sxs-lookup"><span data-stu-id="ae8fc-252">Entry</span></span> | <span data-ttu-id="ae8fc-253">Valeur</span><span class="sxs-lookup"><span data-stu-id="ae8fc-253">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae8fc-254">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ae8fc-254">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="ae8fc-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ae8fc-255">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="ae8fc-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="ae8fc-256">System-Only</span></span>            | <span data-ttu-id="ae8fc-257">Faux</span><span class="sxs-lookup"><span data-stu-id="ae8fc-257">False</span></span>                                                                                         |
| <span data-ttu-id="ae8fc-258">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ae8fc-258">Is-Single-Valued</span></span>       | <span data-ttu-id="ae8fc-259">Vrai</span><span class="sxs-lookup"><span data-stu-id="ae8fc-259">True</span></span>                                                                                          |
| <span data-ttu-id="ae8fc-260">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ae8fc-260">Is Indexed</span></span>             | <span data-ttu-id="ae8fc-261">Faux</span><span class="sxs-lookup"><span data-stu-id="ae8fc-261">False</span></span>                                                                                         |
| <span data-ttu-id="ae8fc-262">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ae8fc-262">In Global Catalog</span></span>      | <span data-ttu-id="ae8fc-263">Vrai</span><span class="sxs-lookup"><span data-stu-id="ae8fc-263">True</span></span>                                                                                          |
| <span data-ttu-id="ae8fc-264">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ae8fc-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="ae8fc-265">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ae8fc-265">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="ae8fc-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ae8fc-266">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="ae8fc-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ae8fc-267">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="ae8fc-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ae8fc-268">Search-Flags</span></span>           | <span data-ttu-id="ae8fc-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ae8fc-269">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="ae8fc-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ae8fc-270">System-Flags</span></span>           | <span data-ttu-id="ae8fc-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ae8fc-271">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="ae8fc-272">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ae8fc-272">Classes used in</span></span>        | [<span data-ttu-id="ae8fc-273">**MSMQ-migrated-User**</span><span class="sxs-lookup"><span data-stu-id="ae8fc-273">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="ae8fc-274">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="ae8fc-274">**User**</span></span>](c-user.md)<br/> |



 

 





