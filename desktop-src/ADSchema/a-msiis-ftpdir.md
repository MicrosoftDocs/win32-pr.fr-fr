---
title: attribut MS-IIS-FTP-dir
description: Cet attribut détermine le répertoire de démarrage de l’utilisateur par rapport au partage de serveur de fichiers. Il est utilisé conjointement avec MS-IIS-FTP-root pour déterminer le répertoire de démarrage de l’utilisateur FTP.
ms.assetid: 99b22b79-1d42-440d-b92b-33bac3e811cb
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut MS-IIS-FTP-dir
- Schéma AD d’attribut msIIS-FTPDir
topic_type:
- apiref
api_name:
- ms-IIS-FTP-Dir
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3067476e7dc275dbe14471d6c3c98fa5445a9dfe
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104519785"
---
# <a name="ms-iis-ftp-dir-attribute"></a><span data-ttu-id="006e6-106">attribut MS-IIS-FTP-dir</span><span class="sxs-lookup"><span data-stu-id="006e6-106">ms-IIS-FTP-Dir attribute</span></span>

<span data-ttu-id="006e6-107">Cet attribut détermine le répertoire de démarrage de l’utilisateur par rapport au partage de serveur de fichiers.</span><span class="sxs-lookup"><span data-stu-id="006e6-107">This attribute determines the user home directory relative to the file server share.</span></span> <span data-ttu-id="006e6-108">Il est utilisé conjointement avec MS-IIS-FTP-root pour déterminer le répertoire de démarrage de l’utilisateur FTP.</span><span class="sxs-lookup"><span data-stu-id="006e6-108">It is used in conjunction with ms-IIS-FTP-Root to determine the FTP user home directory.</span></span>



| <span data-ttu-id="006e6-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="006e6-109">Entry</span></span> | <span data-ttu-id="006e6-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="006e6-110">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="006e6-111">CN</span><span class="sxs-lookup"><span data-stu-id="006e6-111">CN</span></span>                | <span data-ttu-id="006e6-112">MS-IIS-FTP-dir</span><span class="sxs-lookup"><span data-stu-id="006e6-112">ms-IIS-FTP-Dir</span></span>                                                                                                                  |
| <span data-ttu-id="006e6-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="006e6-113">Ldap-Display-Name</span></span> | <span data-ttu-id="006e6-114">msIIS-FTPDir</span><span class="sxs-lookup"><span data-stu-id="006e6-114">msIIS-FTPDir</span></span>                                                                                                                    |
| <span data-ttu-id="006e6-115">Taille</span><span class="sxs-lookup"><span data-stu-id="006e6-115">Size</span></span>              | <span data-ttu-id="006e6-116">30-50 caractères (15-25 caractères Unicode pour chaque propriété)</span><span class="sxs-lookup"><span data-stu-id="006e6-116">30-50 characters (15-25 Unicode characters for each property)</span></span>                                                                   |
| <span data-ttu-id="006e6-117">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="006e6-117">Update Privilege</span></span>  | <span data-ttu-id="006e6-118">Administrateur de domaine & système local</span><span class="sxs-lookup"><span data-stu-id="006e6-118">Domain administrator & local system</span></span>                                                                                             |
| <span data-ttu-id="006e6-119">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="006e6-119">Update Frequency</span></span>  | <span data-ttu-id="006e6-120">Cette propriété est définie lorsque l’administrateur crée le site Web et définit l’isolement FTP.</span><span class="sxs-lookup"><span data-stu-id="006e6-120">This property is set when the administrator creates the website and sets FTP isolation.</span></span> <span data-ttu-id="006e6-121">Cela va rarement changer après cela.</span><span class="sxs-lookup"><span data-stu-id="006e6-121">It's rarely going to change after that.</span></span> |
| <span data-ttu-id="006e6-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="006e6-122">Attribute-Id</span></span>      | <span data-ttu-id="006e6-123">1.2.840.113556.1.4.1786</span><span class="sxs-lookup"><span data-stu-id="006e6-123">1.2.840.113556.1.4.1786</span></span>                                                                                                         |
| <span data-ttu-id="006e6-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="006e6-124">System-Id-Guid</span></span>    | <span data-ttu-id="006e6-125">8a5c99e9-2230-46eb-b8e8-e59d712eb9ee</span><span class="sxs-lookup"><span data-stu-id="006e6-125">8a5c99e9-2230-46eb-b8e8-e59d712eb9ee</span></span>                                                                                            |
| <span data-ttu-id="006e6-126">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="006e6-126">Syntax</span></span>            | [<span data-ttu-id="006e6-127">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="006e6-127">**String(Unicode)**</span></span>](s-string-unicode.md)                                                                                     |



