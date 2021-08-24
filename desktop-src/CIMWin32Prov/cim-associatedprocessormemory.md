---
description: La \_ classe CIM AssociatedProcessorMemory associe le processeur et la mémoire système, ou le cache d’un processeur.
ms.assetid: a4c28a0a-e4cc-4db2-bd77-b7b5023eace6
ms.tgt_platform: multiple
title: Classe CIM_AssociatedProcessorMemory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedProcessorMemory
- CIM_AssociatedProcessorMemory.Antecedent
- CIM_AssociatedProcessorMemory.Dependent
- CIM_AssociatedProcessorMemory.BusSpeed
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 23b2ee879752365e3100866a4ea82a33b01a2236f4f3266539e79b3ee37b94e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119701159"
---
# <a name="cim_associatedprocessormemory-class"></a>\_Classe CIM AssociatedProcessorMemory

La classe **CIM \_ AssociatedProcessorMemory** associe le processeur et la mémoire système, ou le cache d’un processeur.

> [!IMPORTANT]
> Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées. WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[abstract, UUID("{464FFAB1-946F-11d2-AAE2-006008C78BC7}"), AMENDMENT]
class CIM_AssociatedProcessorMemory : CIM_AssociatedMemory
{
  CIM_Memory    REF Antecedent;
  CIM_Processor REF Dependent;
  uint32            BusSpeed;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ AssociatedProcessorMemory** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ AssociatedProcessorMemory** possède les propriétés suivantes.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données **: \_ mémoire CIM**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

[**\_ Mémoire CIM**](cim-memory.md) qui décrit la mémoire installée sur un appareil ou associée à celui-ci.

Cette propriété est héritée de la [**\_ AssociatedMemory CIM**](cim-associatedmemory.md).

</dd> <dt>

**BusSpeed**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« mégahertz »)
</dt> </dl>

Vitesse du bus, en mégahertz (MHz), entre le processeur et la mémoire.

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données **: \_ processeur CIM**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)
</dt> </dl>

[**\_ Processeur CIM**](cim-processor.md) décrivant le processeur qui accède à la mémoire ou utilise le cache.

</dd> </dl>

## <a name="remarks"></a>Remarques

La classe **CIM \_ AssociatedProcessorMemory** est dérivée de [**CIM \_ AssociatedMemory**](cim-associatedmemory.md).

WMI n’implémente pas cette classe. Pour plus d’informations sur les classes dérivées de **CIM \_ AssociatedProcessorMemory**, consultez [classes Win32](win32-provider.md).

Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF. Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.

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

[**\_ASSOCIATEDMEMORY CIM**](cim-associatedmemory.md)
</dt> </dl>

 

