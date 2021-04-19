---
description: Représente l’état de la partition GPU.
ms.assetid: 319b37d5-b5f0-4251-9482-316347a9015b
title: Classe Msvm_GpuPartition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GpuPartition
- Msvm_GpuPartition.DeviceInstancePath
- Msvm_GpuPartition.PartitionId
- Msvm_GpuPartition.PartitionVfLuid
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cc0975644609832c692f5522cc756240f7a5bff6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524891"
---
# <a name="msvm_gpupartition-class"></a>MSVM \_ GpuPartition, classe

Représente l’état de la partition GPU.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GpuPartition : CIM_LogicalDevice
{
  string DeviceInstancePath;
  uint16 PartitionId;
  string PartitionVfLuid;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ GpuPartition** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ GpuPartition** possède les propriétés suivantes.

<dl> <dt>

**DeviceInstancePath**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chaîne contenant le chemin d’accès à l’instance d’appareil qui identifie l’unité de partition GPU.

</dd> <dt>

**PartitionId**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

ID de partition de l’unité de partition GPU.

</dd> <dt>

**PartitionVfLuid**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

La fonction virtuelle LUID, qui représente une partition GPU.

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

[**\_LOGICALDEVICE CIM**](cim-logicaldevice.md)
</dt> </dl>

 

 




