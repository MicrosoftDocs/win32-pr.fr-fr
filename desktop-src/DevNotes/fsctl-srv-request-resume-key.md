---
description: Le code de contrôle de la \_ \_ clé de reprise de la demande FSCTL SRV \_ \_ est utilisé pour récupérer une référence de fichier opaque à utiliser avec le \_ Code de contrôle IOCTL COPYCHUNK.
ms.assetid: a6e0d253-5beb-4de8-8c40-d004f5794d47
title: Code de contrôle FSCTL_SRV_REQUEST_RESUME_KEY
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FSCTL_SRV_REQUEST_RESUME_KEY
api_type:
- NA
api_location: ''
ms.openlocfilehash: 8f11b70f7b4bfd05cbd5f7c29323f1dca00083a4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860661"
---
# <a name="fsctl_srv_request_resume_key-control-code"></a>Code de contrôle de la clé de reprise de la \_ demande FSCTL SRV \_ \_ \_

Le code de contrôle de la clé de reprise de la **\_ \_ demande \_ \_ FSCTL SRV** est utilisé pour récupérer une référence de fichier opaque à utiliser avec le code de contrôle [**IOCTL \_ COPYCHUNK**](ioctl-copychunk.md) .

Pour effectuer cette opération, appelez la fonction [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) avec les paramètres suivants.


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  FSCTL_SRV_REQUEST_RESUME_KEY, // dwIoControlCode
  NULL,                         // lpInBuffer
  0,                            // nInBufferSize
  (LPVOID) lpOutBuffer,         // output buffer
  (DWORD) nOutBufferSize,       // size of output buffer
  (LPDWORD) lpBytesReturned,    // number of bytes returned
  (LPOVERLAPPED) lpOverlapped   // OVERLAPPED structure
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hDevice* \[ dans\]
</dt> <dd>

Handle du fichier pour lequel la clé du fichier source doit être demandée. Pour obtenir ce descripteur, appelez la fonction [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) .

</dd> <dt>

*dwIoControlCode* \[ dans\]
</dt> <dd>

Code de contrôle de l’opération. Utilisez **la \_ \_ clé de \_ reprise \_ de la demande FSCTL SRV** pour cette opération.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Non utilisé avec cette opération ; Affectez la valeur **null**.

</dd> <dt>

*nInBufferSize* \[ dans\]
</dt> <dd>

Non utilisé avec cette opération ; défini à zéro.

</dd> <dt>

*lpOutBuffer* \[ à\]
</dt> <dd>

Pointeur vers la mémoire tampon de sortie, une structure de **\_ clé de \_ reprise \_ de demande SRV** . Pour plus d'informations, consultez la section Notes.

</dd> <dt>

*nOutBufferSize* \[ dans\]
</dt> <dd>

Taille de la mémoire tampon de sortie en octets.

</dd> <dt>

*lpBytesReturned* \[ à\]
</dt> <dd>

Pointeur vers une variable qui reçoit la taille des données stockées dans la mémoire tampon de sortie, en octets.

Si la mémoire tampon de sortie est trop petite, l’appel échoue, la fonction [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne l' **erreur \_ \_ mémoire tampon insuffisante** et *lpBytesReturned* est égal à zéro.

Si le paramètre *lpOverlapped* a la **valeur null**, *lpBytesReturned* ne peut pas avoir la **valeur null**. Même lorsqu’une opération ne retourne aucune donnée de sortie et que le paramètre *lpOutBuffer* a la **valeur null**, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) utilise *lpBytesReturned*. Après une telle opération, la valeur de *lpBytesReturned* est sans signification.

Si *lpOverlapped* n’a pas la **valeur null**, *LpBytesReturned* peut avoir la **valeur null**. Si *lpOverlapped* n’a pas la **valeur null** et que l’opération retourne des données, *lpBytesReturned* n’a aucun sens tant que l’opération avec chevauchement n’est pas terminée. Pour récupérer le nombre d’octets retournés, appelez la fonction [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) . Si le paramètre *hDevice* est associé à un port de terminaison d’e/s, vous pouvez récupérer le nombre d’octets renvoyés en appelant la fonction [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .

</dd> <dt>

*lpOverlapped* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) .

