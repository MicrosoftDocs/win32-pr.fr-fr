---
description: Représente l’état du composant d’interface de service invité, qui fournit un mécanisme permettant d’interagir avec l’ordinateur virtuel à partir des interfaces de gestion sur le système hôte.
ms.assetid: 9A158B42-052B-42B3-8539-00927056306D
title: Classe Msvm_GuestServiceInterfaceComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestServiceInterfaceComponent
- Msvm_GuestServiceInterfaceComponent.Availability
- Msvm_GuestServiceInterfaceComponent.Caption
- Msvm_GuestServiceInterfaceComponent.ConfigManagerErrorCode
- Msvm_GuestServiceInterfaceComponent.ConfigManagerUserConfig
- Msvm_GuestServiceInterfaceComponent.CreationClassName
- Msvm_GuestServiceInterfaceComponent.Description
- Msvm_GuestServiceInterfaceComponent.DeviceID
- Msvm_GuestServiceInterfaceComponent.ErrorCleared
- Msvm_GuestServiceInterfaceComponent.ErrorDescription
- Msvm_GuestServiceInterfaceComponent.InstallDate
- Msvm_GuestServiceInterfaceComponent.LastErrorCode
- Msvm_GuestServiceInterfaceComponent.Name
- Msvm_GuestServiceInterfaceComponent.PNPDeviceID
- Msvm_GuestServiceInterfaceComponent.PowerManagementCapabilities
- Msvm_GuestServiceInterfaceComponent.PowerManagementSupported
- Msvm_GuestServiceInterfaceComponent.Status
- Msvm_GuestServiceInterfaceComponent.StatusInfo
- Msvm_GuestServiceInterfaceComponent.SystemCreationClassName
- Msvm_GuestServiceInterfaceComponent.SystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4c55417edeee6d9a9fb15c474ba4ee9ca2dd93f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533746"
---
# <a name="msvm_guestserviceinterfacecomponent-class"></a><span data-ttu-id="45f8e-103">MSVM \_ GuestServiceInterfaceComponent, classe</span><span class="sxs-lookup"><span data-stu-id="45f8e-103">Msvm\_GuestServiceInterfaceComponent class</span></span>

<span data-ttu-id="45f8e-104">Représente l’état du composant d’interface de service invité, qui fournit un mécanisme permettant d’interagir avec l’ordinateur virtuel à partir des interfaces de gestion sur le système hôte.</span><span class="sxs-lookup"><span data-stu-id="45f8e-104">Represents the state of the guest service interface component, which provides a mechanism to interact with the virtual machine from the management interfaces on the host system.</span></span> <span data-ttu-id="45f8e-105">Cette classe dérive de la classe [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) .</span><span class="sxs-lookup"><span data-stu-id="45f8e-105">This class derives from the [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) class.</span></span>

<span data-ttu-id="45f8e-106">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="45f8e-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="45f8e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="45f8e-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestServiceInterfaceComponent : CIM_LogicalDevice
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
  uint32   LastErrorCode;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="45f8e-108">Membres</span><span class="sxs-lookup"><span data-stu-id="45f8e-108">Members</span></span>

<span data-ttu-id="45f8e-109">La classe **MSVM \_ GuestServiceInterfaceComponent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="45f8e-109">The **Msvm\_GuestServiceInterfaceComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="45f8e-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="45f8e-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="45f8e-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="45f8e-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="45f8e-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="45f8e-112">Methods</span></span>

<span data-ttu-id="45f8e-113">La classe **MSVM \_ GuestServiceInterfaceComponent** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="45f8e-113">The **Msvm\_GuestServiceInterfaceComponent** class has these methods.</span></span>



| <span data-ttu-id="45f8e-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="45f8e-114">Method</span></span>                                                                               | <span data-ttu-id="45f8e-115">Description</span><span class="sxs-lookup"><span data-stu-id="45f8e-115">Description</span></span>                                                                                                                              |
|:-------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="45f8e-116">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="45f8e-116">**RequestStateChange**</span></span>](requeststatechange-msvm-guestserviceinterfacecomponent.md) | <span data-ttu-id="45f8e-117">Demande que l’état du composant d’interface de service invité soit remplacé par la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="45f8e-117">Requests that the state of the guest service interface component be changed to the specified value.</span></span><br/>                           |
| [<span data-ttu-id="45f8e-118">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="45f8e-118">**Reset**</span></span>](/windows/desktop/CIMWin32Prov/reset-method-in-class-cim-logicaldevice)                        | <span data-ttu-id="45f8e-119">Demande la réinitialisation de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="45f8e-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="45f8e-120">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="45f8e-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="45f8e-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="45f8e-121">**SetPowerState**</span></span>](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-logicaldevice)        | <span data-ttu-id="45f8e-122">Définit l’état d’alimentation souhaité pour un périphérique logique et lorsqu’un appareil doit être placé dans cet État.</span><span class="sxs-lookup"><span data-stu-id="45f8e-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="45f8e-123">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="45f8e-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="45f8e-124">Propriétés</span><span class="sxs-lookup"><span data-stu-id="45f8e-124">Properties</span></span>

