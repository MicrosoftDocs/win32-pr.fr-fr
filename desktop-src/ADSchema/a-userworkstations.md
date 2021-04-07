---
title: Attribut User-Workstations
description: Contient les noms NetBIOS ou DNS des ordinateurs exécutant Windows NT Workstation ou Windows 2000 professionnel à partir desquels l’utilisateur peut ouvrir une session.
ms.assetid: 92af070b-dadd-404d-8305-d85974639958
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut User-Workstations
- Schéma AD de l’attribut userWorkstations
topic_type:
- apiref
api_name:
- User-Workstations
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cad59905dbf24c8baa13969d9a2ce5452767163
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103844890"
---
# <a name="user-workstations-attribute"></a><span data-ttu-id="d0092-105">Attribut User-Workstations</span><span class="sxs-lookup"><span data-stu-id="d0092-105">User-Workstations attribute</span></span>

<span data-ttu-id="d0092-106">Contient les noms NetBIOS ou DNS des ordinateurs exécutant Windows NT Workstation ou Windows 2000 professionnel à partir desquels l’utilisateur peut ouvrir une session.</span><span class="sxs-lookup"><span data-stu-id="d0092-106">Contains the NetBIOS or DNS names of the computers running Windows NT Workstation or Windows 2000 Professional from which the user can log on.</span></span> <span data-ttu-id="d0092-107">Chaque nom NetBIOS est séparé par une virgule.</span><span class="sxs-lookup"><span data-stu-id="d0092-107">Each NetBIOS name is separated by a comma.</span></span> <span data-ttu-id="d0092-108">Les noms multiples doivent être séparés par des virgules.</span><span class="sxs-lookup"><span data-stu-id="d0092-108">Multiple names should be separated by commas.</span></span>

>[!Note]
><span data-ttu-id="d0092-109">Cet attribut utilisateur ne doit plus être utilisé.</span><span class="sxs-lookup"><span data-stu-id="d0092-109">This user attribute should not be used anymore.</span></span> <span data-ttu-id="d0092-110">Pour gérer les comptes qui peuvent ouvrir une session sur les stations de travail, nous vous recommandons d’utiliser les fonctionnalités « permettre l’ouverture d’une session locale » et « interdire l’ouverture d’une session locale » ou « autoriser l’ouverture d’une session via le Services Bureau à distance » et « interdire l’ouverture d’une session via Services Bureau à distance ».</span><span class="sxs-lookup"><span data-stu-id="d0092-110">To manage what accounts can logon to which workstations, we recommend using the “Allow Log on locally” and “Deny Log on locally” or “Allow log on through Remote Desktop Services” and “Deny log on through Remote Desktop Services”.</span></span>

| <span data-ttu-id="d0092-111">Entrée</span><span class="sxs-lookup"><span data-stu-id="d0092-111">Entry</span></span> | <span data-ttu-id="d0092-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="d0092-112">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0092-113">CN</span><span class="sxs-lookup"><span data-stu-id="d0092-113">CN</span></span>                | <span data-ttu-id="d0092-114">User-Workstations</span><span class="sxs-lookup"><span data-stu-id="d0092-114">User-Workstations</span></span>                                                                          |
| <span data-ttu-id="d0092-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="d0092-115">Ldap-Display-Name</span></span> | <span data-ttu-id="d0092-116">userWorkstations</span><span class="sxs-lookup"><span data-stu-id="d0092-116">userWorkstations</span></span>                                                                           |
| <span data-ttu-id="d0092-117">Taille</span><span class="sxs-lookup"><span data-stu-id="d0092-117">Size</span></span>              | \-                                                                                         |
| <span data-ttu-id="d0092-118">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="d0092-118">Update Privilege</span></span>  | <span data-ttu-id="d0092-119">Administrateur de domaine ou propriétaire du compte.</span><span class="sxs-lookup"><span data-stu-id="d0092-119">Domain administrator or account owner.</span></span>                                                     |
| <span data-ttu-id="d0092-120">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="d0092-120">Update Frequency</span></span>  | <span data-ttu-id="d0092-121">Lorsque l’enregistrement de l’utilisateur est créé et chaque fois que le privilège de connexion de l’utilisateur doit être modifié.</span><span class="sxs-lookup"><span data-stu-id="d0092-121">When the user's record is created and whenever the user's login privilege needs to change.</span></span> |
| <span data-ttu-id="d0092-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d0092-122">Attribute-Id</span></span>      | <span data-ttu-id="d0092-123">1.2.840.113556.1.4.86</span><span class="sxs-lookup"><span data-stu-id="d0092-123">1.2.840.113556.1.4.86</span></span>                                                                      |
| <span data-ttu-id="d0092-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="d0092-124">System-Id-Guid</span></span>    | <span data-ttu-id="d0092-125">bf9679d7-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="d0092-125">bf9679d7-0de6-11d0-a285-00aa003049e2</span></span>                                                       |
| <span data-ttu-id="d0092-126">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d0092-126">Syntax</span></span>            | [<span data-ttu-id="d0092-127">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="d0092-127">**String(Unicode)**</span></span>](s-string-unicode.md)                                                |



