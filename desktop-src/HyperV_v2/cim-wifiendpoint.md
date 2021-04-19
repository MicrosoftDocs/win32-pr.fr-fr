---
description: Représente un point de terminaison de communication sans fil, qui peut envoyer et recevoir des trames de données lorsque l’appareil d’interface associé est connecté à un réseau local sans fil IEEE 802,11.
ms.assetid: 61743402-f333-4501-ba17-e676d85f72f3
title: Classe CIM_WiFiEndpoint
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_WiFiEndpoint
- CIM_WiFiEndpoint.LANID
- CIM_WiFiEndpoint.ProtocolIFType
- CIM_WiFiEndpoint.EncryptionMethod
- CIM_WiFiEndpoint.OtherEncryptionMethod
- CIM_WiFiEndpoint.AuthenticationMethod
- CIM_WiFiEndpoint.OtherAuthenticationMethod
- CIM_WiFiEndpoint.IEEE8021xAuthenticationProtocol
- CIM_WiFiEndpoint.AccessPointAddress
- CIM_WiFiEndpoint.BSSType
- CIM_WiFiEndpoint.Associated
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2e09d040f9d4530bee4347528d704cfe2e9403b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523335"
---
# <a name="cim_wifiendpoint-class"></a><span data-ttu-id="3f3dc-103">\_Classe CIM WiFiEndpoint</span><span class="sxs-lookup"><span data-stu-id="3f3dc-103">CIM\_WiFiEndpoint class</span></span>

