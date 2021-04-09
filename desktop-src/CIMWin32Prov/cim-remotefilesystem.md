---
description: La \_ classe CIM RemoteFileSystem représente un système de fichiers distant accessible par le biais d’un service lié au réseau. Dans ce cas, le magasin de fichiers est hébergé par un ordinateur qui joue le rôle de serveur de fichiers.
ms.assetid: 932970a8-0ab3-45d8-912d-c4ba7cf433b5
ms.tgt_platform: multiple
title: Classe CIM_RemoteFileSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RemoteFileSystem
- CIM_RemoteFileSystem.AvailableSpace
- CIM_RemoteFileSystem.BlockSize
- CIM_RemoteFileSystem.Caption
- CIM_RemoteFileSystem.CasePreserved
- CIM_RemoteFileSystem.CaseSensitive
- CIM_RemoteFileSystem.CodeSet
- CIM_RemoteFileSystem.CompressionMethod
- CIM_RemoteFileSystem.CreationClassName
- CIM_RemoteFileSystem.CSCreationClassName
- CIM_RemoteFileSystem.CSName
- CIM_RemoteFileSystem.Description
- CIM_RemoteFileSystem.EncryptionMethod
- CIM_RemoteFileSystem.FileSystemSize
- CIM_RemoteFileSystem.InstallDate
- CIM_RemoteFileSystem.MaxFileNameLength
- CIM_RemoteFileSystem.Name
- CIM_RemoteFileSystem.ReadOnly
- CIM_RemoteFileSystem.Root
- CIM_RemoteFileSystem.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7c29e0212ba55b37abd734fb149d118ccc693908
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110258"
---
# <a name="cim_remotefilesystem-class"></a><span data-ttu-id="6b676-104">\_Classe CIM RemoteFileSystem</span><span class="sxs-lookup"><span data-stu-id="6b676-104">CIM\_RemoteFileSystem class</span></span>

<span data-ttu-id="6b676-105">La classe **CIM \_ RemoteFileSystem** représente un système de fichiers distant accessible par le biais d’un service lié au réseau.</span><span class="sxs-lookup"><span data-stu-id="6b676-105">The **CIM\_RemoteFileSystem** class represents a remote file system that is accessed by way of a network-related service.</span></span> <span data-ttu-id="6b676-106">Dans ce cas, le magasin de fichiers est hébergé par un ordinateur qui joue le rôle de serveur de fichiers.</span><span class="sxs-lookup"><span data-stu-id="6b676-106">In this case, the file store is hosted by a computer, which acts as a file server.</span></span> <span data-ttu-id="6b676-107">Par exemple, le magasin de fichiers pour un système de fichiers NFS n’est généralement pas sur un support contrôlé localement d’un ordinateur, et n’est pas directement accessible par le biais d’un pilote de périphérique.</span><span class="sxs-lookup"><span data-stu-id="6b676-107">For example, the file store for an NFS file system is typically not on a computer system's locally controlled media, nor is it directly accessed through a device driver.</span></span> <span data-ttu-id="6b676-108">Les sous-classes **de \_ RemoteFileSystem CIM** contiennent des informations de configuration côté client relatives à l’accès du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="6b676-108">Subclasses of **CIM\_RemoteFileSystem** contain client-side configuration information related to the access of the file system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6b676-109">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="6b676-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6b676-110">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6b676-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="6b676-111">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="6b676-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="6b676-112">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="6b676-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b676-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6b676-113">Syntax</span></span>

