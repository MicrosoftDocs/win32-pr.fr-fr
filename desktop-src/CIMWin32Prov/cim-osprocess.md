---
description: La \_ classe CIM OSProcess associe le système d’exploitation et un ou plusieurs processus en cours d’exécution dans le contexte du système d’exploitation.
ms.assetid: 59d52b29-9d97-464f-bbbc-4191305df8c7
ms.tgt_platform: multiple
title: Classe CIM_OSProcess
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_OSProcess
- CIM_OSProcess.PartComponent
- CIM_OSProcess.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9b11738669c87b402f12932ad65237a512360427
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860750"
---
# <a name="cim_osprocess-class"></a><span data-ttu-id="e70cf-103">\_Classe CIM OSProcess</span><span class="sxs-lookup"><span data-stu-id="e70cf-103">CIM\_OSProcess class</span></span>

<span data-ttu-id="e70cf-104">La classe **CIM \_ OSProcess** associe le système d’exploitation et un ou plusieurs processus en cours d’exécution dans le contexte du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="e70cf-104">The **CIM\_OSProcess** class associates the operating system and one or more processes running in the context of the operating system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e70cf-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="e70cf-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e70cf-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e70cf-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e70cf-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="e70cf-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="e70cf-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="e70cf-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e70cf-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e70cf-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{A361A7AE-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_OSProcess : CIM_Component
{
  CIM_Process         REF PartComponent;
  CIM_OperatingSystem REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="e70cf-110">Membres</span><span class="sxs-lookup"><span data-stu-id="e70cf-110">Members</span></span>

<span data-ttu-id="e70cf-111">La classe **CIM \_ OSProcess** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e70cf-111">The **CIM\_OSProcess** class has these types of members:</span></span>

-   [<span data-ttu-id="e70cf-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e70cf-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e70cf-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e70cf-113">Properties</span></span>

<span data-ttu-id="e70cf-114">La classe **CIM \_ OSProcess** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="e70cf-114">The **CIM\_OSProcess** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e70cf-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="e70cf-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e70cf-116">Type de données : **CIM \_ OperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="e70cf-116">Data type: **CIM\_OperatingSystem**</span></span>
</dt> <dt>

<span data-ttu-id="e70cf-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e70cf-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e70cf-118">Qualificateurs : [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="e70cf-118">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="e70cf-119">Un système d’exploitation [**CIM \_**](cim-operatingsystem.md) décrivant le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="e70cf-119">A [**CIM\_OperatingSystem**](cim-operatingsystem.md) describing the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="e70cf-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="e70cf-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e70cf-121">Type de données **: \_ processus CIM**</span><span class="sxs-lookup"><span data-stu-id="e70cf-121">Data type: **CIM\_Process**</span></span>
</dt> <dt>

<span data-ttu-id="e70cf-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e70cf-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e70cf-123">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e70cf-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e70cf-124">[**\_ Processus CIM**](cim-process.md) décrivant le processus en cours d’exécution dans le contexte du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="e70cf-124">A [**CIM\_Process**](cim-process.md) describing the process running in the context of the operating system</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e70cf-125">Notes</span><span class="sxs-lookup"><span data-stu-id="e70cf-125">Remarks</span></span>

<span data-ttu-id="e70cf-126">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="e70cf-126">WMI does not implement this class.</span></span>

<span data-ttu-id="e70cf-127">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="e70cf-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e70cf-128">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="e70cf-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e70cf-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e70cf-129">Requirements</span></span>



| <span data-ttu-id="e70cf-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e70cf-130">Requirement</span></span> | <span data-ttu-id="e70cf-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="e70cf-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e70cf-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e70cf-132">Minimum supported client</span></span><br/> | <span data-ttu-id="e70cf-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e70cf-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e70cf-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e70cf-134">Minimum supported server</span></span><br/> | <span data-ttu-id="e70cf-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e70cf-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e70cf-136">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e70cf-136">Namespace</span></span><br/>                | <span data-ttu-id="e70cf-137">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="e70cf-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e70cf-138">MOF</span><span class="sxs-lookup"><span data-stu-id="e70cf-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e70cf-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e70cf-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e70cf-140">DLL</span><span class="sxs-lookup"><span data-stu-id="e70cf-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e70cf-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e70cf-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e70cf-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e70cf-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e70cf-143">**\_Composant CIM**</span><span class="sxs-lookup"><span data-stu-id="e70cf-143">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

