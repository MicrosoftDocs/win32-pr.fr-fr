---
description: La \_ classe CIM ParticipatesInSet identifie les éléments physiques qui doivent être remplacés ensemble.
ms.assetid: 417607a3-6682-4745-a5ca-0538a0d4853d
ms.tgt_platform: multiple
title: Classe CIM_ParticipatesInSet
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ParticipatesInSet
- CIM_ParticipatesInSet.Element
- CIM_ParticipatesInSet.Set
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e1a581452ad6ce032dcb8d3ec5c6c0caa505f7bf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861393"
---
# <a name="cim_participatesinset-class"></a><span data-ttu-id="9b76c-103">\_Classe CIM ParticipatesInSet</span><span class="sxs-lookup"><span data-stu-id="9b76c-103">CIM\_ParticipatesInSet class</span></span>

<span data-ttu-id="9b76c-104">La classe **CIM \_ ParticipatesInSet** identifie les éléments physiques qui doivent être remplacés ensemble.</span><span class="sxs-lookup"><span data-stu-id="9b76c-104">The **CIM\_ParticipatesInSet** class identifies physical elements that should be replaced together.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9b76c-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="9b76c-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9b76c-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="9b76c-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9b76c-107">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="9b76c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="9b76c-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="9b76c-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b76c-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9b76c-109">Syntax</span></span>

``` syntax
[Abstract, Association, Aggregation, UUID("{FAF76B6D-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ParticipatesInSet
{
  CIM_PhysicalElement REF Element;
  CIM_ReplacementSet  REF Set;
};
```

## <a name="members"></a><span data-ttu-id="9b76c-110">Membres</span><span class="sxs-lookup"><span data-stu-id="9b76c-110">Members</span></span>

<span data-ttu-id="9b76c-111">La classe **CIM \_ ParticipatesInSet** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="9b76c-111">The **CIM\_ParticipatesInSet** class has these types of members:</span></span>

-   [<span data-ttu-id="9b76c-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9b76c-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9b76c-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9b76c-113">Properties</span></span>

<span data-ttu-id="9b76c-114">La classe **CIM \_ ParticipatesInSet** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="9b76c-114">The **CIM\_ParticipatesInSet** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9b76c-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="9b76c-115">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b76c-116">Type de données : **CIM \_ PhysicalElement**</span><span class="sxs-lookup"><span data-stu-id="9b76c-116">Data type: **CIM\_PhysicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="9b76c-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9b76c-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9b76c-118">Référence à l’élément physique qui doit être remplacé par d’autres éléments, comme un ensemble.</span><span class="sxs-lookup"><span data-stu-id="9b76c-118">Reference to the physical element that should be replaced with other elements, as a set.</span></span>

</dd> <dt>

<span data-ttu-id="9b76c-119">**Définir**</span><span class="sxs-lookup"><span data-stu-id="9b76c-119">**Set**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b76c-120">Type de données : **CIM \_ ReplacementSet**</span><span class="sxs-lookup"><span data-stu-id="9b76c-120">Data type: **CIM\_ReplacementSet**</span></span>
</dt> <dt>

<span data-ttu-id="9b76c-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9b76c-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b76c-122">Qualificateurs : [ **Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9b76c-122">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9b76c-123">Référence au jeu de remplacement d’éléments.</span><span class="sxs-lookup"><span data-stu-id="9b76c-123">Reference to the replacement set of elements.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9b76c-124">Notes</span><span class="sxs-lookup"><span data-stu-id="9b76c-124">Remarks</span></span>

<span data-ttu-id="9b76c-125">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="9b76c-125">WMI does not implement this class.</span></span>

<span data-ttu-id="9b76c-126">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="9b76c-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9b76c-127">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="9b76c-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b76c-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9b76c-128">Requirements</span></span>



| <span data-ttu-id="9b76c-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9b76c-129">Requirement</span></span> | <span data-ttu-id="9b76c-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="9b76c-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b76c-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9b76c-131">Minimum supported client</span></span><br/> | <span data-ttu-id="9b76c-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9b76c-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9b76c-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9b76c-133">Minimum supported server</span></span><br/> | <span data-ttu-id="9b76c-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9b76c-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9b76c-135">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9b76c-135">Namespace</span></span><br/>                | <span data-ttu-id="9b76c-136">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="9b76c-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9b76c-137">MOF</span><span class="sxs-lookup"><span data-stu-id="9b76c-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9b76c-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9b76c-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9b76c-139">DLL</span><span class="sxs-lookup"><span data-stu-id="9b76c-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b76c-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b76c-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

