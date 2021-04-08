---
description: Représente une spécialisation de l’Association de composants système qui établit que le pool de ressources est défini dans le contexte du système.
ms.assetid: 72b68687-2b5f-4fef-bdca-a5c0bbfa3564
title: Classe Msvm_HostedResourcePool
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HostedResourcePool
- Msvm_HostedResourcePool.GroupComponent
- Msvm_HostedResourcePool.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d64488a845e8d51bfe27829b01ebcf0ac7d944c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862070"
---
# <a name="msvm_hostedresourcepool-class"></a><span data-ttu-id="ade0b-103">MSVM \_ HostedResourcePool, classe</span><span class="sxs-lookup"><span data-stu-id="ade0b-103">Msvm\_HostedResourcePool class</span></span>

<span data-ttu-id="ade0b-104">Représente une spécialisation de l’Association de composants système qui établit que le pool de ressources est défini dans le contexte du système.</span><span class="sxs-lookup"><span data-stu-id="ade0b-104">Represents a specialization of the system component association that establishes that the resource pool is defined in the context of the system.</span></span>

<span data-ttu-id="ade0b-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="ade0b-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ade0b-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ade0b-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Composition, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HostedResourcePool : CIM_SystemComponent
{
  Msvm_ComputerSystem REF GroupComponent;
  CIM_ResourcePool    REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="ade0b-107">Membres</span><span class="sxs-lookup"><span data-stu-id="ade0b-107">Members</span></span>

<span data-ttu-id="ade0b-108">La classe **MSVM \_ HostedResourcePool** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ade0b-108">The **Msvm\_HostedResourcePool** class has these types of members:</span></span>

-   [<span data-ttu-id="ade0b-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ade0b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ade0b-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ade0b-110">Properties</span></span>

<span data-ttu-id="ade0b-111">La classe **MSVM \_ HostedResourcePool** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="ade0b-111">The **Msvm\_HostedResourcePool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ade0b-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="ade0b-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ade0b-113">Type de données : **[ **MSVM \_ ComputerSystem**](msvm-computersystem.md)**</span><span class="sxs-lookup"><span data-stu-id="ade0b-113">Data type: **[**Msvm\_ComputerSystem**](msvm-computersystem.md)**</span></span>
</dt> <dt>

<span data-ttu-id="ade0b-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ade0b-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ade0b-115">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="ade0b-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="ade0b-116">Système parent dans l’Association.</span><span class="sxs-lookup"><span data-stu-id="ade0b-116">The parent system in the association.</span></span>

</dd> <dt>

<span data-ttu-id="ade0b-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="ade0b-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ade0b-118">Type de données : **[ **CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="ade0b-118">Data type: **[**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="ade0b-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ade0b-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ade0b-120">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="ade0b-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="ade0b-121">Pool de ressources qui est un composant du système.</span><span class="sxs-lookup"><span data-stu-id="ade0b-121">The resource pool that is a component of the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ade0b-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ade0b-122">Requirements</span></span>



| <span data-ttu-id="ade0b-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ade0b-123">Requirement</span></span> | <span data-ttu-id="ade0b-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="ade0b-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ade0b-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ade0b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ade0b-126">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ade0b-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ade0b-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ade0b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ade0b-128">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ade0b-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ade0b-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ade0b-129">Namespace</span></span><br/>                | <span data-ttu-id="ade0b-130">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="ade0b-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ade0b-131">MOF</span><span class="sxs-lookup"><span data-stu-id="ade0b-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ade0b-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ade0b-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ade0b-133">DLL</span><span class="sxs-lookup"><span data-stu-id="ade0b-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ade0b-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ade0b-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

