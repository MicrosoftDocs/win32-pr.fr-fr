---
description: Représente le point de connexion logique pour une carte réseau. Lorsque le point de terminaison de Wi-Fi est connecté à un port de commutateur, la carte réseau connectée au point de terminaison Wi-Fi dispose d’une connectivité réseau.
ms.assetid: 66ed1503-9c11-4a51-a3a5-21e5d7021197
title: Classe Msvm_WiFiEndpoint
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_WiFiEndpoint
- Msvm_WiFiEndpoint.RequestStateChange
- Msvm_WiFiEndpoint.InstanceID
- Msvm_WiFiEndpoint.Caption
- Msvm_WiFiEndpoint.Description
- Msvm_WiFiEndpoint.ElementName
- Msvm_WiFiEndpoint.InstallDate
- Msvm_WiFiEndpoint.Name
- Msvm_WiFiEndpoint.OperationalStatus
- Msvm_WiFiEndpoint.StatusDescriptions
- Msvm_WiFiEndpoint.Status
- Msvm_WiFiEndpoint.HealthState
- Msvm_WiFiEndpoint.CommunicationStatus
- Msvm_WiFiEndpoint.DetailedStatus
- Msvm_WiFiEndpoint.OperatingStatus
- Msvm_WiFiEndpoint.PrimaryStatus
- Msvm_WiFiEndpoint.EnabledState
- Msvm_WiFiEndpoint.OtherEnabledState
- Msvm_WiFiEndpoint.RequestedState
- Msvm_WiFiEndpoint.EnabledDefault
- Msvm_WiFiEndpoint.TimeOfLastStateChange
- Msvm_WiFiEndpoint.AvailableRequestedStates
- Msvm_WiFiEndpoint.TransitioningToState
- Msvm_WiFiEndpoint.SystemCreationClassName
- Msvm_WiFiEndpoint.SystemName
- Msvm_WiFiEndpoint.CreationClassName
- Msvm_WiFiEndpoint.NameFormat
- Msvm_WiFiEndpoint.ProtocolType
- Msvm_WiFiEndpoint.ProtocolIFType
- Msvm_WiFiEndpoint.OtherTypeDescription
- Msvm_WiFiEndpoint.LANID
- Msvm_WiFiEndpoint.LANType
- Msvm_WiFiEndpoint.OtherLANType
- Msvm_WiFiEndpoint.MACAddress
- Msvm_WiFiEndpoint.AliasAddresses
- Msvm_WiFiEndpoint.GroupAddresses
- Msvm_WiFiEndpoint.MaxDataSize
- Msvm_WiFiEndpoint.Connected
- Msvm_WiFiEndpoint.EncryptionMethod
- Msvm_WiFiEndpoint.OtherEncryptionMethod
- Msvm_WiFiEndpoint.AuthenticationMethod
- Msvm_WiFiEndpoint.OtherAuthenticationMethod
- Msvm_WiFiEndpoint.IEEE8021xAuthenticationProtocol
- Msvm_WiFiEndpoint.AccessPointAddress
- Msvm_WiFiEndpoint.BSSType
- Msvm_WiFiEndpoint.Associated
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f4a0a287d85b7a229b0e8e50a10c402fca734429
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951137"
---
# <a name="msvm_wifiendpoint-class"></a><span data-ttu-id="d2fa5-104">MSVM \_ WiFiEndpoint, classe</span><span class="sxs-lookup"><span data-stu-id="d2fa5-104">Msvm\_WiFiEndpoint class</span></span>

<span data-ttu-id="d2fa5-105">Représente le point de connexion logique pour une carte réseau.</span><span class="sxs-lookup"><span data-stu-id="d2fa5-105">Represents the logical connection point for a network adapter.</span></span> <span data-ttu-id="d2fa5-106">Lorsque le point de terminaison de Wi-Fi est connecté à un port de commutateur, la carte réseau connectée au point de terminaison Wi-Fi dispose d’une connectivité réseau.</span><span class="sxs-lookup"><span data-stu-id="d2fa5-106">When the Wi-Fi endpoint is connected to a switch port, the network adapter connected to the Wi-Fi endpoint has network connectivity.</span></span>

