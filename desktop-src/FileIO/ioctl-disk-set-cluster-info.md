---
description: Définit les informations de cluster sur un disque.
ms.assetid: AB2243D9-4913-4412-87E0-2C8DB8AB10B8
title: IOCTL_DISK_SET_CLUSTER_INFO le code de contrôle (NTDDDISK. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_DISK_SET_CLUSTER_INFO
api_type:
- HeaderDef
api_location:
- Ntdddisk.h
ms.openlocfilehash: 4ba0994dd1c9030e84c22e24b1eb4583eba7e3d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545091"
---
# <a name="ioctl_disk_set_cluster_info-control-code"></a>\_Code de \_ contrôle d' \_ informations de cluster IOCTL Disk Set \_

Définit les informations de cluster sur un disque.

Pour effectuer cette opération, appelez la fonction [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) avec les paramètres suivants.


```C++
BOOL 
WINAPI 
DeviceIoControl( (HANDLE)       hDevice,         // handle to device 
                 IOCTL_DISK_SET_CLUSTER_INFO,    // dwIoControlCode
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

Utilisez **les \_ \_ informations du \_ cluster \_ d’ensemble de disques IOCTL** pour cette opération.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Pointeur vers une structure de données d' [**\_ \_ informations de cluster de disque**](disk-cluster-info.md) qui contient des informations de cluster pour le disque.

</dd> <dt>

*nInBufferSize* 
</dt> <dd>

Taille de la mémoire tampon d’entrée, en octets.

</dd> <dt>

*lpOutBuffer* 
</dt> <dd>

Non utilisé avec cette opération. Affectez la valeur **null**.

</dd> <dt>

*nOutBufferSize* 
</dt> <dd>

Taille de la mémoire tampon de sortie en octets. Défini sur 0 (zéro).

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
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>NTDDDISK. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[Codes de contrôle de gestion des disques](disk-management-control-codes.md)
</dt> <dt>

[**\_informations sur le cluster de disque \_**](disk-cluster-info.md)
</dt> <dt>

[**\_informations de \_ cluster d’extraction de disque IOCTL \_ \_**](ioctl-disk-get-cluster-info.md)
</dt> </dl>

 

