---
description: L' \_ Association CIM ActionSequence définit une série d’opérations qui font passer l’élément logiciel (référencé par l' \_ Association CIM SoftwareElementActions) à son état suivant, ou supprime l’élément logiciel de son état actuel.
ms.assetid: b539c424-bc2a-414b-b56c-72550004720f
ms.tgt_platform: multiple
title: Classe CIM_ActionSequence
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ActionSequence
- CIM_ActionSequence.Next
- CIM_ActionSequence.Prior
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 71150d1ad9785d81579d8f305fe46bc6b7e57d00
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106512894"
---
# <a name="cim_actionsequence-class"></a><span data-ttu-id="66aef-103">\_Classe CIM ActionSequence</span><span class="sxs-lookup"><span data-stu-id="66aef-103">CIM\_ActionSequence class</span></span>

<span data-ttu-id="66aef-104">L’Association **CIM \_ ActionSequence** définit une série d’opérations qui font passer l’élément logiciel (référencé par l’Association [**CIM \_ SoftwareElementActions**](cim-softwareelementactions.md) ) à son état suivant, ou supprime l’élément logiciel de son état actuel.</span><span class="sxs-lookup"><span data-stu-id="66aef-104">The **CIM\_ActionSequence** association defines a series of operations that transition the software element (referenced by the [**CIM\_SoftwareElementActions**](cim-softwareelementactions.md) association) to its next state, or removes the software element from its current state.</span></span>

<span data-ttu-id="66aef-105">Les actions d’état suivant et les actions de désinstallation associées à un élément logiciel particulier doivent être une séquence continue.</span><span class="sxs-lookup"><span data-stu-id="66aef-105">The next-state actions and uninstall actions associated with a particular software element must be a continuous sequence.</span></span> <span data-ttu-id="66aef-106">Étant donné que **CIM \_ ActionSequence** est une association, les boucles sur la classe d' [**\_ action CIM**](cim-action.md) , avec les rôles pour l’action « précédente » et l’action « suivante », forment une séquence.</span><span class="sxs-lookup"><span data-stu-id="66aef-106">Since **CIM\_ActionSequence** is an association, the loops on the [**CIM\_Action**](cim-action.md) class, with roles for the "prior" action and "next" action, form a sequence.</span></span>

<span data-ttu-id="66aef-107">La nécessité d’une séquence continue implique les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="66aef-107">The need for a continuous sequence implies:</span></span>

-   <span data-ttu-id="66aef-108">Dans l’ensemble des actions d’état suivant ou de désinstallation, il n’y a qu’une seule action qui n’a pas d’instance de l’Association **CIM \_ ActionSequence** qui la référence dans le rôle « suivant ».</span><span class="sxs-lookup"><span data-stu-id="66aef-108">Within the set of next-state or uninstall actions, there is only one action that does not have an instance of the **CIM\_ActionSequence** association referencing it in the "next" role.</span></span> <span data-ttu-id="66aef-109">Il s’agit de la première action de la séquence.</span><span class="sxs-lookup"><span data-stu-id="66aef-109">This is the first action in the sequence.</span></span>
-   <span data-ttu-id="66aef-110">Dans l’ensemble des actions d’état suivant ou de désinstallation, il n’y a qu’une seule action qui n’a pas d’instance de l’Association **CIM \_ ActionSequence** qui la référence dans le rôle « antérieur ».</span><span class="sxs-lookup"><span data-stu-id="66aef-110">Within the set of next-state or uninstall actions, there is only one action that does not have an instance of the **CIM\_ActionSequence** association referencing it in the "prior" role.</span></span> <span data-ttu-id="66aef-111">Il s’agit de la dernière action de la séquence.</span><span class="sxs-lookup"><span data-stu-id="66aef-111">This is the last action in the sequence.</span></span>
-   <span data-ttu-id="66aef-112">Toutes les autres actions au sein de l’ensemble des actions d’état suivant et de désinstallation doivent participer à deux instances de l’Association **CIM \_ ActionSequence** , une dans un rôle « antérieur » et une dans le rôle « suivant ».</span><span class="sxs-lookup"><span data-stu-id="66aef-112">All other actions within the set of next-state and uninstall actions must participate in two instances of the **CIM\_ActionSequence** association, one in a "prior" role and one in the "next" role.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="66aef-113">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="66aef-113">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="66aef-114">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="66aef-114">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="66aef-115">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="66aef-115">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="66aef-116">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="66aef-116">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="66aef-117">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="66aef-117">Syntax</span></span>

