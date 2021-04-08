---
title: ACS-événement-niveau de journalisation
description: Niveau de journalisation RSVP.
ms.assetid: 2f3c645d-a064-40fb-965c-388b2fac61bc
ms.tgt_platform: multiple
keywords:
- 'ACS : schéma AD d’attribut de niveau journal des événements'
- Schéma AD de l’attribut aCSEventLogLevel
topic_type:
- apiref
api_name:
- ACS-Event-Log-Level
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62bb5701f665a3685845368eb2adc72fc33d10bd
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744428"
---
# <a name="acs-event-log-level-attribute"></a><span data-ttu-id="d5e23-105">ACS-événement-niveau de journalisation</span><span class="sxs-lookup"><span data-stu-id="d5e23-105">ACS-Event-Log-Level attribute</span></span>

<span data-ttu-id="d5e23-106">Niveau de journalisation RSVP.</span><span class="sxs-lookup"><span data-stu-id="d5e23-106">RSVP logging level.</span></span>



| <span data-ttu-id="d5e23-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="d5e23-107">Entry</span></span> | <span data-ttu-id="d5e23-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="d5e23-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="d5e23-109">CN</span><span class="sxs-lookup"><span data-stu-id="d5e23-109">CN</span></span>                | <span data-ttu-id="d5e23-110">ACS-événement-au niveau du journal</span><span class="sxs-lookup"><span data-stu-id="d5e23-110">ACS-Event-Log-Level</span></span>                     |
| <span data-ttu-id="d5e23-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="d5e23-111">Ldap-Display-Name</span></span> | <span data-ttu-id="d5e23-112">aCSEventLogLevel</span><span class="sxs-lookup"><span data-stu-id="d5e23-112">aCSEventLogLevel</span></span>                        |
| <span data-ttu-id="d5e23-113">Taille</span><span class="sxs-lookup"><span data-stu-id="d5e23-113">Size</span></span>              | <span data-ttu-id="d5e23-114">4 octets peuvent avoir les valeurs 0, 1, 2 et 3.</span><span class="sxs-lookup"><span data-stu-id="d5e23-114">4 bytes can have values 0, 1, 2, and 3.</span></span> |
| <span data-ttu-id="d5e23-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="d5e23-115">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="d5e23-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="d5e23-116">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="d5e23-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d5e23-117">Attribute-Id</span></span>      | <span data-ttu-id="d5e23-118">1.2.840.113556.1.4.769</span><span class="sxs-lookup"><span data-stu-id="d5e23-118">1.2.840.113556.1.4.769</span></span>                  |
| <span data-ttu-id="d5e23-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="d5e23-119">System-Id-Guid</span></span>    | <span data-ttu-id="d5e23-120">7f561286-5301-11d1-a9c5-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="d5e23-120">7f561286-5301-11d1-a9c5-0000f80367c1</span></span>    |
| <span data-ttu-id="d5e23-121">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d5e23-121">Syntax</span></span>            | [<span data-ttu-id="d5e23-122">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="d5e23-122">**Enumeration**</span></span>](s-enumeration.md)    |



## <a name="implementations"></a><span data-ttu-id="d5e23-123">Implémentations</span><span class="sxs-lookup"><span data-stu-id="d5e23-123">Implementations</span></span>

