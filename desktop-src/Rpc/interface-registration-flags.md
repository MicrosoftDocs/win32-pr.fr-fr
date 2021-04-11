---
title: Indicateurs d’inscription de l’interface (rpcdce. h)
description: Les constantes suivantes sont utilisées dans le paramètre flags des fonctions RpcServerRegisterIf2 et RpcServerRegisterIfEx.
ms.assetid: 387311c0-13df-4497-a0ac-ce6aec0e726c
topic_type:
- apiref
api_name:
- RPC_IF_ALLOW_CALLBACKS_WITH_NO_AUTH
- RPC_IF_ALLOW_LOCAL_ONLY
- RPC_IF_AUTOLISTEN
- RPC_IF_OLE
- RPC_IF_ALLOW_UNKNOWN_AUTHORITY
- RPC_IF_ALLOW_SECURE_ONLY
- RPC_IF_SEC_NO_CACHE
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8af938038d2bc7000d80268fb4cb00941f6b282b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105700"
---
# <a name="interface-registration-flags"></a><span data-ttu-id="aff8c-103">Indicateurs d’inscription de l’interface</span><span class="sxs-lookup"><span data-stu-id="aff8c-103">Interface Registration Flags</span></span>

<span data-ttu-id="aff8c-104">Les constantes suivantes sont utilisées dans le paramètre *Flags* des fonctions [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) et [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) .</span><span class="sxs-lookup"><span data-stu-id="aff8c-104">The following constants are used in the *Flags* parameter of the [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) and [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) functions.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="aff8c-105">Constante</span><span class="sxs-lookup"><span data-stu-id="aff8c-105">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="aff8c-106">Description</span><span class="sxs-lookup"><span data-stu-id="aff8c-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="0"></span><dl> <span data-ttu-id="aff8c-107"><dt><strong>entre</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="aff8c-107"><dt><strong>0</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="aff8c-108">Sémantique d’interface standard.</span><span class="sxs-lookup"><span data-stu-id="aff8c-108">Standard interface semantics.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="RPC_IF_ALLOW_CALLBACKS_WITH_NO_AUTH"></span><span id="rpc_if_allow_callbacks_with_no_auth"></span><dl> <span data-ttu-id="aff8c-109"><dt><strong>RPC_IF_ALLOW_CALLBACKS_WITH_NO_AUTH</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="aff8c-109"><dt><strong>RPC_IF_ALLOW_CALLBACKS_WITH_NO_AUTH</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="aff8c-110">Lorsque cet indicateur d’interface est inscrit, le runtime RPC appelle le rappel de sécurité inscrit pour tous les appels, quelle que soit l’identité, la séquence de protocole ou le niveau d’authentification du client.</span><span class="sxs-lookup"><span data-stu-id="aff8c-110">When this interface flag is registered, the RPC runtime invokes the registered security callback for all calls, regardless of identity, protocol sequence, or authentication level of the client.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="aff8c-111">Cet indicateur est disponible à partir de Windows XP avec SP2 et de Windows Server 2003 avec SP1.</span><span class="sxs-lookup"><span data-stu-id="aff8c-111">This flag is available starting with Windows XP with SP2 and Windows Server 2003 with SP1.</span></span> <span data-ttu-id="aff8c-112">Lorsque cet indicateur n’est pas défini, RPC filtre automatiquement tous les appels non authentifiés avant qu’ils n’atteignent le rappel de sécurité.</span><span class="sxs-lookup"><span data-stu-id="aff8c-112">When this flag is not set, RPC automatically filters all unauthenticated calls before they reach the security callback.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="RPC_IF_ALLOW_LOCAL_ONLY"></span><span id="rpc_if_allow_local_only"></span><dl> <span data-ttu-id="aff8c-113"><dt><strong>RPC_IF_ALLOW_LOCAL_ONLY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="aff8c-113"><dt><strong>RPC_IF_ALLOW_LOCAL_ONLY</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="aff8c-114">Lorsque cet indicateur d’interface est inscrit, le runtime RPC rejette les appels effectués par les clients distants.</span><span class="sxs-lookup"><span data-stu-id="aff8c-114">When this interface flag is registered, the RPC runtime rejects calls made by remote clients.</span></span> <span data-ttu-id="aff8c-115">Tous les appels locaux à l’aide de séquences de protocole ncadg_ \* et ncacn_ \* sont également rejetés, à l’exception de ncacn_np.</span><span class="sxs-lookup"><span data-stu-id="aff8c-115">All local calls using ncadg_\* and ncacn_\* protocol sequences are also rejected, with the exception of ncacn_np.</span></span> <span data-ttu-id="aff8c-116">RPC autorise les appels de ncacn_NP uniquement si l’appel n’est pas fourni par SRV.</span><span class="sxs-lookup"><span data-stu-id="aff8c-116">RPC allows ncacn_NP calls only if the call does not come from SRV.</span></span> <span data-ttu-id="aff8c-117">Les appels de Ncalrpc sont toujours traités.</span><span class="sxs-lookup"><span data-stu-id="aff8c-117">Calls from ncalrpc are always processed.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="aff8c-118">Cet indicateur est disponible à partir de Windows XP avec SP2 et de Windows Server 2003 avec SP1.</span><span class="sxs-lookup"><span data-stu-id="aff8c-118">This flag is available starting with Windows XP with SP2 and Windows Server 2003 with SP1.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="RPC_IF_AUTOLISTEN"></span><span id="rpc_if_autolisten"></span><dl> <span data-ttu-id="aff8c-119"><dt><strong>RPC_IF_AUTOLISTEN</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="aff8c-119"><dt><strong>RPC_IF_AUTOLISTEN</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="aff8c-120">Il s’agit d’une interface d' <strong>écoute automatique</strong> .</span><span class="sxs-lookup"><span data-stu-id="aff8c-120">This is an <strong>auto-listen</strong> interface.</span></span> <span data-ttu-id="aff8c-121">Le temps d’exécution commence à écouter les appels dès que la première interface autolistn est inscrite et cesse d’écouter lorsque la dernière interface autolistn est désinscrite.</span><span class="sxs-lookup"><span data-stu-id="aff8c-121">The run time begins listening for calls as soon as the first autolisten interface is registered, and stops listening when the last autolisten interface is unregistered.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="RPC_IF_OLE"></span><span id="rpc_if_ole"></span><dl> <span data-ttu-id="aff8c-122"><dt><strong>RPC_IF_OLE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="aff8c-122"><dt><strong>RPC_IF_OLE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="aff8c-123">Réservé pour OLE.</span><span class="sxs-lookup"><span data-stu-id="aff8c-123">Reserved for OLE.</span></span> <span data-ttu-id="aff8c-124">N’utilisez pas cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="aff8c-124">Do not use this flag.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="RPC_IF_ALLOW_UNKNOWN_AUTHORITY"></span><span id="rpc_if_allow_unknown_authority"></span><dl> <span data-ttu-id="aff8c-125"><dt><strong>RPC_IF_ALLOW_UNKNOWN_AUTHORITY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="aff8c-125"><dt><strong>RPC_IF_ALLOW_UNKNOWN_AUTHORITY</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="aff8c-126">Non implémenté actuellement.</span><span class="sxs-lookup"><span data-stu-id="aff8c-126">Currently not implemented.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="RPC_IF_ALLOW_SECURE_ONLY"></span><span id="rpc_if_allow_secure_only"></span><dl> <span data-ttu-id="aff8c-127"><dt><strong>RPC_IF_ALLOW_SECURE_ONLY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="aff8c-127"><dt><strong>RPC_IF_ALLOW_SECURE_ONLY</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="aff8c-128">Limite les connexions aux clients qui utilisent un niveau d’autorisation supérieur à RPC_C_AUTHN_LEVEL_NONE.</span><span class="sxs-lookup"><span data-stu-id="aff8c-128">Limits connections to clients that use an authorization level higher than RPC_C_AUTHN_LEVEL_NONE.</span></span> <span data-ttu-id="aff8c-129">La spécification de cet indicateur permet aux clients de traverser la session <strong>null</strong> .</span><span class="sxs-lookup"><span data-stu-id="aff8c-129">Specifying this flag allows clients to come through on the <strong>NULL</strong> session.</span></span> <span data-ttu-id="aff8c-130">Sur Windows XP et Windows Server 2003, ces clients ne sont pas autorisés.</span><span class="sxs-lookup"><span data-stu-id="aff8c-130">On Windows XP and Windows Server 2003, such clients are not allowed.</span></span> <span data-ttu-id="aff8c-131">Les clients qui échouent au test de RPC_IF_ALLOW_SECURE_ONLY reçoivent une erreur de RPC_S_ACCESS_DENIED.</span><span class="sxs-lookup"><span data-stu-id="aff8c-131">Clients that fail the RPC_IF_ALLOW_SECURE_ONLY test receive an RPC_S_ACCESS_DENIED error.</span></span> <span data-ttu-id="aff8c-132">L’utilisation de l’indicateur RPC_IF_ALLOW_SECURE_ONLY n’implique pas ou ne garantit pas un niveau élevé de privilège sur la partie de l’utilisateur appelant.</span><span class="sxs-lookup"><span data-stu-id="aff8c-132">Using the RPC_IF_ALLOW_SECURE_ONLY flag does not imply or guarantee a high level of privilege on the part of the calling user.</span></span> <span data-ttu-id="aff8c-133">RPC vérifie uniquement que l’utilisateur dispose d’informations d’identification valides ; l’utilisateur appelant peut utiliser le compte invité ou d’autres comptes à faibles privilèges.</span><span class="sxs-lookup"><span data-stu-id="aff8c-133">RPC only checks that the user has valid credentials; the calling user may be using the guest account or other low privileged accounts.</span></span> <span data-ttu-id="aff8c-134">N’assumez pas de privilèges élevés lorsque RPC_IF_ALLOW_SECURE_ONLY est utilisé.</span><span class="sxs-lookup"><span data-stu-id="aff8c-134">Do not assume high privilege when RPC_IF_ALLOW_SECURE_ONLY is used.</span></span><br/> <span data-ttu-id="aff8c-135"><strong>Windows NT 4,0 et Windows Me/98/95 :  </strong></span><span class="sxs-lookup"><span data-stu-id="aff8c-135"><strong>Windows NT 4.0 and Windows Me/98/95:  </strong></span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="RPC_IF_SEC_NO_CACHE"></span><span id="rpc_if_sec_no_cache"></span><dl> <span data-ttu-id="aff8c-136"><dt><strong>RPC_IF_SEC_NO_CACHE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="aff8c-136"><dt><strong>RPC_IF_SEC_NO_CACHE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="aff8c-137">Désactive la mise en cache des rappels de sécurité, en forçant un rappel de sécurité pour chaque appel RPC sur une interface donnée.</span><span class="sxs-lookup"><span data-stu-id="aff8c-137">Disables security callback caching, forcing a security callback for each RPC call on a given interface.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="aff8c-138">Cet indicateur est disponible à partir de Windows XP avec SP2 et de Windows Server 2003 avec SP1.</span><span class="sxs-lookup"><span data-stu-id="aff8c-138">This flag is available starting with Windows XP with SP2 and Windows Server 2003 with SP1.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="aff8c-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aff8c-139">Requirements</span></span>



| <span data-ttu-id="aff8c-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aff8c-140">Requirement</span></span> | <span data-ttu-id="aff8c-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="aff8c-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="aff8c-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aff8c-142">Minimum supported client</span></span><br/> | <span data-ttu-id="aff8c-143">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aff8c-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="aff8c-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aff8c-144">Minimum supported server</span></span><br/> | <span data-ttu-id="aff8c-145">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aff8c-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="aff8c-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="aff8c-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="aff8c-147"><dt>Rpcdce. h</dt></span><span class="sxs-lookup"><span data-stu-id="aff8c-147"><dt>Rpcdce.h</dt></span></span> </dl> |



 

 





