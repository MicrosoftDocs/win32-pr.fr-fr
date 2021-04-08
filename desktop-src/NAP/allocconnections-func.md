---
title: AllocConnections, fonction (NapUtil. h)
description: Alloue de la mémoire pour un nombre spécifié de structures de connexions.
ms.assetid: 0e0075ed-6e4c-43f7-af40-c6dea2808d05
keywords:
- AllocConnections fonction NAP
topic_type:
- apiref
api_name:
- AllocConnections
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e29521d2fea6eec3765a3a34210b896f1baa4db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743900"
---
# <a name="allocconnections-function"></a><span data-ttu-id="d1358-104">AllocConnections fonction)</span><span class="sxs-lookup"><span data-stu-id="d1358-104">AllocConnections function</span></span>

> [!Note]  
> <span data-ttu-id="d1358-105">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="d1358-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="d1358-106">La fonction **AllocConnections** alloue de la mémoire pour un nombre spécifié de structures de [**connexions**](connections-struct.md) .</span><span class="sxs-lookup"><span data-stu-id="d1358-106">The **AllocConnections** function allocates memory for a specified number of [**Connections**](connections-struct.md) structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1358-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d1358-107">Syntax</span></span>


```C++
NAPAPI HRESULT WINAPI AllocConnections(
  _Inout_ Connections **connections,
  _In_    UINT16      connectionsCount
);
```



## <a name="parameters"></a><span data-ttu-id="d1358-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d1358-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1358-109">*connexions* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="d1358-109">*connections* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d1358-110">Pointeur vers un tableau de structures de [**connexions**](connections-struct.md) qui viennent d’être allouées.</span><span class="sxs-lookup"><span data-stu-id="d1358-110">A pointer to an array of newly allocated [**Connections**](connections-struct.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="d1358-111">*connectionsCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d1358-111">*connectionsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1358-112">Nombre de structures à allouer aux *connexions*.</span><span class="sxs-lookup"><span data-stu-id="d1358-112">The number of structures to allocate to *connections*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1358-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d1358-113">Return value</span></span>



| <span data-ttu-id="d1358-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="d1358-114">Return code</span></span>                                                                                   | <span data-ttu-id="d1358-115">Description</span><span class="sxs-lookup"><span data-stu-id="d1358-115">Description</span></span>                                                                |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d1358-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d1358-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="d1358-117">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="d1358-117">The operation has completed successfully.</span></span><br/>                       |
| <dl> <span data-ttu-id="d1358-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="d1358-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="d1358-119">Un argument non valide a été passé.</span><span class="sxs-lookup"><span data-stu-id="d1358-119">An invalid argument was passed.</span></span><br/>                                 |
| <dl> <span data-ttu-id="d1358-120"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="d1358-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="d1358-121">La mémoire virtuelle du système est insuffisante.</span><span class="sxs-lookup"><span data-stu-id="d1358-121">The system is out of virtual memory.</span></span> <span data-ttu-id="d1358-122">Cette opération a échoué.</span><span class="sxs-lookup"><span data-stu-id="d1358-122">This operation has failed.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d1358-123">Notes</span><span class="sxs-lookup"><span data-stu-id="d1358-123">Remarks</span></span>

<span data-ttu-id="d1358-124">Toutes les interfaces COM prises en charge par le système NAP utilisent des règles de gestion de mémoire COM standard et les allocateurs de mémoire COM (**CoTaskMemAlloc** et **CoTaskMemFree**) :</span><span class="sxs-lookup"><span data-stu-id="d1358-124">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocators (**CoTaskMemAlloc** and **CoTaskMemFree**):</span></span>

-   <span data-ttu-id="d1358-125">Les paramètres **in** sont alloués et libérés par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="d1358-125">**In** parameters are allocated and freed by the caller.</span></span>
-   <span data-ttu-id="d1358-126">Les paramètres **out** sont alloués par l’appelé et libérés par l’appelant à l’aide de **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="d1358-126">**Out** parameters are allocated by the callee and freed by the caller using **CoTaskMem**.</span></span>
-   <span data-ttu-id="d1358-127">Les paramètres **in/out** sont alloués par l’appelant, libérés et réalloués par l’appelé, et libérés au final par l’appelant, à l’aide de **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="d1358-127">**In/out** parameters are allocated by the caller, freed and reallocated by the callee, and ultimately freed by the caller, using **CoTaskMem**.</span></span>

<span data-ttu-id="d1358-128">Toutes les fonctions NAP pour libérer de la mémoire libèrent également tous les pointeurs incorporés.</span><span class="sxs-lookup"><span data-stu-id="d1358-128">All NAP functions for freeing memory also free all embedded pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1358-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d1358-129">Requirements</span></span>



| <span data-ttu-id="d1358-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d1358-130">Requirement</span></span> | <span data-ttu-id="d1358-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="d1358-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d1358-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1358-132">Minimum supported client</span></span><br/> | <span data-ttu-id="d1358-133">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d1358-133">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="d1358-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1358-134">Minimum supported server</span></span><br/> | <span data-ttu-id="d1358-135">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d1358-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d1358-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="d1358-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1358-137"><dt>NapUtil. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1358-137"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="d1358-138">DLL</span><span class="sxs-lookup"><span data-stu-id="d1358-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1358-139"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1358-139"><dt>Qutil.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1358-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d1358-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1358-141">**FreeConnections**</span><span class="sxs-lookup"><span data-stu-id="d1358-141">**FreeConnections**</span></span>](freeconnections-func.md)
</dt> </dl>

 

 





