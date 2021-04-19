---
description: Récupère les informations système spécifiées.
ms.assetid: c91b9a35-ca2b-4d81-973d-fe709144df90
title: ZwQuerySystemInformation fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ZwQuerySystemInformation
api_type:
- DllExport
api_location:
- Ntdll.dll
- ntoskrnl.exe
ms.openlocfilehash: 2e516b12e5109470c1ddb86ea6a665ca29f138b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530553"
---
# <a name="zwquerysysteminformation-function"></a><span data-ttu-id="62a4c-103">ZwQuerySystemInformation fonction)</span><span class="sxs-lookup"><span data-stu-id="62a4c-103">ZwQuerySystemInformation function</span></span>

<span data-ttu-id="62a4c-104">\[**ZwQuerySystemInformation** n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="62a4c-104">\[**ZwQuerySystemInformation** is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="62a4c-105">Utilisez plutôt les autres fonctions indiquées dans cette rubrique.\]</span><span class="sxs-lookup"><span data-stu-id="62a4c-105">Instead, use the alternate functions listed in this topic.\]</span></span>

<span data-ttu-id="62a4c-106">Récupère les informations système spécifiées.</span><span class="sxs-lookup"><span data-stu-id="62a4c-106">Retrieves the specified system information.</span></span>

## <a name="syntax"></a><span data-ttu-id="62a4c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="62a4c-107">Syntax</span></span>


```C++
NTSTATUS WINAPI ZwQuerySystemInformation(
  _In_      SYSTEM_INFORMATION_CLASS SystemInformationClass,
  _Inout_   PVOID                    SystemInformation,
  _In_      ULONG                    SystemInformationLength,
  _Out_opt_ PULONG                   ReturnLength
);
```



## <a name="parameters"></a><span data-ttu-id="62a4c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="62a4c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62a4c-109">*SystemInformationClass* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="62a4c-109">*SystemInformationClass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62a4c-110">Type d’informations système à récupérer.</span><span class="sxs-lookup"><span data-stu-id="62a4c-110">The type of system information to be retrieved.</span></span> <span data-ttu-id="62a4c-111">Ce paramètre peut avoir l’une des valeurs suivantes du type d’énumération de **\_ \_ classe d’informations système** .</span><span class="sxs-lookup"><span data-stu-id="62a4c-111">This parameter can be one of the following values from the **SYSTEM\_INFORMATION\_CLASS** enumeration type.</span></span>

<dt>

<span id="SystemBasicInformation"></span><span id="systembasicinformation"></span><span id="SYSTEMBASICINFORMATION"></span>

<span data-ttu-id="62a4c-112"><span id="SystemBasicInformation"></span><span id="systembasicinformation"></span><span id="SYSTEMBASICINFORMATION"></span>**SystemBasicInformation**</span><span class="sxs-lookup"><span data-stu-id="62a4c-112"><span id="SystemBasicInformation"></span><span id="systembasicinformation"></span><span id="SYSTEMBASICINFORMATION"></span>**SystemBasicInformation**</span></span>


</dt> <dd>

<span data-ttu-id="62a4c-113">Nombre de processeurs dans le système dans une structure d' **\_ \_ information de base du système** .</span><span class="sxs-lookup"><span data-stu-id="62a4c-113">The number of processors in the system in a **SYSTEM\_BASIC\_INFORMATION** structure.</span></span> <span data-ttu-id="62a4c-114">Utilisez à la place la fonction [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) .</span><span class="sxs-lookup"><span data-stu-id="62a4c-114">Use the [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) function instead.</span></span>

</dd> <dt>

<span id="SystemPerformanceInformation"></span><span id="systemperformanceinformation"></span><span id="SYSTEMPERFORMANCEINFORMATION"></span>

<span data-ttu-id="62a4c-115"><span id="SystemPerformanceInformation"></span><span id="systemperformanceinformation"></span><span id="SYSTEMPERFORMANCEINFORMATION"></span>**SystemPerformanceInformation**</span><span class="sxs-lookup"><span data-stu-id="62a4c-115"><span id="SystemPerformanceInformation"></span><span id="systemperformanceinformation"></span><span id="SYSTEMPERFORMANCEINFORMATION"></span>**SystemPerformanceInformation**</span></span>


</dt> <dd>

<span data-ttu-id="62a4c-116">Structure d' **\_ \_ informations sur les performances du système** opaque qui peut être utilisée pour générer une valeur de départ imprévisible pour un générateur de nombres aléatoires.</span><span class="sxs-lookup"><span data-stu-id="62a4c-116">An opaque **SYSTEM\_PERFORMANCE\_INFORMATION** structure that can be used to generate an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="62a4c-117">Utilisez à la place la fonction [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) .</span><span class="sxs-lookup"><span data-stu-id="62a4c-117">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead.</span></span>

</dd> <dt>

<span id="SystemTimeOfDayInformation"></span><span id="systemtimeofdayinformation"></span><span id="SYSTEMTIMEOFDAYINFORMATION"></span>

<span data-ttu-id="62a4c-118"><span id="SystemTimeOfDayInformation"></span><span id="systemtimeofdayinformation"></span><span id="SYSTEMTIMEOFDAYINFORMATION"></span>**SystemTimeOfDayInformation**</span><span class="sxs-lookup"><span data-stu-id="62a4c-118"><span id="SystemTimeOfDayInformation"></span><span id="systemtimeofdayinformation"></span><span id="SYSTEMTIMEOFDAYINFORMATION"></span>**SystemTimeOfDayInformation**</span></span>


</dt> <dd>

