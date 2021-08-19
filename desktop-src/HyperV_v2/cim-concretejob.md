---
description: Version concrète de la classe de \_ tâche CIM. Cette classe représente une unité de travail instanciable générique à exécuter, telle qu’un traitement ou un travail d’impression.
ms.assetid: fad4d894-d1f5-428d-819f-74966dd9f410
title: Classe CIM_ConcreteJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConcreteJob
- CIM_ConcreteJob.InstanceID
- CIM_ConcreteJob.Name
- CIM_ConcreteJob.JobState
- CIM_ConcreteJob.TimeOfLastStateChange
- CIM_ConcreteJob.TimeBeforeRemoval
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a62ab2392ce2c069aa88ebb465f7028368f30bd5432cf96559c7eebe6edb8bdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117813160"
---
# <a name="cim_concretejob-class"></a>\_Classe CIM ConcreteJob

Version concrète de la classe [**de \_ tâche CIM**](cim-job.md) . Cette classe représente une unité de travail instanciable générique à exécuter, telle qu’un traitement ou un travail d’impression.

## <a name="syntax"></a>Syntaxe

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_ConcreteJob : CIM_Job
{
  string   InstanceID;
  string   Name;
  uint16   JobState;
  datetime TimeOfLastStateChange;
  datetime TimeBeforeRemoval = "00000000000500.000000:000";
};
```

## <a name="members"></a>Membres

La classe **CIM \_ ConcreteJob** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **CIM \_ ConcreteJob** possède ces méthodes.



| Méthode                                                           | Description                                                                          |
|:-----------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [**GetError**](cim-concretejob-geterror.md)                     | Récupère les informations d’erreur pour l’état opérationnel d’un travail concret.<br/> |
| [**RequestStateChange**](cim-concretejob-requeststatechange.md) | Demande le changement d’état spécifié à un travail concret.<br/>                    |



 

### <a name="properties"></a>Propriétés

La classe **CIM \_ ConcreteJob** possède les propriétés suivantes.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceId")
</dt> </dl>

Identifie de façon unique et opaque une instance de cette classe dans la portée de l’espace de noms conteneur.

> [!IMPORTANT]
>
> Pour garantir l’unicité au sein de l’espace de noms, la valeur de la propriété **InstanceID** doit être construite au format suivant : *identifiant OrgID*:*LocalID*
>
> *Identifiant OrgID* doit inclure un nom de droits d’auteur, de marque déposée ou d’autre nom unique qui est détenu par l’entité métier qui définit l' **InstanceID**, ou être un ID inscrit qui est affecté par une autorité globale reconnue. Ce modèle est similaire à la structure des noms de classes de schéma. En outre, pour garantir l’unicité, les premiers deux-points dans **InstanceID** doivent être compris entre *identifiant OrgID* et *LocalID*. Par conséquent, le *identifiant OrgID* ne doit pas contenir de signe deux-points («  : »).
>
> *LocalID* est choisi par l’entité métier et ne doit pas être réutilisé pour identifier des éléments réels sous-jacents différents.
>
> Si le modèle ci-dessus n’est pas utilisé, l’entité de définition doit s’assurer que la valeur **InstanceID** obtenue n’est pas réutilisée dans les propriétés **InstanceID** produites par ce fournisseur ou d’autres fournisseurs pour cet espace de noms.
>
> Pour les instances définies pour Distributed Management Task Force (DMTF), le modèle doit être utilisé avec le *identifiant OrgID* défini sur CIM.

 

</dd> <dt>

**JobState**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

L’état opérationnel du travail et la transition entre ces États.

<dt>

<span id="New"></span><span id="new"></span><span id="NEW"></span>

<span id="New"></span><span id="new"></span><span id="NEW"></span>**Nouveau** (2)


</dt> <dd>

le travail n’a jamais été démarré.

</dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Démarrage** (3)


</dt> <dd>

Le travail passe des États « nouveau », « suspendu » ou « service » à l’État « en cours d’exécution ».

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**En cours d’exécution** (4)


</dt> <dd>

Le travail est en cours d’exécution.

</dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspendu** (5)


</dt> <dd>

La tâche est arrêtée, mais peut être redémarrée de manière transparente.

</dd> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arrêt** (6)


</dt> <dd>

Le travail passe à l’état « terminé », « terminé » ou « mort ».

</dd> <dt>

<span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>

<span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Terminé** (7)


</dt> <dd>

Le travail s’est terminé normalement.

</dd> <dt>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Terminé** (8)


</dt> <dd>

La tâche a été arrêtée par une demande de modification d’État « Terminate ». Le travail et tous ses processus sous-jacents sont terminés et peuvent être redémarrés (il s’agit d’un travail spécifique) uniquement en tant que nouveau travail.

</dd> <dt>

<span id="Killed"></span><span id="killed"></span><span id="KILLED"></span>

<span id="Killed"></span><span id="killed"></span><span id="KILLED"></span>**Abattu** (9)


</dt> <dd>

La tâche a été arrêtée par une demande de modification d’État « Kill ». Les processus sous-jacents peuvent avoir été laissés s’exécuter et le nettoyage peut être nécessaire pour libérer des ressources.

</dd> <dt>

<span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span>

<span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span>**Exception** (10)


</dt> <dd>

La tâche est dans un état anormal qui peut indiquer une condition d’erreur. L’état réel peut être affiché en dépit d’objets spécifiques à un travail.

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (11)


</dt> <dd>

La tâche est dans un état spécifique au fournisseur qui prend en charge la détection des problèmes, ou la résolution, ou les deux.

</dd> <dt>

<span id="Query_Pending"></span><span id="query_pending"></span><span id="QUERY_PENDING"></span>

<span id="Query_Pending"></span><span id="query_pending"></span><span id="QUERY_PENDING"></span>**Requête en attente** (12)


</dt> <dd>

En attente de la résolution d’une requête par un client.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (13.. 32767)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fournisseur réservé** (32768.. 65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**obligatoire**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")
</dt> </dl>

Nom convivial de l’instance. En outre, le nom convivial peut être utilisé en tant que propriété pour une recherche ou une requête.

> [!Note]  
> Le nom ne doit pas nécessairement être unique au sein de l’espace de noms.

 

</dd> <dt>

**TimeBeforeRemoval**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [ **requis**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Indique la durée de conservation d’un travail terminé. La valeur par défaut est « 00000000000500.000000:000 » (cinq minutes).

</dd> <dt>

**TimeOfLastStateChange**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Date ou heure de la dernière modification de l’état du travail.

> [!Note]  
> Si l’état de la tâche n’a pas changé et que cette propriété est remplie, elle doit être définie sur une valeur d’intervalle égale à zéro.

 

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

[**\_Travail CIM**](cim-job.md)
</dt> </dl>

 

