---
description: La \_ classe de statistiques CIM représente une association qui associe les éléments système gérés aux groupes statistiques qui s’y appliquent.
ms.assetid: fc75991b-adcd-4e47-b610-7503f6bb7c03
ms.tgt_platform: multiple
title: Classe CIM_Statistics
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Statistics
- CIM_Statistics.Element
- CIM_Statistics.Stats
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b35299a52c771ee3bcb76673ef1e2164af3b3180
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950455"
---
# <a name="cim_statistics-class"></a><span data-ttu-id="6b10d-103">\_Classe de statistiques CIM</span><span class="sxs-lookup"><span data-stu-id="6b10d-103">CIM\_Statistics class</span></span>

<span data-ttu-id="6b10d-104">La classe de **\_ statistiques CIM** représente une association qui associe les éléments système gérés aux groupes statistiques qui s’y appliquent.</span><span class="sxs-lookup"><span data-stu-id="6b10d-104">The **CIM\_Statistics** class represents an association that relates managed system elements to the statistical groups that apply to them.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6b10d-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="6b10d-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6b10d-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6b10d-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="6b10d-107">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="6b10d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="6b10d-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="6b10d-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b10d-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6b10d-109">Syntax</span></span>

``` syntax
[Abstract, Association, UUID("{956597A3-7D80-11D2-AAD3-006008C78BC7}"), AMENDMENT]
class CIM_Statistics
{
  CIM_ManagedSystemElement   REF Element;
  CIM_StatisticalInformation REF Stats;
};
```

## <a name="members"></a><span data-ttu-id="6b10d-110">Membres</span><span class="sxs-lookup"><span data-stu-id="6b10d-110">Members</span></span>

<span data-ttu-id="6b10d-111">La classe de **\_ statistiques CIM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="6b10d-111">The **CIM\_Statistics** class has these types of members:</span></span>

-   [<span data-ttu-id="6b10d-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6b10d-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6b10d-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6b10d-113">Properties</span></span>

<span data-ttu-id="6b10d-114">La classe de **\_ statistiques CIM** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="6b10d-114">The **CIM\_Statistics** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6b10d-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="6b10d-115">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b10d-116">Type de données **: \_ CIM CIM**</span><span class="sxs-lookup"><span data-stu-id="6b10d-116">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="6b10d-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6b10d-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b10d-118">Référence à la [**classe \_ ManagedSystemElement CIM**](cim-managedsystemelement.md) pour laquelle des données statistiques ou métriques sont définies.</span><span class="sxs-lookup"><span data-stu-id="6b10d-118">Reference to the [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) class for which statistical or metric data is defined.</span></span>

</dd> <dt>

<span data-ttu-id="6b10d-119">**Stats**</span><span class="sxs-lookup"><span data-stu-id="6b10d-119">**Stats**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b10d-120">Type de données : **CIM \_ StatisticalInformation**</span><span class="sxs-lookup"><span data-stu-id="6b10d-120">Data type: **CIM\_StatisticalInformation**</span></span>
</dt> <dt>

<span data-ttu-id="6b10d-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6b10d-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b10d-122">Référence aux informations statistiques ou à l’objet.</span><span class="sxs-lookup"><span data-stu-id="6b10d-122">Reference to the statistical information or object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6b10d-123">Notes</span><span class="sxs-lookup"><span data-stu-id="6b10d-123">Remarks</span></span>

<span data-ttu-id="6b10d-124">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="6b10d-124">WMI does not implement this class.</span></span>

<span data-ttu-id="6b10d-125">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="6b10d-125">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6b10d-126">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="6b10d-126">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b10d-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6b10d-127">Requirements</span></span>



| <span data-ttu-id="6b10d-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6b10d-128">Requirement</span></span> | <span data-ttu-id="6b10d-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="6b10d-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b10d-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6b10d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="6b10d-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6b10d-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6b10d-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6b10d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="6b10d-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6b10d-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6b10d-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6b10d-134">Namespace</span></span><br/>                | <span data-ttu-id="6b10d-135">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="6b10d-135">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6b10d-136">MOF</span><span class="sxs-lookup"><span data-stu-id="6b10d-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6b10d-137"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6b10d-137"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6b10d-138">DLL</span><span class="sxs-lookup"><span data-stu-id="6b10d-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b10d-139"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b10d-139"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




