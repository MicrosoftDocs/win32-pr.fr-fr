---
title: attribut de quota ms-DS-default
description: Quota par défaut qui s’applique à un principal de sécurité qui crée un objet dans le contexte de nommage s’il n’existe aucune spécification de quota qui couvre le principal de sécurité.
ms.assetid: 48074aaa-3997-40ac-92fe-b3112408ab45
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut de quota ms-DS-default
- Schéma Active Directory de l’attribut msDS-DefaultQuota
topic_type:
- apiref
api_name:
- ms-DS-Default-Quota
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d96f1429be72c623843608856da88729b1240c38
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103949888"
---
# <a name="ms-ds-default-quota-attribute"></a><span data-ttu-id="f4253-105">attribut de quota ms-DS-default</span><span class="sxs-lookup"><span data-stu-id="f4253-105">ms-DS-Default-Quota attribute</span></span>

<span data-ttu-id="f4253-106">Quota par défaut qui s’applique à un principal de sécurité qui crée un objet dans le contexte de nommage s’il n’existe aucune spécification de quota qui couvre le principal de sécurité.</span><span class="sxs-lookup"><span data-stu-id="f4253-106">The default quota that will apply to a security principal that creates an object in the NC if no quota specification exists that covers the security principal.</span></span>



| <span data-ttu-id="f4253-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="f4253-107">Entry</span></span> | <span data-ttu-id="f4253-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="f4253-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="f4253-109">CN</span><span class="sxs-lookup"><span data-stu-id="f4253-109">CN</span></span>                | <span data-ttu-id="f4253-110">ms-DS-default-quota</span><span class="sxs-lookup"><span data-stu-id="f4253-110">ms-DS-Default-Quota</span></span>                  |
| <span data-ttu-id="f4253-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f4253-111">Ldap-Display-Name</span></span> | <span data-ttu-id="f4253-112">msDS-DefaultQuota</span><span class="sxs-lookup"><span data-stu-id="f4253-112">msDS-DefaultQuota</span></span>                    |
| <span data-ttu-id="f4253-113">Taille</span><span class="sxs-lookup"><span data-stu-id="f4253-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="f4253-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="f4253-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="f4253-115">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="f4253-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="f4253-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f4253-116">Attribute-Id</span></span>      | <span data-ttu-id="f4253-117">1.2.840.113556.1.4.1846</span><span class="sxs-lookup"><span data-stu-id="f4253-117">1.2.840.113556.1.4.1846</span></span>              |
| <span data-ttu-id="f4253-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f4253-118">System-Id-Guid</span></span>    | <span data-ttu-id="f4253-119">6818f726-674b-441b-8a3a-f40596374cea</span><span class="sxs-lookup"><span data-stu-id="f4253-119">6818f726-674b-441b-8a3a-f40596374cea</span></span> |
| <span data-ttu-id="f4253-120">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f4253-120">Syntax</span></span>            | [<span data-ttu-id="f4253-121">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="f4253-121">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="f4253-122">Implémentations</span><span class="sxs-lookup"><span data-stu-id="f4253-122">Implementations</span></span>

