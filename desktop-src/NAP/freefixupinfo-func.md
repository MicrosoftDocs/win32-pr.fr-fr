---
title: FreeFixupInfo, fonction (NapUtil. h)
description: Libère une structure de données FixupInfo.
ms.assetid: 6bf71ccf-2618-46a3-8a04-9f83a5b7b429
keywords:
- FreeFixupInfo fonction NAP
topic_type:
- apiref
api_name:
- FreeFixupInfo
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3abf1fe07557ac786a9f0cb8e8e06a30408f6d41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106543426"
---
# <a name="freefixupinfo-function"></a><span data-ttu-id="fd5e4-104">FreeFixupInfo fonction)</span><span class="sxs-lookup"><span data-stu-id="fd5e4-104">FreeFixupInfo function</span></span>

> [!Note]  
> <span data-ttu-id="fd5e4-105">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="fd5e4-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="fd5e4-106">La fonction **FreeFixupInfo** libère une structure de données [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) .</span><span class="sxs-lookup"><span data-stu-id="fd5e4-106">The **FreeFixupInfo** function frees a [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) data structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd5e4-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fd5e4-107">Syntax</span></span>


```C++
NAPAPI VOID WINAPI FreeFixupInfo(
  _In_ FixupInfo *fixupInfo
);
```



## <a name="parameters"></a><span data-ttu-id="fd5e4-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fd5e4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd5e4-109">*fixupInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fd5e4-109">*fixupInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd5e4-110">Pointeur vers la structure de données [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) à libérer.</span><span class="sxs-lookup"><span data-stu-id="fd5e4-110">A pointer to the [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) data structure to free.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fd5e4-111">Notes</span><span class="sxs-lookup"><span data-stu-id="fd5e4-111">Remarks</span></span>

<span data-ttu-id="fd5e4-112">Toutes les interfaces COM prises en charge par le système NAP utilisent des règles de gestion de mémoire COM standard et les allocateurs de mémoire COM (**CoTaskMemAlloc** et **CoTaskMemFree**) :</span><span class="sxs-lookup"><span data-stu-id="fd5e4-112">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocators (**CoTaskMemAlloc** and **CoTaskMemFree**):</span></span>

-   <span data-ttu-id="fd5e4-113">Les paramètres **in** sont alloués et libérés par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="fd5e4-113">**In** parameters are allocated and freed by the caller.</span></span>
-   <span data-ttu-id="fd5e4-114">Les paramètres **out** sont alloués par l’appelé et libérés par l’appelant à l’aide de **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="fd5e4-114">**Out** parameters are allocated by the callee and freed by the caller using **CoTaskMem**.</span></span>
-   <span data-ttu-id="fd5e4-115">Les paramètres **in/out** sont alloués par l’appelant, libérés et réalloués par l’appelé, et libérés au final par l’appelant, à l’aide de **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="fd5e4-115">**In/out** parameters are allocated by the caller, freed and reallocated by the callee, and ultimately freed by the caller, using **CoTaskMem**.</span></span>

<span data-ttu-id="fd5e4-116">Toutes les fonctions NAP pour libérer de la mémoire libèrent également tous les pointeurs incorporés.</span><span class="sxs-lookup"><span data-stu-id="fd5e4-116">All NAP functions for freeing memory also free all embedded pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd5e4-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fd5e4-117">Requirements</span></span>



| <span data-ttu-id="fd5e4-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fd5e4-118">Requirement</span></span> | <span data-ttu-id="fd5e4-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd5e4-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fd5e4-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd5e4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fd5e4-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fd5e4-121">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="fd5e4-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd5e4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fd5e4-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fd5e4-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="fd5e4-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="fd5e4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd5e4-125"><dt>NapUtil. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd5e4-125"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="fd5e4-126">DLL</span><span class="sxs-lookup"><span data-stu-id="fd5e4-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd5e4-127"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd5e4-127"><dt>Qutil.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd5e4-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd5e4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd5e4-129">**AllocFixupInfo**</span><span class="sxs-lookup"><span data-stu-id="fd5e4-129">**AllocFixupInfo**</span></span>](allocfixupinfo-func.md)
</dt> </dl>

 

 





