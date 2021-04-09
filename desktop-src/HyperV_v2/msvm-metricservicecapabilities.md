---
description: Décrit les fonctionnalités de l’instance MSVM \_ MetricService associée.
ms.assetid: 4E24D675-8265-4B5E-9551-550510B138FE
title: Classe Msvm_MetricServiceCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricServiceCapabilities
- Msvm_MetricServiceCapabilities.InstanceID
- Msvm_MetricServiceCapabilities.Caption
- Msvm_MetricServiceCapabilities.Description
- Msvm_MetricServiceCapabilities.ElementName
- Msvm_MetricServiceCapabilities.ElementNameEditSupported
- Msvm_MetricServiceCapabilities.MaxElementNameLen
- Msvm_MetricServiceCapabilities.RequestedStatesSupported
- Msvm_MetricServiceCapabilities.ElementNameMask
- Msvm_MetricServiceCapabilities.ControllableMetrics
- Msvm_MetricServiceCapabilities.MetricsControlTypes
- Msvm_MetricServiceCapabilities.ControllableManagedElements
- Msvm_MetricServiceCapabilities.ManagedElementControlTypes
- Msvm_MetricServiceCapabilities.SupportedMethods
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 635e153d3184e74ea581a045e3d6d54a5fea199f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868501"
---
# <a name="msvm_metricservicecapabilities-class"></a>MSVM \_ MetricServiceCapabilities, classe

