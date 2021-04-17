---
description: La \_ classe WMI d’association CIMLogicalDeviceCIMDataFile Win32 associe des périphériques logiques et des fichiers de données, indiquant les fichiers de pilote utilisés par l’appareil. Cette classe est utilisée pour détecter les pilotes de périphérique utilisés par un périphérique.
ms.assetid: 892272de-920d-4fa0-adbc-f584ed6e8748
ms.tgt_platform: multiple
title: Classe Win32_CIMLogicalDeviceCIMDataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CIMLogicalDeviceCIMDataFile
- Win32_CIMLogicalDeviceCIMDataFile.Dependent
- Win32_CIMLogicalDeviceCIMDataFile.Antecedent
- Win32_CIMLogicalDeviceCIMDataFile.Purpose
- Win32_CIMLogicalDeviceCIMDataFile.PurposeDescription
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 15db6209360cbd150a722dc98b6255afd696cbe9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523999"
---
# <a name="win32_cimlogicaldevicecimdatafile-class"></a><span data-ttu-id="43d1b-104">\_Classe CIMLogicalDeviceCIMDataFile Win32</span><span class="sxs-lookup"><span data-stu-id="43d1b-104">Win32\_CIMLogicalDeviceCIMDataFile class</span></span>

<span data-ttu-id="43d1b-105">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) d’association **\_ CIMLogicalDeviceCIMDataFile Win32** associe des périphériques logiques et des fichiers de données, indiquant les fichiers de pilote utilisés par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="43d1b-105">The **Win32\_CIMLogicalDeviceCIMDataFile** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates logical devices and data files, indicating the driver files used by the device.</span></span> <span data-ttu-id="43d1b-106">Cette classe est utilisée pour détecter les pilotes de périphérique utilisés par un périphérique.</span><span class="sxs-lookup"><span data-stu-id="43d1b-106">This class is used to discover which device drivers a device uses.</span></span>

