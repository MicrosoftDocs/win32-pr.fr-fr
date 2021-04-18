---
description: Types de partition valides utilisés par les pilotes de disque.
ms.assetid: b2e15b93-a02b-4d6f-b242-b5ec9a30c97b
title: Types de partition de disque (WinIoCtl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4109d4386d4892ca695fe8876b61501110cef455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536583"
---
# <a name="disk-partition-types"></a>Types de partition de disque

Le tableau suivant identifie les types de partition valides qui sont utilisés par les pilotes de disque.



| Constante/valeur                                                                                                                                                                                                                                      | Description                                                                                                                                                |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PARTITION_ENTRY_UNUSED"></span><span id="partition_entry_unused"></span><dl> <dt>**Partition \_ ENTRÉE \_ non utilisée**</dt> <dt>0x00</dt> </dl> | Partition d’entrée inutilisée.<br/>                                                                                                                      |
| <span id="PARTITION_EXTENDED"></span><span id="partition_extended"></span><dl> <dt>**Partition \_**</dt> <dt>0x05</dt> étendu </dl>              | Partition étendue.<br/>                                                                                                                          |
| <span id="PARTITION_FAT_12"></span><span id="partition_fat_12"></span><dl> <dt>**Partition \_ FAT \_ 12**</dt> <dt>0x01</dt> </dl>                   | Partition de système de fichiers FAT12.<br/>                                                                                                                  |
| <span id="PARTITION_FAT_16"></span><span id="partition_fat_16"></span><dl> <dt>**Partition \_ FAT \_ 16**</dt> <dt>0x04</dt> </dl>                   | Partition de système de fichiers FAT16.<br/>                                                                                                                  |
| <span id="PARTITION_FAT32"></span><span id="partition_fat32"></span><dl> <dt>**Partition \_**</dt> <dt>0x0B</dt> FAT32 </dl>                       | Partition de système de fichiers FAT32.<br/>                                                                                                                  |
| <span id="PARTITION_IFS"></span><span id="partition_ifs"></span><dl> <dt>**Partition \_**</dt>Le <dt>0x07</dt> IFS </dl>                             | Partition IFS.<br/>                                                                                                                               |
| <span id="PARTITION_LDM"></span><span id="partition_ldm"></span><dl> <dt>**Partition \_ LDM**</dt> <dt>0x42</dt> </dl>                             | Partition LDM (Logical Disk Manager).<br/>                                                                                                         |
| <span id="PARTITION_NTFT"></span><span id="partition_ntft"></span><dl> <dt>**Partition \_ NTFT**</dt> <dt>0x80</dt> </dl>                          | Une partition NTFT.<br/>                                                                                                                              |
| <span id="VALID_NTFT"></span><span id="valid_ntft"></span><dl> <dt>**Valide \_ NTFT**</dt> <dt>0xC0</dt> </dl>                                      | Une partition NTFT valide.<br/> Le bit le plus élevé d’un code de type de partition indique qu’une partition fait partie d’un miroir NTFT ou d’un tableau agrégé par bandes.<br/> |



## <a name="remarks"></a>Notes

Plusieurs macros peuvent vous aider à détecter le type de partition : **IsContainerPartition**, **IsFTPartition** et **IsRecognizedPartition**. Pour plus d’informations, consultez WinIoCtl. h.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                                               |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>WinIoCtl. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**informations de PARTITION \_ \_ ex**](/windows/desktop/api/WinIoCtl/ns-winioctl-partition_information_ex)
</dt> <dt>

[**\_MBR des informations de partition \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-partition_information_mbr)
</dt> <dt>

[**DÉFINIR \_ les \_ informations de partition**](/windows/desktop/api/WinIoCtl/ns-winioctl-set_partition_information)
</dt> </dl>

 

 




