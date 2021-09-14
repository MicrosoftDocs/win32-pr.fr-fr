---
description: Représente un travail créé à l’aide de la commande AT.
ms.assetid: 2fa69e3f-9a6c-4aa9-8a6c-ea28eb4342ca
ms.tgt_platform: multiple
title: Classe Win32_ScheduledJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ScheduledJob
- Win32_ScheduledJob.Caption
- Win32_ScheduledJob.Description
- Win32_ScheduledJob.InstallDate
- Win32_ScheduledJob.Name
- Win32_ScheduledJob.Status
- Win32_ScheduledJob.ElapsedTime
- Win32_ScheduledJob.Notify
- Win32_ScheduledJob.Owner
- Win32_ScheduledJob.Priority
- Win32_ScheduledJob.TimeSubmitted
- Win32_ScheduledJob.UntilTime
- Win32_ScheduledJob.Command
- Win32_ScheduledJob.DaysOfMonth
- Win32_ScheduledJob.DaysOfWeek
- Win32_ScheduledJob.InteractWithDesktop
- Win32_ScheduledJob.JobId
- Win32_ScheduledJob.JobStatus
- Win32_ScheduledJob.RunRepeatedly
- Win32_ScheduledJob.StartTime
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 50162221e7ca18e07e3599deca2dba67b18ba708
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127124230"
---
# <a name="win32_scheduledjob-class"></a>\_Classe ScheduledJob Win32

La  [classe WMI](../wmisdk/retrieving-a-class.md) **\_ ScheduledJob** WMI   représente un travail créé à l’aide de la commande **at** .

> [!Note]  
> La classe **Win32 \_ ScheduledJob** ne représente pas un travail créé à l’aide de l’Assistant tâche planifiée à partir du panneau de configuration. Vous ne pouvez pas modifier une tâche créée par WMI dans l’interface utilisateur tâches planifiées. Pour plus d'informations, consultez la section Notes.

 

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4E0-5FBB-11D2-AAC1-006008C78BC7}"), SupportsCreate, CreateBy("Create"), SupportsDelete, DeleteBy("Delete"), AMENDMENT]
class Win32_ScheduledJob : CIM_Job
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  datetime ElapsedTime;
  string   Notify;
  string   Owner;
  uint32   Priority;
  datetime TimeSubmitted;
  datetime UntilTime;
  string   Command;
  uint32   DaysOfMonth;
  uint32   DaysOfWeek;
  boolean  InteractWithDesktop;
  uint32   JobId;
  string   JobStatus;
  boolean  RunRepeatedly;
  datetime StartTime;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ ScheduledJob** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **Win32 \_ ScheduledJob** possède ces méthodes.



| Méthode                                                      | Description                                                                                                           |
|:------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [**Créer**](create-method-in-class-win32-scheduledjob.md) | Méthode de classe qui envoie un travail au système d’exploitation pour l’exécuter à une date et une heure futures spécifiées.<br/> |
| [**Supprimer**](delete-method-in-class-win32-scheduledjob.md) | Méthode de classe qui supprime une tâche planifiée.<br/>                                                                 |



 

### <a name="properties"></a>Propriétés

La classe **Win32 \_ ScheduledJob** a ces propriétés.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Caption »)
</dt> </dl>

Brève description textuelle de l’objet.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**Commande**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api les \| structures \| [**de gestion de réseau at \_ info**](/windows/win32/api/lmat/ns-lmat-at_info) \| **Command**")
</dt> </dl>

Nom de la commande, du programme de traitement par lots ou du fichier binaire (et des arguments de ligne de commande) que le service de planification utilise pour appeler le travail.

Exemple : "**Defrag** **/q/f**"

</dd> <dt>

**DaysOfMonth**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| [**at \_ info**](/windows/win32/api/lmat/ns-lmat-at_info) \| **DaysOfMonth**»)
</dt> </dl>

Jours du mois où la tâche est planifiée pour s’exécuter. Si un travail est planifié pour s’exécuter sur plusieurs jours du mois, ces valeurs peuvent être jointes dans un ou logique. Par exemple, si un travail doit s’exécuter le 1er et le 16 de chaque mois, la valeur de la propriété **DaysOfMonth** est 1 ou 32768.

<dt>

<span id="1"></span>

<span id="1"></span>**1** (1)


</dt> <dd>

premier

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2** (2)


</dt> <dd>

2

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**3** (4)