<span data-ttu-id="d2fa5-107">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="d2fa5-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2fa5-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d2fa5-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_WiFiEndpoint : CIM_WiFiEndpoint
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  string   CreationClassName;
  string   NameFormat;
  uint16   ProtocolType;
  uint16   ProtocolIFType = 71;
  string   OtherTypeDescription;
  string   LANID;
  uint16   LANType;
  string   OtherLANType;
  string   MACAddress;
  string   AliasAddresses[];
  string   GroupAddresses[];
  uint32   MaxDataSize;
  boolean  Connected;
  uint16   EncryptionMethod;
  string   OtherEncryptionMethod;
  uint16   AuthenticationMethod;
  string   OtherAuthenticationMethod;
  uint16   IEEE8021xAuthenticationProtocol;
  string   AccessPointAddress;
  uint16   BSSType;
  boolean  Associated;
};
```

## <a name="members"></a><span data-ttu-id="d2fa5-109">Membres</span><span class="sxs-lookup"><span data-stu-id="d2fa5-109">Members</span></span>

<span data-ttu-id="d2fa5-110">La classe **MSVM \_ WiFiEndpoint** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d2fa5-110">The **Msvm\_WiFiEndpoint** class has these types of members:</span></span>

-   [<span data-ttu-id="d2fa5-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d2fa5-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="d2fa5-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d2fa5-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d2fa5-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d2fa5-113">Methods</span></span>

<span data-ttu-id="d2fa5-114">La classe **MSVM \_ WiFiEndpoint** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="d2fa5-114">The **Msvm\_WiFiEndpoint** class has these methods.</span></span>



| <span data-ttu-id="d2fa5-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="d2fa5-115">Method</span></span>                 | <span data-ttu-id="d2fa5-116">Description</span><span class="sxs-lookup"><span data-stu-id="d2fa5-116">Description</span></span>                              |
|:-----------------------|:-----------------------------------------|
| <span data-ttu-id="d2fa5-117">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-117">**RequestStateChange**</span></span> | <span data-ttu-id="d2fa5-118">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="d2fa5-118">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d2fa5-119">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d2fa5-119">Properties</span></span>

<span data-ttu-id="d2fa5-120">La classe **MSVM \_ WiFiEndpoint** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="d2fa5-120">The **Msvm\_WiFiEndpoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d2fa5-121">**AccessPointAddress**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-121">**AccessPointAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2fa5-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2fa5-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2fa5-124">Contient l’adresse MAC du point d’accès auquel le point de terminaison de Wi-Fi est actuellement associé.</span><span class="sxs-lookup"><span data-stu-id="d2fa5-124">Contains the MAC address of the access point with which the Wi-Fi endpoint is currently associated.</span></span> <span data-ttu-id="d2fa5-125">Si le point de terminaison Wi-Fi n’est pas associé actuellement, **AccessPointAddress** doit avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="d2fa5-125">If the Wi-Fi endpoint is not currently associated, then **AccessPointAddress** should be **Null**.</span></span> <span data-ttu-id="d2fa5-126">L’adresse MAC doit être au format 12 chiffres hexadécimaux (par exemple, « 010203040506 »), chaque paire représentant l’un des six octets de l’adresse MAC dans l’ordre des bits canoniques (par exemple, le bit d’adresse de groupe se trouve dans le bit de poids faible du premier caractère de la chaîne).</span><span class="sxs-lookup"><span data-stu-id="d2fa5-126">The MAC address should be formatted as twelve hexadecimal digits (for example, "010203040506"), with each pair representing one of the six octets of the MAC address in canonical bit order (for example, the Group address bit is found in the low order bit of the first character of the string).</span></span>

</dd> <dt>

<span data-ttu-id="d2fa5-127">**AliasAddresses**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-127">**AliasAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2fa5-128">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-128">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2fa5-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2fa5-130">Autres adresses de monodiffusion qui peuvent être utilisées pour communiquer avec le point de terminaison LAN.</span><span class="sxs-lookup"><span data-stu-id="d2fa5-130">Other unicast addresses that may be used to communicate with the LAN endpoint.</span></span> <span data-ttu-id="d2fa5-131">Cette propriété est héritée de la [**\_ LANEndpoint CIM**](/previous-versions//cc136865(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d2fa5-131">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d2fa5-132">**Associé**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-132">**Associated**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2fa5-133">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-133">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2fa5-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2fa5-135">Indique si le point de terminaison Wi-Fi est actuellement associé à un point d’accès ou à une station cliente.</span><span class="sxs-lookup"><span data-stu-id="d2fa5-135">Indicates whether the Wi-Fi endpoint is currently associated to an access point or client station.</span></span>

<span data-ttu-id="d2fa5-136">Contient la **valeur true** si le point de terminaison Wi-Fi est associé à un point d’accès ou à une station cliente. Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="d2fa5-136">Contains **True** if the Wi-Fi endpoint is associated to an access point or client station; otherwise, **False**.</span></span>

</dd> <dt>

<span data-ttu-id="d2fa5-137">**AuthenticationMethod**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-137">**AuthenticationMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2fa5-138">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-138">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2fa5-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2fa5-140">Spécifie la méthode utilisée pour authentifier le point de terminaison de Wi-Fi et le réseau entre eux.</span><span class="sxs-lookup"><span data-stu-id="d2fa5-140">Specifies the method used to authenticate the Wi-Fi endpoint and the network to one another.</span></span>

<dl> <dt>

<span data-ttu-id="d2fa5-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="d2fa5-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-142"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="d2fa5-142"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-143"><span id="Open_System"></span><span id="open_system"></span><span id="OPEN_SYSTEM"></span>**Système ouvert** (2)</span><span class="sxs-lookup"><span data-stu-id="d2fa5-143"><span id="Open_System"></span><span id="open_system"></span><span id="OPEN_SYSTEM"></span>**Open System** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-144"><span id="Shared_Key"></span><span id="shared_key"></span><span id="SHARED_KEY"></span>**Clé partagée** (3)</span><span class="sxs-lookup"><span data-stu-id="d2fa5-144"><span id="Shared_Key"></span><span id="shared_key"></span><span id="SHARED_KEY"></span>**Shared Key** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-145"><span id="WPA_PSK"></span><span id="wpa_psk"></span>**WPA PSK** (4)</span><span class="sxs-lookup"><span data-stu-id="d2fa5-145"><span id="WPA_PSK"></span><span id="wpa_psk"></span>**WPA PSK** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-146"><span id="WPA_IEEE_802.1x"></span><span id="wpa_ieee_802.1x"></span><span id="WPA_IEEE_802.1X"></span>**WPA IEEE 802.1 x** (5)</span><span class="sxs-lookup"><span data-stu-id="d2fa5-146"><span id="WPA_IEEE_802.1x"></span><span id="wpa_ieee_802.1x"></span><span id="WPA_IEEE_802.1X"></span>**WPA IEEE 802.1x** (5)</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-147"><span id="WPA2_PSK"></span><span id="wpa2_psk"></span>**WPA2 PSK** (6)</span><span class="sxs-lookup"><span data-stu-id="d2fa5-147"><span id="WPA2_PSK"></span><span id="wpa2_psk"></span>**WPA2 PSK** (6)</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-148"><span id="WPA2_IEEE_802.1x"></span><span id="wpa2_ieee_802.1x"></span><span id="WPA2_IEEE_802.1X"></span>**WPA2 IEEE 802.1 x** (7)</span><span class="sxs-lookup"><span data-stu-id="d2fa5-148"><span id="WPA2_IEEE_802.1x"></span><span id="wpa2_ieee_802.1x"></span><span id="WPA2_IEEE_802.1X"></span>**WPA2 IEEE 802.1x** (7)</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-149"><span id="CCKM_IEEE_802.1x"></span><span id="cckm_ieee_802.1x"></span><span id="CCKM_IEEE_802.1X"></span>**CCKM IEEE 802.1 x** (8)</span><span class="sxs-lookup"><span data-stu-id="d2fa5-149"><span id="CCKM_IEEE_802.1x"></span><span id="cckm_ieee_802.1x"></span><span id="CCKM_IEEE_802.1X"></span>**CCKM IEEE 802.1x** (8)</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-150"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF réservé** (9..</span><span class="sxs-lookup"><span data-stu-id="d2fa5-150"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (9..</span></span> <span data-ttu-id="d2fa5-151">)</span><span class="sxs-lookup"><span data-stu-id="d2fa5-151">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d2fa5-152">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-152">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2fa5-153">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-153">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2fa5-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2fa5-155">Indique les valeurs possibles pour le paramètre *RequestedState* de la méthode [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) utilisée pour initier un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="d2fa5-155">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="d2fa5-156">Les valeurs répertoriées sont un sous-ensemble des valeurs contenues dans la propriété **RequestedStatesSupported** de l’instance associée de la **\_ EnabledLogicalElementCapabilities CIM**, où les valeurs sélectionnées sont une fonction de l’état actuel du [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d2fa5-156">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="d2fa5-157">Cette propriété peut être non **null** si une implémentation est en mesure de publier l’ensemble de valeurs possibles en tant que fonction de l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="d2fa5-157">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="d2fa5-158">Cette propriété a la **valeur null** si une implémentation ne peut pas déterminer le jeu de valeurs possibles en tant que fonction de l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="d2fa5-158">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="d2fa5-159">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d2fa5-159">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="d2fa5-160"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (2)</span><span class="sxs-lookup"><span data-stu-id="d2fa5-160"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-161"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (3)</span><span class="sxs-lookup"><span data-stu-id="d2fa5-161"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-162"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Arrêter** (4)</span><span class="sxs-lookup"><span data-stu-id="d2fa5-162"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-163"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Hors connexion** (6)</span><span class="sxs-lookup"><span data-stu-id="d2fa5-163"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-164"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="d2fa5-164"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-165"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Différer** (8)</span><span class="sxs-lookup"><span data-stu-id="d2fa5-165"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-166"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Suspension** (9)</span><span class="sxs-lookup"><span data-stu-id="d2fa5-166"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-167"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Redémarrer** (10)</span><span class="sxs-lookup"><span data-stu-id="d2fa5-167"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-168"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Réinitialiser** (11)</span><span class="sxs-lookup"><span data-stu-id="d2fa5-168"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-169"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF réservé** (..</span><span class="sxs-lookup"><span data-stu-id="d2fa5-169"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="d2fa5-170">)</span><span class="sxs-lookup"><span data-stu-id="d2fa5-170">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d2fa5-171">**BSSType**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-171">**BSSType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2fa5-172">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-172">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-173">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2fa5-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2fa5-174">Indique le type BSS (Basic Service Set) du réseau qui correspond à l’instance.</span><span class="sxs-lookup"><span data-stu-id="d2fa5-174">Indicates the Basic Service Set (BSS) type of the network that corresponds to the instance.</span></span> <span data-ttu-id="d2fa5-175">Un ensemble de services de base est un ensemble de stations contrôlées par une seule fonction de coordination.</span><span class="sxs-lookup"><span data-stu-id="d2fa5-175">A Basic Service Set is a set of stations controlled by a single coordination function.</span></span>



| <span data-ttu-id="d2fa5-176">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2fa5-176">Value</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="d2fa5-177">Signification</span><span class="sxs-lookup"><span data-stu-id="d2fa5-177">Meaning</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="d2fa5-178"><dt>**Inconnu**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d2fa5-178"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                |                                                                                    |
| <span id="Independent"></span><span id="independent"></span><span id="INDEPENDENT"></span><dl> <span data-ttu-id="d2fa5-179"><dt>**Indépendant**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="d2fa5-179"><dt>**Independent**</dt> <dt>2</dt></span></span> </dl>                | <span data-ttu-id="d2fa5-180">Le point de terminaison Wi-Fi est directement associé à une autre station cliente.</span><span class="sxs-lookup"><span data-stu-id="d2fa5-180">The Wi-Fi endpoint is associated directly to another client station.</span></span><br/>    |
| <span id="Infrastructure"></span><span id="infrastructure"></span><span id="INFRASTRUCTURE"></span><dl> <span data-ttu-id="d2fa5-181"><dt>**Infrastructure**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="d2fa5-181"><dt>**Infrastructure**</dt> <dt>3</dt></span></span> </dl>    | <span data-ttu-id="d2fa5-182">Le point de terminaison Wi-Fi est associé à un réseau à l’aide d’un point d’accès.</span><span class="sxs-lookup"><span data-stu-id="d2fa5-182">The Wi-Fi endpoint is associated to a network by using an access point.</span></span><br/> |
| <span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span><dl> <span data-ttu-id="d2fa5-183"><dt> **DMTF réservé**</dt> <dt>4..</dt></span><span class="sxs-lookup"><span data-stu-id="d2fa5-183"><dt>**DMTF Reserved** </dt> <dt>4.. </dt></span></span> </dl> |                                                                                    |



 

</dd> <dt>

<span data-ttu-id="d2fa5-184">**Caption**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-184">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2fa5-185">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-186">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2fa5-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2fa5-187">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d2fa5-187">A short description of the object.</span></span> <span data-ttu-id="d2fa5-188">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d2fa5-188">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d2fa5-189">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-189">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2fa5-190">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-190">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-191">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2fa5-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2fa5-192">Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="d2fa5-192">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="d2fa5-193">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="d2fa5-193">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d2fa5-194">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d2fa5-194">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d2fa5-195">**Connecté**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-195">**Connected**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2fa5-196">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-196">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-197">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2fa5-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2fa5-198">Cette propriété a la valeur **true** si le point de terminaison Wi-Fi est connecté à un port de commutateur.</span><span class="sxs-lookup"><span data-stu-id="d2fa5-198">This property is set to **True** if the Wi-Fi endpoint is connected to a switch port.</span></span>

</dd> <dt>

<span data-ttu-id="d2fa5-199">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-199">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2fa5-200">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-201">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2fa5-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-202">Qualificateurs : **clé**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="d2fa5-202">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="d2fa5-203">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="d2fa5-203">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="d2fa5-204">Cette propriété est héritée de [**CIM \_ ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span><span class="sxs-lookup"><span data-stu-id="d2fa5-204">This property is inherited from [**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span></span>

</dd> <dt>

<span data-ttu-id="d2fa5-205">**Description**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-205">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2fa5-206">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-207">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2fa5-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2fa5-208">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="d2fa5-208">A description of the object.</span></span> <span data-ttu-id="d2fa5-209">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d2fa5-209">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d2fa5-210">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-210">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2fa5-211">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-211">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-212">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2fa5-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2fa5-213">Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="d2fa5-213">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="d2fa5-214">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="d2fa5-214">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d2fa5-215">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d2fa5-215">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d2fa5-216">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-216">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2fa5-217">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-218">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2fa5-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2fa5-219">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d2fa5-219">A display name for the object.</span></span> <span data-ttu-id="d2fa5-220">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d2fa5-220">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d2fa5-221">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-221">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2fa5-222">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-222">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-223">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2fa5-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2fa5-224">Configuration par défaut ou de démarrage d’un administrateur pour l’état activé d’un élément.</span><span class="sxs-lookup"><span data-stu-id="d2fa5-224">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="d2fa5-225">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) et sera l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="d2fa5-225">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and will be one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="d2fa5-226"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (2)</span><span class="sxs-lookup"><span data-stu-id="d2fa5-226"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-227"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (3)</span><span class="sxs-lookup"><span data-stu-id="d2fa5-227"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-228"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Activé mais hors connexion** (6)</span><span class="sxs-lookup"><span data-stu-id="d2fa5-228"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Enabled but Offline** (6)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d2fa5-229">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-229">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2fa5-230">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-230">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-231">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2fa5-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2fa5-232">Spécifie l’état activé du système planifié.</span><span class="sxs-lookup"><span data-stu-id="d2fa5-232">Specifies the enabled state of the planned system.</span></span> <span data-ttu-id="d2fa5-233">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))et peut prendre l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="d2fa5-233">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it can be one of the following values.</span></span>



| <span data-ttu-id="d2fa5-234">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2fa5-234">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="d2fa5-235">Signification</span><span class="sxs-lookup"><span data-stu-id="d2fa5-235">Meaning</span></span>                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="d2fa5-236"><dt>**Désactivé**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="d2fa5-236"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="d2fa5-237">Le système est désactivé.</span><span class="sxs-lookup"><span data-stu-id="d2fa5-237">The system is turned off.</span></span><br/>                                             |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="d2fa5-238"><dt>**Non applicable**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="d2fa5-238"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="d2fa5-239">L’élément ne prend pas en charge l’activation ou la désactivation.</span><span class="sxs-lookup"><span data-stu-id="d2fa5-239">The element does not support being enabled or disabled.</span></span><br/>               |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="d2fa5-240"><dt>**Activé mais hors connexion**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="d2fa5-240"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="d2fa5-241">Le système est activé, mais il est hors connexion.</span><span class="sxs-lookup"><span data-stu-id="d2fa5-241">The system is enabled, but offline.</span></span> <span data-ttu-id="d2fa5-242">Toutes les nouvelles demandes seront supprimées.</span><span class="sxs-lookup"><span data-stu-id="d2fa5-242">Any new requests will be dropped.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d2fa5-243">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-243">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2fa5-244">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-244">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-245">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2fa5-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2fa5-246">Spécifie la méthode de chiffrement utilisée pour protéger la confidentialité des données envoyées et reçues par le point de terminaison Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="d2fa5-246">Specifies the encryption method in use to protect the confidentiality of data sent and received by the Wi-Fi endpoint.</span></span>

<dl> <dt>

<span data-ttu-id="d2fa5-247"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="d2fa5-247"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-248"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="d2fa5-248"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-249"><span id="WEP"></span><span id="wep"></span>**Chiffrement WEP** (2)</span><span class="sxs-lookup"><span data-stu-id="d2fa5-249"><span id="WEP"></span><span id="wep"></span>**WEP** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-250"><span id="TKIP"></span><span id="tkip"></span>**TKIP** (3)</span><span class="sxs-lookup"><span data-stu-id="d2fa5-250"><span id="TKIP"></span><span id="tkip"></span>**TKIP** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-251"><span id="CCMP"></span><span id="ccmp"></span>**CCMP** (4)</span><span class="sxs-lookup"><span data-stu-id="d2fa5-251"><span id="CCMP"></span><span id="ccmp"></span>**CCMP** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-252"><span id="None"></span><span id="none"></span><span id="NONE"></span>**Aucun** (5)</span><span class="sxs-lookup"><span data-stu-id="d2fa5-252"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None** (5)</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-253"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF réservé** (6...</span><span class="sxs-lookup"><span data-stu-id="d2fa5-253"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (6..</span></span> <span data-ttu-id="d2fa5-254">)</span><span class="sxs-lookup"><span data-stu-id="d2fa5-254">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d2fa5-255">**GroupAddresses**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-255">**GroupAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2fa5-256">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-256">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-257">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2fa5-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2fa5-258">Adresses de multidiffusion sur lesquelles le point de terminaison LAN écoute.</span><span class="sxs-lookup"><span data-stu-id="d2fa5-258">Multicast addresses to which the LAN endpoint listens.</span></span> <span data-ttu-id="d2fa5-259">Cette propriété est héritée de la [**\_ LANEndpoint CIM**](/previous-versions//cc136865(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d2fa5-259">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d2fa5-260">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-260">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2fa5-261">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-261">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-262">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2fa5-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2fa5-263">Intégrité actuelle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="d2fa5-263">The current health of the element.</span></span> <span data-ttu-id="d2fa5-264">Cette propriété exprime l’intégrité de cet élément, mais pas nécessairement celle de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="d2fa5-264">This property expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="d2fa5-265">Les valeurs possibles sont comprises entre 0 et 30, où 5 signifie que l’élément est entièrement sain et 30 signifie que l’élément est complètement non opérationnel.</span><span class="sxs-lookup"><span data-stu-id="d2fa5-265">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="d2fa5-266">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d2fa5-266">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d2fa5-267">**IEEE8021xAuthenticationProtocol**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-267">**IEEE8021xAuthenticationProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2fa5-268">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-268">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-269">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2fa5-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2fa5-270">Contient le type EAP (Extensible Authentication Protocol) si et seulement si **AuthenticationMethod** contient 5 (WPA IEEE 802.1 x), 7 (WPA2 IEEE 802.1 x) ou 8 (CCKM IEEE 802.1 x).</span><span class="sxs-lookup"><span data-stu-id="d2fa5-270">Contains the Extensible Authentication Protocol (EAP) type if and only if **AuthenticationMethod** contains 5 (WPA IEEE 802.1x), 7 (WPA2 IEEE 802.1x), or 8 (CCKM IEEE 802.1x).</span></span>

<dl> <dt>

<span data-ttu-id="d2fa5-271"><span id="EAP-TLS"></span><span id="eap-tls"></span>**EAP-TLS** (0)</span><span class="sxs-lookup"><span data-stu-id="d2fa5-271"><span id="EAP-TLS"></span><span id="eap-tls"></span>**EAP-TLS** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-272"><span id="EAP-TTLS_MSCHAPv2"></span><span id="eap-ttls_mschapv2"></span><span id="EAP-TTLS_MSCHAPV2"></span>**EAP-TTLS/MSCHAPv2** (1)</span><span class="sxs-lookup"><span data-stu-id="d2fa5-272"><span id="EAP-TTLS_MSCHAPv2"></span><span id="eap-ttls_mschapv2"></span><span id="EAP-TTLS_MSCHAPV2"></span>**EAP-TTLS/MSCHAPv2** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-273"><span id="PEAPv0_EAP-MSCHAPv2"></span><span id="peapv0_eap-mschapv2"></span><span id="PEAPV0_EAP-MSCHAPV2"></span>**PEAPv0/EAP-MSCHAPv2** (2)</span><span class="sxs-lookup"><span data-stu-id="d2fa5-273"><span id="PEAPv0_EAP-MSCHAPv2"></span><span id="peapv0_eap-mschapv2"></span><span id="PEAPV0_EAP-MSCHAPV2"></span>**PEAPv0/EAP-MSCHAPv2** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-274"><span id="PEAPv1_EAP-GTC"></span><span id="peapv1_eap-gtc"></span><span id="PEAPV1_EAP-GTC"></span>**PEAPv1/EAP-GTC** (3)</span><span class="sxs-lookup"><span data-stu-id="d2fa5-274"><span id="PEAPv1_EAP-GTC"></span><span id="peapv1_eap-gtc"></span><span id="PEAPV1_EAP-GTC"></span>**PEAPv1/EAP-GTC** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-275"><span id="EAP-FAST_MSCHAPv2"></span><span id="eap-fast_mschapv2"></span><span id="EAP-FAST_MSCHAPV2"></span>**EAP-FAST/MSCHAPv2** (4)</span><span class="sxs-lookup"><span data-stu-id="d2fa5-275"><span id="EAP-FAST_MSCHAPv2"></span><span id="eap-fast_mschapv2"></span><span id="EAP-FAST_MSCHAPV2"></span>**EAP-FAST/MSCHAPv2** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-276"><span id="EAP-FAST_GTC"></span><span id="eap-fast_gtc"></span>**EAP-FAST/GTC** (5)</span><span class="sxs-lookup"><span data-stu-id="d2fa5-276"><span id="EAP-FAST_GTC"></span><span id="eap-fast_gtc"></span>**EAP-FAST/GTC** (5)</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-277"><span id="EAP-MD5"></span><span id="eap-md5"></span>**EAP-MD5** (6)</span><span class="sxs-lookup"><span data-stu-id="d2fa5-277"><span id="EAP-MD5"></span><span id="eap-md5"></span>**EAP-MD5** (6)</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-278"><span id="EAP-PSK"></span><span id="eap-psk"></span>**EAP-PSK** (7)</span><span class="sxs-lookup"><span data-stu-id="d2fa5-278"><span id="EAP-PSK"></span><span id="eap-psk"></span>**EAP-PSK** (7)</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-279"><span id="EAP-SIM"></span><span id="eap-sim"></span>**EAP-SIM** (8)</span><span class="sxs-lookup"><span data-stu-id="d2fa5-279"><span id="EAP-SIM"></span><span id="eap-sim"></span>**EAP-SIM** (8)</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-280"><span id="EAP-AKA"></span><span id="eap-aka"></span>**EAP-alias** (9)</span><span class="sxs-lookup"><span data-stu-id="d2fa5-280"><span id="EAP-AKA"></span><span id="eap-aka"></span>**EAP-AKA** (9)</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-281"><span id="EAP-FAST_TLS"></span><span id="eap-fast_tls"></span>**EAP-FAST/TLS** (10)</span><span class="sxs-lookup"><span data-stu-id="d2fa5-281"><span id="EAP-FAST_TLS"></span><span id="eap-fast_tls"></span>**EAP-FAST/TLS** (10)</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-282"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF réservé** (11..</span><span class="sxs-lookup"><span data-stu-id="d2fa5-282"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (11..</span></span> <span data-ttu-id="d2fa5-283">)</span><span class="sxs-lookup"><span data-stu-id="d2fa5-283">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d2fa5-284">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-284">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2fa5-285">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-285">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-286">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2fa5-286">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2fa5-287">Date et heure de création de la configuration de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="d2fa5-287">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="d2fa5-288">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d2fa5-288">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d2fa5-289">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-289">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2fa5-290">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-290">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-291">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2fa5-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-292">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-292">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="d2fa5-293">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="d2fa5-293">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="d2fa5-294">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d2fa5-294">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d2fa5-295">**LANID**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-295">**LANID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2fa5-296">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-296">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-297">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2fa5-297">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2fa5-298">Étiquette ou identificateur du segment LAN auquel le point de terminaison est connecté.</span><span class="sxs-lookup"><span data-stu-id="d2fa5-298">A label or identifier for the LAN segment to which the endpoint is connected.</span></span> <span data-ttu-id="d2fa5-299">Si le point de terminaison n’est pas actif/connecté actuellement, ou si ces informations ne sont pas connues, cette propriété aura la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="d2fa5-299">If the endpoint is not currently active/connected, or this information is not known, then this property will be **Null**.</span></span> <span data-ttu-id="d2fa5-300">Cette propriété est héritée de la [**\_ LANEndpoint CIM**](/previous-versions//cc136865(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d2fa5-300">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d2fa5-301">**LANType**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-301">**LANType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2fa5-302">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-302">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-303">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2fa5-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2fa5-304">Cette propriété est déconseillée à la place de la propriété **ProtocolType** .</span><span class="sxs-lookup"><span data-stu-id="d2fa5-304">This property is deprecated in lieu of the **ProtocolType** property.</span></span> <span data-ttu-id="d2fa5-305">Cette propriété est héritée de la [**\_ LANEndpoint CIM**](/previous-versions//cc136865(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d2fa5-305">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d2fa5-306">**MACAddress**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-306">**MACAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2fa5-307">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-308">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2fa5-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-309">Qualificateurs : **MaxLen** (12)</span><span class="sxs-lookup"><span data-stu-id="d2fa5-309">Qualifiers: **MaxLen** ( 12 )</span></span>
</dt> </dl>

<span data-ttu-id="d2fa5-310">Adresse MAC utilisée dans la communication avec le point de terminaison LAN.</span><span class="sxs-lookup"><span data-stu-id="d2fa5-310">The MAC address used in communication with the LAN endpoint.</span></span> <span data-ttu-id="d2fa5-311">L’adresse MAC est mise en forme en tant que 12 chiffres hexadécimaux (par exemple, « 010203040506 »), chaque paire représentant l’un des six octets de l’adresse MAC dans l’ordre des bits canoniques, conformément à la RFC 2469.</span><span class="sxs-lookup"><span data-stu-id="d2fa5-311">The MAC address is formatted as twelve hexadecimal digits (for example, "010203040506"), with each pair representing one of the six octets of the MAC address in canonical bit order according to RFC 2469.</span></span> <span data-ttu-id="d2fa5-312">Cette propriété est héritée de la [**\_ LANEndpoint CIM**](/previous-versions//cc136865(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d2fa5-312">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d2fa5-313">**MaxDataSize**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-313">**MaxDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2fa5-314">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-314">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-315">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2fa5-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-316">Qualificateurs : **unités** (« bits »)</span><span class="sxs-lookup"><span data-stu-id="d2fa5-316">Qualifiers: **Units** ("Bits")</span></span>
</dt> </dl>

<span data-ttu-id="d2fa5-317">Taille maximale, en nombre de bits, du champ d’information qui peut être envoyé ou reçu par le point de terminaison LAN.</span><span class="sxs-lookup"><span data-stu-id="d2fa5-317">The largest size, in number of bits, of the information field that may be sent or received by the LAN endpoint.</span></span> <span data-ttu-id="d2fa5-318">Cette propriété est héritée de la [**\_ LANEndpoint CIM**](/previous-versions//cc136865(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d2fa5-318">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d2fa5-319">**Nom**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-319">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2fa5-320">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-321">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2fa5-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2fa5-322">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="d2fa5-322">The label by which the object is known.</span></span> <span data-ttu-id="d2fa5-323">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d2fa5-323">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d2fa5-324">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-324">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2fa5-325">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-326">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2fa5-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-327">Qualificateurs : **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="d2fa5-327">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="d2fa5-328">Contient l’heuristique d’attribution de noms sélectionnée pour garantir que la valeur de la propriété **Name** est unique.</span><span class="sxs-lookup"><span data-stu-id="d2fa5-328">Contains the naming heuristic that is selected to ensure that the value of the **Name** property is unique.</span></span> <span data-ttu-id="d2fa5-329">Cette propriété est héritée de l' [**\_ ProtocolEndpoint CIM**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span><span class="sxs-lookup"><span data-stu-id="d2fa5-329">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span></span>

</dd> <dt>

<span data-ttu-id="d2fa5-330">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-330">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2fa5-331">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-331">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-332">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2fa5-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2fa5-333">Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="d2fa5-333">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="d2fa5-334">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="d2fa5-334">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d2fa5-335">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d2fa5-335">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d2fa5-336">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-336">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2fa5-337">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-337">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-338">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2fa5-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2fa5-339">États actuels de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d2fa5-339">The current statuses of the object.</span></span> <span data-ttu-id="d2fa5-340">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d2fa5-340">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d2fa5-341">**OtherAuthenticationMethod**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-341">**OtherAuthenticationMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2fa5-342">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-343">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2fa5-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2fa5-344">Spécifie la méthode d’authentification 802,11 si et seulement si **AuthenticationMethod** contient 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="d2fa5-344">Specifies the 802.11 authentication method if and only if **AuthenticationMethod** contains 1 (Other).</span></span> <span data-ttu-id="d2fa5-345">Le format de cette chaîne est spécifique au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="d2fa5-345">The format of this string is vendor specific.</span></span>

</dd> <dt>

<span data-ttu-id="d2fa5-346">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-346">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2fa5-347">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-348">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2fa5-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2fa5-349">Chaîne qui décrit l’état activé ou désactivé de l’élément lorsque la propriété **EnabledState** a la valeur 1 (« other »).</span><span class="sxs-lookup"><span data-stu-id="d2fa5-349">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="d2fa5-350">Cette propriété doit avoir la valeur **null** quand **EnabledState** a une valeur autre que 1.</span><span class="sxs-lookup"><span data-stu-id="d2fa5-350">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="d2fa5-351">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d2fa5-351">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d2fa5-352">**OtherEncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-352">**OtherEncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2fa5-353">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-354">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2fa5-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2fa5-355">Spécifie la méthode de chiffrement 802,11 si et seulement si **EncryptionMethod** contient 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="d2fa5-355">Specifies the 802.11 encryption method if and only if **EncryptionMethod** contains 1 (Other).</span></span> <span data-ttu-id="d2fa5-356">Le format de cette chaîne est spécifique au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="d2fa5-356">The format of this string is vendor specific.</span></span>

</dd> <dt>

<span data-ttu-id="d2fa5-357">**OtherLANType**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-357">**OtherLANType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2fa5-358">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-359">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2fa5-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2fa5-360">Cette propriété est déconseillée à la place de la propriété **OtherTypeDescription** .</span><span class="sxs-lookup"><span data-stu-id="d2fa5-360">This property is deprecated in lieu of the **OtherTypeDescription** property.</span></span> <span data-ttu-id="d2fa5-361">Cette propriété est héritée de la [**\_ LANEndpoint CIM**](/previous-versions//cc136865(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d2fa5-361">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d2fa5-362">**OtherTypeDescription**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-362">**OtherTypeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2fa5-363">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-363">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-364">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2fa5-364">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-365">Qualificateurs : **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="d2fa5-365">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="d2fa5-366">Chaîne qui décrit le type de point de terminaison de protocole lorsque la propriété **ProtocolIFType** de cette classe (ou l’une de ses sous-classes) a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="d2fa5-366">A string that describes the type of protocol endpoint when the **ProtocolIFType** property of this class (or any of its subclasses) is set to 1 (Other).</span></span> <span data-ttu-id="d2fa5-367">Cette propriété doit être définie sur **null** lorsque la propriété **ProtocolIFType** a une valeur autre que 1.</span><span class="sxs-lookup"><span data-stu-id="d2fa5-367">This property should be set to **Null** when the **ProtocolIFType** property is any value other than 1.</span></span> <span data-ttu-id="d2fa5-368">Cette propriété est héritée de l' [**\_ ProtocolEndpoint CIM**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span><span class="sxs-lookup"><span data-stu-id="d2fa5-368">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span></span>

</dd> <dt>

<span data-ttu-id="d2fa5-369">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-369">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2fa5-370">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-370">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-371">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2fa5-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2fa5-372">Fournit des informations d’état de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="d2fa5-372">Provides high level status information.</span></span> <span data-ttu-id="d2fa5-373">Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir des informations d’état d’intégrité de haut niveau et détaillées pour l’élément et ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="d2fa5-373">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="d2fa5-374">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="d2fa5-374">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d2fa5-375">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d2fa5-375">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d2fa5-376">**ProtocolIFType**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-376">**ProtocolIFType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2fa5-377">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-377">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-378">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2fa5-378">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2fa5-379">La propriété est utilisée pour catégoriser et classer les instances de cette classe.</span><span class="sxs-lookup"><span data-stu-id="d2fa5-379">The property is used to categorize and classify instances of this class.</span></span> <span data-ttu-id="d2fa5-380">Si **ProtocolIFType** a la valeur 1 (autre), les informations de type doivent être fournies dans la propriété **OtherTypeDescription** .</span><span class="sxs-lookup"><span data-stu-id="d2fa5-380">If the **ProtocolIFType** is set to 1 (Other), then the type information should be provided in the **OtherTypeDescription** property.</span></span> <span data-ttu-id="d2fa5-381">Cette propriété est héritée de l' [**\_ ProtocolEndpoint CIM**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span><span class="sxs-lookup"><span data-stu-id="d2fa5-381">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span></span>

> [!Note]  
> <span data-ttu-id="d2fa5-382">**ProtocolIFType** est une énumération qui est synchronisée avec la [MIB ifType IANA](https://www.iana.org/assignments/ianaiftype-mib).</span><span class="sxs-lookup"><span data-stu-id="d2fa5-382">**ProtocolIFType** is an enumeration that is synchronized with the [IANA ifType MIB](https://www.iana.org/assignments/ianaiftype-mib).</span></span> <span data-ttu-id="d2fa5-383">Des valeurs supplémentaires définies par le DMTF sont également incluses.</span><span class="sxs-lookup"><span data-stu-id="d2fa5-383">Additional values defined by the DMTF are also included.</span></span>

 

<dl> <dt>

<span data-ttu-id="d2fa5-384"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="d2fa5-384"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-385"><span id="IEEE_802.11"></span><span id="ieee_802.11"></span>**IEEE 802,11** (71)</span><span class="sxs-lookup"><span data-stu-id="d2fa5-385"><span id="IEEE_802.11"></span><span id="ieee_802.11"></span>**IEEE 802.11** (71)</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-386"><span id="IANA_Reserved"></span><span id="iana_reserved"></span><span id="IANA_RESERVED"></span>**IANA réservé** (225.. 4095)</span><span class="sxs-lookup"><span data-stu-id="d2fa5-386"><span id="IANA_Reserved"></span><span id="iana_reserved"></span><span id="IANA_RESERVED"></span>**IANA Reserved** (225..4095)</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-387"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (4301.. 32767)</span><span class="sxs-lookup"><span data-stu-id="d2fa5-387"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (4301..32767)</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-388"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (32768..</span><span class="sxs-lookup"><span data-stu-id="d2fa5-388"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (32768..</span></span> <span data-ttu-id="d2fa5-389">)</span><span class="sxs-lookup"><span data-stu-id="d2fa5-389">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d2fa5-390">**ProtocolType**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-390">**ProtocolType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2fa5-391">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-391">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-392">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2fa5-392">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2fa5-393">Cette propriété est déconseillée à la place de la propriété **ProtocolIFType** .</span><span class="sxs-lookup"><span data-stu-id="d2fa5-393">This property is deprecated in lieu of the **ProtocolIFType** property.</span></span> <span data-ttu-id="d2fa5-394">Cette propriété est héritée de l' [**\_ ProtocolEndpoint CIM**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span><span class="sxs-lookup"><span data-stu-id="d2fa5-394">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span></span>

</dd> <dt>

<span data-ttu-id="d2fa5-395">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-395">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2fa5-396">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-396">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-397">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2fa5-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2fa5-398">Dernier État demandé ou souhaité pour le service de gestion.</span><span class="sxs-lookup"><span data-stu-id="d2fa5-398">The last requested or desired state for the management service.</span></span> <span data-ttu-id="d2fa5-399">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d2fa5-399">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d2fa5-400">**État**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-400">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2fa5-401">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-401">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-402">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2fa5-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2fa5-403">Décrit l’état de l’élément.</span><span class="sxs-lookup"><span data-stu-id="d2fa5-403">Describes the status of the element.</span></span> <span data-ttu-id="d2fa5-404">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d2fa5-404">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="d2fa5-405">OK</span><span class="sxs-lookup"><span data-stu-id="d2fa5-405">"OK"</span></span>

<span data-ttu-id="d2fa5-406">Erreurs</span><span class="sxs-lookup"><span data-stu-id="d2fa5-406">"Error"</span></span>

<span data-ttu-id="d2fa5-407">Détérioré</span><span class="sxs-lookup"><span data-stu-id="d2fa5-407">"Degraded"</span></span>

<span data-ttu-id="d2fa5-408">Connue</span><span class="sxs-lookup"><span data-stu-id="d2fa5-408">"Unknown"</span></span>

<span data-ttu-id="d2fa5-409">« Échec prévu »</span><span class="sxs-lookup"><span data-stu-id="d2fa5-409">"Pred Fail"</span></span>

<span data-ttu-id="d2fa5-410">Démarr</span><span class="sxs-lookup"><span data-stu-id="d2fa5-410">"Starting"</span></span>

<span data-ttu-id="d2fa5-411">Arrêt</span><span class="sxs-lookup"><span data-stu-id="d2fa5-411">"Stopping"</span></span>

<span data-ttu-id="d2fa5-412">Services</span><span class="sxs-lookup"><span data-stu-id="d2fa5-412">"Service"</span></span>

<span data-ttu-id="d2fa5-413">Trop sollicité</span><span class="sxs-lookup"><span data-stu-id="d2fa5-413">"Stressed"</span></span>

<span data-ttu-id="d2fa5-414">« Non récupéré »</span><span class="sxs-lookup"><span data-stu-id="d2fa5-414">"NonRecover"</span></span>

<span data-ttu-id="d2fa5-415">« Aucun contact »</span><span class="sxs-lookup"><span data-stu-id="d2fa5-415">"No Contact"</span></span>

<span data-ttu-id="d2fa5-416">« Comm. perdue »</span><span class="sxs-lookup"><span data-stu-id="d2fa5-416">"Lost Comm"</span></span>

</dd> <dt>

<span data-ttu-id="d2fa5-417">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-417">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2fa5-418">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-418">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-419">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2fa5-419">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2fa5-420">Chaînes qui décrivent les différentes valeurs de tableau **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="d2fa5-420">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="d2fa5-421">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d2fa5-421">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d2fa5-422">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-422">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2fa5-423">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-423">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-424">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2fa5-424">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2fa5-425">Nom de la classe de création du système d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="d2fa5-425">The hosting system's creation class name.</span></span> <span data-ttu-id="d2fa5-426">Cette propriété est héritée de [**CIM \_ ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span><span class="sxs-lookup"><span data-stu-id="d2fa5-426">This property is inherited from [**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span></span>

</dd> <dt>

<span data-ttu-id="d2fa5-427">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-427">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2fa5-428">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-428">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-429">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2fa5-429">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-430">Qualificateurs : **clé**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="d2fa5-430">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="d2fa5-431">Nom du système d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="d2fa5-431">The name of the hosting system.</span></span> <span data-ttu-id="d2fa5-432">Cette propriété est héritée de [**CIM \_ ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span><span class="sxs-lookup"><span data-stu-id="d2fa5-432">This property is inherited from [**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span></span>

</dd> <dt>

<span data-ttu-id="d2fa5-433">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-433">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2fa5-434">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-434">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-435">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2fa5-435">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2fa5-436">Date et heure de la dernière modification de l’état activé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="d2fa5-436">The date and time when the enabled state of the element last changed.</span></span> <span data-ttu-id="d2fa5-437">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d2fa5-437">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d2fa5-438">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-438">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2fa5-439">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2fa5-439">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2fa5-440">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2fa5-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2fa5-441">Indique l’État cible de la transition de l’instance.</span><span class="sxs-lookup"><span data-stu-id="d2fa5-441">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="d2fa5-442">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d2fa5-442">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d2fa5-443">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d2fa5-443">Requirements</span></span>



| <span data-ttu-id="d2fa5-444">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d2fa5-444">Requirement</span></span> | <span data-ttu-id="d2fa5-445">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2fa5-445">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2fa5-446">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d2fa5-446">Minimum supported client</span></span><br/> | <span data-ttu-id="d2fa5-447">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d2fa5-447">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d2fa5-448">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d2fa5-448">Minimum supported server</span></span><br/> | <span data-ttu-id="d2fa5-449">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d2fa5-449">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d2fa5-450">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d2fa5-450">Namespace</span></span><br/>                | <span data-ttu-id="d2fa5-451">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="d2fa5-451">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d2fa5-452">MOF</span><span class="sxs-lookup"><span data-stu-id="d2fa5-452">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d2fa5-453"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d2fa5-453"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d2fa5-454">DLL</span><span class="sxs-lookup"><span data-stu-id="d2fa5-454">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2fa5-455"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d2fa5-455"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

