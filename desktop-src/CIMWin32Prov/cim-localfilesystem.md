---
description: La \_ classe CIM LocalFileSystem représente le magasin de fichiers contrôlé par un système informatique par le biais de moyens locaux (par exemple, accès direct au pilote de l’appareil).
ms.assetid: eab52a25-ca24-4a69-b030-091603d3582c
ms.tgt_platform: multiple
title: Classe CIM_LocalFileSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LocalFileSystem
- CIM_LocalFileSystem.Caption
- CIM_LocalFileSystem.Description
- CIM_LocalFileSystem.InstallDate
- CIM_LocalFileSystem.Name
- CIM_LocalFileSystem.Status
- CIM_LocalFileSystem.AvailableSpace
- CIM_LocalFileSystem.BlockSize
- CIM_LocalFileSystem.CasePreserved
- CIM_LocalFileSystem.CaseSensitive
- CIM_LocalFileSystem.CodeSet
- CIM_LocalFileSystem.CompressionMethod
- CIM_LocalFileSystem.CreationClassName
- CIM_LocalFileSystem.CSCreationClassName
- CIM_LocalFileSystem.CSName
- CIM_LocalFileSystem.EncryptionMethod
- CIM_LocalFileSystem.FileSystemSize
- CIM_LocalFileSystem.MaxFileNameLength
- CIM_LocalFileSystem.ReadOnly
- CIM_LocalFileSystem.Root
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6a4a45541a651c92b45baba70828ba99c911d59a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861237"
---
# <a name="cim_localfilesystem-class"></a><span data-ttu-id="2d319-103">\_Classe CIM LocalFileSystem</span><span class="sxs-lookup"><span data-stu-id="2d319-103">CIM\_LocalFileSystem class</span></span>

<span data-ttu-id="2d319-104">La classe **CIM \_ LocalFileSystem** représente le magasin de fichiers contrôlé par un système informatique par le biais de moyens locaux (par exemple, accès direct au pilote de l’appareil).</span><span class="sxs-lookup"><span data-stu-id="2d319-104">The **CIM\_LocalFileSystem** class represents the file store controlled by a computer system through local means (for example, direct device-driver access).</span></span> <span data-ttu-id="2d319-105">Le magasin de fichiers peut être géré directement par le système informatique, sans qu’un autre ordinateur n’ait besoin d’agir en tant que serveur de fichiers.</span><span class="sxs-lookup"><span data-stu-id="2d319-105">The file store can be managed directly by the computer system, without the need for another computer to act as a file server.</span></span> <span data-ttu-id="2d319-106">Dans le cas d’un système de fichiers en cluster, toutefois, le système de fichiers est local et, par conséquent, diffère du cluster.</span><span class="sxs-lookup"><span data-stu-id="2d319-106">For a clustered file system, however, the file system is local and, therefore, defers to the cluster.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2d319-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="2d319-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2d319-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="2d319-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2d319-109">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="2d319-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="2d319-110">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="2d319-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d319-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2d319-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{5B6C820A-E3D0-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_LocalFileSystem : CIM_FileSystem
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

## <a name="members"></a><span data-ttu-id="2d319-112">Membres</span><span class="sxs-lookup"><span data-stu-id="2d319-112">Members</span></span>

<span data-ttu-id="2d319-113">La classe **CIM \_ LocalFileSystem** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="2d319-113">The **CIM\_LocalFileSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="2d319-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2d319-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2d319-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2d319-115">Properties</span></span>

<span data-ttu-id="2d319-116">La classe **CIM \_ LocalFileSystem** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="2d319-116">The **CIM\_LocalFileSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2d319-117">**AvailableSpace**</span><span class="sxs-lookup"><span data-stu-id="2d319-117">**AvailableSpace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d319-118">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2d319-118">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2d319-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d319-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d319-120">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Partition DMTF \| 002,4 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" octets ")</span><span class="sxs-lookup"><span data-stu-id="2d319-120">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="2d319-121">Quantité d’espace libre, en octets, pour le système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="2d319-121">Amount of free space, in bytes, for the file system.</span></span> <span data-ttu-id="2d319-122">S’il est inconnu, entrez 0.</span><span class="sxs-lookup"><span data-stu-id="2d319-122">If unknown, enter 0.</span></span>

