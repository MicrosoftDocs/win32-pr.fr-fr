---
description: Représente la valeur d’instance d’une mesure définie par une instance de \_ AGGREGATIONMETRICDEFINITION CIM.
ms.assetid: 663ef18a-0238-416f-9682-8809b271b4fc
title: Classe CIM_AggregationMetricValue
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AggregationMetricValue
- CIM_AggregationMetricValue.AggregationTimeStamp
- CIM_AggregationMetricValue.AggregationDuration
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0af264b66838e7c039ef3f99a4f365ebab55c293
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519639"
---
# <a name="cim_aggregationmetricvalue-class"></a>\_Classe CIM AggregationMetricValue

Représente la valeur d’instance d’une mesure définie par une instance **de \_ AggregationMetricDefinition CIM**.

## <a name="syntax"></a>Syntaxe

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_AggregationMetricValue : CIM_BaseMetricValue
{
  datetime AggregationTimeStamp;
  datetime AggregationDuration;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ AggregationMetricValue** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ AggregationMetricValue** possède les propriétés suivantes.

<dl> <dt>

**AggregationDuration**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AggregationMetricValue**.**AggregationTimeStamp**")
</dt> </dl>

Représente la durée pendant laquelle l’agrégation a été calculée. Le début d’un intervalle de surveillance sur lequel la fonction d’agrégation est appliquée est déterminé par la soustraction de la valeur **AggregationDuration** de la valeur **AggregationTimestamp** .

</dd> <dt>

**AggregationTimeStamp**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AggregationMetricValue**.**Duration**»)
</dt> </dl>

Heure à laquelle la fonction d’agrégation a été appliquée pour déterminer la valeur de l’instance de métrique. Cela diffère de l’heure de création de l’instance. La valeur **AggregationTimeStamp** change chaque fois que la fonction d’agrégation est appliquée pour calculer la valeur.

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

[**\_BASEMETRICVALUE CIM**](cim-basemetricvalue.md)
</dt> </dl>

 

