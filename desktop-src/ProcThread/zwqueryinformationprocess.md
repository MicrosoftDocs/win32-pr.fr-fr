---
description: Récupère des informations sur le processus spécifié.
ms.assetid: c36c023f-7f9a-4ba5-a41f-f2f755a24eb6
title: ZwQueryInformationProcess fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ZwQueryInformationProcess
api_type:
- DllExport
api_location:
- Ntdll.dll
- ntoskrnl.exe
ms.openlocfilehash: 30207c8d3d54c54f77194b542e10e9fee94e055a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529827"
---
# <a name="zwqueryinformationprocess-function"></a><span data-ttu-id="cba11-103">ZwQueryInformationProcess fonction)</span><span class="sxs-lookup"><span data-stu-id="cba11-103">ZwQueryInformationProcess function</span></span>

<span data-ttu-id="cba11-104">\[Les **ZwQueryInformationProcess** peuvent être modifiés ou non disponibles dans les futures versions de Windows.</span><span class="sxs-lookup"><span data-stu-id="cba11-104">\[**ZwQueryInformationProcess** may be altered or unavailable in future versions of Windows.</span></span> <span data-ttu-id="cba11-105">Les applications doivent utiliser les autres fonctions présentées dans cette rubrique.\]</span><span class="sxs-lookup"><span data-stu-id="cba11-105">Applications should use the alternate functions listed in this topic.\]</span></span>

<span data-ttu-id="cba11-106">Récupère des informations sur le processus spécifié.</span><span class="sxs-lookup"><span data-stu-id="cba11-106">Retrieves information about the specified process.</span></span>

## <a name="syntax"></a><span data-ttu-id="cba11-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cba11-107">Syntax</span></span>


```C++
NTSTATUS WINAPI ZwQueryInformationProcess(
  _In_      HANDLE           ProcessHandle,
  _In_      PROCESSINFOCLASS ProcessInformationClass,
  _Out_     PVOID            ProcessInformation,
  _In_      ULONG            ProcessInformationLength,
  _Out_opt_ PULONG           ReturnLength
);
```



