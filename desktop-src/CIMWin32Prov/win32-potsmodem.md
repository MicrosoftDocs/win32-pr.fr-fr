---
description: La \_ classe WMI POTSModem WMI représente les services et les caractéristiques d’un modem pots (Plain Old Telephone Service) sur un système informatique exécutant Windows.
ms.assetid: 24589942-e2c3-477e-8179-59ae4a4aa85a
ms.tgt_platform: multiple
title: Win32_POTSModem, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_POTSModem
- Win32_POTSModem.Reset
- Win32_POTSModem.SetPowerState
- Win32_POTSModem.AnswerMode
- Win32_POTSModem.AttachedTo
- Win32_POTSModem.Availability
- Win32_POTSModem.BlindOff
- Win32_POTSModem.BlindOn
- Win32_POTSModem.Caption
- Win32_POTSModem.CompatibilityFlags
- Win32_POTSModem.CompressionInfo
- Win32_POTSModem.CompressionOff
- Win32_POTSModem.CompressionOn
- Win32_POTSModem.ConfigManagerErrorCode
- Win32_POTSModem.ConfigManagerUserConfig
- Win32_POTSModem.ConfigurationDialog
- Win32_POTSModem.CountriesSupported
- Win32_POTSModem.CountrySelected
- Win32_POTSModem.CreationClassName
- Win32_POTSModem.CurrentPasswords
- Win32_POTSModem.DCB
- Win32_POTSModem.Default
- Win32_POTSModem.Description
- Win32_POTSModem.DeviceID
- Win32_POTSModem.DeviceLoader
- Win32_POTSModem.DeviceType
- Win32_POTSModem.DialType
- Win32_POTSModem.DriverDate
- Win32_POTSModem.ErrorCleared
- Win32_POTSModem.ErrorControlForced
- Win32_POTSModem.ErrorControlInfo
- Win32_POTSModem.ErrorControlOff
- Win32_POTSModem.ErrorControlOn
- Win32_POTSModem.ErrorDescription
- Win32_POTSModem.FlowControlHard
- Win32_POTSModem.FlowControlOff
- Win32_POTSModem.FlowControlSoft
- Win32_POTSModem.InactivityScale
- Win32_POTSModem.InactivityTimeout
- Win32_POTSModem.Index
- Win32_POTSModem.IndexEx
- Win32_POTSModem.InstallDate
- Win32_POTSModem.LastErrorCode
- Win32_POTSModem.MaxBaudRateToPhone
- Win32_POTSModem.MaxBaudRateToSerialPort
- Win32_POTSModem.MaxNumberOfPasswords
- Win32_POTSModem.Model
- Win32_POTSModem.ModemInfPath
- Win32_POTSModem.ModemInfSection
- Win32_POTSModem.ModulationBell
- Win32_POTSModem.ModulationCCITT
- Win32_POTSModem.ModulationScheme
- Win32_POTSModem.Name
- Win32_POTSModem.PNPDeviceID
- Win32_POTSModem.PortSubClass
- Win32_POTSModem.PowerManagementCapabilities
- Win32_POTSModem.PowerManagementSupported
- Win32_POTSModem.Prefix
- Win32_POTSModem.Properties
- Win32_POTSModem.ProviderName
- Win32_POTSModem.Pulse
- Win32_POTSModem.Reset
- Win32_POTSModem.ResponsesKeyName
- Win32_POTSModem.RingsBeforeAnswer
- Win32_POTSModem.SpeakerModeDial
- Win32_POTSModem.SpeakerModeOff
- Win32_POTSModem.SpeakerModeOn
- Win32_POTSModem.SpeakerModeSetup
- Win32_POTSModem.SpeakerVolumeHigh
- Win32_POTSModem.SpeakerVolumeInfo
- Win32_POTSModem.SpeakerVolumeLow
- Win32_POTSModem.SpeakerVolumeMed
- Win32_POTSModem.Status
- Win32_POTSModem.StatusInfo
- Win32_POTSModem.StringFormat
- Win32_POTSModem.SupportsCallback
- Win32_POTSModem.SupportsSynchronousConnect
- Win32_POTSModem.SystemCreationClassName
- Win32_POTSModem.SystemName
- Win32_POTSModem.Terminator
- Win32_POTSModem.TimeOfLastReset
- Win32_POTSModem.Tone
- Win32_POTSModem.VoiceSwitchFeature
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6ec9634c5ee86d6819bf8f7a45dd521276565903
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861182"
---
# <a name="win32_potsmodem-class"></a><span data-ttu-id="89049-103">\_Classe POTSModem Win32</span><span class="sxs-lookup"><span data-stu-id="89049-103">Win32\_POTSModem class</span></span>

<span data-ttu-id="89049-104">La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ POTSModem** WMI représente les services et les caractéristiques d’un modem pots (Plain Old Telephone Service) sur un système informatique exécutant Windows.</span><span class="sxs-lookup"><span data-stu-id="89049-104">The **Win32\_POTSModem** [WMI class](../wmisdk/retrieving-a-class.md) represents the services and characteristics of a Plain Old Telephone Service (POTS) modem on a computer system running Windows.</span></span>

