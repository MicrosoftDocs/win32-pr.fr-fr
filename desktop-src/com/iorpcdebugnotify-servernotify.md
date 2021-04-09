---
title: Méthode IOrpcDebugNotify ServerNotify
description: Informe le serveur d’une demande de débogueur entrant du client.
ms.assetid: 6c868b9e-f25b-4d27-80ff-697d0c005b8d
keywords:
- Méthode ServerNotify COM
- Méthode ServerNotify COM, interface IOrpcDebugNotify
- Interface IOrpcDebugNotify COM, méthode ServerNotify
topic_type:
- apiref
api_name:
- IOrpcDebugNotify.ServerNotify
api_location:
- N/A
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d6dab7cf68b305e83212045851a88e1cdecdde9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942809"
---
# <a name="iorpcdebugnotifyservernotify-method"></a><span data-ttu-id="2ddd7-106">IOrpcDebugNotify :: ServerNotify, méthode</span><span class="sxs-lookup"><span data-stu-id="2ddd7-106">IOrpcDebugNotify::ServerNotify method</span></span>

<span data-ttu-id="2ddd7-107">Informe le serveur d’une demande de débogueur entrant du client.</span><span class="sxs-lookup"><span data-stu-id="2ddd7-107">Informs the server of an incoming debugger request from the client.</span></span>

> [!Note]  
> <span data-ttu-id="2ddd7-108">Une bibliothèque d’importation contenant la fonction **ServerNotify** n’est pas incluse dans le kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="2ddd7-108">An import library containing the **ServerNotify** function is not included in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="2ddd7-109">Une application peut utiliser les fonctions [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) et [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) pour récupérer un pointeur de fonction vers [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) à partir de oleaut.dll et fournir cette fonction par le biais de l’interface [**IOrpcDebugNotify**](iorpcdebugnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="2ddd7-109">An application can use the [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) functions to retrieve a function pointer to [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) from oleaut.dll and provide this function via the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="2ddd7-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2ddd7-110">Syntax</span></span>


```C++
void ServerNotify(
   ORPC_DBG_ALL *lpOrpcDebugAll
);
```



## <a name="parameters"></a><span data-ttu-id="2ddd7-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2ddd7-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ddd7-112">*lpOrpcDebugAll*</span><span class="sxs-lookup"><span data-stu-id="2ddd7-112">*lpOrpcDebugAll*</span></span> 
</dt> <dd>

<span data-ttu-id="2ddd7-113">Pointeur vers une structure [**ORPC \_ dbg \_ All**](orpc-dbg-all.md) qui contient des informations spécifiques à la notification que le système RPC com transmet au débogueur.</span><span class="sxs-lookup"><span data-stu-id="2ddd7-113">A pointer to a [**ORPC\_DBG\_ALL**](orpc-dbg-all.md) structure that contains notification specific information the COM RPC system passes to the debugger.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ddd7-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2ddd7-114">Return value</span></span>

<span data-ttu-id="2ddd7-115">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="2ddd7-115">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ddd7-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2ddd7-116">Requirements</span></span>



| <span data-ttu-id="2ddd7-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2ddd7-117">Requirement</span></span> | <span data-ttu-id="2ddd7-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="2ddd7-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="2ddd7-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2ddd7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2ddd7-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2ddd7-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                     |
| <span data-ttu-id="2ddd7-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2ddd7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2ddd7-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2ddd7-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="2ddd7-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="2ddd7-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ddd7-124"><dt>N/A</dt></span><span class="sxs-lookup"><span data-stu-id="2ddd7-124"><dt>N/A</dt></span></span> </dl> |
| <span data-ttu-id="2ddd7-125">MIDL</span><span class="sxs-lookup"><span data-stu-id="2ddd7-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2ddd7-126"><dt>N/A</dt></span><span class="sxs-lookup"><span data-stu-id="2ddd7-126"><dt>N/A</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ddd7-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2ddd7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ddd7-128">**ORPC \_ init \_ args**</span><span class="sxs-lookup"><span data-stu-id="2ddd7-128">**ORPC\_INIT\_ARGS**</span></span>](orpc-init-args.md)
</dt> <dt>

[<span data-ttu-id="2ddd7-129">**DllDebugObjectRPCHook**</span><span class="sxs-lookup"><span data-stu-id="2ddd7-129">**DllDebugObjectRPCHook**</span></span>](dlldebugobjectrpchook.md)
</dt> <dt>

[<span data-ttu-id="2ddd7-130">**IOrpcDebugNotify**</span><span class="sxs-lookup"><span data-stu-id="2ddd7-130">**IOrpcDebugNotify**</span></span>](iorpcdebugnotify.md)
</dt> </dl>

 

