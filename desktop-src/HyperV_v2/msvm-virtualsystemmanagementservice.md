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
ms.openlocfilehash: 7ee79b9690f1eacdf7dc57a2ebfc2133091a1d55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750172"
---
# <a name="msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="eaf5c-103">MSVM \_ VirtualSystemManagementService, classe</span><span class="sxs-lookup"><span data-stu-id="eaf5c-103">Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="eaf5c-104">Représente le service de virtualisation présent sur un système hôte unique.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-104">Represents the virtualization service present on a single host system.</span></span> <span data-ttu-id="eaf5c-105">**MSVM \_ VirtualSystemManagementService** est utilisé pour contrôler la définition, la modification et la suppression d’ordinateurs virtuels.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-105">**Msvm\_VirtualSystemManagementService** is used to control the definition, modification, and deletion of virtual machines.</span></span> <span data-ttu-id="eaf5c-106">Il comporte également des méthodes permettant d’effectuer des opérations sur des machines virtuelles, telles que le clonage, l’instantané et l’importation ou l’exportation d’ordinateurs virtuels.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-106">It also has methods for performing operations on virtual machines, such as cloning, snapshotting, and the importing or exporting of virtual machines.</span></span> <span data-ttu-id="eaf5c-107">Pour récupérer les informations par ordinateur virtuel, utilisez [**MSVM \_ ComputerSystem**](msvm-computersystem.md).</span><span class="sxs-lookup"><span data-stu-id="eaf5c-107">To retrieve per-virtual machine information, use [**Msvm\_ComputerSystem**](msvm-computersystem.md).</span></span>

<span data-ttu-id="eaf5c-108">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="eaf5c-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eaf5c-109">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="eaf5c-110">Membres</span><span class="sxs-lookup"><span data-stu-id="eaf5c-110">Members</span></span>

<span data-ttu-id="eaf5c-111">La classe **MSVM \_ VirtualSystemManagementService** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="eaf5c-111">The **Msvm\_VirtualSystemManagementService** class has these types of members:</span></span>

