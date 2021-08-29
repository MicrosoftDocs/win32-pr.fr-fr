---
description: Représente le service de virtualisation présent sur un système hôte unique.
ms.assetid: 7f4bd9e0-b034-4882-ad01-f7df740939ae
title: Classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService
- Msvm_VirtualSystemManagementService.InstanceID
- Msvm_VirtualSystemManagementService.Caption
- Msvm_VirtualSystemManagementService.Description
- Msvm_VirtualSystemManagementService.ElementName
- Msvm_VirtualSystemManagementService.InstallDate
- Msvm_VirtualSystemManagementService.Name
- Msvm_VirtualSystemManagementService.OperationalStatus
- Msvm_VirtualSystemManagementService.StatusDescriptions
- Msvm_VirtualSystemManagementService.Status
- Msvm_VirtualSystemManagementService.HealthState
- Msvm_VirtualSystemManagementService.CommunicationStatus
- Msvm_VirtualSystemManagementService.DetailedStatus
- Msvm_VirtualSystemManagementService.OperatingStatus
- Msvm_VirtualSystemManagementService.PrimaryStatus
- Msvm_VirtualSystemManagementService.EnabledState
- Msvm_VirtualSystemManagementService.OtherEnabledState
- Msvm_VirtualSystemManagementService.RequestedState
- Msvm_VirtualSystemManagementService.EnabledDefault
- Msvm_VirtualSystemManagementService.TimeOfLastStateChange
- Msvm_VirtualSystemManagementService.AvailableRequestedStates
- Msvm_VirtualSystemManagementService.TransitioningToState
- Msvm_VirtualSystemManagementService.SystemCreationClassName
- Msvm_VirtualSystemManagementService.SystemName
- Msvm_VirtualSystemManagementService.CreationClassName
- Msvm_VirtualSystemManagementService.PrimaryOwnerName
- Msvm_VirtualSystemManagementService.PrimaryOwnerContact
- Msvm_VirtualSystemManagementService.StartMode
- Msvm_VirtualSystemManagementService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a0dab3dc9b530ca565e78ecc1f5a6e50a26bc3f630f5c60491b01c253e09aa97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147992"
---
# <a name="msvm_virtualsystemmanagementservice-class"></a>MSVM \_ VirtualSystemManagementService, classe

