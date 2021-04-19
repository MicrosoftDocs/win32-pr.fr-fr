---
title: Méthode IOrpcDebugNotify ClientGetBufferSize
description: Récupère la taille de la mémoire tampon RPC à partir du débogueur côté client.
ms.assetid: 05475156-1508-4eb2-82a6-bb1701839fbd
keywords:
- Méthode ClientGetBufferSize COM
- Méthode ClientGetBufferSize COM, interface IOrpcDebugNotify
- Interface IOrpcDebugNotify COM, méthode ClientGetBufferSize
topic_type:
- apiref
api_name:
- IOrpcDebugNotify.ClientGetBufferSize
api_location:
- N/A
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50bd925b9c518c78ca37aa8219a00965f398c415
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106518125"
---
# <a name="iorpcdebugnotifyclientgetbuffersize-method"></a><span data-ttu-id="3eea3-106">IOrpcDebugNotify :: ClientGetBufferSize, méthode</span><span class="sxs-lookup"><span data-stu-id="3eea3-106">IOrpcDebugNotify::ClientGetBufferSize method</span></span>

<span data-ttu-id="3eea3-107">Récupère la taille de la mémoire tampon RPC à partir du débogueur côté client.</span><span class="sxs-lookup"><span data-stu-id="3eea3-107">Retrieves the RPC buffer size from the client-side debugger.</span></span>

> [!Note]  
> <span data-ttu-id="3eea3-108">Une bibliothèque d’importation contenant la fonction **ClientGetBufferSize** n’est pas incluse dans le kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="3eea3-108">An import library containing the **ClientGetBufferSize** function is not included in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="3eea3-109">Une application peut utiliser les fonctions [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) et [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) pour récupérer un pointeur de fonction vers [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) à partir de oleaut.dll et fournir cette fonction par le biais de l’interface [**IOrpcDebugNotify**](iorpcdebugnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="3eea3-109">An application can use the [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) functions to retrieve a function pointer to [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) from oleaut.dll and provide this function via the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="3eea3-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3eea3-110">Syntax</span></span>


```C++
void ClientGetBufferSize(
   ORPC_DBG_ALL *lpOrpcDebugAll
);
```



## <a name="parameters"></a><span data-ttu-id="3eea3-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3eea3-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3eea3-112">*lpOrpcDebugAll*</span><span class="sxs-lookup"><span data-stu-id="3eea3-112">*lpOrpcDebugAll*</span></span> 
</dt> <dd>

<span data-ttu-id="3eea3-113">Pointeur vers une structure [**ORPC \_ dbg \_ All**](orpc-dbg-all.md) qui contient des informations spécifiques à la notification que le système RPC com transmet au débogueur.</span><span class="sxs-lookup"><span data-stu-id="3eea3-113">A pointer to a [**ORPC\_DBG\_ALL**](orpc-dbg-all.md) structure that contains notification specific information the COM RPC system passes to the debugger.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3eea3-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3eea3-114">Return value</span></span>

<span data-ttu-id="3eea3-115">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="3eea3-115">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="3eea3-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3eea3-116">Requirements</span></span>



| <span data-ttu-id="3eea3-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3eea3-117">Requirement</span></span> | <span data-ttu-id="3eea3-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="3eea3-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="3eea3-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3eea3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3eea3-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3eea3-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                     |
| <span data-ttu-id="3eea3-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3eea3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3eea3-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3eea3-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="3eea3-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="3eea3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3eea3-124"><dt>N/A</dt></span><span class="sxs-lookup"><span data-stu-id="3eea3-124"><dt>N/A</dt></span></span> </dl> |
| <span data-ttu-id="3eea3-125">MIDL</span><span class="sxs-lookup"><span data-stu-id="3eea3-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3eea3-126"><dt>N/A</dt></span><span class="sxs-lookup"><span data-stu-id="3eea3-126"><dt>N/A</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3eea3-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3eea3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3eea3-128">**ORPC \_ init \_ args**</span><span class="sxs-lookup"><span data-stu-id="3eea3-128">**ORPC\_INIT\_ARGS**</span></span>](orpc-init-args.md)
</dt> <dt>

[<span data-ttu-id="3eea3-129">**DllDebugObjectRPCHook**</span><span class="sxs-lookup"><span data-stu-id="3eea3-129">**DllDebugObjectRPCHook**</span></span>](dlldebugobjectrpchook.md)
</dt> <dt>

[<span data-ttu-id="3eea3-130">**IOrpcDebugNotify**</span><span class="sxs-lookup"><span data-stu-id="3eea3-130">**IOrpcDebugNotify**</span></span>](iorpcdebugnotify.md)
</dt> </dl>

 

