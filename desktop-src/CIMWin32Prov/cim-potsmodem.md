---
description: La \_ classe CIM POTSModem représente un appareil qui convertit les données binaires en modulations d’onde pour une transmission basée sur le son en se connectant au réseau pots (Plain Old Telephone System).
ms.assetid: 2740f305-769d-464c-910a-998522f5121b
ms.tgt_platform: multiple
title: Classe CIM_POTSModem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_POTSModem
- CIM_POTSModem.AnswerMode
- CIM_POTSModem.Availability
- CIM_POTSModem.Caption
- CIM_POTSModem.CompressionInfo
- CIM_POTSModem.ConfigManagerErrorCode
- CIM_POTSModem.ConfigManagerUserConfig
- CIM_POTSModem.CountriesSupported
- CIM_POTSModem.CountrySelected
- CIM_POTSModem.CreationClassName
- CIM_POTSModem.CurrentPasswords
- CIM_POTSModem.Description
- CIM_POTSModem.DeviceID
- CIM_POTSModem.DialType
- CIM_POTSModem.ErrorCleared
- CIM_POTSModem.ErrorControlInfo
- CIM_POTSModem.ErrorDescription
- CIM_POTSModem.InactivityTimeout
- CIM_POTSModem.InstallDate
- CIM_POTSModem.LastErrorCode
- CIM_POTSModem.MaxBaudRateToPhone
- CIM_POTSModem.MaxBaudRateToSerialPort
- CIM_POTSModem.MaxNumberOfPasswords
- CIM_POTSModem.ModulationScheme
- CIM_POTSModem.Name
- CIM_POTSModem.PNPDeviceID
- CIM_POTSModem.PowerManagementCapabilities
- CIM_POTSModem.PowerManagementSupported
- CIM_POTSModem.RingsBeforeAnswer
- CIM_POTSModem.SpeakerVolumeInfo
- CIM_POTSModem.Status
- CIM_POTSModem.StatusInfo
- CIM_POTSModem.SupportsCallback
- CIM_POTSModem.SupportsSynchronousConnect
- CIM_POTSModem.SystemCreationClassName
- CIM_POTSModem.SystemName
- CIM_POTSModem.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d7fbaeedd1de4006dfdccbcec313a7428d7b7f03
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950683"
---
# <a name="cim_potsmodem-class"></a><span data-ttu-id="886e5-103">\_Classe CIM POTSModem</span><span class="sxs-lookup"><span data-stu-id="886e5-103">CIM\_POTSModem class</span></span>

