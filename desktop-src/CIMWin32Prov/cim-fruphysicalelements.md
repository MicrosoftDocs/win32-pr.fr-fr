---
description: La \_ classe CIM FRUPhysicalElements représente les éléments physiques qui composent une unité remplaçable sur site (FRU).
ms.assetid: ecdb19a8-5169-4370-8d2d-a21a0021ea5b
ms.tgt_platform: multiple
title: Classe CIM_FRUPhysicalElements
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FRUPhysicalElements
- CIM_FRUPhysicalElements.Component
- CIM_FRUPhysicalElements.FRU
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5c47160b9053a323f693d76f5b84d922c5120992
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950652"
---
# <a name="cim_fruphysicalelements-class"></a><span data-ttu-id="8e01f-103">\_Classe CIM FRUPhysicalElements</span><span class="sxs-lookup"><span data-stu-id="8e01f-103">CIM\_FRUPhysicalElements class</span></span>

<span data-ttu-id="8e01f-104">La classe **CIM \_ FRUPhysicalElements** représente les éléments physiques qui composent une unité remplaçable sur site (FRU).</span><span class="sxs-lookup"><span data-stu-id="8e01f-104">The **CIM\_FRUPhysicalElements** class represents the physical elements that make up a field replaceable unit (FRU).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8e01f-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="8e01f-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8e01f-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="8e01f-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8e01f-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="8e01f-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="8e01f-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="8e01f-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e01f-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8e01f-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{977E36CA-DB2A-11d2-85FC-0000F8102E5F}"), Aggregation, Association, AMENDMENT]
class CIM_FRUPhysicalElements
{
  CIM_PhysicalElement REF Component;
  CIM_FRU             REF FRU;
};
```

## <a name="members"></a><span data-ttu-id="8e01f-110">Membres</span><span class="sxs-lookup"><span data-stu-id="8e01f-110">Members</span></span>

<span data-ttu-id="8e01f-111">La classe **CIM \_ FRUPhysicalElements** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="8e01f-111">The **CIM\_FRUPhysicalElements** class has these types of members:</span></span>

-   [<span data-ttu-id="8e01f-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8e01f-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8e01f-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8e01f-113">Properties</span></span>

<span data-ttu-id="8e01f-114">La classe **CIM \_ FRUPhysicalElements** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="8e01f-114">The **CIM\_FRUPhysicalElements** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8e01f-115">**Composant**</span><span class="sxs-lookup"><span data-stu-id="8e01f-115">**Component**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e01f-116">Type de données : **CIM \_ PhysicalElement**</span><span class="sxs-lookup"><span data-stu-id="8e01f-116">Data type: **CIM\_PhysicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="8e01f-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8e01f-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e01f-118">Référence à un élément physique qui fait partie de la FRU.</span><span class="sxs-lookup"><span data-stu-id="8e01f-118">Reference to a physical element that is a part of the FRU.</span></span>

</dd> <dt>

<span data-ttu-id="8e01f-119">**FRU**</span><span class="sxs-lookup"><span data-stu-id="8e01f-119">**FRU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e01f-120">Type de données **: \_ FRU CIM**</span><span class="sxs-lookup"><span data-stu-id="8e01f-120">Data type: **CIM\_FRU**</span></span>
</dt> <dt>

<span data-ttu-id="8e01f-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8e01f-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e01f-122">Qualificateurs : [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="8e01f-122">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="8e01f-123">Référence à la FRU.</span><span class="sxs-lookup"><span data-stu-id="8e01f-123">Reference to the FRU.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8e01f-124">Notes</span><span class="sxs-lookup"><span data-stu-id="8e01f-124">Remarks</span></span>

<span data-ttu-id="8e01f-125">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="8e01f-125">WMI does not implement this class.</span></span>

<span data-ttu-id="8e01f-126">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="8e01f-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8e01f-127">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="8e01f-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e01f-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8e01f-128">Requirements</span></span>



| <span data-ttu-id="8e01f-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8e01f-129">Requirement</span></span> | <span data-ttu-id="8e01f-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="8e01f-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8e01f-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8e01f-131">Minimum supported client</span></span><br/> | <span data-ttu-id="8e01f-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8e01f-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8e01f-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8e01f-133">Minimum supported server</span></span><br/> | <span data-ttu-id="8e01f-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8e01f-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8e01f-135">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8e01f-135">Namespace</span></span><br/>                | <span data-ttu-id="8e01f-136">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="8e01f-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8e01f-137">MOF</span><span class="sxs-lookup"><span data-stu-id="8e01f-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8e01f-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8e01f-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8e01f-139">DLL</span><span class="sxs-lookup"><span data-stu-id="8e01f-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e01f-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e01f-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

