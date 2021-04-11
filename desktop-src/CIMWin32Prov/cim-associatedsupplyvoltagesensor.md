---
description: Associe une alimentation à un capteur de tension qui surveille sa tension d’entrée.
ms.assetid: 4164320e-8362-4ce2-9949-f14669278bd8
ms.tgt_platform: multiple
title: Classe CIM_AssociatedSupplyVoltageSensor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedSupplyVoltageSensor
- CIM_AssociatedSupplyVoltageSensor.Dependent
- CIM_AssociatedSupplyVoltageSensor.Antecedent
- CIM_AssociatedSupplyVoltageSensor.MonitoringRange
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ce597fb9e170b63335c56e30f8f8c4ddb30af66c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111090"
---
# <a name="cim_associatedsupplyvoltagesensor-class"></a><span data-ttu-id="d9bd6-103">\_Classe CIM AssociatedSupplyVoltageSensor</span><span class="sxs-lookup"><span data-stu-id="d9bd6-103">CIM\_AssociatedSupplyVoltageSensor class</span></span>

<span data-ttu-id="d9bd6-104">La classe **CIM \_ AssociatedSupplyVoltageSensor** associe une alimentation à un capteur de voltage qui surveille sa tension d’entrée.</span><span class="sxs-lookup"><span data-stu-id="d9bd6-104">The **CIM\_AssociatedSupplyVoltageSensor** class associates a power supply with a voltage sensor that monitors its input voltage.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d9bd6-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="d9bd6-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d9bd6-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="d9bd6-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d9bd6-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="d9bd6-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="d9bd6-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="d9bd6-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9bd6-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d9bd6-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{327ABD78-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_AssociatedSupplyVoltageSensor : CIM_AssociatedSensor
{
  CIM_PowerSupply   REF Dependent;
  CIM_VoltageSensor REF Antecedent;
  uint16                MonitoringRange;
};
```

## <a name="members"></a><span data-ttu-id="d9bd6-110">Membres</span><span class="sxs-lookup"><span data-stu-id="d9bd6-110">Members</span></span>

<span data-ttu-id="d9bd6-111">La classe **CIM \_ AssociatedSupplyVoltageSensor** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d9bd6-111">The **CIM\_AssociatedSupplyVoltageSensor** class has these types of members:</span></span>

-   [<span data-ttu-id="d9bd6-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d9bd6-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d9bd6-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d9bd6-113">Properties</span></span>

<span data-ttu-id="d9bd6-114">La classe **CIM \_ AssociatedSupplyVoltageSensor** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="d9bd6-114">The **CIM\_AssociatedSupplyVoltageSensor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d9bd6-115">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="d9bd6-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9bd6-116">Type de données : **CIM \_ capteur**</span><span class="sxs-lookup"><span data-stu-id="d9bd6-116">Data type: **CIM\_VoltageSensor**</span></span>
</dt> <dt>

<span data-ttu-id="d9bd6-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d9bd6-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9bd6-118">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="d9bd6-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="d9bd6-119">[**\_ Capteur CIM**](cim-voltagesensor.md) qui décrit le capteur de voltage.</span><span class="sxs-lookup"><span data-stu-id="d9bd6-119">A [**CIM\_VoltageSensor**](cim-voltagesensor.md) that describes the voltage sensor.</span></span>

</dd> <dt>

<span data-ttu-id="d9bd6-120">**Charge**</span><span class="sxs-lookup"><span data-stu-id="d9bd6-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9bd6-121">Type de données **: \_ alimentation CIM**</span><span class="sxs-lookup"><span data-stu-id="d9bd6-121">Data type: **CIM\_PowerSupply**</span></span>
</dt> <dt>

<span data-ttu-id="d9bd6-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d9bd6-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9bd6-123">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="d9bd6-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="d9bd6-124">Alimentation [**CIM \_**](cim-powersupply.md) qui décrit l’alimentation associée au capteur de voltage.</span><span class="sxs-lookup"><span data-stu-id="d9bd6-124">A [**CIM\_PowerSupply**](cim-powersupply.md) that describes the power supply associated with the voltage sensor.</span></span>

</dd> <dt>

<span data-ttu-id="d9bd6-125">**MonitoringRange**</span><span class="sxs-lookup"><span data-stu-id="d9bd6-125">**MonitoringRange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9bd6-126">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d9bd6-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d9bd6-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d9bd6-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9bd6-128">Indique la plage de tension d’entrée de l’alimentation mesurée par le capteur associé.</span><span class="sxs-lookup"><span data-stu-id="d9bd6-128">Indicates the power supply's input voltage range measured by the associated sensor.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d9bd6-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="d9bd6-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d9bd6-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="d9bd6-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Range_1"></span><span id="range_1"></span><span id="RANGE_1"></span>

<span data-ttu-id="d9bd6-131"><span id="Range_1"></span><span id="range_1"></span><span id="RANGE_1"></span>**Plage 1** (2)</span><span class="sxs-lookup"><span data-stu-id="d9bd6-131"><span id="Range_1"></span><span id="range_1"></span><span id="RANGE_1"></span>**Range 1** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Range_2"></span><span id="range_2"></span><span id="RANGE_2"></span>

<span data-ttu-id="d9bd6-132"><span id="Range_2"></span><span id="range_2"></span><span id="RANGE_2"></span>**Plage 2** (3)</span><span class="sxs-lookup"><span data-stu-id="d9bd6-132"><span id="Range_2"></span><span id="range_2"></span><span id="RANGE_2"></span>**Range 2** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Both_Range_1_and_2"></span><span id="both_range_1_and_2"></span><span id="BOTH_RANGE_1_AND_2"></span>

<span data-ttu-id="d9bd6-133"><span id="Both_Range_1_and_2"></span><span id="both_range_1_and_2"></span><span id="BOTH_RANGE_1_AND_2"></span>**Les deux plages 1 et 2** (4)</span><span class="sxs-lookup"><span data-stu-id="d9bd6-133"><span id="Both_Range_1_and_2"></span><span id="both_range_1_and_2"></span><span id="BOTH_RANGE_1_AND_2"></span>**Both Range 1 and 2** (4)</span></span>


</dt> <dd>

<span data-ttu-id="d9bd6-134">Plage 1 et 2</span><span class="sxs-lookup"><span data-stu-id="d9bd6-134">Range 1 and 2</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d9bd6-135">Notes</span><span class="sxs-lookup"><span data-stu-id="d9bd6-135">Remarks</span></span>

<span data-ttu-id="d9bd6-136">La classe **CIM \_ AssociatedSupplyVoltageSensor** est dérivée de [**CIM \_ AssociatedSensor**](cim-associatedsensor.md).</span><span class="sxs-lookup"><span data-stu-id="d9bd6-136">The **CIM\_AssociatedSupplyVoltageSensor** class is derived from [**CIM\_AssociatedSensor**](cim-associatedsensor.md).</span></span>

<span data-ttu-id="d9bd6-137">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="d9bd6-137">WMI does not implement this class.</span></span>

<span data-ttu-id="d9bd6-138">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="d9bd6-138">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d9bd6-139">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="d9bd6-139">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9bd6-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d9bd6-140">Requirements</span></span>



| <span data-ttu-id="d9bd6-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d9bd6-141">Requirement</span></span> | <span data-ttu-id="d9bd6-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="d9bd6-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d9bd6-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d9bd6-143">Minimum supported client</span></span><br/> | <span data-ttu-id="d9bd6-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d9bd6-144">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d9bd6-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d9bd6-145">Minimum supported server</span></span><br/> | <span data-ttu-id="d9bd6-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d9bd6-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d9bd6-147">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d9bd6-147">Namespace</span></span><br/>                | <span data-ttu-id="d9bd6-148">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="d9bd6-148">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d9bd6-149">MOF</span><span class="sxs-lookup"><span data-stu-id="d9bd6-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d9bd6-150"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d9bd6-150"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d9bd6-151">DLL</span><span class="sxs-lookup"><span data-stu-id="d9bd6-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d9bd6-152"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9bd6-152"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9bd6-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d9bd6-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9bd6-154">**\_ASSOCIATEDSENSOR CIM**</span><span class="sxs-lookup"><span data-stu-id="d9bd6-154">**CIM\_AssociatedSensor**</span></span>](cim-associatedsensor.md)
</dt> </dl>

 