Représente le service de virtualisation présent sur un système hôte unique. **MSVM \_ VirtualSystemManagementService** est utilisé pour contrôler la définition, la modification et la suppression d’ordinateurs virtuels. Il comporte également des méthodes permettant d’effectuer des opérations sur des machines virtuelles, telles que le clonage, l’instantané et l’importation ou l’exportation d’ordinateurs virtuels. Pour récupérer les informations par ordinateur virtuel, utilisez [**MSVM \_ ComputerSystem**](msvm-computersystem.md).

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemManagementService : CIM_VirtualSystemManagementService
{
  string   InstanceID;
  string   Caption = "Virtual System Management Service";
  string   Description = "Service for creating, manipulating, and managing virtual machines";
  string   ElementName = "Hyper-V Virtual System Management Service";
  datetime InstallDate;
  string   Name = "vmms";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "The service is running normally" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_VirtualSystemManagementService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started = True;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ VirtualSystemManagementService** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **MSVM \_ VirtualSystemManagementService** possède ces méthodes.



| Méthode                                                                                                                 | Description                                                                                                                                                                                                                                        |
|:-----------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddBootSourceSettings**](msvm-virtualsystemmanagementservice-addbootsourcesettings.md)                             | Ajoute des sources de démarrage à une configuration de système virtuel lorsqu’elle est appliquée à une configuration de système virtuel « État ».<br/>                                                                                                                             |
| [**AddFeatureSettings**](addfeaturesettings-msvm-virtualsystemmanagementservice.md)                                   | Ajoute des paramètres de fonctionnalités Ethernet à la configuration d’une connexion Ethernet d’ordinateur virtuel.<br/>                                                                                                                                           |
| [**AddFibreChannelChap**](addfibrechannelchap-msvm-virtualsystemmanagementservice.md)                                 | Ajoute des paramètres DH-CHAP à un port de Fibre Channel synthétique dans un ordinateur virtuel.<br/>                                                                                                                                                         |
| [**AddGuestServiceSettings**](msvm-virtualsystemmanagementservice-addguestservicesettings.md)                         | Ajoute des paramètres de service invité à une configuration de système virtuel.<br/> En cas d’application à des parties d’une configuration de système virtuel « en cours », les services invités secondaires du système virtuel actif peuvent être modifiés.<br/>              |
| [**AddKvpItems**](addkvpitems-msvm-virtualsystemmanagementservice.md)                                                 | Ajoute des paires clé-valeur à un ordinateur virtuel.<br/>                                                                                                                                                                                              |
| [**AddResourceSettings**](addresourcesettings-msvm-virtualsystemmanagementservice.md)                                 | Ajoute des ressources à une configuration d’ordinateur virtuel.<br/>                                                                                                                                                                                      |
| [**AddSystemComponentSettings**](msvm-virtualsystemmanagementservice-addsystemcomponentsettings.md)                   | Ajoute des paramètres génériques à une configuration de système virtuel.<br/>                                                                                                                                                                                |
| [**DefinePlannedSystem**](msvm-virtualsystemmanagementservice-defineplannedsystem.md)                                 | Définit un système virtuel planifié.<br/> L’entrée qui n’est pas complètement spécifiée peut être remplie avec des valeurs par défaut.<br/>                                                                                                              |
| [**DefineSystem**](definesystem-msvm-virtualsystemmanagementservice.md)                                               | Crée une définition de machine virtuelle.<br/>                                                                                                                                                                                               |
| [**DestroySystem**](destroysystem-msvm-virtualsystemmanagementservice.md)                                             | Supprime une définition d’ordinateur virtuel existante.<br/>                                                                                                                                                                                         |
| [**DiagnoseNetworkConnection**](msvm-virtualsystemmanagementservice-diagnosenetworkconnection.md)                     | diagnostique la connectivité réseau d’une machine virtuelle dans un environnement de virtualisation de réseau Windows.<br/>                                                                                                                                             |
| [**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md)                           | Exporte un ordinateur virtuel, ou un instantané d’un ordinateur virtuel, vers un fichier.<br/>                                                                                                                                                               |
| [**FormatError**](formaterror-msvm-virtualsystemmanagementservice.md)                                                 | Retourne une chaîne de message d’erreur mise en forme pour le tableau spécifié d’instances d' [**\_ erreur MSVM**](msvm-error.md) incorporées.<br/>                                                                                                               |
| [**GenerateWwpn**](generatewwpn-msvm-virtualsystemmanagementservice.md)                                               | Génère un ensemble de noms WWPN (World World-of-Port).<br/>                                                                                                                                                                                       |
| [**GetCurrentWwpnFromGenerator**](getcurrentwwpnfromgenerator-msvm-virtualsystemmanagementservice.md)                 | Offre la possibilité de prévisualiser le nom WWPN (World-World Name Name) actuel sans que le WWPN soit réservé.<br/>                                                                                                                                |
| [**GetDefinitionFileSummaryInformation**](getdefinitionfilesummaryinformation-msvm-virtualsystemmanagementservice.md) | Retourne les informations de résumé de l’ordinateur virtuel pour les fichiers de définition d’ordinateur virtuel spécifiés.<br/>                                                                                                                                         |
| [**GetSizeOfSystemFiles**](getsizeofsystemfiles-msvm-virtualsystemmanagementservice.md)                               | Récupère la taille totale des fichiers système de l’ordinateur virtuel.<br/>                                                                                                                                                                        |
| [**GetSummaryInformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md)                             | Retourne les informations de résumé de la machine virtuelle.<br/>                                                                                                                                                                                            |
| [**GetVirtualSystemThumbnailImage**](getvirtualsystemthumbnailimage-msvm-virtualsystemmanagementservice.md)           | Récupère une image miniature d’une machine virtuelle existante.<br/>                                                                                                                                                                             |
| [**ImportSnapshotDefinitions**](importsnapshotdefinitions-msvm-virtualsystemmanagementservice.md)                     | Recherche dans le dossier spécifié les fichiers de définition d’instantané associés au système informatique planifié spécifié et crée un nouvel instantané sur le système informatique planifié pour chaque fichier de définition associé à cet emplacement.<br/> |
| [**ImportSystemDefinition**](importsystemdefinition-msvm-virtualsystemmanagementservice.md)                           | Crée un système informatique planifié basé sur la définition d’ordinateur virtuel spécifiée.<br/>                                                                                                                                                |
| [**ModifyDiskMergeSettings**](modifydiskmergesettings-msvm-virtualsystemmanagementservice.md)                         | Modifie les données de paramètre de fusion de disque.<br/>                                                                                                                                                                                                   |
| [**ModifyFeatureSettings**](modifyfeaturesettings-msvm-virtualsystemmanagementservice.md)                             | Modifie les paramètres de fonctionnalité actuels d’une connexion Ethernet d’ordinateur virtuel.<br/>                                                                                                                                                         |
| [**ModifyGuestServiceSettings**](msvm-virtualsystemmanagementservice-modifyguestservicesettings.md)                   | Modifie les paramètres du service invité.<br/> En cas d’application à des parties d’une configuration de système virtuel « en cours », les services invités secondaires du système virtuel actif peuvent être modifiés.<br/>                                            |
| [**ModifyKvpItems**](modifykvpitems-msvm-virtualsystemmanagementservice.md)                                           | Modifie des paires clé-valeur existantes sur un ordinateur virtuel.<br/>                                                                                                                                                                                 |
| [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md)                           | Modifie les paramètres de ressource virtuelle.<br/>                                                                                                                                                                                                     |
| [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)                             | Modifie les données de paramètre du service.<br/>                                                                                                                                                                                                    |
| [**ModifySystemComponentSettings**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md)             | Modifie les paramètres génériques des composants système.<br/>                                                                                                                                                                                             |
| [**ModifySystemSettings**](modifysystemsettings-msvm-virtualsystemmanagementservice.md)                               | Modifie les paramètres de l’ordinateur virtuel.<br/>                                                                                                                                                                                                      |
| [**RealizePlannedSystem**](realizeplannedsystem-msvm-virtualsystemmanagementservice.md)                               | Valide la configuration d’un ordinateur virtuel planifié et le convertit en ordinateur virtuel réalisé.<br/>                                                                                                                                 |
| [**RemoveBootSourceSettings**](msvm-virtualsystemmanagementservice-removebootsourcesettings.md)                       | Supprime les paramètres de ressources virtuelles d’une configuration de système virtuel.<br/> En cas d’application à des parties d’une configuration de système virtuel « en cours », les ressources d’effets secondaires du système virtuel actif peuvent être supprimées.<br/>            |
| [**RemoveFeatureSettings**](removefeaturesettings-msvm-virtualsystemmanagementservice.md)                             | Supprime les paramètres de fonctionnalité d’une connexion Ethernet d’ordinateur virtuel.<br/>                                                                                                                                                                    |
| [**RemoveFibreChannelChap**](removefibrechannelchap-msvm-virtualsystemmanagementservice.md)                           | Supprime les paramètres DH-CHAP d’un port de Fibre Channel synthétique dans un ordinateur virtuel.<br/>                                                                                                                                                    |
| [**RemoveGuestServiceSettings**](msvm-virtualsystemmanagementservice-removeguestservicesettings.md)                   | Supprime les paramètres de service invité d’une configuration de système virtuel.<br/> En cas d’application à des parties d’une configuration de système virtuel « en cours », les services invités secondaires du système virtuel actif peuvent être modifiés.<br/>         |
| [**RemoveKvpItems**](removekvpitems-msvm-virtualsystemmanagementservice.md)                                           | Supprime des paires clé-valeur existantes d’une machine virtuelle.<br/>                                                                                                                                                                                |
| [**RemoveResourceSettings**](removeresourcesettings-msvm-virtualsystemmanagementservice.md)                           | Supprime les paramètres de ressources virtuelles d’une configuration d’ordinateur virtuel.<br/>                                                                                                                                                                 |
| [**RemoveSystemComponentSettings**](msvm-virtualsystemmanagementservice-removesystemcomponentsettings.md)             | Supprime les paramètres de composant génériques d’une configuration de système virtuel.<br/>                                                                                                                                                                 |
| [**RequestStateChange**](msvm-virtualsystemmanagementservice-requeststatechange.md)                                   | Cette méthode n'est pas prise en charge.<br/>                                                                                                                                                                                                           |
| [**SetGuestNetworkAdapterConfiguration**](setguestnetworkadapterconfiguration-msvm-virtualsystemmanagementservice.md) | Configure les cartes réseau dans le système d’exploitation invité.<br/>                                                                                                                                                                      |
| [**SetInitialMachineConfigurationData**](msvm-virtualsystemmanagementservice-setinitialmachineconfigurationdata.md)   | Définit les données de configuration initiales de l’ordinateur d’une machine virtuelle.<br/>                                                                                                                                                                                         |
| [**StartService**](msvm-virtualsystemmanagementservice-startservice.md)                                               | Cette méthode n'est pas prise en charge.<br/>                                                                                                                                                                                                           |
| [**StopService**](msvm-virtualsystemmanagementservice-stopservice.md)                                                 | Cette méthode n'est pas prise en charge.<br/>                                                                                                                                                                                                           |
| [**TestNetworkConnection**](msvm-virtualsystemmanagementservice-testnetworkconnection.md)                             | teste la connectivité réseau d’une machine virtuelle dans un environnement de virtualisation de réseau Windows.<br/>                                                                                                                                                 |
| [**UpgradeSystemVersion**](msvm-virtualsystemmanagementservice-upgradesystemversion.md)                               | Met à niveau le système virtuel.<br/> En cas d’application aux paramètres système d’une configuration de système virtuel « en cours »<br/>                                                                                                                 |
| [**ValidatePlannedSystem**](validateplannedsystem-msvm-virtualsystemmanagementservice.md)                             | Valide le système planifié spécifié.<br/>                                                                                                                                                                                                 |



 

