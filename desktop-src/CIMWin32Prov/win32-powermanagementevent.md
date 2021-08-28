---
description: Le \_ PowerManagementEvent Win32 &\# 32 ; La classe WMI représente les événements de gestion de l’alimentation résultant des modifications de l’état d’alimentation.
ms.assetid: b5781805-87c7-4eaf-afbb-a1770fcff41c
ms.tgt_platform: multiple
title: Classe Win32_PowerManagementEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PowerManagementEvent
- Win32_PowerManagementEvent.SECURITY_DESCRIPTOR
- Win32_PowerManagementEvent.TIME_CREATED
- Win32_PowerManagementEvent.EventType
- Win32_PowerManagementEvent.OEMEventCode
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 536963be51d665b03af77bb81c7592b44d2a6eb5ddc449bfa82896dd7f7da9b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120064419"
---
# <a name="win32_powermanagementevent-class"></a>\_Classe PowerManagementEvent Win32

La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ PowerManagementEvent** WMI représente les événements de gestion de l’alimentation résultant des modifications de l’état d’alimentation. Ces modifications d’État sont associées à la gestion avancée de l’alimentation (APM) ou aux protocoles de gestion du système ACPI (Advanced Configuration and Power Interface).

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[UUID("{86460B6B-E709-11d2-B139-00105A1F77A1}"), AMENDMENT]
class Win32_PowerManagementEvent : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  uint16 EventType;
  uint16 OEMEventCode;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ PowerManagementEvent** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ PowerManagementEvent** a ces propriétés.

<dl> <dt>

**EventType**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("événements de gestion de l' \| alimentation win32api")
</dt> </dl>

Type de modification de l’état d’alimentation du système.

<dt>

<span id="Entering_Suspend"></span><span id="entering_suspend"></span><span id="ENTERING_SUSPEND"></span>

<span id="Entering_Suspend"></span><span id="entering_suspend"></span><span id="ENTERING_SUSPEND"></span>**Entrée de suspension** (4)


</dt> <dd>

Lorsqu’il est suspendu, l’ordinateur semble être désactivé. Toutefois, il peut être « réveillé » en réponse à différents événements, y compris l’entrée utilisateur (par exemple, le déplacement de la souris ou l’appui sur une touche du clavier). Lorsque l’ordinateur est suspendu, la consommation d’énergie est réduite à l’un des différents niveaux en fonction de la façon dont le système doit être utilisé. Plus le niveau de consommation d’énergie est faible, plus il faut de temps au système pour revenir à l’état de travail. Lorsque l’ordinateur passe à l’état de suspension, le bureau est verrouillé et vous devez appuyer sur CTRL + ALT + SUPPR et fournir un nom d’utilisateur et un mot de passe valides pour reprendre les opérations.

</dd> <dt>

<span id="Resume_from_Suspend"></span><span id="resume_from_suspend"></span><span id="RESUME_FROM_SUSPEND"></span>

<span id="Resume_from_Suspend"></span><span id="resume_from_suspend"></span><span id="RESUME_FROM_SUSPEND"></span>**Reprendre à partir de l’interruption** (7)


</dt> <dd>

Indique qu’un message de reprise après interruption a été envoyé, permettant à l’ordinateur de revenir à son état d’alimentation normal.

</dd> <dt>

<span id="Power_Status_Change"></span><span id="power_status_change"></span><span id="POWER_STATUS_CHANGE"></span>

<span id="Power_Status_Change"></span><span id="power_status_change"></span><span id="POWER_STATUS_CHANGE"></span>**Changement d’État** de l’alimentation (10)


</dt> <dd>

Indique une modification de l’état de l’alimentation de l’ordinateur, par exemple le passage de la batterie à l’alimentation secteur, ou l’alimentation secteur à un onduleur. Le système diffuse également cet événement lorsque la puissance de la batterie devient inférieure au seuil spécifié par l'utilisateur ou change selon un pourcentage spécifié.

</dd> <dt>

<span id="OEM_Event"></span><span id="oem_event"></span><span id="OEM_EVENT"></span>

<span id="OEM_Event"></span><span id="oem_event"></span><span id="OEM_EVENT"></span>**Événement OEM** (11)


</dt> <dd>

Indique qu’un BIOS de gestion avancée de l’alimentation (APM) a envoyé un événement OEM. La valeur de l’événement est capturée dans la propriété **OEMEventCode** . Étant donné que certaines implémentations du BIOS APM ne fournissent pas de notifications d’événements OEM, cet événement peut ne jamais être diffusé sur certains ordinateurs. APM est un schéma de gestion de l’alimentation hérité. Bien que toujours pris en charge, APM a été en grande partie remplacé par ACPI (Advanced Configuration and Power Interface).

</dd> <dt>

<span id="Resume_Automatic"></span><span id="resume_automatic"></span><span id="RESUME_AUTOMATIC"></span>

