---
description: Élément logique qui représente une unité de travail à exécuter, par exemple un script ou un travail d’impression. Un travail est différent d’un processus, car un travail peut être planifié ou mis en file d’attente, et son exécution n’est pas limitée à un seul système.
ms.assetid: 35e35c3f-617b-429b-b68f-fa0c0c330e92
title: Classe CIM_Job (gestion Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Job
- CIM_Job.JobStatus
- CIM_Job.TimeSubmitted
- CIM_Job.ScheduledStartTime
- CIM_Job.StartTime
- CIM_Job.ElapsedTime
- CIM_Job.JobRunTimes
- CIM_Job.RunMonth
- CIM_Job.RunDay
- CIM_Job.RunDayOfWeek
- CIM_Job.RunStartInterval
- CIM_Job.LocalOrUtcTime
- CIM_Job.UntilTime
- CIM_Job.Notify
- CIM_Job.Owner
- CIM_Job.Priority
- CIM_Job.PercentComplete
- CIM_Job.DeleteOnCompletion
- CIM_Job.ErrorCode
- CIM_Job.ErrorDescription
- CIM_Job.RecoveryAction
- CIM_Job.OtherRecoveryAction
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8eb8f63ec9d2cdd881a2ba0946f83a40fb8be866
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474585"
---
# <a name="cim_job-class-hyper-v-management"></a>Classe CIM_Job (gestion Hyper-V)

Élément logique qui représente une unité de travail à exécuter, par exemple un script ou un travail d’impression. Un travail est différent d’un processus, car un travail peut être planifié ou mis en file d’attente, et son exécution n’est pas limitée à un seul système.

## <a name="syntax"></a>Syntaxe

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_Job : CIM_LogicalElement
{
  string   JobStatus;
  datetime TimeSubmitted;
  datetime ScheduledStartTime;
  datetime StartTime;
  datetime ElapsedTime;
  uint32   JobRunTimes = 1;
  uint8    RunMonth;
  sint8    RunDay;
  sint8    RunDayOfWeek;
  datetime RunStartInterval;
  uint16   LocalOrUtcTime;
  datetime UntilTime;
  string   Notify;
  string   Owner;
  uint32   Priority;
  uint16   PercentComplete;
  boolean  DeleteOnCompletion;
  uint16   ErrorCode;
  string   ErrorDescription;
  uint16   RecoveryAction;
  string   OtherRecoveryAction;
};
```

## <a name="members"></a>Membres

La classe de **\_ tâche CIM** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe de **\_ tâche CIM** possède ces méthodes.




| Méthode | Description | 
|--------|-------------|
| <a href="cim-job-killjob.md"><strong>KillJob</strong></a> | Cette méthode est déconseillée. Utilisez à la place la méthode <strong>RequestStateChange</strong> .<br /><blockquote>[!Note]<br />Description déconseillée : ferme un travail.</blockquote><br /> | 




 

### <a name="properties"></a>Propriétés

La classe de **\_ tâche CIM** possède ces propriétés.

<dl> <dt>

**DeleteOnCompletion**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

**True** pour supprimer le travail une fois l’opération terminée ; Sinon, **false**.

> [!Note]  
> Cette propriété ne supprime pas les travaux qui se terminent avant que cette propriété ait la valeur **true**.

 

</dd> <dt>

**ElapsedTime**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Durée d’exécution du travail.

</dd> <dt>

**ErrorCode**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) («**\_ tâche CIM**.**ErrorDescription**»)
</dt> </dl>

Code d’erreur spécifique au fournisseur qui capture les informations de traitement des tâches récurrentes. La valeur doit être égale à zéro si le travail s’est terminé sans erreur.

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) («**\_ tâche CIM**.**ErrorCode**»)
</dt> </dl>

Chaîne de forme libre qui contient une description du code d’erreur correspondant dans la propriété **ErrorCode** .

</dd> <dt>

**JobRunTimes**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Nombre de fois où le travail est exécuté.

</dd> <dt>

**JobStatus**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).**OperationalStatus**»)
</dt> </dl>

Chaîne de forme libre qui représente l’état du travail.

</dd> <dt>

**LocalOrUtcTime**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Indique si les heures dans les propriétés **RunStartInterval** et **UntilTime** représentent des heures locales ou des heures UTC.

<dt>

<span id="Local_Time"></span><span id="local_time"></span><span id="LOCAL_TIME"></span>

**Heure locale** (1)


</dt> <dd></dd> <dt>

<span id="UTC_Time"></span><span id="utc_time"></span><span id="UTC_TIME"></span>

**Heure UTC** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**Notifier**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Utilisateur à notifier lorsqu’un travail se termine ou échoue.

</dd> <dt>

**OtherRecoveryAction**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) («**\_ tâche CIM**.**RecoveryAction**")
</dt> </dl>

Chaîne qui décrit l’action de récupération lorsque la propriété **RecoveryAction** est **autre** (« 1 »).

</dd> <dt>

**Propriétaire**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OwningJobElement**](cim-owningjobelement.md).")
</dt> </dl>

L’utilisateur qui a envoyé le travail, ou le nom du service ou de la méthode qui a demandé le travail.

</dd> <dt>

**PercentComplete**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« percent »), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (101), **punitif** (« percent »)
</dt> </dl>

Pourcentage de la tâche qui est terminé.

> [!Note]  
> La valeur « 101 » n’est pas définie et ne sera pas autorisée dans la prochaine révision majeure de la spécification.

 

</dd> <dt>

**Priorité**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Importance du travail. Plus le numéro est faible, plus la priorité est élevée.

</dd> <dt>

**RecoveryAction**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) («**\_ tâche CIM**.**OtherRecoveryAction**")
</dt> </dl>

Décrit l’action de récupération à entreprendre en cas d’échec d’une tâche d’exécution.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)


</dt> <dd>

Il est inconnu de l’action de récupération à entreprendre.

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)


</dt> <dd>

L’action de récupération sera spécifiée dans la propriété **OtherRecoveryAction** .

</dd> <dt>

<span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>

<span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**Ne pas continuer** (2)


</dt> <dd>

Arrêtez l’exécution du travail et mettez à jour son état de manière appropriée.

</dd> <dt>

<span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>

<span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Continuer avec la tâche suivante** (3)


</dt> <dd>

Passez à la tâche suivante dans la file d’attente.

</dd> <dt>

<span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>

<span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Travail de réexécution** (4)


</dt> <dd>

La tâche doit être réexécutée.

</dd> <dt>

<span id="Run_Recovery_Job"></span><span id="run_recovery_job"></span><span id="RUN_RECOVERY_JOB"></span>

<span id="Run_Recovery_Job"></span><span id="run_recovery_job"></span><span id="RUN_RECOVERY_JOB"></span>**Exécuter la tâche de récupération** (5)


</dt> <dd>

Exécutez le travail associé à l’aide de la relation **RecoveryJob** . Notez que la tâche de récupération doit déjà se trouver dans la file d’attente à partir de laquelle elle sera exécutée.

</dd> </dl>

</dd> <dt>

**RunDay**
</dt> <dd> <dl> <dt>

Type de données : **sint8**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (-31), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (31), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ Job CIM**.**RunMonth**», «**\_ tâche CIM**.**RunDayOfWeek**», «**\_ tâche CIM**.**RunStartInterval**")
</dt> </dl>

Entier utilisé conjointement avec la propriété **RunDayOfWeek** pour indiquer le jour de traitement du travail ; ou, si **RunDayOfWeek** est défini sur zéro, **RunDay** indique le jour du mois où le travail est traité. Si **RunDay** est un entier négatif, il spécifie un jour relatif à la fin du mois, ou si **RunDay** est un entier positif, il spécifie un jour par rapport au début du mois.

</dd> <dt>

**RunDayOfWeek**
</dt> <dd> <dl> <dt>

Type de données : **sint8**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) («**\_ tâche CIM**.**RunMonth**», «**\_ tâche CIM**.**RunDay**», «**\_ tâche CIM**.**RunStartInterval**")
</dt> </dl>

Entier utilisé conjointement avec la propriété **RunDay** pour indiquer le jour de traitement du travail ; ou, si **RunDayOfWeek** est défini sur zéro, **RunDay** indique le jour du mois où le travail est traité.

<dt>

<span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>

**-Samedi** (-7)


</dt> <dd></dd> <dt>

<span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>

**-Vendredi** (-6)


</dt> <dd></dd> <dt>

<span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>

**-Jeudi** (-5)


</dt> <dd></dd> <dt>

<span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>

**-Mercredi** (-4)


</dt> <dd></dd> <dt>

<span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>

**-Mardi** (-3)


</dt> <dd></dd> <dt>

<span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>

**-Lundi** (-2)


</dt> <dd></dd> <dt>

<span id="-Sunday"></span><span id="-sunday"></span><span id="-SUNDAY"></span>

**-Dimanche** (-1)


</dt> <dd></dd> <dt>

<span id="ExactDayOfMonth"></span><span id="exactdayofmonth"></span><span id="EXACTDAYOFMONTH"></span>

**ExactDayOfMonth** (0)


</dt> <dd></dd> <dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>

**Dimanche** (1)


</dt> <dd></dd> <dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>

**Lundi** (2)


</dt> <dd></dd> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>

**Mardi** (3)


</dt> <dd></dd> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>

**Mercredi** (4)


</dt> <dd></dd> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>

**Jeudi** (5)


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

**Vendredi** (6)


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

**Samedi** (7)


</dt> <dd></dd> </dl>

</dd> <dt>

**RunMonth**
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) («**\_ tâche CIM**.**RunDay**», «**\_ tâche CIM**.**RunDayOfWeek**», «**\_ tâche CIM**.**RunStartInterval**")
</dt> </dl>

Mois de traitement du travail.

<dt>

<span id="January"></span><span id="january"></span><span id="JANUARY"></span>

**Janvier** (0)


</dt> <dd></dd> <dt>

<span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>

**Février** (1)


</dt> <dd></dd> <dt>

<span id="March"></span><span id="march"></span><span id="MARCH"></span>

**Mars** (2)


</dt> <dd></dd> <dt>

<span id="April"></span><span id="april"></span><span id="APRIL"></span>

**Avril** (3)


</dt> <dd></dd> <dt>

<span id="May"></span><span id="may"></span><span id="MAY"></span>

**Mai** (4)


</dt> <dd></dd> <dt>

<span id="June"></span><span id="june"></span><span id="JUNE"></span>

**Juin** (5)


</dt> <dd></dd> <dt>

<span id="July"></span><span id="july"></span><span id="JULY"></span>

**Juillet** (6)


</dt> <dd></dd> <dt>

<span id="August"></span><span id="august"></span><span id="AUGUST"></span>

**Août** (7)


</dt> <dd></dd> <dt>

<span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>

**Septembre** (8)


</dt> <dd></dd> <dt>

<span id="October"></span><span id="october"></span><span id="OCTOBER"></span>

**Octobre** (9)


</dt> <dd></dd> <dt>

<span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>

**Novembre** (10)


</dt> <dd></dd> <dt>

<span id="December"></span><span id="december"></span><span id="DECEMBER"></span>

**Décembre** (11)


</dt> <dd></dd> </dl>

</dd> <dt>

**RunStartInterval**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) («**\_ tâche CIM**.**RunMonth**», «**\_ tâche CIM**.**RunDay**», «**\_ tâche CIM**.**RunDayOfWeek**», «**\_ tâche CIM**.**RunStartInterval**")
</dt> </dl>

Intervalle de temps après minuit lorsque le travail est traité. Par exemple, « 00000000020000.000000:000 » indique que le travail est exécuté à l’heure ou après deux heures, heure locale ou heure UTC (UTC est spécifiée avec la propriété **LocalOrUtcTime** ).

</dd> <dt>

**ScheduledStartTime**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) («**\_ tâche CIM**.**RunMonth**», «**\_ tâche CIM**.**RunDay**», «**\_ tâche CIM**.**RunDayOfWeek**», «**\_ tâche CIM**.**RunStartInterval**")
</dt> </dl>

> [!Note]  
> Cette propriété est déconseillée. Au lieu de cela, nous vous recommandons d’utiliser les propriétés **RunMonth**, **RunDay**, **RunDayOfWeek** et **RunStartInterval** .

 

Heure à laquelle le travail en cours est planifié pour démarrer. Cette heure peut être représentée par une date et une heure ou par un intervalle relatif à l’heure à laquelle la propriété est demandée. La valeur zéro indique que le travail est déjà en cours d’exécution.

</dd> <dt>

**StartTime**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Heure à laquelle le travail a démarré. Cette heure peut être représentée par une date et une heure ou par un intervalle relatif à l’heure à laquelle la propriété est demandée.

</dd> <dt>

**TimeSubmitted**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Heure à laquelle le travail a été soumis. La valeur tous les zéros indique que l’élément parent n’est pas capable de signaler une date et une heure.

</dd> <dt>

**UntilTime**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) («**\_ tâche CIM**.**LocalOrUtcTime**")
</dt> </dl>

Heure après laquelle le travail devient non valide ou doit être arrêté. L’heure peut être représentée par une date et une heure ou par un intervalle relatif à l’heure à laquelle cette propriété est demandée. La valeur tous les neuf indique que le travail peut s’exécuter indéfiniment.

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

[**\_LOGICALELEMENT CIM**](cim-logicalelement.md)
</dt> </dl>

 

