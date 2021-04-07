---
title: Attribut SD-Rights-effective
description: Cet attribut construit retourne une valeur DWORD unique qui peut avoir jusqu’à trois bits Set OWNER \_ Security \_ INFORMATIONDACL \_ Security \_ INFORMATIONSACL \_ Security \_ Information Security. Si un bit est défini, l’utilisateur dispose d’un accès en écriture à la partie correspondante du descripteur de sécurité. Owner correspond à la fois au propriétaire et au groupe.
ms.assetid: 66d1aefb-49be-42fc-b144-3fb95c59dd0f
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut de haute qualité SD
- Schéma AD de l’attribut sDRightsEffective
topic_type:
- apiref
api_name:
- SD-Rights-Effective
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac449cd18b3fb75a61f04fffc266c290b7763295
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103844934"
---
# <a name="sd-rights-effective-attribute"></a><span data-ttu-id="3aa32-106">Attribut SD-Rights-effective</span><span class="sxs-lookup"><span data-stu-id="3aa32-106">SD-Rights-Effective attribute</span></span>

<span data-ttu-id="3aa32-107">Cet attribut construit retourne une valeur **DWORD** unique qui peut avoir jusqu’à trois bits définis :</span><span class="sxs-lookup"><span data-stu-id="3aa32-107">This constructed attribute returns a single **DWORD** value that can have up to three bits set:</span></span>

-   <span data-ttu-id="3aa32-108">\_informations de sécurité du propriétaire \_</span><span class="sxs-lookup"><span data-stu-id="3aa32-108">OWNER\_SECURITY\_INFORMATION</span></span>
-   <span data-ttu-id="3aa32-109">\_informations de sécurité DACL \_</span><span class="sxs-lookup"><span data-stu-id="3aa32-109">DACL\_SECURITY\_INFORMATION</span></span>
-   <span data-ttu-id="3aa32-110">\_informations de sécurité SACL \_</span><span class="sxs-lookup"><span data-stu-id="3aa32-110">SACL\_SECURITY\_INFORMATION</span></span>

<span data-ttu-id="3aa32-111">Si un bit est défini, l’utilisateur dispose d’un accès en écriture à la partie correspondante du descripteur de sécurité.</span><span class="sxs-lookup"><span data-stu-id="3aa32-111">If a bit is set, then the user has write access to the corresponding part of the security descriptor.</span></span> <span data-ttu-id="3aa32-112">Owner correspond à la fois au propriétaire et au groupe.</span><span class="sxs-lookup"><span data-stu-id="3aa32-112">Owner means both owner and group.</span></span>



| <span data-ttu-id="3aa32-113">Entrée</span><span class="sxs-lookup"><span data-stu-id="3aa32-113">Entry</span></span> | <span data-ttu-id="3aa32-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="3aa32-114">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="3aa32-115">CN</span><span class="sxs-lookup"><span data-stu-id="3aa32-115">CN</span></span>                | <span data-ttu-id="3aa32-116">SD-droits-effectifs</span><span class="sxs-lookup"><span data-stu-id="3aa32-116">SD-Rights-Effective</span></span>                  |
| <span data-ttu-id="3aa32-117">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="3aa32-117">Ldap-Display-Name</span></span> | <span data-ttu-id="3aa32-118">sDRightsEffective</span><span class="sxs-lookup"><span data-stu-id="3aa32-118">sDRightsEffective</span></span>                    |
| <span data-ttu-id="3aa32-119">Taille</span><span class="sxs-lookup"><span data-stu-id="3aa32-119">Size</span></span>              | \-                                   |
| <span data-ttu-id="3aa32-120">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="3aa32-120">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="3aa32-121">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="3aa32-121">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="3aa32-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="3aa32-122">Attribute-Id</span></span>      | <span data-ttu-id="3aa32-123">1.2.840.113556.1.4.1304</span><span class="sxs-lookup"><span data-stu-id="3aa32-123">1.2.840.113556.1.4.1304</span></span>              |
| <span data-ttu-id="3aa32-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="3aa32-124">System-Id-Guid</span></span>    | <span data-ttu-id="3aa32-125">c3dbafa6-33df-11d2-98b2-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="3aa32-125">c3dbafa6-33df-11d2-98b2-0000f87a57d4</span></span> |
| <span data-ttu-id="3aa32-126">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3aa32-126">Syntax</span></span>            | [<span data-ttu-id="3aa32-127">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="3aa32-127">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="3aa32-128">Implémentations</span><span class="sxs-lookup"><span data-stu-id="3aa32-128">Implementations</span></span>