<span data-ttu-id="886e5-104">La classe **CIM \_ POTSModem** représente un appareil qui convertit les données binaires en modulations d’onde pour une transmission basée sur le son en se connectant au réseau pots (Plain Old Telephone System).</span><span class="sxs-lookup"><span data-stu-id="886e5-104">The **CIM\_POTSModem** class represents a device that translates binary data into wave modulations for sound-based transmission by connecting to the Plain Old Telephone System (POTS) network.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="886e5-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="886e5-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="886e5-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="886e5-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="886e5-107">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="886e5-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="886e5-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="886e5-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="886e5-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="886e5-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C546-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_POTSModem : CIM_LogicalDevice
{
  uint16   AnswerMode;
  uint16   Availability;
  string   Caption;
  uint16   CompressionInfo;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CountriesSupported[];
  string   CountrySelected;
  string   CreationClassName;
  string   CurrentPasswords[];
  string   Description;
  string   DeviceID;
  uint16   DialType;
  boolean  ErrorCleared;
  uint16   ErrorControlInfo;
  string   ErrorDescription;
  uint32   InactivityTimeout;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint32   MaxBaudRateToPhone;
  uint32   MaxBaudRateToSerialPort;
  uint16   MaxNumberOfPasswords;
  uint16   ModulationScheme;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint8    RingsBeforeAnswer;
  uint16   SpeakerVolumeInfo;
  string   Status;
  uint16   StatusInfo;
  boolean  SupportsCallback;
  boolean  SupportsSynchronousConnect;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
};
```

## <a name="members"></a><span data-ttu-id="886e5-110">Membres</span><span class="sxs-lookup"><span data-stu-id="886e5-110">Members</span></span>

<span data-ttu-id="886e5-111">La classe **CIM \_ POTSModem** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="886e5-111">The **CIM\_POTSModem** class has these types of members:</span></span>

-   [<span data-ttu-id="886e5-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="886e5-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="886e5-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="886e5-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="886e5-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="886e5-114">Methods</span></span>

<span data-ttu-id="886e5-115">La classe **CIM \_ POTSModem** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="886e5-115">The **CIM\_POTSModem** class has these methods.</span></span>



| <span data-ttu-id="886e5-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="886e5-116">Method</span></span>                                                               | <span data-ttu-id="886e5-117">Description</span><span class="sxs-lookup"><span data-stu-id="886e5-117">Description</span></span>                                                                                                                              |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="886e5-118">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="886e5-118">**Reset**</span></span>](reset-method-in-class-cim-potsmodem.md)                 | <span data-ttu-id="886e5-119">Demande la réinitialisation de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="886e5-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="886e5-120">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="886e5-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="886e5-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="886e5-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-potsmodem.md) | <span data-ttu-id="886e5-122">Définit l’état d’alimentation souhaité pour un périphérique logique et lorsqu’un appareil doit être placé dans cet État.</span><span class="sxs-lookup"><span data-stu-id="886e5-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="886e5-123">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="886e5-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="886e5-124">Propriétés</span><span class="sxs-lookup"><span data-stu-id="886e5-124">Properties</span></span>

<span data-ttu-id="886e5-125">La classe **CIM \_ POTSModem** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="886e5-125">The **CIM\_POTSModem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="886e5-126">**AnswerMode**</span><span class="sxs-lookup"><span data-stu-id="886e5-126">**AnswerMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="886e5-127">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="886e5-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="886e5-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="886e5-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="886e5-129">La réponse automatique actuelle ou le paramètre de rappel pour le modem.</span><span class="sxs-lookup"><span data-stu-id="886e5-129">Current auto-answer or call-back setting for the modem.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="886e5-130">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="886e5-130">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="886e5-131">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="886e5-131">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="886e5-132">**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="886e5-132">**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Manual_Answer"></span><span id="manual_answer"></span><span id="MANUAL_ANSWER"></span>

<span data-ttu-id="886e5-133">**Réponse manuelle** (3)</span><span class="sxs-lookup"><span data-stu-id="886e5-133">**Manual Answer** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Auto_Answer"></span><span id="auto_answer"></span><span id="AUTO_ANSWER"></span>

<span data-ttu-id="886e5-134">**Réponse automatique** (4)</span><span class="sxs-lookup"><span data-stu-id="886e5-134">**Auto Answer** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Auto_Answer_with_Call-Back"></span><span id="auto_answer_with_call-back"></span><span id="AUTO_ANSWER_WITH_CALL-BACK"></span>

<span data-ttu-id="886e5-135">**Réponse automatique avec appel arrière** (5)</span><span class="sxs-lookup"><span data-stu-id="886e5-135">**Auto Answer with Call-Back** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="886e5-136">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="886e5-136">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="886e5-137">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="886e5-137">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="886e5-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="886e5-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="886e5-139">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="886e5-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="886e5-140">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="886e5-140">Availability and status of the device.</span></span>

<span data-ttu-id="886e5-141">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="886e5-141">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="886e5-142"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="886e5-142"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="886e5-143"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="886e5-143"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="886e5-144"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="886e5-144"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="886e5-145"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="886e5-145"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="886e5-146"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="886e5-146"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="886e5-147"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="886e5-147"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="886e5-148"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="886e5-148"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="886e5-149"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="886e5-149"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="886e5-150"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="886e5-150"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="886e5-151"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="886e5-151"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="886e5-152"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="886e5-152"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="886e5-153"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="886e5-153"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="886e5-154"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="886e5-154"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="886e5-155">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="886e5-155">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="886e5-156"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="886e5-156"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="886e5-157">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="886e5-157">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="886e5-158"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="886e5-158"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="886e5-159">L’appareil ne fonctionne pas, mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="886e5-159">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="886e5-160"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="886e5-160"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="886e5-161"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="886e5-161"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="886e5-162">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="886e5-162">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="886e5-163"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="886e5-163"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="886e5-164">L’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="886e5-164">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="886e5-165"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="886e5-165"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="886e5-166">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="886e5-166">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="886e5-167"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="886e5-167"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="886e5-168">L’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="886e5-168">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="886e5-169"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="886e5-169"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="886e5-170">L’appareil est calme.</span><span class="sxs-lookup"><span data-stu-id="886e5-170">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="886e5-171">**Caption**</span><span class="sxs-lookup"><span data-stu-id="886e5-171">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="886e5-172">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="886e5-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="886e5-173">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="886e5-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="886e5-174">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="886e5-174">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="886e5-175">Courte description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="886e5-175">Short textual description of the object.</span></span>

<span data-ttu-id="886e5-176">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="886e5-176">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="886e5-177">**CompressionInfo**</span><span class="sxs-lookup"><span data-stu-id="886e5-177">**CompressionInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="886e5-178">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="886e5-178">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="886e5-179">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="886e5-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="886e5-180">Caractéristiques de compression des données du modem.</span><span class="sxs-lookup"><span data-stu-id="886e5-180">Data compression characteristics of the modem.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="886e5-181">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="886e5-181">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="886e5-182">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="886e5-182">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Compression"></span><span id="no_compression"></span><span id="NO_COMPRESSION"></span>

<span data-ttu-id="886e5-183">**Aucune compression** (2)</span><span class="sxs-lookup"><span data-stu-id="886e5-183">**No Compression** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="MNP_5"></span><span id="mnp_5"></span>

<span data-ttu-id="886e5-184">**MNP 5** (3)</span><span class="sxs-lookup"><span data-stu-id="886e5-184">**MNP 5** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="V.42bis"></span><span id="v.42bis"></span><span id="V.42BIS"></span>

<span data-ttu-id="886e5-185">**V. 42bis** (4)</span><span class="sxs-lookup"><span data-stu-id="886e5-185">**V.42bis** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="886e5-186">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="886e5-186">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="886e5-187">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="886e5-187">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="886e5-188">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="886e5-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="886e5-189">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="886e5-189">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="886e5-190">Code d’erreur Configuration Manager Win32.</span><span class="sxs-lookup"><span data-stu-id="886e5-190">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="886e5-191">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="886e5-191">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="886e5-192"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="886e5-192"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="886e5-193"> (0)</span><span class="sxs-lookup"><span data-stu-id="886e5-193">(0)</span></span>


</dt> <dd>

<span data-ttu-id="886e5-194">L’appareil fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="886e5-194">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="886e5-195"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="886e5-195"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="886e5-196">(1)</span><span class="sxs-lookup"><span data-stu-id="886e5-196">(1)</span></span>


</dt> <dd>

<span data-ttu-id="886e5-197">L’appareil n’est pas configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="886e5-197">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="886e5-198"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="886e5-198"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="886e5-199">(2)</span><span class="sxs-lookup"><span data-stu-id="886e5-199">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="886e5-200"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="886e5-200"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="886e5-201">(3)</span><span class="sxs-lookup"><span data-stu-id="886e5-201">(3)</span></span>


</dt> <dd>

<span data-ttu-id="886e5-202">Le pilote de cet appareil est peut-être endommagé ou la mémoire ou d’autres ressources du système sont peut-être insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="886e5-202">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="886e5-203"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="886e5-203"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="886e5-204">(4)</span><span class="sxs-lookup"><span data-stu-id="886e5-204">(4)</span></span>


</dt> <dd>

<span data-ttu-id="886e5-205">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="886e5-205">Device is not working properly.</span></span> <span data-ttu-id="886e5-206">L’un de ses pilotes ou le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="886e5-206">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="886e5-207"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="886e5-207"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="886e5-208">(5)</span><span class="sxs-lookup"><span data-stu-id="886e5-208">(5)</span></span>


</dt> <dd>

<span data-ttu-id="886e5-209">Le pilote de l’appareil requiert une ressource que Windows ne peut pas gérer.</span><span class="sxs-lookup"><span data-stu-id="886e5-209">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="886e5-210"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="886e5-210"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="886e5-211"> (6)</span><span class="sxs-lookup"><span data-stu-id="886e5-211">(6)</span></span>


</dt> <dd>

<span data-ttu-id="886e5-212">La configuration de démarrage de l’appareil est en conflit avec d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="886e5-212">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="886e5-213"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="886e5-213"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="886e5-214">(7)</span><span class="sxs-lookup"><span data-stu-id="886e5-214">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="886e5-215"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="886e5-215"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="886e5-216">(8)</span><span class="sxs-lookup"><span data-stu-id="886e5-216">(8)</span></span>


</dt> <dd>

<span data-ttu-id="886e5-217">Le chargeur de pilote de l’appareil est manquant.</span><span class="sxs-lookup"><span data-stu-id="886e5-217">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="886e5-218"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="886e5-218"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="886e5-219">(9)</span><span class="sxs-lookup"><span data-stu-id="886e5-219">(9)</span></span>


</dt> <dd>

<span data-ttu-id="886e5-220">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="886e5-220">Device is not working properly.</span></span> <span data-ttu-id="886e5-221">Le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="886e5-221">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="886e5-222"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="886e5-222"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="886e5-223">(10)</span><span class="sxs-lookup"><span data-stu-id="886e5-223">(10)</span></span>


</dt> <dd>

<span data-ttu-id="886e5-224">Impossible de démarrer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="886e5-224">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="886e5-225"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="886e5-225"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="886e5-226">(11)</span><span class="sxs-lookup"><span data-stu-id="886e5-226">(11)</span></span>


</dt> <dd>

<span data-ttu-id="886e5-227">Échec de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="886e5-227">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="886e5-228"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="886e5-228"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="886e5-229">douze</span><span class="sxs-lookup"><span data-stu-id="886e5-229">(12)</span></span>


</dt> <dd>

<span data-ttu-id="886e5-230">L’appareil ne peut pas trouver suffisamment de ressources libres à utiliser.</span><span class="sxs-lookup"><span data-stu-id="886e5-230">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="886e5-231"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="886e5-231"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="886e5-232">(13)</span><span class="sxs-lookup"><span data-stu-id="886e5-232">(13)</span></span>


</dt> <dd>

<span data-ttu-id="886e5-233">Windows ne peut pas vérifier les ressources de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="886e5-233">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="886e5-234"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="886e5-234"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="886e5-235">(14)</span><span class="sxs-lookup"><span data-stu-id="886e5-235">(14)</span></span>


</dt> <dd>

<span data-ttu-id="886e5-236">L’appareil ne peut pas fonctionner correctement tant que l’ordinateur n’a pas redémarré.</span><span class="sxs-lookup"><span data-stu-id="886e5-236">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="886e5-237"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="886e5-237"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="886e5-238">(15)</span><span class="sxs-lookup"><span data-stu-id="886e5-238">(15)</span></span>


</dt> <dd>

<span data-ttu-id="886e5-239">L’appareil ne fonctionne pas correctement en raison d’un éventuel problème de réénumération.</span><span class="sxs-lookup"><span data-stu-id="886e5-239">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="886e5-240"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="886e5-240"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="886e5-241">(16)</span><span class="sxs-lookup"><span data-stu-id="886e5-241">(16)</span></span>


</dt> <dd>

<span data-ttu-id="886e5-242">Windows ne peut pas identifier toutes les ressources utilisées par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="886e5-242">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="886e5-243"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="886e5-243"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="886e5-244">(17)</span><span class="sxs-lookup"><span data-stu-id="886e5-244">(17)</span></span>


</dt> <dd>

<span data-ttu-id="886e5-245">L’appareil demande un type de ressource inconnu.</span><span class="sxs-lookup"><span data-stu-id="886e5-245">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="886e5-246"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="886e5-246"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="886e5-247">(18)</span><span class="sxs-lookup"><span data-stu-id="886e5-247">(18)</span></span>


</dt> <dd>

<span data-ttu-id="886e5-248">Les pilotes de périphérique doivent être réinstallés.</span><span class="sxs-lookup"><span data-stu-id="886e5-248">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="886e5-249"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="886e5-249"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="886e5-250">(19)</span><span class="sxs-lookup"><span data-stu-id="886e5-250">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="886e5-251"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="886e5-251"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="886e5-252">(20)</span><span class="sxs-lookup"><span data-stu-id="886e5-252">(20)</span></span>


</dt> <dd>

<span data-ttu-id="886e5-253">Le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="886e5-253">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="886e5-254"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="886e5-254"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="886e5-255">(21)</span><span class="sxs-lookup"><span data-stu-id="886e5-255">(21)</span></span>


</dt> <dd>

<span data-ttu-id="886e5-256">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="886e5-256">System failure.</span></span> <span data-ttu-id="886e5-257">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="886e5-257">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="886e5-258">Windows supprime l’appareil.</span><span class="sxs-lookup"><span data-stu-id="886e5-258">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="886e5-259"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="886e5-259"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="886e5-260">(22)</span><span class="sxs-lookup"><span data-stu-id="886e5-260">(22)</span></span>


</dt> <dd>

<span data-ttu-id="886e5-261">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="886e5-261">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="886e5-262"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="886e5-262"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="886e5-263">(23)</span><span class="sxs-lookup"><span data-stu-id="886e5-263">(23)</span></span>


</dt> <dd>

<span data-ttu-id="886e5-264">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="886e5-264">System failure.</span></span> <span data-ttu-id="886e5-265">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="886e5-265">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="886e5-266"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="886e5-266"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="886e5-267">(24)</span><span class="sxs-lookup"><span data-stu-id="886e5-267">(24)</span></span>


</dt> <dd>

<span data-ttu-id="886e5-268">L’appareil n’est pas présent, ne fonctionne pas correctement ou n’a pas tous ses pilotes installés.</span><span class="sxs-lookup"><span data-stu-id="886e5-268">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="886e5-269"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="886e5-269"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="886e5-270">(25)</span><span class="sxs-lookup"><span data-stu-id="886e5-270">(25)</span></span>


</dt> <dd>

<span data-ttu-id="886e5-271">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="886e5-271">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="886e5-272"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="886e5-272"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="886e5-273">(26)</span><span class="sxs-lookup"><span data-stu-id="886e5-273">(26)</span></span>


</dt> <dd>

<span data-ttu-id="886e5-274">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="886e5-274">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="886e5-275"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="886e5-275"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="886e5-276">(27)</span><span class="sxs-lookup"><span data-stu-id="886e5-276">(27)</span></span>


</dt> <dd>

<span data-ttu-id="886e5-277">L’appareil n’a pas une configuration de journal valide.</span><span class="sxs-lookup"><span data-stu-id="886e5-277">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="886e5-278"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="886e5-278"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="886e5-279">(28)</span><span class="sxs-lookup"><span data-stu-id="886e5-279">(28)</span></span>


</dt> <dd>

<span data-ttu-id="886e5-280">Les pilotes de périphérique ne sont pas installés.</span><span class="sxs-lookup"><span data-stu-id="886e5-280">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="886e5-281"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="886e5-281"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="886e5-282">(29)</span><span class="sxs-lookup"><span data-stu-id="886e5-282">(29)</span></span>


</dt> <dd>

<span data-ttu-id="886e5-283">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="886e5-283">Device is disabled.</span></span> <span data-ttu-id="886e5-284">Le microprogramme de l’appareil n’a pas fourni les ressources requises.</span><span class="sxs-lookup"><span data-stu-id="886e5-284">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="886e5-285"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="886e5-285"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="886e5-286">(30)</span><span class="sxs-lookup"><span data-stu-id="886e5-286">(30)</span></span>


</dt> <dd>

<span data-ttu-id="886e5-287">L’appareil utilise une ressource IRQ qu’un autre appareil utilise.</span><span class="sxs-lookup"><span data-stu-id="886e5-287">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="886e5-288"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="886e5-288"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="886e5-289">31</span><span class="sxs-lookup"><span data-stu-id="886e5-289">(31)</span></span>


</dt> <dd>

<span data-ttu-id="886e5-290">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="886e5-290">Device is not working properly.</span></span> <span data-ttu-id="886e5-291">Windows ne peut pas charger les pilotes de périphérique requis.</span><span class="sxs-lookup"><span data-stu-id="886e5-291">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="886e5-292">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="886e5-292">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="886e5-293">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="886e5-293">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="886e5-294">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="886e5-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="886e5-295">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="886e5-295">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="886e5-296">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="886e5-296">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="886e5-297">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="886e5-297">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="886e5-298">**CountriesSupported**</span><span class="sxs-lookup"><span data-stu-id="886e5-298">**CountriesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="886e5-299">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="886e5-299">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="886e5-300">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="886e5-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="886e5-301">Pays ou régions dans lesquels le modem peut fonctionner.</span><span class="sxs-lookup"><span data-stu-id="886e5-301">Countries or regions in which the modem can operate.</span></span>

</dd> <dt>

<span data-ttu-id="886e5-302">**CountrySelected**</span><span class="sxs-lookup"><span data-stu-id="886e5-302">**CountrySelected**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="886e5-303">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="886e5-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="886e5-304">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="886e5-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="886e5-305">Pays ou région pour lequel le modem est actuellement programmé.</span><span class="sxs-lookup"><span data-stu-id="886e5-305">Country or region for which the modem is currently programmed.</span></span> <span data-ttu-id="886e5-306">Lorsque plusieurs pays ou régions sont pris en charge, cette propriété définit celle qui est actuellement sélectionnée pour être utilisée.</span><span class="sxs-lookup"><span data-stu-id="886e5-306">When multiple countries or regions are supported, this property defines which one is currently selected for use.</span></span>

</dd> <dt>

<span data-ttu-id="886e5-307">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="886e5-307">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="886e5-308">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="886e5-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="886e5-309">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="886e5-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="886e5-310">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="886e5-310">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="886e5-311">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="886e5-311">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="886e5-312">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="886e5-312">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="886e5-313">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="886e5-313">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="886e5-314">**CurrentPasswords**</span><span class="sxs-lookup"><span data-stu-id="886e5-314">**CurrentPasswords**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="886e5-315">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="886e5-315">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="886e5-316">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="886e5-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="886e5-317">Mots de passe actuellement définis pour le modem.</span><span class="sxs-lookup"><span data-stu-id="886e5-317">Currently defined passwords for the modem.</span></span> <span data-ttu-id="886e5-318">Ce tableau peut être laissé vide pour des raisons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="886e5-318">This array can be left blank for security reasons.</span></span>

</dd> <dt>

<span data-ttu-id="886e5-319">**Description**</span><span class="sxs-lookup"><span data-stu-id="886e5-319">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="886e5-320">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="886e5-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="886e5-321">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="886e5-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="886e5-322">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="886e5-322">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="886e5-323">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="886e5-323">Textual description of the object.</span></span>

<span data-ttu-id="886e5-324">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="886e5-324">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="886e5-325">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="886e5-325">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="886e5-326">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="886e5-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="886e5-327">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="886e5-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="886e5-328">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="886e5-328">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="886e5-329">Adresse ou d’autres informations d’identification pour nommer de manière unique l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="886e5-329">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="886e5-330">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="886e5-330">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="886e5-331">**DialType**</span><span class="sxs-lookup"><span data-stu-id="886e5-331">**DialType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="886e5-332">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="886e5-332">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="886e5-333">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="886e5-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="886e5-334">Type de composition utilisé.</span><span class="sxs-lookup"><span data-stu-id="886e5-334">Type of dialing that is used.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="886e5-335">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="886e5-335">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Tone"></span><span id="tone"></span><span id="TONE"></span>

<span data-ttu-id="886e5-336">**Ton** (1)</span><span class="sxs-lookup"><span data-stu-id="886e5-336">**Tone** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Pulse"></span><span id="pulse"></span><span id="PULSE"></span>

<span data-ttu-id="886e5-337">**Impulsion** (2)</span><span class="sxs-lookup"><span data-stu-id="886e5-337">**Pulse** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="886e5-338">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="886e5-338">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="886e5-339">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="886e5-339">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="886e5-340">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="886e5-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="886e5-341">Si la **valeur est true**, l’erreur signalée dans la propriété **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="886e5-341">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="886e5-342">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="886e5-342">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="886e5-343">**ErrorControlInfo**</span><span class="sxs-lookup"><span data-stu-id="886e5-343">**ErrorControlInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="886e5-344">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="886e5-344">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="886e5-345">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="886e5-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="886e5-346">Caractéristiques de correction des erreurs du modem.</span><span class="sxs-lookup"><span data-stu-id="886e5-346">Error correction characteristics of the modem.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="886e5-347">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="886e5-347">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="886e5-348">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="886e5-348">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Error_Correction"></span><span id="no_error_correction"></span><span id="NO_ERROR_CORRECTION"></span>

<span data-ttu-id="886e5-349">**Aucune correction d’erreur** (2)</span><span class="sxs-lookup"><span data-stu-id="886e5-349">**No Error Correction** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="MNP_4"></span><span id="mnp_4"></span>

<span data-ttu-id="886e5-350">**MNP 4** (3)</span><span class="sxs-lookup"><span data-stu-id="886e5-350">**MNP 4** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="LAPM"></span><span id="lapm"></span>

<span data-ttu-id="886e5-351">**LAPM** (4)</span><span class="sxs-lookup"><span data-stu-id="886e5-351">**LAPM** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="886e5-352">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="886e5-352">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="886e5-353">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="886e5-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="886e5-354">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="886e5-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="886e5-355">Chaîne de forme libre qui fournit des informations sur l’erreur enregistrée dans la propriété **LastErrorCode** et les actions correctives à effectuer.</span><span class="sxs-lookup"><span data-stu-id="886e5-355">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="886e5-356">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="886e5-356">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="886e5-357">**InactivityTimeout**</span><span class="sxs-lookup"><span data-stu-id="886e5-357">**InactivityTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="886e5-358">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="886e5-358">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="886e5-359">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="886e5-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="886e5-360">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« secondes »)</span><span class="sxs-lookup"><span data-stu-id="886e5-360">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="886e5-361">Limite de temps (en secondes) pour la déconnexion automatique de la ligne téléphonique si aucune donnée n’est échangée.</span><span class="sxs-lookup"><span data-stu-id="886e5-361">Time limit (in seconds) for automatic disconnection of the phone line if no data is exchanged.</span></span> <span data-ttu-id="886e5-362">La valeur 0 (zéro) indique que cette fonctionnalité est présente mais pas activée.</span><span class="sxs-lookup"><span data-stu-id="886e5-362">A value of 0 (zero) indicates that this feature is present but not enabled.</span></span>

</dd> <dt>

<span data-ttu-id="886e5-363">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="886e5-363">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="886e5-364">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="886e5-364">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="886e5-365">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="886e5-365">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="886e5-366">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="886e5-366">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="886e5-367">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="886e5-367">Date and time the object was installed.</span></span> <span data-ttu-id="886e5-368">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="886e5-368">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="886e5-369">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="886e5-369">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="886e5-370">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="886e5-370">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="886e5-371">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="886e5-371">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="886e5-372">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="886e5-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="886e5-373">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="886e5-373">Last error code reported by the logical device.</span></span>

<span data-ttu-id="886e5-374">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="886e5-374">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="886e5-375">**MaxBaudRateToPhone**</span><span class="sxs-lookup"><span data-stu-id="886e5-375">**MaxBaudRateToPhone**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="886e5-376">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="886e5-376">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="886e5-377">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="886e5-377">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="886e5-378">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« bits par seconde »)</span><span class="sxs-lookup"><span data-stu-id="886e5-378">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="886e5-379">Vitesse maximale de communication définissable pour l’accès au système téléphonique.</span><span class="sxs-lookup"><span data-stu-id="886e5-379">Maximum settable communication speed for accessing the phone system.</span></span>

</dd> <dt>

<span data-ttu-id="886e5-380">**MaxBaudRateToSerialPort**</span><span class="sxs-lookup"><span data-stu-id="886e5-380">**MaxBaudRateToSerialPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="886e5-381">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="886e5-381">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="886e5-382">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="886e5-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="886e5-383">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« bits par seconde »)</span><span class="sxs-lookup"><span data-stu-id="886e5-383">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="886e5-384">Vitesse maximale de communication définissable au port COM pour un modem externe.</span><span class="sxs-lookup"><span data-stu-id="886e5-384">Maximum settable communication speed to the COM port for an external modem.</span></span> <span data-ttu-id="886e5-385">Entrez 0 (zéro) si ce n’est pas le cas.</span><span class="sxs-lookup"><span data-stu-id="886e5-385">Enter 0 (zero) if not applicable.</span></span>

</dd> <dt>

<span data-ttu-id="886e5-386">**MaxNumberOfPasswords**</span><span class="sxs-lookup"><span data-stu-id="886e5-386">**MaxNumberOfPasswords**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="886e5-387">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="886e5-387">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="886e5-388">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="886e5-388">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="886e5-389">Nombre maximal de mots de passe définissables dans le modem lui-même.</span><span class="sxs-lookup"><span data-stu-id="886e5-389">Maximum number of passwords definable in the modem itself.</span></span> <span data-ttu-id="886e5-390">Si cette fonctionnalité n’est pas prise en charge, entrez 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="886e5-390">If this feature is not supported, enter 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="886e5-391">**ModulationScheme**</span><span class="sxs-lookup"><span data-stu-id="886e5-391">**ModulationScheme**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="886e5-392">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="886e5-392">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="886e5-393">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="886e5-393">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="886e5-394">Schéma de modulation du modem.</span><span class="sxs-lookup"><span data-stu-id="886e5-394">Modulation scheme of the modem.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="886e5-395">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="886e5-395">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="886e5-396">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="886e5-396">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="886e5-397">**Non pris en charge** (2)</span><span class="sxs-lookup"><span data-stu-id="886e5-397">**Not Supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Bell_103"></span><span id="bell_103"></span><span id="BELL_103"></span>

<span data-ttu-id="886e5-398">**Cloche 103** (3)</span><span class="sxs-lookup"><span data-stu-id="886e5-398">**Bell 103** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bell_212A"></span><span id="bell_212a"></span><span id="BELL_212A"></span>

<span data-ttu-id="886e5-399">**Cloche 212A** (4)</span><span class="sxs-lookup"><span data-stu-id="886e5-399">**Bell 212A** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="V.22bis"></span><span id="v.22bis"></span><span id="V.22BIS"></span>

<span data-ttu-id="886e5-400">**V. 22bis** (5)</span><span class="sxs-lookup"><span data-stu-id="886e5-400">**V.22bis** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="V.32"></span><span id="v.32"></span>

<span data-ttu-id="886e5-401">**V. 32** (6)</span><span class="sxs-lookup"><span data-stu-id="886e5-401">**V.32** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="V.32bis"></span><span id="v.32bis"></span><span id="V.32BIS"></span>

<span data-ttu-id="886e5-402">**V. 32bis** (7)</span><span class="sxs-lookup"><span data-stu-id="886e5-402">**V.32bis** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="V.turbo"></span><span id="v.turbo"></span><span id="V.TURBO"></span>

<span data-ttu-id="886e5-403">**V. Turbo** (8)</span><span class="sxs-lookup"><span data-stu-id="886e5-403">**V.turbo** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="V.FC"></span><span id="v.fc"></span>

<span data-ttu-id="886e5-404">**V. FC** (9)</span><span class="sxs-lookup"><span data-stu-id="886e5-404">**V.FC** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="V.34"></span><span id="v.34"></span>

<span data-ttu-id="886e5-405">**V. 34** (10)</span><span class="sxs-lookup"><span data-stu-id="886e5-405">**V.34** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="V.34bis"></span><span id="v.34bis"></span><span id="V.34BIS"></span>

<span data-ttu-id="886e5-406">**V. 34bis** (11)</span><span class="sxs-lookup"><span data-stu-id="886e5-406">**V.34bis** (11)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="886e5-407">**Nom**</span><span class="sxs-lookup"><span data-stu-id="886e5-407">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="886e5-408">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="886e5-408">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="886e5-409">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="886e5-409">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="886e5-410">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="886e5-410">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="886e5-411">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="886e5-411">Label by which the object is known.</span></span> <span data-ttu-id="886e5-412">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="886e5-412">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="886e5-413">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="886e5-413">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="886e5-414">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="886e5-414">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="886e5-415">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="886e5-415">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="886e5-416">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="886e5-416">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="886e5-417">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="886e5-417">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="886e5-418">Win32 Plug-and-Play identificateur du périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="886e5-418">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="886e5-419">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="886e5-419">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="886e5-420">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="886e5-420">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="886e5-421">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="886e5-421">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="886e5-422">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="886e5-422">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="886e5-423">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="886e5-423">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="886e5-424">Tableau des fonctionnalités d’alimentation spécifiques d’un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="886e5-424">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="886e5-425">Cette propriété est héritée de **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="886e5-425">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="886e5-426"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="886e5-426"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="886e5-427"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="886e5-427"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="886e5-428"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="886e5-428"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="886e5-429"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="886e5-429"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="886e5-430">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="886e5-430">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="886e5-431"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="886e5-431"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="886e5-432">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="886e5-432">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="886e5-433"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="886e5-433"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="886e5-434">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="886e5-434">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="886e5-435">Cette méthode se trouve sur la classe parente du **\_ LogicalDevice CIM** et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="886e5-435">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="886e5-436">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="886e5-436">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="886e5-437"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="886e5-437"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="886e5-438">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation).</span><span class="sxs-lookup"><span data-stu-id="886e5-438">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="886e5-439"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="886e5-439"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="886e5-440">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation) et l' *heure* définie sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="886e5-440">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="886e5-441">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="886e5-441">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="886e5-442">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="886e5-442">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="886e5-443">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="886e5-443">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="886e5-444">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation, c’est-à-dire être mis en état d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="886e5-444">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="886e5-445">Si la valeur est **false**, la valeur entière 1 (« non pris en charge ») doit être la seule entrée dans le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="886e5-445">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="886e5-446">Cette propriété n’indique pas si les fonctionnalités de gestion de l’alimentation sont actuellement activées, ou si elles sont activées, quelles sont les fonctionnalités prises en charge.</span><span class="sxs-lookup"><span data-stu-id="886e5-446">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="886e5-447">Pour plus d’informations, consultez le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="886e5-447">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="886e5-448">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="886e5-448">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="886e5-449">**RingsBeforeAnswer**</span><span class="sxs-lookup"><span data-stu-id="886e5-449">**RingsBeforeAnswer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="886e5-450">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="886e5-450">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="886e5-451">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="886e5-451">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="886e5-452">Nombre d’anneaux avant que le modem ne réponde à un appel entrant.</span><span class="sxs-lookup"><span data-stu-id="886e5-452">Number of rings before the modem answers an incoming call.</span></span>

</dd> <dt>

<span data-ttu-id="886e5-453">**SpeakerVolumeInfo**</span><span class="sxs-lookup"><span data-stu-id="886e5-453">**SpeakerVolumeInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="886e5-454">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="886e5-454">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="886e5-455">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="886e5-455">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="886e5-456">Niveau de volume des tonalités audibles du modem.</span><span class="sxs-lookup"><span data-stu-id="886e5-456">Volume level of the audible tones from the modem.</span></span> <span data-ttu-id="886e5-457">Par exemple, un volume élevé, moyen ou faible peut être signalé.</span><span class="sxs-lookup"><span data-stu-id="886e5-457">For example, high, medium, or low volume can be reported.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="886e5-458">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="886e5-458">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="886e5-459">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="886e5-459">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="886e5-460">**Non pris en charge** (2)</span><span class="sxs-lookup"><span data-stu-id="886e5-460">**Not Supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span data-ttu-id="886e5-461">**Élevé** (3)</span><span class="sxs-lookup"><span data-stu-id="886e5-461">**High** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>

<span data-ttu-id="886e5-462">**Moyenne** (4)</span><span class="sxs-lookup"><span data-stu-id="886e5-462">**Medium** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="886e5-463">**Faible** (5)</span><span class="sxs-lookup"><span data-stu-id="886e5-463">**Low** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>

<span data-ttu-id="886e5-464">**Désactivé** (6)</span><span class="sxs-lookup"><span data-stu-id="886e5-464">**Off** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>

<span data-ttu-id="886e5-465">**Automatique** (7)</span><span class="sxs-lookup"><span data-stu-id="886e5-465">**Auto** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="886e5-466">**État**</span><span class="sxs-lookup"><span data-stu-id="886e5-466">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="886e5-467">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="886e5-467">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="886e5-468">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="886e5-468">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="886e5-469">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="886e5-469">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="886e5-470">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="886e5-470">Current status of the object.</span></span> <span data-ttu-id="886e5-471">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="886e5-471">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="886e5-472">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="886e5-472">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="886e5-473">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="886e5-473">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="886e5-474">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="886e5-474">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="886e5-475">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="886e5-475">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="886e5-476">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="886e5-476">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="886e5-477">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="886e5-477">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="886e5-478">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="886e5-478">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="886e5-479">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="886e5-479">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="886e5-480">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="886e5-480">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="886e5-481">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="886e5-481">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="886e5-482">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="886e5-482">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="886e5-483">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="886e5-483">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="886e5-484">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="886e5-484">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="886e5-485">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="886e5-485">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="886e5-486">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="886e5-486">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="886e5-487">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="886e5-487">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="886e5-488">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="886e5-488">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="886e5-489">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="886e5-489">State of the logical device.</span></span> <span data-ttu-id="886e5-490">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (non applicable) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="886e5-490">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="886e5-491">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="886e5-491">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="886e5-492">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="886e5-492">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="886e5-493">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="886e5-493">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="886e5-494">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="886e5-494">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="886e5-495">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="886e5-495">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="886e5-496">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="886e5-496">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="886e5-497">**SupportsCallback**</span><span class="sxs-lookup"><span data-stu-id="886e5-497">**SupportsCallback**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="886e5-498">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="886e5-498">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="886e5-499">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="886e5-499">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="886e5-500">Si la **valeur est true**, le modem prend en charge le rappel.</span><span class="sxs-lookup"><span data-stu-id="886e5-500">If **TRUE**, the modem supports call-back.</span></span>

</dd> <dt>

<span data-ttu-id="886e5-501">**SupportsSynchronousConnect**</span><span class="sxs-lookup"><span data-stu-id="886e5-501">**SupportsSynchronousConnect**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="886e5-502">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="886e5-502">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="886e5-503">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="886e5-503">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="886e5-504">Si la **valeur est true**, synchrone, et asynchrone, la communication est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="886e5-504">If **TRUE**, synchronous, as well as asynchronous, communication is supported.</span></span>

</dd> <dt>

<span data-ttu-id="886e5-505">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="886e5-505">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="886e5-506">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="886e5-506">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="886e5-507">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="886e5-507">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="886e5-508">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="886e5-508">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="886e5-509">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="886e5-509">Scoping system's creation class name.</span></span>

<span data-ttu-id="886e5-510">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="886e5-510">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="886e5-511">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="886e5-511">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="886e5-512">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="886e5-512">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="886e5-513">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="886e5-513">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="886e5-514">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="886e5-514">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="886e5-515">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="886e5-515">Scoping system's name.</span></span>

<span data-ttu-id="886e5-516">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="886e5-516">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="886e5-517">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="886e5-517">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="886e5-518">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="886e5-518">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="886e5-519">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="886e5-519">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="886e5-520">Date et heure de la dernière réinitialisation de ce contrôleur.</span><span class="sxs-lookup"><span data-stu-id="886e5-520">Date and time this controller was last reset.</span></span> <span data-ttu-id="886e5-521">Cela peut signifier que le contrôleur a été mis hors tension ou réinitialisé.</span><span class="sxs-lookup"><span data-stu-id="886e5-521">This could mean the controller was powered down, or reinitialized.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="886e5-522">Notes</span><span class="sxs-lookup"><span data-stu-id="886e5-522">Remarks</span></span>

<span data-ttu-id="886e5-523">La classe **CIM \_ POTSModem** est dérivée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="886e5-523">The **CIM\_POTSModem** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="886e5-524">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="886e5-524">WMI does not implement this class.</span></span> <span data-ttu-id="886e5-525">Pour les classes WMI dérivées de **CIM \_ POTSModem**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="886e5-525">For WMI classes derived from **CIM\_POTSModem**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="886e5-526">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="886e5-526">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="886e5-527">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="886e5-527">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="886e5-528">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="886e5-528">Requirements</span></span>



| <span data-ttu-id="886e5-529">Condition requise</span><span class="sxs-lookup"><span data-stu-id="886e5-529">Requirement</span></span> | <span data-ttu-id="886e5-530">Valeur</span><span class="sxs-lookup"><span data-stu-id="886e5-530">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="886e5-531">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="886e5-531">Minimum supported client</span></span><br/> | <span data-ttu-id="886e5-532">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="886e5-532">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="886e5-533">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="886e5-533">Minimum supported server</span></span><br/> | <span data-ttu-id="886e5-534">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="886e5-534">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="886e5-535">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="886e5-535">Namespace</span></span><br/>                | <span data-ttu-id="886e5-536">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="886e5-536">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="886e5-537">MOF</span><span class="sxs-lookup"><span data-stu-id="886e5-537">MOF</span></span><br/>                      | <dl> <span data-ttu-id="886e5-538"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="886e5-538"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="886e5-539">DLL</span><span class="sxs-lookup"><span data-stu-id="886e5-539">DLL</span></span><br/>                      | <dl> <span data-ttu-id="886e5-540"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="886e5-540"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="886e5-541">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="886e5-541">See also</span></span>

<dl> <dt>

[<span data-ttu-id="886e5-542">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="886e5-542">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

