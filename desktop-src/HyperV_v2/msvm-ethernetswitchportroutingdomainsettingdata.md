---
description: Représente les données de paramètre du domaine de routage.
ms.assetid: 6216cc4e-b2aa-4344-b8fa-489b986c14be
title: Classe Msvm_EthernetSwitchPortRoutingDomainSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortRoutingDomainSettingData
- Msvm_EthernetSwitchPortRoutingDomainSettingData.RoutingDomainGuid
- Msvm_EthernetSwitchPortRoutingDomainSettingData.RoutingDomainName
- Msvm_EthernetSwitchPortRoutingDomainSettingData.IsolationIdList
- Msvm_EthernetSwitchPortRoutingDomainSettingData.IsolationIdNameList
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 40e16a3c952e63ab89c345201742dafe24cdde7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869270"
---
# <a name="msvm_ethernetswitchportroutingdomainsettingdata-class"></a><span data-ttu-id="ae9a0-103">MSVM \_ EthernetSwitchPortRoutingDomainSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="ae9a0-103">Msvm\_EthernetSwitchPortRoutingDomainSettingData class</span></span>

<span data-ttu-id="ae9a0-104">Représente les données de paramètre du domaine de routage.</span><span class="sxs-lookup"><span data-stu-id="ae9a0-104">Represents the routing domain setting data.</span></span>

<span data-ttu-id="ae9a0-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="ae9a0-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae9a0-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ae9a0-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("BF874DF0-F729-4312-A0FA-194271B88990"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Routing Domain Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortRoutingDomainSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string RoutingDomainGuid = "";
  string RoutingDomainName = "";
  uint32 IsolationIdList[] = {};
  string IsolationIdNameList[] = {};
};
```

## <a name="members"></a><span data-ttu-id="ae9a0-107">Membres</span><span class="sxs-lookup"><span data-stu-id="ae9a0-107">Members</span></span>

<span data-ttu-id="ae9a0-108">La classe **MSVM \_ EthernetSwitchPortRoutingDomainSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ae9a0-108">The **Msvm\_EthernetSwitchPortRoutingDomainSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="ae9a0-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ae9a0-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ae9a0-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ae9a0-110">Properties</span></span>

<span data-ttu-id="ae9a0-111">La classe **MSVM \_ EthernetSwitchPortRoutingDomainSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="ae9a0-111">The **Msvm\_EthernetSwitchPortRoutingDomainSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ae9a0-112">**IsolationIdList**</span><span class="sxs-lookup"><span data-stu-id="ae9a0-112">**IsolationIdList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae9a0-113">Type de données : tableau **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ae9a0-113">Data type: **uint32** array</span></span>
</dt> <dt>

<span data-ttu-id="ae9a0-114">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ae9a0-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ae9a0-115">Qualificateurs : **WmiDataId** (3), [**version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**révision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="ae9a0-115">Qualifiers: **WmiDataId** (3), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="ae9a0-116">ID VirtualSubnetId ou VLAN pour les domaines de routage.</span><span class="sxs-lookup"><span data-stu-id="ae9a0-116">The VirtualSubnetId or VLAN IDs for the routing domains.</span></span>

</dd> <dt>

<span data-ttu-id="ae9a0-117">**IsolationIdNameList**</span><span class="sxs-lookup"><span data-stu-id="ae9a0-117">**IsolationIdNameList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae9a0-118">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="ae9a0-118">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ae9a0-119">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ae9a0-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ae9a0-120">Qualificateurs : **WmiDataId** (4), [**version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**révision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="ae9a0-120">Qualifiers: **WmiDataId** (4), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="ae9a0-121">Tableau de noms conviviaux VirtualSubnetId ou VLAN.</span><span class="sxs-lookup"><span data-stu-id="ae9a0-121">The VirtualSubnetId or VLAN friendly name array.</span></span>

</dd> <dt>

<span data-ttu-id="ae9a0-122">**RoutingDomainGuid**</span><span class="sxs-lookup"><span data-stu-id="ae9a0-122">**RoutingDomainGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae9a0-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ae9a0-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae9a0-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ae9a0-124">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ae9a0-125">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (38), **WmiDataId** (1), [**version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**révision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="ae9a0-125">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (38), **WmiDataId** (1), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="ae9a0-126">GUID du domaine de routage.</span><span class="sxs-lookup"><span data-stu-id="ae9a0-126">The routing domain GUID.</span></span>

</dd> <dt>

<span data-ttu-id="ae9a0-127">**RoutingDomainName**</span><span class="sxs-lookup"><span data-stu-id="ae9a0-127">**RoutingDomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae9a0-128">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ae9a0-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae9a0-129">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ae9a0-129">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ae9a0-130">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (2), [**version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**révision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="ae9a0-130">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (2), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="ae9a0-131">Nom convivial du domaine de routage.</span><span class="sxs-lookup"><span data-stu-id="ae9a0-131">The routing domain friendly name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ae9a0-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ae9a0-132">Requirements</span></span>



| <span data-ttu-id="ae9a0-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ae9a0-133">Requirement</span></span> | <span data-ttu-id="ae9a0-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="ae9a0-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae9a0-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ae9a0-135">Minimum supported client</span></span><br/> | <span data-ttu-id="ae9a0-136">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="ae9a0-136">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="ae9a0-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ae9a0-137">Minimum supported server</span></span><br/> | <span data-ttu-id="ae9a0-138">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="ae9a0-138">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="ae9a0-139">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ae9a0-139">Namespace</span></span><br/>                | <span data-ttu-id="ae9a0-140">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="ae9a0-140">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ae9a0-141">MOF</span><span class="sxs-lookup"><span data-stu-id="ae9a0-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ae9a0-142"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ae9a0-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ae9a0-143">DLL</span><span class="sxs-lookup"><span data-stu-id="ae9a0-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae9a0-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ae9a0-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ae9a0-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ae9a0-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae9a0-146">**MSVM \_ EthernetSwitchPortFeatureSettingData**</span><span class="sxs-lookup"><span data-stu-id="ae9a0-146">**Msvm\_EthernetSwitchPortFeatureSettingData**</span></span>](msvm-ethernetswitchportfeaturesettingdata.md)
</dt> </dl>

 

