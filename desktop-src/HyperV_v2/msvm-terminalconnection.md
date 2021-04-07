---
description: Indique l’état d’une session à distance active qui interagit avec un ordinateur virtuel.
ms.assetid: EAE6082F-A0CB-4E75-8029-51E20649C0A8
title: Classe Msvm_TerminalConnection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TerminalConnection
- Msvm_TerminalConnection.InstanceID
- Msvm_TerminalConnection.Caption
- Msvm_TerminalConnection.Description
- Msvm_TerminalConnection.ElementName
- Msvm_TerminalConnection.InstallDate
- Msvm_TerminalConnection.Name
- Msvm_TerminalConnection.OperationalStatus
- Msvm_TerminalConnection.StatusDescriptions
- Msvm_TerminalConnection.Status
- Msvm_TerminalConnection.HealthState
- Msvm_TerminalConnection.CommunicationStatus
- Msvm_TerminalConnection.DetailedStatus
- Msvm_TerminalConnection.OperatingStatus
- Msvm_TerminalConnection.PrimaryStatus
- Msvm_TerminalConnection.EnabledState
- Msvm_TerminalConnection.OtherEnabledState
- Msvm_TerminalConnection.RequestedState
- Msvm_TerminalConnection.EnabledDefault
- Msvm_TerminalConnection.TimeOfLastStateChange
- Msvm_TerminalConnection.AvailableRequestedStates
- Msvm_TerminalConnection.TransitioningToState
- Msvm_TerminalConnection.ConnectionID
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 66be5000fb7fdd4404e07c87673e3359065af6bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759052"
---
# <a name="msvm_terminalconnection-class"></a><span data-ttu-id="2b3e9-103">MSVM \_ TerminalConnection, classe</span><span class="sxs-lookup"><span data-stu-id="2b3e9-103">Msvm\_TerminalConnection class</span></span>

<span data-ttu-id="2b3e9-104">Indique l’état d’une session à distance active qui interagit avec un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="2b3e9-104">Indicates the state of an active remote session interacting with a virtual machine.</span></span> <span data-ttu-id="2b3e9-105">Il ne peut y avoir qu’une seule connexion à la fois.</span><span class="sxs-lookup"><span data-stu-id="2b3e9-105">There can only be one connection at a time.</span></span>

