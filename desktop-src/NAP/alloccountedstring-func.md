---
title: AllocCountedString, fonction (NapUtil. h)
description: Alloue de la mémoire pour une chaîne terminée par le caractère null et la retourne dans une structure CountedString.
ms.assetid: 6dd503bf-8853-499b-adcd-54de696f01d6
keywords:
- AllocCountedString fonction NAP
topic_type:
- apiref
api_name:
- AllocCountedString
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ab2980ce5eefdd7743907bdcc947cdce1c74823
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510519"
---
# <a name="alloccountedstring-function"></a><span data-ttu-id="d4704-104">AllocCountedString fonction)</span><span class="sxs-lookup"><span data-stu-id="d4704-104">AllocCountedString function</span></span>

> [!Note]  
> <span data-ttu-id="d4704-105">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="d4704-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="d4704-106">La fonction **AllocCountedString** alloue de la mémoire pour une chaîne terminée par le caractère null et la retourne dans une structure [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) .</span><span class="sxs-lookup"><span data-stu-id="d4704-106">The **AllocCountedString** function allocates memory for a null-terminated string and returns it in a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4704-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d4704-107">Syntax</span></span>


```C++
NAPAPI HRESULT WINAPI AllocCountedString(
  _Inout_       CountedString **countedString,
  _In_    const WCHAR         *string
);
```



## <a name="parameters"></a><span data-ttu-id="d4704-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d4704-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4704-109">*countedString* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="d4704-109">*countedString* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d4704-110">Pointeur vers l’adresse d’une structure [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) qui vient d’être allouée.</span><span class="sxs-lookup"><span data-stu-id="d4704-110">A pointer to the address of a newly allocated [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure.</span></span>

</dd> <dt>

<span data-ttu-id="d4704-111">*chaîne* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d4704-111">*string* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4704-112">Pointeur vers la chaîne terminée par le caractère null qui doit être retournée dans *countedString*.</span><span class="sxs-lookup"><span data-stu-id="d4704-112">A pointer to the null-terminated string that is to be returned in *countedString*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4704-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d4704-113">Return value</span></span>



| <span data-ttu-id="d4704-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="d4704-114">Return code</span></span>                                                                                   | <span data-ttu-id="d4704-115">Description</span><span class="sxs-lookup"><span data-stu-id="d4704-115">Description</span></span>                                                                |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d4704-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d4704-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="d4704-117">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="d4704-117">The operation has completed successfully.</span></span><br/>                       |
| <dl> <span data-ttu-id="d4704-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="d4704-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="d4704-119">Un argument non valide a été passé.</span><span class="sxs-lookup"><span data-stu-id="d4704-119">An invalid argument was passed.</span></span><br/>                                 |
| <dl> <span data-ttu-id="d4704-120"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="d4704-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="d4704-121">La mémoire virtuelle du système est insuffisante.</span><span class="sxs-lookup"><span data-stu-id="d4704-121">The system is out of virtual memory.</span></span> <span data-ttu-id="d4704-122">Cette opération a échoué.</span><span class="sxs-lookup"><span data-stu-id="d4704-122">This operation has failed.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d4704-123">Notes</span><span class="sxs-lookup"><span data-stu-id="d4704-123">Remarks</span></span>

<span data-ttu-id="d4704-124">Toutes les interfaces COM prises en charge par le système NAP utilisent des règles de gestion de mémoire COM standard et les allocateurs de mémoire COM (**CoTaskMemAlloc** et **CoTaskMemFree**) :</span><span class="sxs-lookup"><span data-stu-id="d4704-124">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocators (**CoTaskMemAlloc** and **CoTaskMemFree**):</span></span>

-   <span data-ttu-id="d4704-125">Les paramètres **in** sont alloués et libérés par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="d4704-125">**In** parameters are allocated and freed by the caller.</span></span>
-   <span data-ttu-id="d4704-126">Les paramètres **out** sont alloués par l’appelé et libérés par l’appelant à l’aide de **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="d4704-126">**Out** parameters are allocated by the callee and freed by the caller using **CoTaskMem**.</span></span>
-   <span data-ttu-id="d4704-127">Les paramètres **in/out** sont alloués par l’appelant, libérés et réalloués par l’appelé, et libérés au final par l’appelant, à l’aide de **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="d4704-127">**In/out** parameters are allocated by the caller, freed and reallocated by the callee, and ultimately freed by the caller, using **CoTaskMem**.</span></span>

<span data-ttu-id="d4704-128">Toutes les fonctions NAP pour libérer de la mémoire libèrent également tous les pointeurs incorporés.</span><span class="sxs-lookup"><span data-stu-id="d4704-128">All NAP functions for freeing memory also free all embedded pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4704-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d4704-129">Requirements</span></span>



| <span data-ttu-id="d4704-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d4704-130">Requirement</span></span> | <span data-ttu-id="d4704-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4704-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d4704-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d4704-132">Minimum supported client</span></span><br/> | <span data-ttu-id="d4704-133">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d4704-133">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="d4704-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d4704-134">Minimum supported server</span></span><br/> | <span data-ttu-id="d4704-135">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d4704-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d4704-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="d4704-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4704-137"><dt>NapUtil. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4704-137"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="d4704-138">DLL</span><span class="sxs-lookup"><span data-stu-id="d4704-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4704-139"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4704-139"><dt>Qutil.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4704-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d4704-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4704-141">**FreeCountedString**</span><span class="sxs-lookup"><span data-stu-id="d4704-141">**FreeCountedString**</span></span>](freecountedstring-func.md)
</dt> </dl>

 

 





