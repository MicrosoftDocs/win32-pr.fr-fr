---
description: La \_ classe Win32 NetworkAdapter est déconseillée. Utilisez la \_ classe NetAdapter msft à la place. la \_ classe NetworkAdapterWMI Win32 représente une carte réseau d’un ordinateur exécutant un système d’exploitation Windows.
ms.assetid: f79cb2a1-a249-479d-a495-37a44fdea995
ms.tgt_platform: multiple
title: Classe Win32_NetworkAdapter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapter
- Win32_NetworkAdapter.Reset
- Win32_NetworkAdapter.SetPowerState
- Win32_NetworkAdapter.AdapterType
- Win32_NetworkAdapter.AdapterTypeID
- Win32_NetworkAdapter.AutoSense
- Win32_NetworkAdapter.Availability
- Win32_NetworkAdapter.Caption
- Win32_NetworkAdapter.ConfigManagerErrorCode
- Win32_NetworkAdapter.ConfigManagerUserConfig
- Win32_NetworkAdapter.CreationClassName
- Win32_NetworkAdapter.Description
- Win32_NetworkAdapter.DeviceID
- Win32_NetworkAdapter.ErrorCleared
- Win32_NetworkAdapter.ErrorDescription
- Win32_NetworkAdapter.GUID
- Win32_NetworkAdapter.Index
- Win32_NetworkAdapter.InstallDate
- Win32_NetworkAdapter.Installed
- Win32_NetworkAdapter.InterfaceIndex
- Win32_NetworkAdapter.LastErrorCode
- Win32_NetworkAdapter.MACAddress
- Win32_NetworkAdapter.Manufacturer
- Win32_NetworkAdapter.MaxNumberControlled
- Win32_NetworkAdapter.MaxSpeed
- Win32_NetworkAdapter.Name
- Win32_NetworkAdapter.NetConnectionID
- Win32_NetworkAdapter.NetConnectionStatus
- Win32_NetworkAdapter.NetEnabled
- Win32_NetworkAdapter.NetworkAddresses
- Win32_NetworkAdapter.PermanentAddress
- Win32_NetworkAdapter.PhysicalAdapter
- Win32_NetworkAdapter.PNPDeviceID
- Win32_NetworkAdapter.PowerManagementCapabilities
- Win32_NetworkAdapter.PowerManagementSupported
- Win32_NetworkAdapter.ProductName
- Win32_NetworkAdapter.ServiceName
- Win32_NetworkAdapter.Speed
- Win32_NetworkAdapter.Status
- Win32_NetworkAdapter.StatusInfo
- Win32_NetworkAdapter.SystemCreationClassName
- Win32_NetworkAdapter.SystemName
- Win32_NetworkAdapter.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 55ee65b151778dbfbb4bb8e09fabfb3ae59392966344b951586cd9e08dd1f984
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119973036"
---
# <a name="win32_networkadapter-class"></a>\_Classe NetworkAdapter Win32

La classe **Win32 \_ NetworkAdapter** est déconseillée. Utilisez la [**classe \_ NetAdapter msft**](/previous-versions/windows/desktop/legacy/hh968170(v=vs.85)) à la place. la [classe WMI](../wmisdk/retrieving-a-class.md) **\_ NetworkAdapter Win32** représente une carte réseau d’un ordinateur exécutant un système d’exploitation Windows.

