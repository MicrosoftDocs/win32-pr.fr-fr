---
description: Définit l’association entre un commutateur Ethernet et une ressource de commutateur.
ms.assetid: fb29f4cb-50c4-4865-b267-21ff99bb4a8b
title: Classe Msvm_EthernetSwitchInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchInfo
- Msvm_EthernetSwitchInfo.Antecedent
- Msvm_EthernetSwitchInfo.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1106e0930716572b10a95846865d8f90aa991cc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953261"
---
# <a name="msvm_ethernetswitchinfo-class"></a><span data-ttu-id="3d06b-103">MSVM \_ EthernetSwitchInfo, classe</span><span class="sxs-lookup"><span data-stu-id="3d06b-103">Msvm\_EthernetSwitchInfo class</span></span>

<span data-ttu-id="3d06b-104">Définit l’association entre un commutateur Ethernet et une ressource de commutateur.</span><span class="sxs-lookup"><span data-stu-id="3d06b-104">Defines the association between an Ethernet switch and a switch resource.</span></span>

<span data-ttu-id="3d06b-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="3d06b-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d06b-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3d06b-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetSwitchInfo : CIM_Dependency
{
  Msvm_VirtualEthernetSwitch REF Antecedent;
  Msvm_EthernetSwitchData    REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="3d06b-107">Membres</span><span class="sxs-lookup"><span data-stu-id="3d06b-107">Members</span></span>

<span data-ttu-id="3d06b-108">La classe **MSVM \_ EthernetSwitchInfo** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="3d06b-108">The **Msvm\_EthernetSwitchInfo** class has these types of members:</span></span>

-   [<span data-ttu-id="3d06b-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3d06b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3d06b-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3d06b-110">Properties</span></span>

<span data-ttu-id="3d06b-111">La classe **MSVM \_ EthernetSwitchInfo** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="3d06b-111">The **Msvm\_EthernetSwitchInfo** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3d06b-112">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="3d06b-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d06b-113">Type de données : **MSVM \_ VirtualEthernetSwitch**</span><span class="sxs-lookup"><span data-stu-id="3d06b-113">Data type: **Msvm\_VirtualEthernetSwitch**</span></span>
</dt> <dt>

<span data-ttu-id="3d06b-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3d06b-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d06b-115">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="3d06b-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="3d06b-116">Référence à la classe [**MSVM \_ VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) qui représente le système d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="3d06b-116">A reference to the [**Msvm\_VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) class that represents the hosting system.</span></span> <span data-ttu-id="3d06b-117">Cette propriété est dérivée de la [**\_ dépendance CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="3d06b-117">This property is derived from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="3d06b-118">**Charge**</span><span class="sxs-lookup"><span data-stu-id="3d06b-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d06b-119">Type de données : **MSVM \_ EthernetSwitchData**</span><span class="sxs-lookup"><span data-stu-id="3d06b-119">Data type: **Msvm\_EthernetSwitchData**</span></span>
</dt> <dt>

<span data-ttu-id="3d06b-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3d06b-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d06b-121">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="3d06b-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="3d06b-122">Référence à la classe [**MSVM \_ EthernetSwitchData**](msvm-ethernetswitchdata.md) qui représente la ressource Switch.</span><span class="sxs-lookup"><span data-stu-id="3d06b-122">A reference to the [**Msvm\_EthernetSwitchData**](msvm-ethernetswitchdata.md) class that represents the switch resource.</span></span> <span data-ttu-id="3d06b-123">Cette propriété est dérivée de la [**\_ dépendance CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="3d06b-123">This property is derived from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3d06b-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3d06b-124">Requirements</span></span>



| <span data-ttu-id="3d06b-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3d06b-125">Requirement</span></span> | <span data-ttu-id="3d06b-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="3d06b-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d06b-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3d06b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="3d06b-128">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3d06b-128">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3d06b-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3d06b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="3d06b-130">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3d06b-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3d06b-131">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3d06b-131">Namespace</span></span><br/>                | <span data-ttu-id="3d06b-132">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="3d06b-132">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3d06b-133">MOF</span><span class="sxs-lookup"><span data-stu-id="3d06b-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3d06b-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3d06b-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3d06b-135">DLL</span><span class="sxs-lookup"><span data-stu-id="3d06b-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d06b-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3d06b-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

