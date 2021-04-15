---
title: Attribut SPN-Mappings
description: Cet attribut à valeurs multiples contient une liste de noms de principal du service (SPN) pour indiquer l’équivalence des types SPN.
ms.assetid: 6d37618d-426d-4e7b-8475-c912adb595ee
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut SPN-Mappings
- Schéma AD de l’attribut sPNMappings
topic_type:
- apiref
api_name:
- SPN-Mappings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3ccb07e068a22d0a85928832890f0b66ebda016
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104519985"
---
# <a name="spn-mappings-attribute"></a><span data-ttu-id="e8b43-105">Attribut SPN-Mappings</span><span class="sxs-lookup"><span data-stu-id="e8b43-105">SPN-Mappings attribute</span></span>

<span data-ttu-id="e8b43-106">Cet attribut à valeurs multiples contient une liste de noms de principal du service (SPN) pour indiquer l’équivalence des types SPN.</span><span class="sxs-lookup"><span data-stu-id="e8b43-106">This multiple-valued attribute contains a list of service principal names (SPN) to show the equivalence of SPN types.</span></span> <span data-ttu-id="e8b43-107">Le SPN est le nom qu’un client utilise pour identifier de manière unique une instance d’un service.</span><span class="sxs-lookup"><span data-stu-id="e8b43-107">The SPN is the name a client uses to uniquely identify an instance of a service.</span></span> <span data-ttu-id="e8b43-108">Si vous installez plusieurs instances d'un service sur les ordinateurs d'une forêt, chaque instance doit posséder son propre SPN.</span><span class="sxs-lookup"><span data-stu-id="e8b43-108">If you install multiple instances of a service on computers throughout a forest, each instance must have its own SPN.</span></span> <span data-ttu-id="e8b43-109">Une instance de service donnée peut posséder plusieurs noms SPN si les clients peuvent utiliser plusieurs noms pour l'authentification.</span><span class="sxs-lookup"><span data-stu-id="e8b43-109">A given service instance can have multiple SPNs if there are multiple names that clients might use for authentication.</span></span> <span data-ttu-id="e8b43-110">Par exemple, « LDAP/... » Les noms de principal du service (SPN) peuvent être mappés pour qu’ils soient équivalents à « Host/... » SPN.</span><span class="sxs-lookup"><span data-stu-id="e8b43-110">For example, "ldap/..." SPNs could be mapped so that they are equivalent to "host/..." SPNs.</span></span>



| <span data-ttu-id="e8b43-111">Entrée</span><span class="sxs-lookup"><span data-stu-id="e8b43-111">Entry</span></span> | <span data-ttu-id="e8b43-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="e8b43-112">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8b43-113">CN</span><span class="sxs-lookup"><span data-stu-id="e8b43-113">CN</span></span>                | <span data-ttu-id="e8b43-114">SPN-Mappings</span><span class="sxs-lookup"><span data-stu-id="e8b43-114">SPN-Mappings</span></span>                                                                                                       |
| <span data-ttu-id="e8b43-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="e8b43-115">Ldap-Display-Name</span></span> | <span data-ttu-id="e8b43-116">sPNMappings</span><span class="sxs-lookup"><span data-stu-id="e8b43-116">sPNMappings</span></span>                                                                                                        |
| <span data-ttu-id="e8b43-117">Taille</span><span class="sxs-lookup"><span data-stu-id="e8b43-117">Size</span></span>              | \-                                                                                                                 |
| <span data-ttu-id="e8b43-118">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="e8b43-118">Update Privilege</span></span>  | <span data-ttu-id="e8b43-119">Cette valeur est définie lors de l’installation du produit.</span><span class="sxs-lookup"><span data-stu-id="e8b43-119">This value is set during the product installation.</span></span> <span data-ttu-id="e8b43-120">Il peut être modifié par l’administrateur système ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="e8b43-120">It can be modified by the system administrator at a later time.</span></span> |
| <span data-ttu-id="e8b43-121">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="e8b43-121">Update Frequency</span></span>  | \-                                                                                                                 |
| <span data-ttu-id="e8b43-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e8b43-122">Attribute-Id</span></span>      | <span data-ttu-id="e8b43-123">1.2.840.113556.1.4.1347</span><span class="sxs-lookup"><span data-stu-id="e8b43-123">1.2.840.113556.1.4.1347</span></span>                                                                                            |
| <span data-ttu-id="e8b43-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="e8b43-124">System-Id-Guid</span></span>    | <span data-ttu-id="e8b43-125">2ab0e76c-7041-11d2-9905-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="e8b43-125">2ab0e76c-7041-11d2-9905-0000f87a57d4</span></span>                                                                               |
| <span data-ttu-id="e8b43-126">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e8b43-126">Syntax</span></span>            | [<span data-ttu-id="e8b43-127">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="e8b43-127">**String(Unicode)**</span></span>](s-string-unicode.md)                                                                        |



