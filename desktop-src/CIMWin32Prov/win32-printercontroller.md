---
description: La \_ classe WMI de l’Association PrinterController Win32 associe une imprimante et l’appareil local auquel l’imprimante est connectée. Notez que cette classe retourne uniquement des instances pour les imprimantes locales.
ms.assetid: fb483b28-11f1-4153-893e-492f71763712
ms.tgt_platform: multiple
title: Classe Win32_PrinterController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterController
- Win32_PrinterController.AccessState
- Win32_PrinterController.Antecedent
- Win32_PrinterController.Dependent
- Win32_PrinterController.NegotiatedDataWidth
- Win32_PrinterController.NegotiatedSpeed
- Win32_PrinterController.NumberOfHardResets
- Win32_PrinterController.NumberOfSoftResets
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f987ee23b3dd7b65ec391e88200e59c86055e49a5cda23be4c529500359e789c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119759519"
---
# <a name="win32_printercontroller-class"></a>\_Classe PrinterController Win32

La [classe WMI](../wmisdk/retrieving-a-class.md) de l’Association **\_ PrinterController Win32** associe une imprimante et l’appareil local auquel l’imprimante est connectée. Notez que cette classe retourne uniquement des instances pour les imprimantes locales.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class Win32_PrinterController : CIM_ControlledBy
{
  uint16             AccessState;
  CIM_Controller REF Antecedent;
  Win32_Printer  REF Dependent;
  uint32             NegotiatedDataWidth;
  uint64             NegotiatedSpeed;
  uint32             NumberOfHardResets;
  uint32             NumberOfSoftResets;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ PrinterController** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ PrinterController** a ces propriétés.

<dl> <dt>

**AccessState**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

État de l’accès du contrôleur à l’appareil. Ces informations sont nécessaires lorsqu’un périphérique logique peut être utilisé par plusieurs contrôleurs, ou y accéder via.

Cette propriété est héritée de la [**\_ ControlledBy CIM**](cim-controlledby.md).

<dt>

<span id="0"></span>

<span id="0"></span>**entre**


</dt> <dd>

Unknown

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Actif

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Inactif

</dd> </dl>

</dd> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données **: \_ contrôleur CIM**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](../wmisdk/standard-qualifiers.md)
</dt> </dl>

Référence à l’instance de [**\_ contrôleur CIM**](cim-controller.md) représentant l’appareil local associé à cette imprimante.

Cette propriété est héritée de la [**\_ dépendance CIM**](cim-dependency.md).

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données **: \_ imprimante Win32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](../wmisdk/standard-qualifiers.md)
</dt> </dl>

Référence à l’instance d' [**\_ imprimante Win32**](win32-printer.md) représentant l’imprimante associée à l’appareil local.

Cette propriété est héritée de la [**\_ dépendance CIM**](cim-dependency.md).

</dd> <dt>

**NegotiatedDataWidth**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Largeur des données en cours d’utilisation entre les appareils (lorsque plusieurs largeurs de données de bus ou de connexion sont possibles). La largeur des données est spécifiée en bits. Si la largeur des données n’est pas négociée, ou si ces informations ne sont pas disponibles ou importantes pour la gestion des appareils, la propriété doit avoir la valeur 0 (zéro).

Cette propriété est héritée de la [**\_ DeviceConnection CIM**](cim-deviceconnection.md).

</dd> <dt>

**NegotiatedSpeed**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Vitesse d’utilisation entre les appareils (lorsque plusieurs vitesses de bus ou de connexion sont possibles). La vitesse est spécifiée en bits par seconde. Si les vitesses de connexion ou de bus ne sont pas négociées, ou si ces informations ne sont pas disponibles ou importantes pour la gestion des appareils, la propriété doit avoir la valeur 0 (zéro).

Cette propriété est héritée de la [**\_ DeviceConnection CIM**](cim-deviceconnection.md).

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**NumberOfHardResets**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre de réinitialisations matérielles émises par le contrôleur.

Cette propriété est héritée de la [**\_ ControlledBy CIM**](cim-controlledby.md).

</dd> <dt>

**NumberOfSoftResets**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre de réinitialisations logicielles émises par le contrôleur.

Cette propriété est héritée de la [**\_ ControlledBy CIM**](cim-controlledby.md).

</dd> </dl>

## <a name="remarks"></a>Remarques

La classe **Win32 \_ PrinterController** est dérivée de [**CIM \_ ControlledBy**](cim-controlledby.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                      |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                                |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>Win32 \_ Printer. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_CONTROLLEDBY CIM**](cim-controlledby.md)
</dt> <dt>

[Classes matérielles du système informatique](computer-system-hardware-classes.md)
</dt> </dl>

 

 
