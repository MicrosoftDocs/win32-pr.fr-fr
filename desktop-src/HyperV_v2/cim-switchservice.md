---
description: Représente un service de commutateur.
ms.assetid: cf6319fa-7d69-4820-b0e0-775aad8b190c
title: Classe CIM_SwitchService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SwitchService
- CIM_SwitchService.BridgeAddress
- CIM_SwitchService.NumPorts
- CIM_SwitchService.BridgeType
- CIM_SwitchService.BridgeAddressType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9abe6869c5b8ac61630091315e476ae232630717
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531882"
---
# <a name="cim_switchservice-class"></a><span data-ttu-id="0470a-103">\_Classe CIM SwitchService</span><span class="sxs-lookup"><span data-stu-id="0470a-103">CIM\_SwitchService class</span></span>

<span data-ttu-id="0470a-104">Représente un service de commutateur.</span><span class="sxs-lookup"><span data-stu-id="0470a-104">Represents a switch service.</span></span>

## <a name="syntax"></a><span data-ttu-id="0470a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0470a-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::SwitchingBridging")]
class CIM_SwitchService : CIM_ForwardingService
{
  string BridgeAddress;
  uint16 NumPorts;
  uint8  BridgeType;
  uint16 BridgeAddressType;
};
```

## <a name="members"></a><span data-ttu-id="0470a-106">Membres</span><span class="sxs-lookup"><span data-stu-id="0470a-106">Members</span></span>

<span data-ttu-id="0470a-107">La classe **CIM \_ SwitchService** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="0470a-107">The **CIM\_SwitchService** class has these types of members:</span></span>

-   [<span data-ttu-id="0470a-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0470a-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0470a-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0470a-109">Properties</span></span>

<span data-ttu-id="0470a-110">La classe **CIM \_ SwitchService** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="0470a-110">The **CIM\_SwitchService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0470a-111">**BridgeAddress**</span><span class="sxs-lookup"><span data-stu-id="0470a-111">**BridgeAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0470a-112">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0470a-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0470a-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0470a-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0470a-114">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Bridge-MIB. dot1dBaseBridgeAddress "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SwitchService**.**BridgeAddressType**")</span><span class="sxs-lookup"><span data-stu-id="0470a-114">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|BRIDGE-MIB.dot1dBaseBridgeAddress"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SwitchService**.**BridgeAddressType**")</span></span>
</dt> </dl>

<span data-ttu-id="0470a-115">Adresse du service de commutateur, qui est une partie de l’identificateur unique du service.</span><span class="sxs-lookup"><span data-stu-id="0470a-115">The address of the switch service, which is a portion of the unique identifier of the service.</span></span>

</dd> <dt>

<span data-ttu-id="0470a-116">**BridgeAddressType**</span><span class="sxs-lookup"><span data-stu-id="0470a-116">**BridgeAddressType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0470a-117">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0470a-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0470a-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0470a-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0470a-119">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SwitchService**.**BridgeAddress**")</span><span class="sxs-lookup"><span data-stu-id="0470a-119">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SwitchService**.**BridgeAddress**")</span></span>
</dt> </dl>

<span data-ttu-id="0470a-120">Format d’adressage utilisé pour le pont et la propriété **BridgeAddress** .</span><span class="sxs-lookup"><span data-stu-id="0470a-120">The addressing format used for the bridge and the **BridgeAddress** property.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0470a-121">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="0470a-121">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>

<span data-ttu-id="0470a-122">**IPv4** (2)</span><span class="sxs-lookup"><span data-stu-id="0470a-122">**IPv4** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>

<span data-ttu-id="0470a-123">**IPv6** (3)</span><span class="sxs-lookup"><span data-stu-id="0470a-123">**IPv6** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="MAC"></span><span id="mac"></span>

<span data-ttu-id="0470a-124">**Mac** (4)</span><span class="sxs-lookup"><span data-stu-id="0470a-124">**MAC** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="MAC___Spanning_Tree_Priority"></span><span id="mac___spanning_tree_priority"></span><span id="MAC___SPANNING_TREE_PRIORITY"></span>

<span data-ttu-id="0470a-125">**Mac + priorité d’arborescence étendue** (5)</span><span class="sxs-lookup"><span data-stu-id="0470a-125">**MAC + Spanning Tree Priority** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0470a-126">**BridgeType**</span><span class="sxs-lookup"><span data-stu-id="0470a-126">**BridgeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0470a-127">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="0470a-127">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="0470a-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0470a-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0470a-129">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Bridge-MIB. dot1dBaseType ")</span><span class="sxs-lookup"><span data-stu-id="0470a-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|BRIDGE-MIB.dot1dBaseType")</span></span>
</dt> </dl>

<span data-ttu-id="0470a-130">Type de service de commutation à effectuer.</span><span class="sxs-lookup"><span data-stu-id="0470a-130">The type of switching service to perform.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0470a-131">**Inconnu** (1)</span><span class="sxs-lookup"><span data-stu-id="0470a-131">**Unknown** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Transparent-only"></span><span id="transparent-only"></span><span id="TRANSPARENT-ONLY"></span>

<span data-ttu-id="0470a-132">**Transparent uniquement** (2)</span><span class="sxs-lookup"><span data-stu-id="0470a-132">**Transparent-only** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="SourceRoute-only"></span><span id="sourceroute-only"></span><span id="SOURCEROUTE-ONLY"></span>

<span data-ttu-id="0470a-133">**SourceRoute uniquement** (3)</span><span class="sxs-lookup"><span data-stu-id="0470a-133">**SourceRoute-only** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="SRT"></span><span id="srt"></span>

<span data-ttu-id="0470a-134">**SRT** (4)</span><span class="sxs-lookup"><span data-stu-id="0470a-134">**SRT** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0470a-135">**NumPorts**</span><span class="sxs-lookup"><span data-stu-id="0470a-135">**NumPorts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0470a-136">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0470a-136">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0470a-137">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0470a-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0470a-138">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Bridge-MIB. dot1dBaseNumPorts ")</span><span class="sxs-lookup"><span data-stu-id="0470a-138">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|BRIDGE-MIB.dot1dBaseNumPorts")</span></span>
</dt> </dl>

<span data-ttu-id="0470a-139">Nombre de ports de commutateur contrôlés par ce service de commutation.</span><span class="sxs-lookup"><span data-stu-id="0470a-139">The number of switch ports controlled by this switching service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0470a-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0470a-140">Requirements</span></span>



| <span data-ttu-id="0470a-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0470a-141">Requirement</span></span> | <span data-ttu-id="0470a-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="0470a-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0470a-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0470a-143">Minimum supported client</span></span><br/> | <span data-ttu-id="0470a-144">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="0470a-144">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="0470a-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0470a-145">Minimum supported server</span></span><br/> | <span data-ttu-id="0470a-146">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="0470a-146">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="0470a-147">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0470a-147">Namespace</span></span><br/>                | <span data-ttu-id="0470a-148">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="0470a-148">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0470a-149">MOF</span><span class="sxs-lookup"><span data-stu-id="0470a-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0470a-150"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0470a-150"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0470a-151">DLL</span><span class="sxs-lookup"><span data-stu-id="0470a-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0470a-152"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0470a-152"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0470a-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0470a-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0470a-154">**\_FORWARDINGSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="0470a-154">**CIM\_ForwardingService**</span></span>](cim-forwardingservice.md)
</dt> </dl>

 

