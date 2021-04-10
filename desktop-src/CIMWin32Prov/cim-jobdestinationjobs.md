---
description: L' \_ Association CIM JobDestinationJobs décrit l’endroit où un travail est soumis pour traitement (c’est-à-dire la destination du travail).
ms.assetid: 6f732d34-2284-4909-a966-6b4066780cb0
ms.tgt_platform: multiple
title: Classe CIM_JobDestinationJobs
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_JobDestinationJobs
- CIM_JobDestinationJobs.Dependent
- CIM_JobDestinationJobs.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4e59e20f776c410db53294b6f6e98a1b13aef0de
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201023"
---
# <a name="cim_jobdestinationjobs-class"></a><span data-ttu-id="92fb2-103">\_Classe CIM JobDestinationJobs</span><span class="sxs-lookup"><span data-stu-id="92fb2-103">CIM\_JobDestinationJobs class</span></span>

<span data-ttu-id="92fb2-104">L’Association **CIM \_ JobDestinationJobs** décrit l’endroit où un travail est soumis pour traitement (c’est-à-dire la destination du travail).</span><span class="sxs-lookup"><span data-stu-id="92fb2-104">The **CIM\_JobDestinationJobs** association describes where a job is submitted for processing (that is, to which job destination).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="92fb2-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="92fb2-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="92fb2-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="92fb2-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="92fb2-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="92fb2-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="92fb2-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="92fb2-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="92fb2-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="92fb2-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8D079BEE-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_JobDestinationJobs : CIM_Dependency
{
  CIM_Job            REF Dependent;
  CIM_JobDestination REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="92fb2-110">Membres</span><span class="sxs-lookup"><span data-stu-id="92fb2-110">Members</span></span>

<span data-ttu-id="92fb2-111">La classe **CIM \_ JobDestinationJobs** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="92fb2-111">The **CIM\_JobDestinationJobs** class has these types of members:</span></span>

-   [<span data-ttu-id="92fb2-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="92fb2-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="92fb2-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="92fb2-113">Properties</span></span>

<span data-ttu-id="92fb2-114">La classe **CIM \_ JobDestinationJobs** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="92fb2-114">The **CIM\_JobDestinationJobs** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="92fb2-115">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="92fb2-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92fb2-116">Type de données : **CIM \_ JobDestination**</span><span class="sxs-lookup"><span data-stu-id="92fb2-116">Data type: **CIM\_JobDestination**</span></span>
</dt> <dt>

<span data-ttu-id="92fb2-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92fb2-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92fb2-118">Qualificateurs : [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Antecedent »)</span><span class="sxs-lookup"><span data-stu-id="92fb2-118">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="92fb2-119">[**\_ JobDestination CIM**](cim-jobdestination.md) décrivant la destination du travail, éventuellement une file d’attente.</span><span class="sxs-lookup"><span data-stu-id="92fb2-119">A [**CIM\_JobDestination**](cim-jobdestination.md) describing the job destination, possibly a queue.</span></span>

</dd> <dt>

<span data-ttu-id="92fb2-120">**Charge**</span><span class="sxs-lookup"><span data-stu-id="92fb2-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92fb2-121">Type de données **: \_ travail CIM**</span><span class="sxs-lookup"><span data-stu-id="92fb2-121">Data type: **CIM\_Job**</span></span>
</dt> <dt>

<span data-ttu-id="92fb2-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92fb2-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92fb2-123">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="92fb2-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="92fb2-124">[**\_ Tâche CIM**](cim-job.md) décrivant le travail qui se trouve dans la file d’attente/destination du travail.</span><span class="sxs-lookup"><span data-stu-id="92fb2-124">A [**CIM\_Job**](cim-job.md) describing the job that is in the job queue/Destination.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="92fb2-125">Notes</span><span class="sxs-lookup"><span data-stu-id="92fb2-125">Remarks</span></span>

<span data-ttu-id="92fb2-126">**CIM \_ JobDestinationJobs** est dérivé de [**la \_ dépendance CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="92fb2-126">**CIM\_JobDestinationJobs** is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="92fb2-127">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="92fb2-127">WMI does not implement this class.</span></span>

<span data-ttu-id="92fb2-128">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="92fb2-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="92fb2-129">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="92fb2-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="92fb2-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="92fb2-130">Requirements</span></span>



| <span data-ttu-id="92fb2-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="92fb2-131">Requirement</span></span> | <span data-ttu-id="92fb2-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="92fb2-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="92fb2-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="92fb2-133">Minimum supported client</span></span><br/> | <span data-ttu-id="92fb2-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="92fb2-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="92fb2-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="92fb2-135">Minimum supported server</span></span><br/> | <span data-ttu-id="92fb2-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="92fb2-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="92fb2-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="92fb2-137">Namespace</span></span><br/>                | <span data-ttu-id="92fb2-138">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="92fb2-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="92fb2-139">MOF</span><span class="sxs-lookup"><span data-stu-id="92fb2-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="92fb2-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="92fb2-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="92fb2-141">DLL</span><span class="sxs-lookup"><span data-stu-id="92fb2-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="92fb2-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92fb2-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92fb2-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="92fb2-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92fb2-144">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="92fb2-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

