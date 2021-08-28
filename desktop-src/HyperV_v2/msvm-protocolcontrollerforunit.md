---
description: Cette Association indique qu’une sous-classe de l’unité logique (par exemple, un volume de stockage) est connectée par le biais d’un contrôleur de protocole spécifique.
ms.assetid: 93025450-BE6C-48DC-913C-2050674DF81A
title: Classe Msvm_ProtocolControllerForUnit
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ProtocolControllerForUnit
- Msvm_ProtocolControllerForUnit.Antecedent
- Msvm_ProtocolControllerForUnit.Dependent
- Msvm_ProtocolControllerForUnit.DeviceNumber
- Msvm_ProtocolControllerForUnit.AccessPriority
- Msvm_ProtocolControllerForUnit.AccessState
- Msvm_ProtocolControllerForUnit.DeviceAccess
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 73b8478e561d53212e0439219622595751ad954e13d0d086fabdbf57a483039d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086629"
---
# <a name="msvm_protocolcontrollerforunit-class"></a>MSVM \_ ProtocolControllerForUnit, classe

Cette Association indique qu’une sous-classe de l’unité logique (par exemple, un volume de stockage) est connectée par le biais d’un contrôleur de protocole spécifique. Dans de nombreux cas (par exemple, le masquage de LUN de stockage), de nombreuses associations peuvent être utilisées pour établir un lien avec différents objets. Par conséquent, des sous-classes ont été définies pour optimiser l’énumération des associations.

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ProtocolControllerForUnit : CIM_ProtocolControllerForUnit
{
  CIM_ProtocolController REF Antecedent;
  CIM_LogicalDevice      REF Dependent;
  string                     DeviceNumber;
  uint16                     AccessPriority;
  uint16                     AccessState;
  uint16                     DeviceAccess;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ ProtocolControllerForUnit** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ ProtocolControllerForUnit** possède les propriétés suivantes.

<dl> <dt>

**AccessPriority**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Priorité donnée aux accès de l’appareil par le biais de ce contrôleur. Le chemin d’accès avec la priorité la plus élevée aura la valeur la plus faible pour ce paramètre. Cette classe est héritée de **CIM \_ ProtocolControllerForDevice**.

</dd> <dt>

**AccessState**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si le contrôleur commande ou accède activement à l’appareil (2) ou non (3). En outre, la valeur 0 (inconnu) peut être définie. Ces informations sont nécessaires lorsqu’un périphérique logique peut être utilisé par des contrôleurs de protocole, ou être accessible via plusieurs contrôleurs de protocole. Cette classe est héritée de **CIM \_ ProtocolControllerForDevice**.

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)
</dt> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>**Actif** (2)
</dt> <dt>

<span id="Inactive_"></span><span id="inactive_"></span><span id="INACTIVE_"></span>**Inactif** (3)
</dt> </dl>

</dd> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données : **[ **CIM \_ ProtocolController**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Contrôleur de protocole. Cette classe est héritée de la [**\_ dépendance CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données : **[ **\_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Périphérique contrôlé. Cette classe est héritée de la [**\_ dépendance CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).

</dd> <dt>

**DeviceAccess**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Droits d’accès accordés à l’appareil via ce contrôleur. Cette classe est héritée de **CIM \_ ProtocolControllerForUnit**.



| Valeur                                                                               | Signification                    |
|-------------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>0</dt> </dl>        | Unknown<br/>         |
| <dl> <dt>2</dt> </dl>        | Lecture/écriture<br/>      |
| <dl> <dt>3</dt> </dl>        | Lecture seule<br/>       |
| <dl> <dt>4</dt> </dl>        | Pas d'accès.<br/>      |
| <dl> <dt>5.. 15999</dt> </dl> | DMTF, réservé<br/>   |
| <dl> <dt>16000..</dt> </dl>  | Fournisseur réservé<br/> |



 

</dd> <dt>

**DeviceNumber**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Adresse de l’appareil associé dans le contexte du contrôleur antécédent. Cette classe est héritée de **CIM \_ ProtocolControllerForDevice**.

</dd> </dl>

## <a name="remarks"></a>Remarques

L’accès à la classe **MSVM \_ ProtocolControllerForUnit** peut être limité par le filtrage UAC. Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_PROTOCOLCONTROLLERFORUNIT CIM**](cim-protocolcontrollerforunit.md)
</dt> <dt>

[**\_PROTOCOLCONTROLLERFORUNIT CIM**](/previous-versions//cc150672(v=vs.85))
</dt> <dt>

[Stockage Catégories](storage-classes.md)
</dt> </dl>

 

