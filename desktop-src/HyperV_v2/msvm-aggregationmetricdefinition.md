---
description: Représente les aspects de définition d’une mesure dérivée d’une autre valeur de mesure.
ms.assetid: 642f53fe-e51c-4c73-babf-19adb2cf55f4
title: Classe Msvm_AggregationMetricDefinition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AggregationMetricDefinition
- Msvm_AggregationMetricDefinition.InstanceID
- Msvm_AggregationMetricDefinition.Caption
- Msvm_AggregationMetricDefinition.Description
- Msvm_AggregationMetricDefinition.ElementName
- Msvm_AggregationMetricDefinition.Id
- Msvm_AggregationMetricDefinition.Name
- Msvm_AggregationMetricDefinition.DataType
- Msvm_AggregationMetricDefinition.Calculable
- Msvm_AggregationMetricDefinition.Units
- Msvm_AggregationMetricDefinition.BreakdownDimensions
- Msvm_AggregationMetricDefinition.IsContinuous
- Msvm_AggregationMetricDefinition.ChangeType
- Msvm_AggregationMetricDefinition.TimeScope
- Msvm_AggregationMetricDefinition.GatheringType
- Msvm_AggregationMetricDefinition.ProgrammaticUnits
- Msvm_AggregationMetricDefinition.SimpleFunction
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: da52c154c90b58fc147a52268025887d2dfa8f10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204021"
---
# <a name="msvm_aggregationmetricdefinition-class"></a>MSVM \_ AggregationMetricDefinition, classe

