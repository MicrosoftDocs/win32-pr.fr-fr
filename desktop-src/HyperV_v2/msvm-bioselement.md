---
description: Représente le logiciel de bas niveau qui est chargé dans la mémoire RAM pour configurer et démarrer le système.
ms.assetid: D123601A-DEE6-43EA-BD95-1F7F0F2C2B43
title: Classe Msvm_BIOSElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BIOSElement
- Msvm_BIOSElement.InstanceID
- Msvm_BIOSElement.Caption
- Msvm_BIOSElement.Description
- Msvm_BIOSElement.ElementName
- Msvm_BIOSElement.InstallDate
- Msvm_BIOSElement.OperationalStatus
- Msvm_BIOSElement.StatusDescriptions
- Msvm_BIOSElement.Status
- Msvm_BIOSElement.HealthState
- Msvm_BIOSElement.CommunicationStatus
- Msvm_BIOSElement.DetailedStatus
- Msvm_BIOSElement.OperatingStatus
- Msvm_BIOSElement.PrimaryStatus
- Msvm_BIOSElement.Name
- Msvm_BIOSElement.SoftwareElementState
- Msvm_BIOSElement.SoftwareElementID
- Msvm_BIOSElement.TargetOperatingSystem
- Msvm_BIOSElement.OtherTargetOS
- Msvm_BIOSElement.BuildNumber
- Msvm_BIOSElement.SerialNumber
- Msvm_BIOSElement.CodeSet
- Msvm_BIOSElement.IdentificationCode
- Msvm_BIOSElement.LanguageEdition
- Msvm_BIOSElement.Version
- Msvm_BIOSElement.Manufacturer
- Msvm_BIOSElement.PrimaryBIOS
- Msvm_BIOSElement.ListOfLanguages
- Msvm_BIOSElement.CurrentLanguage
- Msvm_BIOSElement.LoadedStartingAddress
- Msvm_BIOSElement.LoadedEndingAddress
- Msvm_BIOSElement.LoadUtilityInformation
- Msvm_BIOSElement.ReleaseDate
- Msvm_BIOSElement.RegistryURIs
- Msvm_BIOSElement.BIOSGUID
- Msvm_BIOSElement.BIOSSerialNumber
- Msvm_BIOSElement.BaseBoardSerialNumber
- Msvm_BIOSElement.ChassisSerialNumber
- Msvm_BIOSElement.ChassisAssetTag
- Msvm_BIOSElement.BIOSNumLock
- Msvm_BIOSElement.BootOrder
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8433c8fda6d438e4f77fb763be42467aab05ab976927f018e895a30d5f9c6226
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118149299"
---
# <a name="msvm_bioselement-class"></a>MSVM \_ BIOSElement, classe

Représente le logiciel de bas niveau qui est chargé dans la mémoire RAM pour configurer et démarrer le système. Le BIOS n’est pas un périphérique logique. par conséquent, le BIOS virtuel ne doit pas être considéré comme un périphérique de machine virtuelle. Comme il ne s’agit pas d’un appareil, il n’a pas de pool de ressources correspondant. L’objet BIOS est associé à la machine virtuelle via l’Association [**MSVM \_ SystemBIOS**](msvm-systembios.md) .

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BIOSElement : CIM_BIOSElement
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   Name = "BIOS";
  uint16   SoftwareElementState = 2;
  string   SoftwareElementID = "Microsoft:GUID\device-specific data";
  uint16   TargetOperatingSystem = 0;
  string   OtherTargetOS;
  string   BuildNumber = 14;
  string   SerialNumber;
  string   CodeSet;
  string   IdentificationCode;
  string   LanguageEdition;
  string   Version = "8.02.00";
  string   Manufacturer = "Microsoft Corporation";
  boolean  PrimaryBIOS = True;
  string   ListOfLanguages[] = "en|US|iso8859-1";
  string   CurrentLanguage = "en|US|iso8859-1";
  unit64   LoadedStartingAddress = 0xE0000;
  unit64   LoadedEndingAddress = 0xFFFFF;
  string   LoadUtilityInformation;
  datetime ReleaseDate;
  string   RegistryURIs[];
  string   BIOSGUID;
  string   BIOSSerialNumber;
  string   BaseBoardSerialNumber;
  string   ChassisSerialNumber;
  string   ChassisAssetTag;
  boolean  BIOSNumLock;
  uint16   BootOrder[];
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ BIOSElement** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ BIOSElement** possède les propriétés suivantes.

<dl> <dt>

**BaseBoardSerialNumber**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Numéro de série de la carte de base sur la machine virtuelle.

</dd> <dt>

**BIOSGUID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Identificateur unique du BIOS.

