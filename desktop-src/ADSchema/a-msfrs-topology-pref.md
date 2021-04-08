---
title: MS-FRS-Topology-attribut pref
description: L’attribut ms-FRS-Topology-pref est utilisé pour enregistrer les paramètres de topologie NTFRS préférés.
ms.assetid: 2804ad8a-bec8-491b-84ea-bdff1c8635d0
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory MS-FRS-Topology-pref Attribute
- Schéma AD d’attribut msFRS-Topology-pref
topic_type:
- apiref
api_name:
- ms-FRS-Topology-Pref
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de417b03385e51d6a97fd68097f81bcc0cb6b9db
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744668"
---
# <a name="ms-frs-topology-pref-attribute"></a><span data-ttu-id="1b608-105">MS-FRS-Topology-attribut pref</span><span class="sxs-lookup"><span data-stu-id="1b608-105">ms-FRS-Topology-Pref attribute</span></span>

<span data-ttu-id="1b608-106">L’attribut **MS-FRS-Topology-pref** est utilisé pour enregistrer les paramètres de topologie NTFRS préférés.</span><span class="sxs-lookup"><span data-stu-id="1b608-106">The **ms-FRS-Topology-Pref** attribute is used to record the preferred NTFRS topology settings.</span></span> <span data-ttu-id="1b608-107">Lorsqu’un membre FRS est ajouté ou supprimé au jeu de réplicas, ces attributs sont référencés et les modifications sont apportées aux connexions entre le reste des membres FRS dans le jeu de réplicas.</span><span class="sxs-lookup"><span data-stu-id="1b608-107">When an FRS member gets added or deleted to the replica set, these attributes are referred, and adjustments made to the connections between the rest of the FRS members in the replica set.</span></span>

<span data-ttu-id="1b608-108">Les valeurs valides pour cet attribut sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="1b608-108">Valid values for this attribute are as follows.</span></span>

| <span data-ttu-id="1b608-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="1b608-109">Value</span></span> | <span data-ttu-id="1b608-110">Description</span><span class="sxs-lookup"><span data-stu-id="1b608-110">Description</span></span>                              |
|-------|------------------------------------------|
| <span data-ttu-id="1b608-111">1</span><span class="sxs-lookup"><span data-stu-id="1b608-111">1</span></span>     | <span data-ttu-id="1b608-112">\_anneau RSTOPOLOGYPREF \_ FRS</span><span class="sxs-lookup"><span data-stu-id="1b608-112">FRS\_RSTOPOLOGYPREF\_RING</span></span><br/>     |
| <span data-ttu-id="1b608-113">2</span><span class="sxs-lookup"><span data-stu-id="1b608-113">2</span></span>     | <span data-ttu-id="1b608-114">\_RSTOPOLOGYPREF FRS \_ HUBSPOKE</span><span class="sxs-lookup"><span data-stu-id="1b608-114">FRS\_RSTOPOLOGYPREF\_HUBSPOKE</span></span><br/> |
| <span data-ttu-id="1b608-115">3</span><span class="sxs-lookup"><span data-stu-id="1b608-115">3</span></span>     | <span data-ttu-id="1b608-116">\_RSTOPOLOGYPREF FRS \_ FULLMESH</span><span class="sxs-lookup"><span data-stu-id="1b608-116">FRS\_RSTOPOLOGYPREF\_FULLMESH</span></span><br/> |
| <span data-ttu-id="1b608-117">4</span><span class="sxs-lookup"><span data-stu-id="1b608-117">4</span></span>     | <span data-ttu-id="1b608-118">\_RSTOPOLOGYPREF FRS \_ personnalisé</span><span class="sxs-lookup"><span data-stu-id="1b608-118">FRS\_RSTOPOLOGYPREF\_CUSTOM</span></span><br/>   |



 



