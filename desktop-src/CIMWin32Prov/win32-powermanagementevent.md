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
ms.openlocfilehash: e0e7dfa68646dbefb6d6b70218fe99830b44a0c1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110727"
---
# <a name="win32_powermanagementevent-class"></a><span data-ttu-id="23aca-103">\_Classe PowerManagementEvent Win32</span><span class="sxs-lookup"><span data-stu-id="23aca-103">Win32\_PowerManagementEvent class</span></span>

<span data-ttu-id="23aca-104">La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ PowerManagementEvent** WMI représente les événements de gestion de l’alimentation résultant des modifications de l’état d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="23aca-104">The **Win32\_PowerManagementEvent** [WMI class](../wmisdk/retrieving-a-class.md) represents power management events resulting from power state changes.</span></span> <span data-ttu-id="23aca-105">Ces modifications d’État sont associées à la gestion avancée de l’alimentation (APM) ou aux protocoles de gestion du système ACPI (Advanced Configuration and Power Interface).</span><span class="sxs-lookup"><span data-stu-id="23aca-105">These state changes are associated with either the Advanced Power Management (APM) or the Advanced Configuration and Power Interface (ACPI) system management protocols.</span></span>

<span data-ttu-id="23aca-106">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="23aca-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="23aca-107">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="23aca-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="23aca-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="23aca-108">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="23aca-109">Membres</span><span class="sxs-lookup"><span data-stu-id="23aca-109">Members</span></span>

<span data-ttu-id="23aca-110">La classe **Win32 \_ PowerManagementEvent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="23aca-110">The **Win32\_PowerManagementEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="23aca-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="23aca-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="23aca-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="23aca-112">Properties</span></span>

<span data-ttu-id="23aca-113">La classe **Win32 \_ PowerManagementEvent** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="23aca-113">The **Win32\_PowerManagementEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="23aca-114">**EventType**</span><span class="sxs-lookup"><span data-stu-id="23aca-114">**EventType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23aca-115">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23aca-115">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="23aca-116">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="23aca-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23aca-117">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("événements de gestion de l' \| alimentation win32api")</span><span class="sxs-lookup"><span data-stu-id="23aca-117">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Power Management Events")</span></span>
</dt> </dl>

<span data-ttu-id="23aca-118">Type de modification de l’état d’alimentation du système.</span><span class="sxs-lookup"><span data-stu-id="23aca-118">Type of change in the system power state.</span></span>

<dt>

<span id="Entering_Suspend"></span><span id="entering_suspend"></span><span id="ENTERING_SUSPEND"></span>

<span data-ttu-id="23aca-119"><span id="Entering_Suspend"></span><span id="entering_suspend"></span><span id="ENTERING_SUSPEND"></span>**Entrée de suspension** (4)</span><span class="sxs-lookup"><span data-stu-id="23aca-119"><span id="Entering_Suspend"></span><span id="entering_suspend"></span><span id="ENTERING_SUSPEND"></span>**Entering Suspend** (4)</span></span>


</dt> <dd>

<span data-ttu-id="23aca-120">Lorsqu’il est suspendu, l’ordinateur semble être désactivé. Toutefois, il peut être « réveillé » en réponse à différents événements, y compris l’entrée utilisateur (par exemple, le déplacement de la souris ou l’appui sur une touche du clavier).</span><span class="sxs-lookup"><span data-stu-id="23aca-120">While suspended, the computer appears to be off; however, it can be "awakened" in response to various events, including user input (such as moving the mouse or pressing a key on the keyboard).</span></span> <span data-ttu-id="23aca-121">Lorsque l’ordinateur est suspendu, la consommation d’énergie est réduite à l’un des différents niveaux en fonction de la façon dont le système doit être utilisé.</span><span class="sxs-lookup"><span data-stu-id="23aca-121">While the computer is suspended, power consumption is reduced to one of several levels depending on how the system is to be used.</span></span> <span data-ttu-id="23aca-122">Plus le niveau de consommation d’énergie est faible, plus il faut de temps au système pour revenir à l’état de travail.</span><span class="sxs-lookup"><span data-stu-id="23aca-122">The lower the level of power consumption, the more time it takes the system to return to the working state.</span></span> <span data-ttu-id="23aca-123">Lorsque l’ordinateur passe à l’état de suspension, le bureau est verrouillé et vous devez appuyer sur CTRL + ALT + SUPPR et fournir un nom d’utilisateur et un mot de passe valides pour reprendre les opérations.</span><span class="sxs-lookup"><span data-stu-id="23aca-123">When the computer enters the suspend state, the desktop is locked, and you must press CTRL+ALT+DELETE and provide a valid user name and password to resume operations</span></span>

