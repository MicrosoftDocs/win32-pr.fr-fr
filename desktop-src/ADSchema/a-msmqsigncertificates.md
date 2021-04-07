---
title: Attribut MSMQ-Sign-Certificates
description: Cet attribut contient un certain nombre de certificats. Un utilisateur peut générer un certificat par ordinateur. Pour chaque certificat, nous conservons également un condensé.
ms.assetid: 70e182c7-3544-43d7-b27a-6e8d03bd2d47
ms.tgt_platform: multiple
keywords:
- Schéma AD des attributs de certificats de signature MSMQ
- Schéma AD de l’attribut mSMQSignCertificates
topic_type:
- apiref
api_name:
- MSMQ-Sign-Certificates
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dd7e81cf145ac249b78e0a3e20be657df68b4af
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845081"
---
# <a name="msmq-sign-certificates-attribute"></a><span data-ttu-id="4cdea-107">Attribut MSMQ-Sign-Certificates</span><span class="sxs-lookup"><span data-stu-id="4cdea-107">MSMQ-Sign-Certificates attribute</span></span>

<span data-ttu-id="4cdea-108">Cet attribut contient un certain nombre de certificats.</span><span class="sxs-lookup"><span data-stu-id="4cdea-108">This attribute contains a number of certificates.</span></span> <span data-ttu-id="4cdea-109">Un utilisateur peut générer un certificat par ordinateur.</span><span class="sxs-lookup"><span data-stu-id="4cdea-109">A user can generate a certificate per computer.</span></span> <span data-ttu-id="4cdea-110">Pour chaque certificat, nous conservons également un condensé.</span><span class="sxs-lookup"><span data-stu-id="4cdea-110">For each certificate we also keep a digest.</span></span>



| <span data-ttu-id="4cdea-111">Entrée</span><span class="sxs-lookup"><span data-stu-id="4cdea-111">Entry</span></span> | <span data-ttu-id="4cdea-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="4cdea-112">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4cdea-113">CN</span><span class="sxs-lookup"><span data-stu-id="4cdea-113">CN</span></span>                | <span data-ttu-id="4cdea-114">Certificats de signature MSMQ</span><span class="sxs-lookup"><span data-stu-id="4cdea-114">MSMQ-Sign-Certificates</span></span>                                                                 |
| <span data-ttu-id="4cdea-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="4cdea-115">Ldap-Display-Name</span></span> | <span data-ttu-id="4cdea-116">mSMQSignCertificates</span><span class="sxs-lookup"><span data-stu-id="4cdea-116">mSMQSignCertificates</span></span>                                                                   |
| <span data-ttu-id="4cdea-117">Taille</span><span class="sxs-lookup"><span data-stu-id="4cdea-117">Size</span></span>              | <span data-ttu-id="4cdea-118">Le type d’attribut est un objet BLOB, la taille n’est pas limitée et les données sont conservées dans notre propre format.</span><span class="sxs-lookup"><span data-stu-id="4cdea-118">The attribute type is a BLOB, size is not limited, and data is kept in our own format.</span></span> |
| <span data-ttu-id="4cdea-119">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="4cdea-119">Update Privilege</span></span>  | \-                                                                                     |
| <span data-ttu-id="4cdea-120">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="4cdea-120">Update Frequency</span></span>  | \-                                                                                     |
| <span data-ttu-id="4cdea-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4cdea-121">Attribute-Id</span></span>      | <span data-ttu-id="4cdea-122">1.2.840.113556.1.4.947</span><span class="sxs-lookup"><span data-stu-id="4cdea-122">1.2.840.113556.1.4.947</span></span>                                                                 |
| <span data-ttu-id="4cdea-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="4cdea-123">System-Id-Guid</span></span>    | <span data-ttu-id="4cdea-124">9a0dc33b-c100-11d1-bbc5-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="4cdea-124">9a0dc33b-c100-11d1-bbc5-0080c76670c0</span></span>                                                   |
| <span data-ttu-id="4cdea-125">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4cdea-125">Syntax</span></span>            | [<span data-ttu-id="4cdea-126">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="4cdea-126">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                                  |



## <a name="implementations"></a><span data-ttu-id="4cdea-127">Implémentations</span><span class="sxs-lookup"><span data-stu-id="4cdea-127">Implementations</span></span>

