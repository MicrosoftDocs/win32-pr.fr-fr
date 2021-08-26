---
description: La \_ classe WMI de l’Association OperatingSystemQFE Win32 associe un système d’exploitation et les mises à jour du produit appliquées comme représenté dans Win32 \_ QuickFixEngineering.
ms.assetid: 71985759-7e45-44df-82a9-f9a93e3b923e
ms.tgt_platform: multiple
title: Classe Win32_OperatingSystemQFE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystemQFE
- Win32_OperatingSystemQFE.Antecedent
- Win32_OperatingSystemQFE.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 60fa11faaf7b6d85ce7d3494e1081afc4742b65e27f11fc2cebcd94949373745
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119972349"
---
# <a name="win32_operatingsystemqfe-class"></a>\_Classe OperatingSystemQFE Win32

La [classe WMI](../wmisdk/retrieving-a-class.md) de l’Association **\_ OperatingSystemQFE Win32** associe un système d’exploitation et les mises à jour du produit appliquées comme représenté dans [**Win32 \_ QuickFixEngineering**](win32-quickfixengineering.md).

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{2CB2C452-C516-11D2-B364-00105A1F77A1}"), AMENDMENT]
class Win32_OperatingSystemQFE : CIM_Dependency
{
  Win32_OperatingSystem     REF Antecedent;
  Win32_QuickFixEngineering REF Dependent;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ OperatingSystemQFE** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ OperatingSystemQFE** a ces propriétés.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données : **Win32 \_ OperatingSystem**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ OperatingSystem")
</dt> </dl>

Référence à l’instance représentant le système affecté par la mise à jour du produit dans cette association.

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données : **Win32 \_ QuickFixEngineering**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**faible**](../wmisdk/standard-qualifiers.md), [**remplacement**](../wmisdk/standard-qualifiers.md) (« dépendant »), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI \| Win32 \_ QuickFixEngineering »)
</dt> </dl>

Référence à l’instance de qui représente l’instance d’objet appliquée au système d’exploitation dans cette association.

</dd> </dl>

## <a name="remarks"></a>Remarques

La classe **Win32 \_ OperatingSystemQFE** est dérivée de la [**\_ dépendance CIM**](cim-dependency.md).

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

[**\_Dépendance CIM**](cim-dependency.md)
</dt> <dt>

[Classes du système d’exploitation](./operating-system-classes.md)
</dt> </dl>

 

 
