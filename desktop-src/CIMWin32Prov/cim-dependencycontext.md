---
description: La \_ relation DEPENDENCYCONTEXT CIM associe une \_ classe de dépendance CIM à un ou plusieurs \_ objets de configuration CIM. Par exemple, les dépendances d’un système informatique peuvent changer en fonction du réseau auquel le système est attaché.
ms.assetid: 9f35fc41-1bfa-4018-a54c-64c875c710d4
ms.tgt_platform: multiple
title: Classe CIM_DependencyContext
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DependencyContext
- CIM_DependencyContext.Context
- CIM_DependencyContext.Dependency
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 69319a4f4d228d484da62411060ae3fead90bb79
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861270"
---
# <a name="cim_dependencycontext-class"></a><span data-ttu-id="83188-104">\_Classe CIM DependencyContext</span><span class="sxs-lookup"><span data-stu-id="83188-104">CIM\_DependencyContext class</span></span>

<span data-ttu-id="83188-105">La **relation \_ DependencyContext CIM** associe une classe de [**\_ dépendance CIM**](cim-dependency.md) à un ou plusieurs objets de [**\_ configuration CIM**](cim-configuration.md) .</span><span class="sxs-lookup"><span data-stu-id="83188-105">The **CIM\_DependencyContext** relationship associates a [**CIM\_Dependency**](cim-dependency.md) class with one or more [**CIM\_Configuration**](cim-configuration.md) objects.</span></span> <span data-ttu-id="83188-106">Par exemple, les dépendances d’un système informatique peuvent changer en fonction du réseau auquel le système est attaché.</span><span class="sxs-lookup"><span data-stu-id="83188-106">For example, a computer system's dependencies can change based on the network to which the system is attached.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="83188-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="83188-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="83188-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="83188-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="83188-109">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="83188-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="83188-110">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="83188-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="83188-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="83188-111">Syntax</span></span>

``` syntax
[Abstract, Aggregation, Association, UUID("{A228E208-DB22-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_DependencyContext
{
  CIM_Configuration REF Context;
  CIM_Dependency    REF Dependency;
};
```

## <a name="members"></a><span data-ttu-id="83188-112">Membres</span><span class="sxs-lookup"><span data-stu-id="83188-112">Members</span></span>

<span data-ttu-id="83188-113">La classe **CIM \_ DependencyContext** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="83188-113">The **CIM\_DependencyContext** class has these types of members:</span></span>

-   [<span data-ttu-id="83188-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="83188-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="83188-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="83188-115">Properties</span></span>

<span data-ttu-id="83188-116">La classe **CIM \_ DependencyContext** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="83188-116">The **CIM\_DependencyContext** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="83188-117">**Contexte**</span><span class="sxs-lookup"><span data-stu-id="83188-117">**Context**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83188-118">Type de données **: \_ configuration CIM**</span><span class="sxs-lookup"><span data-stu-id="83188-118">Data type: **CIM\_Configuration**</span></span>
</dt> <dt>

<span data-ttu-id="83188-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="83188-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83188-120">Qualificateurs : [ **Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="83188-120">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="83188-121">Référence à l’objet de configuration qui agrège la dépendance.</span><span class="sxs-lookup"><span data-stu-id="83188-121">Reference to the configuration object that aggregates the dependency.</span></span>

</dd> <dt>

<span data-ttu-id="83188-122">**Dépendance**</span><span class="sxs-lookup"><span data-stu-id="83188-122">**Dependency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83188-123">Type de données **: \_ dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="83188-123">Data type: **CIM\_Dependency**</span></span>
</dt> <dt>

<span data-ttu-id="83188-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="83188-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83188-125">Référence à une dépendance agrégée.</span><span class="sxs-lookup"><span data-stu-id="83188-125">Reference to an aggregated dependency.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="83188-126">Notes</span><span class="sxs-lookup"><span data-stu-id="83188-126">Remarks</span></span>

<span data-ttu-id="83188-127">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="83188-127">WMI does not implement this class.</span></span>

<span data-ttu-id="83188-128">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="83188-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="83188-129">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="83188-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="83188-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="83188-130">Requirements</span></span>



| <span data-ttu-id="83188-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="83188-131">Requirement</span></span> | <span data-ttu-id="83188-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="83188-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="83188-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="83188-133">Minimum supported client</span></span><br/> | <span data-ttu-id="83188-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="83188-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="83188-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="83188-135">Minimum supported server</span></span><br/> | <span data-ttu-id="83188-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="83188-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="83188-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="83188-137">Namespace</span></span><br/>                | <span data-ttu-id="83188-138">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="83188-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="83188-139">MOF</span><span class="sxs-lookup"><span data-stu-id="83188-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="83188-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="83188-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="83188-141">DLL</span><span class="sxs-lookup"><span data-stu-id="83188-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83188-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83188-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

