---
description: La \_ classe CIM MemoryWithMedia associe la mémoire physique à un support physique et à sa cartouche. La mémoire fournit l’identification du média et stocke les données spécifiques à l’utilisateur.
ms.assetid: 99806d2d-6575-431d-9149-dc8ea767146c
ms.tgt_platform: multiple
title: Classe CIM_MemoryWithMedia
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MemoryWithMedia
- CIM_MemoryWithMedia.Dependent
- CIM_MemoryWithMedia.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3b990f8ba842f313449b6f24f4e2ce59787f7841
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321630"
---
# <a name="cim_memorywithmedia-class"></a><span data-ttu-id="240b4-104">\_Classe CIM MemoryWithMedia</span><span class="sxs-lookup"><span data-stu-id="240b4-104">CIM\_MemoryWithMedia class</span></span>

<span data-ttu-id="240b4-105">La classe **CIM \_ MemoryWithMedia** associe la mémoire physique à un support physique et à sa cartouche.</span><span class="sxs-lookup"><span data-stu-id="240b4-105">The **CIM\_MemoryWithMedia** class associates physical memory with a physical media and its cartridge.</span></span> <span data-ttu-id="240b4-106">La mémoire fournit l’identification du média et stocke les données spécifiques à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="240b4-106">The memory provides media identification and stores user-specific data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="240b4-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="240b4-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="240b4-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="240b4-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="240b4-109">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="240b4-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="240b4-110">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="240b4-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="240b4-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="240b4-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B7E-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_MemoryWithMedia : CIM_Dependency
{
  CIM_PhysicalMedia  REF Dependent;
  CIM_PhysicalMemory REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="240b4-112">Membres</span><span class="sxs-lookup"><span data-stu-id="240b4-112">Members</span></span>

<span data-ttu-id="240b4-113">La classe **CIM \_ MemoryWithMedia** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="240b4-113">The **CIM\_MemoryWithMedia** class has these types of members:</span></span>

-   [<span data-ttu-id="240b4-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="240b4-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="240b4-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="240b4-115">Properties</span></span>

<span data-ttu-id="240b4-116">La classe **CIM \_ MemoryWithMedia** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="240b4-116">The **CIM\_MemoryWithMedia** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="240b4-117">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="240b4-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="240b4-118">Type de données : **CIM \_ PhysicalMemory**</span><span class="sxs-lookup"><span data-stu-id="240b4-118">Data type: **CIM\_PhysicalMemory**</span></span>
</dt> <dt>

<span data-ttu-id="240b4-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="240b4-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="240b4-120">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="240b4-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="240b4-121">[**\_ PhysicalMemory CIM**](cim-physicalmemory.md) qui décrit la mémoire associée au support physique.</span><span class="sxs-lookup"><span data-stu-id="240b4-121">A [**CIM\_PhysicalMemory**](cim-physicalmemory.md) that describes the memory associated with physical media.</span></span>

</dd> <dt>

<span data-ttu-id="240b4-122">**Charge**</span><span class="sxs-lookup"><span data-stu-id="240b4-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="240b4-123">Type de données : **CIM \_ PhysicalMedia**</span><span class="sxs-lookup"><span data-stu-id="240b4-123">Data type: **CIM\_PhysicalMedia**</span></span>
</dt> <dt>

<span data-ttu-id="240b4-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="240b4-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="240b4-125">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="240b4-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="240b4-126">[**\_ PhysicalMedia CIM**](cim-physicalmedia.md) qui décrit le support physique.</span><span class="sxs-lookup"><span data-stu-id="240b4-126">A [**CIM\_PhysicalMedia**](cim-physicalmedia.md) that describes the physical media.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="240b4-127">Notes</span><span class="sxs-lookup"><span data-stu-id="240b4-127">Remarks</span></span>

<span data-ttu-id="240b4-128">**CIM \_ MemoryWithMedia** est héritée de la [**\_ dépendance CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="240b4-128">**CIM\_MemoryWithMedia** is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="240b4-129">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="240b4-129">WMI does not implement this class.</span></span>

<span data-ttu-id="240b4-130">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="240b4-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="240b4-131">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="240b4-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="240b4-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="240b4-132">Requirements</span></span>



| <span data-ttu-id="240b4-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="240b4-133">Requirement</span></span> | <span data-ttu-id="240b4-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="240b4-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="240b4-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="240b4-135">Minimum supported client</span></span><br/> | <span data-ttu-id="240b4-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="240b4-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="240b4-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="240b4-137">Minimum supported server</span></span><br/> | <span data-ttu-id="240b4-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="240b4-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="240b4-139">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="240b4-139">Namespace</span></span><br/>                | <span data-ttu-id="240b4-140">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="240b4-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="240b4-141">MOF</span><span class="sxs-lookup"><span data-stu-id="240b4-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="240b4-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="240b4-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="240b4-143">DLL</span><span class="sxs-lookup"><span data-stu-id="240b4-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="240b4-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="240b4-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="240b4-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="240b4-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="240b4-146">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="240b4-146">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

