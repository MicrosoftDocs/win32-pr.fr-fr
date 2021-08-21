---
description: Représente un système informatique exécutant Windows.
ms.assetid: fdb9fe36-1b8a-4dfa-a1cd-55065017ba2a
ms.tgt_platform: multiple
title: Win32_ComputerSystem, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComputerSystem
- Win32_ComputerSystem.SetPowerState
- Win32_ComputerSystem.AdminPasswordStatus
- Win32_ComputerSystem.AutomaticManagedPagefile
- Win32_ComputerSystem.AutomaticResetBootOption
- Win32_ComputerSystem.AutomaticResetCapability
- Win32_ComputerSystem.BootOptionOnLimit
- Win32_ComputerSystem.BootOptionOnWatchDog
- Win32_ComputerSystem.BootROMSupported
- Win32_ComputerSystem.BootupState
- Win32_ComputerSystem.BootStatus
- Win32_ComputerSystem.Caption
- Win32_ComputerSystem.ChassisBootupState
- Win32_ComputerSystem.ChassisSKUNumber
- Win32_ComputerSystem.CreationClassName
- Win32_ComputerSystem.CurrentTimeZone
- Win32_ComputerSystem.DaylightInEffect
- Win32_ComputerSystem.Description
- Win32_ComputerSystem.DNSHostName
- Win32_ComputerSystem.Domain
- Win32_ComputerSystem.DomainRole
- Win32_ComputerSystem.EnableDaylightSavingsTime
- Win32_ComputerSystem.FrontPanelResetStatus
- Win32_ComputerSystem.HypervisorPresent
- Win32_ComputerSystem.InfraredSupported
- Win32_ComputerSystem.InitialLoadInfo
- Win32_ComputerSystem.InstallDate
- Win32_ComputerSystem.KeyboardPasswordStatus
- Win32_ComputerSystem.LastLoadInfo
- Win32_ComputerSystem.Manufacturer
- Win32_ComputerSystem.Model
- Win32_ComputerSystem.Name
- Win32_ComputerSystem.NameFormat
- Win32_ComputerSystem.NetworkServerModeEnabled
- Win32_ComputerSystem.NumberOfLogicalProcessors
- Win32_ComputerSystem.NumberOfProcessors
- Win32_ComputerSystem.OEMLogoBitmap
- Win32_ComputerSystem.OEMStringArray
- Win32_ComputerSystem.PartOfDomain
- Win32_ComputerSystem.PauseAfterReset
- Win32_ComputerSystem.PCSystemType
- Win32_ComputerSystem.PCSystemTypeEx
- Win32_ComputerSystem.PowerManagementCapabilities
- Win32_ComputerSystem.PowerManagementSupported
- Win32_ComputerSystem.PowerOnPasswordStatus
- Win32_ComputerSystem.PowerState
- Win32_ComputerSystem.PowerSupplyState
- Win32_ComputerSystem.PrimaryOwnerContact
- Win32_ComputerSystem.PrimaryOwnerName
- Win32_ComputerSystem.ResetCapability
- Win32_ComputerSystem.ResetCount
- Win32_ComputerSystem.ResetLimit
- Win32_ComputerSystem.Roles
- Win32_ComputerSystem.Status
- Win32_ComputerSystem.SupportContactDescription
- Win32_ComputerSystem.SystemFamily
- Win32_ComputerSystem.SystemSKUNumber
- Win32_ComputerSystem.SystemStartupDelay
- Win32_ComputerSystem.SystemStartupOptions
- Win32_ComputerSystem.SystemStartupSetting
- Win32_ComputerSystem.SystemType
- Win32_ComputerSystem.ThermalState
- Win32_ComputerSystem.TotalPhysicalMemory
- Win32_ComputerSystem.UserName
- Win32_ComputerSystem.WakeUpType
- Win32_ComputerSystem.Workgroup
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6c6a2d965a764be8925fda55958302d815b62ad6180ce4d3abb48d399fc2e817
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119699999"
---
# <a name="win32_computersystem-class"></a>\_Classe Win32 ComputerSystem

La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **Win32 \_ ComputerSystem** représente un système informatique exécutant Windows.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4B0-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_ComputerSystem : CIM_UnitaryComputerSystem
{
  uint16   AdminPasswordStatus;
  boolean  AutomaticManagedPagefile;
  boolean  AutomaticResetBootOption;
  boolean  AutomaticResetCapability;
  uint16   BootOptionOnLimit;
  uint16   BootOptionOnWatchDog;
  boolean  BootROMSupported;
  string   BootupState;
  uint16   BootStatus[];
  string   Caption;
  uint16   ChassisBootupState;
  string   ChassisSKUNumber;
  string   CreationClassName;
  sint16   CurrentTimeZone;
  boolean  DaylightInEffect;
  string   Description;
  string   DNSHostName;
  string   Domain;
  uint16   DomainRole;
  boolean  EnableDaylightSavingsTime;
  uint16   FrontPanelResetStatus;
  boolean  HypervisorPresent;
  boolean  InfraredSupported;
  string   InitialLoadInfo[];
  datetime InstallDate;
  uint16   KeyboardPasswordStatus;
  string   LastLoadInfo;
  string   Manufacturer;
  string   Model;
  string   Name;
  string   NameFormat;
  boolean  NetworkServerModeEnabled;
  uint32   NumberOfLogicalProcessors;
  uint32   NumberOfProcessors;
  uint8    OEMLogoBitmap[];
  string   OEMStringArray[];
  boolean  PartOfDomain;
  sint64   PauseAfterReset;
  uint16   PCSystemType;
  uint16   PCSystemTypeEx;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   PowerOnPasswordStatus;
  uint16   PowerState;
  uint16   PowerSupplyState;
  string   PrimaryOwnerContact;
  string   PrimaryOwnerName;
  uint16   ResetCapability;
  sint16   ResetCount;
  sint16   ResetLimit;
  string   Roles[];
  string   Status;
  string   SupportContactDescription[];
  string   SystemFamily;
  string   SystemSKUNumber;
  uint16   SystemStartupDelay;
  string   SystemStartupOptions[];
  uint8    SystemStartupSetting;
  string   SystemType;
  uint16   ThermalState;
  uint64   TotalPhysicalMemory;
  string   UserName;
  uint16   WakeUpType;
  string   Workgroup;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ ComputerSystem** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **Win32 \_ ComputerSystem** possède ces méthodes.



| Méthode                                                                                          | Description                                                                                                                                                                                                                                   |
|:------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**JoinDomainOrWorkgroup**](joindomainorworkgroup-method-in-class-win32-computersystem.md)     | Ajoute un système informatique à un domaine ou à un groupe de travail.<br/>                                                                                                                                                                                   |
| [**Renommer**](rename-method-in-class-win32-computersystem.md)                                   | Renomme un ordinateur local.<br/>                                                                                                                                                                                                          |
| **SetPowerState**                                                                               | Non implémenté. Pour plus d’informations sur l’implémentation de cette méthode, consultez la méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) dans [**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md).<br/> |
| [**UnjoinDomainOrWorkgroup**](unjoindomainorworkgroup-method-in-class-win32-computersystem.md) | Supprime un système informatique d’un domaine ou d’un groupe de travail.<br/>                                                                                                                                                                              |



 