<span data-ttu-id="45f8e-125">La classe **MSVM \_ GuestServiceInterfaceComponent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="45f8e-125">The **Msvm\_GuestServiceInterfaceComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="45f8e-126">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="45f8e-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45f8e-127">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="45f8e-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="45f8e-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45f8e-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45f8e-129">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="45f8e-129">Availability and status of the device.</span></span>



| <span data-ttu-id="45f8e-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="45f8e-130">Value</span></span>                                                                                                                                                                                                                                                                                                              | <span data-ttu-id="45f8e-131">Signification</span><span class="sxs-lookup"><span data-stu-id="45f8e-131">Meaning</span></span>                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="45f8e-132"><dt>**Autre**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="45f8e-132"><dt>**Other**</dt> <dt>1 (0x1)</dt></span></span> </dl>                                                                                          |                                                                                                             |
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="45f8e-133"><dt>**Inconnu**</dt> <dt>2 (0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="45f8e-133"><dt>**Unknown**</dt> <dt>2 (0x2)</dt></span></span> </dl>                                                                                  |                                                                                                             |
| <span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span><dl> <span data-ttu-id="45f8e-134"><dt>**En cours d’exécution/Full Power**</dt> <dt>3 (0x3)</dt></span><span class="sxs-lookup"><span data-stu-id="45f8e-134"><dt>**Running/Full Power**</dt> <dt>3 (0x3)</dt></span></span> </dl>                                      |                                                                                                             |
| <span id="Warning"></span><span id="warning"></span><span id="WARNING"></span><dl> <span data-ttu-id="45f8e-135"><dt>**Avertissement**</dt> <dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="45f8e-135"><dt>**Warning**</dt> <dt>4 (0x4)</dt></span></span> </dl>                                                                                  |                                                                                                             |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="45f8e-136"><dt>**Dans le test**</dt> <dt>5 (0x5)</dt></span><span class="sxs-lookup"><span data-stu-id="45f8e-136"><dt>**In Test**</dt> <dt>5 (0x5)</dt></span></span> </dl>                                                                                  |                                                                                                             |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="45f8e-137"><dt>**Non applicable**</dt> <dt>6 (0x6)</dt></span><span class="sxs-lookup"><span data-stu-id="45f8e-137"><dt>**Not Applicable**</dt> <dt>6 (0x6)</dt></span></span> </dl>                                                      |                                                                                                             |
| <span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span><dl> <span data-ttu-id="45f8e-138"><dt>**Mise hors tension**</dt> <dt>7 (0x7)</dt></span><span class="sxs-lookup"><span data-stu-id="45f8e-138"><dt>**Power Off**</dt> <dt>7 (0x7)</dt></span></span> </dl>                                                                          |                                                                                                             |
| <span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span><dl> <span data-ttu-id="45f8e-139"><dt>**Hors ligne**</dt> <dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="45f8e-139"><dt>**Off Line**</dt> <dt>8 (0x8)</dt></span></span> </dl>                                                                              |                                                                                                             |
| <span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span><dl> <span data-ttu-id="45f8e-140"><dt>**Hors droit**</dt> <dt>9 (0x9)</dt></span><span class="sxs-lookup"><span data-stu-id="45f8e-140"><dt>**Off Duty**</dt> <dt>9 (0x9)</dt></span></span> </dl>                                                                              |                                                                                                             |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <span data-ttu-id="45f8e-141"><dt></dt> <dt>10 (0xA)</dt> détérioré</span><span class="sxs-lookup"><span data-stu-id="45f8e-141"><dt>**Degraded**</dt> <dt>10 (0xA)</dt></span></span> </dl>                                                                             |                                                                                                             |
| <span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span><dl> <span data-ttu-id="45f8e-142"><dt>**Non installé**</dt> <dt>11 (0xB)</dt></span><span class="sxs-lookup"><span data-stu-id="45f8e-142"><dt>**Not Installed**</dt> <dt>11 (0xB)</dt></span></span> </dl>                                                         |                                                                                                             |
| <span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span><dl> <span data-ttu-id="45f8e-143"><dt>**Erreur d’installation**</dt> <dt>12 (0xc)</dt></span><span class="sxs-lookup"><span data-stu-id="45f8e-143"><dt>**Install Error**</dt> <dt>12 (0xC)</dt></span></span> </dl>                                                         |                                                                                                             |
| <span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span><dl> <span data-ttu-id="45f8e-144">Économie <dt>**d’énergie-inconnu**</dt> <dt>13 (0xD)</dt></span><span class="sxs-lookup"><span data-stu-id="45f8e-144"><dt>**Power Save - Unknown**</dt> <dt>13 (0xD)</dt></span></span> </dl>                             | <span data-ttu-id="45f8e-145">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="45f8e-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span><br/>                 |
| <span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span><dl> <span data-ttu-id="45f8e-146">Économie <dt>**d’énergie-mode basse puissance**</dt> <dt>14 (0xE)</dt></span><span class="sxs-lookup"><span data-stu-id="45f8e-146"><dt>**Power Save - Low Power Mode**</dt> <dt>14 (0xE)</dt></span></span> </dl> | <span data-ttu-id="45f8e-147">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="45f8e-147">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span><br/> |
| <span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span><dl> <span data-ttu-id="45f8e-148">Économie <dt>**d’énergie-secours**</dt> <dt>15 (0xF)</dt></span><span class="sxs-lookup"><span data-stu-id="45f8e-148"><dt>**Power Save - Standby**</dt> <dt>15 (0xF)</dt></span></span> </dl>                             | <span data-ttu-id="45f8e-149">L’appareil ne fonctionne pas mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="45f8e-149">The device is not functioning but could be brought to full power quickly.</span></span><br/>                        |
| <span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span><dl> <span data-ttu-id="45f8e-150"><dt>**Power cycle**</dt> <dt>16 (0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="45f8e-150"><dt>**Power Cycle**</dt> <dt>16 (0x10)</dt></span></span> </dl>                                                                |                                                                                                             |
| <span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span><dl> <span data-ttu-id="45f8e-151">Économie <dt>**d’énergie-Avertissement**</dt> <dt>17 (0x11)</dt></span><span class="sxs-lookup"><span data-stu-id="45f8e-151"><dt>**Power Save - Warning**</dt> <dt>17 (0x11)</dt></span></span> </dl>                            | <span data-ttu-id="45f8e-152">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="45f8e-152">The device is in a warning state, though also in a power save mode.</span></span><br/>                              |



 

</dd> <dt>

<span data-ttu-id="45f8e-153">**Caption**</span><span class="sxs-lookup"><span data-stu-id="45f8e-153">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45f8e-154">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="45f8e-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45f8e-155">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45f8e-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45f8e-156">Courte description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="45f8e-156">Short textual description of the object.</span></span> <span data-ttu-id="45f8e-157">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="45f8e-157">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="45f8e-158">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="45f8e-158">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45f8e-159">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="45f8e-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="45f8e-160">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45f8e-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45f8e-161">Code d’erreur Configuration Manager Win32.</span><span class="sxs-lookup"><span data-stu-id="45f8e-161">Win32 Configuration Manager error code.</span></span>



| <span data-ttu-id="45f8e-162">Valeur</span><span class="sxs-lookup"><span data-stu-id="45f8e-162">Value</span></span>                                                                                | <span data-ttu-id="45f8e-163">Signification</span><span class="sxs-lookup"><span data-stu-id="45f8e-163">Meaning</span></span>                                                                                                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="45f8e-164"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="45f8e-164"><dt>0 (0x0)</dt></span></span> </dl>   | <span data-ttu-id="45f8e-165">L’appareil fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="45f8e-165">Device is working properly.</span></span><br/>                                                                                                   |
| <dl> <span data-ttu-id="45f8e-166"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="45f8e-166"><dt>1 (0x1)</dt></span></span> </dl>   | <span data-ttu-id="45f8e-167">L’appareil n’est pas configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="45f8e-167">Device is not configured correctly.</span></span><br/>                                                                                           |
| <dl> <span data-ttu-id="45f8e-168"><dt>2 (0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="45f8e-168"><dt>2 (0x2)</dt></span></span> </dl>   | <span data-ttu-id="45f8e-169">Windows ne peut pas charger le pilote de cet appareil.</span><span class="sxs-lookup"><span data-stu-id="45f8e-169">Windows cannot load the driver for this device.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="45f8e-170"><dt>3 (0x3)</dt></span><span class="sxs-lookup"><span data-stu-id="45f8e-170"><dt>3 (0x3)</dt></span></span> </dl>   | <span data-ttu-id="45f8e-171">Le pilote de cet appareil est peut-être endommagé ou la mémoire ou d’autres ressources du système sont peut-être insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="45f8e-171">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span><br/>                             |
| <dl> <span data-ttu-id="45f8e-172"><dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="45f8e-172"><dt>4 (0x4)</dt></span></span> </dl>   | <span data-ttu-id="45f8e-173">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="45f8e-173">Device is not working properly.</span></span> <span data-ttu-id="45f8e-174">L’un de ses pilotes ou le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="45f8e-174">One of its drivers or the registry might be corrupted.</span></span><br/>                                        |
| <dl> <span data-ttu-id="45f8e-175"><dt>5 (0x5)</dt></span><span class="sxs-lookup"><span data-stu-id="45f8e-175"><dt>5 (0x5)</dt></span></span> </dl>   | <span data-ttu-id="45f8e-176">Le pilote de l’appareil requiert une ressource que Windows ne peut pas gérer.</span><span class="sxs-lookup"><span data-stu-id="45f8e-176">Driver for the device requires a resource that Windows cannot manage.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="45f8e-177"><dt>6 (0x6)</dt></span><span class="sxs-lookup"><span data-stu-id="45f8e-177"><dt>6 (0x6)</dt></span></span> </dl>   | <span data-ttu-id="45f8e-178">La configuration de démarrage de l’appareil est en conflit avec d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="45f8e-178">Boot configuration for the device conflicts with other devices.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="45f8e-179"><dt>7 (0x7)</dt></span><span class="sxs-lookup"><span data-stu-id="45f8e-179"><dt>7 (0x7)</dt></span></span> </dl>   | <span data-ttu-id="45f8e-180">Impossible de filtrer.</span><span class="sxs-lookup"><span data-stu-id="45f8e-180">Cannot filter.</span></span><br/>                                                                                                                |
| <dl> <span data-ttu-id="45f8e-181"><dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="45f8e-181"><dt>8 (0x8)</dt></span></span> </dl>   | <span data-ttu-id="45f8e-182">Le chargeur de pilote de l’appareil est manquant.</span><span class="sxs-lookup"><span data-stu-id="45f8e-182">Driver loader for the device is missing.</span></span><br/>                                                                                      |
| <dl> <span data-ttu-id="45f8e-183"><dt>9 (0x9)</dt></span><span class="sxs-lookup"><span data-stu-id="45f8e-183"><dt>9 (0x9)</dt></span></span> </dl>   | <span data-ttu-id="45f8e-184">L’appareil ne fonctionne pas correctement ; le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="45f8e-184">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span><br/>               |
| <dl> <span data-ttu-id="45f8e-185"><dt>10 (0xA)</dt></span><span class="sxs-lookup"><span data-stu-id="45f8e-185"><dt>10 (0xA)</dt></span></span> </dl>  | <span data-ttu-id="45f8e-186">Impossible de démarrer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="45f8e-186">Device cannot start.</span></span><br/>                                                                                                          |
| <dl> <span data-ttu-id="45f8e-187"><dt>11 (0xB)</dt></span><span class="sxs-lookup"><span data-stu-id="45f8e-187"><dt>11 (0xB)</dt></span></span> </dl>  | <span data-ttu-id="45f8e-188">Échec de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="45f8e-188">Device failed.</span></span><br/>                                                                                                                |
| <dl> <span data-ttu-id="45f8e-189"><dt>12 (0xC)</dt></span><span class="sxs-lookup"><span data-stu-id="45f8e-189"><dt>12 (0xC)</dt></span></span> </dl>  | <span data-ttu-id="45f8e-190">L’appareil ne peut pas trouver suffisamment de ressources libres à utiliser.</span><span class="sxs-lookup"><span data-stu-id="45f8e-190">Device cannot find enough free resources to use.</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="45f8e-191"><dt>13 (0xD)</dt></span><span class="sxs-lookup"><span data-stu-id="45f8e-191"><dt>13 (0xD)</dt></span></span> </dl>  | <span data-ttu-id="45f8e-192">Windows ne peut pas vérifier les ressources de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="45f8e-192">Windows cannot verify the device's resources.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="45f8e-193"><dt>14 (0xE)</dt></span><span class="sxs-lookup"><span data-stu-id="45f8e-193"><dt>14 (0xE)</dt></span></span> </dl>  | <span data-ttu-id="45f8e-194">L’appareil ne peut pas fonctionner correctement tant que l’ordinateur n’a pas redémarré.</span><span class="sxs-lookup"><span data-stu-id="45f8e-194">Device cannot work properly until the computer is restarted.</span></span><br/>                                                                  |
| <dl> <span data-ttu-id="45f8e-195"><dt>15 (0xF)</dt></span><span class="sxs-lookup"><span data-stu-id="45f8e-195"><dt>15 (0xF)</dt></span></span> </dl>  | <span data-ttu-id="45f8e-196">L’appareil ne fonctionne pas correctement en raison d’un éventuel problème de réénumération.</span><span class="sxs-lookup"><span data-stu-id="45f8e-196">Device is not working properly due to a possible re-enumeration problem.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="45f8e-197"><dt>16 (0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="45f8e-197"><dt>16 (0x10)</dt></span></span> </dl> | <span data-ttu-id="45f8e-198">Windows ne peut pas identifier toutes les ressources utilisées par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="45f8e-198">Windows cannot identify all of the resources that the device uses.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="45f8e-199"><dt>17 (0x11)</dt></span><span class="sxs-lookup"><span data-stu-id="45f8e-199"><dt>17 (0x11)</dt></span></span> </dl> | <span data-ttu-id="45f8e-200">L’appareil demande un type de ressource inconnu.</span><span class="sxs-lookup"><span data-stu-id="45f8e-200">Device is requesting an unknown resource type.</span></span><br/>                                                                                |
| <dl> <span data-ttu-id="45f8e-201"><dt>18 (0x12)</dt></span><span class="sxs-lookup"><span data-stu-id="45f8e-201"><dt>18 (0x12)</dt></span></span> </dl> | <span data-ttu-id="45f8e-202">Les pilotes de périphérique doivent être réinstallés.</span><span class="sxs-lookup"><span data-stu-id="45f8e-202">Device drivers must be reinstalled.</span></span><br/>                                                                                           |
| <dl> <span data-ttu-id="45f8e-203"><dt>19 (0x13)</dt></span><span class="sxs-lookup"><span data-stu-id="45f8e-203"><dt>19 (0x13)</dt></span></span> </dl> | <span data-ttu-id="45f8e-204">Échec lors de l’utilisation du chargeur VxD.</span><span class="sxs-lookup"><span data-stu-id="45f8e-204">Failure using the VxD loader.</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="45f8e-205"><dt>20 (0x14)</dt></span><span class="sxs-lookup"><span data-stu-id="45f8e-205"><dt>20 (0x14)</dt></span></span> </dl> | <span data-ttu-id="45f8e-206">Le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="45f8e-206">Registry might be corrupted.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="45f8e-207"><dt>21 (0x15)</dt></span><span class="sxs-lookup"><span data-stu-id="45f8e-207"><dt>21 (0x15)</dt></span></span> </dl> | <span data-ttu-id="45f8e-208">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="45f8e-208">System failure.</span></span> <span data-ttu-id="45f8e-209">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="45f8e-209">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="45f8e-210">Windows supprime l’appareil.</span><span class="sxs-lookup"><span data-stu-id="45f8e-210">Windows is removing the device.</span></span><br/> |
| <dl> <span data-ttu-id="45f8e-211"><dt>22 (0x16)</dt></span><span class="sxs-lookup"><span data-stu-id="45f8e-211"><dt>22 (0x16)</dt></span></span> </dl> | <span data-ttu-id="45f8e-212">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="45f8e-212">Device is disabled.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="45f8e-213"><dt>23 (0x17)</dt></span><span class="sxs-lookup"><span data-stu-id="45f8e-213"><dt>23 (0x17)</dt></span></span> </dl> | <span data-ttu-id="45f8e-214">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="45f8e-214">System failure.</span></span> <span data-ttu-id="45f8e-215">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="45f8e-215">If changing the device driver is ineffective, see the hardware documentation.</span></span><br/>                                 |
| <dl> <span data-ttu-id="45f8e-216"><dt>24 (0x18)</dt></span><span class="sxs-lookup"><span data-stu-id="45f8e-216"><dt>24 (0x18)</dt></span></span> </dl> | <span data-ttu-id="45f8e-217">L’appareil n’est pas présent, ne fonctionne pas correctement ou n’a pas tous ses pilotes installés.</span><span class="sxs-lookup"><span data-stu-id="45f8e-217">Device is not present, not working properly, or does not have all of its drivers installed.</span></span><br/>                                   |
| <dl> <span data-ttu-id="45f8e-218"><dt>25 (0x19)</dt></span><span class="sxs-lookup"><span data-stu-id="45f8e-218"><dt>25 (0x19)</dt></span></span> </dl> | <span data-ttu-id="45f8e-219">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="45f8e-219">Windows is still setting up the device.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="45f8e-220"><dt>26 (0x1A)</dt></span><span class="sxs-lookup"><span data-stu-id="45f8e-220"><dt>26 (0x1A)</dt></span></span> </dl> | <span data-ttu-id="45f8e-221">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="45f8e-221">Windows is still setting up the device.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="45f8e-222"><dt>27 (0x1B)</dt></span><span class="sxs-lookup"><span data-stu-id="45f8e-222"><dt>27 (0x1B)</dt></span></span> </dl> | <span data-ttu-id="45f8e-223">L’appareil n’a pas une configuration de journal valide.</span><span class="sxs-lookup"><span data-stu-id="45f8e-223">Device does not have valid log configuration.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="45f8e-224"><dt>28 (0x1C)</dt></span><span class="sxs-lookup"><span data-stu-id="45f8e-224"><dt>28 (0x1C)</dt></span></span> </dl> | <span data-ttu-id="45f8e-225">Les pilotes de périphérique ne sont pas installés.</span><span class="sxs-lookup"><span data-stu-id="45f8e-225">Device drivers are not installed.</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="45f8e-226"><dt>29 (0x1D)</dt></span><span class="sxs-lookup"><span data-stu-id="45f8e-226"><dt>29 (0x1D)</dt></span></span> </dl> | <span data-ttu-id="45f8e-227">L’appareil est désactivé ; le microprogramme de l’appareil n’a pas fourni les ressources requises.</span><span class="sxs-lookup"><span data-stu-id="45f8e-227">Device is disabled; the device firmware did not provide the required resources.</span></span><br/>                                               |
| <dl> <span data-ttu-id="45f8e-228"><dt>30 (0x1E)</dt></span><span class="sxs-lookup"><span data-stu-id="45f8e-228"><dt>30 (0x1E)</dt></span></span> </dl> | <span data-ttu-id="45f8e-229">L’appareil utilise une ressource IRQ qu’un autre appareil utilise.</span><span class="sxs-lookup"><span data-stu-id="45f8e-229">Device is using an IRQ resource that another device is using.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="45f8e-230"><dt>31 (0x1F)</dt></span><span class="sxs-lookup"><span data-stu-id="45f8e-230"><dt>31 (0x1F)</dt></span></span> </dl> | <span data-ttu-id="45f8e-231">L’appareil ne fonctionne pas correctement ; Windows ne peut pas charger les pilotes de périphérique requis.</span><span class="sxs-lookup"><span data-stu-id="45f8e-231">Device is not working properly; Windows cannot load the required device drivers.</span></span><br/>                                              |



 

</dd> <dt>

<span data-ttu-id="45f8e-232">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="45f8e-232">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45f8e-233">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="45f8e-233">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="45f8e-234">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45f8e-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45f8e-235">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="45f8e-235">If **TRUE**, the device is using a user-defined configuration.</span></span>

</dd> <dt>

<span data-ttu-id="45f8e-236">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="45f8e-236">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45f8e-237">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="45f8e-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45f8e-238">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45f8e-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45f8e-239">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="45f8e-239">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="45f8e-240">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="45f8e-240">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="45f8e-241">**Description**</span><span class="sxs-lookup"><span data-stu-id="45f8e-241">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45f8e-242">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="45f8e-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45f8e-243">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45f8e-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45f8e-244">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="45f8e-244">Textual description of the object.</span></span> <span data-ttu-id="45f8e-245">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="45f8e-245">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="45f8e-246">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="45f8e-246">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45f8e-247">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="45f8e-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45f8e-248">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45f8e-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45f8e-249">Adresse ou d’autres informations d’identification pour nommer de manière unique l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="45f8e-249">Address or other identifying information to uniquely name the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="45f8e-250">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="45f8e-250">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45f8e-251">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="45f8e-251">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="45f8e-252">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45f8e-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45f8e-253">Si la **valeur est true**, l’erreur signalée dans la propriété **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="45f8e-253">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

</dd> <dt>

<span data-ttu-id="45f8e-254">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="45f8e-254">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45f8e-255">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="45f8e-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45f8e-256">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45f8e-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45f8e-257">Chaîne de forme libre qui fournit des informations sur l’erreur enregistrée dans la propriété **LastErrorCode** et les actions correctives à effectuer.</span><span class="sxs-lookup"><span data-stu-id="45f8e-257">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

</dd> <dt>

<span data-ttu-id="45f8e-258">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="45f8e-258">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45f8e-259">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="45f8e-259">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="45f8e-260">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45f8e-260">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45f8e-261">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="45f8e-261">Date and time the object was installed.</span></span> <span data-ttu-id="45f8e-262">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="45f8e-262">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="45f8e-263">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="45f8e-263">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="45f8e-264">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="45f8e-264">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45f8e-265">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="45f8e-265">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="45f8e-266">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45f8e-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45f8e-267">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="45f8e-267">Last error code reported by the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="45f8e-268">**Nom**</span><span class="sxs-lookup"><span data-stu-id="45f8e-268">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45f8e-269">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="45f8e-269">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45f8e-270">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45f8e-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45f8e-271">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="45f8e-271">Label by which the object is known.</span></span> <span data-ttu-id="45f8e-272">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="45f8e-272">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="45f8e-273">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="45f8e-273">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="45f8e-274">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="45f8e-274">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45f8e-275">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="45f8e-275">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45f8e-276">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45f8e-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45f8e-277">Indique l’identificateur d’appareil Plug-and-Play Win32 de l’appareil logique.</span><span class="sxs-lookup"><span data-stu-id="45f8e-277">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="45f8e-278">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="45f8e-278">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="45f8e-279">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="45f8e-279">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45f8e-280">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="45f8e-280">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="45f8e-281">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45f8e-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45f8e-282">Tableau des fonctionnalités d’alimentation spécifiques d’un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="45f8e-282">Array of the specific power-related capabilities of a logical device.</span></span> <span data-ttu-id="45f8e-283">Cette propriété est héritée de **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="45f8e-283">This property is inherited from **CIM\_LogicalDevice**.</span></span>



| <span data-ttu-id="45f8e-284">Valeur</span><span class="sxs-lookup"><span data-stu-id="45f8e-284">Value</span></span>                                                                                                                                                                                                                                                                                                                                                                 | <span data-ttu-id="45f8e-285">Signification</span><span class="sxs-lookup"><span data-stu-id="45f8e-285">Meaning</span></span>                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="45f8e-286"><dt>**Inconnu**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="45f8e-286"><dt>**Unknown**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                                                                                                     |                                                                                                                                                                                                                                                                                                                                      |
| <span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span><dl> <span data-ttu-id="45f8e-287"><dt>**Non pris en charge**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="45f8e-287"><dt>**Not Supported**</dt> <dt>1 (0x1)</dt></span></span> </dl>                                                                                                             |                                                                                                                                                                                                                                                                                                                                      |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="45f8e-288"><dt>**Désactivé**</dt> <dt>2 (0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="45f8e-288"><dt>**Disabled**</dt> <dt>2 (0x2)</dt></span></span> </dl>                                                                                                                                 |                                                                                                                                                                                                                                                                                                                                      |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="45f8e-289"><dt>**Activé**</dt> <dt>3 (0x3)</dt></span><span class="sxs-lookup"><span data-stu-id="45f8e-289"><dt>**Enabled**</dt> <dt>3 (0x3)</dt></span></span> </dl>                                                                                                                                     | <span data-ttu-id="45f8e-290">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="45f8e-290">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span><br/>                                                                                                                                                                                               |
| <span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span><dl> <span data-ttu-id="45f8e-291"><dt>**Modes d’économie d’énergie entrés automatiquement**</dt> <dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="45f8e-291"><dt>**Power Saving Modes Entered Automatically**</dt> <dt>4 (0x4)</dt></span></span> </dl> | <span data-ttu-id="45f8e-292">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="45f8e-292">The device can change its power state based on usage or other criteria.</span></span><br/>                                                                                                                                                                                                                                                   |
| <span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span><dl> <span data-ttu-id="45f8e-293"><dt>**État d’alimentation définissable**</dt> <dt>5 (0x5)</dt></span><span class="sxs-lookup"><span data-stu-id="45f8e-293"><dt>**Power State Settable**</dt> <dt>5 (0x5)</dt></span></span> </dl>                                                                                 | <span data-ttu-id="45f8e-294">La méthode [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="45f8e-294">The [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) method is supported.</span></span> <span data-ttu-id="45f8e-295">Cette méthode se trouve sur la classe parente du **\_ LogicalDevice CIM** et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="45f8e-295">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="45f8e-296">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="45f8e-296">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span><br/> |
| <span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span><dl> <span data-ttu-id="45f8e-297"><dt>**Cycle d’alimentation pris en charge**</dt> <dt>6 (0x6)</dt></span><span class="sxs-lookup"><span data-stu-id="45f8e-297"><dt>**Power Cycling Supported**</dt> <dt>6 (0x6)</dt></span></span> </dl>                                                                     | <span data-ttu-id="45f8e-298">La méthode [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) peut être appelée avec le paramètre *PowerState* défini sur 5 (« Power cycle »).</span><span class="sxs-lookup"><span data-stu-id="45f8e-298">The [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span><br/>                                                                                                                                                            |
| <span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span><dl> <span data-ttu-id="45f8e-299"><dt>**Mise sous tension minutée**</dt> <dt>7 (0X7)</dt> pris en charge</span><span class="sxs-lookup"><span data-stu-id="45f8e-299"><dt>**Timed Power On Supported**</dt> <dt>7 (0x7)</dt></span></span> </dl>                                                                 | <span data-ttu-id="45f8e-300">La méthode [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) peut être appelée avec le paramètre *PowerState* défini sur 5 (« Power cycle ») et l' *heure* définie sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="45f8e-300">The [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and *Time* set to a specific date and time, or interval, for power-on.</span></span><br/>                                                                                       |



 

</dd> <dt>

<span data-ttu-id="45f8e-301">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="45f8e-301">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45f8e-302">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="45f8e-302">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="45f8e-303">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45f8e-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45f8e-304">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation, c’est-à-dire être mis en état d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="45f8e-304">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="45f8e-305">Si la valeur est **false**, la valeur entière 1 (« non pris en charge ») doit être la seule entrée dans le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="45f8e-305">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="45f8e-306">Cette propriété n’indique pas si les fonctionnalités de gestion de l’alimentation sont actuellement activées, ou si elles sont activées, quelles sont les fonctionnalités prises en charge.</span><span class="sxs-lookup"><span data-stu-id="45f8e-306">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="45f8e-307">Pour plus d’informations, consultez le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="45f8e-307">For more information, see the **PowerManagementCapabilities** array.</span></span>

</dd> <dt>

<span data-ttu-id="45f8e-308">**État**</span><span class="sxs-lookup"><span data-stu-id="45f8e-308">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45f8e-309">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="45f8e-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45f8e-310">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45f8e-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45f8e-311">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="45f8e-311">Current status of the object.</span></span> <span data-ttu-id="45f8e-312">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="45f8e-312">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="45f8e-313">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="45f8e-313">Values include the following:</span></span>

<dl><span id="OK"></span><span id="ok"></span><dt>

<span data-ttu-id="45f8e-314">**OK**</span><span class="sxs-lookup"><span data-stu-id="45f8e-314">**"OK"**</span></span>
</dt><span id="Error"></span><span id="error"></span><span id="ERROR"></span><dt>

<span data-ttu-id="45f8e-315">**Erreurs**</span><span class="sxs-lookup"><span data-stu-id="45f8e-315">**"Error"**</span></span>
</dt><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dt>

<span data-ttu-id="45f8e-316">**Détérioré**</span><span class="sxs-lookup"><span data-stu-id="45f8e-316">**"Degraded"**</span></span>
</dt><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dt>

<span data-ttu-id="45f8e-317">**Connue**</span><span class="sxs-lookup"><span data-stu-id="45f8e-317">**"Unknown"**</span></span>
</dt><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span><dt>

<span data-ttu-id="45f8e-318">**« Échec prévu »**</span><span class="sxs-lookup"><span data-stu-id="45f8e-318">**"Pred Fail"**</span></span>
</dt><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dt>

<span data-ttu-id="45f8e-319">**Démarr**</span><span class="sxs-lookup"><span data-stu-id="45f8e-319">**"Starting"**</span></span>
</dt><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span><dt>

<span data-ttu-id="45f8e-320">**Arrêt**</span><span class="sxs-lookup"><span data-stu-id="45f8e-320">**"Stopping"**</span></span>
</dt><span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dt>

<span data-ttu-id="45f8e-321">**Services**</span><span class="sxs-lookup"><span data-stu-id="45f8e-321">**"Service"**</span></span>
</dt><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span><dt>

<span data-ttu-id="45f8e-322">**Trop sollicité**</span><span class="sxs-lookup"><span data-stu-id="45f8e-322">**"Stressed"**</span></span>
</dt><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span><dt>

<span data-ttu-id="45f8e-323">**« Non récupéré »**</span><span class="sxs-lookup"><span data-stu-id="45f8e-323">**"NonRecover"**</span></span>
</dt><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dt>

<span data-ttu-id="45f8e-324">**« Aucun contact »**</span><span class="sxs-lookup"><span data-stu-id="45f8e-324">**"No Contact"**</span></span>
</dt><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span><dt>

<span data-ttu-id="45f8e-325">**« Comm. perdue »**</span><span class="sxs-lookup"><span data-stu-id="45f8e-325">**"Lost Comm"**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="45f8e-326">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="45f8e-326">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45f8e-327">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="45f8e-327">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="45f8e-328">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45f8e-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45f8e-329">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="45f8e-329">State of the logical device.</span></span> <span data-ttu-id="45f8e-330">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (« non applicable ») doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="45f8e-330">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span> <span data-ttu-id="45f8e-331">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="45f8e-331">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

<dl> <dt>

<span data-ttu-id="45f8e-332"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="45f8e-332"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1 (0x1))</span></span>
</dt> <dt>

<span data-ttu-id="45f8e-333"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2 (0X2))</span><span class="sxs-lookup"><span data-stu-id="45f8e-333"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2 (0x2))</span></span>
</dt> <dt>

<span data-ttu-id="45f8e-334"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3 (0x3))</span><span class="sxs-lookup"><span data-stu-id="45f8e-334"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3 (0x3))</span></span>
</dt> <dt>

<span data-ttu-id="45f8e-335"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="45f8e-335"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (4 (0x4))</span></span>
</dt> <dt>

<span data-ttu-id="45f8e-336"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (5 (0x5))</span><span class="sxs-lookup"><span data-stu-id="45f8e-336"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (5 (0x5))</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="45f8e-337">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="45f8e-337">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45f8e-338">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="45f8e-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45f8e-339">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45f8e-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45f8e-340">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="45f8e-340">Scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="45f8e-341">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="45f8e-341">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45f8e-342">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="45f8e-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45f8e-343">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45f8e-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45f8e-344">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="45f8e-344">Scoping system's name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="45f8e-345">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="45f8e-345">Requirements</span></span>



| <span data-ttu-id="45f8e-346">Condition requise</span><span class="sxs-lookup"><span data-stu-id="45f8e-346">Requirement</span></span> | <span data-ttu-id="45f8e-347">Valeur</span><span class="sxs-lookup"><span data-stu-id="45f8e-347">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45f8e-348">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="45f8e-348">Minimum supported client</span></span><br/> | <span data-ttu-id="45f8e-349">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="45f8e-349">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="45f8e-350">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="45f8e-350">Minimum supported server</span></span><br/> | <span data-ttu-id="45f8e-351">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="45f8e-351">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="45f8e-352">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="45f8e-352">Namespace</span></span><br/>                | <span data-ttu-id="45f8e-353">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="45f8e-353">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="45f8e-354">MOF</span><span class="sxs-lookup"><span data-stu-id="45f8e-354">MOF</span></span><br/>                      | <dl> <span data-ttu-id="45f8e-355"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="45f8e-355"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="45f8e-356">DLL</span><span class="sxs-lookup"><span data-stu-id="45f8e-356">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45f8e-357"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="45f8e-357"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="45f8e-358">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="45f8e-358">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45f8e-359">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="45f8e-359">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="45f8e-360">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="45f8e-360">**CIM\_LogicalDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicaldevice)
</dt> </dl>

 

