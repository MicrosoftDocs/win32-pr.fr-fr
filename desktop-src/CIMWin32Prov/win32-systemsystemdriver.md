---
description: La \_ classe WMI de l’Association SystemSystemDriver Win32 associe un système informatique et un pilote système s’exécutant sur ce système informatique.
ms.assetid: 82638c29-6769-4410-90bc-b408b27adad4
ms.tgt_platform: multiple
title: Classe Win32_SystemSystemDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemSystemDriver
- Win32_SystemSystemDriver.GroupComponent
- Win32_SystemSystemDriver.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b193d173fa0592a44ba437543659dec456e432ea
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999416"
---
# <a name="win32_systemsystemdriver-class"></a>\_Classe SystemSystemDriver Win32

La [classe WMI](../wmisdk/retrieving-a-class.md) de l’Association **\_ SystemSystemDriver Win32** associe un système informatique et un pilote système s’exécutant sur ce système informatique.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F1-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemSystemDriver : CIM_SystemComponent
{
  Win32_ComputerSystem REF GroupComponent;
  Win32_SystemDriver   REF PartComponent;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ SystemSystemDriver** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ SystemSystemDriver** a ces propriétés.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Type de données : **Win32 \_ ComputerSystem**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**substitution**](../wmisdk/standard-qualifiers.md) (« GroupComponent »), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI \| Win32 \_ ComputerSystem »)
</dt> </dl>

Référence à l’instance de qui représente les propriétés du système informatique sur lequel le pilote s’exécute.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Type de données : **Win32 \_ SystemDriver**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**remplacement**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ SystemDriver")
</dt> </dl>

Référence à l’instance de qui représente le pilote système en cours d’exécution sur le système informatique.

</dd> </dl>

## <a name="remarks"></a>Notes

La classe **Win32 \_ SystemSystemDriver** est dérivée de [**CIM \_ SystemComponent**](cim-systemcomponent.md).

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

[**\_SYSTEMCOMPONENT CIM**](cim-systemcomponent.md)
</dt> <dt>

[Classes du système d’exploitation](./operating-system-classes.md)
</dt> </dl>

 

 