**Win32 \_ NetworkAdapter** fournit uniquement des données IPv4. Pour plus d’informations, consultez [prise en charge d’IPv6 et IPv6 dans WMI](../wmisdk/ipv6-and-ipv4-support-in-wmi.md).

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4C0-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkAdapter : CIM_NetworkAdapter
{
  string   AdapterType;
  uint16   AdapterTypeID;
  boolean  AutoSense;
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   GUID;
  uint32   Index;
  datetime InstallDate;
  boolean  Installed;
  uint32   InterfaceIndex;
  uint32   LastErrorCode;
  string   MACAddress;
  string   Manufacturer;
  uint32   MaxNumberControlled;
  uint64   MaxSpeed;
  string   Name;
  string   NetConnectionID;
  uint16   NetConnectionStatus;
  boolean  NetEnabled;
  string   NetworkAddresses[];
  string   PermanentAddress;
  boolean  PhysicalAdapter;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   ProductName;
  string   ServiceName;
  uint64   Speed;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ NetworkAdapter** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La **classe \_ NetworkAdapter Win32** possède ces méthodes.



| Méthode                                                          | Description                                                                                                                                                                                                                     |
|:----------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Désactive**](disable-method-in-class-win32-networkadapter.md) | Désactive la carte réseau.<br/>                                                                                                                                                                                        |
| [**Activer**](enable-method-in-class-win32-networkadapter.md)   | Active la carte réseau.<br/>                                                                                                                                                                                         |
| **Réinitialiser**                                                       | Non implémenté. Pour plus d’informations sur l’implémentation de cette méthode, consultez la méthode [**Reset**](reset-method-in-class-cim-controller.md) dans [**CIM \_ NetworkAdapter**](cim-networkadapter.md).<br/>                 |
| **SetPowerState**                                               | Non implémenté. Pour plus d’informations sur l’implémentation de cette méthode, consultez la méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) dans [**CIM \_ NetworkAdapter**](cim-networkadapter.md).<br/> |



 

### <a name="properties"></a>Propriétés

La **classe \_ NetworkAdapter Win32** possède ces propriétés.

<dl> <dt>