### <a name="properties"></a>Propriétés

La classe **MSVM \_ VirtualSystemManagementService** possède les propriétés suivantes.

<dl> <dt>

**AvailableRequestedStates**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique les valeurs possibles pour le paramètre *RequestedState* de la méthode **RequestStateChange** . Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Brève description de l’objet. Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « service de gestion du système virtuel Hyper-V ».

</dd> <dt>

**CommunicationStatus**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent. Une valeur **null** indique que cette propriété n’est pas implémentée. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)
</dt> <dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)
</dt> <dt>

<span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)
</dt> <dt>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Communication perdue** (3)
</dt> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Aucun contact** (4)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000.. )
</dt> </dl>

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **clé**, **MaxLen** (256)
</dt> </dl>

Nom de la classe ou de la sous-classe utilisée dans la création d’une instance. Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service)et est toujours définie sur « MSVM \_ VirtualSystemManagementService ».

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Description de l'objet . Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « service pour la création, la manipulation et la gestion des machines virtuelles ».

</dd> <dt>

**DetailedStatus**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires. Une valeur **null** indique que cette propriété n’est pas implémentée. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

<dl> <dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (0)
</dt> <dt>

<span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Aucune information supplémentaire** (1)
</dt> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Souligné** (2)
</dt> <dt>

