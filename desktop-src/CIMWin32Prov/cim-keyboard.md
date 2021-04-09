---
description: La \_ classe de clavier CIM représente les fonctionnalités et la gestion du périphérique logique du clavier.
ms.assetid: c465a731-03dd-4418-8b16-96dc2c8b60b5
ms.tgt_platform: multiple
title: Classe CIM_Keyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Keyboard
- CIM_Keyboard.Availability
- CIM_Keyboard.Caption
- CIM_Keyboard.ConfigManagerErrorCode
- CIM_Keyboard.ConfigManagerUserConfig
- CIM_Keyboard.CreationClassName
- CIM_Keyboard.Description
- CIM_Keyboard.DeviceID
- CIM_Keyboard.ErrorCleared
- CIM_Keyboard.ErrorDescription
- CIM_Keyboard.InstallDate
- CIM_Keyboard.IsLocked
- CIM_Keyboard.LastErrorCode
- CIM_Keyboard.Layout
- CIM_Keyboard.Name
- CIM_Keyboard.NumberOfFunctionKeys
- CIM_Keyboard.Password
- CIM_Keyboard.PNPDeviceID
- CIM_Keyboard.PowerManagementCapabilities
- CIM_Keyboard.PowerManagementSupported
- CIM_Keyboard.Status
- CIM_Keyboard.StatusInfo
- CIM_Keyboard.SystemCreationClassName
- CIM_Keyboard.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7424601632a9d6a0bedcbcde7ab3c27cf27c69cb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110835"
---
# <a name="cim_keyboard-class"></a><span data-ttu-id="11d89-103">\_Classe de clavier CIM</span><span class="sxs-lookup"><span data-stu-id="11d89-103">CIM\_Keyboard class</span></span>

<span data-ttu-id="11d89-104">La classe de **\_ clavier CIM** représente les fonctionnalités et la gestion du périphérique logique du clavier.</span><span class="sxs-lookup"><span data-stu-id="11d89-104">The **CIM\_Keyboard** class represents the capabilities and management of the keyboard logical device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="11d89-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="11d89-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="11d89-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="11d89-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="11d89-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="11d89-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="11d89-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="11d89-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="11d89-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="11d89-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C534-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Keyboard : CIM_UserDevice
{
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  boolean  IsLocked;
  uint32   LastErrorCode;
  string   Layout;
  string   Name;
  uint16   NumberOfFunctionKeys;
  uint16   Password;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="11d89-110">Membres</span><span class="sxs-lookup"><span data-stu-id="11d89-110">Members</span></span>

<span data-ttu-id="11d89-111">La classe de **\_ clavier CIM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="11d89-111">The **CIM\_Keyboard** class has these types of members:</span></span>

-   [<span data-ttu-id="11d89-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="11d89-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="11d89-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="11d89-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="11d89-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="11d89-114">Methods</span></span>

<span data-ttu-id="11d89-115">La classe de **\_ clavier CIM** présente ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="11d89-115">The **CIM\_Keyboard** class has these methods.</span></span>



| <span data-ttu-id="11d89-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="11d89-116">Method</span></span>                                                              | <span data-ttu-id="11d89-117">Description</span><span class="sxs-lookup"><span data-stu-id="11d89-117">Description</span></span>                                                                                                                              |
|:--------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="11d89-118">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="11d89-118">**Reset**</span></span>](reset-method-in-class-cim-keyboard.md)                 | <span data-ttu-id="11d89-119">Demande la réinitialisation de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="11d89-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="11d89-120">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="11d89-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="11d89-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="11d89-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-keyboard.md) | <span data-ttu-id="11d89-122">Définit l’état d’alimentation souhaité pour un périphérique logique et lorsqu’un appareil doit être placé dans cet État.</span><span class="sxs-lookup"><span data-stu-id="11d89-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="11d89-123">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="11d89-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="11d89-124">Propriétés</span><span class="sxs-lookup"><span data-stu-id="11d89-124">Properties</span></span>

