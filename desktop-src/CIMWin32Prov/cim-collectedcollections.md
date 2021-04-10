---
description: La \_ classe COLLECTEDCOLLECTIONS CIM est une association d’agrégation qui représente une collection d’éléments système gérés (MSE) contenus dans une collection de MSEs.
ms.assetid: 7baaf429-1211-4545-ace2-c6312d53c0f6
ms.tgt_platform: multiple
title: Classe CIM_CollectedCollections
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectedCollections
- CIM_CollectedCollections.Collection
- CIM_CollectedCollections.CollectionInCollection
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e592c7799efc8c280d4cd64c2b54ed8a3ea328f6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950701"
---
# <a name="cim_collectedcollections-class"></a><span data-ttu-id="51939-103">\_Classe CIM CollectedCollections</span><span class="sxs-lookup"><span data-stu-id="51939-103">CIM\_CollectedCollections class</span></span>

<span data-ttu-id="51939-104">La **classe \_ CollectedCollections CIM** est une association d’agrégation qui représente une collection d’éléments système gérés (MSE) contenus dans une collection de MSEs.</span><span class="sxs-lookup"><span data-stu-id="51939-104">The **CIM\_CollectedCollections** class is an aggregation association that represents a collection of Managed System Elements (MSE) contained in a collection of MSEs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="51939-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="51939-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="51939-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="51939-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="51939-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="51939-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="51939-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="51939-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="51939-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="51939-109">Syntax</span></span>

``` syntax
class CIM_CollectedCollections
{
  CIM_CollectionOfMSEs REF Collection;
  CIM_CollectionOfMSEs REF CollectionInCollection;
};
```

## <a name="members"></a><span data-ttu-id="51939-110">Membres</span><span class="sxs-lookup"><span data-stu-id="51939-110">Members</span></span>

<span data-ttu-id="51939-111">La classe **CIM \_ CollectedCollections** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="51939-111">The **CIM\_CollectedCollections** class has these types of members:</span></span>

-   [<span data-ttu-id="51939-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="51939-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="51939-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="51939-113">Properties</span></span>

<span data-ttu-id="51939-114">La classe **CIM \_ CollectedCollections** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="51939-114">The **CIM\_CollectedCollections** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="51939-115">**Collection**</span><span class="sxs-lookup"><span data-stu-id="51939-115">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51939-116">Type de données : **CIM \_ CollectionOfMSEs**</span><span class="sxs-lookup"><span data-stu-id="51939-116">Data type: **CIM\_CollectionOfMSEs**</span></span>
</dt> <dt>

<span data-ttu-id="51939-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="51939-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51939-118">Référence au « niveau supérieur » ou à l’élément parent dans l’agrégation.</span><span class="sxs-lookup"><span data-stu-id="51939-118">Reference to the "higher level" or parent element in the aggregation.</span></span>

</dd> <dt>

<span data-ttu-id="51939-119">**CollectionInCollection**</span><span class="sxs-lookup"><span data-stu-id="51939-119">**CollectionInCollection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51939-120">Type de données : **CIM \_ CollectionOfMSEs**</span><span class="sxs-lookup"><span data-stu-id="51939-120">Data type: **CIM\_CollectionOfMSEs**</span></span>
</dt> <dt>

<span data-ttu-id="51939-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="51939-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51939-122">Référence à la **collection**« collectée ».</span><span class="sxs-lookup"><span data-stu-id="51939-122">Reference to the "collected" **Collection**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="51939-123">Notes</span><span class="sxs-lookup"><span data-stu-id="51939-123">Remarks</span></span>

<span data-ttu-id="51939-124">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="51939-124">WMI does not implement this class.</span></span>

<span data-ttu-id="51939-125">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="51939-125">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="51939-126">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="51939-126">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="51939-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="51939-127">Requirements</span></span>



| <span data-ttu-id="51939-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="51939-128">Requirement</span></span> | <span data-ttu-id="51939-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="51939-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="51939-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="51939-130">Minimum supported client</span></span><br/> | <span data-ttu-id="51939-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="51939-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="51939-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="51939-132">Minimum supported server</span></span><br/> | <span data-ttu-id="51939-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="51939-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="51939-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="51939-134">Namespace</span></span><br/>                | <span data-ttu-id="51939-135">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="51939-135">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="51939-136">MOF</span><span class="sxs-lookup"><span data-stu-id="51939-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="51939-137"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="51939-137"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="51939-138">DLL</span><span class="sxs-lookup"><span data-stu-id="51939-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="51939-139"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="51939-139"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




