---
title: attribut ms-TS-Profile-Path
description: Chemin du profil des services Terminal Server spécifie un chemin d’accès de profil itinérant ou obligatoire à utiliser lorsque l’utilisateur ouvre une session sur le serveur Terminal Server. Le chemin d’accès au profil est au format de chemin d’accès réseau \\ \\ NomServeur \\ ProfilesFolderName \\ nom d’utilisateur.
ms.assetid: 9b13f91d-c3ee-4862-800c-fda831dce859
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut ms-TS-Profile-Path
- Schéma AD de l’attribut msTSProfilePath
topic_type:
- apiref
api_name:
- ms-TS-Profile-Path
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67243c2ef588bd1470a50417c0948b1ea4ea7fa9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103943134"
---
# <a name="ms-ts-profile-path-attribute"></a><span data-ttu-id="57dd2-106">attribut ms-TS-Profile-Path</span><span class="sxs-lookup"><span data-stu-id="57dd2-106">ms-TS-Profile-Path attribute</span></span>

<span data-ttu-id="57dd2-107">Chemin du profil des services Terminal Server spécifie un chemin d’accès de profil itinérant ou obligatoire à utiliser lorsque l’utilisateur ouvre une session sur le serveur Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="57dd2-107">Terminal Services Profile Path specifies a roaming or mandatory profile path to use when the user logs on to the terminal server.</span></span> <span data-ttu-id="57dd2-108">Le chemin d’accès au profil est au format de chemin d’accès réseau suivant : **\\\\** _NomServeur_ *_\\_* _ProfilesFolderName_ *_\\_* _nom d’utilisateur_.</span><span class="sxs-lookup"><span data-stu-id="57dd2-108">The profile path is in the following network path format: **\\\\**_ServerName_*_\\_*_ProfilesFolderName_*_\\_*_UserName_.</span></span>



| <span data-ttu-id="57dd2-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="57dd2-109">Entry</span></span> | <span data-ttu-id="57dd2-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="57dd2-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="57dd2-111">CN</span><span class="sxs-lookup"><span data-stu-id="57dd2-111">CN</span></span>                | <span data-ttu-id="57dd2-112">MS-TS-Profile-chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="57dd2-112">ms-TS-Profile-Path</span></span>                          |
| <span data-ttu-id="57dd2-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="57dd2-113">Ldap-Display-Name</span></span> | <span data-ttu-id="57dd2-114">msTSProfilePath</span><span class="sxs-lookup"><span data-stu-id="57dd2-114">msTSProfilePath</span></span>                             |
| <span data-ttu-id="57dd2-115">Taille</span><span class="sxs-lookup"><span data-stu-id="57dd2-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="57dd2-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="57dd2-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="57dd2-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="57dd2-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="57dd2-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="57dd2-118">Attribute-Id</span></span>      | <span data-ttu-id="57dd2-119">1.2.840.113556.1.4.1976</span><span class="sxs-lookup"><span data-stu-id="57dd2-119">1.2.840.113556.1.4.1976</span></span>                     |
| <span data-ttu-id="57dd2-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="57dd2-120">System-Id-Guid</span></span>    | <span data-ttu-id="57dd2-121">e65c30db-316C-4060-a3a0-387b083f09cd</span><span class="sxs-lookup"><span data-stu-id="57dd2-121">e65c30db-316c-4060-a3a0-387b083f09cd</span></span>        |
| <span data-ttu-id="57dd2-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="57dd2-122">Syntax</span></span>            | [<span data-ttu-id="57dd2-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="57dd2-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="57dd2-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="57dd2-124">Implementations</span></span>

