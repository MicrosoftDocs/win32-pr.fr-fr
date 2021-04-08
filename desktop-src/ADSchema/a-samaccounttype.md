---
title: Attribut SAM-Account-type
description: Cet attribut contient des informations sur chaque objet de type de compte.
ms.assetid: 00479b89-1d96-4ace-bbd8-053ca9e548b0
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut SAM-Account-type
- Schéma AD de l’attribut sAMAccountType
topic_type:
- apiref
api_name:
- SAM-Account-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f51de46dac0faabcc248159f7dcabafcd6060725
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103943104"
---
# <a name="sam-account-type-attribute"></a><span data-ttu-id="f15ab-105">Attribut SAM-Account-type</span><span class="sxs-lookup"><span data-stu-id="f15ab-105">SAM-Account-Type attribute</span></span>

<span data-ttu-id="f15ab-106">Cet attribut contient des informations sur chaque objet de type de compte.</span><span class="sxs-lookup"><span data-stu-id="f15ab-106">This attribute contains information about every account type object.</span></span> <span data-ttu-id="f15ab-107">Vous pouvez énumérer une liste de types de comptes, ou vous pouvez utiliser l’API afficher les informations pour créer une liste.</span><span class="sxs-lookup"><span data-stu-id="f15ab-107">You can enumerate a list of account types or you can use the Display Information API to create a list.</span></span> <span data-ttu-id="f15ab-108">Étant donné que les ordinateurs, les comptes d’utilisateurs normaux et les comptes de confiance peuvent également être énumérés en tant qu’objets utilisateur, les valeurs de ces comptes doivent être une plage contiguë.</span><span class="sxs-lookup"><span data-stu-id="f15ab-108">Because computers, normal user accounts, and trust accounts can also be enumerated as user objects, the values for these accounts must be a contiguous range.</span></span>

<span data-ttu-id="f15ab-109">Les valeurs possibles pour cet attribut sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="f15ab-109">The possible values for this attribute are the following:</span></span>

-   <span data-ttu-id="f15ab-110">\_Objet de domaine sam \_ 0x0</span><span class="sxs-lookup"><span data-stu-id="f15ab-110">SAM\_DOMAIN\_OBJECT 0x0</span></span>
-   <span data-ttu-id="f15ab-111">\_Objet de groupe sam \_ 0x10000000</span><span class="sxs-lookup"><span data-stu-id="f15ab-111">SAM\_GROUP\_OBJECT 0x10000000</span></span>
-   <span data-ttu-id="f15ab-112">SAM \_ objet de groupe non de \_ sécurité \_ \_ 0x10000001</span><span class="sxs-lookup"><span data-stu-id="f15ab-112">SAM\_NON\_SECURITY\_GROUP\_OBJECT 0x10000001</span></span>
-   <span data-ttu-id="f15ab-113">\_Objet alias Sam \_ 0x20000000</span><span class="sxs-lookup"><span data-stu-id="f15ab-113">SAM\_ALIAS\_OBJECT 0x20000000</span></span>
-   <span data-ttu-id="f15ab-114">SAM \_ non- \_ sécurité d’objet d' \_ alias \_ 0x20000001</span><span class="sxs-lookup"><span data-stu-id="f15ab-114">SAM\_NON\_SECURITY\_ALIAS\_OBJECT 0x20000001</span></span>
-   <span data-ttu-id="f15ab-115">SAM \_ User, \_ objet 0x30000000</span><span class="sxs-lookup"><span data-stu-id="f15ab-115">SAM\_USER\_OBJECT 0x30000000</span></span>
-   <span data-ttu-id="f15ab-116">SAM \_ \_ compte d’utilisateur normal \_ 0x30000000</span><span class="sxs-lookup"><span data-stu-id="f15ab-116">SAM\_NORMAL\_USER\_ACCOUNT 0x30000000</span></span>
-   <span data-ttu-id="f15ab-117">\_Compte d’ordinateur sam \_ 0x30000001</span><span class="sxs-lookup"><span data-stu-id="f15ab-117">SAM\_MACHINE\_ACCOUNT 0x30000001</span></span>
-   <span data-ttu-id="f15ab-118">\_Compte de confiance sam \_ 0x30000002</span><span class="sxs-lookup"><span data-stu-id="f15ab-118">SAM\_TRUST\_ACCOUNT 0x30000002</span></span>
-   <span data-ttu-id="f15ab-119">SAM \_ app \_ Basic \_ Group 0x40000000</span><span class="sxs-lookup"><span data-stu-id="f15ab-119">SAM\_APP\_BASIC\_GROUP 0x40000000</span></span>
-   <span data-ttu-id="f15ab-120">SAM \_ \_ 0x40000001 groupe de requêtes d’application \_</span><span class="sxs-lookup"><span data-stu-id="f15ab-120">SAM\_APP\_QUERY\_GROUP 0x40000001</span></span>
-   <span data-ttu-id="f15ab-121">\_Type de compte Sam \_ \_ Max 0x7FFFFFFF</span><span class="sxs-lookup"><span data-stu-id="f15ab-121">SAM\_ACCOUNT\_TYPE\_MAX 0x7fffffff</span></span>