### <a name="properties"></a>Propriétés

La classe **Win32 \_ ComputerSystem** possède ces propriétés.

<dl> <dt>

**AdminPasswordStatus**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 24 \| Hardware Security Paramètres \| AdminPasswordStatus")
</dt> </dl>

Paramètres de sécurité du matériel système pour l’état du mot de passe administrateur.

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Désactivé** (0)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Activé** (1)


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

**Non implémenté** (2)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Inconnu** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**AutomaticManagedPagefile**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« WMI »)
</dt> </dl>

Si la **valeur est true**, le système gère le fichier d’échange.

</dd> <dt>

**AutomaticResetBootOption**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ machine \\ \\ System \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| reboot")
</dt> </dl>

Si la **valeur est true**, l’option de démarrage à réinitialisation automatique est activée.

</dd> <dt>

**AutomaticResetCapability**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« WMI »)
</dt> </dl>

Si la **valeur est true**, la réinitialisation automatique est activée.

</dd> <dt>

**BootOptionOnLimit**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« SMBIOS \| type 23 \| - \| option de démarrage on Limit »)
</dt> </dl>

La limite des options de démarrage est activée. Identifie l’action système lorsque la valeur **resetLimit** est atteinte.

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

**Réservé** (0)


</dt> <dd></dd> <dt>

<span id="Operating_system"></span><span id="operating_system"></span><span id="OPERATING_SYSTEM"></span>

**Système d’exploitation** (1)


</dt> <dd></dd> <dt>

<span id="System_utilities"></span><span id="system_utilities"></span><span id="SYSTEM_UTILITIES"></span>

**Utilitaires système** (2)


</dt> <dd></dd> <dt>

<span id="Do_not_reboot"></span><span id="do_not_reboot"></span><span id="DO_NOT_REBOOT"></span>

**Ne pas redémarrer** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**BootOptionOnWatchDog**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| type 23 \| Capabilities \| option Boot option")
</dt> </dl>

Type d’action de redémarrage après l’expiration du minuteur de surveillance.

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

**Réservé** (0)


</dt> <dd></dd> <dt>

<span id="Operating_system"></span><span id="operating_system"></span><span id="OPERATING_SYSTEM"></span>

**Système d’exploitation** (1)


</dt> <dd></dd> <dt>

<span id="System_utilities"></span><span id="system_utilities"></span><span id="SYSTEM_UTILITIES"></span>

**Utilitaires système** (2)


</dt> <dd></dd> <dt>

<span id="Do_not_reboot"></span><span id="do_not_reboot"></span><span id="DO_NOT_REBOOT"></span>

**Ne pas redémarrer** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**BootROMSupported**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« WMI »)
</dt> </dl>

Si la **valeur est true**, indique si une ROM de démarrage est prise en charge.

</dd> <dt>

**BootStatus**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| type 32 \| System Boot information \| Boot Status")
</dt> </dl>

Champs d’État et de données supplémentaires identifiant l’état de démarrage.

Cette valeur provient du membre **État de démarrage** de la structure d' **informations de démarrage du système** dans les informations SMBIOS.

**Windows Server 2012 r2, Windows 8.1, Windows Server 2012, Windows 8, Windows server 2008 r2, Windows 7, Windows server 2008 et Windows Vista :** cette propriété n’est pas prise en charge avant Windows 10 et Windows Server 2016.

</dd> <dt>

**BootupState**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) \| SM \_ CLEANBOOT")
</dt> </dl>

Le système est démarré. Le démarrage de la prévention de défaillance contourne les fichiers de démarrage de l’utilisateur également appelés SafeBoot.

La liste suivante contient les valeurs requises :

<dl> <dd>« Démarrage normal »</dd> <dd>« Démarrage sans échec »</dd> <dd>« Défaillance avec le démarrage réseau »</dd> </dl>

<dt>

<span id="Normal_boot"></span><span id="normal_boot"></span><span id="NORMAL_BOOT"></span>

**Démarrage normal** (« démarrage normal »)


</dt> <dd></dd> <dt>

<span id="Fail-safe_boot"></span><span id="fail-safe_boot"></span><span id="FAIL-SAFE_BOOT"></span>

**Démarrage** de la prévention de défaillance (« démarrage sécurisé »)


</dt> <dd></dd> <dt>

<span id="Fail-safe_with_network_boot"></span><span id="fail-safe_with_network_boot"></span><span id="FAIL-SAFE_WITH_NETWORK_BOOT"></span>

**Prévention de défaillance avec démarrage réseau** (« défaillance avec démarrage réseau »)


</dt> <dd></dd> </dl>

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)
</dt> </dl>

Description succincte de l’objet d’une chaîne d’une ligne.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**ChassisBootupState**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| type 3 \| État de démarrage")
</dt> </dl>

État de démarrage du châssis.

Cette valeur provient du membre d' **État de démarrage** de la structure du **boîtier ou du châssis du système** dans les informations SMBIOS.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Autre** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Inconnu** (2)


