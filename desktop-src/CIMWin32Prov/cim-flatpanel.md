---
description: La classe d’écran plat CIM \_ représente les fonctionnalités et la gestion de l’appareil logique à écran plat.
ms.assetid: 0c515621-4ff9-42af-a281-ac49af6d96ba
ms.tgt_platform: multiple
title: Classe CIM_FlatPanel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FlatPanel
- CIM_FlatPanel.Availability
- CIM_FlatPanel.Caption
- CIM_FlatPanel.ConfigManagerErrorCode
- CIM_FlatPanel.ConfigManagerUserConfig
- CIM_FlatPanel.CreationClassName
- CIM_FlatPanel.Description
- CIM_FlatPanel.DeviceID
- CIM_FlatPanel.DisplayType
- CIM_FlatPanel.ErrorCleared
- CIM_FlatPanel.ErrorDescription
- CIM_FlatPanel.HorizontalResolution
- CIM_FlatPanel.InstallDate
- CIM_FlatPanel.IsLocked
- CIM_FlatPanel.LastErrorCode
- CIM_FlatPanel.LightSource
- CIM_FlatPanel.Name
- CIM_FlatPanel.PNPDeviceID
- CIM_FlatPanel.PowerManagementCapabilities
- CIM_FlatPanel.PowerManagementSupported
- CIM_FlatPanel.ScanMode
- CIM_FlatPanel.Status
- CIM_FlatPanel.StatusInfo
- CIM_FlatPanel.SupportsColor
- CIM_FlatPanel.SystemCreationClassName
- CIM_FlatPanel.SystemName
- CIM_FlatPanel.VerticalResolution
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0c399383223734d2f8ebe68528352c229a74bfbc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950653"
---
# <a name="cim_flatpanel-class"></a><span data-ttu-id="45b99-103">Classe de plates-vous CIM \_</span><span class="sxs-lookup"><span data-stu-id="45b99-103">CIM\_FlatPanel class</span></span>