## <a name="parameters"></a><span data-ttu-id="cba11-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cba11-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cba11-109">*ProcessHandle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cba11-109">*ProcessHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cba11-110">Handle vers le processus dont les informations doivent être récupérées.</span><span class="sxs-lookup"><span data-stu-id="cba11-110">A handle to the process for which information is to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="cba11-111">*ProcessInformationClass* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cba11-111">*ProcessInformationClass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cba11-112">Type d’informations de processus à récupérer.</span><span class="sxs-lookup"><span data-stu-id="cba11-112">The type of process information to be retrieved.</span></span> <span data-ttu-id="cba11-113">Ce paramètre peut avoir l’une des valeurs suivantes de l’énumération **PROCESSINFOCLASS** .</span><span class="sxs-lookup"><span data-stu-id="cba11-113">This parameter can be one of the following values from the **PROCESSINFOCLASS** enumeration.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cba11-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="cba11-114">Value</span></span></th>
<th><span data-ttu-id="cba11-115">Signification</span><span class="sxs-lookup"><span data-stu-id="cba11-115">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="ProcessBasicInformation"></span><span id="processbasicinformation"></span><span id="PROCESSBASICINFORMATION"></span><dl> <span data-ttu-id="cba11-116"><dt><strong>ProcessBasicInformation</strong></dt> <dt>0</dt> </span><span class="sxs-lookup"><span data-stu-id="cba11-116"><dt><strong>ProcessBasicInformation</strong></dt> <dt>0</dt> </span></span></dl></td>
<td><span data-ttu-id="cba11-117">Récupère un pointeur vers une structure PEB qui peut être utilisée pour déterminer si le processus spécifié est en cours de débogage, et une valeur unique utilisée par le système pour identifier le processus spécifié.</span><span class="sxs-lookup"><span data-stu-id="cba11-117">Retrieves a pointer to a PEB structure that can be used to determine whether the specified process is being debugged, and a unique value used by the system to identify the specified process.</span></span> <br/> <span data-ttu-id="cba11-118">Il est préférable d’utiliser les fonctions <a href="/windows/desktop/api/debugapi/nf-debugapi-checkremotedebuggerpresent"><strong>CheckRemoteDebuggerPresent</strong></a> et <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocessid"><strong>GetProcessID,</strong></a> pour obtenir ces informations.</span><span class="sxs-lookup"><span data-stu-id="cba11-118">It is best to use the <a href="/windows/desktop/api/debugapi/nf-debugapi-checkremotedebuggerpresent"><strong>CheckRemoteDebuggerPresent</strong></a> and <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocessid"><strong>GetProcessId</strong></a> functions to obtain this information.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ProcessDebugPort"></span><span id="processdebugport"></span><span id="PROCESSDEBUGPORT"></span><dl> <span data-ttu-id="cba11-119"><dt><strong>ProcessDebugPort</strong></dt> <dt>7</dt> </span><span class="sxs-lookup"><span data-stu-id="cba11-119"><dt><strong>ProcessDebugPort</strong></dt> <dt>7</dt> </span></span></dl></td>
<td><span data-ttu-id="cba11-120">Récupère une valeur <strong>DWORD_PTR</strong> qui est le numéro de port du débogueur pour le processus.</span><span class="sxs-lookup"><span data-stu-id="cba11-120">Retrieves a <strong>DWORD_PTR</strong> value that is the port number of the debugger for the process.</span></span> <span data-ttu-id="cba11-121">Une valeur différente de zéro indique que le processus est en cours d’exécution sous le contrôle d’un débogueur ring 3.</span><span class="sxs-lookup"><span data-stu-id="cba11-121">A nonzero value indicates that the process is being run under the control of a ring 3 debugger.</span></span><br/> <span data-ttu-id="cba11-122">Il est préférable d’utiliser la fonction <a href="/windows/desktop/api/debugapi/nf-debugapi-checkremotedebuggerpresent"><strong>CheckRemoteDebuggerPresent</strong></a> ou <a href="/windows/desktop/api/debugapi/nf-debugapi-isdebuggerpresent"><strong>IsDebuggerPresent</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="cba11-122">It is best to use the <a href="/windows/desktop/api/debugapi/nf-debugapi-checkremotedebuggerpresent"><strong>CheckRemoteDebuggerPresent</strong></a> or <a href="/windows/desktop/api/debugapi/nf-debugapi-isdebuggerpresent"><strong>IsDebuggerPresent</strong></a> function.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ProcessWow64Information"></span><span id="processwow64information"></span><span id="PROCESSWOW64INFORMATION"></span><dl> <span data-ttu-id="cba11-123"><dt><strong>ProcessWow64Information</strong></dt> <dt>26</dt> </span><span class="sxs-lookup"><span data-stu-id="cba11-123"><dt><strong>ProcessWow64Information</strong></dt> <dt>26</dt> </span></span></dl></td>
<td><span data-ttu-id="cba11-124">Détermine si le processus s’exécute dans l’environnement WOW64 (WOW64 est l’émulateur x86 qui permet aux applications Win32 de s’exécuter sur Windows 64 bits).</span><span class="sxs-lookup"><span data-stu-id="cba11-124">Determines whether the process is running in the WOW64 environment (WOW64 is the x86 emulator that allows Win32-based applications to run on 64-bit Windows).</span></span><br/> <span data-ttu-id="cba11-125">Il est préférable d’utiliser la fonction <a href="/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process"><strong>IsWow64Process</strong></a> pour obtenir ces informations.</span><span class="sxs-lookup"><span data-stu-id="cba11-125">It is best to use the <a href="/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process"><strong>IsWow64Process</strong></a> function to obtain this information.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ProcessImageFileName"></span><span id="processimagefilename"></span><span id="PROCESSIMAGEFILENAME"></span><dl> <span data-ttu-id="cba11-126"><dt><strong>ProcessImageFileName</strong></dt> <dt>27</dt> </span><span class="sxs-lookup"><span data-stu-id="cba11-126"><dt><strong>ProcessImageFileName</strong></dt> <dt>27</dt> </span></span></dl></td>
<td><span data-ttu-id="cba11-127">Récupère une valeur <strong>UNICODE_STRING</strong> contenant le nom du fichier image pour le processus.</span><span class="sxs-lookup"><span data-stu-id="cba11-127">Retrieves a <strong>UNICODE_STRING</strong> value containing the name of the image file for the process.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ProcessBreakOnTermination"></span><span id="processbreakontermination"></span><span id="PROCESSBREAKONTERMINATION"></span><dl> <span data-ttu-id="cba11-128"><dt><strong>ProcessBreakOnTermination</strong></dt> <dt>29</dt> </span><span class="sxs-lookup"><span data-stu-id="cba11-128"><dt><strong>ProcessBreakOnTermination</strong></dt> <dt>29</dt> </span></span></dl></td>
<td><span data-ttu-id="cba11-129">Récupère une valeur <strong>ULong</strong> indiquant si le processus est considéré comme critique.</span><span class="sxs-lookup"><span data-stu-id="cba11-129">Retrieves a <strong>ULONG</strong> value indicating whether the process is considered critical.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="cba11-130">Cette valeur peut être utilisée à partir de Windows XP avec SP3.</span><span class="sxs-lookup"><span data-stu-id="cba11-130">This value can be used starting in Windows XP with SP3.</span></span> <span data-ttu-id="cba11-131">À partir de Windows 8.1, <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-isprocesscritical"><strong>IsProcessCritical</strong></a> doit être utilisé à la place.</span><span class="sxs-lookup"><span data-stu-id="cba11-131">Starting in Windows 8.1, <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-isprocesscritical"><strong>IsProcessCritical</strong></a> should be used instead.</span></span>
</blockquote>
<br/></td>
</tr><tr class="even">
<td><span id="ProcessProtectionInformation"></span><span id="processprotectioninformation"></span><span id="PROCESSPROTECTIONINFORMATION"></span><dl> <span data-ttu-id="cba11-132"><dt><strong>ProcessProtectionInformation</strong></dt> <dt>61</dt> </span><span class="sxs-lookup"><span data-stu-id="cba11-132"><dt><strong>ProcessProtectionInformation</strong></dt> <dt>61</dt> </span></span></dl></td>
<td><span data-ttu-id="cba11-133">Récupère une valeur d’octet qui indique le type de processus protégé et le signataire de processus protégé.</span><span class="sxs-lookup"><span data-stu-id="cba11-133">Retrieves a BYTE value indicating the type of protected process and the protected process signer.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="cba11-134">*ProcessInformation* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="cba11-134">*ProcessInformation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cba11-135">Pointeur vers une mémoire tampon fournie par l’application appelante dans laquelle la fonction écrit les informations demandées.</span><span class="sxs-lookup"><span data-stu-id="cba11-135">A pointer to a buffer supplied by the calling application into which the function writes the requested information.</span></span> <span data-ttu-id="cba11-136">La taille des informations écrites varie en fonction de la valeur du paramètre *ProcessInformationClass* :</span><span class="sxs-lookup"><span data-stu-id="cba11-136">The size of the information written varies depending on the value of the *ProcessInformationClass* parameter:</span></span>

