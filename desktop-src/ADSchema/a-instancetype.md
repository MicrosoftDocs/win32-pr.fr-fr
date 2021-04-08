---
title: Attribut Instance-Type
description: Champ de champ binaire qui détermine la façon dont l’objet est instancié sur un serveur particulier.
ms.assetid: ed77c302-3d80-4292-8e48-bfc6cb5079ee
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Instance-Type
- Schéma Active Directory de l’attribut instanceType
topic_type:
- apiref
api_name:
- Instance-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e31eec3c5a7a189f4623e8e77badb3b1e83e0cd4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744836"
---
# <a name="instance-type-attribute"></a><span data-ttu-id="7c6e2-105">Attribut Instance-Type</span><span class="sxs-lookup"><span data-stu-id="7c6e2-105">Instance-Type attribute</span></span>

<span data-ttu-id="7c6e2-106">Champ de champ binaire qui détermine la façon dont l’objet est instancié sur un serveur particulier.</span><span class="sxs-lookup"><span data-stu-id="7c6e2-106">A bitfield that dictates how the object is instantiated on a particular server.</span></span> <span data-ttu-id="7c6e2-107">La valeur de cet attribut peut différer sur différents réplicas même si les réplicas sont synchronisés.</span><span class="sxs-lookup"><span data-stu-id="7c6e2-107">The value of this attribute can differ on different replicas even if the replicas are in sync.</span></span>

<span data-ttu-id="7c6e2-108">Cet attribut peut avoir la valeur zéro ou une combinaison d’une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="7c6e2-108">This attribute can be zero or a combination of one or more of the following values.</span></span>

| <span data-ttu-id="7c6e2-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c6e2-109">Value</span></span>      | <span data-ttu-id="7c6e2-110">Description</span><span class="sxs-lookup"><span data-stu-id="7c6e2-110">Description</span></span>                                                                                        |
|------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c6e2-111">0x00000001</span><span class="sxs-lookup"><span data-stu-id="7c6e2-111">0x00000001</span></span> | <span data-ttu-id="7c6e2-112">Le début du contexte d’appellation.</span><span class="sxs-lookup"><span data-stu-id="7c6e2-112">The head of naming context.</span></span>                                                                        |
| <span data-ttu-id="7c6e2-113">0x00000002</span><span class="sxs-lookup"><span data-stu-id="7c6e2-113">0x00000002</span></span> | <span data-ttu-id="7c6e2-114">Ce réplica n’est pas instancié.</span><span class="sxs-lookup"><span data-stu-id="7c6e2-114">This replica is not instantiated.</span></span>                                                                  |
| <span data-ttu-id="7c6e2-115">0x00000004</span><span class="sxs-lookup"><span data-stu-id="7c6e2-115">0x00000004</span></span> | <span data-ttu-id="7c6e2-116">L’objet est accessible en écriture dans ce répertoire.</span><span class="sxs-lookup"><span data-stu-id="7c6e2-116">The object is writable on this directory.</span></span>                                                          |
| <span data-ttu-id="7c6e2-117">0x00000008</span><span class="sxs-lookup"><span data-stu-id="7c6e2-117">0x00000008</span></span> | <span data-ttu-id="7c6e2-118">Le contexte d’appellation au-dessus de celui-ci est conservé sur ce répertoire.</span><span class="sxs-lookup"><span data-stu-id="7c6e2-118">The naming context above this one on this directory is held.</span></span>                                       |
| <span data-ttu-id="7c6e2-119">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7c6e2-119">0x00000010</span></span> | <span data-ttu-id="7c6e2-120">Le contexte d’appellation est en cours de construction pour la première fois à l’aide de la réplication.</span><span class="sxs-lookup"><span data-stu-id="7c6e2-120">The naming context is in the process of being constructed for the first time by using replication.</span></span> |
| <span data-ttu-id="7c6e2-121">0x00000020</span><span class="sxs-lookup"><span data-stu-id="7c6e2-121">0x00000020</span></span> | <span data-ttu-id="7c6e2-122">Le contexte d’appellation est en cours de suppression du DSA local.</span><span class="sxs-lookup"><span data-stu-id="7c6e2-122">The naming context is in the process of being removed from the local DSA.</span></span>                          |



 



