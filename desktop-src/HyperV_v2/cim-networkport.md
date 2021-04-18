---
description: Représentation logique d’un port réseau sur un périphérique réseau.
ms.assetid: afcfc93d-174e-43b5-a16f-28937b4bf81a
title: Classe CIM_NetworkPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_NetworkPort
- CIM_NetworkPort.Speed
- CIM_NetworkPort.OtherNetworkPortType
- CIM_NetworkPort.PortNumber
- CIM_NetworkPort.LinkTechnology
- CIM_NetworkPort.OtherLinkTechnology
- CIM_NetworkPort.PermanentAddress
- CIM_NetworkPort.NetworkAddresses
- CIM_NetworkPort.FullDuplex
- CIM_NetworkPort.AutoSense
- CIM_NetworkPort.SupportedMaximumTransmissionUnit
- CIM_NetworkPort.ActiveMaximumTransmissionUnit
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9e3ac64b55e17d0526527ebbaca168c3f7b289f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210063"
---
# <a name="cim_networkport-class"></a><span data-ttu-id="26cb9-103">\_Classe CIM NetworkPort</span><span class="sxs-lookup"><span data-stu-id="26cb9-103">CIM\_NetworkPort class</span></span>

<span data-ttu-id="26cb9-104">Représentation logique d’un port réseau sur un périphérique réseau.</span><span class="sxs-lookup"><span data-stu-id="26cb9-104">A logical representation of a network port on a network device.</span></span>

