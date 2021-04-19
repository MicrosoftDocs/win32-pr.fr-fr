---
description: Représente une association entre un système virtuel et l’instantané le plus récent du système. Cette association ne peut exister que si le système virtuel a été créé à l’aide d’un instantané ou si un instantané a été créé à partir du système virtuel.
ms.assetid: e6040818-84cf-4cec-ab7b-a733fe5d01d2
title: Classe CIM_MostCurrentSnapshotInBranch
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MostCurrentSnapshotInBranch
- CIM_MostCurrentSnapshotInBranch.Antecedent
- CIM_MostCurrentSnapshotInBranch.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 078a7c9f1669a2aa0449dce01022eba0eadcb2c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106538669"
---
# <a name="cim_mostcurrentsnapshotinbranch-class"></a><span data-ttu-id="baca2-104">\_Classe CIM MostCurrentSnapshotInBranch</span><span class="sxs-lookup"><span data-stu-id="baca2-104">CIM\_MostCurrentSnapshotInBranch class</span></span>

<span data-ttu-id="baca2-105">Représente une association entre un système virtuel et l’instantané le plus récent du système.</span><span class="sxs-lookup"><span data-stu-id="baca2-105">Represents an association between a virtual system and the most current snapshot of the system.</span></span> <span data-ttu-id="baca2-106">Cette association ne peut exister que si le système virtuel a été créé à l’aide d’un instantané ou si un instantané a été créé à partir du système virtuel.</span><span class="sxs-lookup"><span data-stu-id="baca2-106">This association can only exist if the virtual system was create using a snapshot or if a snapshot was created from the virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="baca2-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="baca2-107">Syntax</span></span>

``` syntax
[Association, Experimental, Version("2.16.0"), AMENDMENT]
class CIM_MostCurrentSnapshotInBranch : CIM_Dependency
{
  CIM_ComputerSystem           REF Antecedent;
  CIM_VirtualSystemSettingData REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="baca2-108">Membres</span><span class="sxs-lookup"><span data-stu-id="baca2-108">Members</span></span>

<span data-ttu-id="baca2-109">La classe **CIM \_ MostCurrentSnapshotInBranch** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="baca2-109">The **CIM\_MostCurrentSnapshotInBranch** class has these types of members:</span></span>

-   [<span data-ttu-id="baca2-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="baca2-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="baca2-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="baca2-111">Properties</span></span>

<span data-ttu-id="baca2-112">La classe **CIM \_ MostCurrentSnapshotInBranch** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="baca2-112">The **CIM\_MostCurrentSnapshotInBranch** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="baca2-113">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="baca2-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="baca2-114">Type de données **: \_ CIM CIM**</span><span class="sxs-lookup"><span data-stu-id="baca2-114">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="baca2-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="baca2-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="baca2-116">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="baca2-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="baca2-117">Référence à l’instance de [**CIM CIM \_**](cim-computersystem.md) qui représente le système virtuel.</span><span class="sxs-lookup"><span data-stu-id="baca2-117">A reference to the instance of [**CIM\_ComputerSystem**](cim-computersystem.md) that represents the virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="baca2-118">**Charge**</span><span class="sxs-lookup"><span data-stu-id="baca2-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="baca2-119">Type de données : **CIM \_ VirtualSystemSettingData**</span><span class="sxs-lookup"><span data-stu-id="baca2-119">Data type: **CIM\_VirtualSystemSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="baca2-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="baca2-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="baca2-121">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="baca2-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="baca2-122">Référence à l’instance de [**\_ VirtualSystemSettingData CIM**](cim-virtualsystemsettingdata.md) qui représente l’instantané du système virtuel.</span><span class="sxs-lookup"><span data-stu-id="baca2-122">A reference to the instance of [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) that represents the virtual system snapshot.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="baca2-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="baca2-123">Requirements</span></span>



| <span data-ttu-id="baca2-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="baca2-124">Requirement</span></span> | <span data-ttu-id="baca2-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="baca2-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="baca2-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="baca2-126">Minimum supported client</span></span><br/> | <span data-ttu-id="baca2-127">Windows 8</span><span class="sxs-lookup"><span data-stu-id="baca2-127">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="baca2-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="baca2-128">Minimum supported server</span></span><br/> | <span data-ttu-id="baca2-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="baca2-129">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="baca2-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="baca2-130">Namespace</span></span><br/>                | <span data-ttu-id="baca2-131">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="baca2-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="baca2-132">MOF</span><span class="sxs-lookup"><span data-stu-id="baca2-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="baca2-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="baca2-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="baca2-134">DLL</span><span class="sxs-lookup"><span data-stu-id="baca2-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="baca2-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="baca2-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="baca2-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="baca2-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="baca2-137">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="baca2-137">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

