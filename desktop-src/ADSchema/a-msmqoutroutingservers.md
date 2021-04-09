---
title: MSMQ-out-Routing-attribut serveurs
description: Les liens DN vers les serveurs de routage MSMQ par le biais desquels tout le trafic sortant de cet ordinateur doit être routé.
ms.assetid: 169558e4-d2a6-4555-bc5f-7e6a89e51789
ms.tgt_platform: multiple
keywords:
- MSMQ-out-Routing-attribut des serveurs, schéma AD
- Schéma AD de l’attribut mSMQOutRoutingServers
topic_type:
- apiref
api_name:
- MSMQ-Out-Routing-Servers
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfc2265b2d809b7a73cd19faace87473552471a3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845090"
---
# <a name="msmq-out-routing-servers-attribute"></a><span data-ttu-id="f5f8b-105">MSMQ-out-Routing-attribut serveurs</span><span class="sxs-lookup"><span data-stu-id="f5f8b-105">MSMQ-Out-Routing-Servers attribute</span></span>

<span data-ttu-id="f5f8b-106">Les liens DN vers les serveurs de routage MSMQ par le biais desquels tout le trafic sortant de cet ordinateur doit être routé.</span><span class="sxs-lookup"><span data-stu-id="f5f8b-106">DN links to MSMQ routing servers through which all outgoing traffic for this computer should be routed.</span></span>



| <span data-ttu-id="f5f8b-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="f5f8b-107">Entry</span></span> | <span data-ttu-id="f5f8b-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="f5f8b-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="f5f8b-109">CN</span><span class="sxs-lookup"><span data-stu-id="f5f8b-109">CN</span></span>                | <span data-ttu-id="f5f8b-110">MSMQ-out-Routing-serveurs</span><span class="sxs-lookup"><span data-stu-id="f5f8b-110">MSMQ-Out-Routing-Servers</span></span>                |
| <span data-ttu-id="f5f8b-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f5f8b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="f5f8b-112">mSMQOutRoutingServers</span><span class="sxs-lookup"><span data-stu-id="f5f8b-112">mSMQOutRoutingServers</span></span>                   |
| <span data-ttu-id="f5f8b-113">Taille</span><span class="sxs-lookup"><span data-stu-id="f5f8b-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="f5f8b-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="f5f8b-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="f5f8b-115">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="f5f8b-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="f5f8b-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f5f8b-116">Attribute-Id</span></span>      | <span data-ttu-id="f5f8b-117">1.2.840.113556.1.4.928</span><span class="sxs-lookup"><span data-stu-id="f5f8b-117">1.2.840.113556.1.4.928</span></span>                  |
| <span data-ttu-id="f5f8b-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f5f8b-118">System-Id-Guid</span></span>    | <span data-ttu-id="f5f8b-119">9a0dc32b-c100-11d1-bbc5-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="f5f8b-119">9a0dc32b-c100-11d1-bbc5-0080c76670c0</span></span>    |
| <span data-ttu-id="f5f8b-120">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f5f8b-120">Syntax</span></span>            | [<span data-ttu-id="f5f8b-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="f5f8b-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="f5f8b-122">Implémentations</span><span class="sxs-lookup"><span data-stu-id="f5f8b-122">Implementations</span></span>