<span data-ttu-id="11d89-125">La classe de **\_ clavier CIM** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="11d89-125">The **CIM\_Keyboard** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="11d89-126">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="11d89-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11d89-127">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="11d89-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="11d89-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="11d89-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11d89-129">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="11d89-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="11d89-130">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="11d89-130">Availability and status of the device.</span></span>

<span data-ttu-id="11d89-131">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="11d89-131">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="11d89-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="11d89-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="11d89-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="11d89-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="11d89-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="11d89-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="11d89-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="11d89-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="11d89-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="11d89-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="11d89-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="11d89-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="11d89-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="11d89-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="11d89-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="11d89-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="11d89-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="11d89-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="11d89-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="11d89-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="11d89-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="11d89-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="11d89-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="11d89-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="11d89-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="11d89-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="11d89-145">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="11d89-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="11d89-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="11d89-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="11d89-147">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="11d89-147">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="11d89-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="11d89-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="11d89-149">L’appareil ne fonctionne pas mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="11d89-149">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="11d89-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="11d89-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="11d89-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="11d89-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="11d89-152">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="11d89-152">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="11d89-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="11d89-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="11d89-154">L’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="11d89-154">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="11d89-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="11d89-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="11d89-156">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="11d89-156">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="11d89-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="11d89-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="11d89-158">L’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="11d89-158">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="11d89-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="11d89-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="11d89-160">L’appareil est calme.</span><span class="sxs-lookup"><span data-stu-id="11d89-160">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="11d89-161">**Caption**</span><span class="sxs-lookup"><span data-stu-id="11d89-161">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11d89-162">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="11d89-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11d89-163">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="11d89-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11d89-164">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="11d89-164">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="11d89-165">Courte description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="11d89-165">Short textual description of the object.</span></span>

<span data-ttu-id="11d89-166">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="11d89-166">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="11d89-167">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="11d89-167">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11d89-168">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="11d89-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="11d89-169">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="11d89-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11d89-170">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="11d89-170">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="11d89-171">Code d’erreur Configuration Manager Win32.</span><span class="sxs-lookup"><span data-stu-id="11d89-171">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="11d89-172">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="11d89-172">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="11d89-173"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="11d89-173"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="11d89-174"> (0)</span><span class="sxs-lookup"><span data-stu-id="11d89-174">(0)</span></span>


</dt> <dd>

<span data-ttu-id="11d89-175">L’appareil fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="11d89-175">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="11d89-176"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="11d89-176"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="11d89-177">(1)</span><span class="sxs-lookup"><span data-stu-id="11d89-177">(1)</span></span>


</dt> <dd>

<span data-ttu-id="11d89-178">L’appareil n’est pas configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="11d89-178">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="11d89-179"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="11d89-179"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="11d89-180">(2)</span><span class="sxs-lookup"><span data-stu-id="11d89-180">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="11d89-181"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="11d89-181"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="11d89-182">(3)</span><span class="sxs-lookup"><span data-stu-id="11d89-182">(3)</span></span>


</dt> <dd>

<span data-ttu-id="11d89-183">Le pilote de cet appareil est peut-être endommagé ou la mémoire ou d’autres ressources du système sont peut-être insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="11d89-183">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="11d89-184"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="11d89-184"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="11d89-185">(4)</span><span class="sxs-lookup"><span data-stu-id="11d89-185">(4)</span></span>


</dt> <dd>

<span data-ttu-id="11d89-186">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="11d89-186">Device is not working properly.</span></span> <span data-ttu-id="11d89-187">L’un de ses pilotes ou le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="11d89-187">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="11d89-188"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="11d89-188"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="11d89-189">(5)</span><span class="sxs-lookup"><span data-stu-id="11d89-189">(5)</span></span>


</dt> <dd>

<span data-ttu-id="11d89-190">Le pilote de l’appareil requiert une ressource que Windows ne peut pas gérer.</span><span class="sxs-lookup"><span data-stu-id="11d89-190">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="11d89-191"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="11d89-191"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="11d89-192"> (6)</span><span class="sxs-lookup"><span data-stu-id="11d89-192">(6)</span></span>


