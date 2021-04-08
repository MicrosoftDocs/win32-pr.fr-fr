---
description: Représente un lecteur de DVD à l’intérieur d’une machine virtuelle.
ms.assetid: BA813950-436F-46F1-8C1F-79C5AB1A459B
title: Msvm_DVDDrive, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DVDDrive
- Msvm_DVDDrive.SetPowerState
- Msvm_DVDDrive.EnableDevice
- Msvm_DVDDrive.OnlineDevice
- Msvm_DVDDrive.QuiesceDevice
- Msvm_DVDDrive.SaveProperties
- Msvm_DVDDrive.RestoreProperties
- Msvm_DVDDrive.InstanceID
- Msvm_DVDDrive.Caption
- Msvm_DVDDrive.Description
- Msvm_DVDDrive.ElementName
- Msvm_DVDDrive.InstallDate
- Msvm_DVDDrive.Name
- Msvm_DVDDrive.OperationalStatus
- Msvm_DVDDrive.StatusDescriptions
- Msvm_DVDDrive.Status
- Msvm_DVDDrive.HealthState
- Msvm_DVDDrive.CommunicationStatus
- Msvm_DVDDrive.DetailedStatus
- Msvm_DVDDrive.OperatingStatus
- Msvm_DVDDrive.PrimaryStatus
- Msvm_DVDDrive.EnabledState
- Msvm_DVDDrive.OtherEnabledState
- Msvm_DVDDrive.RequestedState
- Msvm_DVDDrive.EnabledDefault
- Msvm_DVDDrive.TimeOfLastStateChange
- Msvm_DVDDrive.AvailableRequestedStates
- Msvm_DVDDrive.TransitioningToState
- Msvm_DVDDrive.SystemCreationClassName
- Msvm_DVDDrive.SystemName
- Msvm_DVDDrive.CreationClassName
- Msvm_DVDDrive.DeviceID
- Msvm_DVDDrive.PowerManagementSupported
- Msvm_DVDDrive.PowerManagementCapabilities
- Msvm_DVDDrive.Availability
- Msvm_DVDDrive.StatusInfo
- Msvm_DVDDrive.LastErrorCode
- Msvm_DVDDrive.ErrorDescription
- Msvm_DVDDrive.ErrorCleared
- Msvm_DVDDrive.OtherIdentifyingInfo
- Msvm_DVDDrive.PowerOnHours
- Msvm_DVDDrive.TotalPowerOnHours
- Msvm_DVDDrive.IdentifyingDescriptions
- Msvm_DVDDrive.AdditionalAvailability
- Msvm_DVDDrive.MaxQuiesceTime
- Msvm_DVDDrive.Capabilities
- Msvm_DVDDrive.CapabilityDescriptions
- Msvm_DVDDrive.ErrorMethodology
- Msvm_DVDDrive.CompressionMethod
- Msvm_DVDDrive.NumberOfMediaSupported
- Msvm_DVDDrive.MaxMediaSize
- Msvm_DVDDrive.DefaultBlockSize
- Msvm_DVDDrive.MaxBlockSize
- Msvm_DVDDrive.MinBlockSize
- Msvm_DVDDrive.NeedsCleaning
- Msvm_DVDDrive.MediaIsLocked
- Msvm_DVDDrive.Security
- Msvm_DVDDrive.LastCleaned
- Msvm_DVDDrive.MaxAccessTime
- Msvm_DVDDrive.UncompressedDataRate
- Msvm_DVDDrive.LoadTime
- Msvm_DVDDrive.UnloadTime
- Msvm_DVDDrive.MountCount
- Msvm_DVDDrive.TimeOfLastMount
- Msvm_DVDDrive.TotalMountTime
- Msvm_DVDDrive.UnitsDescription
- Msvm_DVDDrive.MaxUnitsBeforeCleaning
- Msvm_DVDDrive.UnitsUsed
- Msvm_DVDDrive.FormatsSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e4b3c9006babb2c7e18b6aed6e85cbee47299429
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867954"
---
# <a name="msvm_dvddrive-class"></a>MSVM \_ DVDDrive, classe