<span data-ttu-id="89049-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="89049-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="89049-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="89049-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="89049-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="89049-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4BE-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_POTSModem : CIM_PotsModem
{
  uint16   AnswerMode;
  string   AttachedTo;
  uint16   Availability;
  string   BlindOff;
  string   BlindOn;
  string   Caption;
  string   CompatibilityFlags;
  uint16   CompressionInfo;
  string   CompressionOff;
  string   CompressionOn;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   ConfigurationDialog;
  string   CountriesSupported[];
  string   CountrySelected;
  string   CreationClassName;
  string   CurrentPasswords[];
  uint8    DCB[];
  uint8    Default[];
  string   Description;
  string   DeviceID;
  string   DeviceLoader;
  string   DeviceType;
  uint16   DialType;
  datetime DriverDate;
  boolean  ErrorCleared;
  string   ErrorControlForced;
  uint16   ErrorControlInfo;
  string   ErrorControlOff;
  string   ErrorControlOn;
  string   ErrorDescription;
  string   FlowControlHard;
  string   FlowControlOff;
  string   FlowControlSoft;
  string   InactivityScale;
  uint32   InactivityTimeout;
  uint32   Index;
  string   IndexEx;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint32   MaxBaudRateToPhone;
  uint32   MaxBaudRateToSerialPort;
  uint16   MaxNumberOfPasswords;
  string   Model;
  string   ModemInfPath;
  string   ModemInfSection;
  string   ModulationBell;
  string   ModulationCCITT;
  uint16   ModulationScheme;
  string   Name;
  string   PNPDeviceID;
  string   PortSubClass;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Prefix;
  uint8    Properties[];
  string   ProviderName;
  string   Pulse;
  string   Reset;
  string   ResponsesKeyName;
  uint8    RingsBeforeAnswer;
  string   SpeakerModeDial;
  string   SpeakerModeOff;
  string   SpeakerModeOn;
  string   SpeakerModeSetup;
  string   SpeakerVolumeHigh;
  uint16   SpeakerVolumeInfo;
  string   SpeakerVolumeLow;
  string   SpeakerVolumeMed;
  string   Status;
  uint16   StatusInfo;
  string   StringFormat;
  boolean  SupportsCallback;
  boolean  SupportsSynchronousConnect;
  string   SystemCreationClassName;
  string   SystemName;
  string   Terminator;
  datetime TimeOfLastReset;
  string   Tone;
  string   VoiceSwitchFeature;
};
```

## <a name="members"></a><span data-ttu-id="89049-108">Membres</span><span class="sxs-lookup"><span data-stu-id="89049-108">Members</span></span>

<span data-ttu-id="89049-109">La classe **Win32 \_ POTSModem** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="89049-109">The **Win32\_POTSModem** class has these types of members:</span></span>

-   [<span data-ttu-id="89049-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="89049-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="89049-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="89049-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="89049-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="89049-112">Methods</span></span>

<span data-ttu-id="89049-113">La classe **Win32 \_ POTSModem** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="89049-113">The **Win32\_POTSModem** class has these methods.</span></span>



| <span data-ttu-id="89049-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="89049-114">Method</span></span>            | <span data-ttu-id="89049-115">Description</span><span class="sxs-lookup"><span data-stu-id="89049-115">Description</span></span>                                                                                                                                                                            |
|:------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89049-116">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="89049-116">**Reset**</span></span>         | <span data-ttu-id="89049-117">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="89049-117">Not implemented.</span></span> <span data-ttu-id="89049-118">Pour implémenter cette méthode, consultez la méthode [**Reset**](reset-method-in-class-cim-controller.md) dans [**CIM \_ PotsModem**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="89049-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_PotsModem**](cim-potsmodem.md).</span></span><br/>                 |
| <span data-ttu-id="89049-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="89049-119">**SetPowerState**</span></span> | <span data-ttu-id="89049-120">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="89049-120">Not implemented.</span></span> <span data-ttu-id="89049-121">Pour implémenter cette méthode, consultez la méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) dans [**CIM \_ PotsModem**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="89049-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_PotsModem**](cim-potsmodem.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="89049-122">Propriétés</span><span class="sxs-lookup"><span data-stu-id="89049-122">Properties</span></span>

<span data-ttu-id="89049-123">La classe **Win32 \_ POTSModem** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="89049-123">The **Win32\_POTSModem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="89049-124">**AnswerMode**</span><span class="sxs-lookup"><span data-stu-id="89049-124">**AnswerMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-125">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="89049-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="89049-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89049-127">Paramètre de rappel ou de réponse automatique actuel pour le modem.</span><span class="sxs-lookup"><span data-stu-id="89049-127">Current auto-answer or callback setting for the modem.</span></span>

<span data-ttu-id="89049-128">Cette propriété est héritée de la [**\_ PotsModem CIM**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="89049-128">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="89049-129">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="89049-129">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="89049-130">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="89049-130">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="89049-131">**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="89049-131">**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Manual_Answer"></span><span id="manual_answer"></span><span id="MANUAL_ANSWER"></span>

<span data-ttu-id="89049-132">**Réponse manuelle** (3)</span><span class="sxs-lookup"><span data-stu-id="89049-132">**Manual Answer** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Auto_Answer"></span><span id="auto_answer"></span><span id="AUTO_ANSWER"></span>

<span data-ttu-id="89049-133">**Réponse automatique** (4)</span><span class="sxs-lookup"><span data-stu-id="89049-133">**Auto Answer** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Auto_Answer_with_Call-Back"></span><span id="auto_answer_with_call-back"></span><span id="AUTO_ANSWER_WITH_CALL-BACK"></span>

<span data-ttu-id="89049-134">**Réponse automatique avec appel arrière** (5)</span><span class="sxs-lookup"><span data-stu-id="89049-134">**Auto Answer with Call-Back** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="89049-135">**AttachedTo**</span><span class="sxs-lookup"><span data-stu-id="89049-135">**AttachedTo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-136">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="89049-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89049-137">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89049-138">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| AttachedTo")</span><span class="sxs-lookup"><span data-stu-id="89049-138">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|AttachedTo")</span></span>
</dt> </dl>

<span data-ttu-id="89049-139">Port auquel le modem POTS est attaché.</span><span class="sxs-lookup"><span data-stu-id="89049-139">Port to which the POTS modem is attached.</span></span>

<span data-ttu-id="89049-140">Exemple : « COM1 »</span><span class="sxs-lookup"><span data-stu-id="89049-140">Example: "COM1"</span></span>

</dd> <dt>

<span data-ttu-id="89049-141">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="89049-141">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-142">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="89049-142">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="89049-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89049-144">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="89049-144">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="89049-145">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="89049-145">Availability and status of the device.</span></span>

<span data-ttu-id="89049-146">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="89049-146">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="89049-147"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="89049-147"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="89049-148"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="89049-148"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="89049-149"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="89049-149"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="89049-150">En cours d’exécution ou pleine puissance</span><span class="sxs-lookup"><span data-stu-id="89049-150">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="89049-151"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="89049-151"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="89049-152"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="89049-152"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="89049-153"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="89049-153"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="89049-154"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="89049-154"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="89049-155"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="89049-155"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="89049-156"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="89049-156"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="89049-157"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="89049-157"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="89049-158"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="89049-158"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="89049-159"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="89049-159"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="89049-160"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="89049-160"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="89049-161">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="89049-161">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="89049-162"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="89049-162"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="89049-163">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="89049-163">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="89049-164"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="89049-164"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="89049-165">L’appareil ne fonctionne pas, mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="89049-165">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="89049-166"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="89049-166"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="89049-167"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="89049-167"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="89049-168">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="89049-168">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="89049-169"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="89049-169"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="89049-170">L’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="89049-170">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="89049-171"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="89049-171"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="89049-172">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="89049-172">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="89049-173"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="89049-173"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="89049-174">L’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="89049-174">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="89049-175"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="89049-175"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="89049-176">L’appareil est calme.</span><span class="sxs-lookup"><span data-stu-id="89049-176">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="89049-177">**BlindOff**</span><span class="sxs-lookup"><span data-stu-id="89049-177">**BlindOff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-178">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="89049-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89049-179">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89049-180">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| BlindOff")</span><span class="sxs-lookup"><span data-stu-id="89049-180">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|BlindOff")</span></span>
</dt> </dl>

<span data-ttu-id="89049-181">Chaîne de commande utilisée pour détecter une tonalité avant la numérotation.</span><span class="sxs-lookup"><span data-stu-id="89049-181">Command string used to detect a dial tone before dialing.</span></span>

<span data-ttu-id="89049-182">Exemple : « X4 »</span><span class="sxs-lookup"><span data-stu-id="89049-182">Example: "X4"</span></span>

</dd> <dt>

<span data-ttu-id="89049-183">**BlindOn**</span><span class="sxs-lookup"><span data-stu-id="89049-183">**BlindOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-184">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="89049-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89049-185">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89049-186">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| BlindOn")</span><span class="sxs-lookup"><span data-stu-id="89049-186">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|BlindOn")</span></span>
</dt> </dl>

<span data-ttu-id="89049-187">Chaîne de commande utilisée pour indiquer si une tonalité est ou non.</span><span class="sxs-lookup"><span data-stu-id="89049-187">Command string used to dial whether or not there is a dial tone.</span></span>

<span data-ttu-id="89049-188">Exemple : « x3 »</span><span class="sxs-lookup"><span data-stu-id="89049-188">Example: "X3"</span></span>

</dd> <dt>

<span data-ttu-id="89049-189">**Caption**</span><span class="sxs-lookup"><span data-stu-id="89049-189">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-190">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="89049-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89049-191">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89049-192">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="89049-192">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="89049-193">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="89049-193">Short description of the object.</span></span>

<span data-ttu-id="89049-194">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="89049-194">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="89049-195">**CompatibilityFlags**</span><span class="sxs-lookup"><span data-stu-id="89049-195">**CompatibilityFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-196">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="89049-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89049-197">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89049-198">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| CompatibilityFlags")</span><span class="sxs-lookup"><span data-stu-id="89049-198">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|CompatibilityFlags")</span></span>
</dt> </dl>

<span data-ttu-id="89049-199">Tous les protocoles de connexion par modem avec lesquels ce périphérique modem est compatible.</span><span class="sxs-lookup"><span data-stu-id="89049-199">All modem connection protocols with which this modem device is compatible.</span></span>

</dd> <dt>

<span data-ttu-id="89049-200">**CompressionInfo**</span><span class="sxs-lookup"><span data-stu-id="89049-200">**CompressionInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-201">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="89049-201">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="89049-202">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89049-203">Caractéristiques de compression des données du modem.</span><span class="sxs-lookup"><span data-stu-id="89049-203">Data compression characteristics of the modem.</span></span>

<span data-ttu-id="89049-204">Cette propriété est héritée de la [**\_ PotsModem CIM**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="89049-204">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="89049-205"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="89049-205"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="89049-206"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="89049-206"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="89049-207">Unknown</span><span class="sxs-lookup"><span data-stu-id="89049-207">Unknown</span></span>

</dd> <dt>

<span id="No_Compression"></span><span id="no_compression"></span><span id="NO_COMPRESSION"></span>

<span data-ttu-id="89049-208"><span id="No_Compression"></span><span id="no_compression"></span><span id="NO_COMPRESSION"></span>**Aucune compression** (2)</span><span class="sxs-lookup"><span data-stu-id="89049-208"><span id="No_Compression"></span><span id="no_compression"></span><span id="NO_COMPRESSION"></span>**No Compression** (2)</span></span>


</dt> <dd>

<span data-ttu-id="89049-209">Autres</span><span class="sxs-lookup"><span data-stu-id="89049-209">Other</span></span>

</dd> <dt>

<span id="MNP_5"></span><span id="mnp_5"></span>

<span data-ttu-id="89049-210"><span id="MNP_5"></span><span id="mnp_5"></span>**MNP 5** (3)</span><span class="sxs-lookup"><span data-stu-id="89049-210"><span id="MNP_5"></span><span id="mnp_5"></span>**MNP 5** (3)</span></span>


</dt> <dd>

<span data-ttu-id="89049-211">Aucune compression</span><span class="sxs-lookup"><span data-stu-id="89049-211">No Compression</span></span>

</dd> <dt>

<span id="V.42bis"></span><span id="v.42bis"></span><span id="V.42BIS"></span>

<span data-ttu-id="89049-212"><span id="v.42bis"></span><span id="V.42BIS"></span>**V. 42bis** (4)</span><span class="sxs-lookup"><span data-stu-id="89049-212"><span id="v.42bis"></span><span id="V.42BIS"></span>**V.42bis** (4)</span></span>


</dt> <dd>

<span data-ttu-id="89049-213">MNP 5</span><span class="sxs-lookup"><span data-stu-id="89049-213">MNP 5</span></span>

</dd> <dt>

<span id="5"></span>

<span data-ttu-id="89049-214"><span id="5"></span>**5,5**</span><span class="sxs-lookup"><span data-stu-id="89049-214"><span id="5"></span>**5**</span></span>


</dt> <dd>

<span data-ttu-id="89049-215">V. 42bis</span><span class="sxs-lookup"><span data-stu-id="89049-215">V.42bis</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="89049-216">**CompressionOff**</span><span class="sxs-lookup"><span data-stu-id="89049-216">**CompressionOff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-217">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="89049-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89049-218">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89049-219">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("compression de la \| \\ \\ classe de contrôle CurrentControlSet System Win32Registry \\ \\ \\ \\ \| \_ ")</span><span class="sxs-lookup"><span data-stu-id="89049-219">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Compression\_Off")</span></span>
</dt> </dl>

<span data-ttu-id="89049-220">Chaîne de commande utilisée pour désactiver la compression de données matérielles.</span><span class="sxs-lookup"><span data-stu-id="89049-220">Command string used to disable hardware data compression.</span></span>

<span data-ttu-id="89049-221">Exemple : « S46 = 136 »</span><span class="sxs-lookup"><span data-stu-id="89049-221">Example: "S46=136"</span></span>

</dd> <dt>

<span data-ttu-id="89049-222">**CompressionOn**</span><span class="sxs-lookup"><span data-stu-id="89049-222">**CompressionOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-223">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="89049-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89049-224">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89049-225">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| compression \_ ")</span><span class="sxs-lookup"><span data-stu-id="89049-225">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Compression\_On")</span></span>
</dt> </dl>

<span data-ttu-id="89049-226">Chaîne de commande utilisée pour activer la compression de données matérielles.</span><span class="sxs-lookup"><span data-stu-id="89049-226">Command string used to enable hardware data compression.</span></span>

<span data-ttu-id="89049-227">Exemple : « S46 = 138 »</span><span class="sxs-lookup"><span data-stu-id="89049-227">Example: "S46=138"</span></span>

</dd> <dt>

<span data-ttu-id="89049-228">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="89049-228">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-229">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89049-229">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89049-230">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89049-231">Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="89049-231">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="89049-232">Code d’erreur Configuration Manager Win32.</span><span class="sxs-lookup"><span data-stu-id="89049-232">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="89049-233">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="89049-233">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="89049-234"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="89049-234"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="89049-235"> (0)</span><span class="sxs-lookup"><span data-stu-id="89049-235">(0)</span></span>


</dt> <dd>

<span data-ttu-id="89049-236">L’appareil fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="89049-236">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="89049-237"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="89049-237"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="89049-238">(1)</span><span class="sxs-lookup"><span data-stu-id="89049-238">(1)</span></span>


</dt> <dd>

<span data-ttu-id="89049-239">L’appareil n’est pas configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="89049-239">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="89049-240"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="89049-240"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="89049-241">(2)</span><span class="sxs-lookup"><span data-stu-id="89049-241">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="89049-242"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="89049-242"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="89049-243">(3)</span><span class="sxs-lookup"><span data-stu-id="89049-243">(3)</span></span>


</dt> <dd>

<span data-ttu-id="89049-244">Le pilote de cet appareil est peut-être endommagé ou la mémoire ou d’autres ressources du système sont peut-être insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="89049-244">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="89049-245"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="89049-245"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="89049-246">(4)</span><span class="sxs-lookup"><span data-stu-id="89049-246">(4)</span></span>


</dt> <dd>

<span data-ttu-id="89049-247">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="89049-247">Device is not working properly.</span></span> <span data-ttu-id="89049-248">L’un de ses pilotes ou le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="89049-248">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="89049-249"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="89049-249"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="89049-250">(5)</span><span class="sxs-lookup"><span data-stu-id="89049-250">(5)</span></span>


</dt> <dd>

<span data-ttu-id="89049-251">Le pilote de l’appareil requiert une ressource que Windows ne peut pas gérer.</span><span class="sxs-lookup"><span data-stu-id="89049-251">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="89049-252"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="89049-252"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="89049-253"> (6)</span><span class="sxs-lookup"><span data-stu-id="89049-253">(6)</span></span>


</dt> <dd>

<span data-ttu-id="89049-254">La configuration de démarrage de l’appareil est en conflit avec d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="89049-254">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="89049-255"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="89049-255"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="89049-256">(7)</span><span class="sxs-lookup"><span data-stu-id="89049-256">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="89049-257"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="89049-257"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="89049-258">(8)</span><span class="sxs-lookup"><span data-stu-id="89049-258">(8)</span></span>


</dt> <dd>

<span data-ttu-id="89049-259">Le chargeur de pilote de l’appareil est manquant.</span><span class="sxs-lookup"><span data-stu-id="89049-259">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="89049-260"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="89049-260"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="89049-261">(9)</span><span class="sxs-lookup"><span data-stu-id="89049-261">(9)</span></span>


</dt> <dd>

<span data-ttu-id="89049-262">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="89049-262">Device is not working properly.</span></span> <span data-ttu-id="89049-263">Le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="89049-263">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="89049-264"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="89049-264"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="89049-265">(10)</span><span class="sxs-lookup"><span data-stu-id="89049-265">(10)</span></span>


</dt> <dd>

<span data-ttu-id="89049-266">Impossible de démarrer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="89049-266">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="89049-267"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="89049-267"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="89049-268">(11)</span><span class="sxs-lookup"><span data-stu-id="89049-268">(11)</span></span>


</dt> <dd>

<span data-ttu-id="89049-269">Échec de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="89049-269">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="89049-270"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="89049-270"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="89049-271">douze</span><span class="sxs-lookup"><span data-stu-id="89049-271">(12)</span></span>


</dt> <dd>

<span data-ttu-id="89049-272">L’appareil ne peut pas trouver suffisamment de ressources libres à utiliser.</span><span class="sxs-lookup"><span data-stu-id="89049-272">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="89049-273"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="89049-273"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="89049-274">(13)</span><span class="sxs-lookup"><span data-stu-id="89049-274">(13)</span></span>


</dt> <dd>

<span data-ttu-id="89049-275">Windows ne peut pas vérifier les ressources de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="89049-275">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="89049-276"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="89049-276"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="89049-277">(14)</span><span class="sxs-lookup"><span data-stu-id="89049-277">(14)</span></span>


</dt> <dd>

<span data-ttu-id="89049-278">L’appareil ne peut pas fonctionner correctement tant que l’ordinateur n’a pas redémarré.</span><span class="sxs-lookup"><span data-stu-id="89049-278">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="89049-279"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="89049-279"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="89049-280">(15)</span><span class="sxs-lookup"><span data-stu-id="89049-280">(15)</span></span>


</dt> <dd>

<span data-ttu-id="89049-281">L’appareil ne fonctionne pas correctement en raison d’un éventuel problème de réénumération.</span><span class="sxs-lookup"><span data-stu-id="89049-281">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="89049-282"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="89049-282"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="89049-283">(16)</span><span class="sxs-lookup"><span data-stu-id="89049-283">(16)</span></span>


</dt> <dd>

<span data-ttu-id="89049-284">Windows ne peut pas identifier toutes les ressources utilisées par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="89049-284">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="89049-285"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="89049-285"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="89049-286">(17)</span><span class="sxs-lookup"><span data-stu-id="89049-286">(17)</span></span>


</dt> <dd>

<span data-ttu-id="89049-287">L’appareil demande un type de ressource inconnu.</span><span class="sxs-lookup"><span data-stu-id="89049-287">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="89049-288"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="89049-288"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="89049-289">(18)</span><span class="sxs-lookup"><span data-stu-id="89049-289">(18)</span></span>


</dt> <dd>

<span data-ttu-id="89049-290">Les pilotes de périphérique doivent être réinstallés.</span><span class="sxs-lookup"><span data-stu-id="89049-290">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="89049-291"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="89049-291"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="89049-292">(19)</span><span class="sxs-lookup"><span data-stu-id="89049-292">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="89049-293"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="89049-293"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="89049-294">(20)</span><span class="sxs-lookup"><span data-stu-id="89049-294">(20)</span></span>


</dt> <dd>

<span data-ttu-id="89049-295">Le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="89049-295">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="89049-296"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="89049-296"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="89049-297">(21)</span><span class="sxs-lookup"><span data-stu-id="89049-297">(21)</span></span>


</dt> <dd>

<span data-ttu-id="89049-298">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="89049-298">System failure.</span></span> <span data-ttu-id="89049-299">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="89049-299">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="89049-300">Windows supprime l’appareil.</span><span class="sxs-lookup"><span data-stu-id="89049-300">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="89049-301"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="89049-301"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="89049-302">(22)</span><span class="sxs-lookup"><span data-stu-id="89049-302">(22)</span></span>


</dt> <dd>

<span data-ttu-id="89049-303">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="89049-303">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="89049-304"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="89049-304"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="89049-305">(23)</span><span class="sxs-lookup"><span data-stu-id="89049-305">(23)</span></span>


</dt> <dd>

<span data-ttu-id="89049-306">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="89049-306">System failure.</span></span> <span data-ttu-id="89049-307">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="89049-307">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="89049-308"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="89049-308"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="89049-309">(24)</span><span class="sxs-lookup"><span data-stu-id="89049-309">(24)</span></span>


</dt> <dd>

<span data-ttu-id="89049-310">L’appareil n’est pas présent, ne fonctionne pas correctement ou n’a pas tous ses pilotes installés.</span><span class="sxs-lookup"><span data-stu-id="89049-310">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="89049-311"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="89049-311"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="89049-312">(25)</span><span class="sxs-lookup"><span data-stu-id="89049-312">(25)</span></span>


</dt> <dd>

<span data-ttu-id="89049-313">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="89049-313">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="89049-314"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="89049-314"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="89049-315">(26)</span><span class="sxs-lookup"><span data-stu-id="89049-315">(26)</span></span>


</dt> <dd>

<span data-ttu-id="89049-316">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="89049-316">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="89049-317"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="89049-317"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="89049-318">(27)</span><span class="sxs-lookup"><span data-stu-id="89049-318">(27)</span></span>


</dt> <dd>

<span data-ttu-id="89049-319">L’appareil n’a pas une configuration de journal valide.</span><span class="sxs-lookup"><span data-stu-id="89049-319">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="89049-320"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="89049-320"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="89049-321">(28)</span><span class="sxs-lookup"><span data-stu-id="89049-321">(28)</span></span>


</dt> <dd>

<span data-ttu-id="89049-322">Les pilotes de périphérique ne sont pas installés.</span><span class="sxs-lookup"><span data-stu-id="89049-322">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="89049-323"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="89049-323"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="89049-324">(29)</span><span class="sxs-lookup"><span data-stu-id="89049-324">(29)</span></span>


</dt> <dd>

<span data-ttu-id="89049-325">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="89049-325">Device is disabled.</span></span> <span data-ttu-id="89049-326">Le microprogramme de l’appareil n’a pas fourni les ressources requises.</span><span class="sxs-lookup"><span data-stu-id="89049-326">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="89049-327"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="89049-327"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="89049-328">(30)</span><span class="sxs-lookup"><span data-stu-id="89049-328">(30)</span></span>


</dt> <dd>

<span data-ttu-id="89049-329">L’appareil utilise une ressource IRQ qu’un autre appareil utilise.</span><span class="sxs-lookup"><span data-stu-id="89049-329">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="89049-330"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="89049-330"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="89049-331">31</span><span class="sxs-lookup"><span data-stu-id="89049-331">(31)</span></span>


</dt> <dd>

<span data-ttu-id="89049-332">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="89049-332">Device is not working properly.</span></span> <span data-ttu-id="89049-333">Windows ne peut pas charger les pilotes de périphérique requis.</span><span class="sxs-lookup"><span data-stu-id="89049-333">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="89049-334">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="89049-334">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-335">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="89049-335">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="89049-336">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89049-337">Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="89049-337">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="89049-338">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="89049-338">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="89049-339">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="89049-339">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="89049-340">**Renforcée**</span><span class="sxs-lookup"><span data-stu-id="89049-340">**ConfigurationDialog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-341">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="89049-341">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89049-342">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-342">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89049-343">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| ConfigDialog")</span><span class="sxs-lookup"><span data-stu-id="89049-343">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|ConfigDialog")</span></span>
</dt> </dl>

<span data-ttu-id="89049-344">Chaîne d’initialisation du modem.</span><span class="sxs-lookup"><span data-stu-id="89049-344">Modem initialization string.</span></span> <span data-ttu-id="89049-345">Cette propriété est constituée de chaînes de commande d’autres propriétés de cette classe.</span><span class="sxs-lookup"><span data-stu-id="89049-345">This property is made up of command strings from other properties of this class.</span></span>

</dd> <dt>

<span data-ttu-id="89049-346">**CountriesSupported**</span><span class="sxs-lookup"><span data-stu-id="89049-346">**CountriesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-347">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="89049-347">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="89049-348">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89049-349">Tableau de pays/régions dans lesquels le modem peut fonctionner.</span><span class="sxs-lookup"><span data-stu-id="89049-349">Array of countries/regions in which the modem can operate.</span></span>

<span data-ttu-id="89049-350">Cette propriété est héritée de la [**\_ PotsModem CIM**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="89049-350">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="89049-351">**CountrySelected**</span><span class="sxs-lookup"><span data-stu-id="89049-351">**CountrySelected**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-352">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="89049-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89049-353">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89049-354">Pays/région pour lequel le modem est actuellement programmé.</span><span class="sxs-lookup"><span data-stu-id="89049-354">Country/region for which the modem is currently programmed.</span></span> <span data-ttu-id="89049-355">Lorsque plusieurs pays/régions sont pris en charge, cette propriété définit celle qui est actuellement sélectionnée pour être utilisée.</span><span class="sxs-lookup"><span data-stu-id="89049-355">When multiple countries/regions are supported, this property defines which one is currently selected for use.</span></span>

<span data-ttu-id="89049-356">Cette propriété est héritée de la [**\_ PotsModem CIM**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="89049-356">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="89049-357">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="89049-357">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-358">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="89049-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89049-359">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89049-360">Qualificateurs : [ **\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="89049-360">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="89049-361">Nom de la première classe concrète à afficher dans la chaîne d’héritage utilisée lors de la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="89049-361">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="89049-362">Lorsqu’elle est utilisée avec les autres propriétés de clé de la classe, la propriété permet d’identifier de manière unique toutes les instances de cette classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="89049-362">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="89049-363">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="89049-363">This property is inherited from [**CIM\_LogicalDevice**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="89049-364">**CurrentPasswords**</span><span class="sxs-lookup"><span data-stu-id="89049-364">**CurrentPasswords**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-365">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="89049-365">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="89049-366">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89049-367">Liste des mots de passe actuellement définis pour le modem.</span><span class="sxs-lookup"><span data-stu-id="89049-367">List of currently defined passwords for the modem.</span></span> <span data-ttu-id="89049-368">Ce tableau peut être laissé vide pour des raisons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="89049-368">This array may be left blank for security reasons.</span></span>

<span data-ttu-id="89049-369">Cette propriété est héritée de la [**\_ PotsModem CIM**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="89049-369">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="89049-370">**DCB**</span><span class="sxs-lookup"><span data-stu-id="89049-370">**DCB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-371">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="89049-371">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="89049-372">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-372">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89049-373">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« \| structures de communication win32api \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)»)</span><span class="sxs-lookup"><span data-stu-id="89049-373">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)")</span></span>
</dt> </dl>

<span data-ttu-id="89049-374">Contrôler les paramètres d’un appareil de communication série, dans ce cas, le périphérique du modem.</span><span class="sxs-lookup"><span data-stu-id="89049-374">Control settings for a serial communications device, in this case, the modem device.</span></span>

</dd> <dt>

<span data-ttu-id="89049-375">**Par défaut**</span><span class="sxs-lookup"><span data-stu-id="89049-375">**Default**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-376">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="89049-376">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="89049-377">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-377">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89049-378">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| default")</span><span class="sxs-lookup"><span data-stu-id="89049-378">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Default")</span></span>
</dt> </dl>

<span data-ttu-id="89049-379">Si la **valeur est true**, ce modem pots est le modem par défaut sur le système informatique exécutant Windows.</span><span class="sxs-lookup"><span data-stu-id="89049-379">If **TRUE**, this POTS modem is the default modem on the computer system running Windows.</span></span>

</dd> <dt>

<span data-ttu-id="89049-380">**Description**</span><span class="sxs-lookup"><span data-stu-id="89049-380">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-381">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="89049-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89049-382">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89049-383">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="89049-383">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="89049-384">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="89049-384">Description of the object.</span></span>

<span data-ttu-id="89049-385">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="89049-385">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="89049-386">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="89049-386">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-387">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="89049-387">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89049-388">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89049-389">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**remplacement**](../wmisdk/standard-qualifiers.md) (« DeviceID »), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI »)</span><span class="sxs-lookup"><span data-stu-id="89049-389">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="89049-390">Identificateur unique de ce modem POTS provenant d’autres appareils sur le système.</span><span class="sxs-lookup"><span data-stu-id="89049-390">Unique identifier of this POTS modem from other devices on the system.</span></span>

<span data-ttu-id="89049-391">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="89049-391">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="89049-392">**DeviceLoader**</span><span class="sxs-lookup"><span data-stu-id="89049-392">**DeviceLoader**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-393">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="89049-393">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89049-394">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89049-395">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| DevLoader")</span><span class="sxs-lookup"><span data-stu-id="89049-395">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|DevLoader")</span></span>
</dt> </dl>

<span data-ttu-id="89049-396">Nom du chargeur de l’appareil pour le modem.</span><span class="sxs-lookup"><span data-stu-id="89049-396">Name of the device loader for the modem.</span></span> <span data-ttu-id="89049-397">Un chargeur d’appareil charge et gère les pilotes de périphérique et les énumérateurs pour un appareil donné.</span><span class="sxs-lookup"><span data-stu-id="89049-397">A device loader loads and manages device drivers and enumerators for a given device.</span></span>

</dd> <dt>

<span data-ttu-id="89049-398">**DeviceType**</span><span class="sxs-lookup"><span data-stu-id="89049-398">**DeviceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-399">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="89049-399">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89049-400">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89049-401">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| DeviceType")</span><span class="sxs-lookup"><span data-stu-id="89049-401">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|DeviceType")</span></span>
</dt> </dl>

<span data-ttu-id="89049-402">Type physique du modem.</span><span class="sxs-lookup"><span data-stu-id="89049-402">Physical type of the modem.</span></span>

<span data-ttu-id="89049-403">Les valeurs sont :</span><span class="sxs-lookup"><span data-stu-id="89049-403">The values are:</span></span>

<dl> <dd><span data-ttu-id="89049-404">« Null modem »</span><span class="sxs-lookup"><span data-stu-id="89049-404">"Null Modem"</span></span></dd> <dd><span data-ttu-id="89049-405">« Modem interne »</span><span class="sxs-lookup"><span data-stu-id="89049-405">"Internal Modem"</span></span></dd> <dd><span data-ttu-id="89049-406">« Modem externe »</span><span class="sxs-lookup"><span data-stu-id="89049-406">"External Modem"</span></span></dd> <dd><span data-ttu-id="89049-407">« Modem PCMCIA »</span><span class="sxs-lookup"><span data-stu-id="89049-407">"PCMCIA Modem"</span></span></dd> <dd><span data-ttu-id="89049-408">Connue</span><span class="sxs-lookup"><span data-stu-id="89049-408">"Unknown"</span></span></dd> </dl>

<dt>

<span id="Null_Modem"></span><span id="null_modem"></span><span id="NULL_MODEM"></span>

<span data-ttu-id="89049-409">**Null modem** (« null modem »)</span><span class="sxs-lookup"><span data-stu-id="89049-409">**Null Modem** ("Null Modem")</span></span>


</dt> <dd></dd> <dt>

<span id="Internal_Modem"></span><span id="internal_modem"></span><span id="INTERNAL_MODEM"></span>

<span data-ttu-id="89049-410">**Modem interne** (« modem interne »)</span><span class="sxs-lookup"><span data-stu-id="89049-410">**Internal Modem** ("Internal Modem")</span></span>


</dt> <dd></dd> <dt>

<span id="External_Modem"></span><span id="external_modem"></span><span id="EXTERNAL_MODEM"></span>

<span data-ttu-id="89049-411">**Modem externe** (« modem externe »)</span><span class="sxs-lookup"><span data-stu-id="89049-411">**External Modem** ("External Modem")</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Modem"></span><span id="pcmcia_modem"></span><span id="PCMCIA_MODEM"></span>

<span data-ttu-id="89049-412">**Modem PCMCIA** (« Modem PCMCIA »)</span><span class="sxs-lookup"><span data-stu-id="89049-412">**PCMCIA Modem** ("PCMCIA Modem")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="89049-413">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="89049-413">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="89049-414">**DialType**</span><span class="sxs-lookup"><span data-stu-id="89049-414">**DialType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-415">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="89049-415">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="89049-416">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89049-417">Type de méthode de numérotation utilisé.</span><span class="sxs-lookup"><span data-stu-id="89049-417">Type of dialing method used.</span></span>

<span data-ttu-id="89049-418">Cette propriété est héritée de la [**\_ PotsModem CIM**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="89049-418">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="89049-419">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="89049-419">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Tone"></span><span id="tone"></span><span id="TONE"></span>

<span data-ttu-id="89049-420">**Ton** (1)</span><span class="sxs-lookup"><span data-stu-id="89049-420">**Tone** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Pulse"></span><span id="pulse"></span><span id="PULSE"></span>

<span data-ttu-id="89049-421">**Impulsion** (2)</span><span class="sxs-lookup"><span data-stu-id="89049-421">**Pulse** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="89049-422">**DriverDate**</span><span class="sxs-lookup"><span data-stu-id="89049-422">**DriverDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-423">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="89049-423">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="89049-424">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-424">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89049-425">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| DriverDate")</span><span class="sxs-lookup"><span data-stu-id="89049-425">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|DriverDate")</span></span>
</dt> </dl>

<span data-ttu-id="89049-426">Date du pilote de modem.</span><span class="sxs-lookup"><span data-stu-id="89049-426">Date of the modem driver.</span></span>

</dd> <dt>

<span data-ttu-id="89049-427">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="89049-427">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-428">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="89049-428">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="89049-429">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-429">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89049-430">Si la **valeur est true**, l’erreur signalée dans **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="89049-430">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="89049-431">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="89049-431">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="89049-432">**ErrorControlForced**</span><span class="sxs-lookup"><span data-stu-id="89049-432">**ErrorControlForced**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-433">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="89049-433">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89049-434">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-434">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89049-435">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ classe \| ErrorControl \_ Forced")</span><span class="sxs-lookup"><span data-stu-id="89049-435">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|ErrorControl\_Forced")</span></span>
</dt> </dl>

<span data-ttu-id="89049-436">Chaîne de commande utilisée pour activer le contrôle de correction d’erreur lors de l’établissement d’une connexion.</span><span class="sxs-lookup"><span data-stu-id="89049-436">Command string used to enable error correction control when establishing a connection.</span></span> <span data-ttu-id="89049-437">Cela augmente la fiabilité de la connexion.</span><span class="sxs-lookup"><span data-stu-id="89049-437">This increases the reliability of the connection.</span></span>

<span data-ttu-id="89049-438">Exemple : « + Q5S36 = 4S48 = 7 »</span><span class="sxs-lookup"><span data-stu-id="89049-438">Example: "+Q5S36=4S48=7"</span></span>

</dd> <dt>

<span data-ttu-id="89049-439">**ErrorControlInfo**</span><span class="sxs-lookup"><span data-stu-id="89049-439">**ErrorControlInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-440">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="89049-440">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="89049-441">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-441">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89049-442">Caractéristiques de correction des erreurs du modem.</span><span class="sxs-lookup"><span data-stu-id="89049-442">Error correction characteristics of the modem.</span></span>

<span data-ttu-id="89049-443">Cette propriété est héritée de la [**\_ PotsModem CIM**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="89049-443">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="89049-444">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="89049-444">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="89049-445">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="89049-445">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Error_Correction"></span><span id="no_error_correction"></span><span id="NO_ERROR_CORRECTION"></span>

<span data-ttu-id="89049-446">**Aucune correction d’erreur** (2)</span><span class="sxs-lookup"><span data-stu-id="89049-446">**No Error Correction** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="MNP_4"></span><span id="mnp_4"></span>

<span data-ttu-id="89049-447">**MNP 4** (3)</span><span class="sxs-lookup"><span data-stu-id="89049-447">**MNP 4** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="LAPM"></span><span id="lapm"></span>

<span data-ttu-id="89049-448">**LAPM** (4)</span><span class="sxs-lookup"><span data-stu-id="89049-448">**LAPM** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="89049-449">**ErrorControlOff**</span><span class="sxs-lookup"><span data-stu-id="89049-449">**ErrorControlOff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-450">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="89049-450">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89049-451">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-451">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89049-452">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| ErrorControl \_ off")</span><span class="sxs-lookup"><span data-stu-id="89049-452">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|ErrorControl\_Off")</span></span>
</dt> </dl>

<span data-ttu-id="89049-453">Chaîne de commande utilisée pour désactiver le contrôle d’erreur.</span><span class="sxs-lookup"><span data-stu-id="89049-453">Command string used to disable error control.</span></span>

<span data-ttu-id="89049-454">Exemple : « + Q6S36 = 3S48 = 128 »</span><span class="sxs-lookup"><span data-stu-id="89049-454">Example: "+Q6S36=3S48=128"</span></span>

</dd> <dt>

<span data-ttu-id="89049-455">**ErrorControlOn**</span><span class="sxs-lookup"><span data-stu-id="89049-455">**ErrorControlOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-456">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="89049-456">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89049-457">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-457">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89049-458">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| ErrorControl \_ on")</span><span class="sxs-lookup"><span data-stu-id="89049-458">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|ErrorControl\_On")</span></span>
</dt> </dl>

<span data-ttu-id="89049-459">Chaîne de commande utilisée pour activer le contrôle d’erreur.</span><span class="sxs-lookup"><span data-stu-id="89049-459">Command string used to enable error control.</span></span>

<span data-ttu-id="89049-460">Exemple : « + Q5S36 = 7S48 = 7 »</span><span class="sxs-lookup"><span data-stu-id="89049-460">Example: "+Q5S36=7S48=7"</span></span>

</dd> <dt>

<span data-ttu-id="89049-461">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="89049-461">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-462">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="89049-462">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89049-463">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-463">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89049-464">Plus d’informations sur l’erreur enregistrée dans **LastErrorCode**, ainsi que sur les actions correctives qui peuvent être prises.</span><span class="sxs-lookup"><span data-stu-id="89049-464">More information about the error recorded in **LastErrorCode**, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="89049-465">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="89049-465">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="89049-466">**FlowControlHard**</span><span class="sxs-lookup"><span data-stu-id="89049-466">**FlowControlHard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-467">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="89049-467">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89049-468">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-468">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89049-469">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| FlowControl \_ Hard")</span><span class="sxs-lookup"><span data-stu-id="89049-469">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|FlowControl\_Hard")</span></span>
</dt> </dl>

<span data-ttu-id="89049-470">Chaîne de commande utilisée pour activer le contrôle de workflow matériel.</span><span class="sxs-lookup"><span data-stu-id="89049-470">Command string used to enable hardware flow control.</span></span> <span data-ttu-id="89049-471">Le contrôle de Flow est constitué de signaux envoyés entre des ordinateurs qui vérifient que les deux ordinateurs sont prêts à transmettre ou à recevoir des données.</span><span class="sxs-lookup"><span data-stu-id="89049-471">Flow control consists of signals sent between computers that verify that both computers are ready to transmit or receive data.</span></span>

<span data-ttu-id="89049-472">Exemple : « &K1 »</span><span class="sxs-lookup"><span data-stu-id="89049-472">Example: "&K1"</span></span>

</dd> <dt>

<span data-ttu-id="89049-473">**FlowControlOff**</span><span class="sxs-lookup"><span data-stu-id="89049-473">**FlowControlOff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-474">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="89049-474">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89049-475">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-475">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89049-476">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| FlowControl \_ ")</span><span class="sxs-lookup"><span data-stu-id="89049-476">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|FlowControl\_Off")</span></span>
</dt> </dl>

<span data-ttu-id="89049-477">Chaîne de commande utilisée pour désactiver le contrôle de Flow.</span><span class="sxs-lookup"><span data-stu-id="89049-477">Command string used to disable flow control.</span></span> <span data-ttu-id="89049-478">Le contrôle de Flow est constitué de signaux envoyés entre des ordinateurs qui vérifient que les deux ordinateurs sont prêts à transmettre ou à recevoir des données.</span><span class="sxs-lookup"><span data-stu-id="89049-478">Flow control consists of signals sent between computers that verify that both computers are ready to transmit or receive data.</span></span>

<span data-ttu-id="89049-479">Exemple : « &K0 »</span><span class="sxs-lookup"><span data-stu-id="89049-479">Example: "&K0"</span></span>

</dd> <dt>

<span data-ttu-id="89049-480">**FlowControlSoft**</span><span class="sxs-lookup"><span data-stu-id="89049-480">**FlowControlSoft**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-481">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="89049-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89049-482">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-482">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89049-483">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| FlowControl \_ Soft")</span><span class="sxs-lookup"><span data-stu-id="89049-483">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|FlowControl\_Soft")</span></span>
</dt> </dl>

<span data-ttu-id="89049-484">Chaîne de commande utilisée pour activer le contrôle de Workflow.</span><span class="sxs-lookup"><span data-stu-id="89049-484">Command string used to enable software flow control.</span></span> <span data-ttu-id="89049-485">Le contrôle de Flow est constitué de signaux envoyés entre des ordinateurs qui vérifient que les deux ordinateurs sont prêts à transmettre ou à recevoir des données.</span><span class="sxs-lookup"><span data-stu-id="89049-485">Flow control consists of signals sent between computers that verify that both computers are ready to transmit or receive data.</span></span>

<span data-ttu-id="89049-486">Exemple : « &K2 »</span><span class="sxs-lookup"><span data-stu-id="89049-486">Example: "&K2"</span></span>

</dd> <dt>

<span data-ttu-id="89049-487">**InactivityScale**</span><span class="sxs-lookup"><span data-stu-id="89049-487">**InactivityScale**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-488">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="89049-488">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89049-489">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-489">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89049-490">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| InactivityScale")</span><span class="sxs-lookup"><span data-stu-id="89049-490">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|InactivityScale")</span></span>
</dt> </dl>

<span data-ttu-id="89049-491">Multiplicateur utilisé avec la propriété **InactivityTimeout** pour calculer le délai d’expiration d’une connexion.</span><span class="sxs-lookup"><span data-stu-id="89049-491">Multiplier used with the **InactivityTimeout** property to calculate the timeout period of a connection.</span></span>

</dd> <dt>

<span data-ttu-id="89049-492">**InactivityTimeout**</span><span class="sxs-lookup"><span data-stu-id="89049-492">**InactivityTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-493">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89049-493">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89049-494">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-494">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89049-495">Qualificateurs : [**unités**](../wmisdk/standard-qualifiers.md) (« secondes »)</span><span class="sxs-lookup"><span data-stu-id="89049-495">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="89049-496">Limite de temps (en secondes) pour la déconnexion automatique de la ligne téléphonique, si aucune donnée n’est échangée.</span><span class="sxs-lookup"><span data-stu-id="89049-496">Time limit (in seconds) for automatic disconnection of the phone line, if no data is exchanged.</span></span> <span data-ttu-id="89049-497">La valeur 0 (zéro) indique que cette fonctionnalité est présente mais pas activée.</span><span class="sxs-lookup"><span data-stu-id="89049-497">A value of 0 (zero) indicates that this feature is present but not enabled.</span></span>

<span data-ttu-id="89049-498">Cette propriété est héritée de la [**\_ PotsModem CIM**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="89049-498">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="89049-499">**Index**</span><span class="sxs-lookup"><span data-stu-id="89049-499">**Index**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-500">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89049-500">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89049-501">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-501">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89049-502">Numéro d’index de ce modem POTS.</span><span class="sxs-lookup"><span data-stu-id="89049-502">Index number for this POTS modem.</span></span>

<span data-ttu-id="89049-503">Exemple : 0</span><span class="sxs-lookup"><span data-stu-id="89049-503">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="89049-504">**IndexEx**</span><span class="sxs-lookup"><span data-stu-id="89049-504">**IndexEx**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-505">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="89049-505">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89049-506">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-506">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89049-507">ID d’instance d’appareil pour ce modem POTS.</span><span class="sxs-lookup"><span data-stu-id="89049-507">The device instance ID for this POTS modem.</span></span>

<span data-ttu-id="89049-508">Exemple : « 1&08 »</span><span class="sxs-lookup"><span data-stu-id="89049-508">Example: "1&08"</span></span>

<span data-ttu-id="89049-509">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 et Windows Vista :** Cette propriété est disponible à partir de Windows Server 2016 et Windows 10.</span><span class="sxs-lookup"><span data-stu-id="89049-509">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is available beginning with Windows Server 2016 and Windows 10.</span></span>

</dd> <dt>

<span data-ttu-id="89049-510">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="89049-510">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-511">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="89049-511">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="89049-512">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-512">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89049-513">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="89049-513">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="89049-514">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="89049-514">Date and time the object was installed.</span></span> <span data-ttu-id="89049-515">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="89049-515">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="89049-516">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="89049-516">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="89049-517">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="89049-517">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-518">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89049-518">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89049-519">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-519">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89049-520">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="89049-520">Last error code reported by the logical device.</span></span>

<span data-ttu-id="89049-521">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="89049-521">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="89049-522">**MaxBaudRateToPhone**</span><span class="sxs-lookup"><span data-stu-id="89049-522">**MaxBaudRateToPhone**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-523">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89049-523">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89049-524">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-524">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89049-525">Qualificateurs : [**unités**](../wmisdk/standard-qualifiers.md) (« bits par seconde »)</span><span class="sxs-lookup"><span data-stu-id="89049-525">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="89049-526">Vitesse maximale de communication définissable pour l’accès au système téléphonique.</span><span class="sxs-lookup"><span data-stu-id="89049-526">Maximum settable communication speed for accessing the phone system.</span></span>

<span data-ttu-id="89049-527">Cette propriété est héritée de la [**\_ PotsModem CIM**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="89049-527">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="89049-528">**MaxBaudRateToSerialPort**</span><span class="sxs-lookup"><span data-stu-id="89049-528">**MaxBaudRateToSerialPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-529">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89049-529">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89049-530">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-530">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89049-531">Qualificateurs : [**unités**](../wmisdk/standard-qualifiers.md) (« bits par seconde »)</span><span class="sxs-lookup"><span data-stu-id="89049-531">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="89049-532">Vitesse maximale de communication définissable au port COM pour un modem externe.</span><span class="sxs-lookup"><span data-stu-id="89049-532">Maximum settable communication speed to the COM port for an external modem.</span></span> <span data-ttu-id="89049-533">Entrez 0 (zéro) si ce n’est pas le cas.</span><span class="sxs-lookup"><span data-stu-id="89049-533">Enter 0 (zero) if not applicable.</span></span>

<span data-ttu-id="89049-534">Cette propriété est héritée de la [**\_ PotsModem CIM**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="89049-534">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="89049-535">**MaxNumberOfPasswords**</span><span class="sxs-lookup"><span data-stu-id="89049-535">**MaxNumberOfPasswords**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-536">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="89049-536">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="89049-537">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-537">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89049-538">Nombre de mots de passe définissables dans le modem lui-même.</span><span class="sxs-lookup"><span data-stu-id="89049-538">Number of passwords definable in the modem itself.</span></span> <span data-ttu-id="89049-539">Si cette fonctionnalité n’est pas prise en charge, entrez 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="89049-539">If this feature is not supported, enter 0 (zero).</span></span>

<span data-ttu-id="89049-540">Cette propriété est héritée de la [**\_ PotsModem CIM**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="89049-540">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="89049-541">**Modèle**</span><span class="sxs-lookup"><span data-stu-id="89049-541">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-542">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="89049-542">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89049-543">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-543">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89049-544">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| Model")</span><span class="sxs-lookup"><span data-stu-id="89049-544">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Model")</span></span>
</dt> </dl>

<span data-ttu-id="89049-545">Modèle de ce modem POTS.</span><span class="sxs-lookup"><span data-stu-id="89049-545">Model of this POTS modem.</span></span>

<span data-ttu-id="89049-546">Exemple : « Sportster 56K External »</span><span class="sxs-lookup"><span data-stu-id="89049-546">Example: "Sportster 56K External"</span></span>

</dd> <dt>

<span data-ttu-id="89049-547">**ModemInfPath**</span><span class="sxs-lookup"><span data-stu-id="89049-547">**ModemInfPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-548">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="89049-548">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89049-549">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-549">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89049-550">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| InfPath")</span><span class="sxs-lookup"><span data-stu-id="89049-550">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|InfPath")</span></span>
</dt> </dl>

<span data-ttu-id="89049-551">Chemin du fichier. inf de ce modem.</span><span class="sxs-lookup"><span data-stu-id="89049-551">Path to this modem's .inf file.</span></span> <span data-ttu-id="89049-552">Ce fichier contient des informations d’initialisation pour le modem et son pilote.</span><span class="sxs-lookup"><span data-stu-id="89049-552">This file contains initialization information for the modem and its driver.</span></span>

<span data-ttu-id="89049-553">Exemple : « C : \\ Windows \\ INF »</span><span class="sxs-lookup"><span data-stu-id="89049-553">Example: "C:\\Windows\\INF"</span></span>

</dd> <dt>

<span data-ttu-id="89049-554">**ModemInfSection**</span><span class="sxs-lookup"><span data-stu-id="89049-554">**ModemInfSection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-555">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="89049-555">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89049-556">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-556">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89049-557">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| InfSection")</span><span class="sxs-lookup"><span data-stu-id="89049-557">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|InfSection")</span></span>
</dt> </dl>

<span data-ttu-id="89049-558">Nom de la section dans le fichier. inf du modem qui contient des informations sur le modem.</span><span class="sxs-lookup"><span data-stu-id="89049-558">Name of the section in the modem's .inf file that contains information about the modem.</span></span>

</dd> <dt>

<span data-ttu-id="89049-559">**ModulationBell**</span><span class="sxs-lookup"><span data-stu-id="89049-559">**ModulationBell**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-560">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="89049-560">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89049-561">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-561">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89049-562">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| \_ Bell")</span><span class="sxs-lookup"><span data-stu-id="89049-562">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Modulation\_Bell")</span></span>
</dt> </dl>

<span data-ttu-id="89049-563">Chaîne de commande utilisée pour indiquer au modem d’utiliser des modulations de cloche pour 300 et 1200 bps.</span><span class="sxs-lookup"><span data-stu-id="89049-563">Command string used to instruct the modem to use Bell modulations for 300 and 1200 bps.</span></span>

<span data-ttu-id="89049-564">Exemple : « B1 »</span><span class="sxs-lookup"><span data-stu-id="89049-564">Example: "B1"</span></span>

</dd> <dt>

<span data-ttu-id="89049-565">**ModulationCCITT**</span><span class="sxs-lookup"><span data-stu-id="89049-565">**ModulationCCITT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-566">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="89049-566">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89049-567">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-567">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89049-568">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| modulation \_ CCITT")</span><span class="sxs-lookup"><span data-stu-id="89049-568">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Modulation\_CCITT")</span></span>
</dt> </dl>

<span data-ttu-id="89049-569">Chaîne de commande utilisée pour indiquer au modem d’utiliser des modulations CCITT pour 300 et 1200 bps.</span><span class="sxs-lookup"><span data-stu-id="89049-569">Command string used to instruct the modem to use CCITT modulations for 300 and 1200 bps.</span></span>

<span data-ttu-id="89049-570">Exemple : « B0 »</span><span class="sxs-lookup"><span data-stu-id="89049-570">Example: "B0"</span></span>

</dd> <dt>

<span data-ttu-id="89049-571">**ModulationScheme**</span><span class="sxs-lookup"><span data-stu-id="89049-571">**ModulationScheme**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-572">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="89049-572">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="89049-573">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-573">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89049-574">Schéma de modulation du modem.</span><span class="sxs-lookup"><span data-stu-id="89049-574">Modulation scheme of the modem.</span></span>

<span data-ttu-id="89049-575">Cette propriété est héritée de la [**\_ PotsModem CIM**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="89049-575">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="89049-576">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="89049-576">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="89049-577">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="89049-577">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="89049-578">**Non pris en charge** (2)</span><span class="sxs-lookup"><span data-stu-id="89049-578">**Not Supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Bell_103"></span><span id="bell_103"></span><span id="BELL_103"></span>

<span data-ttu-id="89049-579">**Cloche 103** (3)</span><span class="sxs-lookup"><span data-stu-id="89049-579">**Bell 103** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bell_212A"></span><span id="bell_212a"></span><span id="BELL_212A"></span>

<span data-ttu-id="89049-580">**Cloche 212A** (4)</span><span class="sxs-lookup"><span data-stu-id="89049-580">**Bell 212A** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="V.22bis"></span><span id="v.22bis"></span><span id="V.22BIS"></span>

<span data-ttu-id="89049-581">**V. 22bis** (5)</span><span class="sxs-lookup"><span data-stu-id="89049-581">**V.22bis** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="V.32"></span><span id="v.32"></span>

<span data-ttu-id="89049-582">**V. 32** (6)</span><span class="sxs-lookup"><span data-stu-id="89049-582">**V.32** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="V.32bis"></span><span id="v.32bis"></span><span id="V.32BIS"></span>

<span data-ttu-id="89049-583">**V. 32bis** (7)</span><span class="sxs-lookup"><span data-stu-id="89049-583">**V.32bis** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="V.turbo"></span><span id="v.turbo"></span><span id="V.TURBO"></span>

<span data-ttu-id="89049-584">**V. Turbo** (8)</span><span class="sxs-lookup"><span data-stu-id="89049-584">**V.turbo** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="V.FC"></span><span id="v.fc"></span>

<span data-ttu-id="89049-585">**V. FC** (9)</span><span class="sxs-lookup"><span data-stu-id="89049-585">**V.FC** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="V.34"></span><span id="v.34"></span>

<span data-ttu-id="89049-586">**V. 34** (10)</span><span class="sxs-lookup"><span data-stu-id="89049-586">**V.34** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="V.34bis"></span><span id="v.34bis"></span><span id="V.34BIS"></span>

<span data-ttu-id="89049-587">**V. 34bis** (11)</span><span class="sxs-lookup"><span data-stu-id="89049-587">**V.34bis** (11)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="89049-588">**Nom**</span><span class="sxs-lookup"><span data-stu-id="89049-588">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-589">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="89049-589">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89049-590">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-590">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89049-591">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="89049-591">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="89049-592">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="89049-592">Label by which the object is known.</span></span> <span data-ttu-id="89049-593">Lorsqu’elle est sous-classée, la propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="89049-593">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="89049-594">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="89049-594">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="89049-595">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="89049-595">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-596">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="89049-596">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89049-597">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-597">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89049-598">Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="89049-598">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="89049-599">Identificateur d’appareil Windows Plug-and-Play de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="89049-599">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="89049-600">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="89049-600">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="89049-601">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="89049-601">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="89049-602">**PortSubClass**</span><span class="sxs-lookup"><span data-stu-id="89049-602">**PortSubClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-603">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="89049-603">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89049-604">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-604">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89049-605">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| PortSubClass"), **value** ("port parallèle", "port série", "modem")</span><span class="sxs-lookup"><span data-stu-id="89049-605">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|PortSubClass"), **Value** ("Parallel Port", "Serial Port", "Modem")</span></span>
</dt> </dl>

<span data-ttu-id="89049-606">Définition du port utilisé pour ce modem.</span><span class="sxs-lookup"><span data-stu-id="89049-606">Definition of the port used for this modem.</span></span>

<dt>



 <span data-ttu-id="89049-607">(« 00 »)</span><span class="sxs-lookup"><span data-stu-id="89049-607">("00")</span></span>


</dt> <dd>

<span data-ttu-id="89049-608">Port parallèle</span><span class="sxs-lookup"><span data-stu-id="89049-608">Parallel Port</span></span>

</dd> <dt>



 <span data-ttu-id="89049-609">(« 01 »)</span><span class="sxs-lookup"><span data-stu-id="89049-609">("01")</span></span>


</dt> <dd>

<span data-ttu-id="89049-610">Port série</span><span class="sxs-lookup"><span data-stu-id="89049-610">Serial Port</span></span>

</dd> <dt>



 <span data-ttu-id="89049-611">(« 02 »)</span><span class="sxs-lookup"><span data-stu-id="89049-611">("02")</span></span>


</dt> <dd>

<span data-ttu-id="89049-612">Modem</span><span class="sxs-lookup"><span data-stu-id="89049-612">Modem</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="89049-613">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="89049-613">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-614">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="89049-614">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="89049-615">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-615">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89049-616">Tableau des fonctionnalités d’alimentation spécifiques d’un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="89049-616">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="89049-617">Cette propriété est héritée de **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="89049-617">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="89049-618"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="89049-618"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="89049-619"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="89049-619"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="89049-620"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="89049-620"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="89049-621"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="89049-621"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="89049-622">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="89049-622">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="89049-623"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="89049-623"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="89049-624">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="89049-624">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="89049-625"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="89049-625"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="89049-626">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="89049-626">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="89049-627">Cette méthode se trouve sur la classe parente du **\_ LogicalDevice CIM** et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="89049-627">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="89049-628">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="89049-628">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="89049-629"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="89049-629"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="89049-630">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation).</span><span class="sxs-lookup"><span data-stu-id="89049-630">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="89049-631"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="89049-631"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="89049-632">Power-On chronométré pris en charge</span><span class="sxs-lookup"><span data-stu-id="89049-632">Timed Power-On Supported</span></span>

<span data-ttu-id="89049-633">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation) et l' *heure* définie sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="89049-633">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="89049-634">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="89049-634">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-635">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="89049-635">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="89049-636">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-636">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89049-637">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation (il peut être mis en mode veille, et ainsi de suite).</span><span class="sxs-lookup"><span data-stu-id="89049-637">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="89049-638">La propriété n’indique pas que les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais uniquement que l’appareil logique est capable de gérer l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="89049-638">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="89049-639">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="89049-639">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="89049-640">**Préfixe**</span><span class="sxs-lookup"><span data-stu-id="89049-640">**Prefix**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-641">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="89049-641">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89049-642">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-642">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89049-643">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| prefix")</span><span class="sxs-lookup"><span data-stu-id="89049-643">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Prefix")</span></span>
</dt> </dl>

<span data-ttu-id="89049-644">Préfixe de numérotation utilisé pour accéder à une ligne extérieure.</span><span class="sxs-lookup"><span data-stu-id="89049-644">Dialing prefix used to access an outside line.</span></span>

</dd> <dt>

<span data-ttu-id="89049-645">**Propriétés**</span><span class="sxs-lookup"><span data-stu-id="89049-645">**Properties**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-646">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="89049-646">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="89049-647">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-647">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89049-648">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("propriétés de la \| \\ \\ classe de contrôle CurrentControlSet System Win32Registry \\ \\ \\ \\ \| ")</span><span class="sxs-lookup"><span data-stu-id="89049-648">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Properties")</span></span>
</dt> </dl>

<span data-ttu-id="89049-649">Liste de toutes les propriétés (et leurs valeurs) pour ce modem.</span><span class="sxs-lookup"><span data-stu-id="89049-649">List of all the properties (and their values) for this modem.</span></span>

</dd> <dt>

<span data-ttu-id="89049-650">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="89049-650">**ProviderName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-651">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="89049-651">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89049-652">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-652">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89049-653">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| providerName")</span><span class="sxs-lookup"><span data-stu-id="89049-653">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|ProviderName")</span></span>
</dt> </dl>

<span data-ttu-id="89049-654">Chemin d’accès réseau à l’ordinateur qui fournit les services de modem.</span><span class="sxs-lookup"><span data-stu-id="89049-654">Network path to the computer that provides the modem services.</span></span>

</dd> <dt>

<span data-ttu-id="89049-655">**Séché**</span><span class="sxs-lookup"><span data-stu-id="89049-655">**Pulse**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-656">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="89049-656">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89049-657">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-657">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89049-658">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| Pulse")</span><span class="sxs-lookup"><span data-stu-id="89049-658">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Pulse")</span></span>
</dt> </dl>

<span data-ttu-id="89049-659">Chaîne de commande utilisée pour indiquer au modem d’utiliser le mode impulsion pour la numérotation.</span><span class="sxs-lookup"><span data-stu-id="89049-659">Command string used to instruct the modem to use pulse mode for dialing.</span></span> <span data-ttu-id="89049-660">La numérotation par impulsion est nécessaire pour les lignes téléphoniques qui ne peuvent pas gérer la numérotation par tonalité.</span><span class="sxs-lookup"><span data-stu-id="89049-660">Pulse dialing is necessary for phone lines that are unable to handle tone dialing.</span></span>

<span data-ttu-id="89049-661">Exemple : « P »</span><span class="sxs-lookup"><span data-stu-id="89049-661">Example: "P"</span></span>

</dd> <dt>

<span data-ttu-id="89049-662">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="89049-662">**Reset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-663">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="89049-663">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89049-664">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-664">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89049-665">Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) (Reset), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| Reset »)</span><span class="sxs-lookup"><span data-stu-id="89049-665">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) (Reset), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Reset")</span></span>
</dt> </dl>

<span data-ttu-id="89049-666">Chaîne de commande utilisée pour réinitialiser le modem pour l’appel suivant.</span><span class="sxs-lookup"><span data-stu-id="89049-666">Command string used to reset the modem for the next call.</span></span>

<span data-ttu-id="89049-667">Exemple : « AT&F »</span><span class="sxs-lookup"><span data-stu-id="89049-667">Example: "AT&F"</span></span>

</dd> <dt>

<span data-ttu-id="89049-668">**ResponsesKeyName**</span><span class="sxs-lookup"><span data-stu-id="89049-668">**ResponsesKeyName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-669">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="89049-669">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89049-670">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-670">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89049-671">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| ResponsesKeyName")</span><span class="sxs-lookup"><span data-stu-id="89049-671">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|ResponsesKeyName")</span></span>
</dt> </dl>

<span data-ttu-id="89049-672">Réponse : ce modem peut signaler au système d’exploitation pendant le processus de connexion.</span><span class="sxs-lookup"><span data-stu-id="89049-672">Response this modem might report to the operating system during the connection process.</span></span> <span data-ttu-id="89049-673">Les deux premiers caractères spécifient le type de réponse.</span><span class="sxs-lookup"><span data-stu-id="89049-673">The first two characters specify the type of response.</span></span> <span data-ttu-id="89049-674">Les deux deuxièmes caractères spécifient des informations sur la connexion établie.</span><span class="sxs-lookup"><span data-stu-id="89049-674">The second two characters specify information about the connection being made.</span></span> <span data-ttu-id="89049-675">Les deux deuxièmes caractères sont utilisés uniquement pour la progression de la négociation ou les codes de réponse de connexion.</span><span class="sxs-lookup"><span data-stu-id="89049-675">The second two characters are used only for Negotiation Progress or Connect response codes.</span></span> <span data-ttu-id="89049-676">Les huit caractères suivants spécifient la vitesse de ligne modem à modem négociée en bits par seconde (BPS).</span><span class="sxs-lookup"><span data-stu-id="89049-676">The next eight characters specify the modem-to-modem line speed negotiated in bits per second (bps).</span></span> <span data-ttu-id="89049-677">Les caractères représentent un format d’entier long non signé 32 bits (octet et mot inversé).</span><span class="sxs-lookup"><span data-stu-id="89049-677">The characters represent a 32-bit unsigned long integer format (byte and word reversed).</span></span> <span data-ttu-id="89049-678">Les huit derniers caractères indiquent que le modem passe à une vitesse de port ou d’équipement de terminal de données (DTE) différente.</span><span class="sxs-lookup"><span data-stu-id="89049-678">The last eight characters indicate that the modem is changing to a different port or Data Terminal Equipment (DTE) speed.</span></span> <span data-ttu-id="89049-679">En règle générale, ce champ n’est pas utilisé, car les modems effectuent des connexions à une vitesse de port verrouillé, quelle que soit la vitesse du modem à modem ou de l’équipement de communication de données (DCE).</span><span class="sxs-lookup"><span data-stu-id="89049-679">Usually this field is not used because modems make connections at a locked port speed regardless of the modem-to-modem or Data Communications Equipment (DCE) speed.</span></span>

</dd> <dt>

<span data-ttu-id="89049-680">**RingsBeforeAnswer**</span><span class="sxs-lookup"><span data-stu-id="89049-680">**RingsBeforeAnswer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-681">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="89049-681">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="89049-682">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-682">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89049-683">Nombre d’anneaux avant que le modem ne réponde à un appel entrant.</span><span class="sxs-lookup"><span data-stu-id="89049-683">Number of rings before the modem answers an incoming call.</span></span>

<span data-ttu-id="89049-684">Cette propriété est héritée de la [**\_ PotsModem CIM**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="89049-684">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="89049-685">**SpeakerModeDial**</span><span class="sxs-lookup"><span data-stu-id="89049-685">**SpeakerModeDial**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-686">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="89049-686">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89049-687">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-687">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89049-688">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| SpeakerModeDial")</span><span class="sxs-lookup"><span data-stu-id="89049-688">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|SpeakerModeDial")</span></span>
</dt> </dl>

<span data-ttu-id="89049-689">Chaîne de commande utilisée pour activer le haut-parleur du modem après avoir composé un nombre et éteindre l’orateur lorsqu’une connexion a été établie.</span><span class="sxs-lookup"><span data-stu-id="89049-689">Command string used to turn the modem speaker on after dialing a number, and turning the speaker off when a connection has been established.</span></span>

<span data-ttu-id="89049-690">Exemple : « M1 »</span><span class="sxs-lookup"><span data-stu-id="89049-690">Example: "M1"</span></span>

</dd> <dt>

<span data-ttu-id="89049-691">**SpeakerModeOff**</span><span class="sxs-lookup"><span data-stu-id="89049-691">**SpeakerModeOff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-692">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="89049-692">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89049-693">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-693">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89049-694">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| SpeakerModeOff")</span><span class="sxs-lookup"><span data-stu-id="89049-694">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|SpeakerModeOff")</span></span>
</dt> </dl>

<span data-ttu-id="89049-695">Chaîne de commande utilisée pour désactiver le haut-parleur du modem.</span><span class="sxs-lookup"><span data-stu-id="89049-695">Command string used to turn the modem speaker off.</span></span>

<span data-ttu-id="89049-696">Exemple : « M0 »</span><span class="sxs-lookup"><span data-stu-id="89049-696">Example: "M0"</span></span>

</dd> <dt>

<span data-ttu-id="89049-697">**SpeakerModeOn**</span><span class="sxs-lookup"><span data-stu-id="89049-697">**SpeakerModeOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-698">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="89049-698">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89049-699">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-699">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89049-700">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| SpeakerModeOn")</span><span class="sxs-lookup"><span data-stu-id="89049-700">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|SpeakerModeOn")</span></span>
</dt> </dl>

<span data-ttu-id="89049-701">Chaîne de commande utilisée pour activer le haut-parleur du modem.</span><span class="sxs-lookup"><span data-stu-id="89049-701">Command string used to turn the modem speaker on.</span></span>

<span data-ttu-id="89049-702">Exemple : "m2"</span><span class="sxs-lookup"><span data-stu-id="89049-702">Example: "M2"</span></span>

</dd> <dt>

<span data-ttu-id="89049-703">**SpeakerModeSetup**</span><span class="sxs-lookup"><span data-stu-id="89049-703">**SpeakerModeSetup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-704">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="89049-704">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89049-705">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-705">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89049-706">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| SpeakerModeSetup")</span><span class="sxs-lookup"><span data-stu-id="89049-706">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|SpeakerModeSetup")</span></span>
</dt> </dl>

<span data-ttu-id="89049-707">Chaîne de commande utilisée pour indiquer au modem d’allumer le haut-parleur (jusqu’à ce qu’une connexion soit établie).</span><span class="sxs-lookup"><span data-stu-id="89049-707">Command string used to instruct the modem to turn the speaker on (until a connection is established).</span></span>

<span data-ttu-id="89049-708">Exemple : « m3 »</span><span class="sxs-lookup"><span data-stu-id="89049-708">Example: "M3"</span></span>

</dd> <dt>

<span data-ttu-id="89049-709">**SpeakerVolumeHigh**</span><span class="sxs-lookup"><span data-stu-id="89049-709">**SpeakerVolumeHigh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-710">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="89049-710">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89049-711">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-711">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89049-712">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| SpeakerVolume \_ High")</span><span class="sxs-lookup"><span data-stu-id="89049-712">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|SpeakerVolume\_High")</span></span>
</dt> </dl>

<span data-ttu-id="89049-713">Chaîne de commande utilisée pour définir le haut-parleur du modem sur le volume le plus élevé.</span><span class="sxs-lookup"><span data-stu-id="89049-713">Command string used to set the modem speaker to the highest volume.</span></span>

<span data-ttu-id="89049-714">Exemple : « L3 »</span><span class="sxs-lookup"><span data-stu-id="89049-714">Example: "L3"</span></span>

</dd> <dt>

<span data-ttu-id="89049-715">**SpeakerVolumeInfo**</span><span class="sxs-lookup"><span data-stu-id="89049-715">**SpeakerVolumeInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-716">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="89049-716">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="89049-717">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-717">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89049-718">Décrit le niveau de volume des tonalités audibles du modem.</span><span class="sxs-lookup"><span data-stu-id="89049-718">Describes the volume level of the audible tones from the modem.</span></span>

<span data-ttu-id="89049-719">Cette propriété est héritée de la [**\_ PotsModem CIM**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="89049-719">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="89049-720">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="89049-720">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="89049-721">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="89049-721">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="89049-722">**Non pris en charge** (2)</span><span class="sxs-lookup"><span data-stu-id="89049-722">**Not Supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span data-ttu-id="89049-723">**Élevé** (3)</span><span class="sxs-lookup"><span data-stu-id="89049-723">**High** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>

<span data-ttu-id="89049-724">**Moyenne** (4)</span><span class="sxs-lookup"><span data-stu-id="89049-724">**Medium** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="89049-725">**Faible** (5)</span><span class="sxs-lookup"><span data-stu-id="89049-725">**Low** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>

<span data-ttu-id="89049-726">**Désactivé** (6)</span><span class="sxs-lookup"><span data-stu-id="89049-726">**Off** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>

<span data-ttu-id="89049-727">**Automatique** (7)</span><span class="sxs-lookup"><span data-stu-id="89049-727">**Auto** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="89049-728">**SpeakerVolumeLow**</span><span class="sxs-lookup"><span data-stu-id="89049-728">**SpeakerVolumeLow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-729">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="89049-729">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89049-730">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-730">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89049-731">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| SpeakerVolume \_ Low")</span><span class="sxs-lookup"><span data-stu-id="89049-731">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|SpeakerVolume\_Low")</span></span>
</dt> </dl>

<span data-ttu-id="89049-732">Chaîne de commande utilisée pour définir le haut-parleur du modem sur le volume le plus bas.</span><span class="sxs-lookup"><span data-stu-id="89049-732">Command string used to set the modem speaker to the lowest volume.</span></span>

<span data-ttu-id="89049-733">Exemple : « L1 »</span><span class="sxs-lookup"><span data-stu-id="89049-733">Example: "L1"</span></span>

</dd> <dt>

<span data-ttu-id="89049-734">**SpeakerVolumeMed**</span><span class="sxs-lookup"><span data-stu-id="89049-734">**SpeakerVolumeMed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-735">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="89049-735">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89049-736">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-736">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89049-737">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| SpeakerVolume \_ med")</span><span class="sxs-lookup"><span data-stu-id="89049-737">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|SpeakerVolume\_Med")</span></span>
</dt> </dl>

<span data-ttu-id="89049-738">Chaîne de commande utilisée pour définir le haut-parleur du modem sur un volume moyen.</span><span class="sxs-lookup"><span data-stu-id="89049-738">Command string used to set the modem speaker to a medium volume.</span></span>

<span data-ttu-id="89049-739">Exemple : « L2 »</span><span class="sxs-lookup"><span data-stu-id="89049-739">Example: "L2"</span></span>

</dd> <dt>

<span data-ttu-id="89049-740">**État**</span><span class="sxs-lookup"><span data-stu-id="89049-740">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-741">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="89049-741">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89049-742">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-742">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89049-743">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="89049-743">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="89049-744">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="89049-744">Current status of the object.</span></span> <span data-ttu-id="89049-745">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="89049-745">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="89049-746">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="89049-746">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="89049-747">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="89049-747">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="89049-748">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="89049-748">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="89049-749">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="89049-749">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="89049-750">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="89049-750">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="89049-751">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="89049-751">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="89049-752">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="89049-752">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="89049-753">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="89049-753">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="89049-754">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="89049-754">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="89049-755">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="89049-755">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="89049-756">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="89049-756">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="89049-757">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="89049-757">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="89049-758">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="89049-758">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="89049-759">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="89049-759">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="89049-760">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="89049-760">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="89049-761">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="89049-761">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="89049-762">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="89049-762">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="89049-763">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="89049-763">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="89049-764">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="89049-764">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-765">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="89049-765">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="89049-766">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-766">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89049-767">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="89049-767">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="89049-768">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="89049-768">State of the logical device.</span></span> <span data-ttu-id="89049-769">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (non applicable) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="89049-769">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="89049-770">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="89049-770">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="89049-771">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="89049-771">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="89049-772">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="89049-772">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="89049-773">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="89049-773">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="89049-774">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="89049-774">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="89049-775">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="89049-775">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="89049-776">**StringFormat**</span><span class="sxs-lookup"><span data-stu-id="89049-776">**StringFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-777">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="89049-777">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89049-778">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-778">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89049-779">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32 \_ API \| line Device structures \| LINEDEVCAPS \| dwStringFormat")</span><span class="sxs-lookup"><span data-stu-id="89049-779">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Line Device Structures\|LINEDEVCAPS\|dwStringFormat")</span></span>
</dt> </dl>

<span data-ttu-id="89049-780">Type de caractères utilisé pour le texte transmis par le modem.</span><span class="sxs-lookup"><span data-stu-id="89049-780">Type of characters used for text passed through the modem.</span></span>

<span data-ttu-id="89049-781">Les valeurs sont :</span><span class="sxs-lookup"><span data-stu-id="89049-781">The values are:</span></span>

<dl> <dd><span data-ttu-id="89049-782">"Format de chaîne ASCII"</span><span class="sxs-lookup"><span data-stu-id="89049-782">"ASCII string format"</span></span></dd> <dd><span data-ttu-id="89049-783">« Format de chaîne DBCS »</span><span class="sxs-lookup"><span data-stu-id="89049-783">"DBCS string format"</span></span></dd> <dd><span data-ttu-id="89049-784">« Format de chaîne UNICODE »</span><span class="sxs-lookup"><span data-stu-id="89049-784">"UNICODE string format"</span></span></dd> </dl>

<dt>

<span id="ASCII_string_format"></span><span id="ascii_string_format"></span><span id="ASCII_STRING_FORMAT"></span>

<span data-ttu-id="89049-785">**Format de chaîne ASCII** (« format de chaîne ASCII »)</span><span class="sxs-lookup"><span data-stu-id="89049-785">**ASCII string format** ("ASCII string format")</span></span>


</dt> <dd></dd> <dt>

<span id="DBCS_string_format"></span><span id="dbcs_string_format"></span><span id="DBCS_STRING_FORMAT"></span>

<span data-ttu-id="89049-786">**Format de chaîne DBCS** (« format de chaîne DBCS »)</span><span class="sxs-lookup"><span data-stu-id="89049-786">**DBCS string format** ("DBCS string format")</span></span>


</dt> <dd></dd> <dt>

<span id="UNICODE_string_format"></span><span id="unicode_string_format"></span><span id="UNICODE_STRING_FORMAT"></span>

<span data-ttu-id="89049-787">**Format de chaîne Unicode** (« format de chaîne Unicode »)</span><span class="sxs-lookup"><span data-stu-id="89049-787">**UNICODE string format** ("UNICODE string format")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="89049-788">**SupportsCallback**</span><span class="sxs-lookup"><span data-stu-id="89049-788">**SupportsCallback**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-789">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="89049-789">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="89049-790">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-790">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89049-791">Si la **valeur est true**, le modem prend en charge le rappel.</span><span class="sxs-lookup"><span data-stu-id="89049-791">If **TRUE**, the modem supports callback.</span></span>

<span data-ttu-id="89049-792">Cette propriété est héritée de la [**\_ PotsModem CIM**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="89049-792">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="89049-793">**SupportsSynchronousConnect**</span><span class="sxs-lookup"><span data-stu-id="89049-793">**SupportsSynchronousConnect**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-794">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="89049-794">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="89049-795">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-795">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89049-796">Si la **valeur est true**, synchrone, et asynchrone, la communication est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="89049-796">If **TRUE**, synchronous, as well as asynchronous, communication is supported.</span></span>

<span data-ttu-id="89049-797">Cette propriété est héritée de la [**\_ PotsModem CIM**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="89049-797">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="89049-798">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="89049-798">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-799">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="89049-799">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89049-800">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-800">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89049-801">Qualificateurs : [**Propaged**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="89049-801">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="89049-802">Valeur de la propriété **CreationClassName** de l’ordinateur d’étendue.</span><span class="sxs-lookup"><span data-stu-id="89049-802">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="89049-803">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="89049-803">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="89049-804">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="89049-804">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-805">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="89049-805">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89049-806">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-806">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89049-807">Qualificateurs : [**Propaged**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="89049-807">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="89049-808">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="89049-808">Name of the scoping system.</span></span>

<span data-ttu-id="89049-809">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="89049-809">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="89049-810">**Indicateur de fin**</span><span class="sxs-lookup"><span data-stu-id="89049-810">**Terminator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-811">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="89049-811">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89049-812">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-812">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89049-813">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| Terminator")</span><span class="sxs-lookup"><span data-stu-id="89049-813">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Terminator")</span></span>
</dt> </dl>

<span data-ttu-id="89049-814">Chaîne qui marque la fin d’une chaîne de commande.</span><span class="sxs-lookup"><span data-stu-id="89049-814">String that marks the end of a command string.</span></span>

<span data-ttu-id="89049-815">Exemple : « <CR »</span><span class="sxs-lookup"><span data-stu-id="89049-815">Example: "<cr"</span></span>

</dd> <dt>

<span data-ttu-id="89049-816">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="89049-816">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-817">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="89049-817">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="89049-818">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-818">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89049-819">Date et heure de la dernière réinitialisation du modem.</span><span class="sxs-lookup"><span data-stu-id="89049-819">Date and time the modem was last reset.</span></span>

<span data-ttu-id="89049-820">Cette propriété est héritée de la [**\_ PotsModem CIM**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="89049-820">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="89049-821">**Ton**</span><span class="sxs-lookup"><span data-stu-id="89049-821">**Tone**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-822">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="89049-822">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89049-823">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-823">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89049-824">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| Tone")</span><span class="sxs-lookup"><span data-stu-id="89049-824">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Tone")</span></span>
</dt> </dl>

<span data-ttu-id="89049-825">Chaîne de commande qui indique au modem d’utiliser le mode de tonalité pour la numérotation.</span><span class="sxs-lookup"><span data-stu-id="89049-825">Command string that instructs the modem to use tone mode for dialing.</span></span> <span data-ttu-id="89049-826">La ligne téléphonique doit prendre en charge la numérotation par tonalité.</span><span class="sxs-lookup"><span data-stu-id="89049-826">The phone line must support tone dialing.</span></span>

<span data-ttu-id="89049-827">Exemple : « T »</span><span class="sxs-lookup"><span data-stu-id="89049-827">Example: "T"</span></span>

</dd> <dt>

<span data-ttu-id="89049-828">**VoiceSwitchFeature**</span><span class="sxs-lookup"><span data-stu-id="89049-828">**VoiceSwitchFeature**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89049-829">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="89049-829">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89049-830">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89049-830">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89049-831">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| VoiceSwitchFeature")</span><span class="sxs-lookup"><span data-stu-id="89049-831">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|VoiceSwitchFeature")</span></span>
</dt> </dl>

<span data-ttu-id="89049-832">Chaînes de commande utilisées pour activer les fonctionnalités vocales d’un modem vocal.</span><span class="sxs-lookup"><span data-stu-id="89049-832">Command strings used to activate the voice capabilities of a voice modem.</span></span>

<span data-ttu-id="89049-833">Exemple : « AT + V »</span><span class="sxs-lookup"><span data-stu-id="89049-833">Example: "AT+V"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="89049-834">Notes</span><span class="sxs-lookup"><span data-stu-id="89049-834">Remarks</span></span>

<span data-ttu-id="89049-835">La classe **Win32 \_ POTSModem** est dérivée de [**CIM \_ POTSModem**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="89049-835">The **Win32\_POTSModem** class is derived from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="89049-836">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="89049-836">Requirements</span></span>



| <span data-ttu-id="89049-837">Condition requise</span><span class="sxs-lookup"><span data-stu-id="89049-837">Requirement</span></span> | <span data-ttu-id="89049-838">Valeur</span><span class="sxs-lookup"><span data-stu-id="89049-838">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="89049-839">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="89049-839">Minimum supported client</span></span><br/> | <span data-ttu-id="89049-840">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="89049-840">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="89049-841">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="89049-841">Minimum supported server</span></span><br/> | <span data-ttu-id="89049-842">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="89049-842">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="89049-843">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="89049-843">Namespace</span></span><br/>                | <span data-ttu-id="89049-844">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="89049-844">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="89049-845">MOF</span><span class="sxs-lookup"><span data-stu-id="89049-845">MOF</span></span><br/>                      | <dl> <span data-ttu-id="89049-846"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="89049-846"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="89049-847">DLL</span><span class="sxs-lookup"><span data-stu-id="89049-847">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89049-848"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89049-848"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89049-849">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="89049-849">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89049-850">**\_POTSMODEM CIM**</span><span class="sxs-lookup"><span data-stu-id="89049-850">**CIM\_PotsModem**</span></span>](cim-potsmodem.md)
</dt> <dt>

[<span data-ttu-id="89049-851">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="89049-851">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
