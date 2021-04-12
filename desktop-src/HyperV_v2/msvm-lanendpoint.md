---
description: Représente le point de connexion logique pour une carte réseau. Lorsque le point de terminaison de réseau local est connecté à un port de commutateur, la carte réseau connectée au point de terminaison de réseau local dispose d’une connectivité réseau.
ms.assetid: 68aad05e-64b5-44dc-ab5b-8f3051fa77ca
title: Classe Msvm_LANEndpoint
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_LANEndpoint
- Msvm_LANEndpoint.InstanceID
- Msvm_LANEndpoint.Caption
- Msvm_LANEndpoint.Description
- Msvm_LANEndpoint.ElementName
- Msvm_LANEndpoint.InstallDate
- Msvm_LANEndpoint.Name
- Msvm_LANEndpoint.OperationalStatus
- Msvm_LANEndpoint.StatusDescriptions
- Msvm_LANEndpoint.Status
- Msvm_LANEndpoint.HealthState
- Msvm_LANEndpoint.CommunicationStatus
- Msvm_LANEndpoint.DetailedStatus
- Msvm_LANEndpoint.OperatingStatus
- Msvm_LANEndpoint.PrimaryStatus
- Msvm_LANEndpoint.EnabledState
- Msvm_LANEndpoint.OtherEnabledState
- Msvm_LANEndpoint.RequestedState
- Msvm_LANEndpoint.EnabledDefault
- Msvm_LANEndpoint.TimeOfLastStateChange
- Msvm_LANEndpoint.AvailableRequestedStates
- Msvm_LANEndpoint.TransitioningToState
- Msvm_LANEndpoint.SystemCreationClassName
- Msvm_LANEndpoint.SystemName
- Msvm_LANEndpoint.CreationClassName
- Msvm_LANEndpoint.NameFormat
- Msvm_LANEndpoint.ProtocolType
- Msvm_LANEndpoint.ProtocolIFType
- Msvm_LANEndpoint.OtherTypeDescription
- Msvm_LANEndpoint.LANID
- Msvm_LANEndpoint.LANType
- Msvm_LANEndpoint.OtherLANType
- Msvm_LANEndpoint.MACAddress
- Msvm_LANEndpoint.AliasAddresses
- Msvm_LANEndpoint.GroupAddresses
- Msvm_LANEndpoint.MaxDataSize
- Msvm_LANEndpoint.Connected
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7585b92461b435b99a05ed198c4c501e10703439
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203085"
---
# <a name="msvm_lanendpoint-class"></a><span data-ttu-id="62526-104">MSVM \_ LANEndpoint, classe</span><span class="sxs-lookup"><span data-stu-id="62526-104">Msvm\_LANEndpoint class</span></span>

<span data-ttu-id="62526-105">Représente le point de connexion logique pour une carte réseau.</span><span class="sxs-lookup"><span data-stu-id="62526-105">Represents the logical connection point for a network adapter.</span></span> <span data-ttu-id="62526-106">Lorsque le point de terminaison de réseau local est connecté à un port de commutateur, la carte réseau connectée au point de terminaison de réseau local dispose d’une connectivité réseau.</span><span class="sxs-lookup"><span data-stu-id="62526-106">When the LAN endpoint is connected to a switch port, the network adapter connected to the LAN endpoint has network connectivity.</span></span>

