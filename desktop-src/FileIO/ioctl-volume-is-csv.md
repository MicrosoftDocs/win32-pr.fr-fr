---
description: Détermine si un volume est un volume partagé de cluster.
ms.assetid: 6B09B519-1E2F-4757-AAD5-1E4C81023E14
title: IOCTL_VOLUME_IS_CSV le code de contrôle (Ntddvol. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_VOLUME_IS_CSV
api_type:
- HeaderDef
api_location:
- Ntddvol.h
ms.openlocfilehash: 8121e1b89c88ad05a2c2be8537d7170bfabfc412
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320393"
---
# <a name="ioctl_volume_is_csv-control-code"></a>\_Le volume IOCTL \_ est \_ le code de contrôle CSV

Détermine si un volume est un volume partagé de cluster.

Pour effectuer cette opération, appelez la fonction [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) avec les paramètres suivants.


```C++
BOOL 
WINAPI 
DeviceIoControl( (HANDLE) hDevice,              // handle to device
                 IOCTL_VOLUME_IS_CSV,           // dwIoControlCode
                 NULL,                          // input buffer
                 0,                             // size of input buffer
                 (LPVOID) lpOutBuffer,          // lpOutBuffer
                 (DWORD) nOutBufferSize,        // nOutBufferSize
                 (LPDWORD) lpBytesReturned,     // number of bytes returned
                 (LPOVERLAPPED) lpOverlapped ); // OVERLAPPED structure
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hDevice* 
</dt> <dd>

Handle vers le volume. Pour récupérer un handle de volume, appelez la fonction [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) . Seuls les administrateurs peuvent ouvrir des descripteurs de volume.

</dd> <dt>

*dwIoControlCode* 
</dt> <dd>

Code de contrôle de l’opération. L’utilisation du **\_ volume IOCTL \_ est \_ CSV** pour cette opération.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Non utilisé avec cette opération ; Affectez la valeur **null**.

</dd> <dt>

*nInBufferSize* 
</dt> <dd>

Non utilisé avec cette opération ; a la valeur zéro (0).

</dd> <dt>

*lpOutBuffer* 
</dt> <dd>

Pointeur vers **true** si le volume est un volume partagé de cluster (CSV); dans le cas contraire, l’appel de fonction échoue.

</dd> <dt>

*nOutBufferSize* 
</dt> <dd>

Taille de la mémoire tampon de sortie en octets.

</dd> <dt>

*lpBytesReturned* 
</dt> <dd>

Pointeur vers une variable qui reçoit la taille des données stockées dans la mémoire tampon de sortie, en octets.

Si *lpOverlapped* a la **valeur null**, *lpBytesReturned* ne peut pas avoir la **valeur null**. Même lorsqu’une opération ne retourne aucune donnée de sortie et que *lpOutBuffer* a la **valeur null**, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) utilise *lpBytesReturned*. Après une telle opération, la valeur de *lpBytesReturned* est sans signification.

Si *lpOverlapped* n’a pas la **valeur null**, *LpBytesReturned* peut avoir la **valeur null**. Si ce paramètre n’est pas **null** et que l’opération retourne des données, *lpBytesReturned* n’a pas de sens tant que l’opération avec chevauchement n’est pas terminée. Pour récupérer le nombre d’octets retournés, appelez [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult). Si *hDevice* est associé à un port de terminaison d’e/s, vous pouvez récupérer le nombre d’octets retournés en appelant [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus).

</dd> <dt>

*lpOverlapped* 
</dt> <dd>

Pointeur vers une structure [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .

Si *hDevice* a été ouvert sans spécifier d' **indicateur de fichier avec \_ \_ chevauchement**, *lpOverlapped* est ignoré.

Si *hDevice* a été ouvert avec l’indicateur de fichier avec l' **indicateur de \_ \_ chevauchement** , l’opération est exécutée en tant qu’opération Overlapped (asynchrone). Dans ce cas, *lpOverlapped* doit pointer vers une structure [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) valide qui contient un handle vers un objet d’événement. Dans le cas contraire, la fonction échoue de façon imprévisible.

Pour les opérations avec chevauchement, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retourne immédiatement, et l’objet d’événement est signalé lorsque l’opération est terminée. Sinon, la fonction ne retourne pas jusqu’à ce que l’opération soit terminée ou qu’une erreur se produise.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si l’opération se termine correctement, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retourne une valeur différente de zéro.

Si l’opération échoue ou est en attente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retourne la valeur zéro (0). Pour obtenir des informations détaillées sur l’erreur, appelez [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Ntddvol. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[Codes de contrôle de gestion des volumes](volume-management-control-codes.md)
</dt> </dl>

 

