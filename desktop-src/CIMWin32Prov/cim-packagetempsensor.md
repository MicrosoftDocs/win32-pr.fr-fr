---
description: L' \_ Association CIM PackageTempSensor représente la relation dans laquelle un capteur de température est souvent installé dans un package, tel qu’un châssis ou un rack, pour surveiller l’environnement du package.
ms.assetid: 79f2c4d1-5e1a-4c5f-9ef4-0c8bc3926a13
ms.tgt_platform: multiple
title: Classe CIM_PackageTempSensor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PackageTempSensor
- CIM_PackageTempSensor.Dependent
- CIM_PackageTempSensor.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 28c3fa3ba569a2bf3101d62734bb9e4d5372fcf0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110818"
---
# <a name="cim_packagetempsensor-class"></a><span data-ttu-id="e5e0f-103">\_Classe CIM PackageTempSensor</span><span class="sxs-lookup"><span data-stu-id="e5e0f-103">CIM\_PackageTempSensor class</span></span>

<span data-ttu-id="e5e0f-104">L’Association **CIM \_ PackageTempSensor** représente la relation dans laquelle un capteur de température est souvent installé dans un package, tel qu’un châssis ou un rack, pour surveiller l’environnement du package.</span><span class="sxs-lookup"><span data-stu-id="e5e0f-104">The **CIM\_PackageTempSensor** association represents the relationship in which a temperature sensor is often installed in a package, such as a chassis or a rack, to monitor the package's environment.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e5e0f-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="e5e0f-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e5e0f-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e5e0f-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e5e0f-107">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="e5e0f-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="e5e0f-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="e5e0f-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5e0f-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e5e0f-109">Syntax</span></span>

``` syntax
[Abstract, Aggregation, UUID("{FAF76B8F-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PackageTempSensor : CIM_Dependency
{
  CIM_PhysicalPackage   REF Dependent;
  CIM_TemperatureSensor REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="e5e0f-110">Membres</span><span class="sxs-lookup"><span data-stu-id="e5e0f-110">Members</span></span>

<span data-ttu-id="e5e0f-111">La classe **CIM \_ PackageTempSensor** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e5e0f-111">The **CIM\_PackageTempSensor** class has these types of members:</span></span>

-   [<span data-ttu-id="e5e0f-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e5e0f-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e5e0f-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e5e0f-113">Properties</span></span>

<span data-ttu-id="e5e0f-114">La classe **CIM \_ PackageTempSensor** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="e5e0f-114">The **CIM\_PackageTempSensor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e5e0f-115">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="e5e0f-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5e0f-116">Type de données : **CIM \_ capteur**</span><span class="sxs-lookup"><span data-stu-id="e5e0f-116">Data type: **CIM\_TemperatureSensor**</span></span>
</dt> <dt>

<span data-ttu-id="e5e0f-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e5e0f-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5e0f-118">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="e5e0f-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="e5e0f-119">[**\_ Capteur CIM**](cim-temperaturesensor.md) décrivant le capteur de température du package.</span><span class="sxs-lookup"><span data-stu-id="e5e0f-119">A [**CIM\_TemperatureSensor**](cim-temperaturesensor.md) describing the temperature sensor for the package.</span></span>

</dd> <dt>

<span data-ttu-id="e5e0f-120">**Charge**</span><span class="sxs-lookup"><span data-stu-id="e5e0f-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5e0f-121">Type de données : **CIM \_ PhysicalPackage**</span><span class="sxs-lookup"><span data-stu-id="e5e0f-121">Data type: **CIM\_PhysicalPackage**</span></span>
</dt> <dt>

<span data-ttu-id="e5e0f-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e5e0f-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5e0f-123">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="e5e0f-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="e5e0f-124">[**\_ PhysicalPackage CIM**](cim-physicalpackage.md) décrivant le package physique dont l’environnement est analysé.</span><span class="sxs-lookup"><span data-stu-id="e5e0f-124">A [**CIM\_PhysicalPackage**](cim-physicalpackage.md) describing the physical package whose environment is monitored.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e5e0f-125">Notes</span><span class="sxs-lookup"><span data-stu-id="e5e0f-125">Remarks</span></span>

<span data-ttu-id="e5e0f-126">**CIM \_ PackageTempSensor** est dérivé de [**la \_ dépendance CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="e5e0f-126">**CIM\_PackageTempSensor** is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="e5e0f-127">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="e5e0f-127">WMI does not implement this class.</span></span>

<span data-ttu-id="e5e0f-128">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="e5e0f-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e5e0f-129">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="e5e0f-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5e0f-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e5e0f-130">Requirements</span></span>



| <span data-ttu-id="e5e0f-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e5e0f-131">Requirement</span></span> | <span data-ttu-id="e5e0f-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="e5e0f-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e5e0f-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e5e0f-133">Minimum supported client</span></span><br/> | <span data-ttu-id="e5e0f-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e5e0f-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e5e0f-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e5e0f-135">Minimum supported server</span></span><br/> | <span data-ttu-id="e5e0f-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e5e0f-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e5e0f-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e5e0f-137">Namespace</span></span><br/>                | <span data-ttu-id="e5e0f-138">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="e5e0f-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e5e0f-139">MOF</span><span class="sxs-lookup"><span data-stu-id="e5e0f-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e5e0f-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e5e0f-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e5e0f-141">DLL</span><span class="sxs-lookup"><span data-stu-id="e5e0f-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5e0f-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5e0f-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5e0f-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e5e0f-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5e0f-144">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="e5e0f-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

