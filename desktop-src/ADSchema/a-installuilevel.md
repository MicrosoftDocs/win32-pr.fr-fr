---
title: Install-attribut au niveau de l’interface utilisateur
description: Cet attribut contient des informations sur le type (niveau) d’installation utilisé pour l’interface utilisateur.
ms.assetid: 718e04c7-ea96-4519-b312-12534ffd66df
ms.tgt_platform: multiple
keywords:
- Installer-attribut au niveau de l’interface utilisateur schéma AD
- Schéma AD de l’attribut installUiLevel
topic_type:
- apiref
api_name:
- Install-Ui-Level
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b93900bb401d1bdcd72f8881fb78026745c4e8f6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103942998"
---
# <a name="install-ui-level-attribute"></a><span data-ttu-id="c1e1d-105">Install-attribut au niveau de l’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="c1e1d-105">Install-Ui-Level attribute</span></span>

<span data-ttu-id="c1e1d-106">Cet attribut contient des informations sur le type (niveau) d’installation utilisé pour l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c1e1d-106">This attribute contains information for the type (level) of installation that is used for the user interface.</span></span> <span data-ttu-id="c1e1d-107">Les niveaux d’installation possibles sont les suivants : 2 INSTALLUILEVEL \_ aucun (installation sans assistance) 3 INSTALLUILEVEL \_ de base (installation simple avec gestion des erreurs) 4 INSTALLUILEVEL \_ réduit (IU créée, boîtes de dialogue de l’Assistant supprimées) 5 INSTALLUILEVEL \_ complet (interface utilisateur créée avec les assistants, progression, erreurs)</span><span class="sxs-lookup"><span data-stu-id="c1e1d-107">Possible installation levels are as follows: 2 INSTALLUILEVEL\_NONE (silent installation) 3 INSTALLUILEVEL\_BASIC (simple installation with error handling) 4 INSTALLUILEVEL\_REDUCED (authored UI, wizard dialog boxes suppressed) 5 INSTALLUILEVEL\_FULL (authored UI with wizards, progress, errors)</span></span>



| <span data-ttu-id="c1e1d-108">Entrée</span><span class="sxs-lookup"><span data-stu-id="c1e1d-108">Entry</span></span> | <span data-ttu-id="c1e1d-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="c1e1d-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="c1e1d-110">CN</span><span class="sxs-lookup"><span data-stu-id="c1e1d-110">CN</span></span>                | <span data-ttu-id="c1e1d-111">Installer-au niveau de l’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="c1e1d-111">Install-Ui-Level</span></span>                     |
| <span data-ttu-id="c1e1d-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="c1e1d-112">Ldap-Display-Name</span></span> | <span data-ttu-id="c1e1d-113">installUiLevel</span><span class="sxs-lookup"><span data-stu-id="c1e1d-113">installUiLevel</span></span>                       |
| <span data-ttu-id="c1e1d-114">Taille</span><span class="sxs-lookup"><span data-stu-id="c1e1d-114">Size</span></span>              | \-                                   |
| <span data-ttu-id="c1e1d-115">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="c1e1d-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="c1e1d-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="c1e1d-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="c1e1d-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c1e1d-117">Attribute-Id</span></span>      | <span data-ttu-id="c1e1d-118">1.2.840.113556.1.4.847</span><span class="sxs-lookup"><span data-stu-id="c1e1d-118">1.2.840.113556.1.4.847</span></span>               |
| <span data-ttu-id="c1e1d-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c1e1d-119">System-Id-Guid</span></span>    | <span data-ttu-id="c1e1d-120">96a7dd64-9118-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="c1e1d-120">96a7dd64-9118-11d1-aebc-0000f80367c1</span></span> |
| <span data-ttu-id="c1e1d-121">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c1e1d-121">Syntax</span></span>            | [<span data-ttu-id="c1e1d-122">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="c1e1d-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="c1e1d-123">Implémentations</span><span class="sxs-lookup"><span data-stu-id="c1e1d-123">Implementations</span></span>

