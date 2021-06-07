---
title: attribut ms-DFS-Link-Path-v2
description: Chemin de lien DFS relatif au partage cible racine DFS (autrement dit, sans les composants nom de l’espace de noms de serveur/domaine et de l’espace de noms DFS). Utilisez des barres obliques (/) à la place des barres obliques inverses ( \) , afin que les recherches LDAP puissent être effectuées sans avoir à utiliser des séquences d’échappement.
ms.assetid: 98fd6e99-0d7e-4ffa-b8ec-d26ca03ffead
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut ms-DFS-Link-Path-v2
- Schéma AD de l’attribut msDFS-LinkPathv2
topic_type:
- apiref
api_name:
- ms-DFS-Link-Path-v2
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4659dbf00c6a53c77a23e98836ea1af4eeb4c38a
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386858"
---
# <a name="ms-dfs-link-path-v2-attribute"></a><span data-ttu-id="ae552-106">attribut ms-DFS-Link-Path-v2</span><span class="sxs-lookup"><span data-stu-id="ae552-106">ms-DFS-Link-Path-v2 attribute</span></span>

<span data-ttu-id="ae552-107">Chemin de lien DFS relatif au partage cible racine DFS (autrement dit, sans les composants nom de l’espace de noms de serveur/domaine et de l’espace de noms DFS).</span><span class="sxs-lookup"><span data-stu-id="ae552-107">DFS link path relative to the DFS root target share (that is, without the server/domain and DFS namespace name components).</span></span> <span data-ttu-id="ae552-108">Utilisez des barres obliques (/) à la place des barres obliques inverses ( \\ ), afin que les recherches LDAP puissent être effectuées sans avoir à utiliser des séquences d’échappement.</span><span class="sxs-lookup"><span data-stu-id="ae552-108">Use forward slashes (/) instead of backslashes (\\), so that LDAP searches can be done without having to use escapes.</span></span>



