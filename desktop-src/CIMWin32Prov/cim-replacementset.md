---
description: La \_ classe CIM ReplacementSet agrège les éléments physiques qui doivent être remplacés ensemble.
ms.assetid: db55ae2d-49b3-4cc9-95ee-1e757f58a427
ms.tgt_platform: multiple
title: Classe CIM_ReplacementSet
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ReplacementSet
- CIM_ReplacementSet.Description
- CIM_ReplacementSet.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: defc63628e494465d7a31d8adcea758e538c4c9e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110254"
---
# <a name="cim_replacementset-class"></a><span data-ttu-id="d3124-103">\_Classe CIM ReplacementSet</span><span class="sxs-lookup"><span data-stu-id="d3124-103">CIM\_ReplacementSet class</span></span>

<span data-ttu-id="d3124-104">La classe **CIM \_ ReplacementSet** agrège les éléments physiques qui doivent être remplacés ensemble.</span><span class="sxs-lookup"><span data-stu-id="d3124-104">The **CIM\_ReplacementSet** class aggregates physical elements that must be replaced together.</span></span> <span data-ttu-id="d3124-105">Par exemple, lors du remplacement d’une carte mémoire, les puces de mémoire du composant peuvent également être supprimées et remplacées.</span><span class="sxs-lookup"><span data-stu-id="d3124-105">For example, when replacing a memory card, the component memory chips can also be removed and replaced.</span></span> <span data-ttu-id="d3124-106">Cette association peut être utilisée pour remplacer ou mettre à niveau un ensemble de puces mémoire.</span><span class="sxs-lookup"><span data-stu-id="d3124-106">Or, this association can be used to replace or upgrade a set of memory chips.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d3124-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="d3124-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d3124-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="d3124-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d3124-109">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="d3124-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="d3124-110">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="d3124-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3124-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d3124-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B6C-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ReplacementSet
{
  string Description;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="d3124-112">Membres</span><span class="sxs-lookup"><span data-stu-id="d3124-112">Members</span></span>

<span data-ttu-id="d3124-113">La classe **CIM \_ ReplacementSet** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d3124-113">The **CIM\_ReplacementSet** class has these types of members:</span></span>

-   [<span data-ttu-id="d3124-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d3124-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d3124-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d3124-115">Properties</span></span>

<span data-ttu-id="d3124-116">La classe **CIM \_ ReplacementSet** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="d3124-116">The **CIM\_ReplacementSet** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d3124-117">**Description**</span><span class="sxs-lookup"><span data-stu-id="d3124-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3124-118">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d3124-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d3124-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d3124-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3124-120">Chaîne de forme libre qui spécifie les informations relatives à cette classe.</span><span class="sxs-lookup"><span data-stu-id="d3124-120">Free-form string that specifies information related to this class.</span></span> <span data-ttu-id="d3124-121">L’objectif de l’ensemble, ou les informations relatives à la façon dont les éléments du composant sont remplacés, peuvent être inclus dans cette propriété.</span><span class="sxs-lookup"><span data-stu-id="d3124-121">The purpose of the set, or information related to how the component elements are replaced, can be included in this property.</span></span>

</dd> <dt>

<span data-ttu-id="d3124-122">**Nom**</span><span class="sxs-lookup"><span data-stu-id="d3124-122">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3124-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d3124-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d3124-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d3124-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d3124-125">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="d3124-125">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="d3124-126">Chaîne de forme libre qui définit une étiquette pour cette propriété.</span><span class="sxs-lookup"><span data-stu-id="d3124-126">Free-form string that defines a label for this property.</span></span> <span data-ttu-id="d3124-127">Cette propriété est la clé de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d3124-127">This property is the key for the object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d3124-128">Notes</span><span class="sxs-lookup"><span data-stu-id="d3124-128">Remarks</span></span>

<span data-ttu-id="d3124-129">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="d3124-129">WMI does not implement this class.</span></span>

<span data-ttu-id="d3124-130">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="d3124-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d3124-131">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="d3124-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3124-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d3124-132">Requirements</span></span>



| <span data-ttu-id="d3124-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d3124-133">Requirement</span></span> | <span data-ttu-id="d3124-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="d3124-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d3124-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d3124-135">Minimum supported client</span></span><br/> | <span data-ttu-id="d3124-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d3124-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d3124-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d3124-137">Minimum supported server</span></span><br/> | <span data-ttu-id="d3124-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d3124-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d3124-139">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d3124-139">Namespace</span></span><br/>                | <span data-ttu-id="d3124-140">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="d3124-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d3124-141">MOF</span><span class="sxs-lookup"><span data-stu-id="d3124-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d3124-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d3124-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d3124-143">DLL</span><span class="sxs-lookup"><span data-stu-id="d3124-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3124-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3124-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

