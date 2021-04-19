---
title: Attribut Lockout-Duration
description: Durée de verrouillage d’un compte en raison du dépassement de la Lockout-Threshold.
ms.assetid: 6a26ef80-86ed-433f-9032-cdd1aaf00388
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Lockout-Duration
- Schéma AD de l’attribut lockoutDuration
topic_type:
- apiref
api_name:
- Lockout-Duration
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 526fedef47bea20148a591259dbc7ec1702b5a15
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106509956"
---
# <a name="lockout-duration-attribute"></a><span data-ttu-id="c234f-105">Attribut Lockout-Duration</span><span class="sxs-lookup"><span data-stu-id="c234f-105">Lockout-Duration attribute</span></span>

<span data-ttu-id="c234f-106">Durée de verrouillage d’un compte en raison du dépassement du [**seuil de verrouillage**](a-lockoutthreshold.md) .</span><span class="sxs-lookup"><span data-stu-id="c234f-106">The amount of time that an account is locked due to the [**Lockout-Threshold**](a-lockoutthreshold.md) being exceeded.</span></span> <span data-ttu-id="c234f-107">Cette valeur est stockée sous la forme d’un entier long qui représente la valeur négative du nombre d’intervalles de 100 nanosecondes à partir du moment où le [**seuil de verrouillage**](a-lockoutthreshold.md) est dépassé avant le déverrouillage du compte.</span><span class="sxs-lookup"><span data-stu-id="c234f-107">This value is stored as a large integer that represents the negative of the number of 100-nanosecond intervals from the time the [**Lockout-Threshold**](a-lockoutthreshold.md) is exceeded that must elapse before the account is unlocked.</span></span>



