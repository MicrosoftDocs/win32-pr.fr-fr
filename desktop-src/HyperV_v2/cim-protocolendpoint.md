---
description: Point de communication utilisé pour envoyer et recevoir des données entre les systèmes, les interfaces d’ordinateur et les réseaux logiques.
ms.assetid: e23ef66b-0bcb-400e-91ff-d6d687d3f0d2
title: Classe CIM_ProtocolEndpoint
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProtocolEndpoint
- CIM_ProtocolEndpoint.Description
- CIM_ProtocolEndpoint.OperationalStatus
- CIM_ProtocolEndpoint.EnabledState
- CIM_ProtocolEndpoint.TimeOfLastStateChange
- CIM_ProtocolEndpoint.Name
- CIM_ProtocolEndpoint.NameFormat
- CIM_ProtocolEndpoint.ProtocolType
- CIM_ProtocolEndpoint.ProtocolIFType
- CIM_ProtocolEndpoint.OtherTypeDescription
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6b3d492c140d443d14583a80985820f55ff9bec8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544268"
---
# <a name="cim_protocolendpoint-class"></a><span data-ttu-id="bc7a4-103">\_Classe PROTOCOLENDPOINT CIM</span><span class="sxs-lookup"><span data-stu-id="bc7a4-103">CIM\_ProtocolEndpoint class</span></span>

