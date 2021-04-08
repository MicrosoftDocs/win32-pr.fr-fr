---
description: Classe abstraite pour les sous-classes qui représentent une collection d' \_ objets MANAGEDSYSTEMELEMENT CIM. Ces collections permettent de regrouper les éléments système gérés à des fins d’identification et de simplifier l’Association des paramètres et des configurations.
ms.assetid: f47bf1d6-6d89-4d9f-82d1-99a7343481bc
title: Classe CIM_CollectionOfMSEs (gestion Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectionOfMSEs
- CIM_CollectionOfMSEs.CollectionID
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7e467e775c78364718f25cc732d6689d9fb2b9da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864122"
---
# <a name="cim_collectionofmses-class-hyper-v-management"></a><span data-ttu-id="e042d-104">Classe CIM_CollectionOfMSEs (gestion Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="e042d-104">CIM_CollectionOfMSEs class (Hyper-V management)</span></span>

<span data-ttu-id="e042d-105">Classe abstraite pour les sous-classes qui représentent une collection d’objets [**\_ ManagedSystemElement CIM**](cim-managedsystemelement.md) .</span><span class="sxs-lookup"><span data-stu-id="e042d-105">An abstract class for subclasses that represent a collection of [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) objects.</span></span> <span data-ttu-id="e042d-106">Ces collections permettent de regrouper les éléments système gérés à des fins d’identification et de simplifier l’Association des paramètres et des configurations.</span><span class="sxs-lookup"><span data-stu-id="e042d-106">These collections allow managed system elements to be grouped for identification purposes and to simplify the association of settings and configurations.</span></span>

## <a name="syntax"></a><span data-ttu-id="e042d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e042d-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Collection"), AMENDMENT]
class CIM_CollectionOfMSEs : CIM_Collection
{
  string CollectionID;
};
```

## <a name="members"></a><span data-ttu-id="e042d-108">Membres</span><span class="sxs-lookup"><span data-stu-id="e042d-108">Members</span></span>

<span data-ttu-id="e042d-109">La classe **CIM \_ CollectionOfMSEs** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e042d-109">The **CIM\_CollectionOfMSEs** class has these types of members:</span></span>

-   [<span data-ttu-id="e042d-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e042d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e042d-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e042d-111">Properties</span></span>

<span data-ttu-id="e042d-112">La classe **CIM \_ CollectionOfMSEs** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="e042d-112">The **CIM\_CollectionOfMSEs** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e042d-113">**CollectionID**</span><span class="sxs-lookup"><span data-stu-id="e042d-113">**CollectionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e042d-114">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e042d-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e042d-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e042d-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e042d-116">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="e042d-116">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e042d-117">Identification de l’objet de collection.</span><span class="sxs-lookup"><span data-stu-id="e042d-117">The identification of the collection object.</span></span> <span data-ttu-id="e042d-118">Lorsqu’elle est sous-classée **, la propriété** de l’un peut être substituée en tant que propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="e042d-118">When subclassed, the **CollectionID** property can be overridden as a key property.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e042d-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e042d-119">Requirements</span></span>



| <span data-ttu-id="e042d-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e042d-120">Requirement</span></span> | <span data-ttu-id="e042d-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="e042d-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e042d-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e042d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e042d-123">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e042d-123">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="e042d-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e042d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e042d-125">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e042d-125">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="e042d-126">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e042d-126">Namespace</span></span><br/>                | <span data-ttu-id="e042d-127">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="e042d-127">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e042d-128">MOF</span><span class="sxs-lookup"><span data-stu-id="e042d-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e042d-129"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e042d-129"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e042d-130">DLL</span><span class="sxs-lookup"><span data-stu-id="e042d-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e042d-131"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e042d-131"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e042d-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e042d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e042d-133">**\_Collection CIM**</span><span class="sxs-lookup"><span data-stu-id="e042d-133">**CIM\_Collection**</span></span>](cim-collection.md)
</dt> </dl>

 

