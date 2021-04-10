---
description: La \_ classe DEVICEERRORCOUNTS CIM est une classe statistique qui contient des compteurs relatifs aux erreurs pour un périphérique logique. Les types d’erreurs sont définis par CCITT (Rec X. 733) et ISO (IEC 10164-4).
ms.assetid: d65cbc78-40f2-4846-bd47-76e04b2f588b
ms.tgt_platform: multiple
title: Classe CIM_DeviceErrorCounts
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceErrorCounts
- CIM_DeviceErrorCounts.Caption
- CIM_DeviceErrorCounts.Description
- CIM_DeviceErrorCounts.CriticalErrorCount
- CIM_DeviceErrorCounts.DeviceCreationClassName
- CIM_DeviceErrorCounts.DeviceID
- CIM_DeviceErrorCounts.Name
- CIM_DeviceErrorCounts.IndeterminateErrorCount
- CIM_DeviceErrorCounts.MajorErrorCount
- CIM_DeviceErrorCounts.MinorErrorCount
- CIM_DeviceErrorCounts.SystemCreationClassName
- CIM_DeviceErrorCounts.SystemName
- CIM_DeviceErrorCounts.WarningCount
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1602e68b7254811ba8c09726feda8baa7bf23d29
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950727"
---
# <a name="cim_deviceerrorcounts-class"></a><span data-ttu-id="b9635-104">\_Classe CIM DeviceErrorCounts</span><span class="sxs-lookup"><span data-stu-id="b9635-104">CIM\_DeviceErrorCounts class</span></span>

