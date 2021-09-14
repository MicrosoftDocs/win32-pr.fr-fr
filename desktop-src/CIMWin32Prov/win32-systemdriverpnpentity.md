---
description: la \_ classe WMI de l’association Win32 SystemDriverPNPEntity associe un appareil Plug-and-Play sur le système d’ordinateur exécutant Windows et le pilote qui prend en charge le périphérique Plug-and-Play.
ms.assetid: 2696c8e5-3bc3-42e3-807b-a387607c7c09
ms.tgt_platform: multiple
title: Classe Win32_SystemDriverPNPEntity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriverPNPEntity
- Win32_SystemDriverPNPEntity.Antecedent
- Win32_SystemDriverPNPEntity.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8b5a7eedfbd7a545e37cb9cda38c19cf61308761
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999438"
---
# <a name="win32_systemdriverpnpentity-class"></a>\_Classe SystemDriverPNPEntity Win32

la [classe WMI](../wmisdk/retrieving-a-class.md) de l’association **Win32 \_ SystemDriverPNPEntity** associe un appareil Plug-and-Play sur le système d’ordinateur exécutant Windows et le pilote qui prend en charge le périphérique Plug-and-Play.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{0800F074-CB98-11d2-B35D-00104BC97924}"), AMENDMENT]
class Win32_SystemDriverPNPEntity : CIM_Dependency
{
  Win32_PNPEntity    REF Antecedent;
  Win32_SystemDriver REF Dependent;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ SystemDriverPNPEntity** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ SystemDriverPNPEntity** a ces propriétés.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données : **Win32 \_ PNPEntity**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ PNPEntity")
</dt> </dl>

Représente l’appareil Plug-and-Play contrôlé par le pilote.

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données : **Win32 \_ SystemDriver**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**remplacement**](../wmisdk/standard-qualifiers.md) (« dépendant »), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI \| Win32 \_ SystemDriver »)
</dt> </dl>

[**\_ SystemDriver Win32**](win32-systemdriver.md) qui représente le pilote qui prend en charge l’appareil plug-and-Play.

</dd> </dl>

## <a name="remarks"></a>Notes

La classe **Win32 \_ SystemDriverPNPEntity** est dérivée de la [**\_ dépendance CIM**](cim-dependency.md).

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

[**\_Dépendance CIM**](cim-dependency.md)
</dt> <dt>

[Classes matérielles du système informatique](computer-system-hardware-classes.md)
</dt> </dl>

 

 
