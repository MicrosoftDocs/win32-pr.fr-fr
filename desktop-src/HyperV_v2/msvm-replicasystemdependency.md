---
description: Représente une association entre une instance de la classe CIM CIM \_ qui représente le réplica d’ordinateur virtuel et une instance de la \_ classe ComputerSystem CIM qui représente le réplica de machine virtuelle de test.
ms.assetid: c3216ddd-7f70-4287-9f7e-1fd7a60b1a0a
title: Classe Msvm_ReplicaSystemDependency
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicaSystemDependency
- Msvm_ReplicaSystemDependency.Antecedent
- Msvm_ReplicaSystemDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7f6bb3f4879ee0e1c7babaf8f85b8455716ee1b2e61db4e0764d6b28583efefd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130429"
---
# <a name="msvm_replicasystemdependency-class"></a>MSVM \_ ReplicaSystemDependency, classe

Représente une association entre une instance de la [**classe \_ CIM CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) qui représente le réplica d’ordinateur virtuel et une instance de la classe **\_ ComputerSystem CIM** qui représente le réplica de machine virtuelle de test.

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicaSystemDependency : CIM_Dependency
{
  CIM_ComputerSystem REF Antecedent;
  CIM_ComputerSystem REF Dependent;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ ReplicaSystemDependency** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ ReplicaSystemDependency** possède les propriétés suivantes.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données **: \_ CIM CIM**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ dependency. Antecedent")
</dt> </dl>

Référence à une instance de la classe [**CIM \_ CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) qui représente le réplica de machine virtuelle. Cette propriété est héritée de la [**\_ dépendance CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données **: \_ CIM CIM**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dépendance CIM \_ . dependent")
</dt> </dl>

Référence à une instance de la classe [**CIM \_ CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) qui représente le réplica de machine virtuelle de test créé par la méthode [**MSVM \_ ReplicationService. TestReplicaSystem**](testreplicasystem-msvm-replicationservice.md) . Cette propriété est héritée de la [**\_ dépendance CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

