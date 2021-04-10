---
title: FreeConnections, fonction (NapUtil. h)
description: Libère une structure de données de connexions.
ms.assetid: bb339d71-f8e3-48d8-834d-8b957e0cb5ec
keywords:
- FreeConnections fonction NAP
topic_type:
- apiref
api_name:
- FreeConnections
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f840d02572af3e6382a06a1873573fc7a30420e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317134"
---
# <a name="freeconnections-function"></a><span data-ttu-id="dc67b-104">FreeConnections fonction)</span><span class="sxs-lookup"><span data-stu-id="dc67b-104">FreeConnections function</span></span>

> [!Note]  
> <span data-ttu-id="dc67b-105">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="dc67b-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="dc67b-106">La fonction **FreeConnections** libère une structure de données de [**connexions**](connections-struct.md) .</span><span class="sxs-lookup"><span data-stu-id="dc67b-106">The **FreeConnections** function frees a [**Connections**](connections-struct.md) data structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc67b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dc67b-107">Syntax</span></span>


```C++
NAPAPI VOID WINAPI FreeConnections(
  _In_ Connections *connections
);
```



## <a name="parameters"></a><span data-ttu-id="dc67b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dc67b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc67b-109">*connexions* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dc67b-109">*connections* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc67b-110">Pointeur vers la structure de [**connexions**](connections-struct.md) à libérer.</span><span class="sxs-lookup"><span data-stu-id="dc67b-110">A pointer to the [**Connections**](connections-struct.md) structure to free.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dc67b-111">Notes</span><span class="sxs-lookup"><span data-stu-id="dc67b-111">Remarks</span></span>

<span data-ttu-id="dc67b-112">Toutes les interfaces COM prises en charge par le système NAP utilisent des règles de gestion de mémoire COM standard et les allocateurs de mémoire COM (**CoTaskMemAlloc** et **CoTaskMemFree**) :</span><span class="sxs-lookup"><span data-stu-id="dc67b-112">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocators (**CoTaskMemAlloc** and **CoTaskMemFree**):</span></span>

-   <span data-ttu-id="dc67b-113">Les paramètres **in** sont alloués et libérés par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="dc67b-113">**In** parameters are allocated and freed by the caller.</span></span>
-   <span data-ttu-id="dc67b-114">Les paramètres **out** sont alloués par l’appelé et libérés par l’appelant à l’aide de **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="dc67b-114">**Out** parameters are allocated by the callee and freed by the caller using **CoTaskMem**.</span></span>
-   <span data-ttu-id="dc67b-115">Les paramètres **in/out** sont alloués par l’appelant, libérés et réalloués par l’appelé, et libérés au final par l’appelant, à l’aide de **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="dc67b-115">**In/out** parameters are allocated by the caller, freed and reallocated by the callee, and ultimately freed by the caller, using **CoTaskMem**.</span></span>

<span data-ttu-id="dc67b-116">Toutes les fonctions NAP pour libérer de la mémoire libèrent également tous les pointeurs incorporés.</span><span class="sxs-lookup"><span data-stu-id="dc67b-116">All NAP functions for freeing memory also free all embedded pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc67b-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dc67b-117">Requirements</span></span>



| <span data-ttu-id="dc67b-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dc67b-118">Requirement</span></span> | <span data-ttu-id="dc67b-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="dc67b-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="dc67b-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dc67b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="dc67b-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dc67b-121">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="dc67b-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dc67b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="dc67b-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dc67b-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="dc67b-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="dc67b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc67b-125"><dt>NapUtil. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc67b-125"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="dc67b-126">DLL</span><span class="sxs-lookup"><span data-stu-id="dc67b-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc67b-127"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc67b-127"><dt>Qutil.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc67b-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dc67b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc67b-129">**AllocConnections**</span><span class="sxs-lookup"><span data-stu-id="dc67b-129">**AllocConnections**</span></span>](allocconnections-func.md)
</dt> </dl>

 

 