Représente un lecteur de DVD à l’intérieur d’une machine virtuelle. Ce lecteur de DVD peut être un périphérique direct (si un disque dur physique a été attaché à la machine virtuelle) ou synthétique et rempli avec un support de fichier ISO. Étant donné que les lecteurs de DVD virtuels et physiques peuvent être ajoutés et supprimés de la machine virtuelle, il existe deux pools de ressources associés à cette classe, l’un pour les lecteurs de DVD direct et l’autre pour les lecteurs de DVD virtuels. Les lecteurs de DVD ne peuvent être ajoutés ou supprimés que si la machine virtuelle est hors connexion.

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_DVDDrive : CIM_DVDDrive
{
  string   InstanceID;
  string   Caption = "DVD Drive";
  string   Description = "Microsoft Virtual DVD Drive";
  string   ElementName = "DVD Drive";
  datetime InstallDate;
  string   Name = "DVD Drive";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 5;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  uint16   CreationClassName = "Msvm_DVDDrive";
  string   DeviceID = "Microsoft:GUID\device-specific-data";
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability = 6;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  string   OtherIdentifyingInfo[];
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[] = 6;
  uint64   MaxQuiesceTime;
  uint32   Capabilities[] = {3, 7};
  string   CapabilityDescriptions[] = {"Random Access", "Supports Removable Media"};
  string   ErrorMethodology = "None";
  string   CompressionMethod = "Not Compressed";
  uint32   NumberOfMediaSupported = 1;
  uint64   MaxMediaSize = 9400000;
  uint64   DefaultBlockSize = 2048;
  uint64   MaxBlockSize = 2048;
  uint64   MinBlockSize = 2048;
  boolean  NeedsCleaning = False;
  boolean  MediaIsLocked = False;
  uint16   Security = 3;
  datetime LastCleaned;
  uint64   MaxAccessTime = 0;
  uint32   UncompressedDataRate;
  uint64   LoadTime = 0;
  uint64   UnloadTime = 0;
  uint64   MountCount = 0;
  datetime TimeOfLastMount;
  uint64   TotalMountTime = 0;
  string   UnitsDescription;
  uint64   MaxUnitsBeforeCleaning = 0xffffffffffffffff;
  uint64   UnitsUsed = 0;
  uint16   FormatsSupported[] = {16, 22};
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ DVDDrive** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **MSVM \_ DVDDrive** possède ces méthodes.



| Méthode                                                         | Description                              |
|:---------------------------------------------------------------|:-----------------------------------------|
| **EnableDevice**                                               | Cette méthode n'est pas prise en charge.<br/> |
| [**LockMedia**](msvm-dvddrive-lockmedia.md)                   | Verrouille ou libère le média.<br/>  |
| **OnlineDevice**                                               | Cette méthode n'est pas prise en charge.<br/> |
| **QuiesceDevice**                                              | Cette méthode n'est pas prise en charge.<br/> |
| [**RequestStateChange**](msvm-dvddrive-requeststatechange.md) | Demande un changement d’État.<br/>      |
| [**Réinitialiser**](msvm-dvddrive-reset.md)                           | Réinitialise l’appareil virtuel.<br/>    |
| **RestoreProperties**                                          | Cette méthode n'est pas prise en charge.<br/> |
| **SaveProperties**                                             | Cette méthode n'est pas prise en charge.<br/> |
| **SetPowerState**                                              | Cette méthode n'est pas prise en charge.<br/> |



 

### <a name="properties"></a>Propriétés

La classe **MSVM \_ DVDDrive** possède les propriétés suivantes.

<dl> <dt>

**AdditionalAvailability**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Disponibilité et état supplémentaires de l’appareil. Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est définie sur 6 (non applicable).

</dd> <dt>

**Disponibilité**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Disponibilité et état principaux de l’appareil. Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est définie sur 6 (non applicable).

</dd> <dt>

**AvailableRequestedStates**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique les valeurs possibles pour le paramètre *RequestedState* de la méthode [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) utilisée pour initier un changement d’État. Les valeurs répertoriées sont un sous-ensemble des valeurs contenues dans la propriété **RequestedStatesSupported** de l’instance associée de la **\_ EnabledLogicalElementCapabilities CIM**, où les valeurs sélectionnées sont une fonction de l’état actuel de l’objet [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)) . Cette propriété peut être non **null** si une implémentation est en mesure de publier l’ensemble de valeurs possibles en tant que fonction de l’état actuel. Cette propriété a la **valeur null** si une implémentation ne peut pas déterminer le jeu de valeurs possibles en tant que fonction de l’état actuel.

Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).

</dd> <dt>

**Capabilities**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Fonctionnalités de l’appareil d’accès aux médias. Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)et est définie avec les valeurs suivantes.



