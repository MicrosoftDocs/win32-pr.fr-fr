---
description: La \_ classe WMI de l’Association Win32 PnPAllocatedResource représente une association entre les unités logiques et les ressources système.
ms.assetid: e3cef457-cf88-4df5-8db8-b0495f636904
ms.tgt_platform: multiple
title: Classe Win32_PnPAllocatedResource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPAllocatedResource
- Win32_PnPAllocatedResource.Antecedent
- Win32_PnPAllocatedResource.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 492bd510965499393b399e8e02c1b901fc33f9abc00acf191899c5bb6b8b6d71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118008943"
---
# <a name="win32_pnpallocatedresource-class"></a>\_Classe PnPAllocatedResource Win32

La [classe WMI](../wmisdk/retrieving-a-class.md) de l’Association **Win32 \_ PnPAllocatedResource** représente une association entre les unités logiques et les ressources système. Cette classe est utilisée pour découvrir les ressources qui sont utilisées par un périphérique spécifique, par exemple une demande d’interruption (IRQ) ou un canal d’accès direct à la mémoire (DMA).

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("970C0998-41FE-4275-B7D9-7DABAD3FBC4D"), AMENDMENT]
class Win32_PnPAllocatedResource : CIM_AllocatedResource
{
  CIM_SystemResource REF Antecedent;
  Win32_PnPEntity    REF Dependent;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ PnPAllocatedResource** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ PnPAllocatedResource** a ces propriétés.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données : **CIM \_ SystemResource**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ SystemResource")
</dt> </dl>

Référence à l' [**instance \_ SystemResource CIM**](cim-systemresource.md) qui représente les propriétés d’une ressource système disponible pour l’unité logique. Cette propriété est héritée de la [**\_ dépendance CIM**](cim-dependency.md).

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données : **Win32 \_ PnPEntity**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**remplacement**](../wmisdk/standard-qualifiers.md) (« dépendant »), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« CIM \| CIM \_ LogicalDevice »)
</dt> </dl>

Référence à l’instance [**Win32 \_ PnPEntity**](win32-pnpentity.md) qui représente les propriétés de l’unité logique à l’aide des ressources système qui lui sont affectées. Cette propriété est héritée de la [**\_ dépendance CIM**](cim-dependency.md).

</dd> </dl>

## <a name="remarks"></a>Remarques

La classe **Win32 \_ PnPAllocatedResource** est dérivée de [**CIM \_ AllocatedResource**](cim-allocatedresource.md).

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

[**\_ALLOCATEDRESOURCE CIM**](cim-allocatedresource.md)
</dt> <dt>

[Classes matérielles du système informatique](computer-system-hardware-classes.md)
</dt> </dl>

 

 