</dd> <dt>

**BIOSNumLock**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

État activé du verrouillage numérique dans le BIOS.

</dd> <dt>

**BIOSSerialNumber**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Numéro de série du BIOS.

</dd> <dt>

**BootOrder**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexé"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (4)
</dt> </dl>

L’ordre dans lequel les appareils seront recherchés pour un secteur d’amorçage au démarrage.

</dd> <dt>

**BuildNumber**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **MaxLen** (64)
</dt> </dl>

Identificateur interne pour cette compilation d’élément logiciel. Cette propriété est héritée de [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)et est toujours définie sur 14.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **MaxLen** (64)
</dt> </dl>

Brève description de l’objet. Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**ChassisAssetTag**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Renseigné automatiquement par le BIOS lorsque la machine virtuelle est créée.

</dd> <dt>

**ChassisSerialNumber**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Renseigné automatiquement par le BIOS lorsque la machine virtuelle est créée.

</dd> <dt>

**Codes**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **MaxLen** (64)
</dt> </dl>

Ensemble de codes utilisé par l’élément logiciel. Cette propriété est héritée de [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)et est toujours définie sur **null**.

</dd> <dt>

**CommunicationStatus**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent. Une valeur **null** indique que cette propriété n’est pas implémentée. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**CurrentLanguage**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Langue actuellement sélectionnée pour le BIOS. Cette propriété est héritée de [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)et est toujours définie sur « en \| -US \| iso8859-1 ».

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

**ElementName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom complet de l’élément. Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie l’intégrité actuelle de l’élément. Cet attribut exprime l’intégrité de cet élément, mais pas nécessairement celle de ses sous-composants.

Lorsqu’une erreur critique se produit, consultez le journal des événements pour plus d’informations. La propriété **EnabledState** peut également contenir plus d’informations. Par exemple, lorsque l’espace disque est très faible, **HealthState** est défini sur 25, l’ordinateur virtuel s’interrompt et **EnabledState** a la valeur 32768 (suspendu).

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).



| Valeur                                                                                                                                                                                                                                                            | Signification                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <dt>**OK**</dt> <dt>5</dt> </dl>                                                                               | L’ordinateur virtuel est entièrement fonctionnel et fonctionne dans des paramètres opérationnels normaux et sans erreur.<br/>                                                                                                                                                                                    |
| <span id="Major_Failure"></span><span id="major_failure"></span><span id="MAJOR_FAILURE"></span><dl> <dt>**Erreur majeure**</dt> <dt>20</dt> </dl>             | L’ordinateur virtuel a subi un échec majeur. Cette valeur est utilisée lorsqu’un ou plusieurs disques contenant les disques durs virtuels de l’ordinateur virtuel manquent d’espace disque et que l’ordinateur virtuel a été suspendu.<br/>                                                                                                   |
| <span id="Critical_failure"></span><span id="critical_failure"></span><span id="CRITICAL_FAILURE"></span><dl> <dt>**Erreur critique**</dt> <dt>25</dt> </dl> | L’élément n’est pas fonctionnel et la récupération n’est peut-être pas possible. Cela peut indiquer que le processus de travail de l’ordinateur virtuel (Vmwp.exe) ne répond pas aux demandes de contrôle ou d’informations, ou qu’un ou plusieurs disques contenant les disques durs virtuels de l’ordinateur virtuel manquent d’espace disque.<br/> |



 

</dd> <dt>

**IdentificationCode**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **MaxLen** (64)
</dt> </dl>

Identificateur du fabricant de cet élément logiciel. Il s’agit souvent d’une référence (SKU) ou d’un numéro de référence. Cette propriété est héritée de [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)et est toujours définie sur **null**.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Renseigné automatiquement par le BIOS lorsque la machine virtuelle est créée. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

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

**LanguageEdition**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **MaxLen** (32)
</dt> </dl>

Édition linguistique de cet élément logiciel. Cette propriété est héritée de [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)et est toujours définie sur **null**.

</dd> <dt>

**ListOfLanguages**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Liste des langues installables pour le BIOS. Cette propriété est héritée de [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)et est toujours définie sur « en \| -US \| iso8859-1 ».

</dd> <dt>

**LoadedEndingAddress**
</dt> <dd> <dl> <dt>

Type de données : **unit64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Adresse de fin de la mémoire occupée par ce BIOS. Cette propriété est héritée de [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)et est toujours définie sur 0xFFFFF.

</dd> <dt>

**LoadedStartingAddress**
</dt> <dd> <dl> <dt>

Type de données : **unit64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Adresse de début de la mémoire occupée par ce BIOS. Cette propriété est héritée de [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)et est toujours définie sur 0xE0000.

