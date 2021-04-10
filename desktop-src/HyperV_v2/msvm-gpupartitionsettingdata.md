---
description: Représente l’état configuré d’un périphérique de partition GPU.
ms.assetid: 33ec4ea2-4e79-4c84-8abe-da8308ad6702
title: Classe Msvm_GpuPartitionSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GpuPartitionSettingData
- Msvm_GpuPartitionSettingData.MinPartitionVRAM
- Msvm_GpuPartitionSettingData.MaxPartitionVRAM
- Msvm_GpuPartitionSettingData.OptimalPartitionVRAM
- Msvm_GpuPartitionSettingData.MinPartitionEncode
- Msvm_GpuPartitionSettingData.MaxPartitionEncode
- Msvm_GpuPartitionSettingData.OptimalPartitionEncode
- Msvm_GpuPartitionSettingData.MinPartitionDecode
- Msvm_GpuPartitionSettingData.MaxPartitionDecode
- Msvm_GpuPartitionSettingData.OptimalPartitionDecode
- Msvm_GpuPartitionSettingData.MinPartitionCompute
- Msvm_GpuPartitionSettingData.MaxPartitionCompute
- Msvm_GpuPartitionSettingData.OptimalPartitionCompute
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7d8c9809b3a062654eaf0fb7a73b75b0188f7284
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951288"
---
# <a name="msvm_gpupartitionsettingdata-class"></a>MSVM \_ GpuPartitionSettingData, classe

Représente l’état configuré d’un périphérique de partition GPU.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GpuPartitionSettingData : CIM_ResourceAllocationSettingData
{
  uint64 MinPartitionVRAM;
  uint64 MaxPartitionVRAM;
  uint64 OptimalPartitionVRAM;
  uint64 MinPartitionEncode;
  uint64 MaxPartitionEncode;
  uint64 OptimalPartitionEncode;
  uint64 MinPartitionDecode;
  uint64 MaxPartitionDecode;
  uint64 OptimalPartitionDecode;
  uint64 MinPartitionCompute;
  uint64 MaxPartitionCompute;
  uint64 OptimalPartitionCompute;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ GpuPartitionSettingData** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ GpuPartitionSettingData** possède les propriétés suivantes.

<dl> <dt>

**MaxPartitionCompute**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Quantité maximale de moteurs de calcul qui s’affichera dans la partition GPU.

</dd> <dt>

**MaxPartitionDecode**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Quantité maximale de moteurs de décodage qui s’affichent dans la partition GPU.

</dd> <dt>

**MaxPartitionEncode**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Quantité maximale de moteurs d’encodage qui s’affiche dans la partition GPU.

</dd> <dt>

**MaxPartitionVRAM**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Quantité maximale de VRAM qui s’affichera dans la partition GPU.

</dd> <dt>

**MinPartitionCompute**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Quantité minimale de moteurs de calcul qui s’affichera dans la partition GPU.

</dd> <dt>

**MinPartitionDecode**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Quantité minimale de moteurs de décodage qui s’affichent dans la partition GPU.

</dd> <dt>

**MinPartitionEncode**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Quantité minimale de moteurs d’encodage qui s’affiche dans la partition GPU.

</dd> <dt>

**MinPartitionVRAM**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Quantité minimale de VRAM qui apparaîtra dans la partition GPU.

</dd> <dt>

**OptimalPartitionCompute**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Quantité optimale de moteurs de calcul qui s’affichera dans la partition GPU.

</dd> <dt>

**OptimalPartitionDecode**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Quantité optimale de moteurs de décodage qui s’affichent dans la partition GPU.

</dd> <dt>

**OptimalPartitionEncode**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Quantité optimale de moteurs d’encodage qui s’affiche dans la partition GPU.

</dd> <dt>

**OptimalPartitionVRAM**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Quantité optimale de VRAM qui apparaîtra dans la partition GPU.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows 10, version 1703 \[ uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2016<br/>                                                                          |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_RESOURCEALLOCATIONSETTINGDATA CIM**](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

 




