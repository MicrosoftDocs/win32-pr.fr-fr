---
description: Point de terminaison sur un commutateur ou une station terminal qui est affecté à un réseau local virtuel ou qui accepte le trafic à partir d’un ou de plusieurs réseaux locaux virtuels.
ms.assetid: 20943be3-35c3-4bf5-8f1a-d4095fa6897e
title: Classe CIM_VLANEndpoint
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VLANEndpoint
- CIM_VLANEndpoint.DesiredEndpointMode
- CIM_VLANEndpoint.OtherEndpointMode
- CIM_VLANEndpoint.OperationalEndpointMode
- CIM_VLANEndpoint.DesiredVLANTrunkEncapsulation
- CIM_VLANEndpoint.OtherTrunkEncapsulation
- CIM_VLANEndpoint.OperationalVLANTrunkEncapsulation
- CIM_VLANEndpoint.GVRPStatus
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0f7b0d1318e4c24ab7381032877d16a8ea83868b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112007"
---
# <a name="cim_vlanendpoint-class"></a><span data-ttu-id="15fa6-103">\_Classe CIM VLANEndpoint</span><span class="sxs-lookup"><span data-stu-id="15fa6-103">CIM\_VLANEndpoint class</span></span>

<span data-ttu-id="15fa6-104">Point de terminaison sur un commutateur ou une station terminal qui est affecté à un réseau local virtuel ou qui accepte le trafic à partir d’un ou de plusieurs réseaux locaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="15fa6-104">An endpoint on a switch or end station that is assigned to a VLAN, or accepts traffic from one or more VLANs.</span></span>