## <a name="syntax"></a><span data-ttu-id="26cb9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="26cb9-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Ports"), AMENDMENT]
class CIM_NetworkPort : CIM_LogicalPort
{
  uint64  Speed;
  string  OtherNetworkPortType;
  uint16  PortNumber;
  uint16  LinkTechnology;
  string  OtherLinkTechnology;
  string  PermanentAddress;
  string  NetworkAddresses[];
  boolean FullDuplex;
  boolean AutoSense;
  uint64  SupportedMaximumTransmissionUnit;
  uint64  ActiveMaximumTransmissionUnit;
};
```

## <a name="members"></a><span data-ttu-id="26cb9-106">Membres</span><span class="sxs-lookup"><span data-stu-id="26cb9-106">Members</span></span>

<span data-ttu-id="26cb9-107">La classe **CIM \_ NetworkPort** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="26cb9-107">The **CIM\_NetworkPort** class has these types of members:</span></span>

-   [<span data-ttu-id="26cb9-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="26cb9-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="26cb9-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="26cb9-109">Properties</span></span>

<span data-ttu-id="26cb9-110">La classe **CIM \_ NetworkPort** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="26cb9-110">The **CIM\_NetworkPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="26cb9-111">**ActiveMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="26cb9-111">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26cb9-112">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="26cb9-112">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="26cb9-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="26cb9-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26cb9-114">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes"), **punitif** ("Byte")</span><span class="sxs-lookup"><span data-stu-id="26cb9-114">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="26cb9-115">Unité de transmission maximale (MTU) active ou négociée qui est prise en charge par le port.</span><span class="sxs-lookup"><span data-stu-id="26cb9-115">The active or negotiated maximum transmission unit (MTU) that is supported by the port.</span></span>

</dd> <dt>

<span data-ttu-id="26cb9-116">**Détection automatique**</span><span class="sxs-lookup"><span data-stu-id="26cb9-116">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26cb9-117">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="26cb9-117">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="26cb9-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="26cb9-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26cb9-119">**true** si le port peut déterminer automatiquement la vitesse ou d’autres caractéristiques de communication du support réseau attaché ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="26cb9-119">**true** if the port can automatically determine the speed or other communications characteristic of the attached network media; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="26cb9-120">**FullDuplex**</span><span class="sxs-lookup"><span data-stu-id="26cb9-120">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26cb9-121">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="26cb9-121">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="26cb9-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="26cb9-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26cb9-123">**true** si le port fonctionne en mode duplex intégral ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="26cb9-123">**true** if the port is operating in full duplex mode; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="26cb9-124">**LinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="26cb9-124">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26cb9-125">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="26cb9-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="26cb9-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="26cb9-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26cb9-127">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ NetworkPort**.**OtherLinkTechnology**")</span><span class="sxs-lookup"><span data-stu-id="26cb9-127">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_NetworkPort**.**OtherLinkTechnology**")</span></span>
</dt> </dl>

<span data-ttu-id="26cb9-128">Technologie de liaison utilisée par le port.</span><span class="sxs-lookup"><span data-stu-id="26cb9-128">The link technology used by the port.</span></span> <span data-ttu-id="26cb9-129">Quand la valeur est définie sur « 1 » (autre), la propriété **OtherLinkTechnology** contient une description du type de lien.</span><span class="sxs-lookup"><span data-stu-id="26cb9-129">When set to "1" (other), the **OtherLinkTechnology** property contains a description of the link type.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="26cb9-130">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="26cb9-130">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="26cb9-131">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="26cb9-131">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

<span data-ttu-id="26cb9-132">**Ethernet** (2)</span><span class="sxs-lookup"><span data-stu-id="26cb9-132">**Ethernet** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="IB"></span><span id="ib"></span>

<span data-ttu-id="26cb9-133">**IB** (3)</span><span class="sxs-lookup"><span data-stu-id="26cb9-133">**IB** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="FC"></span><span id="fc"></span>

<span data-ttu-id="26cb9-134">**FC** (4)</span><span class="sxs-lookup"><span data-stu-id="26cb9-134">**FC** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="FDDI"></span><span id="fddi"></span>

<span data-ttu-id="26cb9-135">**FDDI** (5)</span><span class="sxs-lookup"><span data-stu-id="26cb9-135">**FDDI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATM"></span><span id="atm"></span>

<span data-ttu-id="26cb9-136">**ATM** (6)</span><span class="sxs-lookup"><span data-stu-id="26cb9-136">**ATM** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>

<span data-ttu-id="26cb9-137">**Token Ring** (7)</span><span class="sxs-lookup"><span data-stu-id="26cb9-137">**Token Ring** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>

<span data-ttu-id="26cb9-138">**Relais de trames** (8)</span><span class="sxs-lookup"><span data-stu-id="26cb9-138">**Frame Relay** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>

<span data-ttu-id="26cb9-139">**Infrarouge** (9)</span><span class="sxs-lookup"><span data-stu-id="26cb9-139">**Infrared** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>

<span data-ttu-id="26cb9-140">**Bluetooth** (10)</span><span class="sxs-lookup"><span data-stu-id="26cb9-140">**BlueTooth** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Wireless_LAN"></span><span id="wireless_lan"></span><span id="WIRELESS_LAN"></span>

<span data-ttu-id="26cb9-141">**Réseau local sans fil** (11)</span><span class="sxs-lookup"><span data-stu-id="26cb9-141">**Wireless LAN** (11)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="26cb9-142">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="26cb9-142">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26cb9-143">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="26cb9-143">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="26cb9-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="26cb9-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26cb9-145">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Carte réseau DMTF 802 Port \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="26cb9-145">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Network Adapter 802 Port\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="26cb9-146">Tableau qui contient les adresses réseau du port.</span><span class="sxs-lookup"><span data-stu-id="26cb9-146">An array that contains the network addresses for the port.</span></span>

</dd> <dt>

<span data-ttu-id="26cb9-147">**OtherLinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="26cb9-147">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26cb9-148">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="26cb9-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26cb9-149">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="26cb9-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26cb9-150">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ NetworkPort**.**LinkTechnology**")</span><span class="sxs-lookup"><span data-stu-id="26cb9-150">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_NetworkPort**.**LinkTechnology**")</span></span>
</dt> </dl>

<span data-ttu-id="26cb9-151">La technologie de liaison lorsque **LinkTechnology** a la valeur « 1 », (autre).</span><span class="sxs-lookup"><span data-stu-id="26cb9-151">The link technology when **LinkTechnology** is set to "1", (other).</span></span>

</dd> <dt>

<span data-ttu-id="26cb9-152">**OtherNetworkPortType**</span><span class="sxs-lookup"><span data-stu-id="26cb9-152">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26cb9-153">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="26cb9-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26cb9-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="26cb9-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26cb9-155">Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**CIM \_ NetworkPort**.**OtherPortType**"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ LogicalPort**](cim-logicalport.md).**PortType**")</span><span class="sxs-lookup"><span data-stu-id="26cb9-155">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**CIM\_NetworkPort**.**OtherPortType**"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_LogicalPort**](cim-logicalport.md).**PortType**")</span></span>
</dt> </dl>

> [!Note]  
> <span data-ttu-id="26cb9-156">Description déconseillée : type de module du port, lorsque la propriété **portType** contient 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="26cb9-156">Deprecated description: The module type of the port, when the **PortType** property contains 1 (other).</span></span>

 

<span data-ttu-id="26cb9-157">Cette propriété est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="26cb9-157">This property is deprecated.</span></span> <span data-ttu-id="26cb9-158">Au lieu de cela, nous vous recommandons d’utiliser la propriété **portType** dans la classe [**CIM \_ LogicalPort**](cim-logicalport.md) .</span><span class="sxs-lookup"><span data-stu-id="26cb9-158">Instead, we recommend the **PortType** property in the [**CIM\_LogicalPort**](cim-logicalport.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="26cb9-159">**PermanentAddress**</span><span class="sxs-lookup"><span data-stu-id="26cb9-159">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26cb9-160">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="26cb9-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26cb9-161">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="26cb9-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26cb9-162">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Carte réseau DMTF 802 Port \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="26cb9-162">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Network Adapter 802 Port\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="26cb9-163">Adresse réseau qui est codée en dur dans un port.</span><span class="sxs-lookup"><span data-stu-id="26cb9-163">The network address that is hardcoded into a port.</span></span> <span data-ttu-id="26cb9-164">L’adresse codée en dur peut être modifiée à l’aide d’une mise à niveau du microprogramme ou d’une configuration logicielle.</span><span class="sxs-lookup"><span data-stu-id="26cb9-164">The hardcoded address can be changed using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="26cb9-165">Lorsque cette modification est apportée, cette propriété doit être mise à jour en même temps.</span><span class="sxs-lookup"><span data-stu-id="26cb9-165">When this change is made, this property should be updated at the same time.</span></span> <span data-ttu-id="26cb9-166">**PermanentAddress** doit être laissé vide si l’adresse n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="26cb9-166">**PermanentAddress** should be left blank if the address doesn't exist.</span></span>

</dd> <dt>

<span data-ttu-id="26cb9-167">**Numéroport**</span><span class="sxs-lookup"><span data-stu-id="26cb9-167">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26cb9-168">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="26cb9-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="26cb9-169">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="26cb9-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26cb9-170">Numéro de port du port réseau.</span><span class="sxs-lookup"><span data-stu-id="26cb9-170">The port number of the network port.</span></span> <span data-ttu-id="26cb9-171">Les ports réseau sont souvent numérotés par rapport à un module logique ou à un élément réseau.</span><span class="sxs-lookup"><span data-stu-id="26cb9-171">Network ports are often numbered relative to either a logical module or a network element.</span></span>

</dd> <dt>

<span data-ttu-id="26cb9-172">**Vitesse**</span><span class="sxs-lookup"><span data-stu-id="26cb9-172">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26cb9-173">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="26cb9-173">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="26cb9-174">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="26cb9-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26cb9-175">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Speed"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits par seconde"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| MIB-II. ifSpeed "," MIF. \|Carte réseau DMTF 802 Port \| 001,5 "), **punitif** (" bit/seconde ")</span><span class="sxs-lookup"><span data-stu-id="26cb9-175">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Speed"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits per Second"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|MIB-II.ifSpeed", "MIF.DMTF\|Network Adapter 802 Port\|001.5"), **PUnit** ("bit / second")</span></span>
</dt> </dl>

<span data-ttu-id="26cb9-176">Bande passante actuelle du port en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="26cb9-176">The current bandwidth of the port in bits per second.</span></span> <span data-ttu-id="26cb9-177">Pour les ports qui varient en bande passante, ou pour ceux pour lesquels aucune estimation précise ne peut être effectuée, cette propriété doit contenir la bande passante nominale.</span><span class="sxs-lookup"><span data-stu-id="26cb9-177">For ports that vary in bandwidth, or for those where no accurate estimation can be made, this property should contain the nominal bandwidth.</span></span>

</dd> <dt>

<span data-ttu-id="26cb9-178">**SupportedMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="26cb9-178">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26cb9-179">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="26cb9-179">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="26cb9-180">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="26cb9-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26cb9-181">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes"), **punitif** ("Byte")</span><span class="sxs-lookup"><span data-stu-id="26cb9-181">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="26cb9-182">Unité de transmission maximale (MTU) prise en charge par le port.</span><span class="sxs-lookup"><span data-stu-id="26cb9-182">The maximum transmission unit (MTU) that is supported by the port.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="26cb9-183">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="26cb9-183">Requirements</span></span>



| <span data-ttu-id="26cb9-184">Condition requise</span><span class="sxs-lookup"><span data-stu-id="26cb9-184">Requirement</span></span> | <span data-ttu-id="26cb9-185">Valeur</span><span class="sxs-lookup"><span data-stu-id="26cb9-185">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26cb9-186">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26cb9-186">Minimum supported client</span></span><br/> | <span data-ttu-id="26cb9-187">Windows 8</span><span class="sxs-lookup"><span data-stu-id="26cb9-187">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="26cb9-188">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26cb9-188">Minimum supported server</span></span><br/> | <span data-ttu-id="26cb9-189">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="26cb9-189">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="26cb9-190">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="26cb9-190">Namespace</span></span><br/>                | <span data-ttu-id="26cb9-191">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="26cb9-191">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="26cb9-192">MOF</span><span class="sxs-lookup"><span data-stu-id="26cb9-192">MOF</span></span><br/>                      | <dl> <span data-ttu-id="26cb9-193"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="26cb9-193"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="26cb9-194">DLL</span><span class="sxs-lookup"><span data-stu-id="26cb9-194">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26cb9-195"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="26cb9-195"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="26cb9-196">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="26cb9-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26cb9-197">**\_LOGICALPORT CIM**</span><span class="sxs-lookup"><span data-stu-id="26cb9-197">**CIM\_LogicalPort**</span></span>](cim-logicalport.md)
</dt> </dl>

 

