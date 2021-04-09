---
description: La \_ classe CIM ResidesOnExtent représente une association entre un système de fichiers et l’extension de stockage où elle se trouve. En règle générale, un système de fichiers réside sur un disque logique.
ms.assetid: 911a81e9-3032-41ff-a337-044c06d02307
ms.tgt_platform: multiple
title: Classe CIM_ResidesOnExtent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResidesOnExtent
- CIM_ResidesOnExtent.Dependent
- CIM_ResidesOnExtent.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 526023fbcc1c961ecaca068be8b0d4ce3e2f84f8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111535"
---
# <a name="cim_residesonextent-class"></a><span data-ttu-id="34048-104">\_Classe CIM ResidesOnExtent</span><span class="sxs-lookup"><span data-stu-id="34048-104">CIM\_ResidesOnExtent class</span></span>

<span data-ttu-id="34048-105">La classe **CIM \_ ResidesOnExtent** représente une association entre un système de fichiers et l’extension de stockage où elle se trouve.</span><span class="sxs-lookup"><span data-stu-id="34048-105">The **CIM\_ResidesOnExtent** class represents an association between a file system and the storage extent where it is located.</span></span> <span data-ttu-id="34048-106">En règle générale, un système de fichiers réside sur un disque logique.</span><span class="sxs-lookup"><span data-stu-id="34048-106">Typically, a file system resides on a logical disk.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="34048-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="34048-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="34048-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="34048-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="34048-109">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="34048-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="34048-110">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="34048-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="34048-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="34048-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{10458E26-DB37-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_ResidesOnExtent : CIM_Dependency
{
  CIM_FileSystem    REF Dependent;
  CIM_StorageExtent REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="34048-112">Membres</span><span class="sxs-lookup"><span data-stu-id="34048-112">Members</span></span>

<span data-ttu-id="34048-113">La classe **CIM \_ ResidesOnExtent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="34048-113">The **CIM\_ResidesOnExtent** class has these types of members:</span></span>

-   [<span data-ttu-id="34048-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="34048-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="34048-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="34048-115">Properties</span></span>

<span data-ttu-id="34048-116">La classe **CIM \_ ResidesOnExtent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="34048-116">The **CIM\_ResidesOnExtent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="34048-117">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="34048-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34048-118">Type de données : **CIM \_ StorageExtent**</span><span class="sxs-lookup"><span data-stu-id="34048-118">Data type: **CIM\_StorageExtent**</span></span>
</dt> <dt>

<span data-ttu-id="34048-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="34048-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34048-120">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="34048-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="34048-121">[**\_ StorageExtent CIM**](cim-storageextent.md) qui décrit l’extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="34048-121">A [**CIM\_StorageExtent**](cim-storageextent.md) that describes the storage extent.</span></span>

</dd> <dt>

<span data-ttu-id="34048-122">**Charge**</span><span class="sxs-lookup"><span data-stu-id="34048-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34048-123">Type de données **: \_ système de fichiers CIM**</span><span class="sxs-lookup"><span data-stu-id="34048-123">Data type: **CIM\_FileSystem**</span></span>
</dt> <dt>

<span data-ttu-id="34048-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="34048-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34048-125">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="34048-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="34048-126">Un système de fichiers [**CIM \_**](cim-filesystem.md) qui décrit le système de fichiers qui se trouve sur l’extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="34048-126">A [**CIM\_FileSystem**](cim-filesystem.md) that describes the file system that is located on the storage extent.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="34048-127">Notes</span><span class="sxs-lookup"><span data-stu-id="34048-127">Remarks</span></span>

<span data-ttu-id="34048-128">La classe **CIM \_ ResidesOnExtent** est dérivée de la [**\_ dépendance CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="34048-128">The **CIM\_ResidesOnExtent** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="34048-129">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="34048-129">WMI does not implement this class.</span></span>

<span data-ttu-id="34048-130">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="34048-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="34048-131">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="34048-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="34048-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="34048-132">Requirements</span></span>



| <span data-ttu-id="34048-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="34048-133">Requirement</span></span> | <span data-ttu-id="34048-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="34048-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="34048-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="34048-135">Minimum supported client</span></span><br/> | <span data-ttu-id="34048-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="34048-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="34048-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="34048-137">Minimum supported server</span></span><br/> | <span data-ttu-id="34048-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="34048-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="34048-139">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="34048-139">Namespace</span></span><br/>                | <span data-ttu-id="34048-140">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="34048-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="34048-141">MOF</span><span class="sxs-lookup"><span data-stu-id="34048-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="34048-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="34048-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="34048-143">DLL</span><span class="sxs-lookup"><span data-stu-id="34048-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="34048-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34048-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34048-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="34048-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34048-146">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="34048-146">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