## <a name="syntax"></a><span data-ttu-id="15fa6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="15fa6-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.26.0"), UMLPackagePath("CIM::Network::VLAN"), AMENDMENT]
class CIM_VLANEndpoint : CIM_ProtocolEndpoint
{
  uint16 DesiredEndpointMode;
  string OtherEndpointMode;
  uint16 OperationalEndpointMode;
  uint16 DesiredVLANTrunkEncapsulation;
  string OtherTrunkEncapsulation;
  uint16 OperationalVLANTrunkEncapsulation;
  uint16 GVRPStatus;
};
```

## <a name="members"></a><span data-ttu-id="15fa6-106">Membres</span><span class="sxs-lookup"><span data-stu-id="15fa6-106">Members</span></span>

<span data-ttu-id="15fa6-107">La classe **CIM \_ VLANEndpoint** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="15fa6-107">The **CIM\_VLANEndpoint** class has these types of members:</span></span>

-   [<span data-ttu-id="15fa6-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="15fa6-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="15fa6-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="15fa6-109">Properties</span></span>

<span data-ttu-id="15fa6-110">La classe **CIM \_ VLANEndpoint** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="15fa6-110">The **CIM\_VLANEndpoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="15fa6-111">**DesiredEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="15fa6-111">**DesiredEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15fa6-112">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="15fa6-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="15fa6-113">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="15fa6-113">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="15fa6-114">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VLANEndpoint**.**OperationalEndpointMode**","**CIM \_ VLANEndpoint**.**OtherEndpointMode**")</span><span class="sxs-lookup"><span data-stu-id="15fa6-114">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VLANEndpoint**.**OperationalEndpointMode**", "**CIM\_VLANEndpoint**.**OtherEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="15fa6-115">Mode VLAN demandé pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="15fa6-115">The requested VLAN mode for the endpoint.</span></span>

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="15fa6-116">**DMTF réservé** (0)</span><span class="sxs-lookup"><span data-stu-id="15fa6-116">**DMTF Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="15fa6-117">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="15fa6-117">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Access"></span><span id="access"></span><span id="ACCESS"></span>

<span data-ttu-id="15fa6-118">**Accès** (2)</span><span class="sxs-lookup"><span data-stu-id="15fa6-118">**Access** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Dynamic_Auto"></span><span id="dynamic_auto"></span><span id="DYNAMIC_AUTO"></span>

<span data-ttu-id="15fa6-119">**Automatique dynamique** (3)</span><span class="sxs-lookup"><span data-stu-id="15fa6-119">**Dynamic Auto** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Dynamic_Desirable"></span><span id="dynamic_desirable"></span><span id="DYNAMIC_DESIRABLE"></span>

<span data-ttu-id="15fa6-120">**Désirable dynamique** (4)</span><span class="sxs-lookup"><span data-stu-id="15fa6-120">**Dynamic Desirable** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Trunk"></span><span id="trunk"></span><span id="TRUNK"></span>

<span data-ttu-id="15fa6-121">**Trunk** (5)</span><span class="sxs-lookup"><span data-stu-id="15fa6-121">**Trunk** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Dot1Q_Tunnel"></span><span id="dot1q_tunnel"></span><span id="DOT1Q_TUNNEL"></span>

<span data-ttu-id="15fa6-122">**Tunnel Dot1Q** (6)</span><span class="sxs-lookup"><span data-stu-id="15fa6-122">**Dot1Q Tunnel** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="15fa6-123">**DMTF réservé** (7.. 32767)</span><span class="sxs-lookup"><span data-stu-id="15fa6-123">**DMTF Reserved** (7..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="15fa6-124">**Fournisseur réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="15fa6-124">**Vendor Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="15fa6-125">**DesiredVLANTrunkEncapsulation**</span><span class="sxs-lookup"><span data-stu-id="15fa6-125">**DesiredVLANTrunkEncapsulation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15fa6-126">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="15fa6-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="15fa6-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="15fa6-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="15fa6-128">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ VLANEndpointCapabilities. SupportsTrunkEncapsulationNegotiation", "**CIM \_ VLANEndpoint**.**OperationalVLANTrunkEncapsulation**","**CIM \_ VLANEndpoint**.**OtherTrunkEncapsulation**")</span><span class="sxs-lookup"><span data-stu-id="15fa6-128">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VLANEndpointCapabilities.SupportsTrunkEncapsulationNegotiation", "**CIM\_VLANEndpoint**.**OperationalVLANTrunkEncapsulation**", "**CIM\_VLANEndpoint**.**OtherTrunkEncapsulation**")</span></span>
</dt> </dl>

<span data-ttu-id="15fa6-129">Type d’encapsulation VLAN demandé.</span><span class="sxs-lookup"><span data-stu-id="15fa6-129">The requested VLAN encapsulation type.</span></span>

> [!Note]  
> <span data-ttu-id="15fa6-130">Cette propriété est utilisée uniquement lorsque le point de terminaison de réseau local virtuel est en mode Trunking.</span><span class="sxs-lookup"><span data-stu-id="15fa6-130">This property is only used when the VLAN endpoint is in trunking mode.</span></span>

 

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="15fa6-131">**DMTF réservé** (0)</span><span class="sxs-lookup"><span data-stu-id="15fa6-131">**DMTF Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="15fa6-132">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="15fa6-132">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="15fa6-133">**Non applicable** (2)</span><span class="sxs-lookup"><span data-stu-id="15fa6-133">**Not Applicable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="802.1q"></span><span id="802.1Q"></span>

<span data-ttu-id="15fa6-134">**802.1 q** (3)</span><span class="sxs-lookup"><span data-stu-id="15fa6-134">**802.1q** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Cisco_ISL"></span><span id="cisco_isl"></span><span id="CISCO_ISL"></span>

<span data-ttu-id="15fa6-135">**Cisco ISL** (4)</span><span class="sxs-lookup"><span data-stu-id="15fa6-135">**Cisco ISL** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>

<span data-ttu-id="15fa6-136">**Négocier** (5)</span><span class="sxs-lookup"><span data-stu-id="15fa6-136">**Negotiate** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="15fa6-137">**DMTF réservé** (6.. 32767)</span><span class="sxs-lookup"><span data-stu-id="15fa6-137">**DMTF Reserved** (6..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="15fa6-138">**Fournisseur réservé** (32768...)</span><span class="sxs-lookup"><span data-stu-id="15fa6-138">**Vendor Reserved** (32768..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="15fa6-139">**GVRPStatus**</span><span class="sxs-lookup"><span data-stu-id="15fa6-139">**GVRPStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15fa6-140">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="15fa6-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="15fa6-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="15fa6-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15fa6-142">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VLANEndpoint**.**OperationalEndpointMode**, CIM \_ VLANEndpointCapabilities. Dot1QTagging ")</span><span class="sxs-lookup"><span data-stu-id="15fa6-142">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VLANEndpoint**.**OperationalEndpointMode**, CIM\_VLANEndpointCapabilities.Dot1QTagging")</span></span>
</dt> </dl>

<span data-ttu-id="15fa6-143">Indique si le protocole GVRP (GARP VLAN Registration Protocol) est activé ou désactivé sur le point de terminaison Trunk.</span><span class="sxs-lookup"><span data-stu-id="15fa6-143">Indicates whether GARP VLAN Registration Protocol (GVRP) is enabled or disabled on the trunk endpoint.</span></span>

> [!Note]  
> <span data-ttu-id="15fa6-144">Cette propriété est utilisée uniquement lorsque le GVRP est pris en charge par le point de terminaison, et le mode Trunking est activé.</span><span class="sxs-lookup"><span data-stu-id="15fa6-144">This property is only used when GVRP is supported by the endpoint, and trunking mode is enabled.</span></span>

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="15fa6-145">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="15fa6-145">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="15fa6-146">**Non applicable** (2)</span><span class="sxs-lookup"><span data-stu-id="15fa6-146">**Not Applicable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="15fa6-147">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="15fa6-147">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="15fa6-148">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="15fa6-148">**Disabled** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="15fa6-149">**OperationalEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="15fa6-149">**OperationalEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15fa6-150">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="15fa6-150">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="15fa6-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="15fa6-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15fa6-152">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VLANEndpoint**.**DesiredEndpointMode**","**CIM \_ VLANEndpoint**.**OtherEndpointMode**")</span><span class="sxs-lookup"><span data-stu-id="15fa6-152">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VLANEndpoint**.**DesiredEndpointMode**", "**CIM\_VLANEndpoint**.**OtherEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="15fa6-153">Mode VLAN actuel pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="15fa6-153">The current VLAN mode for the endpoint.</span></span>

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="15fa6-154">**DMTF réservé** (0)</span><span class="sxs-lookup"><span data-stu-id="15fa6-154">**DMTF Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="15fa6-155">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="15fa6-155">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Access"></span><span id="access"></span><span id="ACCESS"></span>

<span data-ttu-id="15fa6-156">**Accès** (2)</span><span class="sxs-lookup"><span data-stu-id="15fa6-156">**Access** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Dynamic_Auto"></span><span id="dynamic_auto"></span><span id="DYNAMIC_AUTO"></span>

<span data-ttu-id="15fa6-157">**Automatique dynamique** (3)</span><span class="sxs-lookup"><span data-stu-id="15fa6-157">**Dynamic Auto** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Dynamic_Desirable"></span><span id="dynamic_desirable"></span><span id="DYNAMIC_DESIRABLE"></span>

<span data-ttu-id="15fa6-158">**Désirable dynamique** (4)</span><span class="sxs-lookup"><span data-stu-id="15fa6-158">**Dynamic Desirable** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Trunk"></span><span id="trunk"></span><span id="TRUNK"></span>

<span data-ttu-id="15fa6-159">**Trunk** (5)</span><span class="sxs-lookup"><span data-stu-id="15fa6-159">**Trunk** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Dot1Q_Tunnel"></span><span id="dot1q_tunnel"></span><span id="DOT1Q_TUNNEL"></span>

<span data-ttu-id="15fa6-160">**Tunnel Dot1Q** (6)</span><span class="sxs-lookup"><span data-stu-id="15fa6-160">**Dot1Q Tunnel** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="15fa6-161">**DMTF réservé** (7.. 32767)</span><span class="sxs-lookup"><span data-stu-id="15fa6-161">**DMTF Reserved** (7..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="15fa6-162">**Fournisseur réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="15fa6-162">**Vendor Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="15fa6-163">**OperationalVLANTrunkEncapsulation**</span><span class="sxs-lookup"><span data-stu-id="15fa6-163">**OperationalVLANTrunkEncapsulation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15fa6-164">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="15fa6-164">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="15fa6-165">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="15fa6-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15fa6-166">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VLANEndpoint**.**OtherTrunkEncapsulation**","**CIM \_ VLANEndpoint**.**DesiredVLANTrunkEncapsulation**")</span><span class="sxs-lookup"><span data-stu-id="15fa6-166">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VLANEndpoint**.**OtherTrunkEncapsulation**", "**CIM\_VLANEndpoint**.**DesiredVLANTrunkEncapsulation**")</span></span>
</dt> </dl>

<span data-ttu-id="15fa6-167">Type d’encapsulation VLAN actuel.</span><span class="sxs-lookup"><span data-stu-id="15fa6-167">The current VLAN encapsulation type.</span></span>

> [!Note]  
> <span data-ttu-id="15fa6-168">Cette propriété est utilisée uniquement lorsque le point de terminaison de réseau local virtuel est en mode Trunking.</span><span class="sxs-lookup"><span data-stu-id="15fa6-168">This property is only used when the VLAN endpoint is in trunking mode.</span></span>

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="15fa6-169">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="15fa6-169">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="15fa6-170">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="15fa6-170">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="15fa6-171">**Non applicable** (2)</span><span class="sxs-lookup"><span data-stu-id="15fa6-171">**Not Applicable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="802.1q"></span><span id="802.1Q"></span>

<span data-ttu-id="15fa6-172">**802.1 q** (3)</span><span class="sxs-lookup"><span data-stu-id="15fa6-172">**802.1q** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Cisco_ISL"></span><span id="cisco_isl"></span><span id="CISCO_ISL"></span>

<span data-ttu-id="15fa6-173">**Cisco ISL** (4)</span><span class="sxs-lookup"><span data-stu-id="15fa6-173">**Cisco ISL** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Negotiating"></span><span id="negotiating"></span><span id="NEGOTIATING"></span>

<span data-ttu-id="15fa6-174">**Négociation** (5)</span><span class="sxs-lookup"><span data-stu-id="15fa6-174">**Negotiating** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="15fa6-175">**DMTF réservé** (6.. 32767)</span><span class="sxs-lookup"><span data-stu-id="15fa6-175">**DMTF Reserved** (6..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="15fa6-176">**Fournisseur réservé** (32768...)</span><span class="sxs-lookup"><span data-stu-id="15fa6-176">**Vendor Reserved** (32768..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="15fa6-177">**OtherEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="15fa6-177">**OtherEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15fa6-178">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="15fa6-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15fa6-179">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="15fa6-179">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="15fa6-180">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VLANEndpoint**.**DesiredEndpointMode**","**CIM \_ VLANEndpoint**.**OperationalEndpointMode**")</span><span class="sxs-lookup"><span data-stu-id="15fa6-180">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VLANEndpoint**.**DesiredEndpointMode**", "**CIM\_VLANEndpoint**.**OperationalEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="15fa6-181">Type de modèle de point de terminaison VLAN pris en charge par VLANEndpoint lorsque la valeur de **DesiredEndpointMode** est définie sur « 1 » (autre); Sinon, **null**.</span><span class="sxs-lookup"><span data-stu-id="15fa6-181">The type of VLAN endpoint model that is supported by the VLANEndpoint when the value of **DesiredEndpointMode** is set to "1" (other); otherwise, **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="15fa6-182">**OtherTrunkEncapsulation**</span><span class="sxs-lookup"><span data-stu-id="15fa6-182">**OtherTrunkEncapsulation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15fa6-183">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="15fa6-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15fa6-184">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="15fa6-184">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="15fa6-185">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VLANEndpoint**.**DesiredVLANTrunkEncapsulation**","**CIM \_ VLANEndpoint**.**OperationalVLANTrunkEncapsulation**")</span><span class="sxs-lookup"><span data-stu-id="15fa6-185">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VLANEndpoint**.**DesiredVLANTrunkEncapsulation**", "**CIM\_VLANEndpoint**.**OperationalVLANTrunkEncapsulation**")</span></span>
</dt> </dl>

<span data-ttu-id="15fa6-186">Type d’encapsulation VLAN pris en charge par le point de terminaison VLAN lorsque la valeur de la propriété **DesiredVLANTrunkEncapsulation** est définie sur 1 (autre); Sinon, **null**.</span><span class="sxs-lookup"><span data-stu-id="15fa6-186">The type of VLAN encapsulation that is supported by the VLAN endpoint when the value of the **DesiredVLANTrunkEncapsulation** property is set to 1 (other); otherwise, **NULL**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="15fa6-187">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="15fa6-187">Requirements</span></span>



| <span data-ttu-id="15fa6-188">Condition requise</span><span class="sxs-lookup"><span data-stu-id="15fa6-188">Requirement</span></span> | <span data-ttu-id="15fa6-189">Valeur</span><span class="sxs-lookup"><span data-stu-id="15fa6-189">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15fa6-190">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="15fa6-190">Minimum supported client</span></span><br/> | <span data-ttu-id="15fa6-191">Windows 8</span><span class="sxs-lookup"><span data-stu-id="15fa6-191">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="15fa6-192">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="15fa6-192">Minimum supported server</span></span><br/> | <span data-ttu-id="15fa6-193">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="15fa6-193">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="15fa6-194">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="15fa6-194">Namespace</span></span><br/>                | <span data-ttu-id="15fa6-195">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="15fa6-195">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="15fa6-196">MOF</span><span class="sxs-lookup"><span data-stu-id="15fa6-196">MOF</span></span><br/>                      | <dl> <span data-ttu-id="15fa6-197"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="15fa6-197"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="15fa6-198">DLL</span><span class="sxs-lookup"><span data-stu-id="15fa6-198">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15fa6-199"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="15fa6-199"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="15fa6-200">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="15fa6-200">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15fa6-201">**\_PROTOCOLENDPOINT CIM**</span><span class="sxs-lookup"><span data-stu-id="15fa6-201">**CIM\_ProtocolEndpoint**</span></span>](cim-protocolendpoint.md)
</dt> </dl>

 