<dl> <dt>

<span data-ttu-id="cba11-137"><span id="PROCESS_BASIC_INFORMATION"></span><span id="process_basic_information"></span>TRAITER \_ les \_ informations de base</span><span class="sxs-lookup"><span data-stu-id="cba11-137"><span id="PROCESS_BASIC_INFORMATION"></span><span id="process_basic_information"></span>PROCESS\_BASIC\_INFORMATION</span></span>
</dt> <dd>

<span data-ttu-id="cba11-138">Lorsque le paramètre *ProcessInformationClass* est **ProcessBasicInformation**, la mémoire tampon vers laquelle pointe le paramètre *ProcessInformation* doit être suffisamment grande pour contenir une structure d' **\_ \_ informations de base de processus** unique ayant la disposition suivante :</span><span class="sxs-lookup"><span data-stu-id="cba11-138">When the *ProcessInformationClass* parameter is **ProcessBasicInformation**, the buffer pointed to by the *ProcessInformation* parameter should be large enough to hold a single **PROCESS\_BASIC\_INFORMATION** structure having the following layout:</span></span>

``` syntax
typedef struct _PROCESS_BASIC_INFORMATION {
    PVOID Reserved1;
    PPEB PebBaseAddress;
    PVOID Reserved2[2];
    ULONG_PTR UniqueProcessId;
    PVOID Reserved3;
} PROCESS_BASIC_INFORMATION;
```

<span data-ttu-id="cba11-139">Le membre **UniqueProcessId** pointe vers l’identificateur unique du système pour ce processus.</span><span class="sxs-lookup"><span data-stu-id="cba11-139">The **UniqueProcessId** member points to the system's unique identifier for this process.</span></span> <span data-ttu-id="cba11-140">Il est préférable d’utiliser la fonction [**GetProcessID,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessid) pour récupérer ces informations.</span><span class="sxs-lookup"><span data-stu-id="cba11-140">It is best to use the [**GetProcessId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessid) function to retrieve this information.</span></span>