</dt> <dd></dd> <dt>

<span id="Safe"></span><span id="safe"></span><span id="SAFE"></span>

**Coffre** (3)


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

**Avertissement** (4)


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

**Critique** (5)


</dt> <dd></dd> <dt>

<span id="Non-recoverable"></span><span id="non-recoverable"></span><span id="NON-RECOVERABLE"></span>

**Non récupérable** (6)


</dt> <dd></dd> </dl>

</dd> <dt>

**ChassisSKUNumber**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« SMBIOS \| type 3 \| \| SKU Number Number »)
</dt> </dl>

Numéro de référence du châssis ou du boîtier sous forme de chaîne.

Cette valeur provient du membre **numéro de référence (SKU** ) de la structure du **boîtier du système ou du châssis** dans les informations SMBIOS.

**Windows Server 2012 r2, Windows 8.1, Windows Server 2012, Windows 8, Windows server 2008 r2, Windows 7, Windows server 2008 et Windows Vista :** cette propriété n’est pas prise en charge avant Windows 10 et Windows Server 2016.

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Nom de la première classe concrète dans la chaîne d’héritage d’une instance. Vous pouvez utiliser cette propriété avec d’autres propriétés de la classe pour identifier toutes les instances de la classe et ses sous-classes.

Cette propriété est héritée [**du \_ système CIM**](cim-system.md).

</dd> <dt>

**CurrentTimeZone**
</dt> <dd> <dl> <dt>

Type de données : **sint16**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| Time structures \| [**\_ \_ information fuseau horaire**](/windows/desktop/api/timezoneapi/ns-timezoneapi-time_zone_information) \| Bias"), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")
</dt> </dl>

Durée pendant laquelle le système informatique unitaire est décalé par rapport au temps universel coordonné (UTC, Universal Time Coordinated).

</dd> <dt>

**DaylightInEffect**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| Time Functions \| [**GetTimeZoneInformation**](/windows/desktop/api/timezoneapi/nf-timezoneapi-gettimezoneinformation)")
</dt> </dl>

Si la **valeur est true**, le mode d’économie d’heure est activé.

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")
</dt> </dl>

Description de l’objet.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**DNSHostName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| GetComputerNameEx \| ComputerNameDnsHostname")
</dt> </dl>

Nom de l’ordinateur local en fonction du serveur de noms de domaine (DNS).

</dd> <dt>

**Domaine**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| Network Management Structures \| [**wksta \_ info \_ 100**](/windows/desktop/api/lmwksta/ns-lmwksta-wksta_info_100) \| wki100 \_ LANGROUP")
</dt> </dl>

Nom du domaine auquel un ordinateur appartient.

> [!Note]  
> Si l’ordinateur ne fait pas partie d’un domaine, le nom du groupe de travail est retourné.

 

</dd> <dt>

**DomainRole**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| Directory Service (DS) structures \| [**DSROLE \_ principal \_ Domain \_ info \_ Basic**](/windows/desktop/api/dsrole/ns-dsrole-dsrole_primary_domain_info_basic) \| [**DSROLE \_ \_ rôle machine**](/windows/desktop/api/dsrole/ne-dsrole-dsrole_machine_role) \| rôle")
</dt> </dl>

Rôle d’un ordinateur dans un groupe de travail de domaine attribué. Un groupe de travail de domaine est un ensemble d’ordinateurs sur le même réseau. Par exemple, une propriété **DomainRole** peut indiquer qu’un ordinateur est une station de travail membre.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

<dt>

<span id="Standalone_Workstation"></span><span id="standalone_workstation"></span><span id="STANDALONE_WORKSTATION"></span>

**Station de travail autonome** (0)


</dt> <dd></dd> <dt>

<span id="Member_Workstation"></span><span id="member_workstation"></span><span id="MEMBER_WORKSTATION"></span>

**Station de travail membre** (1)


</dt> <dd></dd> <dt>

<span id="Standalone_Server"></span><span id="standalone_server"></span><span id="STANDALONE_SERVER"></span>

**Serveur autonome** (2)


</dt> <dd></dd> <dt>

<span id="Member_Server"></span><span id="member_server"></span><span id="MEMBER_SERVER"></span>

**Serveur membre** (3)


</dt> <dd></dd> <dt>

<span id="Backup_Domain_Controller"></span><span id="backup_domain_controller"></span><span id="BACKUP_DOMAIN_CONTROLLER"></span>

**Contrôleur de domaine secondaire** (4)


</dt> <dd></dd> <dt>

<span id="Primary_Domain_Controller"></span><span id="primary_domain_controller"></span><span id="PRIMARY_DOMAIN_CONTROLLER"></span>

**Contrôleur de domaine principal** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**EnableDaylightSavingsTime**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Active l’heure d’été (DST) sur un ordinateur. La valeur **true** indique que l’heure système passe à une heure en avance ou en retard au démarrage ou à la fin de l’heure d’été. La valeur **false** indique que l’heure système ne passe pas à une heure avant ou après le début ou la fin de l’heure d’été. La valeur **null** indique que l’état de l’heure d’été est inconnu sur un système.

</dd> <dt>

**FrontPanelResetStatus**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 24 \| Hardware Security Paramètres \| FrontPanelResetStatus")
</dt> </dl>

Le tableau suivant répertorie les paramètres de sécurité matérielle pour le bouton Réinitialiser sur un ordinateur.

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Désactivé** (0)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Activé** (1)


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

**Non implémenté** (2)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Inconnu** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**HypervisorPresent**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« WMI »)
</dt> </dl>

Si la **valeur est true**, un hyperviseur est présent.

**Windows server 2008 R2, Windows 7, Windows Server 2008 et Windows Vista :** cette propriété n’est pas prise en charge avant Windows 8 et Windows Server 2012.

</dd> <dt>

**InfraredSupported**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« WMI »)
</dt> </dl>

Si la **valeur est true**, un port infrarouge (IR) existe sur un système informatique.

</dd> <dt>

