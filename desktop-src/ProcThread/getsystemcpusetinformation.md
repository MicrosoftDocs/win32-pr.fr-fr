---
description: Permet à une application d’interroger les ensembles d’UC disponibles sur le système, ainsi que leur état actuel.
ms.assetid: 168B00AB-1B11-44A0-B548-903CA3F4BBDE
title: GetSystemCpuSetInformation, fonction (Processthreadapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetSystemCpuSetInformation
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
- KernelBase.dll
ms.openlocfilehash: d8ce490e3377e45a81b24523504d06941755de49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202855"
---
# <a name="getsystemcpusetinformation-function"></a><span data-ttu-id="2a4e5-103">GetSystemCpuSetInformation fonction)</span><span class="sxs-lookup"><span data-stu-id="2a4e5-103">GetSystemCpuSetInformation function</span></span>

<span data-ttu-id="2a4e5-104">Permet à une application d’interroger les ensembles d’UC disponibles sur le système, ainsi que leur état actuel.</span><span class="sxs-lookup"><span data-stu-id="2a4e5-104">Allows an application to query the available CPU Sets on the system, and their current state.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a4e5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2a4e5-105">Syntax</span></span>


```C++
BOOL WINAPI GetSystemCpuSetInformation(
  _Out_opt_  PSYSTEM_CPU_SET_INFORMATION  Information,
  _In_       ULONG                        BufferLength,
  _Out_      PULONG                       ReturnedLength,
  _In_opt_   HANDLE                       Process,
  _Reserved_ ULONG                        Flags
);
```



## <a name="parameters"></a><span data-ttu-id="2a4e5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2a4e5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a4e5-107">*Informations* \[ out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="2a4e5-107">*Information* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2a4e5-108">Pointeur vers une structure [**d' \_ \_ \_ informations de jeu d’UC système**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information) qui reçoit les données du jeu d’UC.</span><span class="sxs-lookup"><span data-stu-id="2a4e5-108">A pointer to a [**SYSTEM\_CPU\_SET\_INFORMATION**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information) structure that receives the CPU Set data.</span></span> <span data-ttu-id="2a4e5-109">Transmettez la valeur NULL avec une longueur de mémoire tampon de 0 pour déterminer la taille de mémoire tampon requise.</span><span class="sxs-lookup"><span data-stu-id="2a4e5-109">Pass NULL with a buffer length of 0 to determine the required buffer size.</span></span>

</dd> <dt>

<span data-ttu-id="2a4e5-110">*BufferLength* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2a4e5-110">*BufferLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a4e5-111">Longueur, en octets, de la mémoire tampon de sortie passée comme argument d’information.</span><span class="sxs-lookup"><span data-stu-id="2a4e5-111">The length, in bytes, of the output buffer passed as the Information argument.</span></span>

</dd> <dt>

<span data-ttu-id="2a4e5-112">*ReturnedLength* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="2a4e5-112">*ReturnedLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2a4e5-113">Longueur, en octets, des données valides dans la mémoire tampon de sortie si la mémoire tampon est suffisamment grande, ou la taille requise de la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="2a4e5-113">The length, in bytes, of the valid data in the output buffer if the buffer is large enough, or the required size of the output buffer.</span></span> <span data-ttu-id="2a4e5-114">Si aucun ensemble d’UC n’existe, cette valeur est 0.</span><span class="sxs-lookup"><span data-stu-id="2a4e5-114">If no CPU Sets exist, this value will be 0.</span></span>

</dd> <dt>

<span data-ttu-id="2a4e5-115">*Processus* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="2a4e5-115">*Process* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2a4e5-116">Handle facultatif d’un processus.</span><span class="sxs-lookup"><span data-stu-id="2a4e5-116">An optional handle to a process.</span></span> <span data-ttu-id="2a4e5-117">Ce processus est utilisé pour déterminer la valeur de l’indicateur **AllocatedToTargetProcess** dans la structure d’informations du jeu d' \_ UC système \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="2a4e5-117">This process is used to determine the value of the **AllocatedToTargetProcess** flag in the SYSTEM\_CPU\_SET\_INFORMATION structure.</span></span> <span data-ttu-id="2a4e5-118">Si un ensemble d’UC est alloué au processus spécifié, l’indicateur est défini.</span><span class="sxs-lookup"><span data-stu-id="2a4e5-118">If a CPU Set is allocated to the specified process, the flag is set.</span></span> <span data-ttu-id="2a4e5-119">Dans le cas contraire, il est clair.</span><span class="sxs-lookup"><span data-stu-id="2a4e5-119">Otherwise, it is clear.</span></span> <span data-ttu-id="2a4e5-120">Ce descripteur doit disposer du droit d’accès au processus \_ requête \_ sur les \_ informations limitées.</span><span class="sxs-lookup"><span data-stu-id="2a4e5-120">This handle must have the PROCESS\_QUERY\_LIMITED\_INFORMATION access right.</span></span> <span data-ttu-id="2a4e5-121">La valeur retournée par [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) peut également être spécifiée ici.</span><span class="sxs-lookup"><span data-stu-id="2a4e5-121">The value returned by [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) may also be specified here.</span></span>

</dd> <dt>

<span data-ttu-id="2a4e5-122">*Indicateurs*</span><span class="sxs-lookup"><span data-stu-id="2a4e5-122">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="2a4e5-123">Réservé, doit avoir la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="2a4e5-123">Reserved, must be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a4e5-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2a4e5-124">Return value</span></span>

<span data-ttu-id="2a4e5-125">Si l’API fonctionne correctement, elle retourne TRUE.</span><span class="sxs-lookup"><span data-stu-id="2a4e5-125">If the API succeeds it returns TRUE.</span></span> <span data-ttu-id="2a4e5-126">En cas d’échec, la raison de l’erreur est disponible par le biais de **GetLastError**.</span><span class="sxs-lookup"><span data-stu-id="2a4e5-126">If it fails, the error reason is available through **GetLastError**.</span></span> <span data-ttu-id="2a4e5-127">Si la mémoire tampon d’informations était NULL ou n’est pas assez grande, l’erreur de code d’erreur « \_ mémoire tampon insuffisante » \_ est retournée.</span><span class="sxs-lookup"><span data-stu-id="2a4e5-127">If the Information buffer was NULL or not large enough, the error code ERROR\_INSUFFICIENT\_BUFFER is returned.</span></span> <span data-ttu-id="2a4e5-128">Cette API ne peut pas échouer quand des paramètres valides ont été transmis et une mémoire tampon suffisamment grande pour contenir toutes les données de retour.</span><span class="sxs-lookup"><span data-stu-id="2a4e5-128">This API cannot fail when passed valid parameters and a buffer that is large enough to hold all of the return data.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a4e5-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2a4e5-129">Requirements</span></span>



| <span data-ttu-id="2a4e5-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2a4e5-130">Requirement</span></span> | <span data-ttu-id="2a4e5-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a4e5-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a4e5-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2a4e5-132">Minimum supported client</span></span><br/> | <span data-ttu-id="2a4e5-133">Applications Windows 10 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="2a4e5-133">Windows 10 \[desktop apps \| UWP apps\]</span></span><br/>                                            |
| <span data-ttu-id="2a4e5-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2a4e5-134">Minimum supported server</span></span><br/> | <span data-ttu-id="2a4e5-135">Applications de bureau Windows Server 2016 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="2a4e5-135">Windows Server 2016 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="2a4e5-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="2a4e5-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a4e5-137"><dt>Processthreadsapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a4e5-137"><dt>Processthreadsapi.h</dt></span></span> </dl> |
| <span data-ttu-id="2a4e5-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2a4e5-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="2a4e5-139"><dt>Windows. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a4e5-139"><dt>Windows.h</dt></span></span> </dl>          |
| <span data-ttu-id="2a4e5-140">DLL</span><span class="sxs-lookup"><span data-stu-id="2a4e5-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2a4e5-141"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2a4e5-141"><dt>Kernel32.dll</dt></span></span> </dl>       |



 