| <span data-ttu-id="7c6e2-123">Entrée</span><span class="sxs-lookup"><span data-stu-id="7c6e2-123">Entry</span></span> | <span data-ttu-id="7c6e2-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c6e2-124">Value</span></span> |
|-------------------|------------------------------------------------|
| <span data-ttu-id="7c6e2-125">CN</span><span class="sxs-lookup"><span data-stu-id="7c6e2-125">CN</span></span>                | <span data-ttu-id="7c6e2-126">Instance-Type</span><span class="sxs-lookup"><span data-stu-id="7c6e2-126">Instance-Type</span></span>                                  |
| <span data-ttu-id="7c6e2-127">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="7c6e2-127">Ldap-Display-Name</span></span> | <span data-ttu-id="7c6e2-128">instanceType</span><span class="sxs-lookup"><span data-stu-id="7c6e2-128">instanceType</span></span>                                   |
| <span data-ttu-id="7c6e2-129">Taille</span><span class="sxs-lookup"><span data-stu-id="7c6e2-129">Size</span></span>              | <span data-ttu-id="7c6e2-130">4 octets.</span><span class="sxs-lookup"><span data-stu-id="7c6e2-130">4 bytes.</span></span>                                       |
| <span data-ttu-id="7c6e2-131">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="7c6e2-131">Update Privilege</span></span>  | <span data-ttu-id="7c6e2-132">Cette valeur est définie par l’administrateur de schéma.</span><span class="sxs-lookup"><span data-stu-id="7c6e2-132">This value is set by the schema administrator.</span></span> |
| <span data-ttu-id="7c6e2-133">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="7c6e2-133">Update Frequency</span></span>  | <span data-ttu-id="7c6e2-134">Lorsque l’objet est créé.</span><span class="sxs-lookup"><span data-stu-id="7c6e2-134">When the object is created.</span></span>                    |
| <span data-ttu-id="7c6e2-135">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7c6e2-135">Attribute-Id</span></span>      | <span data-ttu-id="7c6e2-136">1.2.840.113556.1.2.1</span><span class="sxs-lookup"><span data-stu-id="7c6e2-136">1.2.840.113556.1.2.1</span></span>                           |
| <span data-ttu-id="7c6e2-137">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="7c6e2-137">System-Id-Guid</span></span>    | <span data-ttu-id="7c6e2-138">bf96798c-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="7c6e2-138">bf96798c-0de6-11d0-a285-00aa003049e2</span></span>           |
| <span data-ttu-id="7c6e2-139">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7c6e2-139">Syntax</span></span>            | [<span data-ttu-id="7c6e2-140">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="7c6e2-140">**Enumeration**</span></span>](s-enumeration.md)           |



## <a name="implementations"></a><span data-ttu-id="7c6e2-141">Implémentations</span><span class="sxs-lookup"><span data-stu-id="7c6e2-141">Implementations</span></span>

