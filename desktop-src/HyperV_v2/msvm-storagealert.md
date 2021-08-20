---
description: Représente un événement déclenché chaque fois que la propriété OperationalStatus de la classe MSVM \_ ResourcePool ou MSVM \_ LogicalDisk change.
ms.assetid: 20E7C22A-A151-4EDC-90D8-4BCD53C42355
title: Classe Msvm_StorageAlert
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageAlert
- Msvm_StorageAlert.AlertingManagedElement
- Msvm_StorageAlert.AlertingElementFormat
- Msvm_StorageAlert.OtherAlertingElementFormat
- Msvm_StorageAlert.AlertType
- Msvm_StorageAlert.PerceivedSeverity
- Msvm_StorageAlert.ProbableCause
- Msvm_StorageAlert.ProbableCauseDescription
- Msvm_StorageAlert.EventTime
- Msvm_StorageAlert.OwningEntity
- Msvm_StorageAlert.MessageArguments
- Msvm_StorageAlert.MessageID
- Msvm_StorageAlert.Message
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 478b4617f56c73e425d833842b313767f85c385e9142314a7ca8978b5783f492
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950228"
---
# <a name="msvm_storagealert-class"></a>MSVM \_ StorageAlert, classe

Représente un événement déclenché chaque fois que la propriété **OperationalStatus** de la classe [**MSVM \_ ResourcePool**](msvm-resourcepool.md) ou [**MSVM \_ LogicalDisk**](msvm-logicaldisk.md) change.

La syntaxe suivante est simplifiée à partir du code MOF et comprend ces propriétés.

## <a name="syntax"></a>Syntaxe

``` syntax
[Indication, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_StorageAlert : CIM_AlertIndication
{
  string   AlertingManagedElement[];
  uint16   AlertingElementFormat;
  uint16   OtherAlertingElementFormat;
  uint16   AlertType;
  uint16   PerceivedSeverity;
  uint16   ProbableCause;
  string   ProbableCauseDescription;
  datetime EventTime;
  string   OwningEntity;
  string   MessageArguments[];
  string   MessageID;
  string   Message;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ StorageAlert** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ StorageAlert** possède les propriétés suivantes.

<dl> <dt>

**AlertingElementFormat**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **ModelCorrespondence** ("CIM \_ AlertIndication. AlertingManagedElement", "CIM \_ AlertIndication. OtherAlertingElementFormat")
</dt> </dl>

Spécifie le format de la propriété **AlertingManagedElement** . Le format est un CIMObjectPath, avec le format *<NamespacePath> : <ClassName> . <Prop1> = \\ " <Value1> \\ ", " <Prop2> = \\ " <Value2> \\ "*, qui spécifie une instance dans le schéma CIM.

Cette propriété est héritée de la classe **CIM \_ AlertIndication** .

Les valeurs possibles sont les suivantes :

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)
</dt> <dt>

<span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>**CIMObjectPath** (2)
</dt> </dl>

</dd> <dt>

**AlertingManagedElement**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chemins d’accès WMI de l’instance pour laquelle l’alerte est générée.

</dd> <dt>

**AlertType**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie la classification principale de l’alerte. Les valeurs possibles pour cette propriété sont :

<dl> <dt>

<span id="Quality_of_Service_Alert"></span><span id="quality_of_service_alert"></span><span id="QUALITY_OF_SERVICE_ALERT"></span>**Alerte de qualité de service** (3)
</dt> </dl>

</dd> <dt>

**EventTime**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Date et heure de détection de l’événement sous-jacent.

</dd> <dt>

**Message**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Message mis en forme qui est construit en combinant tout ou partie des éléments dynamiques spécifiés dans la propriété **MessageArguments** avec les éléments statiques identifiés de manière unique par la propriété **MessageID** dans un registre de messages ou un autre catalogue associé à la propriété **OwningEntity** .

</dd> <dt>

**MessageArguments**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Tableau qui contient le contenu dynamique du message. Si la valeur de **MessageID** est 32930, l’argument situé à la position 0 est le **PoolID** de l’instance [**MSVM \_ ResourcePool**](msvm-resourcepoolcomponent.md) pour laquelle l’alerte est générée.

</dd> <dt>

**MessageID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Identifie de façon unique, dans l’étendue de la propriété **OwningEntity** , le format de la propriété de **message** . Les valeurs possibles pour cette propriété sont :

32930 (« Message de débit insuffisant QoS du Pool Stockage »)

</dd> <dt>

**OtherAlertingElementFormat**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chaîne qui définit les valeurs « Other » pour **AlertingManagedElement**. Cette valeur doit être définie sur une valeur non NULL lorsque **AlertingManagedElement** est défini sur une valeur de 1 (« other »). Pour toutes les autres valeurs de **AlertingManagedElement**, la valeur de cette chaîne doit être définie sur null.

Cette propriété est héritée de la classe **CIM \_ AlertIndication** .

</dd> <dt>

**OwningEntity**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Identifie de façon unique l’entité qui possède la définition du format du **message** décrit dans cette instance. la valeur de cette propriété est toujours « Microsoft-Windows-Hyper-V ».

« Microsoft-Windows-Hyper-V »

</dd> <dt>

**PerceivedSeverity**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Décrit la gravité de l’indication d’alerte. Les valeurs possibles pour cette propriété sont :

<dl> <dt>

<span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Informations** (2)
</dt> <dt>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Détérioré/AVERTISSEMENT** (3)
</dt> </dl>

</dd> <dt>

**ProbableCause**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Décrit la cause probable de la situation qui a entraîné l’indication de l’alerte.

<dl> <dt>

<span id="Storage_Capacity_Problem"></span><span id="storage_capacity_problem"></span><span id="STORAGE_CAPACITY_PROBLEM"></span>**Stockage problème de capacité** (50)
</dt> <dt>

<span id="Previous_Alert_Cleared"></span><span id="previous_alert_cleared"></span><span id="PREVIOUS_ALERT_CLEARED"></span>**Alerte précédente effacée** (59)
</dt> </dl>

</dd> <dt>

**ProbableCauseDescription**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Description textuelle qui correspond à la valeur de la propriété **ProbableCause** .

</dd> </dl>

## <a name="remarks"></a>Remarques

Le fournisseur WMI Hyper-V ne déclenche pas d’événements pour des disques virtuels individuels afin d’éviter d’inonder les clients avec des événements en cas de dysfonctionnements à grande échelle des systèmes de stockage sous-jacents.

lorsqu’un client reçoit un événement **Msvm \_ StorageAlert** , si la valeur de la propriété **ProbableCause** est 50 (Stockage problème de capacité), le client peut détecter les disques virtuels qui fonctionnent en dehors de leur stratégie de QoS à l’aide de l’une des procédures suivantes :

-   Interrogez toutes les instances de [**\_ disque logique MSVM**](msvm-logicaldisk.md) allouées à partir du pool de ressources pour lequel l’événement a été généré. Ces instances de **\_ disque logique MSVM** sont associées au pool de ressources via l’Association [**MSVM \_ ElementAllocatedFromPool**](msvm-elementallocatedfrompool.md) .
-   Filtrez la liste des résultats en sélectionnant les instances dont OperationalStatus contient un débit insuffisant.

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

[**\_ALERTINDICATION CIM**](cim-alertindication.md)
</dt> <dt>

[**\_Disque logique MSVM**](msvm-logicaldisk.md)
</dt> <dt>

[**MSVM \_ ResourcePool**](msvm-resourcepoolcomponent.md)
</dt> </dl>

 

 




