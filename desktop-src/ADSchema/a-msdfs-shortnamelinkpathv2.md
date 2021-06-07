---
title: attribut ms-DFS-Short-Name-Link-Path-v2
description: Chemin d’accès de lien DFS de nom abrégé relatif au partage cible racine DFS (autrement dit, sans les composants de nom de serveur/domaine et d’espace de noms DFS). Utilisez des barres obliques (/) à la place des barres obliques inverses ( \) , afin que les recherches LDAP puissent être effectuées sans avoir à utiliser des séquences d’échappement.
ms.assetid: 0589d3f5-9734-4f95-bba9-22f13bb1c9f1
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut ms-DFS-Short-Name-Link-Path-v2
- Schéma AD de l’attribut msDFS-ShortNameLinkPathv2
topic_type:
- apiref
api_name:
- ms-DFS-Short-Name-Link-Path-v2
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 663ee1ff2dac67eff7bd9eca87aa8eacf40436ff
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386848"
---
# <a name="ms-dfs-short-name-link-path-v2-attribute"></a><span data-ttu-id="13f14-106">attribut ms-DFS-Short-Name-Link-Path-v2</span><span class="sxs-lookup"><span data-stu-id="13f14-106">ms-DFS-Short-Name-Link-Path-v2 attribute</span></span>

<span data-ttu-id="13f14-107">Chemin d’accès de lien DFS de nom abrégé relatif au partage cible racine DFS (autrement dit, sans les composants de nom de serveur/domaine et d’espace de noms DFS).</span><span class="sxs-lookup"><span data-stu-id="13f14-107">Short Name DFS link path relative to the DFS root target share (that is, without the server/domain and DFS namespace name components).</span></span> <span data-ttu-id="13f14-108">Utilisez des barres obliques (/) à la place des barres obliques inverses ( \\ ), afin que les recherches LDAP puissent être effectuées sans avoir à utiliser des séquences d’échappement.</span><span class="sxs-lookup"><span data-stu-id="13f14-108">Use forward slashes (/) instead of backslashes (\\), so that LDAP searches can be done without having to use escapes.</span></span>



| <span data-ttu-id="13f14-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="13f14-109">Entry</span></span> | <span data-ttu-id="13f14-110">Value</span><span class="sxs-lookup"><span data-stu-id="13f14-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="13f14-111">CN</span><span class="sxs-lookup"><span data-stu-id="13f14-111">CN</span></span>                | <span data-ttu-id="13f14-112">MS-DFS-Short-Name-Link-Path-v2</span><span class="sxs-lookup"><span data-stu-id="13f14-112">ms-DFS-Short-Name-Link-Path-v2</span></span>              |
| <span data-ttu-id="13f14-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="13f14-113">Ldap-Display-Name</span></span> | <span data-ttu-id="13f14-114">msDFS-ShortNameLinkPathv2</span><span class="sxs-lookup"><span data-stu-id="13f14-114">msDFS-ShortNameLinkPathv2</span></span>                   |
| <span data-ttu-id="13f14-115">Taille</span><span class="sxs-lookup"><span data-stu-id="13f14-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="13f14-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="13f14-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="13f14-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="13f14-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="13f14-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="13f14-118">Attribute-Id</span></span>      | <span data-ttu-id="13f14-119">1.2.840.113556.1.4.2042</span><span class="sxs-lookup"><span data-stu-id="13f14-119">1.2.840.113556.1.4.2042</span></span>                     |
| <span data-ttu-id="13f14-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="13f14-120">System-Id-Guid</span></span>    | <span data-ttu-id="13f14-121">2d7826f0-4cf7-42e9-a039-1110e0d9ca99</span><span class="sxs-lookup"><span data-stu-id="13f14-121">2d7826f0-4cf7-42e9-a039-1110e0d9ca99</span></span>        |
| <span data-ttu-id="13f14-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="13f14-122">Syntax</span></span>            | [<span data-ttu-id="13f14-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="13f14-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="13f14-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="13f14-124">Implementations</span></span>

