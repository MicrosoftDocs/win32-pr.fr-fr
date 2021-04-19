---
title: attribut ms-DS-NC-RO-Replica-Locations
description: Attribut lié sur un objet de référence croisée pour une partition. Répertorie le contrôleur de périphérique qui doit héberger la partition en lecture seule.
ms.assetid: 2473f201-abf7-4fb1-b005-c8db528aeab8
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory de l’attribut ms-DS-NC-RO-Replica-Locations
- Schéma AD de l’attribut msDS-NC-RO-Replica-Locations
topic_type:
- apiref
api_name:
- ms-DS-NC-RO-Replica-Locations
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 590661cb3dc096caa714066762f7b556e69c5145
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106514692"
---
# <a name="ms-ds-nc-ro-replica-locations-attribute"></a><span data-ttu-id="290dd-106">attribut ms-DS-NC-RO-Replica-Locations</span><span class="sxs-lookup"><span data-stu-id="290dd-106">ms-DS-NC-RO-Replica-Locations attribute</span></span>

<span data-ttu-id="290dd-107">Attribut lié sur un objet de référence croisée pour une partition.</span><span class="sxs-lookup"><span data-stu-id="290dd-107">A linked attribute on a cross reference object for a partition.</span></span> <span data-ttu-id="290dd-108">Répertorie le contrôleur de périphérique qui doit héberger la partition en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="290dd-108">Lists the DC that should host the partition in a read-only manner.</span></span>



| <span data-ttu-id="290dd-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="290dd-109">Entry</span></span> | <span data-ttu-id="290dd-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="290dd-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="290dd-111">CN</span><span class="sxs-lookup"><span data-stu-id="290dd-111">CN</span></span>                | <span data-ttu-id="290dd-112">ms-DS-NC-RO-Replica-Locations</span><span class="sxs-lookup"><span data-stu-id="290dd-112">ms-DS-NC-RO-Replica-Locations</span></span>           |
| <span data-ttu-id="290dd-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="290dd-113">Ldap-Display-Name</span></span> | <span data-ttu-id="290dd-114">msDS-NC-RO-réplica-emplacements</span><span class="sxs-lookup"><span data-stu-id="290dd-114">msDS-NC-RO-Replica-Locations</span></span>            |
| <span data-ttu-id="290dd-115">Taille</span><span class="sxs-lookup"><span data-stu-id="290dd-115">Size</span></span>              | \-                                      |
| <span data-ttu-id="290dd-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="290dd-116">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="290dd-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="290dd-117">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="290dd-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="290dd-118">Attribute-Id</span></span>      | <span data-ttu-id="290dd-119">1.2.840.113556.1.4.1967</span><span class="sxs-lookup"><span data-stu-id="290dd-119">1.2.840.113556.1.4.1967</span></span>                 |
| <span data-ttu-id="290dd-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="290dd-120">System-Id-Guid</span></span>    | <span data-ttu-id="290dd-121">3df793df-9858-4417-A701-735a1ecebf74</span><span class="sxs-lookup"><span data-stu-id="290dd-121">3df793df-9858-4417-a701-735a1ecebf74</span></span>    |
| <span data-ttu-id="290dd-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="290dd-122">Syntax</span></span>            | [<span data-ttu-id="290dd-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="290dd-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="290dd-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="290dd-124">Implementations</span></span>