## <a name="implementations"></a><span data-ttu-id="d0092-128">Implémentations</span><span class="sxs-lookup"><span data-stu-id="d0092-128">Implementations</span></span>

-   [<span data-ttu-id="d0092-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d0092-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d0092-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d0092-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d0092-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d0092-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d0092-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d0092-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d0092-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d0092-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d0092-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d0092-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d0092-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d0092-135">Windows 2000 Server</span></span>



| <span data-ttu-id="d0092-136">Entrée</span><span class="sxs-lookup"><span data-stu-id="d0092-136">Entry</span></span> | <span data-ttu-id="d0092-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="d0092-137">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="d0092-138">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d0092-138">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="d0092-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d0092-139">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="d0092-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="d0092-140">System-Only</span></span>            | <span data-ttu-id="d0092-141">Faux</span><span class="sxs-lookup"><span data-stu-id="d0092-141">False</span></span>                             |
| <span data-ttu-id="d0092-142">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d0092-142">Is-Single-Valued</span></span>       | <span data-ttu-id="d0092-143">Vrai</span><span class="sxs-lookup"><span data-stu-id="d0092-143">True</span></span>                              |
| <span data-ttu-id="d0092-144">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d0092-144">Is Indexed</span></span>             | <span data-ttu-id="d0092-145">Faux</span><span class="sxs-lookup"><span data-stu-id="d0092-145">False</span></span>                             |
| <span data-ttu-id="d0092-146">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d0092-146">In Global Catalog</span></span>      | <span data-ttu-id="d0092-147">Faux</span><span class="sxs-lookup"><span data-stu-id="d0092-147">False</span></span>                             |
| <span data-ttu-id="d0092-148">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d0092-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="d0092-149">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d0092-149">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="d0092-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d0092-150">Range-Lower</span></span>            | <span data-ttu-id="d0092-151">0</span><span class="sxs-lookup"><span data-stu-id="d0092-151">0</span></span>                                 |
| <span data-ttu-id="d0092-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d0092-152">Range-Upper</span></span>            | <span data-ttu-id="d0092-153">1 024</span><span class="sxs-lookup"><span data-stu-id="d0092-153">1024</span></span>                              |
| <span data-ttu-id="d0092-154">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d0092-154">Search-Flags</span></span>           | <span data-ttu-id="d0092-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d0092-155">0x00000010</span></span>                        |
| <span data-ttu-id="d0092-156">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d0092-156">System-Flags</span></span>           | <span data-ttu-id="d0092-157">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d0092-157">0x00000010</span></span>                        |
| <span data-ttu-id="d0092-158">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d0092-158">Classes used in</span></span>        | [<span data-ttu-id="d0092-159">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="d0092-159">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d0092-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d0092-160">Windows Server 2003</span></span>



| <span data-ttu-id="d0092-161">Entrée</span><span class="sxs-lookup"><span data-stu-id="d0092-161">Entry</span></span> | <span data-ttu-id="d0092-162">Valeur</span><span class="sxs-lookup"><span data-stu-id="d0092-162">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="d0092-163">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d0092-163">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="d0092-164">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d0092-164">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="d0092-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="d0092-165">System-Only</span></span>            | <span data-ttu-id="d0092-166">Faux</span><span class="sxs-lookup"><span data-stu-id="d0092-166">False</span></span>                             |
| <span data-ttu-id="d0092-167">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d0092-167">Is-Single-Valued</span></span>       | <span data-ttu-id="d0092-168">Vrai</span><span class="sxs-lookup"><span data-stu-id="d0092-168">True</span></span>                              |
| <span data-ttu-id="d0092-169">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d0092-169">Is Indexed</span></span>             | <span data-ttu-id="d0092-170">Faux</span><span class="sxs-lookup"><span data-stu-id="d0092-170">False</span></span>                             |
| <span data-ttu-id="d0092-171">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d0092-171">In Global Catalog</span></span>      | <span data-ttu-id="d0092-172">Faux</span><span class="sxs-lookup"><span data-stu-id="d0092-172">False</span></span>                             |
| <span data-ttu-id="d0092-173">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d0092-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="d0092-174">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d0092-174">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="d0092-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d0092-175">Range-Lower</span></span>            | <span data-ttu-id="d0092-176">0</span><span class="sxs-lookup"><span data-stu-id="d0092-176">0</span></span>                                 |
| <span data-ttu-id="d0092-177">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d0092-177">Range-Upper</span></span>            | <span data-ttu-id="d0092-178">1 024</span><span class="sxs-lookup"><span data-stu-id="d0092-178">1024</span></span>                              |
| <span data-ttu-id="d0092-179">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d0092-179">Search-Flags</span></span>           | <span data-ttu-id="d0092-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d0092-180">0x00000010</span></span>                        |
| <span data-ttu-id="d0092-181">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d0092-181">System-Flags</span></span>           | <span data-ttu-id="d0092-182">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d0092-182">0x00000010</span></span>                        |
| <span data-ttu-id="d0092-183">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d0092-183">Classes used in</span></span>        | [<span data-ttu-id="d0092-184">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="d0092-184">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d0092-185">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d0092-185">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d0092-186">Entrée</span><span class="sxs-lookup"><span data-stu-id="d0092-186">Entry</span></span> | <span data-ttu-id="d0092-187">Valeur</span><span class="sxs-lookup"><span data-stu-id="d0092-187">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="d0092-188">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d0092-188">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="d0092-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d0092-189">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="d0092-190">System-Only</span><span class="sxs-lookup"><span data-stu-id="d0092-190">System-Only</span></span>            | <span data-ttu-id="d0092-191">Faux</span><span class="sxs-lookup"><span data-stu-id="d0092-191">False</span></span>                             |
| <span data-ttu-id="d0092-192">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d0092-192">Is-Single-Valued</span></span>       | <span data-ttu-id="d0092-193">Vrai</span><span class="sxs-lookup"><span data-stu-id="d0092-193">True</span></span>                              |
| <span data-ttu-id="d0092-194">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d0092-194">Is Indexed</span></span>             | <span data-ttu-id="d0092-195">Faux</span><span class="sxs-lookup"><span data-stu-id="d0092-195">False</span></span>                             |
| <span data-ttu-id="d0092-196">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d0092-196">In Global Catalog</span></span>      | <span data-ttu-id="d0092-197">Faux</span><span class="sxs-lookup"><span data-stu-id="d0092-197">False</span></span>                             |
| <span data-ttu-id="d0092-198">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d0092-198">NT-Security-Descriptor</span></span> | <span data-ttu-id="d0092-199">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d0092-199">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="d0092-200">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d0092-200">Range-Lower</span></span>            | <span data-ttu-id="d0092-201">0</span><span class="sxs-lookup"><span data-stu-id="d0092-201">0</span></span>                                 |
| <span data-ttu-id="d0092-202">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d0092-202">Range-Upper</span></span>            | <span data-ttu-id="d0092-203">1 024</span><span class="sxs-lookup"><span data-stu-id="d0092-203">1024</span></span>                              |
| <span data-ttu-id="d0092-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d0092-204">Search-Flags</span></span>           | <span data-ttu-id="d0092-205">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d0092-205">0x00000010</span></span>                        |
| <span data-ttu-id="d0092-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d0092-206">System-Flags</span></span>           | <span data-ttu-id="d0092-207">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d0092-207">0x00000010</span></span>                        |
| <span data-ttu-id="d0092-208">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d0092-208">Classes used in</span></span>        | [<span data-ttu-id="d0092-209">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="d0092-209">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d0092-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d0092-210">Windows Server 2008</span></span>



| <span data-ttu-id="d0092-211">Entrée</span><span class="sxs-lookup"><span data-stu-id="d0092-211">Entry</span></span> | <span data-ttu-id="d0092-212">Valeur</span><span class="sxs-lookup"><span data-stu-id="d0092-212">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="d0092-213">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d0092-213">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="d0092-214">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d0092-214">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="d0092-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="d0092-215">System-Only</span></span>            | <span data-ttu-id="d0092-216">Faux</span><span class="sxs-lookup"><span data-stu-id="d0092-216">False</span></span>                             |
| <span data-ttu-id="d0092-217">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d0092-217">Is-Single-Valued</span></span>       | <span data-ttu-id="d0092-218">Vrai</span><span class="sxs-lookup"><span data-stu-id="d0092-218">True</span></span>                              |
| <span data-ttu-id="d0092-219">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d0092-219">Is Indexed</span></span>             | <span data-ttu-id="d0092-220">Faux</span><span class="sxs-lookup"><span data-stu-id="d0092-220">False</span></span>                             |
| <span data-ttu-id="d0092-221">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d0092-221">In Global Catalog</span></span>      | <span data-ttu-id="d0092-222">Faux</span><span class="sxs-lookup"><span data-stu-id="d0092-222">False</span></span>                             |
| <span data-ttu-id="d0092-223">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d0092-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="d0092-224">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d0092-224">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="d0092-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d0092-225">Range-Lower</span></span>            | <span data-ttu-id="d0092-226">0</span><span class="sxs-lookup"><span data-stu-id="d0092-226">0</span></span>                                 |
| <span data-ttu-id="d0092-227">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d0092-227">Range-Upper</span></span>            | <span data-ttu-id="d0092-228">1 024</span><span class="sxs-lookup"><span data-stu-id="d0092-228">1024</span></span>                              |
| <span data-ttu-id="d0092-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d0092-229">Search-Flags</span></span>           | <span data-ttu-id="d0092-230">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d0092-230">0x00000010</span></span>                        |
| <span data-ttu-id="d0092-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d0092-231">System-Flags</span></span>           | <span data-ttu-id="d0092-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d0092-232">0x00000010</span></span>                        |
| <span data-ttu-id="d0092-233">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d0092-233">Classes used in</span></span>        | [<span data-ttu-id="d0092-234">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="d0092-234">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d0092-235">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d0092-235">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d0092-236">Entrée</span><span class="sxs-lookup"><span data-stu-id="d0092-236">Entry</span></span> | <span data-ttu-id="d0092-237">Valeur</span><span class="sxs-lookup"><span data-stu-id="d0092-237">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="d0092-238">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d0092-238">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="d0092-239">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d0092-239">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="d0092-240">System-Only</span><span class="sxs-lookup"><span data-stu-id="d0092-240">System-Only</span></span>            | <span data-ttu-id="d0092-241">Faux</span><span class="sxs-lookup"><span data-stu-id="d0092-241">False</span></span>                             |
| <span data-ttu-id="d0092-242">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d0092-242">Is-Single-Valued</span></span>       | <span data-ttu-id="d0092-243">Vrai</span><span class="sxs-lookup"><span data-stu-id="d0092-243">True</span></span>                              |
| <span data-ttu-id="d0092-244">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d0092-244">Is Indexed</span></span>             | <span data-ttu-id="d0092-245">Faux</span><span class="sxs-lookup"><span data-stu-id="d0092-245">False</span></span>                             |
| <span data-ttu-id="d0092-246">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d0092-246">In Global Catalog</span></span>      | <span data-ttu-id="d0092-247">Faux</span><span class="sxs-lookup"><span data-stu-id="d0092-247">False</span></span>                             |
| <span data-ttu-id="d0092-248">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d0092-248">NT-Security-Descriptor</span></span> | <span data-ttu-id="d0092-249">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d0092-249">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="d0092-250">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d0092-250">Range-Lower</span></span>            | <span data-ttu-id="d0092-251">0</span><span class="sxs-lookup"><span data-stu-id="d0092-251">0</span></span>                                 |
| <span data-ttu-id="d0092-252">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d0092-252">Range-Upper</span></span>            | <span data-ttu-id="d0092-253">1 024</span><span class="sxs-lookup"><span data-stu-id="d0092-253">1024</span></span>                              |
| <span data-ttu-id="d0092-254">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d0092-254">Search-Flags</span></span>           | <span data-ttu-id="d0092-255">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d0092-255">0x00000010</span></span>                        |
| <span data-ttu-id="d0092-256">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d0092-256">System-Flags</span></span>           | <span data-ttu-id="d0092-257">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d0092-257">0x00000010</span></span>                        |
| <span data-ttu-id="d0092-258">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d0092-258">Classes used in</span></span>        | [<span data-ttu-id="d0092-259">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="d0092-259">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d0092-260">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d0092-260">Windows Server 2012</span></span>



| <span data-ttu-id="d0092-261">Entrée</span><span class="sxs-lookup"><span data-stu-id="d0092-261">Entry</span></span> | <span data-ttu-id="d0092-262">Valeur</span><span class="sxs-lookup"><span data-stu-id="d0092-262">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="d0092-263">ID de lien</span><span class="sxs-lookup"><span data-stu-id="d0092-263">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="d0092-264">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d0092-264">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="d0092-265">System-Only</span><span class="sxs-lookup"><span data-stu-id="d0092-265">System-Only</span></span>            | <span data-ttu-id="d0092-266">Faux</span><span class="sxs-lookup"><span data-stu-id="d0092-266">False</span></span>                             |
| <span data-ttu-id="d0092-267">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="d0092-267">Is-Single-Valued</span></span>       | <span data-ttu-id="d0092-268">Vrai</span><span class="sxs-lookup"><span data-stu-id="d0092-268">True</span></span>                              |
| <span data-ttu-id="d0092-269">Est indexé</span><span class="sxs-lookup"><span data-stu-id="d0092-269">Is Indexed</span></span>             | <span data-ttu-id="d0092-270">Faux</span><span class="sxs-lookup"><span data-stu-id="d0092-270">False</span></span>                             |
| <span data-ttu-id="d0092-271">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="d0092-271">In Global Catalog</span></span>      | <span data-ttu-id="d0092-272">Faux</span><span class="sxs-lookup"><span data-stu-id="d0092-272">False</span></span>                             |
| <span data-ttu-id="d0092-273">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="d0092-273">NT-Security-Descriptor</span></span> | <span data-ttu-id="d0092-274">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="d0092-274">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="d0092-275">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d0092-275">Range-Lower</span></span>            | <span data-ttu-id="d0092-276">0</span><span class="sxs-lookup"><span data-stu-id="d0092-276">0</span></span>                                 |
| <span data-ttu-id="d0092-277">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d0092-277">Range-Upper</span></span>            | <span data-ttu-id="d0092-278">1 024</span><span class="sxs-lookup"><span data-stu-id="d0092-278">1024</span></span>                              |
| <span data-ttu-id="d0092-279">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d0092-279">Search-Flags</span></span>           | <span data-ttu-id="d0092-280">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d0092-280">0x00000010</span></span>                        |
| <span data-ttu-id="d0092-281">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d0092-281">System-Flags</span></span>           | <span data-ttu-id="d0092-282">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d0092-282">0x00000010</span></span>                        |
| <span data-ttu-id="d0092-283">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="d0092-283">Classes used in</span></span>        | [<span data-ttu-id="d0092-284">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="d0092-284">**User**</span></span>](c-user.md)<br/> |



 

 





