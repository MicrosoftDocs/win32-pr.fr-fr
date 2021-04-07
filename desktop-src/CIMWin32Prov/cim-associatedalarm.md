---
description: La \_ dépendance ASSOCIATEDALARM CIM associe une alarme à un appareil logique.
ms.assetid: ed0ccc81-6d1b-45b0-abf0-7a2bd9a50193
ms.tgt_platform: multiple
title: Classe CIM_AssociatedAlarm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedAlarm
- CIM_AssociatedAlarm.Dependent
- CIM_AssociatedAlarm.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fe6a637482526feecc7528eadc70dc695dafca9b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748708"
---
# <a name="cim_associatedalarm-class"></a><span data-ttu-id="a7a94-103">\_Classe CIM AssociatedAlarm</span><span class="sxs-lookup"><span data-stu-id="a7a94-103">CIM\_AssociatedAlarm class</span></span>

<span data-ttu-id="a7a94-104">La **dépendance \_ AssociatedAlarm CIM** associe une alarme à un appareil logique.</span><span class="sxs-lookup"><span data-stu-id="a7a94-104">The **CIM\_AssociatedAlarm** dependency associates an alarm with a logical device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a7a94-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="a7a94-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a7a94-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a7a94-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a7a94-107">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="a7a94-107">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7a94-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a7a94-108">Syntax</span></span>

``` syntax
[Abstract, UUID("{2280CB02-DB35-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_AssociatedAlarm : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  CIM_AlarmDevice   REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="a7a94-109">Membres</span><span class="sxs-lookup"><span data-stu-id="a7a94-109">Members</span></span>

<span data-ttu-id="a7a94-110">La classe **CIM \_ AssociatedAlarm** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a7a94-110">The **CIM\_AssociatedAlarm** class has these types of members:</span></span>

-   [<span data-ttu-id="a7a94-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a7a94-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a7a94-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a7a94-112">Properties</span></span>

<span data-ttu-id="a7a94-113">La classe **CIM \_ AssociatedAlarm** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="a7a94-113">The **CIM\_AssociatedAlarm** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a7a94-114">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="a7a94-114">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7a94-115">Type de données : **CIM \_ AlarmDevice**</span><span class="sxs-lookup"><span data-stu-id="a7a94-115">Data type: **CIM\_AlarmDevice**</span></span>
</dt> <dt>

<span data-ttu-id="a7a94-116">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a7a94-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7a94-117">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="a7a94-117">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="a7a94-118">[**\_ AlarmDevice CIM**](cim-alarmdevice.md) qui contient l’appareil d’alarme.</span><span class="sxs-lookup"><span data-stu-id="a7a94-118">A [**CIM\_AlarmDevice**](cim-alarmdevice.md) that contains the alarm device.</span></span>

</dd> <dt>

<span data-ttu-id="a7a94-119">**Charge**</span><span class="sxs-lookup"><span data-stu-id="a7a94-119">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7a94-120">Type de données **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="a7a94-120">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="a7a94-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a7a94-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7a94-122">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="a7a94-122">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="a7a94-123">[**\_ LogicalDevice CIM**](cim-logicaldevice.md) qui contient l’appareil logique qui est doté d’une alarme.</span><span class="sxs-lookup"><span data-stu-id="a7a94-123">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that contains the logical device that is alarmed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a7a94-124">Notes</span><span class="sxs-lookup"><span data-stu-id="a7a94-124">Remarks</span></span>

<span data-ttu-id="a7a94-125">La classe **CIM \_ AssociatedAlarm** est dérivée de la [**\_ dépendance CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="a7a94-125">The **CIM\_AssociatedAlarm** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="a7a94-126">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="a7a94-126">WMI does not implement this class.</span></span>

<span data-ttu-id="a7a94-127">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="a7a94-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a7a94-128">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="a7a94-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7a94-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a7a94-129">Requirements</span></span>



| <span data-ttu-id="a7a94-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a7a94-130">Requirement</span></span> | <span data-ttu-id="a7a94-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="a7a94-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a7a94-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a7a94-132">Minimum supported client</span></span><br/> | <span data-ttu-id="a7a94-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a7a94-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a7a94-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a7a94-134">Minimum supported server</span></span><br/> | <span data-ttu-id="a7a94-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a7a94-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a7a94-136">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a7a94-136">Namespace</span></span><br/>                | <span data-ttu-id="a7a94-137">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="a7a94-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a7a94-138">MOF</span><span class="sxs-lookup"><span data-stu-id="a7a94-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a7a94-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a7a94-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a7a94-140">DLL</span><span class="sxs-lookup"><span data-stu-id="a7a94-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7a94-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7a94-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7a94-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a7a94-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7a94-143">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="a7a94-143">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

