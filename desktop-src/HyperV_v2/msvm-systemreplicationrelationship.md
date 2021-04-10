---
description: Représente une association entre une instance de MSVM \_ ComputerSystem qui représente l’ordinateur virtuel et une instance de MSVM \_ ReplicationRelationship qui représente une relation de réplication de l’ordinateur virtuel.
ms.assetid: 23E7BF91-9527-434C-A571-05879E83950E
title: Classe Msvm_SystemReplicationRelationship
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemReplicationRelationship
- Msvm_SystemReplicationRelationship.Antecedent
- Msvm_SystemReplicationRelationship.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: dd5ada4eef811a7d542c01c0a3be66d53cca0916
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950992"
---
# <a name="msvm_systemreplicationrelationship-class"></a><span data-ttu-id="6ca4e-103">MSVM \_ SystemReplicationRelationship, classe</span><span class="sxs-lookup"><span data-stu-id="6ca4e-103">Msvm\_SystemReplicationRelationship class</span></span>

<span data-ttu-id="6ca4e-104">Représente une association entre une instance de [**MSVM \_ ComputerSystem**](msvm-computersystem.md) qui représente l’ordinateur virtuel et une instance de [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) qui représente une relation de réplication de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="6ca4e-104">Represents an association between an instance of [**Msvm\_ComputerSystem**](msvm-computersystem.md) that represents the virtual machine and an instance of [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) that represents a replication relationship of the virtual machine.</span></span> <span data-ttu-id="6ca4e-105">Cette classe dérive de la classe de [**\_ dépendance CIM**](/windows/desktop/CIMWin32Prov/cim-dependency) .</span><span class="sxs-lookup"><span data-stu-id="6ca4e-105">This class derives from the [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency) class.</span></span>

<span data-ttu-id="6ca4e-106">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="6ca4e-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ca4e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6ca4e-107">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SystemReplicationRelationship : CIM_Dependency
{
  Msvm_ComputerSystem          REF Antecedent;
  Msvm_ReplicationRelationship REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="6ca4e-108">Membres</span><span class="sxs-lookup"><span data-stu-id="6ca4e-108">Members</span></span>

<span data-ttu-id="6ca4e-109">La classe **MSVM \_ SystemReplicationRelationship** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="6ca4e-109">The **Msvm\_SystemReplicationRelationship** class has these types of members:</span></span>

-   [<span data-ttu-id="6ca4e-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6ca4e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6ca4e-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6ca4e-111">Properties</span></span>

<span data-ttu-id="6ca4e-112">La classe **MSVM \_ SystemReplicationRelationship** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="6ca4e-112">The **Msvm\_SystemReplicationRelationship** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6ca4e-113">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="6ca4e-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ca4e-114">Type de données : **MSVM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="6ca4e-114">Data type: **Msvm\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="6ca4e-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6ca4e-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ca4e-116">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ dependency. Antecedent")</span><span class="sxs-lookup"><span data-stu-id="6ca4e-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="6ca4e-117">Référence à l’instance de la classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) qui représente l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="6ca4e-117">Reference to the instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="6ca4e-118">**Charge**</span><span class="sxs-lookup"><span data-stu-id="6ca4e-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ca4e-119">Type de données : **MSVM \_ ReplicationRelationship**</span><span class="sxs-lookup"><span data-stu-id="6ca4e-119">Data type: **Msvm\_ReplicationRelationship**</span></span>
</dt> <dt>

<span data-ttu-id="6ca4e-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6ca4e-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ca4e-121">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dépendance CIM \_ . dependent")</span><span class="sxs-lookup"><span data-stu-id="6ca4e-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="6ca4e-122">Référence à l’instance de la classe [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) qui représente la relation de réplication d’un système virtuel.</span><span class="sxs-lookup"><span data-stu-id="6ca4e-122">Reference to the instance of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class that represents the replication relationship of a virtual system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6ca4e-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6ca4e-123">Requirements</span></span>



| <span data-ttu-id="6ca4e-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6ca4e-124">Requirement</span></span> | <span data-ttu-id="6ca4e-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="6ca4e-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ca4e-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6ca4e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="6ca4e-127">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6ca4e-127">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="6ca4e-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6ca4e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="6ca4e-129">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6ca4e-129">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6ca4e-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6ca4e-130">Namespace</span></span><br/>                | <span data-ttu-id="6ca4e-131">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="6ca4e-131">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6ca4e-132">MOF</span><span class="sxs-lookup"><span data-stu-id="6ca4e-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6ca4e-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6ca4e-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6ca4e-134">DLL</span><span class="sxs-lookup"><span data-stu-id="6ca4e-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ca4e-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6ca4e-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6ca4e-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6ca4e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ca4e-137">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="6ca4e-137">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

[<span data-ttu-id="6ca4e-138">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="6ca4e-138">**CIM\_Dependency**</span></span>](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> </dl>

 