Si le paramètre *hDevice* a été ouvert sans spécifier d' **indicateur de fichier avec \_ \_ chevauchement**, *lpOverlapped* est ignoré.

Si *hDevice* a été ouvert avec l’indicateur de fichier avec l' **indicateur de \_ \_ chevauchement** , l’opération est exécutée en tant qu’opération Overlapped (asynchrone). Dans ce cas, *lpOverlapped* doit pointer vers une structure [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) valide qui contient un handle vers un objet d’événement. Dans le cas contraire, la fonction échoue de façon imprévisible.

Pour les opérations avec chevauchement, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) retourne immédiatement, et l’objet d’événement est signalé lorsque l’opération est terminée. Sinon, la fonction ne retourne pas jusqu’à ce que l’opération soit terminée ou jusqu’à ce qu’une erreur se produise.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si l’opération se termine correctement, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) retourne une valeur différente de zéro.

Si l’opération échoue ou est en attente, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) retourne la valeur zéro. Pour obtenir des informations détaillées sur l’erreur, appelez [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Remarques

Ce code de contrôle n’a aucun fichier d’en-tête associé. Vous devez définir le code de contrôle et les structures de données comme suit.

``` syntax
#define FSCTL_SRV_REQUEST_RESUME_KEY CTL_CODE(FILE_DEVICE_NETWORK_FILE_SYSTEM, 30, METHOD_BUFFERED, FILE_ANY_ACCESS)

typedef struct _SRV_RESUME_KEY {
    UINT64 ResumeKey;
    UINT64 Timestamp;
    UINT64 Pid;
} SRV_RESUME_KEY, *PSRV_RESUME_KEY;

typedef struct _SRV_REQUEST_RESUME_KEY {
    SRV_RESUME_KEY Key;
    ULONG  ContextLength;
    BYTE   Context[1];
} SRV_REQUEST_RESUME_KEY, *PSRV_REQUEST_RESUME_KEY;
```

Ces membres peuvent être décrits comme suit.



| Membre                                                                                                                       | Description                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ResumeKey"></span><span id="resumekey"></span><span id="RESUMEKEY"></span>**ResumeKey**<br/>                 | Valeur opaque qui identifie le fichier source sur le serveur.<br/>                                                                                                   |
| <span id="Timestamp"></span><span id="timestamp"></span><span id="TIMESTAMP"></span>**Confirmé**<br/>                 | Valeur opaque qui identifie l’heure à laquelle le fichier a été ouvert.<br/>                                                                                               |
| <span id="Pid"></span><span id="pid"></span><span id="PID"></span>**ELECTRIQUE**<br/>                                         | Valeur opaque qui identifie le processus qui a ouvert le fichier.<br/>                                                                                                |
| <span id="Key"></span><span id="key"></span><span id="KEY"></span>**Essentiel**<br/>                                         | Structure **de \_ \_ clé de reprise SRV** . Pour effectuer une opération de copie côté serveur, utilisez cette structure avec le code de contrôle [**IOCTL \_ COPYCHUNK**](ioctl-copychunk.md) .<br/> |
| <span id="ContextLength"></span><span id="contextlength"></span><span id="CONTEXTLENGTH"></span>**ContextLength**<br/> | Ce membre est réservé à l’usage du système ; n’utilisez pas.<br/>                                                                                                              |
| <span id="Context"></span><span id="context"></span><span id="CONTEXT"></span>**Contexte**<br/>                         | Ce membre est réservé à l’usage du système ; n’utilisez pas.<br/>                                                                                                              |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**\_COPYCHUNK IOCTL**](ioctl-copychunk.md)
</dt> </dl>

 

 