Décrit les fonctionnalités de l’instance [**MSVM \_ MetricService**](msvm-metricservice.md) associée.

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricServiceCapabilities : CIM_MetricServiceCapabilities
{
  string  InstanceID;
  string  Caption = "Hyper-V Metric Service Capabilities";
  string  Description = "Defines Hyper-V Metric Service Capabilities";
  string  ElementName = "Hyper-V Metric Service Capabilities";
  boolean ElementNameEditSupported;
  unit16  MaxElementNameLen;
  unit16  RequestedStatesSupported[];
  string  ElementNameMask;
  string  ControllableMetrics[];
  uint16  MetricsControlTypes[];
  string  ControllableManagedElements[];
  uint16  ManagedElementControlTypes[];
  uint16  SupportedMethods[];
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ MetricServiceCapabilities** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ MetricServiceCapabilities** possède les propriétés suivantes.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Brève description de l’objet. Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « fonctionnalités du service métrique Hyper-V ».

</dd> <dt>

**ControllableManagedElements**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **arrayType** ("indexé")
</dt> </dl>

Identifie les instances de [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) qui peuvent être contrôlées par l' **instance \_ MetricService CIM** associée. Si cette propriété a la **valeur null**, tous les éléments peuvent être contrôlés. Cette propriété est héritée de la **\_ MetricServiceCapabilities CIM**.

</dd> <dt>

**ControllableMetrics**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **arrayType** ("indexé")
</dt> </dl>

Identifie les instances de **\_ BaseMetricDefinition CIM** qui peuvent être contrôlées par l' **instance \_ MetricService CIM** associée. Si cette propriété a la **valeur null**, toutes les mesures peuvent être contrôlées. Cette propriété est héritée de la **\_ MetricServiceCapabilities CIM**.

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Description de l'objet . Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et elle est toujours définie sur « définit les fonctionnalités du service métrique Hyper-V ».

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom complet de l’objet. Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « fonctionnalités du service métrique Hyper-V ».

</dd> <dt>

**ElementNameEditSupported**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la propriété **ElementName** peut être modifiée. Cette propriété est héritée de la **\_ EnabledLogicalElementCapabilities CIM**.

</dd> <dt>

**ElementNameMask**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie les restrictions sur **ElementName**, exprimées sous la forme d’une expression régulière. Cette propriété est héritée de la **\_ EnabledLogicalElementCapabilities CIM**.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **clé**
</dt> </dl>

Identifie de façon unique une instance de cette classe. Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**ManagedElementControlTypes**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **arrayType** ("indexé")
</dt> </dl>

Identifie le type de contrôle pris en charge par l’instance **\_ MetricService CIM** associée pour l’objet [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) identifié par la valeur dans le même index de tableau dans la propriété **ControllableManagedElements** . Si cette propriété a la **valeur null**, tous les types de contrôle sont pris en charge. Cette propriété est héritée de la **\_ MetricServiceCapabilities CIM**.



| Valeur                                                                                   | Signification                    |
|-----------------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>0</dt> </dl>            | Unknown<br/>         |
| <dl> <dt>2</dt> </dl>            | Discret<br/>        |
| <dl> <dt>3</dt> </dl>            | Bloc<br/>            |
| <dl> <dt>4</dt> </dl>            | Les deux<br/>            |
| <dl> <dt>5.. 32767</dt> </dl>     | DMTF, réservé<br/>   |
| <dl> <dt>32768.. 65535</dt> </dl> | Spécifique au fournisseur<br/> |



 

</dd> <dt>

**MaxElementNameLen**
</dt> <dd> <dl> <dt>

Type de données : **unit16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **MaxValue** (256)
</dt> </dl>

Spécifie la longueur maximale prise en charge de la propriété **ElementName** . Cette propriété est héritée de la **\_ EnabledLogicalElementCapabilities CIM**.

</dd> <dt>

**MetricsControlTypes**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **arrayType** ("indexé")
</dt> </dl>

Identifie le type de contrôle pris en charge par l’instance **\_ MetricService CIM** associée pour le **\_ BaseMetricDefinition CIM** identifié par la valeur dans le même index de tableau dans la propriété **ControllableMetrics** . Si cette propriété a la **valeur null**, tous les types de contrôle sont pris en charge. Cette propriété est héritée de la **\_ MetricServiceCapabilities CIM**.



| Valeur                                                                                   | Signification                    |
|-----------------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>0</dt> </dl>            | Unknown<br/>         |
| <dl> <dt>2</dt> </dl>            | Discret<br/>        |
| <dl> <dt>3</dt> </dl>            | Bloc<br/>            |
| <dl> <dt>4</dt> </dl>            | Les deux<br/>            |
| <dl> <dt>5.. 32767</dt> </dl>     | DMTF, réservé<br/>   |
| <dl> <dt>32768.. 65535</dt> </dl> | Spécifique au fournisseur<br/> |



 

</dd> <dt>

**RequestedStatesSupported**
</dt> <dd> <dl> <dt>

Type de données : tableau **unit16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique les États possibles qui peuvent être demandés lors de l’utilisation de la méthode **RequestStateChange** sur l’élément logique activé. Cette propriété est héritée de la **\_ EnabledLogicalElementCapabilities CIM**.



| Valeur                                                                         | Signification              |
|-------------------------------------------------------------------------------|----------------------|
| <dl> <dt>2</dt> </dl>  | activé<br/>   |
| <dl> <dt>3</dt> </dl>  | Désactive<br/>  |
| <dl> <dt>4</dt> </dl>  | Éteindre<br/> |
| <dl> <dt>6</dt> </dl>  | Hors connexion<br/>   |
| <dl> <dt>7</dt> </dl>  | Test<br/>      |
| <dl> <dt>8</dt> </dl>  | Fenêtres<br/>     |
| <dl> <dt>9</dt> </dl>  | Mettre en suspens<br/>   |
| <dl> <dt>10</dt> </dl> | Reboot<br/>    |
| <dl> <dt>11</dt> </dl> | Réinitialiser<br/>     |



 

</dd> <dt>

**SupportedMethods**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie les méthodes prises en charge par le service métrique. Cette propriété est héritée de la **\_ MetricServiceCapabilities CIM**.



| Valeur                                                                                   | Signification                                                                                         |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>2</dt> </dl>            | La méthode [**ControlMetrics**](controlmetrics-msvm-metricservice.md) est prise en charge.<br/> |
| <dl> <dt>3</dt> </dl>            | La méthode **ControlMetricsByClass** est prise en charge.<br/>                                   |
| <dl> <dt>4</dt> </dl>            | La méthode **ShowMetrics** est prise en charge.<br/>                                             |
| <dl> <dt>5</dt> </dl>            | La méthode **ShowMetricsByClass** est prise en charge.<br/>                                      |
| <dl> <dt>6</dt> </dl>            | La méthode **GetMetricValues** est prise en charge.<br/>                                         |
| <dl> <dt>7</dt> </dl>            | La méthode **ControlSampleTimes** est prise en charge.<br/>                                      |
| <dl> <dt>8.. 32767</dt> </dl>     | DMTF, réservé<br/>                                                                        |
| <dl> <dt>32768.. 65535</dt> </dl> | Spécifique au fournisseur<br/>                                                                      |



 

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_METRICSERVICECAPABILITIES CIM**](cim-metricservicecapabilities.md)
</dt> <dt>

[**MSVM \_ MetricService**](msvm-metricservice.md)
</dt> </dl>

 

