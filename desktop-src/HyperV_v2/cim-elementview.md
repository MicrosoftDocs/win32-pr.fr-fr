---
description: Représente l’association entre une vue et une instance qui représente la vue normalisée d’une ressource managée.
ms.assetid: 9c6eb3d5-7366-4954-9e64-12f889c64114
title: Classe CIM_ElementView
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementView
- CIM_ElementView.Antecedent
- CIM_ElementView.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b6ffc0e4b69667800b1880cae1a992a207cc95a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529864"
---
# <a name="cim_elementview-class"></a><span data-ttu-id="52cf7-103">\_Classe CIM ElementView</span><span class="sxs-lookup"><span data-stu-id="52cf7-103">CIM\_ElementView class</span></span>

<span data-ttu-id="52cf7-104">Représente l’association entre une vue et une instance qui représente la vue normalisée d’une ressource managée.</span><span class="sxs-lookup"><span data-stu-id="52cf7-104">Represents and association between a view, and an instance that represents the normalized view of a managed resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="52cf7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="52cf7-105">Syntax</span></span>

``` syntax
[Abstract, Association, Experimental, Version("2.21.1"), UMLPackagePath("CIM::Core::CoreElements")]
class CIM_ElementView : CIM_Dependency
{
  CIM_ManagedElement REF Antecedent;
  CIM_View           REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="52cf7-106">Membres</span><span class="sxs-lookup"><span data-stu-id="52cf7-106">Members</span></span>

<span data-ttu-id="52cf7-107">La classe **CIM \_ ElementView** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="52cf7-107">The **CIM\_ElementView** class has these types of members:</span></span>

-   [<span data-ttu-id="52cf7-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="52cf7-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="52cf7-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="52cf7-109">Properties</span></span>

<span data-ttu-id="52cf7-110">La classe **CIM \_ ElementView** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="52cf7-110">The **CIM\_ElementView** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="52cf7-111">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="52cf7-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52cf7-112">Type de données : **CIM \_ propriété ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="52cf7-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="52cf7-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52cf7-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52cf7-114">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="52cf7-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="52cf7-115">Instance de qui représente la vue normalisée de la ressource managée.</span><span class="sxs-lookup"><span data-stu-id="52cf7-115">The instance that represents the normalized view of the managed resource.</span></span>

</dd> <dt>

<span data-ttu-id="52cf7-116">**Charge**</span><span class="sxs-lookup"><span data-stu-id="52cf7-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52cf7-117">Type de données **: \_ vue CIM**</span><span class="sxs-lookup"><span data-stu-id="52cf7-117">Data type: **CIM\_View**</span></span>
</dt> <dt>

<span data-ttu-id="52cf7-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52cf7-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52cf7-119">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) (« dépendant »)</span><span class="sxs-lookup"><span data-stu-id="52cf7-119">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="52cf7-120">Vue qui représente une vue dénormalisée ou agrégée de la ressource managée.</span><span class="sxs-lookup"><span data-stu-id="52cf7-120">The view that represents a de-normalized or aggregate view of the managed resource.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="52cf7-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="52cf7-121">Requirements</span></span>



| <span data-ttu-id="52cf7-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="52cf7-122">Requirement</span></span> | <span data-ttu-id="52cf7-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="52cf7-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52cf7-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="52cf7-124">Minimum supported client</span></span><br/> | <span data-ttu-id="52cf7-125">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="52cf7-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="52cf7-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="52cf7-126">Minimum supported server</span></span><br/> | <span data-ttu-id="52cf7-127">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="52cf7-127">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="52cf7-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="52cf7-128">Namespace</span></span><br/>                | <span data-ttu-id="52cf7-129">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="52cf7-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="52cf7-130">MOF</span><span class="sxs-lookup"><span data-stu-id="52cf7-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="52cf7-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="52cf7-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="52cf7-132">DLL</span><span class="sxs-lookup"><span data-stu-id="52cf7-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52cf7-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="52cf7-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="52cf7-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="52cf7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52cf7-135">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="52cf7-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