<span id="Resume_Automatic"></span><span id="resume_automatic"></span><span id="RESUME_AUTOMATIC"></span>**Reprendre automatiquement** (18)


</dt> <dd>

Indique que l’ordinateur s’est réveillé en réponse à un événement. Si le système détecte une activité utilisateur (par exemple, un clic de souris), le message ResumeSuspend est diffusé, ce qui permet aux applications de savoir qu’ils peuvent reprendre l’interactivité totale avec l’utilisateur.

</dd> </dl>

</dd> <dt>

**OEMEventCode**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("événements de gestion de l' \| alimentation win32api")
</dt> </dl>

État de l’alimentation du système défini par le fabricant d’ordinateurs OEM lorsque la propriété **eventType** de cette classe est définie sur 11 (événement OEM); dans le cas contraire, cette propriété a la valeur **null**. Les événements OEM sont générés lorsqu’un BIOS APM signale un événement OEM APM. Les codes d’événement OEM se trouvent dans la plage 0x0200h-0x02FFh.

</dd> <dt>

**descripteur de sécurité \_**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Descripteur utilisé par le fournisseur d’événements pour déterminer les utilisateurs qui peuvent recevoir l’événement. Cette propriété est héritée de l' [**\_ \_ événement**](../wmisdk/--event.md). Pour plus d’informations sur les constantes utilisées pour définir ce descripteur de sécurité, voir la rubrique sur les [constantes de sécurité WMI](../wmisdk/wmi-security-constants.md).

</dd> <dt>

**HEURE de \_ création**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Valeur unique qui indique l’heure à laquelle l’événement a été généré. Il s’agit d’une valeur 64 bits qui représente le nombre d’intervalles de 100 nanosecondes après le 1er janvier 1601. Les informations sont au format de temps universel coordonné (UTC).

Cette propriété est héritée de l' [**\_ \_ événement**](../wmisdk/--event.md).

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](../wmisdk/creating-a-wmi-script.md).

</dd> </dl>

## <a name="remarks"></a>Remarques

La classe **Win32 \_ PowerManagementEvent** est dérivée de [**\_ \_ ExtrinsicEvent**](../wmisdk/--extrinsicevent.md).

Les modifications de l’état de l’alimentation indiquent souvent qu’un problème s’est produit avec un ordinateur ou un autre périphérique géré. Si un serveur passe soudainement de l’alimentation secteur à un onduleur, cette modification peut indiquer qu’un problème électrique quelconque s’est produit, soit avec l’ordinateur lui-même, soit avec le système électrique de la pièce dans laquelle l’ordinateur est conservé.

Les administrateurs doivent surveiller ces modifications dans l’état de l’alimentation et être immédiatement informés de ces modifications. Cela leur permet d’agir avant que l’appareil ne perde de l’énergie entièrement. (Par exemple, les systèmes d’alimentation sans coupure peuvent fonctionner pendant 15 minutes seulement, avant d’être arrêtés.)

La classe **Win32 \_ PowerManagementEvent** peut être utilisée pour surveiller les modifications de l’état d’alimentation sur un ordinateur. Ces modifications peuvent inclure un commutateur d’une source d’alimentation à une autre, ainsi qu’une modification de l’état de l’alimentation de l’ordinateur (par exemple, en entrant ou en quittant le mode de suspension).

La classe **Win32 \_ PowerManagementEvent** a uniquement deux propriétés : EventType, utilisée pour indiquer le type d’événement de changement d’alimentation qui s’est produit, et OEMEventType, qui est utilisé par certains fabricants d’équipements d’origine pour définir des événements de changement d’alimentation supplémentaires.

pour plus d’informations sur la réponse aux événements d’alimentation Windows, consultez l’article [surveiller et répondre aux événements d’alimentation Windows avec PowerShell](https://blogs.technet.com/b/heyscriptingguy/archive/2011/08/16/monitor-and-respond-to-windows-power-events-with-powershell.aspx) sur la page bonjour ! Scripting Guy ! .

## <a name="examples"></a>Exemples

Le VBScript suivant surveille les modifications de l’état d’alimentation sur un ordinateur.


```VB
Set colMonitoredEvents = GetObject("winmgmts:")._
 ExecNotificationQuery("SELECT * FROM Win32_PowerManagementEvent")
Do
 Set strLatestEvent = colMonitoredEvents.NextEvent
 Wscript.Echo strLatestEvent.EventType
Loop
```



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

[**\_\_ExtrinsicEvent**](../wmisdk/--extrinsicevent.md)
</dt> <dt>

[Classes matérielles du système informatique](computer-system-hardware-classes.md)
</dt> <dt>

[Surveillance des modifications de l’état d’alimentation de l’ordinateur](/previous-versions/tn-archive/ee176537(v=technet.10))
</dt> </dl>

 

 
