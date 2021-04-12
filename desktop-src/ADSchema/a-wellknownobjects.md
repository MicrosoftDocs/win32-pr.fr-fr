---
title: Attribut des objets connus
description: Cet attribut contient une liste de conteneurs d’objets connus par GUID et par nom unique.
ms.assetid: e3c2d243-6734-4c2f-9ead-bc4ec071d1f1
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory des attributs d’objets bien connus
- Schéma AD de l’attribut wellKnownObjects
topic_type:
- apiref
api_name:
- Well-Known-Objects
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16e21df3db14a29de137af4792f0e9ca6df27b90
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104480197"
---
# <a name="well-known-objects-attribute"></a><span data-ttu-id="ec2f8-105">Attribut des objets connus</span><span class="sxs-lookup"><span data-stu-id="ec2f8-105">Well-Known-Objects attribute</span></span>

<span data-ttu-id="ec2f8-106">Cet attribut contient une liste de conteneurs d’objets connus par GUID et par nom unique.</span><span class="sxs-lookup"><span data-stu-id="ec2f8-106">This attribute contains a list of well-known object containers by GUID and distinguished name.</span></span> <span data-ttu-id="ec2f8-107">Les objets connus sont des conteneurs système.</span><span class="sxs-lookup"><span data-stu-id="ec2f8-107">The well-known objects are system containers.</span></span> <span data-ttu-id="ec2f8-108">Ces informations sont utilisées pour récupérer un objet après qu’il a été déplacé en utilisant uniquement le GUID et le nom de domaine.</span><span class="sxs-lookup"><span data-stu-id="ec2f8-108">This information is used to retrieve an object after it has been moved by using just the GUID and the domain name.</span></span> <span data-ttu-id="ec2f8-109">Chaque fois que l’objet est déplacé, le système met automatiquement à jour la partie nom unique des valeurs des objets connus qui sont référencés par l’objet.</span><span class="sxs-lookup"><span data-stu-id="ec2f8-109">Whenever the object is moved, the system automatically updates the Distinguished Name portion of the Well-Known-Objects values that referred to the object.</span></span> <span data-ttu-id="ec2f8-110">Le fichier ntdsapi. h contient les définitions suivantes, qui peuvent être utilisées pour récupérer un objet (les GUID associés à ces objets sont contenus dans ntdsapi. h) :</span><span class="sxs-lookup"><span data-stu-id="ec2f8-110">The file Ntdsapi.h contains the following definitions, which can be used to retrieve an object (the GUIDs that are associated to these objects are contained in Ntdsapi.h):</span></span>

