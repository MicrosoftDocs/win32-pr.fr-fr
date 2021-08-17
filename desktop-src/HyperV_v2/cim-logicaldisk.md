---
description: Représente une plage contiguë de blocs logiques qui est identifiable par un système de fichiers par le biais du champ de l’ID de périphérique (clé) de disques.
ms.assetid: a70b4bee-7f5d-43b1-a7cc-7f0593bc8a11
title: Classe CIM_LogicalDisk (gestion Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDisk
- CIM_LogicalDisk.NameFormat
- CIM_LogicalDisk.NameNamespace
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0fccc6600e0eb5f04fd7d00360402ad85a94746e55781acbd6b1a35c7f9b94fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117812104"
---
# <a name="cim_logicaldisk-class-hyper-v-management"></a>Classe CIM_LogicalDisk (gestion Hyper-V)

Représente une plage contiguë de blocs logiques qui est identifiable par un système de fichiers par le biais du champ **DeviceID** (Key) du disque. par exemple, dans un environnement Windows, le champ **DeviceID** contient une lettre de lecteur. dans un environnement de UNIX, il contient le chemin d’accès ; dans un environnement NetWare, il contient le nom du volume.

## <a name="syntax"></a>Syntaxe

``` syntax
[Abstract, Version("2.15.0"), UMLPackagePath("CIM::Device::StorageExtents"), AMENDMENT]
class CIM_LogicalDisk : CIM_StorageExtent
{
  uint16 NameFormat = 12;
  uint16 NameNamespace = 8;
};
```

## <a name="members"></a>Membres

La classe de **\_ disque logique CIM** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe de **\_ disque logique CIM** possède ces propriétés.

<dl> <dt>

**NameFormat**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NameFormat")
</dt> </dl>

Indique si l’appareil logique utilise le format de nom du système d’exploitation.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Autre** (1)


</dt> <dd></dd> <dt>

<span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>

**Nom du périphérique du système d’exploitation** (12)


</dt> <dd></dd> </dl>

</dd> <dt>

**NameNamespace**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NameNamespace")
</dt> </dl>

Indique si l’unité logique a le même espace de noms que le système d’exploitation.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Autre** (1)


</dt> <dd></dd> <dt>

<span id="OS_Device_Namespace"></span><span id="os_device_namespace"></span><span id="OS_DEVICE_NAMESPACE"></span>

**Espace de noms du périphérique du système d’exploitation** (8)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8<br/>                                                                                    |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                                          |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_STORAGEEXTENT CIM**](cim-storageextent.md)
</dt> </dl>

 