-   [<span data-ttu-id="7c6e2-142">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7c6e2-142">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7c6e2-143">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7c6e2-143">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7c6e2-144">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="7c6e2-144">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="7c6e2-145">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7c6e2-145">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7c6e2-146">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7c6e2-146">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7c6e2-147">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7c6e2-147">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7c6e2-148">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7c6e2-148">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7c6e2-149">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7c6e2-149">Windows 2000 Server</span></span>



| <span data-ttu-id="7c6e2-150">Entrée</span><span class="sxs-lookup"><span data-stu-id="7c6e2-150">Entry</span></span> | <span data-ttu-id="7c6e2-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c6e2-151">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7c6e2-152">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7c6e2-152">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7c6e2-153">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7c6e2-153">MAPI-Id</span></span>                | <span data-ttu-id="7c6e2-154">0x80BD</span><span class="sxs-lookup"><span data-stu-id="7c6e2-154">0x80BD</span></span>                          |
| <span data-ttu-id="7c6e2-155">System-Only</span><span class="sxs-lookup"><span data-stu-id="7c6e2-155">System-Only</span></span>            | <span data-ttu-id="7c6e2-156">Vrai</span><span class="sxs-lookup"><span data-stu-id="7c6e2-156">True</span></span>                            |
| <span data-ttu-id="7c6e2-157">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7c6e2-157">Is-Single-Valued</span></span>       | <span data-ttu-id="7c6e2-158">Vrai</span><span class="sxs-lookup"><span data-stu-id="7c6e2-158">True</span></span>                            |
| <span data-ttu-id="7c6e2-159">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7c6e2-159">Is Indexed</span></span>             | <span data-ttu-id="7c6e2-160">Faux</span><span class="sxs-lookup"><span data-stu-id="7c6e2-160">False</span></span>                           |
| <span data-ttu-id="7c6e2-161">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7c6e2-161">In Global Catalog</span></span>      | <span data-ttu-id="7c6e2-162">Vrai</span><span class="sxs-lookup"><span data-stu-id="7c6e2-162">True</span></span>                            |
| <span data-ttu-id="7c6e2-163">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7c6e2-163">NT-Security-Descriptor</span></span> | <span data-ttu-id="7c6e2-164">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7c6e2-164">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7c6e2-165">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7c6e2-165">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7c6e2-166">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7c6e2-166">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7c6e2-167">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7c6e2-167">Search-Flags</span></span>           | <span data-ttu-id="7c6e2-168">0x00000008</span><span class="sxs-lookup"><span data-stu-id="7c6e2-168">0x00000008</span></span>                      |
| <span data-ttu-id="7c6e2-169">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7c6e2-169">System-Flags</span></span>           | <span data-ttu-id="7c6e2-170">0x00000012</span><span class="sxs-lookup"><span data-stu-id="7c6e2-170">0x00000012</span></span>                      |
| <span data-ttu-id="7c6e2-171">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7c6e2-171">Classes used in</span></span>        | [<span data-ttu-id="7c6e2-172">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="7c6e2-172">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7c6e2-173">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7c6e2-173">Windows Server 2003</span></span>



| <span data-ttu-id="7c6e2-174">Entrée</span><span class="sxs-lookup"><span data-stu-id="7c6e2-174">Entry</span></span> | <span data-ttu-id="7c6e2-175">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c6e2-175">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7c6e2-176">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7c6e2-176">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7c6e2-177">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7c6e2-177">MAPI-Id</span></span>                | <span data-ttu-id="7c6e2-178">0x80BD</span><span class="sxs-lookup"><span data-stu-id="7c6e2-178">0x80BD</span></span>                          |
| <span data-ttu-id="7c6e2-179">System-Only</span><span class="sxs-lookup"><span data-stu-id="7c6e2-179">System-Only</span></span>            | <span data-ttu-id="7c6e2-180">Vrai</span><span class="sxs-lookup"><span data-stu-id="7c6e2-180">True</span></span>                            |
| <span data-ttu-id="7c6e2-181">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7c6e2-181">Is-Single-Valued</span></span>       | <span data-ttu-id="7c6e2-182">Vrai</span><span class="sxs-lookup"><span data-stu-id="7c6e2-182">True</span></span>                            |
| <span data-ttu-id="7c6e2-183">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7c6e2-183">Is Indexed</span></span>             | <span data-ttu-id="7c6e2-184">Faux</span><span class="sxs-lookup"><span data-stu-id="7c6e2-184">False</span></span>                           |
| <span data-ttu-id="7c6e2-185">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7c6e2-185">In Global Catalog</span></span>      | <span data-ttu-id="7c6e2-186">Vrai</span><span class="sxs-lookup"><span data-stu-id="7c6e2-186">True</span></span>                            |
| <span data-ttu-id="7c6e2-187">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7c6e2-187">NT-Security-Descriptor</span></span> | <span data-ttu-id="7c6e2-188">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7c6e2-188">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7c6e2-189">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7c6e2-189">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7c6e2-190">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7c6e2-190">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7c6e2-191">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7c6e2-191">Search-Flags</span></span>           | <span data-ttu-id="7c6e2-192">0x00000008</span><span class="sxs-lookup"><span data-stu-id="7c6e2-192">0x00000008</span></span>                      |
| <span data-ttu-id="7c6e2-193">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7c6e2-193">System-Flags</span></span>           | <span data-ttu-id="7c6e2-194">0x00000012</span><span class="sxs-lookup"><span data-stu-id="7c6e2-194">0x00000012</span></span>                      |
| <span data-ttu-id="7c6e2-195">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7c6e2-195">Classes used in</span></span>        | [<span data-ttu-id="7c6e2-196">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="7c6e2-196">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="7c6e2-197">ADAM</span><span class="sxs-lookup"><span data-stu-id="7c6e2-197">ADAM</span></span>



| <span data-ttu-id="7c6e2-198">Entrée</span><span class="sxs-lookup"><span data-stu-id="7c6e2-198">Entry</span></span> | <span data-ttu-id="7c6e2-199">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c6e2-199">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7c6e2-200">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7c6e2-200">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7c6e2-201">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7c6e2-201">MAPI-Id</span></span>                | <span data-ttu-id="7c6e2-202">0x80BD</span><span class="sxs-lookup"><span data-stu-id="7c6e2-202">0x80BD</span></span>                          |
| <span data-ttu-id="7c6e2-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="7c6e2-203">System-Only</span></span>            | <span data-ttu-id="7c6e2-204">Vrai</span><span class="sxs-lookup"><span data-stu-id="7c6e2-204">True</span></span>                            |
| <span data-ttu-id="7c6e2-205">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7c6e2-205">Is-Single-Valued</span></span>       | <span data-ttu-id="7c6e2-206">Vrai</span><span class="sxs-lookup"><span data-stu-id="7c6e2-206">True</span></span>                            |
| <span data-ttu-id="7c6e2-207">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7c6e2-207">Is Indexed</span></span>             | <span data-ttu-id="7c6e2-208">Faux</span><span class="sxs-lookup"><span data-stu-id="7c6e2-208">False</span></span>                           |
| <span data-ttu-id="7c6e2-209">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7c6e2-209">In Global Catalog</span></span>      | <span data-ttu-id="7c6e2-210">Vrai</span><span class="sxs-lookup"><span data-stu-id="7c6e2-210">True</span></span>                            |
| <span data-ttu-id="7c6e2-211">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7c6e2-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="7c6e2-212">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7c6e2-212">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7c6e2-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7c6e2-213">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7c6e2-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7c6e2-214">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7c6e2-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7c6e2-215">Search-Flags</span></span>           | <span data-ttu-id="7c6e2-216">0x00000008</span><span class="sxs-lookup"><span data-stu-id="7c6e2-216">0x00000008</span></span>                      |
| <span data-ttu-id="7c6e2-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7c6e2-217">System-Flags</span></span>           | <span data-ttu-id="7c6e2-218">0x00000012</span><span class="sxs-lookup"><span data-stu-id="7c6e2-218">0x00000012</span></span>                      |
| <span data-ttu-id="7c6e2-219">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7c6e2-219">Classes used in</span></span>        | [<span data-ttu-id="7c6e2-220">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="7c6e2-220">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7c6e2-221">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7c6e2-221">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7c6e2-222">Entrée</span><span class="sxs-lookup"><span data-stu-id="7c6e2-222">Entry</span></span> | <span data-ttu-id="7c6e2-223">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c6e2-223">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7c6e2-224">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7c6e2-224">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7c6e2-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7c6e2-225">MAPI-Id</span></span>                | <span data-ttu-id="7c6e2-226">0x80BD</span><span class="sxs-lookup"><span data-stu-id="7c6e2-226">0x80BD</span></span>                          |
| <span data-ttu-id="7c6e2-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="7c6e2-227">System-Only</span></span>            | <span data-ttu-id="7c6e2-228">Vrai</span><span class="sxs-lookup"><span data-stu-id="7c6e2-228">True</span></span>                            |
| <span data-ttu-id="7c6e2-229">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7c6e2-229">Is-Single-Valued</span></span>       | <span data-ttu-id="7c6e2-230">Vrai</span><span class="sxs-lookup"><span data-stu-id="7c6e2-230">True</span></span>                            |
| <span data-ttu-id="7c6e2-231">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7c6e2-231">Is Indexed</span></span>             | <span data-ttu-id="7c6e2-232">Faux</span><span class="sxs-lookup"><span data-stu-id="7c6e2-232">False</span></span>                           |
| <span data-ttu-id="7c6e2-233">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7c6e2-233">In Global Catalog</span></span>      | <span data-ttu-id="7c6e2-234">Vrai</span><span class="sxs-lookup"><span data-stu-id="7c6e2-234">True</span></span>                            |
| <span data-ttu-id="7c6e2-235">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7c6e2-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="7c6e2-236">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7c6e2-236">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7c6e2-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7c6e2-237">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7c6e2-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7c6e2-238">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7c6e2-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7c6e2-239">Search-Flags</span></span>           | <span data-ttu-id="7c6e2-240">0x00000008</span><span class="sxs-lookup"><span data-stu-id="7c6e2-240">0x00000008</span></span>                      |
| <span data-ttu-id="7c6e2-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7c6e2-241">System-Flags</span></span>           | <span data-ttu-id="7c6e2-242">0x00000012</span><span class="sxs-lookup"><span data-stu-id="7c6e2-242">0x00000012</span></span>                      |
| <span data-ttu-id="7c6e2-243">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7c6e2-243">Classes used in</span></span>        | [<span data-ttu-id="7c6e2-244">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="7c6e2-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7c6e2-245">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7c6e2-245">Windows Server 2008</span></span>



| <span data-ttu-id="7c6e2-246">Entrée</span><span class="sxs-lookup"><span data-stu-id="7c6e2-246">Entry</span></span> | <span data-ttu-id="7c6e2-247">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c6e2-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7c6e2-248">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7c6e2-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7c6e2-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7c6e2-249">MAPI-Id</span></span>                | <span data-ttu-id="7c6e2-250">0x80BD</span><span class="sxs-lookup"><span data-stu-id="7c6e2-250">0x80BD</span></span>                          |
| <span data-ttu-id="7c6e2-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="7c6e2-251">System-Only</span></span>            | <span data-ttu-id="7c6e2-252">Vrai</span><span class="sxs-lookup"><span data-stu-id="7c6e2-252">True</span></span>                            |
| <span data-ttu-id="7c6e2-253">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7c6e2-253">Is-Single-Valued</span></span>       | <span data-ttu-id="7c6e2-254">Vrai</span><span class="sxs-lookup"><span data-stu-id="7c6e2-254">True</span></span>                            |
| <span data-ttu-id="7c6e2-255">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7c6e2-255">Is Indexed</span></span>             | <span data-ttu-id="7c6e2-256">Faux</span><span class="sxs-lookup"><span data-stu-id="7c6e2-256">False</span></span>                           |
| <span data-ttu-id="7c6e2-257">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7c6e2-257">In Global Catalog</span></span>      | <span data-ttu-id="7c6e2-258">Vrai</span><span class="sxs-lookup"><span data-stu-id="7c6e2-258">True</span></span>                            |
| <span data-ttu-id="7c6e2-259">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7c6e2-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="7c6e2-260">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7c6e2-260">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7c6e2-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7c6e2-261">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7c6e2-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7c6e2-262">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7c6e2-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7c6e2-263">Search-Flags</span></span>           | <span data-ttu-id="7c6e2-264">0x00000008</span><span class="sxs-lookup"><span data-stu-id="7c6e2-264">0x00000008</span></span>                      |
| <span data-ttu-id="7c6e2-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7c6e2-265">System-Flags</span></span>           | <span data-ttu-id="7c6e2-266">0x00000012</span><span class="sxs-lookup"><span data-stu-id="7c6e2-266">0x00000012</span></span>                      |
| <span data-ttu-id="7c6e2-267">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7c6e2-267">Classes used in</span></span>        | [<span data-ttu-id="7c6e2-268">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="7c6e2-268">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7c6e2-269">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7c6e2-269">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7c6e2-270">Entrée</span><span class="sxs-lookup"><span data-stu-id="7c6e2-270">Entry</span></span> | <span data-ttu-id="7c6e2-271">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c6e2-271">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7c6e2-272">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7c6e2-272">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7c6e2-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7c6e2-273">MAPI-Id</span></span>                | <span data-ttu-id="7c6e2-274">0x80BD</span><span class="sxs-lookup"><span data-stu-id="7c6e2-274">0x80BD</span></span>                          |
| <span data-ttu-id="7c6e2-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="7c6e2-275">System-Only</span></span>            | <span data-ttu-id="7c6e2-276">Vrai</span><span class="sxs-lookup"><span data-stu-id="7c6e2-276">True</span></span>                            |
| <span data-ttu-id="7c6e2-277">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7c6e2-277">Is-Single-Valued</span></span>       | <span data-ttu-id="7c6e2-278">Vrai</span><span class="sxs-lookup"><span data-stu-id="7c6e2-278">True</span></span>                            |
| <span data-ttu-id="7c6e2-279">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7c6e2-279">Is Indexed</span></span>             | <span data-ttu-id="7c6e2-280">Faux</span><span class="sxs-lookup"><span data-stu-id="7c6e2-280">False</span></span>                           |
| <span data-ttu-id="7c6e2-281">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7c6e2-281">In Global Catalog</span></span>      | <span data-ttu-id="7c6e2-282">Vrai</span><span class="sxs-lookup"><span data-stu-id="7c6e2-282">True</span></span>                            |
| <span data-ttu-id="7c6e2-283">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7c6e2-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="7c6e2-284">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7c6e2-284">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7c6e2-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7c6e2-285">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7c6e2-286">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7c6e2-286">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7c6e2-287">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7c6e2-287">Search-Flags</span></span>           | <span data-ttu-id="7c6e2-288">0x00000008</span><span class="sxs-lookup"><span data-stu-id="7c6e2-288">0x00000008</span></span>                      |
| <span data-ttu-id="7c6e2-289">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7c6e2-289">System-Flags</span></span>           | <span data-ttu-id="7c6e2-290">0x00000012</span><span class="sxs-lookup"><span data-stu-id="7c6e2-290">0x00000012</span></span>                      |
| <span data-ttu-id="7c6e2-291">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7c6e2-291">Classes used in</span></span>        | [<span data-ttu-id="7c6e2-292">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="7c6e2-292">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7c6e2-293">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7c6e2-293">Windows Server 2012</span></span>



| <span data-ttu-id="7c6e2-294">Entrée</span><span class="sxs-lookup"><span data-stu-id="7c6e2-294">Entry</span></span> | <span data-ttu-id="7c6e2-295">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c6e2-295">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7c6e2-296">ID de lien</span><span class="sxs-lookup"><span data-stu-id="7c6e2-296">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7c6e2-297">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7c6e2-297">MAPI-Id</span></span>                | <span data-ttu-id="7c6e2-298">0x80BD</span><span class="sxs-lookup"><span data-stu-id="7c6e2-298">0x80BD</span></span>                          |
| <span data-ttu-id="7c6e2-299">System-Only</span><span class="sxs-lookup"><span data-stu-id="7c6e2-299">System-Only</span></span>            | <span data-ttu-id="7c6e2-300">Vrai</span><span class="sxs-lookup"><span data-stu-id="7c6e2-300">True</span></span>                            |
| <span data-ttu-id="7c6e2-301">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="7c6e2-301">Is-Single-Valued</span></span>       | <span data-ttu-id="7c6e2-302">Vrai</span><span class="sxs-lookup"><span data-stu-id="7c6e2-302">True</span></span>                            |
| <span data-ttu-id="7c6e2-303">Est indexé</span><span class="sxs-lookup"><span data-stu-id="7c6e2-303">Is Indexed</span></span>             | <span data-ttu-id="7c6e2-304">Faux</span><span class="sxs-lookup"><span data-stu-id="7c6e2-304">False</span></span>                           |
| <span data-ttu-id="7c6e2-305">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="7c6e2-305">In Global Catalog</span></span>      | <span data-ttu-id="7c6e2-306">Vrai</span><span class="sxs-lookup"><span data-stu-id="7c6e2-306">True</span></span>                            |
| <span data-ttu-id="7c6e2-307">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="7c6e2-307">NT-Security-Descriptor</span></span> | <span data-ttu-id="7c6e2-308">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="7c6e2-308">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7c6e2-309">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7c6e2-309">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7c6e2-310">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7c6e2-310">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7c6e2-311">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7c6e2-311">Search-Flags</span></span>           | <span data-ttu-id="7c6e2-312">0x00000008</span><span class="sxs-lookup"><span data-stu-id="7c6e2-312">0x00000008</span></span>                      |
| <span data-ttu-id="7c6e2-313">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7c6e2-313">System-Flags</span></span>           | <span data-ttu-id="7c6e2-314">0x00000012</span><span class="sxs-lookup"><span data-stu-id="7c6e2-314">0x00000012</span></span>                      |
| <span data-ttu-id="7c6e2-315">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="7c6e2-315">Classes used in</span></span>        | [<span data-ttu-id="7c6e2-316">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="7c6e2-316">**Top**</span></span>](c-top.md)<br/> |



 

 