``` syntax
[Abstract, Association, UUID("{F127E50E-E3E0-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_ActionSequence
{
  CIM_Action REF Next;
  CIM_Action REF Prior;
};
```

## <a name="members"></a><span data-ttu-id="66aef-118">Membres</span><span class="sxs-lookup"><span data-stu-id="66aef-118">Members</span></span>

<span data-ttu-id="66aef-119">La classe **CIM \_ ActionSequence** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="66aef-119">The **CIM\_ActionSequence** class has these types of members:</span></span>

-   [<span data-ttu-id="66aef-120">Propriétés</span><span class="sxs-lookup"><span data-stu-id="66aef-120">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="66aef-121">Propriétés</span><span class="sxs-lookup"><span data-stu-id="66aef-121">Properties</span></span>

<span data-ttu-id="66aef-122">La classe **CIM \_ ActionSequence** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="66aef-122">The **CIM\_ActionSequence** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="66aef-123">**Next**</span><span class="sxs-lookup"><span data-stu-id="66aef-123">**Next**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66aef-124">Type de données **: \_ action CIM**</span><span class="sxs-lookup"><span data-stu-id="66aef-124">Data type: **CIM\_Action**</span></span>
</dt> <dt>

<span data-ttu-id="66aef-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="66aef-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66aef-126">Qualificateurs : [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="66aef-126">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="66aef-127">Référence à l’action suivante.</span><span class="sxs-lookup"><span data-stu-id="66aef-127">Reference to the next action.</span></span>

</dd> <dt>

<span data-ttu-id="66aef-128">**Antérieure**</span><span class="sxs-lookup"><span data-stu-id="66aef-128">**Prior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66aef-129">Type de données **: \_ action CIM**</span><span class="sxs-lookup"><span data-stu-id="66aef-129">Data type: **CIM\_Action**</span></span>
</dt> <dt>

<span data-ttu-id="66aef-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="66aef-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66aef-131">Qualificateurs : [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="66aef-131">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="66aef-132">Référence à l’action précédente.</span><span class="sxs-lookup"><span data-stu-id="66aef-132">Reference to the prior action.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="66aef-133">Notes</span><span class="sxs-lookup"><span data-stu-id="66aef-133">Remarks</span></span>

<span data-ttu-id="66aef-134">Les classes d' [**\_ action CIM**](cim-action.md) qui participent à cette association doivent avoir la même valeur pour la propriété **direction** .</span><span class="sxs-lookup"><span data-stu-id="66aef-134">The [**CIM\_Action**](cim-action.md) classes participating in this association must have the same value for the **Direction** property.</span></span>

<span data-ttu-id="66aef-135">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="66aef-135">WMI does not implement this class.</span></span>

<span data-ttu-id="66aef-136">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="66aef-136">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="66aef-137">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="66aef-137">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="66aef-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="66aef-138">Requirements</span></span>



| <span data-ttu-id="66aef-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="66aef-139">Requirement</span></span> | <span data-ttu-id="66aef-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="66aef-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="66aef-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="66aef-141">Minimum supported client</span></span><br/> | <span data-ttu-id="66aef-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="66aef-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="66aef-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="66aef-143">Minimum supported server</span></span><br/> | <span data-ttu-id="66aef-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="66aef-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="66aef-145">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="66aef-145">Namespace</span></span><br/>                | <span data-ttu-id="66aef-146">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="66aef-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="66aef-147">MOF</span><span class="sxs-lookup"><span data-stu-id="66aef-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="66aef-148"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="66aef-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="66aef-149">DLL</span><span class="sxs-lookup"><span data-stu-id="66aef-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66aef-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66aef-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66aef-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="66aef-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66aef-152">Classes CIM</span><span class="sxs-lookup"><span data-stu-id="66aef-152">CIM Classes</span></span>](/windows/desktop/WmiSdk/cimclas)
</dt> </dl>

 

