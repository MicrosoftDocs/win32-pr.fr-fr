---
title: MS-IIS-FTP-attribut racine
description: Cet attribut détermine le partage de serveur de fichiers. Il est utilisé conjointement avec MS-IIS-FTP-dir pour déterminer le répertoire de démarrage de l’utilisateur FTP.
ms.assetid: b86dcafb-0b0d-4225-924c-690f739092a8
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory MS-IIS-FTP-root Attribute
- Schéma Active Directory msIIS-FTPRoot Attribute
topic_type:
- apiref
api_name:
- ms-IIS-FTP-Root
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e7c55980b8b08865889f7567fa6bdb4dcf7bde1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104480332"
---
# <a name="ms-iis-ftp-root-attribute"></a><span data-ttu-id="bb0b4-106">MS-IIS-FTP-attribut racine</span><span class="sxs-lookup"><span data-stu-id="bb0b4-106">ms-IIS-FTP-Root attribute</span></span>

<span data-ttu-id="bb0b4-107">Cet attribut détermine le partage de serveur de fichiers.</span><span class="sxs-lookup"><span data-stu-id="bb0b4-107">This attribute determines the file server share.</span></span> <span data-ttu-id="bb0b4-108">Il est utilisé conjointement avec MS-IIS-FTP-dir pour déterminer le répertoire de démarrage de l’utilisateur FTP.</span><span class="sxs-lookup"><span data-stu-id="bb0b4-108">It is used in conjunction with ms-IIS-FTP-Dir to determine the FTP user home directory.</span></span>



| <span data-ttu-id="bb0b4-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="bb0b4-109">Entry</span></span> | <span data-ttu-id="bb0b4-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="bb0b4-110">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb0b4-111">CN</span><span class="sxs-lookup"><span data-stu-id="bb0b4-111">CN</span></span>                | <span data-ttu-id="bb0b4-112">MS-IIS-FTP-root</span><span class="sxs-lookup"><span data-stu-id="bb0b4-112">ms-IIS-FTP-Root</span></span>                                                                                                                 |
| <span data-ttu-id="bb0b4-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="bb0b4-113">Ldap-Display-Name</span></span> | <span data-ttu-id="bb0b4-114">msIIS-FTPRoot</span><span class="sxs-lookup"><span data-stu-id="bb0b4-114">msIIS-FTPRoot</span></span>                                                                                                                   |
| <span data-ttu-id="bb0b4-115">Taille</span><span class="sxs-lookup"><span data-stu-id="bb0b4-115">Size</span></span>              | <span data-ttu-id="bb0b4-116">30-50 caractères (15-25 caractères Unicode pour chaque propriété)</span><span class="sxs-lookup"><span data-stu-id="bb0b4-116">30-50 characters (15-25 Unicode characters for each property)</span></span>                                                                   |
| <span data-ttu-id="bb0b4-117">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="bb0b4-117">Update Privilege</span></span>  | <span data-ttu-id="bb0b4-118">Administrateur de domaine & système local</span><span class="sxs-lookup"><span data-stu-id="bb0b4-118">Domain administrator & local system</span></span>                                                                                             |
| <span data-ttu-id="bb0b4-119">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="bb0b4-119">Update Frequency</span></span>  | <span data-ttu-id="bb0b4-120">Cette propriété est définie lorsque l’administrateur crée le site Web et définit l’isolement FTP.</span><span class="sxs-lookup"><span data-stu-id="bb0b4-120">This property is set when the administrator creates the website and sets FTP isolation.</span></span> <span data-ttu-id="bb0b4-121">Cela va rarement changer après cela.</span><span class="sxs-lookup"><span data-stu-id="bb0b4-121">It's rarely going to change after that.</span></span> |
| <span data-ttu-id="bb0b4-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="bb0b4-122">Attribute-Id</span></span>      | <span data-ttu-id="bb0b4-123">1.2.840.113556.1.4.1785</span><span class="sxs-lookup"><span data-stu-id="bb0b4-123">1.2.840.113556.1.4.1785</span></span>                                                                                                         |
| <span data-ttu-id="bb0b4-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="bb0b4-124">System-Id-Guid</span></span>    | <span data-ttu-id="bb0b4-125">2a7827a4-1483-49a5-9d84-52e3812156b4</span><span class="sxs-lookup"><span data-stu-id="bb0b4-125">2a7827a4-1483-49a5-9d84-52e3812156b4</span></span>                                                                                            |
| <span data-ttu-id="bb0b4-126">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bb0b4-126">Syntax</span></span>            | [<span data-ttu-id="bb0b4-127">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="bb0b4-127">**String(Unicode)**</span></span>](s-string-unicode.md)                                                                                     |



