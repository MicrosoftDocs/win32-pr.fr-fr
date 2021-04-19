---
description: Associe une instance de la \_ classe MSVM ComputerSystem ou MSVM \_ PlannedComputerSystem représentant un système virtuel, avec une instance de la \_ classe VirtualSystemSettingData MSVM qui représente l’instantané du système virtuel qui est l’instantané le plus récent dans une branche de captures instantanées dépendantes.
ms.assetid: EEB9D2C1-C463-4EFE-862F-95E8AD8E1753
title: Classe Msvm_MostCurrentSnapshotInBranch
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MostCurrentSnapshotInBranch
- Msvm_MostCurrentSnapshotInBranch.Antecedent
- Msvm_MostCurrentSnapshotInBranch.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d3ed0824fd68670245e2c8d09b73733ff23be16b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106527698"
---
# <a name="msvm_mostcurrentsnapshotinbranch-class"></a><span data-ttu-id="8faf6-103">MSVM \_ MostCurrentSnapshotInBranch, classe</span><span class="sxs-lookup"><span data-stu-id="8faf6-103">Msvm\_MostCurrentSnapshotInBranch class</span></span>

<span data-ttu-id="8faf6-104">Associe une instance de la classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) ou [**MSVM \_ PlannedComputerSystem**](msvm-plannedcomputersystem.md) représentant un système virtuel, avec une instance de la classe [**\_ VirtualSystemSettingData MSVM**](msvm-virtualsystemsettingdata.md) qui représente l’instantané du système virtuel qui est l’instantané le plus récent dans une branche de captures instantanées dépendantes.</span><span class="sxs-lookup"><span data-stu-id="8faf6-104">Associates an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) or [**Msvm\_PlannedComputerSystem**](msvm-plannedcomputersystem.md) class representing a virtual system, with an instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class representing the virtual system snapshot that is the most current snapshot in a branch of dependent snapshots.</span></span>

<span data-ttu-id="8faf6-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="8faf6-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8faf6-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8faf6-106">Syntax</span></span>

``` syntax
[Association, Experimental, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MostCurrentSnapshotInBranch : CIM_MostCurrentSnapshotInBranch
{
  CIM_ComputerSystem            REF Antecedent;
  Msvm_VirtualSystemSettingData REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="8faf6-107">Membres</span><span class="sxs-lookup"><span data-stu-id="8faf6-107">Members</span></span>

<span data-ttu-id="8faf6-108">La classe **MSVM \_ MostCurrentSnapshotInBranch** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="8faf6-108">The **Msvm\_MostCurrentSnapshotInBranch** class has these types of members:</span></span>

-   [<span data-ttu-id="8faf6-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8faf6-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8faf6-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8faf6-110">Properties</span></span>

<span data-ttu-id="8faf6-111">La classe **MSVM \_ MostCurrentSnapshotInBranch** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="8faf6-111">The **Msvm\_MostCurrentSnapshotInBranch** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8faf6-112">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="8faf6-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8faf6-113">Type de données : **[ **CIM CIM \_**](/windows/desktop/CIMWin32Prov/cim-computersystem)**</span><span class="sxs-lookup"><span data-stu-id="8faf6-113">Data type: **[**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)**</span></span>
</dt> <dt>

<span data-ttu-id="8faf6-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8faf6-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8faf6-115">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="8faf6-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="8faf6-116">Référence à une instance de la classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) ou [**MSVM \_ PlannedComputerSystem**](msvm-plannedcomputersystem.md) représentant le système virtuel.</span><span class="sxs-lookup"><span data-stu-id="8faf6-116">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) or [**Msvm\_PlannedComputerSystem**](msvm-plannedcomputersystem.md) class representing the virtual system.</span></span> <span data-ttu-id="8faf6-117">Cette propriété est héritée de la [**\_ dépendance CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="8faf6-117">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="8faf6-118">**Charge**</span><span class="sxs-lookup"><span data-stu-id="8faf6-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8faf6-119">Type de données : **[ **MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="8faf6-119">Data type: **[**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="8faf6-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8faf6-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8faf6-121">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="8faf6-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="8faf6-122">Référence à une instance de la classe [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) qui représente l’instantané du système virtuel qui est l’instantané le plus récent dans une branche de captures instantanées dépendantes.</span><span class="sxs-lookup"><span data-stu-id="8faf6-122">A reference to an instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that represents the virtual system snapshot that is the most current snapshot in a branch of dependent snapshots.</span></span> <span data-ttu-id="8faf6-123">Cette propriété est héritée de la [**\_ dépendance CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="8faf6-123">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8faf6-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8faf6-124">Requirements</span></span>



| <span data-ttu-id="8faf6-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8faf6-125">Requirement</span></span> | <span data-ttu-id="8faf6-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="8faf6-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8faf6-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8faf6-127">Minimum supported client</span></span><br/> | <span data-ttu-id="8faf6-128">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8faf6-128">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="8faf6-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8faf6-129">Minimum supported server</span></span><br/> | <span data-ttu-id="8faf6-130">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8faf6-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8faf6-131">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8faf6-131">Namespace</span></span><br/>                | <span data-ttu-id="8faf6-132">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="8faf6-132">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="8faf6-133">MOF</span><span class="sxs-lookup"><span data-stu-id="8faf6-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8faf6-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8faf6-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8faf6-135">DLL</span><span class="sxs-lookup"><span data-stu-id="8faf6-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8faf6-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8faf6-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