-   <span data-ttu-id="ec2f8-111">\_conteneur d’utilisateurs GUID \_ \_ W</span><span class="sxs-lookup"><span data-stu-id="ec2f8-111">GUID\_USERS\_CONTAINER\_W</span></span>
-   <span data-ttu-id="ec2f8-112">\_conteneur de calculs \_ GUID \_ W</span><span class="sxs-lookup"><span data-stu-id="ec2f8-112">GUID\_COMPUTRS\_CONTAINER\_W</span></span>
-   <span data-ttu-id="ec2f8-113">\_conteneur de systèmes GUID \_ \_ W</span><span class="sxs-lookup"><span data-stu-id="ec2f8-113">GUID\_SYSTEMS\_CONTAINER\_W</span></span>
-   <span data-ttu-id="ec2f8-114">\_conteneur de \_ contrôleurs de domaine GUID \_ \_ W</span><span class="sxs-lookup"><span data-stu-id="ec2f8-114">GUID\_DOMAIN\_CONTROLLERS\_CONTAINER\_W</span></span>
-   <span data-ttu-id="ec2f8-115">conteneur d’infrastructure de GUID \_ \_ \_ W</span><span class="sxs-lookup"><span data-stu-id="ec2f8-115">GUID\_INFRASTRUCTURE\_CONTAINER\_W</span></span>
-   <span data-ttu-id="ec2f8-116">\_conteneur d' \_ objets supprimés GUID \_ \_ W</span><span class="sxs-lookup"><span data-stu-id="ec2f8-116">GUID\_DELETED\_OBJECTS\_CONTAINER\_W</span></span>
-   <span data-ttu-id="ec2f8-117">GUID \_ LOSTANDFOUND \_ conteneur \_ W</span><span class="sxs-lookup"><span data-stu-id="ec2f8-117">GUID\_LOSTANDFOUND\_CONTAINER\_W</span></span>
-   <span data-ttu-id="ec2f8-118">\_conteneur FOREIGNSECURITYPRINCIPALS \_ conteneur \_ W</span><span class="sxs-lookup"><span data-stu-id="ec2f8-118">GUID\_FOREIGNSECURITYPRINCIPALS\_CONTAINER\_W</span></span>
-   <span data-ttu-id="ec2f8-119">\_conteneur de données du programme GUID \_ \_ \_ W</span><span class="sxs-lookup"><span data-stu-id="ec2f8-119">GUID\_PROGRAM\_DATA\_CONTAINER\_W</span></span>
-   <span data-ttu-id="ec2f8-120">GUID \_ de \_ conteneur de données de programme Microsoft \_ \_ \_ W</span><span class="sxs-lookup"><span data-stu-id="ec2f8-120">GUID\_MICROSOFT\_PROGRAM\_DATA\_CONTAINER\_W</span></span>
-   <span data-ttu-id="ec2f8-121">GUID \_ NTDS \_ quotas \_ conteneur \_ W</span><span class="sxs-lookup"><span data-stu-id="ec2f8-121">GUID\_NTDS\_QUOTAS\_CONTAINER\_W</span></span>



| <span data-ttu-id="ec2f8-122">Entrée</span><span class="sxs-lookup"><span data-stu-id="ec2f8-122">Entry</span></span> | <span data-ttu-id="ec2f8-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="ec2f8-123">Value</span></span> |
|-------------------|-------------------------------------------------|
| <span data-ttu-id="ec2f8-124">CN</span><span class="sxs-lookup"><span data-stu-id="ec2f8-124">CN</span></span>                | <span data-ttu-id="ec2f8-125">Objets bien connus</span><span class="sxs-lookup"><span data-stu-id="ec2f8-125">Well-Known-Objects</span></span>                              |
| <span data-ttu-id="ec2f8-126">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="ec2f8-126">Ldap-Display-Name</span></span> | <span data-ttu-id="ec2f8-127">wellKnownObjects</span><span class="sxs-lookup"><span data-stu-id="ec2f8-127">wellKnownObjects</span></span>                                |
| <span data-ttu-id="ec2f8-128">Taille</span><span class="sxs-lookup"><span data-stu-id="ec2f8-128">Size</span></span>              | \-                                              |
| <span data-ttu-id="ec2f8-129">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="ec2f8-129">Update Privilege</span></span>  | <span data-ttu-id="ec2f8-130">Cette valeur est définie par le système.</span><span class="sxs-lookup"><span data-stu-id="ec2f8-130">This value is set by the system.</span></span>                |
| <span data-ttu-id="ec2f8-131">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="ec2f8-131">Update Frequency</span></span>  | <span data-ttu-id="ec2f8-132">Chaque fois que l’un des conteneurs système est déplacé.</span><span class="sxs-lookup"><span data-stu-id="ec2f8-132">Whenever one of the system containers is moved.</span></span> |
| <span data-ttu-id="ec2f8-133">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ec2f8-133">Attribute-Id</span></span>      | <span data-ttu-id="ec2f8-134">1.2.840.113556.1.4.618</span><span class="sxs-lookup"><span data-stu-id="ec2f8-134">1.2.840.113556.1.4.618</span></span>                          |
| <span data-ttu-id="ec2f8-135">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ec2f8-135">System-Id-Guid</span></span>    | <span data-ttu-id="ec2f8-136">05308983-7688-11d1-aded-00c04fd8d5cd</span><span class="sxs-lookup"><span data-stu-id="ec2f8-136">05308983-7688-11d1-aded-00c04fd8d5cd</span></span>            |
| <span data-ttu-id="ec2f8-137">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ec2f8-137">Syntax</span></span>            | [<span data-ttu-id="ec2f8-138">**Object(DN-Binary)**</span><span class="sxs-lookup"><span data-stu-id="ec2f8-138">**Object(DN-Binary)**</span></span>](s-object-dn-binary.md) |



