---
description: La classe de système de \_ fichiers CIM représente un fichier ou un jeu de données local sur un système informatique ou monté à distance à partir d’un serveur de fichiers.
ms.assetid: 5a54ab35-b9b6-49e6-96a8-cb2820b054eb
ms.tgt_platform: multiple
title: Classe CIM_FileSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FileSystem
- CIM_FileSystem.Caption
- CIM_FileSystem.Description
- CIM_FileSystem.InstallDate
- CIM_FileSystem.Name
- CIM_FileSystem.Status
- CIM_FileSystem.AvailableSpace
- CIM_FileSystem.BlockSize
- CIM_FileSystem.CasePreserved
- CIM_FileSystem.CaseSensitive
- CIM_FileSystem.CodeSet
- CIM_FileSystem.CompressionMethod
- CIM_FileSystem.CreationClassName
- CIM_FileSystem.CSCreationClassName
- CIM_FileSystem.CSName
- CIM_FileSystem.EncryptionMethod
- CIM_FileSystem.FileSystemSize
- CIM_FileSystem.MaxFileNameLength
- CIM_FileSystem.ReadOnly
- CIM_FileSystem.Root
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2795e76c686e8f2bb4079aee376dae397b36f510
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861254"
---
# <a name="cim_filesystem-class"></a><span data-ttu-id="32aa3-103">\_Classe de système de fichiers CIM</span><span class="sxs-lookup"><span data-stu-id="32aa3-103">CIM\_FileSystem class</span></span>

