---
description: Représente les paramètres pour l’allocation du port Ethernet, en plus des paramètres fournis par la classe CIM \_ EthernetPort. Ces paramètres sont utilisés pour fournir des informations spécifiques à la ressource elle-même.
ms.assetid: f59ebaf1-60dd-49bd-b48e-d7a6c2650909
title: Classe CIM_EthernetPortAllocationSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_EthernetPortAllocationSettingData
- CIM_EthernetPortAllocationSettingData.DesiredVLANEndpointMode
- CIM_EthernetPortAllocationSettingData.OtherEndpointMode
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7e77b4387f77e88ceaff273b8be72a354c989e7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106512923"
---
# <a name="cim_ethernetportallocationsettingdata-class"></a><span data-ttu-id="b158b-104">\_Classe CIM EthernetPortAllocationSettingData</span><span class="sxs-lookup"><span data-stu-id="b158b-104">CIM\_EthernetPortAllocationSettingData class</span></span>

<span data-ttu-id="b158b-105">Représente les paramètres pour l’allocation du port Ethernet, en plus des paramètres fournis par la classe [**CIM \_ EthernetPort**](cim-ethernetport.md) .</span><span class="sxs-lookup"><span data-stu-id="b158b-105">Represents settings for the allocation of the ethernet port, in addition to the settings provided by the [**CIM\_EthernetPort**](cim-ethernetport.md) class.</span></span> <span data-ttu-id="b158b-106">Ces paramètres sont utilisés pour fournir des informations spécifiques à la ressource elle-même.</span><span class="sxs-lookup"><span data-stu-id="b158b-106">These settings are used to provide information specific to the resource itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="b158b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b158b-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.26.0"), UMLPackagePath("CIM::Core::Resource"), AMENDMENT]
class CIM_EthernetPortAllocationSettingData : CIM_ResourceAllocationSettingData
{
  uint16 DesiredVLANEndpointMode;
  string OtherEndpointMode;
};
```

## <a name="members"></a><span data-ttu-id="b158b-108">Membres</span><span class="sxs-lookup"><span data-stu-id="b158b-108">Members</span></span>

<span data-ttu-id="b158b-109">La classe **CIM \_ EthernetPortAllocationSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b158b-109">The **CIM\_EthernetPortAllocationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="b158b-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b158b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b158b-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b158b-111">Properties</span></span>

<span data-ttu-id="b158b-112">La classe **CIM \_ EthernetPortAllocationSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="b158b-112">The **CIM\_EthernetPortAllocationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b158b-113">**DesiredVLANEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="b158b-113">**DesiredVLANEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b158b-114">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b158b-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b158b-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b158b-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b158b-116">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**","**CIM \_ VLANEndpoint**.**DesiredEndpointMode**","**CIM \_ EthernetPortAllocationSettingData**.**OtherEndpointMode**")</span><span class="sxs-lookup"><span data-stu-id="b158b-116">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**", "**CIM\_VLANEndpoint**.**DesiredEndpointMode**", "**CIM\_EthernetPortAllocationSettingData**.**OtherEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="b158b-117">Mode VLAN demandé.</span><span class="sxs-lookup"><span data-stu-id="b158b-117">The requested VLAN mode.</span></span> <span data-ttu-id="b158b-118">Cette propriété est utilisée pour définir la valeur de la propriété **OperationalEndpointMode** initiale dans l’instance de **\_ VLANEndpoint CIM** associée au port Ethernet.</span><span class="sxs-lookup"><span data-stu-id="b158b-118">This property is used to set the initial **OperationalEndpointMode** property value in the instance of **CIM\_VLANEndpoint** associated with the ethernet port.</span></span>

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="b158b-119">**DMTF réservé** (0)</span><span class="sxs-lookup"><span data-stu-id="b158b-119">**DMTF Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b158b-120">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="b158b-120">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Access"></span><span id="access"></span><span id="ACCESS"></span>

<span data-ttu-id="b158b-121">**Accès** (2)</span><span class="sxs-lookup"><span data-stu-id="b158b-121">**Access** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Dynamic_Auto"></span><span id="dynamic_auto"></span><span id="DYNAMIC_AUTO"></span>

<span data-ttu-id="b158b-122">**Automatique dynamique** (3)</span><span class="sxs-lookup"><span data-stu-id="b158b-122">**Dynamic Auto** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Dynamic_Desirable"></span><span id="dynamic_desirable"></span><span id="DYNAMIC_DESIRABLE"></span>

<span data-ttu-id="b158b-123">**Désirable dynamique** (4)</span><span class="sxs-lookup"><span data-stu-id="b158b-123">**Dynamic Desirable** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Trunk"></span><span id="trunk"></span><span id="TRUNK"></span>

<span data-ttu-id="b158b-124">**Trunk** (5)</span><span class="sxs-lookup"><span data-stu-id="b158b-124">**Trunk** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Dot1Q_Tunnel"></span><span id="dot1q_tunnel"></span><span id="DOT1Q_TUNNEL"></span>

<span data-ttu-id="b158b-125">**Tunnel Dot1Q** (6)</span><span class="sxs-lookup"><span data-stu-id="b158b-125">**Dot1Q Tunnel** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="b158b-126">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="b158b-126">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="b158b-127">**Fournisseur réservé** (0x8000.. 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="b158b-127">**Vendor Reserved** (0x8000..0xFFFF)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b158b-128">**OtherEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="b158b-128">**OtherEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b158b-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b158b-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b158b-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b158b-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b158b-131">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ EthernetPortAllocationSettingData**.**DesiredVLANEndpointMode**")</span><span class="sxs-lookup"><span data-stu-id="b158b-131">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EthernetPortAllocationSettingData**.**DesiredVLANEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="b158b-132">Type de modèle de point de terminaison VLAN pris en charge par ce point de terminaison VLAN, lorsque la valeur de la propriété mode est définie sur « 1 » (autre).</span><span class="sxs-lookup"><span data-stu-id="b158b-132">The type of VLAN endpoint model that is supported by this VLAN endpoint, when the value of the mode property is set to "1" (Other).</span></span> <span data-ttu-id="b158b-133">Cette propriété doit être définie sur **null** lorsque la propriété mode est toute valeur autre que « 1 ».</span><span class="sxs-lookup"><span data-stu-id="b158b-133">This property should be set to **NULL** when the mode property is any value other than "1".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b158b-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b158b-134">Requirements</span></span>



| <span data-ttu-id="b158b-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b158b-135">Requirement</span></span> | <span data-ttu-id="b158b-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="b158b-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b158b-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b158b-137">Minimum supported client</span></span><br/> | <span data-ttu-id="b158b-138">Windows 8</span><span class="sxs-lookup"><span data-stu-id="b158b-138">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="b158b-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b158b-139">Minimum supported server</span></span><br/> | <span data-ttu-id="b158b-140">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b158b-140">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="b158b-141">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b158b-141">Namespace</span></span><br/>                | <span data-ttu-id="b158b-142">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="b158b-142">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b158b-143">MOF</span><span class="sxs-lookup"><span data-stu-id="b158b-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b158b-144"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b158b-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b158b-145">DLL</span><span class="sxs-lookup"><span data-stu-id="b158b-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b158b-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b158b-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b158b-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b158b-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b158b-148">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="b158b-148">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