</dt> <dd>

3e

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**4** (8)


</dt> <dd>

4e

</dd> <dt>

<span id="5"></span>

<span id="5"></span>**5** (16)


</dt> <dd>

5e

</dd> <dt>

<span id="6"></span>

<span id="6"></span>**6** (32)


</dt> <dd>

6e

</dd> <dt>

<span id="7"></span>

<span id="7"></span>**7** (64)


</dt> <dd>

7e

</dd> <dt>

<span id="8"></span>

<span id="8"></span>**8** (128)


</dt> <dd>

8e

</dd> <dt>

<span id="9"></span>

<span id="9"></span>**9** (256)


</dt> <dd>

9e

</dd> <dt>

<span id="10"></span>

<span id="10"></span>**10** (512)


</dt> <dd>

Palmarè

</dd> <dt>

<span id="11"></span>

<span id="11"></span>**11** (1024)


</dt> <dd>

11th

</dd> <dt>

<span id="12"></span>

<span id="12"></span>**12** (2048)


</dt> <dd>

12th

</dd> <dt>

<span id="13"></span>

<span id="13"></span>**13** (4096)


</dt> <dd>

13th

</dd> <dt>

<span id="14"></span>

<span id="14"></span>**14** (8192)


</dt> <dd>

14e

</dd> <dt>

<span id="15"></span>

<span id="15"></span>**15** (16384)


</dt> <dd>

15

</dd> <dt>

<span id="16"></span>

<span id="16"></span>**16** (32768)


</dt> <dd>

16

</dd> <dt>

<span id="17"></span>

<span id="17"></span>**17** (65536)


</dt> <dd>

septième

</dd> <dt>

<span id="18"></span>

<span id="18"></span>**18** (131072)


</dt> <dd>

18e

</dd> <dt>

<span id="19"></span>

<span id="19"></span>**19** (262144)


</dt> <dd>

dix

</dd> <dt>

<span id="20"></span>

<span id="20"></span>**20** (524288)


</dt> <dd>

vingtième

</dd> <dt>

<span id="21"></span>

<span id="21"></span>**21** (1048576)


</dt> <dd>

21st

</dd> <dt>

<span id="22"></span>

<span id="22"></span>**22** (2097152)


</dt> <dd>

22nd

</dd> <dt>

<span id="23"></span>

<span id="23"></span>**23** (4194304)


</dt> <dd>

23rd

</dd> <dt>

<span id="24"></span>

<span id="24"></span>**24** (8388608)


</dt> <dd>

24

</dd> <dt>

<span id="25"></span>

<span id="25"></span>**25** (16777216)


</dt> <dd>

vingt

</dd> <dt>

<span id="26"></span>

<span id="26"></span>**26** (33554432)


</dt> <dd>

26

</dd> <dt>

<span id="27"></span>

<span id="27"></span>**27** (67108864)


</dt> <dd>

27

</dd> <dt>

<span id="28"></span>

<span id="28"></span>**28** (134217728)


</dt> <dd>

28

</dd> <dt>

<span id="29"></span>

<span id="29"></span>**29** (268435456)


</dt> <dd>

29

</dd> <dt>

<span id="30"></span>

<span id="30"></span>**30** (536870912)


</dt> <dd>

30e

</dd> <dt>

<span id="31"></span>

<span id="31"></span>**31** (1073741824)


</dt> <dd>

31

</dd> </dl>

</dd> <dt>

**DaysOfWeek**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| structures de gestion \| [**de réseau at \_ info**](/windows/win32/api/lmat/ns-lmat-at_info) \| **DaysOfWeek**")
</dt> </dl>

Jours de la semaine où un travail est planifié pour s’exécuter. Si un travail est planifié pour s’exécuter plusieurs jours de la semaine, les valeurs peuvent être jointes dans un ou logique. Par exemple, si un travail est planifié pour s’exécuter le lundi, le mercredi et le vendredi, la valeur de la propriété **DaysOfWeek** est 1, 4 ou 16.

<dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>

**Lundi** (1)


</dt> <dd></dd> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>

**Mardi** (2)


</dt> <dd></dd> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>

**Mercredi** (4)


</dt> <dd></dd> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>

**Jeudi** (8)


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

**Vendredi** (16)


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

**Samedi** (32)


</dt> <dd></dd> <dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>

**Dimanche** (64)


</dt> <dd></dd> </dl>

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")
</dt> </dl>

