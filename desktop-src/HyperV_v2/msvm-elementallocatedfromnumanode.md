---
description: Associe une instance d’une ressource allouée au nœud NUMA physique à partir duquel elle a été allouée.
ms.assetid: 811ed19f-9084-4e30-8604-860d2bf722c7
title: Classe Msvm_ElementAllocatedFromNumaNode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ElementAllocatedFromNumaNode
- Msvm_ElementAllocatedFromNumaNode.Antecedent
- Msvm_ElementAllocatedFromNumaNode.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 98940306f25d46c6af1be31133ee336765f8f1a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866406"
---
# <a name="msvm_elementallocatedfromnumanode-class"></a><span data-ttu-id="3041e-103">MSVM \_ ElementAllocatedFromNumaNode, classe</span><span class="sxs-lookup"><span data-stu-id="3041e-103">Msvm\_ElementAllocatedFromNumaNode class</span></span>

<span data-ttu-id="3041e-104">Associe une instance d’une ressource allouée au nœud NUMA physique à partir duquel elle a été allouée.</span><span class="sxs-lookup"><span data-stu-id="3041e-104">Associates an instance of an allocated resource with the physical NUMA node from which it was allocated.</span></span>

<span data-ttu-id="3041e-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="3041e-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3041e-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3041e-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ElementAllocatedFromNumaNode : CIM_Dependency
{
  Msvm_NumaNode      REF Antecedent;
  CIM_LogicalElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="3041e-107">Membres</span><span class="sxs-lookup"><span data-stu-id="3041e-107">Members</span></span>

<span data-ttu-id="3041e-108">La classe **MSVM \_ ElementAllocatedFromNumaNode** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="3041e-108">The **Msvm\_ElementAllocatedFromNumaNode** class has these types of members:</span></span>

-   [<span data-ttu-id="3041e-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3041e-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3041e-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3041e-110">Properties</span></span>

<span data-ttu-id="3041e-111">La classe **MSVM \_ ElementAllocatedFromNumaNode** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="3041e-111">The **Msvm\_ElementAllocatedFromNumaNode** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3041e-112">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="3041e-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3041e-113">Type de données : **[ **MSVM \_ NumaNode**](msvm-numanode.md)**</span><span class="sxs-lookup"><span data-stu-id="3041e-113">Data type: **[**Msvm\_NumaNode**](msvm-numanode.md)**</span></span>
</dt> <dt>

<span data-ttu-id="3041e-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3041e-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3041e-115">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="3041e-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="3041e-116">Nœud NUMA physique.</span><span class="sxs-lookup"><span data-stu-id="3041e-116">The physical NUMA node.</span></span>

</dd> <dt>

<span data-ttu-id="3041e-117">**Charge**</span><span class="sxs-lookup"><span data-stu-id="3041e-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3041e-118">Type de données : **[ **CIM \_ LogicalElement**](/windows/desktop/CIMWin32Prov/cim-logicalelement)**</span><span class="sxs-lookup"><span data-stu-id="3041e-118">Data type: **[**CIM\_LogicalElement**](/windows/desktop/CIMWin32Prov/cim-logicalelement)**</span></span>
</dt> <dt>

<span data-ttu-id="3041e-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3041e-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3041e-120">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="3041e-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="3041e-121">Ressource allouée.</span><span class="sxs-lookup"><span data-stu-id="3041e-121">The allocated resource.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3041e-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3041e-122">Requirements</span></span>



| <span data-ttu-id="3041e-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3041e-123">Requirement</span></span> | <span data-ttu-id="3041e-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="3041e-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3041e-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3041e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="3041e-126">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3041e-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3041e-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3041e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="3041e-128">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3041e-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3041e-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3041e-129">Namespace</span></span><br/>                | <span data-ttu-id="3041e-130">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="3041e-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3041e-131">MOF</span><span class="sxs-lookup"><span data-stu-id="3041e-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3041e-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3041e-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3041e-133">DLL</span><span class="sxs-lookup"><span data-stu-id="3041e-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3041e-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3041e-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

