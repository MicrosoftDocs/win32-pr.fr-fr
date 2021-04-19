---
description: Représente une définition de métrique qui contient les métadonnées d’un \_ objet CIM MetricInstance.
ms.assetid: 6abfb0dc-e80b-4ca6-89d9-2e43283d0abe
title: Classe CIM_BaseMetricDefinition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BaseMetricDefinition
- CIM_BaseMetricDefinition.Id
- CIM_BaseMetricDefinition.Name
- CIM_BaseMetricDefinition.DataType
- CIM_BaseMetricDefinition.Calculable
- CIM_BaseMetricDefinition.Units
- CIM_BaseMetricDefinition.BreakdownDimensions
- CIM_BaseMetricDefinition.IsContinuous
- CIM_BaseMetricDefinition.ChangeType
- CIM_BaseMetricDefinition.TimeScope
- CIM_BaseMetricDefinition.GatheringType
- CIM_BaseMetricDefinition.ProgrammaticUnits
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cac965ed1eae59f1c269d897a12e9aa116183eb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529484"
---
# <a name="cim_basemetricdefinition-class"></a>\_Classe CIM BaseMetricDefinition

Représente une définition de métrique qui contient les métadonnées d’un objet **CIM \_ MetricInstance** .

## <a name="syntax"></a>Syntaxe

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_BaseMetricDefinition : CIM_ManagedElement
{
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
};
```

## <a name="members"></a>Membres

La classe **CIM \_ BaseMetricDefinition** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ BaseMetricDefinition** possède les propriétés suivantes.

<dl> <dt>

**BreakdownDimensions**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Tableau qui contient des chaînes de format libre qui peuvent être utilisées pour décomposer des requêtes d’objets [**\_ BaseMetricValue CIM**](cim-basemetricvalue.md) le long d’une certaine dimension. Les chaînes doivent être significatives pour les utilisateurs finaux des données de métriques. En outre, les chaînes doivent indiquer les dimensions de rupture prises en charge pour la définition de métrique, par l’instrumentation sous-jacente.

Par exemple, un nom de transaction permet de décomposer la valeur totale de toutes les transactions en un ensemble de valeurs, une pour chaque nom de transaction. D’autres exemples sont un système d’applications ou un nom de groupe d’utilisateurs.

</dd> <dt>

**Calculable**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Caractéristiques de la mesure utilisée pour effectuer des calculs.

<dt>

<span id="Non-calculable"></span><span id="non-calculable"></span><span id="NON-CALCULABLE"></span>

<span id="Non-calculable"></span><span id="non-calculable"></span><span id="NON-CALCULABLE"></span>**Non-calculable** (1)


</dt> <dd>

Chaîne. L’arithmétique n’est pas appropriée.

</dd> <dt>

<span id="Summable"></span><span id="summable"></span><span id="SUMMABLE"></span>

<span id="Summable"></span><span id="summable"></span><span id="SUMMABLE"></span>**Summable** (2)


</dt> <dd>

Il est raisonnable de calculer cette valeur sur de nombreuses instances de, par exemple, UnitOfWork, telles que le nombre de fichiers traités dans un travail de sauvegarde. Par exemple, si chaque travail de sauvegarde est un UnitOfWork et que chaque travail sauvegarde 27 000 fichiers en moyenne, il est logique de préciser que 100 travaux de sauvegarde ont traité 2,7 millions fichiers.

</dd> <dt>

<span id="Non-summable"></span><span id="non-summable"></span><span id="NON-SUMMABLE"></span>

<span id="Non-summable"></span><span id="non-summable"></span><span id="NON-SUMMABLE"></span>**Non summable** (3)


</dt> <dd>

Il n’est pas judicieux de faire la somme de cette valeur sur de nombreuses instances de UnitOfWork. C’est le cas, par exemple, d’une mesure qui mesure la longueur de la file d’attente lorsqu’un travail arrive sur un serveur. Si chaque travail est un UnitOfWork et que la longueur moyenne de la file d’attente lorsque chaque travail arrive est 33, il n’est pas judicieux de préciser que la longueur de la file d’attente pour les travaux 100 est 3300. Il est logique de dire que la moyenne est de 33.

</dd> </dl>

</dd> <dt>

**ChangeType**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ BaseMetricDefinition**.**IsContinuous**")
</dt> </dl>

Indique comment la valeur de métrique change à l’aide d’attributs courants tels que le changement de direction, les valeurs minimales et maximales et la sémantique d’encapsulage.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)


</dt> <dd>

Le concepteur de mesures n’a pas qualifié le ChangeType.

</dd> <dt>

<span id="N_A"></span><span id="n_a"></span>

<span id="N_A"></span><span id="n_a"></span>**N/A** (2)


</dt> <dd>

Si la propriété « IsContinuous » a la valeur « false », ChangeType n’a pas de sens et doit être défini sur « N/A ».

</dd> <dt>

<span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span>

<span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span>**Compteur** (3)


</dt> <dd>

La métrique est une mesure de compteur. Il s’agit d’une valeur entière non négative qui augmente de façon monotone jusqu’à atteindre le nombre maximal pouvant être représenté, puis encapsuler et commencer à augmenter de 0. De tels compteurs, également appelés compteurs de substitution, peuvent être utilisés par exemple pour compter le nombre d’erreurs réseau ou le nombre de transactions traitées. La seule façon pour une application cliente d’effectuer le suivi de la boucle est de récupérer la valeur du compteur dans des intervalles de temps appropriés.

</dd> <dt>

<span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span>

<span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span>**Jauge** (4)


</dt> <dd>

La métrique est une mesure de jauge. Celles-ci ont des valeurs entières ou float qui peuvent augmenter et diminuer de façon arbitraire. Une jauge ne doit pas être renvoyée à la ligne lors de l’atteinte du nombre minimal ou maximal pouvant être représenté, à la place de la valeur « sticks » à ce nombre. Valeurs minimales ou maximales à l’intérieur de la plage de valeurs représentables auxquelles la valeur de métrique « bâtons » peut ou non être définie.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (5.. 32767)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fournisseur réservé** (32768.. 65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**DataType**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Type de données de la mesure.

<dt>

<span id="boolean"></span><span id="BOOLEAN"></span>

**booléen** (1)


</dt> <dd></dd> <dt>

<span id="char16"></span><span id="CHAR16"></span>

**char16** (2)


</dt> <dd></dd> <dt>

<span id="datetime"></span><span id="DATETIME"></span>

**DateTime** (3)


</dt> <dd></dd> <dt>

<span id="real32"></span><span id="REAL32"></span>

**real32** (4)


</dt> <dd></dd> <dt>

<span id="real64"></span><span id="REAL64"></span>

**real64** (5)


</dt> <dd></dd> <dt>

<span id="sint16"></span><span id="SINT16"></span>

**sint16** (6)


</dt> <dd></dd> <dt>

<span id="sint32"></span><span id="SINT32"></span>

**sint32** (7)


</dt> <dd></dd> <dt>

<span id="sint64"></span><span id="SINT64"></span>

**sint64** (8)


</dt> <dd></dd> <dt>

<span id="sint8"></span><span id="SINT8"></span>

**sint8** (9)


</dt> <dd></dd> <dt>

<span id="string"></span><span id="STRING"></span>

**chaîne** (10)


</dt> <dd></dd> <dt>

<span id="uint16"></span><span id="UINT16"></span>

**UInt16** (11)


</dt> <dd></dd> <dt>

<span id="uint32"></span><span id="UINT32"></span>

**UInt32** (12)


</dt> <dd></dd> <dt>

<span id="uint64"></span><span id="UINT64"></span>

**UInt64** (13)


</dt> <dd></dd> <dt>

<span id="uint8"></span><span id="UINT8"></span>

**UInt8** (14)


</dt> <dd></dd> </dl>

</dd> <dt>

**GatheringType**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique comment les valeurs de métriques sont collectées par l’instrumentation sous-jacente.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)


</dt> <dd>

Indique que le GatheringType est inconnu.

</dd> <dt>

<span id="OnChange"></span><span id="onchange"></span><span id="ONCHANGE"></span>

<span id="OnChange"></span><span id="onchange"></span><span id="ONCHANGE"></span>**OnChange** (2)


</dt> <dd>

Indique que les valeurs métriques CIM sont mises à jour immédiatement lorsque les valeurs de la ressource mesurée sont modifiées. Les valeurs des mesures OnChange reflètent véritablement la situation actuelle dans la ressource à tout moment. Par exemple, il s’agit du nombre d’utilisateurs connectés qui sont mis à jour immédiatement à mesure que les utilisateurs se connectent et se déconnectent.

</dd> <dt>

<span id="Periodic"></span><span id="periodic"></span><span id="PERIODIC"></span>

<span id="Periodic"></span><span id="periodic"></span><span id="PERIODIC"></span>**Périodique** (3)


</dt> <dd>

" : Indique que les valeurs métriques CIM sont mises à jour régulièrement. Par exemple, pour une application cliente, une valeur métrique s’appliquant à l’heure actuelle est constante pendant chaque intervalle de collecte, puis passe à la nouvelle valeur à la fin de chaque intervalle de collecte.

</dd> <dt>

<span id="OnRequest"></span><span id="onrequest"></span><span id="ONREQUEST"></span>

<span id="OnRequest"></span><span id="onrequest"></span><span id="ONREQUEST"></span>**OnRequest** (4)


</dt> <dd>

Indique que la valeur métrique CIM est déterminée à chaque fois qu’une application cliente la lit. Les valeurs des métriques OnRequest retournent véritablement la situation actuelle au sein de la ressource si une personne en fait la demande. Toutefois, ils ne changent pas « non respecté » et, par conséquent, l’abonnement aux modifications de valeur des métriques OnRequest n’est pas recommandé.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (5.. 32767)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fournisseur réservé** (32768.. 65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**Id**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

ID unique de la définition de la métrique. Les GUID/UUID OSF (Open Software Foundation) sont recommandés.

</dd> <dt>

**IsContinuous**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

True si la valeur métrique est continue ; Sinon, false.

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom de la mesure. Ce nom ne doit pas nécessairement être unique, mais il doit être descriptif et peut contenir des espaces vides.

</dd> <dt>

**ProgrammaticUnits**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Unités spécifiques d’une valeur. La valeur de cette propriété doit être une valeur légale du qualificateur d’unités de programmation, tel que défini dans l’annexe C. 1 de DSP0004 V 2.4 ou version ultérieure.

</dd> <dt>

**TimeScope**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ BaseMetricValue**](cim-basemetricvalue.md).**TimeStamp**","**CIM \_ BaseMetricValue**.**Duration**»)
</dt> </dl>

Étendue de temps qui s’applique au concepteur de mesures.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)


</dt> <dd>

Indique que l’étendue de l’heure n’a pas été qualifiée par le concepteur de mesures ou qu’elle est inconnue du fournisseur.

</dd> <dt>

<span id="Point"></span><span id="point"></span><span id="POINT"></span>

<span id="Point"></span><span id="point"></span><span id="POINT"></span>**Point** (2)


</dt> <dd>

Indique que la mesure s’applique à un point dans le temps. Sur les instances BaseMetricValue correspondantes, TimeStamp spécifie le point dans le temps et la durée est toujours 0.

</dd> <dt>

<span id="Interval"></span><span id="interval"></span><span id="INTERVAL"></span>

<span id="Interval"></span><span id="interval"></span><span id="INTERVAL"></span>**Intervalle** (3)


</dt> <dd>

Indique que la mesure s’applique à un intervalle de temps. Sur les instances BaseMetricValue correspondantes, TimeStamp spécifie la fin de l’intervalle de temps et la durée spécifie sa durée

</dd> <dt>

<span id="StartupInterval"></span><span id="startupinterval"></span><span id="STARTUPINTERVAL"></span>

<span id="StartupInterval"></span><span id="startupinterval"></span><span id="STARTUPINTERVAL"></span>**StartupInterval** (4)


</dt> <dd>

Indique que la mesure s’applique à un intervalle de temps qui a commencé au démarrage de la ressource mesurée (c’est-à-dire, le propriété ManagedElement associé à MetricDefForMe). Sur les instances BaseMetricValue correspondantes, TimeStamp spécifie la fin de l’intervalle de temps. Si la durée est égale à 0, cela indique que le temps de démarrage de la ressource mesurée est inconnu. Sinon, Duration spécifie la durée entre le démarrage de la ressource et l’horodateur.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (5.. 32767)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fournisseur réservé** (32768.. 65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**Unités**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Unités de la métrique. Par exemple, les octets, les paquets, les travaux, les fichiers, les millisecondes et les ampères.

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

[**\_Propriété MANAGEDELEMENT CIM**](cim-managedelement.md)
</dt> </dl>

 

