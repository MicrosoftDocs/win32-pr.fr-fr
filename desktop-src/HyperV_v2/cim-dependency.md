---
description: Représente une association générique utilisée pour établir des relations de dépendance entre des éléments managés.
ms.assetid: a81beedc-5473-49a6-8e7f-67e831d3e8bc
title: Classe CIM_Dependency (gestion Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Dependency
- CIM_Dependency.Antecedent
- CIM_Dependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4e85f59b190e0024fc34489315fa2fae1c0d6b34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544712"
---
# <a name="cim_dependency-class-hyper-v-management"></a><span data-ttu-id="aa270-103">Classe CIM_Dependency (gestion Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="aa270-103">CIM_Dependency class (Hyper-V management)</span></span>

<span data-ttu-id="aa270-104">Représente une association générique utilisée pour établir des relations de dépendance entre des éléments managés.</span><span class="sxs-lookup"><span data-stu-id="aa270-104">Represents a generic association used to establish dependency relationships between managed elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa270-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aa270-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_Dependency
{
  CIM_ManagedElement REF Antecedent;
  CIM_ManagedElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="aa270-106">Membres</span><span class="sxs-lookup"><span data-stu-id="aa270-106">Members</span></span>

<span data-ttu-id="aa270-107">La classe de **\_ dépendance CIM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="aa270-107">The **CIM\_Dependency** class has these types of members:</span></span>

-   [<span data-ttu-id="aa270-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="aa270-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="aa270-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="aa270-109">Properties</span></span>

<span data-ttu-id="aa270-110">La classe de **\_ dépendance CIM** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="aa270-110">The **CIM\_Dependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="aa270-111">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="aa270-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa270-112">Type de données : **CIM \_ propriété ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="aa270-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="aa270-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aa270-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa270-114">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="aa270-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="aa270-115">Objet indépendant dans cette association.</span><span class="sxs-lookup"><span data-stu-id="aa270-115">The independent object in this association.</span></span>

</dd> <dt>

<span data-ttu-id="aa270-116">**Charge**</span><span class="sxs-lookup"><span data-stu-id="aa270-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa270-117">Type de données : **CIM \_ propriété ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="aa270-117">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="aa270-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aa270-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa270-119">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="aa270-119">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="aa270-120">Objet dépendant dans l’Association.</span><span class="sxs-lookup"><span data-stu-id="aa270-120">The dependent object in the association.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="aa270-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aa270-121">Requirements</span></span>



| <span data-ttu-id="aa270-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aa270-122">Requirement</span></span> | <span data-ttu-id="aa270-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="aa270-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa270-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aa270-124">Minimum supported client</span></span><br/> | <span data-ttu-id="aa270-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="aa270-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="aa270-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aa270-126">Minimum supported server</span></span><br/> | <span data-ttu-id="aa270-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="aa270-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="aa270-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="aa270-128">Namespace</span></span><br/>                | <span data-ttu-id="aa270-129">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="aa270-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="aa270-130">MOF</span><span class="sxs-lookup"><span data-stu-id="aa270-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aa270-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="aa270-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="aa270-132">DLL</span><span class="sxs-lookup"><span data-stu-id="aa270-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa270-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="aa270-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

