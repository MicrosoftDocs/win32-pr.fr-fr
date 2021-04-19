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
# <a name="zwquerysysteminformation-function"></a>ZwQuerySystemInformation fonction)

\[**ZwQuerySystemInformation** n’est plus disponible pour une utilisation à partir de Windows 8. Utilisez plutôt les autres fonctions indiquées dans cette rubrique.\]

Récupère les informations système spécifiées.

## <a name="syntax"></a>Syntaxe


```C++
NTSTATUS WINAPI ZwQuerySystemInformation(
  _In_      SYSTEM_INFORMATION_CLASS SystemInformationClass,
  _Inout_   PVOID                    SystemInformation,
  _In_      ULONG                    SystemInformationLength,
  _Out_opt_ PULONG                   ReturnLength
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*SystemInformationClass* \[ dans\]
</dt> <dd>

Type d’informations système à récupérer. Ce paramètre peut avoir l’une des valeurs suivantes du type d’énumération de **\_ \_ classe d’informations système** .

<dt>

<span id="SystemBasicInformation"></span><span id="systembasicinformation"></span><span id="SYSTEMBASICINFORMATION"></span>

<span id="SystemBasicInformation"></span><span id="systembasicinformation"></span><span id="SYSTEMBASICINFORMATION"></span>**SystemBasicInformation**


</dt> <dd>

Nombre de processeurs dans le système dans une structure d' **\_ \_ information de base du système** . Utilisez à la place la fonction [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) .

</dd> <dt>

<span id="SystemPerformanceInformation"></span><span id="systemperformanceinformation"></span><span id="SYSTEMPERFORMANCEINFORMATION"></span>

<span id="SystemPerformanceInformation"></span><span id="systemperformanceinformation"></span><span id="SYSTEMPERFORMANCEINFORMATION"></span>**SystemPerformanceInformation**


</dt> <dd>

Structure d' **\_ \_ informations sur les performances du système** opaque qui peut être utilisée pour générer une valeur de départ imprévisible pour un générateur de nombres aléatoires. Utilisez à la place la fonction [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) .

</dd> <dt>

<span id="SystemTimeOfDayInformation"></span><span id="systemtimeofdayinformation"></span><span id="SYSTEMTIMEOFDAYINFORMATION"></span>

<span id="SystemTimeOfDayInformation"></span><span id="systemtimeofdayinformation"></span><span id="SYSTEMTIMEOFDAYINFORMATION"></span>**SystemTimeOfDayInformation**


</dt> <dd>

Structure d' **\_ \_ informations TimeOfDay du système** opaque qui peut être utilisée pour générer une valeur de départ imprévisible pour un générateur de nombres aléatoires. Utilisez à la place la fonction [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) .

</dd> <dt>

<span id="SystemProcessInformation"></span><span id="systemprocessinformation"></span><span id="SYSTEMPROCESSINFORMATION"></span>

<span id="SystemProcessInformation"></span><span id="systemprocessinformation"></span><span id="SYSTEMPROCESSINFORMATION"></span>**SystemProcessInformation**


</dt> <dd>

Tableau de structures **d' \_ \_ informations de processus système** , un pour chaque processus s’exécutant dans le système.

Ces structures contiennent des informations sur l’utilisation des ressources de chaque processus, y compris le nombre de handles utilisés par le processus, l’utilisation du fichier de page de pic et le nombre de pages de mémoire allouées par le processus.

</dd> <dt>

<span id="SystemProcessorPerformanceInformation"></span><span id="systemprocessorperformanceinformation"></span><span id="SYSTEMPROCESSORPERFORMANCEINFORMATION"></span>

<span id="SystemProcessorPerformanceInformation"></span><span id="systemprocessorperformanceinformation"></span><span id="SYSTEMPROCESSORPERFORMANCEINFORMATION"></span>**SystemProcessorPerformanceInformation**


</dt> <dd>

Tableau des structures **d' \_ \_ \_ informations sur les performances du processeur système** , une pour chaque processeur installé dans le système.

</dd> <dt>

<span id="SystemInterruptInformation"></span><span id="systeminterruptinformation"></span><span id="SYSTEMINTERRUPTINFORMATION"></span>

<span id="SystemInterruptInformation"></span><span id="systeminterruptinformation"></span><span id="SYSTEMINTERRUPTINFORMATION"></span>**SystemInterruptInformation**


</dt> <dd>

Structure d' **\_ \_ informations d’interruption système** opaque qui peut être utilisée pour générer une valeur de départ imprévisible pour un générateur de nombres aléatoires. Utilisez à la place la fonction [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) .

</dd> <dt>

<span id="SystemExceptionInformation"></span><span id="systemexceptioninformation"></span><span id="SYSTEMEXCEPTIONINFORMATION"></span>

<span id="SystemExceptionInformation"></span><span id="systemexceptioninformation"></span><span id="SYSTEMEXCEPTIONINFORMATION"></span>**SystemExceptionInformation**


</dt> <dd>

Structure d' **\_ \_ informations d’exception système** opaque qui peut être utilisée pour générer une valeur de départ imprévisible pour un générateur de nombres aléatoires. Utilisez à la place la fonction [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) .

</dd> <dt>

<span id="SystemRegistryQuotaInformation"></span><span id="systemregistryquotainformation"></span><span id="SYSTEMREGISTRYQUOTAINFORMATION"></span>

<span id="SystemRegistryQuotaInformation"></span><span id="systemregistryquotainformation"></span><span id="SYSTEMREGISTRYQUOTAINFORMATION"></span>**SystemRegistryQuotaInformation**


</dt> <dd>

Structure **d' \_ \_ \_ informations de quota du Registre système** .

</dd> <dt>

<span id="SystemLookasideInformation"></span><span id="systemlookasideinformation"></span><span id="SYSTEMLOOKASIDEINFORMATION"></span>

<span id="SystemLookasideInformation"></span><span id="systemlookasideinformation"></span><span id="SYSTEMLOOKASIDEINFORMATION"></span>**SystemLookasideInformation**


</dt> <dd>

Structure d' **\_ \_ information de système** non opaque qui peut être utilisée pour générer une valeur de départ imprévisible pour un générateur de nombres aléatoires. Utilisez à la place la fonction [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) .

</dd> </dl> </dd> <dt>

*SystemInformation* \[ in, out\]
</dt> <dd>

Pointeur vers une mémoire tampon qui reçoit les informations demandées. La taille et la structure de ces informations varient en fonction de la valeur du paramètre *SystemInformationClass* , comme indiqué dans le tableau suivant.

<dt>

<span id="SYSTEM_BASIC_INFORMATION"></span><span id="system_basic_information"></span>

<span id="SYSTEM_BASIC_INFORMATION"></span><span id="system_basic_information"></span>**\_informations de base sur le système \_**


</dt> <dd>

Lorsque le paramètre *SystemInformationClass* est **SystemBasicInformation**, la mémoire tampon vers laquelle pointe le paramètre *SystemInformation* doit être suffisamment grande pour contenir une structure d' **\_ \_ information de base du système** unique ayant la disposition suivante :

``` syntax
typedef struct _SYSTEM_BASIC_INFORMATION {
    BYTE Reserved1[24];
    PVOID Reserved2[4];
    CCHAR NumberOfProcessors;
} SYSTEM_BASIC_INFORMATION;
```

Le membre **NumberOfProcessors** contient le nombre de processeurs présents dans le système. Utilisez [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) à la place pour récupérer ces informations.

Les autres membres de la structure sont réservés à un usage interne par le système d’exploitation.

</dd> <dt>

<span id="SYSTEM_PERFORMANCE_INFORMATION"></span><span id="system_performance_information"></span>

<span id="SYSTEM_PERFORMANCE_INFORMATION"></span><span id="system_performance_information"></span>**\_informations sur les performances du système \_**


</dt> <dd>

Lorsque le paramètre *SystemInformationClass* est **SystemPerformanceInformation**, la mémoire tampon vers laquelle pointe le paramètre *SystemInformation* doit être suffisamment grande pour contenir une structure d' **\_ \_ informations de performances système** opaque à utiliser pour générer une valeur de départ imprévisible pour un générateur de nombres aléatoires. À cet effet, la structure a la disposition suivante :

``` syntax
typedef struct _SYSTEM_PERFORMANCE_INFORMATION {
    BYTE Reserved1[312];
} SYSTEM_PERFORMANCE_INFORMATION;
```

Les membres individuels de la structure sont réservés à un usage interne par le système d’exploitation.

Utilisez plutôt la fonction [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) pour générer des données aléatoires du point de vue du chiffrement.

</dd> <dt>

<span id="SYSTEM_TIMEOFDAY_INFORMATION"></span><span id="system_timeofday_information"></span>

<span id="SYSTEM_TIMEOFDAY_INFORMATION"></span><span id="system_timeofday_information"></span>**\_informations sur la TimeOfDay du système \_**


</dt> <dd>

Lorsque le paramètre *SystemInformationClass* est **SystemTimeOfDayInformation**, la mémoire tampon vers laquelle pointe le paramètre *SystemInformation* doit être suffisamment grande pour contenir une structure d' **\_ \_ informations TimeOfDay du système** opaque à utiliser pour générer une valeur de départ imprévisible pour un générateur de nombres aléatoires. À cet effet, la structure a la disposition suivante :

``` syntax
typedef struct _SYSTEM_TIMEOFDAY_INFORMATION {
    BYTE Reserved1[48];
} SYSTEM_TIMEOFDAY_INFORMATION;
```

Les membres individuels de la structure sont réservés à un usage interne par le système d’exploitation.

Utilisez plutôt la fonction [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) pour générer des données aléatoires du point de vue du chiffrement.

</dd> <dt>

<span id="SYSTEM_PROCESS_INFORMATION"></span><span id="system_process_information"></span>

<span id="SYSTEM_PROCESS_INFORMATION"></span><span id="system_process_information"></span>**\_informations sur le processus système \_**


</dt> <dd>

Lorsque le paramètre *SystemInformationClass* est **SystemProcessInformation**, la mémoire tampon vers laquelle pointe le paramètre *SystemInformation* doit être suffisamment grande pour contenir un tableau qui contient autant de structures d' **\_ \_ informations sur le processus système** qu’il y a de processus en cours d’exécution dans le système. Chaque structure a la disposition suivante :

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

Le membre **NumberOfThreads** contient le nombre total de threads en cours d’exécution dans le processus.

Le membre **HandleCount** contient le nombre total de handles utilisés par le processus en question ; Utilisez [**GetProcessHandleCount**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocesshandlecount) pour récupérer ces informations à la place.

Le membre **PeakPagefileUsage** contient le nombre maximal d’octets du stockage de fichiers de pages utilisé par le processus, et le membre **PrivatePageCount** contient le nombre de pages mémoire allouées pour l’utilisation de ce processus.

Vous pouvez également récupérer ces informations à l’aide de la fonction [**GetProcessMemoryInfo**](/windows/desktop/api/psapi/nf-psapi-getprocessmemoryinfo) ou de la classe de [**\_ processus Win32**](/windows/desktop/CIMWin32Prov/win32-process) .

Les autres membres de la structure sont réservés à un usage interne par le système d’exploitation.

</dd> <dt>

<span id="SYSTEM_PROCESSOR_PERFORMANCE_INFORMATION"></span><span id="system_processor_performance_information"></span>

<span id="SYSTEM_PROCESSOR_PERFORMANCE_INFORMATION"></span><span id="system_processor_performance_information"></span>**\_ \_ informations sur les performances du processeur système \_**


</dt> <dd>

Lorsque le paramètre *SystemInformationClass* est **SystemProcessorPerformanceInformation**, la mémoire tampon vers laquelle pointe le paramètre *SystemInformation* doit être suffisamment grande pour contenir un tableau qui contient autant de structures d' **\_ \_ informations sur le processus système** qu’il y a de processeurs (UC) installés dans le système. Chaque structure a la disposition suivante :

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

Le membre **IdleTime** contient la durée pendant laquelle le système est inactif, en 1/centièmes de nanoseconde.

Le membre **KernelTime** contient la durée d’exécution du système en mode noyau (y compris tous les threads de tous les processus, sur tous les processeurs), en 1/centièmes de nanosecondes.

Le membre **UserTime** contient la durée d’exécution du système en mode utilisateur (y compris tous les threads de tous les processus, sur tous les processeurs), en 1/centièmes de nanosecondes.

Utilisez [**GetSystemTimes**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getsystemtimes) à la place pour récupérer ces informations.

</dd> <dt>

<span id="SYSTEM_INTERRUPT_INFORMATION"></span><span id="system_interrupt_information"></span>

<span id="SYSTEM_INTERRUPT_INFORMATION"></span><span id="system_interrupt_information"></span>**\_informations sur les interruptions système \_**


</dt> <dd>

Lorsque le paramètre *SystemInformationClass* est **SystemInterruptInformation**, la mémoire tampon vers laquelle pointe le paramètre *SystemInformation* doit être suffisamment grande pour contenir un tableau qui contient autant de structures d' **\_ \_ informations d’interruptions système** opaques qu’il n’y a de processeurs (UC) installés sur le système. Chaque structure, ou le tableau dans son ensemble, peut être utilisée pour générer une valeur de départ imprévisible pour un générateur de nombres aléatoires. À cet effet, la structure a la disposition suivante :

``` syntax
typedef struct _SYSTEM_INTERRUPT_INFORMATION {
    BYTE Reserved1[24];
} SYSTEM_INTERRUPT_INFORMATION;
```

Les membres individuels de la structure sont réservés à un usage interne par le système d’exploitation.

Utilisez plutôt la fonction [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) pour générer des données aléatoires du point de vue du chiffrement.

</dd> <dt>

<span id="SYSTEM_EXCEPTION_INFORMATION"></span><span id="system_exception_information"></span>

<span id="SYSTEM_EXCEPTION_INFORMATION"></span><span id="system_exception_information"></span>**\_informations sur l’exception système \_**


</dt> <dd>

Lorsque le paramètre *SystemInformationClass* est **SystemExceptionInformation**, la mémoire tampon vers laquelle pointe le paramètre *SystemInformation* doit être suffisamment grande pour contenir une structure d' **\_ \_ informations d’exception système** opaque à utiliser pour générer une valeur de départ imprévisible pour un générateur de nombres aléatoires. À cet effet, la structure a la disposition suivante :

``` syntax
typedef struct _SYSTEM_EXCEPTION_INFORMATION {
    BYTE Reserved1[16];
} SYSTEM_EXCEPTION_INFORMATION;
```

Les membres individuels de la structure sont réservés à un usage interne par le système d’exploitation.

Utilisez plutôt la fonction [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) pour générer des données aléatoires du point de vue du chiffrement.

</dd> <dt>

<span id="SYSTEM_REGISTRY_QUOTA_INFORMATION"></span><span id="system_registry_quota_information"></span>

<span id="SYSTEM_REGISTRY_QUOTA_INFORMATION"></span><span id="system_registry_quota_information"></span>**\_ \_ informations sur les quotas du Registre système \_**


</dt> <dd>

Lorsque le paramètre *SystemInformationClass* est **SystemRegistryQuotaInformation**, la mémoire tampon vers laquelle pointe le paramètre *SystemInformation* doit être suffisamment grande pour contenir une structure d' **\_ \_ \_ informations de quota du Registre du système** unique ayant la disposition suivante :

``` syntax
typedef struct _SYSTEM_REGISTRY_QUOTA_INFORMATION {
    ULONG RegistryQuotaAllowed;
    ULONG RegistryQuotaUsed;
    PVOID Reserved1;
} SYSTEM_REGISTRY_QUOTA_INFORMATION;
```

Le membre **RegistryQuotaAllowed** contient la taille maximale, en octets, que le registre peut atteindre sur ce système.

Le membre **RegistryQuotaUsed** contient la taille actuelle du Registre, en octets.

Utilisez [**GetSystemRegistryQuota**](/windows/desktop/api/Winbase/nf-winbase-getsystemregistryquota) à la place pour récupérer ces informations.

L’autre membre de la structure est réservé à un usage interne par le système d’exploitation.

</dd> <dt>

<span id="SYSTEM_LOOKASIDE_INFORMATION"></span><span id="system_lookaside_information"></span>

<span id="SYSTEM_LOOKASIDE_INFORMATION"></span><span id="system_lookaside_information"></span>**\_informations système \_**


</dt> <dd>

Lorsque le paramètre *SystemInformationClass* est **SystemLookasideInformation**, la mémoire tampon vers laquelle pointe le paramètre *SystemInformation* doit être suffisamment grande pour contenir une structure d' **\_ \_ informations de système** insuffisante pour une utilisation lors de la génération d’une valeur de départ imprévisible pour un générateur de nombres aléatoires. À cet effet, la structure a la disposition suivante :

``` syntax
typedef struct _SYSTEM_LOOKASIDE_INFORMATION {
    BYTE Reserved1[32];
} SYSTEM_LOOKASIDE_INFORMATION;
```

Les membres individuels de la structure sont réservés à un usage interne par le système d’exploitation.

Utilisez plutôt la fonction [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) pour générer des données aléatoires du point de vue du chiffrement.

</dd> </dl> </dd> <dt>

*SystemInformationLength* \[ dans\]
</dt> <dd>

Taille de la mémoire tampon vers laquelle pointe le paramètre *SystemInformation* , en octets.

</dd> <dt>

*ReturnLength* \[ out, facultatif\]
</dt> <dd>

Pointeur facultatif vers un emplacement où la fonction écrit la taille réelle des informations demandées. Si cette taille est inférieure ou égale au paramètre *SystemInformationLength* , la fonction copie les informations dans la mémoire tampon *SystemInformation* ; Sinon, elle retourne un code d’erreur NTSTATUS et retourne dans *ReturnLength* la taille de la mémoire tampon requise pour recevoir les informations demandées.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne un code d’erreur ou de réussite NTSTATUS.

Les formulaires et la signification des codes d’erreur de NTSTATUS sont répertoriés dans le fichier d’en-tête Ntstatus. h disponible dans le DDK et sont décrits dans la documentation du DDK.

## <a name="remarks"></a>Notes

La fonction **ZwQuerySystemInformation** et les structures qu’elle retourne sont internes au système d’exploitation et peuvent être modifiées d’une version de Windows à une autre. Pour maintenir la compatibilité de votre application, il est préférable d’utiliser les autres fonctions mentionnées précédemment.

Si vous utilisez **ZwQuerySystemInformation**, accédez à la fonction via la [liaison dynamique au moment de l’exécution](/windows/desktop/Dlls/using-run-time-dynamic-linking). Cela donne à votre code la possibilité de répondre correctement si la fonction a été modifiée ou supprimée du système d’exploitation. Toutefois, les modifications de signature peuvent ne pas être détectables.

Cette fonction n’a pas de bibliothèque d’importation associée. Vous devez utiliser les fonctions [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Ntdll.dll.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo)
</dt> <dt>

[**GetProcessHandleCount**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocesshandlecount)
</dt> <dt>

[**GetProcessMemoryInfo**](/windows/desktop/api/psapi/nf-psapi-getprocessmemoryinfo)
</dt> <dt>

[**GetSystemTimes**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getsystemtimes)
</dt> <dt>

[**GetSystemRegistryQuota**](/windows/desktop/api/Winbase/nf-winbase-getsystemregistryquota)
</dt> </dl>

 

