---
description: Représente une valeur de métrique définie par une instance de la \_ classe MSVM BaseMetricDefinition.
ms.assetid: bd872f21-ab71-4ab7-88d3-b26dd2fbdbe5
title: Classe Msvm_BaseMetricValue
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BaseMetricValue
- Msvm_BaseMetricValue.InstanceID
- Msvm_BaseMetricValue.Caption
- Msvm_BaseMetricValue.Description
- Msvm_BaseMetricValue.ElementName
- Msvm_BaseMetricValue.MetricDefinitionId
- Msvm_BaseMetricValue.MeasuredElementName
- Msvm_BaseMetricValue.TimeStamp
- Msvm_BaseMetricValue.Duration
- Msvm_BaseMetricValue.MetricValue
- Msvm_BaseMetricValue.BreakdownDimension
- Msvm_BaseMetricValue.BreakdownValue
- Msvm_BaseMetricValue.Volatile
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 24d61f6068cffc83f8556637bba30de57308b6a5bcefe5b015bc185ab7811108
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119790219"
---
# <a name="msvm_basemetricvalue-class"></a>MSVM \_ BaseMetricValue, classe

Représente une valeur de métrique définie par une instance de la classe [**MSVM \_ BaseMetricDefinition**](msvm-basemetricdefinition.md) .

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BaseMetricValue : CIM_BaseMetricValue
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
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ BaseMetricValue** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ BaseMetricValue** possède les propriétés suivantes.

<dl> <dt>

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
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