Description textuelle de l’objet.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**ElapsedTime**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Durée d’exécution du travail.

Cette propriété est héritée de la [**\_ tâche CIM**](cim-job.md).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" date d’installation ")
</dt> </dl>

Indique le moment où l’objet a été installé. L’absence de valeur n’indique pas que l’objet n’est pas installé.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**InteractWithDesktop**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| structures de gestion de réseau win32api \| [**at \_ info**](/windows/win32/api/lmat/ns-lmat-at_info) \| **Flags** \| **Job non \_ interactive**")
</dt> </dl>

Le travail spécifié est interactif, ce qui signifie qu’un utilisateur peut fournir une entrée à une tâche planifiée pendant son exécution.

</dd> <dt>

**JobId**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| [**at \_ enum**](/windows/win32/api/lmat/ns-lmat-at_enum) \| **JobID**»)
</dt> </dl>

Numéro d’identification du travail. Elle est utilisée par les méthodes comme handle d’une tâche planifiée sur cet ordinateur.

</dd> <dt>

**JobStatus**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) ("JobStatus"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api les \| structures de gestion \| de réseau à l’indicateur d'[**\_ énumération du**](/windows/win32/api/lmat/ns-lmat-at_enum) \|  \| **travail \_ Exec \_ Error**")
</dt> </dl>

État de l’exécution lors de la dernière planification de l’exécution de ce travail.

<dt>

<span id="Success"></span><span id="success"></span><span id="SUCCESS"></span>

**Succès** (« réussite »)


</dt> <dd></dd> <dt>

<span id="Failure"></span><span id="failure"></span><span id="FAILURE"></span>

**Échec** (« échec »)


</dt> <dd></dd> </dl>

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")
</dt> </dl>

Étiquette par laquelle l’objet est connu. Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**Notifier**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

L’utilisateur est averti en cas d’achèvement ou d’échec de la tâche.

Cette propriété est héritée de la [**\_ tâche CIM**](cim-job.md).

</dd> <dt>

**Propriétaire**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Utilisateur qui a envoyé le travail.

Cette propriété est héritée de la [**\_ tâche CIM**](cim-job.md).

</dd> <dt>

**Priorité**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Importance de l’exécution d’un travail.

Cette propriété est héritée de la [**\_ tâche CIM**](cim-job.md).

</dd> <dt>

**RunRepeatedly**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api les \| structures \| [**de gestion de réseau at \_ info**](/windows/win32/api/lmat/ns-lmat-at_info) \| **Flags** \| **\_ fonctionnent \_ régulièrement**")
</dt> </dl>

La tâche planifiée s’exécute de manière répétée les jours où la tâche est planifiée. Si la **valeur est false**, la tâche est exécutée une fois.

</dd> <dt>

**StartTime**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) ("StartTime"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| structures de gestion de réseau win32api \| [**au JobTime \_ enum**](/windows/win32/api/lmat/ns-lmat-at_enum) \| ")
</dt> </dl>

Heure UTC d’exécution du travail, sous la forme «AAAAMMJJHHMMSS. MMMMMM (+-) OOO», où « AAAAMMJJ » doit être remplacé par « \* \* \* \* \* \* \* \* ». Le remplacement est nécessaire, car le service de planification autorise uniquement la configuration des tâches à exécuter une seule fois, ou une exécution le jour du mois ou de la semaine. Une tâche ne peut pas être exécutée à une date spécifique.

La section « (+-) OOO » de la valeur de la propriété **StartTime** est le décalage actuel pour la traduction de l’heure locale. Le biais correspond à la différence entre l’heure UTC et l’heure locale. Pour calculer le décalage pour votre fuseau horaire, multipliez le nombre d’heures d’avance ou de retard de l’heure de Greenwich (GMT) par 60 (utilisez un nombre positif comme nombre d’heures avant l’heure GMT et un nombre négatif si votre fuseau horaire est situé en arrière-plan GMT). Ajoutez un 60 supplémentaire à votre calcul si votre fuseau horaire utilise l’heure d’été. Par exemple, le fuseau horaire Pacifique est de huit heures après l’heure GMT. par conséquent, le décalage est égal à-420 (-8 \* 60 + 60) lorsque l’heure d’été est utilisée et-480 (-8 \* 60) lorsque l’heure d’été n’est pas utilisée. Vous pouvez également déterminer la valeur du décalage en interrogeant la propriété Bias de la classe [**Win32 \_ TimeZone**](win32-timezone.md) .

Par exemple : « \* \* \* \* \* \* \* \* 123000.000000-420 » spécifie 14,30 (2:30 P.M.) PST avec l’heure d’été en vigueur.

</dd> <dt>

**État**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")
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

**TimeSubmitted**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Heure à laquelle le travail a été soumis.

Cette propriété est héritée de la [**\_ tâche CIM**](cim-job.md).

</dd> <dt>

**UntilTime**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Heure à laquelle le travail n’est pas valide ou doit être arrêté.

Cette propriété est héritée de la [**\_ tâche CIM**](cim-job.md).

</dd> </dl>

## <a name="remarks"></a>Notes

Chaque travail planifié sur le service de planification est stocké de façon permanente (le planificateur peut démarrer un travail après un redémarrage) et est exécuté à l’heure et au jour spécifiés de la semaine ou du mois. Si l’ordinateur n’est pas actif ou si le service planifié n’est pas en cours d’exécution à l’heure de travail spécifiée, le service de planification exécute le travail spécifié le jour suivant à l’heure spécifiée.

Les travaux sont planifiés en fonction du temps universel coordonné (UTC, Universal Time Coordinated) avec décalage de décalage par rapport à l’heure GMT (Greenwich Mean Time), ce qui signifie qu’un travail peut être spécifié à l’aide de n’importe quel fuseau horaire. La **classe \_ ScheduledJob Win32** retourne l’heure locale avec décalage UTC lors de l’énumération d’un objet et convertit en heure locale lors de la création de nouveaux travaux. Par exemple, un travail spécifié pour s’exécuter sur un ordinateur de Boston à 10:30 h 00. Le lundi heure du Pacifique sera planifié pour s’exécuter en local à 1:30 h 00 Mardi est.

> [!Note]  
> Un client doit prendre en compte si l’heure d’été est en cours d’exécution sur l’ordinateur local, et si c’est le cas, soustraire un décalage de 60 minutes à partir de l’offset UTC.

 

La classe **Win32 \_ ScheduledJob** est dérivée de la [**\_ tâche CIM**](cim-job.md). Vous devez être membre du groupe administrateurs pour créer une tâche planifiée à l’aide de cette classe.

la classe **Win32 \_ ScheduledJob** utilise en interne le protocole AT, qui est lié à la désapprobation à partir de Windows 8 et Windows Server 2012. Dans un premier temps, le protocole AT est désactivé par défaut. Si le protocole est désactivé, par exemple, l’appel de la méthode [**Create**](create-method-in-class-win32-scheduledjob.md) sur un objet **Win32 \_ ScheduledJob** échoue avec l’erreur 0x8. Vous pouvez réactiver le protocole AT en ajoutant l’entrée de Registre suivante :

``` syntax
Key: HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Schedule\Configuration 
Name: EnableAt 
Type: REG_DWORD
Value: 1
```

Vous devrez peut-être redémarrer l’ordinateur pour que le paramètre soit effectif.

Étant donné que **Win32 \_ ScheduledJob** est basé sur l’API Win32 [**NetScheduleJobGetInfo**](/windows/win32/api/lmat/nf-lmat-netschedulejobgetinfo) , vous ne pouvez pas utiliser cette classe conjointement avec l’planificateur de tâches. Si vous souhaitez utiliser Planificateur de tâches, utilisez l’API Planificateur de tâches. Pour plus d’informations, consultez la [référence planificateur de tâches](../taskschd/task-scheduler-reference.md).

## <a name="examples"></a>Exemples

L’exemple de code VBScript suivant planifie l’exécution de Notepad.exe de manière interactive à 1:25 par l’heure de l’ordinateur local tous les mercredis.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2")
Set objNewJob = objWMIService.Get("Win32_ScheduledJob")
errJobCreated = objNewJob.Create("Notepad.exe", "********012500.000000-420", True , 4, , True, JobId) 
If errJobCreated <> 0 Then
Wscript.Echo "Error on task creation"
Else
Wscript.Echo "Task created"
End If
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Travail CIM**](cim-job.md)
</dt> <dt>

[Classes du système d’exploitation](./operating-system-classes.md)
</dt> <dt>

[Tâches WMI : tâches planifiées](../wmisdk/wmi-tasks--scheduled-tasks.md)
</dt> </dl>

 

 
