---
title: attribut ms-DS-is-Domain-pour
description: Lien vers l’arrière pour ms-DS-has-Domain-NC. Identifie les contrôleurs de domaine qui détiennent cette partition en tant que domaine principal. | attribut ms-DS-is-Domain-pour
ms.assetid: ec63ddb4-c220-492b-92ce-e3da2069bcb8
ms.tgt_platform: multiple
keywords:
- Schéma AD ms-DS-is-Domain-pour Attribute
- Schéma Active Directory de l’attribut msDS-IsDomainFor
topic_type:
- apiref
api_name:
- ms-DS-Is-Domain-For
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56529497eb8081f53310e26b834194cdcdc11bf5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106527271"
---
# <a name="ms-ds-is-domain-for-attribute"></a><span data-ttu-id="a8095-107">attribut ms-DS-is-Domain-pour</span><span class="sxs-lookup"><span data-stu-id="a8095-107">ms-DS-Is-Domain-For attribute</span></span>

<span data-ttu-id="a8095-108">Lien vers l’arrière pour [**ms-DS-has-Domain-NC**](a-msds-hasdomainncs.md).</span><span class="sxs-lookup"><span data-stu-id="a8095-108">Backward link for [**ms-DS-Has-Domain-NCs**](a-msds-hasdomainncs.md).</span></span> <span data-ttu-id="a8095-109">Identifie les contrôleurs de domaine qui détiennent cette partition en tant que domaine principal.</span><span class="sxs-lookup"><span data-stu-id="a8095-109">Identifies which DCs hold that partition as their primary domain.</span></span>



