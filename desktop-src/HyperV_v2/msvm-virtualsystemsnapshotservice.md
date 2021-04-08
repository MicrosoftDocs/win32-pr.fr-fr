---
description: Service pour créer, appliquer et détruire des instantanés d’ordinateurs virtuels.
ms.assetid: 34efe124-d198-4bad-a3c9-e8457a5faa5e
title: Classe Msvm_VirtualSystemSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotService
- Msvm_VirtualSystemSnapshotService.StartService
- Msvm_VirtualSystemSnapshotService.StopService
- Msvm_VirtualSystemSnapshotService.InstanceID
- Msvm_VirtualSystemSnapshotService.Caption
- Msvm_VirtualSystemSnapshotService.Description
- Msvm_VirtualSystemSnapshotService.ElementName
- Msvm_VirtualSystemSnapshotService.InstallDate
- Msvm_VirtualSystemSnapshotService.Name
- Msvm_VirtualSystemSnapshotService.OperationalStatus
- Msvm_VirtualSystemSnapshotService.StatusDescriptions
- Msvm_VirtualSystemSnapshotService.Status
- Msvm_VirtualSystemSnapshotService.HealthState
- Msvm_VirtualSystemSnapshotService.CommunicationStatus
- Msvm_VirtualSystemSnapshotService.DetailedStatus
- Msvm_VirtualSystemSnapshotService.OperatingStatus
- Msvm_VirtualSystemSnapshotService.PrimaryStatus
- Msvm_VirtualSystemSnapshotService.EnabledState
- Msvm_VirtualSystemSnapshotService.OtherEnabledState
- Msvm_VirtualSystemSnapshotService.RequestedState
- Msvm_VirtualSystemSnapshotService.EnabledDefault
- Msvm_VirtualSystemSnapshotService.TimeOfLastStateChange
- Msvm_VirtualSystemSnapshotService.AvailableRequestedStates
- Msvm_VirtualSystemSnapshotService.TransitioningToState
- Msvm_VirtualSystemSnapshotService.SystemCreationClassName
- Msvm_VirtualSystemSnapshotService.SystemName
- Msvm_VirtualSystemSnapshotService.CreationClassName
- Msvm_VirtualSystemSnapshotService.PrimaryOwnerName
- Msvm_VirtualSystemSnapshotService.PrimaryOwnerContact
- Msvm_VirtualSystemSnapshotService.StartMode
- Msvm_VirtualSystemSnapshotService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: be84d70dd9478012e747626a9a566464d7587789
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862050"
---
# <a name="msvm_virtualsystemsnapshotservice-class"></a><span data-ttu-id="d4dee-103">MSVM \_ VirtualSystemSnapshotService, classe</span><span class="sxs-lookup"><span data-stu-id="d4dee-103">Msvm\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="d4dee-104">Service pour créer, appliquer et détruire des instantanés d’ordinateurs virtuels.</span><span class="sxs-lookup"><span data-stu-id="d4dee-104">Service to create, apply, and destroy snapshots of virtual machines.</span></span>