<span data-ttu-id="62a4c-119">Structure d' **\_ \_ informations TimeOfDay du système** opaque qui peut être utilisée pour générer une valeur de départ imprévisible pour un générateur de nombres aléatoires.</span><span class="sxs-lookup"><span data-stu-id="62a4c-119">An opaque **SYSTEM\_TIMEOFDAY\_INFORMATION** structure that can be used to generate an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="62a4c-120">Utilisez à la place la fonction [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) .</span><span class="sxs-lookup"><span data-stu-id="62a4c-120">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead.</span></span>

</dd> <dt>

<span id="SystemProcessInformation"></span><span id="systemprocessinformation"></span><span id="SYSTEMPROCESSINFORMATION"></span>

<span data-ttu-id="62a4c-121"><span id="SystemProcessInformation"></span><span id="systemprocessinformation"></span><span id="SYSTEMPROCESSINFORMATION"></span>**SystemProcessInformation**</span><span class="sxs-lookup"><span data-stu-id="62a4c-121"><span id="SystemProcessInformation"></span><span id="systemprocessinformation"></span><span id="SYSTEMPROCESSINFORMATION"></span>**SystemProcessInformation**</span></span>


</dt> <dd>

<span data-ttu-id="62a4c-122">Tableau de structures **d' \_ \_ informations de processus système** , un pour chaque processus s’exécutant dans le système.</span><span class="sxs-lookup"><span data-stu-id="62a4c-122">An array of **SYSTEM\_PROCESS\_INFORMATION** structures, one for each process running in the system.</span></span>

<span data-ttu-id="62a4c-123">Ces structures contiennent des informations sur l’utilisation des ressources de chaque processus, y compris le nombre de handles utilisés par le processus, l’utilisation du fichier de page de pic et le nombre de pages de mémoire allouées par le processus.</span><span class="sxs-lookup"><span data-stu-id="62a4c-123">These structures contain information about the resource usage of each process, including the number of handles used by the process, the peak page-file usage, and the number of memory pages that the process has allocated.</span></span>

</dd> <dt>

<span id="SystemProcessorPerformanceInformation"></span><span id="systemprocessorperformanceinformation"></span><span id="SYSTEMPROCESSORPERFORMANCEINFORMATION"></span>

<span data-ttu-id="62a4c-124"><span id="SystemProcessorPerformanceInformation"></span><span id="systemprocessorperformanceinformation"></span><span id="SYSTEMPROCESSORPERFORMANCEINFORMATION"></span>**SystemProcessorPerformanceInformation**</span><span class="sxs-lookup"><span data-stu-id="62a4c-124"><span id="SystemProcessorPerformanceInformation"></span><span id="systemprocessorperformanceinformation"></span><span id="SYSTEMPROCESSORPERFORMANCEINFORMATION"></span>**SystemProcessorPerformanceInformation**</span></span>


</dt> <dd>

<span data-ttu-id="62a4c-125">Tableau des structures **d' \_ \_ \_ informations sur les performances du processeur système** , une pour chaque processeur installé dans le système.</span><span class="sxs-lookup"><span data-stu-id="62a4c-125">An array of **SYSTEM\_PROCESSOR\_PERFORMANCE\_INFORMATION** structures, one for each processor installed in the system.</span></span>

</dd> <dt>

<span id="SystemInterruptInformation"></span><span id="systeminterruptinformation"></span><span id="SYSTEMINTERRUPTINFORMATION"></span>

<span data-ttu-id="62a4c-126"><span id="SystemInterruptInformation"></span><span id="systeminterruptinformation"></span><span id="SYSTEMINTERRUPTINFORMATION"></span>**SystemInterruptInformation**</span><span class="sxs-lookup"><span data-stu-id="62a4c-126"><span id="SystemInterruptInformation"></span><span id="systeminterruptinformation"></span><span id="SYSTEMINTERRUPTINFORMATION"></span>**SystemInterruptInformation**</span></span>


</dt> <dd>

<span data-ttu-id="62a4c-127">Structure d' **\_ \_ informations d’interruption système** opaque qui peut être utilisée pour générer une valeur de départ imprévisible pour un générateur de nombres aléatoires.</span><span class="sxs-lookup"><span data-stu-id="62a4c-127">An opaque **SYSTEM\_INTERRUPT\_INFORMATION** structure that can be used to generate an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="62a4c-128">Utilisez à la place la fonction [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) .</span><span class="sxs-lookup"><span data-stu-id="62a4c-128">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead.</span></span>

</dd> <dt>

<span id="SystemExceptionInformation"></span><span id="systemexceptioninformation"></span><span id="SYSTEMEXCEPTIONINFORMATION"></span>

<span data-ttu-id="62a4c-129"><span id="SystemExceptionInformation"></span><span id="systemexceptioninformation"></span><span id="SYSTEMEXCEPTIONINFORMATION"></span>**SystemExceptionInformation**</span><span class="sxs-lookup"><span data-stu-id="62a4c-129"><span id="SystemExceptionInformation"></span><span id="systemexceptioninformation"></span><span id="SYSTEMEXCEPTIONINFORMATION"></span>**SystemExceptionInformation**</span></span>


</dt> <dd>

<span data-ttu-id="62a4c-130">Structure d' **\_ \_ informations d’exception système** opaque qui peut être utilisée pour générer une valeur de départ imprévisible pour un générateur de nombres aléatoires.</span><span class="sxs-lookup"><span data-stu-id="62a4c-130">An opaque **SYSTEM\_EXCEPTION\_INFORMATION** structure that can be used to generate an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="62a4c-131">Utilisez à la place la fonction [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) .</span><span class="sxs-lookup"><span data-stu-id="62a4c-131">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead.</span></span>

