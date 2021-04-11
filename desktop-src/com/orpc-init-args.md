---
title: Structure ORPC_INIT_ARGS
description: La \_ \_ structure d’arguments ORPC init contient des informations utilisées pour initialiser le débogage à distance à l’aide de l’interface IOrpcDebugNotify.
ms.assetid: be7646c7-3394-45ae-ae8f-9cee68bbc789
keywords:
- Structure COM ORPC_INIT_ARGS
- Pointeur de structure LPORPC_INIT_ARGS COM
topic_type:
- apiref
api_name:
- ORPC_INIT_ARGS
api_location:
- N/A
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e7dca0209f745d5034bde2da852829b99d7dcb8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103256"
---
# <a name="orpc_init_args-structure"></a><span data-ttu-id="69287-105">ORPC \_ Init, \_ structure d’arguments</span><span class="sxs-lookup"><span data-stu-id="69287-105">ORPC\_INIT\_ARGS structure</span></span>

<span data-ttu-id="69287-106">La structure d' **\_ \_ arguments ORPC init** contient des informations utilisées pour initialiser le débogage à distance à l’aide de l’interface [**IOrpcDebugNotify**](iorpcdebugnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="69287-106">The **ORPC\_INIT\_ARGS** structure contains information used to initialize remote debugging using the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="69287-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="69287-107">Syntax</span></span>


```C++
typedef struct ORPC_INIT_ARGS {
  IOrpcDebugNotify *lpIntfOrpcDebug;
  void             *pvPSN;
  DWORD            *dwReserved1;
  DWORD            *dwReserved2;
} ORPC_INIT_ARGS, *LPORPC_INIT_ARGS;
```



## <a name="members"></a><span data-ttu-id="69287-108">Membres</span><span class="sxs-lookup"><span data-stu-id="69287-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="69287-109">**lpIntfOrpcDebug**</span><span class="sxs-lookup"><span data-stu-id="69287-109">**lpIntfOrpcDebug**</span></span>
</dt> <dd>

<span data-ttu-id="69287-110">Pointeur vers l’interface [**IOrpcDebugNotify**](iorpcdebugnotify.md) pour une utilisation par les débogueurs in-process.</span><span class="sxs-lookup"><span data-stu-id="69287-110">A pointer to the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface for use by in-process debuggers.</span></span> <span data-ttu-id="69287-111">Si le débogueur n’est pas in-process ou s’il s’agit d’un système Macintosh, ce champ doit avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="69287-111">If the debugger is not in-process or is a Macintosh system, this field must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="69287-112">**pvPSN**</span><span class="sxs-lookup"><span data-stu-id="69287-112">**pvPSN**</span></span>
</dt> <dd>

<span data-ttu-id="69287-113">Pointeur vers le numéro de série du processus Macintosh du processus du programme débogué.</span><span class="sxs-lookup"><span data-stu-id="69287-113">A pointer to the Macintosh process serial number of the debuggee's process.</span></span> <span data-ttu-id="69287-114">Si le programme débogué n’est pas un système Macintosh, ce champ doit avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="69287-114">If the debuggee is not a Macintosh system, this field must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="69287-115">**dwReserved1**</span><span class="sxs-lookup"><span data-stu-id="69287-115">**dwReserved1**</span></span>
</dt> <dd>

<span data-ttu-id="69287-116">Réservé.</span><span class="sxs-lookup"><span data-stu-id="69287-116">Reserved.</span></span> <span data-ttu-id="69287-117">Doit être égal à 0.</span><span class="sxs-lookup"><span data-stu-id="69287-117">Must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="69287-118">**dwReserved2**</span><span class="sxs-lookup"><span data-stu-id="69287-118">**dwReserved2**</span></span>
</dt> <dd>

<span data-ttu-id="69287-119">Réservé.</span><span class="sxs-lookup"><span data-stu-id="69287-119">Reserved.</span></span> <span data-ttu-id="69287-120">Doit être égal à 0.</span><span class="sxs-lookup"><span data-stu-id="69287-120">Must be 0.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="69287-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="69287-121">Requirements</span></span>



| <span data-ttu-id="69287-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="69287-122">Requirement</span></span> | <span data-ttu-id="69287-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="69287-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="69287-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="69287-124">Minimum supported client</span></span><br/> | <span data-ttu-id="69287-125">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="69287-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                     |
| <span data-ttu-id="69287-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="69287-126">Minimum supported server</span></span><br/> | <span data-ttu-id="69287-127">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="69287-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="69287-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="69287-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="69287-129"><dt>N/A</dt></span><span class="sxs-lookup"><span data-stu-id="69287-129"><dt>N/A</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69287-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="69287-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69287-131">**ORPC \_ dbg \_ tout**</span><span class="sxs-lookup"><span data-stu-id="69287-131">**ORPC\_DBG\_ALL**</span></span>](orpc-dbg-all.md)
</dt> <dt>

[<span data-ttu-id="69287-132">**\_ \_ mémoire tampon dbg ORPC**</span><span class="sxs-lookup"><span data-stu-id="69287-132">**ORPC\_DBG\_BUFFER**</span></span>](orpc-dbg-buffer.md)
</dt> <dt>

[<span data-ttu-id="69287-133">**DllDebugObjectRPCHook**</span><span class="sxs-lookup"><span data-stu-id="69287-133">**DllDebugObjectRPCHook**</span></span>](dlldebugobjectrpchook.md)
</dt> <dt>

[<span data-ttu-id="69287-134">**IOrpcDebugNotify**</span><span class="sxs-lookup"><span data-stu-id="69287-134">**IOrpcDebugNotify**</span></span>](iorpcdebugnotify.md)
</dt> </dl>

 

 





