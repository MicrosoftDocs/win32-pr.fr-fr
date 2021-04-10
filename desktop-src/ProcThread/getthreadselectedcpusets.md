---
description: Retourne l’attribution de jeu d’UC explicite du thread spécifié, si une affectation a été définie à l’aide de l’API SetThreadSelectedCpuSets. Si aucune assignation explicite n’est définie, RequiredIdCount a la valeur 0 et la fonction retourne la valeur TRUE.
ms.assetid: 9ACF72F8-A64C-4FFF-B340-C920E80238CA
title: GetThreadSelectedCpuSets, fonction (Processthreadapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetThreadSelectedCpuSets
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
- KernelBase.dll
ms.openlocfilehash: 26530b1fbb9694ed7ecc8c4e457ad023e971a470
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034512"
---
# <a name="getthreadselectedcpusets-function"></a><span data-ttu-id="0b1cd-104">GetThreadSelectedCpuSets fonction)</span><span class="sxs-lookup"><span data-stu-id="0b1cd-104">GetThreadSelectedCpuSets function</span></span>

<span data-ttu-id="0b1cd-105">Retourne l’attribution de jeu d’UC explicite du thread spécifié, si une affectation a été définie à l’aide de l’API [**SetThreadSelectedCpuSets**](setthreadselectedcpusets.md) .</span><span class="sxs-lookup"><span data-stu-id="0b1cd-105">Returns the explicit CPU Set assignment of the specified thread, if any assignment was set using the [**SetThreadSelectedCpuSets**](setthreadselectedcpusets.md) API.</span></span> <span data-ttu-id="0b1cd-106">Si aucune assignation explicite n’est définie, **RequiredIdCount** a la valeur 0 et la fonction retourne la valeur true.</span><span class="sxs-lookup"><span data-stu-id="0b1cd-106">If no explicit assignment is set, **RequiredIdCount** is set to 0 and the function returns TRUE.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b1cd-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0b1cd-107">Syntax</span></span>


```C++
BOOL WINAPI GetThreadSelectedCpuSets(
  _In_      HANDLE Thread,
  _Out_opt_ PULONG CpuSetIds,
  _In_      ULONG  CpuSetIdCount,
  _Out_     PULONG RequiredIdCount
);
```



## <a name="parameters"></a><span data-ttu-id="0b1cd-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0b1cd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b1cd-109">*Thread* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0b1cd-109">*Thread* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b1cd-110">Spécifie le thread pour lequel interroger les ensembles d’UC sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="0b1cd-110">Specifies the thread for which to query the selected CPU Sets.</span></span> <span data-ttu-id="0b1cd-111">Ce descripteur doit avoir \_ le \_ \_ droit d’accès aux informations limitées du thread.</span><span class="sxs-lookup"><span data-stu-id="0b1cd-111">This handle must have the THREAD\_QUERY\_LIMITED\_INFORMATION access right.</span></span> <span data-ttu-id="0b1cd-112">La valeur retournée par [**GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) peut également être spécifiée ici.</span><span class="sxs-lookup"><span data-stu-id="0b1cd-112">The value returned by [**GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) can also be specified here.</span></span>

</dd> <dt>

<span data-ttu-id="0b1cd-113">*CpuSetIds* \[ out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="0b1cd-113">*CpuSetIds* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0b1cd-114">Spécifie une mémoire tampon facultative pour récupérer la liste des identificateurs d’ensembles d’UC.</span><span class="sxs-lookup"><span data-stu-id="0b1cd-114">Specifies an optional buffer to retrieve the list of CPU Set identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="0b1cd-115">*CpuSetIdCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0b1cd-115">*CpuSetIdCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b1cd-116">Spécifie la capacité de la mémoire tampon spécifiée dans **CpuSetIds**.</span><span class="sxs-lookup"><span data-stu-id="0b1cd-116">Specifies the capacity of the buffer specified in **CpuSetIds**.</span></span> <span data-ttu-id="0b1cd-117">Si la mémoire tampon est NULL, cette valeur doit être 0.</span><span class="sxs-lookup"><span data-stu-id="0b1cd-117">If the buffer is NULL, this must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="0b1cd-118">*RequiredIdCount* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="0b1cd-118">*RequiredIdCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0b1cd-119">Spécifie la capacité requise de la mémoire tampon pour contenir l’intégralité de la liste des ensembles d’UC sélectionnés du thread.</span><span class="sxs-lookup"><span data-stu-id="0b1cd-119">Specifies the required capacity of the buffer to hold the entire list of thread selected CPU Sets.</span></span> <span data-ttu-id="0b1cd-120">En cas de retour réussi, spécifie le nombre d’ID remplis dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="0b1cd-120">On successful return, this specifies the number of IDs filled into the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b1cd-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0b1cd-121">Return value</span></span>

<span data-ttu-id="0b1cd-122">Cette API retourne TRUE en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="0b1cd-122">This API returns TRUE on success.</span></span> <span data-ttu-id="0b1cd-123">Si la mémoire tampon n’est pas assez grande, la valeur de **GetLastError** est une \_ mémoire tampon d’erreur insuffisante \_ .</span><span class="sxs-lookup"><span data-stu-id="0b1cd-123">If the buffer is not large enough, the **GetLastError** value is ERROR\_INSUFFICIENT\_BUFFER.</span></span> <span data-ttu-id="0b1cd-124">Cette API ne peut pas échouer quand des paramètres valides sont transmis et que la mémoire tampon de retour est suffisamment grande.</span><span class="sxs-lookup"><span data-stu-id="0b1cd-124">This API cannot fail when passed valid parameters and the return buffer is large enough.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b1cd-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0b1cd-125">Requirements</span></span>



| <span data-ttu-id="0b1cd-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0b1cd-126">Requirement</span></span> | <span data-ttu-id="0b1cd-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="0b1cd-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b1cd-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0b1cd-128">Minimum supported client</span></span><br/> | <span data-ttu-id="0b1cd-129">Applications Windows 10 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="0b1cd-129">Windows 10 \[desktop apps \| UWP apps\]</span></span><br/>                                            |
| <span data-ttu-id="0b1cd-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0b1cd-130">Minimum supported server</span></span><br/> | <span data-ttu-id="0b1cd-131">Applications de bureau Windows Server 2016 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="0b1cd-131">Windows Server 2016 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="0b1cd-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="0b1cd-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b1cd-133"><dt>Processthreadsapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b1cd-133"><dt>Processthreadsapi.h</dt></span></span> </dl> |
| <span data-ttu-id="0b1cd-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0b1cd-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="0b1cd-135"><dt>Windows. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b1cd-135"><dt>Windows.h</dt></span></span> </dl>          |
| <span data-ttu-id="0b1cd-136">DLL</span><span class="sxs-lookup"><span data-stu-id="0b1cd-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b1cd-137"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b1cd-137"><dt>Kernel32.dll</dt></span></span> </dl>       |



 

