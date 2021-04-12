---
description: Envoie un travail à un système d’exploitation pour une exécution à une date et une heure spécifiées à l’avenir.
ms.assetid: 9d582fbb-24cb-401d-8b77-af7671a24e6d
ms.tgt_platform: multiple
title: Créer une méthode de la classe Win32_ScheduledJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ScheduledJob.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9f1acae94ea29d2d57b2952c0b0adc267ad3066c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317917"
---
# <a name="create-method-of-the-win32_scheduledjob-class"></a>Créer une méthode de la \_ classe ScheduledJob Win32

La méthode **Create** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) soumet un travail à un système d’exploitation pour une exécution à une date et une heure spécifiées à l’avenir. Cette méthode nécessite que le service de planification soit démarré sur l’ordinateur sur lequel le travail est envoyé.

Cette rubrique utilise la syntaxe format MOF (MOF). Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntaxe


```mof
uint32 Create(
  [in]           string   Command,
  [in]           datetime StartTime,
  [in, optional] boolean  RunRepeatedly,
  [in, optional] uint32   DaysOfWeek,
  [in, optional] uint32   DaysOfMonth,
  [in, optional] boolean  InteractWithDesktop,
  [out]          uint32   JobId
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Commande* \[ dans\]
</dt> <dd>

Nom de la commande, du programme de traitement par lots ou du fichier binaire et des paramètres de ligne de commande que le service de planification utilise pour appeler le travail.

Exemple : « Defrag/q/f ».

</dd> <dt>

*StartTime* \[ dans\]
</dt> <dd>

Temps universel coordonné (UTC) pour exécuter un travail. Le formulaire doit être : «AAAAMMJJHHMMSS. MMMMMM (+-) OOO», où « AAAAMMJJ » doit être remplacé par « \* \* \* \* \* \* \* \* ». Par exemple : « \* \* \* \* \* \* \* \* 143000.000000-420 » spécifie 14,30 (2:30 P.M.) PST avec l’heure d’été en vigueur.

La section « (+-) OOO » de la valeur de la propriété StartTime est le décalage actuel pour la traduction de l’heure locale. Le biais correspond à la différence entre l’heure UTC et l’heure locale. Pour calculer le décalage pour votre fuseau horaire, multipliez le nombre d’heures d’avance ou de retard de l’heure de Greenwich (GMT) par 60 (utilisez un nombre positif comme nombre d’heures avant l’heure GMT et un nombre négatif si votre fuseau horaire est situé en arrière-plan GMT). Ajoutez un 60 supplémentaire à votre calcul si votre fuseau horaire utilise l’heure d’été. Par exemple, le fuseau horaire Pacifique est de huit heures après l’heure GMT. par conséquent, le décalage est égal à-420 (-8 \* 60 + 60) lorsque l’heure d’été est utilisée et-480 (-8 \* 60) lorsque l’heure d’été n’est pas utilisée. Vous pouvez également déterminer la valeur du décalage en interrogeant la propriété Bias de la classe [**Win32 \_ TimeZone**](win32-timezone.md) .

</dd> <dt>

*RunRepeatedly* \[ dans, facultatif\]
</dt> <dd>

Si la **valeur est true**, une tâche planifiée s’exécute de manière répétée sur des jours spécifiques. La valeur par défaut est **False**.

</dd> <dt>

*DaysOfWeek* \[ dans, facultatif\]
</dt> <dd>

Jours de la semaine où un travail est planifié pour s’exécuter ; utilisé uniquement lorsque le paramètre *RunRepeatedly* a la **valeur true**. Pour planifier un travail depuis plus d’un jour de la semaine, joignez les valeurs appropriées dans un ou logique. Par exemple, pour planifier un travail pour les mardis et les vendredis, la valeur de *DaysOfWeek* est 2 ou 16.

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


</dt> <dd></dd> </dl> </dd> <dt>

*DaysOfMonth* \[ dans, facultatif\]
</dt> <dd>

Jours du mois où un travail est planifié pour s’exécuter ; utilisé uniquement lorsque le paramètre *RunRepeatedly* a la **valeur true**.

<dt>

<span id="1"></span>

<span id="1"></span>**1** (1)


</dt> <dd>

Jour 1 d’un mois

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2** (2)


</dt> <dd>

Jour 2 du mois

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**3** (4)


</dt> <dd>

Jour 3 du mois

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**4** (8)


</dt> <dd>

Jour 4 d’un mois

</dd> <dt>

<span id="5"></span>

<span id="5"></span>**5** (16)


</dt> <dd>

Jour 5 du mois

</dd> <dt>

<span id="6"></span>

<span id="6"></span>**6** (32)


</dt> <dd>

Jour 6 du mois

</dd> <dt>

<span id="7"></span>

<span id="7"></span>**7** (64)


</dt> <dd>

Jour 7 du mois

</dd> <dt>

<span id="8"></span>

<span id="8"></span>**8** (128)


</dt> <dd>

Jour 8 d’un mois

</dd> <dt>

<span id="9"></span>

<span id="9"></span>**9** (256)


</dt> <dd>

Jour 9 du mois

</dd> <dt>

<span id="10"></span>

<span id="10"></span>**10** (512)


</dt> <dd>

Jour 10 d’un mois

</dd> <dt>

<span id="11"></span>

<span id="11"></span>**11** (1024)


</dt> <dd>

Jour 11 du mois

</dd> <dt>

<span id="12"></span>

<span id="12"></span>**12** (2048)


</dt> <dd>

Jour 12 du mois

</dd> <dt>

<span id="13"></span>

<span id="13"></span>**13** (4096)


</dt> <dd>

Jour 13 du mois

</dd> <dt>

<span id="14"></span>

<span id="14"></span>**14** (8192)


</dt> <dd>

Jour 14 du mois

</dd> <dt>

<span id="15"></span>

<span id="15"></span>**15** (16384)


</dt> <dd>

Jour 15 d’un mois

</dd> <dt>

<span id="16"></span>

<span id="16"></span>**16** (32768)


</dt> <dd>

Jour 16 du mois

</dd> <dt>

<span id="17"></span>

<span id="17"></span>**17** (65536)


</dt> <dd>

Jour 17 d’un mois

</dd> <dt>

<span id="18"></span>

<span id="18"></span>**18** (131072)


</dt> <dd>

Jour 18 du mois

</dd> <dt>

<span id="19"></span>

<span id="19"></span>**19** (262144)


</dt> <dd>

Jour 19 du mois

</dd> <dt>

<span id="20"></span>

<span id="20"></span>**20** (524288)


</dt> <dd>

Jour 20 du mois

</dd> <dt>

<span id="21"></span>

<span id="21"></span>**21** (1048576)


</dt> <dd>

Jour 21 du mois

</dd> <dt>

<span id="22"></span>

<span id="22"></span>**22** (2097152)


</dt> <dd>

Jour 22 du mois

</dd> <dt>

<span id="23"></span>

<span id="23"></span>**23** (4194304)


</dt> <dd>

Jour 23 du mois

</dd> <dt>

<span id="24"></span>

<span id="24"></span>**24** (8388608)


</dt> <dd>

Jour 24 du mois

</dd> <dt>

<span id="25"></span>

<span id="25"></span>**25** (16777216)


</dt> <dd>

Jour 25 du mois

</dd> <dt>

<span id="26"></span>

<span id="26"></span>**26** (33554432)


</dt> <dd>

Jour 26 du mois

</dd> <dt>

<span id="27"></span>

<span id="27"></span>**27** (67108864)


</dt> <dd>

Jour 27 du mois

</dd> <dt>

<span id="28"></span>

<span id="28"></span>**28** (134217728)


</dt> <dd>

Jour 28 du mois

</dd> <dt>

<span id="29"></span>

<span id="29"></span>**29** (268435456)


</dt> <dd>

Jour 29 du mois

</dd> <dt>

<span id="30"></span>

<span id="30"></span>**30** (536870912)


</dt> <dd>

Jour 30 du mois

</dd> <dt>

<span id="31"></span>

<span id="31"></span>**31** (1073741824)


</dt> <dd>

Jour 31 du mois

</dd> </dl> </dd> <dt>

*InteractWithDesktop* \[ dans, facultatif\]
</dt> <dd>

Si la **valeur est true**, le travail spécifié doit être interactif, ce qui signifie qu’un utilisateur peut fournir une entrée à une tâche planifiée pendant l’exécution du travail. La valeur par défaut est **False**.

</dd> <dt>

*JobID* \[ à\]
</dt> <dd>

Numéro d’identification d’un travail. Ce paramètre est un handle vers une tâche planifiée sur un ordinateur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la valeur 0 (zéro) en cas de réussite et un autre nombre pour indiquer une erreur. Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Opération réussie**
</dt> <dd>

0

La demande est acceptée.

</dd> <dt>

**Non pris en charge**
</dt> <dd>

1

La demande n'est pas prise en charge.

</dd> <dt>

**Accès refusé**
</dt> <dd>

2

L’utilisateur n’a pas l’accès nécessaire.

</dd> <dt>

**Échec inconnu**
</dt> <dd>

8

Processus interactif.

</dd> <dt>

**Chemin d'accès introuvable**
</dt> <dd>

9

Le chemin d’accès au répertoire du fichier exécutable du service est introuvable.

</dd> <dt>

**Paramètre non valide**
</dt> <dd>

21

Des paramètres non valides ont été transmis au service.

</dd> <dt>

**Service non démarré**
</dt> <dd>

22

Le compte sous lequel ce service s’exécute n’est pas valide ou ne dispose pas des autorisations nécessaires pour exécuter le service.

</dd> <dt>

**Autres**
</dt> <dd>

23 4294967295

</dd> </dl>

## <a name="remarks"></a>Notes

Si votre tâche planifiée démarre un programme interactif tel que le bloc-notes, la propriété **InteractWithDeskto** doit avoir la valeur **true** ou l’écran du programme n’est pas visible. Le processus apparaît toujours dans le **Gestionnaire des tâches** , même s’il n’apparaît pas à l’écran.

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

[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**\_ScheduledJob Win32**](win32-scheduledjob.md)
</dt> </dl>

 

