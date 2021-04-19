---
description: Représente une association où un élément managé est hébergé par un autre.
ms.assetid: ae8476f7-38a4-4d08-a7dc-21e120d3cbe1
title: Classe CIM_HostedDependency
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedDependency
- CIM_HostedDependency.Antecedent
- CIM_HostedDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 551931fd88fac88f85bcc8ffd51423538de3bb5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514377"
---
# <a name="cim_hosteddependency-class"></a><span data-ttu-id="4121b-103">\_Classe CIM HostedDependency</span><span class="sxs-lookup"><span data-stu-id="4121b-103">CIM\_HostedDependency class</span></span>

<span data-ttu-id="4121b-104">Représente une association où un élément managé est hébergé par un autre.</span><span class="sxs-lookup"><span data-stu-id="4121b-104">Represents an association where a managed element is hosted by another.</span></span>

## <a name="syntax"></a><span data-ttu-id="4121b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4121b-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.8.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_HostedDependency : CIM_Dependency
{
  CIM_ManagedElement REF Antecedent;
  CIM_ManagedElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="4121b-106">Membres</span><span class="sxs-lookup"><span data-stu-id="4121b-106">Members</span></span>

<span data-ttu-id="4121b-107">La classe **CIM \_ HostedDependency** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="4121b-107">The **CIM\_HostedDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="4121b-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4121b-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4121b-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4121b-109">Properties</span></span>

<span data-ttu-id="4121b-110">La classe **CIM \_ HostedDependency** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="4121b-110">The **CIM\_HostedDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4121b-111">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="4121b-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4121b-112">Type de données : **CIM \_ propriété ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="4121b-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="4121b-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4121b-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4121b-114">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="4121b-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="4121b-115">Élément géré par l’hôte.</span><span class="sxs-lookup"><span data-stu-id="4121b-115">The host managed element.</span></span>

</dd> <dt>

<span data-ttu-id="4121b-116">**Charge**</span><span class="sxs-lookup"><span data-stu-id="4121b-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4121b-117">Type de données : **CIM \_ propriété ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="4121b-117">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="4121b-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4121b-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4121b-119">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="4121b-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="4121b-120">Élément managé hébergé.</span><span class="sxs-lookup"><span data-stu-id="4121b-120">The hosted managed element.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4121b-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4121b-121">Requirements</span></span>



| <span data-ttu-id="4121b-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4121b-122">Requirement</span></span> | <span data-ttu-id="4121b-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="4121b-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4121b-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4121b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4121b-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="4121b-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="4121b-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4121b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4121b-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4121b-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="4121b-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4121b-128">Namespace</span></span><br/>                | <span data-ttu-id="4121b-129">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="4121b-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="4121b-130">MOF</span><span class="sxs-lookup"><span data-stu-id="4121b-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4121b-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4121b-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4121b-132">DLL</span><span class="sxs-lookup"><span data-stu-id="4121b-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4121b-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4121b-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4121b-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4121b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4121b-135">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="4121b-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

