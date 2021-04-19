---
title: Attribut COM-ProgID
description: Cet attribut stocke la liste des ID de programme d’objets COM qui sont implémentés dans ce package d’application.
ms.assetid: 9d2945e4-f236-48f6-bed3-145d445ff653
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut COM-ProgID
- Schéma AD de l’attribut cOMProgID
topic_type:
- apiref
api_name:
- COM-ProgID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 686976732bedf2c4ba486186634720568d3b6c3c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106515515"
---
# <a name="com-progid-attribute"></a><span data-ttu-id="55d7e-105">Attribut COM-ProgID</span><span class="sxs-lookup"><span data-stu-id="55d7e-105">COM-ProgID attribute</span></span>

<span data-ttu-id="55d7e-106">Cet attribut stocke la liste des ID de programme d’objets COM qui sont implémentés dans ce package d’application.</span><span class="sxs-lookup"><span data-stu-id="55d7e-106">This attribute stores the list of COM object program IDs that are implemented in this application package.</span></span>



| <span data-ttu-id="55d7e-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="55d7e-107">Entry</span></span> | <span data-ttu-id="55d7e-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="55d7e-108">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="55d7e-109">CN</span><span class="sxs-lookup"><span data-stu-id="55d7e-109">CN</span></span>                | <span data-ttu-id="55d7e-110">COM-ProgID</span><span class="sxs-lookup"><span data-stu-id="55d7e-110">COM-ProgID</span></span>                                                                       |
| <span data-ttu-id="55d7e-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="55d7e-111">Ldap-Display-Name</span></span> | <span data-ttu-id="55d7e-112">cOMProgID</span><span class="sxs-lookup"><span data-stu-id="55d7e-112">cOMProgID</span></span>                                                                        |
| <span data-ttu-id="55d7e-113">Taille</span><span class="sxs-lookup"><span data-stu-id="55d7e-113">Size</span></span>              | \-                                                                               |
| <span data-ttu-id="55d7e-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="55d7e-114">Update Privilege</span></span>  | <span data-ttu-id="55d7e-115">Tout le monde peut mettre à jour cet objet en fonction de la sécurité de l’objet en cours de création.</span><span class="sxs-lookup"><span data-stu-id="55d7e-115">Anyone may update this object based on the security of the object being created.</span></span> |
| <span data-ttu-id="55d7e-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="55d7e-116">Update Frequency</span></span>  | \-                                                                               |
| <span data-ttu-id="55d7e-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="55d7e-117">Attribute-Id</span></span>      | <span data-ttu-id="55d7e-118">1.2.840.113556.1.4.21</span><span class="sxs-lookup"><span data-stu-id="55d7e-118">1.2.840.113556.1.4.21</span></span>                                                            |
| <span data-ttu-id="55d7e-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="55d7e-119">System-Id-Guid</span></span>    | <span data-ttu-id="55d7e-120">bf96793d-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="55d7e-120">bf96793d-0de6-11d0-a285-00aa003049e2</span></span>                                             |
| <span data-ttu-id="55d7e-121">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="55d7e-121">Syntax</span></span>            | [<span data-ttu-id="55d7e-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="55d7e-122">**String(Unicode)**</span></span>](s-string-unicode.md)                                      |



## <a name="implementations"></a><span data-ttu-id="55d7e-123">Implémentations</span><span class="sxs-lookup"><span data-stu-id="55d7e-123">Implementations</span></span>

-   [<span data-ttu-id="55d7e-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="55d7e-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="55d7e-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="55d7e-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="55d7e-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="55d7e-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="55d7e-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="55d7e-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="55d7e-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="55d7e-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="55d7e-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="55d7e-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="55d7e-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="55d7e-130">Windows 2000 Server</span></span>



| <span data-ttu-id="55d7e-131">Entrée</span><span class="sxs-lookup"><span data-stu-id="55d7e-131">Entry</span></span> | <span data-ttu-id="55d7e-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="55d7e-132">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55d7e-133">ID de lien</span><span class="sxs-lookup"><span data-stu-id="55d7e-133">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="55d7e-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="55d7e-134">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="55d7e-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="55d7e-135">System-Only</span></span>            | <span data-ttu-id="55d7e-136">Faux</span><span class="sxs-lookup"><span data-stu-id="55d7e-136">False</span></span>                                                                                                                         |
| <span data-ttu-id="55d7e-137">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="55d7e-137">Is-Single-Valued</span></span>       | <span data-ttu-id="55d7e-138">Faux</span><span class="sxs-lookup"><span data-stu-id="55d7e-138">False</span></span>                                                                                                                         |
| <span data-ttu-id="55d7e-139">Est indexé</span><span class="sxs-lookup"><span data-stu-id="55d7e-139">Is Indexed</span></span>             | <span data-ttu-id="55d7e-140">Faux</span><span class="sxs-lookup"><span data-stu-id="55d7e-140">False</span></span>                                                                                                                         |
| <span data-ttu-id="55d7e-141">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="55d7e-141">In Global Catalog</span></span>      | <span data-ttu-id="55d7e-142">Faux</span><span class="sxs-lookup"><span data-stu-id="55d7e-142">False</span></span>                                                                                                                         |
| <span data-ttu-id="55d7e-143">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="55d7e-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="55d7e-144">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="55d7e-144">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="55d7e-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="55d7e-145">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="55d7e-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="55d7e-146">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="55d7e-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="55d7e-147">Search-Flags</span></span>           | <span data-ttu-id="55d7e-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="55d7e-148">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="55d7e-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="55d7e-149">System-Flags</span></span>           | <span data-ttu-id="55d7e-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="55d7e-150">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="55d7e-151">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="55d7e-151">Classes used in</span></span>        | [<span data-ttu-id="55d7e-152">**Inscription de classe**</span><span class="sxs-lookup"><span data-stu-id="55d7e-152">**Class-Registration**</span></span>](c-classregistration.md)<br/> [<span data-ttu-id="55d7e-153">**Inscription de packages**</span><span class="sxs-lookup"><span data-stu-id="55d7e-153">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="55d7e-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="55d7e-154">Windows Server 2003</span></span>



| <span data-ttu-id="55d7e-155">Entrée</span><span class="sxs-lookup"><span data-stu-id="55d7e-155">Entry</span></span> | <span data-ttu-id="55d7e-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="55d7e-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55d7e-157">ID de lien</span><span class="sxs-lookup"><span data-stu-id="55d7e-157">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="55d7e-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="55d7e-158">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="55d7e-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="55d7e-159">System-Only</span></span>            | <span data-ttu-id="55d7e-160">Faux</span><span class="sxs-lookup"><span data-stu-id="55d7e-160">False</span></span>                                                                                                                         |
| <span data-ttu-id="55d7e-161">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="55d7e-161">Is-Single-Valued</span></span>       | <span data-ttu-id="55d7e-162">Faux</span><span class="sxs-lookup"><span data-stu-id="55d7e-162">False</span></span>                                                                                                                         |
| <span data-ttu-id="55d7e-163">Est indexé</span><span class="sxs-lookup"><span data-stu-id="55d7e-163">Is Indexed</span></span>             | <span data-ttu-id="55d7e-164">Faux</span><span class="sxs-lookup"><span data-stu-id="55d7e-164">False</span></span>                                                                                                                         |
| <span data-ttu-id="55d7e-165">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="55d7e-165">In Global Catalog</span></span>      | <span data-ttu-id="55d7e-166">Faux</span><span class="sxs-lookup"><span data-stu-id="55d7e-166">False</span></span>                                                                                                                         |
| <span data-ttu-id="55d7e-167">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="55d7e-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="55d7e-168">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="55d7e-168">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="55d7e-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="55d7e-169">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="55d7e-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="55d7e-170">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="55d7e-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="55d7e-171">Search-Flags</span></span>           | <span data-ttu-id="55d7e-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="55d7e-172">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="55d7e-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="55d7e-173">System-Flags</span></span>           | <span data-ttu-id="55d7e-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="55d7e-174">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="55d7e-175">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="55d7e-175">Classes used in</span></span>        | [<span data-ttu-id="55d7e-176">**Inscription de classe**</span><span class="sxs-lookup"><span data-stu-id="55d7e-176">**Class-Registration**</span></span>](c-classregistration.md)<br/> [<span data-ttu-id="55d7e-177">**Inscription de packages**</span><span class="sxs-lookup"><span data-stu-id="55d7e-177">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="55d7e-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="55d7e-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="55d7e-179">Entrée</span><span class="sxs-lookup"><span data-stu-id="55d7e-179">Entry</span></span> | <span data-ttu-id="55d7e-180">Valeur</span><span class="sxs-lookup"><span data-stu-id="55d7e-180">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55d7e-181">ID de lien</span><span class="sxs-lookup"><span data-stu-id="55d7e-181">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="55d7e-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="55d7e-182">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="55d7e-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="55d7e-183">System-Only</span></span>            | <span data-ttu-id="55d7e-184">Faux</span><span class="sxs-lookup"><span data-stu-id="55d7e-184">False</span></span>                                                                                                                         |
| <span data-ttu-id="55d7e-185">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="55d7e-185">Is-Single-Valued</span></span>       | <span data-ttu-id="55d7e-186">Faux</span><span class="sxs-lookup"><span data-stu-id="55d7e-186">False</span></span>                                                                                                                         |
| <span data-ttu-id="55d7e-187">Est indexé</span><span class="sxs-lookup"><span data-stu-id="55d7e-187">Is Indexed</span></span>             | <span data-ttu-id="55d7e-188">Faux</span><span class="sxs-lookup"><span data-stu-id="55d7e-188">False</span></span>                                                                                                                         |
| <span data-ttu-id="55d7e-189">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="55d7e-189">In Global Catalog</span></span>      | <span data-ttu-id="55d7e-190">Faux</span><span class="sxs-lookup"><span data-stu-id="55d7e-190">False</span></span>                                                                                                                         |
| <span data-ttu-id="55d7e-191">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="55d7e-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="55d7e-192">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="55d7e-192">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="55d7e-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="55d7e-193">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="55d7e-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="55d7e-194">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="55d7e-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="55d7e-195">Search-Flags</span></span>           | <span data-ttu-id="55d7e-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="55d7e-196">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="55d7e-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="55d7e-197">System-Flags</span></span>           | <span data-ttu-id="55d7e-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="55d7e-198">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="55d7e-199">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="55d7e-199">Classes used in</span></span>        | [<span data-ttu-id="55d7e-200">**Inscription de classe**</span><span class="sxs-lookup"><span data-stu-id="55d7e-200">**Class-Registration**</span></span>](c-classregistration.md)<br/> [<span data-ttu-id="55d7e-201">**Inscription de packages**</span><span class="sxs-lookup"><span data-stu-id="55d7e-201">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="55d7e-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="55d7e-202">Windows Server 2008</span></span>



| <span data-ttu-id="55d7e-203">Entrée</span><span class="sxs-lookup"><span data-stu-id="55d7e-203">Entry</span></span> | <span data-ttu-id="55d7e-204">Valeur</span><span class="sxs-lookup"><span data-stu-id="55d7e-204">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55d7e-205">ID de lien</span><span class="sxs-lookup"><span data-stu-id="55d7e-205">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="55d7e-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="55d7e-206">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="55d7e-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="55d7e-207">System-Only</span></span>            | <span data-ttu-id="55d7e-208">Faux</span><span class="sxs-lookup"><span data-stu-id="55d7e-208">False</span></span>                                                                                                                         |
| <span data-ttu-id="55d7e-209">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="55d7e-209">Is-Single-Valued</span></span>       | <span data-ttu-id="55d7e-210">Faux</span><span class="sxs-lookup"><span data-stu-id="55d7e-210">False</span></span>                                                                                                                         |
| <span data-ttu-id="55d7e-211">Est indexé</span><span class="sxs-lookup"><span data-stu-id="55d7e-211">Is Indexed</span></span>             | <span data-ttu-id="55d7e-212">Faux</span><span class="sxs-lookup"><span data-stu-id="55d7e-212">False</span></span>                                                                                                                         |
| <span data-ttu-id="55d7e-213">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="55d7e-213">In Global Catalog</span></span>      | <span data-ttu-id="55d7e-214">Faux</span><span class="sxs-lookup"><span data-stu-id="55d7e-214">False</span></span>                                                                                                                         |
| <span data-ttu-id="55d7e-215">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="55d7e-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="55d7e-216">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="55d7e-216">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="55d7e-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="55d7e-217">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="55d7e-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="55d7e-218">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="55d7e-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="55d7e-219">Search-Flags</span></span>           | <span data-ttu-id="55d7e-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="55d7e-220">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="55d7e-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="55d7e-221">System-Flags</span></span>           | <span data-ttu-id="55d7e-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="55d7e-222">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="55d7e-223">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="55d7e-223">Classes used in</span></span>        | [<span data-ttu-id="55d7e-224">**Inscription de classe**</span><span class="sxs-lookup"><span data-stu-id="55d7e-224">**Class-Registration**</span></span>](c-classregistration.md)<br/> [<span data-ttu-id="55d7e-225">**Inscription de packages**</span><span class="sxs-lookup"><span data-stu-id="55d7e-225">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="55d7e-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="55d7e-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="55d7e-227">Entrée</span><span class="sxs-lookup"><span data-stu-id="55d7e-227">Entry</span></span> | <span data-ttu-id="55d7e-228">Valeur</span><span class="sxs-lookup"><span data-stu-id="55d7e-228">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55d7e-229">ID de lien</span><span class="sxs-lookup"><span data-stu-id="55d7e-229">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="55d7e-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="55d7e-230">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="55d7e-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="55d7e-231">System-Only</span></span>            | <span data-ttu-id="55d7e-232">Faux</span><span class="sxs-lookup"><span data-stu-id="55d7e-232">False</span></span>                                                                                                                         |
| <span data-ttu-id="55d7e-233">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="55d7e-233">Is-Single-Valued</span></span>       | <span data-ttu-id="55d7e-234">Faux</span><span class="sxs-lookup"><span data-stu-id="55d7e-234">False</span></span>                                                                                                                         |
| <span data-ttu-id="55d7e-235">Est indexé</span><span class="sxs-lookup"><span data-stu-id="55d7e-235">Is Indexed</span></span>             | <span data-ttu-id="55d7e-236">Faux</span><span class="sxs-lookup"><span data-stu-id="55d7e-236">False</span></span>                                                                                                                         |
| <span data-ttu-id="55d7e-237">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="55d7e-237">In Global Catalog</span></span>      | <span data-ttu-id="55d7e-238">Faux</span><span class="sxs-lookup"><span data-stu-id="55d7e-238">False</span></span>                                                                                                                         |
| <span data-ttu-id="55d7e-239">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="55d7e-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="55d7e-240">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="55d7e-240">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="55d7e-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="55d7e-241">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="55d7e-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="55d7e-242">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="55d7e-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="55d7e-243">Search-Flags</span></span>           | <span data-ttu-id="55d7e-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="55d7e-244">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="55d7e-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="55d7e-245">System-Flags</span></span>           | <span data-ttu-id="55d7e-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="55d7e-246">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="55d7e-247">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="55d7e-247">Classes used in</span></span>        | [<span data-ttu-id="55d7e-248">**Inscription de classe**</span><span class="sxs-lookup"><span data-stu-id="55d7e-248">**Class-Registration**</span></span>](c-classregistration.md)<br/> [<span data-ttu-id="55d7e-249">**Inscription de packages**</span><span class="sxs-lookup"><span data-stu-id="55d7e-249">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="55d7e-250">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="55d7e-250">Windows Server 2012</span></span>



| <span data-ttu-id="55d7e-251">Entrée</span><span class="sxs-lookup"><span data-stu-id="55d7e-251">Entry</span></span> | <span data-ttu-id="55d7e-252">Valeur</span><span class="sxs-lookup"><span data-stu-id="55d7e-252">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55d7e-253">ID de lien</span><span class="sxs-lookup"><span data-stu-id="55d7e-253">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="55d7e-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="55d7e-254">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="55d7e-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="55d7e-255">System-Only</span></span>            | <span data-ttu-id="55d7e-256">Faux</span><span class="sxs-lookup"><span data-stu-id="55d7e-256">False</span></span>                                                                                                                         |
| <span data-ttu-id="55d7e-257">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="55d7e-257">Is-Single-Valued</span></span>       | <span data-ttu-id="55d7e-258">Faux</span><span class="sxs-lookup"><span data-stu-id="55d7e-258">False</span></span>                                                                                                                         |
| <span data-ttu-id="55d7e-259">Est indexé</span><span class="sxs-lookup"><span data-stu-id="55d7e-259">Is Indexed</span></span>             | <span data-ttu-id="55d7e-260">Faux</span><span class="sxs-lookup"><span data-stu-id="55d7e-260">False</span></span>                                                                                                                         |
| <span data-ttu-id="55d7e-261">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="55d7e-261">In Global Catalog</span></span>      | <span data-ttu-id="55d7e-262">Faux</span><span class="sxs-lookup"><span data-stu-id="55d7e-262">False</span></span>                                                                                                                         |
| <span data-ttu-id="55d7e-263">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="55d7e-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="55d7e-264">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="55d7e-264">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="55d7e-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="55d7e-265">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="55d7e-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="55d7e-266">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="55d7e-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="55d7e-267">Search-Flags</span></span>           | <span data-ttu-id="55d7e-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="55d7e-268">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="55d7e-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="55d7e-269">System-Flags</span></span>           | <span data-ttu-id="55d7e-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="55d7e-270">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="55d7e-271">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="55d7e-271">Classes used in</span></span>        | [<span data-ttu-id="55d7e-272">**Inscription de classe**</span><span class="sxs-lookup"><span data-stu-id="55d7e-272">**Class-Registration**</span></span>](c-classregistration.md)<br/> [<span data-ttu-id="55d7e-273">**Inscription de packages**</span><span class="sxs-lookup"><span data-stu-id="55d7e-273">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



 

 





