---
title: Attribut ACS-DSBM-DeadTime
description: Cet attribut contient l’intervalle de temps mort d’élection (DSBMDeadInterval) pour un domaine.
ms.assetid: c3a0780c-1786-4631-b870-77146de87f18
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut ACS-DSBM-DeadTime
- Schéma AD de l’attribut aCSDSBMDeadTime
topic_type:
- apiref
api_name:
- ACS-DSBM-DeadTime
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a8b1c980175dc985c3a718d15323be0b8d1b411
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107341"
---
# <a name="acs-dsbm-deadtime-attribute"></a><span data-ttu-id="a6a21-105">Attribut ACS-DSBM-DeadTime</span><span class="sxs-lookup"><span data-stu-id="a6a21-105">ACS-DSBM-DeadTime attribute</span></span>

<span data-ttu-id="a6a21-106">Cet attribut contient l’intervalle de temps mort d’élection (DSBMDeadInterval) pour un domaine.</span><span class="sxs-lookup"><span data-stu-id="a6a21-106">This attribute contains the election dead time interval (DSBMDeadInterval) for a domain.</span></span> <span data-ttu-id="a6a21-107">Si le gestionnaire de bande passante de sous-réseau désigné n’envoie pas une \_ annonce I am \_ DSBM au cours de cet intervalle, les autres gestionnaires de bande passante de sous-réseau (SBMs) dans le domaine choisissent un nouveau DSBM.</span><span class="sxs-lookup"><span data-stu-id="a6a21-107">If the Designated Subnet Bandwidth Manager does not send out an I\_AM\_DSBM advertisement during this interval, then the other Subnet Bandwidth Managers (SBMs) in the domain elect a new DSBM.</span></span>



