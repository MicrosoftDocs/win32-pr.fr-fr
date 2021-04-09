---
description: L' \_ Association CIM AssociatedCooling indique quand des ventilateurs ou d’autres appareils de refroidissement sont spécifiques à un appareil (par rapport à la fourniture d’un boîtier ou d’un refroidissement d’armoire).
ms.assetid: 7b20e429-593c-4365-a340-1aef9b0fadf5
ms.tgt_platform: multiple
title: Classe CIM_AssociatedCooling
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedCooling
- CIM_AssociatedCooling.Dependent
- CIM_AssociatedCooling.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bb838129226b225f024917e8f8e77ddc92ddf2ff
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111098"
---
# <a name="cim_associatedcooling-class"></a><span data-ttu-id="edeba-103">\_Classe CIM AssociatedCooling</span><span class="sxs-lookup"><span data-stu-id="edeba-103">CIM\_AssociatedCooling class</span></span>

<span data-ttu-id="edeba-104">L’Association **CIM \_ AssociatedCooling** indique quand des ventilateurs ou d’autres appareils de refroidissement sont spécifiques à un appareil (par rapport à la fourniture d’un boîtier ou d’un refroidissement d’armoire).</span><span class="sxs-lookup"><span data-stu-id="edeba-104">The **CIM\_AssociatedCooling** association indicates when fans or other cooling devices are specific to a device (versus providing enclosure or cabinet cooling).</span></span>

<span data-ttu-id="edeba-105">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="edeba-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="edeba-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="edeba-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="edeba-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="edeba-107">Syntax</span></span>

``` syntax
[Abstract, UUID("{306F88F2-DB35-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_AssociatedCooling : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  CIM_CoolingDevice REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="edeba-108">Membres</span><span class="sxs-lookup"><span data-stu-id="edeba-108">Members</span></span>

<span data-ttu-id="edeba-109">La classe **CIM \_ AssociatedCooling** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="edeba-109">The **CIM\_AssociatedCooling** class has these types of members:</span></span>

-   [<span data-ttu-id="edeba-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="edeba-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="edeba-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="edeba-111">Properties</span></span>

<span data-ttu-id="edeba-112">La classe **CIM \_ AssociatedCooling** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="edeba-112">The **CIM\_AssociatedCooling** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="edeba-113">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="edeba-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="edeba-114">Type de données : **CIM \_ CoolingDevice**</span><span class="sxs-lookup"><span data-stu-id="edeba-114">Data type: **CIM\_CoolingDevice**</span></span>
</dt> <dt>

<span data-ttu-id="edeba-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="edeba-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="edeba-116">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="edeba-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="edeba-117">[**\_ LogicalDevice CIM**](cim-logicaldevice.md) qui décrit l’appareil de refroidissement.</span><span class="sxs-lookup"><span data-stu-id="edeba-117">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the cooling device.</span></span>

</dd> <dt>

<span data-ttu-id="edeba-118">**Charge**</span><span class="sxs-lookup"><span data-stu-id="edeba-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="edeba-119">Type de données **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="edeba-119">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="edeba-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="edeba-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="edeba-121">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="edeba-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="edeba-122">[**\_ LogicalDevice CIM**](cim-logicaldevice.md) qui fait référence à l’appareil logique refroidi.</span><span class="sxs-lookup"><span data-stu-id="edeba-122">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that references the logical device being cooled.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="edeba-123">Notes</span><span class="sxs-lookup"><span data-stu-id="edeba-123">Remarks</span></span>

<span data-ttu-id="edeba-124">La classe **CIM \_ AssociatedCooling** est dérivée de la [**\_ dépendance CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="edeba-124">The **CIM\_AssociatedCooling** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="edeba-125">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="edeba-125">WMI does not implement this class.</span></span>

<span data-ttu-id="edeba-126">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="edeba-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="edeba-127">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="edeba-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="edeba-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="edeba-128">Requirements</span></span>



| <span data-ttu-id="edeba-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="edeba-129">Requirement</span></span> | <span data-ttu-id="edeba-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="edeba-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="edeba-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="edeba-131">Minimum supported client</span></span><br/> | <span data-ttu-id="edeba-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="edeba-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="edeba-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="edeba-133">Minimum supported server</span></span><br/> | <span data-ttu-id="edeba-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="edeba-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="edeba-135">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="edeba-135">Namespace</span></span><br/>                | <span data-ttu-id="edeba-136">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="edeba-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="edeba-137">MOF</span><span class="sxs-lookup"><span data-stu-id="edeba-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="edeba-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="edeba-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="edeba-139">DLL</span><span class="sxs-lookup"><span data-stu-id="edeba-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="edeba-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="edeba-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="edeba-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="edeba-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edeba-142">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="edeba-142">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

