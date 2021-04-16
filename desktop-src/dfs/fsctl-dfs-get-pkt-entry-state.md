---
title: FSCTL_DFS_GET_PKT_ENTRY_STATE, code de contrôle (LmDfs.h)
description: Le code de contrôle FSCTL_DFS_GET_PKT_ENTRY_STATE peut obtenir les mêmes informations que la fonction NetDfsGetClientInfo, mais peut fournir de meilleures performances dans certaines configurations avec des latences élevées aux serveurs DFS.
ms.assetid: d4eec104-128b-43b5-9fae-08ab0b977dec
topic_type:
- apiref
api_name:
- FSCTL_DFS_GET_PKT_ENTRY_STATE
api_location:
- LmDfs.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a57fb448934908ebc1530e95a298715324aaee6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524031"
---
# <a name="fsctl_dfs_get_pkt_entry_state-control-code"></a>Code de contrôle FSCTL_DFS_GET_PKT_ENTRY_STATE

Le code de contrôle **FSCTL_DFS_GET_PKT_ENTRY_STATE** peut obtenir les mêmes informations que la fonction [**NetDfsGetClientInfo**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo) , mais peut fournir de meilleures performances dans certaines configurations avec des latences élevées aux serveurs DFS. Il n’est pas recommandé d’utiliser le code de contrôle **FSCTL_DFS_GET_PKT_ENTRY_STATE** , sauf s’il existe des problèmes de performances.

Pour effectuer cette opération, appelez la fonction [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) avec les paramètres suivants.

```C++
BOOL 
   WINAPI 
   DeviceIoControl( (HANDLE)       hDevice,            // handle to device
                    (DWORD)        FSCTL_DFS_GET_PKT_ENTRY_STATE, // dwIoControlCode(LPDWORD)      lpInBuffer,         // input buffer
                    (DWORD)        nInBufferSize,      // size of input buffer
                    (LPDWORD)      lpOutBuffer,        // output buffer
                    (DWORD)        nOutBufferSize,     // size of output buffer
                    (LPDWORD)      lpBytesReturned,    // number of bytes returned
                    (LPOVERLAPPED) lpOverlapped );     // OVERLAPPED structure
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*hDevice* [in]
</dt> <dd>

Handle de l’appareil. Pour obtenir un descripteur d’appareil, appelez la fonction [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .

</dd> <dt>

*dwIoControlCode* [in]
</dt> <dd>

Code de contrôle de l’opération. Utilisez **FSCTL_DFS_GET_PKT_ENTRY_STATE** pour cette opération.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Adresse d’une structure [**DFS_GET_PKT_ENTRY_STATE_ARG**](/windows/win32/api/lmdfs/ns-lmdfs-dfs_get_pkt_entry_state_arg) et des chaînes Unicode 1-3 qui suivent.

</dd> <dt>

*nInBufferSize* [in]
</dt> <dd>

Taille, en octets, de la mémoire tampon vers laquelle pointe le paramètre *lpInBuffer* .

</dd> <dt>

*lpOutBuffer* [out]
</dt> <dd>

Adresse d’une **structure \# DFS_INFO_** et toute chaîne et structure vers laquelle pointe la **structure \# DFS_INFO_** . La structure spécifique retournée dépend du membre de **niveau** de la structure [**DFS_GET_PKT_ENTRY_STATE_ARG**](/windows/win32/api/lmdfs/ns-lmdfs-dfs_get_pkt_entry_state_arg) passée dans la mémoire tampon d’entrée.

</dd> <dt>

*nOutBufferSize* [in]
</dt> <dd>

Taille, en octets, de la mémoire tampon vers laquelle pointe le paramètre *lpOutBuffer* . En raison des chaînes et des structures référencées par la **structure \# DFS_INFO_** retournée qui se trouvent également dans la mémoire tampon de sortie, cette mémoire tampon doit être plus grande que la structure **DFS_INFO_ \#** spécifiée.

</dd> <dt>

*lpBytesReturned* [out]
</dt> <dd>

Pointeur vers une variable qui reçoit la taille des données stockées dans la mémoire tampon de sortie, en octets.

Si la mémoire tampon de sortie est trop petite, mais au moins suffisamment grande pour contenir une **valeur DWORD**, l’appel échoue, [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne **ERROR_MORE_DATA**, et le premier **DWORD** de la mémoire tampon de sortie contient la taille requise. Si la mémoire tampon de sortie ne peut pas contenir de **valeur DWORD** , l’appel échoue avec **ERROR_INSUFFICIENT_BUFFER**, et *lpBytesReturned* est égal à zéro.

Si *lpOverlapped* a la **valeur null**, *lpBytesReturned* ne peut pas avoir la **valeur null**. Même lorsqu’une opération ne retourne aucune donnée de sortie et que *lpOutBuffer* a la **valeur null**, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) utilise *lpBytesReturned*. Après une telle opération, la valeur de *lpBytesReturned* est sans signification.

Si *lpOverlapped* n’a pas la **valeur null**, *LpBytesReturned* peut avoir la **valeur null**. Si ce paramètre n’est pas **null** et que l’opération retourne des données, *lpBytesReturned* n’a pas de sens tant que l’opération avec chevauchement n’est pas terminée. Pour récupérer le nombre d’octets retournés, appelez [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult). Si le paramètre *hDevice* est associé à un port de terminaison d’e/s, vous pouvez récupérer le nombre d’octets renvoyés en appelant [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus).

</dd> <dt>

*lpOverlapped* [in]
</dt> <dd>

Pointeur vers une structure [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) .

Si *hDevice* a été ouvert sans spécifier **FILE_FLAG_OVERLAPPED**, *lpOverlapped* est ignoré.

Si *hDevice* a été ouvert avec l’indicateur **FILE_FLAG_OVERLAPPED** , l’opération est exécutée en tant qu’opération Overlapped (asynchrone). Dans ce cas, *lpOverlapped* doit pointer vers une structure [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) valide qui contient un handle vers un objet d’événement. Dans le cas contraire, la fonction échoue de façon imprévisible.

Pour les opérations avec chevauchement, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) retourne immédiatement, et l’objet d’événement est signalé lorsque l’opération est terminée. Sinon, la fonction ne retourne pas jusqu’à ce que l’opération soit terminée ou qu’une erreur se produise.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si l’opération se termine correctement, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retourne une valeur différente de zéro.

Si l’opération échoue ou est en attente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retourne la valeur zéro. Pour obtenir des informations détaillées sur l’erreur, appelez [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                             |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                                       |
| En-tête<br/>                   | <dl> <dt>LmDfs. h (inclure LmDfs. h)</dt> </dl> |

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**NetDfsGetClientInfo**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo)
</dt> </dl>