-   [<span data-ttu-id="57dd2-125">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="57dd2-125">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="57dd2-126">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="57dd2-126">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="57dd2-127">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="57dd2-127">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="57dd2-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="57dd2-128">Windows Server 2008</span></span>



| <span data-ttu-id="57dd2-129">Entrée</span><span class="sxs-lookup"><span data-stu-id="57dd2-129">Entry</span></span> | <span data-ttu-id="57dd2-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="57dd2-130">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="57dd2-131">ID de lien</span><span class="sxs-lookup"><span data-stu-id="57dd2-131">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="57dd2-132">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="57dd2-132">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="57dd2-133">System-Only</span><span class="sxs-lookup"><span data-stu-id="57dd2-133">System-Only</span></span>            | <span data-ttu-id="57dd2-134">Faux</span><span class="sxs-lookup"><span data-stu-id="57dd2-134">False</span></span>                             |
| <span data-ttu-id="57dd2-135">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="57dd2-135">Is-Single-Valued</span></span>       | <span data-ttu-id="57dd2-136">Vrai</span><span class="sxs-lookup"><span data-stu-id="57dd2-136">True</span></span>                              |
| <span data-ttu-id="57dd2-137">Est indexé</span><span class="sxs-lookup"><span data-stu-id="57dd2-137">Is Indexed</span></span>             | <span data-ttu-id="57dd2-138">Faux</span><span class="sxs-lookup"><span data-stu-id="57dd2-138">False</span></span>                             |
| <span data-ttu-id="57dd2-139">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="57dd2-139">In Global Catalog</span></span>      | <span data-ttu-id="57dd2-140">Faux</span><span class="sxs-lookup"><span data-stu-id="57dd2-140">False</span></span>                             |
| <span data-ttu-id="57dd2-141">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="57dd2-141">NT-Security-Descriptor</span></span> | <span data-ttu-id="57dd2-142">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="57dd2-142">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="57dd2-143">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="57dd2-143">Range-Lower</span></span>            | <span data-ttu-id="57dd2-144">0</span><span class="sxs-lookup"><span data-stu-id="57dd2-144">0</span></span>                                 |
| <span data-ttu-id="57dd2-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="57dd2-145">Range-Upper</span></span>            | <span data-ttu-id="57dd2-146">32767</span><span class="sxs-lookup"><span data-stu-id="57dd2-146">32767</span></span>                             |
| <span data-ttu-id="57dd2-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="57dd2-147">Search-Flags</span></span>           | <span data-ttu-id="57dd2-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="57dd2-148">0x00000000</span></span>                        |
| <span data-ttu-id="57dd2-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="57dd2-149">System-Flags</span></span>           | <span data-ttu-id="57dd2-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="57dd2-150">0x00000010</span></span>                        |
| <span data-ttu-id="57dd2-151">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="57dd2-151">Classes used in</span></span>        | [<span data-ttu-id="57dd2-152">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="57dd2-152">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="57dd2-153">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="57dd2-153">Windows Server 2008 R2</span></span>



| <span data-ttu-id="57dd2-154">Entrée</span><span class="sxs-lookup"><span data-stu-id="57dd2-154">Entry</span></span> | <span data-ttu-id="57dd2-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="57dd2-155">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="57dd2-156">ID de lien</span><span class="sxs-lookup"><span data-stu-id="57dd2-156">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="57dd2-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="57dd2-157">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="57dd2-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="57dd2-158">System-Only</span></span>            | <span data-ttu-id="57dd2-159">Faux</span><span class="sxs-lookup"><span data-stu-id="57dd2-159">False</span></span>                             |
| <span data-ttu-id="57dd2-160">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="57dd2-160">Is-Single-Valued</span></span>       | <span data-ttu-id="57dd2-161">Vrai</span><span class="sxs-lookup"><span data-stu-id="57dd2-161">True</span></span>                              |
| <span data-ttu-id="57dd2-162">Est indexé</span><span class="sxs-lookup"><span data-stu-id="57dd2-162">Is Indexed</span></span>             | <span data-ttu-id="57dd2-163">Faux</span><span class="sxs-lookup"><span data-stu-id="57dd2-163">False</span></span>                             |
| <span data-ttu-id="57dd2-164">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="57dd2-164">In Global Catalog</span></span>      | <span data-ttu-id="57dd2-165">Faux</span><span class="sxs-lookup"><span data-stu-id="57dd2-165">False</span></span>                             |
| <span data-ttu-id="57dd2-166">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="57dd2-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="57dd2-167">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="57dd2-167">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="57dd2-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="57dd2-168">Range-Lower</span></span>            | <span data-ttu-id="57dd2-169">0</span><span class="sxs-lookup"><span data-stu-id="57dd2-169">0</span></span>                                 |
| <span data-ttu-id="57dd2-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="57dd2-170">Range-Upper</span></span>            | <span data-ttu-id="57dd2-171">32767</span><span class="sxs-lookup"><span data-stu-id="57dd2-171">32767</span></span>                             |
| <span data-ttu-id="57dd2-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="57dd2-172">Search-Flags</span></span>           | <span data-ttu-id="57dd2-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="57dd2-173">0x00000000</span></span>                        |
| <span data-ttu-id="57dd2-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="57dd2-174">System-Flags</span></span>           | <span data-ttu-id="57dd2-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="57dd2-175">0x00000010</span></span>                        |
| <span data-ttu-id="57dd2-176">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="57dd2-176">Classes used in</span></span>        | [<span data-ttu-id="57dd2-177">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="57dd2-177">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="57dd2-178">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="57dd2-178">Windows Server 2012</span></span>



| <span data-ttu-id="57dd2-179">Entrée</span><span class="sxs-lookup"><span data-stu-id="57dd2-179">Entry</span></span> | <span data-ttu-id="57dd2-180">Valeur</span><span class="sxs-lookup"><span data-stu-id="57dd2-180">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="57dd2-181">ID de lien</span><span class="sxs-lookup"><span data-stu-id="57dd2-181">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="57dd2-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="57dd2-182">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="57dd2-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="57dd2-183">System-Only</span></span>            | <span data-ttu-id="57dd2-184">Faux</span><span class="sxs-lookup"><span data-stu-id="57dd2-184">False</span></span>                             |
| <span data-ttu-id="57dd2-185">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="57dd2-185">Is-Single-Valued</span></span>       | <span data-ttu-id="57dd2-186">Vrai</span><span class="sxs-lookup"><span data-stu-id="57dd2-186">True</span></span>                              |
| <span data-ttu-id="57dd2-187">Est indexé</span><span class="sxs-lookup"><span data-stu-id="57dd2-187">Is Indexed</span></span>             | <span data-ttu-id="57dd2-188">Faux</span><span class="sxs-lookup"><span data-stu-id="57dd2-188">False</span></span>                             |
| <span data-ttu-id="57dd2-189">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="57dd2-189">In Global Catalog</span></span>      | <span data-ttu-id="57dd2-190">Faux</span><span class="sxs-lookup"><span data-stu-id="57dd2-190">False</span></span>                             |
| <span data-ttu-id="57dd2-191">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="57dd2-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="57dd2-192">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="57dd2-192">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="57dd2-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="57dd2-193">Range-Lower</span></span>            | <span data-ttu-id="57dd2-194">0</span><span class="sxs-lookup"><span data-stu-id="57dd2-194">0</span></span>                                 |
| <span data-ttu-id="57dd2-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="57dd2-195">Range-Upper</span></span>            | <span data-ttu-id="57dd2-196">32767</span><span class="sxs-lookup"><span data-stu-id="57dd2-196">32767</span></span>                             |
| <span data-ttu-id="57dd2-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="57dd2-197">Search-Flags</span></span>           | <span data-ttu-id="57dd2-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="57dd2-198">0x00000000</span></span>                        |
| <span data-ttu-id="57dd2-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="57dd2-199">System-Flags</span></span>           | <span data-ttu-id="57dd2-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="57dd2-200">0x00000010</span></span>                        |
| <span data-ttu-id="57dd2-201">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="57dd2-201">Classes used in</span></span>        | [<span data-ttu-id="57dd2-202">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="57dd2-202">**User**</span></span>](c-user.md)<br/> |



 

 





