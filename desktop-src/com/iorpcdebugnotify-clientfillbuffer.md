---
title: Méthode IOrpcDebugNotify ClientFillBuffer
description: Envoie des données du débogueur client au débogueur de serveur.
ms.assetid: d575cf34-34a2-4951-a87e-7835b2c5b7a0
keywords:
- Méthode ClientFillBuffer COM
- Méthode ClientFillBuffer COM, interface IOrpcDebugNotify
- Interface IOrpcDebugNotify COM, méthode ClientFillBuffer
topic_type:
- apiref
api_name:
- IOrpcDebugNotify.ClientFillBuffer
api_location:
- N/A
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 633f4f0a8a3e135ca60468d24356a3f6e038d062
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743708"
---
# <a name="iorpcdebugnotifyclientfillbuffer-method"></a><span data-ttu-id="96dfa-106">IOrpcDebugNotify :: ClientFillBuffer, méthode</span><span class="sxs-lookup"><span data-stu-id="96dfa-106">IOrpcDebugNotify::ClientFillBuffer method</span></span>

<span data-ttu-id="96dfa-107">Envoie des données du débogueur client au débogueur de serveur.</span><span class="sxs-lookup"><span data-stu-id="96dfa-107">Sends data from the client debugger to the server debugger.</span></span>

> [!Note]  
> <span data-ttu-id="96dfa-108">Une bibliothèque d’importation contenant la fonction **ClientFillBuffer** n’est pas incluse dans le kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="96dfa-108">An import library containing the **ClientFillBuffer** function is not included in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="96dfa-109">Une application peut utiliser les fonctions [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) et [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) pour récupérer un pointeur de fonction vers [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) à partir de oleaut.dll et fournir cette fonction par le biais de l’interface [**IOrpcDebugNotify**](iorpcdebugnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="96dfa-109">An application can use the [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) functions to retrieve a function pointer to [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) from oleaut.dll and provide this function via the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="96dfa-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="96dfa-110">Syntax</span></span>


```C++
void ClientFillBuffer(
   ORPC_DBG_ALL *lpOrpcDebugAll
);
```



## <a name="parameters"></a><span data-ttu-id="96dfa-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="96dfa-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96dfa-112">*lpOrpcDebugAll*</span><span class="sxs-lookup"><span data-stu-id="96dfa-112">*lpOrpcDebugAll*</span></span> 
</dt> <dd>

<span data-ttu-id="96dfa-113">Pointeur vers une structure [**ORPC \_ dbg \_ All**](orpc-dbg-all.md) qui contient des informations spécifiques à la notification que le système RPC com transmet au débogueur.</span><span class="sxs-lookup"><span data-stu-id="96dfa-113">A pointer to a [**ORPC\_DBG\_ALL**](orpc-dbg-all.md) structure that contains notification specific information the COM RPC system passes to the debugger.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96dfa-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="96dfa-114">Return value</span></span>

<span data-ttu-id="96dfa-115">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="96dfa-115">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="96dfa-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="96dfa-116">Requirements</span></span>



| <span data-ttu-id="96dfa-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="96dfa-117">Requirement</span></span> | <span data-ttu-id="96dfa-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="96dfa-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="96dfa-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="96dfa-119">Minimum supported client</span></span><br/> | <span data-ttu-id="96dfa-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="96dfa-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                     |
| <span data-ttu-id="96dfa-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="96dfa-121">Minimum supported server</span></span><br/> | <span data-ttu-id="96dfa-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="96dfa-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="96dfa-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="96dfa-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="96dfa-124"><dt>N/A</dt></span><span class="sxs-lookup"><span data-stu-id="96dfa-124"><dt>N/A</dt></span></span> </dl> |
| <span data-ttu-id="96dfa-125">MIDL</span><span class="sxs-lookup"><span data-stu-id="96dfa-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="96dfa-126"><dt>N/A</dt></span><span class="sxs-lookup"><span data-stu-id="96dfa-126"><dt>N/A</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96dfa-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="96dfa-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96dfa-128">**DllDebugObjectRPCHook**</span><span class="sxs-lookup"><span data-stu-id="96dfa-128">**DllDebugObjectRPCHook**</span></span>](dlldebugobjectrpchook.md)
</dt> <dt>

[<span data-ttu-id="96dfa-129">**IOrpcDebugNotify**</span><span class="sxs-lookup"><span data-stu-id="96dfa-129">**IOrpcDebugNotify**</span></span>](iorpcdebugnotify.md)
</dt> </dl>

 