## <a name="implementations"></a><span data-ttu-id="e8b43-128">Implémentations</span><span class="sxs-lookup"><span data-stu-id="e8b43-128">Implementations</span></span>

-   [<span data-ttu-id="e8b43-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e8b43-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e8b43-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e8b43-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e8b43-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e8b43-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e8b43-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e8b43-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e8b43-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e8b43-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e8b43-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e8b43-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e8b43-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e8b43-135">Windows 2000 Server</span></span>



| <span data-ttu-id="e8b43-136">Entrée</span><span class="sxs-lookup"><span data-stu-id="e8b43-136">Entry</span></span> | <span data-ttu-id="e8b43-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="e8b43-137">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="e8b43-138">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e8b43-138">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="e8b43-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e8b43-139">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="e8b43-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="e8b43-140">System-Only</span></span>            | <span data-ttu-id="e8b43-141">Faux</span><span class="sxs-lookup"><span data-stu-id="e8b43-141">False</span></span>                                            |
| <span data-ttu-id="e8b43-142">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e8b43-142">Is-Single-Valued</span></span>       | <span data-ttu-id="e8b43-143">Faux</span><span class="sxs-lookup"><span data-stu-id="e8b43-143">False</span></span>                                            |
| <span data-ttu-id="e8b43-144">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e8b43-144">Is Indexed</span></span>             | <span data-ttu-id="e8b43-145">Faux</span><span class="sxs-lookup"><span data-stu-id="e8b43-145">False</span></span>                                            |
| <span data-ttu-id="e8b43-146">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e8b43-146">In Global Catalog</span></span>      | <span data-ttu-id="e8b43-147">Faux</span><span class="sxs-lookup"><span data-stu-id="e8b43-147">False</span></span>                                            |
| <span data-ttu-id="e8b43-148">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e8b43-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="e8b43-149">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e8b43-149">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="e8b43-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e8b43-150">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="e8b43-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e8b43-151">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="e8b43-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e8b43-152">Search-Flags</span></span>           | <span data-ttu-id="e8b43-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e8b43-153">0x00000000</span></span>                                       |
| <span data-ttu-id="e8b43-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e8b43-154">System-Flags</span></span>           | <span data-ttu-id="e8b43-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e8b43-155">0x00000010</span></span>                                       |
| <span data-ttu-id="e8b43-156">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e8b43-156">Classes used in</span></span>        | [<span data-ttu-id="e8b43-157">**NTDS-service**</span><span class="sxs-lookup"><span data-stu-id="e8b43-157">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e8b43-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e8b43-158">Windows Server 2003</span></span>



| <span data-ttu-id="e8b43-159">Entrée</span><span class="sxs-lookup"><span data-stu-id="e8b43-159">Entry</span></span> | <span data-ttu-id="e8b43-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="e8b43-160">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="e8b43-161">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e8b43-161">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="e8b43-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e8b43-162">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="e8b43-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="e8b43-163">System-Only</span></span>            | <span data-ttu-id="e8b43-164">Faux</span><span class="sxs-lookup"><span data-stu-id="e8b43-164">False</span></span>                                            |
| <span data-ttu-id="e8b43-165">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e8b43-165">Is-Single-Valued</span></span>       | <span data-ttu-id="e8b43-166">Faux</span><span class="sxs-lookup"><span data-stu-id="e8b43-166">False</span></span>                                            |
| <span data-ttu-id="e8b43-167">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e8b43-167">Is Indexed</span></span>             | <span data-ttu-id="e8b43-168">Faux</span><span class="sxs-lookup"><span data-stu-id="e8b43-168">False</span></span>                                            |
| <span data-ttu-id="e8b43-169">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e8b43-169">In Global Catalog</span></span>      | <span data-ttu-id="e8b43-170">Faux</span><span class="sxs-lookup"><span data-stu-id="e8b43-170">False</span></span>                                            |
| <span data-ttu-id="e8b43-171">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e8b43-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="e8b43-172">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e8b43-172">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="e8b43-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e8b43-173">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="e8b43-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e8b43-174">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="e8b43-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e8b43-175">Search-Flags</span></span>           | <span data-ttu-id="e8b43-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e8b43-176">0x00000000</span></span>                                       |
| <span data-ttu-id="e8b43-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e8b43-177">System-Flags</span></span>           | <span data-ttu-id="e8b43-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e8b43-178">0x00000010</span></span>                                       |
| <span data-ttu-id="e8b43-179">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e8b43-179">Classes used in</span></span>        | [<span data-ttu-id="e8b43-180">**NTDS-service**</span><span class="sxs-lookup"><span data-stu-id="e8b43-180">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e8b43-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e8b43-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e8b43-182">Entrée</span><span class="sxs-lookup"><span data-stu-id="e8b43-182">Entry</span></span> | <span data-ttu-id="e8b43-183">Valeur</span><span class="sxs-lookup"><span data-stu-id="e8b43-183">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="e8b43-184">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e8b43-184">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="e8b43-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e8b43-185">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="e8b43-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="e8b43-186">System-Only</span></span>            | <span data-ttu-id="e8b43-187">Faux</span><span class="sxs-lookup"><span data-stu-id="e8b43-187">False</span></span>                                            |
| <span data-ttu-id="e8b43-188">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e8b43-188">Is-Single-Valued</span></span>       | <span data-ttu-id="e8b43-189">Faux</span><span class="sxs-lookup"><span data-stu-id="e8b43-189">False</span></span>                                            |
| <span data-ttu-id="e8b43-190">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e8b43-190">Is Indexed</span></span>             | <span data-ttu-id="e8b43-191">Faux</span><span class="sxs-lookup"><span data-stu-id="e8b43-191">False</span></span>                                            |
| <span data-ttu-id="e8b43-192">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e8b43-192">In Global Catalog</span></span>      | <span data-ttu-id="e8b43-193">Faux</span><span class="sxs-lookup"><span data-stu-id="e8b43-193">False</span></span>                                            |
| <span data-ttu-id="e8b43-194">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e8b43-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="e8b43-195">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e8b43-195">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="e8b43-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e8b43-196">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="e8b43-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e8b43-197">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="e8b43-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e8b43-198">Search-Flags</span></span>           | <span data-ttu-id="e8b43-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e8b43-199">0x00000000</span></span>                                       |
| <span data-ttu-id="e8b43-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e8b43-200">System-Flags</span></span>           | <span data-ttu-id="e8b43-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e8b43-201">0x00000010</span></span>                                       |
| <span data-ttu-id="e8b43-202">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e8b43-202">Classes used in</span></span>        | [<span data-ttu-id="e8b43-203">**NTDS-service**</span><span class="sxs-lookup"><span data-stu-id="e8b43-203">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e8b43-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e8b43-204">Windows Server 2008</span></span>



| <span data-ttu-id="e8b43-205">Entrée</span><span class="sxs-lookup"><span data-stu-id="e8b43-205">Entry</span></span> | <span data-ttu-id="e8b43-206">Valeur</span><span class="sxs-lookup"><span data-stu-id="e8b43-206">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="e8b43-207">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e8b43-207">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="e8b43-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e8b43-208">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="e8b43-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="e8b43-209">System-Only</span></span>            | <span data-ttu-id="e8b43-210">Faux</span><span class="sxs-lookup"><span data-stu-id="e8b43-210">False</span></span>                                            |
| <span data-ttu-id="e8b43-211">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e8b43-211">Is-Single-Valued</span></span>       | <span data-ttu-id="e8b43-212">Faux</span><span class="sxs-lookup"><span data-stu-id="e8b43-212">False</span></span>                                            |
| <span data-ttu-id="e8b43-213">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e8b43-213">Is Indexed</span></span>             | <span data-ttu-id="e8b43-214">Faux</span><span class="sxs-lookup"><span data-stu-id="e8b43-214">False</span></span>                                            |
| <span data-ttu-id="e8b43-215">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e8b43-215">In Global Catalog</span></span>      | <span data-ttu-id="e8b43-216">Faux</span><span class="sxs-lookup"><span data-stu-id="e8b43-216">False</span></span>                                            |
| <span data-ttu-id="e8b43-217">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e8b43-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="e8b43-218">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e8b43-218">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="e8b43-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e8b43-219">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="e8b43-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e8b43-220">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="e8b43-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e8b43-221">Search-Flags</span></span>           | <span data-ttu-id="e8b43-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e8b43-222">0x00000000</span></span>                                       |
| <span data-ttu-id="e8b43-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e8b43-223">System-Flags</span></span>           | <span data-ttu-id="e8b43-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e8b43-224">0x00000010</span></span>                                       |
| <span data-ttu-id="e8b43-225">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e8b43-225">Classes used in</span></span>        | [<span data-ttu-id="e8b43-226">**NTDS-service**</span><span class="sxs-lookup"><span data-stu-id="e8b43-226">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e8b43-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e8b43-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e8b43-228">Entrée</span><span class="sxs-lookup"><span data-stu-id="e8b43-228">Entry</span></span> | <span data-ttu-id="e8b43-229">Valeur</span><span class="sxs-lookup"><span data-stu-id="e8b43-229">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="e8b43-230">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e8b43-230">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="e8b43-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e8b43-231">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="e8b43-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="e8b43-232">System-Only</span></span>            | <span data-ttu-id="e8b43-233">Faux</span><span class="sxs-lookup"><span data-stu-id="e8b43-233">False</span></span>                                            |
| <span data-ttu-id="e8b43-234">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e8b43-234">Is-Single-Valued</span></span>       | <span data-ttu-id="e8b43-235">Faux</span><span class="sxs-lookup"><span data-stu-id="e8b43-235">False</span></span>                                            |
| <span data-ttu-id="e8b43-236">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e8b43-236">Is Indexed</span></span>             | <span data-ttu-id="e8b43-237">Faux</span><span class="sxs-lookup"><span data-stu-id="e8b43-237">False</span></span>                                            |
| <span data-ttu-id="e8b43-238">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e8b43-238">In Global Catalog</span></span>      | <span data-ttu-id="e8b43-239">Faux</span><span class="sxs-lookup"><span data-stu-id="e8b43-239">False</span></span>                                            |
| <span data-ttu-id="e8b43-240">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e8b43-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="e8b43-241">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e8b43-241">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="e8b43-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e8b43-242">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="e8b43-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e8b43-243">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="e8b43-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e8b43-244">Search-Flags</span></span>           | <span data-ttu-id="e8b43-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e8b43-245">0x00000000</span></span>                                       |
| <span data-ttu-id="e8b43-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e8b43-246">System-Flags</span></span>           | <span data-ttu-id="e8b43-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e8b43-247">0x00000010</span></span>                                       |
| <span data-ttu-id="e8b43-248">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e8b43-248">Classes used in</span></span>        | [<span data-ttu-id="e8b43-249">**NTDS-service**</span><span class="sxs-lookup"><span data-stu-id="e8b43-249">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e8b43-250">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e8b43-250">Windows Server 2012</span></span>



| <span data-ttu-id="e8b43-251">Entrée</span><span class="sxs-lookup"><span data-stu-id="e8b43-251">Entry</span></span> | <span data-ttu-id="e8b43-252">Valeur</span><span class="sxs-lookup"><span data-stu-id="e8b43-252">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="e8b43-253">ID de lien</span><span class="sxs-lookup"><span data-stu-id="e8b43-253">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="e8b43-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e8b43-254">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="e8b43-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="e8b43-255">System-Only</span></span>            | <span data-ttu-id="e8b43-256">Faux</span><span class="sxs-lookup"><span data-stu-id="e8b43-256">False</span></span>                                            |
| <span data-ttu-id="e8b43-257">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="e8b43-257">Is-Single-Valued</span></span>       | <span data-ttu-id="e8b43-258">Faux</span><span class="sxs-lookup"><span data-stu-id="e8b43-258">False</span></span>                                            |
| <span data-ttu-id="e8b43-259">Est indexé</span><span class="sxs-lookup"><span data-stu-id="e8b43-259">Is Indexed</span></span>             | <span data-ttu-id="e8b43-260">Faux</span><span class="sxs-lookup"><span data-stu-id="e8b43-260">False</span></span>                                            |
| <span data-ttu-id="e8b43-261">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="e8b43-261">In Global Catalog</span></span>      | <span data-ttu-id="e8b43-262">Faux</span><span class="sxs-lookup"><span data-stu-id="e8b43-262">False</span></span>                                            |
| <span data-ttu-id="e8b43-263">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="e8b43-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="e8b43-264">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="e8b43-264">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="e8b43-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e8b43-265">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="e8b43-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e8b43-266">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="e8b43-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e8b43-267">Search-Flags</span></span>           | <span data-ttu-id="e8b43-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e8b43-268">0x00000000</span></span>                                       |
| <span data-ttu-id="e8b43-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e8b43-269">System-Flags</span></span>           | <span data-ttu-id="e8b43-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e8b43-270">0x00000010</span></span>                                       |
| <span data-ttu-id="e8b43-271">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="e8b43-271">Classes used in</span></span>        | [<span data-ttu-id="e8b43-272">**NTDS-service**</span><span class="sxs-lookup"><span data-stu-id="e8b43-272">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



 

 