</dd> <dt>

<span id="SystemRegistryQuotaInformation"></span><span id="systemregistryquotainformation"></span><span id="SYSTEMREGISTRYQUOTAINFORMATION"></span>

<span data-ttu-id="62a4c-132"><span id="SystemRegistryQuotaInformation"></span><span id="systemregistryquotainformation"></span><span id="SYSTEMREGISTRYQUOTAINFORMATION"></span>**SystemRegistryQuotaInformation**</span><span class="sxs-lookup"><span data-stu-id="62a4c-132"><span id="SystemRegistryQuotaInformation"></span><span id="systemregistryquotainformation"></span><span id="SYSTEMREGISTRYQUOTAINFORMATION"></span>**SystemRegistryQuotaInformation**</span></span>


</dt> <dd>

<span data-ttu-id="62a4c-133">Structure **d' \_ \_ \_ informations de quota du Registre système** .</span><span class="sxs-lookup"><span data-stu-id="62a4c-133">A **SYSTEM\_REGISTRY\_QUOTA\_INFORMATION** structure.</span></span>

</dd> <dt>

<span id="SystemLookasideInformation"></span><span id="systemlookasideinformation"></span><span id="SYSTEMLOOKASIDEINFORMATION"></span>

<span data-ttu-id="62a4c-134"><span id="SystemLookasideInformation"></span><span id="systemlookasideinformation"></span><span id="SYSTEMLOOKASIDEINFORMATION"></span>**SystemLookasideInformation**</span><span class="sxs-lookup"><span data-stu-id="62a4c-134"><span id="SystemLookasideInformation"></span><span id="systemlookasideinformation"></span><span id="SYSTEMLOOKASIDEINFORMATION"></span>**SystemLookasideInformation**</span></span>


</dt> <dd>

<span data-ttu-id="62a4c-135">Structure d' **\_ \_ information de système** non opaque qui peut être utilisée pour générer une valeur de départ imprévisible pour un générateur de nombres aléatoires.</span><span class="sxs-lookup"><span data-stu-id="62a4c-135">An opaque **SYSTEM\_LOOKASIDE\_INFORMATION** structure that can be used to generate an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="62a4c-136">Utilisez à la place la fonction [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) .</span><span class="sxs-lookup"><span data-stu-id="62a4c-136">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="62a4c-137">*SystemInformation* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="62a4c-137">*SystemInformation* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="62a4c-138">Pointeur vers une mémoire tampon qui reçoit les informations demandées.</span><span class="sxs-lookup"><span data-stu-id="62a4c-138">A pointer to a buffer that receives the requested information.</span></span> <span data-ttu-id="62a4c-139">La taille et la structure de ces informations varient en fonction de la valeur du paramètre *SystemInformationClass* , comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="62a4c-139">The size and structure of this information varies depending on the value of the *SystemInformationClass* parameter, as indicated in the following table.</span></span>

<dt>

<span id="SYSTEM_BASIC_INFORMATION"></span><span id="system_basic_information"></span>

<span data-ttu-id="62a4c-140"><span id="SYSTEM_BASIC_INFORMATION"></span><span id="system_basic_information"></span>**\_informations de base sur le système \_**</span><span class="sxs-lookup"><span data-stu-id="62a4c-140"><span id="SYSTEM_BASIC_INFORMATION"></span><span id="system_basic_information"></span>**SYSTEM\_BASIC\_INFORMATION**</span></span>


</dt> <dd>

<span data-ttu-id="62a4c-141">Lorsque le paramètre *SystemInformationClass* est **SystemBasicInformation**, la mémoire tampon vers laquelle pointe le paramètre *SystemInformation* doit être suffisamment grande pour contenir une structure d' **\_ \_ information de base du système** unique ayant la disposition suivante :</span><span class="sxs-lookup"><span data-stu-id="62a4c-141">When the *SystemInformationClass* parameter is **SystemBasicInformation**, the buffer pointed to by the *SystemInformation* parameter should be large enough to hold a single **SYSTEM\_BASIC\_INFORMATION** structure having the following layout:</span></span>

``` syntax
typedef struct _SYSTEM_BASIC_INFORMATION {
    BYTE Reserved1[24];
    PVOID Reserved2[4];
    CCHAR NumberOfProcessors;
} SYSTEM_BASIC_INFORMATION;
```

<span data-ttu-id="62a4c-142">Le membre **NumberOfProcessors** contient le nombre de processeurs présents dans le système.</span><span class="sxs-lookup"><span data-stu-id="62a4c-142">The **NumberOfProcessors** member contains the number of processors present in the system.</span></span> <span data-ttu-id="62a4c-143">Utilisez [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) à la place pour récupérer ces informations.</span><span class="sxs-lookup"><span data-stu-id="62a4c-143">Use [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) instead to retrieve this information.</span></span>

<span data-ttu-id="62a4c-144">Les autres membres de la structure sont réservés à un usage interne par le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="62a4c-144">The other members of the structure are reserved for internal use by the operating system.</span></span>

</dd> <dt>

<span id="SYSTEM_PERFORMANCE_INFORMATION"></span><span id="system_performance_information"></span>

<span data-ttu-id="62a4c-145"><span id="SYSTEM_PERFORMANCE_INFORMATION"></span><span id="system_performance_information"></span>**\_informations sur les performances du système \_**</span><span class="sxs-lookup"><span data-stu-id="62a4c-145"><span id="SYSTEM_PERFORMANCE_INFORMATION"></span><span id="system_performance_information"></span>**SYSTEM\_PERFORMANCE\_INFORMATION**</span></span>