**AdapterType**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)::[OID \_ GEN \_ média \_ en cours d' \_ utilisation](/windows-hardware/drivers/network/oid-gen-media-in-use)")
</dt> </dl>

Support réseau en cours d’utilisation. Les cartes réseau sont les suivantes :

<dt>

<span id="Ethernet_802.3"></span><span id="ethernet_802.3"></span><span id="ETHERNET_802.3"></span>

**Ethernet 802,3** (« Ethernet 802,3 »)


</dt> <dd></dd> <dt>

<span id="Token_Ring_802.5"></span><span id="token_ring_802.5"></span><span id="TOKEN_RING_802.5"></span>

**Token ring 802,5** (« token ring 802,5 »)


</dt> <dd></dd> <dt>

<span id="Fiber_Distributed_Data_Interface__FDDI_"></span><span id="fiber_distributed_data_interface__fddi_"></span><span id="FIBER_DISTRIBUTED_DATA_INTERFACE__FDDI_"></span>

**FDDI (Fiber** Distributed Data Interface) (« interface de données distribuées (FDDI) »)


</dt> <dd></dd> <dt>

<span id="Wide_Area_Network__WAN_"></span><span id="wide_area_network__wan_"></span><span id="WIDE_AREA_NETWORK__WAN_"></span>

**Réseau** étendu (WAN) (« réseau étendu (WAN) »)


</dt> <dd></dd> <dt>

<span id="LocalTalk"></span><span id="localtalk"></span><span id="LOCALTALK"></span>

**LocalTalk** (« LocalTalk »)


</dt> <dd></dd> <dt>

<span id="Ethernet_using_DIX_header_format"></span><span id="ethernet_using_dix_header_format"></span><span id="ETHERNET_USING_DIX_HEADER_FORMAT"></span>

**Ethernet utilisant le format d’en-tête dix** (« Ethernet à l’aide du format d’en-tête dix »)


</dt> <dd></dd> <dt>

<span id="ARCNET"></span><span id="arcnet"></span>

**Arcnet** (« Arcnet »)


</dt> <dd></dd> <dt>

<span id="ARCNET__878.2_"></span><span id="arcnet__878.2_"></span>

**Arcnet (878,2)** ("arcnet (878,2)")


</dt> <dd></dd> <dt>

<span id="ATM"></span><span id="atm"></span>

**ATM** (« ATM »)


</dt> <dd></dd> <dt>

<span id="Wireless"></span><span id="wireless"></span><span id="WIRELESS"></span>

**Sans fil** (« sans fil »)


</dt> <dd></dd> <dt>

<span id="Infrared_Wireless"></span><span id="infrared_wireless"></span><span id="INFRARED_WIRELESS"></span>

**Infrarouge sans fil** (« infrarouge sans fil »)


</dt> <dd></dd> <dt>

<span id="Bpc"></span><span id="bpc"></span><span id="BPC"></span>

**BPC** (« BPC »)


</dt> <dd></dd> <dt>

<span id="CoWan"></span><span id="cowan"></span><span id="COWAN"></span>

**CoWan** (« CoWan »)


</dt> <dd></dd> <dt>

<span id="1394"></span>

**1394** ("1394")


</dt> <dd></dd> </dl>

</dd> <dt>

**AdapterTypeID**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)::[OID \_ GEN \_ média \_ en cours d' \_ utilisation](/windows-hardware/drivers/network/oid-gen-media-in-use)")
</dt> </dl>

Support réseau en cours d’utilisation. Retourne les mêmes informations que la propriété **AdapterType** , sauf que les informations se trouvent sous la forme d’un entier.

<dt>

<span id="Ethernet_802.3"></span><span id="ethernet_802.3"></span><span id="ETHERNET_802.3"></span>

**Ethernet 802,3** (0)


</dt> <dd></dd> <dt>

<span id="Token_Ring_802.5"></span><span id="token_ring_802.5"></span><span id="TOKEN_RING_802.5"></span>

**Token Ring 802,5** (1)


</dt> <dd></dd> <dt>

<span id="Fiber_Distributed_Data_Interface__FDDI_"></span><span id="fiber_distributed_data_interface__fddi_"></span><span id="FIBER_DISTRIBUTED_DATA_INTERFACE__FDDI_"></span>

**FDDI (Fiber Distributed Data Interface)** (2)


</dt> <dd></dd> <dt>

<span id="Wide_Area_Network__WAN_"></span><span id="wide_area_network__wan_"></span><span id="WIDE_AREA_NETWORK__WAN_"></span>

**Réseau étendu (WAN)** (3)


</dt> <dd></dd> <dt>

<span id="LocalTalk"></span><span id="localtalk"></span><span id="LOCALTALK"></span>

**LocalTalk** (4)


</dt> <dd></dd> <dt>

<span id="Ethernet_using_DIX_header_format"></span><span id="ethernet_using_dix_header_format"></span><span id="ETHERNET_USING_DIX_HEADER_FORMAT"></span>

**Ethernet utilisant le format d’en-tête dix** (5)


</dt> <dd></dd> <dt>

<span id="ARCNET"></span><span id="arcnet"></span>

**Arcnet** (6)


</dt> <dd></dd> <dt>

<span id="ARCNET__878.2_"></span><span id="arcnet__878.2_"></span>

**Arcnet (878,2)** (7)


</dt> <dd></dd> <dt>

<span id="ATM"></span><span id="atm"></span>

**ATM** (8)


</dt> <dd></dd> <dt>

<span id="Wireless"></span><span id="wireless"></span><span id="WIRELESS"></span>

**Sans fil** (9)


</dt> <dd></dd> <dt>

<span id="Infrared_Wireless"></span><span id="infrared_wireless"></span><span id="INFRARED_WIRELESS"></span>

**Infrarouge sans fil** (10)


</dt> <dd></dd> <dt>

<span id="Bpc"></span><span id="bpc"></span><span id="BPC"></span>

**BPC** (11)


</dt> <dd></dd> <dt>

<span id="CoWan"></span><span id="cowan"></span><span id="COWAN"></span>

**CoWan** (12)


</dt> <dd></dd> <dt>

<span id="1394"></span>

**1394** (13)


</dt> <dd></dd> </dl>

</dd> <dt>

**Détection automatique**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Si la **valeur est true**, la carte réseau peut déterminer automatiquement la vitesse de l’attachement ou du support réseau.

Cette propriété est héritée de la carte réseau [**CIM \_**](cim-networkadapter.md).

Cette propriété n’a pas encore été implémentée. Elle retourne une valeur **null** par défaut.

</dd> <dt>

**Disponibilité**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")
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

L’appareil est dans un état d’économie d’énergie, mais son état exact est inconnu.

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

L’appareil est dans un état d’avertissement, mais également dans un état d’économie d’énergie.

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

Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Caption »)
</dt> </dl>

Brève description de l’objet : chaîne d’une ligne.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**ConfigManagerErrorCode**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")
</dt> </dl>

Windows Code d’erreur Configuration Manager.

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

<span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**le pilote de cet appareil a besoin d’une ressource qui ne peut pas être gérée par Windows.** (5)