<span data-ttu-id="cba11-141">Le membre **PebBaseAddress** pointe vers une structure [**PEB**](/windows/desktop/api/Winternl/ns-winternl-peb) .</span><span class="sxs-lookup"><span data-stu-id="cba11-141">The **PebBaseAddress** member points to a [**PEB**](/windows/desktop/api/Winternl/ns-winternl-peb) structure.</span></span>

<span data-ttu-id="cba11-142">Les autres membres de cette structure sont réservés à un usage interne par le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="cba11-142">The other members of this structure are reserved for internal use by the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="cba11-143"><span id="ULONG_PTR"></span><span id="ulong_ptr"></span>ULONG ( \_ PTR)</span><span class="sxs-lookup"><span data-stu-id="cba11-143"><span id="ULONG_PTR"></span><span id="ulong_ptr"></span>ULONG\_PTR</span></span>
</dt> <dd>

<span data-ttu-id="cba11-144">Lorsque le paramètre *ProcessInformationClass* est **ProcessWow64Information**, la mémoire tampon vers laquelle pointe le paramètre *ProcessInformation* doit être suffisamment grande pour contenir **un \_ ptr ulong**.</span><span class="sxs-lookup"><span data-stu-id="cba11-144">When the *ProcessInformationClass* parameter is **ProcessWow64Information**, the buffer pointed to by the *ProcessInformation* parameter should be large enough to hold a **ULONG\_PTR**.</span></span> <span data-ttu-id="cba11-145">Si cette valeur est différente de zéro, le processus s’exécute dans un environnement WOW64 ; Sinon, si la valeur est égale à zéro, le processus ne s’exécute pas dans un environnement WOW64.</span><span class="sxs-lookup"><span data-stu-id="cba11-145">If this value is nonzero, the process is running in a WOW64 environment; otherwise, if the value is equal to zero, the process is not running in a WOW64 environment.</span></span>

<span data-ttu-id="cba11-146">Il est préférable d’utiliser la fonction [**IsWow64Process**](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process) pour déterminer si un processus s’exécute dans l’environnement WOW64.</span><span class="sxs-lookup"><span data-stu-id="cba11-146">It is best to use the [**IsWow64Process**](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process) function to determine whether a process is running in the WOW64 environment.</span></span>

</dd> <dt>

<span data-ttu-id="cba11-147"><span id="UNICODE_STRING"></span><span id="unicode_string"></span>\_chaîne Unicode</span><span class="sxs-lookup"><span data-stu-id="cba11-147"><span id="UNICODE_STRING"></span><span id="unicode_string"></span>UNICODE\_STRING</span></span>
</dt> <dd>

<span data-ttu-id="cba11-148">Lorsque le paramètre *ProcessInformationClass* est **ProcessImageFileName**, la mémoire tampon vers laquelle pointe le paramètre *ProcessInformation* doit être suffisamment grande pour contenir une structure de **\_ chaîne Unicode** , ainsi que la chaîne elle-même.</span><span class="sxs-lookup"><span data-stu-id="cba11-148">When the *ProcessInformationClass* parameter is **ProcessImageFileName**, the buffer pointed to by the *ProcessInformation* parameter should be large enough to hold a **UNICODE\_STRING** structure as well as the string itself.</span></span> <span data-ttu-id="cba11-149">La chaîne stockée dans le membre de la **mémoire tampon** est le nom du fichier image.</span><span class="sxs-lookup"><span data-stu-id="cba11-149">The string stored in the **Buffer** member is the name of the image file.</span></span>

<span data-ttu-id="cba11-150">Si la mémoire tampon est trop petite, la fonction échoue avec le \_ code d’erreur d’incompatibilité de la longueur des informations d’état \_ \_ et le paramètre *ReturnLength* est défini sur la taille de mémoire tampon requise.</span><span class="sxs-lookup"><span data-stu-id="cba11-150">If the buffer is too small, the function fails with the STATUS\_INFO\_LENGTH\_MISMATCH error code and the *ReturnLength* parameter is set to the required buffer size.</span></span>

</dd> <dt>

