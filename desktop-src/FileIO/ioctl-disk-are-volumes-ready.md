---
description: Attend que tous les volumes du disque spécifié soient prêts à être utilisés.
ms.assetid: 6cf619bb-7ff5-485e-b533-0f7f6503c6e0
title: IOCTL_DISK_ARE_VOLUMES_READY le code de contrôle (NTDDDISK. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_DISK_ARE_VOLUMES_READY
api_type:
- HeaderDef
api_location:
- ntdddisk.h
ms.openlocfilehash: cba83d8f850151e217460595f5f4fc8831b99ee5ee30fc0bb908c0ca04a9cdce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119981969"
---
# <a name="ioctl_disk_are_volumes_ready-control-code"></a>\_Le disque IOCTL \_ est un code de \_ \_ contrôle prêt pour les volumes

Attend que tous les volumes du disque spécifié soient prêts à être utilisés.

Pour effectuer cette opération, appelez la fonction [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) avec les paramètres suivants.


```C++
BOOL 
WINAPI 
DeviceIoControl( (HANDLE)       hDevice,         // handle to device 
                 IOCTL_DISK_ARE_VOLUMES_READY,   // dwIoControlCode
                 (LPVOID)       NULL,            // lpInBuffer 
                 (DWORD)        0,               // nInBufferSize 
                 (LPVOID)       NULL,            // lpOutBuffer 
                 (DWORD)        0,               // nOutBufferSize
                 (LPDWORD)      lpBytesReturned, // number of bytes returned
                 (LPOVERLAPPED) lpOverlapped );  // OVERLAPPED structure
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hDevice* 
</dt> <dd>

Handle sur le disque.

Pour récupérer un handle d’appareil, appelez la fonction [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) .

</dd> <dt>

*dwIoControlCode* 
</dt> <dd>

Code de contrôle de l’opération.

Utilisez **le \_ disque IOCTL \_ les \_ volumes sont \_ prêts** pour cette opération.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Non utilisé avec cette opération. Affectez la valeur **null**.

</dd> <dt>

*nInBufferSize* 
</dt> <dd>

Taille de la mémoire tampon d’entrée, en octets. Défini sur 0 (zéro).

</dd> <dt>

*lpOutBuffer* 
</dt> <dd>

Non utilisé avec cette opération. Affectez la valeur **null**.

</dd> <dt>

*nOutBufferSize* 
</dt> <dd>

Non utilisé avec cette opération. Défini sur 0 (zéro).

</dd> <dt>

*lpBytesReturned* 
</dt> <dd>

Non utilisé avec cette opération. Affectez la valeur **null**.

</dd> <dt>

*lpOverlapped* 
</dt> <dd>

Pointeur vers une structure [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .

Si *hDevice* a été ouvert sans spécifier d' **indicateur de fichier avec \_ \_ chevauchement**, *lpOverlapped* est ignoré.

Si *hDevice* a été ouvert avec l’indicateur de fichier avec l' **indicateur de \_ \_ chevauchement** , l’opération est exécutée en tant qu’opération Overlapped (asynchrone). Dans ce cas, *lpOverlapped* doit pointer vers une structure [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) valide qui contient un handle vers un objet d’événement. Dans le cas contraire, la fonction échoue de façon imprévisible.

Pour les opérations avec chevauchement, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retourne immédiatement, et l’objet d’événement est signalé lorsque l’opération est terminée. Sinon, la fonction ne retourne pas jusqu’à ce que l’opération soit terminée ou qu’une erreur se produise.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si l’opération se termine correctement, ce qui indique que tous les volumes sur le disque sont prêts à être utilisés, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retourne une valeur différente de zéro.

Si l’opération échoue ou est en attente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retourne la valeur zéro. Pour obtenir des informations détaillées sur l’erreur, appelez [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>NTDDDISK. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[Codes de contrôle de gestion des disques](disk-management-control-codes.md)
</dt> </dl>

 