-   [<span data-ttu-id="3aa32-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="3aa32-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="3aa32-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="3aa32-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="3aa32-131">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="3aa32-131">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="3aa32-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="3aa32-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="3aa32-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="3aa32-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="3aa32-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="3aa32-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="3aa32-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3aa32-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="3aa32-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3aa32-136">Windows 2000 Server</span></span>



| <span data-ttu-id="3aa32-137">Entrée</span><span class="sxs-lookup"><span data-stu-id="3aa32-137">Entry</span></span> | <span data-ttu-id="3aa32-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="3aa32-138">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="3aa32-139">ID de lien</span><span class="sxs-lookup"><span data-stu-id="3aa32-139">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="3aa32-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3aa32-140">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="3aa32-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="3aa32-141">System-Only</span></span>            | <span data-ttu-id="3aa32-142">Faux</span><span class="sxs-lookup"><span data-stu-id="3aa32-142">False</span></span>                           |
| <span data-ttu-id="3aa32-143">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="3aa32-143">Is-Single-Valued</span></span>       | <span data-ttu-id="3aa32-144">Vrai</span><span class="sxs-lookup"><span data-stu-id="3aa32-144">True</span></span>                            |
| <span data-ttu-id="3aa32-145">Est indexé</span><span class="sxs-lookup"><span data-stu-id="3aa32-145">Is Indexed</span></span>             | <span data-ttu-id="3aa32-146">Faux</span><span class="sxs-lookup"><span data-stu-id="3aa32-146">False</span></span>                           |
| <span data-ttu-id="3aa32-147">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="3aa32-147">In Global Catalog</span></span>      | <span data-ttu-id="3aa32-148">Faux</span><span class="sxs-lookup"><span data-stu-id="3aa32-148">False</span></span>                           |
| <span data-ttu-id="3aa32-149">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="3aa32-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="3aa32-150">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="3aa32-150">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="3aa32-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3aa32-151">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="3aa32-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3aa32-152">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="3aa32-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3aa32-153">Search-Flags</span></span>           | <span data-ttu-id="3aa32-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3aa32-154">0x00000000</span></span>                      |
| <span data-ttu-id="3aa32-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3aa32-155">System-Flags</span></span>           | <span data-ttu-id="3aa32-156">0x08000014</span><span class="sxs-lookup"><span data-stu-id="3aa32-156">0x08000014</span></span>                      |
| <span data-ttu-id="3aa32-157">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="3aa32-157">Classes used in</span></span>        | [<span data-ttu-id="3aa32-158">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="3aa32-158">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="3aa32-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3aa32-159">Windows Server 2003</span></span>



| <span data-ttu-id="3aa32-160">Entrée</span><span class="sxs-lookup"><span data-stu-id="3aa32-160">Entry</span></span> | <span data-ttu-id="3aa32-161">Valeur</span><span class="sxs-lookup"><span data-stu-id="3aa32-161">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="3aa32-162">ID de lien</span><span class="sxs-lookup"><span data-stu-id="3aa32-162">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="3aa32-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3aa32-163">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="3aa32-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="3aa32-164">System-Only</span></span>            | <span data-ttu-id="3aa32-165">Faux</span><span class="sxs-lookup"><span data-stu-id="3aa32-165">False</span></span>                           |
| <span data-ttu-id="3aa32-166">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="3aa32-166">Is-Single-Valued</span></span>       | <span data-ttu-id="3aa32-167">Vrai</span><span class="sxs-lookup"><span data-stu-id="3aa32-167">True</span></span>                            |
| <span data-ttu-id="3aa32-168">Est indexé</span><span class="sxs-lookup"><span data-stu-id="3aa32-168">Is Indexed</span></span>             | <span data-ttu-id="3aa32-169">Faux</span><span class="sxs-lookup"><span data-stu-id="3aa32-169">False</span></span>                           |
| <span data-ttu-id="3aa32-170">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="3aa32-170">In Global Catalog</span></span>      | <span data-ttu-id="3aa32-171">Faux</span><span class="sxs-lookup"><span data-stu-id="3aa32-171">False</span></span>                           |
| <span data-ttu-id="3aa32-172">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="3aa32-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="3aa32-173">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="3aa32-173">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="3aa32-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3aa32-174">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="3aa32-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3aa32-175">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="3aa32-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3aa32-176">Search-Flags</span></span>           | <span data-ttu-id="3aa32-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3aa32-177">0x00000000</span></span>                      |
| <span data-ttu-id="3aa32-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3aa32-178">System-Flags</span></span>           | <span data-ttu-id="3aa32-179">0x08000014</span><span class="sxs-lookup"><span data-stu-id="3aa32-179">0x08000014</span></span>                      |
| <span data-ttu-id="3aa32-180">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="3aa32-180">Classes used in</span></span>        | [<span data-ttu-id="3aa32-181">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="3aa32-181">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="3aa32-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="3aa32-182">ADAM</span></span>



| <span data-ttu-id="3aa32-183">Entrée</span><span class="sxs-lookup"><span data-stu-id="3aa32-183">Entry</span></span> | <span data-ttu-id="3aa32-184">Valeur</span><span class="sxs-lookup"><span data-stu-id="3aa32-184">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="3aa32-185">ID de lien</span><span class="sxs-lookup"><span data-stu-id="3aa32-185">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="3aa32-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3aa32-186">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="3aa32-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="3aa32-187">System-Only</span></span>            | <span data-ttu-id="3aa32-188">Faux</span><span class="sxs-lookup"><span data-stu-id="3aa32-188">False</span></span>                           |
| <span data-ttu-id="3aa32-189">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="3aa32-189">Is-Single-Valued</span></span>       | <span data-ttu-id="3aa32-190">Vrai</span><span class="sxs-lookup"><span data-stu-id="3aa32-190">True</span></span>                            |
| <span data-ttu-id="3aa32-191">Est indexé</span><span class="sxs-lookup"><span data-stu-id="3aa32-191">Is Indexed</span></span>             | <span data-ttu-id="3aa32-192">Faux</span><span class="sxs-lookup"><span data-stu-id="3aa32-192">False</span></span>                           |
| <span data-ttu-id="3aa32-193">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="3aa32-193">In Global Catalog</span></span>      | <span data-ttu-id="3aa32-194">Faux</span><span class="sxs-lookup"><span data-stu-id="3aa32-194">False</span></span>                           |
| <span data-ttu-id="3aa32-195">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="3aa32-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="3aa32-196">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="3aa32-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="3aa32-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3aa32-197">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="3aa32-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3aa32-198">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="3aa32-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3aa32-199">Search-Flags</span></span>           | <span data-ttu-id="3aa32-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3aa32-200">0x00000000</span></span>                      |
| <span data-ttu-id="3aa32-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3aa32-201">System-Flags</span></span>           | <span data-ttu-id="3aa32-202">0x08000014</span><span class="sxs-lookup"><span data-stu-id="3aa32-202">0x08000014</span></span>                      |
| <span data-ttu-id="3aa32-203">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="3aa32-203">Classes used in</span></span>        | [<span data-ttu-id="3aa32-204">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="3aa32-204">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="3aa32-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="3aa32-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="3aa32-206">Entrée</span><span class="sxs-lookup"><span data-stu-id="3aa32-206">Entry</span></span> | <span data-ttu-id="3aa32-207">Valeur</span><span class="sxs-lookup"><span data-stu-id="3aa32-207">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="3aa32-208">ID de lien</span><span class="sxs-lookup"><span data-stu-id="3aa32-208">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="3aa32-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3aa32-209">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="3aa32-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="3aa32-210">System-Only</span></span>            | <span data-ttu-id="3aa32-211">Faux</span><span class="sxs-lookup"><span data-stu-id="3aa32-211">False</span></span>                           |
| <span data-ttu-id="3aa32-212">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="3aa32-212">Is-Single-Valued</span></span>       | <span data-ttu-id="3aa32-213">Vrai</span><span class="sxs-lookup"><span data-stu-id="3aa32-213">True</span></span>                            |
| <span data-ttu-id="3aa32-214">Est indexé</span><span class="sxs-lookup"><span data-stu-id="3aa32-214">Is Indexed</span></span>             | <span data-ttu-id="3aa32-215">Faux</span><span class="sxs-lookup"><span data-stu-id="3aa32-215">False</span></span>                           |
| <span data-ttu-id="3aa32-216">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="3aa32-216">In Global Catalog</span></span>      | <span data-ttu-id="3aa32-217">Faux</span><span class="sxs-lookup"><span data-stu-id="3aa32-217">False</span></span>                           |
| <span data-ttu-id="3aa32-218">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="3aa32-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="3aa32-219">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="3aa32-219">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="3aa32-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3aa32-220">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="3aa32-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3aa32-221">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="3aa32-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3aa32-222">Search-Flags</span></span>           | <span data-ttu-id="3aa32-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3aa32-223">0x00000000</span></span>                      |
| <span data-ttu-id="3aa32-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3aa32-224">System-Flags</span></span>           | <span data-ttu-id="3aa32-225">0x08000014</span><span class="sxs-lookup"><span data-stu-id="3aa32-225">0x08000014</span></span>                      |
| <span data-ttu-id="3aa32-226">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="3aa32-226">Classes used in</span></span>        | [<span data-ttu-id="3aa32-227">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="3aa32-227">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="3aa32-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3aa32-228">Windows Server 2008</span></span>



| <span data-ttu-id="3aa32-229">Entrée</span><span class="sxs-lookup"><span data-stu-id="3aa32-229">Entry</span></span> | <span data-ttu-id="3aa32-230">Valeur</span><span class="sxs-lookup"><span data-stu-id="3aa32-230">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="3aa32-231">ID de lien</span><span class="sxs-lookup"><span data-stu-id="3aa32-231">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="3aa32-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3aa32-232">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="3aa32-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="3aa32-233">System-Only</span></span>            | <span data-ttu-id="3aa32-234">Faux</span><span class="sxs-lookup"><span data-stu-id="3aa32-234">False</span></span>                           |
| <span data-ttu-id="3aa32-235">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="3aa32-235">Is-Single-Valued</span></span>       | <span data-ttu-id="3aa32-236">Vrai</span><span class="sxs-lookup"><span data-stu-id="3aa32-236">True</span></span>                            |
| <span data-ttu-id="3aa32-237">Est indexé</span><span class="sxs-lookup"><span data-stu-id="3aa32-237">Is Indexed</span></span>             | <span data-ttu-id="3aa32-238">Faux</span><span class="sxs-lookup"><span data-stu-id="3aa32-238">False</span></span>                           |
| <span data-ttu-id="3aa32-239">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="3aa32-239">In Global Catalog</span></span>      | <span data-ttu-id="3aa32-240">Faux</span><span class="sxs-lookup"><span data-stu-id="3aa32-240">False</span></span>                           |
| <span data-ttu-id="3aa32-241">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="3aa32-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="3aa32-242">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="3aa32-242">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="3aa32-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3aa32-243">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="3aa32-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3aa32-244">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="3aa32-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3aa32-245">Search-Flags</span></span>           | <span data-ttu-id="3aa32-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3aa32-246">0x00000000</span></span>                      |
| <span data-ttu-id="3aa32-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3aa32-247">System-Flags</span></span>           | <span data-ttu-id="3aa32-248">0x08000014</span><span class="sxs-lookup"><span data-stu-id="3aa32-248">0x08000014</span></span>                      |
| <span data-ttu-id="3aa32-249">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="3aa32-249">Classes used in</span></span>        | [<span data-ttu-id="3aa32-250">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="3aa32-250">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="3aa32-251">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3aa32-251">Windows Server 2008 R2</span></span>



| <span data-ttu-id="3aa32-252">Entrée</span><span class="sxs-lookup"><span data-stu-id="3aa32-252">Entry</span></span> | <span data-ttu-id="3aa32-253">Valeur</span><span class="sxs-lookup"><span data-stu-id="3aa32-253">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="3aa32-254">ID de lien</span><span class="sxs-lookup"><span data-stu-id="3aa32-254">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="3aa32-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3aa32-255">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="3aa32-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="3aa32-256">System-Only</span></span>            | <span data-ttu-id="3aa32-257">Faux</span><span class="sxs-lookup"><span data-stu-id="3aa32-257">False</span></span>                           |
| <span data-ttu-id="3aa32-258">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="3aa32-258">Is-Single-Valued</span></span>       | <span data-ttu-id="3aa32-259">Vrai</span><span class="sxs-lookup"><span data-stu-id="3aa32-259">True</span></span>                            |
| <span data-ttu-id="3aa32-260">Est indexé</span><span class="sxs-lookup"><span data-stu-id="3aa32-260">Is Indexed</span></span>             | <span data-ttu-id="3aa32-261">Faux</span><span class="sxs-lookup"><span data-stu-id="3aa32-261">False</span></span>                           |
| <span data-ttu-id="3aa32-262">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="3aa32-262">In Global Catalog</span></span>      | <span data-ttu-id="3aa32-263">Faux</span><span class="sxs-lookup"><span data-stu-id="3aa32-263">False</span></span>                           |
| <span data-ttu-id="3aa32-264">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="3aa32-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="3aa32-265">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="3aa32-265">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="3aa32-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3aa32-266">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="3aa32-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3aa32-267">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="3aa32-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3aa32-268">Search-Flags</span></span>           | <span data-ttu-id="3aa32-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3aa32-269">0x00000000</span></span>                      |
| <span data-ttu-id="3aa32-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3aa32-270">System-Flags</span></span>           | <span data-ttu-id="3aa32-271">0x08000014</span><span class="sxs-lookup"><span data-stu-id="3aa32-271">0x08000014</span></span>                      |
| <span data-ttu-id="3aa32-272">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="3aa32-272">Classes used in</span></span>        | [<span data-ttu-id="3aa32-273">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="3aa32-273">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="3aa32-274">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3aa32-274">Windows Server 2012</span></span>



| <span data-ttu-id="3aa32-275">Entrée</span><span class="sxs-lookup"><span data-stu-id="3aa32-275">Entry</span></span> | <span data-ttu-id="3aa32-276">Valeur</span><span class="sxs-lookup"><span data-stu-id="3aa32-276">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="3aa32-277">ID de lien</span><span class="sxs-lookup"><span data-stu-id="3aa32-277">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="3aa32-278">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3aa32-278">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="3aa32-279">System-Only</span><span class="sxs-lookup"><span data-stu-id="3aa32-279">System-Only</span></span>            | <span data-ttu-id="3aa32-280">Faux</span><span class="sxs-lookup"><span data-stu-id="3aa32-280">False</span></span>                           |
| <span data-ttu-id="3aa32-281">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="3aa32-281">Is-Single-Valued</span></span>       | <span data-ttu-id="3aa32-282">Vrai</span><span class="sxs-lookup"><span data-stu-id="3aa32-282">True</span></span>                            |
| <span data-ttu-id="3aa32-283">Est indexé</span><span class="sxs-lookup"><span data-stu-id="3aa32-283">Is Indexed</span></span>             | <span data-ttu-id="3aa32-284">Faux</span><span class="sxs-lookup"><span data-stu-id="3aa32-284">False</span></span>                           |
| <span data-ttu-id="3aa32-285">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="3aa32-285">In Global Catalog</span></span>      | <span data-ttu-id="3aa32-286">Faux</span><span class="sxs-lookup"><span data-stu-id="3aa32-286">False</span></span>                           |
| <span data-ttu-id="3aa32-287">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="3aa32-287">NT-Security-Descriptor</span></span> | <span data-ttu-id="3aa32-288">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="3aa32-288">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="3aa32-289">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3aa32-289">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="3aa32-290">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3aa32-290">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="3aa32-291">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3aa32-291">Search-Flags</span></span>           | <span data-ttu-id="3aa32-292">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3aa32-292">0x00000000</span></span>                      |
| <span data-ttu-id="3aa32-293">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3aa32-293">System-Flags</span></span>           | <span data-ttu-id="3aa32-294">0x08000014</span><span class="sxs-lookup"><span data-stu-id="3aa32-294">0x08000014</span></span>                      |
| <span data-ttu-id="3aa32-295">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="3aa32-295">Classes used in</span></span>        | [<span data-ttu-id="3aa32-296">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="3aa32-296">**Top**</span></span>](c-top.md)<br/> |



 

 