## <a name="implementations"></a><span data-ttu-id="bb0b4-128">Implémentations</span><span class="sxs-lookup"><span data-stu-id="bb0b4-128">Implementations</span></span>

-   [<span data-ttu-id="bb0b4-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="bb0b4-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="bb0b4-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="bb0b4-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="bb0b4-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="bb0b4-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="bb0b4-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="bb0b4-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="bb0b4-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="bb0b4-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="bb0b4-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bb0b4-134">Windows Server 2003</span></span>



| <span data-ttu-id="bb0b4-135">Entrée</span><span class="sxs-lookup"><span data-stu-id="bb0b4-135">Entry</span></span> | <span data-ttu-id="bb0b4-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="bb0b4-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="bb0b4-137">ID de lien</span><span class="sxs-lookup"><span data-stu-id="bb0b4-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="bb0b4-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bb0b4-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="bb0b4-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="bb0b4-139">System-Only</span></span>            | <span data-ttu-id="bb0b4-140">Faux</span><span class="sxs-lookup"><span data-stu-id="bb0b4-140">False</span></span>                             |
| <span data-ttu-id="bb0b4-141">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="bb0b4-141">Is-Single-Valued</span></span>       | <span data-ttu-id="bb0b4-142">Vrai</span><span class="sxs-lookup"><span data-stu-id="bb0b4-142">True</span></span>                              |
| <span data-ttu-id="bb0b4-143">Est indexé</span><span class="sxs-lookup"><span data-stu-id="bb0b4-143">Is Indexed</span></span>             | <span data-ttu-id="bb0b4-144">Faux</span><span class="sxs-lookup"><span data-stu-id="bb0b4-144">False</span></span>                             |
| <span data-ttu-id="bb0b4-145">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="bb0b4-145">In Global Catalog</span></span>      | <span data-ttu-id="bb0b4-146">Faux</span><span class="sxs-lookup"><span data-stu-id="bb0b4-146">False</span></span>                             |
| <span data-ttu-id="bb0b4-147">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="bb0b4-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="bb0b4-148">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="bb0b4-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="bb0b4-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bb0b4-149">Range-Lower</span></span>            | <span data-ttu-id="bb0b4-150">1</span><span class="sxs-lookup"><span data-stu-id="bb0b4-150">1</span></span>                                 |
| <span data-ttu-id="bb0b4-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bb0b4-151">Range-Upper</span></span>            | <span data-ttu-id="bb0b4-152">256</span><span class="sxs-lookup"><span data-stu-id="bb0b4-152">256</span></span>                               |
| <span data-ttu-id="bb0b4-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bb0b4-153">Search-Flags</span></span>           | <span data-ttu-id="bb0b4-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bb0b4-154">0x00000000</span></span>                        |
| <span data-ttu-id="bb0b4-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bb0b4-155">System-Flags</span></span>           | <span data-ttu-id="bb0b4-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bb0b4-156">0x00000010</span></span>                        |
| <span data-ttu-id="bb0b4-157">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="bb0b4-157">Classes used in</span></span>        | [<span data-ttu-id="bb0b4-158">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="bb0b4-158">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="bb0b4-159">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="bb0b4-159">Windows Server 2003 R2</span></span>



| <span data-ttu-id="bb0b4-160">Entrée</span><span class="sxs-lookup"><span data-stu-id="bb0b4-160">Entry</span></span> | <span data-ttu-id="bb0b4-161">Valeur</span><span class="sxs-lookup"><span data-stu-id="bb0b4-161">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="bb0b4-162">ID de lien</span><span class="sxs-lookup"><span data-stu-id="bb0b4-162">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="bb0b4-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bb0b4-163">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="bb0b4-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="bb0b4-164">System-Only</span></span>            | <span data-ttu-id="bb0b4-165">Faux</span><span class="sxs-lookup"><span data-stu-id="bb0b4-165">False</span></span>                             |
| <span data-ttu-id="bb0b4-166">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="bb0b4-166">Is-Single-Valued</span></span>       | <span data-ttu-id="bb0b4-167">Vrai</span><span class="sxs-lookup"><span data-stu-id="bb0b4-167">True</span></span>                              |
| <span data-ttu-id="bb0b4-168">Est indexé</span><span class="sxs-lookup"><span data-stu-id="bb0b4-168">Is Indexed</span></span>             | <span data-ttu-id="bb0b4-169">Faux</span><span class="sxs-lookup"><span data-stu-id="bb0b4-169">False</span></span>                             |
| <span data-ttu-id="bb0b4-170">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="bb0b4-170">In Global Catalog</span></span>      | <span data-ttu-id="bb0b4-171">Faux</span><span class="sxs-lookup"><span data-stu-id="bb0b4-171">False</span></span>                             |
| <span data-ttu-id="bb0b4-172">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="bb0b4-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="bb0b4-173">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="bb0b4-173">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="bb0b4-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bb0b4-174">Range-Lower</span></span>            | <span data-ttu-id="bb0b4-175">1</span><span class="sxs-lookup"><span data-stu-id="bb0b4-175">1</span></span>                                 |
| <span data-ttu-id="bb0b4-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bb0b4-176">Range-Upper</span></span>            | <span data-ttu-id="bb0b4-177">256</span><span class="sxs-lookup"><span data-stu-id="bb0b4-177">256</span></span>                               |
| <span data-ttu-id="bb0b4-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bb0b4-178">Search-Flags</span></span>           | <span data-ttu-id="bb0b4-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bb0b4-179">0x00000000</span></span>                        |
| <span data-ttu-id="bb0b4-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bb0b4-180">System-Flags</span></span>           | <span data-ttu-id="bb0b4-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bb0b4-181">0x00000010</span></span>                        |
| <span data-ttu-id="bb0b4-182">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="bb0b4-182">Classes used in</span></span>        | [<span data-ttu-id="bb0b4-183">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="bb0b4-183">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="bb0b4-184">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bb0b4-184">Windows Server 2008</span></span>



| <span data-ttu-id="bb0b4-185">Entrée</span><span class="sxs-lookup"><span data-stu-id="bb0b4-185">Entry</span></span> | <span data-ttu-id="bb0b4-186">Valeur</span><span class="sxs-lookup"><span data-stu-id="bb0b4-186">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="bb0b4-187">ID de lien</span><span class="sxs-lookup"><span data-stu-id="bb0b4-187">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="bb0b4-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bb0b4-188">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="bb0b4-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="bb0b4-189">System-Only</span></span>            | <span data-ttu-id="bb0b4-190">Faux</span><span class="sxs-lookup"><span data-stu-id="bb0b4-190">False</span></span>                             |
| <span data-ttu-id="bb0b4-191">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="bb0b4-191">Is-Single-Valued</span></span>       | <span data-ttu-id="bb0b4-192">Vrai</span><span class="sxs-lookup"><span data-stu-id="bb0b4-192">True</span></span>                              |
| <span data-ttu-id="bb0b4-193">Est indexé</span><span class="sxs-lookup"><span data-stu-id="bb0b4-193">Is Indexed</span></span>             | <span data-ttu-id="bb0b4-194">Faux</span><span class="sxs-lookup"><span data-stu-id="bb0b4-194">False</span></span>                             |
| <span data-ttu-id="bb0b4-195">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="bb0b4-195">In Global Catalog</span></span>      | <span data-ttu-id="bb0b4-196">Faux</span><span class="sxs-lookup"><span data-stu-id="bb0b4-196">False</span></span>                             |
| <span data-ttu-id="bb0b4-197">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="bb0b4-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="bb0b4-198">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="bb0b4-198">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="bb0b4-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bb0b4-199">Range-Lower</span></span>            | <span data-ttu-id="bb0b4-200">1</span><span class="sxs-lookup"><span data-stu-id="bb0b4-200">1</span></span>                                 |
| <span data-ttu-id="bb0b4-201">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bb0b4-201">Range-Upper</span></span>            | <span data-ttu-id="bb0b4-202">256</span><span class="sxs-lookup"><span data-stu-id="bb0b4-202">256</span></span>                               |
| <span data-ttu-id="bb0b4-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bb0b4-203">Search-Flags</span></span>           | <span data-ttu-id="bb0b4-204">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bb0b4-204">0x00000000</span></span>                        |
| <span data-ttu-id="bb0b4-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bb0b4-205">System-Flags</span></span>           | <span data-ttu-id="bb0b4-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bb0b4-206">0x00000010</span></span>                        |
| <span data-ttu-id="bb0b4-207">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="bb0b4-207">Classes used in</span></span>        | [<span data-ttu-id="bb0b4-208">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="bb0b4-208">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="bb0b4-209">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bb0b4-209">Windows Server 2008 R2</span></span>



| <span data-ttu-id="bb0b4-210">Entrée</span><span class="sxs-lookup"><span data-stu-id="bb0b4-210">Entry</span></span> | <span data-ttu-id="bb0b4-211">Valeur</span><span class="sxs-lookup"><span data-stu-id="bb0b4-211">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="bb0b4-212">ID de lien</span><span class="sxs-lookup"><span data-stu-id="bb0b4-212">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="bb0b4-213">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bb0b4-213">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="bb0b4-214">System-Only</span><span class="sxs-lookup"><span data-stu-id="bb0b4-214">System-Only</span></span>            | <span data-ttu-id="bb0b4-215">Faux</span><span class="sxs-lookup"><span data-stu-id="bb0b4-215">False</span></span>                             |
| <span data-ttu-id="bb0b4-216">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="bb0b4-216">Is-Single-Valued</span></span>       | <span data-ttu-id="bb0b4-217">Vrai</span><span class="sxs-lookup"><span data-stu-id="bb0b4-217">True</span></span>                              |
| <span data-ttu-id="bb0b4-218">Est indexé</span><span class="sxs-lookup"><span data-stu-id="bb0b4-218">Is Indexed</span></span>             | <span data-ttu-id="bb0b4-219">Faux</span><span class="sxs-lookup"><span data-stu-id="bb0b4-219">False</span></span>                             |
| <span data-ttu-id="bb0b4-220">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="bb0b4-220">In Global Catalog</span></span>      | <span data-ttu-id="bb0b4-221">Faux</span><span class="sxs-lookup"><span data-stu-id="bb0b4-221">False</span></span>                             |
| <span data-ttu-id="bb0b4-222">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="bb0b4-222">NT-Security-Descriptor</span></span> | <span data-ttu-id="bb0b4-223">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="bb0b4-223">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="bb0b4-224">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bb0b4-224">Range-Lower</span></span>            | <span data-ttu-id="bb0b4-225">1</span><span class="sxs-lookup"><span data-stu-id="bb0b4-225">1</span></span>                                 |
| <span data-ttu-id="bb0b4-226">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bb0b4-226">Range-Upper</span></span>            | <span data-ttu-id="bb0b4-227">256</span><span class="sxs-lookup"><span data-stu-id="bb0b4-227">256</span></span>                               |
| <span data-ttu-id="bb0b4-228">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bb0b4-228">Search-Flags</span></span>           | <span data-ttu-id="bb0b4-229">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bb0b4-229">0x00000000</span></span>                        |
| <span data-ttu-id="bb0b4-230">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bb0b4-230">System-Flags</span></span>           | <span data-ttu-id="bb0b4-231">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bb0b4-231">0x00000010</span></span>                        |
| <span data-ttu-id="bb0b4-232">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="bb0b4-232">Classes used in</span></span>        | [<span data-ttu-id="bb0b4-233">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="bb0b4-233">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="bb0b4-234">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bb0b4-234">Windows Server 2012</span></span>



| <span data-ttu-id="bb0b4-235">Entrée</span><span class="sxs-lookup"><span data-stu-id="bb0b4-235">Entry</span></span> | <span data-ttu-id="bb0b4-236">Valeur</span><span class="sxs-lookup"><span data-stu-id="bb0b4-236">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="bb0b4-237">ID de lien</span><span class="sxs-lookup"><span data-stu-id="bb0b4-237">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="bb0b4-238">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bb0b4-238">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="bb0b4-239">System-Only</span><span class="sxs-lookup"><span data-stu-id="bb0b4-239">System-Only</span></span>            | <span data-ttu-id="bb0b4-240">Faux</span><span class="sxs-lookup"><span data-stu-id="bb0b4-240">False</span></span>                             |
| <span data-ttu-id="bb0b4-241">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="bb0b4-241">Is-Single-Valued</span></span>       | <span data-ttu-id="bb0b4-242">Vrai</span><span class="sxs-lookup"><span data-stu-id="bb0b4-242">True</span></span>                              |
| <span data-ttu-id="bb0b4-243">Est indexé</span><span class="sxs-lookup"><span data-stu-id="bb0b4-243">Is Indexed</span></span>             | <span data-ttu-id="bb0b4-244">Faux</span><span class="sxs-lookup"><span data-stu-id="bb0b4-244">False</span></span>                             |
| <span data-ttu-id="bb0b4-245">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="bb0b4-245">In Global Catalog</span></span>      | <span data-ttu-id="bb0b4-246">Faux</span><span class="sxs-lookup"><span data-stu-id="bb0b4-246">False</span></span>                             |
| <span data-ttu-id="bb0b4-247">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="bb0b4-247">NT-Security-Descriptor</span></span> | <span data-ttu-id="bb0b4-248">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="bb0b4-248">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="bb0b4-249">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bb0b4-249">Range-Lower</span></span>            | <span data-ttu-id="bb0b4-250">1</span><span class="sxs-lookup"><span data-stu-id="bb0b4-250">1</span></span>                                 |
| <span data-ttu-id="bb0b4-251">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bb0b4-251">Range-Upper</span></span>            | <span data-ttu-id="bb0b4-252">256</span><span class="sxs-lookup"><span data-stu-id="bb0b4-252">256</span></span>                               |
| <span data-ttu-id="bb0b4-253">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bb0b4-253">Search-Flags</span></span>           | <span data-ttu-id="bb0b4-254">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bb0b4-254">0x00000000</span></span>                        |
| <span data-ttu-id="bb0b4-255">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bb0b4-255">System-Flags</span></span>           | <span data-ttu-id="bb0b4-256">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bb0b4-256">0x00000010</span></span>                        |
| <span data-ttu-id="bb0b4-257">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="bb0b4-257">Classes used in</span></span>        | [<span data-ttu-id="bb0b4-258">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="bb0b4-258">**User**</span></span>](c-user.md)<br/> |



 

 





