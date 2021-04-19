---
description: Représente une association entre un contrôleur de protocole et une unité logique exposée.
ms.assetid: e8bf2b32-b4a6-4963-8a50-2b06776965e8
title: Classe CIM_ProtocolControllerForUnit
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProtocolControllerForUnit
- CIM_ProtocolControllerForUnit.Antecedent
- CIM_ProtocolControllerForUnit.Dependent
- CIM_ProtocolControllerForUnit.DeviceAccess
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 26020745057d5963ed4a892ba8639ac078aaa20b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536743"
---
# <a name="cim_protocolcontrollerforunit-class"></a>\_Classe CIM ProtocolControllerForUnit

Représente une association entre un contrôleur de protocole et une unité logique exposée.

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Abstract, Version("2.8.0"), UMLPackagePath("CIM::Device::ProtocolController"), AMENDMENT]
class CIM_ProtocolControllerForUnit : CIM_ProtocolControllerForDevice
{
  CIM_ProtocolController REF Antecedent;
  CIM_LogicalDevice      REF Dependent;
  uint16                     DeviceAccess;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ ProtocolControllerForUnit** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ ProtocolControllerForUnit** possède les propriétés suivantes.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données : **CIM \_ ProtocolController**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Contrôleur de protocole.

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données **: \_ LogicalDevice CIM**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)
</dt> </dl>

Unité logique associée au contrôleur de protocole.

</dd> <dt>

**DeviceAccess**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Droits d’accès accordés à l’unité logique via le contrôleur de protocole.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Inconnu** (0)


</dt> <dd></dd> <dt>

<span id="Read_Write"></span><span id="read_write"></span><span id="READ_WRITE"></span>

**Lecture/écriture** (2)


</dt> <dd></dd> <dt>

<span id="Read-Only"></span><span id="read-only"></span><span id="READ-ONLY"></span>

**Lecture seule** (3)


</dt> <dd></dd> <dt>

<span id="No_Access"></span><span id="no_access"></span><span id="NO_ACCESS"></span>

**Aucun accès** (4)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF réservé** (5.. 15999)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Fournisseur réservé** (16000...)


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

[**\_PROTOCOLCONTROLLERFORDEVICE CIM**](cim-protocolcontrollerfordevice.md)
</dt> </dl>

 