-   [<span data-ttu-id="13f14-125">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="13f14-125">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="13f14-126">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="13f14-126">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="13f14-127">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="13f14-127">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="13f14-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="13f14-128">Windows Server 2008</span></span>



| <span data-ttu-id="13f14-129">Entrée</span><span class="sxs-lookup"><span data-stu-id="13f14-129">Entry</span></span> | <span data-ttu-id="13f14-130">Value</span><span class="sxs-lookup"><span data-stu-id="13f14-130">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13f14-131">ID de lien</span><span class="sxs-lookup"><span data-stu-id="13f14-131">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="13f14-132">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="13f14-132">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="13f14-133">System-Only</span><span class="sxs-lookup"><span data-stu-id="13f14-133">System-Only</span></span>            | <span data-ttu-id="13f14-134">False</span><span class="sxs-lookup"><span data-stu-id="13f14-134">False</span></span>                                                                                                                  |
| <span data-ttu-id="13f14-135">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="13f14-135">Is-Single-Valued</span></span>       | <span data-ttu-id="13f14-136">True</span><span class="sxs-lookup"><span data-stu-id="13f14-136">True</span></span>                                                                                                                   |
| <span data-ttu-id="13f14-137">Est indexé</span><span class="sxs-lookup"><span data-stu-id="13f14-137">Is Indexed</span></span>             | <span data-ttu-id="13f14-138">False</span><span class="sxs-lookup"><span data-stu-id="13f14-138">False</span></span>                                                                                                                  |
| <span data-ttu-id="13f14-139">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="13f14-139">In Global Catalog</span></span>      | <span data-ttu-id="13f14-140">False</span><span class="sxs-lookup"><span data-stu-id="13f14-140">False</span></span>                                                                                                                  |
| <span data-ttu-id="13f14-141">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="13f14-141">NT-Security-Descriptor</span></span> | <span data-ttu-id="13f14-142">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="13f14-142">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="13f14-143">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="13f14-143">Range-Lower</span></span>            | <span data-ttu-id="13f14-144">0</span><span class="sxs-lookup"><span data-stu-id="13f14-144">0</span></span>                                                                                                                      |
| <span data-ttu-id="13f14-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="13f14-145">Range-Upper</span></span>            | <span data-ttu-id="13f14-146">32766</span><span class="sxs-lookup"><span data-stu-id="13f14-146">32766</span></span>                                                                                                                  |
| <span data-ttu-id="13f14-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="13f14-147">Search-Flags</span></span>           | <span data-ttu-id="13f14-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="13f14-148">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="13f14-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="13f14-149">System-Flags</span></span>           | <span data-ttu-id="13f14-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="13f14-150">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="13f14-151">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="13f14-151">Classes used in</span></span>        | [<span data-ttu-id="13f14-152">**MS-DFS-supprimé-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="13f14-152">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="13f14-153">**MS-DFS-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="13f14-153">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="13f14-154">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="13f14-154">Windows Server 2008 R2</span></span>



| <span data-ttu-id="13f14-155">Entrée</span><span class="sxs-lookup"><span data-stu-id="13f14-155">Entry</span></span> | <span data-ttu-id="13f14-156">Value</span><span class="sxs-lookup"><span data-stu-id="13f14-156">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13f14-157">ID de lien</span><span class="sxs-lookup"><span data-stu-id="13f14-157">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="13f14-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="13f14-158">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="13f14-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="13f14-159">System-Only</span></span>            | <span data-ttu-id="13f14-160">False</span><span class="sxs-lookup"><span data-stu-id="13f14-160">False</span></span>                                                                                                                  |
| <span data-ttu-id="13f14-161">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="13f14-161">Is-Single-Valued</span></span>       | <span data-ttu-id="13f14-162">True</span><span class="sxs-lookup"><span data-stu-id="13f14-162">True</span></span>                                                                                                                   |
| <span data-ttu-id="13f14-163">Est indexé</span><span class="sxs-lookup"><span data-stu-id="13f14-163">Is Indexed</span></span>             | <span data-ttu-id="13f14-164">False</span><span class="sxs-lookup"><span data-stu-id="13f14-164">False</span></span>                                                                                                                  |
| <span data-ttu-id="13f14-165">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="13f14-165">In Global Catalog</span></span>      | <span data-ttu-id="13f14-166">False</span><span class="sxs-lookup"><span data-stu-id="13f14-166">False</span></span>                                                                                                                  |
| <span data-ttu-id="13f14-167">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="13f14-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="13f14-168">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="13f14-168">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="13f14-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="13f14-169">Range-Lower</span></span>            | <span data-ttu-id="13f14-170">0</span><span class="sxs-lookup"><span data-stu-id="13f14-170">0</span></span>                                                                                                                      |
| <span data-ttu-id="13f14-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="13f14-171">Range-Upper</span></span>            | <span data-ttu-id="13f14-172">32766</span><span class="sxs-lookup"><span data-stu-id="13f14-172">32766</span></span>                                                                                                                  |
| <span data-ttu-id="13f14-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="13f14-173">Search-Flags</span></span>           | <span data-ttu-id="13f14-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="13f14-174">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="13f14-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="13f14-175">System-Flags</span></span>           | <span data-ttu-id="13f14-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="13f14-176">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="13f14-177">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="13f14-177">Classes used in</span></span>        | [<span data-ttu-id="13f14-178">**MS-DFS-supprimé-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="13f14-178">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="13f14-179">**MS-DFS-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="13f14-179">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="13f14-180">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="13f14-180">Windows Server 2012</span></span>



| <span data-ttu-id="13f14-181">Entrée</span><span class="sxs-lookup"><span data-stu-id="13f14-181">Entry</span></span> | <span data-ttu-id="13f14-182">Value</span><span class="sxs-lookup"><span data-stu-id="13f14-182">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13f14-183">ID de lien</span><span class="sxs-lookup"><span data-stu-id="13f14-183">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="13f14-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="13f14-184">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="13f14-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="13f14-185">System-Only</span></span>            | <span data-ttu-id="13f14-186">False</span><span class="sxs-lookup"><span data-stu-id="13f14-186">False</span></span>                                                                                                                  |
| <span data-ttu-id="13f14-187">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="13f14-187">Is-Single-Valued</span></span>       | <span data-ttu-id="13f14-188">True</span><span class="sxs-lookup"><span data-stu-id="13f14-188">True</span></span>                                                                                                                   |
| <span data-ttu-id="13f14-189">Est indexé</span><span class="sxs-lookup"><span data-stu-id="13f14-189">Is Indexed</span></span>             | <span data-ttu-id="13f14-190">False</span><span class="sxs-lookup"><span data-stu-id="13f14-190">False</span></span>                                                                                                                  |
| <span data-ttu-id="13f14-191">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="13f14-191">In Global Catalog</span></span>      | <span data-ttu-id="13f14-192">False</span><span class="sxs-lookup"><span data-stu-id="13f14-192">False</span></span>                                                                                                                  |
| <span data-ttu-id="13f14-193">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="13f14-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="13f14-194">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="13f14-194">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="13f14-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="13f14-195">Range-Lower</span></span>            | <span data-ttu-id="13f14-196">0</span><span class="sxs-lookup"><span data-stu-id="13f14-196">0</span></span>                                                                                                                      |
| <span data-ttu-id="13f14-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="13f14-197">Range-Upper</span></span>            | <span data-ttu-id="13f14-198">32766</span><span class="sxs-lookup"><span data-stu-id="13f14-198">32766</span></span>                                                                                                                  |
| <span data-ttu-id="13f14-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="13f14-199">Search-Flags</span></span>           | <span data-ttu-id="13f14-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="13f14-200">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="13f14-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="13f14-201">System-Flags</span></span>           | <span data-ttu-id="13f14-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="13f14-202">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="13f14-203">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="13f14-203">Classes used in</span></span>        | [<span data-ttu-id="13f14-204">**MS-DFS-supprimé-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="13f14-204">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="13f14-205">**MS-DFS-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="13f14-205">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



 

 





