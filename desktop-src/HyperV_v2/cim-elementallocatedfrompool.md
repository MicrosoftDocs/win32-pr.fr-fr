---
description: Représente une association dans laquelle un \_ objet LOGICALELEMENT CIM représente une ressource allouée à partir d’un \_ objet ResourcePool CIM.
ms.assetid: 5e3c95c5-1cbb-40de-b285-0bf9b34a5ca8
title: Classe CIM_ElementAllocatedFromPool
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementAllocatedFromPool
- CIM_ElementAllocatedFromPool.Antecedent
- CIM_ElementAllocatedFromPool.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5fc6d58f5ebf82013f38b39027e0cd02e0e3595a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863117"
---
# <a name="cim_elementallocatedfrompool-class"></a><span data-ttu-id="7bf54-103">\_Classe CIM ElementAllocatedFromPool</span><span class="sxs-lookup"><span data-stu-id="7bf54-103">CIM\_ElementAllocatedFromPool class</span></span>

<span data-ttu-id="7bf54-104">Représente une association dans laquelle un [**objet \_ LogicalElement CIM**](cim-logicalelement.md) représente une ressource allouée à partir d’un objet [**\_ ResourcePool CIM**](cim-resourcepool.md) .</span><span class="sxs-lookup"><span data-stu-id="7bf54-104">Represents an association in which a [**CIM\_LogicalElement**](cim-logicalelement.md) object represents a resource allocated from a [**CIM\_ResourcePool**](cim-resourcepool.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bf54-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7bf54-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Resource"), AMENDMENT]
class CIM_ElementAllocatedFromPool : CIM_Dependency
{
  CIM_ResourcePool   REF Antecedent;
  CIM_LogicalElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="7bf54-106">Membres</span><span class="sxs-lookup"><span data-stu-id="7bf54-106">Members</span></span>

<span data-ttu-id="7bf54-107">La classe **CIM \_ ElementAllocatedFromPool** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="7bf54-107">The **CIM\_ElementAllocatedFromPool** class has these types of members:</span></span>

-   [<span data-ttu-id="7bf54-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7bf54-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7bf54-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7bf54-109">Properties</span></span>

<span data-ttu-id="7bf54-110">La classe **CIM \_ ElementAllocatedFromPool** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="7bf54-110">The **CIM\_ElementAllocatedFromPool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7bf54-111">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="7bf54-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bf54-112">Type de données : **CIM \_ ResourcePool**</span><span class="sxs-lookup"><span data-stu-id="7bf54-112">Data type: **CIM\_ResourcePool**</span></span>
</dt> <dt>

<span data-ttu-id="7bf54-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7bf54-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7bf54-114">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="7bf54-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="7bf54-115">Pool de ressources.</span><span class="sxs-lookup"><span data-stu-id="7bf54-115">The resource pool.</span></span>

</dd> <dt>

<span data-ttu-id="7bf54-116">**Charge**</span><span class="sxs-lookup"><span data-stu-id="7bf54-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bf54-117">Type de données : **CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="7bf54-117">Data type: **CIM\_LogicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="7bf54-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7bf54-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7bf54-119">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="7bf54-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="7bf54-120">Ressource allouée.</span><span class="sxs-lookup"><span data-stu-id="7bf54-120">The allocated resource.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7bf54-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7bf54-121">Requirements</span></span>



| <span data-ttu-id="7bf54-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7bf54-122">Requirement</span></span> | <span data-ttu-id="7bf54-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="7bf54-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bf54-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7bf54-124">Minimum supported client</span></span><br/> | <span data-ttu-id="7bf54-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="7bf54-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="7bf54-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7bf54-126">Minimum supported server</span></span><br/> | <span data-ttu-id="7bf54-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7bf54-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="7bf54-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7bf54-128">Namespace</span></span><br/>                | <span data-ttu-id="7bf54-129">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="7bf54-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="7bf54-130">MOF</span><span class="sxs-lookup"><span data-stu-id="7bf54-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7bf54-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7bf54-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7bf54-132">DLL</span><span class="sxs-lookup"><span data-stu-id="7bf54-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7bf54-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7bf54-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7bf54-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7bf54-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bf54-135">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="7bf54-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

