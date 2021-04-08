---
description: Représente une association entre un système et l’un des éléments qui le composent.
ms.assetid: 728f25bf-3d52-4b1c-bf72-51e8ed0a4e72
title: Classe CIM_SystemComponent (gestion Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SystemComponent
- CIM_SystemComponent.GroupComponent
- CIM_SystemComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 79bb7d3807a93b2d29157a3377d6e6a9079bfe16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864118"
---
# <a name="cim_systemcomponent-class-hyper-v-management"></a><span data-ttu-id="8320d-103">Classe CIM_SystemComponent (gestion Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="8320d-103">CIM_SystemComponent class (Hyper-V management)</span></span>

<span data-ttu-id="8320d-104">Représente une association entre un système et l’un des éléments qui le composent.</span><span class="sxs-lookup"><span data-stu-id="8320d-104">Represents an association between a system and one of the elements that compose it.</span></span>

## <a name="syntax"></a><span data-ttu-id="8320d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8320d-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_SystemComponent : CIM_Component
{
  CIM_System               REF GroupComponent;
  CIM_ManagedSystemElement REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="8320d-106">Membres</span><span class="sxs-lookup"><span data-stu-id="8320d-106">Members</span></span>

<span data-ttu-id="8320d-107">La classe **CIM \_ SystemComponent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="8320d-107">The **CIM\_SystemComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="8320d-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8320d-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8320d-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8320d-109">Properties</span></span>

<span data-ttu-id="8320d-110">La classe **CIM \_ SystemComponent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="8320d-110">The **CIM\_SystemComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8320d-111">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="8320d-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8320d-112">Type de données **: \_ système CIM**</span><span class="sxs-lookup"><span data-stu-id="8320d-112">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="8320d-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8320d-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8320d-114">Qualificateurs : [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="8320d-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="8320d-115">[**\_ Système CIM**](cim-system.md) qui contient l' **PartComponent**.</span><span class="sxs-lookup"><span data-stu-id="8320d-115">The [**CIM\_System**](cim-system.md) that contains the **PartComponent**.</span></span>

</dd> <dt>

<span data-ttu-id="8320d-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="8320d-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8320d-117">Type de données **: \_ CIM CIM**</span><span class="sxs-lookup"><span data-stu-id="8320d-117">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="8320d-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8320d-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8320d-119">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="8320d-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="8320d-120">Le [**\_ ManagedSystemElement CIM**](cim-managedsystemelement.md) enfant qui est un composant du système.</span><span class="sxs-lookup"><span data-stu-id="8320d-120">The child [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) that is a component of the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8320d-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8320d-121">Requirements</span></span>



| <span data-ttu-id="8320d-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8320d-122">Requirement</span></span> | <span data-ttu-id="8320d-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="8320d-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8320d-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8320d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="8320d-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="8320d-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="8320d-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8320d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="8320d-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8320d-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="8320d-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8320d-128">Namespace</span></span><br/>                | <span data-ttu-id="8320d-129">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="8320d-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="8320d-130">MOF</span><span class="sxs-lookup"><span data-stu-id="8320d-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8320d-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8320d-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8320d-132">DLL</span><span class="sxs-lookup"><span data-stu-id="8320d-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8320d-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8320d-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8320d-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8320d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8320d-135">**\_Composant CIM**</span><span class="sxs-lookup"><span data-stu-id="8320d-135">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