</dt> <dd>

<span data-ttu-id="11d89-193">La configuration de démarrage de l’appareil est en conflit avec d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="11d89-193">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="11d89-194"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="11d89-194"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="11d89-195">(7)</span><span class="sxs-lookup"><span data-stu-id="11d89-195">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="11d89-196"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="11d89-196"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="11d89-197">(8)</span><span class="sxs-lookup"><span data-stu-id="11d89-197">(8)</span></span>


</dt> <dd>

<span data-ttu-id="11d89-198">Le chargeur de pilote de l’appareil est manquant.</span><span class="sxs-lookup"><span data-stu-id="11d89-198">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="11d89-199"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="11d89-199"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="11d89-200">(9)</span><span class="sxs-lookup"><span data-stu-id="11d89-200">(9)</span></span>


</dt> <dd>

<span data-ttu-id="11d89-201">L’appareil ne fonctionne pas correctement ; le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="11d89-201">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="11d89-202"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="11d89-202"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="11d89-203">(10)</span><span class="sxs-lookup"><span data-stu-id="11d89-203">(10)</span></span>


</dt> <dd>

<span data-ttu-id="11d89-204">Impossible de démarrer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="11d89-204">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="11d89-205"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="11d89-205"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="11d89-206">(11)</span><span class="sxs-lookup"><span data-stu-id="11d89-206">(11)</span></span>


</dt> <dd>

<span data-ttu-id="11d89-207">Échec de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="11d89-207">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="11d89-208"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="11d89-208"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="11d89-209">douze</span><span class="sxs-lookup"><span data-stu-id="11d89-209">(12)</span></span>


</dt> <dd>

<span data-ttu-id="11d89-210">L’appareil ne peut pas trouver suffisamment de ressources libres à utiliser.</span><span class="sxs-lookup"><span data-stu-id="11d89-210">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="11d89-211"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="11d89-211"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="11d89-212">(13)</span><span class="sxs-lookup"><span data-stu-id="11d89-212">(13)</span></span>


</dt> <dd>

<span data-ttu-id="11d89-213">Windows ne peut pas vérifier les ressources de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="11d89-213">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="11d89-214"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="11d89-214"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="11d89-215">(14)</span><span class="sxs-lookup"><span data-stu-id="11d89-215">(14)</span></span>


</dt> <dd>

<span data-ttu-id="11d89-216">L’appareil ne peut pas fonctionner correctement tant que l’ordinateur n’a pas redémarré.</span><span class="sxs-lookup"><span data-stu-id="11d89-216">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="11d89-217"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="11d89-217"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="11d89-218">(15)</span><span class="sxs-lookup"><span data-stu-id="11d89-218">(15)</span></span>


</dt> <dd>

<span data-ttu-id="11d89-219">L’appareil ne fonctionne pas correctement en raison d’un éventuel problème de réénumération.</span><span class="sxs-lookup"><span data-stu-id="11d89-219">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="11d89-220"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="11d89-220"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="11d89-221">(16)</span><span class="sxs-lookup"><span data-stu-id="11d89-221">(16)</span></span>


</dt> <dd>

<span data-ttu-id="11d89-222">Windows ne peut pas identifier toutes les ressources utilisées par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="11d89-222">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="11d89-223"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="11d89-223"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="11d89-224">(17)</span><span class="sxs-lookup"><span data-stu-id="11d89-224">(17)</span></span>


</dt> <dd>

<span data-ttu-id="11d89-225">L’appareil demande un type de ressource inconnu.</span><span class="sxs-lookup"><span data-stu-id="11d89-225">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="11d89-226"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="11d89-226"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="11d89-227">(18)</span><span class="sxs-lookup"><span data-stu-id="11d89-227">(18)</span></span>


</dt> <dd>

