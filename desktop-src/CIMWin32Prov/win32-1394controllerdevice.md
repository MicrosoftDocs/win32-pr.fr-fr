---
description: La \_ classe WMI de l’Association 1394ControllerDevice Win32 associe le contrôleur de bus série haute vitesse (IEEE 1394 FireWire) et l' \_ instance du LogicalDevice CIM qui lui est connectée.
ms.assetid: 327fbced-4637-4402-a06f-6ac352da920c
ms.tgt_platform: multiple
title: Classe Win32_1394ControllerDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_1394ControllerDevice
- Win32_1394ControllerDevice.NegotiatedDataWidth
- Win32_1394ControllerDevice.NegotiatedSpeed
- Win32_1394ControllerDevice.AccessState
- Win32_1394ControllerDevice.NumberOfHardResets
- Win32_1394ControllerDevice.NumberOfSoftResets
- Win32_1394ControllerDevice.Antecedent
- Win32_1394ControllerDevice.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4877c5e1088e2cf801987d2729d02f64075fc73d1d48daba1fc83b20041c1758
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918109"
---
# <a name="win32_1394controllerdevice-class"></a>\_Classe 1394ControllerDevice Win32

La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de l’Association **\_ 1394ControllerDevice Win32** associe le contrôleur de bus série haute vitesse (IEEE 1394 FireWire) et l’instance du [**\_ LogicalDevice CIM**](cim-logicaldevice.md) qui lui est connectée. Ce bus série offre une connectivité améliorée pour un large éventail d’appareils, notamment les composants audio ou vidéo des consommateurs, les périphériques de stockage, les autres ordinateurs et les appareils portables. IEEE 1394 a été adopté par l’industrie de l’électronique grand public et fournit une interface d’extension compatible Plug-and-Play.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8835CFC9-BAEF-11d2-85E5-0000F8102E5F}"), AMENDMENT]
class Win32_1394ControllerDevice : CIM_ControlledBy
{
  uint32                   NegotiatedDataWidth;
  uint64                   NegotiatedSpeed;
  uint16                   AccessState;
  uint32                   NumberOfHardResets;
  uint32                   NumberOfSoftResets;
  Win32_1394Controller REF Antecedent;
  CIM_LogicalDevice    REF Dependent;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ 1394ControllerDevice** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ 1394ControllerDevice** a ces propriétés.

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

Type de données : **Win32 \_ 1394Controller**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ 1394Controller")
</dt> </dl>

La \_ référence antécédente Win32 1394Controller représente le contrôleur 1394 associé à cet appareil.

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données **: \_ LogicalDevice CIM**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) (« dépendant »), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« CIM \| CIM \_ LogicalDevice »)
</dt> </dl>

La \_ référence dépendante du LOGICALDEVICE CIM représente le \_ LogicalDevice CIM connecté au contrôleur 1394.

</dd> <dt>

**NegotiatedDataWidth**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« bits »)
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

Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« bits par seconde »)
</dt> </dl>

Lorsque plusieurs vitesses de bus ou de connexion sont possibles, cette propriété définit celle qui est utilisée entre les appareils. La vitesse est spécifiée en bits par seconde. Si les vitesses de connexion ou de bus ne sont pas négociées, ou si ces informations ne sont pas disponibles ou importantes pour la gestion des appareils, la propriété doit avoir la valeur 0 (zéro).

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

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

## <a name="remarks"></a>Remarques

La classe **Win32 \_ 1394ControllerDevice** est dérivée de [**CIM \_ ControlledBy**](cim-controlledby.md).

## <a name="examples"></a>Exemples

L’exemple de code PowerShell suivant récupère les informations de périphérique du contrôleur 1394.


```PowerShell
# Helper function to return AccessState

function get-WmiAccessState {
param ([uint16] $char)

# parse and return values

If ($char -le 2 -and $char -ge 0) {

switch ($char) {
0 {"00-Reserved"}
1 {"01-Reserved"}
2 {"02-Unknown"}
}
}

Else {
"$char - unknown value"
}
}

# Get 1394 Controller Device information from WMI
$1394Cont = Get-WMIObject Win32_1394ControllerDevice

# Display Details
"Win32_1394ControllerDevice WMI Information"
"=========================================="

foreach ($device in $1394Cont) {

"Device Characteristics - Device {0}" -f ++$i

"Access State : {0}" -f (Get-WmiAccessState($ch))
"Antecedent : {0}" -f $device.Antecedent
"Negotiated Data Width : {0}" -f $device.NegotiatedDataWidth
"Negotiated Speed : {0}" -f $device.NegotiatedSpeed
"Number of Hard Resets : {0}" -f $device.NumberofHardResets
"Number of Soft Resets : {0}" -f $device.NumberofSoftResets
} 
```



L’exemple de code précédent retourne les informations suivantes :

``` syntax
# Win32_1394ControllerDevice WMI Information

Device Characteristics -Device 1
Access State : 00-Reserved
Antecedent : \\UK0N055\root\CIMV2:Win32_1394Controller.DeviceID="PCI\\VEN_1217&DEV_00F7&SUBSYS_01CC1028
&REV_02\\4&2FE911E8&0&0CF0"
Negotiated Data Width :
Negotiated Speed :
Number of Hard Resets :
Number of Soft Resets :
```

## <a name="requirements"></a>Configuration requise



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

 