<span data-ttu-id="62526-107">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="62526-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="62526-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="62526-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_LANEndpoint : CIM_LANEndpoint
{
  string   InstanceID;
  string   Caption = "LAN Endpoint";
  string   Description = "Microsoft Virtual LAN Endpoint";
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
  uint16   EnabledState;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_LANEndpoint";
  string   NameFormat = "Microsoft Virtual Device ID";
  uint16   ProtocolType;
  uint16   ProtocolIFType;
  string   OtherTypeDescription;
  string   LANID;
  uint16   LANType;
  string   OtherLANType;
  string   MACAddress;
  string   AliasAddresses[];
  string   GroupAddresses[];
  uint32   MaxDataSize;
  boolean  Connected;
};
```

## <a name="members"></a><span data-ttu-id="62526-109">Membres</span><span class="sxs-lookup"><span data-stu-id="62526-109">Members</span></span>

<span data-ttu-id="62526-110">La classe **MSVM \_ LANEndpoint** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="62526-110">The **Msvm\_LANEndpoint** class has these types of members:</span></span>

-   [<span data-ttu-id="62526-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="62526-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="62526-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="62526-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="62526-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="62526-113">Methods</span></span>

<span data-ttu-id="62526-114">La classe **MSVM \_ LANEndpoint** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="62526-114">The **Msvm\_LANEndpoint** class has these methods.</span></span>



| <span data-ttu-id="62526-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="62526-115">Method</span></span>                                                            | <span data-ttu-id="62526-116">Description</span><span class="sxs-lookup"><span data-stu-id="62526-116">Description</span></span>                         |
|:------------------------------------------------------------------|:------------------------------------|
| [<span data-ttu-id="62526-117">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="62526-117">**RequestStateChange**</span></span>](msvm-lanendpoint-requeststatechange.md) | <span data-ttu-id="62526-118">Demande un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="62526-118">Requests a state change.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="62526-119">Propriétés</span><span class="sxs-lookup"><span data-stu-id="62526-119">Properties</span></span>

<span data-ttu-id="62526-120">La classe **MSVM \_ LANEndpoint** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="62526-120">The **Msvm\_LANEndpoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="62526-121">**AliasAddresses**</span><span class="sxs-lookup"><span data-stu-id="62526-121">**AliasAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62526-122">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="62526-122">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="62526-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="62526-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62526-124">Autres adresses de monodiffusion qui peuvent être utilisées pour communiquer avec le point de terminaison LAN.</span><span class="sxs-lookup"><span data-stu-id="62526-124">Other unicast addresses that may be used to communicate with the LAN endpoint.</span></span> <span data-ttu-id="62526-125">Cette propriété est héritée de la [**\_ LANEndpoint CIM**](/previous-versions//cc136865(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="62526-125">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="62526-126">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="62526-126">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62526-127">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="62526-127">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="62526-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="62526-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62526-129">Indique les valeurs possibles pour le paramètre *RequestedState* de la méthode [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) utilisée pour initier un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="62526-129">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="62526-130">Les valeurs répertoriées sont un sous-ensemble des valeurs contenues dans la propriété **RequestedStatesSupported** de l’instance associée de la **\_ EnabledLogicalElementCapabilities CIM**, où les valeurs sélectionnées sont une fonction de l’état actuel du [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="62526-130">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="62526-131">Cette propriété peut être non **null** si une implémentation est en mesure de publier l’ensemble de valeurs possibles en tant que fonction de l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="62526-131">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="62526-132">Cette propriété a la **valeur null** si une implémentation ne peut pas déterminer le jeu de valeurs possibles en tant que fonction de l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="62526-132">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="62526-133">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="62526-133">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="62526-134"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (2)</span><span class="sxs-lookup"><span data-stu-id="62526-134"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="62526-135"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (3)</span><span class="sxs-lookup"><span data-stu-id="62526-135"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="62526-136"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Arrêter** (4)</span><span class="sxs-lookup"><span data-stu-id="62526-136"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="62526-137"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Hors connexion** (6)</span><span class="sxs-lookup"><span data-stu-id="62526-137"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="62526-138"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="62526-138"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="62526-139"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Différer** (8)</span><span class="sxs-lookup"><span data-stu-id="62526-139"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="62526-140"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Suspension** (9)</span><span class="sxs-lookup"><span data-stu-id="62526-140"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="62526-141"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Redémarrer** (10)</span><span class="sxs-lookup"><span data-stu-id="62526-141"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="62526-142"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Réinitialiser** (11)</span><span class="sxs-lookup"><span data-stu-id="62526-142"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="62526-143"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF réservé** (..</span><span class="sxs-lookup"><span data-stu-id="62526-143"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="62526-144">)</span><span class="sxs-lookup"><span data-stu-id="62526-144">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="62526-145">**Caption**</span><span class="sxs-lookup"><span data-stu-id="62526-145">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62526-146">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="62526-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62526-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="62526-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62526-148">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="62526-148">A short description of the object.</span></span> <span data-ttu-id="62526-149">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « point de terminaison LAN ».</span><span class="sxs-lookup"><span data-stu-id="62526-149">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "LAN Endpoint".</span></span>

</dd> <dt>

<span data-ttu-id="62526-150">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="62526-150">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62526-151">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="62526-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="62526-152">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="62526-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62526-153">Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="62526-153">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="62526-154">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="62526-154">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="62526-155">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="62526-155">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="62526-156">**Connecté**</span><span class="sxs-lookup"><span data-stu-id="62526-156">**Connected**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62526-157">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="62526-157">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="62526-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="62526-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62526-159">Cette propriété a la valeur **true** si le point de terminaison LAN est connecté à un port de commutateur.</span><span class="sxs-lookup"><span data-stu-id="62526-159">This property is set to **True** if the LAN endpoint is connected to a switch port.</span></span>

</dd> <dt>

<span data-ttu-id="62526-160">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="62526-160">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62526-161">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="62526-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62526-162">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="62526-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62526-163">Qualificateurs : **clé**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="62526-163">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="62526-164">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="62526-164">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="62526-165">Cette propriété est héritée de [**CIM \_ ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)et est toujours définie sur « MSVM \_ LANEndpoint ».</span><span class="sxs-lookup"><span data-stu-id="62526-165">This property is inherited from [**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint), and it is always set to "Msvm\_LANEndpoint".</span></span>

</dd> <dt>

<span data-ttu-id="62526-166">**Description**</span><span class="sxs-lookup"><span data-stu-id="62526-166">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62526-167">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="62526-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62526-168">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="62526-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62526-169">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="62526-169">A description of the object.</span></span> <span data-ttu-id="62526-170">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « point de terminaison de réseau local virtuel Microsoft ».</span><span class="sxs-lookup"><span data-stu-id="62526-170">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Virtual LAN Endpoint".</span></span>

</dd> <dt>

<span data-ttu-id="62526-171">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="62526-171">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62526-172">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="62526-172">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="62526-173">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="62526-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62526-174">Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="62526-174">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="62526-175">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="62526-175">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="62526-176">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="62526-176">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="62526-177">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="62526-177">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62526-178">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="62526-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62526-179">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="62526-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62526-180">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="62526-180">A display name for the object.</span></span> <span data-ttu-id="62526-181">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="62526-181">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="62526-182">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="62526-182">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62526-183">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="62526-183">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="62526-184">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="62526-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62526-185">Configuration par défaut ou de démarrage d’un administrateur pour l’état activé d’un élément.</span><span class="sxs-lookup"><span data-stu-id="62526-185">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="62526-186">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) et sera l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="62526-186">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and will be one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="62526-187"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (2)</span><span class="sxs-lookup"><span data-stu-id="62526-187"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="62526-188"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (3)</span><span class="sxs-lookup"><span data-stu-id="62526-188"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="62526-189"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Activé mais hors connexion** (6)</span><span class="sxs-lookup"><span data-stu-id="62526-189"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Enabled but Offline** (6)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="62526-190">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="62526-190">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62526-191">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="62526-191">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="62526-192">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="62526-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62526-193">Spécifie l’état activé du système planifié.</span><span class="sxs-lookup"><span data-stu-id="62526-193">Specifies the enabled state of the planned system.</span></span> <span data-ttu-id="62526-194">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))et peut prendre l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="62526-194">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it can be one of the following values.</span></span>



| <span data-ttu-id="62526-195">Valeur</span><span class="sxs-lookup"><span data-stu-id="62526-195">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="62526-196">Signification</span><span class="sxs-lookup"><span data-stu-id="62526-196">Meaning</span></span>                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="62526-197"><dt>**Désactivé**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="62526-197"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="62526-198">Le système est désactivé.</span><span class="sxs-lookup"><span data-stu-id="62526-198">The system is turned off.</span></span><br/>                                             |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="62526-199"><dt>**Non applicable**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="62526-199"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="62526-200">L’élément ne prend pas en charge l’activation ou la désactivation.</span><span class="sxs-lookup"><span data-stu-id="62526-200">The element does not support being enabled or disabled.</span></span><br/>               |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="62526-201"><dt>**Activé mais hors connexion**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="62526-201"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="62526-202">Le système est activé, mais il est hors connexion.</span><span class="sxs-lookup"><span data-stu-id="62526-202">The system is enabled, but offline.</span></span> <span data-ttu-id="62526-203">Toutes les nouvelles demandes seront supprimées.</span><span class="sxs-lookup"><span data-stu-id="62526-203">Any new requests will be dropped.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="62526-204">**GroupAddresses**</span><span class="sxs-lookup"><span data-stu-id="62526-204">**GroupAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62526-205">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="62526-205">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="62526-206">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="62526-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62526-207">Adresses de multidiffusion sur lesquelles le point de terminaison LAN écoute.</span><span class="sxs-lookup"><span data-stu-id="62526-207">Multicast addresses to which the LAN endpoint listens.</span></span> <span data-ttu-id="62526-208">Cette propriété est héritée de la [**\_ LANEndpoint CIM**](/previous-versions//cc136865(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="62526-208">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="62526-209">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="62526-209">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62526-210">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="62526-210">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="62526-211">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="62526-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62526-212">Intégrité actuelle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="62526-212">The current health of the element.</span></span> <span data-ttu-id="62526-213">Cette propriété exprime l’intégrité de cet élément, mais pas nécessairement celle de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="62526-213">This property expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="62526-214">Les valeurs possibles sont comprises entre 0 et 30, où 5 signifie que l’élément est entièrement sain et 30 signifie que l’élément est complètement non opérationnel.</span><span class="sxs-lookup"><span data-stu-id="62526-214">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="62526-215">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est toujours définie sur 5 (OK).</span><span class="sxs-lookup"><span data-stu-id="62526-215">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>



| <span data-ttu-id="62526-216">Valeur</span><span class="sxs-lookup"><span data-stu-id="62526-216">Value</span></span>                                                                        | <span data-ttu-id="62526-217">Signification</span><span class="sxs-lookup"><span data-stu-id="62526-217">Meaning</span></span>                                 |
|------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="62526-218"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="62526-218"><dt>5</dt></span></span> </dl> | <span data-ttu-id="62526-219">L’état d’intégrité est normal.</span><span class="sxs-lookup"><span data-stu-id="62526-219">The health status is normal.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="62526-220">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="62526-220">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62526-221">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="62526-221">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="62526-222">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="62526-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62526-223">Date et heure de création de la configuration de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="62526-223">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="62526-224">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="62526-224">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="62526-225">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="62526-225">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62526-226">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="62526-226">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62526-227">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="62526-227">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62526-228">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="62526-228">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="62526-229">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="62526-229">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="62526-230">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="62526-230">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="62526-231">**LANID**</span><span class="sxs-lookup"><span data-stu-id="62526-231">**LANID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62526-232">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="62526-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62526-233">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="62526-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62526-234">Étiquette ou identificateur du segment LAN auquel le point de terminaison est connecté.</span><span class="sxs-lookup"><span data-stu-id="62526-234">A label or identifier for the LAN segment to which the endpoint is connected.</span></span> <span data-ttu-id="62526-235">Si le point de terminaison n’est pas actif/connecté actuellement, ou si ces informations ne sont pas connues, cette propriété aura la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="62526-235">If the endpoint is not currently active/connected, or this information is not known, then this property will be **Null**.</span></span> <span data-ttu-id="62526-236">Cette propriété est héritée de la [**\_ LANEndpoint CIM**](/previous-versions//cc136865(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="62526-236">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="62526-237">**LANType**</span><span class="sxs-lookup"><span data-stu-id="62526-237">**LANType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62526-238">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="62526-238">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="62526-239">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="62526-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62526-240">Cette propriété est déconseillée à la place de la propriété **ProtocolType** .</span><span class="sxs-lookup"><span data-stu-id="62526-240">This property is deprecated in lieu of the **ProtocolType** property.</span></span> <span data-ttu-id="62526-241">Cette propriété est héritée de la [**\_ LANEndpoint CIM**](/previous-versions//cc136865(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="62526-241">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="62526-242">**MACAddress**</span><span class="sxs-lookup"><span data-stu-id="62526-242">**MACAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62526-243">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="62526-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62526-244">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="62526-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62526-245">Qualificateurs : **MaxLen** (12)</span><span class="sxs-lookup"><span data-stu-id="62526-245">Qualifiers: **MaxLen** ( 12 )</span></span>
</dt> </dl>

<span data-ttu-id="62526-246">Adresse MAC utilisée dans la communication avec le point de terminaison LAN.</span><span class="sxs-lookup"><span data-stu-id="62526-246">The MAC address used in communication with the LAN endpoint.</span></span> <span data-ttu-id="62526-247">L’adresse MAC est mise en forme en tant que 12 chiffres hexadécimaux (par exemple, « 010203040506 »), chaque paire représentant l’un des six octets de l’adresse MAC dans l’ordre des bits canoniques, conformément à la RFC 2469.</span><span class="sxs-lookup"><span data-stu-id="62526-247">The MAC address is formatted as twelve hexadecimal digits (for example, "010203040506"), with each pair representing one of the six octets of the MAC address in canonical bit order according to RFC 2469.</span></span> <span data-ttu-id="62526-248">Cette propriété est héritée de la [**\_ LANEndpoint CIM**](/previous-versions//cc136865(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="62526-248">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="62526-249">**MaxDataSize**</span><span class="sxs-lookup"><span data-stu-id="62526-249">**MaxDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62526-250">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="62526-250">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="62526-251">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="62526-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62526-252">Qualificateurs : **unités** (« bits »)</span><span class="sxs-lookup"><span data-stu-id="62526-252">Qualifiers: **Units** ("Bits")</span></span>
</dt> </dl>

<span data-ttu-id="62526-253">Taille maximale, en nombre de bits, du champ d’information qui peut être envoyé ou reçu par le point de terminaison LAN.</span><span class="sxs-lookup"><span data-stu-id="62526-253">The largest size, in number of bits, of the information field that may be sent or received by the LAN endpoint.</span></span> <span data-ttu-id="62526-254">Cette propriété est héritée de la [**\_ LANEndpoint CIM**](/previous-versions//cc136865(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="62526-254">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="62526-255">**Nom**</span><span class="sxs-lookup"><span data-stu-id="62526-255">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62526-256">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="62526-256">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62526-257">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="62526-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62526-258">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="62526-258">The label by which the object is known.</span></span> <span data-ttu-id="62526-259">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="62526-259">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="62526-260">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="62526-260">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62526-261">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="62526-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62526-262">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="62526-262">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62526-263">Qualificateurs : **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="62526-263">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="62526-264">Contient l’heuristique d’attribution de noms sélectionnée pour garantir que la valeur de la propriété **Name** est unique.</span><span class="sxs-lookup"><span data-stu-id="62526-264">Contains the naming heuristic that is selected to ensure that the value of the **Name** property is unique.</span></span> <span data-ttu-id="62526-265">Cette propriété est héritée de [**CIM \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint)et est définie sur « Microsoft Virtual Device ID ».</span><span class="sxs-lookup"><span data-stu-id="62526-265">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint), and it is set to "Microsoft Virtual Device ID".</span></span>

</dd> <dt>

<span data-ttu-id="62526-266">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="62526-266">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62526-267">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="62526-267">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="62526-268">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="62526-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62526-269">Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="62526-269">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="62526-270">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="62526-270">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="62526-271">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="62526-271">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="62526-272">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="62526-272">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62526-273">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="62526-273">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="62526-274">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="62526-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62526-275">États actuels de l’objet.</span><span class="sxs-lookup"><span data-stu-id="62526-275">The current statuses of the object.</span></span> <span data-ttu-id="62526-276">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), et chaque élément de tableau a toujours la valeur 2 (OK).</span><span class="sxs-lookup"><span data-stu-id="62526-276">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="62526-277">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="62526-277">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62526-278">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="62526-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62526-279">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="62526-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62526-280">Chaîne qui décrit l’état activé ou désactivé de l’élément lorsque la propriété **EnabledState** a la valeur 1 (« other »).</span><span class="sxs-lookup"><span data-stu-id="62526-280">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="62526-281">Cette propriété doit avoir la valeur **null** quand **EnabledState** a une valeur autre que 1.</span><span class="sxs-lookup"><span data-stu-id="62526-281">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="62526-282">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="62526-282">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="62526-283">**OtherLANType**</span><span class="sxs-lookup"><span data-stu-id="62526-283">**OtherLANType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62526-284">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="62526-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62526-285">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="62526-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62526-286">Cette propriété est déconseillée à la place de la propriété **OtherTypeDescription** .</span><span class="sxs-lookup"><span data-stu-id="62526-286">This property is deprecated in lieu of the **OtherTypeDescription** property.</span></span> <span data-ttu-id="62526-287">Cette propriété est héritée de la [**\_ LANEndpoint CIM**](/previous-versions//cc136865(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="62526-287">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="62526-288">**OtherTypeDescription**</span><span class="sxs-lookup"><span data-stu-id="62526-288">**OtherTypeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62526-289">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="62526-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62526-290">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="62526-290">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62526-291">Qualificateurs : **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="62526-291">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="62526-292">Chaîne qui décrit le type de point de terminaison de protocole lorsque la propriété **ProtocolIFType** de cette classe (ou l’une de ses sous-classes) a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="62526-292">A string that describes the type of protocol endpoint when the **ProtocolIFType** property of this class (or any of its subclasses) is set to 1 (Other).</span></span> <span data-ttu-id="62526-293">Cette propriété doit être définie sur **null** lorsque la propriété **ProtocolIFType** a une valeur autre que 1.</span><span class="sxs-lookup"><span data-stu-id="62526-293">This property should be set to **Null** when the **ProtocolIFType** property is any value other than 1.</span></span> <span data-ttu-id="62526-294">Cette propriété est héritée de l' [**\_ ProtocolEndpoint CIM**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span><span class="sxs-lookup"><span data-stu-id="62526-294">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span></span>

</dd> <dt>

<span data-ttu-id="62526-295">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="62526-295">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62526-296">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="62526-296">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="62526-297">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="62526-297">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62526-298">Fournit des informations d’état de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="62526-298">Provides high level status information.</span></span> <span data-ttu-id="62526-299">Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir des informations d’état d’intégrité de haut niveau et détaillées pour l’élément et ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="62526-299">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="62526-300">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="62526-300">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="62526-301">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="62526-301">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="62526-302">**ProtocolIFType**</span><span class="sxs-lookup"><span data-stu-id="62526-302">**ProtocolIFType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62526-303">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="62526-303">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="62526-304">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="62526-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62526-305">La propriété est utilisée pour catégoriser et classer les instances de cette classe.</span><span class="sxs-lookup"><span data-stu-id="62526-305">The property is used to categorize and classify instances of this class.</span></span> <span data-ttu-id="62526-306">Si **ProtocolIFType** a la valeur 1 (autre), les informations de type doivent être fournies dans la propriété **OtherTypeDescription** .</span><span class="sxs-lookup"><span data-stu-id="62526-306">If the **ProtocolIFType** is set to 1 (Other), then the type information should be provided in the **OtherTypeDescription** property.</span></span> <span data-ttu-id="62526-307">Cette propriété est héritée de l' [**\_ ProtocolEndpoint CIM**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span><span class="sxs-lookup"><span data-stu-id="62526-307">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span></span>

> [!Note]  
> <span data-ttu-id="62526-308">**ProtocolIFType** est une énumération qui est synchronisée avec la [MIB ifType IANA](https://www.iana.org/assignments/ianaiftype-mib).</span><span class="sxs-lookup"><span data-stu-id="62526-308">**ProtocolIFType** is an enumeration that is synchronized with the [IANA ifType MIB](https://www.iana.org/assignments/ianaiftype-mib).</span></span> <span data-ttu-id="62526-309">Des valeurs supplémentaires définies par le DMTF sont également incluses.</span><span class="sxs-lookup"><span data-stu-id="62526-309">Additional values defined by the DMTF are also included.</span></span>

 

<dl> <dt>

<span data-ttu-id="62526-310"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="62526-310"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="62526-311"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="62526-311"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="62526-312"><span id="Regular_1822"></span><span id="regular_1822"></span><span id="REGULAR_1822"></span>**Normal 1822** (2)</span><span class="sxs-lookup"><span data-stu-id="62526-312"><span id="Regular_1822"></span><span id="regular_1822"></span><span id="REGULAR_1822"></span>**Regular 1822** (2)</span></span>
</dt> <dt>

<span data-ttu-id="62526-313"><span id="HDH_1822"></span><span id="hdh_1822"></span>**HDH 1822** (3)</span><span class="sxs-lookup"><span data-stu-id="62526-313"><span id="HDH_1822"></span><span id="hdh_1822"></span>**HDH 1822** (3)</span></span>
</dt> <dt>

<span data-ttu-id="62526-314"><span id="DDN_X.25"></span><span id="ddn_x.25"></span>**DDN X. 25** (4)</span><span class="sxs-lookup"><span data-stu-id="62526-314"><span id="DDN_X.25"></span><span id="ddn_x.25"></span>**DDN X.25** (4)</span></span>
</dt> <dt>

<span data-ttu-id="62526-315"><span id="RFC877_X.25"></span><span id="rfc877_x.25"></span>**RFC877 X. 25** (5)</span><span class="sxs-lookup"><span data-stu-id="62526-315"><span id="RFC877_X.25"></span><span id="rfc877_x.25"></span>**RFC877 X.25** (5)</span></span>
</dt> <dt>

<span data-ttu-id="62526-316"><span id="Ethernet_CSMA_CD"></span><span id="ethernet_csma_cd"></span><span id="ETHERNET_CSMA_CD"></span>**Ethernet CSMA/CD** (6)</span><span class="sxs-lookup"><span data-stu-id="62526-316"><span id="Ethernet_CSMA_CD"></span><span id="ethernet_csma_cd"></span><span id="ETHERNET_CSMA_CD"></span>**Ethernet CSMA/CD** (6)</span></span>
</dt> <dt>

<span data-ttu-id="62526-317"><span id="ISO_802.3_CSMA_CD"></span><span id="iso_802.3_csma_cd"></span>**ISO 802,3 CSMA/CD** (7)</span><span class="sxs-lookup"><span data-stu-id="62526-317"><span id="ISO_802.3_CSMA_CD"></span><span id="iso_802.3_csma_cd"></span>**ISO 802.3 CSMA/CD** (7)</span></span>
</dt> <dt>

<span data-ttu-id="62526-318"><span id="ISO_802.4_Token_Bus"></span><span id="iso_802.4_token_bus"></span><span id="ISO_802.4_TOKEN_BUS"></span>**Bus de jetons ISO 802,4** (8)</span><span class="sxs-lookup"><span data-stu-id="62526-318"><span id="ISO_802.4_Token_Bus"></span><span id="iso_802.4_token_bus"></span><span id="ISO_802.4_TOKEN_BUS"></span>**ISO 802.4 Token Bus** (8)</span></span>
</dt> <dt>

<span data-ttu-id="62526-319"><span id="ISO_802.5_Token_Ring"></span><span id="iso_802.5_token_ring"></span><span id="ISO_802.5_TOKEN_RING"></span>**Token Ring ISO 802,5** (9)</span><span class="sxs-lookup"><span data-stu-id="62526-319"><span id="ISO_802.5_Token_Ring"></span><span id="iso_802.5_token_ring"></span><span id="ISO_802.5_TOKEN_RING"></span>**ISO 802.5 Token Ring** (9)</span></span>
</dt> <dt>

<span data-ttu-id="62526-320"><span id="ISO_802.6_MAN"></span><span id="iso_802.6_man"></span>**ISO 802,6 Man** (10)</span><span class="sxs-lookup"><span data-stu-id="62526-320"><span id="ISO_802.6_MAN"></span><span id="iso_802.6_man"></span>**ISO 802.6 MAN** (10)</span></span>
</dt> <dt>

<span data-ttu-id="62526-321"><span id="StarLAN"></span><span id="starlan"></span><span id="STARLAN"></span>**Starlan** (11)</span><span class="sxs-lookup"><span data-stu-id="62526-321"><span id="StarLAN"></span><span id="starlan"></span><span id="STARLAN"></span>**StarLAN** (11)</span></span>
</dt> <dt>

<span data-ttu-id="62526-322"><span id="Proteon_10Mbit"></span><span id="proteon_10mbit"></span><span id="PROTEON_10MBIT"></span>**Proteon 10Mbit** (12)</span><span class="sxs-lookup"><span data-stu-id="62526-322"><span id="Proteon_10Mbit"></span><span id="proteon_10mbit"></span><span id="PROTEON_10MBIT"></span>**Proteon 10Mbit** (12)</span></span>
</dt> <dt>

<span data-ttu-id="62526-323"><span id="Proteon_80Mbit"></span><span id="proteon_80mbit"></span><span id="PROTEON_80MBIT"></span>**Proteon 80Mbit** (13)</span><span class="sxs-lookup"><span data-stu-id="62526-323"><span id="Proteon_80Mbit"></span><span id="proteon_80mbit"></span><span id="PROTEON_80MBIT"></span>**Proteon 80Mbit** (13)</span></span>
</dt> <dt>

<span data-ttu-id="62526-324"><span id="HyperChannel"></span><span id="hyperchannel"></span><span id="HYPERCHANNEL"></span>**Hyperchannel** (14)</span><span class="sxs-lookup"><span data-stu-id="62526-324"><span id="HyperChannel"></span><span id="hyperchannel"></span><span id="HYPERCHANNEL"></span>**HyperChannel** (14)</span></span>
</dt> <dt>

<span data-ttu-id="62526-325"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (15)</span><span class="sxs-lookup"><span data-stu-id="62526-325"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (15)</span></span>
</dt> <dt>

<span data-ttu-id="62526-326"><span id="LAP-B"></span><span id="lap-b"></span>**Lap-B** (16)</span><span class="sxs-lookup"><span data-stu-id="62526-326"><span id="LAP-B"></span><span id="lap-b"></span>**LAP-B** (16)</span></span>
</dt> <dt>

<span data-ttu-id="62526-327"><span id="SDLC"></span><span id="sdlc"></span>**SDLC** (17)</span><span class="sxs-lookup"><span data-stu-id="62526-327"><span id="SDLC"></span><span id="sdlc"></span>**SDLC** (17)</span></span>
</dt> <dt>

<span data-ttu-id="62526-328"><span id="DS1"></span><span id="ds1"></span>**DS1** (18)</span><span class="sxs-lookup"><span data-stu-id="62526-328"><span id="DS1"></span><span id="ds1"></span>**DS1** (18)</span></span>
</dt> <dt>

<span data-ttu-id="62526-329"><span id="E1"></span><span id="e1"></span>**E1** (19)</span><span class="sxs-lookup"><span data-stu-id="62526-329"><span id="E1"></span><span id="e1"></span>**E1** (19)</span></span>
</dt> <dt>

<span data-ttu-id="62526-330"><span id="Basic_ISDN"></span><span id="basic_isdn"></span><span id="BASIC_ISDN"></span>**RNIS de base** (20)</span><span class="sxs-lookup"><span data-stu-id="62526-330"><span id="Basic_ISDN"></span><span id="basic_isdn"></span><span id="BASIC_ISDN"></span>**Basic ISDN** (20)</span></span>
</dt> <dt>

<span data-ttu-id="62526-331"><span id="Primary_ISDN"></span><span id="primary_isdn"></span><span id="PRIMARY_ISDN"></span>**RNIS principal** (21)</span><span class="sxs-lookup"><span data-stu-id="62526-331"><span id="Primary_ISDN"></span><span id="primary_isdn"></span><span id="PRIMARY_ISDN"></span>**Primary ISDN** (21)</span></span>
</dt> <dt>

<span data-ttu-id="62526-332"><span id="Proprietary_Point-to-Point_Serial"></span><span id="proprietary_point-to-point_serial"></span><span id="PROPRIETARY_POINT-TO-POINT_SERIAL"></span>**Série point à point propriétaire** (22)</span><span class="sxs-lookup"><span data-stu-id="62526-332"><span id="Proprietary_Point-to-Point_Serial"></span><span id="proprietary_point-to-point_serial"></span><span id="PROPRIETARY_POINT-TO-POINT_SERIAL"></span>**Proprietary Point-to-Point Serial** (22)</span></span>
</dt> <dt>

<span data-ttu-id="62526-333"><span id="PPP"></span><span id="ppp"></span>**PPP** (23)</span><span class="sxs-lookup"><span data-stu-id="62526-333"><span id="PPP"></span><span id="ppp"></span>**PPP** (23)</span></span>
</dt> <dt>

<span data-ttu-id="62526-334"><span id="Software_Loopback"></span><span id="software_loopback"></span><span id="SOFTWARE_LOOPBACK"></span>**Bouclage logiciel** (24)</span><span class="sxs-lookup"><span data-stu-id="62526-334"><span id="Software_Loopback"></span><span id="software_loopback"></span><span id="SOFTWARE_LOOPBACK"></span>**Software Loopback** (24)</span></span>
</dt> <dt>

<span data-ttu-id="62526-335"><span id="EON"></span><span id="eon"></span>**EON** (25)</span><span class="sxs-lookup"><span data-stu-id="62526-335"><span id="EON"></span><span id="eon"></span>**EON** (25)</span></span>
</dt> <dt>

<span data-ttu-id="62526-336"><span id="Ethernet_3Mbit"></span><span id="ethernet_3mbit"></span><span id="ETHERNET_3MBIT"></span>**3Mbit Ethernet** (26)</span><span class="sxs-lookup"><span data-stu-id="62526-336"><span id="Ethernet_3Mbit"></span><span id="ethernet_3mbit"></span><span id="ETHERNET_3MBIT"></span>**Ethernet 3Mbit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="62526-337"><span id="NSIP"></span><span id="nsip"></span>**NSIP** (27)</span><span class="sxs-lookup"><span data-stu-id="62526-337"><span id="NSIP"></span><span id="nsip"></span>**NSIP** (27)</span></span>
</dt> <dt>

<span data-ttu-id="62526-338"><span id="SLIP"></span><span id="slip"></span>**Slip** (28)</span><span class="sxs-lookup"><span data-stu-id="62526-338"><span id="SLIP"></span><span id="slip"></span>**SLIP** (28)</span></span>
</dt> <dt>

<span data-ttu-id="62526-339"><span id="Ultra"></span><span id="ultra"></span><span id="ULTRA"></span>**Ultra** (29)</span><span class="sxs-lookup"><span data-stu-id="62526-339"><span id="Ultra"></span><span id="ultra"></span><span id="ULTRA"></span>**Ultra** (29)</span></span>
</dt> <dt>

<span data-ttu-id="62526-340"><span id="DS3"></span><span id="ds3"></span>**DS3** (30)</span><span class="sxs-lookup"><span data-stu-id="62526-340"><span id="DS3"></span><span id="ds3"></span>**DS3** (30)</span></span>
</dt> <dt>

<span data-ttu-id="62526-341"><span id="SIP"></span><span id="sip"></span>**SIP** (31)</span><span class="sxs-lookup"><span data-stu-id="62526-341"><span id="SIP"></span><span id="sip"></span>**SIP** (31)</span></span>
</dt> <dt>

<span data-ttu-id="62526-342"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Relais de trames** (32)</span><span class="sxs-lookup"><span data-stu-id="62526-342"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (32)</span></span>
</dt> <dt>

<span data-ttu-id="62526-343"><span id="RS-232"></span><span id="rs-232"></span>**RS-232** (33)</span><span class="sxs-lookup"><span data-stu-id="62526-343"><span id="RS-232"></span><span id="rs-232"></span>**RS-232** (33)</span></span>
</dt> <dt>

<span data-ttu-id="62526-344"><span id="Parallel"></span><span id="parallel"></span><span id="PARALLEL"></span>**Parallèle** (34)</span><span class="sxs-lookup"><span data-stu-id="62526-344"><span id="Parallel"></span><span id="parallel"></span><span id="PARALLEL"></span>**Parallel** (34)</span></span>
</dt> <dt>

<span data-ttu-id="62526-345"><span id="ARCNet"></span><span id="arcnet"></span><span id="ARCNET"></span>**Arcnet** (35)</span><span class="sxs-lookup"><span data-stu-id="62526-345"><span id="ARCNet"></span><span id="arcnet"></span><span id="ARCNET"></span>**ARCNet** (35)</span></span>
</dt> <dt>

<span data-ttu-id="62526-346"><span id="ARCNet_Plus"></span><span id="arcnet_plus"></span><span id="ARCNET_PLUS"></span>**Arcnet plus** (36)</span><span class="sxs-lookup"><span data-stu-id="62526-346"><span id="ARCNet_Plus"></span><span id="arcnet_plus"></span><span id="ARCNET_PLUS"></span>**ARCNet Plus** (36)</span></span>
</dt> <dt>

<span data-ttu-id="62526-347"><span id="ATM"></span><span id="atm"></span>**ATM** (37)</span><span class="sxs-lookup"><span data-stu-id="62526-347"><span id="ATM"></span><span id="atm"></span>**ATM** (37)</span></span>
</dt> <dt>

<span data-ttu-id="62526-348"><span id="MIO_X.25"></span><span id="mio_x.25"></span>**Mio X. 25** (38)</span><span class="sxs-lookup"><span data-stu-id="62526-348"><span id="MIO_X.25"></span><span id="mio_x.25"></span>**MIO X.25** (38)</span></span>
</dt> <dt>

<span data-ttu-id="62526-349"><span id="SONET"></span><span id="sonet"></span>**SONET** (39)</span><span class="sxs-lookup"><span data-stu-id="62526-349"><span id="SONET"></span><span id="sonet"></span>**SONET** (39)</span></span>
</dt> <dt>

<span data-ttu-id="62526-350"><span id="X.25_PLE"></span><span id="x.25_ple"></span>**X. 25 espérance** de la (40)</span><span class="sxs-lookup"><span data-stu-id="62526-350"><span id="X.25_PLE"></span><span id="x.25_ple"></span>**X.25 PLE** (40)</span></span>
</dt> <dt>

<span data-ttu-id="62526-351"><span id="ISO_802.211c"></span><span id="iso_802.211c"></span><span id="ISO_802.211C"></span>**ISO 802.211 c** (41)</span><span class="sxs-lookup"><span data-stu-id="62526-351"><span id="ISO_802.211c"></span><span id="iso_802.211c"></span><span id="ISO_802.211C"></span>**ISO 802.211c** (41)</span></span>
</dt> <dt>

<span data-ttu-id="62526-352"><span id="LocalTalk"></span><span id="localtalk"></span><span id="LOCALTALK"></span>**LocalTalk** (42)</span><span class="sxs-lookup"><span data-stu-id="62526-352"><span id="LocalTalk"></span><span id="localtalk"></span><span id="LOCALTALK"></span>**LocalTalk** (42)</span></span>
</dt> <dt>

<span data-ttu-id="62526-353"><span id="SMDS_DXI"></span><span id="smds_dxi"></span>**SMDS DXi** (43)</span><span class="sxs-lookup"><span data-stu-id="62526-353"><span id="SMDS_DXI"></span><span id="smds_dxi"></span>**SMDS DXI** (43)</span></span>
</dt> <dt>

<span data-ttu-id="62526-354"><span id="Frame_Relay_Service"></span><span id="frame_relay_service"></span><span id="FRAME_RELAY_SERVICE"></span>**Service Frame Relay** (44)</span><span class="sxs-lookup"><span data-stu-id="62526-354"><span id="Frame_Relay_Service"></span><span id="frame_relay_service"></span><span id="FRAME_RELAY_SERVICE"></span>**Frame Relay Service** (44)</span></span>
</dt> <dt>

<span data-ttu-id="62526-355"><span id="V.35"></span><span id="v.35"></span>**V. 35** (45)</span><span class="sxs-lookup"><span data-stu-id="62526-355"><span id="V.35"></span><span id="v.35"></span>**V.35** (45)</span></span>
</dt> <dt>

<span data-ttu-id="62526-356"><span id="HSSI"></span><span id="hssi"></span>**HSSI** (46)</span><span class="sxs-lookup"><span data-stu-id="62526-356"><span id="HSSI"></span><span id="hssi"></span>**HSSI** (46)</span></span>
</dt> <dt>

<span data-ttu-id="62526-357"><span id="HIPPI"></span><span id="hippi"></span>**HIPPA** (47)</span><span class="sxs-lookup"><span data-stu-id="62526-357"><span id="HIPPI"></span><span id="hippi"></span>**HIPPI** (47)</span></span>
</dt> <dt>

<span data-ttu-id="62526-358"><span id="Modem"></span><span id="modem"></span><span id="MODEM"></span>**Modem** (48)</span><span class="sxs-lookup"><span data-stu-id="62526-358"><span id="Modem"></span><span id="modem"></span><span id="MODEM"></span>**Modem** (48)</span></span>
</dt> <dt>

<span data-ttu-id="62526-359"><span id="AAL5"></span><span id="aal5"></span>**AAL5** (49)</span><span class="sxs-lookup"><span data-stu-id="62526-359"><span id="AAL5"></span><span id="aal5"></span>**AAL5** (49)</span></span>
</dt> <dt>

<span data-ttu-id="62526-360"><span id="SONET_Path"></span><span id="sonet_path"></span><span id="SONET_PATH"></span>**Chemin d’accès SONET** (50)</span><span class="sxs-lookup"><span data-stu-id="62526-360"><span id="SONET_Path"></span><span id="sonet_path"></span><span id="SONET_PATH"></span>**SONET Path** (50)</span></span>
</dt> <dt>

<span data-ttu-id="62526-361"><span id="SONET_VT"></span><span id="sonet_vt"></span>**SONET VT** (51)</span><span class="sxs-lookup"><span data-stu-id="62526-361"><span id="SONET_VT"></span><span id="sonet_vt"></span>**SONET VT** (51)</span></span>
</dt> <dt>

<span data-ttu-id="62526-362"><span id="SMDS_ICIP"></span><span id="smds_icip"></span>**SMDS ICIP** (52)</span><span class="sxs-lookup"><span data-stu-id="62526-362"><span id="SMDS_ICIP"></span><span id="smds_icip"></span>**SMDS ICIP** (52)</span></span>
</dt> <dt>

<span data-ttu-id="62526-363"><span id="Proprietary_Virtual_Internal"></span><span id="proprietary_virtual_internal"></span><span id="PROPRIETARY_VIRTUAL_INTERNAL"></span>**Propriétaire virtuel/interne** (53)</span><span class="sxs-lookup"><span data-stu-id="62526-363"><span id="Proprietary_Virtual_Internal"></span><span id="proprietary_virtual_internal"></span><span id="PROPRIETARY_VIRTUAL_INTERNAL"></span>**Proprietary Virtual/Internal** (53)</span></span>
</dt> <dt>

<span data-ttu-id="62526-364"><span id="Proprietary_Multiplexor"></span><span id="proprietary_multiplexor"></span><span id="PROPRIETARY_MULTIPLEXOR"></span>**Multiplexeur propriétaire** (54)</span><span class="sxs-lookup"><span data-stu-id="62526-364"><span id="Proprietary_Multiplexor"></span><span id="proprietary_multiplexor"></span><span id="PROPRIETARY_MULTIPLEXOR"></span>**Proprietary Multiplexor** (54)</span></span>
</dt> <dt>

<span data-ttu-id="62526-365"><span id="IEEE_802.12"></span><span id="ieee_802.12"></span>**IEEE 802,12** (55)</span><span class="sxs-lookup"><span data-stu-id="62526-365"><span id="IEEE_802.12"></span><span id="ieee_802.12"></span>**IEEE 802.12** (55)</span></span>
</dt> <dt>

<span data-ttu-id="62526-366"><span id="Fibre_Channel"></span><span id="fibre_channel"></span><span id="FIBRE_CHANNEL"></span>**Fibre Channel** (56)</span><span class="sxs-lookup"><span data-stu-id="62526-366"><span id="Fibre_Channel"></span><span id="fibre_channel"></span><span id="FIBRE_CHANNEL"></span>**Fibre Channel** (56)</span></span>
</dt> <dt>

<span data-ttu-id="62526-367"><span id="HIPPI_Interface"></span><span id="hippi_interface"></span><span id="HIPPI_INTERFACE"></span>**Interface HIPPA** (57)</span><span class="sxs-lookup"><span data-stu-id="62526-367"><span id="HIPPI_Interface"></span><span id="hippi_interface"></span><span id="HIPPI_INTERFACE"></span>**HIPPI Interface** (57)</span></span>
</dt> <dt>

<span data-ttu-id="62526-368"><span id="Frame_Relay_Interconnect"></span><span id="frame_relay_interconnect"></span><span id="FRAME_RELAY_INTERCONNECT"></span>**Interconnexion du relais de trames** (58)</span><span class="sxs-lookup"><span data-stu-id="62526-368"><span id="Frame_Relay_Interconnect"></span><span id="frame_relay_interconnect"></span><span id="FRAME_RELAY_INTERCONNECT"></span>**Frame Relay Interconnect** (58)</span></span>
</dt> <dt>

<span data-ttu-id="62526-369"><span id="ATM_Emulated_LAN_for_802.3"></span><span id="atm_emulated_lan_for_802.3"></span><span id="ATM_EMULATED_LAN_FOR_802.3"></span>**Réseau local émulé ATM pour 802,3** (59)</span><span class="sxs-lookup"><span data-stu-id="62526-369"><span id="ATM_Emulated_LAN_for_802.3"></span><span id="atm_emulated_lan_for_802.3"></span><span id="ATM_EMULATED_LAN_FOR_802.3"></span>**ATM Emulated LAN for 802.3** (59)</span></span>
</dt> <dt>

<span data-ttu-id="62526-370"><span id="ATM_Emulated_LAN_for_802.5"></span><span id="atm_emulated_lan_for_802.5"></span><span id="ATM_EMULATED_LAN_FOR_802.5"></span>**Réseau local émulé ATM pour 802,5** (60)</span><span class="sxs-lookup"><span data-stu-id="62526-370"><span id="ATM_Emulated_LAN_for_802.5"></span><span id="atm_emulated_lan_for_802.5"></span><span id="ATM_EMULATED_LAN_FOR_802.5"></span>**ATM Emulated LAN for 802.5** (60)</span></span>
</dt> <dt>

<span data-ttu-id="62526-371"><span id="ATM_Emulated_Circuit"></span><span id="atm_emulated_circuit"></span><span id="ATM_EMULATED_CIRCUIT"></span>**Circuit émulé ATM** (61)</span><span class="sxs-lookup"><span data-stu-id="62526-371"><span id="ATM_Emulated_Circuit"></span><span id="atm_emulated_circuit"></span><span id="ATM_EMULATED_CIRCUIT"></span>**ATM Emulated Circuit** (61)</span></span>
</dt> <dt>

<span data-ttu-id="62526-372"><span id="Fast_Ethernet__100BaseT_"></span><span id="fast_ethernet__100baset_"></span><span id="FAST_ETHERNET__100BASET_"></span>**Fast Ethernet (100BaseT)** (62)</span><span class="sxs-lookup"><span data-stu-id="62526-372"><span id="Fast_Ethernet__100BaseT_"></span><span id="fast_ethernet__100baset_"></span><span id="FAST_ETHERNET__100BASET_"></span>**Fast Ethernet (100BaseT)** (62)</span></span>
</dt> <dt>

<span data-ttu-id="62526-373"><span id="ISDN"></span><span id="isdn"></span>**RNIS** (63)</span><span class="sxs-lookup"><span data-stu-id="62526-373"><span id="ISDN"></span><span id="isdn"></span>**ISDN** (63)</span></span>
</dt> <dt>

<span data-ttu-id="62526-374"><span id="V.11"></span><span id="v.11"></span>**V. 11** (64)</span><span class="sxs-lookup"><span data-stu-id="62526-374"><span id="V.11"></span><span id="v.11"></span>**V.11** (64)</span></span>
</dt> <dt>

<span data-ttu-id="62526-375"><span id="V.36"></span><span id="v.36"></span>**V. 36** (65)</span><span class="sxs-lookup"><span data-stu-id="62526-375"><span id="V.36"></span><span id="v.36"></span>**V.36** (65)</span></span>
</dt> <dt>

<span data-ttu-id="62526-376"><span id="G703_at_64K"></span><span id="g703_at_64k"></span><span id="G703_AT_64K"></span>**G703 à 64 Ko** (66)</span><span class="sxs-lookup"><span data-stu-id="62526-376"><span id="G703_at_64K"></span><span id="g703_at_64k"></span><span id="G703_AT_64K"></span>**G703 at 64K** (66)</span></span>
</dt> <dt>

<span data-ttu-id="62526-377"><span id="G703_at_2Mb"></span><span id="g703_at_2mb"></span><span id="G703_AT_2MB"></span>**G703 à 2 Mo** (67)</span><span class="sxs-lookup"><span data-stu-id="62526-377"><span id="G703_at_2Mb"></span><span id="g703_at_2mb"></span><span id="G703_AT_2MB"></span>**G703 at 2Mb** (67)</span></span>
</dt> <dt>

<span data-ttu-id="62526-378"><span id="QLLC"></span><span id="qllc"></span>**QLLC** (68)</span><span class="sxs-lookup"><span data-stu-id="62526-378"><span id="QLLC"></span><span id="qllc"></span>**QLLC** (68)</span></span>
</dt> <dt>

<span data-ttu-id="62526-379"><span id="Fast_Ethernet_100BaseFX"></span><span id="fast_ethernet_100basefx"></span><span id="FAST_ETHERNET_100BASEFX"></span>**Fast Ethernet 100BaseFX** (69)</span><span class="sxs-lookup"><span data-stu-id="62526-379"><span id="Fast_Ethernet_100BaseFX"></span><span id="fast_ethernet_100basefx"></span><span id="FAST_ETHERNET_100BASEFX"></span>**Fast Ethernet 100BaseFX** (69)</span></span>
</dt> <dt>

<span data-ttu-id="62526-380"><span id="Channel"></span><span id="channel"></span><span id="CHANNEL"></span>**Canal** (70)</span><span class="sxs-lookup"><span data-stu-id="62526-380"><span id="Channel"></span><span id="channel"></span><span id="CHANNEL"></span>**Channel** (70)</span></span>
</dt> <dt>

<span data-ttu-id="62526-381"><span id="IEEE_802.11"></span><span id="ieee_802.11"></span>**IEEE 802,11** (71)</span><span class="sxs-lookup"><span data-stu-id="62526-381"><span id="IEEE_802.11"></span><span id="ieee_802.11"></span>**IEEE 802.11** (71)</span></span>
</dt> <dt>

<span data-ttu-id="62526-382"><span id="IBM_260_370_OEMI_Channel"></span><span id="ibm_260_370_oemi_channel"></span><span id="IBM_260_370_OEMI_CHANNEL"></span>**Canal IBM 260/370 OEMI** (72)</span><span class="sxs-lookup"><span data-stu-id="62526-382"><span id="IBM_260_370_OEMI_Channel"></span><span id="ibm_260_370_oemi_channel"></span><span id="IBM_260_370_OEMI_CHANNEL"></span>**IBM 260/370 OEMI Channel** (72)</span></span>
</dt> <dt>

<span data-ttu-id="62526-383"><span id="ESCON"></span><span id="escon"></span>**ESCON** (73)</span><span class="sxs-lookup"><span data-stu-id="62526-383"><span id="ESCON"></span><span id="escon"></span>**ESCON** (73)</span></span>
</dt> <dt>

<span data-ttu-id="62526-384"><span id="Data_Link_Switching"></span><span id="data_link_switching"></span><span id="DATA_LINK_SWITCHING"></span>**Commutation des liaisons de données** (74)</span><span class="sxs-lookup"><span data-stu-id="62526-384"><span id="Data_Link_Switching"></span><span id="data_link_switching"></span><span id="DATA_LINK_SWITCHING"></span>**Data Link Switching** (74)</span></span>
</dt> <dt>

<span data-ttu-id="62526-385"><span id="ISDN_S_T_Interface"></span><span id="isdn_s_t_interface"></span><span id="ISDN_S_T_INTERFACE"></span>**Interface RNIS S/T** (75)</span><span class="sxs-lookup"><span data-stu-id="62526-385"><span id="ISDN_S_T_Interface"></span><span id="isdn_s_t_interface"></span><span id="ISDN_S_T_INTERFACE"></span>**ISDN S/T Interface** (75)</span></span>
</dt> <dt>

<span data-ttu-id="62526-386"><span id="ISDN_U_Interface"></span><span id="isdn_u_interface"></span><span id="ISDN_U_INTERFACE"></span>**Interface RNIS U** (76)</span><span class="sxs-lookup"><span data-stu-id="62526-386"><span id="ISDN_U_Interface"></span><span id="isdn_u_interface"></span><span id="ISDN_U_INTERFACE"></span>**ISDN U Interface** (76)</span></span>
</dt> <dt>

<span data-ttu-id="62526-387"><span id="LAP-D"></span><span id="lap-d"></span>**Lap-D** (77)</span><span class="sxs-lookup"><span data-stu-id="62526-387"><span id="LAP-D"></span><span id="lap-d"></span>**LAP-D** (77)</span></span>
</dt> <dt>

<span data-ttu-id="62526-388"><span id="IP_Switch"></span><span id="ip_switch"></span><span id="IP_SWITCH"></span>**Commutateur IP** (78)</span><span class="sxs-lookup"><span data-stu-id="62526-388"><span id="IP_Switch"></span><span id="ip_switch"></span><span id="IP_SWITCH"></span>**IP Switch** (78)</span></span>
</dt> <dt>

<span data-ttu-id="62526-389"><span id="Remote_Source_Route_Bridging"></span><span id="remote_source_route_bridging"></span><span id="REMOTE_SOURCE_ROUTE_BRIDGING"></span>**Pontage d’itinéraires source distants** (79)</span><span class="sxs-lookup"><span data-stu-id="62526-389"><span id="Remote_Source_Route_Bridging"></span><span id="remote_source_route_bridging"></span><span id="REMOTE_SOURCE_ROUTE_BRIDGING"></span>**Remote Source Route Bridging** (79)</span></span>
</dt> <dt>

<span data-ttu-id="62526-390"><span id="ATM_Logical"></span><span id="atm_logical"></span><span id="ATM_LOGICAL"></span>**ATM logique** (80)</span><span class="sxs-lookup"><span data-stu-id="62526-390"><span id="ATM_Logical"></span><span id="atm_logical"></span><span id="ATM_LOGICAL"></span>**ATM Logical** (80)</span></span>
</dt> <dt>

<span data-ttu-id="62526-391"><span id="DS0"></span><span id="ds0"></span>**DS0** (81)</span><span class="sxs-lookup"><span data-stu-id="62526-391"><span id="DS0"></span><span id="ds0"></span>**DS0** (81)</span></span>
</dt> <dt>

<span data-ttu-id="62526-392"><span id="DS0_Bundle"></span><span id="ds0_bundle"></span><span id="DS0_BUNDLE"></span>**Bundle DS0** (82)</span><span class="sxs-lookup"><span data-stu-id="62526-392"><span id="DS0_Bundle"></span><span id="ds0_bundle"></span><span id="DS0_BUNDLE"></span>**DS0 Bundle** (82)</span></span>
</dt> <dt>

<span data-ttu-id="62526-393"><span id="BSC"></span><span id="bsc"></span>**BSC** (83)</span><span class="sxs-lookup"><span data-stu-id="62526-393"><span id="BSC"></span><span id="bsc"></span>**BSC** (83)</span></span>
</dt> <dt>

<span data-ttu-id="62526-394"><span id="Async"></span><span id="async"></span><span id="ASYNC"></span>**Async** (84)</span><span class="sxs-lookup"><span data-stu-id="62526-394"><span id="Async"></span><span id="async"></span><span id="ASYNC"></span>**Async** (84)</span></span>
</dt> <dt>

<span data-ttu-id="62526-395"><span id="Combat_Net_Radio"></span><span id="combat_net_radio"></span><span id="COMBAT_NET_RADIO"></span>**Radio combat net** (85)</span><span class="sxs-lookup"><span data-stu-id="62526-395"><span id="Combat_Net_Radio"></span><span id="combat_net_radio"></span><span id="COMBAT_NET_RADIO"></span>**Combat Net Radio** (85)</span></span>
</dt> <dt>

<span data-ttu-id="62526-396"><span id="ISO_802.5r_DTR"></span><span id="iso_802.5r_dtr"></span><span id="ISO_802.5R_DTR"></span>**ISO 802.5 r DTR** (86)</span><span class="sxs-lookup"><span data-stu-id="62526-396"><span id="ISO_802.5r_DTR"></span><span id="iso_802.5r_dtr"></span><span id="ISO_802.5R_DTR"></span>**ISO 802.5r DTR** (86)</span></span>
</dt> <dt>

<span data-ttu-id="62526-397"><span id="Ext_Pos_Loc_Report_System"></span><span id="ext_pos_loc_report_system"></span><span id="EXT_POS_LOC_REPORT_SYSTEM"></span>**Système de rapports ext POS Loc** (87)</span><span class="sxs-lookup"><span data-stu-id="62526-397"><span id="Ext_Pos_Loc_Report_System"></span><span id="ext_pos_loc_report_system"></span><span id="EXT_POS_LOC_REPORT_SYSTEM"></span>**Ext Pos Loc Report System** (87)</span></span>
</dt> <dt>

<span data-ttu-id="62526-398"><span id="AppleTalk_Remote_Access_Protocol"></span><span id="appletalk_remote_access_protocol"></span><span id="APPLETALK_REMOTE_ACCESS_PROTOCOL"></span>**Protocole d’accès à distance AppleTalk** (88)</span><span class="sxs-lookup"><span data-stu-id="62526-398"><span id="AppleTalk_Remote_Access_Protocol"></span><span id="appletalk_remote_access_protocol"></span><span id="APPLETALK_REMOTE_ACCESS_PROTOCOL"></span>**AppleTalk Remote Access Protocol** (88)</span></span>
</dt> <dt>

<span data-ttu-id="62526-399"><span id="Proprietary_Connectionless"></span><span id="proprietary_connectionless"></span><span id="PROPRIETARY_CONNECTIONLESS"></span>**Propriétaire sans connexion** (89)</span><span class="sxs-lookup"><span data-stu-id="62526-399"><span id="Proprietary_Connectionless"></span><span id="proprietary_connectionless"></span><span id="PROPRIETARY_CONNECTIONLESS"></span>**Proprietary Connectionless** (89)</span></span>
</dt> <dt>

<span data-ttu-id="62526-400"><span id="ITU_X.29_Host_PAD"></span><span id="itu_x.29_host_pad"></span><span id="ITU_X.29_HOST_PAD"></span>**Bloc-notes de l’hôte ITU X. 29** (90)</span><span class="sxs-lookup"><span data-stu-id="62526-400"><span id="ITU_X.29_Host_PAD"></span><span id="itu_x.29_host_pad"></span><span id="ITU_X.29_HOST_PAD"></span>**ITU X.29 Host PAD** (90)</span></span>
</dt> <dt>

<span data-ttu-id="62526-401"><span id="ITU_X.3_Terminal_PAD"></span><span id="itu_x.3_terminal_pad"></span><span id="ITU_X.3_TERMINAL_PAD"></span>**Boîtier terminal ITU X. 3** (91)</span><span class="sxs-lookup"><span data-stu-id="62526-401"><span id="ITU_X.3_Terminal_PAD"></span><span id="itu_x.3_terminal_pad"></span><span id="ITU_X.3_TERMINAL_PAD"></span>**ITU X.3 Terminal PAD** (91)</span></span>
</dt> <dt>

<span data-ttu-id="62526-402"><span id="Frame_Relay_MPI"></span><span id="frame_relay_mpi"></span><span id="FRAME_RELAY_MPI"></span>**MPI de relais de trames** (92)</span><span class="sxs-lookup"><span data-stu-id="62526-402"><span id="Frame_Relay_MPI"></span><span id="frame_relay_mpi"></span><span id="FRAME_RELAY_MPI"></span>**Frame Relay MPI** (92)</span></span>
</dt> <dt>

<span data-ttu-id="62526-403"><span id="ITU_X.213"></span><span id="itu_x.213"></span>**ITU X. 213** (93)</span><span class="sxs-lookup"><span data-stu-id="62526-403"><span id="ITU_X.213"></span><span id="itu_x.213"></span>**ITU X.213** (93)</span></span>
</dt> <dt>

<span data-ttu-id="62526-404"><span id="ADSL"></span><span id="adsl"></span>**ADSL** (94)</span><span class="sxs-lookup"><span data-stu-id="62526-404"><span id="ADSL"></span><span id="adsl"></span>**ADSL** (94)</span></span>
</dt> <dt>

<span data-ttu-id="62526-405"><span id="RADSL"></span><span id="radsl"></span>**RADSL** (95)</span><span class="sxs-lookup"><span data-stu-id="62526-405"><span id="RADSL"></span><span id="radsl"></span>**RADSL** (95)</span></span>
</dt> <dt>

<span data-ttu-id="62526-406"><span id="SDSL"></span><span id="sdsl"></span>**SDSL** (96)</span><span class="sxs-lookup"><span data-stu-id="62526-406"><span id="SDSL"></span><span id="sdsl"></span>**SDSL** (96)</span></span>
</dt> <dt>

<span data-ttu-id="62526-407"><span id="VDSL"></span><span id="vdsl"></span>**VDSL** (97)</span><span class="sxs-lookup"><span data-stu-id="62526-407"><span id="VDSL"></span><span id="vdsl"></span>**VDSL** (97)</span></span>
</dt> <dt>

<span data-ttu-id="62526-408"><span id="ISO_802.5_CRFP"></span><span id="iso_802.5_crfp"></span>**ISO 802,5 CRFP** (98)</span><span class="sxs-lookup"><span data-stu-id="62526-408"><span id="ISO_802.5_CRFP"></span><span id="iso_802.5_crfp"></span>**ISO 802.5 CRFP** (98)</span></span>
</dt> <dt>

<span data-ttu-id="62526-409"><span id="Myrinet"></span><span id="myrinet"></span><span id="MYRINET"></span>**Myrinet** (99)</span><span class="sxs-lookup"><span data-stu-id="62526-409"><span id="Myrinet"></span><span id="myrinet"></span><span id="MYRINET"></span>**Myrinet** (99)</span></span>
</dt> <dt>

<span data-ttu-id="62526-410"><span id="Voice_Receive_and_Transmit"></span><span id="voice_receive_and_transmit"></span><span id="VOICE_RECEIVE_AND_TRANSMIT"></span>**Réception et transmission vocales** (100)</span><span class="sxs-lookup"><span data-stu-id="62526-410"><span id="Voice_Receive_and_Transmit"></span><span id="voice_receive_and_transmit"></span><span id="VOICE_RECEIVE_AND_TRANSMIT"></span>**Voice Receive and Transmit** (100)</span></span>
</dt> <dt>

<span data-ttu-id="62526-411"><span id="Voice_Foreign_Exchange_Office"></span><span id="voice_foreign_exchange_office"></span><span id="VOICE_FOREIGN_EXCHANGE_OFFICE"></span>**Bureau étranger** à la voix (101)</span><span class="sxs-lookup"><span data-stu-id="62526-411"><span id="Voice_Foreign_Exchange_Office"></span><span id="voice_foreign_exchange_office"></span><span id="VOICE_FOREIGN_EXCHANGE_OFFICE"></span>**Voice Foreign Exchange Office** (101)</span></span>
</dt> <dt>

<span data-ttu-id="62526-412"><span id="Voice_Foreign_Exchange_Service"></span><span id="voice_foreign_exchange_service"></span><span id="VOICE_FOREIGN_EXCHANGE_SERVICE"></span>**Service d’échange étranger vocal** (102)</span><span class="sxs-lookup"><span data-stu-id="62526-412"><span id="Voice_Foreign_Exchange_Service"></span><span id="voice_foreign_exchange_service"></span><span id="VOICE_FOREIGN_EXCHANGE_SERVICE"></span>**Voice Foreign Exchange Service** (102)</span></span>
</dt> <dt>

<span data-ttu-id="62526-413"><span id="Voice_Encapsulation"></span><span id="voice_encapsulation"></span><span id="VOICE_ENCAPSULATION"></span>**Encapsulation vocale** (103)</span><span class="sxs-lookup"><span data-stu-id="62526-413"><span id="Voice_Encapsulation"></span><span id="voice_encapsulation"></span><span id="VOICE_ENCAPSULATION"></span>**Voice Encapsulation** (103)</span></span>
</dt> <dt>

<span data-ttu-id="62526-414"><span id="Voice_over_IP"></span><span id="voice_over_ip"></span><span id="VOICE_OVER_IP"></span>**Voix sur IP** (104)</span><span class="sxs-lookup"><span data-stu-id="62526-414"><span id="Voice_over_IP"></span><span id="voice_over_ip"></span><span id="VOICE_OVER_IP"></span>**Voice over IP** (104)</span></span>
</dt> <dt>

<span data-ttu-id="62526-415"><span id="ATM_DXI"></span><span id="atm_dxi"></span>**DXi ATM** (105)</span><span class="sxs-lookup"><span data-stu-id="62526-415"><span id="ATM_DXI"></span><span id="atm_dxi"></span>**ATM DXI** (105)</span></span>
</dt> <dt>

<span data-ttu-id="62526-416"><span id="ATM_FUNI"></span><span id="atm_funi"></span>**FUNI ATM** (106)</span><span class="sxs-lookup"><span data-stu-id="62526-416"><span id="ATM_FUNI"></span><span id="atm_funi"></span>**ATM FUNI** (106)</span></span>
</dt> <dt>

<span data-ttu-id="62526-417"><span id="ATM_IMA"></span><span id="atm_ima"></span>**Certificat IMA ATM** (107)</span><span class="sxs-lookup"><span data-stu-id="62526-417"><span id="ATM_IMA"></span><span id="atm_ima"></span>**ATM IMA** (107)</span></span>
</dt> <dt>

<span data-ttu-id="62526-418"><span id="PPP_Multilink_Bundle"></span><span id="ppp_multilink_bundle"></span><span id="PPP_MULTILINK_BUNDLE"></span>**Bundle à liaisons multiples PPP** (108)</span><span class="sxs-lookup"><span data-stu-id="62526-418"><span id="PPP_Multilink_Bundle"></span><span id="ppp_multilink_bundle"></span><span id="PPP_MULTILINK_BUNDLE"></span>**PPP Multilink Bundle** (108)</span></span>
</dt> <dt>

<span data-ttu-id="62526-419"><span id="IP_over_CDLC"></span><span id="ip_over_cdlc"></span><span id="IP_OVER_CDLC"></span>**IP sur CDLC** (109)</span><span class="sxs-lookup"><span data-stu-id="62526-419"><span id="IP_over_CDLC"></span><span id="ip_over_cdlc"></span><span id="IP_OVER_CDLC"></span>**IP over CDLC** (109)</span></span>
</dt> <dt>

<span data-ttu-id="62526-420"><span id="IP_over_CLAW"></span><span id="ip_over_claw"></span><span id="IP_OVER_CLAW"></span>**IP sur la griffe** (110)</span><span class="sxs-lookup"><span data-stu-id="62526-420"><span id="IP_over_CLAW"></span><span id="ip_over_claw"></span><span id="IP_OVER_CLAW"></span>**IP over CLAW** (110)</span></span>
</dt> <dt>

<span data-ttu-id="62526-421"><span id="Stack_to_Stack"></span><span id="stack_to_stack"></span><span id="STACK_TO_STACK"></span>**Pile à pile** (111)</span><span class="sxs-lookup"><span data-stu-id="62526-421"><span id="Stack_to_Stack"></span><span id="stack_to_stack"></span><span id="STACK_TO_STACK"></span>**Stack to Stack** (111)</span></span>
</dt> <dt>

<span data-ttu-id="62526-422"><span id="Virtual_IP_Address"></span><span id="virtual_ip_address"></span><span id="VIRTUAL_IP_ADDRESS"></span>**Adresse IP virtuelle** (112)</span><span class="sxs-lookup"><span data-stu-id="62526-422"><span id="Virtual_IP_Address"></span><span id="virtual_ip_address"></span><span id="VIRTUAL_IP_ADDRESS"></span>**Virtual IP Address** (112)</span></span>
</dt> <dt>

<span data-ttu-id="62526-423"><span id="MPC"></span><span id="mpc"></span>**MPC** (113)</span><span class="sxs-lookup"><span data-stu-id="62526-423"><span id="MPC"></span><span id="mpc"></span>**MPC** (113)</span></span>
</dt> <dt>

<span data-ttu-id="62526-424"><span id="IP_over_ATM"></span><span id="ip_over_atm"></span><span id="IP_OVER_ATM"></span>**IP sur ATM** (114)</span><span class="sxs-lookup"><span data-stu-id="62526-424"><span id="IP_over_ATM"></span><span id="ip_over_atm"></span><span id="IP_OVER_ATM"></span>**IP over ATM** (114)</span></span>
</dt> <dt>

<span data-ttu-id="62526-425"><span id="ISO_802.5j_Fibre_Token_Ring"></span><span id="iso_802.5j_fibre_token_ring"></span><span id="ISO_802.5J_FIBRE_TOKEN_RING"></span>Carte **Token Ring ISO 802.5 j** (115)</span><span class="sxs-lookup"><span data-stu-id="62526-425"><span id="ISO_802.5j_Fibre_Token_Ring"></span><span id="iso_802.5j_fibre_token_ring"></span><span id="ISO_802.5J_FIBRE_TOKEN_RING"></span>**ISO 802.5j Fibre Token Ring** (115)</span></span>
</dt> <dt>

<span data-ttu-id="62526-426"><span id="TDLC"></span><span id="tdlc"></span>**TDLC** (116)</span><span class="sxs-lookup"><span data-stu-id="62526-426"><span id="TDLC"></span><span id="tdlc"></span>**TDLC** (116)</span></span>
</dt> <dt>

<span data-ttu-id="62526-427"><span id="Gigabit_Ethernet"></span><span id="gigabit_ethernet"></span><span id="GIGABIT_ETHERNET"></span>**Gigabit Ethernet** (117)</span><span class="sxs-lookup"><span data-stu-id="62526-427"><span id="Gigabit_Ethernet"></span><span id="gigabit_ethernet"></span><span id="GIGABIT_ETHERNET"></span>**Gigabit Ethernet** (117)</span></span>
</dt> <dt>

<span data-ttu-id="62526-428"><span id="HDLC"></span><span id="hdlc"></span>**HDLC** (118)</span><span class="sxs-lookup"><span data-stu-id="62526-428"><span id="HDLC"></span><span id="hdlc"></span>**HDLC** (118)</span></span>
</dt> <dt>

<span data-ttu-id="62526-429"><span id="LAP-F"></span><span id="lap-f"></span>**Lap-F** (119)</span><span class="sxs-lookup"><span data-stu-id="62526-429"><span id="LAP-F"></span><span id="lap-f"></span>**LAP-F** (119)</span></span>
</dt> <dt>

<span data-ttu-id="62526-430"><span id="V.37"></span><span id="v.37"></span>**V. 37** (120)</span><span class="sxs-lookup"><span data-stu-id="62526-430"><span id="V.37"></span><span id="v.37"></span>**V.37** (120)</span></span>
</dt> <dt>

<span data-ttu-id="62526-431"><span id="X.25_MLP"></span><span id="x.25_mlp"></span>**MLP de X. 25** (121)</span><span class="sxs-lookup"><span data-stu-id="62526-431"><span id="X.25_MLP"></span><span id="x.25_mlp"></span>**X.25 MLP** (121)</span></span>
</dt> <dt>

<span data-ttu-id="62526-432"><span id="X.25_Hunt_Group"></span><span id="x.25_hunt_group"></span><span id="X.25_HUNT_GROUP"></span>**X. 25 groupe de recherche** (122)</span><span class="sxs-lookup"><span data-stu-id="62526-432"><span id="X.25_Hunt_Group"></span><span id="x.25_hunt_group"></span><span id="X.25_HUNT_GROUP"></span>**X.25 Hunt Group** (122)</span></span>
</dt> <dt>

<span data-ttu-id="62526-433"><span id="Transp_HDLC"></span><span id="transp_hdlc"></span><span id="TRANSP_HDLC"></span>**Domaine HDLC** (123)</span><span class="sxs-lookup"><span data-stu-id="62526-433"><span id="Transp_HDLC"></span><span id="transp_hdlc"></span><span id="TRANSP_HDLC"></span>**Transp HDLC** (123)</span></span>
</dt> <dt>

<span data-ttu-id="62526-434"><span id="Interleave_Channel"></span><span id="interleave_channel"></span><span id="INTERLEAVE_CHANNEL"></span>**Canal entrelacé** (124)</span><span class="sxs-lookup"><span data-stu-id="62526-434"><span id="Interleave_Channel"></span><span id="interleave_channel"></span><span id="INTERLEAVE_CHANNEL"></span>**Interleave Channel** (124)</span></span>
</dt> <dt>

<span data-ttu-id="62526-435"><span id="FAST_Channel"></span><span id="fast_channel"></span><span id="FAST_CHANNEL"></span>**Canal rapide** (125)</span><span class="sxs-lookup"><span data-stu-id="62526-435"><span id="FAST_Channel"></span><span id="fast_channel"></span><span id="FAST_CHANNEL"></span>**FAST Channel** (125)</span></span>
</dt> <dt>

<span data-ttu-id="62526-436"><span id="IP__for_APPN_HPR_in_IP_Networks_"></span><span id="ip__for_appn_hpr_in_ip_networks_"></span><span id="IP__FOR_APPN_HPR_IN_IP_NETWORKS_"></span>**IP (pour APPN HPR dans les réseaux IP)** (126)</span><span class="sxs-lookup"><span data-stu-id="62526-436"><span id="IP__for_APPN_HPR_in_IP_Networks_"></span><span id="ip__for_appn_hpr_in_ip_networks_"></span><span id="IP__FOR_APPN_HPR_IN_IP_NETWORKS_"></span>**IP (for APPN HPR in IP Networks)** (126)</span></span>
</dt> <dt>

<span data-ttu-id="62526-437"><span id="CATV_MAC_Layer"></span><span id="catv_mac_layer"></span><span id="CATV_MAC_LAYER"></span>**Couche MAC CATV** (127)</span><span class="sxs-lookup"><span data-stu-id="62526-437"><span id="CATV_MAC_Layer"></span><span id="catv_mac_layer"></span><span id="CATV_MAC_LAYER"></span>**CATV MAC Layer** (127)</span></span>
</dt> <dt>

<span data-ttu-id="62526-438"><span id="CATV_Downstream"></span><span id="catv_downstream"></span><span id="CATV_DOWNSTREAM"></span>**CATV en aval** (128)</span><span class="sxs-lookup"><span data-stu-id="62526-438"><span id="CATV_Downstream"></span><span id="catv_downstream"></span><span id="CATV_DOWNSTREAM"></span>**CATV Downstream** (128)</span></span>
</dt> <dt>

<span data-ttu-id="62526-439"><span id="CATV_Upstream"></span><span id="catv_upstream"></span><span id="CATV_UPSTREAM"></span>**CATV en amont** (129)</span><span class="sxs-lookup"><span data-stu-id="62526-439"><span id="CATV_Upstream"></span><span id="catv_upstream"></span><span id="CATV_UPSTREAM"></span>**CATV Upstream** (129)</span></span>
</dt> <dt>

<span data-ttu-id="62526-440"><span id="Avalon_12MPP_Switch"></span><span id="avalon_12mpp_switch"></span><span id="AVALON_12MPP_SWITCH"></span>**Commutateur 12MPP de Avalon** (130)</span><span class="sxs-lookup"><span data-stu-id="62526-440"><span id="Avalon_12MPP_Switch"></span><span id="avalon_12mpp_switch"></span><span id="AVALON_12MPP_SWITCH"></span>**Avalon 12MPP Switch** (130)</span></span>
</dt> <dt>

<span data-ttu-id="62526-441"><span id="Tunnel"></span><span id="tunnel"></span><span id="TUNNEL"></span>**Tunnel** (131)</span><span class="sxs-lookup"><span data-stu-id="62526-441"><span id="Tunnel"></span><span id="tunnel"></span><span id="TUNNEL"></span>**Tunnel** (131)</span></span>
</dt> <dt>

<span data-ttu-id="62526-442"><span id="Coffee"></span><span id="coffee"></span><span id="COFFEE"></span>**Café** (132)</span><span class="sxs-lookup"><span data-stu-id="62526-442"><span id="Coffee"></span><span id="coffee"></span><span id="COFFEE"></span>**Coffee** (132)</span></span>
</dt> <dt>

<span data-ttu-id="62526-443"><span id="Circuit_Emulation_Service"></span><span id="circuit_emulation_service"></span><span id="CIRCUIT_EMULATION_SERVICE"></span>**Service d’émulation de circuit** (133)</span><span class="sxs-lookup"><span data-stu-id="62526-443"><span id="Circuit_Emulation_Service"></span><span id="circuit_emulation_service"></span><span id="CIRCUIT_EMULATION_SERVICE"></span>**Circuit Emulation Service** (133)</span></span>
</dt> <dt>

<span data-ttu-id="62526-444"><span id="ATM_SubInterface"></span><span id="atm_subinterface"></span><span id="ATM_SUBINTERFACE"></span>Sous- **interface ATM** (134)</span><span class="sxs-lookup"><span data-stu-id="62526-444"><span id="ATM_SubInterface"></span><span id="atm_subinterface"></span><span id="ATM_SUBINTERFACE"></span>**ATM SubInterface** (134)</span></span>
</dt> <dt>

<span data-ttu-id="62526-445"><span id="Layer_2_VLAN_using_802.1Q"></span><span id="layer_2_vlan_using_802.1q"></span><span id="LAYER_2_VLAN_USING_802.1Q"></span>**VLAN de couche 2 avec 802.1 q** (135)</span><span class="sxs-lookup"><span data-stu-id="62526-445"><span id="Layer_2_VLAN_using_802.1Q"></span><span id="layer_2_vlan_using_802.1q"></span><span id="LAYER_2_VLAN_USING_802.1Q"></span>**Layer 2 VLAN using 802.1Q** (135)</span></span>
</dt> <dt>

<span data-ttu-id="62526-446"><span id="Layer_3_VLAN_using_IP"></span><span id="layer_3_vlan_using_ip"></span><span id="LAYER_3_VLAN_USING_IP"></span>**Réseau local virtuel de couche 3 utilisant IP** (136)</span><span class="sxs-lookup"><span data-stu-id="62526-446"><span id="Layer_3_VLAN_using_IP"></span><span id="layer_3_vlan_using_ip"></span><span id="LAYER_3_VLAN_USING_IP"></span>**Layer 3 VLAN using IP** (136)</span></span>
</dt> <dt>

<span data-ttu-id="62526-447"><span id="Layer_3_VLAN_using_IPX"></span><span id="layer_3_vlan_using_ipx"></span><span id="LAYER_3_VLAN_USING_IPX"></span>**Réseau local virtuel de couche 3 utilisant IPX** (137)</span><span class="sxs-lookup"><span data-stu-id="62526-447"><span id="Layer_3_VLAN_using_IPX"></span><span id="layer_3_vlan_using_ipx"></span><span id="LAYER_3_VLAN_USING_IPX"></span>**Layer 3 VLAN using IPX** (137)</span></span>
</dt> <dt>

<span data-ttu-id="62526-448"><span id="Digital_Power_Line"></span><span id="digital_power_line"></span><span id="DIGITAL_POWER_LINE"></span>**Power Line numérique** (138)</span><span class="sxs-lookup"><span data-stu-id="62526-448"><span id="Digital_Power_Line"></span><span id="digital_power_line"></span><span id="DIGITAL_POWER_LINE"></span>**Digital Power Line** (138)</span></span>
</dt> <dt>

<span data-ttu-id="62526-449"><span id="Multimedia_Mail_over_IP"></span><span id="multimedia_mail_over_ip"></span><span id="MULTIMEDIA_MAIL_OVER_IP"></span>**Messagerie multimédia sur IP** (139)</span><span class="sxs-lookup"><span data-stu-id="62526-449"><span id="Multimedia_Mail_over_IP"></span><span id="multimedia_mail_over_ip"></span><span id="MULTIMEDIA_MAIL_OVER_IP"></span>**Multimedia Mail over IP** (139)</span></span>
</dt> <dt>

<span data-ttu-id="62526-450"><span id="DTM"></span><span id="dtm"></span>**DTM** (140)</span><span class="sxs-lookup"><span data-stu-id="62526-450"><span id="DTM"></span><span id="dtm"></span>**DTM** (140)</span></span>
</dt> <dt>

<span data-ttu-id="62526-451"><span id="DCN"></span><span id="dcn"></span>**DCN** (141)</span><span class="sxs-lookup"><span data-stu-id="62526-451"><span id="DCN"></span><span id="dcn"></span>**DCN** (141)</span></span>
</dt> <dt>

<span data-ttu-id="62526-452"><span id="IP_Forwarding"></span><span id="ip_forwarding"></span><span id="IP_FORWARDING"></span>**Transfert IP** (142)</span><span class="sxs-lookup"><span data-stu-id="62526-452"><span id="IP_Forwarding"></span><span id="ip_forwarding"></span><span id="IP_FORWARDING"></span>**IP Forwarding** (142)</span></span>
</dt> <dt>

<span data-ttu-id="62526-453"><span id="MSDSL"></span><span id="msdsl"></span>**MSDS** (143)</span><span class="sxs-lookup"><span data-stu-id="62526-453"><span id="MSDSL"></span><span id="msdsl"></span>**MSDSL** (143)</span></span>
</dt> <dt>

<span data-ttu-id="62526-454"><span id="IEEE_1394"></span><span id="ieee_1394"></span>**IEEE 1394** (144)</span><span class="sxs-lookup"><span data-stu-id="62526-454"><span id="IEEE_1394"></span><span id="ieee_1394"></span>**IEEE 1394** (144)</span></span>
</dt> <dt>

<span data-ttu-id="62526-455"><span id="IF-GSN_HIPPI-6400"></span><span id="if-gsn_hippi-6400"></span>**If-GSN/hippai-6400** (145)</span><span class="sxs-lookup"><span data-stu-id="62526-455"><span id="IF-GSN_HIPPI-6400"></span><span id="if-gsn_hippi-6400"></span>**IF-GSN/HIPPI-6400** (145)</span></span>
</dt> <dt>

<span data-ttu-id="62526-456"><span id="DVB-RCC_MAC_Layer"></span><span id="dvb-rcc_mac_layer"></span><span id="DVB-RCC_MAC_LAYER"></span>**Couche MAC-RCC-RCC** (146)</span><span class="sxs-lookup"><span data-stu-id="62526-456"><span id="DVB-RCC_MAC_Layer"></span><span id="dvb-rcc_mac_layer"></span><span id="DVB-RCC_MAC_LAYER"></span>**DVB-RCC MAC Layer** (146)</span></span>
</dt> <dt>

<span data-ttu-id="62526-457"><span id="DVB-RCC_Downstream"></span><span id="dvb-rcc_downstream"></span><span id="DVB-RCC_DOWNSTREAM"></span>**DVB-RCC en aval** (147)</span><span class="sxs-lookup"><span data-stu-id="62526-457"><span id="DVB-RCC_Downstream"></span><span id="dvb-rcc_downstream"></span><span id="DVB-RCC_DOWNSTREAM"></span>**DVB-RCC Downstream** (147)</span></span>
</dt> <dt>

<span data-ttu-id="62526-458"><span id="DVB-RCC_Upstream"></span><span id="dvb-rcc_upstream"></span><span id="DVB-RCC_UPSTREAM"></span>**DVB-RCC en amont** (148)</span><span class="sxs-lookup"><span data-stu-id="62526-458"><span id="DVB-RCC_Upstream"></span><span id="dvb-rcc_upstream"></span><span id="DVB-RCC_UPSTREAM"></span>**DVB-RCC Upstream** (148)</span></span>
</dt> <dt>

<span data-ttu-id="62526-459"><span id="ATM_Virtual"></span><span id="atm_virtual"></span><span id="ATM_VIRTUAL"></span>**Virtuel ATM** (149)</span><span class="sxs-lookup"><span data-stu-id="62526-459"><span id="ATM_Virtual"></span><span id="atm_virtual"></span><span id="ATM_VIRTUAL"></span>**ATM Virtual** (149)</span></span>
</dt> <dt>

<span data-ttu-id="62526-460"><span id="MPLS_Tunnel"></span><span id="mpls_tunnel"></span><span id="MPLS_TUNNEL"></span>**Tunnel MPLS** (150)</span><span class="sxs-lookup"><span data-stu-id="62526-460"><span id="MPLS_Tunnel"></span><span id="mpls_tunnel"></span><span id="MPLS_TUNNEL"></span>**MPLS Tunnel** (150)</span></span>
</dt> <dt>

<span data-ttu-id="62526-461"><span id="SRP"></span><span id="srp"></span>**SRP** (151)</span><span class="sxs-lookup"><span data-stu-id="62526-461"><span id="SRP"></span><span id="srp"></span>**SRP** (151)</span></span>
</dt> <dt>

<span data-ttu-id="62526-462"><span id="Voice_over_ATM"></span><span id="voice_over_atm"></span><span id="VOICE_OVER_ATM"></span>**Voix sur ATM** (152)</span><span class="sxs-lookup"><span data-stu-id="62526-462"><span id="Voice_over_ATM"></span><span id="voice_over_atm"></span><span id="VOICE_OVER_ATM"></span>**Voice over ATM** (152)</span></span>
</dt> <dt>

<span data-ttu-id="62526-463"><span id="Voice_over_Frame_Relay"></span><span id="voice_over_frame_relay"></span><span id="VOICE_OVER_FRAME_RELAY"></span>**Voix sur relais de trame** (153)</span><span class="sxs-lookup"><span data-stu-id="62526-463"><span id="Voice_over_Frame_Relay"></span><span id="voice_over_frame_relay"></span><span id="VOICE_OVER_FRAME_RELAY"></span>**Voice over Frame Relay** (153)</span></span>
</dt> <dt>

<span data-ttu-id="62526-464"><span id="ISDL"></span><span id="isdl"></span>**ISDL** (154)</span><span class="sxs-lookup"><span data-stu-id="62526-464"><span id="ISDL"></span><span id="isdl"></span>**ISDL** (154)</span></span>
</dt> <dt>

<span data-ttu-id="62526-465"><span id="Composite_Link"></span><span id="composite_link"></span><span id="COMPOSITE_LINK"></span>**Lien composite** (155)</span><span class="sxs-lookup"><span data-stu-id="62526-465"><span id="Composite_Link"></span><span id="composite_link"></span><span id="COMPOSITE_LINK"></span>**Composite Link** (155)</span></span>
</dt> <dt>

<span data-ttu-id="62526-466"><span id="SS7_Signaling_Link"></span><span id="ss7_signaling_link"></span><span id="SS7_SIGNALING_LINK"></span>**Lien de signalisation SS7** (156)</span><span class="sxs-lookup"><span data-stu-id="62526-466"><span id="SS7_Signaling_Link"></span><span id="ss7_signaling_link"></span><span id="SS7_SIGNALING_LINK"></span>**SS7 Signaling Link** (156)</span></span>
</dt> <dt>

<span data-ttu-id="62526-467"><span id="Proprietary_P2P_Wireless"></span><span id="proprietary_p2p_wireless"></span><span id="PROPRIETARY_P2P_WIRELESS"></span>**Sans fil P2P propriétaire** (157)</span><span class="sxs-lookup"><span data-stu-id="62526-467"><span id="Proprietary_P2P_Wireless"></span><span id="proprietary_p2p_wireless"></span><span id="PROPRIETARY_P2P_WIRELESS"></span>**Proprietary P2P Wireless** (157)</span></span>
</dt> <dt>

<span data-ttu-id="62526-468"><span id="Frame_Forward"></span><span id="frame_forward"></span><span id="FRAME_FORWARD"></span>**Image vers l’avant** (158)</span><span class="sxs-lookup"><span data-stu-id="62526-468"><span id="Frame_Forward"></span><span id="frame_forward"></span><span id="FRAME_FORWARD"></span>**Frame Forward** (158)</span></span>
</dt> <dt>

<span data-ttu-id="62526-469"><span id="RFC1483_Multiprotocol_over_ATM"></span><span id="rfc1483_multiprotocol_over_atm"></span><span id="RFC1483_MULTIPROTOCOL_OVER_ATM"></span>**RFC1483 Multiprotocol sur ATM** (159)</span><span class="sxs-lookup"><span data-stu-id="62526-469"><span id="RFC1483_Multiprotocol_over_ATM"></span><span id="rfc1483_multiprotocol_over_atm"></span><span id="RFC1483_MULTIPROTOCOL_OVER_ATM"></span>**RFC1483 Multiprotocol over ATM** (159)</span></span>
</dt> <dt>

<span data-ttu-id="62526-470"><span id="USB"></span><span id="usb"></span>**USB** (160)</span><span class="sxs-lookup"><span data-stu-id="62526-470"><span id="USB"></span><span id="usb"></span>**USB** (160)</span></span>
</dt> <dt>

<span data-ttu-id="62526-471"><span id="IEEE_802.3ad_Link_Aggregate"></span><span id="ieee_802.3ad_link_aggregate"></span><span id="IEEE_802.3AD_LINK_AGGREGATE"></span>**Agrégat de liens ad IEEE 802.3** (161)</span><span class="sxs-lookup"><span data-stu-id="62526-471"><span id="IEEE_802.3ad_Link_Aggregate"></span><span id="ieee_802.3ad_link_aggregate"></span><span id="IEEE_802.3AD_LINK_AGGREGATE"></span>**IEEE 802.3ad Link Aggregate** (161)</span></span>
</dt> <dt>

<span data-ttu-id="62526-472"><span id="BGP_Policy_Accounting"></span><span id="bgp_policy_accounting"></span><span id="BGP_POLICY_ACCOUNTING"></span>**Gestion des stratégies BGP** (162)</span><span class="sxs-lookup"><span data-stu-id="62526-472"><span id="BGP_Policy_Accounting"></span><span id="bgp_policy_accounting"></span><span id="BGP_POLICY_ACCOUNTING"></span>**BGP Policy Accounting** (162)</span></span>
</dt> <dt>

<span data-ttu-id="62526-473"><span id="FRF_.16_Multilink_FR"></span><span id="frf_.16_multilink_fr"></span><span id="FRF_.16_MULTILINK_FR"></span>**FRF .16 Multilink fr** (163)</span><span class="sxs-lookup"><span data-stu-id="62526-473"><span id="FRF_.16_Multilink_FR"></span><span id="frf_.16_multilink_fr"></span><span id="FRF_.16_MULTILINK_FR"></span>**FRF .16 Multilink FR** (163)</span></span>
</dt> <dt>

<span data-ttu-id="62526-474"><span id="H.323_Gatekeeper"></span><span id="h.323_gatekeeper"></span><span id="H.323_GATEKEEPER"></span>**Gatekeeper H. 323** (164)</span><span class="sxs-lookup"><span data-stu-id="62526-474"><span id="H.323_Gatekeeper"></span><span id="h.323_gatekeeper"></span><span id="H.323_GATEKEEPER"></span>**H.323 Gatekeeper** (164)</span></span>
</dt> <dt>

<span data-ttu-id="62526-475"><span id="H.323_Proxy"></span><span id="h.323_proxy"></span><span id="H.323_PROXY"></span>**Proxy H. 323** (165)</span><span class="sxs-lookup"><span data-stu-id="62526-475"><span id="H.323_Proxy"></span><span id="h.323_proxy"></span><span id="H.323_PROXY"></span>**H.323 Proxy** (165)</span></span>
</dt> <dt>

<span data-ttu-id="62526-476"><span id="MPLS"></span><span id="mpls"></span>**MPLS** (166)</span><span class="sxs-lookup"><span data-stu-id="62526-476"><span id="MPLS"></span><span id="mpls"></span>**MPLS** (166)</span></span>
</dt> <dt>

<span data-ttu-id="62526-477"><span id="Multi-Frequency_Signaling_Link"></span><span id="multi-frequency_signaling_link"></span><span id="MULTI-FREQUENCY_SIGNALING_LINK"></span>**Lien de signalisation à plusieurs fréquences** (167)</span><span class="sxs-lookup"><span data-stu-id="62526-477"><span id="Multi-Frequency_Signaling_Link"></span><span id="multi-frequency_signaling_link"></span><span id="MULTI-FREQUENCY_SIGNALING_LINK"></span>**Multi-Frequency Signaling Link** (167)</span></span>
</dt> <dt>

<span data-ttu-id="62526-478"><span id="HDSL-2"></span><span id="hdsl-2"></span>**HDSL-2** (168)</span><span class="sxs-lookup"><span data-stu-id="62526-478"><span id="HDSL-2"></span><span id="hdsl-2"></span>**HDSL-2** (168)</span></span>
</dt> <dt>

<span data-ttu-id="62526-479"><span id="S-HDSL"></span><span id="s-hdsl"></span>**S-HDSL** (169)</span><span class="sxs-lookup"><span data-stu-id="62526-479"><span id="S-HDSL"></span><span id="s-hdsl"></span>**S-HDSL** (169)</span></span>
</dt> <dt>

<span data-ttu-id="62526-480"><span id="DS1_Facility_Data_Link"></span><span id="ds1_facility_data_link"></span><span id="DS1_FACILITY_DATA_LINK"></span>**Liaison de données de l’installation DS1** (170)</span><span class="sxs-lookup"><span data-stu-id="62526-480"><span id="DS1_Facility_Data_Link"></span><span id="ds1_facility_data_link"></span><span id="DS1_FACILITY_DATA_LINK"></span>**DS1 Facility Data Link** (170)</span></span>
</dt> <dt>

<span data-ttu-id="62526-481"><span id="Packet_over_SONET_SDH"></span><span id="packet_over_sonet_sdh"></span><span id="PACKET_OVER_SONET_SDH"></span>**Paquet sur SONET/SDH** (171)</span><span class="sxs-lookup"><span data-stu-id="62526-481"><span id="Packet_over_SONET_SDH"></span><span id="packet_over_sonet_sdh"></span><span id="PACKET_OVER_SONET_SDH"></span>**Packet over SONET/SDH** (171)</span></span>
</dt> <dt>

<span data-ttu-id="62526-482"><span id="DVB-ASI_Input"></span><span id="dvb-asi_input"></span><span id="DVB-ASI_INPUT"></span>**Entrée DVB-ASI** (172)</span><span class="sxs-lookup"><span data-stu-id="62526-482"><span id="DVB-ASI_Input"></span><span id="dvb-asi_input"></span><span id="DVB-ASI_INPUT"></span>**DVB-ASI Input** (172)</span></span>
</dt> <dt>

<span data-ttu-id="62526-483"><span id="DVB-ASI_Output"></span><span id="dvb-asi_output"></span><span id="DVB-ASI_OUTPUT"></span>**Sortie DVB-ASI** (173)</span><span class="sxs-lookup"><span data-stu-id="62526-483"><span id="DVB-ASI_Output"></span><span id="dvb-asi_output"></span><span id="DVB-ASI_OUTPUT"></span>**DVB-ASI Output** (173)</span></span>
</dt> <dt>

<span data-ttu-id="62526-484"><span id="Power_Line"></span><span id="power_line"></span><span id="POWER_LINE"></span>**Ligne électrique** (174)</span><span class="sxs-lookup"><span data-stu-id="62526-484"><span id="Power_Line"></span><span id="power_line"></span><span id="POWER_LINE"></span>**Power Line** (174)</span></span>
</dt> <dt>

<span data-ttu-id="62526-485"><span id="Non_Facility_Associated_Signaling"></span><span id="non_facility_associated_signaling"></span><span id="NON_FACILITY_ASSOCIATED_SIGNALING"></span>**Signal non associé à une installation** (175)</span><span class="sxs-lookup"><span data-stu-id="62526-485"><span id="Non_Facility_Associated_Signaling"></span><span id="non_facility_associated_signaling"></span><span id="NON_FACILITY_ASSOCIATED_SIGNALING"></span>**Non Facility Associated Signaling** (175)</span></span>
</dt> <dt>

<span data-ttu-id="62526-486"><span id="TR008"></span><span id="tr008"></span>**TR008** (176)</span><span class="sxs-lookup"><span data-stu-id="62526-486"><span id="TR008"></span><span id="tr008"></span>**TR008** (176)</span></span>
</dt> <dt>

<span data-ttu-id="62526-487"><span id="GR303_RDT"></span><span id="gr303_rdt"></span>**GR303 RDT** (177)</span><span class="sxs-lookup"><span data-stu-id="62526-487"><span id="GR303_RDT"></span><span id="gr303_rdt"></span>**GR303 RDT** (177)</span></span>
</dt> <dt>

<span data-ttu-id="62526-488"><span id="GR303_IDT"></span><span id="gr303_idt"></span>**GR303 IDT** (178)</span><span class="sxs-lookup"><span data-stu-id="62526-488"><span id="GR303_IDT"></span><span id="gr303_idt"></span>**GR303 IDT** (178)</span></span>
</dt> <dt>

<span data-ttu-id="62526-489"><span id="ISUP"></span><span id="isup"></span>**ISUP** (179)</span><span class="sxs-lookup"><span data-stu-id="62526-489"><span id="ISUP"></span><span id="isup"></span>**ISUP** (179)</span></span>
</dt> <dt>

<span data-ttu-id="62526-490"><span id="Proprietary_Wireless_MAC_Layer"></span><span id="proprietary_wireless_mac_layer"></span><span id="PROPRIETARY_WIRELESS_MAC_LAYER"></span>**Couche Mac sans fil propriétaire** (180)</span><span class="sxs-lookup"><span data-stu-id="62526-490"><span id="Proprietary_Wireless_MAC_Layer"></span><span id="proprietary_wireless_mac_layer"></span><span id="PROPRIETARY_WIRELESS_MAC_LAYER"></span>**Proprietary Wireless MAC Layer** (180)</span></span>
</dt> <dt>

<span data-ttu-id="62526-491"><span id="Proprietary_Wireless_Downstream"></span><span id="proprietary_wireless_downstream"></span><span id="PROPRIETARY_WIRELESS_DOWNSTREAM"></span>En **aval sans fil propriétaire** (181)</span><span class="sxs-lookup"><span data-stu-id="62526-491"><span id="Proprietary_Wireless_Downstream"></span><span id="proprietary_wireless_downstream"></span><span id="PROPRIETARY_WIRELESS_DOWNSTREAM"></span>**Proprietary Wireless Downstream** (181)</span></span>
</dt> <dt>

<span data-ttu-id="62526-492"><span id="Proprietary_Wireless_Upstream"></span><span id="proprietary_wireless_upstream"></span><span id="PROPRIETARY_WIRELESS_UPSTREAM"></span>**Flux de communication sans fil propriétaire** (182)</span><span class="sxs-lookup"><span data-stu-id="62526-492"><span id="Proprietary_Wireless_Upstream"></span><span id="proprietary_wireless_upstream"></span><span id="PROPRIETARY_WIRELESS_UPSTREAM"></span>**Proprietary Wireless Upstream** (182)</span></span>
</dt> <dt>

<span data-ttu-id="62526-493"><span id="HIPERLAN_Type_2"></span><span id="hiperlan_type_2"></span><span id="HIPERLAN_TYPE_2"></span>**HiperLAN type 2** (183)</span><span class="sxs-lookup"><span data-stu-id="62526-493"><span id="HIPERLAN_Type_2"></span><span id="hiperlan_type_2"></span><span id="HIPERLAN_TYPE_2"></span>**HIPERLAN Type 2** (183)</span></span>
</dt> <dt>

<span data-ttu-id="62526-494"><span id="Proprietary_Broadband_Wireless_Access_Point_to_Multipoint"></span><span id="proprietary_broadband_wireless_access_point_to_multipoint"></span><span id="PROPRIETARY_BROADBAND_WIRELESS_ACCESS_POINT_TO_MULTIPOINT"></span>**Point d’accès sans fil haut débit propriétaire sur multipoint** (184)</span><span class="sxs-lookup"><span data-stu-id="62526-494"><span id="Proprietary_Broadband_Wireless_Access_Point_to_Multipoint"></span><span id="proprietary_broadband_wireless_access_point_to_multipoint"></span><span id="PROPRIETARY_BROADBAND_WIRELESS_ACCESS_POINT_TO_MULTIPOINT"></span>**Proprietary Broadband Wireless Access Point to Multipoint** (184)</span></span>
</dt> <dt>

<span data-ttu-id="62526-495"><span id="SONET_Overhead_Channel"></span><span id="sonet_overhead_channel"></span><span id="SONET_OVERHEAD_CHANNEL"></span>**Canal de surcharge SONET** (185)</span><span class="sxs-lookup"><span data-stu-id="62526-495"><span id="SONET_Overhead_Channel"></span><span id="sonet_overhead_channel"></span><span id="SONET_OVERHEAD_CHANNEL"></span>**SONET Overhead Channel** (185)</span></span>
</dt> <dt>

<span data-ttu-id="62526-496"><span id="Digital_Wrapper_Overhead_Channel"></span><span id="digital_wrapper_overhead_channel"></span><span id="DIGITAL_WRAPPER_OVERHEAD_CHANNEL"></span>**Canal de surcharge du wrapper numérique** (186)</span><span class="sxs-lookup"><span data-stu-id="62526-496"><span id="Digital_Wrapper_Overhead_Channel"></span><span id="digital_wrapper_overhead_channel"></span><span id="DIGITAL_WRAPPER_OVERHEAD_CHANNEL"></span>**Digital Wrapper Overhead Channel** (186)</span></span>
</dt> <dt>

<span data-ttu-id="62526-497"><span id="ATM_Adaptation_Layer_2"></span><span id="atm_adaptation_layer_2"></span><span id="ATM_ADAPTATION_LAYER_2"></span>**Couche d’adaptation ATM 2** (187)</span><span class="sxs-lookup"><span data-stu-id="62526-497"><span id="ATM_Adaptation_Layer_2"></span><span id="atm_adaptation_layer_2"></span><span id="ATM_ADAPTATION_LAYER_2"></span>**ATM Adaptation Layer 2** (187)</span></span>
</dt> <dt>

<span data-ttu-id="62526-498"><span id="Radio_MAC"></span><span id="radio_mac"></span><span id="RADIO_MAC"></span>**Mac radio** (188)</span><span class="sxs-lookup"><span data-stu-id="62526-498"><span id="Radio_MAC"></span><span id="radio_mac"></span><span id="RADIO_MAC"></span>**Radio MAC** (188)</span></span>
</dt> <dt>

<span data-ttu-id="62526-499"><span id="ATM_Radio"></span><span id="atm_radio"></span><span id="ATM_RADIO"></span>**Radio ATM** (189)</span><span class="sxs-lookup"><span data-stu-id="62526-499"><span id="ATM_Radio"></span><span id="atm_radio"></span><span id="ATM_RADIO"></span>**ATM Radio** (189)</span></span>
</dt> <dt>

<span data-ttu-id="62526-500"><span id="Inter_Machine_Trunk"></span><span id="inter_machine_trunk"></span><span id="INTER_MACHINE_TRUNK"></span>**Trunk inter-machine** (190)</span><span class="sxs-lookup"><span data-stu-id="62526-500"><span id="Inter_Machine_Trunk"></span><span id="inter_machine_trunk"></span><span id="INTER_MACHINE_TRUNK"></span>**Inter Machine Trunk** (190)</span></span>
</dt> <dt>

<span data-ttu-id="62526-501"><span id="MVL_DSL"></span><span id="mvl_dsl"></span>**MVL DSL** (191)</span><span class="sxs-lookup"><span data-stu-id="62526-501"><span id="MVL_DSL"></span><span id="mvl_dsl"></span>**MVL DSL** (191)</span></span>
</dt> <dt>

<span data-ttu-id="62526-502"><span id="Long_Read_DSL"></span><span id="long_read_dsl"></span><span id="LONG_READ_DSL"></span>**Long lecture DSL** (192)</span><span class="sxs-lookup"><span data-stu-id="62526-502"><span id="Long_Read_DSL"></span><span id="long_read_dsl"></span><span id="LONG_READ_DSL"></span>**Long Read DSL** (192)</span></span>
</dt> <dt>

<span data-ttu-id="62526-503"><span id="Frame_Relay_DLCI_Endpoint"></span><span id="frame_relay_dlci_endpoint"></span><span id="FRAME_RELAY_DLCI_ENDPOINT"></span>**Point de terminaison DLCI de relais de trame** (193)</span><span class="sxs-lookup"><span data-stu-id="62526-503"><span id="Frame_Relay_DLCI_Endpoint"></span><span id="frame_relay_dlci_endpoint"></span><span id="FRAME_RELAY_DLCI_ENDPOINT"></span>**Frame Relay DLCI Endpoint** (193)</span></span>
</dt> <dt>

<span data-ttu-id="62526-504"><span id="ATM_VCI_Endpoint"></span><span id="atm_vci_endpoint"></span><span id="ATM_VCI_ENDPOINT"></span>**Point de terminaison VCI ATM** (194)</span><span class="sxs-lookup"><span data-stu-id="62526-504"><span id="ATM_VCI_Endpoint"></span><span id="atm_vci_endpoint"></span><span id="ATM_VCI_ENDPOINT"></span>**ATM VCI Endpoint** (194)</span></span>
</dt> <dt>

<span data-ttu-id="62526-505"><span id="Optical_Channel"></span><span id="optical_channel"></span><span id="OPTICAL_CHANNEL"></span>**Canal optique** (195)</span><span class="sxs-lookup"><span data-stu-id="62526-505"><span id="Optical_Channel"></span><span id="optical_channel"></span><span id="OPTICAL_CHANNEL"></span>**Optical Channel** (195)</span></span>
</dt> <dt>

<span data-ttu-id="62526-506"><span id="Optical_Transport"></span><span id="optical_transport"></span><span id="OPTICAL_TRANSPORT"></span>**Transport optique** (196)</span><span class="sxs-lookup"><span data-stu-id="62526-506"><span id="Optical_Transport"></span><span id="optical_transport"></span><span id="OPTICAL_TRANSPORT"></span>**Optical Transport** (196)</span></span>
</dt> <dt>

<span data-ttu-id="62526-507"><span id="Proprietary_ATM"></span><span id="proprietary_atm"></span><span id="PROPRIETARY_ATM"></span>**ATM propriétaire** (197)</span><span class="sxs-lookup"><span data-stu-id="62526-507"><span id="Proprietary_ATM"></span><span id="proprietary_atm"></span><span id="PROPRIETARY_ATM"></span>**Proprietary ATM** (197)</span></span>
</dt> <dt>

<span data-ttu-id="62526-508"><span id="Voice_over_Cable"></span><span id="voice_over_cable"></span><span id="VOICE_OVER_CABLE"></span>**Câble vocal** (198)</span><span class="sxs-lookup"><span data-stu-id="62526-508"><span id="Voice_over_Cable"></span><span id="voice_over_cable"></span><span id="VOICE_OVER_CABLE"></span>**Voice over Cable** (198)</span></span>
</dt> <dt>

<span data-ttu-id="62526-509"><span id="Infiniband"></span><span id="infiniband"></span><span id="INFINIBAND"></span>**InfiniBand** (199)</span><span class="sxs-lookup"><span data-stu-id="62526-509"><span id="Infiniband"></span><span id="infiniband"></span><span id="INFINIBAND"></span>**Infiniband** (199)</span></span>
</dt> <dt>

<span data-ttu-id="62526-510"><span id="TE_Link"></span><span id="te_link"></span><span id="TE_LINK"></span>**Lien te** (200)</span><span class="sxs-lookup"><span data-stu-id="62526-510"><span id="TE_Link"></span><span id="te_link"></span><span id="TE_LINK"></span>**TE Link** (200)</span></span>
</dt> <dt>

<span data-ttu-id="62526-511"><span id="Q.2931"></span><span id="q.2931"></span>**Q. 2931** (201)</span><span class="sxs-lookup"><span data-stu-id="62526-511"><span id="Q.2931"></span><span id="q.2931"></span>**Q.2931** (201)</span></span>
</dt> <dt>

<span data-ttu-id="62526-512"><span id="Virtual_Trunk_Group"></span><span id="virtual_trunk_group"></span><span id="VIRTUAL_TRUNK_GROUP"></span>**Groupe Trunk virtuel** (202)</span><span class="sxs-lookup"><span data-stu-id="62526-512"><span id="Virtual_Trunk_Group"></span><span id="virtual_trunk_group"></span><span id="VIRTUAL_TRUNK_GROUP"></span>**Virtual Trunk Group** (202)</span></span>
</dt> <dt>

<span data-ttu-id="62526-513"><span id="SIP_Trunk_Group"></span><span id="sip_trunk_group"></span><span id="SIP_TRUNK_GROUP"></span>**Groupe SIP Trunk** (203)</span><span class="sxs-lookup"><span data-stu-id="62526-513"><span id="SIP_Trunk_Group"></span><span id="sip_trunk_group"></span><span id="SIP_TRUNK_GROUP"></span>**SIP Trunk Group** (203)</span></span>
</dt> <dt>

<span data-ttu-id="62526-514"><span id="SIP_Signaling"></span><span id="sip_signaling"></span><span id="SIP_SIGNALING"></span>**Signalisation SIP** (204)</span><span class="sxs-lookup"><span data-stu-id="62526-514"><span id="SIP_Signaling"></span><span id="sip_signaling"></span><span id="SIP_SIGNALING"></span>**SIP Signaling** (204)</span></span>
</dt> <dt>

<span data-ttu-id="62526-515"><span id="CATV_Upstream_Channel"></span><span id="catv_upstream_channel"></span><span id="CATV_UPSTREAM_CHANNEL"></span>**Canal CATV en amont** (205)</span><span class="sxs-lookup"><span data-stu-id="62526-515"><span id="CATV_Upstream_Channel"></span><span id="catv_upstream_channel"></span><span id="CATV_UPSTREAM_CHANNEL"></span>**CATV Upstream Channel** (205)</span></span>
</dt> <dt>

<span data-ttu-id="62526-516"><span id="Econet"></span><span id="econet"></span><span id="ECONET"></span>**Econet** (206)</span><span class="sxs-lookup"><span data-stu-id="62526-516"><span id="Econet"></span><span id="econet"></span><span id="ECONET"></span>**Econet** (206)</span></span>
</dt> <dt>

<span data-ttu-id="62526-517"><span id="FSAN_155Mb_PON"></span><span id="fsan_155mb_pon"></span><span id="FSAN_155MB_PON"></span>**FSAN 155MB PON** (207)</span><span class="sxs-lookup"><span data-stu-id="62526-517"><span id="FSAN_155Mb_PON"></span><span id="fsan_155mb_pon"></span><span id="FSAN_155MB_PON"></span>**FSAN 155Mb PON** (207)</span></span>
</dt> <dt>

<span data-ttu-id="62526-518"><span id="FSAN_622Mb_PON"></span><span id="fsan_622mb_pon"></span><span id="FSAN_622MB_PON"></span>**FSAN 622MB PON** (208)</span><span class="sxs-lookup"><span data-stu-id="62526-518"><span id="FSAN_622Mb_PON"></span><span id="fsan_622mb_pon"></span><span id="FSAN_622MB_PON"></span>**FSAN 622Mb PON** (208)</span></span>
</dt> <dt>

<span data-ttu-id="62526-519"><span id="Transparent_Bridge"></span><span id="transparent_bridge"></span><span id="TRANSPARENT_BRIDGE"></span>**Pont transparent** (209)</span><span class="sxs-lookup"><span data-stu-id="62526-519"><span id="Transparent_Bridge"></span><span id="transparent_bridge"></span><span id="TRANSPARENT_BRIDGE"></span>**Transparent Bridge** (209)</span></span>
</dt> <dt>

<span data-ttu-id="62526-520"><span id="Line_Group"></span><span id="line_group"></span><span id="LINE_GROUP"></span>**Groupe de lignes** (210)</span><span class="sxs-lookup"><span data-stu-id="62526-520"><span id="Line_Group"></span><span id="line_group"></span><span id="LINE_GROUP"></span>**Line Group** (210)</span></span>
</dt> <dt>

<span data-ttu-id="62526-521"><span id="Voice___Feature_Group"></span><span id="voice___feature_group"></span><span id="VOICE___FEATURE_GROUP"></span>**Groupe de fonctionnalités de & vocal** (211)</span><span class="sxs-lookup"><span data-stu-id="62526-521"><span id="Voice___Feature_Group"></span><span id="voice___feature_group"></span><span id="VOICE___FEATURE_GROUP"></span>**Voice & Feature Group** (211)</span></span>
</dt> <dt>

<span data-ttu-id="62526-522"><span id="Voice_FGD_EANA"></span><span id="voice_fgd_eana"></span><span id="VOICE_FGD_EANA"></span>**Voix FGD eana** (212)</span><span class="sxs-lookup"><span data-stu-id="62526-522"><span id="Voice_FGD_EANA"></span><span id="voice_fgd_eana"></span><span id="VOICE_FGD_EANA"></span>**Voice FGD EANA** (212)</span></span>
</dt> <dt>

<span data-ttu-id="62526-523"><span id="Voice_DID"></span><span id="voice_did"></span><span id="VOICE_DID"></span>**Voix** (213)</span><span class="sxs-lookup"><span data-stu-id="62526-523"><span id="Voice_DID"></span><span id="voice_did"></span><span id="VOICE_DID"></span>**Voice DID** (213)</span></span>
</dt> <dt>

<span data-ttu-id="62526-524"><span id="MPEG_Transport"></span><span id="mpeg_transport"></span><span id="MPEG_TRANSPORT"></span>**Transport MPEG** (214)</span><span class="sxs-lookup"><span data-stu-id="62526-524"><span id="MPEG_Transport"></span><span id="mpeg_transport"></span><span id="MPEG_TRANSPORT"></span>**MPEG Transport** (214)</span></span>
</dt> <dt>

<span data-ttu-id="62526-525"><span id="6To4"></span><span id="6to4"></span><span id="6TO4"></span>**6to4** (215)</span><span class="sxs-lookup"><span data-stu-id="62526-525"><span id="6To4"></span><span id="6to4"></span><span id="6TO4"></span>**6To4** (215)</span></span>
</dt> <dt>

<span data-ttu-id="62526-526"><span id="GTP"></span><span id="gtp"></span>**GTP** (216)</span><span class="sxs-lookup"><span data-stu-id="62526-526"><span id="GTP"></span><span id="gtp"></span>**GTP** (216)</span></span>
</dt> <dt>

<span data-ttu-id="62526-527"><span id="Paradyne_EtherLoop_1"></span><span id="paradyne_etherloop_1"></span><span id="PARADYNE_ETHERLOOP_1"></span>**Paradyne EtherLoop 1** (217)</span><span class="sxs-lookup"><span data-stu-id="62526-527"><span id="Paradyne_EtherLoop_1"></span><span id="paradyne_etherloop_1"></span><span id="PARADYNE_ETHERLOOP_1"></span>**Paradyne EtherLoop 1** (217)</span></span>
</dt> <dt>

<span data-ttu-id="62526-528"><span id="Paradyne_EtherLoop_2"></span><span id="paradyne_etherloop_2"></span><span id="PARADYNE_ETHERLOOP_2"></span>**Paradyne EtherLoop 2** (218)</span><span class="sxs-lookup"><span data-stu-id="62526-528"><span id="Paradyne_EtherLoop_2"></span><span id="paradyne_etherloop_2"></span><span id="PARADYNE_ETHERLOOP_2"></span>**Paradyne EtherLoop 2** (218)</span></span>
</dt> <dt>

<span data-ttu-id="62526-529"><span id="Optical_Channel_Group"></span><span id="optical_channel_group"></span><span id="OPTICAL_CHANNEL_GROUP"></span>**Groupe de canaux optiques** (219)</span><span class="sxs-lookup"><span data-stu-id="62526-529"><span id="Optical_Channel_Group"></span><span id="optical_channel_group"></span><span id="OPTICAL_CHANNEL_GROUP"></span>**Optical Channel Group** (219)</span></span>
</dt> <dt>

<span data-ttu-id="62526-530"><span id="HomePNA"></span><span id="homepna"></span><span id="HOMEPNA"></span>**HomePNA** (220)</span><span class="sxs-lookup"><span data-stu-id="62526-530"><span id="HomePNA"></span><span id="homepna"></span><span id="HOMEPNA"></span>**HomePNA** (220)</span></span>
</dt> <dt>

<span data-ttu-id="62526-531"><span id="GFP"></span><span id="gfp"></span>**GFP** (221)</span><span class="sxs-lookup"><span data-stu-id="62526-531"><span id="GFP"></span><span id="gfp"></span>**GFP** (221)</span></span>
</dt> <dt>

<span data-ttu-id="62526-532"><span id="ciscoISLvlan"></span><span id="ciscoislvlan"></span><span id="CISCOISLVLAN"></span>**ciscoISLvlan** (222)</span><span class="sxs-lookup"><span data-stu-id="62526-532"><span id="ciscoISLvlan"></span><span id="ciscoislvlan"></span><span id="CISCOISLVLAN"></span>**ciscoISLvlan** (222)</span></span>
</dt> <dt>

<span data-ttu-id="62526-533"><span id="actelisMetaLOOP"></span><span id="actelismetaloop"></span><span id="ACTELISMETALOOP"></span>**actelisMetaLOOP** (223)</span><span class="sxs-lookup"><span data-stu-id="62526-533"><span id="actelisMetaLOOP"></span><span id="actelismetaloop"></span><span id="ACTELISMETALOOP"></span>**actelisMetaLOOP** (223)</span></span>
</dt> <dt>

<span data-ttu-id="62526-534"><span id="Fcip"></span><span id="fcip"></span><span id="FCIP"></span>**FCIP** (224)</span><span class="sxs-lookup"><span data-stu-id="62526-534"><span id="Fcip"></span><span id="fcip"></span><span id="FCIP"></span>**Fcip** (224)</span></span>
</dt> <dt>

<span data-ttu-id="62526-535"><span id="IANA_Reserved"></span><span id="iana_reserved"></span><span id="IANA_RESERVED"></span>**IANA réservé** (225.. 4095)</span><span class="sxs-lookup"><span data-stu-id="62526-535"><span id="IANA_Reserved"></span><span id="iana_reserved"></span><span id="IANA_RESERVED"></span>**IANA Reserved** (225..4095)</span></span>
</dt> <dt>

<span data-ttu-id="62526-536"><span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>**IPv4** (4096)</span><span class="sxs-lookup"><span data-stu-id="62526-536"><span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>**IPv4** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="62526-537"><span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>**IPv6** (4097)</span><span class="sxs-lookup"><span data-stu-id="62526-537"><span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>**IPv6** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="62526-538"><span id="IPv4_v6"></span><span id="ipv4_v6"></span><span id="IPV4_V6"></span>**IPv4/v6** (4098)</span><span class="sxs-lookup"><span data-stu-id="62526-538"><span id="IPv4_v6"></span><span id="ipv4_v6"></span><span id="IPV4_V6"></span>**IPv4/v6** (4098)</span></span>
</dt> <dt>

<span data-ttu-id="62526-539"><span id="IPX"></span><span id="ipx"></span>**IPX** (4099)</span><span class="sxs-lookup"><span data-stu-id="62526-539"><span id="IPX"></span><span id="ipx"></span>**IPX** (4099)</span></span>
</dt> <dt>

<span data-ttu-id="62526-540"><span id="DECnet"></span><span id="decnet"></span><span id="DECNET"></span>**DECnet** (4100)</span><span class="sxs-lookup"><span data-stu-id="62526-540"><span id="DECnet"></span><span id="decnet"></span><span id="DECNET"></span>**DECnet** (4100)</span></span>
</dt> <dt>

<span data-ttu-id="62526-541"><span id="SNA"></span><span id="sna"></span>**SNA** (4101)</span><span class="sxs-lookup"><span data-stu-id="62526-541"><span id="SNA"></span><span id="sna"></span>**SNA** (4101)</span></span>
</dt> <dt>

<span data-ttu-id="62526-542"><span id="CONP"></span><span id="conp"></span>**CONP** (4102)</span><span class="sxs-lookup"><span data-stu-id="62526-542"><span id="CONP"></span><span id="conp"></span>**CONP** (4102)</span></span>
</dt> <dt>

<span data-ttu-id="62526-543"><span id="CLNP"></span><span id="clnp"></span>**CLNP** (4103)</span><span class="sxs-lookup"><span data-stu-id="62526-543"><span id="CLNP"></span><span id="clnp"></span>**CLNP** (4103)</span></span>
</dt> <dt>

<span data-ttu-id="62526-544"><span id="VINES"></span><span id="vines"></span>**Vignes** (4104)</span><span class="sxs-lookup"><span data-stu-id="62526-544"><span id="VINES"></span><span id="vines"></span>**VINES** (4104)</span></span>
</dt> <dt>

<span data-ttu-id="62526-545"><span id="XNS"></span><span id="xns"></span>**XNS** (4105)</span><span class="sxs-lookup"><span data-stu-id="62526-545"><span id="XNS"></span><span id="xns"></span>**XNS** (4105)</span></span>
</dt> <dt>

<span data-ttu-id="62526-546"><span id="ISDN_B_Channel_Endpoint"></span><span id="isdn_b_channel_endpoint"></span><span id="ISDN_B_CHANNEL_ENDPOINT"></span>**Point de terminaison de canal B RNIS** (4106)</span><span class="sxs-lookup"><span data-stu-id="62526-546"><span id="ISDN_B_Channel_Endpoint"></span><span id="isdn_b_channel_endpoint"></span><span id="ISDN_B_CHANNEL_ENDPOINT"></span>**ISDN B Channel Endpoint** (4106)</span></span>
</dt> <dt>

<span data-ttu-id="62526-547"><span id="ISDN_D_Channel_Endpoint"></span><span id="isdn_d_channel_endpoint"></span><span id="ISDN_D_CHANNEL_ENDPOINT"></span>**Point de terminaison de canal D RNIS** (4107)</span><span class="sxs-lookup"><span data-stu-id="62526-547"><span id="ISDN_D_Channel_Endpoint"></span><span id="isdn_d_channel_endpoint"></span><span id="ISDN_D_CHANNEL_ENDPOINT"></span>**ISDN D Channel Endpoint** (4107)</span></span>
</dt> <dt>

<span data-ttu-id="62526-548"><span id="BGP"></span><span id="bgp"></span>**BGP** (4108)</span><span class="sxs-lookup"><span data-stu-id="62526-548"><span id="BGP"></span><span id="bgp"></span>**BGP** (4108)</span></span>
</dt> <dt>

<span data-ttu-id="62526-549"><span id="OSPF"></span><span id="ospf"></span>**OSPF** (4109)</span><span class="sxs-lookup"><span data-stu-id="62526-549"><span id="OSPF"></span><span id="ospf"></span>**OSPF** (4109)</span></span>
</dt> <dt>

<span data-ttu-id="62526-550"><span id="UDP"></span><span id="udp"></span>**UDP** (4110)</span><span class="sxs-lookup"><span data-stu-id="62526-550"><span id="UDP"></span><span id="udp"></span>**UDP** (4110)</span></span>
</dt> <dt>

<span data-ttu-id="62526-551"><span id="TCP"></span><span id="tcp"></span>**TCP** (4111)</span><span class="sxs-lookup"><span data-stu-id="62526-551"><span id="TCP"></span><span id="tcp"></span>**TCP** (4111)</span></span>
</dt> <dt>

<span data-ttu-id="62526-552"><span id="802.11a"></span><span id="802.11A"></span>**802.11 a** (4112)</span><span class="sxs-lookup"><span data-stu-id="62526-552"><span id="802.11a"></span><span id="802.11A"></span>**802.11a** (4112)</span></span>
</dt> <dt>

<span data-ttu-id="62526-553"><span id="802.11b"></span><span id="802.11B"></span>**802.11 b** (4113)</span><span class="sxs-lookup"><span data-stu-id="62526-553"><span id="802.11b"></span><span id="802.11B"></span>**802.11b** (4113)</span></span>
</dt> <dt>

<span data-ttu-id="62526-554"><span id="802.11g"></span><span id="802.11G"></span>**802.11 g** (4114)</span><span class="sxs-lookup"><span data-stu-id="62526-554"><span id="802.11g"></span><span id="802.11G"></span>**802.11g** (4114)</span></span>
</dt> <dt>

<span data-ttu-id="62526-555"><span id="802.11h"></span><span id="802.11H"></span>**802.11 h** (4115)</span><span class="sxs-lookup"><span data-stu-id="62526-555"><span id="802.11h"></span><span id="802.11H"></span>**802.11h** (4115)</span></span>
</dt> <dt>

<span data-ttu-id="62526-556"><span id="NFS"></span><span id="nfs"></span>**NFS** (4200)</span><span class="sxs-lookup"><span data-stu-id="62526-556"><span id="NFS"></span><span id="nfs"></span>**NFS** (4200)</span></span>
</dt> <dt>

<span data-ttu-id="62526-557"><span id="CIFS"></span><span id="cifs"></span>**CIFS** (4201)</span><span class="sxs-lookup"><span data-stu-id="62526-557"><span id="CIFS"></span><span id="cifs"></span>**CIFS** (4201)</span></span>
</dt> <dt>

<span data-ttu-id="62526-558"><span id="DAFS"></span><span id="dafs"></span>**DAFS** (4202)</span><span class="sxs-lookup"><span data-stu-id="62526-558"><span id="DAFS"></span><span id="dafs"></span>**DAFS** (4202)</span></span>
</dt> <dt>

<span data-ttu-id="62526-559"><span id="WebDAV"></span><span id="webdav"></span><span id="WEBDAV"></span>**WebDAV** (4203)</span><span class="sxs-lookup"><span data-stu-id="62526-559"><span id="WebDAV"></span><span id="webdav"></span><span id="WEBDAV"></span>**WebDAV** (4203)</span></span>
</dt> <dt>

<span data-ttu-id="62526-560"><span id="HTTP"></span><span id="http"></span>**Http** (4204)</span><span class="sxs-lookup"><span data-stu-id="62526-560"><span id="HTTP"></span><span id="http"></span>**HTTP** (4204)</span></span>
</dt> <dt>

<span data-ttu-id="62526-561"><span id="FTP"></span><span id="ftp"></span>**FTP** (4205)</span><span class="sxs-lookup"><span data-stu-id="62526-561"><span id="FTP"></span><span id="ftp"></span>**FTP** (4205)</span></span>
</dt> <dt>

<span data-ttu-id="62526-562"><span id="NDMP"></span><span id="ndmp"></span>**NDMP** (4300)</span><span class="sxs-lookup"><span data-stu-id="62526-562"><span id="NDMP"></span><span id="ndmp"></span>**NDMP** (4300)</span></span>
</dt> <dt>

<span data-ttu-id="62526-563"><span id="Telnet"></span><span id="telnet"></span><span id="TELNET"></span>**Telnet** (4400)</span><span class="sxs-lookup"><span data-stu-id="62526-563"><span id="Telnet"></span><span id="telnet"></span><span id="TELNET"></span>**Telnet** (4400)</span></span>
</dt> <dt>

<span data-ttu-id="62526-564"><span id="SSH"></span><span id="ssh"></span>**SSH** (4401)</span><span class="sxs-lookup"><span data-stu-id="62526-564"><span id="SSH"></span><span id="ssh"></span>**SSH** (4401)</span></span>
</dt> <dt>

<span data-ttu-id="62526-565"><span id="SM_CLP"></span><span id="sm_clp"></span>**SM CLP** (4402)</span><span class="sxs-lookup"><span data-stu-id="62526-565"><span id="SM_CLP"></span><span id="sm_clp"></span>**SM CLP** (4402)</span></span>
</dt> <dt>

<span data-ttu-id="62526-566"><span id="SMTP"></span><span id="smtp"></span>**SMTP** (4403)</span><span class="sxs-lookup"><span data-stu-id="62526-566"><span id="SMTP"></span><span id="smtp"></span>**SMTP** (4403)</span></span>
</dt> <dt>

<span data-ttu-id="62526-567"><span id="LDAP"></span><span id="ldap"></span>**LDAP** (4404)</span><span class="sxs-lookup"><span data-stu-id="62526-567"><span id="LDAP"></span><span id="ldap"></span>**LDAP** (4404)</span></span>
</dt> <dt>

<span data-ttu-id="62526-568"><span id="RDP"></span><span id="rdp"></span>**RDP** (4405)</span><span class="sxs-lookup"><span data-stu-id="62526-568"><span id="RDP"></span><span id="rdp"></span>**RDP** (4405)</span></span>
</dt> <dt>

<span data-ttu-id="62526-569"><span id="HTTPS"></span><span id="https"></span>**Https** (4406)</span><span class="sxs-lookup"><span data-stu-id="62526-569"><span id="HTTPS"></span><span id="https"></span>**HTTPS** (4406)</span></span>
</dt> <dt>

<span data-ttu-id="62526-570"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="62526-570"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="62526-571"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (32768..</span><span class="sxs-lookup"><span data-stu-id="62526-571"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (32768..</span></span> <span data-ttu-id="62526-572">)</span><span class="sxs-lookup"><span data-stu-id="62526-572">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="62526-573">**ProtocolType**</span><span class="sxs-lookup"><span data-stu-id="62526-573">**ProtocolType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62526-574">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="62526-574">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="62526-575">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="62526-575">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62526-576">Cette propriété est déconseillée à la place de la propriété **ProtocolIFType** .</span><span class="sxs-lookup"><span data-stu-id="62526-576">This property is deprecated in lieu of the **ProtocolIFType** property.</span></span> <span data-ttu-id="62526-577">Cette propriété est héritée de l' [**\_ ProtocolEndpoint CIM**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span><span class="sxs-lookup"><span data-stu-id="62526-577">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span></span>

</dd> <dt>

<span data-ttu-id="62526-578">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="62526-578">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62526-579">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="62526-579">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="62526-580">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="62526-580">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62526-581">Dernier État demandé ou souhaité pour le service de gestion.</span><span class="sxs-lookup"><span data-stu-id="62526-581">The last requested or desired state for the management service.</span></span> <span data-ttu-id="62526-582">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur 12 (non applicable).</span><span class="sxs-lookup"><span data-stu-id="62526-582">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>



| <span data-ttu-id="62526-583">Valeur</span><span class="sxs-lookup"><span data-stu-id="62526-583">Value</span></span>                                                                         | <span data-ttu-id="62526-584">Signification</span><span class="sxs-lookup"><span data-stu-id="62526-584">Meaning</span></span>                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="62526-585"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="62526-585"><dt>12</dt></span></span> </dl> | <span data-ttu-id="62526-586">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="62526-586">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="62526-587">**État**</span><span class="sxs-lookup"><span data-stu-id="62526-587">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62526-588">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="62526-588">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62526-589">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="62526-589">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62526-590">Décrit l’état de l’élément.</span><span class="sxs-lookup"><span data-stu-id="62526-590">Describes the status of the element.</span></span> <span data-ttu-id="62526-591">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="62526-591">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="62526-592">OK</span><span class="sxs-lookup"><span data-stu-id="62526-592">"OK"</span></span>

<span data-ttu-id="62526-593">Erreurs</span><span class="sxs-lookup"><span data-stu-id="62526-593">"Error"</span></span>

<span data-ttu-id="62526-594">Détérioré</span><span class="sxs-lookup"><span data-stu-id="62526-594">"Degraded"</span></span>

<span data-ttu-id="62526-595">Connue</span><span class="sxs-lookup"><span data-stu-id="62526-595">"Unknown"</span></span>

<span data-ttu-id="62526-596">« Échec prévu »</span><span class="sxs-lookup"><span data-stu-id="62526-596">"Pred Fail"</span></span>

<span data-ttu-id="62526-597">Démarr</span><span class="sxs-lookup"><span data-stu-id="62526-597">"Starting"</span></span>

<span data-ttu-id="62526-598">Arrêt</span><span class="sxs-lookup"><span data-stu-id="62526-598">"Stopping"</span></span>

<span data-ttu-id="62526-599">Services</span><span class="sxs-lookup"><span data-stu-id="62526-599">"Service"</span></span>

<span data-ttu-id="62526-600">Trop sollicité</span><span class="sxs-lookup"><span data-stu-id="62526-600">"Stressed"</span></span>

<span data-ttu-id="62526-601">« Non récupéré »</span><span class="sxs-lookup"><span data-stu-id="62526-601">"NonRecover"</span></span>

<span data-ttu-id="62526-602">« Aucun contact »</span><span class="sxs-lookup"><span data-stu-id="62526-602">"No Contact"</span></span>

<span data-ttu-id="62526-603">« Comm. perdue »</span><span class="sxs-lookup"><span data-stu-id="62526-603">"Lost Comm"</span></span>

</dd> <dt>

<span data-ttu-id="62526-604">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="62526-604">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62526-605">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="62526-605">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="62526-606">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="62526-606">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62526-607">Chaînes qui décrivent les différentes valeurs de tableau **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="62526-607">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="62526-608">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), et chaque élément de tableau est toujours défini sur « OK ».</span><span class="sxs-lookup"><span data-stu-id="62526-608">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="62526-609">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="62526-609">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62526-610">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="62526-610">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62526-611">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="62526-611">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62526-612">Nom de la classe de création du système d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="62526-612">The hosting system's creation class name.</span></span> <span data-ttu-id="62526-613">Cette propriété est héritée de [**CIM \_ ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span><span class="sxs-lookup"><span data-stu-id="62526-613">This property is inherited from [**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span></span>

</dd> <dt>

<span data-ttu-id="62526-614">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="62526-614">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62526-615">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="62526-615">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62526-616">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="62526-616">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62526-617">Qualificateurs : **clé**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="62526-617">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="62526-618">Nom du système d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="62526-618">The name of the hosting system.</span></span> <span data-ttu-id="62526-619">Cette propriété est héritée de [**CIM \_ ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span><span class="sxs-lookup"><span data-stu-id="62526-619">This property is inherited from [**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span></span>

</dd> <dt>

<span data-ttu-id="62526-620">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="62526-620">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62526-621">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="62526-621">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="62526-622">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="62526-622">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62526-623">Date et heure de la dernière modification de l’état activé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="62526-623">The date and time when the enabled state of the element last changed.</span></span> <span data-ttu-id="62526-624">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mais elle n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="62526-624">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="62526-625">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="62526-625">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62526-626">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="62526-626">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="62526-627">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="62526-627">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62526-628">Indique l’État cible de la transition de l’instance.</span><span class="sxs-lookup"><span data-stu-id="62526-628">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="62526-629">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="62526-629">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="62526-630">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="62526-630">Requirements</span></span>



| <span data-ttu-id="62526-631">Condition requise</span><span class="sxs-lookup"><span data-stu-id="62526-631">Requirement</span></span> | <span data-ttu-id="62526-632">Valeur</span><span class="sxs-lookup"><span data-stu-id="62526-632">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62526-633">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="62526-633">Minimum supported client</span></span><br/> | <span data-ttu-id="62526-634">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="62526-634">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="62526-635">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="62526-635">Minimum supported server</span></span><br/> | <span data-ttu-id="62526-636">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="62526-636">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="62526-637">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="62526-637">Namespace</span></span><br/>                | <span data-ttu-id="62526-638">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="62526-638">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="62526-639">MOF</span><span class="sxs-lookup"><span data-stu-id="62526-639">MOF</span></span><br/>                      | <dl> <span data-ttu-id="62526-640"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="62526-640"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="62526-641">DLL</span><span class="sxs-lookup"><span data-stu-id="62526-641">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62526-642"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="62526-642"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

