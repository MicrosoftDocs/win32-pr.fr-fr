---
description: Établit qu’une \_ instance RESOURCEALLOCATIONSETTINGDATA CIM représentant une allocation de ressources dépend d’une autre allocation de ressources.
ms.assetid: 567ee36a-d47b-444d-8d2f-425873f95bef
title: Classe Msvm_ResourceDependentOnResource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourceDependentOnResource
- Msvm_ResourceDependentOnResource.Antecedent
- Msvm_ResourceDependentOnResource.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 29cf3b607449c6a9145568e3ee858248af3c4248
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538904"
---
# <a name="msvm_resourcedependentonresource-class"></a><span data-ttu-id="dbe17-103">MSVM \_ ResourceDependentOnResource, classe</span><span class="sxs-lookup"><span data-stu-id="dbe17-103">Msvm\_ResourceDependentOnResource class</span></span>

<span data-ttu-id="dbe17-104">Établit qu’une [**instance \_ ResourceAllocationSettingData CIM**](cim-resourceallocationsettingdata.md) représentant une allocation de ressources dépend d’une autre allocation de ressources.</span><span class="sxs-lookup"><span data-stu-id="dbe17-104">Establishes that a [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) instance representing a resource allocation depends on another resource allocation.</span></span>

<span data-ttu-id="dbe17-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="dbe17-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbe17-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dbe17-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ResourceDependentOnResource : CIM_Dependency
{
  CIM_ResourceAllocationSettingData REF Antecedent;
  CIM_ResourceAllocationSettingData REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="dbe17-107">Membres</span><span class="sxs-lookup"><span data-stu-id="dbe17-107">Members</span></span>

<span data-ttu-id="dbe17-108">La classe **MSVM \_ ResourceDependentOnResource** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="dbe17-108">The **Msvm\_ResourceDependentOnResource** class has these types of members:</span></span>

-   [<span data-ttu-id="dbe17-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="dbe17-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dbe17-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="dbe17-110">Properties</span></span>

<span data-ttu-id="dbe17-111">La classe **MSVM \_ ResourceDependentOnResource** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="dbe17-111">The **Msvm\_ResourceDependentOnResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dbe17-112">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="dbe17-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbe17-113">Type de données : **CIM \_ ResourceAllocationSettingData**</span><span class="sxs-lookup"><span data-stu-id="dbe17-113">Data type: **CIM\_ResourceAllocationSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="dbe17-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dbe17-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbe17-115">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="dbe17-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="dbe17-116">[**\_ ResourceAllocationSettingData CIM**](cim-resourceallocationsettingdata.md) qui représente la ressource indépendante dans cette association.</span><span class="sxs-lookup"><span data-stu-id="dbe17-116">A [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) that represents the independent resource in this association.</span></span>

</dd> <dt>

<span data-ttu-id="dbe17-117">**Charge**</span><span class="sxs-lookup"><span data-stu-id="dbe17-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbe17-118">Type de données : **CIM \_ ResourceAllocationSettingData**</span><span class="sxs-lookup"><span data-stu-id="dbe17-118">Data type: **CIM\_ResourceAllocationSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="dbe17-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dbe17-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbe17-120">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) (« dépendant »)</span><span class="sxs-lookup"><span data-stu-id="dbe17-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="dbe17-121">[**\_ ResourceAllocationSettingData CIM**](cim-resourceallocationsettingdata.md) qui représente la ressource qui est dépendante de l’antécédent.</span><span class="sxs-lookup"><span data-stu-id="dbe17-121">A [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) that represents the resource that is dependent on the Antecedent.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dbe17-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dbe17-122">Requirements</span></span>



| <span data-ttu-id="dbe17-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dbe17-123">Requirement</span></span> | <span data-ttu-id="dbe17-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="dbe17-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbe17-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dbe17-125">Minimum supported client</span></span><br/> | <span data-ttu-id="dbe17-126">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dbe17-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="dbe17-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dbe17-127">Minimum supported server</span></span><br/> | <span data-ttu-id="dbe17-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="dbe17-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="dbe17-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="dbe17-129">Namespace</span></span><br/>                | <span data-ttu-id="dbe17-130">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="dbe17-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="dbe17-131">MOF</span><span class="sxs-lookup"><span data-stu-id="dbe17-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dbe17-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dbe17-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="dbe17-133">DLL</span><span class="sxs-lookup"><span data-stu-id="dbe17-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dbe17-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dbe17-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="dbe17-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dbe17-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbe17-136">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="dbe17-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

