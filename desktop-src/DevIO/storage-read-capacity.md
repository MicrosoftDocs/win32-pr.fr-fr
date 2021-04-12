---
description: Contient des informations sur la taille d’un appareil. Elle est retournée à partir du \_ Code de contrôle de capacité de lecture du stockage IOCTL \_ \_ .
ms.assetid: bd18f4b7-f87e-48f6-b7c2-68990beb8d36
title: Structure STORAGE_READ_CAPACITY (Ntddstor. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STORAGE_READ_CAPACITY
api_type:
- HeaderDef
api_location:
- Ntddstor.h
ms.openlocfilehash: e57a9f4420b977598e15f9aae219c060665c9d0d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104392991"
---
# <a name="storage_read_capacity-structure"></a>Structure de la capacité de lecture du stockage \_ \_

Contient des informations sur la taille d’un appareil. Elle est retournée à partir du code de contrôle de [**\_ capacité de \_ lecture \_ du stockage IOCTL**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_read_capacity) .

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _STORAGE_READ_CAPACITY {
  ULONG         Version;
  ULONG         Size;
  ULONG         BlockLength;
  LARGE_INTEGER NumberOfBlocks;
  LARGE_INTEGER DiskLength;
} STORAGE_READ_CAPACITY, *PSTORAGE_READ_CAPACITY;
```



## <a name="members"></a>Membres

<dl> <dt>

**Version**
</dt> <dd>

Version de cette structure. L’appelant doit affecter à ce membre la valeur `sizeof(STORAGE_READ_CAPACITY)` .

</dd> <dt>

**Taille**
</dt> <dd>

Taille des données retournées.

</dd> <dt>

**BlockLength**
</dt> <dd>

Nombre d’octets par bloc.

</dd> <dt>

**NumberOfBlocks**
</dt> <dd>

Nombre total de blocs sur le disque.

</dd> <dt>

**DiskLength**
</dt> <dd>

Taille du disque en octets.

</dd> </dl>

## <a name="remarks"></a>Notes

Le fichier d’en-tête Ntddstor. h est disponible dans le kit WDK (Windows Driver Kit).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2008, Windows Server 2003 avec SP1<br/>                          |
| En-tête<br/>                   | <dl> <dt>Ntddstor. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_capacité de \_ lecture du stockage IOCTL \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_read_capacity)
</dt> </dl>

 

 