<span data-ttu-id="3f3dc-104">Représente un point de terminaison de communication sans fil, qui peut envoyer et recevoir des trames de données lorsque l’appareil d’interface associé est connecté à un réseau local sans fil IEEE 802,11.</span><span class="sxs-lookup"><span data-stu-id="3f3dc-104">Represents a wireless communication endpoint, which can send and receive data frames when its associated interface device is connected with an IEEE 802.11 wireless LAN.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f3dc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3f3dc-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Network::Wireless"), AMENDMENT]
class CIM_WiFiEndpoint : CIM_LANEndpoint
{
  string  LANID;
  uint16  ProtocolIFType = 71;
  uint16  EncryptionMethod;
  string  OtherEncryptionMethod;
  uint16  AuthenticationMethod;
  string  OtherAuthenticationMethod;
  uint16  IEEE8021xAuthenticationProtocol;
  string  AccessPointAddress;
  uint16  BSSType;
  boolean Associated;
};
```

## <a name="members"></a><span data-ttu-id="3f3dc-106">Membres</span><span class="sxs-lookup"><span data-stu-id="3f3dc-106">Members</span></span>

<span data-ttu-id="3f3dc-107">La classe **CIM \_ WiFiEndpoint** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="3f3dc-107">The **CIM\_WiFiEndpoint** class has these types of members:</span></span>

-   [<span data-ttu-id="3f3dc-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3f3dc-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3f3dc-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3f3dc-109">Properties</span></span>

<span data-ttu-id="3f3dc-110">La classe **CIM \_ WiFiEndpoint** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="3f3dc-110">The **CIM\_WiFiEndpoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3f3dc-111">**AccessPointAddress**</span><span class="sxs-lookup"><span data-stu-id="3f3dc-111">**AccessPointAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f3dc-112">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3f3dc-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f3dc-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3f3dc-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f3dc-114">Adresse MAC du point d’accès associé au point de terminaison Wi-Fi ; Sinon, **null**.</span><span class="sxs-lookup"><span data-stu-id="3f3dc-114">The MAC address of the access point that is associated with the Wi-Fi endpoint; otherwise, **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="3f3dc-115">**Associé**</span><span class="sxs-lookup"><span data-stu-id="3f3dc-115">**Associated**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f3dc-116">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="3f3dc-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3f3dc-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3f3dc-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f3dc-118">**true** si le point de terminaison Wi-Fi est actuellement associé à un point d’accès ou à une station cliente. Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="3f3dc-118">**true** if the WiFi endpoint is currently associated with an access point or client station; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="3f3dc-119">**AuthenticationMethod**</span><span class="sxs-lookup"><span data-stu-id="3f3dc-119">**AuthenticationMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f3dc-120">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3f3dc-120">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3f3dc-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3f3dc-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f3dc-122">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("IEEE 802.11-2007 \| 8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ WiFiEndpoint**.**EncryptionMethod**","**CIM \_ WiFiEndpoint**.**IEEE8021xAuthenticationProtocol**","**CIM \_ WiFiEndpoint**.**OtherAuthenticationMethod**")</span><span class="sxs-lookup"><span data-stu-id="3f3dc-122">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("IEEE 802.11-2007 \| 8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_WiFiEndpoint**.**EncryptionMethod**", "**CIM\_WiFiEndpoint**.**IEEE8021xAuthenticationProtocol**", "**CIM\_WiFiEndpoint**.**OtherAuthenticationMethod**")</span></span>
</dt> </dl>

<span data-ttu-id="3f3dc-123">Type d’authentification utilisé entre le point de terminaison de la Wi-Fi et le réseau.</span><span class="sxs-lookup"><span data-stu-id="3f3dc-123">The authentication type used between the Wi-Fi endpoint and the network.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3f3dc-124">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="3f3dc-124">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="3f3dc-125">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="3f3dc-125">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Open_System"></span><span id="open_system"></span><span id="OPEN_SYSTEM"></span>

<span data-ttu-id="3f3dc-126">**Système ouvert** (2)</span><span class="sxs-lookup"><span data-stu-id="3f3dc-126">**Open System** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Shared_Key"></span><span id="shared_key"></span><span id="SHARED_KEY"></span>

<span data-ttu-id="3f3dc-127">**Clé partagée** (3)</span><span class="sxs-lookup"><span data-stu-id="3f3dc-127">**Shared Key** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="WPA_PSK"></span><span id="wpa_psk"></span>

<span data-ttu-id="3f3dc-128">**WPA PSK** (4)</span><span class="sxs-lookup"><span data-stu-id="3f3dc-128">**WPA PSK** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="WPA_IEEE_802.1x"></span><span id="wpa_ieee_802.1x"></span><span id="WPA_IEEE_802.1X"></span>

<span data-ttu-id="3f3dc-129">**WPA IEEE 802.1 x** (5)</span><span class="sxs-lookup"><span data-stu-id="3f3dc-129">**WPA IEEE 802.1x** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="WPA2_PSK"></span><span id="wpa2_psk"></span>

<span data-ttu-id="3f3dc-130">**WPA2 PSK** (6)</span><span class="sxs-lookup"><span data-stu-id="3f3dc-130">**WPA2 PSK** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="WPA2_IEEE_802.1x"></span><span id="wpa2_ieee_802.1x"></span><span id="WPA2_IEEE_802.1X"></span>

<span data-ttu-id="3f3dc-131">**WPA2 IEEE 802.1 x** (7)</span><span class="sxs-lookup"><span data-stu-id="3f3dc-131">**WPA2 IEEE 802.1x** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="CCKM_IEEE_802.1x"></span><span id="cckm_ieee_802.1x"></span><span id="CCKM_IEEE_802.1X"></span>

<span data-ttu-id="3f3dc-132">**CCKM IEEE 802.1 x** (8)</span><span class="sxs-lookup"><span data-stu-id="3f3dc-132">**CCKM IEEE 802.1x** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="3f3dc-133">**DMTF réservé** (9...)</span><span class="sxs-lookup"><span data-stu-id="3f3dc-133">**DMTF Reserved** (9..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3f3dc-134">**BSSType**</span><span class="sxs-lookup"><span data-stu-id="3f3dc-134">**BSSType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f3dc-135">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3f3dc-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3f3dc-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3f3dc-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f3dc-137">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« IEEE 802.11-2007 \| 3,16 »)</span><span class="sxs-lookup"><span data-stu-id="3f3dc-137">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("IEEE 802.11-2007 \| 3.16")</span></span>
</dt> </dl>

<span data-ttu-id="3f3dc-138">Type BSS (Basic Service Set) du réseau qui correspond à l’instance.</span><span class="sxs-lookup"><span data-stu-id="3f3dc-138">The basic service set (BSS) type of the network that corresponds to the instance.</span></span> <span data-ttu-id="3f3dc-139">Un BSS est un ensemble de stations contrôlées par une seule fonction de coordination.</span><span class="sxs-lookup"><span data-stu-id="3f3dc-139">A BSS is a set of stations controlled by a single coordination function.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3f3dc-140">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="3f3dc-140">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Independent"></span><span id="independent"></span><span id="INDEPENDENT"></span>

<span data-ttu-id="3f3dc-141">**Indépendant** (2)</span><span class="sxs-lookup"><span data-stu-id="3f3dc-141">**Independent** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Infrastructure"></span><span id="infrastructure"></span><span id="INFRASTRUCTURE"></span>

<span data-ttu-id="3f3dc-142">**Infrastructure** (3)</span><span class="sxs-lookup"><span data-stu-id="3f3dc-142">**Infrastructure** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="3f3dc-143">**DMTF réservé** (4...)</span><span class="sxs-lookup"><span data-stu-id="3f3dc-143">**DMTF Reserved** (4..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3f3dc-144">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="3f3dc-144">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f3dc-145">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3f3dc-145">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3f3dc-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3f3dc-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f3dc-147">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("IEEE 802.11-2007 \| 8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ WiFiEndpoint**.**AuthenticationMethod**","**CIM \_ WiFiEndpoint**.**OtherEncryptionMethod**")</span><span class="sxs-lookup"><span data-stu-id="3f3dc-147">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("IEEE 802.11-2007 \| 8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_WiFiEndpoint**.**AuthenticationMethod**", "**CIM\_WiFiEndpoint**.**OtherEncryptionMethod**")</span></span>
</dt> </dl>

<span data-ttu-id="3f3dc-148">Type de chiffrement utilisé lors de l’envoi et de la réception de données via le point de terminaison Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="3f3dc-148">The encryption type used when sending and receiving data through the Wi-Fi endpoint.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3f3dc-149">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="3f3dc-149">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="3f3dc-150">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="3f3dc-150">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="WEP"></span><span id="wep"></span>

<span data-ttu-id="3f3dc-151">**Chiffrement WEP** (2)</span><span class="sxs-lookup"><span data-stu-id="3f3dc-151">**WEP** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="TKIP"></span><span id="tkip"></span>

<span data-ttu-id="3f3dc-152">**TKIP** (3)</span><span class="sxs-lookup"><span data-stu-id="3f3dc-152">**TKIP** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="CCMP"></span><span id="ccmp"></span>

<span data-ttu-id="3f3dc-153">**CCMP** (4)</span><span class="sxs-lookup"><span data-stu-id="3f3dc-153">**CCMP** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="3f3dc-154">**Aucun** (5)</span><span class="sxs-lookup"><span data-stu-id="3f3dc-154">**None** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="3f3dc-155">**DMTF réservé** (6...)</span><span class="sxs-lookup"><span data-stu-id="3f3dc-155">**DMTF Reserved** (6..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3f3dc-156">**IEEE8021xAuthenticationProtocol**</span><span class="sxs-lookup"><span data-stu-id="3f3dc-156">**IEEE8021xAuthenticationProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f3dc-157">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3f3dc-157">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3f3dc-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3f3dc-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f3dc-159">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("RFC4017. IETF "," RFC2716. IETF «, draft-ietf-pppext-EAP-TTLS. IETF "," Draft-Kamath-pppext-PEAPv0. IETF "," Draft-Josefsson-pppext-EAP-TLS-EAP "," RFC4851. IETF "," RFC3748. IETF "," RFC4764. IETF "," RFC4186. IETF "," RFC4187. IETF "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ WiFiEndpoint**.**AuthenticationMethod**»)</span><span class="sxs-lookup"><span data-stu-id="3f3dc-159">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("RFC4017.IETF", "RFC2716.IETF", "draft-ietf-pppext-eap-ttls.IETF", "draft-kamath-pppext-peapv0.IETF", "draft-josefsson-pppext-eap-tls-eap", "RFC4851.IETF", "RFC3748.IETF", "RFC4764.IETF", "RFC4186.IETF", "RFC4187.IETF"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_WiFiEndpoint**.**AuthenticationMethod**")</span></span>
</dt> </dl>

<span data-ttu-id="3f3dc-160">Le type EAP (Extensible Authentication Protocol) pour le point de terminaison Wi-Fi lorsque **AuthenticationMethod** contient « 7 » (WPA IEEE 802.1 x) ou « 8 » (CCKM IEEE 802.1 x).</span><span class="sxs-lookup"><span data-stu-id="3f3dc-160">The EAP (Extensible Authentication Protocol) type for the Wi-Fi endpoint when **AuthenticationMethod** contains "7" (WPA IEEE 802.1x) or "8" (CCKM IEEE 802.1x).</span></span>

<dt>

<span id="EAP-TLS"></span><span id="eap-tls"></span>

<span data-ttu-id="3f3dc-161">**EAP-TLS** (0)</span><span class="sxs-lookup"><span data-stu-id="3f3dc-161">**EAP-TLS** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="EAP-TTLS_MSCHAPv2"></span><span id="eap-ttls_mschapv2"></span><span id="EAP-TTLS_MSCHAPV2"></span>

<span data-ttu-id="3f3dc-162">**EAP-TTLS/MSCHAPv2** (1)</span><span class="sxs-lookup"><span data-stu-id="3f3dc-162">**EAP-TTLS/MSCHAPv2** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="PEAPv0_EAP-MSCHAPv2"></span><span id="peapv0_eap-mschapv2"></span><span id="PEAPV0_EAP-MSCHAPV2"></span>

<span data-ttu-id="3f3dc-163">**PEAPv0/EAP-MSCHAPv2** (2)</span><span class="sxs-lookup"><span data-stu-id="3f3dc-163">**PEAPv0/EAP-MSCHAPv2** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PEAPv1_EAP-GTC"></span><span id="peapv1_eap-gtc"></span><span id="PEAPV1_EAP-GTC"></span>

<span data-ttu-id="3f3dc-164">**PEAPv1/EAP-GTC** (3)</span><span class="sxs-lookup"><span data-stu-id="3f3dc-164">**PEAPv1/EAP-GTC** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="EAP-FAST_MSCHAPv2"></span><span id="eap-fast_mschapv2"></span><span id="EAP-FAST_MSCHAPV2"></span>

<span data-ttu-id="3f3dc-165">**EAP-FAST/MSCHAPv2** (4)</span><span class="sxs-lookup"><span data-stu-id="3f3dc-165">**EAP-FAST/MSCHAPv2** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="EAP-FAST_GTC"></span><span id="eap-fast_gtc"></span>

<span data-ttu-id="3f3dc-166">**EAP-FAST/GTC** (5)</span><span class="sxs-lookup"><span data-stu-id="3f3dc-166">**EAP-FAST/GTC** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="EAP-MD5"></span><span id="eap-md5"></span>

<span data-ttu-id="3f3dc-167">**EAP-MD5** (6)</span><span class="sxs-lookup"><span data-stu-id="3f3dc-167">**EAP-MD5** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="EAP-PSK"></span><span id="eap-psk"></span>

<span data-ttu-id="3f3dc-168">**EAP-PSK** (7)</span><span class="sxs-lookup"><span data-stu-id="3f3dc-168">**EAP-PSK** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="EAP-SIM"></span><span id="eap-sim"></span>

<span data-ttu-id="3f3dc-169">**EAP-SIM** (8)</span><span class="sxs-lookup"><span data-stu-id="3f3dc-169">**EAP-SIM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="EAP-AKA"></span><span id="eap-aka"></span>

<span data-ttu-id="3f3dc-170">**EAP-alias** (9)</span><span class="sxs-lookup"><span data-stu-id="3f3dc-170">**EAP-AKA** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="EAP-FAST_TLS"></span><span id="eap-fast_tls"></span>

<span data-ttu-id="3f3dc-171">**EAP-FAST/TLS** (10)</span><span class="sxs-lookup"><span data-stu-id="3f3dc-171">**EAP-FAST/TLS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="3f3dc-172">**DMTF réservé** (11..)</span><span class="sxs-lookup"><span data-stu-id="3f3dc-172">**DMTF Reserved** (11..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3f3dc-173">**LANID**</span><span class="sxs-lookup"><span data-stu-id="3f3dc-173">**LANID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f3dc-174">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3f3dc-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f3dc-175">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3f3dc-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f3dc-176">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LANID"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("IEEE 802.11-2007 \| 7.3.2.1")</span><span class="sxs-lookup"><span data-stu-id="3f3dc-176">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LANID"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("IEEE 802.11-2007 \| 7.3.2.1")</span></span>
</dt> </dl>

<span data-ttu-id="3f3dc-177">Identificateur SSID (Service Set Identifier) du réseau local sans fil associé au point de terminaison Wi-Fi ; Sinon, **null**.</span><span class="sxs-lookup"><span data-stu-id="3f3dc-177">The service set identifier (SSID) of the wireless LAN that is associated with the Wi-Fi endpoint; otherwise, **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="3f3dc-178">**OtherAuthenticationMethod**</span><span class="sxs-lookup"><span data-stu-id="3f3dc-178">**OtherAuthenticationMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f3dc-179">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3f3dc-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f3dc-180">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3f3dc-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f3dc-181">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ WiFiEndpoint**.**AuthenticationMethod**»)</span><span class="sxs-lookup"><span data-stu-id="3f3dc-181">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_WiFiEndpoint**.**AuthenticationMethod**")</span></span>
</dt> </dl>

<span data-ttu-id="3f3dc-182">Type d’authentification utilisé entre le point de terminaison de la Wi-Fi et le réseau lorsque **AuthenticationMethod** contient « 1 » (autre).</span><span class="sxs-lookup"><span data-stu-id="3f3dc-182">The authentication type used between the Wi-Fi endpoint and the network when **AuthenticationMethod** contains "1" (Other).</span></span>

</dd> <dt>

<span data-ttu-id="3f3dc-183">**OtherEncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="3f3dc-183">**OtherEncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f3dc-184">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3f3dc-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f3dc-185">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3f3dc-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f3dc-186">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ WiFiEndpoint**.**EncryptionMethod**»)</span><span class="sxs-lookup"><span data-stu-id="3f3dc-186">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_WiFiEndpoint**.**EncryptionMethod**")</span></span>
</dt> </dl>

<span data-ttu-id="3f3dc-187">Décrit le type de chiffrement pour le point de terminaison Wi-Fi lorsque **EncryptionMethod** contient « 1 » (autre).</span><span class="sxs-lookup"><span data-stu-id="3f3dc-187">Describes the encryption type for the Wi-Fi endpoint when **EncryptionMethod** contains "1" (Other).</span></span>

</dd> <dt>

<span data-ttu-id="3f3dc-188">**ProtocolIFType**</span><span class="sxs-lookup"><span data-stu-id="3f3dc-188">**ProtocolIFType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f3dc-189">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3f3dc-189">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3f3dc-190">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3f3dc-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f3dc-191">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ProtocolIFType")</span><span class="sxs-lookup"><span data-stu-id="3f3dc-191">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ProtocolIFType")</span></span>
</dt> </dl>

<span data-ttu-id="3f3dc-192">Catégorie ou classification de cette instance.</span><span class="sxs-lookup"><span data-stu-id="3f3dc-192">The category or classification of this instance.</span></span> <span data-ttu-id="3f3dc-193">Les valeurs possibles sont limitées à la Wi-Fi et aux valeurs réservées à partir du DMTF et de la [MIB IfType IANA](https://www.iana.org/assignments/ianaiftype-mib).</span><span class="sxs-lookup"><span data-stu-id="3f3dc-193">The possible values are limited to the Wi-Fi and reserved values from the DMTF and [IANA ifType MIB](https://www.iana.org/assignments/ianaiftype-mib).</span></span>

<span data-ttu-id="3f3dc-194">Si la valeur de **ProtocolIFType** est définie sur « 1 » (autre), les informations de type doivent être fournies dans la propriété **OtherTypeDescription** .</span><span class="sxs-lookup"><span data-stu-id="3f3dc-194">If the **ProtocolIFType** is set to "1" (Other), then the type information should be provided in the **OtherTypeDescription** property.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="3f3dc-195">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="3f3dc-195">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.11"></span><span id="ieee_802.11"></span>

<span data-ttu-id="3f3dc-196">**IEEE 802,11** (71)</span><span class="sxs-lookup"><span data-stu-id="3f3dc-196">**IEEE 802.11** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="IANA_Reserved"></span><span id="iana_reserved"></span><span id="IANA_RESERVED"></span>

<span data-ttu-id="3f3dc-197">**IANA réservé** (225.. 4095)</span><span class="sxs-lookup"><span data-stu-id="3f3dc-197">**IANA Reserved** (225..4095)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="3f3dc-198">**DMTF réservé** (4301.. 32767)</span><span class="sxs-lookup"><span data-stu-id="3f3dc-198">**DMTF Reserved** (4301..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="3f3dc-199">**Fournisseur réservé** (32768...)</span><span class="sxs-lookup"><span data-stu-id="3f3dc-199">**Vendor Reserved** (32768..)</span></span>


<span data-ttu-id="3f3dc-200"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="3f3dc-200"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="3f3dc-201">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3f3dc-201">Requirements</span></span>



| <span data-ttu-id="3f3dc-202">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3f3dc-202">Requirement</span></span> | <span data-ttu-id="3f3dc-203">Valeur</span><span class="sxs-lookup"><span data-stu-id="3f3dc-203">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f3dc-204">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3f3dc-204">Minimum supported client</span></span><br/> | <span data-ttu-id="3f3dc-205">Windows 8</span><span class="sxs-lookup"><span data-stu-id="3f3dc-205">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="3f3dc-206">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3f3dc-206">Minimum supported server</span></span><br/> | <span data-ttu-id="3f3dc-207">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3f3dc-207">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="3f3dc-208">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3f3dc-208">Namespace</span></span><br/>                | <span data-ttu-id="3f3dc-209">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="3f3dc-209">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="3f3dc-210">MOF</span><span class="sxs-lookup"><span data-stu-id="3f3dc-210">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3f3dc-211"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3f3dc-211"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3f3dc-212">DLL</span><span class="sxs-lookup"><span data-stu-id="3f3dc-212">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f3dc-213"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3f3dc-213"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3f3dc-214">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f3dc-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f3dc-215">**\_LANENDPOINT CIM**</span><span class="sxs-lookup"><span data-stu-id="3f3dc-215">**CIM\_LANEndpoint**</span></span>](cim-lanendpoint.md)
</dt> </dl>

 