</dt> <dd>

<span data-ttu-id="62a4c-146">Lorsque le paramètre *SystemInformationClass* est **SystemPerformanceInformation**, la mémoire tampon vers laquelle pointe le paramètre *SystemInformation* doit être suffisamment grande pour contenir une structure d' **\_ \_ informations de performances système** opaque à utiliser pour générer une valeur de départ imprévisible pour un générateur de nombres aléatoires.</span><span class="sxs-lookup"><span data-stu-id="62a4c-146">When the *SystemInformationClass* parameter is **SystemPerformanceInformation**, the buffer pointed to by the *SystemInformation* parameter should be large enough to hold an opaque **SYSTEM\_PERFORMANCE\_INFORMATION** structure for use in generating an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="62a4c-147">À cet effet, la structure a la disposition suivante :</span><span class="sxs-lookup"><span data-stu-id="62a4c-147">For this purpose, the structure has the following layout:</span></span>

``` syntax
typedef struct _SYSTEM_PERFORMANCE_INFORMATION {
    BYTE Reserved1[312];
} SYSTEM_PERFORMANCE_INFORMATION;
```

<span data-ttu-id="62a4c-148">Les membres individuels de la structure sont réservés à un usage interne par le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="62a4c-148">Individual members of the structure are reserved for internal use by the operating system.</span></span>

<span data-ttu-id="62a4c-149">Utilisez plutôt la fonction [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) pour générer des données aléatoires du point de vue du chiffrement.</span><span class="sxs-lookup"><span data-stu-id="62a4c-149">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead to generate cryptographically random data.</span></span>

</dd> <dt>

<span id="SYSTEM_TIMEOFDAY_INFORMATION"></span><span id="system_timeofday_information"></span>

<span data-ttu-id="62a4c-150"><span id="SYSTEM_TIMEOFDAY_INFORMATION"></span><span id="system_timeofday_information"></span>**\_informations sur la TimeOfDay du système \_**</span><span class="sxs-lookup"><span data-stu-id="62a4c-150"><span id="SYSTEM_TIMEOFDAY_INFORMATION"></span><span id="system_timeofday_information"></span>**SYSTEM\_TIMEOFDAY\_INFORMATION**</span></span>


</dt> <dd>

<span data-ttu-id="62a4c-151">Lorsque le paramètre *SystemInformationClass* est **SystemTimeOfDayInformation**, la mémoire tampon vers laquelle pointe le paramètre *SystemInformation* doit être suffisamment grande pour contenir une structure d' **\_ \_ informations TimeOfDay du système** opaque à utiliser pour générer une valeur de départ imprévisible pour un générateur de nombres aléatoires.</span><span class="sxs-lookup"><span data-stu-id="62a4c-151">When the *SystemInformationClass* parameter is **SystemTimeOfDayInformation**, the buffer pointed to by the *SystemInformation* parameter should be large enough to hold an opaque **SYSTEM\_TIMEOFDAY\_INFORMATION** structure for use in generating an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="62a4c-152">À cet effet, la structure a la disposition suivante :</span><span class="sxs-lookup"><span data-stu-id="62a4c-152">For this purpose, the structure has the following layout:</span></span>

``` syntax
typedef struct _SYSTEM_TIMEOFDAY_INFORMATION {
    BYTE Reserved1[48];
} SYSTEM_TIMEOFDAY_INFORMATION;
```

<span data-ttu-id="62a4c-153">Les membres individuels de la structure sont réservés à un usage interne par le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="62a4c-153">Individual members of the structure are reserved for internal use by the operating system.</span></span>

<span data-ttu-id="62a4c-154">Utilisez plutôt la fonction [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) pour générer des données aléatoires du point de vue du chiffrement.</span><span class="sxs-lookup"><span data-stu-id="62a4c-154">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead to generate cryptographically random data.</span></span>

</dd> <dt>

<span id="SYSTEM_PROCESS_INFORMATION"></span><span id="system_process_information"></span>

<span data-ttu-id="62a4c-155"><span id="SYSTEM_PROCESS_INFORMATION"></span><span id="system_process_information"></span>**\_informations sur le processus système \_**</span><span class="sxs-lookup"><span data-stu-id="62a4c-155"><span id="SYSTEM_PROCESS_INFORMATION"></span><span id="system_process_information"></span>**SYSTEM\_PROCESS\_INFORMATION**</span></span>


</dt> <dd>

<span data-ttu-id="62a4c-156">Lorsque le paramètre *SystemInformationClass* est **SystemProcessInformation**, la mémoire tampon vers laquelle pointe le paramètre *SystemInformation* doit être suffisamment grande pour contenir un tableau qui contient autant de structures d' **\_ \_ informations sur le processus système** qu’il y a de processus en cours d’exécution dans le système.</span><span class="sxs-lookup"><span data-stu-id="62a4c-156">When the *SystemInformationClass* parameter is **SystemProcessInformation**, the buffer pointed to by the *SystemInformation* parameter should be large enough to hold an array that contains as many **SYSTEM\_PROCESS\_INFORMATION** structures as there are processes running in the system.</span></span> <span data-ttu-id="62a4c-157">Chaque structure a la disposition suivante :</span><span class="sxs-lookup"><span data-stu-id="62a4c-157">Each structure has the following layout:</span></span>

