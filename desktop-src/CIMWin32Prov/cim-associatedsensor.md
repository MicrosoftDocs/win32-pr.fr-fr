---
description: La \_ classe CIM AssociatedSensor associe un capteur installé à un périphérique logique. Le capteur mesure les propriétés d’entrée et de sortie critiques et peut être inclus avec l’appareil ou installé à proximité.
ms.assetid: 8ccaa37f-b95f-4582-a694-23bdc15b8c8b
ms.tgt_platform: multiple
title: Classe CIM_AssociatedSensor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedSensor
- CIM_AssociatedSensor.Dependent
- CIM_AssociatedSensor.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 50eac6b8bd933762df0da0213c420f5895b74640
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861421"
---
# <a name="cim_associatedsensor-class"></a><span data-ttu-id="2333b-104">\_Classe CIM AssociatedSensor</span><span class="sxs-lookup"><span data-stu-id="2333b-104">CIM\_AssociatedSensor class</span></span>

<span data-ttu-id="2333b-105">La classe **CIM \_ AssociatedSensor** associe un capteur installé à un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="2333b-105">The **CIM\_AssociatedSensor** class associates an installed sensor with a logical device.</span></span> <span data-ttu-id="2333b-106">Le capteur mesure les propriétés d’entrée et de sortie critiques et peut être inclus avec l’appareil ou installé à proximité.</span><span class="sxs-lookup"><span data-stu-id="2333b-106">The sensor measures critical input and output properties, and can be included with the device or installed nearby.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2333b-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="2333b-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2333b-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="2333b-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2333b-109">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="2333b-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="2333b-110">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="2333b-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2333b-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2333b-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{956597A0-7D80-11D2-AAD3-006008C78BC7}"), AMENDMENT]
class CIM_AssociatedSensor : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  CIM_Sensor        REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="2333b-112">Membres</span><span class="sxs-lookup"><span data-stu-id="2333b-112">Members</span></span>

<span data-ttu-id="2333b-113">La classe **CIM \_ AssociatedSensor** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="2333b-113">The **CIM\_AssociatedSensor** class has these types of members:</span></span>

-   [<span data-ttu-id="2333b-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2333b-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2333b-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2333b-115">Properties</span></span>

<span data-ttu-id="2333b-116">La classe **CIM \_ AssociatedSensor** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="2333b-116">The **CIM\_AssociatedSensor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2333b-117">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="2333b-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2333b-118">Type de données **: \_ capteur CIM**</span><span class="sxs-lookup"><span data-stu-id="2333b-118">Data type: **CIM\_Sensor**</span></span>
</dt> <dt>

<span data-ttu-id="2333b-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2333b-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2333b-120">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="2333b-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="2333b-121">[**\_ Capteur CIM**](cim-sensor.md) qui décrit le capteur.</span><span class="sxs-lookup"><span data-stu-id="2333b-121">A [**CIM\_Sensor**](cim-sensor.md) that describes the sensor.</span></span>

</dd> <dt>

<span data-ttu-id="2333b-122">**Charge**</span><span class="sxs-lookup"><span data-stu-id="2333b-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2333b-123">Type de données **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="2333b-123">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="2333b-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2333b-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2333b-125">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="2333b-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="2333b-126">[**\_ LogicalDevice CIM**](cim-logicaldevice.md) qui décrit l’unité logique pour laquelle les informations sont mesurées par le capteur.</span><span class="sxs-lookup"><span data-stu-id="2333b-126">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the logical device for which information is measured by the sensor.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2333b-127">Notes</span><span class="sxs-lookup"><span data-stu-id="2333b-127">Remarks</span></span>

<span data-ttu-id="2333b-128">La classe **CIM \_ AssociatedSensor** est dérivée de la [**\_ dépendance CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="2333b-128">The **CIM\_AssociatedSensor** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="2333b-129">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="2333b-129">WMI does not implement this class.</span></span> <span data-ttu-id="2333b-130">Pour plus d’informations sur les classes dérivées de **CIM \_ AssociatedSensor**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="2333b-130">For more information about classes derived from **CIM\_AssociatedSensor**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="2333b-131">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="2333b-131">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2333b-132">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="2333b-132">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2333b-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2333b-133">Requirements</span></span>



| <span data-ttu-id="2333b-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2333b-134">Requirement</span></span> | <span data-ttu-id="2333b-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="2333b-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2333b-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2333b-136">Minimum supported client</span></span><br/> | <span data-ttu-id="2333b-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2333b-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2333b-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2333b-138">Minimum supported server</span></span><br/> | <span data-ttu-id="2333b-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2333b-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2333b-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2333b-140">Namespace</span></span><br/>                | <span data-ttu-id="2333b-141">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="2333b-141">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2333b-142">MOF</span><span class="sxs-lookup"><span data-stu-id="2333b-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2333b-143"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2333b-143"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2333b-144">DLL</span><span class="sxs-lookup"><span data-stu-id="2333b-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2333b-145"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2333b-145"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2333b-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2333b-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2333b-147">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="2333b-147">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

