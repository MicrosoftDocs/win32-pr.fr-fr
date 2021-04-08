---
description: Associe le \_ VirtualSystemReferencePoint MSVM aux objets MSVM \_ VirtualSystem correspondants.
ms.assetid: 5a9cb099-c0ae-4088-a64c-f2720a6cb9c8
title: Classe Msvm_ReferencePointOfVirtualSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReferencePointOfVirtualSystem
- Msvm_ReferencePointOfVirtualSystem.Antecedent
- Msvm_ReferencePointOfVirtualSystem.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8debe1931154c5c7a7868e8ee301daf977076b57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103756897"
---
# <a name="msvm_referencepointofvirtualsystem-class"></a><span data-ttu-id="76563-103">MSVM \_ ReferencePointOfVirtualSystem, classe</span><span class="sxs-lookup"><span data-stu-id="76563-103">Msvm\_ReferencePointOfVirtualSystem class</span></span>

<span data-ttu-id="76563-104">Associe [**le \_ VirtualSystemReferencePoint MSVM**](msvm-virtualsystemreferencepoint.md) aux objets [**MSVM \_ VirtualSystem**](msvm-virtualsystemresourcecomponent.md) correspondants.</span><span class="sxs-lookup"><span data-stu-id="76563-104">Associates the [**Msvm\_VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) to the corresponding [**Msvm\_VirtualSystem**](msvm-virtualsystemresourcecomponent.md) objects.</span></span>

<span data-ttu-id="76563-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="76563-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="76563-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="76563-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReferencePointOfVirtualSystem : CIM_Dependency
{
  Msvm_ComputerSystem              REF Antecedent;
  Msvm_VirtualSystemReferencePoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="76563-107">Membres</span><span class="sxs-lookup"><span data-stu-id="76563-107">Members</span></span>

<span data-ttu-id="76563-108">La classe **MSVM \_ ReferencePointOfVirtualSystem** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="76563-108">The **Msvm\_ReferencePointOfVirtualSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="76563-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="76563-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="76563-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="76563-110">Properties</span></span>

<span data-ttu-id="76563-111">La classe **MSVM \_ ReferencePointOfVirtualSystem** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="76563-111">The **Msvm\_ReferencePointOfVirtualSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="76563-112">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="76563-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76563-113">Type de données : **MSVM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="76563-113">Data type: **Msvm\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="76563-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76563-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76563-115">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="76563-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="76563-116">[**MSVM \_ ComputerSystem**](msvm-computersystem.md) qui représente l’objet indépendant dans cette association.</span><span class="sxs-lookup"><span data-stu-id="76563-116">An [**Msvm\_ComputerSystem**](msvm-computersystem.md) that represents the independent object in this association.</span></span>

</dd> <dt>

<span data-ttu-id="76563-117">**Charge**</span><span class="sxs-lookup"><span data-stu-id="76563-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76563-118">Type de données : **MSVM \_ VirtualSystemReferencePoint**</span><span class="sxs-lookup"><span data-stu-id="76563-118">Data type: **Msvm\_VirtualSystemReferencePoint**</span></span>
</dt> <dt>

<span data-ttu-id="76563-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76563-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76563-120">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) (« dépendant »)</span><span class="sxs-lookup"><span data-stu-id="76563-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="76563-121">[**MSVM \_ VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) qui représente l’objet dépendant de l' **antécédent**.</span><span class="sxs-lookup"><span data-stu-id="76563-121">An [**Msvm\_VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) that represents the object that is dependent on the **Antecedent**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="76563-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="76563-122">Requirements</span></span>



| <span data-ttu-id="76563-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="76563-123">Requirement</span></span> | <span data-ttu-id="76563-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="76563-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76563-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="76563-125">Minimum supported client</span></span><br/> | <span data-ttu-id="76563-126">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="76563-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="76563-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="76563-127">Minimum supported server</span></span><br/> | <span data-ttu-id="76563-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="76563-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="76563-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="76563-129">Namespace</span></span><br/>                | <span data-ttu-id="76563-130">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="76563-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="76563-131">MOF</span><span class="sxs-lookup"><span data-stu-id="76563-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="76563-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="76563-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="76563-133">DLL</span><span class="sxs-lookup"><span data-stu-id="76563-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="76563-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="76563-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="76563-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="76563-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76563-136">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="76563-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