| Valeur                                                                             | Signification                                                                                         |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>{3, 7}</dt> </dl> |                                                                                                 |
| <dl> <dt>3</dt> </dl>      | L’entrée correspondante dans **CapabilityDescriptions** est « accès aléatoire ».<br/>            |
| <dl> <dt>7</dt> </dl>      | L’entrée correspondante dans **CapabilityDescriptions** est « prend en charge les supports amovibles ».<br/> |



 

</dd> <dt>

**CapabilityDescriptions**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Tableau de chaînes de forme libre qui fournit des explications détaillées sur l’accès aux fonctionnalités d’appareil indiquées dans le tableau de propriétés **Capabilities** . Chaque entrée de ce tableau est liée à l’entrée dans le tableau de propriétés des **fonctionnalités** , situé dans le même index. Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Brève description de l’objet. Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**CommunicationStatus**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent. Une valeur **null** indique que cette propriété n’est pas implémentée. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**CompressionMethod**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chaîne qui indique l’algorithme ou l’outil utilisé pour compresser le fichier logique. Si le schéma de compression est inconnu ou n’est pas décrit, utilisez « inconnu ». Si le fichier logique est compressé, mais que le schéma de compression est inconnu ou non décrit, utilisez « compressé ». Si le fichier logique n’est pas compressé, utilisez « non compressé ». Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).

« Non compressé »

Connue

Compact

« Non compressé »

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom de la classe ou de la sous-classe utilisée dans la création d’une instance. Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).

</dd> <dt>

**DefaultBlockSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Taille de bloc par défaut, en octets, pour l’appareil. Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Description de l'objet . Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**DetailedStatus**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires. Une valeur **null** indique que cette propriété n’est pas implémentée. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**DeviceID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est définie sur « Microsoft :*GUID* \\ *Device-Specific-Data*».

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom complet de l’objet. Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**EnabledDefault**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Configuration par défaut ou de démarrage d’un administrateur pour l’état activé d’un élément. Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

États activés et désactivés d’un élément. Il peut également indiquer les transitions entre ces États demandés. Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).

</dd> <dt>

**ErrorCleared**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si l’erreur signalée dans **LastErrorCode** est maintenant désactivée. Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chaîne qui fournit des informations supplémentaires sur l’erreur enregistrée dans **LastErrorCode** et des informations sur les actions correctives qui peuvent être effectuées. Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.

</dd> <dt>

**ErrorMethodology**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chaîne qui décrit les types de détection d’erreurs et de correction pris en charge par cet appareil. Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).

</dd> <dt>

**FormatsSupported**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Formats CD et DVD pris en charge par cet appareil. Cette propriété est héritée de la [**\_ DVDDrive CIM**](/previous-versions//cc136812(v=vs.85)).

Ce tableau contient les valeurs suivantes pour ISO.

<dl> <dt>

{16, 22}
</dt> <dt>

<span id="CD-ROM"></span><span id="cd-rom"></span>**CD-ROM** (16)
</dt> <dt>

<span id="DVD"></span><span id="dvd"></span>**DVD** (22)
</dt> </dl>

Ce tableau contient les valeurs suivantes pour le transfert physique.

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)
</dt> <dt>

<span id="CD-ROM"></span><span id="cd-rom"></span>**CD-ROM** (16)
</dt> <dt>

<span id="CD-ROM_XA"></span><span id="cd-rom_xa"></span>**CD-ROM/XA** (17)
</dt> <dt>

<span id="CD-I"></span><span id="cd-i"></span>**CD-I** (18)
</dt> <dt>

<span id="CD_Recordable"></span><span id="cd_recordable"></span><span id="CD_RECORDABLE"></span>**CD inscriptible** (19)
</dt> <dt>

<span id="DVD"></span><span id="dvd"></span>**DVD** (22)
</dt> <dt>

<span id="DVD-RW_"></span><span id="dvd-rw_"></span>**DVD-RW +** (23)
</dt> <dt>

<span id="DVD-RAM"></span><span id="dvd-ram"></span>**DVD-RAM** (24)
</dt> <dt>

<span id="DVD-ROM"></span><span id="dvd-rom"></span>**DVD-ROM** (25)
</dt> <dt>

<span id="DVD-Video"></span><span id="dvd-video"></span><span id="DVD-VIDEO"></span>**DVD-vidéo** (26)
</dt> <dt>

<span id="Divx"></span><span id="divx"></span><span id="DIVX"></span>**DivX** (27)
</dt> <dt>

<span id="CD-RW"></span><span id="cd-rw"></span>**CD-RW** (33)
</dt> <dt>

<span id="CD-DA"></span><span id="cd-da"></span>**CD-DA** (34)
</dt> <dt>

