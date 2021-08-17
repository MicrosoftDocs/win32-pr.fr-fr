---
description: Représente une association entre une instance de MSVM \_ ComputerSystem qui représente l’ordinateur virtuel et une instance de MSVM \_ ReplicationRelationship qui représente une relation de réplication de l’ordinateur virtuel.
ms.assetid: 23E7BF91-9527-434C-A571-05879E83950E
title: Classe Msvm_SystemReplicationRelationship
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemReplicationRelationship
- Msvm_SystemReplicationRelationship.Antecedent
- Msvm_SystemReplicationRelationship.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 86040e6dc5676f6cd40b223f0a3cbd31864965722de957fda6ff1d140ad94b18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117810603"
---
# <a name="msvm_systemreplicationrelationship-class"></a>MSVM \_ SystemReplicationRelationship, classe

Représente une association entre une instance de [**MSVM \_ ComputerSystem**](msvm-computersystem.md) qui représente l’ordinateur virtuel et une instance de [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) qui représente une relation de réplication de l’ordinateur virtuel. Cette classe dérive de la classe de [**\_ dépendance CIM**](/windows/desktop/CIMWin32Prov/cim-dependency) .

La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SystemReplicationRelationship : CIM_Dependency
{
  Msvm_ComputerSystem          REF Antecedent;
  Msvm_ReplicationRelationship REF Dependent;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ SystemReplicationRelationship** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ SystemReplicationRelationship** possède les propriétés suivantes.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données : **MSVM \_ ComputerSystem**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ dependency. Antecedent")
</dt> </dl>

Référence à l’instance de la classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) qui représente l’ordinateur virtuel.

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données : **MSVM \_ ReplicationRelationship**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dépendance CIM \_ . dependent")
</dt> </dl>

Référence à l’instance de la classe [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) qui représente la relation de réplication d’un système virtuel.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[Applications de bureau R2 uniquement\]<br/>                                                 |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Dépendance CIM**](cim-dependency.md)
</dt> <dt>

[**\_Dépendance CIM**](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> </dl>

 

