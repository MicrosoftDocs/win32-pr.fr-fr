---
description: La \_ classe WMI de l’Association DeviceBus Win32 associe un bus système et un périphérique logique à l’aide du bus. Cette classe est utilisée pour détecter les appareils sur lesquels le bus est utilisé.
ms.assetid: 2d7d83a5-c058-40c0-aab3-7700f4067a16
ms.tgt_platform: multiple
title: Classe Win32_DeviceBus
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DeviceBus
- Win32_DeviceBus.Dependent
- Win32_DeviceBus.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2dde01ee6b3f3be026dbc19f8c4b8e2c238f4ff2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126921876"
---
# <a name="win32_devicebus-class"></a>\_Classe DeviceBus Win32

La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de l’Association **\_ DeviceBus Win32** associe un bus système et un périphérique logique à l’aide du bus. Cette classe est utilisée pour détecter les appareils sur lesquels le bus est utilisé.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C50F-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DeviceBus : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  Win32_Bus         REF Antecedent;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ DeviceBus** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ DeviceBus** a ces propriétés.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données **: \_ bus Win32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) (« Antecedent »), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« \| bus Win32 WMI \_ »)
</dt> </dl>

[**\_ Bus Win32**](win32-bus.md) qui décrit les propriétés du bus système utilisé par l’appareil logique.

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données **: \_ LogicalDevice CIM**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) (« dépendant »), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« CIM \| CIM \_ LogicalDevice »)
</dt> </dl>

[**\_ LogicalDevice CIM**](cim-logicaldevice.md) qui décrit les propriétés de l’appareil logique qui utilise le bus système.

</dd> </dl>

## <a name="remarks"></a>Notes

La classe **Win32 \_ DeviceBus** est dérivée de la [**\_ dépendance CIM**](cim-dependency.md).

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

 

