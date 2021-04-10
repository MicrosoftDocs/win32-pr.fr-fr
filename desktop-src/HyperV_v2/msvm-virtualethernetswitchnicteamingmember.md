---
description: Représente l’association entre un ExternalEthernetPort d’équipe et un ExternalEthernetPort membre.
ms.assetid: e21bea94-d6a8-4788-958e-78ce255837aa
title: Classe Msvm_VirtualEthernetSwitchNicTeamingMember
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchNicTeamingMember
- Msvm_VirtualEthernetSwitchNicTeamingMember.Antecedent
- Msvm_VirtualEthernetSwitchNicTeamingMember.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cbf83f4605d6ab1b7bc9740b14c493393eb93163
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104211104"
---
# <a name="msvm_virtualethernetswitchnicteamingmember-class"></a><span data-ttu-id="21bfd-103">MSVM \_ VirtualEthernetSwitchNicTeamingMember, classe</span><span class="sxs-lookup"><span data-stu-id="21bfd-103">Msvm\_VirtualEthernetSwitchNicTeamingMember class</span></span>

<span data-ttu-id="21bfd-104">Représente l’association entre un ExternalEthernetPort d’équipe et un ExternalEthernetPort membre.</span><span class="sxs-lookup"><span data-stu-id="21bfd-104">Represents the association between a team ExternalEthernetPort and a member ExternalEthernetPort.</span></span>

<span data-ttu-id="21bfd-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="21bfd-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="21bfd-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="21bfd-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualEthernetSwitchNicTeamingMember : CIM_Dependency
{
  Msvm_ExternalEthernetPort REF Antecedent;
  Msvm_ExternalEthernetPort REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="21bfd-107">Membres</span><span class="sxs-lookup"><span data-stu-id="21bfd-107">Members</span></span>

<span data-ttu-id="21bfd-108">La classe **MSVM \_ VirtualEthernetSwitchNicTeamingMember** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="21bfd-108">The **Msvm\_VirtualEthernetSwitchNicTeamingMember** class has these types of members:</span></span>

-   [<span data-ttu-id="21bfd-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="21bfd-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="21bfd-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="21bfd-110">Properties</span></span>

<span data-ttu-id="21bfd-111">La classe **MSVM \_ VirtualEthernetSwitchNicTeamingMember** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="21bfd-111">The **Msvm\_VirtualEthernetSwitchNicTeamingMember** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="21bfd-112">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="21bfd-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21bfd-113">Type de données : **MSVM \_ ExternalEthernetPort**</span><span class="sxs-lookup"><span data-stu-id="21bfd-113">Data type: **Msvm\_ExternalEthernetPort**</span></span>
</dt> <dt>

<span data-ttu-id="21bfd-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="21bfd-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21bfd-115">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="21bfd-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="21bfd-116">Un [**\_ ExternalEthernetPort MSVM**](msvm-externalethernetport.md) qui fait référence à l’instance de port externe externe de l’équipe.</span><span class="sxs-lookup"><span data-stu-id="21bfd-116">An [**Msvm\_ExternalEthernetPort**](msvm-externalethernetport.md) that references the team external ethernet port instance.</span></span>

</dd> <dt>

<span data-ttu-id="21bfd-117">**Charge**</span><span class="sxs-lookup"><span data-stu-id="21bfd-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21bfd-118">Type de données : **MSVM \_ ExternalEthernetPort**</span><span class="sxs-lookup"><span data-stu-id="21bfd-118">Data type: **Msvm\_ExternalEthernetPort**</span></span>
</dt> <dt>

<span data-ttu-id="21bfd-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="21bfd-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21bfd-120">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="21bfd-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="21bfd-121">Référence à l’instance [**MSVM \_ ExternalEthernetPort**](msvm-externalethernetport.md) membre.</span><span class="sxs-lookup"><span data-stu-id="21bfd-121">Reference to the member [**Msvm\_ExternalEthernetPort**](msvm-externalethernetport.md) instance.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="21bfd-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="21bfd-122">Requirements</span></span>



| <span data-ttu-id="21bfd-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="21bfd-123">Requirement</span></span> | <span data-ttu-id="21bfd-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="21bfd-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21bfd-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="21bfd-125">Minimum supported client</span></span><br/> | <span data-ttu-id="21bfd-126">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="21bfd-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="21bfd-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="21bfd-127">Minimum supported server</span></span><br/> | <span data-ttu-id="21bfd-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="21bfd-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="21bfd-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="21bfd-129">Namespace</span></span><br/>                | <span data-ttu-id="21bfd-130">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="21bfd-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="21bfd-131">MOF</span><span class="sxs-lookup"><span data-stu-id="21bfd-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="21bfd-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="21bfd-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="21bfd-133">DLL</span><span class="sxs-lookup"><span data-stu-id="21bfd-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21bfd-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="21bfd-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="21bfd-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="21bfd-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21bfd-136">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="21bfd-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

