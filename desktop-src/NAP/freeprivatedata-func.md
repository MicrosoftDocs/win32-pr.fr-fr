---
title: FreePrivateData, fonction (NapUtil. h)
description: Libère une structure de données PrivateData.
ms.assetid: 94b3618e-224f-4801-94f3-2faa1a298ec0
keywords:
- FreePrivateData fonction NAP
topic_type:
- apiref
api_name:
- FreePrivateData
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4629c264c91a4e0c6e18443cf27a9fd9d182164
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942627"
---
# <a name="freeprivatedata-function"></a><span data-ttu-id="a6ba3-104">FreePrivateData fonction)</span><span class="sxs-lookup"><span data-stu-id="a6ba3-104">FreePrivateData function</span></span>

> [!Note]  
> <span data-ttu-id="a6ba3-105">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="a6ba3-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="a6ba3-106">La fonction **FreePrivateData** libère une structure de données [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) .</span><span class="sxs-lookup"><span data-stu-id="a6ba3-106">The **FreePrivateData** function frees a [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) data structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6ba3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a6ba3-107">Syntax</span></span>


```C++
NAPAPI VOID WINAPI FreePrivateData(
  _In_ PrivateData *privateData
);
```



## <a name="parameters"></a><span data-ttu-id="a6ba3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a6ba3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6ba3-109">*privateData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a6ba3-109">*privateData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6ba3-110">Pointeur vers la structure de données [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) à libérer.</span><span class="sxs-lookup"><span data-stu-id="a6ba3-110">A pointer to the [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) data structure to free.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a6ba3-111">Notes</span><span class="sxs-lookup"><span data-stu-id="a6ba3-111">Remarks</span></span>

<span data-ttu-id="a6ba3-112">Toutes les interfaces COM prises en charge par le système NAP utilisent des règles de gestion de mémoire COM standard et les allocateurs de mémoire COM (**CoTaskMemAlloc** et **CoTaskMemFree**) :</span><span class="sxs-lookup"><span data-stu-id="a6ba3-112">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocators (**CoTaskMemAlloc** and **CoTaskMemFree**):</span></span>

-   <span data-ttu-id="a6ba3-113">Les paramètres **in** sont alloués et libérés par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="a6ba3-113">**In** parameters are allocated and freed by the caller.</span></span>
-   <span data-ttu-id="a6ba3-114">Les paramètres **out** sont alloués par l’appelé et libérés par l’appelant à l’aide de **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="a6ba3-114">**Out** parameters are allocated by the callee and freed by the caller using **CoTaskMem**.</span></span>
-   <span data-ttu-id="a6ba3-115">Les paramètres **in/out** sont alloués par l’appelant, libérés et réalloués par l’appelé, et libérés au final par l’appelant, à l’aide de **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="a6ba3-115">**In/out** parameters are allocated by the caller, freed and reallocated by the callee, and ultimately freed by the caller, using **CoTaskMem**.</span></span>

<span data-ttu-id="a6ba3-116">Toutes les fonctions NAP pour libérer de la mémoire libèrent également tous les pointeurs incorporés.</span><span class="sxs-lookup"><span data-stu-id="a6ba3-116">All NAP functions for freeing memory also free all embedded pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6ba3-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a6ba3-117">Requirements</span></span>



| <span data-ttu-id="a6ba3-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a6ba3-118">Requirement</span></span> | <span data-ttu-id="a6ba3-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="a6ba3-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a6ba3-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a6ba3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a6ba3-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a6ba3-121">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="a6ba3-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a6ba3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a6ba3-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a6ba3-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a6ba3-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="a6ba3-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6ba3-125"><dt>NapUtil. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6ba3-125"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="a6ba3-126">DLL</span><span class="sxs-lookup"><span data-stu-id="a6ba3-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a6ba3-127"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6ba3-127"><dt>Qutil.dll</dt></span></span> </dl> |



 

 





