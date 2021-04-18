---
title: attribut ms-DS-Never-Reveal-Group
description: Utilisé avec les RODC pour définir les utilisateurs, les ordinateurs et les groupes qui ne sont pas autorisés à mettre en cache leurs mots de passe sur un contrôleur de domaine en lecture seule.
ms.assetid: 203a660b-503e-4cf1-a796-eac024629b3e
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut de groupe ms-DS-ne jamais révéler
- Schéma Active Directory de l’attribut msDS-NeverRevealGroup
topic_type:
- apiref
api_name:
- ms-DS-Never-Reveal-Group
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1308fb1bc0818601a037e66b764e607c0a32532
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106529088"
---
# <a name="ms-ds-never-reveal-group-attribute"></a><span data-ttu-id="bbc5c-105">attribut ms-DS-Never-Reveal-Group</span><span class="sxs-lookup"><span data-stu-id="bbc5c-105">ms-DS-Never-Reveal-Group attribute</span></span>

<span data-ttu-id="bbc5c-106">Utilisé avec les RODC pour définir les utilisateurs, les ordinateurs et les groupes qui ne sont pas autorisés à mettre en cache leurs mots de passe sur un contrôleur de domaine en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="bbc5c-106">Used with RODCs to define which users, computers, and groups are not allowed to have their passwords cached on an RODC.</span></span>



| <span data-ttu-id="bbc5c-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="bbc5c-107">Entry</span></span> | <span data-ttu-id="bbc5c-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="bbc5c-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="bbc5c-109">CN</span><span class="sxs-lookup"><span data-stu-id="bbc5c-109">CN</span></span>                | <span data-ttu-id="bbc5c-110">ms-DS-jamais-Reveal-Group</span><span class="sxs-lookup"><span data-stu-id="bbc5c-110">ms-DS-Never-Reveal-Group</span></span>                |
| <span data-ttu-id="bbc5c-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="bbc5c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="bbc5c-112">msDS-NeverRevealGroup</span><span class="sxs-lookup"><span data-stu-id="bbc5c-112">msDS-NeverRevealGroup</span></span>                   |
| <span data-ttu-id="bbc5c-113">Taille</span><span class="sxs-lookup"><span data-stu-id="bbc5c-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="bbc5c-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="bbc5c-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="bbc5c-115">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="bbc5c-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="bbc5c-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="bbc5c-116">Attribute-Id</span></span>      | <span data-ttu-id="bbc5c-117">1.2.840.113556.1.4.1926</span><span class="sxs-lookup"><span data-stu-id="bbc5c-117">1.2.840.113556.1.4.1926</span></span>                 |
| <span data-ttu-id="bbc5c-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="bbc5c-118">System-Id-Guid</span></span>    | <span data-ttu-id="bbc5c-119">15585999-fd49-4d66-B25D-eeb96aba8174</span><span class="sxs-lookup"><span data-stu-id="bbc5c-119">15585999-fd49-4d66-b25d-eeb96aba8174</span></span>    |
| <span data-ttu-id="bbc5c-120">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bbc5c-120">Syntax</span></span>            | [<span data-ttu-id="bbc5c-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="bbc5c-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="bbc5c-122">Implémentations</span><span class="sxs-lookup"><span data-stu-id="bbc5c-122">Implementations</span></span>

