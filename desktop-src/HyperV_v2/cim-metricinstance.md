---
description: Représente une association entre une instance d’une valeur de métrique et une définition de métrique.
ms.assetid: 4c620a7a-8b15-49ad-ae84-246e2fca175d
title: Classe CIM_MetricInstance
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricInstance
- CIM_MetricInstance.Antecedent
- CIM_MetricInstance.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3ff08757b8043e51d43079be6011b69731bdc761f22da27ff85272b95d4795c1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119695059"
---
# <a name="cim_metricinstance-class"></a>\_Classe CIM MetricInstance

Représente une association entre une instance d’une valeur de métrique et une définition de métrique.

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Abstract, Version("2.7.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_MetricInstance : CIM_Dependency
{
  CIM_BaseMetricDefinition REF Antecedent;
  CIM_BaseMetricValue      REF Dependent;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ MetricInstance** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ MetricInstance** possède les propriétés suivantes.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données : **CIM \_ BaseMetricDefinition**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Définition de la valeur de la métrique.

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données : **CIM \_ BaseMetricValue**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)
</dt> </dl>

Valeur de métrique associée à la définition de métrique.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8<br/>                                                                                    |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                                          |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Dépendance CIM**](cim-dependency.md)
</dt> </dl>

 

