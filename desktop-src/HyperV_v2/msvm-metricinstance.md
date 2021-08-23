---
description: Représente une association d’objets de valeur de métrique à leurs définitions de métriques.
ms.assetid: 98ad9390-78b4-4c18-b068-d05efa2f1866
title: Classe Msvm_MetricInstance
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricInstance
- Msvm_MetricInstance.Antecedent
- Msvm_MetricInstance.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 18a15ff6479caa690a8645e89d9b68f4a15f523bd7cee56fedb6957e20373214
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119521539"
---
# <a name="msvm_metricinstance-class"></a>MSVM \_ MetricInstance, classe

Représente une association d’objets de valeur de métrique à leurs définitions de métriques. Cette association lie une instance de [**MSVM \_ BaseMetricValue**](msvm-basemetricvalue.md) à son [**\_ BaseMetricDefinition MSVM**](msvm-basemetricdefinition.md).

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricInstance : CIM_MetricInstance
{
  CIM_ManagedElement REF Antecedent;
  CIM_ManagedElement REF Dependent;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ MetricInstance** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ MetricInstance** possède les propriétés suivantes.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données : * * * * CIM \_ propriété ManagedElement * * * *
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **clé**
</dt> </dl>

Référence à une instance de la classe [**MSVM \_ BaseMetricDefinition**](msvm-basemetricdefinition.md) qui représente les définitions de métriques.

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données : * * * * CIM \_ propriété ManagedElement * * * *
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **clé**
</dt> </dl>

Référence à une instance de la classe [**MSVM \_ BaseMetricValue**](msvm-basemetricvalue.md) qui représente les métriques qui dépendent de l' **antécédent**.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

 




