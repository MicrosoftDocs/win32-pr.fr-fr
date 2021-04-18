---
description: Association qui connecte un service de commutateur virtuel à un service de pontage transparent.
ms.assetid: 4DFD73CA-38F0-4C06-BEBE-C684590E50E8
title: Classe Msvm_HostedSwitchService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HostedSwitchService
- Msvm_HostedSwitchService.Antecedent
- Msvm_HostedSwitchService.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f0b7319dbe58649ac7abce2d36201f3984c1b807
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516422"
---
# <a name="msvm_hostedswitchservice-class"></a><span data-ttu-id="9581f-103">MSVM \_ HostedSwitchService, classe</span><span class="sxs-lookup"><span data-stu-id="9581f-103">Msvm\_HostedSwitchService class</span></span>

<span data-ttu-id="9581f-104">Association qui connecte un service de commutateur virtuel à un service de pontage transparent.</span><span class="sxs-lookup"><span data-stu-id="9581f-104">An association that connects a virtual switch service to a transparent bridging service.</span></span>

<span data-ttu-id="9581f-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="9581f-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9581f-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9581f-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HostedSwitchService : CIM_HostedService
{
  Msvm_VirtualEthernetSwitch REF Antecedent;
  CIM_Service                REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="9581f-107">Membres</span><span class="sxs-lookup"><span data-stu-id="9581f-107">Members</span></span>

<span data-ttu-id="9581f-108">La classe **MSVM \_ HostedSwitchService** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="9581f-108">The **Msvm\_HostedSwitchService** class has these types of members:</span></span>

-   [<span data-ttu-id="9581f-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9581f-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9581f-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9581f-110">Properties</span></span>

<span data-ttu-id="9581f-111">La classe **MSVM \_ HostedSwitchService** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="9581f-111">The **Msvm\_HostedSwitchService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9581f-112">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="9581f-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9581f-113">Type de données : **[ **MSVM \_ VirtualEthernetSwitch**](msvm-virtualethernetswitch.md)**</span><span class="sxs-lookup"><span data-stu-id="9581f-113">Data type: **[**Msvm\_VirtualEthernetSwitch**](msvm-virtualethernetswitch.md)**</span></span>
</dt> <dt>

<span data-ttu-id="9581f-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9581f-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9581f-115">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="9581f-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="9581f-116">Référence à une instance de la classe [**MSVM \_ VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) qui représente le commutateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="9581f-116">A reference to an instance of the [**Msvm\_VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) class that represents the virtual switch.</span></span>

</dd> <dt>

<span data-ttu-id="9581f-117">**Charge**</span><span class="sxs-lookup"><span data-stu-id="9581f-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9581f-118">Type de données : **[ **\_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service)**</span><span class="sxs-lookup"><span data-stu-id="9581f-118">Data type: **[**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service)**</span></span>
</dt> <dt>

<span data-ttu-id="9581f-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9581f-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9581f-120">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="9581f-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="9581f-121">Référence à une instance de la classe [**MSVM \_ TransparentBridgingService**](msvm-transparentbridgingservice.md) qui représente le service de pontage.</span><span class="sxs-lookup"><span data-stu-id="9581f-121">A reference to an instance of the [**Msvm\_TransparentBridgingService**](msvm-transparentbridgingservice.md) class that represents the bridging service.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9581f-122">Notes</span><span class="sxs-lookup"><span data-stu-id="9581f-122">Remarks</span></span>

<span data-ttu-id="9581f-123">L’accès à la classe **MSVM \_ HostedSwitchService** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="9581f-123">Access to the **Msvm\_HostedSwitchService** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="9581f-124">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="9581f-124">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="9581f-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9581f-125">Requirements</span></span>



| <span data-ttu-id="9581f-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9581f-126">Requirement</span></span> | <span data-ttu-id="9581f-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="9581f-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9581f-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9581f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9581f-129">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9581f-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="9581f-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9581f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9581f-131">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9581f-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9581f-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9581f-132">Namespace</span></span><br/>                | <span data-ttu-id="9581f-133">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="9581f-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9581f-134">MOF</span><span class="sxs-lookup"><span data-stu-id="9581f-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9581f-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9581f-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9581f-136">DLL</span><span class="sxs-lookup"><span data-stu-id="9581f-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9581f-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9581f-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9581f-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9581f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9581f-139">**\_Service hébergé CIM**</span><span class="sxs-lookup"><span data-stu-id="9581f-139">**CIM\_HostedService**</span></span>](cim-hostedservice.md)
</dt> <dt>

[<span data-ttu-id="9581f-140">**\_Service hébergé CIM**</span><span class="sxs-lookup"><span data-stu-id="9581f-140">**CIM\_HostedService**</span></span>](/windows/desktop/CIMWin32Prov/cim-hostedservice)
</dt> </dl>

 

