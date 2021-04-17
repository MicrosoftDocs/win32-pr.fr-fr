---
title: Interface IOrpcDebugNotify
description: Fournit des fonctionnalités de débogage distant.
ms.assetid: f91987c0-2e4b-4872-8ed6-e208a23baa49
keywords:
- Interface IOrpcDebugNotify COM
- Interface IOrpcDebugNotify COM, Description
topic_type:
- apiref
api_name:
- IOrpcDebugNotify
api_location:
- N/A
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f4db08daf93997b2a7fa0ed383591cb5d111ac7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519057"
---
# <a name="iorpcdebugnotify-interface"></a><span data-ttu-id="3f021-105">Interface IOrpcDebugNotify</span><span class="sxs-lookup"><span data-stu-id="3f021-105">IOrpcDebugNotify interface</span></span>

<span data-ttu-id="3f021-106">Fournit des fonctionnalités de débogage distant.</span><span class="sxs-lookup"><span data-stu-id="3f021-106">Provides remote debugging functionality.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="3f021-107">Quand implémenter</span><span class="sxs-lookup"><span data-stu-id="3f021-107">When to implement</span></span>

<span data-ttu-id="3f021-108">Implémentez cette interface pour activer le débogage à distance sur RPC.</span><span class="sxs-lookup"><span data-stu-id="3f021-108">Implement this interface to enable remote debugging over RPC.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="3f021-109">Quand l’utiliser</span><span class="sxs-lookup"><span data-stu-id="3f021-109">When to use</span></span>

<span data-ttu-id="3f021-110">Cette interface doit être utilisée pour le débogage distant in-process quand les exceptions logicielles ne doivent pas être utilisées pour les notifications du débogueur COM.</span><span class="sxs-lookup"><span data-stu-id="3f021-110">This interface should be used for in-process remote debugging when software exceptions should not be used for the COM debugger notifications.</span></span> <span data-ttu-id="3f021-111">Elle permet aux débogueurs in-process d’être avertis par des appels directs à l’aide de ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="3f021-111">It enables in-process debuggers to be notified by direct calls using these methods.</span></span>

## <a name="members"></a><span data-ttu-id="3f021-112">Membres</span><span class="sxs-lookup"><span data-stu-id="3f021-112">Members</span></span>

