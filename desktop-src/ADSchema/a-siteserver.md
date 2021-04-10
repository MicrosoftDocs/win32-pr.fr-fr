---
title: Attribut Site-Server
description: Licence du serveur principal pour un site donné.
ms.assetid: bcae8c63-a953-4721-b2d1-96d0376592c6
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Site-Server
- Schéma AD de l’attribut siteServer
topic_type:
- apiref
api_name:
- Site-Server
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 785057cd9ea23c05d58541450dc4c92a502877e5
ms.sourcegitcommit: f10bb95039c20a9de79f21e3fcb93a543f30a00e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/05/2021
ms.locfileid: "104200637"
---
# <a name="site-server-attribute"></a><span data-ttu-id="10b20-105">Attribut Site-Server</span><span class="sxs-lookup"><span data-stu-id="10b20-105">Site-Server attribute</span></span>

<span data-ttu-id="10b20-106">Licence du serveur principal pour un site donné.</span><span class="sxs-lookup"><span data-stu-id="10b20-106">Licensing main server for a given Site.</span></span>



| <span data-ttu-id="10b20-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="10b20-107">Entry</span></span> | <span data-ttu-id="10b20-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="10b20-108">Value</span></span> |
|-------------------|----------------------------------------------|
| <span data-ttu-id="10b20-109">CN</span><span class="sxs-lookup"><span data-stu-id="10b20-109">CN</span></span>                | <span data-ttu-id="10b20-110">Site-Server</span><span class="sxs-lookup"><span data-stu-id="10b20-110">Site-Server</span></span>                                  |
| <span data-ttu-id="10b20-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="10b20-111">Ldap-Display-Name</span></span> | <span data-ttu-id="10b20-112">siteServer</span><span class="sxs-lookup"><span data-stu-id="10b20-112">siteServer</span></span>                                   |
| <span data-ttu-id="10b20-113">Taille</span><span class="sxs-lookup"><span data-stu-id="10b20-113">Size</span></span>              | \-                                           |
| <span data-ttu-id="10b20-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="10b20-114">Update Privilege</span></span>  | <span data-ttu-id="10b20-115">Administrateur de domaine</span><span class="sxs-lookup"><span data-stu-id="10b20-115">Domain administrator</span></span>                         |
| <span data-ttu-id="10b20-116">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="10b20-116">Update Frequency</span></span>  | <span data-ttu-id="10b20-117">Chaque fois que le site de gestion des licences doit être modifié.</span><span class="sxs-lookup"><span data-stu-id="10b20-117">Whenever the licensing site needs to change.</span></span> |
| <span data-ttu-id="10b20-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="10b20-118">Attribute-Id</span></span>      | <span data-ttu-id="10b20-119">1.2.840.113556.1.4.494</span><span class="sxs-lookup"><span data-stu-id="10b20-119">1.2.840.113556.1.4.494</span></span>                       |
| <span data-ttu-id="10b20-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="10b20-120">System-Id-Guid</span></span>    | <span data-ttu-id="10b20-121">1be8f17c-a9ff-11d0-afe2-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="10b20-121">1be8f17c-a9ff-11d0-afe2-00c04fd930c9</span></span>         |
| <span data-ttu-id="10b20-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="10b20-122">Syntax</span></span>            | [<span data-ttu-id="10b20-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="10b20-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)      |



## <a name="implementations"></a><span data-ttu-id="10b20-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="10b20-124">Implementations</span></span>

