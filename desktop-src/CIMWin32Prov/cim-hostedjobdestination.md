---
description: La \_ classe CIM HostedJobDestination représente une association entre une destination de travail et le système sur lequel elle réside. Un système peut héberger de nombreuses files d’attente de travaux. Les destinations du travail diffèrent au système d’hébergement.
ms.assetid: 5d853826-1f27-417b-a053-5e0ee9816376
ms.tgt_platform: multiple
title: Classe CIM_HostedJobDestination
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedJobDestination
- CIM_HostedJobDestination.Dependent
- CIM_HostedJobDestination.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c22e911c6b0adcc38de11fd2410e4797c9381a25
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201027"
---
# <a name="cim_hostedjobdestination-class"></a><span data-ttu-id="69338-105">\_Classe CIM HostedJobDestination</span><span class="sxs-lookup"><span data-stu-id="69338-105">CIM\_HostedJobDestination class</span></span>

<span data-ttu-id="69338-106">La classe **CIM \_ HostedJobDestination** représente une association entre une destination de travail et le système sur lequel elle réside.</span><span class="sxs-lookup"><span data-stu-id="69338-106">The **CIM\_HostedJobDestination** class represents an association between a job destination and the system on which it resides.</span></span> <span data-ttu-id="69338-107">Un système peut héberger de nombreuses files d’attente de travaux.</span><span class="sxs-lookup"><span data-stu-id="69338-107">A system may host many job queues.</span></span> <span data-ttu-id="69338-108">Les destinations du travail diffèrent au système d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="69338-108">Job destinations defer to the hosting system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="69338-109">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="69338-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="69338-110">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="69338-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="69338-111">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="69338-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="69338-112">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="69338-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="69338-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="69338-113">Syntax</span></span>

``` syntax
[Abstract, UUID("{7880DD16-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_HostedJobDestination : CIM_Dependency
{
  CIM_JobDestination REF Dependent;
  CIM_System         REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="69338-114">Membres</span><span class="sxs-lookup"><span data-stu-id="69338-114">Members</span></span>

<span data-ttu-id="69338-115">La classe **CIM \_ HostedJobDestination** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="69338-115">The **CIM\_HostedJobDestination** class has these types of members:</span></span>

-   [<span data-ttu-id="69338-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="69338-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="69338-117">Propriétés</span><span class="sxs-lookup"><span data-stu-id="69338-117">Properties</span></span>

<span data-ttu-id="69338-118">La classe **CIM \_ HostedJobDestination** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="69338-118">The **CIM\_HostedJobDestination** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="69338-119">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="69338-119">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69338-120">Type de données **: \_ système CIM**</span><span class="sxs-lookup"><span data-stu-id="69338-120">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="69338-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="69338-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="69338-122">Qualificateurs : [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Antecedent »)</span><span class="sxs-lookup"><span data-stu-id="69338-122">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="69338-123">[**\_ Système CIM**](cim-system.md) qui décrit le système d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="69338-123">A [**CIM\_System**](cim-system.md) that describes the hosting system.</span></span>

</dd> <dt>

<span data-ttu-id="69338-124">**Charge**</span><span class="sxs-lookup"><span data-stu-id="69338-124">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69338-125">Type de données : **CIM \_ JobDestination**</span><span class="sxs-lookup"><span data-stu-id="69338-125">Data type: **CIM\_JobDestination**</span></span>
</dt> <dt>

<span data-ttu-id="69338-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="69338-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="69338-127">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="69338-127">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="69338-128">[**\_ JobDestination CIM**](cim-jobdestination.md) décrivant la destination du travail hébergée sur le système.</span><span class="sxs-lookup"><span data-stu-id="69338-128">A [**CIM\_JobDestination**](cim-jobdestination.md) describing the job destination hosted on the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="69338-129">Notes</span><span class="sxs-lookup"><span data-stu-id="69338-129">Remarks</span></span>

<span data-ttu-id="69338-130">**CIM \_ HostedJobDestination** est dérivé de [**la \_ dépendance CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="69338-130">**CIM\_HostedJobDestination** is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="69338-131">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="69338-131">WMI does not implement this class.</span></span>

<span data-ttu-id="69338-132">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="69338-132">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="69338-133">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="69338-133">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="69338-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="69338-134">Requirements</span></span>



| <span data-ttu-id="69338-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="69338-135">Requirement</span></span> | <span data-ttu-id="69338-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="69338-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="69338-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="69338-137">Minimum supported client</span></span><br/> | <span data-ttu-id="69338-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="69338-138">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="69338-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="69338-139">Minimum supported server</span></span><br/> | <span data-ttu-id="69338-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="69338-140">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="69338-141">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="69338-141">Namespace</span></span><br/>                | <span data-ttu-id="69338-142">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="69338-142">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="69338-143">MOF</span><span class="sxs-lookup"><span data-stu-id="69338-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="69338-144"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="69338-144"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="69338-145">DLL</span><span class="sxs-lookup"><span data-stu-id="69338-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="69338-146"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="69338-146"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69338-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="69338-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69338-148">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="69338-148">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

