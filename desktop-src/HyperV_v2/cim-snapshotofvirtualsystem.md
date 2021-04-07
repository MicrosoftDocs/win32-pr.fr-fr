---
description: Associe un système virtuel à un instantané du système virtuel.
ms.assetid: f85f6914-dbb8-42c9-a732-11d48613c15c
title: Classe CIM_SnapshotOfVirtualSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SnapshotOfVirtualSystem
- CIM_SnapshotOfVirtualSystem.Antecedent
- CIM_SnapshotOfVirtualSystem.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6e8e0929f1198ececea5ea5ec144e2f7313ec35c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952415"
---
# <a name="cim_snapshotofvirtualsystem-class"></a><span data-ttu-id="507e3-103">\_Classe CIM SnapshotOfVirtualSystem</span><span class="sxs-lookup"><span data-stu-id="507e3-103">CIM\_SnapshotOfVirtualSystem class</span></span>

<span data-ttu-id="507e3-104">Associe un système virtuel à un instantané du système virtuel.</span><span class="sxs-lookup"><span data-stu-id="507e3-104">Associates a virtual system a snapshot of the virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="507e3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="507e3-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.22.0"), AMENDMENT]
class CIM_SnapshotOfVirtualSystem : CIM_Dependency
{
  CIM_ComputerSystem           REF Antecedent;
  CIM_VirtualSystemSettingData REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="507e3-106">Membres</span><span class="sxs-lookup"><span data-stu-id="507e3-106">Members</span></span>

<span data-ttu-id="507e3-107">La classe **CIM \_ SnapshotOfVirtualSystem** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="507e3-107">The **CIM\_SnapshotOfVirtualSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="507e3-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="507e3-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="507e3-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="507e3-109">Properties</span></span>

<span data-ttu-id="507e3-110">La classe **CIM \_ SnapshotOfVirtualSystem** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="507e3-110">The **CIM\_SnapshotOfVirtualSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="507e3-111">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="507e3-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="507e3-112">Type de données **: \_ CIM CIM**</span><span class="sxs-lookup"><span data-stu-id="507e3-112">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="507e3-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="507e3-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="507e3-114">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="507e3-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="507e3-115">Référence au système informatique qui représente le système virtuel.</span><span class="sxs-lookup"><span data-stu-id="507e3-115">A reference to the computer system that represents the virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="507e3-116">**Charge**</span><span class="sxs-lookup"><span data-stu-id="507e3-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="507e3-117">Type de données : **CIM \_ VirtualSystemSettingData**</span><span class="sxs-lookup"><span data-stu-id="507e3-117">Data type: **CIM\_VirtualSystemSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="507e3-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="507e3-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="507e3-119">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="507e3-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="507e3-120">Référence à l’objet de données de paramètres qui représente l’instantané du système virtuel.</span><span class="sxs-lookup"><span data-stu-id="507e3-120">A reference to the settings data object that represents the snapshot of the virtual system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="507e3-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="507e3-121">Requirements</span></span>



| <span data-ttu-id="507e3-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="507e3-122">Requirement</span></span> | <span data-ttu-id="507e3-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="507e3-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="507e3-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="507e3-124">Minimum supported client</span></span><br/> | <span data-ttu-id="507e3-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="507e3-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="507e3-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="507e3-126">Minimum supported server</span></span><br/> | <span data-ttu-id="507e3-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="507e3-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="507e3-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="507e3-128">Namespace</span></span><br/>                | <span data-ttu-id="507e3-129">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="507e3-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="507e3-130">MOF</span><span class="sxs-lookup"><span data-stu-id="507e3-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="507e3-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="507e3-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="507e3-132">DLL</span><span class="sxs-lookup"><span data-stu-id="507e3-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="507e3-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="507e3-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="507e3-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="507e3-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="507e3-135">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="507e3-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