</dd> <dt>

<span id="Resume_from_Suspend"></span><span id="resume_from_suspend"></span><span id="RESUME_FROM_SUSPEND"></span>

<span data-ttu-id="23aca-124"><span id="Resume_from_Suspend"></span><span id="resume_from_suspend"></span><span id="RESUME_FROM_SUSPEND"></span>**Reprendre à partir de l’interruption** (7)</span><span class="sxs-lookup"><span data-stu-id="23aca-124"><span id="Resume_from_Suspend"></span><span id="resume_from_suspend"></span><span id="RESUME_FROM_SUSPEND"></span>**Resume from Suspend** (7)</span></span>


</dt> <dd>

<span data-ttu-id="23aca-125">Indique qu’un message de reprise après interruption a été envoyé, permettant à l’ordinateur de revenir à son état d’alimentation normal.</span><span class="sxs-lookup"><span data-stu-id="23aca-125">Indicates that a Resume from Suspend message has been sent, enabling the computer to return to its regular power state.</span></span>

</dd> <dt>

<span id="Power_Status_Change"></span><span id="power_status_change"></span><span id="POWER_STATUS_CHANGE"></span>

<span data-ttu-id="23aca-126"><span id="Power_Status_Change"></span><span id="power_status_change"></span><span id="POWER_STATUS_CHANGE"></span>**Changement d’État** de l’alimentation (10)</span><span class="sxs-lookup"><span data-stu-id="23aca-126"><span id="Power_Status_Change"></span><span id="power_status_change"></span><span id="POWER_STATUS_CHANGE"></span>**Power Status Change** (10)</span></span>


</dt> <dd>

<span data-ttu-id="23aca-127">Indique une modification de l’état de l’alimentation de l’ordinateur, par exemple le passage de la batterie à l’alimentation secteur, ou l’alimentation secteur à un onduleur.</span><span class="sxs-lookup"><span data-stu-id="23aca-127">Indicates a change in the power status of the computer, such as a switch from battery power to AC, or from AC to an uninterruptible power supply.</span></span> <span data-ttu-id="23aca-128">Le système diffuse également cet événement lorsque la puissance de la batterie devient inférieure au seuil spécifié par l'utilisateur ou change selon un pourcentage spécifié.</span><span class="sxs-lookup"><span data-stu-id="23aca-128">The system also broadcasts this event when remaining battery power slips below the threshold specified by the user or if the battery power changes by a specified percentage.</span></span>

</dd> <dt>

<span id="OEM_Event"></span><span id="oem_event"></span><span id="OEM_EVENT"></span>

<span data-ttu-id="23aca-129"><span id="OEM_Event"></span><span id="oem_event"></span><span id="OEM_EVENT"></span>**Événement OEM** (11)</span><span class="sxs-lookup"><span data-stu-id="23aca-129"><span id="OEM_Event"></span><span id="oem_event"></span><span id="OEM_EVENT"></span>**OEM Event** (11)</span></span>


</dt> <dd>

<span data-ttu-id="23aca-130">Indique qu’un BIOS de gestion avancée de l’alimentation (APM) a envoyé un événement OEM.</span><span class="sxs-lookup"><span data-stu-id="23aca-130">Indicates that an Advanced Power Management (APM) BIOS has sent an OEM event.</span></span> <span data-ttu-id="23aca-131">La valeur de l’événement est capturée dans la propriété **OEMEventCode** .</span><span class="sxs-lookup"><span data-stu-id="23aca-131">The value of the event will be captured in the **OEMEventCode** property.</span></span> <span data-ttu-id="23aca-132">Étant donné que certaines implémentations du BIOS APM ne fournissent pas de notifications d’événements OEM, cet événement peut ne jamais être diffusé sur certains ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="23aca-132">Because some APM BIOS implementations do not provide OEM event notifications, this event might never be broadcast on some computers.</span></span> <span data-ttu-id="23aca-133">APM est un schéma de gestion de l’alimentation hérité.</span><span class="sxs-lookup"><span data-stu-id="23aca-133">APM is a legacy power management scheme.</span></span> <span data-ttu-id="23aca-134">Bien que toujours pris en charge, APM a été en grande partie remplacé par ACPI (Advanced Configuration and Power Interface).</span><span class="sxs-lookup"><span data-stu-id="23aca-134">Although still supported, APM has been largely superseded by ACPI (Advanced Configuration and Power Interface).</span></span>

