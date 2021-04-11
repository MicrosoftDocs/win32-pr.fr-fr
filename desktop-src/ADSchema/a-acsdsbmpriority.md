---
title: ACS-DSBM-Priority (attribut)
description: Cet attribut contient la priorité de ce gestionnaire de bande passante de réseau (SBM).
ms.assetid: 08dd49d2-a2fa-4707-8302-25566680b91d
ms.tgt_platform: multiple
keywords:
- ACS-DSBM-schéma AD d’attribut de priorité
- Schéma AD de l’attribut aCSDSBMPriority
topic_type:
- apiref
api_name:
- ACS-DSBM-Priority
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dd32c9e9cca95dbd5f52569de0b61e886033d13
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104108323"
---
# <a name="acs-dsbm-priority-attribute"></a><span data-ttu-id="611fc-105">ACS-DSBM-Priority (attribut)</span><span class="sxs-lookup"><span data-stu-id="611fc-105">ACS-DSBM-Priority attribute</span></span>

<span data-ttu-id="611fc-106">Cet attribut contient la priorité de ce gestionnaire de bande passante de réseau (SBM).</span><span class="sxs-lookup"><span data-stu-id="611fc-106">This attributes contains the priority for this Subnet Bandwidth Manager (SBM).</span></span> <span data-ttu-id="611fc-107">Lorsqu’un nouveau DSBM (Subnet Bandwidth Manager) désigné doit être choisi, cette valeur est envoyée à d’autres SBMs dans le domaine dans le cadre d’un message de demande de \_ prêt.</span><span class="sxs-lookup"><span data-stu-id="611fc-107">When a new Designated Subnet Bandwidth Manager (DSBM) needs to be elected, this value is sent to other SBMs in the domain as part of a DSBM\_willing message.</span></span> <span data-ttu-id="611fc-108">Le SBM avec la priorité la plus élevée est élu comme nouveau DSBM.</span><span class="sxs-lookup"><span data-stu-id="611fc-108">The SBM with the highest priority is elected as the new DSBM.</span></span>



| <span data-ttu-id="611fc-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="611fc-109">Entry</span></span> | <span data-ttu-id="611fc-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="611fc-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="611fc-111">CN</span><span class="sxs-lookup"><span data-stu-id="611fc-111">CN</span></span>                | <span data-ttu-id="611fc-112">ACS-DSBM-Priority</span><span class="sxs-lookup"><span data-stu-id="611fc-112">ACS-DSBM-Priority</span></span>                    |
| <span data-ttu-id="611fc-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="611fc-113">Ldap-Display-Name</span></span> | <span data-ttu-id="611fc-114">aCSDSBMPriority</span><span class="sxs-lookup"><span data-stu-id="611fc-114">aCSDSBMPriority</span></span>                      |
| <span data-ttu-id="611fc-115">Taille</span><span class="sxs-lookup"><span data-stu-id="611fc-115">Size</span></span>              | <span data-ttu-id="611fc-116">4 octets</span><span class="sxs-lookup"><span data-stu-id="611fc-116">4 bytes</span></span>                              |
| <span data-ttu-id="611fc-117">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="611fc-117">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="611fc-118">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="611fc-118">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="611fc-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="611fc-119">Attribute-Id</span></span>      | <span data-ttu-id="611fc-120">1.2.840.113556.1.4.776</span><span class="sxs-lookup"><span data-stu-id="611fc-120">1.2.840.113556.1.4.776</span></span>               |
| <span data-ttu-id="611fc-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="611fc-121">System-Id-Guid</span></span>    | <span data-ttu-id="611fc-122">1cb3559e-56d0-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="611fc-122">1cb3559e-56d0-11d1-a9c6-0000f80367c1</span></span> |
| <span data-ttu-id="611fc-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="611fc-123">Syntax</span></span>            | [<span data-ttu-id="611fc-124">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="611fc-124">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="611fc-125">Implémentations</span><span class="sxs-lookup"><span data-stu-id="611fc-125">Implementations</span></span>

