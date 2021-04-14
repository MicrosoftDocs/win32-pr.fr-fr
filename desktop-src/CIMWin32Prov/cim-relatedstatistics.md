---
description: L' \_ Association CIM RelatedStatistics représente les hiérarchies et les dépendances des \_ classes StatisticalInformation CIM associées.
ms.assetid: f5cea01d-7854-4ad4-a89e-db0ce9f4a83f
ms.tgt_platform: multiple
title: Classe CIM_RelatedStatistics
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RelatedStatistics
- CIM_RelatedStatistics.RelatedStats
- CIM_RelatedStatistics.Stats
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 01fb70535a4ae8f84d637cf92a06eee4fe318a49
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523116"
---
# <a name="cim_relatedstatistics-class"></a><span data-ttu-id="63803-103">\_Classe CIM RelatedStatistics</span><span class="sxs-lookup"><span data-stu-id="63803-103">CIM\_RelatedStatistics class</span></span>

<span data-ttu-id="63803-104">L’Association **CIM \_ RelatedStatistics** représente les hiérarchies et les dépendances des classes [**\_ StatisticalInformation CIM**](cim-statisticalinformation.md) associées.</span><span class="sxs-lookup"><span data-stu-id="63803-104">The **CIM\_RelatedStatistics** association represents hierarchies and dependencies of related [**CIM\_StatisticalInformation**](cim-statisticalinformation.md) classes.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="63803-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="63803-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="63803-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="63803-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="63803-107">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="63803-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="63803-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="63803-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="63803-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="63803-109">Syntax</span></span>

``` syntax
[Abstract, Association, UUID("{956597A4-7D80-11D2-AAD3-006008C78BC7}"), AMENDMENT]
class CIM_RelatedStatistics
{
  CIM_StatisticalInformation REF RelatedStats;
  CIM_StatisticalInformation REF Stats;
};
```

## <a name="members"></a><span data-ttu-id="63803-110">Membres</span><span class="sxs-lookup"><span data-stu-id="63803-110">Members</span></span>

<span data-ttu-id="63803-111">La classe **CIM \_ RelatedStatistics** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="63803-111">The **CIM\_RelatedStatistics** class has these types of members:</span></span>

-   [<span data-ttu-id="63803-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="63803-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="63803-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="63803-113">Properties</span></span>

<span data-ttu-id="63803-114">La classe **CIM \_ RelatedStatistics** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="63803-114">The **CIM\_RelatedStatistics** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="63803-115">**RelatedStats**</span><span class="sxs-lookup"><span data-stu-id="63803-115">**RelatedStats**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63803-116">Type de données : **CIM \_ StatisticalInformation**</span><span class="sxs-lookup"><span data-stu-id="63803-116">Data type: **CIM\_StatisticalInformation**</span></span>
</dt> <dt>

<span data-ttu-id="63803-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63803-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="63803-118">Référence aux statistiques ou mesures associées.</span><span class="sxs-lookup"><span data-stu-id="63803-118">Reference to the related statistics or metrics.</span></span>

</dd> <dt>

<span data-ttu-id="63803-119">**Stats**</span><span class="sxs-lookup"><span data-stu-id="63803-119">**Stats**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63803-120">Type de données : **CIM \_ StatisticalInformation**</span><span class="sxs-lookup"><span data-stu-id="63803-120">Data type: **CIM\_StatisticalInformation**</span></span>
</dt> <dt>

<span data-ttu-id="63803-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63803-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="63803-122">Référence aux informations statistiques ou à l’objet.</span><span class="sxs-lookup"><span data-stu-id="63803-122">Reference to the statistic information or object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="63803-123">Notes</span><span class="sxs-lookup"><span data-stu-id="63803-123">Remarks</span></span>

<span data-ttu-id="63803-124">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="63803-124">WMI does not implement this class.</span></span>

<span data-ttu-id="63803-125">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="63803-125">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="63803-126">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="63803-126">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="63803-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="63803-127">Requirements</span></span>



| <span data-ttu-id="63803-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="63803-128">Requirement</span></span> | <span data-ttu-id="63803-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="63803-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="63803-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="63803-130">Minimum supported client</span></span><br/> | <span data-ttu-id="63803-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="63803-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="63803-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="63803-132">Minimum supported server</span></span><br/> | <span data-ttu-id="63803-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="63803-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="63803-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="63803-134">Namespace</span></span><br/>                | <span data-ttu-id="63803-135">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="63803-135">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="63803-136">MOF</span><span class="sxs-lookup"><span data-stu-id="63803-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="63803-137"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="63803-137"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="63803-138">DLL</span><span class="sxs-lookup"><span data-stu-id="63803-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63803-139"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63803-139"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