## <a name="implementations"></a><span data-ttu-id="ec2f8-139">Implémentations</span><span class="sxs-lookup"><span data-stu-id="ec2f8-139">Implementations</span></span>

-   [<span data-ttu-id="ec2f8-140">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ec2f8-140">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ec2f8-141">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ec2f8-141">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ec2f8-142">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="ec2f8-142">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="ec2f8-143">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ec2f8-143">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ec2f8-144">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ec2f8-144">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ec2f8-145">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ec2f8-145">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ec2f8-146">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ec2f8-146">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ec2f8-147">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ec2f8-147">Windows 2000 Server</span></span>



| <span data-ttu-id="ec2f8-148">Entrée</span><span class="sxs-lookup"><span data-stu-id="ec2f8-148">Entry</span></span> | <span data-ttu-id="ec2f8-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="ec2f8-149">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ec2f8-150">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ec2f8-150">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ec2f8-151">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec2f8-151">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ec2f8-152">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec2f8-152">System-Only</span></span>            | <span data-ttu-id="ec2f8-153">Vrai</span><span class="sxs-lookup"><span data-stu-id="ec2f8-153">True</span></span>                            |
| <span data-ttu-id="ec2f8-154">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ec2f8-154">Is-Single-Valued</span></span>       | <span data-ttu-id="ec2f8-155">Faux</span><span class="sxs-lookup"><span data-stu-id="ec2f8-155">False</span></span>                           |
| <span data-ttu-id="ec2f8-156">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ec2f8-156">Is Indexed</span></span>             | <span data-ttu-id="ec2f8-157">Faux</span><span class="sxs-lookup"><span data-stu-id="ec2f8-157">False</span></span>                           |
| <span data-ttu-id="ec2f8-158">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ec2f8-158">In Global Catalog</span></span>      | <span data-ttu-id="ec2f8-159">Vrai</span><span class="sxs-lookup"><span data-stu-id="ec2f8-159">True</span></span>                            |
| <span data-ttu-id="ec2f8-160">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ec2f8-160">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec2f8-161">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ec2f8-161">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ec2f8-162">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec2f8-162">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ec2f8-163">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec2f8-163">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ec2f8-164">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec2f8-164">Search-Flags</span></span>           | <span data-ttu-id="ec2f8-165">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec2f8-165">0x00000000</span></span>                      |
| <span data-ttu-id="ec2f8-166">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec2f8-166">System-Flags</span></span>           | <span data-ttu-id="ec2f8-167">0x00000012</span><span class="sxs-lookup"><span data-stu-id="ec2f8-167">0x00000012</span></span>                      |
| <span data-ttu-id="ec2f8-168">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ec2f8-168">Classes used in</span></span>        | [<span data-ttu-id="ec2f8-169">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="ec2f8-169">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ec2f8-170">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ec2f8-170">Windows Server 2003</span></span>



| <span data-ttu-id="ec2f8-171">Entrée</span><span class="sxs-lookup"><span data-stu-id="ec2f8-171">Entry</span></span> | <span data-ttu-id="ec2f8-172">Valeur</span><span class="sxs-lookup"><span data-stu-id="ec2f8-172">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ec2f8-173">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ec2f8-173">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ec2f8-174">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec2f8-174">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ec2f8-175">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec2f8-175">System-Only</span></span>            | <span data-ttu-id="ec2f8-176">Vrai</span><span class="sxs-lookup"><span data-stu-id="ec2f8-176">True</span></span>                            |
| <span data-ttu-id="ec2f8-177">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ec2f8-177">Is-Single-Valued</span></span>       | <span data-ttu-id="ec2f8-178">Faux</span><span class="sxs-lookup"><span data-stu-id="ec2f8-178">False</span></span>                           |
| <span data-ttu-id="ec2f8-179">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ec2f8-179">Is Indexed</span></span>             | <span data-ttu-id="ec2f8-180">Faux</span><span class="sxs-lookup"><span data-stu-id="ec2f8-180">False</span></span>                           |
| <span data-ttu-id="ec2f8-181">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ec2f8-181">In Global Catalog</span></span>      | <span data-ttu-id="ec2f8-182">Vrai</span><span class="sxs-lookup"><span data-stu-id="ec2f8-182">True</span></span>                            |
| <span data-ttu-id="ec2f8-183">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ec2f8-183">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec2f8-184">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ec2f8-184">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ec2f8-185">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec2f8-185">Range-Lower</span></span>            | <span data-ttu-id="ec2f8-186">16</span><span class="sxs-lookup"><span data-stu-id="ec2f8-186">16</span></span>                              |
| <span data-ttu-id="ec2f8-187">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec2f8-187">Range-Upper</span></span>            | <span data-ttu-id="ec2f8-188">16</span><span class="sxs-lookup"><span data-stu-id="ec2f8-188">16</span></span>                              |
| <span data-ttu-id="ec2f8-189">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec2f8-189">Search-Flags</span></span>           | <span data-ttu-id="ec2f8-190">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec2f8-190">0x00000000</span></span>                      |
| <span data-ttu-id="ec2f8-191">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec2f8-191">System-Flags</span></span>           | <span data-ttu-id="ec2f8-192">0x00000012</span><span class="sxs-lookup"><span data-stu-id="ec2f8-192">0x00000012</span></span>                      |
| <span data-ttu-id="ec2f8-193">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ec2f8-193">Classes used in</span></span>        | [<span data-ttu-id="ec2f8-194">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="ec2f8-194">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="ec2f8-195">ADAM</span><span class="sxs-lookup"><span data-stu-id="ec2f8-195">ADAM</span></span>



| <span data-ttu-id="ec2f8-196">Entrée</span><span class="sxs-lookup"><span data-stu-id="ec2f8-196">Entry</span></span> | <span data-ttu-id="ec2f8-197">Valeur</span><span class="sxs-lookup"><span data-stu-id="ec2f8-197">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ec2f8-198">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ec2f8-198">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ec2f8-199">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec2f8-199">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ec2f8-200">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec2f8-200">System-Only</span></span>            | <span data-ttu-id="ec2f8-201">Vrai</span><span class="sxs-lookup"><span data-stu-id="ec2f8-201">True</span></span>                            |
| <span data-ttu-id="ec2f8-202">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ec2f8-202">Is-Single-Valued</span></span>       | <span data-ttu-id="ec2f8-203">Faux</span><span class="sxs-lookup"><span data-stu-id="ec2f8-203">False</span></span>                           |
| <span data-ttu-id="ec2f8-204">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ec2f8-204">Is Indexed</span></span>             | <span data-ttu-id="ec2f8-205">Faux</span><span class="sxs-lookup"><span data-stu-id="ec2f8-205">False</span></span>                           |
| <span data-ttu-id="ec2f8-206">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ec2f8-206">In Global Catalog</span></span>      | <span data-ttu-id="ec2f8-207">Vrai</span><span class="sxs-lookup"><span data-stu-id="ec2f8-207">True</span></span>                            |
| <span data-ttu-id="ec2f8-208">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ec2f8-208">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec2f8-209">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ec2f8-209">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ec2f8-210">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec2f8-210">Range-Lower</span></span>            | <span data-ttu-id="ec2f8-211">16</span><span class="sxs-lookup"><span data-stu-id="ec2f8-211">16</span></span>                              |
| <span data-ttu-id="ec2f8-212">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec2f8-212">Range-Upper</span></span>            | <span data-ttu-id="ec2f8-213">16</span><span class="sxs-lookup"><span data-stu-id="ec2f8-213">16</span></span>                              |
| <span data-ttu-id="ec2f8-214">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec2f8-214">Search-Flags</span></span>           | <span data-ttu-id="ec2f8-215">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec2f8-215">0x00000000</span></span>                      |
| <span data-ttu-id="ec2f8-216">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec2f8-216">System-Flags</span></span>           | <span data-ttu-id="ec2f8-217">0x00000012</span><span class="sxs-lookup"><span data-stu-id="ec2f8-217">0x00000012</span></span>                      |
| <span data-ttu-id="ec2f8-218">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ec2f8-218">Classes used in</span></span>        | [<span data-ttu-id="ec2f8-219">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="ec2f8-219">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ec2f8-220">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ec2f8-220">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ec2f8-221">Entrée</span><span class="sxs-lookup"><span data-stu-id="ec2f8-221">Entry</span></span> | <span data-ttu-id="ec2f8-222">Valeur</span><span class="sxs-lookup"><span data-stu-id="ec2f8-222">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ec2f8-223">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ec2f8-223">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ec2f8-224">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec2f8-224">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ec2f8-225">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec2f8-225">System-Only</span></span>            | <span data-ttu-id="ec2f8-226">Vrai</span><span class="sxs-lookup"><span data-stu-id="ec2f8-226">True</span></span>                            |
| <span data-ttu-id="ec2f8-227">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ec2f8-227">Is-Single-Valued</span></span>       | <span data-ttu-id="ec2f8-228">Faux</span><span class="sxs-lookup"><span data-stu-id="ec2f8-228">False</span></span>                           |
| <span data-ttu-id="ec2f8-229">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ec2f8-229">Is Indexed</span></span>             | <span data-ttu-id="ec2f8-230">Faux</span><span class="sxs-lookup"><span data-stu-id="ec2f8-230">False</span></span>                           |
| <span data-ttu-id="ec2f8-231">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ec2f8-231">In Global Catalog</span></span>      | <span data-ttu-id="ec2f8-232">Vrai</span><span class="sxs-lookup"><span data-stu-id="ec2f8-232">True</span></span>                            |
| <span data-ttu-id="ec2f8-233">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ec2f8-233">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec2f8-234">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ec2f8-234">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ec2f8-235">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec2f8-235">Range-Lower</span></span>            | <span data-ttu-id="ec2f8-236">16</span><span class="sxs-lookup"><span data-stu-id="ec2f8-236">16</span></span>                              |
| <span data-ttu-id="ec2f8-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec2f8-237">Range-Upper</span></span>            | <span data-ttu-id="ec2f8-238">16</span><span class="sxs-lookup"><span data-stu-id="ec2f8-238">16</span></span>                              |
| <span data-ttu-id="ec2f8-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec2f8-239">Search-Flags</span></span>           | <span data-ttu-id="ec2f8-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec2f8-240">0x00000000</span></span>                      |
| <span data-ttu-id="ec2f8-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec2f8-241">System-Flags</span></span>           | <span data-ttu-id="ec2f8-242">0x00000012</span><span class="sxs-lookup"><span data-stu-id="ec2f8-242">0x00000012</span></span>                      |
| <span data-ttu-id="ec2f8-243">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ec2f8-243">Classes used in</span></span>        | [<span data-ttu-id="ec2f8-244">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="ec2f8-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ec2f8-245">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ec2f8-245">Windows Server 2008</span></span>



| <span data-ttu-id="ec2f8-246">Entrée</span><span class="sxs-lookup"><span data-stu-id="ec2f8-246">Entry</span></span> | <span data-ttu-id="ec2f8-247">Valeur</span><span class="sxs-lookup"><span data-stu-id="ec2f8-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ec2f8-248">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ec2f8-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ec2f8-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec2f8-249">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ec2f8-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec2f8-250">System-Only</span></span>            | <span data-ttu-id="ec2f8-251">Vrai</span><span class="sxs-lookup"><span data-stu-id="ec2f8-251">True</span></span>                            |
| <span data-ttu-id="ec2f8-252">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ec2f8-252">Is-Single-Valued</span></span>       | <span data-ttu-id="ec2f8-253">Faux</span><span class="sxs-lookup"><span data-stu-id="ec2f8-253">False</span></span>                           |
| <span data-ttu-id="ec2f8-254">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ec2f8-254">Is Indexed</span></span>             | <span data-ttu-id="ec2f8-255">Faux</span><span class="sxs-lookup"><span data-stu-id="ec2f8-255">False</span></span>                           |
| <span data-ttu-id="ec2f8-256">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ec2f8-256">In Global Catalog</span></span>      | <span data-ttu-id="ec2f8-257">Vrai</span><span class="sxs-lookup"><span data-stu-id="ec2f8-257">True</span></span>                            |
| <span data-ttu-id="ec2f8-258">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ec2f8-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec2f8-259">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ec2f8-259">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ec2f8-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec2f8-260">Range-Lower</span></span>            | <span data-ttu-id="ec2f8-261">16</span><span class="sxs-lookup"><span data-stu-id="ec2f8-261">16</span></span>                              |
| <span data-ttu-id="ec2f8-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec2f8-262">Range-Upper</span></span>            | <span data-ttu-id="ec2f8-263">16</span><span class="sxs-lookup"><span data-stu-id="ec2f8-263">16</span></span>                              |
| <span data-ttu-id="ec2f8-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec2f8-264">Search-Flags</span></span>           | <span data-ttu-id="ec2f8-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec2f8-265">0x00000000</span></span>                      |
| <span data-ttu-id="ec2f8-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec2f8-266">System-Flags</span></span>           | <span data-ttu-id="ec2f8-267">0x00000012</span><span class="sxs-lookup"><span data-stu-id="ec2f8-267">0x00000012</span></span>                      |
| <span data-ttu-id="ec2f8-268">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ec2f8-268">Classes used in</span></span>        | [<span data-ttu-id="ec2f8-269">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="ec2f8-269">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ec2f8-270">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ec2f8-270">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ec2f8-271">Entrée</span><span class="sxs-lookup"><span data-stu-id="ec2f8-271">Entry</span></span> | <span data-ttu-id="ec2f8-272">Valeur</span><span class="sxs-lookup"><span data-stu-id="ec2f8-272">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ec2f8-273">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ec2f8-273">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ec2f8-274">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec2f8-274">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ec2f8-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec2f8-275">System-Only</span></span>            | <span data-ttu-id="ec2f8-276">Vrai</span><span class="sxs-lookup"><span data-stu-id="ec2f8-276">True</span></span>                            |
| <span data-ttu-id="ec2f8-277">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ec2f8-277">Is-Single-Valued</span></span>       | <span data-ttu-id="ec2f8-278">Faux</span><span class="sxs-lookup"><span data-stu-id="ec2f8-278">False</span></span>                           |
| <span data-ttu-id="ec2f8-279">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ec2f8-279">Is Indexed</span></span>             | <span data-ttu-id="ec2f8-280">Faux</span><span class="sxs-lookup"><span data-stu-id="ec2f8-280">False</span></span>                           |
| <span data-ttu-id="ec2f8-281">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ec2f8-281">In Global Catalog</span></span>      | <span data-ttu-id="ec2f8-282">Vrai</span><span class="sxs-lookup"><span data-stu-id="ec2f8-282">True</span></span>                            |
| <span data-ttu-id="ec2f8-283">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ec2f8-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec2f8-284">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ec2f8-284">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ec2f8-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec2f8-285">Range-Lower</span></span>            | <span data-ttu-id="ec2f8-286">16</span><span class="sxs-lookup"><span data-stu-id="ec2f8-286">16</span></span>                              |
| <span data-ttu-id="ec2f8-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec2f8-287">Range-Upper</span></span>            | <span data-ttu-id="ec2f8-288">16</span><span class="sxs-lookup"><span data-stu-id="ec2f8-288">16</span></span>                              |
| <span data-ttu-id="ec2f8-289">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec2f8-289">Search-Flags</span></span>           | <span data-ttu-id="ec2f8-290">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec2f8-290">0x00000000</span></span>                      |
| <span data-ttu-id="ec2f8-291">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec2f8-291">System-Flags</span></span>           | <span data-ttu-id="ec2f8-292">0x00000012</span><span class="sxs-lookup"><span data-stu-id="ec2f8-292">0x00000012</span></span>                      |
| <span data-ttu-id="ec2f8-293">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ec2f8-293">Classes used in</span></span>        | [<span data-ttu-id="ec2f8-294">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="ec2f8-294">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ec2f8-295">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ec2f8-295">Windows Server 2012</span></span>



| <span data-ttu-id="ec2f8-296">Entrée</span><span class="sxs-lookup"><span data-stu-id="ec2f8-296">Entry</span></span> | <span data-ttu-id="ec2f8-297">Valeur</span><span class="sxs-lookup"><span data-stu-id="ec2f8-297">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ec2f8-298">ID de lien</span><span class="sxs-lookup"><span data-stu-id="ec2f8-298">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ec2f8-299">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec2f8-299">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ec2f8-300">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec2f8-300">System-Only</span></span>            | <span data-ttu-id="ec2f8-301">Vrai</span><span class="sxs-lookup"><span data-stu-id="ec2f8-301">True</span></span>                            |
| <span data-ttu-id="ec2f8-302">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="ec2f8-302">Is-Single-Valued</span></span>       | <span data-ttu-id="ec2f8-303">Faux</span><span class="sxs-lookup"><span data-stu-id="ec2f8-303">False</span></span>                           |
| <span data-ttu-id="ec2f8-304">Est indexé</span><span class="sxs-lookup"><span data-stu-id="ec2f8-304">Is Indexed</span></span>             | <span data-ttu-id="ec2f8-305">Faux</span><span class="sxs-lookup"><span data-stu-id="ec2f8-305">False</span></span>                           |
| <span data-ttu-id="ec2f8-306">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="ec2f8-306">In Global Catalog</span></span>      | <span data-ttu-id="ec2f8-307">Vrai</span><span class="sxs-lookup"><span data-stu-id="ec2f8-307">True</span></span>                            |
| <span data-ttu-id="ec2f8-308">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="ec2f8-308">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec2f8-309">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="ec2f8-309">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ec2f8-310">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec2f8-310">Range-Lower</span></span>            | <span data-ttu-id="ec2f8-311">16</span><span class="sxs-lookup"><span data-stu-id="ec2f8-311">16</span></span>                              |
| <span data-ttu-id="ec2f8-312">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec2f8-312">Range-Upper</span></span>            | <span data-ttu-id="ec2f8-313">16</span><span class="sxs-lookup"><span data-stu-id="ec2f8-313">16</span></span>                              |
| <span data-ttu-id="ec2f8-314">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec2f8-314">Search-Flags</span></span>           | <span data-ttu-id="ec2f8-315">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec2f8-315">0x00000000</span></span>                      |
| <span data-ttu-id="ec2f8-316">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec2f8-316">System-Flags</span></span>           | <span data-ttu-id="ec2f8-317">0x00000012</span><span class="sxs-lookup"><span data-stu-id="ec2f8-317">0x00000012</span></span>                      |
| <span data-ttu-id="ec2f8-318">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="ec2f8-318">Classes used in</span></span>        | [<span data-ttu-id="ec2f8-319">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="ec2f8-319">**Top**</span></span>](c-top.md)<br/> |



 

 





