---
description: La \_ classe WMI PrinterDriver WMI représente les pilotes pour une \_ instance d’imprimante Win32.
ms.assetid: baf48bbf-60a3-4d9b-93b7-c1b22518a9c1
ms.tgt_platform: multiple
title: Classe Win32_PrinterDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterDriver
- Win32_PrinterDriver.Caption
- Win32_PrinterDriver.ConfigFile
- Win32_PrinterDriver.CreationClassName
- Win32_PrinterDriver.DataFile
- Win32_PrinterDriver.DefaultDataType
- Win32_PrinterDriver.DependentFiles
- Win32_PrinterDriver.Description
- Win32_PrinterDriver.DriverPath
- Win32_PrinterDriver.FilePath
- Win32_PrinterDriver.HelpFile
- Win32_PrinterDriver.InfName
- Win32_PrinterDriver.InstallDate
- Win32_PrinterDriver.MonitorName
- Win32_PrinterDriver.Name
- Win32_PrinterDriver.OEMUrl
- Win32_PrinterDriver.Started
- Win32_PrinterDriver.StartMode
- Win32_PrinterDriver.Status
- Win32_PrinterDriver.SupportedPlatform
- Win32_PrinterDriver.SystemCreationClassName
- Win32_PrinterDriver.SystemName
- Win32_PrinterDriver.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 615d6561e12f67edee34e0de84dade12f250e0f0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861173"
---
# <a name="win32_printerdriver-class"></a><span data-ttu-id="dccdb-103">\_Classe PrinterDriver Win32</span><span class="sxs-lookup"><span data-stu-id="dccdb-103">Win32\_PrinterDriver class</span></span>

<span data-ttu-id="dccdb-104">La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ PrinterDriver** WMI représente les pilotes pour une instance d' [**\_ imprimante Win32**](win32-printer.md) .</span><span class="sxs-lookup"><span data-stu-id="dccdb-104">The **Win32\_PrinterDriver** [WMI class](../wmisdk/retrieving-a-class.md) represents the drivers for a [**Win32\_Printer**](win32-printer.md) instance.</span></span>

<span data-ttu-id="dccdb-105">La syntaxe suivante est simplifiée du code format MOF (MOF) et inclut toutes les propriétés héritées, mais exclut les méthodes.</span><span class="sxs-lookup"><span data-stu-id="dccdb-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties, but excludes methods.</span></span> <span data-ttu-id="dccdb-106">Pour obtenir des informations de référence sur les méthodes, consultez le tableau des méthodes dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="dccdb-106">For reference information about methods, see the table of methods in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="dccdb-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dccdb-107">Syntax</span></span>

``` syntax
class Win32_PrinterDriver : CIM_Service
{
  string   Caption;
  string   ConfigFile;
  string   CreationClassName;
  string   DataFile;
  string   DefaultDataType;
  string   DependentFiles[];
  string   Description;
  string   DriverPath;
  string   FilePath;
  string   HelpFile;
  string   InfName;
  datetime InstallDate;
  string   MonitorName;
  string   Name;
  string   OEMUrl;
  boolean  Started;
  string   StartMode;
  string   Status;
  string   SupportedPlatform;
  string   SystemCreationClassName;
  string   SystemName;
  uint16   Version;
};
```

## <a name="members"></a><span data-ttu-id="dccdb-108">Membres</span><span class="sxs-lookup"><span data-stu-id="dccdb-108">Members</span></span>

<span data-ttu-id="dccdb-109">La classe **Win32 \_ PrinterDriver** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="dccdb-109">The **Win32\_PrinterDriver** class has these types of members:</span></span>