**InitialLoadInfo**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Données requises pour trouver le périphérique de chargement initial ou le service de démarrage pour demander que le système d’exploitation démarre.

Cette propriété est héritée de la [**\_ UnitaryComputerSystem CIM**](cim-unitarycomputersystem.md).

**Windows Server 2008 R2 :** Cette propriété est disponible, mais vide.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")
</dt> </dl>

L’objet est installé. Un objet n’a pas besoin d’une valeur pour indiquer qu’il est installé.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**KeyboardPasswordStatus**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 24 \| Hardware Security Paramètres \| KeyboardPasswordStatus")
</dt> </dl>

Paramètres de sécurité du matériel système pour l’état du mot de passe du clavier.

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Désactivé** (0)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Activé** (1)


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

**Non implémenté** (2)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Inconnu** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**LastLoadInfo**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Entrée de tableau de la propriété **InitialLoadInfo** qui contient les données pour démarrer le système d’exploitation chargé.

Cette propriété est héritée de la [**\_ UnitaryComputerSystem CIM**](cim-unitarycomputersystem.md).

</dd> <dt>

**Fabricant**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 1 \| System Information \| manufacturer")
</dt> </dl>

Nom du fabricant de l’ordinateur.

Exemple : Adventure Works

</dd> <dt>

**Modèle**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 1 \| System Information \| Product Name")
</dt> </dl>

Nom de produit qu’un fabricant donne à un ordinateur. Cette propriété doit avoir une valeur.

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Clé d’une instance de [**\_ système CIM**](cim-system.md) dans un environnement d’entreprise.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**NameFormat**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Valeur de **nom** de système d’ordinateur générée automatiquement. L' [**objet \_ ComputerSystem CIM**](cim-computersystem.md) et ses dérivés sont des objets de niveau supérieur du Common Information Model (CIM). Ils fournissent l’étendue de plusieurs composants. Des [**clés \_ système CIM**](cim-system.md) uniques sont nécessaires, mais vous pouvez définir une méthode heuristique pour créer le nom **\_ ComputerSystem CIM** qui génère le même nom et qui est indépendant du protocole de découverte. Cela empêche les problèmes d’inventaire et de gestion lorsque la même ressource ou entité est découverte plusieurs fois, mais ne peut pas être résolue en un seul objet. L’utilisation d’une méthode heuristique est recommandée, mais pas obligatoire.

L’heuristique est décrite dans la spécification CIM v2 Common Model Specification et suppose que les règles documentées sont utilisées pour déterminer et assigner un nom. La liste des valeurs de **NameFormat** définit la commande permettant d’attribuer un nom de système informatique. Plusieurs règles sont mappées à la même valeur.

La valeur de [**\_ nom CIM CIM**](cim-computersystem.md) calculée à l’aide de l’heuristique est la valeur de clé du système. Toutefois, utilisez des alias pour attribuer un nom différent pour **le \_ ComputerSystem CIM**, qui peut être plus propre à votre entreprise.

Cette propriété est héritée [**du \_ système CIM**](cim-system.md).

Les valeurs sont notamment les suivantes :

<dt>

<span id="IP"></span><span id="ip"></span>

**IP** (« IP »)


</dt> <dd></dd> <dt>

<span id="Dial"></span><span id="dial"></span><span id="DIAL"></span>

**Composer** (« composer »)


</dt> <dd></dd> <dt>

<span id="HID"></span><span id="hid"></span>

**HID** (« HID »)


</dt> <dd></dd> <dt>

<span id="NWA"></span><span id="nwa"></span>

**NWA** (« NWA »)


</dt> <dd></dd> <dt>

<span id="HWA"></span><span id="hwa"></span>

**Hwa** (« Hwa »)


</dt> <dd></dd> <dt>

<span id="X25"></span><span id="x25"></span>

**X25** (« x25 »)


</dt> <dd></dd> <dt>

<span id="ISDN"></span><span id="isdn"></span>

**RNIS** (« RNIS »)


</dt> <dd></dd> <dt>

<span id="IPX"></span><span id="ipx"></span>

**IPX** (« IPX »)


</dt> <dd></dd> <dt>

<span id="DCC"></span><span id="dcc"></span>

**DCC** (« DCC »)


</dt> <dd></dd> <dt>

<span id="ICD"></span><span id="icd"></span>

**ICD** ("ICD")


</dt> <dd></dd> <dt>

<span id="E.164"></span><span id="e.164"></span>

**E. 164** ("e. 164")


</dt> <dd></dd> <dt>

<span id="SNA"></span><span id="sna"></span>

**SNA** (« SNA »)


</dt> <dd></dd> <dt>

<span id="OID_OSI"></span><span id="oid_osi"></span>

**OID/OSI** (« OID/OSI »)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Autre** (« autre »)


</dt> <dd></dd> </dl>

</dd> <dt>

**NetworkServerModeEnabled**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| Network Management Structures \| [**Server \_ info \_ 101**](/windows/desktop/api/lmserver/ns-lmserver-server_info_101) \| sv101 \_ type \| VP \_ type \_ Server")
</dt> </dl>

Si la **valeur est true**, le mode serveur réseau est activé.

</dd> <dt>

**NumberOfLogicalProcessors**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« WMI »)
</dt> </dl>

Nombre de processeurs logiques disponibles sur l’ordinateur.

Vous pouvez utiliser **NumberOfLogicalProcessors** et **NumberOfProcessors** pour déterminer si l’ordinateur est l’hyperthreading. Pour plus d'informations, consultez la section Notes.

</dd> <dt>

**NumberOfProcessors**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| System Information Structures \| [**System \_ INFO**](/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info) \| dwNumberOfProcessors")
</dt> </dl>

Nombre de processeurs physiques actuellement disponibles sur un système. Il s’agit du nombre de processeurs activés pour un système, qui n’inclut pas les processeurs désactivés. Si un système informatique a deux processeurs physiques contenant chacun deux processeurs logiques, la valeur de **NumberOfProcessors** est 2 et **NumberOfLogicalProcessors** est 4. Les processeurs peuvent être multicœurs ou ils peuvent être des processeurs hyperthreading. Pour plus d'informations, consultez la section Notes.