<span data-ttu-id="b9635-105">La **classe \_ DeviceErrorCounts CIM** est une classe statistique qui contient des compteurs relatifs aux erreurs pour un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="b9635-105">The **CIM\_DeviceErrorCounts** class is a statistical class that contains error-related counters for a logical device.</span></span> <span data-ttu-id="b9635-106">Les types d’erreurs sont définis par CCITT (Rec X. 733) et ISO (IEC 10164-4).</span><span class="sxs-lookup"><span data-stu-id="b9635-106">The types of errors are defined by CCITT (Rec X.733) and ISO (IEC 10164-4).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b9635-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="b9635-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b9635-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b9635-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b9635-109">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="b9635-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="b9635-110">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="b9635-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9635-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b9635-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{117FDB8C-D025-11d2-85F5-0000F8102E5F}"), AMENDMENT]
class CIM_DeviceErrorCounts : CIM_StatisticalInformation
{
  string Caption;
  string Description;
  uint64 CriticalErrorCount;
  string DeviceCreationClassName;
  string DeviceID;
  string Name;
  uint64 IndeterminateErrorCount;
  uint64 MajorErrorCount;
  uint64 MinorErrorCount;
  string SystemCreationClassName;
  string SystemName;
  uint64 WarningCount;
};
```

## <a name="members"></a><span data-ttu-id="b9635-112">Membres</span><span class="sxs-lookup"><span data-stu-id="b9635-112">Members</span></span>

<span data-ttu-id="b9635-113">La classe **CIM \_ DeviceErrorCounts** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b9635-113">The **CIM\_DeviceErrorCounts** class has these types of members:</span></span>

-   [<span data-ttu-id="b9635-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b9635-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="b9635-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b9635-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b9635-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b9635-116">Methods</span></span>

<span data-ttu-id="b9635-117">La classe **CIM \_ DeviceErrorCounts** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="b9635-117">The **CIM\_DeviceErrorCounts** class has these methods.</span></span>



| <span data-ttu-id="b9635-118">Méthode</span><span class="sxs-lookup"><span data-stu-id="b9635-118">Method</span></span>                                                                     | <span data-ttu-id="b9635-119">Description</span><span class="sxs-lookup"><span data-stu-id="b9635-119">Description</span></span>                                                               |
|:---------------------------------------------------------------------------|:--------------------------------------------------------------------------|
| [<span data-ttu-id="b9635-120">**ResetCounter**</span><span class="sxs-lookup"><span data-stu-id="b9635-120">**ResetCounter**</span></span>](resetcounter-method-in-class-cim-deviceerrorcounts.md) | <span data-ttu-id="b9635-121">Réinitialise les compteurs d’erreur et d’avertissement.</span><span class="sxs-lookup"><span data-stu-id="b9635-121">Resets the error and warning counters.</span></span> <span data-ttu-id="b9635-122">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="b9635-122">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b9635-123">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b9635-123">Properties</span></span>

<span data-ttu-id="b9635-124">La classe **CIM \_ DeviceErrorCounts** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="b9635-124">The **CIM\_DeviceErrorCounts** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b9635-125">**Caption**</span><span class="sxs-lookup"><span data-stu-id="b9635-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9635-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b9635-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9635-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b9635-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9635-128">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="b9635-128">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="b9635-129">Description textuelle courte pour la statistique ou la métrique.</span><span class="sxs-lookup"><span data-stu-id="b9635-129">Short textual description for the statistic or metric.</span></span>

<span data-ttu-id="b9635-130">Cette propriété est héritée de la [**\_ StatisticalInformation CIM**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="b9635-130">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="b9635-131">**CriticalErrorCount**</span><span class="sxs-lookup"><span data-stu-id="b9635-131">**CriticalErrorCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9635-132">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b9635-132">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b9635-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b9635-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9635-134">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,7 ")</span><span class="sxs-lookup"><span data-stu-id="b9635-134">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.7")</span></span>
</dt> </dl>

<span data-ttu-id="b9635-135">Nombre d’erreurs critiques.</span><span class="sxs-lookup"><span data-stu-id="b9635-135">Count of the critical errors.</span></span>

<span data-ttu-id="b9635-136">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b9635-136">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b9635-137">**Description**</span><span class="sxs-lookup"><span data-stu-id="b9635-137">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9635-138">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b9635-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9635-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b9635-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9635-140">Description textuelle de la statistique ou métrique.</span><span class="sxs-lookup"><span data-stu-id="b9635-140">Textual description of the statistic or metric.</span></span>

<span data-ttu-id="b9635-141">Cette propriété est héritée de la [**\_ StatisticalInformation CIM**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="b9635-141">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="b9635-142">**DeviceCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b9635-142">**DeviceCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9635-143">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b9635-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9635-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b9635-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9635-145">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ LogicalDevice**](cim-logicaldevice.md).**CreationClassName**"), [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="b9635-145">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_LogicalDevice**](cim-logicaldevice.md).**CreationClassName**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b9635-146">Propriété **CreationClassName** de l’appareil d’étendue.</span><span class="sxs-lookup"><span data-stu-id="b9635-146">The scoping device's **CreationClassName** property.</span></span>

</dd> <dt>

<span data-ttu-id="b9635-147">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="b9635-147">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9635-148">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b9635-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9635-149">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b9635-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9635-150">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ LogicalDevice**](cim-logicaldevice.md).**DeviceID**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="b9635-150">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_LogicalDevice**](cim-logicaldevice.md).**DeviceID**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="b9635-151">Identificateur de l’appareil d’étendue.</span><span class="sxs-lookup"><span data-stu-id="b9635-151">The scoping device's identifier.</span></span>

</dd> <dt>

<span data-ttu-id="b9635-152">**IndeterminateErrorCount**</span><span class="sxs-lookup"><span data-stu-id="b9635-152">**IndeterminateErrorCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9635-153">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b9635-153">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b9635-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b9635-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9635-155">Nombre d’erreurs indéterminées.</span><span class="sxs-lookup"><span data-stu-id="b9635-155">Count of the indeterminate errors.</span></span>

<span data-ttu-id="b9635-156">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b9635-156">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b9635-157">**MajorErrorCount**</span><span class="sxs-lookup"><span data-stu-id="b9635-157">**MajorErrorCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9635-158">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b9635-158">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b9635-159">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b9635-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9635-160">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,8 ")</span><span class="sxs-lookup"><span data-stu-id="b9635-160">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.8")</span></span>
</dt> </dl>

<span data-ttu-id="b9635-161">Nombre d’erreurs majeures.</span><span class="sxs-lookup"><span data-stu-id="b9635-161">Count of the major errors.</span></span>

<span data-ttu-id="b9635-162">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b9635-162">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b9635-163">**MinorErrorCount**</span><span class="sxs-lookup"><span data-stu-id="b9635-163">**MinorErrorCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9635-164">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b9635-164">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b9635-165">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b9635-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9635-166">Nombre d’erreurs mineures.</span><span class="sxs-lookup"><span data-stu-id="b9635-166">Count of the minor errors.</span></span>

<span data-ttu-id="b9635-167">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b9635-167">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b9635-168">**Nom**</span><span class="sxs-lookup"><span data-stu-id="b9635-168">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9635-169">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b9635-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9635-170">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b9635-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9635-171">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="b9635-171">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b9635-172">La propriété de nom héritée fait partie de la clé de l’instance **CIM \_ DeviceErrorCounts** .</span><span class="sxs-lookup"><span data-stu-id="b9635-172">The inherited Name property serves as part of the key for the **CIM\_DeviceErrorCounts** instance.</span></span> <span data-ttu-id="b9635-173">L’objet est limité par le périphérique logique auquel les statistiques s’appliquent.</span><span class="sxs-lookup"><span data-stu-id="b9635-173">The object is scoped by the logical device to which the statistics apply.</span></span>

</dd> <dt>

<span data-ttu-id="b9635-174">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b9635-174">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9635-175">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b9635-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9635-176">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b9635-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9635-177">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ LogicalDevice**](cim-logicaldevice.md).**SystemCreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="b9635-177">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_LogicalDevice**](cim-logicaldevice.md).**SystemCreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b9635-178">**CreationClassName** du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="b9635-178">Scoping system's **CreationClassName**.</span></span>

</dd> <dt>

<span data-ttu-id="b9635-179">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="b9635-179">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9635-180">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b9635-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9635-181">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b9635-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9635-182">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ LogicalDevice**](cim-logicaldevice.md).**SystemName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="b9635-182">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_LogicalDevice**](cim-logicaldevice.md).**SystemName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b9635-183">Propriété de **nom** du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="b9635-183">Scoping system's **Name** property.</span></span>

</dd> <dt>

<span data-ttu-id="b9635-184">**WarningCount**</span><span class="sxs-lookup"><span data-stu-id="b9635-184">**WarningCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9635-185">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b9635-185">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b9635-186">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b9635-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9635-187">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,9 ")</span><span class="sxs-lookup"><span data-stu-id="b9635-187">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.9")</span></span>
</dt> </dl>

<span data-ttu-id="b9635-188">Nombre d’avertissements.</span><span class="sxs-lookup"><span data-stu-id="b9635-188">Count of the warnings.</span></span>

<span data-ttu-id="b9635-189">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b9635-189">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b9635-190">Notes</span><span class="sxs-lookup"><span data-stu-id="b9635-190">Remarks</span></span>

<span data-ttu-id="b9635-191">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="b9635-191">WMI does not implement this class.</span></span>

<span data-ttu-id="b9635-192">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="b9635-192">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b9635-193">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="b9635-193">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9635-194">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b9635-194">Requirements</span></span>



| <span data-ttu-id="b9635-195">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b9635-195">Requirement</span></span> | <span data-ttu-id="b9635-196">Valeur</span><span class="sxs-lookup"><span data-stu-id="b9635-196">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b9635-197">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b9635-197">Minimum supported client</span></span><br/> | <span data-ttu-id="b9635-198">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b9635-198">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b9635-199">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b9635-199">Minimum supported server</span></span><br/> | <span data-ttu-id="b9635-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b9635-200">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b9635-201">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b9635-201">Namespace</span></span><br/>                | <span data-ttu-id="b9635-202">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="b9635-202">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b9635-203">MOF</span><span class="sxs-lookup"><span data-stu-id="b9635-203">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b9635-204"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b9635-204"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b9635-205">DLL</span><span class="sxs-lookup"><span data-stu-id="b9635-205">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9635-206"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9635-206"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9635-207">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b9635-207">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9635-208">**\_STATISTICALINFORMATION CIM**</span><span class="sxs-lookup"><span data-stu-id="b9635-208">**CIM\_StatisticalInformation**</span></span>](cim-statisticalinformation.md)
</dt> </dl>

 