-   [<span data-ttu-id="611fc-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="611fc-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="611fc-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="611fc-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="611fc-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="611fc-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="611fc-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="611fc-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="611fc-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="611fc-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="611fc-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="611fc-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="611fc-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="611fc-132">Windows 2000 Server</span></span>



| <span data-ttu-id="611fc-133">Entrée</span><span class="sxs-lookup"><span data-stu-id="611fc-133">Entry</span></span> | <span data-ttu-id="611fc-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="611fc-134">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="611fc-135">ID de lien</span><span class="sxs-lookup"><span data-stu-id="611fc-135">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="611fc-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="611fc-136">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="611fc-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="611fc-137">System-Only</span></span>            | <span data-ttu-id="611fc-138">Faux</span><span class="sxs-lookup"><span data-stu-id="611fc-138">False</span></span>                                        |
| <span data-ttu-id="611fc-139">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="611fc-139">Is-Single-Valued</span></span>       | <span data-ttu-id="611fc-140">Vrai</span><span class="sxs-lookup"><span data-stu-id="611fc-140">True</span></span>                                         |
| <span data-ttu-id="611fc-141">Est indexé</span><span class="sxs-lookup"><span data-stu-id="611fc-141">Is Indexed</span></span>             | <span data-ttu-id="611fc-142">Faux</span><span class="sxs-lookup"><span data-stu-id="611fc-142">False</span></span>                                        |
| <span data-ttu-id="611fc-143">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="611fc-143">In Global Catalog</span></span>      | <span data-ttu-id="611fc-144">Faux</span><span class="sxs-lookup"><span data-stu-id="611fc-144">False</span></span>                                        |
| <span data-ttu-id="611fc-145">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="611fc-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="611fc-146">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="611fc-146">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="611fc-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="611fc-147">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="611fc-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="611fc-148">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="611fc-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="611fc-149">Search-Flags</span></span>           | <span data-ttu-id="611fc-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="611fc-150">0x00000000</span></span>                                   |
| <span data-ttu-id="611fc-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="611fc-151">System-Flags</span></span>           | <span data-ttu-id="611fc-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="611fc-152">0x00000010</span></span>                                   |
| <span data-ttu-id="611fc-153">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="611fc-153">Classes used in</span></span>        | [<span data-ttu-id="611fc-154">**ACS-sous-réseau**</span><span class="sxs-lookup"><span data-stu-id="611fc-154">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="611fc-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="611fc-155">Windows Server 2003</span></span>



| <span data-ttu-id="611fc-156">Entrée</span><span class="sxs-lookup"><span data-stu-id="611fc-156">Entry</span></span> | <span data-ttu-id="611fc-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="611fc-157">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="611fc-158">ID de lien</span><span class="sxs-lookup"><span data-stu-id="611fc-158">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="611fc-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="611fc-159">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="611fc-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="611fc-160">System-Only</span></span>            | <span data-ttu-id="611fc-161">Faux</span><span class="sxs-lookup"><span data-stu-id="611fc-161">False</span></span>                                        |
| <span data-ttu-id="611fc-162">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="611fc-162">Is-Single-Valued</span></span>       | <span data-ttu-id="611fc-163">Vrai</span><span class="sxs-lookup"><span data-stu-id="611fc-163">True</span></span>                                         |
| <span data-ttu-id="611fc-164">Est indexé</span><span class="sxs-lookup"><span data-stu-id="611fc-164">Is Indexed</span></span>             | <span data-ttu-id="611fc-165">Faux</span><span class="sxs-lookup"><span data-stu-id="611fc-165">False</span></span>                                        |
| <span data-ttu-id="611fc-166">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="611fc-166">In Global Catalog</span></span>      | <span data-ttu-id="611fc-167">Faux</span><span class="sxs-lookup"><span data-stu-id="611fc-167">False</span></span>                                        |
| <span data-ttu-id="611fc-168">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="611fc-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="611fc-169">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="611fc-169">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="611fc-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="611fc-170">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="611fc-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="611fc-171">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="611fc-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="611fc-172">Search-Flags</span></span>           | <span data-ttu-id="611fc-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="611fc-173">0x00000000</span></span>                                   |
| <span data-ttu-id="611fc-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="611fc-174">System-Flags</span></span>           | <span data-ttu-id="611fc-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="611fc-175">0x00000010</span></span>                                   |
| <span data-ttu-id="611fc-176">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="611fc-176">Classes used in</span></span>        | [<span data-ttu-id="611fc-177">**ACS-sous-réseau**</span><span class="sxs-lookup"><span data-stu-id="611fc-177">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="611fc-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="611fc-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="611fc-179">Entrée</span><span class="sxs-lookup"><span data-stu-id="611fc-179">Entry</span></span> | <span data-ttu-id="611fc-180">Valeur</span><span class="sxs-lookup"><span data-stu-id="611fc-180">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="611fc-181">ID de lien</span><span class="sxs-lookup"><span data-stu-id="611fc-181">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="611fc-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="611fc-182">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="611fc-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="611fc-183">System-Only</span></span>            | <span data-ttu-id="611fc-184">Faux</span><span class="sxs-lookup"><span data-stu-id="611fc-184">False</span></span>                                        |
| <span data-ttu-id="611fc-185">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="611fc-185">Is-Single-Valued</span></span>       | <span data-ttu-id="611fc-186">Vrai</span><span class="sxs-lookup"><span data-stu-id="611fc-186">True</span></span>                                         |
| <span data-ttu-id="611fc-187">Est indexé</span><span class="sxs-lookup"><span data-stu-id="611fc-187">Is Indexed</span></span>             | <span data-ttu-id="611fc-188">Faux</span><span class="sxs-lookup"><span data-stu-id="611fc-188">False</span></span>                                        |
| <span data-ttu-id="611fc-189">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="611fc-189">In Global Catalog</span></span>      | <span data-ttu-id="611fc-190">Faux</span><span class="sxs-lookup"><span data-stu-id="611fc-190">False</span></span>                                        |
| <span data-ttu-id="611fc-191">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="611fc-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="611fc-192">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="611fc-192">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="611fc-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="611fc-193">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="611fc-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="611fc-194">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="611fc-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="611fc-195">Search-Flags</span></span>           | <span data-ttu-id="611fc-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="611fc-196">0x00000000</span></span>                                   |
| <span data-ttu-id="611fc-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="611fc-197">System-Flags</span></span>           | <span data-ttu-id="611fc-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="611fc-198">0x00000010</span></span>                                   |
| <span data-ttu-id="611fc-199">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="611fc-199">Classes used in</span></span>        | [<span data-ttu-id="611fc-200">**ACS-sous-réseau**</span><span class="sxs-lookup"><span data-stu-id="611fc-200">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="611fc-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="611fc-201">Windows Server 2008</span></span>



| <span data-ttu-id="611fc-202">Entrée</span><span class="sxs-lookup"><span data-stu-id="611fc-202">Entry</span></span> | <span data-ttu-id="611fc-203">Valeur</span><span class="sxs-lookup"><span data-stu-id="611fc-203">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="611fc-204">ID de lien</span><span class="sxs-lookup"><span data-stu-id="611fc-204">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="611fc-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="611fc-205">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="611fc-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="611fc-206">System-Only</span></span>            | <span data-ttu-id="611fc-207">Faux</span><span class="sxs-lookup"><span data-stu-id="611fc-207">False</span></span>                                        |
| <span data-ttu-id="611fc-208">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="611fc-208">Is-Single-Valued</span></span>       | <span data-ttu-id="611fc-209">Vrai</span><span class="sxs-lookup"><span data-stu-id="611fc-209">True</span></span>                                         |
| <span data-ttu-id="611fc-210">Est indexé</span><span class="sxs-lookup"><span data-stu-id="611fc-210">Is Indexed</span></span>             | <span data-ttu-id="611fc-211">Faux</span><span class="sxs-lookup"><span data-stu-id="611fc-211">False</span></span>                                        |
| <span data-ttu-id="611fc-212">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="611fc-212">In Global Catalog</span></span>      | <span data-ttu-id="611fc-213">Faux</span><span class="sxs-lookup"><span data-stu-id="611fc-213">False</span></span>                                        |
| <span data-ttu-id="611fc-214">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="611fc-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="611fc-215">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="611fc-215">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="611fc-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="611fc-216">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="611fc-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="611fc-217">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="611fc-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="611fc-218">Search-Flags</span></span>           | <span data-ttu-id="611fc-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="611fc-219">0x00000000</span></span>                                   |
| <span data-ttu-id="611fc-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="611fc-220">System-Flags</span></span>           | <span data-ttu-id="611fc-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="611fc-221">0x00000010</span></span>                                   |
| <span data-ttu-id="611fc-222">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="611fc-222">Classes used in</span></span>        | [<span data-ttu-id="611fc-223">**ACS-sous-réseau**</span><span class="sxs-lookup"><span data-stu-id="611fc-223">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="611fc-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="611fc-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="611fc-225">Entrée</span><span class="sxs-lookup"><span data-stu-id="611fc-225">Entry</span></span> | <span data-ttu-id="611fc-226">Valeur</span><span class="sxs-lookup"><span data-stu-id="611fc-226">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="611fc-227">ID de lien</span><span class="sxs-lookup"><span data-stu-id="611fc-227">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="611fc-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="611fc-228">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="611fc-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="611fc-229">System-Only</span></span>            | <span data-ttu-id="611fc-230">Faux</span><span class="sxs-lookup"><span data-stu-id="611fc-230">False</span></span>                                        |
| <span data-ttu-id="611fc-231">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="611fc-231">Is-Single-Valued</span></span>       | <span data-ttu-id="611fc-232">Vrai</span><span class="sxs-lookup"><span data-stu-id="611fc-232">True</span></span>                                         |
| <span data-ttu-id="611fc-233">Est indexé</span><span class="sxs-lookup"><span data-stu-id="611fc-233">Is Indexed</span></span>             | <span data-ttu-id="611fc-234">Faux</span><span class="sxs-lookup"><span data-stu-id="611fc-234">False</span></span>                                        |
| <span data-ttu-id="611fc-235">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="611fc-235">In Global Catalog</span></span>      | <span data-ttu-id="611fc-236">Faux</span><span class="sxs-lookup"><span data-stu-id="611fc-236">False</span></span>                                        |
| <span data-ttu-id="611fc-237">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="611fc-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="611fc-238">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="611fc-238">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="611fc-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="611fc-239">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="611fc-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="611fc-240">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="611fc-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="611fc-241">Search-Flags</span></span>           | <span data-ttu-id="611fc-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="611fc-242">0x00000000</span></span>                                   |
| <span data-ttu-id="611fc-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="611fc-243">System-Flags</span></span>           | <span data-ttu-id="611fc-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="611fc-244">0x00000010</span></span>                                   |
| <span data-ttu-id="611fc-245">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="611fc-245">Classes used in</span></span>        | [<span data-ttu-id="611fc-246">**ACS-sous-réseau**</span><span class="sxs-lookup"><span data-stu-id="611fc-246">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="611fc-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="611fc-247">Windows Server 2012</span></span>



| <span data-ttu-id="611fc-248">Entrée</span><span class="sxs-lookup"><span data-stu-id="611fc-248">Entry</span></span> | <span data-ttu-id="611fc-249">Valeur</span><span class="sxs-lookup"><span data-stu-id="611fc-249">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="611fc-250">ID de lien</span><span class="sxs-lookup"><span data-stu-id="611fc-250">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="611fc-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="611fc-251">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="611fc-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="611fc-252">System-Only</span></span>            | <span data-ttu-id="611fc-253">Faux</span><span class="sxs-lookup"><span data-stu-id="611fc-253">False</span></span>                                        |
| <span data-ttu-id="611fc-254">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="611fc-254">Is-Single-Valued</span></span>       | <span data-ttu-id="611fc-255">Vrai</span><span class="sxs-lookup"><span data-stu-id="611fc-255">True</span></span>                                         |
| <span data-ttu-id="611fc-256">Est indexé</span><span class="sxs-lookup"><span data-stu-id="611fc-256">Is Indexed</span></span>             | <span data-ttu-id="611fc-257">Faux</span><span class="sxs-lookup"><span data-stu-id="611fc-257">False</span></span>                                        |
| <span data-ttu-id="611fc-258">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="611fc-258">In Global Catalog</span></span>      | <span data-ttu-id="611fc-259">Faux</span><span class="sxs-lookup"><span data-stu-id="611fc-259">False</span></span>                                        |
| <span data-ttu-id="611fc-260">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="611fc-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="611fc-261">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="611fc-261">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="611fc-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="611fc-262">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="611fc-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="611fc-263">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="611fc-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="611fc-264">Search-Flags</span></span>           | <span data-ttu-id="611fc-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="611fc-265">0x00000000</span></span>                                   |
| <span data-ttu-id="611fc-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="611fc-266">System-Flags</span></span>           | <span data-ttu-id="611fc-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="611fc-267">0x00000010</span></span>                                   |
| <span data-ttu-id="611fc-268">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="611fc-268">Classes used in</span></span>        | [<span data-ttu-id="611fc-269">**ACS-sous-réseau**</span><span class="sxs-lookup"><span data-stu-id="611fc-269">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 