<span data-ttu-id="43d1b-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="43d1b-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="43d1b-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="43d1b-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="43d1b-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="43d1b-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C510-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_CIMLogicalDeviceCIMDataFile : CIM_Dependency
{
  CIM_DataFile      REF Dependent;
  CIM_LogicalDevice REF Antecedent;
  uint16                Purpose;
  string                PurposeDescription;
};
```

## <a name="members"></a><span data-ttu-id="43d1b-110">Membres</span><span class="sxs-lookup"><span data-stu-id="43d1b-110">Members</span></span>

<span data-ttu-id="43d1b-111">La classe **Win32 \_ CIMLogicalDeviceCIMDataFile** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="43d1b-111">The **Win32\_CIMLogicalDeviceCIMDataFile** class has these types of members:</span></span>

-   [<span data-ttu-id="43d1b-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="43d1b-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="43d1b-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="43d1b-113">Properties</span></span>

<span data-ttu-id="43d1b-114">La classe **Win32 \_ CIMLogicalDeviceCIMDataFile** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="43d1b-114">The **Win32\_CIMLogicalDeviceCIMDataFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="43d1b-115">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="43d1b-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43d1b-116">Type de données **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="43d1b-116">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="43d1b-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="43d1b-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43d1b-118">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| CIM \_ LogicalDevice")</span><span class="sxs-lookup"><span data-stu-id="43d1b-118">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="43d1b-119">[**\_ LogicalDevice CIM**](cim-logicaldevice.md) qui représente les propriétés de l’appareil logique utilisé par le fichier de données.</span><span class="sxs-lookup"><span data-stu-id="43d1b-119">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that represents the properties of the logical device that is being used by the data file.</span></span>

</dd> <dt>

<span data-ttu-id="43d1b-120">**Charge**</span><span class="sxs-lookup"><span data-stu-id="43d1b-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43d1b-121">Type de données **: \_ fichier** de données CIM</span><span class="sxs-lookup"><span data-stu-id="43d1b-121">Data type: **CIM\_DataFile**</span></span>
</dt> <dt>

<span data-ttu-id="43d1b-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="43d1b-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43d1b-123">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) (« dépendant »), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« fichier de \| fichier CIM CIM \_ »)</span><span class="sxs-lookup"><span data-stu-id="43d1b-123">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_DataFile")</span></span>
</dt> </dl>

<span data-ttu-id="43d1b-124">Fichier de données [**CIM \_**](cim-datafile.md) qui représente les propriétés du fichier de données affecté à l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="43d1b-124">A [**CIM\_DataFile**](cim-datafile.md) that represents the properties of the data file assigned to the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="43d1b-125">**Objectif**</span><span class="sxs-lookup"><span data-stu-id="43d1b-125">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43d1b-126">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="43d1b-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="43d1b-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="43d1b-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43d1b-128">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM")</span><span class="sxs-lookup"><span data-stu-id="43d1b-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM")</span></span>
</dt> </dl>

<span data-ttu-id="43d1b-129">Rôle joué par le fichier de données en ce qui concerne son appareil logique associé.</span><span class="sxs-lookup"><span data-stu-id="43d1b-129">Role that the data file plays with regard to its associated logical device.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="43d1b-130">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="43d1b-130">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="43d1b-131">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="43d1b-131">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Driver"></span><span id="driver"></span><span id="DRIVER"></span>

<span data-ttu-id="43d1b-132">**Pilote** (2)</span><span class="sxs-lookup"><span data-stu-id="43d1b-132">**Driver** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Configuration_Software"></span><span id="configuration_software"></span><span id="CONFIGURATION_SOFTWARE"></span>

<span data-ttu-id="43d1b-133">**Logiciel de configuration** (3)</span><span class="sxs-lookup"><span data-stu-id="43d1b-133">**Configuration Software** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_Software"></span><span id="application_software"></span><span id="APPLICATION_SOFTWARE"></span>

<span data-ttu-id="43d1b-134">**Logiciel d’application** (4)</span><span class="sxs-lookup"><span data-stu-id="43d1b-134">**Application Software** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Instrumentation"></span><span id="instrumentation"></span><span id="INSTRUMENTATION"></span>

<span data-ttu-id="43d1b-135">**Instrumentation** (5)</span><span class="sxs-lookup"><span data-stu-id="43d1b-135">**Instrumentation** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Firmware"></span><span id="firmware"></span><span id="FIRMWARE"></span>

<span data-ttu-id="43d1b-136">**Microprogramme** (6)</span><span class="sxs-lookup"><span data-stu-id="43d1b-136">**Firmware** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="43d1b-137">**PurposeDescription**</span><span class="sxs-lookup"><span data-stu-id="43d1b-137">**PurposeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43d1b-138">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="43d1b-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43d1b-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="43d1b-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43d1b-140">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM")</span><span class="sxs-lookup"><span data-stu-id="43d1b-140">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM")</span></span>
</dt> </dl>

<span data-ttu-id="43d1b-141">Étend la valeur de la propriété **Purpose** de cette classe.</span><span class="sxs-lookup"><span data-stu-id="43d1b-141">Extends the value of the **Purpose** property of this class.</span></span>

<span data-ttu-id="43d1b-142">Exemple : « lecteur de disquette »</span><span class="sxs-lookup"><span data-stu-id="43d1b-142">Example: "Floppy Disk Driver"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="43d1b-143">Notes</span><span class="sxs-lookup"><span data-stu-id="43d1b-143">Remarks</span></span>

<span data-ttu-id="43d1b-144">La classe **Win32 \_ CIMLogicalDeviceCIMDataFile** est dérivée de la [**\_ dépendance CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="43d1b-144">The **Win32\_CIMLogicalDeviceCIMDataFile** class is derived from [**CIM\_Dependency**](cim-logicaldevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="43d1b-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="43d1b-145">Requirements</span></span>



| <span data-ttu-id="43d1b-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="43d1b-146">Requirement</span></span> | <span data-ttu-id="43d1b-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="43d1b-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="43d1b-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="43d1b-148">Minimum supported client</span></span><br/> | <span data-ttu-id="43d1b-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="43d1b-149">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="43d1b-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="43d1b-150">Minimum supported server</span></span><br/> | <span data-ttu-id="43d1b-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="43d1b-151">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="43d1b-152">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="43d1b-152">Namespace</span></span><br/>                | <span data-ttu-id="43d1b-153">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="43d1b-153">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="43d1b-154">MOF</span><span class="sxs-lookup"><span data-stu-id="43d1b-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="43d1b-155"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="43d1b-155"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="43d1b-156">DLL</span><span class="sxs-lookup"><span data-stu-id="43d1b-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43d1b-157"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43d1b-157"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43d1b-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="43d1b-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43d1b-159">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="43d1b-159">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

<span data-ttu-id="43d1b-160">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="43d1b-160">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