<span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Défaillance prédictive** (3)
</dt> <dt>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erreur non récupérable** (4)
</dt> <dt>

<span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entité de prise en charge erronée** (5)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000.. )
</dt> </dl>

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom complet de l’objet. Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « service de gestion du système virtuel Hyper-V ».

</dd> <dt>

**EnabledDefault**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Configuration par défaut ou de démarrage d’un administrateur pour l’état activé d’un élément. Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur 2 (activé).



| Valeur                                                                        | Signification            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <dt>2</dt> </dl> | activé<br/> |



 

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

États activés et désactivés d’un élément. Cette propriété peut également indiquer les transitions entre ces États demandés. Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur 2 (activé).



| Valeur                                                                        | Signification            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <dt>2</dt> </dl> | activé<br/> |



 

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Intégrité actuelle de l’élément. Cet attribut exprime l’intégrité de cet élément, mais pas nécessairement celle de ses sous-composants. Les valeurs possibles sont comprises entre 0 et 30, où 5 signifie que l’élément est entièrement sain et 30 signifie que l’élément est complètement non opérationnel. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est toujours définie sur 5 (OK).



| Valeur                                                                        | Signification                                 |
|------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>5</dt> </dl> | L’état d’intégrité est normal.<br/> |



 

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

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **clé**, **MaxLen** (256)
</dt> </dl>

Étiquette par laquelle l’objet est connu. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est toujours définie sur « VMMS ».

</dd> <dt>

**OperatingStatus**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** . Une valeur **null** indique que cette propriété n’est pas implémentée. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)
</dt> <dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)
</dt> <dt>

<span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Maintenance** (2)
</dt> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Démarrage** (3)
</dt> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arrêt** (4)
</dt> <dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrêté** (5)
</dt> <dt>

<span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abandonné** (6)
</dt> <dt>

