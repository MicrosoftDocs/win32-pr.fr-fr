---
description: Représente une association entre une instance de la classe CIM CIM \_ qui représente le réplica d’ordinateur virtuel et une instance de la \_ classe ComputerSystem CIM qui représente le réplica de machine virtuelle de test.
ms.assetid: c3216ddd-7f70-4287-9f7e-1fd7a60b1a0a
title: Classe Msvm_ReplicaSystemDependency
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicaSystemDependency
- Msvm_ReplicaSystemDependency.Antecedent
- Msvm_ReplicaSystemDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d8c0db6e476cb883ee1179fcfcc9ac4b212f0b09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203080"
---
# <a name="msvm_replicasystemdependency-class"></a><span data-ttu-id="f1ed1-103">MSVM \_ ReplicaSystemDependency, classe</span><span class="sxs-lookup"><span data-stu-id="f1ed1-103">Msvm\_ReplicaSystemDependency class</span></span>

<span data-ttu-id="f1ed1-104">Représente une association entre une instance de la [**classe \_ CIM CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) qui représente le réplica d’ordinateur virtuel et une instance de la classe **\_ ComputerSystem CIM** qui représente le réplica de machine virtuelle de test.</span><span class="sxs-lookup"><span data-stu-id="f1ed1-104">Represents an association between an instance of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class that represents the virtual machine replica and an instance of the **CIM\_ComputerSystem** class that represents the test virtual machine replica.</span></span>

<span data-ttu-id="f1ed1-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="f1ed1-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1ed1-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f1ed1-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicaSystemDependency : CIM_Dependency
{
  CIM_ComputerSystem REF Antecedent;
  CIM_ComputerSystem REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="f1ed1-107">Membres</span><span class="sxs-lookup"><span data-stu-id="f1ed1-107">Members</span></span>

<span data-ttu-id="f1ed1-108">La classe **MSVM \_ ReplicaSystemDependency** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="f1ed1-108">The **Msvm\_ReplicaSystemDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="f1ed1-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f1ed1-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f1ed1-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f1ed1-110">Properties</span></span>

<span data-ttu-id="f1ed1-111">La classe **MSVM \_ ReplicaSystemDependency** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="f1ed1-111">The **Msvm\_ReplicaSystemDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f1ed1-112">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="f1ed1-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1ed1-113">Type de données **: \_ CIM CIM**</span><span class="sxs-lookup"><span data-stu-id="f1ed1-113">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="f1ed1-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1ed1-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1ed1-115">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ dependency. Antecedent")</span><span class="sxs-lookup"><span data-stu-id="f1ed1-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="f1ed1-116">Référence à une instance de la classe [**CIM \_ CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) qui représente le réplica de machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="f1ed1-116">A reference to an instance of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class that represents the virtual machine replica.</span></span> <span data-ttu-id="f1ed1-117">Cette propriété est héritée de la [**\_ dépendance CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="f1ed1-117">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="f1ed1-118">**Charge**</span><span class="sxs-lookup"><span data-stu-id="f1ed1-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1ed1-119">Type de données **: \_ CIM CIM**</span><span class="sxs-lookup"><span data-stu-id="f1ed1-119">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="f1ed1-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1ed1-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1ed1-121">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dépendance CIM \_ . dependent")</span><span class="sxs-lookup"><span data-stu-id="f1ed1-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="f1ed1-122">Référence à une instance de la classe [**CIM \_ CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) qui représente le réplica de machine virtuelle de test créé par la méthode [**MSVM \_ ReplicationService. TestReplicaSystem**](testreplicasystem-msvm-replicationservice.md) .</span><span class="sxs-lookup"><span data-stu-id="f1ed1-122">A reference to an instance of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class that represents the test virtual machine replica created by the [**Msvm\_ReplicationService.TestReplicaSystem**](testreplicasystem-msvm-replicationservice.md) method.</span></span> <span data-ttu-id="f1ed1-123">Cette propriété est héritée de la [**\_ dépendance CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="f1ed1-123">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f1ed1-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f1ed1-124">Requirements</span></span>



| <span data-ttu-id="f1ed1-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f1ed1-125">Requirement</span></span> | <span data-ttu-id="f1ed1-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1ed1-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1ed1-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f1ed1-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f1ed1-128">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f1ed1-128">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f1ed1-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f1ed1-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f1ed1-130">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f1ed1-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f1ed1-131">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f1ed1-131">Namespace</span></span><br/>                | <span data-ttu-id="f1ed1-132">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="f1ed1-132">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f1ed1-133">MOF</span><span class="sxs-lookup"><span data-stu-id="f1ed1-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f1ed1-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f1ed1-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f1ed1-135">DLL</span><span class="sxs-lookup"><span data-stu-id="f1ed1-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1ed1-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f1ed1-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

