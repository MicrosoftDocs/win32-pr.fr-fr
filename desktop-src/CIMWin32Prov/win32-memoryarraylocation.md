---
description: La \_ classe WMI de l’Association MemoryArrayLocation Win32 associe un tableau de mémoire logique et le tableau de mémoire physique sur lequel il existe.
ms.assetid: 455daeee-ad67-4599-84d6-fa3f4ac593aa
ms.tgt_platform: multiple
title: Classe Win32_MemoryArrayLocation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_MemoryArrayLocation
- Win32_MemoryArrayLocation.Dependent
- Win32_MemoryArrayLocation.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a0fd01751794dc9177f3840804f0412db70531f6706a452793fe6cbcf3aa2389
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119079797"
---
# <a name="win32_memoryarraylocation-class"></a>\_Classe MemoryArrayLocation Win32

La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de l’Association **\_ MemoryArrayLocation Win32** associe un tableau de mémoire logique et le tableau de mémoire physique sur lequel il existe.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{B24EF561-BBBE-11d2-ABFB-00805F538618}"), AMENDMENT]
class Win32_MemoryArrayLocation : CIM_Realizes
{
  Win32_MemoryArray         REF Dependent;
  Win32_PhysicalMemoryArray REF Antecedent;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ MemoryArrayLocation** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ MemoryArrayLocation** a ces propriétés.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données : **Win32 \_ PhysicalMemoryArray**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ PhysicalMemoryArray")
</dt> </dl>

[**\_ PhysicalMemoryArray Win32**](win32-physicalmemoryarray.md) qui décrit le tableau de mémoire physique qui implémente le tableau de mémoire logique.

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données : **Win32 \_ MemoryArray**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) (« dépendant »), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« WMI \| Win32 \_ MemoryArray »)
</dt> </dl>

[**\_ MemoryArray Win32**](win32-memoryarray.md) qui décrit le tableau de mémoire logique implémenté par le tableau de mémoire physique.

</dd> </dl>

## <a name="remarks"></a>Remarques

La classe **Win32 \_ MemoryArrayLocation** est dérivée de l' [**\_ esprit CIM**](cim-realizes.md).

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

[**CIM \_**](cim-realizes.md)
</dt> <dt>

[Classes matérielles du système informatique](computer-system-hardware-classes.md)
</dt> </dl>

 