Représente les aspects de définition d’une mesure dérivée d’une autre valeur de mesure. L’objet **MSVM \_ AggregationMetricDefinition** doit être associé aux éléments managés auxquels il s’applique.

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AggregationMetricDefinition : CIM_AggregationMetricDefinition
{
  string  InstanceID;
  string  Caption;
  string  Description;
  string  ElementName;
  string  Id;
  string  Name;
  uint16  DataType;
  uint16  Calculable;
  string  Units;
  string  BreakdownDimensions[];
  boolean IsContinuous;
  uint16  ChangeType;
  uint16  TimeScope;
  uint16  GatheringType;
  string  ProgrammaticUnits;
  uint16  SimpleFunction;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ AggregationMetricDefinition** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ AggregationMetricDefinition** possède les propriétés suivantes.

<dl> <dt>

**BreakdownDimensions**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Définit une ou plusieurs chaînes qui peuvent être utilisées pour affiner (décomposer) des requêtes sur les valeurs de métrique le long d’une certaine dimension. Par exemple, un nom de transaction, qui permet de décomposer la valeur totale de toutes les transactions en un ensemble de valeurs, une pour chaque nom de transaction. Il peut s’agir, par exemple, d’un nom de système d’application ou de groupe d’utilisateurs. Les chaînes sont au format libre et doivent être significatives pour les utilisateurs finaux des données de métriques. Les chaînes indiquent les dimensions de rupture prises en charge pour cette définition de métrique par l’instrumentation sous-jacente. Cette propriété est héritée de la **\_ BaseMetricDefinition CIM**.

</dd> <dt>

**Calculable**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Décrit les caractéristiques de la mesure dans le cadre de l’exécution de calculs. Cette propriété est héritée de la **\_ BaseMetricDefinition CIM**. Il peut s’agir de la **valeur null** ou de l’une des valeurs suivantes.



| Valeur                                                                                                                                                                                                                                                   | Signification                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Non-calculable"></span><span id="non-calculable"></span><span id="NON-CALCULABLE"></span><dl> <dt>**Non calculable**</dt> <dt>1</dt> </dl> | La valeur ne peut pas être calculée. Par exemple, une chaîne.<br/>                                                                                                                                                                                                                                                                                                         |
| <span id="Summable"></span><span id="summable"></span><span id="SUMMABLE"></span><dl> <dt>**Summable**</dt> <dt>2</dt> </dl>                         | La valeur peut être additionnée sur de nombreuses instances. Par exemple, si chaque travail de sauvegarde est une unité de travail et que chaque travail sauvegarde 27 000 fichiers en moyenne, 100 travaux de sauvegarde ont traité 2,7 millions fichiers.<br/>                                                                                                                                                                 |
| <span id="Non-summable_"></span><span id="non-summable_"></span><span id="NON-SUMMABLE_"></span><dl> <dt> **Non-summable**</dt> <dt>3</dt> </dl>    | Cette valeur ne peut pas être additionnée sur de nombreuses instances. C’est le cas, par exemple, d’une mesure qui mesure la longueur de la file d’attente lorsqu’un travail arrive sur un serveur. Si chaque travail est une unité de travail et que la longueur moyenne de la file d’attente lorsque chaque travail arrive est 33, il n’est pas judicieux de préciser que la longueur de la file d’attente pour les travaux 100 est 3300. Il est logique de dire que la moyenne est de 33.<br/> |



 

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Brève description de l’objet. Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**ChangeType**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique comment la valeur de la métrique change, sous la forme de combinaisons typiques d’attributs de grain plus fins tels que le changement de direction, les valeurs minimales et maximales et la sémantique d’encapsulation. Cette propriété est héritée de la **\_ BaseMetricDefinition CIM**.



| Valeur                                                                                                                                                                                                                                                                       | Signification                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Inconnu**</dt> <dt>0</dt> </dl>                                                 | Le concepteur de mesures n’a pas qualifié le **ChangeType**.<br/>                                                                                                                               |
| <span id="N_A"></span><span id="n_a"></span><dl> <dt>**N/A**</dt> <dt>2</dt> </dl>                                                                                       | Si la propriété **IsContinuous** est définie sur « false », **ChangeType** n’a pas de sens et doit avoir la valeur « N/A ».<br/>                                                                             |
| <span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span><dl> <dt>**Compteur**</dt> <dt>3</dt> </dl>                                                 | La métrique est une mesure de compteur. Ils ont des valeurs entières non négatives qui augmentent jusqu’à atteindre le nombre maximal pouvant être représenté, puis encapsulent et commencent à augmenter de 0.<br/> |
| <span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span><dl> <dt>**Jauge**</dt> <dt>4</dt> </dl>                                                         | La métrique est une mesure de jauge. Celles-ci ont des valeurs entières ou float qui peuvent augmenter et diminuer de façon arbitraire.<br/>                                                                          |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <dt>**DMTF réservé**</dt> <dt>5.. 32767</dt> </dl>                  |                                                                                                                                                                                                  |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <dt> **Fournisseur réservé**</dt> <dt>32768.. 65535</dt> </dl> | Les fournisseurs peuvent étendre la propriété **ChangeType** dans la plage réservée du fournisseur.<br/>                                                                                                          |



 

</dd> <dt>

**DataType**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Type de données de la mesure. Cette propriété est héritée de la **\_ BaseMetricDefinition CIM**.

<dl> <dt>

<span id="boolean"></span><span id="BOOLEAN"></span>**booléen** (1)
</dt> <dt>

<span id="char16"></span><span id="CHAR16"></span>**char16** (2)
</dt> <dt>

<span id="datetime"></span><span id="DATETIME"></span>**DateTime** (3)
</dt> <dt>

<span id="real32"></span><span id="REAL32"></span>**real32** (4)
</dt> <dt>

<span id="real64"></span><span id="REAL64"></span>**real64** (5)
</dt> <dt>

<span id="sint16"></span><span id="SINT16"></span>**sint16** (6)
</dt> <dt>

<span id="sint32"></span><span id="SINT32"></span>**sint32** (7)
</dt> <dt>

<span id="sint64"></span><span id="SINT64"></span>**sint64** (8)
</dt> <dt>

<span id="sint8"></span><span id="SINT8"></span>**sint8** (9)
</dt> <dt>

<span id="string"></span><span id="STRING"></span>**chaîne** (10)
</dt> <dt>

<span id="uint16"></span><span id="UINT16"></span>**UInt16** (11)
</dt> <dt>

<span id="uint32"></span><span id="UINT32"></span>**UInt32** (12)
</dt> <dt>

<span id="uint64"></span><span id="UINT64"></span>**UInt64** (13)
</dt> <dt>

<span id="uint8_"></span><span id="UINT8_"></span>**UInt8** (14)
</dt> </dl>

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Description de l'objet . Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom complet de l’objet. Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**GatheringType**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique comment les valeurs de métriques sont collectées par l’instrumentation sous-jacente. Cela permet à l’application cliente de choisir la mesure appropriée à cet effet. Cette propriété est héritée de la **\_ BaseMetricDefinition CIM**. Il peut s’agir de la **valeur null** ou de l’une des valeurs suivantes.



| Valeur                                                                                                                                                                                                                                                                       | Signification                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Inconnu**</dt> <dt>0</dt> </dl>                                                 | Le type de regroupement n’est pas connu.<br/>                                                                                                                                                                                                                               |
| <span id="OnChange"></span><span id="onchange"></span><span id="ONCHANGE"></span><dl> <dt>**OnChange**</dt> <dt>2</dt> </dl>                                             | Les valeurs de métriques sont mises à jour immédiatement lorsque les valeurs à l’intérieur de la ressource mesurée changent.<br/>                                                                                                                                                              |
| <span id="Periodic"></span><span id="periodic"></span><span id="PERIODIC"></span><dl> <dt>**Périodique**</dt> <dt>3</dt> </dl>                                             | Les valeurs de mesure sont mises à jour régulièrement. Par exemple, pour une application cliente, une valeur métrique qui s’applique à l’heure actuelle apparaîtra constante pendant chaque intervalle de collecte, puis passera à la nouvelle valeur à la fin de chaque intervalle de collecte.<br/> |
| <span id="OnRequest"></span><span id="onrequest"></span><span id="ONREQUEST"></span><dl> <dt>**OnRequest**</dt> <dt>4</dt> </dl>                                         | La valeur de la métrique est déterminée chaque fois qu’une application cliente la lit.<br/>                                                                                                                                                                                        |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <dt>**DMTF réservé**</dt> <dt>5.. 32767</dt> </dl>                  |                                                                                                                                                                                                                                                                           |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <dt> **Fournisseur réservé**</dt> <dt>32768.. 65535</dt> </dl> |                                                                                                                                                                                                                                                                           |



 

</dd> <dt>

**Id**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **clé**
</dt> </dl>

Chaîne qui identifie de façon unique la définition de la métrique. Cette propriété est héritée de la **\_ BaseMetricDefinition CIM**.

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

**IsContinuous**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la valeur de la métrique est continue ou scalaire. Les mesures de performances sont un exemple de mesure continue. Les codes d’erreur ou les États opérationnels sont des exemples de métriques scalaires. Les métriques continues peuvent être comparées à l’aide de la relation « supérieur à ». Cette propriété est héritée de la **\_ BaseMetricDefinition CIM**.

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom de la mesure. Cette propriété est héritée de la **\_ BaseMetricDefinition CIM**.

</dd> <dt>

**ProgrammaticUnits**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Identifie les unités spécifiques d’une valeur. La valeur de cette propriété est une valeur légale du qualificateur d’unités de programmation, tel que défini dans l’annexe C. 1 de [DSP0004 v 2.4](https://www.dmtf.org/sites/default/files/standards/documents/DSP0004_2.5.0.pdf) ou version ultérieure. Cette propriété est héritée de la **\_ BaseMetricDefinition CIM**.

</dd> <dt>

**SimpleFunction**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Identifie le calcul de base effectué sur une mesure sous-jacente pour arriver à la valeur de cette mesure dérivée. Cette propriété est héritée de **CIM \_ AggregationMetricDefinition** et sera l’une des valeurs suivantes.

<dl> <dt>

<span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>**Minimum** (2)
</dt> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Maximum** (3)
</dt> <dt>

<span id="Average"></span><span id="average"></span><span id="AVERAGE"></span>**Moyenne** (4)
</dt> <dt>

<span id="Median"></span><span id="median"></span><span id="MEDIAN"></span>**Médiane** (5)
</dt> <dt>

<span id="Mode"></span><span id="mode"></span><span id="MODE"></span>**Mode** (6)
</dt> </dl>

</dd> <dt>

**TimeScope**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique l’étendue de temps à laquelle la valeur de mesure s’applique. Cette propriété est héritée de la **\_ BaseMetricDefinition CIM**.



| Valeur                                                                                                                                                                                                                                                                       | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Inconnu**</dt> <dt>0</dt> </dl>                                                 | La portée de l’heure n’a pas été qualifiée par le concepteur de mesures ou est inconnue du fournisseur.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Point"></span><span id="point"></span><span id="POINT"></span><dl> <dt>**Point**</dt> <dt>2</dt> </dl>                                                         | La mesure s’applique à un point dans le temps. Sur les instances [**MSVM \_ BaseMetricValue**](msvm-basemetricvalue.md) correspondantes, la propriété **timestamp** spécifie le point dans le temps, et la propriété **Duration** est toujours égale à 0.<br/>                                                                                                                                                                                                                                                                                              |
| <span id="Interval"></span><span id="interval"></span><span id="INTERVAL"></span><dl> <dt>**Intervalle**</dt> <dt>3</dt> </dl>                                             | La mesure s’applique à un intervalle de temps. Sur les instances [**MSVM \_ BaseMetricValue**](msvm-basemetricvalue.md) correspondantes, la propriété **timestamp** spécifie la fin de l’intervalle de temps et la propriété **Duration** spécifie sa durée.<br/>                                                                                                                                                                                                                                                                        |
| <span id="StartupInterval"></span><span id="startupinterval"></span><span id="STARTUPINTERVAL"></span><dl> <dt>**StartupInterval**</dt> <dt>4</dt> </dl>                 | La mesure s’applique à un intervalle de temps qui a commencé au démarrage de la ressource mesurée (autrement dit, le propriété ManagedElement associé à MetricDefForMe). Sur les instances [**MSVM \_ BaseMetricValue**](msvm-basemetricvalue.md) correspondantes, la propriété **timestamp** spécifie la fin de l’intervalle de temps. Si la propriété **Duration** est égale à 0, cela indique que le temps de démarrage de la ressource mesurée est inconnu. Dans le cas contraire, **Duration** spécifie la durée entre le démarrage de la ressource et l' **horodateur**.<br/> |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <dt>**DMTF réservé**</dt> <dt>5.. 32767</dt> </dl>                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <dt> **Fournisseur réservé**</dt> <dt>32768.. 65535</dt> </dl> |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

</dd> <dt>

**Unités**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Identifie les unités d’une valeur, par exemple, « mégaoctets ». Cette propriété est héritée de la **\_ BaseMetricDefinition CIM**.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

