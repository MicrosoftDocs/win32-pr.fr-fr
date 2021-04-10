---
description: L' \_ agrégation CIM StorageDefect collecte les erreurs de stockage pour une étendue de stockage.
ms.assetid: 7acd3d25-4691-43cb-badc-662684989345
ms.tgt_platform: multiple
title: Classe CIM_StorageDefect
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_StorageDefect
- CIM_StorageDefect.Error
- CIM_StorageDefect.Extent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8e6c2be45fe2f44afa407dc72e3ae90c486593ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950808"
---
# <a name="cim_storagedefect-class"></a><span data-ttu-id="36154-103">\_Classe CIM StorageDefect</span><span class="sxs-lookup"><span data-stu-id="36154-103">CIM\_StorageDefect class</span></span>

<span data-ttu-id="36154-104">L’agrégation **CIM \_ StorageDefect** collecte les erreurs de stockage pour une étendue de stockage.</span><span class="sxs-lookup"><span data-stu-id="36154-104">The **CIM\_StorageDefect** aggregation collects the storage errors for a storage extent.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="36154-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="36154-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="36154-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="36154-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="36154-107">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="36154-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="36154-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="36154-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="36154-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="36154-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{5CC70817-DB31-11d2-85FC-0000F8102E5F}"), Aggregation, Association, AMENDMENT]
class CIM_StorageDefect
{
  CIM_StorageError  REF Error;
  CIM_StorageExtent REF Extent;
};
```

## <a name="members"></a><span data-ttu-id="36154-110">Membres</span><span class="sxs-lookup"><span data-stu-id="36154-110">Members</span></span>

<span data-ttu-id="36154-111">La classe **CIM \_ StorageDefect** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="36154-111">The **CIM\_StorageDefect** class has these types of members:</span></span>

-   [<span data-ttu-id="36154-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="36154-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="36154-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="36154-113">Properties</span></span>

<span data-ttu-id="36154-114">La classe **CIM \_ StorageDefect** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="36154-114">The **CIM\_StorageDefect** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="36154-115">**Error**</span><span class="sxs-lookup"><span data-stu-id="36154-115">**Error**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36154-116">Type de données : **CIM \_ StorageError**</span><span class="sxs-lookup"><span data-stu-id="36154-116">Data type: **CIM\_StorageError**</span></span>
</dt> <dt>

<span data-ttu-id="36154-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="36154-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36154-118">Qualificateurs : [ **faible**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="36154-118">Qualifiers: [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="36154-119">Référence à l’objet d’erreur, qui définit les adresses de début et de fin qui sont mappées en dehors de l’étendue de stockage.</span><span class="sxs-lookup"><span data-stu-id="36154-119">Reference to the error object, which defines the starting and ending addresses that are mapped out of the storage extent.</span></span>

</dd> <dt>

<span data-ttu-id="36154-120">**Extension**</span><span class="sxs-lookup"><span data-stu-id="36154-120">**Extent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36154-121">Type de données : **CIM \_ StorageExtent**</span><span class="sxs-lookup"><span data-stu-id="36154-121">Data type: **CIM\_StorageExtent**</span></span>
</dt> <dt>

<span data-ttu-id="36154-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="36154-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36154-123">Qualificateurs : [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="36154-123">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="36154-124">Référence à l’extension de stockage sur laquelle les erreurs se sont produites.</span><span class="sxs-lookup"><span data-stu-id="36154-124">Reference to the storage extent on which the errors occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="36154-125">Notes</span><span class="sxs-lookup"><span data-stu-id="36154-125">Remarks</span></span>

<span data-ttu-id="36154-126">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="36154-126">WMI does not implement this class.</span></span>

<span data-ttu-id="36154-127">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="36154-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="36154-128">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="36154-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="36154-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="36154-129">Requirements</span></span>



| <span data-ttu-id="36154-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="36154-130">Requirement</span></span> | <span data-ttu-id="36154-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="36154-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="36154-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="36154-132">Minimum supported client</span></span><br/> | <span data-ttu-id="36154-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="36154-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="36154-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="36154-134">Minimum supported server</span></span><br/> | <span data-ttu-id="36154-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="36154-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="36154-136">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="36154-136">Namespace</span></span><br/>                | <span data-ttu-id="36154-137">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="36154-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="36154-138">MOF</span><span class="sxs-lookup"><span data-stu-id="36154-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="36154-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="36154-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="36154-140">DLL</span><span class="sxs-lookup"><span data-stu-id="36154-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36154-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36154-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