| <span data-ttu-id="f15ab-122">Entrée</span><span class="sxs-lookup"><span data-stu-id="f15ab-122">Entry</span></span> | <span data-ttu-id="f15ab-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="f15ab-123">Value</span></span> |
|-------------------|-----------------------------------------------------------------|
| <span data-ttu-id="f15ab-124">CN</span><span class="sxs-lookup"><span data-stu-id="f15ab-124">CN</span></span>                | <span data-ttu-id="f15ab-125">Type de compte SAM</span><span class="sxs-lookup"><span data-stu-id="f15ab-125">SAM-Account-Type</span></span>                                                |
| <span data-ttu-id="f15ab-126">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f15ab-126">Ldap-Display-Name</span></span> | <span data-ttu-id="f15ab-127">sAMAccountType</span><span class="sxs-lookup"><span data-stu-id="f15ab-127">sAMAccountType</span></span>                                                  |
| <span data-ttu-id="f15ab-128">Taille</span><span class="sxs-lookup"><span data-stu-id="f15ab-128">Size</span></span>              | \-                                                              |
| <span data-ttu-id="f15ab-129">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="f15ab-129">Update Privilege</span></span>  | <span data-ttu-id="f15ab-130">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="f15ab-130">This value is set by the system.</span></span>                                |
| <span data-ttu-id="f15ab-131">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="f15ab-131">Update Frequency</span></span>  | <span data-ttu-id="f15ab-132">Cela est défini par le système d’exploitation lors de la création de l’objet.</span><span class="sxs-lookup"><span data-stu-id="f15ab-132">This is set by the operating system when the object is created.</span></span> |
| <span data-ttu-id="f15ab-133">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f15ab-133">Attribute-Id</span></span>      | <span data-ttu-id="f15ab-134">1.2.840.113556.1.4.302</span><span class="sxs-lookup"><span data-stu-id="f15ab-134">1.2.840.113556.1.4.302</span></span>                                          |
| <span data-ttu-id="f15ab-135">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f15ab-135">System-Id-Guid</span></span>    | <span data-ttu-id="f15ab-136">6e7b626c-64f2-11d0-afd2-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="f15ab-136">6e7b626c-64f2-11d0-afd2-00c04fd930c9</span></span>                            |
| <span data-ttu-id="f15ab-137">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f15ab-137">Syntax</span></span>            | [<span data-ttu-id="f15ab-138">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="f15ab-138">**Enumeration**</span></span>](s-enumeration.md)                            |



## <a name="implementations"></a><span data-ttu-id="f15ab-139">Implémentations</span><span class="sxs-lookup"><span data-stu-id="f15ab-139">Implementations</span></span>