-   [<span data-ttu-id="dccdb-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="dccdb-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="dccdb-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="dccdb-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="dccdb-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="dccdb-112">Methods</span></span>

<span data-ttu-id="dccdb-113">La classe **Win32 \_ PrinterDriver** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="dccdb-113">The **Win32\_PrinterDriver** class has these methods.</span></span>



| <span data-ttu-id="dccdb-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="dccdb-114">Method</span></span>                                                                           | <span data-ttu-id="dccdb-115">Description</span><span class="sxs-lookup"><span data-stu-id="dccdb-115">Description</span></span>                              |
|:---------------------------------------------------------------------------------|:-----------------------------------------|
| [<span data-ttu-id="dccdb-116">**AddPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="dccdb-116">**AddPrinterDriver**</span></span>](addprinterdriver-method-in-class-win32-printerdriver.md) | <span data-ttu-id="dccdb-117">Crée un nouveau pilote d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="dccdb-117">Creates a new printer driver.</span></span><br/> |
| [<span data-ttu-id="dccdb-118">**StartService**</span><span class="sxs-lookup"><span data-stu-id="dccdb-118">**StartService**</span></span>](startservice-method-in-class-win32-printerdriver.md)         | <span data-ttu-id="dccdb-119">Démarre le service d’impression.</span><span class="sxs-lookup"><span data-stu-id="dccdb-119">Starts print service.</span></span><br/>         |
| [<span data-ttu-id="dccdb-120">**StopService**</span><span class="sxs-lookup"><span data-stu-id="dccdb-120">**StopService**</span></span>](stopservice-method-in-class-win32-printerdriver.md)           | <span data-ttu-id="dccdb-121">Arrête le service d’impression.</span><span class="sxs-lookup"><span data-stu-id="dccdb-121">Stops print service.</span></span><br/>          |



 

### <a name="properties"></a><span data-ttu-id="dccdb-122">Propriétés</span><span class="sxs-lookup"><span data-stu-id="dccdb-122">Properties</span></span>

<span data-ttu-id="dccdb-123">La classe **Win32 \_ PrinterDriver** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="dccdb-123">The **Win32\_PrinterDriver** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dccdb-124">**Caption**</span><span class="sxs-lookup"><span data-stu-id="dccdb-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dccdb-125">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="dccdb-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dccdb-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dccdb-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dccdb-127">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="dccdb-127">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="dccdb-128">Brève description de l’objet : chaîne d’une ligne.</span><span class="sxs-lookup"><span data-stu-id="dccdb-128">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="dccdb-129">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="dccdb-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dccdb-130">**ConfigFile**</span><span class="sxs-lookup"><span data-stu-id="dccdb-130">**ConfigFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dccdb-131">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="dccdb-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dccdb-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dccdb-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dccdb-133">Fichier de configuration pour ce pilote d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="dccdb-133">Configuration file for this printer driver.</span></span>

<span data-ttu-id="dccdb-134">Exemple : « pscrptui.dll »</span><span class="sxs-lookup"><span data-stu-id="dccdb-134">Example: "pscrptui.dll"</span></span>

</dd> <dt>

<span data-ttu-id="dccdb-135">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="dccdb-135">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dccdb-136">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="dccdb-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dccdb-137">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dccdb-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dccdb-138">Qualificateurs : [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("nom de la classe")</span><span class="sxs-lookup"><span data-stu-id="dccdb-138">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="dccdb-139">Nom de la classe ou de la sous-classe utilisée lors de la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="dccdb-139">Name of the class or the subclass used in the creation of an instance.</span></span> <span data-ttu-id="dccdb-140">Quand elle est utilisée avec les autres propriétés de clé de cette classe, cette propriété autorise l’identification unique de toutes les instances de cette classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="dccdb-140">When used with the other key properties of this class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="dccdb-141">Cette propriété est héritée [**du \_ service CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="dccdb-141">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="dccdb-142">**DataFile**</span><span class="sxs-lookup"><span data-stu-id="dccdb-142">**DataFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dccdb-143">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="dccdb-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dccdb-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dccdb-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dccdb-145">Qualificateurs : [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) (nom de fichier de fichier CIM \_ )</span><span class="sxs-lookup"><span data-stu-id="dccdb-145">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) (CIM\_DataFile.FileName)</span></span>
</dt> </dl>

<span data-ttu-id="dccdb-146">Fichier de données pour ce pilote d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="dccdb-146">Data file for this printer driver.</span></span>

<span data-ttu-id="dccdb-147">Exemple : « qms810. PPD »</span><span class="sxs-lookup"><span data-stu-id="dccdb-147">Example: "qms810.ppd"</span></span>

</dd> <dt>

<span data-ttu-id="dccdb-148">**DefaultDataType**</span><span class="sxs-lookup"><span data-stu-id="dccdb-148">**DefaultDataType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dccdb-149">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="dccdb-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dccdb-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dccdb-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dccdb-151">Type de données par défaut pour ce pilote d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="dccdb-151">Default data type for this printer driver.</span></span>

<span data-ttu-id="dccdb-152">Exemple : « EMF »</span><span class="sxs-lookup"><span data-stu-id="dccdb-152">Example: "EMF"</span></span>

</dd> <dt>

<span data-ttu-id="dccdb-153">**DependentFiles**</span><span class="sxs-lookup"><span data-stu-id="dccdb-153">**DependentFiles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dccdb-154">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="dccdb-154">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="dccdb-155">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dccdb-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dccdb-156">Tableau de fichiers dépendants pour ce pilote d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="dccdb-156">Array of dependent files for this printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="dccdb-157">**Description**</span><span class="sxs-lookup"><span data-stu-id="dccdb-157">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dccdb-158">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="dccdb-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dccdb-159">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dccdb-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dccdb-160">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="dccdb-160">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="dccdb-161">Commentaire qui décrit le lien.</span><span class="sxs-lookup"><span data-stu-id="dccdb-161">Comment that describes the link.</span></span>

<span data-ttu-id="dccdb-162">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="dccdb-162">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dccdb-163">**DriverPath**</span><span class="sxs-lookup"><span data-stu-id="dccdb-163">**DriverPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dccdb-164">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="dccdb-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dccdb-165">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dccdb-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dccdb-166">Qualificateurs : [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( \_ fichier de fichier. Path CIM)</span><span class="sxs-lookup"><span data-stu-id="dccdb-166">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) (CIM\_DataFile.Path)</span></span>
</dt> </dl>

<span data-ttu-id="dccdb-167">Chemin d’accès pour ce pilote d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="dccdb-167">Path for this printer driver.</span></span>

<span data-ttu-id="dccdb-168">Exemple : « C : \\ \\ drivers \\ \\pscript.dll »</span><span class="sxs-lookup"><span data-stu-id="dccdb-168">Example: "C:\\\\drivers\\\\pscript.dll"</span></span>

</dd> <dt>

<span data-ttu-id="dccdb-169">**FilePath**</span><span class="sxs-lookup"><span data-stu-id="dccdb-169">**FilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dccdb-170">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="dccdb-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dccdb-171">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="dccdb-171">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dccdb-172">Chemin d’accès au fichier INF utilisé.</span><span class="sxs-lookup"><span data-stu-id="dccdb-172">Path to the INF file being used.</span></span>

<span data-ttu-id="dccdb-173">Exemple : « c : \\ \\ temp \\ \\ Driver »</span><span class="sxs-lookup"><span data-stu-id="dccdb-173">Example: "c:\\\\temp\\\\driver"</span></span>

</dd> <dt>

<span data-ttu-id="dccdb-174">**HelpFile**</span><span class="sxs-lookup"><span data-stu-id="dccdb-174">**HelpFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dccdb-175">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="dccdb-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dccdb-176">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dccdb-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dccdb-177">Fichier d’aide pour ce pilote d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="dccdb-177">Help file for this printer driver.</span></span>

<span data-ttu-id="dccdb-178">Exemple : « PSCRPTUI. hlp »</span><span class="sxs-lookup"><span data-stu-id="dccdb-178">Example: "pscrptui.hlp"</span></span>

</dd> <dt>

<span data-ttu-id="dccdb-179">**InfName**</span><span class="sxs-lookup"><span data-stu-id="dccdb-179">**InfName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dccdb-180">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="dccdb-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dccdb-181">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="dccdb-181">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dccdb-182">Nom du fichier INF utilisé.</span><span class="sxs-lookup"><span data-stu-id="dccdb-182">Name of the INF file being used.</span></span> <span data-ttu-id="dccdb-183">La valeur par défaut consiste à utiliser un fichier INF d’imprimante fourni par le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="dccdb-183">The default is to use an operating system provided printer INF file.</span></span> <span data-ttu-id="dccdb-184">Un nom de fichier différent est utilisé si le pilote est fourni directement par le fabricant de l’imprimante et non par le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="dccdb-184">A different file name is used if the driver is provided directly by the manufacturer of the printer and not the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="dccdb-185">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="dccdb-185">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dccdb-186">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="dccdb-186">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="dccdb-187">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dccdb-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dccdb-188">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="dccdb-188">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="dccdb-189">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="dccdb-189">Date and time the object is installed.</span></span> <span data-ttu-id="dccdb-190">Cette propriété ne requiert pas de valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="dccdb-190">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="dccdb-191">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="dccdb-191">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dccdb-192">**Nomdumoniteur**</span><span class="sxs-lookup"><span data-stu-id="dccdb-192">**MonitorName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dccdb-193">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="dccdb-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dccdb-194">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dccdb-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dccdb-195">Nom de l’analyse pour ce pilote d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="dccdb-195">Name of the monitor for this printer driver.</span></span>

<span data-ttu-id="dccdb-196">Exemple : « PJL Monitor »</span><span class="sxs-lookup"><span data-stu-id="dccdb-196">Example: "PJL monitor"</span></span>

</dd> <dt>

<span data-ttu-id="dccdb-197">**Nom**</span><span class="sxs-lookup"><span data-stu-id="dccdb-197">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dccdb-198">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="dccdb-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dccdb-199">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dccdb-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dccdb-200">Qualificateurs : [ **clé**](../wmisdk/key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="dccdb-200">Qualifiers: [**Key**](../wmisdk/key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="dccdb-201">Nom du pilote pour cette imprimante.</span><span class="sxs-lookup"><span data-stu-id="dccdb-201">Driver name for this printer.</span></span> <span data-ttu-id="dccdb-202">Il s’agit d’une clé composée composée des valeurs **Name**, **version** et **SupportedPlatform** .</span><span class="sxs-lookup"><span data-stu-id="dccdb-202">This is a compound key composed of the **Name**, **Version**, and **SupportedPlatform** values.</span></span>

<span data-ttu-id="dccdb-203">Cette propriété est héritée de l' [**\_ ManagedSystemElement CIM**](cim-managedsystemelement.md) et remplace la définition de **nom** dans cette classe.</span><span class="sxs-lookup"><span data-stu-id="dccdb-203">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) and overrides the **Name** definition in that class.</span></span>

</dd> <dt>

<span data-ttu-id="dccdb-204">**OEMUrl**</span><span class="sxs-lookup"><span data-stu-id="dccdb-204">**OEMUrl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dccdb-205">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="dccdb-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dccdb-206">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dccdb-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dccdb-207">World Wide Web (WWW) le lien vers le site Web du fabricant de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="dccdb-207">World Wide Web (WWW) link to the printer manufacturer's website.</span></span> <span data-ttu-id="dccdb-208">Notez que cette propriété n’est pas remplie lorsque le fichier. inf Win32 est utilisé et s’applique uniquement aux pilotes fournis directement auprès du fabricant.</span><span class="sxs-lookup"><span data-stu-id="dccdb-208">Note that this property is not populated when the Win32.inf file is used, and is only applicable for drivers provided directly from the manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="dccdb-209">**Cours**</span><span class="sxs-lookup"><span data-stu-id="dccdb-209">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dccdb-210">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="dccdb-210">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dccdb-211">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dccdb-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dccdb-212">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Started")</span><span class="sxs-lookup"><span data-stu-id="dccdb-212">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Started")</span></span>
</dt> </dl>

<span data-ttu-id="dccdb-213">Si la **valeur est true**, le service est démarré.</span><span class="sxs-lookup"><span data-stu-id="dccdb-213">If **TRUE**, the service is started.</span></span> <span data-ttu-id="dccdb-214">Si la **valeur est false**, le service est arrêté.</span><span class="sxs-lookup"><span data-stu-id="dccdb-214">If **FALSE**, the service is stopped.</span></span>

<span data-ttu-id="dccdb-215">Cette propriété est héritée [**du \_ service CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="dccdb-215">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="dccdb-216">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="dccdb-216">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dccdb-217">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="dccdb-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dccdb-218">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dccdb-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dccdb-219">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) (« mode de démarrage »)</span><span class="sxs-lookup"><span data-stu-id="dccdb-219">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Start Mode")</span></span>
</dt> </dl>

<span data-ttu-id="dccdb-220">Le mode de démarrage du service est démarré automatiquement par un système d’exploitation, ou démarré uniquement à la demande.</span><span class="sxs-lookup"><span data-stu-id="dccdb-220">Start mode of the service is automatically started by an operating system, or only started when requested.</span></span>

<span data-ttu-id="dccdb-221">Cette propriété est héritée [**du \_ service CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="dccdb-221">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

<span data-ttu-id="dccdb-222">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="dccdb-222">The following are possible values:</span></span>

<dl> <dd><span data-ttu-id="dccdb-223">Automatique</span><span class="sxs-lookup"><span data-stu-id="dccdb-223">"Automatic"</span></span></dd> <dd><span data-ttu-id="dccdb-224">Opération</span><span class="sxs-lookup"><span data-stu-id="dccdb-224">"Manual"</span></span></dd> </dl>

<dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="dccdb-225">**Automatique** (« automatique »)</span><span class="sxs-lookup"><span data-stu-id="dccdb-225">**Automatic** ("Automatic")</span></span>


</dt> <dd></dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="dccdb-226">**Manuel** (« manuel »)</span><span class="sxs-lookup"><span data-stu-id="dccdb-226">**Manual** ("Manual")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dccdb-227">**État**</span><span class="sxs-lookup"><span data-stu-id="dccdb-227">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dccdb-228">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="dccdb-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dccdb-229">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dccdb-229">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dccdb-230">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="dccdb-230">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="dccdb-231">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="dccdb-231">Current status of the object.</span></span> <span data-ttu-id="dccdb-232">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="dccdb-232">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="dccdb-233">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="dccdb-233">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="dccdb-234">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="dccdb-234">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="dccdb-235">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="dccdb-235">The latter, "Service", can apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="dccdb-236">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="dccdb-236">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="dccdb-237">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="dccdb-237">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="dccdb-238">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="dccdb-238">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="dccdb-239">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="dccdb-239">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="dccdb-240">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="dccdb-240">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="dccdb-241">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="dccdb-241">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dccdb-242">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="dccdb-242">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="dccdb-243">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="dccdb-243">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="dccdb-244">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="dccdb-244">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="dccdb-245">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="dccdb-245">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="dccdb-246">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="dccdb-246">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="dccdb-247">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="dccdb-247">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="dccdb-248">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="dccdb-248">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="dccdb-249">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="dccdb-249">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="dccdb-250">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="dccdb-250">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dccdb-251">**SupportedPlatform**</span><span class="sxs-lookup"><span data-stu-id="dccdb-251">**SupportedPlatform**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dccdb-252">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="dccdb-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dccdb-253">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="dccdb-253">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dccdb-254">Les environnements d’exploitation auxquels le pilote est destiné.</span><span class="sxs-lookup"><span data-stu-id="dccdb-254">Operating environments that the driver is intended for.</span></span>

<span data-ttu-id="dccdb-255">Exemple : « Windows NT x86 ».</span><span class="sxs-lookup"><span data-stu-id="dccdb-255">Example: "Windows NT x86".</span></span>

</dd> <dt>

<span data-ttu-id="dccdb-256">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="dccdb-256">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dccdb-257">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="dccdb-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dccdb-258">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dccdb-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dccdb-259">Qualificateurs : [**Propaged**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" System Class Name ")</span><span class="sxs-lookup"><span data-stu-id="dccdb-259">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="dccdb-260">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="dccdb-260">Scoping system's creation class name.</span></span>

<span data-ttu-id="dccdb-261">Cette propriété est héritée [**du \_ service CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="dccdb-261">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="dccdb-262">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="dccdb-262">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dccdb-263">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="dccdb-263">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dccdb-264">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dccdb-264">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dccdb-265">Qualificateurs : [**Propaged**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" System Name ")</span><span class="sxs-lookup"><span data-stu-id="dccdb-265">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("System Name")</span></span>
</dt> </dl>

<span data-ttu-id="dccdb-266">Nom du système qui héberge ce service.</span><span class="sxs-lookup"><span data-stu-id="dccdb-266">Name of the system that hosts this service.</span></span>

<span data-ttu-id="dccdb-267">Cette propriété est héritée [**du \_ service CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="dccdb-267">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="dccdb-268">**Version**</span><span class="sxs-lookup"><span data-stu-id="dccdb-268">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dccdb-269">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dccdb-269">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dccdb-270">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="dccdb-270">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dccdb-271">Version du système d’exploitation pour le pilote d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="dccdb-271">Operating system version for the printer driver.</span></span>

<dt>

<span id="3"></span>

<span data-ttu-id="dccdb-272"><span id="3"></span>**1,3**</span><span class="sxs-lookup"><span data-stu-id="dccdb-272"><span id="3"></span>**3**</span></span>


</dt> <dd>

<span data-ttu-id="dccdb-273">2000</span><span class="sxs-lookup"><span data-stu-id="dccdb-273">Win2k</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dccdb-274">Notes</span><span class="sxs-lookup"><span data-stu-id="dccdb-274">Remarks</span></span>

<span data-ttu-id="dccdb-275">La classe **Win32 \_ PrinterDriver** est dérivée [**du \_ service CIM**](cim-service.md) qui dérive de [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="dccdb-275">The **Win32\_PrinterDriver** class is derived from [**CIM\_Service**](cim-service.md) which derives from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="dccdb-276">Les utilisateurs peuvent désinstaller un pilote d’imprimante en supprimant une instance correspondante de cette classe.</span><span class="sxs-lookup"><span data-stu-id="dccdb-276">Users can uninstall a printer driver by deleting a corresponding instance of this class.</span></span> <span data-ttu-id="dccdb-277">Pour ce faire, le privilège **SeLoadDriverPrivilege** doit être défini sur le processus appelant pour supprimer une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="dccdb-277">To do so, the calling process must have the **SeLoadDriverPrivilege** privilege set to delete an instance of this class.</span></span>

## <a name="examples"></a><span data-ttu-id="dccdb-278">Exemples</span><span class="sxs-lookup"><span data-stu-id="dccdb-278">Examples</span></span>

<span data-ttu-id="dccdb-279">L’exemple de gestion de pilotes d’imprimante [et de pilotes d’imprimante](https://Gallery.TechNet.Microsoft.Com/710bb2ad-9a8d-42cb-b142-cda2c1452548) pour les pilotes d’imprimante et les ports d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="dccdb-279">The [Manage Printer and Printer Drivers](https://Gallery.TechNet.Microsoft.Com/710bb2ad-9a8d-42cb-b142-cda2c1452548) VBScript sample manages printer drivers and printer ports.</span></span>

<span data-ttu-id="dccdb-280">La [discussion suivante sur les forums TechNet](https://social.technet.microsoft.com/Forums/scriptcenter/6210fa0b-0c32-4bce-a79c-dfe835922613/create-printers-in-powershell-with-wmi-win32printer-createinstance?forum=ITCG) explique comment créer une imprimante et télécharger des pilotes à partir d’un serveur.</span><span class="sxs-lookup"><span data-stu-id="dccdb-280">The following [discussion on the TechNet forums](https://social.technet.microsoft.com/Forums/scriptcenter/6210fa0b-0c32-4bce-a79c-dfe835922613/create-printers-in-powershell-with-wmi-win32printer-createinstance?forum=ITCG) describes how to create a printer and upload drivers from a server.</span></span>

<span data-ttu-id="dccdb-281">L’exemple VBScript suivant répertorie tous les pilotes d’imprimante qui ont été installés sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="dccdb-281">The following VBScript sample lists all the printer drivers that have been installed on a computer.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
Set colInstalledPrinters =  objWMIService.ExecQuery _ 
    ("Select * from Win32_PrinterDriver") 
 
For each objPrinter in colInstalledPrinters 
    Wscript.Echo "Configuration File: " & objPrinter.ConfigFile 
    Wscript.Echo "Data File: " & objPrinter.DataFile 
    Wscript.Echo "Description: " & objPrinter.Description 
    Wscript.Echo "Driver Path: " & objPrinter.DriverPath 
    Wscript.Echo "File Path: " & objPrinter.FilePath 
    Wscript.Echo "Help File: " & objPrinter.HelpFile 
    Wscript.Echo "INF Name: " & objPrinter.InfName 
    Wscript.Echo "Monitor Name: " & objPrinter.MonitorName 
    Wscript.Echo "Name: " & objPrinter.Name 
    Wscript.Echo "OEM Url: " & objPrinter.OEMUrl 
    Wscript.Echo "Supported Platform: " & objPrinter.SupportedPlatform 
    Wscript.Echo "Version: " & objPrinter.Version 
Next 
```



## <a name="requirements"></a><span data-ttu-id="dccdb-282">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dccdb-282">Requirements</span></span>



| <span data-ttu-id="dccdb-283">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dccdb-283">Requirement</span></span> | <span data-ttu-id="dccdb-284">Valeur</span><span class="sxs-lookup"><span data-stu-id="dccdb-284">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="dccdb-285">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dccdb-285">Minimum supported client</span></span><br/> | <span data-ttu-id="dccdb-286">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dccdb-286">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="dccdb-287">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dccdb-287">Minimum supported server</span></span><br/> | <span data-ttu-id="dccdb-288">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dccdb-288">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="dccdb-289">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="dccdb-289">Namespace</span></span><br/>                | <span data-ttu-id="dccdb-290">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="dccdb-290">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="dccdb-291">MOF</span><span class="sxs-lookup"><span data-stu-id="dccdb-291">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dccdb-292"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dccdb-292"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="dccdb-293">DLL</span><span class="sxs-lookup"><span data-stu-id="dccdb-293">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dccdb-294"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dccdb-294"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="dccdb-295">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dccdb-295">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dccdb-296">**\_Service CIM**</span><span class="sxs-lookup"><span data-stu-id="dccdb-296">**CIM\_Service**</span></span>](./cim-service.md)
</dt> <dt>

[<span data-ttu-id="dccdb-297">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="dccdb-297">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
