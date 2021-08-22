---
description: Récupère les attributs du périphérique de disque spécifié.
ms.assetid: 2FF81F67-9E70-43C6-A504-0D60382E0945
title: IOCTL_DISK_GET_CLUSTER_INFO le code de contrôle (NTDDDISK. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_DISK_GET_CLUSTER_INFO
api_type:
- HeaderDef
api_location:
- Ntdddisk.h
ms.openlocfilehash: 3acf923a9f0288bd3fe3a0b12d4c61b71437f61c1c4f96a3a3bef1af5f05fd95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068679"
---
# <a name="ioctl_disk_get_cluster_info-control-code"></a>\_Code de \_ contrôle \_ d' \_ informations de cluster d’IOCTL Disk

Récupère les attributs du périphérique de disque spécifié.

Pour effectuer cette opération, appelez la fonction [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) avec les paramètres suivants.


```C++
BOOL 
WINAPI 
DeviceIoControl( (HANDLE)       hDevice,         // handle to device 
                 IOCTL_DISK_GET_CLUSTER_INFO,    // dwIoControlCode
                 (LPVOID)       NULL,            // lpInBuffer 
                 (DWORD)        0,               // nInBufferSize 
                 (LPVOID)       lpOutBuffer,     // output buffer:GET_DISK_ATTRIBUTES
                 (DWORD)        nOutBufferSize,  // size of output buffer
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

Utilisez **le \_ disque IOCTL \_ obtenir des \_ \_ informations de cluster** pour cette opération.

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

Pointeur vers une mémoire tampon qui reçoit une structure de données d' [**\_ \_ informations de cluster de disque**](disk-cluster-info.md) .

</dd> <dt>

*nOutBufferSize* 
</dt> <dd>

Taille de la mémoire tampon de sortie en octets.

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
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                             |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>NTDDDISK. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[Codes de contrôle de gestion des disques](disk-management-control-codes.md)
</dt> <dt>

[**\_informations sur le cluster de disque \_**](disk-cluster-info.md)
</dt> <dt>

[**\_informations de \_ cluster d’ensemble de disques IOCTL \_ \_**](ioctl-disk-set-cluster-info.md)
</dt> </dl>

 