-   [<span data-ttu-id="f15ab-140">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f15ab-140">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f15ab-141">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f15ab-141">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f15ab-142">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f15ab-142">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f15ab-143">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f15ab-143">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f15ab-144">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f15ab-144">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f15ab-145">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f15ab-145">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f15ab-146">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f15ab-146">Windows 2000 Server</span></span>



| <span data-ttu-id="f15ab-147">Entrée</span><span class="sxs-lookup"><span data-stu-id="f15ab-147">Entry</span></span> | <span data-ttu-id="f15ab-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="f15ab-148">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="f15ab-149">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f15ab-149">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="f15ab-150">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f15ab-150">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="f15ab-151">System-Only</span><span class="sxs-lookup"><span data-stu-id="f15ab-151">System-Only</span></span>            | <span data-ttu-id="f15ab-152">Faux</span><span class="sxs-lookup"><span data-stu-id="f15ab-152">False</span></span>                                                        |
| <span data-ttu-id="f15ab-153">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f15ab-153">Is-Single-Valued</span></span>       | <span data-ttu-id="f15ab-154">Vrai</span><span class="sxs-lookup"><span data-stu-id="f15ab-154">True</span></span>                                                         |
| <span data-ttu-id="f15ab-155">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f15ab-155">Is Indexed</span></span>             | <span data-ttu-id="f15ab-156">Vrai</span><span class="sxs-lookup"><span data-stu-id="f15ab-156">True</span></span>                                                         |
| <span data-ttu-id="f15ab-157">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f15ab-157">In Global Catalog</span></span>      | <span data-ttu-id="f15ab-158">Vrai</span><span class="sxs-lookup"><span data-stu-id="f15ab-158">True</span></span>                                                         |
| <span data-ttu-id="f15ab-159">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f15ab-159">NT-Security-Descriptor</span></span> | <span data-ttu-id="f15ab-160">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f15ab-160">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="f15ab-161">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f15ab-161">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="f15ab-162">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f15ab-162">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="f15ab-163">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f15ab-163">Search-Flags</span></span>           | <span data-ttu-id="f15ab-164">0x00000001</span><span class="sxs-lookup"><span data-stu-id="f15ab-164">0x00000001</span></span>                                                   |
| <span data-ttu-id="f15ab-165">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f15ab-165">System-Flags</span></span>           | <span data-ttu-id="f15ab-166">0x00000012</span><span class="sxs-lookup"><span data-stu-id="f15ab-166">0x00000012</span></span>                                                   |
| <span data-ttu-id="f15ab-167">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f15ab-167">Classes used in</span></span>        | [<span data-ttu-id="f15ab-168">**Sécurité-principal**</span><span class="sxs-lookup"><span data-stu-id="f15ab-168">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f15ab-169">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f15ab-169">Windows Server 2003</span></span>



| <span data-ttu-id="f15ab-170">Entrée</span><span class="sxs-lookup"><span data-stu-id="f15ab-170">Entry</span></span> | <span data-ttu-id="f15ab-171">Valeur</span><span class="sxs-lookup"><span data-stu-id="f15ab-171">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="f15ab-172">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f15ab-172">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="f15ab-173">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f15ab-173">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="f15ab-174">System-Only</span><span class="sxs-lookup"><span data-stu-id="f15ab-174">System-Only</span></span>            | <span data-ttu-id="f15ab-175">Faux</span><span class="sxs-lookup"><span data-stu-id="f15ab-175">False</span></span>                                                        |
| <span data-ttu-id="f15ab-176">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f15ab-176">Is-Single-Valued</span></span>       | <span data-ttu-id="f15ab-177">Vrai</span><span class="sxs-lookup"><span data-stu-id="f15ab-177">True</span></span>                                                         |
| <span data-ttu-id="f15ab-178">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f15ab-178">Is Indexed</span></span>             | <span data-ttu-id="f15ab-179">Vrai</span><span class="sxs-lookup"><span data-stu-id="f15ab-179">True</span></span>                                                         |
| <span data-ttu-id="f15ab-180">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f15ab-180">In Global Catalog</span></span>      | <span data-ttu-id="f15ab-181">Vrai</span><span class="sxs-lookup"><span data-stu-id="f15ab-181">True</span></span>                                                         |
| <span data-ttu-id="f15ab-182">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f15ab-182">NT-Security-Descriptor</span></span> | <span data-ttu-id="f15ab-183">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f15ab-183">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="f15ab-184">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f15ab-184">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="f15ab-185">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f15ab-185">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="f15ab-186">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f15ab-186">Search-Flags</span></span>           | <span data-ttu-id="f15ab-187">0x00000001</span><span class="sxs-lookup"><span data-stu-id="f15ab-187">0x00000001</span></span>                                                   |
| <span data-ttu-id="f15ab-188">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f15ab-188">System-Flags</span></span>           | <span data-ttu-id="f15ab-189">0x00000012</span><span class="sxs-lookup"><span data-stu-id="f15ab-189">0x00000012</span></span>                                                   |
| <span data-ttu-id="f15ab-190">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f15ab-190">Classes used in</span></span>        | [<span data-ttu-id="f15ab-191">**Sécurité-principal**</span><span class="sxs-lookup"><span data-stu-id="f15ab-191">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f15ab-192">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f15ab-192">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f15ab-193">Entrée</span><span class="sxs-lookup"><span data-stu-id="f15ab-193">Entry</span></span> | <span data-ttu-id="f15ab-194">Valeur</span><span class="sxs-lookup"><span data-stu-id="f15ab-194">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="f15ab-195">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f15ab-195">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="f15ab-196">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f15ab-196">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="f15ab-197">System-Only</span><span class="sxs-lookup"><span data-stu-id="f15ab-197">System-Only</span></span>            | <span data-ttu-id="f15ab-198">Faux</span><span class="sxs-lookup"><span data-stu-id="f15ab-198">False</span></span>                                                        |
| <span data-ttu-id="f15ab-199">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f15ab-199">Is-Single-Valued</span></span>       | <span data-ttu-id="f15ab-200">Vrai</span><span class="sxs-lookup"><span data-stu-id="f15ab-200">True</span></span>                                                         |
| <span data-ttu-id="f15ab-201">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f15ab-201">Is Indexed</span></span>             | <span data-ttu-id="f15ab-202">Vrai</span><span class="sxs-lookup"><span data-stu-id="f15ab-202">True</span></span>                                                         |
| <span data-ttu-id="f15ab-203">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f15ab-203">In Global Catalog</span></span>      | <span data-ttu-id="f15ab-204">Vrai</span><span class="sxs-lookup"><span data-stu-id="f15ab-204">True</span></span>                                                         |
| <span data-ttu-id="f15ab-205">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f15ab-205">NT-Security-Descriptor</span></span> | <span data-ttu-id="f15ab-206">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f15ab-206">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="f15ab-207">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f15ab-207">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="f15ab-208">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f15ab-208">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="f15ab-209">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f15ab-209">Search-Flags</span></span>           | <span data-ttu-id="f15ab-210">0x00000001</span><span class="sxs-lookup"><span data-stu-id="f15ab-210">0x00000001</span></span>                                                   |
| <span data-ttu-id="f15ab-211">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f15ab-211">System-Flags</span></span>           | <span data-ttu-id="f15ab-212">0x00000012</span><span class="sxs-lookup"><span data-stu-id="f15ab-212">0x00000012</span></span>                                                   |
| <span data-ttu-id="f15ab-213">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f15ab-213">Classes used in</span></span>        | [<span data-ttu-id="f15ab-214">**Sécurité-principal**</span><span class="sxs-lookup"><span data-stu-id="f15ab-214">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f15ab-215">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f15ab-215">Windows Server 2008</span></span>



| <span data-ttu-id="f15ab-216">Entrée</span><span class="sxs-lookup"><span data-stu-id="f15ab-216">Entry</span></span> | <span data-ttu-id="f15ab-217">Valeur</span><span class="sxs-lookup"><span data-stu-id="f15ab-217">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="f15ab-218">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f15ab-218">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="f15ab-219">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f15ab-219">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="f15ab-220">System-Only</span><span class="sxs-lookup"><span data-stu-id="f15ab-220">System-Only</span></span>            | <span data-ttu-id="f15ab-221">Faux</span><span class="sxs-lookup"><span data-stu-id="f15ab-221">False</span></span>                                                        |
| <span data-ttu-id="f15ab-222">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f15ab-222">Is-Single-Valued</span></span>       | <span data-ttu-id="f15ab-223">Vrai</span><span class="sxs-lookup"><span data-stu-id="f15ab-223">True</span></span>                                                         |
| <span data-ttu-id="f15ab-224">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f15ab-224">Is Indexed</span></span>             | <span data-ttu-id="f15ab-225">Vrai</span><span class="sxs-lookup"><span data-stu-id="f15ab-225">True</span></span>                                                         |
| <span data-ttu-id="f15ab-226">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f15ab-226">In Global Catalog</span></span>      | <span data-ttu-id="f15ab-227">Vrai</span><span class="sxs-lookup"><span data-stu-id="f15ab-227">True</span></span>                                                         |
| <span data-ttu-id="f15ab-228">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f15ab-228">NT-Security-Descriptor</span></span> | <span data-ttu-id="f15ab-229">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f15ab-229">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="f15ab-230">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f15ab-230">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="f15ab-231">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f15ab-231">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="f15ab-232">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f15ab-232">Search-Flags</span></span>           | <span data-ttu-id="f15ab-233">0x00000001</span><span class="sxs-lookup"><span data-stu-id="f15ab-233">0x00000001</span></span>                                                   |
| <span data-ttu-id="f15ab-234">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f15ab-234">System-Flags</span></span>           | <span data-ttu-id="f15ab-235">0x00000012</span><span class="sxs-lookup"><span data-stu-id="f15ab-235">0x00000012</span></span>                                                   |
| <span data-ttu-id="f15ab-236">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f15ab-236">Classes used in</span></span>        | [<span data-ttu-id="f15ab-237">**Sécurité-principal**</span><span class="sxs-lookup"><span data-stu-id="f15ab-237">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f15ab-238">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f15ab-238">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f15ab-239">Entrée</span><span class="sxs-lookup"><span data-stu-id="f15ab-239">Entry</span></span> | <span data-ttu-id="f15ab-240">Valeur</span><span class="sxs-lookup"><span data-stu-id="f15ab-240">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="f15ab-241">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f15ab-241">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="f15ab-242">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f15ab-242">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="f15ab-243">System-Only</span><span class="sxs-lookup"><span data-stu-id="f15ab-243">System-Only</span></span>            | <span data-ttu-id="f15ab-244">Faux</span><span class="sxs-lookup"><span data-stu-id="f15ab-244">False</span></span>                                                        |
| <span data-ttu-id="f15ab-245">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f15ab-245">Is-Single-Valued</span></span>       | <span data-ttu-id="f15ab-246">Vrai</span><span class="sxs-lookup"><span data-stu-id="f15ab-246">True</span></span>                                                         |
| <span data-ttu-id="f15ab-247">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f15ab-247">Is Indexed</span></span>             | <span data-ttu-id="f15ab-248">Vrai</span><span class="sxs-lookup"><span data-stu-id="f15ab-248">True</span></span>                                                         |
| <span data-ttu-id="f15ab-249">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f15ab-249">In Global Catalog</span></span>      | <span data-ttu-id="f15ab-250">Vrai</span><span class="sxs-lookup"><span data-stu-id="f15ab-250">True</span></span>                                                         |
| <span data-ttu-id="f15ab-251">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f15ab-251">NT-Security-Descriptor</span></span> | <span data-ttu-id="f15ab-252">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f15ab-252">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="f15ab-253">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f15ab-253">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="f15ab-254">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f15ab-254">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="f15ab-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f15ab-255">Search-Flags</span></span>           | <span data-ttu-id="f15ab-256">0x00000001</span><span class="sxs-lookup"><span data-stu-id="f15ab-256">0x00000001</span></span>                                                   |
| <span data-ttu-id="f15ab-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f15ab-257">System-Flags</span></span>           | <span data-ttu-id="f15ab-258">0x00000012</span><span class="sxs-lookup"><span data-stu-id="f15ab-258">0x00000012</span></span>                                                   |
| <span data-ttu-id="f15ab-259">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f15ab-259">Classes used in</span></span>        | [<span data-ttu-id="f15ab-260">**Sécurité-principal**</span><span class="sxs-lookup"><span data-stu-id="f15ab-260">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f15ab-261">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f15ab-261">Windows Server 2012</span></span>



| <span data-ttu-id="f15ab-262">Entrée</span><span class="sxs-lookup"><span data-stu-id="f15ab-262">Entry</span></span> | <span data-ttu-id="f15ab-263">Valeur</span><span class="sxs-lookup"><span data-stu-id="f15ab-263">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="f15ab-264">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f15ab-264">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="f15ab-265">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f15ab-265">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="f15ab-266">System-Only</span><span class="sxs-lookup"><span data-stu-id="f15ab-266">System-Only</span></span>            | <span data-ttu-id="f15ab-267">Faux</span><span class="sxs-lookup"><span data-stu-id="f15ab-267">False</span></span>                                                        |
| <span data-ttu-id="f15ab-268">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f15ab-268">Is-Single-Valued</span></span>       | <span data-ttu-id="f15ab-269">Vrai</span><span class="sxs-lookup"><span data-stu-id="f15ab-269">True</span></span>                                                         |
| <span data-ttu-id="f15ab-270">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f15ab-270">Is Indexed</span></span>             | <span data-ttu-id="f15ab-271">Vrai</span><span class="sxs-lookup"><span data-stu-id="f15ab-271">True</span></span>                                                         |
| <span data-ttu-id="f15ab-272">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f15ab-272">In Global Catalog</span></span>      | <span data-ttu-id="f15ab-273">Vrai</span><span class="sxs-lookup"><span data-stu-id="f15ab-273">True</span></span>                                                         |
| <span data-ttu-id="f15ab-274">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f15ab-274">NT-Security-Descriptor</span></span> | <span data-ttu-id="f15ab-275">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f15ab-275">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="f15ab-276">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f15ab-276">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="f15ab-277">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f15ab-277">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="f15ab-278">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f15ab-278">Search-Flags</span></span>           | <span data-ttu-id="f15ab-279">0x00000001</span><span class="sxs-lookup"><span data-stu-id="f15ab-279">0x00000001</span></span>                                                   |
| <span data-ttu-id="f15ab-280">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f15ab-280">System-Flags</span></span>           | <span data-ttu-id="f15ab-281">0x00000012</span><span class="sxs-lookup"><span data-stu-id="f15ab-281">0x00000012</span></span>                                                   |
| <span data-ttu-id="f15ab-282">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f15ab-282">Classes used in</span></span>        | [<span data-ttu-id="f15ab-283">**Sécurité-principal**</span><span class="sxs-lookup"><span data-stu-id="f15ab-283">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



 

 