-   [<span data-ttu-id="10b20-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="10b20-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="10b20-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="10b20-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="10b20-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="10b20-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="10b20-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="10b20-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="10b20-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="10b20-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="10b20-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="10b20-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="10b20-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="10b20-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="10b20-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="10b20-132">Windows 2000 Server</span></span>



| <span data-ttu-id="10b20-133">Entrée</span><span class="sxs-lookup"><span data-stu-id="10b20-133">Entry</span></span> | <span data-ttu-id="10b20-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="10b20-134">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="10b20-135">ID de lien</span><span class="sxs-lookup"><span data-stu-id="10b20-135">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="10b20-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="10b20-136">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="10b20-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="10b20-137">System-Only</span></span>            | <span data-ttu-id="10b20-138">Faux</span><span class="sxs-lookup"><span data-stu-id="10b20-138">False</span></span>                                                                 |
| <span data-ttu-id="10b20-139">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="10b20-139">Is-Single-Valued</span></span>       | <span data-ttu-id="10b20-140">Faux</span><span class="sxs-lookup"><span data-stu-id="10b20-140">False</span></span>                                                                 |
| <span data-ttu-id="10b20-141">Est indexé</span><span class="sxs-lookup"><span data-stu-id="10b20-141">Is Indexed</span></span>             | <span data-ttu-id="10b20-142">Faux</span><span class="sxs-lookup"><span data-stu-id="10b20-142">False</span></span>                                                                 |
| <span data-ttu-id="10b20-143">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="10b20-143">In Global Catalog</span></span>      | <span data-ttu-id="10b20-144">Faux</span><span class="sxs-lookup"><span data-stu-id="10b20-144">False</span></span>                                                                 |
| <span data-ttu-id="10b20-145">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="10b20-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="10b20-146">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="10b20-146">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="10b20-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="10b20-147">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="10b20-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="10b20-148">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="10b20-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="10b20-149">Search-Flags</span></span>           | <span data-ttu-id="10b20-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="10b20-150">0x00000000</span></span>                                                            |
| <span data-ttu-id="10b20-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="10b20-151">System-Flags</span></span>           | <span data-ttu-id="10b20-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="10b20-152">0x00000010</span></span>                                                            |
| <span data-ttu-id="10b20-153">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="10b20-153">Classes used in</span></span>        | [<span data-ttu-id="10b20-154">**Gestion des licences-site-paramètres**</span><span class="sxs-lookup"><span data-stu-id="10b20-154">**Licensing-Site-Settings**</span></span>](c-licensingsitesettings.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="10b20-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="10b20-155">Windows Server 2003</span></span>



| <span data-ttu-id="10b20-156">Entrée</span><span class="sxs-lookup"><span data-stu-id="10b20-156">Entry</span></span> | <span data-ttu-id="10b20-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="10b20-157">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="10b20-158">ID de lien</span><span class="sxs-lookup"><span data-stu-id="10b20-158">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="10b20-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="10b20-159">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="10b20-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="10b20-160">System-Only</span></span>            | <span data-ttu-id="10b20-161">Faux</span><span class="sxs-lookup"><span data-stu-id="10b20-161">False</span></span>                                                                 |
| <span data-ttu-id="10b20-162">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="10b20-162">Is-Single-Valued</span></span>       | <span data-ttu-id="10b20-163">Faux</span><span class="sxs-lookup"><span data-stu-id="10b20-163">False</span></span>                                                                 |
| <span data-ttu-id="10b20-164">Est indexé</span><span class="sxs-lookup"><span data-stu-id="10b20-164">Is Indexed</span></span>             | <span data-ttu-id="10b20-165">Faux</span><span class="sxs-lookup"><span data-stu-id="10b20-165">False</span></span>                                                                 |
| <span data-ttu-id="10b20-166">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="10b20-166">In Global Catalog</span></span>      | <span data-ttu-id="10b20-167">Faux</span><span class="sxs-lookup"><span data-stu-id="10b20-167">False</span></span>                                                                 |
| <span data-ttu-id="10b20-168">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="10b20-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="10b20-169">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="10b20-169">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="10b20-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="10b20-170">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="10b20-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="10b20-171">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="10b20-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="10b20-172">Search-Flags</span></span>           | <span data-ttu-id="10b20-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="10b20-173">0x00000000</span></span>                                                            |
| <span data-ttu-id="10b20-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="10b20-174">System-Flags</span></span>           | <span data-ttu-id="10b20-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="10b20-175">0x00000010</span></span>                                                            |
| <span data-ttu-id="10b20-176">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="10b20-176">Classes used in</span></span>        | [<span data-ttu-id="10b20-177">**Gestion des licences-site-paramètres**</span><span class="sxs-lookup"><span data-stu-id="10b20-177">**Licensing-Site-Settings**</span></span>](c-licensingsitesettings.md)<br/> |



## <a name="adam"></a><span data-ttu-id="10b20-178">ADAM</span><span class="sxs-lookup"><span data-stu-id="10b20-178">ADAM</span></span>



| <span data-ttu-id="10b20-179">Entrée</span><span class="sxs-lookup"><span data-stu-id="10b20-179">Entry</span></span> | <span data-ttu-id="10b20-180">Valeur</span><span class="sxs-lookup"><span data-stu-id="10b20-180">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="10b20-181">ID de lien</span><span class="sxs-lookup"><span data-stu-id="10b20-181">Link-Id</span></span>                | \-           |
| <span data-ttu-id="10b20-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="10b20-182">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="10b20-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="10b20-183">System-Only</span></span>            | <span data-ttu-id="10b20-184">Faux</span><span class="sxs-lookup"><span data-stu-id="10b20-184">False</span></span>        |
| <span data-ttu-id="10b20-185">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="10b20-185">Is-Single-Valued</span></span>       | <span data-ttu-id="10b20-186">Faux</span><span class="sxs-lookup"><span data-stu-id="10b20-186">False</span></span>        |
| <span data-ttu-id="10b20-187">Est indexé</span><span class="sxs-lookup"><span data-stu-id="10b20-187">Is Indexed</span></span>             | <span data-ttu-id="10b20-188">Faux</span><span class="sxs-lookup"><span data-stu-id="10b20-188">False</span></span>        |
| <span data-ttu-id="10b20-189">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="10b20-189">In Global Catalog</span></span>      | <span data-ttu-id="10b20-190">Faux</span><span class="sxs-lookup"><span data-stu-id="10b20-190">False</span></span>        |
| <span data-ttu-id="10b20-191">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="10b20-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="10b20-192">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="10b20-192">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="10b20-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="10b20-193">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="10b20-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="10b20-194">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="10b20-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="10b20-195">Search-Flags</span></span>           | <span data-ttu-id="10b20-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="10b20-196">0x00000000</span></span>   |
| <span data-ttu-id="10b20-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="10b20-197">System-Flags</span></span>           | <span data-ttu-id="10b20-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="10b20-198">0x00000010</span></span>   |
| <span data-ttu-id="10b20-199">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="10b20-199">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="10b20-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="10b20-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="10b20-201">Entrée</span><span class="sxs-lookup"><span data-stu-id="10b20-201">Entry</span></span> | <span data-ttu-id="10b20-202">Valeur</span><span class="sxs-lookup"><span data-stu-id="10b20-202">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="10b20-203">ID de lien</span><span class="sxs-lookup"><span data-stu-id="10b20-203">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="10b20-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="10b20-204">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="10b20-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="10b20-205">System-Only</span></span>            | <span data-ttu-id="10b20-206">Faux</span><span class="sxs-lookup"><span data-stu-id="10b20-206">False</span></span>                                                                 |
| <span data-ttu-id="10b20-207">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="10b20-207">Is-Single-Valued</span></span>       | <span data-ttu-id="10b20-208">Faux</span><span class="sxs-lookup"><span data-stu-id="10b20-208">False</span></span>                                                                 |
| <span data-ttu-id="10b20-209">Est indexé</span><span class="sxs-lookup"><span data-stu-id="10b20-209">Is Indexed</span></span>             | <span data-ttu-id="10b20-210">Faux</span><span class="sxs-lookup"><span data-stu-id="10b20-210">False</span></span>                                                                 |
| <span data-ttu-id="10b20-211">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="10b20-211">In Global Catalog</span></span>      | <span data-ttu-id="10b20-212">Faux</span><span class="sxs-lookup"><span data-stu-id="10b20-212">False</span></span>                                                                 |
| <span data-ttu-id="10b20-213">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="10b20-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="10b20-214">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="10b20-214">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="10b20-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="10b20-215">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="10b20-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="10b20-216">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="10b20-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="10b20-217">Search-Flags</span></span>           | <span data-ttu-id="10b20-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="10b20-218">0x00000000</span></span>                                                            |
| <span data-ttu-id="10b20-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="10b20-219">System-Flags</span></span>           | <span data-ttu-id="10b20-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="10b20-220">0x00000010</span></span>                                                            |
| <span data-ttu-id="10b20-221">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="10b20-221">Classes used in</span></span>        | [<span data-ttu-id="10b20-222">**Gestion des licences-site-paramètres**</span><span class="sxs-lookup"><span data-stu-id="10b20-222">**Licensing-Site-Settings**</span></span>](c-licensingsitesettings.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="10b20-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="10b20-223">Windows Server 2008</span></span>



| <span data-ttu-id="10b20-224">Entrée</span><span class="sxs-lookup"><span data-stu-id="10b20-224">Entry</span></span> | <span data-ttu-id="10b20-225">Valeur</span><span class="sxs-lookup"><span data-stu-id="10b20-225">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="10b20-226">ID de lien</span><span class="sxs-lookup"><span data-stu-id="10b20-226">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="10b20-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="10b20-227">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="10b20-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="10b20-228">System-Only</span></span>            | <span data-ttu-id="10b20-229">Faux</span><span class="sxs-lookup"><span data-stu-id="10b20-229">False</span></span>                                                                 |
| <span data-ttu-id="10b20-230">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="10b20-230">Is-Single-Valued</span></span>       | <span data-ttu-id="10b20-231">Faux</span><span class="sxs-lookup"><span data-stu-id="10b20-231">False</span></span>                                                                 |
| <span data-ttu-id="10b20-232">Est indexé</span><span class="sxs-lookup"><span data-stu-id="10b20-232">Is Indexed</span></span>             | <span data-ttu-id="10b20-233">Faux</span><span class="sxs-lookup"><span data-stu-id="10b20-233">False</span></span>                                                                 |
| <span data-ttu-id="10b20-234">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="10b20-234">In Global Catalog</span></span>      | <span data-ttu-id="10b20-235">Faux</span><span class="sxs-lookup"><span data-stu-id="10b20-235">False</span></span>                                                                 |
| <span data-ttu-id="10b20-236">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="10b20-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="10b20-237">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="10b20-237">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="10b20-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="10b20-238">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="10b20-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="10b20-239">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="10b20-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="10b20-240">Search-Flags</span></span>           | <span data-ttu-id="10b20-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="10b20-241">0x00000000</span></span>                                                            |
| <span data-ttu-id="10b20-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="10b20-242">System-Flags</span></span>           | <span data-ttu-id="10b20-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="10b20-243">0x00000010</span></span>                                                            |
| <span data-ttu-id="10b20-244">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="10b20-244">Classes used in</span></span>        | [<span data-ttu-id="10b20-245">**Gestion des licences-site-paramètres**</span><span class="sxs-lookup"><span data-stu-id="10b20-245">**Licensing-Site-Settings**</span></span>](c-licensingsitesettings.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="10b20-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="10b20-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="10b20-247">Entrée</span><span class="sxs-lookup"><span data-stu-id="10b20-247">Entry</span></span> | <span data-ttu-id="10b20-248">Valeur</span><span class="sxs-lookup"><span data-stu-id="10b20-248">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="10b20-249">ID de lien</span><span class="sxs-lookup"><span data-stu-id="10b20-249">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="10b20-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="10b20-250">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="10b20-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="10b20-251">System-Only</span></span>            | <span data-ttu-id="10b20-252">Faux</span><span class="sxs-lookup"><span data-stu-id="10b20-252">False</span></span>                                                                 |
| <span data-ttu-id="10b20-253">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="10b20-253">Is-Single-Valued</span></span>       | <span data-ttu-id="10b20-254">Faux</span><span class="sxs-lookup"><span data-stu-id="10b20-254">False</span></span>                                                                 |
| <span data-ttu-id="10b20-255">Est indexé</span><span class="sxs-lookup"><span data-stu-id="10b20-255">Is Indexed</span></span>             | <span data-ttu-id="10b20-256">Faux</span><span class="sxs-lookup"><span data-stu-id="10b20-256">False</span></span>                                                                 |
| <span data-ttu-id="10b20-257">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="10b20-257">In Global Catalog</span></span>      | <span data-ttu-id="10b20-258">Faux</span><span class="sxs-lookup"><span data-stu-id="10b20-258">False</span></span>                                                                 |
| <span data-ttu-id="10b20-259">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="10b20-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="10b20-260">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="10b20-260">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="10b20-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="10b20-261">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="10b20-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="10b20-262">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="10b20-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="10b20-263">Search-Flags</span></span>           | <span data-ttu-id="10b20-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="10b20-264">0x00000000</span></span>                                                            |
| <span data-ttu-id="10b20-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="10b20-265">System-Flags</span></span>           | <span data-ttu-id="10b20-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="10b20-266">0x00000010</span></span>                                                            |
| <span data-ttu-id="10b20-267">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="10b20-267">Classes used in</span></span>        | [<span data-ttu-id="10b20-268">**Gestion des licences-site-paramètres**</span><span class="sxs-lookup"><span data-stu-id="10b20-268">**Licensing-Site-Settings**</span></span>](c-licensingsitesettings.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="10b20-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="10b20-269">Windows Server 2012</span></span>



| <span data-ttu-id="10b20-270">Entrée</span><span class="sxs-lookup"><span data-stu-id="10b20-270">Entry</span></span> | <span data-ttu-id="10b20-271">Valeur</span><span class="sxs-lookup"><span data-stu-id="10b20-271">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="10b20-272">ID de lien</span><span class="sxs-lookup"><span data-stu-id="10b20-272">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="10b20-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="10b20-273">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="10b20-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="10b20-274">System-Only</span></span>            | <span data-ttu-id="10b20-275">Faux</span><span class="sxs-lookup"><span data-stu-id="10b20-275">False</span></span>                                                                 |
| <span data-ttu-id="10b20-276">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="10b20-276">Is-Single-Valued</span></span>       | <span data-ttu-id="10b20-277">Faux</span><span class="sxs-lookup"><span data-stu-id="10b20-277">False</span></span>                                                                 |
| <span data-ttu-id="10b20-278">Est indexé</span><span class="sxs-lookup"><span data-stu-id="10b20-278">Is Indexed</span></span>             | <span data-ttu-id="10b20-279">Faux</span><span class="sxs-lookup"><span data-stu-id="10b20-279">False</span></span>                                                                 |
| <span data-ttu-id="10b20-280">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="10b20-280">In Global Catalog</span></span>      | <span data-ttu-id="10b20-281">Faux</span><span class="sxs-lookup"><span data-stu-id="10b20-281">False</span></span>                                                                 |
| <span data-ttu-id="10b20-282">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="10b20-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="10b20-283">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="10b20-283">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="10b20-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="10b20-284">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="10b20-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="10b20-285">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="10b20-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="10b20-286">Search-Flags</span></span>           | <span data-ttu-id="10b20-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="10b20-287">0x00000000</span></span>                                                            |
| <span data-ttu-id="10b20-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="10b20-288">System-Flags</span></span>           | <span data-ttu-id="10b20-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="10b20-289">0x00000010</span></span>                                                            |
| <span data-ttu-id="10b20-290">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="10b20-290">Classes used in</span></span>        | [<span data-ttu-id="10b20-291">**Gestion des licences-site-paramètres**</span><span class="sxs-lookup"><span data-stu-id="10b20-291">**Licensing-Site-Settings**</span></span>](c-licensingsitesettings.md)<br/> |



 

 





