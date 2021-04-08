---
description: Représente les paramètres d’association de cartes réseau du commutateur.
ms.assetid: 7a48bdae-1953-4011-aaa8-1e3ca73494ff
title: Classe Msvm_VirtualEthernetSwitchNicTeamingSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchNicTeamingSettingData
- Msvm_VirtualEthernetSwitchNicTeamingSettingData.TeamingMode
- Msvm_VirtualEthernetSwitchNicTeamingSettingData.LoadBalancingAlgorithm
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 45f306f9ddb388ef4e8124d7ab2c8dd125a62e01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760851"
---
# <a name="msvm_virtualethernetswitchnicteamingsettingdata-class"></a><span data-ttu-id="0e011-103">MSVM \_ VirtualEthernetSwitchNicTeamingSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="0e011-103">Msvm\_VirtualEthernetSwitchNicTeamingSettingData class</span></span>

<span data-ttu-id="0e011-104">Représente les paramètres d’association de cartes réseau du commutateur.</span><span class="sxs-lookup"><span data-stu-id="0e011-104">Represents the switch nic teaming settings.</span></span>

<span data-ttu-id="0e011-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="0e011-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e011-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0e011-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("17AD26F1-DD6F-4ED9-BD2F-3750ADE6B68B"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Nic Teaming Settings"), AMENDMENT]
class Msvm_VirtualEthernetSwitchNicTeamingSettingData : Msvm_EthernetSwitchFeatureSettingData
{
  UINT32 TeamingMode = 0;
  UINT32 LoadBalancingAlgorithm = 5;
};
```

## <a name="members"></a><span data-ttu-id="0e011-107">Membres</span><span class="sxs-lookup"><span data-stu-id="0e011-107">Members</span></span>

<span data-ttu-id="0e011-108">La classe **MSVM \_ VirtualEthernetSwitchNicTeamingSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="0e011-108">The **Msvm\_VirtualEthernetSwitchNicTeamingSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="0e011-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0e011-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0e011-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0e011-110">Properties</span></span>

<span data-ttu-id="0e011-111">La classe **MSVM \_ VirtualEthernetSwitchNicTeamingSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="0e011-111">The **Msvm\_VirtualEthernetSwitchNicTeamingSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0e011-112">**LoadBalancingAlgorithm**</span><span class="sxs-lookup"><span data-stu-id="0e011-112">**LoadBalancingAlgorithm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e011-113">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0e011-113">Data type: **UINT32**</span></span>
</dt> <dt>

<span data-ttu-id="0e011-114">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0e011-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0e011-115">Qualificateurs : **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="0e011-115">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="0e011-116">Algorithme d’équilibrage de charge.</span><span class="sxs-lookup"><span data-stu-id="0e011-116">The load balancing algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="0e011-117">**TeamingMode**</span><span class="sxs-lookup"><span data-stu-id="0e011-117">**TeamingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e011-118">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0e011-118">Data type: **UINT32**</span></span>
</dt> <dt>

<span data-ttu-id="0e011-119">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0e011-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0e011-120">Qualificateurs : **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="0e011-120">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="0e011-121">Mode d’association.</span><span class="sxs-lookup"><span data-stu-id="0e011-121">The teaming mode.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0e011-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0e011-122">Requirements</span></span>



| <span data-ttu-id="0e011-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0e011-123">Requirement</span></span> | <span data-ttu-id="0e011-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e011-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e011-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e011-125">Minimum supported client</span></span><br/> | <span data-ttu-id="0e011-126">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0e011-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="0e011-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e011-127">Minimum supported server</span></span><br/> | <span data-ttu-id="0e011-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="0e011-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="0e011-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0e011-129">Namespace</span></span><br/>                | <span data-ttu-id="0e011-130">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="0e011-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0e011-131">MOF</span><span class="sxs-lookup"><span data-stu-id="0e011-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0e011-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0e011-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0e011-133">DLL</span><span class="sxs-lookup"><span data-stu-id="0e011-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e011-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0e011-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0e011-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e011-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e011-136">**MSVM \_ EthernetSwitchFeatureSettingData**</span><span class="sxs-lookup"><span data-stu-id="0e011-136">**Msvm\_EthernetSwitchFeatureSettingData**</span></span>](msvm-ethernetswitchfeaturesettingdata.md)
</dt> </dl>

 

 