<span data-ttu-id="45b99-104">La classe d’écran plat **CIM \_** représente les fonctionnalités et la gestion de l’appareil logique à écran plat.</span><span class="sxs-lookup"><span data-stu-id="45b99-104">The **CIM\_FlatPanel** class represents the capabilities and management of the flat panel logical device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="45b99-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="45b99-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="45b99-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="45b99-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="45b99-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="45b99-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="45b99-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="45b99-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="45b99-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="45b99-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{1008CCE9-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class CIM_FlatPanel : CIM_Display
{
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  uint16   DisplayType;
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint32   HorizontalResolution;
  datetime InstallDate;
  boolean  IsLocked;
  uint32   LastErrorCode;
  uint16   LightSource;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   ScanMode;
  string   Status;
  uint16   StatusInfo;
  boolean  SupportsColor;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   VerticalResolution;
};
```

## <a name="members"></a><span data-ttu-id="45b99-110">Membres</span><span class="sxs-lookup"><span data-stu-id="45b99-110">Members</span></span>

<span data-ttu-id="45b99-111">La classe de **\_ plates** -formes CIM possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="45b99-111">The **CIM\_FlatPanel** class has these types of members:</span></span>

-   [<span data-ttu-id="45b99-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="45b99-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="45b99-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="45b99-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="45b99-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="45b99-114">Methods</span></span>

<span data-ttu-id="45b99-115">La classe de **\_ plates** -transporteurs CIM présente ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="45b99-115">The **CIM\_FlatPanel** class has these methods.</span></span>



| <span data-ttu-id="45b99-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="45b99-116">Method</span></span>                                                               | <span data-ttu-id="45b99-117">Description</span><span class="sxs-lookup"><span data-stu-id="45b99-117">Description</span></span>                                                                                                                              |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="45b99-118">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="45b99-118">**Reset**</span></span>](reset-method-in-class-cim-flatpanel.md)                 | <span data-ttu-id="45b99-119">Demande la réinitialisation de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="45b99-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="45b99-120">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="45b99-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="45b99-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="45b99-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-flatpanel.md) | <span data-ttu-id="45b99-122">Définit l’état d’alimentation souhaité pour un périphérique logique et lorsqu’un appareil doit être placé dans cet État.</span><span class="sxs-lookup"><span data-stu-id="45b99-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="45b99-123">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="45b99-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="45b99-124">Propriétés</span><span class="sxs-lookup"><span data-stu-id="45b99-124">Properties</span></span>

<span data-ttu-id="45b99-125">La classe du **modèle \_ plat CIM** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="45b99-125">The **CIM\_FlatPanel** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="45b99-126">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="45b99-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45b99-127">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="45b99-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="45b99-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45b99-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45b99-129">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="45b99-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="45b99-130">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="45b99-130">Availability and status of the device.</span></span>

<span data-ttu-id="45b99-131">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="45b99-131">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="45b99-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="45b99-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="45b99-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="45b99-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="45b99-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="45b99-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="45b99-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="45b99-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="45b99-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="45b99-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="45b99-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="45b99-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="45b99-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="45b99-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="45b99-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="45b99-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="45b99-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="45b99-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="45b99-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="45b99-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="45b99-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="45b99-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="45b99-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="45b99-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="45b99-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="45b99-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="45b99-145">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="45b99-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="45b99-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="45b99-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="45b99-147">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="45b99-147">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="45b99-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="45b99-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="45b99-149">L’appareil ne fonctionne pas mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="45b99-149">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="45b99-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="45b99-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="45b99-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="45b99-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="45b99-152">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="45b99-152">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="45b99-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="45b99-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="45b99-154">L’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="45b99-154">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="45b99-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="45b99-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="45b99-156">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="45b99-156">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="45b99-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="45b99-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="45b99-158">L’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="45b99-158">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="45b99-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="45b99-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="45b99-160">L’appareil est calme.</span><span class="sxs-lookup"><span data-stu-id="45b99-160">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="45b99-161">**Caption**</span><span class="sxs-lookup"><span data-stu-id="45b99-161">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45b99-162">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="45b99-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45b99-163">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45b99-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45b99-164">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="45b99-164">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="45b99-165">Courte description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="45b99-165">Short textual description of the object.</span></span>

<span data-ttu-id="45b99-166">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="45b99-166">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="45b99-167">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="45b99-167">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45b99-168">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="45b99-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="45b99-169">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45b99-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45b99-170">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="45b99-170">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="45b99-171">Code d’erreur Configuration Manager Win32.</span><span class="sxs-lookup"><span data-stu-id="45b99-171">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="45b99-172">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="45b99-172">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="45b99-173"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="45b99-173"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="45b99-174"> (0)</span><span class="sxs-lookup"><span data-stu-id="45b99-174">(0)</span></span>


</dt> <dd>

<span data-ttu-id="45b99-175">L’appareil fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="45b99-175">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="45b99-176"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="45b99-176"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="45b99-177">(1)</span><span class="sxs-lookup"><span data-stu-id="45b99-177">(1)</span></span>


</dt> <dd>

<span data-ttu-id="45b99-178">L’appareil n’est pas configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="45b99-178">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="45b99-179"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="45b99-179"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="45b99-180">(2)</span><span class="sxs-lookup"><span data-stu-id="45b99-180">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="45b99-181"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="45b99-181"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="45b99-182">(3)</span><span class="sxs-lookup"><span data-stu-id="45b99-182">(3)</span></span>


</dt> <dd>

<span data-ttu-id="45b99-183">Le pilote de cet appareil est peut-être endommagé ou la mémoire ou d’autres ressources du système sont peut-être insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="45b99-183">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="45b99-184"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="45b99-184"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="45b99-185">(4)</span><span class="sxs-lookup"><span data-stu-id="45b99-185">(4)</span></span>


</dt> <dd>

<span data-ttu-id="45b99-186">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="45b99-186">Device is not working properly.</span></span> <span data-ttu-id="45b99-187">L’un de ses pilotes ou le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="45b99-187">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="45b99-188"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="45b99-188"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="45b99-189">(5)</span><span class="sxs-lookup"><span data-stu-id="45b99-189">(5)</span></span>


</dt> <dd>

<span data-ttu-id="45b99-190">Le pilote de l’appareil requiert une ressource que Windows ne peut pas gérer.</span><span class="sxs-lookup"><span data-stu-id="45b99-190">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="45b99-191"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="45b99-191"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="45b99-192"> (6)</span><span class="sxs-lookup"><span data-stu-id="45b99-192">(6)</span></span>


</dt> <dd>

<span data-ttu-id="45b99-193">La configuration de démarrage de l’appareil est en conflit avec d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="45b99-193">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="45b99-194"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="45b99-194"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="45b99-195">(7)</span><span class="sxs-lookup"><span data-stu-id="45b99-195">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="45b99-196"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="45b99-196"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="45b99-197">(8)</span><span class="sxs-lookup"><span data-stu-id="45b99-197">(8)</span></span>


</dt> <dd>

<span data-ttu-id="45b99-198">Le chargeur de pilote de l’appareil est manquant.</span><span class="sxs-lookup"><span data-stu-id="45b99-198">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="45b99-199"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="45b99-199"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="45b99-200">(9)</span><span class="sxs-lookup"><span data-stu-id="45b99-200">(9)</span></span>


</dt> <dd>

<span data-ttu-id="45b99-201">L’appareil ne fonctionne pas correctement ; le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="45b99-201">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="45b99-202"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="45b99-202"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="45b99-203">(10)</span><span class="sxs-lookup"><span data-stu-id="45b99-203">(10)</span></span>


</dt> <dd>

<span data-ttu-id="45b99-204">Impossible de démarrer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="45b99-204">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="45b99-205"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="45b99-205"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="45b99-206">(11)</span><span class="sxs-lookup"><span data-stu-id="45b99-206">(11)</span></span>


</dt> <dd>

<span data-ttu-id="45b99-207">Échec de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="45b99-207">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="45b99-208"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="45b99-208"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="45b99-209">douze</span><span class="sxs-lookup"><span data-stu-id="45b99-209">(12)</span></span>


</dt> <dd>

<span data-ttu-id="45b99-210">L’appareil ne peut pas trouver suffisamment de ressources libres à utiliser.</span><span class="sxs-lookup"><span data-stu-id="45b99-210">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="45b99-211"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="45b99-211"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="45b99-212">(13)</span><span class="sxs-lookup"><span data-stu-id="45b99-212">(13)</span></span>


</dt> <dd>

<span data-ttu-id="45b99-213">Windows ne peut pas vérifier les ressources de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="45b99-213">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="45b99-214"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="45b99-214"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="45b99-215">(14)</span><span class="sxs-lookup"><span data-stu-id="45b99-215">(14)</span></span>


</dt> <dd>

<span data-ttu-id="45b99-216">L’appareil ne peut pas fonctionner correctement tant que l’ordinateur n’a pas redémarré.</span><span class="sxs-lookup"><span data-stu-id="45b99-216">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="45b99-217"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="45b99-217"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="45b99-218">(15)</span><span class="sxs-lookup"><span data-stu-id="45b99-218">(15)</span></span>


</dt> <dd>

<span data-ttu-id="45b99-219">L’appareil ne fonctionne pas correctement en raison d’un éventuel problème de réénumération.</span><span class="sxs-lookup"><span data-stu-id="45b99-219">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="45b99-220"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="45b99-220"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="45b99-221">(16)</span><span class="sxs-lookup"><span data-stu-id="45b99-221">(16)</span></span>


</dt> <dd>

<span data-ttu-id="45b99-222">Windows ne peut pas identifier toutes les ressources utilisées par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="45b99-222">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="45b99-223"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="45b99-223"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="45b99-224">(17)</span><span class="sxs-lookup"><span data-stu-id="45b99-224">(17)</span></span>


</dt> <dd>

<span data-ttu-id="45b99-225">L’appareil demande un type de ressource inconnu.</span><span class="sxs-lookup"><span data-stu-id="45b99-225">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="45b99-226"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="45b99-226"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="45b99-227">(18)</span><span class="sxs-lookup"><span data-stu-id="45b99-227">(18)</span></span>


</dt> <dd>

<span data-ttu-id="45b99-228">Les pilotes de périphérique doivent être réinstallés.</span><span class="sxs-lookup"><span data-stu-id="45b99-228">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="45b99-229"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="45b99-229"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="45b99-230">(19)</span><span class="sxs-lookup"><span data-stu-id="45b99-230">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="45b99-231"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="45b99-231"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="45b99-232">(20)</span><span class="sxs-lookup"><span data-stu-id="45b99-232">(20)</span></span>


</dt> <dd>

<span data-ttu-id="45b99-233">Le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="45b99-233">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="45b99-234"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="45b99-234"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="45b99-235">(21)</span><span class="sxs-lookup"><span data-stu-id="45b99-235">(21)</span></span>


</dt> <dd>

<span data-ttu-id="45b99-236">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="45b99-236">System failure.</span></span> <span data-ttu-id="45b99-237">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="45b99-237">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="45b99-238">Windows supprime l’appareil.</span><span class="sxs-lookup"><span data-stu-id="45b99-238">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="45b99-239"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="45b99-239"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="45b99-240">(22)</span><span class="sxs-lookup"><span data-stu-id="45b99-240">(22)</span></span>


</dt> <dd>

<span data-ttu-id="45b99-241">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="45b99-241">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="45b99-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="45b99-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="45b99-243">(23)</span><span class="sxs-lookup"><span data-stu-id="45b99-243">(23)</span></span>


</dt> <dd>

<span data-ttu-id="45b99-244">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="45b99-244">System failure.</span></span> <span data-ttu-id="45b99-245">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="45b99-245">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="45b99-246"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="45b99-246"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="45b99-247">(24)</span><span class="sxs-lookup"><span data-stu-id="45b99-247">(24)</span></span>


</dt> <dd>

<span data-ttu-id="45b99-248">L’appareil n’est pas présent, ne fonctionne pas correctement ou n’a pas tous ses pilotes installés.</span><span class="sxs-lookup"><span data-stu-id="45b99-248">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="45b99-249"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="45b99-249"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="45b99-250">(25)</span><span class="sxs-lookup"><span data-stu-id="45b99-250">(25)</span></span>


</dt> <dd>

<span data-ttu-id="45b99-251">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="45b99-251">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="45b99-252"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="45b99-252"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="45b99-253">(26)</span><span class="sxs-lookup"><span data-stu-id="45b99-253">(26)</span></span>


</dt> <dd>

<span data-ttu-id="45b99-254">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="45b99-254">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="45b99-255"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="45b99-255"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="45b99-256">(27)</span><span class="sxs-lookup"><span data-stu-id="45b99-256">(27)</span></span>


</dt> <dd>

<span data-ttu-id="45b99-257">L’appareil n’a pas une configuration de journal valide.</span><span class="sxs-lookup"><span data-stu-id="45b99-257">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="45b99-258"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="45b99-258"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="45b99-259">(28)</span><span class="sxs-lookup"><span data-stu-id="45b99-259">(28)</span></span>


</dt> <dd>

<span data-ttu-id="45b99-260">Les pilotes de périphérique ne sont pas installés.</span><span class="sxs-lookup"><span data-stu-id="45b99-260">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="45b99-261"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="45b99-261"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="45b99-262">(29)</span><span class="sxs-lookup"><span data-stu-id="45b99-262">(29)</span></span>


</dt> <dd>

<span data-ttu-id="45b99-263">L’appareil est désactivé ; le microprogramme de l’appareil n’a pas fourni les ressources requises.</span><span class="sxs-lookup"><span data-stu-id="45b99-263">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="45b99-264"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="45b99-264"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="45b99-265">(30)</span><span class="sxs-lookup"><span data-stu-id="45b99-265">(30)</span></span>


</dt> <dd>

<span data-ttu-id="45b99-266">L’appareil utilise une ressource IRQ qu’un autre appareil utilise.</span><span class="sxs-lookup"><span data-stu-id="45b99-266">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="45b99-267"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="45b99-267"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="45b99-268">31</span><span class="sxs-lookup"><span data-stu-id="45b99-268">(31)</span></span>


</dt> <dd>

<span data-ttu-id="45b99-269">L’appareil ne fonctionne pas correctement ; Windows ne peut pas charger les pilotes de périphérique requis.</span><span class="sxs-lookup"><span data-stu-id="45b99-269">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="45b99-270">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="45b99-270">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45b99-271">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="45b99-271">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="45b99-272">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45b99-272">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45b99-273">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="45b99-273">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="45b99-274">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="45b99-274">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="45b99-275">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="45b99-275">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="45b99-276">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="45b99-276">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45b99-277">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="45b99-277">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45b99-278">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45b99-278">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45b99-279">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="45b99-279">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="45b99-280">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="45b99-280">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="45b99-281">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="45b99-281">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="45b99-282">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="45b99-282">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="45b99-283">**Description**</span><span class="sxs-lookup"><span data-stu-id="45b99-283">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45b99-284">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="45b99-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45b99-285">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45b99-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45b99-286">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="45b99-286">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="45b99-287">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="45b99-287">Textual description of the object.</span></span>

<span data-ttu-id="45b99-288">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="45b99-288">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="45b99-289">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="45b99-289">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45b99-290">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="45b99-290">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45b99-291">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45b99-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45b99-292">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="45b99-292">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="45b99-293">Adresse ou d’autres informations d’identification pour nommer de manière unique l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="45b99-293">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="45b99-294">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="45b99-294">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="45b99-295">**DisplayType**</span><span class="sxs-lookup"><span data-stu-id="45b99-295">**DisplayType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45b99-296">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="45b99-296">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="45b99-297">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45b99-297">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45b99-298">Énumération qui décrit le type d’affichage du panneau plat.</span><span class="sxs-lookup"><span data-stu-id="45b99-298">Enumeration that describes the type of flat panel display.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="45b99-299"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="45b99-299"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="45b99-300"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="45b99-300"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Passive_Matrix_LCD"></span><span id="passive_matrix_lcd"></span><span id="PASSIVE_MATRIX_LCD"></span>

<span data-ttu-id="45b99-301"><span id="Passive_Matrix_LCD"></span><span id="passive_matrix_lcd"></span><span id="PASSIVE_MATRIX_LCD"></span>**LCD à matrice passive** (2)</span><span class="sxs-lookup"><span data-stu-id="45b99-301"><span id="Passive_Matrix_LCD"></span><span id="passive_matrix_lcd"></span><span id="PASSIVE_MATRIX_LCD"></span>**Passive Matrix LCD** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Active_Matrix_LCD"></span><span id="active_matrix_lcd"></span><span id="ACTIVE_MATRIX_LCD"></span>

<span data-ttu-id="45b99-302"><span id="Active_Matrix_LCD"></span><span id="active_matrix_lcd"></span><span id="ACTIVE_MATRIX_LCD"></span>**LCD à matrice active** (3)</span><span class="sxs-lookup"><span data-stu-id="45b99-302"><span id="Active_Matrix_LCD"></span><span id="active_matrix_lcd"></span><span id="ACTIVE_MATRIX_LCD"></span>**Active Matrix LCD** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Cholesteric_LCD"></span><span id="cholesteric_lcd"></span><span id="CHOLESTERIC_LCD"></span>

<span data-ttu-id="45b99-303"><span id="Cholesteric_LCD"></span><span id="cholesteric_lcd"></span><span id="CHOLESTERIC_LCD"></span>**CHOLESTERIC LCD** (4)</span><span class="sxs-lookup"><span data-stu-id="45b99-303"><span id="Cholesteric_LCD"></span><span id="cholesteric_lcd"></span><span id="CHOLESTERIC_LCD"></span>**Cholesteric LCD** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Field_Emission_Display"></span><span id="field_emission_display"></span><span id="FIELD_EMISSION_DISPLAY"></span>

<span data-ttu-id="45b99-304"><span id="Field_Emission_Display"></span><span id="field_emission_display"></span><span id="FIELD_EMISSION_DISPLAY"></span>**Affichage des émissions de champ** (5)</span><span class="sxs-lookup"><span data-stu-id="45b99-304"><span id="Field_Emission_Display"></span><span id="field_emission_display"></span><span id="FIELD_EMISSION_DISPLAY"></span>**Field Emission Display** (5)</span></span>


</dt> <dd>

<span data-ttu-id="45b99-305">Émission de champ</span><span class="sxs-lookup"><span data-stu-id="45b99-305">Field emission</span></span>

</dd> <dt>

<span id="Electro_Luminescent_Display"></span><span id="electro_luminescent_display"></span><span id="ELECTRO_LUMINESCENT_DISPLAY"></span>

<span data-ttu-id="45b99-306"><span id="Electro_Luminescent_Display"></span><span id="electro_luminescent_display"></span><span id="ELECTRO_LUMINESCENT_DISPLAY"></span>**Affichage électroluminescent** (6)</span><span class="sxs-lookup"><span data-stu-id="45b99-306"><span id="Electro_Luminescent_Display"></span><span id="electro_luminescent_display"></span><span id="ELECTRO_LUMINESCENT_DISPLAY"></span>**Electro Luminescent Display** (6)</span></span>


</dt> <dd>

<span data-ttu-id="45b99-307">Électroluminescent</span><span class="sxs-lookup"><span data-stu-id="45b99-307">Electro luminescent</span></span>

</dd> <dt>

<span id="Gas_Plasma"></span><span id="gas_plasma"></span><span id="GAS_PLASMA"></span>

<span data-ttu-id="45b99-308"><span id="Gas_Plasma"></span><span id="gas_plasma"></span><span id="GAS_PLASMA"></span>**Plasma à gaz** (7)</span><span class="sxs-lookup"><span data-stu-id="45b99-308"><span id="Gas_Plasma"></span><span id="gas_plasma"></span><span id="GAS_PLASMA"></span>**Gas Plasma** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="LED"></span><span id="led"></span>

<span data-ttu-id="45b99-309"><span id="LED"></span><span id="led"></span>**LED** (8)</span><span class="sxs-lookup"><span data-stu-id="45b99-309"><span id="LED"></span><span id="led"></span>**LED** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="45b99-310">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="45b99-310">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45b99-311">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="45b99-311">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="45b99-312">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45b99-312">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45b99-313">Si la **valeur est true**, l’erreur signalée dans la propriété **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="45b99-313">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="45b99-314">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="45b99-314">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="45b99-315">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="45b99-315">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45b99-316">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="45b99-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45b99-317">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45b99-317">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45b99-318">Chaîne de forme libre qui fournit des informations sur l’erreur enregistrée dans la propriété **LastErrorCode** et les actions correctives à effectuer.</span><span class="sxs-lookup"><span data-stu-id="45b99-318">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="45b99-319">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="45b99-319">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="45b99-320">**HorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="45b99-320">**HorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45b99-321">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="45b99-321">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="45b99-322">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45b99-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45b99-323">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« pixels »)</span><span class="sxs-lookup"><span data-stu-id="45b99-323">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="45b99-324">Résolution horizontale, en pixels.</span><span class="sxs-lookup"><span data-stu-id="45b99-324">Horizontal resolution, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="45b99-325">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="45b99-325">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45b99-326">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="45b99-326">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="45b99-327">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45b99-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45b99-328">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="45b99-328">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="45b99-329">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="45b99-329">Date and time the object was installed.</span></span> <span data-ttu-id="45b99-330">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="45b99-330">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="45b99-331">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="45b99-331">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="45b99-332">**IsLocked**</span><span class="sxs-lookup"><span data-stu-id="45b99-332">**IsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45b99-333">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="45b99-333">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="45b99-334">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45b99-334">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45b99-335">Si la **valeur est true**, l’appareil est verrouillé, ce qui empêche l’entrée ou la sortie de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="45b99-335">If **TRUE**, the device is locked, preventing user input or output.</span></span>

<span data-ttu-id="45b99-336">Cette propriété est héritée de la [**\_ UserDevice CIM**](cim-userdevice.md).</span><span class="sxs-lookup"><span data-stu-id="45b99-336">This property is inherited from [**CIM\_UserDevice**](cim-userdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="45b99-337">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="45b99-337">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45b99-338">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="45b99-338">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="45b99-339">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45b99-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45b99-340">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="45b99-340">Last error code reported by the logical device.</span></span>

<span data-ttu-id="45b99-341">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="45b99-341">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="45b99-342">**LightSource**</span><span class="sxs-lookup"><span data-stu-id="45b99-342">**LightSource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45b99-343">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="45b99-343">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="45b99-344">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45b99-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45b99-345">Description du type d’éclairage d’affichage.</span><span class="sxs-lookup"><span data-stu-id="45b99-345">Description of the display illumination type.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="45b99-346">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="45b99-346">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="45b99-347">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="45b99-347">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Backlit"></span><span id="backlit"></span><span id="BACKLIT"></span>

<span data-ttu-id="45b99-348">**Rétroéclairé** (2)</span><span class="sxs-lookup"><span data-stu-id="45b99-348">**Backlit** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Edgelit"></span><span id="edgelit"></span><span id="EDGELIT"></span>

<span data-ttu-id="45b99-349">**Edgelit** (3)</span><span class="sxs-lookup"><span data-stu-id="45b99-349">**Edgelit** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Reflective"></span><span id="reflective"></span><span id="REFLECTIVE"></span>

<span data-ttu-id="45b99-350">**Réfléchissant** (4)</span><span class="sxs-lookup"><span data-stu-id="45b99-350">**Reflective** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="45b99-351">**Nom**</span><span class="sxs-lookup"><span data-stu-id="45b99-351">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45b99-352">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="45b99-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45b99-353">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45b99-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45b99-354">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="45b99-354">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="45b99-355">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="45b99-355">Label by which the object is known.</span></span> <span data-ttu-id="45b99-356">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="45b99-356">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="45b99-357">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="45b99-357">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="45b99-358">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="45b99-358">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45b99-359">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="45b99-359">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45b99-360">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45b99-360">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45b99-361">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="45b99-361">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="45b99-362">Win32 Plug-and-Play identificateur du périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="45b99-362">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="45b99-363">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="45b99-363">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="45b99-364">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="45b99-364">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="45b99-365">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="45b99-365">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45b99-366">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="45b99-366">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="45b99-367">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45b99-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45b99-368">Tableau des fonctionnalités d’alimentation spécifiques d’un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="45b99-368">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="45b99-369">Cette propriété est héritée de **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="45b99-369">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="45b99-370"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="45b99-370"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="45b99-371"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="45b99-371"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="45b99-372"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="45b99-372"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="45b99-373"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="45b99-373"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="45b99-374">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="45b99-374">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="45b99-375"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="45b99-375"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="45b99-376">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="45b99-376">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="45b99-377"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="45b99-377"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="45b99-378">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="45b99-378">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="45b99-379">Cette méthode se trouve sur la classe parente du **\_ LogicalDevice CIM** et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="45b99-379">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="45b99-380">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="45b99-380">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="45b99-381"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="45b99-381"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="45b99-382">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation).</span><span class="sxs-lookup"><span data-stu-id="45b99-382">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="45b99-383"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="45b99-383"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="45b99-384">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation) et l' *heure* définie sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="45b99-384">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="45b99-385">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="45b99-385">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45b99-386">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="45b99-386">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="45b99-387">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45b99-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45b99-388">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation, c’est-à-dire être mis en état d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="45b99-388">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="45b99-389">Si la valeur est **false**, la valeur entière 1 (« non pris en charge ») doit être la seule entrée dans le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="45b99-389">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="45b99-390">Cette propriété n’indique pas si les fonctionnalités de gestion de l’alimentation sont actuellement activées, ou si elles sont activées, quelles sont les fonctionnalités prises en charge.</span><span class="sxs-lookup"><span data-stu-id="45b99-390">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="45b99-391">Pour plus d’informations, consultez le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="45b99-391">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="45b99-392">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="45b99-392">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="45b99-393">**ScanMode**</span><span class="sxs-lookup"><span data-stu-id="45b99-393">**ScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45b99-394">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="45b99-394">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="45b99-395">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45b99-395">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45b99-396">Mode d’analyse qui indique une analyse unique ou double, par exemple.</span><span class="sxs-lookup"><span data-stu-id="45b99-396">Scan mode that indicates single or dual scan, for example.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="45b99-397">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="45b99-397">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="45b99-398">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="45b99-398">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Single_Scan"></span><span id="single_scan"></span><span id="SINGLE_SCAN"></span>

<span data-ttu-id="45b99-399">**Analyse unique** (2)</span><span class="sxs-lookup"><span data-stu-id="45b99-399">**Single Scan** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Dual_Scan"></span><span id="dual_scan"></span><span id="DUAL_SCAN"></span>

<span data-ttu-id="45b99-400">**Analyse double** (3)</span><span class="sxs-lookup"><span data-stu-id="45b99-400">**Dual Scan** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="45b99-401">**État**</span><span class="sxs-lookup"><span data-stu-id="45b99-401">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45b99-402">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="45b99-402">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45b99-403">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45b99-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45b99-404">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="45b99-404">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="45b99-405">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="45b99-405">Current status of the object.</span></span> <span data-ttu-id="45b99-406">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="45b99-406">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="45b99-407">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="45b99-407">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="45b99-408">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="45b99-408">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="45b99-409">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="45b99-409">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="45b99-410">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="45b99-410">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="45b99-411">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="45b99-411">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="45b99-412">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="45b99-412">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="45b99-413">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="45b99-413">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="45b99-414">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="45b99-414">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="45b99-415">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="45b99-415">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="45b99-416">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="45b99-416">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="45b99-417">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="45b99-417">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="45b99-418">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="45b99-418">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="45b99-419">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="45b99-419">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="45b99-420">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="45b99-420">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45b99-421">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="45b99-421">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="45b99-422">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45b99-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45b99-423">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="45b99-423">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="45b99-424">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="45b99-424">State of the logical device.</span></span> <span data-ttu-id="45b99-425">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (non applicable) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="45b99-425">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="45b99-426">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="45b99-426">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="45b99-427">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="45b99-427">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="45b99-428">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="45b99-428">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="45b99-429">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="45b99-429">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="45b99-430">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="45b99-430">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="45b99-431">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="45b99-431">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="45b99-432">**SupportsColor**</span><span class="sxs-lookup"><span data-stu-id="45b99-432">**SupportsColor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45b99-433">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="45b99-433">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="45b99-434">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45b99-434">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45b99-435">Si la **valeur est true**, le panneau plat prend en charge l’affichage des couleurs.</span><span class="sxs-lookup"><span data-stu-id="45b99-435">If **TRUE**, the flat panel supports color display.</span></span>

</dd> <dt>

<span data-ttu-id="45b99-436">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="45b99-436">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45b99-437">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="45b99-437">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45b99-438">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45b99-438">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45b99-439">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="45b99-439">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="45b99-440">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="45b99-440">Scoping system's creation class name.</span></span>

<span data-ttu-id="45b99-441">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="45b99-441">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="45b99-442">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="45b99-442">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45b99-443">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="45b99-443">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45b99-444">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45b99-444">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45b99-445">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="45b99-445">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="45b99-446">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="45b99-446">Scoping system's name.</span></span>

<span data-ttu-id="45b99-447">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="45b99-447">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="45b99-448">**VerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="45b99-448">**VerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45b99-449">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="45b99-449">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="45b99-450">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45b99-450">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45b99-451">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« pixels »)</span><span class="sxs-lookup"><span data-stu-id="45b99-451">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="45b99-452">Résolution verticale, en pixels.</span><span class="sxs-lookup"><span data-stu-id="45b99-452">Vertical resolution, in pixels.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="45b99-453">Notes</span><span class="sxs-lookup"><span data-stu-id="45b99-453">Remarks</span></span>

<span data-ttu-id="45b99-454">La classe de l’écran **\_ plat CIM** est dérivée de l' [**\_ affichage CIM**](cim-display.md).</span><span class="sxs-lookup"><span data-stu-id="45b99-454">The **CIM\_FlatPanel** class is derived from [**CIM\_Display**](cim-display.md).</span></span>

<span data-ttu-id="45b99-455">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="45b99-455">WMI does not implement this class.</span></span>

<span data-ttu-id="45b99-456">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="45b99-456">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="45b99-457">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="45b99-457">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="45b99-458">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="45b99-458">Requirements</span></span>



| <span data-ttu-id="45b99-459">Condition requise</span><span class="sxs-lookup"><span data-stu-id="45b99-459">Requirement</span></span> | <span data-ttu-id="45b99-460">Valeur</span><span class="sxs-lookup"><span data-stu-id="45b99-460">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="45b99-461">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="45b99-461">Minimum supported client</span></span><br/> | <span data-ttu-id="45b99-462">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="45b99-462">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="45b99-463">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="45b99-463">Minimum supported server</span></span><br/> | <span data-ttu-id="45b99-464">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="45b99-464">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="45b99-465">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="45b99-465">Namespace</span></span><br/>                | <span data-ttu-id="45b99-466">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="45b99-466">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="45b99-467">MOF</span><span class="sxs-lookup"><span data-stu-id="45b99-467">MOF</span></span><br/>                      | <dl> <span data-ttu-id="45b99-468"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="45b99-468"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="45b99-469">DLL</span><span class="sxs-lookup"><span data-stu-id="45b99-469">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45b99-470"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45b99-470"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45b99-471">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="45b99-471">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45b99-472">**\_Affichage CIM**</span><span class="sxs-lookup"><span data-stu-id="45b99-472">**CIM\_Display**</span></span>](cim-display.md)
</dt> </dl>

 