| <span data-ttu-id="1b608-119">Entrée</span><span class="sxs-lookup"><span data-stu-id="1b608-119">Entry</span></span> | <span data-ttu-id="1b608-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="1b608-120">Value</span></span> |
|-------------------|--------------------------------------------------------------------|
| <span data-ttu-id="1b608-121">CN</span><span class="sxs-lookup"><span data-stu-id="1b608-121">CN</span></span>                | <span data-ttu-id="1b608-122">MS-FRS-Topology-préférences</span><span class="sxs-lookup"><span data-stu-id="1b608-122">ms-FRS-Topology-Pref</span></span>                                               |
| <span data-ttu-id="1b608-123">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="1b608-123">Ldap-Display-Name</span></span> | <span data-ttu-id="1b608-124">msFRS-Topology-pref</span><span class="sxs-lookup"><span data-stu-id="1b608-124">msFRS-Topology-Pref</span></span>                                                |
| <span data-ttu-id="1b608-125">Taille</span><span class="sxs-lookup"><span data-stu-id="1b608-125">Size</span></span>              | \-                                                                 |
| <span data-ttu-id="1b608-126">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="1b608-126">Update Privilege</span></span>  | <span data-ttu-id="1b608-127">Administrateur de domaine</span><span class="sxs-lookup"><span data-stu-id="1b608-127">Domain administrator</span></span>                                               |
| <span data-ttu-id="1b608-128">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="1b608-128">Update Frequency</span></span>  | <span data-ttu-id="1b608-129">Lors de la création du jeu de réplicas ou de la modification de la topologie par défaut.</span><span class="sxs-lookup"><span data-stu-id="1b608-129">When the replica set is created or the preferred topology changes.</span></span> |
| <span data-ttu-id="1b608-130">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1b608-130">Attribute-Id</span></span>      | <span data-ttu-id="1b608-131">1.2.840.113556.1.4.1692</span><span class="sxs-lookup"><span data-stu-id="1b608-131">1.2.840.113556.1.4.1692</span></span>                                            |
| <span data-ttu-id="1b608-132">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="1b608-132">System-Id-Guid</span></span>    | <span data-ttu-id="1b608-133">92aa27e0-5c50-402d-9ec1-ee847def9788</span><span class="sxs-lookup"><span data-stu-id="1b608-133">92aa27e0-5c50-402d-9ec1-ee847def9788</span></span>                               |
| <span data-ttu-id="1b608-134">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1b608-134">Syntax</span></span>            | [<span data-ttu-id="1b608-135">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="1b608-135">**String(Unicode)**</span></span>](s-string-unicode.md)                        |



## <a name="implementations"></a><span data-ttu-id="1b608-136">Implémentations</span><span class="sxs-lookup"><span data-stu-id="1b608-136">Implementations</span></span>