<span data-ttu-id="d4dee-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="d4dee-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4dee-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d4dee-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemSnapshotService : CIM_VirtualSystemSnapshotService
{
  string   InstanceID;
  string   Caption = "Hyper-V Virtual System Snapshot Service";
  string   Description = "Service for creating, destroying, and applying virtual machine snapshots";
  string   ElementName;
  datetime InstallDate;
  string   Name = "vssnapsvc";
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
  uint16   TransitioningToState = 12;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_VirtualSystemSnapshotService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started = True;
};
```

## <a name="members"></a><span data-ttu-id="d4dee-107">Membres</span><span class="sxs-lookup"><span data-stu-id="d4dee-107">Members</span></span>

<span data-ttu-id="d4dee-108">La classe **MSVM \_ VirtualSystemSnapshotService** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d4dee-108">The **Msvm\_VirtualSystemSnapshotService** class has these types of members:</span></span>

-   [<span data-ttu-id="d4dee-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d4dee-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="d4dee-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d4dee-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d4dee-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d4dee-111">Methods</span></span>

<span data-ttu-id="d4dee-112">La classe **MSVM \_ VirtualSystemSnapshotService** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="d4dee-112">The **Msvm\_VirtualSystemSnapshotService** class has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="d4dee-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="d4dee-113">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="d4dee-114">Description</span><span class="sxs-lookup"><span data-stu-id="d4dee-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="d4dee-115"><a href="applysnapshot-msvm-virtualsystemsnapshotservice.md"><strong>ApplySnapshot</strong></a></span><span class="sxs-lookup"><span data-stu-id="d4dee-115"><a href="applysnapshot-msvm-virtualsystemsnapshotservice.md"><strong>ApplySnapshot</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="d4dee-116">Applique un instantané d’ordinateur virtuel à la machine virtuelle à partir de laquelle il a été créé.</span><span class="sxs-lookup"><span data-stu-id="d4dee-116">Applies a virtual machine snapshot to the virtual machine that it was created from.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="d4dee-117"><a href="clearsnapshotstate-msvm-virtualsystemsnapshotservice.md"><strong>ClearSnapshotState</strong></a></span><span class="sxs-lookup"><span data-stu-id="d4dee-117"><a href="clearsnapshotstate-msvm-virtualsystemsnapshotservice.md"><strong>ClearSnapshotState</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="d4dee-118">Efface l’état de l’enregistrement d’un instantané existant.</span><span class="sxs-lookup"><span data-stu-id="d4dee-118">Clears save state from an existing snapshot.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="d4dee-119"><a href="msvm-virtualsystemsnapshotservice-converttoreferencepoint.md"><strong>ConvertToReferencePoint</strong></a></span><span class="sxs-lookup"><span data-stu-id="d4dee-119"><a href="msvm-virtualsystemsnapshotservice-converttoreferencepoint.md"><strong>ConvertToReferencePoint</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="d4dee-120">Convertit un instantané de système virtuel existant en un point de référence.</span><span class="sxs-lookup"><span data-stu-id="d4dee-120">Convert an existing virtual system snapshot to a reference point.</span></span> <span data-ttu-id="d4dee-121">L’instantané est supprimé comme un effet secondaire.</span><span class="sxs-lookup"><span data-stu-id="d4dee-121">The snapshot gets deleted as a side effect.</span></span> <span data-ttu-id="d4dee-122">Seuls les instantanés de récupération peuvent être convertis en points de référence.</span><span class="sxs-lookup"><span data-stu-id="d4dee-122">Only recovery snapshots can be converted to reference points.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="d4dee-123">La prise en charge de cette méthode a été ajoutée dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="d4dee-123">Support for this method was added in Windows 10.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="d4dee-124"><a href="createsnapshot-msvm-virtualsystemsnapshotservice.md"><strong>CreateSnapshot</strong></a></span><span class="sxs-lookup"><span data-stu-id="d4dee-124"><a href="createsnapshot-msvm-virtualsystemsnapshotservice.md"><strong>CreateSnapshot</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="d4dee-125">Crée une capture instantanée d’un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="d4dee-125">Creates a snapshot of a virtual machine.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="d4dee-126"><a href="destroysnapshot-msvm-virtualsystemsnapshotservice.md"><strong>DestroySnapshot</strong></a></span><span class="sxs-lookup"><span data-stu-id="d4dee-126"><a href="destroysnapshot-msvm-virtualsystemsnapshotservice.md"><strong>DestroySnapshot</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="d4dee-127">Détruisez un instantané de machine virtuelle existant.</span><span class="sxs-lookup"><span data-stu-id="d4dee-127">Destroy an existing virtual machine snapshot.</span></span> <span data-ttu-id="d4dee-128">Cette méthode peut, en tant qu’effet secondaire, détruire d’autres instantanés qui sont dépendants de l’instantané affecté.</span><span class="sxs-lookup"><span data-stu-id="d4dee-128">This method may, as a side effect, destroy other snapshots that are dependent on the affected snapshot.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="d4dee-129"><a href="destroysnapshottree-msvm-virtualsystemsnapshotservice.md"><strong>DestroySnapshotTree</strong></a></span><span class="sxs-lookup"><span data-stu-id="d4dee-129"><a href="destroysnapshottree-msvm-virtualsystemsnapshotservice.md"><strong>DestroySnapshotTree</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="d4dee-130">Supprime un instantané existant, ainsi que tous ses enfants, d’un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="d4dee-130">Removes an existing snapshot, and all its children, of a virtual machine.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="d4dee-131"><a href="msvm-virtualsystemsnapshotservice-requeststatechange.md"><strong>RequestStateChange</strong></a></span><span class="sxs-lookup"><span data-stu-id="d4dee-131"><a href="msvm-virtualsystemsnapshotservice-requeststatechange.md"><strong>RequestStateChange</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="d4dee-132">Demande un changement d’État pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="d4dee-132">Requests a state change for the element.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="d4dee-133">La prise en charge de cette méthode a été ajoutée dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="d4dee-133">Support for this method was added in Windows 10.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="d4dee-134"><strong>StartService</strong></span><span class="sxs-lookup"><span data-stu-id="d4dee-134"><strong>StartService</strong></span></span></td>
<td style="text-align: left;"><span data-ttu-id="d4dee-135">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="d4dee-135">This method is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="d4dee-136"><strong>StopService</strong></span><span class="sxs-lookup"><span data-stu-id="d4dee-136"><strong>StopService</strong></span></span></td>
<td style="text-align: left;"><span data-ttu-id="d4dee-137">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="d4dee-137">This method is not supported.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a><span data-ttu-id="d4dee-138">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d4dee-138">Properties</span></span>

<span data-ttu-id="d4dee-139">La classe **MSVM \_ VirtualSystemSnapshotService** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="d4dee-139">The **Msvm\_VirtualSystemSnapshotService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d4dee-140">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="d4dee-140">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4dee-141">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d4dee-141">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d4dee-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4dee-143">Indique les valeurs possibles pour le paramètre *RequestedState* de la méthode **RequestStateChange** utilisée pour initier un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="d4dee-143">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method used to initiate a state change.</span></span> <span data-ttu-id="d4dee-144">Les valeurs répertoriées sont un sous-ensemble des valeurs contenues dans la propriété **RequestedStatesSupported** de l’instance associée de la **\_ EnabledLogicalElementCapabilities CIM**, où les valeurs sélectionnées sont une fonction de l’état actuel de l’objet [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="d4dee-144">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="d4dee-145">Cette propriété peut être non **null** si une implémentation est en mesure de publier l’ensemble de valeurs possibles en tant que fonction de l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="d4dee-145">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="d4dee-146">Cette propriété a la **valeur null** si une implémentation ne peut pas déterminer le jeu de valeurs possibles en tant que fonction de l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="d4dee-146">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="d4dee-147">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d4dee-147">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="d4dee-148"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (2)</span><span class="sxs-lookup"><span data-stu-id="d4dee-148"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-149"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (3)</span><span class="sxs-lookup"><span data-stu-id="d4dee-149"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-150"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Arrêter** (4)</span><span class="sxs-lookup"><span data-stu-id="d4dee-150"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-151"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Hors connexion** (6)</span><span class="sxs-lookup"><span data-stu-id="d4dee-151"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-152"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="d4dee-152"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-153"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Différer** (8)</span><span class="sxs-lookup"><span data-stu-id="d4dee-153"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-154"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Suspension** (9)</span><span class="sxs-lookup"><span data-stu-id="d4dee-154"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-155"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Redémarrer** (10)</span><span class="sxs-lookup"><span data-stu-id="d4dee-155"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-156"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Réinitialiser** (11)</span><span class="sxs-lookup"><span data-stu-id="d4dee-156"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-157"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF réservé** (..</span><span class="sxs-lookup"><span data-stu-id="d4dee-157"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="d4dee-158">)</span><span class="sxs-lookup"><span data-stu-id="d4dee-158">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d4dee-159">**Caption**</span><span class="sxs-lookup"><span data-stu-id="d4dee-159">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4dee-160">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d4dee-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-161">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d4dee-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4dee-162">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d4dee-162">A short description of the object.</span></span> <span data-ttu-id="d4dee-163">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « service d’instantané du système virtuel Hyper-V ».</span><span class="sxs-lookup"><span data-stu-id="d4dee-163">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Virtual System Snapshot Service".</span></span>

</dd> <dt>

<span data-ttu-id="d4dee-164">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="d4dee-164">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4dee-165">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d4dee-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-166">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d4dee-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4dee-167">Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="d4dee-167">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="d4dee-168">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="d4dee-168">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d4dee-169">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d4dee-169">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="d4dee-170"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="d4dee-170"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-171"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="d4dee-171"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-172"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span><span class="sxs-lookup"><span data-stu-id="d4dee-172"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-173"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Communication perdue** (3)</span><span class="sxs-lookup"><span data-stu-id="d4dee-173"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-174"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Aucun contact** (4)</span><span class="sxs-lookup"><span data-stu-id="d4dee-174"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-175"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="d4dee-175"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-176"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="d4dee-176"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="d4dee-177">)</span><span class="sxs-lookup"><span data-stu-id="d4dee-177">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d4dee-178">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d4dee-178">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4dee-179">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d4dee-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-180">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d4dee-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-181">Qualificateurs : **clé**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="d4dee-181">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="d4dee-182">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="d4dee-182">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="d4dee-183">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service)et est toujours définie sur « MSVM \_ VirtualSystemSnapshotService ».</span><span class="sxs-lookup"><span data-stu-id="d4dee-183">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_VirtualSystemSnapshotService".</span></span>

</dd> <dt>

<span data-ttu-id="d4dee-184">**Description**</span><span class="sxs-lookup"><span data-stu-id="d4dee-184">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4dee-185">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d4dee-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-186">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d4dee-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4dee-187">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="d4dee-187">A description of the object.</span></span> <span data-ttu-id="d4dee-188">Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « service pour la création, la destruction et l’application d’instantanés d’ordinateur virtuel ».</span><span class="sxs-lookup"><span data-stu-id="d4dee-188">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Service for creating, destroying, and applying virtual machine snapshots".</span></span>

</dd> <dt>

<span data-ttu-id="d4dee-189">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="d4dee-189">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4dee-190">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d4dee-190">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-191">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d4dee-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4dee-192">Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="d4dee-192">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="d4dee-193">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="d4dee-193">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d4dee-194">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d4dee-194">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="d4dee-195"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="d4dee-195"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-196"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Aucune information supplémentaire** (1)</span><span class="sxs-lookup"><span data-stu-id="d4dee-196"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-197"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Souligné** (2)</span><span class="sxs-lookup"><span data-stu-id="d4dee-197"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-198"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Défaillance prédictive** (3)</span><span class="sxs-lookup"><span data-stu-id="d4dee-198"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-199"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erreur non récupérable** (4)</span><span class="sxs-lookup"><span data-stu-id="d4dee-199"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-200"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entité de prise en charge erronée** (5)</span><span class="sxs-lookup"><span data-stu-id="d4dee-200"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-201"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="d4dee-201"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-202"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="d4dee-202"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="d4dee-203">)</span><span class="sxs-lookup"><span data-stu-id="d4dee-203">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d4dee-204">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="d4dee-204">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4dee-205">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d4dee-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-206">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d4dee-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4dee-207">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d4dee-207">A display name for the object.</span></span> <span data-ttu-id="d4dee-208">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d4dee-208">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d4dee-209">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="d4dee-209">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4dee-210">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d4dee-210">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-211">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d4dee-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4dee-212">Configuration par défaut ou de démarrage d’un administrateur pour l’état activé d’un élément.</span><span class="sxs-lookup"><span data-stu-id="d4dee-212">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="d4dee-213">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur 2 (activé).</span><span class="sxs-lookup"><span data-stu-id="d4dee-213">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="d4dee-214">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4dee-214">Value</span></span>                                                                        | <span data-ttu-id="d4dee-215">Signification</span><span class="sxs-lookup"><span data-stu-id="d4dee-215">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="d4dee-216"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="d4dee-216"><dt>2</dt></span></span> </dl> | <span data-ttu-id="d4dee-217">activé</span><span class="sxs-lookup"><span data-stu-id="d4dee-217">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d4dee-218">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="d4dee-218">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4dee-219">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d4dee-219">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-220">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d4dee-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4dee-221">États activés et désactivés d’un élément.</span><span class="sxs-lookup"><span data-stu-id="d4dee-221">The enabled and disabled states of an element.</span></span> <span data-ttu-id="d4dee-222">Il peut également indiquer les transitions entre ces États demandés.</span><span class="sxs-lookup"><span data-stu-id="d4dee-222">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="d4dee-223">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur 2 (activé).</span><span class="sxs-lookup"><span data-stu-id="d4dee-223">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="d4dee-224">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4dee-224">Value</span></span>                                                                        | <span data-ttu-id="d4dee-225">Signification</span><span class="sxs-lookup"><span data-stu-id="d4dee-225">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="d4dee-226"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="d4dee-226"><dt>2</dt></span></span> </dl> | <span data-ttu-id="d4dee-227">activé</span><span class="sxs-lookup"><span data-stu-id="d4dee-227">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d4dee-228">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="d4dee-228">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4dee-229">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d4dee-229">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-230">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d4dee-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4dee-231">Intégrité actuelle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="d4dee-231">The current health of the element.</span></span> <span data-ttu-id="d4dee-232">Cet attribut exprime l’intégrité de cet élément, mais pas nécessairement celle de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="d4dee-232">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="d4dee-233">Les valeurs possibles sont comprises entre 0 et 30, où 5 signifie que l’élément est entièrement sain et 30 signifie que l’élément est complètement non opérationnel.</span><span class="sxs-lookup"><span data-stu-id="d4dee-233">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="d4dee-234">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est toujours définie sur 5 (OK).</span><span class="sxs-lookup"><span data-stu-id="d4dee-234">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>



| <span data-ttu-id="d4dee-235">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4dee-235">Value</span></span>                                                                        | <span data-ttu-id="d4dee-236">Signification</span><span class="sxs-lookup"><span data-stu-id="d4dee-236">Meaning</span></span>                                 |
|------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="d4dee-237"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="d4dee-237"><dt>5</dt></span></span> </dl> | <span data-ttu-id="d4dee-238">L’état d’intégrité est normal.</span><span class="sxs-lookup"><span data-stu-id="d4dee-238">The health status is normal.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d4dee-239">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d4dee-239">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4dee-240">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d4dee-240">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-241">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d4dee-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4dee-242">Date et heure de création de la configuration de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="d4dee-242">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="d4dee-243">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d4dee-243">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d4dee-244">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d4dee-244">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4dee-245">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d4dee-245">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-246">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d4dee-246">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-247">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="d4dee-247">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="d4dee-248">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="d4dee-248">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="d4dee-249">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d4dee-249">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d4dee-250">**Nom**</span><span class="sxs-lookup"><span data-stu-id="d4dee-250">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4dee-251">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d4dee-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-252">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d4dee-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-253">Qualificateurs : **clé**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="d4dee-253">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="d4dee-254">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="d4dee-254">The label by which the object is known.</span></span> <span data-ttu-id="d4dee-255">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est toujours définie sur « vssnapsvc ».</span><span class="sxs-lookup"><span data-stu-id="d4dee-255">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "vssnapsvc".</span></span>

</dd> <dt>

<span data-ttu-id="d4dee-256">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="d4dee-256">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4dee-257">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d4dee-257">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-258">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d4dee-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4dee-259">Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="d4dee-259">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="d4dee-260">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="d4dee-260">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d4dee-261">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d4dee-261">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="d4dee-262"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="d4dee-262"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-263"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="d4dee-263"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-264"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Maintenance** (2)</span><span class="sxs-lookup"><span data-stu-id="d4dee-264"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-265"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Démarrage** (3)</span><span class="sxs-lookup"><span data-stu-id="d4dee-265"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-266"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arrêt** (4)</span><span class="sxs-lookup"><span data-stu-id="d4dee-266"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-267"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrêté** (5)</span><span class="sxs-lookup"><span data-stu-id="d4dee-267"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-268"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abandonné** (6)</span><span class="sxs-lookup"><span data-stu-id="d4dee-268"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-269"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span><span class="sxs-lookup"><span data-stu-id="d4dee-269"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-270"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Terminé** (8)</span><span class="sxs-lookup"><span data-stu-id="d4dee-270"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-271"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migration** (9)</span><span class="sxs-lookup"><span data-stu-id="d4dee-271"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-272"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="d4dee-272"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-273"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Inmigration** (11)</span><span class="sxs-lookup"><span data-stu-id="d4dee-273"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-274"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Capture d’instantanés** (12)</span><span class="sxs-lookup"><span data-stu-id="d4dee-274"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-275"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arrêt** (13)</span><span class="sxs-lookup"><span data-stu-id="d4dee-275"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-276"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (14)</span><span class="sxs-lookup"><span data-stu-id="d4dee-276"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-277"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transition** (15)</span><span class="sxs-lookup"><span data-stu-id="d4dee-277"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-278"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En service** (16)</span><span class="sxs-lookup"><span data-stu-id="d4dee-278"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-279"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="d4dee-279"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-280"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="d4dee-280"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="d4dee-281">)</span><span class="sxs-lookup"><span data-stu-id="d4dee-281">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d4dee-282">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="d4dee-282">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4dee-283">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d4dee-283">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-284">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d4dee-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4dee-285">États actuels de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d4dee-285">The current statuses of the object.</span></span> <span data-ttu-id="d4dee-286">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), et chaque élément de tableau a toujours la valeur 2 (OK).</span><span class="sxs-lookup"><span data-stu-id="d4dee-286">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="d4dee-287">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="d4dee-287">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4dee-288">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d4dee-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-289">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d4dee-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4dee-290">Chaîne qui décrit l’état activé ou désactivé de l’élément lorsque la propriété **EnabledState** a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="d4dee-290">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="d4dee-291">Cette propriété doit avoir la valeur **null** quand **EnabledState** a une valeur autre que 1.</span><span class="sxs-lookup"><span data-stu-id="d4dee-291">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="d4dee-292">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="d4dee-292">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d4dee-293">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="d4dee-293">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4dee-294">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d4dee-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-295">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d4dee-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-296">Qualificateurs : **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="d4dee-296">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="d4dee-297">Toutes les informations relatives à la façon dont le propriétaire principal du service est accessible (par exemple, numéro de téléphone, adresse e-mail, etc.).</span><span class="sxs-lookup"><span data-stu-id="d4dee-297">Any information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="d4dee-298">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="d4dee-298">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d4dee-299">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="d4dee-299">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4dee-300">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d4dee-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-301">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d4dee-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-302">Qualificateurs : **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="d4dee-302">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="d4dee-303">Nom du propriétaire principal du service, s’il est défini.</span><span class="sxs-lookup"><span data-stu-id="d4dee-303">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="d4dee-304">Le propriétaire principal est le contact de support initial pour le service.</span><span class="sxs-lookup"><span data-stu-id="d4dee-304">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="d4dee-305">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="d4dee-305">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d4dee-306">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="d4dee-306">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4dee-307">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d4dee-307">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-308">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d4dee-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4dee-309">Fournit des informations d’état de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="d4dee-309">Provides high level status information.</span></span> <span data-ttu-id="d4dee-310">Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir un état d’intégrité élevé et détaillé de l’élément et de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="d4dee-310">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="d4dee-311">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="d4dee-311">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d4dee-312">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d4dee-312">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="d4dee-313"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="d4dee-313"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-314"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="d4dee-314"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-315"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (2)</span><span class="sxs-lookup"><span data-stu-id="d4dee-315"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-316"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erreur** (3)</span><span class="sxs-lookup"><span data-stu-id="d4dee-316"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-317"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="d4dee-317"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-318"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="d4dee-318"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="d4dee-319">)</span><span class="sxs-lookup"><span data-stu-id="d4dee-319">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d4dee-320">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="d4dee-320">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4dee-321">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d4dee-321">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-322">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d4dee-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4dee-323">Dernier État demandé ou souhaité pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="d4dee-323">The last requested or desired state for the element.</span></span> <span data-ttu-id="d4dee-324">L’état réel de l’élément est représenté par **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="d4dee-324">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="d4dee-325">Cette propriété est fournie pour comparer les derniers États demandés et actuels d’un élément.</span><span class="sxs-lookup"><span data-stu-id="d4dee-325">This property is provided to compare the last requested and current states for an element.</span></span> <span data-ttu-id="d4dee-326">Une instance particulière de la [**classe \_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)) peut ne pas prendre en charge la propriété **RequestedState** .</span><span class="sxs-lookup"><span data-stu-id="d4dee-326">A particular instance of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) class might not support the **RequestedState** property.</span></span> <span data-ttu-id="d4dee-327">Si cela se produit, la valeur 12 (non applicable) est utilisée.</span><span class="sxs-lookup"><span data-stu-id="d4dee-327">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="d4dee-328">Cette propriété est héritée de la **\_ EnabledLogicalElement CIM** et est toujours définie sur 12 (non applicable).</span><span class="sxs-lookup"><span data-stu-id="d4dee-328">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 12 (Not Applicable).</span></span>



| <span data-ttu-id="d4dee-329">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4dee-329">Value</span></span>                                                                         | <span data-ttu-id="d4dee-330">Signification</span><span class="sxs-lookup"><span data-stu-id="d4dee-330">Meaning</span></span>                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="d4dee-331"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="d4dee-331"><dt>12</dt></span></span> </dl> | <span data-ttu-id="d4dee-332">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="d4dee-332">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d4dee-333">**Cours**</span><span class="sxs-lookup"><span data-stu-id="d4dee-333">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4dee-334">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="d4dee-334">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-335">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d4dee-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4dee-336">Indique si le service est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="d4dee-336">Indicates whether the service is currently running.</span></span> <span data-ttu-id="d4dee-337">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service)et est toujours définie sur **true**.</span><span class="sxs-lookup"><span data-stu-id="d4dee-337">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="d4dee-338">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="d4dee-338">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4dee-339">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d4dee-339">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-340">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d4dee-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-341">Qualificateurs : **MaxLen** (10)</span><span class="sxs-lookup"><span data-stu-id="d4dee-341">Qualifiers: **MaxLen** ( 10 )</span></span>
</dt> </dl>

<span data-ttu-id="d4dee-342">Valeur de chaîne qui indique si le service est démarré automatiquement par un système, un système d’exploitation ou s’il est démarré uniquement sur demande.</span><span class="sxs-lookup"><span data-stu-id="d4dee-342">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="d4dee-343">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="d4dee-343">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d4dee-344">**État**</span><span class="sxs-lookup"><span data-stu-id="d4dee-344">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4dee-345">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d4dee-345">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-346">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d4dee-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4dee-347">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="d4dee-347">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d4dee-348">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="d4dee-348">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4dee-349">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="d4dee-349">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-350">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d4dee-350">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4dee-351">Chaînes qui décrivent les différentes valeurs de tableau **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="d4dee-351">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="d4dee-352">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), et chaque élément de tableau a toujours la valeur « le service s’exécute normalement ».</span><span class="sxs-lookup"><span data-stu-id="d4dee-352">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "The service is running normally".</span></span>

</dd> <dt>

<span data-ttu-id="d4dee-353">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d4dee-353">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4dee-354">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d4dee-354">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-355">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d4dee-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-356">Qualificateurs : **clé**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="d4dee-356">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="d4dee-357">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="d4dee-357">The scoping system's creation class name.</span></span> <span data-ttu-id="d4dee-358">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service)et est toujours définie sur « MSVM \_ ComputerSystem ».</span><span class="sxs-lookup"><span data-stu-id="d4dee-358">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="d4dee-359">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="d4dee-359">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4dee-360">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d4dee-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-361">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d4dee-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-362">Qualificateurs : **clé**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="d4dee-362">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="d4dee-363">Nom NetBIOS du système informatique d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="d4dee-363">The NetBIOS name of the hosting computer system.</span></span> <span data-ttu-id="d4dee-364">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="d4dee-364">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="d4dee-365">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="d4dee-365">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4dee-366">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d4dee-366">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-367">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d4dee-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4dee-368">Date ou heure de la dernière modification de l’état activé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="d4dee-368">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="d4dee-369">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d4dee-369">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d4dee-370">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="d4dee-370">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4dee-371">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d4dee-371">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d4dee-372">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d4dee-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4dee-373">Indique l’État cible de la transition de l’instance.</span><span class="sxs-lookup"><span data-stu-id="d4dee-373">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="d4dee-374">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d4dee-374">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="d4dee-375">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4dee-375">Value</span></span>                                                                                                                                                                                                                                                     | <span data-ttu-id="d4dee-376">Signification</span><span class="sxs-lookup"><span data-stu-id="d4dee-376">Meaning</span></span>                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="d4dee-377"><dt>**Inconnu**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d4dee-377"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                               |                                                                                  |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="d4dee-378"><dt>**Activé**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="d4dee-378"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                               |                                                                                  |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="d4dee-379"><dt>**Désactivé**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="d4dee-379"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                           |                                                                                  |
| <span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span><dl> <span data-ttu-id="d4dee-380"><dt>**Arrêter**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="d4dee-380"><dt>**Shut Down**</dt> <dt>4</dt></span></span> </dl>                       |                                                                                  |
| <span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span><dl> <span data-ttu-id="d4dee-381"><dt>**Aucune modification**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="d4dee-381"><dt>**No Change**</dt> <dt>5</dt></span></span> </dl>                       | <span data-ttu-id="d4dee-382">Aucune transition n’est en cours.</span><span class="sxs-lookup"><span data-stu-id="d4dee-382">No transition is in progress.</span></span><br/>                                         |
| <span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span><dl> <span data-ttu-id="d4dee-383"><dt>**Hors connexion**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="d4dee-383"><dt>**Offline**</dt> <dt>6</dt></span></span> </dl>                               |                                                                                  |
| <span id="Test"></span><span id="test"></span><span id="TEST"></span><dl> <span data-ttu-id="d4dee-384"><dt>**Test**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="d4dee-384"><dt>**Test**</dt> <dt>7</dt></span></span> </dl>                                           |                                                                                  |
| <span id="Defer"></span><span id="defer"></span><span id="DEFER"></span><dl> <span data-ttu-id="d4dee-385"><dt>**Différer**</dt> de <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="d4dee-385"><dt>**Defer**</dt> <dt>8</dt></span></span> </dl>                                       |                                                                                  |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="d4dee-386"><dt>**Suspension**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="d4dee-386"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                               |                                                                                  |
| <span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span><dl> <span data-ttu-id="d4dee-387"><dt>**Redémarrer**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="d4dee-387"><dt>**Reboot**</dt> <dt>10</dt></span></span> </dl>                                  |                                                                                  |
| <span id="Reset"></span><span id="reset"></span><span id="RESET"></span><dl> <span data-ttu-id="d4dee-388"><dt>**Réinitialiser**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="d4dee-388"><dt>**Reset**</dt> <dt>11</dt></span></span> </dl>                                      |                                                                                  |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="d4dee-389"><dt>**Non applicable**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="d4dee-389"><dt>**Not Applicable**</dt> <dt>12</dt></span></span> </dl>  | <span data-ttu-id="d4dee-390">L’implémentation ne prend pas en charge la représentation des transitions en cours.</span><span class="sxs-lookup"><span data-stu-id="d4dee-390">The implementation does not support representing ongoing transitions.</span></span><br/> |
| <span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span><dl> <span data-ttu-id="d4dee-391"><dt> **DMTF réservé**</dt> <dt>..</dt></span><span class="sxs-lookup"><span data-stu-id="d4dee-391"><dt>**DMTF Reserved** </dt> <dt>.. </dt></span></span> </dl> |                                                                                  |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d4dee-392">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d4dee-392">Requirements</span></span>



| <span data-ttu-id="d4dee-393">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d4dee-393">Requirement</span></span> | <span data-ttu-id="d4dee-394">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4dee-394">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4dee-395">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d4dee-395">Minimum supported client</span></span><br/> | <span data-ttu-id="d4dee-396">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d4dee-396">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d4dee-397">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d4dee-397">Minimum supported server</span></span><br/> | <span data-ttu-id="d4dee-398">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d4dee-398">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d4dee-399">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d4dee-399">Namespace</span></span><br/>                | <span data-ttu-id="d4dee-400">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="d4dee-400">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d4dee-401">MOF</span><span class="sxs-lookup"><span data-stu-id="d4dee-401">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d4dee-402"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d4dee-402"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d4dee-403">DLL</span><span class="sxs-lookup"><span data-stu-id="d4dee-403">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4dee-404"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d4dee-404"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

