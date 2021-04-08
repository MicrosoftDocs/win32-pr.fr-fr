---
description: La \_ classe CIM executos représente le système d’exploitation en cours d’exécution. Au maximum, un système d’exploitation peut s’exécuter à tout moment sur un système informatique. le système informatique n’est peut-être pas en cours de démarrage ou son système d’exploitation est peut-être inconnu.
ms.assetid: 93e3d425-d751-4252-aa81-7d6774c8f8c5
ms.tgt_platform: multiple
title: Classe CIM_RunningOS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RunningOS
- CIM_RunningOS.Dependent
- CIM_RunningOS.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1ff86af88342a1b8f0147ecd9721765794faf39e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748949"
---
# <a name="cim_runningos-class"></a><span data-ttu-id="de6de-104">\_Classe en cours d’exécution CIM</span><span class="sxs-lookup"><span data-stu-id="de6de-104">CIM\_RunningOS class</span></span>

<span data-ttu-id="de6de-105">La classe CIM executos représente le système d’exploitation **\_ en** cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="de6de-105">The **CIM\_RunningOS** class represents the currently executing operating system.</span></span> <span data-ttu-id="de6de-106">Au maximum, un système d’exploitation peut s’exécuter à tout moment sur un système informatique. le système informatique n’est peut-être pas en cours de démarrage ou son système d’exploitation est peut-être inconnu.</span><span class="sxs-lookup"><span data-stu-id="de6de-106">At most, one operating system can execute at any time on a computer system; the computer system may not be currently booted, or its operating system may be unknown.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="de6de-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="de6de-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="de6de-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="de6de-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="de6de-109">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="de6de-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="de6de-110">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="de6de-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="de6de-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="de6de-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{1F2EA300-DB37-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_RunningOS : CIM_Dependency
{
  CIM_ComputerSystem  REF Dependent;
  CIM_OperatingSystem REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="de6de-112">Membres</span><span class="sxs-lookup"><span data-stu-id="de6de-112">Members</span></span>

<span data-ttu-id="de6de-113">La classe **CIM \_ Running** contient les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="de6de-113">The **CIM\_RunningOS** class has these types of members:</span></span>

-   [<span data-ttu-id="de6de-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="de6de-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="de6de-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="de6de-115">Properties</span></span>

<span data-ttu-id="de6de-116">La classe **CIM- \_ Running** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="de6de-116">The **CIM\_RunningOS** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="de6de-117">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="de6de-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de6de-118">Type de données : **CIM \_ OperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="de6de-118">Data type: **CIM\_OperatingSystem**</span></span>
</dt> <dt>

<span data-ttu-id="de6de-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="de6de-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de6de-120">Qualificateurs : [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Antecedent »)</span><span class="sxs-lookup"><span data-stu-id="de6de-120">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="de6de-121">Un système d’exploitation [**CIM \_**](cim-operatingsystem.md) qui décrit le système d’exploitation en cours d’exécution sur le système informatique.</span><span class="sxs-lookup"><span data-stu-id="de6de-121">A [**CIM\_OperatingSystem**](cim-operatingsystem.md) that describes the operating system currently running on the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="de6de-122">**Charge**</span><span class="sxs-lookup"><span data-stu-id="de6de-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de6de-123">Type de données **: \_ CIM CIM**</span><span class="sxs-lookup"><span data-stu-id="de6de-123">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="de6de-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="de6de-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de6de-125">Qualificateurs : [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="de6de-125">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="de6de-126">Un [**\_ ComputerSystem CIM**](cim-computersystem.md) qui décrit le système informatique.</span><span class="sxs-lookup"><span data-stu-id="de6de-126">A [**CIM\_ComputerSystem**](cim-computersystem.md) that describes the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="de6de-127">Notes</span><span class="sxs-lookup"><span data-stu-id="de6de-127">Remarks</span></span>

<span data-ttu-id="de6de-128">La classe **CIM \_ en cours d’exécution** est dérivée de la [**\_ dépendance CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="de6de-128">The **CIM\_RunningOS** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="de6de-129">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="de6de-129">WMI does not implement this class.</span></span>

<span data-ttu-id="de6de-130">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="de6de-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="de6de-131">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="de6de-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="de6de-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="de6de-132">Requirements</span></span>



| <span data-ttu-id="de6de-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="de6de-133">Requirement</span></span> | <span data-ttu-id="de6de-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="de6de-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="de6de-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="de6de-135">Minimum supported client</span></span><br/> | <span data-ttu-id="de6de-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="de6de-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="de6de-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="de6de-137">Minimum supported server</span></span><br/> | <span data-ttu-id="de6de-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="de6de-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="de6de-139">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="de6de-139">Namespace</span></span><br/>                | <span data-ttu-id="de6de-140">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="de6de-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="de6de-141">MOF</span><span class="sxs-lookup"><span data-stu-id="de6de-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="de6de-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="de6de-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="de6de-143">DLL</span><span class="sxs-lookup"><span data-stu-id="de6de-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de6de-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de6de-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de6de-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="de6de-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de6de-146">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="de6de-146">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