</dt> <dd>

le pilote de l’appareil requiert une ressource qui ne peut pas être gérée par Windows.

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

<span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows ne pouvez pas vérifier les ressources de ce périphérique.** (13)


</dt> <dd>

Windows ne pouvez pas vérifier les ressources de l’appareil.

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

<span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours d’installation sur cet appareil.** (25)


</dt> <dd>

Windows est toujours en cours de configuration de l’appareil.

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours d’installation sur cet appareil.** (26)


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

<span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**cet appareil ne fonctionne pas correctement car Windows ne peut pas charger les pilotes requis pour cet appareil.** 31


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

Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")
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

Qualificateurs : [ **\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Nom de la première classe concrète à afficher dans la chaîne d’héritage utilisée lors de la création d’une instance. Lorsqu’elle est utilisée avec les autres propriétés de clé de la classe, la propriété permet d’identifier de manière unique toutes les instances de cette classe et de ses sous-classes.

Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")
</dt> </dl>

Description de l’objet.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**DeviceID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("DeviceID"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \\ \\ {4D36E972-E325-11CE-BFC1-08002BE10318}")
</dt> </dl>

Identificateur unique de la carte réseau à partir d’autres périphériques sur le système.

Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

</dd> <dt>

**ErrorCleared**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Si la **valeur est true**, l’erreur signalée dans **LastErrorCode** est maintenant désactivée.

Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Plus d’informations sur l’erreur enregistrée dans **LastErrorCode**, ainsi que sur les actions correctives qui peuvent être prises.

Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

</dd> <dt>

**GUID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Identificateur global unique de la connexion.

</dd> <dt>

**Index**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \\ \\ {4D36E972-E325-11CE-BFC1-08002BE10318}")
</dt> </dl>

Numéro d’index de la carte réseau, stocké dans le registre système.

Exemple : 0

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" date d’installation ")
</dt> </dl>

Date et heure d’installation de l’objet. Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

Cette propriété n’a pas encore été implémentée. Elle retourne une valeur **null** par défaut.

</dd> <dt>

**Installé**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

qualificateurs : [**deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ NetworkCards \| DriverDate")
</dt> </dl>

Si la **valeur est true**, la carte réseau est installée dans le système.

</dd> <dt>

**InterfaceIndex**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Valeur d’index qui identifie de façon unique l’interface réseau locale. La valeur de cette propriété est la même que la valeur de la propriété **InterfaceIndex** dans l’instance de [**Win32 \_ IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable) qui représente l’interface réseau dans la table d’itinéraires.

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

**MACAddress**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« \| fonctions d’entrée et de sortie de l’appareil win32api \| [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)»)
</dt> </dl>

Adresse de contrôle d’accès au média pour cette carte réseau. Une adresse MAC est un numéro unique de 48 bits affecté à la carte réseau par le fabricant. Il identifie de façon unique cette carte réseau et est utilisé pour le mappage des communications réseau TCP/IP.

</dd> <dt>

**Fabricant**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ NetworkCards \| manufacturer")
</dt> </dl>

Nom du fabricant de la carte réseau.

Exemple : « 3COM »

</dd> <dt>

**MaxNumberControlled**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Port du bus DMTF \| 001,9 \| nombre maximal de pièces jointes»)
</dt> </dl>

Nombre maximal de ports directement adressables pris en charge par cette carte réseau. La valeur 0 (zéro) doit être utilisée si le nombre est inconnu.

</dd> <dt>

**MaxSpeed**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**unités**](../wmisdk/standard-qualifiers.md) (« bits par seconde »)
</dt> </dl>

Vitesse maximale, en bits par seconde, pour la carte réseau.

Cette propriété est héritée de la carte réseau [**CIM \_**](cim-networkadapter.md).

Cette propriété n’a pas encore été implémentée. Elle retourne une valeur **null** par défaut.

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")
</dt> </dl>

Étiquette par laquelle l’objet est connu. Lorsqu’elle est sous-classée, la propriété peut être substituée pour être une propriété de clé.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**NetConnectionID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Nom de la connexion réseau tel qu’il apparaît dans le programme **connexions réseau** du panneau de configuration.

</dd> <dt>

**NetConnectionStatus**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