| <span data-ttu-id="ae552-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="ae552-109">Entry</span></span> | <span data-ttu-id="ae552-110">Value</span><span class="sxs-lookup"><span data-stu-id="ae552-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="ae552-111">CN</span><span class="sxs-lookup"><span data-stu-id="ae552-111">CN</span></span>                | <span data-ttu-id="ae552-112">MS-DFS-Link-Path-v2</span><span class="sxs-lookup"><span data-stu-id="ae552-112">ms-DFS-Link-Path-v2</span></span>                         |
| <span data-ttu-id="ae552-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="ae552-113">Ldap-Display-Name</span></span> | <span data-ttu-id="ae552-114">msDFS-LinkPathv2</span><span class="sxs-lookup"><span data-stu-id="ae552-114">msDFS-LinkPathv2</span></span>                            |
| <span data-ttu-id="ae552-115">Taille</span><span class="sxs-lookup"><span data-stu-id="ae552-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="ae552-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="ae552-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="ae552-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="ae552-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="ae552-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ae552-118">Attribute-Id</span></span>      | <span data-ttu-id="ae552-119">1.2.840.113556.1.4.2039</span><span class="sxs-lookup"><span data-stu-id="ae552-119">1.2.840.113556.1.4.2039</span></span>                     |
| <span data-ttu-id="ae552-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ae552-120">System-Id-Guid</span></span>    | <span data-ttu-id="ae552-121">86b021f6-10ab-40a2-a252-1dc0cc3be6a9</span><span class="sxs-lookup"><span data-stu-id="ae552-121">86b021f6-10ab-40a2-a252-1dc0cc3be6a9</span></span>        |
| <span data-ttu-id="ae552-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ae552-122">Syntax</span></span>            | [<span data-ttu-id="ae552-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="ae552-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="ae552-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="ae552-124">Implementations</span></span>

-   [<span data-ttu-id="ae552-125">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ae552-125">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ae552-126">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ae552-126">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ae552-127">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ae552-127">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="ae552-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ae552-128">Windows Server 2008</span></span>



| <span data-ttu-id="ae552-129">Entrée</span><span class="sxs-lookup"><span data-stu-id="ae552-129">Entry</span></span> | <span data-ttu-id="ae552-130">Value</span><span class="sxs-lookup"><span data-stu-id="ae552-130">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae552-131">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ae552-131">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="ae552-132">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ae552-132">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="ae552-133">System-Only</span><span class="sxs-lookup"><span data-stu-id="ae552-133">System-Only</span></span>            | <span data-ttu-id="ae552-134">False</span><span class="sxs-lookup"><span data-stu-id="ae552-134">False</span></span>                                                                                                                  |
| <span data-ttu-id="ae552-135">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ae552-135">Is-Single-Valued</span></span>       | <span data-ttu-id="ae552-136">True</span><span class="sxs-lookup"><span data-stu-id="ae552-136">True</span></span>                                                                                                                   |
| <span data-ttu-id="ae552-137">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ae552-137">Is Indexed</span></span>             | <span data-ttu-id="ae552-138">False</span><span class="sxs-lookup"><span data-stu-id="ae552-138">False</span></span>                                                                                                                  |
| <span data-ttu-id="ae552-139">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ae552-139">In Global Catalog</span></span>      | <span data-ttu-id="ae552-140">False</span><span class="sxs-lookup"><span data-stu-id="ae552-140">False</span></span>                                                                                                                  |
| <span data-ttu-id="ae552-141">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ae552-141">NT-Security-Descriptor</span></span> | <span data-ttu-id="ae552-142">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ae552-142">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="ae552-143">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ae552-143">Range-Lower</span></span>            | <span data-ttu-id="ae552-144">0</span><span class="sxs-lookup"><span data-stu-id="ae552-144">0</span></span>                                                                                                                      |
| <span data-ttu-id="ae552-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ae552-145">Range-Upper</span></span>            | <span data-ttu-id="ae552-146">32766</span><span class="sxs-lookup"><span data-stu-id="ae552-146">32766</span></span>                                                                                                                  |
| <span data-ttu-id="ae552-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ae552-147">Search-Flags</span></span>           | <span data-ttu-id="ae552-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ae552-148">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="ae552-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ae552-149">System-Flags</span></span>           | <span data-ttu-id="ae552-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ae552-150">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="ae552-151">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ae552-151">Classes used in</span></span>        | [<span data-ttu-id="ae552-152">**MS-DFS-supprimé-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="ae552-152">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="ae552-153">**MS-DFS-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="ae552-153">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ae552-154">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ae552-154">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ae552-155">Entrée</span><span class="sxs-lookup"><span data-stu-id="ae552-155">Entry</span></span> | <span data-ttu-id="ae552-156">Value</span><span class="sxs-lookup"><span data-stu-id="ae552-156">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae552-157">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ae552-157">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="ae552-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ae552-158">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="ae552-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="ae552-159">System-Only</span></span>            | <span data-ttu-id="ae552-160">False</span><span class="sxs-lookup"><span data-stu-id="ae552-160">False</span></span>                                                                                                                  |
| <span data-ttu-id="ae552-161">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ae552-161">Is-Single-Valued</span></span>       | <span data-ttu-id="ae552-162">True</span><span class="sxs-lookup"><span data-stu-id="ae552-162">True</span></span>                                                                                                                   |
| <span data-ttu-id="ae552-163">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ae552-163">Is Indexed</span></span>             | <span data-ttu-id="ae552-164">False</span><span class="sxs-lookup"><span data-stu-id="ae552-164">False</span></span>                                                                                                                  |
| <span data-ttu-id="ae552-165">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ae552-165">In Global Catalog</span></span>      | <span data-ttu-id="ae552-166">False</span><span class="sxs-lookup"><span data-stu-id="ae552-166">False</span></span>                                                                                                                  |
| <span data-ttu-id="ae552-167">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ae552-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="ae552-168">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ae552-168">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="ae552-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ae552-169">Range-Lower</span></span>            | <span data-ttu-id="ae552-170">0</span><span class="sxs-lookup"><span data-stu-id="ae552-170">0</span></span>                                                                                                                      |
| <span data-ttu-id="ae552-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ae552-171">Range-Upper</span></span>            | <span data-ttu-id="ae552-172">32766</span><span class="sxs-lookup"><span data-stu-id="ae552-172">32766</span></span>                                                                                                                  |
| <span data-ttu-id="ae552-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ae552-173">Search-Flags</span></span>           | <span data-ttu-id="ae552-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ae552-174">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="ae552-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ae552-175">System-Flags</span></span>           | <span data-ttu-id="ae552-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ae552-176">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="ae552-177">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ae552-177">Classes used in</span></span>        | [<span data-ttu-id="ae552-178">**MS-DFS-supprimé-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="ae552-178">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="ae552-179">**MS-DFS-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="ae552-179">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ae552-180">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ae552-180">Windows Server 2012</span></span>



| <span data-ttu-id="ae552-181">Entrée</span><span class="sxs-lookup"><span data-stu-id="ae552-181">Entry</span></span> | <span data-ttu-id="ae552-182">Value</span><span class="sxs-lookup"><span data-stu-id="ae552-182">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae552-183">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ae552-183">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="ae552-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ae552-184">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="ae552-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="ae552-185">System-Only</span></span>            | <span data-ttu-id="ae552-186">False</span><span class="sxs-lookup"><span data-stu-id="ae552-186">False</span></span>                                                                                                                  |
| <span data-ttu-id="ae552-187">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ae552-187">Is-Single-Valued</span></span>       | <span data-ttu-id="ae552-188">True</span><span class="sxs-lookup"><span data-stu-id="ae552-188">True</span></span>                                                                                                                   |
| <span data-ttu-id="ae552-189">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ae552-189">Is Indexed</span></span>             | <span data-ttu-id="ae552-190">False</span><span class="sxs-lookup"><span data-stu-id="ae552-190">False</span></span>                                                                                                                  |
| <span data-ttu-id="ae552-191">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ae552-191">In Global Catalog</span></span>      | <span data-ttu-id="ae552-192">False</span><span class="sxs-lookup"><span data-stu-id="ae552-192">False</span></span>                                                                                                                  |
| <span data-ttu-id="ae552-193">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ae552-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="ae552-194">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ae552-194">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="ae552-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ae552-195">Range-Lower</span></span>            | <span data-ttu-id="ae552-196">0</span><span class="sxs-lookup"><span data-stu-id="ae552-196">0</span></span>                                                                                                                      |
| <span data-ttu-id="ae552-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ae552-197">Range-Upper</span></span>            | <span data-ttu-id="ae552-198">32766</span><span class="sxs-lookup"><span data-stu-id="ae552-198">32766</span></span>                                                                                                                  |
| <span data-ttu-id="ae552-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ae552-199">Search-Flags</span></span>           | <span data-ttu-id="ae552-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ae552-200">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="ae552-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ae552-201">System-Flags</span></span>           | <span data-ttu-id="ae552-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ae552-202">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="ae552-203">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ae552-203">Classes used in</span></span>        | [<span data-ttu-id="ae552-204">**MS-DFS-supprimé-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="ae552-204">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="ae552-205">**MS-DFS-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="ae552-205">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



 

 