| <span data-ttu-id="a6a21-108">Entrée</span><span class="sxs-lookup"><span data-stu-id="a6a21-108">Entry</span></span> | <span data-ttu-id="a6a21-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="a6a21-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="a6a21-110">CN</span><span class="sxs-lookup"><span data-stu-id="a6a21-110">CN</span></span>                | <span data-ttu-id="a6a21-111">ACS-DSBM-DeadTime</span><span class="sxs-lookup"><span data-stu-id="a6a21-111">ACS-DSBM-DeadTime</span></span>                    |
| <span data-ttu-id="a6a21-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="a6a21-112">Ldap-Display-Name</span></span> | <span data-ttu-id="a6a21-113">aCSDSBMDeadTime</span><span class="sxs-lookup"><span data-stu-id="a6a21-113">aCSDSBMDeadTime</span></span>                      |
| <span data-ttu-id="a6a21-114">Taille</span><span class="sxs-lookup"><span data-stu-id="a6a21-114">Size</span></span>              | <span data-ttu-id="a6a21-115">4 octets</span><span class="sxs-lookup"><span data-stu-id="a6a21-115">4 bytes</span></span>                              |
| <span data-ttu-id="a6a21-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="a6a21-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="a6a21-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="a6a21-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="a6a21-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a6a21-118">Attribute-Id</span></span>      | <span data-ttu-id="a6a21-119">1.2.840.113556.1.4.778</span><span class="sxs-lookup"><span data-stu-id="a6a21-119">1.2.840.113556.1.4.778</span></span>               |
| <span data-ttu-id="a6a21-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a6a21-120">System-Id-Guid</span></span>    | <span data-ttu-id="a6a21-121">1cb355a0-56d0-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="a6a21-121">1cb355a0-56d0-11d1-a9c6-0000f80367c1</span></span> |
| <span data-ttu-id="a6a21-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a6a21-122">Syntax</span></span>            | [<span data-ttu-id="a6a21-123">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="a6a21-123">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="a6a21-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="a6a21-124">Implementations</span></span>

-   [<span data-ttu-id="a6a21-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a6a21-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a6a21-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a6a21-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a6a21-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a6a21-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a6a21-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a6a21-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a6a21-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a6a21-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a6a21-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a6a21-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a6a21-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a6a21-131">Windows 2000 Server</span></span>



| <span data-ttu-id="a6a21-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="a6a21-132">Entry</span></span> | <span data-ttu-id="a6a21-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="a6a21-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a6a21-134">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a6a21-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a6a21-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a6a21-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a6a21-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="a6a21-136">System-Only</span></span>            | <span data-ttu-id="a6a21-137">Faux</span><span class="sxs-lookup"><span data-stu-id="a6a21-137">False</span></span>                                        |
| <span data-ttu-id="a6a21-138">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a6a21-138">Is-Single-Valued</span></span>       | <span data-ttu-id="a6a21-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="a6a21-139">True</span></span>                                         |
| <span data-ttu-id="a6a21-140">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a6a21-140">Is Indexed</span></span>             | <span data-ttu-id="a6a21-141">Faux</span><span class="sxs-lookup"><span data-stu-id="a6a21-141">False</span></span>                                        |
| <span data-ttu-id="a6a21-142">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a6a21-142">In Global Catalog</span></span>      | <span data-ttu-id="a6a21-143">Faux</span><span class="sxs-lookup"><span data-stu-id="a6a21-143">False</span></span>                                        |
| <span data-ttu-id="a6a21-144">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a6a21-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="a6a21-145">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a6a21-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a6a21-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a6a21-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a6a21-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a6a21-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a6a21-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a6a21-148">Search-Flags</span></span>           | <span data-ttu-id="a6a21-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a6a21-149">0x00000000</span></span>                                   |
| <span data-ttu-id="a6a21-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a6a21-150">System-Flags</span></span>           | <span data-ttu-id="a6a21-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a6a21-151">0x00000010</span></span>                                   |
| <span data-ttu-id="a6a21-152">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a6a21-152">Classes used in</span></span>        | [<span data-ttu-id="a6a21-153">**ACS-sous-réseau**</span><span class="sxs-lookup"><span data-stu-id="a6a21-153">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a6a21-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a6a21-154">Windows Server 2003</span></span>



| <span data-ttu-id="a6a21-155">Entrée</span><span class="sxs-lookup"><span data-stu-id="a6a21-155">Entry</span></span> | <span data-ttu-id="a6a21-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="a6a21-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a6a21-157">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a6a21-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a6a21-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a6a21-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a6a21-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="a6a21-159">System-Only</span></span>            | <span data-ttu-id="a6a21-160">Faux</span><span class="sxs-lookup"><span data-stu-id="a6a21-160">False</span></span>                                        |
| <span data-ttu-id="a6a21-161">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a6a21-161">Is-Single-Valued</span></span>       | <span data-ttu-id="a6a21-162">Vrai</span><span class="sxs-lookup"><span data-stu-id="a6a21-162">True</span></span>                                         |
| <span data-ttu-id="a6a21-163">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a6a21-163">Is Indexed</span></span>             | <span data-ttu-id="a6a21-164">Faux</span><span class="sxs-lookup"><span data-stu-id="a6a21-164">False</span></span>                                        |
| <span data-ttu-id="a6a21-165">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a6a21-165">In Global Catalog</span></span>      | <span data-ttu-id="a6a21-166">Faux</span><span class="sxs-lookup"><span data-stu-id="a6a21-166">False</span></span>                                        |
| <span data-ttu-id="a6a21-167">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a6a21-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="a6a21-168">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a6a21-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a6a21-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a6a21-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a6a21-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a6a21-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a6a21-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a6a21-171">Search-Flags</span></span>           | <span data-ttu-id="a6a21-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a6a21-172">0x00000000</span></span>                                   |
| <span data-ttu-id="a6a21-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a6a21-173">System-Flags</span></span>           | <span data-ttu-id="a6a21-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a6a21-174">0x00000010</span></span>                                   |
| <span data-ttu-id="a6a21-175">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a6a21-175">Classes used in</span></span>        | [<span data-ttu-id="a6a21-176">**ACS-sous-réseau**</span><span class="sxs-lookup"><span data-stu-id="a6a21-176">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a6a21-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a6a21-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a6a21-178">Entrée</span><span class="sxs-lookup"><span data-stu-id="a6a21-178">Entry</span></span> | <span data-ttu-id="a6a21-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="a6a21-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a6a21-180">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a6a21-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a6a21-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a6a21-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a6a21-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="a6a21-182">System-Only</span></span>            | <span data-ttu-id="a6a21-183">Faux</span><span class="sxs-lookup"><span data-stu-id="a6a21-183">False</span></span>                                        |
| <span data-ttu-id="a6a21-184">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a6a21-184">Is-Single-Valued</span></span>       | <span data-ttu-id="a6a21-185">Vrai</span><span class="sxs-lookup"><span data-stu-id="a6a21-185">True</span></span>                                         |
| <span data-ttu-id="a6a21-186">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a6a21-186">Is Indexed</span></span>             | <span data-ttu-id="a6a21-187">Faux</span><span class="sxs-lookup"><span data-stu-id="a6a21-187">False</span></span>                                        |
| <span data-ttu-id="a6a21-188">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a6a21-188">In Global Catalog</span></span>      | <span data-ttu-id="a6a21-189">Faux</span><span class="sxs-lookup"><span data-stu-id="a6a21-189">False</span></span>                                        |
| <span data-ttu-id="a6a21-190">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a6a21-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="a6a21-191">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a6a21-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a6a21-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a6a21-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a6a21-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a6a21-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a6a21-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a6a21-194">Search-Flags</span></span>           | <span data-ttu-id="a6a21-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a6a21-195">0x00000000</span></span>                                   |
| <span data-ttu-id="a6a21-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a6a21-196">System-Flags</span></span>           | <span data-ttu-id="a6a21-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a6a21-197">0x00000010</span></span>                                   |
| <span data-ttu-id="a6a21-198">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a6a21-198">Classes used in</span></span>        | [<span data-ttu-id="a6a21-199">**ACS-sous-réseau**</span><span class="sxs-lookup"><span data-stu-id="a6a21-199">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a6a21-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a6a21-200">Windows Server 2008</span></span>



| <span data-ttu-id="a6a21-201">Entrée</span><span class="sxs-lookup"><span data-stu-id="a6a21-201">Entry</span></span> | <span data-ttu-id="a6a21-202">Valeur</span><span class="sxs-lookup"><span data-stu-id="a6a21-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a6a21-203">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a6a21-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a6a21-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a6a21-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a6a21-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="a6a21-205">System-Only</span></span>            | <span data-ttu-id="a6a21-206">Faux</span><span class="sxs-lookup"><span data-stu-id="a6a21-206">False</span></span>                                        |
| <span data-ttu-id="a6a21-207">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a6a21-207">Is-Single-Valued</span></span>       | <span data-ttu-id="a6a21-208">Vrai</span><span class="sxs-lookup"><span data-stu-id="a6a21-208">True</span></span>                                         |
| <span data-ttu-id="a6a21-209">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a6a21-209">Is Indexed</span></span>             | <span data-ttu-id="a6a21-210">Faux</span><span class="sxs-lookup"><span data-stu-id="a6a21-210">False</span></span>                                        |
| <span data-ttu-id="a6a21-211">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a6a21-211">In Global Catalog</span></span>      | <span data-ttu-id="a6a21-212">Faux</span><span class="sxs-lookup"><span data-stu-id="a6a21-212">False</span></span>                                        |
| <span data-ttu-id="a6a21-213">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a6a21-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="a6a21-214">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a6a21-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a6a21-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a6a21-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a6a21-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a6a21-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a6a21-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a6a21-217">Search-Flags</span></span>           | <span data-ttu-id="a6a21-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a6a21-218">0x00000000</span></span>                                   |
| <span data-ttu-id="a6a21-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a6a21-219">System-Flags</span></span>           | <span data-ttu-id="a6a21-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a6a21-220">0x00000010</span></span>                                   |
| <span data-ttu-id="a6a21-221">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a6a21-221">Classes used in</span></span>        | [<span data-ttu-id="a6a21-222">**ACS-sous-réseau**</span><span class="sxs-lookup"><span data-stu-id="a6a21-222">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a6a21-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a6a21-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a6a21-224">Entrée</span><span class="sxs-lookup"><span data-stu-id="a6a21-224">Entry</span></span> | <span data-ttu-id="a6a21-225">Valeur</span><span class="sxs-lookup"><span data-stu-id="a6a21-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a6a21-226">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a6a21-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a6a21-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a6a21-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a6a21-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="a6a21-228">System-Only</span></span>            | <span data-ttu-id="a6a21-229">Faux</span><span class="sxs-lookup"><span data-stu-id="a6a21-229">False</span></span>                                        |
| <span data-ttu-id="a6a21-230">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a6a21-230">Is-Single-Valued</span></span>       | <span data-ttu-id="a6a21-231">Vrai</span><span class="sxs-lookup"><span data-stu-id="a6a21-231">True</span></span>                                         |
| <span data-ttu-id="a6a21-232">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a6a21-232">Is Indexed</span></span>             | <span data-ttu-id="a6a21-233">Faux</span><span class="sxs-lookup"><span data-stu-id="a6a21-233">False</span></span>                                        |
| <span data-ttu-id="a6a21-234">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a6a21-234">In Global Catalog</span></span>      | <span data-ttu-id="a6a21-235">Faux</span><span class="sxs-lookup"><span data-stu-id="a6a21-235">False</span></span>                                        |
| <span data-ttu-id="a6a21-236">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a6a21-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="a6a21-237">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a6a21-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a6a21-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a6a21-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a6a21-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a6a21-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a6a21-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a6a21-240">Search-Flags</span></span>           | <span data-ttu-id="a6a21-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a6a21-241">0x00000000</span></span>                                   |
| <span data-ttu-id="a6a21-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a6a21-242">System-Flags</span></span>           | <span data-ttu-id="a6a21-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a6a21-243">0x00000010</span></span>                                   |
| <span data-ttu-id="a6a21-244">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a6a21-244">Classes used in</span></span>        | [<span data-ttu-id="a6a21-245">**ACS-sous-réseau**</span><span class="sxs-lookup"><span data-stu-id="a6a21-245">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a6a21-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a6a21-246">Windows Server 2012</span></span>



| <span data-ttu-id="a6a21-247">Entrée</span><span class="sxs-lookup"><span data-stu-id="a6a21-247">Entry</span></span> | <span data-ttu-id="a6a21-248">Valeur</span><span class="sxs-lookup"><span data-stu-id="a6a21-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a6a21-249">ID de lien</span><span class="sxs-lookup"><span data-stu-id="a6a21-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a6a21-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a6a21-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a6a21-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="a6a21-251">System-Only</span></span>            | <span data-ttu-id="a6a21-252">Faux</span><span class="sxs-lookup"><span data-stu-id="a6a21-252">False</span></span>                                        |
| <span data-ttu-id="a6a21-253">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="a6a21-253">Is-Single-Valued</span></span>       | <span data-ttu-id="a6a21-254">Vrai</span><span class="sxs-lookup"><span data-stu-id="a6a21-254">True</span></span>                                         |
| <span data-ttu-id="a6a21-255">Est indexé</span><span class="sxs-lookup"><span data-stu-id="a6a21-255">Is Indexed</span></span>             | <span data-ttu-id="a6a21-256">Faux</span><span class="sxs-lookup"><span data-stu-id="a6a21-256">False</span></span>                                        |
| <span data-ttu-id="a6a21-257">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="a6a21-257">In Global Catalog</span></span>      | <span data-ttu-id="a6a21-258">Faux</span><span class="sxs-lookup"><span data-stu-id="a6a21-258">False</span></span>                                        |
| <span data-ttu-id="a6a21-259">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="a6a21-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="a6a21-260">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="a6a21-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a6a21-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a6a21-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a6a21-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a6a21-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a6a21-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a6a21-263">Search-Flags</span></span>           | <span data-ttu-id="a6a21-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a6a21-264">0x00000000</span></span>                                   |
| <span data-ttu-id="a6a21-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a6a21-265">System-Flags</span></span>           | <span data-ttu-id="a6a21-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a6a21-266">0x00000010</span></span>                                   |
| <span data-ttu-id="a6a21-267">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="a6a21-267">Classes used in</span></span>        | [<span data-ttu-id="a6a21-268">**ACS-sous-réseau**</span><span class="sxs-lookup"><span data-stu-id="a6a21-268">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 