État de la connexion de la carte réseau au réseau.

<dt>

<span id="Disconnected"></span><span id="disconnected"></span><span id="DISCONNECTED"></span>

**Déconnecté** (0)


</dt> <dd></dd> <dt>

<span id="Connecting"></span><span id="connecting"></span><span id="CONNECTING"></span>

**Connexion** (1)


</dt> <dd></dd> <dt>

<span id="Connected"></span><span id="connected"></span><span id="CONNECTED"></span>

**Connecté** (2)


</dt> <dd></dd> <dt>

<span id="Disconnecting"></span><span id="disconnecting"></span><span id="DISCONNECTING"></span>

**Déconnexion** (3)


</dt> <dd></dd> <dt>

<span id="Hardware_Not_Present"></span><span id="hardware_not_present"></span><span id="HARDWARE_NOT_PRESENT"></span>

**Matériel** absent (4)


</dt> <dd></dd> <dt>

<span id="Hardware_Disabled"></span><span id="hardware_disabled"></span><span id="HARDWARE_DISABLED"></span>

**Matériel désactivé** (5)


</dt> <dd></dd> <dt>

<span id="Hardware_Malfunction"></span><span id="hardware_malfunction"></span><span id="HARDWARE_MALFUNCTION"></span>

**Défaillance matérielle** (6)


</dt> <dd></dd> <dt>

<span id="Media_Disconnected"></span><span id="media_disconnected"></span><span id="MEDIA_DISCONNECTED"></span>

**Support déconnecté** (7)


</dt> <dd></dd> <dt>

<span id="Authenticating"></span><span id="authenticating"></span><span id="AUTHENTICATING"></span>

**Authentification** (8)


</dt> <dd></dd> <dt>

<span id="Authentication_Succeeded"></span><span id="authentication_succeeded"></span><span id="AUTHENTICATION_SUCCEEDED"></span>

**Authentification réussie** (9)


</dt> <dd></dd> <dt>

<span id="Authentication_Failed"></span><span id="authentication_failed"></span><span id="AUTHENTICATION_FAILED"></span>

**Échec de l’authentification** (10)


</dt> <dd></dd> <dt>

<span id="Invalid_Address"></span><span id="invalid_address"></span><span id="INVALID_ADDRESS"></span>

**Adresse non valide** (11)


</dt> <dd></dd> <dt>

<span id="Credentials_Required"></span><span id="credentials_required"></span><span id="CREDENTIALS_REQUIRED"></span>

**Informations d’identification requises** (12)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Autres**


</dt> <dd>13 – 65535</dd> </dl>

</dd> <dt>

**Netactivé**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si l’adaptateur est activé ou non. Si la **valeur est true**, l’adaptateur est activé. Vous pouvez activer ou désactiver la carte réseau à l’aide des méthodes [**Enable**](enable-method-in-class-win32-networkadapter.md) et [**Disable**](disable-method-in-class-win32-networkadapter.md) .

</dd> <dt>

**NetworkAddresses**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Carte réseau DMTF 802 Port \| 001,3 ")
</dt> </dl>

Tableau d’adresses réseau pour un adaptateur.

Cette propriété est héritée de la carte réseau [**CIM \_**](cim-networkadapter.md).

Cette propriété n’a pas encore été implémentée. Elle retourne une valeur **null** par défaut.

</dd> <dt>

**PermanentAddress**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Carte réseau DMTF 802 Port \| 001,2 ")
</dt> </dl>

Adresse réseau codée en dur dans un adaptateur. Cette adresse codée en dur peut être modifiée par la mise à niveau du microprogramme ou la configuration logicielle. Si c’est le cas, ce champ doit être mis à jour lorsque la modification est apportée. La propriété doit être laissée vide si aucune adresse codée en dur n’existe pour la carte réseau.

Cette propriété est héritée de la carte réseau [**CIM \_**](cim-networkadapter.md).

Cette propriété n’a pas encore été implémentée. Elle retourne une valeur **null** par défaut.

</dd> <dt>

**PhysicalAdapter**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si l’adaptateur est une carte physique ou logique. Si la **valeur est true**, l’adaptateur est physique.

</dd> <dt>

**PNPDeviceID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")
</dt> </dl>

