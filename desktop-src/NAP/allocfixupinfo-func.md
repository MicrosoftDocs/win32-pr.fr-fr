---
title: AllocFixupInfo, fonction (NapUtil. h)
description: Alloue de la mémoire pour une structure FixupInfo de la taille spécifiée.
ms.assetid: e0b66a08-9714-4451-a22d-3822153c6a36
keywords:
- AllocFixupInfo fonction NAP
topic_type:
- apiref
api_name:
- AllocFixupInfo
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0dffda7e5e44302173ac06e460414455eb19c6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843185"
---
# <a name="allocfixupinfo-function"></a><span data-ttu-id="95ed1-104">AllocFixupInfo fonction)</span><span class="sxs-lookup"><span data-stu-id="95ed1-104">AllocFixupInfo function</span></span>

> [!Note]  
> <span data-ttu-id="95ed1-105">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="95ed1-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="95ed1-106">La fonction **AllocFixupInfo** alloue de la mémoire pour une structure [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) de la taille spécifiée.</span><span class="sxs-lookup"><span data-stu-id="95ed1-106">The **AllocFixupInfo** function allocates memory for a [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) structure of the specified size.</span></span>

## <a name="syntax"></a><span data-ttu-id="95ed1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="95ed1-107">Syntax</span></span>


```C++
NAPAPI HRESULT WINAPI AllocFixupInfo(
  _Inout_ FixupInfo **fixupInfo,
  _In_    UINT16    countResultCodes
);
```



## <a name="parameters"></a><span data-ttu-id="95ed1-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="95ed1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95ed1-109">*fixupInfo* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="95ed1-109">*fixupInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="95ed1-110">Pointeur vers l’adresse d’une structure [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) qui vient d’être allouée.</span><span class="sxs-lookup"><span data-stu-id="95ed1-110">A pointer to the address of a newly allocated [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) structure.</span></span>

</dd> <dt>

<span data-ttu-id="95ed1-111">*countResultCodes* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="95ed1-111">*countResultCodes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95ed1-112">Nombre de codes de résultats à allouer à *fixupInfo*.</span><span class="sxs-lookup"><span data-stu-id="95ed1-112">The number of result codes to allocate to *fixupInfo*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95ed1-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="95ed1-113">Return value</span></span>



| <span data-ttu-id="95ed1-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="95ed1-114">Return code</span></span>                                                                                   | <span data-ttu-id="95ed1-115">Description</span><span class="sxs-lookup"><span data-stu-id="95ed1-115">Description</span></span>                                                                |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="95ed1-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="95ed1-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="95ed1-117">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="95ed1-117">The operation has completed successfully.</span></span><br/>                       |
| <dl> <span data-ttu-id="95ed1-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="95ed1-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="95ed1-119">Un argument non valide a été passé.</span><span class="sxs-lookup"><span data-stu-id="95ed1-119">An invalid argument was passed.</span></span><br/>                                 |
| <dl> <span data-ttu-id="95ed1-120"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="95ed1-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="95ed1-121">La mémoire virtuelle du système est insuffisante.</span><span class="sxs-lookup"><span data-stu-id="95ed1-121">The system is out of virtual memory.</span></span> <span data-ttu-id="95ed1-122">Cette opération a échoué.</span><span class="sxs-lookup"><span data-stu-id="95ed1-122">This operation has failed.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="95ed1-123">Notes</span><span class="sxs-lookup"><span data-stu-id="95ed1-123">Remarks</span></span>

<span data-ttu-id="95ed1-124">Toutes les interfaces COM prises en charge par le système NAP utilisent des règles de gestion de mémoire COM standard et les allocateurs de mémoire COM (**CoTaskMemAlloc** et **CoTaskMemFree**) :</span><span class="sxs-lookup"><span data-stu-id="95ed1-124">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocators (**CoTaskMemAlloc** and **CoTaskMemFree**):</span></span>

-   <span data-ttu-id="95ed1-125">Les paramètres **in** sont alloués et libérés par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="95ed1-125">**In** parameters are allocated and freed by the caller.</span></span>
-   <span data-ttu-id="95ed1-126">Les paramètres **out** sont alloués par l’appelé et libérés par l’appelant à l’aide de **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="95ed1-126">**Out** parameters are allocated by the callee and freed by the caller using **CoTaskMem**.</span></span>
-   <span data-ttu-id="95ed1-127">Les paramètres **in/out** sont alloués par l’appelant, libérés et réalloués par l’appelé, et libérés au final par l’appelant, à l’aide de **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="95ed1-127">**In/out** parameters are allocated by the caller, freed and reallocated by the callee, and ultimately freed by the caller, using **CoTaskMem**.</span></span>

<span data-ttu-id="95ed1-128">Toutes les fonctions NAP pour libérer de la mémoire libèrent également tous les pointeurs incorporés.</span><span class="sxs-lookup"><span data-stu-id="95ed1-128">All NAP functions for freeing memory also free all embedded pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="95ed1-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="95ed1-129">Requirements</span></span>



| <span data-ttu-id="95ed1-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="95ed1-130">Requirement</span></span> | <span data-ttu-id="95ed1-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="95ed1-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="95ed1-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="95ed1-132">Minimum supported client</span></span><br/> | <span data-ttu-id="95ed1-133">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="95ed1-133">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="95ed1-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="95ed1-134">Minimum supported server</span></span><br/> | <span data-ttu-id="95ed1-135">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="95ed1-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="95ed1-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="95ed1-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="95ed1-137"><dt>NapUtil. h</dt></span><span class="sxs-lookup"><span data-stu-id="95ed1-137"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="95ed1-138">DLL</span><span class="sxs-lookup"><span data-stu-id="95ed1-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95ed1-139"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95ed1-139"><dt>Qutil.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95ed1-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="95ed1-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95ed1-141">**FreeFixupInfo**</span><span class="sxs-lookup"><span data-stu-id="95ed1-141">**FreeFixupInfo**</span></span>](freefixupinfo-func.md)
</dt> </dl>

 

 