<span data-ttu-id="cba11-151"><span id="PS_PROTECTION"></span><span id="ps_protection"></span>PS_PROTECTION</span><span class="sxs-lookup"><span data-stu-id="cba11-151"><span id="PS_PROTECTION"></span><span id="ps_protection"></span>PS_PROTECTION</span></span>
</dt> <dd>

<span data-ttu-id="cba11-152">Lorsque le paramètre *ProcessInformationClass* est **ProcessProtectionInformation**, la mémoire tampon vers laquelle pointe le paramètre *ProcessInformation* doit être suffisamment grande pour contenir une structure **PS_PROTECTION** unique ayant la disposition suivante :</span><span class="sxs-lookup"><span data-stu-id="cba11-152">When the *ProcessInformationClass* parameter is **ProcessProtectionInformation**, the buffer pointed to by the *ProcessInformation* parameter should be large enough to hold a single **PS_PROTECTION** structure having the following layout:</span></span>

``` syntax
typedef struct _PS_PROTECTION {
    union {
        UCHAR Level;
        struct {
            UCHAR Type   : 3;
            UCHAR Audit  : 1;                  // Reserved
            UCHAR Signer : 4;
        };
    };
} PS_PROTECTION, *PPS_PROTECTION;
```

<span data-ttu-id="cba11-153">Les 3 premiers bits contiennent le type de processus protégé :</span><span class="sxs-lookup"><span data-stu-id="cba11-153">The first 3 bits contain the type of protected process:</span></span>

``` syntax
typedef enum _PS_PROTECTED_TYPE {
    PsProtectedTypeNone = 0,
    PsProtectedTypeProtectedLight = 1,
    PsProtectedTypeProtected = 2
} PS_PROTECTED_TYPE, *PPS_PROTECTED_TYPE;
```

<span data-ttu-id="cba11-154">Les 4 premiers bits contiennent le signataire de processus protégé :</span><span class="sxs-lookup"><span data-stu-id="cba11-154">The top 4 bits contain the protected process signer:</span></span>

``` syntax
typedef enum _PS_PROTECTED_SIGNER {
    PsProtectedSignerNone = 0,
    PsProtectedSignerAuthenticode,
    PsProtectedSignerCodeGen,
    PsProtectedSignerAntimalware,
    PsProtectedSignerLsa,
    PsProtectedSignerWindows,
    PsProtectedSignerWinTcb,
    PsProtectedSignerWinSystem,
    PsProtectedSignerApp,
    PsProtectedSignerMax
} PS_PROTECTED_SIGNER, *PPS_PROTECTED_SIGNER;
```

</dd> </dl> </dd> <dt>

