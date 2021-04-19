---
description: Représente l’association entre deux définitions de métriques ou deux valeurs de métriques.
ms.assetid: 78fb926d-8981-443a-a82d-ebac34d38e13
title: Classe Msvm_MetricCollectionDependency
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricCollectionDependency
- Msvm_MetricCollectionDependency.Antecedent
- Msvm_MetricCollectionDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: dc24cf72975f9d4e47e414425ac4cfbfe5d11847
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106542003"
---
# <a name="msvm_metriccollectiondependency-class"></a><span data-ttu-id="f032b-103">MSVM \_ MetricCollectionDependency, classe</span><span class="sxs-lookup"><span data-stu-id="f032b-103">Msvm\_MetricCollectionDependency class</span></span>

<span data-ttu-id="f032b-104">Représente l’association entre deux définitions de métriques ou deux valeurs de métriques.</span><span class="sxs-lookup"><span data-stu-id="f032b-104">Represents the association between two metric definitions or two metric values.</span></span>

<span data-ttu-id="f032b-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="f032b-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f032b-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f032b-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricCollectionDependency : CIM_Dependency
{
  CIM_ManagedElement REF Antecedent;
  CIM_ManagedElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="f032b-107">Membres</span><span class="sxs-lookup"><span data-stu-id="f032b-107">Members</span></span>

<span data-ttu-id="f032b-108">La classe **MSVM \_ MetricCollectionDependency** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="f032b-108">The **Msvm\_MetricCollectionDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="f032b-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f032b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f032b-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f032b-110">Properties</span></span>

<span data-ttu-id="f032b-111">La classe **MSVM \_ MetricCollectionDependency** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="f032b-111">The **Msvm\_MetricCollectionDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f032b-112">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="f032b-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f032b-113">Type de données : **[ **CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="f032b-113">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="f032b-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f032b-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f032b-115">Référence à une instance de la classe [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) qui représente la définition de métrique indépendante ou la valeur métrique.</span><span class="sxs-lookup"><span data-stu-id="f032b-115">A reference to an instance of the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class that represents the independent metric definition or metric value.</span></span> <span data-ttu-id="f032b-116">Cette propriété est héritée de la [**\_ dépendance CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="f032b-116">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="f032b-117">**Charge**</span><span class="sxs-lookup"><span data-stu-id="f032b-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f032b-118">Type de données : **[ **CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="f032b-118">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="f032b-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f032b-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f032b-120">Référence à une instance de la classe [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) qui représente la définition de métrique ou la valeur de métrique qui est dépendante de l' **antécédent**.</span><span class="sxs-lookup"><span data-stu-id="f032b-120">A reference to an instance of the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class that represents the metric definition or metric value that is dependent on the **Antecedent**.</span></span> <span data-ttu-id="f032b-121">Cette propriété est héritée de la [**\_ dépendance CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="f032b-121">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f032b-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f032b-122">Requirements</span></span>



| <span data-ttu-id="f032b-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f032b-123">Requirement</span></span> | <span data-ttu-id="f032b-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="f032b-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f032b-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f032b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f032b-126">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f032b-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f032b-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f032b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f032b-128">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f032b-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f032b-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f032b-129">Namespace</span></span><br/>                | <span data-ttu-id="f032b-130">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="f032b-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f032b-131">MOF</span><span class="sxs-lookup"><span data-stu-id="f032b-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f032b-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f032b-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f032b-133">DLL</span><span class="sxs-lookup"><span data-stu-id="f032b-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f032b-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f032b-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

