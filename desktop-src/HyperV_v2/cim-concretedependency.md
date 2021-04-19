---
description: Représente une association générique dans laquelle un élément managé dépend d’un autre. CIM \_ ConcreteDependency sous-classe \_ la dépendance CIM pour fournir une version concrète de la \_ dépendance CIM.
ms.assetid: c0e1527d-d350-410d-9b5f-c9d4dedf7393
title: Classe CIM_ConcreteDependency
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConcreteDependency
- CIM_ConcreteDependency.Antecedent
- CIM_ConcreteDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 253f57b1fd29c3844f0e87d488974ced7bec98bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530888"
---
# <a name="cim_concretedependency-class"></a><span data-ttu-id="51050-104">\_Classe CIM ConcreteDependency</span><span class="sxs-lookup"><span data-stu-id="51050-104">CIM\_ConcreteDependency class</span></span>

<span data-ttu-id="51050-105">Représente une association générique dans laquelle un élément managé dépend d’un autre.</span><span class="sxs-lookup"><span data-stu-id="51050-105">Represents a generic association in which a managed element depends on another.</span></span> <span data-ttu-id="51050-106">**CIM \_ ConcreteDependency** sous-classe [**la \_ dépendance CIM**](cim-dependency.md) pour fournir une version concrète de **la \_ dépendance CIM**.</span><span class="sxs-lookup"><span data-stu-id="51050-106">**CIM\_ConcreteDependency** subclasses [**CIM\_Dependency**](cim-dependency.md) to provide a concrete class version of **CIM\_Dependency**.</span></span>

## <a name="syntax"></a><span data-ttu-id="51050-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="51050-107">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_ConcreteDependency : CIM_Dependency
{
  CIM_ManagedElement REF Antecedent;
  CIM_ManagedElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="51050-108">Membres</span><span class="sxs-lookup"><span data-stu-id="51050-108">Members</span></span>

<span data-ttu-id="51050-109">La classe **CIM \_ ConcreteDependency** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="51050-109">The **CIM\_ConcreteDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="51050-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="51050-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="51050-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="51050-111">Properties</span></span>

<span data-ttu-id="51050-112">La classe **CIM \_ ConcreteDependency** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="51050-112">The **CIM\_ConcreteDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="51050-113">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="51050-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51050-114">Type de données : **CIM \_ propriété ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="51050-114">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="51050-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="51050-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51050-116">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="51050-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="51050-117">Objet indépendant dans l’Association.</span><span class="sxs-lookup"><span data-stu-id="51050-117">The independent object in the association.</span></span>

</dd> <dt>

<span data-ttu-id="51050-118">**Charge**</span><span class="sxs-lookup"><span data-stu-id="51050-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51050-119">Type de données : **CIM \_ propriété ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="51050-119">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="51050-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="51050-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51050-121">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="51050-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="51050-122">Objet dépendant dans l’Association.</span><span class="sxs-lookup"><span data-stu-id="51050-122">The dependent object in the association.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="51050-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="51050-123">Requirements</span></span>



| <span data-ttu-id="51050-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="51050-124">Requirement</span></span> | <span data-ttu-id="51050-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="51050-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51050-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="51050-126">Minimum supported client</span></span><br/> | <span data-ttu-id="51050-127">Windows 8</span><span class="sxs-lookup"><span data-stu-id="51050-127">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="51050-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="51050-128">Minimum supported server</span></span><br/> | <span data-ttu-id="51050-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="51050-129">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="51050-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="51050-130">Namespace</span></span><br/>                | <span data-ttu-id="51050-131">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="51050-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="51050-132">MOF</span><span class="sxs-lookup"><span data-stu-id="51050-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="51050-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="51050-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="51050-134">DLL</span><span class="sxs-lookup"><span data-stu-id="51050-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="51050-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="51050-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="51050-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="51050-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51050-137">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="51050-137">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

