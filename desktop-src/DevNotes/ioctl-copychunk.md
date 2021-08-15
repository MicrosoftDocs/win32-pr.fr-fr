---
description: Le \_ Code de contrôle IOCTL COPYCHUNK initie une copie côté serveur d’une plage de données, également appelée un segment.
ms.assetid: 36f68840-bd5c-4cfc-a8ad-0cfbbdc5a2a9
title: Code de contrôle IOCTL_COPYCHUNK
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COPY_CHUNK
api_type:
- NA
api_location: ''
ms.openlocfilehash: 415e94d8ed19d3248beb31d8a5e6327e1adc11078483d4f60fcd42699e4dab89
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001729"
---
# <a name="ioctl_copychunk-control-code"></a>\_Code de contrôle COPYCHUNK IOCTL

Le code de contrôle **IOCTL \_ COPYCHUNK** initie une copie côté serveur d’une plage de données, également appelée un segment.

Pour effectuer cette opération, appelez la fonction [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) avec les paramètres suivants.


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  IOCTL_COPYCHUNK,              // dwIoControlCode
  (LPVOID) lpInBuffer,          // input buffer
  (DWORD) nInBufferSize,        // size of input buffer
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

Handle du fichier qui est la cible de l’opération de copie côté serveur. Pour obtenir ce descripteur, appelez la fonction [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) .

</dd> <dt>

*dwIoControlCode* \[ dans\]
</dt> <dd>

Code de contrôle de l’opération. Utilisez **IOCTL \_ COPYCHUNK** pour cette opération.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Pointeur vers la mémoire tampon d’entrée, une structure de **\_ \_ copie COPYCHUNK SRV** . Pour plus d'informations, consultez la section Notes.

</dd> <dt>

*nInBufferSize* \[ dans\]
</dt> <dd>

Taille de la mémoire tampon d’entrée, en octets.

</dd> <dt>

*lpOutBuffer* \[ à\]
</dt> <dd>

Pointeur vers la mémoire tampon de sortie, une structure de **\_ \_ réponse SRV COPYCHUNK** . Pour plus d'informations, consultez la section Notes.

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
#define IOCTL_COPYCHUNK CTL_CODE(FILE_DEVICE_NETWORK_FILE_SYSTEM, 262, METHOD_BUFFERED,  FILE_READ_ACCESS)

typedef struct _SRV_COPYCHUNK {
    LARGE_INTEGER SourceOffset;
    LARGE_INTEGER DestinationOffset;
    ULONG  Length;
} SRV_COPYCHUNK, *PSRV_COPYCHUNK;

typedef struct _SRV_COPYCHUNK_COPY {
    SRV_RESUME_KEY SourceFile;
    ULONG          ChunkCount;
    ULONG          Reserved;
    SRV_COPYCHUNK  Chunk[1];    // Array
} SRV_COPYCHUNK_COPY, *PSRV_COPYCHUNK_COPY;

typedef struct _SRV_COPYCHUNK_RESPONSE {
    ULONG          ChunksWritten;
    ULONG          ChunkBytesWritten;
    ULONG          TotalBytesWritten;
} SRV_COPYCHUNK_RESPONSE, *PSRV_COPYCHUNK_RESPONSE;
```

Ces membres peuvent être décrits comme suit.



| Membre                                                                                                                                       | Description                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SourceOffset"></span><span id="sourceoffset"></span><span id="SOURCEOFFSET"></span>**SourceOffset**<br/>                     | Offset, en octets, entre le début du fichier source et le segment à copier.<br/>                                                                                                                                                                                                                                                                     |
| <span id="DestinationOffset"></span><span id="destinationoffset"></span><span id="DESTINATIONOFFSET"></span>**DestinationOffset**<br/> | Offset, en octets, entre le début du fichier cible et l’emplacement où le segment doit être copié.<br/>                                                                                                                                                                                                                                               |
| <span id="Length"></span><span id="length"></span><span id="LENGTH"></span>**Base**<br/>                                             | Nombre d’octets de données dans le bloc à copier. Doit être supérieur à zéro et inférieur ou égal à 1 Mo. **Longueur** \* **ChunkCount** doit être inférieur ou égal à 16 Mo.<br/>                                                                                                                                                                         |
| <span id="SourceFile"></span><span id="sourcefile"></span><span id="SOURCEFILE"></span>**SourceFile**<br/>                             | Clé qui représente le fichier source avec les données à copier. Cette clé est obtenue via [**la \_ \_ clé de \_ reprise \_ de la demande FSCTL SRV**](fsctl-srv-request-resume-key.md).<br/>                                                                                                                                                                                   |
| <span id="ChunkCount"></span><span id="chunkcount"></span><span id="CHUNKCOUNT"></span>**ChunkCount**<br/>                             | Nombre de segments à copier. Doit être supérieur à zéro et inférieur ou égal à 256.<br/>                                                                                                                                                                                                                                                                |
| <span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Réservé**<br/>                                     | Ce membre est réservé à l’usage du système ; n’utilisez pas.<br/>                                                                                                                                                                                                                                                                                                        |
| <span id="Chunk"></span><span id="chunk"></span><span id="CHUNK"></span>**Transfert**<br/>                                                 | Tableau de structures **ChunkCount** **SRV \_ COPYCHUNK** , un pour chaque segment à copier. La longueur, en octets, de ce tableau doit être **ChunkCount** \* sizeof (**SRV \_ COPYCHUNK**).<br/>                                                                                                                                                                       |
| <span id="ChunksWritten"></span><span id="chunkswritten"></span><span id="CHUNKSWRITTEN"></span>**ChunksWritten**<br/>                 | Si l’opération a échoué avec un **paramètre d’erreur \_ non valide \_**, cette valeur indique le nombre maximal de segments que le serveur acceptera dans une seule requête, qui est 256. Sinon, cette valeur indique le nombre de segments qui ont été écrits avec succès.<br/>                                                                                               |
| <span id="ChunkBytesWritten"></span><span id="chunkbyteswritten"></span><span id="CHUNKBYTESWRITTEN"></span>**ChunkBytesWritten**<br/> | Si l’opération a échoué avec un **paramètre d’erreur \_ non valide \_**, cette valeur indique le nombre maximal d’octets que le serveur autorisera à écrire en un seul segment, soit 1 Mo. Sinon, cette valeur indique le nombre d’octets qui ont été correctement écrits dans le dernier segment qui n’a pas été traité avec succès (si une écriture partielle s’est produite).<br/> |
| <span id="TotalBytesWritten"></span><span id="totalbyteswritten"></span><span id="TOTALBYTESWRITTEN"></span>**TotalBytesWritten**<br/> | Si l’opération a échoué avec un **paramètre d’erreur \_ non valide \_**, cette valeur indique le nombre maximal d’octets que le serveur doit copier dans une seule requête, qui est de 16 Mo. Sinon, cette valeur indique le nombre d’octets qui ont été écrits avec succès.<br/>                                                                                                 |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**clé de reprise de la \_ demande FSCTL SRV \_ \_ \_**](fsctl-srv-request-resume-key.md)
</dt> </dl>

 

 