-   [<span data-ttu-id="4cdea-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="4cdea-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="4cdea-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4cdea-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4cdea-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4cdea-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4cdea-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4cdea-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4cdea-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4cdea-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4cdea-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4cdea-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="4cdea-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4cdea-134">Windows 2000 Server</span></span>



| <span data-ttu-id="4cdea-135">Entrée</span><span class="sxs-lookup"><span data-stu-id="4cdea-135">Entry</span></span> | <span data-ttu-id="4cdea-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="4cdea-136">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cdea-137">ID de lien</span><span class="sxs-lookup"><span data-stu-id="4cdea-137">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="4cdea-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4cdea-138">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="4cdea-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="4cdea-139">System-Only</span></span>            | <span data-ttu-id="4cdea-140">Faux</span><span class="sxs-lookup"><span data-stu-id="4cdea-140">False</span></span>                                                                                         |
| <span data-ttu-id="4cdea-141">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="4cdea-141">Is-Single-Valued</span></span>       | <span data-ttu-id="4cdea-142">Vrai</span><span class="sxs-lookup"><span data-stu-id="4cdea-142">True</span></span>                                                                                          |
| <span data-ttu-id="4cdea-143">Est indexé</span><span class="sxs-lookup"><span data-stu-id="4cdea-143">Is Indexed</span></span>             | <span data-ttu-id="4cdea-144">Faux</span><span class="sxs-lookup"><span data-stu-id="4cdea-144">False</span></span>                                                                                         |
| <span data-ttu-id="4cdea-145">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="4cdea-145">In Global Catalog</span></span>      | <span data-ttu-id="4cdea-146">Vrai</span><span class="sxs-lookup"><span data-stu-id="4cdea-146">True</span></span>                                                                                          |
| <span data-ttu-id="4cdea-147">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="4cdea-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="4cdea-148">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="4cdea-148">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="4cdea-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4cdea-149">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="4cdea-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4cdea-150">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="4cdea-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4cdea-151">Search-Flags</span></span>           | <span data-ttu-id="4cdea-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4cdea-152">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="4cdea-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4cdea-153">System-Flags</span></span>           | <span data-ttu-id="4cdea-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4cdea-154">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="4cdea-155">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="4cdea-155">Classes used in</span></span>        | [<span data-ttu-id="4cdea-156">**MSMQ-migrated-User**</span><span class="sxs-lookup"><span data-stu-id="4cdea-156">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="4cdea-157">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="4cdea-157">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="4cdea-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4cdea-158">Windows Server 2003</span></span>



| <span data-ttu-id="4cdea-159">Entrée</span><span class="sxs-lookup"><span data-stu-id="4cdea-159">Entry</span></span> | <span data-ttu-id="4cdea-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="4cdea-160">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cdea-161">ID de lien</span><span class="sxs-lookup"><span data-stu-id="4cdea-161">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="4cdea-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4cdea-162">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="4cdea-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="4cdea-163">System-Only</span></span>            | <span data-ttu-id="4cdea-164">Faux</span><span class="sxs-lookup"><span data-stu-id="4cdea-164">False</span></span>                                                                                         |
| <span data-ttu-id="4cdea-165">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="4cdea-165">Is-Single-Valued</span></span>       | <span data-ttu-id="4cdea-166">Vrai</span><span class="sxs-lookup"><span data-stu-id="4cdea-166">True</span></span>                                                                                          |
| <span data-ttu-id="4cdea-167">Est indexé</span><span class="sxs-lookup"><span data-stu-id="4cdea-167">Is Indexed</span></span>             | <span data-ttu-id="4cdea-168">Faux</span><span class="sxs-lookup"><span data-stu-id="4cdea-168">False</span></span>                                                                                         |
| <span data-ttu-id="4cdea-169">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="4cdea-169">In Global Catalog</span></span>      | <span data-ttu-id="4cdea-170">Vrai</span><span class="sxs-lookup"><span data-stu-id="4cdea-170">True</span></span>                                                                                          |
| <span data-ttu-id="4cdea-171">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="4cdea-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="4cdea-172">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="4cdea-172">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="4cdea-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4cdea-173">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="4cdea-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4cdea-174">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="4cdea-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4cdea-175">Search-Flags</span></span>           | <span data-ttu-id="4cdea-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4cdea-176">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="4cdea-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4cdea-177">System-Flags</span></span>           | <span data-ttu-id="4cdea-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4cdea-178">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="4cdea-179">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="4cdea-179">Classes used in</span></span>        | [<span data-ttu-id="4cdea-180">**MSMQ-migrated-User**</span><span class="sxs-lookup"><span data-stu-id="4cdea-180">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="4cdea-181">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="4cdea-181">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4cdea-182">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4cdea-182">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4cdea-183">Entrée</span><span class="sxs-lookup"><span data-stu-id="4cdea-183">Entry</span></span> | <span data-ttu-id="4cdea-184">Valeur</span><span class="sxs-lookup"><span data-stu-id="4cdea-184">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cdea-185">ID de lien</span><span class="sxs-lookup"><span data-stu-id="4cdea-185">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="4cdea-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4cdea-186">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="4cdea-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="4cdea-187">System-Only</span></span>            | <span data-ttu-id="4cdea-188">Faux</span><span class="sxs-lookup"><span data-stu-id="4cdea-188">False</span></span>                                                                                         |
| <span data-ttu-id="4cdea-189">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="4cdea-189">Is-Single-Valued</span></span>       | <span data-ttu-id="4cdea-190">Vrai</span><span class="sxs-lookup"><span data-stu-id="4cdea-190">True</span></span>                                                                                          |
| <span data-ttu-id="4cdea-191">Est indexé</span><span class="sxs-lookup"><span data-stu-id="4cdea-191">Is Indexed</span></span>             | <span data-ttu-id="4cdea-192">Faux</span><span class="sxs-lookup"><span data-stu-id="4cdea-192">False</span></span>                                                                                         |
| <span data-ttu-id="4cdea-193">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="4cdea-193">In Global Catalog</span></span>      | <span data-ttu-id="4cdea-194">Vrai</span><span class="sxs-lookup"><span data-stu-id="4cdea-194">True</span></span>                                                                                          |
| <span data-ttu-id="4cdea-195">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="4cdea-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="4cdea-196">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="4cdea-196">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="4cdea-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4cdea-197">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="4cdea-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4cdea-198">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="4cdea-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4cdea-199">Search-Flags</span></span>           | <span data-ttu-id="4cdea-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4cdea-200">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="4cdea-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4cdea-201">System-Flags</span></span>           | <span data-ttu-id="4cdea-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4cdea-202">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="4cdea-203">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="4cdea-203">Classes used in</span></span>        | [<span data-ttu-id="4cdea-204">**MSMQ-migrated-User**</span><span class="sxs-lookup"><span data-stu-id="4cdea-204">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="4cdea-205">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="4cdea-205">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4cdea-206">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4cdea-206">Windows Server 2008</span></span>



| <span data-ttu-id="4cdea-207">Entrée</span><span class="sxs-lookup"><span data-stu-id="4cdea-207">Entry</span></span> | <span data-ttu-id="4cdea-208">Valeur</span><span class="sxs-lookup"><span data-stu-id="4cdea-208">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cdea-209">ID de lien</span><span class="sxs-lookup"><span data-stu-id="4cdea-209">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="4cdea-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4cdea-210">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="4cdea-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="4cdea-211">System-Only</span></span>            | <span data-ttu-id="4cdea-212">Faux</span><span class="sxs-lookup"><span data-stu-id="4cdea-212">False</span></span>                                                                                         |
| <span data-ttu-id="4cdea-213">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="4cdea-213">Is-Single-Valued</span></span>       | <span data-ttu-id="4cdea-214">Vrai</span><span class="sxs-lookup"><span data-stu-id="4cdea-214">True</span></span>                                                                                          |
| <span data-ttu-id="4cdea-215">Est indexé</span><span class="sxs-lookup"><span data-stu-id="4cdea-215">Is Indexed</span></span>             | <span data-ttu-id="4cdea-216">Faux</span><span class="sxs-lookup"><span data-stu-id="4cdea-216">False</span></span>                                                                                         |
| <span data-ttu-id="4cdea-217">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="4cdea-217">In Global Catalog</span></span>      | <span data-ttu-id="4cdea-218">Vrai</span><span class="sxs-lookup"><span data-stu-id="4cdea-218">True</span></span>                                                                                          |
| <span data-ttu-id="4cdea-219">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="4cdea-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="4cdea-220">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="4cdea-220">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="4cdea-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4cdea-221">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="4cdea-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4cdea-222">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="4cdea-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4cdea-223">Search-Flags</span></span>           | <span data-ttu-id="4cdea-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4cdea-224">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="4cdea-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4cdea-225">System-Flags</span></span>           | <span data-ttu-id="4cdea-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4cdea-226">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="4cdea-227">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="4cdea-227">Classes used in</span></span>        | [<span data-ttu-id="4cdea-228">**MSMQ-migrated-User**</span><span class="sxs-lookup"><span data-stu-id="4cdea-228">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="4cdea-229">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="4cdea-229">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4cdea-230">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4cdea-230">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4cdea-231">Entrée</span><span class="sxs-lookup"><span data-stu-id="4cdea-231">Entry</span></span> | <span data-ttu-id="4cdea-232">Valeur</span><span class="sxs-lookup"><span data-stu-id="4cdea-232">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cdea-233">ID de lien</span><span class="sxs-lookup"><span data-stu-id="4cdea-233">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="4cdea-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4cdea-234">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="4cdea-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="4cdea-235">System-Only</span></span>            | <span data-ttu-id="4cdea-236">Faux</span><span class="sxs-lookup"><span data-stu-id="4cdea-236">False</span></span>                                                                                         |
| <span data-ttu-id="4cdea-237">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="4cdea-237">Is-Single-Valued</span></span>       | <span data-ttu-id="4cdea-238">Vrai</span><span class="sxs-lookup"><span data-stu-id="4cdea-238">True</span></span>                                                                                          |
| <span data-ttu-id="4cdea-239">Est indexé</span><span class="sxs-lookup"><span data-stu-id="4cdea-239">Is Indexed</span></span>             | <span data-ttu-id="4cdea-240">Faux</span><span class="sxs-lookup"><span data-stu-id="4cdea-240">False</span></span>                                                                                         |
| <span data-ttu-id="4cdea-241">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="4cdea-241">In Global Catalog</span></span>      | <span data-ttu-id="4cdea-242">Vrai</span><span class="sxs-lookup"><span data-stu-id="4cdea-242">True</span></span>                                                                                          |
| <span data-ttu-id="4cdea-243">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="4cdea-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="4cdea-244">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="4cdea-244">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="4cdea-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4cdea-245">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="4cdea-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4cdea-246">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="4cdea-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4cdea-247">Search-Flags</span></span>           | <span data-ttu-id="4cdea-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4cdea-248">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="4cdea-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4cdea-249">System-Flags</span></span>           | <span data-ttu-id="4cdea-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4cdea-250">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="4cdea-251">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="4cdea-251">Classes used in</span></span>        | [<span data-ttu-id="4cdea-252">**MSMQ-migrated-User**</span><span class="sxs-lookup"><span data-stu-id="4cdea-252">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="4cdea-253">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="4cdea-253">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4cdea-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4cdea-254">Windows Server 2012</span></span>



| <span data-ttu-id="4cdea-255">Entrée</span><span class="sxs-lookup"><span data-stu-id="4cdea-255">Entry</span></span> | <span data-ttu-id="4cdea-256">Valeur</span><span class="sxs-lookup"><span data-stu-id="4cdea-256">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cdea-257">ID de lien</span><span class="sxs-lookup"><span data-stu-id="4cdea-257">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="4cdea-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4cdea-258">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="4cdea-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="4cdea-259">System-Only</span></span>            | <span data-ttu-id="4cdea-260">Faux</span><span class="sxs-lookup"><span data-stu-id="4cdea-260">False</span></span>                                                                                         |
| <span data-ttu-id="4cdea-261">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="4cdea-261">Is-Single-Valued</span></span>       | <span data-ttu-id="4cdea-262">Vrai</span><span class="sxs-lookup"><span data-stu-id="4cdea-262">True</span></span>                                                                                          |
| <span data-ttu-id="4cdea-263">Est indexé</span><span class="sxs-lookup"><span data-stu-id="4cdea-263">Is Indexed</span></span>             | <span data-ttu-id="4cdea-264">Faux</span><span class="sxs-lookup"><span data-stu-id="4cdea-264">False</span></span>                                                                                         |
| <span data-ttu-id="4cdea-265">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="4cdea-265">In Global Catalog</span></span>      | <span data-ttu-id="4cdea-266">Vrai</span><span class="sxs-lookup"><span data-stu-id="4cdea-266">True</span></span>                                                                                          |
| <span data-ttu-id="4cdea-267">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="4cdea-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="4cdea-268">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="4cdea-268">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="4cdea-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4cdea-269">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="4cdea-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4cdea-270">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="4cdea-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4cdea-271">Search-Flags</span></span>           | <span data-ttu-id="4cdea-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4cdea-272">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="4cdea-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4cdea-273">System-Flags</span></span>           | <span data-ttu-id="4cdea-274">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4cdea-274">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="4cdea-275">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="4cdea-275">Classes used in</span></span>        | [<span data-ttu-id="4cdea-276">**MSMQ-migrated-User**</span><span class="sxs-lookup"><span data-stu-id="4cdea-276">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="4cdea-277">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="4cdea-277">**User**</span></span>](c-user.md)<br/> |



 

 





