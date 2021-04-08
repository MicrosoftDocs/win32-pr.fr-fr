---
description: Représente une relation dans laquelle un élément managé est membre de et est agrégé par une collection.
ms.assetid: 324284fa-ece6-41df-9891-040a7561dce4
title: Classe CIM_MemberOfCollection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MemberOfCollection
- CIM_MemberOfCollection.Collection
- CIM_MemberOfCollection.Member
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9bcebfb08cbbc0cb18e00f1b0e5e2646ca086faf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034803"
---
# <a name="cim_memberofcollection-class"></a><span data-ttu-id="78e24-103">\_Classe CIM MemberOfCollection</span><span class="sxs-lookup"><span data-stu-id="78e24-103">CIM\_MemberOfCollection class</span></span>

<span data-ttu-id="78e24-104">Représente une relation dans laquelle un élément managé est membre de et est agrégé par une collection.</span><span class="sxs-lookup"><span data-stu-id="78e24-104">Represents a relationship in which a managed element is a member of and is aggregated by a collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="78e24-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="78e24-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Core::Collection"), AMENDMENT]
class CIM_MemberOfCollection
{
  CIM_Collection     REF Collection;
  CIM_ManagedElement REF Member;
};
```

## <a name="members"></a><span data-ttu-id="78e24-106">Membres</span><span class="sxs-lookup"><span data-stu-id="78e24-106">Members</span></span>

<span data-ttu-id="78e24-107">La classe **CIM \_ MemberOfCollection** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="78e24-107">The **CIM\_MemberOfCollection** class has these types of members:</span></span>

-   [<span data-ttu-id="78e24-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="78e24-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="78e24-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="78e24-109">Properties</span></span>

<span data-ttu-id="78e24-110">La classe **CIM \_ MemberOfCollection** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="78e24-110">The **CIM\_MemberOfCollection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="78e24-111">**Collection**</span><span class="sxs-lookup"><span data-stu-id="78e24-111">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78e24-112">Type de données **: \_ collecte CIM**</span><span class="sxs-lookup"><span data-stu-id="78e24-112">Data type: **CIM\_Collection**</span></span>
</dt> <dt>

<span data-ttu-id="78e24-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="78e24-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78e24-114">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**agrégat**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="78e24-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="78e24-115">Collection qui agrège les membres.</span><span class="sxs-lookup"><span data-stu-id="78e24-115">The collection that aggregates members.</span></span>

</dd> <dt>

<span data-ttu-id="78e24-116">**Membre**</span><span class="sxs-lookup"><span data-stu-id="78e24-116">**Member**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78e24-117">Type de données : **CIM \_ propriété ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="78e24-117">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="78e24-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="78e24-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78e24-119">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="78e24-119">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="78e24-120">Membre de la collection.</span><span class="sxs-lookup"><span data-stu-id="78e24-120">The member of the collection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="78e24-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="78e24-121">Requirements</span></span>



| <span data-ttu-id="78e24-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="78e24-122">Requirement</span></span> | <span data-ttu-id="78e24-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="78e24-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78e24-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="78e24-124">Minimum supported client</span></span><br/> | <span data-ttu-id="78e24-125">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="78e24-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="78e24-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="78e24-126">Minimum supported server</span></span><br/> | <span data-ttu-id="78e24-127">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="78e24-127">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="78e24-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="78e24-128">Namespace</span></span><br/>                | <span data-ttu-id="78e24-129">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="78e24-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="78e24-130">MOF</span><span class="sxs-lookup"><span data-stu-id="78e24-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="78e24-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="78e24-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="78e24-132">DLL</span><span class="sxs-lookup"><span data-stu-id="78e24-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78e24-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="78e24-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