</dd> <dt>

**OEMLogoBitmap**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« WMI »)
</dt> </dl>

Liste de données pour une image bitmap créée par le fabricant d’ordinateurs OEM.

</dd> <dt>

**OEMStringArray**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| type 11 \| " chaînes OEM ")
</dt> </dl>

Liste des chaînes de forme libre qu’un OEM définit. Par exemple, un OEM définit les numéros des documents de référence système, les informations de contact du fabricant, etc.

</dd> <dt>

**PartOfDomain**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")
</dt> </dl>

Si la **valeur est true**, l’ordinateur fait partie d’un domaine. Si la valeur est **null**, cela indique que l’ordinateur n’est pas dans un domaine ou que l’État est inconnu. Si vous supprimez l’ordinateur d’un domaine, la valeur devient **false**.

</dd> <dt>

**PauseAfterReset**
</dt> <dd> <dl> <dt>

Type de données : **sint64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« SMBIOS \| type 23 \| timeout »), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (« milliseconds »)
</dt> </dl>

Délai avant le lancement d’un redémarrage en millisecondes. Elle est utilisée après un cycle d’alimentation du système, une réinitialisation du système local ou distant et une réinitialisation automatique du système. La valeur 1 (moins un) indique que la valeur de pause est inconnue.

**Windows Vista :** Cette propriété peut retourner un nombre inconnu.

</dd> <dt>

**PCSystemType**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")
</dt> </dl>

Type de l’ordinateur en cours d’utilisation, tel qu’un ordinateur portable, un ordinateur de bureau ou une tablette.

<dt>

<span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span>

<span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span>**Non spécifié** (0)


</dt> <dd></dd> <dt>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>**Bureau** (1)


</dt> <dd></dd> <dt>

<span id="Mobile"></span><span id="mobile"></span><span id="MOBILE"></span>

<span id="Mobile"></span><span id="mobile"></span><span id="MOBILE"></span>**Mobile** (2)


</dt> <dd></dd> <dt>

<span id="Workstation"></span><span id="workstation"></span><span id="WORKSTATION"></span>

<span id="Workstation"></span><span id="workstation"></span><span id="WORKSTATION"></span>**Station de travail** (3)


</dt> <dd></dd> <dt>

<span id="Enterprise_Server"></span><span id="enterprise_server"></span><span id="ENTERPRISE_SERVER"></span>

<span id="Enterprise_Server"></span><span id="enterprise_server"></span><span id="ENTERPRISE_SERVER"></span>**serveur Enterprise** (4)


</dt> <dd></dd> <dt>

<span id="SOHO_Server"></span><span id="soho_server"></span><span id="SOHO_SERVER"></span>

<span id="SOHO_Server"></span><span id="soho_server"></span><span id="SOHO_SERVER"></span>**Serveur Soho** (5)


</dt> <dd>

serveur SOHO (small Office et home Office)

</dd> <dt>

<span id="Appliance_PC"></span><span id="appliance_pc"></span><span id="APPLIANCE_PC"></span>

<span id="Appliance_PC"></span><span id="appliance_pc"></span><span id="APPLIANCE_PC"></span>**PC d’appliance** (6)


</dt> <dd></dd> <dt>

<span id="Performance_Server"></span><span id="performance_server"></span><span id="PERFORMANCE_SERVER"></span>

<span id="Performance_Server"></span><span id="performance_server"></span><span id="PERFORMANCE_SERVER"></span>**Serveur de performances** (7)


</dt> <dd></dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Maximum** (8)


</dt> <dd></dd> </dl>

</dd> <dt>

**PCSystemTypeEx**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")
</dt> </dl>

Type de l’ordinateur en cours d’utilisation, tel qu’un ordinateur portable, un ordinateur de bureau ou une tablette.

**Windows Server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 et Windows Vista :** cette propriété n’est pas prise en charge avant Windows 8.1 et Windows Server 2012 R2.

<dt>

<span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span>

**Non spécifié** (0)


</dt> <dd></dd> <dt>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>

**Bureau** (1)


</dt> <dd></dd> <dt>

<span id="Mobile"></span><span id="mobile"></span><span id="MOBILE"></span>

**Mobile** (2)


</dt> <dd></dd> <dt>

<span id="Workstation"></span><span id="workstation"></span><span id="WORKSTATION"></span>

**Station de travail** (3)


</dt> <dd></dd> <dt>

<span id="Enterprise_Server"></span><span id="enterprise_server"></span><span id="ENTERPRISE_SERVER"></span>

**serveur Enterprise** (4)


</dt> <dd></dd> <dt>

<span id="SOHO_Server"></span><span id="soho_server"></span><span id="SOHO_SERVER"></span>

**Serveur Soho** (5)


</dt> <dd></dd> <dt>

<span id="Appliance_PC"></span><span id="appliance_pc"></span><span id="APPLIANCE_PC"></span>

**PC d’appliance** (6)


</dt> <dd></dd> <dt>

<span id="Performance_Server"></span><span id="performance_server"></span><span id="PERFORMANCE_SERVER"></span>

**Serveur de performances** (7)


</dt> <dd></dd> <dt>

<span id="Slate"></span><span id="slate"></span><span id="SLATE"></span>

**Ardoise** (8)


</dt> <dd></dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

**Maximum** (9)


</dt> <dd></dd> </dl>

</dd> <dt>

**PowerManagementCapabilities**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Contrôle d’alimentation du système DMTF \| 001,2»)
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

Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation, par exemple, un appareil peut être mis en mode de suspension, et ainsi de suite. Cette propriété n’indique pas si les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais elle indique que l’appareil logique est capable de gérer l’alimentation.

Cette propriété est héritée de la [**\_ UnitaryComputerSystem CIM**](cim-unitarycomputersystem.md).

</dd> <dt>

**PowerOnPasswordStatus**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 24 \| Hardware Security Paramètres \| PowerOnPasswordStatus")
</dt> </dl>

Paramètres de sécurité du matériel système pour Power-On l’état du mot de passe.

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Désactivé** (0)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Activé** (1)


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

