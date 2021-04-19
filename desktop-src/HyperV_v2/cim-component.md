---
description: Représente une association générique entre un élément managé parent et un élément managé enfant où l’enfant représente un composant ou une partie du parent.
ms.assetid: b5cef452-2d00-483c-8e70-f804f1e3536b
title: Classe CIM_Component (gestion Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Component
- CIM_Component.GroupComponent
- CIM_Component.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 56ff83a4da51ba18205a8d8ab5e6e57ea1a7794b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534574"
---
# <a name="cim_component-class-hyper-v-management"></a><span data-ttu-id="505a9-103">Classe CIM_Component (gestion Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="505a9-103">CIM_Component class (Hyper-V management)</span></span>

<span data-ttu-id="505a9-104">Représente une association générique entre un élément managé parent et un élément managé enfant où l’enfant représente un composant ou une partie du parent.</span><span class="sxs-lookup"><span data-stu-id="505a9-104">Represents a generic association between a parent managed element and a child managed element where the child represents a component or part of the parent.</span></span>

## <a name="syntax"></a><span data-ttu-id="505a9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="505a9-105">Syntax</span></span>

``` syntax
[Association, Abstract, Aggregation, Version("2.7.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_Component
{
  CIM_ManagedElement REF GroupComponent;
  CIM_ManagedElement REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="505a9-106">Membres</span><span class="sxs-lookup"><span data-stu-id="505a9-106">Members</span></span>

<span data-ttu-id="505a9-107">La classe de **\_ composant CIM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="505a9-107">The **CIM\_Component** class has these types of members:</span></span>

-   [<span data-ttu-id="505a9-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="505a9-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="505a9-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="505a9-109">Properties</span></span>

<span data-ttu-id="505a9-110">La classe de **\_ composant CIM** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="505a9-110">The **CIM\_Component** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="505a9-111">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="505a9-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="505a9-112">Type de données : **CIM \_ propriété ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="505a9-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="505a9-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="505a9-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="505a9-114">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**agrégat**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="505a9-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="505a9-115">Élément parent dans l’Association.</span><span class="sxs-lookup"><span data-stu-id="505a9-115">The parent element in the association.</span></span>

</dd> <dt>

<span data-ttu-id="505a9-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="505a9-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="505a9-117">Type de données : **CIM \_ propriété ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="505a9-117">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="505a9-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="505a9-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="505a9-119">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="505a9-119">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="505a9-120">Élément enfant dans l’Association.</span><span class="sxs-lookup"><span data-stu-id="505a9-120">The child element in the association.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="505a9-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="505a9-121">Requirements</span></span>



| <span data-ttu-id="505a9-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="505a9-122">Requirement</span></span> | <span data-ttu-id="505a9-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="505a9-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="505a9-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="505a9-124">Minimum supported client</span></span><br/> | <span data-ttu-id="505a9-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="505a9-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="505a9-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="505a9-126">Minimum supported server</span></span><br/> | <span data-ttu-id="505a9-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="505a9-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="505a9-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="505a9-128">Namespace</span></span><br/>                | <span data-ttu-id="505a9-129">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="505a9-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="505a9-130">MOF</span><span class="sxs-lookup"><span data-stu-id="505a9-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="505a9-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="505a9-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="505a9-132">DLL</span><span class="sxs-lookup"><span data-stu-id="505a9-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="505a9-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="505a9-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