Windows Identificateur d’appareil Plug-and-Play de l’unité logique.

Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

Exemple : « \* PNP030b »

</dd> <dt>

**PowerManagementCapabilities**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Tableau des fonctionnalités d’alimentation spécifiques d’un périphérique logique.

Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

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

La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) est prise en charge. Cette méthode se trouve sur la classe parente du [**\_ LogicalDevice CIM**](cim-logicaldevice.md) et peut être implémentée. Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)


</dt> <dd>

La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation).

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)


</dt> <dd>

Power-On chronométré pris en charge

La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation) et l' *heure* définie sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.

</dd> </dl>

</dd> <dt>

**PowerManagementSupported**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation (il peut être mis en mode veille, et ainsi de suite). La propriété n’indique pas que les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais uniquement que l’appareil logique est capable de gérer l’alimentation.

Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

</dd> <dt>

**ProductName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ NetworkCards \| ServiceName")
</dt> </dl>

Nom de produit de la carte réseau.

Exemple : « Fast EtherLink XL »

</dd> <dt>

**FormName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ NetworkCards \| ProductName")
</dt> </dl>

Nom de service de la carte réseau. Ce nom est généralement plus petit que le nom complet du produit.

Exemple : « Elnkii »

</dd> <dt>

**Vitesse**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| RFC1213-MIB. ifSpeed "," MIF. \|Carte réseau DMTF 802 Port \| 001,5 "), [**unités**](../wmisdk/standard-qualifiers.md) (" bits par seconde ")
</dt> </dl>

Estimation de la bande passante actuelle en bits par seconde. Pour les points de terminaison qui varient en bande passante ou pour ceux pour lesquels aucune estimation précise ne peut être effectuée, cette propriété doit contenir la bande passante nominale.

Cette propriété est héritée de la carte réseau [**CIM \_**](cim-networkadapter.md).

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**État**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")
</dt> </dl>

État actuel de l’objet. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

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

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|État opérationnel DMTF \| 003,3 ")
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

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Propaged**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Valeur de la propriété **CreationClassName** de l’ordinateur d’étendue.

Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Propaged**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Nom du système d’étendue.

Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

</dd> <dt>

**TimeOfLastReset**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SOFTWARE \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ Perflib \\ \\ 009 \| System Up Time")
</dt> </dl>

Date et heure de la dernière réinitialisation de la carte réseau.

</dd> </dl>

## <a name="remarks"></a>Remarques

La **classe \_ NetworkAdapter Win32** est dérivée de la carte réseau [**CIM \_**](cim-networkadapter.md).

La liste suivante décrit les classes d’associateur pour la carte réseau **Win32 \_**:

-   [**\_PnPEntity Win32**](win32-pnpentity.md)
-   [**\_ComputerSystem Win32**](win32-computersystem.md)
-   [**\_NetworkAdapterConfiguration Win32**](win32-networkadapterconfiguration.md)
-   [**\_IRQResource Win32**](win32-irqresource.md)
-   [**\_DeviceMemoryAddress Win32**](win32-devicememoryaddress.md)
-   [**\_PortResource Win32**](win32-portresource.md)
-   [**\_NetworkProtocol Win32**](win32-networkprotocol.md)
-   [**\_SystemDriver Win32**](win32-systemdriver.md)

De nombreux systèmes possèdent un certain nombre de cartes réseau. Envisagez d’utiliser les éléments suivants comme référence pour rechercher les adaptateurs actuels :

``` syntax
AdapterType: "Ethernet 802.3"
MACAddress: String Length > 16
Availability: 3
PNPDeviceID: InStr ( PNPDeviceID, "PCI") = 1
Installed: vbTrue
ConfigManagerErrorCode: 0
: <keep this as an index to Win32_NetworkAdapterConfiguration>
```

Même en utilisant les qualificateurs ci-dessus, vous récupérerez probablement plus d’une carte réseau valide. Si tel est le cas, vous pouvez utiliser les informations suivantes pour qualifier davantage la recherche de la NetworkAdapterConfiguration Win32 \_ :

``` syntax
Index: <match to DeviceID above>
MACAddress: Length > 16
DefaultIPGateway: String Length > 6
DNSServerSearchOrder: Array of strings with length > 6
IPEnabled: vbTrue
IPAddress: Array of strings with length > 6
```