-   [<span data-ttu-id="d5e23-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d5e23-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d5e23-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d5e23-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d5e23-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d5e23-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d5e23-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d5e23-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d5e23-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d5e23-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d5e23-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d5e23-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d5e23-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d5e23-130">Windows 2000 Server</span></span>



| <span data-ttu-id="d5e23-131">Entrée</span><span class="sxs-lookup"><span data-stu-id="d5e23-131">Entry</span></span> | <span data-ttu-id="d5e23-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="d5e23-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="d5e23-133">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d5e23-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="d5e23-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d5e23-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="d5e23-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="d5e23-135">System-Only</span></span>            | <span data-ttu-id="d5e23-136">Faux</span><span class="sxs-lookup"><span data-stu-id="d5e23-136">False</span></span>                                        |
| <span data-ttu-id="d5e23-137">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d5e23-137">Is-Single-Valued</span></span>       | <span data-ttu-id="d5e23-138">Vrai</span><span class="sxs-lookup"><span data-stu-id="d5e23-138">True</span></span>                                         |
| <span data-ttu-id="d5e23-139">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d5e23-139">Is Indexed</span></span>             | <span data-ttu-id="d5e23-140">Faux</span><span class="sxs-lookup"><span data-stu-id="d5e23-140">False</span></span>                                        |
| <span data-ttu-id="d5e23-141">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d5e23-141">In Global Catalog</span></span>      | <span data-ttu-id="d5e23-142">Faux</span><span class="sxs-lookup"><span data-stu-id="d5e23-142">False</span></span>                                        |
| <span data-ttu-id="d5e23-143">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d5e23-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="d5e23-144">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d5e23-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="d5e23-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d5e23-145">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="d5e23-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d5e23-146">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="d5e23-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d5e23-147">Search-Flags</span></span>           | <span data-ttu-id="d5e23-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d5e23-148">0x00000000</span></span>                                   |
| <span data-ttu-id="d5e23-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d5e23-149">System-Flags</span></span>           | <span data-ttu-id="d5e23-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d5e23-150">0x00000010</span></span>                                   |
| <span data-ttu-id="d5e23-151">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d5e23-151">Classes used in</span></span>        | [<span data-ttu-id="d5e23-152">**ACS-sous-réseau**</span><span class="sxs-lookup"><span data-stu-id="d5e23-152">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d5e23-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d5e23-153">Windows Server 2003</span></span>



| <span data-ttu-id="d5e23-154">Entrée</span><span class="sxs-lookup"><span data-stu-id="d5e23-154">Entry</span></span> | <span data-ttu-id="d5e23-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="d5e23-155">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="d5e23-156">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d5e23-156">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="d5e23-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d5e23-157">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="d5e23-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="d5e23-158">System-Only</span></span>            | <span data-ttu-id="d5e23-159">Faux</span><span class="sxs-lookup"><span data-stu-id="d5e23-159">False</span></span>                                        |
| <span data-ttu-id="d5e23-160">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d5e23-160">Is-Single-Valued</span></span>       | <span data-ttu-id="d5e23-161">Vrai</span><span class="sxs-lookup"><span data-stu-id="d5e23-161">True</span></span>                                         |
| <span data-ttu-id="d5e23-162">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d5e23-162">Is Indexed</span></span>             | <span data-ttu-id="d5e23-163">Faux</span><span class="sxs-lookup"><span data-stu-id="d5e23-163">False</span></span>                                        |
| <span data-ttu-id="d5e23-164">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d5e23-164">In Global Catalog</span></span>      | <span data-ttu-id="d5e23-165">Faux</span><span class="sxs-lookup"><span data-stu-id="d5e23-165">False</span></span>                                        |
| <span data-ttu-id="d5e23-166">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d5e23-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="d5e23-167">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d5e23-167">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="d5e23-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d5e23-168">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="d5e23-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d5e23-169">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="d5e23-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d5e23-170">Search-Flags</span></span>           | <span data-ttu-id="d5e23-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d5e23-171">0x00000000</span></span>                                   |
| <span data-ttu-id="d5e23-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d5e23-172">System-Flags</span></span>           | <span data-ttu-id="d5e23-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d5e23-173">0x00000010</span></span>                                   |
| <span data-ttu-id="d5e23-174">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d5e23-174">Classes used in</span></span>        | [<span data-ttu-id="d5e23-175">**ACS-sous-réseau**</span><span class="sxs-lookup"><span data-stu-id="d5e23-175">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d5e23-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d5e23-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d5e23-177">Entrée</span><span class="sxs-lookup"><span data-stu-id="d5e23-177">Entry</span></span> | <span data-ttu-id="d5e23-178">Valeur</span><span class="sxs-lookup"><span data-stu-id="d5e23-178">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="d5e23-179">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d5e23-179">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="d5e23-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d5e23-180">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="d5e23-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="d5e23-181">System-Only</span></span>            | <span data-ttu-id="d5e23-182">Faux</span><span class="sxs-lookup"><span data-stu-id="d5e23-182">False</span></span>                                        |
| <span data-ttu-id="d5e23-183">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d5e23-183">Is-Single-Valued</span></span>       | <span data-ttu-id="d5e23-184">Vrai</span><span class="sxs-lookup"><span data-stu-id="d5e23-184">True</span></span>                                         |
| <span data-ttu-id="d5e23-185">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d5e23-185">Is Indexed</span></span>             | <span data-ttu-id="d5e23-186">Faux</span><span class="sxs-lookup"><span data-stu-id="d5e23-186">False</span></span>                                        |
| <span data-ttu-id="d5e23-187">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d5e23-187">In Global Catalog</span></span>      | <span data-ttu-id="d5e23-188">Faux</span><span class="sxs-lookup"><span data-stu-id="d5e23-188">False</span></span>                                        |
| <span data-ttu-id="d5e23-189">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d5e23-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="d5e23-190">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d5e23-190">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="d5e23-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d5e23-191">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="d5e23-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d5e23-192">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="d5e23-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d5e23-193">Search-Flags</span></span>           | <span data-ttu-id="d5e23-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d5e23-194">0x00000000</span></span>                                   |
| <span data-ttu-id="d5e23-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d5e23-195">System-Flags</span></span>           | <span data-ttu-id="d5e23-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d5e23-196">0x00000010</span></span>                                   |
| <span data-ttu-id="d5e23-197">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d5e23-197">Classes used in</span></span>        | [<span data-ttu-id="d5e23-198">**ACS-sous-réseau**</span><span class="sxs-lookup"><span data-stu-id="d5e23-198">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d5e23-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d5e23-199">Windows Server 2008</span></span>



| <span data-ttu-id="d5e23-200">Entrée</span><span class="sxs-lookup"><span data-stu-id="d5e23-200">Entry</span></span> | <span data-ttu-id="d5e23-201">Valeur</span><span class="sxs-lookup"><span data-stu-id="d5e23-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="d5e23-202">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d5e23-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="d5e23-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d5e23-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="d5e23-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="d5e23-204">System-Only</span></span>            | <span data-ttu-id="d5e23-205">Faux</span><span class="sxs-lookup"><span data-stu-id="d5e23-205">False</span></span>                                        |
| <span data-ttu-id="d5e23-206">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d5e23-206">Is-Single-Valued</span></span>       | <span data-ttu-id="d5e23-207">Vrai</span><span class="sxs-lookup"><span data-stu-id="d5e23-207">True</span></span>                                         |
| <span data-ttu-id="d5e23-208">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d5e23-208">Is Indexed</span></span>             | <span data-ttu-id="d5e23-209">Faux</span><span class="sxs-lookup"><span data-stu-id="d5e23-209">False</span></span>                                        |
| <span data-ttu-id="d5e23-210">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d5e23-210">In Global Catalog</span></span>      | <span data-ttu-id="d5e23-211">Faux</span><span class="sxs-lookup"><span data-stu-id="d5e23-211">False</span></span>                                        |
| <span data-ttu-id="d5e23-212">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d5e23-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="d5e23-213">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d5e23-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="d5e23-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d5e23-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="d5e23-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d5e23-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="d5e23-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d5e23-216">Search-Flags</span></span>           | <span data-ttu-id="d5e23-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d5e23-217">0x00000000</span></span>                                   |
| <span data-ttu-id="d5e23-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d5e23-218">System-Flags</span></span>           | <span data-ttu-id="d5e23-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d5e23-219">0x00000010</span></span>                                   |
| <span data-ttu-id="d5e23-220">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d5e23-220">Classes used in</span></span>        | [<span data-ttu-id="d5e23-221">**ACS-sous-réseau**</span><span class="sxs-lookup"><span data-stu-id="d5e23-221">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d5e23-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d5e23-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d5e23-223">Entrée</span><span class="sxs-lookup"><span data-stu-id="d5e23-223">Entry</span></span> | <span data-ttu-id="d5e23-224">Valeur</span><span class="sxs-lookup"><span data-stu-id="d5e23-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="d5e23-225">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d5e23-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="d5e23-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d5e23-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="d5e23-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="d5e23-227">System-Only</span></span>            | <span data-ttu-id="d5e23-228">Faux</span><span class="sxs-lookup"><span data-stu-id="d5e23-228">False</span></span>                                        |
| <span data-ttu-id="d5e23-229">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d5e23-229">Is-Single-Valued</span></span>       | <span data-ttu-id="d5e23-230">Vrai</span><span class="sxs-lookup"><span data-stu-id="d5e23-230">True</span></span>                                         |
| <span data-ttu-id="d5e23-231">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d5e23-231">Is Indexed</span></span>             | <span data-ttu-id="d5e23-232">Faux</span><span class="sxs-lookup"><span data-stu-id="d5e23-232">False</span></span>                                        |
| <span data-ttu-id="d5e23-233">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d5e23-233">In Global Catalog</span></span>      | <span data-ttu-id="d5e23-234">Faux</span><span class="sxs-lookup"><span data-stu-id="d5e23-234">False</span></span>                                        |
| <span data-ttu-id="d5e23-235">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d5e23-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="d5e23-236">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d5e23-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="d5e23-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d5e23-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="d5e23-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d5e23-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="d5e23-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d5e23-239">Search-Flags</span></span>           | <span data-ttu-id="d5e23-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d5e23-240">0x00000000</span></span>                                   |
| <span data-ttu-id="d5e23-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d5e23-241">System-Flags</span></span>           | <span data-ttu-id="d5e23-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d5e23-242">0x00000010</span></span>                                   |
| <span data-ttu-id="d5e23-243">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d5e23-243">Classes used in</span></span>        | [<span data-ttu-id="d5e23-244">**ACS-sous-réseau**</span><span class="sxs-lookup"><span data-stu-id="d5e23-244">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d5e23-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d5e23-245">Windows Server 2012</span></span>



| <span data-ttu-id="d5e23-246">Entrée</span><span class="sxs-lookup"><span data-stu-id="d5e23-246">Entry</span></span> | <span data-ttu-id="d5e23-247">Valeur</span><span class="sxs-lookup"><span data-stu-id="d5e23-247">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="d5e23-248">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d5e23-248">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="d5e23-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d5e23-249">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="d5e23-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="d5e23-250">System-Only</span></span>            | <span data-ttu-id="d5e23-251">Faux</span><span class="sxs-lookup"><span data-stu-id="d5e23-251">False</span></span>                                        |
| <span data-ttu-id="d5e23-252">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d5e23-252">Is-Single-Valued</span></span>       | <span data-ttu-id="d5e23-253">Vrai</span><span class="sxs-lookup"><span data-stu-id="d5e23-253">True</span></span>                                         |
| <span data-ttu-id="d5e23-254">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d5e23-254">Is Indexed</span></span>             | <span data-ttu-id="d5e23-255">Faux</span><span class="sxs-lookup"><span data-stu-id="d5e23-255">False</span></span>                                        |
| <span data-ttu-id="d5e23-256">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d5e23-256">In Global Catalog</span></span>      | <span data-ttu-id="d5e23-257">Faux</span><span class="sxs-lookup"><span data-stu-id="d5e23-257">False</span></span>                                        |
| <span data-ttu-id="d5e23-258">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d5e23-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="d5e23-259">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d5e23-259">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="d5e23-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d5e23-260">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="d5e23-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d5e23-261">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="d5e23-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d5e23-262">Search-Flags</span></span>           | <span data-ttu-id="d5e23-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d5e23-263">0x00000000</span></span>                                   |
| <span data-ttu-id="d5e23-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d5e23-264">System-Flags</span></span>           | <span data-ttu-id="d5e23-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d5e23-265">0x00000010</span></span>                                   |
| <span data-ttu-id="d5e23-266">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d5e23-266">Classes used in</span></span>        | [<span data-ttu-id="d5e23-267">**ACS-sous-réseau**</span><span class="sxs-lookup"><span data-stu-id="d5e23-267">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 