``` syntax
typedef struct _SYSTEM_PROCESS_INFORMATION {
    ULONG NextEntryOffset;
    ULONG NumberOfThreads;
    BYTE Reserved1[48];
    PVOID Reserved2[3];
    HANDLE UniqueProcessId;
    PVOID Reserved3;
    ULONG HandleCount;
    BYTE Reserved4[4];
    PVOID Reserved5[11];
    SIZE_T PeakPagefileUsage;
    SIZE_T PrivatePageCount;
    LARGE_INTEGER Reserved6[6];
} SYSTEM_PROCESS_INFORMATION;
```

<span data-ttu-id="62a4c-158">Le membre **NumberOfThreads** contient le nombre total de threads en cours d’exécution dans le processus.</span><span class="sxs-lookup"><span data-stu-id="62a4c-158">The **NumberOfThreads** member contains the total number of currently running threads in the process.</span></span>

<span data-ttu-id="62a4c-159">Le membre **HandleCount** contient le nombre total de handles utilisés par le processus en question ; Utilisez [**GetProcessHandleCount**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocesshandlecount) pour récupérer ces informations à la place.</span><span class="sxs-lookup"><span data-stu-id="62a4c-159">The **HandleCount** member contains the total number of handles being used by the process in question; use [**GetProcessHandleCount**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocesshandlecount) to retrieve this information instead.</span></span>

<span data-ttu-id="62a4c-160">Le membre **PeakPagefileUsage** contient le nombre maximal d’octets du stockage de fichiers de pages utilisé par le processus, et le membre **PrivatePageCount** contient le nombre de pages mémoire allouées pour l’utilisation de ce processus.</span><span class="sxs-lookup"><span data-stu-id="62a4c-160">The **PeakPagefileUsage** member contains the maximum number of bytes of page-file storage used by the process, and the **PrivatePageCount** member contains the number of memory pages allocated for the use of this process.</span></span>

<span data-ttu-id="62a4c-161">Vous pouvez également récupérer ces informations à l’aide de la fonction [**GetProcessMemoryInfo**](/windows/desktop/api/psapi/nf-psapi-getprocessmemoryinfo) ou de la classe de [**\_ processus Win32**](/windows/desktop/CIMWin32Prov/win32-process) .</span><span class="sxs-lookup"><span data-stu-id="62a4c-161">You can also retrieve this information using either the [**GetProcessMemoryInfo**](/windows/desktop/api/psapi/nf-psapi-getprocessmemoryinfo) function or the [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) class.</span></span>

<span data-ttu-id="62a4c-162">Les autres membres de la structure sont réservés à un usage interne par le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="62a4c-162">The other members of the structure are reserved for internal use by the operating system.</span></span>

</dd> <dt>

<span id="SYSTEM_PROCESSOR_PERFORMANCE_INFORMATION"></span><span id="system_processor_performance_information"></span>

<span data-ttu-id="62a4c-163"><span id="SYSTEM_PROCESSOR_PERFORMANCE_INFORMATION"></span><span id="system_processor_performance_information"></span>**\_ \_ informations sur les performances du processeur système \_**</span><span class="sxs-lookup"><span data-stu-id="62a4c-163"><span id="SYSTEM_PROCESSOR_PERFORMANCE_INFORMATION"></span><span id="system_processor_performance_information"></span>**SYSTEM\_PROCESSOR\_PERFORMANCE\_INFORMATION**</span></span>


</dt> <dd>

<span data-ttu-id="62a4c-164">Lorsque le paramètre *SystemInformationClass* est **SystemProcessorPerformanceInformation**, la mémoire tampon vers laquelle pointe le paramètre *SystemInformation* doit être suffisamment grande pour contenir un tableau qui contient autant de structures d' **\_ \_ informations sur le processus système** qu’il y a de processeurs (UC) installés dans le système.</span><span class="sxs-lookup"><span data-stu-id="62a4c-164">When the *SystemInformationClass* parameter is **SystemProcessorPerformanceInformation**, the buffer pointed to by the *SystemInformation* parameter should be large enough to hold an array that contains as many **SYSTEM\_PROCESS\_INFORMATION** structures as there are processors (CPUs) installed in the system.</span></span> <span data-ttu-id="62a4c-165">Chaque structure a la disposition suivante :</span><span class="sxs-lookup"><span data-stu-id="62a4c-165">Each structure has the following layout:</span></span>

``` syntax
typedef struct
_SYSTEM_PROCESSOR_PERFORMANCE_INFORMATION {
    LARGE_INTEGER IdleTime;
    LARGE_INTEGER KernelTime;
    LARGE_INTEGER UserTime;
    LARGE_INTEGER Reserved1[2];
    ULONG Reserved2;
} SYSTEM_PROCESSOR_PERFORMANCE_INFORMATION;
```

<span data-ttu-id="62a4c-166">Le membre **IdleTime** contient la durée pendant laquelle le système est inactif, en 1/centièmes de nanoseconde.</span><span class="sxs-lookup"><span data-stu-id="62a4c-166">The **IdleTime** member contains the amount of time that the system has been idle, in 1/100ths of a nanosecond.</span></span>

<span data-ttu-id="62a4c-167">Le membre **KernelTime** contient la durée d’exécution du système en mode noyau (y compris tous les threads de tous les processus, sur tous les processeurs), en 1/centièmes de nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="62a4c-167">The **KernelTime** member contains the amount of time that the system has spent executing in Kernel mode (including all threads in all processes, on all processors), in 1/100ths of a nanosecond.</span></span>