<span data-ttu-id="2d319-123">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="2d319-123">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="2d319-124">Cette propriété est héritée [**du \_ système de fichiers CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="2d319-124">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="2d319-125">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="2d319-125">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d319-126">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2d319-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2d319-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d319-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d319-128">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="2d319-128">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="2d319-129">Taille de bloc du système de fichiers pour le stockage et la récupération des données.</span><span class="sxs-lookup"><span data-stu-id="2d319-129">Block size of the file system for data storage and retrieval.</span></span>

<span data-ttu-id="2d319-130">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="2d319-130">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="2d319-131">Cette propriété est héritée [**du \_ système de fichiers CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="2d319-131">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="2d319-132">**Caption**</span><span class="sxs-lookup"><span data-stu-id="2d319-132">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d319-133">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2d319-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d319-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d319-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d319-135">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="2d319-135">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="2d319-136">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="2d319-136">A short textual description of the object.</span></span>

<span data-ttu-id="2d319-137">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2d319-137">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2d319-138">**CasePreserved**</span><span class="sxs-lookup"><span data-stu-id="2d319-138">**CasePreserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d319-139">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="2d319-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2d319-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d319-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d319-141">Si la **valeur est true**, la casse des noms de fichiers est conservée.</span><span class="sxs-lookup"><span data-stu-id="2d319-141">If **TRUE**, the case of file names are preserved.</span></span>

<span data-ttu-id="2d319-142">Cette propriété est héritée [**du \_ système de fichiers CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="2d319-142">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="2d319-143">**CaseSensitive**</span><span class="sxs-lookup"><span data-stu-id="2d319-143">**CaseSensitive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d319-144">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="2d319-144">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2d319-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d319-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d319-146">Si la **valeur est true**, les noms de fichiers qui respectent la casse sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="2d319-146">If **TRUE**, case-sensitive file names are supported.</span></span>

<span data-ttu-id="2d319-147">Cette propriété est héritée [**du \_ système de fichiers CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="2d319-147">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="2d319-148">**Codes**</span><span class="sxs-lookup"><span data-stu-id="2d319-148">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d319-149">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2d319-149">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2d319-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d319-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d319-151">Tableau qui définit les jeux de caractères ou l’encodage pris en charge par le système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="2d319-151">Array that defines the character sets or encoding supported by the file system.</span></span>

<span data-ttu-id="2d319-152">Cette propriété est héritée [**du \_ système de fichiers CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="2d319-152">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2d319-153">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="2d319-153">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2d319-154">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="2d319-154">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="ASCII"></span><span id="ascii"></span>

<span data-ttu-id="2d319-155">**ASCII** (2)</span><span class="sxs-lookup"><span data-stu-id="2d319-155">**ASCII** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unicode"></span><span id="unicode"></span><span id="UNICODE"></span>

<span data-ttu-id="2d319-156">**Unicode** (3)</span><span class="sxs-lookup"><span data-stu-id="2d319-156">**Unicode** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO2022"></span><span id="iso2022"></span>

<span data-ttu-id="2d319-157">**Iso2022** (4)</span><span class="sxs-lookup"><span data-stu-id="2d319-157">**ISO2022** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO8859"></span><span id="iso8859"></span>

<span data-ttu-id="2d319-158">**ISO8859** (5)</span><span class="sxs-lookup"><span data-stu-id="2d319-158">**ISO8859** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Extended_UNIX_Code"></span><span id="extended_unix_code"></span><span id="EXTENDED_UNIX_CODE"></span>

<span data-ttu-id="2d319-159">**Code UNIX étendu** (6)</span><span class="sxs-lookup"><span data-stu-id="2d319-159">**Extended UNIX Code** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="UTF-8"></span><span id="utf-8"></span>

<span data-ttu-id="2d319-160">**UTF-8** (7)</span><span class="sxs-lookup"><span data-stu-id="2d319-160">**UTF-8** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="UCS-2"></span><span id="ucs-2"></span>

<span data-ttu-id="2d319-161">**UCS-2** (8)</span><span class="sxs-lookup"><span data-stu-id="2d319-161">**UCS-2** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2d319-162">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="2d319-162">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d319-163">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2d319-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d319-164">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d319-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d319-165">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Partition DMTF \| 002,7»)</span><span class="sxs-lookup"><span data-stu-id="2d319-165">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="2d319-166">Chaîne de forme libre qui indique l’algorithme ou l’outil utilisé pour compresser le fichier logique.</span><span class="sxs-lookup"><span data-stu-id="2d319-166">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="2d319-167">Si le schéma de compression est inconnu ou n’est pas décrit, utilisez « inconnu ».</span><span class="sxs-lookup"><span data-stu-id="2d319-167">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="2d319-168">Si le fichier logique est compressé, mais que le schéma de compression est inconnu ou non décrit, utilisez « compressé ».</span><span class="sxs-lookup"><span data-stu-id="2d319-168">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="2d319-169">Si le fichier logique n’est pas compressé, utilisez « non compressé ».</span><span class="sxs-lookup"><span data-stu-id="2d319-169">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="2d319-170">Cette propriété est héritée [**du \_ système de fichiers CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="2d319-170">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="2d319-171">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2d319-171">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d319-172">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2d319-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d319-173">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d319-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d319-174">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="2d319-174">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="2d319-175">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="2d319-175">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="2d319-176">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="2d319-176">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="2d319-177">Cette propriété est héritée [**du \_ système de fichiers CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="2d319-177">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="2d319-178">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2d319-178">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d319-179">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2d319-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d319-180">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d319-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d319-181">Qualificateurs : [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**CreationClassName**»)</span><span class="sxs-lookup"><span data-stu-id="2d319-181">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="2d319-182">Portée du nom de la classe de création du système de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="2d319-182">Scoping computer system's creation class name.</span></span>

<span data-ttu-id="2d319-183">Cette propriété est héritée [**du \_ système de fichiers CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="2d319-183">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="2d319-184">**CSName**</span><span class="sxs-lookup"><span data-stu-id="2d319-184">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d319-185">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2d319-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d319-186">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d319-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d319-187">Qualificateurs : [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Name**»)</span><span class="sxs-lookup"><span data-stu-id="2d319-187">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="2d319-188">Nom du système d’ordinateur d’étendue.</span><span class="sxs-lookup"><span data-stu-id="2d319-188">Scoping computer system's name.</span></span>

<span data-ttu-id="2d319-189">Cette propriété est héritée [**du \_ système de fichiers CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="2d319-189">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="2d319-190">**Description**</span><span class="sxs-lookup"><span data-stu-id="2d319-190">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d319-191">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2d319-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d319-192">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d319-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d319-193">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="2d319-193">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="2d319-194">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="2d319-194">A textual description of the object.</span></span>

<span data-ttu-id="2d319-195">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2d319-195">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2d319-196">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="2d319-196">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d319-197">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2d319-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d319-198">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d319-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d319-199">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Partition DMTF \| 002,8»)</span><span class="sxs-lookup"><span data-stu-id="2d319-199">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.8")</span></span>
</dt> </dl>

<span data-ttu-id="2d319-200">Chaîne de forme libre qui identifie l’algorithme ou l’outil utilisé pour chiffrer un fichier logique.</span><span class="sxs-lookup"><span data-stu-id="2d319-200">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="2d319-201">Si le schéma de chiffrement n’est pas indulged (pour des raisons de sécurité, par exemple), utilisez « inconnu ».</span><span class="sxs-lookup"><span data-stu-id="2d319-201">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="2d319-202">Si le fichier est chiffré, mais que son schéma de chiffrement est inconnu ou non divulgué, utilisez « chiffré ».</span><span class="sxs-lookup"><span data-stu-id="2d319-202">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="2d319-203">Si le fichier logique n’est pas chiffré, utilisez « non chiffré ».</span><span class="sxs-lookup"><span data-stu-id="2d319-203">If the logical file is not encrypted, use "Not Encrypted".</span></span>

<span data-ttu-id="2d319-204">Cette propriété est héritée [**du \_ système de fichiers CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="2d319-204">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="2d319-205">**FileSystemSize**</span><span class="sxs-lookup"><span data-stu-id="2d319-205">**FileSystemSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d319-206">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2d319-206">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2d319-207">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d319-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d319-208">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="2d319-208">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="2d319-209">Taille du système de fichiers, en octets.</span><span class="sxs-lookup"><span data-stu-id="2d319-209">Size of the file system, in bytes.</span></span> <span data-ttu-id="2d319-210">S’il est inconnu, entrez 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="2d319-210">If unknown, enter 0 (zero).</span></span>

<span data-ttu-id="2d319-211">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="2d319-211">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="2d319-212">Cette propriété est héritée [**du \_ système de fichiers CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="2d319-212">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="2d319-213">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="2d319-213">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d319-214">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2d319-214">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2d319-215">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d319-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d319-216">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="2d319-216">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="2d319-217">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="2d319-217">Indicates when the object was installed.</span></span> <span data-ttu-id="2d319-218">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="2d319-218">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="2d319-219">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2d319-219">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2d319-220">**MaxFileNameLength**</span><span class="sxs-lookup"><span data-stu-id="2d319-220">**MaxFileNameLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d319-221">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2d319-221">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2d319-222">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d319-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d319-223">Longueur maximale d’un nom de fichier dans le système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="2d319-223">Maximum length of a file name within the file system.</span></span> <span data-ttu-id="2d319-224">La valeur 0 (zéro) indique qu’il n’existe aucune limite à la longueur du nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="2d319-224">A value of 0 (zero) indicates that there is no limit to the file name length.</span></span>

<span data-ttu-id="2d319-225">Cette propriété est héritée [**du \_ système de fichiers CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="2d319-225">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="2d319-226">**Nom**</span><span class="sxs-lookup"><span data-stu-id="2d319-226">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d319-227">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2d319-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d319-228">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d319-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d319-229">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="2d319-229">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="2d319-230">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="2d319-230">Label by which the object is known.</span></span> <span data-ttu-id="2d319-231">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="2d319-231">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="2d319-232">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2d319-232">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2d319-233">**Lecture seule**</span><span class="sxs-lookup"><span data-stu-id="2d319-233">**ReadOnly**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d319-234">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="2d319-234">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2d319-235">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d319-235">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d319-236">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Hôte IETF-ressources-MIB. hrFSAccess ")</span><span class="sxs-lookup"><span data-stu-id="2d319-236">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrFSAccess")</span></span>
</dt> </dl>

<span data-ttu-id="2d319-237">Si la **valeur est true**, le système de fichiers est désigné comme étant en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="2d319-237">If **TRUE**, the file system is designated as read only.</span></span>

<span data-ttu-id="2d319-238">Cette propriété est héritée [**du \_ système de fichiers CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="2d319-238">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="2d319-239">**Causes**</span><span class="sxs-lookup"><span data-stu-id="2d319-239">**Root**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d319-240">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2d319-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d319-241">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d319-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d319-242">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Hôte IETF-ressources-MIB. hrFSMountPoint ")</span><span class="sxs-lookup"><span data-stu-id="2d319-242">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrFSMountPoint")</span></span>
</dt> </dl>

<span data-ttu-id="2d319-243">Nom de chemin d’accès ou d’autres informations qui définissent la racine du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="2d319-243">Path name or other information that defines the root of the file system.</span></span>

<span data-ttu-id="2d319-244">Cette propriété est héritée [**du \_ système de fichiers CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="2d319-244">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="2d319-245">**État**</span><span class="sxs-lookup"><span data-stu-id="2d319-245">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d319-246">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2d319-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d319-247">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d319-247">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d319-248">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="2d319-248">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="2d319-249">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="2d319-249">String that indicates the current status of the object.</span></span> <span data-ttu-id="2d319-250">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="2d319-250">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="2d319-251">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="2d319-251">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="2d319-252">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="2d319-252">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="2d319-253">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="2d319-253">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="2d319-254">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="2d319-254">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="2d319-255">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="2d319-255">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="2d319-256">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2d319-256">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="2d319-257">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="2d319-257">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="2d319-258">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="2d319-258">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="2d319-259">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="2d319-259">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="2d319-260">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="2d319-260">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2d319-261">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="2d319-261">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="2d319-262">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="2d319-262">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="2d319-263">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="2d319-263">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="2d319-264">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="2d319-264">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="2d319-265">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="2d319-265">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="2d319-266">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="2d319-266">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="2d319-267">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="2d319-267">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="2d319-268">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="2d319-268">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="2d319-269">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="2d319-269">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="2d319-270"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="2d319-270"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="2d319-271">Notes</span><span class="sxs-lookup"><span data-stu-id="2d319-271">Remarks</span></span>

<span data-ttu-id="2d319-272">La classe **CIM \_ LocalFileSystem** est dérivée du [**système de \_ fichiers CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="2d319-272">The **CIM\_LocalFileSystem** class is derived from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<span data-ttu-id="2d319-273">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="2d319-273">WMI does not implement this class.</span></span>

<span data-ttu-id="2d319-274">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="2d319-274">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2d319-275">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="2d319-275">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d319-276">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2d319-276">Requirements</span></span>



| <span data-ttu-id="2d319-277">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2d319-277">Requirement</span></span> | <span data-ttu-id="2d319-278">Valeur</span><span class="sxs-lookup"><span data-stu-id="2d319-278">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2d319-279">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2d319-279">Minimum supported client</span></span><br/> | <span data-ttu-id="2d319-280">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2d319-280">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2d319-281">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2d319-281">Minimum supported server</span></span><br/> | <span data-ttu-id="2d319-282">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2d319-282">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2d319-283">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2d319-283">Namespace</span></span><br/>                | <span data-ttu-id="2d319-284">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="2d319-284">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2d319-285">MOF</span><span class="sxs-lookup"><span data-stu-id="2d319-285">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2d319-286"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2d319-286"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2d319-287">DLL</span><span class="sxs-lookup"><span data-stu-id="2d319-287">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d319-288"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d319-288"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d319-289">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2d319-289">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d319-290">**\_Système de fichiers CIM**</span><span class="sxs-lookup"><span data-stu-id="2d319-290">**CIM\_FileSystem**</span></span>](cim-filesystem.md)
</dt> </dl>

 

