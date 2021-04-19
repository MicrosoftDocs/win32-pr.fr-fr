---
title: DllDebugObjectRPCHook fonction)
description: Exporté par les DLL COM pour activer le débogage distant.
ms.assetid: a0f8bf12-0889-452d-84d0-255c5c143bc1
keywords:
- DllDebugObjectRPCHook fonction COM
topic_type:
- apiref
api_name:
- DllDebugObjectRPCHook
api_location:
- ole32.dll
- API-MS-Win-Core-Com-private-l1-1-0.dll
- ComBase.dll
- API-MS-Win-Core-COM-Private-l1-1-1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62fffe6cc2d9ca650442d0a1c3fea2048fc6c84b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510360"
---
# <a name="dlldebugobjectrpchook-function"></a><span data-ttu-id="7b109-104">DllDebugObjectRPCHook fonction)</span><span class="sxs-lookup"><span data-stu-id="7b109-104">DllDebugObjectRPCHook function</span></span>

<span data-ttu-id="7b109-105">Exporté par les DLL COM pour activer le débogage distant.</span><span class="sxs-lookup"><span data-stu-id="7b109-105">Exported by COM DLLs to enable remote debugging.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b109-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7b109-106">Syntax</span></span>


```C++
BOOL WINAPI DllDebugObjectRPCHook(
   BOOL             fTrace,
   LPORPC_INIT_ARGS lpOrpcInitArgs
);
```



## <a name="parameters"></a><span data-ttu-id="7b109-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7b109-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b109-108">*fTrace*</span><span class="sxs-lookup"><span data-stu-id="7b109-108">*fTrace*</span></span> 
</dt> <dd>

<span data-ttu-id="7b109-109">Si la **valeur est true**, le débogage à distance est activé.</span><span class="sxs-lookup"><span data-stu-id="7b109-109">If **TRUE**, remote debugging is enabled.</span></span> <span data-ttu-id="7b109-110">Si la **valeur est false**, le débogage à distance n’est pas activé.</span><span class="sxs-lookup"><span data-stu-id="7b109-110">If **FALSE**, remote debugging is not enabled.</span></span>

</dd> <dt>

<span data-ttu-id="7b109-111">*lpOrpcInitArgs*</span><span class="sxs-lookup"><span data-stu-id="7b109-111">*lpOrpcInitArgs*</span></span> 
</dt> <dd>

<span data-ttu-id="7b109-112">Pointeur vers une structure [**d' \_ \_ arguments ORPC init**](orpc-init-args.md) .</span><span class="sxs-lookup"><span data-stu-id="7b109-112">A pointer to an [**ORPC\_INIT\_ARGS**](orpc-init-args.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b109-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7b109-113">Return value</span></span>

<span data-ttu-id="7b109-114">**True** en cas de réussite, **false** dans le cas contraire</span><span class="sxs-lookup"><span data-stu-id="7b109-114">**TRUE** if successful, **FALSE** otherwise</span></span>

## <a name="requirements"></a><span data-ttu-id="7b109-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7b109-115">Requirements</span></span>



| <span data-ttu-id="7b109-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7b109-116">Requirement</span></span> | <span data-ttu-id="7b109-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="7b109-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7b109-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7b109-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7b109-119">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7b109-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="7b109-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7b109-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7b109-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7b109-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="7b109-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="7b109-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b109-123"><dt>N/A</dt></span><span class="sxs-lookup"><span data-stu-id="7b109-123"><dt>N/A</dt></span></span> </dl>       |
| <span data-ttu-id="7b109-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7b109-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="7b109-125"><dt>Ole32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7b109-125"><dt>Ole32.lib</dt></span></span> </dl> |
| <span data-ttu-id="7b109-126">DLL</span><span class="sxs-lookup"><span data-stu-id="7b109-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b109-127"><dt>Ole32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b109-127"><dt>Ole32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b109-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7b109-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b109-129">**ORPC \_ dbg \_ tout**</span><span class="sxs-lookup"><span data-stu-id="7b109-129">**ORPC\_DBG\_ALL**</span></span>](orpc-dbg-all.md)
</dt> <dt>

[<span data-ttu-id="7b109-130">**\_ \_ mémoire tampon dbg ORPC**</span><span class="sxs-lookup"><span data-stu-id="7b109-130">**ORPC\_DBG\_BUFFER**</span></span>](orpc-dbg-buffer.md)
</dt> <dt>

[<span data-ttu-id="7b109-131">**ORPC \_ init \_ args**</span><span class="sxs-lookup"><span data-stu-id="7b109-131">**ORPC\_INIT\_ARGS**</span></span>](orpc-init-args.md)
</dt> <dt>

[<span data-ttu-id="7b109-132">**IOrpcDebugNotify**</span><span class="sxs-lookup"><span data-stu-id="7b109-132">**IOrpcDebugNotify**</span></span>](iorpcdebugnotify.md)
</dt> </dl>

 

 