-   [<span data-ttu-id="c1e1d-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c1e1d-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c1e1d-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c1e1d-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c1e1d-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c1e1d-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c1e1d-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c1e1d-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c1e1d-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c1e1d-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c1e1d-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c1e1d-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c1e1d-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c1e1d-130">Windows 2000 Server</span></span>



| <span data-ttu-id="c1e1d-131">Entrée</span><span class="sxs-lookup"><span data-stu-id="c1e1d-131">Entry</span></span> | <span data-ttu-id="c1e1d-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="c1e1d-132">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="c1e1d-133">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c1e1d-133">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="c1e1d-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c1e1d-134">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="c1e1d-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="c1e1d-135">System-Only</span></span>            | <span data-ttu-id="c1e1d-136">Faux</span><span class="sxs-lookup"><span data-stu-id="c1e1d-136">False</span></span>                                                            |
| <span data-ttu-id="c1e1d-137">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c1e1d-137">Is-Single-Valued</span></span>       | <span data-ttu-id="c1e1d-138">Vrai</span><span class="sxs-lookup"><span data-stu-id="c1e1d-138">True</span></span>                                                             |
| <span data-ttu-id="c1e1d-139">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c1e1d-139">Is Indexed</span></span>             | <span data-ttu-id="c1e1d-140">Faux</span><span class="sxs-lookup"><span data-stu-id="c1e1d-140">False</span></span>                                                            |
| <span data-ttu-id="c1e1d-141">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c1e1d-141">In Global Catalog</span></span>      | <span data-ttu-id="c1e1d-142">Faux</span><span class="sxs-lookup"><span data-stu-id="c1e1d-142">False</span></span>                                                            |
| <span data-ttu-id="c1e1d-143">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c1e1d-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="c1e1d-144">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c1e1d-144">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="c1e1d-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c1e1d-145">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="c1e1d-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c1e1d-146">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="c1e1d-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c1e1d-147">Search-Flags</span></span>           | <span data-ttu-id="c1e1d-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c1e1d-148">0x00000000</span></span>                                                       |
| <span data-ttu-id="c1e1d-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c1e1d-149">System-Flags</span></span>           | <span data-ttu-id="c1e1d-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c1e1d-150">0x00000010</span></span>                                                       |
| <span data-ttu-id="c1e1d-151">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c1e1d-151">Classes used in</span></span>        | [<span data-ttu-id="c1e1d-152">**Inscription de packages**</span><span class="sxs-lookup"><span data-stu-id="c1e1d-152">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c1e1d-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c1e1d-153">Windows Server 2003</span></span>



| <span data-ttu-id="c1e1d-154">Entrée</span><span class="sxs-lookup"><span data-stu-id="c1e1d-154">Entry</span></span> | <span data-ttu-id="c1e1d-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="c1e1d-155">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="c1e1d-156">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c1e1d-156">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="c1e1d-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c1e1d-157">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="c1e1d-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="c1e1d-158">System-Only</span></span>            | <span data-ttu-id="c1e1d-159">Faux</span><span class="sxs-lookup"><span data-stu-id="c1e1d-159">False</span></span>                                                            |
| <span data-ttu-id="c1e1d-160">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c1e1d-160">Is-Single-Valued</span></span>       | <span data-ttu-id="c1e1d-161">Vrai</span><span class="sxs-lookup"><span data-stu-id="c1e1d-161">True</span></span>                                                             |
| <span data-ttu-id="c1e1d-162">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c1e1d-162">Is Indexed</span></span>             | <span data-ttu-id="c1e1d-163">Faux</span><span class="sxs-lookup"><span data-stu-id="c1e1d-163">False</span></span>                                                            |
| <span data-ttu-id="c1e1d-164">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c1e1d-164">In Global Catalog</span></span>      | <span data-ttu-id="c1e1d-165">Faux</span><span class="sxs-lookup"><span data-stu-id="c1e1d-165">False</span></span>                                                            |
| <span data-ttu-id="c1e1d-166">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c1e1d-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="c1e1d-167">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c1e1d-167">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="c1e1d-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c1e1d-168">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="c1e1d-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c1e1d-169">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="c1e1d-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c1e1d-170">Search-Flags</span></span>           | <span data-ttu-id="c1e1d-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c1e1d-171">0x00000000</span></span>                                                       |
| <span data-ttu-id="c1e1d-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c1e1d-172">System-Flags</span></span>           | <span data-ttu-id="c1e1d-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c1e1d-173">0x00000010</span></span>                                                       |
| <span data-ttu-id="c1e1d-174">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c1e1d-174">Classes used in</span></span>        | [<span data-ttu-id="c1e1d-175">**Inscription de packages**</span><span class="sxs-lookup"><span data-stu-id="c1e1d-175">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c1e1d-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c1e1d-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c1e1d-177">Entrée</span><span class="sxs-lookup"><span data-stu-id="c1e1d-177">Entry</span></span> | <span data-ttu-id="c1e1d-178">Valeur</span><span class="sxs-lookup"><span data-stu-id="c1e1d-178">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="c1e1d-179">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c1e1d-179">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="c1e1d-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c1e1d-180">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="c1e1d-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="c1e1d-181">System-Only</span></span>            | <span data-ttu-id="c1e1d-182">Faux</span><span class="sxs-lookup"><span data-stu-id="c1e1d-182">False</span></span>                                                            |
| <span data-ttu-id="c1e1d-183">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c1e1d-183">Is-Single-Valued</span></span>       | <span data-ttu-id="c1e1d-184">Vrai</span><span class="sxs-lookup"><span data-stu-id="c1e1d-184">True</span></span>                                                             |
| <span data-ttu-id="c1e1d-185">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c1e1d-185">Is Indexed</span></span>             | <span data-ttu-id="c1e1d-186">Faux</span><span class="sxs-lookup"><span data-stu-id="c1e1d-186">False</span></span>                                                            |
| <span data-ttu-id="c1e1d-187">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c1e1d-187">In Global Catalog</span></span>      | <span data-ttu-id="c1e1d-188">Faux</span><span class="sxs-lookup"><span data-stu-id="c1e1d-188">False</span></span>                                                            |
| <span data-ttu-id="c1e1d-189">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c1e1d-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="c1e1d-190">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c1e1d-190">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="c1e1d-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c1e1d-191">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="c1e1d-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c1e1d-192">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="c1e1d-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c1e1d-193">Search-Flags</span></span>           | <span data-ttu-id="c1e1d-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c1e1d-194">0x00000000</span></span>                                                       |
| <span data-ttu-id="c1e1d-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c1e1d-195">System-Flags</span></span>           | <span data-ttu-id="c1e1d-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c1e1d-196">0x00000010</span></span>                                                       |
| <span data-ttu-id="c1e1d-197">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c1e1d-197">Classes used in</span></span>        | [<span data-ttu-id="c1e1d-198">**Inscription de packages**</span><span class="sxs-lookup"><span data-stu-id="c1e1d-198">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c1e1d-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c1e1d-199">Windows Server 2008</span></span>



| <span data-ttu-id="c1e1d-200">Entrée</span><span class="sxs-lookup"><span data-stu-id="c1e1d-200">Entry</span></span> | <span data-ttu-id="c1e1d-201">Valeur</span><span class="sxs-lookup"><span data-stu-id="c1e1d-201">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="c1e1d-202">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c1e1d-202">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="c1e1d-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c1e1d-203">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="c1e1d-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="c1e1d-204">System-Only</span></span>            | <span data-ttu-id="c1e1d-205">Faux</span><span class="sxs-lookup"><span data-stu-id="c1e1d-205">False</span></span>                                                            |
| <span data-ttu-id="c1e1d-206">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c1e1d-206">Is-Single-Valued</span></span>       | <span data-ttu-id="c1e1d-207">Vrai</span><span class="sxs-lookup"><span data-stu-id="c1e1d-207">True</span></span>                                                             |
| <span data-ttu-id="c1e1d-208">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c1e1d-208">Is Indexed</span></span>             | <span data-ttu-id="c1e1d-209">Faux</span><span class="sxs-lookup"><span data-stu-id="c1e1d-209">False</span></span>                                                            |
| <span data-ttu-id="c1e1d-210">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c1e1d-210">In Global Catalog</span></span>      | <span data-ttu-id="c1e1d-211">Faux</span><span class="sxs-lookup"><span data-stu-id="c1e1d-211">False</span></span>                                                            |
| <span data-ttu-id="c1e1d-212">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c1e1d-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="c1e1d-213">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c1e1d-213">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="c1e1d-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c1e1d-214">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="c1e1d-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c1e1d-215">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="c1e1d-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c1e1d-216">Search-Flags</span></span>           | <span data-ttu-id="c1e1d-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c1e1d-217">0x00000000</span></span>                                                       |
| <span data-ttu-id="c1e1d-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c1e1d-218">System-Flags</span></span>           | <span data-ttu-id="c1e1d-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c1e1d-219">0x00000010</span></span>                                                       |
| <span data-ttu-id="c1e1d-220">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c1e1d-220">Classes used in</span></span>        | [<span data-ttu-id="c1e1d-221">**Inscription de packages**</span><span class="sxs-lookup"><span data-stu-id="c1e1d-221">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c1e1d-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c1e1d-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c1e1d-223">Entrée</span><span class="sxs-lookup"><span data-stu-id="c1e1d-223">Entry</span></span> | <span data-ttu-id="c1e1d-224">Valeur</span><span class="sxs-lookup"><span data-stu-id="c1e1d-224">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="c1e1d-225">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c1e1d-225">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="c1e1d-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c1e1d-226">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="c1e1d-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="c1e1d-227">System-Only</span></span>            | <span data-ttu-id="c1e1d-228">Faux</span><span class="sxs-lookup"><span data-stu-id="c1e1d-228">False</span></span>                                                            |
| <span data-ttu-id="c1e1d-229">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c1e1d-229">Is-Single-Valued</span></span>       | <span data-ttu-id="c1e1d-230">Vrai</span><span class="sxs-lookup"><span data-stu-id="c1e1d-230">True</span></span>                                                             |
| <span data-ttu-id="c1e1d-231">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c1e1d-231">Is Indexed</span></span>             | <span data-ttu-id="c1e1d-232">Faux</span><span class="sxs-lookup"><span data-stu-id="c1e1d-232">False</span></span>                                                            |
| <span data-ttu-id="c1e1d-233">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c1e1d-233">In Global Catalog</span></span>      | <span data-ttu-id="c1e1d-234">Faux</span><span class="sxs-lookup"><span data-stu-id="c1e1d-234">False</span></span>                                                            |
| <span data-ttu-id="c1e1d-235">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c1e1d-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="c1e1d-236">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c1e1d-236">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="c1e1d-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c1e1d-237">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="c1e1d-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c1e1d-238">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="c1e1d-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c1e1d-239">Search-Flags</span></span>           | <span data-ttu-id="c1e1d-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c1e1d-240">0x00000000</span></span>                                                       |
| <span data-ttu-id="c1e1d-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c1e1d-241">System-Flags</span></span>           | <span data-ttu-id="c1e1d-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c1e1d-242">0x00000010</span></span>                                                       |
| <span data-ttu-id="c1e1d-243">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c1e1d-243">Classes used in</span></span>        | [<span data-ttu-id="c1e1d-244">**Inscription de packages**</span><span class="sxs-lookup"><span data-stu-id="c1e1d-244">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c1e1d-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c1e1d-245">Windows Server 2012</span></span>



| <span data-ttu-id="c1e1d-246">Entrée</span><span class="sxs-lookup"><span data-stu-id="c1e1d-246">Entry</span></span> | <span data-ttu-id="c1e1d-247">Valeur</span><span class="sxs-lookup"><span data-stu-id="c1e1d-247">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="c1e1d-248">ID de lien</span><span class="sxs-lookup"><span data-stu-id="c1e1d-248">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="c1e1d-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c1e1d-249">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="c1e1d-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="c1e1d-250">System-Only</span></span>            | <span data-ttu-id="c1e1d-251">Faux</span><span class="sxs-lookup"><span data-stu-id="c1e1d-251">False</span></span>                                                            |
| <span data-ttu-id="c1e1d-252">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="c1e1d-252">Is-Single-Valued</span></span>       | <span data-ttu-id="c1e1d-253">Vrai</span><span class="sxs-lookup"><span data-stu-id="c1e1d-253">True</span></span>                                                             |
| <span data-ttu-id="c1e1d-254">Est indexé</span><span class="sxs-lookup"><span data-stu-id="c1e1d-254">Is Indexed</span></span>             | <span data-ttu-id="c1e1d-255">Faux</span><span class="sxs-lookup"><span data-stu-id="c1e1d-255">False</span></span>                                                            |
| <span data-ttu-id="c1e1d-256">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="c1e1d-256">In Global Catalog</span></span>      | <span data-ttu-id="c1e1d-257">Faux</span><span class="sxs-lookup"><span data-stu-id="c1e1d-257">False</span></span>                                                            |
| <span data-ttu-id="c1e1d-258">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="c1e1d-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="c1e1d-259">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="c1e1d-259">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="c1e1d-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c1e1d-260">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="c1e1d-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c1e1d-261">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="c1e1d-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c1e1d-262">Search-Flags</span></span>           | <span data-ttu-id="c1e1d-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c1e1d-263">0x00000000</span></span>                                                       |
| <span data-ttu-id="c1e1d-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c1e1d-264">System-Flags</span></span>           | <span data-ttu-id="c1e1d-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c1e1d-265">0x00000010</span></span>                                                       |
| <span data-ttu-id="c1e1d-266">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="c1e1d-266">Classes used in</span></span>        | [<span data-ttu-id="c1e1d-267">**Inscription de packages**</span><span class="sxs-lookup"><span data-stu-id="c1e1d-267">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



 

 