<span data-ttu-id="62a4c-168">Le membre **UserTime** contient la durée d’exécution du système en mode utilisateur (y compris tous les threads de tous les processus, sur tous les processeurs), en 1/centièmes de nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="62a4c-168">The **UserTime** member contains the amount of time that the system has spent executing in User mode (including all threads in all processes, on all processors), in 1/100ths of a nanosecond.</span></span>

<span data-ttu-id="62a4c-169">Utilisez [**GetSystemTimes**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getsystemtimes) à la place pour récupérer ces informations.</span><span class="sxs-lookup"><span data-stu-id="62a4c-169">Use [**GetSystemTimes**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getsystemtimes) instead to retrieve this information.</span></span>

</dd> <dt>

<span id="SYSTEM_INTERRUPT_INFORMATION"></span><span id="system_interrupt_information"></span>

<span data-ttu-id="62a4c-170"><span id="SYSTEM_INTERRUPT_INFORMATION"></span><span id="system_interrupt_information"></span>**\_informations sur les interruptions système \_**</span><span class="sxs-lookup"><span data-stu-id="62a4c-170"><span id="SYSTEM_INTERRUPT_INFORMATION"></span><span id="system_interrupt_information"></span>**SYSTEM\_INTERRUPT\_INFORMATION**</span></span>


</dt> <dd>

<span data-ttu-id="62a4c-171">Lorsque le paramètre *SystemInformationClass* est **SystemInterruptInformation**, la mémoire tampon vers laquelle pointe le paramètre *SystemInformation* doit être suffisamment grande pour contenir un tableau qui contient autant de structures d' **\_ \_ informations d’interruptions système** opaques qu’il n’y a de processeurs (UC) installés sur le système.</span><span class="sxs-lookup"><span data-stu-id="62a4c-171">When the *SystemInformationClass* parameter is **SystemInterruptInformation**, the buffer pointed to by the *SystemInformation* parameter should be large enough to hold an array that contains as many opaque **SYSTEM\_INTERRUPT\_INFORMATION** structures as there are processors (CPUs) installed on the system.</span></span> <span data-ttu-id="62a4c-172">Chaque structure, ou le tableau dans son ensemble, peut être utilisée pour générer une valeur de départ imprévisible pour un générateur de nombres aléatoires.</span><span class="sxs-lookup"><span data-stu-id="62a4c-172">Each structure, or the array as a whole, can be used to generate an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="62a4c-173">À cet effet, la structure a la disposition suivante :</span><span class="sxs-lookup"><span data-stu-id="62a4c-173">For this purpose, the structure has the following layout:</span></span>

``` syntax
typedef struct _SYSTEM_INTERRUPT_INFORMATION {
    BYTE Reserved1[24];
} SYSTEM_INTERRUPT_INFORMATION;
```

<span data-ttu-id="62a4c-174">Les membres individuels de la structure sont réservés à un usage interne par le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="62a4c-174">Individual members of the structure are reserved for internal use by the operating system.</span></span>

<span data-ttu-id="62a4c-175">Utilisez plutôt la fonction [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) pour générer des données aléatoires du point de vue du chiffrement.</span><span class="sxs-lookup"><span data-stu-id="62a4c-175">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead to generate cryptographically random data.</span></span>

</dd> <dt>

<span id="SYSTEM_EXCEPTION_INFORMATION"></span><span id="system_exception_information"></span>

<span data-ttu-id="62a4c-176"><span id="SYSTEM_EXCEPTION_INFORMATION"></span><span id="system_exception_information"></span>**\_informations sur l’exception système \_**</span><span class="sxs-lookup"><span data-stu-id="62a4c-176"><span id="SYSTEM_EXCEPTION_INFORMATION"></span><span id="system_exception_information"></span>**SYSTEM\_EXCEPTION\_INFORMATION**</span></span>


</dt> <dd>

<span data-ttu-id="62a4c-177">Lorsque le paramètre *SystemInformationClass* est **SystemExceptionInformation**, la mémoire tampon vers laquelle pointe le paramètre *SystemInformation* doit être suffisamment grande pour contenir une structure d' **\_ \_ informations d’exception système** opaque à utiliser pour générer une valeur de départ imprévisible pour un générateur de nombres aléatoires.</span><span class="sxs-lookup"><span data-stu-id="62a4c-177">When the *SystemInformationClass* parameter is **SystemExceptionInformation**, the buffer pointed to by the *SystemInformation* parameter should be large enough to hold an opaque **SYSTEM\_EXCEPTION\_INFORMATION** structure for use in generating an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="62a4c-178">À cet effet, la structure a la disposition suivante :</span><span class="sxs-lookup"><span data-stu-id="62a4c-178">For this purpose, the structure has the following layout:</span></span>

``` syntax
typedef struct _SYSTEM_EXCEPTION_INFORMATION {
    BYTE Reserved1[16];
} SYSTEM_EXCEPTION_INFORMATION;
```

<span data-ttu-id="62a4c-179">Les membres individuels de la structure sont réservés à un usage interne par le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="62a4c-179">Individual members of the structure are reserved for internal use by the operating system.</span></span>

<span data-ttu-id="62a4c-180">Utilisez plutôt la fonction [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) pour générer des données aléatoires du point de vue du chiffrement.</span><span class="sxs-lookup"><span data-stu-id="62a4c-180">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead to generate cryptographically random data.</span></span>

</dd> <dt>

<span id="SYSTEM_REGISTRY_QUOTA_INFORMATION"></span><span id="system_registry_quota_information"></span>