-   [<span data-ttu-id="1b608-137">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1b608-137">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1b608-138">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1b608-138">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1b608-139">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1b608-139">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1b608-140">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1b608-140">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1b608-141">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1b608-141">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="1b608-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1b608-142">Windows Server 2003</span></span>



| <span data-ttu-id="1b608-143">Entrée</span><span class="sxs-lookup"><span data-stu-id="1b608-143">Entry</span></span> | <span data-ttu-id="1b608-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="1b608-144">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="1b608-145">ID de lien</span><span class="sxs-lookup"><span data-stu-id="1b608-145">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="1b608-146">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1b608-146">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="1b608-147">System-Only</span><span class="sxs-lookup"><span data-stu-id="1b608-147">System-Only</span></span>            | <span data-ttu-id="1b608-148">Faux</span><span class="sxs-lookup"><span data-stu-id="1b608-148">False</span></span>                                                     |
| <span data-ttu-id="1b608-149">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="1b608-149">Is-Single-Valued</span></span>       | <span data-ttu-id="1b608-150">Vrai</span><span class="sxs-lookup"><span data-stu-id="1b608-150">True</span></span>                                                      |
| <span data-ttu-id="1b608-151">Est indexé</span><span class="sxs-lookup"><span data-stu-id="1b608-151">Is Indexed</span></span>             | <span data-ttu-id="1b608-152">Faux</span><span class="sxs-lookup"><span data-stu-id="1b608-152">False</span></span>                                                     |
| <span data-ttu-id="1b608-153">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="1b608-153">In Global Catalog</span></span>      | <span data-ttu-id="1b608-154">Faux</span><span class="sxs-lookup"><span data-stu-id="1b608-154">False</span></span>                                                     |
| <span data-ttu-id="1b608-155">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="1b608-155">NT-Security-Descriptor</span></span> | <span data-ttu-id="1b608-156">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="1b608-156">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="1b608-157">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1b608-157">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="1b608-158">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1b608-158">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="1b608-159">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1b608-159">Search-Flags</span></span>           | <span data-ttu-id="1b608-160">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1b608-160">0x00000000</span></span>                                                |
| <span data-ttu-id="1b608-161">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1b608-161">System-Flags</span></span>           | <span data-ttu-id="1b608-162">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1b608-162">0x00000000</span></span>                                                |
| <span data-ttu-id="1b608-163">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="1b608-163">Classes used in</span></span>        | [<span data-ttu-id="1b608-164">**NTFRS-jeu de réplicas**</span><span class="sxs-lookup"><span data-stu-id="1b608-164">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1b608-165">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1b608-165">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1b608-166">Entrée</span><span class="sxs-lookup"><span data-stu-id="1b608-166">Entry</span></span> | <span data-ttu-id="1b608-167">Valeur</span><span class="sxs-lookup"><span data-stu-id="1b608-167">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="1b608-168">ID de lien</span><span class="sxs-lookup"><span data-stu-id="1b608-168">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="1b608-169">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1b608-169">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="1b608-170">System-Only</span><span class="sxs-lookup"><span data-stu-id="1b608-170">System-Only</span></span>            | <span data-ttu-id="1b608-171">Faux</span><span class="sxs-lookup"><span data-stu-id="1b608-171">False</span></span>                                                     |
| <span data-ttu-id="1b608-172">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="1b608-172">Is-Single-Valued</span></span>       | <span data-ttu-id="1b608-173">Vrai</span><span class="sxs-lookup"><span data-stu-id="1b608-173">True</span></span>                                                      |
| <span data-ttu-id="1b608-174">Est indexé</span><span class="sxs-lookup"><span data-stu-id="1b608-174">Is Indexed</span></span>             | <span data-ttu-id="1b608-175">Faux</span><span class="sxs-lookup"><span data-stu-id="1b608-175">False</span></span>                                                     |
| <span data-ttu-id="1b608-176">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="1b608-176">In Global Catalog</span></span>      | <span data-ttu-id="1b608-177">Faux</span><span class="sxs-lookup"><span data-stu-id="1b608-177">False</span></span>                                                     |
| <span data-ttu-id="1b608-178">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="1b608-178">NT-Security-Descriptor</span></span> | <span data-ttu-id="1b608-179">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="1b608-179">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="1b608-180">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1b608-180">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="1b608-181">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1b608-181">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="1b608-182">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1b608-182">Search-Flags</span></span>           | <span data-ttu-id="1b608-183">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1b608-183">0x00000000</span></span>                                                |
| <span data-ttu-id="1b608-184">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1b608-184">System-Flags</span></span>           | <span data-ttu-id="1b608-185">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1b608-185">0x00000000</span></span>                                                |
| <span data-ttu-id="1b608-186">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="1b608-186">Classes used in</span></span>        | [<span data-ttu-id="1b608-187">**NTFRS-jeu de réplicas**</span><span class="sxs-lookup"><span data-stu-id="1b608-187">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1b608-188">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1b608-188">Windows Server 2008</span></span>



| <span data-ttu-id="1b608-189">Entrée</span><span class="sxs-lookup"><span data-stu-id="1b608-189">Entry</span></span> | <span data-ttu-id="1b608-190">Valeur</span><span class="sxs-lookup"><span data-stu-id="1b608-190">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="1b608-191">ID de lien</span><span class="sxs-lookup"><span data-stu-id="1b608-191">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="1b608-192">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1b608-192">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="1b608-193">System-Only</span><span class="sxs-lookup"><span data-stu-id="1b608-193">System-Only</span></span>            | <span data-ttu-id="1b608-194">Faux</span><span class="sxs-lookup"><span data-stu-id="1b608-194">False</span></span>                                                     |
| <span data-ttu-id="1b608-195">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="1b608-195">Is-Single-Valued</span></span>       | <span data-ttu-id="1b608-196">Vrai</span><span class="sxs-lookup"><span data-stu-id="1b608-196">True</span></span>                                                      |
| <span data-ttu-id="1b608-197">Est indexé</span><span class="sxs-lookup"><span data-stu-id="1b608-197">Is Indexed</span></span>             | <span data-ttu-id="1b608-198">Faux</span><span class="sxs-lookup"><span data-stu-id="1b608-198">False</span></span>                                                     |
| <span data-ttu-id="1b608-199">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="1b608-199">In Global Catalog</span></span>      | <span data-ttu-id="1b608-200">Faux</span><span class="sxs-lookup"><span data-stu-id="1b608-200">False</span></span>                                                     |
| <span data-ttu-id="1b608-201">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="1b608-201">NT-Security-Descriptor</span></span> | <span data-ttu-id="1b608-202">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="1b608-202">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="1b608-203">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1b608-203">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="1b608-204">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1b608-204">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="1b608-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1b608-205">Search-Flags</span></span>           | <span data-ttu-id="1b608-206">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1b608-206">0x00000000</span></span>                                                |
| <span data-ttu-id="1b608-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1b608-207">System-Flags</span></span>           | <span data-ttu-id="1b608-208">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1b608-208">0x00000000</span></span>                                                |
| <span data-ttu-id="1b608-209">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="1b608-209">Classes used in</span></span>        | [<span data-ttu-id="1b608-210">**NTFRS-jeu de réplicas**</span><span class="sxs-lookup"><span data-stu-id="1b608-210">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1b608-211">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1b608-211">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1b608-212">Entrée</span><span class="sxs-lookup"><span data-stu-id="1b608-212">Entry</span></span> | <span data-ttu-id="1b608-213">Valeur</span><span class="sxs-lookup"><span data-stu-id="1b608-213">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="1b608-214">ID de lien</span><span class="sxs-lookup"><span data-stu-id="1b608-214">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="1b608-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1b608-215">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="1b608-216">System-Only</span><span class="sxs-lookup"><span data-stu-id="1b608-216">System-Only</span></span>            | <span data-ttu-id="1b608-217">Faux</span><span class="sxs-lookup"><span data-stu-id="1b608-217">False</span></span>                                                     |
| <span data-ttu-id="1b608-218">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="1b608-218">Is-Single-Valued</span></span>       | <span data-ttu-id="1b608-219">Vrai</span><span class="sxs-lookup"><span data-stu-id="1b608-219">True</span></span>                                                      |
| <span data-ttu-id="1b608-220">Est indexé</span><span class="sxs-lookup"><span data-stu-id="1b608-220">Is Indexed</span></span>             | <span data-ttu-id="1b608-221">Faux</span><span class="sxs-lookup"><span data-stu-id="1b608-221">False</span></span>                                                     |
| <span data-ttu-id="1b608-222">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="1b608-222">In Global Catalog</span></span>      | <span data-ttu-id="1b608-223">Faux</span><span class="sxs-lookup"><span data-stu-id="1b608-223">False</span></span>                                                     |
| <span data-ttu-id="1b608-224">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="1b608-224">NT-Security-Descriptor</span></span> | <span data-ttu-id="1b608-225">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="1b608-225">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="1b608-226">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1b608-226">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="1b608-227">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1b608-227">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="1b608-228">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1b608-228">Search-Flags</span></span>           | <span data-ttu-id="1b608-229">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1b608-229">0x00000000</span></span>                                                |
| <span data-ttu-id="1b608-230">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1b608-230">System-Flags</span></span>           | <span data-ttu-id="1b608-231">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1b608-231">0x00000000</span></span>                                                |
| <span data-ttu-id="1b608-232">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="1b608-232">Classes used in</span></span>        | [<span data-ttu-id="1b608-233">**NTFRS-jeu de réplicas**</span><span class="sxs-lookup"><span data-stu-id="1b608-233">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1b608-234">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1b608-234">Windows Server 2012</span></span>



| <span data-ttu-id="1b608-235">Entrée</span><span class="sxs-lookup"><span data-stu-id="1b608-235">Entry</span></span> | <span data-ttu-id="1b608-236">Valeur</span><span class="sxs-lookup"><span data-stu-id="1b608-236">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="1b608-237">ID de lien</span><span class="sxs-lookup"><span data-stu-id="1b608-237">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="1b608-238">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1b608-238">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="1b608-239">System-Only</span><span class="sxs-lookup"><span data-stu-id="1b608-239">System-Only</span></span>            | <span data-ttu-id="1b608-240">Faux</span><span class="sxs-lookup"><span data-stu-id="1b608-240">False</span></span>                                                     |
| <span data-ttu-id="1b608-241">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="1b608-241">Is-Single-Valued</span></span>       | <span data-ttu-id="1b608-242">Vrai</span><span class="sxs-lookup"><span data-stu-id="1b608-242">True</span></span>                                                      |
| <span data-ttu-id="1b608-243">Est indexé</span><span class="sxs-lookup"><span data-stu-id="1b608-243">Is Indexed</span></span>             | <span data-ttu-id="1b608-244">Faux</span><span class="sxs-lookup"><span data-stu-id="1b608-244">False</span></span>                                                     |
| <span data-ttu-id="1b608-245">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="1b608-245">In Global Catalog</span></span>      | <span data-ttu-id="1b608-246">Faux</span><span class="sxs-lookup"><span data-stu-id="1b608-246">False</span></span>                                                     |
| <span data-ttu-id="1b608-247">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="1b608-247">NT-Security-Descriptor</span></span> | <span data-ttu-id="1b608-248">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="1b608-248">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="1b608-249">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1b608-249">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="1b608-250">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1b608-250">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="1b608-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1b608-251">Search-Flags</span></span>           | <span data-ttu-id="1b608-252">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1b608-252">0x00000000</span></span>                                                |
| <span data-ttu-id="1b608-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1b608-253">System-Flags</span></span>           | <span data-ttu-id="1b608-254">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1b608-254">0x00000000</span></span>                                                |
| <span data-ttu-id="1b608-255">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="1b608-255">Classes used in</span></span>        | [<span data-ttu-id="1b608-256">**NTFRS-jeu de réplicas**</span><span class="sxs-lookup"><span data-stu-id="1b608-256">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



 

 