<span id="CD_"></span><span id="cd_"></span>**CD +** (35)
</dt> <dt>

<span id="DVD_Recordable"></span><span id="dvd_recordable"></span><span id="DVD_RECORDABLE"></span>**DVD enregistrable** (36)
</dt> <dt>

<span id="DVD-RW"></span><span id="dvd-rw"></span>**DVD-RW** (37)
</dt> <dt>

<span id="DVD-Audio"></span><span id="dvd-audio"></span><span id="DVD-AUDIO"></span>**DVD-audio** (38)
</dt> <dt>

<span id="DVD-5"></span><span id="dvd-5"></span>**DVD-5** (39)
</dt> <dt>

<span id="DVD-9"></span><span id="dvd-9"></span>**DVD-9** (40)
</dt> <dt>

<span id="DVD-10"></span><span id="dvd-10"></span>**DVD-10** (41)
</dt> <dt>

<span id="DVD-18"></span><span id="dvd-18"></span>**DVD-18** (42)
</dt> </dl>

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Intégrité actuelle de l’élément. Cet attribut exprime l’intégrité de cet élément, mais pas nécessairement celle de ses sous-composants. Les valeurs possibles sont comprises entre 0 et 30, où 5 signifie que l’élément est entièrement sain et 30 signifie que l’élément est complètement non opérationnel. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**IdentifyingDescriptions**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Tableau de chaînes de forme libre qui fournissent des explications et des détails sur les entrées du tableau de propriétés **OtherIdentifyingInfo** . Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est définie sur **null**.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Date et heure de création de la configuration de l’ordinateur virtuel. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **clé**
</dt> </dl>

Identifie de façon unique une instance de cette classe. Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**LastCleaned**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Date et heure du dernier nettoyage de l’appareil. Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).

</dd> <dt>

**LastErrorCode**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Dernier code d’erreur signalé par l’unité logique. Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.

</dd> <dt>

**LoadTime**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Durée, en millisecondes, à partir de « Load » pour pouvoir lire ou écrire un média. Par exemple, pour les lecteurs de disque, il s’agit de l’intervalle entre un disque qui ne tourne pas vers le disque signalant qu’il est prêt pour la lecture/écriture (c’est-à-dire le disque tournant à des vitesses nominales). Pour les lecteurs de bande, il s’agit de l’heure à partir d’un support injecté pour signaler qu’il est prêt pour une application. Il s’agit généralement de la zone de robot de la bande. Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).

</dd> <dt>

**MaxAccessTime**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Durée, en millisecondes, à passer du premier emplacement sur le média à l’emplacement le plus éloigné par rapport au temps. Pour un lecteur de disque, il s’agit de la recherche complète et du délai de rotation complète. Pour les lecteurs de bande, il s’agit d’une recherche à partir du début de la bande jusqu’au point le plus éloigné physiquement. (La fin d’une bande peut être à son point le plus éloigné physiquement, mais cela n’est pas nécessairement vrai.) Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).

</dd> <dt>

**MaxBlockSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Taille maximale de bloc, en octets, pour les médias accessibles par l’appareil. Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).

</dd> <dt>

**MaxMediaSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Taille maximale, en kilo-octets, des médias pris en charge par cet appareil. Les kilo-octets sont interprétés comme le nombre d’octets multiplié par 1000 (pas le nombre d’octets multiplié par 1024). Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).

</dd> <dt>

**MaxQuiesceTime**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Cette propriété est dépréciée. Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.

</dd> <dt>

**MaxUnitsBeforeCleaning**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Unités maximales qui peuvent être utilisées avant le nettoyage de l’appareil. Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).

</dd> <dt>

**MediaIsLocked**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

**True** si le média est verrouillé dans l’appareil et ne peut pas être éjecté ; Sinon, **false**. Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).

</dd> <dt>

**MinBlockSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Taille de bloc minimale, en octets, pour les médias accessibles par l’appareil. Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).

</dd> <dt>

**MountCount**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Pour un appareil qui prend en charge les supports amovibles, le nombre de fois que ces médias ont été montés pour le transfert de données ou pour nettoyer l’appareil. Pour les appareils qui accèdent à des médias non amovibles, tels que des disques durs, cette propriété n’est pas applicable et doit être définie sur 0. Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Étiquette par laquelle l’objet est connu. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est identique à la propriété **ElementName** .

</dd> <dt>

**NeedsCleaning**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

**True** si l’appareil d’accès aux médias doit être nettoyé ; Sinon, **false**. Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).

