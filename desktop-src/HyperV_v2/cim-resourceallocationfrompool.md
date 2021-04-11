---
description: Représente une association dans laquelle une \_ instance RESOURCEALLOCATIONSETTINGDATA CIM est allouée à partir d’un pool de ressources.
ms.assetid: ca9060e5-4434-4302-a840-a7d9cf5db714
title: Classe CIM_ResourceAllocationFromPool
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourceAllocationFromPool
- CIM_ResourceAllocationFromPool.Antecedent
- CIM_ResourceAllocationFromPool.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 09bd7b70d49d2304062d35d29586fea886c86a3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952522"
---
# <a name="cim_resourceallocationfrompool-class"></a><span data-ttu-id="f5dc1-103">\_Classe CIM ResourceAllocationFromPool</span><span class="sxs-lookup"><span data-stu-id="f5dc1-103">CIM\_ResourceAllocationFromPool class</span></span>

<span data-ttu-id="f5dc1-104">Représente une association dans laquelle une [**instance \_ ResourceAllocationSettingData CIM**](cim-resourceallocationsettingdata.md) est allouée à partir d’un pool de ressources.</span><span class="sxs-lookup"><span data-stu-id="f5dc1-104">Represents an association in which a [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) instance is allocated from a resource pool.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5dc1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f5dc1-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.22.0"), UMLPackagePath("CIM::System::Resource"), AMENDMENT]
class CIM_ResourceAllocationFromPool : CIM_Dependency
{
  CIM_ResourcePool                  REF Antecedent;
  CIM_ResourceAllocationSettingData REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="f5dc1-106">Membres</span><span class="sxs-lookup"><span data-stu-id="f5dc1-106">Members</span></span>

<span data-ttu-id="f5dc1-107">La classe **CIM \_ ResourceAllocationFromPool** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="f5dc1-107">The **CIM\_ResourceAllocationFromPool** class has these types of members:</span></span>

-   [<span data-ttu-id="f5dc1-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f5dc1-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f5dc1-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f5dc1-109">Properties</span></span>

<span data-ttu-id="f5dc1-110">La classe **CIM \_ ResourceAllocationFromPool** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="f5dc1-110">The **CIM\_ResourceAllocationFromPool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f5dc1-111">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="f5dc1-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5dc1-112">Type de données : **CIM \_ ResourcePool**</span><span class="sxs-lookup"><span data-stu-id="f5dc1-112">Data type: **CIM\_ResourcePool**</span></span>
</dt> <dt>

<span data-ttu-id="f5dc1-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f5dc1-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5dc1-114">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="f5dc1-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="f5dc1-115">Pool de ressources.</span><span class="sxs-lookup"><span data-stu-id="f5dc1-115">The resource pool.</span></span>

</dd> <dt>

<span data-ttu-id="f5dc1-116">**Charge**</span><span class="sxs-lookup"><span data-stu-id="f5dc1-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5dc1-117">Type de données : **CIM \_ ResourceAllocationSettingData**</span><span class="sxs-lookup"><span data-stu-id="f5dc1-117">Data type: **CIM\_ResourceAllocationSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="f5dc1-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f5dc1-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5dc1-119">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="f5dc1-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="f5dc1-120">Données d’allocation de ressources.</span><span class="sxs-lookup"><span data-stu-id="f5dc1-120">The resource allocation data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f5dc1-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f5dc1-121">Requirements</span></span>



| <span data-ttu-id="f5dc1-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f5dc1-122">Requirement</span></span> | <span data-ttu-id="f5dc1-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="f5dc1-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5dc1-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f5dc1-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f5dc1-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="f5dc1-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="f5dc1-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f5dc1-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f5dc1-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f5dc1-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="f5dc1-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f5dc1-128">Namespace</span></span><br/>                | <span data-ttu-id="f5dc1-129">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="f5dc1-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f5dc1-130">MOF</span><span class="sxs-lookup"><span data-stu-id="f5dc1-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f5dc1-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f5dc1-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f5dc1-132">DLL</span><span class="sxs-lookup"><span data-stu-id="f5dc1-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5dc1-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f5dc1-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f5dc1-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f5dc1-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5dc1-135">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="f5dc1-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