-   [<span data-ttu-id="eaf5c-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="eaf5c-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="eaf5c-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="eaf5c-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="eaf5c-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="eaf5c-114">Methods</span></span>

<span data-ttu-id="eaf5c-115">La classe **MSVM \_ VirtualSystemManagementService** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-115">The **Msvm\_VirtualSystemManagementService** class has these methods.</span></span>



| <span data-ttu-id="eaf5c-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="eaf5c-116">Method</span></span>                                                                                                                 | <span data-ttu-id="eaf5c-117">Description</span><span class="sxs-lookup"><span data-stu-id="eaf5c-117">Description</span></span>                                                                                                                                                                                                                                        |
|:-----------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eaf5c-118">**AddBootSourceSettings**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-118">**AddBootSourceSettings**</span></span>](msvm-virtualsystemmanagementservice-addbootsourcesettings.md)                             | <span data-ttu-id="eaf5c-119">Ajoute des sources de démarrage à une configuration de système virtuel lorsqu’elle est appliquée à une configuration de système virtuel « État ».</span><span class="sxs-lookup"><span data-stu-id="eaf5c-119">Adds boot sources to a virtual system configuration when applied to a "state" virtual system configuration.</span></span><br/>                                                                                                                             |
| [<span data-ttu-id="eaf5c-120">**AddFeatureSettings**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-120">**AddFeatureSettings**</span></span>](addfeaturesettings-msvm-virtualsystemmanagementservice.md)                                   | <span data-ttu-id="eaf5c-121">Ajoute des paramètres de fonctionnalités Ethernet à la configuration d’une connexion Ethernet d’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-121">Adds Ethernet feature settings to the configuration of a virtual machine Ethernet connection.</span></span><br/>                                                                                                                                           |
| [<span data-ttu-id="eaf5c-122">**AddFibreChannelChap**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-122">**AddFibreChannelChap**</span></span>](addfibrechannelchap-msvm-virtualsystemmanagementservice.md)                                 | <span data-ttu-id="eaf5c-123">Ajoute des paramètres DH-CHAP à un port de Fibre Channel synthétique dans un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-123">Adds DH-CHAP parameters to a synthetic Fibre Channel port in a virtual machine.</span></span><br/>                                                                                                                                                         |
| [<span data-ttu-id="eaf5c-124">**AddGuestServiceSettings**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-124">**AddGuestServiceSettings**</span></span>](msvm-virtualsystemmanagementservice-addguestservicesettings.md)                         | <span data-ttu-id="eaf5c-125">Ajoute des paramètres de service invité à une configuration de système virtuel.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-125">Adds guest service settings to a virtual system configuration.</span></span><br/> <span data-ttu-id="eaf5c-126">En cas d’application à des parties d’une configuration de système virtuel « en cours », les services invités secondaires du système virtuel actif peuvent être modifiés.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-126">When applied to parts of a "current" virtual system configuration, as a side effect guest services of the active virtual system may be modified.</span></span><br/>              |
| [<span data-ttu-id="eaf5c-127">**AddKvpItems**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-127">**AddKvpItems**</span></span>](addkvpitems-msvm-virtualsystemmanagementservice.md)                                                 | <span data-ttu-id="eaf5c-128">Ajoute des paires clé-valeur à un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-128">Adds key-value pairs to a virtual machine.</span></span><br/>                                                                                                                                                                                              |
| [<span data-ttu-id="eaf5c-129">**AddResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-129">**AddResourceSettings**</span></span>](addresourcesettings-msvm-virtualsystemmanagementservice.md)                                 | <span data-ttu-id="eaf5c-130">Ajoute des ressources à une configuration d’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-130">Adds resources to a virtual machine configuration.</span></span><br/>                                                                                                                                                                                      |
| [<span data-ttu-id="eaf5c-131">**AddSystemComponentSettings**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-131">**AddSystemComponentSettings**</span></span>](msvm-virtualsystemmanagementservice-addsystemcomponentsettings.md)                   | <span data-ttu-id="eaf5c-132">Ajoute des paramètres génériques à une configuration de système virtuel.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-132">Adds generic settings to a virtual system configuration.</span></span><br/>                                                                                                                                                                                |
| [<span data-ttu-id="eaf5c-133">**DefinePlannedSystem**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-133">**DefinePlannedSystem**</span></span>](msvm-virtualsystemmanagementservice-defineplannedsystem.md)                                 | <span data-ttu-id="eaf5c-134">Définit un système virtuel planifié.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-134">Defines a planned virtual system.</span></span><br/> <span data-ttu-id="eaf5c-135">L’entrée qui n’est pas complètement spécifiée peut être remplie avec des valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-135">Input that is not completely specified may be filled out with default values.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="eaf5c-136">**DefineSystem**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-136">**DefineSystem**</span></span>](definesystem-msvm-virtualsystemmanagementservice.md)                                               | <span data-ttu-id="eaf5c-137">Crée une définition de machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-137">Creates a new virtual machine definition.</span></span><br/>                                                                                                                                                                                               |
| [<span data-ttu-id="eaf5c-138">**DestroySystem**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-138">**DestroySystem**</span></span>](destroysystem-msvm-virtualsystemmanagementservice.md)                                             | <span data-ttu-id="eaf5c-139">Supprime une définition d’ordinateur virtuel existante.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-139">Deletes an existing virtual machine definition.</span></span><br/>                                                                                                                                                                                         |
| [<span data-ttu-id="eaf5c-140">**DiagnoseNetworkConnection**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-140">**DiagnoseNetworkConnection**</span></span>](msvm-virtualsystemmanagementservice-diagnosenetworkconnection.md)                     | <span data-ttu-id="eaf5c-141">Diagnostique la connectivité réseau d’une machine virtuelle dans un environnement de virtualisation de réseau Windows.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-141">Diagnoses the network connectivity of a VM in a Windows Network Virtualization Environment.</span></span><br/>                                                                                                                                             |
| [<span data-ttu-id="eaf5c-142">**ExportSystemDefinition**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-142">**ExportSystemDefinition**</span></span>](exportsystemdefinition-msvm-virtualsystemmanagementservice.md)                           | <span data-ttu-id="eaf5c-143">Exporte un ordinateur virtuel, ou un instantané d’un ordinateur virtuel, vers un fichier.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-143">Exports a virtual machine, or a snapshot of a virtual machine, to a file.</span></span><br/>                                                                                                                                                               |
| [<span data-ttu-id="eaf5c-144">**FormatError**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-144">**FormatError**</span></span>](formaterror-msvm-virtualsystemmanagementservice.md)                                                 | <span data-ttu-id="eaf5c-145">Retourne une chaîne de message d’erreur mise en forme pour le tableau spécifié d’instances d' [**\_ erreur MSVM**](msvm-error.md) incorporées.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-145">Returns a formatted error message string for the specified array of embedded [**Msvm\_Error**](msvm-error.md) instances.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="eaf5c-146">**GenerateWwpn**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-146">**GenerateWwpn**</span></span>](generatewwpn-msvm-virtualsystemmanagementservice.md)                                               | <span data-ttu-id="eaf5c-147">Génère un ensemble de noms WWPN (World World-of-Port).</span><span class="sxs-lookup"><span data-stu-id="eaf5c-147">Generates a set of World Wide Port Names (WWPNs).</span></span><br/>                                                                                                                                                                                       |
| [<span data-ttu-id="eaf5c-148">**GetCurrentWwpnFromGenerator**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-148">**GetCurrentWwpnFromGenerator**</span></span>](getcurrentwwpnfromgenerator-msvm-virtualsystemmanagementservice.md)                 | <span data-ttu-id="eaf5c-149">Offre la possibilité de prévisualiser le nom WWPN (World-World Name Name) actuel sans que le WWPN soit réservé.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-149">Provides the ability to preview the current World Wide Port Name (WWPN) without the WWPN being reserved.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="eaf5c-150">**GetDefinitionFileSummaryInformation**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-150">**GetDefinitionFileSummaryInformation**</span></span>](getdefinitionfilesummaryinformation-msvm-virtualsystemmanagementservice.md) | <span data-ttu-id="eaf5c-151">Retourne les informations de résumé de l’ordinateur virtuel pour les fichiers de définition d’ordinateur virtuel spécifiés.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-151">Returns virtual machine summary information for the specified virtual machine definition files.</span></span><br/>                                                                                                                                         |
| [<span data-ttu-id="eaf5c-152">**GetSizeOfSystemFiles**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-152">**GetSizeOfSystemFiles**</span></span>](getsizeofsystemfiles-msvm-virtualsystemmanagementservice.md)                               | <span data-ttu-id="eaf5c-153">Récupère la taille totale des fichiers système de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-153">Retrieves the total size of the system files of virtual machine.</span></span><br/>                                                                                                                                                                        |
| [<span data-ttu-id="eaf5c-154">**GetSummaryInformation**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-154">**GetSummaryInformation**</span></span>](getsummaryinformation-msvm-virtualsystemmanagementservice.md)                             | <span data-ttu-id="eaf5c-155">Retourne les informations de résumé de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-155">Returns virtual machine summary information.</span></span><br/>                                                                                                                                                                                            |
| [<span data-ttu-id="eaf5c-156">**GetVirtualSystemThumbnailImage**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-156">**GetVirtualSystemThumbnailImage**</span></span>](getvirtualsystemthumbnailimage-msvm-virtualsystemmanagementservice.md)           | <span data-ttu-id="eaf5c-157">Récupère une image miniature d’une machine virtuelle existante.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-157">Retrieves a thumbnail image of an existing virtual machine.</span></span><br/>                                                                                                                                                                             |
| [<span data-ttu-id="eaf5c-158">**ImportSnapshotDefinitions**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-158">**ImportSnapshotDefinitions**</span></span>](importsnapshotdefinitions-msvm-virtualsystemmanagementservice.md)                     | <span data-ttu-id="eaf5c-159">Recherche dans le dossier spécifié les fichiers de définition d’instantané associés au système informatique planifié spécifié et crée un nouvel instantané sur le système informatique planifié pour chaque fichier de définition associé à cet emplacement.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-159">Searches the specified folder for any snapshot definition files associated with the specified planned computer system, and creates a new snapshot on the planned computer system for every associated definition file in this location.</span></span><br/> |
| [<span data-ttu-id="eaf5c-160">**ImportSystemDefinition**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-160">**ImportSystemDefinition**</span></span>](importsystemdefinition-msvm-virtualsystemmanagementservice.md)                           | <span data-ttu-id="eaf5c-161">Crée un système informatique planifié basé sur la définition d’ordinateur virtuel spécifiée.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-161">Creates a new planned computer system based on the specified virtual machine definition.</span></span><br/>                                                                                                                                                |
| [<span data-ttu-id="eaf5c-162">**ModifyDiskMergeSettings**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-162">**ModifyDiskMergeSettings**</span></span>](modifydiskmergesettings-msvm-virtualsystemmanagementservice.md)                         | <span data-ttu-id="eaf5c-163">Modifie les données de paramètre de fusion de disque.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-163">Modifies the disk merge setting data.</span></span><br/>                                                                                                                                                                                                   |
| [<span data-ttu-id="eaf5c-164">**ModifyFeatureSettings**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-164">**ModifyFeatureSettings**</span></span>](modifyfeaturesettings-msvm-virtualsystemmanagementservice.md)                             | <span data-ttu-id="eaf5c-165">Modifie les paramètres de fonctionnalité actuels d’une connexion Ethernet d’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-165">Modifies the current feature settings of a virtual machine Ethernet connection.</span></span><br/>                                                                                                                                                         |
| [<span data-ttu-id="eaf5c-166">**ModifyGuestServiceSettings**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-166">**ModifyGuestServiceSettings**</span></span>](msvm-virtualsystemmanagementservice-modifyguestservicesettings.md)                   | <span data-ttu-id="eaf5c-167">Modifie les paramètres du service invité.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-167">Modifies guest service settings.</span></span><br/> <span data-ttu-id="eaf5c-168">En cas d’application à des parties d’une configuration de système virtuel « en cours », les services invités secondaires du système virtuel actif peuvent être modifiés.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-168">When applied to parts of a "current" virtual system configuration, as a side effect guest services of the active virtual system may be modified.</span></span><br/>                                            |
| [<span data-ttu-id="eaf5c-169">**ModifyKvpItems**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-169">**ModifyKvpItems**</span></span>](modifykvpitems-msvm-virtualsystemmanagementservice.md)                                           | <span data-ttu-id="eaf5c-170">Modifie des paires clé-valeur existantes sur un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-170">Modifies existing key-value pairs on a virtual machine.</span></span><br/>                                                                                                                                                                                 |
| [<span data-ttu-id="eaf5c-171">**ModifyResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-171">**ModifyResourceSettings**</span></span>](modifyresourcesettings-msvm-virtualsystemmanagementservice.md)                           | <span data-ttu-id="eaf5c-172">Modifie les paramètres de ressource virtuelle.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-172">Modifies virtual resource settings.</span></span><br/>                                                                                                                                                                                                     |
| [<span data-ttu-id="eaf5c-173">**ModifyServiceSettings**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-173">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-virtualsystemmanagementservice.md)                             | <span data-ttu-id="eaf5c-174">Modifie les données de paramètre du service.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-174">Modifies the service's setting data.</span></span><br/>                                                                                                                                                                                                    |
| [<span data-ttu-id="eaf5c-175">**ModifySystemComponentSettings**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-175">**ModifySystemComponentSettings**</span></span>](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md)             | <span data-ttu-id="eaf5c-176">Modifie les paramètres génériques des composants système.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-176">Modifies generic system component settings.</span></span><br/>                                                                                                                                                                                             |
| [<span data-ttu-id="eaf5c-177">**ModifySystemSettings**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-177">**ModifySystemSettings**</span></span>](modifysystemsettings-msvm-virtualsystemmanagementservice.md)                               | <span data-ttu-id="eaf5c-178">Modifie les paramètres de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-178">Modifies virtual machine settings.</span></span><br/>                                                                                                                                                                                                      |
| [<span data-ttu-id="eaf5c-179">**RealizePlannedSystem**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-179">**RealizePlannedSystem**</span></span>](realizeplannedsystem-msvm-virtualsystemmanagementservice.md)                               | <span data-ttu-id="eaf5c-180">Valide la configuration d’un ordinateur virtuel planifié et le convertit en ordinateur virtuel réalisé.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-180">Validates the configuration of a planned virtual machine and converts it to a realized virtual machine.</span></span><br/>                                                                                                                                 |
| [<span data-ttu-id="eaf5c-181">**RemoveBootSourceSettings**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-181">**RemoveBootSourceSettings**</span></span>](msvm-virtualsystemmanagementservice-removebootsourcesettings.md)                       | <span data-ttu-id="eaf5c-182">Supprime les paramètres de ressources virtuelles d’une configuration de système virtuel.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-182">Removes virtual resource settings from a virtual system configuration.</span></span><br/> <span data-ttu-id="eaf5c-183">En cas d’application à des parties d’une configuration de système virtuel « en cours », les ressources d’effets secondaires du système virtuel actif peuvent être supprimées.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-183">When applied to parts of a "current" virtual system configuration, as a side effect resources of the active virtual system may be removed.</span></span><br/>            |
| [<span data-ttu-id="eaf5c-184">**RemoveFeatureSettings**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-184">**RemoveFeatureSettings**</span></span>](removefeaturesettings-msvm-virtualsystemmanagementservice.md)                             | <span data-ttu-id="eaf5c-185">Supprime les paramètres de fonctionnalité d’une connexion Ethernet d’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-185">Removes feature settings from a virtual machine Ethernet connection.</span></span><br/>                                                                                                                                                                    |
| [<span data-ttu-id="eaf5c-186">**RemoveFibreChannelChap**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-186">**RemoveFibreChannelChap**</span></span>](removefibrechannelchap-msvm-virtualsystemmanagementservice.md)                           | <span data-ttu-id="eaf5c-187">Supprime les paramètres DH-CHAP d’un port de Fibre Channel synthétique dans un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-187">Removes DH-CHAP parameters from a synthetic Fibre Channel port in a virtual machine.</span></span><br/>                                                                                                                                                    |
| [<span data-ttu-id="eaf5c-188">**RemoveGuestServiceSettings**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-188">**RemoveGuestServiceSettings**</span></span>](msvm-virtualsystemmanagementservice-removeguestservicesettings.md)                   | <span data-ttu-id="eaf5c-189">Supprime les paramètres de service invité d’une configuration de système virtuel.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-189">Removes guest service settings from a virtual system configuration.</span></span><br/> <span data-ttu-id="eaf5c-190">En cas d’application à des parties d’une configuration de système virtuel « en cours », les services invités secondaires du système virtuel actif peuvent être modifiés.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-190">When applied to parts of a "current" virtual system configuration, as a side effect guest services of the active virtual system may be modified.</span></span><br/>         |
| [<span data-ttu-id="eaf5c-191">**RemoveKvpItems**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-191">**RemoveKvpItems**</span></span>](removekvpitems-msvm-virtualsystemmanagementservice.md)                                           | <span data-ttu-id="eaf5c-192">Supprime des paires clé-valeur existantes d’une machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-192">Removes existing key-value pairs from a virtual machine.</span></span><br/>                                                                                                                                                                                |
| [<span data-ttu-id="eaf5c-193">**RemoveResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-193">**RemoveResourceSettings**</span></span>](removeresourcesettings-msvm-virtualsystemmanagementservice.md)                           | <span data-ttu-id="eaf5c-194">Supprime les paramètres de ressources virtuelles d’une configuration d’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-194">Removes virtual resource settings from a virtual machine configuration.</span></span><br/>                                                                                                                                                                 |
| [<span data-ttu-id="eaf5c-195">**RemoveSystemComponentSettings**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-195">**RemoveSystemComponentSettings**</span></span>](msvm-virtualsystemmanagementservice-removesystemcomponentsettings.md)             | <span data-ttu-id="eaf5c-196">Supprime les paramètres de composant génériques d’une configuration de système virtuel.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-196">Removes generic component settings from a virtual system configuration.</span></span><br/>                                                                                                                                                                 |
| [<span data-ttu-id="eaf5c-197">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-197">**RequestStateChange**</span></span>](msvm-virtualsystemmanagementservice-requeststatechange.md)                                   | <span data-ttu-id="eaf5c-198">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-198">This method is not supported.</span></span><br/>                                                                                                                                                                                                           |
| [<span data-ttu-id="eaf5c-199">**SetGuestNetworkAdapterConfiguration**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-199">**SetGuestNetworkAdapterConfiguration**</span></span>](setguestnetworkadapterconfiguration-msvm-virtualsystemmanagementservice.md) | <span data-ttu-id="eaf5c-200">Configure les cartes réseau dans le système d’exploitation invité.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-200">Configures the network adapters within the guest operating system.</span></span><br/>                                                                                                                                                                      |
| [<span data-ttu-id="eaf5c-201">**SetInitialMachineConfigurationData**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-201">**SetInitialMachineConfigurationData**</span></span>](msvm-virtualsystemmanagementservice-setinitialmachineconfigurationdata.md)   | <span data-ttu-id="eaf5c-202">Définit les données de configuration initiales de l’ordinateur d’une machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-202">Sets a VM's initial machine configuration data.</span></span><br/>                                                                                                                                                                                         |
| [<span data-ttu-id="eaf5c-203">**StartService**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-203">**StartService**</span></span>](msvm-virtualsystemmanagementservice-startservice.md)                                               | <span data-ttu-id="eaf5c-204">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-204">This method is not supported.</span></span><br/>                                                                                                                                                                                                           |
| [<span data-ttu-id="eaf5c-205">**StopService**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-205">**StopService**</span></span>](msvm-virtualsystemmanagementservice-stopservice.md)                                                 | <span data-ttu-id="eaf5c-206">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-206">This method is not supported.</span></span><br/>                                                                                                                                                                                                           |
| [<span data-ttu-id="eaf5c-207">**TestNetworkConnection**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-207">**TestNetworkConnection**</span></span>](msvm-virtualsystemmanagementservice-testnetworkconnection.md)                             | <span data-ttu-id="eaf5c-208">Teste la connectivité réseau d’une machine virtuelle dans un environnement de virtualisation de réseau Windows.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-208">Tests the network connectivity of a VM in a Windows Network Virtualization Environment.</span></span><br/>                                                                                                                                                 |
| [<span data-ttu-id="eaf5c-209">**UpgradeSystemVersion**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-209">**UpgradeSystemVersion**</span></span>](msvm-virtualsystemmanagementservice-upgradesystemversion.md)                               | <span data-ttu-id="eaf5c-210">Met à niveau le système virtuel.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-210">Upgrades the virtual system.</span></span><br/> <span data-ttu-id="eaf5c-211">En cas d’application aux paramètres système d’une configuration de système virtuel « en cours »</span><span class="sxs-lookup"><span data-stu-id="eaf5c-211">When applied to the system settings of a "current" virtual system configuration</span></span><br/>                                                                                                                 |
| [<span data-ttu-id="eaf5c-212">**ValidatePlannedSystem**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-212">**ValidatePlannedSystem**</span></span>](validateplannedsystem-msvm-virtualsystemmanagementservice.md)                             | <span data-ttu-id="eaf5c-213">Valide le système planifié spécifié.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-213">Validates the specified planned system.</span></span><br/>                                                                                                                                                                                                 |



 

### <a name="properties"></a><span data-ttu-id="eaf5c-214">Propriétés</span><span class="sxs-lookup"><span data-stu-id="eaf5c-214">Properties</span></span>

<span data-ttu-id="eaf5c-215">La classe **MSVM \_ VirtualSystemManagementService** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-215">The **Msvm\_VirtualSystemManagementService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="eaf5c-216">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-216">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaf5c-217">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-217">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-218">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eaf5c-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eaf5c-219">Indique les valeurs possibles pour le paramètre *RequestedState* de la méthode **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="eaf5c-219">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="eaf5c-220">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-220">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="eaf5c-221">**Caption**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-221">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaf5c-222">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-223">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eaf5c-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eaf5c-224">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-224">A short description of the object.</span></span> <span data-ttu-id="eaf5c-225">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « service de gestion du système virtuel Hyper-V ».</span><span class="sxs-lookup"><span data-stu-id="eaf5c-225">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Virtual System Management Service".</span></span>

</dd> <dt>

<span data-ttu-id="eaf5c-226">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-226">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaf5c-227">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-227">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-228">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eaf5c-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eaf5c-229">Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-229">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="eaf5c-230">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-230">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="eaf5c-231">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="eaf5c-231">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="eaf5c-232"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="eaf5c-232"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-233"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="eaf5c-233"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-234"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span><span class="sxs-lookup"><span data-stu-id="eaf5c-234"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-235"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Communication perdue** (3)</span><span class="sxs-lookup"><span data-stu-id="eaf5c-235"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-236"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Aucun contact** (4)</span><span class="sxs-lookup"><span data-stu-id="eaf5c-236"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-237"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="eaf5c-237"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-238"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="eaf5c-238"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="eaf5c-239">)</span><span class="sxs-lookup"><span data-stu-id="eaf5c-239">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="eaf5c-240">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-240">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaf5c-241">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-242">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eaf5c-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-243">Qualificateurs : **clé**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="eaf5c-243">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="eaf5c-244">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-244">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="eaf5c-245">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service)et est toujours définie sur « MSVM \_ VirtualSystemManagementService ».</span><span class="sxs-lookup"><span data-stu-id="eaf5c-245">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_VirtualSystemManagementService".</span></span>

</dd> <dt>

<span data-ttu-id="eaf5c-246">**Description**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-246">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaf5c-247">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-248">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eaf5c-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eaf5c-249">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="eaf5c-249">A description of the object.</span></span> <span data-ttu-id="eaf5c-250">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « service pour la création, la manipulation et la gestion des machines virtuelles ».</span><span class="sxs-lookup"><span data-stu-id="eaf5c-250">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Service for creating, manipulating, and managing virtual machines".</span></span>

</dd> <dt>

<span data-ttu-id="eaf5c-251">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-251">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaf5c-252">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-252">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-253">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eaf5c-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eaf5c-254">Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-254">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="eaf5c-255">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-255">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="eaf5c-256">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="eaf5c-256">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="eaf5c-257"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="eaf5c-257"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-258"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Aucune information supplémentaire** (1)</span><span class="sxs-lookup"><span data-stu-id="eaf5c-258"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-259"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Souligné** (2)</span><span class="sxs-lookup"><span data-stu-id="eaf5c-259"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-260"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Défaillance prédictive** (3)</span><span class="sxs-lookup"><span data-stu-id="eaf5c-260"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-261"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erreur non récupérable** (4)</span><span class="sxs-lookup"><span data-stu-id="eaf5c-261"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-262"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entité de prise en charge erronée** (5)</span><span class="sxs-lookup"><span data-stu-id="eaf5c-262"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-263"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="eaf5c-263"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-264"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="eaf5c-264"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="eaf5c-265">)</span><span class="sxs-lookup"><span data-stu-id="eaf5c-265">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="eaf5c-266">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-266">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaf5c-267">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-268">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eaf5c-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eaf5c-269">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-269">A display name for the object.</span></span> <span data-ttu-id="eaf5c-270">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « service de gestion du système virtuel Hyper-V ».</span><span class="sxs-lookup"><span data-stu-id="eaf5c-270">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Virtual System Management Service".</span></span>

</dd> <dt>

<span data-ttu-id="eaf5c-271">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-271">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaf5c-272">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-272">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-273">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eaf5c-273">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eaf5c-274">Configuration par défaut ou de démarrage d’un administrateur pour l’état activé d’un élément.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-274">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="eaf5c-275">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur 2 (activé).</span><span class="sxs-lookup"><span data-stu-id="eaf5c-275">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="eaf5c-276">Valeur</span><span class="sxs-lookup"><span data-stu-id="eaf5c-276">Value</span></span>                                                                        | <span data-ttu-id="eaf5c-277">Signification</span><span class="sxs-lookup"><span data-stu-id="eaf5c-277">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="eaf5c-278"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="eaf5c-278"><dt>2</dt></span></span> </dl> | <span data-ttu-id="eaf5c-279">activé</span><span class="sxs-lookup"><span data-stu-id="eaf5c-279">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="eaf5c-280">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-280">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaf5c-281">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-281">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-282">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eaf5c-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eaf5c-283">États activés et désactivés d’un élément.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-283">The enabled and disabled states of an element.</span></span> <span data-ttu-id="eaf5c-284">Cette propriété peut également indiquer les transitions entre ces États demandés.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-284">This property can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="eaf5c-285">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur 2 (activé).</span><span class="sxs-lookup"><span data-stu-id="eaf5c-285">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="eaf5c-286">Valeur</span><span class="sxs-lookup"><span data-stu-id="eaf5c-286">Value</span></span>                                                                        | <span data-ttu-id="eaf5c-287">Signification</span><span class="sxs-lookup"><span data-stu-id="eaf5c-287">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="eaf5c-288"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="eaf5c-288"><dt>2</dt></span></span> </dl> | <span data-ttu-id="eaf5c-289">activé</span><span class="sxs-lookup"><span data-stu-id="eaf5c-289">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="eaf5c-290">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-290">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaf5c-291">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-291">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-292">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eaf5c-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eaf5c-293">Intégrité actuelle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-293">The current health of the element.</span></span> <span data-ttu-id="eaf5c-294">Cet attribut exprime l’intégrité de cet élément, mais pas nécessairement celle de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-294">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="eaf5c-295">Les valeurs possibles sont comprises entre 0 et 30, où 5 signifie que l’élément est entièrement sain et 30 signifie que l’élément est complètement non opérationnel.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-295">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="eaf5c-296">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est toujours définie sur 5 (OK).</span><span class="sxs-lookup"><span data-stu-id="eaf5c-296">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>



| <span data-ttu-id="eaf5c-297">Valeur</span><span class="sxs-lookup"><span data-stu-id="eaf5c-297">Value</span></span>                                                                        | <span data-ttu-id="eaf5c-298">Signification</span><span class="sxs-lookup"><span data-stu-id="eaf5c-298">Meaning</span></span>                                 |
|------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="eaf5c-299"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="eaf5c-299"><dt>5</dt></span></span> </dl> | <span data-ttu-id="eaf5c-300">L’état d’intégrité est normal.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-300">The health status is normal.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="eaf5c-301">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-301">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaf5c-302">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-302">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-303">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eaf5c-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eaf5c-304">Date et heure de création de la configuration de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-304">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="eaf5c-305">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="eaf5c-305">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="eaf5c-306">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-306">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaf5c-307">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-308">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eaf5c-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-309">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-309">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="eaf5c-310">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-310">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="eaf5c-311">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="eaf5c-311">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="eaf5c-312">**Nom**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-312">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaf5c-313">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-314">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eaf5c-314">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-315">Qualificateurs : **clé**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="eaf5c-315">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="eaf5c-316">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-316">The label by which the object is known.</span></span> <span data-ttu-id="eaf5c-317">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est toujours définie sur « VMMS ».</span><span class="sxs-lookup"><span data-stu-id="eaf5c-317">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "vmms".</span></span>

</dd> <dt>

<span data-ttu-id="eaf5c-318">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-318">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaf5c-319">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-319">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-320">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eaf5c-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eaf5c-321">Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="eaf5c-321">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="eaf5c-322">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-322">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="eaf5c-323">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="eaf5c-323">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="eaf5c-324"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="eaf5c-324"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-325"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="eaf5c-325"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-326"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Maintenance** (2)</span><span class="sxs-lookup"><span data-stu-id="eaf5c-326"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-327"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Démarrage** (3)</span><span class="sxs-lookup"><span data-stu-id="eaf5c-327"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-328"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arrêt** (4)</span><span class="sxs-lookup"><span data-stu-id="eaf5c-328"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-329"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrêté** (5)</span><span class="sxs-lookup"><span data-stu-id="eaf5c-329"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-330"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abandonné** (6)</span><span class="sxs-lookup"><span data-stu-id="eaf5c-330"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-331"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span><span class="sxs-lookup"><span data-stu-id="eaf5c-331"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-332"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Terminé** (8)</span><span class="sxs-lookup"><span data-stu-id="eaf5c-332"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-333"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migration** (9)</span><span class="sxs-lookup"><span data-stu-id="eaf5c-333"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-334"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="eaf5c-334"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-335"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Inmigration** (11)</span><span class="sxs-lookup"><span data-stu-id="eaf5c-335"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-336"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Capture d’instantanés** (12)</span><span class="sxs-lookup"><span data-stu-id="eaf5c-336"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-337"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arrêt** (13)</span><span class="sxs-lookup"><span data-stu-id="eaf5c-337"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-338"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (14)</span><span class="sxs-lookup"><span data-stu-id="eaf5c-338"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-339"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transition** (15)</span><span class="sxs-lookup"><span data-stu-id="eaf5c-339"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-340"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En service** (16)</span><span class="sxs-lookup"><span data-stu-id="eaf5c-340"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-341"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="eaf5c-341"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-342"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="eaf5c-342"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="eaf5c-343">)</span><span class="sxs-lookup"><span data-stu-id="eaf5c-343">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="eaf5c-344">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-344">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaf5c-345">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-345">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-346">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eaf5c-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eaf5c-347">États actuels de l’objet.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-347">The current statuses of the object.</span></span> <span data-ttu-id="eaf5c-348">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), et chaque élément de tableau a toujours la valeur 2 (OK).</span><span class="sxs-lookup"><span data-stu-id="eaf5c-348">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="eaf5c-349">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-349">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaf5c-350">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-350">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-351">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eaf5c-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eaf5c-352">Chaîne qui décrit l’état activé ou désactivé de l’élément lorsque la propriété **EnabledState** a la valeur 1 (« other »).</span><span class="sxs-lookup"><span data-stu-id="eaf5c-352">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="eaf5c-353">Cette propriété doit avoir la valeur **null** quand **EnabledState** a une valeur autre que 1.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-353">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="eaf5c-354">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-354">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="eaf5c-355">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-355">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaf5c-356">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-356">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-357">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eaf5c-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-358">Qualificateurs : **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="eaf5c-358">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="eaf5c-359">Toutes les informations relatives à la façon dont le propriétaire principal du service est accessible (par exemple, numéro de téléphone, adresse e-mail, etc.).</span><span class="sxs-lookup"><span data-stu-id="eaf5c-359">Any information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="eaf5c-360">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-360">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="eaf5c-361">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-361">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaf5c-362">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-362">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-363">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eaf5c-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-364">Qualificateurs : **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="eaf5c-364">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="eaf5c-365">Nom du propriétaire principal du service, s’il est défini.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-365">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="eaf5c-366">Le propriétaire principal est le contact de support initial pour le service.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-366">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="eaf5c-367">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-367">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="eaf5c-368">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-368">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaf5c-369">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-369">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-370">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eaf5c-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eaf5c-371">Fournit des informations d’état de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-371">Provides high level status information.</span></span> <span data-ttu-id="eaf5c-372">Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir un état d’intégrité élevé et détaillé de l’élément et de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-372">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="eaf5c-373">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-373">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="eaf5c-374">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="eaf5c-374">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="eaf5c-375"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="eaf5c-375"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-376"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="eaf5c-376"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-377"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (2)</span><span class="sxs-lookup"><span data-stu-id="eaf5c-377"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-378"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erreur** (3)</span><span class="sxs-lookup"><span data-stu-id="eaf5c-378"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-379"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="eaf5c-379"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-380"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="eaf5c-380"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="eaf5c-381">)</span><span class="sxs-lookup"><span data-stu-id="eaf5c-381">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="eaf5c-382">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-382">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaf5c-383">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-383">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-384">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eaf5c-384">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eaf5c-385">Dernier État demandé ou souhaité pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-385">The last requested or desired state for the element.</span></span> <span data-ttu-id="eaf5c-386">L’état réel de l’élément est représenté par **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-386">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="eaf5c-387">Cette propriété est fournie pour comparer les derniers États demandés et actuels d’un élément.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-387">This property is provided to compare the last requested and current states for an element.</span></span> <span data-ttu-id="eaf5c-388">Une instance particulière de la [**classe \_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)) peut ne pas prendre en charge la propriété **RequestedState** .</span><span class="sxs-lookup"><span data-stu-id="eaf5c-388">A particular instance of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) class might not support the **RequestedState** property.</span></span> <span data-ttu-id="eaf5c-389">Si cela se produit, la valeur 12 (« non applicable ») est utilisée.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-389">If this occurs, the value 12 ("Not Applicable") is used.</span></span> <span data-ttu-id="eaf5c-390">Cette propriété est héritée de la **\_ EnabledLogicalElement CIM** et est toujours définie sur 12 (non applicable).</span><span class="sxs-lookup"><span data-stu-id="eaf5c-390">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 12 (Not Applicable).</span></span>



| <span data-ttu-id="eaf5c-391">Valeur</span><span class="sxs-lookup"><span data-stu-id="eaf5c-391">Value</span></span>                                                                         | <span data-ttu-id="eaf5c-392">Signification</span><span class="sxs-lookup"><span data-stu-id="eaf5c-392">Meaning</span></span>                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="eaf5c-393"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="eaf5c-393"><dt>12</dt></span></span> </dl> | <span data-ttu-id="eaf5c-394">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-394">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="eaf5c-395">**Cours**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-395">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaf5c-396">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-396">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-397">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eaf5c-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eaf5c-398">Indique si le service est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-398">Indicates whether the service is currently running.</span></span> <span data-ttu-id="eaf5c-399">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service)et est toujours définie sur **true**.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-399">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="eaf5c-400">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-400">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaf5c-401">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-401">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-402">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eaf5c-402">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-403">Qualificateurs : **MaxLen** (10)</span><span class="sxs-lookup"><span data-stu-id="eaf5c-403">Qualifiers: **MaxLen** ( 10 )</span></span>
</dt> </dl>

<span data-ttu-id="eaf5c-404">Valeur de chaîne qui indique si le service est démarré automatiquement par un système, un système d’exploitation ou s’il est démarré uniquement sur demande.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-404">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="eaf5c-405">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-405">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="eaf5c-406">**État**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-406">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaf5c-407">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-407">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-408">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eaf5c-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eaf5c-409">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-409">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="eaf5c-410">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-410">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaf5c-411">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-411">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-412">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eaf5c-412">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eaf5c-413">Chaînes qui décrivent les différentes valeurs de tableau **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="eaf5c-413">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="eaf5c-414">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), et chaque élément de tableau a toujours la valeur « le service s’exécute normalement ».</span><span class="sxs-lookup"><span data-stu-id="eaf5c-414">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "The service is running normally".</span></span>

</dd> <dt>

<span data-ttu-id="eaf5c-415">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-415">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaf5c-416">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-416">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-417">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eaf5c-417">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-418">Qualificateurs : **clé**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="eaf5c-418">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="eaf5c-419">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-419">The scoping system's creation class name.</span></span> <span data-ttu-id="eaf5c-420">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service)et est toujours définie sur « MSVM \_ ComputerSystem ».</span><span class="sxs-lookup"><span data-stu-id="eaf5c-420">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="eaf5c-421">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-421">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaf5c-422">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-422">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-423">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eaf5c-423">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-424">Qualificateurs : **clé**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="eaf5c-424">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="eaf5c-425">Nom NetBIOS du système informatique d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-425">The NetBIOS name of the hosting computer system.</span></span> <span data-ttu-id="eaf5c-426">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="eaf5c-426">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="eaf5c-427">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-427">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaf5c-428">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-428">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-429">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eaf5c-429">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eaf5c-430">Date ou heure de la dernière modification de l’état activé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-430">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="eaf5c-431">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="eaf5c-431">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="eaf5c-432">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-432">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaf5c-433">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-433">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-434">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eaf5c-434">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eaf5c-435">Indique l’État cible de la transition de l’instance.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-435">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="eaf5c-436">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-436">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eaf5c-437">Notes</span><span class="sxs-lookup"><span data-stu-id="eaf5c-437">Remarks</span></span>

<span data-ttu-id="eaf5c-438">L’accès à la classe **MSVM \_ VirtualSystemManagementService** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="eaf5c-438">Access to the **Msvm\_VirtualSystemManagementService** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="eaf5c-439">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="eaf5c-439">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="eaf5c-440">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eaf5c-440">Requirements</span></span>



| <span data-ttu-id="eaf5c-441">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eaf5c-441">Requirement</span></span> | <span data-ttu-id="eaf5c-442">Valeur</span><span class="sxs-lookup"><span data-stu-id="eaf5c-442">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eaf5c-443">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eaf5c-443">Minimum supported client</span></span><br/> | <span data-ttu-id="eaf5c-444">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eaf5c-444">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="eaf5c-445">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eaf5c-445">Minimum supported server</span></span><br/> | <span data-ttu-id="eaf5c-446">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eaf5c-446">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="eaf5c-447">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="eaf5c-447">Namespace</span></span><br/>                | <span data-ttu-id="eaf5c-448">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="eaf5c-448">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="eaf5c-449">MOF</span><span class="sxs-lookup"><span data-stu-id="eaf5c-449">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eaf5c-450"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eaf5c-450"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="eaf5c-451">DLL</span><span class="sxs-lookup"><span data-stu-id="eaf5c-451">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eaf5c-452"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="eaf5c-452"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="eaf5c-453">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eaf5c-453">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eaf5c-454">**\_VIRTUALSYSTEMMANAGEMENTSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="eaf5c-454">**CIM\_VirtualSystemManagementService**</span></span>](cim-virtualsystemmanagementservice.md)
</dt> <dt>

<span data-ttu-id="eaf5c-455">[**\_VIRTUALSYSTEMMANAGEMENTSERVICE CIM**](/previous-versions//cc136952(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="eaf5c-455">[**CIM\_VirtualSystemManagementService**](/previous-versions//cc136952(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="eaf5c-456">[**MSVM \_ VirtualSystemManagementService (v1)**](/previous-versions/windows/desktop/legacy/cc136940(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="eaf5c-456">[**Msvm\_VirtualSystemManagementService (V1)**](/previous-versions/windows/desktop/legacy/cc136940(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="eaf5c-457">Classes de gestion du système virtuel</span><span class="sxs-lookup"><span data-stu-id="eaf5c-457">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> </dl>

 

