---
description: Représente l’association entre deux définitions de métriques ou deux valeurs de métriques.
ms.assetid: 78fb926d-8981-443a-a82d-ebac34d38e13
title: Classe Msvm_MetricCollectionDependency
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricCollectionDependency
- Msvm_MetricCollectionDependency.Antecedent
- Msvm_MetricCollectionDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e79ae7dbdd98cc732868922b8679ae1cc6c610eccde1d0ae9dfb151f1e55022b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148332"
---
# <a name="msvm_metriccollectiondependency-class"></a>MSVM \_ MetricCollectionDependency, classe

Représente l’association entre deux définitions de métriques ou deux valeurs de métriques.

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricCollectionDependency : CIM_Dependency
{
  CIM_ManagedElement REF Antecedent;
  CIM_ManagedElement REF Dependent;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ MetricCollectionDependency** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ MetricCollectionDependency** possède les propriétés suivantes.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données : **[ **CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Référence à une instance de la classe [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) qui représente la définition de métrique indépendante ou la valeur métrique. Cette propriété est héritée de la [**\_ dépendance CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données : **[ **CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Référence à une instance de la classe [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) qui représente la définition de métrique ou la valeur de métrique qui est dépendante de l' **antécédent**. Cette propriété est héritée de la [**\_ dépendance CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

