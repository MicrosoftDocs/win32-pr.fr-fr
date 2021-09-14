---
description: La \_ classe WMI de l’Association POTSModemToSerialPort Win32 associe un modem au port série utilisé par le modem.
ms.assetid: 4dbde5ae-f785-4d2d-80d9-508effd72cf2
ms.tgt_platform: multiple
title: Classe Win32_POTSModemToSerialPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_POTSModemToSerialPort
- Win32_POTSModemToSerialPort.NegotiatedDataWidth
- Win32_POTSModemToSerialPort.NegotiatedSpeed
- Win32_POTSModemToSerialPort.AccessState
- Win32_POTSModemToSerialPort.NumberOfHardResets
- Win32_POTSModemToSerialPort.NumberOfSoftResets
- Win32_POTSModemToSerialPort.Dependent
- Win32_POTSModemToSerialPort.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0a1e6128ffde7afce0132dd4415e4eca1f06b5cb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999472"
---
# <a name="win32_potsmodemtoserialport-class"></a>\_Classe POTSModemToSerialPort Win32

La [classe WMI](../wmisdk/retrieving-a-class.md) de l’Association **\_ POTSModemToSerialPort Win32** associe un modem au port série utilisé par le modem.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4B6-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_POTSModemToSerialPort : CIM_ControlledBy
{
  uint32               NegotiatedDataWidth;
  uint64               NegotiatedSpeed;
  uint16               AccessState;
  uint32               NumberOfHardResets;
  uint32               NumberOfSoftResets;
  Win32_POTSModem  REF Dependent;
  Win32_SerialPort REF Antecedent;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ POTSModemToSerialPort** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ POTSModemToSerialPort** a ces propriétés.

<dl> <dt>

**AccessState**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si le contrôleur commande ou accède activement à l’appareil. Ces informations sont nécessaires lorsqu’un périphérique logique peut être utilisé par plusieurs contrôleurs, ou y accéder via.

Cette propriété est héritée de la [**\_ ControlledBy CIM**](cim-controlledby.md).

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Inconnu** (0)


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

**Actif** (1)


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

**Inactif** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données : **Win32 \_ SerialPort**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ SerialPort")
</dt> </dl>

Un [**\_ SerialPort Win32**](win32-serialport.md) qui représente le port série utilisé par le modem.

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données : **Win32 \_ POTSModem**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**remplacement**](../wmisdk/standard-qualifiers.md) (« dépendant »), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI \| Win32 \_ POTSModem »)
</dt> </dl>

[**\_ POTSModem Win32**](win32-potsmodem.md) qui représente le modem pots utilisant le port série.

</dd> <dt>

**NegotiatedDataWidth**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**unités**](../wmisdk/standard-qualifiers.md) (« bits »)
</dt> </dl>

Lorsque plusieurs largeurs de données de bus ou de connexion sont possibles, cette propriété définit celle qui est utilisée entre les appareils. La largeur des données est spécifiée en bits. Si la largeur des données n’est pas négociée, ou si ces informations ne sont pas disponibles ou importantes pour la gestion des appareils, la propriété doit avoir la valeur 0 (zéro).

Cette propriété est héritée de la [**\_ DeviceConnection CIM**](cim-deviceconnection.md).

</dd> <dt>

**NegotiatedSpeed**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**unités**](../wmisdk/standard-qualifiers.md) (« bits par seconde »)
</dt> </dl>

Lorsque plusieurs vitesses de bus ou de connexion sont possibles, cette propriété définit celle qui est utilisée entre les appareils. La vitesse est spécifiée en bits par seconde. Si les vitesses de connexion ou de bus ne sont pas négociées, ou si ces informations ne sont pas disponibles ou importantes pour la gestion des appareils, la propriété doit avoir la valeur 0 (zéro).

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](../wmisdk/creating-a-wmi-script.md).

Cette propriété est héritée de la [**\_ DeviceConnection CIM**](cim-deviceconnection.md).

</dd> <dt>

**NumberOfHardResets**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre de réinitialisations matérielles émises par le contrôleur. Une réinitialisation matérielle retourne l’appareil à son état d’initialisation ou de démarrage. Toutes les informations sur l’état de l’appareil interne et les données sont perdues.

Cette propriété est héritée de la [**\_ ControlledBy CIM**](cim-controlledby.md).

</dd> <dt>

**NumberOfSoftResets**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre de réinitialisations logicielles émises par le contrôleur. Une réinitialisation logicielle n’efface pas complètement l’état actuel de l’appareil et les données. Les sémantiques exactes dépendent de l’appareil et des protocoles et mécanismes utilisés pour communiquer avec lui.

Cette propriété est héritée de la [**\_ ControlledBy CIM**](cim-controlledby.md).

</dd> </dl>

## <a name="remarks"></a>Notes

La classe **Win32 \_ POTSModemToSerialPort** est dérivée de [**CIM \_ ControlledBy**](cim-controlledby.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_CONTROLLEDBY CIM**](cim-controlledby.md)
</dt> <dt>

[Classes matérielles du système informatique](computer-system-hardware-classes.md)
</dt> </dl>

 

 