</dd> <dt>

<span id="Resume_Automatic"></span><span id="resume_automatic"></span><span id="RESUME_AUTOMATIC"></span>

<span data-ttu-id="23aca-135"><span id="Resume_Automatic"></span><span id="resume_automatic"></span><span id="RESUME_AUTOMATIC"></span>**Reprendre automatiquement** (18)</span><span class="sxs-lookup"><span data-stu-id="23aca-135"><span id="Resume_Automatic"></span><span id="resume_automatic"></span><span id="RESUME_AUTOMATIC"></span>**Resume Automatic** (18)</span></span>


</dt> <dd>

<span data-ttu-id="23aca-136">Indique que l’ordinateur s’est réveillé en réponse à un événement.</span><span class="sxs-lookup"><span data-stu-id="23aca-136">Indicates that the computer has awakened in response to an event.</span></span> <span data-ttu-id="23aca-137">Si le système détecte une activité utilisateur (par exemple, un clic de souris), le message ResumeSuspend est diffusé, ce qui permet aux applications de savoir qu’ils peuvent reprendre l’interactivité totale avec l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="23aca-137">If the system detects user activity (such as a mouse click), the ResumeSuspend message will be broadcast, letting applications know that they can resume full interactivity with the user.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="23aca-138">**OEMEventCode**</span><span class="sxs-lookup"><span data-stu-id="23aca-138">**OEMEventCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23aca-139">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23aca-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="23aca-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="23aca-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23aca-141">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("événements de gestion de l' \| alimentation win32api")</span><span class="sxs-lookup"><span data-stu-id="23aca-141">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Power Management Events")</span></span>
</dt> </dl>

<span data-ttu-id="23aca-142">État de l’alimentation du système défini par le fabricant d’ordinateurs OEM lorsque la propriété **eventType** de cette classe est définie sur 11 (événement OEM); dans le cas contraire, cette propriété a la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="23aca-142">System power state defined by the original equipment manufacturer (OEM) when the **EventType** property of this class is set to 11 (OEM Event); otherwise, this property is set to **NULL**.</span></span> <span data-ttu-id="23aca-143">Les événements OEM sont générés lorsqu’un BIOS APM signale un événement OEM APM.</span><span class="sxs-lookup"><span data-stu-id="23aca-143">OEM events are generated when an APM BIOS signals an APM OEM event.</span></span> <span data-ttu-id="23aca-144">Les codes d’événement OEM se trouvent dans la plage 0x0200h-0x02FFh.</span><span class="sxs-lookup"><span data-stu-id="23aca-144">OEM event codes are in the range 0x0200h - 0x02FFh.</span></span>

</dd> <dt>

<span data-ttu-id="23aca-145">**descripteur de sécurité \_**</span><span class="sxs-lookup"><span data-stu-id="23aca-145">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23aca-146">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="23aca-146">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="23aca-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="23aca-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23aca-148">Descripteur utilisé par le fournisseur d’événements pour déterminer les utilisateurs qui peuvent recevoir l’événement.</span><span class="sxs-lookup"><span data-stu-id="23aca-148">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="23aca-149">Cette propriété est héritée de l' [**\_ \_ événement**](../wmisdk/--event.md).</span><span class="sxs-lookup"><span data-stu-id="23aca-149">This property is inherited from [**\_\_Event**](../wmisdk/--event.md).</span></span> <span data-ttu-id="23aca-150">Pour plus d’informations sur les constantes utilisées pour définir ce descripteur de sécurité, voir la rubrique sur les [constantes de sécurité WMI](../wmisdk/wmi-security-constants.md).</span><span class="sxs-lookup"><span data-stu-id="23aca-150">For more information about constants used to set this security descriptor, see [WMI Security Constants](../wmisdk/wmi-security-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="23aca-151">**HEURE de \_ création**</span><span class="sxs-lookup"><span data-stu-id="23aca-151">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23aca-152">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="23aca-152">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="23aca-153">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="23aca-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23aca-154">Valeur unique qui indique l’heure à laquelle l’événement a été généré.</span><span class="sxs-lookup"><span data-stu-id="23aca-154">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="23aca-155">Il s’agit d’une valeur 64 bits qui représente le nombre d’intervalles de 100 nanosecondes après le 1er janvier 1601.</span><span class="sxs-lookup"><span data-stu-id="23aca-155">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="23aca-156">Les informations sont au format de temps universel coordonné (UTC).</span><span class="sxs-lookup"><span data-stu-id="23aca-156">The information is in the Coordinated Universal Times (UTC) format.</span></span>