``` syntax
[Abstract, UUID("{75BCF4F9-DB46-11D2-B4C8-80080C7B6371}"), AMENDMENT]
class CIM_RemoteFileSystem : CIM_FileSystem
{
  uint64   AvailableSpace;
  uint64   BlockSize;
  string   Caption;
  boolean  CasePreserved;
  boolean  CaseSensitive;
  uint16   CodeSet[];
  string   CompressionMethod;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  string   EncryptionMethod;
  uint64   FileSystemSize;
  datetime InstallDate;
  uint32   MaxFileNameLength;
  string   Name;
  boolean  ReadOnly;
  string   Root;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="6b676-114">Membres</span><span class="sxs-lookup"><span data-stu-id="6b676-114">Members</span></span>

<span data-ttu-id="6b676-115">La classe **CIM \_ RemoteFileSystem** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="6b676-115">The **CIM\_RemoteFileSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="6b676-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6b676-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6b676-117">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6b676-117">Properties</span></span>

<span data-ttu-id="6b676-118">La classe **CIM \_ RemoteFileSystem** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="6b676-118">The **CIM\_RemoteFileSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6b676-119">**AvailableSpace**</span><span class="sxs-lookup"><span data-stu-id="6b676-119">**AvailableSpace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b676-120">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6b676-120">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6b676-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6b676-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b676-122">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Partition DMTF \| 002,4 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" octets ")</span><span class="sxs-lookup"><span data-stu-id="6b676-122">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="6b676-123">Quantité d’espace libre pour le système de fichiers, en octets.</span><span class="sxs-lookup"><span data-stu-id="6b676-123">Amount of free space for the file system, in bytes.</span></span> <span data-ttu-id="6b676-124">S’il est inconnu, entrez 0.</span><span class="sxs-lookup"><span data-stu-id="6b676-124">If unknown, enter 0.</span></span>

<span data-ttu-id="6b676-125">Cette propriété est héritée [**du \_ système de fichiers CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="6b676-125">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<span data-ttu-id="6b676-126">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="6b676-126">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="6b676-127">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="6b676-127">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b676-128">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6b676-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6b676-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6b676-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b676-130">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="6b676-130">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="6b676-131">Taille, en octets, des blocs qui forment l’extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="6b676-131">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="6b676-132">S’il est inconnu, ou si un concept de bloc n’est pas valide (par exemple, pour les extensions d’agrégat, la mémoire ou les disques logiques), entrez 1 (un).</span><span class="sxs-lookup"><span data-stu-id="6b676-132">If unknown, or if a block concept is not valid, (for example, for aggregate extents, memory, or logical disks), enter a 1 (one).</span></span>

<span data-ttu-id="6b676-133">Cette propriété est héritée [**du \_ système de fichiers CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="6b676-133">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<span data-ttu-id="6b676-134">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="6b676-134">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="6b676-135">**Caption**</span><span class="sxs-lookup"><span data-stu-id="6b676-135">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b676-136">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6b676-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b676-137">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6b676-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b676-138">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="6b676-138">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="6b676-139">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6b676-139">Textual description of the object.</span></span>

<span data-ttu-id="6b676-140">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6b676-140">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b676-141">**CasePreserved**</span><span class="sxs-lookup"><span data-stu-id="6b676-141">**CasePreserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b676-142">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="6b676-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6b676-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6b676-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b676-144">Si la **valeur est true**, la casse des noms de fichiers est conservée.</span><span class="sxs-lookup"><span data-stu-id="6b676-144">If **TRUE**, the case of file names are preserved.</span></span>

<span data-ttu-id="6b676-145">Cette propriété est héritée [**du \_ système de fichiers CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="6b676-145">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b676-146">**CaseSensitive**</span><span class="sxs-lookup"><span data-stu-id="6b676-146">**CaseSensitive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b676-147">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="6b676-147">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6b676-148">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6b676-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b676-149">Si la **valeur est true**, les noms de fichiers qui respectent la casse sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="6b676-149">If **TRUE**, case-sensitive file names are supported.</span></span>

<span data-ttu-id="6b676-150">Cette propriété est héritée [**du \_ système de fichiers CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="6b676-150">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b676-151">**Codes**</span><span class="sxs-lookup"><span data-stu-id="6b676-151">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b676-152">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6b676-152">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="6b676-153">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6b676-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b676-154">Jeux de caractères ou encodage pris en charge par le système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="6b676-154">Character sets or encoding supported by the file system.</span></span> <span data-ttu-id="6b676-155">Cette propriété est héritée [**du \_ système de fichiers CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="6b676-155">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6b676-156">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="6b676-156">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6b676-157">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="6b676-157">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="ASCII"></span><span id="ascii"></span>

<span data-ttu-id="6b676-158">**ASCII** (2)</span><span class="sxs-lookup"><span data-stu-id="6b676-158">**ASCII** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unicode"></span><span id="unicode"></span><span id="UNICODE"></span>

<span data-ttu-id="6b676-159">**Unicode** (3)</span><span class="sxs-lookup"><span data-stu-id="6b676-159">**Unicode** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO2022"></span><span id="iso2022"></span>

<span data-ttu-id="6b676-160">**Iso2022** (4)</span><span class="sxs-lookup"><span data-stu-id="6b676-160">**ISO2022** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO8859"></span><span id="iso8859"></span>

<span data-ttu-id="6b676-161">**ISO8859** (5)</span><span class="sxs-lookup"><span data-stu-id="6b676-161">**ISO8859** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Extended_UNIX_Code"></span><span id="extended_unix_code"></span><span id="EXTENDED_UNIX_CODE"></span>

<span data-ttu-id="6b676-162">**Code UNIX étendu** (6)</span><span class="sxs-lookup"><span data-stu-id="6b676-162">**Extended UNIX Code** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="UTF-8"></span><span id="utf-8"></span>

<span data-ttu-id="6b676-163">**UTF-8** (7)</span><span class="sxs-lookup"><span data-stu-id="6b676-163">**UTF-8** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="UCS-2"></span><span id="ucs-2"></span>

<span data-ttu-id="6b676-164">**UCS-2** (8)</span><span class="sxs-lookup"><span data-stu-id="6b676-164">**UCS-2** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6b676-165">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="6b676-165">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b676-166">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6b676-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b676-167">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6b676-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b676-168">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Partition DMTF \| 002,7»)</span><span class="sxs-lookup"><span data-stu-id="6b676-168">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="6b676-169">Chaîne de forme libre qui indique l’algorithme ou l’outil utilisé pour compresser le fichier logique.</span><span class="sxs-lookup"><span data-stu-id="6b676-169">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="6b676-170">Si le schéma de compression est inconnu ou n’est pas décrit, utilisez « inconnu ».</span><span class="sxs-lookup"><span data-stu-id="6b676-170">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="6b676-171">Si le fichier logique est compressé, mais que le schéma de compression est inconnu ou non décrit, utilisez « compressé ».</span><span class="sxs-lookup"><span data-stu-id="6b676-171">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="6b676-172">Si le fichier logique n’est pas compressé, utilisez « non compressé ».</span><span class="sxs-lookup"><span data-stu-id="6b676-172">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="6b676-173">Cette propriété est héritée [**du \_ système de fichiers CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="6b676-173">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b676-174">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="6b676-174">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b676-175">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6b676-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b676-176">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6b676-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b676-177">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="6b676-177">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="6b676-178">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="6b676-178">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="6b676-179">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="6b676-179">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="6b676-180">Cette propriété est héritée [**du \_ système de fichiers CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="6b676-180">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b676-181">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="6b676-181">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b676-182">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6b676-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b676-183">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6b676-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b676-184">Qualificateurs : [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**CreationClassName**»)</span><span class="sxs-lookup"><span data-stu-id="6b676-184">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="6b676-185">Portée du nom de la classe de création du système de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="6b676-185">Scoping computer system's creation class name.</span></span>

<span data-ttu-id="6b676-186">Cette propriété est héritée [**du \_ système de fichiers CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="6b676-186">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b676-187">**CSName**</span><span class="sxs-lookup"><span data-stu-id="6b676-187">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b676-188">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6b676-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b676-189">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6b676-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b676-190">Qualificateurs : [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Name**»)</span><span class="sxs-lookup"><span data-stu-id="6b676-190">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="6b676-191">Nom du système d’ordinateur d’étendue.</span><span class="sxs-lookup"><span data-stu-id="6b676-191">Scoping computer system's name.</span></span>

<span data-ttu-id="6b676-192">Cette propriété est héritée [**du \_ système de fichiers CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="6b676-192">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b676-193">**Description**</span><span class="sxs-lookup"><span data-stu-id="6b676-193">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b676-194">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6b676-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b676-195">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6b676-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b676-196">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="6b676-196">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="6b676-197">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6b676-197">Textual description of the object.</span></span>

<span data-ttu-id="6b676-198">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6b676-198">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b676-199">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="6b676-199">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b676-200">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6b676-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b676-201">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6b676-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b676-202">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Partition DMTF \| 002,8»)</span><span class="sxs-lookup"><span data-stu-id="6b676-202">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.8")</span></span>
</dt> </dl>

<span data-ttu-id="6b676-203">Chaîne de forme libre qui identifie l’algorithme ou l’outil utilisé pour chiffrer un fichier logique.</span><span class="sxs-lookup"><span data-stu-id="6b676-203">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="6b676-204">Si le schéma de chiffrement n’est pas indulged (pour des raisons de sécurité, par exemple), utilisez « inconnu ».</span><span class="sxs-lookup"><span data-stu-id="6b676-204">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="6b676-205">Si le fichier est chiffré, mais que son schéma de chiffrement est inconnu ou non divulgué, utilisez « chiffré ».</span><span class="sxs-lookup"><span data-stu-id="6b676-205">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="6b676-206">Si le fichier logique n’est pas chiffré, utilisez « non chiffré ».</span><span class="sxs-lookup"><span data-stu-id="6b676-206">If the logical file is not encrypted, use "Not Encrypted".</span></span> <span data-ttu-id="6b676-207">Cette propriété est héritée [**du \_ système de fichiers CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="6b676-207">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b676-208">**FileSystemSize**</span><span class="sxs-lookup"><span data-stu-id="6b676-208">**FileSystemSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b676-209">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6b676-209">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6b676-210">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6b676-210">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b676-211">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="6b676-211">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="6b676-212">Taille totale du système de fichiers, en octets.</span><span class="sxs-lookup"><span data-stu-id="6b676-212">Total size of the file system, in bytes.</span></span> <span data-ttu-id="6b676-213">S’il est inconnu, entrez 0.</span><span class="sxs-lookup"><span data-stu-id="6b676-213">If unknown, enter 0.</span></span>

<span data-ttu-id="6b676-214">Cette propriété est héritée [**du \_ système de fichiers CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="6b676-214">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<span data-ttu-id="6b676-215">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="6b676-215">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="6b676-216">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="6b676-216">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b676-217">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6b676-217">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6b676-218">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6b676-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b676-219">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="6b676-219">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="6b676-220">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6b676-220">Date and time the object was installed.</span></span> <span data-ttu-id="6b676-221">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="6b676-221">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="6b676-222">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6b676-222">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b676-223">**MaxFileNameLength**</span><span class="sxs-lookup"><span data-stu-id="6b676-223">**MaxFileNameLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b676-224">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6b676-224">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6b676-225">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6b676-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b676-226">Longueur maximale d’un nom de fichier dans le système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="6b676-226">Maximum length of a file name within the file system.</span></span> <span data-ttu-id="6b676-227">La valeur 0 indique que la longueur du nom de fichier est illimitée.</span><span class="sxs-lookup"><span data-stu-id="6b676-227">A value of 0 indicates that file name length is unlimited.</span></span>

<span data-ttu-id="6b676-228">Cette propriété est héritée [**du \_ système de fichiers CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="6b676-228">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b676-229">**Nom**</span><span class="sxs-lookup"><span data-stu-id="6b676-229">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b676-230">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6b676-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b676-231">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6b676-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b676-232">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="6b676-232">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="6b676-233">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="6b676-233">Label by which the object is known.</span></span> <span data-ttu-id="6b676-234">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="6b676-234">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="6b676-235">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6b676-235">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b676-236">**Lecture seule**</span><span class="sxs-lookup"><span data-stu-id="6b676-236">**ReadOnly**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b676-237">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="6b676-237">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6b676-238">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6b676-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b676-239">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Hôte IETF-ressources-MIB. hrFSAccess ")</span><span class="sxs-lookup"><span data-stu-id="6b676-239">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrFSAccess")</span></span>
</dt> </dl>

<span data-ttu-id="6b676-240">Si la **valeur est true**, le système de fichiers est désigné comme étant en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="6b676-240">If **TRUE**, the file system is designated as read-only.</span></span>

<span data-ttu-id="6b676-241">Cette propriété est héritée [**du \_ système de fichiers CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="6b676-241">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b676-242">**Causes**</span><span class="sxs-lookup"><span data-stu-id="6b676-242">**Root**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b676-243">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6b676-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b676-244">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6b676-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b676-245">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Hôte IETF-ressources-MIB. hrFSMountPoint ")</span><span class="sxs-lookup"><span data-stu-id="6b676-245">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrFSMountPoint")</span></span>
</dt> </dl>

<span data-ttu-id="6b676-246">Nom de chemin d’accès ou d’autres informations qui définissent la racine du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="6b676-246">Path name or other information that defines the root of the file system.</span></span>

<span data-ttu-id="6b676-247">Cette propriété est héritée [**du \_ système de fichiers CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="6b676-247">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b676-248">**État**</span><span class="sxs-lookup"><span data-stu-id="6b676-248">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b676-249">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6b676-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b676-250">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6b676-250">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b676-251">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="6b676-251">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="6b676-252">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6b676-252">Current status of the object.</span></span>

<span data-ttu-id="6b676-253">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6b676-253">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="6b676-254">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="6b676-254">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="6b676-255">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="6b676-255">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="6b676-256">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="6b676-256">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="6b676-257">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="6b676-257">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6b676-258">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="6b676-258">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="6b676-259">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="6b676-259">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="6b676-260">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="6b676-260">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="6b676-261">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="6b676-261">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="6b676-262">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="6b676-262">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="6b676-263">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="6b676-263">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="6b676-264">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="6b676-264">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="6b676-265">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="6b676-265">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="6b676-266">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="6b676-266">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="6b676-267"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="6b676-267"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="6b676-268">Notes</span><span class="sxs-lookup"><span data-stu-id="6b676-268">Remarks</span></span>

<span data-ttu-id="6b676-269">La classe **CIM \_ RemoteFileSystem** est dérivée du [**système de \_ fichiers CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="6b676-269">The **CIM\_RemoteFileSystem** class is derived from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<span data-ttu-id="6b676-270">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="6b676-270">WMI does not implement this class.</span></span>

<span data-ttu-id="6b676-271">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="6b676-271">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6b676-272">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="6b676-272">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b676-273">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6b676-273">Requirements</span></span>



| <span data-ttu-id="6b676-274">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6b676-274">Requirement</span></span> | <span data-ttu-id="6b676-275">Valeur</span><span class="sxs-lookup"><span data-stu-id="6b676-275">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b676-276">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6b676-276">Minimum supported client</span></span><br/> | <span data-ttu-id="6b676-277">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6b676-277">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6b676-278">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6b676-278">Minimum supported server</span></span><br/> | <span data-ttu-id="6b676-279">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6b676-279">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6b676-280">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6b676-280">Namespace</span></span><br/>                | <span data-ttu-id="6b676-281">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="6b676-281">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6b676-282">MOF</span><span class="sxs-lookup"><span data-stu-id="6b676-282">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6b676-283"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6b676-283"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6b676-284">DLL</span><span class="sxs-lookup"><span data-stu-id="6b676-284">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b676-285"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b676-285"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b676-286">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6b676-286">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b676-287">**\_Système de fichiers CIM**</span><span class="sxs-lookup"><span data-stu-id="6b676-287">**CIM\_FileSystem**</span></span>](cim-filesystem.md)
</dt> </dl>

 

