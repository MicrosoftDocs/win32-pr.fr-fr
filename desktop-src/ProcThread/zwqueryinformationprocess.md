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
ms.openlocfilehash: af47ecbe69c4c0449cf6e3282e0992e8a513b5a0
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480875"
---
# <a name="zwqueryinformationprocess-function"></a>ZwQueryInformationProcess fonction)

\[Les **ZwQueryInformationProcess** peuvent être modifiés ou non disponibles dans les futures versions de Windows. Les applications doivent utiliser les autres fonctions présentées dans cette rubrique.\]

Récupère des informations sur le processus spécifié.

## <a name="syntax"></a>Syntaxe


```C++
NTSTATUS WINAPI ZwQueryInformationProcess(
  _In_      HANDLE           ProcessHandle,
  _In_      PROCESSINFOCLASS ProcessInformationClass,
  _Out_     PVOID            ProcessInformation,
  _In_      ULONG            ProcessInformationLength,
  _Out_opt_ PULONG           ReturnLength
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ProcessHandle* \[ dans\]
</dt> <dd>

Handle vers le processus dont les informations doivent être récupérées.

</dd> <dt>

*ProcessInformationClass* \[ dans\]
</dt> <dd>

Type d’informations de processus à récupérer. Ce paramètre peut avoir l’une des valeurs suivantes de l’énumération **PROCESSINFOCLASS** .




| Valeur | Signification | 
|-------|---------|
| <span id="ProcessBasicInformation"></span><span id="processbasicinformation"></span><span id="PROCESSBASICINFORMATION"></span><dl><dt><strong>ProcessBasicInformation</strong></dt><dt>0</dt></dl> | Récupère un pointeur vers une structure PEB qui peut être utilisée pour déterminer si le processus spécifié est en cours de débogage, et une valeur unique utilisée par le système pour identifier le processus spécifié. <br /> Il est préférable d’utiliser les fonctions <a href="/windows/desktop/api/debugapi/nf-debugapi-checkremotedebuggerpresent"><strong>CheckRemoteDebuggerPresent</strong></a> et <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocessid"><strong>GetProcessID,</strong></a> pour obtenir ces informations.<br /> | 
| <span id="ProcessDebugPort"></span><span id="processdebugport"></span><span id="PROCESSDEBUGPORT"></span><dl><dt><strong>ProcessDebugPort</strong></dt><dt>7</dt></dl> | Récupère une valeur <strong>DWORD_PTR</strong> qui est le numéro de port du débogueur pour le processus. Une valeur différente de zéro indique que le processus est en cours d’exécution sous le contrôle d’un débogueur ring 3.<br /> Il est préférable d’utiliser la fonction <a href="/windows/desktop/api/debugapi/nf-debugapi-checkremotedebuggerpresent"><strong>CheckRemoteDebuggerPresent</strong></a> ou <a href="/windows/desktop/api/debugapi/nf-debugapi-isdebuggerpresent"><strong>IsDebuggerPresent</strong></a> .<br /> | 
| <span id="ProcessWow64Information"></span><span id="processwow64information"></span><span id="PROCESSWOW64INFORMATION"></span><dl><dt><strong>ProcessWow64Information</strong></dt><dt>26</dt></dl> | Détermine si le processus s’exécute dans l’environnement WOW64 (WOW64 est l’émulateur x86 qui permet aux applications Win32 de s’exécuter sur les Windows 64 bits).<br /> Il est préférable d’utiliser la fonction <a href="/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process"><strong>IsWow64Process</strong></a> pour obtenir ces informations.<br /> | 
| <span id="ProcessImageFileName"></span><span id="processimagefilename"></span><span id="PROCESSIMAGEFILENAME"></span><dl><dt><strong>ProcessImageFileName</strong></dt><dt>27</dt></dl> | Récupère une valeur <strong>UNICODE_STRING</strong> contenant le nom du fichier image pour le processus.<br /> | 
| <span id="ProcessBreakOnTermination"></span><span id="processbreakontermination"></span><span id="PROCESSBREAKONTERMINATION"></span><dl><dt><strong>ProcessBreakOnTermination</strong></dt><dt>29</dt></dl> | Récupère une valeur <strong>ULong</strong> indiquant si le processus est considéré comme critique.<br /><blockquote>[!Note]<br />cette valeur peut être utilisée à partir de Windows XP avec SP3. à partir de Windows 8.1, <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-isprocesscritical"><strong>IsProcessCritical</strong></a> doit être utilisé à la place.</blockquote><br /> | 
| <span id="ProcessProtectionInformation"></span><span id="processprotectioninformation"></span><span id="PROCESSPROTECTIONINFORMATION"></span><dl><dt><strong>ProcessProtectionInformation</strong></dt><dt>61</dt></dl> | Récupère une valeur d’octet qui indique le type de processus protégé et le signataire de processus protégé.<br /> | 




 

</dd> <dt>

*ProcessInformation* \[ à\]
</dt> <dd>

Pointeur vers une mémoire tampon fournie par l’application appelante dans laquelle la fonction écrit les informations demandées. La taille des informations écrites varie en fonction de la valeur du paramètre *ProcessInformationClass* :

<dl> <dt>

<span id="PROCESS_BASIC_INFORMATION"></span><span id="process_basic_information"></span>TRAITER \_ les \_ informations de base
</dt> <dd>

Lorsque le paramètre *ProcessInformationClass* est **ProcessBasicInformation**, la mémoire tampon vers laquelle pointe le paramètre *ProcessInformation* doit être suffisamment grande pour contenir une structure d' **\_ \_ informations de base de processus** unique ayant la disposition suivante :

``` syntax
typedef struct _PROCESS_BASIC_INFORMATION {
    PVOID Reserved1;
    PPEB PebBaseAddress;
    PVOID Reserved2[2];
    ULONG_PTR UniqueProcessId;
    PVOID Reserved3;
} PROCESS_BASIC_INFORMATION;
```

Le membre **UniqueProcessId** pointe vers l’identificateur unique du système pour ce processus. Il est préférable d’utiliser la fonction [**GetProcessID,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessid) pour récupérer ces informations.

Le membre **PebBaseAddress** pointe vers une structure [**PEB**](/windows/desktop/api/Winternl/ns-winternl-peb) .

Les autres membres de cette structure sont réservés à un usage interne par le système d’exploitation.

</dd> <dt>

<span id="ULONG_PTR"></span><span id="ulong_ptr"></span>ULONG ( \_ PTR)
</dt> <dd>

Lorsque le paramètre *ProcessInformationClass* est **ProcessWow64Information**, la mémoire tampon vers laquelle pointe le paramètre *ProcessInformation* doit être suffisamment grande pour contenir **un \_ ptr ulong**. Si cette valeur est différente de zéro, le processus s’exécute dans un environnement WOW64 ; Sinon, si la valeur est égale à zéro, le processus ne s’exécute pas dans un environnement WOW64.

Il est préférable d’utiliser la fonction [**IsWow64Process**](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process) pour déterminer si un processus s’exécute dans l’environnement WOW64.

</dd> <dt>

<span id="UNICODE_STRING"></span><span id="unicode_string"></span>\_chaîne Unicode
</dt> <dd>

Lorsque le paramètre *ProcessInformationClass* est **ProcessImageFileName**, la mémoire tampon vers laquelle pointe le paramètre *ProcessInformation* doit être suffisamment grande pour contenir une structure de **\_ chaîne Unicode** , ainsi que la chaîne elle-même. La chaîne stockée dans le membre de la **mémoire tampon** est le nom du fichier image.

Si la mémoire tampon est trop petite, la fonction échoue avec le \_ code d’erreur d’incompatibilité de la longueur des informations d’état \_ \_ et le paramètre *ReturnLength* est défini sur la taille de mémoire tampon requise.

</dd> <dt>

<span id="PS_PROTECTION"></span><span id="ps_protection"></span>PS_PROTECTION
</dt> <dd>

Lorsque le paramètre *ProcessInformationClass* est **ProcessProtectionInformation**, la mémoire tampon vers laquelle pointe le paramètre *ProcessInformation* doit être suffisamment grande pour contenir une structure **PS_PROTECTION** unique ayant la disposition suivante :

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

Les 3 premiers bits contiennent le type de processus protégé :

``` syntax
typedef enum _PS_PROTECTED_TYPE {
    PsProtectedTypeNone = 0,
    PsProtectedTypeProtectedLight = 1,
    PsProtectedTypeProtected = 2
} PS_PROTECTED_TYPE, *PPS_PROTECTED_TYPE;
```

Les 4 premiers bits contiennent le signataire de processus protégé :

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

*ProcessInformationLength* \[ dans\]
</dt> <dd>

Taille de la mémoire tampon vers laquelle pointe le paramètre *ProcessInformation* , en octets.

</dd> <dt>

*ReturnLength* \[ out, facultatif\]
</dt> <dd>

Pointeur vers une variable dans laquelle la fonction retourne la taille des informations demandées. Si la fonction a réussi, il s’agit de la taille des informations écrites dans la mémoire tampon vers laquelle pointe le paramètre *ProcessInformation* , mais si la mémoire tampon est trop petite, il s’agit de la taille minimale de la mémoire tampon nécessaire pour recevoir correctement les informations.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne un code d’erreur ou de réussite NTSTATUS.

Les formulaires et la signification des codes d’erreur de NTSTATUS sont répertoriés dans le fichier d’en-tête Ntstatus. h disponible dans le DDK, et sont décrits dans la documentation du DDK sous Kernel-Mode architecture du pilote/Guide de conception/Guide de conception/techniques de programmation des pilotes/erreurs de journalisation.

## <a name="remarks"></a>Remarques

la fonction **ZwQueryInformationProcess** et les structures qu’elle retourne sont internes au système d’exploitation et peuvent être modifiées d’une version de Windows à une autre. Pour maintenir la compatibilité de votre application, il est préférable d’utiliser à la place les fonctions publiques mentionnées dans la description du paramètre *ProcessInformationClass* .

Si vous utilisez **ZwQueryInformationProcess**, accédez à la fonction via la [liaison dynamique au moment de l’exécution](../dlls/using-run-time-dynamic-linking.md). Cela donne à votre code la possibilité de répondre correctement si la fonction a été modifiée ou supprimée du système d’exploitation. Toutefois, les modifications de signature peuvent ne pas être détectables.

Cette fonction n’a pas de bibliothèque d’importation associée. Vous devez utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Ntdll.dll.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CheckRemoteDebuggerPresent**](/windows/win32/api/debugapi/nf-debugapi-checkremotedebuggerpresent)
</dt> <dt>

[**GetProcessID,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessid)
</dt> <dt>

[**IsDebuggerPresent**](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent)
</dt> <dt>

[**IsWow64Process**](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process)
</dt> </dl>

 

 