<span data-ttu-id="11d89-228">Les pilotes de périphérique doivent être réinstallés.</span><span class="sxs-lookup"><span data-stu-id="11d89-228">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="11d89-229"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="11d89-229"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="11d89-230">(19)</span><span class="sxs-lookup"><span data-stu-id="11d89-230">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="11d89-231"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="11d89-231"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="11d89-232">(20)</span><span class="sxs-lookup"><span data-stu-id="11d89-232">(20)</span></span>


</dt> <dd>

<span data-ttu-id="11d89-233">Le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="11d89-233">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="11d89-234"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="11d89-234"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="11d89-235">(21)</span><span class="sxs-lookup"><span data-stu-id="11d89-235">(21)</span></span>


</dt> <dd>

<span data-ttu-id="11d89-236">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="11d89-236">System failure.</span></span> <span data-ttu-id="11d89-237">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="11d89-237">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="11d89-238">Windows supprime l’appareil.</span><span class="sxs-lookup"><span data-stu-id="11d89-238">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="11d89-239"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="11d89-239"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="11d89-240">(22)</span><span class="sxs-lookup"><span data-stu-id="11d89-240">(22)</span></span>


</dt> <dd>

<span data-ttu-id="11d89-241">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="11d89-241">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="11d89-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="11d89-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="11d89-243">(23)</span><span class="sxs-lookup"><span data-stu-id="11d89-243">(23)</span></span>


</dt> <dd>

<span data-ttu-id="11d89-244">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="11d89-244">System failure.</span></span> <span data-ttu-id="11d89-245">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="11d89-245">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="11d89-246"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="11d89-246"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="11d89-247">(24)</span><span class="sxs-lookup"><span data-stu-id="11d89-247">(24)</span></span>


</dt> <dd>

<span data-ttu-id="11d89-248">L’appareil n’est pas présent, ne fonctionne pas correctement ou n’a pas tous ses pilotes installés.</span><span class="sxs-lookup"><span data-stu-id="11d89-248">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="11d89-249"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="11d89-249"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="11d89-250">(25)</span><span class="sxs-lookup"><span data-stu-id="11d89-250">(25)</span></span>


</dt> <dd>

<span data-ttu-id="11d89-251">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="11d89-251">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="11d89-252"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="11d89-252"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="11d89-253">(26)</span><span class="sxs-lookup"><span data-stu-id="11d89-253">(26)</span></span>


</dt> <dd>

<span data-ttu-id="11d89-254">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="11d89-254">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="11d89-255"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="11d89-255"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="11d89-256">(27)</span><span class="sxs-lookup"><span data-stu-id="11d89-256">(27)</span></span>


</dt> <dd>

<span data-ttu-id="11d89-257">L’appareil n’a pas une configuration de journal valide.</span><span class="sxs-lookup"><span data-stu-id="11d89-257">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="11d89-258"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="11d89-258"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="11d89-259">(28)</span><span class="sxs-lookup"><span data-stu-id="11d89-259">(28)</span></span>


</dt> <dd>

<span data-ttu-id="11d89-260">Les pilotes de périphérique ne sont pas installés.</span><span class="sxs-lookup"><span data-stu-id="11d89-260">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="11d89-261"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="11d89-261"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="11d89-262">(29)</span><span class="sxs-lookup"><span data-stu-id="11d89-262">(29)</span></span>


</dt> <dd>

<span data-ttu-id="11d89-263">L’appareil est désactivé ; le microprogramme de l’appareil n’a pas fourni les ressources requises.</span><span class="sxs-lookup"><span data-stu-id="11d89-263">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="11d89-264"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="11d89-264"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="11d89-265">(30)</span><span class="sxs-lookup"><span data-stu-id="11d89-265">(30)</span></span>


</dt> <dd>

<span data-ttu-id="11d89-266">L’appareil utilise une ressource IRQ qu’un autre appareil utilise.</span><span class="sxs-lookup"><span data-stu-id="11d89-266">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="11d89-267"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="11d89-267"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="11d89-268">31</span><span class="sxs-lookup"><span data-stu-id="11d89-268">(31)</span></span>


</dt> <dd>