<span data-ttu-id="cba11-155">*ProcessInformationLength* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cba11-155">*ProcessInformationLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cba11-156">Taille de la mémoire tampon vers laquelle pointe le paramètre *ProcessInformation* , en octets.</span><span class="sxs-lookup"><span data-stu-id="cba11-156">The size of the buffer pointed to by the *ProcessInformation* parameter, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="cba11-157">*ReturnLength* \[ out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="cba11-157">*ReturnLength* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cba11-158">Pointeur vers une variable dans laquelle la fonction retourne la taille des informations demandées.</span><span class="sxs-lookup"><span data-stu-id="cba11-158">A pointer to a variable in which the function returns the size of the requested information.</span></span> <span data-ttu-id="cba11-159">Si la fonction a réussi, il s’agit de la taille des informations écrites dans la mémoire tampon vers laquelle pointe le paramètre *ProcessInformation* , mais si la mémoire tampon est trop petite, il s’agit de la taille minimale de la mémoire tampon nécessaire pour recevoir correctement les informations.</span><span class="sxs-lookup"><span data-stu-id="cba11-159">If the function was successful, this is the size of the information written to the buffer pointed to by the *ProcessInformation* parameter, but if the buffer was too small, this is the minimum size of buffer needed to receive the information successfully.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cba11-160">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cba11-160">Return value</span></span>

<span data-ttu-id="cba11-161">Retourne un code d’erreur ou de réussite NTSTATUS.</span><span class="sxs-lookup"><span data-stu-id="cba11-161">Returns an NTSTATUS success or error code.</span></span>

<span data-ttu-id="cba11-162">Les formulaires et la signification des codes d’erreur de NTSTATUS sont répertoriés dans le fichier d’en-tête Ntstatus. h disponible dans le DDK, et sont décrits dans la documentation du DDK sous Kernel-Mode architecture du pilote/Guide de conception/Guide de conception/techniques de programmation des pilotes/erreurs de journalisation.</span><span class="sxs-lookup"><span data-stu-id="cba11-162">The forms and significance of NTSTATUS error codes are listed in the Ntstatus.h header file available in the DDK, and are described in the DDK documentation under Kernel-Mode Driver Architecture / Design Guide / Driver Programming Techniques / Logging Errors.</span></span>

## <a name="remarks"></a><span data-ttu-id="cba11-163">Notes</span><span class="sxs-lookup"><span data-stu-id="cba11-163">Remarks</span></span>

<span data-ttu-id="cba11-164">La fonction **ZwQueryInformationProcess** et les structures qu’elle retourne sont internes au système d’exploitation et peuvent être modifiées d’une version de Windows à une autre.</span><span class="sxs-lookup"><span data-stu-id="cba11-164">The **ZwQueryInformationProcess** function and the structures that it returns are internal to the operating system and subject to change from one release of Windows to another.</span></span> <span data-ttu-id="cba11-165">Pour maintenir la compatibilité de votre application, il est préférable d’utiliser à la place les fonctions publiques mentionnées dans la description du paramètre *ProcessInformationClass* .</span><span class="sxs-lookup"><span data-stu-id="cba11-165">To maintain the compatibility of your application, it is better to use public functions mentioned in the description of the *ProcessInformationClass* parameter instead.</span></span>

<span data-ttu-id="cba11-166">Si vous utilisez **ZwQueryInformationProcess**, accédez à la fonction via la [liaison dynamique au moment de l’exécution](../dlls/using-run-time-dynamic-linking.md).</span><span class="sxs-lookup"><span data-stu-id="cba11-166">If you do use **ZwQueryInformationProcess**, access the function through [run-time dynamic linking](../dlls/using-run-time-dynamic-linking.md).</span></span> <span data-ttu-id="cba11-167">Cela donne à votre code la possibilité de répondre correctement si la fonction a été modifiée ou supprimée du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="cba11-167">This gives your code an opportunity to respond gracefully if the function has been changed or removed from the operating system.</span></span> <span data-ttu-id="cba11-168">Toutefois, les modifications de signature peuvent ne pas être détectables.</span><span class="sxs-lookup"><span data-stu-id="cba11-168">Signature changes, however, may not be detectable.</span></span>

<span data-ttu-id="cba11-169">Cette fonction n’a pas de bibliothèque d’importation associée.</span><span class="sxs-lookup"><span data-stu-id="cba11-169">This function has no associated import library.</span></span> <span data-ttu-id="cba11-170">Vous devez utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Ntdll.dll.</span><span class="sxs-lookup"><span data-stu-id="cba11-170">You must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Ntdll.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="cba11-171">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cba11-171">Requirements</span></span>



| <span data-ttu-id="cba11-172">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cba11-172">Requirement</span></span> | <span data-ttu-id="cba11-173">Valeur</span><span class="sxs-lookup"><span data-stu-id="cba11-173">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cba11-174">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cba11-174">Minimum supported client</span></span><br/> | <span data-ttu-id="cba11-175">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cba11-175">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="cba11-176">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cba11-176">Minimum supported server</span></span><br/> | <span data-ttu-id="cba11-177">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cba11-177">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="cba11-178">DLL</span><span class="sxs-lookup"><span data-stu-id="cba11-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cba11-179"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cba11-179"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cba11-180">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cba11-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cba11-181">**CheckRemoteDebuggerPresent**</span><span class="sxs-lookup"><span data-stu-id="cba11-181">**CheckRemoteDebuggerPresent**</span></span>](/windows/win32/api/debugapi/nf-debugapi-checkremotedebuggerpresent)
</dt> <dt>

[<span data-ttu-id="cba11-182">**GetProcessID,**</span><span class="sxs-lookup"><span data-stu-id="cba11-182">**GetProcessId**</span></span>](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessid)
</dt> <dt>

[<span data-ttu-id="cba11-183">**IsDebuggerPresent**</span><span class="sxs-lookup"><span data-stu-id="cba11-183">**IsDebuggerPresent**</span></span>](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent)
</dt> <dt>

[<span data-ttu-id="cba11-184">**IsWow64Process**</span><span class="sxs-lookup"><span data-stu-id="cba11-184">**IsWow64Process**</span></span>](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process)
</dt> </dl>

 

 
