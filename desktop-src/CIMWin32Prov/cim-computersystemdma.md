---
description: La \_ classe CIM ComputerSystemDMA représente une association entre un système informatique et ses canaux DMA (Direct Memory Access) disponibles.
ms.assetid: 7d5bce4b-973f-4452-b403-a2196bd4017a
ms.tgt_platform: multiple
title: Classe CIM_ComputerSystemDMA
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ComputerSystemDMA
- CIM_ComputerSystemDMA.PartComponent
- CIM_ComputerSystemDMA.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 23748a3b10c11878069a81cd82f7f69d0ab75792
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533585"
---
# <a name="cim_computersystemdma-class"></a><span data-ttu-id="ef0c6-103">\_Classe CIM ComputerSystemDMA</span><span class="sxs-lookup"><span data-stu-id="ef0c6-103">CIM\_ComputerSystemDMA class</span></span>

<span data-ttu-id="ef0c6-104">La classe **CIM \_ ComputerSystemDMA** représente une association entre un système informatique et ses canaux DMA (Direct Memory Access) disponibles.</span><span class="sxs-lookup"><span data-stu-id="ef0c6-104">The **CIM\_ComputerSystemDMA** class represents an association between a computer system and its available direct memory access (DMA) channels.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ef0c6-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="ef0c6-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ef0c6-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ef0c6-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ef0c6-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="ef0c6-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="ef0c6-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="ef0c6-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef0c6-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ef0c6-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{9B81340B-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_ComputerSystemDMA : CIM_ComputerSystemResource
{
  CIM_DMA            REF PartComponent;
  CIM_ComputerSystem REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="ef0c6-110">Membres</span><span class="sxs-lookup"><span data-stu-id="ef0c6-110">Members</span></span>

<span data-ttu-id="ef0c6-111">La classe **CIM \_ ComputerSystemDMA** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ef0c6-111">The **CIM\_ComputerSystemDMA** class has these types of members:</span></span>

-   [<span data-ttu-id="ef0c6-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ef0c6-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ef0c6-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ef0c6-113">Properties</span></span>

<span data-ttu-id="ef0c6-114">La classe **CIM \_ ComputerSystemDMA** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="ef0c6-114">The **CIM\_ComputerSystemDMA** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ef0c6-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="ef0c6-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0c6-116">Type de données **: \_ CIM CIM**</span><span class="sxs-lookup"><span data-stu-id="ef0c6-116">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="ef0c6-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ef0c6-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef0c6-118">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="ef0c6-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="ef0c6-119">Un [**\_ ComputerSystem CIM**](cim-computersystem.md) qui décrit l’ordinateur associé au DMA.</span><span class="sxs-lookup"><span data-stu-id="ef0c6-119">A [**CIM\_ComputerSystem**](cim-computersystem.md) that describes the computer associated with the DMA.</span></span>

</dd> <dt>

<span data-ttu-id="ef0c6-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="ef0c6-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0c6-121">Type de données **: \_ DMA CIM**</span><span class="sxs-lookup"><span data-stu-id="ef0c6-121">Data type: **CIM\_DMA**</span></span>
</dt> <dt>

<span data-ttu-id="ef0c6-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ef0c6-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef0c6-123">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="ef0c6-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="ef0c6-124">Un [**\_ DMA CIM**](cim-dma.md) qui décrit un canal DMA du système informatique.</span><span class="sxs-lookup"><span data-stu-id="ef0c6-124">A [**CIM\_DMA**](cim-dma.md) that describes a DMA channel of the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ef0c6-125">Notes</span><span class="sxs-lookup"><span data-stu-id="ef0c6-125">Remarks</span></span>

<span data-ttu-id="ef0c6-126">La classe **CIM \_ ComputerSystemDMA** est dérivée de [**CIM \_ ComputerSystemResource**](cim-computersystemresource.md).</span><span class="sxs-lookup"><span data-stu-id="ef0c6-126">The **CIM\_ComputerSystemDMA** class is derived from [**CIM\_ComputerSystemResource**](cim-computersystemresource.md).</span></span>

<span data-ttu-id="ef0c6-127">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="ef0c6-127">WMI does not implement this class.</span></span>

<span data-ttu-id="ef0c6-128">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="ef0c6-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ef0c6-129">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="ef0c6-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef0c6-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ef0c6-130">Requirements</span></span>



| <span data-ttu-id="ef0c6-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ef0c6-131">Requirement</span></span> | <span data-ttu-id="ef0c6-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef0c6-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef0c6-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef0c6-133">Minimum supported client</span></span><br/> | <span data-ttu-id="ef0c6-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ef0c6-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ef0c6-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef0c6-135">Minimum supported server</span></span><br/> | <span data-ttu-id="ef0c6-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ef0c6-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ef0c6-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ef0c6-137">Namespace</span></span><br/>                | <span data-ttu-id="ef0c6-138">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="ef0c6-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ef0c6-139">MOF</span><span class="sxs-lookup"><span data-stu-id="ef0c6-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ef0c6-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ef0c6-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ef0c6-141">DLL</span><span class="sxs-lookup"><span data-stu-id="ef0c6-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef0c6-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef0c6-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef0c6-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef0c6-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef0c6-144">**\_COMPUTERSYSTEMRESOURCE CIM**</span><span class="sxs-lookup"><span data-stu-id="ef0c6-144">**CIM\_ComputerSystemResource**</span></span>](cim-computersystemresource.md)
</dt> </dl>

 

