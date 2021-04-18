---
description: Définit l’affectation de jeux d’UC par défaut pour les threads dans le processus spécifié. Les threads créés, qui n’ont pas d’ensembles d’UC définis explicitement à l’aide de SetThreadSelectedCpuSets, héritent automatiquement des jeux spécifiés par SetProcessDefaultCpuSets.
ms.assetid: 7A510A8D-B06C-4B7B-9A87-BCFE0DE4D17B
title: SetProcessDefaultCpuSets, fonction (Processthreadapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetProcessDefaultCpuSets
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
- KernelBase.dll
ms.openlocfilehash: 7998b20815529b41c5e29204c0ef50fbc15e6288
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519890"
---
# <a name="setprocessdefaultcpusets-function"></a><span data-ttu-id="969af-104">SetProcessDefaultCpuSets fonction)</span><span class="sxs-lookup"><span data-stu-id="969af-104">SetProcessDefaultCpuSets function</span></span>

<span data-ttu-id="969af-105">Définit l’affectation de jeux d’UC par défaut pour les threads dans le processus spécifié.</span><span class="sxs-lookup"><span data-stu-id="969af-105">Sets the default CPU Sets assignment for threads in the specified process.</span></span> <span data-ttu-id="969af-106">Les threads créés, qui n’ont pas d’ensembles d’UC définis explicitement à l’aide de [**SetThreadSelectedCpuSets**](setthreadselectedcpusets.md), héritent automatiquement des jeux spécifiés par **SetProcessDefaultCpuSets** .</span><span class="sxs-lookup"><span data-stu-id="969af-106">Threads that are created, which don’t have CPU Sets explicitly set using [**SetThreadSelectedCpuSets**](setthreadselectedcpusets.md), will inherit the sets specified by **SetProcessDefaultCpuSets** automatically.</span></span>

## <a name="syntax"></a><span data-ttu-id="969af-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="969af-107">Syntax</span></span>


```C++
BOOL WINAPI SetProcessDefaultCpuSets(
  _In_     HANDLE Process,
  _In_opt_ ULONG  CpuSetIds,
  _In_     ULONG  CpuSetIdCound
);
```



## <a name="parameters"></a><span data-ttu-id="969af-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="969af-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="969af-109">*Processus* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="969af-109">*Process* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="969af-110">Spécifie le processus pour lequel définir les ensembles d’UC par défaut.</span><span class="sxs-lookup"><span data-stu-id="969af-110">Specifies the process for which to set the default CPU Sets.</span></span> <span data-ttu-id="969af-111">Ce descripteur doit avoir le droit de définir le processus d' \_ \_ \_ accès limité aux informations.</span><span class="sxs-lookup"><span data-stu-id="969af-111">This handle must have the PROCESS\_SET\_LIMITED\_INFORMATION access right.</span></span> <span data-ttu-id="969af-112">La valeur retournée par [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) peut également être spécifiée ici.</span><span class="sxs-lookup"><span data-stu-id="969af-112">The value returned by [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) can also be specified here.</span></span>

</dd> <dt>

<span data-ttu-id="969af-113">*CpuSetIds* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="969af-113">*CpuSetIds* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="969af-114">Spécifie la liste des ID de jeu d’UC à définir en tant qu’ensemble d’UC de processus par défaut.</span><span class="sxs-lookup"><span data-stu-id="969af-114">Specifies the list of CPU Set IDs to set as the process default CPU set.</span></span> <span data-ttu-id="969af-115">Si la valeur est NULL, **SetProcessDefaultCpuSets** efface toutes les affectations.</span><span class="sxs-lookup"><span data-stu-id="969af-115">If this is NULL, the **SetProcessDefaultCpuSets** clears out any assignment.</span></span>

</dd> <dt>

<span data-ttu-id="969af-116">*CpuSetIdCound* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="969af-116">*CpuSetIdCound* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="969af-117">Spécifie le nombre d’ID dans la liste passée dans l’argument **CpuSetIds** .</span><span class="sxs-lookup"><span data-stu-id="969af-117">Specifies the number of IDs in the list passed in the **CpuSetIds** argument.</span></span> <span data-ttu-id="969af-118">Si cette valeur est NULL, la valeur doit être 0.</span><span class="sxs-lookup"><span data-stu-id="969af-118">If that value is NULL, this should be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="969af-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="969af-119">Return value</span></span>

<span data-ttu-id="969af-120">Cette fonction ne peut pas échouer quand des paramètres valides sont passés.</span><span class="sxs-lookup"><span data-stu-id="969af-120">This function cannot fail when passed valid parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="969af-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="969af-121">Requirements</span></span>



| <span data-ttu-id="969af-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="969af-122">Requirement</span></span> | <span data-ttu-id="969af-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="969af-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="969af-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="969af-124">Minimum supported client</span></span><br/> | <span data-ttu-id="969af-125">Applications Windows 10 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="969af-125">Windows 10 \[desktop apps \| UWP apps\]</span></span><br/>                                            |
| <span data-ttu-id="969af-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="969af-126">Minimum supported server</span></span><br/> | <span data-ttu-id="969af-127">Applications de bureau Windows Server 2016 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="969af-127">Windows Server 2016 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="969af-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="969af-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="969af-129"><dt>Processthreadsapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="969af-129"><dt>Processthreadsapi.h</dt></span></span> </dl> |
| <span data-ttu-id="969af-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="969af-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="969af-131"><dt>Windows. h</dt></span><span class="sxs-lookup"><span data-stu-id="969af-131"><dt>Windows.h</dt></span></span> </dl>          |
| <span data-ttu-id="969af-132">DLL</span><span class="sxs-lookup"><span data-stu-id="969af-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="969af-133"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="969af-133"><dt>Kernel32.dll</dt></span></span> </dl>       |



 

 
