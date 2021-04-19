---
description: Association entre une instance de MSVM \_ VssComponent et une instance de MSVM \_ VssService qui représente un service pour l’exécution d’opérations sur le composant VSS.
ms.assetid: 19fdf2e3-48c4-452b-89d0-ec0b8681fca2
title: Classe Msvm_ServiceOfVssComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ServiceOfVssComponent
- Msvm_ServiceOfVssComponent.Antecedent
- Msvm_ServiceOfVssComponent.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5787dcdd4d8ce1aeefdc1fbafb2c156aec4d467a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541845"
---
# <a name="msvm_serviceofvsscomponent-class"></a><span data-ttu-id="cf2b3-103">MSVM \_ ServiceOfVssComponent, classe</span><span class="sxs-lookup"><span data-stu-id="cf2b3-103">Msvm\_ServiceOfVssComponent class</span></span>

<span data-ttu-id="cf2b3-104">Association entre une instance de [**MSVM \_ VssComponent**](msvm-vsscomponent.md) et une instance de [**MSVM \_ VssService**](msvm-vssservice.md) qui représente un service pour l’exécution d’opérations sur le composant VSS.</span><span class="sxs-lookup"><span data-stu-id="cf2b3-104">An association between an instance of [**Msvm\_VssComponent**](msvm-vsscomponent.md) and an instance of [**Msvm\_VssService**](msvm-vssservice.md) that represents a service for performing operations on the VSS component.</span></span>

<span data-ttu-id="cf2b3-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="cf2b3-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf2b3-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cf2b3-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ServiceOfVssComponent : CIM_Dependency
{
  Msvm_VssComponent REF Antecedent;
  Msvm_VssService   REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="cf2b3-107">Membres</span><span class="sxs-lookup"><span data-stu-id="cf2b3-107">Members</span></span>

<span data-ttu-id="cf2b3-108">La classe **MSVM \_ ServiceOfVssComponent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="cf2b3-108">The **Msvm\_ServiceOfVssComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="cf2b3-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cf2b3-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cf2b3-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cf2b3-110">Properties</span></span>

<span data-ttu-id="cf2b3-111">La classe **MSVM \_ ServiceOfVssComponent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="cf2b3-111">The **Msvm\_ServiceOfVssComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cf2b3-112">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="cf2b3-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf2b3-113">Type de données : **MSVM \_ VssComponent**</span><span class="sxs-lookup"><span data-stu-id="cf2b3-113">Data type: **Msvm\_VssComponent**</span></span>
</dt> <dt>

<span data-ttu-id="cf2b3-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cf2b3-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf2b3-115">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ dependency. Antecedent")</span><span class="sxs-lookup"><span data-stu-id="cf2b3-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="cf2b3-116">[**MSVM \_ VssComponent**](msvm-vsscomponent.md) qui représente le composant VSS.</span><span class="sxs-lookup"><span data-stu-id="cf2b3-116">A, [**Msvm\_VssComponent**](msvm-vsscomponent.md) that represents the VSS component.</span></span>

</dd> <dt>

<span data-ttu-id="cf2b3-117">**Charge**</span><span class="sxs-lookup"><span data-stu-id="cf2b3-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf2b3-118">Type de données : **MSVM \_ VssService**</span><span class="sxs-lookup"><span data-stu-id="cf2b3-118">Data type: **Msvm\_VssService**</span></span>
</dt> <dt>

<span data-ttu-id="cf2b3-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cf2b3-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf2b3-120">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dépendance CIM \_ . dependent")</span><span class="sxs-lookup"><span data-stu-id="cf2b3-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="cf2b3-121">[**MSVM \_ VssService**](msvm-vssservice.md) qui représente le service VSS IC.</span><span class="sxs-lookup"><span data-stu-id="cf2b3-121">An [**Msvm\_VssService**](msvm-vssservice.md) that represents the VSS IC service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cf2b3-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cf2b3-122">Requirements</span></span>



| <span data-ttu-id="cf2b3-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cf2b3-123">Requirement</span></span> | <span data-ttu-id="cf2b3-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="cf2b3-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf2b3-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cf2b3-125">Minimum supported client</span></span><br/> | <span data-ttu-id="cf2b3-126">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cf2b3-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="cf2b3-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cf2b3-127">Minimum supported server</span></span><br/> | <span data-ttu-id="cf2b3-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="cf2b3-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="cf2b3-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="cf2b3-129">Namespace</span></span><br/>                | <span data-ttu-id="cf2b3-130">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="cf2b3-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="cf2b3-131">MOF</span><span class="sxs-lookup"><span data-stu-id="cf2b3-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cf2b3-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cf2b3-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cf2b3-133">DLL</span><span class="sxs-lookup"><span data-stu-id="cf2b3-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf2b3-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cf2b3-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="cf2b3-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cf2b3-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf2b3-136">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="cf2b3-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