**Non implémenté** (2)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Inconnu** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**PowerState**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

État d’alimentation actuel d’un ordinateur et du système d’exploitation qui lui est associé. Les États d’économie d’énergie ont les valeurs suivantes : valeur 4 (inconnu) indique que le système est connu pour être en mode d’économie d’énergie, mais son état exact dans ce mode est inconnu. 2 (mode faible puissance) indique que le système est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées. 3 (veille) indique que le système ne fonctionne pas, mais qu’il peut être mis à la pleine puissance rapidement ; et 7 (avertissement) indique que le système informatique est dans un état d’avertissement et qu’il s’agit d’un mode d’économie d’énergie.

Cette propriété est héritée de la [**\_ UnitaryComputerSystem CIM**](cim-unitarycomputersystem.md).

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)


</dt> <dd></dd> <dt>

<span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>

<span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>**Pleine puissance** (1)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (2)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (3)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (4)


</dt> <dd></dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (5)


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (6)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (7)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Hibernate"></span><span id="power_save_-_hibernate"></span><span id="POWER_SAVE_-_HIBERNATE"></span>

<span id="Power_Save_-_Hibernate"></span><span id="power_save_-_hibernate"></span><span id="POWER_SAVE_-_HIBERNATE"></span>Économie **d’énergie-mise en veille prolongée** (8)


</dt> <dd>

Économie d’énergie en veille prolongée.

</dd> <dt>

<span id="Power_Save_-_Soft_Off"></span><span id="power_save_-_soft_off"></span><span id="POWER_SAVE_-_SOFT_OFF"></span>

<span id="Power_Save_-_Soft_Off"></span><span id="power_save_-_soft_off"></span><span id="POWER_SAVE_-_SOFT_OFF"></span>Économie **d’énergie-désactivation douce** (9)


</dt> <dd>

Économie d’énergie.

</dd> </dl>

</dd> <dt>

**PowerSupplyState**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| type 3 \| Enclosure System ou châssis \| Power Supply State")
</dt> </dl>

État de l’alimentation ou des fournitures lors du dernier démarrage.

Cette valeur provient du membre de l' **État** de l’alimentation du **boîtier du système ou** de la structure du châssis dans les informations SMBIOS.

La liste suivante identifie les valeurs de cette propriété.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)


</dt> <dd></dd> <dt>

<span id="Safe"></span><span id="safe"></span><span id="SAFE"></span>

<span id="Safe"></span><span id="safe"></span><span id="SAFE"></span>**Coffre** (3)


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critique** (5)


</dt> <dd></dd> <dt>

<span id="Non-recoverable"></span><span id="non-recoverable"></span><span id="NON-RECOVERABLE"></span>

<span id="Non-recoverable"></span><span id="non-recoverable"></span><span id="NON-RECOVERABLE"></span>**Non récupérable** (6)


</dt> <dd>

Non récupérable

</dd> </dl>

</dd> <dt>

**PrimaryOwnerContact**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Informations de contact pour le propriétaire du système principal, par exemple, numéro de téléphone, adresse de messagerie, etc.

Cette propriété est héritée [**du \_ système CIM**](cim-system.md).

</dd> <dt>

**PrimaryOwnerName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Nom du propriétaire du système principal.

Cette propriété est héritée [**du \_ système CIM**](cim-system.md).

</dd> <dt>

**ResetCapability**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| System Hardware Security \| 001,4»)
</dt> </dl>

S’il est activé, la valeur est 4 et le système d’ordinateur unitaire peut être réinitialisé à l’aide des boutons d’alimentation et de réinitialisation. Si elle est désactivée, la valeur est 3 et aucune réinitialisation n’est autorisée.

Cette propriété est héritée de la [**\_ UnitaryComputerSystem CIM**](cim-unitarycomputersystem.md).

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (3)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (4)


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>**Non implémenté** (5)


</dt> <dd>

Non récupérable

</dd> </dl>

</dd> <dt>

**ResetCount**
</dt> <dd> <dl> <dt>

Type de données : **sint16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| type 23 \| System Reset rereset \| Count")
</dt> </dl>

Nombre de réinitialisations automatiques depuis la dernière réinitialisation. La valeur 1 (moins un) indique que le nombre est inconnu.

</dd> <dt>

**ResetLimit**
</dt> <dd> <dl> <dt>

Type de données : **sint16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| type 23 \| System Reset reconfigure \| Limit")
</dt> </dl>

Nombre de tentatives de réinitialisation du système consécutives. La valeur 1 (moins un) indique que la limite est inconnue.

</dd> <dt>

**Rôles**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Liste qui spécifie les rôles d’un système dans l’environnement informatique.

Cette propriété est héritée [**du \_ système CIM**](cim-system.md).

</dd> <dt>

**État**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")
</dt> </dl>

État actuel d’un objet.

Pour Win32_ComputerSystem, l’État est toujours « OK ».

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dl>

</dd> <dt>

**SupportContactDescription**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| [**GetPrivateProfileString**](/windows/desktop/api/winbase/nf-winbase-getprivateprofilestring) \| support information")
</dt> </dl>

liste des informations de contact du support technique pour le système d’exploitation Windows.

</dd> <dt>

**SystemFamily**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 1 \| System Information \| Family")
</dt> </dl>

Famille à laquelle appartient un ordinateur particulier. Une famille fait référence à un ensemble d’ordinateurs similaires, mais non identiques à ceux d’un point de vue matériel ou logiciel.

cette valeur provient du membre de la **famille** de la structure **System Information** dans les informations SMBIOS.

**Windows Server 2012 r2, Windows 8.1, Windows Server 2012, Windows 8, Windows server 2008 r2, Windows 7, Windows server 2008 et Windows Vista :** cette propriété n’est pas prise en charge avant Windows 10 et Windows Server 2016.

</dd> <dt>

**SystemSKUNumber**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« SMBIOS \| Type 1 \| System Information \| SKU Number »)
</dt> </dl>

Identifie une configuration d’ordinateur spécifique pour la vente. Il est parfois également appelé ID de produit ou numéro de bon de commande.