-   [<span data-ttu-id="f4253-123">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f4253-123">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f4253-124">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="f4253-124">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="f4253-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f4253-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f4253-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f4253-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f4253-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f4253-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f4253-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f4253-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="f4253-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f4253-129">Windows Server 2003</span></span>



| <span data-ttu-id="f4253-130">Entrée</span><span class="sxs-lookup"><span data-stu-id="f4253-130">Entry</span></span> | <span data-ttu-id="f4253-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="f4253-131">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="f4253-132">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f4253-132">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="f4253-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f4253-133">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="f4253-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="f4253-134">System-Only</span></span>            | <span data-ttu-id="f4253-135">Faux</span><span class="sxs-lookup"><span data-stu-id="f4253-135">False</span></span>                                                             |
| <span data-ttu-id="f4253-136">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f4253-136">Is-Single-Valued</span></span>       | <span data-ttu-id="f4253-137">Vrai</span><span class="sxs-lookup"><span data-stu-id="f4253-137">True</span></span>                                                              |
| <span data-ttu-id="f4253-138">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f4253-138">Is Indexed</span></span>             | <span data-ttu-id="f4253-139">Faux</span><span class="sxs-lookup"><span data-stu-id="f4253-139">False</span></span>                                                             |
| <span data-ttu-id="f4253-140">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f4253-140">In Global Catalog</span></span>      | <span data-ttu-id="f4253-141">Faux</span><span class="sxs-lookup"><span data-stu-id="f4253-141">False</span></span>                                                             |
| <span data-ttu-id="f4253-142">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f4253-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="f4253-143">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f4253-143">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="f4253-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f4253-144">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="f4253-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f4253-145">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="f4253-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f4253-146">Search-Flags</span></span>           | <span data-ttu-id="f4253-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f4253-147">0x00000000</span></span>                                                        |
| <span data-ttu-id="f4253-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f4253-148">System-Flags</span></span>           | <span data-ttu-id="f4253-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f4253-149">0x00000010</span></span>                                                        |
| <span data-ttu-id="f4253-150">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f4253-150">Classes used in</span></span>        | [<span data-ttu-id="f4253-151">**ms-DS-quota-Container**</span><span class="sxs-lookup"><span data-stu-id="f4253-151">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="adam"></a><span data-ttu-id="f4253-152">ADAM</span><span class="sxs-lookup"><span data-stu-id="f4253-152">ADAM</span></span>



| <span data-ttu-id="f4253-153">Entrée</span><span class="sxs-lookup"><span data-stu-id="f4253-153">Entry</span></span> | <span data-ttu-id="f4253-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="f4253-154">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="f4253-155">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f4253-155">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="f4253-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f4253-156">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="f4253-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="f4253-157">System-Only</span></span>            | <span data-ttu-id="f4253-158">Faux</span><span class="sxs-lookup"><span data-stu-id="f4253-158">False</span></span>                                                             |
| <span data-ttu-id="f4253-159">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f4253-159">Is-Single-Valued</span></span>       | <span data-ttu-id="f4253-160">Vrai</span><span class="sxs-lookup"><span data-stu-id="f4253-160">True</span></span>                                                              |
| <span data-ttu-id="f4253-161">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f4253-161">Is Indexed</span></span>             | <span data-ttu-id="f4253-162">Faux</span><span class="sxs-lookup"><span data-stu-id="f4253-162">False</span></span>                                                             |
| <span data-ttu-id="f4253-163">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f4253-163">In Global Catalog</span></span>      | <span data-ttu-id="f4253-164">Faux</span><span class="sxs-lookup"><span data-stu-id="f4253-164">False</span></span>                                                             |
| <span data-ttu-id="f4253-165">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f4253-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="f4253-166">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f4253-166">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="f4253-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f4253-167">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="f4253-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f4253-168">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="f4253-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f4253-169">Search-Flags</span></span>           | <span data-ttu-id="f4253-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f4253-170">0x00000000</span></span>                                                        |
| <span data-ttu-id="f4253-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f4253-171">System-Flags</span></span>           | <span data-ttu-id="f4253-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f4253-172">0x00000010</span></span>                                                        |
| <span data-ttu-id="f4253-173">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f4253-173">Classes used in</span></span>        | [<span data-ttu-id="f4253-174">**ms-DS-quota-Container**</span><span class="sxs-lookup"><span data-stu-id="f4253-174">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f4253-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f4253-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f4253-176">Entrée</span><span class="sxs-lookup"><span data-stu-id="f4253-176">Entry</span></span> | <span data-ttu-id="f4253-177">Valeur</span><span class="sxs-lookup"><span data-stu-id="f4253-177">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="f4253-178">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f4253-178">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="f4253-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f4253-179">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="f4253-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="f4253-180">System-Only</span></span>            | <span data-ttu-id="f4253-181">Faux</span><span class="sxs-lookup"><span data-stu-id="f4253-181">False</span></span>                                                             |
| <span data-ttu-id="f4253-182">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f4253-182">Is-Single-Valued</span></span>       | <span data-ttu-id="f4253-183">Vrai</span><span class="sxs-lookup"><span data-stu-id="f4253-183">True</span></span>                                                              |
| <span data-ttu-id="f4253-184">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f4253-184">Is Indexed</span></span>             | <span data-ttu-id="f4253-185">Faux</span><span class="sxs-lookup"><span data-stu-id="f4253-185">False</span></span>                                                             |
| <span data-ttu-id="f4253-186">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f4253-186">In Global Catalog</span></span>      | <span data-ttu-id="f4253-187">Faux</span><span class="sxs-lookup"><span data-stu-id="f4253-187">False</span></span>                                                             |
| <span data-ttu-id="f4253-188">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f4253-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="f4253-189">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f4253-189">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="f4253-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f4253-190">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="f4253-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f4253-191">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="f4253-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f4253-192">Search-Flags</span></span>           | <span data-ttu-id="f4253-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f4253-193">0x00000000</span></span>                                                        |
| <span data-ttu-id="f4253-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f4253-194">System-Flags</span></span>           | <span data-ttu-id="f4253-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f4253-195">0x00000010</span></span>                                                        |
| <span data-ttu-id="f4253-196">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f4253-196">Classes used in</span></span>        | [<span data-ttu-id="f4253-197">**ms-DS-quota-Container**</span><span class="sxs-lookup"><span data-stu-id="f4253-197">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f4253-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f4253-198">Windows Server 2008</span></span>



| <span data-ttu-id="f4253-199">Entrée</span><span class="sxs-lookup"><span data-stu-id="f4253-199">Entry</span></span> | <span data-ttu-id="f4253-200">Valeur</span><span class="sxs-lookup"><span data-stu-id="f4253-200">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="f4253-201">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f4253-201">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="f4253-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f4253-202">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="f4253-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="f4253-203">System-Only</span></span>            | <span data-ttu-id="f4253-204">Faux</span><span class="sxs-lookup"><span data-stu-id="f4253-204">False</span></span>                                                             |
| <span data-ttu-id="f4253-205">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f4253-205">Is-Single-Valued</span></span>       | <span data-ttu-id="f4253-206">Vrai</span><span class="sxs-lookup"><span data-stu-id="f4253-206">True</span></span>                                                              |
| <span data-ttu-id="f4253-207">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f4253-207">Is Indexed</span></span>             | <span data-ttu-id="f4253-208">Faux</span><span class="sxs-lookup"><span data-stu-id="f4253-208">False</span></span>                                                             |
| <span data-ttu-id="f4253-209">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f4253-209">In Global Catalog</span></span>      | <span data-ttu-id="f4253-210">Faux</span><span class="sxs-lookup"><span data-stu-id="f4253-210">False</span></span>                                                             |
| <span data-ttu-id="f4253-211">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f4253-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="f4253-212">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f4253-212">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="f4253-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f4253-213">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="f4253-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f4253-214">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="f4253-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f4253-215">Search-Flags</span></span>           | <span data-ttu-id="f4253-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f4253-216">0x00000000</span></span>                                                        |
| <span data-ttu-id="f4253-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f4253-217">System-Flags</span></span>           | <span data-ttu-id="f4253-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f4253-218">0x00000010</span></span>                                                        |
| <span data-ttu-id="f4253-219">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f4253-219">Classes used in</span></span>        | [<span data-ttu-id="f4253-220">**ms-DS-quota-Container**</span><span class="sxs-lookup"><span data-stu-id="f4253-220">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f4253-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f4253-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f4253-222">Entrée</span><span class="sxs-lookup"><span data-stu-id="f4253-222">Entry</span></span> | <span data-ttu-id="f4253-223">Valeur</span><span class="sxs-lookup"><span data-stu-id="f4253-223">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="f4253-224">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f4253-224">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="f4253-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f4253-225">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="f4253-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="f4253-226">System-Only</span></span>            | <span data-ttu-id="f4253-227">Faux</span><span class="sxs-lookup"><span data-stu-id="f4253-227">False</span></span>                                                             |
| <span data-ttu-id="f4253-228">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f4253-228">Is-Single-Valued</span></span>       | <span data-ttu-id="f4253-229">Vrai</span><span class="sxs-lookup"><span data-stu-id="f4253-229">True</span></span>                                                              |
| <span data-ttu-id="f4253-230">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f4253-230">Is Indexed</span></span>             | <span data-ttu-id="f4253-231">Faux</span><span class="sxs-lookup"><span data-stu-id="f4253-231">False</span></span>                                                             |
| <span data-ttu-id="f4253-232">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f4253-232">In Global Catalog</span></span>      | <span data-ttu-id="f4253-233">Faux</span><span class="sxs-lookup"><span data-stu-id="f4253-233">False</span></span>                                                             |
| <span data-ttu-id="f4253-234">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f4253-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="f4253-235">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f4253-235">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="f4253-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f4253-236">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="f4253-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f4253-237">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="f4253-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f4253-238">Search-Flags</span></span>           | <span data-ttu-id="f4253-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f4253-239">0x00000000</span></span>                                                        |
| <span data-ttu-id="f4253-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f4253-240">System-Flags</span></span>           | <span data-ttu-id="f4253-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f4253-241">0x00000010</span></span>                                                        |
| <span data-ttu-id="f4253-242">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f4253-242">Classes used in</span></span>        | [<span data-ttu-id="f4253-243">**ms-DS-quota-Container**</span><span class="sxs-lookup"><span data-stu-id="f4253-243">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f4253-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f4253-244">Windows Server 2012</span></span>



| <span data-ttu-id="f4253-245">Entrée</span><span class="sxs-lookup"><span data-stu-id="f4253-245">Entry</span></span> | <span data-ttu-id="f4253-246">Valeur</span><span class="sxs-lookup"><span data-stu-id="f4253-246">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="f4253-247">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f4253-247">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="f4253-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f4253-248">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="f4253-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="f4253-249">System-Only</span></span>            | <span data-ttu-id="f4253-250">Faux</span><span class="sxs-lookup"><span data-stu-id="f4253-250">False</span></span>                                                             |
| <span data-ttu-id="f4253-251">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f4253-251">Is-Single-Valued</span></span>       | <span data-ttu-id="f4253-252">Vrai</span><span class="sxs-lookup"><span data-stu-id="f4253-252">True</span></span>                                                              |
| <span data-ttu-id="f4253-253">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f4253-253">Is Indexed</span></span>             | <span data-ttu-id="f4253-254">Faux</span><span class="sxs-lookup"><span data-stu-id="f4253-254">False</span></span>                                                             |
| <span data-ttu-id="f4253-255">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f4253-255">In Global Catalog</span></span>      | <span data-ttu-id="f4253-256">Faux</span><span class="sxs-lookup"><span data-stu-id="f4253-256">False</span></span>                                                             |
| <span data-ttu-id="f4253-257">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f4253-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="f4253-258">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f4253-258">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="f4253-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f4253-259">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="f4253-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f4253-260">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="f4253-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f4253-261">Search-Flags</span></span>           | <span data-ttu-id="f4253-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f4253-262">0x00000000</span></span>                                                        |
| <span data-ttu-id="f4253-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f4253-263">System-Flags</span></span>           | <span data-ttu-id="f4253-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f4253-264">0x00000010</span></span>                                                        |
| <span data-ttu-id="f4253-265">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f4253-265">Classes used in</span></span>        | [<span data-ttu-id="f4253-266">**ms-DS-quota-Container**</span><span class="sxs-lookup"><span data-stu-id="f4253-266">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



 

 