<span data-ttu-id="bc7a4-104">Point de communication utilisé pour envoyer et recevoir des données entre les systèmes, les interfaces d’ordinateur et les réseaux logiques.</span><span class="sxs-lookup"><span data-stu-id="bc7a4-104">A communication point used to send and receive data between systems, computer interfaces, and logical networks.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc7a4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bc7a4-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.15.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_ProtocolEndpoint : CIM_ServiceAccessPoint
{
  string   Description;
  uint16   OperationalStatus[];
  uint16   EnabledState;
  datetime TimeOfLastStateChange;
  string   Name;
  string   NameFormat;
  uint16   ProtocolType;
  uint16   ProtocolIFType;
  string   OtherTypeDescription;
};
```

## <a name="members"></a><span data-ttu-id="bc7a4-106">Membres</span><span class="sxs-lookup"><span data-stu-id="bc7a4-106">Members</span></span>

<span data-ttu-id="bc7a4-107">La **classe \_ ProtocolEndpoint CIM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="bc7a4-107">The **CIM\_ProtocolEndpoint** class has these types of members:</span></span>

-   [<span data-ttu-id="bc7a4-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="bc7a4-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bc7a4-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="bc7a4-109">Properties</span></span>

<span data-ttu-id="bc7a4-110">La **classe \_ ProtocolEndpoint CIM** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="bc7a4-110">The **CIM\_ProtocolEndpoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bc7a4-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="bc7a4-111">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc7a4-112">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bc7a4-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc7a4-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bc7a4-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc7a4-114">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| If-MIB. ifDescr ")</span><span class="sxs-lookup"><span data-stu-id="bc7a4-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|IF-MIB.ifDescr")</span></span>
</dt> </dl>

<span data-ttu-id="bc7a4-115">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="bc7a4-115">A textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="bc7a4-116">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="bc7a4-116">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc7a4-117">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bc7a4-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bc7a4-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bc7a4-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc7a4-119">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("EnabledState"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| If-MIB. ifAdminStatus ")</span><span class="sxs-lookup"><span data-stu-id="bc7a4-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("EnabledState"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|IF-MIB.ifAdminStatus")</span></span>
</dt> </dl>

<span data-ttu-id="bc7a4-120">État activé d’un élément.</span><span class="sxs-lookup"><span data-stu-id="bc7a4-120">The enabled state of an element.</span></span>

</dd> <dt>

<span data-ttu-id="bc7a4-121">**Nom**</span><span class="sxs-lookup"><span data-stu-id="bc7a4-121">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc7a4-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bc7a4-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc7a4-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bc7a4-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc7a4-124">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-124">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="bc7a4-125">Identificateur unique du point de terminaison de protocole qui indique la fonctionnalité managée.</span><span class="sxs-lookup"><span data-stu-id="bc7a4-125">A unique identifier of the protocol endpoint that indicates the managed functionality.</span></span> <span data-ttu-id="bc7a4-126">La Convention d’affectation de noms pour cette propriété est définie dans la propriété **NameFormat** .</span><span class="sxs-lookup"><span data-stu-id="bc7a4-126">The naming convention for this property is defined in the **NameFormat** property.</span></span>

</dd> <dt>

<span data-ttu-id="bc7a4-127">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="bc7a4-127">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc7a4-128">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bc7a4-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc7a4-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bc7a4-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc7a4-130">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-130">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="bc7a4-131">Convention d’affectation de noms utilisée par la propriété **Name** pour garantir l’unicité des valeurs de **nom** .</span><span class="sxs-lookup"><span data-stu-id="bc7a4-131">The naming convention used by the **Name** property to ensure that **Name** values are unique.</span></span> <span data-ttu-id="bc7a4-132">Par exemple, vous pouvez ajouter la valeur de la propriété **ProtocolIFType** au début du nom, suivi d’un trait de soulignement.</span><span class="sxs-lookup"><span data-stu-id="bc7a4-132">For example, you can append the **ProtocolIFType** property value to the beginning of the name followed by an underscore.</span></span>

</dd> <dt>

<span data-ttu-id="bc7a4-133">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="bc7a4-133">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc7a4-134">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bc7a4-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="bc7a4-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bc7a4-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc7a4-136">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("OperationalStatus"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| If-MIB. ifOperStatus ")</span><span class="sxs-lookup"><span data-stu-id="bc7a4-136">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("OperationalStatus"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|IF-MIB.ifOperStatus")</span></span>
</dt> </dl>

<span data-ttu-id="bc7a4-137">Tableau qui contient l’état actuel de l’élément.</span><span class="sxs-lookup"><span data-stu-id="bc7a4-137">An array that contains the current status of the element.</span></span> <span data-ttu-id="bc7a4-138">La première valeur du tableau **OperationalStatus** doit contenir l’état principal de l’élément.</span><span class="sxs-lookup"><span data-stu-id="bc7a4-138">The first value of the **OperationalStatus** array should contain the primary status for the element.</span></span>

</dd> <dt>

<span data-ttu-id="bc7a4-139">**OtherTypeDescription**</span><span class="sxs-lookup"><span data-stu-id="bc7a4-139">**OtherTypeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc7a4-140">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bc7a4-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc7a4-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bc7a4-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc7a4-142">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ ProtocolEndpoint CIM**.**ProtocolType**« , »**CIM \_ ProtocolEndpoint**.**ProtocolIFType**")</span><span class="sxs-lookup"><span data-stu-id="bc7a4-142">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ProtocolEndpoint**.**ProtocolType**", "**CIM\_ProtocolEndpoint**.**ProtocolIFType**")</span></span>
</dt> </dl>

<span data-ttu-id="bc7a4-143">Description d’un type de protocole réseau qui est utilisé lorsque la propriété **ProtocolIFType** est définie sur « 1 » (autre); dans le cas contraire, cette valeur doit être définie sur null.</span><span class="sxs-lookup"><span data-stu-id="bc7a4-143">A description of a network protocol type that is used when the **ProtocolIFType** property is set to "1" (Other); otherwise, this value should be set to null.</span></span>

</dd> <dt>

<span data-ttu-id="bc7a4-144">**ProtocolIFType**</span><span class="sxs-lookup"><span data-stu-id="bc7a4-144">**ProtocolIFType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc7a4-145">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bc7a4-145">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bc7a4-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bc7a4-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc7a4-147">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| If-MIB. ifType "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ ProtocolEndpoint CIM**.**OtherTypeDescription**")</span><span class="sxs-lookup"><span data-stu-id="bc7a4-147">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|IF-MIB.ifType"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ProtocolEndpoint**.**OtherTypeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="bc7a4-148">Énumération utilisée pour classer et classer différentes instances de cette classe.</span><span class="sxs-lookup"><span data-stu-id="bc7a4-148">An enumeration used to categorize and classify different instances of this class.</span></span> <span data-ttu-id="bc7a4-149">Les valeurs possibles de cette propriété sont synchronisées avec l’IANA (Internet Assigned Numbers Authority) ifType (Management Information base), qui est conservée dans https://www.iana.org/assignments/ianaiftype-mib .</span><span class="sxs-lookup"><span data-stu-id="bc7a4-149">The possible values for this property are synchronized with the Internet Assigned Numbers Authority (IANA) ifType MIB-module (management information base), which is maintained at https://www.iana.org/assignments/ianaiftype-mib.</span></span> <span data-ttu-id="bc7a4-150">Des valeurs supplémentaires définies par le DMTF sont incluses.</span><span class="sxs-lookup"><span data-stu-id="bc7a4-150">Additional values defined by the DMTF are included.</span></span>

> [!Note]  
> <span data-ttu-id="bc7a4-151">Si **ProtocolIFType** a la valeur 1 (autre), les informations sur le type de protocole doivent être fournies dans la propriété **OtherTypeDescription** .</span><span class="sxs-lookup"><span data-stu-id="bc7a4-151">If the **ProtocolIFType** is set to 1 (Other), then the protocol type information should be provided in the **OtherTypeDescription** property.</span></span>

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bc7a4-152">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-152">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="bc7a4-153">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-153">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Regular_1822"></span><span id="regular_1822"></span><span id="REGULAR_1822"></span>

<span data-ttu-id="bc7a4-154">**Normal 1822** (2)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-154">**Regular 1822** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="HDH_1822"></span><span id="hdh_1822"></span>

<span data-ttu-id="bc7a4-155">**HDH 1822** (3)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-155">**HDH 1822** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DDN_X.25"></span><span id="ddn_x.25"></span>

<span data-ttu-id="bc7a4-156">**DDN X. 25** (4)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-156">**DDN X.25** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="RFC877_X.25"></span><span id="rfc877_x.25"></span>

<span data-ttu-id="bc7a4-157">**RFC877 X. 25** (5)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-157">**RFC877 X.25** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_CSMA_CD"></span><span id="ethernet_csma_cd"></span><span id="ETHERNET_CSMA_CD"></span>

<span data-ttu-id="bc7a4-158">**Ethernet CSMA/CD** (6)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-158">**Ethernet CSMA/CD** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO_802.3_CSMA_CD"></span><span id="iso_802.3_csma_cd"></span>

<span data-ttu-id="bc7a4-159">**ISO 802,3 CSMA/CD** (7)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-159">**ISO 802.3 CSMA/CD** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO_802.4_Token_Bus"></span><span id="iso_802.4_token_bus"></span><span id="ISO_802.4_TOKEN_BUS"></span>

<span data-ttu-id="bc7a4-160">**Bus de jetons ISO 802,4** (8)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-160">**ISO 802.4 Token Bus** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO_802.5_Token_Ring"></span><span id="iso_802.5_token_ring"></span><span id="ISO_802.5_TOKEN_RING"></span>

<span data-ttu-id="bc7a4-161">**Token Ring ISO 802,5** (9)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-161">**ISO 802.5 Token Ring** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO_802.6_MAN"></span><span id="iso_802.6_man"></span>

<span data-ttu-id="bc7a4-162">**ISO 802,6 Man** (10)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-162">**ISO 802.6 MAN** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="StarLAN"></span><span id="starlan"></span><span id="STARLAN"></span>

<span data-ttu-id="bc7a4-163">**Starlan** (11)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-163">**StarLAN** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Proteon_10Mbit"></span><span id="proteon_10mbit"></span><span id="PROTEON_10MBIT"></span>

<span data-ttu-id="bc7a4-164">**Proteon 10Mbit** (12)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-164">**Proteon 10Mbit** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Proteon_80Mbit"></span><span id="proteon_80mbit"></span><span id="PROTEON_80MBIT"></span>

<span data-ttu-id="bc7a4-165">**Proteon 80Mbit** (13)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-165">**Proteon 80Mbit** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="HyperChannel"></span><span id="hyperchannel"></span><span id="HYPERCHANNEL"></span>

<span data-ttu-id="bc7a4-166">**Hyperchannel** (14)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-166">**HyperChannel** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="FDDI"></span><span id="fddi"></span>

<span data-ttu-id="bc7a4-167">**FDDI** (15)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-167">**FDDI** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="LAP-B"></span><span id="lap-b"></span>

<span data-ttu-id="bc7a4-168">**Lap-B** (16)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-168">**LAP-B** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="SDLC"></span><span id="sdlc"></span>

<span data-ttu-id="bc7a4-169">**SDLC** (17)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-169">**SDLC** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="DS1"></span><span id="ds1"></span>

<span data-ttu-id="bc7a4-170">**DS1** (18)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-170">**DS1** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="E1"></span><span id="e1"></span>

<span data-ttu-id="bc7a4-171">**E1** (19)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-171">**E1** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Basic_ISDN"></span><span id="basic_isdn"></span><span id="BASIC_ISDN"></span>

<span data-ttu-id="bc7a4-172">**RNIS de base** (20)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-172">**Basic ISDN** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Primary_ISDN"></span><span id="primary_isdn"></span><span id="PRIMARY_ISDN"></span>

<span data-ttu-id="bc7a4-173">**RNIS principal** (21)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-173">**Primary ISDN** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_Point-to-Point_Serial"></span><span id="proprietary_point-to-point_serial"></span><span id="PROPRIETARY_POINT-TO-POINT_SERIAL"></span>

<span data-ttu-id="bc7a4-174">**Série point à point propriétaire** (22)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-174">**Proprietary Point-to-Point Serial** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="PPP"></span><span id="ppp"></span>

<span data-ttu-id="bc7a4-175">**PPP** (23)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-175">**PPP** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Loopback"></span><span id="software_loopback"></span><span id="SOFTWARE_LOOPBACK"></span>

<span data-ttu-id="bc7a4-176">**Bouclage logiciel** (24)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-176">**Software Loopback** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="EON"></span><span id="eon"></span>

<span data-ttu-id="bc7a4-177">**EON** (25)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-177">**EON** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_3Mbit"></span><span id="ethernet_3mbit"></span><span id="ETHERNET_3MBIT"></span>

<span data-ttu-id="bc7a4-178">**3Mbit Ethernet** (26)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-178">**Ethernet 3Mbit** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="NSIP"></span><span id="nsip"></span>

<span data-ttu-id="bc7a4-179">**NSIP** (27)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-179">**NSIP** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="SLIP"></span><span id="slip"></span>

<span data-ttu-id="bc7a4-180">**Slip** (28)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-180">**SLIP** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Ultra"></span><span id="ultra"></span><span id="ULTRA"></span>

<span data-ttu-id="bc7a4-181">**Ultra** (29)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-181">**Ultra** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="DS3"></span><span id="ds3"></span>

<span data-ttu-id="bc7a4-182">**DS3** (30)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-182">**DS3** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="SIP"></span><span id="sip"></span>

<span data-ttu-id="bc7a4-183">**SIP** (31)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-183">**SIP** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>

<span data-ttu-id="bc7a4-184">**Relais de trames** (32)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-184">**Frame Relay** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-232"></span><span id="rs-232"></span>

<span data-ttu-id="bc7a4-185">**RS-232** (33)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-185">**RS-232** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel"></span><span id="parallel"></span><span id="PARALLEL"></span>

<span data-ttu-id="bc7a4-186">**Parallèle** (34)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-186">**Parallel** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="ARCNet"></span><span id="arcnet"></span><span id="ARCNET"></span>

<span data-ttu-id="bc7a4-187">**Arcnet** (35)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-187">**ARCNet** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ARCNet_Plus"></span><span id="arcnet_plus"></span><span id="ARCNET_PLUS"></span>

<span data-ttu-id="bc7a4-188">**Arcnet plus** (36)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-188">**ARCNet Plus** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="ATM"></span><span id="atm"></span>

<span data-ttu-id="bc7a4-189">**ATM** (37)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-189">**ATM** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="MIO_X.25"></span><span id="mio_x.25"></span>

<span data-ttu-id="bc7a4-190">**Mio X. 25** (38)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-190">**MIO X.25** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="SONET"></span><span id="sonet"></span>

<span data-ttu-id="bc7a4-191">**SONET** (39)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-191">**SONET** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="X.25_PLE"></span><span id="x.25_ple"></span>

<span data-ttu-id="bc7a4-192">**X. 25 espérance** de la (40)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-192">**X.25 PLE** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO_802.211c"></span><span id="iso_802.211c"></span><span id="ISO_802.211C"></span>

<span data-ttu-id="bc7a4-193">**ISO 802.211 c** (41)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-193">**ISO 802.211c** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="LocalTalk"></span><span id="localtalk"></span><span id="LOCALTALK"></span>

<span data-ttu-id="bc7a4-194">**LocalTalk** (42)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-194">**LocalTalk** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="SMDS_DXI"></span><span id="smds_dxi"></span>

<span data-ttu-id="bc7a4-195">**SMDS DXi** (43)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-195">**SMDS DXI** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="Frame_Relay_Service"></span><span id="frame_relay_service"></span><span id="FRAME_RELAY_SERVICE"></span>

<span data-ttu-id="bc7a4-196">**Service Frame Relay** (44)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-196">**Frame Relay Service** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="V.35"></span><span id="v.35"></span>

<span data-ttu-id="bc7a4-197">**V. 35** (45)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-197">**V.35** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="HSSI"></span><span id="hssi"></span>

<span data-ttu-id="bc7a4-198">**HSSI** (46)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-198">**HSSI** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="bc7a4-199">**HIPPA** (47)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-199">**HIPPI** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="Modem"></span><span id="modem"></span><span id="MODEM"></span>

<span data-ttu-id="bc7a4-200">**Modem** (48)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-200">**Modem** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="AAL5"></span><span id="aal5"></span>

<span data-ttu-id="bc7a4-201">**AAL5** (49)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-201">**AAL5** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="SONET_Path"></span><span id="sonet_path"></span><span id="SONET_PATH"></span>

<span data-ttu-id="bc7a4-202">**Chemin d’accès SONET** (50)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-202">**SONET Path** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="SONET_VT"></span><span id="sonet_vt"></span>

<span data-ttu-id="bc7a4-203">**SONET VT** (51)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-203">**SONET VT** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="SMDS_ICIP"></span><span id="smds_icip"></span>

<span data-ttu-id="bc7a4-204">**SMDS ICIP** (52)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-204">**SMDS ICIP** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_Virtual_Internal"></span><span id="proprietary_virtual_internal"></span><span id="PROPRIETARY_VIRTUAL_INTERNAL"></span>

<span data-ttu-id="bc7a4-205">**Propriétaire virtuel/interne** (53)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-205">**Proprietary Virtual/Internal** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_Multiplexor"></span><span id="proprietary_multiplexor"></span><span id="PROPRIETARY_MULTIPLEXOR"></span>

<span data-ttu-id="bc7a4-206">**Multiplexeur propriétaire** (54)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-206">**Proprietary Multiplexor** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.12"></span><span id="ieee_802.12"></span>

<span data-ttu-id="bc7a4-207">**IEEE 802,12** (55)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-207">**IEEE 802.12** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="Fibre_Channel"></span><span id="fibre_channel"></span><span id="FIBRE_CHANNEL"></span>

<span data-ttu-id="bc7a4-208">**Fibre Channel** (56)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-208">**Fibre Channel** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI_Interface"></span><span id="hippi_interface"></span><span id="HIPPI_INTERFACE"></span>

<span data-ttu-id="bc7a4-209">**Interface HIPPA** (57)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-209">**HIPPI Interface** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Frame_Relay_Interconnect"></span><span id="frame_relay_interconnect"></span><span id="FRAME_RELAY_INTERCONNECT"></span>

<span data-ttu-id="bc7a4-210">**Interconnexion du relais de trames** (58)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-210">**Frame Relay Interconnect** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="ATM_Emulated_LAN_for_802.3"></span><span id="atm_emulated_lan_for_802.3"></span><span id="ATM_EMULATED_LAN_FOR_802.3"></span>

<span data-ttu-id="bc7a4-211">**Réseau local émulé ATM pour 802,3** (59)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-211">**ATM Emulated LAN for 802.3** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="ATM_Emulated_LAN_for_802.5"></span><span id="atm_emulated_lan_for_802.5"></span><span id="ATM_EMULATED_LAN_FOR_802.5"></span>

<span data-ttu-id="bc7a4-212">**Réseau local émulé ATM pour 802,5** (60)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-212">**ATM Emulated LAN for 802.5** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="ATM_Emulated_Circuit"></span><span id="atm_emulated_circuit"></span><span id="ATM_EMULATED_CIRCUIT"></span>

<span data-ttu-id="bc7a4-213">**Circuit émulé ATM** (61)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-213">**ATM Emulated Circuit** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="Fast_Ethernet__100BaseT_"></span><span id="fast_ethernet__100baset_"></span><span id="FAST_ETHERNET__100BASET_"></span>

<span data-ttu-id="bc7a4-214">**Fast Ethernet (100BaseT)** (62)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-214">**Fast Ethernet (100BaseT)** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="ISDN"></span><span id="isdn"></span>

<span data-ttu-id="bc7a4-215">**RNIS** (63)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-215">**ISDN** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="V.11"></span><span id="v.11"></span>

<span data-ttu-id="bc7a4-216">**V. 11** (64)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-216">**V.11** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="V.36"></span><span id="v.36"></span>

<span data-ttu-id="bc7a4-217">**V. 36** (65)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-217">**V.36** (65)</span></span>


</dt> <dd></dd> <dt>

<span id="G703_at_64K"></span><span id="g703_at_64k"></span><span id="G703_AT_64K"></span>

<span data-ttu-id="bc7a4-218">**G703 à 64 Ko** (66)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-218">**G703 at 64K** (66)</span></span>


</dt> <dd></dd> <dt>

<span id="G703_at_2Mb"></span><span id="g703_at_2mb"></span><span id="G703_AT_2MB"></span>

<span data-ttu-id="bc7a4-219">**G703 à 2 Mo** (67)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-219">**G703 at 2Mb** (67)</span></span>


</dt> <dd></dd> <dt>

<span id="QLLC"></span><span id="qllc"></span>

<span data-ttu-id="bc7a4-220">**QLLC** (68)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-220">**QLLC** (68)</span></span>


</dt> <dd></dd> <dt>

<span id="Fast_Ethernet_100BaseFX"></span><span id="fast_ethernet_100basefx"></span><span id="FAST_ETHERNET_100BASEFX"></span>

<span data-ttu-id="bc7a4-221">**Fast Ethernet 100BaseFX** (69)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-221">**Fast Ethernet 100BaseFX** (69)</span></span>


</dt> <dd></dd> <dt>

<span id="Channel"></span><span id="channel"></span><span id="CHANNEL"></span>

<span data-ttu-id="bc7a4-222">**Canal** (70)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-222">**Channel** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.11"></span><span id="ieee_802.11"></span>

<span data-ttu-id="bc7a4-223">**IEEE 802,11** (71)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-223">**IEEE 802.11** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="IBM_260_370_OEMI_Channel"></span><span id="ibm_260_370_oemi_channel"></span><span id="IBM_260_370_OEMI_CHANNEL"></span>

<span data-ttu-id="bc7a4-224">**Canal IBM 260/370 OEMI** (72)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-224">**IBM 260/370 OEMI Channel** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="bc7a4-225">**ESCON** (73)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-225">**ESCON** (73)</span></span>


</dt> <dd></dd> <dt>

<span id="Data_Link_Switching"></span><span id="data_link_switching"></span><span id="DATA_LINK_SWITCHING"></span>

<span data-ttu-id="bc7a4-226">**Commutation des liaisons de données** (74)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-226">**Data Link Switching** (74)</span></span>


</dt> <dd></dd> <dt>

<span id="ISDN_S_T_Interface"></span><span id="isdn_s_t_interface"></span><span id="ISDN_S_T_INTERFACE"></span>

<span data-ttu-id="bc7a4-227">**Interface RNIS S/T** (75)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-227">**ISDN S/T Interface** (75)</span></span>


</dt> <dd></dd> <dt>

<span id="ISDN_U_Interface"></span><span id="isdn_u_interface"></span><span id="ISDN_U_INTERFACE"></span>

<span data-ttu-id="bc7a4-228">**Interface RNIS U** (76)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-228">**ISDN U Interface** (76)</span></span>


</dt> <dd></dd> <dt>

<span id="LAP-D"></span><span id="lap-d"></span>

<span data-ttu-id="bc7a4-229">**Lap-D** (77)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-229">**LAP-D** (77)</span></span>


</dt> <dd></dd> <dt>

<span id="IP_Switch"></span><span id="ip_switch"></span><span id="IP_SWITCH"></span>

<span data-ttu-id="bc7a4-230">**Commutateur IP** (78)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-230">**IP Switch** (78)</span></span>


</dt> <dd></dd> <dt>

<span id="Remote_Source_Route_Bridging"></span><span id="remote_source_route_bridging"></span><span id="REMOTE_SOURCE_ROUTE_BRIDGING"></span>

<span data-ttu-id="bc7a4-231">**Pontage d’itinéraires source distants** (79)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-231">**Remote Source Route Bridging** (79)</span></span>


</dt> <dd></dd> <dt>

<span id="ATM_Logical"></span><span id="atm_logical"></span><span id="ATM_LOGICAL"></span>

<span data-ttu-id="bc7a4-232">**ATM logique** (80)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-232">**ATM Logical** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="DS0"></span><span id="ds0"></span>

<span data-ttu-id="bc7a4-233">**DS0** (81)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-233">**DS0** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="DS0_Bundle"></span><span id="ds0_bundle"></span><span id="DS0_BUNDLE"></span>

<span data-ttu-id="bc7a4-234">**Bundle DS0** (82)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-234">**DS0 Bundle** (82)</span></span>


</dt> <dd></dd> <dt>

<span id="BSC"></span><span id="bsc"></span>

<span data-ttu-id="bc7a4-235">**BSC** (83)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-235">**BSC** (83)</span></span>


</dt> <dd></dd> <dt>

<span id="Async"></span><span id="async"></span><span id="ASYNC"></span>

<span data-ttu-id="bc7a4-236">**Async** (84)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-236">**Async** (84)</span></span>


</dt> <dd></dd> <dt>

<span id="Combat_Net_Radio"></span><span id="combat_net_radio"></span><span id="COMBAT_NET_RADIO"></span>

<span data-ttu-id="bc7a4-237">**Radio combat net** (85)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-237">**Combat Net Radio** (85)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO_802.5r_DTR"></span><span id="iso_802.5r_dtr"></span><span id="ISO_802.5R_DTR"></span>

<span data-ttu-id="bc7a4-238">**ISO 802.5 r DTR** (86)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-238">**ISO 802.5r DTR** (86)</span></span>


</dt> <dd></dd> <dt>

<span id="Ext_Pos_Loc_Report_System"></span><span id="ext_pos_loc_report_system"></span><span id="EXT_POS_LOC_REPORT_SYSTEM"></span>

<span data-ttu-id="bc7a4-239">**Système de rapports ext POS Loc** (87)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-239">**Ext Pos Loc Report System** (87)</span></span>


</dt> <dd></dd> <dt>

<span id="AppleTalk_Remote_Access_Protocol"></span><span id="appletalk_remote_access_protocol"></span><span id="APPLETALK_REMOTE_ACCESS_PROTOCOL"></span>

<span data-ttu-id="bc7a4-240">**Protocole d’accès à distance AppleTalk** (88)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-240">**AppleTalk Remote Access Protocol** (88)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_Connectionless"></span><span id="proprietary_connectionless"></span><span id="PROPRIETARY_CONNECTIONLESS"></span>

<span data-ttu-id="bc7a4-241">**Propriétaire sans connexion** (89)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-241">**Proprietary Connectionless** (89)</span></span>


</dt> <dd></dd> <dt>

<span id="ITU_X.29_Host_PAD"></span><span id="itu_x.29_host_pad"></span><span id="ITU_X.29_HOST_PAD"></span>

<span data-ttu-id="bc7a4-242">**Bloc-notes de l’hôte ITU X. 29** (90)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-242">**ITU X.29 Host PAD** (90)</span></span>


</dt> <dd></dd> <dt>

<span id="ITU_X.3_Terminal_PAD"></span><span id="itu_x.3_terminal_pad"></span><span id="ITU_X.3_TERMINAL_PAD"></span>

<span data-ttu-id="bc7a4-243">**Boîtier terminal ITU X. 3** (91)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-243">**ITU X.3 Terminal PAD** (91)</span></span>


</dt> <dd></dd> <dt>

<span id="Frame_Relay_MPI"></span><span id="frame_relay_mpi"></span><span id="FRAME_RELAY_MPI"></span>

<span data-ttu-id="bc7a4-244">**MPI de relais de trames** (92)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-244">**Frame Relay MPI** (92)</span></span>


</dt> <dd></dd> <dt>

<span id="ITU_X.213"></span><span id="itu_x.213"></span>

<span data-ttu-id="bc7a4-245">**ITU X. 213** (93)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-245">**ITU X.213** (93)</span></span>


</dt> <dd></dd> <dt>

<span id="ADSL"></span><span id="adsl"></span>

<span data-ttu-id="bc7a4-246">**ADSL** (94)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-246">**ADSL** (94)</span></span>


</dt> <dd></dd> <dt>

<span id="RADSL"></span><span id="radsl"></span>

<span data-ttu-id="bc7a4-247">**RADSL** (95)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-247">**RADSL** (95)</span></span>


</dt> <dd></dd> <dt>

<span id="SDSL"></span><span id="sdsl"></span>

<span data-ttu-id="bc7a4-248">**SDSL** (96)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-248">**SDSL** (96)</span></span>


</dt> <dd></dd> <dt>

<span id="VDSL"></span><span id="vdsl"></span>

<span data-ttu-id="bc7a4-249">**VDSL** (97)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-249">**VDSL** (97)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO_802.5_CRFP"></span><span id="iso_802.5_crfp"></span>

<span data-ttu-id="bc7a4-250">**ISO 802,5 CRFP** (98)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-250">**ISO 802.5 CRFP** (98)</span></span>


</dt> <dd></dd> <dt>

<span id="Myrinet"></span><span id="myrinet"></span><span id="MYRINET"></span>

<span data-ttu-id="bc7a4-251">**Myrinet** (99)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-251">**Myrinet** (99)</span></span>


</dt> <dd></dd> <dt>

<span id="Voice_Receive_and_Transmit"></span><span id="voice_receive_and_transmit"></span><span id="VOICE_RECEIVE_AND_TRANSMIT"></span>

<span data-ttu-id="bc7a4-252">**Réception et transmission vocales** (100)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-252">**Voice Receive and Transmit** (100)</span></span>


</dt> <dd></dd> <dt>

<span id="Voice_Foreign_Exchange_Office"></span><span id="voice_foreign_exchange_office"></span><span id="VOICE_FOREIGN_EXCHANGE_OFFICE"></span>

<span data-ttu-id="bc7a4-253">**Bureau étranger** à la voix (101)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-253">**Voice Foreign Exchange Office** (101)</span></span>


</dt> <dd></dd> <dt>

<span id="Voice_Foreign_Exchange_Service"></span><span id="voice_foreign_exchange_service"></span><span id="VOICE_FOREIGN_EXCHANGE_SERVICE"></span>

<span data-ttu-id="bc7a4-254">**Service d’échange étranger vocal** (102)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-254">**Voice Foreign Exchange Service** (102)</span></span>


</dt> <dd></dd> <dt>

<span id="Voice_Encapsulation"></span><span id="voice_encapsulation"></span><span id="VOICE_ENCAPSULATION"></span>

<span data-ttu-id="bc7a4-255">**Encapsulation vocale** (103)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-255">**Voice Encapsulation** (103)</span></span>


</dt> <dd></dd> <dt>

<span id="Voice_over_IP"></span><span id="voice_over_ip"></span><span id="VOICE_OVER_IP"></span>

<span data-ttu-id="bc7a4-256">**Voix sur IP** (104)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-256">**Voice over IP** (104)</span></span>


</dt> <dd></dd> <dt>

<span id="ATM_DXI"></span><span id="atm_dxi"></span>

<span data-ttu-id="bc7a4-257">**DXi ATM** (105)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-257">**ATM DXI** (105)</span></span>


</dt> <dd></dd> <dt>

<span id="ATM_FUNI"></span><span id="atm_funi"></span>

<span data-ttu-id="bc7a4-258">**FUNI ATM** (106)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-258">**ATM FUNI** (106)</span></span>


</dt> <dd></dd> <dt>

<span id="ATM_IMA"></span><span id="atm_ima"></span>

<span data-ttu-id="bc7a4-259">**Certificat IMA ATM** (107)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-259">**ATM IMA** (107)</span></span>


</dt> <dd></dd> <dt>

<span id="PPP_Multilink_Bundle"></span><span id="ppp_multilink_bundle"></span><span id="PPP_MULTILINK_BUNDLE"></span>

<span data-ttu-id="bc7a4-260">**Bundle à liaisons multiples PPP** (108)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-260">**PPP Multilink Bundle** (108)</span></span>


</dt> <dd></dd> <dt>

<span id="IP_over_CDLC"></span><span id="ip_over_cdlc"></span><span id="IP_OVER_CDLC"></span>

<span data-ttu-id="bc7a4-261">**IP sur CDLC** (109)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-261">**IP over CDLC** (109)</span></span>


</dt> <dd></dd> <dt>

<span id="IP_over_CLAW"></span><span id="ip_over_claw"></span><span id="IP_OVER_CLAW"></span>

<span data-ttu-id="bc7a4-262">**IP sur la griffe** (110)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-262">**IP over CLAW** (110)</span></span>


</dt> <dd></dd> <dt>

<span id="Stack_to_Stack"></span><span id="stack_to_stack"></span><span id="STACK_TO_STACK"></span>

<span data-ttu-id="bc7a4-263">**Pile à pile** (111)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-263">**Stack to Stack** (111)</span></span>


</dt> <dd></dd> <dt>

<span id="Virtual_IP_Address"></span><span id="virtual_ip_address"></span><span id="VIRTUAL_IP_ADDRESS"></span>

<span data-ttu-id="bc7a4-264">**Adresse IP virtuelle** (112)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-264">**Virtual IP Address** (112)</span></span>


</dt> <dd></dd> <dt>

<span id="MPC"></span><span id="mpc"></span>

<span data-ttu-id="bc7a4-265">**MPC** (113)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-265">**MPC** (113)</span></span>


</dt> <dd></dd> <dt>

<span id="IP_over_ATM"></span><span id="ip_over_atm"></span><span id="IP_OVER_ATM"></span>

<span data-ttu-id="bc7a4-266">**IP sur ATM** (114)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-266">**IP over ATM** (114)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO_802.5j_Fibre_Token_Ring"></span><span id="iso_802.5j_fibre_token_ring"></span><span id="ISO_802.5J_FIBRE_TOKEN_RING"></span>

<span data-ttu-id="bc7a4-267">Carte **Token Ring ISO 802.5 j** (115)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-267">**ISO 802.5j Fibre Token Ring** (115)</span></span>


</dt> <dd></dd> <dt>

<span id="TDLC"></span><span id="tdlc"></span>

<span data-ttu-id="bc7a4-268">**TDLC** (116)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-268">**TDLC** (116)</span></span>


</dt> <dd></dd> <dt>

<span id="Gigabit_Ethernet"></span><span id="gigabit_ethernet"></span><span id="GIGABIT_ETHERNET"></span>

<span data-ttu-id="bc7a4-269">**Gigabit Ethernet** (117)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-269">**Gigabit Ethernet** (117)</span></span>


</dt> <dd></dd> <dt>

<span id="HDLC"></span><span id="hdlc"></span>

<span data-ttu-id="bc7a4-270">**HDLC** (118)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-270">**HDLC** (118)</span></span>


</dt> <dd></dd> <dt>

<span id="LAP-F"></span><span id="lap-f"></span>

<span data-ttu-id="bc7a4-271">**Lap-F** (119)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-271">**LAP-F** (119)</span></span>


</dt> <dd></dd> <dt>

<span id="V.37"></span><span id="v.37"></span>

<span data-ttu-id="bc7a4-272">**V. 37** (120)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-272">**V.37** (120)</span></span>


</dt> <dd></dd> <dt>

<span id="X.25_MLP"></span><span id="x.25_mlp"></span>

<span data-ttu-id="bc7a4-273">**MLP de X. 25** (121)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-273">**X.25 MLP** (121)</span></span>


</dt> <dd></dd> <dt>

<span id="X.25_Hunt_Group"></span><span id="x.25_hunt_group"></span><span id="X.25_HUNT_GROUP"></span>

<span data-ttu-id="bc7a4-274">**X. 25 groupe de recherche** (122)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-274">**X.25 Hunt Group** (122)</span></span>


</dt> <dd></dd> <dt>

<span id="Transp_HDLC"></span><span id="transp_hdlc"></span><span id="TRANSP_HDLC"></span>

<span data-ttu-id="bc7a4-275">**Domaine HDLC** (123)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-275">**Transp HDLC** (123)</span></span>


</dt> <dd></dd> <dt>

<span id="Interleave_Channel"></span><span id="interleave_channel"></span><span id="INTERLEAVE_CHANNEL"></span>

<span data-ttu-id="bc7a4-276">**Canal entrelacé** (124)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-276">**Interleave Channel** (124)</span></span>


</dt> <dd></dd> <dt>

<span id="FAST_Channel"></span><span id="fast_channel"></span><span id="FAST_CHANNEL"></span>

<span data-ttu-id="bc7a4-277">**Canal rapide** (125)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-277">**FAST Channel** (125)</span></span>


</dt> <dd></dd> <dt>

<span id="IP__for_APPN_HPR_in_IP_Networks_"></span><span id="ip__for_appn_hpr_in_ip_networks_"></span><span id="IP__FOR_APPN_HPR_IN_IP_NETWORKS_"></span>

<span data-ttu-id="bc7a4-278">**IP (pour APPN HPR dans les réseaux IP)** (126)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-278">**IP (for APPN HPR in IP Networks)** (126)</span></span>


</dt> <dd></dd> <dt>

<span id="CATV_MAC_Layer"></span><span id="catv_mac_layer"></span><span id="CATV_MAC_LAYER"></span>

<span data-ttu-id="bc7a4-279">**Couche MAC CATV** (127)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-279">**CATV MAC Layer** (127)</span></span>


</dt> <dd></dd> <dt>

<span id="CATV_Downstream"></span><span id="catv_downstream"></span><span id="CATV_DOWNSTREAM"></span>

<span data-ttu-id="bc7a4-280">**CATV en aval** (128)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-280">**CATV Downstream** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="CATV_Upstream"></span><span id="catv_upstream"></span><span id="CATV_UPSTREAM"></span>

<span data-ttu-id="bc7a4-281">**CATV en amont** (129)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-281">**CATV Upstream** (129)</span></span>


</dt> <dd></dd> <dt>

<span id="Avalon_12MPP_Switch"></span><span id="avalon_12mpp_switch"></span><span id="AVALON_12MPP_SWITCH"></span>

<span data-ttu-id="bc7a4-282">**Commutateur 12MPP de Avalon** (130)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-282">**Avalon 12MPP Switch** (130)</span></span>


</dt> <dd></dd> <dt>

<span id="Tunnel"></span><span id="tunnel"></span><span id="TUNNEL"></span>

<span data-ttu-id="bc7a4-283">**Tunnel** (131)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-283">**Tunnel** (131)</span></span>


</dt> <dd></dd> <dt>

<span id="Coffee"></span><span id="coffee"></span><span id="COFFEE"></span>

<span data-ttu-id="bc7a4-284">**Café** (132)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-284">**Coffee** (132)</span></span>


</dt> <dd></dd> <dt>

<span id="Circuit_Emulation_Service"></span><span id="circuit_emulation_service"></span><span id="CIRCUIT_EMULATION_SERVICE"></span>

<span data-ttu-id="bc7a4-285">**Service d’émulation de circuit** (133)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-285">**Circuit Emulation Service** (133)</span></span>


</dt> <dd></dd> <dt>

<span id="ATM_SubInterface"></span><span id="atm_subinterface"></span><span id="ATM_SUBINTERFACE"></span>

<span data-ttu-id="bc7a4-286">Sous- **interface ATM** (134)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-286">**ATM SubInterface** (134)</span></span>


</dt> <dd></dd> <dt>

<span id="Layer_2_VLAN_using_802.1Q"></span><span id="layer_2_vlan_using_802.1q"></span><span id="LAYER_2_VLAN_USING_802.1Q"></span>

<span data-ttu-id="bc7a4-287">**VLAN de couche 2 avec 802.1 q** (135)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-287">**Layer 2 VLAN using 802.1Q** (135)</span></span>


</dt> <dd></dd> <dt>

<span id="Layer_3_VLAN_using_IP"></span><span id="layer_3_vlan_using_ip"></span><span id="LAYER_3_VLAN_USING_IP"></span>

<span data-ttu-id="bc7a4-288">**Réseau local virtuel de couche 3 utilisant IP** (136)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-288">**Layer 3 VLAN using IP** (136)</span></span>


</dt> <dd></dd> <dt>

<span id="Layer_3_VLAN_using_IPX"></span><span id="layer_3_vlan_using_ipx"></span><span id="LAYER_3_VLAN_USING_IPX"></span>

<span data-ttu-id="bc7a4-289">**Réseau local virtuel de couche 3 utilisant IPX** (137)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-289">**Layer 3 VLAN using IPX** (137)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Power_Line"></span><span id="digital_power_line"></span><span id="DIGITAL_POWER_LINE"></span>

<span data-ttu-id="bc7a4-290">**Power Line numérique** (138)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-290">**Digital Power Line** (138)</span></span>


</dt> <dd></dd> <dt>

<span id="Multimedia_Mail_over_IP"></span><span id="multimedia_mail_over_ip"></span><span id="MULTIMEDIA_MAIL_OVER_IP"></span>

<span data-ttu-id="bc7a4-291">**Messagerie multimédia sur IP** (139)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-291">**Multimedia Mail over IP** (139)</span></span>


</dt> <dd></dd> <dt>

<span id="DTM"></span><span id="dtm"></span>

<span data-ttu-id="bc7a4-292">**DTM** (140)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-292">**DTM** (140)</span></span>


</dt> <dd></dd> <dt>

<span id="DCN"></span><span id="dcn"></span>

<span data-ttu-id="bc7a4-293">**DCN** (141)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-293">**DCN** (141)</span></span>


</dt> <dd></dd> <dt>

<span id="IP_Forwarding"></span><span id="ip_forwarding"></span><span id="IP_FORWARDING"></span>

<span data-ttu-id="bc7a4-294">**Transfert IP** (142)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-294">**IP Forwarding** (142)</span></span>


</dt> <dd></dd> <dt>

<span id="MSDSL"></span><span id="msdsl"></span>

<span data-ttu-id="bc7a4-295">**MSDS** (143)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-295">**MSDSL** (143)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_1394"></span><span id="ieee_1394"></span>

<span data-ttu-id="bc7a4-296">**IEEE 1394** (144)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-296">**IEEE 1394** (144)</span></span>


</dt> <dd></dd> <dt>

<span id="IF-GSN_HIPPI-6400"></span><span id="if-gsn_hippi-6400"></span>

<span data-ttu-id="bc7a4-297">**If-GSN/hippai-6400** (145)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-297">**IF-GSN/HIPPI-6400** (145)</span></span>


</dt> <dd></dd> <dt>

<span id="DVB-RCC_MAC_Layer"></span><span id="dvb-rcc_mac_layer"></span><span id="DVB-RCC_MAC_LAYER"></span>

<span data-ttu-id="bc7a4-298">**Couche MAC-RCC-RCC** (146)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-298">**DVB-RCC MAC Layer** (146)</span></span>


</dt> <dd></dd> <dt>

<span id="DVB-RCC_Downstream"></span><span id="dvb-rcc_downstream"></span><span id="DVB-RCC_DOWNSTREAM"></span>

<span data-ttu-id="bc7a4-299">**DVB-RCC en aval** (147)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-299">**DVB-RCC Downstream** (147)</span></span>


</dt> <dd></dd> <dt>

<span id="DVB-RCC_Upstream"></span><span id="dvb-rcc_upstream"></span><span id="DVB-RCC_UPSTREAM"></span>

<span data-ttu-id="bc7a4-300">**DVB-RCC en amont** (148)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-300">**DVB-RCC Upstream** (148)</span></span>


</dt> <dd></dd> <dt>

<span id="ATM_Virtual"></span><span id="atm_virtual"></span><span id="ATM_VIRTUAL"></span>

<span data-ttu-id="bc7a4-301">**Virtuel ATM** (149)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-301">**ATM Virtual** (149)</span></span>


</dt> <dd></dd> <dt>

<span id="MPLS_Tunnel"></span><span id="mpls_tunnel"></span><span id="MPLS_TUNNEL"></span>

<span data-ttu-id="bc7a4-302">**Tunnel MPLS** (150)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-302">**MPLS Tunnel** (150)</span></span>


</dt> <dd></dd> <dt>

<span id="SRP"></span><span id="srp"></span>

<span data-ttu-id="bc7a4-303">**SRP** (151)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-303">**SRP** (151)</span></span>


</dt> <dd></dd> <dt>

<span id="Voice_over_ATM"></span><span id="voice_over_atm"></span><span id="VOICE_OVER_ATM"></span>

<span data-ttu-id="bc7a4-304">**Voix sur ATM** (152)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-304">**Voice over ATM** (152)</span></span>


</dt> <dd></dd> <dt>

<span id="Voice_over_Frame_Relay"></span><span id="voice_over_frame_relay"></span><span id="VOICE_OVER_FRAME_RELAY"></span>

<span data-ttu-id="bc7a4-305">**Voix sur relais de trame** (153)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-305">**Voice over Frame Relay** (153)</span></span>


</dt> <dd></dd> <dt>

<span id="ISDL"></span><span id="isdl"></span>

<span data-ttu-id="bc7a4-306">**ISDL** (154)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-306">**ISDL** (154)</span></span>


</dt> <dd></dd> <dt>

<span id="Composite_Link"></span><span id="composite_link"></span><span id="COMPOSITE_LINK"></span>

<span data-ttu-id="bc7a4-307">**Lien composite** (155)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-307">**Composite Link** (155)</span></span>


</dt> <dd></dd> <dt>

<span id="SS7_Signaling_Link"></span><span id="ss7_signaling_link"></span><span id="SS7_SIGNALING_LINK"></span>

<span data-ttu-id="bc7a4-308">**Lien de signalisation SS7** (156)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-308">**SS7 Signaling Link** (156)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_P2P_Wireless"></span><span id="proprietary_p2p_wireless"></span><span id="PROPRIETARY_P2P_WIRELESS"></span>

<span data-ttu-id="bc7a4-309">**Sans fil P2P propriétaire** (157)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-309">**Proprietary P2P Wireless** (157)</span></span>


</dt> <dd></dd> <dt>

<span id="Frame_Forward"></span><span id="frame_forward"></span><span id="FRAME_FORWARD"></span>

<span data-ttu-id="bc7a4-310">**Image vers l’avant** (158)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-310">**Frame Forward** (158)</span></span>


</dt> <dd></dd> <dt>

<span id="RFC1483_Multiprotocol_over_ATM"></span><span id="rfc1483_multiprotocol_over_atm"></span><span id="RFC1483_MULTIPROTOCOL_OVER_ATM"></span>

<span data-ttu-id="bc7a4-311">**RFC1483 Multiprotocol sur ATM** (159)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-311">**RFC1483 Multiprotocol over ATM** (159)</span></span>


</dt> <dd></dd> <dt>

<span id="USB"></span><span id="usb"></span>

<span data-ttu-id="bc7a4-312">**USB** (160)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-312">**USB** (160)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3ad_Link_Aggregate"></span><span id="ieee_802.3ad_link_aggregate"></span><span id="IEEE_802.3AD_LINK_AGGREGATE"></span>

<span data-ttu-id="bc7a4-313">**Agrégat de liens ad IEEE 802.3** (161)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-313">**IEEE 802.3ad Link Aggregate** (161)</span></span>


</dt> <dd></dd> <dt>

<span id="BGP_Policy_Accounting"></span><span id="bgp_policy_accounting"></span><span id="BGP_POLICY_ACCOUNTING"></span>

<span data-ttu-id="bc7a4-314">**Gestion des stratégies BGP** (162)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-314">**BGP Policy Accounting** (162)</span></span>


</dt> <dd></dd> <dt>

<span id="FRF_.16_Multilink_FR"></span><span id="frf_.16_multilink_fr"></span><span id="FRF_.16_MULTILINK_FR"></span>

<span data-ttu-id="bc7a4-315">**FRF .16 Multilink fr** (163)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-315">**FRF .16 Multilink FR** (163)</span></span>


</dt> <dd></dd> <dt>

<span id="H.323_Gatekeeper"></span><span id="h.323_gatekeeper"></span><span id="H.323_GATEKEEPER"></span>

<span data-ttu-id="bc7a4-316">**Gatekeeper H. 323** (164)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-316">**H.323 Gatekeeper** (164)</span></span>


</dt> <dd></dd> <dt>

<span id="H.323_Proxy"></span><span id="h.323_proxy"></span><span id="H.323_PROXY"></span>

<span data-ttu-id="bc7a4-317">**Proxy H. 323** (165)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-317">**H.323 Proxy** (165)</span></span>


</dt> <dd></dd> <dt>

<span id="MPLS"></span><span id="mpls"></span>

<span data-ttu-id="bc7a4-318">**MPLS** (166)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-318">**MPLS** (166)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-Frequency_Signaling_Link"></span><span id="multi-frequency_signaling_link"></span><span id="MULTI-FREQUENCY_SIGNALING_LINK"></span>

<span data-ttu-id="bc7a4-319">**Lien de signalisation à plusieurs fréquences** (167)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-319">**Multi-Frequency Signaling Link** (167)</span></span>


</dt> <dd></dd> <dt>

<span id="HDSL-2"></span><span id="hdsl-2"></span>

<span data-ttu-id="bc7a4-320">**HDSL-2** (168)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-320">**HDSL-2** (168)</span></span>


</dt> <dd></dd> <dt>

<span id="S-HDSL"></span><span id="s-hdsl"></span>

<span data-ttu-id="bc7a4-321">**S-HDSL** (169)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-321">**S-HDSL** (169)</span></span>


</dt> <dd></dd> <dt>

<span id="DS1_Facility_Data_Link"></span><span id="ds1_facility_data_link"></span><span id="DS1_FACILITY_DATA_LINK"></span>

<span data-ttu-id="bc7a4-322">**Liaison de données de l’installation DS1** (170)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-322">**DS1 Facility Data Link** (170)</span></span>


</dt> <dd></dd> <dt>

<span id="Packet_over_SONET_SDH"></span><span id="packet_over_sonet_sdh"></span><span id="PACKET_OVER_SONET_SDH"></span>

<span data-ttu-id="bc7a4-323">**Paquet sur SONET/SDH** (171)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-323">**Packet over SONET/SDH** (171)</span></span>


</dt> <dd></dd> <dt>

<span id="DVB-ASI_Input"></span><span id="dvb-asi_input"></span><span id="DVB-ASI_INPUT"></span>

<span data-ttu-id="bc7a4-324">**Entrée DVB-ASI** (172)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-324">**DVB-ASI Input** (172)</span></span>


</dt> <dd></dd> <dt>

<span id="DVB-ASI_Output"></span><span id="dvb-asi_output"></span><span id="DVB-ASI_OUTPUT"></span>

<span data-ttu-id="bc7a4-325">**Sortie DVB-ASI** (173)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-325">**DVB-ASI Output** (173)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Line"></span><span id="power_line"></span><span id="POWER_LINE"></span>

<span data-ttu-id="bc7a4-326">**Ligne électrique** (174)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-326">**Power Line** (174)</span></span>


</dt> <dd></dd> <dt>

<span id="Non_Facility_Associated_Signaling"></span><span id="non_facility_associated_signaling"></span><span id="NON_FACILITY_ASSOCIATED_SIGNALING"></span>

<span data-ttu-id="bc7a4-327">**Signal non associé à une installation** (175)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-327">**Non Facility Associated Signaling** (175)</span></span>


</dt> <dd></dd> <dt>

<span id="TR008"></span><span id="tr008"></span>

<span data-ttu-id="bc7a4-328">**TR008** (176)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-328">**TR008** (176)</span></span>


</dt> <dd></dd> <dt>

<span id="GR303_RDT"></span><span id="gr303_rdt"></span>

<span data-ttu-id="bc7a4-329">**GR303 RDT** (177)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-329">**GR303 RDT** (177)</span></span>


</dt> <dd></dd> <dt>

<span id="GR303_IDT"></span><span id="gr303_idt"></span>

<span data-ttu-id="bc7a4-330">**GR303 IDT** (178)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-330">**GR303 IDT** (178)</span></span>


</dt> <dd></dd> <dt>

<span id="ISUP"></span><span id="isup"></span>

<span data-ttu-id="bc7a4-331">**ISUP** (179)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-331">**ISUP** (179)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_Wireless_MAC_Layer"></span><span id="proprietary_wireless_mac_layer"></span><span id="PROPRIETARY_WIRELESS_MAC_LAYER"></span>

<span data-ttu-id="bc7a4-332">**Couche Mac sans fil propriétaire** (180)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-332">**Proprietary Wireless MAC Layer** (180)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_Wireless_Downstream"></span><span id="proprietary_wireless_downstream"></span><span id="PROPRIETARY_WIRELESS_DOWNSTREAM"></span>

<span data-ttu-id="bc7a4-333">En **aval sans fil propriétaire** (181)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-333">**Proprietary Wireless Downstream** (181)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_Wireless_Upstream"></span><span id="proprietary_wireless_upstream"></span><span id="PROPRIETARY_WIRELESS_UPSTREAM"></span>

<span data-ttu-id="bc7a4-334">**Flux de communication sans fil propriétaire** (182)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-334">**Proprietary Wireless Upstream** (182)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPERLAN_Type_2"></span><span id="hiperlan_type_2"></span><span id="HIPERLAN_TYPE_2"></span>

<span data-ttu-id="bc7a4-335">**HiperLAN type 2** (183)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-335">**HIPERLAN Type 2** (183)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_Broadband_Wireless_Access_Point_to_Mulipoint"></span><span id="proprietary_broadband_wireless_access_point_to_mulipoint"></span><span id="PROPRIETARY_BROADBAND_WIRELESS_ACCESS_POINT_TO_MULIPOINT"></span>

<span data-ttu-id="bc7a4-336">**Point d’accès sans fil haut débit propriétaire vers Mulipoint** (184)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-336">**Proprietary Broadband Wireless Access Point to Mulipoint** (184)</span></span>


</dt> <dd></dd> <dt>

<span id="SONET_Overhead_Channel"></span><span id="sonet_overhead_channel"></span><span id="SONET_OVERHEAD_CHANNEL"></span>

<span data-ttu-id="bc7a4-337">**Canal de surcharge SONET** (185)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-337">**SONET Overhead Channel** (185)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Wrapper_Overhead_Channel"></span><span id="digital_wrapper_overhead_channel"></span><span id="DIGITAL_WRAPPER_OVERHEAD_CHANNEL"></span>

<span data-ttu-id="bc7a4-338">**Canal de surcharge du wrapper numérique** (186)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-338">**Digital Wrapper Overhead Channel** (186)</span></span>


</dt> <dd></dd> <dt>

<span id="ATM_Adaptation_Layer_2"></span><span id="atm_adaptation_layer_2"></span><span id="ATM_ADAPTATION_LAYER_2"></span>

<span data-ttu-id="bc7a4-339">**Couche d’adaptation ATM 2** (187)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-339">**ATM Adaptation Layer 2** (187)</span></span>


</dt> <dd></dd> <dt>

<span id="Radio_MAC"></span><span id="radio_mac"></span><span id="RADIO_MAC"></span>

<span data-ttu-id="bc7a4-340">**Mac radio** (188)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-340">**Radio MAC** (188)</span></span>


</dt> <dd></dd> <dt>

<span id="ATM_Radio"></span><span id="atm_radio"></span><span id="ATM_RADIO"></span>

<span data-ttu-id="bc7a4-341">**Radio ATM** (189)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-341">**ATM Radio** (189)</span></span>


</dt> <dd></dd> <dt>

<span id="Inter_Machine_Trunk"></span><span id="inter_machine_trunk"></span><span id="INTER_MACHINE_TRUNK"></span>

<span data-ttu-id="bc7a4-342">**Trunk inter-machine** (190)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-342">**Inter Machine Trunk** (190)</span></span>


</dt> <dd></dd> <dt>

<span id="MVL_DSL"></span><span id="mvl_dsl"></span>

<span data-ttu-id="bc7a4-343">**MVL DSL** (191)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-343">**MVL DSL** (191)</span></span>


</dt> <dd></dd> <dt>

<span id="Long_Read_DSL"></span><span id="long_read_dsl"></span><span id="LONG_READ_DSL"></span>

<span data-ttu-id="bc7a4-344">**Long lecture DSL** (192)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-344">**Long Read DSL** (192)</span></span>


</dt> <dd></dd> <dt>

<span id="Frame_Relay_DLCI_Endpoint"></span><span id="frame_relay_dlci_endpoint"></span><span id="FRAME_RELAY_DLCI_ENDPOINT"></span>

<span data-ttu-id="bc7a4-345">**Point de terminaison DLCI de relais de trame** (193)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-345">**Frame Relay DLCI Endpoint** (193)</span></span>


</dt> <dd></dd> <dt>

<span id="ATM_VCI_Endpoint"></span><span id="atm_vci_endpoint"></span><span id="ATM_VCI_ENDPOINT"></span>

<span data-ttu-id="bc7a4-346">**Point de terminaison VCI ATM** (194)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-346">**ATM VCI Endpoint** (194)</span></span>


</dt> <dd></dd> <dt>

<span id="Optical_Channel"></span><span id="optical_channel"></span><span id="OPTICAL_CHANNEL"></span>

<span data-ttu-id="bc7a4-347">**Canal optique** (195)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-347">**Optical Channel** (195)</span></span>


</dt> <dd></dd> <dt>

<span id="Optical_Transport"></span><span id="optical_transport"></span><span id="OPTICAL_TRANSPORT"></span>

<span data-ttu-id="bc7a4-348">**Transport optique** (196)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-348">**Optical Transport** (196)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_ATM"></span><span id="proprietary_atm"></span><span id="PROPRIETARY_ATM"></span>

<span data-ttu-id="bc7a4-349">**ATM propriétaire** (197)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-349">**Proprietary ATM** (197)</span></span>


</dt> <dd></dd> <dt>

<span id="Voice_over_Cable"></span><span id="voice_over_cable"></span><span id="VOICE_OVER_CABLE"></span>

<span data-ttu-id="bc7a4-350">**Câble vocal** (198)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-350">**Voice over Cable** (198)</span></span>


</dt> <dd></dd> <dt>

<span id="Infiniband"></span><span id="infiniband"></span><span id="INFINIBAND"></span>

<span data-ttu-id="bc7a4-351">**InfiniBand** (199)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-351">**Infiniband** (199)</span></span>


</dt> <dd></dd> <dt>

<span id="TE_Link"></span><span id="te_link"></span><span id="TE_LINK"></span>

<span data-ttu-id="bc7a4-352">**Lien te** (200)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-352">**TE Link** (200)</span></span>


</dt> <dd></dd> <dt>

<span id="Q.2931"></span><span id="q.2931"></span>

<span data-ttu-id="bc7a4-353">**Q. 2931** (201)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-353">**Q.2931** (201)</span></span>


</dt> <dd></dd> <dt>

<span id="Virtual_Trunk_Group"></span><span id="virtual_trunk_group"></span><span id="VIRTUAL_TRUNK_GROUP"></span>

<span data-ttu-id="bc7a4-354">**Groupe Trunk virtuel** (202)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-354">**Virtual Trunk Group** (202)</span></span>


</dt> <dd></dd> <dt>

<span id="SIP_Trunk_Group"></span><span id="sip_trunk_group"></span><span id="SIP_TRUNK_GROUP"></span>

<span data-ttu-id="bc7a4-355">**Groupe SIP Trunk** (203)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-355">**SIP Trunk Group** (203)</span></span>


</dt> <dd></dd> <dt>

<span id="SIP_Signaling"></span><span id="sip_signaling"></span><span id="SIP_SIGNALING"></span>

<span data-ttu-id="bc7a4-356">**Signalisation SIP** (204)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-356">**SIP Signaling** (204)</span></span>


</dt> <dd></dd> <dt>

<span id="CATV_Upstream_Channel"></span><span id="catv_upstream_channel"></span><span id="CATV_UPSTREAM_CHANNEL"></span>

<span data-ttu-id="bc7a4-357">**Canal CATV en amont** (205)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-357">**CATV Upstream Channel** (205)</span></span>


</dt> <dd></dd> <dt>

<span id="Econet"></span><span id="econet"></span><span id="ECONET"></span>

<span data-ttu-id="bc7a4-358">**Econet** (206)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-358">**Econet** (206)</span></span>


</dt> <dd></dd> <dt>

<span id="FSAN_155Mb_PON"></span><span id="fsan_155mb_pon"></span><span id="FSAN_155MB_PON"></span>

<span data-ttu-id="bc7a4-359">**FSAN 155MB PON** (207)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-359">**FSAN 155Mb PON** (207)</span></span>


</dt> <dd></dd> <dt>

<span id="FSAN_622Mb_PON"></span><span id="fsan_622mb_pon"></span><span id="FSAN_622MB_PON"></span>

<span data-ttu-id="bc7a4-360">**FSAN 622MB PON** (208)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-360">**FSAN 622Mb PON** (208)</span></span>


</dt> <dd></dd> <dt>

<span id="Transparent_Bridge"></span><span id="transparent_bridge"></span><span id="TRANSPARENT_BRIDGE"></span>

<span data-ttu-id="bc7a4-361">**Pont transparent** (209)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-361">**Transparent Bridge** (209)</span></span>


</dt> <dd></dd> <dt>

<span id="Line_Group"></span><span id="line_group"></span><span id="LINE_GROUP"></span>

<span data-ttu-id="bc7a4-362">**Groupe de lignes** (210)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-362">**Line Group** (210)</span></span>


</dt> <dd></dd> <dt>

<span id="Voice_E_M_Feature_Group"></span><span id="voice_e_m_feature_group"></span><span id="VOICE_E_M_FEATURE_GROUP"></span>

<span data-ttu-id="bc7a4-363">**Groupe de fonctionnalités vocal E&M** (211)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-363">**Voice E&M Feature Group** (211)</span></span>


</dt> <dd></dd> <dt>

<span id="Voice_FGD_EANA"></span><span id="voice_fgd_eana"></span><span id="VOICE_FGD_EANA"></span>

<span data-ttu-id="bc7a4-364">**Voix FGD eana** (212)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-364">**Voice FGD EANA** (212)</span></span>


</dt> <dd></dd> <dt>

<span id="Voice_DID"></span><span id="voice_did"></span><span id="VOICE_DID"></span>

<span data-ttu-id="bc7a4-365">**Voix** (213)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-365">**Voice DID** (213)</span></span>


</dt> <dd></dd> <dt>

<span id="MPEG_Transport"></span><span id="mpeg_transport"></span><span id="MPEG_TRANSPORT"></span>

<span data-ttu-id="bc7a4-366">**Transport MPEG** (214)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-366">**MPEG Transport** (214)</span></span>


</dt> <dd></dd> <dt>

<span id="6To4"></span><span id="6to4"></span><span id="6TO4"></span>

<span data-ttu-id="bc7a4-367">**6to4** (215)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-367">**6To4** (215)</span></span>


</dt> <dd></dd> <dt>

<span id="GTP"></span><span id="gtp"></span>

<span data-ttu-id="bc7a4-368">**GTP** (216)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-368">**GTP** (216)</span></span>


</dt> <dd></dd> <dt>

<span id="Paradyne_EtherLoop_1"></span><span id="paradyne_etherloop_1"></span><span id="PARADYNE_ETHERLOOP_1"></span>

<span data-ttu-id="bc7a4-369">**Paradyne EtherLoop 1** (217)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-369">**Paradyne EtherLoop 1** (217)</span></span>


</dt> <dd></dd> <dt>

<span id="Paradyne_EtherLoop_2"></span><span id="paradyne_etherloop_2"></span><span id="PARADYNE_ETHERLOOP_2"></span>

<span data-ttu-id="bc7a4-370">**Paradyne EtherLoop 2** (218)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-370">**Paradyne EtherLoop 2** (218)</span></span>


</dt> <dd></dd> <dt>

<span id="Optical_Channel_Group"></span><span id="optical_channel_group"></span><span id="OPTICAL_CHANNEL_GROUP"></span>

<span data-ttu-id="bc7a4-371">**Groupe de canaux optiques** (219)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-371">**Optical Channel Group** (219)</span></span>


</dt> <dd></dd> <dt>

<span id="HomePNA"></span><span id="homepna"></span><span id="HOMEPNA"></span>

<span data-ttu-id="bc7a4-372">**HomePNA** (220)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-372">**HomePNA** (220)</span></span>


</dt> <dd></dd> <dt>

<span id="GFP"></span><span id="gfp"></span>

<span data-ttu-id="bc7a4-373">**GFP** (221)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-373">**GFP** (221)</span></span>


</dt> <dd></dd> <dt>

<span id="ciscoISLvlan"></span><span id="ciscoislvlan"></span><span id="CISCOISLVLAN"></span>

<span data-ttu-id="bc7a4-374">**ciscoISLvlan** (222)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-374">**ciscoISLvlan** (222)</span></span>


</dt> <dd></dd> <dt>

<span id="actelisMetaLOOP"></span><span id="actelismetaloop"></span><span id="ACTELISMETALOOP"></span>

<span data-ttu-id="bc7a4-375">**actelisMetaLOOP** (223)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-375">**actelisMetaLOOP** (223)</span></span>


</dt> <dd></dd> <dt>

<span id="Fcip"></span><span id="fcip"></span><span id="FCIP"></span>

<span data-ttu-id="bc7a4-376">**FCIP** (224)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-376">**Fcip** (224)</span></span>


</dt> <dd></dd> <dt>

<span id="IANA_Reserved"></span><span id="iana_reserved"></span><span id="IANA_RESERVED"></span>

<span data-ttu-id="bc7a4-377">**IANA réservé** (225.. 4095)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-377">**IANA Reserved** (225..4095)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>

<span data-ttu-id="bc7a4-378">**IPv4** (4096)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-378">**IPv4** (4096)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>

<span data-ttu-id="bc7a4-379">**IPv6** (4097)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-379">**IPv6** (4097)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv4_v6"></span><span id="ipv4_v6"></span><span id="IPV4_V6"></span>

<span data-ttu-id="bc7a4-380">**IPv4/v6** (4098)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-380">**IPv4/v6** (4098)</span></span>


</dt> <dd></dd> <dt>

<span id="IPX"></span><span id="ipx"></span>

<span data-ttu-id="bc7a4-381">**IPX** (4099)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-381">**IPX** (4099)</span></span>


</dt> <dd></dd> <dt>

<span id="DECnet"></span><span id="decnet"></span><span id="DECNET"></span>

<span data-ttu-id="bc7a4-382">**DECnet** (4100)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-382">**DECnet** (4100)</span></span>


</dt> <dd></dd> <dt>

<span id="SNA"></span><span id="sna"></span>

<span data-ttu-id="bc7a4-383">**SNA** (4101)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-383">**SNA** (4101)</span></span>


</dt> <dd></dd> <dt>

<span id="CONP"></span><span id="conp"></span>

<span data-ttu-id="bc7a4-384">**CONP** (4102)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-384">**CONP** (4102)</span></span>


</dt> <dd></dd> <dt>

<span id="CLNP"></span><span id="clnp"></span>

<span data-ttu-id="bc7a4-385">**CLNP** (4103)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-385">**CLNP** (4103)</span></span>


</dt> <dd></dd> <dt>

<span id="VINES"></span><span id="vines"></span>

<span data-ttu-id="bc7a4-386">**Vignes** (4104)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-386">**VINES** (4104)</span></span>


</dt> <dd></dd> <dt>

<span id="XNS"></span><span id="xns"></span>

<span data-ttu-id="bc7a4-387">**XNS** (4105)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-387">**XNS** (4105)</span></span>


</dt> <dd></dd> <dt>

<span id="ISDN_B_Channel_Endpoint"></span><span id="isdn_b_channel_endpoint"></span><span id="ISDN_B_CHANNEL_ENDPOINT"></span>

<span data-ttu-id="bc7a4-388">**Point de terminaison de canal B RNIS** (4106)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-388">**ISDN B Channel Endpoint** (4106)</span></span>


</dt> <dd></dd> <dt>

<span id="ISDN_D_Channel_Endpoint"></span><span id="isdn_d_channel_endpoint"></span><span id="ISDN_D_CHANNEL_ENDPOINT"></span>

<span data-ttu-id="bc7a4-389">**Point de terminaison de canal D RNIS** (4107)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-389">**ISDN D Channel Endpoint** (4107)</span></span>


</dt> <dd></dd> <dt>

<span id="BGP"></span><span id="bgp"></span>

<span data-ttu-id="bc7a4-390">**BGP** (4108)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-390">**BGP** (4108)</span></span>


</dt> <dd></dd> <dt>

<span id="OSPF"></span><span id="ospf"></span>

<span data-ttu-id="bc7a4-391">**OSPF** (4109)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-391">**OSPF** (4109)</span></span>


</dt> <dd></dd> <dt>

<span id="UDP"></span><span id="udp"></span>

<span data-ttu-id="bc7a4-392">**UDP** (4110)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-392">**UDP** (4110)</span></span>


</dt> <dd></dd> <dt>

<span id="TCP"></span><span id="tcp"></span>

<span data-ttu-id="bc7a4-393">**TCP** (4111)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-393">**TCP** (4111)</span></span>


</dt> <dd></dd> <dt>

<span id="802.11a"></span><span id="802.11A"></span>

<span data-ttu-id="bc7a4-394">**802.11 a** (4112)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-394">**802.11a** (4112)</span></span>


</dt> <dd></dd> <dt>

<span id="802.11b"></span><span id="802.11B"></span>

<span data-ttu-id="bc7a4-395">**802.11 b** (4113)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-395">**802.11b** (4113)</span></span>


</dt> <dd></dd> <dt>

<span id="802.11g"></span><span id="802.11G"></span>

<span data-ttu-id="bc7a4-396">**802.11 g** (4114)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-396">**802.11g** (4114)</span></span>


</dt> <dd></dd> <dt>

<span id="802.11h"></span><span id="802.11H"></span>

<span data-ttu-id="bc7a4-397">**802.11 h** (4115)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-397">**802.11h** (4115)</span></span>


</dt> <dd></dd> <dt>

<span id="NFS"></span><span id="nfs"></span>

<span data-ttu-id="bc7a4-398">**NFS** (4200)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-398">**NFS** (4200)</span></span>


</dt> <dd></dd> <dt>

<span id="CIFS"></span><span id="cifs"></span>

<span data-ttu-id="bc7a4-399">**CIFS** (4201)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-399">**CIFS** (4201)</span></span>


</dt> <dd></dd> <dt>

<span id="DAFS"></span><span id="dafs"></span>

<span data-ttu-id="bc7a4-400">**DAFS** (4202)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-400">**DAFS** (4202)</span></span>


</dt> <dd></dd> <dt>

<span id="WebDAV"></span><span id="webdav"></span><span id="WEBDAV"></span>

<span data-ttu-id="bc7a4-401">**WebDAV** (4203)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-401">**WebDAV** (4203)</span></span>


</dt> <dd></dd> <dt>

<span id="HTTP"></span><span id="http"></span>

<span data-ttu-id="bc7a4-402">**Http** (4204)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-402">**HTTP** (4204)</span></span>


</dt> <dd></dd> <dt>

<span id="FTP"></span><span id="ftp"></span>

<span data-ttu-id="bc7a4-403">**FTP** (4205)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-403">**FTP** (4205)</span></span>


</dt> <dd></dd> <dt>

<span id="NDMP"></span><span id="ndmp"></span>

<span data-ttu-id="bc7a4-404">**NDMP** (4300)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-404">**NDMP** (4300)</span></span>


</dt> <dd></dd> <dt>

<span id="Telnet"></span><span id="telnet"></span><span id="TELNET"></span>

<span data-ttu-id="bc7a4-405">**Telnet** (4400)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-405">**Telnet** (4400)</span></span>


</dt> <dd></dd> <dt>

<span id="SSH"></span><span id="ssh"></span>

<span data-ttu-id="bc7a4-406">**SSH** (4401)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-406">**SSH** (4401)</span></span>


</dt> <dd></dd> <dt>

<span id="SM_CLP"></span><span id="sm_clp"></span>

<span data-ttu-id="bc7a4-407">**SM CLP** (4402)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-407">**SM CLP** (4402)</span></span>


</dt> <dd></dd> <dt>

<span id="SMTP"></span><span id="smtp"></span>

<span data-ttu-id="bc7a4-408">**SMTP** (4403)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-408">**SMTP** (4403)</span></span>


</dt> <dd></dd> <dt>

<span id="LDAP"></span><span id="ldap"></span>

<span data-ttu-id="bc7a4-409">**LDAP** (4404)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-409">**LDAP** (4404)</span></span>


</dt> <dd></dd> <dt>

<span id="RDP"></span><span id="rdp"></span>

<span data-ttu-id="bc7a4-410">**RDP** (4405)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-410">**RDP** (4405)</span></span>


</dt> <dd></dd> <dt>

<span id="HTTPS"></span><span id="https"></span>

<span data-ttu-id="bc7a4-411">**Https** (4406)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-411">**HTTPS** (4406)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="bc7a4-412">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-412">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="bc7a4-413">**Fournisseur réservé** (32768...)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-413">**Vendor Reserved** (32768..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bc7a4-414">**ProtocolType**</span><span class="sxs-lookup"><span data-stu-id="bc7a4-414">**ProtocolType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc7a4-415">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bc7a4-415">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bc7a4-416">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bc7a4-416">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc7a4-417">Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**\_ ProtocolEndpoint CIM**.**ProtocolIFType**"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ ProtocolEndpoint CIM**.**OtherTypeDescription**")</span><span class="sxs-lookup"><span data-stu-id="bc7a4-417">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**CIM\_ProtocolEndpoint**.**ProtocolIFType**"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ProtocolEndpoint**.**OtherTypeDescription**")</span></span>
</dt> </dl>

> [!Note]  
> <span data-ttu-id="bc7a4-418">Description déconseillée : énumération utilisée pour classer et classer les différentes instances de cette classe.</span><span class="sxs-lookup"><span data-stu-id="bc7a4-418">Deprecated description: An enumeration used to categorize and classify different instances of this class.</span></span>

 

<span data-ttu-id="bc7a4-419">Cette propriété est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="bc7a4-419">This property is deprecated.</span></span> <span data-ttu-id="bc7a4-420">Utilisez plutôt la propriété **ProtocolIFType** .</span><span class="sxs-lookup"><span data-stu-id="bc7a4-420">Instead, use the **ProtocolIFType** property.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bc7a4-421">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-421">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="bc7a4-422">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-422">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>

<span data-ttu-id="bc7a4-423">**IPv4** (2)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-423">**IPv4** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>

<span data-ttu-id="bc7a4-424">**IPv6** (3)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-424">**IPv6** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="IPX"></span><span id="ipx"></span>

<span data-ttu-id="bc7a4-425">**IPX** (4)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-425">**IPX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="AppleTalk"></span><span id="appletalk"></span><span id="APPLETALK"></span>

<span data-ttu-id="bc7a4-426">**AppleTalk** (5)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-426">**AppleTalk** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="DECnet"></span><span id="decnet"></span><span id="DECNET"></span>

<span data-ttu-id="bc7a4-427">**DECnet** (6)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-427">**DECnet** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SNA"></span><span id="sna"></span>

<span data-ttu-id="bc7a4-428">**SNA** (7)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-428">**SNA** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="CONP"></span><span id="conp"></span>

<span data-ttu-id="bc7a4-429">**CONP** (8)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-429">**CONP** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="CLNP"></span><span id="clnp"></span>

<span data-ttu-id="bc7a4-430">**CLNP** (9)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-430">**CLNP** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="VINES"></span><span id="vines"></span>

<span data-ttu-id="bc7a4-431">**Vignes** (10)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-431">**VINES** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="XNS"></span><span id="xns"></span>

<span data-ttu-id="bc7a4-432">**XNS** (11)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-432">**XNS** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="ATM"></span><span id="atm"></span>

<span data-ttu-id="bc7a4-433">**ATM** (12)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-433">**ATM** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>

<span data-ttu-id="bc7a4-434">**Relais de trames** (13)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-434">**Frame Relay** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

<span data-ttu-id="bc7a4-435">**Ethernet** (14)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-435">**Ethernet** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="TokenRing"></span><span id="tokenring"></span><span id="TOKENRING"></span>

<span data-ttu-id="bc7a4-436">**TokenRing** (15)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-436">**TokenRing** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="FDDI"></span><span id="fddi"></span>

<span data-ttu-id="bc7a4-437">**FDDI** (16)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-437">**FDDI** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Infiniband"></span><span id="infiniband"></span><span id="INFINIBAND"></span>

<span data-ttu-id="bc7a4-438">**InfiniBand** (17)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-438">**Infiniband** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Fibre_Channel"></span><span id="fibre_channel"></span><span id="FIBRE_CHANNEL"></span>

<span data-ttu-id="bc7a4-439">**Fibre Channel** (18)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-439">**Fibre Channel** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="ISDN_BRI_Endpoint"></span><span id="isdn_bri_endpoint"></span><span id="ISDN_BRI_ENDPOINT"></span>

<span data-ttu-id="bc7a4-440">**Point de terminaison BRI RNIS** (19)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-440">**ISDN BRI Endpoint** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="ISDN_B_Channel_Endpoint"></span><span id="isdn_b_channel_endpoint"></span><span id="ISDN_B_CHANNEL_ENDPOINT"></span>

<span data-ttu-id="bc7a4-441">**Point de terminaison de canal B RNIS** (20)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-441">**ISDN B Channel Endpoint** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="ISDN_D_Channel_Endpoint"></span><span id="isdn_d_channel_endpoint"></span><span id="ISDN_D_CHANNEL_ENDPOINT"></span>

<span data-ttu-id="bc7a4-442">**Point de terminaison de canal D RNIS** (21)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-442">**ISDN D Channel Endpoint** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv4_v6"></span><span id="ipv4_v6"></span><span id="IPV4_V6"></span>

<span data-ttu-id="bc7a4-443">**IPv4/v6** (22)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-443">**IPv4/v6** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="BGP"></span><span id="bgp"></span>

<span data-ttu-id="bc7a4-444">**BGP** (23)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-444">**BGP** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="OSPF"></span><span id="ospf"></span>

<span data-ttu-id="bc7a4-445">**OSPF** (24)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-445">**OSPF** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="MPLS"></span><span id="mpls"></span>

<span data-ttu-id="bc7a4-446">**MPLS** (25)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-446">**MPLS** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="UDP"></span><span id="udp"></span>

<span data-ttu-id="bc7a4-447">**UDP** (26)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-447">**UDP** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="TCP"></span><span id="tcp"></span>

<span data-ttu-id="bc7a4-448">**TCP** (27)</span><span class="sxs-lookup"><span data-stu-id="bc7a4-448">**TCP** (27)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bc7a4-449">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="bc7a4-449">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc7a4-450">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="bc7a4-450">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="bc7a4-451">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bc7a4-451">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc7a4-452">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("TimeOfLastStateChange"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| If-MIB. ifLastChange ")</span><span class="sxs-lookup"><span data-stu-id="bc7a4-452">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("TimeOfLastStateChange"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|IF-MIB.ifLastChange")</span></span>
</dt> </dl>

<span data-ttu-id="bc7a4-453">Date et heure de la dernière modification de la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="bc7a4-453">The date and time when the **EnabledState** property last changed.</span></span> <span data-ttu-id="bc7a4-454">Si **EnabledState** n’a pas changé et que cette propriété est remplie, elle doit être définie sur une valeur d’intervalle égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="bc7a4-454">If **EnabledState** has not changed and this property is populated, then it must be set to a zero interval value.</span></span> <span data-ttu-id="bc7a4-455">Si une modification d’État a été demandée, mais rejetée ou n’a pas encore été traitée, la propriété ne doit pas être mise à jour.</span><span class="sxs-lookup"><span data-stu-id="bc7a4-455">If a state change was requested, but rejected or not yet processed, the property must not be updated.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bc7a4-456">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bc7a4-456">Requirements</span></span>



| <span data-ttu-id="bc7a4-457">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bc7a4-457">Requirement</span></span> | <span data-ttu-id="bc7a4-458">Valeur</span><span class="sxs-lookup"><span data-stu-id="bc7a4-458">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc7a4-459">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bc7a4-459">Minimum supported client</span></span><br/> | <span data-ttu-id="bc7a4-460">Windows 8</span><span class="sxs-lookup"><span data-stu-id="bc7a4-460">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="bc7a4-461">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bc7a4-461">Minimum supported server</span></span><br/> | <span data-ttu-id="bc7a4-462">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bc7a4-462">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="bc7a4-463">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="bc7a4-463">Namespace</span></span><br/>                | <span data-ttu-id="bc7a4-464">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="bc7a4-464">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="bc7a4-465">MOF</span><span class="sxs-lookup"><span data-stu-id="bc7a4-465">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bc7a4-466"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bc7a4-466"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bc7a4-467">DLL</span><span class="sxs-lookup"><span data-stu-id="bc7a4-467">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc7a4-468"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bc7a4-468"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bc7a4-469">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bc7a4-469">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc7a4-470">**\_SERVICEACCESSPOINT CIM**</span><span class="sxs-lookup"><span data-stu-id="bc7a4-470">**CIM\_ServiceAccessPoint**</span></span>](cim-serviceaccesspoint.md)
</dt> </dl>

 