cette valeur provient du membre **numéro de référence (SKU** ) de la structure **System Information** dans les informations SMBIOS.

**Windows Server 2012 r2, Windows 8.1, Windows Server 2012, Windows 8, Windows server 2008 r2, Windows 7, Windows server 2008 et Windows Vista :** cette propriété n’est pas prise en charge avant Windows 10 et Windows Server 2016.

</dd> <dt>

**SystemStartupDelay**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Privileges**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("SeSystemEnvironmentPrivilege"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| [**GetPrivateProfileInt**](/windows/desktop/api/winbase/nf-winbase-getprivateprofileint) \| Boot Loader \| timeout"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")
</dt> </dl>

**SystemStartupDelay** ne peut plus être utilisé, car Boot.ini n’est pas utilisé pour configurer le démarrage du système. Utilisez plutôt les [classes BCD](/previous-versions/windows/desktop/bcd/bcd-classes) fournies par le fournisseur WMI données de configuration de démarrage (BCD) (BCD) ou la commande **bcdedit** .

</dd> <dt>

**SystemStartupOptions**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Privileges**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("SeSystemEnvironmentPrivilege"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| [**GetPrivateProfileSection**](/windows/desktop/api/winbase/nf-winbase-getprivateprofilesection) \| Operating Systems")
</dt> </dl>

**SystemStartupOptions** ne peut plus être utilisé, car Boot.ini n’est pas utilisé pour configurer le démarrage du système. Utilisez plutôt les [classes BCD](/previous-versions/windows/desktop/bcd/bcd-classes) fournies par le fournisseur WMI données de configuration de démarrage (BCD) (BCD) ou la commande **bcdedit** .

</dd> <dt>

**SystemStartupSetting**
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**privilèges**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) (« SeSystemEnvironmentPrivilege »), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« WMI »)
</dt> </dl>

**SystemStartupSetting** ne peut plus être utilisé, car Boot.ini n’est pas utilisé pour configurer le démarrage du système. Utilisez plutôt les [classes BCD](/previous-versions/windows/desktop/bcd/bcd-classes) fournies par le fournisseur WMI données de configuration de démarrage (BCD) (BCD) ou la commande **bcdedit** .

</dd> <dt>

**SystemType**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| System Information Structures \| [**System \_ INFO**](/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info) \| wProcessorArchitecture")
</dt> </dl>

système s’exécutant sur l’ordinateur Windows. Cette propriété doit avoir une valeur.

La liste suivante identifie certaines des valeurs possibles pour cette propriété.

<dl> <dd>« PC basé sur x64 »</dd> <dd>« PC x86 »</dd> <dd>« PC basé sur MIPS »</dd> <dd>« PC à base alpha »</dd> <dd>« Power PC »</dd> <dd>« SH-x PC »</dd> <dd>« StrongARM PC »</dd> <dd>« PC Intel 64 bits »</dd> <dd>« PC alpha 64 bits »</dd> <dd>Connue</dd> <dd>« PC x86-Nec98 »</dd> </dl>

<dt>

<span id="X86-based_PC"></span><span id="x86-based_pc"></span><span id="X86-BASED_PC"></span>

**PC x86** (« PC x86 »)


</dt> <dd></dd> <dt>

<span id="MIPS-based_PC"></span><span id="mips-based_pc"></span><span id="MIPS-BASED_PC"></span>

**PC basé sur mips** (« PC basé sur mips »)


</dt> <dd></dd> <dt>

<span id="Alpha-based_PC"></span><span id="alpha-based_pc"></span><span id="ALPHA-BASED_PC"></span>

**PC à base alpha** (« PC à base alpha »)


</dt> <dd></dd> <dt>

<span id="Power_PC"></span><span id="power_pc"></span><span id="POWER_PC"></span>

**Power PC** (« Power PC »)


</dt> <dd></dd> <dt>

<span id="SH-x_PC"></span><span id="sh-x_pc"></span><span id="SH-X_PC"></span>

**SH-x PC** (« SH-x PC »)


</dt> <dd></dd> <dt>

<span id="StrongARM_PC"></span><span id="strongarm_pc"></span><span id="STRONGARM_PC"></span>

**StrongARM PC** (« StrongARM PC »)


</dt> <dd></dd> <dt>

<span id="64-bit_Intel_PC"></span><span id="64-bit_intel_pc"></span><span id="64-BIT_INTEL_PC"></span>

**PC intel 64 bits** (« pc Intel 64 bits »)


</dt> <dd></dd> <dt>

<span id="x64-based_PC"></span><span id="x64-based_pc"></span><span id="X64-BASED_PC"></span>

**PC avec processeur x64** (« PC basé sur x64 »)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Inconnu** ("inconnu")


</dt> <dd></dd> <dt>

<span id="X86-Nec98_PC"></span><span id="x86-nec98_pc"></span><span id="X86-NEC98_PC"></span>

**PC x86-NEC98 PC** (« PC x86-NEC98 »)


</dt> <dd></dd> </dl>

</dd> <dt>

**ThermalState**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| type 3 \| Enclosure System ou châssis \| thermal State")
</dt> </dl>

État thermique du système au dernier démarrage.

Cette valeur provient du membre d' **état thermique** de la structure du **boîtier ou du châssis du système** dans les informations SMBIOS.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Autre** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Inconnu** (2)


</dt> <dd></dd> <dt>

<span id="Safe"></span><span id="safe"></span><span id="SAFE"></span>

**Coffre** (3)


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

**Avertissement** (4)


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

**Critique** (5)


</dt> <dd></dd> <dt>

<span id="Non-recoverable"></span><span id="non-recoverable"></span><span id="NON-RECOVERABLE"></span>

**Non récupérable** (6)


</dt> <dd></dd> </dl>

</dd> <dt>

**TotalPhysicalMemory**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api de \| gestion de mémoire \| [**MEMORYSTATUS**](/windows/desktop/api/winbase/ns-winbase-memorystatus) \| dwTotalPhys"), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")
</dt> </dl>

