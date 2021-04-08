---
description: Abstraction ou émulation d’une entité matérielle qui peut ou ne peut pas être basée sur du matériel physique.
ms.assetid: e31c82ed-2da2-4a18-a55e-16931d74f243
title: Classe CIM_LogicalDevice (gestion Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice
- CIM_LogicalDevice.SystemCreationClassName
- CIM_LogicalDevice.SystemName
- CIM_LogicalDevice.CreationClassName
- CIM_LogicalDevice.DeviceID
- CIM_LogicalDevice.PowerManagementSupported
- CIM_LogicalDevice.PowerManagementCapabilities
- CIM_LogicalDevice.Availability
- CIM_LogicalDevice.StatusInfo
- CIM_LogicalDevice.LastErrorCode
- CIM_LogicalDevice.ErrorDescription
- CIM_LogicalDevice.ErrorCleared
- CIM_LogicalDevice.OtherIdentifyingInfo
- CIM_LogicalDevice.PowerOnHours
- CIM_LogicalDevice.TotalPowerOnHours
- CIM_LogicalDevice.IdentifyingDescriptions
- CIM_LogicalDevice.AdditionalAvailability
- CIM_LogicalDevice.MaxQuiesceTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 471b10f8d3c8640cfcc4277d0151bdd46d59db86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749653"
---
# <a name="cim_logicaldevice-class-hyper-v-management"></a><span data-ttu-id="95569-103">Classe CIM_LogicalDevice (gestion Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="95569-103">CIM_LogicalDevice class (Hyper-V management)</span></span>

<span data-ttu-id="95569-104">Abstraction ou émulation d’une entité matérielle qui peut ou ne peut pas être basée sur du matériel physique.</span><span class="sxs-lookup"><span data-stu-id="95569-104">An abstraction or emulation of a hardware entity that may or may not be based on physical hardware.</span></span>

## <a name="syntax"></a><span data-ttu-id="95569-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="95569-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.8.0"), UMLPackagePath("CIM::Core::Device"), AMENDMENT]
class CIM_LogicalDevice : CIM_EnabledLogicalElement
{
  string  SystemCreationClassName;
  string  SystemName;
  string  CreationClassName;
  string  DeviceID;
  boolean PowerManagementSupported;
  uint16  PowerManagementCapabilities[];
  uint16  Availability;
  uint16  StatusInfo;
  uint32  LastErrorCode;
  string  ErrorDescription;
  boolean ErrorCleared;
  string  OtherIdentifyingInfo[];
  uint64  PowerOnHours;
  uint64  TotalPowerOnHours;
  string  IdentifyingDescriptions[];
  uint16  AdditionalAvailability[];
  uint64  MaxQuiesceTime;
};
```

## <a name="members"></a><span data-ttu-id="95569-106">Membres</span><span class="sxs-lookup"><span data-stu-id="95569-106">Members</span></span>

<span data-ttu-id="95569-107">La classe **CIM \_ LogicalDevice** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="95569-107">The **CIM\_LogicalDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="95569-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="95569-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="95569-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="95569-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="95569-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="95569-110">Methods</span></span>

<span data-ttu-id="95569-111">La classe **CIM \_ LogicalDevice** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="95569-111">The **CIM\_LogicalDevice** class has these methods.</span></span>



| <span data-ttu-id="95569-112">Méthode</span><span class="sxs-lookup"><span data-stu-id="95569-112">Method</span></span>                                                           | <span data-ttu-id="95569-113">Description</span><span class="sxs-lookup"><span data-stu-id="95569-113">Description</span></span>                                                                                                                                                                                                                              |
|:-----------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="95569-114">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="95569-114">**EnableDevice**</span></span>](cim-logicaldevice-enabledevice.md)           | <span data-ttu-id="95569-115">Cette méthode est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="95569-115">This method is deprecated.</span></span> <span data-ttu-id="95569-116">Utilisez à la place la méthode **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="95569-116">Instead, use the **RequestStateChange** method.</span></span><br/> <span data-ttu-id="95569-117">**Description déconseillée :** Active ou désactive l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="95569-117">**Deprecated description:** Enables or disables the logical device.</span></span><br/>                                                                     |
| [<span data-ttu-id="95569-118">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="95569-118">**OnlineDevice**</span></span>](cim-logicaldevice-onlinedevice.md)           | <span data-ttu-id="95569-119">Cette méthode est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="95569-119">This method is deprecated.</span></span> <span data-ttu-id="95569-120">Utilisez à la place la méthode **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="95569-120">Instead, use the **RequestStateChange** method.</span></span><br/> <span data-ttu-id="95569-121">**Description déconseillée :** Met l’appareil logique en ligne afin qu’il puisse accepter les requêtes ou hors connexion afin qu’il ne puisse plus accepter de demandes.</span><span class="sxs-lookup"><span data-stu-id="95569-121">**Deprecated description:** Brings the logical device online so it can accept requests, or offline so it can no longer accept requests.</span></span><br/> |
| [<span data-ttu-id="95569-122">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="95569-122">**QuiesceDevice**</span></span>](cim-logicaldevice-quiescedevice.md)         | <span data-ttu-id="95569-123">Cette méthode est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="95569-123">This method is deprecated.</span></span> <span data-ttu-id="95569-124">Utilisez à la place la méthode **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="95569-124">Instead, use the **RequestStateChange** method.</span></span><br/> <span data-ttu-id="95569-125">**Description déconseillée :** Interrompt temporairement l’activité sur l’unité logique ou réactive l’activité.</span><span class="sxs-lookup"><span data-stu-id="95569-125">**Deprecated description:** Temporarily suspends activity on the logical device, or re-enables the activity.</span></span><br/>                            |
| [<span data-ttu-id="95569-126">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="95569-126">**Reset**</span></span>](cim-logicaldevice-reset.md)                         | <span data-ttu-id="95569-127">Réinitialise l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="95569-127">Resets the logical device.</span></span><br/>                                                                                                                                                                                                    |
| [<span data-ttu-id="95569-128">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="95569-128">**RestoreProperties**</span></span>](cim-logicaldevice-restoreproperties.md) | <span data-ttu-id="95569-129">Restaure une configuration et un État antérieurs de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="95569-129">Restores a previous configuration and state of the logical device.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="95569-130">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="95569-130">**SaveProperties**</span></span>](cim-logicaldevice-saveproperties.md)       | <span data-ttu-id="95569-131">Enregistre la configuration et l’état de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="95569-131">Saves the configuration and state of the logical device.</span></span><br/>                                                                                                                                                                      |
| [<span data-ttu-id="95569-132">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="95569-132">**SetPowerState**</span></span>](cim-logicaldevice-setpowerstate.md)         | <span data-ttu-id="95569-133">Cette méthode est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="95569-133">This method is deprecated.</span></span> <span data-ttu-id="95569-134">Utilisez plutôt la propriété **SetPowerState** de la classe **CIM \_ PowerManagementService** .</span><span class="sxs-lookup"><span data-stu-id="95569-134">Instead, use the **SetPowerState** property of the **CIM\_PowerManagementService** class.</span></span><br/> <span data-ttu-id="95569-135">**Description déconseillée :** Définit l’état d’alimentation de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="95569-135">**Deprecated description:** Sets the power state of the logical device.</span></span><br/>                       |



 

### <a name="properties"></a><span data-ttu-id="95569-136">Propriétés</span><span class="sxs-lookup"><span data-stu-id="95569-136">Properties</span></span>

<span data-ttu-id="95569-137">La classe **CIM \_ LogicalDevice** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="95569-137">The **CIM\_LogicalDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="95569-138">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="95569-138">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95569-139">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="95569-139">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="95569-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95569-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95569-141">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ LogicalDevice**.**Disponibilité**»)</span><span class="sxs-lookup"><span data-stu-id="95569-141">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_LogicalDevice**.**Availability**")</span></span>
</dt> </dl>

<span data-ttu-id="95569-142">Tableau qui contient les informations de disponibilité relatives à l’appareil logique, en plus de celle de la propriété **Availability** .</span><span class="sxs-lookup"><span data-stu-id="95569-142">An array that contains availability information about of the logical device, in addition to the that of the **Availability** property.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="95569-143">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="95569-143">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="95569-144">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="95569-144">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="95569-145">**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="95569-145">**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="95569-146">**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="95569-146">**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="95569-147">**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="95569-147">**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="95569-148">**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="95569-148">**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="95569-149">**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="95569-149">**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="95569-150">**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="95569-150">**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="95569-151">**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="95569-151">**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="95569-152">**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="95569-152">**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="95569-153">**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="95569-153">**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="95569-154">**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="95569-154">**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="95569-155">Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="95569-155">**Power Save - Unknown** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="95569-156">Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="95569-156">**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="95569-157">Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="95569-157">**Power Save - Standby** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="95569-158">**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="95569-158">**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="95569-159">Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="95569-159">**Power Save - Warning** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="95569-160">En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="95569-160">**Paused** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="95569-161">**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="95569-161">**Not Ready** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="95569-162">**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="95569-162">**Not Configured** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="95569-163">**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="95569-163">**Quiesced** (21)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="95569-164">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="95569-164">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95569-165">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="95569-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="95569-166">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95569-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95569-167">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 006,5 "," MIB. IETF \| Host-Resources-MIB. hrDeviceStatus "," MIF. \|Appareil hôte DMTF \| 001,5 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ LogicalDevice**.**AdditionalAvailability**")</span><span class="sxs-lookup"><span data-stu-id="95569-167">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|006.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus", "MIF.DMTF\|Host Device\|001.5"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_LogicalDevice**.**AdditionalAvailability**")</span></span>
</dt> </dl>

<span data-ttu-id="95569-168">Contient la disponibilité de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="95569-168">Contains the availability of the logical device.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="95569-169">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="95569-169">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="95569-170">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="95569-170">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="95569-171">**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="95569-171">**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="95569-172">**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="95569-172">**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="95569-173">**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="95569-173">**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="95569-174">**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="95569-174">**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="95569-175">**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="95569-175">**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="95569-176">**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="95569-176">**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="95569-177">**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="95569-177">**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="95569-178">**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="95569-178">**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="95569-179">**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="95569-179">**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="95569-180">**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="95569-180">**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="95569-181">Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="95569-181">**Power Save - Unknown** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="95569-182">Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="95569-182">**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="95569-183">Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="95569-183">**Power Save - Standby** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="95569-184">**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="95569-184">**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="95569-185">Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="95569-185">**Power Save - Warning** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="95569-186">En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="95569-186">**Paused** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="95569-187">**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="95569-187">**Not Ready** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="95569-188">**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="95569-188">**Not Configured** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="95569-189">**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="95569-189">**Quiesced** (21)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="95569-190">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="95569-190">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95569-191">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="95569-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95569-192">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95569-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95569-193">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="95569-193">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="95569-194">Nom de la classe utilisé pour créer une instance de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="95569-194">The class name used to create an instance of the logical device.</span></span> <span data-ttu-id="95569-195">**CreationClassName** est combiné avec d’autres propriétés de clé de cette classe pour identifier de manière unique les instances de cette classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="95569-195">**CreationClassName** is combined with other key properties of this class to uniquely identify instances of this class and its subclasses.</span></span>

</dd> <dt>

<span data-ttu-id="95569-196">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="95569-196">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95569-197">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="95569-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95569-198">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95569-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95569-199">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="95569-199">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="95569-200">Identificateur unique de l’unité logique, tel que l’adresse.</span><span class="sxs-lookup"><span data-stu-id="95569-200">A unique identifier of the logical device, such as the address.</span></span>

</dd> <dt>

<span data-ttu-id="95569-201">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="95569-201">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95569-202">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="95569-202">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="95569-203">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95569-203">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95569-204">Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**\_ ManagedSystemElement CIM**](cim-managedsystemelement.md).**OperationalStatus**»)</span><span class="sxs-lookup"><span data-stu-id="95569-204">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).**OperationalStatus**")</span></span>
</dt> </dl>

<span data-ttu-id="95569-205">Cette propriété est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="95569-205">This property is deprecated.</span></span> <span data-ttu-id="95569-206">Utilisez plutôt la propriété **OperationalStatus** de la classe **\_ ManagedSystemElement CIM** .</span><span class="sxs-lookup"><span data-stu-id="95569-206">Instead, use the **OperationalStatus** property from the **CIM\_ManagedSystemElement** class.</span></span>

<span data-ttu-id="95569-207">**Description déconseillée :** Indique si une erreur signalée par la propriété **LastErrorCode** est effacée.</span><span class="sxs-lookup"><span data-stu-id="95569-207">**Deprecated description:** Indicates whether an error reported by the **LastErrorCode** property is cleared.</span></span>

</dd> <dt>

<span data-ttu-id="95569-208">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="95569-208">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95569-209">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="95569-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95569-210">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95569-210">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95569-211">Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ DeviceErrorData. ErrorDescription")</span><span class="sxs-lookup"><span data-stu-id="95569-211">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_DeviceErrorData.ErrorDescription")</span></span>
</dt> </dl>

<span data-ttu-id="95569-212">Cette propriété est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="95569-212">This property is deprecated.</span></span> <span data-ttu-id="95569-213">Utilisez plutôt la propriété **ErrorDescription** de la classe **CIM \_ DeviceErrorData** .</span><span class="sxs-lookup"><span data-stu-id="95569-213">Instead, use the **ErrorDescription** property from the **CIM\_DeviceErrorData** class.</span></span>

<span data-ttu-id="95569-214">**Description déconseillée :** Informations supplémentaires sur l’erreur signalée par la propriété **LastErrorCode** .</span><span class="sxs-lookup"><span data-stu-id="95569-214">**Deprecated description:** Additional information about the error reported by the **LastErrorCode** property.</span></span>

</dd> <dt>

<span data-ttu-id="95569-215">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="95569-215">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95569-216">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="95569-216">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="95569-217">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95569-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95569-218">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ LogicalDevice**.**OtherIdentifyingInfo**")</span><span class="sxs-lookup"><span data-stu-id="95569-218">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_LogicalDevice**.**OtherIdentifyingInfo**")</span></span>
</dt> </dl>

<span data-ttu-id="95569-219">Tableau de chaînes qui décrivent les éléments de tableau **OtherIdentifyingInfo** du même index.</span><span class="sxs-lookup"><span data-stu-id="95569-219">An array of strings that describe the **OtherIdentifyingInfo** array items of the same index.</span></span>

</dd> <dt>

<span data-ttu-id="95569-220">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="95569-220">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95569-221">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="95569-221">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="95569-222">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95569-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95569-223">Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ DeviceErrorData. LastErrorCode")</span><span class="sxs-lookup"><span data-stu-id="95569-223">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_DeviceErrorData.LastErrorCode")</span></span>
</dt> </dl>

<span data-ttu-id="95569-224">Cette propriété est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="95569-224">This property is deprecated.</span></span> <span data-ttu-id="95569-225">Au lieu de cela, nous utilisons la propriété **LastErrorCode** à partir de la classe **CIM \_ DeviceErrorData** .</span><span class="sxs-lookup"><span data-stu-id="95569-225">Instead, we use the **LastErrorCode** property from the **CIM\_DeviceErrorData** class.</span></span>

<span data-ttu-id="95569-226">**Description déconseillée :** Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="95569-226">**Deprecated description:** The last error code reported by the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="95569-227">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="95569-227">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95569-228">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="95569-228">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="95569-229">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95569-229">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95569-230">Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) (« aucune valeur »), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« millisecondes »)</span><span class="sxs-lookup"><span data-stu-id="95569-230">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MilliSeconds")</span></span>
</dt> </dl>

<span data-ttu-id="95569-231">Cette propriété est déconseillée et ne doit pas être utilisée.</span><span class="sxs-lookup"><span data-stu-id="95569-231">This property is deprecated and should not be used.</span></span>

<span data-ttu-id="95569-232">**Description déconseillée :** Durée maximale, en millisecondes, pendant laquelle un appareil peut rester dans un état désactivé temporairement (les propriétés **Availability** et **AdditionalAvailability** ont la valeur « 21 ».</span><span class="sxs-lookup"><span data-stu-id="95569-232">**Deprecated description:** The maximum time in milliseconds, that a device can remain in a temporarily disabled state (**Availability** and **AdditionalAvailability** properties set to "21"   quiescent ).</span></span> <span data-ttu-id="95569-233">La valeur « 0 » indique que l’appareil logique peut rester indéfiniment dans un état désactivé temporairement.</span><span class="sxs-lookup"><span data-stu-id="95569-233">A value of "0" indicates that the logical device can remain in a temporarily disabled state indefinitely.</span></span>

</dd> <dt>

<span data-ttu-id="95569-234">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="95569-234">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95569-235">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="95569-235">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="95569-236">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95569-236">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95569-237">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ LogicalDevice**.**IdentifyingDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="95569-237">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_LogicalDevice**.**IdentifyingDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="95569-238">Informations identifiant l’unité logique, autre que **DeviceID**.</span><span class="sxs-lookup"><span data-stu-id="95569-238">Information that identifies the logical device, other than **DeviceID**.</span></span>

</dd> <dt>

<span data-ttu-id="95569-239">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="95569-239">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95569-240">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="95569-240">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="95569-241">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95569-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95569-242">Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ PowerManagementCapabilities. PowerCapabilities")</span><span class="sxs-lookup"><span data-stu-id="95569-242">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_PowerManagementCapabilities.PowerCapabilities")</span></span>
</dt> </dl>

<span data-ttu-id="95569-243">Cette propriété est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="95569-243">This property is deprecated.</span></span> <span data-ttu-id="95569-244">Utilisez plutôt la classe **CIM \_ PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="95569-244">Instead, use the **CIM\_PowerManagementCapabilities** class.</span></span>

<span data-ttu-id="95569-245">**Description déconseillée :** Tableau qui contient les fonctionnalités de gestion de l’alimentation de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="95569-245">**Deprecated description:** An array that contains the power management capabilities of the device.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="95569-246">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="95569-246">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="95569-247">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="95569-247">**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="95569-248">**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="95569-248">**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="95569-249">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="95569-249">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="95569-250">**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="95569-250">**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="95569-251">**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="95569-251">**Power State Settable** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="95569-252">**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="95569-252">**Power Cycling Supported** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="95569-253">**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="95569-253">**Timed Power On Supported** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="95569-254">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="95569-254">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95569-255">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="95569-255">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="95569-256">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95569-256">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95569-257">Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ PowerManagementCapabilities")</span><span class="sxs-lookup"><span data-stu-id="95569-257">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_PowerManagementCapabilities")</span></span>
</dt> </dl>

<span data-ttu-id="95569-258">Cette propriété est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="95569-258">This property is deprecated.</span></span> <span data-ttu-id="95569-259">Utilisez plutôt la classe **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="95569-259">Instead, use the **PowerManagementCapabilities** class.</span></span>

<span data-ttu-id="95569-260">**Description déconseillée : true** si l’appareil logique peut être géré par l’alimentation ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="95569-260">**Deprecated description:  true** if the logical device can be power managed; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="95569-261">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="95569-261">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95569-262">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="95569-262">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="95569-263">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95569-263">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95569-264">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« heures »), **compteur**</span><span class="sxs-lookup"><span data-stu-id="95569-264">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hours"), **Counter**</span></span>
</dt> </dl>

<span data-ttu-id="95569-265">Nombre d’heures consécutives de l’alimentation de l’appareil logique depuis son dernier cycle d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="95569-265">The number of consecutive hours the logical device has been powered, since its last power cycle.</span></span>

</dd> <dt>

<span data-ttu-id="95569-266">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="95569-266">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95569-267">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="95569-267">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="95569-268">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95569-268">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95569-269">Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md).**EnabledState**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|État opérationnel DMTF \| 006,4 ")</span><span class="sxs-lookup"><span data-stu-id="95569-269">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md).**EnabledState**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|006.4")</span></span>
</dt> </dl>

<span data-ttu-id="95569-270">Cette propriété est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="95569-270">This property is deprecated.</span></span> <span data-ttu-id="95569-271">Utilisez plutôt la classe **CIM \_ PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="95569-271">Instead, use the **CIM\_PowerManagementCapabilities** class.</span></span>

<span data-ttu-id="95569-272">**Description déconseillée :** Indique si l’appareil logique est activé ou dans un état associé.</span><span class="sxs-lookup"><span data-stu-id="95569-272">**Deprecated description:** Indicates whether the logical device is enabled or in a related state.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="95569-273">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="95569-273">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="95569-274">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="95569-274">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="95569-275">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="95569-275">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="95569-276">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="95569-276">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="95569-277">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="95569-277">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="95569-278">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="95569-278">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95569-279">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="95569-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95569-280">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95569-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95569-281">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagée**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ système CIM**](cim-system.md).**CreationClassName**»)</span><span class="sxs-lookup"><span data-stu-id="95569-281">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="95569-282">Nom de la classe utilisé pour créer une instance du système qui contient l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="95569-282">The class name used to create an instance of the system that contains the logical device.</span></span> <span data-ttu-id="95569-283">**SystemCreationClassName** est combiné avec d’autres propriétés de clé de cette classe pour identifier de manière unique les instances de cette classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="95569-283">**SystemCreationClassName** is combined with other key properties of this class to uniquely identify instances of this class and its subclasses.</span></span>

</dd> <dt>

<span data-ttu-id="95569-284">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="95569-284">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95569-285">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="95569-285">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95569-286">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95569-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95569-287">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagée**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ système CIM**](cim-system.md).**Name**»)</span><span class="sxs-lookup"><span data-stu-id="95569-287">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="95569-288">Nom du système qui contient l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="95569-288">The name of the system that contains the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="95569-289">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="95569-289">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95569-290">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="95569-290">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="95569-291">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95569-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95569-292">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« heures »), **compteur**</span><span class="sxs-lookup"><span data-stu-id="95569-292">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hours"), **Counter**</span></span>
</dt> </dl>

<span data-ttu-id="95569-293">Nombre total d’heures d’alimentation de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="95569-293">The total number of hours the logical device has been powered.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="95569-294">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="95569-294">Requirements</span></span>



| <span data-ttu-id="95569-295">Condition requise</span><span class="sxs-lookup"><span data-stu-id="95569-295">Requirement</span></span> | <span data-ttu-id="95569-296">Valeur</span><span class="sxs-lookup"><span data-stu-id="95569-296">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95569-297">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="95569-297">Minimum supported client</span></span><br/> | <span data-ttu-id="95569-298">Windows 8</span><span class="sxs-lookup"><span data-stu-id="95569-298">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="95569-299">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="95569-299">Minimum supported server</span></span><br/> | <span data-ttu-id="95569-300">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="95569-300">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="95569-301">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="95569-301">Namespace</span></span><br/>                | <span data-ttu-id="95569-302">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="95569-302">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="95569-303">MOF</span><span class="sxs-lookup"><span data-stu-id="95569-303">MOF</span></span><br/>                      | <dl> <span data-ttu-id="95569-304"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="95569-304"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="95569-305">DLL</span><span class="sxs-lookup"><span data-stu-id="95569-305">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95569-306"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="95569-306"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="95569-307">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="95569-307">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95569-308">**\_ENABLEDLOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="95569-308">**CIM\_EnabledLogicalElement**</span></span>](cim-enabledlogicalelement.md)
</dt> </dl>

 