<span data-ttu-id="11d89-269">L’appareil ne fonctionne pas correctement ; Windows ne peut pas charger les pilotes de périphérique requis.</span><span class="sxs-lookup"><span data-stu-id="11d89-269">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="11d89-270">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="11d89-270">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11d89-271">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="11d89-271">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="11d89-272">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="11d89-272">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11d89-273">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="11d89-273">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="11d89-274">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="11d89-274">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="11d89-275">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="11d89-275">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="11d89-276">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="11d89-276">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11d89-277">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="11d89-277">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11d89-278">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="11d89-278">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11d89-279">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="11d89-279">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="11d89-280">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="11d89-280">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="11d89-281">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="11d89-281">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="11d89-282">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="11d89-282">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="11d89-283">**Description**</span><span class="sxs-lookup"><span data-stu-id="11d89-283">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11d89-284">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="11d89-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11d89-285">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="11d89-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11d89-286">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="11d89-286">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="11d89-287">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="11d89-287">Textual description of the object.</span></span>

<span data-ttu-id="11d89-288">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="11d89-288">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="11d89-289">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="11d89-289">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11d89-290">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="11d89-290">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11d89-291">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="11d89-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11d89-292">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="11d89-292">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="11d89-293">Adresse ou d’autres informations d’identification pour nommer de manière unique l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="11d89-293">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="11d89-294">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="11d89-294">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="11d89-295">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="11d89-295">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11d89-296">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="11d89-296">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="11d89-297">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="11d89-297">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11d89-298">Si la **valeur est true**, l’erreur signalée dans la propriété **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="11d89-298">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="11d89-299">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="11d89-299">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="11d89-300">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="11d89-300">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11d89-301">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="11d89-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11d89-302">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="11d89-302">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11d89-303">Chaîne de forme libre qui fournit des informations sur l’erreur enregistrée dans la propriété **LastErrorCode** et les actions correctives à entreprendre.</span><span class="sxs-lookup"><span data-stu-id="11d89-303">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to take.</span></span>

<span data-ttu-id="11d89-304">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="11d89-304">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="11d89-305">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="11d89-305">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11d89-306">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="11d89-306">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="11d89-307">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="11d89-307">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11d89-308">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="11d89-308">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="11d89-309">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="11d89-309">Date and time the object was installed.</span></span> <span data-ttu-id="11d89-310">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="11d89-310">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="11d89-311">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="11d89-311">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="11d89-312">**IsLocked**</span><span class="sxs-lookup"><span data-stu-id="11d89-312">**IsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11d89-313">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="11d89-313">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="11d89-314">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="11d89-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11d89-315">Si la **valeur est true**, l’appareil est verrouillé, ce qui empêche l’entrée ou la sortie de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="11d89-315">If **TRUE**, the device is locked, preventing user input or output.</span></span>