<span data-ttu-id="2b3e9-106">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="2b3e9-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b3e9-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2b3e9-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TerminalConnection : CIM_EnabledLogicalElement
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
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
  uint16   TransitioningToState = 12;
  string   ConnectionID;
};
```

## <a name="members"></a><span data-ttu-id="2b3e9-108">Membres</span><span class="sxs-lookup"><span data-stu-id="2b3e9-108">Members</span></span>

<span data-ttu-id="2b3e9-109">La classe **MSVM \_ TerminalConnection** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="2b3e9-109">The **Msvm\_TerminalConnection** class has these types of members:</span></span>

-   [<span data-ttu-id="2b3e9-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2b3e9-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="2b3e9-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2b3e9-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2b3e9-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2b3e9-112">Methods</span></span>

<span data-ttu-id="2b3e9-113">La classe **MSVM \_ TerminalConnection** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="2b3e9-113">The **Msvm\_TerminalConnection** class has these methods.</span></span>



| <span data-ttu-id="2b3e9-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="2b3e9-114">Method</span></span>                                                                   | <span data-ttu-id="2b3e9-115">Description</span><span class="sxs-lookup"><span data-stu-id="2b3e9-115">Description</span></span>                         |
|:-------------------------------------------------------------------------|:------------------------------------|
| [<span data-ttu-id="2b3e9-116">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="2b3e9-116">**RequestStateChange**</span></span>](msvm-terminalconnection-requeststatechange.md) | <span data-ttu-id="2b3e9-117">Demande un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="2b3e9-117">Requests a state change.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="2b3e9-118">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2b3e9-118">Properties</span></span>

<span data-ttu-id="2b3e9-119">La classe **MSVM \_ TerminalConnection** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="2b3e9-119">The **Msvm\_TerminalConnection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2b3e9-120">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="2b3e9-120">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b3e9-121">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2b3e9-121">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2b3e9-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2b3e9-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b3e9-123">Indique les valeurs possibles pour le paramètre *RequestedState* de la méthode **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="2b3e9-123">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="2b3e9-124">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="2b3e9-124">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="2b3e9-125">**Caption**</span><span class="sxs-lookup"><span data-stu-id="2b3e9-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b3e9-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2b3e9-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b3e9-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2b3e9-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b3e9-128">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="2b3e9-128">A short description of the object.</span></span> <span data-ttu-id="2b3e9-129">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="2b3e9-129">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2b3e9-130">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="2b3e9-130">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b3e9-131">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2b3e9-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2b3e9-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2b3e9-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b3e9-133">Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="2b3e9-133">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="2b3e9-134">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="2b3e9-134">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="2b3e9-135">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2b3e9-135">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="2b3e9-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="2b3e9-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2b3e9-137"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="2b3e9-137"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2b3e9-138"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span><span class="sxs-lookup"><span data-stu-id="2b3e9-138"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2b3e9-139"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Communication perdue** (3)</span><span class="sxs-lookup"><span data-stu-id="2b3e9-139"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2b3e9-140"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Aucun contact** (4)</span><span class="sxs-lookup"><span data-stu-id="2b3e9-140"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="2b3e9-141"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="2b3e9-141"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="2b3e9-142"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="2b3e9-142"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="2b3e9-143">)</span><span class="sxs-lookup"><span data-stu-id="2b3e9-143">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2b3e9-144">**ConnectionID**</span><span class="sxs-lookup"><span data-stu-id="2b3e9-144">**ConnectionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b3e9-145">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2b3e9-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b3e9-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2b3e9-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b3e9-147">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2b3e9-147">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2b3e9-148">Identificateur unique d’une instance de l’objet de connexion de terminal.</span><span class="sxs-lookup"><span data-stu-id="2b3e9-148">The unique identifier for an instance of the terminal connection object.</span></span> <span data-ttu-id="2b3e9-149">L’identificateur se présente sous la forme « Microsoft :*VMID* \\ *index*».</span><span class="sxs-lookup"><span data-stu-id="2b3e9-149">The identifier is of the form "Microsoft:*VMID*\\*Index*".</span></span> <span data-ttu-id="2b3e9-150">Par exemple, « Microsoft : 67A5D397-A02D-11DB-AC13-001676AA34F0 \\ 0 ».</span><span class="sxs-lookup"><span data-stu-id="2b3e9-150">For example, "Microsoft:67A5D397-A02D-11DB-AC13-001676AA34F0\\0".</span></span>

</dd> <dt>

<span data-ttu-id="2b3e9-151">**Description**</span><span class="sxs-lookup"><span data-stu-id="2b3e9-151">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b3e9-152">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2b3e9-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b3e9-153">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2b3e9-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b3e9-154">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="2b3e9-154">A description of the object.</span></span> <span data-ttu-id="2b3e9-155">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="2b3e9-155">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2b3e9-156">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="2b3e9-156">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b3e9-157">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2b3e9-157">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2b3e9-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2b3e9-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b3e9-159">Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="2b3e9-159">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="2b3e9-160">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="2b3e9-160">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="2b3e9-161">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2b3e9-161">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="2b3e9-162"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="2b3e9-162"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2b3e9-163"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Aucune information supplémentaire** (1)</span><span class="sxs-lookup"><span data-stu-id="2b3e9-163"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2b3e9-164"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Souligné** (2)</span><span class="sxs-lookup"><span data-stu-id="2b3e9-164"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2b3e9-165"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Défaillance prédictive** (3)</span><span class="sxs-lookup"><span data-stu-id="2b3e9-165"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2b3e9-166"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erreur non récupérable** (4)</span><span class="sxs-lookup"><span data-stu-id="2b3e9-166"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="2b3e9-167"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entité de prise en charge erronée** (5)</span><span class="sxs-lookup"><span data-stu-id="2b3e9-167"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="2b3e9-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="2b3e9-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="2b3e9-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="2b3e9-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="2b3e9-170">)</span><span class="sxs-lookup"><span data-stu-id="2b3e9-170">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2b3e9-171">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="2b3e9-171">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b3e9-172">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2b3e9-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b3e9-173">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2b3e9-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b3e9-174">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="2b3e9-174">A display name for the object.</span></span> <span data-ttu-id="2b3e9-175">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="2b3e9-175">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2b3e9-176">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="2b3e9-176">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b3e9-177">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2b3e9-177">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2b3e9-178">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2b3e9-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b3e9-179">Configuration par défaut ou de démarrage d’un administrateur pour l’état activé d’un élément.</span><span class="sxs-lookup"><span data-stu-id="2b3e9-179">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="2b3e9-180">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2b3e9-180">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="2b3e9-181">Valeur</span><span class="sxs-lookup"><span data-stu-id="2b3e9-181">Value</span></span>                                                                        | <span data-ttu-id="2b3e9-182">Signification</span><span class="sxs-lookup"><span data-stu-id="2b3e9-182">Meaning</span></span>             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="2b3e9-183"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="2b3e9-183"><dt>2</dt></span></span> </dl> | <span data-ttu-id="2b3e9-184">activé</span><span class="sxs-lookup"><span data-stu-id="2b3e9-184">Enabled</span></span><br/>  |
| <dl> <span data-ttu-id="2b3e9-185"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="2b3e9-185"><dt>3</dt></span></span> </dl> | <span data-ttu-id="2b3e9-186">Désactivé</span><span class="sxs-lookup"><span data-stu-id="2b3e9-186">Disabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2b3e9-187">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="2b3e9-187">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b3e9-188">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2b3e9-188">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2b3e9-189">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2b3e9-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b3e9-190">États activés et désactivés d’un élément.</span><span class="sxs-lookup"><span data-stu-id="2b3e9-190">The enabled and disabled states of an element.</span></span> <span data-ttu-id="2b3e9-191">Il peut également indiquer les transitions entre ces États demandés.</span><span class="sxs-lookup"><span data-stu-id="2b3e9-191">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="2b3e9-192">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2b3e9-192">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="2b3e9-193">Valeur</span><span class="sxs-lookup"><span data-stu-id="2b3e9-193">Value</span></span>                                                                        | <span data-ttu-id="2b3e9-194">Signification</span><span class="sxs-lookup"><span data-stu-id="2b3e9-194">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="2b3e9-195"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="2b3e9-195"><dt>2</dt></span></span> </dl> | <span data-ttu-id="2b3e9-196">activé</span><span class="sxs-lookup"><span data-stu-id="2b3e9-196">Enabled</span></span><br/>        |
| <dl> <span data-ttu-id="2b3e9-197"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="2b3e9-197"><dt>3</dt></span></span> </dl> | <span data-ttu-id="2b3e9-198">Désactivé</span><span class="sxs-lookup"><span data-stu-id="2b3e9-198">Disabled</span></span><br/>       |
| <dl> <span data-ttu-id="2b3e9-199"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="2b3e9-199"><dt>5</dt></span></span> </dl> | <span data-ttu-id="2b3e9-200">Non applicable</span><span class="sxs-lookup"><span data-stu-id="2b3e9-200">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2b3e9-201">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="2b3e9-201">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b3e9-202">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2b3e9-202">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2b3e9-203">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2b3e9-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b3e9-204">Intégrité actuelle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="2b3e9-204">The current health of the element.</span></span> <span data-ttu-id="2b3e9-205">Cet attribut exprime l’intégrité de cet élément, mais pas nécessairement celle de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="2b3e9-205">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="2b3e9-206">Les valeurs possibles sont comprises entre 0 et 30, où 5 signifie que l’élément est entièrement sain et 30 signifie que l’élément est complètement non opérationnel.</span><span class="sxs-lookup"><span data-stu-id="2b3e9-206">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="2b3e9-207">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est toujours définie sur 5 (OK).</span><span class="sxs-lookup"><span data-stu-id="2b3e9-207">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="2b3e9-208">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="2b3e9-208">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b3e9-209">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2b3e9-209">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2b3e9-210">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2b3e9-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b3e9-211">Date et heure de création de la configuration de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="2b3e9-211">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="2b3e9-212">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2b3e9-212">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2b3e9-213">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2b3e9-213">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b3e9-214">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2b3e9-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b3e9-215">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2b3e9-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b3e9-216">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="2b3e9-216">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="2b3e9-217">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="2b3e9-217">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="2b3e9-218">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="2b3e9-218">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2b3e9-219">**Nom**</span><span class="sxs-lookup"><span data-stu-id="2b3e9-219">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b3e9-220">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2b3e9-220">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b3e9-221">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2b3e9-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b3e9-222">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="2b3e9-222">The label by which the object is known.</span></span> <span data-ttu-id="2b3e9-223">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est identique à la propriété **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="2b3e9-223">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is the same as the **ElementName** property.</span></span>

</dd> <dt>

<span data-ttu-id="2b3e9-224">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="2b3e9-224">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b3e9-225">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2b3e9-225">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2b3e9-226">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2b3e9-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b3e9-227">Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="2b3e9-227">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="2b3e9-228">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="2b3e9-228">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="2b3e9-229">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2b3e9-229">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="2b3e9-230"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="2b3e9-230"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2b3e9-231"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="2b3e9-231"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2b3e9-232"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Maintenance** (2)</span><span class="sxs-lookup"><span data-stu-id="2b3e9-232"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2b3e9-233"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Démarrage** (3)</span><span class="sxs-lookup"><span data-stu-id="2b3e9-233"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2b3e9-234"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arrêt** (4)</span><span class="sxs-lookup"><span data-stu-id="2b3e9-234"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="2b3e9-235"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrêté** (5)</span><span class="sxs-lookup"><span data-stu-id="2b3e9-235"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="2b3e9-236"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abandonné** (6)</span><span class="sxs-lookup"><span data-stu-id="2b3e9-236"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="2b3e9-237"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span><span class="sxs-lookup"><span data-stu-id="2b3e9-237"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="2b3e9-238"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Terminé** (8)</span><span class="sxs-lookup"><span data-stu-id="2b3e9-238"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="2b3e9-239"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migration** (9)</span><span class="sxs-lookup"><span data-stu-id="2b3e9-239"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="2b3e9-240"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="2b3e9-240"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="2b3e9-241"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Inmigration** (11)</span><span class="sxs-lookup"><span data-stu-id="2b3e9-241"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="2b3e9-242"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Capture d’instantanés** (12)</span><span class="sxs-lookup"><span data-stu-id="2b3e9-242"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="2b3e9-243"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arrêt** (13)</span><span class="sxs-lookup"><span data-stu-id="2b3e9-243"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="2b3e9-244"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (14)</span><span class="sxs-lookup"><span data-stu-id="2b3e9-244"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="2b3e9-245"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transition** (15)</span><span class="sxs-lookup"><span data-stu-id="2b3e9-245"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="2b3e9-246"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En service** (16)</span><span class="sxs-lookup"><span data-stu-id="2b3e9-246"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="2b3e9-247"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="2b3e9-247"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="2b3e9-248"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="2b3e9-248"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="2b3e9-249">)</span><span class="sxs-lookup"><span data-stu-id="2b3e9-249">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2b3e9-250">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="2b3e9-250">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b3e9-251">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2b3e9-251">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2b3e9-252">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2b3e9-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b3e9-253">États actuels de l’objet.</span><span class="sxs-lookup"><span data-stu-id="2b3e9-253">The current statuses of the object.</span></span> <span data-ttu-id="2b3e9-254">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2b3e9-254">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2b3e9-255">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="2b3e9-255">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b3e9-256">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2b3e9-256">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b3e9-257">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2b3e9-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b3e9-258">Chaîne qui décrit l’état activé ou désactivé de l’élément lorsque la propriété **EnabledState** a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="2b3e9-258">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="2b3e9-259">Cette propriété doit avoir la valeur **null** quand **EnabledState** a une valeur autre que 1.</span><span class="sxs-lookup"><span data-stu-id="2b3e9-259">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="2b3e9-260">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="2b3e9-260">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="2b3e9-261">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="2b3e9-261">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b3e9-262">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2b3e9-262">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2b3e9-263">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2b3e9-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b3e9-264">Fournit des informations d’état de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="2b3e9-264">Provides high level status information.</span></span> <span data-ttu-id="2b3e9-265">Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir un état d’intégrité élevé et détaillé de l’élément et de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="2b3e9-265">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="2b3e9-266">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="2b3e9-266">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="2b3e9-267">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2b3e9-267">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="2b3e9-268"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="2b3e9-268"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2b3e9-269"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="2b3e9-269"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2b3e9-270"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (2)</span><span class="sxs-lookup"><span data-stu-id="2b3e9-270"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2b3e9-271"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erreur** (3)</span><span class="sxs-lookup"><span data-stu-id="2b3e9-271"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2b3e9-272"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="2b3e9-272"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="2b3e9-273"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="2b3e9-273"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="2b3e9-274">)</span><span class="sxs-lookup"><span data-stu-id="2b3e9-274">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2b3e9-275">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="2b3e9-275">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b3e9-276">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2b3e9-276">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2b3e9-277">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2b3e9-277">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b3e9-278">Dernier État demandé ou souhaité pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="2b3e9-278">The last requested or desired state for the element.</span></span> <span data-ttu-id="2b3e9-279">L’état réel de l’élément est représenté par **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="2b3e9-279">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="2b3e9-280">Cette propriété est fournie pour comparer les derniers États activés et actuellement activés ou désactivés.</span><span class="sxs-lookup"><span data-stu-id="2b3e9-280">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="2b3e9-281">Une instance particulière de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)) peut ne pas prendre en charge **RequestStateChange**.</span><span class="sxs-lookup"><span data-stu-id="2b3e9-281">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support **RequestStateChange**.</span></span> <span data-ttu-id="2b3e9-282">Si cela se produit, la valeur 12 est utilisée.</span><span class="sxs-lookup"><span data-stu-id="2b3e9-282">If this occurs, the value 12 is used.</span></span> <span data-ttu-id="2b3e9-283">Cette propriété est héritée de la **\_ EnabledLogicalElement CIM**.</span><span class="sxs-lookup"><span data-stu-id="2b3e9-283">This property is inherited from **CIM\_EnabledLogicalElement**.</span></span>



| <span data-ttu-id="2b3e9-284">Valeur</span><span class="sxs-lookup"><span data-stu-id="2b3e9-284">Value</span></span>                                                                         | <span data-ttu-id="2b3e9-285">Signification</span><span class="sxs-lookup"><span data-stu-id="2b3e9-285">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="2b3e9-286"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="2b3e9-286"><dt>12</dt></span></span> </dl> | <span data-ttu-id="2b3e9-287">Non applicable</span><span class="sxs-lookup"><span data-stu-id="2b3e9-287">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2b3e9-288">**État**</span><span class="sxs-lookup"><span data-stu-id="2b3e9-288">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b3e9-289">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2b3e9-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b3e9-290">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2b3e9-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b3e9-291">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="2b3e9-291">The current status of the object.</span></span> <span data-ttu-id="2b3e9-292">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="2b3e9-292">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2b3e9-293">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="2b3e9-293">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b3e9-294">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="2b3e9-294">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2b3e9-295">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2b3e9-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b3e9-296">Chaînes qui décrivent les différentes valeurs de tableau **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="2b3e9-296">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="2b3e9-297">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2b3e9-297">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2b3e9-298">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="2b3e9-298">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b3e9-299">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2b3e9-299">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2b3e9-300">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2b3e9-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b3e9-301">Date ou heure de la dernière modification de l’état activé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="2b3e9-301">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="2b3e9-302">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="2b3e9-302">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="2b3e9-303">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="2b3e9-303">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b3e9-304">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2b3e9-304">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2b3e9-305">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2b3e9-305">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b3e9-306">Indique l’État cible de la transition de l’instance.</span><span class="sxs-lookup"><span data-stu-id="2b3e9-306">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="2b3e9-307">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2b3e9-307">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="2b3e9-308">Valeur</span><span class="sxs-lookup"><span data-stu-id="2b3e9-308">Value</span></span>                                                                         | <span data-ttu-id="2b3e9-309">Signification</span><span class="sxs-lookup"><span data-stu-id="2b3e9-309">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="2b3e9-310"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="2b3e9-310"><dt>12</dt></span></span> </dl> | <span data-ttu-id="2b3e9-311">Non applicable</span><span class="sxs-lookup"><span data-stu-id="2b3e9-311">Not Applicable</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2b3e9-312">Notes</span><span class="sxs-lookup"><span data-stu-id="2b3e9-312">Remarks</span></span>

<span data-ttu-id="2b3e9-313">L’accès à la classe **MSVM \_ TerminalConnection** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="2b3e9-313">Access to the **Msvm\_TerminalConnection** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="2b3e9-314">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="2b3e9-314">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="2b3e9-315">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2b3e9-315">Requirements</span></span>



| <span data-ttu-id="2b3e9-316">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2b3e9-316">Requirement</span></span> | <span data-ttu-id="2b3e9-317">Valeur</span><span class="sxs-lookup"><span data-stu-id="2b3e9-317">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b3e9-318">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2b3e9-318">Minimum supported client</span></span><br/> | <span data-ttu-id="2b3e9-319">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2b3e9-319">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2b3e9-320">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2b3e9-320">Minimum supported server</span></span><br/> | <span data-ttu-id="2b3e9-321">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2b3e9-321">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2b3e9-322">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2b3e9-322">Namespace</span></span><br/>                | <span data-ttu-id="2b3e9-323">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="2b3e9-323">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2b3e9-324">MOF</span><span class="sxs-lookup"><span data-stu-id="2b3e9-324">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2b3e9-325"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2b3e9-325"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2b3e9-326">DLL</span><span class="sxs-lookup"><span data-stu-id="2b3e9-326">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b3e9-327"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2b3e9-327"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2b3e9-328">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2b3e9-328">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b3e9-329">**\_ENABLEDLOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="2b3e9-329">**CIM\_EnabledLogicalElement**</span></span>](cim-enabledlogicalelement.md)
</dt> <dt>

<span data-ttu-id="2b3e9-330">[**\_ENABLEDLOGICALELEMENT CIM**](/previous-versions//cc136818(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2b3e9-330">[**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="2b3e9-331">Classes vidéo</span><span class="sxs-lookup"><span data-stu-id="2b3e9-331">Video Classes</span></span>](video-classes.md)
</dt> </dl>

 