</dd> <dt>

**LoadUtilityInformation**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chaîne qui décrit l’utilitaire Flash/chargement BIOS requis pour mettre à jour l’élément BIOS. La version et d’autres informations peuvent être indiquées dans cette propriété. Cette propriété est héritée de [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)et est toujours définie sur **null**.

</dd> <dt>

**Fabricant**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **MaxLen** (256)
</dt> </dl>

Fabricant de ce BIOS. Cette propriété est héritée de [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)et est toujours définie sur « Microsoft Corporation ».

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **MaxLen** (1024)
</dt> </dl>

Nom utilisé pour identifier cet élément logiciel. Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé. Cette propriété est héritée de la [**\_ SoftwareElement CIM**](/windows/desktop/CIMWin32Prov/cim-softwareelement)et est toujours définie sur « BIOS ».

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

Tableau qui contient les États actuels de l’objet. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement). La valeur à l’index zéro (0) est l’une des valeurs suivantes.



| Valeur                                                                                                                                                                                                                                                                   | Signification                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <dt>**OK**</dt> <dt>2</dt> </dl>                                                                                      | L’ordinateur virtuel est fonctionnel et fonctionne normalement.<br/>                                                                                                                                                                                              |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <dt>**Dégradé**</dt> <dt>3</dt> </dl>                                         | L’ordinateur virtuel ne fonctionne que partiellement. Cela indique que le stockage qui contient la configuration n’est pas accessible. Une machine virtuelle dans cet État peut uniquement être désactivée ou supprimée. <br/>                                               |
| <span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span><dl> <dt>**Échec prédictif**</dt> <dt>5</dt> </dl> | L’ordinateur virtuel est fonctionnel mais peut échouer à l’avenir. Cela indique que l’espace libre est insuffisant sur le stockage qui contient le disque dur virtuel de l’ordinateur virtuel. L’ordinateur virtuel sera mis en pause si l’espace disque disponible est insuffisant.<br/> |
| <span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span><dl> <dt></dt> <dt>10</dt> arrêtés </dl>                                            | Cette valeur n’est pas prise en charge. Si la machine virtuelle est arrêtée, la propriété **EnabledState** aura la valeur 3 (désactivé).<br/>                                                                                                                       |
| <span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span><dl> <dt>**Dans le service**</dt> <dt>11</dt> </dl>                                | L’ordinateur virtuel est en cours de traitement d’une demande.<br/>                                                                                                                                                                                                           |
| <span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span><dl> <dt>**Dormant**</dt> <dt>15</dt> </dl>                                            | Cette valeur n’est pas prise en charge. Si la machine virtuelle est interrompue ou suspendue, la propriété **EnabledState** aura la valeur 32769 (suspendu) ou 32768 (suspendu).<br/>                                                                                    |



 

La valeur à l’index 1 (1) est facultative et contient des informations d’état secondaire. Un client doit utiliser l’état principal de l’index zéro (0) pour déterminer si une nouvelle demande peut être émise pour l’ordinateur virtuel. Si **OperationalStatus** \[ 0 \] est égal à 2 (OK), l’opération indiquée par **OperationalStatus** \[ 1 \] peut être interrompue.

La valeur à **OperationalStatus** \[ 1 \] est l’une des valeurs suivantes.



| Valeur                                                                                                                                                                                                                                                                                                   | Signification                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="Creating_Snapshot"></span><span id="creating_snapshot"></span><span id="CREATING_SNAPSHOT"></span><dl> <dt>**Création de l’instantané**</dt> <dt>32768</dt> </dl>                                 | Un instantané est en cours de création pour l’ordinateur virtuel.<br/>             |
| <span id="Applying_Snapshot"></span><span id="applying_snapshot"></span><span id="APPLYING_SNAPSHOT"></span><dl> <dt>**Application de l’instantané**</dt> <dt>32769</dt> </dl>                                 | Un instantané est en cours d’application sur la machine virtuelle.<br/>              |
| <span id="Deleting_Snapshot"></span><span id="deleting_snapshot"></span><span id="DELETING_SNAPSHOT"></span><dl> <dt>**Suppression de l’instantané**</dt> <dt>32770</dt> </dl>                                 | Un instantané est en cours de suppression de l’ordinateur virtuel.<br/>            |
| <span id="Waiting_to_Start"></span><span id="waiting_to_start"></span><span id="WAITING_TO_START"></span><dl> <dt>**En attente de démarrage de**</dt> <dt>32771</dt> </dl>                                     | L’ordinateur virtuel démarre une fois que le délai de démarrage automatique s’est écoulé.<br/> |
| <span id="Merging_Disks"></span><span id="merging_disks"></span><span id="MERGING_DISKS"></span><dl> <dt>**Fusion des disques**</dt> <dt>32772</dt> </dl>                                                 | Les disques durs virtuels des instantanés précédemment supprimés sont en cours de fusion.<br/>             |
| <span id="Exporting_Virtual_Machine"></span><span id="exporting_virtual_machine"></span><span id="EXPORTING_VIRTUAL_MACHINE"></span><dl> <dt>**Exportation de l’ordinateur virtuel**</dt> <dt>32773</dt> </dl> | L’ordinateur virtuel est en cours d’exportation.<br/>                                             |
| <span id="Migrating_Virtual_Machine"></span><span id="migrating_virtual_machine"></span><span id="MIGRATING_VIRTUAL_MACHINE"></span><dl> <dt>**Migration de la machine virtuelle**</dt> <dt>32774</dt> </dl> | L’ordinateur virtuel est en cours de migration dynamique d’un ordinateur physique vers un autre.<br/>  |



 