</dd> <dt>

**NumberOfMediaSupported**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre maximal de plusieurs médias individuels qui peuvent être pris en charge ou insérés. Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).

</dd> <dt>

**OperatingStatus**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** . Une valeur **null** indique que cette propriété n’est pas implémentée. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

États actuels de l’objet. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**OtherEnabledState**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

État activé ou désactivé de l’élément lorsque la propriété **EnabledState** a la valeur 1 (autre). Cette propriété doit être définie sur **null** lorsque la propriété **EnabledState** a une valeur autre que 1. Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Toutes les données supplémentaires, au-delà des informations d’ID d’appareil, qui peuvent être utilisées pour identifier un périphérique logique. Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est définie sur **null**.

</dd> <dt>

**PowerManagementCapabilities**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Les fonctionnalités de gestion de l’alimentation de l’appareil. Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.

</dd> <dt>

**PowerManagementSupported**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si l’appareil peut être géré par l’alimentation. Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.

</dd> <dt>

**PowerOnHours**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre d’heures consécutives de mise sous tension de cet appareil depuis son dernier cycle d’alimentation. Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.

</dd> <dt>

**PrimaryStatus**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Fournit des informations d’état de haut niveau. Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir des informations d’état d’intégrité de haut niveau et détaillées pour l’élément et ses sous-composants. Une valeur **null** indique que cette propriété n’est pas implémentée. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**RequestedState**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Dernier État demandé ou souhaité pour l’élément. L’état réel de l’élément est représenté par la propriété **EnabledState** . Cette propriété est fournie pour comparer les derniers États activés et actuellement activés ou désactivés. Une instance particulière de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)) peut ne pas prendre en charge la méthode **RequestStateChange** . Si cela se produit, la valeur 12 (non applicable) est utilisée. Cette propriété est héritée de la **\_ EnabledLogicalElement CIM**.

</dd> <dt>

**Sécurité**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

La sécurité opérationnelle définie pour l’appareil. Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).

</dd> <dt>

**État**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

État actuel de l’objet. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mais elle n’est pas utilisée.

</dd> <dt>

**StatusDescriptions**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chaînes qui décrivent les différentes valeurs de tableau **OperationalStatus** . Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**StatusInfo**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

État actuel de l’unité logique. Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom de la classe de création du système d’étendue. Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Identificateur unique de la machine virtuelle d’étendue. Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).

</dd> <dt>

**TimeOfLastMount**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Pour un appareil qui prend en charge les supports amovibles, la date et l’heure les plus récentes de montage du média sur l’appareil. Pour les appareils qui accèdent à des médias non amovibles, tels que des disques durs, cette propriété n’a aucune signification et n’est pas applicable. Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).

</dd> <dt>

**TimeOfLastStateChange**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Date ou heure de la dernière modification de l’état activé de l’élément. Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.

</dd> <dt>

**TotalMountTime**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Pour un appareil qui prend en charge les supports amovibles, durée totale (en secondes) de montage des médias pour le transfert de données ou le nettoyage de l’appareil. Pour les appareils qui accèdent à des médias non amovibles, tels que des disques durs, cette propriété n’est pas applicable et doit être définie sur 0. Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).

</dd> <dt>

**TotalPowerOnHours**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre total d’heures d’alimentation de cet appareil. Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.

</dd> <dt>

**TransitioningToState**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique l’État cible de la transition de l’instance. Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mais elle n’est pas utilisée.

</dd> <dt>

**UncompressedDataRate**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Taux de transfert de données soutenu, en Ko/s, que l’appareil peut lire et écrire sur un média. Il s’agit d’un débit de données brutes soutenu. Les taux ou taux maximaux en supposant que la compression ne doit pas être signalée dans cette propriété. Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).

</dd> <dt>

**UnitsDescription**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Unités relatives à son utilisation dans **MaxUnitsBeforeCleaning**. Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).

</dd> <dt>

**UnitsUsed**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre actuel d’unités utilisées. Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).

</dd> <dt>

**UnloadTime**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Durée, en millisecondes, de la possibilité de lire ou d’écrire un média dans son « déchargement ». Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).

</dd> </dl>

## <a name="remarks"></a>Notes

L’accès à la classe **MSVM \_ DVDDrive** peut être limité par le filtrage UAC. Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_DVDDRIVE CIM**](cim-dvddrive.md)
</dt> <dt>

[**\_DVDDRIVE CIM**](/previous-versions//cc136812(v=vs.85))
</dt> <dt>

[Classes de stockage](storage-classes.md)
</dt> </dl>

 