<span data-ttu-id="23aca-157">Cette propriété est héritée de l' [**\_ \_ événement**](../wmisdk/--event.md).</span><span class="sxs-lookup"><span data-stu-id="23aca-157">This property is inherited from [**\_\_Event**](../wmisdk/--event.md).</span></span>

<span data-ttu-id="23aca-158">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="23aca-158">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="23aca-159">Notes</span><span class="sxs-lookup"><span data-stu-id="23aca-159">Remarks</span></span>

<span data-ttu-id="23aca-160">La classe **Win32 \_ PowerManagementEvent** est dérivée de [**\_ \_ ExtrinsicEvent**](../wmisdk/--extrinsicevent.md).</span><span class="sxs-lookup"><span data-stu-id="23aca-160">The **Win32\_PowerManagementEvent** class is derived from [**\_\_ExtrinsicEvent**](../wmisdk/--extrinsicevent.md).</span></span>

<span data-ttu-id="23aca-161">Les modifications de l’état de l’alimentation indiquent souvent qu’un problème s’est produit avec un ordinateur ou un autre périphérique géré.</span><span class="sxs-lookup"><span data-stu-id="23aca-161">Changes in power status often indicate that a problem has occurred with a computer or with another managed device.</span></span> <span data-ttu-id="23aca-162">Si un serveur passe soudainement de l’alimentation secteur à un onduleur, cette modification peut indiquer qu’un problème électrique quelconque s’est produit, soit avec l’ordinateur lui-même, soit avec le système électrique de la pièce dans laquelle l’ordinateur est conservé.</span><span class="sxs-lookup"><span data-stu-id="23aca-162">If a server suddenly switches from AC power to an uninterruptible power supply, this change can indicate that an electrical problem of some kind has occurred, either with the computer itself or with the electrical system in the room in which the computer is kept.</span></span>

<span data-ttu-id="23aca-163">Les administrateurs doivent surveiller ces modifications dans l’état de l’alimentation et être immédiatement informés de ces modifications.</span><span class="sxs-lookup"><span data-stu-id="23aca-163">Administrators need to monitor these changes in power status and be notified of such changes immediately.</span></span> <span data-ttu-id="23aca-164">Cela leur permet d’agir avant que l’appareil ne perde de l’énergie entièrement.</span><span class="sxs-lookup"><span data-stu-id="23aca-164">This enables them to take action before the device loses power entirely.</span></span> <span data-ttu-id="23aca-165">(Par exemple, les systèmes d’alimentation sans coupure peuvent fonctionner pendant 15 minutes seulement, avant d’être arrêtés.)</span><span class="sxs-lookup"><span data-stu-id="23aca-165">(Uninterruptible power supply systems, for example, might run for only 15 minutes or so before shutting down.)</span></span>

<span data-ttu-id="23aca-166">La classe **Win32 \_ PowerManagementEvent** peut être utilisée pour surveiller les modifications de l’état d’alimentation sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="23aca-166">The **Win32\_PowerManagementEvent** class can be used to monitor changes in power status on a computer.</span></span> <span data-ttu-id="23aca-167">Ces modifications peuvent inclure un commutateur d’une source d’alimentation à une autre, ainsi qu’une modification de l’état de l’alimentation de l’ordinateur (par exemple, en entrant ou en quittant le mode de suspension).</span><span class="sxs-lookup"><span data-stu-id="23aca-167">These changes can include a switch from one power source to another as well as a change in computer power state (for example, entering or exiting Suspend mode).</span></span>

