---
title: Fonctions de handle de liaison
description: Le tableau suivant contient la liste des routines runtime RPC qui fonctionnent sur des handles de liaison et spécifie le type de handle de liaison autorisé.
ms.assetid: 16effe59-ebe2-48c3-b97a-90656b6d3b51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89e00b3cbb2d5fc5637b9414d6f009cfb2e4ade4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512432"
---
# <a name="binding-handle-functions"></a><span data-ttu-id="da3dc-103">Fonctions de handle de liaison</span><span class="sxs-lookup"><span data-stu-id="da3dc-103">Binding Handle Functions</span></span>

<span data-ttu-id="da3dc-104">Le tableau suivant contient la liste des routines runtime RPC qui fonctionnent sur des handles de liaison et spécifie le type de handle de liaison autorisé.</span><span class="sxs-lookup"><span data-stu-id="da3dc-104">The following table contains the list of RPC run-time routines that operate on binding handles and specifies the type of binding handle allowed.</span></span>



| <span data-ttu-id="da3dc-105">Routine</span><span class="sxs-lookup"><span data-stu-id="da3dc-105">Routine</span></span>                                                            | <span data-ttu-id="da3dc-106">Argument d’entrée</span><span class="sxs-lookup"><span data-stu-id="da3dc-106">Input argument</span></span>   | <span data-ttu-id="da3dc-107">Argument de sortie</span><span class="sxs-lookup"><span data-stu-id="da3dc-107">Output argument</span></span> |
|--------------------------------------------------------------------|------------------|-----------------|
| [<span data-ttu-id="da3dc-108">**RpcBindingCopy**</span><span class="sxs-lookup"><span data-stu-id="da3dc-108">**RpcBindingCopy**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingcopy)                           | <span data-ttu-id="da3dc-109">Serveur</span><span class="sxs-lookup"><span data-stu-id="da3dc-109">Server</span></span>           | <span data-ttu-id="da3dc-110">Serveur</span><span class="sxs-lookup"><span data-stu-id="da3dc-110">Server</span></span>          |
| [<span data-ttu-id="da3dc-111">**RpcBindingFree**</span><span class="sxs-lookup"><span data-stu-id="da3dc-111">**RpcBindingFree**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree)                           | <span data-ttu-id="da3dc-112">Serveur</span><span class="sxs-lookup"><span data-stu-id="da3dc-112">Server</span></span>           | <span data-ttu-id="da3dc-113">Aucun</span><span class="sxs-lookup"><span data-stu-id="da3dc-113">None</span></span>            |
| [<span data-ttu-id="da3dc-114">**RpcBindingFromStringBinding**</span><span class="sxs-lookup"><span data-stu-id="da3dc-114">**RpcBindingFromStringBinding**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) | <span data-ttu-id="da3dc-115">Aucun</span><span class="sxs-lookup"><span data-stu-id="da3dc-115">None</span></span>             | <span data-ttu-id="da3dc-116">Serveur</span><span class="sxs-lookup"><span data-stu-id="da3dc-116">Server</span></span>          |
| [<span data-ttu-id="da3dc-117">**RpcBindingInqAuthClient**</span><span class="sxs-lookup"><span data-stu-id="da3dc-117">**RpcBindingInqAuthClient**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient)         | <span data-ttu-id="da3dc-118">Client</span><span class="sxs-lookup"><span data-stu-id="da3dc-118">Client</span></span>           | <span data-ttu-id="da3dc-119">None</span><span class="sxs-lookup"><span data-stu-id="da3dc-119">None</span></span>            |
| [<span data-ttu-id="da3dc-120">**RpcBindingInqAuthInfo**</span><span class="sxs-lookup"><span data-stu-id="da3dc-120">**RpcBindingInqAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfo)             | <span data-ttu-id="da3dc-121">Serveur</span><span class="sxs-lookup"><span data-stu-id="da3dc-121">Server</span></span>           | <span data-ttu-id="da3dc-122">Aucun</span><span class="sxs-lookup"><span data-stu-id="da3dc-122">None</span></span>            |
| [<span data-ttu-id="da3dc-123">**RpcBindingInqObject**</span><span class="sxs-lookup"><span data-stu-id="da3dc-123">**RpcBindingInqObject**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqobject)                 | <span data-ttu-id="da3dc-124">Serveur ou client</span><span class="sxs-lookup"><span data-stu-id="da3dc-124">Server or client</span></span> | <span data-ttu-id="da3dc-125">Aucun</span><span class="sxs-lookup"><span data-stu-id="da3dc-125">None</span></span>            |
| [<span data-ttu-id="da3dc-126">**RpcBindingReset**</span><span class="sxs-lookup"><span data-stu-id="da3dc-126">**RpcBindingReset**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset)                         | <span data-ttu-id="da3dc-127">Serveur</span><span class="sxs-lookup"><span data-stu-id="da3dc-127">Server</span></span>           | <span data-ttu-id="da3dc-128">Aucun</span><span class="sxs-lookup"><span data-stu-id="da3dc-128">None</span></span>            |
| [<span data-ttu-id="da3dc-129">**RpcBindingSetAuthInfo**</span><span class="sxs-lookup"><span data-stu-id="da3dc-129">**RpcBindingSetAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)             | <span data-ttu-id="da3dc-130">Serveur</span><span class="sxs-lookup"><span data-stu-id="da3dc-130">Server</span></span>           | <span data-ttu-id="da3dc-131">Aucun</span><span class="sxs-lookup"><span data-stu-id="da3dc-131">None</span></span>            |
| [<span data-ttu-id="da3dc-132">**RpcBindingSetObject**</span><span class="sxs-lookup"><span data-stu-id="da3dc-132">**RpcBindingSetObject**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetobject)                 | <span data-ttu-id="da3dc-133">Serveur</span><span class="sxs-lookup"><span data-stu-id="da3dc-133">Server</span></span>           | <span data-ttu-id="da3dc-134">Aucun</span><span class="sxs-lookup"><span data-stu-id="da3dc-134">None</span></span>            |
| [<span data-ttu-id="da3dc-135">**RpcBindingToStringBinding**</span><span class="sxs-lookup"><span data-stu-id="da3dc-135">**RpcBindingToStringBinding**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding)     | <span data-ttu-id="da3dc-136">Serveur ou client</span><span class="sxs-lookup"><span data-stu-id="da3dc-136">Server or client</span></span> | <span data-ttu-id="da3dc-137">Aucun</span><span class="sxs-lookup"><span data-stu-id="da3dc-137">None</span></span>            |
| [<span data-ttu-id="da3dc-138">**RpcBindingVectorFree**</span><span class="sxs-lookup"><span data-stu-id="da3dc-138">**RpcBindingVectorFree**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingvectorfree)               | <span data-ttu-id="da3dc-139">Serveur</span><span class="sxs-lookup"><span data-stu-id="da3dc-139">Server</span></span>           | <span data-ttu-id="da3dc-140">Aucun</span><span class="sxs-lookup"><span data-stu-id="da3dc-140">None</span></span>            |
| [<span data-ttu-id="da3dc-141">**RpcNsBindingExport**</span><span class="sxs-lookup"><span data-stu-id="da3dc-141">**RpcNsBindingExport**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta)                   | <span data-ttu-id="da3dc-142">Serveur</span><span class="sxs-lookup"><span data-stu-id="da3dc-142">Server</span></span>           | <span data-ttu-id="da3dc-143">Aucun</span><span class="sxs-lookup"><span data-stu-id="da3dc-143">None</span></span>            |
| [<span data-ttu-id="da3dc-144">**RpcNsBindingImportNext**</span><span class="sxs-lookup"><span data-stu-id="da3dc-144">**RpcNsBindingImportNext**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext)           | <span data-ttu-id="da3dc-145">Aucun</span><span class="sxs-lookup"><span data-stu-id="da3dc-145">None</span></span>             | <span data-ttu-id="da3dc-146">Serveur</span><span class="sxs-lookup"><span data-stu-id="da3dc-146">Server</span></span>          |
| [<span data-ttu-id="da3dc-147">**RpcNsBindingLookupNext**</span><span class="sxs-lookup"><span data-stu-id="da3dc-147">**RpcNsBindingLookupNext**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext)           | <span data-ttu-id="da3dc-148">Aucun</span><span class="sxs-lookup"><span data-stu-id="da3dc-148">None</span></span>             | <span data-ttu-id="da3dc-149">Serveur</span><span class="sxs-lookup"><span data-stu-id="da3dc-149">Server</span></span>          |
| [<span data-ttu-id="da3dc-150">**RpcNsBindingSelect**</span><span class="sxs-lookup"><span data-stu-id="da3dc-150">**RpcNsBindingSelect**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingselect)                   | <span data-ttu-id="da3dc-151">Serveur</span><span class="sxs-lookup"><span data-stu-id="da3dc-151">Server</span></span>           | <span data-ttu-id="da3dc-152">Serveur</span><span class="sxs-lookup"><span data-stu-id="da3dc-152">Server</span></span>          |
| [<span data-ttu-id="da3dc-153">**RpcServerInqBindings**</span><span class="sxs-lookup"><span data-stu-id="da3dc-153">**RpcServerInqBindings**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings)               | <span data-ttu-id="da3dc-154">Aucun</span><span class="sxs-lookup"><span data-stu-id="da3dc-154">None</span></span>             | <span data-ttu-id="da3dc-155">Serveur</span><span class="sxs-lookup"><span data-stu-id="da3dc-155">Server</span></span>          |



 

 

 