Une fois que vous avez effectué cette opération, vous aurez probablement réduit votre liste à une ou deux cartes configurées.

Vous pouvez également utiliser la procédure suivante pour Rechercher l’adaptateur par défaut :

1.  Exécutez la requête suivante :

    `"SELECT InterfaceIndex, Destination FROM Win32_IP4RouteTable WHERE Destination='0.0.0.0'"`

    Vous ne devez avoir qu’une destination réseau 0.0.0.0 par défaut.

2.  Utilisez **InterfaceIndex** pour récupérer la carte réseau de votre choix.

    `"SELECT * FROM Win32_NetworkAdapter WHERE InterfaceIndex=" + insertVariableHere`

## <a name="examples"></a>Exemples

l’exemple de code PowerShell [functions WMI](https://Gallery.TechNet.Microsoft.Com/Two-WMI-Functions-94c31b5f) de la galerie TechNet utilise la carte **Win32 \_ NetworkAdapter** pour recréer l’applet de commande Windows [Get-netadapter](/powershell/module/netadapter/get-netadapter?view=win10-ps) .

L’exemple PowerShell [Get-ComputerInfo-Query Computer Info from local/Remote Computers-(WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) PowerShell de la Galerie TechNet utilise un certain nombre d’appels au matériel et aux logiciels, notamment **Win32 \_ NetworkAdapter**, pour afficher des informations sur un système local ou distant.

L' \# exemple de code C suivant utilise l’espace de noms [Microsoft. Management. infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) pour récupérer les cartes réseau actuelles sur l’ordinateur local.


```CSharp
using Microsoft.Management.Infrastructure;
...
static void QueryInstanceFunc()
        {
 
            CimSession session = CimSession.Create("localHost");
            IEnumerable<CimInstance> queryInstance = session.QueryInstances(@"root\cimv2", "WQL", "SELECT * FROM Win32_NetworkAdapter");

            foreach (CimInstance cimObj in queryInstance)
            {
                Console.WriteLine(cimObj.CimInstanceProperties["Name"].ToString());
                Console.WriteLine(cimObj.CimInstanceProperties["Description"].ToString());
                Console.WriteLine();
            }

            Console.ReadLine();
        }
```



L' \# exemple de code C suivant utilise l' https://msdn.microsoft.com/library/system.management.aspx espace de noms pour récupérer les cartes réseau actuelles sur l’ordinateur local.

> [!Note]  
> https://msdn.microsoft.com/library/system.management.aspx contient les classes d’origine utilisées pour accéder à WMI ; Toutefois, ils sont considérés comme plus lents et ne sont généralement pas mis à l’échelle, ainsi que leurs équivalents [Microsoft. Management. infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) .

 


```CSharp
using System.Management;
...
        static void oldSchoolQueryInstanceFunc()
        {

            ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_NetworkAdapter");
            ManagementObjectSearcher searcher = new ManagementObjectSearcher(query);


            ManagementObjectCollection queryCollection = searcher.Get();
            foreach (ManagementObject m in queryCollection)
            {
                Console.WriteLine("ServiceName : {0}", m["Name"]);
                Console.WriteLine("MACAddress : {0}", m["Description"]);
                Console.WriteLine();
            }
            Console.ReadLine();

        }
```



L’exemple de code VBScript suivant décrit comment récupérer les cartes réseau actuelles sur l’ordinateur local.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
Set colItems = objWMIService.ExecQuery("SELECT * FROM Win32_NetworkAdapter")

For Each objItem in colItems 
    Wscript.Echo "Name: " & objItem.Name
    Wscript.Echo "Description: " & objItem.Description
    Wscript.Echo
Next
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

[**\_NETWORKADAPTER CIM**](cim-networkadapter.md)
</dt> <dt>

[Classes matérielles du système informatique](computer-system-hardware-classes.md)
</dt> <dt>

[Tâches WMI : mise en réseau](../wmisdk/wmi-tasks--networking.md)
</dt> <dt>

[Prise en charge D’ipv6 et IPv6 dans WMI](../wmisdk/ipv6-and-ipv4-support-in-wmi.md)
</dt> </dl>

 

 
