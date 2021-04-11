---
description: La \_ classe CIM AssociatedSupplyCurrentSensor associe une alimentation à un capteur courant (intensité) qui surveille sa fréquence d’entrée.
ms.assetid: bed4714f-ecf4-4c53-b231-c8fac673371f
ms.tgt_platform: multiple
title: Classe CIM_AssociatedSupplyCurrentSensor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedSupplyCurrentSensor
- CIM_AssociatedSupplyCurrentSensor.Dependent
- CIM_AssociatedSupplyCurrentSensor.Antecedent
- CIM_AssociatedSupplyCurrentSensor.MonitoringRange
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 70a88d87c68b36db5bd44413e3c68940db44f29b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201069"
---
# <a name="cim_associatedsupplycurrentsensor-class"></a><span data-ttu-id="04388-103">\_Classe CIM AssociatedSupplyCurrentSensor</span><span class="sxs-lookup"><span data-stu-id="04388-103">CIM\_AssociatedSupplyCurrentSensor class</span></span>

<span data-ttu-id="04388-104">La classe **CIM \_ AssociatedSupplyCurrentSensor** associe une alimentation à un capteur courant (intensité) qui surveille sa fréquence d’entrée.</span><span class="sxs-lookup"><span data-stu-id="04388-104">The **CIM\_AssociatedSupplyCurrentSensor** class associates a power supply with a current (amperage) sensor that monitors its input frequency.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="04388-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="04388-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="04388-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="04388-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="04388-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="04388-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="04388-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="04388-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="04388-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="04388-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{29B273F2-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_AssociatedSupplyCurrentSensor : CIM_AssociatedSensor
{
  CIM_PowerSupply   REF Dependent;
  CIM_CurrentSensor REF Antecedent;
  uint16                MonitoringRange;
};
```

## <a name="members"></a><span data-ttu-id="04388-110">Membres</span><span class="sxs-lookup"><span data-stu-id="04388-110">Members</span></span>

<span data-ttu-id="04388-111">La classe **CIM \_ AssociatedSupplyCurrentSensor** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="04388-111">The **CIM\_AssociatedSupplyCurrentSensor** class has these types of members:</span></span>

-   [<span data-ttu-id="04388-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="04388-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="04388-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="04388-113">Properties</span></span>

<span data-ttu-id="04388-114">La classe **CIM \_ AssociatedSupplyCurrentSensor** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="04388-114">The **CIM\_AssociatedSupplyCurrentSensor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="04388-115">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="04388-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04388-116">Type de données : **CIM \_ CurrentSensor**</span><span class="sxs-lookup"><span data-stu-id="04388-116">Data type: **CIM\_CurrentSensor**</span></span>
</dt> <dt>

<span data-ttu-id="04388-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="04388-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04388-118">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="04388-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="04388-119">[**\_ CurrentSensor CIM**](cim-currentsensor.md) qui décrit le capteur actuel.</span><span class="sxs-lookup"><span data-stu-id="04388-119">A [**CIM\_CurrentSensor**](cim-currentsensor.md) that describes the current sensor.</span></span>

</dd> <dt>

<span data-ttu-id="04388-120">**Charge**</span><span class="sxs-lookup"><span data-stu-id="04388-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04388-121">Type de données **: \_ alimentation CIM**</span><span class="sxs-lookup"><span data-stu-id="04388-121">Data type: **CIM\_PowerSupply**</span></span>
</dt> <dt>

<span data-ttu-id="04388-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="04388-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04388-123">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="04388-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="04388-124">Alimentation [**CIM \_**](cim-powersupply.md) qui décrit l’alimentation associée au capteur actuel.</span><span class="sxs-lookup"><span data-stu-id="04388-124">A [**CIM\_PowerSupply**](cim-powersupply.md) that describes the power supply associated with the current sensor.</span></span>

</dd> <dt>

<span data-ttu-id="04388-125">**MonitoringRange**</span><span class="sxs-lookup"><span data-stu-id="04388-125">**MonitoringRange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04388-126">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="04388-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="04388-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="04388-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04388-128">Indique la plage de fréquences d’entrée de l’alimentation mesurée par le capteur associé.</span><span class="sxs-lookup"><span data-stu-id="04388-128">Indicates the power supply input frequency range measured by the associated sensor.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="04388-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="04388-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="04388-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="04388-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Range_1"></span><span id="range_1"></span><span id="RANGE_1"></span>

<span data-ttu-id="04388-131"><span id="Range_1"></span><span id="range_1"></span><span id="RANGE_1"></span>**Plage 1** (2)</span><span class="sxs-lookup"><span data-stu-id="04388-131"><span id="Range_1"></span><span id="range_1"></span><span id="RANGE_1"></span>**Range 1** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Range_2"></span><span id="range_2"></span><span id="RANGE_2"></span>

<span data-ttu-id="04388-132"><span id="Range_2"></span><span id="range_2"></span><span id="RANGE_2"></span>**Plage 2** (3)</span><span class="sxs-lookup"><span data-stu-id="04388-132"><span id="Range_2"></span><span id="range_2"></span><span id="RANGE_2"></span>**Range 2** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Both_Range_1_and_2"></span><span id="both_range_1_and_2"></span><span id="BOTH_RANGE_1_AND_2"></span>

<span data-ttu-id="04388-133"><span id="Both_Range_1_and_2"></span><span id="both_range_1_and_2"></span><span id="BOTH_RANGE_1_AND_2"></span>**Les deux plages 1 et 2** (4)</span><span class="sxs-lookup"><span data-stu-id="04388-133"><span id="Both_Range_1_and_2"></span><span id="both_range_1_and_2"></span><span id="BOTH_RANGE_1_AND_2"></span>**Both Range 1 and 2** (4)</span></span>


</dt> <dd>

<span data-ttu-id="04388-134">Plage 1 et 2</span><span class="sxs-lookup"><span data-stu-id="04388-134">Range 1 and 2</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="04388-135">Notes</span><span class="sxs-lookup"><span data-stu-id="04388-135">Remarks</span></span>

<span data-ttu-id="04388-136">La classe **CIM \_ AssociatedSupplyCurrentSensor** est dérivée de [**CIM \_ AssociatedSensor**](cim-associatedsensor.md).</span><span class="sxs-lookup"><span data-stu-id="04388-136">The **CIM\_AssociatedSupplyCurrentSensor** class is derived from [**CIM\_AssociatedSensor**](cim-associatedsensor.md).</span></span>

<span data-ttu-id="04388-137">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="04388-137">WMI does not implement this class.</span></span>

<span data-ttu-id="04388-138">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="04388-138">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="04388-139">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="04388-139">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="04388-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="04388-140">Requirements</span></span>



| <span data-ttu-id="04388-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="04388-141">Requirement</span></span> | <span data-ttu-id="04388-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="04388-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="04388-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="04388-143">Minimum supported client</span></span><br/> | <span data-ttu-id="04388-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="04388-144">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="04388-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="04388-145">Minimum supported server</span></span><br/> | <span data-ttu-id="04388-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="04388-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="04388-147">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="04388-147">Namespace</span></span><br/>                | <span data-ttu-id="04388-148">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="04388-148">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="04388-149">MOF</span><span class="sxs-lookup"><span data-stu-id="04388-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="04388-150"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="04388-150"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="04388-151">DLL</span><span class="sxs-lookup"><span data-stu-id="04388-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04388-152"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04388-152"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04388-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="04388-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04388-154">**\_ASSOCIATEDSENSOR CIM**</span><span class="sxs-lookup"><span data-stu-id="04388-154">**CIM\_AssociatedSensor**</span></span>](cim-associatedsensor.md)
</dt> </dl>

 

