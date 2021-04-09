---
description: Représente une association générique utilisée pour établir les parties d’une relation entre des éléments managés.
ms.assetid: 9785ea8b-fb76-4ffe-8649-aa2fe1b01d5f
title: Classe CIM_ConcreteComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConcreteComponent
- CIM_ConcreteComponent.GroupComponent
- CIM_ConcreteComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 77ee0f33f540bfd215ec10a24c3c574976189d07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865782"
---
# <a name="cim_concretecomponent-class"></a><span data-ttu-id="9b18f-103">\_Classe CIM ConcreteComponent</span><span class="sxs-lookup"><span data-stu-id="9b18f-103">CIM\_ConcreteComponent class</span></span>

<span data-ttu-id="9b18f-104">Représente une association générique utilisée pour établir les parties d’une relation entre des éléments managés.</span><span class="sxs-lookup"><span data-stu-id="9b18f-104">Represents a generic association used to establish the parts of a relationship between managed elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b18f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9b18f-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_ConcreteComponent : CIM_Component
{
  CIM_ManagedElement REF GroupComponent;
  CIM_ManagedElement REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="9b18f-106">Membres</span><span class="sxs-lookup"><span data-stu-id="9b18f-106">Members</span></span>

<span data-ttu-id="9b18f-107">La classe **CIM \_ ConcreteComponent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="9b18f-107">The **CIM\_ConcreteComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="9b18f-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9b18f-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9b18f-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9b18f-109">Properties</span></span>

<span data-ttu-id="9b18f-110">La classe **CIM \_ ConcreteComponent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="9b18f-110">The **CIM\_ConcreteComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9b18f-111">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="9b18f-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b18f-112">Type de données : **CIM \_ propriété ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="9b18f-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="9b18f-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9b18f-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b18f-114">Qualificateurs : [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="9b18f-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="9b18f-115">Élément parent dans l’Association.</span><span class="sxs-lookup"><span data-stu-id="9b18f-115">The parent element in the association.</span></span>

</dd> <dt>

<span data-ttu-id="9b18f-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="9b18f-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b18f-117">Type de données : **CIM \_ propriété ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="9b18f-117">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="9b18f-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9b18f-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b18f-119">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="9b18f-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="9b18f-120">Élément enfant dans l’Association.</span><span class="sxs-lookup"><span data-stu-id="9b18f-120">The child element in the association.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9b18f-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9b18f-121">Requirements</span></span>



| <span data-ttu-id="9b18f-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9b18f-122">Requirement</span></span> | <span data-ttu-id="9b18f-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="9b18f-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b18f-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9b18f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="9b18f-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="9b18f-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="9b18f-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9b18f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="9b18f-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9b18f-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="9b18f-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9b18f-128">Namespace</span></span><br/>                | <span data-ttu-id="9b18f-129">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="9b18f-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="9b18f-130">MOF</span><span class="sxs-lookup"><span data-stu-id="9b18f-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9b18f-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9b18f-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9b18f-132">DLL</span><span class="sxs-lookup"><span data-stu-id="9b18f-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b18f-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9b18f-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9b18f-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9b18f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b18f-135">**\_Composant CIM**</span><span class="sxs-lookup"><span data-stu-id="9b18f-135">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