-   [<span data-ttu-id="f5f8b-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f5f8b-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f5f8b-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f5f8b-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f5f8b-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f5f8b-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f5f8b-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f5f8b-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f5f8b-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f5f8b-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f5f8b-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f5f8b-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f5f8b-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f5f8b-129">Windows 2000 Server</span></span>



| <span data-ttu-id="f5f8b-130">Entrée</span><span class="sxs-lookup"><span data-stu-id="f5f8b-130">Entry</span></span> | <span data-ttu-id="f5f8b-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="f5f8b-131">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="f5f8b-132">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f5f8b-132">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="f5f8b-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f5f8b-133">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="f5f8b-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="f5f8b-134">System-Only</span></span>            | <span data-ttu-id="f5f8b-135">Faux</span><span class="sxs-lookup"><span data-stu-id="f5f8b-135">False</span></span>                                                        |
| <span data-ttu-id="f5f8b-136">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f5f8b-136">Is-Single-Valued</span></span>       | <span data-ttu-id="f5f8b-137">Faux</span><span class="sxs-lookup"><span data-stu-id="f5f8b-137">False</span></span>                                                        |
| <span data-ttu-id="f5f8b-138">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f5f8b-138">Is Indexed</span></span>             | <span data-ttu-id="f5f8b-139">Faux</span><span class="sxs-lookup"><span data-stu-id="f5f8b-139">False</span></span>                                                        |
| <span data-ttu-id="f5f8b-140">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f5f8b-140">In Global Catalog</span></span>      | <span data-ttu-id="f5f8b-141">Vrai</span><span class="sxs-lookup"><span data-stu-id="f5f8b-141">True</span></span>                                                         |
| <span data-ttu-id="f5f8b-142">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f5f8b-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="f5f8b-143">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f5f8b-143">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="f5f8b-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f5f8b-144">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="f5f8b-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f5f8b-145">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="f5f8b-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f5f8b-146">Search-Flags</span></span>           | <span data-ttu-id="f5f8b-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f5f8b-147">0x00000000</span></span>                                                   |
| <span data-ttu-id="f5f8b-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f5f8b-148">System-Flags</span></span>           | <span data-ttu-id="f5f8b-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f5f8b-149">0x00000010</span></span>                                                   |
| <span data-ttu-id="f5f8b-150">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f5f8b-150">Classes used in</span></span>        | [<span data-ttu-id="f5f8b-151">**Configuration MSMQ**</span><span class="sxs-lookup"><span data-stu-id="f5f8b-151">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f5f8b-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f5f8b-152">Windows Server 2003</span></span>



| <span data-ttu-id="f5f8b-153">Entrée</span><span class="sxs-lookup"><span data-stu-id="f5f8b-153">Entry</span></span> | <span data-ttu-id="f5f8b-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="f5f8b-154">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="f5f8b-155">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f5f8b-155">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="f5f8b-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f5f8b-156">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="f5f8b-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="f5f8b-157">System-Only</span></span>            | <span data-ttu-id="f5f8b-158">Faux</span><span class="sxs-lookup"><span data-stu-id="f5f8b-158">False</span></span>                                                        |
| <span data-ttu-id="f5f8b-159">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f5f8b-159">Is-Single-Valued</span></span>       | <span data-ttu-id="f5f8b-160">Faux</span><span class="sxs-lookup"><span data-stu-id="f5f8b-160">False</span></span>                                                        |
| <span data-ttu-id="f5f8b-161">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f5f8b-161">Is Indexed</span></span>             | <span data-ttu-id="f5f8b-162">Faux</span><span class="sxs-lookup"><span data-stu-id="f5f8b-162">False</span></span>                                                        |
| <span data-ttu-id="f5f8b-163">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f5f8b-163">In Global Catalog</span></span>      | <span data-ttu-id="f5f8b-164">Vrai</span><span class="sxs-lookup"><span data-stu-id="f5f8b-164">True</span></span>                                                         |
| <span data-ttu-id="f5f8b-165">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f5f8b-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="f5f8b-166">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f5f8b-166">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="f5f8b-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f5f8b-167">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="f5f8b-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f5f8b-168">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="f5f8b-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f5f8b-169">Search-Flags</span></span>           | <span data-ttu-id="f5f8b-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f5f8b-170">0x00000000</span></span>                                                   |
| <span data-ttu-id="f5f8b-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f5f8b-171">System-Flags</span></span>           | <span data-ttu-id="f5f8b-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f5f8b-172">0x00000010</span></span>                                                   |
| <span data-ttu-id="f5f8b-173">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f5f8b-173">Classes used in</span></span>        | [<span data-ttu-id="f5f8b-174">**Configuration MSMQ**</span><span class="sxs-lookup"><span data-stu-id="f5f8b-174">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f5f8b-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f5f8b-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f5f8b-176">Entrée</span><span class="sxs-lookup"><span data-stu-id="f5f8b-176">Entry</span></span> | <span data-ttu-id="f5f8b-177">Valeur</span><span class="sxs-lookup"><span data-stu-id="f5f8b-177">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="f5f8b-178">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f5f8b-178">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="f5f8b-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f5f8b-179">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="f5f8b-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="f5f8b-180">System-Only</span></span>            | <span data-ttu-id="f5f8b-181">Faux</span><span class="sxs-lookup"><span data-stu-id="f5f8b-181">False</span></span>                                                        |
| <span data-ttu-id="f5f8b-182">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f5f8b-182">Is-Single-Valued</span></span>       | <span data-ttu-id="f5f8b-183">Faux</span><span class="sxs-lookup"><span data-stu-id="f5f8b-183">False</span></span>                                                        |
| <span data-ttu-id="f5f8b-184">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f5f8b-184">Is Indexed</span></span>             | <span data-ttu-id="f5f8b-185">Faux</span><span class="sxs-lookup"><span data-stu-id="f5f8b-185">False</span></span>                                                        |
| <span data-ttu-id="f5f8b-186">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f5f8b-186">In Global Catalog</span></span>      | <span data-ttu-id="f5f8b-187">Vrai</span><span class="sxs-lookup"><span data-stu-id="f5f8b-187">True</span></span>                                                         |
| <span data-ttu-id="f5f8b-188">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f5f8b-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="f5f8b-189">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f5f8b-189">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="f5f8b-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f5f8b-190">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="f5f8b-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f5f8b-191">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="f5f8b-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f5f8b-192">Search-Flags</span></span>           | <span data-ttu-id="f5f8b-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f5f8b-193">0x00000000</span></span>                                                   |
| <span data-ttu-id="f5f8b-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f5f8b-194">System-Flags</span></span>           | <span data-ttu-id="f5f8b-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f5f8b-195">0x00000010</span></span>                                                   |
| <span data-ttu-id="f5f8b-196">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f5f8b-196">Classes used in</span></span>        | [<span data-ttu-id="f5f8b-197">**Configuration MSMQ**</span><span class="sxs-lookup"><span data-stu-id="f5f8b-197">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f5f8b-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f5f8b-198">Windows Server 2008</span></span>



| <span data-ttu-id="f5f8b-199">Entrée</span><span class="sxs-lookup"><span data-stu-id="f5f8b-199">Entry</span></span> | <span data-ttu-id="f5f8b-200">Valeur</span><span class="sxs-lookup"><span data-stu-id="f5f8b-200">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="f5f8b-201">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f5f8b-201">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="f5f8b-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f5f8b-202">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="f5f8b-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="f5f8b-203">System-Only</span></span>            | <span data-ttu-id="f5f8b-204">Faux</span><span class="sxs-lookup"><span data-stu-id="f5f8b-204">False</span></span>                                                        |
| <span data-ttu-id="f5f8b-205">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f5f8b-205">Is-Single-Valued</span></span>       | <span data-ttu-id="f5f8b-206">Faux</span><span class="sxs-lookup"><span data-stu-id="f5f8b-206">False</span></span>                                                        |
| <span data-ttu-id="f5f8b-207">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f5f8b-207">Is Indexed</span></span>             | <span data-ttu-id="f5f8b-208">Faux</span><span class="sxs-lookup"><span data-stu-id="f5f8b-208">False</span></span>                                                        |
| <span data-ttu-id="f5f8b-209">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f5f8b-209">In Global Catalog</span></span>      | <span data-ttu-id="f5f8b-210">Vrai</span><span class="sxs-lookup"><span data-stu-id="f5f8b-210">True</span></span>                                                         |
| <span data-ttu-id="f5f8b-211">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f5f8b-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="f5f8b-212">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f5f8b-212">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="f5f8b-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f5f8b-213">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="f5f8b-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f5f8b-214">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="f5f8b-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f5f8b-215">Search-Flags</span></span>           | <span data-ttu-id="f5f8b-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f5f8b-216">0x00000000</span></span>                                                   |
| <span data-ttu-id="f5f8b-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f5f8b-217">System-Flags</span></span>           | <span data-ttu-id="f5f8b-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f5f8b-218">0x00000010</span></span>                                                   |
| <span data-ttu-id="f5f8b-219">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f5f8b-219">Classes used in</span></span>        | [<span data-ttu-id="f5f8b-220">**Configuration MSMQ**</span><span class="sxs-lookup"><span data-stu-id="f5f8b-220">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f5f8b-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f5f8b-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f5f8b-222">Entrée</span><span class="sxs-lookup"><span data-stu-id="f5f8b-222">Entry</span></span> | <span data-ttu-id="f5f8b-223">Valeur</span><span class="sxs-lookup"><span data-stu-id="f5f8b-223">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="f5f8b-224">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f5f8b-224">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="f5f8b-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f5f8b-225">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="f5f8b-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="f5f8b-226">System-Only</span></span>            | <span data-ttu-id="f5f8b-227">Faux</span><span class="sxs-lookup"><span data-stu-id="f5f8b-227">False</span></span>                                                        |
| <span data-ttu-id="f5f8b-228">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f5f8b-228">Is-Single-Valued</span></span>       | <span data-ttu-id="f5f8b-229">Faux</span><span class="sxs-lookup"><span data-stu-id="f5f8b-229">False</span></span>                                                        |
| <span data-ttu-id="f5f8b-230">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f5f8b-230">Is Indexed</span></span>             | <span data-ttu-id="f5f8b-231">Faux</span><span class="sxs-lookup"><span data-stu-id="f5f8b-231">False</span></span>                                                        |
| <span data-ttu-id="f5f8b-232">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f5f8b-232">In Global Catalog</span></span>      | <span data-ttu-id="f5f8b-233">Vrai</span><span class="sxs-lookup"><span data-stu-id="f5f8b-233">True</span></span>                                                         |
| <span data-ttu-id="f5f8b-234">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f5f8b-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="f5f8b-235">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f5f8b-235">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="f5f8b-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f5f8b-236">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="f5f8b-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f5f8b-237">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="f5f8b-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f5f8b-238">Search-Flags</span></span>           | <span data-ttu-id="f5f8b-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f5f8b-239">0x00000000</span></span>                                                   |
| <span data-ttu-id="f5f8b-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f5f8b-240">System-Flags</span></span>           | <span data-ttu-id="f5f8b-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f5f8b-241">0x00000010</span></span>                                                   |
| <span data-ttu-id="f5f8b-242">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f5f8b-242">Classes used in</span></span>        | [<span data-ttu-id="f5f8b-243">**Configuration MSMQ**</span><span class="sxs-lookup"><span data-stu-id="f5f8b-243">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f5f8b-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f5f8b-244">Windows Server 2012</span></span>



| <span data-ttu-id="f5f8b-245">Entrée</span><span class="sxs-lookup"><span data-stu-id="f5f8b-245">Entry</span></span> | <span data-ttu-id="f5f8b-246">Valeur</span><span class="sxs-lookup"><span data-stu-id="f5f8b-246">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="f5f8b-247">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f5f8b-247">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="f5f8b-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f5f8b-248">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="f5f8b-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="f5f8b-249">System-Only</span></span>            | <span data-ttu-id="f5f8b-250">Faux</span><span class="sxs-lookup"><span data-stu-id="f5f8b-250">False</span></span>                                                        |
| <span data-ttu-id="f5f8b-251">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f5f8b-251">Is-Single-Valued</span></span>       | <span data-ttu-id="f5f8b-252">Faux</span><span class="sxs-lookup"><span data-stu-id="f5f8b-252">False</span></span>                                                        |
| <span data-ttu-id="f5f8b-253">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f5f8b-253">Is Indexed</span></span>             | <span data-ttu-id="f5f8b-254">Faux</span><span class="sxs-lookup"><span data-stu-id="f5f8b-254">False</span></span>                                                        |
| <span data-ttu-id="f5f8b-255">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f5f8b-255">In Global Catalog</span></span>      | <span data-ttu-id="f5f8b-256">Vrai</span><span class="sxs-lookup"><span data-stu-id="f5f8b-256">True</span></span>                                                         |
| <span data-ttu-id="f5f8b-257">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f5f8b-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="f5f8b-258">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f5f8b-258">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="f5f8b-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f5f8b-259">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="f5f8b-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f5f8b-260">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="f5f8b-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f5f8b-261">Search-Flags</span></span>           | <span data-ttu-id="f5f8b-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f5f8b-262">0x00000000</span></span>                                                   |
| <span data-ttu-id="f5f8b-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f5f8b-263">System-Flags</span></span>           | <span data-ttu-id="f5f8b-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f5f8b-264">0x00000010</span></span>                                                   |
| <span data-ttu-id="f5f8b-265">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f5f8b-265">Classes used in</span></span>        | [<span data-ttu-id="f5f8b-266">**Configuration MSMQ**</span><span class="sxs-lookup"><span data-stu-id="f5f8b-266">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



 

 





