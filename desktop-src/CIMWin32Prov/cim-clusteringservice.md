---
description: La \_ classe CIM ClusteringService représente la fonctionnalité fournie par un cluster. Par exemple, la fonctionnalité de basculement peut être modélisée en tant que service d’un cluster de basculement.
ms.assetid: 550e3be3-c1e2-4714-b702-49cb1213c65b
ms.tgt_platform: multiple
title: Classe CIM_ClusteringService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ClusteringService
- CIM_ClusteringService.Caption
- CIM_ClusteringService.Description
- CIM_ClusteringService.InstallDate
- CIM_ClusteringService.Status
- CIM_ClusteringService.CreationClassName
- CIM_ClusteringService.Name
- CIM_ClusteringService.Started
- CIM_ClusteringService.StartMode
- CIM_ClusteringService.SystemCreationClassName
- CIM_ClusteringService.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dc31c760ea41761db06da5e1048d3ae1cc248c5fdde7f387e0cfeda209bb716a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119700929"
---
# <a name="cim_clusteringservice-class"></a>\_Classe CIM ClusteringService

La classe **CIM \_ ClusteringService** représente la fonctionnalité fournie par un cluster. Par exemple, la fonctionnalité de basculement peut être modélisée en tant que service d’un cluster de basculement.

> [!IMPORTANT]
> Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées. WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Abstract, UUID("{debac832-6b54-4add-8a62-8d3861b97b1d}"), AMENDMENT]
class CIM_ClusteringService : CIM_Service
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   CreationClassName;
  string   Name;
  boolean  Started;
  string   StartMode;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ ClusteringService** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **CIM \_ ClusteringService** possède ces méthodes.



| Méthode                                                                     | Description                                                                                                |
|:---------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [**AddNode**](addnode-method-in-class-cim-clusteringservice.md)           | Méthode de classe qui introduit un nouveau système informatique dans un cluster. Non implémenté par WMI.<br/>          |
| [**EvictNode**](evictnode-method-in-class-cim-clusteringservice.md)       | Méthode de la classe qui supprime un système informatique d’un cluster. Non implémenté par WMI.<br/>             |
| [**StartService**](startservice-method-in-class-cim-clusteringservice.md) | Méthode de classe qui tente de placer le service dans son état de démarrage. Non implémenté par WMI.<br/> |
| [**StopService**](stopservice-method-in-class-cim-clusteringservice.md)   | Méthode de classe qui place le service dans l’état arrêté. Non implémenté par WMI.<br/>              |



 

### <a name="properties"></a>Propriétés

La classe **CIM \_ ClusteringService** possède les propriétés suivantes.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)
</dt> </dl>

Brève description textuelle de l’objet.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nom de la classe")
</dt> </dl>

Nom de la classe ou de la sous-classe utilisée dans la création d’une instance. Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.

Cette propriété est héritée [**du \_ service CIM**](cim-service.md).

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")
</dt> </dl>

Description textuelle de l’objet.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")
</dt> </dl>

Indique le moment où l’objet a été installé. L’absence de valeur n’indique pas que l’objet n’est pas installé.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

La propriété Name identifie de façon unique le service et fournit une indication de la fonctionnalité gérée. Cette fonctionnalité est décrite plus en détail dans la propriété Description de l’objet.

Cette propriété est héritée [**du \_ service CIM**](cim-service.md).

</dd> <dt>

**Démarré**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Started")
</dt> </dl>

Si la **valeur est true**, le service a démarré.

Cette propriété est héritée [**du \_ service CIM**](cim-service.md).

</dd> <dt>

**StartMode**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« mode de démarrage »)
</dt> </dl>

Indique si le service est démarré automatiquement (par exemple, par un système d’exploitation) ou s’il est démarré uniquement à la demande.

Cette propriété est héritée [**du \_ service CIM**](cim-service.md).

<dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

**Automatique** (« automatique »)


</dt> <dd></dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

**Manuel** (« manuel »)


</dt> <dd></dd> </dl>

</dd> <dt>

**État**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")
</dt> </dl>

Chaîne qui indique l’état actuel de l’objet. L’état opérationnel et non opérationnel peut être défini. L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ». « Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).

L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ». Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives. Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

Les valeurs sont notamment les suivantes :

<dt>

<span id="OK"></span><span id="ok"></span>

**OK** (« OK »)


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Erreur** (« erreur »)


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Détérioré** (« détérioré »)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Inconnu** ("inconnu")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Échec** prévu (« échec prédit »)


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Démarrage** en cours (« démarrage »)


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Arrêt** en cours (« arrêt »)


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Service** (« service »)


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Stressed** (« stressed »)


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

Non **récupéré** (« non récupéré »)


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Aucun contact** (« aucun contact »)


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Communication perdue** (« inversée comm »)


</dt> <dd></dd> </dl>

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" System Class Name ")
</dt> </dl>

Nom de la classe de création du système d’étendue.

Cette propriété est héritée [**du \_ service CIM**](cim-service.md).

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" System Name ")
</dt> </dl>

Nom du système qui héberge le service.

Cette propriété est héritée [**du \_ service CIM**](cim-service.md).

</dd> </dl>

## <a name="remarks"></a>Remarques

La classe **CIM \_ ClusteringService** est dérivée [**du \_ service CIM**](cim-service.md).

WMI n’implémente pas cette classe.

Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF. Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Service CIM**](cim-service.md)
</dt> </dl>

 

