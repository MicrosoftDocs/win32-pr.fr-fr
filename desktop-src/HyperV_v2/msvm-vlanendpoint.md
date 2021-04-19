---
description: Représente le point de terminaison VLAN d’un port de commutateur.
ms.assetid: 82F2EC39-0C9C-4A9D-A6C4-1543A62A341D
title: Classe Msvm_VLANEndpoint
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VLANEndpoint
- Msvm_VLANEndpoint.InstanceID
- Msvm_VLANEndpoint.Caption
- Msvm_VLANEndpoint.Description
- Msvm_VLANEndpoint.ElementName
- Msvm_VLANEndpoint.InstallDate
- Msvm_VLANEndpoint.Name
- Msvm_VLANEndpoint.OperationalStatus
- Msvm_VLANEndpoint.StatusDescriptions
- Msvm_VLANEndpoint.Status
- Msvm_VLANEndpoint.HealthState
- Msvm_VLANEndpoint.CommunicationStatus
- Msvm_VLANEndpoint.DetailedStatus
- Msvm_VLANEndpoint.OperatingStatus
- Msvm_VLANEndpoint.PrimaryStatus
- Msvm_VLANEndpoint.EnabledState
- Msvm_VLANEndpoint.OtherEnabledState
- Msvm_VLANEndpoint.RequestedState
- Msvm_VLANEndpoint.EnabledDefault
- Msvm_VLANEndpoint.TimeOfLastStateChange
- Msvm_VLANEndpoint.AvailableRequestedStates
- Msvm_VLANEndpoint.TransitioningToState
- Msvm_VLANEndpoint.SystemCreationClassName
- Msvm_VLANEndpoint.SystemName
- Msvm_VLANEndpoint.CreationClassName
- Msvm_VLANEndpoint.NameFormat
- Msvm_VLANEndpoint.ProtocolType
- Msvm_VLANEndpoint.ProtocolIFType
- Msvm_VLANEndpoint.OtherTypeDescription
- Msvm_VLANEndpoint.DesiredEndpointMode
- Msvm_VLANEndpoint.OtherEndpointMode
- Msvm_VLANEndpoint.OperationalEndpointMode
- Msvm_VLANEndpoint.DesiredVLANTrunkEncapsulation
- Msvm_VLANEndpoint.OtherTrunkEncapsulation
- Msvm_VLANEndpoint.OperationalVLANTrunkEncapsulation
- Msvm_VLANEndpoint.GVRPStatus
- Msvm_VLANEndpoint.SupportedEndpointModes
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5606e18fd1327f17feaac07570e5bf8c0c8eb59d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544619"
---
# <a name="msvm_vlanendpoint-class"></a><span data-ttu-id="6798f-103">MSVM \_ VLANEndpoint, classe</span><span class="sxs-lookup"><span data-stu-id="6798f-103">Msvm\_VLANEndpoint class</span></span>

<span data-ttu-id="6798f-104">Représente le point de terminaison VLAN d’un port de commutateur.</span><span class="sxs-lookup"><span data-stu-id="6798f-104">Represents the VLAN endpoint of a switch port.</span></span> <span data-ttu-id="6798f-105">La configuration de ce point de terminaison modifiera la façon dont le port commuté envoie les paquets VLAN via le commutateur.</span><span class="sxs-lookup"><span data-stu-id="6798f-105">The configuration of this endpoint will change the way the switch port sends VLAN packets through the switch.</span></span>

