---
description: Représente une association entre un système et un pool de ressources qui est un composant du système.
ms.assetid: 0ac60dbd-0498-4978-b2d6-f4c9926a83a8
title: Classe CIM_HostedResourcePool
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedResourcePool
- CIM_HostedResourcePool.GroupComponent
- CIM_HostedResourcePool.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: dbb6d523b533d6e8b2f5bc1e21de93962cfd860f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106540809"
---
# <a name="cim_hostedresourcepool-class"></a><span data-ttu-id="1d375-103">\_Classe CIM HostedResourcePool</span><span class="sxs-lookup"><span data-stu-id="1d375-103">CIM\_HostedResourcePool class</span></span>

<span data-ttu-id="1d375-104">Représente une association entre un système et un pool de ressources qui est un composant du système.</span><span class="sxs-lookup"><span data-stu-id="1d375-104">Represents an association between a system and a resource pool that is a component of the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d375-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1d375-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Composition, Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Resource")]
class CIM_HostedResourcePool : CIM_SystemComponent
{
  CIM_System       REF GroupComponent;
  CIM_ResourcePool REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="1d375-106">Membres</span><span class="sxs-lookup"><span data-stu-id="1d375-106">Members</span></span>

<span data-ttu-id="1d375-107">La classe **CIM \_ HostedResourcePool** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="1d375-107">The **CIM\_HostedResourcePool** class has these types of members:</span></span>

-   [<span data-ttu-id="1d375-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1d375-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1d375-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1d375-109">Properties</span></span>

<span data-ttu-id="1d375-110">La classe **CIM \_ HostedResourcePool** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="1d375-110">The **CIM\_HostedResourcePool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1d375-111">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="1d375-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d375-112">Type de données **: \_ système CIM**</span><span class="sxs-lookup"><span data-stu-id="1d375-112">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="1d375-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1d375-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d375-114">Qualificateurs : [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="1d375-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="1d375-115">Système parent dans l’Association.</span><span class="sxs-lookup"><span data-stu-id="1d375-115">The parent system in the association.</span></span>

</dd> <dt>

<span data-ttu-id="1d375-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="1d375-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d375-117">Type de données : **CIM \_ ResourcePool**</span><span class="sxs-lookup"><span data-stu-id="1d375-117">Data type: **CIM\_ResourcePool**</span></span>
</dt> <dt>

<span data-ttu-id="1d375-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1d375-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d375-119">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="1d375-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="1d375-120">Pool de ressources qui est un composant du système.</span><span class="sxs-lookup"><span data-stu-id="1d375-120">The resource pool that is a component of the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1d375-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1d375-121">Requirements</span></span>



| <span data-ttu-id="1d375-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1d375-122">Requirement</span></span> | <span data-ttu-id="1d375-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="1d375-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d375-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1d375-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1d375-125">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="1d375-125">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="1d375-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1d375-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1d375-127">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="1d375-127">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="1d375-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1d375-128">Namespace</span></span><br/>                | <span data-ttu-id="1d375-129">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="1d375-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="1d375-130">MOF</span><span class="sxs-lookup"><span data-stu-id="1d375-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1d375-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1d375-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1d375-132">DLL</span><span class="sxs-lookup"><span data-stu-id="1d375-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d375-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1d375-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1d375-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1d375-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d375-135">**\_SYSTEMCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="1d375-135">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> </dl>

 

