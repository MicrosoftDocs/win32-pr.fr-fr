---
description: La \_ classe du processeur CIM représente les fonctionnalités et la gestion du périphérique logique du processeur.
ms.assetid: 7af3208f-f1d5-4911-b6ab-46b54eec0b69
ms.tgt_platform: multiple
title: CIM_Processor, classe (fournisseurs WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Processor
- CIM_Processor.AddressWidth
- CIM_Processor.Availability
- CIM_Processor.Caption
- CIM_Processor.ConfigManagerErrorCode
- CIM_Processor.ConfigManagerUserConfig
- CIM_Processor.CreationClassName
- CIM_Processor.CurrentClockSpeed
- CIM_Processor.DataWidth
- CIM_Processor.Description
- CIM_Processor.DeviceID
- CIM_Processor.ErrorCleared
- CIM_Processor.ErrorDescription
- CIM_Processor.Family
- CIM_Processor.InstallDate
- CIM_Processor.LastErrorCode
- CIM_Processor.LoadPercentage
- CIM_Processor.MaxClockSpeed
- CIM_Processor.Name
- CIM_Processor.OtherFamilyDescription
- CIM_Processor.PNPDeviceID
- CIM_Processor.PowerManagementCapabilities
- CIM_Processor.PowerManagementSupported
- CIM_Processor.Role
- CIM_Processor.Status
- CIM_Processor.StatusInfo
- CIM_Processor.Stepping
- CIM_Processor.SystemCreationClassName
- CIM_Processor.SystemName
- CIM_Processor.UniqueId
- CIM_Processor.UpgradeMethod
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0120ce0327c21098b8c2950bd5dfa9a9fe2a709c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483000"
---
# <a name="cim_processor-class-cimwin32-wmi-providers"></a>CIM_Processor, classe (fournisseurs WMI CIMWin32)

La classe du **\_ processeur CIM** représente les fonctionnalités et la gestion du périphérique logique du processeur.

> [!IMPORTANT]
> Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées. WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Abstract, UUID("{8502C54B-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Processor : CIM_LogicalDevice
{
  uint16   AddressWidth;
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint32   CurrentClockSpeed;
  uint16   DataWidth;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint16   Family;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint16   LoadPercentage;
  uint32   MaxClockSpeed;
  string   Name;
  string   OtherFamilyDescription;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Role;
  string   Status;
  uint16   StatusInfo;
  string   Stepping;
  string   SystemCreationClassName;
  string   SystemName;
  string   UniqueId;
  uint16   UpgradeMethod;
};
```

## <a name="members"></a>Membres

La classe de **\_ processeur CIM** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe du **\_ processeur CIM** possède ces méthodes.



| Méthode                                                               | Description                                                                                                                              |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [**Réinitialiser**](reset-method-in-class-cim-processor.md)                 | Demande la réinitialisation de l’unité logique. Non implémenté par WMI.<br/>                                                               |
| [**SetPowerState**](setpowerstate-method-in-class-cim-processor.md) | Définit l’état d’alimentation souhaité pour un périphérique logique et lorsqu’un appareil doit être placé dans cet État. Non implémenté par WMI.<br/> |



 

### <a name="properties"></a>Propriétés

La classe du **\_ processeur CIM** possède ces propriétés.

<dl> <dt>

**AddressWidth**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« bits »)
</dt> </dl>

Largeur de l’adresse du processeur, en bits.

</dd> <dt>

**Disponibilité**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")
</dt> </dl>

Disponibilité et état de l’appareil.

Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)


</dt> <dd>

En cours d’exécution ou pleine puissance

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)


</dt> <dd>

L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)


</dt> <dd>

L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)


</dt> <dd>

L’appareil ne fonctionne pas, mais peut être mis à la pleine puissance rapidement.

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)


</dt> <dd>

L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)


</dt> <dd>

L’appareil est suspendu.

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)


</dt> <dd>

Le périphérique n’est pas prêt.

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)


</dt> <dd>

L’appareil n’est pas configuré.

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)


</dt> <dd>

L’appareil est calme.

</dd> </dl>

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)
</dt> </dl>

Courte description textuelle de l’objet.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**ConfigManagerErrorCode**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")
</dt> </dl>

Code d’erreur Configuration Manager Win32.

Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Ce périphérique fonctionne correctement.**  (0)


</dt> <dd>

L’appareil fonctionne correctement.

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Ce périphérique n’est pas configuré correctement.** (1)


</dt> <dd>

L’appareil n’est pas configuré correctement.

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows ne peut pas charger le pilote de cet appareil.** (2)


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.** (3)


</dt> <dd>

Le pilote de cet appareil est peut-être endommagé ou la mémoire ou d’autres ressources du système sont peut-être insuffisantes.

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.** (4)


</dt> <dd>

L’appareil ne fonctionne pas correctement. L’un de ses pilotes ou le Registre est peut-être endommagé.

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.** (5)


</dt> <dd>

Le pilote de l’appareil requiert une ressource que Windows ne peut pas gérer.

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**  (6)


</dt> <dd>

La configuration de démarrage de l’appareil est en conflit avec d’autres appareils.

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossible de filtrer.** (7)


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Le chargeur de pilote de l’appareil est manquant.** (8)


</dt> <dd>

Le chargeur de pilote de l’appareil est manquant.

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.** (9)


</dt> <dd>

L’appareil ne fonctionne pas correctement. Le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossible de démarrer cet appareil.** (10)


</dt> <dd>

Impossible de démarrer l’appareil.

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Échec de cet appareil.** (11)


</dt> <dd>

Échec de l’appareil.

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.** douze


</dt> <dd>

L’appareil ne peut pas trouver suffisamment de ressources libres à utiliser.

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows ne peut pas vérifier les ressources de cet appareil.** (13)


</dt> <dd>

Windows ne peut pas vérifier les ressources de l’appareil.

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.** (14)


</dt> <dd>

L’appareil ne peut pas fonctionner correctement tant que l’ordinateur n’a pas redémarré.

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.** (15)


</dt> <dd>

L’appareil ne fonctionne pas correctement en raison d’un éventuel problème de réénumération.

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.** (16)


</dt> <dd>

Windows ne peut pas identifier toutes les ressources utilisées par l’appareil.

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Ce périphérique demande un type de ressource inconnu.** (17)


</dt> <dd>

L’appareil demande un type de ressource inconnu.

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Réinstallez les pilotes pour cet appareil.** (18)


</dt> <dd>

Les pilotes de périphérique doivent être réinstallés.

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Échec lors de l’utilisation du chargeur VxD.** (19)


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Votre registre est peut-être endommagé.** (20)


</dt> <dd>

Le Registre est peut-être endommagé.

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.** (21)


</dt> <dd>

Défaillance du système. Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel. Windows supprime l’appareil.

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Cet appareil est désactivé.** (22)


</dt> <dd>

L’appareil est désactivé.

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.** (23)


</dt> <dd>

Défaillance du système. Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.** (24)


</dt> <dd>

L’appareil n’est pas présent, ne fonctionne pas correctement ou n’a pas tous ses pilotes installés.

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.** (25)


</dt> <dd>

Windows est toujours en cours de configuration de l’appareil.

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.** (26)


</dt> <dd>

Windows est toujours en cours de configuration de l’appareil.

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Cet appareil n’a pas de configuration de journal valide.** (27)


</dt> <dd>

L’appareil n’a pas une configuration de journal valide.

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Les pilotes de cet appareil ne sont pas installés.** (28)


</dt> <dd>

Les pilotes de périphérique ne sont pas installés.

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.** (29)


</dt> <dd>

L’appareil est désactivé. Le microprogramme de l’appareil n’a pas fourni les ressources requises.

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.** (30)


</dt> <dd>

L’appareil utilise une ressource IRQ qu’un autre appareil utilise.

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.** 31


</dt> <dd>

L’appareil ne fonctionne pas correctement. Windows ne peut pas charger les pilotes de périphérique requis.

</dd> </dl>

</dd> <dt>

**ConfigManagerUserConfig**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")
</dt> </dl>

Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.

Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Nom de la classe ou de la sous-classe utilisée dans la création d’une instance. Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.

Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

</dd> <dt>

**CurrentClockSpeed**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Processeur DMTF \| 006,6 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" mégahertz ")
</dt> </dl>

Vitesse actuelle (en mégahertz) du processeur.

</dd> <dt>

**DataWidth**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« bits »)
</dt> </dl>

Largeur des données du processeur, en bits.

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")
</dt> </dl>

Description textuelle de l’objet.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**DeviceID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Adresse ou d’autres informations d’identification pour nommer de manière unique l’unité logique.

Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

</dd> <dt>

**ErrorCleared**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Si la **valeur est true**, l’erreur signalée dans la propriété **LastErrorCode** est maintenant désactivée.

Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chaîne de forme libre qui fournit des informations sur l’erreur enregistrée dans la propriété **LastErrorCode** et les actions correctives à effectuer.

Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

</dd> <dt>

**Famille**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Processeur DMTF \| 014,3 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ processeur CIM**.**OtherFamilyDescription**")
</dt> </dl>

Type de la famille de processeurs.

Cette propriété est héritée **du \_ processeur CIM**.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)


</dt> <dd></dd> <dt>

<span id="8086"></span>

<span id="8086"></span>**8086** (3)


</dt> <dd></dd> <dt>

<span id="80286"></span>

<span id="80286"></span>**80286** (4)


</dt> <dd></dd> <dt>

<span id="80386"></span>

<span id="80386"></span>**80386** (5)


</dt> <dd></dd> <dt>

<span id="80486"></span>

<span id="80486"></span>**80486** (6)


</dt> <dd></dd> <dt>

<span id="8087"></span>

<span id="8087"></span>**8087** (7)


</dt> <dd></dd> <dt>

<span id="80287"></span>

<span id="80287"></span>**80287** (8)


</dt> <dd></dd> <dt>

<span id="80387"></span>

<span id="80387"></span>**80387** (9)


</dt> <dd></dd> <dt>

<span id="80487"></span>

<span id="80487"></span>**80487** (10)


</dt> <dd></dd> <dt>

<span id="Pentium_R__brand"></span><span id="pentium_r__brand"></span><span id="PENTIUM_R__BRAND"></span>

<span id="Pentium_R__brand"></span><span id="pentium_r__brand"></span><span id="PENTIUM_R__BRAND"></span>**Pentium (R)** (11)


</dt> <dd>

La personnalisation de la Pentium

</dd> <dt>

<span id="Pentium_R__Pro"></span><span id="pentium_r__pro"></span><span id="PENTIUM_R__PRO"></span>

<span id="Pentium_R__Pro"></span><span id="pentium_r__pro"></span><span id="PENTIUM_R__PRO"></span>**Pentium (R) Pro** (12)


</dt> <dd>

Pentium Pro

</dd> <dt>

<span id="Pentium_R__II"></span><span id="pentium_r__ii"></span><span id="PENTIUM_R__II"></span>

<span id="Pentium_R__II"></span><span id="pentium_r__ii"></span><span id="PENTIUM_R__II"></span>**Pentium (R) II** (13)


</dt> <dd>

Pentium II

</dd> <dt>

<span id="Pentium_R__processor_with_MMX_TM__technology"></span><span id="pentium_r__processor_with_mmx_tm__technology"></span><span id="PENTIUM_R__PROCESSOR_WITH_MMX_TM__TECHNOLOGY"></span>

<span id="Pentium_R__processor_with_MMX_TM__technology"></span><span id="pentium_r__processor_with_mmx_tm__technology"></span><span id="PENTIUM_R__PROCESSOR_WITH_MMX_TM__TECHNOLOGY"></span>**Processeur Pentium (R) avec technologie MMX (TM)** (14)


</dt> <dd>

Processeur Pentium avec technologie MMX

</dd> <dt>

<span id="Celeron_TM_"></span><span id="celeron_tm_"></span><span id="CELERON_TM_"></span>

<span id="Celeron_TM_"></span><span id="celeron_tm_"></span><span id="CELERON_TM_"></span>**Celeron (TM)** (15)


</dt> <dd>

Celeron

</dd> <dt>

<span id="Pentium_R__II_Xeon_TM_"></span><span id="pentium_r__ii_xeon_tm_"></span><span id="PENTIUM_R__II_XEON_TM_"></span>

<span id="Pentium_R__II_Xeon_TM_"></span><span id="pentium_r_:xeon_tm_"></span><span id="PENTIUM_R__II_XEON_TM_"></span>**Pentium (R) II Xeon (TM)** (16)


</dt> <dd>

Pentium II Xeon

</dd> <dt>

<span id="Pentium_R__III"></span><span id="pentium_r__iii"></span><span id="PENTIUM_R__III"></span>

<span id="Pentium_R__III"></span><span id="pentium_r__iii"></span><span id="PENTIUM_R__III"></span>**Pentium (R) III** (17)


</dt> <dd>

Pentium III

</dd> <dt>

<span id="M1_Family"></span><span id="m1_family"></span><span id="M1_FAMILY"></span>

<span id="M1_Family"></span><span id="m1_family"></span><span id="M1_FAMILY"></span>**Famille M1** (18)


</dt> <dd></dd> <dt>

<span id="M2_Family"></span><span id="m2_family"></span><span id="M2_FAMILY"></span>

<span id="M2_Family"></span><span id="m2_family"></span><span id="M2_FAMILY"></span>**Famille m2** (19)


</dt> <dd></dd> <dt>

<span id="K5_Family"></span><span id="k5_family"></span><span id="K5_FAMILY"></span>

<span id="K5_Family"></span><span id="k5_family"></span><span id="K5_FAMILY"></span>**Famille K5** (24)


</dt> <dd>

Famille de processeurs AMD Duron

</dd> <dt>

<span id="K6_Family"></span><span id="k6_family"></span><span id="K6_FAMILY"></span>

<span id="K6_Family"></span><span id="k6_family"></span><span id="K6_FAMILY"></span>**Famille K6** (25)


</dt> <dd>

Famille K5

</dd> <dt>

<span id="K6-2"></span><span id="k6-2"></span>

<span id="K6-2"></span><span id="k6-2"></span>**K6-2** (26)


</dt> <dd></dd> <dt>

<span id="K6-3"></span><span id="k6-3"></span>

<span id="K6-3"></span><span id="k6-3"></span>**K6-3** (27)


</dt> <dd></dd> <dt>

<span id="AMD_Athlon_TM__Processor_Family"></span><span id="amd_athlon_tm__processor_family"></span><span id="AMD_ATHLON_TM__PROCESSOR_FAMILY"></span>

<span id="AMD_Athlon_TM__Processor_Family"></span><span id="amd_athlon_tm__processor_family"></span><span id="AMD_ATHLON_TM__PROCESSOR_FAMILY"></span>**Famille de processeurs AMD Athlon (TM)** (28)


</dt> <dd>

Famille de processeurs AMD Athlon

</dd> <dt>

<span id="AMD_R__Duron_TM__Processor"></span><span id="amd_r__duron_tm__processor"></span><span id="AMD_R__DURON_TM__PROCESSOR"></span>

<span id="AMD_R__Duron_TM__Processor"></span><span id="amd_r__duron_tm__processor"></span><span id="AMD_R__DURON_TM__PROCESSOR"></span>**Processeur AMD (R) Duron (TM)** (29)


</dt> <dd>

Processeur AMD Duron

</dd> <dt>

<span id="AMD29000_Family"></span><span id="amd29000_family"></span><span id="AMD29000_FAMILY"></span>

<span id="AMD29000_Family"></span><span id="amd29000_family"></span><span id="AMD29000_FAMILY"></span>**Famille AMD29000** (30)


</dt> <dd>

Famille AMD2900

</dd> <dt>

<span id="K6-2_"></span><span id="k6-2_"></span>

<span id="K6-2_"></span><span id="k6-2_"></span>**K6-2 +** (31)


</dt> <dd></dd> <dt>

<span id="Power_PC_Family"></span><span id="power_pc_family"></span><span id="POWER_PC_FAMILY"></span>

<span id="Power_PC_Family"></span><span id="power_pc_family"></span><span id="POWER_PC_FAMILY"></span>**Famille Power PC** (32)


</dt> <dd></dd> <dt>

<span id="Power_PC_601"></span><span id="power_pc_601"></span><span id="POWER_PC_601"></span>

<span id="Power_PC_601"></span><span id="power_pc_601"></span><span id="POWER_PC_601"></span>**Power PC 601** (33)


</dt> <dd></dd> <dt>

<span id="Power_PC_603"></span><span id="power_pc_603"></span><span id="POWER_PC_603"></span>

<span id="Power_PC_603"></span><span id="power_pc_603"></span><span id="POWER_PC_603"></span>**Power PC 603** (34)


</dt> <dd></dd> <dt>

<span id="Power_PC_603_"></span><span id="power_pc_603_"></span><span id="POWER_PC_603_"></span>

<span id="Power_PC_603_"></span><span id="power_pc_603_"></span><span id="POWER_PC_603_"></span>**Power PC 603 +** (35)


</dt> <dd></dd> <dt>

<span id="Power_PC_604"></span><span id="power_pc_604"></span><span id="POWER_PC_604"></span>

<span id="Power_PC_604"></span><span id="power_pc_604"></span><span id="POWER_PC_604"></span>**Power PC 604** (36)


</dt> <dd></dd> <dt>

<span id="Power_PC_620"></span><span id="power_pc_620"></span><span id="POWER_PC_620"></span>

<span id="Power_PC_620"></span><span id="power_pc_620"></span><span id="POWER_PC_620"></span>**Power PC 620** (37)


</dt> <dd></dd> <dt>

<span id="Power_PC_X704"></span><span id="power_pc_x704"></span><span id="POWER_PC_X704"></span>

<span id="Power_PC_X704"></span><span id="power_pc_x704"></span><span id="POWER_PC_X704"></span>**Power PC X704** (38)


</dt> <dd></dd> <dt>

<span id="Power_PC_750"></span><span id="power_pc_750"></span><span id="POWER_PC_750"></span>

<span id="Power_PC_750"></span><span id="power_pc_750"></span><span id="POWER_PC_750"></span>**Power PC 750** (39)


</dt> <dd></dd> <dt>

<span id="Alpha_Family"></span><span id="alpha_family"></span><span id="ALPHA_FAMILY"></span>

<span id="Alpha_Family"></span><span id="alpha_family"></span><span id="ALPHA_FAMILY"></span>**Famille alpha** (48)


</dt> <dd></dd> <dt>

<span id="Alpha_21064"></span><span id="alpha_21064"></span><span id="ALPHA_21064"></span>

<span id="Alpha_21064"></span><span id="alpha_21064"></span><span id="ALPHA_21064"></span>**Alpha 21064** (49)


</dt> <dd></dd> <dt>

<span id="Alpha_21066"></span><span id="alpha_21066"></span><span id="ALPHA_21066"></span>

<span id="Alpha_21066"></span><span id="alpha_21066"></span><span id="ALPHA_21066"></span>**Alpha 21066** (50)


</dt> <dd></dd> <dt>

<span id="Alpha_21164"></span><span id="alpha_21164"></span><span id="ALPHA_21164"></span>

<span id="Alpha_21164"></span><span id="alpha_21164"></span><span id="ALPHA_21164"></span>**Alpha 21164** (51)


</dt> <dd></dd> <dt>

<span id="Alpha_21164PC"></span><span id="alpha_21164pc"></span><span id="ALPHA_21164PC"></span>

<span id="Alpha_21164PC"></span><span id="alpha_21164pc"></span><span id="ALPHA_21164PC"></span>**Alpha 21164PC** (52)


</dt> <dd></dd> <dt>

<span id="Alpha_21164a"></span><span id="alpha_21164a"></span><span id="ALPHA_21164A"></span>

<span id="Alpha_21164a"></span><span id="alpha_21164a"></span><span id="ALPHA_21164A"></span>**Alpha 21164a** (53)


</dt> <dd></dd> <dt>

<span id="Alpha_21264"></span><span id="alpha_21264"></span><span id="ALPHA_21264"></span>

<span id="Alpha_21264"></span><span id="alpha_21264"></span><span id="ALPHA_21264"></span>**Alpha 21264** (54)


</dt> <dd></dd> <dt>

<span id="Alpha_21364"></span><span id="alpha_21364"></span><span id="ALPHA_21364"></span>

<span id="Alpha_21364"></span><span id="alpha_21364"></span><span id="ALPHA_21364"></span>**Alpha 21364** (55)


</dt> <dd></dd> <dt>

<span id="MIPS_Family"></span><span id="mips_family"></span><span id="MIPS_FAMILY"></span>

<span id="MIPS_Family"></span><span id="mips_family"></span><span id="MIPS_FAMILY"></span>**Famille mips** (64)


</dt> <dd></dd> <dt>

<span id="MIPS_R4000"></span><span id="mips_r4000"></span>

<span id="MIPS_R4000"></span><span id="mips_r4000"></span>**R4000 mips** (65)


</dt> <dd></dd> <dt>

<span id="MIPS_R4200"></span><span id="mips_r4200"></span>

<span id="MIPS_R4200"></span><span id="mips_r4200"></span>**R4200 mips** (66)


</dt> <dd></dd> <dt>

<span id="MIPS_R4400"></span><span id="mips_r4400"></span>

<span id="MIPS_R4400"></span><span id="mips_r4400"></span>**R4400 mips** (67)


</dt> <dd></dd> <dt>

<span id="MIPS_R4600"></span><span id="mips_r4600"></span>

<span id="MIPS_R4600"></span><span id="mips_r4600"></span>**R4600 mips** (68)


</dt> <dd></dd> <dt>

<span id="MIPS_R10000"></span><span id="mips_r10000"></span>

<span id="MIPS_R10000"></span><span id="mips_r10000"></span>**R10000 mips** (69)


</dt> <dd></dd> <dt>

<span id="SPARC_Family"></span><span id="sparc_family"></span><span id="SPARC_FAMILY"></span>

<span id="SPARC_Family"></span><span id="sparc_family"></span><span id="SPARC_FAMILY"></span>**Famille sparc** (80)


</dt> <dd></dd> <dt>

<span id="SuperSPARC"></span><span id="supersparc"></span><span id="SUPERSPARC"></span>

<span id="SuperSPARC"></span><span id="supersparc"></span><span id="SUPERSPARC"></span>**SuperSPARC** (81)


</dt> <dd></dd> <dt>

<span id="microSPARC_II"></span><span id="microsparc_ii"></span><span id="MICROSPARC_II"></span>

<span id="microSPARC_II"></span><span id="microsparc_ii"></span><span id="MICROSPARC_II"></span>**MICROSPARC II** (82)


</dt> <dd></dd> <dt>

<span id="microSPARC_IIep"></span><span id="microsparc_iiep"></span><span id="MICROSPARC_IIEP"></span>

<span id="microSPARC_IIep"></span><span id="microsparc_iiep"></span><span id="MICROSPARC_IIEP"></span>**MicroSPARC IIep** (83)


</dt> <dd></dd> <dt>

<span id="UltraSPARC"></span><span id="ultrasparc"></span><span id="ULTRASPARC"></span>

<span id="UltraSPARC"></span><span id="ultrasparc"></span><span id="ULTRASPARC"></span>**UltraSPARC** (84)


</dt> <dd></dd> <dt>

<span id="UltraSPARC_II"></span><span id="ultrasparc_ii"></span><span id="ULTRASPARC_II"></span>

<span id="UltraSPARC_II"></span><span id="ultrasparc_ii"></span><span id="ULTRASPARC_II"></span>**ULTRASPARC II** (85)


</dt> <dd></dd> <dt>

<span id="UltraSPARC_IIi"></span><span id="ultrasparc_iii"></span><span id="ULTRASPARC_III"></span>

<span id="UltraSPARC_IIi"></span><span id="ultrasparc_iii"></span><span id="ULTRASPARC_III"></span>**UltraSPARC III** (86)


</dt> <dd></dd> <dt>

<span id="UltraSPARC_III"></span><span id="ultrasparc_iii"></span><span id="ULTRASPARC_III"></span>

<span id="UltraSPARC_III"></span><span id="ultrasparc_iii"></span><span id="ULTRASPARC_III"></span>**ULTRASPARC III** (87)


</dt> <dd></dd> <dt>

<span id="UltraSPARC_IIIi"></span><span id="ultrasparc_iiii"></span><span id="ULTRASPARC_IIII"></span>

<span id="UltraSPARC_IIIi"></span><span id="ultrasparc_iiii"></span><span id="ULTRASPARC_IIII"></span>**UltraSPARC IIIi** (88)


</dt> <dd></dd> <dt>

<span id="68040"></span>

<span id="68040"></span>**68040** (96)


</dt> <dd></dd> <dt>

<span id="68xxx_Family"></span><span id="68xxx_family"></span><span id="68XXX_FAMILY"></span>

<span id="68xxx_Family"></span><span id="68xxx_family"></span><span id="68XXX_FAMILY"></span>**famille 68xxx** (97)


</dt> <dd></dd> <dt>

<span id="68000"></span>

<span id="68000"></span>**68000** (98)


</dt> <dd></dd> <dt>

<span id="68010"></span>

<span id="68010"></span>**68010** (99)


</dt> <dd></dd> <dt>

<span id="68020"></span>

<span id="68020"></span>**68020** (100)


</dt> <dd></dd> <dt>

<span id="68030"></span>

<span id="68030"></span>**68030** (101)


</dt> <dd></dd> <dt>

<span id="Hobbit_Family"></span><span id="hobbit_family"></span><span id="HOBBIT_FAMILY"></span>

<span id="Hobbit_Family"></span><span id="hobbit_family"></span><span id="HOBBIT_FAMILY"></span>**Famille Hobbit** (112)


</dt> <dd></dd> <dt>

<span id="Crusoe_TM__TM5000_Family"></span><span id="crusoe_tm__tm5000_family"></span><span id="CRUSOE_TM__TM5000_FAMILY"></span>

<span id="Crusoe_TM__TM5000_Family"></span><span id="crusoe_tm__tm5000_family"></span><span id="CRUSOE_TM__TM5000_FAMILY"></span>**Famille Crusoe (TM) TM5000** (120)


</dt> <dd>

Famille Crusoe TM5000

</dd> <dt>

<span id="Crusoe_TM__TM3000_Family"></span><span id="crusoe_tm__tm3000_family"></span><span id="CRUSOE_TM__TM3000_FAMILY"></span>

<span id="Crusoe_TM__TM3000_Family"></span><span id="crusoe_tm__tm3000_family"></span><span id="CRUSOE_TM__TM3000_FAMILY"></span>**Famille Crusoe (TM) TM3000** (121)


</dt> <dd>

Famille Crusoe TM3000

</dd> <dt>

<span id="Efficeon_TM__TM8000_Family"></span><span id="efficeon_tm__tm8000_family"></span><span id="EFFICEON_TM__TM8000_FAMILY"></span>

<span id="Efficeon_TM__TM8000_Family"></span><span id="efficeon_tm__tm8000_family"></span><span id="EFFICEON_TM__TM8000_FAMILY"></span>**Famille Efficeon (TM) TM8000** (122)


</dt> <dd>

Famille Efficeon8000

</dd> <dt>

<span id="Weitek"></span><span id="weitek"></span><span id="WEITEK"></span>

<span id="Weitek"></span><span id="weitek"></span><span id="WEITEK"></span>**Weitek** (128)


</dt> <dd></dd> <dt>

<span id="Itanium_TM__Processor"></span><span id="itanium_tm__processor"></span><span id="ITANIUM_TM__PROCESSOR"></span>

<span id="Itanium_TM__Processor"></span><span id="itanium_tm__processor"></span><span id="ITANIUM_TM__PROCESSOR"></span>**Processeur Itanium (** 130)


</dt> <dd>

Processeur Itanium

</dd> <dt>

<span id="AMD_Athlon_TM__64_Processor_Family"></span><span id="amd_athlon_tm__64_processor_family"></span><span id="AMD_ATHLON_TM__64_PROCESSOR_FAMILY"></span>

<span id="AMD_Athlon_TM__64_Processor_Family"></span><span id="amd_athlon_tm__64_processor_family"></span><span id="AMD_ATHLON_TM__64_PROCESSOR_FAMILY"></span>**Famille de processeurs AMD Athlon (TM) 64** (131)


</dt> <dd>

AMD Athlon 

</dd> <dt>

<span id="AMD_Opteron_TM__Family"></span><span id="amd_opteron_tm__family"></span><span id="AMD_OPTERON_TM__FAMILY"></span>

<span id="AMD_Opteron_TM__Family"></span><span id="amd_opteron_tm__family"></span><span id="AMD_OPTERON_TM__FAMILY"></span>**Famille AMD Opteron (TM)** (132)


</dt> <dd>

Famille AMD Opteron

</dd> <dt>

<span id="PA-RISC_Family"></span><span id="pa-risc_family"></span><span id="PA-RISC_FAMILY"></span>

<span id="PA-RISC_Family"></span><span id="pa-risc_family"></span><span id="PA-RISC_FAMILY"></span>**Famille PA-RISC** (144)


</dt> <dd></dd> <dt>

<span id="PA-RISC_8500"></span><span id="pa-risc_8500"></span>

<span id="PA-RISC_8500"></span><span id="pa-risc_8500"></span>**PA-RISC 8500** (145)


</dt> <dd></dd> <dt>

<span id="PA-RISC_8000"></span><span id="pa-risc_8000"></span>

<span id="PA-RISC_8000"></span><span id="pa-risc_8000"></span>**PA-RISC 8000** (146)


</dt> <dd></dd> <dt>

<span id="PA-RISC_7300LC"></span><span id="pa-risc_7300lc"></span>

<span id="PA-RISC_7300LC"></span><span id="pa-risc_7300lc"></span>**PA-RISC 7300LC** (147)


</dt> <dd></dd> <dt>

<span id="PA-RISC_7200"></span><span id="pa-risc_7200"></span>

<span id="PA-RISC_7200"></span><span id="pa-risc_7200"></span>**PA-RISC 7200** (148)


</dt> <dd></dd> <dt>

<span id="PA-RISC_7100LC"></span><span id="pa-risc_7100lc"></span>

<span id="PA-RISC_7100LC"></span><span id="pa-risc_7100lc"></span>**PA-RISC 7100LC** (149)


</dt> <dd></dd> <dt>

<span id="PA-RISC_7100"></span><span id="pa-risc_7100"></span>

<span id="PA-RISC_7100"></span><span id="pa-risc_7100"></span>**PA-RISC 7100** (150)


</dt> <dd></dd> <dt>

<span id="V30_Family"></span><span id="v30_family"></span><span id="V30_FAMILY"></span>

<span id="V30_Family"></span><span id="v30_family"></span><span id="V30_FAMILY"></span>**Famille V30** (160)


</dt> <dd></dd> <dt>

<span id="Pentium_R__III_Xeon_TM_"></span><span id="pentium_r__iii_xeon_tm_"></span><span id="PENTIUM_R__III_XEON_TM_"></span>

<span id="Pentium_R__III_Xeon_TM_"></span><span id="pentium_r__iii_xeon_tm_"></span><span id="PENTIUM_R__III_XEON_TM_"></span>**Pentium (R) III Xeon (TM)** (176)


</dt> <dd>

Pentium III Xeon

</dd> <dt>

<span id="Pentium_R__III_Processor_with_Intel_R__SpeedStep_TM__Technology"></span><span id="pentium_r__iii_processor_with_intel_r__speedstep_tm__technology"></span><span id="PENTIUM_R__III_PROCESSOR_WITH_INTEL_R__SPEEDSTEP_TM__TECHNOLOGY"></span>

<span id="Pentium_R__III_Processor_with_Intel_R__SpeedStep_TM__Technology"></span><span id="pentium_r__iii_processor_with_intel_r__speedstep_tm__technology"></span><span id="PENTIUM_R__III_PROCESSOR_WITH_INTEL_R__SPEEDSTEP_TM__TECHNOLOGY"></span>**Processeur Pentium (r) III avec technologie Intel (r) SpeedStep (TM)** (177)


</dt> <dd>

Processeur Pentium III avec technologie Intel SpeedStep

</dd> <dt>

<span id="Pentium_R__4"></span><span id="pentium_r__4"></span><span id="PENTIUM_R__4"></span>

<span id="Pentium_R__4"></span><span id="pentium_r__4"></span><span id="PENTIUM_R__4"></span>**Pentium (R) 4** (178)


</dt> <dd>

Pentium 4

</dd> <dt>

<span id="Intel_R__Xeon_TM_"></span><span id="intel_r__xeon_tm_"></span><span id="INTEL_R__XEON_TM_"></span>

<span id="Intel_R__Xeon_TM_"></span><span id="intel_r__xeon_tm_"></span><span id="INTEL_R__XEON_TM_"></span>**Intel (R) Xeon (TM)** (179)


</dt> <dd>

Processeur Intel Xeon

</dd> <dt>

<span id="AS400_Family"></span><span id="as400_family"></span><span id="AS400_FAMILY"></span>

<span id="AS400_Family"></span><span id="as400_family"></span><span id="AS400_FAMILY"></span>**Famille AS400** (180)


</dt> <dd></dd> <dt>

<span id="Intel_R__Xeon_TM__processor_MP"></span><span id="intel_r__xeon_tm__processor_mp"></span><span id="INTEL_R__XEON_TM__PROCESSOR_MP"></span>

<span id="Intel_R__Xeon_TM__processor_MP"></span><span id="intel_r__xeon_tm__processor_mp"></span><span id="INTEL_R__XEON_TM__PROCESSOR_MP"></span>**Processeur Intel (R) Xeon (TM) MP** (181)


</dt> <dd>

Processeur Intel Xeon MP

</dd> <dt>

<span id="AMD_AthlonXP_TM__Family"></span><span id="amd_athlonxp_tm__family"></span><span id="AMD_ATHLONXP_TM__FAMILY"></span>

<span id="AMD_AthlonXP_TM__Family"></span><span id="amd_athlonxp_tm__family"></span><span id="AMD_ATHLONXP_TM__FAMILY"></span>**Famille AMD AthlonXP (TM)** (182)


</dt> <dd>

Famille AMD AthlonXP

</dd> <dt>

<span id="AMD_AthlonMP_TM__Family"></span><span id="amd_athlonmp_tm__family"></span><span id="AMD_ATHLONMP_TM__FAMILY"></span>

<span id="AMD_AthlonMP_TM__Family"></span><span id="amd_athlonmp_tm__family"></span><span id="AMD_ATHLONMP_TM__FAMILY"></span>**Famille AMD AthlonMP (TM)** (183)


</dt> <dd>

Famille AMD AthlonMP

</dd> <dt>

<span id="Intel_R__Itanium_R__2"></span><span id="intel_r__itanium_r__2"></span><span id="INTEL_R__ITANIUM_R__2"></span>

<span id="Intel_R__Itanium_R__2"></span><span id="intel_r__itanium_r__2"></span><span id="INTEL_R__ITANIUM_R__2"></span>**Intel (r) Itanium (r) 2** (184)


</dt> <dd>

Intel Itanium 2

</dd> <dt>

<span id="Intel_Pentium_M_Processor"></span><span id="intel_pentium_m_processor"></span><span id="INTEL_PENTIUM_M_PROCESSOR"></span>

<span id="Intel_Pentium_M_Processor"></span><span id="intel_pentium_m_processor"></span><span id="INTEL_PENTIUM_M_PROCESSOR"></span>**Processeur Intel Pentium M** (185)


</dt> <dd></dd> <dt>

<span id="K7"></span><span id="k7"></span>

<span id="K7"></span><span id="k7"></span>**K7** (190)


</dt> <dd></dd> <dt>

<span id="IBM390_Family"></span><span id="ibm390_family"></span><span id="IBM390_FAMILY"></span>

<span id="IBM390_Family"></span><span id="ibm390_family"></span><span id="IBM390_FAMILY"></span>**Famille IBM390** (200)


</dt> <dd></dd> <dt>

<span id="G4"></span><span id="g4"></span>

<span id="G4"></span><span id="g4"></span>**G4** (201)


</dt> <dd></dd> <dt>

<span id="G5"></span><span id="g5"></span>

<span id="G5"></span><span id="g5"></span>**G5** (202)


</dt> <dd></dd> <dt>

<span id="G6"></span><span id="g6"></span>

<span id="G6"></span><span id="g6"></span>**G6** (203)


</dt> <dd></dd> <dt>

<span id="z_Architecture_base"></span><span id="z_architecture_base"></span><span id="Z_ARCHITECTURE_BASE"></span>

<span id="z_Architecture_base"></span><span id="z_architecture_base"></span><span id="Z_ARCHITECTURE_BASE"></span>**base z/architecture** (204)


</dt> <dd></dd> <dt>

<span id="i860"></span><span id="I860"></span>

<span id="i860"></span><span id="I860"></span>**i860** (250)


</dt> <dd></dd> <dt>

<span id="i960"></span><span id="I960"></span>

<span id="i960"></span><span id="I960"></span>**i960** (251)


</dt> <dd></dd> <dt>

<span id="SH-3"></span><span id="sh-3"></span>

<span id="SH-3"></span><span id="sh-3"></span>**SH-3** (260)


</dt> <dd></dd> <dt>

<span id="SH-4"></span><span id="sh-4"></span>

<span id="SH-4"></span><span id="sh-4"></span>**SH-4** (261)


</dt> <dd></dd> <dt>

<span id="ARM"></span><span id="arm"></span>

<span id="ARM"></span><span id="arm"></span>**ARM** (280)


</dt> <dd></dd> <dt>

<span id="StrongARM"></span><span id="strongarm"></span><span id="STRONGARM"></span>

<span id="StrongARM"></span><span id="strongarm"></span><span id="STRONGARM"></span>**StrongARM** (281)


</dt> <dd></dd> <dt>

<span id="6x86"></span><span id="6X86"></span>

<span id="6x86"></span><span id="6X86"></span>**6 x86** (300)


</dt> <dd></dd> <dt>

<span id="MediaGX"></span><span id="mediagx"></span><span id="MEDIAGX"></span>

<span id="MediaGX"></span><span id="mediagx"></span><span id="MEDIAGX"></span>**MediaGX** (301)


</dt> <dd></dd> <dt>

<span id="MII"></span><span id="mii"></span>

<span id="MII"></span><span id="mii"></span>**MII** (302)


</dt> <dd></dd> <dt>

<span id="WinChip"></span><span id="winchip"></span><span id="WINCHIP"></span>

<span id="WinChip"></span><span id="winchip"></span><span id="WINCHIP"></span>**WinChip** (320)


</dt> <dd></dd> <dt>

<span id="DSP"></span><span id="dsp"></span>

<span id="DSP"></span><span id="dsp"></span>**DSP** (350)


</dt> <dd></dd> <dt>

<span id="Video_Processor"></span><span id="video_processor"></span><span id="VIDEO_PROCESSOR"></span>

<span id="Video_Processor"></span><span id="video_processor"></span><span id="VIDEO_PROCESSOR"></span>**Processeur vidéo** (500)


</dt> <dd></dd> </dl>

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")
</dt> </dl>

Date et heure d’installation de l’objet. Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**LastErrorCode**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Dernier code d’erreur signalé par l’unité logique.

Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

</dd> <dt>

**LoadPercentage**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. hrProcessorLoad "), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (" percent ")
</dt> </dl>

Chargement du processeur, en moyenne au cours de la dernière minute, en pourcentage.

</dd> <dt>

**MaxClockSpeed**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Processeur DMTF \| 006,5 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" mégahertz ")
</dt> </dl>

Vitesse maximale (en mégahertz) du processeur.

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")
</dt> </dl>

Étiquette par laquelle l’objet est connu. Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**OtherFamilyDescription**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ processeur CIM**.**Family**»)
</dt> </dl>

Description du type de la famille de processeurs. Cette propriété est utilisée lorsque la propriété **Family** a la valeur 1 (« other »). Cette chaîne doit être définie sur Null lorsque la propriété **Family** est une valeur autre que 1.

</dd> <dt>

**PNPDeviceID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")
</dt> </dl>

Identificateur d’appareil Plug-and-Play de l’unité logique. Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

Exemple : « \* PNP030b »

</dd> <dt>

**PowerManagementCapabilities**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Tableau des fonctionnalités d’alimentation spécifiques d’un périphérique logique.

Cette propriété est héritée de **CIM \_ LogicalDevice**.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)


</dt> <dd>

Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)


</dt> <dd>

L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)


</dt> <dd>

La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) est prise en charge. Cette méthode se trouve sur la classe parente du **\_ LogicalDevice CIM** et peut être implémentée. Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)


</dt> <dd>

La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation).

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)


</dt> <dd>

La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation) et l' *heure* définie sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.

</dd> </dl>

</dd> <dt>

**PowerManagementSupported**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation, c’est-à-dire être mis en état d’économie d’énergie. Si la valeur est **false**, la valeur entière 1 (« non pris en charge ») doit être la seule entrée dans le tableau **PowerManagementCapabilities** .

Cette propriété n’indique pas si les fonctionnalités de gestion de l’alimentation sont actuellement activées, ou si elles sont activées, quelles sont les fonctionnalités prises en charge. Pour plus d’informations, consultez le tableau **PowerManagementCapabilities** . Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

</dd> <dt>

**Rôle**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chaîne de forme libre qui décrit le rôle du processeur. Par exemple, « processeur central » ou « processeur mathématique ».

</dd> <dt>

**État**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")
</dt> </dl>

État actuel de l’objet.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

Les valeurs sont notamment les suivantes :

<dt>

<span id="OK"></span><span id="ok"></span>

**OK** (« OK »)


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Erreur** (« erreur »)


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Détérioré** (« détérioré »)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Inconnu** ("inconnu")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Échec** prévu (« échec prédit »)


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Démarrage** en cours (« démarrage »)


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Arrêt** en cours (« arrêt »)


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Service** (« service »)


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Stressed** (« stressed »)


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

Non **récupéré** (« non récupéré »)


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Aucun contact** (« aucun contact »)


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Communication perdue** (« inversée comm »)


</dt> <dd></dd> </dl>

</dd> <dt>

**StatusInfo**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,3 ")
</dt> </dl>

État de l’unité logique. Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (non applicable) doit être utilisée.

Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Autre** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Inconnu** (2)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Activé** (3)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Désactivé** (4)


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**Non applicable** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**Exécution pas à pas**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) («**\_ processeur CIM**».**Family**»)
</dt> </dl>

Chaîne de forme libre qui indique le niveau de révision du processeur au sein de la famille de processeurs.

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Nom de la classe de création du système d’étendue.

Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Nom du système d’étendue.

Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

</dd> <dt>

**UniqueId**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Identificateur global unique du processeur. Cet identificateur peut uniquement être unique au sein d’une famille de processeurs.

</dd> <dt>

**UpgradeMethod**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Processeur DMTF \| 006,7 ")
</dt> </dl>

Les informations de socket de processeur, qui incluent des données sur la mise à niveau du processeur (si les mises à niveau sont prises en charge).

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)


</dt> <dd></dd> <dt>

<span id="Daughter_Board"></span><span id="daughter_board"></span><span id="DAUGHTER_BOARD"></span>

<span id="Daughter_Board"></span><span id="daughter_board"></span><span id="DAUGHTER_BOARD"></span>**Carte fille** (3)


</dt> <dd></dd> <dt>

<span id="ZIF_Socket"></span><span id="zif_socket"></span><span id="ZIF_SOCKET"></span>

<span id="ZIF_Socket"></span><span id="zif_socket"></span><span id="ZIF_SOCKET"></span>**Connecteur ZIF** (4)


</dt> <dd></dd> <dt>

<span id="Replacement_Piggy_Back"></span><span id="replacement_piggy_back"></span><span id="REPLACEMENT_PIGGY_BACK"></span>

<span id="Replacement_Piggy_Back"></span><span id="replacement_piggy_back"></span><span id="REPLACEMENT_PIGGY_BACK"></span>**Remplacement/** superposition (5)


</dt> <dd>

Remplacement ou remontée

</dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span id="None"></span><span id="none"></span><span id="NONE"></span>**Aucun** (6)


</dt> <dd></dd> <dt>

<span id="LIF_Socket"></span><span id="lif_socket"></span><span id="LIF_SOCKET"></span>

<span id="LIF_Socket"></span><span id="lif_socket"></span><span id="LIF_SOCKET"></span>**Socket LIF** (7)


</dt> <dd></dd> <dt>

<span id="Slot_1"></span><span id="slot_1"></span><span id="SLOT_1"></span>

<span id="Slot_1"></span><span id="slot_1"></span><span id="SLOT_1"></span>**Emplacement 1** (8)


</dt> <dd></dd> <dt>

<span id="Slot_2"></span><span id="slot_2"></span><span id="SLOT_2"></span>

<span id="Slot_2"></span><span id="slot_2"></span><span id="SLOT_2"></span>**Emplacement 2** (9)


</dt> <dd></dd> <dt>

<span id="370_Pin_Socket"></span><span id="370_pin_socket"></span><span id="370_PIN_SOCKET"></span>

<span id="370_Pin_Socket"></span><span id="370_pin_socket"></span><span id="370_PIN_SOCKET"></span>**Socket de broche 370** (10)


</dt> <dd></dd> <dt>

<span id="Slot_A"></span><span id="slot_a"></span><span id="SLOT_A"></span>

<span id="Slot_A"></span><span id="slot_a"></span><span id="SLOT_A"></span>**Emplacement A** (11)


</dt> <dd></dd> <dt>

<span id="Slot_M"></span><span id="slot_m"></span><span id="SLOT_M"></span>

<span id="Slot_M"></span><span id="slot_m"></span><span id="SLOT_M"></span>**Emplacement M** (12)


</dt> <dd></dd> <dt>

<span id="Socket_423"></span><span id="socket_423"></span><span id="SOCKET_423"></span>

<span id="Socket_423"></span><span id="socket_423"></span><span id="SOCKET_423"></span>**Socket 423** (13)


</dt> <dd></dd> <dt>

<span id="Socket_A__Socket_462_"></span><span id="socket_a__socket_462_"></span><span id="SOCKET_A__SOCKET_462_"></span>

<span id="Socket_A__Socket_462_"></span><span id="socket_a__socket_462_"></span><span id="SOCKET_A__SOCKET_462_"></span>**Socket A (socket 462)** (14)


</dt> <dd></dd> <dt>

<span id="Socket_478"></span><span id="socket_478"></span><span id="SOCKET_478"></span>

<span id="Socket_478"></span><span id="socket_478"></span><span id="SOCKET_478"></span>**Socket 478** (15)


</dt> <dd></dd> <dt>

<span id="Socket_754"></span><span id="socket_754"></span><span id="SOCKET_754"></span>

<span id="Socket_754"></span><span id="socket_754"></span><span id="SOCKET_754"></span>**Socket 754** (16)


</dt> <dd></dd> <dt>

<span id="Socket_940"></span><span id="socket_940"></span><span id="SOCKET_940"></span>

<span id="Socket_940"></span><span id="socket_940"></span><span id="SOCKET_940"></span>**Socket 940** (17)


</dt> <dd></dd> <dt>

<span id="Socket_939"></span><span id="socket_939"></span><span id="SOCKET_939"></span>

<span id="Socket_939"></span><span id="socket_939"></span><span id="SOCKET_939"></span>**Socket 939** (18)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Notes

La classe de **\_ processeur CIM** est dérivée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

WMI n’implémente pas cette classe. Pour les classes WMI dérivées du **\_ processeur CIM**, consultez [classes Win32](win32-provider.md).

Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF. Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.

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

[**\_LOGICALDEVICE CIM**](cim-logicaldevice.md)
</dt> </dl>

 

