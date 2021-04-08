---
description: Représente la valeur d’instance d’une mesure définie par une instance de la \_ classe MSVM AggregationMetricDefinition.
ms.assetid: 6dfcb711-6137-492a-aff4-82facbd11949
title: Classe Msvm_AggregationMetricValue
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AggregationMetricValue
- Msvm_AggregationMetricValue.InstanceID
- Msvm_AggregationMetricValue.Caption
- Msvm_AggregationMetricValue.Description
- Msvm_AggregationMetricValue.ElementName
- Msvm_AggregationMetricValue.MetricDefinitionId
- Msvm_AggregationMetricValue.MeasuredElementName
- Msvm_AggregationMetricValue.TimeStamp
- Msvm_AggregationMetricValue.Duration
- Msvm_AggregationMetricValue.MetricValue
- Msvm_AggregationMetricValue.BreakdownDimension
- Msvm_AggregationMetricValue.BreakdownValue
- Msvm_AggregationMetricValue.Volatile
- Msvm_AggregationMetricValue.AggregationTimeStamp
- Msvm_AggregationMetricValue.AggregationDuration
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f6842e5a23fbbf7cf1d639862cf5b9737bc1ff96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034961"
---
# <a name="msvm_aggregationmetricvalue-class"></a>MSVM \_ AggregationMetricValue, classe

Représente la valeur d’instance d’une mesure définie par une instance de la classe [**MSVM \_ AggregationMetricDefinition**](msvm-aggregationmetricdefinition.md) . Les propriétés héritées de [**MSVM \_ BaseMetricValue**](msvm-basemetricvalue.md) fournissent la valeur de métrique réelle. Les propriétés définies par cette classe fournissent des informations sur l’intervalle auquel la fonction d’agrégation a été appliquée.

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AggregationMetricValue : CIM_AggregationMetricValue
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  string   MetricDefinitionId;
  string   MeasuredElementName;
  datetime TimeStamp;
  datetime Duration;
  string   MetricValue;
  string   BreakdownDimension;
  string   BreakdownValue;
  boolean  Volatile;
  datetime AggregationTimeStamp;
  datetime AggregationDuration;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ AggregationMetricValue** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ AggregationMetricValue** possède les propriétés suivantes.

<dl> <dt>

**AggregationDuration**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Représente la durée pendant laquelle l’agrégation a été calculée. Le début d’un intervalle d’analyse sur lequel la fonction d’agrégation est appliquée est déterminé par la soustraction des **AggregationDuration** du **AggregationTimeStamp**. Cette propriété est héritée de la **\_ AggregationMetricValue CIM**.

</dd> <dt>

**AggregationTimeStamp**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Identifie l’heure à laquelle la fonction d’agrégation a été appliquée pour déterminer la valeur de l’instance de métrique. Ce n’est pas le même que l’heure de création de l’instance. Pour une instance **\_ AggregationMetricValue CIM** donnée, **AggregationTimeStamp** change chaque fois que la fonction d’agrégation est appliquée pour calculer la valeur. Cette propriété est héritée de la **\_ AggregationMetricValue CIM**.

</dd> <dt>

**BreakdownDimension**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie une dimension de répartition à partir du tableau **BreakdownDimensions** défini dans le [**\_ BaseMetricDefinition MSVM**](msvm-basemetricdefinition.md)associé. Il s’agit de la dimension selon laquelle cet ensemble de valeurs de métriques est divisé. Cette propriété est héritée de la [**\_ BaseMetricDefinition CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**BreakdownValue**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Définit une valeur de la propriété **BreakdownDimension** définie pour cette instance de la valeur métrique. Par exemple, si **BreakdownDimension** est « TransactionName », cette propriété peut nommer la transaction réelle à laquelle s’applique cette valeur de mesure particulière. Cette propriété est héritée de la [**\_ BaseMetricDefinition CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Brève description de l’objet. Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Description de l'objet . Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**Durée**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie la durée pendant laquelle cette valeur métrique est valide. Cette propriété ne doit pas exister pour les horodatages qui s’appliquent uniquement à un point dans le temps, mais doivent être spécifiées pour les valeurs considérées comme valides pour une certaine période (par exemple, échantillonnage). Si la propriété **Duration** existe et que n’a pas la **valeur null**, la propriété **timestamp** spécifie la fin de l’intervalle. Cette propriété est héritée de la [**\_ BaseMetricDefinition CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom complet de l’objet. Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **clé**
</dt> </dl>

Chaîne qui identifie de façon unique une instance de cette classe. Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**MeasuredElementName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom descriptif de l’élément auquel la valeur de la métrique appartient (l’élément mesuré). Cette propriété est héritée de la [**\_ BaseMetricDefinition CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**MetricDefinitionId**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Clé de l’instance [**MSVM \_ BaseMetricDefinition**](msvm-basemetricdefinition.md) pour cette valeur. Cette propriété est héritée de la [**\_ BaseMetricDefinition CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**MetricValue**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Valeur de la métrique représentée sous forme de chaîne. Cette propriété est héritée de la [**\_ BaseMetricDefinition CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**Confirmé**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie l’heure à laquelle la valeur de mesure a été capturée ou calculée. Sachez que cela diffère de l’heure de création de l’instance. Cette propriété est héritée de la [**\_ BaseMetricDefinition CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**Volatile**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

**True** si la valeur du point suivant dans le temps utilise la même instance de classe et modifie simplement les valeurs de propriété (telles que la **valeur** ou l' **horodateur**). Si la **valeur est true**, l’instance est réutilisée. Si la **valeur est false**, les instances existantes restent inchangées et une nouvelle instance est créée pour le nouveau point dans le temps. Cette propriété est héritée de la [**\_ BaseMetricDefinition CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

