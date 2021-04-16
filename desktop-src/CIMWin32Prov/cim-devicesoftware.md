---
description: La \_ relation DEVICESOFTWARE CIM identifie les logiciels associés à un appareil, tels que les pilotes, les logiciels de configuration ou d’application, ou le microprogramme.
ms.assetid: 831d0014-2a01-49f4-9642-fae5682f0388
ms.tgt_platform: multiple
title: Classe CIM_DeviceSoftware
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceSoftware
- CIM_DeviceSoftware.Dependent
- CIM_DeviceSoftware.Antecedent
- CIM_DeviceSoftware.Purpose
- CIM_DeviceSoftware.PurposeDescription
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 467fa670e8bb3f7d6ee967e6dd422102a2026a57
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523887"
---
# <a name="cim_devicesoftware-class"></a><span data-ttu-id="df0c8-103">\_Classe CIM DeviceSoftware</span><span class="sxs-lookup"><span data-stu-id="df0c8-103">CIM\_DeviceSoftware class</span></span>

<span data-ttu-id="df0c8-104">La **relation \_ DeviceSoftware CIM** identifie les logiciels associés à un appareil, tels que les pilotes, les logiciels de configuration ou d’application, ou le microprogramme.</span><span class="sxs-lookup"><span data-stu-id="df0c8-104">The **CIM\_DeviceSoftware** relationship identifies software that is associated with a device, such as drivers, configuration or application software, or firmware.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="df0c8-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="df0c8-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="df0c8-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="df0c8-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="df0c8-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="df0c8-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="df0c8-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="df0c8-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="df0c8-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="df0c8-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{36363AAA-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_DeviceSoftware : CIM_Dependency
{
  CIM_LogicalDevice   REF Dependent;
  CIM_SoftwareElement REF Antecedent;
  uint16                  Purpose;
  string                  PurposeDescription;
};
```

## <a name="members"></a><span data-ttu-id="df0c8-110">Membres</span><span class="sxs-lookup"><span data-stu-id="df0c8-110">Members</span></span>

<span data-ttu-id="df0c8-111">La classe **CIM \_ DeviceSoftware** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="df0c8-111">The **CIM\_DeviceSoftware** class has these types of members:</span></span>

-   [<span data-ttu-id="df0c8-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="df0c8-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="df0c8-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="df0c8-113">Properties</span></span>

<span data-ttu-id="df0c8-114">La classe **CIM \_ DeviceSoftware** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="df0c8-114">The **CIM\_DeviceSoftware** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="df0c8-115">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="df0c8-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df0c8-116">Type de données : **CIM \_ SoftwareElement**</span><span class="sxs-lookup"><span data-stu-id="df0c8-116">Data type: **CIM\_SoftwareElement**</span></span>
</dt> <dt>

<span data-ttu-id="df0c8-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df0c8-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df0c8-118">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="df0c8-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="df0c8-119">[**\_ SoftwareElement CIM**](cim-softwareelement.md) qui décrit l’élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="df0c8-119">A [**CIM\_SoftwareElement**](cim-softwareelement.md) that describes the software element.</span></span>

</dd> <dt>

<span data-ttu-id="df0c8-120">**Charge**</span><span class="sxs-lookup"><span data-stu-id="df0c8-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df0c8-121">Type de données **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="df0c8-121">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="df0c8-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df0c8-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df0c8-123">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="df0c8-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="df0c8-124">[**\_ LogicalDevice CIM**](cim-logicaldevice.md) qui décrit l’appareil logique qui requiert ou utilise le logiciel.</span><span class="sxs-lookup"><span data-stu-id="df0c8-124">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the logical device that requires or uses the software.</span></span>

</dd> <dt>

<span data-ttu-id="df0c8-125">**Objectif**</span><span class="sxs-lookup"><span data-stu-id="df0c8-125">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df0c8-126">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df0c8-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="df0c8-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df0c8-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df0c8-128">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ DeviceSoftware**.**PurposeDescription**")</span><span class="sxs-lookup"><span data-stu-id="df0c8-128">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_DeviceSoftware**.**PurposeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="df0c8-129">Rôle que le logiciel prend concernant son appareil associé.</span><span class="sxs-lookup"><span data-stu-id="df0c8-129">Role that the software takes regarding its associated device.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="df0c8-130"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="df0c8-130"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="df0c8-131">Inconnu.</span><span class="sxs-lookup"><span data-stu-id="df0c8-131">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="df0c8-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="df0c8-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="df0c8-133">Autre.</span><span class="sxs-lookup"><span data-stu-id="df0c8-133">Other.</span></span>

</dd> <dt>

<span id="Driver"></span><span id="driver"></span><span id="DRIVER"></span>

<span data-ttu-id="df0c8-134"><span id="Driver"></span><span id="driver"></span><span id="DRIVER"></span>**Pilote** (2)</span><span class="sxs-lookup"><span data-stu-id="df0c8-134"><span id="Driver"></span><span id="driver"></span><span id="DRIVER"></span>**Driver** (2)</span></span>


</dt> <dd>

<span data-ttu-id="df0c8-135">Pilote.</span><span class="sxs-lookup"><span data-stu-id="df0c8-135">Driver.</span></span>

</dd> <dt>

<span id="Configuration_Software"></span><span id="configuration_software"></span><span id="CONFIGURATION_SOFTWARE"></span>

<span data-ttu-id="df0c8-136"><span id="Configuration_Software"></span><span id="configuration_software"></span><span id="CONFIGURATION_SOFTWARE"></span>**Logiciel de configuration** (3)</span><span class="sxs-lookup"><span data-stu-id="df0c8-136"><span id="Configuration_Software"></span><span id="configuration_software"></span><span id="CONFIGURATION_SOFTWARE"></span>**Configuration Software** (3)</span></span>


</dt> <dd>

<span data-ttu-id="df0c8-137">Logiciel de configuration.</span><span class="sxs-lookup"><span data-stu-id="df0c8-137">Configuration software.</span></span>

</dd> <dt>

<span id="Application_Software"></span><span id="application_software"></span><span id="APPLICATION_SOFTWARE"></span>

<span data-ttu-id="df0c8-138"><span id="Application_Software"></span><span id="application_software"></span><span id="APPLICATION_SOFTWARE"></span>**Logiciel d’application** (4)</span><span class="sxs-lookup"><span data-stu-id="df0c8-138"><span id="Application_Software"></span><span id="application_software"></span><span id="APPLICATION_SOFTWARE"></span>**Application Software** (4)</span></span>


</dt> <dd>

<span data-ttu-id="df0c8-139">Logiciel d’application.</span><span class="sxs-lookup"><span data-stu-id="df0c8-139">Application software.</span></span>

</dd> <dt>

<span id="Instrumentation"></span><span id="instrumentation"></span><span id="INSTRUMENTATION"></span>

<span data-ttu-id="df0c8-140"><span id="Instrumentation"></span><span id="instrumentation"></span><span id="INSTRUMENTATION"></span>**Instrumentation** (5)</span><span class="sxs-lookup"><span data-stu-id="df0c8-140"><span id="Instrumentation"></span><span id="instrumentation"></span><span id="INSTRUMENTATION"></span>**Instrumentation** (5)</span></span>


</dt> <dd>

<span data-ttu-id="df0c8-141">Instrumentation.</span><span class="sxs-lookup"><span data-stu-id="df0c8-141">Instrumentation.</span></span>

</dd> <dt>

<span id="Firmware"></span><span id="firmware"></span><span id="FIRMWARE"></span>

<span data-ttu-id="df0c8-142"><span id="Firmware"></span><span id="firmware"></span><span id="FIRMWARE"></span>**Microprogramme** (6)</span><span class="sxs-lookup"><span data-stu-id="df0c8-142"><span id="Firmware"></span><span id="firmware"></span><span id="FIRMWARE"></span>**Firmware** (6)</span></span>


</dt> <dd>

<span data-ttu-id="df0c8-143">Microcode.</span><span class="sxs-lookup"><span data-stu-id="df0c8-143">Firmware.</span></span>

</dd> <dt>

<span id="BIOS"></span><span id="bios"></span>

<span data-ttu-id="df0c8-144"><span id="BIOS"></span><span id="bios"></span>**BIOS** (7)</span><span class="sxs-lookup"><span data-stu-id="df0c8-144"><span id="BIOS"></span><span id="bios"></span>**BIOS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="df0c8-145">BIOS.</span><span class="sxs-lookup"><span data-stu-id="df0c8-145">BIOS.</span></span>

</dd> <dt>

<span id="Boot_ROM"></span><span id="boot_rom"></span><span id="BOOT_ROM"></span>

<span data-ttu-id="df0c8-146"><span id="Boot_ROM"></span><span id="boot_rom"></span><span id="BOOT_ROM"></span>**ROM de démarrage** (8)</span><span class="sxs-lookup"><span data-stu-id="df0c8-146"><span id="Boot_ROM"></span><span id="boot_rom"></span><span id="BOOT_ROM"></span>**Boot ROM** (8)</span></span>


</dt> <dd>

<span data-ttu-id="df0c8-147">ROM de démarrage.</span><span class="sxs-lookup"><span data-stu-id="df0c8-147">Boot ROM.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="df0c8-148">**PurposeDescription**</span><span class="sxs-lookup"><span data-stu-id="df0c8-148">**PurposeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df0c8-149">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="df0c8-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df0c8-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df0c8-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df0c8-151">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ DeviceSoftware**.**Objet**»)</span><span class="sxs-lookup"><span data-stu-id="df0c8-151">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_DeviceSoftware**.**Purpose**")</span></span>
</dt> </dl>

<span data-ttu-id="df0c8-152">Chaîne de forme libre qui fournit plus d’informations sur la propriété **Purpose** , par exemple, « application Software ».</span><span class="sxs-lookup"><span data-stu-id="df0c8-152">Free-form string that provides more information for the **Purpose** property, for example, "Application Software".</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="df0c8-153">Notes</span><span class="sxs-lookup"><span data-stu-id="df0c8-153">Remarks</span></span>

<span data-ttu-id="df0c8-154">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="df0c8-154">WMI does not implement this class.</span></span>

<span data-ttu-id="df0c8-155">La classe **CIM \_ DeviceSoftware** est dérivée de la [**\_ dépendance CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="df0c8-155">The **CIM\_DeviceSoftware** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="df0c8-156">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="df0c8-156">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="df0c8-157">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="df0c8-157">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="df0c8-158">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="df0c8-158">Requirements</span></span>



| <span data-ttu-id="df0c8-159">Condition requise</span><span class="sxs-lookup"><span data-stu-id="df0c8-159">Requirement</span></span> | <span data-ttu-id="df0c8-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="df0c8-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="df0c8-161">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="df0c8-161">Minimum supported client</span></span><br/> | <span data-ttu-id="df0c8-162">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="df0c8-162">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="df0c8-163">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="df0c8-163">Minimum supported server</span></span><br/> | <span data-ttu-id="df0c8-164">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="df0c8-164">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="df0c8-165">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="df0c8-165">Namespace</span></span><br/>                | <span data-ttu-id="df0c8-166">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="df0c8-166">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="df0c8-167">MOF</span><span class="sxs-lookup"><span data-stu-id="df0c8-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="df0c8-168"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="df0c8-168"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="df0c8-169">DLL</span><span class="sxs-lookup"><span data-stu-id="df0c8-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df0c8-170"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df0c8-170"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df0c8-171">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="df0c8-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df0c8-172">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="df0c8-172">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

