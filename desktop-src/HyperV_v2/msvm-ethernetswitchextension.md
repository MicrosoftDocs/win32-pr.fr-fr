---
description: Représente une instance d’un composant d’extension lié à un commutateur Ethernet virtuel.
ms.assetid: 5b3e26e3-4cb9-47c9-865e-2f3232bbfc8e
title: Classe Msvm_EthernetSwitchExtension
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchExtension
- Msvm_EthernetSwitchExtension.InstanceID
- Msvm_EthernetSwitchExtension.Caption
- Msvm_EthernetSwitchExtension.Description
- Msvm_EthernetSwitchExtension.ElementName
- Msvm_EthernetSwitchExtension.InstallDate
- Msvm_EthernetSwitchExtension.OperationalStatus
- Msvm_EthernetSwitchExtension.StatusDescriptions
- Msvm_EthernetSwitchExtension.Status
- Msvm_EthernetSwitchExtension.HealthState
- Msvm_EthernetSwitchExtension.CommunicationStatus
- Msvm_EthernetSwitchExtension.DetailedStatus
- Msvm_EthernetSwitchExtension.OperatingStatus
- Msvm_EthernetSwitchExtension.PrimaryStatus
- Msvm_EthernetSwitchExtension.EnabledState
- Msvm_EthernetSwitchExtension.OtherEnabledState
- Msvm_EthernetSwitchExtension.RequestedState
- Msvm_EthernetSwitchExtension.EnabledDefault
- Msvm_EthernetSwitchExtension.TimeOfLastStateChange
- Msvm_EthernetSwitchExtension.AvailableRequestedStates
- Msvm_EthernetSwitchExtension.TransitioningToState
- Msvm_EthernetSwitchExtension.SystemCreationClassName
- Msvm_EthernetSwitchExtension.SystemName
- Msvm_EthernetSwitchExtension.CreationClassName
- Msvm_EthernetSwitchExtension.Name
- Msvm_EthernetSwitchExtension.ExtensionType
- Msvm_EthernetSwitchExtension.Vendor
- Msvm_EthernetSwitchExtension.Version
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a6d760737ded1a12cf369ccb3a46595627d8e38e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531232"
---
# <a name="msvm_ethernetswitchextension-class"></a><span data-ttu-id="2ee9d-103">MSVM \_ EthernetSwitchExtension, classe</span><span class="sxs-lookup"><span data-stu-id="2ee9d-103">Msvm\_EthernetSwitchExtension class</span></span>

<span data-ttu-id="2ee9d-104">Représente une instance d’un composant d’extension lié à un commutateur Ethernet virtuel.</span><span class="sxs-lookup"><span data-stu-id="2ee9d-104">Represents an instance of an extension component bound to a virtual Ethernet switch.</span></span>