<span data-ttu-id="23aca-168">La classe **Win32 \_ PowerManagementEvent** a uniquement deux propriétés : EventType, utilisée pour indiquer le type d’événement de changement d’alimentation qui s’est produit, et OEMEventType, qui est utilisé par certains fabricants d’équipements d’origine pour définir des événements de changement d’alimentation supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="23aca-168">The **Win32\_PowerManagementEvent** class has only two properties: EventType, used to indicate the type of power change event that occurred, and OEMEventType, which is used by some original equipment manufacturers to define additional power change events.</span></span>

<span data-ttu-id="23aca-169">Pour plus d’informations sur la réponse aux événements d’alimentation Windows, consultez l’article [surveiller et répondre aux événements d’alimentation Windows avec PowerShell](https://blogs.technet.com/b/heyscriptingguy/archive/2011/08/16/monitor-and-respond-to-windows-power-events-with-powershell.aspx) sur la page Bonjour !</span><span class="sxs-lookup"><span data-stu-id="23aca-169">For more information on responding to Windows power events, see the [Monitor and Respond to Windows Power Events with PowerShell](https://blogs.technet.com/b/heyscriptingguy/archive/2011/08/16/monitor-and-respond-to-windows-power-events-with-powershell.aspx) article on the Hey!</span></span> <span data-ttu-id="23aca-170">Scripting Guy !</span><span class="sxs-lookup"><span data-stu-id="23aca-170">Scripting Guy!</span></span> <span data-ttu-id="23aca-171">.</span><span class="sxs-lookup"><span data-stu-id="23aca-171">blog.</span></span>

## <a name="examples"></a><span data-ttu-id="23aca-172">Exemples</span><span class="sxs-lookup"><span data-stu-id="23aca-172">Examples</span></span>

<span data-ttu-id="23aca-173">Le VBScript suivant surveille les modifications de l’état d’alimentation sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="23aca-173">The following VBScript monitors changes in power status on a computer.</span></span>


```VB
Set colMonitoredEvents = GetObject("winmgmts:")._
 ExecNotificationQuery("SELECT * FROM Win32_PowerManagementEvent")
Do
 Set strLatestEvent = colMonitoredEvents.NextEvent
 Wscript.Echo strLatestEvent.EventType
Loop
```



## <a name="requirements"></a><span data-ttu-id="23aca-174">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="23aca-174">Requirements</span></span>



| <span data-ttu-id="23aca-175">Condition requise</span><span class="sxs-lookup"><span data-stu-id="23aca-175">Requirement</span></span> | <span data-ttu-id="23aca-176">Valeur</span><span class="sxs-lookup"><span data-stu-id="23aca-176">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="23aca-177">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="23aca-177">Minimum supported client</span></span><br/> | <span data-ttu-id="23aca-178">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="23aca-178">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="23aca-179">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="23aca-179">Minimum supported server</span></span><br/> | <span data-ttu-id="23aca-180">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="23aca-180">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="23aca-181">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="23aca-181">Namespace</span></span><br/>                | <span data-ttu-id="23aca-182">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="23aca-182">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="23aca-183">MOF</span><span class="sxs-lookup"><span data-stu-id="23aca-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="23aca-184"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="23aca-184"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="23aca-185">DLL</span><span class="sxs-lookup"><span data-stu-id="23aca-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23aca-186"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23aca-186"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23aca-187">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="23aca-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23aca-188">**\_\_ExtrinsicEvent**</span><span class="sxs-lookup"><span data-stu-id="23aca-188">**\_\_ExtrinsicEvent**</span></span>](../wmisdk/--extrinsicevent.md)
</dt> <dt>

[<span data-ttu-id="23aca-189">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="23aca-189">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

<span data-ttu-id="23aca-190">[Surveillance des modifications de l’état d’alimentation de l’ordinateur](/previous-versions/tn-archive/ee176537(v=technet.10))</span><span class="sxs-lookup"><span data-stu-id="23aca-190">[Monitoring Changes in Computer Power Status](/previous-versions/tn-archive/ee176537(v=technet.10))</span></span>
</dt> </dl>

 

 