<span data-ttu-id="62a4c-181"><span id="SYSTEM_REGISTRY_QUOTA_INFORMATION"></span><span id="system_registry_quota_information"></span>**\_ \_ informations sur les quotas du Registre système \_**</span><span class="sxs-lookup"><span data-stu-id="62a4c-181"><span id="SYSTEM_REGISTRY_QUOTA_INFORMATION"></span><span id="system_registry_quota_information"></span>**SYSTEM\_REGISTRY\_QUOTA\_INFORMATION**</span></span>


</dt> <dd>

<span data-ttu-id="62a4c-182">Lorsque le paramètre *SystemInformationClass* est **SystemRegistryQuotaInformation**, la mémoire tampon vers laquelle pointe le paramètre *SystemInformation* doit être suffisamment grande pour contenir une structure d' **\_ \_ \_ informations de quota du Registre du système** unique ayant la disposition suivante :</span><span class="sxs-lookup"><span data-stu-id="62a4c-182">When the *SystemInformationClass* parameter is **SystemRegistryQuotaInformation**, the buffer pointed to by the *SystemInformation* parameter should be large enough to hold a single **SYSTEM\_REGISTRY\_QUOTA\_INFORMATION** structure having the following layout:</span></span>

``` syntax
typedef struct _SYSTEM_REGISTRY_QUOTA_INFORMATION {
    ULONG RegistryQuotaAllowed;
    ULONG RegistryQuotaUsed;
    PVOID Reserved1;
} SYSTEM_REGISTRY_QUOTA_INFORMATION;
```

<span data-ttu-id="62a4c-183">Le membre **RegistryQuotaAllowed** contient la taille maximale, en octets, que le registre peut atteindre sur ce système.</span><span class="sxs-lookup"><span data-stu-id="62a4c-183">The **RegistryQuotaAllowed** member contains the maximum size, in bytes, that the Registry can attain on this system.</span></span>

<span data-ttu-id="62a4c-184">Le membre **RegistryQuotaUsed** contient la taille actuelle du Registre, en octets.</span><span class="sxs-lookup"><span data-stu-id="62a4c-184">The **RegistryQuotaUsed** member contains the current size of the Registry, in bytes.</span></span>

<span data-ttu-id="62a4c-185">Utilisez [**GetSystemRegistryQuota**](/windows/desktop/api/Winbase/nf-winbase-getsystemregistryquota) à la place pour récupérer ces informations.</span><span class="sxs-lookup"><span data-stu-id="62a4c-185">Use [**GetSystemRegistryQuota**](/windows/desktop/api/Winbase/nf-winbase-getsystemregistryquota) instead to retrieve this information.</span></span>

<span data-ttu-id="62a4c-186">L’autre membre de la structure est réservé à un usage interne par le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="62a4c-186">The other member of the structure is reserved for internal use by the operating system.</span></span>

</dd> <dt>

<span id="SYSTEM_LOOKASIDE_INFORMATION"></span><span id="system_lookaside_information"></span>

<span data-ttu-id="62a4c-187"><span id="SYSTEM_LOOKASIDE_INFORMATION"></span><span id="system_lookaside_information"></span>**\_informations système \_**</span><span class="sxs-lookup"><span data-stu-id="62a4c-187"><span id="SYSTEM_LOOKASIDE_INFORMATION"></span><span id="system_lookaside_information"></span>**SYSTEM\_LOOKASIDE\_INFORMATION**</span></span>


</dt> <dd>

<span data-ttu-id="62a4c-188">Lorsque le paramètre *SystemInformationClass* est **SystemLookasideInformation**, la mémoire tampon vers laquelle pointe le paramètre *SystemInformation* doit être suffisamment grande pour contenir une structure d' **\_ \_ informations de système** insuffisante pour une utilisation lors de la génération d’une valeur de départ imprévisible pour un générateur de nombres aléatoires.</span><span class="sxs-lookup"><span data-stu-id="62a4c-188">When the *SystemInformationClass* parameter is **SystemLookasideInformation**, the buffer pointed to by the *SystemInformation* parameter should be large enough to hold an opaque **SYSTEM\_LOOKASIDE\_INFORMATION** structure for use in generating an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="62a4c-189">À cet effet, la structure a la disposition suivante :</span><span class="sxs-lookup"><span data-stu-id="62a4c-189">For this purpose, the structure has the following layout:</span></span>

``` syntax
typedef struct _SYSTEM_LOOKASIDE_INFORMATION {
    BYTE Reserved1[32];
} SYSTEM_LOOKASIDE_INFORMATION;
```

<span data-ttu-id="62a4c-190">Les membres individuels de la structure sont réservés à un usage interne par le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="62a4c-190">Individual members of the structure are reserved for internal use by the operating system.</span></span>

<span data-ttu-id="62a4c-191">Utilisez plutôt la fonction [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) pour générer des données aléatoires du point de vue du chiffrement.</span><span class="sxs-lookup"><span data-stu-id="62a4c-191">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead to generate cryptographically random data.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="62a4c-192">*SystemInformationLength* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="62a4c-192">*SystemInformationLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62a4c-193">Taille de la mémoire tampon vers laquelle pointe le paramètre *SystemInformation* , en octets.</span><span class="sxs-lookup"><span data-stu-id="62a4c-193">The size of the buffer pointed to by the *SystemInformation* parameter, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="62a4c-194">*ReturnLength* \[ out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="62a4c-194">*ReturnLength* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="62a4c-195">Pointeur facultatif vers un emplacement où la fonction écrit la taille réelle des informations demandées.</span><span class="sxs-lookup"><span data-stu-id="62a4c-195">An optional pointer to a location where the function writes the actual size of the information requested.</span></span> <span data-ttu-id="62a4c-196">Si cette taille est inférieure ou égale au paramètre *SystemInformationLength* , la fonction copie les informations dans la mémoire tampon *SystemInformation* ; Sinon, elle retourne un code d’erreur NTSTATUS et retourne dans *ReturnLength* la taille de la mémoire tampon requise pour recevoir les informations demandées.</span><span class="sxs-lookup"><span data-stu-id="62a4c-196">If that size is less than or equal to the *SystemInformationLength* parameter, the function copies the information into the *SystemInformation* buffer; otherwise, it returns an NTSTATUS error code and returns in *ReturnLength* the size of buffer required to receive the requested information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62a4c-197">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="62a4c-197">Return value</span></span>