<span data-ttu-id="3f021-113">L’interface **IOrpcDebugNotify** hérite de l’interface [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="3f021-113">The **IOrpcDebugNotify** interface inherits from the [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="3f021-114">**IOrpcDebugNotify** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="3f021-114">**IOrpcDebugNotify** also has these types of members:</span></span>

-   [<span data-ttu-id="3f021-115">Méthodes</span><span class="sxs-lookup"><span data-stu-id="3f021-115">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3f021-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="3f021-116">Methods</span></span>

<span data-ttu-id="3f021-117">L’interface **IOrpcDebugNotify** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="3f021-117">The **IOrpcDebugNotify** interface has these methods.</span></span>



| <span data-ttu-id="3f021-118">Méthode</span><span class="sxs-lookup"><span data-stu-id="3f021-118">Method</span></span>                                                              | <span data-ttu-id="3f021-119">Description</span><span class="sxs-lookup"><span data-stu-id="3f021-119">Description</span></span>                                                                    |
|:--------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="3f021-120">**ClientFillBuffer**</span><span class="sxs-lookup"><span data-stu-id="3f021-120">**ClientFillBuffer**</span></span>](iorpcdebugnotify-clientfillbuffer.md)       | <span data-ttu-id="3f021-121">Envoie des données du débogueur client au débogueur de serveur.</span><span class="sxs-lookup"><span data-stu-id="3f021-121">Sends data from the client debugger to the server debugger.</span></span><br/>         |
| [<span data-ttu-id="3f021-122">**ClientGetBufferSize**</span><span class="sxs-lookup"><span data-stu-id="3f021-122">**ClientGetBufferSize**</span></span>](iorpcdebugnotify-clientgetbuffersize.md) | <span data-ttu-id="3f021-123">Récupère la taille de la mémoire tampon RPC à partir du débogueur côté client.</span><span class="sxs-lookup"><span data-stu-id="3f021-123">Retrieves the RPC buffer size from the client-side debugger.</span></span><br/>        |
| [<span data-ttu-id="3f021-124">**ClientNotify**</span><span class="sxs-lookup"><span data-stu-id="3f021-124">**ClientNotify**</span></span>](iorpcdebugnotify-clientnotify.md)               | <span data-ttu-id="3f021-125">Informe le client d’une demande de débogueur sortant au serveur.</span><span class="sxs-lookup"><span data-stu-id="3f021-125">Informs the client of an outgoing debugger request to the server.</span></span><br/>   |
| [<span data-ttu-id="3f021-126">**ServerFillBuffer**</span><span class="sxs-lookup"><span data-stu-id="3f021-126">**ServerFillBuffer**</span></span>](iorpcdebugnotify-serverfillbuffer.md)       | <span data-ttu-id="3f021-127">Envoie des données du débogueur de serveur au débogueur client.</span><span class="sxs-lookup"><span data-stu-id="3f021-127">Sends data from the server debugger to the client debugger.</span></span><br/>         |
| [<span data-ttu-id="3f021-128">**ServerGetBufferSize**</span><span class="sxs-lookup"><span data-stu-id="3f021-128">**ServerGetBufferSize**</span></span>](iorpcdebugnotify-servergetbuffersize.md) | <span data-ttu-id="3f021-129">Récupère la taille de la mémoire tampon RPC à partir du débogueur côté serveur.</span><span class="sxs-lookup"><span data-stu-id="3f021-129">Retrieves the RPC buffer size from the server-side debugger.</span></span><br/>        |
| [<span data-ttu-id="3f021-130">**ServerNotify**</span><span class="sxs-lookup"><span data-stu-id="3f021-130">**ServerNotify**</span></span>](iorpcdebugnotify-servernotify.md)               | <span data-ttu-id="3f021-131">Informe le serveur d’une demande de débogueur entrant du client.</span><span class="sxs-lookup"><span data-stu-id="3f021-131">Informs the server of an incoming debugger request from the client.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3f021-132">Notes</span><span class="sxs-lookup"><span data-stu-id="3f021-132">Remarks</span></span>

<span data-ttu-id="3f021-133">Une bibliothèque d’importation contenant l’interface **IOrpcDebugNotify** n’est pas incluse dans le kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="3f021-133">An import library containing the **IOrpcDebugNotify** interface is not included in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="3f021-134">Une application peut utiliser les fonctions [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) et [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) pour récupérer un pointeur de fonction vers [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) à partir de oleaut.dll et fournir ces méthodes via l’interface **IOrpcDebugNotify** .</span><span class="sxs-lookup"><span data-stu-id="3f021-134">An application can use the [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) functions to retrieve a function pointer to [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) from oleaut.dll and provide these methods via the **IOrpcDebugNotify** interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f021-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3f021-135">Requirements</span></span>



| <span data-ttu-id="3f021-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3f021-136">Requirement</span></span> | <span data-ttu-id="3f021-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="3f021-137">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="3f021-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3f021-138">Minimum supported client</span></span><br/> | <span data-ttu-id="3f021-139">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3f021-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                     |
| <span data-ttu-id="3f021-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3f021-140">Minimum supported server</span></span><br/> | <span data-ttu-id="3f021-141">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3f021-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="3f021-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="3f021-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f021-143"><dt>N/A</dt></span><span class="sxs-lookup"><span data-stu-id="3f021-143"><dt>N/A</dt></span></span> </dl> |
| <span data-ttu-id="3f021-144">MIDL</span><span class="sxs-lookup"><span data-stu-id="3f021-144">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3f021-145"><dt>N/A</dt></span><span class="sxs-lookup"><span data-stu-id="3f021-145"><dt>N/A</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f021-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f021-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f021-147">**IUnknown**</span><span class="sxs-lookup"><span data-stu-id="3f021-147">**IUnknown**</span></span>](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)
</dt> <dt>

[<span data-ttu-id="3f021-148">**ORPC \_ dbg \_ tout**</span><span class="sxs-lookup"><span data-stu-id="3f021-148">**ORPC\_DBG\_ALL**</span></span>](orpc-dbg-all.md)
</dt> <dt>

[<span data-ttu-id="3f021-149">**\_ \_ mémoire tampon dbg ORPC**</span><span class="sxs-lookup"><span data-stu-id="3f021-149">**ORPC\_DBG\_BUFFER**</span></span>](orpc-dbg-buffer.md)
</dt> <dt>

[<span data-ttu-id="3f021-150">**ORPC \_ init \_ args**</span><span class="sxs-lookup"><span data-stu-id="3f021-150">**ORPC\_INIT\_ARGS**</span></span>](orpc-init-args.md)
</dt> <dt>

[<span data-ttu-id="3f021-151">**DllDebugObjectRPCHook**</span><span class="sxs-lookup"><span data-stu-id="3f021-151">**DllDebugObjectRPCHook**</span></span>](dlldebugobjectrpchook.md)
</dt> </dl>

 