## <a name="implementations"></a><span data-ttu-id="006e6-128">Implémentations</span><span class="sxs-lookup"><span data-stu-id="006e6-128">Implementations</span></span>

-   [<span data-ttu-id="006e6-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="006e6-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="006e6-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="006e6-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="006e6-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="006e6-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="006e6-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="006e6-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="006e6-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="006e6-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="006e6-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="006e6-134">Windows Server 2003</span></span>



| <span data-ttu-id="006e6-135">Entrée</span><span class="sxs-lookup"><span data-stu-id="006e6-135">Entry</span></span> | <span data-ttu-id="006e6-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="006e6-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="006e6-137">ID de lien</span><span class="sxs-lookup"><span data-stu-id="006e6-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="006e6-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="006e6-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="006e6-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="006e6-139">System-Only</span></span>            | <span data-ttu-id="006e6-140">Faux</span><span class="sxs-lookup"><span data-stu-id="006e6-140">False</span></span>                             |
| <span data-ttu-id="006e6-141">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="006e6-141">Is-Single-Valued</span></span>       | <span data-ttu-id="006e6-142">Vrai</span><span class="sxs-lookup"><span data-stu-id="006e6-142">True</span></span>                              |
| <span data-ttu-id="006e6-143">Est indexé</span><span class="sxs-lookup"><span data-stu-id="006e6-143">Is Indexed</span></span>             | <span data-ttu-id="006e6-144">Faux</span><span class="sxs-lookup"><span data-stu-id="006e6-144">False</span></span>                             |
| <span data-ttu-id="006e6-145">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="006e6-145">In Global Catalog</span></span>      | <span data-ttu-id="006e6-146">Faux</span><span class="sxs-lookup"><span data-stu-id="006e6-146">False</span></span>                             |
| <span data-ttu-id="006e6-147">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="006e6-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="006e6-148">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="006e6-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="006e6-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="006e6-149">Range-Lower</span></span>            | <span data-ttu-id="006e6-150">1</span><span class="sxs-lookup"><span data-stu-id="006e6-150">1</span></span>                                 |
| <span data-ttu-id="006e6-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="006e6-151">Range-Upper</span></span>            | <span data-ttu-id="006e6-152">256</span><span class="sxs-lookup"><span data-stu-id="006e6-152">256</span></span>                               |
| <span data-ttu-id="006e6-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="006e6-153">Search-Flags</span></span>           | <span data-ttu-id="006e6-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="006e6-154">0x00000000</span></span>                        |
| <span data-ttu-id="006e6-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="006e6-155">System-Flags</span></span>           | <span data-ttu-id="006e6-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="006e6-156">0x00000010</span></span>                        |
| <span data-ttu-id="006e6-157">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="006e6-157">Classes used in</span></span>        | [<span data-ttu-id="006e6-158">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="006e6-158">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="006e6-159">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="006e6-159">Windows Server 2003 R2</span></span>



| <span data-ttu-id="006e6-160">Entrée</span><span class="sxs-lookup"><span data-stu-id="006e6-160">Entry</span></span> | <span data-ttu-id="006e6-161">Valeur</span><span class="sxs-lookup"><span data-stu-id="006e6-161">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="006e6-162">ID de lien</span><span class="sxs-lookup"><span data-stu-id="006e6-162">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="006e6-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="006e6-163">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="006e6-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="006e6-164">System-Only</span></span>            | <span data-ttu-id="006e6-165">Faux</span><span class="sxs-lookup"><span data-stu-id="006e6-165">False</span></span>                             |
| <span data-ttu-id="006e6-166">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="006e6-166">Is-Single-Valued</span></span>       | <span data-ttu-id="006e6-167">Vrai</span><span class="sxs-lookup"><span data-stu-id="006e6-167">True</span></span>                              |
| <span data-ttu-id="006e6-168">Est indexé</span><span class="sxs-lookup"><span data-stu-id="006e6-168">Is Indexed</span></span>             | <span data-ttu-id="006e6-169">Faux</span><span class="sxs-lookup"><span data-stu-id="006e6-169">False</span></span>                             |
| <span data-ttu-id="006e6-170">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="006e6-170">In Global Catalog</span></span>      | <span data-ttu-id="006e6-171">Faux</span><span class="sxs-lookup"><span data-stu-id="006e6-171">False</span></span>                             |
| <span data-ttu-id="006e6-172">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="006e6-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="006e6-173">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="006e6-173">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="006e6-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="006e6-174">Range-Lower</span></span>            | <span data-ttu-id="006e6-175">1</span><span class="sxs-lookup"><span data-stu-id="006e6-175">1</span></span>                                 |
| <span data-ttu-id="006e6-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="006e6-176">Range-Upper</span></span>            | <span data-ttu-id="006e6-177">256</span><span class="sxs-lookup"><span data-stu-id="006e6-177">256</span></span>                               |
| <span data-ttu-id="006e6-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="006e6-178">Search-Flags</span></span>           | <span data-ttu-id="006e6-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="006e6-179">0x00000000</span></span>                        |
| <span data-ttu-id="006e6-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="006e6-180">System-Flags</span></span>           | <span data-ttu-id="006e6-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="006e6-181">0x00000010</span></span>                        |
| <span data-ttu-id="006e6-182">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="006e6-182">Classes used in</span></span>        | [<span data-ttu-id="006e6-183">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="006e6-183">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="006e6-184">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="006e6-184">Windows Server 2008</span></span>



| <span data-ttu-id="006e6-185">Entrée</span><span class="sxs-lookup"><span data-stu-id="006e6-185">Entry</span></span> | <span data-ttu-id="006e6-186">Valeur</span><span class="sxs-lookup"><span data-stu-id="006e6-186">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="006e6-187">ID de lien</span><span class="sxs-lookup"><span data-stu-id="006e6-187">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="006e6-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="006e6-188">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="006e6-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="006e6-189">System-Only</span></span>            | <span data-ttu-id="006e6-190">Faux</span><span class="sxs-lookup"><span data-stu-id="006e6-190">False</span></span>                             |
| <span data-ttu-id="006e6-191">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="006e6-191">Is-Single-Valued</span></span>       | <span data-ttu-id="006e6-192">Vrai</span><span class="sxs-lookup"><span data-stu-id="006e6-192">True</span></span>                              |
| <span data-ttu-id="006e6-193">Est indexé</span><span class="sxs-lookup"><span data-stu-id="006e6-193">Is Indexed</span></span>             | <span data-ttu-id="006e6-194">Faux</span><span class="sxs-lookup"><span data-stu-id="006e6-194">False</span></span>                             |
| <span data-ttu-id="006e6-195">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="006e6-195">In Global Catalog</span></span>      | <span data-ttu-id="006e6-196">Faux</span><span class="sxs-lookup"><span data-stu-id="006e6-196">False</span></span>                             |
| <span data-ttu-id="006e6-197">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="006e6-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="006e6-198">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="006e6-198">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="006e6-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="006e6-199">Range-Lower</span></span>            | <span data-ttu-id="006e6-200">1</span><span class="sxs-lookup"><span data-stu-id="006e6-200">1</span></span>                                 |
| <span data-ttu-id="006e6-201">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="006e6-201">Range-Upper</span></span>            | <span data-ttu-id="006e6-202">256</span><span class="sxs-lookup"><span data-stu-id="006e6-202">256</span></span>                               |
| <span data-ttu-id="006e6-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="006e6-203">Search-Flags</span></span>           | <span data-ttu-id="006e6-204">0x00000000</span><span class="sxs-lookup"><span data-stu-id="006e6-204">0x00000000</span></span>                        |
| <span data-ttu-id="006e6-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="006e6-205">System-Flags</span></span>           | <span data-ttu-id="006e6-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="006e6-206">0x00000010</span></span>                        |
| <span data-ttu-id="006e6-207">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="006e6-207">Classes used in</span></span>        | [<span data-ttu-id="006e6-208">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="006e6-208">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="006e6-209">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="006e6-209">Windows Server 2008 R2</span></span>



| <span data-ttu-id="006e6-210">Entrée</span><span class="sxs-lookup"><span data-stu-id="006e6-210">Entry</span></span> | <span data-ttu-id="006e6-211">Valeur</span><span class="sxs-lookup"><span data-stu-id="006e6-211">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="006e6-212">ID de lien</span><span class="sxs-lookup"><span data-stu-id="006e6-212">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="006e6-213">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="006e6-213">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="006e6-214">System-Only</span><span class="sxs-lookup"><span data-stu-id="006e6-214">System-Only</span></span>            | <span data-ttu-id="006e6-215">Faux</span><span class="sxs-lookup"><span data-stu-id="006e6-215">False</span></span>                             |
| <span data-ttu-id="006e6-216">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="006e6-216">Is-Single-Valued</span></span>       | <span data-ttu-id="006e6-217">Vrai</span><span class="sxs-lookup"><span data-stu-id="006e6-217">True</span></span>                              |
| <span data-ttu-id="006e6-218">Est indexé</span><span class="sxs-lookup"><span data-stu-id="006e6-218">Is Indexed</span></span>             | <span data-ttu-id="006e6-219">Faux</span><span class="sxs-lookup"><span data-stu-id="006e6-219">False</span></span>                             |
| <span data-ttu-id="006e6-220">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="006e6-220">In Global Catalog</span></span>      | <span data-ttu-id="006e6-221">Faux</span><span class="sxs-lookup"><span data-stu-id="006e6-221">False</span></span>                             |
| <span data-ttu-id="006e6-222">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="006e6-222">NT-Security-Descriptor</span></span> | <span data-ttu-id="006e6-223">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="006e6-223">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="006e6-224">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="006e6-224">Range-Lower</span></span>            | <span data-ttu-id="006e6-225">1</span><span class="sxs-lookup"><span data-stu-id="006e6-225">1</span></span>                                 |
| <span data-ttu-id="006e6-226">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="006e6-226">Range-Upper</span></span>            | <span data-ttu-id="006e6-227">256</span><span class="sxs-lookup"><span data-stu-id="006e6-227">256</span></span>                               |
| <span data-ttu-id="006e6-228">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="006e6-228">Search-Flags</span></span>           | <span data-ttu-id="006e6-229">0x00000000</span><span class="sxs-lookup"><span data-stu-id="006e6-229">0x00000000</span></span>                        |
| <span data-ttu-id="006e6-230">System-Flags</span><span class="sxs-lookup"><span data-stu-id="006e6-230">System-Flags</span></span>           | <span data-ttu-id="006e6-231">0x00000010</span><span class="sxs-lookup"><span data-stu-id="006e6-231">0x00000010</span></span>                        |
| <span data-ttu-id="006e6-232">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="006e6-232">Classes used in</span></span>        | [<span data-ttu-id="006e6-233">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="006e6-233">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="006e6-234">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="006e6-234">Windows Server 2012</span></span>



| <span data-ttu-id="006e6-235">Entrée</span><span class="sxs-lookup"><span data-stu-id="006e6-235">Entry</span></span> | <span data-ttu-id="006e6-236">Valeur</span><span class="sxs-lookup"><span data-stu-id="006e6-236">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="006e6-237">ID de lien</span><span class="sxs-lookup"><span data-stu-id="006e6-237">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="006e6-238">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="006e6-238">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="006e6-239">System-Only</span><span class="sxs-lookup"><span data-stu-id="006e6-239">System-Only</span></span>            | <span data-ttu-id="006e6-240">Faux</span><span class="sxs-lookup"><span data-stu-id="006e6-240">False</span></span>                             |
| <span data-ttu-id="006e6-241">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="006e6-241">Is-Single-Valued</span></span>       | <span data-ttu-id="006e6-242">Vrai</span><span class="sxs-lookup"><span data-stu-id="006e6-242">True</span></span>                              |
| <span data-ttu-id="006e6-243">Est indexé</span><span class="sxs-lookup"><span data-stu-id="006e6-243">Is Indexed</span></span>             | <span data-ttu-id="006e6-244">Faux</span><span class="sxs-lookup"><span data-stu-id="006e6-244">False</span></span>                             |
| <span data-ttu-id="006e6-245">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="006e6-245">In Global Catalog</span></span>      | <span data-ttu-id="006e6-246">Faux</span><span class="sxs-lookup"><span data-stu-id="006e6-246">False</span></span>                             |
| <span data-ttu-id="006e6-247">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="006e6-247">NT-Security-Descriptor</span></span> | <span data-ttu-id="006e6-248">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="006e6-248">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="006e6-249">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="006e6-249">Range-Lower</span></span>            | <span data-ttu-id="006e6-250">1</span><span class="sxs-lookup"><span data-stu-id="006e6-250">1</span></span>                                 |
| <span data-ttu-id="006e6-251">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="006e6-251">Range-Upper</span></span>            | <span data-ttu-id="006e6-252">256</span><span class="sxs-lookup"><span data-stu-id="006e6-252">256</span></span>                               |
| <span data-ttu-id="006e6-253">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="006e6-253">Search-Flags</span></span>           | <span data-ttu-id="006e6-254">0x00000000</span><span class="sxs-lookup"><span data-stu-id="006e6-254">0x00000000</span></span>                        |
| <span data-ttu-id="006e6-255">System-Flags</span><span class="sxs-lookup"><span data-stu-id="006e6-255">System-Flags</span></span>           | <span data-ttu-id="006e6-256">0x00000010</span><span class="sxs-lookup"><span data-stu-id="006e6-256">0x00000010</span></span>                        |
| <span data-ttu-id="006e6-257">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="006e6-257">Classes used in</span></span>        | [<span data-ttu-id="006e6-258">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="006e6-258">**User**</span></span>](c-user.md)<br/> |



 

 