<span data-ttu-id="62a4c-198">Retourne un code d’erreur ou de réussite NTSTATUS.</span><span class="sxs-lookup"><span data-stu-id="62a4c-198">Returns an NTSTATUS success or error code.</span></span>

<span data-ttu-id="62a4c-199">Les formulaires et la signification des codes d’erreur de NTSTATUS sont répertoriés dans le fichier d’en-tête Ntstatus. h disponible dans le DDK et sont décrits dans la documentation du DDK.</span><span class="sxs-lookup"><span data-stu-id="62a4c-199">The forms and significance of NTSTATUS error codes are listed in the Ntstatus.h header file available in the DDK, and are described in the DDK documentation.</span></span>

## <a name="remarks"></a><span data-ttu-id="62a4c-200">Notes</span><span class="sxs-lookup"><span data-stu-id="62a4c-200">Remarks</span></span>

<span data-ttu-id="62a4c-201">La fonction **ZwQuerySystemInformation** et les structures qu’elle retourne sont internes au système d’exploitation et peuvent être modifiées d’une version de Windows à une autre.</span><span class="sxs-lookup"><span data-stu-id="62a4c-201">The **ZwQuerySystemInformation** function and the structures that it returns are internal to the operating system and subject to change from one release of Windows to another.</span></span> <span data-ttu-id="62a4c-202">Pour maintenir la compatibilité de votre application, il est préférable d’utiliser les autres fonctions mentionnées précédemment.</span><span class="sxs-lookup"><span data-stu-id="62a4c-202">To maintain the compatibility of your application, it is better to use the alternate functions previously mentioned instead.</span></span>

<span data-ttu-id="62a4c-203">Si vous utilisez **ZwQuerySystemInformation**, accédez à la fonction via la [liaison dynamique au moment de l’exécution](/windows/desktop/Dlls/using-run-time-dynamic-linking).</span><span class="sxs-lookup"><span data-stu-id="62a4c-203">If you do use **ZwQuerySystemInformation**, access the function through [run-time dynamic linking](/windows/desktop/Dlls/using-run-time-dynamic-linking).</span></span> <span data-ttu-id="62a4c-204">Cela donne à votre code la possibilité de répondre correctement si la fonction a été modifiée ou supprimée du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="62a4c-204">This gives your code an opportunity to respond gracefully if the function has been changed or removed from the operating system.</span></span> <span data-ttu-id="62a4c-205">Toutefois, les modifications de signature peuvent ne pas être détectables.</span><span class="sxs-lookup"><span data-stu-id="62a4c-205">Signature changes, however, may not be detectable.</span></span>

<span data-ttu-id="62a4c-206">Cette fonction n’a pas de bibliothèque d’importation associée.</span><span class="sxs-lookup"><span data-stu-id="62a4c-206">This function has no associated import library.</span></span> <span data-ttu-id="62a4c-207">Vous devez utiliser les fonctions [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Ntdll.dll.</span><span class="sxs-lookup"><span data-stu-id="62a4c-207">You must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Ntdll.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="62a4c-208">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="62a4c-208">Requirements</span></span>



| <span data-ttu-id="62a4c-209">Condition requise</span><span class="sxs-lookup"><span data-stu-id="62a4c-209">Requirement</span></span> | <span data-ttu-id="62a4c-210">Valeur</span><span class="sxs-lookup"><span data-stu-id="62a4c-210">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="62a4c-211">DLL</span><span class="sxs-lookup"><span data-stu-id="62a4c-211">DLL</span></span><br/> | <dl> <span data-ttu-id="62a4c-212"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62a4c-212"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62a4c-213">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="62a4c-213">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62a4c-214">**GetSystemInfo**</span><span class="sxs-lookup"><span data-stu-id="62a4c-214">**GetSystemInfo**</span></span>](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo)
</dt> <dt>

[<span data-ttu-id="62a4c-215">**GetProcessHandleCount**</span><span class="sxs-lookup"><span data-stu-id="62a4c-215">**GetProcessHandleCount**</span></span>](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocesshandlecount)
</dt> <dt>

[<span data-ttu-id="62a4c-216">**GetProcessMemoryInfo**</span><span class="sxs-lookup"><span data-stu-id="62a4c-216">**GetProcessMemoryInfo**</span></span>](/windows/desktop/api/psapi/nf-psapi-getprocessmemoryinfo)
</dt> <dt>

[<span data-ttu-id="62a4c-217">**GetSystemTimes**</span><span class="sxs-lookup"><span data-stu-id="62a4c-217">**GetSystemTimes**</span></span>](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getsystemtimes)
</dt> <dt>

[<span data-ttu-id="62a4c-218">**GetSystemRegistryQuota**</span><span class="sxs-lookup"><span data-stu-id="62a4c-218">**GetSystemRegistryQuota**</span></span>](/windows/desktop/api/Winbase/nf-winbase-getsystemregistryquota)
</dt> </dl>

 