| <span data-ttu-id="c234f-108">Entrée</span><span class="sxs-lookup"><span data-stu-id="c234f-108">Entry</span></span> | <span data-ttu-id="c234f-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="c234f-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="c234f-110">CN</span><span class="sxs-lookup"><span data-stu-id="c234f-110">CN</span></span>                | <span data-ttu-id="c234f-111">Lockout-Duration</span><span class="sxs-lookup"><span data-stu-id="c234f-111">Lockout-Duration</span></span>                     |
| <span data-ttu-id="c234f-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="c234f-112">Ldap-Display-Name</span></span> | <span data-ttu-id="c234f-113">lockoutDuration</span><span class="sxs-lookup"><span data-stu-id="c234f-113">lockoutDuration</span></span>                      |
| <span data-ttu-id="c234f-114">Taille</span><span class="sxs-lookup"><span data-stu-id="c234f-114">Size</span></span>              | \-                                   |
| <span data-ttu-id="c234f-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="c234f-115">Update Privilege</span></span>  | <span data-ttu-id="c234f-116">Administrateur de domaine</span><span class="sxs-lookup"><span data-stu-id="c234f-116">Domain administrator</span></span>                 |
| <span data-ttu-id="c234f-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="c234f-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="c234f-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c234f-118">Attribute-Id</span></span>      | <span data-ttu-id="c234f-119">1.2.840.113556.1.4.60</span><span class="sxs-lookup"><span data-stu-id="c234f-119">1.2.840.113556.1.4.60</span></span>                |
| <span data-ttu-id="c234f-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c234f-120">System-Id-Guid</span></span>    | <span data-ttu-id="c234f-121">bf9679a5-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="c234f-121">bf9679a5-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="c234f-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c234f-122">Syntax</span></span>            | [<span data-ttu-id="c234f-123">**Défini**</span><span class="sxs-lookup"><span data-stu-id="c234f-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="c234f-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="c234f-124">Implementations</span></span>

-   [<span data-ttu-id="c234f-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c234f-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c234f-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c234f-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c234f-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c234f-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c234f-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c234f-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c234f-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c234f-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c234f-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c234f-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c234f-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c234f-131">Windows 2000 Server</span></span>



| <span data-ttu-id="c234f-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="c234f-132">Entry</span></span> | <span data-ttu-id="c234f-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="c234f-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c234f-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c234f-134">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="c234f-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c234f-135">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="c234f-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="c234f-136">System-Only</span></span>            | <span data-ttu-id="c234f-137">Faux</span><span class="sxs-lookup"><span data-stu-id="c234f-137">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="c234f-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c234f-138">Is-Single-Valued</span></span>       | <span data-ttu-id="c234f-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="c234f-139">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="c234f-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c234f-140">Is Indexed</span></span>             | <span data-ttu-id="c234f-141">Faux</span><span class="sxs-lookup"><span data-stu-id="c234f-141">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="c234f-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c234f-142">In Global Catalog</span></span>      | <span data-ttu-id="c234f-143">Faux</span><span class="sxs-lookup"><span data-stu-id="c234f-143">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="c234f-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c234f-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="c234f-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c234f-145">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="c234f-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c234f-146">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="c234f-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c234f-147">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="c234f-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c234f-148">Search-Flags</span></span>           | <span data-ttu-id="c234f-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c234f-149">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="c234f-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c234f-150">System-Flags</span></span>           | <span data-ttu-id="c234f-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c234f-151">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="c234f-152">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c234f-152">Classes used in</span></span>        | [<span data-ttu-id="c234f-153">**Stratégie de domaine**</span><span class="sxs-lookup"><span data-stu-id="c234f-153">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="c234f-154">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="c234f-154">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="c234f-155">**Sam-domaine-base**</span><span class="sxs-lookup"><span data-stu-id="c234f-155">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c234f-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c234f-156">Windows Server 2003</span></span>



| <span data-ttu-id="c234f-157">Entrée</span><span class="sxs-lookup"><span data-stu-id="c234f-157">Entry</span></span> | <span data-ttu-id="c234f-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="c234f-158">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c234f-159">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c234f-159">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="c234f-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c234f-160">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="c234f-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="c234f-161">System-Only</span></span>            | <span data-ttu-id="c234f-162">Faux</span><span class="sxs-lookup"><span data-stu-id="c234f-162">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="c234f-163">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c234f-163">Is-Single-Valued</span></span>       | <span data-ttu-id="c234f-164">Vrai</span><span class="sxs-lookup"><span data-stu-id="c234f-164">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="c234f-165">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c234f-165">Is Indexed</span></span>             | <span data-ttu-id="c234f-166">Faux</span><span class="sxs-lookup"><span data-stu-id="c234f-166">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="c234f-167">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c234f-167">In Global Catalog</span></span>      | <span data-ttu-id="c234f-168">Faux</span><span class="sxs-lookup"><span data-stu-id="c234f-168">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="c234f-169">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c234f-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="c234f-170">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c234f-170">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="c234f-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c234f-171">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="c234f-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c234f-172">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="c234f-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c234f-173">Search-Flags</span></span>           | <span data-ttu-id="c234f-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c234f-174">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="c234f-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c234f-175">System-Flags</span></span>           | <span data-ttu-id="c234f-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c234f-176">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="c234f-177">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c234f-177">Classes used in</span></span>        | [<span data-ttu-id="c234f-178">**Stratégie de domaine**</span><span class="sxs-lookup"><span data-stu-id="c234f-178">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="c234f-179">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="c234f-179">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="c234f-180">**Sam-domaine-base**</span><span class="sxs-lookup"><span data-stu-id="c234f-180">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c234f-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c234f-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c234f-182">Entrée</span><span class="sxs-lookup"><span data-stu-id="c234f-182">Entry</span></span> | <span data-ttu-id="c234f-183">Valeur</span><span class="sxs-lookup"><span data-stu-id="c234f-183">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c234f-184">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c234f-184">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="c234f-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c234f-185">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="c234f-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="c234f-186">System-Only</span></span>            | <span data-ttu-id="c234f-187">Faux</span><span class="sxs-lookup"><span data-stu-id="c234f-187">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="c234f-188">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c234f-188">Is-Single-Valued</span></span>       | <span data-ttu-id="c234f-189">Vrai</span><span class="sxs-lookup"><span data-stu-id="c234f-189">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="c234f-190">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c234f-190">Is Indexed</span></span>             | <span data-ttu-id="c234f-191">Faux</span><span class="sxs-lookup"><span data-stu-id="c234f-191">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="c234f-192">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c234f-192">In Global Catalog</span></span>      | <span data-ttu-id="c234f-193">Faux</span><span class="sxs-lookup"><span data-stu-id="c234f-193">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="c234f-194">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c234f-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="c234f-195">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c234f-195">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="c234f-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c234f-196">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="c234f-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c234f-197">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="c234f-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c234f-198">Search-Flags</span></span>           | <span data-ttu-id="c234f-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c234f-199">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="c234f-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c234f-200">System-Flags</span></span>           | <span data-ttu-id="c234f-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c234f-201">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="c234f-202">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c234f-202">Classes used in</span></span>        | [<span data-ttu-id="c234f-203">**Stratégie de domaine**</span><span class="sxs-lookup"><span data-stu-id="c234f-203">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="c234f-204">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="c234f-204">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="c234f-205">**Sam-domaine-base**</span><span class="sxs-lookup"><span data-stu-id="c234f-205">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c234f-206">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c234f-206">Windows Server 2008</span></span>



| <span data-ttu-id="c234f-207">Entrée</span><span class="sxs-lookup"><span data-stu-id="c234f-207">Entry</span></span> | <span data-ttu-id="c234f-208">Valeur</span><span class="sxs-lookup"><span data-stu-id="c234f-208">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c234f-209">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c234f-209">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="c234f-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c234f-210">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="c234f-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="c234f-211">System-Only</span></span>            | <span data-ttu-id="c234f-212">Faux</span><span class="sxs-lookup"><span data-stu-id="c234f-212">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="c234f-213">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c234f-213">Is-Single-Valued</span></span>       | <span data-ttu-id="c234f-214">Vrai</span><span class="sxs-lookup"><span data-stu-id="c234f-214">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="c234f-215">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c234f-215">Is Indexed</span></span>             | <span data-ttu-id="c234f-216">Faux</span><span class="sxs-lookup"><span data-stu-id="c234f-216">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="c234f-217">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c234f-217">In Global Catalog</span></span>      | <span data-ttu-id="c234f-218">Faux</span><span class="sxs-lookup"><span data-stu-id="c234f-218">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="c234f-219">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c234f-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="c234f-220">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c234f-220">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="c234f-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c234f-221">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="c234f-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c234f-222">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="c234f-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c234f-223">Search-Flags</span></span>           | <span data-ttu-id="c234f-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c234f-224">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="c234f-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c234f-225">System-Flags</span></span>           | <span data-ttu-id="c234f-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c234f-226">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="c234f-227">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c234f-227">Classes used in</span></span>        | [<span data-ttu-id="c234f-228">**Stratégie de domaine**</span><span class="sxs-lookup"><span data-stu-id="c234f-228">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="c234f-229">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="c234f-229">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="c234f-230">**Sam-domaine-base**</span><span class="sxs-lookup"><span data-stu-id="c234f-230">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c234f-231">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c234f-231">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c234f-232">Entrée</span><span class="sxs-lookup"><span data-stu-id="c234f-232">Entry</span></span> | <span data-ttu-id="c234f-233">Valeur</span><span class="sxs-lookup"><span data-stu-id="c234f-233">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c234f-234">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c234f-234">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="c234f-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c234f-235">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="c234f-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="c234f-236">System-Only</span></span>            | <span data-ttu-id="c234f-237">Faux</span><span class="sxs-lookup"><span data-stu-id="c234f-237">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="c234f-238">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c234f-238">Is-Single-Valued</span></span>       | <span data-ttu-id="c234f-239">Vrai</span><span class="sxs-lookup"><span data-stu-id="c234f-239">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="c234f-240">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c234f-240">Is Indexed</span></span>             | <span data-ttu-id="c234f-241">Faux</span><span class="sxs-lookup"><span data-stu-id="c234f-241">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="c234f-242">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c234f-242">In Global Catalog</span></span>      | <span data-ttu-id="c234f-243">Faux</span><span class="sxs-lookup"><span data-stu-id="c234f-243">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="c234f-244">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c234f-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="c234f-245">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c234f-245">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="c234f-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c234f-246">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="c234f-247">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c234f-247">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="c234f-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c234f-248">Search-Flags</span></span>           | <span data-ttu-id="c234f-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c234f-249">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="c234f-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c234f-250">System-Flags</span></span>           | <span data-ttu-id="c234f-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c234f-251">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="c234f-252">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c234f-252">Classes used in</span></span>        | [<span data-ttu-id="c234f-253">**Stratégie de domaine**</span><span class="sxs-lookup"><span data-stu-id="c234f-253">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="c234f-254">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="c234f-254">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="c234f-255">**Sam-domaine-base**</span><span class="sxs-lookup"><span data-stu-id="c234f-255">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c234f-256">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c234f-256">Windows Server 2012</span></span>



| <span data-ttu-id="c234f-257">Entrée</span><span class="sxs-lookup"><span data-stu-id="c234f-257">Entry</span></span> | <span data-ttu-id="c234f-258">Valeur</span><span class="sxs-lookup"><span data-stu-id="c234f-258">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c234f-259">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c234f-259">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="c234f-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c234f-260">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="c234f-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="c234f-261">System-Only</span></span>            | <span data-ttu-id="c234f-262">Faux</span><span class="sxs-lookup"><span data-stu-id="c234f-262">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="c234f-263">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c234f-263">Is-Single-Valued</span></span>       | <span data-ttu-id="c234f-264">Vrai</span><span class="sxs-lookup"><span data-stu-id="c234f-264">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="c234f-265">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c234f-265">Is Indexed</span></span>             | <span data-ttu-id="c234f-266">Faux</span><span class="sxs-lookup"><span data-stu-id="c234f-266">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="c234f-267">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c234f-267">In Global Catalog</span></span>      | <span data-ttu-id="c234f-268">Faux</span><span class="sxs-lookup"><span data-stu-id="c234f-268">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="c234f-269">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c234f-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="c234f-270">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c234f-270">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="c234f-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c234f-271">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="c234f-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c234f-272">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="c234f-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c234f-273">Search-Flags</span></span>           | <span data-ttu-id="c234f-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c234f-274">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="c234f-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c234f-275">System-Flags</span></span>           | <span data-ttu-id="c234f-276">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c234f-276">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="c234f-277">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c234f-277">Classes used in</span></span>        | [<span data-ttu-id="c234f-278">**Stratégie de domaine**</span><span class="sxs-lookup"><span data-stu-id="c234f-278">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="c234f-279">**Sam-domaine**</span><span class="sxs-lookup"><span data-stu-id="c234f-279">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="c234f-280">**Sam-domaine-base**</span><span class="sxs-lookup"><span data-stu-id="c234f-280">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="see-also"></a><span data-ttu-id="c234f-281">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c234f-281">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c234f-282">**Seuil de verrouillage**</span><span class="sxs-lookup"><span data-stu-id="c234f-282">**Lockout-Threshold**</span></span>](a-lockoutthreshold.md)
</dt> </dl>

 

 