| <span data-ttu-id="a8095-110">Entrée</span><span class="sxs-lookup"><span data-stu-id="a8095-110">Entry</span></span> | <span data-ttu-id="a8095-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="a8095-111">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="a8095-112">CN</span><span class="sxs-lookup"><span data-stu-id="a8095-112">CN</span></span>                | <span data-ttu-id="a8095-113">ms-DS-est-domain-pour</span><span class="sxs-lookup"><span data-stu-id="a8095-113">ms-DS-Is-Domain-For</span></span>                     |
| <span data-ttu-id="a8095-114">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="a8095-114">Ldap-Display-Name</span></span> | <span data-ttu-id="a8095-115">msDS-IsDomainFor</span><span class="sxs-lookup"><span data-stu-id="a8095-115">msDS-IsDomainFor</span></span>                        |
| <span data-ttu-id="a8095-116">Taille</span><span class="sxs-lookup"><span data-stu-id="a8095-116">Size</span></span>              | \-                                      |
| <span data-ttu-id="a8095-117">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="a8095-117">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="a8095-118">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="a8095-118">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="a8095-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a8095-119">Attribute-Id</span></span>      | <span data-ttu-id="a8095-120">1.2.840.113556.1.4.1933</span><span class="sxs-lookup"><span data-stu-id="a8095-120">1.2.840.113556.1.4.1933</span></span>                 |
| <span data-ttu-id="a8095-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a8095-121">System-Id-Guid</span></span>    | <span data-ttu-id="a8095-122">ff155a2a-44e5-4de0-8318-13a58988de4f</span><span class="sxs-lookup"><span data-stu-id="a8095-122">ff155a2a-44e5-4de0-8318-13a58988de4f</span></span>    |
| <span data-ttu-id="a8095-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a8095-123">Syntax</span></span>            | [<span data-ttu-id="a8095-124">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="a8095-124">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="a8095-125">Implémentations</span><span class="sxs-lookup"><span data-stu-id="a8095-125">Implementations</span></span>

-   [<span data-ttu-id="a8095-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a8095-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a8095-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a8095-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a8095-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a8095-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="a8095-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a8095-129">Windows Server 2008</span></span>



| <span data-ttu-id="a8095-130">Entrée</span><span class="sxs-lookup"><span data-stu-id="a8095-130">Entry</span></span> | <span data-ttu-id="a8095-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="a8095-131">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a8095-132">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a8095-132">Link-Id</span></span>                | <span data-ttu-id="a8095-133">2027</span><span class="sxs-lookup"><span data-stu-id="a8095-133">2027</span></span>                            |
| <span data-ttu-id="a8095-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a8095-134">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="a8095-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="a8095-135">System-Only</span></span>            | <span data-ttu-id="a8095-136">Vrai</span><span class="sxs-lookup"><span data-stu-id="a8095-136">True</span></span>                            |
| <span data-ttu-id="a8095-137">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a8095-137">Is-Single-Valued</span></span>       | <span data-ttu-id="a8095-138">Faux</span><span class="sxs-lookup"><span data-stu-id="a8095-138">False</span></span>                           |
| <span data-ttu-id="a8095-139">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a8095-139">Is Indexed</span></span>             | <span data-ttu-id="a8095-140">Faux</span><span class="sxs-lookup"><span data-stu-id="a8095-140">False</span></span>                           |
| <span data-ttu-id="a8095-141">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a8095-141">In Global Catalog</span></span>      | <span data-ttu-id="a8095-142">Faux</span><span class="sxs-lookup"><span data-stu-id="a8095-142">False</span></span>                           |
| <span data-ttu-id="a8095-143">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a8095-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="a8095-144">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a8095-144">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a8095-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a8095-145">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a8095-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a8095-146">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a8095-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a8095-147">Search-Flags</span></span>           | <span data-ttu-id="a8095-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a8095-148">0x00000000</span></span>                      |
| <span data-ttu-id="a8095-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a8095-149">System-Flags</span></span>           | <span data-ttu-id="a8095-150">0x00000011</span><span class="sxs-lookup"><span data-stu-id="a8095-150">0x00000011</span></span>                      |
| <span data-ttu-id="a8095-151">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a8095-151">Classes used in</span></span>        | [<span data-ttu-id="a8095-152">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="a8095-152">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a8095-153">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a8095-153">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a8095-154">Entrée</span><span class="sxs-lookup"><span data-stu-id="a8095-154">Entry</span></span> | <span data-ttu-id="a8095-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="a8095-155">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a8095-156">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a8095-156">Link-Id</span></span>                | <span data-ttu-id="a8095-157">2027</span><span class="sxs-lookup"><span data-stu-id="a8095-157">2027</span></span>                            |
| <span data-ttu-id="a8095-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a8095-158">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="a8095-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="a8095-159">System-Only</span></span>            | <span data-ttu-id="a8095-160">Vrai</span><span class="sxs-lookup"><span data-stu-id="a8095-160">True</span></span>                            |
| <span data-ttu-id="a8095-161">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a8095-161">Is-Single-Valued</span></span>       | <span data-ttu-id="a8095-162">Faux</span><span class="sxs-lookup"><span data-stu-id="a8095-162">False</span></span>                           |
| <span data-ttu-id="a8095-163">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a8095-163">Is Indexed</span></span>             | <span data-ttu-id="a8095-164">Faux</span><span class="sxs-lookup"><span data-stu-id="a8095-164">False</span></span>                           |
| <span data-ttu-id="a8095-165">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a8095-165">In Global Catalog</span></span>      | <span data-ttu-id="a8095-166">Faux</span><span class="sxs-lookup"><span data-stu-id="a8095-166">False</span></span>                           |
| <span data-ttu-id="a8095-167">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a8095-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="a8095-168">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a8095-168">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a8095-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a8095-169">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a8095-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a8095-170">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a8095-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a8095-171">Search-Flags</span></span>           | <span data-ttu-id="a8095-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a8095-172">0x00000000</span></span>                      |
| <span data-ttu-id="a8095-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a8095-173">System-Flags</span></span>           | <span data-ttu-id="a8095-174">0x00000011</span><span class="sxs-lookup"><span data-stu-id="a8095-174">0x00000011</span></span>                      |
| <span data-ttu-id="a8095-175">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a8095-175">Classes used in</span></span>        | [<span data-ttu-id="a8095-176">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="a8095-176">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a8095-177">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a8095-177">Windows Server 2012</span></span>



| <span data-ttu-id="a8095-178">Entrée</span><span class="sxs-lookup"><span data-stu-id="a8095-178">Entry</span></span> | <span data-ttu-id="a8095-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="a8095-179">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a8095-180">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a8095-180">Link-Id</span></span>                | <span data-ttu-id="a8095-181">2027</span><span class="sxs-lookup"><span data-stu-id="a8095-181">2027</span></span>                            |
| <span data-ttu-id="a8095-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a8095-182">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="a8095-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="a8095-183">System-Only</span></span>            | <span data-ttu-id="a8095-184">Vrai</span><span class="sxs-lookup"><span data-stu-id="a8095-184">True</span></span>                            |
| <span data-ttu-id="a8095-185">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a8095-185">Is-Single-Valued</span></span>       | <span data-ttu-id="a8095-186">Faux</span><span class="sxs-lookup"><span data-stu-id="a8095-186">False</span></span>                           |
| <span data-ttu-id="a8095-187">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a8095-187">Is Indexed</span></span>             | <span data-ttu-id="a8095-188">Faux</span><span class="sxs-lookup"><span data-stu-id="a8095-188">False</span></span>                           |
| <span data-ttu-id="a8095-189">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a8095-189">In Global Catalog</span></span>      | <span data-ttu-id="a8095-190">Faux</span><span class="sxs-lookup"><span data-stu-id="a8095-190">False</span></span>                           |
| <span data-ttu-id="a8095-191">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a8095-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="a8095-192">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a8095-192">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a8095-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a8095-193">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a8095-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a8095-194">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a8095-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a8095-195">Search-Flags</span></span>           | <span data-ttu-id="a8095-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a8095-196">0x00000000</span></span>                      |
| <span data-ttu-id="a8095-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a8095-197">System-Flags</span></span>           | <span data-ttu-id="a8095-198">0x00000011</span><span class="sxs-lookup"><span data-stu-id="a8095-198">0x00000011</span></span>                      |
| <span data-ttu-id="a8095-199">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a8095-199">Classes used in</span></span>        | [<span data-ttu-id="a8095-200">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="a8095-200">**Top**</span></span>](c-top.md)<br/> |



 

 





