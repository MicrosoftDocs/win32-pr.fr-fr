---
description: La \_ classe WMI d’association abstraite SystemSetting de Win32 associe un système informatique et un paramètre général sur ce système.
ms.assetid: 796ee263-2526-43f8-bd3d-23442b6bd4ca
ms.tgt_platform: multiple
title: Classe Win32_SystemSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemSetting
- Win32_SystemSetting.Element
- Win32_SystemSetting.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 75c4ee9db2f48d02151c3874cc0ac5775f04e2d119ada972db09826dd1f791c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827789"
---
# <a name="win32_systemsetting-class"></a>\_Classe SystemSetting Win32

La [classe WMI](../wmisdk/retrieving-a-class.md) d’association abstraite **\_ SystemSetting de Win32** associe un système informatique et un paramètre général sur ce système.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Abstract, UUID("{8502C501-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemSetting : CIM_ElementSetting
{
  Win32_ComputerSystem REF Element;
  CIM_Setting          REF Setting;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ SystemSetting** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ SystemSetting** a ces propriétés.

<dl> <dt>

**Element**
</dt> <dd> <dl> <dt>

Type de données : **Win32 \_ ComputerSystem**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")
</dt> </dl>

Référence à l’instance de qui représente les propriétés d’un système informatique sur lequel ce paramètre peut être appliqué.

</dd> <dt>

**Paramètre**
</dt> <dd> <dl> <dt>

Type de données **: \_ paramètre CIM**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**remplacement**](../wmisdk/standard-qualifiers.md) (« paramètre »), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« paramètre CIM \| CIM \_ »)
</dt> </dl>

Référence à l’instance de qui représente les propriétés du paramètre qui peut être appliqué au système informatique.

</dd> </dl>

## <a name="remarks"></a>Remarques

La classe **Win32 \_ SystemSetting** est dérivée de [**CIM \_ ElementSetting**](cim-elementsetting.md).

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

[**\_ELEMENTSETTING CIM**](cim-elementsetting.md)
</dt> <dt>

[Classes du système d’exploitation](./operating-system-classes.md)
</dt> </dl>

 

 