-   [<span data-ttu-id="bbc5c-123">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="bbc5c-123">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="bbc5c-124">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="bbc5c-124">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="bbc5c-125">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="bbc5c-125">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="bbc5c-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bbc5c-126">Windows Server 2008</span></span>



| <span data-ttu-id="bbc5c-127">Entrée</span><span class="sxs-lookup"><span data-stu-id="bbc5c-127">Entry</span></span> | <span data-ttu-id="bbc5c-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="bbc5c-128">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bbc5c-129">ID de lien</span><span class="sxs-lookup"><span data-stu-id="bbc5c-129">Link-Id</span></span>                | <span data-ttu-id="bbc5c-130">2106</span><span class="sxs-lookup"><span data-stu-id="bbc5c-130">2106</span></span>                                                                               |
| <span data-ttu-id="bbc5c-131">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bbc5c-131">MAPI-Id</span></span>                | \-                                                                                 |
| <span data-ttu-id="bbc5c-132">System-Only</span><span class="sxs-lookup"><span data-stu-id="bbc5c-132">System-Only</span></span>            | <span data-ttu-id="bbc5c-133">Faux</span><span class="sxs-lookup"><span data-stu-id="bbc5c-133">False</span></span>                                                                              |
| <span data-ttu-id="bbc5c-134">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="bbc5c-134">Is-Single-Valued</span></span>       | <span data-ttu-id="bbc5c-135">Faux</span><span class="sxs-lookup"><span data-stu-id="bbc5c-135">False</span></span>                                                                              |
| <span data-ttu-id="bbc5c-136">Est indexé</span><span class="sxs-lookup"><span data-stu-id="bbc5c-136">Is Indexed</span></span>             | <span data-ttu-id="bbc5c-137">Faux</span><span class="sxs-lookup"><span data-stu-id="bbc5c-137">False</span></span>                                                                              |
| <span data-ttu-id="bbc5c-138">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="bbc5c-138">In Global Catalog</span></span>      | <span data-ttu-id="bbc5c-139">Faux</span><span class="sxs-lookup"><span data-stu-id="bbc5c-139">False</span></span>                                                                              |
| <span data-ttu-id="bbc5c-140">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="bbc5c-140">NT-Security-Descriptor</span></span> | <span data-ttu-id="bbc5c-141">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="bbc5c-141">O:BAG:BAD:S:</span></span>                                                                       |
| <span data-ttu-id="bbc5c-142">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bbc5c-142">Range-Lower</span></span>            | \-                                                                                 |
| <span data-ttu-id="bbc5c-143">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bbc5c-143">Range-Upper</span></span>            | \-                                                                                 |
| <span data-ttu-id="bbc5c-144">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bbc5c-144">Search-Flags</span></span>           | <span data-ttu-id="bbc5c-145">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bbc5c-145">0x00000000</span></span>                                                                         |
| <span data-ttu-id="bbc5c-146">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bbc5c-146">System-Flags</span></span>           | <span data-ttu-id="bbc5c-147">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bbc5c-147">0x00000010</span></span>                                                                         |
| <span data-ttu-id="bbc5c-148">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="bbc5c-148">Classes used in</span></span>        | [<span data-ttu-id="bbc5c-149">**Computer**</span><span class="sxs-lookup"><span data-stu-id="bbc5c-149">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="bbc5c-150">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="bbc5c-150">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="bbc5c-151">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bbc5c-151">Windows Server 2008 R2</span></span>



| <span data-ttu-id="bbc5c-152">Entrée</span><span class="sxs-lookup"><span data-stu-id="bbc5c-152">Entry</span></span> | <span data-ttu-id="bbc5c-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="bbc5c-153">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bbc5c-154">ID de lien</span><span class="sxs-lookup"><span data-stu-id="bbc5c-154">Link-Id</span></span>                | <span data-ttu-id="bbc5c-155">2106</span><span class="sxs-lookup"><span data-stu-id="bbc5c-155">2106</span></span>                                                                               |
| <span data-ttu-id="bbc5c-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bbc5c-156">MAPI-Id</span></span>                | \-                                                                                 |
| <span data-ttu-id="bbc5c-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="bbc5c-157">System-Only</span></span>            | <span data-ttu-id="bbc5c-158">Faux</span><span class="sxs-lookup"><span data-stu-id="bbc5c-158">False</span></span>                                                                              |
| <span data-ttu-id="bbc5c-159">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="bbc5c-159">Is-Single-Valued</span></span>       | <span data-ttu-id="bbc5c-160">Faux</span><span class="sxs-lookup"><span data-stu-id="bbc5c-160">False</span></span>                                                                              |
| <span data-ttu-id="bbc5c-161">Est indexé</span><span class="sxs-lookup"><span data-stu-id="bbc5c-161">Is Indexed</span></span>             | <span data-ttu-id="bbc5c-162">Faux</span><span class="sxs-lookup"><span data-stu-id="bbc5c-162">False</span></span>                                                                              |
| <span data-ttu-id="bbc5c-163">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="bbc5c-163">In Global Catalog</span></span>      | <span data-ttu-id="bbc5c-164">Faux</span><span class="sxs-lookup"><span data-stu-id="bbc5c-164">False</span></span>                                                                              |
| <span data-ttu-id="bbc5c-165">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="bbc5c-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="bbc5c-166">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="bbc5c-166">O:BAG:BAD:S:</span></span>                                                                       |
| <span data-ttu-id="bbc5c-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bbc5c-167">Range-Lower</span></span>            | \-                                                                                 |
| <span data-ttu-id="bbc5c-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bbc5c-168">Range-Upper</span></span>            | \-                                                                                 |
| <span data-ttu-id="bbc5c-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bbc5c-169">Search-Flags</span></span>           | <span data-ttu-id="bbc5c-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bbc5c-170">0x00000000</span></span>                                                                         |
| <span data-ttu-id="bbc5c-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bbc5c-171">System-Flags</span></span>           | <span data-ttu-id="bbc5c-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bbc5c-172">0x00000010</span></span>                                                                         |
| <span data-ttu-id="bbc5c-173">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="bbc5c-173">Classes used in</span></span>        | [<span data-ttu-id="bbc5c-174">**Computer**</span><span class="sxs-lookup"><span data-stu-id="bbc5c-174">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="bbc5c-175">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="bbc5c-175">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="bbc5c-176">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bbc5c-176">Windows Server 2012</span></span>



| <span data-ttu-id="bbc5c-177">Entrée</span><span class="sxs-lookup"><span data-stu-id="bbc5c-177">Entry</span></span> | <span data-ttu-id="bbc5c-178">Valeur</span><span class="sxs-lookup"><span data-stu-id="bbc5c-178">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bbc5c-179">ID de lien</span><span class="sxs-lookup"><span data-stu-id="bbc5c-179">Link-Id</span></span>                | <span data-ttu-id="bbc5c-180">2106</span><span class="sxs-lookup"><span data-stu-id="bbc5c-180">2106</span></span>                                                                               |
| <span data-ttu-id="bbc5c-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bbc5c-181">MAPI-Id</span></span>                | \-                                                                                 |
| <span data-ttu-id="bbc5c-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="bbc5c-182">System-Only</span></span>            | <span data-ttu-id="bbc5c-183">Faux</span><span class="sxs-lookup"><span data-stu-id="bbc5c-183">False</span></span>                                                                              |
| <span data-ttu-id="bbc5c-184">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="bbc5c-184">Is-Single-Valued</span></span>       | <span data-ttu-id="bbc5c-185">Faux</span><span class="sxs-lookup"><span data-stu-id="bbc5c-185">False</span></span>                                                                              |
| <span data-ttu-id="bbc5c-186">Est indexé</span><span class="sxs-lookup"><span data-stu-id="bbc5c-186">Is Indexed</span></span>             | <span data-ttu-id="bbc5c-187">Faux</span><span class="sxs-lookup"><span data-stu-id="bbc5c-187">False</span></span>                                                                              |
| <span data-ttu-id="bbc5c-188">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="bbc5c-188">In Global Catalog</span></span>      | <span data-ttu-id="bbc5c-189">Faux</span><span class="sxs-lookup"><span data-stu-id="bbc5c-189">False</span></span>                                                                              |
| <span data-ttu-id="bbc5c-190">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="bbc5c-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="bbc5c-191">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="bbc5c-191">O:BAG:BAD:S:</span></span>                                                                       |
| <span data-ttu-id="bbc5c-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bbc5c-192">Range-Lower</span></span>            | \-                                                                                 |
| <span data-ttu-id="bbc5c-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bbc5c-193">Range-Upper</span></span>            | \-                                                                                 |
| <span data-ttu-id="bbc5c-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bbc5c-194">Search-Flags</span></span>           | <span data-ttu-id="bbc5c-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bbc5c-195">0x00000000</span></span>                                                                         |
| <span data-ttu-id="bbc5c-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bbc5c-196">System-Flags</span></span>           | <span data-ttu-id="bbc5c-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bbc5c-197">0x00000010</span></span>                                                                         |
| <span data-ttu-id="bbc5c-198">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="bbc5c-198">Classes used in</span></span>        | [<span data-ttu-id="bbc5c-199">**Computer**</span><span class="sxs-lookup"><span data-stu-id="bbc5c-199">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="bbc5c-200">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="bbc5c-200">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