<span data-ttu-id="32aa3-104">La classe de système de **\_ fichiers CIM** représente un fichier ou un jeu de données local sur un système informatique ou monté à distance à partir d’un serveur de fichiers.</span><span class="sxs-lookup"><span data-stu-id="32aa3-104">The **CIM\_FileSystem** class represents a file or data set local to a computer system or remotely mounted from a file server.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="32aa3-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="32aa3-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="32aa3-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="32aa3-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="32aa3-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="32aa3-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="32aa3-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="32aa3-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="32aa3-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="32aa3-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{4DA18760-E3D0-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_FileSystem : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint64   AvailableSpace;
  uint64   BlockSize;
  boolean  CasePreserved;
  boolean  CaseSensitive;
  uint16   CodeSet[];
  string   CompressionMethod;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  string   EncryptionMethod;
  uint64   FileSystemSize;
  uint32   MaxFileNameLength;
  boolean  ReadOnly;
  string   Root;
};
```

## <a name="members"></a><span data-ttu-id="32aa3-110">Membres</span><span class="sxs-lookup"><span data-stu-id="32aa3-110">Members</span></span>

<span data-ttu-id="32aa3-111">La classe de **\_ système de fichiers CIM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="32aa3-111">The **CIM\_FileSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="32aa3-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="32aa3-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="32aa3-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="32aa3-113">Properties</span></span>

<span data-ttu-id="32aa3-114">La classe de **\_ système de fichiers CIM** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="32aa3-114">The **CIM\_FileSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="32aa3-115">**AvailableSpace**</span><span class="sxs-lookup"><span data-stu-id="32aa3-115">**AvailableSpace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32aa3-116">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="32aa3-116">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="32aa3-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="32aa3-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32aa3-118">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Partition DMTF \| 002,4 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" octets ")</span><span class="sxs-lookup"><span data-stu-id="32aa3-118">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="32aa3-119">Quantité d’espace libre, en octets, pour le système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="32aa3-119">Amount of free space, in bytes, for the file system.</span></span> <span data-ttu-id="32aa3-120">S’il est inconnu, entrez 0.</span><span class="sxs-lookup"><span data-stu-id="32aa3-120">If unknown, enter 0.</span></span>

<span data-ttu-id="32aa3-121">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="32aa3-121">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="32aa3-122">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="32aa3-122">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32aa3-123">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="32aa3-123">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="32aa3-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="32aa3-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32aa3-125">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="32aa3-125">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="32aa3-126">Taille de bloc du système de fichiers pour le stockage et la récupération des données.</span><span class="sxs-lookup"><span data-stu-id="32aa3-126">Block size of the file system for data storage and retrieval.</span></span>

<span data-ttu-id="32aa3-127">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="32aa3-127">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="32aa3-128">**Caption**</span><span class="sxs-lookup"><span data-stu-id="32aa3-128">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32aa3-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="32aa3-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32aa3-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="32aa3-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32aa3-131">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="32aa3-131">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="32aa3-132">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="32aa3-132">A short textual description of the object.</span></span>

<span data-ttu-id="32aa3-133">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="32aa3-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="32aa3-134">**CasePreserved**</span><span class="sxs-lookup"><span data-stu-id="32aa3-134">**CasePreserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32aa3-135">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="32aa3-135">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="32aa3-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="32aa3-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32aa3-137">Si la **valeur est true**, la casse des noms de fichiers est conservée.</span><span class="sxs-lookup"><span data-stu-id="32aa3-137">If **TRUE**, the case of file names are preserved.</span></span>

</dd> <dt>

<span data-ttu-id="32aa3-138">**CaseSensitive**</span><span class="sxs-lookup"><span data-stu-id="32aa3-138">**CaseSensitive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32aa3-139">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="32aa3-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="32aa3-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="32aa3-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32aa3-141">Si la **valeur est true**, les noms de fichiers qui respectent la casse sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="32aa3-141">If **TRUE**, case-sensitive file names are supported.</span></span>

</dd> <dt>

<span data-ttu-id="32aa3-142">**Codes**</span><span class="sxs-lookup"><span data-stu-id="32aa3-142">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32aa3-143">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="32aa3-143">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="32aa3-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="32aa3-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32aa3-145">Tableau qui définit les jeux de caractères ou l’encodage pris en charge par le système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="32aa3-145">Array that defines the character sets or encoding supported by the file system.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="32aa3-146">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="32aa3-146">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="32aa3-147">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="32aa3-147">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="ASCII"></span><span id="ascii"></span>

<span data-ttu-id="32aa3-148">**ASCII** (2)</span><span class="sxs-lookup"><span data-stu-id="32aa3-148">**ASCII** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unicode"></span><span id="unicode"></span><span id="UNICODE"></span>

<span data-ttu-id="32aa3-149">**Unicode** (3)</span><span class="sxs-lookup"><span data-stu-id="32aa3-149">**Unicode** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO2022"></span><span id="iso2022"></span>

<span data-ttu-id="32aa3-150">**Iso2022** (4)</span><span class="sxs-lookup"><span data-stu-id="32aa3-150">**ISO2022** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO8859"></span><span id="iso8859"></span>

<span data-ttu-id="32aa3-151">**ISO8859** (5)</span><span class="sxs-lookup"><span data-stu-id="32aa3-151">**ISO8859** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Extended_UNIX_Code"></span><span id="extended_unix_code"></span><span id="EXTENDED_UNIX_CODE"></span>

<span data-ttu-id="32aa3-152">**Code UNIX étendu** (6)</span><span class="sxs-lookup"><span data-stu-id="32aa3-152">**Extended UNIX Code** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="UTF-8"></span><span id="utf-8"></span>

<span data-ttu-id="32aa3-153">**UTF-8** (7)</span><span class="sxs-lookup"><span data-stu-id="32aa3-153">**UTF-8** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="UCS-2"></span><span id="ucs-2"></span>

<span data-ttu-id="32aa3-154">**UCS-2** (8)</span><span class="sxs-lookup"><span data-stu-id="32aa3-154">**UCS-2** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="32aa3-155">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="32aa3-155">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32aa3-156">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="32aa3-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32aa3-157">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="32aa3-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32aa3-158">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Partition DMTF \| 002,7»)</span><span class="sxs-lookup"><span data-stu-id="32aa3-158">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="32aa3-159">Chaîne de forme libre qui indique l’algorithme ou l’outil utilisé pour compresser le fichier logique.</span><span class="sxs-lookup"><span data-stu-id="32aa3-159">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="32aa3-160">Si le schéma de compression est inconnu ou n’est pas décrit, utilisez « inconnu ».</span><span class="sxs-lookup"><span data-stu-id="32aa3-160">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="32aa3-161">Si le fichier logique est compressé, mais que le schéma de compression est inconnu ou non décrit, utilisez « compressé ».</span><span class="sxs-lookup"><span data-stu-id="32aa3-161">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="32aa3-162">Si le fichier logique n’est pas compressé, utilisez « non compressé ».</span><span class="sxs-lookup"><span data-stu-id="32aa3-162">If the logical file is not compressed, use "Not Compressed".</span></span>

</dd> <dt>

<span data-ttu-id="32aa3-163">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="32aa3-163">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32aa3-164">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="32aa3-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32aa3-165">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="32aa3-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32aa3-166">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="32aa3-166">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="32aa3-167">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="32aa3-167">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="32aa3-168">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="32aa3-168">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="32aa3-169">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="32aa3-169">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32aa3-170">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="32aa3-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32aa3-171">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="32aa3-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32aa3-172">Qualificateurs : [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**CreationClassName**»)</span><span class="sxs-lookup"><span data-stu-id="32aa3-172">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="32aa3-173">Portée du nom de la classe de création du système de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="32aa3-173">Scoping computer system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="32aa3-174">**CSName**</span><span class="sxs-lookup"><span data-stu-id="32aa3-174">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32aa3-175">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="32aa3-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32aa3-176">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="32aa3-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32aa3-177">Qualificateurs : [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Name**»)</span><span class="sxs-lookup"><span data-stu-id="32aa3-177">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="32aa3-178">Nom du système d’ordinateur d’étendue.</span><span class="sxs-lookup"><span data-stu-id="32aa3-178">Scoping computer system's name.</span></span>

</dd> <dt>

<span data-ttu-id="32aa3-179">**Description**</span><span class="sxs-lookup"><span data-stu-id="32aa3-179">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32aa3-180">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="32aa3-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32aa3-181">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="32aa3-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32aa3-182">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="32aa3-182">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="32aa3-183">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="32aa3-183">A textual description of the object.</span></span>

<span data-ttu-id="32aa3-184">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="32aa3-184">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="32aa3-185">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="32aa3-185">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32aa3-186">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="32aa3-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32aa3-187">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="32aa3-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32aa3-188">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Partition DMTF \| 002,8»)</span><span class="sxs-lookup"><span data-stu-id="32aa3-188">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.8")</span></span>
</dt> </dl>

<span data-ttu-id="32aa3-189">Chaîne de forme libre qui identifie l’algorithme ou l’outil utilisé pour chiffrer un fichier logique.</span><span class="sxs-lookup"><span data-stu-id="32aa3-189">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="32aa3-190">Si le schéma de chiffrement n’est pas indulged (pour des raisons de sécurité, par exemple), utilisez « inconnu ».</span><span class="sxs-lookup"><span data-stu-id="32aa3-190">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="32aa3-191">Si le fichier est chiffré, mais que son schéma de chiffrement est inconnu ou non divulgué, utilisez « chiffré ».</span><span class="sxs-lookup"><span data-stu-id="32aa3-191">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="32aa3-192">Si le fichier logique n’est pas chiffré, utilisez « non chiffré ».</span><span class="sxs-lookup"><span data-stu-id="32aa3-192">If the logical file is not encrypted, use "Not Encrypted".</span></span>

</dd> <dt>

<span data-ttu-id="32aa3-193">**FileSystemSize**</span><span class="sxs-lookup"><span data-stu-id="32aa3-193">**FileSystemSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32aa3-194">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="32aa3-194">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="32aa3-195">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="32aa3-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32aa3-196">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="32aa3-196">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="32aa3-197">Taille du système de fichiers, en octets.</span><span class="sxs-lookup"><span data-stu-id="32aa3-197">Size of the file system, in bytes.</span></span> <span data-ttu-id="32aa3-198">S’il est inconnu, entrez 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="32aa3-198">If unknown, enter 0 (zero).</span></span>

<span data-ttu-id="32aa3-199">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="32aa3-199">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="32aa3-200">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="32aa3-200">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32aa3-201">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="32aa3-201">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="32aa3-202">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="32aa3-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32aa3-203">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="32aa3-203">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="32aa3-204">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="32aa3-204">Indicates when the object was installed.</span></span> <span data-ttu-id="32aa3-205">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="32aa3-205">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="32aa3-206">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="32aa3-206">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="32aa3-207">**MaxFileNameLength**</span><span class="sxs-lookup"><span data-stu-id="32aa3-207">**MaxFileNameLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32aa3-208">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="32aa3-208">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="32aa3-209">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="32aa3-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32aa3-210">Longueur maximale d’un nom de fichier dans le système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="32aa3-210">Maximum length of a file name within the file system.</span></span> <span data-ttu-id="32aa3-211">La valeur 0 (zéro) indique qu’il n’existe aucune limite à la longueur du nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="32aa3-211">A value of 0 (zero) indicates that there is no limit to the file name length.</span></span>

</dd> <dt>

<span data-ttu-id="32aa3-212">**Nom**</span><span class="sxs-lookup"><span data-stu-id="32aa3-212">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32aa3-213">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="32aa3-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32aa3-214">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="32aa3-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32aa3-215">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="32aa3-215">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="32aa3-216">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="32aa3-216">Label by which the object is known.</span></span> <span data-ttu-id="32aa3-217">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="32aa3-217">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="32aa3-218">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="32aa3-218">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="32aa3-219">**Lecture seule**</span><span class="sxs-lookup"><span data-stu-id="32aa3-219">**ReadOnly**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32aa3-220">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="32aa3-220">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="32aa3-221">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="32aa3-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32aa3-222">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Hôte IETF-ressources-MIB. hrFSAccess ")</span><span class="sxs-lookup"><span data-stu-id="32aa3-222">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrFSAccess")</span></span>
</dt> </dl>

<span data-ttu-id="32aa3-223">Si la **valeur est true**, le système de fichiers est désigné comme étant en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="32aa3-223">If **TRUE**, the file system is designated as read only.</span></span>

</dd> <dt>

<span data-ttu-id="32aa3-224">**Causes**</span><span class="sxs-lookup"><span data-stu-id="32aa3-224">**Root**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32aa3-225">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="32aa3-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32aa3-226">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="32aa3-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32aa3-227">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Hôte IETF-ressources-MIB. hrFSMountPoint ")</span><span class="sxs-lookup"><span data-stu-id="32aa3-227">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrFSMountPoint")</span></span>
</dt> </dl>

<span data-ttu-id="32aa3-228">Nom de chemin d’accès ou d’autres informations qui définissent la racine du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="32aa3-228">Path name or other information that defines the root of the file system.</span></span>

</dd> <dt>

<span data-ttu-id="32aa3-229">**État**</span><span class="sxs-lookup"><span data-stu-id="32aa3-229">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32aa3-230">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="32aa3-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32aa3-231">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="32aa3-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32aa3-232">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="32aa3-232">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="32aa3-233">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="32aa3-233">String that indicates the current status of the object.</span></span> <span data-ttu-id="32aa3-234">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="32aa3-234">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="32aa3-235">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="32aa3-235">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="32aa3-236">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="32aa3-236">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="32aa3-237">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="32aa3-237">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="32aa3-238">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="32aa3-238">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="32aa3-239">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="32aa3-239">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="32aa3-240">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="32aa3-240">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="32aa3-241">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="32aa3-241">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="32aa3-242">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="32aa3-242">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="32aa3-243">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="32aa3-243">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="32aa3-244">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="32aa3-244">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="32aa3-245">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="32aa3-245">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="32aa3-246">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="32aa3-246">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="32aa3-247">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="32aa3-247">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="32aa3-248">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="32aa3-248">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="32aa3-249">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="32aa3-249">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="32aa3-250">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="32aa3-250">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="32aa3-251">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="32aa3-251">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="32aa3-252">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="32aa3-252">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="32aa3-253">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="32aa3-253">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="32aa3-254"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="32aa3-254"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="32aa3-255">Notes</span><span class="sxs-lookup"><span data-stu-id="32aa3-255">Remarks</span></span>

<span data-ttu-id="32aa3-256">La classe de **\_ système de fichiers CIM** est dérivée de [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="32aa3-256">The **CIM\_FileSystem** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="32aa3-257">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="32aa3-257">WMI does not implement this class.</span></span>

<span data-ttu-id="32aa3-258">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="32aa3-258">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="32aa3-259">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="32aa3-259">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="32aa3-260">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="32aa3-260">Requirements</span></span>



| <span data-ttu-id="32aa3-261">Condition requise</span><span class="sxs-lookup"><span data-stu-id="32aa3-261">Requirement</span></span> | <span data-ttu-id="32aa3-262">Valeur</span><span class="sxs-lookup"><span data-stu-id="32aa3-262">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="32aa3-263">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="32aa3-263">Minimum supported client</span></span><br/> | <span data-ttu-id="32aa3-264">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="32aa3-264">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="32aa3-265">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="32aa3-265">Minimum supported server</span></span><br/> | <span data-ttu-id="32aa3-266">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="32aa3-266">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="32aa3-267">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="32aa3-267">Namespace</span></span><br/>                | <span data-ttu-id="32aa3-268">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="32aa3-268">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="32aa3-269">MOF</span><span class="sxs-lookup"><span data-stu-id="32aa3-269">MOF</span></span><br/>                      | <dl> <span data-ttu-id="32aa3-270"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="32aa3-270"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="32aa3-271">DLL</span><span class="sxs-lookup"><span data-stu-id="32aa3-271">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32aa3-272"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32aa3-272"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32aa3-273">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="32aa3-273">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32aa3-274">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="32aa3-274">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

