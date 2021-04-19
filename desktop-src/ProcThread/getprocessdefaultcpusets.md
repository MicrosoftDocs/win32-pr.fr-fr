---
description: Récupère la liste des ensembles d’UC dans l’ensemble de processus par défaut qui a été défini par SetProcessDefaultCpuSets. Si aucun jeu d’UC par défaut n’est défini pour un processus donné, RequiredIdCount a la valeur 0 et la fonction est exécutée correctement.
ms.assetid: 85DC5331-9EC0-4603-94FD-B49E725301B1
title: GetProcessDefaultCpuSets, fonction (Processthreadapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProcessDefaultCpuSets
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
- KernelBase.dll
ms.openlocfilehash: a5bd7c27b76efbbac923317837ac82b3a6700197
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518677"
---
# <a name="getprocessdefaultcpusets-function"></a><span data-ttu-id="487e4-104">GetProcessDefaultCpuSets fonction)</span><span class="sxs-lookup"><span data-stu-id="487e4-104">GetProcessDefaultCpuSets function</span></span>

<span data-ttu-id="487e4-105">Récupère la liste des ensembles d’UC dans l’ensemble de processus par défaut qui a été défini par [**SetProcessDefaultCpuSets**](setprocessdefaultcpusets.md).</span><span class="sxs-lookup"><span data-stu-id="487e4-105">Retrieves the list of CPU Sets in the process default set that was set by [**SetProcessDefaultCpuSets**](setprocessdefaultcpusets.md).</span></span> <span data-ttu-id="487e4-106">Si aucun jeu d’UC par défaut n’est défini pour un processus donné, **RequiredIdCount** a la valeur 0 et la fonction est exécutée correctement.</span><span class="sxs-lookup"><span data-stu-id="487e4-106">If no default CPU Sets are set for a given process, then the **RequiredIdCount** is set to 0 and the function succeeds.</span></span>

## <a name="syntax"></a><span data-ttu-id="487e4-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="487e4-107">Syntax</span></span>


```C++
BOOL WINAPI GetProcessDefaultCpuSets(
  _In_      HANDLE Process,
  _Out_opt_ PULONG CpuSetIds,
  _In_      ULONG  CpuSetIdCount,
  _Out_     PULONG RequiredIdCount
);
```



## <a name="parameters"></a><span data-ttu-id="487e4-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="487e4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="487e4-109">*Processus* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="487e4-109">*Process* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="487e4-110">Spécifie un handle de processus pour le processus à interroger.</span><span class="sxs-lookup"><span data-stu-id="487e4-110">Specifies a process handle for the process to query.</span></span> <span data-ttu-id="487e4-111">Ce descripteur doit disposer du droit d’accès au processus \_ requête \_ sur les \_ informations limitées.</span><span class="sxs-lookup"><span data-stu-id="487e4-111">This handle must have the PROCESS\_QUERY\_LIMITED\_INFORMATION access right.</span></span> <span data-ttu-id="487e4-112">La valeur retournée par [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) peut également être spécifiée ici.</span><span class="sxs-lookup"><span data-stu-id="487e4-112">The value returned by [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) can also be specified here.</span></span>

</dd> <dt>

<span data-ttu-id="487e4-113">*CpuSetIds* \[ out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="487e4-113">*CpuSetIds* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="487e4-114">Spécifie une mémoire tampon facultative pour récupérer la liste des identificateurs d’ensembles d’UC.</span><span class="sxs-lookup"><span data-stu-id="487e4-114">Specifies an optional buffer to retrieve the list of CPU Set identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="487e4-115">*CpuSetIdCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="487e4-115">*CpuSetIdCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="487e4-116">Spécifie la capacité de la mémoire tampon spécifiée dans **CpuSetIds**.</span><span class="sxs-lookup"><span data-stu-id="487e4-116">Specifies the capacity of the buffer specified in **CpuSetIds**.</span></span> <span data-ttu-id="487e4-117">Si la mémoire tampon est NULL, cette valeur doit être 0.</span><span class="sxs-lookup"><span data-stu-id="487e4-117">If the buffer is NULL, this must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="487e4-118">*RequiredIdCount* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="487e4-118">*RequiredIdCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="487e4-119">Spécifie la capacité requise de la mémoire tampon pour contenir l’intégralité de la liste des ensembles d’UC par défaut du processus.</span><span class="sxs-lookup"><span data-stu-id="487e4-119">Specifies the required capacity of the buffer to hold the entire list of process default CPU Sets.</span></span> <span data-ttu-id="487e4-120">En cas de retour réussi, spécifie le nombre d’ID remplis dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="487e4-120">On successful return, this specifies the number of IDs filled into the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="487e4-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="487e4-121">Return value</span></span>

<span data-ttu-id="487e4-122">Cette API retourne TRUE en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="487e4-122">This API returns TRUE on success.</span></span> <span data-ttu-id="487e4-123">Si la mémoire tampon n’est pas assez grande, l’API retourne FALSe et la valeur de **GetLastError** est une \_ mémoire tampon d’erreur insuffisante \_ .</span><span class="sxs-lookup"><span data-stu-id="487e4-123">If the buffer is not large enough the API returns FALSE, and the **GetLastError** value is ERROR\_INSUFFICIENT\_BUFFER.</span></span> <span data-ttu-id="487e4-124">Cette API ne peut pas échouer quand des paramètres valides sont transmis et que la mémoire tampon de retour est suffisamment grande.</span><span class="sxs-lookup"><span data-stu-id="487e4-124">This API cannot fail when passed valid parameters and the return buffer is large enough.</span></span>

## <a name="requirements"></a><span data-ttu-id="487e4-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="487e4-125">Requirements</span></span>



| <span data-ttu-id="487e4-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="487e4-126">Requirement</span></span> | <span data-ttu-id="487e4-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="487e4-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="487e4-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="487e4-128">Minimum supported client</span></span><br/> | <span data-ttu-id="487e4-129">Applications Windows 10 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="487e4-129">Windows 10 \[desktop apps \| UWP apps\]</span></span><br/>                                            |
| <span data-ttu-id="487e4-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="487e4-130">Minimum supported server</span></span><br/> | <span data-ttu-id="487e4-131">Applications de bureau Windows Server 2016 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="487e4-131">Windows Server 2016 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="487e4-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="487e4-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="487e4-133"><dt>Processthreadsapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="487e4-133"><dt>Processthreadsapi.h</dt></span></span> </dl> |
| <span data-ttu-id="487e4-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="487e4-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="487e4-135"><dt>Windows. h</dt></span><span class="sxs-lookup"><span data-stu-id="487e4-135"><dt>Windows.h</dt></span></span> </dl>          |
| <span data-ttu-id="487e4-136">DLL</span><span class="sxs-lookup"><span data-stu-id="487e4-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="487e4-137"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="487e4-137"><dt>Kernel32.dll</dt></span></span> </dl>       |



 