</dd> <dt>

**OtherTargetOS**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **MaxLen** (64)
</dt> </dl>

Fabricant et système d’exploitation d’un élément logiciel lorsque la propriété **TargetOperatingSystem** a la valeur 1 (autre), ce qui nécessite que la propriété **OtherTargetOS** ait une valeur non **null** . Pour toutes les autres valeurs de **TargetOperatingSystem**, la propriété **OtherTargetOS** doit avoir la **valeur null**. Cette propriété est héritée de [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)et est toujours définie sur **null**.

</dd> <dt>

**PrimaryBIOS**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Si la valeur est true, il s’agit du BIOS principal du système informatique. Cette propriété est héritée de [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)et est toujours définie sur **true**.

</dd> <dt>

**PrimaryStatus**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Fournit des informations d’état de haut niveau. Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir des informations d’état d’intégrité de haut niveau et détaillées pour l’élément et ses sous-composants. Une valeur **null** indique que cette propriété n’est pas implémentée. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**RegistryURIs**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Tableau de chaînes représentant l’emplacement de publication du registre des attributs BIOS ou des registres dont l’implémentation est conforme. Cette propriété est héritée de la [**\_ BIOSElement CIM**](/windows/desktop/CIMWin32Prov/cim-bioselement).

</dd> <dt>

**ReleaseDate**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Date à laquelle le BIOS a été publié. Cette propriété est héritée de la [**\_ BIOSElement CIM**](/windows/desktop/CIMWin32Prov/cim-bioselement).

</dd> <dt>

**SerialNumber**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **MaxLen** (64)
</dt> </dl>

Numéro de série attribué au BIOS. Cette propriété est héritée de la [**\_ SoftwareElement CIM**](/windows/desktop/CIMWin32Prov/cim-softwareelement).

</dd> <dt>

**SoftwareElementID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **MaxLen** (256)
</dt> </dl>

Identificateur de l’élément logiciel. Cette propriété est héritée de [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)et est toujours définie sur « Microsoft :*GUID* \\ *Device-Specific Data*».

</dd> <dt>

**SoftwareElementState**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

État du cycle de vie d’un élément de logiciel. Cette propriété est héritée de [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)et est toujours définie sur 2 (exécutable).

</dd> <dt>

**État**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mais elle n’est pas utilisée.

</dd> <dt>

**StatusDescriptions**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **arrayType** ("indexé")
</dt> </dl>

Tableau qui contient des chaînes qui décrivent les valeurs de tableau **OperationalStatus** correspondantes. Par exemple, si 11 (en service) est la valeur affectée à **OperationalStatus** \[ 0 \] , **StatusDescriptions** \[ 0 \] peut contenir une explication sur la raison pour laquelle l’ordinateur virtuel traite une demande. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**TargetOperatingSystem**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Environnement du système d’exploitation de l’élément. Cette propriété est héritée de la [**\_ SoftwareElement CIM**](/windows/desktop/CIMWin32Prov/cim-softwareelement)et est toujours définie sur 0 (inconnu).

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **MaxLen** (64)
</dt> </dl>

Version du BIOS. Cette propriété est héritée de [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)et est toujours définie sur « 8.02.00 ».

</dd> </dl>

## <a name="remarks"></a>Remarques

L’accès à la classe **MSVM \_ BIOSElement** peut être limité par le filtrage UAC. Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_BIOSELEMENT CIM**](cim-bioselement.md)
</dt> <dt>

[Classes BIOS](bios-classes.md)
</dt> <dt>

[**\_BIOSELEMENT CIM**](/windows/desktop/CIMWin32Prov/cim-bioselement)
</dt> </dl>

 

