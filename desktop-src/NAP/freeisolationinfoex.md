---
title: FreeIsolationInfoEx, fonction (NapUtil. h)
description: Libère une structure de données IsolationInfoEx.
ms.assetid: 9ca0e5ae-aed9-43e9-b8f7-90f13d62ac16
keywords:
- FreeIsolationInfoEx fonction NAP
topic_type:
- apiref
api_name:
- FreeIsolationInfoEx
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01cf3f13f38130fe86383fee5bebe3a536ea9aad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105421"
---
# <a name="freeisolationinfoex-function"></a><span data-ttu-id="77331-104">FreeIsolationInfoEx fonction)</span><span class="sxs-lookup"><span data-stu-id="77331-104">FreeIsolationInfoEx function</span></span>

> [!Note]  
> <span data-ttu-id="77331-105">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="77331-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="77331-106">La fonction **FreeIsolationInfoEx** libère une structure de données [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) .</span><span class="sxs-lookup"><span data-stu-id="77331-106">The **FreeIsolationInfoEx** function frees an [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) data structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="77331-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="77331-107">Syntax</span></span>


```C++
NAPAPI VOID WINAPI FreeIsolationInfoEx(
  _In_ IsolationInfoEx *isolationInfo
);
```



## <a name="parameters"></a><span data-ttu-id="77331-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="77331-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77331-109">*isolationInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="77331-109">*isolationInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77331-110">Pointeur vers la structure de données [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) à libérer.</span><span class="sxs-lookup"><span data-stu-id="77331-110">A pointer to the [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) data structure to free.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="77331-111">Notes</span><span class="sxs-lookup"><span data-stu-id="77331-111">Remarks</span></span>

<span data-ttu-id="77331-112">Toutes les interfaces COM prises en charge par le système NAP utilisent des règles de gestion de mémoire COM standard et les allocateurs de mémoire COM (**CoTaskMemAlloc** et **CoTaskMemFree**) :</span><span class="sxs-lookup"><span data-stu-id="77331-112">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocators (**CoTaskMemAlloc** and **CoTaskMemFree**):</span></span>

-   <span data-ttu-id="77331-113">Les paramètres **in** sont alloués et libérés par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="77331-113">**In** parameters are allocated and freed by the caller.</span></span>
-   <span data-ttu-id="77331-114">Les paramètres **out** sont alloués par l’appelé et libérés par l’appelant à l’aide de **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="77331-114">**Out** parameters are allocated by the callee and freed by the caller using **CoTaskMem**.</span></span>
-   <span data-ttu-id="77331-115">Les paramètres **in/out** sont alloués par l’appelant, libérés et réalloués par l’appelé, et libérés au final par l’appelant, à l’aide de **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="77331-115">**In/out** parameters are allocated by the caller, freed and reallocated by the callee, and ultimately freed by the caller, using **CoTaskMem**.</span></span>

<span data-ttu-id="77331-116">Toutes les fonctions NAP pour libérer de la mémoire libèrent également tous les pointeurs incorporés.</span><span class="sxs-lookup"><span data-stu-id="77331-116">All NAP functions for freeing memory also free all embedded pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="77331-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="77331-117">Requirements</span></span>



| <span data-ttu-id="77331-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="77331-118">Requirement</span></span> | <span data-ttu-id="77331-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="77331-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="77331-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="77331-120">Minimum supported client</span></span><br/> | <span data-ttu-id="77331-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="77331-121">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="77331-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="77331-122">Minimum supported server</span></span><br/> | <span data-ttu-id="77331-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="77331-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="77331-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="77331-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="77331-125"><dt>NapUtil. h</dt></span><span class="sxs-lookup"><span data-stu-id="77331-125"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="77331-126">DLL</span><span class="sxs-lookup"><span data-stu-id="77331-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77331-127"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77331-127"><dt>Qutil.dll</dt></span></span> </dl> |



 

 