<span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)
</dt> <dt>

<span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Terminé** (8)
</dt> <dt>

<span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migration** (9)
</dt> <dt>

<span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)
</dt> <dt>

<span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Inmigration** (11)
</dt> <dt>

<span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Capture d’instantanés** (12)
</dt> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arrêt** (13)
</dt> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (14)
</dt> <dt>

<span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transition** (15)
</dt> <dt>

<span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En service** (16)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000.. )
</dt> </dl>

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

États actuels de l’objet. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), et chaque élément de tableau a toujours la valeur 2 (OK).

</dd> <dt>

**OtherEnabledState**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chaîne qui décrit l’état activé ou désactivé de l’élément lorsque la propriété **EnabledState** a la valeur 1 (« other »). Cette propriété doit avoir la valeur **null** quand **EnabledState** a une valeur autre que 1. Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.

</dd> <dt>

**PrimaryOwnerContact**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **MaxLen** (256)
</dt> </dl>

Toutes les informations relatives à la façon dont le propriétaire principal du service est accessible (par exemple, numéro de téléphone, adresse e-mail, etc.). Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service)et est toujours définie sur **null**.

</dd> <dt>

**PrimaryOwnerName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **MaxLen** (64)
</dt> </dl>

Nom du propriétaire principal du service, s’il est défini. Le propriétaire principal est le contact de support initial pour le service. Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service)et est toujours définie sur **null**.

</dd> <dt>

**PrimaryStatus**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Fournit des informations d’état de haut niveau. Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir un état d’intégrité élevé et détaillé de l’élément et de ses sous-composants. Une valeur **null** indique que cette propriété n’est pas implémentée. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)
</dt> <dt>

<span id="OK"></span><span id="ok"></span>**OK** (1)
</dt> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (2)
</dt> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erreur** (3)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000.. )
</dt> </dl>

</dd> <dt>

**RequestedState**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Dernier État demandé ou souhaité pour l’élément. L’état réel de l’élément est représenté par **EnabledState**. Cette propriété est fournie pour comparer les derniers États demandés et actuels d’un élément. Une instance particulière de la [**classe \_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)) peut ne pas prendre en charge la propriété **RequestedState** . Si cela se produit, la valeur 12 (« non applicable ») est utilisée. Cette propriété est héritée de la **\_ EnabledLogicalElement CIM** et est toujours définie sur 12 (non applicable).



| Valeur                                                                         | Signification                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>12</dt> </dl> | Non applicable.<br/> |



 

</dd> <dt>

**Démarré**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si le service est en cours d’exécution. Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service)et est toujours définie sur **true**.

</dd> <dt>

**StartMode**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **MaxLen** (10)
</dt> </dl>

Valeur de chaîne qui indique si le service est démarré automatiquement par un système, un système d’exploitation ou s’il est démarré uniquement sur demande. Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service)et est toujours définie sur **null**.

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
</dt> </dl>

Chaînes qui décrivent les différentes valeurs de tableau **OperationalStatus** . Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), et chaque élément de tableau a toujours la valeur « le service s’exécute normalement ».

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **clé**, **MaxLen** (256)
</dt> </dl>

Nom de la classe de création du système d’étendue. Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service)et est toujours définie sur « MSVM \_ ComputerSystem ».

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **clé**, **MaxLen** (256)
</dt> </dl>

Nom NetBIOS du système informatique d’hébergement. Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service).

</dd> <dt>

**TimeOfLastStateChange**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Date ou heure de la dernière modification de l’état activé de l’élément. Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).

</dd> <dt>

**TransitioningToState**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique l’État cible de la transition de l’instance. Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.

</dd> </dl>

## <a name="remarks"></a>Remarques

L’accès à la classe **MSVM \_ VirtualSystemManagementService** peut être limité par le filtrage UAC. Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**\_VIRTUALSYSTEMMANAGEMENTSERVICE CIM**](cim-virtualsystemmanagementservice.md)
</dt> <dt>

[**\_VIRTUALSYSTEMMANAGEMENTSERVICE CIM**](/previous-versions//cc136952(v=vs.85))
</dt> <dt>

[**MSVM \_ VirtualSystemManagementService (v1)**](/previous-versions/windows/desktop/legacy/cc136940(v=vs.85))
</dt> <dt>

[Classes de gestion du système virtuel](virtual-system-management-classes.md)
</dt> </dl>

 

