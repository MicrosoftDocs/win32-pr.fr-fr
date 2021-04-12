---
description: La \_ classe CIM ElementCapacity associe un \_ objet PhysicalCapacity CIM à un ou plusieurs éléments physiques. Elle associe une description de la configuration matérielle minimale et maximale (ou des fonctionnalités) aux éléments physiques en cours de description.
ms.assetid: 368c31e8-d56b-4b90-ba3f-20d9b0de8730
ms.tgt_platform: multiple
title: Classe CIM_ElementCapacity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementCapacity
- CIM_ElementCapacity.Capacity
- CIM_ElementCapacity.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7c6ecac913f6d4affcd9784a30d85fa08dfe0486
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483376"
---
# <a name="cim_elementcapacity-class"></a><span data-ttu-id="837ca-104">\_Classe CIM ElementCapacity</span><span class="sxs-lookup"><span data-stu-id="837ca-104">CIM\_ElementCapacity class</span></span>

<span data-ttu-id="837ca-105">La classe **CIM \_ ElementCapacity** associe un objet [**\_ PhysicalCapacity CIM**](cim-physicalcapacity.md) à un ou plusieurs éléments physiques.</span><span class="sxs-lookup"><span data-stu-id="837ca-105">The **CIM\_ElementCapacity** class associates a [**CIM\_PhysicalCapacity**](cim-physicalcapacity.md) object with one or more physical elements.</span></span> <span data-ttu-id="837ca-106">Elle associe une description de la configuration matérielle minimale et maximale (ou des fonctionnalités) aux éléments physiques en cours de description.</span><span class="sxs-lookup"><span data-stu-id="837ca-106">It associates a description of the minimum and maximum hardware requirements (or capabilities) to the physical elements being described.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="837ca-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="837ca-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="837ca-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="837ca-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="837ca-109">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="837ca-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="837ca-110">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="837ca-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="837ca-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="837ca-111">Syntax</span></span>

``` syntax
[Abstract, Association, UUID("{FAF76B6A-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ElementCapacity
{
  CIM_PhysicalCapacity REF Capacity;
  CIM_PhysicalElement  REF Element;
};
```

## <a name="members"></a><span data-ttu-id="837ca-112">Membres</span><span class="sxs-lookup"><span data-stu-id="837ca-112">Members</span></span>

<span data-ttu-id="837ca-113">La classe **CIM \_ ElementCapacity** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="837ca-113">The **CIM\_ElementCapacity** class has these types of members:</span></span>

-   [<span data-ttu-id="837ca-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="837ca-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="837ca-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="837ca-115">Properties</span></span>

<span data-ttu-id="837ca-116">La classe **CIM \_ ElementCapacity** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="837ca-116">The **CIM\_ElementCapacity** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="837ca-117">**Capacité**</span><span class="sxs-lookup"><span data-stu-id="837ca-117">**Capacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="837ca-118">Type de données : **CIM \_ PhysicalCapacity**</span><span class="sxs-lookup"><span data-stu-id="837ca-118">Data type: **CIM\_PhysicalCapacity**</span></span>
</dt> <dt>

<span data-ttu-id="837ca-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="837ca-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="837ca-120">Référence à la classe [**CIM \_ PhysicalCapacity**](cim-physicalcapacity.md) qui décrit les exigences minimales et maximales et la capacité à prendre en charge différents types de matériel pour un élément physique.</span><span class="sxs-lookup"><span data-stu-id="837ca-120">Reference to the [**CIM\_PhysicalCapacity**](cim-physicalcapacity.md) class that describes the minimum and maximum requirements and the ability to support different types of hardware for a physical element.</span></span>

</dd> <dt>

<span data-ttu-id="837ca-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="837ca-121">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="837ca-122">Type de données : **CIM \_ PhysicalElement**</span><span class="sxs-lookup"><span data-stu-id="837ca-122">Data type: **CIM\_PhysicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="837ca-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="837ca-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="837ca-124">Qualificateurs : [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="837ca-124">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="837ca-125">Référence à l’élément physique qui est décrit.</span><span class="sxs-lookup"><span data-stu-id="837ca-125">Reference to the physical element being described.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="837ca-126">Notes</span><span class="sxs-lookup"><span data-stu-id="837ca-126">Remarks</span></span>

<span data-ttu-id="837ca-127">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="837ca-127">WMI does not implement this class.</span></span>

<span data-ttu-id="837ca-128">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="837ca-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="837ca-129">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="837ca-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="837ca-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="837ca-130">Requirements</span></span>



| <span data-ttu-id="837ca-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="837ca-131">Requirement</span></span> | <span data-ttu-id="837ca-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="837ca-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="837ca-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="837ca-133">Minimum supported client</span></span><br/> | <span data-ttu-id="837ca-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="837ca-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="837ca-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="837ca-135">Minimum supported server</span></span><br/> | <span data-ttu-id="837ca-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="837ca-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="837ca-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="837ca-137">Namespace</span></span><br/>                | <span data-ttu-id="837ca-138">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="837ca-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="837ca-139">MOF</span><span class="sxs-lookup"><span data-stu-id="837ca-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="837ca-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="837ca-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="837ca-141">DLL</span><span class="sxs-lookup"><span data-stu-id="837ca-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="837ca-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="837ca-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

