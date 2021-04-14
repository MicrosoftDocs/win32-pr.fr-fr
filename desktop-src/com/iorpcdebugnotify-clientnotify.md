---
title: Méthode IOrpcDebugNotify ClientNotify
description: Informe le client d’une demande de débogueur sortant au serveur.
ms.assetid: a41e3eaa-6d1f-46bf-9103-f83e45b2cd90
keywords:
- Méthode ClientNotify COM
- Méthode ClientNotify COM, interface IOrpcDebugNotify
- Interface IOrpcDebugNotify COM, méthode ClientNotify
topic_type:
- apiref
api_name:
- IOrpcDebugNotify.ClientNotify
api_location:
- N/A
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9e788a51e278df09715aaf9d4993ac5724ed65b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466958"
---
# <a name="iorpcdebugnotifyclientnotify-method"></a><span data-ttu-id="25919-106">IOrpcDebugNotify :: ClientNotify, méthode</span><span class="sxs-lookup"><span data-stu-id="25919-106">IOrpcDebugNotify::ClientNotify method</span></span>

<span data-ttu-id="25919-107">Informe le client d’une demande de débogueur sortant au serveur.</span><span class="sxs-lookup"><span data-stu-id="25919-107">Informs the client of an outgoing debugger request to the server.</span></span>

> [!Note]  
> <span data-ttu-id="25919-108">Une bibliothèque d’importation contenant la fonction **ClientNotify** n’est pas incluse dans le kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="25919-108">An import library containing the **ClientNotify** function is not included in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="25919-109">Une application peut utiliser les fonctions [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) et [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) pour récupérer un pointeur de fonction vers [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) à partir de oleaut.dll et fournir cette fonction par le biais de l’interface [**IOrpcDebugNotify**](iorpcdebugnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="25919-109">An application can use the [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) functions to retrieve a function pointer to [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) from oleaut.dll and provide this function via the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="25919-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="25919-110">Syntax</span></span>


```C++
void ClientNotify(
   ORPC_DBG_ALL *lpOrpcDebugAll
);
```



## <a name="parameters"></a><span data-ttu-id="25919-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="25919-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25919-112">*lpOrpcDebugAll*</span><span class="sxs-lookup"><span data-stu-id="25919-112">*lpOrpcDebugAll*</span></span> 
</dt> <dd>

<span data-ttu-id="25919-113">Pointeur vers une structure [**ORPC \_ dbg \_ All**](orpc-dbg-all.md) qui contient des informations spécifiques à la notification que le système RPC com transmet au débogueur.</span><span class="sxs-lookup"><span data-stu-id="25919-113">A pointer to a [**ORPC\_DBG\_ALL**](orpc-dbg-all.md) structure that contains notification specific information the COM RPC system passes to the debugger.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25919-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="25919-114">Return value</span></span>

<span data-ttu-id="25919-115">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="25919-115">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="25919-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="25919-116">Requirements</span></span>



| <span data-ttu-id="25919-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="25919-117">Requirement</span></span> | <span data-ttu-id="25919-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="25919-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="25919-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="25919-119">Minimum supported client</span></span><br/> | <span data-ttu-id="25919-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="25919-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                     |
| <span data-ttu-id="25919-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="25919-121">Minimum supported server</span></span><br/> | <span data-ttu-id="25919-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="25919-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="25919-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="25919-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="25919-124"><dt>N/A</dt></span><span class="sxs-lookup"><span data-stu-id="25919-124"><dt>N/A</dt></span></span> </dl> |
| <span data-ttu-id="25919-125">MIDL</span><span class="sxs-lookup"><span data-stu-id="25919-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="25919-126"><dt>N/A</dt></span><span class="sxs-lookup"><span data-stu-id="25919-126"><dt>N/A</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25919-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25919-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25919-128">**ORPC \_ init \_ args**</span><span class="sxs-lookup"><span data-stu-id="25919-128">**ORPC\_INIT\_ARGS**</span></span>](orpc-init-args.md)
</dt> <dt>

[<span data-ttu-id="25919-129">**DllDebugObjectRPCHook**</span><span class="sxs-lookup"><span data-stu-id="25919-129">**DllDebugObjectRPCHook**</span></span>](dlldebugobjectrpchook.md)
</dt> <dt>

[<span data-ttu-id="25919-130">**IOrpcDebugNotify**</span><span class="sxs-lookup"><span data-stu-id="25919-130">**IOrpcDebugNotify**</span></span>](iorpcdebugnotify.md)
</dt> </dl>

 