-   [<span data-ttu-id="290dd-125">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="290dd-125">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="290dd-126">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="290dd-126">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="290dd-127">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="290dd-127">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="290dd-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="290dd-128">Windows Server 2008</span></span>



| <span data-ttu-id="290dd-129">Entrée</span><span class="sxs-lookup"><span data-stu-id="290dd-129">Entry</span></span> | <span data-ttu-id="290dd-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="290dd-130">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="290dd-131">ID de lien</span><span class="sxs-lookup"><span data-stu-id="290dd-131">Link-Id</span></span>                | <span data-ttu-id="290dd-132">2114</span><span class="sxs-lookup"><span data-stu-id="290dd-132">2114</span></span>                                       |
| <span data-ttu-id="290dd-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="290dd-133">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="290dd-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="290dd-134">System-Only</span></span>            | <span data-ttu-id="290dd-135">Faux</span><span class="sxs-lookup"><span data-stu-id="290dd-135">False</span></span>                                      |
| <span data-ttu-id="290dd-136">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="290dd-136">Is-Single-Valued</span></span>       | <span data-ttu-id="290dd-137">Faux</span><span class="sxs-lookup"><span data-stu-id="290dd-137">False</span></span>                                      |
| <span data-ttu-id="290dd-138">Est indexé</span><span class="sxs-lookup"><span data-stu-id="290dd-138">Is Indexed</span></span>             | <span data-ttu-id="290dd-139">Faux</span><span class="sxs-lookup"><span data-stu-id="290dd-139">False</span></span>                                      |
| <span data-ttu-id="290dd-140">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="290dd-140">In Global Catalog</span></span>      | <span data-ttu-id="290dd-141">Faux</span><span class="sxs-lookup"><span data-stu-id="290dd-141">False</span></span>                                      |
| <span data-ttu-id="290dd-142">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="290dd-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="290dd-143">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="290dd-143">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="290dd-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="290dd-144">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="290dd-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="290dd-145">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="290dd-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="290dd-146">Search-Flags</span></span>           | <span data-ttu-id="290dd-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="290dd-147">0x00000000</span></span>                                 |
| <span data-ttu-id="290dd-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="290dd-148">System-Flags</span></span>           | <span data-ttu-id="290dd-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="290dd-149">0x00000010</span></span>                                 |
| <span data-ttu-id="290dd-150">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="290dd-150">Classes used in</span></span>        | [<span data-ttu-id="290dd-151">**Référence croisée**</span><span class="sxs-lookup"><span data-stu-id="290dd-151">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="290dd-152">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="290dd-152">Windows Server 2008 R2</span></span>



| <span data-ttu-id="290dd-153">Entrée</span><span class="sxs-lookup"><span data-stu-id="290dd-153">Entry</span></span> | <span data-ttu-id="290dd-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="290dd-154">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="290dd-155">ID de lien</span><span class="sxs-lookup"><span data-stu-id="290dd-155">Link-Id</span></span>                | <span data-ttu-id="290dd-156">2114</span><span class="sxs-lookup"><span data-stu-id="290dd-156">2114</span></span>                                       |
| <span data-ttu-id="290dd-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="290dd-157">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="290dd-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="290dd-158">System-Only</span></span>            | <span data-ttu-id="290dd-159">Faux</span><span class="sxs-lookup"><span data-stu-id="290dd-159">False</span></span>                                      |
| <span data-ttu-id="290dd-160">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="290dd-160">Is-Single-Valued</span></span>       | <span data-ttu-id="290dd-161">Faux</span><span class="sxs-lookup"><span data-stu-id="290dd-161">False</span></span>                                      |
| <span data-ttu-id="290dd-162">Est indexé</span><span class="sxs-lookup"><span data-stu-id="290dd-162">Is Indexed</span></span>             | <span data-ttu-id="290dd-163">Faux</span><span class="sxs-lookup"><span data-stu-id="290dd-163">False</span></span>                                      |
| <span data-ttu-id="290dd-164">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="290dd-164">In Global Catalog</span></span>      | <span data-ttu-id="290dd-165">Faux</span><span class="sxs-lookup"><span data-stu-id="290dd-165">False</span></span>                                      |
| <span data-ttu-id="290dd-166">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="290dd-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="290dd-167">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="290dd-167">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="290dd-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="290dd-168">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="290dd-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="290dd-169">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="290dd-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="290dd-170">Search-Flags</span></span>           | <span data-ttu-id="290dd-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="290dd-171">0x00000000</span></span>                                 |
| <span data-ttu-id="290dd-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="290dd-172">System-Flags</span></span>           | <span data-ttu-id="290dd-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="290dd-173">0x00000010</span></span>                                 |
| <span data-ttu-id="290dd-174">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="290dd-174">Classes used in</span></span>        | [<span data-ttu-id="290dd-175">**Référence croisée**</span><span class="sxs-lookup"><span data-stu-id="290dd-175">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="290dd-176">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="290dd-176">Windows Server 2012</span></span>



| <span data-ttu-id="290dd-177">Entrée</span><span class="sxs-lookup"><span data-stu-id="290dd-177">Entry</span></span> | <span data-ttu-id="290dd-178">Valeur</span><span class="sxs-lookup"><span data-stu-id="290dd-178">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="290dd-179">ID de lien</span><span class="sxs-lookup"><span data-stu-id="290dd-179">Link-Id</span></span>                | <span data-ttu-id="290dd-180">2114</span><span class="sxs-lookup"><span data-stu-id="290dd-180">2114</span></span>                                       |
| <span data-ttu-id="290dd-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="290dd-181">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="290dd-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="290dd-182">System-Only</span></span>            | <span data-ttu-id="290dd-183">Faux</span><span class="sxs-lookup"><span data-stu-id="290dd-183">False</span></span>                                      |
| <span data-ttu-id="290dd-184">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="290dd-184">Is-Single-Valued</span></span>       | <span data-ttu-id="290dd-185">Faux</span><span class="sxs-lookup"><span data-stu-id="290dd-185">False</span></span>                                      |
| <span data-ttu-id="290dd-186">Est indexé</span><span class="sxs-lookup"><span data-stu-id="290dd-186">Is Indexed</span></span>             | <span data-ttu-id="290dd-187">Faux</span><span class="sxs-lookup"><span data-stu-id="290dd-187">False</span></span>                                      |
| <span data-ttu-id="290dd-188">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="290dd-188">In Global Catalog</span></span>      | <span data-ttu-id="290dd-189">Faux</span><span class="sxs-lookup"><span data-stu-id="290dd-189">False</span></span>                                      |
| <span data-ttu-id="290dd-190">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="290dd-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="290dd-191">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="290dd-191">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="290dd-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="290dd-192">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="290dd-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="290dd-193">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="290dd-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="290dd-194">Search-Flags</span></span>           | <span data-ttu-id="290dd-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="290dd-195">0x00000000</span></span>                                 |
| <span data-ttu-id="290dd-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="290dd-196">System-Flags</span></span>           | <span data-ttu-id="290dd-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="290dd-197">0x00000010</span></span>                                 |
| <span data-ttu-id="290dd-198">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="290dd-198">Classes used in</span></span>        | [<span data-ttu-id="290dd-199">**Référence croisée**</span><span class="sxs-lookup"><span data-stu-id="290dd-199">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



 

 