<span data-ttu-id="2ee9d-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="2ee9d-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ee9d-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2ee9d-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetSwitchExtension : CIM_EnabledLogicalElement
{
  string   InstanceID;
  string   Caption = "Virtual Switch Extension";
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
  uint16   EnabledState = 5;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_VirtualEthernetSwitch";
  string   SystemName;
  string   CreationClassName = "Msvm_EthernetSwitchExtension";
  string   Name;
  uint8    ExtensionType;
  string   Vendor;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="2ee9d-107">Membres</span><span class="sxs-lookup"><span data-stu-id="2ee9d-107">Members</span></span>

<span data-ttu-id="2ee9d-108">La classe **MSVM \_ EthernetSwitchExtension** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="2ee9d-108">The **Msvm\_EthernetSwitchExtension** class has these types of members:</span></span>

-   [<span data-ttu-id="2ee9d-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2ee9d-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="2ee9d-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2ee9d-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2ee9d-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2ee9d-111">Methods</span></span>

<span data-ttu-id="2ee9d-112">La classe **MSVM \_ EthernetSwitchExtension** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="2ee9d-112">The **Msvm\_EthernetSwitchExtension** class has these methods.</span></span>



| <span data-ttu-id="2ee9d-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="2ee9d-113">Method</span></span>                                                                        | <span data-ttu-id="2ee9d-114">Description</span><span class="sxs-lookup"><span data-stu-id="2ee9d-114">Description</span></span>                         |
|:------------------------------------------------------------------------------|:------------------------------------|
| [<span data-ttu-id="2ee9d-115">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="2ee9d-115">**RequestStateChange**</span></span>](msvm-ethernetswitchextension-requeststatechange.md) | <span data-ttu-id="2ee9d-116">Demande un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="2ee9d-116">Requests a state change.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="2ee9d-117">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2ee9d-117">Properties</span></span>

<span data-ttu-id="2ee9d-118">La classe **MSVM \_ EthernetSwitchExtension** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="2ee9d-118">The **Msvm\_EthernetSwitchExtension** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2ee9d-119">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="2ee9d-119">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee9d-120">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2ee9d-120">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2ee9d-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2ee9d-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2ee9d-122">Indique les valeurs possibles pour le paramètre *RequestedState* de la méthode [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) utilisée pour initier un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="2ee9d-122">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="2ee9d-123">Les valeurs répertoriées sont un sous-ensemble des valeurs contenues dans la propriété **RequestedStatesSupported** de l’instance associée de la **\_ EnabledLogicalElementCapabilities CIM**, où les valeurs sélectionnées sont une fonction de l’état actuel du [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2ee9d-123">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="2ee9d-124">Cette propriété peut être non **null** si une implémentation est en mesure de publier l’ensemble de valeurs possibles en tant que fonction de l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="2ee9d-124">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="2ee9d-125">Cette propriété a la **valeur null** si une implémentation ne peut pas déterminer le jeu de valeurs possibles en tant que fonction de l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="2ee9d-125">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="2ee9d-126">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2ee9d-126">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="2ee9d-127"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (2)</span><span class="sxs-lookup"><span data-stu-id="2ee9d-127"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2ee9d-128"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (3)</span><span class="sxs-lookup"><span data-stu-id="2ee9d-128"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2ee9d-129"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Arrêter** (4)</span><span class="sxs-lookup"><span data-stu-id="2ee9d-129"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="2ee9d-130"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Hors connexion** (6)</span><span class="sxs-lookup"><span data-stu-id="2ee9d-130"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="2ee9d-131"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="2ee9d-131"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="2ee9d-132"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Différer** (8)</span><span class="sxs-lookup"><span data-stu-id="2ee9d-132"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="2ee9d-133"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Suspension** (9)</span><span class="sxs-lookup"><span data-stu-id="2ee9d-133"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="2ee9d-134"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Redémarrer** (10)</span><span class="sxs-lookup"><span data-stu-id="2ee9d-134"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="2ee9d-135"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Réinitialiser** (11)</span><span class="sxs-lookup"><span data-stu-id="2ee9d-135"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="2ee9d-136"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF réservé** (..</span><span class="sxs-lookup"><span data-stu-id="2ee9d-136"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="2ee9d-137">)</span><span class="sxs-lookup"><span data-stu-id="2ee9d-137">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2ee9d-138">**Caption**</span><span class="sxs-lookup"><span data-stu-id="2ee9d-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee9d-139">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2ee9d-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2ee9d-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2ee9d-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2ee9d-141">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="2ee9d-141">A short description of the object.</span></span> <span data-ttu-id="2ee9d-142">Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « extension de commutateur virtuel ».</span><span class="sxs-lookup"><span data-stu-id="2ee9d-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Virtual Switch Extension".</span></span>

</dd> <dt>

<span data-ttu-id="2ee9d-143">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="2ee9d-143">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee9d-144">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2ee9d-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2ee9d-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2ee9d-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2ee9d-146">Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="2ee9d-146">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="2ee9d-147">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="2ee9d-147">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="2ee9d-148">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2ee9d-148">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2ee9d-149">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2ee9d-149">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee9d-150">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2ee9d-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2ee9d-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2ee9d-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2ee9d-152">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="2ee9d-152">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="2ee9d-153">Nom de la classe ou de la sous-classe utilisée lors de la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="2ee9d-153">The name of the class or subclass that is used in the creation of an instance.</span></span> <span data-ttu-id="2ee9d-154">Cette propriété a toujours la valeur « MSVM \_ EthernetSwitchExtension ».</span><span class="sxs-lookup"><span data-stu-id="2ee9d-154">This property is always set to "Msvm\_EthernetSwitchExtension".</span></span>

</dd> <dt>

<span data-ttu-id="2ee9d-155">**Description**</span><span class="sxs-lookup"><span data-stu-id="2ee9d-155">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee9d-156">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2ee9d-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2ee9d-157">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2ee9d-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2ee9d-158">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="2ee9d-158">A description of the object.</span></span> <span data-ttu-id="2ee9d-159">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="2ee9d-159">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2ee9d-160">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="2ee9d-160">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee9d-161">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2ee9d-161">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2ee9d-162">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2ee9d-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2ee9d-163">Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="2ee9d-163">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="2ee9d-164">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="2ee9d-164">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="2ee9d-165">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2ee9d-165">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2ee9d-166">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="2ee9d-166">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee9d-167">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2ee9d-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2ee9d-168">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2ee9d-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2ee9d-169">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="2ee9d-169">A display name for the object.</span></span> <span data-ttu-id="2ee9d-170">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="2ee9d-170">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2ee9d-171">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="2ee9d-171">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee9d-172">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2ee9d-172">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2ee9d-173">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2ee9d-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2ee9d-174">Configuration par défaut ou de démarrage d’un administrateur pour l’état activé d’un élément.</span><span class="sxs-lookup"><span data-stu-id="2ee9d-174">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="2ee9d-175">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) et sera l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="2ee9d-175">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and will be one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="2ee9d-176"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (2)</span><span class="sxs-lookup"><span data-stu-id="2ee9d-176"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2ee9d-177"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (3)</span><span class="sxs-lookup"><span data-stu-id="2ee9d-177"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2ee9d-178"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Activé mais hors connexion** (6)</span><span class="sxs-lookup"><span data-stu-id="2ee9d-178"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Enabled but Offline** (6)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2ee9d-179">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="2ee9d-179">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee9d-180">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2ee9d-180">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2ee9d-181">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2ee9d-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2ee9d-182">États activés et désactivés d’un élément.</span><span class="sxs-lookup"><span data-stu-id="2ee9d-182">The enabled and disabled states of an element.</span></span> <span data-ttu-id="2ee9d-183">Cette propriété peut également indiquer les transitions entre ces États demandés.</span><span class="sxs-lookup"><span data-stu-id="2ee9d-183">This property can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="2ee9d-184">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2ee9d-184">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="2ee9d-185">Valeur</span><span class="sxs-lookup"><span data-stu-id="2ee9d-185">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="2ee9d-186">Signification</span><span class="sxs-lookup"><span data-stu-id="2ee9d-186">Meaning</span></span>                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="2ee9d-187"><dt>**Inconnu**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2ee9d-187"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 |                                                                                                                                                                                                             |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="2ee9d-188"><dt>**Autre**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="2ee9d-188"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                             |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="2ee9d-189"><dt>**Activé**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="2ee9d-189"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="2ee9d-190">L’élément est ou peut exécuter des commandes, traite toutes les commandes mises en file d’attente et met en file d’attente les nouvelles requêtes.</span><span class="sxs-lookup"><span data-stu-id="2ee9d-190">The element is or could be executing commands, will process any queued commands, and queues new requests.</span></span><br/>                                                                                        |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="2ee9d-191"><dt>**Désactivé**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="2ee9d-191"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="2ee9d-192">L’élément n’exécutera pas de commande et supprimera toutes les nouvelles demandes.</span><span class="sxs-lookup"><span data-stu-id="2ee9d-192">The element will not execute commands and will drop any new requests.</span></span><br/>                                                                                                                            |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="2ee9d-193"><dt>**Arrêt**</dt> de <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="2ee9d-193"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="2ee9d-194">L’élément est en cours de passage à un état désactivé.</span><span class="sxs-lookup"><span data-stu-id="2ee9d-194">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                      |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="2ee9d-195"><dt>**Non applicable**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="2ee9d-195"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="2ee9d-196">L’élément ne prend pas en charge l’activation ou la désactivation.</span><span class="sxs-lookup"><span data-stu-id="2ee9d-196">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                          |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="2ee9d-197"><dt>**Activé mais hors connexion**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="2ee9d-197"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="2ee9d-198">L’élément peut exécuter des commandes et supprimer toutes les nouvelles demandes.</span><span class="sxs-lookup"><span data-stu-id="2ee9d-198">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                     |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="2ee9d-199"><dt>**Dans le test**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="2ee9d-199"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="2ee9d-200">L’élément est dans un état de test.</span><span class="sxs-lookup"><span data-stu-id="2ee9d-200">The element is in a test state.</span></span><br/>                                                                                                                                                                  |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="2ee9d-201"><dt>**Différé**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="2ee9d-201"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="2ee9d-202">L’élément peut exécuter des commandes, mais il met en file d’attente toutes les nouvelles demandes.</span><span class="sxs-lookup"><span data-stu-id="2ee9d-202">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                    |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="2ee9d-203"><dt>**Suspension**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="2ee9d-203"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="2ee9d-204">L’élément est activé, mais en mode restreint.</span><span class="sxs-lookup"><span data-stu-id="2ee9d-204">The element is enabled but in a restricted mode.</span></span> <span data-ttu-id="2ee9d-205">Le comportement de l’élément est similaire à l’état activé, mais ne traite qu’un ensemble restreint de commandes.</span><span class="sxs-lookup"><span data-stu-id="2ee9d-205">The behavior of the element is similar to the Enabled state, but it processes only a restricted set of commands.</span></span> <span data-ttu-id="2ee9d-206">Toutes les autres demandes sont mises en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="2ee9d-206">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="2ee9d-207">À <dt>**partir**</dt> de <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="2ee9d-207"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="2ee9d-208">L’élément est en train d’accéder à un état activé.</span><span class="sxs-lookup"><span data-stu-id="2ee9d-208">The element is in the process of going to an Enabled state.</span></span> <span data-ttu-id="2ee9d-209">Les nouvelles demandes sont mises en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="2ee9d-209">New requests are queued.</span></span><br/>                                                                                                             |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="2ee9d-210"><dt>**DMTF réservé**</dt> <dt>11 32767</dt></span><span class="sxs-lookup"><span data-stu-id="2ee9d-210"><dt>**DMTF Reserved**</dt> <dt>11 32767</dt></span></span> </dl>                  | <span data-ttu-id="2ee9d-211">Réservé.</span><span class="sxs-lookup"><span data-stu-id="2ee9d-211">Reserved.</span></span><br/>                                                                                                                                                                                        |
| <span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span><dl> <span data-ttu-id="2ee9d-212"><dt>**Fournisseur réservé**</dt> <dt>32768 65535</dt></span><span class="sxs-lookup"><span data-stu-id="2ee9d-212"><dt>**Vendor Reserved**</dt> <dt>32768 65535</dt></span></span> </dl>       | <span data-ttu-id="2ee9d-213">Réservé.</span><span class="sxs-lookup"><span data-stu-id="2ee9d-213">Reserved.</span></span><br/>                                                                                                                                                                                        |



 

</dd> <dt>

<span data-ttu-id="2ee9d-214">**ExtensionType**</span><span class="sxs-lookup"><span data-stu-id="2ee9d-214">**ExtensionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee9d-215">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="2ee9d-215">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="2ee9d-216">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2ee9d-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2ee9d-217">Indique le type du composant d’extension.</span><span class="sxs-lookup"><span data-stu-id="2ee9d-217">Indicates the type of the extension component.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2ee9d-218">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="2ee9d-218">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Capture"></span><span id="capture"></span><span id="CAPTURE"></span>

<span data-ttu-id="2ee9d-219">**Capture** (1)</span><span class="sxs-lookup"><span data-stu-id="2ee9d-219">**Capture** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Filter"></span><span id="filter"></span><span id="FILTER"></span>

<span data-ttu-id="2ee9d-220">**Filtre** (2)</span><span class="sxs-lookup"><span data-stu-id="2ee9d-220">**Filter** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Forwarding"></span><span id="forwarding"></span><span id="FORWARDING"></span>

<span data-ttu-id="2ee9d-221">**Transfert** (3)</span><span class="sxs-lookup"><span data-stu-id="2ee9d-221">**Forwarding** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Monitoring"></span><span id="monitoring"></span><span id="MONITORING"></span>

<span data-ttu-id="2ee9d-222">**Analyse** (4)</span><span class="sxs-lookup"><span data-stu-id="2ee9d-222">**Monitoring** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Native"></span><span id="native"></span><span id="NATIVE"></span>

<span data-ttu-id="2ee9d-223">**Natif** (5)</span><span class="sxs-lookup"><span data-stu-id="2ee9d-223">**Native** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2ee9d-224">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="2ee9d-224">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee9d-225">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2ee9d-225">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2ee9d-226">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2ee9d-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2ee9d-227">Spécifie l’intégrité actuelle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="2ee9d-227">Specifies the current health of the element.</span></span> <span data-ttu-id="2ee9d-228">Cet attribut exprime l’intégrité de cet élément, mais pas nécessairement celle de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="2ee9d-228">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span>

<span data-ttu-id="2ee9d-229">Lorsqu’une erreur critique se produit, consultez le journal des événements pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="2ee9d-229">When a critical error occurs, check the event log for details.</span></span> <span data-ttu-id="2ee9d-230">La propriété **EnabledState** peut également contenir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="2ee9d-230">The **EnabledState** property can also contain more information.</span></span> <span data-ttu-id="2ee9d-231">Par exemple, lorsque l’espace disque est très faible, **HealthState** est défini sur 25, l’ordinateur virtuel s’interrompt et **EnabledState** a la valeur 32768 (suspendu).</span><span class="sxs-lookup"><span data-stu-id="2ee9d-231">For example, when disk space is critically low, **HealthState** is set to 25, the virtual machine pauses, and **EnabledState** is set to 32768 (Paused).</span></span>

<span data-ttu-id="2ee9d-232">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2ee9d-232">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="2ee9d-233">Valeur</span><span class="sxs-lookup"><span data-stu-id="2ee9d-233">Value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="2ee9d-234">Signification</span><span class="sxs-lookup"><span data-stu-id="2ee9d-234">Meaning</span></span>                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="2ee9d-235"><dt>**OK**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="2ee9d-235"><dt>**OK**</dt> <dt>5</dt></span></span> </dl>                                                                               | <span data-ttu-id="2ee9d-236">L’élément est entièrement fonctionnel et fonctionne dans des paramètres opérationnels normaux et sans erreur.</span><span class="sxs-lookup"><span data-stu-id="2ee9d-236">The element is fully functional and is operating within normal operational parameters and without error.</span></span><br/> |
| <span id="Major_Failure"></span><span id="major_failure"></span><span id="MAJOR_FAILURE"></span><dl> <span data-ttu-id="2ee9d-237"><dt>**Erreur majeure**</dt> <dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="2ee9d-237"><dt>**Major Failure**</dt> <dt>20</dt></span></span> </dl>             | <span data-ttu-id="2ee9d-238">L’élément a subi un échec majeur.</span><span class="sxs-lookup"><span data-stu-id="2ee9d-238">The element has suffered a major failure.</span></span><br/>                                                                |
| <span id="Critical_failure"></span><span id="critical_failure"></span><span id="CRITICAL_FAILURE"></span><dl> <span data-ttu-id="2ee9d-239"><dt>**Erreur critique**</dt> <dt>25</dt></span><span class="sxs-lookup"><span data-stu-id="2ee9d-239"><dt>**Critical failure**</dt> <dt>25</dt></span></span> </dl> | <span data-ttu-id="2ee9d-240">L’élément n’est pas fonctionnel et la récupération n’est peut-être pas possible.</span><span class="sxs-lookup"><span data-stu-id="2ee9d-240">The element is nonfunctional, and recovery might not be possible.</span></span><br/>                                        |



 

</dd> <dt>

<span data-ttu-id="2ee9d-241">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="2ee9d-241">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee9d-242">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2ee9d-242">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2ee9d-243">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2ee9d-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2ee9d-244">Date et heure de création de la configuration d’ordinateur virtuel pour un ordinateur virtuel, ou **valeur null**, pour un système d’exploitation de gestion.</span><span class="sxs-lookup"><span data-stu-id="2ee9d-244">The date and time the virtual machine configuration was created for a virtual machine, or **Null**, for a management operating system.</span></span> <span data-ttu-id="2ee9d-245">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2ee9d-245">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2ee9d-246">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2ee9d-246">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee9d-247">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2ee9d-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2ee9d-248">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2ee9d-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2ee9d-249">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="2ee9d-249">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="2ee9d-250">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="2ee9d-250">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="2ee9d-251">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="2ee9d-251">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2ee9d-252">**Nom**</span><span class="sxs-lookup"><span data-stu-id="2ee9d-252">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee9d-253">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2ee9d-253">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2ee9d-254">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2ee9d-254">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2ee9d-255">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) ("nom"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="2ee9d-255">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="2ee9d-256">Nom unique du composant d’extension.</span><span class="sxs-lookup"><span data-stu-id="2ee9d-256">The unique name of the extension component.</span></span>

</dd> <dt>

<span data-ttu-id="2ee9d-257">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="2ee9d-257">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee9d-258">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2ee9d-258">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2ee9d-259">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2ee9d-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2ee9d-260">Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="2ee9d-260">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="2ee9d-261">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="2ee9d-261">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="2ee9d-262">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2ee9d-262">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2ee9d-263">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="2ee9d-263">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee9d-264">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2ee9d-264">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2ee9d-265">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2ee9d-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2ee9d-266">Tableau qui contient les États actuels de l’objet.</span><span class="sxs-lookup"><span data-stu-id="2ee9d-266">An array that contains the current statuses of the object.</span></span> <span data-ttu-id="2ee9d-267">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2ee9d-267">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2ee9d-268">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="2ee9d-268">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee9d-269">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2ee9d-269">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2ee9d-270">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2ee9d-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2ee9d-271">État activé ou désactivé de l’élément lorsque la propriété **EnabledState** a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="2ee9d-271">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="2ee9d-272">Cette propriété doit avoir la valeur **null** quand **EnabledState** a une valeur autre que 1.</span><span class="sxs-lookup"><span data-stu-id="2ee9d-272">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="2ee9d-273">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="2ee9d-273">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="2ee9d-274">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="2ee9d-274">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee9d-275">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2ee9d-275">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2ee9d-276">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2ee9d-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2ee9d-277">Fournit des informations d’état de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="2ee9d-277">Provides high level status information.</span></span> <span data-ttu-id="2ee9d-278">Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir des informations d’état d’intégrité de haut niveau et détaillées pour l’élément et ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="2ee9d-278">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="2ee9d-279">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="2ee9d-279">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="2ee9d-280">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2ee9d-280">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2ee9d-281">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="2ee9d-281">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee9d-282">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2ee9d-282">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2ee9d-283">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2ee9d-283">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2ee9d-284">Dernier État demandé ou souhaité pour l’élément passé à la méthode **RequestStateChange** , ou 12 (non applicable) si aucun changement d’État n’est en cours.</span><span class="sxs-lookup"><span data-stu-id="2ee9d-284">The last requested or desired state for the element as passed to the **RequestStateChange** method, or 12 (Not Applicable) if no state change is in progress.</span></span> <span data-ttu-id="2ee9d-285">L’état réel de l’élément est représenté par **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="2ee9d-285">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="2ee9d-286">Cette propriété est fournie pour comparer les derniers États activés et actuellement activés ou désactivés.</span><span class="sxs-lookup"><span data-stu-id="2ee9d-286">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="2ee9d-287">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2ee9d-287">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="2ee9d-288">**État**</span><span class="sxs-lookup"><span data-stu-id="2ee9d-288">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee9d-289">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2ee9d-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2ee9d-290">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2ee9d-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2ee9d-291">Chaîne qui spécifie l’état de l’élément.</span><span class="sxs-lookup"><span data-stu-id="2ee9d-291">A string that specifies the status of the element.</span></span> <span data-ttu-id="2ee9d-292">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2ee9d-292">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2ee9d-293">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="2ee9d-293">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee9d-294">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="2ee9d-294">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2ee9d-295">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2ee9d-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2ee9d-296">Qualificateurs : **arrayType** ("indexé")</span><span class="sxs-lookup"><span data-stu-id="2ee9d-296">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="2ee9d-297">Tableau qui contient des chaînes qui décrivent les valeurs de tableau **OperationalStatus** correspondantes.</span><span class="sxs-lookup"><span data-stu-id="2ee9d-297">An array that contains strings that describe the corresponding **OperationalStatus** array values.</span></span> <span data-ttu-id="2ee9d-298">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2ee9d-298">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2ee9d-299">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2ee9d-299">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee9d-300">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2ee9d-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2ee9d-301">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2ee9d-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2ee9d-302">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**propagée**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ système CIM**](cim-system.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="2ee9d-302">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="2ee9d-303">Nom de la classe de création du système.</span><span class="sxs-lookup"><span data-stu-id="2ee9d-303">The system creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="2ee9d-304">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="2ee9d-304">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee9d-305">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2ee9d-305">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2ee9d-306">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2ee9d-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2ee9d-307">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**propagée**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ système CIM**](cim-system.md).**Name**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="2ee9d-307">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="2ee9d-308">Nom du commutateur virtuel auquel l’instance d’extension est liée.</span><span class="sxs-lookup"><span data-stu-id="2ee9d-308">The name of the virtual switch to which the extension instance is bound to.</span></span>

</dd> <dt>

<span data-ttu-id="2ee9d-309">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="2ee9d-309">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee9d-310">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2ee9d-310">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2ee9d-311">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2ee9d-311">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2ee9d-312">Date et heure de la dernière modification de l’état activé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="2ee9d-312">The date and time when the enabled state of the element last changed.</span></span> <span data-ttu-id="2ee9d-313">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2ee9d-313">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="2ee9d-314">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="2ee9d-314">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee9d-315">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2ee9d-315">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2ee9d-316">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2ee9d-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2ee9d-317">Indique l’État cible de la transition de l’instance.</span><span class="sxs-lookup"><span data-stu-id="2ee9d-317">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="2ee9d-318">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="2ee9d-318">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2ee9d-319">**Fournisseur**</span><span class="sxs-lookup"><span data-stu-id="2ee9d-319">**Vendor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee9d-320">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2ee9d-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2ee9d-321">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2ee9d-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2ee9d-322">Indique le fournisseur qui fournit l’extension.</span><span class="sxs-lookup"><span data-stu-id="2ee9d-322">Indicates the vendor providing the extension.</span></span>

</dd> <dt>

<span data-ttu-id="2ee9d-323">**Version**</span><span class="sxs-lookup"><span data-stu-id="2ee9d-323">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee9d-324">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2ee9d-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2ee9d-325">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2ee9d-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2ee9d-326">Version de l’extension dans un format «*major*. *Minor*», par exemple « 2,0 ».</span><span class="sxs-lookup"><span data-stu-id="2ee9d-326">The version of the extension in a format of "*major*.*minor*", for example "2.0".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2ee9d-327">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2ee9d-327">Requirements</span></span>



| <span data-ttu-id="2ee9d-328">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2ee9d-328">Requirement</span></span> | <span data-ttu-id="2ee9d-329">Valeur</span><span class="sxs-lookup"><span data-stu-id="2ee9d-329">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ee9d-330">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2ee9d-330">Minimum supported client</span></span><br/> | <span data-ttu-id="2ee9d-331">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2ee9d-331">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2ee9d-332">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2ee9d-332">Minimum supported server</span></span><br/> | <span data-ttu-id="2ee9d-333">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2ee9d-333">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2ee9d-334">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2ee9d-334">Namespace</span></span><br/>                | <span data-ttu-id="2ee9d-335">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="2ee9d-335">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2ee9d-336">MOF</span><span class="sxs-lookup"><span data-stu-id="2ee9d-336">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2ee9d-337"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2ee9d-337"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2ee9d-338">DLL</span><span class="sxs-lookup"><span data-stu-id="2ee9d-338">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2ee9d-339"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2ee9d-339"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