<span data-ttu-id="6798f-106">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="6798f-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6798f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6798f-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VLANEndpoint : CIM_VLANEndpoint
{
  string   InstanceID;
  String   Caption = "VLAN Endpoint";
  string   Description = "Microsoft VLAN Endpoint";
  String   ElementName;
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
  String   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_VirtualSwitch";
  string   SystemName;
  String   CreationClassName = "Msvm_VLANEndpoint";
  String   NameFormat;
  uint16   ProtocolType;
  uint16   ProtocolIFType = 1;
  String   OtherTypeDescription = "Virtual Ethernet";
  uint16   DesiredEndpointMode;
  string   OtherEndpointMode;
  uint16   OperationalEndpointMode;
  uint16   DesiredVLANTrunkEncapsulation;
  string   OtherTrunkEncapsulation;
  uint16   OperationalVLANTrunkEncapsulation;
  uint16   GVRPStatus;
  uint16   SupportedEndpointModes[];
};
```

## <a name="members"></a><span data-ttu-id="6798f-108">Membres</span><span class="sxs-lookup"><span data-stu-id="6798f-108">Members</span></span>

<span data-ttu-id="6798f-109">La classe **MSVM \_ VLANEndpoint** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="6798f-109">The **Msvm\_VLANEndpoint** class has these types of members:</span></span>

-   [<span data-ttu-id="6798f-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="6798f-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="6798f-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6798f-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6798f-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="6798f-112">Methods</span></span>

<span data-ttu-id="6798f-113">La classe **MSVM \_ VLANEndpoint** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="6798f-113">The **Msvm\_VLANEndpoint** class has these methods.</span></span>



| <span data-ttu-id="6798f-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="6798f-114">Method</span></span>                                                             | <span data-ttu-id="6798f-115">Description</span><span class="sxs-lookup"><span data-stu-id="6798f-115">Description</span></span>                         |
|:-------------------------------------------------------------------|:------------------------------------|
| [<span data-ttu-id="6798f-116">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="6798f-116">**RequestStateChange**</span></span>](msvm-vlanendpoint-requeststatechange.md) | <span data-ttu-id="6798f-117">Demande un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="6798f-117">Requests a state change.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="6798f-118">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6798f-118">Properties</span></span>

<span data-ttu-id="6798f-119">La classe **MSVM \_ VLANEndpoint** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="6798f-119">The **Msvm\_VLANEndpoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6798f-120">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="6798f-120">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6798f-121">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6798f-121">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="6798f-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6798f-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6798f-123">Indique les valeurs possibles pour le paramètre *RequestedState* de la méthode [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) utilisée pour initier un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="6798f-123">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="6798f-124">Les valeurs répertoriées sont un sous-ensemble des valeurs contenues dans la propriété **RequestedStatesSupported** de l’instance associée de la **\_ EnabledLogicalElementCapabilities CIM**, où les valeurs sélectionnées sont une fonction de l’état actuel du [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6798f-124">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="6798f-125">Cette propriété peut être non **null** si une implémentation est en mesure de publier l’ensemble de valeurs possibles en tant que fonction de l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="6798f-125">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="6798f-126">Cette propriété a la **valeur null** si une implémentation ne peut pas déterminer le jeu de valeurs possibles en tant que fonction de l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="6798f-126">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="6798f-127">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6798f-127">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="6798f-128"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (2)</span><span class="sxs-lookup"><span data-stu-id="6798f-128"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="6798f-129"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (3)</span><span class="sxs-lookup"><span data-stu-id="6798f-129"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="6798f-130"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Arrêter** (4)</span><span class="sxs-lookup"><span data-stu-id="6798f-130"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="6798f-131"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Hors connexion** (6)</span><span class="sxs-lookup"><span data-stu-id="6798f-131"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="6798f-132"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="6798f-132"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="6798f-133"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Différer** (8)</span><span class="sxs-lookup"><span data-stu-id="6798f-133"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="6798f-134"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Suspension** (9)</span><span class="sxs-lookup"><span data-stu-id="6798f-134"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="6798f-135"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Redémarrer** (10)</span><span class="sxs-lookup"><span data-stu-id="6798f-135"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="6798f-136"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Réinitialiser** (11)</span><span class="sxs-lookup"><span data-stu-id="6798f-136"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="6798f-137"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF réservé** (..</span><span class="sxs-lookup"><span data-stu-id="6798f-137"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="6798f-138">)</span><span class="sxs-lookup"><span data-stu-id="6798f-138">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6798f-139">**Caption**</span><span class="sxs-lookup"><span data-stu-id="6798f-139">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6798f-140">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6798f-140">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="6798f-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6798f-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6798f-142">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6798f-142">A short description of the object.</span></span> <span data-ttu-id="6798f-143">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « point de terminaison VLAN ».</span><span class="sxs-lookup"><span data-stu-id="6798f-143">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "VLAN Endpoint".</span></span>

</dd> <dt>

<span data-ttu-id="6798f-144">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="6798f-144">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6798f-145">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6798f-145">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6798f-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6798f-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6798f-147">Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="6798f-147">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="6798f-148">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="6798f-148">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="6798f-149">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="6798f-149">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="6798f-150">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="6798f-150">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6798f-151">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6798f-151">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="6798f-152">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6798f-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6798f-153">Nom de la classe ou de la sous-classe utilisée lors de la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="6798f-153">The name of the class or the subclass used in the creation of an instance.</span></span> <span data-ttu-id="6798f-154">Cette propriété est héritée de [**CIM \_ ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)et est toujours définie sur « MSVM \_ VLANEndpoint ».</span><span class="sxs-lookup"><span data-stu-id="6798f-154">This property is inherited from [**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint), and it is always set to "Msvm\_VLANEndpoint".</span></span>

</dd> <dt>

<span data-ttu-id="6798f-155">**Description**</span><span class="sxs-lookup"><span data-stu-id="6798f-155">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6798f-156">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6798f-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6798f-157">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6798f-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6798f-158">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="6798f-158">A description of the object.</span></span> <span data-ttu-id="6798f-159">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « point de terminaison VLAN Microsoft ».</span><span class="sxs-lookup"><span data-stu-id="6798f-159">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft VLAN Endpoint".</span></span>

</dd> <dt>

<span data-ttu-id="6798f-160">**DesiredEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="6798f-160">**DesiredEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6798f-161">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6798f-161">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6798f-162">Type d’accès : écriture seule</span><span class="sxs-lookup"><span data-stu-id="6798f-162">Access type: Write-only</span></span>
</dt> </dl>

<span data-ttu-id="6798f-163">Mode VLAN requis pour l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="6798f-163">The desired VLAN mode that is requested for use.</span></span> <span data-ttu-id="6798f-164">Le mode actuel est fourni par la propriété **OperationalEndpointMode** .</span><span class="sxs-lookup"><span data-stu-id="6798f-164">The current mode is given by the **OperationalEndpointMode** property.</span></span> <span data-ttu-id="6798f-165">Cette propriété est héritée de la [**\_ VLANEndpoint CIM**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span><span class="sxs-lookup"><span data-stu-id="6798f-165">This property is inherited from [**CIM\_VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span></span>



| <span data-ttu-id="6798f-166">Valeur</span><span class="sxs-lookup"><span data-stu-id="6798f-166">Value</span></span>                                                                                                                                                                                                                                                                     | <span data-ttu-id="6798f-167">Signification</span><span class="sxs-lookup"><span data-stu-id="6798f-167">Meaning</span></span>                                                                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="6798f-168"><dt>**DMTF réservé**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6798f-168"><dt>**DMTF Reserved**</dt> <dt>0</dt></span></span> </dl>                       |                                                                                                                                                                                                                                                                                  |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="6798f-169"><dt>**Autre**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="6798f-169"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                       |                                                                                                                                                                                                                                                                                  |
| <span id="Access"></span><span id="access"></span><span id="ACCESS"></span><dl> <span data-ttu-id="6798f-170"><dt>**Access**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="6798f-170"><dt>**Access**</dt> <dt>2</dt></span></span> </dl>                                                   | <span data-ttu-id="6798f-171">Place le point de terminaison/port de commutateur en mode non Trunking permanent et négocie pour convertir le lien en un lien non-Trunk.</span><span class="sxs-lookup"><span data-stu-id="6798f-171">Puts the endpoint/switch port into permanent nontrunking mode and negotiates to convert the link into a nontrunk link.</span></span> <span data-ttu-id="6798f-172">Le point de terminaison devient une interface qui n’est pas un Trunk.</span><span class="sxs-lookup"><span data-stu-id="6798f-172">The endpoint becomes a nontrunk interface.</span></span><br/>                                                                                                     |
| <span id="Dynamic_Auto"></span><span id="dynamic_auto"></span><span id="DYNAMIC_AUTO"></span><dl> <span data-ttu-id="6798f-173"><dt>**Dynamique automatique**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="6798f-173"><dt>**Dynamic Auto**</dt> <dt>3</dt></span></span> </dl>                           | <span data-ttu-id="6798f-174">Permet au point de terminaison de convertir le lien en lien Trunk.</span><span class="sxs-lookup"><span data-stu-id="6798f-174">Makes the endpoint able to convert the link to a trunk link.</span></span> <span data-ttu-id="6798f-175">Le point de terminaison devient une interface Trunk si l’interface voisine est définie en mode Trunk ou désirable.</span><span class="sxs-lookup"><span data-stu-id="6798f-175">The endpoint becomes a trunk interface if the neighboring interface is set to trunk or desirable mode.</span></span><br/>                                                                                                   |
| <span id="Dynamic_Desirable"></span><span id="dynamic_desirable"></span><span id="DYNAMIC_DESIRABLE"></span><dl> <span data-ttu-id="6798f-176"><dt>**Désirable dynamique**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="6798f-176"><dt>**Dynamic Desirable**</dt> <dt>4</dt></span></span> </dl>       | <span data-ttu-id="6798f-177">Fait en sorte que le point de terminaison tente activement de convertir le lien en lien Trunk.</span><span class="sxs-lookup"><span data-stu-id="6798f-177">Makes the endpoint actively attempt to convert the link to a trunk link.</span></span> <span data-ttu-id="6798f-178">Le point de terminaison devient une interface Trunk si l’interface voisine est définie en mode Trunk, désirable ou auto.</span><span class="sxs-lookup"><span data-stu-id="6798f-178">The endpoint becomes a trunk interface if the neighboring interface is set to trunk, desirable, or auto mode.</span></span> <span data-ttu-id="6798f-179">Le mode de port commuté par défaut pour toutes les interfaces Ethernet est souhaitable dynamiquement.</span><span class="sxs-lookup"><span data-stu-id="6798f-179">The default switch-port mode for all Ethernet interfaces is dynamic desirable.</span></span><br/> |
| <span id="Trunk"></span><span id="trunk"></span><span id="TRUNK"></span><dl> <span data-ttu-id="6798f-180"><dt>**Trunk**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="6798f-180"><dt>**Trunk**</dt> <dt>5</dt></span></span> </dl>                                                       | <span data-ttu-id="6798f-181">Place le point de terminaison en mode Trunking permanent et négocie pour convertir le lien en lien Trunk.</span><span class="sxs-lookup"><span data-stu-id="6798f-181">Puts the endpoint into permanent trunking mode and negotiates to convert the link into a trunk link.</span></span> <span data-ttu-id="6798f-182">Le point de terminaison devient une interface Trunk même si l’interface voisine n’est pas une interface Trunk.</span><span class="sxs-lookup"><span data-stu-id="6798f-182">The endpoint becomes a trunk interface even if the neighboring interface is not a trunk interface.</span></span><br/>                                                               |
| <span id="Dot1Q_Tunnel"></span><span id="dot1q_tunnel"></span><span id="DOT1Q_TUNNEL"></span><dl> <span data-ttu-id="6798f-183"><dt>**Tunnel Dot1Q**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="6798f-183"><dt>**Dot1Q Tunnel**</dt> <dt>6</dt></span></span> </dl>                           | <span data-ttu-id="6798f-184">Configure l’interface en tant que point de terminaison/port (sans Trunking) de tunnel à connecter dans un lien asymétrique avec un port 802.1 Q Trunk.</span><span class="sxs-lookup"><span data-stu-id="6798f-184">Configures the interface as a tunnel (nontrunking) endpoint/port to be connected in an asymmetric link with an 802.1Q trunk port.</span></span> <span data-ttu-id="6798f-185">le tunneling 802.1 q est utilisé pour maintenir l’intégrité VLAN du client sur un réseau de fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="6798f-185">802.1Q tunneling is used to maintain customer VLAN integrity across a service provider network.</span></span><br/>                                     |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="6798f-186"><dt>**DMTF réservé**</dt> <dt>7 32767</dt></span><span class="sxs-lookup"><span data-stu-id="6798f-186"><dt>**DMTF Reserved**</dt> <dt>7 32767</dt></span></span> </dl>                 |                                                                                                                                                                                                                                                                                  |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="6798f-187"><dt> **Fournisseur réservé**</dt> <dt>32768 65535</dt></span><span class="sxs-lookup"><span data-stu-id="6798f-187"><dt>**Vendor Reserved** </dt> <dt>32768 65535</dt></span></span> </dl> |                                                                                                                                                                                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="6798f-188">**DesiredVLANTrunkEncapsulation**</span><span class="sxs-lookup"><span data-stu-id="6798f-188">**DesiredVLANTrunkEncapsulation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6798f-189">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6798f-189">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6798f-190">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6798f-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6798f-191">Type d’encapsulation de réseau local virtuel qui est demandé pour l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="6798f-191">The type of VLAN encapsulation that is requested for use.</span></span> <span data-ttu-id="6798f-192">L’encapsulation en cours d’utilisation est donnée par la propriété **OperationalVLANTrunkEncapsulation** .</span><span class="sxs-lookup"><span data-stu-id="6798f-192">The encapsulation currently in use is given by the **OperationalVLANTrunkEncapsulation** property.</span></span> <span data-ttu-id="6798f-193">Cette propriété s’applique uniquement lorsque le point de terminaison fonctionne en mode Trunking (pour plus d’informations, consultez la propriété **OperationalEndpointMode** ).</span><span class="sxs-lookup"><span data-stu-id="6798f-193">This property is only applicable when the endpoint is operating in a trunking mode (see the **OperationalEndpointMode** property for additional details).</span></span> <span data-ttu-id="6798f-194">Cette propriété a la valeur 2 (non applicable) (autrement dit, le point de terminaison ne sera jamais placé en mode Trunking), un type particulier (802.1 Q ou Cisco ISL) ou 5 (Negotiate) (autrement dit, le résultat de la négociation entre cette interface et son voisin).</span><span class="sxs-lookup"><span data-stu-id="6798f-194">This property is either 2 (Not Applicable) (that is, the endpoint will never be placed in a trunking mode), a particular type (802.1Q or Cisco ISL), or 5 (Negotiate) (that is, the result of the negotiation between this interface and its neighbor).</span></span> <span data-ttu-id="6798f-195">La valeur, 5 (Negotiate) n’est pas autorisée si le point de terminaison ne prend pas en charge la négociation.</span><span class="sxs-lookup"><span data-stu-id="6798f-195">The value, 5 (Negotiate) is not allowed if the endpoint does not support negotiation.</span></span> <span data-ttu-id="6798f-196">Cette fonctionnalité dépend du matériel et des fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="6798f-196">This capability is hardware and vendor dependent.</span></span> <span data-ttu-id="6798f-197">Cette propriété est héritée de la [**\_ VLANEndpoint CIM**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span><span class="sxs-lookup"><span data-stu-id="6798f-197">This property is inherited from [**CIM\_VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span></span>

<dl> <dt>

<span data-ttu-id="6798f-198"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (0)</span><span class="sxs-lookup"><span data-stu-id="6798f-198"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6798f-199"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="6798f-199"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="6798f-200"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (2)</span><span class="sxs-lookup"><span data-stu-id="6798f-200"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (2)</span></span>
</dt> <dt>

<span data-ttu-id="6798f-201"><span id="802.1Q"></span><span id="802.1q"></span>**802.1 q** (3)</span><span class="sxs-lookup"><span data-stu-id="6798f-201"><span id="802.1Q"></span><span id="802.1q"></span>**802.1Q** (3)</span></span>
</dt> <dt>

<span data-ttu-id="6798f-202"><span id="Cisco_ISL"></span><span id="cisco_isl"></span><span id="CISCO_ISL"></span>**Cisco ISL** (4)</span><span class="sxs-lookup"><span data-stu-id="6798f-202"><span id="Cisco_ISL"></span><span id="cisco_isl"></span><span id="CISCO_ISL"></span>**Cisco ISL** (4)</span></span>
</dt> <dt>

<span data-ttu-id="6798f-203"><span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>**Négocier** (5)</span><span class="sxs-lookup"><span data-stu-id="6798f-203"><span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>**Negotiate** (5)</span></span>
</dt> <dt>

<span data-ttu-id="6798f-204"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (6 32767)</span><span class="sxs-lookup"><span data-stu-id="6798f-204"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (6 32767)</span></span>
</dt> <dt>

<span data-ttu-id="6798f-205"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (32768 65535)</span><span class="sxs-lookup"><span data-stu-id="6798f-205"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (32768 65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6798f-206">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="6798f-206">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6798f-207">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6798f-207">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6798f-208">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6798f-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6798f-209">Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="6798f-209">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="6798f-210">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="6798f-210">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="6798f-211">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="6798f-211">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="6798f-212">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="6798f-212">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6798f-213">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6798f-213">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="6798f-214">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6798f-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6798f-215">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6798f-215">A display name for the object.</span></span> <span data-ttu-id="6798f-216">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="6798f-216">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="6798f-217">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="6798f-217">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6798f-218">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6798f-218">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6798f-219">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6798f-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6798f-220">Configuration par défaut ou de démarrage d’un administrateur pour l’état activé d’un élément.</span><span class="sxs-lookup"><span data-stu-id="6798f-220">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="6798f-221">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) et a toujours la valeur 2 (activé).</span><span class="sxs-lookup"><span data-stu-id="6798f-221">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="6798f-222">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="6798f-222">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6798f-223">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6798f-223">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6798f-224">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6798f-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6798f-225">États activés et désactivés de cet élément.</span><span class="sxs-lookup"><span data-stu-id="6798f-225">The enabled and disabled states of this element.</span></span> <span data-ttu-id="6798f-226">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est toujours définie sur 5 (non applicable).</span><span class="sxs-lookup"><span data-stu-id="6798f-226">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="6798f-227">**GVRPStatus**</span><span class="sxs-lookup"><span data-stu-id="6798f-227">**GVRPStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6798f-228">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6798f-228">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6798f-229">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6798f-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6798f-230">Indique si le protocole GVRP (GARP VLAN Registration Protocol) est activé ou désactivé sur le point de terminaison/port trunk.</span><span class="sxs-lookup"><span data-stu-id="6798f-230">Indicates whether GARP VLAN Registration Protocol (GVRP) is enabled or disabled on the trunk endpoint/port.</span></span> <span data-ttu-id="6798f-231">Cette propriété est 2 (non applicable) sauf si le GVRP est pris en charge par le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="6798f-231">This property is 2 (Not Applicable) unless GVRP is supported by the endpoint.</span></span> <span data-ttu-id="6798f-232">Cette propriété s’applique uniquement lorsque le point de terminaison fonctionne en mode Trunking (pour plus d’informations, consultez la propriété **OperationalEndpointMode** ).</span><span class="sxs-lookup"><span data-stu-id="6798f-232">This property is applicable only when the endpoint is operating in trunking mode (see the **OperationalEndpointMode** property for additional details).</span></span> <span data-ttu-id="6798f-233">Cette propriété est héritée de la [**\_ VLANEndpoint CIM**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span><span class="sxs-lookup"><span data-stu-id="6798f-233">This property is inherited from [**CIM\_VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span></span>

<dl> <dt>

<span data-ttu-id="6798f-234"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="6798f-234"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6798f-235"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (2)</span><span class="sxs-lookup"><span data-stu-id="6798f-235"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (2)</span></span>
</dt> <dt>

<span data-ttu-id="6798f-236"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="6798f-236"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="6798f-237"><span id="Disabled_"></span><span id="disabled_"></span><span id="DISABLED_"></span>**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="6798f-237"><span id="Disabled_"></span><span id="disabled_"></span><span id="DISABLED_"></span>**Disabled** (4 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6798f-238">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="6798f-238">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6798f-239">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6798f-239">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6798f-240">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6798f-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6798f-241">Intégrité actuelle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="6798f-241">The current health of the element.</span></span> <span data-ttu-id="6798f-242">Cette propriété exprime l’intégrité de cet élément, mais pas nécessairement celle de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="6798f-242">This property expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="6798f-243">Les valeurs possibles sont comprises entre 0 et 30, où 5 signifie que l’élément est entièrement sain et 30 signifie que l’élément est complètement non opérationnel.</span><span class="sxs-lookup"><span data-stu-id="6798f-243">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="6798f-244">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est toujours définie sur 5 (OK).</span><span class="sxs-lookup"><span data-stu-id="6798f-244">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="6798f-245">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="6798f-245">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6798f-246">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6798f-246">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6798f-247">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6798f-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6798f-248">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6798f-248">The date and time when the object was installed.</span></span> <span data-ttu-id="6798f-249">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="6798f-249">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6798f-250">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="6798f-250">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6798f-251">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6798f-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6798f-252">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6798f-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6798f-253">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="6798f-253">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="6798f-254">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="6798f-254">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="6798f-255">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="6798f-255">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="6798f-256">**Nom**</span><span class="sxs-lookup"><span data-stu-id="6798f-256">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6798f-257">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6798f-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6798f-258">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6798f-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6798f-259">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="6798f-259">The label by which the object is known.</span></span> <span data-ttu-id="6798f-260">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="6798f-260">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="6798f-261">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="6798f-261">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6798f-262">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6798f-262">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="6798f-263">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6798f-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6798f-264">L’heuristique d’attribution de noms qui est sélectionnée pour garantir que la valeur de la propriété **Name** est unique.</span><span class="sxs-lookup"><span data-stu-id="6798f-264">The naming heuristic that is selected to ensure that the value of the **Name** property is unique.</span></span> <span data-ttu-id="6798f-265">Cette propriété est héritée de l' [**\_ ProtocolEndpoint CIM**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint) et n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="6798f-265">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6798f-266">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="6798f-266">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6798f-267">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6798f-267">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6798f-268">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6798f-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6798f-269">Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="6798f-269">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="6798f-270">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="6798f-270">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="6798f-271">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="6798f-271">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="6798f-272">**OperationalEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="6798f-272">**OperationalEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6798f-273">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6798f-273">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6798f-274">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6798f-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6798f-275">Mode de configuration pour le point de terminaison de réseau local virtuel.</span><span class="sxs-lookup"><span data-stu-id="6798f-275">The configuration mode for the VLAN endpoint.</span></span> <span data-ttu-id="6798f-276">Cette propriété est héritée de la [**\_ VLANEndpoint CIM**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span><span class="sxs-lookup"><span data-stu-id="6798f-276">This property is inherited from [**CIM\_VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span></span>



| <span data-ttu-id="6798f-277">Valeur</span><span class="sxs-lookup"><span data-stu-id="6798f-277">Value</span></span>                                                                                                                                                                                                                                                                     | <span data-ttu-id="6798f-278">Signification</span><span class="sxs-lookup"><span data-stu-id="6798f-278">Meaning</span></span>                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="6798f-279"><dt>**DMTF réservé**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6798f-279"><dt>**DMTF Reserved**</dt> <dt>0</dt></span></span> </dl>                       |                                                                                                                                                                                                                                                                     |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="6798f-280"><dt>**Autre**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="6798f-280"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                       | <span data-ttu-id="6798f-281">Le point de terminaison ne prend pas en charge les réseaux locaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="6798f-281">The endpoint is not VLAN aware.</span></span><br/>                                                                                                                                                                                                                          |
| <span id="Access"></span><span id="access"></span><span id="ACCESS"></span><dl> <span data-ttu-id="6798f-282"><dt>**Access**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="6798f-282"><dt>**Access**</dt> <dt>2</dt></span></span> </dl>                                                   | <span data-ttu-id="6798f-283">Place le point de terminaison en mode non Trunking permanent et négocie pour convertir le lien en un lien non-Trunk.</span><span class="sxs-lookup"><span data-stu-id="6798f-283">Puts the endpoint into permanent nontrunking mode and negotiates to convert the link into a nontrunk link.</span></span> <span data-ttu-id="6798f-284">Le point de terminaison devient une interface qui n’est pas un Trunk.</span><span class="sxs-lookup"><span data-stu-id="6798f-284">The endpoint becomes a nontrunk interface.</span></span><br/>                                                                                                    |
| <span id="Dynamic_Auto"></span><span id="dynamic_auto"></span><span id="DYNAMIC_AUTO"></span><dl> <span data-ttu-id="6798f-285"><dt>**Dynamique automatique**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="6798f-285"><dt>**Dynamic Auto**</dt> <dt>3</dt></span></span> </dl>                           | <span data-ttu-id="6798f-286">Permet au point de terminaison de convertir le lien en lien Trunk.</span><span class="sxs-lookup"><span data-stu-id="6798f-286">Makes the endpoint able to convert the link to a trunk link.</span></span> <span data-ttu-id="6798f-287">Le point de terminaison devient une interface Trunk si l’interface voisine est définie en mode Trunk ou désirable.</span><span class="sxs-lookup"><span data-stu-id="6798f-287">The endpoint becomes a trunk interface if the neighboring interface is set to trunk or desirable mode.</span></span><br/>                                                                                      |
| <span id="Dynamic_Desirable"></span><span id="dynamic_desirable"></span><span id="DYNAMIC_DESIRABLE"></span><dl> <span data-ttu-id="6798f-288"><dt>**Désirable dynamique**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="6798f-288"><dt>**Dynamic Desirable**</dt> <dt>4</dt></span></span> </dl>       | <span data-ttu-id="6798f-289">Fait en sorte que le point de terminaison tente activement de convertir le lien en lien Trunk.</span><span class="sxs-lookup"><span data-stu-id="6798f-289">Makes the endpoint actively attempt to convert the link to a trunk link.</span></span> <span data-ttu-id="6798f-290">Le point de terminaison devient une interface Trunk si l’interface voisine est définie en mode Trunk, désirable ou auto.</span><span class="sxs-lookup"><span data-stu-id="6798f-290">The endpoint becomes a trunk interface if the neighboring interface is set to trunk, desirable, or auto mode.</span></span> <span data-ttu-id="6798f-291">Il s’agit du mode de port commuté par défaut pour toutes les interfaces Ethernet.</span><span class="sxs-lookup"><span data-stu-id="6798f-291">This is the default switch-port mode for all Ethernet interfaces.</span></span><br/> |
| <span id="Trunk"></span><span id="trunk"></span><span id="TRUNK"></span><dl> <span data-ttu-id="6798f-292"><dt>**Trunk**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="6798f-292"><dt>**Trunk**</dt> <dt>5</dt></span></span> </dl>                                                       | <span data-ttu-id="6798f-293">Place le point de terminaison en mode Trunking permanent et négocie pour convertir le lien en lien Trunk.</span><span class="sxs-lookup"><span data-stu-id="6798f-293">Puts the endpoint into permanent trunking mode and negotiates to convert the link into a trunk link.</span></span> <span data-ttu-id="6798f-294">Le point de terminaison devient une interface Trunk même si l’interface voisine n’est pas une interface Trunk.</span><span class="sxs-lookup"><span data-stu-id="6798f-294">The endpoint becomes a trunk interface even if the neighboring interface is not a trunk interface.</span></span><br/>                                                  |
| <span id="Dot1Q_Tunnel"></span><span id="dot1q_tunnel"></span><span id="DOT1Q_TUNNEL"></span><dl> <span data-ttu-id="6798f-295"><dt>**Tunnel Dot1Q**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="6798f-295"><dt>**Dot1Q Tunnel**</dt> <dt>6</dt></span></span> </dl>                           | <span data-ttu-id="6798f-296">Configure l’interface en tant que point de terminaison/port (sans Trunking) de tunnel à connecter dans un lien asymétrique avec un port 802.1 Q Trunk.</span><span class="sxs-lookup"><span data-stu-id="6798f-296">Configures the interface as a tunnel (nontrunking) endpoint/port to be connected in an asymmetric link with an 802.1Q trunk port.</span></span> <span data-ttu-id="6798f-297">le tunneling 802.1 q est utilisé pour maintenir l’intégrité VLAN du client sur un réseau de fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="6798f-297">802.1Q tunneling is used to maintain customer VLAN integrity across a service provider network.</span></span><br/>                        |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="6798f-298"><dt>**DMTF réservé**</dt> <dt>7 32767</dt></span><span class="sxs-lookup"><span data-stu-id="6798f-298"><dt>**DMTF Reserved**</dt> <dt>7 32767</dt></span></span> </dl>                 |                                                                                                                                                                                                                                                                     |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="6798f-299"><dt> **Fournisseur réservé**</dt> <dt>32768 65535</dt></span><span class="sxs-lookup"><span data-stu-id="6798f-299"><dt>**Vendor Reserved** </dt> <dt>32768 65535</dt></span></span> </dl> |                                                                                                                                                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="6798f-300">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="6798f-300">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6798f-301">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6798f-301">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="6798f-302">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6798f-302">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6798f-303">États actuels de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6798f-303">The current statuses of the object.</span></span> <span data-ttu-id="6798f-304">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), et chaque élément de tableau a toujours la valeur 2 (OK).</span><span class="sxs-lookup"><span data-stu-id="6798f-304">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="6798f-305">**OperationalVLANTrunkEncapsulation**</span><span class="sxs-lookup"><span data-stu-id="6798f-305">**OperationalVLANTrunkEncapsulation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6798f-306">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6798f-306">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6798f-307">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6798f-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6798f-308">Type d’encapsulation VLAN en cours d’utilisation sur un point de terminaison/port trunk.</span><span class="sxs-lookup"><span data-stu-id="6798f-308">The type of VLAN encapsulation in use on a trunk endpoint/port.</span></span> <span data-ttu-id="6798f-309">Cette propriété a la valeur 2 (non applicable) (autrement dit, le point de terminaison ne fonctionne pas en mode Trunking), un type particulier (3-802.1 Q ou 4-Cisco ISL), 5 (Negotiate) (autrement dit, les points de terminaison négocient le type d’encapsulation).</span><span class="sxs-lookup"><span data-stu-id="6798f-309">This property is either 2 (Not Applicable) (that is, the endpoint is not operating in trunking mode), a particular type (3 - 802.1Q or 4 - Cisco ISL), 5 (Negotiate) (that is, the endpoints are negotiating the encapsulation type).</span></span> <span data-ttu-id="6798f-310">Cette propriété s’applique uniquement lorsque le point de terminaison fonctionne en mode Trunking (pour plus d’informations, consultez la propriété **OperationalEndpointMode** ).</span><span class="sxs-lookup"><span data-stu-id="6798f-310">This property is only applicable when the endpoint is operating in a trunking mode (see the **OperationalEndpointMode** property for additional details).</span></span> <span data-ttu-id="6798f-311">Cette propriété est héritée de la [**\_ VLANEndpoint CIM**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span><span class="sxs-lookup"><span data-stu-id="6798f-311">This property is inherited from [**CIM\_VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span></span>

<dl> <dt>

<span data-ttu-id="6798f-312"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="6798f-312"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6798f-313"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="6798f-313"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="6798f-314"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (2)</span><span class="sxs-lookup"><span data-stu-id="6798f-314"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (2)</span></span>
</dt> <dt>

<span data-ttu-id="6798f-315"><span id="802.1Q"></span><span id="802.1q"></span>**802.1 q** (3)</span><span class="sxs-lookup"><span data-stu-id="6798f-315"><span id="802.1Q"></span><span id="802.1q"></span>**802.1Q** (3)</span></span>
</dt> <dt>

<span data-ttu-id="6798f-316"><span id="Cisco_ISL"></span><span id="cisco_isl"></span><span id="CISCO_ISL"></span>**Cisco ISL** (4)</span><span class="sxs-lookup"><span data-stu-id="6798f-316"><span id="Cisco_ISL"></span><span id="cisco_isl"></span><span id="CISCO_ISL"></span>**Cisco ISL** (4)</span></span>
</dt> <dt>

<span data-ttu-id="6798f-317"><span id="Negotiating"></span><span id="negotiating"></span><span id="NEGOTIATING"></span>**Négociation** (5)</span><span class="sxs-lookup"><span data-stu-id="6798f-317"><span id="Negotiating"></span><span id="negotiating"></span><span id="NEGOTIATING"></span>**Negotiating** (5)</span></span>
</dt> <dt>

<span data-ttu-id="6798f-318"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (6 32767)</span><span class="sxs-lookup"><span data-stu-id="6798f-318"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (6 32767)</span></span>
</dt> <dt>

<span data-ttu-id="6798f-319"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (32768 65535)</span><span class="sxs-lookup"><span data-stu-id="6798f-319"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (32768 65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6798f-320">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="6798f-320">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6798f-321">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6798f-321">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="6798f-322">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6798f-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6798f-323">Chaîne qui décrit l’état activé ou désactivé de l’élément lorsque la propriété **EnabledState** a la valeur 1 (« other »).</span><span class="sxs-lookup"><span data-stu-id="6798f-323">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="6798f-324">Cette propriété doit avoir la valeur **null** quand **EnabledState** a une valeur autre que 1.</span><span class="sxs-lookup"><span data-stu-id="6798f-324">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="6798f-325">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="6798f-325">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="6798f-326">**OtherEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="6798f-326">**OtherEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6798f-327">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6798f-327">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6798f-328">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6798f-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6798f-329">Type de modèle de point de terminaison VLAN pris en charge par ce point de terminaison VLAN, lorsque la valeur de la propriété **OperationalEndpointMode** est définie sur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="6798f-329">The type of VLAN endpoint model that is supported by this VLAN endpoint, when the value of the **OperationalEndpointMode** property is set to 1 (Other).</span></span> <span data-ttu-id="6798f-330">Cette propriété doit être définie sur **null** lorsque la propriété **OperationalEndpointMode** a une valeur autre que 1.</span><span class="sxs-lookup"><span data-stu-id="6798f-330">This property should be set to **Null** when the **OperationalEndpointMode** property is any value other than 1.</span></span> <span data-ttu-id="6798f-331">Cette propriété est héritée de la [**\_ VLANEndpoint CIM**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span><span class="sxs-lookup"><span data-stu-id="6798f-331">This property is inherited from [**CIM\_VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span></span>

</dd> <dt>

<span data-ttu-id="6798f-332">**OtherTrunkEncapsulation**</span><span class="sxs-lookup"><span data-stu-id="6798f-332">**OtherTrunkEncapsulation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6798f-333">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6798f-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6798f-334">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6798f-334">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6798f-335">Type d’encapsulation VLAN pris en charge par ce point de terminaison VLAN, lorsque la valeur de la propriété **OperationalVLANTrunkEncapsulation** est définie sur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="6798f-335">The type of VLAN encapsulation that is supported by this VLAN endpoint, when the value of the **OperationalVLANTrunkEncapsulation** property is set to 1 (Other).</span></span> <span data-ttu-id="6798f-336">Cette propriété doit être définie sur **null** lorsque la propriété d’encapsulation souhaitée est toute valeur autre que 1.</span><span class="sxs-lookup"><span data-stu-id="6798f-336">This property should be set to **Null** when the desired encapsulation property is any value other than 1.</span></span> <span data-ttu-id="6798f-337">Cette propriété est héritée de la [**\_ VLANEndpoint CIM**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span><span class="sxs-lookup"><span data-stu-id="6798f-337">This property is inherited from [**CIM\_VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span></span>

</dd> <dt>

<span data-ttu-id="6798f-338">**OtherTypeDescription**</span><span class="sxs-lookup"><span data-stu-id="6798f-338">**OtherTypeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6798f-339">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6798f-339">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="6798f-340">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6798f-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6798f-341">Type de point de terminaison de protocole lorsque la propriété **type** de cette classe (ou de l’une de ses sous-classes) est définie sur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="6798f-341">The type of protocol endpoint when the **Type** property of this class (or any of its subclasses) is set to 1 (Other).</span></span> <span data-ttu-id="6798f-342">Cette propriété est héritée de l' [**\_ ProtocolEndpoint CIM**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint)et est toujours définie sur « Ethernet virtuel ».</span><span class="sxs-lookup"><span data-stu-id="6798f-342">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint), and it is always set to "Virtual Ethernet".</span></span>

</dd> <dt>

<span data-ttu-id="6798f-343">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="6798f-343">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6798f-344">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6798f-344">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6798f-345">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6798f-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6798f-346">Fournit des informations d’état de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="6798f-346">Provides high level status information.</span></span> <span data-ttu-id="6798f-347">Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir des informations d’état d’intégrité de haut niveau et détaillées pour l’élément et ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="6798f-347">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="6798f-348">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="6798f-348">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="6798f-349">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="6798f-349">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="6798f-350">**ProtocolIFType**</span><span class="sxs-lookup"><span data-stu-id="6798f-350">**ProtocolIFType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6798f-351">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6798f-351">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6798f-352">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6798f-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6798f-353">[MIB IfType IANA](https://www.iana.org/assignments/ianaiftype-mib).</span><span class="sxs-lookup"><span data-stu-id="6798f-353">The [IANA ifType MIB](https://www.iana.org/assignments/ianaiftype-mib).</span></span> <span data-ttu-id="6798f-354">Cette propriété est héritée de l' [**\_ ProtocolEndpoint CIM**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint)et est toujours définie sur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="6798f-354">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint), and it is always set to 1 (Other).</span></span>

</dd> <dt>

<span data-ttu-id="6798f-355">**ProtocolType**</span><span class="sxs-lookup"><span data-stu-id="6798f-355">**ProtocolType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6798f-356">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6798f-356">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6798f-357">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6798f-357">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6798f-358">Cette propriété est héritée de l' [**\_ ProtocolEndpoint CIM**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint) et n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="6798f-358">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6798f-359">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="6798f-359">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6798f-360">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6798f-360">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6798f-361">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6798f-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6798f-362">Dernier État demandé ou souhaité pour le service de gestion.</span><span class="sxs-lookup"><span data-stu-id="6798f-362">The last requested or desired state for the management service.</span></span> <span data-ttu-id="6798f-363">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur 12 (non applicable).</span><span class="sxs-lookup"><span data-stu-id="6798f-363">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>



| <span data-ttu-id="6798f-364">Valeur</span><span class="sxs-lookup"><span data-stu-id="6798f-364">Value</span></span>                                                                         | <span data-ttu-id="6798f-365">Signification</span><span class="sxs-lookup"><span data-stu-id="6798f-365">Meaning</span></span>                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="6798f-366"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="6798f-366"><dt>12</dt></span></span> </dl> | <span data-ttu-id="6798f-367">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="6798f-367">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6798f-368">**État**</span><span class="sxs-lookup"><span data-stu-id="6798f-368">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6798f-369">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6798f-369">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6798f-370">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6798f-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6798f-371">Décrit l’état de l’élément.</span><span class="sxs-lookup"><span data-stu-id="6798f-371">Describes the status of the element.</span></span> <span data-ttu-id="6798f-372">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="6798f-372">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="6798f-373">OK</span><span class="sxs-lookup"><span data-stu-id="6798f-373">"OK"</span></span>

<span data-ttu-id="6798f-374">Erreurs</span><span class="sxs-lookup"><span data-stu-id="6798f-374">"Error"</span></span>

<span data-ttu-id="6798f-375">Détérioré</span><span class="sxs-lookup"><span data-stu-id="6798f-375">"Degraded"</span></span>

<span data-ttu-id="6798f-376">Connue</span><span class="sxs-lookup"><span data-stu-id="6798f-376">"Unknown"</span></span>

<span data-ttu-id="6798f-377">« Échec prévu »</span><span class="sxs-lookup"><span data-stu-id="6798f-377">"Pred Fail"</span></span>

<span data-ttu-id="6798f-378">Démarr</span><span class="sxs-lookup"><span data-stu-id="6798f-378">"Starting"</span></span>

<span data-ttu-id="6798f-379">Arrêt</span><span class="sxs-lookup"><span data-stu-id="6798f-379">"Stopping"</span></span>

<span data-ttu-id="6798f-380">Services</span><span class="sxs-lookup"><span data-stu-id="6798f-380">"Service"</span></span>

<span data-ttu-id="6798f-381">Trop sollicité</span><span class="sxs-lookup"><span data-stu-id="6798f-381">"Stressed"</span></span>

<span data-ttu-id="6798f-382">« Non récupéré »</span><span class="sxs-lookup"><span data-stu-id="6798f-382">"NonRecover"</span></span>

<span data-ttu-id="6798f-383">« Aucun contact »</span><span class="sxs-lookup"><span data-stu-id="6798f-383">"No Contact"</span></span>

<span data-ttu-id="6798f-384">« Comm. perdue »</span><span class="sxs-lookup"><span data-stu-id="6798f-384">"Lost Comm"</span></span>

</dd> <dt>

<span data-ttu-id="6798f-385">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="6798f-385">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6798f-386">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="6798f-386">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6798f-387">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6798f-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6798f-388">Chaînes qui décrivent les différentes valeurs de tableau **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="6798f-388">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="6798f-389">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), et chaque élément de tableau est toujours défini sur « OK ».</span><span class="sxs-lookup"><span data-stu-id="6798f-389">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="6798f-390">**SupportedEndpointModes**</span><span class="sxs-lookup"><span data-stu-id="6798f-390">**SupportedEndpointModes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6798f-391">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6798f-391">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="6798f-392">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6798f-392">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6798f-393">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexé")</span><span class="sxs-lookup"><span data-stu-id="6798f-393">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="6798f-394">Modes de point de terminaison pris en charge par ce port.</span><span class="sxs-lookup"><span data-stu-id="6798f-394">The endpoint modes supported by this port.</span></span>

</dd> <dt>

<span data-ttu-id="6798f-395">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="6798f-395">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6798f-396">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6798f-396">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6798f-397">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6798f-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6798f-398">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="6798f-398">The creation class name of the scoping system.</span></span> <span data-ttu-id="6798f-399">Cette propriété est héritée de [**CIM \_ ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)et est toujours définie sur « MSVM \_ VirtualSwitch ».</span><span class="sxs-lookup"><span data-stu-id="6798f-399">This property is inherited from [**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint), and it is always set to "Msvm\_VirtualSwitch"</span></span>

</dd> <dt>

<span data-ttu-id="6798f-400">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="6798f-400">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6798f-401">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6798f-401">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6798f-402">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6798f-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6798f-403">Nom système du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="6798f-403">The system name of the scoping system.</span></span> <span data-ttu-id="6798f-404">Cette propriété est héritée de [**CIM \_ ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span><span class="sxs-lookup"><span data-stu-id="6798f-404">This property is inherited from [**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span></span>

</dd> <dt>

<span data-ttu-id="6798f-405">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="6798f-405">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6798f-406">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6798f-406">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6798f-407">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6798f-407">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6798f-408">Date et heure de la dernière modification de l’état activé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="6798f-408">The date and time when the enabled state of the element last changed.</span></span> <span data-ttu-id="6798f-409">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mais elle n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="6798f-409">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="6798f-410">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="6798f-410">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6798f-411">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6798f-411">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6798f-412">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6798f-412">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6798f-413">Indique l’État cible de la transition de l’instance.</span><span class="sxs-lookup"><span data-stu-id="6798f-413">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="6798f-414">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="6798f-414">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6798f-415">Notes</span><span class="sxs-lookup"><span data-stu-id="6798f-415">Remarks</span></span>

<span data-ttu-id="6798f-416">L’accès à la classe **MSVM \_ VLANEndpoint** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="6798f-416">Access to the **Msvm\_VLANEndpoint** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="6798f-417">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="6798f-417">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="6798f-418">Exemples</span><span class="sxs-lookup"><span data-stu-id="6798f-418">Examples</span></span>

<span data-ttu-id="6798f-419">Consultez [interrogation d’objets de mise en réseau](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="6798f-419">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6798f-420">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6798f-420">Requirements</span></span>



| <span data-ttu-id="6798f-421">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6798f-421">Requirement</span></span> | <span data-ttu-id="6798f-422">Valeur</span><span class="sxs-lookup"><span data-stu-id="6798f-422">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6798f-423">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6798f-423">Minimum supported client</span></span><br/> | <span data-ttu-id="6798f-424">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6798f-424">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6798f-425">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6798f-425">Minimum supported server</span></span><br/> | <span data-ttu-id="6798f-426">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6798f-426">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6798f-427">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6798f-427">Namespace</span></span><br/>                | <span data-ttu-id="6798f-428">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="6798f-428">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6798f-429">MOF</span><span class="sxs-lookup"><span data-stu-id="6798f-429">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6798f-430"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6798f-430"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6798f-431">DLL</span><span class="sxs-lookup"><span data-stu-id="6798f-431">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6798f-432"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6798f-432"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6798f-433">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6798f-433">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6798f-434">**\_VLANENDPOINT CIM**</span><span class="sxs-lookup"><span data-stu-id="6798f-434">**CIM\_VLANEndpoint**</span></span>](cim-vlanendpoint.md)
</dt> <dt>

[<span data-ttu-id="6798f-435">**\_VLANENDPOINT CIM**</span><span class="sxs-lookup"><span data-stu-id="6798f-435">**CIM\_VLANEndpoint**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint)
</dt> </dl>

 