<span data-ttu-id="11d89-316">Cette propriété est héritée de la [**\_ UserDevice CIM**](cim-userdevice.md).</span><span class="sxs-lookup"><span data-stu-id="11d89-316">This property is inherited from [**CIM\_UserDevice**](cim-userdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="11d89-317">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="11d89-317">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11d89-318">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="11d89-318">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="11d89-319">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="11d89-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11d89-320">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="11d89-320">Last error code reported by the logical device.</span></span>

<span data-ttu-id="11d89-321">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="11d89-321">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="11d89-322">**Disposition**</span><span class="sxs-lookup"><span data-stu-id="11d89-322">**Layout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11d89-323">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="11d89-323">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11d89-324">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="11d89-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11d89-325">Chaîne de forme libre qui indique le format et la mise en page du clavier.</span><span class="sxs-lookup"><span data-stu-id="11d89-325">Free-form string that indicates the format and layout of the keyboard.</span></span>

</dd> <dt>

<span data-ttu-id="11d89-326">**Nom**</span><span class="sxs-lookup"><span data-stu-id="11d89-326">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11d89-327">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="11d89-327">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11d89-328">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="11d89-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11d89-329">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="11d89-329">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="11d89-330">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="11d89-330">Label by which the object is known.</span></span> <span data-ttu-id="11d89-331">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="11d89-331">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="11d89-332">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="11d89-332">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="11d89-333">**NumberOfFunctionKeys**</span><span class="sxs-lookup"><span data-stu-id="11d89-333">**NumberOfFunctionKeys**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11d89-334">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="11d89-334">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="11d89-335">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="11d89-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11d89-336">Nombre de touches de fonction sur le clavier.</span><span class="sxs-lookup"><span data-stu-id="11d89-336">Number of function keys on the keyboard.</span></span>

</dd> <dt>

<span data-ttu-id="11d89-337">**Mot de passe**</span><span class="sxs-lookup"><span data-stu-id="11d89-337">**Password**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11d89-338">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="11d89-338">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="11d89-339">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="11d89-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11d89-340">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| System Hardware Security \| 001,2»)</span><span class="sxs-lookup"><span data-stu-id="11d89-340">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Hardware Security\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="11d89-341">Entier qui indique si un mot de passe de niveau matériel est activé sur le clavier pour empêcher une entrée locale.</span><span class="sxs-lookup"><span data-stu-id="11d89-341">Integer that indicates whether a hardware-level password is enabled on the keyboard to prevent local input.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="11d89-342">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="11d89-342">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="11d89-343">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="11d89-343">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="11d89-344">**Désactivé** (3)</span><span class="sxs-lookup"><span data-stu-id="11d89-344">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="11d89-345">**Activé** (4)</span><span class="sxs-lookup"><span data-stu-id="11d89-345">**Enabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

<span data-ttu-id="11d89-346">**Non implémenté** (5)</span><span class="sxs-lookup"><span data-stu-id="11d89-346">**Not Implemented** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="11d89-347">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="11d89-347">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11d89-348">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="11d89-348">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11d89-349">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="11d89-349">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11d89-350">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="11d89-350">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="11d89-351">Win32 Plug-and-Play identificateur du périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="11d89-351">Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="11d89-352">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="11d89-352">Example: "\*PNP030b"</span></span>

<span data-ttu-id="11d89-353">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="11d89-353">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="11d89-354">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="11d89-354">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11d89-355">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="11d89-355">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="11d89-356">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="11d89-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11d89-357">Tableau des fonctionnalités d’alimentation spécifiques d’un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="11d89-357">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="11d89-358">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="11d89-358">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="11d89-359"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="11d89-359"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="11d89-360"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="11d89-360"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="11d89-361"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="11d89-361"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="11d89-362"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="11d89-362"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="11d89-363">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="11d89-363">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="11d89-364"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="11d89-364"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="11d89-365">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="11d89-365">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="11d89-366"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="11d89-366"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="11d89-367">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="11d89-367">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="11d89-368">Cette méthode se trouve sur la classe parente du **\_ LogicalDevice CIM** et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="11d89-368">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="11d89-369">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="11d89-369">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="11d89-370"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="11d89-370"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="11d89-371">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation).</span><span class="sxs-lookup"><span data-stu-id="11d89-371">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="11d89-372"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="11d89-372"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="11d89-373">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation) et l' *heure* définie sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="11d89-373">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="11d89-374">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="11d89-374">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11d89-375">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="11d89-375">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="11d89-376">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="11d89-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11d89-377">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation, c’est-à-dire être mis en état d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="11d89-377">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="11d89-378">Si la valeur est **false**, la valeur entière 1 (« non pris en charge ») doit être la seule entrée dans le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="11d89-378">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="11d89-379">Cette propriété n’indique pas si les fonctionnalités de gestion de l’alimentation sont actuellement activées, ou si elles sont activées, quelles sont les fonctionnalités prises en charge.</span><span class="sxs-lookup"><span data-stu-id="11d89-379">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="11d89-380">Pour plus d’informations, consultez le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="11d89-380">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="11d89-381">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="11d89-381">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="11d89-382">**État**</span><span class="sxs-lookup"><span data-stu-id="11d89-382">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11d89-383">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="11d89-383">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11d89-384">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="11d89-384">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11d89-385">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="11d89-385">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="11d89-386">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="11d89-386">Current status of the object.</span></span>

<span data-ttu-id="11d89-387">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="11d89-387">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="11d89-388">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="11d89-388">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="11d89-389">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="11d89-389">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="11d89-390">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="11d89-390">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="11d89-391">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="11d89-391">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="11d89-392">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="11d89-392">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="11d89-393">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="11d89-393">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="11d89-394">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="11d89-394">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="11d89-395">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="11d89-395">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="11d89-396">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="11d89-396">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="11d89-397">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="11d89-397">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="11d89-398">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="11d89-398">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="11d89-399">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="11d89-399">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="11d89-400">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="11d89-400">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="11d89-401">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="11d89-401">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11d89-402">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="11d89-402">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="11d89-403">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="11d89-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11d89-404">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="11d89-404">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="11d89-405">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="11d89-405">State of the logical device.</span></span> <span data-ttu-id="11d89-406">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (non applicable) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="11d89-406">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="11d89-407">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="11d89-407">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="11d89-408">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="11d89-408">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="11d89-409">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="11d89-409">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="11d89-410">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="11d89-410">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="11d89-411">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="11d89-411">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="11d89-412">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="11d89-412">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="11d89-413">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="11d89-413">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11d89-414">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="11d89-414">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11d89-415">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="11d89-415">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11d89-416">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="11d89-416">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="11d89-417">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="11d89-417">Scoping system's creation class name.</span></span>

<span data-ttu-id="11d89-418">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="11d89-418">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="11d89-419">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="11d89-419">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11d89-420">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="11d89-420">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11d89-421">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="11d89-421">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11d89-422">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="11d89-422">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="11d89-423">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="11d89-423">Scoping system's name.</span></span>

<span data-ttu-id="11d89-424">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="11d89-424">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="11d89-425">Notes</span><span class="sxs-lookup"><span data-stu-id="11d89-425">Remarks</span></span>

<span data-ttu-id="11d89-426">La classe de **\_ clavier CIM** est dérivée de la [**\_ UserDevice CIM**](cim-userdevice.md).</span><span class="sxs-lookup"><span data-stu-id="11d89-426">The **CIM\_Keyboard** class is derived from [**CIM\_UserDevice**](cim-userdevice.md).</span></span>

<span data-ttu-id="11d89-427">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="11d89-427">WMI does not implement this class.</span></span> <span data-ttu-id="11d89-428">Pour les classes dérivées du **\_ clavier CIM**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="11d89-428">For classes derived from **CIM\_Keyboard**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="11d89-429">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="11d89-429">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="11d89-430">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="11d89-430">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="11d89-431">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="11d89-431">Requirements</span></span>



| <span data-ttu-id="11d89-432">Condition requise</span><span class="sxs-lookup"><span data-stu-id="11d89-432">Requirement</span></span> | <span data-ttu-id="11d89-433">Valeur</span><span class="sxs-lookup"><span data-stu-id="11d89-433">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="11d89-434">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="11d89-434">Minimum supported client</span></span><br/> | <span data-ttu-id="11d89-435">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="11d89-435">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="11d89-436">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="11d89-436">Minimum supported server</span></span><br/> | <span data-ttu-id="11d89-437">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="11d89-437">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="11d89-438">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="11d89-438">Namespace</span></span><br/>                | <span data-ttu-id="11d89-439">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="11d89-439">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="11d89-440">MOF</span><span class="sxs-lookup"><span data-stu-id="11d89-440">MOF</span></span><br/>                      | <dl> <span data-ttu-id="11d89-441"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="11d89-441"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="11d89-442">DLL</span><span class="sxs-lookup"><span data-stu-id="11d89-442">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11d89-443"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11d89-443"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11d89-444">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="11d89-444">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11d89-445">**\_USERDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="11d89-445">**CIM\_UserDevice**</span></span>](cim-userdevice.md)
</dt> </dl>

 