Taille totale de la mémoire physique. Sachez que, dans certains cas, cette propriété peut ne pas retourner une valeur exacte pour la mémoire physique. Par exemple, il n’est pas exact si le BIOS utilise une partie de la mémoire physique. Pour obtenir une valeur précise, utilisez à la place la propriété **Capacity** dans [**Win32 \_ PhysicalMemory**](win32-physicalmemory.md) .

Exemple : 67108864

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**UserName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| System Information functions \| [**GetUserName**](/windows/desktop/api/winbase/nf-winbase-getusernamea)")
</dt> </dl>

Nom d’un utilisateur qui a ouvert une session actuellement. Cette propriété doit avoir une valeur. Dans une session des services Terminal Server, **username** retourne le nom de l’utilisateur qui est connecté à la console, et non celui de l’utilisateur connecté pendant la session du service Terminal Server.

Exemple : JeffSmith

</dd> <dt>

**WakeUpType**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| type 1 \| System Information \| type de mise en éveil")
</dt> </dl>

Événement qui provoque la mise sous tension du système.

cette valeur provient du membre de **Type de mise en éveil** de la structure **System Information** dans les informations SMBIOS.

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

**Réservé** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Autre** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Inconnu** (2)


</dt> <dd></dd> <dt>

<span id="APM_Timer"></span><span id="apm_timer"></span><span id="APM_TIMER"></span>

**Minuteur APM** (3)


</dt> <dd></dd> <dt>

<span id="Modem_Ring"></span><span id="modem_ring"></span><span id="MODEM_RING"></span>

**Sonnerie de modem** (4)


</dt> <dd></dd> <dt>

<span id="LAN_Remote"></span><span id="lan_remote"></span><span id="LAN_REMOTE"></span>

**Réseau local distant** (5)


</dt> <dd></dd> <dt>

<span id="Power_Switch"></span><span id="power_switch"></span><span id="POWER_SWITCH"></span>

**Commutateur d’alimentation** (6)


</dt> <dd></dd> <dt>

<span id="PCI_PME_"></span><span id="pci_pme_"></span>

**PME \# PCI** Commission(7


</dt> <dd></dd> <dt>

<span id="AC_Power_Restored"></span><span id="ac_power_restored"></span><span id="AC_POWER_RESTORED"></span>

**Alimentation secteur restaurée** (8)


</dt> <dd></dd> </dl>

</dd> <dt>

**Groupe de travail**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")
</dt> </dl>

Nom du groupe de travail pour cet ordinateur. Si la valeur de la propriété **PartOfDomain** est **false**, le nom du groupe de travail est retourné.

</dd> </dl>

## <a name="remarks"></a>Remarques

Pour déterminer le nombre total d’instances de processeur associées à un objet système informatique, utilisez la classe d’association [**Win32 \_ ComputerSystemProcessor**](win32-computersystemprocessor.md) .

Plusieurs instances de [**\_ processeur Win32**](win32-processor.md) sont associées à une instance **\_ ComputerSystem Win32** avec plusieurs processeurs physiques. Si la valeur de **NumberOfLogicalProcessors** est supérieure à la valeur de **NumberOfProcessors** , le système informatique est soit un système multicœur, soit un ou plusieurs processeurs activés pour l’hyperthreading. Pour plus d’informations, consultez les propriétés **NumberOfLogicalProcessors** et **NumberOfCores** et la section Notes dans le **\_ processeur Win32**.

La classe **Win32 \_ ComputerSystem** est dérivée de la [**\_ UnitaryComputerSystem CIM**](cim-unitarycomputersystem.md).

## <a name="examples"></a>Exemples

L' [exemple de code](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Display-computers-status-c8ff289d) du centre de script suivant utilise **Win32 \_ ComputerSystem** pour récupérer des informations à partir de plusieurs systèmes informatiques et les afficher dans une interface utilisateur graphique.

Vous trouverez un exemple de script qui obtient les données du système d’exploitation et du processeur à partir de **Win32 \_ ComputerSystem**, du [**\_ processeur Win32**](win32-processor.md)et de [**Win32 \_ OperatingSystem**](win32-operatingsystem.md) dans les exemples de sujets relatifs au [**\_ processeur Win32**](win32-processor.md) .

L’exemple VBScript suivant décrit comment récupérer le nom de domaine de l’ordinateur local à partir d’instances de **Win32 \_ ComputerSystem**.


```VB
Set SystemSet = GetObject("winmgmts:").InstancesOf ("Win32_ComputerSystem")

for each System in SystemSet
 WScript.Echo System.Domain
next
```



L’exemple perl suivant décrit comment récupérer le nom de l’ordinateur local à partir des instances de **Win32 \_ ComputerSystem**.


```
use strict;
use Win32::OLE;

my ($SystemSet, $System);  
eval {$SystemSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
  InstancesOf ("Win32_ComputerSystem") };
  
unless($@)
{
 foreach $System (in $SystemSet)
 {
  print "\n", $System->{Domain}, "\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



L’exemple perl suivant décrit comment récupérer le nom de domaine DNS de l’ordinateur local à partir des instances de **Win32 \_ ComputerSystem**.


```
use strict;
use Win32::OLE;

close (STDERR);

my ($NICSet, $NIC);  
eval {$NICSet = Win32::OLE->GetObject("winmgmts:!\\\\.\\root\\cimv2")->
 ExecQuery("SELECT * FROM Win32_NetworkAdapterConfiguration WHERE IPEnabled=true"); };
if (!$@ && defined $NICSet)
{
 foreach $NIC (in $NICSet)
 {
  if(defined $NIC->{DNSDomain})
  {
   print "\n", $NIC->{DNSDomain}, "\n";
  }
 }
}
else
{
 print Win32::OLE->LastError, "\n";
}
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

[**\_UNITARYCOMPUTERSYSTEM CIM**](cim-unitarycomputersystem.md)
</dt> <dt>

[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[Tâches WMI : comptes et domaines](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[Tâches WMI : matériel de l’ordinateur](/windows/desktop/WmiSdk/wmi-tasks--computer-hardware)
</dt> <dt>

[Tâches WMI : gestion des postes de travail](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> </dl>

 

